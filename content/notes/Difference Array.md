---
title: "Difference Array"
draft: true
---

Youtube Video Link: https://www.youtube.com/watch?v=R-PBfqsRGP0

Similar concept to [[Prefix Sum Array]]

## How it works

Difference Array works similar to Prefix Sum Array as in instead it depends on the previous element value to determine the value.

It has an initial value (which is not modified) and rest of the proceeding values are the different of the current value and the previous value

Python code implementation:

```python
arr = [5, 9, 4, 7, 10]

for i in range(len(arr) - 1, 0, -1):
	arr[i] = arr[i] - arr[i - 1]
```

Let's trace it out:

```
Pseudocode

arr = [5, 9, 4, 7, 10]

arr[4] = arr[4] - arr[3]

[5, 9, 4, 7, 3]

arr[3] = arr[3] - arr[2]

[5, 9, 4, 3, 3]

arr[2] = arr[2] - arr[1]

[5, 9, -5, 3, 3]

arr[1] = arr[1] - arr[0]

[5, 4, -5, 3, 3]

END

The reason we end at arr[1] is because we want our first value to stay consistent. This process of converting the array into a difference array is O(n) but any operations we might want to do with the array is O(1)
```

## Difference Array Operations

Lets say you have an array of x number of cash piles. You want to add money to y cash piles from a certain range.

Doing this each time without a difference array is O(n) time complexity but using a difference array makes it O(1) time complexity

Formulas: 
- `arr[first_index] += change_value`
- `arr[last_index + 1] -= change_value`

```
arr = [5, 9, 4, 7, 10] # This is our cash pile with each number representing how many dollars are in that pile

Lets say I want to add 5 dollars to piles in index 1 to 3

Result: [5, 14, 9, 12, 10]

Code Implementation (Python):

for i in range(1, 4):
	arr[i] += 5

This is inefficient compared to utilizing a difference sum array

Difference sum array: [5, 4, -5, 3, 3]

Add 5 to the first index you want to add the money to and remove 5 from the (last index + 1) you want to add the money to

[5, 9, -5, 3, -2]

If you reverse the logic and go back to a normal array you get

[5, 14, 9, 12, 10]

The 2 solutions match, therefore this method works
```

