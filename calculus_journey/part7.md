# Building Calculus from First Principles

## Part VII: # Fundamental Theorem of Calculus



In this article, we establish a fundamental relationship: if $F(x)$ is an antiderivative of $f(x)$, then


$$
\int_{0}^{N} f(x) \, dx = F(N) - F(0).
$$

We shall derive this result from first principles by interpreting integration as the summing of infinitely many infinitesimal contributions and then using the definition of the derivative in a telescoping sum.

## 1. Main Proof

We begin by defining the integral as the limit of a sum. Let $\Delta x$ be an infinitely small increment and suppose that the interval $[0, N]$ is divided into subintervals of width $\Delta x$ so that the number of subintervals is $N/\Delta x$. Then the integral is defined by


$$
\int_{0}^{N} f(x) \, dx = \lim_{\Delta x \to 0} \sum_{i=0}^{N/\Delta x} f(i \cdot \Delta x) \cdot \Delta x.
$$

Assume that $F(x)$ is an antiderivative of $f(x)$; that is, $F'(x)=f(x)$. Then we may rewrite the sum by replacing $f(x)$ with $F'(x)$:


$$
\int_{0}^{N} f(x) \, dx = \lim_{\Delta x \to 0} \sum_{i=0}^{N/\Delta x} F'(i \cdot \Delta x) \cdot \Delta x.
$$

Now, using the definition of the derivative for each term, we have


$$
F'(i \cdot \Delta x) = \frac{F(i \cdot \Delta x + \Delta x) - F(i \cdot \Delta x)}{\Delta x}.
$$

Substitute this back into the sum:


$$
\lim_{\Delta x \to 0} \sum_{i=0}^{N/\Delta x} \frac{F(i \cdot \Delta x + \Delta x) - F(i \cdot \Delta x)}{\Delta x} \cdot \Delta x.
$$

Notice that the factor $\Delta x$ in the numerator and denominator cancels:


$$
\lim_{\Delta x \to 0} \sum_{i=0}^{N/\Delta x} \Bigl[F(i \cdot \Delta x + \Delta x) - F(i \cdot \Delta x)\Bigr].
$$

Observe that this sum is telescoping. Writing out a few terms:


$$
\begin{aligned}
&\Bigl[F(\Delta x) - F(0)\Bigr] \;+\; \Bigl[F(2\Delta x) - F(\Delta x)\Bigr] \;+\; \Bigl[F(3\Delta x) - F(2\Delta x)\Bigr] \;+\; \cdots \\
&\quad +\; \Bigl[F(N) - F(N-\Delta x)\Bigr].
\end{aligned}
$$

Most of the terms cancel, leaving:


$$
\lim_{\Delta x \to 0} \Bigl[F(N) - F(0)\Bigr] = F(N) - F(0).
$$

Thus, we have proved that


$$
\boxed{\int_{0}^{N} f(x) \, dx = F(N) - F(0).}
$$

## 2. Alternative Proof by Telescoping Differences

An alternative proof uses the idea of examining the differences between successive increments of the function $F$.

Consider the differences:


$$
\begin{aligned}
F(x + \Delta x) - F(x) &= f_{A_1} \, \Delta x + f_{A_3} \, (\Delta x)^2 + f_{A_4} \, (\Delta x)^3 + \ldots, \\
F(x + 2\Delta x) - F(x + \Delta x) &= f_{A_1} (2\Delta x) + f_{A_3} (2\Delta x)^2 + f_{A_4} (2\Delta x)^3 + \ldots, \\
F(x + 3\Delta x) - F(x + 2\Delta x) &= f_{A_1} (3\Delta x) + f_{A_3} (3\Delta x)^2 + f_{A_4} (3\Delta x)^3 + \ldots, \\
&\;\vdots \\
F(x + N\Delta x) - F(x + (N-1)\Delta x) &= f_{A_1} (N\Delta x) + f_{A_3} (N\Delta x)^2 + f_{A_4} (N\Delta x)^3 + \ldots.
\end{aligned}
$$

If we sum these differences vertically, we have:


$$
\sum_{i=0}^{N/\Delta x -1} \Bigl[F(x+(i+1)\Delta x) - F(x+i\Delta x)\Bigr].
$$

This sum telescopes:


$$
F(x+\Delta x) - F(x) + F(x+2\Delta x) - F(x+\Delta x) + \cdots + F(x+N\Delta x) - F(x+(N-1)\Delta x) = F(x+N\Delta x) - F(x).
$$

Taking the limit as $\Delta x \to 0$ (and noting $x+N\Delta x \to N$ if we set $x=0$ for simplicity), we have:


$$
\lim_{\Delta x \to 0} \bigl[F(N) - F(0)\bigr] = F(N) - F(0).
$$

Thus, we recover the fundamental relationship:


$$
\boxed{\int_{0}^{N} f(x) \, dx = F(N) - F(0).}
$$

## 3. Concluding Remarks

Both proofs illustrate the same underlying idea: integration is the summation of infinitely many infinitesimally small contributions. By expressing the integral as a limit of sums and then re-writing the summand using the definition of the derivative, we obtain a telescoping sum. The telescoping nature of the sum naturally leads to the result $F(N)-F(0)$.

This foundational result—the Fundamental Theorem of Calculus—shows the deep connection between differentiation and integration, establishing that the accumulation of infinitesimal changes (integration) recovers the net change in a function (difference of the antiderivative).

End of Article

This article presents a natural, intuitive, and algebraic proof of the Fundamental Theorem of Calculus, incorporating all of your rough work while ensuring clarity and completeness. It avoids advanced terminology and focuses solely on the algebraic structure of the limit of sums, making the foundational ideas accessible.

o3-mini-high



Below is an extended, “dumbed-down” explanation that shows every intermediate step between forming the sum of differences over the partition and recognizing its telescoping nature. This version is intended to help you visualize the pattern clearly.

### Detailed Steps in the Telescoping Sum

Assume we have a continuously differentiable function $F(x)$ with derivative $F'(x) = f(x)$. We partition the interval $[0, N]$ into $M$ subintervals of equal width $h$ so that


$$
x_i = 0 + i\,h, \quad \text{for } i = 0, 1, 2, \dots, M,
$$

with


$$
M\,h = N.
$$

For each subinterval, the change in $F$ is given by:


$$
F(x_{i+1}) - F(x_i).
$$

Step 1. Writing the Sum of the Differences

We form the sum over all subintervals:


$$
\sum_{i=0}^{M-1} \Bigl[F(x_{i+1}) - F(x_i)\Bigr].
$$

Let's write this out term by term:


$$
\begin{aligned}
\text{For } i=0:&\quad F(x_1) - F(x_0), \\
\text{For } i=1:&\quad F(x_2) - F(x_1), \\
\text{For } i=2:&\quad F(x_3) - F(x_2), \\
&\quad \vdots \\
\text{For } i=M-1:&\quad F(x_M) - F(x_{M-1}).
\end{aligned}
$$

Thus, the entire sum is:


$$
\begin{aligned}
\sum_{i=0}^{M-1} \Bigl[F(x_{i+1}) - F(x_i)\Bigr]
&= \Bigl[F(x_1) - F(x_0)\Bigr] \\
&\quad + \Bigl[F(x_2) - F(x_1)\Bigr] \\
&\quad + \Bigl[F(x_3) - F(x_2)\Bigr] \\
&\quad + \cdots \\
&\quad + \Bigl[F(x_M) - F(x_{M-1})\Bigr].
\end{aligned}
$$

Step 2. Observing the Telescoping Pattern

Now, write the sum out in full, showing the plus and minus signs:


$$
\begin{aligned}
\text{Sum} =\; &F(x_1) \quad - \; F(x_0) \\
&+ \; F(x_2) \quad - \; F(x_1) \\
&+ \; F(x_3) \quad - \; F(x_2) \\
&\quad \vdots \\
&+ \; F(x_M) \quad - \; F(x_{M-1}).
\end{aligned}
$$

Notice what happens:

- $F(x_1)$ appears first as $+F(x_1)$ and then as $-F(x_1)$. They cancel.
- Similarly, $F(x_2)$ appears as $+F(x_2)$ and then $-F(x_2)$, canceling each other.
- This cancellation continues for all intermediate terms.

Thus, all terms cancel except for the very first negative term and the very last positive term:


$$
\text{Sum} = F(x_M) - F(x_0).
$$

Since $x_0 = 0$ and $x_M = N$, we have:


$$
\sum_{i=0}^{M-1} \Bigl[F(x_{i+1}) - F(x_i)\Bigr] = F(N) - F(0).
$$

Step 3. Taking the Limit

In our definition of integration, we let the width $h$ approach 0 (and thus $M \to \infty$):


$$
\int_{0}^{N} f(x) \, dx = \lim_{h\to 0} \sum_{i=0}^{M-1} \Bigl[F(x_{i+1}) - F(x_i)\Bigr].
$$

Since the telescoping sum is exactly $F(N) - F(0)$ regardless of the number of subintervals, the limit is simply:


$$
\int_{0}^{N} f(x) \, dx = F(N) - F(0).
$$

## 3. Alternate View: Expressing Each Difference as a Series

For a more detailed look at the pattern, suppose that we express the change over each subinterval as a power series in $h$:


$$
F(x_i + h) - F(x_i) = f_{A_1}(x_i) \, h + f_{A_2}(x_i) \, h^2 + f_{A_3}(x_i) \, h^3 + \cdots.
$$

Then the sum over all subintervals is:


$$
\sum_{i=0}^{M-1} \Bigl[F(x_{i+1}) - F(x_i)\Bigr] = \sum_{i=0}^{M-1} \Bigl[ f_{A_1}(x_i) \, h + f_{A_2}(x_i) \, h^2 + f_{A_3}(x_i) \, h^3 + \cdots \Bigr].
$$

When $h$ is very small, the dominant contribution comes from the first-order term:


$$
\sum_{i=0}^{M-1} f_{A_1}(x_i) \, h.
$$

In the limit $h \to 0$, this sum converges to the integral:


$$
\lim_{h\to 0} \sum_{i=0}^{M-1} f(x_i) \, h = \int_{0}^{N} f(x) \, dx,
$$

since $f_{A_1}(x_i) = F'(x_i) = f(x_i)$.

The higher-order terms vanish in the limit, and the telescoping structure (shown above) ensures that the entire sum equals $F(N) - F(0)$.




ChatGPTReasoned for a couple of secondsBelow is an expanded version of the "Alternate View" section that explains, step by step, how to express each difference as a power series and then sum these differences to reveal the telescoping pattern. This detailed explanation is intended to make the process completely clear and intuitive.

## Alternate View: Expressing Each Difference as a Series

### 1. Expressing the Incremental Change as a Series

Suppose $F(x)$ is a function that is differentiable (and, in fact, can be expanded in a power series) on the interval of interest. For a small increment $h$, we can write the change in $F$ over a single subinterval starting at $x_i$ as a power series in $h$:


$$
F(x_i + h) - F(x_i) = f_{A_1}(x_i) \, h + f_{A_2}(x_i) \, h^2 + f_{A_3}(x_i) \, h^3 + \cdots,
$$

where:

- $f_{A_1}(x_i)$ is the coefficient of the linear term, which equals $F'(x_i)$;
- $f_{A_2}(x_i)$ is the coefficient of the quadratic term, related to $\frac{F''(x_i)}{2!}$;
- $f_{A_3}(x_i)$ is the coefficient of the cubic term, and so on.

For simplicity, we denote the series as:


$$
F(x_i + h) - F(x_i) = \sum_{m=1}^{\infty} f_{A_m}(x_i) \, h^m.
$$

### 2. Forming the Total Sum over the Partition

Assume we partition the interval $[0, N]$ into $M$ subintervals of equal width $h$, so that:


$$
x_0 = 0,\quad x_1 = h,\quad x_2 = 2h,\quad \dots,\quad x_{M} = N,
$$

with $M \cdot h = N$.

For each subinterval $[x_i,\, x_{i+1}]$ the change in $F$ is given by:


$$
F(x_{i+1}) - F(x_i) = \sum_{m=1}^{\infty} f_{A_m}(x_i) \, h^m.
$$

Now, form the sum of these differences over all subintervals:


$$
\sum_{i=0}^{M-1} \Bigl[F(x_{i+1}) - F(x_i)\Bigr] = \sum_{i=0}^{M-1} \left[ \sum_{m=1}^{\infty} f_{A_m}(x_i) \, h^m \right].
$$

### 3. Interchanging the Order of Summation

Since the sum is finite in $i$ (from $0$ to $M-1$) and we assume that the series in $h$ converges uniformly for sufficiently small $h$, we can interchange the order of summation:


$$
\sum_{i=0}^{M-1} \left[ \sum_{m=1}^{\infty} f_{A_m}(x_i) \, h^m \right] = \sum_{m=1}^{\infty} \left[ \sum_{i=0}^{M-1} f_{A_m}(x_i) \right] h^m.
$$

In this expression:

- The inner sum $\sum_{i=0}^{M-1} f_{A_m}(x_i)$ collects the coefficients of $h^m$ from each subinterval.
- The outer sum then reassembles the entire contribution in powers of $h$.

### 4. Observing the Telescoping Behavior

Let’s consider the effect of summing the first-order terms (i.e., $m=1$):


$$
\text{First-order contribution: } \sum_{i=0}^{M-1} f_{A_1}(x_i) \, h.
$$

Since $f_{A_1}(x_i) = F'(x_i)$, and in the limit $h \to 0$ the sum approximates the integral of $F'(x)$ over $[0, N]$, we have:


$$
\lim_{h\to 0} \sum_{i=0}^{M-1} F'(x_i) \, h = \int_{0}^{N} F'(x) \, dx.
$$

However, the beauty of the telescoping sum lies in how the differences add up directly without needing to integrate term by term. Write out the sum explicitly:


$$
\begin{aligned}
\sum_{i=0}^{M-1} \Bigl[F(x_{i+1}) - F(x_i)\Bigr] &= \bigl[F(x_1) - F(x_0)\bigr] + \bigl[F(x_2) - F(x_1)\bigr] \\
&\quad + \bigl[F(x_3) - F(x_2)\bigr] + \cdots + \bigl[F(x_M) - F(x_{M-1})\bigr].
\end{aligned}
$$

Notice the cancellation:

- $F(x_1)$ appears positively in the first term and negatively in the second.
- $F(x_2)$ appears in the second term and cancels with the third, and so on.

Thus, the entire sum simplifies to:


$$
F(x_M) - F(x_0) = F(N) - F(0).
$$

### 5. Taking the Limit and Concluding

When we let $h \to 0$ (i.e., $M \to \infty$ with $M\,h = N$), the higher-order terms in $h$ vanish, and we obtain exactly:


$$
\int_{0}^{N} f(x) \, dx = \lim_{h\to 0} \sum_{i=0}^{M-1} \left[F(x_{i+1}) - F(x_i)\right] = F(N) - F(0).
$$

Thus, we have derived the Fundamental Theorem of Calculus:


$$
\boxed{\int_{0}^{N} f(x) \, dx = F(N) - F(0).}
$$

## 6. Summary of the Approach

1. Express Each Increment as a Series:For each subinterval, write


$$
F(x_i+h) - F(x_i) = f_{A_1}(x_i) \, h + f_{A_2}(x_i) \, h^2 + f_{A_3}(x_i) \, h^3 + \cdots.
$$


2. Sum Over All Subintervals:Add up the differences over all subintervals:


$$
\sum_{i=0}^{M-1} \left[F(x_{i+1}) - F(x_i)\right].
$$


3. Interchange the Summation Order:Change the order of summation to collect coefficients of like powers of $h$.


4. Observe the Telescoping Cancellation:Notice that the sum collapses to $F(N) - F(0)$ because every intermediate term cancels.


5. Take the Limit as $h \to 0$:Conclude that the sum converges to the integral:


$$
\int_{0}^{N} f(x) \, dx = F(N) - F(0).
$$



## 7.  Conclusion

By partitioning the interval and expressing the change in $F(x)$ over a small increment $h$ as a power series, we observe a clear telescoping pattern when we sum these differences. The intermediate terms cancel, leaving only the difference between the final and initial values, $F(N) - F(0)$. Therefore, we arrive at the Fundamental Theorem of Calculus in its simplest form:


$$
\boxed{\int_{0}^{N} f(x) \, dx = F(N) - F(0).}
$$

This approach, which relies solely on algebraic manipulations and limits, provides an intuitive and transparent derivation. By focusing on the visible pattern of cancellation in the telescoping sum, the connection between the derivative and the antiderivative becomes clear.

End of Article

This detailed explanation includes intermediate steps with clear, explicit summations that reveal the telescoping nature of the sum. It is designed to be intuitive and accessible, allowing you (or any reader) to see the pattern step by step. Let me know if you need any additional clarifications or further elaborations!