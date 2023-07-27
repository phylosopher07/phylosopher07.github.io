---
layout: post
title: "Interpretations of the Wavefunction"
subtitle: "qm1.13"
classification: "Quantum Mechanics 1.13"
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

## Interpretations of the Wavefunction

### The Copenhagen Interpretation

The **Copenhagen interpretation** is the most widely accepted interpretation of quantum mechanics.
It was developed by Niels Bohr and Werner Heisenberg in the 1920s.
The Copenhagen interpretation is a statistical interpretation of the wavefunction,
which states that the square of the wavefunction gives the probability of finding a particle at a given position.

### Probability density and Probability current

By the Copenhagen interpretation, the probability density is given by,

\\[ \rho(\b{x},t) = \abs{\Psi(\b{x},t)}^2 \\]

Similarly, the probability current of a spin-0 particle is given by,

\\[ \b{j}(\b{x},t) = \frac{\hbar}{2mi} \left( \Psi^\ast\grad\Psi-\Psi\grad\Psi^\ast \right) \\]

We can verify whether the probability continuity equation is satisfied, since the whole probability must be conserved.

\\[ \begin{align\*}
\div\b{j}
&= \frac{\hbar}{2mi} \left( \Psi^\ast\grad^2\Psi-\Psi\grad^2\Psi^\ast \right) \nl
&= -\frac{\hbar}{2mi} \frac{2m}{\hbar^2} \left[ \Psi^\ast(\hat{H}-V)\Psi - \Psi(\hat{H}-V)\Psi^\ast \right] \nl
&= \frac{i}{\hbar} \left[ \Psi^\ast\hat{H}\Psi - \Psi\hat{H}\Psi^\ast \right] \nl
&= - \left[ \Psi^\ast \pdv{ }{t}\Psi - \Psi \pdv{ }{t}\Psi^\ast \right] \nl
&= - \pdv{ }{t} \abs{\Psi}^2 \nl
&= - \pdv{\rho}{t}
\end{align\*} \\]

Therefore, the probability continuity equation is satisfied.

\\[ \pdv{\rho}{t} + \div\b{j} = 0 \\]

## Classical limit

To understand the physical significance of the wavefunction, let's write as

\\[ \Psi(\b{x},t) = \sqrt{\rho(\b{x},t)} \exp\left[ \frac{iS(\b{x},t)}{\hbar} \right] \\]

We can then write the probability current as

\\[ \b{j} = \frac{\rho\grad S}{m} \\]

Since classically $\b{j}=\rho\b{v}$, we can assume that $\grad S/m=\b{v}$. This yields,

\\[ \grad S = \b{p} \\]

To explore the classical limit of the wavefunction, let's also substitute the wavefunction above into the Schrödinger equation.
After some complicated differentiations, we get

\\[ -\frac{\hbar^2}{2m}
\left[ \laplacian\sqrt{\rho} + \frac{2i}{\hbar} (\grad\sqrt{\rho})\cdot(\grad S)-\frac{1}{\hbar^2} \sqrt{\rho} \abs{\grad S}^2
+\frac{i}{\hbar} \sqrt{\rho} \laplacian S \right] \exp\left[ \frac{iS(\b{x},t)}{\hbar} \right] + V \sqrt{\rho} \exp\left[ \frac{iS(\b{x},t)}{\hbar} \right] =
i\hbar \left[ \pdv{\sqrt{\rho}}{t}+\frac{i}{\hbar}\sqrt{\rho}\pdv{S}{t} \right] \exp\left[ \frac{iS(\b{x},t)}{\hbar} \right]
\\]

Assume that $\; \hbar\laplacian S\ll \abs{\grad S}^2 $, we can simply the equation.

\\[ -\frac{\hbar^2}{2m} \laplacian\sqrt{\rho} - \frac{i\hbar}{m} (\grad\sqrt{\rho})\cdot(\grad S) + \frac{1}{2m} \sqrt{\rho} \abs{\grad S}^2 + V \sqrt{\rho} =
i\hbar \pdv{\sqrt{\rho}}{t} - \sqrt{\rho}\pdv{S}{t} \\]

We can then collect terms that do not explicitly contain $\hbar$ to obtain a nonlinear PDE for $S$.

\\[ \frac{1}{2m}\abs{\grad S(\b{x},t)}^2 + V(\b{x}) + \pdv{S(\b{x},t)}{t} = 0 \\]

We recognize this to be the **Hamilton-Jacobi equation** in classical mechanics, where $S(\b{x},t)$ stands for Hamiltonian's principal function.
The interpretation for the fact is that, classical mechanics is contained in quantum mechanics in the $\hbar\to0$ limit.