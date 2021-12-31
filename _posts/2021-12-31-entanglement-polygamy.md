---
layout: post
title: Entanglement polygamy is possible for qudits
date: 2021-12-31
description: an example of a blog post with some math
tags: quantum information
categories: physics
---

*Assume reader background knowledge: quantum mechanics, 2-state system, density matrix formalism*

In condensed matter or quantum information textbooks, you may have encountered the concept [**entanglement monogamy**](https://en.wikipedia.org/wiki/Monogamy_of_entanglement), which states that there can be at most two qubits that are maximally entangled; i.e. if two qubits are maximally entangled, you cannot entangle them with additional qubits. 

Background knowledge: what does it mean for 2 qubits to be maximally entangled?
There are two ways to show that 2 qubits are maximally entangled. Let $$\ket{\psi}$$ be the state of interest. 

1) One way is to measure the spin-spin correlation function $$\bra{\psi} S_i\otimes S_i \ket{\psi}$$ in all spatial directions. If the state is maximally entangled, then the correlation function is 



I will show that one of the Einstein-Pedolsky-Rosen (EPR) state 





Now, it is easy to think that quantum particles in general exhibit entanglement monogamy; this turns out to be wrong. I made this mistake, that's why I am writing this post to repend for my sins. In short, entanglement monogamy only applies to qubits, which are particles with two possible states. To circumvent entanglement monogamy, we will instead use qu**d**its, which are particles with $$d$$ possible states. 

that it is in fact possible to maximally entangled arbitrary number of particles. I call this **entanglement polygamy**. 

Since entanglement monogamy rules out qubits 




\begin{equation}
\label{eq:cauchy-schwarz}
\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
\end{equation}

and by adding `\label{...}` inside the equation environment, we can now refer to the equation using `\eqref`.