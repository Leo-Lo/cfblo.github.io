---
layout: distill
title: Entanglement polygamy is possible for qudits (draft)
date: 2021-12-31
description: Or, given more room, quantum particles enjoy more company.
tags: quantum-information draft exposition
categories: physics
comments: true

authors:
  - name: Leo Lo
    url: "https://leo-lo.github.io"
    affiliations:
      name: Columbia University

toc:
  - name: Intro
  - name: Maximally entangled defined
  - name: Bell state example
  - name: Maximally entangle 3 quantum particles

---


(Warning: This post is incomplete)

*Assume reader background knowledge: quantum mechanics, 2-state system*

## Intro

In condensed matter or quantum information textbooks, you may have encountered the concept [**entanglement monogamy**](https://en.wikipedia.org/wiki/Monogamy_of_entanglement), which states that there can be at most two qubits that are maximally entangled; i.e. if two qubits are maximally entangled, you cannot entangle them with additional qubits. 

Now, it is easy to think that quantum particles in general exhibit entanglement monogamy; this turns out to be wrong. I made this mistake, that's why I am writing this post to repend for my sins. In short, entanglement monogamy only applies to *qubits*, which are particles with two possible states. To circumvent entanglement monogamy, we will instead use *qu**d**its*, which are particles with $$d$$ possible states. Then, it is in fact possible to maximally entangled arbitrary number of particles. I call this **entanglement polygamy**. This is the result we will arrive at by the end of this blogpost. For the experts, feel free to directly skip to the [Maximally entangle 3 quantum particles](https://leo-lo.github.io/blog/2021/entanglement-polygamy-distill/#maximally-entangle-3-quantum-particles) section.

### Conventions

Here are the convention I will use (feel free to skip this part now and come back to this when you see it used in the article.

 * The spin-1/2 angular momentum operators acts as $$S_i \ket{psi} = \frac{\hbar}{2} \sigma_i \ket{\psi}$$. 
 * For a qubits, the two possible states are $$\ket{\uparrow}$$ and $$\ket{\downarrow}$$ such that $$S_z \ket{\uparrow} = \frac{\hbar}{2} \ket{\uparrow}$$ and $$S_z \ket{\downarrow} = -\frac{\hbar}{2} \ket{\downarrow}$$. 
 * For bipartite system, which can be expressed as a tensor product state, the operator are in general of the from $$\sum_{i,j} A_i \otimes B_j$$.


## Maximally entangled defined

What does it mean for 2 qubits to be maximally entangled? Let $$\ket{\psi}$$ be the state of representing the 2 qubits. We can measure the spin-spin correlation function $$\bra{\psi} S_i\otimes S_i \ket{\psi}$$ in all 3 spatial directions ($$i=1,2,3$$) and see if the correlation function is maximized in *all 3* spatial directions. If all 3 are maximized, the 2 qubits are maximally entangled.


## Bell state example

I will now show that one of the [Bell states](https://en.wikipedia.org/wiki/Bell_state) (sometimes also called the EPR pairs)

\begin{equation}
\ket{EPR}= \frac{1}{\sqrt{2}}\left(\ket{00}+\ket{11}\right)
\end{equation}

is a maximally entangled state (in fact, all 4 Bell states are maximally entangled). 

Working out the correlation function $$\langle S_x^{(1)}\otimes S_x^{(2)} \rangle$$ explicitly:

$$
\begin{align*}
\langle S_x^{(1)}\otimes S_x^{(2)} \rangle = \bra{EPR} S_x^{(1)}\otimes S_x^{(2)} \ket{EPR} &= \text{Tr} (S_x^{(1)}\otimes S_x^{(2)} \rho_{EPR})\\
&= \text{Tr} \left[\frac{1}{\sqrt{2}}\left(S_x^{(1)}\ket{0}\otimes S_x^{(2)}\ket{0} + S_x^{(1)}\ket{1}\otimes S_x^{(2)}\ket{1}\right)\bra{EPR}\right]\\
&= \frac{\hbar^2}{4} \text{Tr} \left[\frac{1}{\sqrt{2}}\left(\ket{1}\otimes \ket{1} + \ket{0}\otimes \ket{0}\right)\bra{EPR}\right]\\
&= \frac{\hbar^2}{4} \text{Tr} \left[\ket{EPR}\bra{EPR}\right]\\
&= \frac{\hbar^2}{4} \text{Tr} [\rho_{EPR}]\\
&= \frac{\hbar^2}{4}
\end{align*}
$$

The spin-spin correlation function is maximized, since it reports the value $$\frac{\hbar^2}{4}$$, which means whenever one measure the 1st spin to have $$S_x$$ expectation value $$\pm \frac{\hbar}{2}$$, the 2nd spin would also have expectation value $$\pm \frac{\hbar}{2}$$.

The correlation function in the other 2 directions can be obtained in the same way, so I shall leave it as an exercise for the reader ;) What's important is the result: in **all 3 directions, the spin-spin correlation function is maximized**. This is the indicator for a maximcally entangled spin state.

As a side remark, having maximized spin-spin correlation functions in all spatial directions is not possible for any classical state. The best a classical state can do is a mixed state, e.g. $$\rho = \frac{1}{2} \ket{00}\bra{00} +\frac{1}{2} \ket{00}\bra{00}$$, which maximized the spin-spin correlation function in 1 direction: $$\langle S_z^{(1)}\otimes S_z^{(2)} \rangle$$; however, the x- and y- component of spin will be completely uncorrelated, i.e. , $$\langle S_x^{(1)}\otimes S_x^{(2)} \rangle = \langle S_y^{(1)}\otimes S_y^{(2)} \rangle = 0$$.

Another way to see that $\ket{EPR}$ is maximally entangled is that even though it is a pure state, the reduced density matrix is $$\rho = \frac{1}{2}\ket{0}\bra{0} + \frac{1}{2}\ket{1}\bra{1}$$, which is a classical mixed state with maximal Von Neumann entropy.


## Maximally entangle 3 quantum particles

In order to maximally entangle 3 particles, my idea is to not restrict ourselves to just qubits (spin-1/2 particles), but use spin-1 particle. My claim is that the following state is maximally entangled

$$
\ket{\psi} = \frac{1}{\sqrt{3}} (\ket{abc} + \ket{bca} + \ket{cab})
$$

where $$a=-1, b=0, c=1$$.

Now, as a first indicator that it is maximally entangled, we note that the reduced density matrix for the 1-particle subsystem is $$ \rho_1 =  \frac{1}{3}\ket{a}\bra{a} + \frac{1}{3}\ket{b}\bra{b} + \frac{1}{3}\ket{c}\bra{c}$$, which is a classically maximally mixed state. 

We then calculate the spin-spin correlation function. 

To be continued...










Addendum: For anyone who is interested in learning more about these materials, I highly recommend checking out *Quantum Computation and Quantum Information* by Michael Nielson and Isaac Chuang (or sometimes affectionately refered to as Mike & Ike); it is very pedagogical on a lot of fascinating topics. 










