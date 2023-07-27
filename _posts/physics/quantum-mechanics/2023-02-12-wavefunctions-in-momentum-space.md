---
layout: post
title: "Wavefunctions in Momentum Space"
subtitle: "qm1.11"
classification: "Quantum Mechanics 1.11"
categories: physics
tags: quantum-mechanics
image:
    path: /assets/img/physics/quantum-mechanics/Sakurai.svg
---

from **「Modern Quantum Mechanics」**: _Sakurai, J. J._
{:.figcaption}

> The position and momentum operators.

<!--more-->
* this unordered seed list will be replaced by the toc
{:toc}

## Momentum space

We've seen that the wavefunction in position space is given by as follows, where $\ket{\alpha}$ is an arbitrary state vector.

\\[ \hat{\b{x}}\ket{\b{x}\rq} = \b{x}\rq\ket{\b{x}\rq} \\]
\\[ \psi_\alpha(\b{x}) = \brkt{\b{x}}{\alpha} \\]

Similarly, we can describe the wavefunction in momentum space, too.

\\[ \hat{\b{p}}\ket{\b{p}\rq} = \b{p}\rq\ket{\b{p}\rq} \\]
\\[ \phi_\alpha(\b{p}) = \brkt{\b{p}}{\alpha} \\]

Let's discuss eigenstate and eigenvalue of the momentum operator at 1-dimensional position space.
We cet get such differential equation:

\\[ p\brkt{x}{p} = -i\hbar\pdv{ }{x} \brkt{x}{p} \\]

The solution is,

\\[ \brkt{x}{p} = A \exp\left( \frac{ipx}{\hbar} \right) \\]

To get the normalization constant $A$, let's consider following inner product:

\\[ \brkt{x_1}{x_2} = \int \d{p} \brkt{x_1}{p}\brkt{p}{x_2} \\]

LHS is actually $\delta(x_1-x_2)$, and RHS can be evaluated using the solution above.

\\[ \begin{align\*}
\delta(x_1-x_2)
&= \abs{A}^2 \int \d{p} \exp\left[ \frac{ip(x_1-x_2)}{\hbar} \right]
&= 2\pi\hbar\abs{A}^2 \delta(x_1-x_2)
\end{align\*} \\]

Choosing $A$ to be real and positive by convention, we have

\\[ \brkt{x}{p} = \frac{1}{\sqrt{2\pi\hbar}} \exp\left( \frac{ipx}{\hbar} \right) \\]

We can now demonstrate how the position and momentum wavefunctions are related to each other.
It'd be done just by substituting the momentum eigenstate into the following equations.

\\[ \begin{gather\*}
\brkt{x}{\alpha} = \int \d{p} \brkt{x}{p}\brkt{p}{\alpha} \nl
\brkt{p}{\alpha} = \int \d{x} \brkt{p}{x}\brkt{x}{\alpha}
\end{gather\*} \\]

\\[ \begin{gather\*}
\psi(x) = \frac{1}{\sqrt{2\pi\hbar}} \int \d{p} \exp\left( \frac{ipx}{\hbar} \right) \phi(p) \nl
\phi(p) = \frac{1}{\sqrt{2\pi\hbar}} \int \d{x} \exp\left( -\frac{ipx}{\hbar} \right) \psi(x)
\end{gather\*} \\]

The pair of equations are exactly the Fourier transform and the inverse Fourier transform.

## Generalization to Three dimensions

Similarly, we get the 3-dimensional analogue of the equations above.

\\[ \begin{gather\*}
\psi(\b{x}) = \frac{1}{\sqrt{2\pi\hbar}^3} \int \d^3{\b{p}} \exp\left( \frac{i\b{p}\cdot\b{x}}{\hbar} \right) \phi(\b{p}) \nl
\phi(\b{p}) = \frac{1}{\sqrt{2\pi\hbar}^3} \int \d^3{\b{x}} \exp\left( -\frac{i\b{p}\cdot\b{x}}{\hbar} \right) \psi(\b{x})
\end{gather\*} \\]