---
title: 'Optimal Transport'
date: 2020-04-10
permalink: /posts/2020/04/optimal_transport/
tags:
  - mathematics
  - control
  - machine learning
---


<img src="/images/optimal_transport.png" width=200>

Optimal transport studies turning one measure to another while some cost of transportation is minimized. It started in 17th century with practical problems. The theory behind optimal transport developed extensively in nineteenth and twenteenth centruries.

In this post, I review the main theoretical ideas of optimal transport and their interpretations.

There are two major historical points in optimal transport marked with two names _Monge (1781)_ and _Kantorovich (1940)_. In order to compress in one sentence, Monge tried to find a deterministic transport map while Kantorovich is fine with a probabilistic map as well.

We start with a definition of _image measure_ that will be recurring over and over in this post.

**Definition 1.** *Given $X, Y$ spaces, take $T:X\to Y$ and $\mu\in\mathcal{P}(X)$. The image measure represented
    $T\mu\in\mathcal{P}(Y)$ as*

    \begin{equation}
    \forall A\in \mathcal{B}(Y): \quad (T\mu)(A):= \mu(T(A))
    \end{equation}

It can be shown that $T_\#\mu$ is a probability measure on $Y$. Notice that this defintion is one-way, i.e., the pullback operator $S^\#$ does not necessarily give a probability measure.

One practical way to check $\nu\stackrel{?}{=}T_\#\mu$ is to integrate all Borel and Bounded maps $\phi:Y\to\mathbb{R}$ against the measures of both sides

\begin{equation}
\int_{Y} \varphi(y) d \nu(y)=\int_{X} \varphi(T(x)) d \mu(x)
\end{equation}

As a corollary, the _push-forward_ condition is known as

\begin{equation}
\nu=T_# \mu \Rightarrow \int_{Y} \varphi d\left(T_{#} \mu\right)=\int_{X} \varphi \circ T d \mu \label{eq:push_forward_condition}
\end{equation}

for any $\phi:X\to\mathbb{R}$ Borel and bounded.


Measures can be pushed forward via the composition of functions

\begin{equation}
(S \circ T)_{\#} \mu=S_{\#}\left(T_{\#} \mu\right)
\end{equation}

**Definition 2.** *Given $\mu\in\mathcal{P}(X)$ and $\nu\in\mathcal{P}(Y)$, a map $T:X\to Y$ 
    is called a **transport map** from $\mu$ to $\nu$ if $T_\#\mu=\nu$. *

With this defintion, given a $\mu$ and $\nu$, there might be no map that transports $\mu$ to $\nu$. 
To generalize a little bit, **coupling** is defined as a probabilistic map

**Definition 3.** *$\gamma\in\mathcal{P}(X\times Y)$ is called a coupling of $\mu$ and $\nu$ if*

\begin{equation}
\left(\pi_{X}\right)_{\#} \gamma=\mu \text { and }\left(\pi_{Y}\right)_{\#} \gamma=\nu
\end{equation}

*where*

\begin{equation}
\pi_{X}(x, y)=x, \quad \pi_{Y}(x, y)=y \quad \forall(x, y) \in X \times Y
\end{equation}

According to the push-forward condition \eqref{eq:push_forward_condition}, Borel bounded functions $\phi$ and $\psi$ can be used verify a coupling as

\begin{equation}
\forall \varphi: X \rightarrow \mathbb{R} \quad \int_{X \times Y} \varphi(x) d \gamma(x, y)=\int_{X \times Y} \varphi \circ \pi_{X}(x, y) d \gamma(x, y)=\int_{X} \varphi(x) d \mu(x)
\end{equation}

and

\begin{equation}
\forall \psi: Y \rightarrow \mathbb{R} \quad \int_{X \times Y} \psi(y) d \gamma(x, y)=\int_{X \times Y} \psi \circ \pi_{Y}(x, y) d \gamma(x, y)=\int_{Y} \psi(y) d \nu(y)
\end{equation}

Let denote the set of all couplings of the measures $\mu$ and $\nu$ by $\Gamma(\mu, \nu)$. Despite the transport map that can be non-existing for a given $\mu$ and $\nu$, $\Gamma(\mu, \nu)$ is always non-empty. Because at least $\gamma=\mu \otimes \nu$.

Any transport map $T$ induces a couple denoted by $\gamma_T$ defined as

\begin{equation}
\gamma_{T}:=(\mathrm{id} \times T)_{\#} \mu \in \mathcal{P}(X \times Y) \label{eq:transport_map_induces_coupling}
\end{equation}
