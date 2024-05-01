# Operations on Vectors

Resources:
- [[Info - Vectors in n-space]]

*Note:* These operations are the same as the ones we have defined for matrices.

---

## Vector Equality

![[definition-vector-equality.png]]

## Vector Addition

![[definition-vector-addition.png]]

## Scalar Multiplication

See above!

---

## Geometric Representations

These operations also have geometric interpretations!

## Vector Equality

Two vectors are equal if they refer to the same arrow or point in $\mathbb{R}^n$

### Vector Addition

Treating $u$ and $v$ as arrows in $\mathbb{R}^n$ whose tails are at the origin, their sum $u + v$ is obtained by... 

1. Repositioning $v$ so its tail is at the tip of $u$
2. Drawing the arrow from the origin to the tip of $v$

![[geometric-sum-of-vectors.png]]

Treating $u$ and $v$ as *arrows* in $\mathbb{R}^n$ whose tails are at the origin, their difference $u-v$ is obtained by...

Drawing the arrow starting from the tip of $v$ to the tip of $u$!

![[geometric-difference-of-vectors-arrows.png]]

Treating $u$ and $v$ as *points* in $\mathbb{R}^n$, their difference $u-v$ is obtained by...

Drawing the arrow from $v$ to $u$!

![[geometric-difference-of-vectors-points.png]]

Representing a single vector $u$ is the arrow formed by the difference $u-0$, when $u$ and $0$ are represented by points.

![[geometric-single-vector.png]]

### Scalar Multiplication

Multiplying a vector $v$ by a positive scalar $k \in \mathbb{R}$ results in a vector pointing in the same direction as $v$, but whose length is scaled by $k$.

![[geometric-multiplication-positive.png]]

If the scalar $k$ is negative, the vector is reflected across the origin, reversing its direction.

![[geometric-multiplication-negative.png]]

Other things to note:

- Two vectors are *parallel* if they are scalar multiples of each other.
- Two vectors point in the *same direction* if each is a positive scalar multiple of the other.
- Two vectors point in the *opposite direction* if each is a negative scalar multiple of the other.