# MCS-202 — Study Checklist (Dec 2026)

> **How to use:** Work top to bottom. Tick the boxes as you finish each sub-topic.
> ⭐ = number of papers out of 7 where it appeared. More stars = study it first.
> Everything below comes from the actual question papers (Jun 2023 – Jun 2026).

**Exam:** 3 Dec 2026, 2–5 PM · Q1 compulsory (40 m) + any 3 of Q2–Q5 (20 m each)

---

# 🥇 START HERE — appears in almost every paper

## 1. Addressing Modes ⭐7 · up to 10 marks
**One diagram style + one example per mode = full marks.**
- [ ] Immediate — operand is inside the instruction itself
- [ ] Direct — address of operand is in the instruction
- [ ] Indirect — instruction points to a location that holds the address
- [ ] Register — operand is in a register
- [ ] Register Indirect — register holds the address of the operand
- [ ] Relative — address = PC + offset
- [ ] Base Register — address = base register + offset
- [ ] Index — address = index register + base
- [ ] **The 10-mark diagram** (memory contents + registers + instruction) — copy the June 2024 style

## 2. Interrupts ⭐7 · 5–15 marks per paper
- [ ] What is an interrupt + why it exists
- [ ] The 7 processing steps (finish current instruction → save PC/status → … → fetch ISR → restore)
- [ ] Interrupt-driven I/O + flowchart/diagram
- [ ] Interrupt Cycle (one page)
- [ ] Interrupt Vector Table (IVT) — role + how it works
- [ ] INT 21h with one example

## 3. Micro-operations & Control Unit ⭐7 · 5–10 marks
- [ ] What is a micro-operation (register-transfer, arithmetic, logic — 1 example each)
- [ ] Fetch cycle micro-ops using PC, IR, MAR, DR (memorise the 4–5 lines)
- [ ] Micro-programmed control unit — block diagram + how it works
- [ ] Wilkes control unit — diagram
- [ ] Horizontal vs vertical micro-instructions
- [ ] Encoded vs unencoded micro-instructions (10-mark compare in Jun 2026)

## 4. 8086 Architecture ⭐7 · 5–6 marks
- [ ] Flag register — role + can it be a GPR? (came 3 papers in a row!)
- [ ] All 9 flags, one line each: CF, ZF, SF, OF, PF, AF, TF, IF, DF
- [ ] Segment registers: CS, DS, SS, ES — use of each
- [ ] General purpose / address / data registers
- [ ] Full 8086 components diagram (EU, BIU, queues)
- [ ] Bus Interface Unit — 2 lines

## 5. 8086 Assembly Programs ⭐7 · 4–8 marks
**One template (MOV → LEA/DX → loop → INT 21h) covers all of them — only the operation changes.**
- [ ] Add five numbers in an array → AX
- [ ] Add two numbers + store sum and carry
- [ ] Find largest in an array / largest of two + subtract smaller
- [ ] Swap (interchange) two memory locations
- [ ] ASCII digit → binary
- [ ] Binary → ASCII digit
- [ ] 2-digit ASCII → packed BCD

## 6. I/O Techniques ⭐7 · 5–8 marks
- [ ] Programmed I/O — concept + diagram
- [ ] Interrupt-driven I/O — how it differs from programmed
- [ ] DMA — block diagram, how it works
- [ ] DMA vs programmed I/O vs I/O processor — when to use which
- [ ] I/O interface — what it is + functions

## 7. Cache Memory ⭐6 · 5–6 marks
- [ ] Why cache is needed + **locality of reference** (1 example)
- [ ] Direct mapping + example
- [ ] Associative mapping + example
- [ ] Set-associative (2-way) + example
- [ ] Cache coherence (short note, 4–5 lines)
- [ ] Associative memory — advantages/disadvantages (2 lines)

## 8. K-Map ⭐6 · 5–6 marks
- [ ] 3-variable K-map F(A,B,C) → simplify
- [ ] 4-variable K-map F(A,B,C,D) → simplify
- [ ] Draw circuit with AND, OR, NOT gates
- [ ] Draw circuit with NAND gates only
- [ ] Practice the 5 past-paper functions: Σ(5,6,8,11,13,14,15) · Σ(2,3,6,7,9,10,11,12,15) · Σ(2,3,4,5) · Σ(0,1,3,4,5,6) · Σ(0,3,5,7,9,10,11,12,15) · Σ(0,4,8,11,12,13)

---

# 🥈 THEN — big marks, slightly less frequent

## 9. Flip-Flops ⭐6 · 7–10 marks
- [ ] SR latch using NOR gates + characteristic table
- [ ] SR flip-flop — diagram + characteristic + excitation table
- [ ] JK flip-flop — same three things
- [ ] D flip-flop (short note style)
- [ ] Master-slave flip-flop
- [ ] Edge-triggered flip-flop
- [ ] Flip-flop vs latch (2 lines)

## 10. Disk & Storage ⭐6 · 5–10 marks
- [ ] Magnetic disk structure + diagram
- [ ] Disk access time — definition + formula + each parameter
- [ ] CAV vs CLV (table)
- [ ] Disk scheduling: FCFS, SSTF, SCAN, C-SCAN, LOOK — 2 lines each
- [ ] RAID 0, 1, 5 — characteristics (10-mark question once)
- [ ] SSD vs HDD (short note)

## 11. Main Memory ⭐6 · 4–6 marks
- [ ] SRAM vs DRAM (table)
- [ ] DRAM (short note)
- [ ] Memory hierarchy — why + diagram
- [ ] Memory interleaving + example
- [ ] RAM cell logic diagram (Jun 2026, 6 m)
- [ ] RAM chips calculation → see Numericals #3

---

# 🥉 QUICK WINS — 2 hours total, easy marks

## 12. Von Neumann & Harvard ⭐7 · 5 marks — 2 diagrams + 3 differences
## 13. RISC vs CISC ⭐5 · 4–10 marks
- [ ] Comparison table (instruction set, addressing, code size, power, use)
- [ ] Large register file + procedure calls (1 diagram)
## 14. Subroutines & Programs ⭐5 · 4–5 marks
- [ ] Call/return using stack — steps
- [ ] FAR vs NEAR
- [ ] .COM vs .EXE
## 15. MUX & Decoder ⭐4 · 8 marks
- [ ] 4×1 MUX — truth table + logic diagram
- [ ] 3×8 decoder — truth table + logic diagram (2×4 also fine)
## 16. 8086 Instructions ⭐3 · 4–10 marks — 1 example each:
- [ ] SHL · RCL · ROL · XCHG · DEC · XOR
## 17. Peripherals 1-liners ⭐6 · 4–5 marks — never study deeper:
- [ ] CRT · Video cards · LCD vs LED · Impact vs non-impact printers · CCD · Voice input · Parity bit
## 18. Easy short notes (2 lines + 1 example):
- [ ] Instruction pipelining · Multiprocessor vs multicore · Multiport memory · Half/full adder · Counters · SOP/POS · Fixed-point ALU · Floating vs fixed point

---

# 🔢 NUMERICALS — only if time allows (avg ~11 marks, sometimes ZERO)

## 1st priority: 2's Complement + Conversions (together 6/7 papers)
- [ ] 8-bit add/sub with overflow + reason (practice: +50/−50, +120/+9, −39/+126)
- [ ] Decimal → binary / hex / octal (873, 384, 225)
- [ ] Hex → octal via binary, octal → decimal
- [ ] Fraction → binary (17.89)
- [ ] ASCII string → UTF-8 ("the escape sequence")

## 2nd priority: Physical Address ⭐2 (easy 6 marks)
- [ ] Segment × 10h + Offset — practice CS:IP, SS:SP, DS:BX (Jun 2023 & Dec 2025 sets)

## 3rd priority: One-line formulas
- [ ] RAM chips: 1MB with 256K×4 chips → 4 chips (verify by solving)
- [ ] IEEE-754 32-bit → decimal (Dec 2025 example: S=0, Exp=10001001, M=1111…)

---

## ✅ Final self-test before the exam
- [ ] June 2026 Q1 timed, alone → target 32+/40
- [ ] Any one optional set (Q2–Q5) → target 30+/60
