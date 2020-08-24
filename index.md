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

<!-- [View it on GitHub](https://github.com/pmarsceill/just-the-docs){: .btn .fs-5 .mb-4 .mb-md-0 } -->

---

## 使用说明

### Python基础

因为。。

```python
import numpy as np
```

也可以嵌入interactive python console, so cool:

<iframe src="https://trinket.io/embed/python3/3f11f21375" width="100%" height="600" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

### 数据呈现


1. Add Just the Docs to your Jekyll site's `_config.yml` as a [remote theme](https://blog.github.com/2017-11-29-use-any-theme-with-github-pages/)
```yaml
remote_theme: pmarsceill/just-the-docs
```
<small>You must have GitHub Pages enabled on your repo, one or more Markdown files, and a `_config.yml` file. [See an example repository](https://github.com/pmarsceill/jtd-remote)</small>

### Local installation: Use the gem-based theme

1. Install the Ruby Gem
```bash
$ gem install just-the-docs
```
```yaml
# .. or add it to your your Jekyll site’s Gemfile
gem "just-the-docs"
```
2. Add Just the Docs to your Jekyll site’s `_config.yml`
```yaml
theme: "just-the-docs"
```
3. _Optional:_ Initialize search data (creates `search-data.json`)
```bash
$ bundle exec just-the-docs rake search:init
```
3. Run you local Jekyll server
```bash
$ jekyll serve
```
```bash
# .. or if you're using a Gemfile (bundler)
$ bundle exec jekyll serve
```
4. Point your web browser to [http://localhost:4000](http://localhost:4000)

If you're hosting your site on GitHub Pages, [set up GitHub Pages and Jekyll locally](https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll) so that you can more easily work in your development environment.

### Configure Just the Docs

-

---

## About the project

Just the Docs is &copy; 2017-{{ "now" | date: "%Y" }} by [Patrick Marsceill](http://patrickmarsceill.com).

### License

Just the Docs is distributed by an [MIT license](https://github.com/pmarsceill/just-the-docs/tree/master/LICENSE.txt).

### Contributing

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
