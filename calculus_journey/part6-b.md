
# Derivation of Sums of Powers

## 1. Introduction

We wish to understand the structure of the sum


$$
S_p(n) = \sum_{k=1}^{n} k^p,
$$

which is known to be a polynomial in $n$ of degree $p+1$. A key ingredient in deriving the general formula is the binomial identity:


$$
(n+1)^{p+1} - n^{p+1} = \sum_{j=0}^{p} \binom{p+1}{j} n^j.
$$

In this discussion, we will explore the basics of the binomial theorem, derive this identity step by step, and explain how it helps us “build” the general formula by revealing the patterns in the sums.

## 2. The Binomial Theorem: Basics

The Binomial Theorem states that for any nonnegative integer $m$ and any numbers $a$ and $b$,


$$
(a+b)^m = \sum_{j=0}^{m} \binom{m}{j} a^{m-j}b^j,
$$

where the binomial coefficient is defined as


$$
\binom{m}{j} = \frac{m!}{j!(m-j)!}.
$$

A particularly simple case is obtained by setting $a = n$ and $b = 1$. Then,


$$
(n+1)^m = \sum_{j=0}^{m} \binom{m}{j} n^j.
$$

In our case, we will choose $m = p+1$, so that:


$$
(n+1)^{p+1} = \sum_{j=0}^{p+1} \binom{p+1}{j} n^j.
$$

## 3. Deriving the Key Binomial Identity

We are interested in the difference:


$$
(n+1)^{p+1} - n^{p+1}.
$$

Using the binomial theorem, we write:


$$
(n+1)^{p+1} = \sum_{j=0}^{p+1} \binom{p+1}{j} n^j.
$$

Now, notice that the term corresponding to $j = p+1$ is


$$
\binom{p+1}{p+1} n^{p+1} = n^{p+1}.
$$

Subtracting $n^{p+1}$ cancels that term:


$$
(n+1)^{p+1} - n^{p+1} = \sum_{j=0}^{p+1} \binom{p+1}{j} n^j - n^{p+1}.
$$

Since the $j = p+1$ term is exactly $n^{p+1}$, we have:


$$
(n+1)^{p+1} - n^{p+1} = \sum_{j=0}^{p} \binom{p+1}{j} n^j.
$$

Intermediate Steps Explanation:

1. Write the full expansion:


$$
(n+1)^{p+1} = \binom{p+1}{0}n^{p+1} + \binom{p+1}{1} n^{p} + \binom{p+1}{2} n^{p-1} + \cdots + \binom{p+1}{p} n + \binom{p+1}{p+1}.
$$


2. Identify the last term:


$$
\binom{p+1}{p+1} n^{0} = 1.
$$

(Notice: Often one writes the expansion as $(n+1)^{p+1} = n^{p+1} + \binom{p+1}{1}n^p + \cdots + \binom{p+1}{p}n + 1$.)


3. Subtract $n^{p+1}$:


$$
(n+1)^{p+1} - n^{p+1} = \binom{p+1}{1}n^p + \binom{p+1}{2}n^{p-1} + \cdots + \binom{p+1}{p}n + 1.
$$

Here, we re-index by letting $j = 0$ represent the constant term, $j=1$ represent the term with $n$, and so on. That is,


$$
(n+1)^{p+1} - n^{p+1} = \sum_{j=0}^{p} \binom{p+1}{j} n^{j},
$$

where we understand that $\binom{p+1}{0} = 1$.



Thus, the identity is established.

## 4. How This Identity Helps in Deriving the General Formula

### 4.1 Setting Up the Recurrence

The identity


$$
(n+1)^{p+1} - n^{p+1} = \sum_{j=0}^{p} \binom{p+1}{j} n^{j}
$$

is powerful because it expresses the incremental change in $(n+1)^{p+1}$ in terms of lower powers of $n$.

Now, suppose that


$$
S_p(n) = \sum_{k=1}^{n} k^p
$$

is a polynomial in $n$ of degree $p+1$:


$$
S_p(n) = a_{p,0} + a_{p,1}\,n + a_{p,2}\,n^2 + \cdots + a_{p,p+1}\,n^{p+1}.
$$

Since $S_p(0)=0$, we have $a_{p,0} = 0$.

### 4.2 Telescoping via Summation

We can sum the identity for consecutive values of $n$. Consider:


$$
S_p(n+1) - S_p(n) = (n+1)^p.
$$

If we sum both sides from $n=0$ to $N-1$, the left-hand side telescopes:


$$
\sum_{n=0}^{N-1} \Bigl[S_p(n+1) - S_p(n)\Bigr] = S_p(N) - S_p(0) = S_p(N).
$$

On the right-hand side, using the binomial identity, we have:


$$
\sum_{n=0}^{N-1} (n+1)^p.
$$

Alternatively, if we sum the identity


$$
(n+1)^{p+1} - n^{p+1} = \sum_{j=0}^{p} \binom{p+1}{j} n^{j}
$$

from $n=0$ to $N-1$, the left-hand side telescopes to:


$$
N^{p+1} - 0^{p+1} = N^{p+1}.
$$

The right-hand side becomes:


$$
\sum_{j=0}^{p} \binom{p+1}{j} \sum_{n=0}^{N-1} n^{j} = \sum_{j=0}^{p} \binom{p+1}{j} S_j(N-1).
$$

This yields a recurrence that expresses $N^{p+1}$ (a known polynomial) in terms of the sums $S_j$ for $j \le p$. If you already know $S_0, S_1, \dots, S_{p-1}$, you can solve for $S_p(N-1)$.

### 4.3 Directly Observing the Pattern

A key insight is that the left-hand side, $(n+1)^{p+1} - n^{p+1}$, when expanded, contains only powers of $n$ up to $n^p$. Therefore, if we compare the coefficients on both sides (after writing $S_p(n)$ as a polynomial), we obtain a system of equations relating the coefficients $a_{p,k}$ to binomial coefficients. In particular, one finds that:


$$
\sum_{k=j+1}^{p+1} a_{p,k}\,\binom{k}{j} = \binom{p}{j}, \quad \text{for } j=0,1,\dots,p.
$$

This system allows you to solve for the coefficients $a_{p,k}$ one by one. Notably, the highest coefficient comes out to be:


$$
a_{p,p+1} = \frac{1}{p+1},
$$

which is consistent with the observation that the leading term of the polynomial is $\frac{n^{p+1}}{p+1}$ (as one would expect from the integral of $x^p$). The lower-order coefficients are determined by the binomial coefficients and display a symmetry that is both combinatorial and elegant.

## 5. Conclusion

The binomial identity


$$
(n+1)^{p+1} - n^{p+1} = \sum_{j=0}^{p} \binom{p+1}{j} n^{j}
$$

provides a powerful and intuitive way to derive the general formula for sums of powers. By summing over $n$ and changing the order of summation, we obtain a recurrence relation that expresses $S_p(n)$ in terms of lower-order sums. This approach not only confirms that $S_p(n)$ is a polynomial of degree $p+1$ with leading coefficient $\frac{1}{p+1}$ but also reveals that the other coefficients are determined by binomial coefficients.

This method is both natural and intuitive because it builds on the familiar binomial theorem and the telescoping property of finite differences. Once you grasp this approach, you can derive the general formula (Faulhaber’s formula) systematically, and you gain deep insight into the combinatorial structure underlying these sums.

End of Article

This article provides an expanded, intuitive, and step-by-step explanation of the role of the binomial identity in deriving the general formula for sums of powers. It emphasizes changing the order of summation, setting up the recurrence, and observing the symmetry in the coefficients. 