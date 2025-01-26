# Ultraspherical polynomials

Jacobi polynomial with $\alpha=\beta>-1$, are called the ultraspherical polynomials or Gegenbauer polynomial. We will denote ultraspherical polynomial by $P_{n}^{\lambda}(x)$ where, $\alpha=\lambda-\frac{1}{2}$. Note that $\lambda>-\frac{1}{2}$.

$$
P_{n}^{(\lambda)}(x)=\frac{\Gamma\left(\lambda+\frac{1}{2}\right)}{\Gamma\left(2\lambda\right)}\frac{\Gamma\left(n+2\lambda\right)}{\Gamma\left(n+\lambda+\frac{1}{2}\right)}P_{n}^{\left(\alpha,\alpha\right)}(x),\quad\alpha=\lambda-\frac{1}{2}
$$

we can also write

$$
P_{n}^{(\lambda)}(x)=\frac{\Gamma\left(\alpha+1\right)}{\Gamma\left(2\alpha+1\right)}\frac{\Gamma\left(n+2\alpha+1\right)}{\Gamma\left(n+\alpha+1\right)}P_{n}^{\left(\alpha,\alpha\right)}(x),\quad\alpha=\lambda-\frac{1}{2}
$$

- Note that for $\alpha=-1/2$, or $\lambda=0$, $\Gamma\left(2\alpha+1\right)$is not defined, and this case should be handled carefully.

- The $P_{n}^{\lambda}$ are orthogonal with respect to the following weight function.

$$
w(x)=(1-x^{2})^{\alpha}=(1-x^{2})^{\lambda-0.5}
$$

- The support of ultraspherical polynomial is $[-1,1].$

# First few Ultraspherical polynomials

$$
P_{0}^{(\lambda)}=1
$$

$$
P_{1}^{(\lambda)}=2\lambda x
$$

- For $\lambda=1/2$, $\alpha=0$, and we get Legendre polynomial.

$$
P_{n}(x)=P_{n}^{(\lambda)}(x)
$$

- For $\lambda=1$, $\alpha=1/2$, we get Chebyshev polynomial of second kind.

$$
U_{n}(x)=P_{n}^{(\lambda)}(x)
$$

# Leading coefficient

The leading coefficient of $P_{n}^{(\lambda)}$ is denoted by $k_{n}$ and it is given by

$$
\begin{aligned}k_{n} & =\frac{1}{2^{n}}\frac{\Gamma\left(2n+2\alpha+1\right)}{n!\Gamma\left(n+2\alpha+1\right)}\frac{\Gamma\left(\alpha+1\right)}{\Gamma\left(2\alpha+1\right)}\frac{\Gamma\left(n+2\alpha+1\right)}{\Gamma\left(n+\alpha+1\right)}\\
 & =\frac{1}{2^{n}n!}\frac{\Gamma\left(2n+2\alpha+1\right)}{\Gamma\left(n+\alpha+1\right)}\frac{\Gamma\left(\alpha+1\right)}{\Gamma\left(2\alpha+1\right)}\\
 & =\frac{2^{n}}{n!}\frac{\Gamma\left(n+\lambda\right)}{\Gamma\left(\lambda\right)}\quad\lambda\ne0
\end{aligned}
$$

Here, we have used the following identity.

$$
\frac{\Gamma\left(2z\right)}{\Gamma(z)}=\frac{\Gamma(z+\frac{1}{2})}{2^{0.5-2z}\sqrt{2\pi}}
$$

$$
\frac{k_{n+1}}{k_{n}}=2\left(\frac{n+\lambda}{n+1}\right)
$$

# Norm

The norm of $P_{n}^{(\lambda)}$ is given below:

$$
\Vert P_{n}^{(\lambda)}\Vert^{2}=:h_{n}^{\lambda}=\left(2^{1-2\lambda}\right)\frac{\pi}{\left[\Gamma(\lambda)\right]^{2}}\frac{\Gamma\left(n+2\lambda\right)}{\left(n+\lambda\right)\Gamma\left(n+1\right)}
$$

$$
\frac{h_{n-1}^{\lambda}}{h_{n}^{\lambda}}=\frac{n(n+\lambda)}{(n+\lambda-1)(n+2\lambda-1)}
$$

$$
\frac{h_{n+1}^{\lambda}}{h_{n}^{\lambda}}=\frac{(n+\lambda)(n+2\lambda)}{(n+1)(n+\lambda+1)}
$$

# Symmetry

$$
P_{n}^{(\lambda)}(x)=\left(-1\right)^{n}P_{n}^{(\lambda)}(-x)
$$

Therefore, $P_{n}^{(\lambda)}(x)$ is even if $n$ is even and odd if $n$ is odd.

# Scaling

$$
P_{n}^{(\lambda)}(\pm1)=\left(\pm1\right)^{n}\left(\begin{array}{c}
n+2\lambda-1\\
n
\end{array}\right)
$$


# Boundedness


# Derivatives

$$
\frac{dP_{n}^{(\lambda)}}{dx}=2\lambda P_{n-1}^{\left(\lambda+1\right)}
$$

or

$$
P_{n-1}^{\left(\lambda+1\right)}=\frac{1}{2\lambda}\frac{dP_{n}^{(\lambda)}}{dx}
$$

# Orthogonality

$$
\int_{-1}^{+1}P_{m}^{(\lambda)}(x)P_{n}^{(\lambda)}(x)(1-x^{2})^{\lambda-0.5}dx=h_{m}^{(\lambda)}\delta_{mn}
$$

$$
\int_{-1}^{+1}\frac{dP_{m}^{(\lambda)}(x)}{dx}\frac{dP_{n}^{(\lambda)}(x)}{dx}\left(1-x^{2}\right)^{\lambda+0.5}dx=4\lambda^{2}h_{n-1}^{\left(\lambda+1\right)}\delta_{mn}
$$

# Polynomial representation

$$
P_{n}^{(\lambda)}(x)=\frac{1}{\Gamma\left(\lambda\right)}\sum_{m=0}^{\left[n/2\right]}\left(-1\right)^{m}2^{n-2m}\frac{\Gamma\left(\lambda+n-m\right)}{m!\left(n-2m\right)!}x^{n-2m}
$$

where $\left[n/2\right]$ is the integer part of $n/2$.


# Strum-Liovile equation

$$
\frac{1}{\left(1-x^{2}\right)^{\alpha}}\frac{d}{dx}\left(\left(1-x^{2}\right)^{\alpha+1}\frac{dy}{dx}\right)+n\left(n+2\alpha+1\right)y=0
$$


# Rodrigues's Formula

$$
\left(1-x^{2}\right)^{\lambda-0.5}P_{n}^{(\lambda)}(x)=\frac{\left(-2\right)^{n}}{n!}\frac{\Gamma\left(\lambda+n\right)}{\Gamma\left(\lambda\right)}\frac{\Gamma\left(n+2\lambda\right)}{\Gamma\left(2n+2\lambda\right)}\frac{d^{n}}{dx^{n}}\left[\left(1-x^{2}\right)^{n+\lambda-0.5}\right]
$$


# Recurrence relation for monic Ultraspherical polynomial

Let $\pi_{n}^{(\lambda)}$ denotes the monic orthogonal Ultraspherical polynomial.

$$
\pi_{n+1}^{(\lambda)}=\left(x-\alpha_{n}\right)\pi_{n}^{(\lambda)}-\beta_{n}\pi_{n-1}^{(\lambda)},\quad n=0,1,2
$$

$$
\alpha_{n}=0,n\ge0
$$

$$
\beta_{0}=2^{2\alpha+1}\frac{\left[\Gamma\left(\alpha+1\right)\right]^{2}}{\Gamma\left(2\left(\alpha+1\right)\right)}=\frac{\pi}{\lambda2^{2\lambda-1}}\frac{\Gamma(2\lambda)}{\left[\Gamma(\lambda)\right]^{2}}
$$

$$
\beta_{1}=\frac{1}{(3+2\alpha)}=\frac{1}{2+2\lambda}
$$

$$
\begin{aligned}\beta_{n\ge2} & =\frac{n(n+2\alpha)}{(2n+2\alpha+1)(2n+2\alpha-1)}\\
 & =\frac{n(2\lambda+n-1)}{4(n+\lambda)(n+\lambda-1)}
\end{aligned}
$$

# Recurrence relation for monic orthonormal Ultraspherical polynomial

Let $\tilde{\pi}_{n}^{(\lambda)}$ denotes the monic orthonormal Ultraspherical polynomial.

$$
\tilde{\pi}_{n+1}^{(\lambda)}=\frac{\left(x-\alpha_{n}\right)}{\sqrt{\beta_{n+1}}}\tilde{\pi}_{n}^{(\lambda)}-\frac{\beta_{n}}{\sqrt{\beta_{n+1}\beta_{n}}}\tilde{\pi}_{n-1}^{(\lambda)},\quad n=0,1,2
$$

or

$$
\tilde{\pi}_{n+1}^{(\lambda)}=\left(x-\alpha_{n}\right)s_{n}^{a}\tilde{\pi}_{n}^{(\lambda)}-\beta_{n}s_{n}^{b}\tilde{\pi}_{n-1}^{(\lambda)},\quad n=0,1,2
$$

$$
s_{n}^{a}=\frac{1}{\sqrt{\beta_{n+1}}}
$$

$$
s_{n}^{b}=\frac{1}{\sqrt{\beta_{n}\beta_{n+1}}}=s_{n}^{a}s_{n-1}^{a}
$$

# Recurrence relation for Ultraspherical polynomials

$$
P_{-1}^{(\lambda)}=0,
$$

$$
P_{0}^{(\lambda)}=1
$$

$$
P_{1}^{(\lambda)}=2\lambda x
$$

$$
P_{n+1}^{(\lambda)}=\left(x-\alpha_{n}\right)s_{n}^{a}P_{n}^{(\lambda)}-\beta_{n}s_{n}^{b}P_{n-1}^{(\lambda)},\quad n=0,1,2
$$

where,

$$
s_{n}^{a}=\frac{k_{n+1}}{k_{n}}=2\left(\frac{n+\lambda}{n+1}\right)
$$

$$
s_{n}^{b}=s_{n}^{a}s_{n-1}^{a}
$$

$$
s_{0}^{b}=\frac{s_{0}^{a}}{\sqrt{\beta_{0}}}
$$

Alternatively, we can write the above recurrence relationship as:

$$
P_{n+1}^{(\lambda)}=\left(a_{n}x\right)P_{n}^{(\lambda)}-c_{n}P_{n-1}^{(\lambda)},\quad n=1,2,\cdots
$$

$$
a_{n}=s_{n}^{a}=2\left(\frac{n+\lambda}{n+1}\right)
$$

$$
c_{n}=\beta_{n}s_{n}^{b}=\frac{n+2\lambda-1}{n+1}
$$

# Recurrence relation for orthonormal Ultraspherical polynomials

$$
\tilde{P}_{n+1}^{(\lambda)}=\left(x-\alpha_{n}\right)s_{n}^{a}\tilde{P}_{n}^{(\lambda)}-\beta_{n}s_{n}^{b}\tilde{P}_{n-1}^{(\lambda)},\quad n=0,1,2
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

# Recurrence relation for derivative of Ultraspherical polynomial

The gradient can be computed by following recurrence relationship:

$$
\left(1-x^{2}\right)\frac{dP_{n}^{(\lambda)}}{dx}=2\beta_{n}\left(n+\lambda\right)s_{n-1}^{a}P_{n-1}^{(\lambda)}+\left(-nx\right)P_{n}^{(\lambda)}
$$

$$
\left(\frac{dP_{n}}{dx}\right)_{x=1}=\frac{1}{2}\left(n+2\lambda\right)\frac{\Gamma\left(n+\lambda+1/2\right)}{\left(n-1\right)!\Gamma\left(\lambda+3/2\right)}
$$

$$
\left(\frac{dP_{n}}{dx}\right)_{x=-1}=\left(-1\right)^{n-1}\frac{1}{2}\left(n+2\lambda\right)\frac{\Gamma\left(n+\lambda+1/2\right)}{\left(n-1\right)!\Gamma\left(\lambda+3/2\right)}
$$

$$
s_{n}^{a}=\frac{k_{n+1}}{k_{n}}=2\left(\frac{n+\lambda}{n+1}\right)
$$

# More recurrence relation for derivative of Ultraspherical polynomial

$$
nP_{n}^{(\lambda)}=x\frac{dP_{n}^{(\lambda)}}{dx}-\frac{dP_{n-1}^{(\lambda)}}{dx}
$$

$$
P_{n}^{(\lambda)}=-\frac{x}{n+2\lambda}\frac{dP_{n}^{(\lambda)}}{dx}+\frac{1}{n+2\lambda}\frac{dP_{n+1}^{(\lambda)}}{dx}
$$

$$
P_{n}^{(\lambda)}=\frac{1}{2\left(n+\lambda\right)}\frac{d}{dx}\left(P_{n+1}^{(\lambda)}-P_{n-1}^{(\lambda)}\right)
$$

# Recurrence relation for derivative of orthonormal Ultraspherical polynomial

$$
\left(1-x^{2}\right)\frac{d\tilde{P}_{n}^{(\lambda)}}{dx}=2\beta_{n}\left(n+\lambda\right)s_{n-1}^{a}\tilde{P}_{n-1}^{(\lambda)}+\left(-nx\right)\tilde{P}_{n}^{(\lambda)}
$$

$$
s_{n-1}^{a}=\frac{1}{\sqrt{\beta_{n}}}
$$

# Recurrence relation for derivative of monic Ultraspherical polynomial

$$
\left(1-x^{2}\right)\frac{d\pi_{n}^{(\lambda)}}{dx}=2\beta_{n}\left(n+\lambda\right)\pi_{n-1}^{(\lambda)}+\left(-nx\right)\pi_{n}^{(\lambda)}
$$

# Recurrence relation for derivative of monic orthonormal Ultraspherical polynomial

$$
\left(1-x^{2}\right)\frac{d\tilde{\pi}_{n}^{(\lambda)}}{dx}=2\beta_{n}\left(n+\lambda\right)s_{n-1}^{a}\tilde{\pi}_{n-1}^{(\lambda)}+\left(-nx\right)\tilde{\pi}_{n}^{(\lambda)}
$$

$$
s_{n-1}^{a}=\frac{1}{\sqrt{\beta_{n}}}
$$

# Kernel polynomial

# More recurrence relations

# Additional properties

# Ultraspherical-Gauss Quadratures

Jacobi-matrix for Ultraspherical polynomials is a symmetric tridiagonal matrix ${\bf J}_{n}=\left\{ {\bf D}_{n},{\bf E}_{n}\right\}$. The main diagonal ${\bf D}_{n}$ and sub-diagonal ${\bf E}_{n}$ are given by

$$
{\bf D}_{n}=\boldsymbol{0}\in R^{n}
$$

$$
{\bf E}_{n}=\left[\sqrt{\beta_{1}},\sqrt{\beta_{2}},\cdots,\sqrt{\beta_{n-1}}\right]\in R^{n-1}
$$

- The $N+1$ point Ultraspherical-Gauss quadrature rule is denoted by $\left\{ x_{j}^{G},w_{j}^{G}\right\} _{j=0}^{N}$.

- The points $x_{j}^{G}$ are zeros of $P_{N+1}^{(\lambda)}$, that is,

$$
P_{N+1}^{(\lambda)}(x_{j}^{G})=0,j=0,1,\cdots,N
$$

- and $\left\{ x_{j}^{G}\right\}_{j=0}^{N}$ are the eigenvalues of Jacobi matrix ${\bf J}_{N+1}$.

- Weights are given by

$$
w_{j}=,j=0,\cdots,N
$$

# Ultraspherical Gauss-Radau Quadratures

Jacobi Gauss-Radau matrix for Ultraspherical polynomials is a symmetric tridiagonal matrix ${\bf J}_{n+1}^{R,a}=\left\{ {\bf D}_{n+1},{\bf E}_{n+1}\right\}$. The main diagonal ${\bf D}_{n+1}$ and sub-diagonal ${\bf E}_{n+1}$ are given by

$$
{\bf D}_{n+1}=\left[\boldsymbol{0},\alpha_{n}^{R}\right]\in R^{n+1}
$$

$$
{\bf E}_{n}=\left[\sqrt{\beta_{1}},\sqrt{\beta_{2}},\cdots,\sqrt{\beta_{n-1}},\sqrt{\beta_{n}}\right]\in R^{n}
$$

where,

$$
\alpha_{n}^{R}=\frac{a}{2}\left(\frac{n+2\lambda}{n+\lambda}\right)
$$

The $N+1$ point Ultraspherical Gauss-Radau quadrature rule is denoted by $\left\{ x_{j}^{R},w_{j}^{R}\right\} _{j=0}^{n}$, which are the eigenvalues of Jacobi Gauss-Radau matrix. The weights are given by

$$
w_{j}=,j=0,\cdots,n
$$

# Ultraspherical Gauss-Lobatto Quadratures

Jacobi Gauss-Lobatto matrix for Ultraspherical polynomials is a symmetric tridiagonal matrix ${\bf J}_{n+2}^{L}=\left\{ {\bf D}_{n+2},{\bf E}_{n+2}\right\}$. The main diagonal ${\bf D}_{n+2}$ and sub-diagonal ${\bf E}_{n+2}$ are given by

$$
{\bf D}_{n+2}=\boldsymbol{0}\in R^{n+2}
$$

$$
{\bf E}_{n+2}=\left[\sqrt{\beta_{1}},\sqrt{\beta_{2}},\cdots,\sqrt{\beta_{n-1}},\sqrt{\beta_{n}},\sqrt{\beta_{n+1}^{L}}\right]\in R^{n+1}
$$

The $n+2$ point Jacobi Gauss-Lobatto quadrature rule is denoted by $\left\{ x_{j}^{L},w_{j}^{L}\right\} _{j=0}^{n+1}$, which are the eigenvalues of Jacobi Gauss-Lobatto matrix.The weights are given by

$$
w_{j}=,j=0,\cdots,n+1
$$

# Lagrange polynomial for Ultraspherical-Gauss points

The Lagrange interpolation polynomials, $\left\{ l_{j}(x)\right\}_{j=0}^{N}$, based on the Gauss quadrature points, $\left\{ x_{j}\right\}_{j=0}^{N},$are

$$
l_{i}(x)=\frac{P_{N+1}^{(\lambda)}(x)}{(x-x_{i})\frac{d}{dx}P_{N+1}^{(\lambda)}(x_{i})},\quad i=0,\cdots,N
$$

# Lagrange polynomial for Ultraspherical-Gauss-Lobatto points

The Lagrange interpolation polynomials, $\left\{ l_{j}(x)\right\}_{j=0}^{N}$, based on the Gauss-Lobatto quadrature points, $\left\{ x_{j}\right\}_{j=0}^{N},$are

$$
l_{i}(x)=\begin{cases}
(\lambda+0.5)\Pi_{N,i}^{(\lambda)}(x) & i=0,N\\
\Pi_{N,i}^{(\lambda)}(x) & \text{otherwise}
\end{cases}
$$

where,

$$
\Pi_{N,i}^{(\lambda)}(x)=-\frac{1}{N(N+2\lambda)}\frac{(1-x^{2})}{(x-x_{i})P_{N}^{(\lambda)}(x_{i})}\frac{dP_{N}^{(\lambda)}(x)}{dx}
$$

# Lagrange polynomial for Ultraspherical-Gauss-Radau points

The Lagrange interpolation polynomials, $\left\{ l_{j}(x)\right\}_{j=0}^{N}$, based on the Gauss-Radau quadrature points, $\left\{ x_{j}\right\}_{j=0}^{N},$are

$$
l_{i}(x)=\begin{cases}
(\lambda+0.5)\Pi_{N,i}^{(\lambda)}(x) & i=0,orN\\
\Pi_{N,i}^{(\lambda)}(x) & \text{otherwise}
\end{cases}
$$

where,

$$
\begin{aligned}\Pi_{N,i}^{(\lambda)}(x) & =\frac{1}{2(N+\lambda+0.5)(N+2\lambda)}\frac{(1-x_{i})}{P_{N}^{(\lambda)}(x_{i})}\\
 & \times\frac{(N+1)P_{N+1}^{(\lambda)}(x)+(N+2\lambda)P_{N}^{(\lambda)}(x)}{(x-x_{i})}
\end{aligned}
$$
