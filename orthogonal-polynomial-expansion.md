---
sidebar_position: 1
---

# Orthogonal Polynomial expansions

# Continuous expansion

Let $u(x)$ be any continuous function defined over $\left[-1,1\right]$ and $p_{n}(x)$ be an orthogonal polynomial of degree $n$ and $\lambda>-\frac{1}{2}$ . Then the continuous polynomial expansion of $u$ in terms of $p_{n}(x)$ is given by:

$$
u(x)=\sum_{n=0}^{\infty}\hat{u}_{n}p_{n}(x)
$$

where,

$$
\hat{u}_{n}=\frac{1}{\Vert p_{n}\Vert^{2}}\int_{-1}^{+1}u(x)p_{n}(x)w(x)dx
$$

The $m$th derivative of $u(x)$ has a similar expansion with coefficients $\hat{u}_{n}^{(m)}$:

$$
\partial_{x}^{m}u(x)=\sum_{n=0}^{\infty}\hat{u}_{n}^{(m)}p_{n}(x)
$$

# Truncated expansion

In practice, we employ truncated polynomial expansion by using orthognonal polynomials $\left\{ p_{n}\right\}_{n=0}^{N}$:

$$
\mathcal{P}_{N}u(x)=\sum_{n=0}^{N}\hat{u}_{n}p_{n}(x)
$$

where,

$$
\hat{u}_{n}=\frac{1}{\Vert p_{n}\Vert^{2}}\int_{-1}^{+1}u(x)p_{n}(x)w(x)dx
$$

The $m$th derivative of $u(x)$ in the frequency space is given by:

$$
\mathcal{P}_{N}\partial_{x}^{m}u(x)=\sum_{n=0}^{N}\hat{u}_{n}^{(m)}p_{n}(x)
$$

The $m$th derivative of $u(x)$ in the physical space is given by:

$$
\mathcal{P}_{N}\partial_{x}^{m}u(x)=\sum_{j=0}^{N}\hat{u}_{n}\partial_{x}^{m}l_{j}(x)
$$

where, $l_{j}(x)$ is the Lagrange polynomial of order $N$ (the details are given in forthcoming sections).


# Discrete expansion

Let $\left\{ x_{j},w_{j}\right\} _{j=0}^{N}$ be a set of Gauss, Gauss-Radau or Gauss-Lobatto quadrature nodes and weights. Let $f,g\in L_{w}^{2}\left[-1,1\right]$, then we can use the quadrature points to evaluate the discrete inner product and norm as:

$$
\left(f,g\right)_{w}=\int_{-1}^{+1}f(x)g(x)w(x)dx\Rightarrow\left(f,g\right)_{w,N}=\sum f(x_{i})g(x_{i})w_{i}
$$

$$
\Vert f\Vert_{w}^{2}=\left(f,f\right)_{w}\Rightarrow\Vert f\Vert_{w,N}^{2}=\sum_{i=0}^{N}f(x_{i})g(x_{i})w_{i}
$$

where, $\left(f,g\right)_{w,N}$ and $\Vert f\Vert_{w,N}^{2}$ are the discrete inner product and discrete norm.

- Note that discrete inner products and norms are approximation to their continuous counterparts, and the exactness of Gauss-type quadrature rules implies:

$$
\left(f,g\right)_{w,N}=\left(f,g\right)_{w},\forall f,g\in P_{2N+q}
$$

where, $q=1,0,-1$ for Gauss, Gauss-Radau, and Gauss-Lobatto quadrature rules.

- $N+1$ Gauss-Quadrature rule is accurate upto $2N+1$ order polynomial

- $N+1$ Gauss-Radau Quadrature rule is accurate upto $2N$ order polynomial

- $N+1$ Gauss-Lobatto Quadrature rule is accurate upto $2N-1$ order polynomial

If $f\in\mathcal{P}_{N}$ then, the $f^{2}\in\mathcal{P}_{2N}$, therefore, $N+1$ Gauss points and Gauss-Radau points are enough for computing the norm. However, Gauss-Lobatto points are not enough to compute the norm. In practice, Gauss-Lobatto rules are very useful as they include boundary nodes. Thanks to following lemma we can compute the equivalent norm by using the Gauss-Lobatto points.

Now, we can describe the discrete polynomial expansion as:

$$
\mathcal{I}_{N}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}p_{n}(x)
$$

where $\tilde{u}_{n}$ are the coefficients of discrete expansion:

$$
\tilde{u}_{n}=\frac{1}{\Vert p_{n}\Vert_{N}^{2}}\sum_{j=0}^{N}u(x_{j})p_{n}(x_{j})w_{j}
$$

- It is noteworthy that $\Vert p_{N}\Vert_{N}^{2}$ would be exact for Gauss and Gauss-Radau quadratures, but it would be approximate for Gauss-Lobatto points.

- $\left\{ u(x_{j})\right\}_{j=0}^{N}$ denotes value of $u$ at quadrature points, we will refer it to nodal-values in physical space, or simply nodal values of $u$.

- $\left\{ \tilde{u}_{n}\right\}_{n=0}^{N}$ denotes the coefficient of polynomial expansion, we will refer it to modal-values in frequency space, or simply modal values $u$.

- Computing $\left\{ \tilde{u}_{n}\right\}_{n=0}^{N}$ from $\left\{ u(x_{j})\right\}_{j=0}^{N}$ will be refered to as **forward discrete polynomial transform**.

- Computing $\left\{ u(x_{j})\right\}_{j=0}^{N}$ from $\left\{ \tilde{u}_{n}\right\}_{n=0}^{N}$ will be refered to as **inverse discrete polynomial transform**.

# Cardinal function

Let $\left\{ x_{j},w_{j}\right\} _{j=0}^{N}$ defines a quadrature rule of N+1 points. Now consider the following discrete polynomial expansion:

$$
\mathcal{I}_{N}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}p_{n}(x)
$$

where,

$$
\tilde{u}_{n}=\frac{1}{\Vert p_{n}\Vert_{N}^{2}}\sum_{j=0}^{N}u(x_{j})p_{n}(x_{j})w_{j}
$$

Then,

$$
\begin{aligned}\mathcal{I}_{N}u(x) & =\sum_{n=0}^{N}\tilde{u}_{n}p_{n}(x)\\
 & =\sum_{n=0}^{N}\frac{1}{\Vert p_{n}\Vert_{N}^{2}}\sum_{j=0}^{N}u(x_{j})p_{n}(x_{j})w_{j}p_{n}(x)\\
 & =\sum_{j=0}^{N}\left(w_{j}\sum_{n=0}^{N}\frac{p_{n}(x)p_{n}(x_{j})}{\Vert p_{n}\Vert_{N}^{2}}\right)u(x_{j})\\
 & \sum_{j=0}^{N}l_{j}\left(x\right)u(x_{j})
\end{aligned}
$$

where, $l_{j}(x)$ is the generalized Lagrange polynomial (or cardinal function) satisfying $l_{j}\left(x_{i}\right)=\delta_{ij}$.

$$
l_{j}\left(x\right)=w_{j}\sum_{n=0}^{N}\frac{p_{n}(x)p_{n}(x_{j})}{\Vert p_{n}\Vert_{N}^{2}}
$$

The right hand side can be evaluated by using Christoff-Darboux formula.

$$
\sum_{n=0}^{N}\frac{p_{n}(x)p_{n}(x_{j})}{\Vert p_{n}\Vert_{N}^{2}}=\begin{cases}
\frac{1}{\Vert p_{N}\Vert_{N}^{2}}\frac{k_{N}}{k_{N+1}}\left(\frac{p_{N+1}\left(x\right)p_{N}\left(x_{j}\right)-p_{N}\left(x\right)p_{N+1}\left(x_{j}\right)}{x-x_{j}}\right) & x\ne x_{j}\\
\frac{1}{\Vert p_{N}\Vert_{N}^{2}}\frac{k_{N}}{k_{N+1}}\left[\partial_{x}p_{N+1}\left(x_{j}\right)p_{N}\left(x_{j}\right)-\partial_{x}p_{N}\left(x_{j}\right)p_{N+1}\left(x_{j}\right)\right] & x=x_{j}
\end{cases}
$$

where, $k_{N}$ is the leading coefficient of $p_{N}(x)$.

# Orthogonal projection and Aliasing error

Let $\left\{ x_{j},w_{j}\right\} _{j=0}^{N}$ defines a quadrature rule of N+1 points. Now consider the following discrete polynomial expansion:

$$
\mathcal{I}_{N}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}p_{n}(x)
$$

we have

$$
\mathcal{I}_{N}u(x_{i})=u\left(x_{i}\right)
$$

Therefore, for any continuous function $v$

$$
\left(\mathcal{I}_{N}u,v\right)_{N}=\left(u,v\right)_{N}
$$

Therefore, the interpolant $\mathcal{I}_{N}u$ is the orthognonal projection of $u$ onto $\mathbb{P}_{N}$ with respect to the discrete inner product.

In general $\tilde{u}_{n}$ are approximation of $\hat{u}_{n}$, the error in this coefficient is called the aliasing error. This is because, in discrete case

$$
\left(p_{l},p_{k}\right)_{N}\ne0,\forall l>N,k=0,1,\cdots,N
$$

Therefore, from

$$
\tilde{u}_{k}=\frac{1}{\Vert p_{n}\Vert_{N}^{2}}\left(u,p_{k}\right)_{N}\forall k=0,1,\cdots,N
$$

$$
\tilde{u}_{k}=\hat{u}_{k}+\frac{1}{\Vert p_{k}\Vert_{N}^{2}}\sum_{l>N}\left(p_{l},p_{k}\right)_{N}\hat{u}_{l},\forall k=0,1,\cdots,N
$$

This means that the $k$th coefficient of interpolant depends on the kth mode (coefficient) of $u$ and all the modes whose wavenumber is larger than $N$.

Therefore,

$$
\mathcal{I}_{N}u=\mathcal{P}_{N}u+\mathcal{R}_{N}u
$$

where,

$$
\mathcal{R}_{N}u=\sum_{k=0}^{N}\left(\frac{1}{\Vert p_{k}\Vert_{N}^{2}}\sum_{l>N}\left(p_{l},p_{k}\right)_{N}\hat{u}_{l}\right)p_{k}
$$

can be viewed as the aliasing error due to interpolation. The aliasing error is orthogonal to the truncation error $u-\mathcal{P}_{N}u$ so that

$$
\Vert u-\mathcal{I}_{N}u\Vert_{w}^{2}=\Vert u-\mathcal{P}_{N}u\Vert_{w}^{2}+\Vert\mathcal{R}_{N}u\Vert_{w}^{2}
$$

Note that aliasing error will be zero if $u\in\mathbb{P}_{N}$.

# Differentiation in physical space

In the frequency space the discrete polynomial expansion is given by finite sum of orthogonal polynomials:

$$
\mathcal{I}_{N}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}p_{n}(x)
$$

Similary, in the physical space, we can write the discrete expansion by using the Lagrange polynomials with interpolation points as the Gauss quadrature points $\left\{ x_{j}\right\}_{j=0}^{N}$.

$$
\mathcal{I}_{N}u(x)=\sum_{j=0}^{N}u(x_{j})l_{j}(x)
$$

- All Lagrange polynomials, $\left\{ l_{j}(x)\right\}_{j=0}^{N}$, are $N$ order polynomials, and $l_{j}(x_{i})=\delta_{ij}$.

- Lagrange polynomial depends upon the orthogonal polynomials and the quadrature rules. For example, for a given orthogonal polynomial family, the expression of Lagrange polynomials will be different for Gauss, Gauss-Radau, and Gauss-Lobatto polynomials.

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
\partial_{x}{\bf u}={\bf D}{\bf u}
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
p_{N+1}(x) & \text{Gauss}\\
p_{N+1}(x)-\frac{p_{N+1}(a)}{p_{N}(a)}p_{N}(x) & \text{Gauss-Radau}\\
p_{N+1}(x)+\alpha_{N}p_{N}(x)+\beta_{N}p_{N-1}(x) & \text{Gauss-Lobatto}
\end{cases}
$$

In the case of Gauss-Radau $a\in\left\{ -1,1\right\} ,$and in the case of Gauss-Lobatto, $\alpha_{N}$ and $\beta_{N}$ are obtained by solving following 2×2 system of equations:

$$
\left[\begin{array}{cc}
p_{N}(-1) & p_{N-1}(-1)\\
p_{N}(1) & p_{N-1}(1)
\end{array}\right]\left\{ \begin{array}{c}
\alpha_{N}\\
\beta_{N}
\end{array}\right\} =-\left\{ \begin{array}{c}
p_{N+1}(-1)\\
p_{N+1}(+1)
\end{array}\right\}
$$

- The $m$th order derivative of $u$ at quadrature point is given by:

$$
\partial_{x}^{m}{\bf u}={\bf D}^{m}{\bf u}
$$

# Differentiation in frequency space

The process of Differentiation in the frequency space is relatively simpler than that in the physical space. In the frequency space, $\mathcal{I}_{N}u(x)\in P_{N}$,

$$
\mathcal{I}_{N}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}p_{n}(x)
$$

and $\mathcal{I}_{N}\partial_{x}u(x)\in P_{N-1}$

$$
\mathcal{I}_{N}\partial_{x}u(x)=\sum_{n=0}^{N}\tilde{u}_{n}\partial_{x}p_{n}(x)=\sum_{n=0}^{N}\tilde{u}_{n}^{(1)}p_{n}(x)
$$

where, $\tilde{u}_{n}^{(1)}$ are the modal coefficients for first derivative, and $\tilde{u}_{N}^{(1)}=0$.

Now we want to express $\left\{ \tilde{u}_{n}^{(1)}\right\}_{n=0}^{N}$ in terms of $\left\{ \tilde{u}_{n}\right\}_{n=0}^{N}$. In the case of classical orthognonal polynomials $\left\{ \partial_{x}p_{n}(x)\right\} _{n=0}^{N}$are also orthogonal. So, we have following three-term recurrence relationship:

$$
\partial_{x}p_{n+1}(x)=\left(a_{n}^{(1)}x+b_{n}^{(1)}\right)\partial_{x}p_{n}(x)-c_{n}^{(1)}\partial_{x}p_{n-1}(x)
$$

In addition, $\left\{ p_{n}(x)\right\}_{n=0}^{N}$ satisfy:

$$
p_{n+1}(x)=\left(a_{n}x+b_{n}\right)p_{n}(x)-c_{n}p_{n-1}(x)
$$

Then,

$$
\partial_{x}p_{n+1}=a_{n}p_{n}+a_{n}x\partial_{x}p_{n}+b_{n}\partial_{x}p_{n}-c_{n}\partial_{x}p_{n-1}
$$

or

$$
\begin{aligned}p_{n} & =\frac{c_{n}}{a_{n}}\partial_{x}p_{n-1}-\left(x+\frac{b_{n}}{a_{n}}\right)\partial_{x}p_{n}+\frac{1}{a_{n}}\partial_{x}p_{n+1}\\
 & =\tilde{a}_{n}\partial_{x}p_{n-1}+\tilde{b}_{n}\partial_{x}p_{n}+\tilde{c}_{n}\partial_{x}p_{n+1}
\end{aligned}
$$

Now, we can use following **backward subtitution algorithm** to get $\left\{ \tilde{u}_{n}^{(1)}\right\}_{n=0}^{N}$from $\left\{ \tilde{u}_{n}\right\}_{n=0}^{N}$:

1. Initialization: $\tilde{u}_{N}^{(1)}=0$, $\tilde{u}_{N-1}^{(1)}=\frac{1}{\tilde{c}_{N-1}}\tilde{u}_{N}$

2. For $n=N-1,\cdots,1$: $\tilde{u}_{n-1}^{(1)}=\frac{1}{\tilde{c}_{n-1}}\left[\tilde{u}_{n}-\tilde{b}_{n}\tilde{u}_{n}^{(1)}-\tilde{a}_{n+1}\tilde{u}_{n+1}^{(1)}\right]$

Summary: Consider the nodal values in physical space, $\left\{ u(x_{j})\right\}_{j=0}^{N}$, then use Forward discrete polynomial transform to compute $\left\{ \tilde{u}_{n}\right\}_{n=0}^{N}$, then we use backward subtitution scheme to compute, $\left\{ \tilde{u}_{n}^{(1)}\right\}_{n=0}^{N}$, and finally perform inverse discrete polynomial transform to compute $\frac{d}{dx}u(x_{j})$.

# Clenshaw's algorithm

Clenshaw's algorithm is an efficient way to evaluate the finite sum of orthogonal polynomials at given points. Let $p_{n}(x)$ be the orthogonal polynomials with following three-term recurrence relationship:

$$
p_{n+1}=(x-\alpha_{n})p_{n}-\beta_{n}p_{n-1},n=0,1,\cdots
$$

with given initial values $p_{0}$and $p_{-1}$. Then we can evaluate the finite sum

$$
s(x)=\sum_{n=0}^{N}c_{n}p_{n}(x)
$$

by using Clenshaw's algorithm:

- Initialization: $u_{n}=c_{n},u_{n+1}=0$

- For $k=n-1,\cdots,0$, do

  - $u_{k}=(x-\alpha_{k})u_{k+1}-\beta_{k+1}u_{k+2}+c_{k}$

- Result: $s(x)=u_{0}p_{0}-\beta_{0}u_{1}p_{-1}$

Note that if $p_{-1}=0$, then $s(x)=u_{0}p_{0}$

# Conversion algorithm

Let $\left\{ p_{n}\right\}$ be the monic orthogonal polynomials satisfying the following three-term recurrence relation:

$$
p_{n+1}=(x-a_{n})p_{n}-b_{n}p_{n-1},n=0,1,\cdots
$$

with, $p_{0}=1$ and $p_{-1}=0$. Let $\left\{ \pi_{n}\right\}$ be another monic orthogonal polynomials satisfying the following three-term recurrence relation:

$$
\pi_{n+1}=(x-\alpha_{n})\pi_{n}-\beta_{n}\pi_{n-1},n=0,1,\cdots
$$

with, $\pi_{0}=1$ and $\pi_{-1}=0$. Now consider the finite sum:

$$
s(x)=\sum_{n=0}^{N}c_{n}p_{n}(x)
$$

we want to express this finite sum in terms of $\pi_{n}(x)$.

$$
s(x)=\sum_{n=0}^{N}d_{n}\pi_{n}(x)
$$

Then, $d_{n}$ can be obtained by following algorithm:

- Initialization: $\sigma_{00}=\beta_{0}$,

  $\sigma_{-1,l}=0$, $\sigma_{k,k-1}=\sigma_{k+1,k-1}=0$, for $k=0,\cdots,n$

- For $l=0,1,\cdots,n-1$

  - For $k=0,1,\cdots,l+1$

    - $\sigma_{k,l+1}=\sigma_{k+1,l}+(\alpha_{k}-a_{l})\sigma_{kl}+\beta_{k}\sigma_{k-1,l}-b_{l}\sigma_{k,l-1}$

- $d_{k}=\frac{1}{\sigma_{kk}}\sum_{l=k}^{n}\sigma_{kl}c_{l}$

# Barrio-Clenshaw-Smith algorithm

# Compensated Clenshaw algorithm
