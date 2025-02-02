Below is the final, elaborated article for Part VI: Integration from First Principles in your series. In this presentation we define integration as the summing of infinitesimal contributions, and we develop several basic examples—integrating the constant function, $x$, and $x^2$—all without invoking standard terms like “Riemann sum” or “approximation.” Instead, we rely solely on elementary algebra, limits, and known summation formulas to reveal the underlying structure.

# Building Calculus from First Principles

## Part VI: Integration from First Principles

### Preface

In our earlier parts of the series, we showed how functions could be expanded into series and how algebraic patterns in these expansions reveal the rules of differentiation. In this article we turn our attention to integration—understood as the process of summing an infinite collection of infinitesimally small contributions. Here, integration is defined from first principles using a limit process that captures the cumulative effect of these contributions. We will illustrate this by computing the integrals of simple functions such as the constant function, $x$, and $x^2$, using elementary summation techniques.

### 1. A Foundational Definition of Integration

Let $f(x)$ be a function defined on an interval, and consider dividing the interval into a large number of subintervals of equal width $\Delta x$. If we let


$$
N = \frac{n}{\Delta x},
$$

then we define the integral of $f(x)$ over a suitable interval as the limit of a sum of the form


$$
\int_{0}^{N} f(x)\, dx = \lim_{\Delta x \to 0} \sum_{i=0}^{\frac{n}{\Delta x}} f(i\, \Delta x) \cdot \Delta x.
$$

In our approach, we interpret this definition as the exact summing of infinitely many small contributions from $f(x)$. (For our purposes, we avoid the usual technical terms and focus on the algebraic structure of the sum.)

### 2. Integration Examples

2.1 Integration of the Constant FunctionConsider the constant function:


$$
f(x) = 1.
$$

Then the cumulative sum over the interval (from 0 to $x$) is


$$
\begin{aligned}
\int_{0}^{x} 1 \, dx &= \sum_{i=0}^{\frac{n}{\Delta x}} 1 \cdot \Delta x \\
&= \left(\frac{n}{\Delta x}\right) \Delta x \\
&= x.
\end{aligned}
$$

Thus, we obtain


$$
\boxed{\int 1 \, dx = x + C.}
$$

2.2 Integration of $x$Now, consider:


$$
f(x) = x.
$$

We form the sum


$$
\int_{0}^{x} x \, dx = \lim_{\Delta x \to 0} \sum_{i=0}^{\frac{n}{\Delta x}} \Bigl(i\, \Delta x\Bigr) \Delta x.
$$

Recall the well-known summation formula for the first $N$ natural numbers:


$$
\sum_{i=0}^{N} i = \frac{N(N+1)}{2}.
$$

Interpreting $N = \frac{n}{\Delta x}$, we have


$$
\sum_{i=0}^{\frac{n}{\Delta x}} i = \frac{\frac{n}{\Delta x}\left(\frac{n}{\Delta x} + 1\right)}{2}.
$$

Multiplying by $(\Delta x)^2$ (since each term is multiplied by $\Delta x$ from the summation), we obtain


$$
\begin{aligned}
\int_{0}^{x} x \, dx &= \lim_{\Delta x \to 0} \left[ \frac{\frac{n}{\Delta x}\left(\frac{n}{\Delta x} + 1\right)}{2} \cdot (\Delta x)^2 \right] \\
&= \lim_{\Delta x \to 0} \left[ \frac{n^2}{2\Delta x^2} (\Delta x)^2 + \frac{n}{2\Delta x} (\Delta x)^2 \right] \\
&= \frac{n^2}{2} + \frac{n\,\Delta x}{2}.
\end{aligned}
$$

Since $n\,\Delta x = x$ and in the limit $\Delta x \to 0$ the second term vanishes, we deduce that


$$
\boxed{\int x \, dx = \frac{1}{2} x^2 + C.}
$$

2.3 Integration of $x^2$Next, consider:


$$
f(x) = x^2.
$$

We express the sum as


$$
\int_{0}^{x} x^2 \, dx = \lim_{\Delta x \to 0} \sum_{i=0}^{\frac{n}{\Delta x}} \Bigl(i\, \Delta x\Bigr)^2 \Delta x.
$$

Recall the formula for the sum of the squares of the first $N$ natural numbers:


$$
\sum_{i=0}^{N} i^2 = \frac{N(N+1)(2N+1)}{6}.
$$

Substitute $N = \frac{n}{\Delta x}$ and multiply by $(\Delta x)^3$:


$$
\begin{aligned}
\int_{0}^{x} x^2 \, dx &= \lim_{\Delta x \to 0} \left[ \frac{\frac{n}{\Delta x}\left(\frac{n}{\Delta x}+1\right)\left(2\frac{n}{\Delta x}+1\right)}{6} \cdot (\Delta x)^3 \right] \\
&= \frac{n^3}{3},
\end{aligned}
$$

since the lower order terms vanish as $\Delta x$ becomes infinitely small, and noting that $n\,\Delta x = x$. Thus, we conclude that


$$
\boxed{\int x^2 \, dx = \frac{1}{3} x^3 + C.}
$$

Note: In these derivations, standard summation formulas for $\sum i$ and $\sum i^2$ are used to reveal the pattern. This method of "summing contributions" from infinitesimally small intervals is the cornerstone of our integration approach from first principles.

### 3. Summary of the Method

In each example, we:

- Divide the interval into many subintervals of width $\Delta x$.
- Sum the contributions $f(i\,\Delta x) \cdot \Delta x$ for $i = 0, 1, 2, \ldots$.
- Use known formulas for the sums of integers and their powers.
- Take the limit as $\Delta x \to 0$ to obtain an exact expression for the integral.

This approach illustrates that integration is the process of summing infinitely many infinitesimal contributions, and that the antiderivative of a function emerges naturally from these summation patterns.

### 4. Pedagogical Insights and Benefits

- Clear Algebraic Patterns:By writing the integration process as a limit of sums and then using standard summation formulas, the underlying algebraic structure becomes evident. Students can see how the expressions for $\int 1\,dx$, $\int x\,dx$, and $\int x^2\,dx$ arise from basic arithmetic patterns.


- Elementary Foundation:This method uses only elementary algebra and limits, providing a very accessible entry point to the concept of integration. It avoids technical terminology and focuses on visible patterns, which can be especially beneficial for beginners.


- Unified Perspective:Integration, seen in this light, is not an abstract or isolated concept; it is simply the inverse process of differentiation. The same idea of “peeling off” contributions is used in both integration and differentiation, offering a unified perspective.


- Preparation for Advanced Topics:Understanding integration from this foundational standpoint prepares students to later tackle more sophisticated techniques and to appreciate the logical structure of calculus.



### 5. Conclusion

We have defined integration from first principles as the summing of infinitely many infinitesimal contributions, and we demonstrated this by explicitly deriving the antiderivatives for the constant function, $x$, and $x^2$. In each case, we employed the idea of partitioning the interval and summing contributions over each subinterval, using standard summation formulas to reveal the final algebraic expressions.

Thus, we conclude:

- $\displaystyle \int 1\,dx = x + C$,
- $\displaystyle \int x\,dx = \frac{1}{2} x^2 + C$,
- $\displaystyle \int x^2\,dx = \frac{1}{3} x^3 + C$.

This integration approach, based on recognizing and summing algebraic patterns, provides a fresh, intuitive entry point to calculus—building from first principles and reinforcing the deep connection between differentiation and integration.

End of Part VI

This comprehensive article should serve as a detailed and engaging exposition on integration from first principles. All your original LaTeX content has been preserved and elaborated upon with clear explanations, theoretical insights, and practical examples. Feel free to adjust or integrate this article as part of your series.

