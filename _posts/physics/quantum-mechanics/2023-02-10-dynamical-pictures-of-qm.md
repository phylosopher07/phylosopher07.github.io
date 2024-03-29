---
layout: post
title: "Dynamical Pictures"
subtitle: "qm1.6"
classification: "Quantum Mechanics 1.6"
categories: physics
tags: quantum-mechanics
image:
    path: /assets/img/physics/quantum-mechanics/Sakurai.svg
---

from **「Modern Quantum Mechanics」**: _Sakurai, J. J._
{:.figcaption}

> Several equivalent pictures to interpret quantum mechanics.

<!--more-->
* this unordered seed list will be replaced by the toc
{:toc}

## Time-evolution operator

The **time-evolution operator** $U(t,t_0)$ is defined as the operator which acts on the ket at time $t_0$
to produce the ket at some other time $t$:
* $ \ket{\Psi(t)}=\hat{U}(t,t_0)\ket{\Psi(t_0)} $
* $ \bra{\Psi(t)}=\bra{\Psi(t_0)}\hat{U}^\dag(t,t_0) $

### Properties

1. Unitarity
  * $ \hat{U}^\dag(t,t_0)\hat{U}(t,t_0) = \mathbb{I} $
2. Identity
  * $ \hat{U}(t_0,t_0) = \mathbb{I} $
3. Closure
  * $ \hat{U}(t,t_0)=\hat{U}(t,t_1)\hat{U}(t_1,t_0) $

### Differential equation for time-evolution operator

We drop the $t_0$ index in the time evolution operator with the convention that $t_0=0$ and write it as $U(t)$.

Using the Schrödinger equation, we get the differential equation of $U$.

\\[ i\hbar\pdv{ }{t}\hat{U}(t)\ket{\Psi(0)} = \hat{H}\hat{U}(t)\ket{\Psi(0)}  \\]

\\[ \Rightarrow  i\hbar\pdv{ }{t}\hat{U}(t) = \hat{H}\hat{U}(t)  \\]

If the Hamiltonian is independent of time, the solution to the above equation is: 

\\[ \hat{U}(t) = \exp\left( -\frac{it}{\hbar}\hat{H} \right) \\]

If the Hamiltonian is dependent on time, but the Hamiltonians at different times commute,
then the time evolution operator can be written as:

\\[ \hat{U}(t) = \exp\left( -\frac{i}{\hbar}\int_0^t\hat{H}(t\rq)dt\rq  \right) \\]

If the Hamiltonian is dependent on time, but the Hamiltonians at different times do not commute,
then the time evolution operator can be written in following form 
where $\mathcal{T}$ is **time-ordering operator**, which is sometimes known as the **Dyson series**.

\\[ \hat{U}(t) = \mathcal{T}\exp\left( -\frac{i}{\hbar}\int_0^t\hat{H}(t\rq)dt\rq  \right) \\]

See the wiki for more information. ([Dyson series](/physics/dyson-series.html))


## Dynamical pictures

**Dynamical pictures** (or representations) are the multiple equivalent ways to mathematically formulate
the dynamics of a quantum system.

### Schrödinger picture

**Schrödinger picture** is a method of fixing the observable and interpreting the state vector to change over time.

* Ket state: $ \ket{\Psi_S(t)}=\hat{U}(t)\ket{\Psi_S(0)} $
* Observable: constant

### Heisenberg picture

**Heisenberg picture** is a method of fixing the state vector and interpreting that the observable changes over time.

* $ \expct{\hat{A}}_t = \brktop{\Psi(t)}{\hat{A}}{\Psi(t)} =
\brktop{\Psi(0)}{\hat{U}^\dag(t)\hat{A}\hat{U}(t)}{\Psi(0)} $
* $ \hat{A}_H(t) \coloneqq \hat{U}^\dag(t)\hat{A}\hat{U}(t) $

Let's find out then how the expectation value of an observable changes over time.

\\[ \begin{align\*}
\odv{ }{t} \hat{A}_H(t) &= \pdv{\hat{U}^\dag}{t}\hat{A}\hat{U} + \hat{U}^\dag\pdv{\hat{A}}{t}\hat{U} + \hat{U}^\dag\hat{A}\pdv{\hat{U}}{t} \nl
&= \frac{i}{\hbar}\hat{U}^\dag\hat{H}\hat{A}\hat{U} + \hat{U}^\dag\pdv{\hat{A}}{t}\hat{U} + \frac{i}{\hbar}\hat{U}^\dag\hat{A}(-\hat{H})\hat{U} \nl
&= \frac{i}{\hbar}\left(\hat{H}\hat{A}_H-\hat{A}_H\hat{H}\right) + \left(\pdv{\hat{A}}{t}\right)_H
\end{align\*} \\]

\\[\therefore\; \boxed{  \odv{ }{t}\hat{A}_H(t) =
\frac{i}{\hbar}\comm{\hat{H}}{\hat{A}_H(t)} + \left(\pdv{\hat{A}}{t}\right)_H  }\\]

In conclusion,
* Ket state: constant
* Observable: $ \hat{A}_H(t)=\hat{U}^\dag(t)\hat{A}\hat{U}(t) $

### Interaction picture

---
<center>
⚠️writing⚠️ <br>
https://en.wikipedia.org/wiki/Dynamical_pictures
</center>
---

### Comparison of pictures

|Evolution|Picture| | |
| |Schrödinger (S)|Heisenberg (H)|Interaction (I)|
|:---:|:---:|:---:|:---:|
|Ket state|$ \ket{\Psi_S(t)}=e^{-i\frac{\hat{H}_S}{\hbar}t}\ket{\Psi_S(0)} $| constant |$ \ket{\Psi_I(t)}=e^{i\frac{\hat{H}_0}{\hbar}t}\ket{\Psi_S(t)} $|
|Observable| constant |$ \hat{A}_H(t)=e^{i\frac{\hat{H}_S}{\hbar}t}\hat{A}_S e^{-i\frac{\hat{H}_S}{\hbar}t} $|$ \hat{A}_I(t)= e^{i\frac{\hat{H}_0}{\hbar}t}\hat{A}_S e^{-i\frac{\hat{H}_0}{\hbar}t} $|
{:.center-table}
