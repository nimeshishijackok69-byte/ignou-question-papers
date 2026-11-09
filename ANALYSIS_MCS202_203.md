# MCS-202 & MCS-203 PYQ Analysis — How to Score 60+ Marks

**Papers analysed:** 14 official IGNOU TEE papers
- MCS-202 Computer Organisation — June 2023, Dec 2023, June 2024, Dec 2024, June 2025, Dec 2025, June 2026
- MCS-203 Operating Systems — June 2023, Dec 2023, June 2024, Dec 2024, June 2025, Dec 2025, June 2026

Files: `MCS-202_Computer_Organisation/`, `MCS-203_Operating_Systems/`
Index: `MCS-202_MCS-203_PYQ_INDEX.md`

---

## Exam Pattern — Both Courses

- Time: 3 Hours, Maximum Marks: 100, Weightage: 70%
- **MCS-202:** Q1 compulsory 40 marks (7–9 sub-parts × 4–6 marks). Q2–Q5, attempt any 3 × 20 marks.
- **MCS-203:** Q1 compulsory 40 marks (4 × 10 marks). Q2–Q5, attempt any 3 × 20 marks. Q5 is almost always Short Notes 4×5=20.

**To get 60/100 in TEE:** ~35–40 from Q1 (compulsory) + ~20–25 from 3 optional questions.
Q1 topics are non-negotiable. Optional topics you can choose based on strength.

Every long question expects **diagram + example + (where applicable) truth table / steps**. Theory-only answers get ~5/10.

Question types that repeat across both papers:
1. **Numerical** — formulaic, practice = guaranteed marks
2. **Diagram-based theory** — labelled diagram is compulsory
3. **Comparison / Difference table** — RISC vs CISC, SRAM vs DRAM, etc.
4. **Algorithm / Program / Process steps** — pseudocode, 8086 program, interrupt steps

---

## MCS-202 : Computer Organisation

### Frequency out of 7 papers

| Topic | Papers | Marks / Type |
| :--- | :--- | :--- |
| K-map simplification + draw circuit (NAND / AND-OR-NOT) | 7/7 | 5–6, Q1/Q2, 4-var Σ minterms |
| Cache mapping — Direct / Associative / Set-associative | 7/7 | 5, Q1 + numerical location Jun 2025 |
| Addressing modes (all modes + diagram) | 7/7 | 5–10, diagram with memory/register content |
| Flip-flop / Counter — SR, JK, D, Master-Slave, Edge-triggered; truth + excitation table | 7/7 | 7–10 |
| DMA / Programmed I/O vs Interrupt-driven I/O, I/O Interface | 7/7 | 5–8, block diagram |
| Micro-operations / Fetch cycle / Microprogrammed CU / Wilkes control | 7/7 | 5–10 |
| 8086 Assembly program | 7/7 | 5–8: add 2 numbers, ASCII↔Binary/BCD, interchange, largest, add 5 numbers |
| Number conversions (Decimal/Binary/Hex/Octal/ASCII→UTF-8) + 2's complement overflow | 6/7 | 5–6. **Missing in Jun 2026** |
| Interrupt — concept, processing steps, INT 21h, Interrupt Cycle, IVT | 6/7 | 5–6, steps list |
| 8086: Segment registers, Flag register, Physical address CS:IP | 6/7 | 5–6. Flag register: Dec 2025, Jun 2025, Jun 2026 (3 in a row) |
| RISC vs CISC + Large Register File | 6/7 | 4–5 |
| Decoder / MUX / Adder — truth table + logic diagram | 5/7 | 8 |
| Disk / Storage: CLV/CAV, SSD vs HDD, RAID, SRAM vs DRAM, Magnetic disk | 5/7 | 5, rotating |
| CPU architecture: Von Neumann / Harvard, CPU components | 4/7 | 5–6, diagram |
| 8086 Instructions SHL/RCL/ROL/XCHG/DEC/XOR, FAR/NEAR, .COM vs .EXE | 4–5/7 | 4–5, example each |
| Pipelining / Multiprocessor / Multicore / Cache Coherence / Parallelism | 4/7 | Short notes 5 — easy marks |
| Peripherals trivia: CRT, LCD/LED, Printers, CCD, Voice input, Video cards | 4/7 | 4–5, 1-liners only |

### Emerging trends 2025–26

1. **Jun 2026 Q1 format change:** All theory/diagram (K-map, RAM cell, Direct Cache, Interrupt steps, 8086 components, FAR procedure, Flag register) — *no conversions / 2's complement*. K-map, Cache, Interrupt, Flag are now guaranteed.
2. **Addressing modes question is getting bigger:** Dec 2024 & Jun 2024 = 10 marks with diagram (memory + registers + instructions/operands/addresses). Jun 2026 = 5 modes list (Indirect, Relative, Register, Based, Immediate). Learn all modes with example + diagram.
3. **IEEE-754 numerical** appeared Dec 2025 (6 marks). Floating-point vs Fixed-point appeared Dec 2023. Prepare IEEE conversion steps.
4. **Physical address numerical** (CS:IP, SS:SP, DS:Offset) appeared Jun 2023 and Dec 2025. Recurring 6-mark numerical.
5. **Peripherals trivia is fading** to 4-mark short notes. Prepare 1-liners, don't spend deep time.

### 60-mark blueprint — MCS-202

Master these 8 for Q1 (= ~40 marks):

1. K-map — practice Σ minterms from all 7 papers
2. Cache mapping — all 3 types + direct-map address numerical
3. Interrupt processing steps — list all steps + diagram
4. Addressing modes — all 8 modes, example + memory diagram
5. 8086 Flag + Segment registers + Physical address calculation
6. Conversions + 2's complement overflow
7. Micro-ops / Fetch cycle / Microprogrammed CU diagram
8. RISC/CISC + Large Register File diagram

Then for optional Q2–Q5, master these 5 (pick any 3 strongest):
- Flip-flop characteristic + excitation table
- Decoder / MUX truth table + logic diagram
- DMA vs Programmed I/O vs Interrupt-driven I/O
- Microprogrammed Control Unit (10 marks)
- 8086 program (any 1 type — add, convert, interchange, largest)

---

## MCS-203 : Operating Systems

### Frequency out of 7 papers

| Topic | Papers | Marks / Type |
| :--- | :--- | :--- |
| Memory Mgmt: Paging, Segmentation, Virtual Memory, Demand Paging, Address mapping, valid/invalid bits | 7/7 | 10, theory + diagram |
| OS Types & Functions: Batch, Time-sharing, Real-time, Distributed, Interactive, essential functions | 7/7 | 10, rising in Jun 2025–26 |
| Distributed Systems design issues / goals | 7/7 (design/models) | 10, exact repeat Jun 2023, Jun 2024, Dec 2025 |
| CPU Scheduling numerical: FCFS/SJF/SRTN/RR, Gantt, TAT/WAT/Throughput/Utilization | 3/7 | 10 when it comes, always Q1 |
| Page Replacement numerical: LRU/FIFO/LFU/OPT, page faults | 4/7 | 10, all Dec papers |
| Disk Scheduling numerical: SSTF/SCAN/C-SCAN, head movement | 3/7 | 10, increasing in Dec |
| Deadlock: Conditions, RAG, Banker's, Havender, Detection/Recovery | 5/7 | 5–10. Jun 2026 = new RAG graph numerical |
| Semaphore: Producer-Consumer, Dining Philosopher, Reader-Writer | 5/7 | 10, most repeated algorithm |
| Linux: Architecture/Kernel, Memory Mgmt, Security (accounts/permissions/encryption) | 5/7 | 10 + short note |
| iOS: Layered Architecture, Features, Evolution, Directories | 5/7 | Layered arch: Jun 2024, Jun 2025, Dec 2025 (3 in a row) |
| Android: Layered Arch, Processes, Memory, File/Security, Libraries | 6/7 | Jun 2025 new: Foreground/Visible/Service/Background/Empty |
| Windows 10: Process Mgmt, Memory Mgmt (Virtual/Demand), IPC, Features | 6/7 | 10 |
| Distributed models: Client/Server, RPC, Distributed Objects, DSM, loosely/tightly coupled | 4/7 | 10 + short note |
| Distributed Mutual Exclusion: Lamport, Ricart-Agrawala, Bakery | 4/7 | 10, name rotates |
| Multiprocessor sync: Test-and-set, Compare-and-swap, Fetch-and-add, Master-Slave / Separate Supervisor | 4/7 | 10 |
| Mobile OS design issues | 4/7 | 8–10 + short note |
| File System: Directory structures (2-level/acyclic/general graph), File allocation (continuous/non-continuous) | 3/7 | Jun papers |
| Security Models: Access Matrix, RBAC/Rule-based | 2/7 new | Jun 2025–26 short notes |
| Partition Allocation First-fit/Best-fit/Worst-fit + Thrashing | 1/7 new | Jun 2026, 10 marks |

### Emerging trends 2025–26

1. **Numerical slot rotates:** Scheduling *or* Page Replacement *or* Disk Scheduling = 10 marks in Q1/Q2. You must prepare all 3 — they are formulaic, practice = guaranteed 10.
2. **Jun 2026 new numerical styles:** Partition Allocation (First/Best/Worst fit), RAG Deadlock Detection graph (4 processes / 2 resources), Thrashing cause/detection/elimination. Prepare fundamentals, not just old numbers.
3. **iOS Layered Architecture** is the hottest architecture topic. Next: Linux Kernel, Android Layered.
4. **Android Processes classification** (Jun 2025) is a new specific topic — learn all 5 process types.
5. **Short Notes Q5 (4×5=20) are not new topics** — they repeat main topics: Demand Segmentation, Deadlock Avoidance/Detection, RPC, Linux Memory/Security, Android Libraries/Layers, iOS Directories, Mobile Design Issues, Windows Features, DSM, Process vs Thread. Prepare 1-page notes for each.

### 60-mark blueprint — MCS-203

Master these for Q1 (= ~40 marks):

1. **Numerical trio** — Scheduling (Gantt + TAT/WAT), Page Replacement (page faults), Disk Scheduling (head movement)
2. **Semaphore classic** — Producer-Consumer + Dining Philosopher (pseudocode)
3. **Deadlock** — 4 conditions + RAG + Banker's algorithm
4. **OS Architecture** — iOS Layered (highest probability) + Linux Kernel + Android Layered (learn to draw each in <5 min)

Then optional Q2–Q5, pick 3 strongest:
- Distributed Design Issues
- Virtual Memory / Paging / Segmentation diagram
- Windows 10 Process Management
- Distributed Mutual Exclusion (Lamport / Ricart-Agrawala)
- Partition Allocation First/Best/Worst fit
- Memory Management in Linux / Windows

---

## Combined Priority — Limited Time

### Tier-1 (Must — ~70% of both papers)
- **MCS-202:** K-map, Cache, Interrupt, Addressing modes, Flag/Segment, Flip-flop, DMA/I/O, Microprogrammed CU, Conversions/2's complement, 8086 program
- **MCS-203:** Scheduling + Page + Disk numericals, Semaphore, Deadlock, Virtual Memory, Linux/iOS/Android architectures, Distributed design

### Tier-2 (Likely — short notes + 5 marks)
- **MCS-202:** RISC/CISC, Pipelining, Multiprocessor/Multicore, .COM/.EXE, Von Neumann/Harvard, IEEE-754, Decoder/MUX
- **MCS-203:** Lamport/Ricart mutual exclusion, Multiprocessor sync, Mobile design issues, Windows 10, File directory structures, OS types (Batch/Time-sharing/Real-time)

### Tier-3 (1-liners only)
- Peripherals (CRT/LCD/Printers/CCD), Wireless (Bluetooth/NFC/IR), Mobile CPUs (Snapdragon/Atom), Symbian, Voice input recognition

---

## How to use this for Dec 2026 prep

1. Solve all 7 papers topic-wise (not year-wise) — e.g., do K-map from all 7 papers together, then Cache from all 7.
2. For every diagram topic, practice drawing it blank in under 5 minutes.
3. For every numerical, write the formula/steps first, then substitute — examiners give step marks.
4. Short notes: make 1-page notes for Tier-2 topics — they are 5 marks each and repeat.
5. Mock: attempt Q1 fully (40) + any 3 optional (60) in 3 hours, target 60+ before exam.

**Based on:** `MCS-202_TEE_*.pdf` and `MCS-203_TEE_*.pdf` in this repo (official IGNOU TEE papers, Jun 2023–Jun 2026).
