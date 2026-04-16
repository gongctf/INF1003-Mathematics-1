# Product and Sum Rules
## Product Rule
If there is a procedure that consists of 2 **independent tasks/sets**,
- There are m ways to do the first task while there are n ways to do the second task
- Therefore, there are mn ways to do the procedure.

Example:
- A new company with just two employees, Sanchez and Patel, rents a floor of a building with 12 offices. How many ways are there to assign different offices to these two employees?
	- 12 x 11 = 32

Example:
- How many different license plates can be made if each plate contains a sequence of 3 uppercase alphabets followed by 3 digits?
	- 26 x 26 x 26 x 10 x 10 x 10 = 17576000

## Sum Rule
If there is a procedure that consists of 2 **dependent tasks**,
- The procedure can be done either in 1 of m ways or in 1 of n ways, where the sets of ways are **mutually exclusive** 
- Then, there are m + n ways to do the procedure

## Examples
Variable Name:
```
In a version of the computer language BASIC, the name of a variable is a string of
one or two alphanumeric characters, where uppercase and lowercase letters are not distinguished. An alphanumeric character is either one of the 26 English letters or one of the 10 digits. Moreover, a variable name must begin with a letter and must be different from the five strings of two characters that are reserved for programming use.
```
How many different variable names are there in this version of BASIC?
- $V_{1}$: Number of variable names that are 1 character long = 26
- $V_{2}$: Number of variable names that are 2 characters long - 5 reserved keywords = 26 x 36 - 5
- 26 + 26 x 36 - 5

```
Each user on a computer system has a password, which is 6 characters long, where each character is an uppercase letter or a digit. Each password must contain at least 1 digit.
```
How many possible passwords are there?
- $V_{1}$: Total number of possible passwords of length 6 = 36<sup>6</sup>
- $V_{2}$: Total number of possible passwords using only uppercase letters = 26<sup>6</sup>
- $V_{3}$: Total number of possible passwords that must contain at least a digit = 36<sup>6</sup> - 26<sup>6</sup> 

Similarly, if we want to find the number of passwords with 6 to 8 characters long with the same specifications:
- $P_{6}$: 36<sup>6</sup> - 26<sup>6</sup> 
- $P_{7}$: 36<sup>7</sup> - 26<sup>7</sup> 
- $P_{8}$: 36<sup>8</sup> - 26<sup>8</sup> 
- Total number of passwords of varying lengths 6 to 8: (36<sup>6</sup> - 26<sup>6</sup>) + (36<sup>7</sup> - 26<sup>7</sup>) + (36<sup>8</sup> - 26<sup>8</sup>)

# Subtraction and Division Rules
## Subtraction Rule
If a task can be done either in one of m ways or n ways, then the number of ways to do the task is **m+n minus the number of ways to do the task that are common to the two different ways**.

Total ways = m + n - common ways

Example:
```
Find the total number of numerical strings of length 4 that start OR end with 0
```
Solution:
- $N_{1}$: Total strings that start with 0 = 10 x 10 x 10
- $N_{2}$: Total strings that end with 0 = 10 x 10 x 10
- $N_{3}$: Total strings that has 0 at start and end = 10 x 10
- $N_{4}$: Total number of strings that start with 0 OR end with 0 = 1000 + 1000 - 100 = 1900

## Division Rule
The division rule is used when we are finding the number of ways to do a task that can be done in n ways, but **some of the ways are equivalent or indistinguishable**. 

Example: Count the number of ways to arrange 4 books on a shelf, but book A and B are the same
- $A_{1}$: 4 unique books arranged in n ways: 4! = 4 x 3 x 2 x 1 = 24 ways
- $A_{2}$: 4 books arranged but A and B are the same book in n ways: 4! / 2 = 12 ways

General Formula:

$$
\frac{n}{d} = \frac{\text{number of ways to a task}}{\text{number of ways that are equivalent}}
$$

n = overall ways to do a task without considering equivalences or repetitions  
d = number of ways that are equivalent

---
# Permutations
A permutation of a set of distinct objects is an **ordered** arrangement of these objects
An ordered arrangement of r elements from a set is called an r-permutation

Example: 
- Let S = {1,2,3} be a set. The ordered arrangement (3,1,2) is a permutation of S. The ordered arrangement (3,2) is a 2-permutation of S

> [!NOTE] Notation
> The number of r-permutations of a set with n element is denoted by P(n,r)

### Formulas for permutations:
**First formula is used <font color="#00b0f0">when one has N ITEMS and ARRANGE R of them in a specific order</font>**

$$
P(n,r) = \frac{n!}{(n-r)!}=n(n-1)(n-2)\dots(n-r+1)
$$

- The numerator **n!** means multiplying a series of consecutive positive integers
- The denominator **(n-r)!** accounts for the fact that we are considering only r elements out of the total n elements, and it eliminates the possible arrangements of the remaining (n-r) elements. (aka division rule)

Special property:
- P(n, 0) = 1 whenever n is a non-negative integer, there is exactly 1 way to order 0 elements

**Second formula is when one has N ITEMS and <font color="#00b0f0">arrange ALL of them</font> in a specific order**:

$$
n!
$$

### Examples:
1. What are all the ways of arranging letters A, B, C, D?
	- In this case, we are choosing 4 out of 4 elements in the set, so we are looking at P(4,4)
	- 4!/(4-4)! = 4! = 24

2. How many ways are there to select 3 letters from a set of 6 letters without repetition? S = {A,B,C,D,E,F}
	- n = 6 (total number of letters in the set)
	- r = (number of letters to be selected)
	- P(6,3) = $\frac{6!}{(6-3)!}$
	- P(6,3) = 120

3. How many ways are there in choosing a relay team of 4 from a class of 30 students?
	- n = 30
	- r = 4
	- P(30,4) = $\frac{30!}{(30-4)!}$ = 657720

4. There are 8 runners, there are gold, silver and bronze medalists for the race, how many different possible ways are there to award these medals?
	- P(8,3) = $\frac{8!}{(8-3)!}$ = 336

5. How many permutations of the letters ABCDEFGH contain the string ABC?
	- We consider the block "ABC" as a single entity. This reduces the problem to finding the number of arrangements of only 6 objects
	- We use X to denote ABC, thus altogether, the set to find permutations is XDEFGH
	- 6 elements = 6! = 720
	- There are 720 permutations of the letters A to H, that contain the string ABC

# Combinations
The number of r-combinations of a set with n elements, where n is a non-negative integer and r is an integer with $0\le r \le n$:

$$
C(n,r)=\frac{n!}{r!(n-r)!}
$$

- n! is the number of ways that we can arrange n elements, if we care about the order
- r! means that when we divide by r! is to not care about the order of the r selected elements
- (n-r)! is so to consider r elements

Special Property:

$$
C(n,r) = C(n,n-r)
$$

### Examples
1. Find the number of possible ways to choose a pair of letters from the set {a,b,c,d}
	- C(4,2) = $\frac{4!}{2!(4-2)!}$ = 6

2. In poker, every player gets 5 cards from the deck of 52 cards, called a hand. How many different hands can be dealt?
	- C(52,5) = $\frac{52!}{5!(52-5)!}$ = 2598960
	- 
	- This would also work for selecting 47 cards from a standard deck of 52 cards, because of the special property
	- C(52,47) =  $\frac{52!}{47!(52-47)!}$ = 2598960

3. A group of 30 people have been trained as astronauts to go on the first mission to Mars. How many ways are there to select a crew of six people to go on this mission?
	- Use combination formula = 593775

4. If every crew member has a specific duty on board, how many ways are there to select the crew of 6 from the group of 30 people?
	- Use [[Combinatorics#Formula for permutations|Permutation Formula]] = 427518000

5. Suppose that there are 9 faculty members in the Engineering cluster and 11 in the ICT cluster. How many ways are there to select a committee to develop a programming module if the committee is to consist of 3 faculty members from the Engineering cluster and 4 from the ICT cluster?
	- C(9,3) x C(11,4) = $\frac{9!}{3!6!}$ x $\frac{11!}{4!7!}$ = 84 x 330 = 22720

# Pigeonhole Principle
### Theorem
If k+1 or more objects are placed into k boxes, then there is at least 1 box containing 2 or more objects

Worse Case Scenario Formula:

$$
k(m-1) = \text{Pigeons}
$$

k = pigeonholes
m = objects

### Examples
1. There's a bag with 30 blue and green socks. If you take out socks from without looking, how many socks do you need to draw, to ensure that you have a pair of socks of the same color
	- There are 2 colors
	- 2 colors = pigeonholes	
	- If we draw 3 socks, 2 of them are guaranteed to be in the same pigeonhole

2. Among any group of 367 people, there must be at least two with the same birthday, because there are only 366 possible birthdays.
	- 366 possible birthdays: pigeonholes
	- 367 people: pigeon

3. In any group of 27 English words, there must be at least two that be in with the same letter.
	- Pigeons: 26 alphabets
	- Pigeonholes: English words
	- The principle only guarantees that there will be at least 1 letter that will have more than 1 word starting with it

## Generalized Pigeonhole Principle
### Theorem
If N objects are placed into k boxes, then there is at least 1 box containing at least $\lceil N/k \rceil$ objects.

Ceiling function to round up integer
13 pigeons, 6 pigeonholes, $\lceil 13/6 \rceil$ = 3 : at least 1 hole has 3 objects

### Examples
1. Among 100 people, what is the maximum amount of people that were born in the same month.
	- Pigeons: 100 people
	- Pigeonhole: 12 months
	- $\left\lceil  \frac{100}{12} \right\rceil =9$ 

2. 6 computers on a network are connected to at least 1 other computer. Show there are at least two computers that have the same number of connections.
	- A computer can only have 5 possible number of connections
	- Pigeons: 6 computers
	- Pigeonhole: 5 connections
	- $\left\lceil  \frac{6}{5}  \right\rceil=2$
	- At least 2 computers have the same number of connections

3. How many cards must be selected from a standard deck of 52 cards to guarantee that at least three cards of the same suit are chosen?
	- There are 4 suits in a standard deck
	- Worst case scenario is having 2 cards of each suit: 2 * 4 = 8 cards then getting the next card guaranteeing the card
	- 8+1 = 9

4. How many students in a class must there to be to ensure that 6 students get the same grade if the grading system has the following possible grades: A, B, C, D, E, F
	- Pigeonhole: 5 different grades
	- Worst case scenario: 5 students each get 5 of the grades + 1
	- 5 * 5 + 1 = 26

5. Show that given any 5 points inside a square of side length 2, there is always a pair whose distance apart is at most $\sqrt{ 2 }$.
	- Pigeons: 5 points
	- Pigeonholes: split the grid into 4 quadrants
	- $\left\lceil  \frac{5}{4}  \right\rceil=2$
 
