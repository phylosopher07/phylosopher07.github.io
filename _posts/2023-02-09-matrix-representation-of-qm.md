---
title: Matrix representation of Quantum Mechanics
subtitle: Quantum Mechanics 1.4
author: jiho
date: 2023-02-09 18:00:00 +0800
categories: [Learning, Physics, Quantum Mechanics]
tags: [physics, quantum mechanics, matrix mechanics]
math: true
---
$ \global\def\nl{\newline} $
$ \global\def\dps{\displaystyle} $
$ \global\def\b{\bold} $
$ \global\def\brkt#1#2{\braket{#1\|#2}} $
$ \global\def\Brkt#1#2{\Braket{#1\|#2}} $
$ \global\def\brktop#1#2#3{\braket{#1\|#2\|#3}} $
$ \global\def\Brktop#1#2#3{\Braket{#1\|#2\|#3}} $

## Matrix representation of state vectors

Any state vector can be represented by the sum of eigenvectors for an Hermitian operator $L$.
* $ \dps \ket{\psi}=\sum_n c_n\ket{\psi_n} $

Then, we can use those eigenvectors as a basis, with coordinates $c_n$.
The state vector can be represented as a column vector:

\\[ \ket{\psi} \longrightarrow \begin{bmatrix} c_1 \nl c_2 \nl c_3 \nl \vdots \end{bmatrix},\;
\bra{\psi} \longrightarrow \begin{bmatrix} c_1^\ast & c_2^\ast & c_3^\ast & \cdots \end{bmatrix} \\]

And if the eigenvectors are _orthonormal_; $\brkt{\psi_n}{\psi_m}=\delta_{nm}$;
it can be represented with inner products: 

\\[ \ket{\psi} \longrightarrow
\begin{bmatrix} \brkt{\psi_1}{\psi} \nl \brkt{\psi_2}{\psi} \nl \brkt{\psi_3}{\psi} \nl \vdots \end{bmatrix} \\]

If we use $[\cdot]$ to denote matrix representation, an inner product is expressed as follows.
* $ \brkt{f}{g} = [f]^\dag [g]$

## Matrix representation of operators

An operator can be represented as a matrix similary:

\\[ T \longrightarrow
\begin{bmatrix}
\brktop{\psi_1}{\hat{T}}{\psi_1} & \brktop{\psi_1}{\hat{T}}{\psi_2} & \brktop{\psi_1}{\hat{T}}{\psi_3} & \cdots \nl
\brktop{\psi_2}{\hat{T}}{\psi_1} & \brktop{\psi_2}{\hat{T}}{\psi_2} & \brktop{\psi_2}{\hat{T}}{\psi_3} & \cdots \nl
\brktop{\psi_3}{\hat{T}}{\psi_1} & \brktop{\psi_3}{\hat{T}}{\psi_2} & \brktop{\psi_3}{\hat{T}}{\psi_3} & \cdots \nl
\vdots & \vdots & \vdots & \ddots
\end{bmatrix} \\]

Then, an operation at a state vector is identical with general matrix multiplication.

* $ \hat{T}\ket{f} \longrightarrow [T][f] $
* $ \brktop{f}{\hat{T}}{g} \longrightarrow [f]^\dag[T][g] $

Also, following identity is true for any linear operator $T$.
* $ [T^\dag]=[T]^\dag $