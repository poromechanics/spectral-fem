# Jacobi Polynomial Expansion

# Continuous expansion

Let $u(x)$ be any continuous function defined over $\left[-1,1\right]$ and $P_{n}^{(\alpha,\beta)}(x)$ be the Jacobi polynomial of degree $n$ and $\alpha,\beta>-1$ . Then the continuous polynomial expansion of $u$ in terms of $P_{n}^{(\alpha,\beta)}(x)$ is given by:

$$
u(x)=\sum_{n=0}^{\infty}\hat{u}_{n}P_{n}^{(\alpha,\beta)}(x)
$$

where,

$$
\hat{u}_{n}=\frac{1}{\Vert p_{n}\Vert^{2}}\int_{-1}^{+1}u(x)P_{n}^{(\alpha,\beta)}(x)\left(1-x\right)^{\alpha}\left(1+x\right)^{\beta}dx
$$

The $m$th derivative of $u(x)$ has a similar expansion with coefficients $\hat{u}_{n}^{(m)}$:

$$
\partial_{x}^{m}u(x)=\sum_{n=0}^{\infty}\hat{u}_{n}^{(m)}P_{n}^{(\alpha,\beta)}(x)
$$

# Truncated expansion

In practice, we employ truncated polynomial expansion by using the finite number of Jacobi polynomials $\left\{ P_{n}^{(\alpha,\beta)}\right\}_{n=0}^{N}$:

$$
\mathcal{P}_{N}u(x)=\sum_{n=0}^{N}\hat{u}_{n}P_{n}^{(\alpha,\beta)}(x)
$$

where,

$$
\hat{u}_{n}=\frac{1}{\Vert P_{n}^{(\alpha,\beta)}\Vert^{2}}\int_{-1}^{+1}u(x)P_{n}^{(\alpha,\beta)}(x)w(x)dx
$$

The $m$th derivative of $u(x)$ in the frequency space is given by:

$$
\mathcal{P}_{N}\partial_{x}^{m}u(x)=\sum_{n=0}^{N}\hat{u}_{n}^{(m)}P_{n}^{(\alpha,\beta)}(x)
$$

The $m$th derivative of $u(x)$ in the physical space is given by:

$$
\mathcal{P}_{N}\partial_{x}^{m}u(x)=\sum_{j=0}^{N}\hat{u}_{n}\partial_{x}^{m}l_{j}(x)
$$

where, $l_{j}(x)$ is the Lagrange polynomial of order $N$ (the details are given in forthcoming sections).

# Discrete expansion

Let $\left\{ x_{j},w_{j}\right\} _{j=0}^{N}$ be a set of Jacobi Gauss, Gauss-Radau or Gauss-Lobatto quadrature nodes and weights. The discrete Jacobi polynomial expansion is given by Inverse Discrete Jacobi Transform (or_Inverse Jacobi Transform_):

$$
\mathcal{I}_{N}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}P_{n}^{(\alpha,\beta)}(x)
$$

where $\tilde{u}_{n}$ are the coefficients of discrete polynomial expansion compute by Forward Discrete Jacobi Transform (or_Jacobi Transform_):

$$
\tilde{u}_{n}=\frac{1}{\Vert P_{n}^{(\alpha,\beta)}\Vert_{N}^{2}}\sum_{j=0}^{N}u(x_{j})P_{n}^{(\alpha,\beta)}(x_{j})w_{j}
$$

- It is noteworthy that $\Vert P_{n}^{(\alpha,\beta)}\Vert_{N}^{2}$ would be exact for Gauss and Gauss-Radau quadratures, but it would be approximate for Gauss-Lobatto points.

- $\left\{ u(x_{j})\right\}_{j=0}^{N}$ denotes value of $u$ at quadrature points, we will refer it to nodal-values in physical space, or simply nodal values of $u$.

- $\left\{ \tilde{u}_{n}\right\}_{n=0}^{N}$ denotes the coefficient of polynomial expansion, we will refer it to modal-values in frequency space, or simply modal values $u$.

# Differentiation in physical space

In the physical space, we can write the discrete Jacobi expansion by using the Lagrange polynomials with interpolation points as the Gauss quadrature points $\left\{ x_{j}\right\}_{j=0}^{N}$.

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

- If the $N+1$ quadrature points are zeros of polynomial $Q\in P_{N+1}$, ($Q$ is also called the quadrature polynomial) then Lagrange polynomial and $D_{ij}$ are given by:

$$
l_{j}(x)=\frac{Q(x)}{\partial_{x}Q(x_{j})}\frac{1}{\left(x-x_{j}\right)},j=0,\cdots,N
$$

$$
D_{ij}=\begin{cases}
\frac{\partial_{x}Q(x_{i})}{\partial_{x}Q(x_{j})}\frac{1}{x_{i}-x_{j}} & i\ne j\\
\frac{\partial_{x}^{2}Q(x_{i})}{2\partial_{x}Q(x_{j})} & i=j
\end{cases}
$$

Quadrature polynomial $Q$ for Gauss, Gauss-Radau, and Gauss-Lobatto quadrature are given by

$$
Q=\begin{cases}
P_{N+1}^{(\alpha,\beta)}(x) & \text{Gauss}\\
P_{N+1}^{(\alpha,\beta)}(x)-\frac{P_{N+1}^{(\alpha,\beta)}(a)}{P_{N}^{(\alpha,\beta)}(a)}P_{N}^{(\alpha,\beta)}(x) & \text{Gauss-Radau}\\
P_{N+1}^{(\alpha,\beta)}(x)+\alpha_{N}P_{N}^{(\alpha,\beta)}(x)+\beta_{N}P_{N-1}^{(\alpha,\beta)}(x) & \text{Gauss-Lobatto}
\end{cases}
$$

In the case of Gauss-Radau $a\in\left\{ -1,1\right\} ,$and in the case of Gauss-Lobatto, $\alpha_{N}$ and $\beta_{N}$ are obtained by solving following 2×2 system of equations:

$$
\left[\begin{array}{cc}
P_{N}^{(\alpha,\beta)}(-1) & P_{N-1}^{(\alpha,\beta)}(-1)\\
P_{N}^{(\alpha,\beta)}(1) & P_{N-1}^{(\alpha,\beta)}(1)
\end{array}\right]\left\{ \begin{array}{c}
\alpha_{N}\\
\beta_{N}
\end{array}\right\} =-\left\{ \begin{array}{c}
P_{N+1}^{(\alpha,\beta)}(-1)\\
P_{N+1}^{(\alpha,\beta)}(+1)
\end{array}\right\}
$$

- The $m$th order derivative of $u$ at quadrature point is given by:

$$
\frac{d^{m}{\bf u}}{dx^{m}}={\bf D}^{m}{\bf u}
$$

# Derivative in frequency space

The process of Differentiation in the frequency space is relatively simpler than that in the physical space. In the frequency space, $\mathcal{I}_{N}u(x)\in P_{N}$,

$$
\mathcal{I}_{N}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}P_{n}^{(\alpha,\beta)}(x)
$$

and $\mathcal{I}_{N}\frac{d}{dx}u(x)\in P_{N-1}$

$$
\mathcal{I}_{N}\frac{d}{dx}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}\frac{d}{dx}P_{n}^{(\alpha,\beta)}(x)=\sum_{n=0}^{N}\tilde{u}_{n}^{(1)}P_{n}^{(\alpha,\beta)}(x)
$$

where, $\tilde{u}_{n}^{(1)}$ are the modal coefficients for first derivative, and $\tilde{u}_{N}^{(1)}=0$.

We can use following **backward subtitution algorithm** to get $\left\{ \tilde{u}_{n}^{(1)}\right\}_{n=0}^{N}$from $\left\{ \tilde{u}_{n}\right\}_{n=0}^{N}$:

1. Initialization: $\tilde{u}_{N}^{(1)}=0$, $\tilde{u}_{N-1}^{(1)}=\frac{1}{\tilde{c}_{N-1}}\tilde{u}_{N}$

2. For $n=N-1,\cdots,1$: $\tilde{u}_{n-1}^{(1)}=\frac{1}{\tilde{c}_{n-1}}\left[\tilde{u}_{n}-\tilde{b}_{n}\tilde{u}_{n}^{(1)}-\tilde{a}_{n+1}\tilde{u}_{n+1}^{(1)}\right]$

where,

$$
\tilde{a}_{n}=\frac{-2\left(n+\alpha\right)\left(n+\beta\right)}{\left(n+\alpha+\beta\right)\left(2n+\alpha+\beta\right)\left(2n+\alpha+\beta+1\right)}
$$

$$
\tilde{b}_{n}=\frac{2\left(\alpha-\beta\right)}{\left(2n+\alpha+\beta\right)\left(2n+\alpha+\beta+2\right)}
$$

$$
\tilde{c}_{n}=\frac{2\left(n+\alpha+\beta+1\right)}{\left(2n+\alpha+\beta+1\right)\left(2n+\alpha+\beta+2\right)}
$$

$$
\tilde{c}_{0}=\frac{2}{\left(\alpha+\beta+2\right)}
$$

# Jacobi Gauss-Lobatto expansion

- Jacobi Transformation:

$$
\tilde{u}_{n}=\frac{1}{\Vert P_{n}^{(\alpha,\beta)}\Vert_{N}^{2}}\sum_{j=0}^{N}u(x_{j})P_{n}^{(\alpha,\beta)}(x_{j})w_{j}
$$

$$
\Vert P_{n}^{(\alpha,\beta)}\Vert_{N}^{2}=\begin{cases}
\Vert P_{n}^{(\alpha,\beta)}\Vert^{2} & n<N\\
\left(2+\frac{\alpha+\beta+1}{N}\right)\Vert P_{N}^{(\alpha,\beta)}\Vert^{2} & n=N
\end{cases}
$$

where,

$$
\Vert P_{n}^{(\alpha,\beta)}\Vert^{2}=\frac{2^{\alpha+\beta+1}}{2N+\alpha+\beta+1}\frac{\Gamma(N+\alpha+1)\Gamma(N+\beta+1)}{N!\Gamma(N+\alpha+\beta+1)}
$$

- Inverse Jacobi Transformation:

$$
u(x_{j})=\sum_{n=0}^{N}\tilde{u}_{n}P_{n}^{(\alpha,\beta)}(x_{j})
$$

or

$$
{\bf u}={\bf P}\tilde{{\bf u}}
$$

where,

$$
P_{ij}=P_{j}^{(\alpha,\beta)}(x_{i})
$$

$$
\tilde{{\bf u}}=\left[\tilde{u}_{0},\tilde{u}_{1},\cdots,\tilde{u}_{N}\right]^{T}
$$

$$
{\bf u}=\left[u(x_{0}),u(x_{1}),\cdots,u(x_{N})\right]^{T}
$$

Note that inverse Jacobi transform is computed by using Clenshaw algorithm.

Differentiation in physical space is performed by using $D$ matrix. The quadrature polynomial for Jacobi-Gauss-Lobatto expansion is given by:

$$
\begin{aligned}Q(x) & =\left(1-x^{2}\right)P_{N-1}^{(\alpha+1,\beta+1)}\\
 & =2\left(a_{n}+x\right)P_{n}^{(\alpha,\beta)}(x)-2b_{n}P_{n+1}^{(\alpha,\beta)}(x)
\end{aligned}
$$

where,

$$
a_{n}=\frac{\alpha-\beta}{\left(2n+\alpha+\beta+2\right)}
$$

$$
b_{n}=\frac{2n+2}{2n+\alpha+\beta+2}
$$

Let

$$
J(x)=\partial_{x}P_{N-1}^{(\alpha+1,\beta+1)}=\partial_{x}P_{N}^{\alpha+1,\beta}(x)-\partial_{x}P_{N}^{\alpha,\beta+1}(x)
$$

Then,

$$
\partial_{x}Q(x_{j})=\begin{cases}
\frac{2\Gamma(N+\beta+1)}{(-1)^{N-1}\Gamma(N)\Gamma(\beta+2)} & j=0\\
(1-x_{j}^{2})J(x_{j}) & j=1,\cdots,N-1\\
\frac{-2\Gamma(N+\alpha+1)}{\Gamma(N)\Gamma(\alpha+2)} & j=N
\end{cases}
$$

$$
\partial_{x}^{2}Q(x_{j})=\begin{cases}
\frac{2\left[\alpha-N(N+\alpha+\beta+1)\right]\Gamma(N+\beta+1)}{(-1)^{N+1}\Gamma(N)\Gamma(\beta+3)} & j=0\\
\left[\alpha-\beta+\left(\alpha+\beta\right)x_{j}\right]J(x_{j}) & j=1,\cdots,N-1\\
\frac{2\left[\beta-N(N+\alpha+\beta+1)\right]\Gamma(N+\alpha+1)}{\Gamma(N)\Gamma(\alpha+3)} & j=N
\end{cases}
$$

Zeroth column of $D$ matrix is given by:

$$
D_{i0}=\begin{cases}
\frac{\alpha-N(N+\alpha+\beta+1)}{2(\beta+2)} & i=0\\
\frac{\left(-1\right)^{N-1}\Gamma(N)\Gamma(\beta+2)}{2\Gamma(N+\beta+1)}\left(1-x_{i}\right)J(x_{i}) & i=1,\cdots,N-1\\
\frac{\left(-1\right)^{N}}{2}\frac{\Gamma(\beta+2)\Gamma(N+\alpha+1)}{\Gamma(N+\beta+1)\Gamma(\alpha+2)} & i=N
\end{cases}
$$

The last column of $D$ matrix is given by:

$$
D_{iN}=\begin{cases}
\frac{\left(-1\right)^{N+1}}{2}\frac{\Gamma(\alpha+2)\Gamma(N+\beta+1)}{\Gamma(N+\alpha+1)\Gamma(\beta+2)} & i=0\\
\frac{\Gamma(N)\Gamma(\alpha+2)}{2\Gamma(N+\alpha+1)}\left(1+x_{i}\right)J(x_{i}) & i=1,\cdots,N-1\\
\frac{-\beta+N(N+\alpha+\beta+1)}{2(\alpha+2)} & i=N
\end{cases}
$$

Columns 1 to $N-1$ of $D$ matrix are given by:

$$
D_{ij}=\begin{cases}
\frac{2\left(-1\right)^{N}\Gamma(N+\beta+1)}{\Gamma(N)\Gamma(\beta+2)(1-x_{j})(1+x_{j})^{2}J(x_{j})} & i=0\\
\frac{(1-x_{i}^{2})J(x_{i})}{(1-x_{j}^{2})J(x_{j})}\frac{1}{\left(x_{i}-x_{j}\right)} & i\ne j,i=1,\cdots,N-1\\
\frac{\alpha-\beta+(\alpha+\beta)x_{i}}{2(1-x_{i}^{2})} & i=j=1,\cdots,N-1\\
\frac{-2\Gamma(N+\alpha+1)}{\Gamma(N)\Gamma(\alpha+2)(1-x_{j})^{2}(1+x_{j})J(x_{j})} & i=N
\end{cases}
$$

# Jacobi Gauss expansion

- Jacobi Transformation:

$$
\tilde{u}_{n}=\frac{1}{\Vert P_{n}^{(\alpha,\beta)}\Vert^{2}}\sum_{j=0}^{N}u(x_{j})P_{n}^{(\alpha,\beta)}(x_{j})w_{j}
$$

- Inverse Jacobi Transformation:

$$
u(x_{j})=\sum_{n=0}^{N}\tilde{u}_{n}P_{n}^{(\alpha,\beta)}(x_{j})
$$

or

$$
{\bf u}={\bf P}\tilde{{\bf u}}
$$

Differentiation in physical space is performed by using $D$ matrix. The quadrature polynomial for Jacobi-Gauss expansion is given by:

$$
\begin{aligned}Q(x) & =P_{N+1}^{(\alpha,\beta)}\end{aligned}
$$

$$
D_{ij}=\begin{cases}
\frac{\partial_{x}P_{N+1}^{(\alpha,\beta)}(x_{i})}{\partial_{x}P_{N+1}^{(\alpha,\beta)}(x_{j})}\frac{1}{x_{i}-x_{j}} & 0\le i\ne j\le N\\
\frac{\alpha-\beta+(\alpha+\beta+2)x_{i}}{2(1-x_{i}^{2})} & 0\le i=j\le N
\end{cases}
$$
