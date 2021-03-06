---
layout: default
title: Home
nav_order: 1
description: "Just the Docs is a responsive Jekyll theme with built-in search that is easily customizable and hosted on GitHub Pages."
permalink: /
last_modified_date: 2020-04-27T17:54:08+0000
---

## AI 在线
{: .fs-9 }

由于人工智能是一个综合性学科，所以其对资源地整合有着更高的要求。具体来说，人工智能领域下的机器学习模型和深度学习模型所涉及的学科内容包括且不限于以下的内容:
* 基本数学知识(比如矩阵运算和函数求导)
* 基本的编程知识(比如Python基础)
* 简单的统计概念(比如数据清洗及其可视化等)
* 具体的生活场景应用(比如AI医疗和智慧城市等)

因此，为了更加有效地推进人工智能学科的学习，增加普罗大众对这个领域的认识，该网站试图有序地整合和呈现相关资源，尽可能成为人工智能领域内具有一定审美趣味的一站式索引终端。

{: .fs-6 .fw-300 }

[使用说明](#使用说明){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[案例展示](#案例展示){: .btn .btn-blue .fs-5 .mb-4 .mb-md-0 .mr-2 }

<!-- [View it on GitHub](https://github.com/pmarsceill/just-the-docs){: .btn .fs-5 .mb-4 .mb-md-0 } -->

---

## 使用说明

### 手机用户

首次访问该网站时，除了在线实验模块的Python在线编译器加载需要时间之外，其余的下属网址和内容显示都较为流畅。用户如果想要回到主页的话，可以
- 通过点击左上角的**人工智能一站索引**标题
- 通过向上滑动点击右上角的紫色索引键

本网站的内容有知识讲解和代码展示构成，对于想要进行代码运行的用户，可以到**在线实验**模块进行在线运或者在自由平台上复制代码后运行。比如，用户可以复制下面的代码到自己的平台上运行:

```python
import numpy as np

m1 = np.asmatrix([[1, 0], [0, 1]])  # 建立一个简单的矩阵
```


### 电脑用户

因为电脑屏幕可显示内容较多，电脑用户访问该网站时，所有的导引都会自动显示，这里就不做额外的讲解了。



## 案例展示

这里，我们选取


---

## About the project

该网站设计版权归 &copy; 2017-{{ "now" | date: "%Y" }} by [Patrick Marsceill](http://patrickmarsceill.com); 内容版权归 &copy; 2019-{{ "now" | date: "%Y" }} by [Michael](https://www.michaelyunfei.com).

### License

Just the Docs is distributed by an [MIT license](https://github.com/pmarsceill/just-the-docs/tree/master/LICENSE.txt).

### Contributing

如果想要对此开源项目进行编码贡献，请发送邮件联系Github repository的创建者，获得赞许后方可参与网站共建。详情请浏览[our GitHub repo](https://github.com/pmarsceill/just-the-docs#contributing).

When contributing to this repository, please first discuss the change you wish to make via issue,
email, or any other method with the owners of this repository before making a change. Read more about becoming a contributor in [our GitHub repo](https://github.com/pmarsceill/just-the-docs#contributing).


#### Thank you to the contributors of Just the Docs!

<ul class="list-style-none">
{% for contributor in site.github.contributors %}
  <li class="d-inline-block mr-1">
     <a href="{{ contributor.html_url }}"><img src="{{ contributor.avatar_url }}" width="32" height="32" alt="{{ contributor.login }}"/></a>
  </li>
{% endfor %}
</ul>

### Code of Conduct

Just the Docs is committed to fostering a welcoming community.

[View our Code of Conduct](https://github.com/pmarsceill/just-the-docs/tree/master/CODE_OF_CONDUCT.md) on our GitHub repository.
