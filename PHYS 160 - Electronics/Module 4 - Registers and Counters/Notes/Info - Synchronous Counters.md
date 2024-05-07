# Synchronous Counter

Resources:

- p. 271 of digital textbook (Chapter 6.4)
- [[Info - Counters]]
- [[Info - Ripple Counters]]

Biblically accurate circuits up ahead... dies

---

# Synchronous Counters

Synchronous counters are different from ripple counters in that clock pulses are applied to the inputs of all flip‐flops.

A common clock triggers all flip‐flops simultaneously, rather than one at a time in succession as in a ripple counter.

---

## Examples of Synchronous Counters

### Binary Counter

A flip-flop in any other position is complemented when all the bits in the lower significant positions are equal to 1.

e.g. if present state is 0011, next state is 0100, then 0101, then 0110, then 0111, then 1000... etc..

![[four-bit-synchronous-binary-counter.png]]

### Up-Down Binary Counter

A synchronous countdown binary counter goes through the binary states in reverse order, from 1111 down to 0000 and back to 1111 to repeat the count.

It is possible to design a countdown counter in the usual manner, but the result is predictable by inspection of the downward binary count.

The bit in the least significant position is complemented with each pulse. A bit in any other position is complemented if all lower significant bits are equal to 0.

A countdown binary counter can be constructed as shown below, except that the inputs to the AND gates must come from the complemented outputs, instead of the normal outputs, of the previous flip‐flops.

![[four-bit-synchronous-binary-counter.png]]

![[four-bit-up-down-binary-counter.png]]

### BCD Counter



### Binary Counter with Parallel Load