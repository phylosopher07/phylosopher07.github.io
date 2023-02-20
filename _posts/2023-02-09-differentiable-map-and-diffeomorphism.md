---
title: Differentiable Map and Diffeomorphism
subtitle: Differential Geometry 1.4
author: jiho
date: 2023-02-09 00:00:00 +0800
categories: [Learning, Mathematics, Differential Geometry]
tags: [mathematics, differential geometry, differentiable map, diffeomorphism]
math: true
---

## Differentiable map
Given an $m$-dimensional differentiable manifold $M$ and an $n$-dimensional differentiable manifold $N$,
we can think of a function $f$ from $M$ to $N$.
If the function from a local coordinate of $M$ to a local coordinate of $N$ is differentiable,
$f$ is called a **differentiable map**.

* $ \exist(U,\varphi)\in\mathcal{A}_M,\; (V,\psi)\in\mathcal{A}_N $
* $ \psi\circ f\circ\varphi^{-1} : \varphi(U)\to\psi(V) \;\text{is}\; C^k \Rightarrow f\in C^k(M,N) $

For example,
* $ f\in C^0(M,N) $ : continuous map
* $ f\in C^1(M,N) $ : differentiable map
* $ f\in C^\infty(M,N) $ : smooth map
* $ f\in C^\omega(M,N) $ : analytic map

## Diffeomorphism

In the same situation as above, let's continue discussing about the function $f$.
If $f$ satisfies the following properties, we call it a **diffeomorphism**.
* $f$ is a _bijection_
* $f$ is _differentiable_
* $f^{-1}$ is _differentialbe_

If such $f$ exists, $M$ and $N$ are **diffeomorphic**; $M \simeq N$. 

This concept can be extended as $C^k$ diffeomorphicity;
with $C^k$ condition instead of the differentiability condition.

In addition, we can define _local diffeomorphism_ when the domain is restricted.
* $ x\in M,\; V\in\mathcal{N}_x,\; W=f(V) $
* $ f\|_V : V \to W $ : a local diffeomorphism at $x$
