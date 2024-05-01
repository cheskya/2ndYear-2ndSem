# Quick Outline

for Module 1

---

## Digital Systems and Binary Numbers

### Digital Systems

- digital systems have the ability to manipulate discrete elements of information represented internally in binary form
- a binary digit (called a bit) has either the value 1 or 0
- discrete elements of information are represented with groups of bit called binary codes

### Binary Numbers

- a number expressed in a base-$r$ system is like this: $a_nr^n+a_{n-1}r^{n-1}+...$
- to convert from binary to decimal, add only the numbers with powers of two corresponding to the bits with value 1 e.g. $(10)_2 = 2^1 + 0 = (2)_2$
- to add, subtract, or multiply binary numbers, it's just the same (take note of the allowable digits e.g. 1 + 1 = 10, 1 + 1 + 1 = 11)

### Number-Base Conversions

- for decimal to binary
	- keep dividing number and its quotients by 2
	- if remainder 1, multiple that power of 2
	- if remainder 0, leave out that power of 2
	- go from bottom to top (backtrack) to get the value
	- ARCHUR IF YOU ARE READING THIS IT'S BASICALLY EUCLIDEAN!!
- for decimal to any base-r system
	- same as binary, except replace 2 with r
	- if decimal, same as binary, except multiply and go from top to bottom

### Octal and Hexadecimal Numbers

- for binary to octal
	- group bits into 3's
	- get the octal digit for each group
	- put the digits together
- for binary to hexadecimal
	- group bits into 4's
	- get the hexadecimal digit for each group
	- put the digits together
- most computer manuals use either octal or hexadecimal numbers to specify binary quantities

### Complements of Numbers

- complements are used to simplify the subtraction operation and for logical manipulation
- the complement of the complement restores the number to its original value
- radix complement
	- AKA $r$'s complement (e.g. 10's complement in decimal)
	- defined as $r^n-N$ for $N \neq 0$ and as $0$ for $N = 0$, where $r$ is the base, $n$ is the number of digits, and $N$ is the number
	- easier technique: adding 1 to the $(r-1)$'s complement
- diminished radix complement
	- AKA $(r-1)$'s complement (e.g. 9's complement in decimal)
	- defined as $(r^n-1)-N$ where $r$ is the base, $n$ is the number of digits, and $N$ is the number
	- easier technique: subtracting each digit from $(r-1)$
		![[easy-9-complement.png]]
	- even easier technique (for binary): flip each digit
		 ![[easy-1-complement.png]]
- subtraction with complements	
	- using (r-1)'s complement
		![[sub-2.png]]
	- using r's complement
		![[sub-with-complements.png]]
		![[example-sub-2-complement.png]]
		

### Signed Binary Numbers

- signed-magnitude convention
	- consists of a magnitude and a symbol (+ or -) or a bit (0 or 1) indicating the sign
	- negates a number by changing its sign
- signed-complement conversion
	- negates a number by changing its complement
- possible representations of a negative number in binary
	- signed-magnitude
		- only flip the sign bit in the leftmost position of the original positive number
	- signed-1's-complement representation
		- take the 1's complement of the original positive number
	- signed-2's-complement representation
		- take the 2's complement of the original positive number

![[signed-binary-numbers.png]]

arithmetic addition

- using signed binary numbers with negative represented in signed-2's-complement form
	- add like usual
	- discard the carry out of the sign-bit position
	- note: the negative sums will automatically be in signed-2's-complement form

![[signed-complement-addition.png]]

arithmetic subtraction

- using signed binary numbers with negative represented in signed-2's-complement form
	- take the 2's complement of the subtrahend (including the sign bit)
	- add this to minuend (including the sign bit)
	- discard the carry out of the sign-bit position

![[signed-complement-subtraction.png]]

### Binary Codes

- n-bit binary code
	- group of n bits that assumes up to $2^n$ distinct combos of 0's and 1's, with each ombo representing one element of the set that is being coded
	- BCD
		- binary-coded decimal
		- each group of 4 bits representing one decimal digit
		- binary combos 1010 through 1111 are not used and have no meaning in BCD

![[bcd-chart.png]]

BCD addition

- add the BCDs like you would decimal digits
- for carries
	- add 0110 to get the desired BCD and a carry

![[bcd-unsigned-addition.png]]

Decimal Arithmetic

(confused look at this later)

Other Decimal Codes

- weighted code
	- each bit position is assigned a weighting factor in such a way that each digit can be evaluated by adding the weights of all the 1's in the coded combo

Gray Code

ASCII Character Code

### Binary Code

yeah

---

## Boolean Algebra and Logic

### Introduction

### Basic Definitions

### Axiomatic Definition of Boolean Algebra

### Basic Theorems and Properties of Boolean Algebra

![[postulates-theorems-boolean-algebra.png]]

(proof in textbook)

Operator Precedence

1. Parentheses
2. NOT (')
3. AND (·)
4. OR (+)

### Boolean Functions

- there is only one way for a Boolean function to be represented in a truth table
- but when the function is in algebraic form, it can be expressed in a variety of ways (all of which have equivalent logic)

Complement of the Function

- MY procedure
	- basically just NOT the whole expression
	- keep applying De Morgan's law until simplified

![[complement-function.png]]

- another simple procedure
	- take the dual of the function (interchange of AND and OR operator and 1's and 0's)
	- complement each literal

![[complement-function-dual.png]]

### Canonical and Standard Forms

minterms

- those that give the 1's in a truth table
- sum of minterms
- 

maxterms