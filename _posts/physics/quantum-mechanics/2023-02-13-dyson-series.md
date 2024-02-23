---
layout: post
title: "Dyson Series"
subtitle: "qm1.12"
classification: "Quantum Mechanics 1.12"
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

## Time Propagator

As we have seen [here](/physics/dynamical-pictures-of-qm.html), the time evolution of a state is given by the time propagator
if the hamiltonian of the system is time-independent. The time propagator is given by

\\[ \hat{\mathcal{U}}(t,t_0) = \exp\left[ -\frac{i(t-t_0)}{\hbar} \hat{H} \right] \\]

If the hamiltonian is time-dependent but still commutes with itself at different times,
the following equation holds.

\\[ \begin{gather\*}
\hat{G}(t,t_0) \coloneqq -\frac{i}{\hbar} \int_{t_0}^t \hat{H}(t\rq) \d{t\rq} \nt
\comm{\hat{H}(t)}{\hat{G}(t)} = 0 \;\Rightarrow\;
\Psi(t) = \exp\left( \hat{G}(t,t_0) \right) \Psi(t_0)
\end{gather\*} \\]

This can be proved easily. However, the equation is not always true because $\hat{H}(t)$ and $\hat{G}(t)$ do not always commute.
Therefore, we need to use the time-ordering operator $\mathcal{T}$ to make the equation true, which is known as the **Dyson series**.

## Dyson Series

The Dyson series is given by the following equation.

\\[ \hat{\mathcal{U}}(t,t_0) = \sum_{n=0}^\infty \left( -\frac{i}{\hbar} \right)^n
\int_{t_0}^t \d{t_1} \int_{t_0}^{t_1} \d{t_2} \cdots \int_{t_0}^{t_{n-1}} \d{t_n} \prod_{i=1}^n \hat{H}(t_i) \\]

From the equation above, we can know that $t_i$ are ordered. Specifically, $t\ge t_1\ge t_2\ge \cdots $.
Let's see whether the series works well as a time propagator.

\\[ \begin{align\*}
i\hbar\pdv{ }{t} \Psi(t) &=
i\hbar\pdv{ }{t} \left[ \sum_{n=0}^\infty \left( -\frac{i}{\hbar} \right)^n
\int_{t_0}^t \d{t_1} \int_{t_0}^{t_1} \d{t_2} \cdots \int_{t_0}^{t_{n-1}} \d{t_n} \prod_{i=1}^n \hat{H}(t_i) \right] \Psi(t_0) \nl
&= \hat{H}(t) \left[ \sum_{n=1}^\infty \left( -\frac{i}{\hbar} \right)^{n-1}
\int_{t_0}^t \d{t_2} \cdots \int_{t_0}^{t_{n-1}} \d{t_n} \prod_{i=2}^n \hat{H}(t_i) \right] \Psi(t_0) \nl
&= \hat{H}(t) \left[ \sum_{n=0}^\infty \left( -\frac{i}{\hbar} \right)^n
\int_{t_0}^t \d{t_1} \int_{t_0}^{t_1} \d{t_2} \cdots \int_{t_0}^{t_{n-1}} \d{t_n} \prod_{i=1}^n \hat{H}(t_i) \right] \Psi(t_0) \nl
&= \hat{H}(t) \Psi(t)
\end{align\*} \\]

The Schrödinger equation holds, so we have proved that we can write a time propagator in the form of the Dyson series.

## Time-Ordering Operator

The time-ordering operator $\mathcal{T}$ is an operator that orders the operators in the order of time.
It isn't actually an operator, since it just rearranges the sequence of the product. However, it is often called a meta-operator.
The time-ordering operator is defined as follows.

\\[ \mathcal{T} \left[ \prod_{i=1}^n \hat{H}(t_i) \right] = \prod_{i=1}^n \hat{H}( t_{\sigma(i)} ) \quad
( t_{\sigma(1)} \ge \cdots \ge t_{\sigma(n)}) \\]

where $\sigma$ is a permutation.
While, we can express the dyson series simply using the time-ordering operator. Let's first discover some interesting properties.

\\[ \begin{align\*}
\mathcal{T} \left[ \hat{G}(t,t_0)^n \right]
&= \left( -\frac{i}{\hbar} \right)^n \mathcal{T} \left[ \prod_{i=1}^n \int_{t_0}^t \hat{H}(t_i) \d{t_i} \right] \nl
&= \left( -\frac{i}{\hbar} \right)^n \mathcal{T} \left[ \int_{t_0}^t \d{t_1} \cdots \int_{t_0}^t \d{t_n} \prod_{i=1}^n \hat{H}(t_i) \right] \nl
&= n! \left( -\frac{i}{\hbar} \right)^n \int_{t_0}^t \d{t_1} \int_{t_0}^{t_1} \d{t_2} \cdots \int_{t_0}^{t_{n-1}} \d{t_n} \prod_{i=1}^n \hat{H}(t_i)
\end{align\*} \\]

This is exactly the same as the $n$-th term of the Dyson series without the factor $n!$. Therefore, we can write the Dyson series as follows.

\\[ \begin{align\*}
\hat{\mathcal{U}}(t,t_0)
&= \sum_{n=0}^\infty \frac{1}{n!} \mathcal{T} \left[ \hat{G}(t,t_0)^n \right] \nl
&= \mathcal{T} \left[ \sum_{n=0}^\infty \frac{1}{n!} \hat{G}(t,t_0)^n \right] \nl
&= \mathcal{T} \exp\left( \hat{G}(t,t_0) \right)
\end{align\*} \\]

Then we finally get the general form of the time propagator.

\\[ \hat{\mathcal{U}}(t,t_0) = \mathcal{T} \exp\left( -\frac{i}{\hbar} \int_{t_0}^t \hat{H}(t\rq) \d{t\rq} \right) \\]