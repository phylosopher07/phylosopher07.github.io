---
title: Hermitian operator
subtitle: Quantum Mechanics 1.3
author: jiho
date: 2023-02-08 15:00:00 +0800
categories: [Learning, Physics, Quantum Mechanics]
tags: [physics, quantum mechanics, hermitian, self-adjoit, operator, eigenvalue, expectation]
math: true
---
$ \global\def\nl{\newline} $
$ \global\def\dps{\displaystyle} $
$ \global\def\b{\bold} $
$ \global\def\brkt#1#2{\braket{#1\|#2}} $
$ \global\def\Brkt#1#2{\Braket{#1\|#2}} $
$ \global\def\brktop#1#2#3{\braket{#1\|#2\|#3}} $
$ \global\def\Brktop#1#2#3{\Braket{#1\|#2\|#3}} $

## Hermitian operator

A **Hermitian operator**, or **self-adjoint operator** is an operator that is equal to its own hermitian conjugate.
* $ \hat{A}=\hat{A}^\dag $

Since operators with such properties are treated very importantly in quantum mechanics,
we're going to summarize their properties from now on.

### Expectation value of Hermitian operator is real

\\[  \langle\hat{A}\rangle = \brkt{\psi}{\hat{A}\psi} \\]

\\[ \begin{align\*}
\langle\hat{A}\rangle^\ast &= \brkt{\psi}{\hat{A}\psi}^\ast \nl
&= \brkt{\hat{A}\psi}{\psi} \nl
&= \brkt{\hat{A}^\dag \psi}{\psi} \nl
&= \brkt{\psi}{\hat{A}\psi}
\end{align\*} \\]

\\[  \therefore\; \langle\hat{A}\rangle = \langle\hat{A}\rangle^\ast  \\]

This implies that the physical quantities of Hermitian operators are observable;
in this respect, Hermitian operators are called **observables**.

### Different eigenfunctions of Hermitian operator are orthogonal

\\[ \begin{cases}
\hat{A}\ket{\psi_n}=a_n\ket{\psi_n} \nl
\hat{A}\ket{\psi_m}=a_m\ket{\psi_m}
\end{cases} \\]

\\[ \begin{cases}
\brkt{\psi_n}{\hat{A}\psi_m} = a_m\brkt{\psi_n}{\psi_m} \nl
\brkt{\hat{A}\psi_n}{\psi_m} = a_n^\ast\brkt{\psi_n}{\psi_m} = a_n\brkt{\psi_n}{\psi_m}
\end{cases} \\]

\\[ \Rightarrow (a_n-a_m)\brkt{\psi_n}{\psi_m}=0 \\]

\\[ \therefore \brkt{\psi_n}{\psi_m}=\delta_{nm} \\]

This implies that any _normalized wavefunction_ can be represented as the sum of eigenfunctions of an observable,
which are elements of an orthogonal basis.

\\[ \ket{\psi}=\sum_n c_n\ket{\psi_n} \enspace \left( \sum_n \|c_n\|^2=1 \right) \\]

If then, the **probability** for observing the state $\ket{\psi_n}$ is $\|c_n\|^2$.
Keep in mind that in quantum mechanics, a measure of the physical quantity becomes one of the **eigenvalues**,
not the expectation value.

### Extra
For any operator $\hat{A}$, all of the following operators are hermitian.
* $ \hat{A}+\hat{A}^\dag $
* $ i(\hat{A}-\hat{A}^\dag) $
* $ \hat{A}\hat{A}^\dag $
