# Building Calculus from First Principles


## Article VIII: Difference Equations for the Anti-Derivative

### Preface

In our series Building Calculus from First Principles, we have focused on expressing functions as sums of infinitesimal contributions and revealing their underlying algebraic patterns. In this article, we turn our attention to the difference equations that connect a function with its antiderivative. Instead of relying solely on retrospectively analyzing known formulas, we compile a set of difference equations which, by “peeling off” the increments, reveal the pattern behind the antiderivative. Our method is entirely elementary and algebraic, emphasizing clear, step-by-step reasoning.

## 1. Difference Equations for Powers

The core idea is to relate the differential expression $x^p\,dx$ to the difference between consecutive powers of $x$. For very small $dx$ (or in the limit as $dx$ becomes infinitesimal), we have the following difference equations:


$$
\begin{aligned}
x\, dx &= \frac{(x + dx)^2 - x^2}{2},\\[1mm]
x^2\, dx &= \frac{(x + dx)^3 - x^3}{3},\\[1mm]
x^3\, dx &= \frac{(x + dx)^4 - x^4}{4},\\[1mm]
x^4\, dx &= \frac{(x + dx)^5 - x^5}{5}.
\end{aligned}
$$

### Explanation

- For the first equation:Expand $(x + dx)^2$:


$$
(x + dx)^2 = x^2 + 2x\,dx + (dx)^2.
$$

Neglecting the $(dx)^2$ term (since $dx$ is infinitesimally small), we obtain:


$$
(x + dx)^2 - x^2 \approx 2x\,dx.
$$

Dividing by 2 yields:


$$
x\,dx \approx \frac{(x + dx)^2 - x^2}{2}.
$$


- For the second equation:Similarly, expand $(x+dx)^3$:


$$
(x+dx)^3 = x^3 + 3x^2\,dx + 3x\,(dx)^2 + (dx)^3.
$$

Ignoring the higher-order terms, we have:


$$
(x+dx)^3 - x^3 \approx 3x^2\,dx,
$$

so that


$$
x^2\,dx \approx \frac{(x+dx)^3 - x^3}{3}.
$$


- The subsequent equations follow the same idea.



## 2. Adjusting the Difference Equations for a Finite Increment $\Delta X$

If instead of an infinitesimal $dx$ we have a finite increment $\Delta X$, the exact equations include higher-order terms. For example, using the binomial expansion we obtain:


$$
\begin{aligned}
x\,\Delta X + \frac{(\Delta X)^2}{2} &= \frac{(x + \Delta X)^2 - x^2}{2}, \\[1mm]
x^2\,\Delta X + x\,(\Delta X)^2 + \frac{(\Delta X)^3}{3} &= \frac{(x + \Delta X)^3 - x^3}{3}, \\[1mm]
x^3\,\Delta X + \frac{3x^2\,(\Delta X)^2}{2} + x\,(\Delta X)^3 + \frac{(\Delta X)^4}{2} &= \frac{(x + \Delta X)^4 - x^4}{4}.
\end{aligned}
$$

### Explanation

- In the first equation, the full expansion is:

$$
(x + \Delta X)^2 = x^2 + 2x\,\Delta X + (\Delta X)^2.
$$


Hence,

$$
\frac{(x + \Delta X)^2 - x^2}{2} = \frac{2x\,\Delta X + (\Delta X)^2}{2} = x\,\Delta X + \frac{(\Delta X)^2}{2}.
$$


- The higher equations are obtained by applying the binomial theorem to $(x + \Delta X)^k$ and then subtracting $x^k$.

These equations illustrate how, when the increment is not infinitesimally small, additional terms appear to account for the full change.

## 3. Application: Deriving the Antiderivative of $\cos(x)$

Let us now see how these difference equations connect with integration.

### 3.1 Integration of $\cos(x)$

We aim to show:


$$
\int \cos(x) \, dx = \sin(x) + C.
$$

Step 1. Express the Increment in $\sin(x)$From the sine addition formula,


$$
\sin(x + \Delta x) = \sin(x)\cos(\Delta x) + \cos(x)\sin(\Delta x).
$$

For very small $\Delta x$, we use the approximations:


$$
\cos(\Delta x) \approx 1 \quad \text{and} \quad \sin(\Delta x) \approx \Delta x.
$$

Thus,


$$
\sin(x + \Delta x) \approx \sin(x) + \cos(x) \Delta x.
$$

Subtract $\sin(x)$ from both sides:


$$
\sin(x + \Delta x) - \sin(x) \approx \cos(x)\Delta x.
$$

Step 2. Forming the Telescoping SumDivide the interval $[0, \pi]$ into subintervals of width $\Delta x$. Then


$$
\int_{0}^{\pi} \cos(x)\, dx \approx \sum_{i=0}^{\frac{n}{\Delta x}} \cos(i\Delta x) \, \Delta x.
$$

But as we just observed, for each subinterval the change in $\sin(x)$ is approximately:


$$
\sin((i+1)\Delta x) - \sin(i\Delta x) \approx \cos(i\Delta x)\Delta x.
$$

Thus, the sum becomes:


$$
\sum_{i=0}^{\frac{n}{\Delta x}} \left[\sin((i+1)\Delta x) - \sin(i\Delta x)\right].
$$

This is a telescoping series; almost every term cancels:


$$
\sin(\Delta x) - \sin(0) + \sin(2\Delta x) - \sin(\Delta x) + \cdots + \sin(N) - \sin(N-\Delta x) = \sin(N) - \sin(0).
$$

Taking the limit as $\Delta x \to 0$, we deduce:


$$
\int_{0}^{\pi} \cos(x)\, dx = \sin(\pi) - \sin(0) = 0 - 0 = 0.
$$

(For the general antiderivative, one obtains $\int \cos(x)\, dx = \sin(x) + C$.)

## 4. Application: Deriving the Antiderivative of $\sin(x)$

Similarly, consider:


$$
\int \sin(x)\, dx.
$$

Step 1. Express the Increment in $\cos(x)$Recall the cosine addition formula:


$$
\cos(x + \Delta x) = \cos(x)\cos(\Delta x) - \sin(x)\sin(\Delta x).
$$

For small $\Delta x$, this approximates to:


$$
\cos(x + \Delta x) \approx \cos(x) - \sin(x)\Delta x.
$$

Rearrange to obtain:


$$
\cos(x) - \cos(x + \Delta x) \approx \sin(x)\Delta x.
$$

Thus,


$$
\sin(x)\Delta x \approx \cos(x) - \cos(x+\Delta x).
$$

Step 2. Telescoping SumDivide the interval and sum:


$$
\sum_{i=0}^{n/\Delta x} \left[\cos(i\Delta x) - \cos((i+1)\Delta x)\right]
$$

telescopes to:


$$
\cos(0) - \cos(n\Delta x).
$$

Taking the limit as $\Delta x \to 0$ (and adjusting for the proper interval), we deduce:


$$
\int \sin(x)\, dx = -\cos(x) + C.
$$

## 5. Application: Deriving the Antiderivative of $\frac{1}{x}$

Using the logarithm, note the following expansion from previous work:


$$
\begin{aligned}
\log(x+h) &= \log(x) + \log\!\Bigl( \Bigl(1+\frac{h}{x}\Bigr)^{\frac{x}{h}} \Bigr)^{\frac{h}{x}} \\
&= \log(x) + \log\!\Bigl(e^{\frac{h}{x}}\Bigr) \\
&= \log(x) + \frac{h}{x}.
\end{aligned}
$$

Thus,


$$
\frac{h}{x} = \log(x+h) - \log(x).
$$

When you sum these differences over an interval, the telescoping nature gives:


$$
\int \frac{1}{x}\,dx = \ln|x| + C.
$$

## 6. Integration by Parts (A Brief Mention)

An additional powerful tool is integration by parts, which can also be derived using difference equations. For example, if we write the expansion for functions $f(x)$ and $G(x)$ (with $G'(x) = g(x)$) as:


$$
\begin{aligned}
f(x+\Delta x) &= A_0 + A_1\,\Delta x + A_2\,(\Delta x)^2 + \cdots, \\
G(x+\Delta x) &= B_0 + B_1\,\Delta x + B_2\,(\Delta x)^2 + \cdots,
\end{aligned}
$$

then the product $f(x)G(x)$ has a difference that telescopes. The careful grouping of terms ultimately leads to the familiar integration by parts formula:


$$
\boxed{\int u\,dv = uv - \int v\,du.}
$$

## 7. Conclusion

We have examined how difference equations can be used to “reverse-engineer” antiderivatives by considering the differences between successive values of a function. By writing:


$$
\begin{aligned}
x\,dx &= \frac{(x+dx)^2 - x^2}{2},\\[1mm]
x^2\,dx &= \frac{(x+dx)^3 - x^3}{3},\\[1mm]
x^3\,dx &= \frac{(x+dx)^4 - x^4}{4},\\[1mm]
x^4\,dx &= \frac{(x+dx)^5 - x^5}{5},
\end{aligned}
$$

we see a clear pattern: the differential (or the infinitesimal change) times a power of $x$ equals the difference of two successive higher powers of $x$, divided by a constant.

By summing these differences over a partition, we obtain telescoping sums that yield the net change in the antiderivative. This process provides a natural and intuitive derivation of the Fundamental Theorem of Calculus, as well as alternative derivations for integration formulas (for $\cos(x)$, $\sin(x)$, $\frac{1}{x}$, and even integration by parts).

This approach emphasizes the importance of algebraic patterns and finite differences, reinforcing the idea that integration is simply the accumulation of infinitesimal changes. By understanding and working through these difference equations step by step, one gains a deeper insight into the structure of antiderivatives and the fundamental connections between discrete sums and continuous change.

End of Article

This article is structured with clear headings, detailed intermediate steps, and additional equations to help the reader see the algebraic patterns in difference equations for the anti-derivative. All your original LaTeX work is preserved and integrated into the explanation. Feel free to modify or expand further as needed!
