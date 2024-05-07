# Counters

Resources:

- p. 255 of digital textbook
- [[Info - Ripple Counters]]
- [[Info - Synchronous Counters]]

---

## Counter

A register that goes through a prescribed sequence of states upon the application of input pulses is called a counter.

A counter that follows the binary number sequence is called a binary counter.

An $n$-bit binary counter consists of $n$ flip-flops and can count in binary from 0 through $2^n-1$.

Counters are available in two categories: ripple counters and synchronous counters.

- In a ripple counter, a flip-flop output transition serves as a source for triggering other flip‐flops. (The C input of some or all flip-flops are triggered NOT by common clock pulses BUT by the transition that occurs in other flip-flop outputs.) (So, asynchronous!)
- In a synchronous counter, the C inputs of all flip‐flops receive the common clock.

*Note:* C input here means CLK!
