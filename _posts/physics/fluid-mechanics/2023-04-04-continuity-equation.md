---
layout: post
title: "Continuity equation"
subtitle: "flun"
classification: "Fluid Mechanics Unclassified"
categories: physics
tags: fluid-mechanics
image:
    path: /assets/img/physics/fluid-mechanics/Landau.jpg
---

from **「Fluid Mechanics」**: _Landau, L.D. & Lifschitz, E.M._
{:.figcaption}

> The continuity equation.

<!--more-->
* this unordered seed list will be replaced by the toc
{:toc}

## Continuity equation

In fluid dynamics, the **continuity equation** states that the rate at which mass enters a system is equal to 
the rate at which mass leaves the system plus the accumulation of mass within the system.

\\[ \frac{\partial\rho}{\partial t} + \nabla\cdot(\rho\b{u}) = 0 \\]

where $\rho$ is the density of the fluid, $\b{u}$ is the velocity of the fluid, and $t$ is time.

The continuity equation is a consequence of the conservation of mass, and we'll derive the equation
from the assumption now.

### Derivation

We consider some volume $V_0$ of space. The change per unit time in the mass of fluid in this volume
should be the same as the quantity flowing in unit time through the surface of the volume.
Therefore, we can write as follows:

\\[ \frac{\partial}{\partial t}\int_{V_0}\rho \,\d V = -\oint_{\partial V_0}\rho\b{u}\cdot\,\d\b{S} \\]

The surface integral can be transformed by the _divergence theorem_ to a volume integral, thus:

\\[ \frac{\partial}{\partial t}\int_{V_0}\rho \,\d V = -\int_{V_0}\nabla\cdot(\rho\b{u}) \d V \nl\;\nl
\\int_{V_0}\left[ \frac{\partial\rho}{\partial t}+\nabla\cdot(\rho\b{u})\right] \d V = 0 \\]

Since the equation must hold for any volume $V_0$, the integrand must vanish.

\\[ \frac{\partial\rho}{\partial t} + \nabla\cdot(\rho\b{u}) = 0 \\]

Defining the vector $\b{j}$ as $\rho\b{u}$, we can write the continuity equation as:

\\[ \frac{\partial\rho}{\partial t} + \nabla\cdot\b{j} = 0 \\]

Here $\b{j}$ is called the **mass flux density**. Its direction is that of the motion of the fluid,
while its magnitude equals the mass of fluid flowing in unit time through unit area perpendicular to the velocity.

### Interpretation

Expanding the expression for the mass flux density, we have:

\\[ \frac{\partial\rho}{\partial t} + \rho\nabla\cdot\b{u} + (\nabla\rho)\cdot\b{u} = 0 \\]

We can simplyfy the equation by the _material derivative_,

\\[ \frac{D}{Dt} = \frac{\partial}{\partial t} + \b{u}\cdot\nabla \\]

we get the following equation.

\\[ \frac{D\rho}{Dt} + \rho\b{u}\cdot\nabla\b{u} = 0 \\]

A change in the density over time should be proportional to the divergence of the velocity field.
So if the fluid is _incompressible_, the divergence of the velocity field must be zero, which is expressed as:

\\[ \nabla\cdot\b{u} = 0 \\]