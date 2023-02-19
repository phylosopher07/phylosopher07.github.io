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

\\[ \hamiltonian = -\frac{\hbar^2}{2m_e}(\nabla_1^2+\nabla_2^2) -\frac{e^2}{4\pi\varepsilon_0}\left[ \frac{2}{r_1}+\frac{2}{r_2}-\frac{1}{\abs{\b{r}_1-\b{r}_2}} \right] \\]

Let's set the trial wavefunction as the product of the ground state wavefunction of the hydrogen atom system,
ignoring the interaction of electrons, which are regarded identical.

\\[ \psi(\b{r}_1,\b{r}_2) = \psi _{100}(\b{r_1})\psi _{100}(\b{r}_2) \\\]

Then, let's change the Hamiltonian to the following form for simple calculations.

\\[ \hamiltonian =
\left( -\frac{\hbar^2}{2m_e}\nabla_1^2-\frac{Ze^2}{4\pi\varepsilon_0r_1} \right) + \left( -\frac{\hbar^2}{2m_e}\nabla_2^2-\frac{Ze^2}{4\pi\varepsilon_0r_2} \right)
+\frac{e^2}{4\pi\varepsilon_0}\left[ \frac{Z-2}{r_1}+\frac{Z-2}{r_2}+\frac{1}{\abs{\b{r}_1-\b{r}_2}} \right] \\]

We see that the term inside parentheses are the Hamiltonian of hydrogen-like atoms of atomic number $Z$, respectively.
However, here $Z$ doesn't have to be an integer since it's a parameter for the variational method;
it reflects the **screening effect** of the electrons. Therefore, $Z$ is an **effective nuclear charge**, and we'll calculate it later.

Recall that $\Expct{\dfrac{1}{r}}=\dfrac{Z}{a_0}$ is satisfied at the ground state of the hydrogen-like atom.
The expectation value of the Hamiltonian is, where $E_1$ is the ground state energy of the hydrogen:

$ \global\def\Zeff{Z_\text{eff}} $

\\[ \begin{align\*}
\expct{\hat{\hamiltonian}}
&= \Zeff^2E_1 + \Zeff^2E_1 + \frac{(\Zeff-2)e^2}{4\pi\varepsilon_0}\left[ \Expct{\frac{1}{r_1}}+\Expct{\frac{1}{r_2}} \right] +
\frac{e^2}{4\pi\varepsilon_0}\Expct{\frac{1}{\abs{\b{r}_1-\b{r}_2}}} \nl
&= 2\Zeff^2E_1-4\Zeff(\Zeff-2)E_1 + \frac{e^2}{4\pi\varepsilon_0}\Expct{\frac{1}{\abs{\b{r}_1-\b{r}_2}}}
\end{align\*} \\]
