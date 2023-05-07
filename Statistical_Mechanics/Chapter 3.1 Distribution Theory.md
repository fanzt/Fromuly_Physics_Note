# Chapter 3.1 分布理论

![节点](./Images/4.png)
>封面图源网络，侵删
>注：本文为笔者学习朗道《统计物理学I》过程中的笔记与相关内容的补充。笔者是初学者，文章内容如有错误，欢迎指正。

$$
    \newcommand{dbar}{\mathrm{d}\kern{-4.3pt}\bar{\small\phantom{q}}\kern{-0.7pt}}
    \newcommand{d}{\mathrm{d}}
    \newcommand{p}{\partial}
    \newcommand{l}{\left}
    \newcommand{r}{\right}
    \newcommand{<}{\langle}
    \newcommand{>}{\rangle}
$$

## 分布理论

### 1.吉布斯分布

&emsp;&emsp;再次考虑第一章中讨论的如下问题：若将任何宏观物体视作某个大的闭合系统的微小子系统，求其分布函数。
&emsp;&emsp;为了解决这个问题，我们要将微正则分布应用于整个系统。考虑原始量子微正则分布的公式：
    $$
        \d{w}=C·\delta(E-E_0)\prod\limits_a\d\Gamma_a
    $$

&emsp;&emsp;将闭合系统划分为由研究对象与其余部分（称为对象所在的介质）两部分，并将微正则分布写为：
    $$
        \d{w}=C·\delta(E+E'-E_0)\d{\Gamma}\d{\Gamma'}
    $$

其中 $E$ 与 $\d\Gamma$ 分别为研究对象的能量与统计权重，$E'$ 与 $\d\Gamma$ 则分别属于介质。考虑研究对象处于一个固定的状态而介质处于具有 $\Delta\Gamma'$ 展宽的量子态上，对上式积分，有：
    $$
        w=C\cdot\int\delta(E_n+E'-E_0)\d{\Gamma'}
    $$

考虑 $\Gamma'=\Gamma'(E')$ 以及熵的定义，我们有：
    $$
        w=C\cdot\int\delta(E_n+E'-E_0)\frac{\exp[S'(E')]}{\Delta{E'}}\d{E'}
    $$

计算积分，有:
    $$
    \begin{aligned}
        w&=C\cdot{\Delta{(E_0-E_n)}}
        \\&=C\cdot\frac{\exp[S'(E_0-E_n)]}{\Delta{(E_0-E_n)}}
    \end{aligned}
    $$

考虑 $S'=S'(E_0-E_n)$，将其展开：
    $$
        S'(E_0-E_n)=S'(E_0)-E_n\frac{\d{S(E_0)}}{\d{E}}
    $$

这里出现了熵对能量的导数，而显然根据定义，熵对能量的导数正是温度。于是我们就可以得到 $w_n$ 的表达式：
    $$
        w_n=A\exp\l(-\frac{E_n}{T}\r)
    $$

其中 $A$ 是一个与 $E_n$ 无关的归一化常量。该公式确定了任何作为一个大闭合体系的小部分的宏观物体的统计分布规律。上式的分布被称为**吉布斯分布**或**正则分布**。
&emsp;&emsp;归一化常数 $A$ 由概率密度的归一化 $\displaystyle\sum{w_n}=1$ 确定，因此我们有：
    $$
        \frac{1}{A}=\sum_{n}\exp\l(-\frac{E_n}{T}\r)
    $$

&emsp;&emsp;在得到了分布函数之后，我们首先可以计算的便是任何物理量的平均值：
    $$
        \<f\>=\sum_n{w_{n}f_{nn}}=\frac{\displaystyle\sum_n{f_{nn}\exp\l(-\frac{E_n}{T}\r)}}{\displaystyle\sum_{n}\exp\l(-\frac{E_n}{T}\r)}
    $$

其中 $f_{nn}$ 是物理量 $f$ 对应的算符进行缩并后的结果。
&emsp;&emsp;而在经典统计中，我们也同样可以写出相空间的分布函数为：
    $$
        \rho(p,q)=A\exp\l(-\frac{E(p,q)}{T}\r)
    $$

其中归一化常量 $A$ 由下式给出：
    $$
        A\int{\exp\l(-\frac{E(p,q)}{T}\r)}\d{p}\d{q}=1
    $$

&emsp;&emsp;然而，在有些情况下，粒子的运动对应于这样一种情况：其部分自由度的运动是准经典的，而另外一部分自由度的运动又是量子的（例如分子本身的平动具有准经典的特征，而分子内部原子的运动则具有量子化的特性）。在这种情况下，物体的能级将可以写作准经典的坐标与动量的函数，即 $E_n=E_n(p,q)$，于是吉布斯分布可写为：
    $$
        \d{w_n}(p,q)=A\exp\l(-\frac{E_n(p,q)}{T}\r)\d{p_{cl}}\d{q_{cl}}
    $$

