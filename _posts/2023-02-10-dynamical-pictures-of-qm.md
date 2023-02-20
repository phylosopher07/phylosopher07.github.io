---
title: Dynamical pictures
subtitle: Quantum Mechanics 1.7
author: jiho
date: 2023-02-10 14:00:00 +0800
categories: [Learning, Physics, Quantum Mechanics]
tags: [physics, quantum mechanics, dynamical pictures]
math: true
---

## Time-evolution operator

The **time-evolution operator** $U(t,t_0)$ is defined as the operator which acts on the ket at time $t_0$
to produce the ket at some other time $t$:
* $ \ket{\Psi(t)}=\hat{U}(t,t_0)\ket{\Psi(t_0)} $
* $ \bra{\Psi(t)}=\bra{\Psi(t_0)}\hat{U}^\dag(t,t_0) $

### Properties

1. Unitarity
  * $ \hat{U}^\dag(t,t_0)\hat{U}(t,t_0)=I $
2. Identity
  * $ \hat{U}(t_0,t_0)=I $
3. Closure
  * $ \hat{U}(t,t_0)=\hat{U}(t,t_1)\hat{U}(t_1,t_0) $

### Differential equation for time-evolution operator

We drop the $t_0$ index in the time evolution operator with the convention that $t_0=0$ and write it as $U(t)$.

Using the Schrödinger equation, we get the differential equation of $U$.

\\[ i\hbar\frac{\partial}{\partial t}\hat{U}(t)\ket{\Psi(0)} = \hat{\mathcal{H}}\hat{U}(t)\ket{\Psi(0)}  \\]

\\[ \Rightarrow  i\hbar\frac{\partial}{\partial t}\hat{U}(t) = \hat{\mathcal{H}}\hat{U}(t)  \\]

If the Hamiltonian is independent of time, the solution to the above equation is: 

\\[ \hat{U}(t) = e^{-\frac{it}{\hbar}\hat{\mathcal{H}}} \\]

If the Hamiltonian is dependent on time, but the Hamiltonians at different times commute,
then the time evolution operator can be written as:

\\[ \hat{U}(t) = \exp\left( -\frac{i}{\hbar}\int_0^t\hat{\mathcal{H}}(t\rq)dt\rq  \right) \\]

If the Hamiltonian is dependent on time, but the Hamiltonians at different times do not commute,
then the time evolution operator can be written in following form 
where $\mathcal{T}$ is **time-ordering operator**, which is sometimes known as the **Dyson series**.

\\[ \hat{U}(t) = \mathcal{T}\exp\left( -\frac{i}{\hbar}\int_0^t\hat{\mathcal{H}}(t\rq)dt\rq  \right) \\]

See the wiki for more information. ([Dyson series](https://en.wikipedia.org/wiki/Dyson_series))


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
\frac{d}{dt} \hat{A}_H(t) &= \frac{\partial\hat{U}^\dag}{\partial t}\hat{A}\hat{U} + \hat{U}^\dag\frac{\partial\hat{A}}{\partial t}\hat{U} + \hat{U}^\dag\hat{A}\frac{\partial\hat{U}}{\partial t} \nl
&= \frac{i}{\hbar}\hat{U}^\dag\hat{\mathcal{H}}\hat{A}\hat{U} + \hat{U}^\dag\frac{\partial\hat{A}}{\partial t}\hat{U} + \frac{i}{\hbar}\hat{U}^\dag\hat{A}(-\hat{\mathcal{H}})\hat{U} \nl
&= \frac{i}{\hbar}\left(\hat{\mathcal{H}}\hat{A}_H-\hat{A}_H\hat{\mathcal{H}}\right) + \left(\frac{\partial\hat{A}}{\partial t}\right)_H
\end{align\*} \\]

\\[\therefore\; \boxed{  \frac{d}{dt}\hat{A}_H(t) =
\frac{i}{\hbar}\com{\hat{\mathcal{H}}}{\hat{A}_H(t)} + \left(\frac{\partial\hat{A}}{\partial t}\right)_H  }\\]

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

|Evolution|Picture|||
||Schrödinger (S)|Heisenberg (H)|Interaction (I)|
|:---:|:---:|:---:|:---:|
|Ket state|$ \ket{\Psi_S(t)}=e^{-i\frac{\hat{\mathcal{H}}_S}{\hbar}t}\ket{\Psi_S(0)} $| constant |$ \ket{\Psi_I(t)}=e^{i\frac{\hat{\mathcal{H}}_0}{\hbar}t}\ket{\Psi_S(t)} $|
|Observable| constant |$ \hat{A}_H(t)=e^{i\frac{\hat{\mathcal{H}}_S}{\hbar}t}\hat{A}_S e^{-i\frac{\hat{\mathcal{H}}_S}{\hbar}t} $|$ \hat{A}_I(t)= e^{i\frac{\hat{\mathcal{H}}_0}{\hbar}t}\hat{A}_S e^{-i\frac{\hat{\mathcal{H}}_0}{\hbar}t} $|
{:.center-table}
