# State Reduction and Assignment

*Resources:*

- p. 231 of digital textbook

The problem of state reduction is to find ways of reducing the number of states in a sequential circuit without altering the input-output relationships.

However, the fact that a state table has been reduced to fewer states does not guarantee a saving in the number of flip-flops or the number of gates.

In actual practice designers may skip this step because target devices are rich in resources.

---

## State Reduction

### General Procedure

1. State diagram
2. State table
3. Find equivalent states, merge them

### Algorithms

Two states are said to be equivalent if, for each member of the set of inputs, they give exactly the same output and send the circuit either to the same state or to an equivalent state.

(When two states are equivalent, one of them can be removed without altering the input-output relationships.)

---

## State Assignment

In order to design a sequential circuit with physical components, it is necessary to assign

unique coded binary values to the states.

For a circuit with $m$ states, the codes must contain $n$ bits, where $2^n\geq m$. (*Note:* It is different for one-hot encoding, since the number of bits is equal to the number of states.) 

- Gray code makes it easier for the Boolean functions to be placed in the map for simplification
- One-hot encoding usually leads to simpler decoding logic for the next state and output

![[state-assignment.png]]