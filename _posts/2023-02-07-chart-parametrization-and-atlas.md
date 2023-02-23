---
title: Chart, Parametrization and Atlas
subtitle: Differential Geometry 1.2
author: jiho
date: 2023-02-07 09:00:00 +0800
categories: [Learning, Mathematics, Differential Geometry]
tags: [mathematics, differential geometry, chart, parametrization, atlas, transition map]
math: true
---

## Introduction

Topological manifold is one of topological spaces which is locally euclidean.
Thus, we can think of coordinates which represents the neighborhood of a point of the topological manifold.

## Atlas

Let's think of $n$-dimensional topological manifold $M$ and its neighborhoods $U_\alpha$.
Then following homeomorphisms $\varphi_\alpha$ exist, by its definition.
* $ \varphi_\alpha : U_\alpha \to \varphi_\alpha(U_\alpha) \sub \R^n $

Then we call $\varphi_\alpha$ a **coordinate chart** or a **chart**, and $\varphi_\alpha^{-1}$ a **parametrization**.
These terms are very intuitive.

Also, we can think of a set which contains the pair of each neighborhood and chart 
in order to represent the whole manifold.

* $ \dps \mathcal{A} \coloneqq \Set{(U_\alpha,\varphi_\alpha) \| \bigcup_{\alpha\in \Lambda} U_\alpha=M} $

The set $\mathcal{A}$ is called an **atlas** of the topological manifold $M$.
If given the atlas, the topological manifold is called a ***'manifold'***.

## Transition map

Since points of different neighborhoods act on different charts,
it is required to connect them in order to watch some global features(topology) of the manifold.
It's possible using **transition maps**.

Given $n$-dimensional manifold and its atlas $\mathcal{A}$, there'll be neighborhoods which intersects.
(This is assured by the Hausdorff condition of a topological manifold.)

* $ (U_\alpha,\varphi_\alpha),(U_\beta,\varphi_\beta)\in\mathcal{A},\; W=U_\alpha\cap U_\beta \not= \empty $
* $ \tau_{\alpha\beta} : \varphi_\alpha(W) \to \varphi_\beta(W),\;
\tau_{\alpha\beta} \coloneqq \varphi_\beta \vert_W \circ \varphi_\alpha^{-1}\vert_W $

$\tau_{\alpha\beta}$ is a transition map, and it's also a homeomorphism
from a subset of $\R^n$ to a subset of $\R^n$.
Therefore, it's possible to talk about the _continuity_ and _differentiability_ of them.


![Transition map](https://upload.wikimedia.org/wikipedia/commons/0/06/Two_coordinate_charts_on_a_manifold.svg)
_An image describing transition map_
