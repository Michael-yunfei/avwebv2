---
layout: default
title: 函数
parent: Python基础
nav_order: 5
---

# 函数
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---


### 简单的函数编写

函数的创建是为了可以重复性得调用模式化的程序体，从而更高效地解决不同问题。函数创建的三要素为:
- <span style="background-color: RGB(229, 77, 66)"> 输入和输出</span>
- <span style="background-color: RGB(229, 77, 66)"> 函数名</span>
- <span style="background-color: RGB(229, 77, 66)"> 函数体</span>

```python
def print_hello():
  print("Hello")


# 调用函数
print_hello()  # Hello


# 有一个输入的函数
def print_hello2(name):
  """
  输入: name - 字符串 string
  输出: print("Hello", name)
  """
  print("Hello", name)


print_hello2("Michael")
```

### 函数的输入

我们在定义函数时，有时需要规定输入的格式，Python中具体的输入格式设置为:
-默认格式: 按照设定的顺序和程序对局部变量名的使用来运行
-关键值格式: 规定默认关键值后，函数则忽略此前的输入顺序
-多态输入: 如果函数使用<span style="background-color: rgb(229, 77, 66)"> \*args</span> 那么多个输入会被收集为元组；如果函数使用<span style="background-color: rgb(229, 77, 66)">\*kargs</span>那么多个输入会被收集为字典。

认真体会下面打印输出的结果的差异

```python
def func(name, job):
    print(name, 'is a', job)


func('Bob', 'developer')
# Prints Bob is a developer
func('developer', 'Bob')
# Prints developer is a Bob


# 规定了关键值
def func(name, job):
    print(name, 'is a', job)

func(name='Bob', job='developer')
# Prints Bob is a developer

func(job='developer', name='Bob')
# Prints Bob is a developer
```

```python
def print_arguments(*args):
    print(args)

print_arguments(1, 54, 60, 8, 98, 12)
# Prints (1, 54, 60, 8, 98, 12)


def print_arguments(**kwargs):
    print(kwargs)

print_arguments(name='Bob', age=25, job='dev')
# Prints {'name': 'Bob', 'age': 25, 'job': 'dev'}
```

### 函数的输出

函数的输出可以是一个，也可以是多个。

```python
def resid(a, b):
  """
  取余数的函数:
    输入 - a, b
    输出 - a % b
  """
  c = a % b   # 取余数
  return c


print(resid(7, 3))
```



























<!--  -->
