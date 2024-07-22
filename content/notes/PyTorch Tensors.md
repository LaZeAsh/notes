---
title: "PyTorch Tensors"
---

Tensors are the center of everything we do in PyTorch.

## Terminology

- 1-dimensional tensor is called a vector
- 2-dimensional tensor is referred to as a matrix
- Anything more than two dimensions is generally just called a tensor

## Define a Tensors

```python
torch.empty(3, 4) # Creates a tensor with 3 rows and 4 columns which is empty

torch.zeros(2, 3) # Creates a tensor with 2 rows and 3 columns with zeros

torch.ones(2, 3) # Creates a tensor with 2 rows and 3 columns with ones

torch.rand(2, 3) # Creates a tensor with 2 rows and 3 columns with random values between 0 and 1

torch.tensor([[3.1415926, 2.71828], [1.61803, 0.0072897]]) # Creates a 2 x 2 tensor with values populated that we mentioned
```

Before using `torch.rand` it is common practice to use `torch.manual_seed` as this allows our results to be reproducible

`torch.tensor` creates a copy of the data
## Tensor Shapes

When performing operations on two or more tensors they will need to be the same shape

`Tensor Shape` - Having the same number of dimensions and same number of cells in each dimension

```python
x = torch.empty(2, 2, 3)

torch.empty_like(x) # Makes a tensor thats the same shape as x and is empty

torch.zeros_like(x) # Makes a tensor thats the same shape as x and is filled with zeros

torch.ones_like(x) # Makes a tensor thats the same shape as x and is filled with ones 

torch.rand_like(x) # Makes a tensor thats the same shape as x and is filled with random values between 0 and 1
```

`.shape` property of a tensor contains a list of each dimension in a tensor

## Tensor Data Types

Setting the datatype of a tensor is possible in a few ways

```python
a = torch.ones((2, 3), dtype=torch.int16) # Makes a tensor with ones as integers (int32)

b = torch.rand((2, 3), dtype=torch.float64) # Makes a tensor with float64 values

c = b.to(torch.int32) # Converts values to int32; contains same values just truncated to int
```

When you define a data type when you print the tensor it specifies its dtype by printing the dtype value

## Math  & Logic with PyTorch Tensors

```python
ones = torch.zeros(2, 2) + 1 # Adds one to the value of the tensor
twos = torch.ones(2, 2) * 2 # Multiples the value of the tensor by 2
threes = (torch.ones(2, 2) * 7 - 1) / 2 # Populates tensor with the value of 3
fours = twos ** 2 # Squares the values of the tensor
sqrt2s = twos ** 0.5 # Square root the values of the tensor
```


```python
powers2 = twos ** torch.tensor([[1, 2], [3, 4]]) # outputs tensor([[2., 4.], [8., 16.]])

fives = ones + fours # Does Matrix Addition

dozens = threes * fours # Does Matrix Multiplication
```


Tensors follow the same rules as [[Matrices]] so you cannot do arithmetic operations with 2 tensors which have different shapes (with the exception of tensor broadcasting)

## Tensor Broadcasting

The exception to the rule mentioned above is tensor broadcasting
## More Math With Tensors

Checkout https://pytorch.org/tutorials/beginner/introyt/tensors_deeper_tutorial.html#more-math-with-tensors for all the possible operations

