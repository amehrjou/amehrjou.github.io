---
title: 'Brownian Motion'
date: 2020-04-10
permalink: /posts/2020/04/brownian_motion/
tags:
  - mathematics
  - stochastic calculus
---

<p align="center">
<img src="/images/Brownian_motion.gif">
</p>
Brownian motion is the random, uncontrolled movement of particles in a fluid as they constantly collide with other molecules. Brownian motion has been well studied in mathematics and physics and its connections to other seemingly distant areas of mathematics is well established.

In this blog post, I am reviewing the basic concepts of Brownian motion from the perspective of a machine learning researcher.

## Definition of (one-dimensional) Brownian motion

Definition1.1. *We say that the real-valued process $(B(t))_{t≥0}$ is a one-dimensional Brownian motion started from $0$ if:*
* $B(0) = 0$ almost  surely,  and  for  all $t≥0$,  the  law  of $B(t)$ is $\mathcal{N}(0,t)$ (centered Gaussian with variance $t$)
* For  all  positive  integerkand  all $0≤t_1< t_2<···< t_k$,  thekincrements $B(t_1)−B(0),B(t_2)−B(t_1),...,B(t_k)−B(t_{k−1})$ are independent random variables.
* For each $t≥0$ and $h >0$, the law of $B(t+h)−B(t)$ is the same as the law of $B(h)−B(0)$.
* There  exists  a  measurable  set $A$ with  probability $1$ , such that for all $\omega\in A$, the map $t\to B(t)$ is continuous on $R_+$.

The first interesting thing about the Brownin motion is _its existence_. The proof is constructive and gives an iterative way to produce a Brownian motion on dyadic intervals and then extend it to continuous domain.
<p align="center">
<img src="/images/bm_iterative_construction.png" alt="iterative_construction" width="300">
</p>
## Connection to Harmonic Functions

