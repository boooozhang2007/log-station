---
title: FastAPI学习
date: 2026-02-13 20:47:51
tags:
  - Python
  - FastAPI

---

## 基础操作

### 路由

基本写法如下

```python
#导入fastapi库
from fastapi import FastAPI

#创建一个FastAPI对象
app = FastAPI()

#路由，访问时会执行下方函数
@app.get("/")
async def index():
    return {"message":"Welcome"}
```

### 发送参数

#### 路径参数Path()

```python
#导入fastapi库
from fastapi import FastAPI，Path

#创建一个FastAPI对象
app = FastAPI()

#路由，访问时会执行下方函数
#1.填入路径
@app.get("/{username}")
async def index(
    #2.路径与参数同名
	username: str = Path("root",min_length=2, max_length=10)
):
    return {"message":f"Welcome,{username}"}
```



#### 查询参数Query()

```python
#导入fastapi库
from fastapi import FastAPI,Query

#创建一个FastAPI对象
app = FastAPI()

#路由，访问时会执行下方函数
@app.get("/")#无需路径，使用?和＆传参
async def index(
    username: str = Query("root", min_length=2, max_length=10)#写法类似
):
    return {"message":f"Welcome,{username}"}
```



#### 请求体参数Field()

```python
#导入fastapi库
from fastapi import FastAPI
#从pydantic导入Field和BaseModel
from pydantic import BaseModel,Field

#创建一个FastAPI对象
app = FastAPI()

class User(BaseModel):
    username: str = Field("root", min_length=2, max_length=10)
	user_year: int = Field(..., gt=0)
    
#路由，访问时会执行下方函数
@app.get("/")#传入基类BaseModel
async def index(user:User):
    return {"message":"Welcome","information":user}
```



### 接收请求

#### json

默认返回即json格式

#### html

##### 装饰器指定响应类

```python
#导入fastapi库
from fastapi import FastAPI,Path
#从fastapi.response导入
from fastapi.response import HTMLResponse

#创建一个FastAPI对象
app = FastAPI()

#路由，访问时会执行下方函数
@app.get("/{username}", response_class = HTMLResponse)
async def index(username: str = Path(...)):
    return f"<h1>Welcome,{username}<h1>"
```



##### 返回响应对象

```python
#导入fastapi库
from fastapi import FastAPI,Path
#从fastapi.response导入
from fastapi.response import HTMLResponse

#创建一个FastAPI对象
app = FastAPI()

#路由，访问时会执行下方函数
@app.get("/{username}")
async def index(username: str = Path(...)):
    return HTMLResponse(f"<h1>Welcome,{username}<h1>")
```



#### file

```python
#导入fastapi库
from fastapi import FastAPI,Path
#从fastapi.response导入
from fastapi.response import FileResponse

#创建一个FastAPI对象
app = FastAPI()

#路由，访问时会执行下方函数
@app.get("/")
async def index():
    file_path = "./files/1.jpeg"
    return FileResponse(file_path)
```



#### 自定义响应

```python
#导入fastapi库
from fastapi import FastAPI
#从pydantic导入Field和BaseModel
from pydantic import BaseModel

#创建一个FastAPI对象
app = FastAPI()

class User(BaseModel):
    username: str
	user_year: int
    
#路由，访问时会执行下方函数
#指定response_model为User
@app.get("/", response_model = User)
async def index():
    #自动校验数据格式，保证安全
    return {
        "username" : "root",
        "user_year" : 1
    }
```



### 异常处理

使用HTTPException

```python
#导入fastapi库
from fastapi import FastAPI,HTTPException

#创建一个FastAPI对象
app = FastAPI()

#路由，访问时会执行下方函数
@app.get("/{id}")
async def index(id: int):
    ids = [1, 2, 3, 4, 5]
    if id not in ids:
    	raise HTTPException(status_code=404, detail="当前id不存在")
    return {"message":f"当前id是{id}"}
```

## 进阶

### 中间件

每个请求前、响应前均执行一次的代码，可以有多个中间件

```python
#导入fastapi库
from fastapi import FastAPI

#创建一个FastAPI对象
app = FastAPI()

#创建一个中间件，
@app.middleware("http")
async def middleware1(request, call_next):
    print("中间件1 开始")
    response = await call_next(request)
    print("中间件1 结束")
    #返回响应以继续执行
    return response
    
#路由，访问时会执行下方函数
@app.get("/")
async def index():
    return {"message":"Welcome"}
```



### 依赖注入

共享通用逻辑，减少重复

```python
#导入fastapi库
from fastapi import FastAPI,Depends,Query

#创建一个FastAPI对象
app = FastAPI()

#封装一个依赖项(函数)
async def common(
	page: int = Query(0, ge=0),
    page_size: int
):
    return {"page":page, "page_size": page_size}

#路由，访问时会执行下方函数
@app.get("/list")
async def list(commons = Depends(common)):
    return commons
```

### ORM

自动处理与数据库连接，使用面向对象编程操作数据库

使用sqlalchemy和aiomysql库

#### 建表

```python
#导入fastapi库
from fastapi import FastAPI
#导入建表函数
from sqlalchemy.ext.asyncio import create_async_engine

#创建一个FastAPI对象
app = FastAPI()

#创建异步引擎，根据实际情况更改
ASYNC_DATABASE_URL = "mysql+aiomysql://root:123456@localhost:3306/fastapi?charset=utf8"
async_engine = create_async_engine(
    ASYNC_DATABASE_URL,
    echo=True, #输出日志
    pool_size=10, #设置活跃连接池数量
    max_overflow=20 #允许额外连接数
)

#路由，访问时会执行下方函数
@app.get("/")
async def index():
    return {"message":"Welcome"}
```

#### 定义模型类

基类：创建时间、更新时间

书籍表：书名、作者、简介

```python
#导入基类模型，Mapped约定属性类型，mapped_column映射字段
from sqlalchemy.orm import DeclarativeBase,mapped_column,Mapped
from sqlalchemy import DateTime, String
from sqlalchemy.sql import func

#定义基类
class Base(DeclarativeBase):
    created_time : Mapped[datetime] = mapped_column(DateTime, insert_default=func.now(),default=func.now(),comment="创建时间")
    updated_time : Mapped[datetime] = mapped_column(DateTime, insert_default=func.now(), default=func.now(),onupdate=func.now(),comment="修改时间")

#定义表
class Book(Base):
    __tablename__ = "book"
    book_id : Mapped[int] = mapped_column(primary_key=True, comment="书籍id")
    book_name : Mapped[str] = mapped_column(String(255),comment="名称")
    book_introduction : Mapped[str] =mapped_column(String(255),comment="简介")

```

#### 建表

```
#寤鸿〃
@asynccontextmanager
async def lifespan(app: FastAPI):
    async with async_engine.begin() as conn:
        await conn.run_sync(Base.metadata.create_all)
    yield
    await async_engine.dispose()

app = FastAPI(lifespan=lifespan)

```

