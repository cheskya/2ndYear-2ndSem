# Module 1.2 - Quick Outline
## Greatest Common Divisor
- definition of the greatest common divisor (gcd) *(9.4.1)*
	- biggest number (max) divisible by a and b
- relatively prime if gcd is 1 *(9.4.2)*
- definition of the least common multiple (lcm) *(9.4.3)*
	- smallest number (min) divisible by a and b
- prime factorization *(9.4.4)*
	- if gcd, get the minimum prime factors
	- if lcm, get the maximum prime factors
- a times b is equal to gcd(a,b) times lcm(a,b) *(9.4.5)*
- connection between lcm and gcm *(9.4.6)*
- gcd and lcm operations are commutative and associative *(9.4.7)*
- extension of gcd and lcm to accept an arbitary number of arguments *(9.4.8)*
- recursiveness of gcd and lcm functions *(9.4.9)*

## The Euclidean Algorithm
*note:* the euclidean algorithm is an efficient method for computing gcd without prime factorization
- gcd(a,b) is equal to gcd(b, a mod b) *(9.5.1)*
- euclidean algo's gcd is correct for integer non-zero inputs a and b *(9.5.2)*
- euclidean algo's running time is O(log min(a,b)) *(9.5.3)*

## GCD as Linear Combinations
*note:* equations in which we are only interested in integer solutions are called diophantine equations
- there exists infinitely many integer solutions to as+bt=c iff gcd(a,b)|c *(9.6.1)*
- there exists infinitely many integer solutions to as + bt = gcd(a,b) (bezout's theorem) *(9.6.2)*

## Extended Euclidean Algorithm
*note:* this is a more systematic and efficient method of solving
- extension of the euclidean algorithm *(9.7.1)*
- extension is correct and runs in O(log min(a,b)) *(9.7.2)*
- general approach to enumerating the entire solution set for two variables *(9.7.3)*
- general approach to enumerating the entire solution set for three variables *(9.7.4)*
- 