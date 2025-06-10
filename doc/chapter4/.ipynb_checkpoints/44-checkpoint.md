# Section 4.4

Remember:

:::{prf:definition}
:label: basicLogNote
* The common logarithm is $\log_{10}(x)=\log(x)$.
* The natural logarithm is $\log_{e}(x)=\ln(x)$.
:::

:::{prf:theorem} Change Base Formula
:label: changeBase
For any positive real number $x$, $a$, and $b$ where $a\ne 1$ and $b\ne 1$, the following holds true.

$$\log_a(x)=\frac{\log_b(x)}{\log_a(x)}$$
:::

Consider, $2^x=7$ if and only if $\log_2(7)=x$. However, most simple scientific calculators are not able to compute this number. With the change base formula, we have:

$$\log_2(7)=\frac{\ln(7)}{\ln(2)}$$

That is, $\log_2(7)\approx 2.80735$ and $\frac{\ln(7)}{\ln(2)} \approx 2.80735$.