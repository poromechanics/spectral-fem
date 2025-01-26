# Legendre Polynomial Expansion

## Continuous expansion

Legendre polynomial can be obtained from Ultraspherical polynomial, by using $\lambda=0.5$. The continuous Legendre expansion is given by

$$
u(x)=\sum_{n=0}^{\infty}\hat{u}_{n}P_{n}(x)
$$

with the following expansion coefficients,

$$
\hat{u}_{n}=\frac{1}{\Vert P_{n}\Vert^{2}}\int_{-1}^{+1}u(x)P_{n}(x)dx
$$

where,

$$
\Vert P_{n}\Vert^{2}=\frac{2}{2n+1}
$$

The $m$th derivative of $u(x)$ has a similar expansion with coefficients $\hat{u}_{n}^{(m)}$:

$$
\partial_{x}^{m}u(x)=\sum_{n=0}^{\infty}\hat{u}_{n}^{(m)}P_{n}^{(\lambda)}(x)
$$

The relation between $\hat{u}_{n}$ and $\hat{u}_{n}^{(1)}$ is given below:

$$
\hat{u}_{n}=\frac{\hat{u}_{n-1}^{(1)}}{\left(2n-1\right)}-\frac{\hat{u}_{n+1}^{(1)}}{\left(2n+3\right)}
$$

Similarly,

$$
\hat{u}_{n}^{(m-1)}=\frac{\hat{u}_{n-1}^{(m)}}{\left(2n-1\right)}-\frac{\hat{u}_{n+1}^{(m)}}{\left(2n+3\right)}
$$

Therefore, one can easily compute the expansion coefficient of the function from the expansion coefficients of its derivative.


## Truncated expansion

In practice, we consider expansion of $u(x)$ by using the finite number of polynomials $P_{n}(x)$ with $n\le N$,

$$
\mathcal{P}_{N}u(x)=\sum_{n=0}^{N}\hat{u}_{n}P_{n}(x)
$$

In this way, $\mathcal{P}_{N}u(x)$ denotes the projection of $u(x)$ on $\mathcal{P}_{N}$, therefore, $\hat{u}_{n}=0,\forall n>N$.

Let us now consider the first derivative of $u$.

$$
\mathcal{P}_{N}\frac{du(x)}{dx}=\sum_{n=0}^{N}\hat{u}_{n}^{(1)}P_{n}(x),
$$

with $\hat{u}_{n}^{(1)}=0,\forall n>N$ and $\mathcal{P}_{N}\frac{du(x)}{dx}\in\mathcal{P}_{N-1}$. We can obtain coefficients of derivative from backward subtitution.

$$
\hat{u}_{n-1}^{(m)}=\left(\frac{2n-1}{2n+3}\right)\hat{u}_{n+1}^{(m)}+\left(2n-1\right)\hat{u}_{n}^{(m-1)},\text{with }\hat{u}_{N}^{(m)}=0
$$

## Discrete expansion

Let $\left\{ x_{j},w_{j}\right\} _{j=0}^{N}$ be a set of Gauss, Gauss-Radau or Gauss-Lobatto quadrature nodes and weights. The discrete Legendre polynomial expansion is given by (_Inverse Legendre Transform_):

$$
\mathcal{I}_{N}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}P_{n}(x)
$$

where $\tilde{u}_{n}$ are the coefficients of discrete polynomial expansion compute by Forward Discrete Legendre Transform (or_Legendre Transform_ation):

$$
\tilde{u}_{n}=\frac{1}{\Vert P_{n}\Vert_{N}^{2}}\sum_{j=0}^{N}u(x_{j})P_{n}(x_{j})w_{j}
$$

- It is noteworthy that $\Vert P_{n}\Vert_{N}^{2}$ would be exact for Gauss and Gauss-Radau quadratures, but it would be approximate for Gauss-Lobatto points.

- $\left\{ u(x_{j})\right\}_{j=0}^{N}$ denotes value of $u$ at quadrature points, we will refer it to nodal-values in physical space, or simply nodal values of $u$.

- $\left\{ \tilde{u}_{n}\right\}_{n=0}^{N}$ denotes the coefficient of polynomial expansion, we will refer it to modal-values in frequency space, or simply modal values $u$.

If $f\in\mathcal{P}_{N}$ then, the $f^{2}\in\mathcal{P}_{2N}$, therefore, $N+1$ Gauss-Quadrature points and Gauss-Radau points are enough for computing the norm. However, Gauss-Lobatto points are not enough to compute the norm. In practice, Gauss-Lobatto rules are very useful as they include boundary nodes. Thanks to following lemma we can compute the equivalent norm by using the Gauss-Lobatto points.

## Differentiation in physical space

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

- If the $N+1$ quadrature points are zeros of polynomial $Q\in\mathcal{P}_{N+1}$, ($Q$ is also called the quadrature polynomial) then Lagrange polynomial and $D_{ij}$ are given by:

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
P_{N+1}(x) & \text{Gauss}\\
P_{N+1}(x)-\frac{P_{N+1}(a)}{P_{N}(a)}P_{N}(x) & \text{Gauss-Radau}\\
P_{N+1}(x)+\alpha_{N}P_{N}(x)+\beta_{N}P_{N-1}(x) & \text{Gauss-Lobatto}
\end{cases}
$$

In the case of Gauss-Radau $a\in\left\{ -1,1\right\} ,$and in the case of Gauss-Lobatto, $\alpha_{N}$ and $\beta_{N}$ are obtained by solving following 2×2 system of equations:

$$
\left[\begin{array}{cc}
P_{N}(-1) & P_{N-1}(-1)\\
P_{N}(1) & P_{N-1}(1)
\end{array}\right]\left\{ \begin{array}{c}
\alpha_{N}\\
\beta_{N}
\end{array}\right\} =-\left\{ \begin{array}{c}
P_{N+1}(-1)\\
P_{N+1}(+1)
\end{array}\right\}
$$

- The $m$th order derivative of $u$ at quadrature point is given by:

$$
\frac{d^{m}{\bf u}}{dx^{m}}={\bf D}^{m}{\bf u}
$$

## Derivative in frequency space

The process of Differentiation in the frequency space is relatively simpler than that in the physical space. In the frequency space, $\mathcal{I}_{N}u(x)\in\mathcal{P}_{N}$,

$$
\mathcal{I}_{N}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}P_{n}(x)
$$

and $\mathcal{I}_{N}\frac{d}{dx}u(x)\in P_{N-1}$

$$
\mathcal{I}_{N}\frac{d}{dx}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}\frac{d}{dx}P_{n}(x)=\sum_{n=0}^{N}\tilde{u}_{n}^{(1)}P_{n}(x)
$$

where, $\tilde{u}_{n}^{(1)}$ are the modal coefficients for first derivative, and $\tilde{u}_{N}^{(1)}=0$. We can use following **backward subtitution algorithm** to get $\left\{ \tilde{u}_{n}^{(1)}\right\}_{n=0}^{N}$from $\left\{ \tilde{u}_{n}\right\}_{n=0}^{N}$:

1. Initialization: $\tilde{u}_{N}^{(1)}=0$, $\tilde{u}_{N-1}^{(1)}=\left(2N-1\right)\tilde{u}_{N}$

2. For $n=N-1,\cdots,1$: $\tilde{u}_{n-1}^{(1)}=\left(2n-1\right)\tilde{u}_{n}+\left(\frac{2n-1}{2n+3}\right)\tilde{u}_{n+1}^{(1)}$

## Legendre Gauss-Lobatto expansion

- Legendre transformation

$$
\tilde{u}_{n}=\frac{1}{\Vert P_{n}\Vert_{N}^{2}}\sum_{i=0}^{N}u(x_{i})P_{n}(x_{i})w_{i}
$$

$$
\Vert P_{n}\Vert_{N}^{2}=\begin{cases}
\frac{2}{2n+1} & n<N\\
\frac{2}{N} & n=N
\end{cases}
$$

- Inverse Legendre Transformation:

$$
\mathcal{I}_{N}u(x)=\sum_{i=0}^{N}\tilde{u}_{i}P_{i}(x)
$$

Differentiation in physical space is performed by using $D$ matrix, which is given below.

$$
D_{ij}=\begin{cases}
-\frac{N(N+1)}{4} & i=j=0\\
0 & i=j\in[1,\cdots,N-1]\\
\frac{P_{N}(x_{i})}{P_{N}(x_{j})}\frac{1}{x_{i}-x_{j}} & i\ne j\\
\frac{N(N+1)}{4} & i=j=N
\end{cases}
$$

## Legendre Gauss Expansion

- Legendre transformation

$$
\tilde{u}_{n}=\frac{1}{\Vert P_{n}\Vert_{N}^{2}}\sum_{i=0}^{N}u(x_{i})P_{n}(x_{i})w_{i}
$$

$$
\Vert P_{n}\Vert_{N}^{2}=\Vert P_{n}\Vert^{2}=\frac{2}{2n+1}
$$

- Inverse Legendre Transformation:

$$
\mathcal{I}_{N}u(x)=\sum_{i=0}^{N}\tilde{u}_{i}P_{i}(x)
$$

Differentiation in physical space is performed by using $D$ matrix.

$$
D_{ij}=\begin{cases}
\frac{x_{i}}{1-x_{i}^{2}} & i=j\\
\frac{1}{x_{i}-x_{j}}\frac{\partial_{x}P_{N+1}(x_{i})}{\partial_{x}P_{N+1}(x_{j})} & i\ne j
\end{cases}
$$

## Legendre Gauss-Radau Expansion

- Legendre transformation

$$
\tilde{u}_{n}=\frac{1}{\Vert P_{n}\Vert_{N}^{2}}\sum_{i=0}^{N}u(x_{i})P_{n}(x_{i})w_{i}
$$

$$
\Vert P_{n}\Vert_{N}^{2}=\Vert P_{n}\Vert^{2}=\frac{2}{2n+1}
$$

- Inverse Legendre Transformation:

$$
\mathcal{I}_{N}u(x)=\sum_{i=0}^{N}\tilde{u}_{i}P_{i}(x)
$$
