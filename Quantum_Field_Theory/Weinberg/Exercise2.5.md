# 2+1维时空的单粒子态

> 本文主要内容来自笔者对 Weinberg 量子场论卷一第二章习题 2.5 与 2.6 的解答，如有错误还请读者指正。
> ***本文全篇使用爱因斯坦求和约定，取东海岸度规。***
> ***2+1维时空中的指标取值为0,1,2.***

*首先我不是二次元，其次我不是二次元，最后我不是二次元。败犬女主真好看。*

&emsp;&emsp;众所周知，我们日常生活所接触到的世界一般由三个空间维度与一个时间维度组成，也就是所谓的3+1维时空。基于狭义相对性原理，我们知道3+1维时空中的物理理论必须满足 Poincaré 对称性，亦即在 $O(3,1)$ 群元的变换下不发生改变。依此要求与Wigner基本定理（保证对称变换的幺正/反幺正性），我们可以推导出3+1维时空中的单粒子态。在本文中，我们尝试来探讨一下去除一个空间维度的“二次元”世界，也即2+1维时空中的单粒子态。

## $O(2,1)$ 群及其代数

&emsp;&emsp;显然地，2+1维时空中的 Poincaré 对称性变为了在群 $O(2,1)$ 的变换下物理体系不变。所以我们先来研究群 $O(2,1)$ 的性质。如同群 $O(3,1)$ 的操作一样，群 $O(2,1)$ 有保三维度规 $\eta_{\mu\nu}=diag(-1,1,1)$ 的条件，即：

$$
	\eta_{\mu\nu}{\Lambda^{\mu}}_{\rho}{\Lambda^{\nu}}_{\sigma}=\eta_{\rho\sigma}    	
$$

其中 $\Lambda$ 是群 $O(2,1)$ 的群元。用 $U(\Lambda)$ 表示其对应的幺正变换，显然其应满足乘法规则：

$$
	U(\bar{\Lambda},\bar{a})U(\Lambda,a)=U(\bar{\Lambda}\Lambda,\bar{\Lambda}a+\bar{a})
$$

取无穷小变换 ${\Lambda^{\mu}}_{\nu}={\delta^\mu}_\nu+{\omega^\mu}_\nu$，$a^\rho=\varepsilon^\rho$，并将其展开为幂级数形式：

$$
	U(1+\omega,\varepsilon)=1+\frac{1}{2}i\omega_{\mu\nu}J^{\mu\nu}-i\varepsilon_{\rho}P^{\rho}+\cdot\cdot\cdot
$$

其中生成元 $J^{\mu\nu}$ 与 $P^{\rho}$ 仍旧是厄米算符，且 $\omega_{\mu\nu}$ 与 $J^{\mu\nu}$ 依然是反对称矩阵。考虑如下算式：

$$
	U^{-1}(\Lambda,a)U(1+\omega,\varepsilon)U(\Lambda,a)
$$

我们容易看到，一方面上式等于：

$$
	U^{-1}(\Lambda,a)(1+\frac{1}{2}i\omega_{\rho\sigma}J^{\rho\sigma}-i\varepsilon_{\lambda}P^{\lambda})U(\Lambda,a)
$$

另一方面应用乘法规则再展开后又等于:

$$
	1+\frac{1}{2}i\omega_{\rho\sigma}\left({\Lambda^{\rho}}_{\mu}{\Lambda^{\sigma}}_{\nu}J^{\mu\nu}-{\Lambda^{\rho}}_{\lambda}a^{\sigma}P^{\lambda}\right)-i\varepsilon_{\rho}{\Lambda^{\rho}}_{\lambda}P^{\lambda}
$$

使二者相等，并注意使用 $\omega_{\mu\nu}$ 的反对称性，我们可以得到：

$$
	U^{-1}(\Lambda,a)J^{\rho\sigma}U(\Lambda,a)
    \\={\Lambda^{\rho}}_{\mu}{\Lambda^{\sigma}}_{\nu}J^{\mu\nu}+{\Lambda^{\sigma}}_{\lambda}a^{\rho}P^{\lambda}-{\Lambda^{\rho}}_{\lambda}a^{\sigma}P^{\lambda}
$$

以及：

$$
	U^{-1}(\Lambda,a)P^{\lambda}U(\Lambda,a)={\Lambda^{\lambda}}_{\rho}P^{\rho}
$$

再次取另一组无穷小变换 ${\Lambda^{\mu}}_{\nu}={\delta^\mu}_\nu+{\omega^\mu}_\nu$，$a^\rho=\varepsilon^\rho$，同样注意使用 $\omega_{\mu\nu}$ 的反对称性，我们便可以计算出其生成元的对易关系（看起来和 $O(3,1)$ 的没什么两样）：

$$
\begin{aligned}
	i[J^{\rho\sigma},J^{\mu\nu}]&=\eta^{\rho\mu}J^{\nu\sigma}-\eta^{\rho\nu}J^{\mu\sigma}+\eta^{\sigma\mu}J^{\rho\nu}-\eta^{\sigma\nu}J^{\rho\mu}
    \\i[P^{\lambda},J^{\rho\sigma}]&=\eta^{\rho\lambda}P^{\sigma}-\eta^{\sigma\lambda}P^{\rho}
\end{aligned}
$$

但由于缺少了一个空间维度，实际上的 $J^{\mu\nu}$ 仅剩下了三个独立分量 $J^{01}、J^{02}、J^{12}$，其中前两个对应于 Boost 变换的生成元，而第三个则对应于子群 $SO(2)$ 中的唯一转动生成元。因而实际上的对易关系与3+1维时空中的不大一样。

## 有质量单粒子态

### 小群表示

考虑2+1维Lorentz变换在有质量单粒子态上的作用。我们同样使用 $\sigma$ 标记所有除动量之外的自由度。类似于3+1维的情况，我们有：

$$
\begin{aligned}
	P^{\mu}U(\Lambda)|p,\sigma\rangle&=U(\Lambda)U^{-1}(\Lambda)P^{\mu}U(\Lambda)|p,\sigma\rangle
    \\&=U(\Lambda){\Lambda^{\mu}}_{\nu}P^{\nu}|p,\sigma\rangle
    \\&={\Lambda^{\mu}}_{\nu}p^{\nu}U(\Lambda)|p,\sigma\rangle
\end{aligned}
$$

可见 $U(\Lambda)$ 使一动量为 $p^{\mu}$ 的单粒子态变为动量为 ${\Lambda^{\mu}}_{\nu}p^{\nu}$ 的单粒子态。因而我们有：

$$
	U(\Lambda)|p,\sigma\rangle=\sum_{\sigma'}C_{\sigma'\sigma}|p,\sigma'\rangle
$$

效仿 Weinberg 的做法，我们仍旧使用小群（迷向子群）来获得 $U(\Lambda)$ 的表示。小群被定义为保标准动量 $k^{\mu}$ 不变的 Lorentz 子群。对于有质量粒子，自然地选择标准动量为 $k^{\mu}=(M,0,0)$，以及标准 Lorentz 变换 $L(p)$，使得有 ${L(p)^{\mu}}_{\nu}k^\nu=p^{\mu}$. 2+1维时空中有质量粒子的小群为 $SO(2)$，即我们最熟悉的二维旋转群。 定义一般动量态为：

$$
	|p,\sigma\rangle=\sqrt{\frac{\Lambda{p^0}}{p^0}}U(L(p))|k,\sigma\rangle
$$

其中 $\sqrt{\frac{\Lambda{p^0}}{p^0}}$ 是归一化系数。容易得到：

$$
\begin{aligned}
	&U(\Lambda)|p,\sigma\rangle=\sqrt{\frac{\Lambda{p^0}}{p^0}}U(\Lambda{L(p)})|k,\sigma\rangle
    \\&=\sqrt{\frac{\Lambda{p^0}}{p^0}}U\left(L(\Lambda{p})L^{-1}(\Lambda{p})\Lambda{L(p)}\right)|k,\sigma\rangle
\end{aligned}
$$

容易看出 $L^{-1}(\Lambda{p})\Lambda{L(p)}$ 是保 $k^{\mu}$ 不变的，因而其属于小群 $SO(2)$. 对于小群任意群元 $W$ 的幺正表示，我们总有：

$$
	U(W)|k,\sigma\rangle=\sum_{\sigma'}D(W)_{\sigma'\sigma}|k,\sigma'\rangle
$$

其中 $D(W)_{\sigma'\sigma}$ 是幺正算符 $U(W)$ 的矩阵元。因而我们有：

$$
	U(\Lambda)|p,\sigma\rangle=\sqrt{\frac{\Lambda{p^0}}{p^0}}\sum_{\sigma'}D(W)_{\sigma'\sigma}|\Lambda{p},\sigma\rangle
$$

由于2+1维情况下小群是 $SO(2)$，所以这种情况的矩阵元 $D(W)_{\sigma'\sigma}$ 是显然的，即 $\exp(i\theta\sigma)\delta_{\sigma'\sigma}$，其中 $\theta=\theta(\Lambda,p)$ 依赖于动量与 Lorentz 变换。因此，我们得到了2+1维中有质量单粒子态在 Lorentz 变换下的行为：

$$
	U(\Lambda)|p,\sigma\rangle=\sqrt{\frac{\Lambda{p^0}}{p^0}}\exp(i\theta\sigma)|\Lambda{p},\sigma\rangle
$$

### 反演变换

定义时间反演变换为：

$$
	\mathscr{T}=\begin{pmatrix}
   	-1&0&0
    \\0&1&0
    \\0&0&1
    \end{pmatrix}
$$

空间反演变换为：

$$
	\mathscr{P}=\begin{pmatrix}
    1&0&0
    \\0&-1&0
    \\0&0&-1
    \end{pmatrix}
$$

在不考虑弱相互作用的情况下近似地认为 $\mathscr{T}$ 与 $\mathscr{P}$ 守恒，则我们要求存在：

$$
	\mathcal{P}\equiv{U(\mathscr{P,0})}\qquad\mathcal{T}\equiv{U(\mathscr{T,0})}
$$

使得：

$$
\begin{aligned}
	\mathcal{P^{-1}}U(\Lambda,a)\mathcal{P}=U(\mathscr{P^{-1}}\Lambda\mathscr{P},\mathscr{P}a)
    \\\mathcal{T^{-1}}U(\Lambda,a)\mathcal{T}=U(\mathscr{T^{-1}}\Lambda\mathscr{T},\mathscr{T}a)
\end{aligned}
$$

利用和上述计算 $O(2,1)$ 的幺正算符与生成元对易关系的方法类似，我们可以计算出如下结果：

$$
\begin{aligned}
	\mathcal{P^{-1}}iJ^{\rho\sigma}\mathcal{P}&=i{\mathscr{P}^{\rho}}_{\mu}{\mathscr{P}^{\sigma}}_{\nu}J^{\mu\nu}
    \\\mathcal{P^{-1}}iP^{\tau}\mathcal{P}&=i{\mathscr{P}^{\tau}}_{\rho}P^{\rho}
\end{aligned}
$$

以及：

$$
\begin{aligned}
	\mathcal{T^{-1}}iJ^{\rho\sigma}\mathcal{T}&=i{\mathscr{T}^{\rho}}_{\mu}{\mathscr{T}^{\sigma}}_{\nu}J^{\mu\nu}
    \\\mathcal{T^{-1}}iP^{\tau}\mathcal{T}&=i{\mathscr{T}^{\tau}}_{\rho}P^{\rho}
\end{aligned}
$$

分别取 $\tau$ 指标为 $0$，可以看出为保证正能态，我们必须要求 $\mathcal{P}$ 是线性且幺正的而 $\mathcal{T}$ 是反（线性）幺正的。
因此我们有：

$$
	P^{\mu}\mathcal{P}|k,\sigma\rangle=\mathcal{P}(H,-\mathbf{P})|k,\sigma\rangle={\mathscr{P}^{\mu}}_{\nu}k^{\nu}\mathcal{P}|k,\sigma\rangle
$$

以及：

$$
	J^{12}\mathcal{P}|k,\sigma\rangle=\mathcal{P}J^{12}|k,\sigma\rangle=\sigma\mathcal{P}|k,\sigma\rangle
$$

容易看出，对于有质量粒子，$\mathcal{P}$ 不改变 $P^{\mu}$ 与 $J^{12}$ 的本征值。因此，我们只能有：

$$
	\mathcal{P}|k,\sigma\rangle=\eta_{\sigma}|k,\sigma\rangle
$$

并且我们有：

$$
\begin{aligned}
	\mathcal{P}|p,\sigma\rangle&=\sqrt{\frac{M}{p^0}}U\left(\mathscr{P}L(p)\mathscr{P}^{-1}\right)\mathcal{P}|k,\sigma\rangle
    \\&=\eta_{\sigma}\sqrt{\frac{M}{p^0}}U(L(\mathscr{P}p))|k,\sigma\rangle
    \\&=\eta_{\sigma}|\mathscr{P}p,\sigma\rangle
\end{aligned}
$$

其中 $\eta_{\sigma}$ 是一个模为 $1$ 的相位。但由于2+1维时空中似乎并不存在其余与 $\sigma$ 相关的算符，笔者无法仿照3+1维时空中那样判断 $\eta_{\sigma}$ 是否与 $\sigma$ 无关。若读者有想法欢迎来讨论。

类似的，我们有：

$$
	P^{\mu}\mathcal{T}|k,\sigma\rangle={\mathscr{P}^{\mu}}_{\nu}k^{\nu}\mathcal{T}|k,\sigma\rangle
$$

以及：

$$
	J^{12}\mathcal{T}|k,\sigma\rangle=-\mathcal{T}J^{12}|k,\sigma\rangle=-\sigma\mathcal{T}|k,\sigma\rangle
$$

可见我们有：

$$
	\mathcal{T}|k,\sigma\rangle=\zeta_{\sigma}|k,-\sigma\rangle
$$

以及：

$$
\begin{aligned}
	\mathcal{T}|p,\sigma\rangle&=\sqrt{\frac{M}{p^0}}U\left(\mathscr{T}L(p)\mathscr{T}^{-1}\right)\mathcal{T}|k,\sigma\rangle
    \\&=\zeta_{\sigma}\sqrt{\frac{M}{p^0}}U(L(\mathscr{P}p))|k,-\sigma\rangle
    \\&=\zeta_{\sigma}|\mathscr{P}p,-\sigma\rangle
\end{aligned}
$$

这里的 $\zeta_{\sigma}$ 同样为一个模为 $1$ 的相位。虽然我们仍不知道 $\zeta$ 与 $\sigma$ 的依赖关系，但我们可以重定义 $|k,\sigma\rangle'=\zeta^{1/2}|k,\sigma\rangle$ 来消去这个模长，因而其不具有物理意义。

## 无质量单粒子态

### 小群表示

&emsp;&emsp;对于2+1维的无质量单粒子态，取 $k^{\mu}=(\kappa,0,\kappa)$. 其小群为 $ISO(1)=E(1)$. 该群的表示会导致无质量粒子要么仅有一个连续的“自旋/螺旋度”来标记不同单粒子态，要么不存在可以区分不同单粒子态的“自旋/螺旋度”，仅能依靠其统计性质区分粒子。在这里我们仍旧不希望出现连续的自由度来标记不同粒子态，因而笔者选择了直接使用动量作为区分2+1维单粒子态的唯一自由度，即：

$$
	U(\Lambda)|p\rangle=\sqrt{\frac{\Lambda{p^0}}{p^0}}|\Lambda{p}\rangle
$$

（这样的选择不一定完全合理，如有其他想法欢迎和笔者讨论交流。）


关于2+1维时空中的单粒子态、小群与其表示的更多讨论，读者可以参看参考书目2 (arxiv.org/pdf/1610.08526) 中的4.3节。

### 反演变换

我们仍旧有：

$$
	P^{\mu}\mathcal{P}|k,\sigma\rangle=\mathcal{P}(H,-\mathbf{P})|k,\sigma\rangle={\mathscr{P}^{\mu}}_{\nu}k^{\nu}\mathcal{P}|k,\sigma\rangle
$$

但在无质量情况下 $\mathbf{P}\neq0$ 因而 $\mathcal{P}$ 改变了 $k^{\mu}$. 同样为了方便，我们考虑算符 $U(R_{3}^{-1})\mathcal{P}$，其中 $U(R_3)=\exp(i\pi{J^{12}})$ 为180°旋转变换，其将 $-\mathbf{P}$ 变回 $\mathbf{P}$. 因而 $U(R_{3}^{-1})\mathcal{P}$ 保 $k^{\mu}$ 不变。于是我们有：

$$
	U(R_{3}^{-1})\mathcal{P}|k\rangle=\eta|k\rangle
$$

进一步计算一般动量态，有：

$$
	\mathcal{P}|p\rangle=\mathcal{P}\sqrt{\frac{\Lambda{p^0}}{p^0}}U(L(p))|k\rangle
$$

仍旧取 $L(p)=R(\hat{\mathbf{p}})B\left(\frac{|\hat{\mathbf{p}}|}{\kappa}\right)$，其中 $B\left(\frac{|\hat{\mathbf{p}}|}{\kappa}\right)$ 是在2-方向上的 Boost 而 $R(\hat{\mathbf{p}})=\exp(i\theta{J^{12}})$ 使 2-方向转向 $\hat{\mathbf{p}}$ 方向。因此有：

$$
\begin{aligned}
	\mathcal{P}|p\rangle&=\sqrt{\frac{\Lambda{p^0}}{p^0}}U\left(\mathscr{P}R(\hat{\mathbf{p}})B\left(\frac{|\hat{\mathbf{p}}|}{\kappa}\right)\right)|k\rangle
    \\&=\sqrt{\frac{\Lambda{p^0}}{p^0}}U\left(R(\hat{\mathbf{p}})R_{3}R_{3}^{-1}\mathscr{P}B\left(\frac{|\hat{\mathbf{p}}|}{\kappa}\right)\right)|k\rangle
    \\&=\sqrt{\frac{\Lambda{p^0}}{p^0}}U\left(R(\hat{\mathbf{p}})R_{3}B\left(\frac{|\hat{\mathbf{p}}|}{\kappa}\right)\right)U(R_{3}^{-1}\mathscr{P})|k\rangle
    \\&=\eta\sqrt{\frac{\Lambda{p^0}}{p^0}}U\left(R(\hat{\mathbf{p}})R_{3}B\left(\frac{|\hat{\mathbf{p}}|}{\kappa}\right)\right)|k\rangle
\end{aligned}
$$

不同于3+1维情况额外多出的一个旋转，这里的 $R(\hat{\mathbf{p}})R_{3}$ 刚好就是 $R(-\hat{\mathbf{p}})$. 因此，我们可以直接得到：

$$
	\mathcal{P}|p\rangle=\sqrt{\frac{\Lambda{p^0}}{p^0}}\eta|\mathscr{P}p\rangle
$$

类似的，对于时间反演算符，我们可以得到：

$$
	\mathcal{T}|p\rangle=\sqrt{\frac{\Lambda{p^0}}{p^0}}\zeta|\mathscr{P}p\rangle
$$

----

以上内容即为笔者计算的2+1维时空中的单粒子态情况，如有错误还请指正。

参考书目：

***The Quantum Theory of Fields Volume I***, Steven Weinberg

***BMS Particles in Three Dimensions***, Blagoje Oblak

*封面图源网络，侵删*
