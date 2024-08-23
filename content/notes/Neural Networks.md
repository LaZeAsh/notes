---
title: "Neural Networks"
draft: true
---

Many different forms of neural networks but this is dedicated to the plain vanilla form of neural network (Artificial Neural Network).

Neural networks are based off a brain 

## Neuron

A value in a neural network represented by a number between 0 and 1
- This number is called the "Activation"

It's helpful to think of a Neuron as a function that takes the output of the previous layer and spits out a number between 0 and 1
## Layers

- There are 3 types of layers in a neural network
	- Input layer
	- Hidden layers
	- Output layer

## Weights & Biases

Weights and Biases are numbers that can be tweaked to get the desired output you want in a neural network

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

## Sigmoid vs ReLU (Rectified Linear Unit)

Sigmoid at one point was really hard to train with so ReLU was made

What ReLU does is if the neuron passes the threshold it would be identity the function if it is not then it'd just equal 0

Simplification.