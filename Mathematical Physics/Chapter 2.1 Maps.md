# Chapter 2 Maps, Equivalence relation and Linear Space 映射，等价关系与线性空间

![节点](./Images/1.jpg)

----

## $\S$ 2.1.1 Definitions

设 $X$ 与 $Y$ 分别为两个集合，则一个映射（map）$f$ 被定义为对每个 $x\in{X}$ 都指定了一个 $y\in{Y}$ 的规则。我们将其写为：
    $$
        f:X\:\rightarrow\:Y
        \tag{2.1}
    $$

如果 $f$ 通过某个明确的表达式定义，则我们常常将其写为：
    $$
        f:x\:\mapsto\:f(x)
        \tag{2.2}
    $$

显然可能会有不止一个 $X$ 中的元素被映射到同一个 $y\in{Y}$，因此我们定义由映射到 $y\in{Y}$ 的所有 $x$ 构成的 $X$ 的子集为 $y$ 在映射 $f$ 下的原像，记作 $f^{-1}(y)=\{x\in{X}|f(x)=y\}$. 集合 $X$ 称为映射 $f$ 的定义域，而集合 $Y$ 称为该映射的值域。
