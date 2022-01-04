---
layout: post
title: How to detect entanglement in pure state (very rough draft)
date: 2022-01-01
description: 
tags: quantum-information exposition draft
categories: physics
comments: true
---
(Warning: This post is incomplete)

As an example, I will now show that one of the [Bell states](https://en.wikipedia.org/wiki/Bell_state) (sometimes also called the EPR pairs)

\begin{equation}
\ket{EPR}= \frac{1}{\sqrt{2}}\left(\ket{00}+\ket{11}\right)
\end{equation}

is entangled state, using both approach mentioned above. I will use the density matrix formalism, since the second approach (which involves calculating the Von Neumann entropy) hinges on the density matrix formalism. In this formalism, the density matrix representing the state is 

$$
\rho_{EPR} = \ket{EPR}\bra{EPR} =
\begin{pmatrix}
1/2 & 0 & 0 & 1/2 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
1/2 & 0 & 0 & 1/2
\end{pmatrix}
$$

where the indexing of the 4 entries are $$\ket{00},\ket{01},\ket{10},\ket{11}$$. 


An important identity we need to know is that in density matrix formalism, the expectation value is obtained by 

$$
\begin{align*}
\bra{\psi} \mathcal O \ket{\psi} = Tr (\mathcal O \rho)
&= 
\end{align*}
$$

where $$\rho$$ is the density matrix for the state $$\ket{\psi}$$; the above equality can be demonstrated using the cyclic property of trace. 




### 2nd approach: Relative Von Neumann entropy of reduced density matrices

First of all, we will use the following fact:
* Von Neumann entropy of a state $$\rho$$ is given by $$S = - \Tr(\rho \log \rho) = -sum_i (\lambda_i \log \lambda_i)$$, where $$\lambda_i$$ are the eigenvalues of the density matrix $$\rho$$
* Von Neumann entropy of a pure state is zero. Check it!
* 






We will proceed in 2 steps: 1) obtain the reduced density matrix of a subsystem of just 1 spin, 2) calculate the Von Neumann entropy of the subsystem. 

The reduced density matrix can be obtained using partial trace (WLOG, we partial trace away the 2nd qubit to obtain the reduced density matrix of the 1st qubit):

$$
\begin{align*}
\rho_1 &= \Tr_2(\rho_{EPR})\\
&= \Tr_2(\frac{1}{2}\ket{00}\bra{00} + \frac{1}{2}\ket{00}\bra{11} + \frac{1}{2}\ket{11}\bra{00} + \frac{1}{2}\ket{11}\bra{11}\\
&= \frac{1}{2}\braket{0|0}\ket{0}\bra{0} + \frac{1}{2}\braket{0|1}\ket{0}\bra{1} + \frac{1}{2}\braket{1|0}\ket{1}\bra{0} + \frac{1}{2}\braket{1|1}\ket{1}\bra{1}\\
&= \frac{1}{2}\ket{0}\bra{0} + \frac{1}{2}\ket{1}\bra{1}
\end{align*}
$$




Then we calculate the Von Neumann entropy
$$
\begin{align*}
S &= -\Tr(\rho_1 \log \rho_1)\\
&= \sum_i \Tr(\lambda_i \log \lambda_i) \quad \quad \quad \text{where $\lambda_i$ are the eigenvalues of $\rho_1$}\\
&= \log 2
\end{align*}
$$
