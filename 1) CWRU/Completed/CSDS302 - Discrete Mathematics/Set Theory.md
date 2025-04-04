---
date: 12-19-2024
tags:
  - "#CSDS/Discrete"
  - CSDS
  - "#Math"
---
# Set Definition
## Sets
Sets are just groupings of elements. Not determined by order or repeat values. Sets can contain other sets
- EX:
	- A1 = {1,2,3}
	- A2 = {2,2,2,1,3}
	- Then A1= A2
		- A1 and A2 have the same unique elements so they represent the same set
Magnitude is how many unique elements there are. This notation is Cardinality! 
- |A2| = 3 because 3 unique elements
- Z
	- Set of all integers
	- |Z| = infinity
- Q
	- Set of rational numbers (fractions)
	- |Q| = infinity
- R
	- Set of real numbers (non imaginary)
	- |R| = Infinity
- |Z| = |Q| < |R|
## Property Base Form
- A = { Set | Condition(s) }  
- Ex:
	- A2 = { x 𝜖 Z | 1 < x < 3 }
	- A2. { 2 }
## Cartesian Products
One set X another set creates a coordinate system
- Ex:
	- A x B = { (a,b) | a 𝜖 A, b 𝜖 B }
	- | A x B | = m n |A| = m |B| = n 
## Subsets
- A is a Subset of B (A<B) if every x 𝜖 A, x 𝜖 B
- What is a Power Set?
	- P(A) = the set of all Subsets of A
	- EX.
		- A2 = {2,1}
		- P(A2) = { {2}, {1}, {1,2}, phi (empty) } 
	- |A| = n
	- |P(A)| = 2^n 
	- P(A) is made of n-bits, either set contains or does not contain each element in the set
## Null Set / Empty Set
$\phi$ is the empty set. $\phi$ is a subset of any set.
# Relations & Functions
## Relations
Def A and B are sets A relation R from A to B is a subset of AxB
- Ex
	- A = {1,2}         B = {1,2,3}
	- Define a relation R from A to B as(x,y) 𝜖 R of (x-y) / z 𝜖 R
	- R = { (1,1), (2,2), (1,3) }
## Functions
Definition of Function:
- Function F from A to B is a special relation
- 1) For every element x 𝜖 A there is always y 𝜖 B such that (x,y) 𝜖 R
- 2) For every element x 𝜖 A, y 𝜖 B, z 𝜖 B. If (x,y) 𝜖 F and (x,z) 𝜖 F then y = z
## Domain
Set of all possible inputs in the function / relation
## Co-domain
Set of all possible outputs in the function / relation
## Range
Set of all outputs in the function / relation
- Ex. A function’s co-domain could include 0 but if 0 is never an output to a specific function / relation, which would mean the range does not include 0 but the co-domain would include 0.
## Image 
The image is the output for a specific input
- For a function, the image is a value, but for relations the image could be a set of values
## Pre-image
The pre-image is a set of inputs that correspond to one output
## 1 to 1 functions
- Must follow all function rules
- Each input has only 1 unique output, meaning each output is different than other outputs
- |X| <= |Y|
## Onto functions
- Every y Y has a pre-image 
- Range of F = |Y|
- |X| >= |Y|
## Bijective function
both 1 to 1 and onto 
- |X| = |Y|
# Set Operations
## Union
Given 2 sets, $A,B$ the union of these sets is $A\cup B$ which is the unique set of elements in either $A$ or $B$. I am defining unique as no repeated elements.
## Intersection
Given 2 sets, $A,B$ the intersection of these sets is $A\cap B$ which is the unique set of elements in both $A$ and $B$.
## Complement
Given a set $A$ the complement of $A$ is denoted as $A'$ which refers to all elements not in $A$ but still part of the space. For example, let $A\in \mathbf N$ (natural numbers) and $A=\{1,2,3\}$. Then $A'=\{0,4,5,6,7,8,9,...\}$.
## Disjoint Sets
Given sets $A,B$, they are disjoint iff $A\cap B=\phi$ meaning they share no elements. 