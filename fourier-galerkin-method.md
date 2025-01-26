# Fourier-Galerkin method

Let $L$ be a differential operator (linear or nonlinear). Consider following initial-boundary-value problem on $[0,2\pi]$.

$$
\frac{\partial u(x,t)}{\partial t}=Lu,\quad u(x,0)=u_{0}(x)
$$

Also, $u(0,t)=u(2\pi,t),\forall t$

Recall that $\hat{\mathfrak{B}}_{N}:=span\{e^{inx}\vert\quad\vert n\vert\le N/2\}$. Then, we seek solutions in $\hat{\mathfrak{B}}_{N}$ by approximating $u$ as $u_{N}\in\hat{\mathfrak{B}}_{N}$ such that

$$
u_{N}(x,t):=\sum_{\vert n\vert\le N/2}\hat{a}_{n}(t)e^{inx}
$$

Note that, in general:

$$
\hat{a}_{n}(t)\ne\hat{u}_{n}(t)=\frac{1}{2\pi}\int_{0}^{2\pi}u(x)e^{-inx}
$$

Residual:

$$
R(x,t)=\frac{\partial u_{N}}{\partial t}-Lu_{N}
$$

The coefficients $\hat{a}_{n}$are obtained by the requirement that the residual $R(x,t)$ is orthogonal to $\hat{\mathfrak{B}}_{N}$, that is:

$$
\int_{0}^{2\pi}R(x,t)e^{-inx}dx=0,\quad\forall\vert n\vert\le N/2
$$

So, if we express $R$ as follows,

$$
R(x,t)=\sum_{\vert n\vert\le\infty}\hat{R}_{n}(t)e^{inx}
$$

then,

$$
\hat{R}_{n}(t)=\frac{1}{2\pi}\int_{0}^{2\pi}R(x,t)e^{-inx}dx=0,\quad\forall\vert n\vert\le N/2
$$

These are $N+1$ ODEs to determine $N+1$ unknowns, $\hat{a}_{n}(t)$, with following initial conditions.

$$
\hat{a}_{n}(0)=\frac{1}{2\pi}\int_{0}^{2\pi}u_{0}(x)e^{-inx}dx,\quad\forall\vert n\vert\le N/2
$$

Now we ask following questions:

When does $R(x,t)$ is orthogonal to $\hat{\mathfrak{B}}_{N}$?

What if $R(x,t)$ is NOT orthogonal to $\hat{\mathfrak{B}}_{N}$?

What if $R(x,t)$ is in $\hat{\mathfrak{B}}_{N}$

## Examples

Constant coefficient problem.

$$
Lu=c\frac{\partial u(x,t)}{\partial x}+\nu\frac{\partial^{2}u(x,t)}{\partial t^{2}}
$$

Variable coefficient problem

$$
Lu=\sin(x)\frac{\partial u(x,t)}{\partial x}
$$

Nonlinear problem

$$
Lu=u(x,t)\frac{\partial u(x,t)}{\partial x}
$$

Strongly nonlinear problem

$$
Lu=e^{u(x,t)}\frac{\partial u(x,t)}{\partial x}
$$

Fourier-Galerkin method is very efficient for linear, constant coefficient problem

It becomes complicated for variable coefficient and nonlinear problem

