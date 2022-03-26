---
layout: post
title: Tight-binding convention
date: 2022-03-24
description: Fourier transform convention for the 2nd quantized operators
tags: condensed-matter reference
categories: physics
comments: true
---





In second quantized notation, a tight-binding Hamiltonian is given by 
$$
H=\sum_{\bold{R}} c^\dagger_{\bold R \alpha} h_{\alpha\beta}(\bold R) c_{\bold R \beta} = \sum_{\bold{R}}\vec{c}^\dagger_{\bold R} h(\bold R) \vec{c}_{\bold R}
$$
To diagonalize it, we need to transform to the Fourier basis. Below is the convention for (inverse) Fourier transform
$$
\begin{align*} c_{\bold R} &= \frac{1}{\sqrt{N}}\sum_{\bold k} e^{i\bold k \cdot \bold R} c_{\bold k} \quad \quad \quad & c_{\bold k} = \frac{1}{\sqrt{N}}\sum_{\bold R} e^{-i\bold k \cdot \bold R} c_{\bold R}\\c^\dagger_{\bold R} &= \frac{1}{\sqrt{N}}\sum_{\bold k} e^{-i\bold k \cdot \bold R} c^\dagger_{\bold k} \quad \quad \quad & c^\dagger_{\bold k} = \frac{1}{\sqrt{N}}\sum_{\bold R} e^{i\bold k \cdot \bold R} c^\dagger_{\bold R} \end{align*}
$$
And the definition of Kronecker delta 
$$
\delta_{\bold{k}\bold{k’}} = \frac{1}{N} \sum_{\bold R} e^{i(\bold k - \bold k’) \cdot \bold R}
$$
That's it. Now I don't ever need to go back to textbook/random scribbled notes to check the sign convention I should use.

