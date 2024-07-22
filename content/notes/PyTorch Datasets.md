---
title: "PyTorch Datasets"
draft: true
---

We want to decouple our dataset code from our model training code as processing data samples can get messy

PyTorch provides two data primitives: `torch,utils.data.DataLoader` and `torch.utils.data.Dataset` that allow you to use pre-loaded datasets as well as your own data.

- `Dataset` - stores the samples and their corresponding labels
- `Dataloader` - wraps an iterable around the `Dataset` to enable easy access to samples

## Loading a dataset

We're going to be loading a Fashion-MNIST (this is a dataset of Zalando's article images consisting of 60,000 training examples and 10,000 test examples) dataset from TorchVision

We can load the FashionMNIST Dataset with these parameters:
- `root` - path where train/test data is stored
- `train` - specifies training or test dataset
- `download=True` downloads the data from the internet if it's not available at root
- `transform` and `target_transform` specify the feature and label transformations

```python
import torch
from torch.utils.data import Dataset
from torchvision import datasets
from torchvision.transforms import ToTensor
import matplotlib.pyplot as plt


training_data = datasets.FashionMNIST(
    root="data",
    train=True,
    download=True,
    transform=ToTensor()
)

test_data = datasets.FashionMNIST(
    root="data",
    train=False,
    download=True,
    transform=ToTensor()
)
```
