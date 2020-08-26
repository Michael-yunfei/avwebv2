---
layout: default
title: 模块
parent: Python基础
nav_order: 6
---

# 模块(Modules)
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---


### 为什么需要模块

随着程序变得越来越长，你或许会想把它拆分成几个文件，以方便维护。你亦或想在不同的程序中使用一个便捷的函数， 而不必把这个函数复制到每一个程序中去。为支持这些，Python有一种方法可以把很多程序或函数定义放在一个文件里，比如讲该文件命名为`math.py`，那么下次就可以先导入这个文件，然后再调取里面的方程。这样的文件被称作模块(modules)。

导入模块的方式有两种:
- 通过<span style = "color:RGB(229, 77, 66)">import</span> 直接导入
- 通过<span style = "color:RGB(229, 77, 66)">import as</span> 导入后给模块一个简称

```python
import math
import numpy as np

print(sin(3))  # sin 函数是从 模块 math 中调取的
m1 = np.asmatrix([[1, 0], [0, 1]])  # np 为模块 numpy, np.asmatrix 是调用其中的函数
print(m1)
```

在人工智能领域较为常用的模块包括

| 模块       | 说明                             | 常用导入指令                    |
|------------|----------------------------------|---------------------------------|
| Numpy      | 处理数值运算和矩阵运算的主要模块 | import numpy as np              |
| pandas     | 处理数据表格和数据整理的主要模块 | import pandas as pd             |
| matplotlib | 主要进行数据可视化和作图模块     | import matplotlib.pyplot as plt |







































<!--  -->
