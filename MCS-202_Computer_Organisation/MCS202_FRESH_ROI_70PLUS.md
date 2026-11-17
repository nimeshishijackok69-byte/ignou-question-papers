# MCS-202 — Fresh ROI Analysis (70+ Target)

**Source:** ONLY `PYQ Text MCS 202.md` (7 official TEE papers: Jun 2023 – Jun 2026). Every mark below is counted question-by-question from the actual papers.
**Next exam:** Dec 2026 TEE (3 Dec, 2–5 PM).

---

## 1. The big verdict — is "numericals are only ~20 marks" true?

Pure numerical marks (solve-by-formula: conversions, 2's complement, physical address, RAM chips, IEEE-754, cache address-locating):

| Paper | Pure numerical marks /100 |
|---|---|
| Jun 2023 | 17 (2's comp 6 + conversions 5 + phys addr 6) |
| Dec 2023 | 6 (2's comp only) |
| Jun 2024 | 5 (conversions only) |
| Dec 2024 | 5 (conversions only) |
| Jun 2025 | 16 (binary equiv 6 + 2's comp 4 + cache numeric 6) |
| Dec 2025 | 27 (2's comp 5 + K-map-side 0 + RAM chips 5 + IEEE 6 + phys addr 6 + conversions 0) |
| Jun 2026 | **0** — no conversions, no 2's complement, no physical address |

**Average ≈ 11 marks. Range 0–27. Never more than 27.**

✅ **Your hypothesis is confirmed.** Pure numericals are a small, volatile bucket. Theory + pattern topics carry 75–95 marks every single paper. Strategy: theory-first is CORRECT. Numericals = top-3 shortlist only, if time allows.

⚠️ One correction though: don't count **K-map, cache mapping, flip-flop tables, MUX/decoder, 8086 programs** as "numericals". They are **mix** topics — solved on paper like a numerical, but they appear far more reliably than conversions/2's-complement. They are non-negotiable for 70+.

---

## 2. The three buckets (marks counted from all 7 papers)

### Bucket A — PURE NUMERICAL (~11 avg, max 27, twice zero)
| Topic | Papers | Total marks | Notes |
|---|---|---|---|
| Base conversions (dec↔bin/hex/oct, fraction 17.89, ASCII→UTF-8) | 4/7 | 21 | Missing Jun 2026 & Dec 2023 |
| 2's complement add/sub + overflow | 4/7 | 21 | 8-bit; Jun 2025 asked −23456 (16-bit!) |
| Physical address Seg×10h+Offset | 2/7 | 12 | Jun 23, Dec 25 |
| Cache numeric (address→location) | 1/7 | 6 | Jun 25 |
| RAM chips calc (256K×4 → 1MB) | 1/7 | 5 | Dec 25 |
| IEEE-754 → decimal | 1/7 | 6 | Dec 25 |

**Top-3 numerical shortlist (do ONLY these):**
1. **2's complement + conversions combined** — together they appeared 6/7 papers, 42 marks total, ~6/paper. Highest numerical ROI by far.
2. **Physical address** — 2 of last 4 papers, easy 6 marks, 3-minute drill.
3. **RAM chips + IEEE-754** — one-line formulas, appeared Dec 25, low effort.

### Bucket B — MIX / PATTERN-SOLVED (~24 avg, appears EVERY paper)
Truth tables, K-maps, small programs, logic diagrams. Study = practice the pattern once, marks are near-guaranteed.

| Topic | Papers | Total marks |
|---|---|---|
| 8086 assembly programs (largest, swap, add+carry, ASCII↔binary, packed BCD) | **7/7** | 50 |
| K-map + draw circuit (AND/OR/NOT or NAND) | 6/7 | 31 |
| Flip-flops: SR latch, JK, D, master-slave, edge — logic diagram + characteristic + excitation table | 6/7 | 41 |
| MUX / Decoder (2×4, 3×8, 4×1, 3×1) truth table + logic diagram | 4/7 | 29 |
| Cache mapping (direct / associative / set-assoc) with example | 6/7 | 32 (+9 locality/assoc-mem) |
| Adders (half/full) | 1/7 | 6 |
| SOP/POS, Boolean simplification | 1–2/7 | 10 |

### Bucket C — PURE THEORY (the real exam: ~60–65 marks/paper)
| Topic | Papers | Total marks | 10-mark potential |
|---|---|---|---|
| Addressing modes (ALL, with memory diagram) | **7/7** | ~60 | Jun 24, Dec 24, Jun 26 = 10m each |
| Micro-operations, fetch cycle, micro-programmed CU, Wilkes, encoded/unencoded | **7/7** | ~58 | Dec 24, Jun 26 = 10m |
| I/O: programmed vs interrupt-driven vs DMA, I/O interface | **7/7** | ~50 | 8m questions common |
| 8086 architecture: registers, flag register, components, BIU | **7/7** | ~40 | Flag register: 3 papers in a row (Jun 25→Jun 26) |
| Interrupts: concept, processing steps, IVT, INT 21h, interrupt cycle | **7/7** | ~41 | Jun 26 gave it 15 marks total |
| Von Neumann/Harvard + CPU components | **7/7** | ~37 | 5–6m each, easy |
| Disk/storage: access time, CAV/CLV, scheduling, SSD, RAID | 6/7 | ~54 | RAID 10m (Jun 25) |
| Memory: SRAM/DRAM, hierarchy, interleaving, RAM cell | 6/7 | ~42 | Jun 26 RAM cell 6m |
| RISC vs CISC + large register file | 5/7 | ~28 | 10m possible (Jun 26) |
| Subroutine call/return, FAR/NEAR, .COM vs .EXE | 5/7 | ~27 | FAR 5m Jun 26 |
| Peripherals 1-liners (CRT, LCD/LED, printers, CCD, voice, video cards, parity) | 6/7 | ~33 | Always 4–5m, never deeper |
| Pipelining, counters, fixed-point ALU, floating/fixed components | 2–3/7 | ~30 | 5–8m each |

---

## 3. Priority tiers for 70+ (ranked by marks-per-effort)

**TIER 1 — master completely (these ARE the exam):**
1. Addressing modes — 7/7, up to 10 marks, full-marks template = Jun 2024 diagram style
2. Interrupts (steps + IVT + INT 21h + interrupt-driven I/O) — 7/7
3. Micro-ops / fetch cycle / micro-programmed CU — 7/7
4. 8086 architecture (flag register FIRST, then segment/GPR, components) — 7/7
5. 8086 assembly programs (one template covers largest/add/swap/convert) — 7/7
6. I/O trio: programmed vs interrupt vs DMA + interface — 7/7
7. Cache mapping (all 3 + locality) — 6/7
8. K-map + circuit — 6/7

**TIER 2 — high marks, slightly less frequent:**
9. Flip-flops (SR/JK/D/master-slave + both tables) — 41 marks
10. Disk/storage (access time formula, CAV/CLV, scheduling, RAID 3-levels)
11. Memory (SRAM vs DRAM, hierarchy, interleaving, RAM cell)

**TIER 3 — cheap marks, low effort:**
12. RISC vs CISC + register file (1 comparison table + 1 diagram)
13. Von Neumann/Harvard/CPU components (2 diagrams)
14. Subroutine/FAR-NEAR/.COM-.EXE
15. MUX + 3×8 decoder truth tables
16. Peripherals 1-liners + short-note list

**TIER 4 — numericals, ONLY if time allows:** the top-3 shortlist above.

---

## 4. 70+ blueprint

- **Q1 (40, compulsory):** comes from Tier 1 + K-map + at most 1 numerical. Jun 2026 Q1 = K-map + RAM cell + direct cache + interrupt steps + 8086 components + FAR + flags — all Tier 1/Tier 3. Target **32+/40**.
- **Optionals:** pick your 3 strongest of Q2–Q5. Reliable picks every year: flip-flop question, MUX/decoder question, 8086 program, RISC/CISC-micro-instruction compare. Target **30–35** from 60 available.
- **Where 70+ is actually won:** the 10-mark answers — addressing modes with diagram (10), micro-programmed CU (10), encoded vs unencoded (10), 5 instructions (10), RAID (10). Shallow answers cap you at 60; depth on these 5 question types pushes you to 70+.

---

## 5. Dec 2026 trend notes (from the last 3 papers)

- Q1 is drifting **all-theory + diagram**: Jun 2026 had zero arithmetic numericals. K-map, cache, interrupt, flag = guaranteed Q1 residents.
- Flag register: appeared Jun 25, Dec 25, Jun 26 — 3 in a row. Learn all 9 flags, 1 line each.
- Interrupts got 15 marks total in Jun 2026 (steps + interrupt cycle + IVT). Heaviest-reward theory topic right now.
- Expect ~1 numerical in Q1 (2's complement OR physical address OR RAM chips — any one) and possibly a conversions set in an optional. Cover the top-3 shortlist and you're safe.
