*Related resources:*
- MATH 51.4 Onsite Lecture from January 17, 2024
- https://eng.libretexts.org/Bookshelves/Computer_Science/Programming_and_Computation_Fundamentals/Mathematics_for_Computer_Science_(Lehman_Leighton_and_Meyer)/02%3A_Structures/08%3A_Number_Theory/8.01%3A_Divisibility

# Divisibility
*Note:* proofs have been left out for this one. try to find them on your own again :0
(i can't write all that here...)

---

## "d divides n"
### Definition
- If $d$ and $n$ are integers with $d\neq0$, we say that *$d$ divides $n$* if $\frac{n}{d}$ is an integer.
- Alternatively, *$d$ divides $n$* if there exists an integer $k$ such that $n=kd$.

$d|n$ -> d divides n
$d\not{|}n$ -> d does not divide n

### Theorem 1 - $d$ is greater than $n$
Let $d$ and $n$ be positive integers such that $d|n$. Then $d\leq n$.

### Theorem 2 - $d$ divides $m \pm n$
Let m, n. d be integers where $d\neq0$. If $d|m$ and $d|n$, then $d|(m\pm n)$.

### Theorem 3 - $d$ divides $tn$
Let n, d, be integers where $d\neq 0$. If $d|n$ then $d|tn$ for all integers $t$.

### Corollary 1 - $d$ divides $n^m$
If $d|n$, then $d|n^m$ for all positive integer $m$.

### Theorem 4 - $a$ divides $c$
Let a, b, c, be integers with $a\neq0$ and $b\neq0$. If $a|b$ and $b|c$ then $a|c$.

### Theorem 5 - $d$ divides $am + bn$
Let d, m, n be integers with $d\neq0$. If $d|m$ and $d|n$, then $d|(am+bn)$ for all integers $a$ and $b$.

### Theorem 6 -  $d$ divides $m + n$
Let m, n, d be integers where $d\neq0$. Suppose that $d|m$. Then $d|n$ if and only if $d|(m+n)$.

---

## "divisible by"
*Note:* Expand the number. e.g. 543 = 500 + 40 + 3

### Theorem 1 - Divisible by 2
A positive integer is divisible by 2 if and only if its last digit is divisible by 2.
*Note:* Remember that $2|10$ and $2|10^m$. e.g. 20 and 500 is divisible by 2.

### Theorem 2 - Divisible by 5
A positive integer is divisible by 5 if and only if its last digit is divisible by 5.

### Theorem 3 -  Divisible by 10
A positive integer is divisible by 10 if and only if its last digit is divisible by 10.

### Theorem 4 - Divisible by 4
A positive integer is divisible by 4 if and only if its last two digits is divisible by 4.
*Note:* Remember that $4|10^2$ and $4|10^k$ if $k\geq2$. e.g. 100 and 200 is divisible by 4.

### Theorem 5 - Divisible by $2^t$
A positive integer is divisible by $2^t$ (where $t$ is a positive integer) if and only if its last $t$ digits is divisible by $2^t$.

### Theorem 6 - Divisible by 3
A positive integer is divisible by 3 if and only if *the sum of its digits* is divisible by 3.

### Theorem 7 - Divisible by 6
A positive integer is divisible by 6 if and only if it *passes the divisibility tests* for 2 and 3.

### Theorem 8 -  Divisible by 7
(skip divisible by 7 first)

### Theorem 9 - Divisible by 11
A positive integer is divisible by 11 if and only if *the alternating sum of its digits* is divisible by 11.

---

## Exercises
1. Show that $11|(10^n-1)$ whenever $n$ is an even positive integer.
2. Show that $11|(10^n+1)$ whenever $n$ is an odd positive integer.