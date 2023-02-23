---
title: Schrödinger equation
subtitle: Quantum Mechanics 1.6
author: jiho
date: 2023-02-10 09:00:00 +0800
categories: [Learning, Physics, Quantum Mechanics]
tags: [physics, quantum mechanics, schrödinger equation, wavefunction]
math: true
---

## Prerequisites

Like a photon, the momentum and energy of a quantum-like particle
with wave-like properties and particle-like properties(i.e., duality) are summarized as follows.
(Duality derived by De Broglie)
* $ p=\dfrac{h}{\lambda}=\hbar k $
* $ E=h\nu=\hbar\omega $

Since we are considering particles with this duality, let's use wavefunction in classical mechanics.
* $ \psi(\b{r},t)=Ae^{i(\b{k}\cdot\b{r}-\omega t)} $

## Induction of time-dependent Schrödinger equation

Then,
* $ \nabla\psi = i\b{k}\psi = \dfrac{i}{\hbar}\b{p}\psi $
* $ \b{p}\psi=-i\hbar\nabla\psi $

Thus, the **momentum operator** in the position space is as follows. 

\\[ \hat{\b{p}}=-i\hbar\nabla \\]

We can write a **Hamiltonian operator** using this result:
* $ \hat{\mathcal{H}} = \hat{T}+\hat{V} = \dfrac{\hat{p}^2}{2m}+\hat{V} = -\dfrac{\hbar^2}{2m}\nabla^2+\hat{V} $

Summarizing,

\\[ \hat{\mathcal{H}} = -\dfrac{\hbar^2}{2m}\nabla^2+\hat{V} \\]

Also,
* $ \dfrac{\partial\psi}{\partial t} = -i\omega\psi = -\dfrac{i}{\hbar}E\psi $
* $ E\psi = i\hbar\dfrac{\partial}{\partial t}\psi $

Since the eigenvalue of a Hamiltonian operator is energy,
we finally get **time-dependent Schrödinger equation**.
Let's rewrite the wavefunction $\psi$ to the state vector $\ket{\Psi(t)}$.

\\[\boxed{  i\hbar\frac{\partial}{\partial t}\ket{\Psi(t)} = \hat{\mathcal{H}}\ket{\Psi(t)}  }\\]

## Induction of time-independent Schrödinger equation

Now let's separate the state vector into terms for time and terms for Hamiltonian's eigenfunctions
assuming that the Hamiltonian is _independent_ for time.
* $ \ket{\Psi(t)}=T(t)\ket{\psi} $

Then we get **time-independent Schrödinger equation**.
\\[\boxed{  \hat{\mathcal{H}}\ket{\psi}=E\ket{\psi}  }\\]

The solutions (_eigenfunctions of the Hamiltonian_) obtained through the separation of variables are not all solutions of the Schrödinger equation,
but all solutions can be expressed by the basis containing those eigenfunctions.

\\[ \begin{align\*}
i\hbar\frac{\partial}{\partial t}\ket{\Psi(t)} &= i\hbar\frac{\partial T}{\partial t}\ket{\psi} \nl
= \hat{\mathcal{H}}\ket{\Psi(t)} &= ET\ket{\psi}
\end{align\*} \\]

\\[ \Rightarrow  i\hbar\frac{\partial T}{\partial t}=ET \\]

\\[ T(t) = e^{-i\frac{E}{\hbar}t} \\]
$T$ is called a **time-evolution operator** or a **propagator**.

\\[ \therefore  \ket{\Psi(t)}=e^{-i\frac{E}{\hbar}t}\ket{\psi} \\]

Therefore, if we fully know the state vector at $t=0$, it is possible to describe how the system changes over time.
\\[ \therefore  \ket{\Psi(t)}=\sum_n \brkt{\psi_n}{\Psi(0)}e^{-i\frac{E_n}{\hbar}t}\ket{\psi_n} \\]
