---
layout: post
title: "Variational Method"
subtitle: "qmun"
classification: "Quantum Mechanics Unclassified"
categories: physics
tags: quantum-mechanics
image:
    path: /assets/img/physics/quantum-mechanics/Sakurai.svg
---

from **「Modern Quantum Mechanics」**: _Sakurai, J. J._
{:.figcaption}

> The numerical method to analyze quantum systems.

<!--more-->
* this unordered seed list will be replaced by the toc
{:toc}

## Variational method

**Variational method** is one way of finding approximations to the _ground state_, and some _excited states_.
This allows for calculating approximate wavefunctions such as _molecular orbitals_.
The basis for this method is the variational principle.

The method consists of choosing a **"trial wavefunction"** depending on one or more parameters,
and finding the values of these parameters for which the expectation value of the energy is the _lowest_ possible.
The wavefunction obtained by fixing the parameters to such values is then an approximation to the ground state wavefunction,
and the expectation value of the energy in that state is an upper bound to the ground state energy.

$ \global\def\psit{\psi_\text{trial}} $
$ \global\def\Egs{E_\text{gs}} $

\\[ \brktop{\psit}{ \hat{H} }{\psit}\ge \Egs \\]

Since the wavefunction is an element of Hilbert space, it can be represented as a linear combination of the eigenfunctions of the Hamiltonian.

\\[ \ket{\psit} = \sum_n \ket{\psi_n}\brkt{\psi_n}{\psit} \\]

Therefore, the expectation value of the Hamiltonian is:

\\[ \begin{align\*}
\expct{\hat{H}} &= \sum_n \abs{\brkt{\psi_n}{\psit}}^2 E_n \nl
&= \sum_n \abs{\brkt{\psi_n}{\psit}}^2 (E_n-\Egs) + \Egs \nl
&\ge \Egs
\end{align\*} \\]

Also, we can compute an upper bound to the energy level of the _first excited state_ similarly.
If we fully know the ground state wavefunction $\psi_\text{gs}$ and have the trial wavefunction orthogonal to it,
i.e. $\brkt{\psi_\text{gs}}{\psit}=0$, we get:

\\[ \expct{\hat{H}} \ge E_\text{fe} \\]

Trivially,

\\[ \begin{gather\*}
\begin{cases} \brkt{\psi_\text{gs}}{\psit}=0 \nl \brkt{\psi_\text{fe}}{\psit}=0 \end{cases}
\Rightarrow \expct{\hat{H}}\ge E_\text{se} \nl
\vdots
\end{gather\*} \\]
