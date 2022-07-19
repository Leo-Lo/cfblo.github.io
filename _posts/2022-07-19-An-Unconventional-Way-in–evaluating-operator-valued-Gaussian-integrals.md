---
layout: post
title: An Unconventional Way in evaluating operator-valued Gaussian integrals
date: 2022-07-19
description: Slogan: to hell with ordering at first, and ask for forgiveness later.
tags: exposition reference operator-algebra
categories: physics math
comments: true
---


I want to prove the following resolution to the identity: 
$$
\begin{equation}
\mathbb 1 = \frac{1}{\pi} \int d^2\alpha\space \ket{\alpha} \bra{\alpha} 
\end{equation}
$$
where $$d^2\alpha = d\mathbb{Re}(\alpha) d\mathbb{Im}(\alpha)= \frac{1}{2}d\alpha d\bar\alpha$$, and the state $$\ket{\alpha} = e^{-|\alpha|^2/2}e^{\alpha a^\dagger} \ket{0}$$ denotes a coherent state.

## My unconventional method

The main idea of the method can be captured by the slogan "to hell with ordering at first, and ask for forgiveness later." We first massage the RHS into the form
$$
\begin{align*}
RHS &=\frac{1}{2 \pi} \int d\alpha \space d\bar\alpha \space e^{-|\alpha|^2} e^{\alpha a^\dagger} \ket{0}\bra{0} e^{\bar\alpha a}\\
&= \frac{1}{\pi}\int  dR \space dI \space e^{- R^2-I^2} e^{(R+iI) a^\dagger} \ket{0}\bra{0} e^{(R-iI) a}
\end{align*}
$$
where I have defined $$R\equiv \mathbb{Re}(\alpha), I=\mathbb{Im}(\alpha)$$ to simplify notation.

Observe that the above integral is a Gaussian integral waiting to be completed the square, except it is obstructed by the ladder operators. Nonetheless, we say, to hell with ordering, let's complete the square directly (and omit the projector $$\ket{0}\bra{0}$$ for now). 
$$
\begin{align*}
RHS &=\space:\frac{1}{\pi} \int dR\space dI \space e^{-R^2 + R(a^\dagger + a)-I^2 + iI(a^\dagger -a)}:\\
&=\space :\frac{1}{\pi}\int dR \space e^{-R^2 + R(a^\dagger + a)} \int dI \space e^{-I^2 + iI(a^\dagger -a)}:\\
&=\space :\frac{1}{\pi} \int dR \space e^{-[R-\frac{1}{2}(a^\dagger+a)]^2 + \frac{1}{4}(a^\dagger+a)^2} \int dI \space e^{-[I-\frac{i}{2}(a^\dagger - a)]^2-\frac{1}{4}(a^\dagger-a)^2}:\\
&=\space : \frac{1}{\pi}\space e^{\frac{1}{4}(a^\dagger+a)^2-\frac{1}{4}(a^\dagger-a)^2}\int d\tilde{R}\space e^{-\tilde R^2} \int d\tilde{I}\space e^{-\tilde I^2}:\\
&=\space : \space e^{\frac{1}{4}(a^\dagger+a)^2-\frac{1}{4}(a^\dagger-a)^2}:
\end{align*}
$$
You might be pulling your hair wondering why I can just break up the exponential and recombine them as if they are just c-numbers instead of operators (normally this would introduce new terms using the BCH formula). So now it's time for me to ask for forgiveness. Observe that initially the identity is normal-ordered: i.e. all the raising operators are to the left, whereas all the lowering operators are to the right. Therefore, the apparent ordering of the above expressions doesn't matter; they are all actually in disguise of a normal-ordered product of operators. That's why I surrounds the expression by colons, to signify that it is in normal ordering.

So let's restore the normal ordering. This means that we are free to move all the raising operators to the left and all the lower operators to the right without introducing commutator terms in the above expression: 
$$
\begin{align*}
''RHS'' &=\space : e^{\frac{1}{4}(a^\dagger+a)^2-\frac{1}{4}(a^\dagger-a)^2}: \\
&= \space :e^{\frac{1}{2}a^\dagger a + \frac{1}{2}a^\dagger a}: \\
&= \space :e^{a^\dagger a}:
\end{align*}
$$
Finally, we need to be careful about how $$e^{a^\dagger a}$$ acts on the projector $$\ket{0}\bra{0}$$. All the raising operators must be to the left of $$\ket{0}\bra{0}$$, whereas all the lowering operators must be to the right of $$\ket{0}\bra{0}$$. So we expand the exponential acting on $$\ket{0}\bra{0}$$ that respects the normal-order:
$$
\begin{align*}
\space e^{a^\dagger a} \text{ (acts on) } \ket{0}\bra{0} &=  \sum_{n=0}^{\infty} \frac{1}{n!}(a^\dagger)^n \ket{0}\bra{0} a^n\\
RHS &=  \sum_{n=0}^{\infty} \frac{1}{n!}\sqrt{n!} \ket{n}\bra{n} \sqrt{n!} \quad \quad \quad \text{since }a^\dagger \ket{n} = \sqrt{n+1} \ket{n+1}\\
&=  \sum_{n=0}^{\infty}\ket{n}\bra{n}\\
&= \mathbb{1}
\end{align*}
$$
Q.E.D.

## Reflection

When I first work it out it is just to see where things go without worrying too much about correctness (since I was pretty clueless lol). But in retrospect, the validity of this method lies in the normal-ordering of the operators in the RHS of the identity. Even though completing the square seems to scramble the ordering of the ladder operators, as long as we assert that at the end we have to recover the normal-ordered operators again, then we are safe. 

It is important to note that I am not applying the normal ordering as an operation. If one tries to normal order an equation that wasn't originally in normal order, we can get non-sensical results such as the following (due to S. Coleman):
$$
a^\dagger a = a a^\dagger -1  \xrightarrow{?} :a^\dagger a:\space =\space : a a^\dagger : -1 \implies a^\dagger a = a^\dagger a -1 \implies 0 = -1
$$
Instead, I start with an expression that is already in normal order, do the Gaussian integrals that apparently scramble the normal order, but insist in the end that it is still in normal order.

