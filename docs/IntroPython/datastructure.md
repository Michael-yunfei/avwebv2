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
一旦被创建，其元素将会被标注为，而且透过这些标注也可以调用相应元素。

![](https://github.com/Michael-yunfei/avwebv2/blob/gh-pages/images/listIndex.png)

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
