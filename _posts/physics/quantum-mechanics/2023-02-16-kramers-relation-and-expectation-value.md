---
layout: post
title: "Kramers' Relation and Expectation Values of Hydrogen Atom"
subtitle: "qmun"
classification: "Quantum Mechanics Unclassified"
categories: physics
tags: quantum-mechanics
image:
    path: /assets/img/physics/quantum-mechanics/Sakurai.svg
---

from **「Modern Quantum Mechanics」**: _Sakurai, J. J._
{:.figcaption}

> Analysis for hydrogen atom model.

<!--more-->
* this unordered seed list will be replaced by the toc
{:toc}

## Kramers' relation

**Kramers’ relation**, named after the Dutch physicist _Hans Kramers_,
is a relationship between expectation values of _nearby_ powers of $r$ for the hydrogen-like atoms:

\\[ \frac{s+1}{n^2}\expct{r^s} -(2s+1)\left(\frac{a_0}{Z}\right)\expct{r^{s-1}} + \frac{s}{4}\left[ (2l+1)^2-s^2 \right]\left(\frac{a_0}{Z}\right)^2\expct{r^{s-2}} = 0 \\]

The relation is very important when computing, specifically, perturbative corrections to the hydrogen spectrum,
as those computations require expectation values of the radial Hamiltonian and potentially perturbative corrections
that have higher negative powers of $r$. Having this relation handy makes a lot of those calculations go more quickly.

### Proof

Let's remind how we solved the Schrödinger equation for hydrogen-like atoms; the radial differential equation is typically written as:

\\[ -\frac{\hbar^2}{2\mu}\pdvn{2}{u}{r} + \left[ \frac{\hbar^2l(l+1)}{2\mu r^2}-\frac{Ze^2}{4\pi\vpmt r} \right]u = Eu \\]

where $u=rR(r)$. Since

\\[ a_0=\frac{4\pi\vpmt\hbar^2}{\mu e^2} ,\; E=-\frac{\hbar^2}{2\mu}\frac{Z^2}{n^2a_0^2} \\]

we can simplify the equation:

\\[ u\rq\rq=\left[ \frac{l(l+1)}{r^2}-\frac{2Z}{a_0r}+\frac{Z^2}{n^2a_0^2} \right]u       \label{1}\tag{1}\\]

If we multiply both sides by $r^s$, then we’ll get exactly the powers of $r$ that we need for Kramer’s relation:

\\[ r^s u\rq\rq=\left[ l(l+1)r^{s-2}-\frac{2Z}{a_0}r^{s-1}+\frac{Z^2}{n^2a_0^2}r^s \right]u \\]

Now what we need to do is multiply both sides by $u^\ast=u$ and integrate.
We'll get the expected value on RHS since variables are separated, and each is normalized.

\\[ \int_0^\infty ur^su\rq\rq \d r = l(l+1)\expct{r^{s-2}}-\frac{2Z}{a_0}\expct{r^{s-1}}+\frac{Z^2}{n^2a_0^2}\expct{r^s}     \label{2}\tag{2}\\]

Let's integrate $\ref{2}$ in parts.

\\[ \begin{align\*}
\int_0^\infty ur^su\rq\rq \d r
&= \bigg[ ur^s u\rq \bigg]_0^\infty -\int_0^\infty \left( u\rq r^s+sur^{s-1} \right)u\rq \d r \nl
&= \underbrace{ -\int_0^\infty u\rq r^s u\rq \d r } _{\dps I_1} + \underbrace{ -s\int_0^\infty ur^{s-1}u\rq \d r } _{\dps I_2}
\end{align\*} \\]

Let's calculate $I_1$ integrating by parts.

\\[ \begin{align\*}
I_1 &= -\left[ \frac{r^{s+1}}{s+1} u\rq^2 \right]_0^\infty + \frac{2}{s+1}\int_0^\infty r^{s+1}u\rq u\rq\rq \d r \nl
&= \frac{2}{s+1}\int_0^\infty r^{s+1}u\rq u\rq\rq \d r
\end{align\*} \\]

Here, we substitute $\ref{1}$ to $u\rq\rq$.

\\[ I_1 = \frac{2}{s+1}\int_0^\infty u\rq\left[ l(l+1)r^{s-1}-\frac{2Z}{a_0}r^s-\frac{Z^2}{n^2a_0^2}r^{s+1} \right]u \d r \\]

Meanwhile,

\\[ \begin{align\*}
\int_0^\infty r^s uu\rq \d r &= \bigg[r^su^2\bigg]_0^\infty -\int_0^\infty\left( sr^{s-1}u^2 + r^s uu\rq \right)\d r \nl
&= -s\expct{r^{s-1}} -\int_0^\infty r^s uu\rq \d r
\end{align\*} \\]

\\[ \therefore \int_0^\infty r^suu\rq \d r = -\frac{s}{2}\expct{r^{s-1}}  \label{3}\tag{3} \\]

According to $\ref{3}$, we get $I_1$:

\\[ I_1 = -\frac{l(l+1)(s-1)}{s+1}\expct{r^{s-2}} + \frac{2Zs}{(s+1)a_0}\expct{r^{s-1}} - \frac{Z^2}{n^2a_0^2}\expct{r^s} \\]

We can also compute $I_2$ using $\ref{3}$:

\\[ I_2 = \frac{s(s-1)}{2}\expct{r^{s-2}} \\]

Substituting $I_1$ and $I_2$ to $\ref{2}$, we finally get the Kramers' relation.

\\[ \therefore \frac{s+1}{n^2}\expct{r^s} -(2s+1)\left(\frac{a_0}{Z}\right)\expct{r^{s-1}} + \frac{s}{4}\left[ (2l+1)^2-s^2 \right]\left(\frac{a_0}{Z}\right)^2\expct{r^{s-2}} = 0 \\]

## Expectation values

By using **Hellmann–Feynman theorem** and **Kramers' relation**, we can induce various expectation values of hydrogen-like atoms.

\1. $ \Expct{\dfrac{1}{r}} = \dfrac{Z}{n^2a_0} $
<details markdown="1"> <summary> Proof </summary>

Let's use the fundamental charge $e$ as a parameter for the Hellman-Feynman theorem.

\\[ \hat{H}(e) = -\frac{\hbar^2}{2\mu}\laplacian - \frac{Ze^2}{4\pi\vpmt r} \\]
  
Then,
  
\\[ \pdv{\hat{H}}{e} = -\frac{Ze}{2\pi\vpmt r} \\]
  
The energy of the electron dependent on $e$ is:
  
\\[ E_n(e) = -\frac{\mu}{2\hbar^2}\left( \frac{Ze^2}{4\pi\vpmt} \right)^2 \\]
  
Then,
  
\\[ \pdv{E_n}{e} = -\frac{1}{2\pi\vpmt}\frac{Z^2}{n^2a_0} \\]
  
By the Hellmann-Feynman theorem, we get:
  
\\[ \begin{align\*}
\pdv{E_n}{e} 
&= \Expct{\pdv{\hat{H}}{e}} \nl
&= -\frac{Ze}{2\pi\vpmt}\Expct{\frac{1}{r}}
\end{align\*} \\]

Therefore,

\\[ \therefore \Expct{\frac{1}{r}} = \frac{Z}{n^2a_0} \\]

It can be also derived from substituting $s=0$ to the Kramers' relation.

</details> <br>


\2. $ \Expct{\dfrac{1}{r^2}} = \dfrac{2Z^2}{(2l+1)n^3a_0^2} $
<details markdown="1"> <summary> Proof </summary>

Let's use the angular momentum quantum number $l$ as a parameter for the Hellman-Feynman theorem.

\\[ \hat{H}(l) = \frac{\hbar^2}{2\mu r}\pdvn{2}{ }{r}r + \frac{\hbar^2l(l+1)}{2\mu r^2} - \frac{Ze^2}{4\pi\vpmt r} \\]

Then,

\\[ \pdv{\hat{H}}{l} = \frac{\hbar^2(2l+1)}{2\mu r^2} \\]

We showed that the principle quantum number $n$ and the angular momentum quantum number $l$ 
has the following relationship finding the eigenfunction of hydrogen-like atoms:

\\[ n=l+N+1 \;(N\in\N_0) \\]

The energy of the electron dependent on $l$ is:

\\[ E_n(l) = -\frac{\hbar^2}{2\mu} \frac{Z^2}{(l+N+1)^2a_0^2} \\]

Then,

\\[ \pdv{E_n}{l} = \frac{\hbar^2}{\mu} \frac{Z^2}{(l+N+1)^3a_0^2} \\]

By the Hellmann-Feynman theorem, we get:

\\[ \begin{align\*}
\pdv{E_n}{l}
&= \Expct{\pdv{\hat{H}}{l}} \nl
&= \frac{\hbar^2(2l+1)}{2\mu} \Expct{\frac{1}{r^2}}
\end{align\*} \\]

Therefore,

\\[ \therefore \Expct{\frac{1}{r^2}} = \frac{2Z^2}{(2l+1)n^3a_0^2} \\]

It can be also derived from substituting $s=1$ to the Kramers' relation.
</details> <br>

\3. $ \Expct{\dfrac{1}{r^3}} = \dfrac{1}{l(l+\frac{1}{2})(l+1)} \dfrac{Z^3}{n^3a_0^3} $
<details markdown="1"> <summary> Proof </summary>

Let's put $s=-1$ for the Kramers' relation.

\\[ \frac{a_0}{Z}\Expct{\frac{1}{r^2}} - \frac{1}{4}\left[ (2l+1)^2-1 \right]\left(\frac{a_0}{Z}\right)^2\Expct{\frac{1}{r^3}} = 0  \\]

\\[ \therefore \Expct{\frac{1}{r^3}} = \frac{1}{l(l+\frac{1}{2})(l+1)} \frac{Z^3}{n^3a_0^3} \\]

</details> <br>

\4. $ \expct{r} = \dfrac{1}{2}\Big[ 3n^2-l(l+1) \Big]\dfrac{a_0}{Z} $
<details markdown="1"> <summary> Proof </summary>

It can be similarly shown by the Kramers' relation.

</details> <br>

\5. $ \expct{r^2} = \dfrac{1}{2}\Big[ 5n^2+1-3l(l+1) \Big]\dfrac{n^2a_0^2}{Z^2} $
<details markdown="1"> <summary> Proof </summary>

Either.

</details> <br>

\6. $ \Expct{H} = -\dfrac{Z^2e^2}{8\pi\vpmt n^2a_0} $
<details markdown="1"> <summary> Proof </summary>

We showed it _[here](/physics/hydrogen-atom-schrodinger.html)_.

</details> <br>

\7. $ \Expct{V} = -\dfrac{Z^2e^2}{4\pi\vpmt n^2a_0} $
<details markdown="1"> <summary> Proof </summary>

It is trivial from 1.

</details> <br>

\8. $ \Expct{T} = \dfrac{Z^2e^2}{8\pi\vpmt n^2a_0} $
<details markdown="1"> <summary> Proof </summary>

It is trivial from 6 and 7.

</details> <br>

We can also check that classical _virial theorem_, which is here $ \expct{T}=-\dfrac{1}{2}\expct{V} $, is satisfied.