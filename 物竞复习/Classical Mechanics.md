# 力学 物竞复习

$$
    \newcommand{dbar}{\delta}
    \newcommand{d}{\mathrm{d}}
    \newcommand{p}{\partial}
    \newcommand{l}{\left}
    \newcommand{r}{\right}
$$

## 1.基本微分方程

$$
    \boldsymbol{F}=m\boldsymbol{a}
$$

## 2.天体

### (1).常用公式

$$
\begin{aligned}
    r&=\frac{p}{1±e\cos{\theta}}
    \\e&=\sqrt{1+\frac{2EL^2}{G^2M^2m^3}}
    \\p&=\frac{L^2}{GMm^2}
    \\T&=2\pi\sqrt{\frac{a^3}{GM}}
\end{aligned}
$$

### (2).LRL矢量

$$
    \boldsymbol{e}=\frac{\boldsymbol{v}\times\boldsymbol{L}}{\alpha}+\hat{r}
$$

其中对于天体运动， $\alpha=-GMm$.

### (3).二体系统

双星系统换单中心天体系统，只需令中心天体质量变为 $M+m$，轨道天体质量变为 $\mu=\frac{Mm}{M+m}$，其余公式直接套用。

## 3.曲率半径

### 1.直角坐标系
    
$$
    \rho=\frac{(1+y'^2)^{\frac{3}{2}}}{|y''|}
$$

参数方程形式：
$$
    \rho=\frac{(x'^2+y'^2)^{\frac{3}{2}}}{|x''y'-y''x'|}
$$

### 2.极坐标系

$$
    \rho=\frac{(r^2+r'^2)^{\frac{3}{2}}}{|2r'^2+r^2-rr''|}
$$

## 4.重弹簧

一级修正（$m\ll{M}$）下，有重弹簧等效于轻弹簧下挂一 $m'=\frac{1}{3}m$ 的重物。

## 5.常见转动惯量

球： $\frac{2}{5}mR^2$
球壳：$\frac{2}{3}mR^2$
圆环：$mR^2$（垂直环面），$\frac{1}{2}mR^2$（平行环面）
椭圆：$\frac{1}{4}m(a^2+b^2)$（垂直圆面）
圆盘：$\frac{1}{2}mR^2$（垂直环面），$\frac{1}{4}mR^2$（平行环面）
圆柱：$\frac{1}{2}mR^2$（沿轴线），$\frac{1}{4}mR^2+\frac{1}{12}ml^2$（垂直轴线）
圆锥：$\frac{3}{10}mR^2$（沿轴线）
椭球：$I_i=\frac{1}{5}m(j^2+k^2)$，$i,j,k$ 取 $a,b,c$.