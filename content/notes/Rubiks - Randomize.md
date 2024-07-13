---
title: "Rubiks - Randomize"
---

In this program I want to be able to randomize my rubiks cube so I am figuring out different approaches to do that.

## RNG

My original plan was to make an algorithm that will loop through the number of individual cubes (54) in the rubiks cube and assign each of them a color value and ensuring each color is only limited to 9.

This however wouldn't work, this cube needs to be able to be solved if I randomly assign values there's a 91% chance that the cube will be unsolvable. 

## Turns

Other viable option is to take the base cube and perform a random number of moves on it to randomize the cube enough.

This seems to be the most reasonable, although it'll require me to make algorithms to be able to turn the cube.
