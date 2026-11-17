# MCS-202 Topics to Study

Based on all 7 papers: June 2023 – June 2026.
Q1 is compulsory (40 marks). Attempt any 3 of Q2–Q5 (20 marks each).

---

## Must Do (came in every paper or almost every paper)

### 1. K-Map Simplification
- Simplify F(A,B,C) and F(A,B,C,D) using K-map.
- Draw the circuit using AND, OR, NOT gates or NAND gates.
- Came in all 7 papers, 5–6 marks.

### 2. Signed 2's Complement Arithmetic
- 8-bit 2's complement addition and subtraction.
- Check overflow and give the reason.
- Came in all 7 papers, 4–6 marks.

### 3. Number Base Conversions
- Decimal to binary, hexadecimal, octal.
- Hexadecimal to octal (via binary), octal to decimal.
- Fractional decimal to binary (e.g. 17.89).
- ASCII string to UTF-8.
- Came in all 7 papers, 5–6 marks.

### 4. Addressing Modes
- Immediate, Direct, Register, Register Indirect.
- Base Register, Index, Relative, Based, Indirect.
- With one example each, and with memory/register diagrams.
- Came in all 7 papers, 6–10 marks.

### 5. Cache Memory Mapping
- Direct mapping (with example).
- Associative mapping (with example).
- Set-associative / two-way set-associative (with example).
- Numeric example: given RAM size and cache size, find where an address goes.
- Locality of reference. Cache coherence.
- Came in all 7 papers, 5–6 marks.

### 6. Interrupts
- What is an interrupt. Steps to process an interrupt.
- Interrupt-driven I/O with flowchart/diagram.
- Interrupt Vector Table (IVT). Interrupt 21h.
- Came in all 7 papers, 5–6 marks.

### 7. 8086 Registers
- Segment registers (CS, DS, SS, ES) and their uses.
- Flag register — roles of flags (CF, ZF, SF, OF, PF, AF, TF, IF, DF).
- General purpose, address and data registers.
- Physical address = Segment × 10h + Offset (compute for CS:IP, DS:BX, SS:SP).
- Came in 6 of 7 papers, 5–6 marks.

### 8. 8086 Assembly Programs
- Find largest value in an array.
- Swap two memory values.
- Add two numbers, store sum and carry.
- ASCII to binary, binary to ASCII conversion.
- 2-digit ASCII to packed BCD.
- Largest of two numbers, subtract smaller from larger.
- Came in all 7 papers, 4–8 marks.

### 9. RISC vs CISC
- Differences between RISC and CISC.
- Features of RISC.
- Large register file in RISC and its use in procedure calls.
- Came in 6 of 7 papers, 4–5 marks.

### 10. Von Neumann and Harvard Architecture
- Von Neumann architecture with diagram.
- Harvard architecture with diagram.
- Difference between the two.
- Came in 5 of 7 papers, 5 marks.

### 11. Micro-programmed Control Unit
- Micro-programmed control unit — working with block diagram.
- Wilkes control unit.
- Horizontal vs vertical micro-instructions.
- Encoded vs unencoded micro-instructions.
- Micro-operation: fetch cycle (PC, IR, MAR, DR).
- Register-transfer, arithmetic, logic micro-operations.
- Came in 6 of 7 papers, 5–10 marks.

### 12. Flip-Flops
- SR latch using NOR gates.
- SR, JK, D flip-flops — logic diagram, characteristic table, excitation table.
- Master-slave flip-flop. Edge-triggered flip-flop.
- Flip-flop vs latch.
- Came in 6 of 7 papers, 5–8 marks.

---

## Also Important (came in 4–5 papers)

### 13. Instruction Pipelining
- What is instruction pipelining, with diagram.

### 14. I/O Techniques
- Programmed I/O.
- Interrupt-driven I/O vs programmed I/O.
- DMA — block diagram, DMA vs programmed I/O, DMA vs I/O processor, when to use DMA.

### 15. I/O Interface
- What is an I/O interface, its functions.

### 16. Magnetic Disk
- Disk structure with diagram.
- CAV vs CLV.
- Disk access time — definition and formula.
- Disk scheduling: FCFS, SSTF, SCAN, C-SCAN, LOOK.

### 17. Memory
- SRAM vs DRAM.
- Memory hierarchy — why and how, with diagram.
- Memory interleaving with example.
- RAM chip calculation (e.g. how many 256K × 4 chips for 1 MB).
- RAM cell logic diagram.

### 18. Multiplexer and Decoder
- 4×1 multiplexer — truth table, logic diagram.
- 2×4 decoder, 3×8 decoder — truth table, logic diagram.

### 19. 8086 Instructions
- SHL, RCL, ROL, XCHG, DEC, XOR — with one example each.

### 20. .COM vs .EXE Programs
- Differences, with example.

### 21. Subroutine Call and Return
- Steps for subroutine call and return using a stack.
- FAR and NEAR procedures.

---

## Short Notes (know 2 lines + 1 example each)

- IEEE 754 32-bit number to decimal.
- SOP and POS forms.
- Half adder and full adder.
- Ripple counter and synchronous counter.
- RAID — levels 0, 1, 5.
- Fixed-point ALU block diagram.
- Multiprocessor vs multicore.
- Parallelism in uniprocessors. Multiport memory.
- SSD vs HDD.
- CCD (Charge-Coupled Devices).
- CRT, video cards, LCD vs LED.
- Impact vs non-impact printers.
- Voice-based input devices.
- Parity bit for error detection.
- Bus Interface Unit in 8086.
- Assembly language programming tools.
- Floating point vs fixed point number components.
- Associative memory — advantages and disadvantages.

---

## Exam Weight

- Numericals and programs: about 15–35 marks per paper.
- Theory: the rest, about 65–85 marks per paper.
- Q1 alone is almost fully from the "Must Do" list.

---

## Theory vs Numerical Division

### Numerical / Solve Type (about 22% of marks)

These are fixed types. Same question, new numbers.

1. 2's complement addition and subtraction, with overflow check.
2. Number base conversions (binary, octal, decimal, hexadecimal, UTF-8, fractions).
3. K-map simplification of F(A,B,C) and F(A,B,C,D).
4. Physical address = Segment × 10h + Offset.
5. 8086 assembly programs (the 6 programs listed in topic 8).
6. Cache mapping numeric example (find where an address goes).
7. RAM chip calculation (e.g. 256K × 4 chips for 1 MB).
8. IEEE 754 32-bit to decimal.
9. Boolean simplification (SOP form problems).

### Semi-Numerical (read like theory, solved like a pattern)

1. Truth tables and logic diagrams: multiplexer, decoder, counters, RAM cell.
2. Flip-flop characteristic and excitation tables.
3. Half adder and full adder.
4. Disk access time formula.
5. Cache mapping with a worked example.

### Theory / Explain Type (about 78% of marks)

1. Von Neumann vs Harvard architecture.
2. Addressing modes with examples and diagrams.
3. Cache mapping types — explanation part.
4. Interrupts, IVT, interrupt-driven I/O.
5. 8086 registers, flag register, segment registers.
6. RISC vs CISC.
7. Micro-programmed control unit, Wilkes control, micro-instructions.
8. Micro-operations (fetch cycle, register transfer).
9. Instruction pipelining.
10. Programmed I/O vs interrupt-driven I/O vs DMA.
11. I/O interface.
12. Magnetic disk, CAV vs CLV, disk scheduling.
13. SRAM vs DRAM, memory hierarchy, memory interleaving.
14. 8086 instructions with examples.
15. .COM vs .EXE, FAR vs NEAR procedures.
16. Subroutine call and return using stack.
17. All the short notes topics listed above.
