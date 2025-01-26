# Chebyshev Polynomial

Chebyshev polynomial family has a simple explicit formula and is straightforward to compute. Chebyshev polynomials are proportional to the Jacobi polynomial, $P_{n}^{(-0.5,-0.5)}(x)$, and denoted by $T_{n}(x)$.

$$
T_{n}(x)=\frac{\left(n!2^{n}\right)^{2}}{(2n)!}P_{N}^{(-0.5,-0.5)}(x)
$$

$T_{n}(x)$ are orthogonal with respect to the weight:

$$
w(x)=\frac{1}{\sqrt{1-x^{2}}}
$$

The support of Chebyshev polynomial is $\left[-1,1\right]$.

> Legendre's polynomials are best from the point of view of minimizing the $L^{\infty}$ error.


## First few Chebyshev polynomials

$$
T_{0}(x)=1
$$

$$
T_{1}(x)=x
$$

$$
T_{2}(x)=2x^{2}-1
$$

$$
T_{3}(x)=4x^{3}-3x
$$

$$
T_{4}(x)=8x^{4}-8x^{2}+1
$$

$$
T_{5}(x)=16x^{5}-20x^{3}+5x
$$

## Leading coefficient

The leading coefficient of $T_{n}$ is denoted by $k_{n}$, and it is given by

$$
k_{n}=2^{n-1}c_{n}
$$

$$
c_{n}=\begin{cases}
2 & n=0\\
1 & n\ge1
\end{cases}
$$

$$
\frac{k_{n+1}}{k_{n}}=\frac{2}{c_{n}},\quad n\ge0
$$

## Norm

The norm of $T_{n}$ is given below:

$$
\Vert T_{n}\Vert^{2}=:h_{n}=\frac{c_{n}\pi}{2}=\begin{cases}
\pi & n=0\\
\frac{\pi}{2} & n\ge1
\end{cases}
$$

$$
\frac{h_{n-1}}{h_{n}}=c_{n}
$$

$$
\frac{h_{n+1}}{h_{n}}=\frac{1}{c_{n+1}}
$$

## Symmetry

$$
T_{n}(-x)=\left(-1\right)^{n}T_{n}(x)
$$

## Scaling

$$
T_{n}\left(\pm1\right)=\left(\pm1\right)^{n}
$$

$$
\frac{d}{dx}T_{n}\left(\pm1\right)=\left(\pm1\right)^{n+1}n^{2}
$$

$$
\frac{d^{2}}{dx^{2}}T_{n}\left(\pm1\right)=\frac{1}{3}\left(\pm1\right)^{n}n^{2}\left(n^{2}-1\right)
$$

## Boundedness

$$
\vert T_{n}(x)\vert\le1,\quad\left|\frac{dT_{n}}{dt}\right|\le n^{2}
$$

## Derivatives

## Orthogonality

$$
\int_{-1}^{+1}T_{m}(x)T_{n}(x)\frac{1}{\sqrt{1-x^{2}}}dx=\frac{c_{n}\pi}{2}\delta_{mn}
$$

$$
\int_{-1}^{+1}\frac{dT_{m}(x)}{dx}\frac{dT_{n}(x)}{dx}\sqrt{1-x^{2}}dx=\frac{n^{2}c_{n}\pi}{2}\delta_{mn}
$$

## Polynomial representation

## Strum-Liovile equation

$$
\frac{d}{dx}\left(\sqrt{1-x^{2}}\frac{dT_{n}}{dx}\right)+\frac{\lambda_{n}}{\sqrt{1-x^{2}}}T_{n}=0
$$

where, the eigenvalue $\lambda_{n}=n^{2}$.

If we set $x=\cos\theta$, then

$$
\frac{d^{2}T_{n}(\theta)}{d\theta^{2}}+\lambda_{n}T_{n}(\theta)=0
$$

therefore, $T_{n}(\theta)=\cos\left(n\theta\right)$.

## Rodrigues's Formula

$$
T_{n}(x)=\frac{\left(-1\right)^{n}n!2^{n}}{(2n)!}\sqrt{1-x^{2}}\frac{d^{n}}{dx^{n}}\left[\left(1-x^{2}\right)^{n-\frac{1}{2}}\right]
$$

## Recurrence relation for monic polynomial

Let $\pi_{n}$ denotes the monic orthogonal Chebyshev polynomial of first kind.

$$
\pi_{n+1}=\left(x-\alpha_{n}\right)\pi_{n}-\beta_{n}\pi_{n-1},\quad n=0,1,2
$$

$$
\alpha_{n}=0,n\ge0
$$

$$
\beta_{0}=\pi
$$

$$
\beta_{n\ge1}=\frac{c_{n-1}}{4}
$$

## Recurrence relation for monic orthonormal polynomial

Let $\tilde{\pi}_{n}$ denotes the monic orthonormal Chebyshev polynomial of first kind.

$$
\tilde{\pi}_{n+1}=\frac{\left(x-\alpha_{n}\right)}{\sqrt{\beta_{n+1}}}\tilde{\pi}_{n}-\frac{\beta_{n}}{\sqrt{\beta_{n+1}\beta_{n}}}\tilde{\pi}_{n-1},\quad n=0,1,2
$$

or

$$
\tilde{\pi}_{n+1}=\left(x-\alpha_{n}\right)s_{n}^{a}\tilde{\pi}_{n}-\beta_{n}s_{n}^{b}\tilde{\pi}_{n-1},\quad n=0,1,2
$$

$$
s_{n}^{a}=\frac{1}{\sqrt{\beta_{n+1}}}=\frac{2}{\sqrt{c_{n}}}
$$

$$
s_{n}^{b}=s_{n}^{a}s_{n-1}^{a}
$$

$$
s_{0}^{b}=\frac{s_{0}^{a}}{\sqrt{\beta_{0}}}
$$

## Recurrence relation for Chebyshev polynomials

Chebyshev polynomial $T_{n}$ is neither monic nor orthonormal.

$$
T_{-1}=0,\quad T_{0}=1
$$

$$
T_{1}=x
$$

$$
T_{n+1}=2xT_{n}-T_{n-1},\quad n\ge1
$$

or,

$$
T_{n+1}=\left(x-\alpha_{n}\right)s_{n}^{a}T_{n}-\beta_{n}s_{n}^{b}T_{n-1},\quad n=0,1,2
$$

where,

$$
s_{n}^{a}=\frac{k_{n+1}}{k_{n}}=\frac{2}{c_{n}}
$$

$$
s_{n}^{b}=s_{n}^{a}s_{n-1}^{a}
$$

$$
s_{0}^{b}=\frac{s_{0}^{a}}{\sqrt{\beta_{0}}}
$$

## Recurrence relation for orthonormal Chebyshev polynomials

Let $\tilde{T}_{n}$ denote the orthonormal Chebyshev polynomials.

$$
\tilde{T}_{n+1}=\left(x-\alpha_{n}\right)s_{n}^{a}\tilde{P}_{n}-\beta_{n}s_{n}^{b}\tilde{P}_{n-1},\quad n=0,1,2
$$

where,

$$
s_{n}^{a}=\frac{1}{\sqrt{\beta_{n+1}}}=\frac{2}{\sqrt{c_{n}}}
$$

$$
s_{n}^{b}=s_{n}^{a}s_{n-1}^{a}
$$

$$
s_{0}^{b}=\frac{s_{0}^{a}}{\sqrt{\beta_{0}}}
$$

## Recurrence relation for derivative of Chebyshev polynomial

The gradient can be computed by following recurrence relationship:

$$
\left(1-x^{2}\right)\frac{dT_{n}}{dx}=\beta_{n}\left(2n+1\right)s_{n-1}^{a}T_{n-1}+\left(-nx\right)T_{n}
$$

$$
\frac{d}{dx}T_{n}\left(\pm1\right)=\left(\pm1\right)^{n+1}n^{2}
$$

$$
s_{n}^{a}=\frac{k_{n+1}}{k_{n}}=\frac{2}{c_{n}}
$$

## More recurrence relation for derivative of Chebyshev polynomial

$$
\left(1-x^{2}\right)\frac{dT_{n}}{dx}=\frac{n}{2}T_{n-1}-\frac{n}{2}T_{n+1}
$$

$$
T_{n}=-\frac{1}{2(n-1)}\frac{dT_{n-1}}{dx}+\frac{1}{2(n+1)}\frac{dT_{n+1}}{dx}
$$

$$
\frac{dT_{n+1}}{dx}=2(n+1)T_{n}+\frac{(n+1)}{(n-1)}\frac{dT_{n-1}}{dx}
$$

## Recurrence relation for derivative of orthonormal Chebyshev polynomial

$$
\left(1-x^{2}\right)\frac{d\tilde{T}_{n}}{dx}=\beta_{n}\left(2n+1\right)s_{n-1}^{a}\tilde{T}_{n-1}+\left(-nx\right)\tilde{T}_{n}
$$

$$
s_{n-1}^{a}=\frac{1}{\sqrt{\beta_{n}}}=\begin{cases}
\frac{1}{\sqrt{\beta_{0}}} & n=0\\
\frac{2}{\sqrt{c_{n-1}}} & n\ge1
\end{cases}
$$

## Recurrence relation for derivative of monic Chebyshev polynomial

$$
\left(1-x^{2}\right)\frac{d\pi_{n}}{dx}=\beta_{n}\left(2n+1\right)\pi_{n-1}+\left(-nx\right)\pi_{n}
$$

## Recurrence relation for derivative of monic orthonormal Chebyshev polynomial

$$
\left(1-x^{2}\right)\frac{d\tilde{\pi}_{n}}{dx}=\beta_{n}\left(2n+1\right)s_{n-1}^{a}\tilde{\pi}_{n-1}+\left(-nx\right)\tilde{\pi}_{n}
$$

$$
s_{n-1}^{a}=\frac{1}{\sqrt{\beta_{n}}}=\begin{cases}
\frac{1}{\sqrt{\beta_{0}}} & n=0\\
\frac{2}{\sqrt{c_{n-1}}} & n\ge1
\end{cases}
$$

## Kernel polynomial


## More recurrence results

## Additional properties

## Chebyshev-Gauss Quadratures

Jacobi-matrix for Chebyshev polynomials is a symmetric tridiagonal matrix ${\bf J}_{n}=\left\{ {\bf D}_{n},{\bf E}_{n}\right\}$. The main diagonal ${\bf D}_{n}$ and sub-diagonal ${\bf E}_{n}$ are given by

$$
{\bf D}_{n}=\boldsymbol{0}\in R^{n}
$$

$$
{\bf E}_{n}=\left[\sqrt{2},2\cdots,2\right]\in R^{n-1}
$$

- The $N+1$ point Chebyshev-Gauss quadrature rule is denoted by $\left\{ x_{j}^{G},w_{j}^{G}\right\} _{j=0}^{N}$.

- The points $x_{j}^{G}$ are zeros of $T_{N+1}$, that is

$$
T_{N+1}(x_{j}^{G})=\cos\left(N+1\right)\theta=0,j=0,1,\cdots,N
$$

- and $\left\{ x_{j}^{G}\right\}_{j=0}^{N}$ are the eigenvalues of Jacobi matrix ${\bf J}_{N+1}$ :

$$
x_{j}^{G}=-\cos\frac{(2j+1)\pi}{2N+2},j=0,\cdots,N
$$

- Weights are given by

$$
w_{j}=\frac{\pi}{N+1},j=0,\cdots,N
$$

## Chebyshev Gauss-Radau Quadratures

- Left Chebyshev Gauss-Radau quadratures:

$$
x_{j}^{R}=-\cos\frac{2\pi j}{2N+1},j=0,\cdots,N
$$

$$
w_{0}^{R}=\frac{\pi}{2N+1}
$$

$$
w_{j}^{R}=\frac{2\pi}{2N+1},j=1,\cdots,N
$$

- Right Chebyshev Gauss-Radau quadratures:

$$
x_{j}^{R}=-\cos\frac{(2j+1)\pi}{2N+1},j=0,\cdots,N
$$

$$
w_{0}^{R}=\frac{\pi}{2N+1}
$$

$$
w_{j}^{R}=\frac{2\pi}{2N+1},j=1,\cdots,N
$$

## Chebyshev Gauss-Lobatto Quadratures

$$
x_{j}^{L}=-\cos\frac{\pi j}{N},j=0,\cdots,N
$$

$$
w_{0}^{R}=w_{N}^{R}=\frac{\pi}{2N}
$$

$$
w_{j}^{R}=\frac{\pi}{N},j=1,\cdots,N-1
$$


## Lagrange polynomial for Chebyshev-Gauss points

## Lagrange polynomial for Chebyshev-Gauss-Lobatto points

## Lagrange polynomial for Chebyshev-Gauss-Radau points
