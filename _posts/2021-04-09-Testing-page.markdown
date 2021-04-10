---
layout: article
title:  测试页面
date:   2021-04-09 14:48:44 +0800
tags: 测试
show_author_profile: true
modify_date: 2021-04-10
---

  本页面用于测试各种渲染效果。

<!--more-->

***

# 1.代码片

  `_posts`

# 2.代码段

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

# 3.链接

  [GitHub](https://github.com/jylicmp)

  [ORCID](https://orcid.org/0000-0002-5204-5310)

# 4.图片

  插入图片

  ![测试图1](/assets/pictures/test_fig.jpg)

# 5.公式

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


# 6.引用

  >这是引用的内容
  >>可以嵌套引用

***
