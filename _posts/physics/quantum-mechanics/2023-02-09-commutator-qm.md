---
layout: post
title: "Commutator"
subtitle: "qm1.4"
classification: "Quantum Mechanics 1.4"
categories: physics
tags: quantum-mechanics
image:
   path: /assets/img/physics/quantum-mechanics/Sakurai.svg
---

from **「Modern Quantum Mechanics」**: _Sakurai, J. J._
{:.figcaption}

> Commutators not only imply the non-commutativity of operators. You should look further.

<!--more-->
* this unordered seed list will be replaced by the toc
{:toc}

## Commutator

For operators $\hat{A}$ and $\hat{B}$ acting on wavefunctions,
the following operator is called the **`commutator`** of $\hat{A}$ and $\hat{B}$.

\\[
\comm{\hat{A}}{\hat{B}} \coloneqq \hat{A}\hat{B}-\hat{B}\hat{A}
\\]

If $\comm{\hat{A}}{\hat{B}}=0$, we say that, $\hat{A}$ and $\hat{B}$ ***commute***.
In other words, there is no difference between the result of acting $\hat{A}$ after acting $\hat{B}$,
and the result of acting $\hat{B}$ after acting $\hat{A}$.

### Properties
1. Bilinearity
   * $ \comm{\hat{A}+\hat{B}}{\hat{C}} = \comm{\hat{A}}{\hat{C}}+\comm{\hat{B}}{\hat{C}} $
   * $ \comm{\hat{A}}{\hat{B}+\hat{C}} = \comm{\hat{A}}{\hat{B}}+\comm{\hat{A}}{\hat{C}} $
2. Alternativity
   * $ \comm{\hat{A}}{\hat{B}} = -\comm{\hat{B}}{\hat{A}} $
3. Jacobi identity
   * $ \comm{\hat{A}}{\comm{\hat{B}}{\hat{C}}} + \comm{\hat{B}}{\comm{\hat{C}}{\hat{A}}} + 
\comm{\hat{C}}{\comm{\hat{A}}{\hat{B}}} = 0 $
4. Additional Property
   * $ \comm{\hat{A}}{\hat{B}\hat{C}} = \comm{\hat{A}}{\hat{B}}\hat{C}+\hat{B}\comm{\hat{A}}{\hat{C}} $
   * $ \comm{\hat{A}\hat{B}}{\hat{C}} = \hat{A}\comm{\hat{B}}{\hat{C}}+\comm{\hat{A}}{\hat{C}}\hat{B} $

Read [Commutator (ring theory)](https://en.wikipedia.org/wiki/Commutator) for further details.


### Condition under which two operators are commutative

* If a common eigenfunction of any two different operators exists, they commute.

\\[ \begin{cases}
A\psi=a\psi \nl
B\psi=b\psi
\end{cases} \Rightarrow \comm{A}{B}=0
\\]

It's very easy to show.

## Anticommutator

We can also define **anticommutators**:

* $ \acomm{\hat{A}}{\hat{B}} \coloneqq \hat{A}\hat{B}+\hat{B}\hat{A} $