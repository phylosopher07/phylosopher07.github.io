---
title: Commutator
subtitle: Quantum Mechanics 1.5
author: jiho
date: 2023-02-09 20:00:00 +0800
categories: [Learning, Physics, Quantum Mechanics]
tags: [physics, quantum mechanics, commutator]
math: true
---

## Commutator

For operators $\hat{A}$ and $\hat{B}$ acting on wavefunctions,
the following operator is called the **commutator** of $\hat{A}$ and $\hat{B}$.

* $ \com{\hat{A}}{\hat{B}} \coloneqq \hat{A}\hat{B}-\hat{B}\hat{A} $

If $\com{\hat{A}}{\hat{B}}=0$, we say that, $\hat{A}$ and $\hat{B}$ **commute**.
In other words, there is no difference between the result of acting $\hat{A}$ after acting $\hat{B}$,
and the result of acting $\hat{B}$ after acting $\hat{A}$.

### Properties
1. Bilinearity
   * $ \com{\hat{A}+\hat{B}}{\hat{C}} = \com{\hat{A}}{\hat{C}}+\com{\hat{B}}{\hat{C}} $
   * $ \com{\hat{A}}{\hat{B}+\hat{C}} = \com{\hat{A}}{\hat{B}}+\com{\hat{A}}{\hat{C}} $
2. Alternativity
   * $ \com{\hat{A}}{\hat{B}} = -\com{\hat{B}}{\hat{A}} $
3. Jacobi identity
   * $ \com{\hat{A}}{\com{\hat{B}}{\hat{C}}} + \com{\hat{B}}{\com{\hat{C}}{\hat{A}}} + 
\com{\hat{C}}{\com{\hat{A}}{\hat{B}}} = 0 $
4. Additional Property
   * $ \com{\hat{A}}{\hat{B}\hat{C}} = \com{\hat{A}}{\hat{B}}\hat{C}+\hat{B}\com{\hat{A}}{\hat{C}} $
   * $ \com{\hat{A}\hat{B}}{\hat{C}} = \hat{A}\com{\hat{B}}{\hat{C}}+\com{\hat{A}}{\hat{C}}\hat{B} $

Read [Commutator (ring theory)](https://en.wikipedia.org/wiki/Commutator) for further details.


### Condition under which two operators are commutative

* If a common eigenfunction of any two different operators exists, they commute.

\\[ \begin{cases} A\psi=a\psi \nl B\psi=b\psi \end{cases} \Rightarrow \com{A}{B}=0 \\]

It's very easy to show.

## Anticommutator

We can also define **anticommutators**:

* $ \acom{\hat{A}}{\hat{B}} \coloneqq \hat{A}\hat{B}+\hat{B}\hat{A} $
