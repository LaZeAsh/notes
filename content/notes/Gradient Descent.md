---
title: "Gradient Descent"
---

How neural networks learn.

Gradient Descent is a powerful optimization algorithm used to train Machine Learning models with the objective of minimizing the Cost Function.
## Cost Function

### Analogy

The way you train a computer to do better is by insulting it, when training the network you mention to the computer what it should be and compare it what the computer returned and tell it to do better. I loved this analogy from the 3Blue1Brown video loool

### Mathematically

You add the up the squares of the differences between the trash output activations and the value you want them to have. This is called the cost of a single training example

Eg: \[(x$_1$ - x$_2$)$^2$ + ... ]

Cost is `high` when the network doesn't seem like it knows what it's doing

Cost is `small` when the network classifies correctly

Average cost is the average of the costs of all the training example, it's also a measure of how lousy the network is and how "bad" the computer should "feel"


What we mean when we say a network is learning is that we're just minimizing the cost function
