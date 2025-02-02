# Building Calculus from First Principles

## Part IV: Division Properties and Infinite Series

### Preface

In our previous articles, we developed an elementary, algebraic approach to express functions as sums of contributions from different orders of an infinitely small increment. We saw that by “peeling off” the constant term, then the coefficient of $\Delta x$, then that of $(\Delta x)^2$, etc., we arrive naturally at the familiar Taylor series expansion.

In this installment, we extend that approach to functions involving division. We will:

- Develop a series expansion for reciprocal functions such as $\frac{1}{x+h}$ using the method of long division.
- Derive important differentiation formulas (for example, for $x^{-1}$) from these series.
- Present infinite series formulas for functions like $\frac{1}{1+x}$ in both the standard geometric and Laurent forms.
- Show how algebraic manipulation in series leads naturally to product and chain rules when division is involved.

Our aim is to give the reader a clear, pattern-based entry into these topics—revealing the algebraic structure underlying many fundamental formulas in calculus.

## 1. Division Properties and Infinite Series

Let us begin by considering the derivative of a reciprocal function:


$$
\frac{d}{dx}\frac{1}{x} \quad \text{or} \quad \frac{d}{dx}\,x^{-1}.
$$

To understand this from first principles, we wish to expand


$$
f(x+h) = \frac{1}{x+h}
$$

into a power series in $h$ (or $\Delta x$) so that we can identify the coefficient of $h$.

### 1.1 Using Long Division

To bring the expression into a form where the coefficient of $h$ is visible, we employ the Long Division method. If you have forgotten the process of long division, here is a brief revision:

Long Division RevisionTo perform the long division for, say,


$$
\frac{x^4 - 4}{x + 2},
$$

follow these steps:

1. Divide the first term of the numerator ($x^4$) by the first term of the denominator ($x$); this gives $x^3$.
2. Multiply the entire denominator ($x + 2$) by $x^3$ and subtract the result from the numerator.
3. Bring down the next term and repeat until all terms are used.

An example of a long division layout in LaTeX is:


$$
\begin{array}{c|cccc}
& x^3 & -2x^2 & +4x & -8 \\
\hline
x + 2 & x^4 & 0 & 0 & -1 \\
& x^4 & +2x^3 & & \\
\hline
& & -2x^3 & & -1 \\
& & -2x^3 & -4x^2 & \\
\hline
& & & 4x^2 & -1 \\
& & & 4x^2 & +8x \\
\hline
& & & & -8x - 1 \\
& & & & -8x - 16 \\
\hline
& & & & 15 \\
\end{array}
$$

A step-by-step breakdown for dividing $x^4 - 1$ by $x + 2$ is given by:


$$
\begin{aligned}
x^4 - 1 & = (x + 2)(x^3) - 2x^3 - 1 \\
& = (x + 2)(x^3) - (x + 2)(2x^2) + 4x^2 - 1 \\
& = (x + 2)(x^3) - (x + 2)(2x^2) + (x + 2)(4x) - 8x - 1 \\
& = (x + 2)(x^3) - (x + 2)(2x^2) + (x + 2)(4x) - (x + 2)(8) - 15 \\
& = (x + 2)(x^3 - 2x^2 + 4x - 8) - 15.
\end{aligned}
$$

This serves as a review for performing long division on polynomials.

## 2. Series Expansion for $\frac{1}{x+h}$ via Long Division

We now apply the long division technique to derive the series expansion for the function


$$
\frac{1}{x+h}.
$$

Begin with the expression:


$$
\frac{1}{x+h}.
$$

The idea is to rewrite and expand the expression into a series of the form:


$$
\frac{1}{x+h} = \frac{1}{x} - \frac{h}{x^2} + \frac{h^2}{x^3} - \frac{h^3}{x^4} + \ldots.
$$

The derivation follows these steps:

1. Rewriting the Expression:

Write $\frac{1}{x+h}$ as an expression in powers of $h$. One way to proceed is to factor out $x$:


$$
\frac{1}{x+h} = \frac{1}{x\left(1 + \frac{h}{x}\right)} = \frac{1}{x} \cdot \frac{1}{1 + \frac{h}{x}}.
$$


2. Expanding as a Geometric Series:

For $\left|\frac{h}{x}\right| < 1$, the expression


$$
\frac{1}{1 + \frac{h}{x}}
$$

can be expanded as a geometric series:


$$
\frac{1}{1 + \frac{h}{x}} = \sum_{n=0}^{\infty} \left(-\frac{h}{x}\right)^n.
$$


3. Writing the Final Series:

Multiplying by $\frac{1}{x}$ gives:


$$
\frac{1}{x+h} = \frac{1}{x} \sum_{n=0}^{\infty} \left(-\frac{h}{x}\right)^n = \frac{1}{x} - \frac{h}{x^2} + \frac{h^2}{x^3} - \frac{h^3}{x^4} + \cdots.
$$



Notice that the general term in the series is:


$$
\frac{(-1)^n h^n}{x^{n+1}}.
$$

Thus, we have derived the series expansion for $\frac{1}{x+h}$.

### 2.1 Deriving the Derivative of $x^{-1}$

The series expansion for $\frac{1}{x+h}$ is:


$$
\frac{1}{x+h} = \frac{1}{x} - \frac{h}{x^2} + \frac{h^2}{x^3} - \frac{h^3}{x^4} + \cdots.
$$

The coefficient of the first-order term $h$ in this expansion is $-\frac{1}{x^2}$. Hence, by our first-principles method, we conclude that:


$$
\frac{d}{dx}\left(x^{-1}\right) = -\frac{1}{x^2}.
$$

## 3. Some Infinite Series Formulas

Below are some classic infinite series expressions that follow naturally from the geometric series:

1. Binomial Series (for $|x| < 1$):


$$
\frac{1}{1+x} = \sum_{n=0}^{\infty} (-1)^n x^n = 1 - x + x^2 - x^3 + x^4 - \ldots.
$$


2. Laurent Series (for $|x| > 1$):


$$
\frac{1}{1+x} = \frac{1}{x} \sum_{n=0}^{\infty} (-1)^n x^{-n} = \frac{1}{x} - \frac{1}{x^2} + \frac{1}{x^3} - \ldots.
$$


3. Generalized Form:

For example, for constants $a$ and $b$, one may write:


$$
\frac{1}{ax+by} = \frac{1}{by} \sum_{n=0}^{\infty} (-1)^n \left(\frac{ax}{by}\right)^n,
$$

valid when $\left|\frac{ax}{by}\right| < 1$.



These series are examples of infinite geometric series, where the sum can be expressed as:


$$
\text{Sum} = \frac{a}{1 - r},
$$

with $a$ the first term and $r$ the common ratio.

## 4. Properties Involving Division

### 4.1 Derivative of $\sec(x)$

Statement:


$$
\frac{d}{dx}[\sec(x)] = \sec(x) \tan(x).
$$

Proof Sketch:

1. Start with:

$$
\sec(x+h) = \frac{1}{\cos(x+h)}.
$$


2. Express $\cos(x+h)$ in its series form:

$$
\cos(x+h) = \cos(x)\cos(h) - \sin(x)\sin(h).
$$


3. For small $h$, approximate:

$$
\cos(h) \approx 1 \quad \text{and} \quad \sin(h) \approx h.
$$


Hence:

$$
\cos(x+h) \approx \cos(x) - \sin(x) h.
$$


4. Then:

$$
\sec(x+h) \approx \frac{1}{\cos(x) - \sin(x) h}.
$$


5. Expanding this series (using a similar technique as for $\frac{1}{x+h}$), one obtains an expansion where the coefficient of $h$ is $-\frac{\sin(x)}{\cos^2(x)}$. Combining this with the constant term $1/\cos(x)$ leads to the derivative formula:

$$
\frac{d}{dx}[\sec(x)] = \sec(x)\tan(x).
$$



### 4.2 Chain Rule Example Using $\sec(x)$ and Other Functions

Consider the composite function


$$
f(g(x+h)) = f(B_0 + B_1h + B_2h^2 + \ldots),
$$

where $B_0 = g(x)$ and $B_1 = g'(x)$. By expanding $f$ in a series around $g(x)$, one obtains:


$$
f(g(x+h)) = C_0 + C_1 (B_1h + B_2h^2 + \ldots) + C_2 (B_1h + B_2h^2 + \ldots)^2 + \cdots.
$$

Collecting the coefficient of $h$ yields:


$$
\text{Coefficient of } h = C_1B_1,
$$

or in familiar terms,


$$
\frac{d}{dx}[f(g(x))] = f'(g(x))\,g'(x).
$$

### 4.3 Derivative of $\csc(x)$

Statement:


$$
\frac{d}{dx}[\csc(x)] = -\csc(x)\cot(x).
$$

Proof Sketch:

1. Start with:

$$
\csc(x+h) = \frac{1}{\sin(x+h)}.
$$


2. Use the series expansion for $\sin(x+h)$:

$$
\sin(x+h) = \sin(x) + \cos(x) h,
$$


(ignoring higher order terms).
3. Then:

$$
\csc(x+h) \approx \frac{1}{\sin(x) + \cos(x)h}.
$$


4. Expanding in a series shows that the coefficient of $h$ is $-\frac{\cos(x)}{\sin^2(x)}$. This algebraic pattern corresponds to:

$$
\frac{d}{dx}[\csc(x)] = -\csc(x)\cot(x).
$$



### 4.4 Derivative of $\tan(x)$

Statement:


$$
\frac{d}{dx}[\tan(x)] = \sec^2(x).
$$

Proof Sketch:

1. Express:

$$
\tan(x+h) = \frac{\sin(x+h)}{\cos(x+h)}.
$$


2. Expand both $\sin(x+h)$ and $\cos(x+h)$ in series:

$$
\sin(x+h) \approx \sin(x) + \cos(x)h, \quad \cos(x+h) \approx \cos(x) - \sin(x)h.
$$


3. Write:

$$
\tan(x+h) \approx \frac{\sin(x) + \cos(x)h}{\cos(x) - \sin(x)h}.
$$


4. By finding the coefficient of $h$ in this quotient (using an expansion of the reciprocal of the denominator), one finds that it equals $\sec^2(x)$.

### 4.5 Derivative of $\log(x)$

Statement:


$$
\frac{d}{dx}[\log(x)] = \frac{1}{x}.
$$

Proof Sketch:

1. Express:

$$
\log(x+h) = \log\left(x\left(1+\frac{h}{x}\right)\right) = \log(x) + \log\left(1+\frac{h}{x}\right).
$$


2. Use the series expansion for $\log(1+\frac{h}{x})$ (which is $\frac{h}{x}$ to first order):

$$
\log\left(1+\frac{h}{x}\right) \approx \frac{h}{x}.
$$


3. Therefore,

$$
\log(x+h) \approx \log(x) + \frac{h}{x}.
$$


4. The coefficient of $h$ in this expansion is $\frac{1}{x}$, giving

$$
\frac{d}{dx}[\log(x)] = \frac{1}{x}.
$$



## 5. Pedagogical Benefits of the Pattern-Based Approach

This series of articles, including the present work on division and infinite series, offers several benefits for building calculus from first principles:

- Visible and Clear Patterns:By focusing on the algebraic structure—identifying the contributions of each order of an infinitesimally small quantity—students can clearly see how fundamental rules emerge naturally.


- Elementary and Self-Contained:The approach relies solely on elementary algebra and the concept of limits. There is no reliance on geometric interpretations (such as slopes or rates of change), making it accessible to learners from a purely algebraic viewpoint.


- Natural Emergence of Differentiation Rules:The multiplication rule and chain rule are shown to be direct consequences of how series multiply and compose. This method demystifies these rules by reducing them to simple, pattern-based operations.


- A Fresh Entry Point to Calculus:Instead of introducing the Taylor series as an advanced tool after integration or differential equations, this approach presents it as the natural decomposition of a function’s behavior from the very start.


- Foundation for Advanced Topics:Once students understand these basic patterns, they are well-prepared to tackle more advanced subjects in calculus and analysis, with a solid conceptual foundation.



## 6. Conclusion

In this article, we have extended our first-principles approach to include division properties and infinite series. By using the method of long division and series expansion, we derived the expansion for $\frac{1}{x+h}$ and demonstrated how the coefficients in this series yield the derivative of $x^{-1}$ (namely, $-x^{-2}$). We further explored how infinite series formulas, such as those for $\frac{1}{1+x}$, naturally arise from these ideas. Finally, we showed that the algebraic patterns in these series lead directly to standard differentiation formulas for functions like $\sec(x)$, $\tan(x)$, and $\log(x)$.

This pattern-based, algebraic approach provides a clear and elementary entry point to calculus, emphasizing that the fundamental rules of differentiation are built into the very structure of the series expansions. By exposing these patterns, we offer both a new perspective for learners and a rigorous foundation from which more advanced topics can later be developed.

End of Article

This article incorporates all of your rough work while preserving your LaTeX expressions and ideas. It adds clear headings, commentary, and pedagogical insights to help readers see the algebraic patterns and appreciate the benefits of this approach to building calculus from first principles.
