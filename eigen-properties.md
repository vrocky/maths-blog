
# Eigenvalues and Properties

## Introduction

Eigenvalues and eigenvectors are fundamental concepts in linear algebra. They play a crucial role in various mathematical and engineering applications. In this document, we will explore the concept of eigenvalues, their properties, and provide a proof for one of these properties.

## Eigenvalues and Eigenvectors

Eigenvalues (λ) and eigenvectors (v) are related to square matrices (A) by the equation:

A *v = λ* v

Where:

- A is a square matrix
- v is a nonzero vector
- λ is a scalar (the eigenvalue)

Eigenvalues represent the scaling factors by which the eigenvectors are stretched or compressed when multiplied by the matrix A.

## Properties of Eigenvalues

1. Sum of eigenvalues equals the trace:
If A is a square matrix with eigenvalues λ₁, λ₂, ..., λₙ, then:
Trace(A) = λ₁ + λ₂ + ... + λₙ

2. Product of eigenvalues equals the determinant:
If A is a square matrix with eigenvalues λ₁, λ₂, ..., λₙ, then:
det(A) = λ₁ *λ₂* ... * λₙ

3. Eigenvalues of a triangular matrix:
For an upper triangular or lower triangular matrix, the eigenvalues are the diagonal elements.

4. Eigenvalues of a scalar multiple of a matrix:
If A is a matrix with eigenvalues λ₁, λ₂, ..., λₙ, and k is a scalar, then the eigenvalues of kA are kλ₁, kλ₂, ..., kλₙ.

5. Eigenvalues of the inverse of a matrix:
If A is a square matrix with eigenvalues λ₁, λ₂, ..., λₙ, and A⁻¹ exists, then the eigenvalues of A⁻¹ are 1/λ₁, 1/λ₂, ..., 1/λₙ.

6. Eigenvalues of matrix powers:
If A is a square matrix with eigenvalues λ₁, λ₂, ..., λₙ, then the eigenvalues of A raised to a positive integer power k (A^k) are λ₁^k, λ₂^k, ..., λₙ^k.

## Proof of Property 1 2 3

To work on our proof lets do our analysis around characterstic equation.

 To find the characteristic equation of a matrix, we use the formula $\text{det}(A - \lambda I) = 0$, where $A$ is the matrix, $\lambda$ is an eigenvalue, and $I$ is the identity matrix. For the matrix $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the characteristic equation is found by calculating the determinant of $A - \lambda I$, which is:

$$
\text{det}\left( \begin{pmatrix} a & b \\ c & d \end{pmatrix} - \begin{pmatrix} \lambda & 0 \\ 0 & \lambda \end{pmatrix} \right) = 0
$$

This simplifies to:

$$
\text{det}\left( \begin{pmatrix} a - \lambda & b \\ c & d - \lambda \end{pmatrix} \right) = 0
$$

The determinant of this 2x2 matrix is:

$$
(a - \lambda)(d - \lambda) - bc = 0
$$

Expanding this, we get the characteristic equation:

$$
\lambda^2 - (a + d)\lambda + (ad - bc) = 0
$$

This is the characteristic equation for the given matrix.

Lets there be general euqation of  $Ax^2 + Bx + C$

and suppose $\lambda_1$ and $\lambda_2$ are roots of a equation

$$
\begin{align*}
(x - \lambda_1)(x - \lambda_2) &= x^2 - (\lambda_2 + \lambda_1)x + \lambda_1\lambda_2 \\
Ax^2 + Bx + C &= x^2 - (\lambda_2 + \lambda_1)x + \lambda_1\lambda_2
\end{align*}

$$

so now we can clearly say that  $\lambda_1$ and $\lambda_2$ are sum of dialognal elements

if you got the hint what we are trying to analyse with this pattern lets go deeper

## generalized characteristic equation

The generalized characteristic equation for an $n \times n$ matrix $A$ can be derived from the determinant of the matrix $A - \lambda I$, where $\lambda$ is a scalar and $I$ is the $n \times n$ identity matrix. The characteristic polynomial $P(\lambda)$ is obtained by computing the determinant of $A - \lambda I$, and the characteristic equation is set by equating this polynomial to zero:

$P(\lambda) = \det(A - \lambda I) = 0$

For an $n \times n$ matrix, the characteristic polynomial will be a polynomial of degree $n$ in $\lambda$. The general form of the characteristic polynomial for a 2x2, 3x3, ... nxn matrix can be expressed as follows:

<h3>For a 2x2 matrix:</h3>

Let $ A = \begin{bmatrix} a & b \\ c & d \end{bmatrix} $ , then
$P(\lambda) = \det(A - \lambda I) = \det \begin{bmatrix} a-\lambda & b \\ c & d-\lambda \end{bmatrix} = (a-\lambda)(d-\lambda) - bc = \lambda^2 - (a + d)\lambda + (ad - bc)$

<h3>For a 3x3 matrix:</h3>

Let $A = \begin{bmatrix} a & b & c \\ d & e & f \\ g & h & i \end{bmatrix}$, then
$P(\lambda) = \det(A - \lambda I) = \lambda^3 - (a + e + i)\lambda^2 + (ae + ei + ai - bf - cg - dh)\lambda - (aei + bfg + cdh - afh - bdi - ceg)$

<h3>For an nxn matrix:</h3>

$$
p(\lambda) = \det(A - \lambda I) =
\begin{vmatrix}
a_{11} - \lambda & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} - \lambda & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{n1} & a_{n2} & \cdots & a_{nn} - \lambda
\end{vmatrix} =
(-1)^n \lambda^n + c_{1}\lambda^{n-1} + c_{2}\lambda^{n-2} + \cdots + c_{n-1}\lambda + c_n,

$$

<br>

The characteristic polynomial will be of the form:
$P(\lambda) = (-1)^n \lambda^n + c_{n-1}\lambda^{n-1} + c_{n-2}\lambda^{n-2} + ... + c_2\lambda^2 + c_1\lambda + c_0$

Where:

- $c_{n-1}$, $c_{n-2}$, ..., $c_1$, $c_0$ are coefficients that are functions of the entries of the matrix $A$. These coefficients are determined by the sums of products of the entries of $A$, following specific patterns related to permutations of matrix entries and their sign, according to the Leibniz formula for determinants.

The roots of the characteristic polynomial $P(\lambda)$ are the eigenvalues of the matrix $A$. Each eigenvalue may correspond to one or more eigenvectors, and the set of all eigenvectors associated with an eigenvalue, along with the zero vector, forms the eigenspace for that eigenvalue.

### Determinant

Lets recall our work with determinant formula
$$
\begin{equation}
\det(A) = \sum_{i=1}^{n} (-1)^{i+j} \cdot a_{ij} \cdot M_{ij}
\end{equation}
$$

$$
\begin{vmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{vmatrix} =
\sum_{i=1}^{n} (-1)^{i+j} \cdot a_{ij} \cdot
\begin{vmatrix}
a_{11} & \cdots & a_{1(j-1)} & a_{1(j+1)} & \cdots & a_{1n} \\
a_{21} & \cdots & a_{2(j-1)} & a_{2(j+1)} & \cdots & a_{2n} \\
\vdots & \ddots & \vdots & \vdots & \ddots & \vdots \\
a_{(i-1)1} & \cdots & a_{(i-1)(j-1)} & a_{(i-1)(j+1)} & \cdots & a_{(i-1)n} \\
a_{(i+1)1} & \cdots & a_{(i+1)(j-1)} & a_{(i+1)(j+1)} & \cdots & a_{(i+1)n} \\
\vdots & \ddots & \vdots & \vdots & \ddots & \vdots \\
a_{n1} & \cdots & a_{n(j-1)} & a_{n(j+1)} & \cdots & a_{nn}
\end{vmatrix}
$$

$$

\det(A) = \sum_{\tau \in S_{n}} \operatorname{sgn}(\tau) \cdot \prod_{i=1}^{n} a_{i,\tau(i)} = \sum_{\sigma \in S_{n}} \operatorname{sgn}(\sigma) \cdot \prod_{i=1}^{n} a_{\sigma(i),i}

$$

The Leibniz formula for the determinant of an $n \times n$ matrix $A$ can be represented using LaTeX as follows:

$\det(A) = \sum_{\tau \in S_{n}} \operatorname{sgn}(\tau) \prod_{i=1}^{n} a_{i,\tau(i)} = \sum_{\sigma \in S_{n}} \operatorname{sgn}(\sigma) \prod_{i=1}^{n} a_{\sigma(i),i}$

Here's a breakdown of this formula:

- $\det(A)$ represents the determinant of the matrix $A$.
- The sums run over all permutations $\tau$ and $\sigma$ in the symmetric group $S_n$, which consists of all possible permutations of the set $\{1, 2, \ldots, n\}$.
- $\operatorname{sgn}(\tau)$ and $\operatorname{sgn}(\sigma)$ denote the sign of the permutations $\tau$ and $\sigma$, respectively. This sign is $+1$ for an even permutation and $-1$ for an odd permutation.
- $\prod_{i=1}^{n} a_{i,\tau(i)}$ and $\prod_{i=1}^{n} a_{\sigma(i),i}$ represent the product of matrix elements for each permutation. In each product, $a_{ij}$ is the element of $A$ in the $i$-th row and $j$-th column.

This formula elegantly captures the determinant of a matrix as a sum over all permutations of the product of elements chosen according to the permutation, each weighted by the sign of the permutation.
<br>
<br>

$$
\begin{array}{c} A = \begin{bmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33} \\
\end{bmatrix} \end{array}
$$
$\text{det}(A) = a_{11}a_{22}a_{33} - a_{11}a_{23}a_{32} - a_{12}a_{21}a_{33} + a_{12}a_{23}a_{31} + a_{13}a_{21}a_{32} - a_{13}a_{22}a_{31}$
<br>
<br>
<br>

$$
A = \begin{bmatrix}
a_{11} & a_{12} & a_{13} & a_{14} \\
a_{21} & a_{22} & a_{23} & a_{24} \\
a_{31} & a_{32} & a_{33} & a_{34} \\
a_{41} & a_{42} & a_{43} & a_{44} \\
\end{bmatrix}
$$
$$
\begin{array}{c} \text{det}(A) = a_{11}a_{22}a_{33}a_{44} - a_{11}a_{22}a_{34}a_{43} - a_{11}a_{23}a_{32}a_{44} + a_{11}a_{23}a_{34}a_{42} + a_{11}a_{24}a_{32}a_{43} - a_{11}a_{24}a_{33}a_{42} \\
- a_{12}a_{21}a_{33}a_{44} + a_{12}a_{21}a_{34}a_{43} + a_{12}a_{23}a_{31}a_{44} - a_{12}a_{23}a_{34}a_{41} - a_{12}a_{24}a_{31}a_{43} + a_{12}a_{24}a_{33}a_{41} \\
- a_{13}a_{21}a_{32}a_{44} - a_{13}a_{21}a_{34}a_{42} - a_{13}a_{22}a_{31}a_{44} + a_{13}a_{22}a_{34}a_{41} + a_{13}a_{24}a_{31}a_{42} - a_{13}a_{24}a_{32}a_{41} \\
- a_{14}a_{21}a_{32}a_{43} + a_{14}a_{21}a_{33}a_{42} + a_{14}a_{22}a_{31}a_{43} - a_{14}a_{22}a_{33}a_{41} - a_{14}a_{23}a_{31}a_{42} + a_{14}a_{23}a_{32}a_{41} \end{array}

$$

Substituting the values for each permutation, you can calculate the determinant of the 3x3 matrix \(A\) using Leibniz's formula.

back to pattern analysis

$$ \begin{align*}
(x - \lambda_1)(x - \lambda_2) &= x^2 - (\lambda_2 + \lambda_1)x + \lambda_1\lambda_2 \\
\end{align*} $$

<br>

$$
(x - \lambda_1)(x - \lambda_2)(x - \lambda_3) = x^3 - (\lambda_1 + \lambda_2 + \lambda_3)x^2 + (\lambda_1\lambda_2 + \lambda_2\lambda_3 + \lambda_1\lambda_3)x - \lambda_1\lambda_2\lambda_3
$$

<br>

$$
\begin{align*}
&(x - \lambda_1)(x - \lambda_2)(x - \lambda_3)(x - \lambda_4) \\
&= x^4 - (\lambda_1 + \lambda_2 + \lambda_3 + \lambda_4)x^3 + (\lambda_1\lambda_2 + \lambda_1\lambda_3 + \lambda_1\lambda_4 + \lambda_2\lambda_3 + \lambda_2\lambda_4 + \lambda_3\lambda_4)x^2 \\
&\quad - (\lambda_1\lambda_2\lambda_3 + \lambda_1\lambda_2\lambda_4 + \lambda_1\lambda_3\lambda_4 + \lambda_2\lambda_3\lambda_4)x + \lambda_1\lambda_2\lambda_3\lambda_4
\end{align*}
$$

the characteristic equations for 2x2, 3x3, 4x4, and 5x5 matrices in the form you provided:

1. For a 2x2 matrix:

$$
\begin{array}{c} \text{det}\left( \begin{pmatrix} a & b \\ c & d \end{pmatrix} - \begin{pmatrix} \lambda & 0 \\ 0 & \lambda \end{pmatrix} \right) = 0 \end{array}
$$
$$
\lambda^2 - (a + d)\lambda + (ad - bc) = 0
$$

2. For a 3x3 matrix:

    $$
    \begin{array}{c} \text{det}\left( \begin{pmatrix} a & b & c & d \\ e & f & g & h \\ i & j & k & l \\ m & n & o & p \end{pmatrix} - \begin{pmatrix} \lambda & 0 & 0 & 0 \\ 0 & \lambda & 0 & 0 \\ 0 & 0 & \lambda & 0 \\ 0 & 0 & 0 & \lambda \end{pmatrix} \right) = 0 \end{array}
    $$

    $\lambda^3 - (a + e + i)\lambda^2 + (ae + ai + ei - fh - fi - gh)\lambda - (aei + bfg + cdh - ceg - bdi - afh) = 0$

3. For a 4x4 matrix:

    $$
    \begin{array}{c} \text{det}\left( \begin{pmatrix} a & b & c & d \\ e & f & g & h \\ i & j & k & l \\ m & n & o & p \end{pmatrix} - \begin{pmatrix} \lambda & 0 & 0 & 0 \\ 0 & \lambda & 0 & 0 \\ 0 & 0 & \lambda & 0 \\ 0 & 0 & 0 & \lambda \end{pmatrix} \right) = 0 \end{array}
    $$

    $$

        \lambda^4 - (a + f + k + p)\lambda^3 \\+ (af + ak + ap + fk + fp + kp - bce - bcf - bck - bde - bdf - bdp - ceh - cek - cep - dfh - dfk - dfp - ghi - ghk - ghp - jli - jlk - jlp - moi - mok - mop)\lambda^2 \\- (afk + afp + akp + fkp + bcef + bcek + bcep + bdef + bdek + bdep + cefk + cefp + cekp + defk + defp + dekp + efgh + efij + efik + efkl + efkp + fgij + fgik + fgil + fgkl + fgkp + ghij + ghik + ghil + ghkl + jlik + jlip + jlkp + jlmp + mokp)\lambda + \\ \\ (afkp + bcefk + bcefp + bcekp + bdefk + bdefp + bdekp + cefkp + defkp + efghk + efghp + efijp + efikp + efklp + fgijp + fgikp + fgklp + ghijp + ghikp + ghklp + jlikp + mokp) = 0

    $$

There are some results we want to reach are the characteristic equations for 2x2, 3x3, 4x4, and 5x5 matrices in the form you mentioned:

- For a 2x2 matrix A, the characteristic equation is:

    $\lambda^2 - \text{Tr}(A) \lambda + \text{det}(A) = 0$

- For a 3x3 matrix A, the characteristic equation is:

    $\lambda^3 - \text{Tr}(A) \lambda^2 + \left(\frac{1}{2}[\text{Tr}(A)^2 - \text{Tr}(A^2)]\right) \lambda - \text{det}(A) = 0$

- For a 4x4 matrix A, the characteristic equation is more complex, but it follows the same pattern:

    $\lambda^4 - \text{Tr}(A) \lambda^3 + \left(\frac{1}{2}[\text{Tr}(A)^2 - \text{Tr}(A^2)]\right) \lambda^2 - \left(\frac{1}{6}[\text{Tr}(A)^3 - 3\text{Tr}(A)\text{Tr}(A^2) + 2\text{Tr}(A^3)]\right) \lambda + \text{det}(A) = 0$

- For a 5x5 matrix A, the characteristic equation is also more complex:

    $\lambda^5 - \text{Tr}(A) \lambda^4 + \left(\frac{1}{2}[\text{Tr}(A)^2 - \text{Tr}(A^2)]\right) \lambda^3 - \left(\frac{1}{6}[\text{Tr}(A)^3 - 3\text{Tr}(A)\text{Tr}(A^2) + 2\text{Tr}(A^3)]\right) \lambda^2 + \left(\frac{1}{24}[\text{Tr}(A)^4 - 6\text{Tr}(A)^2\text{Tr}(A^2) + 8\text{Tr}(A)\text{Tr}(A^3) + 3\text{Tr}(A^2)^2 - 6\text{Tr}(A^4)]\right) \lambda - \text{det}(A) = 0$

- The characteristic equation for a 6x6 matrix A can be expressed as follows:
    $$
    \lambda^6 - \text{Tr}(A) \lambda^5 + \left(\frac{1}{2}[\text{Tr}(A)^2 - \text{Tr}(A^2)]\right) \lambda^4 - \left(\frac{1}{6}[\text{Tr}(A)^3 - 3\text{Tr}(A)\text{Tr}(A^2) + 2\text{Tr}(A^3)]\right) \lambda^3 + \left(\frac{1}{24}[\text{Tr}(A)^4 - 6\text{Tr}(A)^2\text{Tr}(A^2) + 8\text{Tr}(A)\text{Tr}(A^3) + 3\text{Tr}(A^2)^2 - 6\text{Tr}(A^4)]\right) \lambda^2 - \left(\frac{1}{120}[\text{Tr}(A)^5 - 10\text{Tr}(A)^3\text{Tr}(A^2) + 20\text{Tr}(A)^2\text{Tr}(A^3) + 30\text{Tr}(A)\text{Tr}(A^2)^2 - 60\text{Tr}(A^3)^2 + 120\text{Tr}(A^5)]\right) \lambda + \text{det}(A) = 0

    $$

These equations can be used to find the eigenvalues of matrices of the respective sizes.

Let

$$

A - \lambda I = \begin{pmatrix} a - \lambda & b & c \\ d & e - \lambda & f \\ g & h & i - \lambda \end{pmatrix}

$$

$$
 \text{det}(A) = a_{11}a_{22}a_{33} - a_{11}a_{23}a_{32} - a_{12}a_{21}a_{33} + a_{12}a_{23}a_{31} + a_{13}a_{21}a_{32} - a_{13}a_{22}a_{31}

$$

So
$$
\begin{align*}
\text{det}(A - \lambda I) &= (a-\lambda)(e-\lambda)(i-\lambda) + bdf + cgh - c(e-\lambda)d - b(g)(i-\lambda) - (a-\lambda)hf \\
&= (a-\lambda)(e-\lambda)(i-\lambda) + bdf + cgh - ced + \lambda cd - big + \lambda bg - ahi + \lambda hf
\end{align*}
$$

Let, $P_n$ denotes the number of terms with $-\lambda$ in our row permutation terms from leibniz formula for determinants

$P_3 = (a-\lambda)(e-\lambda)(i-\lambda)  \\$

$P_2 = NIL \\$

$P_1 = - c(e-\lambda)d - b(g)(i-\lambda) - (a-\lambda)hf  \\$

$P_0 =   bdf + cgh\\$

Here
$$
P_3 = (a - λ)(e - λ)(i - λ) = -\lambda^3 + (a + e + i)\lambda^2 - (ae + ai + ei)\lambda + aei
$$

$$
P_1 = (a - \lambda)cf + bd(i - \lambda) + (e - \lambda)cg + bh(a - \lambda)  =  \lambda(-cf - bd - cg - bh) + acf + bdi + ecg + bha
$$

So,

$$
 \text{det}(A - \lambda I) =  -a b h - a c f + a e i - a e \lambda - a i \lambda + a \lambda^2 - b d i + b d \lambda + b f g + b h \lambda + c d h - c e g + c f \lambda + c g \lambda - e i \lambda + e \lambda^2 + i \lambda^2 - \lambda^3
$$

$$

\text{det}(A - \lambda I) = \text{= }-c e g+b f g+c d h-a f h-b d i+a e i+b d \lambda -a e \lambda +c g \lambda +f h \lambda -a i \lambda -e i \lambda +a \lambda ^2+e \lambda ^2+i \lambda ^2-\lambda ^3
$$
$$

\text{det}(A - \lambda I) = -c e g + b f g + c d h - a f h - b d i + a e i + (b d + c g + f h - e i - a (e + i)) \lambda + (a + e + i) \lambda^2 - \lambda^3

$$

Lets do this again with 4x4 Matrix

$$A  = \left(\begin{array}{cccc}
a & b & c & d\\
e & f & g & h\\
i & j & k & l\\
m & n & o & p
\end{array}\right)$$

$\text{det}(A) =  a\,f\,k\,p-a\,f\,l\,o-a\,g\,j\,p+a\,g\,l\,n+a\,h\,j\,o-a\,h\,k\,n-b\,e\,k\,p+b\,e\,l\,o+b\,g\,i\,p-b\,g\,l\,m-b\,h\,i\,o+b\,h\,k\,m+c\,e\,j\,p-c\,e\,l\,n-c\,f\,i\,p+c\,f\,l\,m+c\,h\,i\,n-c\,h\,j\,m-d\,e\,j\,o+d\,e\,k\,n+d\,f\,i\,o-d\,f\,k\,m-d\,g\,i\,n+d\,g\,j\,m$

$$
  A - \lambda I  = \left( \begin{array}{cccc}
a-\lambda  & b & c & d\\
e & f-\lambda  & g & h\\
i & j & k-\lambda  & l\\
m & n & o & p-\lambda
\end{array}\right)

$$



$b\,e\,l\,o-b\,g\,l\,m-b\,h\,i\,o-c\,e\,l\,n+c\,h\,i\,n-c\,h\,j\,m-d\,e\,j\,o-d\,g\,i\,n+d\,g\,j\,m-b\,g\,i\,{(\lambda -p)}+b\,h\,m\,{(k-\lambda )}-c\,e\,j\,{(\lambda -p)}+c\,l\,m\,{(f-\lambda )}+d\,e\,n\,{(k-\lambda )}+d\,i\,o\,{(f-\lambda )}+g\,l\,n\,{(a-\lambda )}+h\,j\,o\,{(a-\lambda )}+b\,e\,{(k-\lambda )}\,{(\lambda -p)}+c\,i\,{(f-\lambda )}\,{(\lambda -p)}-d\,m\,{(f-\lambda )}\,{(k-\lambda )}+g\,j\,{(a-\lambda )}\,{(\lambda -p)}-h\,n\,{(a-\lambda )}\,{(k-\lambda )}-l\,o\,{(a-\lambda )}\,{(f-\lambda )}-{(a-\lambda )}\,{(f-\lambda )}\,{(k-\lambda )}\,{(\lambda -p)}$

Let, $P_n$ denotes the number of terms with $-\lambda$ in our row permutation terms from leibniz formula for determinants

$P_4 =-{(a-\lambda )}\,{(f-\lambda )}\,{(k-\lambda )}\,{(\lambda -p)} \\$

$P_3 = NIL  \\$

$P_2 = b\,e\,{(k-\lambda )}\,{(\lambda -p)}+c\,i\,{(f-\lambda )}\,{(\lambda -p)}-d\,m\,{(f-\lambda )}\,{(k-\lambda )}+g\,j\,{(a-\lambda )}\,{(\lambda -p)}-h\,n\,{(a-\lambda )}\,{(k-\lambda )}-l\,o\,{(a-\lambda )}\,{(f-\lambda )} \\$

here, 
$b e (k−λ)(λ−p) = -b e k p + (b e k + b e p) \lambda - b e \lambda^2$


$P_1 = -b\,g\,i\,{(\lambda -p)}+b\,h\,m\,{(k-\lambda )}-c\,e\,j\,{(\lambda -p)}+c\,l\,m\,{(f-\lambda )}+d\,e\,n\,{(k-\lambda )}+d\,i\,o\,{(f-\lambda )}+g\,l\,n\,{(a-\lambda )}+h\,j\,o\,{(a-\lambda )} \\$

$P_0 = b\,e\,l\,o-b\,g\,l\,m-b\,h\,i\,o-c\,e\,l\,n+c\,h\,i\,n-c\,h\,j\,m-d\,e\,j\,o-d\,g\,i\,n+d\,g\,j\,m-b\,g\,i\,$


Lets expand, 

$P_4 = \lambda ^3 (-a-f-k-p)+\lambda ^2 (a (f+k+p)+f (k+p)+k p)+\lambda  (-a (f (k+p)+k p)-f k p)+a f k p+\lambda ^4 
\\$

$$
    P_2 = -dm f k - (ci f + be k) p - 
 a (hn k + f lo + gj p) + (a gj + a hn + be k + hn k + dm (f + k) + 
    a lo + f lo + be p + gj p + ci (f + p)) \lambda + (-be - ci - 
    dm - gj - hn - lo) \lambda]^2
$$

$P_1 = clm f + dio f + a gln + a hjo + bhm k + den k + bgi p + 
 cej p + (-bgi - bhm - cej - clm - den - dio - gln - hjo) \lambda$


So the final answer is 
$$

\text{det} (A - \lambda I ) =  
\lambda^4 +{\left(-a-f-k-p\right)}\,\lambda^3 +{\left(a\,f-b\,e+a\,k-c\,i+a\,p-d\,m+f\,k-g\,j+f\,p-h\,n+k\,p-l\,o\right)}\,\lambda^2 +{\left(a\,g\,j-a\,f\,k+b\,e\,k-b\,g\,i-c\,e\,j+c\,f\,i-a\,f\,p+a\,h\,n+b\,e\,p-b\,h\,m-d\,e\,n+d\,f\,m-a\,k\,p+a\,l\,o+c\,i\,p-c\,l\,m-d\,i\,o+d\,k\,m-f\,k\,p+f\,l\,o+g\,j\,p-g\,l\,n-h\,j\,o+h\,k\,n\right)}\,\lambda +a\,f\,k\,p-a\,f\,l\,o-a\,g\,j\,p+a\,g\,l\,n+a\,h\,j\,o-a\,h\,k\,n-b\,e\,k\,p+b\,e\,l\,o+b\,g\,i\,p-b\,g\,l\,m-b\,h\,i\,o+b\,h\,k\,m+c\,e\,j\,p-c\,e\,l\,n-c\,f\,i\,p+c\,f\,l\,m+c\,h\,i\,n-c\,h\,j\,m-d\,e\,j\,o+d\,e\,k\,n+d\,f\,i\,o-d\,f\,k\,m-d\,g\,i\,n+d\,g\,j\,m

$$


Lets do some pattern practice 

$(x - a) (x - b) = x^2 +{(-a-b)}\,x+a\,b\\$

$(x - a) (x - b) (x - c) = x^3 +{(-a-b-c)}\,x^2 +{(ab+ca+cb)}\,x-a\,b\,c\\$

$(x - a) (x - b) (x - c) (x - d) = x^4 +{\left(-a-b-c-d\right)}\,x^3 +{\left(a\,b+d\,{\left(a+b+c\right)}+c\,{\left(a+b\right)}\right)}\,x^2 +{\left(-d\,{\left(a\,b+c\,{\left(a+b\right)}\right)}-a\,b\,c\right)}\,x+a\,b\,c\,d$


Looking at all the pattern I have seen its simple combinatrics and I have reached to the proof for Property 1 2 3 and 4,  


For 5 , the determinant of a product of two matrices holds the following property:

$A = \left(\begin{array}{ccc}
a_{1,1}  & a_{2,1}  & a_{3,1} \\
a_{1,2}  & a_{2,2}  & a_{3,2} \\
a_{1,3}  & a_{2,3}  & a_{3,3} 
\end{array}\right)$
$B = \left(\begin{array}{ccc}
b_{1,1}  & b_{2,1}  & b_{3,1} \\
b_{1,2}  & b_{2,2}  & b_{3,2} \\
b_{1,3}  & b_{2,3}  & b_{3,3} 
\end{array}\right)$

$A\, B = \left(\begin{array}{ccc}
a_{1,1}  & a_{2,1}  & a_{3,1} \\
a_{1,2}  & a_{2,2}  & a_{3,2} \\
a_{1,3}  & a_{2,3}  & a_{3,3} 
\end{array}\right)  \left(\begin{array}{ccc}
b_{1,1}  & b_{2,1}  & b_{3,1} \\
b_{1,2}  & b_{2,2}  & b_{3,2} \\
b_{1,3}  & b_{2,3}  & b_{3,3} 
\end{array}\right)$

$A\, B =\left(\begin{array}{ccc}
a_{1,1} \,b_{1,1} +a_{2,1} \,b_{1,2} +a_{3,1} \,b_{1,3}  & a_{1,1} \,b_{2,1} +a_{2,1} \,b_{2,2} +a_{3,1} \,b_{2,3}  & a_{1,1} \,b_{3,1} +a_{2,1} \,b_{3,2} +a_{3,1} \,b_{3,3} \\
a_{1,2} \,b_{1,1} +a_{2,2} \,b_{1,2} +a_{3,2} \,b_{1,3}  & a_{1,2} \,b_{2,1} +a_{2,2} \,b_{2,2} +a_{3,2} \,b_{2,3}  & a_{1,2} \,b_{3,1} +a_{2,2} \,b_{3,2} +a_{3,2} \,b_{3,3} \\
a_{1,3} \,b_{1,1} +a_{2,3} \,b_{1,2} +a_{3,3} \,b_{1,3}  & a_{1,3} \,b_{2,1} +a_{2,3} \,b_{2,2} +a_{3,3} \,b_{2,3}  & a_{1,3} \,b_{3,1} +a_{2,3} \,b_{3,2} +a_{3,3} \,b_{3,3} 
\end{array}\right)$

It is evident using combinatorics that $\text{det}(A)*\text{det}(B)$ will have same terms as $\text{det}(AB)$, but it is hard to visualize the sign of term.


$\text{det}(A)  = a_{1,1} \,a_{2,2} \,a_{3,3} -a_{1,1} \,a_{2,3} \,a_{3,2} -a_{1,2} \,a_{2,1} \,a_{3,3} +a_{1,2} \,a_{2,3} \,a_{3,1} +a_{1,3} \,a_{2,1} \,a_{3,2} -a_{1,3} \,a_{2,2} \,a_{3,1}$

$\text{det}(B)  =b_{1,1} \,b_{2,2} \,b_{3,3} -b_{1,1} \,b_{2,3} \,b_{3,2} -b_{1,2} \,b_{2,1} \,b_{3,3} +b_{1,2} \,b_{2,3} \,b_{3,1} +b_{1,3} \,b_{2,1} \,b_{3,2} -b_{1,3} \,b_{2,2} \,b_{3,1}$


$\text{det}(A\,B) = \\a_{1,1} \,a_{2,2} \,a_{3,3} \,b_{1,1} \,b_{2,2} \,b_{3,3} -a_{1,1} \,a_{2,2} \,a_{3,3} \,b_{1,1} \,b_{2,3} \,b_{3,2} -a_{1,1} \,a_{2,2} \,a_{3,3} \,b_{1,2} \,b_{2,1} \,b_{3,3} +a_{1,1} \,a_{2,2} \,a_{3,3} \,b_{1,2} \,b_{2,3} \,b_{3,1} +a_{1,1} \,a_{2,2} \,a_{3,3} \,b_{1,3} \,b_{2,1} \,b_{3,2} -a_{1,1} \,a_{2,2} \,a_{3,3} \,b_{1,3} \,b_{2,2} \,b_{3,1} -a_{1,1} \,a_{2,3} \,a_{3,2} \,b_{1,1} \,b_{2,2} \,b_{3,3} +a_{1,1} \,a_{2,3} \,a_{3,2} \,b_{1,1} \,b_{2,3} \,b_{3,2} +a_{1,1} \,a_{2,3} \,a_{3,2} \,b_{1,2} \,b_{2,1} \,b_{3,3} -a_{1,1} \,a_{2,3} \,a_{3,2} \,b_{1,2} \,b_{2,3} \,b_{3,1} -a_{1,1} \,a_{2,3} \,a_{3,2} \,b_{1,3} \,b_{2,1} \,b_{3,2} +a_{1,1} \,a_{2,3} \,a_{3,2} \,b_{1,3} \,b_{2,2} \,b_{3,1} -a_{1,2} \,a_{2,1} \,a_{3,3} \,b_{1,1} \,b_{2,2} \,b_{3,3} +a_{1,2} \,a_{2,1} \,a_{3,3} \,b_{1,1} \,b_{2,3} \,b_{3,2} +a_{1,2} \,a_{2,1} \,a_{3,3} \,b_{1,2} \,b_{2,1} \,b_{3,3} -a_{1,2} \,a_{2,1} \,a_{3,3} \,b_{1,2} \,b_{2,3} \,b_{3,1} -a_{1,2} \,a_{2,1} \,a_{3,3} \,b_{1,3} \,b_{2,1} \,b_{3,2} +a_{1,2} \,a_{2,1} \,a_{3,3} \,b_{1,3} \,b_{2,2} \,b_{3,1} +a_{1,2} \,a_{2,3} \,a_{3,1} \,b_{1,1} \,b_{2,2} \,b_{3,3} -a_{1,2} \,a_{2,3} \,a_{3,1} \,b_{1,1} \,b_{2,3} \,b_{3,2} -a_{1,2} \,a_{2,3} \,a_{3,1} \,b_{1,2} \,b_{2,1} \,b_{3,3} +a_{1,2} \,a_{2,3} \,a_{3,1} \,b_{1,2} \,b_{2,3} \,b_{3,1} +a_{1,2} \,a_{2,3} \,a_{3,1} \,b_{1,3} \,b_{2,1} \,b_{3,2} -a_{1,2} \,a_{2,3} \,a_{3,1} \,b_{1,3} \,b_{2,2} \,b_{3,1} +a_{1,3} \,a_{2,1} \,a_{3,2} \,b_{1,1} \,b_{2,2} \,b_{3,3} -a_{1,3} \,a_{2,1} \,a_{3,2} \,b_{1,1} \,b_{2,3} \,b_{3,2} -a_{1,3} \,a_{2,1} \,a_{3,2} \,b_{1,2} \,b_{2,1} \,b_{3,3} +a_{1,3} \,a_{2,1} \,a_{3,2} \,b_{1,2} \,b_{2,3} \,b_{3,1} +a_{1,3} \,a_{2,1} \,a_{3,2} \,b_{1,3} \,b_{2,1} \,b_{3,2} -a_{1,3} \,a_{2,1} \,a_{3,2} \,b_{1,3} \,b_{2,2} \,b_{3,1} -a_{1,3} \,a_{2,2} \,a_{3,1} \,b_{1,1} \,b_{2,2} \,b_{3,3} +a_{1,3} \,a_{2,2} \,a_{3,1} \,b_{1,1} \,b_{2,3} \,b_{3,2} +a_{1,3} \,a_{2,2} \,a_{3,1} \,b_{1,2} \,b_{2,1} \,b_{3,3} -a_{1,3} \,a_{2,2} \,a_{3,1} \,b_{1,2} \,b_{2,3} \,b_{3,1} -a_{1,3} \,a_{2,2} \,a_{3,1} \,b_{1,3} \,b_{2,1} \,b_{3,2} +a_{1,3} \,a_{2,2} \,a_{3,1} \,b_{1,3} \,b_{2,2} \,b_{3,1}$



$det(AB)=$

$+a_{1,1} \,a_{2,2} \,a_{3,3} \,b_{1,1} \,b_{2,2} \,b_{3,3} -a_{1,1} \,a_{2,2} \,a_{3,3} \,b_{1,1} \,b_{2,3} \,b_{3,2} -a_{1,1} \,a_{2,2} \,a_{3,3} \,b_{1,2} \,b_{2,1} \,b_{3,3} +a_{1,1} \,a_{2,2} \,a_{3,3} \,b_{1,2} \,b_{2,3} \,b_{3,1} +a_{1,1} \,a_{2,2} \,a_{3,3} \,b_{1,3} \,b_{2,1} \,b_{3,2} -a_{1,1} \,a_{2,2} \,a_{3,3} \,b_{1,3} \,b_{2,2} \,b_{3,1} \\-  a_{1,1} \,a_{2,3} \,a_{3,2} \,b_{1,1} \,b_{2,2} \,b_{3,3} +a_{1,1} \,a_{2,3} \,a_{3,2} \,b_{1,1} \,b_{2,3} \,b_{3,2} +a_{1,1} \,a_{2,3} \,a_{3,2} \,b_{1,2} \,b_{2,1} \,b_{3,3} -a_{1,1} \,a_{2,3} \,a_{3,2} \,b_{1,2} \,b_{2,3} \,b_{3,1} -a_{1,1} \,a_{2,3} \,a_{3,2} \,b_{1,3} \,b_{2,1} \,b_{3,2}  +a_{1,1} \,a_{2,3} \,a_{3,2} \,b_{1,3} \,b_{2,2} \,b_{3,1} \\-a_{1,2} \,a_{2,1} \,a_{3,3} \,b_{1,1} \,b_{2,2} \,b_{3,3} +a_{1,2} \,a_{2,1} \,a_{3,3} \,b_{1,1} \,b_{2,3} \,b_{3,2} +a_{1,2} \,a_{2,1} \,a_{3,3} \,b_{1,2} \,b_{2,1} \,b_{3,3} -a_{1,2} \,a_{2,1} \,a_{3,3} \,b_{1,2} \,b_{2,3} \,b_{3,1}  -a_{1,2} \,a_{2,1} \,a_{3,3} \,b_{1,3} \,b_{2,1} \,b_{3,2} +a_{1,2} \,a_{2,1} \,a_{3,3} \,b_{1,3} \,b_{2,2} \,b_{3,1} \\ +a_{1,2} \,a_{2,3} \,a_{3,1} \,b_{1,1} \,b_{2,2} \,b_{3,3} -a_{1,2} \,a_{2,3} \,a_{3,1} \,b_{1,1} \,b_{2,3} \,b_{3,2}  -a_{1,2} \,a_{2,3} \,a_{3,1} \,b_{1,2} \,b_{2,1} \,b_{3,3} +a_{1,2} \,a_{2,3} \,a_{3,1} \,b_{1,2} \,b_{2,3} \,b_{3,1} +a_{1,2} \,a_{2,3} \,a_{3,1} \,b_{1,3} \,b_{2,1} \,b_{3,2} -a_{1,2} \,a_{2,3} \,a_{3,1} \,b_{1,3} \,b_{2,2} \,b_{3,1} \\+a_{1,3} \,a_{2,1} \,a_{3,2} \,b_{1,1} \,b_{2,2} \,b_{3,3} -a_{1,3} \,a_{2,1} \,a_{3,2} \,b_{1,1} \,b_{2,3} \,b_{3,2}  -a_{1,3} \,a_{2,1} \,a_{3,2} \,b_{1,2} \,b_{2,1} \,b_{3,3} +a_{1,3} \,a_{2,1} \,a_{3,2} \,b_{1,2} \,b_{2,3} \,b_{3,1} +a_{1,3} \,a_{2,1} \,a_{3,2} \,b_{1,3} \,b_{2,1} \,b_{3,2} -a_{1,3} \,a_{2,1} \,a_{3,2} \,b_{1,3} \,b_{2,2} \,b_{3,1} \\-a_{1,3} \,a_{2,2} \,a_{3,1} \,b_{1,1} \,b_{2,2} \,b_{3,3} +a_{1,3} \,a_{2,2} \,a_{3,1} \,b_{1,1} \,b_{2,3} \,b_{3,2}  +a_{1,3} \,a_{2,2} \,a_{3,1} \,b_{1,2} \,b_{2,1} \,b_{3,3} -a_{1,3} \,a_{2,2} \,a_{3,1} \,b_{1,2} \,b_{2,3} \,b_{3,1} -a_{1,3} \,a_{2,2} \,a_{3,1} \,b_{1,3} \,b_{2,1} \,b_{3,2} +a_{1,3} \,a_{2,2} \,a_{3,1} \,b_{1,3} \,b_{2,2} \,b_{3,1}$




## Conclusion

Eigenvalues and eigenvectors are essential concepts in linear algebra with various applications. Understanding their properties, such as the relationship between eigenvalues and determinants, is crucial for solving problems in mathematics and science.
