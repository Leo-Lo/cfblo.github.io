---
layout: post
title: Tight-binding convention
date: 2022-03-24
description: Fourier transform convention for the 2nd quantized operators
tags: condensed-matter reference
categories: physics
comments: true
---



Convention: we use natural units $c=\hbar=1$.

# Landau level Chern number

I want to discuss what is the Landau level, and why it has Chern number $1$.

## The setting

For a (spinless) electron in a $B$ field in the $z$ direction, the Hamiltonian is
$$
\hat H = (\hat{\bold{p}}-e\hat{\bold A})^2/2m
$$
We choose the Landau gauge $\bold A = (0,xB,0)^T$ such that $\bold B = \nabla \times \bold A =\frac{\partial}{\partial x} (xB) \hat z= B\hat z$.

Now expanding the Hamiltonian in terms of its spatial components
$$
\begin{align*}
\hat{H} &= \frac{1}{2m}\left[\hat{p}_x^2 + (\hat{p}_y-e\hat{x}B)^2\right]\\
&= -\frac{1}{2m}\partial_x^2 + \frac{1}{2m}\left[ (p_y - eBx)^2\right]\\
&= -\frac{1}{2m}\partial_x^2 + \frac{1}{2}m\frac{e^2B^2}{m^2} \left(\frac{p_y}{eB} - x\right)^2
\end{align*}
$$
where in the second equality, we use the eigenbasis of $\hat{p}_y$ such that it reduce from an operator to a scalar. We also use the eigenbasis of $x$. Now, the problem looks like that of a simple harmonic oscillator that oscillate at angular frequency $\omega =\frac{eB}{m} $ about the equilibrium position $x_0= \frac{p_y}{eB}$.



Alright, until now this has nothing to do with band in a condensed matter context, so how do we calculate the Chern number?

First, recall the definition of the Berry curvature or Berry connection

Berry connection: $\bold A(\bold k) = \bra{u} \partial_{\bold k} \ket{u}$

Berry curvature: $\bold B = \nabla \times \bold A = $ . Or can also define it as the sympletic 2-form? 



How the fuck do I get the state if the band structure may not even be well-defined? 

### What are the form of the eigenstates of Landau levels?

Since it is a harmonic oscillator problem, the lowest Landau level will just be a Gaussian in the $x$ direction, and plane wave in the $y$ direction. 

For the simplest equation $(-\partial_x^2 + x^2)\psi(x) = E_0 \psi(x)$, I can guess the solution $\psi(x)=Ae^{\alpha x^2}$. Then 
$$
\begin{align*}
\partial_x^2 (Ae^{\alpha x^2}) &= A\partial_x(2\alpha x e^{\alpha x^2}) \\
&= 2\alpha A (e^{\alpha x^2} + 2\alpha x^2e^{\alpha x^2})\\
&= 2\alpha A e^{\alpha x^2} + 4\alpha^2 A x^2e^{\alpha x^2}\\
\end{align*}
$$
Then 
$$
-2\alpha A - 4\alpha^2 Ax^2 + x^2 = E_0 \implies 
\begin{cases}
4\alpha^2A^2 = 1\\
-2\alpha A = E_0
\end{cases}
$$
which fixes $A = \pm \frac{1}{2\alpha}$ and $E_0 = \mp 1$.



















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

