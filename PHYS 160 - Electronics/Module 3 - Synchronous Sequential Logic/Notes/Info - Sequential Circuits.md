# Sequential Circuits

*Resources:*

- p. 190 of digital textbook
- Canvas modules

---

## Basics of Sequential Circuits

A sequential circuit consists of a [[Info - Design of Combinational Digital Circuits|combinational circuit]] to which [[Info - Storage Elements|storage elements]] are connected to form a feedback path.

The outputs in a sequential circuit are a function not only of the inputs, but the present state of the [[Info - Storage Elements|storage elements]] as well.

Thus, a sequential circuit is *specified by a time sequence of inputs, outputs, and internal states*.

![[sequential-circuit.png]]

---

## Types of Sequential Circuits

### Synchronous Sequential Circuit

Its behavior can be defined from the knowledge of its signals at *discrete instants of time*.

Synchronization is achieved by a timing device called the *clock generator*, which provides a clock signal having the form of a periodic train of *clock pulses*.

In practice, the clock pulses determine *when* computational activity will occur within the circuit, and other signals (external inputs and otherwise) determine *what* changes will take place affecting the storage elements and the outputs.

Synchronous sequential circuits that use clocks are called *clocked sequential circuits*. The storage elements used here are [[Info - Storage Elements#Flip-Flops|flip-flops]].

### Asynchronous Sequential Circuit

Its behavior depends upon the input signals at *any instant of time* and the *order in which the inputs change*.

Thus, it may be regarded as a combinational circuit with feedback. Because of the feedback among the logic gates, an asynchronous sequential circuit may become unstable at times