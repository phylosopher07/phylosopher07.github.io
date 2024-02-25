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

**Generalized Ehrenfest's theorem**:

\\[ \odv{ }{t}\expct{\hat{Q}} = \frac{i}{\hbar}\expct{\comm{ \hat{H} }{ \hat{Q} }} +
\Expct{\pdv{\hat{Q}}{t}}  \\]

The equation is the same as the _Heisenberg image_, but let's derive it from the _Schrödinger image_.

\\[ \begin{align\*}
\odv{ }{t}\expct{\hat{Q}} &= \odv{ }{t}\brktop{\psi}{\hat{Q}}{\psi} \nl
&= \Brktop{\pdv{\psi}{t}}{\hat{Q}}{\psi} + \Brktop{\psi}{\pdv{\hat{Q}}{t}}{\psi} + \Brktop{\psi}{\hat{Q}}{\pdv{\psi}{t}}
\end{align\*} \\]

Using the Schrödinger equation $\dps i\hbar\pdv{ }{t}\ket{\psi}=\hat{H}\ket{\psi}$,

\\[ \odv{ }{t}\expct{\hat{Q}} = -\frac{1}{i\hbar}\brkt{ \hat{H}\psi }{ \hat{Q}\psi } + \Expct{\pdv{\hat{Q}}{t}} + \frac{1}{i\hbar}\brkt{ \psi }{ \hat{Q}\hat{H}\psi } \\]

\\[ \therefore \odv{ }{t}\expct{\hat{Q}} = \frac{i}{\hbar}\expct{\comm{ \hat{H} }{ \hat{Q} }} +
\Expct{\pdv{\hat{Q}}{t}} \\]

### Examples

* $\dps m\odv{\expct{\b{r}}}{t} = \expct{\b{p}} $

* $\dps \odv{\expct{\b{p}}}{t} = -\Expct{ \nabla V(\b{r}) } $


## Time-energy uncertainty relation

If $\hat{Q}$ is not explicit for $t$, by the Ehrenfest's theorem; 

* $\dps \sigma_H\sigma_Q \ge \frac{1}{2}\abs{\expct{ \comm{\hat{H}}{\hat{Q}} }} =
\frac{\hbar}{2}\abs{ \odv{\expct{\hat{Q}}}{t} } $

Here we define $\Delta E \coloneqq \sigma_H$ and $\Delta t \coloneqq \dfrac{\sigma_Q}{\abs{ \odvi{\expct{\hat{Q}}}{t} }} $.

Then we get, time **time-energy uncertainty relation**: 
* $\dps \Delta E\Delta t \ge \frac{\hbar}{2} $

The _'uncertainty' in time_ is expressed as the average time taken, starting in state $\ket{\psi}$,
for the expectation of some arbitrary observable $\hat{Q}$ to change by its standard deviation.
This is reasonable as a definition for time uncertainty because it gives the shortest time scale
on which we will be able to notice changes by using $\hat{Q}$ in state $\ket{\psi}$.
