## Understanding Infinitesimal Calculus: The Power of Δx and Orders of Infinitely Small

Calculus is a branch of mathematics that has revolutionized our understanding of the physical world and plays a fundamental role in various scientific disciplines. At the heart of calculus lies the concept of "infinitesimal calculus," which deals with infinitesimally small quantities and their impact on functions and equations. In this article, we'll explore the significance of Δx and the concept of orders of infinitely small quantities in calculus.

## Orders of Infinitely Small Quantities

In calculus, not all infinitesimals are created equal. Some infinitesimals are smaller than others, and we can categorize them into different "orders" based on their size relative to Δx. The three most common orders of infinitesimal quantities are:

1. First Order Infinitesimals: These are quantities that approach zero at the same rate as Δx. They are usually represented by terms like Δx, Δy, or Δt. First-order infinitesimals are fundamental for calculating derivatives.


2. Higher Order Infinitesimals: These are quantities that decrease faster than Δx as it approaches zero. They are typically represented by terms like Δx², Δx³, and so on. Higher-order infinitesimals are essential for understanding more intricate aspects of functions, such as concavity, curvature, and higher derivatives.


3. Fractional Order Infinitesimals: These are quantities that decrease slower than Δx as it approaches zero. Fractional-order infinitesimals are less commonly used but find applications in advanced mathematics and specialized areas of science.



Understanding the concept of orders of infinitesimals allows mathematicians and scientists to dissect and analyze the behavior of functions with increasing precision. It enables us to explore not only how functions change but also how they change in response to changes in their rate of change.
# Proving the Taylor Series Using Simple Arithmetic

## Introduction
The Taylor series is a powerful mathematical tool used to approximate functions with polynomials. It plays a crucial role in various fields, such as calculus, physics, engineering, and computer science. In this article, we will explore the concept of Taylor series and demonstrate its derivation through straightforward arithmetic, making it accessible to readers with basic mathematical knowledge.


## Understanding the Taylor Series
Before we dive into the arithmetic, let's grasp the fundamental idea behind the Taylor series. It is a representation of a function as an infinite sum of terms, each of which is related to the function's derivatives at a specific point. The Taylor series for a function f(x) centered at a point 'a' is given by:

$f(x) = f(a) + f'(a)(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \frac{f'''(a)}{3!}(x-a)^3 + \ldots$

Here, f'(a), f''(a), f'''(a), and so on, represent the derivatives of the function f(x) evaluated at the point 'a'. The higher-order terms capture more intricate details of the function's behavior around 'a'.

## Deriving the Taylor Series Step by Step:


Let's consider a function such that if we move $\Delta x$ , it shows changes in many orders of infinely small $\Delta x$,


$f(x +  \Delta x) = A_0 + A_1 (\Delta x) + A_3 (\Delta x)^2 + A_4 (\Delta x)^3 + \ldots + A_{n+1} (\Delta x)^n$



clearly here, $A_0 = f(x)$

Lets try another,



$$f'(x) = \frac{f(x + \Delta x) - f(x)}{\Delta x}$$



Substituting the expression for $f(x + \Delta x)$, we get:

$f'(x) = \lim_{\Delta x \to 0} \frac{A_0 + A_1 (\Delta x) + A_2 (\Delta x)^2 + A_3 (\Delta x)^3 + \ldots + A_{n+1} (\Delta x)^n - A_0}{\Delta x}$

Simplifying, and noting that $A_0 = f(x)$ cancels out:

$f'(x) = \lim_{\Delta x \to 0} \frac{A_1 (\Delta x) + A_2 (\Delta x)^2 + A_3 (\Delta x)^3 + \ldots + A_{n+1} (\Delta x)^n}{\Delta x}$

We can further simplify this by dividing each term in the numerator by $\Delta x$:

$f'(x) = \lim_{\Delta x \to 0} \left( A_1 + A_2 \Delta x + A_3 (\Delta x)^2 + \ldots + A_{n+1} (\Delta x)^{n-1} \right)$

As $\Delta x$ approaches zero, all terms containing $\Delta x$ will also approach zero. Therefore, the limit simplifies to:

$f'(x) = A_1$

Thus, the derivative $f'(x)$ of the function is equal to the coefficient $A_1$ of the first-order term in your series expansion.




### Proof for second derivative

To prove a formula for the second derivative using first derivatives, we can use the definition of the derivative and its limit properties. The first derivative of a function $f$ at a point $a$ is defined as:

$f'(a) = \lim_{h \to 0} \frac{f(a + h) - f(a)}{h}$

Now, the second derivative $f''(a)$ is the derivative of the first derivative $f'(x)$. This means we need to find the limit as $h$ approaches 0 of the difference quotient of $f'(x)$. The expression for the second derivative is:

$f''(a) = \lim_{h \to 0} \frac{f'(a + h) - f'(a)}{h}$


 To derive a formula for the second derivative using first derivatives without involving nested limits, we'll use an approximation with an infinitely small increment, $\Delta x$, instead of taking the limit. This method, while not as rigorous as the limit definition, can provide a good intuition and a working formula.

Let's start by considering the first derivative of $f(x)$ at two points, $x = a$ and $x = a + \Delta x$, where $\Delta x$ is an infinitely small increment:

1. The first derivative at $x = a$ is approximately $f'(a) \approx \frac{f(a + \Delta x) - f(a)}{\Delta x}$.
2. The first derivative at $x = a + \Delta x$ is approximately $f'(a + \Delta x) \approx \frac{f(a + 2\Delta x) - f(a + \Delta x)}{\Delta x}$.

Now, the second derivative at $x = a$ can be approximated as the change in the first derivative over an interval $\Delta x$:

$f''(a) \approx \frac{f'(a + \Delta x) - f'(a)}{\Delta x}$

Substituting the approximations for $f'(a + \Delta x)$ and $f'(a)$, we get:

$f''(a) \approx \frac{\left( \frac{f(a + 2\Delta x) - f(a + \Delta x)}{\Delta x} \right) - \left( \frac{f(a + \Delta x) - f(a)}{\Delta x} \right)}{\Delta x}$

Expanding this, we have:

$f''(a) \approx \frac{f(a + 2\Delta x) - f(a + \Delta x) - f(a + \Delta x) + f(a)}{\Delta x^2}$

Simplifying:

$f''(a) \approx \frac{f(a + 2\Delta x) - 2f(a + \Delta x) + f(a)}{\Delta x^2}$

This formula provides an approximation for the second derivative of $f(x)$ at $x = a$, using the concept of an infinitely small $\Delta x$. Note that this is an approximation and not as precise as using the limit definition. However, it can be quite useful in numerical methods and for gaining an intuitive understanding of the second derivative.


So now we worked 

$f'(x) =$ $\frac{f\left(a+h\right)-f\left(a\right)}{h}$


Similarly we arrive at result for 
$$\begin{align}

f''(a) &= -\frac{\frac{f\left(a+h\right)-f\left(a\right)}{h}+\frac{f\left(a+h\right)-f\left(a+2\,h\right)}{h}}{h} = \frac{f\left(a\right)-2\,f\left(a+h\right)+f\left(a+2\,h\right)}{h^2 } \\
 
f'''(a) &= \frac{3\,f\left(a+h\right)-f\left(a\right)-3\,f\left(a+2\,h\right)+f\left(a+3\,h\right)}{h^3 }   \\


f''''(a) &=  \frac{f\left(a\right)-4\,f\left(a+h\right)+6\,f\left(a+2\,h\right)-4\,f\left(a+3\,h\right)+f\left(a+4\,h\right)}{h^4 }   \\

f^5(a) &=  \frac{5\,f\left(a+h\right)-f\left(a\right)-10\,f\left(a+2\,h\right)+10\,f\left(a+3\,h\right)-5\,f\left(a+4\,h\right)+f\left(a+5\,h\right)}{h^5 }   \\

f^6(a) &=  \frac{f\left(a\right)-6\,f\left(a+h\right)+15\,f\left(a+2\,h\right)-20\,f\left(a+3\,h\right)+15\,f\left(a+4\,h\right)-6\,f\left(a+5\,h\right)+f\left(a+6\,h\right)}{h^6 }   \\


\end{align}$$

Now we are going to put $f(x +  \Delta x) = A_0 + A_1 (\Delta x) + A_3 (\Delta x)^2 + A_4 (\Delta x)^3 + \ldots + A_{n+1} (\Delta x)^n$ to above difference equations

Here,



Also,

$$\begin{align}

f(a + h) &= A_0 + A_1 (h) + A_2 (h)^2 + A_3 (h)^3 + \ldots + A_{n+1} (h)^n  \\


f(a + 2h) &= A_0 +{\left(2\,h\right)}\,A_1 +{\left(4\,h^2 \right)}\,A_2 +{\left(8\,h^3 \right)}\,A_3 +{\left(16\,h^4 \right)}\,A_4 +{\left(32\,h^5 \right)}\,A_5 +{\left(64\,h^6 \right)}\,A_6 + \ldots   \\

f(a + 3h) &= A_0 +{\left(3\,h\right)}\,A_1 +{\left(9\,h^2 \right)}\,A_2 +{\left(27\,h^3 \right)}\,A_3 +{\left(81\,h^4 \right)}\,A_4 +{\left(243\,h^5 \right)}\,A_5 +{\left(729\,h^6 \right)}\,A_6 + \ldots  \\


f(a + 4h) &= A_0 +{\left(4\,h\right)}\,A_1 +{\left(16\,h^2 \right)}\,A_2 +{\left(64\,h^3 \right)}\,A_3 +{\left(256\,h^4 \right)}\,A_4 +{\left(1024\,h^5 \right)}\,A_5 +{\left(4096\,h^6 \right)}\,A_6 +  \ldots \\

f(a + 5h) &= A_0 +{\left(5\,h\right)}\,A_1 +{\left(25\,h^2 \right)}\,A_2 +{\left(125\,h^3 \right)}\,A_3 +{\left(625\,h^4 \right)}\,A_4 +{\left(3125\,h^5 \right)}\,A_5 +{\left(15625\,h^6 \right)}\,A_6 + \ldots

\end{align}$$


So now,

Lets find $f'(x)$ , 

$f'(x) =$ $\frac{f\left(a+h\right)-f\left(a\right)}{h}$


$$\begin{aligned}
 f(a + h) &= A_0 + A_1 (h) + A_2 (h)^2 + A_3 (h)^3 + \ldots + A_{n+1} (h)^n \\
  f(a) &= A_0 \\

   f(a + h) -f(a) &=  A_1 (h) + A_2 (h)^2 + A_3 (h)^3 + \ldots + A_{n+1} (h)^n \\ \\

    f'(x)   =   \frac{f\left(a+h\right)-f\left(a\right)}{h} &= A_1 +h\,A_2 +h^2 \,A_3 +h^3 \,A_4 +h^4 \,A_5 +h^5 \,A_6 + \ldots \\\\\\

      f'(x) &\approx A_1
\end{aligned}$$



Lets find $f''(a)$ , 

$f''(a) =$ $\frac{f\left(a\right)-2\,f\left(a+h\right)+f\left(a+2\,h\right)}{h^2 }$


$$\begin{aligned}
f(a + 2h) &= A_0 +{\left(2\,h\right)}\,A_1 +{\left(4\,h^2 \right)}\,A_2 +{\left(8\,h^3 \right)}\,A_3 +{\left(16\,h^4 \right)}\,A_4 +{\left(32\,h^5 \right)}\,A_5 +{\left(64\,h^6 \right)}\,A_6 \\
 2f(a + h) &= 2A_0 + 2A_1 (h) + 2A_2 (h)^2 + 2A_3 (h)^3 + \ldots + 2A_{n+1} (h)^n \\
  f(a) &= A_0 \\ \\

   f\left(a\right)-2\,f\left(a+h\right)+f\left(a+2\,h\right) &=  0 + 0 + 2\,A_2 +{\left(6\,h\right)}\,A_3 +{\left(14\,h^2 \right)}\,A_4 +{\left(30\,h^3 \right)}\,A_5 +{\left(62\,h^4 \right)}\,A_6 + \ldots \\ \\

    f''(a) = \frac{f\left(a\right)-2\,f\left(a+h\right)+f\left(a+2\,h\right)}{h^2 } &= 2\,A_2 +{\left(6\,h\right)}\,A_3 +{\left(14\,h^2 \right)}\,A_4 +{\left(30\,h^3 \right)}\,A_5 +{\left(62\,h^4 \right)}\,A_6 +  \ldots \\\\\\

      f''(a) &\approx 2\,A_2
\end{aligned}$$





Lets find $f'''(a)$ , 

$f'''(a) =$ $\frac{3\,f\left(a+h\right)-f\left(a\right)-3\,f\left(a+2\,h\right)+f\left(a+3\,h\right)}{h^3 }$


$$\begin{aligned}
f(a + 2h) &= A_0 +{\left(2\,h\right)}\,A_1 +{\left(4\,h^2 \right)}\,A_2 +{\left(8\,h^3 \right)}\,A_3 +{\left(16\,h^4 \right)}\,A_4 +{\left(32\,h^5 \right)}\,A_5 +{\left(64\,h^6 \right)}\,A_6 + \ldots \\ \\\\


-3f(a+2h)  &= -3\,A_0 +{\left(-6\,h\right)}\,A_1 +{\left(-12\,h^2 \right)}\,A_2 +{\left(-24\,h^3 \right)}\,A_3 +{\left(-48\,h^4 \right)}\,A_4 +{\left(-96\,h^5 \right)}\,A_5 +{\left(-192\,h^6 \right)}\,A_6\\



 3f(a + h) &= 3A_0 + 3A_1 (h) + 3A_2 (h)^2 + 3A_3 (h)^3 + \ldots + 3A_{n+1} (h)^n \\
  -f(a) &= -A_0 \\
  
  
  f(a + 3h) &=A_0 +{\left(3\,h\right)}\,A_1 +{\left(9\,h^2 \right)}\,A_2 +{\left(27\,h^3 \right)}\,A_3 +{\left(81\,h^4 \right)}\,A_4 +{\left(243\,h^5 \right)}\,A_5 +{\left(729\,h^6 \right)}\,A_6
  
  
  \\

3\,f\left(a+h\right)-f\left(a\right)-3\,f\left(a+2\,h\right)+f\left(a+3\,h\right) &=  0 + 0 + 0 + 6\,A_3 +{\left(36\,h\right)}\,A_4 +{\left(150\,h^2 \right)}\,A_5 +{\left(540\,h^3 \right)}\,A_6 + \ldots \\


\\ \\

 f'''(a) =\frac{3\,f\left(a+h\right)-f\left(a\right)-3\,f\left(a+2\,h\right)+f\left(a+3\,h\right)}{h^3 } &= 6\,A_3 +{\left(36\,h\right)}\,A_4 +{\left(150\,h^2 \right)}\,A_5 +{\left(540\,h^3 \right)}\,A_6 + \ldots
 
 \\\\\\

      f'''(a) &\approx 6\,A_3
\end{aligned}$$


Now, we some results,
$$\begin{align}

    f'(x) &= A_1 +h\,A_2 +h^2 \,A_3 +h^3 \,A_4 +h^4 \,A_5 +h^5 \,A_6 + \ldots\\

    f''(x) &= 2\,A_2 +{\left(6\,h\right)}\,A_3 +{\left(14\,h^2 \right)}\,A_4 +{\left(30\,h^3 \right)}\,A_5 +{\left(62\,h^4 \right)}\,A_6 + \ldots  \\


    f'''(x) &= 6\,A_3 +{\left(36\,h\right)}\,A_4 +{\left(150\,h^2 \right)}\,A_5 +{\left(540\,h^3 \right)}\,A_6 +  \ldots\\


    f''''(x)  &= 24\,A_4 +{\left(240\,h\right)}\,A_5 +{\left(1560\,h^2 \right)}\,A_6  + \ldots\\

    f^5(x) &= 120\,A_5 +{\left(1800\,h\right)}\,A_6 + \ldots
\end{align}$$

this gives us


$$\begin{align}

    f'(x) &\approx A_1 \\

    f''(x) &\approx 2\,A_2   \\


    f'''(x) &\approx 6\,A_3 \\


    f''''(x)  &\approx 24\,A_4 \\

    f^5(x) &\approx 120\,A_5 \\

\end{align}$$

which tells that the coefficients $A_0, A_1, A_2, A_3, A_4, A_5$ in the Taylor series expansion are determined by the derivatives of the function $f(x)$ evaluated at the point $x$ where you are expanding the series. Here are the first six coefficients:

$$\begin{align*}
A_0 &= f(x) \\
A_1 &= f'(x) \\
A_2 &= \frac{f''(x)}{2!} \\
A_3 &= \frac{f'''(x)}{3!} \\
A_4 &= \frac{f''''(x)}{4!} \\
A_5 &= \frac{f'''''(x)}{5!} \\
\end{align*}$$

The Taylor series expansion for the function $f(x + \Delta x)$ around the point $x$ is given by:

$$f(x + \Delta x) = A_0 + A_1 (\Delta x) + \frac{A_2}{2!} (\Delta x)^2 + \frac{A_3}{3!} (\Delta x)^3 + \frac{A_4}{4!} (\Delta x)^4 + \frac{A_5}{5!} (\Delta x)^5 + \ldots$$

You can continue this pattern for higher-order terms by increasing the power of $\Delta x$ and using the corresponding coefficients $A_k$, where $k$ is the order of the derivative.


## Insights for proof for differentiation formulas

We can easily see $A_1$ cofficient and find derivative of and instead of remembering derivative lets keep  these expansion in mind.

## Simple formulas

1. $(x + \Delta x)^2 = x^2 + 2x\Delta x + (\Delta x)^2$


2. $(x + \Delta x)^3 = x^3 + 3x^2\Delta x + 3x(\Delta x)^2 + (\Delta x)^3$


3. $(x + \Delta x)^4 = x^4 + 4x^3\Delta x + 6x^2(\Delta x)^2 + 4x(\Delta x)^3 + (\Delta x)^4$


4. $(x + \Delta x)^5 = x^5 + 5x^4\Delta x + 10x^3(\Delta x)^2 + 10x^2(\Delta x)^3 + 5x(\Delta x)^4 + (\Delta x)^5$


5. $(x + \Delta x)^6 = x^6 + 6x^5\Delta x + 15x^4(\Delta x)^2 + 20x^3(\Delta x)^3 + 15x^2(\Delta x)^4 + 6x(\Delta x)^5 + (\Delta x)^6$


6. $(x + \Delta x)^7 = x^7 + 7x^6\Delta x + 21x^5(\Delta x)^2 + 35x^4(\Delta x)^3 + 35x^3(\Delta x)^4 + 21x^2(\Delta x)^5 + 7x(\Delta x)^6 + (\Delta x)^7$


7. $\cos(x + \Delta x) = \cos(x)\cos(\Delta x) - \sin(x)\sin(\Delta x) \approx \cos(x) - \sin(x) \Delta x$

8. $\sin(x + \Delta x) = \sin(x)\cos(\Delta x) + \cos(x)\sin(\Delta x)  \approx \sin(x) + \cos(x)\Delta x$


<br>

## Multiplication rule for differentiation 

Lets proof multiplication rule for differentiation for next steps: 

Let , 

$f(x + h)  = A_0 + A_1 h + A_2 h^2 + A_3 h^3 + A_4 h^4 + A_5 h^5 + A_6 h^6+\ldots$



$g(x + h) = B_0 + B_1 h + B_2 h^2 + B_3 h^3 + B_4 h^4 + B_5 h^5 + B_6 h^6 + \ldots$

Now 
$$
f(x + h) g(x + h) = A_0 \,B_0 +\mathrm{h}\,{
  \left(A_0 \,B_1 +A_1 \,B_0 \right)}
  +{\mathrm{h}}^2 \,{\left(A_0 \,B_2 +A_1 \,B_1 +A_2 \,B_0 \right)}
  +{\mathrm{h}}^3 \,{\left(A_0 \,B_3 +A_1 \,B_2 +A_2 \,B_1 +A_3 \,B_0 \right)}
  +{\mathrm{h}}^4 \,{\left(A_0 \,B_4 +A_1 \,B_3 +A_2 \,B_2 +A_3 \,B_1 +A_4 \,B_0 \right)}+  \ldots
$$
The coefficient of $dx$ in the above equation serves as a clear manifestation of the chain rule's role in differentiation.
The matrix representation of coefficients provides a convenient way to visualize this process in real-time, akin to how Cantor's diagonal argument is employed to demonstrate the uncountability of sets, especially when dealing with infinite matrices.


## Chain rule for differentiation 

Lets try to proof chain rule for differentiation

### Statement

Let , 


$f(x + h)  = A_0 + A_1 h + A_2 h^2 + A_3 h^3 + A_4 h^4 + A_5 h^5 + A_6 h^6 + \ldots$

$g(x + h) = B_0 + B_1 h + B_2 h^2 + B_3 h^3 + B_4 h^4 + B_5 h^5 + B_6 h^6 + \ldots$



Now we want to analyse the cofficient of h in expansion of $f(g(x+h))$

### Proof Idea workout

before working through this lets take simple case,

for now take case where

$f(x + h)  = A_0 + A_1 h + A_2 h^2 + A_3 h^3 + A_4 h^4 + A_5 h^5 + A_6 h^6 + \ldots$

$g(x + h) = B_0 + h = g(x) + h$

Let say,

$f(g(x) + h) =  C_0 + C_1 h + C_2 h^2 + C_3 h^3 + C_4 h^4 + C_5 h^5 + C_6 h^6 + \ldots$


$f(g(x+h))= f(B_0 + h) =  f(g(x)+h)  =  C_0 + C_1 h + C_2 h^2 + C_3 h^3 + C_4 h^4 + C_5 h^5 + C_6 h^6 + \ldots$

another case


$f(g(x) + h) =  C_0 + C_1 h + C_2 h^2 + C_3 h^3 + C_4 h^4 + C_5 h^5 + C_6 h^6 + \ldots$

$g(x + h) = B_0 + B_1 h  = f(g(x) + B_1 h)$

$f(g(x+h))= f(B_0 + B_1 h) = f(g(x) + B_1 h)  =  C_0 + C_1 B_1 h + C_2 B_1^2 h^2 + C_3 B_1^3 h^3 + C_4 B_1^4 h^4 + C_5 B_1^5 h^5 + C_6 B_1^6 h^6 + \ldots$

we can notice the cofficient of h gives us $\frac{d}{dx} [f(g(x))] = f'(g(x)) \cdot g'(x)$

### Proof
Now lets workout on general case,


$g(x + h) = B_0 + B_1 h + B_2 h^2 + B_3 h^3 + B_4 h^4 + B_5 h^5 + B_6 h^6 + \ldots$






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



we can see from these equations that cofficient of $h^0, h^1 , h^2, ...$ are 

$$\begin{aligned}
\text{Coff}(f(g(x+h)),h^0) &= C_0 \\
\text{Coff}(f(g(x+h)),h^1) &= B_1 C_1 \\
\text{Coff}(f(g(x+h)),h^2) &= B_2 C_1 +  B_1 C_2 \\
\text{Coff}(f(g(x+h)),h^3) &= B_3 C_1 +  B_2 C_2 + B_1 C_3 \\
\text{Coff}(f(g(x+h)),h^4) &= B_4 C_1 +  B_3 C_2 + B_2 C_3 + B_1 C_4
\end{aligned}$$


Well the cofficient of h gives us $\frac{d}{dx} [f(g(x))] = f'(g(x)) \cdot g'(x)$


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


## L Hospital Rule

Statement: If the limit of the quotient of two functions $f(x)$ and $g(x)$ as $x$ approaches $a$ is an indeterminate form $0/0$ or $\infty/\infty$, and both $f(x)$ and $g(x)$ are differentiable functions near $x = a$ (except possibly at $a$), then the limit can be found by taking the derivative of the numerator and denominator and evaluating the limit again.

$$
\lim_{{x \to a}} \frac{f(x)}{g(x)} = \lim_{{x \to a}} \frac{f'(x)}{g'(x)}

$$

### Proof:

1. Start with the indeterminate form:

$$
\lim_{{x \to a}} \frac{f(x)}{g(x)} = \frac{0}{0} \text{ or } \frac{\infty}{\infty}.
$$

1. Write the Taylor series expansion of both $f(x)$ and $g(x)$ centered at $x = a$:

$$
f(x) = f(a) + f'(a)h + \frac{f''(a)}{2}h^2 + \ldots
$$

$$
g(x) = g(a) + g'(a)h + \frac{g''(a)}{2}h^2 + \ldots
$$

1. Since we have an indeterminate form, $f(a)$ and $g(a)$ should both be $0$ (for $0/0$) or $\infty$ (for $\infty/\infty$).


2. Divide both the numerator and denominator by $h$:



$$
\lim_{{x \to a}} \frac{f(x)}{g(x)} = \lim_{{x \to a}} \frac{f(a) + f'(a)h + \frac{f''(a)}{2}h^2 + \ldots}{g(a) + g'(a)h + \frac{g''(a)}{2}h^2 + \ldots}
$$

1. Cancel out the common factor of $h$ in the numerator and denominator:

$$
\lim_{{x \to a}} \frac{f(x)}{g(x)} = \lim_{{x \to a}} \frac{f'(a) + \frac{f''(a)}{2}h + \ldots}{g'(a) + \frac{g''(a)}{2}h + \ldots}
$$

1. As $x$ approaches $a$, all terms with $h$ in the numerator and denominator go to zero. We are then left with:

$$
\lim_{{x \to a}} \frac{f(x)}{g(x)} = \frac{f'(a)}{g'(a)}
$$

1. The limit of $\frac{f(x)}{g(x)}$ as $x$ approaches $a$ is equal to the limit of $\frac{f'(x)}{g'(x)}$ as $x$ approaches $a$:

$$
\lim_{{x \to a}} \frac{f(x)}{g(x)} = \lim_{{x \to a}} \frac{f'(x)}{g'(x)}
$$

This completes the proof of L'Hôpital's Rule.


## Division Properties and Infinte series

Lets work for $\frac{d}{dx}\frac{1}{x}$ or $\frac{d}{dx}{x^{-1}}$ 


So lets expand $(x+h)^{-1}$
$$
f(x + h) = \frac{1}{x+h}
$$

What is your idea to get it into form so that we can get cofficient of $h$ . Its strange how i was missing on this concept from so long . Here we have to use **Long Division** method. 

If you forgot what is long division let me remind you 

### Long division Revision

To perform the long division for $\frac{x^4 - 4}{x + 2}$ and represent it in LaTeX, we'll follow the same method as shown in your example. Let's go through the division step by step and then I'll provide the LaTeX code for it.

Long Division Steps:
1. Divide the first term of the numerator ($x^4$) by the first term of the denominator ($x$), which gives $x^3$.
2. Multiply the entire denominator ($x + 2$) by $x^3$ and subtract this from the numerator.
3. Bring down the next term of the numerator and repeat these steps until all terms of the numerator are used.

$$\begin{array}{c|cccc}
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
\end{array}$$


the long division process of $x^4 - 1$ by $x + 2$ into a step-by-step equation format:

$$\begin{align*}
x^4 - 1 & = (x + 2)(x^3) - 2x^3 - 1 \\
& = (x + 2)(x^3) - (x + 2)(2x^2) + 4x^2 - 1 \\
& = (x + 2)(x^3) - (x + 2)(2x^2) + (x + 2)(4x) - 8x - 1 \\
& = (x + 2)(x^3) - (x + 2)(2x^2) + (x + 2)(4x) - (x + 2)(-8) - 15 \\
& = (x + 2)(x^3 - 2x^2 + 4x - 8) - 15.
\end{align*}$$

This is the step-by-step breakdown of the long division process for $x^4 - 1$ divided by $x + 2$.


Lets do the same with $\frac{1}{x + h}$,

You can derive the series expansion for $\frac{1}{x + h}$ using the method you've mentioned, which is to expand the expression step by step. Here's the derivation:

Starting with $\frac{1}{x + h}$, you can rewrite it as:

$$
\frac{1}{x + h} = (x + h) \left(\frac{1}{x}\right) - \frac{h}{x}
$$

Now, you can expand the first term on the right side:

$$
= (x + h) \left(\frac{1}{x}\right) - (x + h)\left(\frac{h}{x^2}\right)
$$

Next, expand the second term:

$$
= (x + h) \left(\frac{1}{x}\right) - (x + h)\left(\frac{h}{x^2}\right) + (x + h)\left(\frac{h^2}{x^3}\right)
$$

We can continue this process by expanding each new term obtained:

$$
= (x + h) \left(\frac{1}{x}\right) - (x + h)\left(\frac{h}{x^2}\right) + (x + h)\left(\frac{h^2}{x^3}\right) - (x + h)\left(\frac{h^3}{x^4}\right) + \ldots
$$

Notice that each term alternates in sign and involves higher powers of $h$ and lower powers of $x$. The general term in the series expansion is given by:

$$
\frac{(-1)^n h^n}{x^{n+1}}
$$

Step 6: Final Series Expansion
The series expansion for $\frac{1}{x + h}$ is obtained by summing all these terms:

$$
\frac{1}{x + h} = \frac{1}{x} - \frac{h}{x^2} + \frac{h^2}{x^3} - \frac{h^3}{x^4} + \frac{h^4}{x^5} - \ldots
$$


In this tutorial, we have learned how to derive the series expansion for $\frac{1}{x + h}$ using algebraic manipulation. By breaking down the expression into a series of terms and identifying the general term, we can express the function as an infinite sum involving powers of $h$ and $x$. This technique is valuable in mathematics and science for approximating functions and solving complex problems.


This is the series expansion for $\frac{1}{x + h}$.

and clearly cofficient of $h$ gets us $\frac{d}{dx}\frac{1}{x}$  =  $\frac{1}{-x^2}$ or $\frac{d}{dx}{x^{-1}}$  = $-x^{-2}$.




I understand you'd like an infinite series representation for the function $\frac{1}{ax+by}$ without using Taylor series. You can try to express it as a power series in terms of $x$ and $y$ directly. However, keep in mind that not all functions can be easily expressed as simple power series without Taylor series expansion.

## Some Infinite series formulas

### $\frac{1}{x+1} = \sum_{n=0}^{\infty} (-1)^n x^n$ , For $|x| < 1$,  series converges

### $\frac{1}{x+1} = \sum_{n=0}^{\infty} (-1)^n \frac{1}{x}^n$ , For $|x| > 1$,  series converges


### Proof:
We can proof the both with our long division that we take as elementary proof, 

but lets me give you traditional words on it for the reference :

derive the summation formulas for both series expansions of $(1 + x)^{-1}$.

1. Binomial Series Expansion: The summation formula when $|x| < 1$ is a geometric series. The general term of the series is given by $(-1)^n x^n$. The summation formula is:
$\sum_{n=0}^{\infty} (-1)^n x^n = 1 - x + x^2 - x^3 + x^4 - \ldots$
For $|x| < 1$, this series converges to $(1 + x)^{-1}$.


2. Laurent Series Expansion: The summation formula for the case when $|x| > 1$ also follows a geometric progression but with terms involving negative powers of $x$. The general term is $(-1)^{n+1} x^{-n}$. The summation formula is:
$\sum_{n=1}^{\infty} (-1)^{n+1} x^{-n} = x^{-1} - x^{-2} + x^{-3} - \ldots$
This series converges to $(1 + x)^{-1}$ for $|x| > 1$.



Both of these are examples of infinite geometric series, where the sum of the series can be expressed as:
$\text{Sum} = \frac{a}{1 - r}$
where $a$ is the first term and $r$ is the common ratio.

- For the binomial series, $a = 1$ and $r = -x$, so the sum is $\frac{1}{1 - (-x)} = \frac{1}{1 + x}$.
- For the Laurent series, $a = x^{-1}$ and $r = -x^{-1}$, so the sum is $\frac{x^{-1}}{1 - (-x^{-1})} = \frac{1}{x + 1} = (1 + x)^{-1}$, which is valid for $|x| > 1$.




### $\frac{1}{ax+by}= \frac{1}{by} \sum_{n=0}^{\infty} (-1)^n \left(\frac{ax}{by}\right)^n$ , For $|\frac{x}{y}| < 1$,  series converges

### $\frac{1}{ax+by}= \frac{1}{bx} \sum_{n=0}^{\infty} (-1)^n \left(\frac{by}{ax}\right)^n$ , For $|\frac{y}{x}| < 1$,  series converges





### Proof:
$$
\begin{align*}
  \frac{1}{k+1} &= \sum_{n=0}^{\infty} (-1)^n k^n \\

  \frac{1}{ax+by} &= \frac{1}{by} \cdot \frac{1}{k+1} \\
  & = \frac{1}{by} \sum_{n=0}^{\infty} (-1)^n k^n  \\

  & = \frac{1}{by} \sum_{n=0}^{\infty} (-1)^n \left(\frac{ax}{by}\right)^n\\



\end{align*}
$$


## Properties with division involved





### $\frac{d}{dx}[\sec(x)] = \sec(x) \tan(x)$

### Proof:


$$
\begin{align*}
\sec(x + h) &= \frac{1}{\cos(x + h)} \\

\because \cos(x + h) &= \cos(x)\cos(h) - \sin(x)\sin(h) \\

\sec(x + h) &= \frac{1}{\cos(x)\cos(h) - \sin(x)\sin(h)} \\

 \sec(x + h)  &= \frac{1}{ \cos(x) - \sin(x) h}    \\

\end{align*}
$$

Now we can expand this infinite series and get the cofficient of $h$,

or

We can directly say this series is having ratio $(-\sin(x)h)/\cos(x)$  so the term containing $h$ will be $(-\sin(x)h)/\cos^2(x)$ and sign $(-1)^1$

which gives us the requried formula


Lets do the same again with chain rule where


$$\begin{align*}
  f(x) &=  \frac{1}{x} \\
  g(x) &= \cos(x)
\end{align*}$$

we need to find $f(g(x + h))$


$$
\begin{align*}
\sec(x + h) &= \frac{1}{\cos(x + h)} \\

\because \cos(x + h) &= \cos(x)\cos(h) - \sin(x)\sin(h) \\

\sec(x + h) &= \frac{1}{\cos(x)\cos(h) - \sin(x)\sin(h)} \\

 \sec(x + h)  &= \frac{1}{ \cos(x) - \sin(x) h}    \\

\end{align*}
$$

you can easily visualize that expanding first function has given us  $g'(x)$ then $f'(g(x))$ we can remember this as for composite function $h$ is replaced by $g'(x) h$

So we our expansion strategy is very much working same mentally also



### $\frac{d}{dx}[\csc(x)] = -\csc(x) \cot(x)$

### Proof:



$$
\begin{align*}
\csc(x + h) &= \frac{1}{\sin(x + h)}  \\

\because \sin(x + h) &= \sin(x)\cos(h) + \cos(x)\sin(h) \\
\csc(x + h) &= \frac{1}{\sin(x)\cos(h) + \cos(x)\sin(h)} \\
 &= \frac{1}{\sin(x) + \cos(x)h}
\end{align*}
$$

We can directly say this series is having ratio $(\cos(x)h)/\sin(x)$  so the term containing $h$ will be $(\cos(x)h)/\sin^2(x)$ and sign $(-1)^2$

this gives us the requried formula 




### $\frac{d}{dx}(\tan(x)) = \sec^2(x)$

### Proof:


$$
\begin{align*}
\tan(x+h)  &= \frac{\sin(x+h)}{\cos(x+h)} \\
\because \sin(x + \Delta x) &= \sin(x)\cos(\Delta x) + \cos(x)\sin(\Delta x)  \approx \sin(x) + \cos(x)\Delta x\\
\because \cos(x + \Delta x) &= \cos(x)\cos(\Delta x) - \sin(x)\sin(\Delta x) \approx \cos(x) - \sin(x) \Delta x \\

\tan(x+h)  &=\frac{sin(x) + \cos(x)h}{\cos(x) - \sin(x) h } \\
\tan(x+h)  &= [sin(x) + \cos(x)h] * [\frac{1}{\cos(x) - \sin(x) h }] \\

           
\end{align*}

$$

We need to find the cofficient of $h$ in expansion of above term

For $\frac{1}{\cos(x) - \sin(x) h }$ We can directly say this series is having ratio $(\sin(x)h)/\cos(x)$ 


 
 Let, term with  of $h^0$ , $C_0$ and   term with $h^1$ be $C_1$
  
   $$
\begin{align*}
 C_0 &=  \frac{1}{\cos(x)} \\
 C_1 &=  \frac{\sin(x)h}{\cos^2(x)}
 
\end{align*}

$$
   



  Now we can directly say that 




$$
\begin{align*}

\tan(x+h)  &= [sin(x) + \cos(x)h] * [\frac{1}{\cos(x) - \sin(x) h }] \\
           &=  [sin(x) + \cos(x)h] *[C_0 + C_1 x + \ldots]


           
\end{align*}

$$

We can analyse that terms of cofficient of $h$ are $C_0 \cos(x) + C_1\sin(x) $




$$
\begin{align*}

C_0 \cos(x) + C_1\sin(x) &= 1 + \tan^2(x) \\
                          &= \sec^2(x)

 
\end{align*}
$$

## $\frac{d}{dx}(\log(x)) = \frac{1}{x}$


### Proof: 

Lets expand $\log(x+h)$ in terms of power of $h$

$$
\begin{align*}
\log(x + h) &= \log(x(1 + \frac{h}{x}))\\
 &= \log(x) + \log(1 + \frac{h}{x}) \\
 &= \log(x) + \log(1 + \frac{h}{x})
\end{align*}
$$



$$

\begin{align*}


\log(x + h) &= \log(x) + \log(((1+\frac{h}{x})^\frac{x}{h})^\frac{h}{x} ) \\
            & = \log(x) + \log((e)^\frac{h}{x} ) \\
            &= \log(x) + \frac{h}{x}
 
\end{align*}

$$


# Integration

We define integration as 

Let $N = n/\Delta x$

$$

\int_{0}^{N} f(x) \, dx = \lim_{{\Delta x \to 0}} \sum_{i=0}^{n/\Delta x} f(i \cdot \Delta x) \cdot \Delta x
$$




So from here

### $\int 1 \, dx = x + C$
$$
\begin{align*}

\int_{0}^{N} f(x) \, dx &=  \sum_{i=0}^{n/\Delta x} f(i \cdot \Delta x) \cdot \Delta x \\ \\

f(x) &= 1 \\

\int_{0}^{x} 1 \, dx &=\sum_{i=0}^{n/\Delta x} 1 \cdot \Delta x \\
                      &= (n/\Delta x ) \Delta x  \\
                      &= x

\end{align*}
$$


### $\int x \, dx = \frac{1}{2}x^2 + C$
$$
\begin{align*}
\int_{0}^{N} f(x) \, dx &= \lim_{{\Delta n \to 0}} \sum_{i=0}^{n/\Delta x} f(i \cdot \Delta x) \cdot \Delta x  \\




\int_{0}^{x} x \, dx &= \lim_{{\Delta n \to 0}} \sum_{i=0}^{n/\Delta x} (i \cdot \Delta x) \cdot \Delta x \\


\because \frac{n(n + 1)}{2} &= \frac{ n^2 + n}{2}  = \frac{n^2 }{2}+\frac{n }{2} \\


      &= \sum_{i=0}^{n/\Delta x} (i ) \cdot \Delta x^2  \\

      &= [\frac{n^2}{2 \cdot \Delta x^2} \Delta x +  \frac{n}{2 \cdot \Delta x} \Delta x] \cdot  \Delta x



\end{align*}

$$





### $\int x^2 \, dx = \frac{1}{3}x^3 + C$





$$
\begin{align*}

\int_{0}^{N} f(x) \, dx &= \lim_{{\Delta n \to 0}} \sum_{i=0}^{n/\Delta x} f(i \cdot \Delta x) \cdot \Delta x \\


\int_{0}^{N} x^2 \, dx &= \lim_{{\Delta n \to 0}} \sum_{i=0}^{n/\Delta x} (i \cdot \Delta x)^2 \cdot \Delta x \\ \\


\because \frac{n(n + 1)(2n + 1)}{6} &= \frac{2n^3 + 3n^2 + n}{6}  = \frac{n^3 }{3}+\frac{n^2 }{2}+\frac{n}{6} \\




\sum_{i=0}^{n/\Delta x} (i \cdot \Delta x)^2 \cdot \Delta x  &= \cdot [
  
                                                                      \frac{n^3 \cdot \Delta x^2 }{3\,{\mathrm{\Delta x}}^3 }
                                                                    + \frac{n^2 \cdot \Delta x^2 }{2\,{\mathrm{\Delta x}}^2 }
                                                                    + \frac{n \cdot \Delta x^2 }{6\,\mathrm{\Delta x}}


                                                                            ] \Delta x  =\frac{n^3}{3} \\



\end{align*}
$$



Lets try to find pattern in sum of $n , n^2 ,n^3, n^4$


$$

\begin{align*}
\sum{n^3} = \left(\frac{n(n + 1)}{2}\right)^2 &= \left(\frac{n^2 + n}{2}\right)^2 \\
&= \frac{n^4 + 2n^3 + n^2}{4}. \\

& = \frac{n^4 }{4}+\frac{n^3 }{2}+\frac{n^2 }{4}
\end{align*}
$$

Ops, i found these formulas on <a link="https://en.wikipedia.org/wiki/Faulhaber's_formula">https://en.wikipedia.org/wiki/Faulhaber's_formula</a>

$$



\begin{array}{c}
\displaystyle
\begin{aligned}
\sum_{k=1}^{n}k^{0} &= \frac{1}{1} n \\
\sum_{k=1}^{n}k^{1} &= \frac{1}{2} \left(n^2 + \frac{2}{2}n\right) \\
\sum_{k=1}^{n}k^{2} &= \frac{1}{3} \left(n^3 + \frac{3}{2}n^2 + \frac{3}{6}n\right) \\
\sum_{k=1}^{n}k^{3} &= \frac{1}{4} \left(n^4 + \frac{4}{2}n^3 + \frac{6}{6}n^2 + 0n\right) \\
\sum_{k=1}^{n}k^{4} &= \frac{1}{5} \left(n^5 + \frac{5}{2}n^4 + \frac{10}{6}n^3 + 0n^2 - \frac{5}{30}n\right) \\
\sum_{k=1}^{n}k^{5} &= \frac{1}{6} \left(n^6 + \frac{6}{2}n^5 + \frac{15}{6}n^4 + 0n^3 - \frac{15}{30}n^2 + 0n\right) \\
\sum_{k=1}^{n}k^{6} &= \frac{1}{7} \left(n^7 + \frac{7}{2}n^6 + \frac{21}{6}n^5 + 0n^4 - \frac{35}{30}n^3 + 0n^2 + \frac{7}{42}n\right).
\end{aligned}
\end{array}

$$



It appears that as we delve into more complex mathematical operations involving higher powers, humans may struggle to compute them from first principles. In light of this, it seems prudent to consider the Fundamental Theorem of Calculus.








# Fundamental Theorm of Calculus

We want to show that:

$\int_{0}^{N} f(x) \, dx = F(N) - F(0)$

Now, using the provided formula:

$\int_{0}^{N} f(x) \, dx = \lim_{{\Delta x \to 0}} \sum_{i=0}^{N/\Delta x} f(i \cdot \Delta x) \cdot \Delta x$

Let's rewrite the right-hand side of the equation:

$\lim_{{\Delta x \to 0}} \sum_{i=0}^{N/\Delta x} F'(i \cdot \Delta x) \cdot \Delta x$

Now, we'll use the definition of the derivative to rewrite $F'(i \cdot \Delta x)$:

$F'(i \cdot \Delta x) = \frac{F(i \cdot \Delta x + \Delta x) - F(i \cdot \Delta x)}{\Delta x}$

Substitute this back into the equation:

$\lim_{{\Delta x \to 0}} \sum_{i=0}^{N/\Delta x} \frac{F(i \cdot \Delta x + \Delta x) - F(i \cdot \Delta x)}{\Delta x} \cdot \Delta x$

Now, notice that $\Delta x$ cancels out in each term of the sum:

$\lim_{{\Delta x \to 0}} \sum_{i=0}^{N/\Delta x} F(i \cdot \Delta x + \Delta x) - F(i \cdot \Delta x)$

We can now rewrite this as a telescoping sum:

$\lim_{{\Delta x \to 0}} \left[F(\Delta x) - F(0) + F(2\Delta x) - F(\Delta x) + \ldots + F(N) - F(N - \Delta x)\right]$

Now, many terms will cancel out:

$\lim_{{\Delta x \to 0}} \left[F(N) - F(0)\right]$

As $\Delta x$ approaches 0, the sum becomes:

$F(N) - F(0)$

Therefore, we have proved that:

$\int_{0}^{N} f(x) \, dx = F(N) - F(0)$

This completes the proof of the Fundamental Theorem of Calculus.


$$


$$

## Alternative Proof

Consider,
$$
\begin{aligned}

f(x +  \Delta x) - f(x)  &=    

                                        f_{A_1} (\Delta x) +f_{A_3} (\Delta x)^2 + f_{A_4} (\Delta x)^3 + \ldots   \\
f(x +  2 \Delta x) - f(x + \Delta x) &= 

                                        f_{A_1} (2 \cdot \Delta x) +f_{A_3} (2 \cdot \Delta x)^2 + f_{A_4} (2 \cdot \Delta x)^3 + \ldots  \\
f(x +  3 \Delta x) - f(x + 2 \Delta x)  &= 

                                          f_{A_1} (3 \cdot \Delta x) +f_{A_3} (3 \cdot \Delta x)^2 + f_{A_4} (3 \cdot \Delta x)^3 + \ldots \\
f(x +  4 \Delta x) - f(x + 3 \Delta x)  &=

                                             f_{A_1} (4 \cdot\ \Delta x) +f_{A_3} (4 \cdot\ \Delta x)^2 + f_{A_4} (4 \cdot\  \Delta x)^3 + \ldots \\
f(x +  5 \Delta x) - f(x + 4 \Delta x)  &= 
                                              f_{A_1} (5 \cdot\ \Delta x) +f_{A_3} (5 \cdot\  \Delta x)^2 + f_{A_4} (5 \cdot\  \Delta x)^3 + \ldots \\


                              &\vdots  \\

f(x + N \cdot \Delta x) - f(x + [N -1 ] \cdot \Delta x )  &= 
                              f_{A_1}(x + [N -1 ] \cdot \Delta x )  (\Delta x) 
                              + f_{A_1}(x + [N -1 ] \cdot \Delta x )  (\Delta x)^2 
                              + f_{A_1}(x + [N -1 ] \cdot \Delta x ) (\Delta x)^3 
                              + \ldots  \\




\end{aligned}
$$

Now if we will take sum of vertically we can get the desired proof



# Difference equations for Anti Derivative


I believe it's necessary for us to compile a set of difference equations, as relying solely on retroactively analyzing equations is the only course of action available to us.


$$
\begin{aligned}
xdx &= \frac{(x + dx)^2 - x^2}{2}\\
x^2dx &= \frac{(x + dx)^3 - x^3}{3}\\
x^3dx &= \frac{(x + dx)^4 - x^4}{4}\\
x^4dx &= \frac{(x + dx)^5 - x^5}{5}\\
\end{aligned}
$$

suppose if any bigger number would be there instead of dx let say $\Delta X$ then equations would have looked like

$$
\begin{aligned}


 x\Delta X +
\frac{(\Delta X)^2}{2} &=  

                            \frac{(x + \Delta X)^2 - x^2}{2} \\ 

 x^2\Delta X
+ x(\Delta X)^2 +\frac{ (\Delta X)^3 }{3} &= 
                                                \frac{(x + \Delta X)^3 - x^3}{3}  \\


 x^3\Delta x
+ \frac{ 3x^2(\Delta x)^2}{2} + x(\Delta x)^3 + \frac{(\Delta x)^4}{2} &= 
                                                                            \frac{(x + \Delta X)^4 - x^4}{4}  \\




\end{aligned}


$$



### $\int \cos(x) \, dx = \sin(x) + C$

$$
\begin{aligned}

\int_{0}^{\pi} \cos(x) dx &= \sum_{i = 0}^{n / \Delta x} \cos(i \cdot \Delta x) \cdot \Delta x  \\
                          &=  \\
                        
\because sin ⁡ \left(\right. x + \Delta x \left.\right) &= sin ⁡ \left(\right. x \left.\right) cos ⁡ \left(\right. \Delta x \left.\right) + cos ⁡ \left(\right. x \left.\right) sin ⁡ \left(\right. \Delta x \left.\right) \\ 

&\approx sin ⁡ \left(\right. x \left.\right) + cos ⁡ \left(\right. x \left.\right) \Delta x  \\


\therefore \cos(x) \Delta x &= \sin(x + \Delta x) - \sin (x)  \\


\int_{0}^{\pi} \cos(x) \, dx &= \sum_{i = 0}^{n / \Delta x} \cos(i \cdot \Delta x) \cdot \Delta x  \\

                              &= \sum_{i = 0}^{n / \Delta x} (\sin(i \cdot \Delta x + \Delta x) - \sin(i \cdot \Delta x)) \cdot \Delta x    \\  

                            \because \text{This is a telescopic series}  \\
                            
                             &= \sin(n)     


\end{aligned}


$$

We now know that we need to know prior that what could be the solution for the telescoping series for the given summation problem

Note :  
if $\Delta x$ would not be infinitely small , Lets say any bigger number $\Delta X$ then, 

$$
\begin{aligned}

\because sin ⁡ \left(\right. x + \Delta X \left.\right) &= sin ⁡ \left(\right. x \left.\right) cos ⁡ \left(\right. \Delta X \left.\right) + cos ⁡ \left(\right. x \left.\right) sin ⁡ \left(\right. \Delta X \left.\right) \\ 


\end{aligned}
$$


Instead of 

$$

\cos(x) \Delta x = \sin(x + \Delta x) - \sin (x) 

$$

We get 
$$

\sin(x + \Delta X) = \sin(x) \cos(\Delta X) + \cos(x) \sin(\Delta X) \\ 

\sin(x + \Delta X) - \sin(x) \cos(\Delta X) = \cos(x) \sin(\Delta X) \\

\therefore \cos(x) \sin(\Delta X)  =  \sin(x + \Delta X) - \sin(x) \cos(\Delta X) 


$$

From here we can see that we are not actually taking,

$$
\begin{aligned}
\int_{0}^{\pi} \cos(x) dx &= \sum_{i = 0}^{n / \Delta x} \cos(i \cdot \Delta x) \cdot \Delta x  \\
                          &= \sum_{i = 0}^{n / \Delta x} \cos(i \cdot \Delta X) \cdot \sin(\Delta X) \\
                          &= \sum_{i = 0}^{n / \Delta x} \sin(x + \Delta X) - \sin(x) \cos(\Delta X) 

\end{aligned}
$$







### $\int \sin(x) \, dx = \cos(x) + C$


$$
\begin{aligned}
\int_{0}^{\pi} \sin(x) \, dx &= \sum_{i = 0}^{n} \sin(i \cdot \Delta x) \cdot \Delta x  \\



\because cos ⁡ \left(\right. x + \Delta x \left.\right) 

&= cos ⁡ \left(\right. x \left.\right) cos ⁡ \left(\right. \Delta x \left.\right) - sin ⁡ \left(\right. x \left.\right) sin ⁡ \left(\right. \Delta x \left.\right)  \\


cos ⁡ \left(\right. x + \Delta x \left.\right)  &\approx cos ⁡ \left(\right. x \left.\right) - sin ⁡ \left(\right. x \left.\right) \Delta x \\

\therefore   \sin(x) \Delta x &= -[\cos(x + \Delta x) - \cos(x)]   \\



                              &= -1 \cdot [\sum_{i = 0}^{n/\Delta x} (\cos((i + 1) \cdot \Delta x) - \cos(i \cdot \Delta x)) \cdot \Delta x ]\\

       \because \text{This is a telescopic series}  \\
                              &= - \cos(n)




\end{aligned}

$$


### $\int \frac{1}{x} \, dx = \ln(|x|) + C$

We know from previous work,

$$

\begin{align*}


\log(x + h) &= \log(x) +
\log(((1+\frac{h}{x})^\frac{x}{h})^\frac{h}{x} ) \\
            & = \log(x) + \log((e)^\frac{h}{x} ) \\
            &= \log(x) + \frac{h}{x}
\end{align*}
$$

which tells us, 
$$
\frac{h}{x} = \log(x+h) - \log(x)

$$

And putting this into our summation formula we can proof $\int \frac{1}{x} \, dx = \ln(|x|) + C$


## Integration by parts


Intergration 


$$
\int u \, dv = uv - \int v \, du


$$


$$

\int f(x) \, g'(x) \, dx = f(x) \, g(x) - \int g(x) \, f'(x) \, dx
$$


$$
\int f(x) \, g(x) \, dx = f(x) \, G(x) - \int f'(x) \, G(x) \, dx
$$



### Proof

Certainly! The integration by parts formula is derived from the product rule for differentiation. It states:

$$
\int u \, dv = uv - \int v \, du
$$

where:

- $u$ is a differentiable function of $x$.
- $dv$ is a differentiable function of $x$ (often chosen as $dv/dx$ or $dx$ itself).
- $du$ is the derivative of $u$ with respect to $x$.
- $v$ is the integral of $dv$ with respect to $x$.

Here's a proof of the integration by parts formula using the fundamental theorem of calculus:

We start with the product rule for differentiation:

$$
(uv)' = u \, dv + v \, du
$$

Now, let's integrate both sides with respect to $x$ from $a$ to $b$:

$$
\int_{a}^{b} (u \, dv + v \, du) \, dx = \int_{a}^{b} (uv)' \, dx
$$

By the fundamental theorem of calculus, the left side becomes:

$$
\int_{a}^{b} u \, dv \, dx + \int_{a}^{b} v \, du \, dx = [uv]_{a}^{b}
$$

where $[uv]_{a}^{b}$ represents the evaluation of $uv$ at the upper and lower limits of integration.

So, we have:

$$
\int_{a}^{b} u \, dv \, dx + \int_{a}^{b} v \, du \, dx = uv(b) - uv(a)
$$

Now, we can isolate the integral of $u \, dv$ on one side:

$$
\int_{a}^{b} u \, dv \, dx = uv(b) - uv(a) - \int_{a}^{b} v \, du \, dx
$$

Finally, if we take the limit as $a$ approaches negative infinity and $b$ approaches positive infinity (assuming the integrals converge), we get the standard integration by parts formula:

$$
\int u \, dv = uv - \int v \, du
$$

This completes the proof of the integration by parts formula.


## Alternative Proof  Work


$$

f(x +  \Delta x) = A_0 + A_1 (\Delta x) +
A_3 (\Delta x)^2 + A_4 (\Delta x)^3 + \ldots + A_{n+1} (\Delta
x)^n\\


G(x +  \Delta x) = B_0 + B_1 (\Delta x) +
B_3 (\Delta x)^2 + B_4 (\Delta x)^3 + \ldots + B_{n+1} (\Delta
x)^n
$$


$$

G(x +  \Delta x) = G(x) + g(x) (\Delta x) +
B_3 (\Delta x)^2 + B_4 (\Delta x)^3 + \ldots + B_{n+1} (\Delta
x)^n
$$


From the formula,

$$

\int_{0}^{N} f(x) \, dx = \lim_{{\Delta x \to 0}} \sum_{i=0}^{n/\Delta x} f(i \cdot \Delta x) \cdot \Delta x
$$

Here
$$
\begin{align*}
\int f(x) \, g(x) \, dx &= \lim_{{\Delta x \to 0}} \sum_{i=0}^{n/\Delta x} f(i \cdot \Delta x) \cdot g(i \cdot \Delta x) \cdot \Delta x \\

                        &=   \left[ \sum_{i=0}^{\frac{n}{\Delta x}} \left( f(i \cdot \Delta x) - f((i-1) \cdot \Delta x) \right) \right] \cdot 

                  \sum_{i=0}^{n/\Delta x}  g(i \cdot \Delta x)

                 \,  -  \, 

                   \sum_{i=0}^{n/\Delta x} \left[ A_1 \cdot \sum_{i=0}^{\frac{n}{\Delta x}} g(i \cdot \Delta x) \right]


\end{align*}

$$


I guess this is getting complex but surely if we work we can see through it, but you can go to previous proof and visualize expansion every time they talk about differentiation. We can easily work to this proof with that technique.

















