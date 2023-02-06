---
title: Basis and Dimension
subtitle: Linear Algebra 1.4
author: jiho
date: 2023-02-04 15:00:00 +0800
categories: [Learning, Mathematics, Linear Algebra]
tags: [mathematics, linear algebra, basis, dimension]
math: true
---
$ \global\def\b{\bold} $
$ \global\def\dsum{\displaystyle\sum} $
$ \global\def\span{\text{span}} $
$ \global\def\card#1{\|#1\|} $

## Basis

A set $B$ of vectors in a vector space $V$ is called a **basis** if
every element of $V$ may be written in a unique way as a finite linear combination of elements of $B$.
The coefficients of this linear combination are referred to as **components** or **coordinates**
of the vector with respect to $B$. The elements of a basis are called **basis vectors**.

* $ B \subset V $
* $B$ is linearly independent
* $ \span(B)=V $

An ordering can be done by numbering the basis elements.
In order to emphasize that an order has been chosen, one speaks of an **ordered basis**,
which is therefore not simply an unstructured set, but a sequence; an indexed family.


### Properties
* $L$: a linearly independent subset of a spanning set $S \sube V$ <br>
basis $ \exist B \;\text{s.t.}\; L \sube B \sube V $
  + This implies that it is possible to make a basis by choosing and adding some vectors from $V$ properly.
    The possibility is guaranteed by the _axiom of choice_.


## Dimension

All bases of an arbitary vector space have the same cardinality, which is called the **dimension** of vector space.
* $B$ is a basis of $V$ $ \Rightarrow \dim{V}= \card{B} $
* The defintion apllies equally even when $B$ is an infinite set.

It is so easy to prove that the dimension is well-defined; read wikipedia for the details.
* [Steinitz exchange lemma](https://en.wikipedia.org/wiki/Steinitz_exchange_lemma) (for finite dimensions)
* [Dimension theorem](https://en.wikipedia.org/wiki/Dimension_theorem_for_vector_spaces) (for infinite dimensions)

### Properties
* $ W \le V \Rightarrow \dim{W} \le \dim{V} $
* For a vector space $V$ on a field $F$, <br>
$ \card{V}= \begin{cases}
\card{F}^{\dim{V}} & :\text{finite} \newline
\max(\card{F},\dim V) & :\text{infintie}
\end{cases} $