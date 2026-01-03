---
title: SCAU-OJ/华南农业大学OJ系统题目
date: 2026-01-03 22:55:17
tags:
- 华南农业大学
- 编程
---

## 实验1 C语言程序初步

### 堂前习题

#### 6567 第一个C程序

 描述：

将下列程序输入Visual C++，编译、连接和运行该程序，运行通过后，提交程序。

 


 输入：

无


 输出：

```
The first C Program

```

 答案：

```c
#include <stdio.h>
int main()
{
    printf(“The first C Program\n”);
    return 0;
}

```

解析：


-  第一行是头文件，意思是本程序需要包含名为“stdio.h”的头文件。
 头文件在百度百科上的含义是：头文件作为一种包含功能函数、数据接口声明的载体文件,主要用于保存程序的声明,而定义文件用于保存程序的实现。
  简单来说，头文件就是有人在里面提前帮你写好了一些函数，你直接调用就可以了。
  比如本程序中的`stdio.h`头文件就是标准输入输出头文件，只要是和输入(如`scanf()`)输出(如`printf()`)有关的都在这里面了。


-  第二行是主函数的函数体，`main`前面只能写`int`


-  第四行的意思就是输出`The first C Program\n `这一个字符串，`\n `是换行符，在输出的时候会体现为换行。


-  第五行就是返回 0 ，主函数结束。

 

---

#### 1001 计算a+b

 Description

由键盘输入两个整数，计算并输出两个整数的和。


 输入格式

两个整数 a 和 b


 输出格式

输出 a+b 的结果


 输入样例

```
1 2

```

 输出样例

```
3

```

 答案：

```c
#include <stdio.h>
int main()
{
    int a,b;
    scanf(“%d%d”,&a,&b);
    printf(“%d”,a+b);
    return 0;
}

```

---

### 堂上练习

#### 11126 输出a与b中的较大值

 Description

下面程序实现由键盘输入两个整数 a 和 b ，判断并输出 a 与 b 中较大值。请在计算机上执行并验证该程序的正确性，之后提交到在线评判系统。


 输入格式

两个整数，以空格分隔


 输出格式

输出较大的那个数


 输入样例

```
5 7

```

 输出样例

```
7

```

 做法一：

```c
#include <stdio.h>
int main()
{
    int a,b;
    scanf(“%d%d”,&a,&b);
    
    if(a>b) printf(“%d”,a);
    else printf(“%d”,b);
    return 0;
}

```

**提醒：**像这样在某个区域空开一行有助于理清思路，可以养成好习惯


 做法二(调用函数)：

```c
#include <stdio.h>

int max(int a,int b)
{
    if(a>b) return a;
    else return b;
}

int main()
{
    int a,b;
    scanf(“%d%d”,&a,&b);
    printf(“%d”,max(a,b));
    return 0;
}

```

---

## 实验2 基本类型与运算

### 堂前习题

#### 1117 变量定义，按要求完成程序

 Description

下面给出一个程序，但是缺少部分语句，请按右边的提示补充完整缺少的语句。


```c
#include <stdio.h>
int main()
{
    _______________________ /*定义整型变量a和b*/
    _______________________ /*定义浮点变量i和j*/
    a=5;
    b=6;
    i=3.14; j=i*a*b;
    printf("a=%d,b=%d,i=%.2f,j=%.2f\n", a, b, i, j);
}

```

 答案：

```c
#include <stdio.h>
int main()
{
    int a,b;    /*定义整型变量a和b*/
    float i,j;  /*定义浮点变量i和j*/
    a=5;
    b=6;
    i=3.14;j=i*a*b;
    printf("a=%d,b=%d,i=%.2f,j=%.2f\n",a,b,i,j);
}

```

代码后面出现过什么就声明什么变量就好了


---

#### 6568 在显示屏上显示指定字符

 Description

要求编写一个程序，在显示屏上显示如下内容(全为半角字符，且不包含空格)：


```
C:\ABC.TXT

```

[提示] 注意转义字符在程序中的使用。


 输入格式

无


 输出格式

如题


 输出样例

```
C:\ABC.TXT

```

 答案：

```c
#include <stdio.h>
int main()
{
    printf(“C:\\ABC.TXT”);
    return 0;
}

```

注意：`\` 字符不能直接打出，要在前面加一个转义字符变成`\\`才能正常打出


---

#### 1119基本运算，写出程序运算结果

 Description

阅读下面程序，写出运行结果：

 


程序到此结束 请用下面程序输出你的答案(注意转义字符的正确表达)


```c
#include <stdio.h>
int main()
{
    printf("_______________________");
}

```

 答案：

```c
#include <stdio.h>
int main()
{
    printf("0,2,1,15.000000,1.000000,1.500000");
}

```

把上面的代码(图片)打一次然后复制下来，直接粘贴就能运行了。


究其原理
 我们看一下


- 声明了3个整型变量：a ，b ，c 。
- 声明了3个浮点型变量：d ，e ，f 。其中 d=15(实际上写 15.0 更规范一些)

-  `a=35%7;`
 把 35 对 7 取模并把值赋值给 a ，也就是现在 a=0。


-  `b=15/10;`
 把 15÷10 的值赋值给 b ，原本 15÷10 应该是等于 1.5 的，但是除号两边都是整型，因此 1.5 要向下取整，也就是 ⌊1015⌋ 得到 1 ，因此现在 b=1 。


-  `c=b++;`
 这一行的执行顺序可以拆分成两条：
  首先是`c=b;`
  其次是`b++;`
  所以现在 c 等于 b 原来的值，也就是 c=1.
  然后 b 递增，也就是 b=2。

 

注意！！！
 假如这个地方是`c=++b;`的话就要反过来！！


- 首先是`++b;`
- 其次是`c=b;`

所以首先 b递增，也就是 b=2.
 然后 c 等于 b 现在的值，也就是 c=2 .


- `e=15/10;`
 这个地方经常容易错！！很多人以为是 1.500000 ！！！
  这一行的意思是把`15/10`的值赋值给 e，原本 15÷10 应该是等于 1.5 的，但是除号两边都是整型，因此 1.5 要向下取整，也就是⌊1015⌋ 得到 1 。但是 1 是整型，e 是浮点型，所以要先把 1 转换成浮点型，也就是 1.000000 ，再赋值给 e 。所以现在 e=1.000000
- `f=d/10;`
 这一行的意思是把`d/10`的值赋值给 e，由于被除数 d 是浮点型，因此我们可以得到`d/10`的值是浮点型，也就是 1.500000 ，可以直接赋值给 f，所以 f=1.500000。

---

### 堂上练习

#### 1118 赋值表达式与赋值语句，写出程序运行结果

 Description

阅读下面程序，写出运行结果：

 


程序到此结束 请用下面程序输出你的答案(注意转义字符的正确表达)


```c
#include <stdio.h>
int main()
{
    printf("_______________________");
}

```

 答案：

```c
#include <stdio.h>
int main()
{
    printf("3.500000,3,330,J,a");
}

```

我们继续理清原理！！


- a 是浮点型。
- b 和 c 是整型。
- d 和 e 是字符。

-  `a=3.5;`
 把 3.5 赋值给 a ，a=3.50000。


-  `b=a;`
 把 a 赋值给 b ，要先把 a 转换成整型再赋值给 b ，要向下取整，3.5 转换成整型是 3，因此 b=3 。


-  `c=330;`


-  d=c;
 这里把 c 转换成ASCII码对应的字符赋值给 d，所以 d 是 `J`


-  `e='\141';`
 数字前面加反斜杠代表这个数是八进制数。这里是把 1418 转换成一个十进制的ASCII码对应的字符，赋值给 e ，所以 e 是 `a`。

 

---

## 实验3 基本输入与输出

### 堂前习题

#### 1126 字符的输入与输出

 Description

编程实现由键盘输入一个字符后，在屏幕上输出该字符。


 输入样例

```
a

```

 输出样例

```
a

```

 答案

```c
#include <stdio.h>

int main()

{
    char c;
    scanf("%c",&c);
    printf("%c",c);
    return 0;
}

```

 更简洁的答案

```c
#include <stdio.h>
int main()
{
    putchar(getchar());
    return 0;
}

```

答案应该不需要解释了，我可以讲一下这一个更简洁的答案
 `putchar(getchar());`
 这里包含了两个函数：


- 一个是`putchar();`
 他可以输出括号里面的字符，比如`putchar(‘K’);`他就会输出`K`。(仅限单个的字符)
- 另一个是`getchar();`
 他可以接受你在键盘上敲进来的字符(也叫标准输入)，并且把这个字符作为函数返回值进行返回。

然后这一串代码的逻辑就是：`getchar();`接收了你的输入并返回，然后`putchar();`接收到`getchar();`的返回值，然后直接输出。
 这样的好处就是节约了内存而且更简洁(是吧)。


---

#### 1127 计算加法

 Description

编程实现由键盘输入一个加法式，输出正确的结果。(两个加数均为整数)


 输入样例

```
10+20

```

 输出样例

```
30

```

 答案：

```c
#include <stdio.h>
int main()
{
    int a,b;
    scanf("%d+%d",&a,&b);
    printf("%d",a+b);
    return 0;
}

```

---

#### 1014 求圆面积

 Description

由键盘输入圆半径 r ，请计算并输出该圆的面积。(注：π 取 3.14159 ，结果采用浮点数表示，且要求仅显示两位小数位)


 输入格式

一个实数


 输出格式

输出以该实数为半径的圆面积


 输入样例

```
65.2

```

 输出样例

```
13355.02

```

 答案：

```c
#include <stdio.h>
int main()
{
    double r,s;
    scanf("%lf",&r);
    s=3.14159*r*r;
    printf("%.2f\n",s);
}

```

解释：
 注意！这里建议：需要用到浮点数的时候直接全部用`double`，不要用`float`！
 用`double`的时候输入要变成` %lf`，输出还是 `%f`不用变。


---

#### 1015 计算摄氏温度值

 Description

从键盘输入一个华氏温度值，要求按格式输出其对应的摄氏温度值，精确到小数点后两位。
 数学公式描述为：
 摄氏温度值等于9分之5 乘上 华氏温度值减去32的差 所得到的积。
 太恶心了居然连公式还要描述成这个样子 (我补充一下)$^{\circ}C = \frac{^{\circ}F-32}{1.8} $


 输入格式

华氏温度值


 输出格式

摄氏温度值，精确到小数点后两位


 输入样例

```
100

```

 输出样例

```
37.78

```

 答案：

```c
#include <stdio.h>
int main()
{
    double f,c;
    scanf("%lf",&f);
    c=5.0*(f-32)/9.0;
    printf("%.2f",c);
    return 0;
}

```

 错误答案

注意：也有同学是这样写的：


```c
#include <stdio.h>
int main()
{
    double t;
    scanf("%lf",&t);
    printf("%.2f",(9/5)*(t-32));
    return 0;
}

```

这样写是有问题的！
 为什么呢，是因为程序在计算`(9/5)`的时候是把他们当整型来计算的，所以`(9/5)` 相当于 1 而不是 1.8。


那么怎么改呢，我这里有两种方法：


- 第一种，把` (9/5)` 改成` (9.0/5)`
- 第二种，把 `(9/5) `改成 `(double)(9/5)`，强制类型转换。

这样子，就能得到 1.8 了。
 或者，你直接写 `1.8` 也行。


---

### 堂上练习

#### 11127 各位数字

 Description

从键盘输入一个 3 位数的正整数，要求先后输出该数的百位数字与个位数字，各占一行


 输入格式

一个三位整数


 输出格式

输出该数的百位数字与个位数字


 输入样例

```
123

```

 输出样例

```
1
3

```

 答案：

```c
#include <stdio.h>
int main()
{
    int n;
    scanf("%d",&n);
    printf("%d\n%d",n/100,n%10);
    return 0;
}

```

---

## 实验4 选择结构

### 堂前习题

#### 1018 数的排序

 Description

由键盘输入三个整数 a 、b 、c，按从小到大的顺序输出这三个数。


 输入格式

三个数由逗句分隔


 输入样例

```
65,45,90

```

 输出样例

```
45,65,90

```

 答案：

```c
#include <stdio.h>
#include <stdlib.h>
int main()
{
    int a,b,c,t;
    scanf("%d,%d,%d",&a,&b,&c);
    if(a>b){t=a;a=b;b=t;}
    if(a>c){t=a;a=c;c=t;}
    if(b>c){t=b;b=c;c=t;}
    printf("%d,%d,%d",a,b,c);
    return 0;
}

```

 答案(含指针)(较正式)：

```c
#include <stdio.h>

void swap(int *a,int *b)
{
    *a += *b;
    *b = *a - *b;
    *a -= *b;
}

int main()
{
    int a,b,c;
    scanf("%d,%d,%d",&a,&b,&c);
    if(a>b) swap(&a,&b);
    if(a>c) swap(&a,&c);
    if(b>c) swap(&b,&c);
    printf("%d,%d,%d",a,b,c);
    return 0;
}

```

解释：
 这里涉及到交换数据。
 最标准的写法就是写一个`swap()`函数(当然如果是c++的话直接调用库函数`std::swap`就好了)
 怎么写呢(毕竟交换不一定是交换整型，也可能是交换结构体嘛)


```c
void swap(数据类型 *a,数据类型 *b)
{
    数据类型 c;
    c = *a;
    *a = *b;
    *b = c;
}

```

这样就好了。
 然后你调用的时候括号里面要用指针(也就是地址，用`scanf`的时候里面那种)
 但是！我们经常用到的交换都是整型的交换，接下来我给大家介绍三种交换整型的方法：


- 创建中间变量

```c
int temp = a;
a = b;
b = temp;

```

很常用吧


- 加减法(随便起的名字)

```c
a = a+b;
b = a-b;
a = a-b;

```

举个例子:
 我们有变量 a 和 b
 设 a1=a+b
 设 bnew=a1−b
 设 anew=a1−bnew
 最后再看看
 bnew=a1−b=a+b−b=a
 anew=a1−bnew=a+b−a=b
 很自然而然就完成了变量交换


- 位运算法

```c
a^=b;
b^=a;
a^=b;

```

挺神奇的()，但是这个东西你们要先学完计概/计导才能明白，
 自己去探索一下吧！我这里就不展开解释了。


最后再讲一下这三个数排序的算法


- 首先判断是否 a<b ，不是就交换，这样就确保 a<b。
- 然后再判断是否 a<c，不是就交换，这样就确保 a<c，这样就确定 a 既小于 b ，又小于 c 。
- 再处理两个较大的数：判断是否 b<c ，不是就交换，这样就确保 b<c。

这样下来，就确定 a , b , c是有序的了！


---

#### 1016 字符变换

 Description

由键盘输入 5 个字符，将其中的大写字符变成小写(其它类型的字符不变)，最后，按输入顺序输出这 5 个字符。


 输入样例

```
ApPLe

```

 输出样例

```
apple

```

 答案：

```c
#include <stdio.h>
int main()
{
    char a,b,c,d,e;
    scanf("%c%c%c%c%c",&a,&b,&c,&d,&e);
    if(a<='Z'&&a>='A') a=a+32;
    if(b<='Z'&&b>='A') b=b+32;
    if(c<='Z'&&c>='A') c=c+32;
    if(d<='Z'&&d>='A') d=d+32;
    if(e<='Z'&&e>='A') e=e+32;
    printf("%c%c%c%c%c",a,b,c,d,e);
}

```

答案的做法没什么要补充的，32是ASCII码’a’和’A’的差值。


 我的做法(直接调用库函数)：

```c
#include <stdio.h>
#include <ctype.h>
int main()
{
    char a[5];  
    for(int i = 0 ; i < 5 ; i ++) scanf("%c",&a[i]);
    for(int i = 0 ; i < 5 ; i ++) printf("%c",tolower(a[i]));
    return 0;
}

```

我的做法的话


- 首先需要补充一个头文件 `<ctype.h>`
 里面包含了`tolower()`函数
  这个函数可以把字母转换成小写字母，如果是小写字母就不变(要返回字符，否则无效)
  具体操作应该也是类似的
- 其次使用了循环方便输入，可以简化代码
 大家以后会学到的

我的建议是大家熟练掌握答案的普遍做法之后可以简单了解一下 ` <ctype.h>` 头文件及其相关函数，可以方便大家操作


---

#### 1019 数的整除

 Description

由键盘输入 5 个整数，逐个判断它们能否被 27 整除，能的输出`YES`，不能的输出`NO`(注意，输出时，一个判断结果占一行， 5 个数的判断共占 5 行)。


 输入格式

用空格分隔


 输出格式

一行一个判断


 输入样例

```
8  27  17577  325  54

```

 输出样例

```
NO
YES
YES
NO
YES

```

 答案1：

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int a,b,c,d,e;
    scanf("%d %d %d %d %d",&a,&b,&c,&d,&e);
    if (a%27==0) printf("YES\n");
    else printf("NO\n");
    if (b%27==0) printf("YES\n");
    else printf("NO\n");
    if (c%27==0) printf("YES\n");
    else printf("NO\n");
    if (d%27==0) printf("YES\n");
    else printf("NO\n");
    if (e%27==0) printf("YES\n");
    else printf("NO\n");
}

```

 答案2：

```c
#include <stdio.h>
int main()
{
    int a[5];
    for(int i = 0 ; i < 5 ; i ++) scanf("%d",&a[i]);
    for(int i = 0 ; i < 5 ; i ++)
    {
        if(a[i]%27 == 0) printf("YES\n");
        else printf("NO\n");
    }
    return 0;
}

```

两种答案本质上是一样的，就是答案2使用了数组存储，并且加了循环简化代码


---

#### 1020 正负奇偶判断

 Description

由键盘输入非零整数 x，判断该数正负，正数输出`positive`，负数输出`negative`，接着判断该数的奇偶性，奇数输出`odd`，偶数输出`even`。


 输出格式

注意，正负判断结果与奇偶判断结果之间用回车符分隔


 输入样例

```
-43

```

 输出样例

```
negative
odd

```

 答案：

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int n;
    scanf("%d",&n);
    if(n>0) printf("positive\n");
    else if(n<0) printf("negative\n");
    if (n%2==0) printf("even\n");
    else printf("odd\n");
    return 0;
}

```

这题本质上和上一题是相同的，甚至是没有多测，就不再过多赘述了


---

#### 1023 简单计算器

 Description

下面程序是实现一个简单的运算器(保留两位小数点)，如果由键盘输入`10+50`，计算机可以输出结果`60.00`；如果输入`8＊6`，计算机输出`48.00`；如果输入`20/4`，计算机输出`5.00`；如果输入`8-6`，计算机输出`2.00`，请在空处填上适当的代码，运行通过后并提交。

 


 输入样例

```
45*2

```

 输出样例

```
result=90.00

```

 答案：

```c
#include <stdio.h>
int main()
{
    float a,b,c;
    char op;
    scanf("%f%c%f",&a,&op,&b);
    switch(op)
    {
        case'+':c=a+b;break;
        case'-':c=a-b;break;
        case'*':c=a*b;break;
        case'/':c=a/b;break;
        default:printf("error");return 0;
    }
    printf("result=%.2f",c);
    return 0;
}

```

这题其实还蛮简单的，老师甚至还挖了空给你
 只要按逻辑填空就好了
 关键是记得在`case`后面加`break`


---

### 堂上练习

#### 1007 判断平方数

 Description

由键盘输入一个正整数，判断该数是否为平方数，是输出Y，否则输出N


 输入格式

一个整数


 输出格式

```
Y`或者`N
```


 输入样例

```
49

```

 输出样例

```
Y

```

 答案：

```c
#include <stdio.h>
#include "math.h"
int main()
{
    int n;
    scanf("%d", &n);
    if((int)sqrt(n)*(int)sqrt(n)==n) printf("Y");
    else printf("N");
}

```

这里用到了`<math.h> `头文件中的函数 `sqrt()`
 该函数可以给你输入的数字开平方根并以`double`为类型返回
 应该很好理解的，就不再赘述了


给大家介绍一种笨方法：


```c
#include <stdio.h>
int main()
{
    int a , b;
    scanf("%d",&a);
    for(b = 0;b*b<=a;b++)
    {
        if(b*b == a)
        {
            printf("Y");
            return 0;   
        }   
        else continue;  
    } 
    printf("N"); 
    return 0;   
}

```

由于鄙人当时在写这道题目的时候并不知道有这个函数
 因此我写了如上程序
 一样能过
 逻辑就是从 0 找到一个平方之后比他大的数
 看看平方之后能不能等于那个数
 能就输出`Y`并结束程序
 不能就继续循环直到循环结束才输出`N`


---

#### 1017 求数的位数

 Description

由键盘输入一个不多于9位的正整数，要求输出它是几位数。


 输入格式

一个整数


 输出格式

输出该数为几位数


 输入样例

```
349213

```

 输出样例

```
6

```

 答案：

```c
#include <stdio.h>
int main()
{  
    int n,place;
    scanf("%ld",&n);
    if(n>99999999)  place=9;
    else if(n>9999999)  place=8;
    else if(n>999999)  place=7;
    else if(n>99999)  place=6;
    else if(n>9999)  place=5;
    else if(n>999)  place=4;
    else if(n>99)  place=3;
    else if(n>9)  place=2;
    else  place=1;
    printf("%ld\n",place);
}

```

这里我不得不吐槽答案真的写得太冗杂了
 但鉴于考虑到同学们应该还没学到循环也能理解
 下面就给出循环的解法


我的做法：


```c
#include <stdio.h>
int main()
{
    long long a,ans = 0;
    scanf("%lld",&a);
    while(a)
    {
        ans++;
        a/=10;
    }
    printf("%lld",ans);
    return 0;
}

```

因为`int`的上限差不多是 109 ，所以为了保险起见我开了`long long`
 又是因为是正整数，所以不需要考虑 0 的情况
 思路就是这样子了


---

#### 1120 判断点是否在圆上

 Description

由键盘输入一个点的坐标, 要求编程判断这个点是否在单位圆(圆心在坐标0,0)上，点在圆上输出`Y`, 不在圆上输出`N`。
 使用小数点后 3 位精度进行判断。


 输入样例

```
0.707,0.707

```

 输出样例

```
Y

```

 答案1:

```c
#include <stdio.h>
#include "math.h"
int main()
{
    double a,b;
    scanf("%lf,%lf",&a,&b);
    if(fabs(sqrt(a*a+b*b)-1)<1e-3)
    printf("Y\n");
    else  printf("N\n");
}

```

我记得这题是很多人不会写的(一开始)
 这个逻辑答案已经写得很清楚了
 其中补充一下`fabs()`函数，他会以`double`类型返回一个数的绝对值
 如果不会`fabs()`函数也没关系，
 我一开始也不知道有这个函数，
 这样子写也是可以的


 答案2：

```c
#include <stdio.h>
int main()
{
    double a,b,c;
    scanf("%lf,%lf",&a,&b);
    c=a*a+b*b;
    if(c >= 0.999 && c <= 1.001) printf("Y");
    else printf("N");
    return 0;   
}

```

这个程序实际上和答案1是等价的


---

## 实验5 循环结构(一)

### 堂前习题

#### 1024 计算阶乘

 Description

输入正整数 n(n<12)，计算 n!(注n!=1∗2∗3∗...∗n)


 输入样例

```
3

```

 输出样例

```
6

```

 答案：

```c
#include<stdio.h>
int main()
{
    int n,i;
    long s=1;
    scanf("%d",&n);
    for(i=1;i<=n;i++) s=s*i;
    printf("%d",s);
    return 0;
}

```

这一部分答案写得已经很清楚了，
 从 1 乘到 n，
 如果要保险一点的话建议开`long long`


---

#### 1025 计算简单数列和

 Description

有数列 1，3，5，7，9，11，…
 现要求由键盘输入 n ，计算输出该数列的前 n 项和。(n<10000)


 输入样例

```
5

```

 输出样例

```
25

```

 答案：

```c
#include<stdio.h>
int main()
{
    int i,n,sum;
    scanf("%d",&n);
    sum=0;
    for(i=1;i<=n;i++)
    {
        sum=sum+(2*i-1);
    }
    printf("%d",sum);
    return 0;
}

```

这个地方答案就是一个很暴力很无脑的做法
 难道刚刚高考完的学生连一个等差数列前 n 项和求和公式都记不住了吗


我的代码


```c
#include <stdio.h>
int main()
{
    int a;
    scanf("%d",&a);
    a=(1+(a*2-1))*a/2;
    printf("%d",a);
    return 0;   
}

```

虽然这样就丧失了老师想要同学们写循环的意义
 但是雀氏效率更高嘛


---

#### 1044 输出最小值

 Description

从键盘输入十个整数，输出最小值


 输入格式

输入的整数绝对值不会超过 10000


 输出格式

按样例格式输出结果


 输入样例

```
12  45  76  87  5  87  43  55  99  21

```

 输出样例

```
5

```

 答案

```c
#include <stdio.h>
int main()
{  
    int i,t,min;
    scanf("%d", &min);
    for(i=1;i<10;i++)
    {
        scanf("%d", &t);
        if(t<min) min=t;
    }
    printf("%d\n",min);
}

```

这个问题的关键就在于对 min 的初始化
 答案给出的解法是把第一个数初始化为最小值
 这也是最常用且稳定性最高的做法之一(我写题也经常这样写)
 但是我们就题论题啊
 这个输入的整数最大不超过 10000
 这么小
 那我们设定最小值初始化为比 10000 大的数不就好了吗
 这样操作逻辑就更加简单了


我的代码


```c
#include <stdio.h>
int main()
{  
    int i,t,min=100000;
    for(i=1;i<=10;i++)
    {
    scanf("%d", &t);
    if(t<min) min=t;
    }
    printf("%d\n",min);
}

```

---

### 堂上练习

#### 1030 字符变换

 Description

由键盘输入一个句子(字符个数不定，最多不超过 80 个，以`'\n'`结束)，将其中的大写字符变成小写(其它类型的字符不变)，
 最后输出变换后的句子。


 输入样例

```
ThiS IS My fIrSt C ProgrAm!

```

 输出样例

```
this is my first c program!

```

这题实际上就是个循环嵌套一个选择结构
 照着前面实验3那道字符变换往循环里塞就行


 答案

```c
#include<stdio.h>
int main()
{
    char i;
    while((i=getchar())!='\n')
    {
        if('A'<=i&&i<='Z')
        i+=32;
        printf("%c",i);
    }
    return 0;
}

```

我的代码(这答案多麻烦啊)


```c
#include <stdio.h>
#include <ctype.h>
int main()
{
    char c;
    while((c = getchar()) != '\n')
    printf("%c",tolower(c));
    return 0;
}

```

---

#### 1037 计算数列和

 Description

有数列：

 


编程实现，由键盘输入 n，计算输出数列前 n 项和。(结果保留四位小数，提示：要使用`double`，否则精度不够)


 输出格式

请按格式输出


 输入样例

```
20

```

 输出样例

```
32.6603

```

 答案：

```c
#include<stdio.h>
int main()
{  
    int i,n;
    double a=2,b=1,s=0;
    scanf("%d",&n);
    for(i=1;i<=n;i++)
    {  
        s=s+a/b;
        a=a+b;
        b=a-b;
    }
    printf("%.4f\n",s);
}

```

这题就是一个斐波那契数列的一个变形
 跟着题目写就好了
 `a`和`b`都用`double`也行
 我个人习惯是强制转换成double
 最后记得保留四位小数


---

#### 1029 求最大公约数

 Description

由键盘输入两个正整数 m、n(m、n<1000000) ，计算它们的最大公约数。


 输入样例

```
16,24

```

 输出样例

```
8

```

 答案

```c
#include<stdio.h>
int main()
{  
    long r,m,n;
    scanf("%ld,%ld",&m,&n);
    while((r=n%m)!=0)
    {  
        n=m;
        m=r;
    }
    printf("%ld\n",m);
} 

```

是不是很惊讶答案为什么这么写
 这是欧几里得算法求最大公约数
 求余、交换，直到余数为 0
 打acm的经常会用到(虽然可以直接调用stl就是了)
 如果不会的也可以直接暴力求解
 像我最开始那样


我的“朴素”解法


```c
#include <stdio.h>
int main() 
{
    int a,b,c,min;
    scanf("%d,%d",&a,&b);
    for(min=c=1;c<=a||c<=b;c++)
    {
        if(a%c==0&&b%c==0)
        {
            min = c;    
        }
    }
    printf("%d",min);
    return 0;
}

```

---

#### 1031 统计单词个数

 Description

写一个函数实现：输入一行字符，以空格分割单词，回车结束输入，输出单词的个数


 输入样例

```
There are many students and many trees!

```

 输出样例

```
7

```

这题实际上就是需要你做一个标记
 标记这个字符的前一个字符是不是字母


- 如果前一个是字母而这一个不是，那说明这到了单词的末尾
- 如果前一个是字母且这一个是，那说明现在在单词中间
- 如果前一个不是字母这一个也不是，那就不用管它
- 如果前一个不是字母而这一个是，说明这是在单词的开头

我们只需要在单词开头的地方记录单词数量 +1


最后输出单词数量就好了


 答案

```c
#include<stdio.h>
int main()
{  
    int num=0,word=0;
    char c;
    while((c=getchar())!='\n')
    {
        if(!(c>='a'&&c<='z'||c>='A'&&c<='Z')) word=0;
        else if(word==0)
        {  
            word=1;
            num++;
        }
    }
    printf("%d",num);
}

```

答案还是比较巧妙的


---

#### 1042 百万富翁

 Description

一个百万富翁遇到一个陌生人，陌生人找他谈了一个换钱的计划。该计划如下：我每天给你 m 元，
 而你第一天只需给我一分钱。第二天我仍给你 m 元，你给我 2 分钱。第三天，我仍给你 m 元，
 你给我 4 分钱。依次类推，你每天给我的钱是前一天的两倍，直到一个月( 30 天)。
 百万富翁很高兴，欣然接受这个契约。现要求，编写一个程序，由键盘输入 m ，
 计算多少天后，百万富翁开始亏钱。


 输入样例

```
100

```

 输出样例

```
18

```

很显然这只需要一个`while循环`就好了
 亏钱了就`break`


 答案

```c
#include <stdio.h>
int main()
{
    int m,a=1,d=1,sum=0;
    scanf("%d",&m);
    m=m*100;
    while(1)
    {  
        sum=a+sum;
        if(sum>m*d) break;
        d++;
        a=2*a;
    }
    printf("%d",d);
    return 0;
}

```

---

## 实验6 循环结构(二)

### 堂前习题

#### 1035 打印菱形图案

 Description

由键盘输入正数 n(n<30)，要求输出如下 2×n+1行的菱形图案。


 输出格式

菱形右边不留多余空格


 输入样例

```
2

```

 输出样例

```
  *
 ***
*****
 ***
  *

```

 答案：

```c
#include <stdio.h>
int main()
{
int n;
scanf("%d",&n);

for(int i = 1 ; i <= n ; i ++)
{
    int kong = n - i + 1;
    int xing = 2*i-1;   
    for(int j = 1 ; j <= kong ; j ++) printf(" ");  
    for(int b = 1 ; b <= xing ; b ++) printf("*")   
    printf("\n");
}

for(int i = 1 ; i <= 2*n+1 ; i ++) printf("*");
printf("\n");

for(int i = n ; i >= 1 ; i --)
{
    int kong = n - i + 1;
    int xing = 2*i-1;
    for(int j = 1 ; j <= kong ; j ++) printf(" ");  
    for(int b = 1 ; b <= xing ; b ++) printf("*");  
    printf("\n");
}
return 0;
}

```

虽然代码长了点，
 但是实际上下面的部分是上面部分复制下来的
 只是改了第一行的变量而已
 变量的设置还是很有逻辑性的


其实编程不是越短越好
 像现在刚入门的话
 还是最好先把代码写清晰
 写明白了才是最重要的
 至于什么时空复杂度，什么鲁棒性健壮性，那就是以后提升的事了


---

### 堂上练习

#### 1028 求素数

 Description

输出 2 到 200 之间(包括 2、200 )的所有素数(注：要求 1 行 1 个素数，按由小到大的顺序输出)。


 输入样例

(无)


 输出样例

```
2
3
5
7
……
199

```

 答案1：

```c
# include<stdio.h>
# include<math.h>
int main()
{  
    int m,k,i;
    for(m=2;m<=200;m++)
    {  
        k=sqrt(m);
        for(i=2;i<=k;i++)
        if(m%i==0) break;
        if(i>k) printf("%d\n",m);
    }
}

```

`sqrt()`函数我们接触过，忘记的我们可以看看：实验4 堂上练习 1007 判断平方数


答案为什么这样子写呢？


首先我们看：什么是素数？？

 

 素数就是质数，只能整除1和它本身

 

那假如有一个合数 n ，他除了能整除 1 和它本身，还能整除另外的数
 那它除以另一个数时候，得出的商也算是它的因子
 这两个数(另一个因子 和 商)必然一大一小，
 当较小的数最大的时候，不能超过 n 
            
             
           
 而我们只需要判断 n 是否能整除一个不是 1 和他本身的数就可以了
 所以遍历检查到根号 n 即可。


但是！
 其实这题没这个必要，直接遍历到 n−1 就可以了（数据范围不大）
 另：养成加括号和 `return 0` 的好习惯！


 答案2：

```c
# include<stdio.h>
# include<math.h>
int main()
{  
    int m,k,i;
    for(m=2;m<=200;m++)
    {  
        for(i=2;i<m;i++)
        {
            if(m%i==0) break;
        }
        if(i == m) printf("%d\n",m);    
    }
    return 0;
}

```

---

#### 1137 找满足要求的数字

 Description

输出 1 到 9999 中能被 7 整除，而且至少有一位数字是 5 的所有数字


 输出格式

一行一个


 输出样例

```
35
56
105
154
......

```

 答案1：

```c
#include <stdio.h>
int main()
{ 
    int i, j;
    for(i=7; i<=9999; i=i+7)
    { 
        j=i;
        while(j!=0)
        {
            if(j%10==5) break;
            j=j/10;
        }
        if(j!=0) printf("%d\n", i);
    }
}

```

这题稍微有一点点复杂，但是我们只需要关注到两个点：


- 能被 7 整除
- 至少有一位数字是 5

我们只需要判断这两个条件就可以了


答案1写得挺好的，时间复杂度也够(剪了一下枝)
 但是逻辑不够暴力，大家可以看着学习一下
 我再给一个更加平白的代码


 答案2：

```c
#include <stdio.h>
int main()
{
    for(int i = 1 ; i <= 9999 ; i ++)
    {
        int jud = 0;    
        int temp = i;   
        while(temp != 0)    
        {   
            if(temp % 10 == 5) jud = 1; 
            temp /= 10; 
        }
        if(i%7 == 0 && jud == 1) printf("%d\n",i);
    }
    return 0;
}

```

像这样暴力就好了


---

#### 1038 打印图案

 Description

由键盘输入正数 n(n<10) ，要求输出如下中间数字为 n 的菱形图案。


 输出格式

菱形右边不留多余空格


 输入样例

```
4

```

 输出样例

```
   1
  121
 12321
1234321
 12321
  121
   1

```

 答案：

```c
#include <stdio.h>
int main()
{
int n;
scanf("%d",&n);

for(int i = 1 ; i < n ; i ++)
{
    int kong = n - i;   
    for(int j = 1 ; j <= kong ; j ++) printf(" ");  
    for(int j = 1 ; j < i ; j ++) printf("%d",j);   
    for(int j = i ; j >= 1 ; j --) printf("%d",j);  
    printf("\n");
}

for(int i = 1 ; i < n ; i ++) printf("%d",i);
for(int i = n ; i >= 1 ; i --) printf("%d",i);
printf("\n");

for(int i = n-1 ; i >= 1 ; i --)
{
    int kong = n - i;   
    for(int j = 1 ; j <= kong ; j ++) printf(" ");  
    for(int j = 1 ; j < i ; j ++) printf("%d",j);   
    for(int j = i ; j >= 1 ; j --) printf("%d",j);  
    printf("\n");
}
return 0;
}

```

这题其实和 堂前习题 1028 打印菱形图案十分类似
 只要把输出的星号改一下就好了


---

## 实验7 数组的应用

### 堂上练习

#### 1039 倒序

 Description

由键盘输入 10 个整数，倒序输出。


 输入样例

```
70
5
14
20
19
2
99
67
13
66

```

 输出样例

```
66
13
67
99
2
19
20
14
5
70

```

 答案1：

```c
#include <stdio.h>
int main()
{
    int a[10];
    for(int i = 0 ; i < 10 ; i ++) scanf("%d",&a[i]);
    for(int i = 9 ; i >= 0 ; i --) printf("%d\n",a[i]);
    return 0;
}

```

把数字存在数组里面，然后倒着输出就可以了


甚至我可以不用数组存，用函数递归


 答案2

```c
#include <stdio.h>

void p(int t)
{
    int num;
    scanf("%d",&num);
    if(t < 10) p(t+1);
    printf("%d\n",num);
}

int main()
{
    p(1);
    return 0;
}

```

这些都是可以的


---

#### 1062 打印矩阵

 Description

由键盘输入一个 3×4的矩阵，要求输出它的转置矩阵。


 输入格式

3 行 4 列的矩阵，数与数之间由一个空格分隔


 输出格式

4 行 3 列的矩阵，数与数之间由一个空格分隔


 输入样例

```
1 6 9 3
1 1 0 2
1 9 8 9

```

 输出样例

```
1 1 1
6 1 9
9 0 8
3 2 9

```

 答案：

```c
#include <stdio.h>
int main()
{
    int a[3][4],b[4][3],i,j;
    for(i=0;i<3;i++)
    for(j=0;j<4;j++)
    {
        scanf("%d",&a[i][j]);
        b[j][i]=a[i][j];
    }
    for(i=0;i<4;i++)
    {
        for(j=0;j<3;j++) printf("%d ",b[i][j]);
        printf("\n");
    }
}

```

答案写得很规范，是这样的操作没错


- 一开始我们是按行存储的
 然后我们只要按列输出就可以了

或者


- 存储的时候直接存到即将输出的位置(直接矩阵转换)
 输出就可以直接按行输出了

---

### 堂上练习

#### 1047 冒泡排序

 Description

由键盘输入 10 个数，用“冒泡法”对 10 个数从小到大排序，并按格式要求输出。代码如下，请填充完整。


```c
#include <stdio.h>
int main()
{ 
    int a[10], i, j, t;
    for(i=0;i<10;i++)
        scanf("%d",_______________________) ;  
    for(_______________________)
    {   
        for(j=0;j<_______________________;j++)
        if (_______________________)
            {_______________________}
    }
    for(i=0;i<10;i++)
        printf("%d ",a[i]);
}

```

 输入样例

```
70 5 14 20 19 2 99 67 13 66

```

 输出样例

```
2 5 13 14 19 20 66 67 70 99

```

 答案：

```c
#include <stdio.h>
int main()
{  
    int a[10], i, j, t;
    for(i=0;i<10;i++)
        scanf("%d",&a[i]) ;   
    for(i=0;i<9;i++)
    {   
        for(j=0;j<9-i;j++)
        if (a[j]>a[j+1])
            {
                t=a[j];
                a[j]=a[j+1];
                a[j+1]=t;
            }
    }
    for(i=0;i<10;i++)
        printf("%d ",a[i]);
}

```

 答案（纯享版）

```c
&a[i]

i=0;i<9;i++

9-i

a[j]>a[j+1]

t=a[j];a[j]=a[j+1];a[j+1]=t;

```

这个程序真的写得好恶心啊
 最讨厌这种填空的题目了


**注意！！！**大家写这些题目的时候一定要先编译完通过之后再复制粘贴到框里面
 **而且！！！**粘贴完之后看看有没有少个分号或者多个分号之类的
 特别容易错！！！
 考试要是因为这些错！！贼亏！！！


我们拆开看一下


- `scanf("%d",&a[i]); `
 第一个空就是存储，这个很简单
- `for(i=0;i<9;i++)`
 每一次遍历扫一次，把最大的数放到后面，这里扫9次还是10次都没关系
- `for(j=0;j<9-i;j++)`
 其实这个地方不一定要9-i，直接写9也是可以的
  因为后面的已经有序了，再去遍历不会造成任何影响
- `if (a[j]>a[j+1])`
 这里就是当现在的数大于后面的数的时候就执行下面的代码
  因为这里涉及到判断i+1的数，所以上面的9-i部分写的时候不能填10
  否则会数组越界
- `{t=a[j];a[j]=a[j+1];a[j+1]=t;}`
 这里就是很经典的交换变量内容的代码了

---

#### 1040 统计不同数字的个数

 Description

由键盘输入 20 个整数，统计不同数字的个数。


 输入样例

```
70  5  14  22  19  2  99  67  13  66  5  93  44  38  22  11  39  22  33  11

```

 输出样例

```
16

```

 提示

因为 5 有 1 个重复数字， 11 有 1 个重复数字， 22 有 2 个重复数字


 答案1：

```c
#include<stdio.h>
int main()
{  
int a[20];
  int i,t,p=0;
  for(i=0;i<20;i++)
  {  
  scanf("%d",&a[i]);
for(t=0;t<i;t++)
  if(a[t]==a[i])break;
if(t==i)
p++;
  }
  printf("%d",p);
} 

```

这是一种暴力做法，确实很暴力。


但是吧，我个人比较喜欢计数数组。


 答案2：

```c
#include <stdio.h>
int a[1000010];
int main()
{  
    int i; 
    for(i=0;i<20;i++)
    {   
        int num;    
        scanf("%d",&num);   
        a[num] ++;
    }
    int ans = 0;
    for(int i = 0 ; i < 1000010 ; i ++)
    {
        if(a[i] > 0) ans ++;
    }
    printf("%d",ans);
    return 0;
}

```

注意：这个数组一定要开在全局变量(就是`main`函数的上面)
 不然无法运行的
 而且全局变量的数组内容默认为 0
 不用初始化


---

#### 1051 找矩阵中的鞍点

 Description

由键盘输入一个 3×4 ( 3 行 4 列)的数字矩阵，其中任意两个数字均不相同。要求输出该数字矩阵中的鞍点(即在矩阵行中最大，列中最小的数)。
 若没有鞍点，输出`NO`字样。


 输入样例

```
87  90  110  98
70  97  210  65
99  45  120  30

```

 输出样例

```
110

```

 答案：

```c
#include <stdio.h>
#include <stdlib.h>
int main()
{
    int i,j,a[3][4],flag,col;
    for(i=0;i<3;i++)
    for(j=0;j<4;j++)
    scanf("%d",&a[i][j]);
    for(i=0;i<3;i++)
    {
        col=0;
        for(j=1;j<4;j++)
        if(a[i][j]>a[i][col]) col=j;
        flag=1;
        for(j=0;j<3;j++)
        {
            if(a[j][col]<a[i][col])  flag=0;
        }
        if(flag==1)
        {
            printf("%d", a[i][col]);
            return 0;
        }
    }
    printf("NO\n");
    return 0;
}

```

这题相对于之前的题目，难度开始提升了
 答案写得很好，找出每一行的最大值，然后对最大值所在的列遍历，找最小值
 看看两者是否相同：


- 如果相同就输出
- 如果不同就继续找

一旦输出就结束程序
 要是遍历完整个矩阵都还没有输出，就输出 `NO`


---

#### 1046 计算高精度加法

 Description

由键盘输入两个位数很长的整数(一行一个，最多不超过 80 位)，试计算并输出这两个数的和。


 输入样例

```
1234567890123456789353534532453453453434534
987654321098765324534534534534532

```

 输出样例

```
1234567891111111110452299856987987987969066

```

 答案：

```c
#include <stdio.h>
#include <string.h>

const int N = 1e4;
int a[N],b[N],c[N];
char s[N];

int main()
{  
    int i=0,max=0,e=0;
    
    gets(s);
    int n1=strlen(s);
    for(i=n1-1;i>=0;i--) a[n1-1-i]=s[i]-'0';
    
    gets(s);
    int n2=strlen(s);
    for(i=n2-1;i>=0;i--) b[n2-1-i]=s[i]-'0';
    
    if(n1>n2) max=n1;
    else max=n2;
    
    for(i=0;i<=max;i++)
    {   
        c[i]=(a[i]+b[i]+e)%10;
        e=(a[i]+b[i]+e)/10;
    }
    if(c[max]>0) printf("%d",c[max]);
    for(i=max-1;i>=0;i--) printf("%d",c[i]);
    return 0;
}

```

高精度加法，这题真的已经很难了
 我先解释一下我们要怎么做：


- 首先我们要把输入的数字存储起来(用字符串)
- 然后把字符串的内容反过来一个一个数字存在数组里面
- 然后模拟加法的操作
 一位一位加(并且记录是否要进位加1)，
  把每一位的结果存储在另一个数组里面
- 最后再判断最后一位是否需要进1(加一位)
- 然后逆序输出这个数组就可以了

现在我们来逐行解析：


- `int a[100]={0},b[100]={0},c[100]={0};`
 创建数组，数组a存储加数1，数组b存储加数2，数组c存储和，初始化为0
- `int i=0,n1=0,n2=0,max=0,e=0;` 注：e是存储上一位是否进一的变量。
 `gets(s);`
  `n1=strlen(s);`
  获得加数1的字符串并判断其长度
- `for(i=n1-1;i>=0;i--) a[n1-1-i]=s[i]-'0';`
 把字符串中的加数1转移到数组a中(逆序)
- `gets(s);`
 `n2=strlen(s);`
  获得加数2的字符串并判断其长度
- `for(i=n2-1;i>=0;i--) b[n2-1-i]=s[i]-'0';`
 把字符串中的加数2转移到数组a中(逆序)
- `if(n1>n2) max=n1;`
 `else max=n2;`
  判断较长的位数是多少(因为加法要运算到这一位)
- `for(i=0;i<=max;i++)`
 每一位进行遍历加法运算
  但是注意！如果是每一位加法的话，那应该是 < max
  这里是 <=max 是因为顺便处理了最后一个进位(使得第max位可能是0或1)
- `c[i]=(a[i]+b[i]+e)%10;`
 这个是加法运算后结果第i位上的结果
- `e=(a[i]+b[i]+e)/10;`
 下一位要进位多少(可能是0或者1)
- `if(c[max]>0) printf("%d",c[max]);`
 如果第max位大于0，那么这一位就是有数字的，那就要输出
- `for(i=max-1;i>=0;i--)`
 `printf("%d",c[i]);`
  然后逆序输出剩下的每一位

附：`gets(s);`是一个函数，作用是直接读入一行的内容，并把这些内容以字符串的形式存储在括号内(你给)的字符串内


---

## 实验8 字符数组及串

### 堂前习题

#### 1121 定义存贮字符串的数组

 Description

在下面程序中填充定义字符数组的语句，使程序完整。


```c
#include <stdio.h>
#include <string.h>
int main()
{  
    _______________________/*define a array named s to store string*/
    strcpy(s, "abcdefghijklmn");
    printf("%s", s);
    return 0;
}

```

 答案：

```
char s[15];

```

没什么好说的，过了下一个


---

#### 1122 字符串的合并

 Description

从键盘输入 3 个字符串(每个字符串以回车符做为结束标志)，将 3 个字符串以输入先后顺序合并到字符串 s 中，
 请填空使用程序完整。


```c
#include <stdio.h>
#include <string.h>
int main()
{  
    char s[100]="";
    char a[30];
    _______________________
    printf("%s", s);
}

```

 输入样例

```
123
abc
456

```

 输出样例

```
123abc456

```

 答案1：

```c
char b[30],c[30];
gets(a);
gets(b);
gets(c);
strcat(s,a);
strcat(s,b);
strcat(s,c);

```

一行内可不止能写一个分号(乐)
 介绍一下`strcat()`函数
 如`strcat(s,a)`，这样子写就是可以把 a字符串复制到s字符串结尾，使他们拼接起来(但是要注意内容不要越界)
 其实就算你不会这个函数也能写


 答案2：

```c
char b[30],c[30];
gets(a);
gets(b);
gets(c);
printf("%s%s%s",a,b,c); 

```

虽然这个没有达到老师的目的，但是也能过题就是了


---

#### 1123 字符串的输入与输出

 Description

下面程序实现从键盘读入字符串，然后输出到屏幕，请填充必要的语句。


```c
#include <stdio.h>
int main()
{  
    char s[50];
    printf("What's your name?\n");
    _______________________ /*iput your name from the keyboard*/
    printf("Your name is ");
    printf("_______________________", s); /*output your name*/
}

```

 输入样例

```
Wang

```

 输出样例

```
What's your name?
Your name is Wang

```

 答案：

```c
#include <stdio.h>
int main()
{  
    char s[50];
    printf("What's your name?\n");
    gets(s); /*iput your name from the keyboard*/
    printf("Your name is ");
    printf("%s", s);  /*output your name*/
}

```

没什么好说的


---

### 堂上练习

#### 1145 回文串

 Description

读入一行字符串(不多于 80 个字符，以回车结束)，判断该字符串是否为回文串(即从左向右拼写与从右向左拼写是一样的)，是则输出`Y`，不是则输出`N`。


 输入格式

一行字符串


 输出格式

是则输出`Y`，不是则输出`N`


 输入样例

```
abba

```

 输出样例

```
Y

```

#### 提示

 input1:

```
abcba

```

 output2:

```
Y

```

 input2:

```
abc

```

 output2:

```
N

```

 答案1：

```c
#include <stdio.h>
#include <string.h>
int main()
{ 
    int i, j;
    char a[100];
    scanf("%s",buf);
    for(i=0, j=strlen(buf)-1;i<j; i++, j--)
        if(buf[i]!=buf[j]) break;
    if(i>=j) printf("Y");
    else printf("N");
}

```

就是：
 设字符串长度为 l
 从下标为 0 开始，比较下标为 i 的字符与下标为 l−i−1 的字符是否相同
 直到 i>l/2 为止


我不太喜欢这种写法，虽然同样是双指针
 我比较喜欢这样写


 答案2：

```c
#include <stdio.h>
#include <string.h>

int main()
{
    char s[10000];
    scanf("%s",s);
    int begin = 0;;
    int end = strlen(s) - 1;
    while(begin < end)
    {
        if(s[begin] != s[end])  
        {   
            printf("N");    
            return 0;   
        }   
        begin ++;   
        end --;
    }
    printf("Y");
    return 0;
}

```

完全模拟出两个指针指向开头和结尾，
 向中间逼近判断的过程。


---

#### 1050 寻找字符串

 Description

由键盘输入两个字符串(假设第一个字符串必包含第二个字符串，如第一个字符串为`ABCDEF`，第二个为`CDE`，
 则`CDE`包含在`ABCDEF`中，现要求编程输出第二字符串在第一行字符串中出现的位置。
 (如果第二个字符串在第一个字符串中出现多次，则以最前出现的为准)


 输入样例

```
ABCDEFG
DE

```

 输出样例

```
4

```

 提示

因为`DE`在`ABCDEFG`中的第 4 个字符处出现


 答案：

```c
#include  <stdio.h>

int main()
{  
    int i,j;
    char a[80], b[80];
    gets(a);
    gets(b);
    for(i=0;a[i]!='\0';i++)
    {   
        for(j=0;b[j]!='\0';j++)
        {   
            if(a[i+j]!=b[j]) break; 
        }   
        if(b[j]=='\0')
        {
            printf("%d",i+1);
            return 0;
        }
    }
    printf("Not Found");
    return 0;
}

```

我们都知道，`gets()`函数得到的字符串是以空字符 `\0` 结尾的
 也就是说，如果我们检测字符串b到空字符的话，这一串字符串是与字符串b完全相同的
 这个时候输出答案终止程序即可


PS：注意！这样子写并不是效率最高的！想学一些进阶内容的同学可以去了解一下KMP算法


---

## 实验9 函数的应用

### 堂前习题

#### 1083 编写函数计算阶乘

 Description

下面程序实现由键盘读入整数 n ，计算并输出 n!，请补充完整计算阶乘的函数。


```c
#include <stdio.h>

_______________________

main()
{   
    int n;
    scanf("%d", &n);
    printf("%ld", fanc(n));
}

```

 输入样例

```
3

```

 输出样例

```
6

```

 答案1：

```c
long fanc(int a){
    long i,product;
    product=1;
    for(i=1;i<=a;i++)
    {
        product=product*i;
    }
    return product;
}

```

这样写就是使用了循环，从 1 乘到 a 形成循环
 但是既然都是返回值了，为什么不用递归呢(也很好写的)
 大家可以体会一下什么是递归


 答案2（递归写法）：

```c
long fanc(int n)
{
    if(n <= 1) return 1;
    else return n*fanc(n-1);
}

```

举个例子，如果调用 fanc(5)，函数的执行过程如下：
 fanc(5) 调用 fanc(4) 并乘以 5
 fanc(4) 调用 fanc(3) 并乘以 4
 fanc(3) 调用 fanc(2) 并乘以 3
 fanc(2) 调用 fanc(1) 并乘以 2


fanc(1) 返回 1
 fanc(2) 返回 2×1=2
 fanc(3) 返回 3×2=6
 fanc(4) 返回 4×6=24
 fanc(5) 返回 5×24=120


因此，fanc(5) 的结果是 120 ，即 5 的阶乘。
 特殊的，0 的阶乘是 1


---

#### 1124 函数中的变量

 Description

写出下面程序的运行结果：


```c
int f1(int x)
{   
    static int z=3,y=0;
    y++;
    z++;    
    return(x+y+z);
}

main()
{   
    int a=1,k;
    for(k=0;k<3;k++) printf("%4d",f1(a));
}

```

程序到此结束 请用下面程序输出你的答案(注意转义字符的正确表达)


```c
#include <stdio.h>
main()
{
    printf("_______________________");
}

```

 答案：

```
  6  8  10

```

复制下来粘贴上去就好了
 或者你写三个`%4d`也不是不行


---

### 堂上练习

#### 1059 [填空题]函数定义

 Description

下面是使用辗转相除法，求最大公约数的程序，请补充完整程序中函数的定义与调用，运行通过后提交代码。


```c
#include  <stdio.h>

_______________________
{
    int  r;
    while ((r=m%n)!=0)
    {
        m=n;
        n=r;
    }
    return  n;
}

main()
{
    int  a, b, n;
    scanf("%d%d", &a, &b);
    printf("%d\n", _______________________);
}

```

 输入样例

```
24 16

```

 输出样例

```
8

```

答案(不唯一)：


```c
int c(int m,int n)

c(a,b)

```

答案的 c 可以随便换，其他不变就行


---

#### 1084 [填空题]十进制数转二进制数

 Description

下面程序，实现由键盘输入一个正整数(不大于 100000000)，输出其对应的二进制数(原码表示)。
 请填空：


```c
#include <stdio.h>

_______________________

main()
{
    int n;
    scanf("%d", &n);
    binary(n);
}

```

 输入样例

```
12

```

 输出样例

```
1100

```

 答案：

```c
void binary(int i)
{
    if(i>1) binary(i/2);
    printf("%d",i%2);
}

```

如果不是很懂的话
 可以先手动写一个数再自己推一下


举个例子，如果我们调用 binary(5)，函数的工作流程如下：


- 首先，i=5，大于 1，所以进行递归调用  binary(2) (因为 ⌊25⌋=2)。
- 在 binary(2); 中，i=2 ，大于 1，所以进行递归调用 binary(1) (因为 ⌊22⌋=1)。
- 在 binary(1) 中，i=1，不大于 1，所以打印 1(1%2=1)，然后返回。
- 返回到 binary(2)，此时 i=2，但由于递归调用已经返回，接下来执行 `printf("%d",i%2)`;，打印 0(2%2=0)。
- 最后，返回到最初的 binary(5) ，此时仍然 $ i=5$，但由于递归调用已经返回，接下来执行 `printf("%d",i%2)`，打印 1(5%2=1)。

因此，binary(5) 的输出将是 101，这正是 5 的二进制表示(从最低位到最高位)。


---

#### 1151 求函数值

 Description

输入 x ( x 为整数)，求函数值
 函数定义如下：


```c
F(x)=x                  //x小于3
F(x)=F(x/3)*2           //x大于等于3且x为3的倍数
F(x)=F((x-1)/3)+1       //x大于等于3且x除3余1
F(x)=F((x-2)/3)+2       //x大于等于3且x除3余2

```

 输入格式

一个整数


 输出格式

结果


 输入样例

```
20

```

 输出样例

```
6

```

 答案：

```c
#include<stdio.h>

int F(int x)
{
  int y;
  if(x<3) y=x;
  else if(x%3==0) y=F(x/3)*2;
  else if(x%3==1) y=F((x-1)/3)+1;
  else if(x%3==2) y=F((x-2)/3)+2;
  return y;
}

int main()
{
  int x;
  scanf("%d",&x);
  printf("%d",F(x));
}

```

这题就是这样，按着题目的意思写就好了


---

## 实验10 指针与结构体

### 堂前习题

#### 1091 [填空]交换两数，由大到小输出

 Description

下面程序，交换两数，使两数由大到小输出，请填空


```c
#include <stdio.h>

void swap(_______________________)     
{ 
    int temp;
    temp=*p1;
    *p1=*p2;
    *p2=temp; 
} 

int main()                        
{ 
    int a,b; int *pa,*pb;
    scanf("%d%d", &a, &b);
    pa=&a; pb=&b;
    if(a<b) swap(_______________________);
    printf("%d %d\n",a,b);
} 

```

 输入样例

```
1 2

```

 输出样例

```
2 1

```

 答案(固定)：

```c
int *p1,int *p2

&a,&b

```

因为要在main函数外交换两个变量(非全局变量)的值，所以要传指针


---

#### 11128 字符串与指针

 Description

请写出下列程序的运行结果


```c
#include<stdio.h>

int main( )
{  
    char string[30] = "How_are_you" ;
    char *p=&string[0],*p2=string+8;
    printf("%s,%s\n",p,p2) ;
}

```

程序运行结果为：


```c
#include <stdio.h>

int main()
{
    printf("_______________________");
}

```

 答案：

```
How_are_you,you

```

直接运行程序复制粘贴就好


我们可以看到，输出字符串的时候放一个字符串指针
 实际上就是输出从这个指针到空字符的这一段字符串


---

#### 1125 定义结构体类型

 Description

要求定义一个名为student的结构体类型，其包含如下成员：


- 字符数组name，最多可存放10个字符；
- 字符变量sex，用于记录性别；
- 整数类型变量num，用于记录学号；
- float类型变量score，用于记录成绩；

并使下列代码完整。


```c
#include <stdio.h>

_______________________

int main()
{
    struct  student stu;
    gets(stu.name);
    scanf("%c",  &stu.sex);
    scanf("%d",  &stu.num);
    scanf("%f",  &stu.score);
    printf("%s\n", stu.name);
    printf("%c\n", stu.sex);
    printf("%d\n", stu.num);
    printf("%f\n", stu.score);
    return 0;
}

```

 答案：

```c
struct student {
    char name[11];
    char sex;
    int num;
    float score;
};

```

有什么就写什么就好了


---

### 堂上练习

#### 1092 [填空]函数实现求字符串长度

 Description

下面程序实现由函数实现求字符串长度，再填空完成


```c
#include <stdio.h>

/*create function f*/

_______________________

int main()
{
    char s[80];
    int i;
    scanf("%s", s);
    i=f(s);
    printf("%d", i);
}

```

 输入样例

```
Hello!

```

 输出样例

```
6

```

 答案：

```c
int f(char *s)
{
    int i = 0;
    while(s[i] != '\0') i++;
    return i;
}

```

肯定有很多人问为什么不用`strlen`，能不能用c++的`string`类
 回答：不能
 别问，问就是试过
 这题编译不给带`strlen`，也只能用`GCC`编译，开不了`string`
 偷鸡不了一点，还是老老实实遍历吧


---

#### 1065 数组中的指针

 Description

设有如下数组定义：
 `int a[3][4]={{1,3,5,7},{9,11,13,15},{17,19,21,23}};`
 计算下面各项的值(设数组 a 的首地址为 2000 ，一个 `int`类型数占四个字节)。
 (1) a[2][1] (2)a[1] (3)a (4)a+1
 (5) *a+1 (6)*(a+1) (7)a[2]+1 (8)*(a+1)+1
 (9)*(*(a+2)+2)
 编写一个程序直接输出你的答案，一行一个。


 输出样例

```
19
2016
……
……
……

```

#### 提示

注意：


- 地址则输出地址
- 变量则输出变量值；

 输出格式

要求，一行一个答案，不允许多余空格


这题属于是有点恶心了，因为涉及到数组指针和普通指针的混用


 答案1(逻辑清晰版)：

```c
#include <stdio.h>
int main()
{
    int a[3][4]=
    {
        {1,3,5,7},  
        {9,11,13,15},   
        {17,19,21,23},
    };
    printf("%d\n",a[2][1]);
    printf("%d\n",(a[1]-a[0])*4+2000);
    printf("%d\n",(a-a)*4+2000);
    printf("%d\n",(*(a+1)-*a)*4+2000);
    printf("%d\n",((*a+1)-*a)*4+2000);
    printf("%d\n",((*(a+1))-*a)*4+2000);
    printf("%d\n",((a[2]+1)-a[0])*4+2000);
    printf("%d\n",((*(a+1)+1)-*a)*4+2000);
    printf("%d\n",*(*(a+2)+2));
    return 0; 
}

```

其实还好，只要判断出哪个是指针哪个是变量


- 变量就直接输出
- 指针就计算他和第一个指针的差，乘 4 再加上 2000 就好了

还有一个暴力输出的版本


 答案2(背答案版)：

```c
#include <stdio.h>
int main()
{
    printf("19\n");
    printf("2016\n");
    printf("2000\n");
    printf("2016\n");
    printf("2004\n");
    printf("2016\n");
    printf("2036\n");
    printf("2020\n");
    printf("21\n");
    return 0;
}

```

---

## 实验11 链表操作

### 堂上练习

#### 1099 [填空题]链表的合并

 Description

下面程序创建两个链表，然后将第二个链表合并到第一个链表未尾，但合并部分的代码未完成，请你完成这部分代码。


```c
#include <stdio.h>
#include "malloc.h"
#define LEN sizeof(struct student)

struct student
{
    long num;
    int score;
    struct student *next;
};

struct student *create(int n)
{ 
    struct student *head=NULL,*p1=NULL,*p2=NULL;
    int i;
    for(i=1;i<=n;i++)
    { 
        p1=(struct student *)malloc(LEN);
        scanf("%ld",&p1->num);   
        scanf("%d",&p1->score);   
        p1->next=NULL;
        if(i==1) head=p1;
        else p2->next=p1;
        p2=p1;
    }
    return(head);
}

struct student *merge(struct student *head, struct student *head2)
{ 
    _______________________
}

void print(struct student *head)
{
    struct student *p;
    p=head;
    while(p!=NULL)
    {
        printf("%8ld%8d",p->num,p->score);
        p=p->next;
        printf("\n");
    }
}

main()
{
    struct student *head, *head2;
    int n;
    long del_num;
    scanf("%d",&n); 
    head=create(n);
    print(head);
    scanf("%d",&n); 
    head2=create(n);
    print(head2);
    head = merge(head, head2);   
    print(head);
}

```

 输入样例

```
2           (the 1st linked list, 2 students)
1           (code of no.1 studentof the 1st linked list)
98          (score of no.1 student of the 1st linked list)
7           (code of no.2 student of the 1st linked list)
99          (score of no.2 student of the 1st linked list)
1           (the 2nd linked list, 1 student)
5           (code of no.1 student of the 2nd linked list)
87          (score of no.1 student of the 2nd linked list)

```

 输出样例

```
1 98
7 99
5 87
1 98
7 99
5 87

```

 答案：

```c
struct student *merge(struct student *head, struct student *head2)
{ 
    if(head == NULL) return head2;
    struct student *p = head;
    while(p->next != NULL) p = p->next;
    p->next = head2;
    return head;
}

```

答案写得很好
 就是遍历第一个链表到尾部
 然后把后面那个链表的头部插上去就好了


---

### 堂上练习

#### 1098 [填空]链表结点的插入

 Description

完成插入链表结点的函数(按学号顺序)，并调试通过、提交。


```c
#include <stdio.h>
#include "malloc.h"
#define LEN sizeof(struct student)

struct student
{
    long num;
    int score;
    struct student *next;
};

struct student *create(int n)
{ 
    struct student *head=NULL,*p1=NULL,*p2=NULL;
    int i;
    for(i=1;i<=n;i++)
    {  
        p1=(struct student *)malloc(LEN);
        scanf("%ld",&p1->num);   
        scanf("%d",&p1->score);   
        p1->next=NULL;
        if(i==1) head=p1;
        else p2->next=p1;
        p2=p1;
    }
    return(head);
}

void print(struct student *head)
{
    struct student *p;
    p=head;
    while(p!=NULL)
    {
        printf("%8ld%8d",p->num,p->score);
        p=p->next;
        printf("\n");
    }
}
 
struct student *insert(struct student *head, struct student *stud)
{  
    _______________________
}

main()
{
    struct student *head,*stu;
    int n;
    scanf("%d",&n);  
    head=create(n);
    print(head);
    stu=(struct student *)malloc(LEN);
    scanf("%ld",&stu->num);     
    scanf("%d",&stu->score);   
    stu->next = NULL;
    head=insert(head,stu);
    print(head);
}

```

 输入样例

```
3           (3 students)
1           (code of no.1 student)
98          (score of no.1 student)
3           (code of no.2 student)
99          (score of no.2 student)
5           (code of no.3 student)
87          (score of no.3 student)
4           (code of no.3 student needs be inserted)
77          (score of no.3 student needs be inserted)

```

 输出样例

```
1 98
3 99
5 87
1 98
3 99
4 77
5 87

```

 答案：

```c
struct student *insert(struct student *head, struct student *stud)
{  
    struct student *p , *pre;
    if(head == NULL) return stud;
    p = head;
    while (p->num < stud->num)
    {
        pre = p;
        p = p->next;
    }
    if(p == NULL) pre->next=stud;
    else
    {
        stud->next=p;
        pre->next=stud;
    }
    return head;
}

```

就是从头去遍历，找到要插入的地方插入就好了


就是要注意，找到要插入的地方的时候，要插入的节点应该是占据现在指向的节点，也就是：


- 让上一个节点指向要插入的节点
- 让要插入的节点指向被占据位置的节点

所以我们只要再创建一个指向前一个节点的指针(用于记录上一个节点)就好了


---

#### 1104 [填空题]链表的倒序

 Description

下面程序，先创建一个链表，然后调用`reverse`函数，将链表中各结点变为倒序排列。请完成`reverse`函数，


```c
#include <stdio.h>
#include "malloc.h"
#define LEN sizeof(struct student)

struct student
{
    long num;
    int score;
    struct student *next;
};

struct student *create(int n)
{ 
    struct student *head=NULL,*p1=NULL,*p2=NULL;
    int i;
    for(i=1;i<=n;i++)
    {  
        p1=(struct student *)malloc(LEN);
        scanf("%ld",&p1->num);
        scanf("%d",&p1->score);
        p1->next=NULL;
        if(i==1) head=p1;
        else p2->next=p1;
        p2=p1;
    }
    return(head);
}

void print(struct student *head)
{
    struct student *p;
    p=head;
    while(p!=NULL)
    {
        printf("%8ld%8d",p->num,p->score);
        p=p->next;
        printf("\n");
    }
}

struct student *reverse(struct student *head)
{
    _______________________
}

main()
{
    struct student *head,*stu;
    int n;
    scanf("%d",&n);  
    head=create(n);
    print(head);
    head=reverse(head);
    print(head);
}

```

 输入样例

```
3           (3 students)
1           (code of no.1 student)
98          (score of no.1 student)
4           (code of no.2 student)
99          (score of no.2 student)
5           (code of no.3 student)
87          (score of no.3 student)

```

 输出样例

```
1 98
4 99
5 87
5 87
4 99
1 98

```

 答案：

```c
struct student *reverse(struct student *head)
{
    struct student *head2 = NULL;
    if(head == NULL) return NULL;
    struct student *p = head, *p2;
    while(p != NULL)
    {
        p2 = p->next;
        p->next = head2;    
        head2 = p;  
        p = p2;
    }
    return head2;
}

```

这个链表反转最重要的是循环内“反转”的操作：
 在循环中，


- 首先保存 p 的下一个节点地址到 p2，然后将 p 的 next 指针指向 head2(即当前反转链表的末尾)。
- 这样， p 就被“摘”下来并插入到了新的链表的前面。
- 接着，将 head2 更新为 p，这样 head2 就总是指向新链表的头节点。
- 最后，将 p 更新为 p2 ，以便处理链表的下一个节点。

#### 1101 [填空题]链表的排序

 Description

下面程序，先创建一个链表(链表中各结点未按学号由小到大排序)，然后调用sort函数，将链表中各结点按学号由小到大排序。


```c
#include <stdio.h>
#include "malloc.h"
#define LEN sizeof(struct student)

struct student
{
    long num;
    int score;
    struct student *next;
};

struct student *create(int n)
{ 
    struct student *head=NULL,*p1=NULL,*p2=NULL;
    int i;
    for(i=1;i<=n;i++)
    {  
        p1=(struct student *)malloc(LEN);
        scanf("%ld",&p1->num);   
        scanf("%d",&p1->score);   
        p1->next=NULL;
        if(i==1) head=p1;
        else p2->next=p1;
        p2=p1;
    }
    return(head);
}

void print(struct student *head)
{
    struct student *p;
    p=head;
    while(p!=NULL)
    {
        printf("%8ld%8d",p->num,p->score);
        p=p->next;
        printf("\n");
    }
}

struct student *insert(struct student *head, struct student *stud)
{  
    struct student *p0,*p1,*p2;
    p1=head;
    p0=stud;
    if(head==NULL)
    {
        head=p0;
    }
    else
    { 
        while( (p0->num > p1->num) && (p1->next!=NULL) )
        { 
            p2=p1;
            p1=p1->next;
        }
        if( p0->num <= p1->num )
        {  
            if( head==p1 ) head=p0;
            else p2->next=p0;
            p0->next=p1; 
        }
        else 
        {  
            p1->next=p0;
        }
    }
    return(head);
}

struct student *del(struct student *head,long num)
{
    struct student *p1,*p2;
    p1=head;
    while(p1!=NULL)
    {
        if(p1->num == num)
        {
            if(p1 == head) head=p1->next;
            else p2->next=p1->next;
            free(p1);
            break;
        }
        p2=p1;
        p1=p1->next;
    }
    return(head);
}

struct student *sort(struct student *head)
{
    _______________________
}

main()
{
    struct student *head,*stu;
    int n;
    scanf("%d",&n);
    head=create(n);
    print(head);
    head=sort(head);
    print(head);
}

```

 输入样例

```
3           (the 1st linked list, 2 students)
1           (code of no.1 student)
98          (score of no.1 student)
7           (code of no.2 student)
99          (score of no.2 student)
5           (code of no.3 student)
87          (score of no.3 student)

```

 输出样例

```
1 98
7 99
5 87
1 98
5 87
7 99

```

 答案：

```c
struct student *sort(struct student *head)
{
    struct student *head2=NULL;
    if(head == NULL) return NULL;
    struct student *p = head, *p2;
    while(p != NULL)
    {
        p2 = p->next;
        p->next = NULL;
        head2 = insert(head2,p);
        p = p2;
    }
    return head2;
}

```

这个排序其实挺暴力的，
 就是从头到尾把每一个点拿出来，再`insert`回去(就是我们之前写的那个函数)
 使得链表有序


---

## 实验12 文件操作

### 堂前习题

#### 1105 [填空]文本文件操作_字符读入

 Description

在当前目录中存在文件名为"case1.in"的文本文件，现要求你使用fopen函数命令打开该文件，读出里面的所有字符， 遇到大写字母的，将其变为小写字母，其它字符不变，最后将所有字符按顺序在屏幕上输出。请填空完成程序， (注意，填空题，请不要使用return 0结束，否则会影响评判而判错)


(如case1.in内容如下)


```
Hello my Dear:
Have a GooD Time!

```

(在屏幕上输出结果如下)


```
hello my dear:
have a good time!

```

(提示，在提交前要测试自己的代码是否正确，可在源文件所有目录自己创建一个名为case1.in的文本文件，
 在文件中自己打入一些字母，以便测试自己的代码是否正确)


```c
#include <stdio.h>

int main()
{
    FILE *fp;
    char ch;
    if((_______________________)==NULL) return 0;
    while(_______________________)
    {
        if ('A'<=ch && ch<='Z')
            ch = ch + 32;
        _______________________;
    }
    fclose(fp);
}

```

 答案：

```c
#include <stdio.h>

int main()
{
    FILE *fp;
    char ch;

    if((fp=fopen("case1.in","r"))==NULL) return 0;
    while((ch=fgetc(fp))!=EOF)
    {
        if ('A'<=ch && ch<='Z')
            ch = ch + 32;
        putchar(ch);
    }
    fclose(fp);
}

```

没什么好说的


---

#### 1106 文本文件操作_字符写入

 Description

由键盘输入任意个字符(以连着的三个小写字符bye做为结束标志)，将所有字符(包括bye)，写入新建的文件answer.txt中(注：文件放在当前目录)。 请完成该功能，(注意，填空题，请不要使用return 0结束，否则会影响评判而判错)
 (如键盘输入内容如下)


```
He, can you write the code?
Yes, you can.bye
No, you can't.

```

(程序执行后，在文件answer.txt中内容如下)


```
He, can you write the code?
Yes, you can.bye

```

(注：因No, you can’t.在bye之后，所以不输出)
 (注：代码中不要使用return及exit()函数，以免误判)


```c
#include <stdio.h>

main()
{
_______________________
}

```

 答案：

```c
FILE *fp = fopen("answer.txt", "w");
char ch, ch1=' ', ch2=' ', ch3=' ';
while((ch=getchar())!=EOF)
{   
    fputc(ch, fp);
    ch1 = ch2;ch2 = ch3;ch3 = ch;
    if (ch1 == 'b' && ch2 == 'y' && ch3 == 'e')
        break;
}
fclose(fp);

```

没什么好说的，就是用 3 个字符存一下加个判断就好了


---

### 堂上练习

#### 11129 文本文件操作_读取与选择显示

 Description

在当前目录中存在文件名为"case1.in"的文本文件，现要求打开该文件，读出里面的所有字符，只将其中的数字字符按先后顺序显示在屏幕上。
 (如case1.in内容如下)


```
13 cats and 22 bikes

```

(在屏幕上输出结果如下)


```
1322

#include <stdio.h>

int main()
{
    FILE *fp;
    char ch;
    if((_______________________)==NULL) return 0;
    while(_______________________)
    {
        _______________________
    }
    fclose(fp);
}

```

 答案：

```c
#include <stdio.h>

int main()
{
    FILE *fp;
    char ch;
    if((fp = fopen("case1.in","r")) == NULL) return 0;
    while((ch = fgetc(fp)) != EOF)
    {
        if((ch>='0')&&(ch<='9'))
            putchar(ch);
    }
    fclose(fp);
}

```

没什么好说的，只要把上两题和前面的选择结构的题目结合一下就能写了


---

#### 1107 文本文件操作_单词的排序

 Description

在当前目录有文件“case1.in”，文件里存放有多个(总个数不超过10000个)英文单词(每个英文单词不会超过10个字文字符)， 每行一个，单词未排序。现要求，将文件中的所有单词按字典顺序排序，然后将排序好的单词写入新建的文件answer.txt中(注：文件存放于当前目录)。 请完成程序，实现该功能，(注意，填空题，请不要使用return 0结束，否则会影响评判而判错)
 (如case1.in文件中原内容如下)


```
hello
bye
yes

```

(程序执行后，在文件answer.txt中内容如下)


```
bye
hello
yes

#include <stdio.h>
#include <string.h>

int main()
{
    _______________________
}

```

 答案：

```c
    char ch[10000][11],a[11];
    FILE *fp = fopen("case1.in","r")
    FILE *fp1 = fopen("answer.txt","w");
    int i,j,n=0;
    if(fp == NULL) return 0;
    while((fscanf(fp, "%s", ch[n]))>0) n++;
    for(i=0; i<n-1; i++)
    {
        for(j=0; j<n-i-1; j++)
        {
            if(strcmp(ch[j],ch[j+1])>0)
            {
                strcpy(a,ch[j]);
                strcpy(ch[j],ch[j+1]); 
                strcpy(ch[j+1],a);
            }
        }
    }
    for(i=0;i<n;i++)
        fprintf(fp1,"%s\n",ch[i]);
    fclose(fp);
    fclose(fp1);

```

这段代码的做法主要就是使用`strcmp()`函数来进行字符串大小的比较
 排序算法是用的冒泡排序