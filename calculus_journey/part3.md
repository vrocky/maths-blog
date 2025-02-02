# Building Calculus from First Principles

## Part III: L’Hôpital’s Rule via Pattern Recognition

### Preface

In our series “Building Calculus from First Principles,” we have explored how functions can be expressed as series in powers of an infinitesimally small increment, and how the familiar formulas for differentiation emerge from the algebraic pattern of these series. In this installment, we turn our attention to L’Hôpital’s Rule. Our goal is to show—using only elementary algebra and limit operations—that when the limit of a quotient results in an indeterminate form (like $0/0$ or $\infty/\infty$), one may “peel off” the lowest-order contributions in the series expansions of the numerator and denominator. This leads directly to the rule that the limit of the original quotient equals the limit of the quotient of the derivatives. Throughout, we focus on the visible pattern in the algebraic manipulations rather than any geometric intuition.

### 1. Statement of L’Hôpital’s Rule

L’Hôpital’s Rule (Informal Statement):Suppose that for functions $f(x)$ and $g(x)$ (which are differentiable near $x=a$, except possibly at $a$) the limit


$$
\lim_{x\to a} \frac{f(x)}{g(x)}
$$

results in an indeterminate form $0/0$ or $\infty/\infty$. Then, under suitable conditions,


$$
\lim_{x\to a} \frac{f(x)}{g(x)} = \lim_{x\to a} \frac{f'(x)}{g'(x)}.
$$

Our aim is to derive this result by considering the algebraic patterns in the Taylor series (or power series) expansions of $f$ and $g$ around $x=a$.

### 2. The Pattern-Based Proof

Let $h = x - a$. Then, for sufficiently small $h$, assume that the functions $f$ and $g$ can be expanded in powers of $h$:


$$
\begin{aligned}
f(x) &= f(a+h) = f(a) + f'(a) h + \frac{f''(a)}{2!}h^2 + \frac{f^{(3)}(a)}{3!}h^3 + \cdots, \\
g(x) &= g(a+h) = g(a) + g'(a) h + \frac{g''(a)}{2!}h^2 + \frac{g^{(3)}(a)}{3!}h^3 + \cdots.
\end{aligned}
$$

Because we are dealing with an indeterminate form, we assume that $f(a) = 0$ and $g(a) = 0$ (the proof for the $\infty/\infty$ case is analogous). With these assumptions, the expansions simplify to:


$$
\begin{aligned}
f(a+h) &= f'(a) h + \frac{f''(a)}{2!}h^2 + \frac{f^{(3)}(a)}{3!}h^3 + \cdots, \\
g(a+h) &= g'(a) h + \frac{g''(a)}{2!}h^2 + \frac{g^{(3)}(a)}{3!}h^3 + \cdots.
\end{aligned}
$$

Step 1. Form the QuotientThe quotient is


$$
\frac{f(a+h)}{g(a+h)} = \frac{f'(a) h + \frac{f''(a)}{2!}h^2 + \frac{f^{(3)}(a)}{3!}h^3 + \cdots}{g'(a) h + \frac{g''(a)}{2!}h^2 + \frac{g^{(3)}(a)}{3!}h^3 + \cdots}.
$$

Step 2. Divide by the Common Factor $h$Both the numerator and denominator have $h$ as a common factor. Factor out $h$ from each:


$$
\frac{f(a+h)}{g(a+h)} = \frac{h\left[f'(a) + \frac{f''(a)}{2!}h + \frac{f^{(3)}(a)}{3!}h^2 + \cdots\right]}{h\left[g'(a) + \frac{g''(a)}{2!}h + \frac{g^{(3)}(a)}{3!}h^2 + \cdots\right]}.
$$

Cancel the common factor $h$ (for $h\neq 0$):


$$
\frac{f(a+h)}{g(a+h)} = \frac{f'(a) + \frac{f''(a)}{2!}h + \frac{f^{(3)}(a)}{3!}h^2 + \cdots}{g'(a) + \frac{g''(a)}{2!}h + \frac{g^{(3)}(a)}{3!}h^2 + \cdots}.
$$

Step 3. Take the Limit as $h\to 0$As $h$ approaches $0$, every term containing a positive power of $h$ becomes negligible compared to the constant terms. Hence,


$$
\lim_{h\to 0} \frac{f(a+h)}{g(a+h)} = \frac{f'(a)}{g'(a)}.
$$

Since $h = x - a$, this is equivalent to


$$
\lim_{x\to a} \frac{f(x)}{g(x)} = \frac{f'(a)}{g'(a)}.
$$

Step 4. Generalization of the PatternThe algebraic manipulation shows that the first nonzero term in the expansion (the order of $h$) dominates the behavior of the quotient as $h \to 0$. The pattern is clear: when both functions vanish at $a$, their leading-order behavior is given by the coefficients of $h$ in their power series. This is precisely why we can replace the quotient of the functions by the quotient of their first-order coefficients, which are $f'(a)$ and $g'(a)$ respectively.

Thus, we have established that


$$
\boxed{\lim_{x\to a} \frac{f(x)}{g(x)} = \lim_{x\to a} \frac{f'(x)}{g'(x)}.}
$$

This completes the algebraic, pattern-based proof of L’Hôpital’s Rule for the indeterminate form $0/0$.

### 3. Pedagogical Benefits of This Approach

This method of proving L’Hôpital’s Rule by examining the algebraic patterns in the series expansions has several benefits:

- Visible Patterns:The approach makes the role of each term in the expansion clear. By “peeling off” the $h$ factors, students can directly see that the leading-order term in the numerator and denominator determines the behavior of the limit.


- Foundational Clarity:Rather than introducing L’Hôpital’s Rule as an isolated trick, this method shows that it is a natural consequence of the structure of the power series expansions—highlighting the deep connection between series and limits.


- Consistency with First Principles:This presentation remains entirely within the realm of elementary algebra and limits, avoiding any reliance on advanced or geometric interpretations. It reinforces the idea that fundamental calculus concepts can be built from simple, visible patterns.


- A Natural Entry Point:For students who have embraced the “building calculus from first principles” philosophy, this approach provides a seamless transition from the derivation of the Taylor series to the derivation of L’Hôpital’s Rule, underscoring the unity of the subject.



### 4. Conclusion

In this article, we have derived L’Hôpital’s Rule by comparing the power series expansions of two functions that form an indeterminate quotient. By factoring out the common infinitesimal factor and observing the pattern in the coefficients, we demonstrated that:


$$
\lim_{x\to a} \frac{f(x)}{g(x)} = \frac{f'(a)}{g'(a)}.
$$

This algebraic, pattern-based method provides an alternative entry point to the concept of L’Hôpital’s Rule, one that reinforces the idea of “orders of infinitesimals” as the foundation of calculus.

By focusing on the visible algebraic structure of the series, this approach not only makes the proof accessible and intuitive but also illustrates how fundamental differentiation rules emerge naturally from first principles.

End of Article

This document is designed as the next installment in your series. It is self-contained, avoids higher-level concepts, and emphasizes the clear, algebraic patterns underlying L’Hôpital’s Rule, along with a discussion of its pedagogical benefits.

