---
title: "C++"
---

I started learning C++ in my Senior Year of High School

I am going to be dedicating this notes page on how to do things I found "niche" to C++

## Lowercase/Uppercase a string

Normally you would have a function that does it all for you but noooooo not in C++

```cpp
    transform(input1.begin(), input1.end(), input1.begin(), [](unsigned char c) {return tolower(c);});
```

This will change the string input1 to all lowercase
