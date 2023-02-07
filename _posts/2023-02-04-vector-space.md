---
title: Vector Space
subtitle: Linear Algebra 1.1
author: jiho
date: 2023-02-04 01:00:00 +0800
categories: [Learning, Mathematics, Linear Algebra]
tags: [mathematics, linear algebra, vector space]
math: true
---

## Introduction

In mathematics and physics, a vector space is a set whose elements, often called vectors,
may be added together and multiplied by numbers called scalars.
Scalars are often real numbers, but can be complex numbers or, more generally, elements of any field.


## Vector space

**Vector space** is a _module_ whose ring is a _field_. <br>
More specifically, if we have a field $F$, then a vector space over $F$ is a set $V$ together
with two binary operations that satisfy the eight axioms(i.e. _vector axioms_) listed below.
In this context, the elements of $V$, an _$F$-vector space_, are commonly called vectors, and the elements of $F$ are called scalars.
* $ \forall \bold{u,v,w}\in V $
* $ \forall a,b\in F $

| Axiom                                                             | Description                                                  |
|-------------------------------------------------------------------|--------------------------------------------------------------|
| Associativity of vector addition                                  | $ \bold{u+(v+w)=(u+v)+w} $                                   |
| Commutativity of vector addition                                  | $ \bold{u+v=v+u} $                                           |
| Identity element of vector addition                               | $ \exist\bold{0}\in V \;\text{s.t.}\; \bold{v+0=v} $         |
| Inverse elements of vector addition                               | $ \exist\bold{-v}\in V \;\text{s.t.}\; \bold{v+(-v)=0} $     |
| Compatibility of scalar multiplication with field multiplication  | $ a(b\bold{v})=(ab)\bold{v} $                                |
| Identity element of scalar multiplication                         | $ 1\bold{v=v},\; 1:\; \text{multiplicative identity in}\;F $ |
| Distributivity of scalar multiplication with respect to vector addition | $ a\bold{(u+v)}=a\bold{u}+a\bold{v} $ |
| Distributivity of scalar multiplication with respect to field addition | $ (a+b)\bold{v}=a\bold{v}+b\bold{v} $ |

### Examples
* Zero vector space, $ \set{ \bold{0} } $
* Field
* Coordinate space
* Matrices
* Function space
