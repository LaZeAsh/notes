---
title: "Systems of Linear Equations"
---

Introduced in [[Math 115]]

> [! Definition 2.1.2]
> A **linear equation** in n variables is an equation of the form 
> 
> $a_1x_1 + a_2x_2 + \dots a_nx_n = b$
> Where $x_1, \dots , x_n \in \mathbb{R}$ are the variables or unknowns, $a_1, \dots , a_n \in \mathbb{R}$ are coefficients and b $\in \mathbb{R}$ is the constant term. A system of linear equations (also called a linear system of equations) is a collection of finitely many linear equations

A linear system of equations is considered **consistent** if it has at least one solution. Otherwise, we call the linear system **inconsistent**

> [! Definition 2.2.5]
> The first nonzero entry in each row of a matrix is called a **leading entry** (or a **pivot**). A matrix is in **Row Echelon Form (REF)** if
> 
> a) All rows whose entries are all zero appear below all rows that contain nonzero entries
> 
> b) Each leading entry is to the right of the leading entries above it
> A matrix is in **Reduced Row Echelon Form (RREF)** if it is in REF and
> 
> c) Each leading entry is a 1, called a **leading one**
> 
> d) Each leading entry is the only nonzero entry in its column

