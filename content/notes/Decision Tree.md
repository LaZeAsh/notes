---
title: "Decision Tree"
draft: true
---

Decision Tree is a powerful non-parametric supervised learning algorithm

## Attributes of a Decision Tree

`Root Node:`
- The attribute that best classifies training data, use this attribute at the root of the tree
- First split which decides whether the population or sample data should further get divided into 2 or more homogenous sets

`Splitting:` Process of dividing a node in 2 or more sub-nodes

`Decision Node:` This node decides whether/when sub-node splits into further sub-nodes or not

`Leaf:` Terminal Node that predicts the outcome (categorical or continues value). The colored nodes (eg: Yes and No nodes, are leaves)


## ID3 (Iterative Dichotomiser)

ID3 decision tree algorithm uses Information Gain to decide the splitting points. In order to measure information we gain we can use [[Entropy]] (AP Chemistry reference wow) to calculate the homogeneity of a sample.

Flowchart of the ID3 algorithm:

1. Compute the Entropy for data-set [[Entropy]](s)
	- Calculate Entropy (Amount of uncertainty in dataset):
		- Entropy (S) = $\frac{-p}{p + n}$log$_2$($\frac{p}{p+n}$) - $\frac{n}{p+n}$log$_2$($\frac{n}{p+n}$)
2. For every attribute / feature:
	- Calculate entropy for all other values **Entropy(A)**
	- Take **Average Information Entropy** for the current attribute
		- Calculate **Average Information**

## Terminology

`Information Gain`: a measure used in decision trees to evaluate the quality of a split. It represents the expected reduction in impurity (or uncertainty) after splitting a node based on a particular attribute.

Difference between the entropy of the parent node and the weighted average of the entropies of the child nodes