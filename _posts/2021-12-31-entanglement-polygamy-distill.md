---
layout: distill
title: Entanglement polygamy is possible for qudits dist
date: 2021-12-31
description: Or, given more room, quantum particles enjoy more company.
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

*Assume reader background knowledge: quantum mechanics, 2-state system, density matrix formalism*

## Intro

In condensed matter or quantum information textbooks, you may have encountered the concept [**entanglement monogamy**](https://en.wikipedia.org/wiki/Monogamy_of_entanglement), which states that there can be at most two qubits that are maximally entangled; i.e. if two qubits are maximally entangled, you cannot entangle them with additional qubits. 

Now, it is easy to think that quantum particles in general exhibit entanglement monogamy; this turns out to be wrong. I made this mistake, that's why I am writing this post to repend for my sins. In short, entanglement monogamy only applies to *qubits*, which are particles with two possible states. To circumvent entanglement monogamy, we will instead use *qu**d**its*, which are particles with $$d$$ possible states. Then, it is in fact possible to maximally entangled arbitrary number of particles. I call this **entanglement polygamy**. This is the result we will arrive at by the end of this blogpost.

### Conventions

Here are the convention I will use (feel free to skip this part now and come back to this when you see it used in the article.

 * For a qubits, the two possible states are $$\ket{\uparrow}$$ and $$\ket{\downarrow}$$ such that $$S_z \ket{\uparrow} = \frac{\hbar}{2} \ket{\uparrow}$$ and $$S_z \ket{\downarrow} = -\frac{\hbar}{2} \ket{\downarrow}$$. 
 * For multi-particle system, which can be expressed as a tensor product state, 


## Maximally entangled defined

What does it mean for 2 qubits to be maximally entangled? There are two ways to show that 2 qubits are maximally entangled. Let $$\ket{\psi}$$ be the state of interest. 

1) One way is to measure the spin-spin correlation function $$\bra{\psi} S_i\otimes S_i \ket{\psi}$$ in all 3 spatial directions ($$i=1,2,3$$) and see if the correlation function is maximally in *all 3* spatial directions. 

2) Another way is to look at the reduced density matrix for each of the particle, then calculate whether the corresponding Von Neumann entropy is maximized, i.e. that of a uniform probability distribution.


## Bell state example

I will now show that one of the [Bell states](https://en.wikipedia.org/wiki/Bell_state) (sometimes also called the EPR pairs)

\begin{equation}
\ket{EPR}= \frac{1}{\sqrt{2}}\left(\ket{00}+\ket{11}\right)
\end{equation}

is a maximally entangled state, using both approach mentioned above. I will use the density matrix formalism, since the second approach (which involves calculating the Von Neumann entropy) hinges on the density matrix formalism. In this formalism, the density matrix representing the state is 

$$
\rho = \ket{EPR}\bra{EPR} = \frac{1}{2}
\begin{pmatrix}
1 & 0 & 0 & 1 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
1 & 0 & 0 & 1
\end{pmatrix}
$$

where the indexing of the 4 entries are $$\ket{00},\ket{01},\ket{10},\ket{11}$$. 


### 1st approach: spin-spin correlation function

$$
\begin{align*}
1 &= 2\\
2 &= 3
\end{align*}
$$


### 2nd approach: Von Neumann entropy of reduced density matrices





## Maximally entangle 3 quantum particles

The idea I have is to not restrict ourselves to just 


















