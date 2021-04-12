---
layout: article
title:  测试页面
date:   2021-04-09 14:48:44 +0800
tags: 测试
show_author_profile: true
modify_date: 2021-04-12
key: Post_test-page
artical_header:
  type: cover
  image:
  src: <img src="https://i.loli.net/2021/04/12/mHhWOQyaAELjCpJ.jpg" />
---

  本页面用于测试各种渲染效果。

<!--more-->

***

# 1.代码

## 行内代码

`_posts`

## 高亮代码

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

# 2.链接

{% highlight markdown %}
[text](link)
{% endhighlight %}

[GitHub](https://github.com/jylicmp)

[ORCID](https://orcid.org/0000-0002-5204-5310)

# 3.图片

## 直接插入
{% highlight html %}
<img class="image image--md" src="/assets/images/logo/logo.svg"/> #image image--md为默认大小
This is a lemon
{% endhighlight %}

<img class="image image--md" src="/assets/images/logo/logo.svg"/>

*This is a lemon*

调整图片大小：只需将`image--md`中的`md`改为`xs,sm,md,lg,xl`即可。

## Item方式

{% highlight html %}
<div class="item">
  <div class="item__image">
    <img class="image" src="..."/>
  </div>
  <div class="item__content">
    <div class="item__header">
      <h4>name</h4>
    </div>
    <div class="item__description">
      <p>Caption</p>
    </div>
  </div>
</div>
{% endhighlight %}

<div class="item">
  <div class="item__image">
    <img class="image" src="/assets/images/logo/logo.svg"/>
  </div>
  <div class="item__content">
    <div class="item__header">
      <h4>Lemon too</h4>
    </div>
    <div class="item__description">
      <p>This is a lemon too.</p>
    </div>
  </div>
</div>

## card方式

{% highlight html %}
<div class="card">
  <div class="card__image">
    <img class="image" src="..."/>
  </div>
  <div class="card__content">
    <div class="card__header">
      <h4>Name</h4>
    </div>
    <p>Caption</p>
  </div>
</div>
{% endhighlight %}

<div class="card">
  <div class="card__image">
    <img class="image image--sm" src="/assets/images/logo/logo.svg"/>
  </div>
  <div class="card__content">
    <div class="card__header">
      <h4>Lemon again</h4>
    </div>
    <p>This is a lemon again.</p>
  </div>
</div>



# 4.公式

## 行间公式

使用`$$...$$`，如

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

## 行内公式

使用`\\( ... \\)`，如 `\\( \alpha +  \beta = \gamma .\\)` 显示为 \\( \alpha +  \beta = \gamma .\\)

## 公式引用

先用`\label{...}`标签公式，如

{% highlight latex %}
$$
  n! \approx \sqrt{2 \pi n} \left( \frac{n}{e} \right) ^{n}.
  \label{Stirling}
$$
{% endhighlight %}

斯特灵公式：

$$
  n! \approx \sqrt{2 \pi n} \left( \frac{n}{e} \right) ^{n}.
  \label{Stirling}
$$

然后用`$\eqref{Stirling}$`便可引用，Eq. $\eqref{Stirling}$。


# 5.引用

  >这是引用的内容
  >>可以嵌套引用

***
