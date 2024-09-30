---
title: "Recursion"
---

Recursion occurs when a function calls itself.

2 Rules of Recursion:
- Must have a base case
- Must make progress toward that base case

Example of Recursion (Factorial Implementation):

```C
#include <stdio.h>  
#include <assert.h>  
  
int factorial(unsigned int n)  {  
 if (n == 0) // Base case  
	 return 1;  
 else  
	 return n * factorial(n - 1);  
}  
  
int main(void) {  
    assert(factorial(0) == 1);  
    assert(factorial(1) == 1);  
	assert(factorial(6) == 720);  
}  
```

