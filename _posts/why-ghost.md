---
layout: post
title: Why do ghost appear in gauge theories?
date: 2021-10-31
description: 
tags: quantum-field-theory draft exposition
categories: physics
comments: true
---

*For obvious terminology reason, I am retroactively putting the date of this post to be at Halloween. But the Halloween of 2021 also happened to be around the time I pondered and realized the answer to the question of this blogpost.*

# Intro

[Gauge theory](https://en.wikipedia.org/wiki/Gauge_theory) is fundamental in building the Standard Model and many interesting condensed matter model. There is a gauge degree of freedom in the theory, which is just a redundancy in description, but it is needed in order to write down the theory in a manifestly Lorentz-invariant way (as all action should be). 

First, the **short answer** for why ghost arises in gauge theory is that **we need ghosts to fix the gauge in a gauge-invariant way.** At first sight this might seem paradoxical, so the goal of this post is to pinpoint exactly where ghost is needed in the formalism of gauge theories. 

# The main player: the Jacobian determinant

We impose gauge constraints $$G_i(x_j)=0$$, where $$x_i$$ are the gauge degree of freedom, by inserting the Dirac delta into the $$\delta (G_i)


Under a gauge transformation $x\rightarrow y$, this introduces a Jacobian determinant to the gauge fixing

$$ \delta(G_i(x_j)) \rightarrow \frac{1}{det(\mathcal F_{jk})} \delta(G_i(y_k))$$ 

where $$F_{jk}= \frac{\partial y_j}{\partial x^k}$$ is the Jacobian matrix that essentially describe how the differential volume element is changed after the gauge transformation. Since gauge transformation only amounts to choosing a different representative in the gauge orbit, there is no change to the physics. So we want to make sure that the gauge fixing condition is invariant under gauge transformation. Therefore, the invariant gauge fixing condition is 

\begin{equation}
det(\mathcal F_{jk})\delta(G_i(y_k))
\end{equation}

where we multiple with the Jacobian determinant to counter-balance the $$1/(\delta(G_i(y_k))$$ factor from the Dirac delta term. 

# Represent in terms of Feynman diagram

Next, we want to represent everything in the language of Feynman diagrams, i.e. write all the terms in the partition function as a Gaussian integral. In order for the determinant factor to be expressed as an Gaussian integral, we use the following fact about multi-dimensional Grassmann integral: 

\begin{equation}
\int \prod da_i \prod db_j e^{a_i D_{ij} b_j} = \det (D)
\end{equation}

where $$a,b$$ are Grassmann variables (think of them as fermionic field at the classical level). Applying this to our case, we have 

\begin{equation}
\int D \bar{c}_i Dc_j e^{\bar{c}_i \mathcal{F}_{ij} c_j} = \det (\mathcal{F})
\end{equation}

where $$c, \bar{c}$$ are Grassmann-valued fields: $$c$$ is the ghost and $$\bar{c}$$ is the anti-ghost field. Therefore, in order to express the determinant factor as a Gaussian integral (which is necesssary for the gauge fixing condition to transform properly under gauge transformation), we are forced to introduce ghost and anti-ghost. 
















