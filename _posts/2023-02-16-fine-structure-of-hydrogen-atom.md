---
title: Fine Structure of Hydrogen Atom
subtitle: Unclassified
author: jiho
date: 2023-02-16 10:00:00 +0800
categories: [Learning, Physics, Quantum Mechanics]
tags: [physics, quantum mechanics, perturbation theory, spin-orbit interaction, darwin term, hydrogen atom]
math: true
---

## Introduction

The **fine structure** describes the splitting of the spectral lines of atoms due to
_electron spin_ and _relativistic corrections_ to the non-relativistic Schrödinger equation, by usin _time-independent perturbation theory_.

## Kinetic energy relativistic correction

The gross structure assumes the kinetic energy term of the Hamiltonian takes the same form as in classical mechanics:

\\[ \hamiltonian_0 = \frac{p^2}{2m_e}+V \\]

However, when considering _special relativity_, we must use a relativistic form of kinetic energy, which is way more accurate.

\\[ \begin{align\*}
T &= \sqrt{p^2c^2+m_e^2c^4}-mc^2 \nl
&= m_ec^2 \left[ \sqrt{1+\frac{p^2}{m_e^2c^2}}-1 \right] \nl
&= \frac{p^2}{2m_e} - \frac{p^4}{2m_e^3c^2} + \cdots
\end{align\*} \\]

Although there are an infinite number of terms in this series, the later terms are much smaller than earlier terms,
so we can ignore all but the first two. Since the first term above is already part of the classical Hamiltonian,
the first-order correction to the Hamiltonian is:

\\[ \hamiltonian\rq_\text{KE} = - \frac{p^4}{2m_e^3c^2} \\]

Using this as a perturbation, we can calculate the first-order energy corrections due to relativistic effects.
Let's think of hydrogen-like atoms of atomic number $Z$.

\\[ \begin{align\*}
E_\text{KE}^{(1)} &= \brktop{\psi^{(0)}}{ \hat{\hamiltonian}\rq_\text{KE} }{\psi^{(0)}} \nl
&= -\frac{1}{8m_e^3c^2} \brktop{\psi^{(0)}}{ \hat{p}^4 }{\psi^{(0)}} \nl
&= -\frac{1}{8m_e^3c^2} \Brktop{\psi^{(0)}}{ \left[ 2m(E_n-\hat{V}) \right]^2 }{\psi^{(0)}} \nl
&= -\frac{1}{2m_ec^2} \left[ E_n^2 -2E_n\expct{V} + \expct{V^2} \right] \nl
&= -\frac{1}{2m_ec^2} \left[ E_n^2 +2E_n\frac{Ze^2}{4\pi\epzro}\Expct{\frac{1}{r}} + \left( \frac{Ze^2}{4\pi\epzro} \right)^2 \Expct{\frac{1}{r^2}} \right] \nl
\end{align\*} \\]

For the hydrogenic atoms, as we showed [here](/posts/kramers-relation-and-expectation-value/),

\\[ \Expct{\frac{1}{r}} = \frac{Z}{n^2a_0},\; \Expct{\frac{1}{r^2}} = \frac{Z^2}{ (l+\frac{1}{2})n^3a_0^2 } \\]

where $a_0$ is the Bohr radius, $n$ is the principal quantum number, $l$ is the azimuthal quantum number.
Remember that the unperturbed energy of the hydrogenic atoms is:

\\[ E_n = -\frac{e^2}{8\pi\epzroa_0} \frac{Z^2}{n^2} \\]

Therefore, the first-order relativistic correction for the hydrogenic atoms is:

\\[ \therefore E^{(1)}_\text{KE} = -\frac{E_n^2}{2m_ec^2} \left( \frac{4n}{l+\frac{1}{2}}-3 \right) \\]

## Spin-orbit interaction

⚠️[Studying](https://webhome.phy.duke.edu/~rgb/Class/phy319/phy319/node134.html)⚠️

The **spin-orbit interaction** (i.e. **spin-orbit coupling**) can be understood by shifting from the reference where the electron orbits the nucleus
into one where the electron is stationary and the nucleus instead orbits it.
In this case the orbiting nucleus functions as an effective current loop, which in turn will generate a magnetic field.
However, the electron itself has a magnetic moment due to its intrinsic angular momentum; i.e. _spin_.
The two magnetic vectors couple together so that there is a certain energy cost depending on their relative orientation.

Electrons are bound within the electric field of the atomic nucleus.
In relativistic electromagnetism, when the electric field of the nucleus is $\b{E}$,
an electron with a velocity of $\b{v}$ observes the following magnetic field.

\\[ \b{B} = -\gamma\bs{\beta}\cross\b{E} \\]

Considering only the first-term for $\bs{\beta}$,

\\[ \begin{align\*}
\b{B} &\approx -\bs{\beta}\cross\b{E} \nl
&= -\frac{\b{p}}{m_ec} \cross \left( -\frac{d\Phi}{dr}\hat{\b{r}} \right) \nl
&= \frac{1}{m_ec}\left( \frac{1}{r} \frac{d\Phi}{dr} \right) \b{L} \nl
&= \frac{1}{m_ec}\left( -\frac{Ze}{4\pi\epzro r^3} \right) \b{L}
\end{align\*} \\]

Then we can calculate the perturbed Hamiltonian (implying the _Larmor precession_), as below,

\\[ \begin{align\*}
\hamiltonian_\text{Larmor}\rq
&= -\bs{\mu}_\text{S} \cdot \b{B} \nl
&= \left( -\frac{g _\text{s} e}{2m_e} \b{S} \right) \cdot \left( -\frac{1}{m_ec} \frac{Ze}{4\pi\epzro r^3} \b{L} \right) \nl
&= \frac{Ze^2}{4\pi\epzro} \frac{g _\text{s}}{2m_e^2c^2} \frac{ \b{L}\cdot\b{S} }{r^2}
\end{align\*} \\]

where $g_\text{s}$ is the _spin g-factor_.
We're not done yet. We should also consider the _Thomas precession_ which derives from special relativity.

\\[ \begin{align\*}
\hamiltonian_\text{Thomas}\rq
&= \omega_\text{T} \cdot \b{S} \nl
& \quad \vdots \nl
&= -\frac{Ze^2}{4\pi\epzro} \frac{1}{2m_e^2c^2} \frac{ \b{L}\cdot\b{S} }{r^3}
\end{align\*} \\]

The entire perturbation is the sum of two Hamiltonians. Let's assume that the spin g-factor $g_\text{s}$ is $2$.

\\[ \begin{align\*}
\hamiltonian_\text{SO}\rq &= \hamiltonian_\text{Larmor}\rq + \hamiltonian_\text{Thomas}\rq \nl
&= \frac{Ze^2}{4\pi\epzro} \frac{g _\text{s}-1}{2m_e^2c^2} \frac{ \b{L}\cdot\b{S} }{r^3} \nl
&= \frac{Ze^2}{8\pi\epzro} \frac{1}{m_e^2c^2} \frac{ \b{L}\cdot\b{S} }{r^3}
\end{align\*} \\]

The perturbed Hamiltonian $\hamiltonian_\text{SO}\rq$ does not commute with orbital angular momentum operator $\b{L}$
and spin angular momentum operator $\b{S}$, while it commutes with $L^2$ and $S^2$.
Also, it doesn't commute with total angular momentum operator $\b{J}=\b{L}+\b{S}$ but commutes with $J^2$.

Therefore, a good set of quantum numbers to describe the system is $\Set{l,s,j}$. Let's rewrite the Hamiltonian.

\\[ \hamiltonian_\text{SO}\rq = 
\frac{Ze^2}{8\pi\epzro} \frac{1}{m_e^2c^2r^3} \frac{1}{2}\left( J^2-L^2-S^2 \right) \\]

We can calculate the first-order energy corrections due to spin-orbit interaction.

\\[ \begin{align\*}
E_\text{SO}^{(1)} &= \brktop{\psi^{(0)}}{ \hamiltonian_\text{SO}\rq }{\psi^{(0)}} \nl
&= \frac{Ze^2}{8\pi\epzro} \frac{1}{m_e^2c^2} \Expct{\frac{1}{r^3}} \frac{\hbar^2}{2} \Big[ j(j+1)-l(l+1)-s(s+1) \Big]
\end{align\*} \\]

For the hydrogenic atoms [(also here)](/posts/kramers-relation-and-expectation-value/),

\\[ \Expct{\frac{1}{r^3}} = \frac{Z^3}{n^3a_0^3} \frac{1}{l(l+\frac{1}{2})(l+1)} \\]

Since the spin of an electron is $\frac{1}{2}$, the first order spin-orbit correction for the hydrogenic atoms is:

\\[ \therefore E_\text{SO}^{(1)} = \frac{E_n^2}{m_ec^2} \frac{ n\left[ j(j+1)-l(l+1)-\frac{3}{4} \right] }{ l(l+\frac{1}{2})(l+1) } \\]

where $j$ is the total angular momentum quantum number.

## Darwin term

**Darwin correction** is impossible to interpret classically and intuitively.
It should be understood as the $s$ orbital wavefunction overlapping with the nucleus.
Therefore, every wavefunction but the $s$ orbital has the contribution of the term zero.

There is one last term in the non-relativistic expansion of the Dirac equation, which is called the _Darwin term_, and is given by:

\\[ \hamiltonian_\text{Darwin}\rq = \frac{\hbar^2}{8m_e^2c^2} \frac{Ze^2}{4\pi\epzro} 4\pi\delta^3(\b{r}) \\]

We can calculate the first-order energy corrections due to the Darwin correction.

\\[ \begin{align\*}
E_\text{Darwin}^{(1)} &= \brktop{\psi^{(0)}}{ \hamiltonian_\text{Darwin}\rq }{\psi^{(0)}}
&= \frac{\hbar^2\pi}{2m_e^2c^2} \frac{Ze^2}{4\pi\epzro} \abs{\psi(\b{0})}^2
\end{align\*} \\]

Since,

\\[ \psi(\b{0}) = \begin{cases}
\dfrac{1}{\sqrt{\pi}} \left(\dfrac{Z}{na_0}\right)^\frac{3}{2} &(l=0) \nl
0 &(l>0)
\end{cases} \\]

Therefore, the Darwin correction for the hydrogenic atoms is:

\\[ \therefore E_\text{Darwin}^{(1)} = \frac{E_n^2}{m_ec^2} 2n\delta_{l0} \\]

## Total effect

The full Hamiltonian is given by:

\\[ \hamiltonian = \hamiltonian_0 + \hamiltonian_\text{KE} + \hamiltonian_\text{SO} + \hamiltonian_\text{Darwin} \\]

The total effect, obtained by summing the three perturbations up, is given by the following expression:

\\[ \begin{align\*}
\Delta E_\text{fs}
&= -\frac{E_n^2}{2m_ec^2} \left( \frac{4n}{l+\frac{1}{2}}-3 \right) + \frac{E_n^2}{m_ec^2} \frac{ n\left[ j(j+1)-l(l+1)-\frac{3}{4} \right] }{ l(l+\frac{1}{2})(l+1) } + \frac{E_n^2}{m_ec^2} 2n\delta_{l0} \nl
&= \frac{E_n^2}{2m_ec^2} \left[ 3+4n\left( \delta_{l0}-\frac{1}{j+\frac{1}{2}} \right)\right]
\end{align\*} \\]

Expression with the _fine structure constant_ $ \alpha = \dfrac{e^2}{4\pi\epzro\hbar c} $ is:

\\[ \Delta E_\text{fs} = E_n \left(\frac{Z\alpha}{2n}\right)^2 \left[ 4n\left( \frac{1}{j+\frac{1}{2}}-\delta_{l0} \right)-3 \right] \\]

The formula without the Darwin term is also popular, too.

\\[ \Delta E_\text{fs} = E_n \left(\frac{Z\alpha}{2n}\right)^2 \left( \frac{4n}{j+\frac{1}{2}}-3 \right) \\]

Therefore, we get the final energy level considering the perturbations:

\\[ E_\text{fs} = E_n\left[ 1+ \left(\frac{Z\alpha}{2n}\right)^2 \left( \frac{4n}{j+\frac{1}{2}}-3 \right)\right]  \\]

This formula is identical to the exact energy level formula derived through the Dirac equation up to $\alpha^2$.
