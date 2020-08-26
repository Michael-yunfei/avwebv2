---
layout: default
title: 运算符
parent: Python基础
nav_order: 1
---

# 运算符
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

### 算数运算符

数学运算符，是为了对数进行运算，主要的算数运算符包括(主要适用于整数和小数):
<div class="code-example" markdown="1">

| 运算符     | 说明          | 案例 |
|:-------------|:------------------|:------|
| +           | 加法 | 2+3;  x + y  |
| - | 减法   | 7.2 - 5.9; x - y  |
| *           | 乘法     | 11 * 5.6; x * y   |
| /           | 除法 | 6/2; x/y  |
| %           |  取余  | 7%3; x%y |
|**           |  指数运算  |3\* \* 2; x\*\*y|
|//           |   整除  |9//4; x//y |

</div>

我们看一下具体的例子和代码:
```python
x = 6
y = 2

# 加、减、乘、除
print(x + y)  # 8

print(x - y)  # 4

print(x * y)  # 12

print(x / y)  # 3.0

# 取余
print(x % y)  # 0
print(9 % 2)  # 1

# 指数
print(x ** y)	# 36

# 整除
print(x // y)  # 3
print(9 // 2)  # 4
```
{: .fs-5 }


### 赋值运算符

赋值运算符是建立变量和更改变量内容时，需要使用的运算符，主要包含:
<div class="code-example" markdown="1">

| 运算符     | 说明          | 案例 | 等同于|
|:-------------|:------------------|:------| :------|
| = | 赋值符号| x = 2; x = "hello" | |
| +=          | 变量增加后重新赋值 | x += 3|  x = x + 3  |
| - | 变量减去后重新赋值  | x -= 6  |x = x - 6 |
| *           |  变量相乘后重新赋值    |    | |
| /           |  变量相除后重新赋值 |   | |
| %           |  变量取余后重新赋值  | | |
|**           |  变量指数运算后重新赋值  | | |
|//           |   变量整除后重新赋值  | | |

</div>

```python
x = 2
x += 3
print(x)  # 5

x = 6
x *=2
print(x)  # 12
```
{: .fs-5 }

### 关系运算符

类似于我们数学中的运算一样，关系运算符是用来进行比较的，比较之后返回真(True)或假(False)的结果:

<div class="code-example" markdown="1">

| 运算符     | 说明          | 案例 |
|:-------------|:------------------|:------|
| ==           | 等同于 | x == y  |
| != | 不等同于   | x != y  |
| >           | 大于     | x > y  |
| <           | 小于 | x < y |
| >=         |  大于等于  | x >= y |
| <=          |  小于等于  | x <= y|

</div>

```python
x = 6
y = 2

# equal to
print(x == y)  # False

# not equal to
print(x != y)  # True

# greater than
print(x > y)  # True

# less than
print(x < y)  # False

# greater than or equal to
print(x >= y)  # True

# less than or equal to
print(x <= y)  # False
```
{: .fs-5 }

### 逻辑运算符

Python 也可以进行逻辑运算, 与(and), 或(or), 非(not):

<div class="code-example" markdown="1">

| 运算符     | 说明          | 案例 |
|:-------------|:------------------|:------|
| and | A and B : 只有A和B同真时为真，否则为假 | (10 > 2) and (2 < 1) 结果: False |
| or | A or B: 只要有一个为真则为真，否则为假 | (10 > 2) or (2 < 1) 结果: True |
|not |  not A: A的否定 | not (100 > 2) 结果: False |

</div>

```python
x = 2
y = -2

# and
print(x > 0 and y < 0)  # True

# or
print(x > 0 or y < 0)  # True

# not
print(not(x > 0 and y < 0))  # False
```
{: .fs-5 }


### 其它的运算符

Python里还有一些其它的运算符，由于其在编程过程中并不常用，我们留待后面再介绍。
