 # Yes
etc

---

## Matrices
- an array of numbers
- denoted by $A=\left[a_{ij}\right]$
	- where $i$ is the row position
	- where $j$ is the column position

![[matrix-example.png | 300]]
![[matrix-example-2.png]]

We say that $A$ is an $m \times n$ matrix (where $m \times n$ is the size).
Also, $A \in \mathbb{R}^{m \times n}$

**Examples (for matrices):**
{to put pictures of board later}
{there are 2}

**Notes:**
- a row vector is a matrix with one row
- a column vector is a matrix with one column
- two matrices $A$ and $B$ are equal to each other if they have the same size and $a_{ij}=b_{ij}$ for all $i$, $j$
- let $A$ and $B$ be matrices of the same size. then, $A + B = \left[a_{ij}+b_{ij}\right]$

**Examples again (for notes about matrices):**
{to put pictures of board later}
{there is 1}

---

## Linear Systems
A linear system in $n$ variables $x_1,x_2,...,x_n$ is given in the form...
$a_1x_1+a_2x_2+...+a_nx_n = b$

**Notes:**
- $a_i$'s are called coefficients
- $a_i$'s and $b$ are constant
- $a_1$ is the leading coefficient
- $x_1$ is the leading variable
- the $n$-tuple ($s_1,s_2,...,s_n$) is a solution to a linear system if $a_1s_1+a_2s_2+...+a_ns_n = b$
- a linear equation can be expressed as a row matrix using the equation's coefficients
	- $a_1x_1+a_2x_2+...+a_nx_n = b$ becomes...
	- $\left[a_1,a_2,...,a_n\right]$ and $\left[b\right]$

---

## Matrix Product
### Scalar Product
$cA = \left[c \cdot a_{ij} \right]$

![[scalar-product-example.png|300]]

### Matrix-Vector Product
![[matrix-vector-product-example.png]]

*Note:* the $n$ in size $m \times n$ of the matrix, and the $n$ in size $n \times 1$ of the column vector, must be EQUAL in value for a vector product to be possible (consequently, the size of the resulting matrix will be $m \times 1$)

**Examples:**

### Matrix-Matrix Product
![[matrix-matrix-product-example.png]]

*note:* the $n$ in size $m \times n$ of the first matrix, and the $m$ in size $m \times n$ of the second matrix, must be EQUAL in value for a matrix product to be possible (consequently, the size of the resulting matrix will be $m \times n$, where $m$ is from the first matrix and $n$ is from the second matrix)


---

## Linear Systems and Matrices (Augmented)
(augmented because we're gonna add the right side of the equation to the matrix)

*Operations we can do:*
- interchange rows
- multiply a row by a constant (non-zero)
- add a multiple of one row to another row

By doing these operations, we can find a solution to a system of equations.

THEREFORE...
- we can find the solution to a system of equations using just matrices!
- using matrices makes this easier to code!! yay!

{pictures of board to add later}

The goal is to end up with a matrix like this:
![[matrix-system-of-equations-example.png|300]]

--- 

### Gaussian Elimination
