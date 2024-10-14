---
title: "The Norm and Dot Product"
---

## Norm
The norm (aka length or magnitude) of $\overrightarrow{x}$ = $\begin{bmatrix} x_1 \\ x_2 \\ ... \\ x_k \end{bmatrix}$
\|$\vec{x}$\| = $\sqrt{x_1^2 + \cdots + x_k^2}$

$\vec{x}$ = $\begin{bmatrix} 1 \\ 2 \end{bmatrix}$ $\in$ $\mathbb{R}^2$ then \| $\vec{x}$ \| = $\sqrt{1^2 + 2^2}$ = $\sqrt{5}$

## Properties of the Norm

Let $\vec{x}, \vec{y} \in \mathbb{R}^n$ and c $\in \mathbb{R}$. Then

1. \\| $\vec{x}$ \| $\geq$ 0 with equality if and only if $\vec{x} = \vec{0}$ 
2. \\| c $\vec{x}$ \| = \| c \| \| $\vec{x}$ \| 
3. \\| $\vec{x} + \vec{y}$ \| $\leq$ \| $\vec{x}$ \| + \| $\vec{y}$ \| (The Triangle Inequality)


2 nonzero vectors in $\mathbb{R}^n$ are parallel if they are scalar multiples of one other

A vector $\vec{x}$ is a unit vector if \| $\vec{x}$ \| = 1

$\hat{x}  = \frac{1}{\| \vec{x} \| }\vec{x}$ 

is called the normalization of $\vec{x}$ 

## Dot Product

Let $\vec{x}$ = $\begin{bmatrix} x_1 \\ ... \\ x_n \end{bmatrix}$ and $\vec{y}$ = $\begin{bmatrix} y_1 \\ ... \\ y_n \end{bmatrix}$ be vectors in $\mathbb{R}^n$. The dot product of $\vec{x}$ and $\vec{y}$ is the real number

$\vec{x} \cdot \vec{y}$ = $x_1 y_1 + \dots + x_ny_n$

## Properties of Dot Product

Let $\vec{w}, \vec{x}, \vec{y} \in \mathbb{R}^n$ and c $\in \mathbb{R}$

1. $\vec{x} \cdot \vec{y} \in \mathbb{R}$
2. $\vec{x} \cdot \vec{y}$ = $\vec{y} \cdot \vec{x}$
3. $\vec{x} \cdot \vec{0}$ = 0
4. $\vec{x} \cdot \vec{x}$ = \| $\vec{x}$ \|$^2$ 
5. $(c\vec{x}) \cdot \vec{y} = c(\vec{x} \cdot \vec{y}) = \vec{x} \cdot (c \vec{y})$
6. $\vec{w} \cdot (\vec{x} \pm \vec{y}) = \vec{w} \cdot \vec{x} \pm \vec{w} \cdot \vec{y}$

## Cauchy–Schwarz Inequalty

This is how the theorem is spelled in the textbook

For any two vectors $\vec{x}, \vec{y} \in \mathbb{R}^n$ we have

\| $\vec{x} \cdot \vec{y} \| \leq \| \vec{x} \| \| \vec{y} \|$


Two vectors are said to be `orthogonal` if $\vec{x} \cdot \vec{y} = \vec{0}$ 

$\theta$ = arccos ($\frac{\vec{x} \cdot \vec{y}}{\| \vec{x} \| \| \vec{y} \|})$

- $\vec{x} \cdot \vec{y} > 0 \iff 0 \leq \theta \frac{\pi}{2} \iff \vec{x}$  and $\vec{y}$ determine an acute angle
- $\vec{x} \cdot \vec{y} = 0 \iff 0 = \frac{\pi}{2} \iff \vec{x}$  and $\vec{y}$ are perpendicular
- $\vec{x} \cdot \vec{y} < 0 \iff \frac{\pi}{2} < \theta \pi \iff \vec{x}$  and $\vec{y}$ determine an obtuse angle


