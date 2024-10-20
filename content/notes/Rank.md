---
title: "Rank"
---

Introduced in [[Math 115]]

> [!Definition 2.3.1]
>
> The rank of matrix A, denoted by rank(A), is the number of leading entries in any REF of A.
> 
> If \[A | $\vec{b}$] is an augmented matrix, then rank(\[A | $\vec{b}$]) is the number of leading entries in any REF of \[A | $\vec{b}$]


![[Pasted image 20241018004123.png]]

rank(A) $\leq$ min{m, n}

> [!System Rank Theorem]
> 
> Let \[A | $\vec{b}$] be the augmented matrix of a system of m linear equations in n variables
> 
> a) The system is only consistent if and only if rank(A) = rank(\[A | $\vec{b}$])
> 
> b) If the system is consistent, then the number of parameters in general solution is the number of variables minus the rank of A
>
>	`# of parameters = n - rank(A)`
>	
> c) The system is consistent for all $\vec{b} \in \mathbb{R}^m$ if and only if rank(A) = m

A system of m linear equations in n variables is overdetermined if n < m, this is, if it has more equations than variables

