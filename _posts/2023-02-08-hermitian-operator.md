---
title: Hermitian operator
subtitle: Quantum Mechanics 1.3
author: jiho
date: 2023-02-08 15:00:00 +0800
categories: [Learning, Physics, Quantum Mechanics]
tags: [physics, quantum mechanics, hermitian, self-adjoint, operator, eigenvalue, expectation value]
math: true
---

## Hermitian operator

A **Hermitian operator**, or **self-adjoint operator** is an operator that is equal to its own hermitian conjugate.
* $ \hat{A}=\hat{A}^\dag $

Since operators with such properties are treated very importantly in quantum mechanics,
we're going to summarize their properties from now on.

## Expectation value of Hermitian operator is real

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

## Different eigenfunctions of Hermitian operator are orthogonal

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

### Measurements and probabilities
The result above implies that any wavefunction can be represented as the sum of eigenfunctions of an observable,
which are elements of an orthogonal basis.

\\[ \ket{\psi}=\sum_n c_n\ket{\psi_n} \enspace \left( \sum_n \|c_n\|^2=\brkt{\psi}{\psi} \right) \\]

If then, the **probability** for observing the state $\ket{\psi_n}$ is proportional to
$\|⟨\psi_n\|\psi⟩\|^2 = \|c_n\|^2$; suppose it's $k\|c_n\|^2$.
The overall probability $k\brkt{\psi}{\psi}$ should be $1$, and this results:
* $ P(\psi_n)=\dfrac{\|c_n\|^2}{\brkt{\psi}{\psi}} $

And if $\ket{\psi}$ is _normalized_,
* $ P(\psi_n)=\|c_n\|^2 $.

Keep in mind that in quantum mechanics, a measure of the physical quantity becomes one of the **eigenvalues**,
not the expectation value.

### Normalization
And this also implies that if state vector $\ket{f}$ and $\ket{g}$ are in following relation,
they're representing identical physical system.
* $ \ket{f}=c\ket{g} \;(c\in\Complex) $

Then we can **normalize** any state vectors using _phase factors_ $e^{iz}$, of which norm is $1$.
* $ \ket{\psi} \to \dfrac{e^{iz}\ket{\psi}}{\sqrt{\brkt{\psi}{\psi}}}$

### Wavefunction collapse

The measurement transforms the system to become an eigenvector for the measured value,
which is called a **wavefunction collapse**.
(It can be understood that it collapses the probability of an eigenvalue different from the measured value.)

\\[ \ket{\psi} \xrightarrow[\text{eigenvalue}:\; l \;/\; \text{eigenvector}:\; \ket{l}]{\text{observable}:\; L} \ket{l} \\]

## Extra
For any operator $\hat{A}$, all of the following operators are hermitian.
* $ \hat{A}+\hat{A}^\dag $
* $ i(\hat{A}-\hat{A}^\dag) $
* $ \hat{A}\hat{A}^\dag $

Also, there's an property about a commutator:
* $ [\hat{A},\hat{B}]=0 \Rightarrow \hat{A}\hat{B}=\left(\hat{A}\hat{B}\right)^\dag $

We'll talk about commutators later.
