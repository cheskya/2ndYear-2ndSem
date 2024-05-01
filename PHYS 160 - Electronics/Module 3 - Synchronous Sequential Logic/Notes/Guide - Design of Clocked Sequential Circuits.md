# Design of Clocked Sequential Circuits

*Resources:*

- p. 236 of digital textbook
- Experiment 6 of PHYS 160
- [[Info - Storage Elements]]

The part of the design that follows a well-defined procedure is referred to as synthesis.

---

## Concepts

### Excitation Tables

Using an excitation table will be needed for flip-flops other than the D flip-flops, as these flip-flops' next states are derived from both the current state and input equations.

For example, the [[Guide - Design of Clocked Sequential Circuits#Using JK Flip-Flops|JK flip-flop]] and the [[Guide - Design of Clocked Sequential Circuits#Using T Flip-Flops|T flip-flop]] will need this.

An excitation table lists the required inputs for a given change of state.

![[excitation-tables.png]]

---

## General Procedure

1. From the word description and specifications of the desired operation, derive a state diagram for the circuit.
2. Reduce the number of states if necessary.
3. Assign binary values to the states.
4. Obtain the binary-coded state table.
5. Choose the type of flip-flops to be used.
6. Derive the simplified flip-flop input equations and output equations.
7. Draw the logic diagram.

---

### Using D Flip-Flops

From the state diagram created...

1. Create a table
	- The present states and inputs are in truth table format.

2. Find the equations
	- Create K-maps with the present states and inputs as the variables, and the next states and outputs as the values of the variables. (The next states and outputs should have separate K-maps.)
	- From here, find the simplified equations.

3. Create the circuit

---

### Using JK Flip-Flops

From the state diagram created...

1. Create a table
	- The present states and inputs are in truth table format.
	- Use the excitation tables to find the needed flip-flop inputs for the next states

2. Find the equations
	- Create K-maps with the present states and inputs as the variables, and the *flip-flop inputs* and outputs as the values of the variables. (The flip-flop inputs and outputs should have separate K-maps.)
	- From here, find the simplified equations.

3. Create the circuit

---

### Using T Flip-Flops

Same as [[Guide - Design of Clocked Sequential Circuits#Using JK Flip-Flops|JK flip-flops]].