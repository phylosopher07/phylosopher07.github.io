---
layout: post
title: "Quantum Harmonic Oscillator"
subtitle: "qm2.3"
classification: "Quantum Mechanics 2.3"
categories: physics
tags: quantum-mechanics
image:
    path: /assets/img/physics/quantum-mechanics/Sakurai.svg
---

from **「Modern Quantum Mechanics」**: _Sakurai, J. J._
{:.figcaption}

> Quantum Harmonic Oscillator

<!--more-->
* this unordered seed list will be replaced by the toc
{:toc}

## Quantum Harmonic Oscillator

**Quantum Harmonic Oscillator** is a system that has a harmonic potential.
It is one of the most important systems in quantum mechanics, and it is also a system that can be solved exactly.
Since it is applied to many situations and also used as a model for quantum field theory, it is important to deeply understand the QHO.

Let's start with the Schrödinger equation for the 1-dimensional QHO.

\\[ -\frac{\hbar^2}{2m} \odvn{2}{\psi}{x} + \frac{1}{2}m\omega^2x^2\psi = E\psi \\]

We're now going to solve this equation in two different ways.

### Analytic Solution

First, let's nondimensionalize the equation so that it is easier to solve.

\\[ \xi = \sqrt{\frac{m\omega}{\hbar}}x ,\quad \epsilon = \frac{2E}{\hbar\omega} \nt
\odvn{2}{\psi}{\xi} + (\epsilon-\xi^2)\psi = 0 \\]

The equation is not easy to solve, so let's try an approximation.
We find that $\xi \gg 1 \to \psi \propto \exp(-\xi^2/2)$, so assume that $\psi$ has a following form;

\\[ \psi = A H(\xi) \exp\left( -\frac{\xi^2}{2} \right) \\]

where $H(\xi)$ is a function to be determined and $A$ is an normalization constant. Substituting this into the Schrödinger equation, we get

\\[ \odvn{2}{H}{\xi} - 2\xi\odv{H}{\xi} + (\epsilon-1)H = 0 \\]

We'll use the power series method to solve this equation.

\\[
H(\xi) = \sum_{k=0}^\infty a_k\xi^k \;\Rightarrow\;
\sum_{k=0}^\infty \Big[ (k+2)(k+1)a_{k+2}-2ka_k+(\epsilon-1)a_k \Big]\xi^k = 0 \nt
a_{k+2} = \frac{2k+1 -\epsilon}{(k+2)(k+1)}a_k
\\]

Since the solution has to not diverge, there must be a $k$ such that $a_k=0$ and after all.
Therefore, $\epsilon=2n+1$ for non-negative integer $n$. Then we rewrite the differential equation for $H(\xi)$ as

\\[ \odvn{2}{H}{\xi} - 2\xi\odv{H}{\xi} + 2nH = 0 \\]

This is the **Hermite differential equation**. The solution is called **Hermite polynomial** $H_n(\xi)$ and are the orthogonal polynomials.
The final solution after the normalization and rescaling is,

\\[ \psi_n(x) = \frac{1}{\sqrt{2^n n!}} \left( \frac{m\omega}{\pi\hbar} \right)^{1/4} H_n\left( \sqrt{\frac{m\omega}{\hbar}}x\right ) \exp\left( -\frac{m\omega}{2\hbar}x^2 \right) \\]

The energy eigenvalue is

\\[ E_n = \hbar\omega\left( n+\frac{1}{2} \right) \\]

We can see that the energy is quantized, and the energy difference between the adjacent levels is $\hbar\omega$.
Also, the ground state energy is nonzero. This is a significant difference from the classical case.

### Ladder Operator Method(Algebraic Solution)

However, an analytic approach is not the best way to understand the QHO.
We can solve the QHO in a more elegant way using the ladder operator method.

First, we define the following operators where $\beta=\sqrt{m\omega/\hbar}$.

$ \gdef\ann{\hat{a}} \gdef\cre{\hat{a}^\dagger} $

\\[ \begin{align\*}
\ann &= \frac{\beta}{\sqrt{2}}\left( \hat{x} + i\frac{\hat{p}}{m\omega} \right) \nl
\cre &= \frac{\beta}{\sqrt{2}}\left( \hat{x} - i\frac{\hat{p}}{m\omega} \right)
\end{align\*} \\]

These operators are called **annihilation operator** and **creation operator** respectively,
and are called **ladder operators** together. We can easily check the commutation relation between them.

\\[ \begin{align\*}
\ann\cre &= \frac{\beta^2}{2}\left( \hat{x}^2 + \frac{\hat{p}^2}{m^2\omega^2} - \frac{i}{m\omega}\comm{\hat{x}}{\hat{p}} \right) \nl
&= \frac{1}{\hbar\omega} \left( \frac{\hat{p}^2}{2m} + \frac{1}{2}m\omega^2\hat{x}^2 \right) - \frac{i}{\hbar} \cdot i\hbar \nl
&= \frac{1}{\hbar\omega} \hat{H} + \frac{1}{2} \nt
\cre\ann &= \frac{1}{\hbar\omega} \hat{H} - \frac{1}{2}
\end{align\*} \\]

\\[ \therefore \comm{\ann}{\cre} = 1 \\]

If classical, Hamiltonian would just be the product of $\ann$ and $\cre$.
However, quantum mechanics works in a different way. $\ann$ and $\cre$ do not commute, and the Hamiltonian is not the product of them.
To seek for the properties of ladder operators, let's look for operators that commute with Hamiltonian.

\\[ \comm{\hat{H}}{\hat{Q}} = \lambda\hat{Q} \nt
\Rightarrow \hat{H}\hat{Q}\psi = (\lambda\hat{Q}+\hat{Q}\hat{H})\psi = (\lambda+E)\hat{Q}\psi \\]

This means that $\hat{Q}\psi$ is an state with the energy $\lambda+E$ if $\psi$ is an state with the energy $E$.
Now we see what ladder operators do.

\\[ \comm{\hat{H}}{\ann} = -\hbar\omega\ann \nl
\comm{\hat{H}}{\cre} = \hbar\omega\cre \\]

This means that $\ann$ and $\cre$ lower and raise the energy of the state by $\hbar\omega$ respectively.
Then, we can think of the ground state $\psi_0$ as the state that $\ann$ cannot lower anymore.
Ground state wavefunction can be obtained by solving simple differential equation.

\\[ \ann\psi_0 = 0 \nt
\therefore \psi_0 = \left( \frac{m\omega}{\pi\hbar} \right)^{1/4} \exp\left( -\frac{m\omega}{2\hbar}x^2 \right) \\]

Ground state energy is also obtained.

\\[ \hat{H}\psi_0 = \hbar\omega\left(\cre\ann+\frac{1}{2}\right)\psi_0 = \frac{1}{2}\hbar\omega\psi_0 \nt
\therefore E_0 = \frac{1}{2}\hbar\omega \\]

Then, $n$-th excited state can be obtained by applying $\cre$ to the ground state $n$ times. By using Dirac notation,

\\[
\ann\cre\ket{n} = \left( \frac{1}{\hbar\omega}\hat{H}-\frac{1}{2} \right)\ket{n} = n\ket{n} \nl
\cre\ann\ket{n} = \left( \frac{1}{\hbar\omega}\hat{H}+\frac{1}{2} \right)\ket{n} = (n+1)\ket{n}
\\]

Let's find the normalizing constants by using the property above.

\\[
\brktop{n}{\cre\ann}{n} = n\brkt{n}{n} = \abs{c_n}^2\brkt{n-1}{n-1} \nl
\brktop{n}{\ann\cre}{n} = (n+1)\brkt{n}{n} = \abs{d_n}^2\brkt{n+1}{n+1} \nt
\ann\ket{n} = \sqrt{n}\ket{n-1} \nl
\cre\ket{n} = \sqrt{n+1}\ket{n+1}
\\]

Finally, we can express the $n$-th excited state in terms of the ground state and creation operator.

\\[ \ket{n} = \frac{1}{\sqrt{n!}}(\cre)^n\ket{0} \\]

## Expectation Values

\1. $ \Expct{x} = 0 $
<details markdown="1"> <summary> Proof </summary>

\\[ \begin{align\*}
\Expct{x} &= \brktop{n}{\hat{x}}{n} \nl
&= \frac{1}{\sqrt{2}\beta}\brktop{n}{\ann+\cre}{n} = 0
\end{align\*} \\]

</details> <br>

\2. $ \Expct{p} = 0 $
<details markdown="1"> <summary> Proof </summary>

\\[ \begin{align\*}
\Expct{p} &= \brktop{n}{\hat{p}}{n} \nl
&= \frac{1}{\sqrt{2}\beta} \frac{m\omega}{i} \brktop{n}{\ann-\cre}{n} = 0
\end{align\*} \\]

</details> <br>

\3. $\dps \Expct{x^2} = \frac{\hbar}{m\omega}\left(n+\frac{1}{2}\right) $
<details markdown="1"> <summary> Proof </summary>

\\[ \begin{align\*}
\Expct{x^2} &= \frac{1}{2\beta^2} \brkt{(\cre+\ann)n}{(\ann+\cre)n} \nl
&= \frac{1}{2\beta^2} \left( \sqrt{n}^2 + \sqrt{n+1}^2 \right) \brkt{n}{n} \nl
&= \frac{\hbar}{m\omega} \left( n+\frac{1}{2} \right)
\end{align\*} \\]

</details> <br>

\4. $\dps \Expct{p^2} = m\omega\hbar\left(n+\frac{1}{2}\right) $
<details markdown="1"> <summary> Proof </summary>

\\[ \begin{align\*}
\Expct{p^2} &= -\frac{m^2\omega^2}{2\beta^2} \brkt{(\cre-\ann)n}{(\ann-\cre)n} \nl
&= -\frac{m^2\omega^2}{2\beta^2} \left( -\sqrt{n}^2 - \sqrt{n+1}^2 \right) \brkt{n}{n} \nl
&= m\omega\hbar \left( n+\frac{1}{2} \right)
\end{align\*} \\]

</details> <br>

\5. $\dps \Expct{T} = \frac{1}{2} \hbar\omega\left(n+\frac{1}{2}\right) $
<details markdown="1"> <summary> Proof </summary>

\\[ \Expct{T} = \frac{\Expct{p^2}}{2m} \\]

</details> <br>

\6. $\dps \Expct{V} = \frac{1}{2} \hbar\omega\left(n+\frac{1}{2}\right) $
<details markdown="1"> <summary> Proof </summary>

\\[ \Expct{V} = \frac{1}{2}m\omega^2\Expct{x^2} \\]

</details> <br>

We can also check that classical virial theorem is also valid in quantum mechanics.

\\[ \Expct{T} = \Expct{V} = \frac{1}{2}\Expct{E} \\]

## Uncertainty Principle

\\[ \sigma_x = \sqrt{ \Expct{x^2} - \Expct{x}^2 } = \sqrt{ \frac{\hbar}{m\omega}\left(n+\frac{1}{2}\right) } \nl
\sigma_p = \sqrt{ \Expct{p^2} - \Expct{p}^2 } = \sqrt{ m\omega\hbar\left(n+\frac{1}{2}\right) } \\]

\\[ \sigma_x\sigma_p = \hbar\left(n+\frac{1}{2}\right) \ge \frac{\hbar}{2} \\]

We also checked that the uncertainty principle holds well, and the equality holds when the system is in the ground state.

## 3D Harmonic Oscillator

Since harmonic potential is separable, the solution of the Schrödinger equation is the product of three 1-dimensional harmonic oscillator solutions.
Also, energy is additive, so the energy of the system is the sum of three 1-dimensional harmonic oscillator energies.

\\[ E = \hbar\omega\left( n_x + n_y + n_z + \frac{3}{2} \right) \\]