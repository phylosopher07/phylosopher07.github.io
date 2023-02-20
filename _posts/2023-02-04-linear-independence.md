---
title: Linear Independence
subtitle: Linear Algebra 1.2
author: jiho
date: 2023-02-04 12:00:00 +0800
categories: [Learning, Mathematics, Linear Algebra]
tags: [mathematics, linear algebra, linear combination, linear independence]
math: true
---

## Linear combination
Given a set S of elements of a $F$-vector space $V$,
a **linear combination** of elements of S is an element of V of the following form.

* $ i\in\set{1,\dotsc,n} $
* $ a_i\in F,\; S=\set{\b{v}_i\in V}\subset V $
* $ \dsum_{i=1}^n a_i\b{v}_i $ : a linear combination of $S$

The scalars $ a_i $ are called the coefficients of the linear combination.


## Linear independence
We can then define whether the vectors of $S$ are independent or dependent. <br>
The elements of a subset $S$ of $V$ are said to be linearly independent if no element of $S$ can be written 
as a linear combination of the other elements of $S$.
Equivalently, they are linearly independent if two linear combinations of elements of $S$ 
define the same element of $V$ if and only if they have the same coefficients.

* **Linearly independent**: $ \dsum_{i=1}^n a_i\b{v}_i=0 \iff \forall a_i=0 $
* **Linearly dependent**: $ \neg $ linearly independent


