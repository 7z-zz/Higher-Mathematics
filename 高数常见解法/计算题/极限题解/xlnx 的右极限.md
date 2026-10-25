# 题目

$$
\lim_{x\to0^+}x\ln x
$$

# 观察

当 $x\to0^+$ 时，

$$
x\to0,\qquad \ln x\to-\infty.
$$

这属于 $0\cdot\infty$ 型未定式。这里的无穷大实际是 $-\infty$，不能看到一个因子趋于 $0$，就直接认为乘积也趋于 $0$。

可以考虑把乘积改写成 $\dfrac{\infty}{\infty}$ 型或者 $\dfrac00$ 型，再用洛必达法则。

## 把乘积转成商

现在 $x$ 趋于 $0$，它的倒数 $\dfrac1x$ 就趋于 $+\infty$。把乘以 $x$ 改成除以 $\dfrac1x$：

$$
x\ln x=\frac{\ln x}{\frac1x}\qquad(x>0).
$$

此时分子趋于 $-\infty$，分母趋于 $+\infty$，就变成了 $\dfrac{\infty}{\infty}$ 型。

选择这种写法，是因为 $\ln x$ 求导后变成 $\dfrac1x$，分母求导后变成 $-\dfrac1{x^2}$，两者相除很容易化简：

$$
\frac{(\ln x)'}{\left(\frac1x\right)'}
=\frac{\frac1x}{-\frac1{x^2}}
=-x\longrightarrow0\qquad(x\to0^+).
$$

在 $(0,1)$ 内，分子、分母都可导，分母的导数 $-\dfrac1{x^2}\ne0$，并且导数之比的极限存在，所以可以使用洛必达法则。

# 最终

$$
\boxed{
\lim_{x\to0^+}x\ln x
=\lim_{x\to0^+}\frac{\ln x}{\frac1x}
=\lim_{x\to0^+}\frac{\frac1x}{-\frac1{x^2}}
=\lim_{x\to0^+}(-x)
=0
}.
$$

本题的关键是把趋零因子取倒数，放到分母，让乘积变成可以使用洛必达法则的商式。两种改写方向与选择方法见 [[3. 0 乘 inf：化乘积为商|0乘无穷型：化乘积为商]]。
