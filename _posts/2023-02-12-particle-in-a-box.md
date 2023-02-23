---
title: A Particle in a Box
subtitle: Quantum Mechanics 2.2
author: jiho
date: 2023-02-12 00:30:00 +0800
categories: [Learning, Physics, Quantum Mechanics]
tags: [physics, quantum mechanics, particle in a box, schrödinger equation, infinite potential wall]
math: true
---

## Introduction

In quantum mechanics, the **particle in a box** model
(also known as the **infinite potential well** or the **infinite square well**)
describes a particle free to move in a small space surrounded by impenetrable barriers.
The model is mainly used as a hypothetical example to illustrate the differences between classical and quantum systems.

## One-dimensional solution

The simplest form of the particle in a box model considers a one-dimensional system.
Here, the particle may only move backward and forwards along a straight line with impenetrable barriers at either end.
The walls of a one-dimensional box may be seen as regions of space with infinitely large potential energy.

The potential energy in this model is given as

\\[ V(x) = \begin{cases} 0 &(0<x<L) \nl \infty &(\text{otherwise}) \end{cases}\\]

![Infinite potential wall](https://upload.wikimedia.org/wikipedia/commons/1/13/Infinite_potential_well-en.svg)
_The barriers outside a one-dimensional box have infinitely large potential,
while the interior of the box has a constant, zero potential._

Using the time-independent Schrödinger equation,

\\[ -\frac{\hbar^2}{2m}\frac{\partial^2\psi}{\partial x^2}+V\psi=E\psi \\]

The two potential barriers result in two boundary conditions:

\\[ \psi(0)=\psi(L)=0 \\]

Since the particle can only exist at $0<x<L$, where the potential $V(x)$ is $0$,
the equation becomes simpler:

\\[ -\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2}=E\psi  \\]

The solution to this equation is:

\\[  \psi(x)=A\sin kx+B\cos kx \\]

where $k^2=\dfrac{2mE}{\hbar^2}$. By the boundary conditions, we get

\\[  B=0,\;kL=n\pi \\]

Therefore, we determine the energy.

\\[  E=\frac{\hbar^2 k^2}{2m}=\frac{n^2\pi^2\hbar^2}{2mL^2} \\]

Now let's find the wave function.

\\[ \psi(x)=A\sin\left(\frac{n\pi x}{L}\right) \\]

$A$ is determined by normalization:

\\[ \begin{align\*}
\int_{-\infty}^{\infty} \abs{\psi(x)}^2dx &= \abs{A}^2 \int_0^L \sin^2\left(\frac{n\pi x}{L}\right)dx \nl
&= \abs{A}^2 \cdot \frac{L}{2} \nl
&= 1
\end{align\*} \\]

Therefore, we get the wavefunction.

\\[ \psi(x)=\sqrt{\frac{2}{L}}\sin\left(\frac{n\pi x}{L}\right)  \\]

The results are summarized as follows.

\\[ \psi_n(x)=\sqrt{\frac{2}{L}}\sin\left(\frac{n\pi x}{L}\right) \\]
\\[ E_n=\frac{n^2\pi^2\hbar^2}{2mL^2} \\]

![Solutions](https://upload.wikimedia.org/wikipedia/commons/f/f0/Particle-in-a-box-wave-functions.svg)
_Examples of eigen-wavefunction_

The formula shows that the energy of a particle is **quantized** (not continuous).
Also, in the **ground state**, the energy of the particle is not zero, meaning that the particle can never "sit still".
Additionally, it is more likely to be found at certain positions than at others, depending on its energy level.
The particle may never be detected at certain positions, known as spatial **nodes**.

### Expectation values

\\[ \begin{align\*}
\expct{x} &= \int_0^L \psi^\ast x\psi \,dx \nl
&= \frac{2}{L} \int_0^L x\sin^2\left(\frac{n\pi x}{L}\right) dx \nl
&= \frac{L}{2}
\end{align\*} \\]

This means that the particles are observed in the center of the box on average.

\\[ \begin{align\*}
\expct{x^2} &= \int_0^L \psi^\ast x^2 \psi \,dx \nl
&= \frac{2}{L} \int_0^L x^2\sin^2\left(\frac{n\pi x}{L}\right) dx \nl
&= L^2\left(\frac{1}{3}-\frac{1}{2n^2\pi^2}\right)
\end{align\*} \\]
<br>
\\[ \begin{align\*}
\expct{p} &= \int_0^L \psi \left(-i\hbar\frac{\partial\psi}{\partial x}\right) dx \nl 
&= -\frac{2i\hbar}{L} \int_0^L \sin\left(\frac{n\pi x}{L}\right) \frac{d}{dx}\left[\sin\left(\frac{n\pi x}{L}\right)\right] dx \nl
&= 0
\end{align\*} \\]

Since the particle has movement in both $+x$ and $-x$ directions, the average momentum measurement is zero.

\\[ \begin{align\*}
\expct{p^2} &= \int_0^L \psi \left(-\hbar^2\frac{\partial^2\psi}{\partial x^2}\right) dx \nl
&= -\frac{2\hbar^2}{L} \int_0^L \sin\left(\frac{n\pi x}{L}\right) \frac{d^2}{dx^2}\left[\sin\left(\frac{n\pi x}{L}\right)\right] dx \nl
&= \left(\frac{n\pi\hbar}{L}\right)^2
\end{align\*} \\]

### Uncertainty principle

\\[ \begin{align\*}
\sigma_x &= \frac{L}{2}\sqrt{\frac{1}{2}-\frac{2}{n^2\pi^2}} \nl
\sigma_p &= \frac{n\pi\hbar}{L}
\end{align\*} \\]

\\[ \therefore \sigma_x\sigma_p = \frac{\hbar}{2}\sqrt{\frac{n^2\pi^2}{3}-2} \ge \frac{\hbar}{2} \\]

### Correspondence principle

![Correspondence principle](https://w.namu.la/s/107f7879227979921b03e5968eec1bc821e49e7f220406c63cf0bf2b49c922987b2ef292b3e21f339d280e38cac3b1f09f89309ef3784169fd84ef8a1e697cd8a3a167318271131d108405c8dd4a763b3416202833bc9a743af3f00ba967bcdb){: w="500" }
_Comparison of probability density at very large quantum number $n$ with classical mechanics_ 

\\[ P_\text{CM}=\frac{1}{L} \\]

\\[ \begin{align\*}
P_\text{QM} &= \frac{2}{L}\sin^2\left(\frac{n\pi x}{L}\right) \nl
&= \frac{1}{L}\left[1-\cos\left(\frac{2\pi nx}{L}\right)\right]
\end{align\*} \\]

When $n$ becomes very large, the probability at $a<x<b$ converges to:

\\[ \lim_{n\to\infty}\int_a^b P_\text{QM} \,dx = \frac{b-a}{L} \\]

This is indistinguishable from classical results; called the **correspondence principle**.

## Higher dimensions

### Two-dimensional solution

The potential energy is given as

\\[ V(x,y) = \begin{cases} 0 &(0<x<L_x,\; 0<y<L_y) \nl \infty &(\text{otherwise}) \end{cases}\\]

Using the time-independent Schrödinger equation,

\\[ -\frac{\hbar^2}{2m}\nabla^2\psi=E\psi  \\]

By the separation of variables, we get differential equations for $x$ and $y$, assuming that $E=E_x+E_y$.

\\[ \psi(x,y)=X(x)Y(y) \\]

\\[ -\frac{\hbar^2}{2m}\left(\frac{\partial^2}{\partial x^2}+\frac{\partial^2}{\partial y^2}\right)\psi = E\psi \\]

\\[ \Rightarrow \begin{cases}
-\dfrac{\hbar^2}{2m}\dfrac{d^2 X}{dx^2} = E_x X \nl \nl
-\dfrac{\hbar^2}{2m}\dfrac{d^2 Y}{dy^2}=  E_y Y
\end{cases} \\]

This differential equation is identical to the one-dimensional box, so we get:

\\[ \psi_{n_xn_y}(x,y)=\sqrt{\frac{4}{L_xL_y}}\sin\left(\frac{n_x\pi x}{L_x}\right)\sin\left(\frac{n_y\pi y}{L_y}\right) \\]
\\[ E_{n_xn_y}=\frac{\pi^2\hbar^2}{2m}\left[\left(\frac{n_x}{L_x}\right)^2 + \left(\frac{n_y}{L_y}\right)^2\right] \\]

Note that at $(n_x,n_y)=(a,b)$ and $(n_x,n_y)=(b,a)$, the wavefunctions are different but the energy has the same value.
This is called a **degeneration**, and such states are called **degenerated states**.

![2D well](https://upload.wikimedia.org/wikipedia/commons/6/6d/Particle2D.svg)
_The wavefunction of a 2D well with $(n_x,n_y)=(4,4)$_

### Three-dimensional solution

It is almost the same as the previous ones.

\\[ \psi_{n_xn_yn_z}(x,y,z)=\sqrt{\frac{8}{L_xL_yL_z}}\sin\left(\frac{n_x\pi x}{L_x}\right)\sin\left(\frac{n_y\pi y}{L_y}\right)\sin\left(\frac{n_z\pi z}{L_z}\right) \\]
\\[ E_{n_xn_yn_z}=\frac{\pi^2\hbar^2}{2m}\left[\left(\frac{n_x}{L_x}\right)^2 + \left(\frac{n_y}{L_y}\right)^2 + \left(\frac{n_z}{L_z}\right)^2\right] \\]

Degeneration occurs in this case, too.

### Hyperrectangular well

An analogue for higher dimensions of the particle-in-a-box problem is as follows:

\\[ \psi_{n_1\cdots n_k}(x_1,\cdots,x_k)=\prod_{i=1}^k \sqrt{\frac{2}{L_i}} \sin\left(\frac{n_i\pi x_i}{L_i}\right) \\]
\\[ E_{n_1\cdots n_k}=\frac{\pi^2\hbar^2}{2m}\sum_{i=1}^k \left(\frac{n_i}{L_i}\right)^2 \\]


## Circular infinite potential well

The potential energy of a particle confined in a circular infinite well is given as

\\[ V(x) = \begin{cases} 0 &(\rho<R) \nl \infty &(\rho\ge R) \end{cases}\\]

Using the time-independent Schrödinger equation,

\\[ \begin{align\*}
-\frac{\hbar^2}{2m}\nabla^2\psi &=
-\frac{\hbar^2}{2m}\left[ \frac{1}{\rho}\frac{\partial}{\partial\rho}\left(\rho\frac{\partial}{\partial\rho}\right) +
\frac{1}{\rho^2}\frac{\partial^2}{\partial\phi^2} \right] \psi \nl
&= E\psi
\end{align\*} \\]

By the separation of variables, we get differential equations for $\rho$ and $\phi$. Let's put $k^2=\dfrac{2mE}{\hbar^2}$.

\\[ \psi(\rho,\phi)=C\Rho(\rho)\Phi(\phi) \\]

\\[ \frac{\rho}{\Rho}\frac{d}{d\rho}\left(\rho\frac{d\Rho}{d\rho}\right) + 
\frac{1}{\Phi}\frac{d^2\Phi}{d\phi^2} + k^2\rho^2 = 0  \\]

Let's assume that:

\\[ \frac{1}{\Phi}\frac{d^2\Phi}{d\phi^2}=-m^2 \\]

Then we get the solution for $\Phi$.

\\[ \Phi(\phi)=e^{im\phi} \\]

Since it has to satisfy the spherical symmetry $\Phi(\phi)=\Phi(\phi+2\pi)$, we get that $m\in\Z$.

The differential equation of $\rho$ is:

\\[ \rho\frac{d}{d\rho}\left(\rho\frac{d\Rho}{d\rho}\right) + (k^2\rho^2-m^2)\Rho = 0 \\]

The solutions of this differential equation are the _Bessel function_ $J_m(k\rho)$ and the _Neumann function_ $Y_m(k\rho)$.
However, Neumman functions cannot be the solution to this problem since $\dps \lim_{x\to0}Y_m(x)=-\infty$.

Therefore, we get the solution for $\Rho$.

\\[ \Rho(\rho)=J_m(k\rho) \\]

Since we have the boundary condition $\Phi(R)=0$, we get following equation where $j_{mn}$ is the $n$th zero point
of the Bessel function $J_m(x)$.

\\[ kR=j_{mn} \\]

Therefore, we can determine the energy and the wavefunction.

\\[ E_{mn}=\frac{j_{mn}^2\hbar^2}{2mR^2} \\]

\\[ \psi_{mn}(\rho,\phi)=C_{mn}J_{m}\left(\frac{j_{mn}\rho}{R}\right)e^{im\phi} \\]

Let's normalize it. By the orthogonality of the Bessel function,

\\[ \begin{align\*}
\int_0^{2\pi} \int_0^R \abs{\psi_{mn}}^2 \rho \, d\rho d\phi
&= \abs{C_{mn}}^2 \int_0^{2\pi}d\phi \int_0^R \rho J_m\left(\frac{j_{mn}\rho}{R}\right)^2 d\rho \nl
&= \pi\abs{C_{mn}}^2 J_m\rq(j_{mn})^2 \nl
&= 1
\end{align\*} \\]

The results are summarized as follows.

\\[ \psi_{mn}(\rho,\phi) = \frac{1}{\sqrt{\pi}\abs{J_m\rq(j_{mn})}} J_{m}\left(\frac{j_{mn}\rho}{R}\right)e^{im\phi} \\]
\\[ E_{mn}=\frac{j_{mn}^2\hbar^2}{2mR^2} \\]

![Circular infinite well](https://w.namu.la/s/bf6f8a245a2e4549a157543fb331ee98567a64739a0d1d4222833ff48aacdf2460214b445f5aec2b29ef79b81031c38e3a5568054bdba29ddbcba6ab3a322906a0faa067682a0a8fd6722b3443bc7d45b41451d06a3553031f84e2cf304b53af0e6828c4c8389cc55af8eb7c45687094)
_Probability density function for $(n,m)=(1,2)$._
