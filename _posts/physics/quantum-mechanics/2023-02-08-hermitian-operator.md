---
layout: post
title: "Hermitian operator"
subtitle: "qm1.3"
classification: "Quantum Mechanics 1.3"
categories: physics
tags: quantum-mechanics
image:
    path: /assets/img/physics/quantum-mechanics/Sakurai.svg
---

from **「Modern Quantum Mechanics」**: _Sakurai, J. J._
{:.figcaption}

> What we should consider are the _Hermitians_.

<!--more-->
* this unordered seed list will be replaced by the toc
{:toc}

## Hermitian operator

A **`Hermitian operator`**, or **`self-adjoint operator`** is an operator that is equal to its own hermitian conjugate.
* $ \hat{A}=\hat{A}^\dag $

Since operators with such properties are treated very importantly in quantum mechanics,
we're going to summarize their properties from now on.

## Expectation value of Hermitian operator is real

\\[
\expct{\hat{A}} = \brkt{\psi}{\hat{A}\psi}
\nt
\begin{align\*}
\expct{\hat{A}}^\ast &= \brkt{\psi}{\hat{A}\psi}^\ast \nl
&= \brkt{\hat{A}\psi}{\psi} \nl
&= \brkt{\hat{A}^\dag \psi}{\psi} \nl
&= \brkt{\psi}{\hat{A}\psi}
\end{align\*}
\nt
\therefore\; \expct{\hat{A}} = \expct{\hat{A}}^\ast
\\]

This implies that the physical quantities of Hermitian operators are observable (since it's _real_);
in this respect, Hermitian operators are called **`observables`**.

## _Orthogonality_ of eigenfunctions

\\[
\begin{cases}
\hat{A}\ket{\psi_n} = a_n\ket{\psi_n} \nl
\hat{A}\ket{\psi_m} = a_m\ket{\psi_m}
\end{cases}
\nt
\begin{cases}
\brkt{\psi_n}{\hat{A}\psi_m} = a_m\brkt{\psi_n}{\psi_m} \nl
\brkt{\hat{A}\psi_n}{\psi_m} = a_n^\ast\brkt{\psi_n}{\psi_m} = a_n\brkt{\psi_n}{\psi_m}
\end{cases}
\nt
\Rightarrow (a_n-a_m)\brkt{\psi_n}{\psi_m}=0
\nt
\therefore \brkt{\psi_n}{\psi_m}=\delta_{nm}
\\]

### Measurements and probabilities
The result above implies that any wavefunction can be represented as the sum of eigenfunctions of an observable,
which are elements of an _orthogonal basis_.

\\[ \ket{\psi}=\sum_n c_n\ket{\psi_n} \; \left( \sum_n \|c_n\|^2=\brkt{\psi}{\psi} \right) \\]

If then, the **probability** for observing the state $\ket{\psi_n}$ is proportional to
$$ \abs{\brkt{\psi_n}{\psi}}^2 = \abs{c_n}^2 $$; suppose it's $k\|c_n\|^2$.
The overall probability $ k\brkt{\psi}{\psi} $ should be $1$, and this results:
* $ P(\psi_n) = \dfrac{\abs{c_n}^2}{\brkt{\psi}{\psi}} $

And if $$ \ket{\psi} $$ is _normalized_,
* $ P(\psi_n)=\abs{c_n}^2 $.

Keep in mind that in quantum mechanics, a measure of the physical quantity becomes one of the **eigenvalues**,
not the expectation value.

### Normalization
And this also implies that if state vector $\ket{f}$ and $\ket{g}$ are in following relation,
they're representing identical physical system.
* $ \ket{f}=c\ket{g} \;(c\in\Complex) $

Then we can **normalize** any state vectors using _phase factors_ $e^{iz}$, of which norm is $1$.
* $ \ket{\psi} \to \dfrac{e^{iz}\ket{\psi}}{\sqrt{\brkt{\psi}{\psi}}} $

### Wavefunction collapse

The measurement transforms the system to become an eigenvector for the measured value,
which is called a **`wavefunction collapse`**.
(It can be understood that it collapses the probability of an eigenvalue different from the measured value.)

\\[
\ket{\psi} \xrightarrow[\text{eigenvalue}:\; l \;/\; \text{eigenvector}:\; \ket{l}]{\text{observable}:\; L} \ket{l}
\\]

## Extra
For any operator $\hat{A}$, all of the following operators are hermitian.
* $ \hat{A}+\hat{A}^\dag $
* $ i(\hat{A}-\hat{A}^\dag) $
* $ \hat{A}\hat{A}^\dag $

Also, there's a property about a _commutator_:
* $ [\hat{A},\hat{B}]=0 \Rightarrow \hat{A}\hat{B}=\left(\hat{A}\hat{B}\right)^\dag $

We'll talk about commutators later.