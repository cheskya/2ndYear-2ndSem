# Module 1.1 - Quick Outline
## Divisibility and Divisibility Tests
- definition of divisibility *(9.1.1)*
	- $d|n$, and $n=kd$
	- d divides n
	- d is a factor of n
	- d is a divisor of n
	- n is a multiple of d
	- n is divisible by d
- since d divides n, d is less than or equal to n *(9.1.2)*
- properties
	- addition and subtraction *(9.1.3)*
	- multiplication (and division ig) *(9.1.4)*
	- transitivity *(9.1.5)*
	- linear combination (addition and multiplication rules combined) *(9.1.6)*
	- stronger addition *(9.1.7)*
- divisibility tests
	- divisible by 2
		- if last digit is divisible by 2
		- same with divisible by 4, 8, and $2^n$ (if last $n$ digits are divisible by $2^n$)
	- divisible by 5
		- if last digit is divisible by 5
		- same with divisible by 10 (if last digit is divisible by 10)
	- divisible by 3
		- if the sum of its digit is divisible by 3
	- divisible by 6
		- if it passes the divisibility tests for 2 and 3

*Note:* What is NOT true is if a divides n and b divides n, then ab divides n (See GCD)

## The Division Algorithm
- division algorithm (or division theorem) *(9.2.1)*
	- $a,b$, and $a=bq+r$
	- also, $q=\lfloor\frac{a}{b}\rfloor$
	- also, $r=a\mod b$
	- a is the dividend
	- b is the divisor
	- q is the quotient
	- r is the remainder
- to check if divisible, check if remainder is 0 *(9.2.2)*