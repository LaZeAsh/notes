---
title: "PyTorch Tensors"
---

Tensors are the center of everything we do in PyTorch.

Source: https://pytorch.org/tutorials/beginner/introyt/tensors_deeper_tutorial.html
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

If you run the code:

```python
rand = torch.rand(2, 4)
doubled = rand * (torch.ones(1, 4) * 2)
```

The code will not run into errors, but how?

In the example above the one-row, four column tensor is multiplied by both rows of the two-row, four column tensor

Rules for broadcasting are:
- Each tensor must have at least one dimension - no empty tensors
- One of the dimensions must be of size 1, or
- The dimension does not exist in one of the tensors
## More Math With Tensors

Checkout https://pytorch.org/tutorials/beginner/introyt/tensors_deeper_tutorial.html#more-math-with-tensors for all the possible operations

## Copying Tensors

Assigning a tensor to a variables makes the variable a label of the tensor, and does not copy it.

If you want a separate copy of the data to work on, use the `clone()` method

```python
a = torch.ones(2, 2)
b = a.clone()
```

even though `a` and `b` are different objects in memory they have the same contents

> [!Autograd]
> When using `clone()` if your source tensor has autograd enabled then so will the clone

## Manipulating Tensor Shapes

One case where you might need to change the number of dimensions is when passing a single instance of input to your model. PyTorch models generally expect batches of input

```python
a = torch.rand(3, 226, 226)
b = a.unsqueeze(0)
```

The `unsqueeze()` method adds a dimension of extent 1. `unsqueeze(0)` adds it as a new zeroth dimension

By unsqueezing we're taking advantage of the fact that any dimension of extent 1 does not change the number of elements in a tensor

```python
c = torch.rand(1, 1, 1, 1, 1)
print(c)

# Ouput: tensor([[[[[0.2347]]]]])
```

On the other hand if you want to do some non-batched computation what you can do is use `squeeze()`

```python
a = torch.ones(1, 20)
# a = tensor([[1., 1., 1.]]) and so on until 20

b = a.squeeze(0)
# b = tensor([1., 1. 1.]) and so on until 20
```


`squeeze()` and `unsqueeze()` can only act on dimensions of extent 1 because otherwise you would change the number of elements in a tensor

there are also `squeeze_()` and `unsqueeze_()` the difference between these and the original function is that `squeeze()` and `unsqueeze()` return a new tensor but `squeeze_()` and `unsqueeze_()` modify the existing tensor


When you want to change the shape of a tensor more drastically and want to preserve the number of elements and their contents you can use the `reshape()` method. This reshape method will result in an output tensor of shape features x width x height but in 1-dimension.

Example:

```python
output3d = torch.rand(6, 20, 20)

input1d = output3d.reshape(6 * 20 * 20)
```

the `input1d` is a 1 dimensional input which has 2400 elements

`reshape()` will return a view on the tensor to be changed (separate tensor object looking at the same underlying region of memory) unless you run `clone()` on it

## NumPy Bridge

If you have existing ML/Scientific Code with data stored in NumPy ndarrays and you want to express the same data as PyTorch tensors its easy to switch between ndarrays and PyTorch tensors

```python
import numpy as np

numpy_array = np.ones((2, 3))

pytorch_tensor = torch.from_numpy(numpy_array)
```

PyTorch creates a tensor of same shape and containing the same data as the NumPy array, going as far as to keep the default 64-bit float data type

Conversion can also go the other way

```python
pytorch_rand = torch.rand(2, 3)

numpy_rand = pytorch_rand.numpy()
```

> [!Memory]
> The converted objects are using the same underlying memory the change to one are reflected in the other.


