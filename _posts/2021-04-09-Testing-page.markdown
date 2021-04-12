---
layout: article
title:  测试页面
date:   2021-04-09 14:48:44 +0800
tags: 测试
show_author_profile: true
modify_date: 2021-04-12
key: Post_test-page
---

  本页面用于测试各种渲染效果。

<!--more-->

***

# 1.代码

  - 行内代码

  `_posts`

  - 高亮代码

  {% highlight ruby %}
  def print_hi(name)
    puts "Hi, #{name}"
  end
  print_hi('Tom')
  #=> prints 'Hi, Tom' to STDOUT.
  {% endhighlight %}

# 2.链接

  [GitHub](https://github.com/jylicmp)

  [ORCID](https://orcid.org/0000-0002-5204-5310)

# 3.图片

  插入图片
  {% highlight html %}
  <img class="image image--md" src="/assets/images/logo/logo.svg"/> #image image--md为默认大小
  This is a lemon
  {% endhighlight %}

  <img class="image image--md" src="/assets/images/logo/logo.svg"/>

  *This is a lemon*

  {% highlight html %}
  <img class="image image--xs" src="/assets/images/logo/logo.svg"/>
  <img class="image image--sm" src="/assets/images/logo/logo.svg"/>
  <img class="image image--md" src="/assets/images/logo/logo.svg"/>
  <img class="image image--lg" src="/assets/images/logo/logo.svg"/>
  <img class="image image--xl" src="/assets/images/logo/logo.svg"/>
  {% endhighlight %}


# 4.公式

  - 行间公式：使用`$$...$$`，如

  {% highlight latex %}
  $$
    \Gamma (z) = \int _{0}^{\infty} t^{z-1} e^{-t} dt.
  $$
  {% endhighlight %}

  显示为

  $$
    \Gamma (z) = \int _{0}^{\infty} t^{z-1} e^{-t} dt.
  $$

  或者使用`\\[...\\]`， 效果同上。如不需要公式编号，则添加`\notag`，如

  {% highlight latex %}
  $$
    \mathrm{erf}(x) = \frac{1}{\sqrt{\pi}} \int _{-x}^{x} e^{-t^{2}} dt.
    \notag
  $$
  {% endhighlight %}

  显示为

  $$
    \mathrm{erf}(x) = \frac{1}{\sqrt{\pi}} \int _{-x}^{x} e^{-t^{2}} dt.
    \notag
  $$

  - 行内公式：使用`\\( ... \\)`，如 `\\( \alpha +  \beta = \gamma .\\)` 显示为 \\( \alpha +  \beta = \gamma .\\)


# 5.引用

  >这是引用的内容
  >>可以嵌套引用

***
