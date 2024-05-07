# Ripple Counters

Resources:

- p. 266 of digital textbook (Chapter 6.3)
- [[Info - Counters|Info - Counters]]
- [[Info - Synchronous Counters]]

---

## Ripple Counter



---

## Example of Ripple Counters

### Binary Ripple Counter

A binary ripple counter consists of a series connection of complementing flip‐flops, with the output of each flip‐flop connected to the C input of the next higher order flip‐flop.

The least significant bit, $A_0$, is complemented with each count pulse input.

Every time that $A_0$ goes from 1 to 0, it complements $A_1$. Every time $A_1$ goes from 1 to 0, it complements $A_2$. And so on...!

(NEGATIVE TRANSITION SIGNAL TO COUNT UPWARDS!!!)

![[binary-count-sequence.png]]

![[four-bit-binary-ripple-counter.png]]

A binary counter with a reverse count is called a *binary countdown counter*. In a countdown counter, the binary count is decremented by 1 with every input count pulse.

Every other bit besides the least significant bit ($A_0$) in the sequence is complemented if its previous least significant bit goes from 0 to 1

(POSITIVE TRANSITION STATE TO COUNT DOWNWARDS!!!)

### BCD Ripple Counter

Note: <https://www.electronics-tutorials.ws/binary/binary-coded-decimal.html>

The sequence of states in a decimal counter is dictated by the binary code used to represent a decimal digit.

A decimal counter is similar to a binary counter, except that the state after 1001 (the code for decimal digit 9) is 0000 (the code for decimal digit 0).

![[bcd-counter-state-diagram.png]]

![[bcd-ripple-counter.png]]

The four outputs are designated by the letter symbol Q, with a numeric subscript equal to the binary weight of the corresponding bit in the BCD code.

If the BCD counter counts from 0 to 9, it's a *decade* counter. To count in decimal from 0 to 99, we need a two‐decade counter. To count from 0 to 999, we need a three‐decade counter

Multiple decade counters can be constructed by connecting BCD counters in cascade, one for each decade.


![[three-decade-bcd-counter.png]]