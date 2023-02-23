---
title: Bra-ket notation and Wavefunction
subtitle: Quantum Mechanics 1.2
author: jiho
date: 2023-02-08 09:00:00 +0800
categories: [Learning, Physics, Quantum Mechanics]
tags: [physics, quantum mechanics, bra-ket, state vector, operator, wavefunction]
math: true
---

## Bras & kets

A physical system is represented by a state vector $\ket{\Psi}$,
an element of **$L^2$ complex Hilbert space $\mathcal{H}$**.
(In fact, it doesn't have to be $L^2$.
See [$C^*$ formalism](https://math.uchicago.edu/~may/VIGRE/VIGRE2009/REUPapers/Gleason.pdf) who wants exactness.)
We denote the dual (covector) of the state vector as $\bra{\Psi}$. Psi is mainly used for the vectors.

$\ket{\Psi}$ is called a **ket**, and $\bra{\Psi}$ is called a **bra**.
This nomenclature is derived from _bra-c-ket_〈 〉.
$^\dagger$ denotes the hermitian conjugate.

* $ \ket{\Psi} \in \mathcal{H},\; \bra{\Psi} \in \mathcal{H}^* $
* $ \bra{\Psi}^\dagger=\ket{\Psi},\; \ket{\Psi}^\dagger=\bra{\Psi} $

An inner product is expressed as follows, where $^\ast$ denotes the complex conjugate.
* $ \brkt{\phi}{\psi} = \brkt{\psi}{\phi}^\ast  $
* $ \brkt{\phi}{c_1\psi_1+c_2\psi_2} = c_1\brkt{\phi}{\psi_1}+c_2\brkt{\phi}{\psi_2} $
* $ \brkt{c_1\phi_1+c_2\phi_2}{\psi} = c_1^\ast \brkt{\phi_1}{\psi}+c_2^\ast \brkt{\phi_2}{\psi} $

In addition, **normalized** state vectors satisfy the following property:
* $ \brkt{\psi}{\psi}=1 $

## Operators

Since we can think of ket as a vector and bra as a co-vector, a linear **operator** can be considered a square matrix.
The _hat_ $\hat{\;\;}$ is often used to indicate an operator.
(Regarding an operator as a matrix is not correct since the vectors are infinite-dimensional,
but in quantum physics, it doesn't matter.)

* $ \hat{A}\ket{\Psi} = \ket{\hat{A}\Psi},\; \bra{\Psi}\hat{A} = \bra{\hat{A}^\dagger\Psi} $
* $ \brktop{\phi}{\hat{A}}{\psi} \coloneqq \left(\bra{\phi}\hat{A}\right)\ket{\psi} 
= \bra{\phi}\left(\hat{A}\ket{\psi}\right) $

If the same state vector appears on both the bra and ket sides,
* $ \langle\hat{A}\rangle \coloneqq \brktop{\psi}{\hat{A}}{\psi} $

then this expression gives the **expectation value**, or mean or average value,
of the observable represented by operator $\hat{A}$ for the physical system in the state $\ket{\psi}$.

A convenient way to define linear operators on a Hilbert space is given by the outer product :
* $ \ket{\phi}\bra{\psi} $

One of the uses of the outer product is to construct projection operators. Given a ket $\ket{\psi}$ of norm $1$,
the orthogonal projection onto the subspace spanned by $\ket{\psi}$ is :
* $ \ket{\psi}\bra{\psi} $

## Basis

State vectors are elements of infinite-dimensional Hilbert space, which is a vector space.
This implies that there exists a basis, which spans every state vectors.
We can write this using projection operators.
* $ \dps \ket{\psi} = \sum_{i\in\N} \left( \ket{e_i} \bra{e_i} \right) \ket{\psi}
= \sum_{i\in\N} \brkt{e_i}{\psi} \ket{e_i} $
* $ \dps \sum_{i\in\N} \ket{e_i} \bra{e_i} = \mathbb{I} $

## Position space and wavefunction

Any vectors that generate the Hilbert space can be a basis.
Let's take a look at **position space** first.
This label is the eigenvalue of the position operator acting on such a basis state,
$ \hat{\b{r}}\ket{\b{r}} = \b{r}\ket{\b{r}}$.

The $\ket{\b{r}}$ are the basis vectors, which are orthonormal so their inner product is a delta function;
* $ \brkt{\b{r}\rq}{\b{r}} = \delta^3(\b{r}\rq-\b{r}) $

Thus, starting from any ket $\ket{\Psi}$ in this Hilbert space,
one may define a complex scalar function $\Psi(\b{r})$, known as a **wavefunction** :
* $ \Psi(\b{r}) \coloneqq \brkt{\b{r}}{\Psi} $
* $ \dps \ket{\Psi} = \int d^3\b{r}\; \Psi(\b{r})\ket{\b{r}} $
* $ \hat{A}(\b{r})\Psi(\b{r}) = \brktop{\b{r}}{\hat{A}}{\Psi} $

Let's re-write the properties of state vectors with wavefunctions.
* $ \dps \brkt{\phi}{\psi} = \int \phi(\b{r})^\ast \psi(\b{r}) d^3\b{r} $
* $ \dps \brkt{\psi}{\psi} = \int \| \psi(\b{r}) \|^2 d^3\b{r} \enspace$ ($1$ if _normalized_)

We'll talk about _momentum space_ later.
