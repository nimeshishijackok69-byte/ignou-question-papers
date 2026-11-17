# IGNOU BCA_NEW Dec 2026 — 60% Guaranteed Study Plan
**Enrolment:** 2451405498 — BCA_NEW | Centre: 29049P I.P. Estate New Delhi-110002
**Goal:** 60/100 (30/50 for 50-mark papers) in every course, from PYQs only.
**Based on:** 50 TEE PDFs in this repo (Jun 2021 – Jun 2026) + Assignments + Datesheet image.

---

## Datesheet

| Date | Code | Course | Slot | Pattern |
|---|---|---|---|---|
| 2026-12-03 | MCS202 | Computer Organisation | 2-5 PM | Q1 40 comp + any 3×20 /100 |
| 2026-12-04 | MCS203 | Operating Systems | 2-5 PM | Q1 40 comp + any 3×20 /100 |
| 2026-12-08 | BCS42 | Algorithm Design | 10 AM-1 PM | Q1 20 comp + any 3×10 /50 (2h) |
| 2026-12-09 | MSEI23 | Cyber Security | 10 AM-1 PM | Q1 any 4/5×5=20 + any 2/3×5 + any 2/3×10 /50 (2h) |
| 2026-12-10 | BCS151 | Software Engineering | 10 AM-1 PM | Q1 40 comp + any 3×20 /100 |
| 2026-12-23 | BECS184 | Data Analysis | 2-5 PM | Any 2/4×20 + any 5/7×12 /100 |
| 2026-12-26 | BCOS184 | E-Commerce | 10 AM-1 PM | Any 5/8×20 (Q7/Q8 are 4×5) /100 |

Gaps: 5-7 Dec → BCS42, 11-22 Dec → BECS184, 24-25 Dec → BCOS184.

---

## MCS-202 Computer Organisation (3 Dec) — 7 papers 2023-2026

**Q1 must-master (~40m):**
1. **K-map** 7/7 — Σ minterms + NAND/AND-OR-NOT
2. **Cache mapping** 7/7 + numerical
3. **Interrupt steps + IVT** 6/7
4. **Addressing modes** 7/7 — all modes + diagram (growing to 10m)
5. **8086 Flag + Segment registers + Physical address CS:IP** — Flag 3 in a row since Dec 2025
6. **Conversions + 2's complement overflow** 6/7
7. **Micro-ops / Fetch cycle / Microprogrammed CU** 7/7
8. **RISC vs CISC** 6/7

**Optional bank:** Flip-flop tables, Decoder/MUX, DMA vs Programmed I/O, Microprogrammed CU (10m), 8086 program (add/convert/interchange/largest)

**Emerging:** Jun 2026 Q1 all-theory, no conversions. IEEE-754 numerical Dec 2025. Peripherals fading to 4m short notes.

---

## MCS-203 Operating Systems (4 Dec) — 7 papers 2023-2026

**Q1 must-master (~40m):**
1. **Numerical trio** — Scheduling (FCFS/SJF/SRTN/RR Gantt+TAT/WAT), Page Replacement (LRU/FIFO faults), Disk Scheduling (SSTF/SCAN head movement)
2. **Semaphore** — Producer-Consumer + Dining Philosopher pseudocode 5/7
3. **Deadlock** — 4 conditions + RAG + Banker's + Detection 5/7
4. **Architectures** — iOS Layered (3 in a row = hottest), Linux Kernel, Android Layered — draw each <5 min

**Optional:** Distributed Design Issues (7/7), Virtual Memory/Paging, Windows 10, Lamport mutual exclusion, Partition Allocation (First/Best/Worst — new Jun 2026), RAG graph numerical (new Jun 2026)

**Emerging:** Numerical slot rotates. Short Notes Q5 repeats main topics — make 1-page notes for each.

---

## BCS-042 Algorithm Design (8 Dec) — 7 papers 2021-2024, 50m/2h
**Target 30/50.** Q1 comp 20 (4-5 crumbs) + any 3×10.

**Q1 guaranteed by 4 topics:**
1. **Asymptotics ordering + O/Θ proof + symbols Ω/Θ/O** 5/7 — order O(n), O(n log n), O(n²), O(2ⁿ), n!; prove 6n²+8n+6=O(n²), 7n²+8n-9=Θ(n²)
2. **Recurrence writing + tree solving** 6/7 — Fib/Factorial + T(n)=aT(n/2)+n tree + Master 3 cases
3. **Linear + Binary Search** 4/7 — pseudocode + best/worst + comparisons (search 15, search 9, 64 elements)
4. **Adjacency List + Matrix** 5/7 — Q1 free 5m

**Any 3 optionals (10m each):**
5. **Kruskal MCST** 7/7 any MST, 4/7 Kruskal apply + Prim compare
6. **DFS traversal** 6/7 BFS-or-DFS, DFS 3/3 in 2023-24 (replaced BFS) — expect DFS + O(V+E)
7. **Dijkstra** 4/7 — pseudocode + trace + negative-weight failure
8. **Bubble + Quick Sort** 6/7 any sorting — intermediate tables (Jun 2024 anomaly = 0 sorting, expect return)
9. **Induction** — 0/7 in 2021-22 → 3/3 in 2023-24 (1+...+n, 1²+...+n²) — memorise both
10. **Euclid GCD** 3/7 — GCD(325,95) steps

**Emerging:** Master method/Strassen/Karatsuba/Horner vanished 2023-24. Fractional Knapsack is wild-card. Assignment 2024-25 mirrors full pool.

---

## MSEI-023 Cyber Security (9 Dec) — 6 papers 2021-2024, 50m/2h
**Target 30/50.** Q1 any 4/5×5=20 + any 2/3×5=10 + any 2/3×10=20.

**Verbatim repeats to hijack:**
- **Social engineering attack cycle** 6/6 (note + short)
- **XSS + XSRF + thwarting** long 10m verbatim Jun23→Dec23
- **SQL Injection + example** 3/6 identical
- **Shadow Paging Recovery** long 10m verbatim Jun23→Dec23
- **Concurrency Control** long 10m verbatim Dec21→Jun24
- **Extended/Base services of server programs** 3/6 long

**Note bank (12, need 4):** Trojan, Phishing, Email spoofing/bombing, Social Networking, Waste Mgmt, Reverse Engg, Impersonation, Social Bookmarking, White-label SNS, ACID, Data Fragmentation

**Emerging 2023-24:** XSS+XSRF paired, 3-tier vs 2-tier diagram (Jun24), email tracking, hybrid crack. DBMS fundamentals now in Section A (ER, Data Dictionary, Client/Server).

**60+ =** Note bank 15-20/20 + XSS+XSRF + Shadow paging + Concurrency rehearsed as full 10m.

---

## BCS-151 Software Engineering (10 Dec) — 7 papers 2021-2024, 100m/3h
**Q1 = 40 always:** (a) SRS IEEE 15-25m + (b) SDLC model 7-10m + (c) FOD/structure/cohesion/data dictionary/UML 5-10m. Q2-Q5 any 3×20, each has diagram for *same SRS system.*

**Must-master 10:**
1. **IEEE SRS 25m** 7/7 — biggest block. Memorise: Purpose, Scope, Definitions, Roles, Functional Req, Non-functional, Interfaces, Assumptions. Case studies: Hospital→Online Shopping→Online Banking→OEFSS→OSCAS→OAS→OASS. Dec 2026 = new "Online ___ University ___"
2. **SDLC model vs Waterfall** 7/7 — Waterfall, Prototype, Spiral, Iterative, RAD diagram+advantages
3. **DFD Zero + Level-1** 7/7 (10m)
4. **ERD** 5/7, 3/3 in 2023-24 — now mandatory
5. **Use-case** 5/7 (or Data Dictionary Jun24)
6. **PERT vs GANTT** 7/7 — PERT Jun21/Jun23/Dec23, GANTT Dec21/Dec22/Jun24 → lean PERT Dec 2026
7. **FOD principles/features + cohesion/coupling** 4/7, 3/3 recent
8. **Static Objects / OOD identification** 5/7, 4/4 recent
9. **Testing** 6/7 — white/black, unit/module/integration, alpha/beta, V&V, 5 tools
10. **CMM 5 levels** 4/7

**Scoring path:** SRS 25 + model 8 + FOD 4 = 37/40 + DFD 9 + PERT/GANTT 8 + ERD 8 = **62 before Q4/Q5**. Practice Railway Reservation (Asst 2024-25) + OAS/OASS on blank paper.

---

## BECS-184 Data Analysis (23 Dec) — 4 papers 2022-2024, 100m/3h
**Any 2/4×20 + any 5/7×12.** Pick 1 numerical + 1 theory 20m.

**Repeats:**
- **Qualitative vs Quantitative** 4/4
- **Histogram + Normal + Ogive + Skewness/Kurtosis** 4/4
- **Correlation r + t significance** 3/4 (+Asst) — Dec22 20m numerical
- **Composite Index** 3/4 (Ranking Dec23)
- **Non-sampling errors** 3/4

**Blueprint:** 1×20m numerical (correlation r + t=±2.776 OR Mean/SD + histogram OR HM/percentile) + 1×20m theory (dispersion/variability + reliability OR Composite Index OR Census stages) + 5×12m (Multivariate vs Univariate + ANOVA, Type I/II + Null/Alt + Z/t/F, Case Study vs Participatory, Sampling frame + mall/snowball, t-distribution). Short notes: Ethnography, FGDs, Grounded Theory, Data mining, Model, Outlier.

**Emerging:** Mathematical Modelling + Logic (Dec23 = Asst verbatim), Case Study 2023-24, mall-intercept sampling (Jun24), percentile/HM numericals.

---

## BCOS-184 E-Commerce (26 Dec) — 5 papers 2022-2024, 100m/3h
**Any 5/8×20.** Q7/Q8 4×5 matrices = safest 20m, never skip.

**Repeats:**
- **Digital vs Electronic Signature + Symmetric vs Asymmetric** 5/5 = 10m guaranteed
- **Payment systems EFT/NEFT/RTGS/IMPS/UPI** 4/5 (20m)
- **IT Act 2000 vs 2008 + offences/punishments** 4/5 (20m)
- **Gartner e-Gov model + Digital India 9 Pillars** 4/5
- **Cyber Security trends/types** 4/5

**Blueprint:** Lock Q7/Q8 (signatures + payments = 40) + IT Act 20m + e-Comm advantages 20m = 80 potential. Matrices to drill: Linux vs Windows, Internet vs WWW, e-NAM vs GeM, Web vs App server.

**Emerging:** DLT, Digital vs Virtual vs Crypto (Jun24), Fintech (Dec23), SDLC/App Dev. Fading: AI/IoT long, Player-functioning (Amazon/Flipkart) — skip.

---

## Day-by-day plan (24 days to first exam)

**Nov 10-14 – MCS-202:** Solve K-map + Cache + Addressing modes topic-wise from all 7 papers. Diagram drills. Then Micro-ops/CU + Interrupt + Flip-flop + DMA. Write 8086 programs. Mock Jun 2026 Q1 (theory-only).
**Nov 15-19 – MCS-203:** Numerical trio (Scheduling Gantt, Page faults, Disk head) — write formulas first, step marks. Then Semaphore + Deadlock/RAG + architectures (draw iOS/Linux/Android <5 min). 1-page short notes bank.
**Nov 20-22 – Mock:** MCS-202 + MCS-203 full mocks 3h, target 60+ each. Fix weak spots.
**Nov 23-27 – BCS-042:** Asymptotics + recurrence tree + search + adjacency + Kruskal + DFS + Dijkstra + sorting tables + induction. 1 random Kruskal graph + 1 DFS trace per day.
**Nov 28-30 – BCS-151 part 1:** IEEE SRS skeleton on blank paper (Railway Reservation + OAS). DFD Zero+1 + ERD for same system. PERT/GANTT both.
**Dec 1-2 – BCS-151 part 2 + revision:** Model vs Waterfall, FOD, Static Objects, Testing, CMM. Full SRS+DFD+ERD set on new "Online Library/Hostel" system each day.
**Dec 3 MCS-202, Dec 4 MCS-203** — morning quick recall only, no new topics.
**Dec 5-7 – BCS-042 rapid:** Redo all Q1 crumbs + Kruskal/DFS/Dijkstra traces. Night 7: early sleep for 9 AM exam.
**Dec 8 BCS-042. Afternoon Dec 8 → Dec 9:** MSEI-023 note bank + XSS/XSRF + Shadow paging + Concurrency full answers. DBMS basics (ER, Client/Server).
**Dec 9 MSEI-023.** Afternoon Dec 9 → Dec 10 (no gap!): Final BCS-151 SRS rehearsal — MCS-202/203 taught us Q1 SRS is not new, rehearse Railway + OAS blank.
**Dec 10 BCS-151.**
**Dec 11-20 – BECS-184:** One 20m numerical per day (correlation, histogram, HM/percentile) + one 20m theory + 5×12m tables. Build short-note bank.
**Dec 21-22 – Mock BECS.** **Dec 23 exam.**
**Dec 24-25 – BCOS-184:** Matrices (Signatures, Payments, IT Act, Gartner, Digital India) + 2×20m longs. **Dec 26 exam.**

### Daily method (all 7 courses)
1. Solve topic-wise, not year-wise (e.g., all K-maps together).
2. Diagram blank in <5 min; if you can't, repeat.
3. Numerics: formula/steps first → substitute (step marks).
4. Every 5m answer = 1 example / 1 diagram / 1 table.
5. Mock under 3h, target 60% before exam.

## Subjective risks for 60+ on EVERY paper
- **Highest risk:** BCS-151 (SRS 25m decides pass/fail — must be able to write IEEE SRS on unknown "Online ___" system).
- **Second:** MCS-203 numerical rotation + iOS/Linux/Android diagrams (theory-only = 5/10).
- **Easiest 60s:** BCOS-184 (2 matrices = 40) + BECS-184 (1 numerical + 1 theory + 5×12) + MSEI-023 (note bank + 2 verbatim longs).
