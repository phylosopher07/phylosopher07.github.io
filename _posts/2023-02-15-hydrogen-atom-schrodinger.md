---
title: Hydrogen Atom
subtitle: Unclassified
author: jiho
date: 2023-02-15 12:00:00 +0800
categories: [Learning, Physics, Quantum Mechanics]
tags: [physics, quantum mechanics, schrödinger equation, hydrogen atom]
math: true
---

## Introduction

The Schrödinger equation allows one to calculate the stationary states and also the time evolution of quantum systems.
Exact analytical answers are available for the non-relativistic **hydrogen atoms** and also for the **hydrogen-like atoms**
(atom or ion consisting an only electron), such as $\ce{H}$, $\ce{He+}$, $\ce{Li^2+}$, $\ce{Be^3+}$, etc.

## Schrödinger equation

The Hamiltonian of a _hydrogen-like atom_ with the atomic number $Z$ is the radial kinetic energy operator and Coulomb attraction force
between $Z$ positive protons and a negative electron. Using the time-independent Schrödinger equation, ignoring all spin-coupling interactions, and using the reduced mass
$ \mu=\dfrac{m_em_N}{m_e+m_N} $, the equation is written as:

\\[ \left( -\frac{\hbar^2}{2\mu}\nabla^2-\frac{Ze^2}{4\pi\epzro r} \right)\psi = E\psi\\]

Expanding the Laplacian in spherical coordinates:

\\[ \left[ -\frac{\hbar^2}{2\mu}\left\\{ \frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial}{\partial r}\right) +
\frac{1}{r^2\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial}{\partial\theta}\right) +
\frac{1}{r^2\sin^2\theta}\frac{\partial^2}{\partial\varphi^2} \right\\} - \frac{Ze^2}{4\pi\epzro r} \right] \psi = E\psi  \\]

This is a separable, partial differential equation that can be solved in terms of special functions. When the wavefunction is separated as a product of functions
$R(r)$, $\Theta(\theta)$ and $\Phi(\varphi)$ three independent differential functions appears:

\\[ \psi(r,\theta,\varphi) = CR(r)Y(\theta,\varphi)=CR(r)\Theta(\theta)\Phi(\varphi) \\]

\\[ \frac{1}{R}\frac{d}{dr}\left(r^2\frac{dR}{dr}\right) - \frac{2\mu r^2}{\hbar^2}\left(-\frac{Ze^2}{4\pi\epzro r}-E\right) = 
-\frac{1}{Y}\left[ \frac{1}{\sin\theta}\frac{\partial}{\partial\theta}\left(\sin\theta\frac{\partial Y}{\partial \theta}\right) + 
\frac{1}{\sin^2\theta}\frac{\partial^2 Y}{\partial \varphi^2} \right]  \\]

Since the left and right sides consist of only variables respectively, the whole term is constant. Let's put it $l(l+1)$.

\\[ \frac{1}{\Theta}\left[\sin\theta\frac{d}{d\theta}\left(\sin\theta\frac{d\Theta}{d\theta}\right)\right] + l(l+1)\sin^2\theta = 
-\frac{1}{\Phi}\frac{d^2\Phi}{d\varphi^2} \\]

With the same logic, let's put the whole term $m_l^2$. Remark that $l$ and $m_l$ are complex numbers. We finally get three differential equations:

\\[ \therefore \begin{cases}
\dps \frac{1}{R}\frac{d}{dr}\left(r^2\frac{dR}{dr}\right) - \frac{2\mu r^2}{\hbar^2}\left(-\frac{Ze^2}{4\pi\epzro r}-E\right) = l(l+1) \nl\nl
\dps \frac{1}{\Theta}\left[\sin\theta\frac{d}{d\theta}\left(\sin\theta\frac{d\Theta}{d\theta}\right)\right] + l(l+1)\sin^2\theta = m_l^2 \nl\nl
\dps \frac{1}{\Phi}\frac{d^2\Phi}{d\varphi^2} = -m_l^2
\end{cases} \\]

We know the solution for $\Phi$ and $\Theta$, where $P_l^{m_l}$ is the **associated Legendre function**.

\\[ \begin{align\*}
\Phi(\varphi) &\propto e^{im_l\phi} \nl
\Theta(\theta) &\propto P_l^{m_l}(\cos\theta)
\end{align\*} \\]

We also get the condition for $m_l$ and $l$.

\\[ \begin{align\*}
&\bullet\; m_l\in\Z ,\; \abs{m_l} \le l \nl
&\bullet\; l\in\Z ,\; l\ge0
\end{align\*} \\]

Therefore, $Y(\theta,\varphi)$ becomes the **spherical harmonic function** by setting appropriate coefficients.

\\[ \therefore Y(\theta,\varphi) = DP_l^{m_l}(\cos\theta)e^{im_l\varphi} = Y_l^{m_l}(\theta,\varphi) \\]

Let's then take a look at $R$.

\\[ \frac{d}{dr}\left(r^2\frac{dR}{dr}\right) - \frac{2\mu r^2}{\hbar^2}\left( -\frac{Ze^2}{4\pi\epzro r} -E\right)R = l(l+1)R  \\]

Let's define a new function $u(r) \coloneqq rR(r)$:

\\[ -\frac{\hbar^2}{2\mu}\frac{d^2u}{dr^2} + \left[ -\frac{Ze^2}{4\pi\epzro r}+\frac{\hbar^2}{2\mu}\frac{l(l+1)}{r^2} \right]u = Eu \\]

We can simplify the equation by _nondimensionalization_:

\\[ \begin{align\*}
\kappa &\coloneqq \frac{\sqrt{-2\mu E}}{\hbar} \nl
\lambda &\coloneqq \frac{Z\mu e^2}{2\pi\epzro\hbar^2\kappa} \nl
\rho & \coloneqq \kappa r
\end{align\*} \\]

\\[ \Rightarrow \frac{d^2u}{d\rho^2} = \left[ 1-\frac{\lambda}{\rho}+\frac{l(l+1)}{\rho^2} \right]u \\]

It is hard to solve this differential equation directly; let's try an _asymptotic analysis_.
We should find converging solutions.

\\[ \begin{cases}
\rho\to\infty &: u\rq\rq \approx u &\Rightarrow u \approx k_1e^{-\rho} \nl
\rho\to0 &: u\rq\rq \approx l(l+1)\rho^{-2}u &\Rightarrow u \approx k_2\rho^{l+1}
\end{cases} \\]

Therefore, it is possible to reset $u$ using a new function $L(\rho)$.

\\[ u \equiv \rho^{l+1}e^{-\rho}L(\rho) \\]

We then get a differential equation of $L$.

\\[ \rho\frac{d^2L}{d\rho^2} + 2(l+1-\rho)\frac{dL}{d\rho} + \left\\{\lambda-2(l+1)\right\\}L = 0 \\]

Let's use the _Frobenius method_ to solve this equation.

\\[ L=\sum_{j=0}^\infty c_j\rho^j \\]

\\[ \sum_{j=0}^\infty \Big[ j(j+1)c_{j+1} + 2(l+1)(j+1)c_j - 2jc_j + \left\\{\lambda-2(l+1)\right\\}c_j \Big]\rho^j = 0 \\]

\\[ \Rightarrow c_{j+1} = \frac{2(j+l+1)-\lambda}{(j+1)(j+2l+2)}c_j \\]

It seems to be good to use an asymptotic analysis again.

\\[ \begin{align\*} j\to\infty \;:\; c_{j+1} \approx \frac{2}{j}c_j
&\Rightarrow c_j \approx \frac{2^j}{j!}c_0 \nl
&\Rightarrow L \approx c_0\sum_{j=0}^\infty \frac{2^j}{j!}\rho^j = c_0e^{2\rho} \nl
&\Rightarrow c_0\rho^{l+1}e^\rho
\end{align\*} \\]

The solution diverges, so it cannot be the right function describing the system.
Therefore, we could guess that the recurrence relation has to be ***cut off***, after a particular term.
This implies the condition for $\lambda$.

\\[ \begin{align\*}
\lambda &= 2(j+l+1) \nl
&= 2n \;(n\in\N)
\end{align\*} \\]

Let's get back to the differential equation. By changing the variable as $x \coloneqq 2\rho$:

\\[ x\frac{d^2L}{dx^2} + (2l+2-x)\frac{dL}{dx} + (n-l-1)L = 0 \\]

This is the equation for **generalized Laguerre function**.

\\[ L \propto L_{n-l-1}^{2l+1}(x) \\]

We finally get the entire solution of $R$.

\\[ R \propto \frac{1}{r}\rho^{l+1}e^{-\rho}L_{n-l-1}^{2l+1}(2\rho) \\]

Remember that $\lambda$ was a nondimensionalizing variable, we can write $R$ as a function of $r$ where $a_0$ is **Bohr radius**.

\\[ \begin{align\*}
\rho &= \frac{r}{\kappa} \nl
&= \frac{Z\mu e^2}{2\pi\epzro\hbar^2}\cdot\frac{r}{\lambda} = \frac{Z\mu e^2}{4\pi\epzro\hbar^2}\cdot\frac{r}{n} \nl
&= \frac{Zr}{na_0} \;\left( a_0 \coloneqq \frac{4\pi\epzro\hbar^2}{\mu e^2} \right)
\end{align\*} \\]

\\[ \therefore R(r) = \left(\frac{2Zr}{na_0}\right)^l \exp\left(-\frac{Zr}{na_0}\right) L_{n-l-1}^{2l+1}\left(\frac{2Zr}{na_0}\right)  \\]

It's almost done.

\\[ \psi = C\left(\frac{2Zr}{na_0}\right)^l \exp\left(-\frac{Zr}{na_0}\right) L_{n-l-1}^{2l+1}\left(\frac{2Zr}{na_0}\right) Y_l^{m_l}(\theta,\varphi) \\]

We should normalize the wavefunction. By some complex calculations, we get:

\\[ \oint_{\Omega}\int_0^\infty \abs{\psi}^2 r^2\, drd\Omega = 1 \\]

\\[ \begin{align\*}
\therefore \psi_{nlm_l}(r,\theta,\varphi) &= \sqrt{\left(\frac{2Z}{na_0}\right)^3 \frac{(n-l-1)!}{2n \cdot (n+l)!}}
\left(\frac{2Zr}{na_0}\right)^l \exp\left(-\frac{Zr}{na_0}\right) L_{n-l-1}^{2l+1}\left(\frac{2Zr}{na_0}\right) Y_l^{m_l}(\theta,\varphi) \nl
&= \ket{n,l,m_l}
\end{align\*} \\]

Now we should calculate energy, the eigenvalue of the Hamiltonian.

Remember that $\kappa$ contained $E$:

\\[ E=-\frac{\hbar^2\kappa^2}{2\mu},\; \kappa = \frac{2Z}{\lambda a_0} \\]

We finally get the energy, where $\Ryd$ is the **Rydberg unit of energy**.

\\[ \begin{align\*}
\therefore E_n &= -\frac{\hbar^2}{2\mu}\frac{Z^2}{n^2a_0^2} \nl
&= -\frac{Z^2}{n^2}\Ryd \;\left( \Ryd \coloneqq \frac{e^2}{8\pi\epzro a_0} \right)
\end{align\*} \\]

Let's summarize.

\\[ \psi_{nlm_l}(r,\theta,\varphi) = \sqrt{\left(\frac{2Z}{na_0}\right)^3 \frac{(n-l-1)!}{2n \cdot (n+l)!}}
\left(\frac{2Zr}{na_0}\right)^l \exp\left(-\frac{Zr}{na_0}\right) L_{n-l-1}^{2l+1}\left(\frac{2Zr}{na_0}\right) Y_l^{m_l}(\theta,\varphi) \\]

\\[ E_n = -\frac{Z^2}{n^2}\Ryd \\]

![Hello](https://upload.wikimedia.org/wikipedia/commons/e/e7/Hydrogen_Density_Plots.png)

![Hydrogen 1](https://live.staticflickr.com/65535/49963063667_ff1d1e2504_o.png)
