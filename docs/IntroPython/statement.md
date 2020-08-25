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

### for 循环语句

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


```python
name_english = ["Lucy", "David", "Michael", "Leo", "Emmet"]
for i in name_english:
    print(i)

# Lucy
# David
# Michael
# Leo
# Emmet

grade_mandarin = [98, 87, 90, 69, 83]
for gd in grade_mandarin:
    if gd >= 90:
        print("成绩优秀")
    elif gd >= 80:
        print("成绩良好")
    else:
        print("不及格或成绩一般")

# 成绩优秀
# 成绩良好
# 成绩优秀
# 不及格或成绩一般
# 成绩良好
```

循环语句只有在存在可迭代对象时才可以使用，以下就是常见的可迭代对象。

|     可迭代对象    |                           说明                           |
|:-----------------:|:--------------------------------------------------------:|
|    字符串string   | <for var in "string":>                                     |
|      列表list     | for var in [0, 1, "hello"]:                              |
|      字典dict     | for key, value in {"Michael": 90, "Marion": 80}.items(): |
|                   | for key in {"Michael": 80, "Marion": 90}.keys():         |
|                   | for value in {"Michael": 60, "Marion": 80}.values():     |
|     元组tuple     | for t in (10, 12):                                       |
|   索引函数range   | for i in range(6):                                       |
| 索引函数enumerate | for index, var in enumerate("string"):                   |

这里要特别讲一下range()函数，当我们已知遍历的次数，但是无法从原有可迭代数据提取数字索引值时，我们可以使用range()
函数:
```python
for i in range(4):
    print(i)
# 0
# 1
# 2
# 3
```

### for 循环中的continue, break

在遍历所有内容时，我们经常需要根据不同的情况跳出或者终止循环，比如Leo的语文成绩错误，需要单独修改他的语文成绩。

| 序号 | 中文姓名 | 英文姓名 | 语文 | 数学 | 英文 |
|------|:--------:|:--------:|:----:|:----:|:----:|
|   1  |  李飞飞  |   Lucy   |  98  |  85  |  96  |
|   2  |  刘泰宇  |   David  |  87  |  93  |  92  |
|   3  |  王云逸  |  Michael |  90  |  91  |  93  |
|   4  |  陈小帅  |    <span style="color:red;">Leo</span>   |  <span style="color:red;">69</span> |  89  |  88  |
|   5  |  董明翔  |   Emmet  |  83  |  93  |  87  |

```python
name_english = ["Lucy", "David", "Michael", "Leo", "Emmet"]
grade_mandarin = [98, 87, 90, 69, 83]
for nm in range(len(name_english)):
    print(nm)
    print(name_english[nm])
    print(grade_mandarin[nm])
    if name_english[nm] == "Leo":
        grade_mandarin[nm] = 79
        break
print(grade_mandarin)  # [98, 87, 90, 79, 83]
# 0
# Lucy
# 98
# 1
# David
# 87
# 2
# Michael
# 90
# 3
# Leo
# 69
```

现在我们考虑另外一种情况，只有Leo的语文成绩没错，其它的都错了。

| 序号 | 中文姓名 | 英文姓名 | 语文 | 数学 | 英文 |
|------|:--------:|:--------:|:----:|:----:|:----:|
|   1  |  李飞飞  |    <span style="color:red;">Lucy</span>  |   <span style="color:red;">98</span> |  85  |  96  |
|   2  |  刘泰宇  |    <span style="color:red;">David</span> |   <span style="color:red;">87</span>  |  93  |  92  |
|   3  |  王云逸  |   <span style="color:red;">Michael</span> |   <span style="color:red;">90</span>  |  91  |  93  |
|   4  |  陈小帅  |   Leo   |  <span style="color:red;">69</span> |  69  |  88  |
|   5  |  董明翔  |    <span style="color:red;">Emmet</span> |   <span style="color:red;">83</span>  |  93  |  87  |

```python
name_english = ["Lucy", "David", "Michael", "Leo", "Emmet"]
grade_mandarin = [98, 87, 90, 69, 83]
grade_yuwen = [100, 100, 100, 100, 100]
for nm in range(len(name_english)):
    print(nm)
    print(name_english[nm])
    if name_english[nm] == "Leo":
        continue
    grade_mandarin[nm] = grade_yuwen[nm]
    print(grade_mandarin[nm]) # [100, 100, 100, 69, 100]

# 0
# Lucy
# 100
# 1
# David
# 100
# 2
# Michael
# 100
# 3
# Leo
# 4
# Emmet
# 100
```

### while 循环

与 for 循环不同，while 循环需要设置初始条件，并且以此来验证循环是否继续。因为while循环时条件判定循环，所有经常在人工智能中用来:
- 判定损失函数差值小于容错值时来结束循环
- 循环次数大于某个特定值时来介绍循环

```python
name_english = ["Lucy", "David", "Michael", "Leo", "Emmet"]
i = 0  # 设置初始条件
while i < len(name_english):
    print(i)
    print(name_english[i])
    i = i + 1

i = 0
error = 1.0
while error > 0.003:
  error -= 0.00001
  i += 1

print(i)
```

最后给出for循环和while循环的对比:

|          |             for             |           while           |
|----------|:---------------------------:|:-------------------------:|
| 初始条件 |           可有可无          |       多数情况下需要      |
| 进入循环 |      for i in iterable:     |        while True:        |
| 循环次数 |             固定            |       由判定条件决定      |
| 相关函数 |            break            |           break           |
|          |           continue          |          continue         |
|          |             pass            |            pass           |
| 如何选择 | 已知可迭代对象的长度优选for | 条件判定下的循环优选while |
