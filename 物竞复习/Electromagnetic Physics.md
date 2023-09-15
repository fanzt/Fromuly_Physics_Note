# 电磁学 物竞复习

$$
    \newcommand{dbar}{\mathrm{d}\kern{-4.3pt}\bar{\small\phantom{q}}\kern{-0.7pt}}
    \newcommand{d}{\mathrm{d}}
    \newcommand{p}{\partial}
    \newcommand{l}{\left}
    \newcommand{r}{\right}
$$

## 1.基本微分方程组

$$
\begin{aligned}
    \nabla\cdot{\boldsymbol{D}}&=\rho_f
    \\\nabla\times{\boldsymbol{E}}&=-\frac{\p{\boldsymbol{B}}}{\p{t}}
    \\\nabla\cdot{\boldsymbol{B}}&=0
    \\\nabla\times\boldsymbol{H}&=\boldsymbol{j}_f+\frac{\p{\boldsymbol{D}}}{\p{t}}
\end{aligned}
$$

## 2.静电场极化

### (1).介质球柱的极化

首先给出静电场的拉普拉斯方程：
    $$
        \nabla^2\varphi=0
    $$

以及球坐标系下轴对称拉普拉斯方程的通解：
    $$
        \varphi=\sum_n\l(A_nr^n+\frac{B_n}{r^{n+1}}\r)P_n(\cos{\theta})
    $$

其中 $P_n(x)$ 是勒让德多项式。
设球外电势分布为 $\varphi_1$，设球内电势分布为 $\varphi_2$.
根据基本微分方程组，我们可以给出本问题的边值关系：
    $$
    \begin{aligned}
        \l.\varphi_1\r|_R&=\l.\varphi_2\r|_R
        \\\varepsilon_1\l.\frac{\p{\varphi_1}}{\p{r}}\r|_R&=\varepsilon_2\l.\frac{\p{\varphi_2}}{\p{r}}\r|_R
    \end{aligned}
    $$

以及边界条件：
    $$
    \begin{aligned}
        \lim_{r\rightarrow\infty}\varphi_1&=-E_0r\cos{\theta}
        \\\lim_{r\rightarrow{0}}\varphi_2&=finity
    \end{aligned}
    $$

将通解带入边界条件，有：
    $$
    \begin{aligned}
        \varphi_1&=-E_0r\cos{\theta}+\sum_n\frac{B_{1n}}{r^{n+1}}P_n(\cos{\theta})
        \\\varphi_2&=\sum_nA_{2n}r^nP_n(\cos{\theta})
    \end{aligned}
    $$

再将通解带入边值关系，有：
    $$
    \begin{aligned}
        -E_0R\cos{\theta}+\sum_n\frac{B_{1n}}{R^{n+1}}P_n(\cos{\theta})=\sum_nA_{2n}R^nP_n(\cos{\theta})
    \end{aligned}
    $$

以及：
    $$
        \varepsilon_1\l(-E_0\cos{\theta}-\sum_n(n+1)\frac{B_{1n}}{R^{n+2}}P_n(\cos{\theta})\r)\\=\varepsilon_2\l(\sum_nnA_{2n}R^{n-1}P_n(\cos{\theta})\r)
    $$

依据勒让德多项式的正交性，进行对比系数，有：
    $$
    \begin{aligned}
        -E_0+\frac{B_{11}}{R^3}&=A_{21}
        \\-\varepsilon_1\l(E_0+2\frac{B_{11}}{R^3}\r)&=\varepsilon_2A_{21}
    \end{aligned}
    $$

联立解得：
    $$
    \begin{aligned}
        B_{11}&=\frac{\varepsilon_2-\varepsilon_1}{\varepsilon_2+2\varepsilon_1}E_0R^3
        \\A_{21}&=-\frac{3\varepsilon_1}{\varepsilon_2+\varepsilon_1}E_0
    \end{aligned}
    $$

于是有：
    $$
    \begin{aligned}
        \varphi_1&=-E_0r\cos{\theta}+\frac{\varepsilon_2-\varepsilon_1}{\varepsilon_2+2\varepsilon_1}\frac{R^3}{r^{2}}E_0\cos{\theta}
        \\\varphi_2&=-\frac{3\varepsilon_1}{\varepsilon_2+\varepsilon_1}E_0r\cos{\theta}
    \end{aligned}
    $$

**以上过程演示了简单情况下拉普拉斯方程的求解。
接下来我们不加证明的给出几个结论方便记忆。**

### (2).介质柱在匀强场的极化

球坐标系下轴对称体系拉普拉斯方程的通解为：
    $$
        \varphi=C_0+D_0\ln{r}+\sum_{n=1}^{\infty}\l(A_n\cos{n\theta}+B_n\sin{n\theta}\r)\l(C_nr^n+D_nr^{-n}\r)
    $$

基于此通解，我们可以得到介质柱在匀强场中的极化：
    $$
    \begin{aligned}
        \varphi_1&=-E_0r\cos{\theta}+\frac{\varepsilon_2-\varepsilon_1}{\varepsilon_2+\varepsilon_1}\frac{R^2}{r}E_0\cos{\theta}
        \\\varphi_2&=-\frac{2\varepsilon_1}{\varepsilon_2+\varepsilon_1}E_0r\cos{\theta}
    \end{aligned}
    $$

## 2.导体椭球的电容

不加证明地给出结论，以便记忆。
    $$
        C=\frac{4\pi\varepsilon_0\sqrt{a^2-c^2}}{F\l(\arcsin{\sqrt{\frac{a^2-c^2}{a^2}}},\sqrt{\frac{a^2-b^2}{a^2-c^2}}\r)}
    $$

其中 $F(\phi,k)$ 为第一类椭圆积分。
*特殊情况*：
旋转椭球面的电容：
    $$
        C=\l\{
            \begin{aligned}
                &\frac{8\pi\varepsilon_0\sqrt{b^2-a^2}}{\ln{\frac{b+\sqrt{b^2-a^2}}{b-\sqrt{b^2-a^2}}}}\qquad b>a
                \\
                \\&\frac{4\pi\varepsilon_0\sqrt{a^2-b^2}}{\arcsin{\frac{\sqrt{a^2-b^2}}{a}}}\qquad b<a
            \end{aligned}
        \r.
    $$

## 3.轴对称磁场的相关性质

考虑与 $\theta$ 无关的轴对称磁场，根据磁场散度为零，我们有：
    $$
        \frac{1}{\rho}\frac{\p{(\rho{B_\rho})}}{\p{\rho}}+\frac{\p{B_z}}{\p{z}}=0
    $$

认为 $\displaystyle\frac{\p{B_z}}{\p{z}}$ 近似不变，我们就有：
    $$
        B_\rho\approx-\frac{\rho}{2}\frac{\p{B_z}}{\p{z}}
    $$

该关系在磁镜等情况下十分常用。

## 4.偶极子相关

偶极子产生的势与场：
    $$
    \begin{aligned}
        \varphi&=\frac{1}{4\pi\varepsilon_0}\frac{\boldsymbol{p}\cdot\boldsymbol{r}}{r^3}
        \\\boldsymbol{E}&=\frac{1}{4\pi\varepsilon_0}\frac{p}{r^3}(2\cos{\theta}\hat{r}+\sin{\theta}\hat{\theta})
    \end{aligned}
    $$

偶极子在外场中的性质：
    $$
    \begin{aligned}
        E_p&=-\boldsymbol{p}\cdot\boldsymbol{E}
        \\\boldsymbol{F}&=(\boldsymbol{p}\cdot\nabla)\boldsymbol{E}
        \\\boldsymbol{M}&=\boldsymbol{p}\times\boldsymbol{E}\quad(力偶矩)
    \end{aligned}
    $$

## 5.介质的微观解释

&emsp;&emsp;考虑一个充满分子小球的气体，对该气体施加一个外场，则其中的每个小球都会受到一个场的作用而产生极化，于是整个气体宏观上便会产生极化，考虑研究宏观的极化性质与微观的粒子极化之间的关系。
&emsp;&emsp;假设分子数密度为 $n$，每个分子小球在感受到外电场后会产生偶极矩，满足：
    $$
        \boldsymbol{p}=\alpha\boldsymbol{E_{micro}}
    $$

依据极化强度矢量的定义，有：
    $$
        \boldsymbol{P}=\frac{N\boldsymbol{p}}{V}=n\boldsymbol{p}
    $$

以及宏观极化性质：
    $$
        \boldsymbol{P}=\chi\epsilon_0\boldsymbol{E_{macro}}
    $$

认为小球所感受到的电场与小球本身的电场叠加后产生宏观外电场，于是有：
    $$
        \boldsymbol{E_{micro}}-\frac{\boldsymbol{P}}{3\varepsilon_0}=\boldsymbol{E_{macro}}
    $$

于是我们有：
    $$
        \boldsymbol{E_{micro}}-\frac{n\alpha\boldsymbol{E_{micro}}}{3\varepsilon_0}=\frac{n\alpha\boldsymbol{E_{micro}}}{\chi\varepsilon_0}
    $$

得出：
    $$
        \chi=\frac{n\alpha}{(1-\frac{n\alpha}{3\varepsilon_0})\varepsilon_0}
    $$

认为分子是导体球，带入 $\alpha=4\pi{R^3}\varepsilon_0$，有：
    $$
        \chi=\frac{4\pi{R^3}n}{1-\frac{4\pi{R^3}n}{3}}
    $$

## 6.等离子体震荡与等离子体波