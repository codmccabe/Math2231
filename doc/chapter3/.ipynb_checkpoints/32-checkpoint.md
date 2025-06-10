# Section 3.2

## Real Number Division Algorithm

:::{prf:definition} Division Algorithm (Real Numbers)
:label: divAlgRealNumbers
Let $a$ and $b$ be any real number where $b\ne0$. Then there exists a unique real number $q$ and $r$ such that 

$$a=b\cdot q+r$$

where $0<r<b$ or $r=0$.
:::

:::{prf:example}
:label: divExample1
If we look at $12$ and $3$ we know that

$$12=3\cdot 4 + 0$$

This can be shown by doing long division:

\begin{alignat*}{10}
& \phantom{11}4\\
3 & )\overline{12}\\
- & \underline{\phantom{)}12} & \leftarrow4(3)\phantom{--}\\
 & \phantom{)1}0 & \leftarrow12-12
\end{alignat*}

If we look at $13$ and $3$ we know that

$$13 = 3\cdot 4 + 1$$

This can be shown by doing long division:

\begin{alignat*}{10}
& \phantom{11}4\\
3 & )\overline{13}\\
- & \underline{\phantom{)}12} & \leftarrow4(3)\phantom{--}\\
 & \phantom{)1}1 & \leftarrow13-12
\end{alignat*}
:::

Since the division algorithm for real numbers is $a=bq+r$ we know that if we divide both sides by $b$ we have

$$\frac{a}{b} = q+\frac{r}{b}$$

We will use this fact to rewrite polynomial over polynomial expressions later on. For example, we know that $13=3(4)+1$. If we divide both sides by $3$ we have: $\frac{13}{3} = 4+\frac{1}{3}$.

## Division Algorithm for Polynomials

:::{prf:definition} Division Algorithm for Polynomials
:label: divAlgPolynomial
Let $f(x)$ and $g(x)$ be polynomials with $g(x)$ of lesser degree than $f(x)$ and $g(x)$ is of degree one or higher. Then there exists a unique $q(x)$ and $r(x)$ such that 

$$f(x)=g(x)\cdot q(x)+r(x)$$

where $0<\text{deg}(r(x))<\text{deg}(g(x))$ or $\text{deg}(r(x))=0$.
:::

:::{prf:example}
:label: polyLongExam1
If we look at $x^2+3x+2$ and $x+1$ we know that 

$$x^2+3x+2=(x+1)(x+2)+0$$ 

by factoring $x2+3x+2$. This can also be done by polynomial long division.

\begin{alignat*}{10}
 & \phantom{)x^{2}+)}x+2\\
x+1 & )\overline{x^{2}+3x+2}\\
- & \underline{\phantom{)}x^{2}+x} & \leftarrow x(x+1)\phantom{)-(x^{2}+x)}\\
 & \phantom{)x^{2}+)}2x+2 & \leftarrow(x^{2}+3x)-(x^{2}+x)\\
 & \underline{-\phantom{x^{2}))}2x+2} & \leftarrow2(x+1)\phantom{))))(2x+2}\\
 & \phantom{-x^{2}))2x+)}0 & \leftarrow(2x+2)-(2x+2)
\end{alignat*}
:::

From the previous example, we also know that

$$\frac{x^2+3x+2}{x+1}=(x+2)$$

Let's do another polynomial long-division problem.

::::{prf:example}
:label: polyLongExam2
Use polynomial long division to evaluate $\frac{3x^3-2x^2-150}{x^2-4}$.
:::{dropdown} Solution:
We should first notice that the numerator and denominator are missing an $x$ term. This would be like saying $12$ is the same as $102$. Therefore, we must first rewrite the quotient.

$$\frac{3x^3-2x^2+0x-150}{x^2+0x-4}$$

Next, we have the following setup

\begin{align*}
x^{2}+0x-4 & )\overline{3x^{3}-2x^{2}+0x-150}
\end{align*}

Then we start the polynomial long division

\begin{alignat*}{10}
 & \phantom{)3x^{3}-2x^{2}+)}3x-2\\
x^{2}+0x-4 & )\overline{3x^{3}-2x^{2}+0x-150}\\
- & \underline{\phantom{)}3x^{3}-0x^{2}-12x} & \leftarrow3x(x^{2}+0x-4)\phantom{x)-(3x^{3}-2x^{2}-12)}\\
 & \phantom{)3^{3}}-2x^{2}+12x-150 & \leftarrow(3x^{3}-2x^{2}+0x)-(3x^{3}-2x^{2}-12x)\\
- & \underline{\phantom{xx}-2x^{2}+0x\phantom{x}+8} & \leftarrow-2(x^{2}+0x-4)\phantom{150)-(-2x^{2}+0x+))}\\
 & \phantom{xxxxxxxx}12x-158 & \leftarrow(-2x^{2}+12x-150)-(-2x^{2}+0x+8)\\
\end{alignat*}

Therefore, we have

$$\frac{3x^3-2x^2-150}{x^2-4}=3x-2+\frac{12x-158}{x^2-4}$$
:::
::::

## Synthetic Division

In **special cases**, we can use a method called synthetic division instead of polynomial long division. We can use synthetic division when a polynomial is divided by a binomial $x-k$. This means the previous example could not be done by synthetic division.

Consider the following polynomial long division of $\frac{3x^3-2x^2+0x-150}{x-4}$. Notice that the denominator satisfied the $x-k$ requirement. We then have

\begin{alignat*}{10}
 & \phantom{)3x^{3}-}3x^{2}+10x+40\\
x-4 & )\overline{3x^{3}-2x^{2}\phantom{xx}+0x-150}\\
- & \underline{\phantom{x}3x^{3}-12x^{2}} & \leftarrow3x^{2}(x-4)\phantom{x)-(3x^{3}-2x^{2}-12xxxx)}\\
 & \phantom{)3^{3}xxxx}10x^{2}+0x & \leftarrow(3x^{3}-2x^{2}+0x)-(3x^{3}-2x^{2}-12x)\\
- & \underline{\phantom{xxxxxx}10x^{2}-40x} & \leftarrow-2(x^{2}+0x-4)\phantom{150)-(-2x^{2}+0x+))}\\
 & \phantom{xxxxxxxxxxx}40x-150 & \leftarrow(-2x^{2}+12x-150)-(-2x^{2}+0x+8)\\
- & \underline{\phantom{xxxxxxxxxxx}40x-160} & \leftarrow40(x-4)\phantom{0)-(4x-160xxxxxxxxxxx)}\\
 & \phantom{xxxxxxxxxxxxxxxx}10 & \leftarrow(40x-150)-(4x-160)\phantom{xxxxxxxxxx)}
\end{alignat*}

Next, we want to do this again but remove all the $x^n$ factors.

\begin{alignat*}{10}
& \phantom{)3x^{3}-}3\phantom{xx}10\phantom{xxxx}40\\
-4 & )\overline{3\phantom{xx}-2\phantom{xx}0\phantom{x}-150}\\
- & \underline{\phantom{)}3\phantom{xx}-4}\\
 & \phantom{)3^{3}}10\phantom{xxxx}0\\
- & \underline{\phantom{xxx}10\phantom{xxx}40}\\
 & \phantom{xxxxxxxx}40\phantom{x}-150\\
- & \underline{\phantom{xxxxxxxx}40\phantom{x}-160}\\
 & \phantom{xxxxxxxxxxxxx}10
\end{alignat*}

where $q(x)=3x^2+10x+40$ and $r(x)=10$ still. We can still remove some items from the work:

\begin{alignat*}{10}
 & \phantom{)3x^{3}-}3\phantom{xx}10\phantom{xxxx}40\\
-4 & )\overline{3\phantom{xx}-2\phantom{xx}0\phantom{x}-150}\\
- & \underline{\phantom{)}\phantom{xxx}-4}\\
 & \phantom{)3^{3}xx}10\phantom{xxxx}\\
- & \underline{\phantom{xxxxi}10\phantom{xx}40}\\
 & \phantom{xxxxxxxx}40\phantom{x}\\
- & \underline{\phantom{xxxxxxxx}40\phantom{x}-160}\\
 & \phantom{xxxxxxxxxxxxx}10
\end{alignat*}

Next, we can smash everything together to get

\begin{align*}
 & \phantom{)3x^{3}-}3\phantom{xx}10\phantom{xxxx}40\\
-4 & )\overline{3\phantom{xx}-2\phantom{xxxxx}0\phantom{x}-150}\\
- & \underline{\phantom{xxx}-12\phantom{xx}-40\phantom{x}-160}\\
 & \phantom{xxxxx}10\phantom{xxxx}40\phantom{xxx}10
\end{align*}

Finally, if we use $4$ instead of $-4$ and add down instead of subtract down we have synthetic division:

\begin{align*}
 & \phantom{)3x^{3}-}3\phantom{xxxxx}10\phantom{xxxx}40\\
4 & )\overline{3\phantom{xx}-2\phantom{xxxxx}0\phantom{x}-150}\\
+ & \underline{\phantom{xxxxx}12\phantom{xxxx}40\phantom{xxx}160}\\
 & \phantom{xxxxx}10\phantom{xxxx}40\phantom{xxxx}10
\end{align*}

Again, doing this shows that $q(x)=3x^2+10x+40$ and $r(x)=10$. We also have

$$\frac{3x^3-2x^2+0x-150}{x-4}=3x^2+10x+40+\frac{10}{x-4}$$

### Synthetic Division Examples

::::{prf:example}
:label: synDivExam1
Rewrite $\frac{5x^3-6x^2-28x-2}{x+2}$ as $q(x)+\frac{r(x)}{x+2}$.
:::{dropdown} Solution:
In this case $x-k$ we have $x+2=x-(-2)$. This means $k=-2$.

\begin{align*}
 & \phantom{xxxxxx}5\phantom{xx}-16\phantom{xxxx}4\\
-2 & )\overline{5\phantom{xx}-6\phantom{xx}-28\phantom{xx}-2}\\
+ & \underline{\phantom{xxx}-10\phantom{xxxx}32\phantom{xx}-8}\\
 & \phantom{xxx}-16\phantom{xxxxx}4\phantom{xx}-10
\end{align*}

Therefore,

$$\frac{5x^3-6x^2-28x-2}{x+2} = 5x^2 -16x +4 + \frac{-10}{x+2}$$
:::
::::

::::{prf:example}
:label: synDivExam2
Evaluate $\frac{5x^3-6x^2+3x}{x-1}$
:::{dropdown} Solution:
Here $k=1$.

\begin{align*}
 & \phantom{xxxxxx}5\phantom{xx}-1\phantom{xxxx}2\\
1 & )\overline{5\phantom{xx}-6\phantom{xxx}3\phantom{xxxxx}0}\\
+ & \underline{\phantom{xxxxxx}5\phantom{x}-1\phantom{xxxxx}2}\\
 & \phantom{xxx}-1\phantom{xxxxx}2\phantom{xxxx}2
\end{align*}

Therefore, we have $\frac{5x^3-6x^2+3x}{x-1}=5x^2-x+2+\frac{2}{x-1}$.
:::
::::

---

Quick reminder: $i=\sqrt{-1}$, $i^2=-1$, $i^3=-i$, and $i^4=1$.

The following are examples of how to do arithmetic involving $i$.

\begin{align*}
    (2-i)(-8+4i) & = -16 + 8i + 8i - 4(-1)\\
    & = -16+16i+4\\
    & = -12+16i
\end{align*}

$$30+(4+i) = 34 + i$$

$$(14+5i)+(-4-8i)=10-3i$$

---

::::{prf:example}
:label: synDivExam3
Let $f(x)=x^3+9x^2+28x+30%$. Use synthetic division with $k=-3+i$.
:::{dropdown} Solution:
Here is the setup

\begin{align*}
 & \phantom{xxxxxx)}1\\
-3+i & )\overline{\phantom{x}1\phantom{xxxx}9\phantom{xxxx}28\phantom{xxxx}30}\\
+ & \underline{\phantom{xxxxxxxxxxxxxxxxxxxx}}\\
 & \phantom{xxxxxxxxxxxxxxxxxxxx}
\end{align*}

Then we will compute $1(-3+i)=-3+i$ and then compute $9+(-3+i)=6+i$. This then gives:

\begin{align*}
 & \phantom{xxxxxx)}1\phantom{xxx}6+i\\
-3+i & )\overline{\phantom{x}1\phantom{xxxx}9\phantom{xxxx}28\phantom{xxxx}30}\\
+ & \underline{\phantom{xxx}-3+i\phantom{xxxxxxxxxxxx}}\\
 & \phantom{xxxxx}6+i
\end{align*}

Then we will compute ($i^2=-1$) $(6+i)(-3+i)=-19+3i$ and then compute $28-(-19+3i)$. This then gives:

\begin{align*}
 & \phantom{xxxxxx)}1\phantom{xxxxx}6+i\phantom{xxxxx}9+3i\\
-3+i & )\overline{\phantom{x}1\phantom{xxxx}9\phantom{xxxxxx}28\phantom{xxxxxxx}30}\\
+ & \underline{\phantom{xxx}-3+i\phantom{x}-19+3i\phantom{xxxxxxxx}}\\
 & \phantom{xxxxx}6+i\phantom{xxxx}9+3i
\end{align*}

Then we will compute $(9+3i)(-3+i)=30$ and then compute $30+(-30)=0$. This then gives:

\begin{align*}
 & \phantom{xxxxxx)}1\phantom{xxxxx}6+i\phantom{xxxxx}9+3i\\
-3+i & )\overline{\phantom{x}1\phantom{xxxx}9\phantom{xxxxxx}28\phantom{xxxxxxx}30}\\
+ & \underline{\phantom{xxx}-3+i\phantom{x}-19+3i\phantom{xxxxx}30}\\
 & \phantom{xxxxx}6+i\phantom{xxxx}9+3i\phantom{xxxxxx}0
\end{align*}

Therefore, we have $\frac{x^3+9x^2+28x+30}{x+3-i}=x^2+(6+i)x+(9+3i)$
:::
::::

## Remainder Theorem

We know that $f(x)=g(x)q(x)+r(x)$ is from the division algorithm. If we force $g(x)=x-k$ then we have the following identity

$$f(x)=(x-k)q(x)+r(x)$$

where $r(x)$ is going to be a constant value. In fact, this leads to an important theorem.

:::{prf:definition} Remainder Theorem
:label: remaindTheorem
If a polynomial $f(x)$ is divided by $x-k$, then the remainder is equal to $f(k)$.
:::

::::{prf:example}
:label: remaindExam1
Let $f(x)=-x^4+3x^2-4x-5$. Evaluate $f(-3)$.
:::{dropdown} Solution:
Instead of evaluating $f(-3)$ as the following:

\begin{align*}
    f(-3) & = -(-3)^4+3(-3)^2-4(-3)-5\\
    & = -81 + 27 + 12 - 5\\
    & = -47
\end{align*}

We can do the following:

\begin{align*}
 & \phantom{xxxxx}-1\phantom{xxx}3\phantom{xxx}-6\phantom{xxxxx}14\\
-3 & )\overline{\phantom{x}-1\phantom{xx}0\phantom{xxxx}3\phantom{xx}-4\phantom{xxxx}-5}\\
+ & \underline{\phantom{xxxxxxx}3\phantom{xx}-9\phantom{xxx}18\phantom{xxx}-42}\\
 & \phantom{xxxxxxx}3\phantom{xx}-6\phantom{xxx}14\phantom{xxx}-47
\end{align*}

Would also say, $f(-3)=-47$. 
:::
::::

## Root (or Zero) of a Function

:::{prf:definition} Root (or Zero) or a Function
:label: rootofFunction
A root (or zero) of a  polynomial function $f(x)$ is a number $k$ such that $f(k)=0$.
:::

Currently, finding roots of a polynomial function is difficult when considering all possible real numbers as potential roots. However, in the following section, we can narrow down the search. For now, we will consider testing $x=0$, $x=1$, or $x=-1$.

::::{prf:example}
:label: rootExam1
Let $f(x)=x^4-6x^3+8x^2+6x-9$. Find all the roots for $f(x)$.
:::{dropdown} Solution:
It should be obvious that $x=0$ is not a root. Therefore, we will move on to $x=1$. Using the remainder theorem we will see if $f(1)=0$.

\begin{align*}
 & \phantom{xxxxxxx}1\phantom{xx}-5\phantom{xxx}3\phantom{xxx}9\\
1 & )\overline{\phantom{x}1\phantom{xx}-6\phantom{xxxx}8\phantom{xxx}6\phantom{x}-9}\\
+ & \underline{\phantom{xxxxxxx}1\phantom{xx}-5\phantom{xxx}3\phantom{xxx}9}\\
 & \phantom{xxxxx}-5\phantom{xxxx}3\phantom{xxx}9\phantom{xxx}0
\end{align*}

This means, $f(1)=0$ and 

$$f(x)=(x-1)(x^3-5x^2+3x+9)$$

We then want to see if $f(-1)=0$. Using the remainder theorem we will evaluate $x^3-5x^2+3x+9$ at $x=-1$.

\begin{align*}
 & \phantom{xxxxxxx}1\phantom{xx}-6\phantom{xxxx}9\\
1 & )\overline{\phantom{x}1\phantom{xx}-5\phantom{xxxx}3\phantom{xxxx}9}\\
+ & \underline{\phantom{xxxxxxx}1\phantom{xxxx}6\phantom{xx}-9}\\
 & \phantom{xxxxx}-6\phantom{xxxx}3\phantom{xxxx}0
\end{align*}

This means, $f(-1)=0$ and

$$f(x)=(x-1)(x+1)(x^2-6x+9)$$

Looking at $x^2-6x+9$ we know that it factors to $(x-3)(x-3)$. Therefore,

$$f(x)=(x-1)(x+1)(x-3)^2$$

and all the roots of $f$ is $\{1,-1,3\}$.
:::
::::

In the next section, we will discover how to find all possible rational roots. This will help find zero of polynomials more efficiently.