---
title: Helium Atom
subtitle: Unclassified
author: jiho
date: 2023-02-19 16:00:00 +0800
categories: [Learning, Physics, Quantum Mechanics]
tags: [physics, quantum mechanics, variational method, approximation, wavefunction, ground state, helium atom, spin]
math: true
---

## Ground state of the helium atom
Let's approximate the ground state energy of the helium atom using the variational method.
The Hamiltonian of the system is; ignoring the motion of the nucleus (Born–Oppenheimer approximation):

$ \global\def\Zef{Z\rq} $

\\[ \hamiltonian = -\frac{\hbar^2}{2m_e}(\nabla_1^2+\nabla_2^2) -\frac{e^2}{4\pi\epzro}\left[ \frac{2}{r_1}+\frac{2}{r_2}-\frac{1}{\abs{\b{r}_1-\b{r}_2}} \right] \\]

Let's set the trial wavefunction as the product of the ground state wavefunction of the hydrogenic atom system,
ignoring the interaction of electrons, which are regarded as identical. Here we add a parameter $\Zef$ for the variation.

\\[ \begin{align\*}
\psi(\b{r}_1,\b{r}_2) &= \psi _{100}(\b{r_1})\psi _{100}(\b{r}_2) \nl
&= \frac{\Zef^3}{\pi a_0^3} \exp\left[ -\frac{\Zef}{a_0}(r_1+r_2) \right]
\end{align\*} \\]

Then, let's change the Hamiltonian to the following form for simple calculations.

\\[ \hamiltonian =
\left( -\frac{\hbar^2}{2m_e}\nabla_1^2-\frac{\Zef e^2}{4\pi\epzro r_1} \right) + \left( -\frac{\hbar^2}{2m_e}\nabla_2^2-\frac{\Zef e^2}{4\pi\epzro r_2} \right)
+\frac{e^2}{4\pi\epzro}\left[ \frac{\Zef-2}{r_1}+\frac{\Zef-2}{r_2}+\frac{1}{\abs{\b{r}_1-\b{r}_2}} \right] \\]

We see that the terms inside parentheses are the Hamiltonian of hydrogen-like atoms of atomic number $\Zef$, respectively.
However, here $\Zef$ doesn't have to be an integer since it's a parameter for the variational method;
it reflects the **shielding effect** (or **screening effect**) of the electrons.
Therefore, $\Zef$ is an **effective nuclear charge** $Z_\text{eff}$, and we'll calculate it later.

Recall that $\Expct{\dfrac{1}{r}}=\dfrac{\Zef}{a_0}$ is satisfied at the ground state of the hydrogen-like atom.
The expectation value of the Hamiltonian is, where $E_1$ is the ground state energy of the hydrogen:

\\[ \begin{align\*}
\expct{\hat{\hamiltonian}}
&= \Zef^2E_1 + \Zef^2E_1 + \frac{(\Zef-2)e^2}{4\pi\epzro}\left[ \Expct{\frac{1}{r_1}}+\Expct{\frac{1}{r_2}} \right] +
\frac{e^2}{4\pi\epzro}\Expct{\frac{1}{\abs{\b{r}_1-\b{r}_2}}} \nl
&= 2\Zef^2E_1-4\Zef(\Zef-2)E_1 + \frac{e^2}{4\pi\epzro}\Expct{\frac{1}{\abs{\b{r}_1-\b{r}_2}}}
\end{align\*} \\]

Let's calculate the expectation value:

\\[ \Expct{\frac{1}{\abs{\b{r}_1-\b{r}_2}}} = \left(\frac{Z^3}{\pi a_0^3}\right)^2  \underbrace{
\int _{\R^3}\int _{\R^3} \frac{1}{\abs{\b{r}_1-\b{r}_2}} \exp\left[ -\frac{2\Zef}{a_0}(r_1+r_2) \right] \d^3\b{r}_1 \d^3\b{r}_2 } _{\dps I} \\]

Let's use the _multipole expansion_ using _spherical harmonics_, where $ Y_0^0 \equiv \dfrac{1}{\sqrt{4\pi}} $.
By the orthogonality of the spherical harmonic functions, we get:

\\[ \begin{align\*}
I &= \int_0^\infty\int_0^\infty \exp\left[ -\frac{2\Zef}{a_0}(r_1+r_2) \right] \sum_{l=0}^\infty\sum_{m=-l}^l
\frac{4\pi}{2l+1}\frac{r_<^l}{r_>^{l+1}} r_1^2r_2^2 \,\d r_1\d r_2
\oint_{\Omega_1}\oint_{\Omega_2} Y_l^{m\ast}(\theta_1,\varphi_1) Y_l^m(\theta_2,\varphi_2) \d\Omega_2 \d\Omega_1 \nl
&= \int_0^\infty\int_0^\infty \exp\left[ -\frac{2\Zef}{a_0}(r_1+r_2) \right] \sum_{l=0}^\infty\sum_{m=-l}^l
\frac{4\pi}{2l+1}\frac{r_<^l}{r_>^{l+1}} r_1^2r_2^2 \,\d r_1 \d r_2 \cdot
4\pi \oint_{\Omega_1} Y_l^{m\ast}(\theta_1,\varphi_1)Y_0^0(\theta_1,\varphi_1)\d\Omega_1 \oint_{\Omega_2} Y_0^{0\ast}(\theta_2,\varphi_2)Y_l^m(\theta_2,\varphi_2)\d\Omega_2 \nl
&= \int_0^\infty\int_0^\infty \exp\left[ -\frac{2\Zef}{a_0}(r_1+r_2) \right] \sum_{l=0}^\infty\sum_{m=-l}^l \delta_{l0}\delta_{m0}
\frac{(4\pi)^2}{2l+1}\frac{r_<^l}{r_>^{l+1}} r_1^2r_2^2 \,\d r_1 \d r_2 \nl
&= (4\pi)^2 \int_0^\infty\int_0^\infty \exp\left[ -\frac{2\Zef}{a_0}(r_1+r_2) \right] \frac{r_1^2r_2^2}{r_>} \,\d r_1 \d r_2 \nl
&= \frac{5\pi^2}{8\Zef^5}a_0^5
\end{align\*} \\]

Therefore,

\\[ \begin{align\*}
\frac{e^2}{4\pi\epzro}\Expct{\frac{1}{\abs{\b{r}_1-\b{r}_2}}} &=
\frac{e^2}{4\pi\epzro} \left(\frac{Z^3}{\pi a_0^3}\right)^2 \frac{5\pi^2}{8\Zef^5}a_0^5 \nl
&= -\frac{5}{4}\Zef E_1
\end{align\*} \\]

Then we finally get the expectation of the Hamiltonian:

\\[ \begin{align\*}
\expct{\hat{\hamiltonian}}
&= \left( -2\Zef^2+\frac{27}{4}\Zef \right) E_1 \nl
&= \left( 2\Zef^2-\frac{27}{4}\Zef \right) \Ryd
\end{align\*} \\]

This value is minimized when $\Zef$ is $\dfrac{27}{16}$.

\\[ \begin{align\*}
\expct{\hat{\hamiltonian}} &\ge \frac{729}{128}E_1 \nl
&\approx -77.489 \,\eV
\end{align\*} \\]

An experimental value is $-78.975 \,\eV$, which shows that our approximation is pretty accurate. (error of $ 1.88\,\% $).

We can also calculate the ionization energy of helium.
Since the first ionization energy of helium is trivially (and also approximately) $ 4\Ryd=54.423\,\eV $,
we get the second ionization energy naturally, of which value is $23.066\,\eV$.
Although this isn't accurate enough (over $5\,\%$ of the error to experiments) to use, it still provides us the rough value.

Summarizing,
* $ Z_\text{eff} \approx 1.6875 $
* $ E_\text{gs} \approx -77.489\,\eV $
* The wavefunction of the ground state helium can be thought of as the product of the wavefunctions of $\ce{He+}$.

### Helium-like atom

A **two-electron atom** or **helium-like ion** is a quantum mechanical system consisting of
one nucleus with a charge of $Ze$ and just two electrons. ($\ce{H-}$, $\ce{He}$, $\ce{Li+}$, $\ce{Be^2+}$, ...)

The expectation of Hamiltonian can be computed in the same way,

\\[ \expct{\hat{\hamiltonian}} =
\left( -2\Zef^2+\frac{16Z-5}{4}\Zef \right)E_1 \\]

Therefore,
* $ Z_\text{eff} \approx Z-\dfrac{5}{16} $
* $ E_\text{gs} \approx 2\left(Z-\dfrac{5}{16}\right)^2 E_1 $

This is approximation is quite good, surprisingly!
Compare with experimental values in the tables here.
- [Ionization Energy](https://en.wikipedia.org/wiki/Molar_ionization_energies_of_the_elements#All_Ionization_Energies)
- [Effective Nuclear Charge](https://en.wikipedia.org/wiki/Effective_nuclear_charge#Values)

### Better approximations

⚠️**Studying**⚠️

[Link](https://chem.libretexts.org/Bookshelves/Physical_and_Theoretical_Chemistry_Textbook_Maps/Physical_Chemistry_(LibreTexts)/08%3A_Multielectron_Atoms/8.02%3A_Perturbation_Theory_and_the_Variational_Method_for_Helium)
[File](https://github.com/phylosopher07/phylosopher07/files/10780277/var-mthd.with.2.pars.pdf)

## Excited states of the helium atom

⚠️**Studying**⚠️

[LINK](https://chem.libretexts.org/Bookshelves/Physical_and_Theoretical_Chemistry_Textbook_Maps/Supplemental_Modules_(Physical_and_Theoretical_Chemistry)/Quantum_Mechanics/10%3A_Multi-electron_Atoms/8%3A_The_Helium_Atom)
[PDF](https://www.physik.fu-berlin.de/einrichtungen/ag/ag-heyne/docs/teaching/SoSe08/Amol1/AMol_Teil2.pdf)
