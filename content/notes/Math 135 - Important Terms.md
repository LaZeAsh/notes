---
title: "Math 135 - Important Terms"
---

Important Terms for the course [[Math 135]] at the [[University of Waterloo]]

## Chapter 1

1. Sets - [[Set Notation]]
2. `Statement` - a sentence that has the definite state of being true or false
	1. 2 + 3 = 6 (false statement) | $\pi$ + 2 $\geq$ 5 (true statement)
	2. Does 7 = 5? (not a mathematical statement because you cannot assign true or false to it)
3. `Natural Numbers` denoted by $\mathbb{N}$ 
4. Set of `integers` where negative, positive, or zero are denoted by $\mathbb{Z}$
5. Set of `rational numbers` denoted by $\mathbb{Q}$ contains all the numbers of the form $\frac{a}{b}$ where a is an integer and b is a non-zero integer
6. Set of `real numbers` denoted by $\mathbb{R}$ contains all the numbers in decimal form
7. `Negation` - Finding the inverse meaning of a statement
	1. Suppose A is a true statement, $\neg$ A would be false
		1. $\neg$ ($\neg$ A) = A
8. `Quantified Statements` contains 4 parts:
	1. A quantifier
	2. A variable (any symbol representing a quantity or mathematical object)
	3. a domain (any set)
	4. an open sentence involving the variable
9. `Open Sentence` - A sentence that contains a variable, where the truth of the sentence is determined by the value of the variable chosen from the domain of the variable
10. `Quantifiers` - Describe "how many" elements of the domain are claimed to make the open sentence true
11. $\forall$ - Universal Quantifier
12. $\exists$ - Existential Quantifier
13. `Universally Quantified Statement` - $\forall$ x $\in$ S, P(x)
	1. This statement is read as "For all x in S, P(x) is true"
14. `Existentially Quantified Statement` - $\exists$ x $\in$ S, P(x)
	1. This statement is read as "There exists at least one value of x in S for which P(x) is true"
15. `Nested Quantifiers` - Quantifiers in a statement containing more than one quantifier
16. $\forall$ s $\in$ $\mathbb{R}$, $\exists$ t $\in$ $\mathbb{R}$, t > s
	1. For all real numbers s, there exists a real number t such that t > s
17. $\exists$ x $\in$ X, $\forall$ y $\in$ Y, $\exists$ z $\in$ Z, R(x,y,z)
	1. Can be rewritten as:
		1. $\exists$ x $\in$ X, P(x), where P(x) is $\forall$ y $\in$ Y, Q(x, y), where Q(x, y) is $\exists$ z $\in$ Z, R(x, y, z)

## Chapter 2

1. Negation is denoted by $\neg$ or the keyword "not" (Eg: $\neg$A / not A)
2. `Compound Statement` is a statement composed of several individual statements, each of which is called a `Component Statement`
3. A $\land$ B translates to A **and** B. This is similar to `and` statement in programming. Both A and B have to be true for A $\land$ B to be true
4. A $\lor$ B translates to A **or** B. This is similar to `or` statement in programming. Either A OR B have to be true for A $\lor$ B to be true
5. Brackets are important, they specify the order of operation
6. `De Morgan's Law (DML)`
	1. $\neg$ (A $\land$ B) $\equiv$ ($\neg$ A) $\lor$ ($\neg$ B)
	2. $\neg$ (A $\lor$ B) $\equiv$ ($\neg$ A) $\land$ ($\neg$ B)
7. Commutative Laws:
	1. A $\land$ B $\equiv$ B $\land$ A
	2. A $\lor$ B $\equiv$ B $\lor$ A
8. Associative Laws:
	1. A $\land$ (B $\land$ C) $\equiv$ (A $\land$ B) $\land$ C
	2. A $\lor$ (B $\lor$ C) $\equiv$ (A $\lor$ B) $\lor$ C
9. Distributive Laws:
	1. A $\land$ (B $\lor$ C) $\equiv$ (A $\land$ B) $\lor$ (A $\land$ C)
	2. A $\lor$ (B $\land$ C) $\equiv$ (A $\lor$ B) $\land$ (A $\lor$ C)
10. `Implication`:
	1. Format: A $\implies$ B
		1. Only false when A is true and B is false
		2. All other times true
11. Implication B $\implies$ A is called the `converse` of A $\implies$ B
12. Implication ($\neg$B) $\implies$ ($\neg$A) is called the `contrapositive` of A $\implies$ B
13. `If and only if (iff)` is represented by A $\iff$ B
	1. Only true when both A and B are same truth value (both have to be true or false)
	2. (A $\iff$ B) $\equiv$ ((A $\implies$ B) $\land$ (B $\implies$ A))

## Chapter 3

- We `prove` a statement when we demonstrate its true and the argument to do is called a `proof`
	- You can prove an inequality by proving all of it's constraints (eg: x $\leq$ 1 and x $\geq$ 3)
	- 
- We `disprove` a statement when we demonstrate it's false
	- To disprove a universally quantified statement find a counter-example. For example if the statement is true for all domains find a value for which it isn't
	- To disprove $\exists$ x $\in$ S, P(x) prove it's negation $\forall$ x $\in$ S, $\neg$P(x)
- When proving an identity we do **NOT** start by assuming the truth of that identity
- Be on the look out for `extraneous solutions` (solutions not in the domain created by acts such as rearranging the equation) 
- $\forall$ k $\in$ $\mathbb{Z}$, $\exists$ x $\in$ $\mathbb{R}$, x$^2$ + 2kx + k = 0 $\neq$ $\exists$ x $\in$ $\mathbb{R}$, $\forall$ k $\in$ $\mathbb{Z}$, x$^2$ + 2kx + k = 0
	- Changing the order of nested quantifiers can change the truth value of a quantified statement
- To prove the implication $\forall$ x $\in$ S, P(x) $\implies$ Q(x)
	- Assume x is an arbitrary element
	- Assume P(x) is true
	- Use that assumption to show Q(x) is true
- We assume an integer is even if it can be written as 2k (k = an integer). Otherwise an integer is written in the form 2k + 1 where we say the integer is odd
- 3 $\mid$ 6 exists since 6 = 3 * 2, exists an integer k such that 6 = 3k
- -3 $\mid$ 6 exists since 6 = (-3) * (-2), exists an integer k such that 6 = -3k
- 5 $\nmid$ 6 since no integer k exists so that 6 = k * 5
- For all integers a, a $\mid$ 0 $\because$ 0 = 0 * a
- For all non-zero integers a, a $\mid$ 0 since no integer k so that k * 0 = a
- For all integers b, 1 $\mid$ b since b can be written as b = b * 1 and -1 $\mid$ b since b can be written b = (-b) * (-1)
- `Transfer of Divisibility (TD)` - For all integers a, b, and c, if a $\mid$ b and b $\mid$ c, then a $\mid$ c
- `Proposition 8:` For all integers if a, b and c, if a $\mid$ b or a $\mid$ c, then a $\mid$ bc
	- If a $\mid$ b, then a $\mid$ bc
		- Assume a $\mid$ b, there exists an integer k so that b = ka. Substitute for b in product bc, we get
		- bc = (ka)c = kac = (kc)a
		- $\because$ kc is an integer we can conclude a $\mid$ bc
	- If a $\mid$ c, then a $\mid$ bc
		- Exists integer m so that c = ma. Substituting this equation we get
		- bc = b(ma) = bma = (bm)a
		- bm is an integer we conclude a $\mid$ bc
	- These proofs can be re-written as if a $\mid$ c, then a $\mid$ bc is similar, and is omitted
- `Divisibility of Integer Combinations (DIC)` - For all integers a, b and c, if a $\mid$ b and a $\mid$ c, then for all integers x and y, a $\mid$ (bx + cy)
- To prove an implication using contrapositive (A $\implies$ B) replace it with it's contrapositive ($\neg$B) $\implies$ ($\neg$A)
- Anytime we come across an argument claiming A and $\neg$A are true we say there must be a `contradiction` in the argument
- (A $\lor$ B $\implies$ C) $\equiv$ ((A $\implies$ C) $\land$ (B $\implies$ C))
- `Proof by Contradiction` - 


## Chapter 4

- `Properties of Summation (PS)`
	1. Multiplying by a constant
		- $\sum_{i=m}^{k} cx_{i}$ = c $\sum_{i=m}^{k} x_i$ (where c is constant)
	2. Adding two sums and subtracting two sums
		- $\sum_{i=m}^{k} x_i$ + $\sum_{i=m}^{k} y_i$ = $\sum_{i=m}^{k} (x_i + y_i)$
		- $\sum_{i=m}^{k} x_i$ - $\sum_{i=m}^{k} y_i$ = $\sum_{i=m}^{k}(x_i - y_i)$
	3. Change the bounds of the index of summation
		- $\sum_{i=m}^{k} x_i$ $\sum_{i=m+r}^{k+r} x_{i-r}$ 
	4. Breaking a sum apart
		- $\sum_{i=m}^{k} x_i$ = $\sum_{i=m}^{r} x_i$ + $\sum_{i=r+1}^{k} x_i$ 
- `Product Notation`
	- $\prod_{i=m}^{k} x_i$ = x$_m$x$_{m+1}$ $\dots$ x$_{k-1}$x$_k$
- `Axiom` is a statement that is assumed to be true. No proof given
- `Principle of Mathematical Induction (POMI)`
	- Let P(n) be an open sentence depends on n $\in$ $\mathbb{N}$
		- If statements 1 and 2 are both true:
			- P(1)
			- For all k $\in$ $\mathbb{N}$, if P(k), then P(k + 1)
		- then statement 3 is true:
			- For all n $\in$ $\mathbb{N}$, P(n)
- `Principle of Strong Induction (POSI)`
	- Let P(n) be an open sentence that depends on n $\in$ $\mathbb{N}$
	- If statements 1 and 2 are both true



## Chapter 5

- Number of elements in a finite set is called `cardinality` denoted by | S |
- `Universe of Discourse` $\mathcal{U}$ - contains all the objects we might encounter in a given situation
- {x $\in$ $\mathcal{U}$ : P(x)}
	- x is an element of $\mathcal{U}$
	- P(x) is true
- {f(x) : x $\in$ $\mathcal{U}$}
	- containing all objects of the form f(x) such that x is an element of $\mathcal{U}$
- {f(x) : x $\in$ $\mathcal{U}$, P(x)} or {f(x) : P(x), x $\in$ $\mathcal{U}$}
	- x is an element of $\mathcal{U}$
	- P(x) is true
- Union of two sets S and T written S $\cup$ T is the set of all elements belonging to either set S or set T(or both)
	- S $\cup$ T = {x: x $\in$ S OR x $\in$ T} = {x: (x $\in$ S) $\lor$ (x $\in$ T)}
- The intersection of two sets S and T, written S $\cap$ T is the set of all elements belonging to both set S and set T
	- S $\cap$ T = {x: x $\in$ S AND x $\in$ T} = {x: (x $\in$ S) $\land$ (x $\in$ T)}
- Set difference of two sets S and T is written as S - T (or S `\` T) is the set of all elements belonging to S but not T 
	- S - T = {x : x $\in$ S AND x $\in$ T} = {x : (x $\in$ S) $\land$ (x $\notin$ T)} = {x : (x $\in$ S) $\land$ ($\neg$(x $\in$ T))}
- Complement of set S, written $\overline{S}$ is set of all elements not in S
	- $\overline{S}$ = {x : x $\notin$ S}
- $\overline{S}$ = $\mathcal{U}$ - $\mathcal{S}$
	- $\overline{S}$ = $\mathcal{U}$ - $\mathcal{S}$ 

