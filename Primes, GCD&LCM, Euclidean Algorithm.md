# Prime Numbers
are integers that have positive factors that are 1 and itself

Composite numbers are just the opposite

### Prime Factorization
Every integer greater than 1 can be expressed uniquely as a prime or as a product of two or more primes

Examples:
- 100 = 2 x 50 = 2 x 2 x 25 = 2 x 2 x 5 x 5 = 2<sup>2</sup> x 5<sup>2</sup>
- 999 = 3 x 333 = 3 x 3 x 111 = 3<sup>3</sup> x 37
- 1024 = 2 x 512 = 2<sup>10</sup>
- 1001 = 7 x 11 x 13

### Finding Primes easier using sqrt
If n is a composite number, then n has a prime factor $\le\sqrt{ n }$

Is 403 a prime?
- $\sqrt{ 403 }\approx$  20.07
- 403 = 13 x 31, no

Is 101 a prime?
- $\sqrt{ 101 }\approx$ 10.05
- Yes its prime

---
# Greatest Common Divisor & Least Common Multiple
## Greatest Common Divisor
is the largest integer that divides 2 integers aka the highest common factor

### Relatively Prime
The integers a and b are relatively prime if their GCD is 1

Factors of 10: 1, 2, 5, 10  
Factors of 17: 1, 17  
10 and 17 are relatively prime

We also say integers a, b and c are pairwise relatively prime when their GCD is 1

Factors of 10: 1, 2, 5, 10  
Factors of 17: 1, 17  
Factors of 21: 1, 3, 7, 21  
10, 17 and 21 are pairwise relatively prime

### GCD Prime Factorization Method
$$
gcd(a,b) = P_{1}^{min(a_{1},b_{1})} P_{2}^{min(a_{2},b_{2})} \dots P_{n}^{min(a_{n},b_{n})}
$$

Example: 
120 = 2<sup>3</sup> x 3 x 5  
500 = 2<sup>2</sup> x 3<sup>0</sup> x 5<sup>3</sup>  
GCD is taking the minimum powers of each number: 2<sup>2</sup> x 3<sup>0</sup> x 5<sup>1</sup> = 20

## Least Common Multiple
is the smallest positive integer that is divisible by both numbers a and b

$$
lcm(a,b) = P_{1}^{max(a_{1},b_{1})} P_{2}^{max(a_{2},b_{2})} \dots P_{n}^{max(a_{n},b_{n})}
$$

Example:  
12 = 2<sup>2</sup> x 3<sup>1</sup>  
18 = 2<sup>1</sup> x 3<sup>2</sup>  
LCM is taking the maximum powers of each number: 2<sup>2</sup> x 3<sup>2</sup> = 36

---
# Euclidean Algorithm
is an efficient method for computing the GCD of 2 integers

For any 2 integers a and b, if a = bq+r, then gcd(a,b) = gcd(b,r) and 0 $\le$ r $\le$ b.

Example: Find GCD of 287 and 91  
- 287 = 91 x q + r
- 287 = 91 x 3 + 14
- gcd(287, 91) = gcd(91,14)
- 91 = 14 x 6 + 7
- 14 = 7 x 2 + 0
- gcd(287, 91) = gcd(7,0) = 7

### Extended Euclidean Algorithm (Find values from coefficients)
$$
as + bt = gcd(a,b)
$$

Example: Express gcd(252,198) as 252s + 198t for some integers s and t
1. Find the GCD of 252 and 198
	 - 252 = 198 x 1 + 54
	 - 198 = 54 x 3 + 36
	 - 54 = 36 x 1 + 18
	 - 36 = 18 x 2 + 0
	 - gcd(252, 198) = 18
2. Goal: Find s and t such that 18 = 252s + 198t, rewrite previous equations (by making the **remainder LHS**)
	- 54 = 252 - 198 x 1
	- 36 = 198 - 54 x 3
	- 18 = 54 - 36 x 1
3. Solve 18 = 252s + 198t by subbing equations in
	- 18 = 252s + 198t
	- 18 = 54 - 36 x 1 
	- 18 = 54 - 1 x (198-54x3) 
	- 18 = 54 - 198 + 54 x 3
	- 18 = 4 x 54 - 1 x 198
	- 18 = 4 x (252-198x1) - 1 x 198
	- 18 = 4 x 252 - 198 x 4 - 1 x 198
	- 18 = 252 x 4 - 198 x 5
4. Compare equations, s = 4, t = -5    <--- **Watch for negative numbers**

Practice:
- gcd(1331, 1001)
	- 1331 = 1001 x 1 + 330
	- 1001 = 330 x 3 + 11
	- 330 = 11 x 30 + 0
	- 
	- 330 = 1331 - 1001 x 1
	- 11 = 1001 - 330 x 3
	- 
	- 11 = 1331s + 1001t
	- 11 = 1001 - (1331 - 1001 x 1) x 3
	- 11 = 1001 - 3 x 1331 + 3 x 1001
	- 11 = 1001 x 4 - 1331 x 3
	- s = -3, t = 4



