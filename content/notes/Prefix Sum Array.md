---
title: "Prefix Sum Array"
---

[[Ching Lam Lau]] recommended I check out this algorithm for P1 on Back to School'24

Youtube Video with better explanation: https://youtu.be/pVS3yhlzrlQ?si=52-DprxwwiG1Xtn0
## How it works

Normal Array: \[6, 3, -2, 4, -1, 0, -5]

Prefix Sum Array: \[6, 9, 7, 11, 10, 10, 5]

O(1) time complexity

Pseudocode of how prefix sum array works:
```
Let x represent an index of the array

When x > 0:

array[x] = array[x-1] + array[x]
```

`Note: Prefix Sum Array is modifying the same array not making a new one`
## Why is it special?

1. If you are told to calculate the sum of the first 5 elements of the original array then using the prefix sum array you can grab the 4th element of the array (since arrays are 0 indexed) which will give you the sum of the first 5 elements of the array

Going back to our original example 

Normal Array: \[6, 3, -2, 4, -1, 0, -5]

Prefix Sum Array: \[6, 9, 7, 11, 10, 10, 5]

4th element of prefix sum array = 10

Calculating the normal way: 6 + 3 - 2 + 4 - 1 = 10

WOWWWWW they match


2. Prefix Sum Arrays aren't only used to find the sum of the first x integers... You can also use them to find the sum of integers in a range like 2 to 6

We don't have the sum calculated of 2 to 6 but we have the sum calculated of 0 to 6 using the previous method we calculated

Sum of 2 to 6 = 6th element of prefix sum array - (2 - 1) element of prefix sum array

5 - 9 = -4

Formula to find sum of low range and high range: prefix_sum_array\[high_range] - prefix_sum_array\[low_range - 1]
