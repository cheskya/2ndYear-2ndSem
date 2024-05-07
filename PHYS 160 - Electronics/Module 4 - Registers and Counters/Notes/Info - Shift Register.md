# Shift Register

Resources:

- p. 258 of digital textbook (Chapter 6.2)

"When we do problems we'll start from the basic structure and build from there." - Sir Bennett

---

## Shift Registers

A Shift Register is a group of flip flops used to store multiple bits of data. It is capable of shifting the binary information held in each cell to its neighboring cell, in a selected direction.

The logical configuration of a shift register consists of a chain of flip‐flops in cascade, with the output of one flip‐flop connected to the input of the next flip‐flop. All flip‐flops receive common clock pulses, which activate the shift of data from one stage to the next.

- The serial input determines what goes into the leftmost flip-flop during the shift.
- The serial output is taken from the output of the rightmost flip-flop

### Application

Shift registers are often used to interface digital systems situated remotely from each other.

e.g. Since it is more economical to use a single line and transmit the information serially (one bit at a time), then we can use a shift register to accept the data in parallel, across the common line. Then another shift register can get the data serially, then taken out in parallel.

---

## Transfer of Data in Shift Registers

### Serial Transfer (Serial Mode)

Information is transferred one bit at a time by shifting the bits out of the source register and into the destination register.

In the serial mode, the registers have a single serial input and a single serial output. The information is transferred one bit at a time while the registers are shifted in the same direction.

![[serial-transfer.png]]

![[serial-transfer-example.png]]

Notes:

- the output of shift register A is fed back into its input
- the output of shift register A goes to the input of shift register B

### Parallel Transfer (Parallel Mode)

All the bits of the register are transferred at the same time.

 In the parallel mode, information is available from all bits of a register and all bits can be transferred simultaneously during one clock pulse.

---

## Operations

- Operations in digital computers are usually done in parallel because that is a faster mode of operation.
- Serial operations are slower because a datapath operation takes several clock cycles, but serial operations have the advantage of requiring fewer hardware components. 

### Serial Addition

The serial adder is a sequential circuit which consists of a full adder and a flip-flop that stores the output carry.

(This design is typical in serial operations because the result of a bit-time operation may depend not only on the present inputs, but also on previous inputs that must be stored in flip‐flops.)

![[serial-adder.png]]

![[serial-adder-state-table.png]]

Operation:

1. Register A holds the augend
2. Register B holds the addend
3. Carry flip-flop is cleared to 0
4. The outputs of A and B provide a pair of significant bits for the full adder at $x$ and $y$
5. The shift control enables both registers and the carry flip-flop, so at the next clock pulse...
	- Registers are shifted once to the right
	- The sum bit from S enters the leftmost flip-flop of A
	- output carry is transferred into flip-flop 

For each succeeding clock pulse, a new sum bit is transferred to A, a new carry is transferred to Q, and both registers are shifted once to the right.

This process continues until the shift control is disabled.

### Parallel Addition

The parallel adder is a combinational circuit.

(See Section 4.4 of digital textbook)

---

## Example Shift Registers

### Four-Bit Shift Register

The output of a given flip-flop is connected to the D input of the flip-flop at its right. Note that this simplified schematic does not show a reset signal, but such a signal is required in practical designs.

shift 1, i dont
shift 0, si dont

---

### Serial Adder

![[serial-adder.png]]

![[serial-adder-second.png]]

(According to sir, tracing this will be in the exam.)

How this works:

- Shift Register A is the augend (first number to add)
- Shift Register B is the addend (second number to add)
- Serial Input is the third number to add
	- If this is set to 0000, automatically only the two numbers in the two registers are added.
	- The value of this is moved to Shift Register B once the first two numbers are added. (The sum of the first two numbers is moved to Shift Register B.)

Every time one bit is shifted out by the register, it goes into the full adder.

The sum of the full adder is shifted into Shift Register A, while the last bit of the serial input is shifted into Shift Register B.

---

### Universal Shift Register

If the flip‐flop outputs of a shift register are accessible, then information entered serially
by shifting can be taken out in parallel from the outputs of the flip‐flops. If a parallel
load capability is added to a shift register, then data entered in parallel can be taken out in serial fashion by shifting the data stored in the register.

A register capable of shifting in one direction only is a *unidirectional* shift register. One that can shift in both directions is a *bidirectional* shift register. If the register has both shifts and parallel‐load capabilities, it is referred to as a universal shift register.

(Check digital textbook p. 266 for explanations)

The most general shift register has the following capabilities:

- A clear control to clear the register to 0.
- A clock input to synchronize the operations.
- A shift-right control to enable the shift-right operation and the serial input and output lines associated with the shift right.
- A shift-left control to enable the shift-left operation and the serial input and output lines associated with the shift left
- A parallel-load control to enable a parallel transfer and the n input lines associated with the parallel transfer.
- $n$ parallel output lines
- a control state that leaves the information in the register unchanged in response to the clock. Other shift registers may have only some of the preceding functions with at least one shift operation.

![[four-bit-universal-shift-register.png]]

![[four-bit-universal-shift-register-table.png]]


---


