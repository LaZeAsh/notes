---
title: "Lexicographical order"
draft: true
---

Learned Lexicographical Order while solving [[Codeforces]] Problem Petya and Strings 112A

Lexicographical Order is referred to as dictionary or alphabetical order of sorting sequences of items based on alphabetical order of their component letters. This is widely applied in Computer Science for sorting and organizing strings of characters.

## How it works?

1. Comparison goes from left to right
2. Order is determined by characters' positions in the alphabet (eg: 'a' comes before 'b' so 'apple' comes before 'banana')
3. If all the characters in the shorter sequence match the beginning of a longer sequence then the shorter sequence is considered smaller (eg: 'app' is less than 'apple') 
4. Some cases lowercase and uppercase are handled differently although this varies case by case (haha get it....)

