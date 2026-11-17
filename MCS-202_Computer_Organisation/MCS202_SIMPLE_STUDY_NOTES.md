# MCS-202 — SIMPLE STUDY NOTES
**Learn WHILE you solve. No separate theory. Every topic = 1 exam question from your papers.**

> How to use this file: For each topic do this order:
> 1. Read **Simple idea** (2 min) 2. Read **How exam asks** 3. Copy the **Solved example on blank paper** yourself 4. Then do the other paper's question without looking.
> Never just read. Always write.

---

## HOW MCS-202 PAPER WORKS (2 min)

- Q1 is compulsory = 40 marks. If you miss Q1, you fail. Q1 is always small pieces: K-map, Cache, Interrupt, Flag, Addressing modes, Conversions.
- Q2 to Q5: attempt any 3 x 20 marks. These are Flip-flop, Decoder, 8086 program, RISC/CISC, DMA, Microprogrammed CU.
- Total = 100. You need ~60. So: get 30+ in Q1 + 30+ in optionals.

**Exam rule for every answer:** Write formula/steps first, then solve. Diagram is compulsory for theory. Theory-only = 5/10. Diagram + steps + example = full marks.

---
---

# DAY 1 — Q1 40-MARK LOCK

## 1. K-MAP (Karnaugh Map) — *Appears in all 7 papers, ULTRA important*

### Simple idea
Computer has only 0 and 1. You are given a list of combinations where output should be 1. Example: `F(A,B,C,D) = Σ(0,4,8,11,12,13)` means: when ABCD = 0000, 0100, 1000, 1011, 1100, 1101, output F=1. For all other 10 combinations, F=0.
All such combinations together form one big expression like `F = A'B'C'D' + ...` very long and hard.
**K-map makes it short.** You put 0s and 1s in a special table of boxes. Then you group 1s to remove same parts. The groups directly give you short `F = ...` (only AND, OR, NOT gates).

Think of it like this: You have 16 friends. 6 of them raise hand (1). K-map lets you find the rule they all share, so you can describe them in short sentence.

### How exam asks (usually 5-6 marks)
- 3+ variables: e.g. `F(A,B,C)=Σ(2,3,4,5)`, `F(A,B,C,D)=Σ(0,4,8,11,12,13)`, `Σ(0,3,5,7,9,10,11,12,15)`
- You must: 1) draw K-map, 2) simplify, 3) draw logic circuit using AND/OR/NOT or NAND gates.

### 5 steps to solve any K-map (learn this)

**Step 1: Count variables.**
- 3 variables (A,B,C) → 2³ = 8 boxes.
- 4 variables (A,B,C,D) → 2⁴ = 16 boxes.

**Step 2: Draw the map in Gray code order (not 0,1,2,3...).**
Order is always: 00, 01, 11, 10. This is the trick — neighbouring boxes differ by only 1 bit, so grouping works.

3-var map:
```
      BC
     00 01 11 10
A=0 | 0  1  1  0
A=1 | 0  1  1  0
```

4-var map:
```
      CD
     00 01 11 10
AB=00| 0  0  0  0
AB=01| 0  0  0  0
AB=11| 0  0  0  0
AB=10| 0  0  0  0
```
Label rows and columns with AB and CD in 00,01,11,10.

**Step 3: Fill 1s where Σ says so, 0s elsewhere.**
Example June 2024: `F(A,B,C)=Σ(2,3,4,5)`
Binary: 2=010 (A=0,B=1,C=0), 3=011, 4=100, 5=101 → fill those 4 boxes with 1.
```
      BC
     00 01 11 10
A=0 | 0  1  1  0
A=1 | 0  1  1  0
```

**Step 4: Group 1s (always sizes 1,2,4,8,16 — never 3,5,6...).** Rules:
- Circle groups of 1,2,4,8. Bigger group = fewer literals = shorter gate circuit, so try biggest first.
- Groups can overlap. A 1 can be in 2 different groups.
- Edges wrap around: left edge joins right edge, top joins bottom. Corners combine all 4 corners into one group of 4.
- 0s break groups. You cannot cover a 0.

In the June 2024 example: the 4 ones form a column group covering `BC=01 and 11` for both A=0 and A=1 → one variable `B` remains common → `F = B`. That's the answer: one wire, no gates needed. This is how simple it can be.

**Step 5: Read each group left to right.**
- For each group, find variables that stay 1 in whole group → include as is (e.g. `A`).
- Variables that stay 0 in whole group → include as `A'` (A-bar).
- Variables that change inside group → drop them (they cancel).
- Join all groups with `+` (OR). Inside a group join with nothing (AND).

Example: group of 2 where A stays 0, B=1, C changes → `A' B`.
FINAL: `F = A' B + ...`

**Step 6: Draw circuit.**
`A' B` means: NOT A, then AND with B. Each `+` term is one AND gate, then OR all together.
For NAND version: remember `A + B = NAND( NAND(A,A), NAND(B,B) )` — many textbooks ask this. If unsure, draw AND-OR-NOT first — examiner accepts it (June 2026 asks for it).

### Common mistakes
- Drawing map in normal 00,01,10,11 order (wrong — must be 00,01,11,10).
- Group of 3 or 6 (not allowed).
- Forgetting wrap-around rule — June 2026 Σ(0,4,8,12...) is exactly a wrap case.
- Drawing circuit but not writing final simplified F.

### Practice (from 2-day plan)
Redo these 3 on blank paper, timed 6 min each:
- June 2026: `Σ(0,4,8,11,12,13)` + AND/OR/NOT diagram
- Dec 2025: `Σ(0,3,5,7,9,10,11,12,15)` + logic circuit
- June 2024: `Σ(2,3,4,5)` + NAND circuit

> K-map = grouping game. If you can group 4 corners, you can do any paper.

---

## 2. CACHE MEMORY — *Appears in all 7 papers*

### Simple idea
CPU is very fast. RAM (main memory) is slow. Cache is a tiny, very fast memory kept *inside near CPU* to store data CPU needs again and again.

Analogy: Book on your table (cache) vs book in cupboard (RAM). Table = fast, small. Cupboard = slow, big.

Cache is divided into **blocks / lines**. Each block holds one chunk of RAM data + a **tag** (which RAM block it is) so CPU knows if it is correct.

3 words you must know:
- **Tag:** The name/label of the block = "Which RAM block is this copy from?"
- **Line/Index:** The slot number in cache = "Where to keep it?"
- **Word offset:** The exact byte inside block = "Which word inside the chunk?"

16-bit address = Tag bits + Line bits + Word bits. Exam asks you to split it.

### How exam asks (5-6 marks)
- Define Direct mapping / 2-way Set-Associative mapping
- Draw diagram (tag+line+word bits + one example)
- Or: memory address = 1024 words, block size = 4, draw cache organisation

### The 3 techniques (in simple words)

**1. Direct Mapping (simplest)**
Rule: Every RAM block has *exactly one* fixed slot in cache. RAM block 10 always goes to cache slot 10. No choice, no searching.
- Fast, cheap, but wasteful: if block 10 is already there and you want block 20 that also maps to slot 10, you must remove 10 (conflict miss).

**2. Associative Mapping (most flexible)**
Rule: Any RAM block can go to any cache slot. All slots open.
- No conflicts, but you must search all slots in parallel. Slow + costly.

**3. Set-Associative (middle ground — EXAM FAVOURITE)**
Rule: Cache slots are grouped into **sets of 2** (for 2-way). RAM block can go to either slot inside its assigned set only.
- Example: blocks 10 and 20 both go to Set 10, but set has 2 slots, so both can live together. Less conflict than Direct, cheaper than fully Associative.
- This is exactly June 2024 Q1: "2-way Set-Associative mapping".

### How to solve Tag/Line/Word numerical — STEP BY STEP

For any question:
1. **Find total cache lines** = Cache size / Block size.
2. **Find line bits** = 2ⁿ ≥ lines. E.g. 8 lines → n=3 bits.
3. **Find word bits** = block size. Block size 4 words → bits = 2 (addresses 00,01,10,11).
4. **Tag bits** = 16 - line bits - word bits (for 16-bit CPU address).
5. **Check:** Tag = 16-3-2 = 11 bits. This means lines numbered 0-7 (3 bits), each line has 4 words (2 bits).

Direct: Line bits split whole address.
2-way Set-Associative: Same maths, but line bits = set bits + 1 bit inside set (since set has 2 slots). Exam gives same numbers, just state "2 slots per set".

**Diagram you must draw:** Start from left: `[ Tag | Line/Set | Word ]` on top, arrows down to cache blocks below. Label every part.

### Solved micro-example
"Cache has 8 lines, block size=4, CPU address 16-bit, Direct mapping."
- lines=8 → line bits = 3
- block size=4 → word bits = 2
- tag = 16-3-2 = 11 bits
Address = `[11-bit Tag][3-bit Line][2-bit Word]`
If address = `1010 0000 0010 0100` (16-bit): Tag=10100000000, Line=001, Word=00 → Block 1, word 0.

### Common mistakes
- Mixing Tag and Line. Tag = which RAM block. Line = where in cache. Tag comes first (leftmost).
- Forgetting to convert block size to bits (4 bytes → 2 bits, 8 bytes → 3 bits).
- Drawing diagram without labels — must label Tag, Line, Word.

### Practice
- June 2026 Direct Cache (6m), June 2024 2-way Set-Associative (5m).
- Drill: Random 16-bit address → split Tag/Line/Word for Direct vs 2-way in <3 min.

---

## 3. INTERRUPT — *Appears in 6/7 papers*

### Simple idea
CPU is busy doing your program. Suddenly a keyboard key is pressed (hardware) or an error happens (software). CPU must **stop current work, handle the urgent thing, then return** to old work without losing anything.

That “handle the urgent thing” is called an **Interrupt Service Routine (ISR)** — a small program already stored in memory to handle that event.

Think of hostel warden: teaching (current program), doorbell rings (interrupt), warden writes down where he stopped, answers door, comes back and continues teaching from same line.

### How exam asks (5-6 marks, always 7 steps)
- "Explain interrupt processing steps"
- "Interrupt-driven I/O with diagram"
- "Interrupt cycle / IVT role"

### The 7 steps — MEMORISE THIS LIST (exam marks = list ticks)

When interrupt occurs:
1. **Finish current instruction** (CPU does not break in middle of one instruction).
2. **Save PC / IP** (address of next instruction) + status/flags in stack/register — so we can return.
3. **Disable further interrupts** (so new interrupt does not disturb this one) — clear IF flag.
4. **Find ISR address** — CPU looks up **IVT (Interrupt Vector Table)** which stores address of ISR for this interrupt number.
5. **Load ISR address into PC** (or load ISR) and jump to ISR.
6. **Execute ISR** (run the small handling program — e.g. read keyboard, finish disk transfer).
7. **Restore PC, flags, registers** + RE-ENABLE interrupts (set IF), then return to main program at saved PC.

Mnemonic: **Finish → Save → Disable → IVT → Fetch ISR → Execute → Restore & Return**

### IVT in simple words
Imagine a phone book. Each page = one interrupt type (keyboard, disk, divide-by-zero). Page stores the address of the small program to run. IVT is that phone book. CPU just opens the book, gets address, jumps there. June 2026 Q5c asks exactly this.

**Interrupt Cycle** (June 2026 Q3v): T1 to T4 — fetch instruction opcode, then check interrupt flag between instructions. If interrupt = 1, go to steps above. (1 page note is enough.)

### Interrupt-driven I/O vs Programmed I/O (Dec 2025 Q3a)
- **Programmed I/O:** CPU keeps asking device "Ready? Ready? Ready?" — wastes 100% time.
- **Interrupt-driven I/O:** CPU does other work. Device rings bell (interrupt) when data ready. CPU stops, reads data, returns. CPU freed.

### Common mistakes
- Forgetting "save PC + flags" and "restore" — examiner always checks these 2.
- No diagram. Draw: CPU ↔ Interrupt Controller ↔ Devices (keyboard, disk) with arrows both ways + ISR in memory.

### Practice
- June 2026 Q1d rewrite all steps + diagram. Time: 6 min. If you can recite 7 steps from memory, you have 6 marks.

---

## 4. FLAG REGISTER + PHYSICAL ADDRESS — *3 papers in a row (Dec 2025, Jun 2025, Jun 2026)*

### Simple idea — Flag Register
Flag register is a special register that stores **status of last operation** — like a dashboard light.
- Did addition overflow? (Overflow Flag OF=1)
- Did result become zero? (Zero Flag ZF=1)
- Did carry happen? (Carry Flag CF=1)
CPU sets/resets these automatically after each calculation. Next instruction (like `JUMP IF CARRY=1`) reads these flags to decide.

### The 9 flags — 1 line each (memorise this table)

| Flag | Full name | Meaning (simple) | When =1? |
|---|---|---|---|
| CF | Carry Flag | Carry came out | Addition overflowed beyond 8/16 bits |
| PF | Parity Flag | Even parity | Number of 1s is even (error check) |
| AF | Auxiliary Carry | Carry from lower half | Low nibble carried to high nibble (BCD use) |
| ZF | Zero Flag | Zero result | Result = 0 |
| SF | Sign Flag | Sign of result | Top bit = 1 (negative in signed) |
| TF | Trap Flag | Single-step debug | CPU stops after each instruction |
| IF | Interrupt Flag | Interrupts allowed | IF=1 allow, IF=0 mask |
| DF | Direction Flag | String direction | DF=0 forward, DF=1 backward |
| OF | Overflow Flag | Signed overflow | Signed answer doesn't fit (e.g. +120 + +9 in 8-bit) |

In exam: **Directly writes 3-4 flags with 1-line meaning = full marks.** June 2026 asks 3 flags, Dec 2025 asks 4 flags + "can it be GPR?". Answer: No, special register, not General Purpose.

### Simple idea — Physical Address (8086 Segment:Offset)
8086 memory is huge, but CPU uses 16-bit addressing. To make 20-bit address, it uses **Segment + Offset**:
`Physical Address = Segment × 16 + Offset` (in decimal, or Segment shift left by 4 + Offset in hex)

Think of it like: Segment = building number, Offset = flat number. Segment starting address + offset inside building = full address.

In 8086: CS:IP = Code Segment:Instruction Pointer, SS:SP = Stack Segment:Stack Pointer, DS:Offset = Data Segment:Offset.

### Solved example (Dec 2025 Q5c style)
`CS:IP = 0FABh : 01FAh`
Physical = 0FAB0h + 01FAh = 10A... let's do it:
0FABh × 10h = 0FAB0h
0FAB0h + 01FAh = 0FAAAh? Let's add slowly:
```
  0FAB0h
+ 01FAh
= 105AAh  (FAB0 + 01FA = 105AA — show hex addition steps in exam, step marks!)
```
Do same for SS:SP=1F0Ah:0267h → 1F0A0h+0267h=1F307h, DS:A11Ah:0565h → A11A0h+0565h=A16... → A1705h.

**Always show hex addition column-wise in exam.** That earns steps even if final wrong.

### Common mistakes
- Forgetting ×16 = add one 0 in hex (0FABh → 0FAB0h).
- Adding columns right to left, not showing carry.
- Writing flags without "when =1" — 1 line is required.

### Practice
- Do 3 physical addresses daily, always hex addition shown.
- Write 9 flags table from memory 3 times — takes 2 min.

---

## 5. ADDRESSING MODES — *Appears in all 7 papers, 5-10 marks, BIG diagram*

### Simple idea
When CPU needs a value (operand), where does it get it from? There are many places:
- Value is already in register → don't go to memory (fast)
- Value is in memory at a known address → fetch it
- Value is in memory but address itself is inside register, or in another memory location…

Each way of finding the operand is an **addressing mode**. Think of many ways to reach office: direct bus, car with driver, auto rickshaw, painted address + landmark...

### The 8 modes — simple definition + example

1. **Immediate Mode**
   Operand is inside the instruction itself. `MOV AX, 50` → 50 is directly in instruction. No memory access. Fastest.
   Address = instruction itself.

2. **Register Mode**
   Operand is in a register. `MOV AX, BX` → BX already in register. No memory.
   Address = register name.

3. **Register Indirect Mode**
   Register stores *address* of operand. `MOV AX, [BX]` → BX contains address, go to that address in memory to get value.

4. **Direct Mode**
   Address is written directly in instruction. `MOV AX, [1020]` → go to memory address 1020.

5. **Indirect Mode (Memory Indirect)**
   Instruction contains address of address. `MOV AX, [[1020]]` → Address 1020 contains another address, e.g. 2040, then go to 2040 to get value. Double hop.

6. **Based Mode**
   Base register + fixed offset. `MOV AX, [BX+10]` → BX is base (e.g. 1000), +10 → address 1010. Used for arrays starting at BX.

7. **Indexed Mode**
   Index register + fixed offset. `MOV AX, [SI+20]` → SI varies (index), +20 fixed. Used when moving inside array.

8. **Relative Mode**
   PC (Program Counter) + offset. `JUMP +10` → current PC + 10 = target. Used for jumps/loops nearby so nearby code stays together.

**Exam asks only 4-5 modes** — June 2026 asks: Indirect, Relative, Register, Based, Immediate (10m). Dec 2025 asks any 4 with example. June 2024 asks Register Indirect + Relative **with diagram**.

### Diagram style that gets full marks (June 2024 template)
Draw 3 boxes:
- Box 1: **CPU / Register** (show BX, PC value)
- Box 2: **Instruction memory** (show instruction + operand address)
- Box 3: **Data memory** (show final address + value)

With arrows: Instruction → Operand address → Data value. Label "Register holds address" etc.

Example diagram for Register Indirect:
```
PC = 1000
Register BX = 2040 (address)
Memory at 2040 contains 50
Instruction: MOV AX, [BX]  → AX = 50
```

### Common mistakes
- Mixing Direct vs Indirect (Direct = 1 hop, Indirect = 2 hops). Adding diagram fixes it.
- No example — every definition needs `MOV AX, ...` example.
- Writing only 1 line per mode — need **mode + example + diagram** = full marks.

### Practice
- June 2026 Q4a (5 modes, 10m) + June 2024 Q4a diagram style (10m). Copy diagram by hand 3 times until fluent.

---

## 6. NUMBER CONVERSIONS + 2'S COMPLEMENT + IEEE-754

### Simple idea — Number Systems
- **Binary** base 2 digits 0,1 (computer language). Example 101
- **Decimal** base 10 digits 0-9 (our normal)
- **Octal** base 8 digits 0-7
- **Hex** base 16 digits 0-9, A=10, B=11, C=12, D=13, E=14, F=15 (short for binary, 4 bits = 1 hex digit)

Conversion = writing same value in another base.

### 5 conversions from June 2024 Q1b (5 marks, practice all)

1. **873 → Binary:** Keep dividing by 2, note remainders, read bottom to top.
   873/2=436 r1, 436/2=218 r0, 218/2=109 r0, 109/2=54 r1, 54/2=27 r0, 27/2=13 r1, 13/2=6 r1, 6/2=3 r0, 3/2=1 r1, 1/2=0 r1 → 1101101001
   Shortcut memory-based approach also accepted: groups work in exam.

2. **384 → Hex:** Divide by 16. 384/16=24 r0, 24/16=1 r8, 1/16=0 r1 → 180h. Check: 1×256+8×16+0=384 ✓

3. **FAB → Octal:** Each hex digit = 4 bits: F=1111, A=1010, B=1011 → binary 1111 1010 1011 → group in 3 bits from right: 1 111 101 010 11 → 111 101 010 011 = 7 5 2 3 → 7523 octal. (Pad to 3 bits.)

4. **'the escape sequence' → UTF-8:** Unicode. Each basic char like letters, space = 1 byte in UTF-8 (ASCII same). Space = 32 (00100000). Total 20 characters including spaces? Count exact string length × 1 byte each, write hex/decimal of each char. Exam wants concept: UTF-8 = 1-4 bytes, ASCII subset = 1 byte.

5. **765 (octal) → Decimal:** 7×8²+6×8+5×1 = 7×64+48+5 = 448+53=501.

**Rule of thumb for exam:** Write formula first: `(digit × base^position)` — step marks.

### Simple idea — 2's Complement (negatives in computer)
Computer has no minus sign. To store -50, we use 2's complement trick:
```
+50 in 8-bit = 00110010
-50: Flip all bits of +50 → 11001101, then Add 1 → 11001110
```
That's it! To get negative: **1's complement (flip bits) + 1.**

Check: +50 + (-50) = 00110010 + 11001110 = 00000000 with carry discarded = 0 ✓

### Overflow (Dec 2025 Q1c: +120 / +9)
In 8-bit signed, range is -128 to +127. +120+9=129 which is >127 → can't fit → sign bit flips wrong → **Overflow Flag OF=1**. Answer must state overflow occurred.
Formula: If both operands same sign and result sign differs → overflow.

### IEEE-754 (Dec 2025 Q2a, 6 marks)
Floating point format: **Sign (1 bit) | Exponent (8 bits) | Mantissa (23 bits)** for 32-bit.
Exam gives binary like S=0, Exp=10001001, Mantissa=1111..., asks decimal value.
3-step code to write:
1. Sign: 0=positive, 1=negative.
2. Exponent: binary to decimal, then subtract 127 (bias). Exp=10001001 binary = 137 decimal -127 = 10.
3. Mantissa: 1.xxxxx... = 1 + sum(2^-pos × bit). Then Value = sign × 1.mantissa × 2^(exp).
Memorise these 3 steps — even if number wrong, steps = method marks.

### Common mistakes
- Reading binary remainders top-to-bottom instead of bottom-to-top.
- Hex to octal without converting through binary.
- 2's complement forgetting "+1" at end.
- Overflow: not checking range -128 to 127.

### Practice
- June 2024 all 5 conversions (5m) + Dec 2025 +50/-50, +120/+9 with overflow note (5m). Do without calculator.

---

# DAY 2 — OPTIONAL 3×20 LOCK

## 7. MICROPROGRAMMED CONTROL UNIT + FETCH CYCLE MICRO-OPS

### Simple idea
CPU runs a big instruction (like ADD) by doing many tiny steps. Each tiny step = **micro-operation**. Example:
- `DR ← M[AR]` means: "Put content of memory at address in AR into DR register"
- `PC ← PC + 1` means: "Increase Program Counter by 1"

All micro-ops of fetch cycle are like:
1. PC goes to Memory Address Register (**MAR/AR ← PC**)
2. Memory to Data Register (**DR ← M[AR]**)
3. PC increments (**PC ← PC+1**)

**Control Unit (CU)** is the manager telling each part when to do its micro-op. **Microprogrammed CU** stores all micro-ops as a small program in **Control Memory (firmware)**, and a **microprogram sequencer** reads them one by one like PC reads instructions.

Think: Big instruction = book, micro-ops = letters inside book. Control memory = book shelf of all books.

### How exam asks (6-10 marks)
- Draw Microprogrammed CU diagram (Control memory, Microprogram sequencer, Control Address Register CAR, Control Data Register CDR, MAR, DR, PC)
- Write fetch cycle micro-ops
- Difference: Unencoded vs Encoded micro-instructions (June 2026 Q4b, 10m)
- Short note: Wilkes control

### Fetch cycle micro-ops (Dec 2025 Q1f, memorise this sequence)

| Step | Micro-op | Simple meaning |
|---|---|---|
| T1 | `AR ← PC` | Put PC address into AR |
| T2 | `DR ← M[AR]` | Get instruction from memory into DR |
| T3 | `PC ← PC+1` | Move PC to next instruction |
| T4 | Decode DR | Check which instruction it is |

This is the exact 4-step fetch exam expects.

### Unencoded vs Encoded micro-instructions (June 2026 Q4b, 10m)
- **Unencoded:** One bit per micro-op. 50 micro-ops = 50 bits. Simple, fast, but uses lots of memory. (Like giving each friend separate phone.)
- **Encoded:** Uses code. 50 micro-ops = only 6 bits (since 2^6=64). Saves memory but complex, slower to decode.
Diagram: show Control Word with fields. Table compare is enough for 10m.

### Common mistakes
- Diagram without labels (CAR, CDR, Sequencer, Control Memory) = no marks.
- Writing micro-ops in wrong order (AR→PC first, not DR first).

### Practice
- Dec 2025 Q1f diagram + fetch ops (6m) + June 2026 Q2b operation description (6m) + Unencoded/Encoded table.

---

## 8. FLIP-FLOPS + DECODERS

### Simple idea — Flip-Flop = 1-bit memory
A flip-flop can store only **0 or 1** (one bit). It's a switch that stays in last position. 8 flip-flops = 1 byte.

Each type has truth table (inputs → output) and **excitation table** (desired output → what inputs to apply). Exam asks characteristic equation → excitation.

**The 4 types (simple):**

1. **SR Flip-Flop:** Inputs S(set=1), R(reset=0). S=1,R=0 → Q=1. S=0,R=1 → Q=0. S=0,R=0 → Hold (Q stays same). S=1,R=1 → **Forbidden** (not allowed, Q becomes 0 in many designs).

2. **JK Flip-Flop:** Fixes SR forbidden case. S=1,R=1 → **Toggle** (Q flips: 0→1, 1→0). Rest same. Most exam asks **characteristic: Q⁺ = J Q' + K' Q** and excitation table 4 lines.

3. **D Flip-Flop (Delay):** One input D = "Whatever D is, Q becomes D". Q⁺=D. No forbidden case. Used for memory. Short note June 2026 Q3ii.

4. **T Flip-Flop:** Toggle on clock. T=1 flips, T=0 holds. Used in counters.

Diagram you must draw: Boxes with S,R inputs, Clock (C) arrow, Q output, Q' output, truth table inside/next to it.

**Characteristic → Excitation mapping (memorise logic):**
- To go Q=0 → Q=0: J=0,K=x (don't care)
- Q=0 → Q=1: J=1,K=0
- Q=1 → Q=0: J=0,K=1
- Q=1 → Q=1: J=x,K=0
Exam marks this table.

### Simple idea — Decoder
Decoder takes **n inputs** and activates exactly **one of 2ⁿ outputs**. Like a router: 2 input bits (00,01,10,11) → choose out of 4 output lines. **3×8 decoder: 3 inputs → 8 outputs.**

Think: Door bell panel. You press code 010, only bell 2 rings, others silent.

### How exam asks (7-8 marks)
- Draw SR/JK flip-flop + truth table + excitation table
- Draw 3×8 decoder truth table (8 rows) + logic diagram (NAND gates)

### 3×8 Decoder truth table (write this first)
```
A B C | Y0 Y1 Y2 Y3 Y4 Y5 Y6 Y7
0 0 0 | 1  0  0  0  0  0  0  0
0 0 1 | 0  1  0  0  0  0  0  0
0 1 0 | 0  0  1  0  0  0  0  0
... (8 rows, exactly one 1 per row) ...
1 1 1 | 0  0  0  0  0  0  0  1
```

Logic: Each Y = AND of ABC or their NOTs using NAND/NAND gates. Draw NOT for A,B,C then 8 AND/NAND gates.

### Common mistakes
- Flip-flop without clock arrow.
- JK forbidden = toggle, not hold.
- Decoder truth table with more than one 1 per row (means wrong).

### Practice
- Dec 2025 Q2b SR+JK characteristic+excitation (8m) + June 2024 Q2c SR diagram (7m) + 3×8 & 2×4 decoder (8m each). Drill: characteristic → excitation in <2 min.

---

## 9. RISC vs CISC + LARGE REGISTER FILE

### Simple idea — RISC vs CISC
Both are types of computer instruction sets. Difference is **simple few vs many complex instructions**.

- **RISC (Reduced Instruction Set Computer):** Few, simple, same-length instructions. Each does one tiny job very fast. Needs more instructions to do big task, but each is fast. Low power → mobiles, ARM processors.
  Example: ADD, LOAD, STORE only (no MUL directly? etc.)

- **CISC (Complex Instruction Set Computer):** Many, powerful, variable-length instructions. One instruction does big job. Fewer instructions needed, but each takes more time and power. Complex hardware. → Old Intel x86.

Think: RISC = scissors cutting paper strip by strip (many simple steps). CISC = machine that cuts+measures+stitches in one go (complex).

### Compare table (June 2024 Q1e, June 2026 Q4b, Dec 2025 Q1h — memorise 5 rows)

| Point | RISC | CISC |
|---|---|---|
| Instruction set size | Small (few) | Large (many) |
| Instruction length | Fixed (same) | Variable (different) |
| Execution speed per instruction | Fast, 1 clock | Slow, many clocks |
| Power consumption | Low | High |
| Code size | Larger (more instructions) | Smaller (fewer, bigger) |
| Examples | ARM, MIPS | Intel x86, VAX |

Diagram: Dec 2025 asks Large Register File diagram with it.

### Large Register File (short note June 2026 Q3iv)
Normal computer has few registers (AX,BX,CX,DX). Large register file has **many registers** (e.g. 32 registers like in MIPS/RISC) so compiler can keep many values without going to slow memory. More registers = less memory traffic = faster.
Diagram: Array of registers with read/write ports, decoder.

### Common mistakes
- Only 2 rows in table (need 5-6 rows for full marks).
- No example processor names.

### Practice
- Write 1-page compare table + Large Register File diagram from scratch, 5 min each.

---

## 10. DMA vs PROGRAMMED I/O + RAM CELL

### Simple idea — How data comes from devices (keyboard, disk)
CPU needs data from device. Three ways:

**1. Programmed I/O:** CPU asks again and again "Aaya? Aaya?" (polling). 100% busy waiting. Slow, wastes CPU.
Example: CPU reads keyboard by looping: check flag → wait → read.

**2. Interrupt-driven I/O:** CPU works on other task. Device sends interrupt when ready. CPU pauses, reads data, returns. CPU free most time.
Example: Mouse interrupt wakes CPU only when mouse moves.

**3. DMA (Direct Memory Access):** A special DMA controller directly copies data from device to RAM **without involving CPU**. CPU does main work in parallel. DMA borrows memory bus, returns it. Used for big bulk transfer (disk → RAM).
Example: Copying 1MB file from disk — DMA does it, CPU doesn't stop 1M times.

### June 2024 Q3a + Dec 2025 Q3a (8 marks)
Draw block diagram: CPU ↔ Bus ↔ RAM ↔ DMA Controller ↔ Disk/Keyboard.
Table comparison + "When DMA wins: bulk transfer, fast device".

### Simple idea — RAM Cell (June 2026 Q1b, 6 marks)
RAM cell stores 1 bit. There are 2 types:
- **SRAM:** 6 transistors, fast, expensive, needs power to retain (cache). Draw flip-flop based cell.
- **DRAM:** 1 transistor + 1 capacitor, cheap, slow, needs refresh, used as main RAM. Capacitor stores charge (1=charged, 0=empty). Charge leaks, so refresh every few ms.

Diagram: transistors + capacitor + word line + bit line. Label each.

### Practice
- DMA vs Programmed I/O diagram + table (8m) + RAM cell diagram (6m).

---

## 11. 8086 PROGRAM — *Appears in all 7 papers, BUT only 3 templates*

### Simple idea
8086 program is just: `MOV, ADD, LOOP, INT 21h` — write instructions to make CPU do calculation. Exam asks you to write program for: add numbers, convert binary to ASCII, etc. You **don't need to run it** — just write instructions + explain each line = full marks.

Every 8086 program follows **same skeleton**:

```
MOV AX, @DATA        ; load data segment
MOV DS, AX           ; point DS to data
; now use data

MOV CX, 05           ; count = 5 (how many numbers)
LEA SI, NUMS         ; SI points to first number (LEA = load address)
MOV AX, 00           ; sum = 0
LOOP_START:
  ADD AL, [SI]       ; add byte at SI to AL
  INC SI             ; move to next number
  LOOP LOOP_START    ; repeat CX times (CX auto decreases)
MOV RESULT, AX       ; store answer

INT 21h              ; end program (in exam, mention)
```

**Change only the operation** inside loop to cover all papers:
- June 2026 Q2a Add 5 byte numbers → AX (use above template)
- Dec 2025 Q5a Binary → ASCII digit: loop 8 times, shift left, AND with 0FH, add 30h to get ASCII '0'-'9' (0=00110000)
  Concept: Binary digit 0/1 → ASCII '0'/'1' by adding 30h.
- June 2024 Q4c 2-digit ASCII → packed BCD: subtract 30h from ASCII to get digits, multiply by 10 + add second digit.

### The 3 steps examiner checks
1. **Set DS** (MOV AX,@DATA / MOV DS,AX)
2. **Loop with CX + LEA/SI/DX** (pointer to data)
3. **INT 21h** or result store (MOV RESULT, AX)

Missing DS setup = no marks. Always write it.

### Common mistakes
- Forgetting DS setup.
- No comments per line (examiner gives 1 mark per explained line).
- Wrong register size: byte = AL, word = AX.

### Practice
- All 3 programs (8m,8m,5m) using same template. Write program twice: once with data segment declared (`NUMS DB 10,20,30...`).

---

## 12. INSTRUCTION DRILL + FAR/NEAR + .COM/.EXE

### Instructions you must explain with 1 example each (June 2026 Q5b, 10m)

- **ROL (Rotate Left):** Shifts bits left, top bit wraps to bottom, CF = last shifted bit.
  Example: `ROL AX, 1` : 1000 0000 → 0000 0001
- **SHL (Shift Left):** Shifts left, top bit lost, CF = last shifted, 0 comes in bottom.
  Example: `SHL AX, 1` : 1000 0000 → 0000 0000, CF=1
- **XCHG (Exchange):** Swaps contents of two registers. `XCHG AX, BX` → AX↔BX swapped.
- **DEC (Decrement):** Subtracts 1 from register. `DEC CX` → CX = CX-1 (used in LOOP)
- **XOR (Exclusive OR):** Output 1 only if inputs differ. Used to zero a register fast: `XOR AX,AX` → AX=0. Also for parity.

Write **instruction + what it does + example + result**. That's full marks.

### FAR vs NEAR (June 2026 Q1f, 5m)
- **NEAR call/jump:** Same segment (CS same). Only offset changes. Default: `CALL NEAR PTR` / `JMP Label` (near)
- **FAR call/jump:** Different segment. Address = segment:offset (32-bit). `CALL FAR PTR Proc` / `JMP FAR PTR [addr]`
Diagram: Same CS block vs different CS block. 1 page note.

### .COM vs .EXE (Dec 2025 Q4b, 6m)
- **.COM file:** Small (<64KB), single segment, code+data+stack in same segment, no header. Simple, fast to load.
- **.EXE file:** Larger (>64KB), multiple segments, has header with relocations info, code/data/stack separated. Complex, flexible.

Table: size, segments, header, loading.

### Tier-3 1-liners (don't waste time)
- **CRT:** Old monitor with electron gun + phosphor screen (June 2026 Q3 short note, 1 para max)
- **Video cards:** Converts digital image to monitor signals (GPU, VRAM)
- **Cache coherence:** Multiple CPUs sharing cache must keep copies same (MESI)
- **Parallelism:** Doing many tasks at once (pipelining, multiprocessor, multicore)

---

# FINAL CHECKLIST (tick after practising)

- [ ] 3 K-maps: AND/OR/NOT and NAND both fluent
- [ ] 1 Cache Tag/Line/Word split from memory
- [ ] Interrupt 7 steps recited + diagram
- [ ] 9 flags 1-line + 3 physical addresses hex addition
- [ ] 5 addressing modes + June 2024-style diagram
- [ ] Conversions + 2's complement overflow no calculator
- [ ] Microprogrammed CU diagram + fetch ops
- [ ] SR/JK + D flip-flop + 3×8 decoder truth tables
- [ ] RISC/CISC 6-row table + Large Register File diagram
- [ ] DMA vs Programmed I/O + RAM cell diagrams
- [ ] 8086 add-5-numbers template (swap to cover all 3)
- [ ] ROL, SHL, XCHG, DEC, XOR 1 example each + FAR/NEAR + .COM/.EXE table
- [ ] June 2026 Q1 timed 30+/40

> **Expected Dec 2026 Q1:** K-map (new Σ) + Direct/Set Cache + Interrupt steps + Addressing modes + Flag register + 1 numerical (Physical addr / IEEE-754 / 2's complement / RAM chips). No conversions-only paper.

*Notes prepared for MCS-202 2-day plan (Nov 10-11). Each topic tied to exact PYQ. Simple-language explanations + solved examples + diagram instructions.*
