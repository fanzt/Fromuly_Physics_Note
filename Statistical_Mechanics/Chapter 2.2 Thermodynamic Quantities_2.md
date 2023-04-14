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

#### (1).Maxwell 关系

&emsp;&emsp;考虑到我们常常需要将热力学量彼此之间的各种导数变换成由别的热力学量组成的量，接下来我们考虑热力学量的导数之间的关系。
*朗道本节后面的内容都在讨论如何计算热容，我看得不是很懂所以不想写了，这里直接讨论 Maxwell 关系*
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
        \\\l(\frac{\p{F}}{\p{T}}\r)_V&=-S\qquad\l(\frac{\p{F}}{\p{V}}\r)_T=-P
        \\\l(\frac{\p{G}}{\p{T}}\r)_P&=-S\qquad\l(\frac{\p{G}}{\p{P}}\r)_T=V
    \end{aligned}
    $$

考虑到求导可以换序，我们有：
    $$
    \begin{aligned}
        \l(\frac{\p{T}}{\p{V}}\r)_S=-\l(\frac{\p{P}}{\p{S}}\r)_V
        \\\l(\frac{\p{T}}{\p{P}}\r)_S=\l(\frac{\p{V}}{\p{S}}\r)_P
        \\\l(\frac{\p{S}}{\p{V}}\r)_T=\l(\frac{\p{P}}{\p{T}}\r)_V
        \\\l(\frac{\p{S}}{\p{P}}\r)_T=-\l(\frac{\p{V}}{\p{T}}\r)_P
    \end{aligned}
    $$

在此引入 Jacobi 行列式：
    $$
        \frac{\p(u,v)}{\p(x,y)}=
            \l|\begin{matrix}
                \displaystyle\frac{\p{u}}{\p{x}} & \displaystyle\frac{\p{u}}{\p{y}}
                \\\displaystyle\frac{\p{v}}{\p{x}} & \displaystyle\frac{\p{v}}{\p{y}}
            \end{matrix}\r|
    $$

显然其具有性质：
    $$
    \begin{aligned}
        \frac{\p(u,y)}{\p(x,y)}&=
            \l|\begin{matrix}
                \displaystyle\frac{\p{u}}{\p{x}} & \displaystyle\frac{\p{u}}{\p{y}}
                \\\displaystyle\frac{\p{y}}{\p{x}} & \displaystyle\frac{\p{y}}{\p{y}}
            \end{matrix}\r|
            \\&=
            \l|\begin{matrix}
                \displaystyle\frac{\p{u}}{\p{x}} & \displaystyle\frac{\p{u}}{\p{y}}
                \\0 & 1
            \end{matrix}\r|
            \\&=\l(\frac{\p{u}}{\p{x}}\r)_y
    \end{aligned}
    $$

----

#### (2).等压热容与等容热容之间的一些关系

*还是写点吧……*
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

接下来我们利用以上知识证明一个事实：不论何种情况何种状态，对于所有的物体，我们总有：
    $$
        C_p-C_v>0
    $$

证：
首先写出 $C_v$ 的表达式：
    $$
        C_v=T\l(\frac{\p{S}}{\p{T}}\r)_V
    $$

利用 Jacobi 行列式，并经过一系列化简，我们有：
    $$
    \begin{aligned}
        C_v&=T\frac{\p(S,V)}{\p(T,V)}
        \\&=T\frac{\frac{\p(S,V)}{\p(T,P)}}{\frac{\p(T,V)}{\p(T,P)}}
        \\&=T
            \frac{
            \l(
                \frac{\p{S}}{\p{T}}
            \r)_P
            \l(
                \frac{\p{V}}{\p{P}}
            \r)_T
            -\l(
                \frac{\p{S}}{\p{P}}
            \r)_T
            \l(
                \frac{\p{V}}{\p{T}}
            \r)_P}{
                \l(
                    \frac{\p{V}}{\p{P}}
                \r)_T
            }
        \\&=C_p-T\frac{
            \l(
                \frac{\p{S}}{\p{P}}
            \r)_T
            \l(
                \frac{\p{V}}{\p{T}}
            \r)_P}{
                \l(
                    \frac{\p{V}}{\p{P}}
                \r)_T
            }
    \end{aligned}
    $$

带入 Maxwell 关系中的一个，我们有：
    $$
    \begin{aligned}
        C_v&=C_p+T\frac{
            \l(
                \frac{\p{V}}{\p{T}}
            \r)^2_P}{
                \l(
                    \frac{\p{V}}{\p{P}}
                \r)_T
            }
    \end{aligned}
    $$

于是我们就有：
    $$
        C_p-C_v=-T\frac{
            \l(
                \frac{\p{V}}{\p{T}}
            \r)^2_P}{
                \l(
                    \frac{\p{V}}{\p{P}}
                \r)_T
            }
    $$

用类似的方法，我们有：
    $$
    \begin{aligned}
        C_p&=T\l(\frac{\p{S}}{\p{T}}\r)_P
        \\&=T\frac{\p(S,P)}{\p(T,P)}
        \\&=T\frac{\frac{\p(S,P)}{\p(T,V)}}{\frac{\p(T,P)}{\p(T,V)}}
        \\&=T
            \frac{
            \l(
                \frac{\p{S}}{\p{T}}
            \r)_V
            \l(
                \frac{\p{P}}{\p{V}}
            \r)_T
            -\l(
                \frac{\p{S}}{\p{V}}
            \r)_T
            \l(
                \frac{\p{P}}{\p{T}}
            \r)_V}{
                \l(
                    \frac{\p{P}}{\p{V}}
                \r)_T
            }
        \\&=C_v-T\frac{
            \l(
                \frac{\p{P}}{\p{T}}
            \r)^2_V}{
                \l(
                    \frac{\p{P}}{\p{V}}
                \r)_T
            }
    \end{aligned}
    $$

于是我们有：
    $$
        C_p-C_v=-T\frac{
            \l(
                \frac{\p{P}}{\p{T}}
            \r)^2_V}{
                \l(
                    \frac{\p{P}}{\p{V}}
                \r)_T
            }
    $$

这里我们需要注意到一个显然的事实：对于一个等温过程，物体如果体积增大则压强必然减小，如果体积减小则压强必然增大。因而我们有：
    $$
        C_p>C_v
    $$

----

#### (3).绝热压缩率与等温压缩率

再考虑绝热压缩率与等温压缩率之间的关系。
首先写出绝热压缩率：
    $$
    \begin{aligned}
        \l(\frac{\p{V}}{\p{P}}\r)_S&=\frac{\p(V,S)}{\p(P,S)}
        \\&=\frac{\frac{\p(V,S)}{\p(V,T)}}{\frac{\p(P,S)}{\p(P,T)}}\frac{\p(V,T)}{\p(P,T)}
        \\&=\frac{\l(\frac{\p{S}}{\p{T}}\r)_V}{\l(\frac{\p{S}}{\p{T}}\r)_P}\l(\frac{\p{V}}{\p{P}}\r)_T
    \end{aligned}
    $$

再考虑到 $C_p$ 与 $C_v$ 的定义：
    $$
        C_p=T\l(\frac{\p{S}}{\p{T}}\r)_P
        \\C_v=T\l(\frac{\p{S}}{\p{T}}\r)_V
    $$

于是我们有：
    $$
        \l(\frac{\p{V}}{\p{P}}\r)_S=\frac{C_v}{C_p}\l(\frac{\p{V}}{\p{P}}\r)_T
    $$

又因为我们有：
    $$
        C_p>C_v
    $$

所以我们有：
    $$
         \l(\frac{\p{V}}{\p{P}}\r)_S<\l(\frac{\p{V}}{\p{P}}\r)_T
    $$

即绝热压缩率的绝对值小于等温压缩率的绝对值。

----

### 2.相关应用

#### (1).最大功与卡诺定理

&emsp;&emsp;考虑由几个互相不处于热平衡态的物体组成的绝热体系。在其过渡到平衡态的过程中，体系会向外界做功。作为过程量，做功的大小显然和过程的种类有关。因此，我们接下来将讨论如何才能让该过程向外输出的功率最大。
&emsp;&emsp;考虑到我们感兴趣的是系统从不平衡过渡到平衡这个过程所做的功，而非处于平衡态的一般情况下气体膨胀所做的功，所以我们假设气体初末态的体积不变。
&emsp;&emsp;设系统的初始能量为 $E_0$，在平衡态的情况下能量视为熵的函数，记为 $E(S)$. 考虑到系统是热绝缘的，由能量守恒有：
    $$
        |W|=E_0-E(S)
    $$

将 $|W|$ 对末态的熵求导，有：
    $$
        \frac{\p{|W|}}{\p{S}}=-\l(\frac{\p{E}}{\p{S}}\r)_V=-T
    $$

可以看到结果是负的系统末态温度。考虑到温度必须是正数，这说明该导数本身是负的。也就是说，随着末态的熵的增大，系统对外做的功会越来越小。因此，想要让熵最大的方法就是令系统的熵不变，也就是可逆过程。
&emsp;&emsp;因此，我们可以得到结论：系统在按照可逆方式向平衡态过度时所做的功最大。
&emsp;&emsp;接下来我们考虑如何构造一个实际的过程来输出最大功，也就是众所周知的卡诺循环。
&emsp;&emsp;设有两个具有不同温度 $T_1$ 与 $T_2$ 的物体，且 $T_2>T_1$. 首先考虑最简单的过程：直接将两个物体贴在一起。显然该过程不会产生任何的功；且该过程不可逆，因为其会造成 $\displaystyle\delta{S}=\l(\frac{1}{T_1}-\frac{1}{T_2}\r)\delta{E}$ 的熵增。
&emsp;&emsp;因此，为了实现最大功，我们需要一个可以实现某种可你循环过程的“工作物体”引入系统。该物体所要实现的循环过程便是卡诺循环，即：

&emsp;&emsp;**“将该物体等温地从 $T_2$ 处获得部分能量，再绝热地冷却到 $T_1$，再等温地将能量给予 $T_1$ 的物体，再绝热地返回初态”**

&emsp;&emsp;接下来我们可以计算该过程所做的功：首先考虑到整个过程的可逆性，这保证了总熵不变，即 $\delta{S_1}=-\delta{S_2}$；始终取物体获得能量为正，于是有：
    $$
        |\delta{W}|=-\delta{E_2}-\delta{E_1}=-T_1\delta{S_1}-T_2\delta{S_2}=(T_1-T_2)\delta{S_2}
    $$

亦即：
    $$
        |\delta{W}|=\frac{T_2-T_1}{T_2}|\delta{E_2}|
    $$

显然 $|\delta{E_2}|$ 是工作物体从高温热源吸收的热量，于是我们定义 $\displaystyle\eta=\l|\frac{\delta{R}}{\delta{E_2}}\r|$，即有：
    $$
        \eta_{max}=1-\frac{T_1}{T_2}
    $$

即卡诺定理。

----

#### (2).介质中的最大功与热力学不等式

*懒得写了，也懒得看了。*

----

#### (3).勒夏特列原理

&emsp;&emsp;考虑一个由介质和被介质包围的物体组成的闭合系统。设 $S$ 为系统的总熵，并分别记 $x$ 与 $y$ 为以下两个量：当 $\displaystyle\frac{\p{S}}{\p{y}}=0$ 时说明物体本身处于平衡态；而当 $\displaystyle\frac{\p{S}}{\p{y}}=0$ 且 $\displaystyle\frac{\p{S}}{\p{x}}=0$ 时说明物体本身以及物体与介质都处于平衡态。
&emsp;&emsp;考虑熵极大条件与熵增，在平衡状态下我们有：
    $$
        \frac{\p{S}}{\p{x}}=\frac{\p{S}}{\p{y}}=0
        \\\frac{\p^2{S}}{\p{x}^2}\d{x}^2+\frac{\p^2{S}}{\p{y}^2}\d{y}^2+2\frac{\p^2{S}}{\p{x}\p{y}}\d{x}\d{y}>0
    $$

&emsp;&emsp;记：
    $$
        X=-\frac{\p{S}}{\p{x}}
        \\Y=-\frac{\p{S}}{\p{y}}
    $$

即有：
    $$
        X=0\qquad Y=0
    $$

以及：
    $$
        \l(\frac{\p^2{S}}{\p{x^2}}\r)_{y}<0
        \\\l(\frac{\p^2{S}}{\p{y^2}}\r)_{x}<0
        \\
    \begin{aligned}
        \\&\frac{\p^2{S}}{\p{x}^2}\d{x}^2+\frac{\p^2{S}}{\p{y}^2}\d{y}^2+2\frac{\p^2{S}}{\p{x}\p{y}}\d{x}\d{y}<0
    \end{aligned}
    $$

考虑到：
    $$
        \frac{\p^2{S}}{\p{x}^2}\d{x}^2+\frac{\p^2{S}}{\p{y}^2}\d{y}^2\leq2\sqrt{\frac{\p^2{S}}{\p{x}^2}\frac{\p^2{S}}{\p{y}^2}}\d{x}\d{y}
    $$

我们有：
    $$
    \begin{aligned}
        \\&\sqrt{\frac{\p^2{S}}{\p{x}^2}\frac{\p^2{S}}{\p{y}^2}}+\frac{\p^2{S}}{\p{x}\p{y}}<0
    \end{aligned}
    $$

即：
    $$
    \begin{aligned}
        \\&\frac{\p^2{S}}{\p{x}^2}\frac{\p^2{S}}{\p{y}^2}-\l(\frac{\p^2{S}}{\p{x}\p{y}}\r)^2<0
    \end{aligned}
    $$

&emsp;&emsp;接下来我们假定，体系经过了某种不太大的外部作用，导致物体与介质的平衡被破坏，因此体系的熵不再处于极大值，$X=0$ 的条件也因此被破坏。至于量 $y$，则假定它并不受到该作用的直接影响。假设在该影响下 $x$ 变化了 $\Delta{x}$，则在受到作用的那一瞬间，$X$ 的变化量为：
    $$
        (\Delta{X})_y=\l(\frac{\p{X}}{\p{x}}\r)_y\Delta{x}
    $$

&emsp;&emsp;而在 $y$ 不变的情况下，$x$ 的变化仍旧会导致 $Y=0$ 的条件被破坏，也就是物体内部的平衡会被破坏。而在物体内部重新达成新的平衡后，量 $X\equiv\Delta{X}$ 将会取数值：
    $$
        (\Delta{X})_{Y=0}=\l(\frac{\p{X}}{\p{x}}\r)_{Y=0}\Delta{x}
    $$

其中的导数是在 $Y$ 恒定为零的情况下取值的。
&emsp;&emsp;我们比较 $\Delta{X}$ 的这两个数值，并考虑 Jacobi 行列式的性质，我们有：
    $$
        \l(\frac{\p{X}}{\p{x}}\r)_{Y=0}
        =\frac{\p(X,Y)}{\p(x,Y)}
        =\frac{\frac{\p(X,Y)}{\p(x,y)}}{\frac{\p(x,Y)}{\p(x,y)}}
        =\l(\frac{\p{X}}{\p{x}}\r)_y-\frac{\l(\frac{\p{X}}{\p{y}}\r)_x\l(\frac{\p{Y}}{\p{x}}\r)_x}{\l(\frac{\p{Y}}{\p{y}}\r)_x}
    $$

考虑到：
    $$
        \l(\frac{\p{X}}{\p{y}}\r)_x=\l(-\frac{\p^2{S}}{\p{x}\p{y}}\r)_x=\l(\frac{\p{Y}}{\p{x}}\r)_x
    $$

我们有：
    $$
        \l(\frac{\p{X}}{\p{x}}\r)_{Y=0}
        =\frac{\p(X,Y)}{\p(x,Y)}
        =\frac{\frac{\p(X,Y)}{\p(x,y)}}{\frac{\p(x,Y)}{\p(x,y)}}
        =\l(\frac{\p{X}}{\p{x}}\r)_y-\frac{\l(\frac{\p{X}}{\p{y}}\r)^2_x}{\l(\frac{\p{Y}}{\p{y}}\r)_x}
    $$

由于：
    $$
        \l(\frac{\p^2{S}}{\p{y^2}}\r)_{x}<0
        \\\frac{\p^2{S}}{\p{x}^2}\frac{\p^2{S}}{\p{y}^2}-\l(\frac{\p^2{S}}{\p{x}\p{y}}\r)^2<0
    $$

因此我们有：
    $$
        \l(\frac{\p{X}}{\p{x}}\r)_y>\l(\frac{\p{X}}{\p{x}}\r)_{Y=0}>0
    $$

亦即：
    $$
        |(\Delta{X})_y|>|(\Delta{X}_{Y=0})|
    $$

上式称为勒夏特列原理。
&emsp;&emsp;我们将 $x$ 的变化量 $\Delta{x}$ 看作外界对物体作用的量度，而将 $\Delta{X}$ 看作这种作用影响下物体性质变化的量度。上述不等式表明，相比于物体刚刚受到外部作用的时刻其性质的变化，物体回归平衡态后其性质的变化要更小。这说明：使物体离开平衡状态的外部作用，会在物体中引发一些能够减弱该作用的影响的过程。