---
layout: post
title: "Euler equations"
subtitle: "flun"
classification: "Fluid Mechanics Unclassified"
categories: physics
tags: fluid-mechanics
image:
    path: /assets/img/physics/fluid-mechanics/Landau.jpg
---

from **「Fluid Mechanics」**: _Landau, L.D. & Lifschitz, E.M._
{:.figcaption}

> Equations for adiabatic and inviscid flow.

<!--more-->
* this unordered seed list will be replaced by the toc
{:toc}

## Momentum equation

The **momentum equation** is a partial differential equation that describes the motion of an ideal fluid,

\\[ \frac{D\b{u}}{Dt} = -\frac{1}{\rho}\nabla p \\]

where $\frac{D}{Dt}$ is the _material derivative_.
The momentum equation is derived from the conservation of momentum,
which states that the total momentum of a system is constant.

### Proof

Let us consider some volume $V_0$ in the fluid.
The total force acting on this volume is equal to the surface integral of the pressure.
It can be transformed to a volume integral by the _divergence theorem_:

\\[ -\oint_{\partial V_0}p\d\b{f} = -\int_{V_0} \nabla p \d V \\]

