---
layout: article
title:  规范场论-I-1
date:   2021-04-10 23:00:00
tags: 学习笔记
show_author_profile: true
modify_date: 2021-04-10
---

规范场论是研究_全局_和_局部_对称变换下不变的场论，对应于阿贝尔和非阿贝尔规范场论，其中非阿贝尔规范场论的著名例子就是[杨-米尔斯（Yang-Mills）](https://en.wikipedia.org/wiki/Yang%E2%80%93Mills_theory)理论。本系列由本人的课堂笔记整理而成。

本系列主要分成三部分：

- 经典场论中的规范不变性

- 对称性自发破缺规范理论

- 规范场的路径积分量子化

<!--more-->

***

# Part I: 经典场论中的规范不变性

## 整体对称性和定域对称性

著名的[诺特定理](https://en.wikipedia.org/wiki/Noether%27s_theorem)指出，若一个体系的在连续的整体对称变化下保持不变，则该体系存在相应的守恒量。
这里的整体对称性，指的是对于场\\( \psi(\mathbf{r},t) \equiv \psi(x) \\)所做的变换是与空间\\( \mathbf{r} \\)和时间\\( t \\)都无关的。
常见的例子是时间平移不变性对应能量守恒，空间平移不变性对应于动量守恒等等。我们列出常见的整体对称性与相应的守恒量如下表所示：

|---
| 整体对称性 | 相应的守恒量
|:-:|:-:
| 时间-空间平移 | 能量-动量
| 整体Lorentz变换 | 角动量[^1]
| 整体相位变换 \\( \psi(x)\rightarrow e^{i\theta}\psi(x) \\) | 电荷
| 同位旋变换 \\( \psi(x)\rightarrow e^{i \boldsymbol{\tau} \cdot \boldsymbol{\theta}}\psi(x) \\) | 同位旋
|---

[^1]: 这里的角动量守恒有别于普通物理中的角动量守恒。一般认为角动量守恒是与空间旋转不变性对应的，然而空间旋转变换是依赖于空间坐标的（在旋转变换中至少有一个点\\(\mathbf{r}_{0}\\)是不发生变化的），因此不是整体对称性。因此这里所说的是相对论角动量守恒：\\(\partial_{\gamma}\mathcal{J}^{\alpha\beta\gamma}=0\\)。$$具体可参考[这里](https://en.wikipedia.org/wiki/Relativistic_angular_momentum)。
