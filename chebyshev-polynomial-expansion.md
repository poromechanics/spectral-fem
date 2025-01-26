# Chebyshev Polynomial Expansion

# Continuous expansion

The continuous Chebyshev expansion of a function $u(x)$ is given by

$$
u(x)=\sum_{n=0}^{\infty}\hat{u}_{n}T_{n}(x)
$$

where, the expansion coefficients are defined by:

$$
\hat{u}_{n}=\frac{2}{c_{n}\pi}\int_{-1}^{+1}u(x)T_{n}(x)\frac{1}{\sqrt{1-x^{2}}}dx
$$

where,

$$
c_{n}=\begin{cases}
2 & n=0\\
1 & n>0
\end{cases}
$$

The norm of Chebyshev polynomial is given by

$$
\Vert T_{n}\Vert^{2}=\frac{c_{n}\pi}{2}
$$

The $m$th derivative of $u(x)$ has a similar expansion with coefficients $\hat{u}_{n}^{(m)}$:

$$
\partial_{x}^{m}u(x)=\sum_{n=0}^{\infty}\hat{u}_{n}^{(m)}T_{n}(x)
$$

The relationship between $\hat{u}_{n}^{(m-1)}$ and $\hat{u}_{n}^{(m)}$ is given by:

$$
\hat{u}_{n}^{(m-1)}=\frac{c_{n-1}}{2n}\hat{u}_{n-1}^{(m)}-\frac{1}{2n}\hat{u}_{n+1}^{(m)}
$$

The relationship between $\hat{u}_{n}^{(m)}$and $\hat{u}_{n}^{(m-1)}$ is given by:

$$
\hat{u}_{n}^{(m)}=\frac{2}{c_{n}}\sum_{\begin{aligned}p=n+1\\
n+p\text{ odd}
\end{aligned}
}^{\infty}p\hat{u}_{p}^{(m-1)}\quad\forall n
$$

# Truncated expansion

In practice, we consider expansion of $u(x)$ by using the finite number of polynomials $T_{n}(x)$ with $n\le N$,

$$
\mathcal{P}_{N}u(x)=\sum_{n=0}^{N}\hat{u}_{n}T_{n}(x)
$$

In this way, $\mathcal{P}_{N}u(x)$ denotes the projection of $u(x)$ on $\mathcal{P}_{N}$, therefore, $\hat{u}_{n}=0,\forall n>N$.

Let us now consider the first derivative of $u$.

$$
\mathcal{P}_{N}\frac{du(x)}{dx}=\sum_{n=0}^{N}\hat{u}_{n}^{(1)}T_{n}(x),
$$

with $\hat{u}_{n}^{(1)}=0,\forall n>N$ and $\mathcal{P}_{N}\frac{du(x)}{dx}\in\mathcal{P}_{N-1}$. We can obtain coefficients of derivative from backward subtitution.

$$
c_{n-1}\hat{u}_{n-1}^{(m)}=\hat{u}_{n+1}^{(m)}+2n\hat{u}_{n}^{(m-1)},\text{with }\hat{u}_{N}^{(m)}=0
$$

# Discrete expansion

Let $\left\{ x_{j},w_{j}\right\} _{j=0}^{N}$ be a set of Gauss, Gauss-Radau or Gauss-Lobatto quadrature nodes and weights. The discrete Chebyshev polynomial expansion is given by (_Inverse Chebyshev Transform_):

$$
\mathcal{I}_{N}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}T_{n}(x)
$$

where $\tilde{u}_{n}$ are the coefficients of discrete polynomial expansion compute by Forward Discrete Chebyshev Transform (or_Chebyshev Transform_ation):

$$
\tilde{u}_{n}=\frac{1}{\Vert P_{n}\Vert_{N}^{2}}\sum_{j=0}^{N}u(x_{j})T_{n}(x_{j})w_{j}
$$

- It is noteworthy that $\Vert P_{n}\Vert_{N}^{2}$ would be exact for Gauss and Gauss-Radau quadratures, but it would be approximate for Gauss-Lobatto points.

- $\left\{ u(x_{j})\right\}_{j=0}^{N}$ denotes value of $u$ at quadrature points, we will refer it to nodal-values in physical space, or simply nodal values of $u$.

- $\left\{ \tilde{u}_{n}\right\}_{n=0}^{N}$ denotes the coefficient of polynomial expansion, we will refer it to modal-values in frequency space, or simply modal values $u$.

If $f\in\mathcal{P}_{N}$ then, the $f^{2}\in\mathcal{P}_{2N}$, therefore, $N+1$ Gauss-Quadrature points and Gauss-Radau points are enough for computing the norm. However, Gauss-Lobatto points are not enough to compute the norm. In practice, Gauss-Lobatto rules are very useful as they include boundary nodes. Thanks to following lemma we can compute the equivalent norm by using the Gauss-Lobatto points.

- **Theorem**: For $u\in$ $H_{w}^{p}[-1,1]$ where $p>\frac{1}{2}$ and $0\le q\le p$, there exists a constant, $C$, which is independent of $N$, such that: $\Vert u-\mathcal{I}_{N}u\Vert_{H_{w}^{q}\left[-1,1\right]}\le CN^{2q-p}\Vert u\Vert_{H_{w}^{p}\left[-1,1\right]}$.

- **Theorem**: For $u\in$ $H_{w}^{p}[-1,1]$ where $p>\frac{1}{2}$ , there exists a constant, $C$, which is independent of $N$, such that: $\Vert u-\mathcal{I}_{N}u\Vert_{L^{\infty}\left[-1,1\right]}\le CN^{1/2-p}\Vert u\Vert_{H_{w}^{p}\left[-1,1\right]}$.


# Differentiation in physical space

In the physical space, we can write the discrete Legendre expansion by using the Lagrange polynomials with interpolation points as the Gauss quadrature points $\left\{ x_{j}\right\}_{j=0}^{N}$.

$$
\mathcal{I}_{N}u(x)=\sum_{j=0}^{N}u(x_{j})l_{j}(x)
$$

- All Lagrange polynomials, $\left\{ l_{j}(x)\right\}_{j=0}^{N}$, are $N$ order polynomials, and $l_{j}(x_{i})=\delta_{ij}$.

- Lagrange polynomial depend upon the quadrature rules used in the discrete transformation.

The differentiation in physical space is given by:

$$
\partial_{x}^{m}\mathcal{I}_{N}u(x)=\sum_{j=0}^{N}u(x_{j})\partial_{x}^{m}l_{j}(x)
$$

If we evaluate the derivatives at quadrature points, then

$$
\begin{aligned}\partial_{x}^{m}\mathcal{I}_{N}u(x_{i}) & =\sum_{j=0}^{N}u(x_{j})\partial_{x}^{m}l_{j}(x_{i}),\quad i=0,\cdots,N\end{aligned}
$$

Consider $m=1$:

$$
\begin{aligned}\partial_{x}\mathcal{I}_{N}u(x_{i}) & =\sum_{j=0}^{N}u(x_{j})\partial_{x}l_{j}(x_{i}),\quad i=0,\cdots,N\\
 & =\sum_{j=0}^{N}u(x_{j})D_{ij}
\end{aligned}
$$

where, $D_{ij}$ is called the Differentiation matrix, which is a square matrix of size $N+1$. In the matrix-vector form:

$$
\frac{d{\bf u}}{dx}={\bf D}{\bf u}
$$

- The entries of matrix ${\bf D}$ depend upon the orthogonal polynomial family, and quadrature type.

- The $m$th order derivative of $u$ at quadrature point is given by:

$$
\frac{d^{m}{\bf u}}{dx^{m}}={\bf D}^{m}{\bf u}
$$

# Derivative in frequency space

The process of Differentiation in the frequency space is relatively simpler than that in the physical space. In the frequency space, $\mathcal{I}_{N}u(x)\in\mathcal{P}_{N}$,

$$
\mathcal{I}_{N}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}T_{n}(x)
$$

and $\mathcal{I}_{N}\frac{d}{dx}u(x)\in P_{N-1}$

$$
\mathcal{I}_{N}\frac{d}{dx}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}\frac{d}{dx}T_{n}(x)=\sum_{n=0}^{N}\tilde{u}_{n}^{(1)}T_{n}(x)
$$

where, $\tilde{u}_{n}^{(1)}$ are the modal coefficients for first derivative, and $\tilde{u}_{N}^{(1)}=0$. We can use following **backward subtitution algorithm** to get $\left\{ \tilde{u}_{n}^{(1)}\right\}_{n=0}^{N}$from $\left\{ \tilde{u}_{n}\right\}_{n=0}^{N}$:

1. Initialization: $\tilde{u}_{N}^{(1)}=0$, $\tilde{u}_{N-1}^{(1)}=\left(\frac{2N}{c_{N-1}}\right)\tilde{u}_{N}$

2. For $n=N-1,\cdots,1$: $c_{n-1}\tilde{u}_{n-1}^{(1)}=\tilde{u}_{n+1}^{(1)}+2n\tilde{u}_{n}$

# Chebyshev Gauss-Lobatto expansion

Chebyshev Gauss-Lobatto rule is given by:

$$
x_{j}=-\cos\left(\frac{\pi j}{N}\right)
$$

$$
w_{j}=\frac{\pi}{c_{j}N}
$$

$$
\theta_{j}=\pi+\frac{\pi j}{N}
$$

$$
T_{n}(x_{j})=cos\left(n\pi+\frac{n\pi j}{N}\right)=\left(-1\right)^{n}cos\left(\frac{n\pi j}{N}\right)
$$

$$
T_{n}(x_{j})=\cos\left(\frac{n\pi j}{N}\right)
$$

- Chebyshev transformation

$$
\begin{aligned}\tilde{u}_{n} & =\frac{1}{\Vert T_{n}\Vert_{N}^{2}}\sum_{i=0}^{N}u(x_{i})\cos\left(\frac{n\pi i}{N}\right)w_{i}\end{aligned}
$$

where,

$$
\Vert T_{n}\Vert_{N}^{2}=\frac{\pi}{2}\tilde{c}_{n}
$$

and,

$$
\tilde{c}_{n}=\begin{cases}
2 & n=0,N\\
1 & \text{otherwise}
\end{cases}
$$

Finally, the Chebyshev Gauss-Lobatto expansion of a function $u(x)$ on $[-1,1]$ is given by:

$$
\begin{aligned}\tilde{u}_{n} & =\frac{2}{N\tilde{c}_{n}}\sum_{i=0}^{N}\frac{u(x_{i})}{\tilde{c}_{i}}\cos\left(\frac{n\pi i}{N}\right)\end{aligned}
$$

- Inverse Chebyshev Transformation:

$$
\mathcal{I}_{N}u(x)=\sum_{i=0}^{N}\tilde{u}_{i}T_{i}(x)
$$

Differentiation in physical space is performed by using $D$ matrix, which is given below.

$$
D_{ij}=\begin{cases}
-\frac{2N^{2}+1}{6} & i=j=0\\
-\frac{x_{i}}{2(1-x_{i}^{2})} & i=j\in[1,\cdots,N-1]\\
\frac{\tilde{c}_{i}}{\tilde{c}_{j}}\frac{\left(-1\right)^{i+j}}{x_{i}-x_{j}} & i\ne j\\
-D_{00} & i=j=N
\end{cases}
$$

To achieve higher order accuracy in spectral differentiations, we use:

$$
D_{ij}=\begin{cases}
-\frac{2N^{2}+1}{6} & i=j=0\\
-\frac{x_{i}}{2\sin^{2}\left(\frac{\pi i}{N}\right)} & i=j\in[1,\cdots,N-1]\\
\frac{\tilde{c}_{i}}{2\tilde{c}_{j}}\frac{\left(-1\right)^{i+j}}{\sin\left(\frac{i+j}{2N}\pi\right)\sin\left(\frac{i-j}{2N}\pi\right)} & i\ne j\\
-D_{00} & i=j=N
\end{cases}
$$

# Chebyshev Gauss expansion

Chebyshev Gauss points are:

$$
x_{j}=-\cos\left(\frac{(2j+1)\pi}{2N+2}\right)
$$

$$
w_{j}=\frac{\pi}{N+1}
$$

$$
\theta_{j}=\pi+\frac{\left(2j+1\right)\pi}{2N+2}
$$

$$
T_{n}(x_{j})=cos\left(n\pi+\frac{n\left(2j+1\right)\pi}{2N+2}\right)=\left(-1\right)^{n}\cos n\left(\frac{2j+1}{2N+2}\right)\pi
$$

Therefore,

$$
T_{n}(x_{j})=\cos n\left(\frac{2j+1}{2N+2}\right)\pi
$$

- Chebyshev transformation:

$$
\begin{aligned}\tilde{u}_{n} & =\frac{2}{c_{n}(N+1)}\sum_{i=0}^{N}u(x_{i})\cos\frac{n(2i+1)}{N+1}\frac{\pi}{2}\end{aligned}
$$

- Inverse Chebyshev Transformation:

$$
\mathcal{I}_{N}u(x)=\sum_{i=0}^{N}\tilde{u}_{i}T_{i}(x)
$$

Differentiation in physical space is performed by using $D$ matrix, which is given below.

$$
D_{ij}=\begin{cases}
\frac{z_{i}}{2(1-z_{i}^{2})} & i=j\\
\frac{\partial_{x}T_{N+1}(x_{i})}{\partial_{x}T_{N+1}(x_{j})}\frac{1}{x_{i}-x_{j}} & i\ne j
\end{cases}
$$
