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


f(a + 2h) &= A_0 +{\left(2\,h\right)}\,A_1 +{\left(4\,h^2 \right)}\,A_2 +{\left(8\,h^3 \right)}\,A_3 +{\left(16\,h^4 \right)}\,A_4 +{\left(32\,h^5 \right)}\,A_5 +{\left(64\,h^6 \right)}\,A_6   \\

f(a + 3h) &= A_0 +{\left(3\,h\right)}\,A_1 +{\left(9\,h^2 \right)}\,A_2 +{\left(27\,h^3 \right)}\,A_3 +{\left(81\,h^4 \right)}\,A_4 +{\left(243\,h^5 \right)}\,A_5 +{\left(729\,h^6 \right)}\,A_6   \\


f(a + 4h) &= A_0 +{\left(4\,h\right)}\,A_1 +{\left(16\,h^2 \right)}\,A_2 +{\left(64\,h^3 \right)}\,A_3 +{\left(256\,h^4 \right)}\,A_4 +{\left(1024\,h^5 \right)}\,A_5 +{\left(4096\,h^6 \right)}\,A_6  \\

f(a + 5h) &= A_0 +{\left(5\,h\right)}\,A_1 +{\left(25\,h^2 \right)}\,A_2 +{\left(125\,h^3 \right)}\,A_3 +{\left(625\,h^4 \right)}\,A_4 +{\left(3125\,h^5 \right)}\,A_5 +{\left(15625\,h^6 \right)}\,A_6 

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

   f\left(a\right)-2\,f\left(a+h\right)+f\left(a+2\,h\right) &=  0 + 0 + 2\,A_2 +{\left(6\,h\right)}\,A_3 +{\left(14\,h^2 \right)}\,A_4 +{\left(30\,h^3 \right)}\,A_5 +{\left(62\,h^4 \right)}\,A_6 + ldots \\ \\

    f''(a) = \frac{f\left(a\right)-2\,f\left(a+h\right)+f\left(a+2\,h\right)}{h^2 } &= 2\,A_2 +{\left(6\,h\right)}\,A_3 +{\left(14\,h^2 \right)}\,A_4 +{\left(30\,h^3 \right)}\,A_5 +{\left(62\,h^4 \right)}\,A_6 \\\\\\

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

