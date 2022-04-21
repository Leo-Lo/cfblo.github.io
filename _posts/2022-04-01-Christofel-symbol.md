---
layout: post
title: Tight-binding convention
date: 2022-03-24
description: Fourier transform convention for the 2nd quantized operators
tags: condensed-matter reference
categories: physics
comments: true
---





# Christofel symbol

I will derive the Christofel symbol. I learned this derivation from Andrei Boloborodov's course on General Relativity, which imo better motivate the use of Christofel symbol than that presented in Sean Carroll's book.

## Motivation

Why do we need the Christofel symbol? It arises in the context of taking derivative on a general manifold—the partial derivative $\partial_\mu$ does not give a tensorial quantity, and usually we only work with tensors because they transform nicely under the group action (e.g. Lorentz group in general relativity). So the Christofel symbol is introduced to cancel out with the nontensorial part of the partial derivative.

## Concept

A vector $\vec V$ is an invariant object, in the sense that it is independent of the choice of basis. Whereas the component of a vector $V_i$ is dependent on the choice of basis. When learning index notation, we usually abuse notation and call the component $V_i$ the vector, but it is actually the key in this derivation to distinguish between the two.

## Derivation

$$
\begin{align*}
\partial_\mu \vec V &= \partial_\mu (V^\nu \hat e_\nu)\\
&= (\partial_\mu V^\nu)\hat e_\nu + V^\nu (\partial_\mu \hat e_\nu)\\
&\equiv (\partial_\mu V^\lambda)\hat e_\lambda + V^\nu \Gamma_{\mu\nu}^{\lambda}\hat e_\lambda\\
\partial (V^\lambda \hat e_\lambda)&= (\partial_\mu V^\lambda + V^\nu \Gamma_{\mu\nu}^{\lambda})\hat e_\lambda
\end{align*}
$$

where we use the product rule in the 2nd equality, we switch the dummy index $\nu\rightarrow \lambda$ for the 4th equality, and in the 3rd equality we define the Christofel symbol to be
$$
\Gamma^\lambda_{\mu\nu} \hat e_{\lambda} \equiv \partial_\mu \hat e_{\nu}.
$$
such that we can factor out the unit vector $\hat e_\lambda$ at the end.



At the end, we arrive at the defintion of a covariant derivative (which acts on just the component of a vector):
$$
\nabla_\mu V^\nu = \partial_\mu V^\nu + \Gamma^\nu_{\mu\lambda} V^\lambda
$$
If we compare and contrast, 



