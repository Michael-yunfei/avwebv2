---
layout: default
title: 字符串
parent: Python基础
nav_order: 2
---

## 字符串(string)

Python 中有多个字符组成的类型，我们称为字符串(string), 字符串(string)是Python中的基本类型。下面这些用双引号输入的内容都是字符串。

```python
print("hello world")  # hello world

print("^_@")  # ^_@
```
{: .fs-5 }

下面我们创建几个字符串

```python
s1 = "Hello World"
s2 = "你好世界"
```
{: .fs-5 }

字符串也可以进行基本的运算，其常用函数和基本运算有:
<div class="code-example" markdown="1">

| 运算符     | 说明          | 案例 |
|:-------------|:------------------|:------|
| +           | 加法, 字符串合并 | "abc" + "df"  |
| * | 乘法, 字符串扩展  | "ab"  * 2  |
| len()           | 查看字符串长度     | len("abc")   |

</div>

```python
"a" + "b"
print(“a”+“b”)  # ab
s1 = "Hello"
s2 = "world"
print(s1+s2)  # Helloworld
print("SenseTime" * 2)  # SenseTimeSenseTime
print(“Sense Time” * 2)  # Sense TimeSense Time  # 注意空格位置
```
{: .fs-5 }
