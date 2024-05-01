# Analysis of Clocked Sequential Circuits

*Resources:*

- p. 204 of digital textbook
- Experiment 6 of PHYS 160
- [[Info - Storage Elements]]

---

## Concepts 

### State Equations

The behavior of a clocked sequential circuit can be described algebraically by means of state equations.

A state equation (aka transition equation) specifies the next state as a function of the present states and inputs.

$A(t+1)$ is A in the next state.

$A(t)$ is A in the current state.

![[state-equation-example.png]]

### State Table

A state table (aka transition table) is where inputs, outputs, and flip-flop states can be enumerated.

![[state-table-example.png]]

### State Diagram

A state diagram can be used to represent the information in a state table graphically.

![[state-diagram-example.png]]

---

## General Procedure

1. Circuit diagram
2. Equations
3. State table
4. State diagram
5. Explanation

----

### Using D Flip-Flops

Same as [[Guide - Analysis of Clocked Sequential Circuits#General Procedure|general procedure]].

---

### Using JK Flip-Flops

The next-state values can be derived as follows:

1. Determine the flip-flop input equations in terms of the present state and input variables.
	- You really need to just figure it out from the circuit.
2. List the binary values of each input equation.
3. Use the corresponding flip-flop characteristic table to determine the next-state values in the state table.

![[jk-flip-flop-analysis.png]]

flip-flop input equations (using present states and inputs) -> next states

---

### Using T Flip-Flops

Same as [[Guide - Analysis of Clocked Sequential Circuits#Using JK Flip-Flops|JK flip-flops]].

---

## Sequential Circuit Models

They differ only in the way the output is generated.

The two models of a sequential circuit are commonly referred to as a finite state machine, abbreviated as FSM.

![[mealy-moore.png]]

### Mealy Model

AKA Mealy FSM or Mealy Machine.

The output is a function of both the present state and the input.

The output is the value that is present immediately before the active edge of the clock.

### Moore Model

AKA Moore FSM or Moore Machine.

The output is a function of only the present state.

The outputs are *synchronized with the clock*, because they depend only on flip-flop outputs that are synchronized on the clock.