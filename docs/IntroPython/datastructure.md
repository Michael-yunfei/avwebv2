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

![ListIndex](/images/listindex.png)
