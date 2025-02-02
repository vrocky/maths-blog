
# Building Calculus from First Principles

## Part V-1: Division Properties and Infinite Series

### Preface

In the previous articles of this series, we built the foundations of calculus by examining how functions behave under infinitesimal changes. We avoided geometric interpretations and instead focused on recognizing algebraic patterns in function expansions.

Now, we extend our exploration to division properties and infinite series expansions, which will naturally lead to differentiation formulas for reciprocal functions and more complex expressions. Instead of memorizing derivatives, we emphasize pattern recognition and how the rules emerge algebraically.

In this part, we will:

- Understand long division as a method for expanding functions,
- Derive the series expansion for $\frac{1}{x+h}$,
- Use infinite series representations to extend this to general division-based functions,
- Derive the derivatives of $\sec(x)$, $\csc(x)$, $\tan(x)$, and $\log(x)$,
- Showcase how patterns in algebra naturally reveal differentiation rules.

## 1. Division Properties and the Expansion of $\frac{1}{x+h}$

### 1.1 Expanding $\frac{1}{x+h}$ Using Long Division

Consider the reciprocal function:


$$
f(x + h) = \frac{1}{x+h}.
$$

Our goal is to express this in a form that reveals the coefficient of $h$ clearly, leading to its derivative. Long division is a powerful tool here.

If you need a refresher on long division, let's first illustrate it with an algebraic example:

### 1.2 Long Division Example: $\frac{x^4 - 4}{x + 2}$

Performing the division step by step:


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

The step-by-step breakdown is:


$$
x^4 - 1 = (x + 2)(x^3) - 2x^3 - 1.
$$

Expanding further:


$$
(x + 2)(x^3 - 2x^2 + 4x - 8) - 15.
$$

This technique will now be applied to $\frac{1}{x+h}$.

### 1.3 Long Division Expansion of $\frac{1}{x+h}$

Rewriting the function:


$$
\frac{1}{x+h} = \frac{1}{x} \cdot \frac{1}{1+\frac{h}{x}}.
$$

Using the geometric series expansion for $\frac{1}{1+y}$ when $|y| < 1$:


$$
\frac{1}{1+\frac{h}{x}} = \sum_{n=0}^{\infty} (-1)^n \left(\frac{h}{x}\right)^n.
$$

Multiplying by $\frac{1}{x}$, we obtain:


$$
\frac{1}{x+h} = \frac{1}{x} - \frac{h}{x^2} + \frac{h^2}{x^3} - \frac{h^3}{x^4} + \frac{h^4}{x^5} - \ldots.
$$

Each term alternates in sign, following the pattern:


$$
\frac{(-1)^n h^n}{x^{n+1}}.
$$

The coefficient of $h$ is $-\frac{1}{x^2}$, so we immediately deduce:


$$
\boxed{\frac{d}{dx} \left( x^{-1} \right) = -x^{-2}.}
$$

## 2. Infinite Series and Division-Based Differentiation

### 2.1 Binomial Series Expansion (for $|x| < 1$)


$$
\frac{1}{x+1} = \sum_{n=0}^{\infty} (-1)^n x^n.
$$

This expands explicitly as:


$$
1 - x + x^2 - x^3 + x^4 - \ldots,
$$

which converges for $|x| < 1$.

### 2.2 Laurent Series Expansion (for $|x| > 1$)


$$
\frac{1}{x+1} = \sum_{n=1}^{\infty} (-1)^{n+1} x^{-n}.
$$

Expanding explicitly:


$$
x^{-1} - x^{-2} + x^{-3} - \ldots,
$$

which converges for $|x| > 1$.

### 2.3 A Generalized Expansion

For constants $a$ and $b$, the function:


$$
\frac{1}{ax+by}
$$

has the expansion:


$$
\frac{1}{by} \sum_{n=0}^{\infty} (-1)^n \left(\frac{ax}{by}\right)^n, \quad \text{for } \left|\frac{x}{y}\right| < 1.
$$

Proof:
$$
\begin{aligned}
\frac{1}{ax+by} &= \frac{1}{by} \cdot \frac{1}{1+\frac{ax}{by}} \\[1mm]
&= \frac{1}{by} \sum_{n=0}^{\infty} (-1)^n \left(\frac{ax}{by}\right)^n.
\end{aligned}
$$

ChatGPTReasoned for a few secondsUnraveling the analysis

Breaking down the expansion of $\frac{1}{ax+by}$, including geometric series and convergence conditions, to reveal the general term and underlying patterns.

Below is an independent, detailed article devoted to the "Generalized Expansion" for functions of the form


$$
\frac{1}{ax+by},
$$

presented in an elementary, algebraic style. This article elaborates on the derivation step by step, explains the underlying patterns, and concludes with remarks on its significance. You can later incorporate this into your series as a standalone section.

# A Generalized Expansion for $\frac{1}{ax+by}$

### 1. Introduction

In many applications, it is useful to express functions in the form of an infinite series. One important example is the reciprocal function. In our approach we have already seen that elementary functions like


$$
\frac{1}{1+x}
$$

can be expressed as an infinite geometric series. Here, we extend this idea to a more generalized expression,


$$
\frac{1}{ax+by},
$$

where $a$ and $b$ are constants, and $x$ and $y$ are variables. Our goal is to derive an infinite series representation for $\frac{1}{ax+by}$ by elementary means—using long division and geometric series techniques—and to highlight the algebraic patterns that emerge.

### 2. Setting Up the Expression

We begin with the function


$$
\frac{1}{ax+by}.
$$

A common strategy to derive a series expansion is to factor out one of the terms in the denominator so that the remainder appears in a form suitable for applying the geometric series formula. For instance, if we assume that $|\frac{ax}{by}| < 1$ (or equivalently, that $\left|\frac{x}{y}\right|$ is sufficiently small relative to the constant ratio), we can factor out $by$ from the denominator:


$$
\frac{1}{ax+by} = \frac{1}{by} \cdot \frac{1}{1 + \frac{ax}{by}}.
$$

Here, the term $\frac{ax}{by}$ will serve as our “small” parameter.

### 3. Applying the Geometric Series Expansion

Recall that for any number $t$ satisfying $|t| < 1$, the geometric series expansion is given by:


$$
\frac{1}{1+t} = \sum_{n=0}^{\infty} (-1)^n t^n.
$$

Setting


$$
t = \frac{ax}{by},
$$

we have


$$
\frac{1}{1+\frac{ax}{by}} = \sum_{n=0}^{\infty} (-1)^n \left(\frac{ax}{by}\right)^n.
$$

Multiplying this series by the prefactor $\frac{1}{by}$, we obtain:


$$
\frac{1}{ax+by} = \frac{1}{by} \sum_{n=0}^{\infty} (-1)^n \left(\frac{ax}{by}\right)^n.
$$

Rearranging, the series becomes:


$$
\frac{1}{ax+by} = \sum_{n=0}^{\infty} (-1)^n \frac{a^n}{b^{n+1}} \, \frac{x^n}{y^{n+1}}.
$$

Thus, the final series expansion is:


$$
\boxed{\frac{1}{ax+by} = \frac{1}{by} - \frac{ax}{b^2y^2} + \frac{a^2x^2}{b^3y^3} - \frac{a^3x^3}{b^4y^4} + \cdots,}
$$

with the convergence condition:


$$
\left|\frac{ax}{by}\right| < 1.
$$

### 4. Discussion of the Pattern

Let us examine the structure of the series carefully:

1. Overall Factor:The series begins with the factor $\frac{1}{by}$, which is the “zeroth-order” term corresponding to the constant part of the denominator.


2. Alternating Signs:Each term is multiplied by $(-1)^n$, indicating that the signs alternate. This is a hallmark of the geometric series expansion for $\frac{1}{1+t}$.


3. Powers of $x$ and $y$:The $n$th term involves $x^n$ in the numerator and $y^{n+1}$ in the denominator. Additionally, the constants $a$ and $b$ appear in the form $a^n$ and $b^{n+1}$, respectively. This shows that as $n$ increases, higher powers of $x$ and lower powers of $y$ (relative to the constant $b$) come into play.


4. General Term:The general term is:


$$
T_n = (-1)^n \frac{a^n}{b^{n+1}} \, \frac{x^n}{y^{n+1}}.
$$

This pattern is consistent for all $n \ge 0$.


5. Convergence Condition:The series converges provided:


$$
\left|\frac{ax}{by}\right| < 1,
$$

which controls the relative sizes of $x$ and $y$ (and the constants $a$ and $b$).



### 5. Conclusion

We have derived the generalized infinite series expansion for the function


$$
\frac{1}{ax+by}
$$

using elementary methods. The final expansion is:


$$
\boxed{\frac{1}{ax+by} = \frac{1}{by} - \frac{ax}{b^2y^2} + \frac{a^2x^2}{b^3y^3} - \frac{a^3x^3}{b^4y^4} + \cdots, \quad \text{for } \left|\frac{ax}{by}\right| < 1.}
$$

This expansion not only provides a valuable tool for approximating functions but also reveals a beautiful algebraic pattern: each term in the series corresponds to a higher power of the small parameter $\frac{ax}{by}$, and the series is an instance of an infinite geometric series. Recognizing these patterns reinforces the idea that many standard results in calculus—especially those involving division and infinite series—emerge naturally from basic algebraic manipulations.

