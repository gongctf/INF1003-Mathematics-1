# Predicates
Predicate Logic is a formal system for reasoning about statements that involve objects and their properties.
- It is an extension of propositional logic
- Allows more reasoning with complex statements

Some examples include:
- All dogs have 4 legs.
- Every bird can fly.
- All men are mortal.
- Some students are hard-working.

Example #1:
- p = "There is a student in the class that has red hair"
- Can define a function called Red(x)
	- This function takes a name of a person as an input
	- Then, returns True or False if the person has red hair or not
	- This is called a **predicate**
- Allowed to use the function to write Red(Alice), Red(Bob), Red(Claire)
	- These are predicates
	- Can attach the property of having red hair to different objects

## Notation
$$
L(x): \text{x is a lecturer}
$$

L(x): A propositional function
- Applying the predicate to a variable.
- It <font color="#00b0f0">becomes a proposition when a specific value</font> is assigned to x.
L: A predicate
- Properties of the objects in the form of a general function
x: A variable
- Represent objects from a group (e.g. the group of all people)

## Variables
are associated with a specific domain or set of objects.  
This domain will determine the range of values that a variable can take on.
- Can sometimes be referred to as the universe and often indicated with the letter U.

Problem:
- The definition of Red(x): x has red hair, x was meant to represent students in the class, or maybe it can be from the domain of all people, or all mammals?
- Therefore, there is a need to clearly define the domain of the variable.

Example:
$L(x): \text{x is a lecturer}$
- L is the predicate
- If John is an actual lecturer and Jenny is not a lecturer
	- Then, the proposition L(John) is True
	- The proposition L(Jenny) is False
Let P(x) denote "x>0" and the domain be the integers
- The function will evaluate true or false whether the number is positive
	- The predicate assigns the property of being greater than 0
- If x is -3, the statement evaluates to false
- If x is 0, the statement evaluates to false
- If x is 3, the statement evaluates to true.
Let "x+y=z" be denoted by R(x,y,z) and U, the domain if all 3 variables is integers.
- Find the truth values of R(2,1,1)
	- Substitute the corresponding values
	- $2+1=1$ is false
	- Therefore R(2,1,1) is False

## Compound Expressions
Connectives from propositional logic work the same. $\wedge\& \vee$

However, when a variable is present in a expression, the expressions are not propositions.

Example:
If P(x) denotes "x > 0", find the truth values of the following:
- P(3)$\vee$P(-1) = $T\vee F$ = True
- P(3)$\wedge$P(-1) = $T\wedge F$ = False

# Quantifiers
specify the scope of the variables.
## Notation
Example:

$$
Red(x)
$$

means student x has red hair

### Universal Quantifier
$$
\forall ~ x ~ Red(x)
$$

means every student has red hair
- $\forall$ this symbol represents "for all" or "every"
- It asserts that a statement **is true for all possible values of that variable**
- This expression is a **proposition**, true if all student have red hair, false if at least 1 student does not have red hair

### Existential Quantifier
$$
\exists ~ x ~ Red(x)
$$

means some students have red hair
- $\exists$ this symbol represents "there is" or "exists"
- It assert that there **exists at least 1 value for the variable that makes the statement true**
- Expression is also a proposition

Example:
Py(x): x knows Python & C(x): x knows C  
x is from the domain of all the students in our class
- $\forall~x~Py(x)$: All students know Python
- $\exists ~x~Py(x)$: There are students that know Python
- $\exists x(Py(x)\wedge C(x))$: There are students that know Python and C
- $\forall x(\neg Py(x)\wedge C(x))$: No student knows Python, but all of them knows C

## The Universal Quantifier
U specifies the domain  
It is important to consider the definition of the predicate and the domain when evaluating a quantified expression.  
Example:
- $P(x): x>0$  where U = All integers
	- $\forall x ~P(x) = False$
- $P(x): x>0$  where U = All positive integers
	- $\forall x ~P(x) = True$
- $P(x): \text{x is even}$  where U = All integers
	- $\forall x ~P(x) = False$

### To refute a universal quantification proposition
Must find a counterexample by identifying a value of x that makes P(x) is false

Example:  
Let Q(x) be the statement "x is less than 2" What is the truth value of the quantification $\forall x Q(x)$ where U = All real numbers.
- Find a counterexample for value x where x > 2
- Substitute x = 3 into the statement. The truth value is false
- Since, there exists at least 1 real number in this case, the proposition is false.

Example:  
Suppose that P(x) is "x<sup>2</sup> > 0". Show that the statement $\forall xP(x)$ is false where the universe of disclosure consists of all integers
- Find a counterexample for value x
- If x = 0, x<sup>2</sup> = 0 $\ngtr$ 0
- Since, the counterexample demonstrates that the statement is false, can conclude that the proposition is false.

Example:  
What is the truth value of $\forall x(x^2 \ge x)$ is, if the domain consists of all real numbers?
- If x is 0.5, 0.5<sup>2</sup> = 0.25 $\ngeq$ 0.5
- The statement is false

## The Existential Quantifier
U specified the domain

Example:
- $P(x): x>0$ where U = All integers
	- $\exists xP(x) = True$
- $P(x):x<0$ where U = All positive integers
	- $\exists xP(x) = False$


## Negating Quantified Expression
### Negation of Universal Quantifiers
Example:  
Original Statement: "Every cat in the world is friendly"  
Negated Statement:
1.  "It is not the case that every cat in the world is friendly"
2.  "There is some cat in the world that is not friendly"

Notation:  
Domain: All cats in the world  
Predicate P(x): "x is friendly"  
- $\forall xP(x)$ - Original
- $\neg \forall xP(x)$ - Negated from 1.
- $\exists x(\neg P(x))$ - Negated from 2.
$\neg \forall xP(x) \equiv \exists x(\neg P(x))$ 

Example:
$\forall xPy(x)$ : Every student in your class has taken a course in Python
- Domain: all students in your class
- Predicate Py(x): "x has take a course in Python"
Negation:
- $\neg \forall xPy(x)$: It is not the case that every student in your class has taken a course in Python
- $\exists x(\neg Py(x))$: There is at least a student in your class who has not take a course in Python


### Negation of Existential Quantifiers
Example:  
$\exists xP(x)$: "There exists a student in your class who has taken a course in Python"
- Domain: all students in your class
- Predicate: P(x): "x has taken a course in Python"
Negation:
- $\neg\exists xP(x)$: It is not the case that there exists a student in your class who has taken a course in Python
- $\forall x\neg P(x)$: For all students in your class, it is not true that they have taken a course in Python
$\neg \exists xP(x) \equiv \forall x\neg P(x)$

## Nested Quantifiers
Example: "Every real number has an inverse"  
- Can formalise this by using and introducing variables that can help formulate.
- $\forall x\exists y(x+y=0)$ where the domains of x and y are real numbers
- For every x, there is a y, such that x + y = 0
Another way to formalise:
- Q(x,y) : x+y=0
- $\forall x\exists yQ(x,y)$
- where the domains of x and y are the real numbers

### Quantification of 2 variables
![[{E8C86E7F-CD20-42CD-B423-0D167D6C6168}.png]]
#### Both quantifiers are universal
Example: $\forall x\forall y((x>0)\wedge(y<0)\implies(x.y<0))$ 
- Write this in English
- "For every two numbers, if 1 of them is positive and the other is negative, then their product is always negative"
- This statement is True because if x is positive and y is negative then product will be negative

Example: $\forall x\forall y(x\ge_{}0)\wedge(y\lt_{0})\implies(x.y<0)$
- Think of a counter example that state that this statement is not correct.
- x=0, y=-8
- In this case, x >= 0 and y<0 are both true, and the statement $x.y$ < 0 is false, contradicting the implication. Therefor, this is an example where the statement is false.

#### 1 universal & 1 existential quantifier
Example: $\forall x\exists y\left( \frac{x}{y}=1 \right)$
- "For all value of x, there exists a value y that x/y = 1"
- Find a counterexample to make the statement false
- x=0, y=1

Example: $\exists x\forall yP(x,y)$ where P(x,y): y<sup>x</sup> = 1
- "There is a value of x so that P(x,y) is true for every value of y."
- Find an example to make the statement true.
- x = 0

#### Both quantifiers are existential
Example: $\exists x\exists y(x+y=5)$
- Statement is true because x can be 3, y can be 2

Example: $\exists x\exists y\left( x \neq y \wedge \frac{x}{y} = 1 \right)$ 
- Statement is false because any value of x and y will not satisfy this proposition

## Translating Nested Quantifiers
Example: Translate the statement $\forall x(C(x)\vee \exists y(C(y)\wedge F(x,y))$ where the domain for x and y is students at SIT
- C(x) = "x has a computer"
- F(x, y) = "x and y are friends"
	- "Every SIT student has a computer or has a friend that has a computer"





