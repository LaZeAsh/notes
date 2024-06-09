---
title: "Softmax Function"
---

$\sigma$($\vec{z}$)$_i$ = $\frac{e^{z_i}}{\sum_{j=1}^K e^{z_j}}$

- $\sigma$ = Softmax
- $\vec{z}$ = input vector
- e$^{z_i}$ = standard exponential function for input vector
- K = number of classes in multi-class classifier
- e$^{z_j}$ = standard exponential function for output vector

Learned about Softmax Equation when learning about [[Temperature (LLMs)]]

## Purpose

The purpose of the function is to convert a set of numbers into probabilities. Each number represents confidence level of a model that a particular data point belongs to a certain class.

Basically takes input and outputs probabilities (from my understanding) of that being the next thing generated

Similar to the [[Maxwell-Botlzmann Speed Distribution]]
