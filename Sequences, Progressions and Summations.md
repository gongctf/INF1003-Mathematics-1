# Sequences
Sequence is an ordered list of elements with a pattern

### General Formula
represents a sequence by directly expressing how each term depends on its position.  
You can get a specified term's value **without calculating** other terms' values

### Recursive Formula
defines a sequence by showing how a term depends on previous term.  
You **have to calculate other terms' values** in order to get the specified term's value

---

# Progressions

### Arithmetic Progression
is a sequence with **first term a** and **common difference d**, and has its terms given by the formula

a<sub>n</sub> = a<sub>1</sub> + (n-1)d  
- a is the first term
- n is the term specified
- d is the common difference

#### Simple Interest
is a fixed interest every year calculated on the first year  
Arithmetic Progression Formula can be used to calculate the total principal after n amount of years

a = first term = 1000  
d = common difference = 5% of 1000 = 50  
a<sub>n</sub> = 1000 + (n-1)50

sub in n = 10 for after 10 years, it will be a<sub>10</sub> = 1450

### Geometric Progression
is a sequence of numbers in which **the ratio between consecutive terms remain constant** throughout the sequence

a<sub>n</sub> = ar<sup>n-1</sup>
- a is the first term
- n is the term specified
- r is the common ratio (multiplier or divider)

#### Compound Interest
is interest that is calculated on the previous year

End of n<sup>th</sup> year: $P(1+r)<sup>n</sup> 

---

# Summation
is the operation of adding a sequence of numbers together  
It is denoted by the symbol $\Sigma$ 

You can express the combined value or total of multiple terms in a concise manner. 

$$
\sum_{j=m}^{n}a_{j}=a_{m} +a_{m+1}+\dots+a_{n}
$$

where:  
j = index of summation  
m = lower limit  
n = upper limit


Example: summation of the series 1,2,3,4

$$
\sum_{n=1}^{4} n = 1+ 2 + 3+4=10
$$

Example: summation of series $\frac{1}{1}$+$\frac{1}{2}$+$\frac{1}{3}$ +$\dots$+$\frac{1}{100}$

$$
\sum_{j=1}^{100} \frac{1}{j} = \frac{1}{1} + \frac{1}{2} + \dots + \frac{1}{100}
$$

## Common Formulas for computing Sums

### Sum of the first n integers

$$
\sum_{k=1}^{n} k = 1 + 2 +3 + \dots + n = \frac{n(n+1)}{2}
$$

### Sum of the squares of the first n integers

$$
\sum_{k=1}^n k^2 = 1^2 + 2^2 + 3^2 + \dots + n^2 = \frac{n(n+1)(2n+1)}{6}
$$

$$
= \frac{1}{3}n^3+\frac{1}{2}n^2+\frac{1}{6}n
$$

## Special properties of Summation
### 1 element only

$$
\sum_{k=m}^m a_{k} = a_{m}
$$

Essentially, there's no need for addition operations, because its just 1 element

### Going reverse

$$
\sum_{k=m}^n a_{k} = \sum_{k=m}^{n-1} a_{k}+a_{n}=\sum^{n-2}_{k=m}a_{k} + a_{n-1}+a_{n}=\sum_{k=m}^{n-3}a_{k} +a_{n-2}+a_{n-1}+a_{n}
$$

$$
=a_{m}+a_{m+1}+a_{m+2}+a_{m+3}+\dots+a_{n}
$$

### Addition of 2 series of the same limits
If we want to compute the total sum of 2 series by adding them together **provided they share the same upper and lower limits**

$$
\sum_{k=m}^na_{k}+\sum_{k=m}^nb_{k}=\sum_{k=m}^n(a_{k}+b_{k})
$$
### Summation Multiplier
$$
\sum^n_{k=m}C.a_{k} = C.\sum^n_{k=m}a_{k}
$$
## Summation of an Arithmetic Sequence
$$
\sum_{i=0}^{n-1}(a_{1}+id)
$$

Formula:  
If you have the **common difference**,

$$
S_{n} = \frac{n(2a_{1}+(n-1)d)}{2}
$$

<font color="#ff00">If you have the **value of the last term**,</font>

$$
S_{n}=\frac{n(a_{1}+a_{n})}{2}
$$

Note: you can get the value of the last term by using [this formula](.md#Arithmetic%20Progression)

## Summation of Geometric Sequence
### Formula **(when the series has n terms, index starts from 1)**:
$$
S_{n} = \frac{a_{1}(r^n-1)}{r-1} = \sum_{i=1}^n ar^{i-1}
$$

$a_{1}$ = first term  
r = constant ratio where r =/ 1  
n = number of terms

###### Example: Series of n terms
$$
3 + 3(2) + 3(2)^2 + \dots + 3(2)^{n-1}
$$

$$
3(2) + 3(2)^2 + \dots + 3(2)^{n}
$$


### Formula **(when the series has n+1 terms, index starts from 0)**:
$$
S_{n+1} = \frac{a_{1}(r^{n+1}-1)}{r-1} = \sum^n_{i=0} ar^i
$$

###### Example: Series of n+1 terms
$$
2 + 2(2) + 2(2)^2 + \dots + 2(2)^n
$$

Explanation: You need to add 1 to n to account for 0 which is part of the number of terms

## Summation of an infinite sequence (geometric sequence)
Where -1 < r < 1

$$
\lim_{ n \to \infty } r^n = 0
$$

It means that when the value of n approaches infinity, the value of r<sup>n</sup> approaches zero  
Therefore, the sum of an infinite geometric sequence **where -1 < r < 1**:

$$
S_{\infty} = \lim_{ n \to \infty } \frac{a(1-r^{n-1})}{1-r} = \frac{a}{1-r} 
$$

$S_{\infty}$ = Sum of an infinite progression
a = first term
r - constant ratio where -1 < r < 1
