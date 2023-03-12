# Chapter 2.2 热力学量的关系与应用

![节点](./Images/3.png)
>封面图源网络，侵删
>注：本文为笔者学习朗道《统计物理学I》过程中的笔记与相关内容的补充。笔者是初学者，文章内容如有错误，欢迎指正。

$$
    \newcommand{dbar}{\mathrm{d}\kern{-4.3pt}\bar{\small\phantom{q}}\kern{-0.7pt}}
    \newcommand{d}{\mathrm{d}}
    \newcommand{p}{\partial}
    \newcommand{(}{\left(}
    \newcommand{)}{\right)}
$$

## 热力学量之间的关系

### 1.热力学量的导数之间的关系

&emsp;&emsp;考虑到我们常常需要将热力学量彼此之间的各种导数变换成由别的热力学量组成的量，接下来我们考虑热力学量的导数之间的关系。
&emsp;&emsp;首先考虑使用 $V$ 和 $T$ 作为自变量，变换的结果应当可以通过 $P$ 与 $C_v$ （作为 $V$ 和 $T$ 的函数）表达出来。类似地，在选取 $P$ 和 $T$ 作为自变量时，变换的结果应当可以通过 $V$ 与 $C_p$ 表示出来。我们将联系 $P$、$V$、$T$ 的方程称为物态方程。实际上，物态方程本身就可以用来确定 $C_v$ 对 $V$ 的依赖关系以及 $C_p$ 对 $P$ 的依赖关系。利用 $\displaystyle S=-\(\frac{\p{F}}{\p{T}}\)_V$，我们有：
    $$
    \begin{aligned}
        \(\frac{\p{C_v}}{\p{V}}\)_T&=\(\frac{\p}{\p{V}}\(T\frac{\p{S}}{\p{T}}\)_V\)_T
        \\&=\(\frac{\p}{\p{V}}\(T\frac{\p}{\p{T}}\(-\frac{\p{F}}{\p{T}}\)_V\)_V\)_T
        \\&=-T\frac{\p^3{F}}{\p{V}\p{T}^2}
        \\&=-T\frac{\p^2}{\p{T}^2}\(\frac{\p{F}}{\p{V}}\)_T
    \end{aligned}
    $$

又因为 $\displaystyle\(\frac{\p{F}}{\p{V}}\)_T=-P$，于是我们得到：
    $$
        \(\frac{\p{C_v}}{\p{V}}\)_T=T\(\frac{\p^2{P}}{\p{T}^2}\)_V
    $$

类似地，我们有：
    $$
        \(\frac{\p{C_p}}{\p{P}}\)_T=-T\(\frac{\p^2{V}}{\p{T}^2}\)_P
    $$

*朗道本节后面的内容都在讨论如何计算热容，我看不懂所以不想写了，这里直接讨论 Maxwell 关系*
&emsp;&emsp;接下来我们讨论各个热力学量的导数之间的关系。首先给出热力学基本微分方程及其变形：
    $$
        \d{E}=T\d{S}-P\d{V}
        \\\d{H}=T\d{S}+V\d{P}
        \\\d{F}=-S\d{T}-P\d{V}
        \\\d{G}=-S\d{T}+V\d{P}
    $$
再给出相应热力学量的全微分表达式：
    $$
    \begin{aligned}
        \d{E}&=\(\frac{\p{E}}{\p{S}}\)_V\d{S}+\(\frac{\p{E}}{\p{V}}\)_S\d{V}
        \\\d{H}&=\(\frac{\p{H}}{\p{S}}\)_P\d{S}+\(\frac{\p{H}}{\p{P}}\)_S\d{P}
        \\\d{F}&=\(\frac{\p{F}}{\p{T}}\)_V\d{T}+\(\frac{\p{F}}{\p{V}}\)_T\d{V}
        \\\d{G}&=\(\frac{\p{G}}{\p{T}}\)_P\d{T}+\(\frac{\p{G}}{\p{P}}\)_T\d{P}
    \end{aligned}
    $$

对比系数，我们可以立刻得到：
    $$
    \begin{aligned}
        \(\frac{\p{E}}{\p{S}}\)_V&=T\qquad\(\frac{\p{E}}{\p{V}}\)_S=-P
        \\\(\frac{\p{H}}{\p{S}}\)_P&=T\qquad\(\frac{\p{H}}{\p{P}}\)_S=V
        \\\(\frac{\p{F}}{\p{T}}\)_V&=-S\quad\:\:\(\frac{\p{F}}{\p{V}}\)_T=-P
        \\\(\frac{\p{G}}{\p{T}}\)_P&=-S\quad\:\:\(\frac{\p{G}}{\p{P}}\)_T=V
    \end{aligned}
    $$

考虑到求导可以换序，我们有：
    $$
        \(\frac{\p{T}}{\p{V}}\)_S=-\(\frac{\p{P}}{\p{S}}\)_V
        \\\(\frac{\p{T}}{\p{P}}\)_S=\(\frac{\p{V}}{\p{S}}\)_P
        \\\(\frac{\p{S}}{\p{V}}\)_T=\(\frac{\p{P}}{\p{T}}\)_V
        \\\(\frac{\p{S}}{\p{P}}\)_T=-\(\frac{\p{V}}{\p{T}}\)_P
    $$

