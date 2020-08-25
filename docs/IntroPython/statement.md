---
layout: default
title: 程序控制结构
parent: Python基础
nav_order: 4
---

# 程序控制结构
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

### 顺序结构

Python代码的运行先后顺序遵循由上到下的顺序，这种程序运行结构，我们成为顺序结构。

```python
x = 3
x += 2
print(x)
y = 6
import numpy as np
m1 = np.matrix([[1, 0], [0, 1]])  # 先导入再使用
```

### 分支语句

分支语句是建立在我们之前关系运算符之上的。

```python
x, y = 7, 5
if x > y:
	print('x 大于 y')  #  x 大于 y

# any non-zero value
if -3:
  print('True')  # Prints True

# mathematical expression
x, y = 7, 5
if x + y:
  print('True')  # Prints True

# nonempty container
L = ['red','green']
if L:
  print('True')  # Prints True

x, y = 7, 5
if x < y:
  print('y is greater')
else:
  print('x is greater')  # Prints x is greater

x, y = 5, 5
if x > y:
  print('x is greater')
elif x < y:
  print('y is greater')
else:
  print('x and y are equal')
```

### 循环语句

循环语句对于第一次接触的学员来说，可能需要多做几个练习来熟练, 我们以一个案例穿插整个讲解。下面是某一个班级的成绩统计，我们根据不同的情况，经常需要:
- 逐个打印每位同学的数学成绩
- 修改特定同学成绩(数据较多，不知道其具体的位置)
- 除去某位同学，修改余下所有学生的成绩

| 序号 | 中文姓名 | 英文姓名 | 语文 | 数学 | 英文 |
|------|:--------:|:--------:|:----:|:----:|:----:|
|   1  |  李飞飞  |   Lucy   |  98  |  85  |  96  |
|   2  |  刘泰宇  |   David  |  87  |  93  |  92  |
|   3  |  王云逸  |  Michael |  90  |  91  |  93  |
|   4  |  陈小帅  |    Leo   |  69  |  89  |  88  |
|   5  |  董明翔  |   Emmet  |  83  |  93  |  87  |
