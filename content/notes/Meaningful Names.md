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

## Avoid Disinformation

- Avoid leaving false clues that obscure the meaning of the code
	- For example: hp, aix, and sco. These names represent unix platforms / variants which might provide misinformation
- Do not refer to things as a certain variable type if they are not that type
	- For example: do not refer to a grouping of accounts `accountList` unless it's actually a `List`
- Do not use names that vary in a small way
	- For example: XYZControllerForEfficientHandlingOfStrings and XYZControllerForEfficientStorageOfStrings, it takes too long to spot the difference between these names 
- `Information`: Spelling similar concepts similarly
- `Disinformation`: Using inconsistent spelling

> [!Awful Example of disinformative names] 
> The use of lowercase L or uppercase O especially as a combination

```java
int a = l; if ( O == l )

a=O1; else

l=01;
```

## Make Meaningful Distinctions

- Programmer's create problems for themselves when they write code solely to satisfy a compiler/interpreter
	- For example: Because you cannot use the same name to refer to 2 different things you might be tempted to change one name in an arbitrary way; Sometimes done by misspelling leading to compilation errors
	- Number series naming (a1, a2, .. aN) is the opposite of intentional naming
		- These names aren't disinformative but rather noninformative, they provide no clue to the author's intention
	- Noise words are another meaningless distinction
		- For example: `Product` , `ProductInfo`, and `ProductData` are different names but they don't mean anything different. `Info` and `Data` are distinct noise words like `a`, `an`, and `the`
	- 


