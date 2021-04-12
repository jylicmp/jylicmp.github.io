---
layout: article
title:  规范场论-1
date:   2021-04-10 23:30:00 +0800
tags: 学习笔记
show_author_profile: true
modify_date: 2021-04-11s
key: Post_gauge_1
---

规范场论是研究整体和局部对称变换下不变的场论，对应于阿贝尔和非阿贝尔规范场论，其中非阿贝尔规范场论的著名例子就是[杨-米尔斯（Yang-Mills）](https://en.wikipedia.org/wiki/Yang%E2%80%93Mills_theory)理论。本系列由本人的课堂笔记整理而成。

本系列主要分成三部分：

- 经典场论中的规范不变性

- 对称性自发破缺规范理论

- 规范场的路径积分量子化

<!--more-->

***

# Part I: 经典场论中的规范不变性

## 1.整体对称性和局域对称性

著名的[诺特定理（Noether's theorem）](https://en.wikipedia.org/wiki/Noether%27s_theorem)指出，经典物理中，若一个体系的在连续对称变换下保持不变，则该体系存在相应的守恒量。在量子力学中，则为整体对称性对应于守恒律。
这里的整体对称性，指的是对于场\\( \psi(\mathbf{r},t) \equiv \psi(x) \\)所做的变换是与空间\\( \mathbf{r} \\)和时间\\( t \\)都无关的。
常见的例子是时间平移不变性对应能量守恒，空间平移不变性对应于动量守恒等等。我们列出常见的整体对称性与相应的守恒量如下表所示：

|---
| 整体对称性 | 相应的守恒量
|:-:|:-:
| 时间-空间平移 | 能量-动量
| 整体Lorentz变换 | 角动量\\(^{\dagger}\\)
| 整体相位变换 \\( \psi(x)\rightarrow e^{i\theta}\psi(x) \\) | 电荷
| 同位旋变换 \\( \psi(x)\rightarrow e^{i 𝛕 \cdot 𝛉}\psi(x) \\) | 同位旋
|---

\\(\dagger\\) 这里的角动量守恒有别于普通物理中的角动量守恒。一般认为角动量守恒是与空间旋转不变性对应的，然而空间旋转变换是依赖于空间坐标的，存在某些点不发生变化（在旋转轴上的点），因此不是整体对称性。因此这里所说的是相对论角动量守恒：\\(\partial_{\gamma}\mathcal{J}^{\alpha\beta\gamma}=0\\)。具体可参考[这里](https://en.wikipedia.org/wiki/Relativistic_angular_momentum)。
{:.warning}

与整体对称相对应的，局域对称性描述的是时空相关的变换。局域对称性并不会导致守恒律，而是会在原有场的基础上引入相互作用的场。最典型的例子是考虑局域的规范变换引入电磁相互作用（电磁场），具体讨论见第二节。我们同样列出部分局域对称性与相互作用的对应关系：

|---
| 局域对称性 | 相互作用（场）
| :-: | :-:
| 局域Lorentz变换 | 引力场
| 局域相位变换 \\( \psi(x)\rightarrow e^{i\theta(x)}\psi(x) \\) | 电磁场
| 定域同位旋变换 \\( \psi(x)\rightarrow e^{i 𝛕 \cdot 𝛉(x)}\psi(x) \\) | \\( SU(2) \\)规范场

小结：整体对称变换 ⟺ 守恒量，局域对称变换 ⟺ 相互作用（场）
{:.info}


## 2.\\( U(1)\\)规范群和电磁场

波函数的相位是一个重要的量，然而波函数在某点的相位并不可测量，即\\( \psi(x) \\)与\\( e^{-i\theta(x)}\psi(x) \\)都描述同一个波函数（量子态对应于希尔伯特空间中的射线），描述相同的物理现象。我们可以定义一个相位变换，或者我们更习惯称之为**规范变换（gauge transformation\\(^{\ddagger}\\)）**: \\( U(x)=e^{-i\theta(x)}\\)，不难验证\\(U^{\dagger}(x)=U^{-1}(x)\\)是一个幺正（酉）算符。变换前后的两个波函数描述相同的物理现象，意味着系统在变换\\( \psi(x)\rightarrow U(x)\psi(x) \\)下保持不变。显然，对于所有的规范变换\\( U_{i}(x)=e^{i\theta_{i}(x)}\\)，它们构成一个群，称为\\(U(1)\\)群；而且对于任意两个群元都有

$$
U_{i}(x)U_{j}(x) = U_{j}(x)U_{i}(x) ⟺ \left[ U_{i}(x),U_{j}(x) \right] = 0,
$$

则\\( U(1) \\)群是一个[阿贝尔（Abel）](https://en.wikipedia.org/wiki/Niels_Henrik_Abel)群。

\\(\ddagger\\) gauge transformation原意指**标度变换**，即长度发生变化的变换。历史上源于[外尔（Weyl）](https://en.wikipedia.org/wiki/Hermann_Weyl)对波函数对称变换下不变的先驱研究，但他的工作中的变换为\\(U(x)=e^{-\theta(x)}\\)，是一个衰减因子。故而当波函数在空间完成一个周期演化回到原点后，波函数的模平方会减小，对应于粒子的凭空消失。这使他放弃了进一步的研究。
{:.warning}

自由电子满足[狄拉克（Dirac）](https://en.wikipedia.org/wiki/Paul_Dirac)方程，相应的拉氏量为

$$
  \mathcal{L} _ {0} = -\bar{\psi} \gamma _ {\mu}\partial_{\mu}\psi - m\bar{\psi}\psi,
$$

其中\\( \bar{\psi}=\psi^{\dagger}\gamma_{4} \\)，\\( \mu =0,1,2,3\\)，\\(0\\)是时间分量，重复指标表示求和。在局域的\\( U(1) \\)变换下

$$
  \psi(x) \rightarrow \psi ^{\prime}(x) = e^{-i\theta(x)}\psi(x), \ \ \bar{\psi}(x) \rightarrow \bar{\psi^{\prime}}(x) = e^{i\theta(x)}\bar{\psi}(x), \label{eq_psi}
$$

而导数项变为

$$
  \partial_{\mu} \psi(x) \rightarrow \partial_{\mu} \psi^{\prime}(x) = e^{-i\theta(x)}\left[\partial_{\mu} - i\partial_{\mu} \theta (x) \right] \psi(x).
$$

则很明显

$$
  \mathcal{L} _{0} \rightarrow \mathcal{L} _{0}^{\prime} = -\bar{\psi}\gamma _{\mu} \left[ \partial _{\mu} - i \partial _{\mu} \theta  (x) \right] \psi - m \bar{\psi} \psi \neq \mathcal{L} _{0},
$$

即在\\( U(1) \\)变换下拉氏量\\( \mathcal{L} _{0} \\)的形式会发生变化，相应的运动方程也会发生变化。这意味着我们可以区分出变换前后的两个波函数，这明显有悖于我们之前的认知。

为了使拉氏量在局域\\(U(1)\\)变换下不变，我们需要引入相互作用场\\( A_{\mu} \\)，并将偏导数项替换为协变导数

$$
  D _{\mu} = \partial _{\mu} - ie A _{\mu}.
$$

现在的拉氏量变为

$$
  \begin{equation}
  \begin{aligned}
  \mathcal{L} &= - \bar{\psi} \gamma _{\mu} D _{\mu} \psi - m\bar{\psi} \psi \\
  &= - \bar{\psi} \gamma _{\mu}\partial _{\mu} \psi - m \bar{\psi}\psi  + ie \bar{\psi} \gamma _{\mu} \psi A _{\mu} \\
  &= \mathcal{L} _{0} + J _{\mu}A _{\mu},
  \end{aligned}
  \end{equation} \label{eq_L}
$$

即引入了电磁相互作用\\( J _{\mu} A _{\mu}\\)，\\( J _{\mu} \\)是电流密度。

现在当我们对\\( \psi (x) \\)做\\( U(1) \\)变换Eq. $\eqref{eq_psi}$时，也需要对相互作用场做变换\\( A _{\mu} \rightarrow A _{\mu}^{\prime} \\)：

$$
  \mathcal{L} \rightarrow \mathcal{L}^{\prime} = \mathcal{L} _{0} + \bar{\psi} \gamma _{\mu} \left[ i\partial _{\mu} \theta (x) \right]\psi + ie \bar{\psi} \gamma _{\mu} A _{\mu}^{\prime} \psi.
$$

规范不变性要求上式应和Eq. $\eqref{eq_L}$相同，因此得出相互作用场在\\( U(1) \\)下的变换为

$$
  A _{\mu} \rightarrow A _{\mu}^{\prime} = A _{\mu} - \frac{1}{e} \partial _{\mu} \theta (x).
$$

我们称从规范不变性得出的场\\( A _{\mu} \\)为**规范场**，由于\\( U(1) \\)是阿贝尔的，所以\\( A _{\mu} \\)是**阿贝尔规范场**。

规范场\\( A _{\mu} \\)并不具有规范不变性，因此不是物理上的可观测量，或者说它们的值会随着规范的选取而改变。直观的例子便是谈论标量势和矢量势\\( (\phi , \mathbf{A}) \\)的绝对数值并没有意义，只有它们的时空变化量才能导致可观测的结果（电磁场）。电磁场由[麦克斯韦（Maxwell）方程组](https://en.wikipedia.org/wiki/Maxwell%27s_equations)给出：

$$
  F _{\mu \nu} = \partial _{\mu} A _{\nu} - \partial _{\nu} A _{\mu},
$$

同时留意到

$$
  \begin{equation}
  \begin{aligned}
  \left[ D _{\mu}, D _{\nu} \right]\psi &= - ie A _{\mu} (\partial _{\nu}\psi ) +\partial _{\mu} (-ie A _{\nu} \psi) + ie A _{\nu} (\partial _{\mu} \psi) -\partial _{\nu} (-ie A _{\mu} \psi) \\
  &= \frac{e}{i} \left( \partial _{\mu} A _{\nu} - \partial _{\nu} A _{\mu} \right) \psi ,
  \end{aligned}
  \end{equation}
$$

我们因而可将电磁场改写成协变导数的对易关系

$$
  F _{\mu \nu} = \frac{i}{e} \left[ D _{\mu}, D _{\nu} \right].
$$

利用此式，我们很容易发现，在规范变换\\( D _{\mu} \rightarrow D _{\mu}^{\prime} = D _{\mu} + i \partial _{\mu} \theta (x) \\)下，电磁场张量\\( F _{\mu \nu}\\)是规范不变的，因此是可观测量。


小结：我们从自由电子满足局域\\( U(1) \\)规范不变性，导出阿贝尔规范场\\( A _{\mu} \\)和相互作用项\\( J _{\mu} A _{\mu} \\)；规范场\\( A _{\mu} \\)因不满足规范不变而不可观测，但其对应的张量场——电磁场\\( F _{\mu \nu} \\)满足规范不变性，因此是可观测量。
{:.info}

<center>下节预告：从同位旋的非阿贝尔$ SU(2)$规范群出发，导出非阿贝尔规范场。</center>

***
