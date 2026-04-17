# Direct Proof
Direct Proof Approach:
- $p\implies q$
- Assume that p is true. Use rules of inference, axioms and logical equivalences to show that q must also be true

Example: "Prove that the sum of 2 rational numbers is rational"
- Rational numbers are rational if it can be expressed in fraction
- Rational = 1/9
- Irrational = $\sqrt{ 2 } \text{ or }\pi$
Every x and y are rational then x + y is also rational.
- ^ We modify it into the form of p implies q. To prove this statement of this structure, we assume that p is true.
	- **Assume** x and y are rational, show x+y is rational

| Step                                                                                                                                                | Reason                                                                                                                      |
| --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| 1. x and y are rational                                                                                                                             | Assuming p                                                                                                                  |
| 2. $\exists p_{1},p_{2},q_{1},q_{2}\left( x=\frac{p_{1}}{q_{1}}\wedge y=\frac{p_{2}}{q_{2}} \right)$                                                | By definition (We know that rational number can be represented as a ratio between 2 integers) (Can write it in English too) |
| 3. x+y = p1/q1 + p2/q2                                                                                                                              | By (2)                                                                                                                      |
| 4. x+y = (p1q2 + p2q1)/(q1q2)                                                                                                                       | By (3)                                                                                                                      |
| 5. Let<br>$p_{3} = p_{1}\cdot q_{2} + p_{2} \cdot q_{1}$<br>and<br>$q_{3} = q_{1}\cdot q_{2}$<br><br>$p_{3}\text{ and } q_{3} \text{ are integers}$ | We know that 2 integers multiplied or added together are integers                                                           |
| 6. x+y = p3/q3                                                                                                                                      | By (4) and (5)                                                                                                              |

Example: "If n is an odd integer, then n squared is also odd."  
Hint: We define that an integer n is odd, if there exists another integer, m, such that n=2m+1

# Indirect Proof
Establish the truth of an implication by proving its contrapositive statement
- $\neg q\implies \neg p$

Example: Prove that n is an integer and 3n + 2 is odd, then n is odd.
- p: n is an integer and 3n + 2 is odd
- q: n is odd
- Contrapositive: $\neg q\implies \neg p$
- $\neg q$: n is even
- $\neg p$ 3n+2 is even

| Step                                     | Reason                                                                                      |
| ---------------------------------------- | ------------------------------------------------------------------------------------------- |
| 1. n = 2k where k is an integer          | Premise. n is even so anything multiplied by 2 will be even                                 |
| 2. 3(2k)+2 = 6k + 2                      | From (1)                                                                                    |
| 3. 6k+2 = 2(3k + 1)                      | From (2) Factorise 2 out                                                                    |
| 4. Let m be 3k + 1 where m is an integer | Because multiplication of 3 and addition of 1 of an integer will still result in an integer |
| 5. 2(3k+1) = 2m                          | From (3) and (4)                                                                            |
| 6. 3n+2 = 2m                             | From (5)                                                                                    |
| 7. 3n+2 is not odd                       | From (6)                                                                                    |
By the contraposition rule, we have proven that if n is an integer and 3n+2 is odd, then n is odd.

# Trivial & Vacuous Proof
## Trivial proof
If we know q is true, then $p\implies q$ is true as well.
- ![[{D2EE38E5-0B3D-422E-A436-8B2042E49203}.png]]

Example: The statement "If I watch a movie tonight, the sun will shine tomorrow"
- $p\implies q$
- We know that the sun shines every day, so this statement is true regardless of whether I watch a movie or not. 
- **The implication is true** because q is true. 
- The statement is true.

Example: "Show that for every real number x, if x>0 then x<sup>2</sup> + 2x +2 > 0"

| Step                                                                                  | Reason                           |
| ------------------------------------------------------------------------------------- | -------------------------------- |
| 1. <br>x<sup>2</sup>+2x+2<br>=(x<sup>2</sup>+2x+1) +1<br>=(x+1)<sup>2</sup>+1<br><br> | Simplification of the expression |
| 2. (x+1)<sup>2</sup> $\ge$ 0                                                          | Every squared number is positive |
| 3. (x+1)<sup>2</sup> + 1$\gt$ 0                                                       | From (2)                         |
| 4. (x<sup>2</sup>+2x+2) > 0 is True for every x                                       | From (1) and (3)                 |
| 5. "if x>0 then x<sup>2</sup> +2x+2 > 0" is True                                      | Trivial Proof                    |

## Vacuous Proof
To prove that $p\implies q$ is True, show that p is False.
- ![[{1569592E-C421-445D-A9F8-7EBED4932C16}.png]]

Example: "Show that if $x^2 + 4x + 5 \le 0 \text{ then }x\le 0$"

| Step                                                           | Reason                                          |
| -------------------------------------------------------------- | ----------------------------------------------- |
| 1.<br>$x^2 + 4x + 5$<br>=$(x^2 + 4x + 4) +1$<br>=$(x+2)^2 + 1$ | Simplification of expression                    |
| 2. $(x+2)^2 + 1 \gt 0$                                         | From (1) & every squared number + 1 is positive |
| 3. $x^2 + 4x + 5 \gt 0$                                        | From (2)                                        |
| 4. $x^2 + 4x + 5 \le 0$ is False                               | From (3)                                        |
| 5. "if $x^2 + 4x + 5 \le 0 \text{ then }x\le 0$" is True       | Vacuous Proof                                   |

# Proof by Contradiction
To prove p, assume $\neg p$ and derive a contradiction such as $p\wedge \neg p$
- $\neg p = False$
- $\neg(\neg p)=\neg False=True$
- p = True

It is a method of proving the truth of a statement by **assuming that the statement is false** and showing that this assumption **leads to a logical contradiction.**

Example: 
- Prove that there is no smallest positive rational number
	1. Let's assume that there is a smallest positive rational number $r=\frac{p}{q}$
	2. We introduce a new rational and positive number $s=\frac{p}{2q}$, s is smaller than r and it is rational and positive.
	3. We arrived at a contradiction, so r cannot exist. (Because r cannot be the smallest positive, rational number)
	4. There is no smallest positive rational number.

Example: Statement: $p\implies q$ 
- Proof contradiction by assuming $\neg(p\implies q)$
- $\neg(p\implies q)\equiv(p\wedge \neg q)$
- Goal: show this assumption leads to a contradiction

# Counterexamples
A specific case that **contradicts a general statement** or rule
- Demonstrates that the statement fails to hold universally

Applies only to general statements:
- All dogs have tails
- All men are mortal

Example: "All birds can fly."
- We need to provide a counterexample of a bird that cannot fly
- Counterexample: A penguin is a bird that cannot fly

Example:
- Show that the statement "Every positive integer is the sum of the squares of 2 integers" is false
	1. Let's consider the number 3
	2. The squares not exceeding 3 are 0<sup>2</sup> = 0 and 1<sup>2</sup> = 1
	3. Evaluating the possible combinations
		- 0<sup>2</sup> + 0<sup>2</sup> = 0, 0<sup>2</sup> + 1<sup>2</sup> = 1, 1<sup>2</sup> + 1<sup>2</sup> = 2
	4. Thus, we observe that 3 cannot be expressed as the sum of squares of 2 integers.

# Exhaustive Proof
Some theorems cannot be proven with just 1 argument.

Show that the statement is true based on the findings for each case, leaving no room for exceptions.
- **All possible values or conditions of the statement must be considered**, demonstrate that the statement holds true based on the findings for each and every case. 
- This approach is only suitable for statements that apply to a limited number of objects. 
	- Examines every single possibility, ensuring that the statement holds true universally.

Example: Prove that (n+1)<sup>3</sup> $\ge$ 3<sup>n</sup> if n is a positive integer with n $\le$ 4.
Solution: we only have to verify the inequality for n=1;2;3 and 4
- Case 1: For n = 1, (1+1)$^3$ = 2$^3$ = 8 > 3$^1$ = 3
- Case 2: For n = 2, (2+1)$^3$ = 27, 27 > 3$^2$ 
- Case 3, For n = 3, (3+1)$^3$ = 64, 64 > 3$^3$ 
- Case 4, For n = 4, (4+1)$^3$ = 125, 125 > 3$^4$
- We conclude that the statement "(n+1)<sup>3</sup> $\ge$ 3<sup>n</sup> if n is a positive integer with n $\le$ 4" is proven exhaustively.

# Proof by Cases
Similar to Exhaustive Proof, we divide the statement into distinct cases and prove each case separately.
- This approach focuses groups of objects or conditions within the statement, proving each one separately.
- Each group may be finite or infinite.

Example: Prove that if $\text{a and b}$ are real numbers, and $b \ne 0$ then $\frac{|a|}{|b|} = |\frac{a}{b}|$
- Think of either a or b can be positive or negative. Cover all 4 possibilities
- Case 1 (a>=0 and b>0): 
	- |a| = a, |b| = b
	- $\frac{a}{b}\ge 0$, so $|\frac{a}{b}| = \frac{a}{b}$
	- Hence $\frac{|a|}{|b|} = \frac{a}{b} = |\frac{a}{b}|$.
- Case 2 (a>=0 and b<0):
	- |a| = a and |b| = −b (since b < 0).
	- a/b ≤ 0, so |a/b| = −a/b = a/(−b).
	- Hence |a|/|b| = a/(−b) = |a/b|.
- Case 3 (a<0 and b>0):  
	- |a| = −a and |b| = b.
	- a/b < 0, so |a/b| = −a/b = (−a)/b.
	- Hence |a|/|b| = (−a)/b = |a/b|.
- Case 3 (a<0 and b<0):  
	- |a| = −a and |b| = −b.
	- a/b > 0, so |a/b| = a/b.
	- Hence |a|/|b| = (−a)/(−b) = a/b = |a/b|.
- In all cases $\frac{|a|}{|b|} = |\frac{a}{b}|$.

Example: Let's consider the statement: "For any real number x, x$^2 \ge 0$"
- Case 1: $x\ge 0$ If we squared a positive number or zero, the result will always be positive.
- Case 2: $x\lt 0$ If we squared a negative number, the result will always be positive.
- These both cases cover every possible instance or object that needs to be considered, so proving the two cases shows that the statement hold for any real number.

# Existence Proof
Many theorems are assertions that objects of a particular type exist.
- Such as propositions expressed in the form $\exists xP(x)$
- "There is a largest natural number"
- "There is a student that was born in Japan"

To prove such statements, we can use constructive and non-constructive approaches.
- In a constructive proof, we find an actual example of an object that makes the statement true
- In a non-constructive proof, we don't find such an example, but we show logically that such an example must exist.

## Constructive Existence Proof
Find an explicit value of c, for which P(c) is true.  
Then, $\exists xP(x)$ is true by Existential Generalisation (EG)

Example: "Show there is a positive integer that can be written as the sum of cubes of positive integers in 2 different ways"
- We look for a number n,a,b,c,d such that for some

$$
\begin{gathered}
n = a^3 +b^3 = c^3 + d^3\\
1729 = 10^3+9^3 = 12^3+1^3
\end{gathered}
$$

## Non-constructive Existence Proof
In non-constructive proof, we establish the existence of an element, denoted as 'c', without explicitly determining its value. We know that it must exist.

We can achieve this by employing proof of contradiction. We assume that no such element exists and then arrive at a contradiction.

Example: "Proof that there is a prime number greater than 3"

|         Constructive Approach         |                                                                                                                                                Non-Constructive Approach                                                                                                                                                |
| :-----------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| 5 is a prime number<br>greater than 3 | 1. Suppose there is no prime number greater than 3<br>2. Then the only prime numbers are 2 and 3<br>3. We should be able to represent any other number as a product of powers of 2 and 3<br>4. 25 cannot be represented as a product of powers of 2 and 3.<br>5. Therefore there must be at least 1 other prime number. |

# Uniqueness Proof
Some theorems claim the existence of a singular element possessing a specific property.
- Meaning there is **precisely 1 element exhibiting this property**
- "There is exactly 1 student in class that was born in Japan"

Consists of 2 components:
- An element x with the desired property exists. This shows only the existence part of the proof.
- If there is another element y with the same property, then y=x. This shows the uniqueness part of the proof.

Example: "Show that if a and b are real numbers, a =/ 0, then there is a unique real number r such that ar + b = 0"
- Existence: $r=-\frac{b}{a}$ solves the equation
- Uniqueness: Suppose there is s, such that as + b = 0
- $ar+b=0\to ar+b=as+b\implies r=s$
- $as+b=0\to r=s$
- We assumed another number s that meets the requirement and realised it must be the same as r. Therefore, this number r is indeed unique.
