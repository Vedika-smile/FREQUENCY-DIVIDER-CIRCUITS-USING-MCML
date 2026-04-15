# Frequency Divider Design using MCML (Cadence Simulation)
## Project Overview

This project focuses on the design and simulation of frequency divider circuits using MOS Current Mode Logic (MCML). The objective is to achieve high-speed operation with optimized performance, which is important in communication systems such as PLLs and RF circuits.

The project involves designing basic building blocks like inverter, D-latch, and D flip-flop, and then using them to implement divide-by-2 and divide-by-3 frequency divider circuits. All circuits are simulated using Cadence Virtuoso with 180nm CMOS technology.

## Objectives
- Understand MCML (MOS Current Mode Logic) design
- Design basic digital circuits using MCML
- Implement D-latch and D flip-flop
- Design frequency dividers (divide-by-2 and divide-by-3)
- Analyze circuit behavior using simulation waveforms
## Tools and Technology
- Cadence Virtuoso
- 180nm CMOS Technology
- MOS Current Mode Logic (MCML)
- Analog and Mixed Signal Design
## Background
### Frequency Divider

A frequency divider is a circuit that reduces the input frequency.

- Divide-by-2 → Output = f / 2
- Divide-by-3 → Output = f / 3

These circuits are widely used in PLLs, clock generation, and communication systems.

### MCML Logic

MCML is used instead of CMOS in high-frequency applications due to:

#### Advantages:

- High-speed operation
- Reduced switching noise
- Better noise immunity

#### Disadvantages:
- Higher static power consumption
## Design Description
### MCML Inverter

The inverter is the basic building block. It uses a differential pair and constant current source. The output swing depends on load resistance and bias current.

### D-Latch

The D-latch is implemented using tri-state buffer concepts with MCML logic.

Operation:

When CLK = 1 → Output follows input
When CLK = 0 → Output is stored

### D Flip-Flop

The D flip-flop is implemented using a master-slave configuration of two D-latches. It captures input on clock transitions.

### Frequency Divider (Divide-by-2)

The divide-by-2 circuit is implemented using a D flip-flop. The output toggles at half the input frequency.

- If input frequency = f
- Output frequency = f / 2

### Frequency Divider (Divide-by-3)

The divide-by-3 frequency divider is implemented using MCML-based latch architecture and logic control. The circuit ensures that the output completes one cycle for every three input cycles.

This design is more complex than divide-by-2 and involves careful synchronization of latches and logic to maintain correct sequencing.

- If input frequency = f
- Output frequency = f / 3

## Results and Observations
- Divide-by-2 and divide-by-3 operations are successfully verified
- Output frequencies match expected values (f/2 and f/3)
- MCML circuits provide stable and clean waveforms
- High-speed performance is achieved
- Trade-off observed between speed and power consumption
