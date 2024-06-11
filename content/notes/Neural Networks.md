---
title: "Neural Networks"
---

Many different forms of neural networks but this is dedicated to the plain vanilla form of neural network (Artificial Neural Network).

Neural networks are based off a brain 

## Neuron

A value in a neural network represented by a 0 or 1

## Layers

- There are 3 types of layers in a neural network
	- Input layer
	- Hidden layers
	- Output layer

## Node

Uses a [[Linear Regression]] to predict future events

The weights (or the connection between the nodes) determines how much influence each input has on the output

Each node is composed of: Input data, weights, a bias/threshold, and an output

## Feed forward network

Data being passed between nodes

In the video I am watching this person explained how a neural network works using an example of whether to go surfing or not

![[Math-195.jpg]]


## Rely on training data

As we train the model we want to evaluate it's accuracy using the [[Cost Function]]

Ultimate goal is to minimize the cost function and that happens by adjusting the weights and biases to fit the training dataset

[[Gradient Descent]] allowing the model to determine the direction the direction to take to reduce errors (aka minimizing the cost function)

## Neural Networks have multiple types

- [[Convolutional Neural Networks]] (suited for image recognition)
- [[Recurrent Neural Networks]] (suited for making predictions about future events)