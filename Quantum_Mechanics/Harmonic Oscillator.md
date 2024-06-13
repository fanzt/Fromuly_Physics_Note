# 1.2 Harmonic Oscillator

![233](./Images/2.png)

> 本章节用于复习谐振子的相关计算，下述所有均采取一维谐振子。
> p.s.鉴于波函数的求解绕不开厄米多项式的相关知识，懒得写了（其实是没学过特殊函数）

## 1.2.1 Schrodinger Equation

第一个方法是直接解谐振子的Schrodinger方程。
首先我们需要求解能级，因而写出定态Schrodinger方程有：
    $$
        \left[-\frac{\hbar^2}{2m}\frac{\mathrm{d}^2}{\mathrm{d}{x}^2}+\frac{1}{2}m\omega^2x^2\right]\psi(x)=E\psi(x)
    $$

进行无量纲化，定义：
    $$
        x_0=\sqrt{\frac{\hbar}{m\omega}}
    $$

并对上式进行化简，有：
    $$
        \left[x_0^2\frac{\mathrm{d}^2}{\mathrm{d}{x}^2}+\frac{2E}{\hbar\omega}-\frac{x^2}{x_0^2}\right]\psi(x)==0
    $$

定义 $\xi=\frac{x}{x_0}$，并记 $\displaystyle\lambda=\frac{2E}{\hbar\omega}$ 有：
    $$
        \frac{\mathrm{d}^2{\psi}}{\mathrm{d}{\xi}^2}+\left(\lambda-\xi^2\right)\psi=0
    $$

直接带入级数解得到的递推关系存在一定困难，因而首先考虑其在 $±\infty$ 处应有的行为。取 $\xi\rightarrow±\infty$，有：
    $$
        \frac{\mathrm{d}^2{\psi}}{\mathrm{d}{\xi}^2}-\xi^2\psi=0
    $$

显然形如 $\displaystyle{e^{±\xi^2/2}}$ 形式的高斯函数是上式的解。考虑到我们要求波函数在无穷远处渐进为零，构造如下形式的试探函数：
    $$
        \psi(\xi)=u(\xi)e^{-\xi^2/2}
    $$

带入Schrodinger方程，有：
    $$
        \frac{\mathrm{d}^2u}{\mathrm{d}{\xi}^2}-2\xi\frac{\mathrm{d}u}{\mathrm{d}{\xi}}+(\lambda-1)u=0
    $$

此时我们便可以带入级数解，容易得到系数的递推关系：
    $$
        c_{k+2}=\frac{2k+1-\lambda}{(k+2)(k+1)}c_k
    $$

考虑到如果满足上述递推关系系数的波函数 $\psi$ 必然不满足无穷远收敛的条件，我们必须要求该系数在某一项截断，即满足对某一 $k$，有：
    $$
        \lambda=2k+1
    $$

亦即：
    $$
        E=\left(k+\frac{1}{2}\right)\hbar\omega
    $$

于是我们获得了谐振子能级的表达式。
而对于谐振子的波函数，通过上式解出的递推方程，有：
    $$
        \psi_n(x)=c_nH_n\left(x\sqrt{\frac{m\omega}{\hbar}}\right)e^{-m\omega{x}^2/2\hbar}
    $$

其中 $H_n(x)$ 为厄米多项式（详见特殊函数概论）。

## 1.2.2 二次量子化

写出Hamiltonian的形式为：
    $$
        H=\frac{p^2}{2m}+\frac{1}{2}m\omega^2x^2
    $$

首先重定义两个约化算符来将Hamiltonian的形式无量纲化
    $$
        X=\sqrt{\frac{m\omega}{\hbar}}x\qquad\qquad{P}=\sqrt{\frac{1}{m\hbar\omega}}p
    $$

于是我们有：
    $$
        H=\frac{1}{2}\hbar\omega\left(X^2+P^2\right)
    $$

并且有正则对易关系：
    $$
        [X,P]=i
    $$

借此无量纲化手法，我们可以将Hamiltonian分解为共轭的两部分：
    $$
    \begin{aligned}
        a&=\frac{1}{\sqrt{2}}(X+iP)
        \\a^\dagger&=\frac{1}{\sqrt{2}}(X-iP)
    \end{aligned}
    $$

计算二者乘积，有：
    $$
    \begin{aligned}
        a^\dagger{a}&=\frac{1}{2}(X-iP)(X+iP)
        \\&=\frac{1}{2}(X^2+iXP-iPX+P^2)
        \\&=\frac{1}{2}(X^2+P^2+i[X,P])
        \\&=\frac{1}{2}(X^2+P^2-1)
    \end{aligned}
    $$

以及：
    $$
    \begin{aligned}
        aa^\dagger&=\frac{1}{2}(X-iP)(X+iP)
        \\&=\frac{1}{2}(X^2+P^2+1)
    \end{aligned}
    $$

于是我们有：
    $$
        H=(a^\dagger{a}+\frac{1}{2})\hbar\omega
    $$

定义 $N=a^\dagger{a}$ 并将该算符的本征矢记为 $|n\rangle$，我们即有：
    $$
        E_n|n\rangle=H|n\rangle=\left(n+\frac{1}{2}\right)\hbar\omega
    $$

同样给出谐振子能谱。而波函数则依据递推关系由 $\langle{x}|{n}\rangle$ 给出。

## 1.2.3 路径积分方法

