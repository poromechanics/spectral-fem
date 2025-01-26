# Fourier Collocation Method

-   We will use interpolating operator $\mathcal{I}_{N}$ instead of projection operator $\mathcal{P}_{N}$.
-   It mean we seek solution in $\tilde{\mathfrak{B}}_{N}$ and not in $\hat{\mathfrak{B}}_{N}$ .
-   This method is called Fourier-collocation method or pseudospectral method

Quadrature formulas and grid points are critical part of this method?

- **Collocation grid**: In collocation method, we require that the residual $R(x,t)$ vanishes exactly on some set of gridpoints $y_{j}$. These gridpoints are called Collocation points or Collocation grids.
- **Interpolation grid:** Collection of grid points, such as $x_{j}=\frac{2\pi}{N}j,\quad j=0,1,\cdots,N-1$, which is used in $\mathcal{I}_{N}$.

There is no need for collocation grid and interpolation grid to be identical to each other.

Let $L$ be a differential operator (linear or nonlinear). Consider following initial-boundary-value problem on $[0,2\pi]$.

$$
\frac{\partial u(x,t)}{\partial t}=Lu,\quad u(x,0)=u_{0}(x)
$$


Recall that $\tilde{\mathfrak{B}}_{N}:=span\{e^{inx}\vert\quad\vert n\vert\le N/2\}/\sin\left(\frac{Nx}{2}\right)$. Then, we seek solutions in $\tilde{\mathfrak{B}}_{N}$ by approximating $u$ as:

$$
u_{N}(x,t):=\sum_{j=0}^{N-1}u_{N}(x_{j},t)g_{j}(x)
$$


There are $N$ unknown coefficients $u_{N}(x_{j},t)$, and $g_{j}(x)$ is the Lagrange interpolation polynomial for an even numbe of points, and $x_{j}=\frac{2\pi}{N}j,j=0,1,\cdots N-1$.

Residual:

$$
R_{N}(x,t)=\frac{\partial u_{N}}{\partial t}-Lu_{N}
$$


Collocation method:

$$
R_{N}(y_{j},t)=0,\forall j=0,1,\cdots,N-1
$$


These are $N$ equations which should be sufficient to find $N$ unknows.

In the collocation method the only use we make of the Fourier approximation is in obtaining the derivatives of the numerical approximation in physical space.
