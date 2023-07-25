---
layout: post
title: "Canonical Commutation Relation"
subtitle: "qm1.10"
classification: "Quantum Mechanics 1.10"
categories: physics
tags: quantum-mechanics
image:
    path: /assets/img/physics/quantum-mechanics/Sakurai.svg
---

from **「Modern Quantum Mechanics」**: _Sakurai, J. J._
{:.figcaption}

> The position and momentum operators.

<!--more-->
* this unordered seed list will be replaced by the toc
{:toc}

## Translation operator

\\[ \global\def\T{\hat{\mathscr{T}}} \\]

Let's define the spatial displacement, or _**translation operator**_ $\hat{\mathscr{T}}(\Delta\b{x})$ as follows:

\\[ \T\ket{\b{x}} \coloneqq \ket{\b{x}+\Delta\b{x}} \\]

Then, the translation operator $\T$ is unitary:

\\[ \brktop{\b{x}}{ \T^\dagger\T }{\b{x}} = \brkt{\b{x}}{\b{x}} \\]

\\[ \therefore \T^\dagger\T = \mathbb{I} \\]

Also, infinitesimal translation operator should be additional:

\\[ \T(\d\b{x}_2) \T(\d\b{x}_1) = \T(\d\b{x}_1+\d\b{x}_2) \\]

Similarly, we expect the opposite direction of translation operator is the inverse of the original one:

\\[ \T(-\d\b{x}) = \T^{-1}(\d\b{x}) \\]

Finally, we demand that as $\d\b{x}\to 0$, $\T(\d\b{x})\to \mathbb{I}$.

\\[ \lim_{\d\b{x}\to 0} \T(\d\b{x}) = \mathbb{I} \\]

These properties are satisfied if the difference between $\T(\d\b{x})$ and $\mathbb{I}$ be of the first order in \d\b{x}.
Therefore, we can demonstrate the infinitesimal translation operator in such form,

\\[ \T(\d\b{x}) = \mathbb{I} - i\b{K}\cdot\d\b{x} \\]

where the components of $\b{K}$ are Hermitian operators. The formula shows that $\b{K}$ is the generator of translation.
By a simple calculation, we can show the following commutation relation:

\\[ \com{ \b{x} }{ \T(\d\b{x}) } = \d\b{x} \\]

Therefore, we obtain the commutation relation between $\b{x}$ and $\b{K}$.

\\[ \com{ x_i }{ K_j } = i\delta_{ij} \\]

## Momentum operator

\\[ \global\def\p{\hat{\b{p}}} \\]

The momentum operator $\p$ is defined as the generator of translation, or equivalently as the gradient of the translation operator:

\\[ \p \coloneqq \hbar \left( \nabla\T(\b{x}) \middle)\right\vert_{\b{x}=\b{0}} \\]

We actually get familiar form when we expand the gradient:

\\[ \p = -i\hbar\nabla \\]

The definition of momentum operator then results some commutation relations trivially,

* $ \com{p_i}{p_j} = 0 $
* $ \com{x_i}{p_j} = i\hbar\delta_{ij} $

Also, by the fact that the momentum operator is a generator of translation, we get several properties.
First, the momentum operator is Hermitian since the translation operator is unitary.
Second, arbitrary translation operator can be expressed as follows:

\\[ \begin{align\*}
\T(\Delta\b{x})
&= \lim_{N\to\infty} \left[ 1-\frac{ i\b{p}\cdot\Delta\b{x} }{ N\hbar } \right]^N \nl
&= \exp\left( -\frac{ i\b{p}\cdot\Delta\b{x} }{ \hbar } \right)
\end{align\*} \\]

## Canonical commutation relation

We summarize the commutation relations we have obtained so far:

\\[ \begin{align\*}
\com{x_i}{x_j} &= 0 \nl
\com{p_i}{p_j} &= 0 \nl
\com{x_i}{p_j} &= i\hbar\delta_{ij}
\end{align\*} \\]