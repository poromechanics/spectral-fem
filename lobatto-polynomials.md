# Lobatto Polynomials

$$
l_{0}\left(x\right)=\frac{1-x}{2}=\frac{1}{2}P_{0}-\frac{1}{2}P_{1}
$$

$$
l_{1}\left(x\right)=\frac{1+x}{2}=\frac{1}{2}P_{0}+\frac{1}{2}P_{1}
$$

$$
l_{m+2}\left(x\right)=\frac{1}{\Vert P_{m+1}\Vert}\int_{-1}^{x}P_{m+1}(x)dx,\quad m\ge0
$$

where,

$$
\Vert P_{m+1}\Vert=\sqrt{\frac{2}{2m+3}}
$$

or,

$$
l_{m}\left(x\right)=\frac{1}{\Vert P_{m-1}\Vert}\int_{-1}^{x}P_{m-1}(x)dx,\quad m\ge2
$$

where,

$$
\Vert P_{m-1}\Vert=\sqrt{\frac{2}{2m-1}}
$$

so,

$$
l_{m+2}\left(x\right)=\sqrt{\frac{2m+3}{2}}\int_{-1}^{x}P_{m+1}(x)dx,\quad m\ge0
$$

Noting that

$$
P_{m}\left(x\right)=\frac{1}{2m+1}\frac{d}{dx}\left(P_{m+1}-P_{m-1}\right)
$$

It can be shown that

$$
l_{m+2}\left(x\right)=\frac{1}{\sqrt{2\left(2m+3\right)}}\left[P_{m+2}\left(x\right)-P_{m}\left(x\right)\right],\quad m\ge0
$$

The above expression can also be written as:

$$
l_{m}\left(x\right)=\frac{1}{\sqrt{2\left(2m-1\right)}}\left[P_{m}\left(x\right)-P_{m-2}\left(x\right)\right],\quad m\ge2
$$


## Lobatto polynomials as Jacobi polynomials

Lobatto polynomials can also be given by

$$
l_{0}=\frac{1-x}{2}=\frac{1}{2}P_{0}-\frac{1}{2}P_{1}
$$

$$
l_{1}=\frac{1+x}{2}=\frac{1}{2}P_{0}+\frac{1}{2}P_{1}
$$

$$
l_{m+2}(x)=-l_{0}(x)l_{1}(x)\frac{\sqrt{2\left(2m+3\right)}}{m+1}P_{m}^{\left(1,1\right)}(x),\quad m\ge0
$$

or

$$
l_{m}(x)=-l_{0}(x)l_{1}(x)\frac{\sqrt{2\left(2m-1\right)}}{m-1}P_{m-2}^{\left(1,1\right)}(x),\quad m\ge2
$$

where $P_{m}^{\left(1,1\right)}(x)$ for $m=0,1,\cdots$ are the Jacobi polynomials. We can also write Lobatto polynomials in terms of Ultraspherical polynomials as shown below:

$$
l_{m+2}(x)=-l_{0}(x)l_{1}(x)\frac{\sqrt{8\left(2m+3\right)}}{\left(m+1\right)\left(m+2\right)}P_{m}^{(1.5)}\left(x\right),\quad m\ge0
$$


## First few lobatto polynomials

$$
l_{0}=\frac{1-x}{2}
$$

$$
l_{1}=\frac{1+x}{2}
$$

$$
l_{2}=\frac{1}{2}\sqrt{\frac{3}{2}}\left(x^{2}-1\right)
$$

$$
l_{3}=\frac{1}{2}\sqrt{\frac{5}{2}}\left(x^{2}-1\right)x
$$

$$
l_{4}=\frac{1}{8}\sqrt{\frac{7}{2}}\left(x^{2}-1\right)\left(5x^{2}-1\right)
$$

$$
l_{5}=\frac{1}{8}\sqrt{\frac{9}{2}}\left(x^{2}-1\right)\left(7x^{2}-3\right)x
$$

## Derivative of lobatto polynomials

$$
\frac{dl_{m+2}}{dx}=\sqrt{\frac{2m+3}{2}}P_{m+1}(x),m\ge0
$$

or

$$
\frac{dl_{m}}{dx}=\sqrt{\frac{2m-1}{2}}P_{m-1}(x),m\ge2
$$

we know that

$$
P_{n-1}^{(\lambda+1)}\left(x\right)=\frac{1}{2\lambda}\frac{dP_{n}^{(\lambda)}}{dx}\left(x\right),\lambda>-1/2
$$

$$
\frac{dl_{m}}{dx}\left(x\right)=\sqrt{\frac{2m-1}{2}}P_{m-1}^{(-1+1/2+1)}(x),m\ge2
$$

$$
\frac{dl_{m}}{dx}\left(x\right)=\sqrt{\frac{2m-1}{2}}P_{m-1}^{(1/2)}(x),m\ge2
$$

$$
\frac{dl_{0}}{dx}=-\frac{1}{2}
$$

$$
\frac{dl_{1}}{dx}=\frac{1}{2}
$$

## Leading coefficients

$$
k_{0}=-\frac{1}{2}
$$

$$
k_{1}=\frac{1}{2}
$$

$$
k_{m+2}=\frac{1}{\sqrt{2\left(2m+3\right)}}\frac{\left(2m+4\right)!}{2^{m+2}\left[\left(m+2\right)!\right]^{2}},\quad m\ge0
$$

$$
k_{2}=\sqrt{\frac{3}{8}}
$$

$$
\frac{k_{1}}{k_{0}}=-1
$$

$$
\frac{k_{2}}{k_{1}}=\sqrt{\frac{3}{32}}
$$

$$
\frac{k_{m+3}}{k_{m+2}}=\frac{\sqrt{\left(2m+3\right)\left(2m+5\right)}}{\left(m+3\right)},\quad m\ge0
$$

## Norm

We define norm of lobatto polynomial as

$$
\int_{-1}^{1}\left(l_{m}\right)^{2}dx=:\Vert l_{m}\Vert^{2}=h_{m}
$$

$$
h_{0}=\Vert l_{0}\Vert^{2}=\frac{2}{3}
$$

$$
h_{1}=\Vert l_{1}\Vert^{2}=\frac{2}{3}
$$

$$
h_{m+2}=\Vert l_{m+2}\Vert^{2}=\frac{2}{\left(2m+1\right)\left(2m+5\right)}
$$

$$
\frac{h_{0}}{h_{1}}=1
$$

$$
\frac{h_{1}}{h_{2}}=
$$

$$
\frac{h_{m+2}}{h_{m+3}}=,\quad m\ge0
$$

## Moments

$$
l_{m+2}=\frac{1}{\sqrt{2\left(2m+3\right)}}\left[P_{m+2}\left(x\right)-P_{m}\left(x\right)\right],\quad m\ge0
$$

Zero moment

$$
\left\langle l_{m}\right\rangle_{0}:=\int_{-1}^{+1}l_{m}dx
$$

$$
\left\langle l_{0}\right\rangle_{0}=\left\langle l_{1}\right\rangle_{0}=1
$$

$$
\left\langle l_{m+2}\right\rangle_{0}=\begin{cases}
-\sqrt{\frac{2}{3}} & m=0\\
0 & m\ge1
\end{cases}
$$

## Mass matrix

$$
\left(l_{0},l_{0}\right)=\frac{2}{3}
$$

$$
\left(l_{0},l_{1}\right)=\frac{1}{3}
$$

$$
\left(l_{0},l_{m+2}\right)=\begin{cases}
-\frac{1}{\sqrt{6}} & m=0\\
\frac{1}{3\sqrt{10}} & m=1\\
0 & m\ge2
\end{cases}
$$

$$
\left(l_{1},l_{1}\right)=\frac{2}{3}
$$

$$
\left(l_{1},l_{m+2}\right)=\begin{cases}
-\frac{1}{\sqrt{6}} & m=0\\
-\frac{1}{3\sqrt{10}} & m=1\\
0 & m\ge2
\end{cases}
$$

$$
\left(l_{m+2},l_{m+2}\right)=\frac{2}{\left(2m+1\right)\left(2m+5\right)}
$$

$$
\left(l_{m+2},l_{m+4}\right)=\frac{-1}{\left(2m+5\right)\sqrt{\left(2m+7\right)\left(2m+3\right)}}
$$

$$
M=\left[\begin{array}{cccccccc}
l_{00} & l_{01} & l_{02} & l_{03} & 0 & 0 & 0 & \cdots\\
l_{10} & l_{11} & l_{12} & l_{13} & 0 & 0 & 0 & \cdots\\
l_{20} & l_{21} & l_{22} & 0 & l_{24} & 0 & 0 & \cdots\\
l_{30} & l_{31} & 0 & l_{33} & 0 & l_{35} & 0 & \cdots\\
0 & 0 & l_{42} & 0 & l_{44} & 0 & l_{46} & \cdots\\
0 & 0 & 0 & l_{53} & 0 & l_{55} & 0 & \cdots\\
0 & 0 & 0 & 0 & l_{64} & 0 & l_{66} & \cdots\\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \ddots
\end{array}\right]
$$

## Stiffness matrix

$$
a(l_{m},l_{n})=\int_{-1}^{+1}\frac{dl_{m}}{dx}\frac{dl_{n}}{dx}dx
$$

$$
a(l_{0},l_{0})=\frac{1}{2},\quad a(l_{0},l_{1})=-\frac{1}{2}
$$

$$
a(l_{1},l_{0})=-\frac{1}{2},\quad a(l_{1},l_{1})=\frac{1}{2}
$$

$$
a(l_{0},l_{m+2})=0,\quad m\ge0
$$

$$
a(l_{1},l_{m+2})=0,\quad m\ge0
$$

$$
a\left(l_{m+2},l_{n+2}\right)=\begin{cases}
1 & m=n\ge0\\
0 & m\ne n
\end{cases}
$$

$$
K=\left[\begin{array}{ccccc}
0.5 & -0.5 & 0 & 0 & 0\\
-0.5 & 0.5 & 0 & 0 & 0\\
0 & 0 & 1.0 & 0 & 0\\
0 & 0 & 0 & 1.0 & 0\\
0 & 0 & 0 & 0 & 1.0
\end{array}\right]
$$

## Zeros

Zero of $l_{0}=1$, zero of $l_{1}=-1$, and by noting that

$$
l_{m+2}=\sqrt{\frac{\left(2m+3\right)}{2\left(m+1\right)^{2}(m+2)^{2}}}\left(x^{2}-1\right)\frac{dP_{m+1}}{dx}
$$

zeros of $l_{m+2}$ are $\bar{\pm1}$, and zeros of $\frac{dP_{m+1}}{dx}$ or $P_{m}^{1,1}$.

## Derivation of kernel polynomials

By noting that:

$$
\begin{aligned}\left(1-x^{2}\right)\frac{dP_{m}}{dx} & =\frac{m(m+1)}{2m+1}\left[P_{m-1}(x)-P_{m+1}(x)\right]\\
 & =-\frac{m(m+1)}{2m+1}\sqrt{2\left(2m+1\right)}l_{m+1}\\
 & =-m(m+1)\sqrt{\frac{2}{\left(2m+1\right)}}l_{m+1}
\end{aligned}
$$

we get:

$$
\begin{aligned}l_{m+1}(x) & =\sqrt{\frac{\left(2m+1\right)}{2m^{2}(m+1)^{2}}}\left(x^{2}-1\right)\frac{dP_{m}}{dx}\\
 & =\sqrt{\frac{\left(2m+1\right)}{2m^{2}(m+1)^{2}}}\left(x^{2}-1\right)\frac{m+1}{2}P_{m-1}^{1,1}(x)\\
 & =\sqrt{\frac{\left(2m+1\right)}{8m^{2}}}\left(x^{2}-1\right)P_{m-1}^{1,1}(x)\\
 & =-\frac{\left(1-x^{2}\right)}{4}\sqrt{\frac{16\left(2m+1\right)}{8m^{2}}}P_{m-1}^{1,1}(x)\\
 & =-l_{0}(x)l_{1}(x)\sqrt{\frac{16\left(2m+1\right)}{8m^{2}}}P_{m-1}^{1,1}(x)
\end{aligned}
$$

therefore,

$$
\phi_{m-1}(x)=-\frac{\sqrt{2\left(2m+1\right)}}{m}P_{m-1}^{1,1}(x)
$$

Now we use following definition of ultraspherical polynomials:

$$
P_{m}^{\alpha+\frac{1}{2}}(x)=\frac{\Gamma\left(\alpha+1\right)}{\Gamma\left(2\alpha+1\right)}\frac{\Gamma\left(m+2\alpha+1\right)}{\Gamma\left(m+\alpha+1\right)}P_{m}^{\alpha,\alpha}(x),\quad\alpha=\lambda-\frac{1}{2}
$$

then by setting $\alpha=1$, we get:

$$
P_{m}^{1+\frac{1}{2}}(x)=\frac{\Gamma\left(2\right)}{\Gamma\left(3\right)}\frac{\Gamma\left(m+3\right)}{\Gamma\left(m+2\right)}P_{m}^{1,1}(x)=\frac{m+2}{2}P_{m}^{1,1}(x)
$$

or

$$
P_{m}^{1,1}(x)=\frac{2}{m+2}P_{m}^{1.5}(x)
$$

subtituting the above expression in kernel polynomial:

$$
\phi_{m-1}=-\frac{\sqrt{8\left(2m+1\right)}}{m\left(m+1\right)}P_{m-1}^{1.5}(x)
$$

This completes the proof.
