---
layout: article
title:  规范场论-2
date:   2021-04-18 12:00:00 +0800
tags: 学习笔记
show_author_profile: true
modify_date: 2021-04-18
comments: true
key: Post_gauge_2
---

在上一部分，我们从自由电子的阿贝尔\\( U(1) \\)规范群出发，得出局域\\( U(1) \\)规范不变性诱导出的阿贝尔规范场，即电磁相互作用。本文将以类似的步骤，从同位旋的非阿贝尔\\( SU(2) \\)规范群入手，导出非阿贝尔规范场，也被称为[杨-米尔斯（Yang-Mills）场](https://en.wikipedia.org/wiki/Yang%E2%80%93Mills_theory)。

<!--more-->

***

# 3.非阿贝尔规范群和规范场

## 整体\\( SU(2) \\)规范变换和同位旋

行列式为\\( 1\\)的二阶酉矩阵（幺正矩阵）在矩阵乘法下构成\\( SU(2) \\)群，\\( SU(2) \\)群的群元可以看作一个规范变换\\( U=e^{-i \mathbf{T} \cdot 𝛉} \\), 其中\\( 𝛉 = (\theta _{1}, \theta _{2}, \theta _{3},) \\)为群参数，\\( \mathbf{T} \\)为\\( SU(2) \\)群的生成元，满足代数

$$
\left[ T _{i}, T _{j} \right] = i \varepsilon _{ijk} T _{k},
$$

这里的\\( \varepsilon _{ijk} \\)是三阶完全反对称张量。\\( SU(2) \\)群的结构由生成元的代数决定，而每一个群元由三个参数\\( \theta _{i} \\)决定。

这样的一个\\( SU(2) \\)规范变换可以发生在一个类似于自旋旋量态的二态系统，同位旋（isospin）二重态就是这样的一个体系。同位旋概念最早由[海森堡（Heisenberg）](https://zh.wikipedia.org/wiki/%E7%BB%B4%E5%B0%94%E7%BA%B3%C2%B7%E6%B5%B7%E6%A3%AE%E5%A0%A1)在1932年提出。我们知道组成原子核的质子和中子（或者统称核子）的质量几乎相等，并且二者可以在一定条件下互相转化，它们最大的差异就是质子带一个单位正电荷而中子不带电；更重要的是，实验表明核子之间（无论是质子间还是中子间）的强相互作用是相同的。电荷是电磁相互作用的范畴，于是从强相互作用力来看，质子和中子二者应该别无二致，或者应是同一个粒子的两种不同的状态。因此，海森堡从这些现象出发，将质子中子看成一个类似于自旋的二重态，相应的量子数就是同位旋。

我们以质子-中子二重态作为表示空间，一个\\( SU(2) \\)规范变换就是

$$
\left(\begin{array}{c}
p\\
n
\end{array}\right) \rightarrow e ^{-i \mathbf{T} \cdot 𝛉}
\left(\begin{array}{c}
p\\
n
\end{array}\right)
=
U(𝛉) \left(\begin{array}{c}
p\\
n
\end{array}\right).
$$

在此表示空间下，我们可以取\\( T _{i} = \sigma _{i} /2 \\)，\\( \sigma _{i} \\)是我们所熟悉的[泡利（Pauli）](https://zh.wikipedia.org/zh/%E6%B2%83%E5%B0%94%E5%A4%AB%E5%86%88%C2%B7%E6%B3%A1%E5%88%A9)矩阵:

$$
\sigma _{1} = \left(
    \begin{array}{cc}
    0 & 1 \\
    1 & 0
    \end{array}
     \right),
\
\sigma _{2} = \left(
    \begin{array}{cc}
    0 & -i \\
    i & 0
    \end{array}
     \right),
\
\sigma _{3} = \left(
    \begin{array}{cc}
    1 & 0 \\
    0 & -1
    \end{array}
     \right).
$$

利用指数函数的级数展开和泡利矩阵的性质，我们不难求出

$$
U(𝛉) = \cos \frac{\theta}{2} - i 𝛔 \cdot \hat{𝛉} \sin \frac{\theta}{2},
$$

其中\\( \theta = \sqrt{\theta _{1}^{2} + \theta _{2}^{2} + \theta _{3}^{2}}, \ \hat{𝛉} = 𝛉 / \theta \\)。满足此对称性所导致的守恒律，便是同位旋守恒。


小结：同位旋二重态是具有类似于自旋二重态的二重态结构，描述强相互作用下质子和中子间的对称性，这种对称性用\\((SU(2)\\))规范变换描述。
{:.info}


## 局域\\(SU(2)\\)规范变换

近日补充……




***
