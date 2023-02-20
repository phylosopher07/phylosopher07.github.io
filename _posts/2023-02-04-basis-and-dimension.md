---
title: Basis and Dimension
subtitle: Linear Algebra 1.4
author: jiho
date: 2023-02-04 15:00:00 +0800
categories: [Learning, Mathematics, Linear Algebra]
tags: [mathematics, linear algebra, basis, dimension]
math: true
---

## Basis

A set $B$ of vectors in a vector space $V$ is called a **basis** if
every element of $V$ may be written in a unique way as a finite linear combination of elements of $B$.
The coefficients of this linear combination are referred to as **components** or **coordinates**
of the vector with respect to $B$. The elements of a basis are called **basis vectors**.

* $ B \subset V $
* $B$ is linearly independent
* $ \span(B)=V $

An ordering can be done by numbering the basis elements.
To emphasize that an order has been chosen, one speaks of an **ordered basis**,
which is therefore not simply an unstructured set, but a sequence; an indexed family.

![Basis](https://upload.wikimedia.org/wikipedia/commons/f/f4/3d_two_bases_same_vector.svg)
_The same vector can be represented in two different bases (purple and red arrows)._


### Properties
* $L$: a linearly independent subset of a spanning set $S \sube V$ <br>
basis $ \exist B \;\text{s.t.}\; L \sube B \sube V $
  + This implies that it is possible to make a basis by properly choosing and adding vectors from $V$.
    The possibility is guaranteed by the _axiom of choice_.


## Dimension

All bases of an arbitrary vector space have the same cardinality, which is called the **dimension** of vector space.
* $B$ is a basis of $V$ $ \Rightarrow \dim{V}= \card{B} $
* The definition applies equally even when $B$ is an infinite set.

It is so easy to prove that the dimension is well-defined; read Wikipedia for the details.
* [Steinitz exchange lemma](https://en.wikipedia.org/wiki/Steinitz_exchange_lemma) (for finite dimensions)
* [Dimension theorem](https://en.wikipedia.org/wiki/Dimension_theorem_for_vector_spaces) (for infinite dimensions)

### Properties
* $ W \le V \Rightarrow \dim{W} \le \dim{V} $
* For a vector space $V$ on a field $F$, <br>
$ \card{V}= \begin{cases}
\card{F}^{\dim{V}} & :\text{finite} \newline
\max(\card{F},\dim V) & :\text{infinite}
\end{cases} $
