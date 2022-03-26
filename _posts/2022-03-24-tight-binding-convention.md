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
H=\sum_{\boldsymbol{R}} c^\dagger_{\boldsymbol R \alpha} h_{\alpha\beta}(\boldsymbol R) c_{\boldsymbol R \beta} = \sum_{\boldsymbol{R}}\vec{c}^\dagger_{\boldsymbol R} h(\boldsymbol R) \vec{c}_{\boldsymbol R}.
$$


To diagonalize it, we need to transform to the Fourier basis. Below is the convention for (inverse) Fourier transform
$$
\begin{align*} c_{\boldsymbol R} &= \frac{1}{\sqrt{N}}\sum_{\boldsymbol k} e^{i\boldsymbol k \cdot \boldsymbol R} c_{\boldsymbol k} \quad \quad \quad & c_{\boldsymbol k} = \frac{1}{\sqrt{N}}\sum_{\boldsymbol R} e^{-i\boldsymbol k \cdot \boldsymbol R} c_{\boldsymbol R}\\c^\dagger_{\boldsymbol R} &= \frac{1}{\sqrt{N}}\sum_{\boldsymbol k} e^{-i\boldsymbol k \cdot \boldsymbol R} c^\dagger_{\boldsymbol k} \quad \quad \quad & c^\dagger_{\boldsymbol k} = \frac{1}{\sqrt{N}}\sum_{\boldsymbol R} e^{i\boldsymbol k \cdot \boldsymbol R} c^\dagger_{\boldsymbol R} \end{align*}
$$


And the definition of Kronecker delta is
$$
\delta_{\boldsymbol{k}\boldsymbol{k’}} = \frac{1}{N} \sum_{\boldsymbol R} e^{i(\boldsymbol k - \boldsymbol k’) \cdot \boldsymbol R}.
$$
That's it. Now I don't ever need to go back to textbook/random scribbled notes to check the sign convention I should use.

