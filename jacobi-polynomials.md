# Jacobi polynomial

Jacobi polynomial of order $n$ is denoted by $P_{n}^{(\alpha,\beta)}\left(x\right)$. 

Here $\alpha$ and $\beta$ are parameters of Jacobi polynomial. Note that

$$1+\alpha>0,\quad1+\beta>0$$

The Jacobi polynomials are orthogonal with respect to the following weight function.

$$w(x)=(1-x)^{\alpha}(1+x)^{\beta}$$

The support of Jacobi polynomial is $[-1,1].$


## Leading coefficient

The leading coefficient of $P_{n}^{(\alpha,\beta)}$ is denoted by $k_{n}$ and it is given by

$$k_{n}=\frac{1}{2^{n}}\left(\begin{array}{c}
2n+\alpha+\beta\\
n
\end{array}\right)=\frac{1}{2^{n}}\frac{\Gamma\left(2n+\alpha+\beta+1\right)}{n!\Gamma\left(n+\alpha+\beta+1\right)}$$

$$\frac{k_{n+1}}{k_{n}}=\frac{1}{2}\left(\frac{2n+\alpha+\beta+2}{n+1}\right)\left(\frac{2n+\alpha+\beta+1}{n+\alpha+\beta+1}\right)$$

$$\frac{k_{1}}{k_{0}}=\frac{1}{2}\left(\alpha+\beta+2\right)$$

## Norm

The norm of $P_{n}^{(\alpha,\beta)}$ is given below:

$$\Vert P_{n}^{(\alpha,\beta)}\Vert^{2}=:h_{n}^{(\alpha,\beta)}=\frac{2^{\alpha+\beta+1}}{2n+\alpha+\beta+1}\frac{\Gamma(n+\alpha+1)\Gamma(n+\beta+1)}{n!\Gamma(n+\alpha+\beta+1)}$$

$$\frac{h_{n-1}^{(\alpha,\beta)}}{h_{n}^{(\alpha,\beta)}}=\begin{cases}
\frac{3+\alpha+\beta}{\left(1+\alpha\right)\left(1+\beta\right)} & n=1\\
\frac{n\left(2n+\alpha+\beta+1\right)\left(n+\alpha+\beta\right)}{\left(2n+\alpha+\beta-1\right)\left(n+\alpha\right)\left(n+\beta\right)} & n>1
\end{cases}$$

$$\frac{h_{n+1}^{(\alpha,\beta)}}{h_{n}^{(\alpha,\beta)}}=\begin{cases}
\frac{\left(1+\alpha\right)\left(1+\beta\right)}{\left(3+\alpha+\beta\right)} & n=0\\
\frac{\left(2n+\alpha+\beta+1\right)\left(n+\alpha+1\right)\left(n+\beta+1\right)}{\left(n+1\right)\left(2n+\alpha+\beta+3\right)\left(n+\alpha+\beta+1\right)} & n\ge1
\end{cases}$$

## Scaling

Jacobi polynomials are scaled such that the value of $P_{n}^{(\alpha,\beta)}$ at $x=1$ is given by

$$P_{n}^{(\alpha,\beta)}(1)=\frac{\Gamma(n+\alpha+1)}{n!\Gamma(1+\alpha)}=\left(\begin{array}{c}
n+\alpha\\
n
\end{array}\right)$$

$$P_{n}^{(\alpha,\beta)}\left(-1\right)=\left(-1\right)^{n}\frac{\Gamma(n+\beta+1)}{n!\Gamma(1+\beta)}=\left(-1\right)^{n}\left(\begin{array}{c}
n+\beta\\
n
\end{array}\right)$$

## Symmetry

Symmetry of Jacobi polynomial depends upon $n$ and $\alpha,\beta$ as shown below.

$$P_{n}^{(\alpha,\beta)}(x)=\left(-1\right)^{n}P_{n}^{(\beta,\alpha)}(-x)$$

## Scaling

## Boundedness

## Derivatives

Derivative of Jacobi polynomial $P_{n}^{(\alpha,\beta)}$ is also a Jacobi Polynomial of order $n-1$ and parameter $\alpha+1$ and $\beta+1$.

$$\frac{dP_{n}^{(\alpha,\beta)}}{dx}=\frac{1}{2}\left(n+\alpha+\beta+1\right)P_{n-1}^{\left(\alpha+1,\beta+1\right)}$$

Derivative of $P_{n}^{(\alpha,\beta)}$ is also a Jacobi Polynomial of order $n-k$ and parameters $\alpha+k$ and $\beta+k$.

$$\frac{d^{k}P_{n}^{(\alpha,\beta)}}{dx^{k}}=\frac{\Gamma\left(n+k+\alpha+\beta+1\right)}{2^{k}\Gamma\left(n+\alpha+\beta+1\right)}P_{n-k}^{\left(\alpha+k,\beta+k\right)}$$

## Orthogonality


## Polynomial representation

$P_{n}^{(\alpha,\beta)}$ can be expressed as

$$
P_{n}^{(\alpha,\beta)}(x)=\sum_{k=0}^{n}a_{k}^{n}(x-1)^{k}
$$

where,

$$
\frac{a_{k+1}^{n}}{a_{k}^{n}}=\frac{h_{n}^{(\alpha,\beta)}-k\left(k+\alpha+\beta+1\right)}{2(k+1)(k+\alpha+1)}
$$

with

$$
a_{0}^{n}=P_{n}^{(\alpha,\beta)}(1)=\frac{\Gamma(n+\alpha+1)}{n!\Gamma(1+\alpha)}=\left(\begin{array}{c}
n+\alpha\\
n
\end{array}\right)
$$

Therefore, we can expand Jacobi polynomial by

$$
P_{n}^{(\alpha,\beta)}(x)=\frac{\Gamma(n+\alpha+1)}{n!\Gamma(n+\alpha+\beta+1)}\sum_{k=0}^{n}\left(\begin{array}{c}
n\\
k
\end{array}\right)\frac{\Gamma\left(n+k+\alpha+\beta+1\right)}{\Gamma\left(k+\alpha+1\right)}\left(\frac{x-1}{2}\right)^{k}
$$

There is another representation:

$$
P_{n}^{(\alpha,\beta)}(x)=\frac{1}{2^{n}}\sum_{k=0}^{n}\left(\begin{array}{c}
n+\alpha\\
k
\end{array}\right)\left(\begin{array}{c}
n+\beta\\
n-k
\end{array}\right)\left(x-1\right)^{n-k}\left(x+1\right)^{k}
$$

## Strum-Liovile equation

$P_{n}^{(\alpha,\beta)}$ is solution of following Strum-Liovile differential equation:

$$
\frac{1}{\left(1-x\right)^{\alpha}\left(1+x\right)^{\beta}}\frac{d}{dx}\left(\left(1-x\right)^{\alpha+1}\left(1+x\right)^{\beta+1}\frac{dy}{dx}\right)+n\left(n+\alpha+\beta+1\right)y=0
$$

## Rodrigues's Formula

$$
\left(1-x\right)^{\alpha}\left(1+x\right)^{\beta}P_{n}^{(\alpha,\beta)}(x)=\frac{\left(-1\right)^{n}}{2^{n}n!}\frac{d^{n}}{dx^{n}}\left[\left(1-x\right)^{n+\alpha}\left(1+x\right)^{n+\beta}\right]
$$


## Recurrence relation for monic Jacobi polynomials

Let $\pi_{n}^{(\alpha,\beta)}$ be the monic Jacobi polynomials, the three-term reccurence relationship for monic polynomial:

$$\pi_{n+1}^{(\alpha,\beta)}=\left(x-\alpha_{n}\right)\pi_{n}^{(\alpha,\beta)}-\beta_{n}\pi_{n-1}^{(\alpha,\beta)},\quad n=0,1,2$$

$$\beta_{0}=2^{\alpha+\beta+1}\frac{\Gamma(\alpha+1)\Gamma(\beta+1)}{\Gamma(\alpha+\beta+2)}$$

$$\beta_{1}=\frac{4(1+\alpha)(1+\beta)}{(2+\alpha+\beta)^{2}(3+\alpha+\beta)}$$

$$\beta_{n\ge2}=\frac{4n(n+\alpha)(n+\beta)(n+\alpha+\beta)}{(2n+\alpha+\beta)^{2}(2n+\alpha+\beta+1)(2n+\alpha+\beta-1)}$$

$$\alpha_{0}=\frac{\beta-\alpha}{\alpha+\beta+2}$$

$$\alpha_{n\ge1}=\frac{\beta^{2}-\alpha^{2}}{(2n+\alpha+\beta)(2n+\alpha+\beta+2)}$$

## Recurrence relation for monic orthonormal Jacobi polynomials 

Let $\tilde{\pi}_{n}^{(\alpha,\beta)}$ be the monic orthonormal Jacobi polynomials, the three-term reccurence relationship:

$$\tilde{\pi}_{n+1}^{(\alpha,\beta)}=\frac{\left(x-\alpha_{n}\right)}{\sqrt{\beta_{n+1}}}\tilde{\pi}_{n}^{(\alpha,\beta)}-\frac{\beta_{n}}{\sqrt{\beta_{n+1}\beta_{n}}}\tilde{\pi}_{n-1}^{(\alpha,\beta)},\quad n=0,1,2$$

or

$$\tilde{\pi}_{n+1}^{(\alpha,\beta)}=\left(x-\alpha_{n}\right)s_{n}^{a}\tilde{\pi}_{n}^{(\alpha,\beta)}-\beta_{n}s_{n}^{b}\tilde{\pi}_{n-1}^{(\alpha,\beta)},\quad n=0,1,2$$

$$s_{n}^{a}=\frac{1}{\sqrt{\beta_{n+1}}}$$

$$s_{n}^{b}=\frac{1}{\sqrt{\beta_{n}\beta_{n+1}}}=s_{n}^{a}s_{n-1}^{a}$$


## Recurrence relation for Jacobi polynomial 

Let $P_{n}^{(\alpha,\beta)}$ be the Jacobi polynomial with initial values:

$$P_{-1}^{(\alpha,\beta)}=0$$

$$P_{0}^{(\alpha,\beta)}=1$$

$$P_{1}^{(\alpha,\beta)}=\frac{1}{2}\left(\alpha+\beta+2\right)x+\frac{1}{2}\left(\alpha-\beta\right)$$

then, the three term recurrence relationship is given by:

$$P_{n+1}^{(\alpha,\beta)}=\left(x-\alpha_{n}\right)s_{n}^{a}P_{n}^{(\alpha,\beta)}-\beta_{n}s_{n}^{b}P_{n-1}^{(\alpha,\beta)},\quad n=0,1,2$$

where,

$$s_{n}^{a}=\frac{k_{n+1}}{k_{n}}=\frac{1}{2}\left(\frac{2n+\alpha+\beta+2}{n+1}\right)\left(\frac{2n+\alpha+\beta+1}{n+\alpha+\beta+1}\right)$$

$$s_{n}^{b}=s_{n}^{a}s_{n-1}^{a}$$

$$s_{0}^{a}=\frac{k_{1}}{k_{0}}=\frac{1}{2}\left(\alpha+\beta+2\right)$$

$$s_{0}^{b}=\frac{s_{0}^{a}}{\sqrt{\beta_{0}}}$$

Alternatively, we can write the three term relationship as:

$$P_{n+1}^{(\alpha,\beta)}=\left(a_{n}x+b_{n}\right)P_{n}^{(\alpha,\beta)}-c_{n}P_{n-1}^{(\alpha,\beta)},\quad n=1,2,\cdots$$

$$a_{n}=s_{n}^{a}=\frac{\left(2n+\alpha+\beta+2\right)\left(2n+\alpha+\beta+1\right)}{2\left(n+1\right)\left(n+\alpha+\beta+1\right)}$$

$$b_{n}=-\alpha_{n}s_{n}^{a}=\frac{\left(\alpha^{2}-\beta^{2}\right)\left(2n+\alpha+\beta+1\right)}{2\left(n+1\right)\left(n+\alpha+\beta+1\right)\left(2n+\alpha+\beta\right)}$$

$$c_{n}=\beta_{n}s_{n}^{a}s_{n-1}^{a}=\frac{\left(n+\alpha\right)\left(n+\beta\right)\left(2n+\alpha+\beta+2\right)}{\left(n+1\right)\left(n+\alpha+\beta+1\right)\left(2n+\alpha+\beta\right)}$$

## Recurrence relation for orthonormal Jacobi polynomials

Let $\tilde{P}_{n}^{(\alpha,\beta)}$ be the orthonormal Jacobi polynomials, then the recurrence relationship is given by: $$\tilde{P}_{n+1}^{(\alpha,\beta)}=\left(x-\alpha_{n}\right)s_{n}^{a}\tilde{P}_{n}^{(\alpha,\beta)}-\beta_{n}s_{n}^{b}\tilde{P}_{n-1}^{(\alpha,\beta)},\quad n=0,1,2$$

$$s_{n}^{a}=\frac{k_{n+1}}{k_{n}}\frac{\Vert P_{n}^{(\alpha,\beta)}\Vert}{\Vert P_{n+1}^{(\alpha,\beta)}\Vert}$$

$$\begin{aligned}s_{n}^{b} & =\frac{k_{n+1}}{k_{n-1}}\frac{\Vert P_{n-1}^{(\alpha,\beta)}\Vert}{\Vert P_{n+1}^{(\alpha,\beta)}\Vert}\\
 & =\frac{k_{n+1}}{k_{n-1}}\frac{k_{n}}{k_{n}}\frac{\Vert P_{n-1}^{(\alpha,\beta)}\Vert}{\Vert P_{n+1}^{(\alpha,\beta)}\Vert}\frac{\Vert P_{n}^{(\alpha,\beta)}\Vert}{\Vert P_{n}^{(\alpha,\beta)}\Vert}\\
 & =\frac{k_{n+1}}{k_{n}}\frac{\Vert P_{n}^{(\alpha,\beta)}\Vert}{\Vert P_{n+1}^{(\alpha,\beta)}\Vert}\frac{k_{n}}{k_{n-1}}\frac{\Vert P_{n-1}^{(\alpha,\beta)}\Vert}{\Vert P_{n}^{(\alpha,\beta)}\Vert}\\
 & =s_{n}^{a}s_{n-1}^{a}
\end{aligned}$$

$$\frac{\Vert\pi_{n}\Vert}{\Vert\pi_{n-1}\Vert}=\frac{k_{n-1}\Vert P_{n}^{(\alpha,\beta)}\Vert}{k_{n}\Vert P_{n-1}^{(\alpha,\beta)}\Vert}=\sqrt{\beta_{n}}$$

$$\frac{\Vert P_{n}^{(\alpha,\beta)}\Vert}{\Vert P_{n-1}^{(\alpha,\beta)}\Vert}=\frac{k_{n}}{k_{n-1}}\sqrt{\beta_{n}}$$

$$\frac{\Vert P_{n}^{(\alpha,\beta)}\Vert}{\Vert P_{n+1}^{(\alpha,\beta)}\Vert}=\frac{k_{n}}{k_{n+1}\sqrt{\beta_{n+1}}}$$

$$\begin{aligned}s_{n}^{a} & =\frac{k_{n+1}}{k_{n}}\frac{k_{n}}{k_{n+1}\sqrt{\beta_{n+1}}}\\
 & =\frac{1}{\sqrt{\beta_{n+1}}}
\end{aligned}$$

$$s_{n}^{b}=s_{n}^{a}s_{n-1}^{a}=\frac{1}{\sqrt{\beta_{n+1}\beta_{n}}}$$

$$s_{0}^{b}=\frac{1}{\sqrt{\beta_{1}}}\frac{1}{\sqrt{\beta_{0}}}=\frac{s_{0}^{a}}{\sqrt{\beta_{0}}}$$

## Recurrence relation for derivative of Jacobi polynomial

$$
P_{n+1}^{\alpha,\beta}=\left(x-\alpha_{n}\right)s_{n}^{a}P_{n}^{\alpha,\beta}-\beta_{n}s_{n}^{b}P_{n-1}^{\alpha,\beta}
$$

$$
s_{n}^{a}=\frac{k_{n+1}}{k_{n}}=\frac{1}{2}\left(\frac{2n+\alpha+\beta+2}{n+1}\right)\left(\frac{2n+\alpha+\beta+1}{n+\alpha+\beta+1}\right)
$$

$$
s_{n}^{b}=s_{n}^{a}s_{n-1}^{a}
$$

Then gradient can be computed by following recurrence relationship:

$$
\left(1-x^{2}\right)\frac{dP_{n}^{\alpha,\beta}}{dx}=\beta_{n}\left(2n+\alpha+\beta+1\right)s_{n-1}^{a}P_{n-1}^{\alpha,\beta}+\left(\frac{n(\alpha-\beta)}{2n+\alpha+\beta}-nx\right)P_{n}^{\alpha,\beta}
$$

$$
\left(\frac{dP_{n}}{dx}\right)_{x=1}=\frac{1}{2}\left(n+\alpha+\beta+1\right)\frac{\Gamma\left(n+\alpha+1\right)}{\left(n-1\right)!\Gamma\left(\alpha+2\right)}
$$

$$
\left(\frac{dP_{n}}{dx}\right)_{x=-1}=\left(-1\right)^{n-1}\frac{1}{2}\left(n+\alpha+\beta+1\right)\frac{\Gamma\left(n+\beta+1\right)}{\left(n-1\right)!\Gamma\left(\beta+2\right)}
$$

**Proof**: It is know that

$$
\left(1-x^{2}\right)\frac{dP_{n}^{\alpha,\beta}}{dx}=A_{n}P_{n-1}^{\alpha,\beta}+B_{n}P_{n}^{\alpha,\beta}-C_{n}P_{n+1}^{\alpha,\beta}
$$

with

$$
A_{n}=\frac{2(n+\alpha)(n+\beta)(n+\alpha+\beta+1)}{(2n+\alpha+\beta)(2n+\alpha+\beta+1)}
$$

$$
B_{n}=\frac{(\alpha-\beta)2n(n+\alpha+\beta+1)}{(2n+\alpha+\beta)(2n+\alpha+\beta+2)}
$$

$$
C_{n}=\frac{2n(n+1)(n+\alpha+\beta+1)}{(2n+\alpha+\beta+1)(2n+\alpha+\beta+2)}
$$

Using recurrence relationship for $P_{n+1}^{\alpha,\beta}$, we obtain:

$$
\left(1-x^{2}\right)\frac{dP_{n}^{\alpha,\beta}}{dx}=\left(A_{n}+\beta_{n}C_{n}s_{n}^{b}\right)P_{n-1}^{\alpha,\beta}+\left[B_{n}-C_{n}\left(x-\alpha_{n}\right)s_{n}^{a}\right]P_{n}^{\alpha,\beta}
$$

Noting that,$P_{n}^{\alpha,\beta}$

$$
C_{n}s_{n}^{b}=ns_{n-1}^{a},\text{ or }C_{n}=\frac{n}{s_{n}^{a}}
$$

By using these relationship:

$$
\left(1-x^{2}\right)\frac{dP_{n}^{\alpha,\beta}}{dx}=\left(A_{n}+n\beta_{n}s_{n-1}^{a}\right)P_{n-1}^{\alpha,\beta}+\left(B_{n}-n\left(x-\alpha_{n}\right)\right)P_{n}^{\alpha,\beta}
$$

Now note that

$$
n\beta_{n}s_{n-1}^{a}=\frac{2n\left(n+\alpha\right)\left(n+\beta\right)}{\left(2n+\alpha+\beta\right)\left(2n+\alpha+\beta+1\right)}
$$

$$
A_{n}+n\beta_{n}s_{n-1}^{a}=\frac{2\left(n+\alpha\right)\left(n+\beta\right)}{\left(2n+\alpha+\beta\right)}
$$

and

$$
B_{n}+n\alpha_{n}=\frac{n(\alpha-\beta)}{\left(2n+\alpha+\beta\right)}
$$

The above recurrence simplifies to:

$$
\left(1-x^{2}\right)\frac{dP_{n}^{\alpha,\beta}}{dx}=\frac{2\left(n+\alpha\right)\left(n+\beta\right)}{\left(2n+\alpha+\beta\right)}P_{n-1}^{\alpha,\beta}+\left(\frac{n(\alpha-\beta)}{2n+\alpha+\beta}-nx\right)P_{n}^{\alpha,\beta}
$$

$$
\left(1-x^{2}\right)\frac{dP_{n}^{\alpha,\beta}}{dx}=\beta_{n}\left(2n+\alpha+\beta+1\right)s_{n-1}^{a}P_{n-1}^{\alpha,\beta}+\left(\frac{n(\alpha-\beta)}{2n+\alpha+\beta}-nx\right)P_{n}^{\alpha,\beta}
$$

This completes the proof.

## More recurrence relationships for derivative of Jacobi polynomial

Three term recurrence

$$\left(1-x^{2}\right)\frac{dP_{n}^{\alpha,\beta}}{dx}=A_{n}P_{n-1}^{\alpha,\beta}+B_{n}P_{n}^{\alpha,\beta}-C_{n}P_{n+1}^{\alpha,\beta}$$ with $$A_{n}=\frac{2(n+\alpha)(n+\beta)(n+\alpha+\beta+1)}{(2n+\alpha+\beta)(2n+\alpha+\beta+1)}$$ $$B_{n}=\frac{(\alpha-\beta)2n(n+\alpha+\beta+1)}{(2n+\alpha+\beta)(2n+\alpha+\beta+2)}$$ $$C_{n}=\frac{2n(n+1)(n+\alpha+\beta+1)}{(2n+\alpha+\beta+1)(2n+\alpha+\beta+2)}$$

## Recurrence relation for derivative of orthonormal Jacobi polynomial

$$\left(1-x^{2}\right)\frac{d\tilde{P}_{n}^{\alpha,\beta}}{dx}=\beta_{n}\left(2n+\alpha+\beta+1\right)s_{n-1}^{a}\tilde{P}_{n-1}^{\alpha,\beta}+\left(\frac{n(\alpha-\beta)}{2n+\alpha+\beta}-nx\right)\tilde{P}_{n}^{\alpha,\beta}$$

$$s_{n-1}^{a}=\frac{1}{\sqrt{\beta_{n}}}$$

## Recurrence relation for derivative of monic Jacobi polynomial

$$\left(1-x^{2}\right)\frac{d\pi_{n}}{dx}=\frac{2\left(n+\alpha\right)\left(n+\beta\right)}{\left(2n+\alpha+\beta\right)}\frac{k_{n-1}}{k_{n}}\pi_{n-1}+\left(\frac{n(\alpha-\beta)}{2n+\alpha+\beta}-nx\right)\pi_{n}$$

$$\begin{aligned}\frac{2\left(n+\alpha\right)\left(n+\beta\right)}{\left(2n+\alpha+\beta\right)}\frac{k_{n-1}}{k_{n}} & =\frac{4n\left(n+\alpha\right)\left(n+\beta\right)\left(n+\alpha+\beta\right)}{\left(2n+\alpha+\beta\right)^{2}\left(2n+\alpha+\beta-1\right)}\\
 & =\beta_{n}\left(2n+\alpha+\beta+1\right)
\end{aligned}$$

$$\beta_{n\ge2}=\frac{4n\left(n+\alpha\right)\left(n+\beta\right)\left(n+\alpha+\beta\right)}{\left(2n+\alpha+\beta\right)^{2}\left(2n+\alpha+\beta+1\right)\left(2n+\alpha+\beta-1\right)}$$

$$\left(1-x^{2}\right)\frac{d\pi_{n}}{dx}=\beta_{n}\left(2n+\alpha+\beta+1\right)\pi_{n-1}+\left(\frac{n(\alpha-\beta)}{2n+\alpha+\beta}-nx\right)\pi_{n}$$

## Recurrence relation for derivative of monic orthonormal Jacobi polynomial

$$\left(1-x^{2}\right)\frac{d\tilde{\pi}_{n}}{dx}=\beta_{n}\left(2n+\alpha+\beta+1\right)\tilde{\pi}_{n-1}\frac{\Vert\pi_{n-1}\Vert}{\Vert\pi_{n}\Vert}+\left(\frac{n(\alpha-\beta)}{2n+\alpha+\beta}-nx\right)\tilde{\pi}_{n}$$

$$\left(1-x^{2}\right)\frac{d\tilde{\pi}_{n}}{dx}=\beta_{n}\left(2n+\alpha+\beta+1\right)\frac{1}{\sqrt{\beta_{n}}}\tilde{\pi}_{n-1}+\left(\frac{n(\alpha-\beta)}{2n+\alpha+\beta}-nx\right)\tilde{\pi}_{n}$$

$$\left(1-x^{2}\right)\frac{d\tilde{\pi}_{n}}{dx}=\beta_{n}\left(2n+\alpha+\beta+1\right)s_{n-1}^{a}\tilde{\pi}_{n-1}+\left(\frac{n(\alpha-\beta)}{2n+\alpha+\beta}-nx\right)\tilde{\pi}_{n}$$

$$s_{n-1}^{a}=\frac{1}{\sqrt{\beta_{n}}}$$

## Kernel polynomial

$$K_{n}(x,y):=\sum_{m=0}^{n}\frac{P_{m}^{\alpha,\beta}(x)P_{m}^{\alpha,\beta}(y)}{h_{m}^{\alpha,\beta}}$$

$$K_{n}(x,1):=\sum_{m=0}^{n}\frac{P_{m}^{\alpha,\beta}(1)}{h_{m}^{\alpha,\beta}}P_{m}^{\alpha,\beta}(x)=d_{n}^{\alpha,\beta}P_{n}^{\alpha+1,\beta}(x)$$

$$d_{n}^{\alpha,\beta}=\frac{P_{m}^{\alpha,\beta}(1)k_{n}^{\alpha,\beta}}{k_{n}^{\alpha+1,\beta}h_{n}^{\alpha,\beta}}=\frac{1}{2^{\alpha+\beta+1}}\frac{\Gamma\left(n+\alpha+\beta+2\right)}{\Gamma\left(\alpha+1\right)\Gamma\left(n+\beta+1\right)}$$

## More recurrence relations

Jacobi polynomial $P_{n}^{\alpha+1,\beta}(x)$ is a linear combination of $P_{m}^{\alpha,\beta}(x),m=0,1,\cdots n$, that is

$$P_{n}^{\alpha+1,\beta}(x)=\frac{\Gamma(n+\beta+1)}{\Gamma(n+\alpha+\beta+2)}\sum_{m=0}^{n}\frac{\left(2m+\alpha+\beta+1\right)\Gamma\left(m+\alpha+\beta+1\right)}{\Gamma(m+\beta+1)}P_{m}^{\alpha,\beta}(x)$$

or

$$P_{n}^{\alpha+1,\beta}(x)=\frac{2}{\left(2n+\alpha+\beta+2\right)}\frac{\left(n+\alpha+1\right)P_{n}^{\alpha,\beta}(x)-\left(n+1\right)P_{n+1}^{\alpha,\beta}(x)}{\left(1-x\right)}$$

Similarly,

$$P_{n}^{\alpha,\beta+1}(x)=\frac{\Gamma(n+\alpha+1)}{\Gamma(n+\alpha+\beta+2)}\sum_{m=0}^{n}\left(-1\right)^{n-m}\frac{\left(2m+\alpha+\beta+1\right)\Gamma\left(m+\alpha+\beta+1\right)}{\Gamma(m+\alpha+1)}P_{m}^{\alpha,\beta}(x)$$

or

$$P_{n}^{\alpha,\beta+1}(x)=\frac{2}{\left(2n+\alpha+\beta+2\right)}\frac{\left(n+\beta+1\right)P_{n}^{\alpha,\beta}(x)+\left(n+1\right)P_{n+1}^{\alpha,\beta}(x)}{\left(1+x\right)}$$

-   Relation between $P_{n}^{(\alpha+1,\beta+1)}$ and $P_{n}^{\left(\alpha,\beta\right)}$ $$\begin{aligned}P_{n-1}^{\alpha+1,\beta+1}(x) & =P_{n}^{\alpha+1,\beta}(x)-P_{n}^{\alpha,\beta+1}(x)\\
     & =\frac{2}{\left(1-x^{2}\right)}\left[\left(\frac{\alpha-\beta}{\left(2n+\alpha+\beta+2\right)}+x\right)P_{n}^{\alpha,\beta}(x)-\frac{2n+2}{2n+\alpha+\beta+2}P_{n+1}^{\alpha,\beta}(x)\right]\\
     & =\frac{2}{\left(1-x^{2}\right)}\left[\left(a_{n}+x\right)P_{n}^{\alpha,\beta}(x)-b_{n}P_{n+1}^{\alpha,\beta}(x)\right]
    \end{aligned}$$

$$P_{n}^{\alpha+1,\beta+1}(x)=\frac{1}{n+\alpha+\beta}\left[\left(n+\beta\right)P_{n}^{\alpha+1,\beta}(x)+\left(n+\alpha\right)P_{n}^{\alpha,\beta+1}(x)\right]$$


## Additional properties

### Property-1

Note that $\left\{ \frac{dP_{m}^{\alpha,\beta}}{dx}\right\} _{m=1}^{n+1}$ forms an orthogonal basis of $\mathcal{P}^{n}$, hence we can write $P_{n}^{\alpha,\beta}$ as

$$P_{n}^{\alpha,\beta}=a_{n}\frac{dP_{n-1}^{\alpha,\beta}}{dx}+b_{n}\frac{dP_{n}^{\alpha,\beta}}{dx}+c_{n}\frac{dP_{n+1}^{\alpha,\beta}}{dx}$$

where,

$$a_{n}=\frac{-2(n+\alpha)(n+\beta)}{(n+\alpha+\beta)(2n+\alpha+\beta)(2n+\alpha+\beta+1)}$$

$$b_{n}=\frac{2(\alpha-\beta)}{(2n+\alpha+\beta)(2n+\alpha+\beta+2)}$$

$$c_{n}=\frac{2(n+\alpha+\beta+1)}{(2n+\alpha+\beta+1)(2n+\alpha+\beta+2)}$$

### Property-2

$$\left(1-x^{2}\right)\frac{dP_{n+1}^{\alpha,\beta}}{dx}=-\left(N+1\right)\left[x+\frac{\beta-\alpha}{2n+\alpha+\beta+2}\right]P_{n+1}^{\alpha,\beta}+2\left[\frac{\left(n+\alpha+1\right)\left(n+\beta+1\right)}{2n+\alpha+\beta+2}\right]P_{n}^{\alpha,\beta}$$

So, if $\left\{ x_{n+1}^{j}\right\} _{j=0}^{n}$ are zeros of $P_{n+1}^{\alpha,\beta}$, then $$\left(1-x_{j}^{2}\right)\frac{dP_{n+1}^{\alpha,\beta}\left(x_{j}\right)}{dx}=2\left[\frac{\left(n+\alpha+1\right)\left(n+\beta+1\right)}{2n+\alpha+\beta+2}\right]P_{n}^{\alpha,\beta}\left(x_{j}\right)$$


## Jacobi-Gauss Quadratures

Jacobi-matrix for Jacobi polynomials is a symmetric tridiagonal matrix ${\bf J}_{n}=\left\{ {\bf D}_{n},{\bf E}_{n}\right\}$. The main diagonal ${\bf D}_{n}$ and sub-diagonal ${\bf E}_{n}$ are given by

$${\bf D}_{n}=\left[\alpha_{0},\alpha_{1},\cdots,\alpha_{n-1}\right]\in R^{n}$$

$${\bf E}_{n}=\left[\sqrt{\beta_{1}},\sqrt{\beta_{2}},\cdots,\sqrt{\beta_{n-1}}\right]\in R^{n-1}$$

The N-point Jacobi-Gauss quadrature rule is denoted by $\left\{ x_{j}^{G},w_{j}^{G}\right\} _{j=0}^{n-1}$.

The points $x_{j}^{G}$ are zeros of $P_{N}^{\alpha,\beta}$, that is

$$P_{N}^{\alpha,\beta}(x_{j}^{G})=0,j=0,1,\cdots n-1$$

and $\left\{ x_{j}^{G}\right\} _{n=0}^{n-1}$ are the eigenvalues of Jacobi matrix ${\bf J}_{n}$ .

## Jacobi Gauss-Radau Quadratures

Jacobi Gauss-Radau matrix for Jacobi polynomials is a symmetric tridiagonal matrix ${\bf J}_{n+1}^{R,a}=\left\{ {\bf D}_{n+1},{\bf E}_{n+1}\right\}$. The main diagonal ${\bf D}_{n+1}$ and sub-diagonal ${\bf E}_{n+1}$ are given by

$${\bf D}_{n+1}=\left[\alpha_{0},\alpha_{1},\cdots,\alpha_{n-1},\alpha_{n}^{R}\right]\in R^{n+1}$$

$${\bf E}_{n}=\left[\sqrt{\beta_{1}},\sqrt{\beta_{2}},\cdots,\sqrt{\beta_{n-1}},\sqrt{\beta_{n}}\right]\in R^{n}$$

Where,

$$\alpha_{n}^{R}=a+\frac{(1-a)n(n+\alpha)-(1+a)n(n+\beta)}{(2n+\alpha+\beta)(2n+\alpha+\beta+1)}$$

The $n+1$ point Jacobi Gauss-Radau Gauss quadrature rule is denoted by $\left\{ x_{j}^{R},w_{j}^{R}\right\} _{j=0}^{n}$, which are the eigenvalues of Jacobi Gauss-Radau matrix.

There is another point of view for understanding the Gauss-Radau quadrature points.

- For $a=-1$, $x_{0}^{R}=-1$, and $n$ points $x_{j}^{R},j=1,\cdots n$ are zeros of $P_{n}^{\alpha,\beta+1}(x)$
- For $a=1$, $x_{n}^{R}=1$, and $n$ points $x_{j}^{R},j=0,\cdots n-1$ are zeros $P_{n}^{\alpha+1,\beta}(x)$


## Jacobi Gauss-Lobatto Quadratures

Jacobi Gauss-Lobatto matrix for Jacobi polynomials is a symmetric tridiagonal matrix ${\bf J}_{n+2}^{L}=\left\{ {\bf D}_{n+2},{\bf E}_{n+2}\right\}$. The main diagonal ${\bf D}_{n+2}$ and sub-diagonal ${\bf E}_{n+2}$ are given by

$${\bf D}_{n+2}=\left[\alpha_{0},\alpha_{1},\cdots,\alpha_{n-1},\alpha_{n},\alpha_{n+1}^{L}\right]\in R^{n+2}$$

$${\bf E}_{n+2}=\left[\sqrt{\beta_{1}},\sqrt{\beta_{2}},\cdots,\sqrt{\beta_{n-1}},\sqrt{\beta_{n}},\sqrt{\beta_{n+1}^{L}}\right]\in R^{n+1}$$

Where,

$$\alpha_{n+1}^{L}=\frac{\alpha-\beta}{2n+\alpha+\beta+2}$$

$$\beta_{n+1}^{L}=4\frac{\left(n+\alpha+1\right)\left(n+\beta+1\right)\left(n+\alpha+\beta+1\right)}{\left(2n+\alpha+\beta+1\right)\left(2n+\alpha+\beta+2\right)^{2}}$$

The $n+2$ point Jacobi Gauss-Lobatto quadrature rule is denoted by $\left\{ x_{j}^{R},w_{j}^{R}\right\} _{j=0}^{n+1}$, which are the eigenvalues of Jacobi Gauss-Lobatto matrix.

There is another point of view for understanding the Gauss-Lobatto quadrature points.

> $x_{0}^{L}=-1$ and $x_{n+1}^{L}=1$, the $n-1$ points $x_{j}^{L},j=1,\cdots n-1$ are zeros of $P_{n-1}^{\alpha+1,\beta+1}(x)$ , that is zeros of $\frac{dP_{n}^{\alpha,\beta}}{dx}$


## Lagrange polynomials for Jacobi-Gauss points

## Lagrange polynomials for Jacobi-Gauss-Lobatto points

## Lagrange polynomials for Jacobi-Gauss-Radau points
