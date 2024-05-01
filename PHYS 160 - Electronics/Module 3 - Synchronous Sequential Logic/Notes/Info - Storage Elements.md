# Storage Element

*Resources:*

- p. 193 and p. 196 of digital textbook
- *[[Info - Sequential Circuits]]
- <https://en.wikipedia.org/wiki/Flip-flop_(electronics)>

---

## Types of Storage Elements

### Latches

Storage elements that operate with *signal levels* (rather than signal transitions). These are level-sensitive devices.

Latches are the basic circuits from which all flip-flops are constructed.

Although latches are useful for storing binary information and for the design of asynchronous sequential circuits, they are not practical for use as storage elements in synchronous sequential circuits. (They're really mostly for constructing flip-flops, which are more useful.)

![[latches-symbols.png]]

#### SR Latch

- two cross-coupled NOR or NAND gates
	- the NAND gate version is sometimes referred to as an $S'R'$ Latch
		- input signals for the NAND version are the complement of the values used for the NOR version
		- requires a 0 signal to change its state
	- the NOR gate version is sometimes referred to as an $RS$ Latch (not in book, see [here](https://onlinedocs.microchip.com/pr/GUID-C866D457-41E2-43C7-8442-2F1193FAAD9F-en-US-4/index.html?GUID-65A9C6D5-B95F-4A18-ABB1-7A556BF7E08A) and [here](https://www.geeksforgeeks.org/difference-between-sr-flip-flop-and-rs-flip-flop/))

- two inputs labeled $S$ for set and $R$ for reset

	- for NOR gate version
		- under normal conditions, both inputs are 0
		- even when switching states, both inputs must be set to 0 first (to avoid the forbidden state)
		- $S=1,R=0$ gives you $Q=1,Q'=0$ (set state)
		- $S=0,R=1$ gives you $Q=0,Q'=1$ (reset state)
		- $S=R=1$ gives you $Q=Q'=0$ (forbidden state)

	- for NAND gate version
		- under normal conditions, both inputs are 1
		- even when switching states, both inputs must be set to 1 first (to avoid the forbidden state)
		- $S=0,R=1$ gives you $Q=1,Q'=0$ (set state)
		- $S=1,R=0$ gives you $Q=0,Q'=1$ (reset state)
		- $S=R=0$ gives you $Q=Q'=1$ (forbidden state)

- an additional input ($En$) can be added that controls *when* the state of the latch can be changed by determining whether $S$ and $R$ (or $S'$ and $R'$) can affect the circuit

This indeterminate condition makes this circuit difficult to manage, and it is seldom used in practice.

![[sr-nor.png]]

![[sr-nand.png]]

![[sr-control.png]]

#### D Latch (Transparent Latch)

A somewhat modified [[Info - Storage Elements#SR Latch|SR latch]] with control input. It eliminates the condition of the indeterminate state in the [[Info - Storage Elements#SR Latch|SR latch]] by ensuring that inputs $S$ and $R$ are never equal to 1 at the same time.

- two inputs $D$ (data) and $En$ (enable)
	- in an SR latch with control input, D goes to S while D' goes to R.
	- $D=0$ gives you $Q=0$ (reset state)
	- $D=1$ gives you $Q=1$ (set state)

The output follows changes in the data input as long as the enable input is asserted.

![[d-latch.png]]

---

### Flip-Flops

Storage elements that are controlled by a *clock transition*. It is a binary storage device capable of storing one bit of information. These are edge-sensitive devices.

The transition of one state to the next occurs only at predetermined intervals dictated by the clock pulses.

**Characteristic Tables:**

A characteristic table defines the logical properties of a flip-flop by describing its operation in tabular form. 

![[flip-flop-tables.png]]

**Characteristic Equations:**

The logical properties of a flip-flop, as described in the characteristic table, can be

expressed algebraically with a characteristic equation.

D flip-flop

- $Q(t+1)=D$

JK flip-flop

- $Q(t+1)=JQ'+K'Q$

T flip-flop

- $Q(t+1)=T \oplus Q = TQ' + T'Q$

Note: Q(t)$ is the value of the flip-flop output before a clock transition, and $Q(t+1)$ is after a clock transition. We can use $Q$ to generalize.

#### Edge-Triggered D Flip-Flop

- can be made using...
	- two [[Info - Storage Elements#D Latch (Transparent Latch)|D latches]] and an inverter
		- first latch is called master, second latch is called slave
	- three [[Info - Storage Elements#SR Latch|SR latches]]
- one input $D$
	- same situation as the inputs in a [[Info - Storage Elements#D Latch (Transparent Latch)|D latch]]

![[d-flip-flop.png]]

![[d-flip-flop-positive.png]]

![[d-flip-flop-symbols.png]]

#### JK Flip-Flop

- can be made using...
	- one [[Info - Storage Elements#Edge-Triggered D Flip-Flop|D flip-flop]] and gates
- two inputs $J$ and $K$
	- $J$ input sets the flip-flop to 1
	- $K$ input sets the flip-flop to 0
	- both inputs enabled complement the output (toggle)

![[jk-flip-flop.png]]

#### T (toggle) Flip-Flop

- can be made using...
	- a [[Info - Storage Elements#JK Flip-Flop|JK flip-flop]] when inputs J and K are tied together
	- a [[Info - Storage Elements#Edge-Triggered D Flip-Flop|D flip-flop]] and an exclusive-OR gate
- one input $T$
	- $T=0$ ($J=K=0$) does not change the output
	- $T=1$ ($J=K=1$) complements the output

![[t-flip-flop.png]]

---

## Direct Inputs

Some flip-flops have asynchronous inputs that are used to force the flip-flop to a particular state independent of the clock.

- The input that sets the flip-flop to 1 is called *preset* or *direct set*.
- The input that sets the flip-flop to 0 is called *clear* or *direct reset*.

For example:

![[d-flip-flop-asynch-reset.png]]