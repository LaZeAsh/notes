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

## Creating a Custom Dataset

```python
import os
import pandas as pd
from torchvision.io import read_image

class CustomImageDataset(Dataset):
    def __init__(self, annotations_file, img_dir, transform=None, target_transform=None):
        self.img_labels = pd.read_csv(annotations_file)
        self.img_dir = img_dir
        self.transform = transform
        self.target_transform = target_transform

    def __len__(self):
        return len(self.img_labels)

    def __getitem__(self, idx):
        img_path = os.path.join(self.img_dir, self.img_labels.iloc[idx, 0])
        image = read_image(img_path)
        label = self.img_labels.iloc[idx, 1]
        if self.transform:
            image = self.transform(image)
        if self.target_transform:
            label = self.target_transform(label)
        return image, label
```

Breaking down what happens in this function

### \_\_init__

`__init__` function is run once when initializing the Dataset object. We initialize the directory containing the images, the annotations file, and both transforms

### \_\_len__

`__len__` function returns the number of samples in our dataset

### \_\_getitem__

`__getitem__` function returns a sample dataset at the given index `idx`

Based on the index it identifies image's location on the disk, converts it to tensor using `read_image` retrieves the corresponding label from the csv data in `self.img_labels`, calls the transform functions on them, and returns the image and corresponding label in a tuple


## Preparing your data for training




