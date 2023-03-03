---
layout: post
title: "Ehrenfest's Theorem"
subtitle: "qm1.9"
classification: "Quantum Mechanics 1.9"
categories: physics
tags: quantum-mechanics
image:
    path: /assets/img/physics/quantum-mechanics/Sakurai.svg
---

from **「Modern Quantum Mechanics」**: _Sakurai, J. J._
{:.figcaption}

> About the Ehrenfest's Theorem.

<!--more-->
* this unordered seed list will be replaced by the toc
{:toc}

## Ehrenfest's theorem

**`Generalized Ehrenfest's theorem`**:

\\[\boxed{  \frac{d}{dt}\expct{\hat{Q}} = \frac{i}{\hbar}\expct{\com{ \hat{\mathcal{H}} }{ \hat{Q} }} +
\Expct{\frac{\partial \hat{Q}}{\partial t}}  }\\]

The equation is the same as the _Heisenberg image_, but let's derive it from the _Schrödinger image_.

\\[ \begin{align\*}
\frac{d}{dt}\expct{\hat{Q}} &= \frac{d}{dt}\brktop{\psi}{\hat{Q}}{\psi} \nl
&= \Brktop{\frac{\partial\psi}{\partial t}}{\hat{Q}}{\psi} + \Brktop{\psi}{\frac{\partial \hat{Q}}{\partial t}}{\psi} + \Brktop{\psi}{\hat{Q}}{\frac{\partial\psi}{\partial t}}
\end{align\*} \\]

Using the Schrödinger equation $i\hbar\dfrac{\partial}{\partial t}\ket{\psi}=\hat{\mathcal{H}}\ket{\psi}$,

\\[ \frac{d}{dt}\expct{\hat{Q}} = -\frac{1}{i\hbar}\brkt{ \hat{\mathcal{H}}\psi }{ \hat{Q}\psi } + \Expct{\frac{\partial \hat{Q}}{\partial t}} + \frac{1}{i\hbar}\brkt{ \psi }{ \hat{Q}\hat{\mathcal{H}}\psi } \\]

\\[ \therefore \frac{d}{dt}\expct{\hat{Q}} = \frac{i}{\hbar}\expct{\com{ \hat{\mathcal{H}} }{ \hat{Q} }} +
\Expct{\frac{\partial \hat{Q}}{\partial t}} \\]

### Examples

* $ m\dfrac{d\expct{ \b{r} }}{dt} = \expct{\b{p}} $

* $ \dfrac{d\expct{ \b{p} }}{dt} = -\Expct{ \nabla V(\b{r}) } $


## Time-energy uncertainty relation

If $\hat{Q}$ is not explicit for $t$, by the Ehrenfest's theorem; 

* $ \sigma_\mathcal{H}\sigma_Q \ge \dfrac{1}{2}\abs{\expct{ \com{\hat{\mathcal{H}}}{\hat{Q}} }} =
\dfrac{\hbar}{2}\abs{ \dfrac{d\expct{\hat{Q}}}{dt} } $

Here we define $\Delta E \coloneqq \sigma_\mathcal{H}$ and $\Delta t \coloneqq \dfrac{\sigma_Q}{\abs{ d\expct{\hat{Q}} / dt }} $.

Then we get, time **time-energy uncertainty relation**: 
* $ \Delta E\Delta t \ge \dfrac{\hbar}{2} $

The _'uncertainty' in time_ is expressed as the average time taken, starting in state $\ket{\psi}$,
for the expectation of some arbitrary observable $\hat{Q}$ to change by its standard deviation.
This is reasonable as a definition for time uncertainty because it gives the shortest time scale
on which we will be able to notice changes by using $\hat{Q}$ in state $\ket{\psi}$.
