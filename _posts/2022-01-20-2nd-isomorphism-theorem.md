---
layout: post
title: The second isomorphism theorem
date: 2022-01-20
description: 
tags: algebra reference
categories: math
comments: true
---

# Motivation

As I often forget how to prove the second isomorphism theorem in group theory, here is one (in all painstaking details) for the record. 

# Theorem statement

Given group $$G$$, subgroup $$S\leq G$$, normal subgroup $$N\trianglelefteq G$$, then
(1) $$SN \leq G$$
(2) $$S\cap N \trianglelefteq S$$
(3) $$(SN)/N \cong S/(S\cap N)$$

## Proof of (1)
First, to show that $$SN$$ is a subset. $$SN=\{sn | s\in S, n\in N\}$$. Since $$s\in G, n \in G$$, by closure of group multiplication, $$sn\in G$$, so $$SN$$ is a subset of $$G$. 

Next, we need to show that $$SN$$ is itself a group. Check the group axioms:

1) Identity: $$e$$ is the identity element in $$SN$$.
2) Inverse: Given $$sn \in SN$$, then its inverse is $$n^{-1}s^{-1}$$. Let $$n_3 = sn^{-1}s^{-1}$$; since $$N$$ is normal, $$n_3\in N$$. Then the inverse element $$n^{-1}s^{-1}= s^{-1}n_3$$, which is in $$SN$$. 
3) Associativity: Since $$s_in_i$$ is an element in $$G$$, by associativity of $$G$$, $$(s_1n_1\cdot s_2n_2)\cdot s_3n_3 = s_1n_1\cdot (s_2n_2\cdot s_3n_3)$$
4) Closure: Need to show $$s_1n_1s_2n_2 \in SN$$. Let $$n_3 = s_2^{-1}n_1s_2$$; by normality of $$N$$, $$n_3\in N$$. Then $$s_1n_1s_2n_2 = s_1 s_2 n_3 n_2$$, which is manifestly in $$SN$$.


## Proof of (2)
First, $$S\cap N$$ is obviously a subset of $$S$$. 

Next, to show that $$S\cap N$$ is a group. Again check the group axioms:

1) Identity: $$e\in S$$ and $$e\in N$$, so identity exists.
2) Inverse: $$ given k \in S\cap N$$, $$k \in S$$ implies $$ k^{-1} \in S$$; $$k \in N$$ implies $$ k^{-1} \in N$$; hence $$k^{-1}\in S\cap N$$.
3) Associativity: Obvious as group elements of $$G$$.
4) Closure: Given $$k,p \in S\cap N$$, $$kp \in S$$, $$kp \in N$$, so $$kp \in S\cap N$$.

Last, to show that $$S\cap N$$ is normal with respect to $$S$$, need to show $$\forall k \in S\cap N, \forall s\in S, sks^{-1} \in S\cap N$$. Since both $$s,k\in S, sks^{-1}\in S$$. Since $$k\in N, s\in G$$ and $$N \trianglelefteq G$$, sks^{-1} \in N$$. So $$sks^{-1} \in S\cap N$$.

## Proof of (3)

In order to form the quotient group $$(SN)/N$$, need to first show that $$N \trianglelefteq SN$$. We already know $$N$$ is a subset of $$SN$$, and it is a group, so it remains to show the normality condition. $$\forall n'\in N, sn \in SN$$, need to show $$(sn) n' (sn)^{-1}=snn'n^{-1}s^{-1} \in N$$. First insert pairs of $$s^{-1}s$$ in between every elements of $$N$$ to obtain $$(s n s^{-1}) (s n' s^{-1})(s n^{-1} s^{-1})$$. Since $$N \trianglelefteq G$$, all three parathesized elements are in $$N$$, and then use closure to conclude $$(sn) n' (sn)^{-1}\in N$$. 

Next, need to understand the group element in $$(SN)/N$$ and $$S/(S\cap N)$$. $$(SN)/N=\{[[sn] \in SN| s_1n_1 \sim s_2 n_2 \text{ if } \exists n \text{ such that } s_1n_1 = n \cdot s_2n_2\}. 

One strategy is to construct a homomorphism $$(SN)/N \rightarrow S/(S\cap N)$$, then show its inverse exists. Or show it is both injective and surjective. This requires quite a lot of low-level detail defining the homormophisms and proving their properties.

A better strategy is to use the first isomorphism theorem: given a homomorphism $$h: G\rightarrow H$$, then $$G/\text{ker}(h) = \text{Im}(h)$$. I can choose a surjective homormophism such that either of
1) $$h: SN \rightarrow S/(S\cap N)$$ such that $$\text{ker}(h)=N, \text{Im}(h) = S/(S\cap N)$$
2) $$h: S \rightarrow (SN)/N$$ such that $$\text{ker}(h)=S\cap N, \text{Im}(h) = (SN)/N$$

We will take option 1). Define the homomorphism $$h: SN \rightarrow S/(S\cap N)$$ as $$h(sn) = [s]$$, with the equivalence relation $$s_1\sim s_2$$ if $$\exists n\in N$$ such that $$s_1=n s_2$$. This homomorphism is surjective since $$\forall [s]\in S/(S\cap N), \exists s\in S$$ such that $$h(s)=[s]. To find the kernel of the homomorphism, need to know what is in the equivalence class $$[e]$$, which by definition of $$S/(S\cap N)$$, is $$N$$. Then $$\forall n\in N, h(n) = [e]$$. For $$s \in SN, s\notin N$$, h(s)=[s]\neq [e]$$. Therefore, $$\text{ker}(h)=N. 

Q.E.D.






















