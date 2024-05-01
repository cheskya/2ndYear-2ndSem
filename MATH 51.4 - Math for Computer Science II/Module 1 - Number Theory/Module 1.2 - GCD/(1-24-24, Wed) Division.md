*Related resources:*
- MATH 51.4 Onsite Lecture from January 24, 2024

```
lcm(a,b,c) {
	return lcm(a, lcm(b, c))
}

```

---

# Division Algorithm

## Theorem 1 - Division Algorithm
Let $a$ be an integer and $b$ be a positive integer. Then there are unique integers $q$ and $r$ with $0 \leq r < b$ such that $a=bq+r$
*Note:* $q=\lfloor\frac{a}{b}\rfloor$ and $r=a\pmod{b}$

## Corollary 1 - Modular Division and the Division Algorithm
Let $a$ be an integer and $b$ be a positive integer. Then $b|a$ if and only if $a\bmod{b}=0$

## Theorem 2 - Divisors of a Given Number
Let $n$ be a positive integer and $d$ be a divisor of $n$. Then at least one of $d$ and $\frac{n}{d}$ is less than or equal to $\sqrt{n}$.

## Definition 1 - Prime and Composite Numbers
An integer $p>1$ is called a *prime* if the only possible factors are 1 and $p$ itself. Otherwise, the integer is *composite*.
*Note:* Try searching for "Sieve of Erathostenes"!

## Definition 2 - Greatest Common Divisor (GCD)
Let $a$, $b$ be integers not both zero. The largest integer $d$ such that $d|a$ and $d|b$ is the *greatest common divisor* of $a$ and $b$, denoted by $gcd(a,b)$
*Note:* $a$ and $b$ cannot be both zero because you cannot find a greatest (will be infinite, therefore undefined)

*Examples:*
- $gcd(12,36)=12$
- $gcd(10,1)=1$
- $gcd(0,10)=10$

## Definition 3 - Relatively Prime
The integers $a$ and $b$ are *relatively prime* if $gcd(a,b)=1$.

## Definition 4 - Least Common Multiple (LCM)
The *least common multiple* of the positive integers $a$ and $b$ is the smallest integer that is divisible by both  $a$ and $b$, denoted by $lcm(a,b)$

*Examples:*
- $lcd(12,36)=36$
- $lcd(10,1)=10$

## Theorem 3 - Prime Factorization
Let the prime factorization of positive integers $a$ and $b$ be
$a=p_1^{a_1}p_2^{a_2}...$ and $b=p_1^{b_1}b_2^{b_2}...$

*Example:*
$15=2^03^15^17^011^0...$

Then,
$gcd(a,b)=p_1^{min(a_1,b_1)}p_2^{min(a_2,b_2)}...$ -> get the minimum
$lcm(a,b)=p_1^{max(a_1,b_1)}p_2^{max(a_2,b_2)}...$ -> get the maximum

*Example:*
$12=2^23^1$
$36=2^23^2$

$$
\begin{align*}
gcd(12,36)&=2^{min(2,2)}3^{min(1,2)}\\
&=2^23^1 \\
&=12 \\
\end{align*}
$$
$$
\begin{align*}
lcm(12,36)&=2^{max(2,2)}3^{max(1,2)}\\
&=2^23^2 \\
&=36 \\
\end{align*}
$$

## Theorem? - Product using GCD and LCM
$ab=gcd(a,b) \cdot lcm(a,b)$
(The product of two numbers is the product of their GCD and LCM.)

$gcd(a,b)=\frac{ab}{lcm(a,b)}$
$lcdm(a,b)=\frac{ab}{gcd(a,b)}$

## Theorem - Euclidean Algorithm (GCD without Prime Factorization)
Let $a$, $b$, be positive integers not both equal to 0.

Then,
$gcd(a,b)=gcd(b,a\bmod b)$

*Note:* The theorem is best used when $a\ge b$ (since modular division)
*Note:* You can move around the numbers inside the $gcd$ function! So you can keep reassigning $a$ and $b$ and reapplying the theorem (until you get two numbers whose GCD is obvious).

## Theorem - Diophantine Equation
Let $a$, $b$, $c$ be integers with $a$ and $b$ not both equal to zero. Then there exists a solution $(s,t)$ to $as+bt=c$ if and only if $gcd(a,b)|c$.

*Note:* If there is a solution, there are infinitely many of them.

