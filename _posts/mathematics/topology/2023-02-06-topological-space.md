---
layout: post
title: "Topological Space"
subtitle: "tplg1.1"
classification: "Topology 1.1"
categories: mathematics
tags: topology
image:
    path: /assets/img/mathematics/topology/Munkres.jpg
---

from **「Topology」**: _James R. Munkres_
{:.figcaption}

<!--more-->
* this unordered seed list will be replaced by the toc
{:toc}

## Topological space

**Topological space** is, roughly speaking, a geometrical space in which closeness is defined but cannot necessarily
be measured by a numeric distance. More specifically, a topological space is a set whose elements are called **points**,
along with an additional structure called a **topology**, which can be defined as a set of neighbourhoods for
each point that satisfy some axioms formalizing the concept of closeness.

Given a set $X$, a set $\mathcal{T}\sub\mathcal{P}(X)$ is called the **topology** if it satifies following conditions. 
If then, we call the pair $(X,\mathcal{T})$ a topological space.
* $ \empty,X \in \mathcal{T} $
* $ S\sube\mathcal{T} \Rightarrow \bigcup S\sube\mathcal{T} $
* $ U,V\in\mathcal{T} \Rightarrow U\cap V\in\mathcal{T} $

Every set $X$ has its **trivial topology** $\set{\empty,X}$ and **discrete topology** $\mathcal{P}(X)$.

## Open and closed set

We usually define an **open set** as an element of a topolofical space, and **closed set** the complement of them.

For a topological space $(X,\mathcal{T})$,
* $ U\in\mathcal{T} \Rightarrow U: \text{open set} $
* $ F\sub X \;\text{s.t.}\; X\setminus F\in\mathcal{T} \Rightarrow F: \text{closed set} $
* If a set is both open and closed, it is called **clopen set**.

## Examples
* Hausdorff spaces
* Hilbert spaces
* Metric spaces
* Proximity spaces
* Uniform spaces
* Function spaces
* Cauchy spaces
