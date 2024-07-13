---
title: "Meaningful Names"
---

Notes of Chapter 2 of Clean Code

## Intention-Revealing Name

- Choosing good names takes time but saves more than it takes
- Name of a variable, function, or class should all answer big questions.
	- Why it exists?
	- What it does?
	- How it's used?
- If the name requires a comment then the name does not reveal it's intent
	- Bad name example:
		- int d;
	- Good name example:
		- int elapsedTimeInDays; 
		- int daysSinceCreation; 
		- int daysSinceModification; 
		- int fileAgeInDays;


Let's analyze this code block

```java
public List<int[]> getThem() {  
List<int[]> list1 = new ArrayList<int[]>(); 
for (int[] x : theList)
	if (x[0] == 4) list1.add(x);
return list1;
}
```

This code is reasonably written with good spacing and indentations, so why is this code so hard to read? 

Because, the context is not explicit in the code itself. 

`Code Implicity` requires answers to questions such as:
1. What kind of things are in `theList`
2. What is the significance of the zeroth subscript of an item in `theList`
3. What is the significance of the value 4
4. How would I use the list being returned

Let's say we're working on a minesweeper game we can make these changes to make the code more explicit
- Board is a list of cells called `theList`, rename that to `gameBoard`
- When iterating through the board we know that we're iterating through cells of the board, rename `x` to `cell`
- zeroth subscript of a cell is the location of status value, define a variable `STATUS_VALUE` that equals to 0
- value 4 means flagged, define a variable `FLAGGED` that equals to 4

Updated improved code

```java
public List<int[]> getFlaggedCells() {  
List<int[]> flaggedCells = new ArrayList<int[]>(); 

for (int[] cell : gameBoard)
	if (cell[STATUS_VALUE] == FLAGGED) 
		flaggedCells.add(cell);
return flaggedCells; }
```

The complexity of the code has not changed, although the code has become more explicit

