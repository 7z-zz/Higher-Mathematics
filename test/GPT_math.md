# 根式乘积的极限

## 题目

计算题图中的例 2：

$$
\lim_{x\to1}
\frac{(1-x^{\frac12})(1-x^{\frac13})\cdots(1-x^{\frac1n})}
{(1-x)^{n-1}}.
$$

按题意，$n$ 为固定整数，$n\ge2$。在实数范围内，原式要求 $x\ge0$ 且 $x\ne1$；求极限时可在 $1$ 附近取 $x>0$、$x\ne1$，左右两侧均有定义。

## 思路

当 $x\to1$ 时，分子、分母都趋于 $0$，直接代入得到 $\frac00$ 型未定式。

分子从 $k=2$ 到 $k=n$ 共有 $n-1$ 个因子，正好可以把分母中的 $n-1$ 个 $1-x$ 分别配给它们。每个比值 $\frac{1-x^{1/k}}{1-x}$ 都能用幂差公式约去零因子，因此选用因式分解求极限。

## 解答

先将原式写成

$$
\frac{(1-x^{\frac12})(1-x^{\frac13})\cdots(1-x^{\frac1n})}
{(1-x)^{n-1}}
=\frac{1-x^{\frac12}}{1-x}
\cdot\frac{1-x^{\frac13}}{1-x}
\cdots\frac{1-x^{\frac1n}}{1-x}.
$$

对任意固定的 $k\in\{2,3,\ldots,n\}$，利用幂差公式，有

$$
\begin{aligned}
1-x
&=1-\left(x^{\frac1k}\right)^k\\
&=(1-x^{\frac1k})
\left(1+x^{\frac1k}+x^{\frac2k}+\cdots+x^{\frac{k-1}{k}}\right).
\end{aligned}
$$

在 $x>0$、$x\ne1$ 时，$1-x^{1/k}\ne0$，所以可以约去该因子，得到

$$
\frac{1-x^{\frac1k}}{1-x}
=\frac{1}{1+x^{\frac1k}+x^{\frac2k}+\cdots+x^{\frac{k-1}{k}}}.
$$

当 $x\to1$ 时，右侧分母中的 $k$ 项都趋于 $1$，分母趋于非零数 $k$，故

$$
\lim_{x\to1}\frac{1-x^{\frac1k}}{1-x}=\frac1k.
$$

由于 $n$ 固定，原式只有有限个因子，且各因子的极限都存在，因此由极限的乘法法则，

$$
\boxed{
\lim_{x\to1}
\frac{(1-x^{\frac12})(1-x^{\frac13})\cdots(1-x^{\frac1n})}
{(1-x)^{n-1}}
=\frac12\cdot\frac13\cdots\frac1n
=\frac1{n!}
}.
$$

这里 $n!=1\cdot2\cdots n$。约分是在 $x\ne1$ 时进行的；化简后的式子在 $x=1$ 有定义，并不表示原式在该点也有定义。
