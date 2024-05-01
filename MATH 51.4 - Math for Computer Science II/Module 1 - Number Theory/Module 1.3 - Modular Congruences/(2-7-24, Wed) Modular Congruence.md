*Related resources:*
- MATH 51.4 Onsite Lecture from February 7, 2024.

---

## Linear Diophantine Equations
$ax+by=c$ has solutions if and only if $gcd(a,b)|c$

## Bezout's Theorem
$ax+by=gcd(a,b)$ has infinitely many solutions

## Definition 1
If $m|(a-b)$, then $a\equiv b \pmod n$

### Theorem 1
$a\equiv b\pmod n$ if and only if $a\pmod m = b \pmod m$

### Theorem 2
Given $a \equiv b \pmod m$ and $c \equiv d \pmod m$
- $a+c \equiv (b+d)\pmod m$
- $ac \equiv (bd)\pmod m$

## Definition 2 - Inverse
$aa^{-1}=a^{-1}a=1\pmod m$

### Theorem 3
$a^{-1} \pmod m$ exists if and only if $gcd(a,m)=1$ 

### Corollary 1
if $p$ is prime, then $\{1,2,...,p-1\}$ will have an inverse modulo $p$.

*Note:* These are equivalent...
- $x\equiv a^{01} \pmod m$
- $ax \equiv 1 \pmod m$
- $ax + my = 1$

These assume $gcd(a,m) = 1$. Otherwise, the three will not have a solution for $x$.

