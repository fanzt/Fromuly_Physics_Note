# Chapter 2.2 热力学量的关系与应用

![节点](./Images/3.png)
>封面图源网络，侵删
>注：本文为笔者学习朗道《统计物理学I》过程中的笔记与相关内容的补充。笔者是初学者，文章内容如有错误，欢迎指正。

$$
    \newcommand{dbar}{\mathrm{d}\kern{-4.3pt}\bar{\small\phantom{q}}\kern{-0.7pt}}
    \newcommand{d}{\mathrm{d}}
    \newcommand{p}{\partial}
    \newcommand{l}{\left}
    \newcommand{r}{\right}
$$

## 热力学量之间的关系

### 1.热力学量的导数之间的关系

&emsp;&emsp;考虑到我们常常需要将热力学量彼此之间的各种导数变换成由别的热力学量组成的量，接下来我们考虑热力学量的导数之间的关系。
&emsp;&emsp;首先考虑使用 $V$ 和 $T$ 作为自变量，变换的结果应当可以通过 $P$ 与 $C_v$ （作为 $V$ 和 $T$ 的函数）表达出来。类似地，在选取 $P$ 和 $T$ 作为自变量时，变换的结果应当可以通过 $V$ 与 $C_p$ 表示出来。我们将联系 $P$、$V$、$T$ 的方程称为物态方程。实际上，物态方程本身就可以用来确定 $C_v$ 对 $V$ 的依赖关系以及 $C_p$ 对 $P$ 的依赖关系。利用 $\displaystyle S=-\l(\frac{\p{F}}{\p{T}}\r)_V$，我们有：
    $$
    \begin{aligned}
        \l(\frac{\p{C_v}}{\p{V}}\r)_T&=\l(\frac{\p}{\p{V}}\l( T\frac{\p{S}}{\p{T}}\r)_V\r)_T
        \\&=\l(\frac{\p}{\p{V}}\l( T\frac{\p}{\p{T}}\l(-\frac{\p{F}}{\p{T}}\r)_V\r)_V\r)_T
        \\&=-T\frac{\p^3{F}}{\p{V}\p{T}^2}
        \\&=-T\frac{\p^2}{\p{T}^2}\l(\frac{\p{F}}{\p{V}}\r)_T
    \end{aligned}
    $$

又因为 $\displaystyle\l(\frac{\p{F}}{\p{V}}\r)_T=-P$，于是我们得到：
    $$
        \l(\frac{\p{C_v}}{\p{V}}\r)_T=T\l(\frac{\p^2{P}}{\p{T}^2}\r)_V
    $$

类似地，我们有：
    $$
        \l(\frac{\p{C_p}}{\p{P}}\r)_T=-T\l(\frac{\p^2{V}}{\p{T}^2}\r)_P
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
        \d{E}&=\l(\frac{\p{E}}{\p{S}}\r)_V\d{S}+\l(\frac{\p{E}}{\p{V}}\r)_S\d{V}
        \\\d{H}&=\l(\frac{\p{H}}{\p{S}}\r)_P\d{S}+\l(\frac{\p{H}}{\p{P}}\r)_S\d{P}
        \\\d{F}&=\l(\frac{\p{F}}{\p{T}}\r)_V\d{T}+\l(\frac{\p{F}}{\p{V}}\r)_T\d{V}
        \\\d{G}&=\l(\frac{\p{G}}{\p{T}}\r)_P\d{T}+\l(\frac{\p{G}}{\p{P}}\r)_T\d{P}
    \end{aligned}
    $$

对比系数，我们可以立刻得到：
    $$
    \begin{aligned}
        \l(\frac{\p{E}}{\p{S}}\r)_V&=T\qquad\l(\frac{\p{E}}{\p{V}}\r)_S=-P
        \\\l(\frac{\p{H}}{\p{S}}\r)_P&=T\qquad\l(\frac{\p{H}}{\p{P}}\r)_S=V
        \\\l(\frac{\p{F}}{\p{T}}\r)_V&=-S\quad\:\:\l(\frac{\p{F}}{\p{V}}\r)_T=-P
        \\\l(\frac{\p{G}}{\p{T}}\r)_P&=-S\quad\:\:\l(\frac{\p{G}}{\p{P}}\r)_T=V
    \end{aligned}
    $$

考虑到求导可以换序，我们有：
    $$
        \l(\frac{\p{T}}{\p{V}}\r)_S=-\l(\frac{\p{P}}{\p{S}}\r)_V
        \\\l(\frac{\p{T}}{\p{P}}\r)_S=\l(\frac{\p{V}}{\p{S}}\r)_P
        \\\l(\frac{\p{S}}{\p{V}}\r)_T=\l(\frac{\p{P}}{\p{T}}\r)_V
        \\\l(\frac{\p{S}}{\p{P}}\r)_T=-\l(\frac{\p{V}}{\p{T}}\r)_P
    $$

