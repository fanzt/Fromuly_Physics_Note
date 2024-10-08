# Chapter 2 Maps, Equivalence relation, Group and Linear Space

![节点](./Images/1.jpg)

----

## $\S$ 2.1 Maps and Equivalence relation

### $\S$ 2.1.1 映射的基本概念

*我们先来讲一些小学生都非常懂的简单东西。*

#### $\S$ 2.1.1.1 映射；定义域、值域、原像、像

&emsp;&emsp;设 $X$ 与 $Y$ 分别为两个集合，则一个映射（map）$f$ 被定义为对每个 $x\in{X}$ 都指定了一个 $y\in{Y}$ 的规则。我们将其写为：
    $$
        f:X\:\rightarrow\:Y
    $$

如果 $f$ 通过某个明确的表达式定义，则我们常常将其写为：
    $$
        f:x\:\mapsto\:f(x)
    $$

&emsp;&emsp;显然可能会有不止一个 $X$ 中的元素被映射到同一个 $y\in{Y}$，因此我们定义由映射到 $y\in{Y}$ 的所有 $x$ 构成的 $X$ 的子集为 $y$ 在映射 $f$ 下的原像，记作 $f^{-1}(y)=\{x\in{X}|f(x)=y\}$. 集合 $X$ 称为映射 $f$ 的定义域，而集合 $Y$ 称为该映射的值域。
&emsp;&emsp;集合的像被定义为 $f(X)=\{y\in{Y}|y=f(x),x\in{X}\}$，也常记为 $\mathrm{Im}{f}$.
&emsp;&emsp;需要注意的是，映射的像必须在选定了定义域与值域的情况下才可以被定义。

----

#### $\S$ 2.1.1.2 单射、满射、双射与常映射

&emsp;&emsp;接下来我们介绍几种符合特定情况的映射。

> &emsp;
> *定义 2.1:*
>
> 1. 如果一个映射符合 $\forall x\neq{x'}$ 都有 $f(x)\neq{f(x')}$，则称该映射为一个单射（或称为“一一的”）；
> 2. 如果一个映射符合 $\forall y\in{Y}$ 都有至少一个 $x\in{X}$ 使得 $f(x)=y$，则称该映射为一个满射（或称为“到上的”）；
> 3. 如果一个映射既是单射又是满射，则称其为双射（一一且到上的）。
> 4. 一个常映射 $c:X\rightarrow{Y}$ 被定义为 $c(x)=y_0$，其中 $y_0$ 是一个 $Y$ 中的固定元素，而 $x$ 则是 $X$ 中的任意一个元素。

----

#### $\S$ 2.1.1.3 限制映射与映射的复合

&emsp;&emsp;对于一个映射，我们可以考虑将其的值域限制为 $A\subset{X}$，在这样限制下的映射记为 $f|_A:A\rightarrow{Y}$.
&emsp;&emsp;给定两个映射 $f:X\rightarrow{Y}$ 以及 $g:Y\rightarrow{Z}$，二者的复合记为 $g\:\circ\:f:X\rightarrow{Z}$ 被定义为 $g\:\circ\:f(x)=g(f(x))$.

----

#### $\S$ 2.1.1.4 同态与同构

&emsp;&emsp;考虑在集合 $X$ 与 $Y$ 上分别附加某个特定的代数结构（例如某种加法或者乘法）。如果一个映射 $f:X\rightarrow{Y}$ 是保代数结构的，则我们称 $f$ 是一个同态。
> 例如：我们在 $X$ 与 $Y$ 上定义出“乘法”，分别记为 $\mathop{\times}\limits_{X}$ 与 $\mathop{\times}\limits_{Y}$。如果对于映射 $f$，我们有 $f(a\mathop{\times}\limits_{X}b)=f(a)\mathop{\times}\limits_{Y}f(b)$，则该映射将是一个同态。

&emsp;&emsp;而如果一个映射既是同态又是双射，则我们就称该映射为一个同构，并将集合 $X$ 与 $Y$ 称为相互同构的，记为 $x\cong{y}$.

----

### $\S$ 2.1.2 等价关系与等价类

*接下来讲一些小学生可能不是非常懂的东西。*

#### $\S$ 2.1.2.1 等价关系的定义

&emsp;&emsp;在数学中，我们所需要的最重要的概念之一就是等价关系与等价类。等价关系将告诉我们在什么情况下可以认为两个对象之间是“相等”的。

> &emsp;&emsp;
> *定义 2.2：* 如果一个记为 $\sim$ 的关系满足以下条件，则该关系就被称为一种等价关系。
>
> 1. $a\sim{a}$ （反身性）
> 2. 如果 $a\sim{b}$，则 $b\sim{a}$（对称性）
> 3. 如果 $a\sim{b}$，且 $b\sim{c}$，则 $a\sim{c}$ （传递性）

&emsp;&emsp;例如，如果我们定义一个关系 $\sim$ 为：如果两个整数 $a$ 和 $b$ 除以二的余数相同，则我们认为二者有关系 $a\sim{b}$. 可以证明该关系为一个等价关系：
> &emsp;&emsp;首先对于整数 $a$ 显然有 $a$ 除以二的余数等于$a$ 除以二的余数，即有 $a\sim{a}$；
> &emsp;&emsp;其次显然如果 $a$ 除以二的余数和 $b$ 除以二的余数相同，则 $b$ 除以二的余数和 $a$ 除以二的余数相同，即对于 $a\sim{b}$ 总有 $b\sim{a}$；
> &emsp;&emsp;最后显然如果 $a$ 除以二的余数与 $b$ 除以二的余数相同，且 $b$ 除以二的余数和 $c$ 除以二的余数相同，则 $a$ 除以二的余数和 $c$ 除以二的余数相同，即对于 $a\sim{b}$，$b\sim{c}$ 总有 $a\sim{c}$.

----

#### $\S$ 2.1.2.2 等价类、商空间

&emsp;&emsp;对于一个给定的集合 $X$ 和一个给定的等价关系 $\sim$，我们可以将 $X$ 分割为一系列互不相交的子集，称为等价类，记为 $[a]$. 等价类 $[a]$ 被定义为所有满足 $x\in{X}$ 且 $x\sim{a}$ 的 $x$ 构成的集合，即：
    $$
        [a]=\{x\in{X}|x\sim{a}\}
    $$

其中 $a$ 被称作 $[a]$ 的代表元。
&emsp;&emsp;等价类有以下两个特点：

> 1. 等价类 $[a]$ 永远不可能是空集，因为其中至少有一个元素 $a$ 满足 $a\in{X}$ 且 $a\sim{a}$
> 2. 如果对于两个等价类 $[a]$ 和 $[b]$，我们有 $[a]\cap[b]\neq\emptyset$，则 $[a]=[b]$

&emsp;&emsp;对于集合 $X$，其所有等价类组成的集合叫做 $X$ 的商空间，记作 $X/\sim$.

----

#### $\S$ 2.1.2.3 商空间的几何意义

&emsp;&emsp;事实上，商空间所代表的几何意义便是所谓的“认同”或者“粘合”操作。上文中我们写到，商空间被定义为某一集合中所有等价类组成的新集合。这实质上是把某一等价类中的所有元素（即几何空间中的“点”）认同为一个元素（点），也就意味着所谓的“粘合”操作。
&emsp;&emsp;例如，对于一个闭圆盘 $D^2=\{(x,y)\in\mathbb{R}^2|x^2+y^2\leq1\}$，对其商掉边缘 $S^1=\{(x,y\in\mathbb{R}^2|x^2+y^2=1\}$，就相当于将整个圆盘的边缘粘成一个点，因而我们就可以得到三维空间中的二维球面 $S^2$. 进一步的，我们总有 $D^n/S^{n-1}=S^n$. 

----

> *练习1* 令 $\mathrm{H}$ 一上半复平面 $\{\tau\in\mathbb{C}|\mathrm{Im}{\:\tau}\geq{0}\}$. 定义群: 
> $$
> \mathrm{SL}(2,\mathbb{Z})\equiv\left\{
>   \begin{pmatrix}
>           a & b
>           \\c & d
>   \end{pmatrix}\right|\left.\begin{matrix}\\\\\end{matrix}a,b,c,d\in\mathbb{Z},ad-bc=1\right\}
>$$
> 再定义关系 $\sim$，对于 $\tau,\tau'\in\mathrm{H}$，若满足存在矩阵 $\mathbf{A}\in{\mathrm{SL}(2,\mathbb{Z})}$，使得:
> $$
>   \tau'=(a\tau+b)/(c\tau+d)
> $$
> 则称 $\tau\sim\tau'$
> 证明这是一个等价关系。
> *证明*：
> 1.反身性：取 $\mathbf{A}=\mathbf{I}=diag(1,1)=\delta^i_j$ 即可.
> 2.对称性：设 $\mathbf{A}=\begin{pmatrix}
>           a & b
>           \\c & d
>   \end{pmatrix}$, $\mathbf{A'}=\begin{pmatrix}
>           a' & b'
>           \\c' & d'
>   \end{pmatrix}$，应有：$\displaystyle(a'\frac{a\tau+b}{c\tau+d}+b')/(c'\frac{a\tau+b}{c\tau+d}+d')=\tau$，化简并令 $\tau$ 的相同次幂项的系数为0，并要求其属于 $\mathrm{SL}(2,\mathbb{Z})$ 即有：
> $$
> \begin{aligned}
>     c'a+d'c=0
>     \\c'b+d'd-a'a-b'c=0
>     \\a'b+b'd=0
>     \\a'd'-b'c'=1
> \end{aligned}
> $$
> 解得 $a'=\pm{d}$，$b'=\mp{b}$，$c'=\mp{c}$，$d'=\pm{a}$
> 因而取 $\mathbf{A'}=\mathbf{A}^{-1}$ 或 $-\mathbf{A}^{-1}$ 即可。
> 3.传递性
> 设 $\mathbf{A}=\begin{pmatrix}
>           a_{11} & a_{12}
>           \\a_{21} & a_{22}
>   \end{pmatrix}$，$\mathbf{B}=\begin{pmatrix}
>           b_{11} & b_{12}
>           \\b_{21} & b_{22}
>   \end{pmatrix}$ 满足 $a_{11}a_{22}-a_{12}a_{21}=b_{11}b_{22}-b_{12}b_{21}=1$，令 $a=\displaystyle\frac{a_{11}b+a_{12}}{a_{21}b+a_{22}}$，$b=\displaystyle\frac{b_{11}c+b_{12}}{b_{21}c+b_{22}}$，即有 $c\sim{b}$，$b\sim{a}$，代入化简，则有：
> $$
>   a=\frac{(a_{11}b_{11}+a_{12}b_{21})c+(a_{11}b_{12}+a_{12}b_{22})}{(a_{21}b_{11}+a_{22}b_{21})c+(a_{21}b_{12}+a_{22}b_{22})}
> $$
> 且有：
> $$
> \begin{aligned}
>   &(a_{11}b_{11}+a_{12}b_{21})(a_{21}b_{12}+a_{22}b_{22})-(a_{11}b_{12}+a_{12}b_{22})(a_{21}b_{11}+a_{22}b_{21})
\\&=(a_{11}b_{11}a_{22}b_{22}-a_{12}b_{22}a_{21}b_{11})+(a_{11}b_{12}a_{22}b_{21}-a_{12}b_{22}a_{21}b_{11})
\\&+a_{11}b_{11}a_{21}b_{12}+a_{12}b_{21}a_{22}b_{22}-a_{11}b_{12}a_{21}b_{11}-a_{12}b_{22}a_{22}b_{21}
\\&=(a_{11}a_{22}-a_{12}a_{21})(b_{11}b_{22}-b_{12}b_{21})
\\&=1
> \end{aligned}
> $$
> 因而取 $\mathbf{C}=\begin{pmatrix}
>           a_{11}b_{11}+a_{12}b_{21} & a_{11}b_{12}+a_{12}b_{22}
>           \\a_{21}b_{11}+a_{22}b_{21} & a_{21}b_{12}+a_{22}b_{22}
>   \end{pmatrix}=\mathbf{AB}$，即可有 $c\sim{a}$.
>

----

### $\S$ 2.1.3 群、陪集、正规子群与商群

*群主在哪里？管理在哪里？涩图又在哪里？？*

#### $\S$ 2.1.3.1 群

> *定义 2.3：* 给定某集合 $G$ 以及于其上定义的二元运算 $\cdot:G\times{G}\rightarrow{G}$ （称为群乘法），若其符合以下条件，则称 $G$ 与其上的二元运算结构构成一个群：
>
> 1. $\forall{a,b}\in{G}，a\cdot{b}\in{G}$（封闭性）;
> 2. $\forall{a,b,c}\in{G},(a\cdot{b})\cdot{c}=a\cdot{(b\cdot{c})}$（结合律）;
> 3. $\exists{e}\in{G},s.t.\forall{g}\in{G},e\cdot{g}=g\cdot{e}=g$（单位元）;
> 4. $\forall{g}\in{G},\exists{g^{-1}}\in{G},s.t.{g^{-1}\cdot{g}=g\cdot{g}^{-1}=e}$（逆元）.

#### $\S$ 2.1.3.2 陪集、正规子群与商群

## $\S$ 2.2 Vector Space and Linear Algebra
