---
layout: default
title: 数据结构
parent: Python基础
nav_order: 3
---

# 数据结构
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

### 列表

列表(list)是由多个元素构成的有序的集合，其特点为:
- 元素可以是数字，也可以是字符串，或其它类型
- 元素按照创建时输入的顺序依次标注为 0， 1， 2， 3，...
- 元素的内存空间使用具有可变性
- 使用函数len() 来查看其长度

比如，创建一个列表:
```python
L1 = [123, "Hello", 58.92, "world"]  # 有数字 也有 字符
print(len(L1))  # 4
```
{: .fs-5 }

一旦被创建，其元素将会被标注为，而且透过这些标注也可以调用相应元素。

<!-- ![](https://github.com/Michael-yunfei/avwebv2/blob/gh-pages/images/listIndex.png) -->

列表的相关函数和运算可以概括在下面的表格中

<div class="code-example" markdown="1">

| 相关函数和符号    | 说明          |
|:-------------|:------------------|
| len( ) | 查看列表长度 |
|[ ]| 调取列表中某一个元素|
|[ : ] |调取列表中的某一段元素|
|+| 列表并置|
|* | 列表元素重复|
|L.append() | 在列表L中添加新的元素，放在最末尾|
|L.pop( ) | 删除列表L中的元素 |
|L.insert( , ) | 在列表L中具体位置插入新的元素 |


</div>

```python
name_english = ["Lucy", "David", "Michael", "Leo", "Emmet"]
grade_mandarin = [98, 87, 90, 69, 83]
print(name_english[0])
print(name_english[1])  # David
print(name_english[2])
print(name_english[3])

grade_mandarin[3] = 100  # 修改内容
print(grade_mandarin)  # [98, 87, 90, 100, 83]
```
{: .fs-5 }

练习使用添加和删除函数

```python
grade = [96, 95, 93]
subject = ["Math", "Arts", "Science"]
grade.append(88)  
print(grade)  # [96, 95, 93, 88]
subject.append("English")
print(subject)  # [‘Math’, ‘Arts’, ‘Science’, ‘English’]    
grade.insert(2, 100)
print(grade)  # [96, 95, 100, 93, 88]
subject.insert(2, "Music")
print(subject)  # ['Math', 'Arts', 'Music', 'Science', 'English']

grade.pop()
print(grade) # [96, 95, 100, 93]
subject.pop()
print(subject)  # ['Math', 'Arts', 'Music', 'Science']
grade.pop(2)
print(grade)  # [96, 95, 93]
subject.pop(2)
print(subject)  # ['Math', 'Arts', 'Science']
```
{: .fs-5 }

### 字典

字典(dict), 由多个元素构成的集合，与列表不同，字典没有默认数字索引。因为字典没有默认数字索引，所以我们需要引入索引键(key)来访问对应的元素值(value)。

```python
Lucy = {"Math": 98, "English": 86, "Science": 93}
Michael = {“Math”: 93, “English”: 92, “Science”: 86}
print(Lucy["Math"])  # 98
```
{: .fs-5 }

字典的相关函数和运算可以概括在下面的表格中

<div class="code-example" markdown="1">

|       函数       |           说明           |
|:----------------:|:------------------------:|
|      len( )      |       查看字典长度       |
|     [‘key’ ]     |  根据索引键来调取某个值  |
|    dict.keys()   |     显示字典的索引键     |
|   dict.values()  |     显示字典的元素值     |
|   dict.items()   | 显示字典的索引键和元素值 |
|    dict.copy()   |         复制字典         |
| dict.pop(‘key’ ) |     删除字典中的元素     |

</div>

练习一下相应的函数:
```python
dict1 = {"Math": 98, "English": 86, "Science": 93}
print(dict1.items())  #
print(dict1.keys())  #
print(dict1.values())  #
dict2 = {"name": "Michael", "Math": 98, "English": 86, "Science": 93}
print(dict2["Math"])
dict2.pop("Math")
print(dict2)  #
```
{: .fs-5 }

### 元组

元组(tuple), 由多个元素构成的有序的集合，但是一旦创建则不可以修改。元组可以理解为不可以修改的列表。

```python
tuple1 = ("Math", 19, "Science")
print(tuple1[2])  # Science
```
{: .fs-5 }
