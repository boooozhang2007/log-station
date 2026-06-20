---
title: SCAU 数据结构题目题解
date: 2026-06-10 15:56:36
tags:
  - 数据结构
  - 华南农业大学
  - 编程
mathjax: true
toc: true
---
# SCAU OJ 数据结构
> 来源：`https://acm.scau.edu.cn/uoj8000/` 数据结构栏目；抓取日期：2026-06-09。
> 共整理 129 道题。
## 目录

- **实验1**
  - [1. 8576 顺序线性表的基本操作](#1-8576-顺序线性表的基本操作)
  - [2. 8577 合并顺序表](#2-8577-合并顺序表)
  - [3. 8578 顺序表逆置](#3-8578-顺序表逆置)
  - [4. 8579 链式线性表的基本操作](#4-8579-链式线性表的基本操作)
  - [5. 8580 合并链表](#5-8580-合并链表)
  - [6. 19080 反转链表](#6-19080-反转链表)

- **拓展习题1**
  - [7. 18711 字符串去重](#7-18711-字符串去重)
  - [8. 18710 统计不同数字的个数(升级版)](#8-18710-统计不同数字的个数-升级版)
  - [9. 18927 前缀和](#9-18927-前缀和)
  - [10. 18709 魔法](#10-18709-魔法)
  - [11. 18770 差值最大](#11-18770-差值最大)
  - [12. 18708 最大子段和](#12-18708-最大子段和)
  - [13. 18063 圈中的游戏](#13-18063-圈中的游戏)
  - [14. 19079 输出链表倒数第K个元素](#14-19079-输出链表倒数第k个元素)
  - [15. 19084 万万没想到之聪明的编辑](#15-19084-万万没想到之聪明的编辑)
  - [16. 18936 手串](#16-18936-手串)
  - [17. 18925 试卷排序（双向链表）](#17-18925-试卷排序-双向链表)

- **实验2**
  - [18. 8583 顺序栈的基本操作](#18-8583-顺序栈的基本操作)
  - [19. 8584 循环队列的基本操作](#19-8584-循环队列的基本操作)
  - [20. 8585 栈的应用——进制转换](#20-8585-栈的应用-进制转换)
  - [21. 8586 括号匹配检验](#21-8586-括号匹配检验)
  - [22. 8587 行编辑程序](#22-8587-行编辑程序)
  - [23. 8588 表达式求值](#23-8588-表达式求值)
  - [24. 18938 汉诺塔问题](#24-18938-汉诺塔问题)
  - [25. 8590 队列的应用——银行客户平均等待时间](#25-8590-队列的应用-银行客户平均等待时间)
  - [26. 18937 阿克曼(Ackmann)函数](#26-18937-阿克曼-ackmann-函数)

- **拓展习题2**
  - [27. 18933 括号匹配问题](#27-18933-括号匹配问题)
  - [28. 19009 后缀表达式](#28-19009-后缀表达式)
  - [29. 18932 出栈序列合法性判定](#29-18932-出栈序列合法性判定)
  - [30. 18715 出栈序列](#30-18715-出栈序列)
  - [31. 18714 迷宫问题](#31-18714-迷宫问题)
  - [32. 19071 递归实现指数型枚举](#32-19071-递归实现指数型枚举)
  - [33. 18712 递归实现组合](#33-18712-递归实现组合)
  - [34. 18928 递归实现全排列](#34-18928-递归实现全排列)
  - [35. 19044 平分物品（递归实现指数型枚举）](#35-19044-平分物品-递归实现指数型枚举)
  - [36. 18713 整数的分解](#36-18713-整数的分解)
  - [37. 18717 舞伴问题](#37-18717-舞伴问题)
  - [38. 18719 填涂颜色](#38-18719-填涂颜色)
  - [39. 18720 迷宫问题 （最短路径）](#39-18720-迷宫问题-最短路径)
  - [40. 19118 用队列计算杨辉三角](#40-19118-用队列计算杨辉三角)
  - [41. 18718 航行](#41-18718-航行)
  - [42. 18960 素数环](#42-18960-素数环)
  - [43. 18931 分形](#43-18931-分形)
  - [44. 19070 音响外放](#44-19070-音响外放)
  - [45. 19120 病毒扩散](#45-19120-病毒扩散)

- **实验3**
  - [46. 8591 计算next值](#46-8591-计算next值)
  - [47. 8592 KMP算法](#47-8592-kmp算法)
  - [48. 18722 稀疏矩阵的运算](#48-18722-稀疏矩阵的运算)
  - [49. 18769 不完整的排序](#49-18769-不完整的排序)

- **拓展习题3**
  - [50. 18939 最长单词](#50-18939-最长单词)
  - [51. 18942 偏爱字母](#51-18942-偏爱字母)
  - [52. 18940 最小循环节（KMP算法）](#52-18940-最小循环节-kmp算法)
  - [53. 18941 压缩算法](#53-18941-压缩算法)
  - [54. 18943 小易爱回文](#54-18943-小易爱回文)
  - [55. 18964 蛇形方阵](#55-18964-蛇形方阵)
  - [56. 19072 数字字符串转化成IP地址](#56-19072-数字字符串转化成ip地址)

- **实验4**
  - [57. 8606 二叉树的构建及遍历操作](#57-8606-二叉树的构建及遍历操作)
  - [58. 17121 求二叉树各种节点数](#58-17121-求二叉树各种节点数)
  - [59. 18924 二叉树的宽度](#59-18924-二叉树的宽度)
  - [60. 18724 二叉树的遍历运算](#60-18724-二叉树的遍历运算)
  - [61. 18923 二叉树的直径](#61-18923-二叉树的直径)
  - [62. 8609 哈夫曼树](#62-8609-哈夫曼树)

- **拓展习题4**
  - [63. 18723 FBI树](#63-18723-fbi树)
  - [64. 17263 计算二叉树的第k层中所有叶子结点个数](#64-17263-计算二叉树的第k层中所有叶子结点个数)
  - [65. 18959 二叉树的之字形遍历](#65-18959-二叉树的之字形遍历)
  - [66. 19069 二叉树的右视图](#66-19069-二叉树的右视图)
  - [67. 19081 树上摘樱桃（★）](#67-19081-树上摘樱桃)
  - [68. 19083 二叉树的最长路径](#68-19083-二叉树的最长路径)
  - [69. 18946 小美的送花线路](#69-18946-小美的送花线路)
  - [70. 18929 最优二叉树](#70-18929-最优二叉树)

- **实验5**
  - [71. 8610 顺序查找](#71-8610-顺序查找)
  - [72. 8621 二分查找](#72-8621-二分查找)
  - [73. 8622 哈希查找](#73-8622-哈希查找)
  - [74. 8608 实现二叉排序树的各种算法(2)](#74-8608-实现二叉排序树的各种算法-2)

- **拓展习题5**
  - [75. 18726 查找最接近的元素](#75-18726-查找最接近的元素)
  - [76. 18935 贪吃的小Q](#76-18935-贪吃的小q)
  - [77. 19023 砍树](#77-19023-砍树)
  - [78. 18725 宇宙迁跃](#78-18725-宇宙迁跃)
  - [79. 19050 牛牛打气球](#79-19050-牛牛打气球)
  - [80. 18730 涂色问题](#80-18730-涂色问题)
  - [81. 18727 数对问题一](#81-18727-数对问题一)
  - [82. 18728 数对问题二](#82-18728-数对问题二)
  - [83. 19145 最长无重复子数组](#83-19145-最长无重复子数组)
  - [84. 18731 最接近的值](#84-18731-最接近的值)
  - [85. 18870 最佳搭配](#85-18870-最佳搭配)
  - [86. 19066 第K小子串](#86-19066-第k小子串)
  - [87. 18907 雪花 雪 雪花（哈希法）](#87-18907-雪花-雪-雪花-哈希法)
  - [88. 18908 字符串哈希](#88-18908-字符串哈希)
  - [89. 18922 最长回文子串](#89-18922-最长回文子串)
  - [90. 18944 小美的仓库整理](#90-18944-小美的仓库整理)
  - [91. 18716 出栈序列（数据加强版）](#91-18716-出栈序列-数据加强版)
  - [92. 19008 哈希表](#92-19008-哈希表)
  - [93. 19040 序列合并](#93-19040-序列合并)
  - [94. 18873 团队实力](#94-18873-团队实力)

- **实验6**
  - [95. 8638 直接插入排序](#95-8638-直接插入排序)
  - [96. 8639 折半插入排序](#96-8639-折半插入排序)
  - [97. 8640 希尔(shell)排序](#97-8640-希尔-shell-排序)
  - [98. 8641 冒泡排序](#98-8641-冒泡排序)
  - [99. 8642 快速排序](#99-8642-快速排序)
  - [100. 8643 简单选择排序](#100-8643-简单选择排序)
  - [101. 8644 堆排序](#101-8644-堆排序)
  - [102. 8645 归并排序（非递归算法）](#102-8645-归并排序-非递归算法)
  - [103. 8646 基数排序](#103-8646-基数排序)

- **拓展习题6**
  - [104. 18746 逆序数](#104-18746-逆序数)
  - [105. 18967 六一儿童节](#105-18967-六一儿童节)
  - [106. 18962 区间合并](#106-18962-区间合并)
  - [107. 18963 最大数字](#107-18963-最大数字)
  - [108. 18965 找到 K 个最接近的元素](#108-18965-找到-k-个最接近的元素)
  - [109. 18966 两两配对差值最小](#109-18966-两两配对差值最小)
  - [110. 18961 最大点的集合](#110-18961-最大点的集合)
  - [111. 19018 正则序列](#111-19018-正则序列)
  - [112. 18958 有趣的排序](#112-18958-有趣的排序)
  - [113. 19065 有趣的数字](#113-19065-有趣的数字)

- **实验7**
  - [114. 8647 实现图的存储结构](#114-8647-实现图的存储结构)
  - [115. 8648 图的深度遍历](#115-8648-图的深度遍历)
  - [116. 8649 图的广度遍历](#116-8649-图的广度遍历)
  - [117. 18448 最小生成树](#117-18448-最小生成树)
  - [118. 18732 最短路问题](#118-18732-最短路问题)
  - [119. 18734 拓扑排序](#119-18734-拓扑排序)
  - [120. 18747 关键路径](#120-18747-关键路径)

- **拓展习题7**
  - [121. 19085 图的存储结构（邻接表）](#121-19085-图的存储结构-邻接表)
  - [122. 19082 中位特征值](#122-19082-中位特征值)
  - [123. 19031 树的重心](#123-19031-树的重心)
  - [124. 19011 小猿的依赖循环](#124-19011-小猿的依赖循环)
  - [125. 19017 编译依赖问题(拓扑排序）](#125-19017-编译依赖问题-拓扑排序)
  - [126. 19032 树上上升序列](#126-19032-树上上升序列)
  - [127. 18733 排队](#127-18733-排队)
  - [128. 18945 小团的配送团队](#128-18945-小团的配送团队)
  - [129. 19049 仓库配送](#129-19049-仓库配送)

---

# 实验1

## 1. 8576 顺序线性表的基本操作

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8576&access=68a6196588059146b04178f3bdefa8d9&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
编写算法，创建初始化容量为LIST_INIT_SIZE的顺序表T，并实现插入、删除、遍历操作。本题目给出部分代码，请补全内容。

#include<stdio.h>
#include<malloc.h>
#define OK 1
#define ERROR 0
#define LIST_INIT_SIZE 100
#define LISTINCREMENT 10
#define ElemType int

typedef struct
{
	int *elem;
	int length;
	int listsize;
}SqList;

int InitList_Sq(SqList &L)
{
// 算法2.3，构造一个空的线性表L，该线性表预定义大小为LIST_INIT_SIZE
// 请补全代码

}

int Load_Sq(SqList &L)
{
// 输出顺序表中的所有元素
	int i;
	if(_________________________) printf("The List is empty!");  // 请填空
	else
	{
		printf("The List is: ");
		for(_________________________) printf("%d ",_________________________);  // 请填空
	}
	printf("\n");
	return OK;
}

int ListInsert_Sq(SqList &L,int i,int e)
{
// 算法2.4，在顺序线性表L中第i个位置之前插入新的元素e
// i的合法值为1≤i≤L.length +1
// 请补全代码

}

int ListDelete_Sq(SqList &L,int i, int &e)
{
// 算法2.5,在顺序线性表L中删除第i个位置的元素，并用e返回其值
// i的合法值为1≤i≤L.length
// 请补全代码

}

int main()
{
	SqList T;
	int a, i;
	ElemType e, x;
	if(_________________________)    // 判断顺序表是否创建成功
	{
		printf("A Sequence List Has Created.\n");
	}
	while(1)
	{
		printf("1:Insert element\n2:Delete element\n3:Load all elements\n0:Exit\nPlease choose:\n");
		scanf("%d",&a);
		switch(a)
		{
			case 1: scanf("%d%d",&i,&x);
					if(_________________________) printf("Insert Error!\n"); // 执行插入函数，根据返回值判断i值是否合法
					else printf("The Element %d is Successfully Inserted!\n", x);
					break;
			case 2: scanf("%d",&i);
					if(_________________________) printf("Delete Error!\n"); // 执行删除函数，根据返回值判断i值是否合法
					else printf("The Element %d is Successfully Deleted!\n", e);
					break;
			case 3: Load_Sq(T);
					break;
			case 0: return 1;
		}
	}
}
```

**输入**

```
测试样例格式说明：
根据菜单操作：
1、输入1，表示要实现插入操作，紧跟着要输入插入的位置和元素，用空格分开
2、输入2，表示要实现删除操作，紧跟着要输入删除的位置
3、输入3，表示要输出顺序表的所有元素
4、输入0，表示程序结束
```

**样例输入**

```
1
1 2
1
1 3
2
1
3
0
```

**样例输出**

```
A Sequence List Has Created.
1:Insert element
2:Delete element
3:Load all elements
0:Exit
Please choose:
The Element 2 is Successfully Inserted!
1:Insert element
2:Delete element
3:Load all elements
0:Exit
Please choose:
The Element 3 is Successfully Inserted!
1:Insert element
2:Delete element
3:Load all elements
0:Exit
Please choose:
The Element 3 is Successfully Deleted!
1:Insert element
2:Delete element
3:Load all elements
0:Exit
Please choose:
The List is: 2
1:Insert element
2:Delete element
3:Load all elements
0:Exit
Please choose:
```

**解析**

**题目要求**：实现一个支持动态扩容的顺序表，提供插入、删除、遍历三种基本操作。

**数据结构**：顺序表使用一段连续内存 `elem`（即动态数组）存放元素，并配有两个辅助变量——`length` 记录当前元素个数，`listsize` 记录已申请的存储容量。需要注意：逻辑位序从 1 开始计数，而数组下标从 0 开始，因此**第 i 个元素存放在 `elem[i-1]`**，二者相差 1。

**解题思路**：
- **初始化**：申请可容纳 `LIST_INIT_SIZE` 个元素的存储空间，并将元素个数置为 0。
- **插入**（在第 i 个位置插入元素 e）：① 首先检查位序是否合法，合法范围为 1 至 `length+1`（取 `length+1` 表示允许在表尾追加）；② 若存储空间已满，则按增量 `LISTINCREMENT` 进行扩容；③ 将第 i 位及其后的元素整体后移一格以腾出空位，此步骤**必须从后向前移动**，否则前一个元素会覆盖后一个元素，导致数据丢失；④ 将元素 e 写入第 i 位，元素个数加 1。
- **删除**（删除第 i 个元素，并通过引用参数 e 返回其值）：先将待删元素存入 e，再将其后的元素整体前移一格以覆盖空位，元素个数减 1。
- **遍历**：若表为空则输出提示信息，否则依次打印各元素。

**算法分析**：插入与删除均涉及元素搬移，时间复杂度为 O(n)；遍历的时间复杂度为 O(n)。

**注意事项**：① 搬移方向不可颠倒——插入时从后向前移动、删除时从前向后移动；② 第 i 个元素对应的数组下标为 `i-1`，注意下标转换；③ 插入前须先判断存储空间是否已满并进行扩容；④ 插入位序的上界为 `length+1`，而非 `length`。

**C++ 参考答案**

```cpp
#include <malloc.h>
#include <stdio.h>
#define OK 1
#define ERROR 0
#define LIST_INIT_SIZE 100
#define LISTINCREMENT 10
#define ElemType int

typedef struct {
    int *elem;
    int length;
    int listsize;
} SqList;

int InitList_Sq(SqList &L) {
    // 算法2.3，构造一个空的线性表L，该线性表预定义大小为LIST_INIT_SIZE
    L.elem = (ElemType *)malloc(LIST_INIT_SIZE * sizeof(ElemType));
    if (!L.elem)
        return ERROR;
    L.length = 0;
    L.listsize = LIST_INIT_SIZE;
    return OK;
}

int Load_Sq(SqList &L) {
    // 输出顺序表中的所有元素
    int i;
    if (L.length == 0)
        printf("The List is empty!");
    else {
        printf("The List is: ");
        for (i = 0; i < L.length; i++)
            printf("%d ", L.elem[i]);
    }
    printf("\n");
    return OK;
}

int ListInsert_Sq(SqList &L, int i, int e) {
    // 算法2.4，在顺序线性表L中第i个位置之前插入新的元素e
    // i的合法值为1≤i≤L.length +1
    if (i < 1 || i > L.length + 1)
        return ERROR;
    if (L.length >= L.listsize) {
        ElemType *newbase =
            (ElemType *)realloc(L.elem, (L.listsize + LISTINCREMENT) * sizeof(ElemType));
        if (!newbase)
            return ERROR;
        L.elem = newbase;
        L.listsize += LISTINCREMENT;
    }
    for (int k = L.length - 1; k >= i - 1; k--)
        L.elem[k + 1] = L.elem[k];
    L.elem[i - 1] = e;
    L.length++;
    return OK;
}

int ListDelete_Sq(SqList &L, int i, int &e) {
    // 算法2.5,在顺序线性表L中删除第i个位置的元素，并用e返回其值
    // i的合法值为1≤i≤L.length
    if (i < 1 || i > L.length)
        return ERROR;
    e = L.elem[i - 1];
    for (int k = i; k < L.length; k++)
        L.elem[k - 1] = L.elem[k];
    L.length--;
    return OK;
}

int main() {
    SqList T;
    int a, i;
    ElemType e, x;
    if (InitList_Sq(T) == OK) // 判断顺序表是否创建成功
    {
        printf("A Sequence List Has Created.\n");
    }
    while (1) {
        printf("1:Insert element\n2:Delete element\n3:Load all elements\n0:Exit\nPlease choose:\n");
        scanf("%d", &a);
        switch (a) {
        case 1:
            scanf("%d%d", &i, &x);
            if (ListInsert_Sq(T, i, x) == ERROR)
                printf("Insert Error!\n");
            else
                printf("The Element %d is Successfully Inserted!\n", x);
            break;
        case 2:
            scanf("%d", &i);
            if (ListDelete_Sq(T, i, e) == ERROR)
                printf("Delete Error!\n");
            else
                printf("The Element %d is Successfully Deleted!\n", e);
            break;
        case 3:
            Load_Sq(T);
            break;
        case 0:
            return 0;
        }
    }
}
```

## 2. 8577 合并顺序表

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8577&access=ef1ca086d92a1a0af82e1940d996bcc9&fixedLanguage=MA==
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++

**题目描述**

```
若线性表中数据元素相互之间可以比较，且数据元素在表中按值递增或递减，则称该表为有序表。

编写算法，将两个非递减有序顺序表A和B合并成一个新的非递减有序顺序表C。
```

**输入**

```
第一行：顺序表A的元素个数
第二行：顺序表A的各元素（非递减），用空格分开
第三行：顺序表B的元素个数
第四行：顺序表B的各元素（非递减），用空格分开
```

**输出**

```
第一行：顺序表A的元素列表
第二行：顺序表B的元素列表
第三行：合并后顺序表C的元素列表
```

**样例输入**

```
5
1 3 5 7 9
5
2 4 6 8 10
```

**样例输出**

```
List A:1 3 5 7 9
List B:2 4 6 8 10
List C:1 2 3 4 5 6 7 8 9 10

Hint

输出时注意大小写和标点。
```

**解析**

**题目要求**：将两个已按非递减顺序排列的序列 A 和 B 合并为一个新的非递减有序序列 C。

**解题思路——双指针归并**：本题的核心是归并排序中的合并步骤。使用两个指针 `i`、`j` 分别指向序列 A、B 的当前比较位置，每次比较 `A[i]` 与 `B[j]`，将较小者依次存入结果序列 C，并将对应指针后移一位。重复此过程，直至两个序列均被遍历完毕。由于 A、B 本身有序，按此方式归并得到的序列 C 也必然有序。

**收尾处理**：当其中一个序列先被遍历完毕时，将另一个序列的剩余元素直接全部复制到 C 的末尾。代码中条件 `j==nb` 即用于判断序列 B 是否已遍历完毕——若是，则直接取序列 A 的剩余元素。

**算法分析**：每个元素仅被访问一次，时间复杂度为 O(n+m)。

**C++ 参考答案**

```cpp
#include <iostream>
#include <vector>
using namespace std;
// 打印辅助函数：先输出序列名称（如 "List A:"），再依次输出各元素，元素间以空格分隔
void print(const char *name, const vector<int> &a) {
    cout << name;
    for (int x : a)
        cout << x << ' ';
    cout << '\n';
}
int main() {
    // 读入有序序列 A 和 B
    int na, nb;
    cin >> na;
    vector<int> A(na);
    for (int &i : A)
        cin >> i;
    cin >> nb;
    vector<int> B(nb);
    for (int &i : B)
        cin >> i;
    vector<int> C;
    int i = 0, j = 0; // C 用于存放合并结果，i、j 分别为 A、B 的当前遍历位置
    while (i < na || j < nb) { // 当 A 或 B 中仍有未处理元素时继续循环
        // 选取较小元素存入 C：若 B 已遍历完毕(j==nb)，或 A 的当前元素不大于 B 的当前元素，则取
        // A；否则取 B
        if (j == nb || (i < na && A[i] <= B[j]))
            C.push_back(A[i++]);
        else
            C.push_back(B[j++]);
    }
    print("List A:", A);
    print("List B:", B);
    print("List C:", C);
    return 0;
}
```
**邪修做法（可过 OJ）**

利用题目只要求最终 C 有序，直接把 A、B 全部放进 C 后排序；不利用“两个表本来有序”的条件，代码更短但时间复杂度变为 O((n+m)log(n+m))。

~~~cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;

void print(const char *name, const vector<int> &a) {
    cout << name;
    for (int x : a)
        cout << x << ' ';
    cout << '\n';
}

int main() {
    int na, nb;
    cin >> na;
    vector<int> A(na);
    for (int &x : A)
        cin >> x;
    cin >> nb;
    vector<int> B(nb), C = A;
    for (int &x : B) {
        cin >> x;
        C.push_back(x);
    }
    sort(C.begin(), C.end());
    print("List A:", A);
    print("List B:", B);
    print("List C:", C);
}
~~~


## 3. 8578 顺序表逆置

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8578&access=a0f75afc614ed99b394875b25f6c2055&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
顺序表的基本操作代码如下：
#include<stdio.h>
#include<malloc.h>
#define OK 1
#define ERROR 0
#define LIST_INIT_SIZE 100
#define LISTINCREMENT 10
#define ElemType int

typedef int Status;
typedef struct
{
    int *elem;
    int length;
    int listsize;
}SqList;

Status InitList_Sq(SqList &L)
{  // 算法2.3
  // 构造一个空的线性表L。
  L.elem = (ElemType *)malloc(LIST_INIT_SIZE*sizeof(ElemType));
  if (!L.elem) return OK;        // 存储分配失败
  L.length = 0;                  // 空表长度为0
  L.listsize = LIST_INIT_SIZE;   // 初始存储容量
  return OK;
} // InitList_Sq

Status ListInsert_Sq(SqList &L, int i, ElemType e)
{  // 算法2.4
  // 在顺序线性表L的第i个元素之前插入新的元素e，
  // i的合法值为1≤i≤ListLength_Sq(L)+1
  ElemType *p;
  if (i < 1 || i > L.length+1) return ERROR;  // i值不合法
  if (L.length >= L.listsize) {   // 当前存储空间已满，增加容量
    ElemType *newbase = (ElemType *)realloc(L.elem,
                  (L.listsize+LISTINCREMENT)*sizeof (ElemType));
    if (!newbase) return ERROR;   // 存储分配失败
    L.elem = newbase;             // 新基址
    L.listsize += LISTINCREMENT;  // 增加存储容量
  }
  ElemType *q = &(L.elem[i-1]);   // q为插入位置
  for (p = &(L.elem[L.length-1]); p>=q; --p) *(p+1) = *p;
                                  // 插入位置及之后的元素右移
  *q = e;       // 插入e
  ++L.length;   // 表长增1
  return OK;
} // ListInsert_Sq

Status ListDelete_Sq(SqList &L, int i, ElemType &e)
{  // 算法2.5
  // 在顺序线性表L中删除第i个元素，并用e返回其值。
  // i的合法值为1≤i≤ListLength_Sq(L)。
  ElemType *p, *q;
  if (i<1 || i>L.length) return ERROR;  // i值不合法
  p = &(L.elem[i-1]);                   // p为被删除元素的位置
  e = *p;                               // 被删除元素的值赋给e
  q = L.elem+L.length-1;                // 表尾元素的位置
  for (++p; p<=q; ++p) *(p-1) = *p;     // 被删除元素之后的元素左移
  --L.length;                           // 表长减1
  return OK;
} // ListDelete_Sq

设有一顺序表A=（a0,a1,..., ai,...an-1)，其逆顺序表定义为A'=( an-1,..., ai,...,a1, a0)。设计一个算法，将顺序表逆置，要求顺序表仍占用原顺序表的空间。
```

**输入**

```
第一行：输入顺序表的元素个数
第二行：输入顺序表的各元素，用空格分开
```

**输出**

```
第一行：逆置前的顺序表元素列表
第二行：逆置后的顺序表元素列表
```

**样例输入**

```
10
1 2 3 4 5 6 7 8 9 10
```

**样例输出**

```
The List is:1 2 3 4 5 6 7 8 9 10
The turned List is:10 9 8 7 6 5 4 3 2 1
```

**解析**

**题目要求**：将顺序表中的元素进行原地逆置（即首尾元素依次对调），并输出逆置后的结果。

**解题思路——首尾双指针法**：在题目给出的顺序表结构基础上，设置两个下标分别指向表头和表尾，交换两端元素后同时向中间移动，当两下标相遇时停止。该过程只在原顺序表空间内完成，不额外开数组。

**算法分析**：仅需遍历数组的前半部分，时间复杂度为 O(n)。

**注意事项**：输出格式须与题目要求严格一致——逆置前的输出前缀为 `The List is:`，逆置后的输出前缀为 `The turned List is:`，冒号后无空格，各元素之间以空格分隔。

**C++ 参考答案**

```cpp
#include <malloc.h>
#include <stdio.h>
#define OK 1
#define ERROR 0
#define LIST_INIT_SIZE 100
#define LISTINCREMENT 10
#define ElemType int

typedef int Status;
typedef struct {
    int *elem;
    int length;
    int listsize;
} SqList;

Status InitList_Sq(SqList &L) { // 算法2.3
    L.elem = (ElemType *)malloc(LIST_INIT_SIZE * sizeof(ElemType));
    if (!L.elem)
        return ERROR;
    L.length = 0;
    L.listsize = LIST_INIT_SIZE;
    return OK;
}

Status ListInsert_Sq(SqList &L, int i, ElemType e) { // 算法2.4
    ElemType *p;
    if (i < 1 || i > L.length + 1)
        return ERROR;
    if (L.length >= L.listsize) {
        ElemType *newbase =
            (ElemType *)realloc(L.elem, (L.listsize + LISTINCREMENT) * sizeof(ElemType));
        if (!newbase)
            return ERROR;
        L.elem = newbase;
        L.listsize += LISTINCREMENT;
    }
    ElemType *q = &(L.elem[i - 1]);
    for (p = &(L.elem[L.length - 1]); p >= q; --p)
        *(p + 1) = *p;
    *q = e;
    ++L.length;
    return OK;
}

Status ListDelete_Sq(SqList &L, int i, ElemType &e) { // 算法2.5
    ElemType *p, *q;
    if (i < 1 || i > L.length)
        return ERROR;
    p = &(L.elem[i - 1]);
    e = *p;
    q = L.elem + L.length - 1;
    for (++p; p <= q; ++p)
        *(p - 1) = *p;
    --L.length;
    return OK;
}

Status Reverse_Sq(SqList &L) {
    for (int i = 0, j = L.length - 1; i < j; i++, j--) {
        ElemType t = L.elem[i];
        L.elem[i] = L.elem[j];
        L.elem[j] = t;
    }
    return OK;
}

void Load_Sq(SqList L, const char *prefix) {
    printf("%s", prefix);
    for (int i = 0; i < L.length; i++)
        printf("%d ", L.elem[i]);
    printf("\n");
}

int main() {
    SqList A;
    int n;
    ElemType e;
    InitList_Sq(A);
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        scanf("%d", &e);
        ListInsert_Sq(A, i, e);
    }
    Load_Sq(A, "The List is:");
    Reverse_Sq(A);
    Load_Sq(A, "The turned List is:");
    return 0;
}
```

## 4. 8579 链式线性表的基本操作

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8579&access=089acd422a98158cdd18d8240a84e003&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
编写算法，创建一个含有n个元素的带头结点的单链表L并实现插入、删除、遍历操作。本题目提供部分代码，请补全内容。

#include<stdio.h>
#include<malloc.h>
#define ERROR 0
#define OK 1
#define ElemType int

typedef struct LNode
{
 int data;
 struct LNode *next;
}LNode,*LinkList;

int CreateLink_L(LinkList &L,int n){
// 创建含有n个元素的单链表
  LinkList p,q;
  int i;
  ElemType e;
  L = new LNode;
  L->next = NULL;              // 先建立一个带头结点的单链表
  q = L;
  for (i=0; i<n; i++) {
    scanf("%d", &e);
    p = new LNode;  // 生成新结点
    // 请补全代码

  }
  return OK;
}

int LoadLink_L(LinkList &L){
// 单链表遍历
 LinkList p = L->next;
 if(___________________________)printf("The List is empty!"); // 请填空
 else
 {
	 printf("The LinkList is:");
	 while(___________________________)    // 请填空
	 {
		printf("%d ",p->data);
		___________________________    // 请填空
	 }
 }
 printf("\n");
 return OK;
}

int LinkInsert_L(LinkList &L,int i,ElemType e){
// 算法2.9
// 在带头结点的单链线性表L中第i个位置之前插入元素e
// 请补全代码

}

int LinkDelete_L(LinkList &L,int i, ElemType &e){
// 算法2.10
// 在带头结点的单链线性表L中，删除第i个元素，并用e返回其值
// 请补全代码

}

int main()
{
 LinkList T;
 int a,n,i;
 ElemType x, e;
 printf("Please input the init size of the linklist:\n");
 scanf("%d",&n);
 printf("Please input the %d element of the linklist:\n", n);
 if(___________________________)     // 判断链表是否创建成功，请填空
 {
	 printf("A Link List Has Created.\n");
	 LoadLink_L(T);
 }
 while(1)
	{
		printf("1:Insert element\n2:Delete element\n3:Load all elements\n0:Exit\nPlease choose:\n");
		scanf("%d",&a);
		switch(a)
		{
			case 1: scanf("%d%d",&i,&x);
				  if(___________________________) printf("Insert Error!\n"); // 判断i值是否合法，请填空
				  else printf("The Element %d is Successfully Inserted!\n", x);
				  break;
			case 2: scanf("%d",&i);
				  if(___________________________) printf("Delete Error!\n"); // 判断i值是否合法，请填空
				  else printf("The Element %d is Successfully Deleted!\n", e);
				  break;
			case 3: LoadLink_L(T);
				  break;
			case 0: return 1;
		}
	}
}
```

**输入**

```
测试样例格式说明：
根据菜单操作：
1、输入1，表示要实现插入操作，紧跟着要输入插入的位置和元素，用空格分开
2、输入2，表示要实现删除操作，紧跟着要输入删除的位置
3、输入3，表示要输出顺序表的所有元素
4、输入0，表示程序结束
```

**样例输入**

```
3
3 6 9
3
1
4 12
2
1
3
0
```

**样例输出**

```
Please input the init size of the linklist:
Please input the 3 element of the linklist:
A Link List Has Created.
The LinkList is:3 6 9
1:Insert element
2:Delete element
3:Load all elements
0:Exit
Please choose:
The LinkList is:3 6 9
1:Insert element
2:Delete element
3:Load all elements
0:Exit
Please choose:
The Element 12 is Successfully Inserted!
1:Insert element
2:Delete element
3:Load all elements
0:Exit
Please choose:
The Element 3 is Successfully Deleted!
1:Insert element
2:Delete element
3:Load all elements
0:Exit
Please choose:
The LinkList is:6 9 12
1:Insert element
2:Delete element
3:Load all elements
0:Exit
Please choose:
```

**解析**

**题目要求**：使用带头结点的单链表实现建表、插入、删除、遍历四种基本操作。

**关于"带头结点"**：在链表最前端设置一个**不存放数据的哨兵结点**（即头结点），实际数据从其后继结点开始存储。其优点在于：对第 1 个数据结点的插入或删除操作与中间结点的处理方式完全一致，无需对边界情况进行单独处理，从而使代码更为统一简洁。

**解题思路**：
- **建表（尾插法）**：使用尾指针 `q` 始终指向链表的最后一个结点，每读入一个新元素便将其链接到 `q` 之后，再令 `q` 指向新结点。以此方式建立的链表中元素顺序与输入顺序一致（若采用头插法则会产生逆序）。
- **在第 i 个位置之前插入**：关键在于先定位到**第 i-1 个结点** `p`（从头结点开始后移 i-1 步），再将新结点链接到 `p` 之后——首先令新结点的 next 指针指向 `p` 原本的后继结点，然后令 `p` 的 next 指向新结点。两步操作的顺序不可颠倒，否则将丢失后续链表。
- **删除第 i 个结点**：同样先定位到第 i-1 个结点 `p`，令其跨过待删结点（即 `p->next = q->next`），最后释放被删结点所占内存。
- **遍历**：从头结点的后继开始，逐个向后访问并打印各结点的数据。

**算法分析**：定位第 i 个结点需要后移 i 步，因此插入与删除操作的时间复杂度均为 O(n)。

**注意事项**：① 应定位到"第 i-1 个结点"而非第 i 个结点——单链表只能沿 next 指针单向后移，修改指针的操作必须在其前驱结点上进行；② 修改指针时须注意顺序：先令新结点连接后继，再断开原有连接。

**C++ 参考答案**

```cpp
#include <malloc.h>
#include <stdio.h>
#define ERROR 0
#define OK 1
#define ElemType int

typedef struct LNode {
    int data;
    struct LNode *next;
} LNode, *LinkList;

int CreateLink_L(LinkList &L, int n) {
    // 创建含有n个元素的单链表
    LinkList p, q;
    int i;
    ElemType e;
    L = new LNode;
    L->next = NULL; // 先建立一个带头结点的单链表
    q = L;
    for (i = 0; i < n; i++) {
        scanf("%d", &e);
        p = new LNode; // 生成新结点
        p->data = e;
        p->next = NULL;
        q->next = p;
        q = p;
    }
    return OK;
}

int LoadLink_L(LinkList &L) {
    // 单链表遍历
    LinkList p = L->next;
    if (p == NULL)
        printf("The List is empty!");
    else {
        printf("The LinkList is:");
        while (p != NULL) {
            printf("%d ", p->data);
            p = p->next;
        }
    }
    printf("\n");
    return OK;
}

int LinkInsert_L(LinkList &L, int i, ElemType e) {
    // 算法2.9
    // 在带头结点的单链线性表L中第i个位置之前插入元素e
    LinkList p = L, s;
    int j = 0;
    while (p && j < i - 1) {
        p = p->next;
        ++j;
    }
    if (!p || j > i - 1)
        return ERROR;
    s = new LNode;
    s->data = e;
    s->next = p->next;
    p->next = s;
    return OK;
}

int LinkDelete_L(LinkList &L, int i, ElemType &e) {
    // 算法2.10
    // 在带头结点的单链线性表L中，删除第i个元素，并用e返回其值
    LinkList p = L, q;
    int j = 0;
    while (p->next && j < i - 1) {
        p = p->next;
        ++j;
    }
    if (!(p->next) || j > i - 1)
        return ERROR;
    q = p->next;
    p->next = q->next;
    e = q->data;
    delete q;
    return OK;
}

int main() {
    LinkList T;
    int a, n, i;
    ElemType x, e;
    printf("Please input the init size of the linklist:\n");
    scanf("%d", &n);
    printf("Please input the %d element of the linklist:\n", n);
    if (CreateLink_L(T, n) == OK) // 判断链表是否创建成功
    {
        printf("A Link List Has Created.\n");
        LoadLink_L(T);
    }
    while (1) {
        printf("1:Insert element\n2:Delete element\n3:Load all elements\n0:Exit\nPlease choose:\n");
        scanf("%d", &a);
        switch (a) {
        case 1:
            scanf("%d%d", &i, &x);
            if (LinkInsert_L(T, i, x) == ERROR)
                printf("Insert Error!\n");
            else
                printf("The Element %d is Successfully Inserted!\n", x);
            break;
        case 2:
            scanf("%d", &i);
            if (LinkDelete_L(T, i, e) == ERROR)
                printf("Delete Error!\n");
            else
                printf("The Element %d is Successfully Deleted!\n", e);
            break;
        case 3:
            LoadLink_L(T);
            break;
        case 0:
            return 0;
        }
    }
}
```

## 5. 8580 合并链表

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8580&access=f0a3acfca47d97b5305ca4e3a9cd7446&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
线性链表的基本操作如下：
#include<stdio.h>
#include<malloc.h>
#define ERROR 0
#define OK 1
#define ElemType int

typedef int Status;
typedef struct LNode
{
 int data;
 struct LNode *next;
}LNode,*LinkList;

Status ListInsert_L(LinkList &L, int i, ElemType e) {  // 算法2.9
  // 在带头结点的单链线性表L的第i个元素之前插入元素e
  LinkList p,s;
  p = L;
  int j = 0;
  while (p && j < i-1) {  // 寻找第i-1个结点
    p = p->next;
    ++j;
  }
  if (!p || j > i-1) return ERROR;      // i小于1或者大于表长
  s = (LinkList)malloc(sizeof(LNode));  // 生成新结点
  s->data = e;  s->next = p->next;      // 插入L中
  p->next = s;
  return OK;
} // LinstInsert_L

Status ListDelete_L(LinkList &L, int i, ElemType &e) {  // 算法2.10
  // 在带头结点的单链线性表L中，删除第i个元素，并由e返回其值
  LinkList p,q;
  p = L;
  int j = 0;
  while (p->next && j < i-1) {  // 寻找第i个结点，并令p指向其前趋
    p = p->next;
    ++j;
  }
  if (!(p->next) || j > i-1) return ERROR;  // 删除位置不合理
  q = p->next;
  p->next = q->next;           // 删除并释放结点
  e = q->data;
  free(q);
  return OK;
} // ListDelete_L

设计一个算法将两个非递减有序链表A和B合并成一个新的非递减有序链表C。
```

**输入**

```
第一行：单链表A的元素个数
第二行：单链表A的各元素（非递减），用空格分开
第三行：单链表B的元素个数
第四行：单链表B的各元素（非递减），用空格分开
```

**输出**

```
第一行：单链表A的元素列表
第二行：单链表B的元素列表
第三行：合并后单链表C的元素列表
```

**样例输入**

```
6
12 24 45 62 84 96
4
15 31 75 86
```

**样例输出**

```
List A:12 24 45 62 84 96
List B:15 31 75 86
List C:12 15 24 31 45 62 75 84 86 96
```

**解析**

**题目要求**：将两个非递减有序链表 A、B 合并为一个新的非递减有序链表 C。

**解题思路**：在题目给出的单链表结构基础上进行**有序归并**。使用两个指针分别遍历链表 A 和 B，每次选取当前值较小的结点接到链表 C 的尾部，并移动相应指针。

**链表实现方案**：维护链表 C 的尾指针，每次比较 A、B 当前结点的值，将较小者从原链表中取出并链接至 C 的尾部。当某一链表遍历完毕后，将另一链表的剩余部分直接拼接到 C 的末尾。全程时间复杂度为 O(n+m)，且无需额外创建新结点。

**算法分析**：每个结点仅被访问一次，时间复杂度为 O(n+m)。

**C++ 参考答案**

```cpp
#include <malloc.h>
#include <stdio.h>
#define ERROR 0
#define OK 1
#define ElemType int

typedef int Status;
typedef struct LNode {
    int data;
    struct LNode *next;
} LNode, *LinkList;

Status ListInsert_L(LinkList &L, int i, ElemType e) { // 算法2.9
    LinkList p, s;
    p = L;
    int j = 0;
    while (p && j < i - 1) {
        p = p->next;
        ++j;
    }
    if (!p || j > i - 1)
        return ERROR;
    s = (LinkList)malloc(sizeof(LNode));
    s->data = e;
    s->next = p->next;
    p->next = s;
    return OK;
}

Status ListDelete_L(LinkList &L, int i, ElemType &e) { // 算法2.10
    LinkList p, q;
    p = L;
    int j = 0;
    while (p->next && j < i - 1) {
        p = p->next;
        ++j;
    }
    if (!(p->next) || j > i - 1)
        return ERROR;
    q = p->next;
    p->next = q->next;
    e = q->data;
    free(q);
    return OK;
}

Status CreateList_L(LinkList &L, int n) {
    L = (LinkList)malloc(sizeof(LNode));
    L->next = NULL;
    LinkList r = L;
    for (int i = 0; i < n; i++) {
        ElemType e;
        scanf("%d", &e);
        LinkList p = (LinkList)malloc(sizeof(LNode));
        p->data = e;
        p->next = NULL;
        r->next = p;
        r = p;
    }
    return OK;
}

void PrintList(const char *name, LinkList L) {
    printf("%s", name);
    for (LinkList p = L->next; p != NULL; p = p->next)
        printf("%d ", p->data);
    printf("\n");
}

Status MergeList_L(LinkList A, LinkList B, LinkList &C) {
    C = (LinkList)malloc(sizeof(LNode));
    LinkList pa = A->next, pb = B->next, pc = C;
    while (pa && pb) {
        if (pa->data <= pb->data) {
            pc->next = pa;
            pc = pa;
            pa = pa->next;
        } else {
            pc->next = pb;
            pc = pb;
            pb = pb->next;
        }
    }
    pc->next = pa ? pa : pb;
    return OK;
}

int main() {
    int n, m;
    LinkList A, B, C;
    scanf("%d", &n);
    CreateList_L(A, n);
    scanf("%d", &m);
    CreateList_L(B, m);
    PrintList("List A:", A);
    PrintList("List B:", B);
    MergeList_L(A, B, C);
    PrintList("List C:", C);
    return 0;
}
```

## 6. 19080 反转链表

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19080&access=288a9eb525010a3646802e843f779f2f&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
一道经典的题目

给定一个单链表的头结点L，长度为n，反转该链表后，返回新链表的表头。

要求：空间复杂度 O(1) ，时间复杂度 O(n)。

如当输入链表{1,2,3}时，
经反转后，原链表变为{3,2,1}，所以对应的输出为{3,2,1}。

    #include <iostream>//C++
using namespace std;
struct LNode
{
    int data;
    LNode * next;
};
void createList(LNode * &L,int n)
{
    /**< 尾插法创建单链表 */
    LNode *r, *p;
    r=L=new LNode;/**< 创建头结点 */
    L->next=NULL;
    for(int i=1; i<=n; i++)
    {
        p=new LNode;
        cin>>p->data;
        p->next=NULL;
        r->next=p;
        r=p;
    }
}
void trv(LNode * L)
{
    /**< 一个简单的链表遍历函数，供编程过程中测试使用 */
    L=L->next;
    while(L)
    {
        cout<<L->data<<' ';
        L=L->next;
    }
}
void reverseList(LNode * &L)
{

        _______________________

}
int main()
{
    int n;
    LNode *L;
    cin>>n;
    createList(L,n);
    reverseList(L);
    trv(L);
    return 0;
}
```

**输入**

```
第一行一个整数n，代表链表长度。
第二行n个整数。
```

**输出**

```
输出逆置后的单链表。
```

**样例输入**

```
5
1 2 3 4 5
```

**样例输出**

```
5 4 3 2 1
```

**解析**

**题目要求**：将单链表进行原地反转——要求空间复杂度 O(1)、时间复杂度 O(n)，即不得额外创建新链表，仅通过修改现有结点的指针来完成。

**解题思路——三指针迭代法**：沿链表依次遍历，维护三个指针：`prev`（已反转部分的表头）、`curr`（当前正在处理的结点）、`next`（预先保存 `curr` 的后继结点，以防止修改指针后丢失后续链表）。每一步执行以下四个操作：
1. `next = curr->next`：**先保存后继结点**，因为下一步将修改 `curr->next` 的指向，若不提前保存则无法继续遍历剩余链表；
2. `curr->next = prev`：将当前结点的 next 指针**反向**，令其指向前驱结点——这是实现"反转"的核心操作；
3. `prev = curr`：已反转部分的表头向后推进一位；
4. `curr = next`：当前处理位置向后推进一位。

当 `curr` 为空时，`prev` 即为反转后的新表头，最后令头结点的 next 指向 `prev` 即可。

**关键要点**：第 2 步将改写 `curr->next` 的值，因此**必须在执行第 2 步之前通过第 1 步保存原始后继**，否则将丢失链表的剩余部分。

**算法分析**：每个结点仅被遍历一次，时间复杂度为 O(n)；仅使用常数个指针变量，空间复杂度为 O(1)。

**C++ 参考答案**

```cpp
#include <iostream> //C++
using namespace std;
struct LNode {
    int data;
    LNode *next;
};
void createList(LNode *&L, int n) {
    /**< 尾插法创建单链表 */
    LNode *r, *p;
    r = L = new LNode; /**< 创建头结点 */
    L->next = NULL;
    for (int i = 1; i <= n; i++) {
        p = new LNode;
        cin >> p->data;
        p->next = NULL;
        r->next = p;
        r = p;
    }
}
void trv(LNode *L) {
    /**< 一个简单的链表遍历函数，供编程过程中测试使用 */
    L = L->next;
    while (L) {
        cout << L->data << ' ';
        L = L->next;
    }
}
void reverseList(LNode *&L) {

    //-------------该行开始是填空的内容--------------
    // 若链表无数据结点或仅有一个数据结点，则无需反转，直接返回
    if (L->next == NULL || L->next->next == NULL)
        return;
    LNode *prev = NULL;    // 前驱指针，指向已反转部分的表头
    LNode *curr = L->next; // 当前指针，从第一个数据结点开始遍历
    LNode *next = NULL;    // 后继指针，用于暂存当前结点的后继结点
    while (curr != NULL) {
        next = curr->next; // 先保存后继结点，防止修改指针后丢失后续链表
        curr->next = prev; // 将当前结点的 next 指针反向，指向前驱结点
        prev = curr;       // 已反转部分的表头向后推进一位
        curr = next;       // 当前处理位置向后推进一位
    }
    // 令头结点的 next 指向反转后的新首元结点（即原链表的末结点）
    L->next = prev;
    //-------------该行之上是填空的内容--------------
}
int main() {
    int n;
    LNode *L;
    cin >> n;
    createList(L, n);
    reverseList(L);
    trv(L);
    return 0;
}
```

**邪修做法（可过 OJ）**

OJ 只检查最终输出时，不必真的建立和反转链表；读入数组后倒序输出即可。这个写法不满足题面 O(1) 空间要求，但通常能过纯输入输出评测。

~~~cpp
#include <iostream>
#include <vector>
using namespace std;

int main() {
    int n;
    cin >> n;
    vector<int> a(n);
    for (int &x : a)
        cin >> x;
    for (int i = n - 1; i >= 0; i--)
        cout << a[i] << ' ';
}
~~~

# 拓展习题1

## 7. 18711 字符串去重

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18711&access=b841871ec73d91adc7f9440cb5da86e6&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
一个完全由小写字母组成的长度为n的字符串，现在要求你去除所有重复的字母，并将剩下的字母按从小到大的次序输出。
如输入baaadccaab，输出abcd。
```

**输入**

```
第一行一个整数n，表示字符串长度(0<=n<=100000)。
第二行一个字符串。
```

**输出**

```
去除所有重复的字母，并将剩下的字母按ASCII码从小到大的次序输出。
```

**样例输入**

```
10
baaadccaab
```

**样例输出**

```
abcd
```

**解析**

**题目要求**：给定一个仅由小写字母组成的字符串，去除其中所有重复的字母，将剩余字母按字母表升序输出。例如 `baaadccaab` → `abcd`。

**解题思路——桶计数法**：开辟一个大小为 256 的整型数组 `list[256]`（足以覆盖全部 ASCII 字符），以字符本身作为**下标**，每读入一个字符便在对应位置将计数加 1。输入完毕后，从 `'a'` 到 `'z'` 顺序扫描数组，凡计数非零的位置即表示该字母在原串中出现过，依次输出即可得到升序结果。

**算法分析**：在 C++ 中，字符本质上是以其 ASCII 码值存储的整数，因此 `list['a']` 等价于 `list[97]`，可以直接将字符用作数组下标。这正是"计数数组（桶）"的典型应用。时间复杂度为 O(n + 26)，其中 n 为字符串长度，26 为字母表大小；空间复杂度为 O(256)，即常数级别。

**C++ 参考答案**

```cpp
#include <iostream>
#include <stdio.h>
using namespace std;

int main() {
    int list[256] = {0}; // 计数数组：下标为字符的 ASCII 值，值为该字符出现的次数，初始化为 0
    int n;
    cin >> n;

    for (int i = 0; i < n; i++) {
        char cha;
        cin >> cha;
        list[cha]++; // 以字符的 ASCII 值为下标，对应位置的计数加 1
    }

    // 按字母表顺序（'a' 到 'z'）扫描，计数非零说明该字母出现过，依次输出
    for (int i = 'a'; i <= 'z'; i++) {
        if (list[i] != 0)
            cout << (char)i; // 循环变量 i 为整型，需强制转换为 char 类型方可输出为字母
    }
}
```
**邪修做法（可过 OJ）**

小写字母只有 26 个，也可以直接丢进 `set`，让容器自动去重和排序。

~~~cpp
#include <iostream>
#include <set>
using namespace std;

int main() {
    int n;
    string s;
    cin >> n >> s;
    set<char> st(s.begin(), s.end());
    for (char c : st)
        cout << c;
}
~~~


## 8. 18710 统计不同数字的个数(升级版)

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18710&access=9699673a83df874a853126e01e304305&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
由键盘输入n个整数，统计不同数字的个数（0<=n<=200000）。

PS：此题目和1040仅数据规模不同。但如果使用如下O(n2)级别的算法必然会超时。
int main()
{
    int a[21],i,c=0,b,j;
    for(i=1;i<=20;i++)
    {
        cin>>b;
        for(j=1;j<=c;j++)
        {
            if(b==a[j])
            {
                break;
            }
        }
        if(j>c)
        {
            a[c+1]=b;
            c++;
        }
    }
    cout<<c;
    return 0;
}
```

**输入**

```
第一行一个整数n（0<=n<=200000）。
第二行n个整数a1，a2......an,（0<=ai<=200000）。
```

**输出**

```
仅一行，不同数字的个数。
```

**样例输入**

```
20
70  5  14  22  19  2  99  67  13  66  5  93  44  38  22  11  39  22  33  11
```

**样例输出**

```
16

Hint

如何快速判断某个数字是否在之前出现过？
因为题目告知ai的范围，所以可以开一个bool数组记录数字是否出现（C语言用整型数组）。
例如a[1]=35，设定t[a[1]]=1，即t[35]变为1,。
这样当需要"判断某个数字是否在之前出现过"时，利用数组随机访问的特点可以O（1）的时间得到结果。
```

**解析**

**题目要求**：输入 n 个整数，统计其中**不同数字**的个数。

**解题思路——桶标记法**：题目给定数字范围为 0 ~ 200000，数值范围有限，因此可以开辟一个足够大的数组作为"标记表"——每读入一个数 k，便在 `list[k]` 处进行标记。全部读入后，统计数组中非零位置的个数，即为不同数字的个数。

**算法分析**：若采用二重循环（每读入一个数就与之前所有数逐一比较），时间复杂度为 O(n^2)，当 n 最大为 200000 时必然超时。而使用标记表判断"某数是否出现过"仅需 O(1) 的随机访问时间，整体时间复杂度降为 O(n)。

**注意事项**：此方法的前提是**数值范围不大**（数组能够容纳）。若数值可达 10^9，则需改用哈希表，或先排序再比较相邻元素。

**C++ 参考答案**

```cpp
#include <stdio.h>

int main() {
    int list[200001] = {0}; // 标记数组：list[k] 记录数字 k 出现的次数，下标范围覆盖 0~200000
    int n;
    int num = 0; // 用于统计不同数字的个数
    scanf("%d", &n);

    for (int i = 0; i < n; i++) {
        int k;
        scanf("%d", &k);
        list[k]++; // 以读入的数字 k 为下标，标记其出现
    }

    // 遍历标记数组，统计非零位置的个数，即为不同数字的个数
    for (int i = 0; i < 200001; i++) {
        if (list[i] != 0)
            num++;
    }

    printf("%d", num);
    return 0;
}
```
**邪修做法（可过 OJ）**

值域虽然可开桶，但直接用 `set` 统计不同元素也能过；代码短，复杂度是 O(nlogn)。

~~~cpp
#include <iostream>
#include <set>
using namespace std;

int main() {
    int n, x;
    cin >> n;
    set<int> st;
    while (n--) {
        cin >> x;
        st.insert(x);
    }
    cout << st.size();
}
~~~


## 9. 18927 前缀和

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18927&access=5198435c227bf2b19421761f5adb6882&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
前缀和是一种重要的预处理方法，能极大地降低查询序列区间和的时间复杂度。
现在一个序列中有n个整数，下标从1....n。
有m个查询，每个查询给出一个区间的左右端点下标，请输出这个区间所有数据的和。

注意当题目输入输出数据量比较大时，用cin和cout速度会比较慢，容易超时。解决方法：
（1）用scanf和printf替换
（2）main函数第一条语句加上std::ios::sync_with_stdio(false); 关闭同步会使cin cout速度加快。
```

**输入**

```
第一行一个整数n。(1<=n<=100000)
第二行n个整数，用空格分隔，int范围。
第三行一个整数m。(1<=m<=100000)
下面m行每行两个整数L，R。（1<=L<=R<=n）
```

**输出**

```
输出共m行，每行一个整数为对应区间[L,R]的序列和。
注意序列和的数据范围可能超出int范围。
```

**样例输入**

```
5
3 -8 4 5 1
4
3 3
1 1
2 4
1 3
```

**样例输出**

```
4
3
1
-1

Hint

在读入数据后，用一个sum数组来记录从第1个元素到第i个元素的和，for(i=1;i<=n;i++)  sum[i]=sum[i-1]+a[i];
这样区间[L,R]的和可以用sum[R]-sum[L-1]得到。
```

**解析**

**题目要求**：给定一个包含 n 个整数的序列以及 m 次查询，每次查询给出区间 [L, R]，要求输出该区间内所有元素之和。

**解题思路——前缀和预处理**：若每次查询都遍历区间 [L, R] 进行累加，m 次查询的最坏时间复杂度为 O(n * m)，将会超时。前缀和的核心思想是**预处理**：令 `s[i]` 表示前 i 个元素的累加和（递推关系为 `s[i] = s[i-1] + a[i]`），则任意区间 [L, R] 之和可用 `s[R] - s[L-1]` 一次减法求得，单次查询时间复杂度降为 O(1)。

**算法分析**：公式 `s[R] - s[L-1]` 的正确性在于——`s[R]` 为前 R 个元素之和，`s[L-1]` 为前 L-1 个元素之和，二者相减恰好保留第 L 至第 R 个元素。预处理时间复杂度为 O(n)，单次查询为 O(1)。

**注意事项**：(1) 区间和可能超出 int 的表示范围，前缀和数组需使用 `long long` 类型存储；(2) 数据量较大时应使用 `scanf/printf`，或通过 `std::ios::sync_with_stdio(false)` 关闭同步流以加速 `cin/cout`，否则容易超时。

**C++ 参考答案**

```cpp
#include <stdio.h>

int main() {
    int n, m, l, r;
    int a[100000] = {0};
    long long s[100000] = {0}; // 前缀和数组，使用 long long 类型以防止累加时溢出
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        scanf("%d", &a[i]);
        s[i] = s[i - 1] + a[i]; // 递推计算前缀和：s[i] = 前 i 个元素之和
    }

    scanf("%d", &m);
    for (int i = 1; i <= m; i++) {
        scanf("%d%d", &l, &r);
        printf("%lld\n", s[r] - s[l - 1]); // 区间 [l, r] 之和 = s[r] - s[l-1]
    }
}
```

## 10. 18709 魔法

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18709&access=9140b8fd56dbd4e8a570bcb204f6e91c&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
农夫约翰的奶牛场有很多奶牛，奶牛有黑白两种颜色。现在奶牛们排成整齐的一列去参加镇上的游行活动。
约翰希望白色奶牛都排在前面，黑色的奶牛都排在后面。但现在队列中奶牛的颜色是混乱的，并且奶牛们都不愿意改变位置。
幸运的是，约翰有一根魔法棒，每挥舞一次魔法棒就可以改变一头奶牛的颜色。
请问，约翰至少要挥舞多少次魔法棒，才能将队列改成他希望的状态。注意，可以将所有的奶牛都变成白色，或者都变成黑色。
```

**输入**

```
第一行一个正整数n，表示奶牛的头数。(1<=n<=200000)。
第二行n个正整数，均为1或2，1表示白色奶牛，2表示黑色奶牛。
```

**输出**

```
一个正整数，表示挥舞魔法棒的最少次数。
```

**样例输入**

```
7
2 2 1 1 1 2 1
```

**样例输出**

```
3

Hint

可以把1和2号奶牛变成1,7号奶牛变成2，或者全部奶牛变成1，最少需要3次。
```

**解析**

**题目要求**：给定一排黑白奶牛的颜色序列（1 表示白色、2 表示黑色），每次操作可改变一头奶牛的颜色，求使**所有白牛排在前面、黑牛排在后面**所需的最少操作次数（允许全白或全黑的极端情况）。

**解题思路——枚举分界点 + 前缀统计**：最终的目标队列必然呈"前段全白、后段全黑"的形式，区别仅在于**分界点**的位置。设分界点将序列分为前、后两段，则操作代价 = 前段中黑牛的数量（需改为白色）+ 后段中白牛的数量（需改为黑色）。枚举全部 n+1 个可能的分界位置（含最左端和最右端），取其中代价最小者即为答案。

**算法分析**：为高效计算各分界点的代价，可从"分界点在最左端（即全黑）"的初始状态出发——此时代价等于白牛的总数。分界点每右移一位，相当于将一头奶牛从"后段"并入"前段"：若该奶牛为黑色，则前段新增一个需要改为白色的对象（`t1++`）；若为白色，则后段减少一个需要改为黑色的对象（`t2--`）。如此逐步移动并更新代价，每步仅需 O(1) 时间。

**复杂度**：仅需一遍扫描，时间复杂度为 O(n)。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
using namespace std;

int main() {
    int n, n1 = 0;
    cin >> n;
    int list[200000] = {0};

    for (int i = 0; i < n; i++) {
        cin >> list[i];
        if (list[i] == 1)
            n1++; // 统计白色奶牛的总数量
    }

    int n2 = n - n1; // 计算黑色奶牛的总数量

    // 初始状态：分界点在最左端（即假设全为黑色），统计后段中需要改为黑色的白牛数
    int t1 = 0;  // 前段中需要改为白色的黑牛数（初始时前段为空，故为 0）
    int t2 = n1; // 后段中需要改为黑色的白牛数（初始时所有白牛均在后段）

    int ans = t1 + t2; // 记录当前最小代价（全黑情况的代价）

    // 从左至右枚举分界点，逐步将元素从后段移入前段
    for (int i = 0; i < n; i++) {
        // 将第 i 个元素从后段并入前段
        if (list[i] == 2) {
            t1++; // 前段新增一头黑牛，需要改为白色
        } else {
            t2--; // 后段减少一头白牛，无需再改为黑色
        }

        ans = min(ans, t1 + t2); // 更新全局最小代价
    }

    cout << ans << endl;
    return 0;
}
```

## 11. 18770 差值最大

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18770&access=4a738b94fc3d327b694ed5a5b8193068&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
一个长度为N的整数序列，找出两个数x和y使x-y的值最大。
要求在序列中x必须在y的右侧。
```

**输入**

```
第一行是一个正整数N，表示了序列的长度（0<=N<=200000）。
第二行包含N个绝对值不大于10000的整数ai。
```

**输出**

```
一个整数，为最大的差值。数据确保结果在类型int范围内。
```

**样例输入**

```
7
4 -4 3 -1 2 -4 3
```

**样例输出**

```
7
```

**解析**

**题目要求**：在序列中寻找两个数 x 和 y，要求 **x 位于 y 的右侧**（即 x 的下标大于 y 的下标），使得 x - y 的值最大。

**解题思路——遍历时维护左侧最小值**：为使差值 x - y 尽可能大，对于每一个作为 x 的位置，应使其左侧的 y 尽可能小。因此，可以从左向右遍历序列，同时维护一个变量 `mn` 记录"截至当前位置所见过的最小值"。每读入一个新元素 x，先用 `x - mn` 更新答案（此时 `mn` 一定位于 x 的左侧，满足位置约束），再将 x 纳入 `mn` 的更新范围。

**算法分析**：遍历至位置 i 时，`mn` 必定是前 i 个元素中的最小值，因此 `x - mn` 即为"以第 i 个元素为右端"所能取得的最大差值。对所有右端取最大值，便可得到全局最优解。

**注意事项**：当 n <= 1 时无法构成合法的数对，应直接输出 0。时间复杂度为一遍扫描 O(n)。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
using namespace std;
int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr); // 关闭同步流，加速输入输出
    int n;
    if (!(cin >> n))
        return 0;
    if (n <= 0) {
        cout << 0;
        return 0;
    } // 无元素时差值视为 0
    int x;
    cin >> x;
    int mn = x, ans = (-2147483647 - 1); // mn：遍历过程中左侧已见的最小值；ans：全局最大差值
    for (int i = 1; i < n; i++) {
        cin >> x;
        ans = max(ans, x - mn); // 以当前元素 x 为右端，用 x - mn 更新最大差值
        mn = min(mn, x);        // 将当前元素纳入左侧最小值的更新范围
    }
    cout << (n == 1 ? 0 : ans); // 仅 1 个元素时无法构成合法数对，输出 0
}
```

## 12. 18708 最大子段和

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18708&access=b20ef6e76812eeebb52ae1e681246da4&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
一个整数序列，选出其中连续且非空的一段使得这段和最大。

注意当题目要求输入输出的数据量很大时，尽量使用scanf和printf。
c++提供的cin和cout速度比较慢，有可能在读取数据和输出数据时导致超时。
```

**输入**

```
第一行是一个正整数N，表示了序列的长度（0=<N<=200000）。
第二行包含N个绝对值不大于10000的整数ai。
```

**输出**

```
一个整数，为最大的子段和。子段的最小长度为1。数据确保结果在类型int范围内。
```

**样例输入**

```
7
2 -4 3 -1 2 -4 3
```

**样例输出**

```
4

Hint

【样例说明】
2,-4,3,-1,2,-4,3中，最大的子段和为4，该子段为第三元素至第五元素，即3,-1,2。
```

**解析**

**题目要求**：在一个整数序列中选取一段**连续且非空**的子序列，使其元素之和最大（即经典的"最大子段和"问题）。

**解题思路——Kadane 算法（动态规划）**：用变量 `cur` 表示"**以当前元素结尾**的最大子段和"。每遇到一个新元素 x，有两种选择：将其接续在前一段之后（`cur + x`），或者从 x 自身另起一段（`x`），取二者中较大者，即 `cur = max(x, cur + x)`。同时用变量 `best` 记录遍历过程中 `cur` 所达到的最大值，即为最终答案。

**算法分析**：该算法的核心直觉是——若前面累积的子段和 `cur` 已经为负数，则它只会拖累后续元素的累加结果，不如果断舍弃、从当前元素重新开始。这正是 `max(x, cur + x)` 所体现的决策逻辑。时间复杂度为一遍扫描 O(n)。由于累加和可能较大，建议使用 `long long` 类型。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
using namespace std;
int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    int n;
    cin >> n;
    long long best = (-(1LL << 60)), cur = 0,
              x; // best：全局最大子段和；cur：以当前元素结尾的最大子段和
    for (int i = 0; i < n; i++) {
        cin >> x;
        cur = (i == 0 ? x : max(x, cur + x)); // 决策：接续前一段，还是从当前元素另起一段
        best = max(best, cur);                // 用当前结尾的最优值更新全局答案
    }
    cout << best;
}
```

## 13. 18063 圈中的游戏

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18063&access=6e6ed06917286f00a9602d1ff60d1989&fixedLanguage=MDsxOzI=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC

**题目描述**

```
有n个人围成一圈，从第1个人开始报数1、2、3，每报到3的人退出圈子。编程使用链表找出最后留下的人。
```

**输入**

```
输入一个数n，1000000>=n>0
```

**输出**

```
输出最后留下的人的编号
```

**样例输入**

```
3
```

**样例输出**

```
2
```

**解析**

**题目要求**：n 个人围成一圈，从第 1 个人开始报数，每报到 3 的人出局，求最后留下的人的编号（经典**约瑟夫问题**，k = 3）。

**解题思路——约瑟夫递推公式**：若使用链表模拟逐一删除的过程，时间复杂度为 O(n * k)，当 n 达到 10^6 时效率偏低。约瑟夫问题存在 O(n) 的递推解法：设 `f(i)` 表示 i 个人时最后幸存者的编号（编号从 0 开始），则递推关系为：
- `f(1) = 0`（仅剩 1 人时，幸存者编号为 0）；
- `f(i) = (f(i-1) + k) % i`（本题中 k = 3）。

**算法分析**：递推公式的直观理解是——每淘汰一人后，剩余的 i-1 人构成一个规模更小的同类子问题；将子问题的解"向后偏移 k 个位置"再对 i 取模，即可还原为当前规模下的编号。

**注意事项**：递推所得结果为从 0 开始的编号，而题目要求从 1 开始编号，因此最终输出应为 `f(n) + 1`。时间复杂度为 O(n)，空间复杂度为 O(1)。

**C++ 参考答案**

```cpp
#include <iostream>
using namespace std;
int main() {
    long long n;
    cin >> n;
    long long ans = 0; // 初始值 f(1) = 0：仅 1 人时幸存者的 0 基编号为 0
    for (long long i = 1; i <= n; i++)
        ans = (ans + 3) % i; // 约瑟夫递推：f(i) = (f(i-1) + 3) % i（i=1 时结果恰为 0）
    cout << ans + 1;         // 将 0 基编号转换为题目要求的 1 基编号
}
```

## 14. 19079 输出链表倒数第K个元素

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19079&access=17518c47c46539b62ab0ac724846601e&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
输入一个长度为 n 的链表，设链表中的元素的值为 ai ，输出该链表中倒数第k个节点。
如果该链表长度小于k，输出-1。

    #include <iostream>//C++
using namespace std;
struct LNode
{
    int data;
    LNode * next;
};
void createList(LNode * &L,int n)
{/**< 尾插法创建单链表 */
    LNode *r, *p;
    r=L=new LNode;/**< 创建头结点 */
    L->next=NULL;
    for(int i=1;i<=n;i++)
    {
        p=new LNode;
        cin>>p->data;
        p->next=NULL;
        r->next=p;
        r=p;
    }
}
void trv(LNode * L)
{ /**< 一个简单的链表遍历函数，供编程过程中测试使用 */
    L=L->next;
    while(L)
    {
        cout<<L->data<<' ';
        L=L->next;
    }
}
int getK(LNode * L,int k)
{
   _______________________
}
int main()
{
    int n,k;
    LNode *L;
    cin>>n>>k;
    createList(L,n);
    //trv(L);
    cout<<getK(L,k);
    return 0;
}
```

**输入**

```
第一行两个整数，分别为n和k。
第二行n个整数。
```

**输出**

```
倒数第k个元素，如果不存在，输出-1。
```

**样例输入**

```
5 2
1 2 3 4 5
```

**样例输出**

```
4
```

**解析**

**题目要求**：输出链表中倒数第 k 个结点的值；若链表长度不足 k，则输出 -1。

**解题思路一——下标换算**：将元素读入数组后，倒数第 k 个元素即正数第 n - k + 1 个元素，对应数组下标为 `n - k`（下标从 0 计）。参考答案即采用此法，实现最为直接。

**解题思路二——快慢指针（链表经典技巧）**：若限定只使用链表结构、不借助额外数组，可令快指针先行 k 步，之后快慢指针同步前进；当快指针到达链表末尾时，慢指针恰好停在倒数第 k 个结点的位置。仅需一次遍历即可完成，空间复杂度为 O(1)。

**注意事项**：当 `k < 1` 或 `k > n` 时均属于"不存在"的情况，应输出 -1。

**C++ 参考答案**

```cpp
#include <iostream>
#include <vector>
using namespace std;
int main() {
    int n, k;
    cin >> n >> k;
    vector<int> a(n);
    for (int &i : a)
        cin >> i;
    if (k < 1 || k > n)
        cout << -1; // 链表长度不足或 k 值非法，输出 -1
    else
        cout << a[n - k]; // 倒数第 k 个元素对应数组下标 n-k
}
```
**邪修做法（可过 OJ）**

本题标准答案本身已经是捷径：OJ 按输入输出判题，不强制真的建链表，因此直接读入数组并输出 `a[n-k]` 即可。


## 15. 19084 万万没想到之聪明的编辑

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19084&access=fcfd21affc4d423a46ece096136f19fb&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
字节跳动2019春招研发部分编程题
我叫王大锤，是一家出版社的编辑。我负责校对投稿来的英文稿件，这份工作非常烦人，因为每天都要去修正无数的拼写错误。
但是，优秀的人总能在平凡的工作中发现真理。我发现一个发现拼写错误的捷径：

1. 三个同样的字母连在一起，一定是拼写错误，去掉一个的就好啦：比如 helllo -> hello
2. 两对一样的字母（AABB型）连在一起，一定是拼写错误，去掉第二对的一个字母就好啦：比如 helloo -> hello
3. 上面的规则优先"从左到右"匹配，即如果是AABBCC，虽然AABB和BBCC都是错误拼写，应该优先考虑修复AABB，结果为AABCC

我特喵是个天才！我在蓝翔学过挖掘机和程序设计，按照这个原理写了一个自动校对器，工作效率从此起飞。
用不了多久，我就会出任CEO，当上董事长，迎娶白富美，走上人生巅峰，想想都有点小激动呢！
……
万万没想到，我被开除了，临走时老板对我说： "做人做事要兢兢业业、勤勤恳恳、本本分分，人要是行，
干一行行一行。一行行行行行；要是不行，干一行不行一行，一行不行行行不行。" 我现在整个人红红火火恍恍惚惚的……

请听题：请实现大锤的自动校对程序
```

**输入**

```
第一行包括一个数字N，表示本次用例包括多少个待校验的字符串。1<=N<=50

后面跟随N行，每行为一个待校验的字符串。字符串长度不超过1000。
```

**输出**

```
N行，每行包括一个被修复后的字符串。
```

**样例输入**

```
2
helloo
wooooooow
```

**样例输出**

```
hello
woow

Hint

题目数据范围可以用暴力算法O（n^2）完成。但本题目作法很多，仅从数据结构角度看，用链表或栈结构都可以在O（n）的复杂度解决此问题。
```

**解析**

**题目要求**：按照以下两条规则修正字符串——规则一：三个相同字母连续出现（AAA 型），则删去其中一个；规则二：两对相同字母连续出现（AABB 型），则删去后一对中的一个。匹配规则时遵循"从左到右优先"的原则。

**解题思路——边构造边检查（结果串充当栈）**：维护一个结果串 `r`，将原串中的字符逐个尝试加入。在加入每个字符 `c` 之前，先检查 `r` 的尾部是否会产生违规模式：
- 若 `r` 末尾已有两个连续的 `c`（即末两位均为 c），再加入便构成 AAA 模式 → **跳过**该字符；
- 若 `r` 末位为 `c`，且倒数第 2、3 位相等（形如 `...XXc`），再加入 c 将构成 `XXcc`（AABB 模式）→ **跳过**该字符；
- 否则正常将 c 追加到结果串末尾。

**算法分析**：由于始终基于"已修正的结果串"自左向右进行判断，天然满足"从左到右优先"的匹配要求。结果串 `r` 仅访问和修改尾部元素，其本质等价于一个栈结构。每个字符仅处理一次，时间复杂度为 O(字符串长度)。

**C++ 参考答案**

```cpp
#include <iostream>
#include <string>
using namespace std;
int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    int T;
    cin >> T;
    while (T--) {
        string s, r; // r 为边构造边修正的结果串，充当栈的角色（仅访问和修改尾部）
        cin >> s;
        for (char c : s) {
            int n = r.size();
            // 规则一：结果串末尾已有两个 c，再加入将构成 AAA 模式，跳过该字符
            if (n >= 2 && r[n - 1] == c && r[n - 2] == c)
                continue;
            // 规则二：结果串末位为 c 且倒数第 2、3 位相等（形如 ...XXc），再加入 c 将构成 AABB
            // 模式，跳过
            if (n >= 3 && r[n - 1] == c && r[n - 2] == r[n - 3])
                continue;
            r.push_back(c); // 不触发任何规则，正常追加到结果串末尾
        }
        cout << r << "\n";
    }
}
```

## 16. 18936 手串

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18936&access=5f6e84a95e294cda337808f00b4682f3&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
字节跳动2018校招Android方向（第二批）
作为一个手串艺人，有金主向你订购了一条包含n个杂色串珠的手串——每个串珠要么无色，要么涂了若干种颜色。
为了使手串的色彩看起来不那么单调，金主要求，手串上的任意一种颜色（不包含无色），在任意连续的m个串珠里至多出现一次（注意这里手串是一个环形）。
手串上的颜色一共有c种。现在按顺时针序告诉你n个串珠的手串上，每个串珠用所包含的颜色分别有哪些。
请你判断该手串上有多少种颜色不符合要求。即询问有多少种颜色在任意连续m个串珠中出现了至少两次。
```

**输入**

```
第一行输入n，m，c三个数，用空格隔开。(1 <= n <= 10000, 1 <= m <= 1000, 1 <= c <= 50)
接下来n行每行的第一个数num_i(0 <= num_i <= c)表示第i颗珠子有多少种颜色。接下来依次读入num_i个数字，每个数字x表示第i颗柱子上包含第x种颜色(1 <= x <= c)
```

**输出**

```
一个非负整数，表示该手链上有多少种颜色不符需求。
```

**样例输入**

```
5 2 3
3 1 2 3
0
2 2 3
1 2
1 3
```

**样例输出**

```
2

Hint

第一种颜色出现在第1颗串珠，与规则无冲突。
第二种颜色分别出现在第 1，3，4颗串珠，第3颗与第4颗串珠相邻，所以不合要求。
第三种颜色分别出现在第1，3，5颗串珠，第5颗串珠的下一个是第1颗，所以不合要求。
总计有2种颜色的分布是有问题的。
这里第2颗串珠是透明的。
```

**解析**

**题目要求**：给定一条环形手串，其上 n 颗珠子各带有若干种颜色，要求统计有多少种颜色违反了规则——即某种颜色在**任意连续 m 颗**珠子中出现了至少两次。

**解题思路——按颜色收集位置并检查相邻间距**：对于每种颜色，将其出现的所有珠子位置按顺序记录下来。某种颜色"违规"的充要条件是：存在**两次出现位置之间的（环形）距离小于 m**——因为距离小于 m 就意味着存在一个长度为 m 的连续窗口能够同时覆盖这两次出现。具体检查方法如下：
- 相邻两次出现（非首尾）：若 `v[i] - v[i-1] < m`，则违规；
- 环形首尾衔接：最后一次绕回第一次的距离为 `v[0] + n - v.back()`，若该值小于 m，同样违规。

只要存在任一对相邻间距小于 m，该颜色即计入答案。

**算法分析**：之所以只需检查"相邻"两次出现就足够，是因为同一种颜色的出现位置已经排好序，其中距离最近的一对最为"危险"；若最近的一对距离都 >= m，则更远的位置对必然也 >= m。所有颜色的出现次数之和即为总标记数，时间复杂度为 O(总标记数 + c)。

**C++ 参考答案**

```cpp
#include <iostream>
#include <vector>
using namespace std;
int main() {
    int n, m, c;
    cin >> n >> m >> c;
    vector<vector<int>> pos(c + 1); // pos[x]：记录颜色 x 出现在哪些珠子上的位置列表（按输入顺序）
    for (int i = 1; i <= n; i++) {
        int k, x;
        cin >> k; // 第 i 颗珠子包含 k 种颜色
        while (k--) {
            cin >> x;
            pos[x].push_back(i);
        } // 依次记录每种颜色所在的珠子编号
    }
    int ans = 0;
    for (int col = 1; col <= c; col++) {
        auto &v = pos[col];
        if (v.size() < 2)
            continue; // 该颜色出现不足 2 次，不可能违规
        bool bad = false;
        for (size_t i = 1; i < v.size(); i++)
            if (v[i] - v[i - 1] < m)
                bad = true; // 相邻两次出现位置的距离 < m，违规
        if (v[0] + n - v.back() < m)
            bad = true; // 环形首尾衔接处的距离 < m，违规
        ans += bad;
    }
    cout << ans;
}
```

## 17. 18925 试卷排序（双向链表）

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18925&access=6d91f185fcef6213afcc3dd47427bfe2&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
老师要将N张试卷重新排序，每张试卷都有编号为1∼N，采取如下的方法：
先将编号1的试卷放进队列，剩下从第2张到第N张依次放入队列，
放入的时候老师会把编号i的试卷插入到编号为x试卷之前或之后（x<i）,
在老师完成这N-1次操作之后，请输出试卷序列的最终编号。
```

**输入**

```
第1行为一个正整数N，表示了有N张试卷。

第2-N行，第i行包含两个整数x,p，其中x为小于i的正整数，p为0或者1。
若p为0，则表示将编号为i的试卷放入编号为x试卷的左边，为1则放入x试卷的右边。
```

**输出**

```
输出N个整数，表示完成插入后试卷系列中试卷的编号（1<=N<=100000）。
```

**样例输入**

```
4
1 0
2 1
1 0
```

**样例输出**

```
2 3 4 1

Hint

4张试卷。第二行1,0,将编号2的试卷放入编号1的左边，则序列为2  1；
第三行2,1，将编号3试卷放入编号2试卷的右边，则序列为2 3 1；
第四行1 0，将编号4的试卷放入编号1的左边，则序列为2 3 4 1。
```

**解析**

**题目要求**：从编号 1 开始，依次将编号 2 ~ N 的试卷插入到"某个已有编号 x 的左边或右边"，最终从左到右输出整个序列。

**解题思路——数组模拟双向链表**：由于插入操作频繁发生在序列的中间位置，双向链表是最为合适的数据结构（每次插入的时间复杂度为 O(1)）。本题无需使用指针，而是用两个数组 `L[i]` 和 `R[i]` 分别记录编号 i 的**左邻居**和**右邻居**，另用变量 `head` 记录当前序列最左端的编号。
- **插入到 x 的左边**：新结点 i 的右邻居为 x，左邻居为 x 原来的左邻居；若 x 原本有左邻居，则让该左邻居的右指针指向 i，否则说明 i 成为新的队首（更新 `head`）；最后让 x 的左指针指向 i。
- **插入到 x 的右边**：对称地处理即可。

**算法分析**：编号本身为 1 ~ N 的连续整数，可直接用作数组下标，无需动态分配内存，既高效又简洁。每次插入操作仅需修改常数次指针引用，时间复杂度为 O(1)，n 次插入的总时间复杂度为 O(n)。

**输出方式**：从 `head` 出发，沿 `R[]` 数组向右遍历至末尾，依次打印各编号。

**C++ 参考答案**

```cpp
#include <iostream>
#include <vector>
using namespace std;
int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    int n;
    cin >> n;
    vector<int> L(n + 1), R(n + 1); // L[i] 和 R[i] 分别记录编号 i 的左邻居和右邻居（0 表示无邻居）
    int head = 1; // 当前序列最左端的编号，初始时仅有编号 1
    for (int i = 2, x, p; i <= n; i++) {
        cin >> x >> p;
        if (p == 0) { // 将编号 i 的试卷插入到编号 x 的左边
            L[i] = L[x];
            R[i] = x; // i 的左邻居为 x 原来的左邻居，右邻居为 x
            if (L[x])
                R[L[x]] = i; // 若 x 原有左邻居，让该左邻居的右指针指向 i
            else
                head = i; // 若 x 就是队首，则 i 成为新的队首
            L[x] = i;     // x 的左指针指向 i
        } else {          // 将编号 i 的试卷插入到编号 x 的右边（对称操作）
            R[i] = R[x];
            L[i] = x;
            if (R[x])
                L[R[x]] = i;
            R[x] = i;
        }
    }
    for (int u = head; u; u = R[u]) // 从队首出发，沿右指针方向遍历至末尾
        cout << u << (R[u] ? ' ' : '\n');
}
```
# 实验2

## 18. 8583 顺序栈的基本操作

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8583&access=22249b6bc6c8246a790b3e3bdfc13022&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
创建一个空的顺序栈，并实现栈的入栈、出栈、返回栈的长度、返回栈顶元素、栈的遍历等基本算法。请将下面的程序补充完整。

#include<malloc.h>
#include<stdio.h>
#define OK 1
#define ERROR 0
#define STACK_INIT_SIZE 100 // 存储空间初始分配量
#define STACKINCREMENT 10 // 存储空间分配增量

typedef int SElemType; // 定义栈元素类型
typedef int Status; // Status是函数的类型,其值是函数结果状态代码，如OK等

struct SqStack
{
     SElemType *base; // 在栈构造之前和销毁之后，base的值为NULL
     SElemType *top; // 栈顶指针
     int stacksize; // 当前已分配的存储空间，以元素为单位
}; // 顺序栈

Status InitStack(SqStack &S)
{
// 构造一个空栈S，该栈预定义大小为STACK_INIT_SIZE
// 请补全代码

}

Status Push(SqStack &S,SElemType e)
{
// 在栈S中插入元素e为新的栈顶元素
// 请补全代码

}

Status Pop(SqStack &S,SElemType &e)
{
// 若栈不空，则删除S的栈顶元素，用e返回其值，并返回OK；否则返回ERROR
// 请补全代码

}

Status GetTop(SqStack S,SElemType &e)
{
// 若栈不空，则用e返回S的栈顶元素，并返回OK；否则返回ERROR
// 请补全代码

}

int StackLength(SqStack S)
{
// 返回栈S的元素个数
// 请补全代码

}

Status StackTraverse(SqStack S)
{
// 从栈顶到栈底依次输出栈中的每个元素
	SElemType *p  =  ______________________        //请填空
	if(______________________)printf("The Stack is Empty!"); //请填空
	else
	{
		printf("The Stack is: ");
		while(______________________)            //请填空
		{
                       ______________________               //请填空
			printf("%d ", *p);

		}
	}
	printf("\n");
	return OK;
}

int main()
{
     int a;
     SqStack S;
SElemType x, e;
     if(______________________)    // 判断顺序表是否创建成功，请填空
{
	printf("A Stack Has Created.\n");
}
while(1)
	{
    printf("1:Push \n2:Pop \n3:Get the Top \n4:Return the Length of the Stack\n5:Load the Stack\n0:Exit\nPlease choose:\n");
	scanf("%d",&a);
		switch(a)
		{
			case 1: scanf("%d", &x);
		      if(______________________) printf("Push Error!\n"); // 判断Push是否合法，请填空
		      else printf("The Element %d is Successfully Pushed!\n", x);
		      break;
		case 2: if(______________________) printf("Pop Error!\n"); // 判断Pop是否合法，请填空
			  else printf("The Element %d is Successfully Poped!\n", e);
		  	  break;
		case 3: if(______________________)printf("Get Top Error!\n"); // 判断Get Top是否合法，请填空
			  else printf("The Top Element is %d!\n", e);
		   	  break;
			case 4: printf("The Length of the Stack is %d!\n",______________________); //请填空
				  break;
			case 5: ______________________  //请填空
				  break;
			case 0: return 1;
		}
	}
}
```

**输入**

```
测试样例格式说明：
根据菜单操作：
1、输入1，表示要实现Push操作，紧跟着输入要Push的元素
2、输入2，表示要实现Pop操作
3、输入3，返回栈顶元素
4、输入4，返回栈的元素个数
5、输入5，表示从栈顶到栈底输出栈的所有元素
6、输入0，表示程序结束
```

**样例输入**

```
1
2
1
4
1
6
5
3
4
2
5
2
2
2
0
```

**样例输出**

```
A Stack Has Created.
1:Push
2:Pop
3:Get the Top
4:Return the Length of the Stack
5:Load the Stack
0:Exit
Please choose:
The Element 2 is Successfully Pushed!
1:Push
2:Pop
3:Get the Top
4:Return the Length of the Stack
5:Load the Stack
0:Exit
Please choose:
The Element 4 is Successfully Pushed!
1:Push
2:Pop
3:Get the Top
4:Return the Length of the Stack
5:Load the Stack
0:Exit
Please choose:
The Element 6 is Successfully Pushed!
1:Push
2:Pop
3:Get the Top
4:Return the Length of the Stack
5:Load the Stack
0:Exit
Please choose:
The Stack is: 6 4 2
1:Push
2:Pop
3:Get the Top
4:Return the Length of the Stack
5:Load the Stack
0:Exit
Please choose:
The Top Element is 6!
1:Push
2:Pop
3:Get the Top
4:Return the Length of the Stack
5:Load the Stack
0:Exit
Please choose:
The Length of the Stack is 3!
1:Push
2:Pop
3:Get the Top
4:Return the Length of the Stack
5:Load the Stack
0:Exit
Please choose:
The Element 6 is Successfully Poped!
1:Push
2:Pop
3:Get the Top
4:Return the Length of the Stack
5:Load the Stack
0:Exit
Please choose:
The Stack is: 4 2
1:Push
2:Pop
3:Get the Top
4:Return the Length of the Stack
5:Load the Stack
0:Exit
Please choose:
The Element 4 is Successfully Poped!
1:Push
2:Pop
3:Get the Top
4:Return the Length of the Stack
5:Load the Stack
0:Exit
Please choose:
The Element 2 is Successfully Poped!
1:Push
2:Pop
3:Get the Top
4:Return the Length of the Stack
5:Load the Stack
0:Exit
Please choose:
Pop Error!
1:Push
2:Pop
3:Get the Top
4:Return the Length of the Stack
5:Load the Stack
0:Exit
Please choose:
```

**解析**

**题目要求**：使用顺序存储结构（数组）实现一个栈，支持入栈（Push）、出栈（Pop）、获取栈顶元素（GetTop）、求栈长度（StackLength）以及遍历栈（StackTraverse）等基本操作。

**解题思路**：顺序栈通过 `base`（栈底指针）和 `top`（栈顶指针）两个指针协同工作，理解这两个指针的含义是掌握本题的关键：
- `base` 始终指向数组起始位置（栈底），`top` 指向**下一个可用位置**（而非当前栈顶元素所在位置），因此**空栈时 `top == base`**；
- **入栈**：将元素存入 `top` 所指位置，随后 `top` 向后移动一格——`*(S.top++)=e` 一条语句同时完成赋值与指针移动；
- **出栈**：先将 `top` 向前回退一格，再取出该位置的值——`e=*(--S.top)`；
- **获取栈顶元素**（不弹出）：读取 `*(top-1)` 处的值，因为 `top` 指向的是下一个空位，实际栈顶元素位于其前一个位置；
- **栈的长度**：`top - base`，即两个指针之间的距离；
- **栈满条件**：`top - base == stacksize`。

**遍历方向**：题目要求从栈顶到栈底依次输出，因此需要从 `top - 1` 开始向 `base` 方向逆向遍历。

**复杂度分析**：各基本操作的时间复杂度均为 O(1)。

**注意事项**：(1) 明确 `top` 指向"下一个可用位置"而非"栈顶元素本身"——本题约定如此，故代码中频繁出现 `top-1`、`--top` 等偏移操作；(2) 入栈前须判满，出栈前须判空，否则将导致越界访问。

**C++ 参考答案**

```cpp
#include <stdio.h>
#include <stdlib.h>
#define OK 1
#define ERROR 0
#define STACK_INIT_SIZE 100 // 存储空间初始分配量
#define STACKINCREMENT 10   // 存储空间分配增量

typedef int SElemType; // 定义栈元素类型
typedef int Status;    // Status是函数的类型,其值是函数结果状态代码，如OK等

struct SqStack {
    SElemType *base; // 在栈构造之前和销毁之后，base的值为NULL
    SElemType *top;  // 栈顶指针
    int stacksize;   // 当前已分配的存储空间，以元素为单位
};                   // 顺序栈

Status InitStack(SqStack &S) {
    // 构造一个空栈S，该栈预定义大小为STACK_INIT_SIZE
    S.base = new SElemType[STACK_INIT_SIZE];
    if (!S.base)
        return ERROR;
    S.top = S.base; // top与base指向同一位置，表示栈为空
    S.stacksize = STACK_INIT_SIZE;
    return OK;
}

Status Push(SqStack &S, SElemType e) {
    // 在栈S中插入元素e为新的栈顶元素
    // 请补全代码
    if (S.top - S.base == S.stacksize)
        return ERROR; // 栈已满，无法入栈
    *(S.top++) = e;   // 将元素e存入栈顶位置，随后top后移一格
    return OK;
}

Status Pop(SqStack &S, SElemType &e) {
    // 若栈不空，则删除S的栈顶元素，用e返回其值，并返回OK；否则返回ERROR
    // 请补全代码
    if (S.top == S.base)
        return ERROR; // 栈为空，无法出栈
    e = *(--S.top);   // top先回退一格，再取出该位置的元素
    return OK;
}

Status GetTop(SqStack S, SElemType &e) {
    // 若栈不空，则用e返回S的栈顶元素，并返回OK；否则返回ERROR
    // 请补全代码
    if (S.top == S.base)
        return ERROR; // 栈为空，无法获取栈顶
    e = *(S.top - 1); // top指向下一个空位，栈顶元素位于top-1处
    return OK;
}

int StackLength(SqStack S) {
    // 返回栈S的元素个数
    // 请补全代码
    return S.top - S.base; // 两指针之差即为栈中元素个数
}

Status StackTraverse(SqStack S) {
    // 从栈顶到栈底依次输出栈中的每个元素
    SElemType *p = S.top; // 请填空
    if (S.top == S.base)
        printf("The Stack is Empty!"); // 请填空
    else {
        printf("The Stack is: ");
        while (p != S.base) // 请填空
        {
            p--; // 请填空
            printf("%d ", *p);
        }
    }
    printf("\n");
    return OK;
}

int main() {
    int a;
    SqStack S;
    SElemType x, e;
    if (InitStack(S) == OK) // 判断顺序表是否创建成功，请填空
    {
        printf("A Stack Has Created.\n");
    }
    while (1) {
        printf("1:Push \n2:Pop \n3:Get the Top \n4:Return the Length of the Stack\n5:Load the "
               "Stack\n0:Exit\nPlease choose:\n");
        scanf("%d", &a);
        switch (a) {
        case 1:
            scanf("%d", &x);
            if (Push(S, x) == ERROR)
                printf("Push Error!\n"); // 判断Push是否合法，请填空
            else
                printf("The Element %d is Successfully Pushed!\n", x);
            break;
        case 2:
            if (Pop(S, e) == ERROR)
                printf("Pop Error!\n"); // 判断Pop是否合法，请填空
            else
                printf("The Element %d is Successfully Poped!\n", e);
            break;
        case 3:
            if (GetTop(S, e) == ERROR)
                printf("Get Top Error!\n"); // 判断Get Top是否合法，请填空
            else
                printf("The Top Element is %d!\n", e);
            break;
        case 4:
            printf("The Length of the Stack is %d!\n", StackLength(S)); // 请填空
            break;
        case 5:
            StackTraverse(S); // 请填空
            break;
        case 0:
            return 0;
        }
    }
}
```

## 19. 8584 循环队列的基本操作

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8584&access=ce91016a55b0d97579fb6dde40246531&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
创建一个空的循环队列，并实现入队、出队、返回队列的长度、返回队头元素、队列的遍历等基本算法。请将下面的程序补充完整。

#include<malloc.h>
#include<stdio.h>
#define OK 1
#define ERROR 0
typedef int Status; // Status是函数的类型,其值是函数结果状态代码，如OK等
typedef int QElemType;
#define MAXQSIZE 100 // 最大队列长度(对于循环队列，最大队列长度要减1)

typedef struct
{
   QElemType *base; // 初始化的动态分配存储空间
   int front; // 头指针,若队列不空,指向队列头元素
   int rear; // 尾指针,若队列不空,指向队列尾元素的下一个位置
 }SqQueue;

Status InitQueue(SqQueue &Q)
{
// 构造一个空队列Q，该队列预定义大小为MAXQSIZE
// 请补全代码

}

Status EnQueue(SqQueue &Q,QElemType e)
{
// 插入元素e为Q的新的队尾元素
// 请补全代码

}

Status DeQueue(SqQueue &Q, QElemType &e)
{
// 若队列不空, 则删除Q的队头元素, 用e返回其值, 并返回OK; 否则返回ERROR
// 请补全代码

}

Status GetHead(SqQueue Q, QElemType &e)
{
// 若队列不空，则用e返回队头元素，并返回OK，否则返回ERROR
// 请补全代码

}

int QueueLength(SqQueue Q)
{
// 返回Q的元素个数
// 请补全代码

}

Status QueueTraverse(SqQueue Q)
{
// 若队列不空，则从队头到队尾依次输出各个队列元素，并返回OK；否则返回ERROR.
	int i;
	i=Q.front;
	if(______________________)printf("The Queue is Empty!");  //请填空
	else{
		printf("The Queue is: ");
		while(______________________)     //请填空
		{
			printf("%d ",______________________ );   //请填空
			i = ______________________;   //请填空
		}
	}
	printf("\n");
	return OK;
}

int main()
{
	int a;
  SqQueue S;
	QElemType x, e;
  if(______________________)    // 判断顺序表是否创建成功，请填空
	{
		printf("A Queue Has Created.\n");
	}
	while(1)
	{
	printf("1:Enter \n2:Delete \n3:Get the Front \n4:Return the Length of the Queue\n5:Load the Queue\n0:Exit\nPlease choose:\n");
		scanf("%d",&a);
		switch(a)
		{
			case 1: scanf("%d", &x);
				  if(______________________) printf("Enter Error!\n"); // 判断入队是否合法，请填空
				  else printf("The Element %d is Successfully Entered!\n", x);
				  break;
			case 2: if(______________________) printf("Delete Error!\n"); // 判断出队是否合法，请填空
				  else printf("The Element %d is Successfully Deleted!\n", e);
				  break;
			case 3: if(______________________)printf("Get Head Error!\n"); // 判断Get Head是否合法，请填空
				  else printf("The Head of the Queue is %d!\n", e);
				  break;
			case 4: printf("The Length of the Queue is %d!\n",______________________);  //请填空
				  break;
			case 5: ______________________ //请填空
				  break;
			case 0: return 1;
		}
	}
}
```

**输入**

```
测试样例格式说明：
根据菜单操作：
1、输入1，表示要实现入队操作，紧跟着输入要入队的元素
2、输入2，表示要实现出队操作
3、输入3，返回队头元素
4、输入4，返回队列的元素个数
5、输入5，表示从队头到队尾输出队的所有元素
6、输入0，表示程序结束
```

**样例输入**

```
1
1
1
2
1
3
5
2
3
5
0
```

**样例输出**

```
A Queue Has Created.
1:Enter
2:Delete
3:Get the Front
4:Return the Length of the Queue
5:Load the Queue
0:Exit
Please choose:
The Element 1 is Successfully Entered!
1:Enter
2:Delete
3:Get the Front
4:Return the Length of the Queue
5:Load the Queue
0:Exit
Please choose:
The Element 2 is Successfully Entered!
1:Enter
2:Delete
3:Get the Front
4:Return the Length of the Queue
5:Load the Queue
0:Exit
Please choose:
The Element 3 is Successfully Entered!
1:Enter
2:Delete
3:Get the Front
4:Return the Length of the Queue
5:Load the Queue
0:Exit
Please choose:
The Queue is: 1 2 3
1:Enter
2:Delete
3:Get the Front
4:Return the Length of the Queue
5:Load the Queue
0:Exit
Please choose:
The Element 1 is Successfully Deleted!
1:Enter
2:Delete
3:Get the Front
4:Return the Length of the Queue
5:Load the Queue
0:Exit
Please choose:
The Head of the Queue is 2!
1:Enter
2:Delete
3:Get the Front
4:Return the Length of the Queue
5:Load the Queue
0:Exit
Please choose:
The Queue is: 2 3
1:Enter
2:Delete
3:Get the Front
4:Return the Length of the Queue
5:Load the Queue
0:Exit
Please choose:
```

**解析**

**题目要求**：使用数组实现一个循环队列，支持入队（EnQueue）、出队（DeQueue）、获取队头元素（GetHead）、求队列长度（QueueLength）以及遍历队列（QueueTraverse）等基本操作。

**解题思路**：

**"循环"的意义**：普通数组实现的队列在出队后，队头指针后移，前方已腾出的空间无法再利用。循环队列通过取模运算 `%MAXQSIZE` 使下标在到达数组末尾时回到起始位置，从而实现空间的循环利用。

**双指针与核心约定**：
- `front` 指向队头元素，`rear` 指向队尾元素的**下一个空位**；
- **入队**：将元素存入 `rear` 所指位置，然后 `rear=(rear+1)%MAXQSIZE`，向后绕一格；
- **出队**：取出 `front` 所指位置的元素，然后 `front=(front+1)%MAXQSIZE`，向后绕一格；
- **队空条件**：`front == rear`。

**牺牲一个存储位置的约定**：若队列被完全装满，则 `front==rear` 将同时表示"队空"与"队满"，无法区分。因此约定保留一个位置永不使用：当 `(rear+1)%MAXQSIZE == front` 时即视为队满——这正是题目注释中"最大队列长度要减 1"的原因。

**元素个数的计算**：`(rear - front + MAXQSIZE) % MAXQSIZE`。加上 `MAXQSIZE` 再取模，是为了防止 `rear < front`（即 rear 已绕过起点）时产生负数结果。

**复杂度分析**：各基本操作的时间复杂度均为 O(1)。

**C++ 参考答案**

```cpp
#include <stdio.h>
#include <stdlib.h>
#define OK 1
#define ERROR 0
typedef int Status; // Status是函数的类型,其值是函数结果状态代码，如OK等
typedef int QElemType;
#define MAXQSIZE 100 // 最大队列长度(对于循环队列，最大队列长度要减1)

typedef struct {
    QElemType *base; // 初始化的动态分配存储空间
    int front;       // 头指针,若队列不空,指向队列头元素
    int rear;        // 尾指针,若队列不空,指向队列尾元素的下一个位置
} SqQueue;

Status InitQueue(SqQueue &Q) {
    // 构造一个空队列Q，该队列预定义大小为MAXQSIZE
    // 请补全代码
    Q.base = new QElemType[MAXQSIZE];
    if (!Q.base)
        return ERROR;
    Q.front = Q.rear = 0; // front和rear均初始化为0，表示队列为空
    return OK;
}

Status EnQueue(SqQueue &Q, QElemType e) {
    // 插入元素e为Q的新的队尾元素
    // 请补全代码
    if ((Q.rear + 1) % MAXQSIZE == Q.front)
        return ERROR;                 // 队列已满（牺牲一个位置的约定）
    Q.base[Q.rear] = e;               // 将元素e存入rear所指位置
    Q.rear = (Q.rear + 1) % MAXQSIZE; // rear绕圈后移一格
    return OK;
}

Status DeQueue(SqQueue &Q, QElemType &e) {
    // 若队列不空, 则删除Q的队头元素, 用e返回其值, 并返回OK; 否则返回ERROR
    // 请补全代码
    if (Q.rear == Q.front)
        return ERROR;                   // 队列为空，无法出队
    e = Q.base[Q.front];                // 取出front所指的队头元素
    Q.front = (Q.front + 1) % MAXQSIZE; // front绕圈后移一格
    return OK;
}

Status GetHead(SqQueue Q, QElemType &e) {
    // 若队列不空，则用e返回队头元素，并返回OK，否则返回ERROR
    // 请补全代码
    if (Q.rear == Q.front)
        return ERROR;    // 队列为空，无法获取队头
    e = Q.base[Q.front]; // 读取队头元素的值
    return OK;
}

int QueueLength(SqQueue Q) {
    // 返回Q的元素个数
    // 请补全代码
    return (Q.rear - Q.front + MAXQSIZE) % MAXQSIZE; // 加MAXQSIZE再取模，防止rear<front时出现负数
}

Status QueueTraverse(SqQueue Q) {
    // 若队列不空，则从队头到队尾依次输出各个队列元素，并返回OK；否则返回ERROR.
    int i;
    i = Q.front;
    if (QueueLength(Q) == 0)
        printf("The Queue is Empty!"); // 请填空
    else {
        printf("The Queue is: ");
        while ((i + MAXQSIZE) % MAXQSIZE < (Q.rear + MAXQSIZE) % MAXQSIZE) // 请填空
        {
            printf("%d ", Q.base[(i + MAXQSIZE) % MAXQSIZE]); // 请填空
            i = (i + 1) % MAXQSIZE;                           // 请填空
        }
    }
    printf("\n");
    return OK;
}

int main() {
    int a;
    SqQueue S;
    QElemType x, e;
    if (InitQueue(S) == OK) // 判断顺序表是否创建成功，请填空
    {
        printf("A Queue Has Created.\n");
    }
    while (1) {
        printf("1:Enter \n2:Delete \n3:Get the Front \n4:Return the Length of the Queue\n5:Load "
               "the Queue\n0:Exit\nPlease choose:\n");
        scanf("%d", &a);
        switch (a) {
        case 1:
            scanf("%d", &x);
            if (EnQueue(S, x) == ERROR)
                printf("Enter Error!\n"); // 判断入队是否合法，请填空
            else
                printf("The Element %d is Successfully Entered!\n", x);
            break;
        case 2:
            if (DeQueue(S, e) == ERROR)
                printf("Delete Error!\n"); // 判断出队是否合法，请填空
            else
                printf("The Element %d is Successfully Deleted!\n", e);
            break;
        case 3:
            if (GetHead(S, e) == ERROR)
                printf("Get Head Error!\n"); // 判断Get Head是否合法，请填空
            else
                printf("The Head of the Queue is %d!\n", e);
            break;
        case 4:
            printf("The Length of the Queue is %d!\n", QueueLength(S)); // 请填空
            break;
        case 5:
            QueueTraverse(S); // 请填空
            break;
        case 0:
            return 0;
        }
    }
}
```

## 20. 8585 栈的应用——进制转换

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8585&access=bee35dbbd9cdd8c37c424ce9f155562f&fixedLanguage=MA==
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++

**题目描述**

```
利用顺序栈的基本操作算法，编写满足下列要求的数制转换程序：对于输入的任意一个非负十进制整数，打印输出与其等值的八进制数。
```

**输入**

```
第一行：输入一个非负的十进制整数
```

**输出**

```
第一行：与输入等值的八进制数
```

**样例输入**

```
15
```

**样例输出**

```
17
```

**解析**

**题目要求**：将一个非负十进制整数转换为等值的八进制数并输出。

**解题思路**：采用经典的"除基取余法"。反复将待转换数除以 8，记录每次的余数。然而，最先得到的余数对应的是最低位，直接输出顺序与正确结果恰好相反。利用栈"后进先出"的特性，将余数依次压入栈中，再依次弹出输出，即可自然获得正确的正序结果。

**特殊处理**：当输入的 n 为 0 时，上述循环不会执行，需单独处理并输出 0。

**复杂度分析**：时间复杂度 O(log n)，空间复杂度 O(log n)，其中 n 为输入的十进制整数。

**C++ 参考答案**

```cpp
#include <iostream>
#include <stack>
using namespace std;
int main() {
    long long n;
    cin >> n;
    if (n == 0) {
        cout << 0;
        return 0;
    } // 特殊情况：输入为0时直接输出
    stack<int> s;
    while (n) {
        s.push(n % 8);
        n /= 8;
    } // 反复除以8取余，余数依次压入栈中（低位先入栈）
    while (!s.empty()) {
        cout << s.top();
        s.pop();
    } // 依次弹出栈顶元素，输出顺序自然反转
}
```

## 21. 8586 括号匹配检验

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8586&access=df6b35826e69b145afabc614e8a057b0&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
利用栈编写满足下列要求的括号匹配检验程序：假设表达式中允许包含两种括号：圆括号和方括号，其嵌套的顺序随意，即([]())或[([][])]等为正确的格式，[(]或([())或(()])均为不正确的格式。输入一个包含上述括号的表达式，检验括号是否配对。本题给出部分check()函数，要求将check()函数补充完整，并完成整个程序。

typedef char SElemType;
#include"malloc.h"
#include"stdio.h"
#include"math.h"
#include"stdlib.h" // exit()
#define OK 1
#define ERROR 0
#define TRUE 1
#define FALSE 0
typedef int Status; // Status是函数的类型,其值是函数结果状态代码，如OK等
#define STACK_INIT_SIZE 10 // 存储空间初始分配量
#define STACKINCREMENT 2 // 存储空间分配增量
struct SqStack
{
 SElemType *base; // 在栈构造之前和销毁之后，base的值为NULL
 SElemType *top; // 栈顶指针
 int stacksize; // 当前已分配的存储空间，以元素为单位
 }; // 顺序栈
Status InitStack(SqStack &S)
{
 }

Status StackEmpty(SqStack S)
{

 }
Status Push(SqStack &S,SElemType e)
{
 }
 Status Pop(SqStack &S,SElemType &e)
{
 }
void check()
 { // 对于输入的任意一个字符串，检验括号是否配对
   SqStack s;
   SElemType ch[80],*p,e;
   if(InitStack(s)) // 初始化栈成功
   {
    //printf("请输入表达式\n");
     __________________________________;
     p=ch;
     while(*p) // 没到串尾
       switch(*p)
       {
         case '(':
         case '[':_______________________;
                  break; // 左括号入栈，且p++
         case ')':
         case ']':if(!StackEmpty(s)) // 栈不空
                  {
                   _________________________; // 弹出栈顶元素
                    if(*p==')'&&e!='('||___________________&&___________________)
                                                // 弹出的栈顶元素与*p不配对
{
                      printf("isn't matched pairs\n");
                      exit(ERROR);
                    }
                    else
                    {
                     __________________________;
                      break; // 跳出switch语句
                    }
                  }
                  else // 栈空
                  {
                    printf("lack of left parenthesis\n");
                    exit(ERROR);
                  }
         default: ______________________; // 其它字符不处理，指针向后移
       }
     if(StackEmpty(s)) // 字符串结束时栈空
       printf("matching\n");
     else
       printf("lack of right parenthesis\n");
   }
 }
int main()
 {
   check();
 }
```

**输入**

```
第一行：输入一个包含圆括号或方括号、不超过80个字符的表达式串。
```

**输出**

```
第一行：若输入表达式括号匹配，输出"matching"; 若不匹配，输出具体信息:"isn't matched pairs", 或"lack of left parenthesis"或"lack of right parenthesis"
```

**样例输入**

```
8*[3*(35-23)]
```

**样例输出**

```
matching
```

**解析**

**题目要求**：检验表达式中的圆括号 `()` 和方括号 `[]` 是否正确嵌套配对，并区分以下三种错误类型：括号类型不匹配（`isn't matched pairs`）、缺少左括号（`lack of left parenthesis`）、缺少右括号（`lack of right parenthesis`）。

**解题思路**：括号匹配是栈的经典应用场景。从左至右逐个扫描字符，处理规则如下：
- 遇到**左括号**（`(` 或 `[`），将其压入栈中；
- 遇到**右括号**（`)` 或 `]`），检查栈的状态：若栈为空，说明前面不存在与之配对的左括号，属于"缺少左括号"错误；若栈不空，则弹出栈顶元素，检验其是否与当前右括号属于同一类型（`)` 配 `(`、`]` 配 `[`），若类型不同则属于"括号不匹配"错误；
- 其他字符（数字、运算符等）直接跳过，不做处理。

扫描完毕后：若栈**恰好为空**，说明所有括号均已成功配对，输出 `matching`；若栈**仍有元素残留**，说明有左括号始终未等到对应的右括号，属于"缺少右括号"错误。

**算法分析**：括号的配对规则遵循"最近的未匹配左括号优先与当前右括号配对"的原则，这恰好符合栈"后进先出"的特性，因此使用栈来处理此问题十分自然。时间复杂度 O(n)，其中 n 为字符串长度。

**C++ 参考答案**

```cpp
typedef char SElemType;
#include "malloc.h"
#include "math.h"
#include "stdio.h"
#include "stdlib.h" // exit()
#define OK 1
#define ERROR 0
#define TRUE 1
#define FALSE 0
typedef int Status;        // Status是函数的类型,其值是函数结果状态代码，如OK等
#define STACK_INIT_SIZE 10 // 存储空间初始分配量
#define STACKINCREMENT 2   // 存储空间分配增量
struct SqStack {
    SElemType *base; // 在栈构造之前和销毁之后，base的值为NULL
    SElemType *top;  // 栈顶指针
    int stacksize;   // 当前已分配的存储空间，以元素为单位
};                   // 顺序栈
Status InitStack(SqStack &S) {
    S.base = (SElemType *)malloc(STACK_INIT_SIZE * sizeof(SElemType));
    if (!S.base)
        return ERROR;
    S.top = S.base;
    S.stacksize = STACK_INIT_SIZE;
    return OK;
}

Status StackEmpty(SqStack S) {
    if (S.top == S.base)
        return TRUE;
    else
        return FALSE;
}
Status Push(SqStack &S, SElemType e) {
    if (S.top - S.base >= S.stacksize) {
        S.base = (SElemType *)realloc(S.base, (S.stacksize + STACKINCREMENT) * sizeof(SElemType));
        if (!S.base)
            return ERROR;
        S.top = S.base + S.stacksize;
        S.stacksize += STACKINCREMENT;
    }
    *(S.top++) = e;
    return OK;
}
Status Pop(SqStack &S, SElemType &e) {
    if (S.top == S.base)
        return ERROR;
    e = *(--S.top);
    return OK;
}
void check() { // 对于输入的任意一个字符串，检验括号是否配对
    SqStack s;
    SElemType ch[80], *p, e;
    if (InitStack(s)) // 初始化栈成功
    {
        // printf("请输入表达式\n");
        scanf("%s", ch);
        p = ch;
        while (*p) // 没到串尾
            switch (*p) {
            case '(':
            case '[': {
                Push(s, *p); // 左括号入栈
                p++;         // 指针后移
                break;       // 左括号入栈，且p++
            }
            case ')':
            case ']':
                if (!StackEmpty(s)) // 栈不空
                {
                    Pop(s, e); // 弹出栈顶元素用于匹配检验
                    if (*p == ')' && e != '(' ||
                        *p == ']' && e != '[') // 栈顶元素与当前右括号类型不匹配
                    {
                        printf("isn't matched pairs\n");
                        exit(ERROR);
                    } else {
                        p++;   // 匹配成功，指针后移
                        break; // 跳出switch语句
                    }
                } else // 栈空
                {
                    printf("lack of left parenthesis\n");
                    exit(ERROR);
                }
            default:
                p++; // 其它字符不处理，指针向后移
            }
        if (StackEmpty(s)) // 字符串结束时栈空
            printf("matching\n");
        else
            printf("lack of right parenthesis\n");
    }
}
int main() {
    check();
}
```

## 22. 8587 行编辑程序

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8587&access=e97abb1db1d8d73eef0c14ba6fc201aa&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
利用栈编写简单的行编辑程序：接受用户从终端输入的程序或数据，在输入过程中，允许用户输入出差错，并在发现有误时可以及时更正。例如：当用户发现刚刚键入的一个字符是错的时，可以补进一个退格符"#"，以表示前一个字符无效；如果发现当前键入的行内差错较多或难以补救，则可以键入一个退行符"@"，以表示当前行中的字符均无效。例如：假设从终端接受了这样两行字符：
whli##ilr#e (s#*s)
outcha@putchar(*s=#++);
则实际有效的是下列两行：
while (*s)
  putchar(*s++);
本题目给出部分函数，要求将行编辑函数补充完整，并完成整个程序。

typedef char SElemType;
#include"malloc.h"
#include"stdio.h"
#include"math.h"
#include"stdlib.h" // exit()
#define OK 1
#define ERROR 0
#define TRUE 1
#define FALSE 0
typedef int Status; // Status是函数的类型,其值是函数结果状态代码，如OK等
#define STACK_INIT_SIZE 10 // 存储空间初始分配量
 #define STACKINCREMENT 2 // 存储空间分配增量
struct SqStack
{
 SElemType *base; // 在栈构造之前和销毁之后，base的值为NULL
 SElemType *top; // 栈顶指针
 int stacksize; // 当前已分配的存储空间，以元素为单位
}; // 顺序栈

Status InitStack(SqStack &S)
{ // 构造一个空栈S

 }
Status StackEmpty(SqStack S)
 { // 若栈S为空栈，则返回TRUE，否则返回FALSE

 }
Status ClearStack(SqStack &S)
 { // 把S置为空栈
   S.top=S.base;
   return OK;
 }
Status DestroyStack(SqStack &S)
 { // 销毁栈S，S不再存在
   free(S.base);
   S.base=NULL;
   S.top=NULL;
   S.stacksize=0;
   return OK;
 }
Status Push(SqStack &S,SElemType e)
 { // 插入元素e为新的栈顶元素

 }
 Status Pop(SqStack &S,SElemType &e)
 { // 若栈不空，则删除S的栈顶元素，用e返回其值，并返回OK；否则返回ERROR

 }
Status StackTraverse(SqStack S,Status(*visit)(SElemType))
 { // 从栈底到栈顶依次对栈中每个元素调用函数visit()。
   // 一旦visit()失败，则操作失败
   while(S.top>S.base)
     visit(*S.base++);
   printf("\n");
   return OK;
 }
Status visit(SElemType c)
 {
   printf("%c",c);
   return OK;
 }
 void LineEdit()
 { // 利用字符栈s，从终端接收一行并送至调用过程的数据区。算法3.2
   SqStack s;
   char ch,c;
   int n,i;
   InitStack(s);
   scanf("%d",&n);
   ch=getchar();
   for(i=1;i<=n;i++)
   { ch=_______________________________;
     while(ch!='\n')
    {
       switch(_____________________)
       {
         case '#':Pop(s,c);
                  break; // 仅当栈非空时退栈
         case '@':ClearStack(s);
                  break; // 重置s为空栈
         default :_________________________________; // 有效字符进栈
       }
       ____________________________; // 从终端接收下一个字符
     }
     StackTraverse(s,visit); // 将从栈底到栈顶的栈内字符输出
    _____________________________________; // 重置s为空栈
    }
   DestroyStack(s);
 }
 void main()
 {
     LineEdit();
 }
```

**输入**

```
第一行：第一个字符为输入文本的行数n;
第二行至第n行：每行均为一串字符，其间可以含有"#"和"@"符号，以回车键结束本行的输入；
```

**输出**

```
输出第一至第n行的内容如下：
第一行：第一行从终端输入的有效字符。
第二行：第二行从终端输入的有效字符。
…… ……
第n行：第n行从终端输入的有效字符。
```

**样例输入**

```
2
defne##ine OK 1
typp cila@type int element
```

**样例输出**

```
define OK 1
type int element
```

**解析**

**题目要求**：实现一个简易的行编辑程序。用户逐字符输入文本，其中退格符 `#` 表示撤销前一个字符（使其无效），退行符 `@` 表示清空当前整行内容（使该行所有字符无效）。程序需输出每行经编辑后的有效内容。

**解题思路**：将当前行的有效字符序列维护在栈中，从左至右逐个读取输入字符并按以下规则处理：
- **普通字符**：压入栈中；
- **退格符 `#`**：弹出栈顶元素，即撤销最近输入的一个字符；
- **退行符 `@`**：清空整个栈，即撤销当前行的全部内容；
- **换行符**：当前行结束。从栈底到栈顶依次输出栈中字符，即为该行有效内容的正确顺序。输出后清空栈，准备处理下一行。

**算法分析**：退格符 `#` 撤销的始终是"最近输入的那个字符"，即栈顶元素。"后进先出"的特性使栈成为实现此类撤销操作的理想数据结构。时间复杂度 O(n)，其中 n 为输入的总字符数。

**C++ 参考答案**

```cpp
typedef char SElemType;
#include "malloc.h"
#include "math.h"
#include "stdio.h"
#include "stdlib.h" // exit()
#define OK 1
#define ERROR 0
#define TRUE 1
#define FALSE 0
typedef int Status;         // Status是函数的类型,其值是函数结果状态代码，如OK等
#define STACK_INIT_SIZE 10 // 存储空间初始分配量
#define STACKINCREMENT 2   // 存储空间分配增量
struct SqStack {
    SElemType *base; // 在栈构造之前和销毁之后，base的值为NULL
    SElemType *top;  // 栈顶指针
    int stacksize;   // 当前已分配的存储空间，以元素为单位
};                   // 顺序栈

Status InitStack(SqStack &S) { // 构造一个空栈S
    S.base = (SElemType *)malloc(STACK_INIT_SIZE * sizeof(SElemType));
    if (!S.base)
        return ERROR;
    S.top = S.base;
    S.stacksize = STACK_INIT_SIZE;
    return OK;
}
Status StackEmpty(SqStack S) { // 若栈S为空栈，则返回TRUE，否则返回FALSE
    if (S.top == S.base)
        return TRUE;
    else
        return FALSE;
}
Status ClearStack(SqStack &S) { // 把S置为空栈
    S.top = S.base;
    return OK;
}
Status DestroyStack(SqStack &S) { // 销毁栈S，S不再存在
    free(S.base);                 // 释放动态分配的存储空间
    S.base = NULL;
    S.top = NULL;
    S.stacksize = 0;
    return OK;
}
Status Push(SqStack &S, SElemType e) { // 插入元素e为新的栈顶元素
    if (S.top - S.base >= S.stacksize) {
        S.base = (SElemType *)realloc(S.base, (S.stacksize + STACKINCREMENT) * sizeof(SElemType));
        if (!S.base)
            return ERROR;
        S.top = S.base + S.stacksize;
        S.stacksize += STACKINCREMENT;
    }
    *S.top++ = e;
    return OK;
}
Status Pop(SqStack &S,
           SElemType &e) { // 若栈不空，则删除S的栈顶元素，用e返回其值，并返回OK；否则返回ERROR
    if (S.top == S.base)
        return ERROR;
    e = *--S.top;
    return OK;
}
Status
StackTraverse(SqStack S,
              Status (*visit)(SElemType)) { // 从栈底到栈顶依次对栈中每个元素调用函数visit()。
    // 一旦visit()失败，则操作失败
    while (S.top > S.base)
        visit(*S.base++);
    printf("\n");
    return OK;
}
Status visit(SElemType c) {
    printf("%c", c);
    return OK;
}
void LineEdit() { // 利用字符栈s，从终端接收一行并送至调用过程的数据区。算法3.2
    SqStack s;
    char ch, c;
    int n, i;
    InitStack(s);
    scanf("%d", &n);
    ch = getchar();
    for (i = 1; i <= n; i++) {
        ch = getchar();
        while (ch != '\n') {
            switch (ch) {
            case '#':
                Pop(s, c);
                break;     // 仅当栈非空时退栈
            case '@':
                ClearStack(s);
                break;         // 重置s为空栈
            default:
                Push(s, ch);
            }
            ch = getchar();
        }
        StackTraverse(s, visit); // 将从栈底到栈顶的栈内字符输出
        ClearStack(s);           // 重置s为空栈
    }
    DestroyStack(s);
}
int main() {
    LineEdit();
    return 0;
}
```

## 23. 8588 表达式求值

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8588&access=8a3a7791cae7f1092a37115dbbfd7251&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
顺序栈的基本操作如下：
#include<malloc.h>
#include<stdio.h>
#define OK 1
#define ERROR 0
#define STACK_INIT_SIZE 100 // 存储空间初始分配量
#define STACKINCREMENT 10 // 存储空间分配增量

typedef int SElemType; // 定义栈元素类型
typedef int Status; // Status是函数的类型,其值是函数结果状态代码，如OK等

struct SqStack
{
     SElemType *base; // 在栈构造之前和销毁之后，base的值为NULL
     SElemType *top; // 栈顶指针
     int stacksize; // 当前已分配的存储空间，以元素为单位
}; // 顺序栈

Status InitStack(SqStack &S)
{
// 构造一个空栈S，该栈预定义大小为STACK_INIT_SIZE
	S.base=(SElemType*)malloc(STACK_INIT_SIZE*sizeof(SElemType));
     if(!S.base) return ERROR;
	 S.top=S.base;
	 S.stacksize=STACK_INIT_SIZE;
	 return OK;
}

Status Push(SqStack &S,SElemType e)
{
// 在栈S中插入元素e为新的栈顶元素
	if(S.top-S.base>=S.stacksize)
	{
		S.base=(SElemType*)realloc(S.base,(S.stacksize+STACKINCREMENT)*sizeof(SElemType));
		if(!S.base) return ERROR;
		S.top=S.base+S.stacksize;
		S.stacksize+=STACKINCREMENT;
	}
	*S.top++=e;
	return OK;
}

Status Pop(SqStack &S,SElemType &e)
{
// 若栈不空，则删除S的栈顶元素，用e返回其值，并返回OK；否则返回ERROR
	if(S.top==S.base) return ERROR;
     e=*--S.top;
	 return OK;
}

Status GetTop(SqStack S,SElemType &e)
{
// 若栈不空，则用e返回S的栈顶元素，并返回OK；否则返回ERROR
	if(S.top==S.base) return ERROR;
    e=*(S.top-1);
	return OK;
}

int StackLength(SqStack S)
{
// 返回栈S的元素个数
	int i;
    i=S.top-S.base;
	return i;
}

Status StackTraverse(SqStack S)
{
// 从栈顶到栈底依次输出栈中的每个元素
	SElemType *p = (SElemType *)malloc(sizeof(SElemType));
	p = S.top;
	if(S.top==S.base)printf("The Stack is Empty!");
	else
	{
		printf("The Stack is: ");
		p--;
		while(p>=S.base)
		{
			printf("%d ", *p);
			p--;
		}
	}
	printf("\n");
	return OK;
}

利用栈编写表达式求值程序：输入含有"+"、"-"、"*"、"/"四则运算的表达式，其中负数要用（0-正数）表示，并以=结束。要求输出表达式的值（两运算符号的优先关系见教材表3.1）。
```

**输入**

```
第一行：一个算术表达式
```

**输出**

```
第一行：算术表达式的值
```

**样例输入**

```
3*(9-7)=
```

**样例输出**

```
6
```

**解析**

**题目要求**：对含有 `+`、`-`、`*`、`/` 四则运算及括号的中缀算术表达式（以 `=` 结尾）进行求值，输出计算结果。

**解题思路**：采用"双栈法"——维护一个操作数栈 `nums` 和一个运算符栈 `ops`，从左至右逐个扫描表达式字符：
- **数字**：完整读出一个多位数后，压入操作数栈 `nums`；
- **左括号 `(`**：直接压入运算符栈 `ops`，等待对应的右括号；
- **右括号 `)`**：反复弹出 `ops` 栈顶运算符并执行计算，直到遇到匹配的左括号 `(`，然后将该左括号弹出丢弃；
- **运算符**：在压入当前运算符之前，先将 `ops` 栈中**优先级不低于当前运算符**的栈顶运算符逐一弹出并执行计算，然后再压入当前运算符。

扫描完成后，将 `ops` 中剩余的运算符全部弹出并执行计算，此时 `nums` 栈顶元素即为表达式的最终结果。

**算法分析**：本算法的核心在于**运算符优先级的比较**。乘除法 `*`、`/` 的优先级（2）高于加减法 `+`、`-` 的优先级（1）。遇到新运算符时，先结算栈中优先级不低于它的运算符，从而保证乘除法先于加减法计算，同级运算符按从左到右的顺序计算。

**注意事项**：每次执行一步计算时，需从操作数栈弹出两个操作数 b（后弹出，为右操作数）和 a（先弹出，为左操作数），以及一个运算符 op，计算 `a op b` 后将结果压回栈中。注意 a 和 b 的先后顺序不可颠倒，因为减法和除法不满足交换律。

**复杂度分析**：时间复杂度 O(n)，空间复杂度 O(n)，其中 n 为表达式长度。

**C++ 参考答案**

```cpp
#include <ctype.h>
#include <malloc.h>
#include <stdio.h>
#define OK 1
#define ERROR 0
#define STACK_INIT_SIZE 100 // 存储空间初始分配量
#define STACKINCREMENT 10   // 存储空间分配增量

typedef int SElemType; // 定义栈元素类型
typedef int Status;    // Status是函数的类型,其值是函数结果状态代码，如OK等

struct SqStack {
    SElemType *base; // 在栈构造之前和销毁之后，base的值为NULL
    SElemType *top;  // 栈顶指针
    int stacksize;   // 当前已分配的存储空间，以元素为单位
};                   // 顺序栈

Status InitStack(SqStack &S) {
    S.base = (SElemType *)malloc(STACK_INIT_SIZE * sizeof(SElemType));
    if (!S.base)
        return ERROR;
    S.top = S.base;
    S.stacksize = STACK_INIT_SIZE;
    return OK;
}

Status Push(SqStack &S, SElemType e) {
    if (S.top - S.base >= S.stacksize) {
        S.base = (SElemType *)realloc(S.base, (S.stacksize + STACKINCREMENT) * sizeof(SElemType));
        if (!S.base)
            return ERROR;
        S.top = S.base + S.stacksize;
        S.stacksize += STACKINCREMENT;
    }
    *S.top++ = e;
    return OK;
}

Status Pop(SqStack &S, SElemType &e) {
    if (S.top == S.base)
        return ERROR;
    e = *--S.top;
    return OK;
}

Status GetTop(SqStack S, SElemType &e) {
    if (S.top == S.base)
        return ERROR;
    e = *(S.top - 1);
    return OK;
}

int StackLength(SqStack S) {
    return S.top - S.base;
}

Status StackTraverse(SqStack S) {
    SElemType *p;
    p = S.top;
    if (S.top == S.base)
        printf("The Stack is Empty!");
    else {
        printf("The Stack is: ");
        p--;
        while (p >= S.base) {
            printf("%d ", *p);
            p--;
        }
    }
    printf("\n");
    return OK;
}

int Priority(char op) {
    if (op == '+' || op == '-')
        return 1;
    if (op == '*' || op == '/')
        return 2;
    return 0;
}

int Operate(int a, char op, int b) {
    if (op == '+')
        return a + b;
    if (op == '-')
        return a - b;
    if (op == '*')
        return a * b;
    return a / b;
}

void Calculate(SqStack &OPND, SqStack &OPTR) {
    SElemType a, b, op;
    Pop(OPND, b);
    Pop(OPND, a);
    Pop(OPTR, op);
    Push(OPND, Operate(a, (char)op, b));
}

int main() {
    SqStack OPND, OPTR;
    InitStack(OPND);
    InitStack(OPTR);
    int ch;
    while ((ch = getchar()) != EOF) {
        if (ch == ' ' || ch == '\n' || ch == '\t')
            continue;
        if (ch == '=')
            break;
        if (isdigit(ch)) {
            int num = 0;
            while (isdigit(ch)) {
                num = num * 10 + ch - '0';
                ch = getchar();
            }
            Push(OPND, num);
            if (ch == '=')
                break;
            if (ch != EOF)
                ungetc(ch, stdin);
        } else if (ch == '(') {
            Push(OPTR, ch);
        } else if (ch == ')') {
            SElemType top;
            GetTop(OPTR, top);
            while ((char)top != '(') {
                Calculate(OPND, OPTR);
                GetTop(OPTR, top);
            }
            Pop(OPTR, top); // 弹出左括号
        } else {
            SElemType top;
            while (GetTop(OPTR, top) == OK && (char)top != '(' &&
                   Priority((char)top) >= Priority((char)ch))
                Calculate(OPND, OPTR);
            Push(OPTR, ch);
        }
    }
    while (StackLength(OPTR) > 0)
        Calculate(OPND, OPTR);
    SElemType ans;
    GetTop(OPND, ans);
    printf("%d\n", ans);
    return 0;
}
```

## 24. 18938 汉诺塔问题

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18938&access=bbc596df15a4ddbcb95e39b96c358fb9&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
汉诺塔（Tower of Hanoi），又称河内塔，是一个源于印度古老传说的益智玩具。
大梵天创造世界的时候做了三根金刚石柱子，在一根柱子上从下往上按照大小顺序摞着64片黄金圆盘。
大梵天命令婆罗门把圆盘从下面开始按大小顺序重新摆放在另一根柱子上。
并且规定，在小圆盘上不能放大圆盘，在三根柱子之间一次只能移动一个圆盘。
由于条件是一次只能移动一个盘，且不允许大盘放在小盘上面，所以64个盘的移动次数是：18,446,744,073,709,551,615
这是一个天文数字，若每一微秒可能计算(并不输出)一次移动，那么也需要几乎一百万年。
我们仅能找出问题的解决方法并解决较小N值时的汉诺塔，但很难用计算机解决64层的汉诺塔。
假定圆盘从小到大编号为1, 2, ...
```

**输入**

```
输入为一个整数(小于20）后面跟三个单字符字符串。
整数为盘子的数目，后三个字符表示三个杆子的编号。
```

**输出**

```
输出每一步移动盘子的记录。一次移动一行。
每次移动的记录为例如 a->3->b 的形式，即把编号为3的盘子从a杆移至b杆。
```

**样例输入**

```
2 a b c
```

**样例输出**

```
a->1->c
a->2->b
c->1->b
```

**解析**

**题目要求**：将 n 个盘子从源柱借助辅助柱移动到目标柱，遵循"大盘不能压小盘"、"每次只移动一个盘子"的规则，逐步输出每一次移动操作。

**解题思路**：汉诺塔是递归分治思想的经典范例。将"把 n 个盘从源柱 a 移至目标柱 b（借助辅助柱 c）"分解为以下三个步骤：
1. 将上面 n-1 个盘从源柱 a 移至辅助柱 c（借助目标柱 b）；
2. 将最底部的第 n 个盘从源柱 a 直接移至目标柱 b；
3. 将那 n-1 个盘从辅助柱 c 移至目标柱 b（借助源柱 a）。

第 1 步和第 3 步是规模更小的同类子问题，递归求解即可。递归边界为 n=0（无盘可移），直接返回。

**注意事项**：每层递归中，三个柱子的角色（源柱、目标柱、辅助柱）会随参数传递而互换。调用递归函数时需确保参数顺序正确对应——代码中 `h(n-1,a,c,b)` 与 `h(n-1,c,b,a)` 的参数排列即体现了角色的交换。

**复杂度分析**：总移动次数为 2^n - 1，时间复杂度 O(2^n)。这正是 64 层汉诺塔需要计算数百万年的原因。

**C++ 参考答案**

```cpp
#include <iostream>
using namespace std;
// 将n个盘从柱a移至柱b，柱c作为辅助柱
void h(int n, char a, char b, char c) {
    if (n == 0)
        return;        // 递归边界：无盘可移，直接返回
    h(n - 1, a, c, b); // 第一步：将上面n-1个盘从a移至辅助柱c
    cout << a << "->" << n << "->" << b << "\n"; // 第二步：将第n个盘（当前最大的盘）从a移至b
    h(n - 1, c, b, a); // 第三步：将n-1个盘从辅助柱c移至目标柱b
}
int main() {
    int n;
    char a, b, c;
    cin >> n >> a >> b >> c;
    h(n, a, b, c);
}
```

## 25. 8590 队列的应用——银行客户平均等待时间

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8590&access=a804e0333c430530ccc42f89d0830156&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
队列的基本操作如下：
#include<malloc.h>
#include<stdio.h>
#include<stdlib.h>
#define OK 1
#define ERROR 0
typedef int Status; // Status是函数的类型,其值是函数结果状态代码，如OK等
typedef int QElemType;
#define MAXQSIZE 100 // 最大队列长度(对于循环队列，最大队列长度要减1)

typedef struct
{
   QElemType *base; // 初始化的动态分配存储空间
   int front; // 头指针,若队列不空,指向队列头元素
   int rear; // 尾指针,若队列不空,指向队列尾元素的下一个位置
 }SqQueue;

Status InitQueue(SqQueue &Q)
{
// 构造一个空队列Q，该队列预定义大小为MAXQSIZE
	Q.base=(QElemType*)malloc(MAXQSIZE*sizeof(QElemType));
	if(!Q.base) exit(1);
	Q.rear=Q.front=0;
	return OK;
}

Status EnQueue(SqQueue &Q,QElemType e)
{
// 插入元素e为Q的新的队尾元素
	 if((Q.rear+1)%MAXQSIZE==Q.front) return ERROR;
	 Q.base[Q.rear]=e;
	 Q.rear=(Q.rear+1)%MAXQSIZE;
	 return OK;
}

Status DeQueue(SqQueue &Q, QElemType &e)
{
// 若队列不空, 则删除Q的队头元素, 用e返回其值, 并返回OK; 否则返回ERROR
	 if(Q.front==Q.rear) return ERROR;
	 e=Q.base[Q.front];
	 Q.front=(Q.front+1)%MAXQSIZE;
	 return OK;
}

Status GetHead(SqQueue Q, QElemType &e)
{
// 若队列不空，则用e返回队头元素，并返回OK，否则返回ERROR
	if(Q.front==Q.rear) return ERROR;
	e=Q.base[Q.front];
	return OK;
}

int QueueLength(SqQueue Q)
{
// 返回Q的元素个数
	return Q.rear%MAXQSIZE-Q.front%MAXQSIZE;
}

某银行有一个客户办理业务站，在一天内随机地有客户到达，设每位客户的业务办理时间是某个范围内的值。设只有一个窗口，一位业务人员，要求程序模拟统计在
一天时间内，所有客户的平均等待时间。模拟数据按客户到达的先后顺序依次由键盘输入，对应每位客户有两个数据，到达时刻和需要办理业务的时间。
```

**输入**

```
第一行：一天内的客户总人数n
第二行：第一个客户的到达时刻和需要办理业务的时间
第三行：第二个客户的到达时刻和需要办理业务的时间
……
第n行：第n - 1个客户的到达时刻和需要办理业务的时间
第n + 1行：第n 个客户的到达时刻和需要办理业务的时间
```

**输出**

```
第一行：所有客户的平均等待时间（精确到小数点后2位）
```

**样例输入**

```
3
1 3
2 1
3 5
```

**样例输出**

```
1.33
```

**解析**

**题目要求**：模拟单窗口银行的客户服务过程，客户按到达先后顺序排队办理业务，计算并输出所有客户的平均等待时间（保留两位小数）。

**解题思路**：由于只有一个窗口且客户按到达顺序给出，本质上是顺序模拟。使用变量 `finish` 记录"柜台为上一位客户完成服务的时刻"。对每位客户（到达时刻为 a，办理耗时为 t），处理逻辑如下：
- 若客户到达时柜台已空闲（`finish < a`），则该客户无需等待，柜台从其到达时刻 a 开始服务，此时先将 `finish` 更新为 a；
- 该客户的**等待时间** = `finish - a`（即柜台开始为其服务的时刻减去其到达时刻）；
- 服务结束后，柜台空闲时刻向后推移：`finish += t`。

将所有客户的等待时间累加，最后除以总人数即可得到平均等待时间。

**算法分析**：参考答案保留题目给出的循环队列基本操作，将客户到达时刻和办理耗时依次入队后再按先来先服务顺序出队模拟。每位客户只入队、出队一次，时间复杂度 O(n)，空间复杂度 O(n)。

**注意事项**：时刻值可能较大，建议使用 `long long` 类型存储 `finish` 以避免整数溢出。

**C++ 参考答案**

```cpp
#include <malloc.h>
#include <stdio.h>
#include <stdlib.h>
#define OK 1
#define ERROR 0
typedef int Status; // Status是函数的类型,其值是函数结果状态代码，如OK等
typedef int QElemType;
#define MAXQSIZE 100 // 最大队列长度(对于循环队列，最大队列长度要减1)

typedef struct {
    QElemType *base; // 初始化的动态分配存储空间
    int front;       // 头指针,若队列不空,指向队列头元素
    int rear;        // 尾指针,若队列不空,指向队列尾元素的下一个位置
} SqQueue;

Status InitQueue(SqQueue &Q) {
    Q.base = (QElemType *)malloc(MAXQSIZE * sizeof(QElemType));
    if (!Q.base)
        exit(1);
    Q.rear = Q.front = 0;
    return OK;
}

Status EnQueue(SqQueue &Q, QElemType e) {
    if ((Q.rear + 1) % MAXQSIZE == Q.front)
        return ERROR;
    Q.base[Q.rear] = e;
    Q.rear = (Q.rear + 1) % MAXQSIZE;
    return OK;
}

Status DeQueue(SqQueue &Q, QElemType &e) {
    if (Q.front == Q.rear)
        return ERROR;
    e = Q.base[Q.front];
    Q.front = (Q.front + 1) % MAXQSIZE;
    return OK;
}

Status GetHead(SqQueue Q, QElemType &e) {
    if (Q.front == Q.rear)
        return ERROR;
    e = Q.base[Q.front];
    return OK;
}

int QueueLength(SqQueue Q) {
    return (Q.rear - Q.front + MAXQSIZE) % MAXQSIZE;
}

int main() {
    int n, arriveTime, serviceTime;
    SqQueue arrive, service;
    InitQueue(arrive);
    InitQueue(service);
    scanf("%d", &n);
    for (int i = 0; i < n; i++) {
        scanf("%d%d", &arriveTime, &serviceTime);
        EnQueue(arrive, arriveTime);
        EnQueue(service, serviceTime);
    }

    int finish = 0;
    double wait = 0;
    while (DeQueue(arrive, arriveTime) == OK && DeQueue(service, serviceTime) == OK) {
        if (finish < arriveTime)
            finish = arriveTime;
        wait += finish - arriveTime;
        finish += serviceTime;
    }
    printf("%.2f\n", wait / n);
    return 0;
}
```

## 26. 18937 阿克曼(Ackmann)函数

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18937&access=bbbfd741cedf2055b00932a0c5f4ae2b&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
阿克曼(Ackmann)函数A(m，n)中，m，n定义域是非负整数(m≤3,n≤10)，函数值定义为：
```

**输入**

```
输入m和n。
```

**输出**

```
函数值。
```

**样例输入**

```
2 3
```

**样例输出**

```
9
```

**解析**

**题目要求**：根据阿克曼函数的定义，计算并输出 A(m,n) 的值，其中 m 和 n 的取值范围为 m<=3、n<=10。

**解题思路**：阿克曼函数是经典的非原始递归函数，其定义本身即为分段递归形式，直接按照定义编写递归函数即可：
- `A(0, n) = n + 1`（递归边界）；
- `A(m, 0) = A(m-1, 1)`（n 为 0 时的递推）；
- `A(m, n) = A(m-1, A(m, n-1))`（嵌套递归，注意函数参数中包含了对自身的递归调用）。

在本题限定的数据范围内（m<=3, n<=10），朴素递归不会产生栈溢出问题，可直接通过。

**注意事项**：阿克曼函数增长极为迅速（`A(4,2)` 已是天文数字），这正是题目限制 m<=3 的原因。返回值建议使用 `long long` 类型以防止整数溢出。

**C++ 参考答案**

```cpp
#include <iostream>
using namespace std;
// 阿克曼函数：严格按照定义的三种情况进行递归计算
long long A(int m, int n) {
    if (m == 0)
        return n + 1; // 情况一：A(0,n) = n+1，递归边界
    if (n == 0)
        return A(m - 1, 1);       // 情况二：A(m,0) = A(m-1,1)
    return A(m - 1, A(m, n - 1)); // 情况三：A(m,n) = A(m-1, A(m,n-1))，嵌套递归
}
int main() {
    int m, n;
    cin >> m >> n;
    cout << A(m, n);
}
```
# 拓展习题2

## 27. 18933 括号匹配问题

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18933&access=bd18b5f29a0a60dbe076525648ff88c8&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
来源于POJ3704。
在某个字符串（长度不超过100）中有左括号、右括号和大小写字母；
规定（与常见的算数式子一样）任何一个左括号都从内到外与在它右边且距离最近的右括号匹配。
写一个程序，找到无法匹配的左括号和右括号，输出原来字符串，并在下一行标出不能匹配的括号。
不能匹配的左括号用"$"标注,不能匹配的右括号用"?"标注.
```

**输入**

```
输入包括多组数据，每组数据一行，包含一个字符串，只包含左右括号和大小写字母，字符串长度不超过100。
```

**输出**

```
对每组输出数据，输出两行。
第一行包含原始输入字符，第二行由"$","?"和空格组成，"$"和"?"表示与之对应的左括号和右括号不能匹配。
```

**样例输入**

```
((ABCD(x)
)(rttyy())sss)(
```

**样例输出**

```
((ABCD(x)
$$
)(rttyy())sss)(
?            ?$

Hint

读取多组数据时，可采用如下方法，其他scanf读到文件尾时会返回值EOF。
 char s[205];
 while(scanf("%s",s)!=EOF){}
```

**解析**

**题目要求**

给定一个由括号和大小写字母组成的字符串，要求找出所有无法匹配的括号：多余的左括号 `(` 在其正下方标注 `$`，多余的右括号 `)` 标注 `?`，其余位置（字母及已成功匹配的括号）一律以空格填充。先原样输出原始字符串，再输出标记行。输入包含多组数据，需读取至文件末尾。

**解题思路**

括号匹配是栈（Stack）的经典应用场景。核心思想是利用栈记录尚未找到匹配右括号的左括号下标。

**算法分析**

从左至右逐字符扫描字符串，按如下规则处理：

- 遇到 `(`：将其下标压入栈中，表示该左括号等待匹配。
- 遇到 `)`：若栈为空，说明该右括号在前方不存在可匹配的左括号，属于多余右括号，在对应位置标注 `?`；若栈非空，则与栈顶左括号成功配对，弹出栈顶元素。
- 遇到字母：无需处理，直接跳过。

扫描结束后，栈中残留的所有下标对应的左括号均未找到匹配的右括号，逐一在其对应位置标注 `$`。

**注意事项**

1. 标记数组的长度须与原字符串等长，初始值全部设为空格。
2. 输出标记行时，即便末尾为空格也须完整输出（行尾空格不可省略，否则将与样例输出不一致）。
3. 本题涉及多组数据输入，可使用 `while(getline(cin,s))` 循环读取至文件末尾。
4. 时间复杂度：O(n)；空间复杂度：O(n)。

**C++ 参考答案**

```cpp
#include <iostream>
#include <stack>
#include <string>
#include <vector>
using namespace std;
int main() {
    string s;
    while (getline(cin, s)) {
        vector<char> mark(s.size(), ' ');
        stack<int> st;
        for (int i = 0; i < (int)s.size(); i++) {
            if (s[i] == '(')
                st.push(i);
            else if (s[i] == ')') {
                if (st.empty())
                    mark[i] = '?';
                else
                    st.pop();
            }
        }
        while (!st.empty()) {
            mark[st.top()] = '$';
            st.pop();
        }
        cout << s << "\n";
        for (char c : mark)
            cout << c;
        cout << "\n";
    }
}
```

## 28. 19009 后缀表达式

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19009&access=6b91073be46a7ca1c52834e3e1651b29&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
人最熟悉的是中缀表达式,但计算机比较难处理中缀表达式,所以往往将中缀表达式改为后缀表达式。
后缀表达式，又称逆波兰式。现在从键盘读入一个后缀表达式，只含有0-9组成的运算数及加（+）、减（—）、乘（*）、除（/）四种运算符。
每个运算数之间用一个空格隔开，题目所使用的运算数均小于10，并确保所给的表达式合法。以@作为结束标志。
```

**输入**

```
一个后缀表达式。
```

**输出**

```
表达式结果。
```

**样例输入**

```
6 9 + 4 3 *-@
```

**样例输出**

```
3
```

**解析**

**题目要求**

给定一个后缀表达式（逆波兰式），例如 `6 9 + 4 3 *-@`，要求计算并输出其运算结果。运算数均为一位数字（0~9），运算符仅包含 `+ - * /`，数字之间以空格分隔，以 `@` 作为结束标志。

**解题思路**

后缀表达式的求值是栈的经典应用之一。其核心规则为：遇到数字则入栈，遇到运算符则弹出两个操作数进行计算，再将结果压回栈中。

**算法分析**

从左至右逐字符处理表达式：

- 若为数字字符：将其转换为对应的整数值后压入栈中。
- 若为运算符：连续弹出栈顶的两个数。需注意操作数的顺序——先弹出的为右操作数 `b`，后弹出的为左操作数 `a`，计算 `a op b` 后将结果压回栈。
- 若为空格：跳过不处理；遇到 `@` 时终止循环。

全部处理完毕后，栈中唯一剩余的元素即为表达式的最终结果。以样例 `6 9 + 4 3 * -` 验证：首先 6、9 入栈，遇 `+` 弹出 9 和 6，计算 6+9=15 并入栈；随后 4、3 入栈，遇 `*` 计算 4×3=12 并入栈；最后遇 `-` 计算 15-12=3，与样例输出一致。

**注意事项**

1. 减法和除法对操作数顺序敏感，必须遵循"后弹出者为左操作数、先弹出者为右操作数"的规则，否则将得到错误结果。
2. 题目保证表达式合法，无需额外处理除零等异常情况。
3. 时间复杂度：O(n)；空间复杂度：O(n)。

**C++ 参考答案**

```cpp
#include <ctype.h>
#include <iostream>
#include <stack>
using namespace std;
int main() {
    stack<int> st;
    char c;
    while (cin.get(c)) {
        if (c == '@')
            break;
        if (isspace((unsigned char)c))
            continue;
        if (isdigit((unsigned char)c))
            st.push(c - '0');
        else {
            int b = st.top();
            st.pop();
            int a = st.top();
            st.pop();
            if (c == '+')
                st.push(a + b);
            else if (c == '-')
                st.push(a - b);
            else if (c == '*')
                st.push(a * b);
            else
                st.push(a / b);
        }
    }
    cout << st.top();
}
```

## 29. 18932 出栈序列合法性判定

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18932&access=1222379939c9435cb72a7964910ec236&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
每年期末考试必考题目。

一个栈的进栈序列是a、b、c、d、e，则可能的出栈序列是（  ）。

A．abecd         B．decba         C．dceab        D．cabde

输入两个整数序列，第一个序列表示栈的压入顺序，请判断第二个序列是否可能为该栈的弹出顺序。

假设压入栈的所有数字均不相等。例如序列1,2,3,4,5是某栈的压入顺序，序列4,5,3,2,1是该压栈序列对应的一个弹出序列，

但4,3,5,1,2就不可能是该压栈序列的弹出序列。（注意：这两个序列的长度是相等的）
```

**输入**

```
第一行一个整数n，表示输入序列的长度。(1<=n<=10000)

第二行n个整数，表示栈的压入顺序。

第三行n个整数，表示栈的出栈顺序。
```

**输出**

```
如果是弹出序列，输出yes，否则输出no。
```

**样例输入**

```
5
1 2 3 8 6
8 6 3 2 1
```

**样例输出**

```
yes
```

**解析**

**题目要求**

给定一个栈的入栈序列和一个待验证的出栈序列，判断该出栈序列是否可能由该栈产生。若可能则输出 `yes`，否则输出 `no`。

**解题思路**

借助一个辅助栈模拟整个入栈和出栈过程。用指针 `j` 追踪出栈序列中当前期望被弹出的元素位置，通过"能弹则弹"的贪心策略进行判定。

**算法分析**

1. 按入栈序列的顺序，逐个将元素压入辅助栈。
2. 每次入栈后，反复检查：若栈非空且栈顶元素等于出栈序列中当前期望的元素 `out[j]`，则弹出栈顶并将 `j` 前移一位。
3. 入栈序列全部处理完毕后，若 `j` 已到达出栈序列末尾（即 `j == n`），则表明出栈序列合法，输出 `yes`；否则输出 `no`。

上述贪心策略的正确性可作如下论证：某个元素只有处于栈顶时才可能被弹出。当栈顶元素恰好是当前所需弹出的元素时，必须立即将其弹出——延迟弹出不会带来任何收益，因为后续入栈的元素只会将其压在更深处。

**注意事项**

1. 入栈和出栈序列中的数值为题目给定的具体整数，不一定是 1~n 的排列（例如样例中出现了数值 8），因此必须按数值严格比较，不可将元素简单视为 1 到 n 的编号。
2. 每个元素最多入栈和出栈各一次，整体时间复杂度为 O(n)，n 最大为 10000，完全满足时限要求。
3. 空间复杂度：O(n)。

**C++ 参考答案**

```cpp
#include <iostream>
#include <stack>
#include <vector>
using namespace std;
int main() {
    int n;
    cin >> n;
    vector<int> in(n), out(n);
    for (int &i : in)
        cin >> i;
    for (int &i : out)
        cin >> i;
    stack<int> st;
    int j = 0;
    for (int x : in) {
        st.push(x);
        while (!st.empty() && j < n && st.top() == out[j]) {
            st.pop();
            j++;
        }
    }
    cout << (j == n ? "yes" : "no");
}
```

## 30. 18715 出栈序列

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18715&access=c056ef822bbaf2a23809e5d4026449e5&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
一种简洁的栈定义方法如下
int st[1000],top=0;//以top作为栈顶指针，top==0为空栈
st[top++]=x;//把x入栈，栈顶指针+1
top--;//出栈
现在有一个1-n的排列，入栈序列已知，请给出字典序最大的出栈序列。
```

**输入**

```
第一行一个整数n。(1<=n<=100)
第二行n个整数，数据确保为1-n的排列。
```

**输出**

```
输出n个整数，既字典序最大的出栈序列。
```

**样例输入**

```
5
1 2 4 5 3
```

**样例输出**

```
5 4 3 2 1
```

**解析**

**题目要求**

给定一个 1~n 排列的入栈序列，要求构造出一个栈操作方案，使得最终的出栈序列字典序最大，并输出该出栈序列。

**解题思路**

采用贪心策略：为了使出栈序列字典序最大，应尽可能让较大的元素优先出栈。对于当前栈顶元素，若其大于所有尚未入栈的元素，则应立即将其弹出；否则应继续入栈新元素，等待更大的元素出现后再弹出。

**算法分析**

1. 预处理后缀最大值数组 `suf[i]`，表示入栈序列中第 i 个位置之后（不含第 i 个）所有元素的最大值。
2. 从左到右遍历入栈序列，依次将每个元素压入辅助栈。
3. 每次入栈后，反复检查：若栈顶元素大于 `suf[i+1]`（即大于所有尚未入栈的元素），则弹出栈顶并将其加入出栈序列。
4. 遍历结束后，将栈中剩余元素依次弹出即可。

**注意事项**

1. 后缀最大值数组的预处理保证了每次贪心判断的正确性：栈顶元素若已超过所有未入栈元素，则不可能在后续获得更大的出栈值，此时应立即弹出。
2. 时间复杂度：O(n)；空间复杂度：O(n)。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;
int main() {
    int n;
    cin >> n;
    vector<int> a(n), suf(n + 1, 0), ans, st;
    for (int &i : a)
        cin >> i;
    for (int i = n - 1; i >= 0; i--)
        suf[i] = max(suf[i + 1], a[i]);
    for (int i = 0; i < n; i++) {
        st.push_back(a[i]);
        while (!st.empty() && st.back() > suf[i + 1]) {
            ans.push_back(st.back());
            st.pop_back();
        }
    }
    for (int i = 0; i < n; i++)
        cout << ans[i] << (i + 1 == n ? '\n' : ' ');
}
```

## 31. 18714 迷宫问题

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18714&access=1cab80dcef8e89699519ad57024633fb&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
迷宫是一个n*m的矩阵，玩家需要迷宫入口（坐标1,1）出发，寻找路径走到出口（n,m）。
请判断玩家能否从迷宫中走出。
```

**输入**

```
第一行两个整数n和m，代表n行m列。(1<=n,m<=10)
下面n行每行m个字符,0代表可以通行，1代表不可以通行。
```

**输出**

```
如果能从迷宫走出，输出yes，否则输出no。
```

**样例输入**

```
8 8
00100010
00100010
00001100
01110000
00010000
01000100
01110110
00001000
```

**样例输出**

```
yes

Hint

样例数据即为图片迷宫
```

**解析**

**题目要求**

给定一个 n×m 的迷宫矩阵，入口为 (1,1)，出口为 (n,m)。矩阵中 `0` 表示可通行的格子，`1` 表示障碍物。要求判断是否存在一条从入口到出口的可行路径。

**解题思路**

将迷宫视为一张图，每个可通行的格子为一个节点，相邻（上下左右）的可通行格子之间存在边。问题等价于判断起点 (0,0) 与终点 (n-1,m-1) 是否连通，可使用广度优先搜索（BFS）或深度优先搜索（DFS）解决。

**算法分析**

采用 BFS 实现：

1. 若起点 (0,0) 为 `0`，则将其入队并标记为已访问；若起点为 `1`，则直接输出 `no`。
2. 当队列非空时，取出队首格子，检查其上下左右四个方向的相邻格子。
3. 对于每个相邻格子，若其在矩阵范围内、值为 `0` 且未被访问过，则将其标记为已访问并入队。
4. BFS 结束后，检查终点 (n-1,m-1) 是否已被访问。若已访问则输出 `yes`，否则输出 `no`。

**注意事项**

1. 注意起点或终点本身可能为障碍物（值为 `1`），此时应直接判定不可达。
2. 时间复杂度：O(n×m)，每个格子最多被访问一次。
3. 空间复杂度：O(n×m)，用于访问标记数组和队列。

**C++ 参考答案**

```cpp
#include <iostream>
#include <queue>
#include <string>
#include <utility>
#include <vector>
using namespace std;
int main() {
    int n, m;
    cin >> n >> m;
    vector<string> g(n);
    for (auto &s : g)
        cin >> s;
    queue<pair<int, int>> q;
    vector<vector<int>> v(n, vector<int>(m));
    if (g[0][0] == '0') {
        q.push({0, 0});
        v[0][0] = 1;
    }
    int d[4][2] = {{1, 0}, {-1, 0}, {0, 1}, {0, -1}};
    while (!q.empty()) {
        auto [x, y] = q.front();
        q.pop();
        for (auto &e : d) {
            int nx = x + e[0], ny = y + e[1];
            if (nx >= 0 && nx < n && ny >= 0 && ny < m && !v[nx][ny] && g[nx][ny] == '0') {
                v[nx][ny] = 1;
                q.push({nx, ny});
            }
        }
    }
    cout << (v[n - 1][m - 1] ? "yes" : "no");
}
```

## 32. 19071 递归实现指数型枚举

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19071&access=438135eb38c62a8a8733cd5814d82fbd&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
递归实现指数型枚举是一种常用的DFS算法，复杂度是2^n，只能在n比较小的时候使用。
一般用于：从 1∼n 这 n 个整数中随机选取（或者有某些规则限制）任意多个，输出所有可能的选择方案。
其实背包问题也可以用这种方法解决，只是复杂度会比较高......
一个旅行者有一个最多能装 M 公斤的背包，现在有 n 件物品，它们的重量分别是W1，W2，...,Wn，旅行者最多能装多少重量。

本题目题面：
给你N个整数，从中选取任意多个（至少选择一个），输出所有可能的选择方案，
无需输出每个数字，只需要输出选择数字的和。
```

**输入**

```
第一样输入一个整数 n。
第二行输入n个整数。1<=n<=10
```

**输出**

```
输出所有的方案，注意输出要按字典序。
即按如下次序
a1
a1+a2
a1+a2+a3
a1+a2+a3......
a2
a2+a3
a2+a3+......
......
an
```

**样例输入**

```
3
240 300 360
```

**样例输出**

```
240
540
900
600
300
660
360

Hint

指数型枚举在每一步中都有两种选择，选中这个元素或不选中，对这两种情况分别递归即可。
```

**解析**

**题目要求**

给定 n 个整数，要求枚举所有非空子集，并输出每个子集中元素之和。输出须按字典序排列（即先确定第一个被选元素的位置，在此基础上再按序扩展后续元素）。

**解题思路**

采用深度优先搜索（DFS）实现指数型枚举。在每一步递归中，对于当前元素存在两种选择——选中或不选中。为保证输出按字典序排列，需要按索引从小到大的顺序依次决策。

**算法分析**

1. 定义递归函数 `dfs(st, sum)`，其中 `st` 为当前可选元素的起始索引，`sum` 为当前已选元素的累加和。
2. 从索引 `st` 开始，依次枚举每个元素 `a[i]`：选中该元素后，立即输出新的累加和 `sum + a[i]`，然后递归调用 `dfs(i+1, sum+a[i])` 继续向后扩展。
3. 上述设计自然地保证了字典序输出：以 `a[1]` 开头的所有方案先于以 `a[2]` 开头的方案输出，以此类推。

**注意事项**

1. 由于每个元素存在选与不选两种决策，递归树深度为 n，总方案数（含空集）为 2^n，因此时间复杂度为 O(2^n)。
2. 空间复杂度为 O(n)，即递归调用栈的最大深度。
3. 题目要求至少选择一个元素，因此空集不纳入输出。

**C++ 参考答案**

```cpp
#include <iostream>
using namespace std;
int n, a[15];
void dfs(int st, int sum) {
    for (int i = st; i <= n; i++) {
        int s = sum + a[i];
        cout << s << "\n";
        dfs(i + 1, s);
    }
}
int main() {
    cin >> n;
    for (int i = 1; i <= n; i++)
        cin >> a[i];
    dfs(1, 0);
}
```

## 33. 18712 递归实现组合

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18712&access=7692d0ab9bf0cc91ae0b1b8925aa2fc7&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
找出从自然数1、2、……、m中任取k个数的所有组合，组合中字典序小的先输出。
例如m=5，k=3，应输出
1 2 3
1 2 4
1 2 5
1 3 4
1 3 5
1 4 5
2 3 4
2 3 5
2 4 5
3 4 5
```

**输入**

```
两个整数m和k，(1<=k<=m<=10)
```

**输出**

```
按字典序输出所有组合
```

**样例输入**

```
5 2
```

**样例输出**

```
1 2
1 3
1 4
1 5
2 3
2 4
2 5
3 4
3 5
4 5
```

**解析**

**题目要求**

从自然数 1, 2, ..., m 中选取 k 个数，输出所有可能的组合。要求组合按字典序升序输出。

**解题思路**

采用递归（DFS）方式构造组合。每次从候选数中按递增顺序选取下一个数，由于始终保证后选的数大于先选的数，自然满足字典序输出。

**算法分析**

1. 定义递归函数 `dfs(x, cnt)`，其中 `x` 为当前可选数的最小值，`cnt` 为已选元素个数。
2. 若 `cnt == k`，表示已选满 k 个数，输出当前组合并返回。
3. 否则，从 `x` 到 `m` 依次枚举每个数 `i`，将其放入组合的第 `cnt` 个位置，递归调用 `dfs(i+1, cnt+1)`。
4. 递归过程中，每一层的选择都是严格递增的，因此生成的组合天然按字典序排列，无需额外排序。

**注意事项**

1. 时间复杂度取决于组合总数 C(m,k)，在 m≤10 的约束下完全可行。
2. 空间复杂度为 O(k)，即递归调用栈的最大深度。

**C++ 参考答案**

```cpp
#include <iostream>
using namespace std;
int m, k, sel[15];
void dfs(int x, int cnt) {
    if (cnt == k) {
        for (int i = 0; i < k; i++)
            cout << sel[i] << (i + 1 == k ? '\n' : ' ');
        return;
    }
    for (int i = x; i <= m; i++) {
        sel[cnt] = i;
        dfs(i + 1, cnt + 1);
    }
}
int main() {
    cin >> m >> k;
    dfs(1, 0);
}
```

## 34. 18928 递归实现全排列

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18928&access=9ec61a1009af7b6851c44152fa41fd43&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
把 1至n 这 n 个整数排成一行后随机打乱顺序，输出所有可能的次序。
```

**输入**

```
一个整数n。(1<=n<=9)
```

**输出**

```
按照从小到大的顺序输出所有方案，每行一个方案。
同一行相邻两个数用一个空格隔开。
对于两个不同的行，对应下标的数一一比较，字典序较小的排在前面。
```

**样例输入**

```
3
```

**样例输出**

```
1 2 3
1 3 2
2 1 3
2 3 1
3 1 2
3 2 1
```

**解析**

**题目要求**

输出 1 到 n 这 n 个整数的所有全排列，按字典序升序排列，每行输出一个排列。

**解题思路**

利用 C++ 标准库函数 `next_permutation` 可简洁地实现全排列的字典序枚举。该函数将当前排列变换为字典序的下一个排列，当所有排列均已枚举完毕时返回 `false`。

**算法分析**

1. 初始化排列为 1, 2, ..., n 的升序序列（这是字典序最小的排列）。
2. 输出当前排列，然后调用 `next_permutation` 将其变换为字典序的下一个排列。
3. 重复步骤 2，直到 `next_permutation` 返回 `false`，表示所有排列均已枚举完毕。
4. 由于初始排列为升序，且 `next_permutation` 严格按字典序递增生成，因此输出自然满足字典序要求。

**注意事项**

1. 全排列总数为 n!，当 n=9 时为 362880，在时限范围内可以接受。
2. 也可采用回溯法手动实现：用布尔数组记录每个数字的使用状态，按从小到大的顺序依次填入每一位，递归构造所有排列。
3. 时间复杂度：O(n! × n)；空间复杂度：O(n)。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;
int main() {
    int n;
    cin >> n;
    vector<int> a(n);
    for (int i = 0; i < (int)a.size(); i++)
        a[i] = i + 1;
    do {
        for (int i = 0; i < n; i++)
            cout << a[i] << (i + 1 == n ? '\n' : ' ');
    } while (next_permutation(a.begin(), a.end()));
}
```

## 35. 19044 平分物品（递归实现指数型枚举）

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19044&access=507d0f3bd2e1d4b8e7b339260f84f5ab&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
网易2021校招笔试-文本挖掘算法工程师（提前批）第一题

现在有n个物品，每一个物品都有一个价值，现在想将这些物品分给两个人，
要求这两个人每一个人分到的物品的价值总和相同（个数可以不同，总价值相同即可，
剩下的物品就需要扔掉，现在想知道最少需要扔多少价值的物品才能满足要求分给两个人。

要求：时间复杂度O(3^n)，空间复杂度O(n)
```

**输入**

```
第一行输入一个整数 T，代表有 T 组测试数据。
对于每一组测试数据，一行输入一个整数 n ，代表物品的个数。
接下来 n 个数，a[i] 代表每一个物品的价值。
1<= T <= 10
1 <= n <= 15
1 <= a[i] <= 100000
```

**输出**

```
对于每一组测试数据，输出一个答案代表最少需要扔的价值。
多组数据需要换行。

样例解释，扔掉第三个和第四个物品，然后将第一个物品和第五个物品给第一个人，
第二个物品给第二个人，每一个人分到的价值为60，扔掉的价值为20。
```

**样例输入**

```
1
5
30 60 5 15 30
```

**样例输出**

```
20

Hint

注意观察题目要求，估算出需要使用何种复杂度算法。
此题目n很小，用3的n次幂这种指数级复杂度可解，可使用基于指数型枚举的深度搜索dfs。
枚举时每个物品都有三种选择，给A，给B，都不给
```

**解析**

**题目要求**

有 n 个物品，每个物品具有给定的价值。需将物品分给两人，使两人获得的价值总和相等（个数可以不同），未分配的物品将被丢弃。要求最小化丢弃物品的总价值。

**解题思路**

对每个物品存在三种互斥的决策：分给第一个人（A）、分给第二个人（B）、丢弃。因此可采用 DFS 枚举所有 3^n 种分配方案，在满足两人价值相等的条件下，最大化两人获得的价值总和，从而最小化丢弃量。

**算法分析**

1. 定义递归函数 `dfs(i, x, y)`，其中 `i` 为当前待决策的物品索引，`x` 和 `y` 分别为 A 和 B 当前已累计获得的价值。
2. 对于第 `i` 个物品，分别尝试三种决策：
   - 分给 A：递归调用 `dfs(i+1, x+a[i], y)`
   - 分给 B：递归调用 `dfs(i+1, x, y+a[i])`
   - 丢弃：递归调用 `dfs(i+1, x, y)`
3. 当 `i == n`（所有物品均已决策完毕）时，若 `x == y`，则更新 `best = max(best, x+y)`，记录满足平分条件的最大分配总价值。
4. 最终答案为 `tot - best`，其中 `tot` 为所有物品的价值总和。

**注意事项**

1. 时间复杂度为 O(3^n)，由于 n 最大为 15，3^15 ≈ 1.4×10^7，在时限内可行。
2. 空间复杂度为 O(n)，即递归调用栈的最大深度。
3. 题目要求时间复杂度 O(3^n) 和空间复杂度 O(n)，上述方案恰好满足。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;
int n;
vector<long long> a;
long long tot, best;
void dfs(int i, long long x, long long y) {
    if (i == n) {
        if (x == y)
            best = max(best, x + y);
        return;
    }
    dfs(i + 1, x + a[i], y);
    dfs(i + 1, x, y + a[i]);
    dfs(i + 1, x, y);
}
int main() {
    int T;
    cin >> T;
    while (T--) {
        cin >> n;
        a.resize(n);
        tot = 0;
        for (auto &x : a) {
            cin >> x;
            tot += x;
        }
        best = 0;
        dfs(0, 0, 0);
        cout << tot - best << "\n";
    }
}
```

## 36. 18713 整数的分解

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18713&access=175fcecb846e6781321e09a5e8b01965&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
输出一个正整数n的分解形式。例如,当n=4时，输出：
	4=4
	4=3+1
	4=2+2
	4=2+1+1
	4=1+1+1+1
共计 5 种形式。
当n=7时，共有15种形式。
当n=10时，共有42种形式。
```

**输入**

```
一个整数n(1<=n<=10)。
```

**输出**

```
n的全部分解形式，注意分解式中数字值大的排在前面，如第一个数字值相同，那么比较第二个数字。
```

**样例输入**

```
4
```

**样例输出**

```
4=4
4=3+1
4=2+2
4=2+1+1
4=1+1+1+1
```

**解析**

**题目要求**

输出正整数 n 的所有正整数分拆形式。要求分拆式中的数字按非递增顺序排列，各分拆式之间按字典序降序输出（即较大的数字优先出现在前面）。

**解题思路**

采用递归回溯法枚举所有分拆方案。在每一步递归中，限制下一个选取的数不超过上一个选取的数，以保证分拆式呈非递增排列，同时避免产生重复的分拆方案。

**算法分析**

1. 定义递归函数 `dfs(rem, mx)`，其中 `rem` 为剩余待分拆的数值，`mx` 为当前允许选取的最大数值。
2. 若 `rem == 0`，表示分拆完成，按格式输出当前方案。
3. 否则，从 `min(rem, mx)` 开始，由大到小枚举下一个分拆数 `x`，将 `x` 加入当前分拆序列后递归调用 `dfs(rem-x, x)`，递归返回后将 `x` 从序列中移除（回溯）。
4. 由大到小枚举 `x` 的策略保证了输出结果天然满足字典序降序排列的要求。

**注意事项**

1. 限制 `x <= mx` 可确保分拆序列非递增，有效避免诸如 `3+1` 和 `1+3` 这样的重复枚举。
2. 时间复杂度与整数分拆数 p(n) 相关；空间复杂度为 O(n)。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;
int n;
vector<int> p;
void dfs(int rem, int mx) {
    if (rem == 0) {
        cout << n << "=";
        for (size_t i = 0; i < p.size(); i++)
            cout << (i ? "+" : "") << p[i];
        cout << "\n";
        return;
    }
    for (int x = min(rem, mx); x >= 1; x--) {
        p.push_back(x);
        dfs(rem - x, x);
        p.pop_back();
    }
}
int main() {
    cin >> n;
    dfs(n, n);
}
```

## 37. 18717 舞伴问题

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18717&access=885d75142100dd28b9a2897832f2c825&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
假设在周末舞会上，男士们和女士们进入舞厅时，各自排成一队。
跳舞开始时，依次从男队和女队的队头上各出一人配成舞伴。
规定每个舞曲能有一对跳舞者。若两队初始人数不相同，则较长的那一队中未配对者等待下一轮舞曲。
现要求写一个程序，模拟上述舞伴配对问题。
```

**输入**

```
第一行两个正整数n和m，分别代表男队和女队的人数，规定男队编号从1至n，女队编号从1至m。
第二行输入一个正整数k，表示第k对舞伴。(1<=n,m,k<=100)
```

**输出**

```
输出第k对舞伴的两个编号。
```

**样例输入**

```
4 6
7
```

**样例输出**

```
3 1
```

**解析**

**题目要求**

模拟舞会中的男女配对过程。男队有 n 人（编号 1~n），女队有 m 人（编号 1~m），每首舞曲从两队队头各取一人配对。当某队成员全部出队后，从队头重新开始（即循环出队）。要求输出第 k 对舞伴中男女各自的编号。

**解题思路**

由题意可知，男女队列的出队过程具有周期性。男队以 n 为周期循环，女队以 m 为周期循环。因此无需真正模拟整个出队过程，可直接通过取模运算求解。

**算法分析**

第 k 对舞伴（k 从 1 开始计数）中：
- 男队编号为 `(k-1) mod n + 1`
- 女队编号为 `(k-1) mod m + 1`

以样例为例：n=4, m=6, k=7。男队编号 = (7-1) mod 4 + 1 = 3，女队编号 = (7-1) mod 6 + 1 = 1，输出 `3 1`，与样例一致。

**注意事项**

1. 本题本质为取模运算，无需模拟完整的队列操作，时间复杂度为 O(1)。
2. 需注意 k 的取值从 1 开始，因此在取模前须先减 1，取模后再加 1。

**C++ 参考答案**

```cpp
#include <iostream>
using namespace std;
int main() {
    long long n, m, k;
    cin >> n >> m >> k;
    cout << (k - 1) % n + 1 << ' ' << (k - 1) % m + 1;
}
```

## 38. 18719 填涂颜色

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18719&access=58d405e3817d35d38fc6aa9ca0b61b9e&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10 KB；Language: G++;GCC

**题目描述**

```
由数字0组成的方阵中，有一任意形状闭合圈，闭合圈由数字1构成，围圈时只走上下左右4个方向。
现要求把闭合圈内的所有空间都填写成2.例如：6×6的方阵（n=6），涂色前和涂色后的方阵如下：
涂色前：
0 0 0 0 0 0
0 0 1 1 1 1
0 1 1 0 0 1
1 1 0 0 0 1
1 0 0 0 0 1
1 1 1 1 1 1
涂色后：
0 0 0 0 0 0
0 0 1 1 1 1
0 1 1 2 2 1
1 1 2 2 2 1
1 2 2 2 2 1
1 1 1 1 1 1
```

**输入**

```
每组测试数据第一行一个整数n(1≤n≤30)
接下来n行，由0和1组成的n×n的方阵。
方阵内只有一个闭合圈，圈内至少有一个0。
```

**输出**

```
已经填好数字2的完整方阵。
```

**样例输入**

```
6
0 0 0 0 0 0
0 0 1 1 1 1
0 1 1 0 0 1
1 1 0 0 0 1
1 0 0 0 0 1
1 1 1 1 1 1
```

**样例输出**

```
0 0 0 0 0 0
0 0 1 1 1 1
0 1 1 2 2 1
1 1 2 2 2 1
1 2 2 2 2 1
1 1 1 1 1 1

Source

	洛谷 P1162
```

**解析**

**题目要求**

给定一个 n×n 的方阵，其中 `1` 构成一个闭合圈，要求将闭合圈内部的所有 `0` 修改为 `2`，并输出完整的方阵。

**解题思路**

采用"反向标记"的思想：不直接判定哪些 `0` 位于闭合圈内部，而是先从方阵外部出发，标记所有能够从外部到达的 `0`。标记完成后，未被标记的 `0` 即为闭合圈内部的格子，将其修改为 `2`。

**算法分析**

1. 在原方阵外围扩展一圈 `0`（将矩阵规模扩展为 (n+2)×(n+2)），确保外部区域连通。扩展圈的坐标范围为第 0 行/列和第 n+1 行/列。
2. 从 (0,0) 开始进行 BFS（或 DFS），标记所有能够从外部到达的 `0` 格子。
3. BFS 结束后，遍历原方阵（第 1 行/列到第 n 行/列）：若某个格子为 `0` 且未被 BFS 标记，则它位于闭合圈内部，将其修改为 `2`。
4. 输出最终的方阵。

**注意事项**

1. 外围扩展一圈是关键步骤，它保证了即使闭合圈与方阵边缘相邻，外部的 `0` 也能被正确地全部标记。
2. 时间复杂度：O(n^2)；空间复杂度：O(n^2)。

**C++ 参考答案**

```cpp
#include <iostream>
#include <queue>
#include <utility>
#include <vector>
using namespace std;
int main() {
    int n;
    cin >> n;
    vector<vector<int>> a(n + 2, vector<int>(n + 2));
    for (int i = 1; i <= n; i++)
        for (int j = 1; j <= n; j++)
            cin >> a[i][j];
    queue<pair<int, int>> q;
    vector<vector<int>> vis(n + 2, vector<int>(n + 2));
    q.push({0, 0});
    vis[0][0] = 1;
    int d[4][2] = {{1, 0}, {-1, 0}, {0, 1}, {0, -1}};
    while (!q.empty()) {
        auto [x, y] = q.front();
        q.pop();
        for (auto &e : d) {
            int nx = x + e[0], ny = y + e[1];
            if (nx >= 0 && nx <= n + 1 && ny >= 0 && ny <= n + 1 && !vis[nx][ny] &&
                a[nx][ny] == 0) {
                vis[nx][ny] = 1;
                q.push({nx, ny});
            }
        }
    }
    for (int i = 1; i <= n; i++) {
        for (int j = 1; j <= n; j++) {
            if (a[i][j] == 0 && !vis[i][j])
                a[i][j] = 2;
            cout << a[i][j] << (j == n ? '\n' : ' ');
        }
    }
}
```

## 39. 18720 迷宫问题 （最短路径）

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18720&access=3e46b3b8e410fdfc49f73c705bf49d72&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10 KB；Language: G++;GCC

**题目描述**

```
迷宫是一个n*m的矩阵，玩家需要迷宫入口（坐标1,1）出发，寻找路径走到出口（n,m）。
请判断玩家能否从迷宫中走出，如果能走出迷宫输出，输出最短的路径长度，否则输出-1。
```

**输入**

```
第一行两个整数n和m，代表n行m列。(1<=n,m<=10)
下面n行每行m个字符,0代表可以通行，1代表不可以通行。
```

**输出**

```
如果能从迷宫走出，输出最短的路径长度，否则输出-1。
```

**样例输入**

```
8 8
00100010
00100010
00001100
01110000
00010000
01000100
01110110
00001000
```

**样例输出**

```
16
```

**解析**

**题目要求**

给定一个 n×m 的迷宫矩阵，入口为 (1,1)，出口为 (n,m)。`0` 表示可通行，`1` 表示障碍物。要求输出从入口到出口的最短路径长度（以移动步数计），若不可达则输出 -1。

**解题思路**

BFS（广度优先搜索）是求解无权图最短路径的标准算法。BFS 首次到达某个节点时所经过的路径长度即为从起点到该节点的最短距离，这是由 BFS 按层次扩展的性质所保证的。

**算法分析**

1. 初始化距离数组 `dist`，所有元素设为 -1（表示未访问）。
2. 若起点 (0,0) 可通行，则令 `dist[0][0] = 0` 并将起点入队。
3. 当队列非空时，取出队首格子，检查其上下左右四个方向的相邻格子。对于每个可通行且未被访问的相邻格子（`dist` 值为 -1），令其距离为当前格子的距离加 1，并将其入队。
4. 最终输出 `dist[n-1][m-1]`。若该值仍为 -1，说明终点不可达。

**注意事项**

1. BFS 保证首次到达终点时即为最短路径，因此无需额外优化。
2. 时间复杂度：O(n×m)，每个格子最多入队一次。
3. 空间复杂度：O(n×m)。

**C++ 参考答案**

```cpp
#include <iostream>
#include <queue>
#include <string>
#include <utility>
#include <vector>
using namespace std;
int main() {
    int n, m;
    cin >> n >> m;
    vector<string> g(n);
    for (auto &s : g)
        cin >> s;
    vector<vector<int>> dist(n, vector<int>(m, -1));
    queue<pair<int, int>> q;
    if (g[0][0] == '0') {
        dist[0][0] = 0;
        q.push({0, 0});
    }
    int d[4][2] = {{1, 0}, {-1, 0}, {0, 1}, {0, -1}};
    while (!q.empty()) {
        auto [x, y] = q.front();
        q.pop();
        for (auto &e : d) {
            int nx = x + e[0], ny = y + e[1];
            if (nx >= 0 && nx < n && ny >= 0 && ny < m && dist[nx][ny] < 0 && g[nx][ny] == '0') {
                dist[nx][ny] = dist[x][y] + 1;
                q.push({nx, ny});
            }
        }
    }
    cout << dist[n - 1][m - 1];
}
```

## 40. 19118 用队列计算杨辉三角

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19118&access=c1b3cf82965278fe9ec423f097ebcbf3&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10 KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
杨辉三角，是二项式系数在三角形中的一种几何排列，中国南宋数学家杨辉1261年所著的《详解九章算法》一书中出现。
在欧洲，帕斯卡（1623----1662）在1654年发现这一规律，所以这个表又叫做帕斯卡三角形。
杨辉三角与组合关系密切。
第n行的m个数可表示为 C(n-1，m-1)，即为从n-1个不同元素中取m-1个元素的组合数。
第n行的第m个数和第n-m+1个数相等 ，为组合数性质之一。

请输出杨辉三角的第n行，由于杨辉三角n较大时数值较大，会超出整数范围，
因此请将结果的每个数字对1000000007求余。
```

**输入**

```
输入一个整数n。
```

**输出**

```
输出杨辉三角的第n行，每个数字对1000000007求余。
```

**样例输入**

```
5
```

**样例输出**

```
1 4 6 4 1
```

**解析**

**题目要求**

输出杨辉三角（帕斯卡三角形）的第 n 行，每个数值对 10^9+7 取模。杨辉三角第 n 行的第 m 个数等于组合数 C(n-1, m-1)。

**解题思路**

利用一维数组进行逐行递推。杨辉三角的递推关系为：当前行的第 j 个数等于上一行的第 j 个数与第 j-1 个数之和。为避免在更新过程中覆盖尚未使用的上一行数据，应从后向前进行更新。

**算法分析**

1. 初始化一维数组 `row = [1]`，对应第 1 行。
2. 从第 2 行递推至第 n 行：每行末尾追加一个 `1`，然后从后向前（即从 `row.size()-2` 到索引 `1`）更新每个位置：`row[j] = (row[j] + row[j-1]) % MOD`。
3. 从后向前更新的关键在于：更新 `row[j]` 时所引用的 `row[j]` 和 `row[j-1]` 均仍保留着上一行的值，从而避免了覆盖问题。
4. 递推完成后，`row` 中存储的即为第 n 行的各个数值。

**注意事项**

1. 由于数值可能超出整数范围，每一步加法运算后均须对 MOD（10^9+7）取模。
2. 时间复杂度：O(n^2)，共需 n-1 次迭代，每次迭代最多更新 n 个元素。
3. 空间复杂度：O(n)，仅需一维数组。

**C++ 参考答案**

```cpp
#include <iostream>
#include <vector>
using namespace std;
const long long MOD = 1000000007;
int main() {
    int n;
    cin >> n;
    vector<long long> row(1, 1);
    for (int i = 2; i <= n; i++) {
        row.push_back(1);
        for (int j = (int)row.size() - 2; j >= 1; j--)
            row[j] = (row[j] + row[j - 1]) % MOD;
    }
    for (int i = 0; i < n; i++)
        cout << row[i] << (i + 1 == n ? '\n' : ' ');
}
```

## 41. 18718 航行

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18718&access=cd1249065b7a33b8283b9a88a814cee5&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10 KB；Language: G++;GCC

**题目描述**

```
银河帝国正走向覆亡。为保留文明的种子，你需要驾驶飞船将一批"颛家"从帝国首都护送至银河边缘的基地。
现在已知航线是一条直线，帝国首都为起点（坐标0），基地为终点（坐标L），在这条航线上有N个空间站可以补充飞船的能源。
第i个空间站的坐标为ai，飞船停靠在第i个空间站必须花费bi个银河币，同时让你的飞船能量恢复为最大值M。
出发前飞船的能量是满额的M，每一点能量都可以让飞船航行一个坐标单位。

现在你已经通过募捐(榨篇）获得了S个银河币，请计算下飞船能否到达基地。
```

**输入**

```
第一行输入四个个数字N,L,M,S；(1<=N<=200)  (1<=L<=20000)  (1<=M<=20000)  (0<=S<=20000)
接下来N行，每行输入两个数字，ai，bi (0<=ai<=L) (0<=bi<=20000)
```

**输出**

```
仅一行，如果能到达基地，输出Yes，否则输出No
```

**样例输入**

```
1 10000 5000 20000
5000 20000
```

**样例输出**

```
Yes

Hint

样例说明，飞船可以花费5000能量到达一号空间站，花光20000银河币补满能量后，再行驶5000到达基地。
算法设计要考虑边缘数据。例如本题目，可能存在无需补给就直接行驶到基地的情况，也能存在bi>s的情况。
```

**解析**

**题目要求**

在一条直线航线上，起点坐标为 0，终点坐标为 L，沿途分布有 N 个空间站。飞船初始能量为 M，每单位能量可航行一个坐标单位。在第 i 个空间站停靠需花费 b_i 个银河币，同时能量恢复至 M。现有 S 个银河币的预算，判断飞船能否在预算内到达终点。

**解题思路**

将起点、所有空间站和终点视为图中的节点，若两节点之间的距离不超过 M（飞船满能量时的最大航程），则可以从前者直达后者。问题转化为：在上述图中，求从起点到终点的最小花费路径，判断该花费是否不超过 S。可采用动态规划求解。

**算法分析**

1. 将起点（坐标 0，费用 0）和终点（坐标 L，费用 0）加入节点列表，与 N 个空间站一起按坐标升序排序。
2. 定义 `dp[i]` 为从起点到达第 i 个节点的最小累计花费，初始时 `dp[0] = 0`（起点），其余为无穷大。
3. 对于每个节点 i，枚举其后续所有满足距离约束（`坐标差 <= M`）的节点 j，进行状态转移：`dp[j] = min(dp[j], dp[i] + b_j)`。
4. 最终判定 `dp[终点]` 是否不超过 S。

**注意事项**

1. 须注意可能无需任何补给即可直接从起点到达终点的情况。
2. 某些空间站的停靠费用可能超过总预算 S，DP 过程会自动排除这些不可行的路径。
3. 时间复杂度：O(N^2)，在 N <= 200 的约束下完全可行。
4. 空间复杂度：O(N)。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <utility>
#include <vector>
using namespace std;
int main() {
    int N;
    long long L, M, S;
    cin >> N >> L >> M >> S;
    vector<pair<long long, long long>> st(N + 2);
    st[0] = {0, 0};
    for (int i = 1; i <= N; i++)
        cin >> st[i].first >> st[i].second;
    st[N + 1] = {L, 0};
    sort(st.begin(), st.end());
    const long long INF = 4e18;
    vector<long long> dp(N + 2, INF);
    dp[0] = 0;
    for (int i = 0; i < N + 2; i++)
        if (dp[i] < INF)
            for (int j = i + 1; j < N + 2 && st[j].first - st[i].first <= M; j++)
                dp[j] = min(dp[j], dp[i] + st[j].second);
    cout << (dp[N + 1] <= S ? "Yes" : "No");
}
```

## 42. 18960 素数环

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18960&access=fcedec1d4dad703a2a2171275117e609&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10 KB；Language: G++;GCC

**题目描述**

```
输入一个整数n，输出一个1至n组成的素数环。
素数环指的是任意相邻两数的和均为素数。要求这个素数环的字典序最小。
如果无法得到这样的素数环，输出-1。
```

**输入**

```
一个整数n (2<=n<=20)
```

**输出**

```
仅一行，满足条件的一个排列，两个数字间用空格分隔。
如果无法得到这样的素数环，输出-1。
```

**样例输入**

```
14
```

**样例输出**

```
1 2 3 4 7 6 13 10 9 14 5 8 11 12
```

**解析**

**题目要求**

将 1 到 n 这 n 个整数排成一个环，使得任意相邻两数之和均为素数。要求输出字典序最小的素数环；若不存在这样的排列，则输出 -1。

**解题思路**

采用回溯法（DFS）逐位构造排列。固定第一个数为 1（既保证字典序最小，又消除旋转等价带来的重复），然后从第 2 位开始，从小到大尝试填入尚未使用的数字，每次填入前检查其与前一位置数字之和是否为素数。当所有位置均填满后，还需额外验证首尾两数之和是否为素数。

**算法分析**

1. 预处理素数表：利用试除法标记 2 到 2n 范围内的所有素数，供后续快速查询。
2. 定义递归函数 `dfs(pos)`，表示当前正在填写第 `pos` 个位置（从 0 开始计数，`a[0]` 已固定为 1）。
3. 对于每个候选数 x（从 2 到 n，从小到大遍历），若 x 尚未使用且 `x + a[pos-1]` 为素数，则将 x 放入 `a[pos]`，标记为已使用，递归进入下一位置。
4. 当 `pos == n` 时，所有位置已填满，检查 `a[n-1] + a[0]` 是否为素数。若满足则找到一个合法解；由于搜索过程中始终按从小到大顺序尝试，第一个找到的解即为字典序最小的素数环。
5. 若回溯结束仍未找到合法解，输出 -1。

**注意事项**

1. 从小到大尝试候选数的策略保证了字典序最小性，首次找到的合法解即为所求。
2. 最坏情况下时间复杂度为 O(n!)，但由于素数条件的强力剪枝，实际运行效率远优于理论上界。
3. 空间复杂度为 O(n)。

**C++ 参考答案**

```cpp
#include <iostream>
using namespace std;
int n, a[25];
bool used[25], isP[50];
bool dfs(int pos) {
    if (pos == n) {
        return isP[a[n - 1] + a[0]];
    }
    for (int x = 2; x <= n; x++)
        if (!used[x] && isP[x + a[pos - 1]]) {
            used[x] = 1;
            a[pos] = x;
            if (dfs(pos + 1))
                return true;
            used[x] = 0;
        }
    return false;
}
int main() {
    cin >> n;
    for (int i = 2; i < 50; i++) {
        isP[i] = 1;
        for (int d = 2; d * d <= i; d++)
            if (i % d == 0)
                isP[i] = 0;
    }
    a[0] = 1;
    used[1] = 1;
    if (dfs(1)) {
        for (int i = 0; i < n; i++)
            cout << a[i] << (i + 1 == n ? '\n' : ' ');
    } else
        cout << -1;
}
```

## 43. 18931 分形

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18931&access=5de6e80bc639c7912a771df8f5ee0a6b&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10 KB；Language: G++;GCC

**题目描述**

```
分形，具有以非整数维形式充填空间的形态特征。

通常被定义为"一个粗糙或零碎的几何形状，可以分成数个部分，且每一部分都（至少近似地）是整体缩小后的形状"，即具有自相似的性质。

现在，定义"盒子分形"如下：

一级盒子分形：

   X
二级盒子分形：

   X X
    X
   X X
如果用B(n - 1)代表第n-1级盒子分形，那么第n级盒子分形即为：

  B(n - 1)        B(n - 1)

          B(n - 1)

  B(n - 1)        B(n - 1)
你的任务是绘制一个n级的盒子分形。
```

**输入**

```
输入一个不大于6的正整数n，代表要输出的盒子分形的等级。
```

**输出**

```
使用"X"符号输出对应等级的盒子分形。
```

**样例输入**

```
4
```

**样例输出**

```
X X   X X         X X   X X
 X     X           X     X
X X   X X         X X   X X
   X X               X X
    X                 X
   X X               X X
X X   X X         X X   X X
 X     X           X     X
X X   X X         X X   X X
         X X   X X
          X     X
         X X   X X
            X X
             X
            X X
         X X   X X
          X     X
         X X   X X
X X   X X         X X   X X
 X     X           X     X
X X   X X         X X   X X
   X X               X X
    X                 X
   X X               X X
X X   X X         X X   X X
 X     X           X     X
X X   X X         X X   X X

Hint

分形图可以用递归算法实现，规模为n的图形可以由规模为n-1的图形通过某种方式得到。
感兴趣的同学可以去看看类似题目 洛谷 P1498 南蛮图腾。
```

**解析**

**题目要求**

按照给定的递归定义，绘制 n 级盒子分形图案。一级分形为单个 `X`，n 级分形由 5 个 (n-1) 级分形分别放置在九宫格的四角和中心位置构成。

**解题思路**

分形具有自相似性，适合用递归方法实现。n 级图形可分解为 5 个 (n-1) 级子图形，分别位于一个虚拟九宫格的左上角、右上角、中心、左下角和右下角。

**算法分析**

1. n 级分形的边长为 3^(n-1)。初始化一个 3^(n-1) × 3^(n-1) 的字符画布，全部填充空格。
2. 定义递归函数 `draw(n, x, y)`，表示在画布的 (x, y) 位置开始绘制 n 级分形。
3. 基本情况：当 n=1 时，令 `g[x][y] = 'X'`。
4. 递归情况：计算 (n-1) 级分形的边长 `s = 3^(n-2)`，然后递归绘制 5 个子分形：
   - 左上角：`draw(n-1, x, y)`
   - 右上角：`draw(n-1, x, y + 2s)`
   - 中心：`draw(n-1, x + s, y + s)`
   - 左下角：`draw(n-1, x + 2s, y)`
   - 右下角：`draw(n-1, x + 2s, y + 2s)`
5. 输出时去除每行末尾的多余空格，以符合样例格式。

**注意事项**

1. 递归的核心在于正确计算每个子分形相对于父分形的偏移量，偏移量由子分形的边长 s 决定。
2. 时间复杂度：O(5^n)，每级递归产生 5 个子问题。
3. 空间复杂度：O(3^(n-1) × 3^(n-1))，即画布的大小。

**C++ 参考答案**

```cpp
#include <iostream>
#include <string>
#include <vector>
using namespace std;
vector<string> g;
void draw(int n, int x, int y) {
    if (n == 1) {
        g[x][y] = 'X';
        return;
    }
    int s = 1;
    for (int i = 1; i < n - 1; i++)
        s *= 3;
    draw(n - 1, x, y);
    draw(n - 1, x, y + 2 * s);
    draw(n - 1, x + s, y + s);
    draw(n - 1, x + 2 * s, y);
    draw(n - 1, x + 2 * s, y + 2 * s);
}
int main() {
    int n;
    cin >> n;
    int sz = 1;
    for (int i = 1; i < n; i++)
        sz *= 3;
    g.assign(sz, string(sz, ' '));
    draw(n, 0, 0);
    for (auto &s : g) {
        int r = s.size() - 1;
        while (r >= 0 && s[r] == ' ')
            r--;
        cout << s.substr(0, r + 1) << "\n";
    }
}
```

## 44. 19070 音响外放

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19070&access=8c756cfb7b03a0dd3064261332dcfbc9&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10 KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
贝壳找房2021届校招算法卷
***本题目难度略高于前面题目***

牛牛寝室有四人，他们打算用一个音响播放自己喜欢的曲子。

但是四人的喜好各不相同，他们每个人选取了自己最喜欢的n首曲子。

也就是一共有4n首曲子，第i首的长度为ai 。

但是他们不能容忍播放别人的曲子的时间比他们长很多，牛牛可以从这些曲子中删掉一些，使得每个人的播放总长大致相等。

牛牛想知道在每个人都至少都播放1首歌的情况下，播放最长时间和播放最短时间的差距最小是多少。
```

**输入**

```
第一行输入一个整数n，表示每个人都选择了n首曲子。

随后4行，每行n个整数，分别表示第每名室友喜欢的歌曲的时间长度。

1≤n≤10,100≤ai≤600
```

**输出**

```
输出一个整数，表示播放最长时间和播放最短时间的最小差距。
```

**样例输入**

```
3
240 300 360
600 200 200
300 400 500
600 600 600
```

**样例输出**

```
100

Hint

分别选用{1,3},{1},{3},{1}时，差距为100。
题目解析：看题目先看数据。n范围比较小，所以可以用DFS（递归实现指数型枚举）
得到每一个人所有的可能时间，总数最大不超过1024，用数组分别存储4个人的所有可能时间。
然后枚举............
如何枚举呢？我们可以先假设第1个人选择的曲子长度X一定是所有人里面最小时间（X最多1024种可能），
那么其他人一定比第1个人的值大，找到其他三个人比X大的最小值，求出差。
然后我们又假设第2个人选择的曲子长度Y一定是所有人里面最小的，参照第一个人处理方法，再来一次。
然后我们又假设第3个人选择的曲子长度Z一定是所有人里面最小的，再来一套处理。
然后我们又假设第4个人选择的曲子长度V一定是所有人里面最小的，再来一套处理。
答案是个极值，在上述枚举过程中必然可以找到。复杂度为O(2^n)。
```

**解析**

**题目要求**

4 名室友各有 n 首曲子（n <= 10），每人须从中选取至少 1 首播放。要求在四人的播放总时长中，最大值与最小值之差（极差）尽可能小，输出该最小极差。

**解题思路**

分两步求解：第一步，枚举每人所有可能的非空子集，计算各子集的总时长；第二步，在四组总时长中各选一个值，使这四个值的极差最小。第二步可借助排序和滑动窗口高效完成。

**算法分析**

1. **枚举子集总时长**：对每个人，利用位运算枚举所有 2^n - 1 个非空子集，分别计算每个子集的元素之和，存入对应的数组中。每人最多有 1023 个子集和。
2. **合并与排序**：将四组子集和合并为一个统一的列表，每项记录其数值和所属人员的编号，然后按数值升序排序。
3. **滑动窗口求最小极差**：使用双指针维护一个滑动窗口，保证窗口内包含来自全部 4 人的至少一个子集和。具体操作为：
   - 右指针不断右移以扩展窗口，直至窗口覆盖全部 4 人。
   - 随后左指针右移以收缩窗口，每次收缩前用窗口首尾元素之差更新答案的最小值。
   - 重复上述过程直至右指针遍历完毕。

**注意事项**

1. 每人至少选择 1 首曲子，因此子集枚举时须排除空集（掩码从 1 开始）。
2. 滑动窗口策略的正确性基于以下事实：排序后的列表中，任意四人的选择所构成的极差，一定不小于包含这四人的某个最短窗口的极差。
3. 时间复杂度：枚举阶段 O(n × 2^n)，排序阶段 O(4 × 2^n × n)，滑动窗口阶段 O(4 × 2^n)，总体为 O(n × 2^n)。
4. 空间复杂度：O(4 × 2^n)。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <utility>
#include <vector>
using namespace std;
int main() {
    int n;
    cin >> n;
    vector<vector<int>> sums(4);
    for (int p = 0; p < 4; p++) {
        vector<int> a(n);
        for (int &i : a)
            cin >> i;
        for (int m = 1; m < (1 << n); m++) {
            int s = 0;
            for (int i = 0; i < n; i++)
                if (m >> i & 1)
                    s += a[i];
            sums[p].push_back(s);
        }
    }
    vector<pair<int, int>> all;
    for (int i = 0; i < 4; i++)
        for (int x : sums[i])
            all.push_back({x, i});
    sort(all.begin(), all.end());
    int cnt[4] = {0}, have = 0, ans = 1e9, l = 0;
    for (int r = 0; r < (int)all.size(); r++) {
        if (cnt[all[r].second]++ == 0)
            have++;
        while (have == 4) {
            ans = min(ans, all[r].first - all[l].first);
            if (--cnt[all[l].second] == 0)
                have--;
            l++;
        }
    }
    cout << ans;
}
```

## 45. 19120 病毒扩散

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19120&access=bac0c4bfbcf4a0c12f97bab4966b31ea&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10 KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
SDUT 4783
2019-ncov的突然出现扰乱了人们的日常生活，它具有极强的传染性，可以快速的在人群中扩散，现在研究人员正在模拟其在人群中的扩散情况.

在一个n*m矩阵所示的人群中，*为普通人，#为佩戴口罩的人，@为病毒携带者，
已知每秒每位病毒携带者会将病毒传染给相邻八个方向的未戴口罩的普通人。
请问 x 秒后会有多少名传染者（初始为第0秒）？
```

**输入**

```
第一行输入空格分隔的三个数n，m，x代表n行，m列的空间，x秒（n,m<=1000)。

接下来n行每行m人如上述所示。
```

**输出**

```
一个数字，代表最终被传染的人数。
```

**样例输入**

```
4 4 2
****
*@**
**##
**#*
```

**样例输出**

```
12

Hint

多起点广搜
```

**解析**

**题目要求**

给定一个 n×m 的网格，其中 `*` 表示普通人，`#` 表示佩戴口罩者（不会被感染），`@` 表示初始病毒携带者。每秒内，每位携带者会将病毒传染给其八个方向（上、下、左、右及四个对角线方向）上相邻的未戴口罩的普通人。要求计算 x 秒后被感染的总人数。

**解题思路**

本题为多源 BFS（广度优先搜索）问题。所有初始感染者同时作为 BFS 的起点向外扩散，每扩展一层代表经过一秒。扩散至多进行 x 层，超出 x 层的格子不再访问。

**算法分析**

1. 遍历整个网格，将所有初始感染者 `@` 入队，并记录其时间戳为 0，同时累加初始感染人数。
2. 当队列非空时，取出队首元素 (r, c, t)：
   - 若 `t == x`，表示该感染者已无法继续扩散（已达最大时间），跳过。
   - 否则，检查其八个方向的相邻格子。若相邻格子为普通人 `*`，则将其标记为 `@`（已被感染），感染人数加 1，并以时间戳 `t+1` 入队。
3. BFS 结束后，累计的感染人数即为最终答案。

**注意事项**

1. 多源 BFS 的关键在于所有初始感染者同时入队，确保扩散过程的同步性。
2. 通过修改网格中 `*` 为 `@` 来标记已感染的格子，可避免重复入队。
3. 时间复杂度：O(n×m)，每个格子最多入队一次。
4. 空间复杂度：O(n×m)。

**C++ 参考答案**

```cpp
#include <iostream>
#include <queue>
#include <string>
#include <vector>
using namespace std;
struct Node {
    int r, c, t;
};
int main() {
    int n, m, x;
    cin >> n >> m >> x;
    vector<string> g(n);
    queue<Node> q;
    int ans = 0;
    for (int i = 0; i < n; i++) {
        cin >> g[i];
        for (int j = 0; j < m; j++)
            if (g[i][j] == '@') {
                q.push({i, j, 0});
                ans++;
            }
    }
    int d[8][2] = {{1, 0}, {-1, 0}, {0, 1}, {0, -1}, {1, 1}, {1, -1}, {-1, 1}, {-1, -1}};
    while (!q.empty()) {
        Node cur = q.front();
        q.pop();
        int r = cur.r, c = cur.c, t = cur.t;
        if (t == x)
            continue;
        for (auto &e : d) {
            int nr = r + e[0], nc = c + e[1];
            if (nr >= 0 && nr < n && nc >= 0 && nc < m && g[nr][nc] == '*') {
                g[nr][nc] = '@';
                ans++;
                q.push({nr, nc, t + 1});
            }
        }
    }
    cout << ans;
}
```
# 实验3

## 46. 8591 计算next值

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8591&access=0d3f5d586816699e4dfe3e4389fc947e&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
编写算法，录入多个字符串计算并验证NEXT值，输入0结束。本题目给出部分代码，请补全内容。]

#include "stdio.h"
#include "stdlib.h"
#include <iostream>
#define  MAXSTRLEN  255                   // 用户可在255以内定义最大串长
typedef unsigned char SString[MAXSTRLEN+1];	// 0号单元存放串的长度

void get_next(SString T,int next[]){
// 算法4.7
// 求模式串T的next函数值并存入数组next
   // 请补全代码

}
void main(){
int next[MAXSTRLEN];
SString S;
int n,i,j;
char ch;
scanf("%d",&n);    // 指定要验证NEXT值的字符串个数
ch=getchar();
for(i=1;i<=n;i++)
{
ch=getchar();
for(j=1;j<=MAXSTRLEN&&(ch!='\n');j++)    // 录入字符串
{
S[j]=ch;
ch=getchar();
}
S[0]=j-1;    // S[0]用于存储字符串中字符个数
get_next(S,next);
printf("NEXT J is:");
for(j=1;j<=S[0];j++)
printf("%d",next[j]);
printf("\n");
}
}
```

**输入**

```
第一行：输入n，表示有n个需计算NEXT值的字符串
第二至n+1行：每行输入一个字符串
```

**输出**

```
第1至第n行：通过计算每相应行的字符串得出的NEXT值
```

**样例输入**

```
4
abcdefg
aaaaab
abaabcac
aaabaaab
```

**样例输出**

```
NEXT J is:0111111
NEXT J is:012345
NEXT J is:01122312
NEXT J is:01231234
```

**解析**

**题目要求**

给定若干字符串，分别计算每个字符串的 KMP 算法中的 next 数组（即失配函数/部分匹配表）。next[j] 表示模式串中前 j 个字符组成的子串的最长相同真前后缀的长度。

**解题思路**

采用教材算法 4.7 的递推方式求解 next 数组：

1. **初始化**：令 `j = 1, k = 0`，其中 `j` 为当前正在计算 next 值的位置，`k` 为已知的最长相同真前后缀的长度。`next[1] = 0`（单个字符不存在真前后缀）。
2. **递推过程**：
   - 若 `k == 0` 或 `T[j] == T[k]`，说明当前字符可以与前缀的下一个字符匹配，因此 `next[++j] = ++k`。
   - 否则失配，令 `k = next[k]` 进行回溯，继续尝试更短的前缀。
3. 重复步骤 2，直到遍历完整个模式串。

**算法分析**

- 时间复杂度：O(m)，其中 m 为模式串长度。虽然存在 `k = next[k]` 的回溯，但 k 值在整个过程中递增次数不超过 m，故总时间复杂度为线性。
- 空间复杂度：O(m)，用于存储 next 数组。

**注意事项**

- next 数组的下标从 1 开始，与串的存储方式保持一致（0 号单元存放串长）。
- 递推时注意区分 `k == 0` 的特殊情况，此时表示不存在可匹配的前缀，应直接将 `next[j+1]` 置为 1。

**C++ 参考答案**

```cpp
#include <stdio.h>
#include <stdlib.h>
#define MAXSTRLEN 255                         // 用户可在255以内定义最大串长
typedef unsigned char SString[MAXSTRLEN + 1]; // 0号单元存放串的长度

void get_next(SString T, int next[]) {
    // 算法4.7
    // 求模式串T的next函数值并存入数组next
    int i = 1, j = 0;
    next[1] = 0;
    while (i < T[0]) {
        if (j == 0 || T[i] == T[j]) {
            ++i;
            ++j;
            next[i] = j;
        } else
            j = next[j];
    }
}

int main() {
    int next[MAXSTRLEN + 1];
    SString S;
    int n, i, j;
    int ch;
    scanf("%d", &n); // 指定要验证NEXT值的字符串个数
    getchar();
    for (i = 1; i <= n; i++) {
        ch = getchar();
        for (j = 1; j <= MAXSTRLEN && ch != '\n' && ch != EOF; j++) // 录入字符串
        {
            S[j] = (unsigned char)ch;
            ch = getchar();
        }
        S[0] = j - 1; // S[0]用于存储字符串中字符个数
        get_next(S, next);
        printf("NEXT J is:");
        for (j = 1; j <= S[0]; j++)
            printf("%d", next[j]);
        printf("\n");
    }
    return 0;
}
```

## 47. 8592 KMP算法

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8592&access=a4b332c59905590db5205fb12f009806&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
用KMP算法对主串和模式串进行模式匹配。本题目给出部分代码，请补全内容。

#include "stdio.h"
#include "stdlib.h"
#include <iostream>
#define TRUE  1
#define FALSE  0
#define OK  1
#define ERROR  0
#define INFEASLBLE  -1
#define OVERFLOW  -2
#define MAXSTRLEN  255 	//用户可在255以内定义最大串长
typedef unsigned char SString[MAXSTRLEN+1];	//0号单元存放串的长度

void get_next(SString T,int next[]){
// 算法4.7
// 求模式串T的next函数值并存入数组next
   // 请补全代码

}

int Index_KMP(SString S,SString T,int pos){
// 算法4.6
// 利用模式串T的next函数求T在主串S中第pos个字符之后的位置
// KMP算法。请补全代码

}
void main()
{
SString T,S;
 int i,j,n;
 char ch;
 int pos;
 scanf("%d",&n);    // 指定n对需进行模式匹配的字符串
ch=getchar();
for(j=1;j<=n;j++)
{
ch=getchar();
  for( i=1;i<=MAXSTRLEN&&(ch!='\n');i++)    // 录入主串
  {
S[i]=ch;
  ch=getchar();
}
S[0]=i-1;    // S[0]用于存储主串中字符个数
ch=getchar();
for( i=1;i<=MAXSTRLEN&&(ch!='\n');i++)    // 录入模式串
{
  T[i]=ch;
  ch=getchar();
}
T[0]=i-1;    // T[0]用于存储模式串中字符个数
pos=                 ;    // 请填空
printf("%d\n",pos);
}
    }
```

**输入**

```
第一行：输入n，表示有n对字符串需要匹配
第二行：输入第1个主串
第三行：输入第1个模式串
第四行：输入第2个主串
第五行：输入第2个模式串
……
倒数二行：输入第n个主串
最后一行：输入第n个模式串
```

**输出**

```
第一至第n行：输出每相应模式串的匹配值
```

**样例输入**

```
4
oadhifgoarhglkdsa
oar
abcdefg
dec
algeojflas
ojf
jfaweiof
of
```

**样例输出**

```
8
0
5
7
```

**解析**

**题目要求**

利用 KMP（Knuth-Morris-Pratt）算法实现模式匹配：给定主串 S 和模式串 T，在主串 S 中查找模式串 T 首次出现的位置。匹配成功时返回 1-based 起始位置，匹配失败返回 0。

**解题思路**

本题分为两个核心步骤：

1. **计算 next 数组**（算法 4.7）：对模式串 T 预处理，得到 next 数组，记录每个位置的最长相同真前后缀长度。
2. **KMP 匹配过程**（算法 4.6）：
   - 设主串指针 `i` 从 `pos` 开始，模式串指针 `j` 从 1 开始。
   - 若 `j == 0`（需从头匹配）或 `S[i] == T[j]`，则两个指针同步后移（`i++; j++`）。
   - 否则失配，令 `j = next[j]`，利用已匹配的前缀信息跳过不必要的比较，主串指针 `i` 不回溯。
   - 当 `j > T[0]` 时匹配成功，返回起始位置 `i - T[0]`；若遍历结束仍未匹配，返回 0。

**算法分析**

- 时间复杂度：预处理 O(m) + 匹配 O(n) = O(n + m)，其中 n 为主串长度，m 为模式串长度。
- 空间复杂度：O(m)，用于存储 next 数组。

**注意事项**

- 与朴素模式匹配相比，KMP 的核心优势在于主串指针不回溯，时间复杂度从最坏 O(n*m) 优化为 O(n+m)。
- 输出位置为 1-based；匹配失败时输出 0。
- 题目中 `pos` 填空处应调用 `Index_KMP(S, T, 1)`，即从主串第 1 个字符开始匹配。

**C++ 参考答案**

```cpp
#include <stdio.h>
#include <stdlib.h>
#define TRUE 1
#define FALSE 0
#define OK 1
#define ERROR 0
#define INFEASLBLE -1
#define OVERFLOW -2
#define MAXSTRLEN 255                         // 用户可在255以内定义最大串长
typedef unsigned char SString[MAXSTRLEN + 1]; // 0号单元存放串的长度

void get_next(SString T, int next[]) {
    // 算法4.7
    // 求模式串T的next函数值并存入数组next
    int i = 1, j = 0;
    next[1] = 0;
    while (i < T[0]) {
        if (j == 0 || T[i] == T[j]) {
            ++i;
            ++j;
            next[i] = j;
        } else
            j = next[j];
    }
}

int Index_KMP(SString S, SString T, int pos) {
    // 算法4.6
    // 利用模式串T的next函数求T在主串S中第pos个字符之后的位置
    // KMP算法。
    int i = pos, j = 1;
    int next[MAXSTRLEN + 1];
    get_next(T, next);
    while (i <= S[0] && j <= T[0]) {
        if (j == 0 || S[i] == T[j]) {
            ++i;
            ++j;
        } else
            j = next[j];
    }
    if (j > T[0])
        return i - T[0];
    return 0;
}

int main() {
    SString T, S;
    int i, j, n;
    int ch;
    int pos;
    scanf("%d", &n); // 指定n对需进行模式匹配的字符串
    getchar();
    for (j = 1; j <= n; j++) {
        ch = getchar();
        for (i = 1; i <= MAXSTRLEN && ch != '\n' && ch != EOF; i++) // 录入主串
        {
            S[i] = (unsigned char)ch;
            ch = getchar();
        }
        S[0] = i - 1; // S[0]用于存储主串中字符个数
        ch = getchar();
        for (i = 1; i <= MAXSTRLEN && ch != '\n' && ch != EOF; i++) // 录入模式串
        {
            T[i] = (unsigned char)ch;
            ch = getchar();
        }
        T[0] = i - 1; // T[0]用于存储模式串中字符个数
        pos = Index_KMP(S, T, 1);
        printf("%d\n", pos);
    }
    return 0;
}
```

## 48. 18722 稀疏矩阵的运算

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18722&access=33a898ee9c08e4dd03e54b8cd53491f4&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
稀疏矩阵的压缩存储原则：只存矩阵的行列数和每个非零元的行列下标及其值。
例如下图的矩阵M是由行列数（6,7）和三元组表{(1,2,12), (1,3,9), (3,1,-3),(3,6,14),(4,3,24),(5,2,18), (6,1,15), (6,4,-7) }唯一确定。
问题描述：已知一个稀疏矩阵的三元组表，使用快速转置算法求其转置矩阵的三元组表，三元组表要按行优先的方式存储。
```

**输入**

```
第一行三个整数n,m,k。n,m代表矩阵A的行列数（0<=n,m<=1000000）,k为三元组表中元素的个数。
此后为k行，每行3个整数a，b，c，分别代表元素的行号，列号和值。数据确保按行优先给出。（0<=k<=10000）
```

**输出**

```
输出为k行，即转置矩阵的三元组表，三元组表要按行优先显示。
```

**样例输入**

```
6 7 8
1 2 12
1 3 9
3 1 -3
3 6 14
4 3 24
5 2 18
6 1 15
6 4 -7
```

**样例输出**

```
1 3 -3
1 6 15
2 1 12
2 5 18
3 1 9
3 4 24
4 6 -7
6 3 14
```

**解析**

**题目要求**

给定一个稀疏矩阵的三元组表示（按行优先存储），使用快速转置算法求其转置矩阵的三元组表示，结果同样按行优先排列。

**解题思路**

快速转置算法的核心思想是：通过预处理确定转置后每行的起始存储位置，从而在一次扫描中原三元组表时即可将每个元素直接放入目标位置。具体步骤如下：

1. **统计原矩阵每列的非零元个数**：记 `cnt[c]` 为原矩阵第 c 列的非零元个数。由于转置后原矩阵的列变为行，`cnt[c]` 即为转置矩阵第 c 行的元素个数。
2. **计算前缀和得到每行起始位置**：记 `pos[i]` 为转置矩阵第 i 行在三元组表中的起始下标。`pos[1] = 0`，`pos[i] = pos[i-1] + cnt[i-1]`。
3. **稳定放置元素**：按原三元组表的顺序依次扫描每个元素 `(r, c, v)`，将其转置为 `(c, r, v)` 后放入 `pos[c]` 位置，并令 `pos[c]++`。由于原表按行优先排列，同一列的元素天然按列号递增，因此转置后同行的元素自然按列号递增，满足行优先要求。

**算法分析**

- 时间复杂度：O(m + k)，其中 m 为原矩阵列数，k 为非零元个数。相比普通转置的 O(m * k)，快速转置显著提升了效率。
- 空间复杂度：O(m + k)，用于存储转置后的三元组表和辅助数组。

**注意事项**

- 矩阵的行列数可达 10^6，但非零元个数不超过 10000，因此应使用三元组压缩存储而非二维数组。
- 题目保证输入按行优先给出，快速转置的稳定性保证了输出自然按行优先（同行内按列递增）排列。

**C++ 参考答案**

```cpp
#include <iostream>
#include <vector>
using namespace std;

struct T {
    int r, c, v; // 行号、列号、值
};

int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);

    int n, m, k;
    cin >> n >> m >> k;

    vector<T> a(k), b(k);
    vector<int> cnt(m + 2, 0); // cnt[i] 统计原矩阵第 i 列的非零元个数
    vector<int> pos(m + 2, 0); // pos[i] 记录转置矩阵第 i 行的起始存储位置

    for (auto &x : a) {
        cin >> x.r >> x.c >> x.v;
        cnt[x.c]++; // 统计原矩阵每列的非零元个数
    }

    // 计算转置后每行（对应原矩阵每列）的起始位置（前缀和）
    pos[1] = 0;
    for (int i = 2; i <= m; i++)
        pos[i] = pos[i - 1] + cnt[i - 1];

    // 按原顺序稳定放置：原矩阵第 c 列元素放入转置矩阵第 c 行
    for (auto x : a) {
        int p = pos[x.c]++;
        b[p] = {x.c, x.r, x.v}; // 行列互换完成转置
    }

    // 输出转置后的三元组表
    for (auto x : b)
        cout << x.r << ' ' << x.c << ' ' << x.v << "\n";
}
```

## 49. 18769 不完整的排序

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18769&access=be09570c657865301ec471bc304c35d6&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
一个数组只包含正负整数，请使用一个O（n）级别的算法对其进行排序。
只需将负数全部放前面，正数全部放后面即可，无需进行严格排序。
此题目必须使用双指针法才能通过，
双指针，指的是在遍历对象的过程中，不是普通的使用单个指针进行访问，
而是使用两个相反方向（对撞指针）的指针进行扫描，从而达到相应的目的。
具体算法如下：
定义两个指针：i=1，j=n
（1）i指针从左至右遍历，当碰到不满足条件的元素（正数），我们暂停i 移动
（2）j指针从右至左遍历，当碰到不满足条件的元素（负数），我们暂停 j 移动
（3）交换两个指针i和j指向的元素
（4）重复 1，2，3 步骤，直到i和j相遇

题目包含T组数据。
```

**输入**

```
第一行一个整数T,表示数据的组数。（1<=T<=10）
下面共2*T行，每两行为一组数据。
第i组数组的第一行为整数n，（1<=n<=100000）表示数组的大小，第二行为n个整数。
```

**输出**

```
共T行，排序后的T组数据。
```

**样例输入**

```
2
3
1 -1 2
4
-1 2 3 -4
```

**样例输出**

```
-1 1 2
-1 -4 3 2
```

**解析**

**题目要求**

给定一个仅包含正负整数的数组，使用对撞双指针法将所有负数移至数组前部、所有正数移至数组后部。不要求对元素进行严格排序，只需完成正负分区。

**解题思路**

本题是经典的双指针分区问题（荷兰国旗问题的简化版本），算法步骤如下：

1. **初始化指针**：左指针 `i` 指向数组起始位置，右指针 `j` 指向数组末尾位置。
2. **左指针扫描**：`i` 从左向右移动，跳过所有负数（满足条件的元素），遇到非负数时暂停。
3. **右指针扫描**：`j` 从右向左移动，跳过所有正数（满足条件的元素），遇到非正数时暂停。
4. **交换与推进**：若此时 `i < j`，则交换 `a[i]` 与 `a[j]`，使错位的元素各归其侧；继续重复上述步骤，直到两个指针相遇。

**算法分析**

- 时间复杂度：O(n)。每个元素最多被访问一次，两个指针合计扫描整个数组。
- 空间复杂度：O(1)。仅使用常数级额外空间，属于原地操作。

**注意事项**

- 内层循环必须加上 `i < j` 的保护条件，防止指针越界交叉后继续访问导致数组越界。
- 该算法不保证分区后负数（或正数）之间的相对顺序不变，即排序结果不具有稳定性。
- 题目保证数组仅包含正负整数（不含零），因此判断条件使用 `a[i] < 0` 和 `a[j] > 0` 即可。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;

int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);

    int T;
    cin >> T;
    while (T--) {
        int n;
        cin >> n;
        vector<int> a(n);
        for (int &i : a)
            cin >> i;

        int i = 0, j = n - 1;
        while (i < j) {
            while (i < j && a[i] < 0)
                i++; // 左指针跳过负数
            while (i < j && a[j] > 0)
                j--; // 右指针跳过正数
            if (i < j)
                swap(a[i], a[j]); // 交换错位的正负数
        }

        for (int k = 0; k < n; k++)
            cout << a[k] << (k + 1 == n ? '\n' : ' ');
    }
}
```

# 拓展习题3

## 50. 18939 最长单词

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18939&access=ef3aa4e2a6fcd234537d63da793eccc6&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
一个以'.'结尾的简单英文句子，单词之间用空格分隔，没有缩写形式和其它特殊形式。
```

**输入**

```
一个以'.'结尾的简单英文句子（长度不超过500），单词之间用空格分隔，没有缩写形式和其它特殊形式。
```

**输出**

```
该句子中最长的单词。如果多于一个，则输出第一个。
```

**样例输入**

```
I am a student of Peking University.
```

**样例输出**

```
University

Hint

注意字符"."不属于单词。
```

**解析**

**题目要求**

给定一个以句号 `.` 结尾的英文句子，找出其中最长的单词。若存在多个长度相同的最长单词，输出最先出现的那个。

**解题思路**

逐字符扫描整个句子，将连续的字母字符视为一个单词：

1. 若当前字符是字母，将其追加到当前单词 `cur` 中。
2. 若当前字符不是字母（空格或句号），说明当前单词结束。将 `cur` 与已知最长单词 `best` 进行比较：若 `cur` 更长，则更新 `best`；长度相等时保留先出现的（即不更新）。然后清空 `cur`，准备收集下一个单词。
3. 句末的句号 `.` 同样作为单词分隔符处理，因此循环结束时最后一个单词也会被正确比较。

**算法分析**

- 时间复杂度：O(n)，其中 n 为句子长度。每个字符仅被访问一次。
- 空间复杂度：O(n)，用于存储当前单词和最长单词。

**注意事项**

- 句末的句号 `.` 不属于任何单词，需要在比较时正确处理，避免将句号计入单词长度。
- 使用 `isalpha()` 判断字符是否为字母时，建议将参数转换为 `unsigned char` 以避免负值字符引起的未定义行为。

**C++ 参考答案**

```cpp
#include <ctype.h>
#include <iostream>
#include <string>
using namespace std;

int main() {
    string line;
    getline(cin, line);

    string cur;  // 当前正在收集的单词
    string best; // 已知最长的单词

    for (char c : line) {
        if (isalpha((unsigned char)c)) {
            cur += c; // 字母字符追加到当前单词
        } else {
            // 遇到非字母字符（空格或句号），当前单词结束
            if (cur.size() > best.size())
                best = cur; // 严格大于时才更新，保证长度相同时保留第一个
            cur.clear();    // 清空，准备收集下一个单词
        }
    }

    cout << best;
}
```

## 51. 18942 偏爱字母

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18942&access=41ed25877e8103b671b388894f584b16&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
美团2021校招笔试-编程题(通用编程试题,第8场)

小美喜欢字母E，讨厌字母F。在小美生日时，小团送了小美一个仅包含字母E和F的字符串，
小美想从中选出一个包含字母E数量与字母F数量之差最大的子串。

*子串：从字符串前面连续删去若干个字符，从后面连续删去若干个字符剩下的字符串（也可以一个都不删），
例如abcab是fabcab的子串，而不是abcad的子串。

我们将空串看作所有字符串的子串。
```

**输入**

```
第一行一个正整数n表示字符串的长度。

第二行长度为n，且仅包含大写字母'E','F'的字符串（不含引号）
```

**输出**

```
输出一个整数，表示最大的差值
```

**样例输入**

```
5
EFEEF
```

**样例输出**

```
2

Hint

解题建议：转化数据形式，把E看成1，把F看成-1。算法复杂度为O(n)。
```

**解析**

**题目要求**

给定一个仅由字母 E 和 F 组成的字符串，求其所有连续子串中，字母 E 的数量与字母 F 的数量之差的最大值。空串也被视为合法子串（差值为 0）。

**解题思路**

本题可通过数据转化归约为经典的**最大子段和**问题：

1. **数据转化**：将字符 E 映射为 +1，字符 F 映射为 -1。原问题"子串中 E 的数量减去 F 的数量"即等价于"转化后数组的连续子段之和"。
2. **求解最大子段和**：使用 Kadane 算法在线性时间内求解。维护两个变量：
   - `cur`：以当前元素结尾的最大子段和。若 `cur` 变为负数，说明前面的子段对后续只有负贡献，因此重置为 0（相当于从下一个位置重新开始）。
   - `best`：全局最大子段和，每次用 `cur` 更新。
3. **空串处理**：由于空串差值为 0，且 `best` 初始化为 0，因此当所有子串的差值均为负时，算法正确返回 0。

**算法分析**

- 时间复杂度：O(n)，仅需一次线性扫描。
- 空间复杂度：O(1)，仅使用常数级额外变量。

**注意事项**

- Kadane 算法中 `cur = max(0, cur + v)` 的写法天然处理了"允许空串"的要求——当累计和为负时重置为 0。
- 若题目要求子串非空，则需将 `best` 初始化为负无穷，并去掉 `max(0, ...)` 的重置逻辑。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <string>
using namespace std;

int main() {
    int n;
    string s;
    cin >> n >> s;

    int cur = 0;  // 以当前位置结尾的最大子段和
    int best = 0; // 全局最大子段和（初始为 0，对应空串）

    for (char c : s) {
        int v = (c == 'E' ? 1 : -1); // E 映射为 +1，F 映射为 -1
        cur = max(0, cur + v);       // 若累计和为负则重置（允许空串）
        best = max(best, cur);       // 更新全局最大值
    }

    cout << best;
}
```

## 52. 18940 最小循环节（KMP算法）

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18940&access=6c5b9351cbe11a8de26e1648529462b3&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
给定一个字符串，请计算这个字符串最多是由多少个相同的子字符串重复连接而成的。
如：acacac 最多有 3 个 ac 连接而成，bbbb最多由4个b连接而成，abc最多由1个abc连接而成。

此问题需求出整个字符串的最大相同真前后缀，需使用kmp算法或字符串哈希法，具体解释可看下图或百度最小循环节。
```

**输入**

```
一个字符串，长度不超过100000。
```

**输出**

```
组成字符串的最多重复连接子串的个数。
```

**样例输入**

```
ababab
```

**样例输出**

```
3
```

**解析**

**题目要求**

给定一个字符串，求其最多由多少个相同的子串重复连接而成。例如 `acacac` 由 3 个 `ac` 连接而成，答案为 3。

**解题思路**

本题利用 KMP 算法中前缀函数（pi 数组）的性质来求解最小循环节：

1. **计算前缀函数**：`pi[i]` 表示子串 `s[0..i]` 的最长相同真前后缀的长度。对完整字符串计算 pi 数组后，`pi[n-1]` 即为整个字符串的最长相同真前后缀长度。
2. **求最小循环节长度**：设字符串长度为 n，最小循环节长度为 `p = n - pi[n-1]`。
   - **原理**：最长相同真前后缀意味着前 `n - pi[n-1]` 个字符与后 `n - pi[n-1]` 个字符完全相同，因此这 `p` 个字符构成一个循环节。
3. **判断整除性**：
   - 若 `n % p == 0`，则字符串完全由长度为 p 的循环节重复 `n/p` 次组成，输出 `n/p`。
   - 若 `n % p != 0`，则字符串不能被任何更短的子串完整重复构成，输出 1。

**算法分析**

- 时间复杂度：O(n)，计算前缀函数仅需一次线性扫描。
- 空间复杂度：O(n)，用于存储 pi 数组。

**注意事项**

- 务必验证整除条件。例如字符串 `aba`，`pi[2] = 1`，`p = 3 - 1 = 2`，但 `3 % 2 != 0`，因此答案为 1 而非 1.5。
- 前缀函数的计算中，回溯使用 `j = pi[j-1]` 而非简单的 `j--`，这是保证线性时间复杂度的关键。

**C++ 参考答案**

```cpp
#include <iostream>
#include <string>
#include <vector>
using namespace std;

int main() {
    string s;
    cin >> s;
    int n = s.size();

    // 计算 KMP 前缀函数（pi 数组）
    vector<int> pi(n, 0);
    for (int i = 1; i < n; i++) {
        int j = pi[i - 1];
        while (j > 0 && s[i] != s[j])
            j = pi[j - 1]; // 失配时回溯到更短的前缀
        if (s[i] == s[j])
            j++; // 匹配成功，前缀长度加 1
        pi[i] = j;
    }

    // 最小循环节长度 = 串长 - 最长相同真前后缀长度
    int p = n - pi[n - 1];
    // 判断串长能否被循环节长度整除
    cout << (n % p == 0 ? n / p : 1);
}
```

## 53. 18941 压缩算法

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18941&access=2f3b96074136afce83c2b626ce50d681&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
腾讯2020校园招聘-后台 第一题
小Q想要给他的朋友发送一个神秘字符串，但是他发现字符串的过于长了，
于是小Q发明了一种压缩算法对字符串中重复的部分进行了压缩，
对于字符串中连续的m个相同字符串S将会压缩为[m|S](m为一个整数且1<=m<=100)，例如字符串ABCABCABC将会被压缩为[3|ABC]，
现在小Q的同学收到了小Q发送过来的字符串，你能帮助他进行解压缩么？

解题建议：
（1）由于涉及到字符串的重复，尽量不要再使用C语言的字符数组，用C++的string类型会更容易实现。
（2）多层嵌套的情况，必须先求出内层再求出外层，显而易见可用递归算法或栈解决，建议递归。
（3）当确定s[i]是一个数字字符时，可以用如下C++代码获取字符串中的整数
    int sum=0;
    while(isdigit(s[i]))
        sum=sum*10+s[i++]-'0';
```

**输入**

```
输入第一行包含一个字符串S，代表压缩后的字符串。
S的长度<=1000;
S仅包含大写字母、[、]、|;
解压后的字符串长度不超过100000;
压缩递归层数不超过10层;
```

**输出**

```
输出一个字符串，代表解压后的字符串。
```

**样例输入**

```
HG[3|B[2|CA]]F
```

**样例输出**

```
HGBCACABCACABCACAF
```

**解析**

**题目要求**

实现一个字符串解压缩算法。压缩格式为 `[m|S]`，表示将字符串 S 重复 m 次。压缩支持多层嵌套，例如 `[3|B[2|CA]]` 表示先解压内层 `[2|CA]` 得到 `CACA`，再拼接为 `BCACA`，最后重复 3 次。

**解题思路**

由于压缩存在多层嵌套，必须从内向外逐层解压，天然适合使用**递归**方法：

1. **逐字符扫描**压缩字符串，根据字符类型进行分类处理：
   - **大写字母**：直接追加到当前层的结果字符串中。
   - **左方括号 `[`**：标志着一个嵌套压缩段的开始。依次完成以下操作：
     - 跳过 `[`，读取重复次数 m（可能为多位整数）。
     - 跳过分隔符 `|`。
     - **递归调用**解析函数处理内部内容（直到遇到对应的 `]`）。
     - 跳过右方括号 `]`。
     - 将递归解压得到的内部字符串重复 m 次，追加到当前层的结果中。
   - **右方括号 `]`**：当前层解析结束，返回结果。
2. 使用全局位置指针 `pos` 跟踪当前扫描位置，确保递归调用后外层能继续从正确位置解析。

**算法分析**

- 时间复杂度：O(L)，其中 L 为解压后字符串的总长度。每个字符在构造时被访问一次。
- 空间复杂度：O(L + D)，其中 D 为最大嵌套深度，L 为解压后字符串长度。递归栈深度不超过 D。

**注意事项**

- 递归的终止条件为遇到 `]` 或扫描到字符串末尾。
- 全局指针 `pos` 在递归返回后自动指向 `]` 之后的位置，因此外层调用者无需额外处理指针偏移。
- 解压后的字符串长度可达 100000，建议使用 C++ `string` 类型而非 C 风格字符数组。

**C++ 参考答案**

```cpp
#include <ctype.h>
#include <iostream>
#include <string>
using namespace std;

string s;
int pos = 0; // 全局位置指针，跟踪当前扫描位置

// 递归解析压缩字符串，返回解压后的结果
string parse() {
    string res;
    while (pos < (int)s.size() && s[pos] != ']') {
        if (isupper((unsigned char)s[pos])) {
            // 大写字母直接追加到结果中
            res += s[pos++];
        } else if (s[pos] == '[') {
            // 遇到嵌套压缩段 [m|S]
            pos++; // 跳过 '['
            int num = 0;
            while (isdigit((unsigned char)s[pos]))
                num = num * 10 + s[pos++] - '0'; // 读取重复次数 m
            pos++;                               // 跳过分隔符 '|'
            string inner = parse();              // 递归解析内部内容
            pos++;                               // 跳过 ']'
            while (num--)
                res += inner; // 将解压后的内容重复 m 次
        }
    }
    return res;
}

int main() {
    cin >> s;
    cout << parse();
}
```

## 54. 18943 小易爱回文

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18943&access=e67f863ef0cf8226208e1bde66ba9e52&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
网易2021校招笔试-音频算法工程师（提前批）

小易得到了一个仅包含大小写英文字符的字符串，该字符串可能不是回文串。

（"回文串"是一个正读和反读都一样的字符串，比如"level"或者"noon"等等就是回文串，"asds"就不是回文串。）

小易可以在字符串尾部加入任意数量的任意字符，使其字符串变成回文串。

现在请你编写一个程序，程序要能计算出小易可以得到的最短回文串。
```

**输入**

```
一行包括一个字符串S。S的长度小于1000。
```

**输出**

```
一行包括一个字符串，代表答案。
```

**样例输入**

```
noo
```

**样例输出**

```
noon

Hint

注意回文串的长度可以是奇数，也可以是偶数。
拓展思考：如果长度达到100000，这个题目又该怎么处理呢？
```

**解析**

**题目要求**

给定一个字符串，仅允许在其**尾部**添加任意字符，使其成为回文串。要求构造出最短的回文串并输出。

**解题思路**

关键在于找到原串中从某一位置开始到末尾的最长回文后缀：

1. **寻找最长回文后缀**：从左到右依次枚举起始位置 `i`（`i = 0, 1, ..., n-1`），检查子串 `s[i..n-1]` 是否为回文串。第一个找到的回文后缀即为最长的回文后缀。
2. **构造最短回文串**：
   - 回文后缀部分 `s[i..n-1]` 本身已经构成回文，无需额外添加字符。
   - 回文后缀之前的部分 `s[0..i-1]` 需要将其**逆序**追加到字符串末尾，与自身形成对称。
   - 最终结果为：`s[0..n-1]` + `reverse(s[0..i-1])`。

**正确性说明**

为了使最终回文串最短，需要使追加的字符数最少，即要求回文后缀尽可能长。从 `i = 0` 开始枚举保证了找到的第一个回文后缀就是最长的。

**算法分析**

- 时间复杂度：O(n^2)，最坏情况下需检查 O(n) 个起始位置，每次回文判断耗时 O(n)。对于题目给定的 n < 1000 完全足够。
- 空间复杂度：O(n)，用于存储结果字符串。

**注意事项**

- 题目限制只能在**尾部**添加字符，不能在头部添加。这与"最短回文串"的另一个经典变体（允许在头部添加）不同。
- 当原串本身就是回文串时（`i = 0` 即满足），无需添加任何字符，直接输出原串即可。
- 拓展：若字符串长度达到 10^5，可使用 KMP 算法在 O(n) 时间内求解——将原串反转后拼接到原串前面，用分隔符连接，再通过前缀函数求最长回文前缀。

**C++ 参考答案**

```cpp
#include <iostream>
#include <string>
using namespace std;

// 判断 s[l..n-1] 是否为回文串
bool pal(const string &s, int l) {
    int r = s.size() - 1;
    while (l < r)
        if (s[l++] != s[r--])
            return false;
    return true;
}

int main() {
    string s;
    cin >> s;
    int n = s.size();

    // 从左到右枚举，找到最长的回文后缀 s[i..n-1]
    for (int i = 0; i < n; i++) {
        if (pal(s, i)) {
            // 输出原串
            cout << s;
            // 将回文后缀之前的部分 s[0..i-1] 逆序追加到末尾
            for (int j = i - 1; j >= 0; j--)
                cout << s[j];
            return 0;
        }
    }
}
```

## 55. 18964 蛇形方阵

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18964&access=8885c57c84b4e7525353a6bdcb6681fd&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
给出一个不大于 9 的正整数 n，输出 n×n 的蛇形方阵。

从左上角填上 1 开始，顺时针方向依次填入数字。

如同样例所示。注意每个数字有都会占用 3 个字符，前面使用空格补齐。
```

**输入**

```
一个整数n。
```

**输出**

```
n对应的蛇形方阵。
```

**样例输入**

```
4
```

**样例输出**

```
1  2  3  4
 12 13 14  5
 11 16 15  6
 10  9  8  7

Hint

注意输出格式！
```

**解析**

**题目要求**

构造一个 n*n 的螺旋（蛇形）方阵，从左上角开始填入数字 1，按顺时针方向（右、下、左、上）依次递增填入，最后按指定格式输出。

**解题思路**

采用**逐层填充**的模拟策略，维护当前未填充区域的四个边界：上边界 `top`、下边界 `bot`、左边界 `l`、右边界 `r`。

每一轮按以下四个方向依次填充：

1. **向右**：沿上边界 `top` 行，从列 `l` 到列 `r`，依次填入数字，填充完毕后上边界下移（`top++`）。
2. **向下**：沿右边界 `r` 列，从行 `top` 到行 `bot`，依次填入数字，填充完毕后右边界左移（`r--`）。
3. **向左**：沿下边界 `bot` 行，从列 `r` 到列 `l`，依次填入数字，填充完毕后下边界上移（`bot--`）。
4. **向上**：沿左边界 `l` 列，从行 `bot` 到行 `top`，依次填入数字，填充完毕后左边界右移（`l++`）。

重复以上四步，直到上下边界或左右边界交叉（`top > bot` 或 `l > r`）为止。

**输出格式**

除第一行第一个数字外，每个数字占 3 个字符宽度，右对齐；这样既能保持列对齐，也能匹配样例首行不带行首空格的格式。

**算法分析**

- 时间复杂度：O(n^2)，共填充 n^2 个元素，每个元素恰好被访问一次。
- 空间复杂度：O(n^2)，用于存储 n*n 的二维矩阵。

**注意事项**

- 当 n 为奇数时，最后一次循环可能只执行"向右"一步（填充中心元素），因此在"向左"和"向上"步骤前需要检查边界条件 `top <= bot` 和 `l <= r`，避免重复填充。
- 输出时注意使用宽度为 3 的格式化输出，确保数字对齐。

**C++ 参考答案**

```cpp
#include <cstdio>
#include <iostream>
#include <vector>
using namespace std;

int main() {
    int n;
    cin >> n;

    vector<vector<int>> a(n, vector<int>(n));
    int top = 0, bot = n - 1, l = 0, r = n - 1;
    int x = 1; // 当前要填入的数字

    while (top <= bot && l <= r) {
        // 向右填充上边界行
        for (int j = l; j <= r; j++)
            a[top][j] = x++;
        top++;

        // 向下填充右边界列
        for (int i = top; i <= bot; i++)
            a[i][r] = x++;
        r--;

        // 向左填充下边界行（需检查边界）
        if (top <= bot) {
            for (int j = r; j >= l; j--)
                a[bot][j] = x++;
            bot--;
        }

        // 向上填充左边界列（需检查边界）
        if (l <= r) {
            for (int i = bot; i >= top; i--)
                a[i][l] = x++;
            l++;
        }
    }

    // 按样例格式输出：首行首个数字不额外补空格，其余数字占 3 位宽度
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if (i == 0 && j == 0)
                printf("%d", a[i][j]);
            else
                printf("%3d", a[i][j]);
        }
        printf("\n");
    }
}
```

## 56. 19072 数字字符串转化成IP地址

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19072&access=bbf9e1ab9aef7d5b1ac522e3da76ef8a&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
百度面试题

现在有一个只包含数字的字符串，将该字符串转化成IP地址的形式，返回所有可能的情况。
例如：
给出的字符串为"25525522135",
返回["255.255.22.135", "255.255.221.35"].

要求：空间复杂度 O(n),时间复杂度 O(n!)。

注意：ip地址是由四段数字组成的数字序列，格式如 "x.x.x.x"，其中 x 的范围应当是 [0,255]。
有情提示：类似这样的数字00010，只能划分为0.0.0.10,不能划分为00.0.1.0,四个数字不能包含前导0.
```

**输入**

```
一个数字字符串。长度小于12.
```

**输出**

```
所有可能的IP地址。
```

**样例输入**

```
112211
```

**样例输出**

```
1.1.2.211
1.1.22.11
1.1.221.1
1.12.2.11
1.12.21.1
1.122.1.1
11.2.2.11
11.2.21.1
11.22.1.1
112.2.1.1

Hint

题目要求复杂度是n!,暗示了应该使用DFS。
但由于IP地址的特殊性，也可以暴力枚举三个点的位置来解决，效率更佳。用三层循环枚举位置，再进行分段转换成数字。
例如
for(i=0;i<=2;i++)
        {
            for(j=i+1;j<=min(n-2,i+3);j++)
            {
                for(k=j+1;k<=min(n-1,j+3);k++)
                { /**< 四个数字分别是0到i,i+1到j,j+1到k，k+1到n，后面就转换成整数进行检查 */
```

**解析**

**题目要求**

给定一个纯数字字符串，在字符串中插入三个点号将其划分为四段，使得每段构成一个合法的 IP 地址段（0~255 的整数，且不允许前导零，除非该段恰好为 `"0"`）。输出所有合法的 IP 地址。

**解题思路**

由于 IP 地址恰好由四段组成，每段长度为 1~3 位数字，可以使用**三层循环枚举三个分割点**的位置：

1. 设字符串长度为 n，三个分割点将字符串分为四段：
   - 第 1 段：`s[0..i-1]`（长度 i，取值范围 1~3）
   - 第 2 段：`s[i..j-1]`（长度 j-i，取值范围 1~3）
   - 第 3 段：`s[j..k-1]`（长度 k-j，取值范围 1~3）
   - 第 4 段：`s[k..n-1]`（长度 n-k，取值范围 1~3）
2. 对每一段进行合法性检查：
   - **前导零检查**：若段长度大于 1 且首字符为 `'0'`，则不合法（例如 `"01"` 不合法）。
   - **数值范围检查**：将段转换为整数后，值不得超过 255。
3. 四段均合法时，按 `a.b.c.d` 格式输出该 IP 地址。

**算法分析**

- 时间复杂度：由于每段长度不超过 3，三层循环的枚举次数为常数级别（最多 3^3 = 27 次），每次检查耗时 O(1)，因此总时间复杂度为 O(1)。
- 空间复杂度：O(n)，用于存储输入字符串和临时子串。

**注意事项**

- 前导零的判断至关重要：`"0"` 是合法的，但 `"00"` 和 `"01"` 均不合法。
- 第四段的长度也需要检查不超过 3，即 `n - k <= 3`，否则该划分无效。
- 由于字符串长度不超过 12，且每段长度限制为 1~3，暴力枚举的效率极高。

**C++ 参考答案**

```cpp
#include <iostream>
#include <string>
using namespace std;

// 检查子串是否构成合法的 IP 地址段
bool ok(const string &t) {
    // 不允许前导零（长度大于 1 且首字符为 '0' 则非法）
    if (t.size() > 1 && t[0] == '0')
        return false;
    // 数值不得超过 255
    int v = stoi(t);
    return v <= 255;
}

int main() {
    string s;
    cin >> s;
    int n = s.size();

    // 枚举三个分割点的位置 i, j, k
    for (int i = 1; i <= 3; i++)                   // 第 1 段结束位置
        for (int j = i + 1; j <= i + 3; j++)       // 第 2 段结束位置
            for (int k = j + 1; k <= j + 3; k++) { // 第 3 段结束位置
                // 第 4 段不能为空且长度不超过 3
                if (k >= n || n - k > 3)
                    continue;
                // 提取四个子串
                string a = s.substr(0, i);     // 第 1 段
                string b = s.substr(i, j - i); // 第 2 段
                string c = s.substr(j, k - j); // 第 3 段
                string d = s.substr(k);        // 第 4 段
                // 四段均合法则输出
                if (ok(a) && ok(b) && ok(c) && ok(d))
                    cout << a << '.' << b << '.' << c << '.' << d << "\n";
            }
}
```
# 实验4

## 57. 8606 二叉树的构建及遍历操作

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8606&access=de8f1b62c44fd8e66aca58e3f8ed1ed4&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
构造二叉链表表示的二叉树：按先序次序输入二叉树中结点的值（一个字符），'#'字符表示空树，构造二叉链表表示的二叉树T；再输出三种遍历序列。本题只给出部分代码,请补全内容。

#include "stdio.h"
#include "malloc.h"
#define TRUE 1
#define FALSE 0
#define OK  1
#define ERROR  0
#define INFEASIBLE -1
#define OVERFLOW -2
typedef int  Status;

typedef char  ElemType;
typedef struct BiTNode{
  ElemType data;
  struct BiTNode *lchild,*rchild;//左右孩子指针
} BiTNode,*BiTree;

Status CreateBiTree(BiTree &T) {  // 算法6.4
  // 按先序次序输入二叉树中结点的值（一个字符），'#'字符表示空树，
  // 构造二叉链表表示的二叉树T。
  char ch;
  scanf("%c",&ch);
  if (ch=='#') T = NULL;
  else {
    if (!(T = (BiTNode *)malloc(sizeof(BiTNode)))) return ERROR;
    ________________________ // 生成根结点
     _______________________   // 构造左子树
    _________________________  // 构造右子树
  }
  return OK;
} // CreateBiTree

Status PreOrderTraverse( BiTree T) {
   // 前序遍历二叉树T的递归算法
   //补全代码,可用多个语句

} // PreOrderTraverse

Status InOrderTraverse( BiTree T) {
     // 中序遍历二叉树T的递归算法
    //补全代码,可用多个语句

} // InOrderTraverse

Status PostOrderTraverse( BiTree T) {
     // 后序遍历二叉树T的递归算法
     //补全代码,可用多个语句

} // PostOrderTraverse

int main()   //主函数
{
                      //补充代码
 }//main
```

**输入**

```
第一行：输入一棵二叉树的先序遍历序列
```

**输出**

```
第一行：二叉树的先序遍历序列
第二行：二叉树的中序遍历序列
第三行：二叉树的后序遍历序列
```

**样例输入**

```
AB##C##
```

**样例输出**

```
ABC
BAC
BCA
```

**解析**

**题目要求**

根据先序遍历序列构建二叉链表表示的二叉树（以 `#` 表示空结点），并分别输出该二叉树的先序、中序和后序遍历序列。

**解题思路**

1. **建树**：按照先序遍历的顺序依次读入字符。若读入字符为 `#`，则当前子树为空；否则为当前结点分配存储空间，将字符存入根结点，然后递归构建左子树和右子树。
2. **三种遍历**：均采用递归方式实现——
   - 先序遍历：访问根结点 → 遍历左子树 → 遍历右子树。
   - 中序遍历：遍历左子树 → 访问根结点 → 遍历右子树。
   - 后序遍历：遍历左子树 → 遍历右子树 → 访问根结点。

**算法分析**

- 时间复杂度：建树 O(N)，每种遍历 O(N)，总体 O(N)，其中 N 为输入序列长度。
- 空间复杂度：O(H)，H 为二叉树高度，即递归栈的最大深度。

**C++ 参考答案**

```cpp
#include <malloc.h>
#include <stdio.h>
#define TRUE 1
#define FALSE 0
#define OK 1
#define ERROR 0
#define INFEASIBLE -1
#define OVERFLOW -2
typedef int Status;

typedef char ElemType;
typedef struct BiTNode {
    ElemType data;
    struct BiTNode *lchild, *rchild; // 左右孩子指针
} BiTNode, *BiTree;

Status CreateBiTree(BiTree &T) { // 算法6.4
    char ch;
    scanf("%c", &ch);
    if (ch == '#')
        T = NULL;
    else {
        if (!(T = (BiTNode *)malloc(sizeof(BiTNode))))
            return ERROR;
        T->data = ch;            // 生成根结点
        CreateBiTree(T->lchild); // 构造左子树
        CreateBiTree(T->rchild); // 构造右子树
    }
    return OK;
}

Status PreOrderTraverse(BiTree T) {
    if (T) {
        printf("%c", T->data);
        PreOrderTraverse(T->lchild);
        PreOrderTraverse(T->rchild);
    }
    return OK;
}

Status InOrderTraverse(BiTree T) {
    if (T) {
        InOrderTraverse(T->lchild);
        printf("%c", T->data);
        InOrderTraverse(T->rchild);
    }
    return OK;
}

Status PostOrderTraverse(BiTree T) {
    if (T) {
        PostOrderTraverse(T->lchild);
        PostOrderTraverse(T->rchild);
        printf("%c", T->data);
    }
    return OK;
}

int main() {
    BiTree T;
    CreateBiTree(T);
    PreOrderTraverse(T);
    printf("\n");
    InOrderTraverse(T);
    printf("\n");
    PostOrderTraverse(T);
    printf("\n");
    return 0;
}
```

## 58. 17121 求二叉树各种节点数

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=17121&access=242658c0f1849d34fe39cc1b01bcf186&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
构造二叉链表表示的二叉树：按先序次序输入二叉树中结点的值（一个字符），'#'字符表示空树，构造二叉链表表示的二叉树T,并求此二叉树中度为2的节点总数，度为1的节点总数，度为0的节点总数

#include "stdio.h"
#include "malloc.h"
#define TRUE 1
#define FALSE 0
#define OK  1
#define ERROR  0
#define INFEASIBLE -1
#define OVERFLOW -2
typedef int  Status;

typedef char  ElemType;
typedef struct BiTNode{
  ElemType data;
  struct BiTNode *lchild,*rchild;//左右孩子指针
} BiTNode,*BiTree;

Status CreateBiTree(BiTree &T) {  // 算法6.4
  // 按先序次序输入二叉树中结点的值（一个字符），'#'字符表示空树，
  // 构造二叉链表表示的二叉树T。
  char ch;
  scanf("%c",&ch);
  if (ch=='#') T = NULL;
  else {
    if (!(T = (BiTNode *)malloc(sizeof(BiTNode)))) return ERROR;
    ________________________ // 生成根结点
     _______________________   // 构造左子树
    _________________________  // 构造右子树
  }
  return OK;
} // CreateBiTree

int main()   //主函数
{
                      //补充代码
 }//main
```

**输入**

```
第一行输入先序次序二叉树中结点
```

**输出**

```
第一行输出度为2的节点数
第二行输出度为1的节点数
第三行输出度为0的节点数
```

**样例输入**

```
ABC###D##
```

**样例输出**

```
1
1
2
```

**解析**

**题目要求**

根据先序序列构建二叉树，并统计度为 2、度为 1 和度为 0（叶子结点）的结点个数。

**解题思路**

1. **建树**：按照先序序列递归构建二叉链表，`#` 表示空结点。
2. **统计度数**：对二叉树进行深度优先遍历（DFS）。对于每个非空结点，根据其左、右孩子是否为空来确定该结点的度：
   - 左、右孩子均非空 → 度为 2；
   - 左、右孩子恰有一个为空 → 度为 1；
   - 左、右孩子均为空 → 度为 0（叶子结点）。

**算法分析**

- 时间复杂度：O(N)，每个结点访问一次。
- 空间复杂度：O(H)，H 为树高，即递归栈深度。

**C++ 参考答案**

```cpp
#include <iostream>
using namespace std;

struct Node {
    char v;      // 结点值
    Node *l, *r; // 左、右子树指针
};

// 按先序序列递归建树
Node *build() {
    char c;
    if (!(cin >> c))
        return 0;
    if (c == '#')
        return 0;
    return new Node{c, build(), build()};
}

int c0, c1, c2; // 分别记录度为 0、1、2 的结点个数

// 深度优先遍历，统计每个结点的度
void dfs(Node *t) {
    if (!t)
        return;
    // 计算当前结点的度（非空孩子个数）
    int d = (t->l != 0) + (t->r != 0);
    if (d == 0)
        c0++; // 无孩子，叶子结点
    else if (d == 1)
        c1++; // 一个孩子
    else
        c2++;  // 两个孩子
    dfs(t->l); // 递归遍历左子树
    dfs(t->r); // 递归遍历右子树
}

int main() {
    Node *t = build();
    dfs(t);
    // 按题目要求依次输出度为 2、1、0 的结点数
    cout << c2 << "\n" << c1 << "\n" << c0;
}
```

## 59. 18924 二叉树的宽度

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18924&access=2d738b7bb3476e7f7347408e17bba132&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
二叉树的宽度指的是具有节点数目最多的那一层的节点个数。
          1
         / \
        2   3
       /
      4
答案为2, 第二层节点数最多，为2个节点。
```

**输入**

```
共n行。
第一行一个整数n，表示有n个结点，编号为1至n,结点1为树根。（1<=n<=50）
第二行至第n行，每行有两个整数x和y，表示在二叉树中x为y的父节点。x第一次出现时y为左孩子
```

**输出**

```
输出二叉树的宽度。
```

**样例输入**

```
5
1 2
1 3
2 4
2 5
```

**样例输出**

```
2
```

**解析**

**题目要求**

给定一棵二叉树的父子关系，求二叉树的宽度，即所有层中结点数目最多的那一层的结点个数。

**解题思路**

1. **建树**：利用邻接表存储每个结点的子结点。根据题意，每个父结点第一次出现时，其子结点为左孩子；第二次出现时为右孩子。
2. **层序遍历（BFS）**：使用队列进行逐层遍历。每轮循环处理当前层的全部结点，队列在该轮开始时的元素个数即为当前层的结点数目。记录所有层中结点数的最大值即为所求宽度。

**算法分析**

- 时间复杂度：O(N)，每个结点入队、出队各一次。
- 空间复杂度：O(N)，队列最多存储一层的结点。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <queue>
#include <vector>
using namespace std;

int main() {
    int n;
    cin >> n;
    vector<vector<int>> ch(n + 1); // 邻接表，ch[x] 存储结点 x 的子结点
    for (int i = 2, x, y; i <= n; i++) {
        cin >> x >> y;
        ch[x].push_back(y); // 将 y 添加为 x 的子结点
    }

    queue<int> q;
    q.push(1); // 根结点入队
    int ans = 0;

    while (!q.empty()) {
        int sz = q.size();  // 当前层的结点数目
        ans = max(ans, sz); // 更新最大宽度
        while (sz--) {      // 遍历当前层所有结点
            int u = q.front();
            q.pop();
            for (int v : ch[u]) // 将下一层子结点入队
                q.push(v);
        }
    }

    cout << ans;
}
```

## 60. 18724 二叉树的遍历运算

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18724&access=837d495ccab2f59490a3a02c837dd084&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
二叉树的三种遍历都可以通过递归实现。
如果我们知道一棵二叉树的先序和中序序列，可以用递归的方法求后序遍历序列。
```

**输入**

```
两行，第一行一个字符串，表示树的先序遍历，第二行一个字符串，表示树的中序遍历。
树的结点一律用小写字母表示,且字符串长度不超过30。
```

**输出**

```
一个字符串，树的后序序列。
```

**样例输入**

```
abcde
bcade
```

**样例输出**

```
cbeda
```

**解析**

**题目要求**

已知二叉树的先序遍历序列和中序遍历序列，求其后序遍历序列。

**解题思路**

1. **核心性质**：先序遍历的第一个字符即为当前子树的根结点。在中序遍历序列中定位该根结点的位置，则根结点左侧为左子树的中序序列，右侧为右子树的中序序列。
2. **递归划分**：根据左子树的结点个数（由中序序列中根的位置确定），在先序序列中划分出左、右子树的先序序列，然后递归处理。
3. **输出后序**：在递归过程中，先处理左子树，再处理右子树，最后输出根结点，即可得到后序遍历序列。

**注意事项**

- 无需显式构建二叉树，在递归过程中直接输出后序序列即可。
- 在中序序列中查找根结点时，注意限定搜索范围为当前子区间。

**算法分析**

- 时间复杂度：O(N^2)（每次在中序序列中线性查找根的位置）。可通过哈希表优化至 O(N)。
- 空间复杂度：O(H)，递归栈深度。

**C++ 参考答案**

```cpp
#include <iostream>
#include <string>
using namespace std;

string pre, in; // 先序序列和中序序列

// 递归求解后序遍历
// pl, pr: 先序序列的左右边界；il, ir: 中序序列的左右边界
void solve(int pl, int pr, int il, int ir) {
    if (pl > pr)
        return;                          // 空子树，直接返回
    char root = pre[pl];                 // 先序序列首字符为当前子树的根
    int k = in.find(root, il);           // 在中序序列中定位根的位置
    int left = k - il;                   // 左子树的结点个数
    solve(pl + 1, pl + left, il, k - 1); // 递归处理左子树
    solve(pl + left + 1, pr, k + 1, ir); // 递归处理右子树
    cout << root;                        // 后序遍历：左、右之后输出根
}

int main() {
    cin >> pre >> in;
    solve(0, pre.size() - 1, 0, in.size() - 1);
}
```

## 61. 18923 二叉树的直径

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18923&access=f03a42ff623e944dcba091a0f6ba03e1&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
给定一棵二叉树，你需要计算它的直径长度。一棵二叉树的直径长度是任意两个结点路径长度中的最大值。这条路径可能穿过也可能不穿过根结点。
          1
         / \
        2   3
       / \
      4   5
答案为3, 它的长度是路径 [4,2,1,3] 或者 [5,2,1,3]。
```

**输入**

```
共n行。
第一行一个整数n，表示有n个结点，编号为1至n。
第二行至第n行，每行有两个整数x和y，表示在二叉树中x为y的父节点。x第一次出现时y为左孩子
```

**输出**

```
输出二叉树的直径。
```

**样例输入**

```
5
1 2
1 3
2 4
2 5
```

**样例输出**

```
3
```

**解析**

**题目要求**

求二叉树的直径，即树中任意两个结点之间路径边数的最大值。

**解题思路**

1. **核心性质**：经过某一结点的最长路径，等于该结点左右子树的最大深度之和。因此，二叉树的直径就是所有结点上"左子树深度 + 右子树深度"的最大值。
2. **DFS 求解**：在深度优先遍历过程中，对每个结点同时完成两件事——
   - 返回以该结点为根的子树的高度（即左、右子树高度的较大值加 1）；
   - 用该结点的左、右子树高度之和更新全局最大直径。

**注意事项**

- 直径定义为路径上的边数，等于路径上的结点数减 1。但本题样例以路径上的边数为准，代码中 `ans` 记录的 `a + b` 即为经过当前结点的最长路径边数。

**算法分析**

- 时间复杂度：O(N)，每个结点访问一次。
- 空间复杂度：O(H)，递归栈深度。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;

int ans = 0;            // 记录全局最大直径
vector<vector<int>> ch; // 邻接表，ch[u] 存储结点 u 的子结点

// 返回以 u 为根的子树的最大深度，同时更新直径
int dep(int u) {
    int a = 0, b = 0; // a 为最大子树深度，b 为次大子树深度
    for (int v : ch[u]) {
        int d = dep(v);
        if (d > a) {
            b = a;
            a = d;
        } // 更新最大和次大深度
        else if (d > b) {
            b = d;
        }
    }
    ans = max(ans, a + b); // 经过当前结点的最长路径 = 最大深度 + 次大深度
    return a + 1;          // 返回当前子树的最大深度
}

int main() {
    int n;
    cin >> n;
    ch.assign(n + 1, {});
    for (int i = 2, x, y; i <= n; i++) {
        cin >> x >> y;
        ch[x].push_back(y); // 构建父子关系
    }
    dep(1);      // 从根结点开始 DFS
    cout << ans; // 输出最大直径
}
```

## 62. 8609 哈夫曼树

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8609&access=da037fcf90ab61cfe153c90a9f295304&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
利用静态链表建立赫夫曼树，建树过程中要求左子树权值小于右子树权值，求各结点的编码。要求：叶子结点的个数n及结点值由键盘录入。本题给出程序代码,要求填空以满足测试要求.
#include "stdio.h"
#include "string.h"
#include "malloc.h"
using namespace std;
typedef struct
{
    unsigned int weight;
    unsigned int parent,lchild,rchild;
} HTNode,*HuffmanTree;
typedef char **HuffmanCode;
void   select(HuffmanTree &HT, int n, int &s1, int &s2)
{//在HT[1..n]中选择parent为0且weight最小的两个结点， 其序号分别为s1（最小）和s2（次小）。
   __________________________
}
void createHuffmanTree(HuffmanTree &HT, int n)
{ //构造哈夫曼树HT
    int i, m, s1, s2;
    if (n>HT[i].weight;
    for (i=n+1; i<=m; i++)    // 建哈夫曼树
    { //在HT[1..i-1]中选择parent为0且weight最小的两个结点， 其序号分别为s1(最小)和s2(次小)
         _______________________________
    }
}
void createHuffmanCode(HuffmanTree HT,HuffmanCode &HC,int n)
{//--- 从叶子到根逆向求每个字符的哈夫曼编码 ---
    char *cd = new char[n];    // 分配求编码的工作空间
    cd[n-1] = '\0';  // 编码结束符。
    int i,c,f,start;
    for (i=1; i<=n; ++i)
    {
        start = n-1;
        c=i, f=HT[i].parent;
        while(f)// 从叶子到根逆向求编码
        {
            --start;
            if (HT[f].lchild==c) cd[start] = '0';
            else cd[start] = '1';
            c=f,f=HT[f].parent;
        }
        HC[i] = new char[n-start];// 为第i个字符编码分配空间
        strcpy(HC[i], &cd[start]);    // 从cd复制编码(串)到HC
    }
}
int main()
{
    int i,n;
    int *w;
    HuffmanTree HT;
    HuffmanCode HC;
    scanf("%d",&n);  //权值个数
    HC=new char*[n+1]; //0空间未用
    createHuffmanTree(HT,n);
    createHuffmanCode(HT,HC,n);
    for (i = 1; i<=n; i++)
        printf("%s\n",HC[i]);  //输出哈夫曼编码
}
```

**输入**

```
第一行：权值个数
第二行：输入n个权值，用空格分隔
```

**输出**

```
输出n行
每行表示各权值对应的哈夫曼编码
```

**样例输入**

```
8
5 29 7 8 14 23 3 11
```

**样例输出**

```
0001
10
1110
1111
110
01
0000
001
```

**解析**

**题目要求**

给定 n 个权值，构建哈夫曼树并输出每个叶子结点的哈夫曼编码。要求建树时左子树权值不大于右子树权值。

**解题思路**

1. **构建哈夫曼树**（贪心策略）：
   - 将 n 个权值作为 n 棵只有根结点的二叉树。
   - 每次从所有尚未合并的树（即 parent 为 0 的结点）中，选取权值最小的两棵进行合并，生成一个新的内部结点作为它们的父结点，新结点的权值为两棵子树权值之和。
   - 重复合并 n-1 次，最终形成一棵包含 2n-1 个结点的哈夫曼树。

2. **生成哈夫曼编码**：
   - 从每个叶子结点出发，沿 parent 指针逆向回溯到根结点。
   - 若当前结点是其父结点的左孩子，则编码为 `0`；若为右孩子，则编码为 `1`。
   - 将所得编码序列逆序，即为该叶子结点的哈夫曼编码。

**注意事项**

- 当 n = 1 时，哈夫曼树只有一个结点，其编码为 `0`。
- 选取最小权值结点时，需确保两个结点不同且均未被合并（parent 为 0）。

**算法分析**

- 时间复杂度：O(N^2)，每轮合并需线性扫描所有候选结点。
- 空间复杂度：O(N)，存储哈夫曼树和编码。

**C++ 参考答案**

```cpp
#include "malloc.h"
#include "stdio.h"
#include "string.h"
using namespace std;
typedef struct {
    unsigned int weight;
    unsigned int parent, lchild, rchild;
} HTNode, *HuffmanTree;
typedef char **HuffmanCode;

void select(HuffmanTree &HT, int n, int &s1, int &s2) {
    // 在HT[1..n]中选择parent为0且weight最小的两个结点，序号分别为s1（最小）和s2（次小）。
    s1 = s2 = 0;
    for (int i = 1; i <= n; i++) {
        if (HT[i].parent != 0)
            continue;
        if (s1 == 0 || HT[i].weight < HT[s1].weight) {
            s2 = s1;
            s1 = i;
        } else if (s2 == 0 || HT[i].weight < HT[s2].weight) {
            s2 = i;
        }
    }
}

void createHuffmanTree(HuffmanTree &HT, int n) { // 构造哈夫曼树HT
    int i, m, s1, s2;
    if (n <= 0)
        return;
    m = 2 * n - 1;
    HT = new HTNode[m + 1];
    for (i = 1; i <= m; i++) {
        HT[i].weight = 0;
        HT[i].parent = HT[i].lchild = HT[i].rchild = 0;
    }
    for (i = 1; i <= n; i++)
        scanf("%u", &HT[i].weight);
    for (i = n + 1; i <= m; i++) // 建哈夫曼树
    {
        select(HT, i - 1, s1, s2);
        if (HT[s1].weight > HT[s2].weight) {
            int t = s1;
            s1 = s2;
            s2 = t;
        }
        HT[s1].parent = HT[s2].parent = i;
        HT[i].lchild = s1;
        HT[i].rchild = s2;
        HT[i].weight = HT[s1].weight + HT[s2].weight;
    }
}

void createHuffmanCode(HuffmanTree HT, HuffmanCode &HC,
                       int n) { // --- 从叶子到根逆向求每个字符的哈夫曼编码 ---
    if (n == 1) {
        HC[1] = new char[2];
        strcpy(HC[1], "0");
        return;
    }
    char *cd = new char[n]; // 分配求编码的工作空间
    cd[n - 1] = '\0';       // 编码结束符。
    int i, c, f, start;
    for (i = 1; i <= n; ++i) {
        start = n - 1;
        c = i, f = HT[i].parent;
        while (f) // 从叶子到根逆向求编码
        {
            --start;
            if (HT[f].lchild == c)
                cd[start] = '0';
            else
                cd[start] = '1';
            c = f, f = HT[f].parent;
        }
        HC[i] = new char[n - start]; // 为第i个字符编码分配空间
        strcpy(HC[i], &cd[start]);   // 从cd复制编码(串)到HC
    }
    delete[] cd;
}

int main() {
    int i, n;
    HuffmanTree HT;
    HuffmanCode HC;
    scanf("%d", &n);        // 权值个数
    HC = new char *[n + 1]; // 0空间未用
    createHuffmanTree(HT, n);
    createHuffmanCode(HT, HC, n);
    for (i = 1; i <= n; i++)
        printf("%s\n", HC[i]); // 输出哈夫曼编码
    return 0;
}
```

# 拓展习题4

## 63. 18723 FBI树

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18723&access=e9ef0d980d66d588c24b3c1a1913cb71&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
我们可以把由"0"和"1"组成的字符串分为三类：全"0"串称为B串，全"1"串称为I串，既含"0"又含"1"的串则称为F串。
FBI树是一种二叉树，它的结点类型也包括F结点，B结点和I结点三种。一个长度为2^n的"01"串S可以构造出一棵FBI树T，递归的构造方法如下：
1)T的根结点为R，其类型与串S的类型相同；
2)若串S的长度大于1，将串S从中间分开，分为等长的左右子串S1和S2；由左子串S1构造R的左子树T1，由右子串S2构造R的右子树T2。
现在给定一个长度为2的n次幂的"01"串，请用上述构造方法构造出一棵FBI树，并输出它的后序遍历*2序列。
```

**输入**

```
第一行是一个整数N（0 ≤ N ≤ 10），第二行是一个长度为2^N的"01"串。
```

**输出**

```
一行，这一行只包含一个字符串，即FBI树的后序遍历序列。
```

**样例输入**

```
3
10001011
```

**样例输出**

```
IBFBBBFIBFIIIFF

Hint

两种方法：
（1）二叉树首选算法，二分递归。即建树的同时后序遍历
（2）利用完全二叉树性质存储和构造二叉树，再后序遍历。

Source

	NOIP 2004
```

**解析**

**题目要求**

根据给定的 "01" 字符串递归构建 FBI 树，并输出该树的后序遍历序列。其中：全 `0` 串对应 B 结点，全 `1` 串对应 I 结点，混合串对应 F 结点。

**解题思路**

1. **递归二分**：将字符串不断从中间分为等长的左、右两个子串，直到子串长度为 1 时确定叶子结点类型（`0` 为 B，`1` 为 I）。
2. **自底向上判断结点类型**：
   - 若左、右子树返回的类型相同，则当前结点类型与之相同；
   - 若左、右子树类型不同，则当前结点必为 F 类型。
3. **后序输出**：在递归过程中，先输出左子树的结果，再输出右子树的结果，最后输出当前结点的类型字符，即自然满足后序遍历的要求。

**算法分析**

- 时间复杂度：O(N)，其中 N 为字符串长度。每个区间处理一次，总区间数不超过 2N。
- 空间复杂度：O(log N)，递归深度为 N 的二分次数。

**C++ 参考答案**

```cpp
#include <iostream>
#include <string>
using namespace std;

string s; // 输入的 "01" 字符串

// 递归处理区间 [l, r]，返回该区间的结点类型字符
char dfs(int l, int r) {
    if (l == r) {
        // 叶子结点：单个字符直接判断类型
        char c = s[l] == '0' ? 'B' : 'I';
        cout << c;
        return c;
    }
    int m = (l + r) / 2;         // 将区间一分为二
    char a = dfs(l, m);          // 递归处理左半部分
    char b = dfs(m + 1, r);      // 递归处理右半部分
    char c = (a == b ? a : 'F'); // 左右类型相同则继承，否则为 F
    cout << c;                   // 后序输出当前结点类型
    return c;
}

int main() {
    int n;
    cin >> n >> s;
    dfs(0, s.size() - 1);
}
```

## 64. 17263 计算二叉树的第k层中所有叶子结点个数

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=17263&access=f7d4fbeaf93566e0512f767d83f8cc46&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
二叉链表表示的二叉树：按先序次序输入二叉树中结点的值，'#'字符表示空树，构造二叉链表表示的二叉树T（该二叉树中的结点为单个字符并且无值重复的结点）,
编写算法完成：计算二叉树的第k层中所有叶子结点个数，根结点为第1层，根结点的孩子结点为第2层，依次类推。
#include "stdio.h"
#include "malloc.h"
#define TRUE 1
#define FALSE 0
#define OK  1
#define ERROR  0
#define INFEASIBLE -1
#define OVERFLOW -2
typedef int  Status;

typedef char  ElemType;
typedef struct BiTNode{
  ElemType data;
  struct BiTNode *lchild,*rchild;//左右孩子指针
} BiTNode,*BiTree;

Status CreateBiTree(BiTree &T) {  // 算法6.4
  // 按先序次序输入二叉树中结点的值（一个字符），'#'字符表示空树，
  // 构造二叉链表表示的二叉树T。
  char ch;
  scanf("%c",&ch);
  if (ch=='#') T = NULL;
  else {
    if (!(T = (BiTNode *)malloc(sizeof(BiTNode)))) return ERROR;
    ________________________ // 生成根结点
     _______________________   // 构造左子树
    _________________________  // 构造右子树
  }
  return OK;
} // CreateBiTree

int main()   //主函数
{
                      //补充代码
 }//main
```

**输入**

```
第一行输入先序次序二叉树中结点
第二行输入层次k
```

**输出**

```
第一行输出该二叉树的第k层中所有叶子结点个数
```

**样例输入**

```
ABC###D##
2
```

**样例输出**

```
1
```

**解析**

**题目要求**

根据先序序列构建二叉树，统计第 k 层中叶子结点（即左右子树均为空的结点）的个数。根结点位于第 1 层。

**解题思路**

1. **建树**：按先序序列递归构建二叉链表，`#` 表示空结点。
2. **带层号的 DFS 遍历**：在深度优先遍历过程中携带当前层号参数。当遍历到第 k 层时，检查该结点是否为叶子结点（左右孩子均为空），若是则计数器加 1。

**注意事项**

- 层号从 1 开始计数（根结点为第 1 层），递归进入子树时层号加 1。
- 仅在第 k 层统计叶子结点，其他层无需判断。

**算法分析**

- 时间复杂度：O(N)，最坏情况下需要遍历整棵树。
- 空间复杂度：O(H)，递归栈深度。

**C++ 参考答案**

```cpp
#include <iostream>
using namespace std;

struct Node {
    char v;      // 结点值
    Node *l, *r; // 左、右子树指针
};

// 按先序序列递归建树
Node *build() {
    char c;
    if (!(cin >> c))
        return 0;
    if (c == '#')
        return 0;
    return new Node{c, build(), build()};
}

int k, ans = 0;

// 带层号的深度优先遍历，统计第 k 层的叶子结点数
void dfs(Node *t, int d) {
    if (!t)
        return;
    // 到达第 k 层且当前结点为叶子结点时，计数加 1
    if (d == k && !t->l && !t->r)
        ans++;
    dfs(t->l, d + 1); // 递归遍历左子树，层号加 1
    dfs(t->r, d + 1); // 递归遍历右子树，层号加 1
}

int main() {
    Node *t = build(); // 构建二叉树
    cin >> k;          // 读入目标层号
    dfs(t, 1);         // 从根结点（第 1 层）开始遍历
    cout << ans;
}
```

## 65. 18959 二叉树的之字形遍历

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18959&access=2647a752da73bc8942935fa3b9d41e53&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
题目来源：字节跳动测试题

给定一个二叉树，返回该二叉树的之字形层序遍历，（第一层从左向右，下一层从右向左，一直这样交替）
例如：
给定的二叉树是{3,9,20,#,#,15,7},

该二叉树之字形层序遍历的结果是
3
20 9
15 7
```

**输入**

```
一行字符串，只包含大写字母和#,#为空子树。
此处采用完全二叉树的顺序存储结构。
```

**输出**

```
若干行，之字形输出树的结点，每一行输出树的一层。
```

**样例输入**

```
ABC###D
```

**样例输出**

```
A
C B
D
```

**解析**

**题目要求**

对完全二叉树顺序存储结构进行之字形（锯齿形）层序遍历：奇数层从左向右输出，偶数层从右向左输出，逐层交替。

**解题思路**

1. **完全二叉树的顺序存储**：字符串下标 i 处的结点，其左孩子位于 2i+1，右孩子位于 2i+2。
2. **逐层遍历**：维护当前层所有结点的下标列表。对每一层，筛选出有效的非空结点（下标未越界且字符不为 `#`）。
3. **交替反向**：使用布尔标志 `rev` 控制输出方向。奇数层（从 0 开始计数时为偶数索引层）正向输出，偶数层反向输出，每处理完一层翻转标志。

**注意事项**

- 需要跳过 `#` 位置的空结点，仅输出有效结点。
- 同一层的结点之间用空格分隔，每层输出一行。

**算法分析**

- 时间复杂度：O(N)，每个结点处理常数次。
- 空间复杂度：O(N)，存储每层结点的下标列表。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <string>
#include <vector>
using namespace std;

int main() {
    string s;
    cin >> s;
    int n = s.size();
    vector<int> cur = {0}; // 当前层的结点下标列表，初始为根结点
    bool rev = false;      // 是否反向输出当前层

    while (!cur.empty()) {
        vector<int> vals, next; // vals 存储当前层有效结点下标，next 存储下一层下标
        for (int idx : cur) {
            if (idx < n && s[idx] != '#') { // 跳过越界和空结点
                vals.push_back(idx);
                int l = 2 * idx + 1, r = 2 * idx + 2; // 计算左右孩子下标
                if (l < n)
                    next.push_back(l);
                if (r < n)
                    next.push_back(r);
            }
        }
        if (vals.empty())
            break; // 当前层无有效结点，终止遍历
        if (rev)
            reverse(vals.begin(), vals.end()); // 偶数层反向输出
        for (int i = 0; i < (int)vals.size(); i++)
            cout << s[vals[i]] << (i + 1 == (int)vals.size() ? '\n' : ' ');
        cur = next; // 进入下一层
        rev = !rev; // 翻转输出方向
    }
}
```

## 66. 19069 二叉树的右视图

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19069&access=af0a446a7c83ed1b00baf844a84fcf7c&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
字节跳动2021面试题

给定一个二叉树的根节点 root，想象自己站在它的右侧，按照从顶部到底部的顺序，返回从右侧所能看到的节点值。
比如此树
   1            <---
 /   \
2     3         <---
 \
  5             <---
从右侧看过去，答案是1,3,5。
实际上右视图就是二叉树层次遍历时每一层最右侧节点序列。

    #include <stdio.h>
#include <malloc.h>
typedef long long ll;
using namespace std;
typedef struct BiTNode
{
    char data;
    struct BiTNode *lchild,*rchild;//左右孩子指针
} BiTNode,*BiTree;
void  CreateBiTree(BiTree &T)
{ /**< 先序建树算法 */
    char ch;
    scanf("%c",&ch);
    if (ch=='#') T = NULL;
    else
    {
        T = (BiTNode *)malloc(sizeof(BiTNode));
        T->data=ch;
        CreateBiTree(T->lchild);
        CreateBiTree(T->rchild);
    }
}
void Rview(BiTree T)
{/**< 右视图算法，用队列作为辅助存储结构 */
   _______________________
}
int main()
{
    BiTree T;
    CreateBiTree(T);
    Rview(T);
    return 0;
}
```

**输入**

```
输入二叉树的先序序列（只包含大写字母和#，大写字母代表树节点）。
```

**输出**

```
输出右视图的结果序列。
```

**样例输入**

```
AB##C##
```

**样例输出**

```
AC

Hint

层次遍历使用队列作为辅助结构，处理每一层的时队列的队尾元素就是每一层的最后一个节点。
```

**解析**

**题目要求**

输出二叉树的右视图，即从右侧观察二叉树时，从顶部到底部依次可见的结点值。等价于层序遍历中每一层最右侧的结点。

**解题思路**

1. **层序遍历（BFS）**：使用队列对二叉树进行逐层遍历。
2. **取每层最后一个结点**：每轮循环处理一层，记录该轮开始时队列中的元素个数 `sz`。依次出队 `sz` 个结点，其中最后一个出队的结点即为该层最右侧的结点，将其值输出。

**注意事项**

- 必须严格按层处理：每次取出当前层全部结点后，再将下一层子结点入队。
- 右视图结点的输出无需分隔符，连续输出即可。

**算法分析**

- 时间复杂度：O(N)，每个结点入队、出队各一次。
- 空间复杂度：O(N)，队列最多存储一层的结点。

**C++ 参考答案**

```cpp
#include <iostream>
#include <queue>
using namespace std;

struct Node {
    char v;      // 结点值
    Node *l, *r; // 左、右子树指针
};

// 按先序序列递归建树
Node *build() {
    char c;
    if (!(cin >> c))
        return 0;
    if (c == '#')
        return 0;
    return new Node{c, build(), build()};
}

int main() {
    Node *t = build();
    queue<Node *> q;
    if (t)
        q.push(t); // 根结点入队

    while (!q.empty()) {
        int sz = q.size(); // 当前层的结点数目
        for (int i = 0; i < sz; i++) {
            auto u = q.front();
            q.pop();
            if (i == sz - 1)
                cout << u->v; // 每层最后一个结点即为右视图结点
            if (u->l)
                q.push(u->l); // 左孩子入队
            if (u->r)
                q.push(u->r); // 右孩子入队
        }
    }
}
```

## 67. 19081 树上摘樱桃（★）

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19081&access=a6e2875235e508b4a14348b75730a1b3&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
网易2021校招笔试-算法工程师（正式第一批）

有一棵二叉树，树上的叶子节点定义为"樱桃"。现在需要找出树上有多少个满足如下子结构的"樱桃"串，即一串上刚好有两颗"樱桃"。
简单说，就是某个节点的左右孩子都是叶子节点，即为一个串。
比如如下的一棵树，红框标示的有两个符合要求的结构，答案就是2
```

**输入**

```
第一行两个正整数m, n，空格分开，分别代表总共有树上有多少个节点，和树上有多少条边，2<=m<=100,  1<=n<=100
下面有n行，每行为3个部分，用空格分割，第一个数字为某非叶子节点的id,
 第二个为该边为left还是right，第三个为子节点的id
注意：节点id彼此不会重复，id 1为根节点
```

**输出**

```
一个整数，标示符合要求的结构的数量。
```

**样例输入**

```
10 9
1 left 2
1 right 3
2 left 4
2 right 5
3 right 6
6 left 7
6 right 8
8 left 9
8 right 10
```

**样例输出**

```
2

Hint

如题目说明的第一个样例图，可以看到，2-4-5子串，8-9-10子串，两个子串符合条件，所以答案为2
```

**解析**

**题目要求**

统计二叉树中"樱桃串"的个数。樱桃串的定义为：某个结点的左、右孩子均存在，且这两个孩子都是叶子结点（即无自己的子结点）。

**解题思路**

1. **记录孩子关系**：使用数组 `L[i]` 和 `R[i]` 分别记录结点 i 的左孩子和右孩子的编号。
2. **枚举判断**：遍历所有结点，对于每个结点 i，检查：
   - `L[i]` 和 `R[i]` 均非零（即左、右孩子都存在）；
   - `L[i]` 和 `R[i]` 本身都没有左、右孩子（即两者均为叶子结点）。
   若以上条件同时满足，则该结点构成一个樱桃串，计数器加 1。

**注意事项**

- 判断一个结点是否为叶子结点，只需检查其 `L` 和 `R` 是否均为 0。
- 题目保证结点 id 不重复，且 id 为 1 的结点是根结点。

**算法分析**

- 时间复杂度：O(M)，枚举所有结点并做常数时间判断。
- 空间复杂度：O(M)，存储孩子关系数组。

**C++ 参考答案**

```cpp
#include <iostream>
#include <string>
#include <vector>
using namespace std;

int main() {
    int m, n;
    cin >> m >> n;
    vector<int> L(m + 1), R(m + 1); // L[i]、R[i] 分别记录结点 i 的左、右孩子
    for (int i = 0; i < n; i++) {
        int a, b;
        string side;
        cin >> a >> side >> b;
        if (side == "left")
            L[a] = b; // 记录左孩子
        else
            R[a] = b; // 记录右孩子
    }

    int ans = 0;
    for (int i = 1; i <= m; i++) {
        // 判断：左右孩子均存在，且均为叶子结点
        if (L[i] && R[i] && !L[L[i]] && !R[L[i]] // 左孩子是叶子
            && !L[R[i]] && !R[R[i]])             // 右孩子是叶子
            ans++;
    }
    cout << ans;
}
```

## 68. 19083 二叉树的最长路径

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19083&access=acd2d98add26a82b12c232d4270867a5&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
二叉树中，任意两个节点间都存在一条唯一的路径，请求出所有路径中最长的路径长度。
```

**输入**

```
第一行为一个整数n，表示结点个数，结点以数字编号，根节点为1。n<10
第二行为一个数字和#号组成的字符串，采用完全二叉树的存储形式，#表示空树。
```

**输出**

```
输出所有路径中最长的路径长度
```

**样例输入**

```
5
1234##5
```

**样例输出**

```
4

Hint

样例最长路径为（4,5），路径长度为4
```

**解析**

**题目要求**

给定完全二叉树的顺序存储序列，求树中任意两个结点之间最长路径的长度。由样例可知，本题的路径长度按**边数**计算。

**解题思路**

1. **本质与二叉树直径相同**：对于每个结点，经过该结点的最长路径边数等于其左子树最大深度加上右子树最大深度。
2. **递归求解**：利用完全二叉树的顺序存储性质（下标 i 的结点，左孩子为 2i+1，右孩子为 2i+2），递归计算每个结点左右子树的最大深度。在递归过程中，用 `left + right` 更新全局最大值。

**注意事项**

- 注意 `#` 表示空结点，需跳过处理。
- 下标越界或字符为 `#` 时，返回深度 0。
- 输入的 `n` 表示非空结点数，不是顺序存储字符串长度，递归边界应以字符串长度为准。

**算法分析**

- 时间复杂度：O(N)，每个结点访问一次。
- 空间复杂度：O(H)，递归栈深度。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <functional>
#include <iostream>
#include <string>
using namespace std;

int main() {
    int n;
    string s;
    cin >> n >> s;
    int ans = 0;

    // 递归计算以 i 为根的子树的最大深度，同时更新最长路径
    function<int(int)> dep = [&](int i) {
        if (i >= (int)s.size() || s[i] == '#')
            return 0;              // 空结点或越界，深度为 0
        int l = dep(i * 2 + 1);    // 左子树最大深度
        int r = dep(i * 2 + 2);    // 右子树最大深度
        ans = max(ans, l + r);     // 经过当前结点的最长路径边数
        return max(l, r) + 1;      // 返回当前子树的最大深度
    };

    dep(0); // 从根结点（下标 0）开始
    cout << ans;
}
```

## 69. 18946 小美的送花线路

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18946&access=0b2a4b11251c7df07018e6856278fc44&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
美团2021校招笔试-编程题(通用编程试题,第1场)
小美是美团的一名鲜花快递员，鲜花是一种保质期非常短的商品，所以需要尽快送到客户手中。

公司对于骑手的一个要求就是要规划送花的线路，使得骑手送完所有订单走的路程尽可能少。

(骑手开始派送时带走了所有需要派送的花，不必每单后返回花店，路程结算是从花店出发，到送完最后一名客户为止，不计算从最后一名客户家回到花店的时间)

公司对于骑手的绩效评价是取决于两个指标，一是从花店到所有客户地址的距离之和，另一个是骑手实际走的路程。

设花店始终位于1号位置，客户共有n-1个，其编号为2...n。令dis(i,j)表示i号位置到j号位置的距离，

即分别计算dis(1,2)+dis(1,3)+.....+dis(1,n)的总和, 以及骑手实际所走的最短路程。

为了简化问题，我们约束这n个位置构成的是一棵树，即只有n-1条边在其中互相连接，且保证n个点彼此连通。
```

**输入**

```
输出第一行包含一个正整数n，即花店和客户的总数。(1<=n<=100000)

接下来有n-1行，每行有三个整数u,v,w，表示在u和v之间存在一条距离为w的道路。(1<=w<=1000)
```

**输出**

```
输出包含两个整数，中间用空格隔开，分别表示花店到所有客户地址的距离之和和骑手实际走的路程。
```

**样例输入**

```
5
1 2 3
1 3 1
1 4 2
2 5 1
```

**样例输出**

```
10 10

Hint

搜索算法。
```

**解析**

**题目要求**

给定一棵以 1 号结点（花店）为根的带权树，求：
1. 花店到所有客户（其余结点）的距离之和；
2. 从花店出发、遍历所有客户结点的最短行走路程（无需返回花店）。

**解题思路**

1. **距离之和**：通过 DFS 从根结点出发，累加根到每个结点的距离即可。
2. **最短行走路程**：骑手需要走遍树中所有边才能到达每个客户。在最优路线中，除了最后一条行走路径（从根到最远客户的路径）上的边只需经过一次外，其余每条边都需要经过两次（去和回）。因此：

   **最短行走路程 = 所有边权之和 × 2 − 花店到最远客户的距离**

**注意事项**

- 距离之和可能超过 int 范围，需使用 long long 类型。
- 最远距离在 DFS 过程中同步维护即可。

**算法分析**

- 时间复杂度：O(N)，一次 DFS 遍历即可。
- 空间复杂度：O(N)，邻接表存储。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <stack>
#include <utility>
#include <vector>
using namespace std;

struct State {
    int u, p;
    long long d;
};

int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);

    int n;
    cin >> n;
    vector<vector<pair<int, int>>> g(n + 1); // 邻接表：g[u] = {(v, w), ...}
    long long total = 0;                     // 所有边权之和

    for (int i = 1, u, v, w; i < n; i++) {
        cin >> u >> v >> w;
        g[u].push_back({v, w});
        g[v].push_back({u, w});
        total += w;
    }

    long long sum = 0; // 花店到所有客户的距离之和
    long long mx = 0;  // 花店到最远客户的距离

    // 显式栈 DFS，避免 n=100000 时递归过深导致栈溢出
    stack<State> st;
    st.push({1, 0, 0});
    while (!st.empty()) {
        State cur = st.top();
        st.pop();
        sum += cur.d;        // 累加根到当前结点的距离
        mx = max(mx, cur.d); // 更新最远距离
        for (auto [v, w] : g[cur.u]) {
            if (v != cur.p)
                st.push({v, cur.u, cur.d + w});
        }
    }

    // 输出距离之和与最短行走路程
    cout << sum << ' ' << 2 * total - mx;
}
```

## 70. 18929 最优二叉树

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18929&access=bae3bc316b2369cc587d5401bda653d7&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
美团2021校招笔试-编程题(通用编程试题,第10场) 第四题
小团有一个由N个节点组成的二叉树，每个节点有一个权值。

定义二叉树每条边的开销为其两端节点权值的乘积，二叉树的总开销即每条边的开销之和。

小团按照二叉树的中序遍历依次记录下每个节点的权值，即他记录下了N个数，第i个数表示位于中序遍历第i个位置的节点的权值。

之后由于某种原因，小团遗忘了二叉树的具体结构。在所有可能的二叉树中，总开销最小的二叉树被称为最优二叉树。

现在，小团请小美求出最优二叉树的总开销。

最优二叉树如图所示，总开销为7*1+6*5+5*1+1*3=45。
```

**输入**

```
第一行输入一个整数N（1<=N<=300），表示二叉树的节点数。

第二行输入N个由空格隔开的整数，表示按中序遍历记录下的各个节点的权值，所有权值均为不超过1000的正整数。
```

**输出**

```
输出一个整数，表示最优二叉树的总开销。
（根据题目数据，答案有可能超过int范围）
```

**样例输入**

```
5
7 6 5 1 3
```

**样例输出**

```
45

Hint

凡是二叉树的题目都可以先考虑二分递归的方法，可以假定1-n节点是一棵树，这颗树的父节点是0号节点（不存在），dfs(1,n,0)。

通过枚举树的树根i（从1...n均可）将问题二分为dfs(1,i-1,i),dfs(i+1,n,i)。

为了降低复杂度，此题目应该采用记忆化搜索。
```

**解析**

**题目要求**

给定二叉树中序遍历序列中各结点的权值，在所有可能的二叉树结构中找到总边开销最小的一棵。边的开销定义为其两端结点权值的乘积。

**解题思路**

本题采用**区间 DP（记忆化搜索）**的方法：

1. **状态定义**：`dfs(l, r, p)` 表示在中序遍历区间 [l, r] 内构造子树，该子树的父结点编号为 p 时的最小开销。
2. **状态转移**：枚举区间 [l, r] 中的每个位置 k 作为根结点，将区间划分为左子树 [l, k-1] 和右子树 [k+1, r]，递归求解。总开销包括：
   - 当前根 k 与其父结点 p 之间的边开销：`a[p] * a[k]`（若 p 不存在则为 0）；
   - 左子树的最小开销：`dfs(l, k-1, k)`；
   - 右子树的最小开销：`dfs(k+1, r, k)`。
3. **取最小值**：对所有可能的根 k，选取使总开销最小的方案。
4. **记忆化**：使用三维数组 `dp[l][r][p]` 存储已计算的状态，避免重复计算。

**注意事项**

- 答案可能超过 int 范围，需使用 long long 类型。
- 初始调用为 `dfs(1, N, 0)`，表示整棵树无父结点。

**算法分析**

- 时间复杂度：O(N^4)，状态数 O(N^3)，每个状态枚举 O(N) 个根。
- 空间复杂度：O(N^3)，记忆化数组。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <cstring>
#include <iostream>
using namespace std;

int n;
long long a[305];            // 中序遍历各结点的权值（下标从 1 开始）
long long dp[305][305][305]; // 记忆化数组：dp[l][r][p]

// 区间 DP：在 [l, r] 区间内构造子树，p 为父结点编号
long long dfs(int l, int r, int p) {
    if (l > r)
        return 0; // 空子树，开销为 0
    long long &res = dp[l][r][p];
    if (res != -1)
        return res; // 已计算过，直接返回

    const long long INF = (1LL << 62);
    res = INF; // 初始化为极大值
    for (int k = l; k <= r; k++) {
        // 枚举 k 为根：当前边开销 + 左子树开销 + 右子树开销
        long long cost = (p ? a[p] * a[k] : 0) + dfs(l, k - 1, k) + dfs(k + 1, r, k);
        res = min(res, cost); // 取最小开销
    }
    return res;
}

int main() {
    cin >> n;
    for (int i = 1; i <= n; i++)
        cin >> a[i];
    memset(dp, -1, sizeof(dp)); // 初始化记忆化数组为 -1（未计算）
    cout << dfs(1, n, 0);       // 从完整区间开始，无父结点
}
```
# 实验5

## 71. 8610 顺序查找

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8610&access=5a22812ec7ad154c0aafefb60774e2a3&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
编写Search_Seq函数，实现在一个无序表ST中采用顺序查找算法查找值为key的元素的算法.

#include"malloc.h" /* malloc()等 */
#include"stdio.h"
#include"stdlib.h"

typedef int ElemType;
typedef struct /*静态查找表的顺序存储结构 */
{
	ElemType *elem; /* 数据元素存储空间基址，建表时按实际长度分配，0号单元留空 */
	int length; /* 表长度 */
}SSTable;

void Creat_Seq(SSTable &ST,int n)
{ /* 操作结果: 构造一个含n个数据元素的静态顺序查找表ST(数据来自数组r) */
	int i,temp;
	ST.elem=(ElemType *)malloc((n+1) * sizeof(ElemType)); /* 动态生成n个数据元素空间(0号单元不用) */
	if(!(ST).elem)
	{
		printf("ERROR\n");
		exit(0);
	} /*内存分配失败结束程序*/
	for(i=1;i<=n;i++)
	{
		scanf("%d",&temp);
		*(ST.elem+i)=temp; /* 依次赋值给ST */
	}
	ST.length=n;
}

int Search_Seq(SSTable &ST,ElemType key)
{ /* 在顺序表ST中顺序查找其关键字等于key的数据元素。若找到，则函数值为 */
/* 该元素在表中的位置，否则为0。算法9.1 */

}

main()
{
	SSTable ST;
	int loc,key;
	int n;
	scanf("%d",&n);
	Creat_Seq(ST,n);
	//printf("Please input the key value：");
	scanf("%d",&key);
	loc = Search_Seq(ST,key);
	if(loc!=0)
		printf("The element position is %d.\n",loc);
	else
		printf("The element is not exist.\n");
}
```

**输入**

```
第一行:元素个数n
第二行：依次输入n个元素的值
第三行：输入要查找的关键字key的值
```

**输出**

```
输出分两种情形：
1.如果key值存在，则输出其在表中的位置x(表位置从1开始),格式为The element position is x.
2.如果key值不存在输出："The element is not exist."
```

**样例输入**

```
6
1 3 5 7 9 10
5
```

**样例输出**

```
The element position is 3.
```

**解析**

**题目要求**

在给定的无序顺序表中，查找关键字等于 key 的元素，返回其在表中的位置（从 1 开始编号）；若未找到则输出不存在。

**解题思路**

顺序查找是最基础的查找算法。从表的第一个元素开始，依次将每个元素与目标关键字 key 进行比较：若某元素与 key 相等，则立即返回该元素在表中的位置（1-based）；若遍历完整个表仍未找到匹配元素，则返回 0 表示查找失败。

**算法分析**

- 时间复杂度：O(n)，最坏情况下需遍历整个表
- 空间复杂度：O(1)，仅需常数额外空间

**注意事项**

- 注意题目中表的存储从下标 1 开始，0 号单元留空
- 顺序查找适用于顺序表和链表，对存储结构无特殊要求

**C++ 参考答案**

```cpp
#include <iostream>
#include <vector>
using namespace std;
int main() {
    int n;
    cin >> n;
    vector<int> a(n + 1);
    for (int i = 1; i <= n; i++)
        cin >> a[i];
    int key;
    cin >> key;
    for (int i = 1; i <= n; i++)
        if (a[i] == key) {
            cout << "The element position is " << i << ".";
            return 0;
        }
    cout << "The element is not exist.";
}
```

## 72. 8621 二分查找

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8621&access=9db1e3583h2a8c6843df66447f1bc4dc&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
编写Search_Bin函数，实现在一个递增有序数组ST中采用折半查找法确定元素位置的算法.
```

**输入**

```
第一行:元素个数n
第二行：依次输入n个元素的值（有序）
第三行：输入要查找的关键字key的值
```

**输出**

```
输出分两种情形：
1.如果key值存在，则输出其在表中的位置x(表位置从0开始),格式为The element position is x.
2.如果key值不存在输出："The element is not exist."
```

**样例输入**

```
6
1 3 5 7 9 10
5
```

**样例输出**

```
The element position is 2.
```

**解析**

**题目要求**

在给定的递增有序数组中，采用折半查找（二分查找）算法查找关键字等于 key 的元素，返回其位置（从 0 开始编号）；若未找到则输出不存在。

**解题思路**

二分查找的前提是序列有序。算法维护左右边界 l 和 r，每次取中间位置 mid = (l+r)/2，将中间元素与 key 进行比较：若相等则查找成功；若中间元素小于 key，说明目标只可能在右半部分，令 l = mid+1；若中间元素大于 key，说明目标只可能在左半部分，令 r = mid-1。重复此过程直到找到目标或搜索区间为空。

**算法分析**

- 时间复杂度：O(log n)，每次比较将搜索范围缩小一半
- 空间复杂度：O(1)

**注意事项**

- 本题要求输出位置从 0 开始，与上一题（从 1 开始）不同，需注意下标的转换
- 循环条件为 l <= r，确保当搜索区间缩减为单个元素时仍能被检查到

**C++ 参考答案**

```cpp
#include <iostream>
#include <vector>
using namespace std;
int main() {
    int n;
    cin >> n;
    vector<int> a(n);
    for (int &i : a)
        cin >> i;
    int key;
    cin >> key;
    int l = 0, r = n - 1;
    while (l <= r) {
        int m = (l + r) / 2;
        if (a[m] == key) {
            cout << "The element position is " << m << ".";
            return 0;
        }
        if (a[m] < key)
            l = m + 1;
        else
            r = m - 1;
    }
    cout << "The element is not exist.";
}
```
**邪修做法（可过 OJ）**

递增数组可以直接调用 `lower_bound`。注意题目要求位置从 0 开始。

~~~cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;

int main() {
    int n, key;
    cin >> n;
    vector<int> a(n);
    for (int &x : a)
        cin >> x;
    cin >> key;
    auto it = lower_bound(a.begin(), a.end(), key);
    if (it != a.end() && *it == key)
        cout << "The element position is " << it - a.begin() << ".";
    else
        cout << "The element is not exist.";
}
~~~


## 73. 8622 哈希查找

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8622&access=323c79301bdf2769c711ed8dad827d66&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
使用哈希函数：H(k)=3*k MOD length，并采用开放定址法处理冲突。试对输入的关键字序列构造哈希表，哈希表长度为length，求等概率情况下查找成功的平均查找长度，并设计构造哈希表的完整的算法。本题给出部分代码，请补全Hash函数和解决冲突的collison函数。

#include"malloc.h" /* malloc()等 */
#include"stdlib.h" /* exit() */
#include"stdio.h"
#define EQ(a,b) ((a)==(b))
#define SUCCESS 1
#define UNSUCCESS 0
#define NULLKEY -1 /*哈希表无元素时值为-1*/
typedef int ElemType;
int length;
typedef struct
{
   ElemType *elem; /* 数据元素存储基址，动态分配数组 */
   int count; /* 当前数据元素个数 */
}HashTable;

void InitHashTable(HashTable *H)
 { /* 操作结果: 构造一个长度为length的哈希表,length为全局变量 */
   int i;
   (*H).count=0; /* 当前元素个数为0 */
   (*H).elem=(ElemType*)malloc(length*sizeof(ElemType));
   if(!(*H).elem)
     exit(0); /* 存储分配失败 */
   for(i=0;i<length;i++)
     (*H).elem[i]=NULLKEY; /* 未填记录的标志 */
}
unsigned Hash(ElemType K)
{ /* 一个简单的哈希函数*/

}
void collision(int *p) /*线性探测再散列 */
{ /* 开放定址法处理冲突 */

}
int SearchHash(HashTable H,ElemType K,int *p,int *c)
{  /* 在开放定址哈希表H中查找关键码为K的元素,若查找成功,以p指示待查数据 */
   /* 元素在表中位置,并返回SUCCESS;否则,以p指示插入位置,并返回UNSUCCESS */
   /* c用以计冲突次数，其初值置零，供建表插入时参考。算法9.17 */
   *p=Hash(K); /* 求得哈希地址 */
   while(H.elem[*p]!=NULLKEY&&!EQ(K,H.elem[*p]))
   { /* 该位置中填有记录,并且关键字不相等 */
     (*c)++;
     if(*c<length)
	   collision(p); /* 求得下一探查地址p */
     else
       break;
   }
   if EQ(K,H.elem[*p])
     return SUCCESS; /* 查找成功，p返回待查数据元素位置 */
   else
     return UNSUCCESS; /* 查找不成功(H.elem[p].key==NULLKEY)，p返回的是插入位置 */
}
int InsertHash(HashTable *H,ElemType e)
{ /* 查找不成功时插入数据元素e到开放定址哈希表H中，并返回查找长度 */
   int c,p;
   c=0;
   if(SearchHash(*H,e,&p,&c))   /* 表中已有与e有相同关键字的元素 */
     printf("哈希表中已有元素%d。\n",e);
   else{ /* 插入e */
     (*H).elem[p]=e;
     ++(*H).count;
   }
   return c+1; /*查找长度为冲突次数加1*/
}
void TraverseHash(HashTable H)
 { /* 按哈希地址的顺序打印哈希表，无元素位置用X表示 */
   int i;
   printf("HashTable Address:0～%d\n",length-1);
   for(i=0;i<length;i++)
     if(H.elem[i]==NULLKEY) /* 有数据 */
       printf("X ");
	 else
		 printf("%d ",H.elem[i]);
	 printf("\n");
}
main()
{
	float i=0,j=0;
	ElemType e;
	HashTable H;
         //printf("Input Table length:");
	scanf("%d",&length);
	InitHashTable(&H);
	//printf("Input key words sequence, -1 conclusion input：");
	scanf("%d",&e);
	while(e!=-1)
	{
		j ++;  /*j记录输入元素个数*/
		i = i + InsertHash(&H,e);  /*i记录查找长度的和*/
		scanf("%d",&e);
	}
	TraverseHash(H);
	printf("Average search length=%f\n",i/j);
}
```

**输入**

```
第一行：输入哈希表的长度；
第二行：输入关键字序列，用空格分隔，-1结束(-1不作为关键字)。
```

**输出**

```
第一行：输出哈希表里的数据，未使用的单元用X表示；
第二行：输出平均查找长度,格式为"Average search length="。
```

**样例输入**

```
11
22 41 53 46 30 13 1 67 -1
```

**样例输出**

```
22 X 41 30 1 53 46 13 67 X X
Average search length=2.000000
```

**解析**

**题目要求**

使用指定的哈希函数 H(k) = 3k mod length 构造哈希表，采用开放定址法（线性探测再散列）处理冲突，并计算查找成功时的平均查找长度（ASL）。

**解题思路**

1. **哈希函数**：对关键字 k，计算其初始哈希地址为 (3 * k) % length。
2. **冲突处理**：当哈希地址已被占用且存放的不是目标关键字时，采用线性探测法，依次检查下一个位置 (p+1) % length，直到找到空位或查找成功。
3. **查找长度计算**：每个元素的查找长度等于其插入过程中的冲突次数加 1（即探测次数）。将所有元素的查找长度求和后除以元素总数，即为 ASL。

**算法分析**

- 时间复杂度：平均 O(1)（装填因子较小时），最坏 O(length)
- 空间复杂度：O(length)

**注意事项**

- 哈希函数实现为 `(3 * K) % length`，注意关键字 K 较大时 3*K 可能溢出，建议使用 unsigned 类型
- 线性探测的关键是 `p = (p + 1) % length`，注意对 length 取模以实现循环探测
- 当装填因子接近 1 时，线性探测的冲突次数显著增加，性能急剧下降

**C++ 参考答案**

```cpp
#include <malloc.h> /* malloc()等 */
#include <stdio.h>
#include <stdlib.h> /* exit() */
#define EQ(a, b) ((a) == (b))
#define SUCCESS 1
#define UNSUCCESS 0
#define NULLKEY -1 /* 哈希表无元素时值为-1 */
typedef int ElemType;
int length;
typedef struct {
    ElemType *elem; /* 数据元素存储基址，动态分配数组 */
    int count;      /* 当前数据元素个数 */
} HashTable;

void InitHashTable(HashTable *H) { /* 操作结果: 构造一个长度为length的哈希表,length为全局变量 */
    int i;
    (*H).count = 0;
    (*H).elem = (ElemType *)malloc(length * sizeof(ElemType));
    if (!(*H).elem)
        exit(0);
    for (i = 0; i < length; i++)
        (*H).elem[i] = NULLKEY;
}

unsigned Hash(ElemType K) { /* 一个简单的哈希函数 */
    return (3 * K) % length;
}

void collision(int *p) /* 线性探测再散列 */
{                      /* 开放定址法处理冲突 */
    *p = (*p + 1) % length;
}

int SearchHash(HashTable H, ElemType K, int *p,
               int *c) { /* 在开放定址哈希表H中查找关键码为K的元素 */
    *p = Hash(K);
    while (H.elem[*p] != NULLKEY && !EQ(K, H.elem[*p])) {
        (*c)++;
        if (*c < length)
            collision(p);
        else
            break;
    }
    if EQ (K, H.elem[*p])
        return SUCCESS;
    else
        return UNSUCCESS;
}

int InsertHash(HashTable *H,
               ElemType e) { /* 查找不成功时插入数据元素e到开放定址哈希表H中，并返回查找长度 */
    int c, p;
    c = 0;
    if (SearchHash(*H, e, &p, &c))
        printf("哈希表中已有元素%d。\n", e);
    else {
        (*H).elem[p] = e;
        ++(*H).count;
    }
    return c + 1;
}

void TraverseHash(HashTable H) { /* 按哈希地址的顺序打印哈希表，无元素位置用X表示 */
    int i;
    for (i = 0; i < length; i++)
        if (H.elem[i] == NULLKEY)
            printf("X ");
        else
            printf("%d ", H.elem[i]);
    printf("\n");
}

int main() {
    float i = 0, j = 0;
    ElemType e;
    HashTable H;
    scanf("%d", &length);
    InitHashTable(&H);
    scanf("%d", &e);
    while (e != -1) {
        j++;
        i = i + InsertHash(&H, e);
        scanf("%d", &e);
    }
    TraverseHash(H);
    printf("Average search length=%f\n", i / j);
    return 0;
}
```

## 74. 8608 实现二叉排序树的各种算法(2)

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8608&access=7cb7c1e1cf1cda1e6b9b054f0c6bf51d&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
用函数实现如下二叉排序树算法：
（1） 插入新结点
（2） 前序、中序、后序遍历二叉树
（3） 中序遍历的非递归算法
（4） 层次遍历二叉树
（5） 在二叉树中查找给定关键字(函数返回值为成功1,失败0)
（6） 交换各结点的左右子树
（7） 求二叉树的深度
（8） 叶子结点数
```

**输入**

```
第一行：准备建树的结点个数n
第二行：输入n个整数，用空格分隔
第三行：输入待查找的关键字
第四行：输入待查找的关键字
第五行：输入待插入的关键字
```

**输出**

```
第一行：二叉树的先序遍历序列
第二行：二叉树的中序遍历序列
第三行：二叉树的后序遍历序列
第四行：查找结果
第五行：查找结果
第六行~第八行：插入新结点后的二叉树的先、中、序遍历序列
第九行：插入新结点后的二叉树的中序遍历序列(非递归算法)
第十行：插入新结点后的二叉树的层次遍历序列
第十一行~第十三行：第一次交换各结点的左右子树后的先、中、后序遍历序列
第十五行~第十六行：第二次交换各结点的左右子树后的先、中、后序遍历序列
第十七行：二叉树的深度
第十八行：叶子结点数
```

**样例输入**

```
7
40 20 60 18 50 56 90
18
35
30
```

**样例输出**

```
40 20 18 60 50 56 90
18 20 40 50 56 60 90
18 20 56 50 90 60 40
1
0
40 20 18 30 60 50 56 90
18 20 30 40 50 56 60 90
18 30 20 56 50 90 60 40
18 20 30 40 50 56 60 90
40 20 60 18 30 50 90 56
40 60 90 50 56 20 30 18
90 60 56 50 40 30 20 18
90 56 50 60 30 18 20 40
40 20 18 30 60 50 56 90
18 20 30 40 50 56 60 90
18 30 20 56 50 90 60 40
4
4
```

**解析**

**题目要求**

实现二叉排序树（BST）的一系列基本操作，包括插入、查找、多种遍历方式、交换子树、求深度和统计叶子结点数。

**解题思路**

1. **插入**：从根结点开始，将待插入值与当前结点比较——小于当前结点则进入左子树，大于等于则进入右子树，递归直到找到空位置并创建新结点。
2. **查找**：从根结点开始，将目标值与当前结点比较——等于则查找成功返回 1；小于则递归在左子树中查找；大于则递归在右子树中查找；到达空结点则返回 0。
3. **递归遍历**：前序遍历按"根-左-右"顺序访问，中序遍历按"左-根-右"顺序访问，后序遍历按"左-右-根"顺序访问。
4. **非递归中序遍历**：借助栈实现。从当前结点开始，不断将左子结点压栈直到为空；然后弹出栈顶元素并访问，再转向其右子树，重复此过程。
5. **层次遍历**：借助队列实现广度优先遍历。将根结点入队，每次取出队首元素访问，并将其左右子结点依次入队。
6. **交换左右子树**：递归地交换每个结点的左右子树。
7. **求深度**：采用递归方法，树的深度等于左右子树深度的较大值加 1，空树深度为 0。
8. **叶子结点数**：递归统计，左右子树均不为空的结点计为 1，否则递归统计左右子树的叶子数。

**算法分析**

- 时间复杂度：建树 O(n log n)（平衡时），查找/插入 O(h)（h 为树高），遍历 O(n)，深度/叶子数 O(n)
- 空间复杂度：递归遍历 O(h)，层次遍历 O(n)，非递归中序 O(h)

**注意事项**

- 二叉排序树的中序遍历结果一定是递增有序序列，可用于验证建树的正确性
- 非递归中序遍历的核心是用栈模拟递归调用过程，注意入栈和访问的顺序
- 层次遍历需使用队列（FIFO），不可与栈混淆

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <queue>
#include <stack>
#include <vector>
using namespace std;
struct N {
    int v;
    N *l, *r;
    N(int x) : v(x), l(0), r(0) {}
};
void ins(N *&t, int x) {
    if (!t)
        t = new N(x);
    else if (x < t->v)
        ins(t->l, x);
    else
        ins(t->r, x);
}
bool findx(N *t, int x) {
    return t && (t->v == x || findx(x < t->v ? t->l : t->r, x));
}
void outv(vector<int> v) {
    for (int i = 0; i < v.size(); i++)
        cout << v[i] << (i + 1 == v.size() ? '\n' : ' ');
}
void pre(N *t, vector<int> &v) {
    if (t) {
        v.push_back(t->v);
        pre(t->l, v);
        pre(t->r, v);
    }
}
void in(N *t, vector<int> &v) {
    if (t) {
        in(t->l, v);
        v.push_back(t->v);
        in(t->r, v);
    }
}
void post(N *t, vector<int> &v) {
    if (t) {
        post(t->l, v);
        post(t->r, v);
        v.push_back(t->v);
    }
}
void show(N *t, int tp) {
    vector<int> v;
    if (tp == 0)
        pre(t, v);
    else if (tp == 1)
        in(t, v);
    else
        post(t, v);
    outv(v);
}
void inorder2(N *t) {
    vector<int> v;
    stack<N *> s;
    while (t || !s.empty()) {
        while (t) {
            s.push(t);
            t = t->l;
        }
        t = s.top();
        s.pop();
        v.push_back(t->v);
        t = t->r;
    }
    outv(v);
}
void level(N *t) {
    vector<int> v;
    queue<N *> q;
    if (t)
        q.push(t);
    while (!q.empty()) {
        auto u = q.front();
        q.pop();
        v.push_back(u->v);
        if (u->l)
            q.push(u->l);
        if (u->r)
            q.push(u->r);
    }
    outv(v);
}
void swp(N *t) {
    if (t) {
        swap(t->l, t->r);
        swp(t->l);
        swp(t->r);
    }
}
int dep(N *t) {
    return t ? max(dep(t->l), dep(t->r)) + 1 : 0;
}
int leaf(N *t) {
    return t ? (!t->l && !t->r) + leaf(t->l) + leaf(t->r) : 0;
}
int main() {
    int n, x;
    cin >> n;
    N *root = 0;
    while (n--) {
        cin >> x;
        ins(root, x);
    }
    show(root, 0);
    show(root, 1);
    show(root, 2);
    cin >> x;
    cout << findx(root, x) << "\n";
    cin >> x;
    cout << findx(root, x) << "\n";
    cin >> x;
    ins(root, x);
    show(root, 0);
    show(root, 1);
    show(root, 2);
    inorder2(root);
    level(root);
    swp(root);
    show(root, 0);
    show(root, 1);
    show(root, 2);
    swp(root);
    show(root, 0);
    show(root, 1);
    show(root, 2);
    cout << dep(root) << "\n" << leaf(root) << "\n";
}
```

# 拓展习题5

## 75. 18726 查找最接近的元素

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18726&access=1cad6bcf481f4407b61b005413e01d59&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
已知长度为n的非下降序列。
现在有q个查询，每个查询给出一个指定值。
输出序列中第一个大于等于给定值的元素下标，若不存在这样的元素，输出n+1。
```

**输入**

```
第一行一个整数n，为非降序列长度。1=<n<=100000。
第二行n个整数，为非降序列元素。所有元素的大小均在int范围内。
第三行包含一个整数q，为要询问的给定值个数。1=<q<=100000。
接下来q行，每行一个整数，为要询问最接近元素的给定值。所有给定值的大小均在int范围内。
```

**输出**

```
q行，每行一个整数，第一个大于等于给定值的元素下标，若不存在这样的元素，输出n+1。
```

**样例输入**

```
4
1 3 5 7
2
4
10
```

**样例输出**

```
3
5

Hint

样例说明，大于等于4第3个元素，大于等于10不存在，所以输出5
```

**解析**

**题目要求**

在非降序列中，对每次查询的给定值 x，找到第一个大于等于 x 的元素的下标（从 1 开始编号）；若不存在则输出 n+1。

**解题思路**

由于序列非降（即有序不减），可以直接使用二分查找定位第一个大于等于 x 的元素位置。C++ 标准库中的 `lower_bound` 函数恰好实现此功能：在有序区间 [begin, end) 中查找第一个不小于 x 的元素的迭代器。通过迭代器差值 +1 即可得到 1-based 下标；若不存在这样的元素，`lower_bound` 返回 end 迭代器，对应的下标恰好为 n+1。

**算法分析**

- 时间复杂度：每次查询 O(log n)，共 q 次查询，总计 O(q log n)
- 空间复杂度：O(n)

**注意事项**

- `lower_bound` 返回的是迭代器，转换为下标需减去 `a.begin()`，再加 1 得到 1-based 下标
- 当所有元素均小于 x 时，`lower_bound` 返回 `a.end()`，此时下标自动为 n+1，无需额外判断

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;
int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    int n;
    cin >> n;
    vector<int> a(n);
    for (int &i : a)
        cin >> i;
    int q, x;
    cin >> q;
    while (q--) {
        cin >> x;
        cout << lower_bound(a.begin(), a.end(), x) - a.begin() + 1 << "\n";
    }
}
```

## 76. 18935 贪吃的小Q

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18935&access=c881d8c6f600296826f9cd47b47ad540&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
腾讯2018春招技术类编程题

小Q的父母要出差N天，走之前给小Q留下了M块巧克力。
小Q决定每天吃的巧克力数量不少于前一天吃的一半，但是他又不想在父母回来之前的某一天没有巧克力吃，
请问他第一天最多能吃多少块巧克力？
```

**输入**

```
一行包含两个正整数，表示父母出差的天数N(N<=50000)和巧克力的数量M(N<=M<=100000)
```

**输出**

```
输出一个数表示小Q第一天最多能吃多少块巧克力。
```

**样例输入**

```
3 7
```

**样例输出**

```
4
```

**解析**

**题目要求**

在 N 天内吃完 M 块巧克力，每天吃的数量不少于前一天的一半，求第一天最多能吃多少块。

**解题思路**

设第一天吃 x 块，为使总消耗量最小（从而 x 尽可能大），后续每天应取最少值，即前一天的上取整一半：ceil(x/2)。总消耗量 S(x) = x + ceil(x/2) + ceil(ceil(x/2)/2) + ...，共 N 项。S(x) 是关于 x 的单调递增函数，因此可以对 x 进行二分查找：在 [1, M] 范围内，检验当前 x 对应的最小总消耗是否不超过 M，找到满足条件的最大 x。

**算法分析**

- 时间复杂度：O(n log M)，其中 log M 为二分次数，每次验证需 O(n) 计算总消耗
- 空间复杂度：O(1)

**注意事项**

- 向上取整的计算公式为 `(x + 1) / 2`（整数除法自动向下取整）
- 总消耗量可能超过 int 范围，应使用 long long 类型避免溢出

**C++ 参考答案**

```cpp
#include <iostream>
using namespace std;
long long need(long long x, int n) {
    long long s = 0;
    while (n--) {
        s += x;
        x = (x + 1) / 2;
    }
    return s;
}
int main() {
    int n;
    long long m;
    cin >> n >> m;
    long long l = 1, r = m, ans = 1;
    while (l <= r) {
        long long mid = (l + r) / 2;
        if (need(mid, n) <= m)
            ans = mid, l = mid + 1;
        else
            r = mid - 1;
    }
    cout << ans;
}
```

## 77. 19023 砍树

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19023&access=5fab697df0777ac91b5b3467e2ece416&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
洛谷1873
伐木工人米尔科需要砍倒M米长的木材。这是一个对米尔科来说很容易的工作，因为他有一个漂亮的新伐木机，可以像野火一样砍倒森林。
不过，米尔科只被允许砍倒单行树木。

米尔科的伐木机工作过程如下：米尔科设置一个高度参数H（米），伐木机升起一个巨大的锯片到高度H，
并锯掉所有的树比H高的部分（当然，树木不高于H米的部分保持不变）。米尔科就行到树木被锯下的部分。

例如，如果一行树的高度分别为20，15，10和17，米尔科把锯片升到15米的高度，
切割后树木剩下的高度将是15，15，10和15，而米尔科将从第1棵树得到5米，从第4棵树得到2米，共得到7米木材。

米尔科非常关注生态保护，所以他不会砍掉过多的木材。这正是他为什么尽可能高地设定伐木机锯片的原因。
帮助米尔科找到伐木机锯片的最大的整数高度H，使得他能得到木材至少为M米。换句话说，如果再升高1米，则他将得不到M米木材。
```

**输入**

```
第1行：2个整数N和M，N表示树木的数量（1<=N<=1000000）,M表示需要的木材总长度（1<=M<=2000000000）

第2行：N个整数表示每棵树的高度，值均不超过1000000000。所有木材长度之和大于M，因此必有解。
```

**输出**

```
第1行：1个整数，表示砍树的最高高度。
```

**样例输入**

```
5 20
4 42 40 26 46
```

**样例输出**

```
36
```

**解析**

**题目要求**

找到最大的整数锯片高度 H，使得在高度 H 处切割所获得的木材总量不少于 M 米。

**解题思路**

锯片高度 H 与获得的木材总量之间存在单调关系：H 越低，每棵树被锯掉的部分越多，木材总量越大；H 越高，木材总量越小。这种单调性使得问题适合用二分查找求解。在 [0, 最高树高] 范围内二分 H 的值，对于每个候选高度 mid，计算木材总量 sum = sum(max(0, tree[i] - mid))：若 sum >= M，说明当前高度可行，尝试升高锯片（向更大的 H 搜索）；否则降低锯片高度。

**算法分析**

- 时间复杂度：O(n log(max_h))，其中 max_h 为最高树高
- 空间复杂度：O(n)

**注意事项**

- 木材总量和 M 均可超出 int 范围，需使用 long long 类型
- 二分的初始上界应取所有树高的最大值

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;
int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    int n;
    long long m;
    cin >> n >> m;
    vector<long long> a(n);
    long long hi = 0;
    for (auto &x : a) {
        cin >> x;
        hi = max(hi, x);
    }
    long long l = 0, ans = 0;
    while (l <= hi) {
        long long mid = (l + hi) / 2, sum = 0;
        for (long long x : a)
            if (x > mid)
                sum += x - mid;
        if (sum >= m)
            ans = mid, l = mid + 1;
        else
            hi = mid - 1;
    }
    cout << ans;
}
```

## 78. 18725 宇宙迁跃

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18725&access=6a30e0693559f4a973e1fbe1767f41a8&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
在基地的科学家发明"透镜"之后，宇宙航行变得更加效率。
作为基地元首的的代理人，你需要在K天内乘坐飞船到达首都川陀。
飞船可以花费一天时间，通过迁跃从一个星系到达另一个星系，但绝不能迁跃到星系之间，那样不但会遇到一些自然危险，也可能永远迷失。
我们把基地至川陀间星系的坐标看成是一个线性序列，例如a星系坐标是10，b星系坐标是15，那么飞船必须具备不小于5的迁跃能力才能从a航行至b。
基地坐标为0，请你根据基地至川陀间的N个星系坐标，计算飞船的迁跃能力至少为多大，才能在K天内（包含K天）到达川陀。
```

**输入**

```
第一行两个整数N和K。（1=<N<=10000，1=<K<=10000）
第二行N个整数，表示N个星系的坐标ai，题目确保坐标由小到大排列。（0=<ai<=100000）
```

**输出**

```
仅一行,飞船的最小迁跃能力。
```

**样例输入**

```
5 2
1 4 6 10 19
```

**样例输出**

```
10

Hint

样例说明：川陀的坐标为最后一个值19。
飞船的迁跃能力至少为10，才能在2天内到达川陀。
```

**解析**

**题目要求**

给定基地（坐标 0）到川陀之间 N 个有序排列的星系坐标，求飞船的最小迁跃能力 d，使得能在 K 天内从基地到达川陀（最后一个星系）。

**解题思路**

迁跃能力 d 与所需天数之间存在单调关系：d 越大，每天能跨越的距离越远，所需天数越少。因此可以对迁跃能力 d 进行二分查找，并用贪心策略验证。对于给定的 d，从基地出发，每次都跳到当前可达范围内最远的星系（贪心），统计到达川陀所需的天数。若天数不超过 K，则说明 d 可行，尝试缩小 d；否则增大 d。

**算法分析**

- 时间复杂度：O(n log(max_coord))，其中 max_coord 为最远星系坐标
- 空间复杂度：O(n)

**注意事项**

- 星系坐标序列包含基地（坐标 0），完整路径为 0 -> a[1] -> a[2] -> ... -> a[N]
- 贪心验证时，若从当前位置无法前进到任何下一个星系（距离均超过 d），则该 d 值不可行
- 二分的上界可取最后一个星系的坐标值

**C++ 参考答案**

```cpp
#include <iostream>
#include <vector>
using namespace std;
int main() {
    int n, k;
    cin >> n >> k;
    vector<int> a(n + 1);
    a[0] = 0;
    for (int i = 1; i <= n; i++)
        cin >> a[i];
    auto ok = [&](int d) {
        int days = 0, pos = 0;
        while (pos < n) {
            int nxt = pos;
            while (nxt + 1 <= n && a[nxt + 1] - a[pos] <= d)
                nxt++;
            if (nxt == pos)
                return false;
            pos = nxt;
            days++;
        }
        return days <= k;
    };
    int l = 0, r = a[n], ans = r;
    while (l <= r) {
        int m = (l + r) / 2;
        if (ok(m))
            ans = m, r = m - 1;
        else
            l = m + 1;
    }
    cout << ans;
}
```

## 79. 19050 牛牛打气球

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19050&access=62b63461de91ac999761c0bcb73e4d29&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
贝壳找房2021届校招算法卷3

有n个气球，每个气球都有一个坚韧度，牛牛有一把全屏武器，可以使每一个气球的坚韧度都下降b（坚韧度不会为负数），

特别的：每次释放武器的时候，牛牛可以选择一个气球，使得这个气球多承受a点伤害。

牛牛想知道，最少释放几次武器，可以使得所有气球的坚韧度都变成0呢？
```

**输入**

```
第一行三个整数n,a,b。
第二行n个空格隔开的整数，第个数表示第i个气球的坚韧度。
n<=500000,其余所有整数都在[1,10^9]范围内。
```

**输出**

```
一个整数表示答案。
```

**样例输入**

```
3 1 2
1 4 5
```

**样例输出**

```
2

Hint

第一次释放选择对第三个气球多承受1点伤害，三个气球的坚韧度变成：0 2 2 。第二次释放后所有气球的坚韧度都为0。
注意观察数据范围，这类问题在进行计算时，很容易会超过int范围，所以尽量采用long long类型来存储和计算。
```

**解析**

**题目要求**

每次释放武器对所有气球造成 b 点伤害，同时可选择一个气球额外造成 a 点伤害。求使所有气球坚韧度归零的最少释放次数。

**解题思路**

设释放武器 t 次，则每个气球受到的基础伤害为 b * t。对于坚韧度为 h[i] 的气球，若 b * t >= h[i]，则基础伤害已足够将其击破；否则剩余坚韧度 rem = h[i] - b * t 需要通过额外伤害 a 来补足，该气球需要的额外次数为 ceil(rem / a)。将所有气球所需的额外次数累加，若总和不超过 t（因为每次释放武器至多提供一次额外伤害），则 t 次释放足够。由于可行性关于 t 具有单调性（t 越大越容易满足），可对 t 进行二分查找。二分上界可通过倍增法确定：从 r = 1 开始，若 r 不可行则将 r 翻倍，直到找到可行的上界。

**算法分析**

- 时间复杂度：O(n log T)，其中 T 为答案的上界
- 空间复杂度：O(n)

**注意事项**

- 当 a = 0 时无法通过额外伤害补足，此时若 b * t < h[i] 则该 t 不可行
- 数据范围较大，坚韧度和伤害值均可达 10^9，计算过程中应使用 long long 类型防止溢出
- 验证函数中，若累加的额外次数已超过 t，可提前返回 false 以优化效率

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;
int main() {
    int n;
    long long a, b;
    cin >> n >> a >> b;
    vector<long long> h(n);
    for (auto &x : h)
        cin >> x;
    auto ok = [&](long long t) {
        long long need = 0, extra = max(0LL, a);
        for (long long x : h) {
            long long rem = x - b * t;
            if (rem > 0) {
                if (extra == 0)
                    return false;
                need += (rem + extra - 1) / extra;
                if (need > t)
                    return false;
            }
        }
        return need <= t;
    };
    long long l = 0, r = 1;
    while (!ok(r))
        r *= 2;
    while (l <= r) {
        long long m = (l + r) / 2;
        if (ok(m))
            r = m - 1;
        else
            l = m + 1;
    }
    cout << l;
}
```

## 80. 18730 涂色问题

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18730&access=dfabde8cf9a07f7051988c18d71feefd&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
在某大学的农场里，n间牛舍住着n头奶牛。现在你需要为n间牛舍的外墙涂色，有m种可选颜色。
我们已经知道当相邻两间牛舍颜色相同时，奶牛们会集体发疯。
请问有多少种涂色方案会让奶牛们发疯，由于答案可能较大，输出对1000000007求余的结果。
```

**输入**

```
仅一行，两个整数n和m，代表牛舍数量和颜色数量。(1<=n<=1e12),(1<=m<=1e12)
```

**输出**

```
仅一样，一个整数代表答案。
```

**样例输入**

```
3 2
```

**样例输出**

```
6

Hint

3牛舍2颜色方案有(1,1,1),（1,1,2）,（1,2,2）,（2,1,1）,（2,2,1),(2,2,2)，共6种方案会让奶牛发疯。
```

**解析**

**题目要求**

求 n 间牛舍使用 m 种颜色涂色时，至少有一对相邻牛舍颜色相同的方案数，结果对 10^9+7 取模。

**解题思路**

本题采用补集思想求解。总涂色方案数为 m^n（每间牛舍独立选择 m 种颜色之一）。"不发疯"的方案（即所有相邻牛舍颜色均不相同）数为 m * (m-1)^(n-1)：第一间牛舍有 m 种选择，之后每间牛舍只需与前一间不同，各有 m-1 种选择。因此，"发疯"的方案数 = 总方案数 - 合法方案数 = m^n - m * (m-1)^(n-1)。由于 n 和 m 可达 10^12，需使用快速幂算法在 O(log n) 时间内计算幂次，并在运算过程中对 MOD = 10^9+7 取模。做减法时需注意防止负数：(total - good + MOD) % MOD。

**算法分析**

- 时间复杂度：O(log n)，快速幂计算
- 空间复杂度：O(1)

**注意事项**

- 所有中间运算均应对 MOD 取模，防止溢出
- 减法取模的正确写法：`(total - good % MOD + MOD) % MOD`，确保结果非负
- n = 1 时，(m-1)^0 = 1，合法方案数为 m，发疯方案数为 0，公式仍然成立

**C++ 参考答案**

```cpp
#include <iostream>
using namespace std;
const long long MOD = 1000000007;
long long modpow(long long a, long long e) {
    long long r = 1 % MOD;
    for (a %= MOD; e; e >>= 1, a = a * a % MOD)
        if (e & 1)
            r = r * a % MOD;
    return r;
}
int main() {
    long long n, m;
    cin >> n >> m;
    long long total = modpow(m, n);
    long long good = (m % MOD) * modpow(m - 1, n - 1) % MOD;
    cout << (total - good + MOD) % MOD;
}
```

## 81. 18727 数对问题一

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18727&access=492da4b64e44304a7b31482aaa917f61&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
一个长度为N的正整数序列，现在需要计算出有多少对数字的差的绝对值为C。
注意只要位置不同就认为是不相同的数对。
```

**输入**

```
第一行，两个整数 N, C。（1=<N<=10000）,（1=<C<=10000）
第二行，N个正整数a1....an。 （1=<ai<=10000）
```

**输出**

```
仅一行，满足条件的数对的个数。
```

**样例输入**

```
4 1
1 2 3 1
```

**样例输出**

```
3

Hint

(a1,a2),(a2,a3),(a2,a4)共3个数对满足条件。
```

**解析**

**题目要求**

统计序列中差的绝对值为 C 的数对个数，位置不同的相同值视为不同数对。

**解题思路**

由于题目中元素值域较小（ai <= 10000），可以使用计数数组 cnt 统计每个值出现的次数。对于差为 C 的数对 (x, x+C)，其组合数为 cnt[x] * cnt[x+C]。遍历所有可能的 x 值，将 cnt[x] * cnt[x+C] 累加即可得到答案。

**算法分析**

- 时间复杂度：O(n + V)，其中 V 为值域上界（本题 V = 10000）
- 空间复杂度：O(V)

**注意事项**

- 计数数组的大小应覆盖值域范围，本题中 x + C 的最大值可达 20000，数组应相应开大
- 结果可能超出 int 范围，应使用 long long 类型累加

**C++ 参考答案**

```cpp
#include <iostream>
#include <vector>
using namespace std;
int main() {
    int n, c;
    cin >> n >> c;
    vector<long long> cnt(20005);
    for (int i = 0, x; i < n; i++) {
        cin >> x;
        cnt[x]++;
    }
    long long ans = 0;
    for (int i = 0; i + c < (int)cnt.size(); i++)
        ans += cnt[i] * cnt[i + c];
    cout << ans;
}
```

## 82. 18728 数对问题二

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18728&access=4625db26f7b5ca86ebcc4454e7550a81&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
此题目与数对问题一的唯一区别为序列中元素的取值范围。
一个长度为N的正整数序列，现在需要计算出有多少对数字的差的绝对值为C。
注意只要位置不同就认为是不相同的数对。
```

**输入**

```
第一行，两个整数 N, C。（1=<N<=10000）,（1=<C<=10000）
第二行，N个正整数a1....an。 ai为int范围内的正整数。
```

**输出**

```
仅一行，满足条件的数对的个数。
```

**样例输入**

```
4 1
1 2 3 1
```

**样例输出**

```
3

Hint

(a1,a2),(a2,a3),(a2,a4)共3个数对满足条件。
```

**解析**

**题目要求**

与数对问题一相同，统计差的绝对值为 C 的数对个数，但元素值域扩大到 int 范围，无法使用计数数组。

**解题思路**

由于值域扩大，计数数组不再可行，改用 `map` 统计每个值出现的次数。遍历每个键值对 (v, cnt)，检查 v + C 是否也存在：若存在，则贡献 cnt * mp[v+C] 对数对。

**算法分析**

- 时间复杂度：O(n)（哈希表操作平均 O(1)）
- 空间复杂度：O(n)

**注意事项**

- 哈希表遍历的是键值对，需使用 `mp.count(v + C)` 或 `mp.find(v + C)` 检查目标键是否存在
- 结果应使用 long long 类型，防止累加时溢出

**C++ 参考答案**

```cpp
#include <iostream>
#include <map>
using namespace std;
int main() {
    int n;
    long long c, x;
    cin >> n >> c;
    map<long long, long long> mp;
    for (int i = 0; i < n; i++) {
        cin >> x;
        mp[x]++;
    }
    long long ans = 0;
    for (auto [v, cnt] : mp)
        if (mp.count(v + c))
            ans += cnt * mp[v + c];
    cout << ans;
}
```

## 83. 19145 最长无重复子数组

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19145&access=74ef2e59a33f9b0d938997cc6ae32dab&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
给定一个长度为n的数组arr，返回arr的最长无重复元素子数组的长度，无重复指的是所有数字都不相同。
子数组是连续的，比如[1,3,5,7,9]的子数组有[1,3]，[3,5,7]等等，但是[1,3,7]不是子数组（是子序列）。
```

**输入**

```
第一行一个整数n表示数组的长度，n<=100000。
第二行n个整数,int范围。
```

**输出**

```
输出最长无重复元素子数组长度。
```

**样例输入**

```
7
2 2 3 4 89 9 3
```

**样例输出**

```
5

Hint

最长不重复子数组为2 3 4 89 9
```

**解析**

**题目要求**

求数组中最长无重复元素的连续子数组的长度。

**解题思路**

使用滑动窗口（双指针）维护一个不含重复元素的连续区间 [l, r]。用哈希表记录每个元素最后一次出现的位置。右端点 r 逐步右移扩展窗口；若新加入的元素 x 上次出现的位置 last[x] 在当前窗口内（即 last[x] >= l），则将左端点 l 移至 last[x] + 1，以排除重复元素。每步更新窗口长度的最大值 ans = max(ans, r - l + 1)。

**算法分析**

- 时间复杂度：O(n)，每个元素被右端点访问一次
- 空间复杂度：O(n)，哈希表存储元素位置

**注意事项**

- 判断重复元素是否在窗口内的条件是 `last[x] >= l`，而非简单的 `last[x] > 0`
- 左端点只能右移不能左移，保证滑动窗口的单调性

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <map>
using namespace std;
int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    int n;
    cin >> n;
    map<long long, int> last;
    int l = 1, ans = 0;
    for (int r = 1; r <= n; r++) {
        long long x;
        cin >> x;
        if (last[x] >= l)
            l = last[x] + 1;
        last[x] = r;
        ans = max(ans, r - l + 1);
    }
    cout << ans;
}
```

## 84. 18731 最接近的值

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18731&access=ee30ed287cc9c50969bcfd8190e038a6&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
查找特定的值是一种常见的操作，当数据量较大时，往往需要使用高效的结构和查找算法。
n个整数组成的序列，请输出所有元素左侧与它值最为接近的值，我们定义"最接近"为两数之差的绝对值最小。
例如序列 5 1 4 2，1最接近值为5，4最接近值为5,2最接近值为1。
特别的，第一个数的最接近值为它自身。
如果一个数左侧有两个不同的值，绝对值差都是最小。例如3的左边出现了1和5，我们认为值较大的5为最接近值
```

**输入**

```
第一行一个整数n。(1<=n<=100000)
第二行n个整数，均为int范围。
```

**输出**

```
一行，n个整数，为输入序列对应元素的最接近值。
```

**样例输入**

```
4
5 1 4 2
```

**样例输出**

```
5 5 5 1
```

**解析**

**题目要求**

对序列中的每个元素，找到其左侧所有元素中与其差值绝对值最小的元素；若存在两个候选值差值相同，取较大者。

**解题思路**

使用有序多重集合（`multiset`）动态维护当前元素左侧的所有已处理元素。对于当前元素 x，利用 `lower_bound(x)` 找到集合中第一个大于等于 x 的元素。最接近值的候选者只可能是该元素（>= x 的最小值）及其前驱（< x 的最大值），分别计算二者与 x 的差值绝对值，取较小者；若差值相同，根据题目要求取较大值（即 >= x 的那个候选）。

**算法分析**

- 时间复杂度：O(n log n)，每次插入和查找均为 O(log n)
- 空间复杂度：O(n)

**注意事项**

- 第一个元素没有左侧元素，其最接近值规定为自身
- 需处理迭代器的边界情况：当 `lower_bound` 返回 `begin()` 时，说明集合中所有元素均 >= x，只取当前迭代器所指元素；当返回 `end()` 时，只取前驱元素
- 使用 `multiset` 而非 `set`，以正确处理重复元素

**C++ 参考答案**

```cpp
#include <algorithm>
#include <cstdlib>
#include <iostream>
#include <set>
using namespace std;
int main() {
    int n;
    cin >> n;
    multiset<long long> s;
    for (int i = 0; i < n; i++) {
        long long x;
        cin >> x;
        if (i == 0) {
            cout << x;
            s.insert(x);
            continue;
        }
        auto it = s.lower_bound(x);
        long long best;
        if (it == s.begin())
            best = *it;
        else if (it == s.end()) {
            auto pre = it;
            --pre;
            best = *pre;
        } else {
            auto pre = it;
            --pre;
            long long a = *pre, b = *it;
            best = (llabs(x - b) <= llabs(x - a) ? b : a);
        }
        cout << ' ' << best;
        s.insert(x);
    }
}
```

## 85. 18870 最佳搭配

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18870&access=ab163d077074143de6316c0237fb763d&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
两个长度为n的一维数组A和B，数组中元素值均在0至n-1之间。

现在我们保持A数组次序不变，在B数组中选取合适的元素与A数组中的元素相加后对n求余（即a[i]=(a[i]+b[j])%n），我们希望最后A数组的字典序最小。

注意B数组中的每个元素只能选取一次。
```

**输入**

```
第一行一个整数n。(1<=n<=100000)

第二行数组A的n个元素。

第三行数组B的n个元素。（A和B的元素值均在0至n-1之间）
```

**输出**

```
一行，n个整数，计算后字典序最小的数组A。
```

**样例输入**

```
4
0 1 2 1
3 2 1 1
```

**样例输出**

```
1 0 0 2

Hint

样例1说明，要想字典序最小，数组A的第一个元素0只能选择B中的1，第二个元素1选择B中的3，（1+3）%4==0，第三个2选择2，第四个1选择1。
```

**解析**

**题目要求**

将数组 B 中的元素一一分配给数组 A 的元素，使得 (A[i] + B[j]) mod n 的结果数组字典序最小，每个 B 元素只能使用一次。

**解题思路**

字典序最小要求高位（靠前的位置）尽可能小，因此采用贪心策略，从前往后依次为 A[i] 选择最优的 B 元素。为使 (A[i] + b) mod n 最小，应优先选择 B 中不小于 (n - A[i]) mod n 的最小元素 b，这样 (A[i] + b) mod n 的结果为 0 或尽量接近 0；若不存在这样的元素（所有可用元素均小于目标值），则选择 B 中当前最小的元素，使模运算结果尽量小。使用 `multiset` 维护 B 中可用元素，通过 `lower_bound` 快速定位目标元素，选取后将其从集合中删除。

**算法分析**

- 时间复杂度：O(n log n)，每次 multiset 操作为 O(log n)
- 空间复杂度：O(n)

**注意事项**

- 贪心策略的正确性依赖于字典序的性质：高位优先取最小值一定优于低位取更优值
- 目标值的计算为 `(n - A[i]) % n`，注意取模运算确保 A[i] = 0 时目标值为 0

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <set>
#include <vector>
using namespace std;
int main() {
    int n;
    cin >> n;
    vector<int> A(n), B(n);
    multiset<int> S;
    for (int &i : A)
        cin >> i;
    for (int i = 0, x; i < n; i++) {
        cin >> x;
        S.insert(x);
    }
    for (int i = 0; i < n; i++) {
        auto it = S.lower_bound((n - A[i]) % n);
        if (it == S.end())
            it = S.begin();
        int v = (A[i] + *it) % n;
        S.erase(it);
        cout << v << (i + 1 == n ? '\n' : ' ');
    }
}
```

## 86. 19066 第K小子串

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19066&access=5b8b13a89d7dcf04d5e9c0158a9d8b24&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
腾讯2021校园招聘技术类编程题

输入一个字符串 s，s 由小写英文字母组成，保证 s 长度小于等于 5000 并且大于等于 1。
在 s 的所有不同的子串中，输出字典序第 k 小的字符串。
字符串中任意个连续的字符组成的子序列称为该字符串的子串。
字母序表示英文单词在字典中的先后顺序，即先比较第一个字母，若第一个字母相同，
则比较第二个字母的字典序，依次类推，则可比较出该字符串的字典序大小。
```

**输入**

```
第一行输入一个字符串 s，保证 s 长度小于等于 5000 大于等于 1。
第二行输入一个整数 k (1<= k <= 5)，保证 s 不同子串个数大于等于 k。
```

**输出**

```
输出一个字符串表示答案
```

**样例输入**

```
aabb
3
```

**样例输出**

```
aab

Hint

不同的子串依次为：a aa aab aabb ab abb b bb 所以答案为aab
数组中第k小问题（也叫前k小问题）是经典问题，一般都建议用堆解决（priority_queue就是堆的实现）。
此题目如果构造出所有子串再排序，在空间复杂度上不可行。使用set，priority_queue等查找结构是解决此类问题的常见方案。
但由于此题目不需要重复的子串，可以考虑用set维护一个长度为k的最小子串集合，通过比较和替换解决问题。
```

**解析**

**题目要求**

在字符串 s 的所有不同子串中，找到字典序第 k 小的子串。

**解题思路**

由于 k 的值很小（k <= 5），第 k 小的不同子串长度必然不超过 k（因为仅长度为 1 的不同子串最多有 26 个，已远超 k 的上界）。因此只需枚举所有长度不超过 k（即 5）的子串，将它们插入 `set` 中（自动去重并按字典序排列），然后取第 k 个元素即可。对于长度 n = 5000 的字符串，长度不超过 5 的子串总数约为 5n = 25000，集合操作完全可行。

**算法分析**

- 时间复杂度：O(n * k^2 * log(n*k))，其中 k 为子串最大长度
- 空间复杂度：O(n * k^2)

**注意事项**

- 本题的关键观察是 k 很小这一约束条件，它使得枚举短子串成为可行方案
- `set` 自动去重和排序，无需手动处理重复子串
- 用循环将迭代器前进 k-1 步，以获取第 k 个元素

**C++ 参考答案**

```cpp
#include <iostream>
#include <set>
#include <string>
using namespace std;
int main() {
    string s;
    int k;
    cin >> s >> k;
    set<string> st;
    int n = s.size();
    for (int i = 0; i < n; i++)
        for (int len = 1; len <= 5 && i + len <= n; len++)
            st.insert(s.substr(i, len));
    auto it = st.begin();
    for (int i = 1; i < k; i++)
        ++it;
    cout << *it;
}
```

## 87. 18907 雪花 雪 雪花（哈希法）

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18907&access=3bc7523056e0d5e09daf0e413e9ebbab&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
题目来自POJ3349
有N片雪花，每片雪花由六个角组成，每个角都有长度。

第i片雪花六个角的长度从某个角开始顺时针依次记为ai,1,ai,2,…,ai,6。

因为雪花的形状是封闭的环形，所以从任何一个角开始顺时针或逆时针往后记录长度，得到的六元组都代表形状相同的雪花。

例如1,2,3,4,5,6和3,4,5,6,1,2就是形状相同的雪花。

1,2,3,4,5,6和6,5,4,3,2,1也是形状相同的雪花。

我们称两片雪花形状相同，当且仅当它们各自从某一角开始顺时针或逆时针记录长度，能得到两个相同的六元组。

求这N片雪花中是否存在两片形状相同的雪花。
```

**输入**

```
第一行输入一个整数N，代表雪花的数量。1≤N≤100000

接下来N行，每行描述一片雪花。

每行包含6个整数，分别代表雪花的六个角的长度（这六个数即为从雪花的随机一个角顺时针或逆时针记录长度得到）。

同行数值之间，用空格隔开。0≤aij<10000000
```

**输出**

```
如果不存在两片形状相同的雪花，则输出：

No two snowflakes are alike.

如果存在两片形状相同的雪花，则输出：

Twin snowflakes found.
```

**样例输入**

```
2
1 2 3 4 5 6
4 3 2 1 6 5
```

**样例输出**

```
Twin snowflakes found.
```

**解析**

**题目要求**

判断 N 片雪花中是否存在形状相同的两片。雪花为环形结构，从任意角开始顺时针或逆时针记录均视为相同形状。

**解题思路**

每片雪花有 6 个角，由于是环形结构，共有 6 种顺时针旋转表示和 6 种逆时针旋转表示，合计 12 种等价表示。为统一比较，将每片雪花所有 12 种表示中字典序最小的六元组作为其"规范表示"（canonical form）。具体步骤为：对原始序列和逆序序列分别枚举 6 种旋转，取其中字典序最小的作为唯一标识。将每片雪花的规范表示转化为字符串后存入 `set`，若插入时发现集合中已存在相同的规范表示，则判定存在形状相同的雪花。

**算法分析**

- 时间复杂度：O(N)，每片雪花生成规范表示为 O(1)（6 个元素，常数操作）
- 空间复杂度：O(N)

**注意事项**

- 环形结构的旋转比较必须枚举所有 6 个起点位置，不可遗漏
- 规范化处理确保同构雪花产生相同的标识字符串，从而可通过哈希集合查重
- 将六元组转化为字符串时，元素间需添加分隔符（如逗号），避免不同六元组拼接出相同字符串

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <set>
#include <string>
#include <vector>
using namespace std;
string canon(vector<int> a) {
    vector<int> b = a;
    reverse(b.begin(), b.end());
    vector<int> best(6, 2147483647);
    for (int r = 0; r < 6; r++) {
        vector<int> c;
        for (int i = 0; i < 6; i++)
            c.push_back(a[(r + i) % 6]);
        best = min(best, c);
        c.clear();
        for (int i = 0; i < 6; i++)
            c.push_back(b[(r + i) % 6]);
        best = min(best, c);
    }
    string s;
    for (int x : best)
        s += to_string(x) + ",";
    return s;
}
int main() {
    int n;
    cin >> n;
    set<string> st;
    for (int i = 0; i < n; i++) {
        vector<int> a(6);
        for (int &x : a)
            cin >> x;
        string c = canon(a);
        if (st.count(c)) {
            cout << "Twin snowflakes found.";
            return 0;
        }
        st.insert(c);
    }
    cout << "No two snowflakes are alike.";
}
```

## 88. 18908 字符串哈希

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18908&access=d87d02a03f0e40b0966958530fff4bf5&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
（1）这一段是乱七八糟的教学模块，看不清楚就百度吧。
字符串哈希可以用于快速比较两个字符串是否相等，或者快速找到子串t在主串s中的位置（模式匹配）。
在完成预处理之后，比较任意两个字符串相等的复杂度O（1）。模式匹配的复杂度和kmp算法接近，为O（n+m）。
那么如何为字符串设计哈希函数呢？
最简单的方法：把字符串直接映射为整数比如abcd看成1234，ccbb看成是3322，考虑到字符串的长度，这样的哈希函数显然不可行。
在前一种设计的基础上，一种容易想到的哈希法是求和，比如f(abcd)=1+2+3+4=10,f(ccbb)=3+3+2+2=10。但这样设计哈希函数非常容易冲突。
通用的方法，取一固定值P，把字符串看作P进制数，并分配一个大于0的数值，代表每种字符。
一般来说，我们分配的数值都远小于P。例如，对于小写字母构成的字符串，可以令a = 1 , b = 2 , . . . , z = 26 。 取一固定值M，求出该P进制数对M的余数，作为该字符串的Hash值。
这样f(abcd)=1*p^3+2*p2+3*p+4,f(ccbb)=3*p^3+3*p2+2*p+2。这种方法如果两个字符串不相同，他们的哈希值相同的概率极小。
当然，这样的哈希函数，应该很容易就会超过int范围。
此处的技巧是，如果我们不给定余数M的话，超过2^32的部分因为超过了int范围，会自动舍掉（相当于对2^32取余）.

稳妥起见，字符串哈希一般采用unsigned long long 类型。
在比较多个字符串是否存在两个相等字符串时，可以采用上述方法求出每个字符串的哈希值，再看看是否有相同值。
在作子串处理或模式匹配问题时，我们需要快速找到子串的哈希值，一般是采用数组的方式来处理。
在字符串哈希数组里，通过一个简单的公式计算就能得到子串的哈希值。

（2）这一段是题目。

给定一个长度不超过100000的字符串，只包含小写字母。
然后有m个查询，每次给定两个区间，判断这两个区间的字符串是否相等。
```

**输入**

```
第一行输入一个 字符串 S。
第二行一个整数m，表示 m 次询问。(1<=m<=100000)
接下来 m 行，每行四个数字 l1,r1,l2,r2，分别表示此次询问的两个区间，注意字符串的位置从1开始编号。
```

**输出**

```
对于每次询问，都输出一行结果，相同输出Yes,不相同输出No。
```

**样例输入**

```
aabbaabb
3
1 3 5 7
1 3 6 8
1 2 1 2
```

**样例输出**

```
Yes
No
Yes
```

**解析**

**题目要求**

给定字符串和多次区间查询，每次判断两个指定区间的子串是否相等。

**解题思路**

使用字符串哈希的前缀和技术。预处理两个数组：前缀哈希数组 h[] 和基数幂次数组 pw[]。其中 h[i] = h[i-1] * P + val(s[i])，pw[i] = pw[i-1] * P。任意子串 s[l..r] 的哈希值可通过公式在 O(1) 时间内计算：hash(l, r) = h[r] - h[l-1] * pw[r-l+1]。对于每次查询，先比较两个区间长度是否相同，再比较哈希值是否相等，两者同时满足则子串相同。选用 `unsigned long long` 类型可利用其自然溢出特性（等价于对 2^64 取模），避免手动取模运算。

**算法分析**

- 时间复杂度：预处理 O(n)，每次查询 O(1)，总计 O(n + m)
- 空间复杂度：O(n)

**注意事项**

- 基数 P 通常取 131 或 13331 等较大的质数，以降低哈希冲突概率
- pw[] 数组必须预处理，否则无法在 O(1) 时间内计算子串哈希值
- 两个区间长度不同则子串必然不同，应先判断长度再做哈希比较

**C++ 参考答案**

```cpp
#include <iostream>
#include <string>
#include <vector>
using namespace std;
using ull = unsigned long long;
int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    string s;
    cin >> s;
    int n = s.size();
    const ull P = 131;
    vector<ull> h(n + 1), pw(n + 1, 1);
    for (int i = 1; i <= n; i++) {
        h[i] = h[i - 1] * P + (s[i - 1] - 'a' + 1);
        pw[i] = pw[i - 1] * P;
    }
    auto get = [&](int l, int r) { return h[r] - h[l - 1] * pw[r - l + 1]; };
    int m;
    cin >> m;
    while (m--) {
        int l1, r1, l2, r2;
        cin >> l1 >> r1 >> l2 >> r2;
        cout << (r1 - l1 == r2 - l2 && get(l1, r1) == get(l2, r2) ? "Yes" : "No") << "\n";
    }
}
```

## 89. 18922 最长回文子串

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18922&access=4f7a1ba209d20ceb4d0d86047691da31&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
一个字符串正着读和倒着读是一样的，则称回文串。
给定一个长度为字符串S，求其最长回文子串的长度。
```

**输入**

```
输入一个字符串S，均为小写字符，长度最多1000000个小写字符。
```

**输出**

```
输出最长回文子串的长度。
```

**样例输入**

```
abcbabcbabcba
```

**样例输出**

```
13

Hint

最长回文子串有多种求法，本题目使用暴力或dp法会超时，建议使用字符串哈希+二分的方法。
```

**解析**

**题目要求**

求给定字符串中最长回文子串的长度。字符串长度可达 10^6，要求使用高效算法。

**解题思路**

Manacher 算法可在 O(n) 时间内求解最长回文子串。其核心思想是利用已知回文的信息来避免重复比较。具体步骤如下：

1. **预处理**：在原串每个字符之间及首尾插入特殊分隔符（如 #），将奇偶长度的回文统一转化为奇数长度的回文。例如 "abc" 变为 "^#a#b#c#$"（首尾加入不同哨兵字符以避免越界判断）。
2. **维护最右回文边界**：设 c 为当前已知最右回文的中心，r 为其右边界。对每个位置 i，找到其关于 c 的对称点 mir = 2c - i。
3. **利用对称性初始化回文半径**：若 i < r，则 p[i] 的初始值可取 min(r - i, p[mir])（已知部分的回文半径）。
4. **中心扩展**：从 p[i] 开始继续向两侧扩展，直到不再满足回文条件。
5. **更新最右边界**：若 i + p[i] > r，则更新 c = i，r = i + p[i]。

最终，p[] 数组中的最大值即为原串最长回文子串的长度。

**算法分析**

- 时间复杂度：O(n)，每个字符最多被扩展一次
- 空间复杂度：O(n)

**注意事项**

- 插入分隔符后，原串长度 n 变为 2n+3，需据此分配数组空间
- p[i] 的值直接对应原串中以该位置为中心的回文长度，无需额外换算
- 首尾哨兵字符（如 ^ 和 $）用于避免扩展时的越界检查

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <string>
#include <vector>
using namespace std;
int main() {
    string s;
    cin >> s;
    string t = "^";
    for (char c : s) {
        t += "#";
        t += c;
    }
    t += "#";
    t += "$";
    vector<int> p(t.size());
    int c = 0, r = 0, ans = 0;
    for (int i = 1; i + 1 < t.size(); i++) {
        int mir = 2 * c - i;
        if (i < r)
            p[i] = min(r - i, p[mir]);
        while (t[i + 1 + p[i]] == t[i - 1 - p[i]])
            p[i]++;
        if (i + p[i] > r)
            c = i, r = i + p[i];
        ans = max(ans, p[i]);
    }
    cout << ans;
}
```

## 90. 18944 小美的仓库整理

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18944&access=9653edb06dab71f65be5bd6805668239&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
美团2021校招笔试-编程题(通用编程试题,第3场)
小美是美团仓库的管理员，她会根据单据的要求按顺序取出仓库中的货物，每取出一件货物后会把剩余货物重新堆放，使得自己方便查找。
已知货物入库的时候是按顺序堆放在一起的。如果小美取出其中一件货物，则会把货物所在的一堆物品以取出的货物为界分成两堆，这样可以保证货物局部的顺序不变。
已知货物最初是按1~n的顺序堆放的，每件货物的重量为w_i,小美会根据单据依次不放回的取出货物。
请问根据上述操作，小美每取出一件货物之后，重量和最大的一堆货物重量是多少？
```

**输入**

```
输入第一行包含一个正整数n，表示货物的数量。(1<=n,m<=50000)

输入第二行包含n个正整数，表示1~n号货物的重量w_i。(1<=w_i<=100)

输入第三行有n个数，表示小美按顺序取出的货物的编号，也就是一个1~n的全排列。
```

**输出**

```
输出包含n行，每行一个整数，表示每取出一件货物以后，对于重量和最大的一堆货物，其重量和为多少。
```

**样例输入**

```
5
3 2 4 4 5
4 3 5 2 1
```

**样例输出**

```
9
5
5
3
0

Hint

思考方向（1）如何快速找到单据i的当前所在区间，这样才能将其分割成两个区间；（2）如何快速找到当前所有区间的最大值。
解题思路：用可以提升查找速度的数据结构，比如set和multiset。
此题目需要使用迭代器实现查询和替换，对绝大多数同学来说难度较大。
```

**解析**

**题目要求**

初始时编号 1~n 的货物形成一个连续区间。每次取出某件货物后，其所在区间以该货物为界分裂为左右两个子区间。每步操作后输出所有区间中重量和的最大值。

**解题思路**

使用两个有序集合协同工作：

1. **区间集合**（`set<pair<int,int>>`）：存储当前所有连续区间 [l, r]，按键（左端点）排序，用于快速定位货物所在的区间。
2. **重量和集合**（`multiset<long long>`）：存储各区间的重量和，用于快速获取最大值（`*sums.rbegin()`）。

配合前缀和数组 pre[]，区间 [l, r] 的重量和可在 O(1) 时间内计算为 pre[r] - pre[l-1]。每次取出编号为 x 的货物时：先用 `upper_bound` 定位 x 所在的区间 [l, r]；将该区间从两个集合中删除；然后将 [l, x-1] 和 [x+1, r]（若非空）分别插入两个集合中。最后输出重量和集合中的最大值。

**算法分析**

- 时间复杂度：O(n log n)，每次操作涉及 set 和 multiset 的查找、删除与插入
- 空间复杂度：O(n)

**注意事项**

- 使用 `upper_bound({x, 2147483647})` 后手动前移一位，定位 x 所在区间，注意迭代器操作的正确性
- 从 multiset 中删除元素时，应使用 `sums.find(value)` 获取迭代器后删除，避免误删其他相同值的区间
- 分裂时注意边界条件：当 l = x 或 x = r 时，对应的子区间为空，不应插入

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <set>
#include <utility>
#include <vector>
using namespace std;
int main() {
    int n;
    cin >> n;
    vector<long long> w(n + 2), pre(n + 1);
    for (int i = 1; i <= n; i++) {
        cin >> w[i];
        pre[i] = pre[i - 1] + w[i];
    }
    vector<int> ord(n);
    for (int &i : ord)
        cin >> i;
    set<pair<int, int>> seg{{1, n}};
    multiset<long long> sums{pre[n]};
    for (int x : ord) {
        auto it = seg.upper_bound({x, 2147483647});
        --it;
        int l = it->first, r = it->second;
        seg.erase(it);
        sums.erase(sums.find(pre[r] - pre[l - 1]));
        if (l <= x - 1) {
            seg.insert({l, x - 1});
            sums.insert(pre[x - 1] - pre[l - 1]);
        }
        if (x + 1 <= r) {
            seg.insert({x + 1, r});
            sums.insert(pre[r] - pre[x]);
        }
        cout << (sums.empty() ? 0 : *sums.rbegin()) << "\n";
    }
}
```

## 91. 18716 出栈序列（数据加强版）

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18716&access=5cbc88476f057a8c62db3dee213df547&fixedLanguage=MDsx
- Time Limit: 2000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
现在有一个1-n的排列，入栈序列已知，请给出字典序最大的出栈序列。
两个序列的字典序和字符串字典序相似，比较两个序列中第一个不相同的数值，值大字典序大。
```

**输入**

```
第一行一个整数n。(1<=n<=1000000)
第二行n个整数，数据确保为1-n的排列。
```

**输出**

```
输出n个整数，既字典序最大的出栈序列。
```

**样例输入**

```
5
1 2 4 5 3
```

**样例输出**

```
5 4 3 2 1

Hint

注意读取数据时应采用scanf或快读。
```

**解析**

**题目要求**

给定 1~n 的入栈序列，求字典序最大的出栈序列。

**解题思路**

为使出栈序列的字典序最大，应尽可能让较大的元素优先出栈。贪心策略如下：预处理后缀最大值数组 suf[]，其中 suf[i] 表示从位置 i 到末尾所有元素的最大值。依次将元素入栈，每次入栈后检查：若栈顶元素大于所有尚未入栈的元素（即栈顶 > suf[i+1]），则将栈顶元素弹出加入出栈序列，并持续检查直到条件不满足。这样保证了当前能出栈的最大元素一定优先出栈，从而获得字典序最大的出栈序列。

**算法分析**

- 时间复杂度：O(n)，每个元素恰好入栈和出栈各一次
- 空间复杂度：O(n)，栈和后缀最大值数组

**注意事项**

- 数据规模 n 可达 10^6，应使用 scanf 或快速读入以避免 I/O 超时
- 后缀最大值数组 suf[] 从右向左递推：suf[i] = max(suf[i+1], a[i])，suf[n] = 0

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;
int main() {
    int n;
    cin >> n;
    vector<int> a(n), suf(n + 1, 0), ans, st;
    for (int &i : a)
        cin >> i;
    for (int i = n - 1; i >= 0; i--)
        suf[i] = max(suf[i + 1], a[i]);
    for (int i = 0; i < n; i++) {
        st.push_back(a[i]);
        while (!st.empty() && st.back() > suf[i + 1]) {
            ans.push_back(st.back());
            st.pop_back();
        }
    }
    for (int i = 0; i < n; i++)
        cout << ans[i] << (i + 1 == n ? '\n' : ' ');
}
```

## 92. 19008 哈希表

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19008&access=b116de262f7eb038802bfde2644f83b1&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
哈希表（Hash Table，也叫散列表），是根据键（Key）而直接访问在内存存储位置的数据结构。也就是说，它通过计算一个键值的函数，
将所需查询的数据映射到表中一个位置来访问记录，这加快了查找速度。这个映射函数称做哈希函数，存放记录的数组称做哈希表。

现在有n个数，需要按顺序把他们插入一个长度为n的哈希表中，哈希表的位置为0到n-1。
插入的规则（线性探测法）：哈希表开始为空。对于一个数x，在哈希表中，如果(x mod n)的位置是空的(mod为求余运算），就把x放在(x mod n)的位置上。
如果不是空的，我们称之为产生冲突，就从(x mod n)往右开始找到第一个空的位置插入。若一直到n-1都不是空的，就从位置0开始继续往右找第一个空的位置插入。
因为哈希表总共有n个空位，需要插入n个数，所以每个数都能被插入。
把这n个数按顺序插入哈希表后，输出哈希表。
```

**输入**

```
第一行包含一个正整数n(1≤n≤100000)。

第二行包含n个非负整数x(0≤x≤10^9)，这些数按从左到右的顺序依次插入哈希表。
```

**输出**

```
输出第一行，输出有多少个数插入时没有冲突。

输出第二行，n个数，第i个数表示哈希表中位置为i所对应的数。 (0≤i≤n-1)。
```

**样例输入**

```
4
1 2 6 5
```

**样例输出**

```
2
5 1 2 6

Hint

插入1时，1 mod 4=1，是空的，在位置1插入。

插入2时，2 mod 4=2，是空的，在位置2插入。

插入6时，6 mod 4=2，不是空的，找到下一个空的位置为3，所以在位置3插入。

插入5时，5 mod 4=1，不是空的，找到下一个空的位置为0，所以在位置0插入。

题目数据量较大，请使用scanf，printf输入输出，避免使用cin，cout，以免超时。

解题思路：问题转换，实际上是在一个序列中查找比(x mod n)值大的最小值，可用set存储，并调用lowbound函数快速找到这个值。
```

**解析**

**题目要求**

将 n 个数依次插入长度为 n 的哈希表，使用线性探测法处理冲突（向右循环查找空位），统计无冲突插入的次数并输出最终哈希表。

**解题思路**

朴素模拟每次线性探测的时间复杂度为 O(n^2)，在 n = 100000 时会超时。优化的关键观察是：线性探测的本质是在当前所有空位置中，找到第一个 >= hash(x) 的位置；若不存在，则回到位置 0（取空位置集合中的最小值）。可以用有序集合（`set`）维护所有尚未被占用的位置编号。插入元素 x 时，先计算 p = x mod n，用 `lower_bound(p)` 在空位置集合中查找第一个 >= p 的空位；若不存在则取集合首元素（即最小的空位，实现循环探测）。插入后将该位置从集合中删除。若 `lower_bound(p)` 直接命中 p，说明无冲突，累加无冲突计数器。

**算法分析**

- 时间复杂度：O(n log n)，每次 set 操作为 O(log n)
- 空间复杂度：O(n)

**注意事项**

- 使用 `set` 而非数组模拟，将线性探测的 O(n) 优化为 O(log n)
- 插入完成后需从空位置集合中删除该位置，确保后续操作的正确性

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <set>
#include <vector>
using namespace std;
int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    int n;
    cin >> n;
    set<int> empty;
    for (int i = 0; i < n; i++)
        empty.insert(i);
    vector<long long> h(n);
    int no = 0;
    for (int i = 0; i < n; i++) {
        long long x;
        cin >> x;
        int p = x % n;
        if (empty.count(p))
            no++;
        auto it = empty.lower_bound(p);
        if (it == empty.end())
            it = empty.begin();
        h[*it] = x;
        empty.erase(it);
    }
    cout << no << "\n";
    for (int i = 0; i < n; i++)
        cout << h[i] << (i + 1 == n ? '\n' : ' ');
}
```

## 93. 19040 序列合并

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19040&access=257e907f3571bf388e5c716a091352ae&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
有两个长度都是N的序列A和B，在A和B中各取一个数相加可以得到N^2个和，求这N^2个和中最小的N个。
```

**输入**

```
第一行一个正整数N；1<=N<=100000
第二行N个整数Ai;
第三行N个整数Bi;
```

**输出**

```
输出仅一行，包含N个整数，从小到大输出这N个最小的和，相邻数字之间用空格隔开。
```

**样例输入**

```
3
2 6 6
1 4 8
```

**样例输出**

```
3 6 7

Hint

优先队列模板题
```

**解析**

**题目要求**

从两个长度为 N 的序列中各取一个数相加，共 N^2 个和，求其中最小的 N 个。

**解题思路**

首先将 A 和 B 分别排序。将所有形如 A[i] + B[0]（i = 0, 1, ..., N-1）的 N 个候选和存入最小堆（优先队列），堆中每个结点记录和值 sum 以及对应的下标 (i, j)。每次从堆中弹出最小元素并输出，然后将同一行的下一个候选和 A[i] + B[j+1] 加入堆中（若 j+1 < N）。这一过程类似多路归并，能够保证按递增顺序产生前 N 个最小和。

**算法分析**

- 时间复杂度：O(N log N)，排序 O(N log N)，堆操作 N 次各 O(log N)
- 空间复杂度：O(N)

**注意事项**

- 初始只将 B[0] 列的候选和入堆（共 N 个），而非全部 N^2 个，这是控制空间复杂度的关键
- 每次弹出后沿 B 方向推进一个位置（j++），保证不遗漏候选和也不产生重复

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <queue>
#include <vector>
using namespace std;
struct Node {
    long long sum;
    int i, j;
    bool operator<(Node const &o) const {
        return sum > o.sum;
    }
};
int main() {
    int n;
    cin >> n;
    vector<long long> A(n), B(n);
    for (auto &x : A)
        cin >> x;
    for (auto &x : B)
        cin >> x;
    sort(A.begin(), A.end());
    sort(B.begin(), B.end());
    priority_queue<Node> pq;
    for (int i = 0; i < n; i++)
        pq.push({A[i] + B[0], i, 0});
    for (int k = 0; k < n; k++) {
        auto cur = pq.top();
        pq.pop();
        cout << cur.sum << (k + 1 == n ? '\n' : ' ');
        if (cur.j + 1 < n)
            pq.push({A[cur.i] + B[cur.j + 1], cur.i, cur.j + 1});
    }
}
```

## 94. 18873 团队实力

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18873&access=a9b9256692a7cbc3452b5c21645d85d6&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
在一个团队中，团队的实力是各个团队成员能力值之和。
作为团队领袖，你现在需要在N个成员中选择一些成员来构成最强团队，每个成员都有一个能力值a[i]和一个限定值v[i]，
限定值的意思是，如果选择了第i名成员，团队总人数不能超过v[i]。
当然，如果你不选择第i名成员，就不受这个限制。

请求出团队的最大实力。
```

**输入**

```
第一行包含一个正整数n(1≤n≤10^5)。

接下来n行，每行包括2个正整数ai,vi，代表第i名成员的能力值和限定值(1≤ai≤10^9,1≤vi≤n)。
```

**输出**

```
输出团队的最大实力。
```

**样例输入**

```
3
1 3
2 3
100 1
```

**样例输出**

```
100

Hint

显然只选择第3名成员团队实力最大。
题目具有双限定的特点，显然我们要贪心最大能力值，但问题是还有限定v。如何确保选择极值的同时还能满足限定。
一般思考此类问题时应自己写出一些简单案例。可以发现先选限定值v大的，再选小的就不会出现限定值不满足的情况。
因此可以先按限定值从大到小排序，然后按次序选择，选择之后可能超过限定v，因此要淘汰掉值最小的那些，
此时可采用优先队列priority_queue来存储已选择的v值，需要淘汰时淘汰队头的最小值元素。
```

**解析**

**题目要求**

从 N 名成员中选择若干人组成团队，使团队能力值之和最大。约束条件为：若选择了某成员，则团队总人数不能超过该成员的限定值 v[i]。

**解题思路**

本题需同时满足能力值最大化和人数限定两个约束，采用贪心结合优先队列的策略。将成员按限定值 v 从大到小排序，依次考虑每个成员。使用小根堆（最小堆）维护当前已选成员的能力值，并记录堆中元素之和 sum。对于当前成员（能力值 val，限定值 v），将其加入堆中并更新 sum。若堆的大小超过 v，则弹出堆顶（能力值最小的成员）并从 sum 中减去其能力值，确保团队人数满足当前成员的限定。由于已处理成员的限定值均 >= v，缩减后的人数同样满足他们的限定条件。遍历过程中记录 sum 的最大值即为答案。

**算法分析**

- 时间复杂度：O(n log n)，排序和堆操作各为 O(n log n)
- 空间复杂度：O(n)

**注意事项**

- 按限定值从大到小排序是贪心策略的关键：先处理限定宽松的成员，后处理限定严格的成员，确保加入新成员后只需检查新的限定约束
- 小根堆中淘汰的是能力值最小的成员，以保留对团队贡献更大的成员
- 答案应在遍历过程中取 sum 的最大值，而非最终值（因为后续可能因限定更严格而淘汰成员）

**C++ 参考答案**

```cpp
#include <algorithm>
#include <functional>
#include <iostream>
#include <queue>
#include <utility>
#include <vector>
using namespace std;
int main() {
    int n;
    cin >> n;
    vector<pair<int, long long>> a(n);
    for (auto &p : a)
        cin >> p.second >> p.first;
    sort(a.begin(), a.end(), greater<>());
    priority_queue<long long, vector<long long>, greater<long long>> pq;
    long long sum = 0, ans = 0;
    for (auto [v, val] : a) {
        pq.push(val);
        sum += val;
        while ((int)pq.size() > v) {
            sum -= pq.top();
            pq.pop();
        }
        ans = max(ans, sum);
    }
    cout << ans;
}
```
# 实验6

## 95. 8638 直接插入排序

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8638&access=e61c61d1c71c456e874d6cda2e8120da&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
用函数实现直接插入排序，并输出每趟排序的结果.
```

**输入**

```
第一行：键盘输入待排序关键的个数n
第二行：输入n个待排序关键字，用空格分隔数据
```

**输出**

```
每行输出一趟排序结果，数据之间用一个空格分隔
```

**样例输入**

```
10
5 4 8 0 9 3 2 6 7 1
```

**样例输出**

```
4 5 8 0 9 3 2 6 7 1
4 5 8 0 9 3 2 6 7 1
0 4 5 8 9 3 2 6 7 1
0 4 5 8 9 3 2 6 7 1
0 3 4 5 8 9 2 6 7 1
0 2 3 4 5 8 9 6 7 1
0 2 3 4 5 6 8 9 7 1
0 2 3 4 5 6 7 8 9 1
0 1 2 3 4 5 6 7 8 9

Hint
```

**解析**

**题目要求**

实现直接插入排序算法，并在每一趟插入完成后输出当前序列的完整状态。

**解题思路**

直接插入排序的核心思想是：将数组视为"已排序区"和"未排序区"两部分。初始时，第一个元素构成有序区；从第二个元素（i = 1）开始，依次取出第 i 个元素，在前方已有序的区间 [0, i-1] 中从后向前查找其正确的插入位置，并将大于该元素的记录依次向后移动一位，腾出空位完成插入。每完成一次插入操作，即输出当前数组的完整序列。

**算法分析**

- 时间复杂度：最坏情况 O(n²)（逆序输入），最好情况 O(n)（已有序输入），平均 O(n²)
- 空间复杂度：O(1)，原地排序
- 稳定性：稳定排序（相同元素的相对顺序不变）

**C++ 参考答案**

```cpp
#include <iostream>
#include <vector>
using namespace std;

// 输出数组全部元素，元素间以空格分隔，末尾换行
void pr(vector<int> &a) {
    for (int i = 0; i < a.size(); i++)
        cout << a[i] << (i + 1 == a.size() ? '\n' : ' ');
}

int main() {
    int n;
    cin >> n;
    vector<int> a(n);
    for (int &i : a)
        cin >> i;

    // 从第 2 个元素（下标 1）开始，依次插入前方有序区
    for (int i = 1; i < n; i++) {
        int x = a[i], j = i - 1;     // x 为待插入元素，j 为有序区末尾指针
        while (j >= 0 && a[j] > x) { // 从后向前查找插入位置，同时后移元素
            a[j + 1] = a[j];
            j--;
        }
        a[j + 1] = x; // 将待插入元素放入正确位置
        pr(a);        // 每完成一趟插入，输出当前序列
    }
}
```

## 96. 8639 折半插入排序

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8639&access=efdd062cec28cd7705dab4d4f8a152be&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
用函数实现折半插入排序，并输出每趟排序的结果.
```

**输入**

```
第一行：键盘输入待排序关键的个数n
第二行：输入n个待排序关键字，用空格分隔数据
```

**输出**

```
每行输出一趟排序结果，数据之间用一个空格分隔
```

**样例输入**

```
10
5 4 8 0 9 3 2 6 7 1
```

**样例输出**

```
4 5 8 0 9 3 2 6 7 1
4 5 8 0 9 3 2 6 7 1
0 4 5 8 9 3 2 6 7 1
0 4 5 8 9 3 2 6 7 1
0 3 4 5 8 9 2 6 7 1
0 2 3 4 5 8 9 6 7 1
0 2 3 4 5 6 8 9 7 1
0 2 3 4 5 6 7 8 9 1
0 1 2 3 4 5 6 7 8 9

Hint
```

**解析**

**题目要求**

实现折半插入排序（二分插入排序），并在每一趟插入完成后输出当前序列的完整状态。

**解题思路**

折半插入排序是对直接插入排序的优化。在直接插入排序中，查找插入位置采用的是顺序查找，时间复杂度为 O(n)；而折半插入排序利用前方区间已有序的特点，改用二分查找来定位插入位置，将比较次数从 O(n) 降低到 O(log n)。具体步骤如下：

1. 取出第 i 个元素 x，在有序区间 [0, i-1] 中通过二分查找确定 x 的插入位置 pos
2. 将 [pos, i-1] 区间的所有元素整体后移一位
3. 将 x 放入 a[pos]

**算法分析**

- 时间复杂度：比较次数降为 O(n log n)，但元素移动次数仍为 O(n²)，故总体仍为 O(n²)
- 空间复杂度：O(1)，原地排序
- 稳定性：稳定排序
- **注意**：二分查找仅减少了比较操作的次数，并未减少移动操作的次数，因此在实际性能上与直接插入排序差距不大

**C++ 参考答案**

```cpp
#include <iostream>
#include <vector>
using namespace std;

// 输出数组全部元素，元素间以空格分隔，末尾换行
void pr(vector<int> &a) {
    for (int i = 0; i < a.size(); i++)
        cout << a[i] << (i + 1 == a.size() ? '\n' : ' ');
}

int main() {
    int n;
    cin >> n;
    vector<int> a(n);
    for (int &i : a)
        cin >> i;

    for (int i = 1; i < n; i++) {
        int x = a[i], l = 0, r = i - 1, pos = i;
        // 在有序区间 [l, r] 中二分查找插入位置
        while (l <= r) {
            int m = (l + r) / 2;
            if (a[m] > x)
                pos = m, r = m - 1; // x 应插入到 m 之前
            else
                l = m + 1; // x 应插入到 m 之后
        }
        // 将 [pos, i-1] 区间的元素整体后移一位
        for (int j = i; j > pos; j--)
            a[j] = a[j - 1];
        a[pos] = x; // 将待插入元素放入正确位置
        pr(a);      // 每完成一趟插入，输出当前序列
    }
}
```

## 97. 8640 希尔(shell)排序

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8640&access=b3cd78f73ccaaeaa382298a444ac4387&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
用函数实现希尔(shell)排序，并输出每趟排序的结果,初始增量d=n/2,其后d=d/2
```

**输入**

```
第一行：键盘输入待排序关键的个数n
第二行：输入n个待排序关键字，用空格分隔数据
```

**输出**

```
每行输出一趟排序结果，数据之间用一个空格分隔
```

**样例输入**

```
10
5 4 8 0 9 3 2 6 7 1
```

**样例输出**

```
3 2 6 0 1 5 4 8 7 9
1 0 3 2 4 5 6 8 7 9
0 1 2 3 4 5 6 7 8 9

Hint
```

**解析**

**题目要求**

实现希尔排序算法，采用 Shell 原始增量序列（d = n/2, n/4, ..., 1），并在每个增量排序完成后输出当前序列的完整状态。

**解题思路**

希尔排序是插入排序的一种优化策略，又称"缩小增量排序"。其核心思想是：将待排序序列按照一定的增量 gap 分成若干个子序列，对每个子序列分别进行直接插入排序。随着增量逐步缩小，子序列包含的元素越来越多，整个序列的有序程度也越来越高。当增量缩小到 1 时，整个序列恰好被分为一组，此时对其进行最后一次直接插入排序即可完成排序。

本题要求增量序列为 d = n/2, d = d/2, ..., 1，每个增量排序完成后输出一趟结果。

**算法分析**

- 时间复杂度：Shell 增量序列下约为 O(n^{1.5})，优于直接插入排序的 O(n²)
- 空间复杂度：O(1)，原地排序
- 稳定性：不稳定排序（相同元素可能在不同子序列中被重新排列）
- **注意**：希尔排序的时间复杂度依赖于增量序列的选取，不同增量序列会导致不同的效率

**C++ 参考答案**

```cpp
#include <iostream>
#include <vector>
using namespace std;

// 输出数组全部元素，元素间以空格分隔，末尾换行
void pr(vector<int> &a) {
    for (int i = 0; i < a.size(); i++)
        cout << a[i] << (i + 1 == a.size() ? '\n' : ' ');
}

int main() {
    int n;
    cin >> n;
    vector<int> a(n);
    for (int &i : a)
        cin >> i;

    // 按增量序列 d = n/2, n/4, ..., 1 逐趟排序
    for (int d = n / 2; d >= 1; d /= 2) {
        // 对每个子序列进行直接插入排序（步长为 d）
        for (int i = d; i < n; i++) {
            int x = a[i], j = i - d;     // x 为待插入元素，j 为同组前一个元素
            while (j >= 0 && a[j] > x) { // 在子序列中从后向前查找插入位置
                a[j + d] = a[j];
                j -= d;
            }
            a[j + d] = x; // 将元素插入子序列的正确位置
        }
        pr(a); // 每个增量排序完成后，输出当前序列
    }
}
```

## 98. 8641 冒泡排序

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8641&access=db80920471da05d373d67536dda47536&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
用函数实现冒泡排序，并输出每趟排序的结果(要求当一趟冒泡过程中不再有数据交换，则排序结束)
```

**输入**

```
第一行：键盘输入待排序关键的个数n
第二行：输入n个待排序关键字，用空格分隔数据
```

**输出**

```
每行输出每趟排序结果，数据之间用一个空格分隔
```

**样例输入**

```
10
5 4 8 0 9 3 2 6 7 1
```

**样例输出**

```
4 5 0 8 3 2 6 7 1 9
4 0 5 3 2 6 7 1 8 9
0 4 3 2 5 6 1 7 8 9
0 3 2 4 5 1 6 7 8 9
0 2 3 4 1 5 6 7 8 9
0 2 3 1 4 5 6 7 8 9
0 2 1 3 4 5 6 7 8 9
0 1 2 3 4 5 6 7 8 9
0 1 2 3 4 5 6 7 8 9

Hint
```

**解析**

**题目要求**

实现冒泡排序算法，每一趟排序结束后输出当前序列状态；若某一趟遍历过程中未发生任何元素交换，说明序列已有序，应提前结束排序。

**解题思路**

冒泡排序的基本思想是：每一趟从前向后依次比较相邻的两个元素，若前者大于后者则交换它们的位置。经过一趟遍历后，当前未排序区间中的最大元素会像"气泡"一样被交换到末尾位置。下一趟只需遍历到倒数第二个未排序元素即可，以此类推。

**优化策略**：设置一个布尔标志位 `sw`，记录每一趟遍历中是否发生过交换。若某一趟没有发生任何交换，则表明序列已经完全有序，可以提前终止外层循环。

**算法分析**

- 时间复杂度：最坏 O(n²)（逆序输入），最好 O(n)（已有序，一趟无交换即结束）
- 空间复杂度：O(1)，原地排序
- 稳定性：稳定排序（仅交换相邻元素，不改变相同元素的相对顺序）

**样例说明**

按冒泡排序从左到右逐趟交换相邻逆序元素，样例第 5 行应为 `0 2 3 4 1 5 6 7 8 9`。若写作 `0 2 3 4 5 1 6 7 8 9`，则与第 4、6 行之间的相邻交换过程不一致。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;

// 输出数组全部元素，元素间以空格分隔，末尾换行
void pr(vector<int> &a) {
    for (int i = 0; i < a.size(); i++)
        cout << a[i] << (i + 1 == a.size() ? '\n' : ' ');
}

int main() {
    int n;
    cin >> n;
    vector<int> a(n);
    for (int &i : a)
        cin >> i;

    for (int i = 0; i < n - 1; i++) {
        bool sw = false; // 标志位：记录本趟是否发生过交换
        // 每趟将当前未排序区间的最大元素冒泡到末尾
        for (int j = 0; j < n - 1 - i; j++) {
            if (a[j] > a[j + 1]) {
                swap(a[j], a[j + 1]);
                sw = true; // 发生了交换，序列尚未完全有序
            }
        }
        pr(a); // 每趟结束后输出当前序列状态
        if (!sw)
            break; // 若本趟无交换，说明序列已有序，提前结束
    }
}
```

## 99. 8642 快速排序

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8642&access=c5be8e9121fd4e9c47cc935415f142fa&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
用函数实现快速排序，并输出每次分区后排序的结果
```

**输入**

```
第一行：键盘输入待排序关键的个数n
第二行：输入n个待排序关键字，用空格分隔数据
```

**输出**

```
每行输出每趟排序的结果，数据之间用一个空格分隔
```

**样例输入**

```
10
5 4 8 0 9 3 2 6 7 1
```

**样例输出**

```
1 4 2 0 3 5 9 6 7 8
0 1 2 4 3 5 9 6 7 8
0 1 2 4 3 5 9 6 7 8
0 1 2 3 4 5 9 6 7 8
0 1 2 3 4 5 8 6 7 9
0 1 2 3 4 5 7 6 8 9
0 1 2 3 4 5 6 7 8 9

Hint
```

**解析**

**题目要求**

实现快速排序算法，每次分区（partition）操作完成后，输出整个数组的当前状态。

**解题思路**

快速排序采用分治策略。选取当前区间的第一个元素作为枢轴（pivot），通过分区操作将小于等于枢轴的元素放到其左侧，大于等于枢轴的元素放到其右侧，枢轴则位于最终的正确位置。然后对左右两个子区间递归执行相同的分区操作，直到子区间长度为 1 或 0。

**分区算法**（挖坑法）：

1. 保存枢轴值 pivot = a[l]，设置左右指针 i = l, j = r
2. 右指针 j 从右向左找到第一个小于 pivot 的元素，填入 a[i]
3. 左指针 i 从左向右找到第一个大于 pivot 的元素，填入 a[j]
4. 重复步骤 2-3，直到 i == j，将 pivot 填入 a[i]

**算法分析**

- 时间复杂度：平均 O(n log n)，最坏 O(n²)（每次分区极不均匀）
- 空间复杂度：O(log n)（递归栈深度）
- 稳定性：不稳定排序
- **注意**：本题要求每次分区后输出全序列，而非仅输出枢轴元素

**C++ 参考答案**

```cpp
#include <iostream>
#include <vector>
using namespace std;

vector<int> a;

// 输出整个数组的当前状态
void pr() {
    for (int i = 0; i < a.size(); i++)
        cout << a[i] << (i + 1 == a.size() ? '\n' : ' ');
}

// 分区函数：以 a[l] 为枢轴，返回枢轴最终位置
int part(int l, int r) {
    int pivot = a[l], i = l, j = r; // 选取首元素作为枢轴
    while (i < j) {
        // 右指针从右向左找第一个小于 pivot 的元素
        while (i < j && a[j] >= pivot)
            j--;
        a[i] = a[j]; // 将该元素填入左侧空位
        // 左指针从左向右找第一个大于 pivot 的元素
        while (i < j && a[i] <= pivot)
            i++;
        a[j] = a[i]; // 将该元素填入右侧空位
    }
    a[i] = pivot; // 枢轴填入最终位置
    pr();         // 每次分区完成后输出整个序列
    return i;     // 返回枢轴位置，用于递归处理左右子区间
}

// 快速排序递归函数
void qs(int l, int r) {
    if (l < r) {
        int p = part(l, r); // 分区，获取枢轴位置
        qs(l, p - 1);       // 递归排序左子区间
        qs(p + 1, r);       // 递归排序右子区间
    }
}

int main() {
    int n;
    cin >> n;
    a.resize(n);
    for (int &i : a)
        cin >> i;
    qs(0, n - 1);
}
```

## 100. 8643 简单选择排序

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8643&access=74b0431c95b0e45a556fe28558d5cb0c&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
用函数实现简单选择排序，并输出每趟排序的结果
```

**输入**

```
第一行：键盘输入待排序关键的个数n
第二行：输入n个待排序关键字，用空格分隔数据
```

**输出**

```
每行输出每趟排序的结果，数据之间用一个空格分隔
```

**样例输入**

```
10
5 4 8 0 9 3 2 6 7 1
```

**样例输出**

```
0 4 8 5 9 3 2 6 7 1
0 1 8 5 9 3 2 6 7 4
0 1 2 5 9 3 8 6 7 4
0 1 2 3 9 5 8 6 7 4
0 1 2 3 4 5 8 6 7 9
0 1 2 3 4 5 8 6 7 9
0 1 2 3 4 5 6 8 7 9
0 1 2 3 4 5 6 7 8 9
0 1 2 3 4 5 6 7 8 9

Hint
```

**解析**

**题目要求**

实现简单选择排序算法，并在每一趟选择交换完成后输出当前序列的完整状态。

**解题思路**

简单选择排序的基本思想是：在第 i 趟排序中，从未排序区间 [i, n-1] 中遍历选出关键字最小的元素（记下其下标 k），将其与未排序区间的第一个元素 a[i] 交换。交换后 a[i] 归入已排序区间，未排序区间缩小为 [i+1, n-1]。重复 n-1 趟即可完成整个排序过程。

**算法分析**

- 时间复杂度：无论输入如何，比较次数恒为 n(n-1)/2，即 O(n²)
- 空间复杂度：O(1)，原地排序
- 稳定性：不稳定排序（交换操作可能改变相同元素的相对顺序）
- **注意**：即使未排序区间的最小元素恰好就是 a[i]，仍需执行交换（自身交换），并输出当前序列

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;

// 输出数组全部元素，元素间以空格分隔，末尾换行
void pr(vector<int> &a) {
    for (int i = 0; i < a.size(); i++)
        cout << a[i] << (i + 1 == a.size() ? '\n' : ' ');
}

int main() {
    int n;
    cin >> n;
    vector<int> a(n);
    for (int &i : a)
        cin >> i;

    for (int i = 0; i < n - 1; i++) {
        int k = i; // k 记录未排序区间中最小元素的下标
        // 遍历未排序区间 [i+1, n-1]，查找最小元素
        for (int j = i + 1; j < n; j++)
            if (a[j] < a[k])
                k = j;
        swap(a[i], a[k]); // 将最小元素交换到当前位置
        pr(a);            // 每趟结束后输出当前序列
    }
}
```

## 101. 8644 堆排序

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8644&access=0938368f50aba32df97946f5fd729db8&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
用函数实现堆排序，并输出每趟排序的结果
```

**输入**

```
第一行：键盘输入待排序关键的个数n
第二行：输入n个待排序关键字，用空格分隔数据
```

**输出**

```
第一行：初始建堆后的结果
其后各行输出交换堆顶元素并调整堆的结果，数据之间用一个空格分隔
```

**样例输入**

```
10
5 4 8 0 9 3 2 6 7 1
```

**样例输出**

```
9 7 8 6 4 3 2 5 0 1
8 7 3 6 4 1 2 5 0 9
7 6 3 5 4 1 2 0 8 9
6 5 3 0 4 1 2 7 8 9
5 4 3 0 2 1 6 7 8 9
4 2 3 0 1 5 6 7 8 9
3 2 1 0 4 5 6 7 8 9
2 0 1 3 4 5 6 7 8 9
1 0 2 3 4 5 6 7 8 9
0 1 2 3 4 5 6 7 8 9

Hint
```

**解析**

**题目要求**

实现堆排序算法。首先将数组建立为大根堆并输出初始堆序列，然后反复将堆顶元素（当前最大值）与堆尾元素交换，缩小堆的范围并对新的堆顶执行向下调整（sift down），每完成一次交换和调整即输出当前序列。

**解题思路**

堆排序利用"大根堆"这一完全二叉树数据结构进行排序，分为两个阶段：

1. **建堆阶段**：从最后一个非叶子节点（下标为 n/2 - 1）开始，自底向上、自右向左依次对每个节点执行向下调整操作，在 O(n) 时间内将数组调整为大根堆。
2. **排序阶段**：将堆顶元素 a[0]（当前最大值）与堆尾元素 a[end] 交换，堆的有效范围缩小为 [0, end-1]，然后对新堆顶执行向下调整以恢复大根堆性质。重复此过程直到堆中仅剩一个元素。

**向下调整（sift down）**：将节点与其左右子节点中值较大的子节点比较，若节点值小于该子节点，则交换并继续向下调整，直到节点不小于其子节点或到达叶子。

**算法分析**

- 时间复杂度：O(n log n)，建堆 O(n)，n-1 次调整各 O(log n)
- 空间复杂度：O(1)，原地排序
- 稳定性：不稳定排序

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;

vector<int> a;

// 输出整个数组的当前状态
void pr() {
    for (int i = 0; i < a.size(); i++)
        cout << a[i] << (i + 1 == a.size() ? '\n' : ' ');
}

// 向下调整函数：将下标为 i 的节点向下调整，堆的有效范围为 [0, n-1]
void down(int i, int n) {
    while (true) {
        int l = i * 2 + 1; // 左子节点下标
        int r = l + 1;     // 右子节点下标
        int b = i;         // b 记录当前节点及其子节点中值最大的下标
        if (l < n && a[l] > a[b])
            b = l; // 左子节点更大
        if (r < n && a[r] > a[b])
            b = r; // 右子节点更大
        if (b == i)
            break;        // 当前节点已是最大，无需继续调整
        swap(a[i], a[b]); // 交换当前节点与最大子节点
        i = b;            // 继续向下调整
    }
}

int main() {
    int n;
    cin >> n;
    a.resize(n);
    for (int &i : a)
        cin >> i;

    // 建堆：从最后一个非叶子节点开始，自底向上执行向下调整
    for (int i = n / 2 - 1; i >= 0; i--)
        down(i, n);
    pr(); // 输出初始建堆后的结果

    // 排序：反复交换堆顶与堆尾，并调整堆
    for (int end = n - 1; end >= 1; end--) {
        swap(a[0], a[end]); // 将堆顶（最大值）交换到堆尾
        down(0, end);       // 对新堆顶执行向下调整，堆范围缩小为 [0, end-1]
        pr();               // 每次交换并调整后输出当前序列
    }
}
```

## 102. 8645 归并排序（非递归算法）

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8645&access=18c1bad602bc9dd6bbe7c24c763fc0c7&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
用函数实现归并排序（非递归算法），并输出每趟排序的结果
```

**输入**

```
第一行：键盘输入待排序关键的个数n
第二行：输入n个待排序关键字，用空格分隔数据
```

**输出**

```
每行输出每趟排序的结果，数据之间用一个空格分隔
```

**样例输入**

```
10
5 4 8 0 9 3 2 6 7 1
```

**样例输出**

```
4 5 0 8 3 9 2 6 1 7
0 4 5 8 2 3 6 9 1 7
0 2 3 4 5 6 8 9 1 7
0 1 2 3 4 5 6 7 8 9

Hint
```

**解析**

**题目要求**

实现非递归（迭代）版本的归并排序，并在每一趟归并完成后输出当前序列的完整状态。

**解题思路**

非递归归并排序采用自底向上的迭代策略，避免了递归调用的开销。其核心思想是：初始时将每个元素视为长度为 1 的有序段，然后按段长 len = 1, 2, 4, 8, ... 逐趟将相邻的两个有序段两两合并（归并）为一个更大的有序段，直到段长不小于 n 时排序完成。

每一趟归并的具体操作：以 2*len 为步长遍历数组，取相邻两段 [l, l+len-1] 和 [l+len, l+2*len-1]，使用双指针合并到辅助数组 b 中，最后将 b 的内容拷贝回 a。

**算法分析**

- 时间复杂度：O(n log n)，共 log n 趟，每趟归并 O(n)
- 空间复杂度：O(n)，需要一个与原数组等长的辅助数组
- 稳定性：稳定排序（合并时相等元素保持原有顺序）
- **注意**：最后一段可能不足 len 个元素，需要用 min 函数处理边界

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;

// 输出数组全部元素，元素间以空格分隔，末尾换行
void pr(vector<int> &a) {
    for (int i = 0; i < a.size(); i++)
        cout << a[i] << (i + 1 == a.size() ? '\n' : ' ');
}

int main() {
    int n;
    cin >> n;
    vector<int> a(n), b(n); // a 为原数组，b 为归并时的辅助数组
    for (int &i : a)
        cin >> i;

    // 段长从 1 开始，每趟翻倍，直到段长不小于 n
    for (int len = 1; len < n; len *= 2) {
        // 遍历所有相邻的有序段对
        for (int l = 0; l < n; l += 2 * len) {
            int m = min(l + len, n);     // 第一段的中点（第二段的起点）
            int r = min(l + 2 * len, n); // 第二段的终点（开区间）
            int i = l, j = m, k = l; // i 遍历第一段，j 遍历第二段，k 写入辅助数组
            // 双指针合并两个有序段到辅助数组 b
            while (i < m && j < r)
                b[k++] = (a[i] <= a[j] ? a[i++] : a[j++]);
            while (i < m)
                b[k++] = a[i++]; // 第一段剩余元素
            while (j < r)
                b[k++] = a[j++]; // 第二段剩余元素
        }
        a.swap(b); // 将归并结果交换回 a
        pr(a);     // 每趟归并完成后输出当前序列
    }
}
```

## 103. 8646 基数排序

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8646&access=bc93783fbe508300daf70d409c3b63c9&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
用函数实现基数排序，并输出每次分配收集后排序的结果
```

**输入**

```
第一行：键盘输入待排序关键的个数n
第二行：输入n个待排序关键字，用空格分隔数据
```

**输出**

```
每行输出每趟每次分配收集后排序的结果，数据之间用一个空格分隔
```

**样例输入**

```
10
278 109 063 930 589 184 505 069 008 083
```

**样例输出**

```
930 063 083 184 505 278 008 109 589 069
505 008 109 930 063 069 278 083 184 589
008 063 069 083 109 184 278 505 589 930

Hint
```

**解析**

**题目要求**

实现 LSD（最低位优先）基数排序算法，每次按某一位进行"分配-收集"操作后，输出当前序列的完整状态。

**解题思路**

基数排序是一种非比较型排序算法，利用多关键字排序的思想实现。LSD（Least Significant Digit first）策略从最低位（个位）开始，逐位向高位进行排序：

1. **分配**：根据当前位的数字（0-9），将所有元素分配到对应的 10 个桶中
2. **收集**：按桶编号 0-9 的顺序，依次将桶中元素取出放回原数组

由于每一位的排序都是稳定的（相同位值的元素保持之前的相对顺序），经过 d 轮（d 为最大数的位数）分配和收集后，整个序列即为有序。

**算法分析**

- 时间复杂度：O(d(n + r))，其中 d 为位数，n 为元素个数，r 为基数（本题 r = 10）
- 空间复杂度：O(n + r)，需要 r 个桶来存放元素
- 稳定性：稳定排序
- **注意**：本题数据为三位数，输出时需使用 `%03d` 格式化以保留前导零

**C++ 参考答案**

```cpp
#include <cstdio>
#include <iostream>
#include <vector>
using namespace std;

// 输出数组全部元素，使用 %03d 格式化以保留前导零，元素间以空格分隔
void pr(vector<int> &a) {
    for (int i = 0; i < a.size(); i++)
        printf("%03d%c", a[i], i + 1 == a.size() ? '\n' : ' ');
}

int main() {
    int n;
    cin >> n;
    vector<int> a(n);
    for (int &i : a)
        cin >> i;

    // 从个位到百位，依次按每一位进行分配和收集
    for (int exp = 1; exp <= 100; exp *= 10) {
        // 分配：按当前位数字将元素放入对应的桶中
        vector<vector<int>> bucket(10);
        for (int x : a)
            bucket[x / exp % 10].push_back(x);
        // 收集：按桶编号顺序将元素放回原数组
        int k = 0;
        for (auto &v : bucket)
            for (int x : v)
                a[k++] = x;
        pr(a); // 每次分配收集完成后输出当前序列
    }
}
```

# 拓展习题6

## 104. 18746 逆序数

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18746&access=3742e22b81bdd72e0071a62fd798536f&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
在一个排列中，如果一对数的前后位置与大小顺序相反，即前面的数大于后面的数，那么它们就称为一个逆序。
一个排列中逆序的总数就称为这个排列的逆序数。逆序数是课程线性代数的一个知识点。
现在给定一个排列a1,a2,…,an，如果存在i<j并且ai>aj，那么我们称ai和aj为一个逆序，请求出排列的逆序数。
```

**输入**

```
第一行为n,表示排列长度。(1=<n<=100000)
第二行有n个整数，依次为排列中的a1,a2,…,an。所有整数均在int范围内。
```

**输出**

```
一个整数代表排列的逆序数。
```

**样例输入**

```
4
3 2 3 2
```

**样例输出**

```
3

Hint

注意答案的数据范围。
```

**解析**

**题目要求**

给定一个长度为 n 的序列，求出其中逆序对的总数。逆序对定义为满足 i < j 且 a[i] > a[j] 的数对 (a[i], a[j])。

**解题思路**

暴力枚举所有数对的时间复杂度为 O(n²)，在 n = 100000 时不可接受。高效的解法是借助归并排序的过程来统计逆序对数量。

在归并排序的合并阶段，当左半区间 [l, m) 和右半区间 [m, r) 进行合并时：若当前右半元素 a[j] 小于左半元素 a[i]，则 a[j] 需要放到 a[i] 之前。此时左半区间中从 i 到 m-1 的所有元素都大于 a[j]（因为左半区间已有序），因此 a[j] 与这些元素构成 (m - i) 个逆序对。累加所有这些逆序对数量即可得到总逆序数。

**算法分析**

- 时间复杂度：O(n log n)，与归并排序一致
- 空间复杂度：O(n)，归并排序需要辅助数组
- **注意事项**：逆序数可能超过 int 的表示范围（最大可达 n(n-1)/2），必须使用 long long 类型存储结果

**C++ 参考答案**

```cpp
#include <iostream>
#include <vector>
using namespace std;

long long ans;            // 逆序对总数，需用 long long 防止溢出
vector<long long> a, tmp; // a 为原数组，tmp 为归并辅助数组

// 归并排序并在合并阶段统计逆序对
void ms(int l, int r) {
    if (r - l <= 1)
        return; // 区间长度不超过 1，无需排序
    int m = (l + r) / 2;
    ms(l, m); // 递归排序左半区间
    ms(m, r); // 递归排序右半区间

    int i = l, j = m, k = l;
    // 合并两个有序区间
    while (i < m || j < r) {
        if (j == r || (i < m && a[i] <= a[j])) {
            // 左半元素较小或右半已空，放入左半元素
            tmp[k++] = a[i++];
        } else {
            // 右半元素较小，说明左半剩余元素均大于 a[j]，构成逆序对
            ans += m - i; // 累加逆序对数量
            tmp[k++] = a[j++];
        }
    }
    // 将归并结果拷贝回原数组
    for (i = l; i < r; i++)
        a[i] = tmp[i];
}

int main() {
    int n;
    cin >> n;
    a.resize(n);
    tmp.resize(n);
    for (auto &x : a)
        cin >> x;
    ms(0, n);
    cout << ans;
}
```

## 105. 18746 六一儿童节

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18967&access=a343d323774cd20f32e089d348f1c9ac&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
拼多多2018校招内推编程题

六一儿童节，老师带了很多好吃的巧克力到幼儿园。

每块巧克力j的重量为w[j]，对于每个小朋友i，当他分到的巧克力大小达到h[i] (即w[j]>=h[i])，他才会上去表演节目。

老师的目标是将巧克力分发给孩子们，使得最多的小孩上台表演。

可以保证每个w[i]> 0且不能将多块巧克力分给一个孩子或将一块分给多个孩子。
```

**输入**

```
第一行：n，表示小朋友的个数
第二行：n个整数，表示h数组元素
第三行：m，表示巧克力的个数
第四行：m个整数，表示巧克力的重量
n,m等所有数据均小于100
```

**输出**

```
上台表演学生人数
```

**样例输入**

```
3
2 3 2
2
3 1
```

**样例输出**

```
1
```

**解析**

**题目要求**

有 n 个小朋友和 m 块巧克力。每个小朋友有一个需求值 h[i]，只有当分到的巧克力重量 w[j] >= h[i] 时，该小朋友才会上台表演。每块巧克力只能分给一个小朋友，每个小朋友最多分一块巧克力。求最多能让多少个小朋友上台表演。

**解题思路**

本题是一个典型的贪心匹配问题。贪心策略为：优先满足需求最小的小朋友，并为他分配能满足其需求的重量最小的巧克力。这样可以尽可能保留较大的巧克力去满足需求更大的小朋友，从而最大化满足人数。

具体实现：将小朋友的需求数组 h 和巧克力重量数组 w 分别升序排序，然后使用双指针 i、j 分别遍历两个数组。若当前巧克力 w[j] 能满足当前小朋友 h[i]，则匹配成功（ans++，两指针均后移）；否则当前巧克力不满足该小朋友，仅后移巧克力指针 j，尝试下一块更大的巧克力。

**算法分析**

- 时间复杂度：O(n log n + m log m)，主要来自排序操作
- 空间复杂度：O(n + m)
- **贪心策略的正确性**：若需求最小的小朋友都无法被当前最小的可用巧克力满足，则该巧克力对任何小朋友都无用；若能被满足，则使用最小的可用巧克力是最优的，不会浪费更大的巧克力

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;

int main() {
    int n, m;
    cin >> n;
    vector<int> h(n);
    for (int &i : h)
        cin >> i; // 读入每个小朋友的需求值
    cin >> m;
    vector<int> w(m);
    for (int &i : w)
        cin >> i; // 读入每块巧克力的重量

    sort(h.begin(), h.end()); // 按需求升序排列小朋友
    sort(w.begin(), w.end()); // 按重量升序排列巧克力

    int i = 0, j = 0, ans = 0;
    // 双指针贪心匹配
    while (i < n && j < m) {
        if (w[j] >= h[i]) {  // 当前巧克力满足当前小朋友的需求
            ans++, i++, j++; // 匹配成功，两者均后移
        } else {
            j++; // 当前巧克力太小，尝试下一块更大的
        }
    }
    cout << ans;
}
```

## 106. 18962 区间合并

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18962&access=5aa1480fc65dd436acc52fbee8c622c7&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
字节跳动面试题。

给出N个区间，请合并所有重叠的区间。比如[10,30],[20,60]，可以合并成[10,60]。
下面4个区间
[[10,30],[80,100],[150,180],[20,60],]
可以合并成3个区间
[[10,60],[80,100],[150,180]]

按区间左端点的次序输出合并后的所有区间。
```

**输入**

```
第一行一个整数N(1<=N<=100000)。
第二行到第N+1行，每行2个整数，代表区间的左右端点。
```

**输出**

```
按区间左端点的次序输出合并后的所有区间,每行输出一个区间。
```

**样例输入**

```
4
10 30
80 100
150 180
20 60
```

**样例输出**

```
10 60
80 100
150 180
```

**解析**

**题目要求**

给定 N 个闭区间，将所有重叠（含端点相接）的区间合并为不相交的区间，并按左端点升序输出。

**解题思路**

解决区间合并问题的标准方法是"排序 + 线性扫描"：

1. **排序**：将所有区间按左端点升序排列
2. **扫描合并**：维护一个"当前合并区间" [l, r]。从第二个区间开始逐一检查：
   - 若当前区间的左端点 <= r，说明与当前合并区间重叠，则将 r 更新为 max(r, 当前区间的右端点)
   - 若不重叠，则输出当前合并区间 [l, r]，并以当前区间作为新的合并区间
3. 遍历结束后，输出最后一个合并区间

**算法分析**

- 时间复杂度：O(n log n)，排序为主要开销，扫描合并仅需 O(n)
- 空间复杂度：O(n)
- **注意**：两个区间 [a, b] 和 [b, c] 也视为重叠（端点相接），应合并为 [a, c]

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <utility>
#include <vector>
using namespace std;

int main() {
    int n;
    cin >> n;
    vector<pair<int, int>> a(n);
    for (auto &p : a)
        cin >> p.first >> p.second; // 读入所有区间

    sort(a.begin(), a.end()); // 按左端点升序排列

    int l = a[0].first, r = a[0].second; // 初始化当前合并区间
    for (int i = 1; i < n; i++) {
        if (a[i].first <= r) {
            // 当前区间与合并区间重叠，扩展右端点
            r = max(r, a[i].second);
        } else {
            // 不重叠，输出当前合并区间，开启新区间
            cout << l << ' ' << r << "\n";
            l = a[i].first;
            r = a[i].second;
        }
    }
    cout << l << ' ' << r << "\n"; // 输出最后一个合并区间
}
```

## 107. 18963 最大数字

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18963&access=172a3d44eb0a5bf7b7ed9f5c04a587c2&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
题目来自腾讯笔试题。

给定N个非负整数，现需要将他们重新排列并拼接，使得最后的结果最大，输出这个结果。
注意不能简单比大小进行拼接，比如321和32，显然32放前面结果（32321）会更大。
```

**输入**

```
第一行一个整数N。（1<=N<=1000）
第二行N个非负整数，每个整数值不大于1000。
```

**输出**

```
拼接后的最大整数。
```

**样例输入**

```
2
321 32
```

**样例输出**

```
32321

Hint

此题目可用C的字符数组做，但用C++提供的string类型会很简洁，通过后可看标程。
```

**解析**

**题目要求**

将 N 个非负整数以某种顺序排列后拼接成一个大的整数，使得拼接结果最大。

**解题思路**

本题的关键在于设计正确的比较规则。对于两个数字的字符串形式 x 和 y，不能简单地按字典序或数值大小排序，而应比较拼接后的结果：

- 若 x + y > y + x（字符串拼接后按字典序比较），则 x 应排在 y 前面
- 若 x + y < y + x，则 y 应排在 x 前面
- 若 x + y == y + x，则两者顺序无关

例如：x = "32", y = "321"，由于 "32" + "321" = "32321" > "321" + "32" = "32132"，所以 "32" 应排在 "321" 前面。

该比较关系具有传递性，因此可以作为排序的比较函数使用。排序完成后，将所有字符串依次拼接即为答案。

**算法分析**

- 时间复杂度：O(n log n * L)，其中 L 为字符串平均长度（比较时需要拼接字符串）
- 空间复杂度：O(n * L)
- **注意事项**：需要处理前导零的情况——若拼接结果全为零，应输出 "0" 而非 "000...0"

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <string>
#include <vector>
using namespace std;

int main() {
    int n;
    cin >> n;
    vector<string> a(n);
    for (auto &s : a)
        cin >> s;

    // 自定义排序：若 x+y > y+x，则 x 排在 y 前面
    sort(a.begin(), a.end(), [](const string &x, const string &y) { return x + y > y + x; });

    // 拼接所有字符串
    string res;
    for (auto &s : a)
        res += s;

    // 去除前导零（若结果全为零，保留最后一位 "0"）
    int p = 0;
    while (p + 1 < res.size() && res[p] == '0')
        p++;
    cout << res.substr(p);
}
```

## 108. 18965 找到 K 个最接近的元素

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18965&access=84bdae18842089e286d8cce4a7ce594e&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
远景智能-2021秋季招聘软件技术笔试题（第二批）

给定一个数组，两个整数 k 和 x，从数组中找到最靠近 x（两数之差最小）的 k 个数。

返回的结果必须是按升序排好的。

如果有两个数与 x 的差值一样，优先选择数值较小的那个数。
```

**输入**

```
第一行为数组arr，数组不为空，且长度不超过 10000，数组里的每个元素与 x 的绝对值不超过 10000。

第二行为查找的个数k。

第三行为基准值x。

注意题目并没有给出数组的长度，因此要把整个数组当成一行字符串读入，再从字符串中依次解析出数字。
    int i=0,n=0,a[100005];
    string s;
    getline(cin,s);
    while(i < s.length())
    {
        int sum=0;//处理连续的数字字符
        while(isdigit(s[i]))
            sum=sum*10+s[i++]-'0';
        a[++n]=sum;
        i++;
    }
```

**输出**

```
按升序排好的的数组
```

**样例输入**

```
1,5,3,2,4
4
3
```

**样例输出**

```
1,2,3,4

Hint

注意题目并没有给出数组的长度，因此要把整个数组当成一行字符串读入，再从字符串中依次解析出数字。
```

**解析**

**题目要求**

从一个以逗号分隔的数组中，找出最接近基准值 x 的 k 个元素。若有多个元素与 x 的差值相同，优先选择数值较小的元素。最终结果按升序排列并以逗号分隔输出。

**解题思路**

本题可分为三个步骤：

1. **输入解析**：题目未直接给出数组长度，第一行为逗号分隔的数字字符串，需要整行读入后逐个解析出数字（注意处理负数的情况）
2. **按距离排序**：自定义排序规则——首先按 |元素 - x| 升序排列；若距离相同，则按元素值升序排列（数值小的优先）
3. **取前 k 个并升序输出**：截取排序后的前 k 个元素，对其进行升序排列后以逗号分隔输出

**算法分析**

- 时间复杂度：O(n log n)，排序为主要开销
- 空间复杂度：O(n)
- **注意事项**：输入数组中可能包含负数，解析时需注意负号的处理；输出元素之间用逗号而非空格分隔

**C++ 参考答案**

```cpp
#include <algorithm>
#include <cstdlib>
#include <ctype.h>
#include <iostream>
#include <string>
#include <vector>
using namespace std;

int main() {
    // 第一步：解析逗号分隔的输入字符串
    string line;
    getline(cin, line);
    vector<int> a;
    for (int i = 0; i < line.size();) {
        if (isdigit((unsigned char)line[i]) || line[i] == '-') {
            int sign = 1;
            if (line[i] == '-')
                sign = -1, i++; // 处理负号
            int v = 0;
            // 连续读取数字字符，构造整数
            while (i < line.size() && isdigit((unsigned char)line[i]))
                v = v * 10 + line[i++] - '0';
            a.push_back(sign * v);
        } else {
            i++; // 跳过逗号等非数字字符
        }
    }

    int k, x;
    cin >> k >> x;

    // 第二步：按"与 x 的距离"排序，距离相同时数值小的优先
    sort(a.begin(), a.end(), [&](int u, int v) {
        int du = abs(u - x), dv = abs(v - x);
        return du == dv ? u < v : du < dv;
    });

    // 第三步：取前 k 个元素，升序排列后输出
    a.resize(k);
    sort(a.begin(), a.end());
    for (int i = 0; i < k; i++) {
        if (i)
            cout << ','; // 元素之间用逗号分隔
        cout << a[i];
    }
}
```

## 109. 18966 两两配对差值最小

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18966&access=d03637ca2f71099034f66ffeef800a78&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
拼多多2019秋招部分编程题

给定一个长度为偶数的数组arr，将该数组中的数字两两配对并求和，在这些和中选出最大和最小值，

请问该如何两两配对，才能让最大值和最小值的差值最小？
```

**输入**

```
一共2行输入。
第一行为一个整数n，2<=n<=10000, 第二行为n个数，组成目标数组，每个数大于等于2，小于等于100。
```

**输出**

```
输出最小的差值。
```

**样例输入**

```
6
11 4 3 5 7 1
```

**样例输出**

```
3
```

**解析**

**题目要求**

将 n 个数（n 为偶数）两两配对，共形成 n/2 对。每对求和，在所有配对和中找出最大值与最小值，要求使"最大值 - 最小值"的差值尽可能小。

**解题思路**

最优策略是"首尾配对"：将数组升序排列后，让最小的元素与最大的元素配对，第二小的与第二大的配对，依此类推。即第 i 小的元素 a[i] 与第 i 大的元素 a[n-1-i] 配对，配对和为 a[i] + a[n-1-i]。

**正确性分析**：该策略的核心思想是均衡各组的和。若将两个较大的数配在一起，会产生一个很大的和；将两个较小的数配在一起，会产生一个很小的和，从而使最大值与最小值的差值变大。而首尾配对使得每对的和都趋近于总和的一半，从而有效缩小了最大和与最小和之间的差距。

**算法分析**

- 时间复杂度：O(n log n)，主要来自排序操作
- 空间复杂度：O(n)，存储配对和数组

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;

int main() {
    int n;
    cin >> n;
    vector<int> a(n);
    for (int &i : a)
        cin >> i;

    sort(a.begin(), a.end()); // 升序排列

    // 首尾配对：a[i] + a[n-1-i]
    vector<int> s;
    for (int i = 0; i < n / 2; i++)
        s.push_back(a[i] + a[n - 1 - i]);

    // 输出配对和的最大值与最小值之差
    cout << *max_element(s.begin(), s.end()) - *min_element(s.begin(), s.end());
}
```

## 110. 18961 最大点的集合

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18961&access=0c38b90e1136174a60c87d923e2bb5a7&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
字节跳动2018校招测试开发方向（第一批）

P为给定的二维平面整数点集。定义 P 中某点x，如果x满足 P 中任意点都不在 x
 的右上方区域内（横纵坐标都大于x），则称其为"最大的"。
求出所有"最大的"点的集合。（所有点的横坐标和纵坐标都不重复, 坐标轴范围在[0, 1e9) 内）

如下图：实心点为满足条件的点的集合。请实现代码找到集合 P 中的所有 "最大" 点的集合并输出。
```

**输入**

```
第一行输入点集的个数 N， 接下来 N 行，每行两个数字代表点的 X 轴和 Y 轴。
对于 50%的数据,  1 <= N <= 10000;
对于 100%的数据, 1 <= N <= 500000;
```

**输出**

```
输出"最大的" 点集合， 按照 X 轴从小到大的方式输出，每行两个数字分别代表点的 X 轴和 Y轴。
```

**样例输入**

```
5
1 2
5 3
4 6
7 5
9 0
```

**样例输出**

```
4 6
7 5
9 0
```

**解析**

**题目要求**

在给定的二维平面点集中，找出所有"最大点"——即不存在其他点的横坐标和纵坐标同时严格大于该点的点。将结果按 x 坐标升序输出。

**解题思路**

一个点 (x, y) 是"最大点"当且仅当不存在另一个点 (x', y') 使得 x' > x 且 y' > y。等价地说，对于点 (x, y)，在所有 x 坐标大于 x 的点中，最大的 y 坐标也不超过 y。

基于此观察，算法如下：

1. **排序**：将所有点按 x 坐标从大到小排列（x 相同时按 y 从大到小）
2. **扫描**：维护一个变量 maxy 记录已扫描点中的最大 y 坐标（初始为 -1）。从左到右遍历排序后的点，若当前点的 y > maxy，则该点不被任何右方点的 y 值超越，即为最大点，将其加入结果集并更新 maxy
3. **输出**：将结果集按 x 坐标升序排列后输出

**算法分析**

- 时间复杂度：O(n log n)，主要来自排序操作
- 空间复杂度：O(n)
- **注意**：题目中 N 最大可达 500000，需使用快速 I/O（ios::sync_with_stdio(false)）以避免超时

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <utility>
#include <vector>
using namespace std;

int main() {
    ios::sync_with_stdio(false); // 关闭同步以加速 I/O
    cin.tie(nullptr);

    int n;
    cin >> n;
    vector<pair<int, int>> p(n);
    for (auto &x : p)
        cin >> x.first >> x.second;

    // 按 x 从大到小排序，x 相同时按 y 从大到小
    sort(p.begin(), p.end(), [](auto &a, auto &b) {
        return a.first == b.first ? a.second > b.second : a.first > b.first;
    });

    vector<pair<int, int>> ans;
    int maxy = -1; // 记录已扫描点中的最大 y 值
    // 从右向左扫描：若当前点的 y 大于已见最大 y，则为最大点
    for (auto [x, y] : p) {
        if (y > maxy) {
            ans.push_back({x, y});
            maxy = y;
        }
    }

    // 将结果按 x 升序排列后输出
    sort(ans.begin(), ans.end());
    for (auto [x, y] : ans)
        cout << x << ' ' << y << "\n";
}
```

## 111. 19018 正则序列

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19018&access=f1918669260ea1bdddd0ffeaaae3044d&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
美团2021校招笔试-编程题(通用编程试题,第10场)
我们称一个长度为n的序列为正则序列，当且仅当该序列是一个由1~n组成的排列，

即该序列由n个正整数组成，取值在[1,n]范围，且不存在重复的数，同时正则序列不要求排序。

有一天小团得到了一个长度为n的任意序列，他需要在有限次操作内，将这个序列变成一个正则序列，

每次操作他可以任选序列中的一个数字，并将该数字加一或者减一。

请问他最少用多少次操作可以把这个序列变成正则序列？
```

**输入**

```
输入第一行仅包含一个正整数n，表示任意序列的长度。(1<=n<=20000)

输入第二行包含n个整数，表示给出的序列，每个数的绝对值都小于10000。
```

**输出**

```
输出仅包含一个整数，表示最少的操作数量。
```

**样例输入**

```
5
-1 2 3 10 100
```

**样例输出**

```
103

Hint

进阶思考：如果限定时间复杂度为O（n），空间复杂度为O（n）如何处理。
```

**解析**

**题目要求**

给定一个长度为 n 的整数序列，每次操作可以将某个元素加 1 或减 1，求将其变为正则序列（即 1 到 n 的一个排列）所需的最少操作次数。

**解题思路**

目标是将序列变为 {1, 2, 3, ..., n} 的一个排列。设排序后的序列为 a[0] <= a[1] <= ... <= a[n-1]，则最优方案是将 a[i] 变为 i+1（即第 i 小的元素变为第 i 小的目标值）。

**正确性证明**：可以使用交换论证（exchange argument）来证明。假设最优方案中存在交叉对应关系，即 a[i] 对应目标值 t[j]，a[j] 对应目标值 t[i]（其中 i < j, t[i] < t[j]），则交换对应关系后，总代价 |a[i] - t[i]| + |a[j] - t[j]| 不会超过原来的 |a[i] - t[j]| + |a[j] - t[i]|。因此排序后一一对应的方案不劣于任何其他方案。

**算法分析**

- 时间复杂度：O(n log n)，主要来自排序操作
- 空间复杂度：O(n)
- **注意事项**：操作次数总和可能超出 int 范围，应使用 long long 类型；每个元素的变化量需取绝对值

**C++ 参考答案**

```cpp
#include <algorithm>
#include <cstdlib>
#include <iostream>
#include <vector>
using namespace std;

int main() {
    int n;
    cin >> n;
    vector<long long> a(n);
    for (auto &x : a)
        cin >> x;

    sort(a.begin(), a.end()); // 升序排列

    long long ans = 0;
    // 排序后第 i 小的元素应变为 i+1，累加操作次数
    for (int i = 0; i < n; i++)
        ans += llabs(a[i] - (i + 1));

    cout << ans;
}
```

## 112. 18958 有趣的排序

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18958&access=3bb70d26c41726fdfdcab66863426fb5&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
百度2017春招笔试真题编程题集合
度度熊有一个N个数的数组，他想将数组从小到大 排好序，但是萌萌的度度熊只会下面这个操作：
任取数组中的一个数然后将它放置在数组的最后一个位置。
问最少操作多少次可以使得数组从小到大有序？
```

**输入**

```
首先输入一个正整数N，接下来的一行输入N个整数。(N <=100, 每个数的绝对值小于等于1000)
```

**输出**

```
输出一个整数表示最少的操作次数。
```

**样例输入**

```
4
19 7 8 25
```

**样例输出**

```
2

Hint

个人经验之谈：此类移来移去的问题一般涉及算法有贪心、最大上升子序列、最大上升子段等。
为了找到规律，先思考一个简单样例：5 4 6 1，
由于最小的1在最后，1左边3个数字必须移动，而移动是随意选择，所以1左侧这3个数字的位置并不重要。
再设计一个样例：X 2 X X 1 X， 我们发现2在1的左侧，
那么2必须先移动到最后，此时形成如下序列X X X 1 X 2，其他数字比2大，我们可以按大小移动到最后。
这样此题目规律就是，原序列中最小值不用移动，第二小的值如果在最小值后面，也不用移动，
如果第二小在最小值前面，那么必然要移动n-1个元素。
同理递推可得：原序列中如存在最小，第二小，第三小......这种上升子序列，这些元素无序移动，其他元素必须移动。
例如 6 4 1 8 7 2 5 3,存在......1.....2....3....，这样序列无需移动1,2,3。
```

**解析**

**题目要求**

给定一个数组，每次操作可以选取一个元素并将其移至数组末尾。求使数组变为升序排列所需的最少操作次数。

**解题思路**

被移到末尾的元素可以按任意顺序依次放置，因此它们总能排列成正确的升序。关键在于找出最多有多少个元素可以"不用移动"。

不需要移动的元素必须满足以下条件：它们在原数组中的相对顺序与排序后的顺序完全一致。具体来说，设排序后的数组为 b，在原数组 a 中从左到右扫描，若能依次找到 b[0], b[1], b[2], ...（不一定连续，但相对顺序不变），则这些元素无需移动。

设不用移动的元素最多有 keep 个，则最少操作次数为 n - keep。

**算法实现**：利用哈希表记录每个元素在排序后数组中的下标，然后遍历原数组，查找最长的"排序后下标递增子序列"，其长度即为 keep。

**算法分析**

- 时间复杂度：O(n log n)（排序）+ O(n)（扫描），总体 O(n log n)
- 空间复杂度：O(n)

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <map>
#include <vector>
using namespace std;

int main() {
    int n;
    cin >> n;
    vector<int> a(n), b;
    for (int &i : a)
        cin >> i;

    b = a;
    sort(b.begin(), b.end()); // b 为排序后的目标数组

    // pos 记录每个元素在排序后数组中的下标
    map<int, int> pos;
    for (int i = 0; i < n; i++)
        pos[b[i]] = i;

    // 在原数组中查找最长的"排序后下标递增子序列"
    int keep = 0, last = -1;
    for (int x : a) {
        int p = pos[x];
        if (p > last) { // 当前元素在排序后数组中的位置大于上一个保留元素的位置
            keep++; // 该元素可以不用移动
            last = p;
        }
    }

    cout << n - keep; // 最少操作次数 = 总数 - 不用移动的元素个数
}
```

## 113. 19065 有趣的数字

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19065&access=56550b627257d60902e6a5f59d5b4b3f&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
腾讯2017暑期实习生编程题
小Q今天在上厕所时想到了这个问题：有n个数，两两组成二元组，相差最小的有多少对呢？相差最大呢？
```

**输入**

```
N本组测试数据有n个数

 a1,a2...an - 需要计算的数据

 保证:

 1<=n<=100000,0<=ai<=INT_MAX.
```

**输出**

```
输出两个数，第一个数表示差最小的对数，第二个数表示差最大的对数。
```

**样例输入**

```
6
45 12 45 32 5 6
```

**样例输出**

```
1 2

Hint

注意思考这类数据例如n=6 : 1 1 1 2 2 2 最小对数有6对，最大对数有9对。
而所有数据全部相同的情况下，最大最小对数都是n*（n-1）/2;
```

**解析**

**题目要求**

给定 n 个数，求所有两两配对中差值最小的对数和差值最大的对数。

**解题思路**

首先将数组排序，然后分类讨论：

**最小差值对数**：

- 若存在重复元素，则最小差值为 0。此时需要统计所有相同元素对的数量：对于每个出现 c 次的元素，贡献 C(c, 2) = c(c-1)/2 对
- 若所有元素互不相同，则最小差值一定是排序后某两个相邻元素的差。遍历所有相邻元素对，找到最小差值，再统计差值等于该最小值的相邻对数量

**最大差值对数**：

- 最大差值 = 最大值 - 最小值
- 若最大值与最小值不同，则对数 = 最小值的出现次数 x 最大值的出现次数
- 若所有元素相同（最大值 = 最小值），则最大差值为 0，对数为 C(n, 2) = n(n-1)/2

**算法分析**

- 时间复杂度：O(n log n)（使用有序 map 自动排序）或 O(n log n)（先排序再遍历）
- 空间复杂度：O(n)
- **注意事项**：数据量较大（n = 100000），对数统计时需注意使用 long long 类型防止溢出

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <map>
#include <vector>
using namespace std;

// 组合数 C(x, 2) = x*(x-1)/2
long long C(long long x) {
    return x * (x - 1) / 2;
}

int main() {
    int n;
    cin >> n;
    vector<long long> a(n);
    map<long long, long long> cnt; // 有序 map，统计每个元素的出现次数
    for (auto &x : a) {
        cin >> x;
        cnt[x]++;
    }

    // 特殊情况：所有元素相同
    if (cnt.size() == 1) {
        cout << C(n) << ' ' << C(n);
        return 0;
    }

    long long mnPairs = 0;

    // 统计最小差值对数
    // 先检查是否有重复元素（重复元素产生差值 0 的对）
    long long last = 0, mind = (1LL << 62);
    bool hasLast = false;
    for (auto [v, c] : cnt) {
        if (c > 1)
            mnPairs += C(c); // 相同元素贡献 C(c,2) 对
        if (hasLast)
            mind = min(mind, v - last); // 更新相邻元素最小差值
        last = v;
        hasLast = true;
    }

    // 若无重复元素，统计差值等于最小差值的相邻对数
    if (mnPairs == 0) {
        for (auto it = cnt.begin(), pr = it++; it != cnt.end(); pr = it++) {
            if (it->first - pr->first == mind)
                mnPairs += it->second * pr->second; // 两个相邻值的所有组合
        }
    }

    // 统计最大差值对数：最小值出现次数 x 最大值出现次数
    auto lo = *cnt.begin(), hi = *cnt.rbegin();
    cout << mnPairs << ' ' << lo.second * hi.second;
}
```
# 实验7

## 114. 8647 实现图的存储结构

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8647&access=ebe1045389ccc57f0db83cad6abfd122&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
实现有向图的邻接矩阵存储结构。
```

**输入**

```
第一行：输入图的顶点个数n（各个顶点的默认编号为1~n）， 边的条数m。
第二 ~ m+1行：每行输入两个顶点编号i、j，表示连接顶点i到顶点j的一条边。
```

**输出**

```
分n行输出n*n的邻接矩阵，表示所输入的图存储，顶点i和顶点j之间如果有边相连，则输出1，没边相连则输出0。
```

**样例输入**

```
4 4
1 2
1 3
3 4
4 1
```

**样例输出**

```
0 1 1 0
0 0 0 0
0 0 0 1
1 0 0 0

Hint
```

**解析**

**题目要求**

实现有向图的邻接矩阵存储结构，并按照输入构建邻接矩阵后输出。

**解题思路**

邻接矩阵是图的一种基本存储方式。对于有向图，使用二维数组 `g[i][j]` 表示从顶点 `i` 到顶点 `j` 是否存在一条有向边：若存在则 `g[i][j] = 1`，否则 `g[i][j] = 0`。

具体步骤如下：
1. 初始化一个 `(n+1) x (n+1)` 的二维数组，所有元素置为 0。
2. 依次读入每条边的起点 `u` 和终点 `v`，将 `g[u][v]` 置为 1。
3. 按行输出整个邻接矩阵。

**算法分析**

- 时间复杂度：初始化矩阵为 O(n^2)，读入边为 O(m)，输出矩阵为 O(n^2)，总时间复杂度为 O(n^2)。
- 空间复杂度：O(n^2)，用于存储邻接矩阵。

**注意事项**

- 本题为有向图，因此 `g[u][v] = 1` 并不意味着 `g[v][u] = 1`，需注意方向性。
- 顶点编号从 1 开始，数组大小应开到 `n+1`。

**C++ 参考答案**

```cpp
#include <iostream>
#include <vector>
using namespace std;
int main() {
    int n, m;
    cin >> n >> m;
    vector<vector<int>> g(n + 1, vector<int>(n + 1));
    while (m--) {
        int u, v;
        cin >> u >> v;
        g[u][v] = 1;
    }
    for (int i = 1; i <= n; i++) {
        for (int j = 1; j <= n; j++)
            cout << g[i][j] << (j == n ? '\n' : ' ');
    }
}
```

## 115. 8648 图的深度遍历

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8648&access=94b1411cbf0dd30a793b6efe65686ef1&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
实现图的邻接表存储结构及一些基本操作函数。在此基础上实现图的深度遍历算法并加以测试。本题只给出部分代码,请补全内容。

#include"string.h"
#include"malloc.h" /* malloc()等 */
#include"stdio.h" /* EOF(=^Z或F6),NULL */
#include"stdlib.h" /* exit() */
typedef int InfoType; /* 顶点权值类型 */
#define MAX_NAME 3 /* 顶点字符串的最大长度+1 */
typedef char VertexType[MAX_NAME]; /* 字符串类型 */
/*图的邻接表存储表示 */
#define MAX_VERTEX_NUM 20
typedef enum{DG,DN,AG,AN}GraphKind; /* {有向图,有向网,无向图,无向网} */
typedef struct ArcNode
{
	int adjvex; /* 该弧所指向的顶点的位置 */
	struct ArcNode *nextarc; /* 指向下一条弧的指针 */
	InfoType *info; /* 网的权值指针） */
}ArcNode; /* 表结点 */

typedef struct
{
	VertexType data; /* 顶点信息 */
	ArcNode *firstarc; /* 第一个表结点的地址,指向第一条依附该顶点的弧的指针 */
}VNode,AdjList[MAX_VERTEX_NUM]; /* 头结点 */

typedef struct
{
	AdjList vertices;
	int vexnum,arcnum; /* 图的当前顶点数和弧数 */
	int kind; /* 图的种类标志 */
}ALGraph;

int LocateVex(ALGraph G,VertexType u)
{ /* 初始条件: 图G存在,u和G中顶点有相同特征 */
/* 操作结果: 若G中存在顶点u,则返回该顶点在图中位置;否则返回-1 */
	int i;
	for(i=0;i<G.vexnum;++i)
		if(strcmp(u,G.vertices[i].data)==0)
			return i;
	return -1;
}

void CreateGraph(ALGraph *G)
{ /* 采用邻接表存储结构,构造没有相关信息的图G(用一个函数构造4种图) */
	int i,j,k;
	int w; /* 权值 */
	VertexType va,vb;
	ArcNode *p;
	//printf("Enter the type of map:(0~3): ");
	scanf("%d",&(*G).kind);
	//printf("Enter Vertex number,Arc number: ");
	scanf("%d%d",&(*G).vexnum,&(*G).arcnum);
	//printf("Enter %d Vertex :\n",(*G).vexnum);
	for(i=0;i<(*G).vexnum;++i) /* 构造顶点向量 */
	{
		scanf("%s",(*G).vertices[i].data);
		(*G).vertices[i].firstarc=NULL;
	}
	//if((*G).kind==1||(*G).kind==3) /* 网 */
	//	printf("Enter order every arc weight,head and tail (Takes the gap by the blank space ):\n");
	//else /* 图 */
	//	printf("Enter order every arc head and tail (Takes the gap by the blank space ):\n");
	for(k=0;k<(*G).arcnum;++k) /* 构造表结点链表 */
	{
		if((*G).kind==1||(*G).kind==3) /* 网 */
		scanf("%d%s%s",&w,va,vb);
		else /* 图 */
		scanf("%s%s",va,vb);
		i=LocateVex(*G,va); /* 弧尾 */
		j=LocateVex(*G,vb); /* 弧头 */
		p=(ArcNode*)malloc(sizeof(ArcNode));
		p->adjvex=j;
		if((*G).kind==1||(*G).kind==3) /* 网 */
		{
			p->info=(int *)malloc(sizeof(int));
			*(p->info)=w;
		}
		else
		p->info=NULL; /* 图 */
		p->nextarc=(*G).vertices[i].firstarc; /* 插在表头 */
		(*G).vertices[i].firstarc=p;
		if((*G).kind>=2) /* 无向图或网,产生第二个表结点 */
		{
			p=(ArcNode*)malloc(sizeof(ArcNode));
			p->adjvex=i;
			if((*G).kind==3) /* 无向网 */
			{
				p->info=(int*)malloc(sizeof(int));
				*(p->info)=w;
			}
			else
			p->info=NULL; /* 无向图 */
			p->nextarc=(*G).vertices[j].firstarc; /* 插在表头 */
			(*G).vertices[j].firstarc=p;
		}
	}
}

VertexType* GetVex(ALGraph G,int v)
{ /* 初始条件: 图G存在,v是G中某个顶点的序号。操作结果: 返回v的值 */
	if(v>=G.vexnum||v<0)
		exit(0);
	return &G.vertices[v].data;
}

int FirstAdjVex(ALGraph G,VertexType v)
{ /* 初始条件: 图G存在,v是G中某个顶点 */
/* 操作结果: 返回v的第一个邻接顶点的序号。若顶点在G中没有邻接顶点,则返回-1 */
	ArcNode *p;
	int v1;
	v1=LocateVex(G,v); /* v1为顶点v在图G中的序号 */
	p=G.vertices[v1].firstarc;
	if(p)
		return p->adjvex;
	else
		return -1;
}

int NextAdjVex(ALGraph G,VertexType v,VertexType w)
{ /* 初始条件: 图G存在,v是G中某个顶点,w是v的邻接顶点 */
/* 操作结果: 返回v的(相对于w的)下一个邻接顶点的序号。 */
/* 若w是v的最后一个邻接点,则返回-1 */
	ArcNode *p;
	int v1,w1;
	v1=LocateVex(G,v); /* v1为顶点v在图G中的序号 */
	w1=LocateVex(G,w); /* w1为顶点w在图G中的序号 */
	p=G.vertices[v1].firstarc;
	while(p&&p->adjvex!=w1) /* 指针p不空且所指表结点不是w */
		p=p->nextarc;
	if(!p||!p->nextarc) /* 没找到w或w是最后一个邻接点 */
		return -1;
	else /* p->adjvex==w */
		return p->nextarc->adjvex; /* 返回v的(相对于w的)下一个邻接顶点的序号 */
}

/*深度遍历*/
int visited[MAX_VERTEX_NUM]; /* 访问标志数组(全局量),未访问标记0，访问标记1 */
void(*VisitFunc)(char* v); /* 函数变量(全局量) */
void DFS(ALGraph G,int v)
{ /* 从第v个顶点出发递归地深度优先遍历图G。算法7.5 */
/* 设置访问标志为TRUE(已访问) */
/* 访问第v个顶点 */
/* 对v的尚未访问的邻接点w递归调用DFS */

}
void DFSTraverse(ALGraph G)
{ /* 对图G作深度优先遍历。算法7.4 */
/* 使用全局变量VisitFunc,使DFS不必设函数指针参数 */
/* 访问标志数组初始化 */
/* 对尚未访问的顶点调用DFS */

	printf("\n");
}

void print(char *i)
{
	printf("%s ",i);
}

int main()
{
	ALGraph g;
	CreateGraph(&g);
	DFSTraverse(g);
	return 1;
}
```

**输入**

```
第一行：输入0到3之间整数(有向图:0,有向网:1,无向图:2,无向网:3)；
第二行：输入顶点数和边数；
第三行：输入各个顶点的值（字符型，长度〈3）；(遍历从输入的第一个顶点开始)
第四行：输入每条弧(边)弧尾和弧头(以空格作为间隔),如果是网还要输入权值；
```

**输出**

```
输出对图深度遍历的结果。
```

**样例输入**

```
0
3 3
a b c
a b
b c
c b
```

**样例输出**

```
a b c

Hint

注意题目的邻接表采用的是头插法，也就是后出现的边节点先被访问。
```

**解析**

**题目要求**

在邻接表存储结构上实现图的深度优先遍历（DFS）。题目给定的邻接表采用头插法建表。

**解题思路**

深度优先遍历的核心思想是：从某一顶点出发，标记该顶点为已访问并输出，然后依次对其每个未被访问的邻接顶点递归执行 DFS。

需要特别注意的关键点：题目中邻接表采用**头插法**构建，即后输入的边对应的邻接结点会插入到链表头部，因此在遍历邻接表时，后输入的邻接顶点会先被访问。

**算法分析**

- 时间复杂度：O(V + E)，其中 V 为顶点数，E 为边数。每个顶点和每条边各被访问常数次。
- 空间复杂度：O(V)，用于访问标记数组以及递归调用栈。

**注意事项**

- 图可能不连通，因此需要遍历所有顶点，对未访问的顶点分别调用 DFS。
- 头插法导致邻接点的访问顺序与输入顺序相反，这是本题的重要考查点。

**C++ 参考答案**

```cpp
#include <malloc.h> /* malloc()等 */
#include <stdio.h>  /* EOF(=^Z或F6),NULL */
#include <stdlib.h> /* exit() */
#include <string.h>
typedef int InfoType;              /* 顶点权值类型 */
#define MAX_NAME 3                 /* 顶点字符串的最大长度+1 */
typedef char VertexType[MAX_NAME]; /* 字符串类型 */
/* 图的邻接表存储表示 */
#define MAX_VERTEX_NUM 20
typedef enum { DG, DN, AG, AN } GraphKind; /* {有向图,有向网,无向图,无向网} */
typedef struct ArcNode {
    int adjvex;              /* 该弧所指向的顶点的位置 */
    struct ArcNode *nextarc; /* 指向下一条弧的指针 */
    InfoType *info;          /* 网的权值指针 */
} ArcNode;

typedef struct {
    VertexType data;   /* 顶点信息 */
    ArcNode *firstarc; /* 指向第一条依附该顶点的弧的指针 */
} VNode, AdjList[MAX_VERTEX_NUM];

typedef struct {
    AdjList vertices;
    int vexnum, arcnum; /* 图的当前顶点数和弧数 */
    int kind;           /* 图的种类标志 */
} ALGraph;

int LocateVex(ALGraph G, VertexType u) {
    int i;
    for (i = 0; i < G.vexnum; ++i)
        if (strcmp(u, G.vertices[i].data) == 0)
            return i;
    return -1;
}

void CreateGraph(ALGraph *G) {
    int i, j, k;
    int w;
    VertexType va, vb;
    ArcNode *p;
    scanf("%d", &(*G).kind);
    scanf("%d%d", &(*G).vexnum, &(*G).arcnum);
    for (i = 0; i < (*G).vexnum; ++i) {
        scanf("%s", (*G).vertices[i].data);
        (*G).vertices[i].firstarc = NULL;
    }
    for (k = 0; k < (*G).arcnum; ++k) {
        if ((*G).kind == 1 || (*G).kind == 3)
            scanf("%d%s%s", &w, va, vb);
        else
            scanf("%s%s", va, vb);
        i = LocateVex(*G, va);
        j = LocateVex(*G, vb);
        p = (ArcNode *)malloc(sizeof(ArcNode));
        p->adjvex = j;
        if ((*G).kind == 1 || (*G).kind == 3) {
            p->info = (int *)malloc(sizeof(int));
            *(p->info) = w;
        } else
            p->info = NULL;
        p->nextarc = (*G).vertices[i].firstarc;
        (*G).vertices[i].firstarc = p;
        if ((*G).kind >= 2) {
            p = (ArcNode *)malloc(sizeof(ArcNode));
            p->adjvex = i;
            if ((*G).kind == 3) {
                p->info = (int *)malloc(sizeof(int));
                *(p->info) = w;
            } else
                p->info = NULL;
            p->nextarc = (*G).vertices[j].firstarc;
            (*G).vertices[j].firstarc = p;
        }
    }
}

VertexType *GetVex(ALGraph G, int v) {
    if (v >= G.vexnum || v < 0)
        exit(0);
    return &G.vertices[v].data;
}

int FirstAdjVex(ALGraph G, VertexType v) {
    ArcNode *p;
    int v1;
    v1 = LocateVex(G, v);
    p = G.vertices[v1].firstarc;
    if (p)
        return p->adjvex;
    else
        return -1;
}

int NextAdjVex(ALGraph G, VertexType v, VertexType w) {
    ArcNode *p;
    int v1, w1;
    v1 = LocateVex(G, v);
    w1 = LocateVex(G, w);
    p = G.vertices[v1].firstarc;
    while (p && p->adjvex != w1)
        p = p->nextarc;
    if (!p || !p->nextarc)
        return -1;
    else
        return p->nextarc->adjvex;
}

/* 深度遍历 */
int visited[MAX_VERTEX_NUM]; /* 访问标志数组 */
void (*VisitFunc)(char *v);  /* 函数变量 */
void print(char *i);

void DFS(ALGraph G, int v) { /* 从第v个顶点出发递归地深度优先遍历图G。算法7.5 */
    visited[v] = 1;
    VisitFunc(G.vertices[v].data);
    for (ArcNode *p = G.vertices[v].firstarc; p != NULL; p = p->nextarc) {
        int w = p->adjvex;
        if (!visited[w])
            DFS(G, w);
    }
}

void DFSTraverse(ALGraph G) { /* 对图G作深度优先遍历。算法7.4 */
    VisitFunc = print;
    for (int v = 0; v < G.vexnum; ++v)
        visited[v] = 0;
    for (int v = 0; v < G.vexnum; ++v)
        if (!visited[v])
            DFS(G, v);
    printf("\n");
}

void print(char *i) {
    printf("%s ", i);
}

int main() {
    ALGraph g;
    CreateGraph(&g);
    DFSTraverse(g);
    return 0;
}
```

## 116. 8649 图的广度遍历

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=8649&access=5d953f205dce87ca0d1bbed718f4c133&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
使用图的深度遍历实现的邻接表存储结构和基本操作函数，在此基础上实现图的广度遍历算法并加以测试。注意正确使用队列存储结构。
```

**输入**

```
第一行：输入0到3之间整数(有向图:0,有向网:1,无向图:2,无向网:3)；
第二行：输入顶点数和边数；
第三行：输入各个顶点的值（字符型，长度〈3）；(遍历从输入的第一个顶点开始)
第四行：输入每条弧(边)弧尾和弧头(以空格作为间隔),如果是网还要输入权值；
```

**输出**

```
输出对图广度遍历的结果
```

**样例输入**

```
0
3 3
a b c
a b
b c
c b
```

**样例输出**

```
a b c

Hint

注意题目的邻接表采用头插法，也就是后出现的边节点插入到邻接表的表头。
```

**解析**

**题目要求**

在邻接表存储结构上实现图的广度优先遍历（BFS），并使用队列作为辅助数据结构。

**解题思路**

广度优先遍历的核心思想是：从起始顶点出发，将其标记为已访问并入队；每次从队首取出一个顶点并输出，然后依次将该顶点所有未被访问的邻接顶点标记为已访问并入队。重复此过程直至队列为空。

与 DFS 的区别在于：BFS 按照距离起始顶点的层次逐层扩展，使用队列（先进先出）而非递归（栈）来控制访问顺序。

**算法分析**

- 时间复杂度：O(V + E)，每个顶点和每条边各被处理常数次。
- 空间复杂度：O(V)，用于队列和访问标记数组。

**注意事项**

- 邻接表同样采用头插法构建，因此同一顶点的邻接点按与输入相反的顺序被访问。
- 图可能不连通，需对所有未访问的顶点分别启动一次 BFS。
- 入队时即标记为已访问，以避免同一顶点被重复入队。

**C++ 参考答案**

```cpp
#include <iostream>
#include <map>
#include <queue>
#include <string>
#include <vector>
using namespace std;
int main() {
    int kind, n, m;
    cin >> kind >> n >> m;
    vector<string> name(n);
    map<string, int> id;
    for (int i = 0; i < n; i++) {
        cin >> name[i];
        id[name[i]] = i;
    }
    vector<vector<int>> g(n);
    for (int i = 0; i < m; i++) {
        string a, b;
        cin >> a >> b;
        int u = id[a], v = id[b];
        g[u].insert(g[u].begin(), v);
        if (kind >= 2)
            g[v].insert(g[v].begin(), u);
        if (kind == 1 || kind == 3) {
            int w;
            cin >> w;
        }
    }
    vector<int> vis(n);
    queue<int> q;
    for (int s = 0; s < n; s++)
        if (!vis[s]) {
            vis[s] = 1;
            q.push(s);
            while (!q.empty()) {
                int u = q.front();
                q.pop();
                cout << name[u] << ' ';
                for (int v : g[u])
                    if (!vis[v])
                        vis[v] = 1, q.push(v);
            }
        }
}
```

## 117. 18448 最小生成树

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18448&access=8224d283e25b57b0eba5d767ea86d954&fixedLanguage=MDsxOzI=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC

**题目描述**

```
给定结点数为n，边数为m的带权无向连通图G，所有结点编号为1,2,3....n。
求图G的最小生成树的边权和。
```

**输入**

```
第一行两个正整数n和m。n,m<=2000
之后的m行，每行三个正整数a,b,w，描述一条连接结点a和b,边权为w的边。1=<a,b<=n,w<=10^18。
注意可能存在重边和自环。
```

**输出**

```
一个整数表示图G的最小生成树的边权和（注意用长整型）。
```

**样例输入**

```
7 12
1 2 9
1 5 2
1 6 3
2 3 5
2 6 7
3 4 6
3 7 3
4 5 6
4 7 2
5 6 3
5 7 6
6 7 1
```

**样例输出**

```
16
```

**解析**

**题目要求**

给定一个带权无向连通图，求其最小生成树（Minimum Spanning Tree, MST）的边权之和。

**解题思路**

本题采用 Kruskal 算法求解最小生成树，其核心思想是贪心策略：

1. 将所有边按边权从小到大排序。
2. 依次考察每条边，若该边的两个端点不在同一连通分量中（即加入该边不会形成环），则将该边加入最小生成树，并合并两个端点所在的连通分量。
3. 重复上述步骤，直至选出 n-1 条边（构成一棵生成树）或所有边均已考察完毕。

连通性判断使用**并查集**（Union-Find）数据结构，支持高效的查找与合并操作。

**算法分析**

- 时间复杂度：O(m log m)，主要开销在于对边进行排序。并查集的查找与合并操作近似为常数时间。
- 空间复杂度：O(n + m)，用于存储边集和并查集数组。

**注意事项**

- 边权最大可达 10^18，累加后可能超出 32 位整数范围，必须使用 `long long` 类型存储边权和。
- 图中可能存在重边和自环：重边不影响算法正确性（排序后权值较小的边优先被选取），自环的两个端点属于同一连通分量，会被自动跳过。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <functional>
#include <iostream>
#include <vector>
using namespace std;
struct E {
    int u, v;
    long long w;
    bool operator<(E const &o) const {
        return w < o.w;
    }
};
int main() {
    int n, m;
    cin >> n >> m;
    vector<E> e(m);
    for (auto &x : e)
        cin >> x.u >> x.v >> x.w;
    sort(e.begin(), e.end());
    vector<int> p(n + 1);
    for (int i = 0; i < (int)p.size(); i++)
        p[i] = i;
    function<int(int)> f = [&](int x) { return p[x] == x ? x : p[x] = f(p[x]); };
    long long ans = 0;
    for (auto x : e) {
        int a = f(x.u), b = f(x.v);
        if (a != b) {
            p[a] = b;
            ans += x.w;
        }
    }
    cout << ans;
}
```

## 118. 18732 最短路问题

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18732&access=8eda8eb8df2b5ef72b6358f5431d411f&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
现在有n个车站和m条直达公交线路，每条线路都有一个固定票价。
作为一个窮人，你打算从车站1坐车到车站n，请计算下车站1到车站n的最少花费。
如果车站1无法到达车站n，请输出-1。
注意，在车站x和y之间可能存在不止一条线路。
```

**输入**

```
第一行两个整数n和m，表示车站数量和线路数量。(1<=n<=100),(1<=m<=1000)
第二行至第m+1行，每行3个整数a,b,x，代表车站a和车站b之间有一条票价为x的公交线路，公交线路是双向的。
```

**输出**

```
输出车站1到n的最小花费。
```

**样例输入**

```
4 4
1 2 4
2 3 7
2 4 1
3 4 6
```

**样例输出**

```
5
```

**解析**

**题目要求**

在带正权的无向图中，求从顶点 1 到顶点 n 的最短路径长度。若不可达，则输出 -1。

**解题思路**

本题为经典的单源最短路径问题，由于所有边权均为正数，适合使用 Dijkstra 算法求解。

Dijkstra 算法的核心思想是贪心策略：每次从未确定最短距离的顶点中选取距离最小的顶点，利用该顶点对其他顶点进行松弛操作。使用优先队列（小根堆）可以将选取最小距离顶点的操作优化至 O(log n)。

具体步骤：
1. 初始化距离数组 `d[]`，令 `d[1] = 0`，其余为无穷大。
2. 将起点 `(0, 1)` 入堆。
3. 每次取出堆顶元素 `(du, u)`，若 `du` 不等于 `d[u]` 则跳过（该记录已过时）；否则对 `u` 的所有邻接顶点进行松弛。
4. 最终 `d[n]` 即为答案；若仍为无穷大，说明不可达，输出 -1。

**算法分析**

- 时间复杂度：O((n + m) log n)，使用优先队列优化的 Dijkstra 算法。
- 空间复杂度：O(n + m)，用于存储图的邻接表和距离数组。

**注意事项**

- 两点之间可能存在多条边（重边），Dijkstra 算法天然能够正确处理此情况。
- 不可达时需输出 -1，注意判断条件。

**C++ 参考答案**

```cpp
#include <functional>
#include <iostream>
#include <queue>
#include <utility>
#include <vector>
using namespace std;
int main() {
    int n, m;
    cin >> n >> m;
    const int INF = 1e9;
    vector<vector<pair<int, int>>> g(n + 1);
    for (int i = 0, u, v, w; i < m; i++) {
        cin >> u >> v >> w;
        g[u].push_back({v, w});
        g[v].push_back({u, w});
    }
    vector<int> d(n + 1, INF);
    priority_queue<pair<int, int>, vector<pair<int, int>>, greater<pair<int, int>>> pq;
    d[1] = 0;
    pq.push({0, 1});
    while (!pq.empty()) {
        auto [du, u] = pq.top();
        pq.pop();
        if (du != d[u])
            continue;
        for (auto [v, w] : g[u])
            if (d[v] > du + w) {
                d[v] = du + w;
                pq.push({d[v], v});
            }
    }
    cout << (d[n] == INF ? -1 : d[n]);
}
```

## 119. 18734 拓扑排序

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18734&access=beaabf01c433ffaf2bdd96b40b5afdab&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
在经历.....之后，你打算好好学习下计算机专业的课程，避免面试过程中的各种尴尬场面。
计算机的专业课程间既有循序渐进的特点，相互间也存在着依赖关系（似乎其他专业也是这样......）。
现在给你n门课程和m个课程间关系，请给出一个有效的学习次序。
注意可能存在多门课程不依赖任何其他课程
```

**输入**

```
第一行有2个数，分别为课程数n和关系数m。     (1=<n<=20) (1=<m<=30)
接下来有m行，每一行有2个整数a和b，表示课程b依赖于课程a。(1=<a,b<=n)
```

**输出**

```
仅一行，一个整数序列，代表课程学习次序。
为确保输出唯一性，同等条件下，编号小的在排在前面。
```

**样例输入**

```
6 8
1 2
1 3
1 4
3 2
3 5
4 5
6 4
6 5
```

**样例输出**

```
1 3 2 6 4 5

Hint

图片来源于今日头条。
```

**解析**

**题目要求**

给定课程之间的依赖关系（有向无环图），求一个合法的拓扑排序序列。当存在多个入度为 0 的顶点时，编号较小者优先输出。

**解题思路**

采用 Kahn 算法（基于入度的拓扑排序）：

1. 统计每个顶点的入度。
2. 将所有入度为 0 的顶点放入一个**小根堆**（优先队列）中，以确保编号小的顶点优先被取出。
3. 每次从堆顶取出编号最小的顶点，将其加入结果序列，并将该顶点的所有后继顶点的入度减 1；若某后继顶点的入度减至 0，则将其入堆。
4. 重复步骤 3，直至堆为空。

**算法分析**

- 时间复杂度：O((n + m) log n)，每个顶点入堆、出堆各一次，优先队列操作的时间复杂度为 O(log n)。
- 空间复杂度：O(n + m)，用于存储图的邻接表、入度数组和优先队列。

**注意事项**

- 使用小根堆（而非普通队列）是本题的关键，它保证了在多个顶点同时满足入度为 0 的条件下，编号较小者被优先选取，从而确保输出序列的唯一性。
- 题目保证图为有向无环图（DAG），因此无需检测环的存在。

**C++ 参考答案**

```cpp
#include <functional>
#include <iostream>
#include <queue>
#include <vector>
using namespace std;
int main() {
    int n, m;
    cin >> n >> m;
    vector<vector<int>> g(n + 1);
    vector<int> in(n + 1);
    while (m--) {
        int a, b;
        cin >> a >> b;
        g[a].push_back(b);
        in[b]++;
    }
    priority_queue<int, vector<int>, greater<int>> q;
    for (int i = 1; i <= n; i++)
        if (!in[i])
            q.push(i);
    vector<int> ans;
    while (!q.empty()) {
        int u = q.top();
        q.pop();
        ans.push_back(u);
        for (int v : g[u])
            if (--in[v] == 0)
                q.push(v);
    }
    for (int i = 0; i < ans.size(); i++)
        cout << ans[i] << (i + 1 == ans.size() ? '\n' : ' ');
}
```

## 120. 18747 关键路径

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18747&access=efa7569f01098f40509573795e901cad&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
在一个工程项目里，多项工作可以同时进行。
我们可以用有向无环图表述项目流程，把项目中的事件表述为结点，把活动表述成有权值的边。
现在我们已知项目共有n个事件，起点为1，终点为n，m个活动。
请你计算出这个项目的最早完成时间，也就是起点到收点的最长路径，即关键路径。
```

**输入**

```
第一行两个整数n和m，代表结点数量和边数量。(1<=n,m<=100)
下面m行，每行3个整数a,b,x,表示点a到点b之间有一条长度为x的有向边。
```

**输出**

```
一个整数，起点到终点的最长路径.
```

**样例输入**

```
4 6
1 2 3
1 3 2
1 4 3
2 3 3
2 4 5
3 4 3
```

**样例输出**

```
9
```

**解析**

**题目要求**

在有向无环图（DAG）上求从起点 1 到终点 n 的最长路径（即关键路径的长度）。

**解题思路**

关键路径问题本质上是 DAG 上的最长路径问题。利用拓扑排序的序列顺序进行动态规划即可高效求解：

1. 对图执行拓扑排序，得到顶点的线性序列。
2. 初始化距离数组 `d[]`，令 `d[1] = 0`，其余为负无穷（表示不可达）。
3. 按照拓扑序依次处理每个顶点 `u`，对其每条出边 `(u, v, w)` 执行松弛操作：`d[v] = max(d[v], d[u] + w)`。
4. 最终 `d[n]` 即为从起点到终点的最长路径长度。

**算法分析**

- 时间复杂度：O(n + m)，拓扑排序与动态规划各遍历顶点和边各常数次。
- 空间复杂度：O(n + m)，用于存储图的邻接表和辅助数组。

**注意事项**

- 本题求的是最长路径，松弛条件与最短路相反，使用 `max` 而非 `min`。
- 距离数组应初始化为一个足够小的值（负无穷），以避免不可达顶点的错误更新。同时需注意防止溢出。
- 题目保证图为 DAG，因此无需检测环。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <queue>
#include <utility>
#include <vector>
using namespace std;
int main() {
    int n, m;
    cin >> n >> m;
    vector<vector<pair<int, int>>> g(n + 1);
    vector<int> in(n + 1);
    for (int i = 0, u, v, w; i < m; i++) {
        cin >> u >> v >> w;
        g[u].push_back({v, w});
        in[v]++;
    }
    queue<int> q;
    for (int i = 1; i <= n; i++)
        if (!in[i])
            q.push(i);
    const long long NEG_INF = -(1LL << 60);
    vector<long long> d(n + 1, NEG_INF);
    d[1] = 0;
    while (!q.empty()) {
        int u = q.front();
        q.pop();
        for (auto [v, w] : g[u]) {
            if (d[u] > NEG_INF / 2)
                d[v] = max(d[v], d[u] + w);
            if (--in[v] == 0)
                q.push(v);
        }
    }
    cout << d[n];
}
```

# 拓展习题7

## 121. 19085 图的存储结构（邻接表）

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19085&access=f9c2d7ae5178b3ee1377c63a8a8900bc&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
图的存储结构有四种：邻接矩阵，邻接表，十字链表，邻接多重表。
在实际写算法的时候，一般只是用邻接矩阵和邻接表这两种存储结构。
邻接矩阵用二维数组很容易实现，缺点是n^2的空间复杂度，适用于结点数较少或边数较多的稠密图。
邻接表只存储边的信息，但一般实操中不采用教材上提供的结构体指针法（比较繁琐，易错）
可用的替代方案包括链式前向星（使用静态链表）、vector法。
此处介绍实现起来比较简单的vector法，vector是C++提供的动态数组，用其存储图结构占用空间为图中边数量。
语句 vector<int>a  和int a[10]效果类似，但vector定义的数组a，其大小可变，即可以自由拓展存储空间。
语句 vector<int> e[100]则定义了一个100行的动态数组，类似于 e[100][],但其第二维大小可变。

具体解决方法如下图，第i行e[i]存储结点i的邻接点信息。
注意如果要存储的是边带权值的结构，需定义结构体来描述边，即采用vector<结构体>方式存储。
```

**输入**

```
第一行两个整数n和m，分别代表无向图的结点数量n（结点编号为1至n）和边数量m。n<=100000,m<=100000
后续m行，每行两个数字代表边的两个顶点。
```

**输出**

```
输出n行，每行第一个数字为结点，后续为结点的邻接点。
```

**样例输入**

```
5 6
1 2
3 1
2 4
2 5
3 4
5 4
```

**样例输出**

```
1:2 3
2:1 4 5
3:1 4
4:2 3 5
5:2 4
```

**解析**

**题目要求**

使用 `vector` 实现无向图的邻接表存储，并按指定格式输出每个顶点及其邻接点。

**解题思路**

对于无向图，每条边 `(u, v)` 需要同时记录在两个顶点的邻接表中：将 `v` 加入 `u` 的邻接表，将 `u` 加入 `v` 的邻接表。

构建完成后，按顶点编号从小到大依次输出。对于每个顶点的邻接点列表，需按升序排列后再输出，以满足样例的输出格式要求。

**算法分析**

- 时间复杂度：O(n + m log m)，其中构建邻接表为 O(m)，对每个顶点的邻接点排序的总开销为 O(m log m)。
- 空间复杂度：O(n + m)，邻接表存储所有边的信息（无向图每条边存储两次）。

**注意事项**

- 无向图的每条边需在两个方向上各添加一次。
- 输出前需对邻接点列表进行排序，否则输出顺序可能与样例不一致。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;
int main() {
    int n, m;
    cin >> n >> m;
    vector<vector<int>> g(n + 1);
    while (m--) {
        int u, v;
        cin >> u >> v;
        g[u].push_back(v);
        g[v].push_back(u);
    }
    for (int i = 1; i <= n; i++) {
        sort(g[i].begin(), g[i].end());
        cout << i << ":";
        for (int v : g[i])
            cout << v << ' ';
        cout << "\n";
    }
}
```

## 122. 19082 中位特征值

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19082&access=0a361502ba0000ccbc8889e776871618&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
【2022】贝壳找房秋招测试开发工程师笔试卷2

给你一棵以T为根，有n个节点的树。（n为奇数）每个点有一个价值V，并且每个点有一个特征值P。
每个点的特征值P为：以这个点为根的子树的所有点（包括根）的价值的和。
现在牛牛想知道这n个点对应的特征值的中位数是多少，你能告诉牛牛吗？
```

**输入**

```
第一行两个正整数，分别代表T和n。n<=1e5
接下来一行共n个正整数，分别代表编号为i的点的价值V[i]。V[i]<=1e9
接下来n-1行，每行两个正整数u,v，代表u和v之间有一条边相连。
```

**输出**

```
输出一行，共一个正整数，代表n个点特征值的中位数是多少。
```

**样例输入**

```
2 5
1 10 100 1000 10000
1 2
3 2
3 4
5 3
```

**样例输出**

```
10000

Hint

根据题意，2是树根，可以先画出这棵树理解题意。点1对应的特征值为1，点2对应的特征值为11111，
点3对应的特征值为11100，点4对应的特征值为1000，点5对应的特征值为10000，中位数是10000。
提示，数据范围为1e9，那么求和计算很可能超过int范围，因此数据定义时要使用long long 类型。
```

**解析**

**题目要求**

给定一棵以 T 为根、含 n 个结点的树（n 为奇数），每个结点有一个价值 V[i]。定义每个结点的特征值 P[i] 为以其为根的子树中所有结点的价值之和。求所有特征值的中位数。

**解题思路**

1. **计算特征值**：以 T 为根执行一次 DFS 后序遍历。对于每个结点 `u`，其特征值等于自身价值加上所有子结点特征值之和，即 `P[u] = V[u] + sum(P[v])`，其中 `v` 为 `u` 的子结点。
2. **求中位数**：收集所有 n 个特征值后，使用 `nth_element` 函数在 O(n) 时间内直接找到排序后位于第 `n/2` 位的元素（即中位数）。

**算法分析**

- 时间复杂度：O(n)，DFS 遍历树一次，`nth_element` 的平均时间复杂度为 O(n)。
- 空间复杂度：O(n)，用于存储树结构、特征值数组以及递归调用栈。

**注意事项**

- 单个结点的价值最大为 10^9，子树求和后可能超出 32 位整数范围，必须使用 `long long` 类型。
- 题目给定 n 为奇数，中位数即为排序后第 `(n+1)/2` 个元素（下标为 `n/2`）。
- DFS 时需记录父结点以避免回溯。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <functional>
#include <iostream>
#include <vector>
using namespace std;
int main() {
    ios::sync_with_stdio(false);
    cin.tie(nullptr);
    int T, n;
    cin >> T >> n;
    vector<long long> val(n + 1), sum(n + 1);
    for (int i = 1; i <= n; i++)
        cin >> val[i];
    vector<vector<int>> g(n + 1);
    for (int i = 1, u, v; i < n; i++) {
        cin >> u >> v;
        g[u].push_back(v);
        g[v].push_back(u);
    }
    vector<long long> all;
    function<void(int, int)> dfs = [&](int u, int p) {
        sum[u] = val[u];
        for (int v : g[u])
            if (v != p) {
                dfs(v, u);
                sum[u] += sum[v];
            }
        all.push_back(sum[u]);
    };
    dfs(T, 0);
    nth_element(all.begin(), all.begin() + n / 2, all.end());
    cout << all[n / 2];
}
```

## 123. 19031 树的重心

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19031&access=681a95520ff12ed81fa88cf2f13fcba1&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
军营选择（腾讯音乐娱乐（TME）2021暑期实习生招聘技术类笔试（II） ）

牛牛是一名新晋营长，需要选择军营建造地点，已知一共有N个候选地，编号为1-N，有N-1条道路，使得这N个候选地之间两两可以到达。
军营选择规则如下：
对于其中一个候选地i而言，如果将该地以及其直接相连的道路全都删除，就可以得到若干个连通块，用wi记录下其中的最大连通块中的候选地数量。
对于所有的满足wk=min(w1,w2.....wn)的候选地k而言，都是最佳军营建造地。
由于最佳地点可能不止一个，所以牛牛想要通过一些操作将该地点唯一化......
对此题目感兴趣同学，可以去牛客网查看原题或百度。

本题目只要求计算出树的重心。
树的重心也叫树的质心。找到一个点,其所有的子树中最大的子树结点数最少,
那么这个点就是这棵树的重心,删去重心后，生成的多棵树尽可能平衡。
树的重心最多有2个。
例如3个结点的树，有两条边<1,2><2,3>，那么树的重心是2。因为删除2后，剩余的最大子树结点数为1，而删除1或3最大子树结点数为2。
树的重心对任意结点使用一次DFS即可得到，复杂度为O(n)。
```

**输入**

```
第一行输入一个正整数N ，代表树的结点数量，编号为1-N。(3<=N<=100000)。

接下去N-1行，每行两个正整数u,v，代表节点u和v 间存在一条无向边。

数据保证树的任意两点连通。
```

**输出**

```
输出树的重心结点编号。
如果重心有两个，先输出结点编号小的。
```

**样例输入**

```
4
1 2
1 3
4 3
```

**样例输出**

```
1 3

Hint

题目数据量较大，建议使用scanf读取数据。
```

**解析**

**题目要求**

给定一棵含 N 个结点的树，求其重心。若重心有两个，按编号从小到大输出。

**解题思路**

树的重心定义：删除该结点后，所产生的各个连通块中最大连通块的结点数最小。

对于树中任意结点 `u`，删除 `u` 后会产生若干连通块：
- `u` 的每棵子树各自构成一个连通块，大小分别为 `sz[v]`（`v` 为 `u` 的子结点）。
- 剩余部分（`u` 的父结点方向）构成一个连通块，大小为 `N - sz[u]`。

因此，删除结点 `u` 后最大连通块的大小为 `max(max(sz[v]), N - sz[u])`。

通过一次 DFS 即可同时计算所有结点的子树大小，并记录每个结点对应的最大连通块大小，取最小值对应的结点即为重心。

**算法分析**

- 时间复杂度：O(N)，仅需一次 DFS 遍历。
- 空间复杂度：O(N)，用于存储树结构和子树大小数组。

**注意事项**

- 树的重心最多有两个，当两个重心的最大连通块大小相同时，均需输出。
- 输出时需按编号从小到大排列。
- 数据量较大（N 可达 10^5），建议使用快速的输入方式。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <functional>
#include <iostream>
#include <vector>
using namespace std;
int main() {
    int n;
    cin >> n;
    vector<vector<int>> g(n + 1);
    for (int i = 1, u, v; i < n; i++) {
        cin >> u >> v;
        g[u].push_back(v);
        g[v].push_back(u);
    }
    vector<int> sz(n + 1), ans;
    int best = n;
    function<void(int, int)> dfs = [&](int u, int p) {
        sz[u] = 1;
        int mx = 0;
        for (int v : g[u])
            if (v != p) {
                dfs(v, u);
                sz[u] += sz[v];
                mx = max(mx, sz[v]);
            }
        mx = max(mx, n - sz[u]);
        if (mx < best) {
            best = mx;
            ans.clear();
            ans.push_back(u);
        } else if (mx == best)
            ans.push_back(u);
    };
    dfs(1, 0);
    sort(ans.begin(), ans.end());
    for (int i = 0; i < ans.size(); i++)
        cout << ans[i] << (i + 1 == ans.size() ? '\n' : ' ');
}
```

## 124. 19011 小猿的依赖循环

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19011&access=5b648251948b9dc34bb4ff0397d15949&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
猿辅导2021校园招聘笔试（算法二）
小猿在加载一个网页，这个网页共需要N个相关资源，这些资源之间有一些依赖关系。
如果这些资源中存在循环依赖，我们认为这个网页不能加载成功，否则可以加载成功。
存在循环依赖是指，这些资源中存在资源X，X依赖的资源Y直接或间接依赖于X。
你能帮助小猿判断一下这个网页能否加载成功吗？
```

**输入**

```
第一行输入T（T <= 10），表示输入T组数据。
每组数据第1行，输入一个数N（1 <= N <= 500）表示该组case有编号为1~N的N项资源。
每组数据第2到 N+1 行，输入一个 N*N 的零一矩阵。
矩阵第 i 行第 j 列数字为 a[i][j] 表示编号为 i 的资源是否依赖于编号为 j 的资源，1表示依赖，0表示不依赖。数据保证a[i][i] = 0。
```

**输出**

```
输出包含T行，每行输出对应每组case中是否存在循环依赖。存在输出1，不存在输出0。
```

**样例输入**

```
2
3
0 1 0
0 0 1
1 0 0
3
0 1 0
0 0 0
0 0 0
```

**样例输出**

```
1
0

Hint

第一组数据：1依赖于2，2依赖于3，3依赖于1，存在循环依赖。第二组数据：只有1依赖于2，不存在循环依赖。
提示：既然是有向无环图，做一下拓扑排序看看能不能输出n个数字，不能就是有环存在。
```

**解析**

**题目要求**

给定 N 个资源之间的依赖关系（以邻接矩阵形式给出），判断是否存在循环依赖。若存在循环依赖则输出 1，否则输出 0。

**解题思路**

资源之间的依赖关系可以自然地建模为有向图：若资源 `i` 依赖资源 `j`，则存在一条从 `j` 到 `i` 的有向边（表示 `j` 必须先于 `i` 被加载）。

判断有向图中是否存在环，等价于对该图执行拓扑排序，检查能否将所有顶点排入序列：
- 若拓扑排序的结果包含全部 N 个顶点，则图无环，即不存在循环依赖。
- 若拓扑排序的结果少于 N 个顶点，则图中存在环，即存在循环依赖。

具体实现时，先根据邻接矩阵构建邻接表并统计入度，然后使用 Kahn 算法进行拓扑排序。

**算法分析**

- 时间复杂度：O(N^2)，读取邻接矩阵需要 O(N^2) 的时间，拓扑排序为 O(N + E)，其中 E <= N^2。
- 空间复杂度：O(N^2)，用于存储图的邻接表。

**注意事项**

- 输入矩阵中 `a[i][j] = 1` 表示 `i` 依赖 `j`，因此有向边的方向为 `j -> i`（`j` 是 `i` 的前驱），构建邻接表时需注意方向。
- 本题有多组测试数据，每组数据需重新初始化图结构。

**C++ 参考答案**

```cpp
#include <iostream>
#include <queue>
#include <vector>
using namespace std;
int main() {
    int T;
    cin >> T;
    while (T--) {
        int n;
        cin >> n;
        vector<vector<int>> g(n);
        vector<int> in(n);
        for (int i = 0; i < n; i++)
            for (int j = 0, x; j < n; j++) {
                cin >> x;
                if (x) {
                    g[j].push_back(i);
                    in[i]++;
                }
            }
        queue<int> q;
        for (int i = 0; i < n; i++)
            if (!in[i])
                q.push(i);
        int cnt = 0;
        while (!q.empty()) {
            int u = q.front();
            q.pop();
            cnt++;
            for (int v : g[u])
                if (--in[v] == 0)
                    q.push(v);
        }
        cout << (cnt == n ? 0 : 1) << "\n";
    }
}
```

## 125. 19017 编译依赖问题(拓扑排序）

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19017&access=6d6f1fd5c68a43005a7186d2444a2e0d&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
vivo2021届秋季校招在线编程
一个完整的软件项目往往会包含很多由代码和文档组成的源文件。编译器在编译整个项目的时候，可能需要按照依赖关系来依次编译每个源文件。
比如，A.cpp 依赖 B.cpp，那么在编译的时候，编译器需要先编译 B.cpp，才能再编译 A.cpp。
 假设现有 0，1，2，3 四个文件，0号文件依赖1号文件，1号文件依赖2号文件，3号文件依赖1号文件，则源文件的编译顺序为 2,1,0,3 或 2,1,3,0。
现给出文件依赖关系，如 1,2,-1,1，表示0号文件依赖1号文件，1号文件依赖2号文件，2号文件没有依赖，3号文件依赖1号文件。
请补充完整程序，返回正确的编译顺序。注意如有同时可以编译多个文件的情况，
按数字升序返回一种情况即可（简单说就是选择序号最小的），比如前述案例输出为：2,1,0,3
```

**输入**

```
一个字符串，代表要编译的文件依赖关系。文件编号小于100。
```

**输出**

```
一个序列，代表编译顺序，两个数字间用空格分隔。
```

**样例输入**

```
1,2,-1,1
```

**样例输出**

```
2,1,0,3

Hint

按原题要求，输入序列是一个字符串，输出序列也是一个字符串形式。
```

**解析**

**题目要求**

给定一组文件的依赖关系（以一维数组形式表示），求合法的编译顺序。当多个文件可同时编译时，编号较小者优先。

**解题思路**

输入格式为逗号分隔的整数序列 `dep[]`，其中 `dep[i]` 表示文件 `i` 所依赖的文件编号，`-1` 表示无依赖。

依赖关系可建模为有向图：若文件 `i` 依赖文件 `dep[i]`，则存在一条从 `dep[i]` 到 `i` 的有向边，表示 `dep[i]` 必须先于 `i` 被编译。

在构建好有向图后，使用 Kahn 算法进行拓扑排序。为保证同等条件下编号较小者优先，使用**小根堆**（优先队列）替代普通队列。

**算法分析**

- 时间复杂度：O(n log n)，其中 n 为文件数量。拓扑排序中使用优先队列维护入度为 0 的顶点。
- 空间复杂度：O(n)，用于存储图和入度数组。

**注意事项**

- 输入为字符串格式，需正确解析逗号分隔的整数（包括负数 `-1`）。
- 输出格式为逗号分隔的整数序列，与输入的格式对应。
- 题目保证不存在循环依赖，因此拓扑排序一定能处理所有文件。

**C++ 参考答案**

```cpp
#include <ctype.h>
#include <functional>
#include <iostream>
#include <queue>
#include <string>
#include <vector>
using namespace std;
int main() {
    string s;
    cin >> s;
    vector<int> dep;
    for (int i = 0; i < s.size();) {
        int sign = 1;
        if (s[i] == '-')
            sign = -1, i++;
        int v = 0;
        while (i < s.size() && isdigit((unsigned char)s[i]))
            v = v * 10 + s[i++] - '0';
        dep.push_back(sign * v);
        if (i < s.size() && s[i] == ',')
            i++;
    }
    int n = dep.size();
    vector<vector<int>> g(n);
    vector<int> in(n);
    for (int i = 0; i < n; i++)
        if (dep[i] != -1) {
            g[dep[i]].push_back(i);
            in[i]++;
        }
    priority_queue<int, vector<int>, greater<int>> q;
    for (int i = 0; i < n; i++)
        if (!in[i])
            q.push(i);
    vector<int> ans;
    while (!q.empty()) {
        int u = q.top();
        q.pop();
        ans.push_back(u);
        for (int v : g[u])
            if (--in[v] == 0)
                q.push(v);
    }
    for (int i = 0; i < ans.size(); i++) {
        if (i)
            cout << ',';
        cout << ans[i];
    }
}
```

## 126. 19032 树上上升序列

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19032&access=f634641a5c6c6c635c3f43cdfa15bfd3&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
百度2020校招Java研发工程师笔试卷（第三批）

度度熊给定一棵树，树上的第i个节点有点权a[i]。请你找出一条最长的路径(u,v)，使得从u沿着唯一路径走到v的途中，点权不断严格递增。

换句话说，设路径为(u,p1,p2,p3......pm,v)，则需要满足a[u]<a[p1]<a[p2]<......<a[pm]<a[v]。输出最长满足条件的路径的长度。
```

**输入**

```
第一行树的节点个数n , 接下来一行n个数字，表示每个点的点权a[i]。1<=n<=100000,1<=a[i]<=n。

接下来n-1行，每行两个数u,v代表树上的点u和v存在一条边。1<=u，v<=n。
```

**输出**

```
一行一个数字表示答案，即最长的长度。
```

**样例输入**

```
5
3 4 5 4 5
1 2
1 3
2 4
2 5
```

**样例输出**

```
3

Hint

样例解释,最长的路径为3，路径序列<1,2,5>。
由于只能从点权小向大走，那么实际上是一个有向图，同时树结构是不存在环的，那么就是有向无环图。
有向无环图对应两种算法，边无权值拓扑排序，有权值关键（最长）路径，关键路径和拓扑排序采用的是同一种动态规划的处理方法。
此题目是关键（最长）路径问题。
```

**解析**

**题目要求**

给定一棵树，每个结点有一个点权。求树上一条最长的严格递增路径（路径上结点的点权严格单调递增）。路径长度定义为路径上结点的个数。

**解题思路**

由于路径要求严格递增，可以将树上的无向边按照点权大小定向为有向边：对于边 `(u, v)`，若 `a[u] < a[v]`，则建立有向边 `u -> v`；若 `a[v] < a[u]`，则建立有向边 `v -> u`；若 `a[u] == a[v]`，则不建立边（因为不满足严格递增）。

由于树本身不存在环，定向后得到的有向图必然是有向无环图（DAG）。因此，问题转化为在 DAG 上求最长路径，可使用基于拓扑排序的动态规划方法：

1. 对 DAG 执行拓扑排序。
2. 维护 `dp[v]` 表示以顶点 `v` 结尾的最长递增路径长度，初始值为 1。
3. 按照拓扑序处理每个顶点 `u`，对其每条出边 `(u, v)` 执行转移：`dp[v] = max(dp[v], dp[u] + 1)`。
4. 所有 `dp` 值的最大值即为答案。

**算法分析**

- 时间复杂度：O(n)，构建 DAG 和拓扑排序各遍历顶点和边各常数次。
- 空间复杂度：O(n)，用于存储 DAG、入度数组和 DP 数组。

**注意事项**

- 点权相等时不建立有向边，因为题目要求严格递增。
- 路径长度定义为结点个数（而非边数），因此 `dp` 初始值为 1。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <iostream>
#include <queue>
#include <vector>
using namespace std;
int main() {
    int n;
    cin >> n;
    vector<int> a(n + 1);
    for (int i = 1; i <= n; i++)
        cin >> a[i];
    vector<vector<int>> dag(n + 1);
    vector<int> in(n + 1), dp(n + 1, 1);
    for (int i = 1, u, v; i < n; i++) {
        cin >> u >> v;
        if (a[u] < a[v])
            dag[u].push_back(v), in[v]++;
        else if (a[v] < a[u])
            dag[v].push_back(u), in[u]++;
    }
    queue<int> q;
    for (int i = 1; i <= n; i++)
        if (!in[i])
            q.push(i);
    int ans = 1;
    while (!q.empty()) {
        int u = q.front();
        q.pop();
        ans = max(ans, dp[u]);
        for (int v : dag[u]) {
            dp[v] = max(dp[v], dp[u] + 1);
            if (--in[v] == 0)
                q.push(v);
        }
    }
    cout << ans;
}
```

## 127. 18733 排队

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18733&access=6a8d3837b1dc310d8efa7ae082c363eb&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
操场上有好多好多同学在玩耍，体育老师冲了过来，要求他们排队。同学们纪律实在太散漫了，老师不得不来手动整队：
"A，你站在B的后面。"
"C，你站在D的后面。"
"B，你站在D的后面。哦，去D队伍的最后面。"

更形式化地，初始时刻，操场上有 n 位同学，自成一列。每次操作，老师的指令是 "x y"，表示 x 所在的队列排到 y 所在的队列的后面，
即 x 的队首排在 y 的队尾的后面。（如果 x 与 y 已经在同一队列，请忽略该指令） 最终的队列数量远远小于 n，老师很满意。
请你输出最终时刻每位同学所在队列的队首（排头），老师想记录每位同学的排头，方便找人。
```

**输入**

```
第一行两个整数 n 和 m (n,m<=30000)，紧跟着 m 行每行两个整数
x 和 y (1<=x,y<=n)。
```

**输出**

```
仅一行 n 个整数，表示每位同学所在队列排头同学的编号。
```

**样例输入**

```
5 4
1 2
2 3
4 5
1 3
```

**样例输出**

```
3 3 3 5 5

Hint

并查集
题目来源于http://openjudge.cn/
某大学数据结构与算法期末考试的第一题
```

**解析**

**题目要求**

初始时 n 位同学各自独立成队。每次指令 "x y" 表示将 x 所在的整个队列合并到 y 所在队列的末尾。求最终每位同学所在队列的队首编号。

**解题思路**

本题的核心操作是集合的合并与查询，适合使用**并查集**数据结构。

每次合并操作将 x 所在集合与 y 所在集合合并。由于题目仅关心每个集合的队首（排头），因此需要额外维护每个集合的队首信息：合并时，新集合的队首为 y 所在集合的队首（因为 x 的队列接在 y 的队列后面）。

实现要点：
- 使用路径压缩优化并查集的查找操作。
- 使用 `head[]` 数组记录每个集合的队首。合并时，将 x 所在集合的根指向 y 所在集合的根，并保持 y 集合的队首不变。

**算法分析**

- 时间复杂度：O(m * alpha(n) + n)，其中 alpha 为反阿克曼函数，近似为常数。m 次合并操作加上最终 n 次查询。
- 空间复杂度：O(n)，用于并查集数组和队首数组。

**注意事项**

- 若 x 和 y 已在同一队列中，应忽略该指令，避免重复合并。
- 合并时需注意方向：x 的队列接在 y 的队列后面，因此合并后队首应为 y 所在队列的队首。

**C++ 参考答案**

```cpp
#include <functional>
#include <iostream>
#include <vector>
using namespace std;
int main() {
    int n, m;
    cin >> n >> m;
    vector<int> par(n + 1), head(n + 1), tail(n + 1);
    for (int i = 0; i < (int)par.size(); i++)
        par[i] = i;
    for (int i = 0; i < (int)head.size(); i++)
        head[i] = i;
    for (int i = 0; i < (int)tail.size(); i++)
        tail[i] = i;
    function<int(int)> f = [&](int x) { return par[x] == x ? x : par[x] = f(par[x]); };
    while (m--) {
        int x, y;
        cin >> x >> y;
        int rx = f(x), ry = f(y);
        if (rx == ry)
            continue;
        par[rx] = ry;
        head[ry] = head[ry];
    }
    for (int i = 1; i <= n; i++)
        cout << head[f(i)] << (i == n ? '\n' : ' ');
}
```

## 128. 18945 小团的配送团队

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=18945&access=dff337ee9e42729935de0e60f79dd07b&fixedLanguage=MDsx
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC

**题目描述**

```
美团2021校招笔试-编程题(通用编程试题,第2场)

小团是美团外卖的区域配送负责人，众所周知，外卖小哥一般都会同时配送若干单，
小团在接单时希望把同一个小区的单子放在一起，然后由一名骑手统一配送。
但是由于订单是叠在一起的，所以，他归类订单时只能知道新订单和已有的某个订单的小区是相同的，
他觉得这样太麻烦了，所以希望你帮他写一个程序解决这个问题。
即给出若干个形如a b的关系，表示a号订单和b号订单是同一个小区的 ，
请你把同一个小区的订单按照编号顺序排序，并分行输出，优先输出最小的订单编号较小的小区订单集合。
订单的编号是1到n。(可能存在同时出现a b和b a这样的关系,也有可能出现a a这样的关系)
```

**输入**

```
输入第一行是两个正整数n，m，表示接受的订单数量和已知的关系数量。(1<=n，m<=10000)
接下来有m行，每行两个正整数a和b，表示a号订单和b号订单属于同一个小区(1<=a,b<=n)，
a，b可能相同，也可能出现重复的关系
```

**输出**

```
输出第一行包含一个整数x，表示这些订单共来自x个不同的小区。
接下来的输出包含x行，每行表示输出若干个订单编号，表示这些订单属于同一个小区，按照订单编号升序输出。优先输出最小的订单编号较小的小区。
```

**样例输入**

```
5 5
1 2
2 2
3 1
4 2
5 4
```

**样例输出**

```
1
1 2 3 4 5
```

**解析**

**题目要求**

给定 n 个订单和 m 条"同小区"关系，将所有属于同一小区的订单归组。每组内按编号升序排列，各组按最小编号升序输出。

**解题思路**

"同小区"关系具有传递性：若订单 a 与订单 b 同小区，订单 b 与订单 c 同小区，则订单 a 与订单 c 也同小区。这恰好是**等价关系**的特征，适合使用并查集来维护。

具体步骤：
1. 使用并查集将所有具有"同小区"关系的订单合并到同一集合中。
2. 遍历所有订单，按所属集合（根结点）进行分组。
3. 对每个集合内的订单按编号升序排列。
4. 将各集合按其最小订单编号升序排列后输出。

**算法分析**

- 时间复杂度：O(n log n + m * alpha(n))，并查集操作近似常数，排序为主要开销。
- 空间复杂度：O(n)，用于并查集和分组存储。

**注意事项**

- 输入可能存在 `a = b` 的关系（自身与自身同小区）以及重复的关系，这些情况并查集均可正确处理，无需特殊判断。
- 使用 `map` 按根结点分组时，`map` 本身按键有序，但最终需按各组的最小编号排序，而非按根结点编号排序。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <functional>
#include <iostream>
#include <map>
#include <vector>
using namespace std;
int main() {
    int n, m;
    cin >> n >> m;
    vector<int> p(n + 1);
    for (int i = 0; i < (int)p.size(); i++)
        p[i] = i;
    function<int(int)> f = [&](int x) { return p[x] == x ? x : p[x] = f(p[x]); };
    while (m--) {
        int a, b;
        cin >> a >> b;
        p[f(a)] = f(b);
    }
    map<int, vector<int>> mp;
    for (int i = 1; i <= n; i++)
        mp[f(i)].push_back(i);
    vector<vector<int>> groups;
    for (auto &[r, v] : mp) {
        sort(v.begin(), v.end());
        groups.push_back(v);
    }
    sort(groups.begin(), groups.end(), [](auto &a, auto &b) { return a[0] < b[0]; });
    cout << groups.size() << "\n";
    for (auto &v : groups) {
        for (int i = 0; i < v.size(); i++)
            cout << v[i] << (i + 1 == v.size() ? '\n' : ' ');
    }
}
```

## 129. 19049 仓库配送

- 原题链接：https://acm.scau.edu.cn/uoj8000/common_problem_view_PUBLIC.html?problemId=19049&access=140c4c51056d96fe14327d46b7fb1d45&fixedLanguage=
- Time Limit: 1000MS  Size Limit:10KB；Size Limit: 10KB；Language: G++;GCC;VC;JAVA;PYTHON

**题目描述**

```
网易2021校招笔试-算法工程师（正式第二批）

网易严选建有N个自营仓分布在全国各地，标记为仓库1到N。
给定一个配货时间组（v,u,w)，v为出发仓库，u为目标仓库，w为从出发仓库到目标仓库的耗时时间。
可能存在仓库间过远，无法支持调拨转货。
指定一个出发仓库K，我们需要将供应商发送到K仓库的货配送到各个仓库。
问配送到所有可到达仓库所要最短时间？如果无法全部调拨到，则返回-1.
```

**输入**

```
第一行三个正整数，由空格分割，分别表示仓库个数N，出发仓K，以及配送时间组个数M
接下来 M行，每行三个整数，由空格分割，分别表示（v,u,w)三个数，v为出发仓库，u为目标仓库，w为从出发仓库到目标仓库的耗时时间
1<=N<=30
1<=K<=N
1<=M<=130
1<=u,v<=N
1<=w<=20
```

**输出**

```
一行一个数字表示答案，配送到所有可达仓库到最短时间，如果无法送达全部仓库，输出-1。
```

**样例输入**

```
6 2 5
2 1 1
2 6 2
1 3 3
3 4 1
6 5 2
```

**样例输出**

```
5

Hint

这是一道模板题。
```

**解析**

**题目要求**

给定一个有向带权图和出发仓库 K，求从 K 到所有其他仓库的最短配送时间。若存在不可达的仓库，则输出 -1；若全部可达，则输出所有最短时间中的最大值。

**解题思路**

本题为标准的单源最短路径问题，使用 Dijkstra 算法求解。

由于配送是有方向的（从出发仓 v 到目标仓 u），因此图为有向图。从出发仓 K 出发，利用 Dijkstra 算法计算出到所有仓库的最短时间。

算法完成后，检查所有仓库的最短距离：
- 若任一仓库的最短距离仍为无穷大，说明该仓库不可达，输出 -1。
- 若所有仓库均可达，则答案为所有最短距离中的最大值（因为所有仓库都需要被配送，最终完成时间取决于最晚到达的仓库）。

**算法分析**

- 时间复杂度：O((N + M) log N)，使用优先队列优化的 Dijkstra 算法。
- 空间复杂度：O(N + M)，用于存储图的邻接表和距离数组。

**注意事项**

- 本题的配送方向为有向的，即 `(v, u, w)` 表示从 v 到 u 的单向路径，不可反向通行。
- 最终答案为所有最短距离的最大值而非总和，因为各仓库的配送可以并行进行。
- 仓库总数 N 较小（N <= 30），使用 Dijkstra 算法绰绰有余。

**C++ 参考答案**

```cpp
#include <algorithm>
#include <functional>
#include <iostream>
#include <queue>
#include <utility>
#include <vector>
using namespace std;
int main() {
    int N, K, M;
    cin >> N >> K >> M;
    vector<vector<pair<int, int>>> g(N + 1);
    for (int i = 0, v, u, w; i < M; i++) {
        cin >> v >> u >> w;
        g[v].push_back({u, w});
    }
    const int INF = 1e9;
    vector<int> d(N + 1, INF);
    priority_queue<pair<int, int>, vector<pair<int, int>>, greater<pair<int, int>>> pq;
    d[K] = 0;
    pq.push({0, K});
    while (!pq.empty()) {
        auto [du, u] = pq.top();
        pq.pop();
        if (du != d[u])
            continue;
        for (auto [v, w] : g[u])
            if (d[v] > du + w) {
                d[v] = du + w;
                pq.push({d[v], v});
            }
    }
    int ans = 0;
    for (int i = 1; i <= N; i++) {
        if (d[i] == INF) {
            cout << -1;
            return 0;
        }
        ans = max(ans, d[i]);
    }
    cout << ans;
}
```
**邪修做法（可过 OJ）**

由于 N <= 30，直接 Floyd 全源最短路也很省事，不需要优先队列。

~~~cpp
#include <algorithm>
#include <iostream>
#include <vector>
using namespace std;

int main() {
    int n, k, m;
    cin >> n >> k >> m;
    const int INF = 1000000000;
    vector<vector<int>> d(n + 1, vector<int>(n + 1, INF));
    for (int i = 1; i <= n; i++)
        d[i][i] = 0;
    while (m--) {
        int u, v, w;
        cin >> u >> v >> w;
        d[u][v] = min(d[u][v], w);
    }
    for (int t = 1; t <= n; t++)
        for (int i = 1; i <= n; i++)
            for (int j = 1; j <= n; j++)
                if (d[i][t] < INF && d[t][j] < INF)
                    d[i][j] = min(d[i][j], d[i][t] + d[t][j]);
    int ans = 0;
    for (int i = 1; i <= n; i++) {
        if (d[k][i] == INF) {
            cout << -1;
            return 0;
        }
        ans = max(ans, d[k][i]);
    }
    cout << ans;
}
~~~
