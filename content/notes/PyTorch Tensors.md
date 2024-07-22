---
title: "PyTorch Tensors"
draft: true
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
```

Before using `torch.rand` it is common practice to use `torch.manual_seed` as this allows our results to be reproducible

## Tensor Shapes

When performing operations on two or more tensors they will need to be the same shape

`Tensor Shape` - Having the same number of dimensions and same number of cells in each dimension

```python

```
