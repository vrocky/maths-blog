# Building Calculus from First Principles

## Part II: Algebraic Patterns in Differentiation Formulas

### Preface

In the first installment of this series, we showed that by representing a function with an infinitesimally small increment as


$$
f(x+\Delta x) = A_0 + A_1\,\Delta x + A_2\,(\Delta x)^2 + A_3\,(\Delta x)^3 + \cdots,
$$

and by “peeling off” the contributions term‐by‐term, we discovered that


$$
A_0 = f(x),\quad A_1 = f'(x),\quad A_2 = \frac{f''(x)}{2!},\quad \dots,
$$

which yields the Taylor series expansion. In this article, we continue our journey by exploring how algebraic patterns in series expansions lead naturally to the differentiation formulas for products and compositions of functions. Our approach remains entirely elementary and algebraic; we refrain from invoking geometric notions such as slopes or rates of change. Instead, we focus on seeing and understanding the patterns that arise when we manipulate these series.

### 1. Simple Algebraic Expansions

To build our intuition, consider the following familiar expansions:

1. Square:

$$
(x+\Delta x)^2 = x^2 + 2x\,\Delta x + (\Delta x)^2.
$$


2. Cube:

$$
(x+\Delta x)^3 = x^3 + 3x^2\,\Delta x + 3x\,(\Delta x)^2 + (\Delta x)^3.
$$


3. Fourth Power:

$$
(x+\Delta x)^4 = x^4 + 4x^3\,\Delta x + 6x^2\,(\Delta x)^2 + 4x\,(\Delta x)^3 + (\Delta x)^4.
$$


4. Fifth Power:

$$
(x+\Delta x)^5 = x^5 + 5x^4\,\Delta x + 10x^3\,(\Delta x)^2 + 10x^2\,(\Delta x)^3 + 5x\,(\Delta x)^4 + (\Delta x)^5.
$$



These formulas display a clear pattern: each expansion is composed of terms of increasing order in $\Delta x$. Our method in this series is to “read off” these patterns and use them to derive differentiation formulas.

### 2. Insights for Differentiation Formulas

Recall from our previous article that the coefficient of $\Delta x$ in the expansion of $f(x+\Delta x)$ is obtained by subtracting $f(x)$ and dividing by $\Delta x$; in the limit as $\Delta x \to 0$ this coefficient becomes $f'(x)$. In other words, the algebraic pattern we see in the expansion is:

- The constant term (order $0$) is $f(x)$.
- The coefficient of $\Delta x$ (first order) is $f'(x)$.
- The coefficient of $(\Delta x)^2$ (second order) is $\frac{f''(x)}{2!}$.
- And so on.

Our goal now is to apply this pattern to derive the multiplication rule and the chain rule.

### 3. The Multiplication Rule for Differentiation

Consider two functions $f$ and $g$. Suppose that for a small increment $h$ we have their series expansions:


$$
\begin{aligned}
f(x+h) &= A_0 + A_1\,h + A_2\,h^2 + A_3\,h^3 + \cdots,\\[1mm]
g(x+h) &= B_0 + B_1\,h + B_2\,h^2 + B_3\,h^3 + \cdots,
\end{aligned}
$$

where, by our earlier results,


$$
A_0 = f(x),\quad A_1 = f'(x),\quad \ldots \quad \text{and} \quad B_0 = g(x),\quad B_1 = g'(x),\quad \ldots
$$

When we multiply these two series, the product becomes:


$$
\begin{aligned}
f(x+h)\,g(x+h) &= (A_0 + A_1\,h + A_2\,h^2 + \cdots)(B_0 + B_1\,h + B_2\,h^2 + \cdots)\\[1mm]
&= A_0B_0\\[1mm]
&\quad + h\,(A_0B_1 + A_1B_0)\\[1mm]
&\quad + h^2\,(A_0B_2 + A_1B_1 + A_2B_0)\\[1mm]
&\quad + h^3\,(A_0B_3 + A_1B_2 + A_2B_1 + A_3B_0) + \cdots.
\end{aligned}
$$

Focusing on the coefficient of $h$ (the first-order term), we see it is


$$
A_0B_1 + A_1B_0.
$$

Substituting the known identities, this becomes


$$
f(x)\,g'(x) + f'(x)\,g(x).
$$

Thus, by recognizing the algebraic pattern in the product series, we recover the multiplication rule for differentiation:


$$
\boxed{\frac{d}{dx}[f(x)g(x)] = f(x)g'(x) + f'(x)g(x).}
$$

### 4. The Chain Rule for Differentiation

One of the most powerful and important rules in calculus is the chain rule. We'll develop it here using our series expansion approach, showing how it emerges naturally from algebraic patterns.

#### 4.1 Understanding the Challenge

When we compose two functions - that is, when we apply one function to the output of another - we need to understand how their derivatives interact. Our series expansion method will reveal this relationship through careful algebraic manipulation.

#### 4.2 Setting Up the Problem

Let's start with two functions expressed in their series forms. We want to see what happens when we compose them:

$$
f(x + h)  = A_0 + A_1 h + A_2 h^2 + A_3 h^3 + A_4 h^4 + A_5 h^5 + A_6 h^6 + \ldots
$$

$$
g(x + h) = B_0 + B_1 h + B_2 h^2 + B_3 h^3 + B_4 h^4 + B_5 h^5 + B_6 h^6 + \ldots
$$

#### 4.3 Building Intuition Through Simple Cases

Before tackling the general case, let's build our understanding through simpler scenarios. This step-by-step approach will help us see the emerging patterns more clearly.

##### Case 1: Linear Inner Function
First, consider what happens when g(x) only has a linear term in its expansion. This simplest case will give us our first glimpse of the pattern:

$$
g(x + h) = B_0 + h = g(x) + h
$$

Let say,

$$
f(g(x) + h) =  C_0 + C_1 h + C_2 h^2 + C_3 h^3 + C_4 h^4 + C_5 h^5 + C_6 h^6 + \ldots
$$

$$
f(g(x+h))= f(B_0 + h) =  f(g(x)+h)  =  C_0 + C_1 h + C_2 h^2 + C_3 h^3 + C_4 h^4 + C_5 h^5 + C_6 h^6 + \ldots
$$

##### Case 2: Two-Term Inner Function
Next, we'll see what happens when g(x) has both constant and linear terms. This reveals more of the general pattern:

$$
g(x + h) = B_0 + B_1 h  = f(g(x) + B_1 h)
$$

$$
f(g(x+h))= f(B_0 + B_1 h) = f(g(x) + B_1 h)  =  C_0 + C_1 B_1 h + C_2 B_1^2 h^2 + C_3 B_1^3 h^3 + C_4 B_1^4 h^4 + C_5 B_1^5 h^5 + C_6 B_1^6 h^6 + \ldots
$$

We can notice the coefficient of h gives us $\frac{d}{dx} [f(g(x))] = f'(g(x)) \cdot g'(x)$

#### 4.4 The General Case: Full Proof

Now that we've built some intuition, let's tackle the complete proof. We'll see how the pattern we observed in simpler cases extends to the general situation:

$$\begin{aligned}

f(g(x+h)) &= f(B_0 + B_1 h + B_2 h^2 + \ldots ) \\
 f(g(x+h)) &= f(B_0 + h(B_1  + B_2 h + B_3 h^2 + \ldots) )\\
  f(g(x+h)) &= f(g(x) + h(B_1  + B_2 h + B_3 h^2 + \ldots) )  \\\\
f(g(x+h)) &= C_0 + \\
&  C_1 (B_1  + B_2 h + B_3 h^2 + \ldots) h  +\\ 
&  C_2 (B_1  + B_2 h + B_3 h^2 + \ldots)^2 h^2  +\\
&  C_3 (B_1  + B_2 h + B_3 h^2 + \ldots)^3 h^3  +\\
&  C_4 (B_1  + B_2 h + B_3 h^2 + \ldots)^4 h^4 + \\
&  C_5 (B_1  + B_2 h + B_3 h^2 + \ldots)^5 h^5 + \ldots  \\\\

f(g(x+h)) &= C_0 + \\
&  C_1 (B_1 h + B_2 h^2 + \ldots )  +\\ 
&  C_2 (B_1 h + B_2 h^2 + \ldots )^2   +\\
&  C_3 (B_1 h + B_2 h^2 + \ldots )^3  +\\
&  C_4 (B_1 h + B_2 h^2 + \ldots )^4  + \\
&  C_5 (B_1 h + B_2 h^2 + \ldots )^5  + \ldots \\ \\


f(g(x+h)) &= C_0 + 
 C_1 (B_1 h + B_2 h^2 + \ldots )  +  C_2 (B_1 h + B_2 h^2 + \ldots )^2   +  C_3 (B_1 h + B_2 h^2 + \ldots )^3  +
  C_4 (B_1 h + B_2 h^2 + \ldots )^4  + 
  C_5 (B_1 h + B_2 h^2 + \ldots )^5  + \ldots \quad(1)


\end{aligned}$$



We can see from these equations that the coefficients of $h^0, h^1 , h^2, ...$ are 

$$\begin{aligned}
\text{Coff}(f(g(x+h)),h^0) &= C_0 \\
\text{Coff}(f(g(x+h)),h^1) &= B_1 C_1 \\
\text{Coff}(f(g(x+h)),h^2) &= B_2 C_1 +  B_1 C_2 \\
\text{Coff}(f(g(x+h)),h^3) &= B_3 C_1 +  B_2 C_2 + B_1 C_3 \\
\text{Coff}(f(g(x+h)),h^4) &= B_4 C_1 +  B_3 C_2 + B_2 C_3 + B_1 C_4
\end{aligned}$$


Well the coefficient of h gives us $\frac{d}{dx} [f(g(x))] = f'(g(x)) \cdot g'(x)$

#### 4.5 Understanding What We Found

The algebraic manipulation reveals something remarkable: when we look at the coefficient of h in our final expansion, it's exactly the product of:
- The derivative of the outer function (evaluated at the inner function's value)
- The derivative of the inner function

This is precisely the chain rule! The pattern shows us that:

$$
\frac{d}{dx}[f(g(x))] = f'(g(x)) \cdot g'(x)
$$

Our algebraic approach has revealed this fundamental relationship without relying on geometric intuition or rates of change.

### Excercise

$\frac{d}{dx}\cos(x^2)$ 

here ,

$f(x)= \cos(x)$ and $g(x) = x^2$

Now, $g(x+h) = (x^2 + 2 x h +  h^2)$

here we can see $f(g(x+h))$ is not lucky enough like $f(x+h)$ to have $+h$ in function which we know expansion of but looking closer it has $+h$ but with some multiplier from $(1)$


$$\begin{aligned}

f(g(x+h)) &= f(B_0 + B_1 h + B_2 h^2 + \ldots ) \\\\

\cos(x + \Delta x) &= \cos(x)\cos(\Delta x) - \sin(x)\sin(\Delta x) \approx \cos(x) - \sin(x) \Delta x \\

\therefore \, \cos(x^2 + 2x h +  h^2) &=  \cos(x^2) - \sin(x^2)\Delta x \\

                                      &= \cos(x^2) - \sin(x^2)(2x h +  h^2)
\end{aligned}$$

from this expansion it is evident that $\frac{d}{dx}\cos(x^2) = - \sin(x^2)(2x)$ 



## differentiation formulas visible from the pattern very easily





1. $(x + \Delta x)^2 = x^2 + 2x\Delta x + (\Delta x)^2$


2. $(x + \Delta x)^3 = x^3 + 3x^2\Delta x + 3x(\Delta x)^2 + (\Delta x)^3$


3. $(x + \Delta x)^4 = x^4 + 4x^3\Delta x + 6x^2(\Delta x)^2 + 4x(\Delta x)^3 + (\Delta x)^4$


4. $(x + \Delta x)^5 = x^5 + 5x^4\Delta x + 10x^3(\Delta x)^2 + 10x^2(\Delta x)^3 + 5x(\Delta x)^4 + (\Delta x)^5$


5. $(x + \Delta x)^6 = x^6 + 6x^5\Delta x + 15x^4(\Delta x)^2 + 20x^3(\Delta x)^3 + 15x^2(\Delta x)^4 + 6x(\Delta x)^5 + (\Delta x)^6$


6. $(x + \Delta x)^7 = x^7 + 7x^6\Delta x + 21x^5(\Delta x)^2 + 35x^4(\Delta x)^3 + 35x^3(\Delta x)^4 + 21x^2(\Delta x)^5 + 7x(\Delta x)^6 + (\Delta x)^7$


7. $\cos(x + \Delta x) = \cos(x)\cos(\Delta x) - \sin(x)\sin(\Delta x) \approx \cos(x) - \sin(x) \Delta x$

8. $\sin(x + \Delta x) = \sin(x)\cos(\Delta x) + \cos(x)\sin(\Delta x)  \approx \sin(x) + \cos(x)\Delta x$




### 6. Pedagogical Benefits of the Pattern-Based Approach

This algebraic, pattern-focused method for developing differentiation formulas offers several advantages as an entry point to calculus:

- Clarity Through Patterns:By “peeling off” the series term-by-term, students can see very clearly how each term corresponds to a higher order of the infinitesimally small quantity. The pattern $A_n = \frac{f^{(n)}(x)}{n!}$ becomes self-evident through elementary algebra.


- Foundation for Differentiation Rules:The multiplication and chain rules emerge naturally from the algebraic manipulation of series. Rather than memorizing rules, students observe that these rules are simply consequences of the underlying patterns in the series expansions.


- A Fresh Entry Point:This approach serves as an alternative starting point for calculus. Instead of beginning with limits and geometric interpretations, the focus is on algebraic patterns—making the subject accessible from a first-principles perspective.


- Consistency and Rigor:Although the presentation is elementary, the method is entirely rigorous when the appropriate limit operations are performed. It reinforces that the standard differentiation formulas are not arbitrary but are built into the very structure of functions expressed as power series.


- Motivation for Further Study:Once students see the natural emergence of these patterns, they are better prepared to understand more advanced topics. The method provides a strong conceptual foundation that can be built upon in courses on analysis, differential equations, and beyond.



### 7. Conclusion

In this article, we extended our first-principles approach by exploring the algebraic patterns that lead to differentiation formulas for products and compositions of functions. We showed that:

- The multiplication of two series produces a pattern where the coefficient of the first-order term is $f(x)g'(x) + f'(x)g(x)$.
- The composition of functions, when expanded in series, reveals that the coefficient of the first-order term is $f'(g(x)) \cdot g'(x)$.

These results—obtained by matching the coefficients of like powers of $h$ or $\Delta x$—demonstrate the multiplication and chain rules in an entirely algebraic and elementary fashion.

This approach not only offers a clear, pattern-based entry point to calculus but also reinforces the idea that the structure of differentiation formulas is inherent in the algebra of infinitesimally small increments. It serves as a foundation that deepens understanding and prepares students for more advanced studies in mathematics.

End of Article

This document should serve as a clear, enhanced version of your work, emphasizing algebraic patterns and pedagogical benefits while avoiding geometric language. It is intended to be part of a series that builds calculus from first principles.

