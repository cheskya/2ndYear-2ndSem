# Registers

Resources:

- p. 255 of digital textbook (Chapter 6.1)
- Canvas Modules
	- Registers
- [[Info - Sequential Circuits]]
- https://www.electronics-tutorials.ws/sequential/seq_5.html

---

## Register

A register is a digital device used for storage and transfer of data. It consists of a group of flip-flops, each one of which shares a *common clock* and is capable of storing *one bit of information*.

An $n$-bit register consists of a group of $n$ flip-flops capable of storing $n$ bits of binary information.

In its broadest definition, a register consists of a group of flip-flops together with gates that affect their operation.

- flip-flops hold the binary information
- gates determine how the information is transferred into the register

*NOTE:* It isn't good to have logic gates control the clock input, as this might make the clock not synchronized. A preferred alternative in high‐speed circuits is to suppress the clock action, rather than gate the clock signal, by leaving the clock path unchanged, but recirculating the output of each register cell back through a two‐channel mux whose output is connected to the input of the cell. When the clock action is not suppressed, the other channel of the mux provides a datapath to the cell.

---

## Loading into Registers

The transfer of new information into a register is referred to as *loading* or *updating* the register.

### Parallel Load

If all the bits of the register are loaded simultaneously with a common clock pulse, we say that the loading is done in *parallel*.

In this configuration, if the contents of the register must be left unchanged, the inputs must be held constant or the clock must be inhibited from the circuit.

*Note:* Inserting gates into the clock path is ill advised because it means that logic is performed with clock pulses. The insertion of logic gates produces uneven propagation delays between the master clock and the inputs of flip‐flops. T

### Serial Load

Load the flip-flops once at a time.


---

## Example Registers
### Four-Bit Register

The value of ($I_3$, $I_2$, $I_1$, $I_0$) immediately before the clock edge determines the value of ($A_3$, $A_2$, $A_1$, $A_0$) after the clock edge.

The $Clear\_b$ input is useful for clearing the register to all 0's prior to its clocked operation.

![[four-bit-register.png]]

### Four-Bit Register with Parallel Load

The additional gates implement a two-channel mux whose output drives the input to the register with either the data bus or the output of the register.

The load input to the register determines the action to be taken with each clock pulse.

- When load input is 1, data at the four external inputs are transferred into the register (with next positive edge of clock)
- When load input is 0, the outputs of the flip-flops are connected to their respective inputs.

![[four-bit-register-with-parallel-load.png]]