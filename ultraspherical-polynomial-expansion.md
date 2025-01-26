# Ultraspherical Polynomial Expansion


# Continuous expansion

Let $u(x)$ be any continuous function defined over $\left[-1,1\right]$ and $P_{n}^{(\lambda)}(x)$ be an ultraspherical polynomial of degree $n$ and $\lambda>-\frac{1}{2}$ . Then the continuous polynomial expansion of $u$ in terms of ultraspherical polynomials is given by:

$$
u(x)=\sum_{n=0}^{\infty}\hat{u}_{n}P_{n}^{(\lambda)}(x)
$$

with the following expansion coefficients,

$$
\hat{u}_{n}=\frac{1}{\Vert P_{n}^{(\lambda)}\Vert^{2}}\int_{-1}^{+1}u(x)P_{n}^{(\lambda)}(x)\left(1-x^{2}\right)^{\lambda-\frac{1}{2}}dx
$$

where,

$$
\Vert P_{n}^{(\lambda)}\Vert^{2}=\left(2^{1-2\lambda}\right)\frac{\pi}{\left[\Gamma(\lambda)\right]^{2}}\frac{\Gamma\left(n+2\lambda\right)}{\left(n+\lambda\right)\Gamma\left(n+1\right)}
$$

The $m$th derivative of $u(x)$ has a similar expansion with coefficients $\hat{u}_{n}^{(m)}$:

$$
\partial_{x}^{m}u(x)=\sum_{n=0}^{\infty}\hat{u}_{n}^{(m)}P_{n}^{(\lambda)}(x)
$$

Now, we should ask, "what is the relation between $\hat{u}_{n}^{(m)}$ and $\hat{u}_{n}^{(m-1)}$?" To get the answer let us start with the first derivative, that is, $m=1$.

$$
\partial_{x}u(x)=\sum_{n=0}^{\infty}\hat{u}_{n}^{(1)}P_{n}^{(\lambda)}(x)=\sum_{n=0}^{\infty}\hat{u}_{n}\partial_{x}P_{n}^{(\lambda)}(x)
$$

From the previous chapter, we know that,

$$
P_{n}^{(\lambda)}=\frac{1}{2\left(n+\lambda\right)}\frac{d}{dx}\left(P_{n+1}^{(\lambda)}-P_{n-1}^{(\lambda)}\right)
$$

Hence,

$$
\partial_{x}u(x)=\sum_{n=0}^{\infty}\hat{u}_{n}^{(1)}\frac{1}{2\left(n+\lambda\right)}\frac{dP_{n+1}^{(\lambda)}}{dx}-\sum_{n=0}^{\infty}\hat{u}_{n}^{(1)}\frac{1}{2\left(n+\lambda\right)}\frac{dP_{n-1}^{(\lambda)}}{dx}
$$

Now note that

$$
\frac{dP_{-1}^{(\lambda)}}{dx}=\frac{dP_{0}^{(\lambda)}}{dx}=0
$$

hence,

$$
\partial_{x}u(x)=\sum_{n=0}^{\infty}\hat{u}_{n}^{(1)}\frac{1}{2\left(n+\lambda\right)}\frac{dP_{n+1}^{(\lambda)}}{dx}-\sum_{n=2}^{\infty}\hat{u}_{n}^{(1)}\frac{1}{2\left(n+\lambda\right)}\frac{dP_{n-1}^{(\lambda)}}{dx}
$$

or,

$$
\partial_{x}u(x)=\sum_{n=0}^{\infty}\left(\frac{\hat{u}_{n-1}^{(1)}}{2\left(n+\lambda-1\right)}-\frac{\hat{u}_{n+1}^{(1)}}{2\left(n+\lambda+1\right)}\right)\frac{dP_{n}^{(\lambda)}}{dx}
$$

Therefore,

$$
\hat{u}_{n}=\frac{\hat{u}_{n-1}^{(1)}}{2\left(n+\lambda-1\right)}-\frac{\hat{u}_{n+1}^{(1)}}{2\left(n+\lambda+1\right)}
$$

Similarly,

$$
\hat{u}_{n}^{(m-1)}=\frac{\hat{u}_{n-1}^{(m)}}{2\left(n+\lambda-1\right)}-\frac{\hat{u}_{n+1}^{(m)}}{2\left(n+\lambda+1\right)}
$$

Therefore, one can easily compute the expansion coefficient of the function from the expansion coefficients of its derivative. We can invert this relationship to get the coefficient of derivative from the expansion coefficient of the functions.

$$
\hat{u}_{n}^{(m)}=\left(2n+\lambda\right)\sum_{\begin{aligned}p=n+1\\
n+p\text{ odd}
\end{aligned}
}^{\infty}\hat{u}_{p}^{(m-1)}
$$

# Truncated expansion

In practice, we consider expansion of $u(x)$ by using the finite number of polynomials $P_{n}^{(\lambda)}(x)$ with $n\le N$,

$$
\mathcal{P}_{N}u(x)=\sum_{n=0}^{N}\hat{u}_{n}P_{n}^{(\lambda)}(x)
$$

In this way, $\mathcal{P}_{N}u(x)$ denotes the projection of $u(x)$ on ${\bf \mathcal{P}}_{N}$, therefore, $\hat{u}_{n}=0,\forall n>N$.

Let us now consider the first derivative of $u$.

$$
\mathcal{P}_{N}\frac{du(x)}{dx}=\sum_{n=0}^{N}\hat{u}_{n}^{(1)}P_{n}^{(\lambda)}(x),
$$

with $\hat{u}_{n}^{(1)}=0,\forall n>N$. Therefore,

$$
\hat{u}_{N}^{(1)}:=\left(2N+\lambda\right)\sum_{\begin{aligned}p=N+1\\
N+p\text{ odd}
\end{aligned}
}^{\infty}\hat{u}_{p}=0
$$

It means $\mathcal{P}_{N}\frac{du(x)}{dx}\in\mathcal{P}_{N-1}$. Then, we can obtain coefficients of derivative from backward subtitution.

$$
\hat{u}_{n-1}^{(m)}=\left(\frac{n+\lambda-1}{n+\lambda+1}\right)\hat{u}_{n+1}^{(m)}+2\left(n+\lambda-1\right)\hat{u}_{n}^{(m-1)},\text{with }\hat{u}_{N}^{(m)}=0
$$

- **Theorem**: For any $u(x)\in H_{w}^{p}\left[-1,1\right]$, $p\ge0$, there exists a constant $C$, independent of N, such that:

$$
\Vert u-\mathcal{P}_{N}u\Vert_{L_{w}^{2}\left[-1,1\right]}\le CN^{-p}\Vert u\Vert_{H_{w}^{p}\left[-1,1\right]}
$$

According to this theorem, the error in $u$ decays spectrally in weighted $L^{2}$ norm.

- **Theorem**: Let $u(x)\in H_{w}^{p}\left[-1,1\right]$; there exists a constant $C$, independent of N, such that:

$$
\Vert\mathcal{P}_{N}\frac{du}{dx}-\frac{d}{dx}\mathcal{P}_{N}u\Vert_{H_{w}^{q}\left[-1,1\right]}\le CN^{2q-p+3/2}\Vert u\Vert_{H_{w}^{p}\left[-1,1\right]},\quad0\le q\le p
$$

According to this theorem, the error in $u$ decays spectrally in weighted Sobolev norm.

- **Theorem**: For any $u(x)\in H_{w}^{p}\left[-1,1\right]$; there exists a constant $C$, independent of N, such that:

$$
\Vert u-\mathcal{P}_{N}u\Vert_{H_{w}^{q}\left[-1,1\right]}\le CN^{\sigma(q,p)}\Vert u\Vert_{H_{w}^{p}\left[-1,1\right]},\quad0\le q\le p
$$

where,

$$
\sigma(q,p)=\begin{cases}
\frac{3}{2}q-p & 0\le q\le1\\
2q-p-\frac{1}{2} & q\ge1
\end{cases}
$$

According to this theorem, the error in $u$ decays spectrally in weighted Sobolev norm.

# Discrete expansion

Let $\left\{ x_{j},w_{j}\right\} _{j=0}^{N}$ be a set of Gauss, Gauss-Radau or Gauss-Lobatto quadrature nodes and weights. The discrete Ultraspherical polynomial expansion is given by Inverse Discrete Ultraspherical Transform (or_Inverse Ultraspherical Transform_):

$$
\mathcal{I}_{N}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}P_{n}^{(\lambda)}(x)
$$

where $\tilde{u}_{n}$ are the coefficients of discrete polynomial expansion compute by Forward Discrete Ultraspherical Transform (or_Ultraspherical Transform_):

$$
\tilde{u}_{n}=\frac{1}{\Vert P_{n}^{(\lambda)}\Vert_{N}^{2}}\sum_{j=0}^{N}u(x_{j})P_{n}^{(\lambda)}(x_{j})w_{j}
$$

- It is noteworthy that $\Vert P_{n}^{(\lambda)}\Vert_{N}^{2}$ would be exact for Gauss and Gauss-Radau quadratures, but it would be approximate for Gauss-Lobatto points.

- $\left\{ u(x_{j})\right\}_{j=0}^{N}$ denotes value of $u$ at quadrature points, we will refer it to nodal-values in physical space, or simply nodal values of $u$.

- $\left\{ \tilde{u}_{n}\right\}_{n=0}^{N}$ denotes the coefficient of polynomial expansion, we will refer it to modal-values in frequency space, or simply modal values $u$.

If $f\in\mathcal{P}_{N}$ then, the $f^{2}\in\mathcal{P}_{2N}$, therefore, $N+1$ Gauss-Quadrature points and Gauss-Radau points are enough for computing the norm. However, Gauss-Lobatto points are not enough to compute the norm. In practice, Gauss-Lobatto rules are very useful as they include boundary nodes. Thanks to following lemma we can compute the equivalent norm by using the Gauss-Lobatto points.

- **Lemma**: Let $\left\{ x_{i}\right\}_{i=1}^{N-1}$ be the $N-1$ interior Gauss-Lobatto points, then the ultraspherical polynomials, $P_{N}^{(\lambda)}$ satisfy

>
$$
\frac{d}{dx}P_{N-1}^{(\lambda)}(x_{i})=-NP_{N}^{(\lambda)}(x_{j})\quad\forall j\in\left[1,\cdots,N-1\right],
$$

The proof is direct by noting that

>
$$
nP_{n}^{(\lambda)}=x\frac{dP_{n}^{(\lambda)}}{dx}-\frac{dP_{n-1}^{(\lambda)}}{dx}
$$

and $\left\{ x_{i}\right\}_{i=1}^{N-1}$ are zeros of $\frac{dP_{N}^{(\lambda)}}{dx}$. Therefore, the discrete norm $\Vert P_{N}^{(\lambda)}\Vert_{N}$ by using **Gauss-Lobatto** points:

$$
\Vert P_{N}^{(\lambda)}\Vert_{N}^{2}=\frac{1}{N^{2}}\sum_{i=0}^{N}\left(\frac{d}{dx}P_{N-1}^{(\lambda)}(x_{i})\right)^{2}w_{i}
$$

Note that

$$
\frac{dP_{N-1}^{\left(\lambda\right)}}{dx}=2\lambda P_{N-2}^{\left(\lambda+1\right)}
$$

Hence,

$$
\Vert P_{N}^{(\lambda)}\Vert_{N}^{2}=\frac{1}{N^{2}}\left\Vert \frac{dP_{N-1}^{(\lambda)}}{dx}\right\Vert_{N}^{2}=\frac{4\lambda^{2}}{N^{2}}\left\Vert P_{N-2}^{\left(\lambda+1\right)}\right\Vert_{N}^{2}=2^{2\lambda}\frac{\Gamma^{2}(\lambda+\frac{1}{2})\Gamma(N+2\lambda)}{NN!\Gamma^{2}(2\lambda)}
$$

# Differentiation in physical space

In the physical space, we can write the discrete Ultraspherical expansion by using the Lagrange polynomials with interpolation points as the Gauss quadrature points $\left\{ x_{j}\right\}_{j=0}^{N}$.

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
P_{N+1}^{(\lambda)}(x) & \text{Gauss}\\
P_{N+1}^{(\lambda)}(x)-\frac{P_{N+1}^{(\lambda)}(a)}{P_{N}^{(\lambda)}(a)}P_{N}^{(\lambda)}(x) & \text{Gauss-Radau}\\
P_{N+1}^{(\lambda)}(x)+\alpha_{N}P_{N}^{(\lambda)}(x)+\beta_{N}P_{N-1}^{(\lambda)}(x) & \text{Gauss-Lobatto}
\end{cases}
$$

In the case of Gauss-Radau $a\in\left\{ -1,1\right\} ,$and in the case of Gauss-Lobatto, $\alpha_{N}$ and $\beta_{N}$ are obtained by solving following 2×2 system of equations:

$$
\left[\begin{array}{cc}
P_{N}^{(\lambda)}(-1) & P_{N-1}^{(\lambda)}(-1)\\
P_{N}^{(\lambda)}(1) & P_{N-1}^{(\lambda)}(1)
\end{array}\right]\left\{ \begin{array}{c}
\alpha_{N}\\
\beta_{N}
\end{array}\right\} =-\left\{ \begin{array}{c}
P_{N+1}^{(\lambda)}(-1)\\
P_{N+1}^{(\lambda)}(+1)
\end{array}\right\}
$$

- The $m$th order derivative of $u$ at quadrature point is given by:

$$
\frac{d^{m}{\bf u}}{dx^{m}}={\bf D}^{m}{\bf u}
$$

# Differentiation in frequency space

The process of Differentiation in the frequency space is relatively simpler than that in the physical space. In the frequency space, $\mathcal{I}_{N}u(x)\in\mathcal{P}_{N}$,

$$
\mathcal{I}_{N}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}P_{n}^{(\lambda)}(x)
$$

and $\mathcal{I}_{N}\frac{d}{dx}u(x)\in P_{N-1}$

$$
\mathcal{I}_{N}\frac{d}{dx}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}\frac{d}{dx}P_{n}^{(\lambda)}(x)=\sum_{n=0}^{N}\tilde{u}_{n}^{(1)}P_{n}^{(\lambda)}(x)
$$

where, $\tilde{u}_{n}^{(1)}$ are the modal coefficients for first derivative, and $\tilde{u}_{N}^{(1)}=0$. We can use following **backward subtitution algorithm** to get $\left\{ \tilde{u}_{n}^{(1)}\right\}_{n=0}^{N}$from $\left\{ \tilde{u}_{n}\right\}_{n=0}^{N}$:

1. Initialization: $\tilde{u}_{N}^{(1)}=0$, $\tilde{u}_{N-1}^{(1)}=2\left(N+\lambda-1\right)\tilde{u}_{N}$

2. For $n=N-1,\cdots,1$: $\tilde{u}_{n-1}^{(1)}=2\left(n+\lambda-1\right)\tilde{u}_{n}+\left(\frac{n+\lambda-1}{n+\lambda+1}\right)\tilde{u}_{n+1}^{(1)}$

# Ultraspherical Gauss-Lobatto expansion

- Ultraspherical Transformation:

$$
\tilde{u}_{n}=\frac{1}{\Vert P_{n}^{(\lambda)}\Vert_{N}^{2}}\sum_{j=0}^{N}u(x_{j})P_{n}^{(\lambda)}(x_{j})w_{j}
$$

$$
\Vert P_{n}^{(\lambda)}\Vert_{N}^{2}=\begin{cases}
\Vert P_{n}^{(\lambda)}\Vert^{2} & n<N\\
2\left(\frac{N+\lambda}{N}\right)\Vert P_{N}^{(\lambda)}\Vert^{2} & n=N
\end{cases}
$$

where,

$$
\Vert P_{n}^{(\lambda)}\Vert^{2}=\left(2^{1-2\lambda}\right)\frac{\pi}{\left[\Gamma(\lambda)\right]^{2}}\frac{\Gamma\left(n+2\lambda\right)}{\left(n+\lambda\right)\Gamma\left(n+1\right)}
$$

- Inverse Ultraspherical Transformation:

$$
u(x_{j})=\sum_{n=0}^{N}\tilde{u}_{n}P_{n}^{(\lambda)}(x_{j})
$$

Note that the inverse Jacobi transform is computed by using Clenshaw algorithm. Differentiation in physical space is performed by using $D$ matrix, which is given below.

$$
D_{ij}=\begin{cases}
\frac{\lambda-0.5-N(N+2\lambda)}{(2\lambda+3)} & i=j=0\\
\frac{\left(\lambda-0.5\right)x_{i}}{\left(1-x_{i}^{2}\right)} & i=j=1,\cdots,N-1\\
-D_{00} & i=j=N\\
\frac{\lambda+0.5}{x_{i}-x_{j}}\frac{P_{N}^{(\lambda)}(x_{i})}{P_{N}^{(\lambda)}(x_{j})} & i\ne j,j=0,N\\
\frac{1}{x_{i}-x_{j}}\frac{P_{N}^{(\lambda)}(x_{i})}{P_{N}^{(\lambda)}(x_{j})} & i\ne j=1,\cdots,N-1
\end{cases}
$$

Ultraspherical-Gauss-Lobatto differentiation matrix is centro-symmetric:

$$
D_{ij}=-D_{N-i,N-j}
$$

This centro-symmetric corresponds to the property that if the vector containing function value is reversed, that is, $(u_{0},u_{1}\cdots,u_{N})$ is replaced by $(u_{N},u_{N-1}\cdots,u_{0})$, then the derivative is reversed and also multiply by $-1$. This property can be used to develop fast differentiation algorithms. Let ${\bf u}$ be the vector (in $R^{N+1}$) of nodal values (Lobatto points) of function $u(x)$. Let us consider that $N$ is odd. So

$$
{\bf u}={\bf e}+{\bf o}
$$

where,

$$
e_{i}=\frac{1}{2}\left(u_{i}+u_{N-i}\right),i=0,1,\cdots,N
$$

$$
e_{i}=\frac{1}{2}\left(u_{i}-u_{N-i}\right),i=0,1,\cdots,N
$$

Note that

$$
e_{i}=e_{N-i}
$$

$$
o_{i}=-o_{N-i}
$$

Now we can write differentiation in physical space as:

$$
{\bf u}^{(1)}={\bf D}{\bf u}={\bf D}{\bf e}+{\bf D}{\bf o}={\bf e}'+{\bf o}'
$$

where, $\forall i=0,1,\cdots,N/2$

$$
e'_{i}=\sum_{j=0}^{N/2}\left(D_{ij}+D_{i,N-j}\right)e_{j}
$$

$$
e'_{N-i}=-e_{i}'
$$

$$
o'_{i}=\sum_{j=0}^{N/2}\left(D_{ij}-D_{i,N-j}\right)o_{j}
$$

$$
o'_{N-i}=o_{i}'
$$

Therefore,$\forall i=0,1,\cdots,N/2$

$$
u_{i}'=e'_{i}+o'_{i}
$$

$$
u'_{N-i}=-e'_{i}+o'_{i}
$$

# Ultraspherical Gauss expansion

- Ultraspherical transformation:

$$
\tilde{u}_{n}=\frac{1}{\Vert P_{n}^{(\lambda)}\Vert^{2}}\sum_{j=0}^{N}u(x_{j})P_{n}^{(\lambda)}(x_{j})w_{j}
$$

- Inverse Ultraspherical transformation:

$$
u(x_{j})=\sum_{n=0}^{N}\tilde{u}_{n}P_{n}^{(\lambda)}(x_{j})
$$

Differentiation in physical space is performed by using $D$ matrix.

$$
D_{ij}=\begin{cases}
\frac{\partial_{x}P_{N+1}^{(\lambda)}(x_{i})}{\partial_{x}P_{N+1}^{(\lambda)}(x_{j})}\frac{1}{x_{i}-x_{j}} & 0\le i\ne j\le N\\
\frac{\left(\lambda+0.5\right)x_{i}}{\left(1-x_{i}^{2}\right)} & 0\le i=j\le N
\end{cases}
$$

# Ultraspherical Gauss-Radau expansion

- Ultraspherical transformation:

$$
\tilde{u}_{n}=\frac{1}{\Vert P_{n}^{(\lambda)}\Vert^{2}}\sum_{j=0}^{N}u(x_{j})P_{n}^{(\lambda)}(x_{j})w_{j}
$$

- Inverse Ultraspherical transformation:

$$
u(x_{j})=\sum_{n=0}^{N}\tilde{u}_{n}P_{n}^{(\lambda)}(x_{j})
$$
