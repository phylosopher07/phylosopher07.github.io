---
title: Helium Atom
subtitle: Unclassified
author: jiho
date: 2023-02-19 16:00:00 +0800
categories: [Learning, Physics, Quantum Mechanics]
tags: [physics, quantum mechanics, variational method, approximation, wavefunction, ground state, helium atom, spin]
math: true
---

## Approximation of the ground state of helium atom
Let's approximate the ground state energy of helium atom using the variational method.
The Hamiltonian of the system is; ignoring the motion of nucleus (Born–Oppenheimer approximation):

$ \global\def\Zef{Z\rq} $

\\[ \hamiltonian = -\frac{\hbar^2}{2m_e}(\nabla_1^2+\nabla_2^2) -\frac{e^2}{4\pi\varepsilon_0}\left[ \frac{2}{r_1}+\frac{2}{r_2}-\frac{1}{\abs{\b{r}_1-\b{r}_2}} \right] \\]

Let's set the trial wavefunction as the product of the ground state wavefunction of the hydrogenic atom system,
ignoring the interaction of electrons, which are regarded identical. Here we add a parameter $\Zef$ for the variation.

\\[ \begin{align\*}
\psi(\b{r}_1,\b{r}_2) &= \psi _{100}(\b{r_1})\psi _{100}(\b{r}_2) \nl
&= \frac{\Zef^3}{\pi a_0^3} \exp\left[ -\frac{\Zef}{a_0}(r_1+r_2) \right]
\end{align\*} \\]

Then, let's change the Hamiltonian to the following form for simple calculations.

\\[ \hamiltonian =
\left( -\frac{\hbar^2}{2m_e}\nabla_1^2-\frac{\Zef e^2}{4\pi\varepsilon_0r_1} \right) + \left( -\frac{\hbar^2}{2m_e}\nabla_2^2-\frac{\Zef e^2}{4\pi\varepsilon_0r_2} \right)
+\frac{e^2}{4\pi\varepsilon_0}\left[ \frac{\Zef-2}{r_1}+\frac{\Zef-2}{r_2}+\frac{1}{\abs{\b{r}_1-\b{r}_2}} \right] \\]

We see that the term inside parentheses are the Hamiltonian of hydrogen-like atoms of atomic number $\Zef$, respectively.
However, here $\Zef$ doesn't have to be an integer since it's a parameter for the variational method;
it reflects the **shielding effect** (or **screening effect**) of the electrons.
Therefore, $\Zef$ is an **effective nuclear charge** $Z_\text{eff}$, and we'll calculate it later.

Recall that $\Expct{\dfrac{1}{r}}=\dfrac{\Zef}{a_0}$ is satisfied at the ground state of the hydrogen-like atom.
The expectation value of the Hamiltonian is, where $E_1$ is the ground state energy of the hydrogen:

\\[ \begin{align\*}
\expct{\hat{\hamiltonian}}
&= \Zef^2E_1 + \Zef^2E_1 + \frac{(\Zef-2)e^2}{4\pi\varepsilon_0}\left[ \Expct{\frac{1}{r_1}}+\Expct{\frac{1}{r_2}} \right] +
\frac{e^2}{4\pi\varepsilon_0}\Expct{\frac{1}{\abs{\b{r}_1-\b{r}_2}}} \nl
&= 2\Zef^2E_1-4\Zef(\Zef-2)E_1 + \frac{e^2}{4\pi\varepsilon_0}\Expct{\frac{1}{\abs{\b{r}_1-\b{r}_2}}}
\end{align\*} \\]

Let's calculate the expectation value:

\\[  aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa\\]
