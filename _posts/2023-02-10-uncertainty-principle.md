---
title: Uncertainty Principle
subtitle: Quantum Mechanics 1.8
author: jiho
date: 2023-02-10 16:00:00 +0800
categories: [Learning, Physics, Quantum Mechanics]
tags: [physics, quantum mechanics, uncertainty principle, heisenberg limit]
math: true
---

## Standard deviation of a measurement

For an arbitrary _Hermitian operator_ $\hat{L}$ we can associate a _standard deviation_:

\\[ \begin{align\*}
\sigma_L^2 &=\expct{\hat{L}^2}-\expct{\hat{L}}^2 \nl
&= \expct{\hat{L}^2}-2\expct{\hat{L}}\expct{\hat{L}}+\expct{\hat{L}}^2 \nl
&= \Brktop{\psi}{\hat{L}^2-2\hat{L}\expct{\hat{L}}+\expct{\hat{L}}^2}{\psi} \nl
&= \Brktop{\psi}{(\hat{L}-\expct{\hat{L}})^2}{\psi} \nl
&= \Brkt{(\hat{L}-\expct{\hat{L}})\psi}{(\hat{L}-\expct{\hat{L}})\psi}
\end{align\*} \\]

Using $\hat{\delta}_L=\hat{L}-\expct{\hat{L}}$, we can write it simply.

\\[ \sigma_L^2=\Brkt{\hat{\delta}_L\psi}{\hat{\delta}_L\psi} \\]


## Robertson–Schrödinger uncertainty relations

The product of the two deviations of _Hermitian operators_ $\hat{A}$ and $\hat{B}$ can thus be expressed as

\\[ \sigma_A^2\sigma_B^2 = \Brkt{\hat{\delta}_A\psi}{\hat{\delta}_A\psi}\Brkt{\hat{\delta}_B\psi}{\hat{\delta}_B\psi} \\]

By the _Cauchy–Schwarz inequality_,

\\[ \begin{align\*}
\sigma_A^2\sigma_B^2 &\ge \abs{\Brkt{\hat{\delta}_A\psi}{\hat{\delta}_B\psi}}^2 \nl
&= \abs{\expct{ \hat{\delta}_A\hat{\delta}_B }}^2 \nl
&= \Re\left( \expct{\hat{\delta}_A\hat{\delta}_B} \right)^2 + \Im\left( \expct{\hat{\delta}_A\hat{\delta}_B} \right)^2 \nl
&= \abs{\frac{1}{2}\left[ \expct{\hat{\delta}_A\hat{\delta}_B}+\expct{\hat{\delta}_B\hat{\delta}_A} \right]}^2 + \abs{\frac{1}{2i}\left[ \expct{\hat{\delta}_A\hat{\delta}_B}-\expct{\hat{\delta}_B\hat{\delta}_A} \right]}^2
\end{align\*} \\]

We find that

\\[ \begin{align\*}
\expct{\hat{\delta}_A\hat{\delta}_B} &= \Expct{ (\hat{A}-\expct{\hat{A}})(\hat{B}-\expct{\hat{B}}) } \nl
&= \Expct{ \hat{A}\hat{B}-\hat{A}\expct{\hat{B}}-\hat{B}\expct{\hat{A}}+\expct{\hat{A}}\expct{\hat{B}} } \nl
&= \expct{\hat{A}\hat{B}}-\expct{\hat{A}}\expct{\hat{B}}
\end{align\*} \\]

We now substitute this back into the equation above and get

\\[ \begin{align\*}
\sigma_A^2\sigma_B^2 &\ge \abs{\frac{1}{2}\left[ \expct{\hat{A}\hat{B}}+\expct{\hat{B}\hat{A}}-2\expct{\hat{A}}\expct{\hat{B}} \right]}^2 + \abs{\frac{1}{2}\left[ \expct{\hat{A}\hat{B}}-\expct{\hat{B}\hat{A}} \right]}^2 \nl
&= \abs{\frac{1}{2}\left[ \expct{\acom{\hat{A}}{\hat{B}}}-2\expct{\hat{A}}\expct{\hat{B}} \right]}^2 + \abs{\frac{1}{2}\left[ \expct{\com{\hat{A}}{\hat{B}}} \right]}^2
\end{align\*} \\]

Then we finally get the **Schrödinger uncertainty relation**: 
\\[\boxed{  \sigma_A\sigma_B \ge \frac{1}{2}\sqrt{ \abs{\expct{\acom{\hat{A}}{\hat{B}}}-2\expct{\hat{A}}\expct{\hat{B}}}^2 +
\abs{\expct{\com{\hat{A}}{\hat{B}}}}^2 }  }\\]


There is also the **Robertson uncertainty relation** that has a slightly weaker condition, a more familiar form.
\\[\boxed{  \sigma_A\sigma_B \ge \frac{1}{2}\abs{\expct{\com{\hat{A}}{\hat{B}}}}  }\\]

### Example

Let's find uncertainty about the measurement of position and momentum.

Since $\com{\hat{x}}{\hat{p}}=i\hbar$,
* $ \sigma_x\sigma_p \ge \dfrac{\hbar}{2} $

## Heisenberg limit

In quantum metrology, and especially interferometry, the **Heisenberg limit** is the optimal rate
at which the accuracy of a measurement can scale with the energy used in the measurement.
Typically, this is the measurement of a phase (applied to one arm of a beam-splitter)
and the energy is given by the number of photons used in an interferometer.

## Simultaneously measurable quantities

By the (Robertson) uncertainty relation, there exists a Heisenberg limit of two physical quantities
if the two respective operators are not commutating. However, if the two operators commute, then there isn't
a Heisenberg limit, which means the two quantities are **simultaneously measurable**.
