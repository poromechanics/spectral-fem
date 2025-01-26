# Legendre polynomials

Jacobi polynomial with $\alpha=\beta=0$, are called the Legendre polynomials. We will denote Legendre polynomial by $P_{n}(x)$.

$$
P_{n}(x)=P_{n}^{(1/2)}(x)=P_{n}^{(0,0)}(x)
$$

The $P_{n}$ are orthogonal with respect to the following weight function.

$$
w(x)=1
$$

The support of Legendre polynomial is $\left[-1,1\right].$ Legendre polynomials are best from the point of view of minimizing the $L^{2}$ error.


## First few Legendre polynomials

The first five legendre polynomials are given below.

$$
P_{0}=x^{0}
$$

$$
P_{1}=x
$$

$$
P_{2}=\frac{3}{2}x^{2}-\frac{1}{2}
$$

$$
P_{3}=\frac{1}{2}x\left(5x^{2}-3\right)
$$

$$
P_{4}=\frac{1}{8}\left(35x^{4}-30x^{2}+3\right)
$$

$$
P_{5}=\frac{1}{8}x\left(63x^{4}-70x^{2}+15\right)
$$

## Leading coefficient

The leading coefficient of $P_{n}$ is denoted by $k_{n}$, and it is given by

$$
k_{n}=\frac{\left(2n\right)!}{2^{n}\left(n!\right)^{2}}
$$

$$
\frac{k_{n+1}}{k_{n}}=\frac{2n+1}{\left(n+1\right)}
$$

## Norm

The norm of $P_{n}$ is given below:

$$
\Vert P_{n}\Vert^{2}=:h_{n}=\frac{2}{2n+1}
$$

$$
\frac{h_{n-1}}{h_{n}}=\frac{2n+1}{2n-1}
$$

$$
\frac{h_{n}}{h_{n-1}}=\frac{2n-1}{2n+1}
$$

$$
\frac{h_{n+1}}{h_{n}}=\frac{2n+1}{2n+3}
$$

## Symmetry

$$
P_{n}(x)=\left(-1\right)^{n}P_{n}(-x)
$$

Therefore, $P_{n}(x)$ is even if $n$ is even and odd if $n$ is odd.

## Scaling

$$
P_{n}(\pm1)=\left(\pm1\right)^{n}
$$

$$
\frac{dP_{n}}{dx}\left(\pm1\right)=\frac{1}{2}\left(\pm1\right)^{n-1}n(n+1)
$$

$$
\frac{d^{2}P_{n}}{dx^{2}}\left(\pm1\right)=\left(\pm1\right)^{n}n(n+1)\left(n+2\right)/8
$$

## Boundedness

$$
\vert P_{n}\vert\le1
$$

$$
\left|\frac{dP_{n}}{dx}\right|\le\frac{1}{2}n(n+1)
$$

## Derivatives

$$
\frac{dP_{n}}{dx}=P_{n-1}^{(3/2)}=\frac{n+1}{2}P_{n-1}^{\left(1,1\right)}
$$

$$
\frac{dP_{n}}{dx}=\sum_{\begin{aligned}k=0\\
k+n & \text{odd}
\end{aligned}
}^{n-1}\left(2k+1\right)P_{k}(x)
$$

$$
\frac{d^{2}P_{n}}{dx^{2}}=\sum_{\begin{aligned}k=0\\
k+n & \text{even}
\end{aligned}
}^{n-2}\left(k+\frac{1}{2}\right)\left[n\left(n+1\right)-k\left(k+1\right)\right]P_{k}(x)
$$

## Orthogonality

$$
\int_{-1}^{+1}P_{m}(x)P_{n}(x)dx=h_{m}\delta_{mn}
$$

$$
\int_{-1}^{+1}\frac{dP_{m}(x)}{dx}\frac{dP_{n}(x)}{dx}\left(1-x^{2}\right)dx=h_{n}n(n+1)\delta_{mn}
$$

## Polynomial representation

$$
P_{n}(x)=\frac{1}{2^{n}}\sum_{m=0}^{\left[n/2\right]}\left(-1\right)^{m}\left(\begin{array}{c}
n\\
m
\end{array}\right)\left(\begin{array}{c}
2n-2m\\
n
\end{array}\right)x^{n-2m}
$$

where $\left[n/2\right]$ is the integer part of $n/2$.

## Strum-Liovile equation

$$
\frac{d}{dx}\left(\left(1-x^{2}\right)\frac{dy}{dx}\right)+n\left(n+1\right)y=0
$$

## Rodrigues's Formula

$$
P_{n}(x)=\frac{\left(-1\right)^{n}}{2^{n}n!}\frac{d^{n}}{dx^{n}}\left[\left(1-x^{2}\right)^{n}\right]
$$

## Recurrence relation for monic Legendre polynomial

Let $\pi_{n}$ denotes the monic orthogonal Legendre polynomial.

$$
\pi_{n+1}=\left(x-\alpha_{n}\right)\pi_{n}-\beta_{n}\pi_{n-1},\quad n=0,1,2
$$

$$
\alpha_{n}=0,n\ge0
$$

$$
\beta_{0}=2
$$

$$
\beta_{n\ge1}=\frac{n^{2}}{4n^{2}-1}
$$

## Recurrence relation for monic orthonormal Legendre polynomial

$$
\tilde{\pi}_{n+1}=\frac{\left(x-\alpha_{n}\right)}{\sqrt{\beta_{n+1}}}\tilde{\pi}_{n}-\frac{\beta_{n}}{\sqrt{\beta_{n+1}\beta_{n}}}\tilde{\pi}_{n-1},\quad n=0,1,2
$$

or

$$
\tilde{\pi}_{n+1}=\left(x-\alpha_{n}\right)s_{n}^{a}\tilde{\pi}_{n}-\beta_{n}s_{n}^{b}\tilde{\pi}_{n-1},\quad n=0,1,2
$$

$$
s_{n}^{a}=\frac{1}{\sqrt{\beta_{n+1}}}
$$

$$
s_{n}^{b}=\frac{1}{\sqrt{\beta_{n}\beta_{n+1}}}=s_{n}^{a}s_{n-1}^{a}
$$

## Recurrence relation for Legendre polynomials

Legendre polynomial $P_{n}$ is neither monic nor orthonormal. First few Legendre polynomials are:

$$
P_{-1}=0
$$

$$
P_{0}=1
$$

$$
P_{1}=x
$$

- The following three term-term recurrence relationship can be used to compute the Legendre polynomial:

$$
(n+1)P_{n+1}=\left(2n+1\right)xP_{n}-nP_{n-1},\quad n=1,2,\cdots
$$

We can also use the following three-term recurrence relationship:

$$
P_{n+1}=\left(x-\alpha_{n}\right)s_{n}^{a}P_{n}-\beta_{n}s_{n}^{b}P_{n-1},\quad n=0,1,2
$$

where,

$$
s_{n}^{a}=\frac{k_{n+1}}{k_{n}}=\frac{2n+1}{n+1}
$$

$$
s_{n}^{b}=s_{n}^{a}s_{n-1}^{a}
$$

$$
s_{0}^{b}=\frac{s_{0}^{a}}{\sqrt{\beta_{0}}}
$$

## Recurrence relation for orthonormal Legendre polynomials

Let $\tilde{P}_{n}$ denote the orthonormal Legendre polynomials.

$$
\tilde{P}_{n+1}=\left(x-\alpha_{n}\right)s_{n}^{a}\tilde{P}_{n}-\beta_{n}s_{n}^{b}\tilde{P}_{n-1},\quad n=0,1,2
$$

where,

$$
s_{n}^{a}=\frac{1}{\sqrt{\beta_{n+1}}}
$$

$$
s_{n}^{b}=s_{n}^{a}s_{n-1}^{a}
$$

$$
s_{0}^{b}=\frac{s_{0}^{a}}{\sqrt{\beta_{0}}}
$$

## Recurrence relation for derivative of Legendre polynomial

The gradient can be computed by using the following three-term recurrence relationship:

$$
\left(1-x^{2}\right)\frac{dP_{n}}{dx}=\beta_{n}\left(2n+1\right)s_{n-1}^{a}P_{n-1}+\left(-nx\right)P_{n}
$$

$$
\frac{dP_{n}}{dx}\left(\pm1\right)=\frac{1}{2}\left(\pm1\right)^{n-1}n(n+1)
$$

$$
s_{n}^{a}=\frac{k_{n+1}}{k_{n}}=\frac{2n+1}{n+1}
$$

## More recurrence relation for derivative of Legendre polynomial

$$
nP_{n}=x\frac{dP_{n}}{dx}-\frac{dP_{n-1}}{dx}
$$

$$
P_{n}=-\frac{x}{n+1}\frac{dP_{n}}{dx}+\frac{1}{n+1}\frac{dP_{n+1}}{dx}
$$

$$
P_{n}=\frac{1}{\left(2n+1\right)}\frac{d}{dx}\left(P_{n+1}-P_{n-1}\right)
$$

$$
\left(1-x^{2}\right)\frac{dP_{n}}{dx}=\frac{n\left(n+1\right)}{2n+1}\left(P_{n-1}-P_{n+1}\right)
$$

## Recurrence relation for derivative of orthonormal Legendre polynomial

$$
\left(1-x^{2}\right)\frac{d\tilde{P}_{n}}{dx}=\beta_{n}\left(2n+1\right)s_{n-1}^{a}\tilde{P}_{n-1}+\left(-nx\right)\tilde{P}_{n}
$$

$$
s_{n-1}^{a}=\frac{1}{\sqrt{\beta_{n}}}
$$

## Recurrence relation for derivative of monic Legendre polynomial

$$
\left(1-x^{2}\right)\frac{d\pi_{n}}{dx}=\beta_{n}\left(2n+1\right)\pi_{n-1}+\left(-nx\right)\pi_{n}
$$

## Recurrence relation for derivative of monic orthonormal Legendre polynomial

$$
\left(1-x^{2}\right)\frac{d\tilde{\pi}_{n}}{dx}=\beta_{n}\left(2n+1\right)s_{n-1}^{a}\tilde{\pi}_{n-1}+\left(-nx\right)\tilde{\pi}_{n}
$$

$$
s_{n-1}^{a}=\frac{1}{\sqrt{\beta_{n}}}
$$


## Kernel polynomial

## More recurrence results

$$
P_{n}^{1,0}(x)=\frac{P_{n}(x)-P_{n+1}(x)}{\left(1-x\right)}
$$

$$
P_{n}^{0,1}(x)=\frac{P_{n}(x)+P_{n+1}(x)}{\left(1+x\right)}
$$

## Additional properties

$$
\left(1-x^{2}\right)\frac{dP_{n+1}}{dx}=-\left(N+1\right)xP_{n+1}+\left(n+1\right)P_{n}
$$

So, if $\left\{ x_{j}\right\}_{j=0}^{n}$ are $n+1$ zeros of $P_{n+1}$, then
$$
\left(1-x_{j}^{2}\right)\frac{dP_{n+1}\left(x_{j}\right)}{dx}=\left(n+1\right)P_{n}\left(x_{j}\right)
$$

**Theorem**: If $x_{j}$ is zero of $P_{n}$, then
$$
\frac{dP_{n}\left(x_{j}\right)}{dx}=\frac{n}{1-x_{j}^{2}}P_{n-1}\left(x_{j}\right)
$$

## Legendre-Gauss Quadratures

Jacobi-matrix for Legendre polynomials is a symmetric tridiagonal matrix ${\bf J}_{n}=\left\{ {\bf D}_{n},{\bf E}_{n}\right\}$. The main diagonal ${\bf D}_{n}$ and sub-diagonal ${\bf E}_{n}$ are given by

$$
{\bf D}_{n}=\boldsymbol{0}\in R^{n}
$$

$$
{\bf E}_{n}=\left[\sqrt{\beta_{1}},\sqrt{\beta_{2}},\cdots,\sqrt{\beta_{n-1}}\right]\in R^{n-1}
$$

- The $N+1$ point Legendre-Gauss quadrature rule is denoted by $\left\{ x_{j}^{G},w_{j}^{G}\right\} _{j=0}^{N}$.

- The points $x_{j}^{G}$ are zeros of $P_{N+1}$, that is

$$
P_{N+1}(x_{j}^{G})=0,j=0,1,\cdots,N
$$

- and $\left\{ x_{j}^{G}\right\}_{j=0}^{N}$ are the eigenvalues of Jacobi matrix ${\bf J}_{N+1}$.

- Weights are given by

$$
w_{j}=\frac{2}{\left[1-\left(x_{j}^{G}\right)^{2}\right]\left[\frac{dP_{N+1}}{dx}\left(x_{j}^{G}\right)\right]^{2}},j=0,\cdots,N
$$

But, we know that

$$
\frac{d}{dx}P_{N+1}\left(x_{j}^{G}\right)=\frac{N+1}{1-\left(x_{j}^{G}\right)^{2}}P_{N}\left(x_{j}^{G}\right)
$$

then weights become

$$
w_{j}=\frac{2\left[1-\left(x_{j}^{G}\right)^{2}\right]}{\left(N+1\right)^{2}\left[P_{N}\left(x_{j}^{G}\right)\right]^{2}},j=0,\cdots,N
$$

## Legendre Gauss-Radau Quadratures

Jacobi Gauss-Radau matrix for Legendre polynomials is a symmetric tridiagonal matrix ${\bf J}_{n+1}^{R,a}=\left\{ {\bf D}_{n+1},{\bf E}_{n+1}\right\}$. The main diagonal ${\bf D}_{n+1}$ and sub-diagonal ${\bf E}_{n+1}$ are given by

$$
{\bf D}_{n+1}=\left[\boldsymbol{0},\alpha_{n}^{R}\right]\in R^{n+1}
$$

$$
{\bf E}_{n}=\left[\sqrt{\beta_{1}},\sqrt{\beta_{2}},\cdots,\sqrt{\beta_{n-1}},\sqrt{\beta_{n}}\right]\in R^{n}
$$

Where,

$$
\alpha_{n}^{R}=a\left(\frac{n+1}{2n+1}\right)
$$

The $n+1$ point Legendre Gauss-Radau Gauss quadrature rule is denoted by $\left\{ x_{j}^{R},w_{j}^{R}\right\} _{j=0}^{n}$, which are the eigenvalues of Jacobi Gauss-Radau matrix. The weights are given by

$$
w_{j}=\frac{1}{\left(n+1\right)^{2}}\frac{1+ax_{j}^{R}}{\left[P_{n}(x_{j}^{R})\right]^{2}},j=0,\cdots,n
$$

There is another point of view for understanding the Gauss-Radau quadrature points.

- For $a=-1$, $x_{0}=-1$, and $n$ points $x_{j}^{R},1=0,\cdots n$ are zeros of $P_{n}^{0,1}(x)$ that is,
$$
P_{n}^{0,1}(x_{j}^{R})=0,j=1,\cdots n
$$

- For $a=1$, $x_{n}^{R}=1$, and $n$ points $x_{j}^{R},j=0,\cdots n-1$ are zeros $P_{n}^{1,0}(x)$ that is,
$$
P_{n}^{1,0}(x_{j}^{R})=0,j=0,\cdots n-1
$$

## Legendre Gauss-Lobatto Quadratures

Jacobi Gauss-Lobatto matrix for Legendre polynomials is a symmetric tridiagonal matrix ${\bf J}_{n+2}^{L}=\left\{ {\bf D}_{n+2},{\bf E}_{n+2}\right\}$. The main diagonal ${\bf D}_{n+2}$ and sub-diagonal ${\bf E}_{n+2}$ are given by

$$
{\bf D}_{n+2}=\boldsymbol{0}\in R^{n+2}
$$

$$
{\bf E}_{n+2}=\left[\sqrt{\beta_{1}},\sqrt{\beta_{2}},\cdots,\sqrt{\beta_{n-1}},\sqrt{\beta_{n}},\sqrt{\beta_{n+1}^{L}}\right]\in R^{n+1}
$$

$$
\beta_{n+1}^{L}=\frac{n+1}{2n+1}
$$

The $n+2$ point Jacobi Gauss-Lobatto quadrature rule is denoted by $\left\{ x_{j}^{L},w_{j}^{L}\right\} _{j=0}^{n+1}$, which are the eigenvalues of Jacobi Gauss-Lobatto matrix.The weights are given by

$$
w_{j}=\frac{2}{\left(n+2\right)\left(n+1\right)}\frac{1}{\left[P_{n+1}(x_{j}^{R})\right]^{2}},j=0,\cdots,n+1
$$

There is another point of view for understanding the Gauss-Lobatto quadrature points.

> $x_{0}^{L}=-1$ and $x_{n+1}^{L}=1$, the $n$ points $x_{j}^{L},j=1,\cdots n$ are zeros of $P_{n}^{1,1}(x)$ , that is zeros of $\frac{dP_{n+1}}{dx}$


## Lagrange polynomial for Legendre-Gauss points

## Lagrange polynomial for Legendre-Gauss-Lobatto points

## Lagrange polynomial for Legendre-Gauss-Radau points
