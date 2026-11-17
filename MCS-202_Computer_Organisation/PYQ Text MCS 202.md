# MCS-202 — Previous Year Question Papers (Full Text)

Complete text extracted from the 7 official TEE question papers in this repository (June 2023 – June 2026). Source PDFs are in `MCS-202_Computer_Organisation/`.

> **Accuracy note:** Text extracted programmatically from the official PDFs (PyMuPDF). The PDFs contain stray printed-page artifacts like `P. T. O.`, `[ 2 ]`, and paper codes (`A–30/MCS–202`) interleaved in the text; those are part of the original document layout and are preserved. Some mangled fragments (e.g., split numbers, misplaced marks column, the June 2025 Boolean expression, and some math symbols like Σ) are PDF-extraction artifacts of the source file itself — where text was unreadable due to layout, it is marked `⚠`. Cross-check those lines against the original PDF before relying on them.

---

## Table of Contents

1. [June 2023](#june-2023)
2. [December 2023](#december-2023)
3. [June 2024](#june-2024)
4. [December 2024](#december-2024)
5. [June 2025](#june-2025)
6. [December 2025](#december-2025)
7. [June 2026](#june-2026)

---

# June 2023

**MCS-202**
POST GRADUATE DIPLOMA IN COMPUTER APPLICATIONS (PGDCA–NEW)
Term-End Examination
**June, 2023**
**MCS-202 : COMPUTER ORGANISATION**
Time : 3 Hours | Maximum Marks : 100 | Weightage : 70%

**Note :** Question Number 1 is compulsory and carries 40 marks. Attempt any three questions from Question No. 2 to Question No. 5.

### 1.
**(a)** Perform the following operations using signed 2’s complement notation of size 8 bits, which includes the sign bit. Also indicate overflow or no-overflow, giving reasons thereof :
*(6 marks)*
  (i) Add – 39 and + 126
  (ii) Subtract – 38 from 90
  (iii) Add –79 and –49

**(b)** Simplify the following function using Karnaugh’s map :
*(5 marks)*
`F(A, B, C, D) = Σ (5, 6, 8, 11, 13, 14, 15)`
Draw the logic circuit for the simplified function.

**(c)** Explain the Direct Cache mapping scheme with the help of an example.
*(5 marks)*

**(d)** What is an interrupt ? List all the steps that are required to be performed by hardware or software to process an interrupt.
*(5 marks)*

**(e)** Explain the steps required to process Branch (BR) instruction, subroutine call and return instruction of a computer which uses a stack for storing the return address. You may assume the necessary registers required for this purpose.
*(5 marks)*

**(f)** Explain the horizontal and vertical micro-instructions with the help of a suitable diagram.
*(5 marks)*

**(g)** Explain the following instructions of 8086 microprocessor with the help of an example :
*(4 marks)*
  (i) SHL
  (ii) RCL

**(h)** Write a 8086 assembly language program to find the largest value in an array consisting of 5 values. You may assume that these values are stored in the memory. The largest value may be kept in AX register. Make suitable assumptions.
*(5 marks)*

### 2.
**(a)** Perform the following conversions :
*(5 marks)*
  (i) (225)₁₀ ⚠ *(extraction: destination base garbled in PDF text)*
  (ii) (AAA)₁₆ to hexadecimal ⚠ *(layout artifact in PDF)*
  (iii) (6761)₈ to octal ⚠
  (iv) (ABC)₁₆ to hexadecimal ⚠
  (v) (225)₈ to decimal ⚠

**[Original PDF rendering]**
```
(i)   (225)10
(ii)  (AAA)   to hexadecimal
              16
(iii) (6761)  to octal
              8
(iv)  (ABC)   to hexadecimal
              16
(v)   (225)   to decimal
      8 to decimal
```

**(b)** Explain the functions of the components of a central processing unit with the help of a diagram.
*(5 marks)*

**(c)** Draw the truth table and logic diagram of a 4 × 1 multiplexer and explain its functioning.
*(5 marks)*

**(d)** Draw the logic diagram of a ripple counter and explain its functioning.
*(5 marks)*

### 3.
**(a)** Explain the structure of magentic disk *(typo preserved from original)* with the help of a diagram. Also, explain the term constant angular velocity (CAV) in this context.
*(5 marks)*

**(b)** Explain the concept of memory interleaving with the help of an example.
*(4 marks)*

**(c)** What is the role of Input/Output interfaces ? Explain.
*(5 marks)*

**(d)** Explain the following terms in the context of Input/Output technologies :
*(6 marks)*
  (i) Refresh rate
  (ii) Optical resolution
  (iii) Impact printers

### 4.
**(a)** Explain the following addressing schemes with the help of an example for each :
*(6 marks)*
  (i) Immediate addressing
  (ii) Direct addressing
  (iii) Register addressing

**(b)** Explain the microoperations required for Fetching an Instruction (FI). You may assume suitable registers for this.
*(5 marks)*

**(c)** Explain the working of a Wilke’s *(typo preserved, = Wilkes)* control-unit with the help of a diagram.
*(5 marks)*

**(d)** Explain any four differences between the RISC and CISC machines.
*(4 marks)*

### 5.
**(a)** Compute the physical address in 8086 microprocessor for the following pairs : (all values are in hexadecimal)
*(6 marks)*
  (i) CS : IP ≡ 10FFh : 0111h
  (ii) DS : BX ≡ 0322h : 20FFh
  (iii) SS : SP ≡ 0111h : 2222h

**(b)** Explain the differences between .COM programs and .EXE programs, in the context of Assembly language, with the help of an example.
*(5 marks)*

**(c)** Write a program in 8086 assembly language to interchange the values of two byte locations in the memory.
*(5 marks)*

**(d)** Explain the concept of FAR and NEAR procedures in 8086 assembly language.
*(4 marks)*

---

# December 2023

**MCS–202**
POST GRADUATE DIPLOMA IN COMPUTER APPLICATIONS (PGDCA–NEW)
Term-End Examination
**December, 2023**
**MCS-202 : COMPUTER ORGANISATION**
Time : 3 Hours | Maximum Marks : 100 | Weightage : 70%

**Note :** Question Number 1 is compulsory and carries 40 marks. Attempt any three questions from Question No. 2 to Question No. 5.

### 1.
**(a)** Perform the following operations using signed 2’s complement notation of 8-bits, (including the sign bit). You must indicate overflow or no-overflow and the reasons thereof :
*(6 marks)*
  (i) Add + 69 and + 59
  (ii) Subtract 90 from – 38
  (iii) Add – 76 and + 86

**(b)** Simplify the following function using Karnaugh’s map :
*(5 marks)*
`F(A, B, C, D) = Σ (2, 3, 6, 7, 9, 10, 11, 12, 15)`
Draw the logic diagram of the simplified function using AND, OR and NOT gates.

**(c)** What is the need of Cache memory ? Explain the associative mapping scheme of Cache memory with the help of an example.
*(5 marks)*

**(d)** Explain with the help of a flowchart how Interrupt-driven Input/Output technique is used to perform input function.
*(5 marks)*

**(e)** Explain the following addressing modes with the help of one example each :
*(6 marks)*
  (i) Register indirect addressing
  (ii) Base register addressing
  (iii) Direct addressing

**(f)** What is instruction pipelining ? Explain with the help of a diagram.
*(4 marks)*

**(g)** What are the segment registers in 8086 microprocessor ? Explain their uses with the help of an example.
*(4 marks)*

**(h)** Write a program in 8080 assembly language that finds the largest of two byte numbers stored in the memory. The program then subtracts smaller number from the larger number. The result is left in AX register.
*(5 marks)*

### 2.
**(a)** Explain the Von-Neumann architecture. How is it different than the Harward *(typo preserved, = Harvard)* architecture ?
*(5 marks)*

**(b)** Explain different components of a floating point number. How are they different than the fixed point numbers ?
*(5 marks)*

**(c)** Draw the S-R latch using NOR gates and explain its functioning. Also make the characteristic table of S-R flip-flop.
*(5 marks)*

**(d)** Draw the truth table and block diagram for synchronous counter. Explain its functioning.
*(5 marks)*

### 3.
**(a)** Explain the term access time in the context of a hard disk. Also differentiate between CLV and CAV in the context of secondary storage technologies.
*(5 marks)*

**(b)** Explain the set-associative cache mapping scheme.
*(6 marks)*

**(c)** What is DMA ? Explain the structure of DMA module with the help of a block diagram.
*(5 marks)*

**(d)** Explain the following terms in the context of Input/Output technologies :
*(4 marks)*
  (i) Colour depth
  (ii) Non-impact printers

### 4.
**(a)** Explain the steps of subroutine call and return instructions with the help of an example. Assume suitable register set.
*(4 marks)*

**(b)** What is a micro-operation ? Explain register-transfer, arithmetic and logic micro-operations with the help of an example.
*(7 marks)*

**(c)** Explain the features of RISC processors.
*(4 marks)*

**(d)** Explain the operations of micro-programmed control unit with the help of a block diagram.
*(5 marks)*

### 5.
**(a)** Explain the following in the context of 8086 microprocessor :
*(15 marks)*
  (i) Bus interface unit
  (ii) Tools for assembly language programming
  (iii) Interrupt processing in 8086 micro-processor

**(b)** Write a program in 8086 assembly language that converts an ASCII digit stored in a memory location into its equivalent binary.
*(5 marks)*

---

# June 2024

**MCS–202**
POST GRADUATE DIPLOMA IN COMPUTER APPLICATIONS (PGDCA-NEW)
Term-End Examination
**June, 2024**
**MCS-202 : COMPUTER ORGANISATION**
Time : 3 Hours | Maximum Marks : 100 | Weightage : 70%

**Note :** Question No. 1 is compulsory and carries 40 marks. Attempt any three questions from the remaining Question No. 2 to Question No. 5.

### 1.
**(a)** Explain Harvard architecture with the help of a diagram.
*(5 marks)*

**(b)** Perform the following conversions :
*(5 marks)*
  (i) Decimal (873)₁₀ to Binary
  (ii) Decimal (384)₁₀ to Hexadecimal
  (iii) Hexadecimal (FAB)₁₆ to Octal
  (iv) ASCII string ‘the escape sequence’ to UTF8
  (v) Octal (765)₈ to Decimal

**(c)** Differentiate between CLV and CAV type of disk organizations.
*(5 marks)*

**(d)** Explain two-way set associative Cache mapping with a suitable example.
*(5 marks)*

**(e)** Differentiate between RISC processor and CISC processor. Give utility of each.
*(5 marks)*

**(f)** What is an interrupt ? Explain the use of interrupt in input/output with the help of an example.
*(5 marks)*

**(g)** List the various register categories involved with 8086 microprocessor. Also, give the role of each type of register category.
*(5 marks)*

**(h)** Compare direct addressing mode and indirect addressing mode. Give example for each.
*(5 marks)*

### 2.
**(a)** Simplify the function :
`F(A, B, C) = Σ (2, 3, 4, 5)`
using k-map. Also, draw the circuit using NAND gates.
*(5 marks)*

**(b)** Explain the functioning of 2×4 decoder. Draw its truth table and explain its logic diagram with the help of example input.
*(8 marks)*

**(c)** Explain the working of SR flip-flop with the help of a logic diagram and characteristic table. Also, explain the excitation table of SR flip-flop.
*(7 marks)*

### 3.
**(a)** Explain the concept of programmed I/O. How is Direct Memory Access (DMA) technique differ from programmed I/O technique ? Under what situation is it better to use DMA over programmed I/O ?
*(8 marks)*

**(b)** Define disk access time. Write the equation to compute disk access time. Also, discuss the meaning of all the parameters involved in the computation of disk access time.
*(7 marks)*

**(c)** What are Charge-Coupled Devices (CCDs) ? Briefly discuss the utility of CCDs.
*(5 marks)*

### 4.
**(a)** Explain the following addressing modes, with the help of a suitable diagram (showing content of sample memory and registers) :
*(10 marks)*
  (i) Register Indirect Addressing
  (ii) Relative Addressing
**Note :** Your diagram should include instructions, operands and addresses.

**(b)** What is a micro-operation ? Explain register transfer micro-operation with a suitable example.
*(5 marks)*

**(c)** Write a program in 8086 assembly language, which converts a two digit ASCII number to a packed BCD number. Explain each step of the program.
*(5 marks)*

### 5.
Write short notes on the following :
*(5×4=20 marks)*
  (i) Cache coherence
  (ii) Parallelism in uniprocessor systems
  (iii) .Com programs and .Exe programs
  (iv) Wilkes control

---

# December 2024

**MCS–202**
POST GRADUATE DIPLOMA IN COMPUTER APPLICATIONS (PGDCA—NEW)
Term-End Examination
**December, 2024**
**MCS–202 : COMPUTER ORGANIZATION**
Time : 3 Hours | Maximum Marks : 100 | Weightage : 70%

**Note :** Question No. 1 is compulsory and carries 40 marks. Attempt any three questions from the remaining question no 2 to question no. 5.

### 1.
**(a)** Explain Von Neumann Architecture with the help of a diagram.
*(5 marks)*

**(b)** Perform the following conversions :
*(5 marks)*
  (i) Decimal (384)₁₀ to Binary
  (ii) Decimal (873)₁₀ to Hexadecimal
  (iii) Hexadecimal (B1D)₁₆ to Octal
  (iv) ASCII string “ASCII to UTF” to UTF 8
  (v) Octal (670)₈ to Decimal

**(c)** Differentiate between SRAM and DRAM.
*(5 marks)*

**(d)** Explain Associative cache mapping with the help of an example.
*(5 marks)*

**(e)** What is the need of RISC processor ? How large register file in RISC is useful for procedure calls ? Explain with the help of a diagram.
*(5 marks)*

**(f)** What is DMA ? How does DMA differ from I/O processor ? Explain the importance of DMA with the help of a diagram.
*(5 marks)*

**(g)** What is interrupt 21h in the context of 8086 microprocessor ? Explain the use of interrupt 21h, with the help of an example.
*(5 marks)*

**(h)** What are segment registers ? Discuss the utility of all four segment registers of 8086 microprocessor.
*(5 marks)*

### 2.
**(a)** Simplify the function `F(A, B, C) = ∑(0, 1, 3, 4, 5, 6)` using k-map. Also, draw the circuit using NAND gates.
*(5 marks)*

**(b)** Explain the functioning of 3×1 multiplexer. Draw its truth table and explain its logic diagram with the help of an example input.
*(8 marks)*

**(c)** Explain the working of J-K flip-flop with the help of logic diagram and characteristic table. Also, explain the excitation table of J-K flip-flop.
*(7 marks)*

### 3.
**(a)** Explain the concept of Programmed I/O. How does programmed I/O technique differ from interrupt driven I/O ? Under what situations, it is better to use programmed I/O over interrupt driven I/O ?
*(8 marks)*

**(b)** What is the aim of disk scheduling algorithm ? Briefly discuss the following disk scheduling algorithms :
*(7 marks)*
  (i) FCFS
  (ii) SSTF
  (iii) SCAN
  (iv) C-SCAN
  (v) LOOK

**(c)** What are Solid State Devices (SSD) ? How do SSD differ from HDD ?
*(5 marks)*

### 4.
**(a)** Explain the following addressing modes, with the help of suitable diagram (showing content of sample memory and registers) :
*(10 marks)*
  (i) Index Addressing
  (ii) Base Register addressing
**Note :** Your diagram should include instructions, operands and addresses.

**(b)** Explain the working of microprogrammed control unit with the help of a suitable diagram.
*(10 marks)*

### 5.
**(a)** Write a program using 8086 assembly language that adds two binary numbers (assume the numbers are of byte type) stored in consecutive memory locations. The result of the addition and carry, if any are also stored in memory locations. Also explain its each step of execution.
*(5 marks)*

**(b)** Write short notes on following :
*(3×5=15 marks)*
  (i) Instruction pipeline
  (ii) Multiprocessor
  (iii) Multiport memory

---

# June 2025

**MCS–202**
POST GRADUATE DIPLOMA IN COMPUTER APPLICATIONS (PGDCA–NEW)
Term-End Examination
**June, 2025**
**MCS-202 : COMPUTER ORGANIZATION**
Time : 3 Hours | Maximum Marks : 100 | Weightage : 70%

**Note :** Question No. 1 is compulsory and carries 40 marks. Attempt any three questions from Q. No. 2 to Q. No. 5.

### 1.
**(a)** Write the binary equivalent for the following decimal numbers :
*(6 marks)*
  (i) –23456
  (ii) 299
  (iii) 17.89

**(b)** Explain the importance of locality of reference with the help of an example.
*(5 marks)*

**(c)** What is the role of a ‘flag’ register in 8086 microprocessor ? Can it be used as a general purpose register ?
*(5 marks)*

**(d)** List and explain any four data transfer instructions of a computer.
*(4 marks)*

**(e)** Add the following decimal numbers by converting them to 8 bit signed 2’s complement notation :
*(4 marks)*
  (i) + 56 and – 56
  (ii) + 121 and + 8

**(f)** What is an I/O interface ? List major functions of I/O interface.
*(4 marks)*

**(g)** With the help of a block diagram, explain the concept of Direct Memory Access (DMA).
*(4 marks)*

**(h)** Write an 8086 assembly program that interchanges the values of two memory locations.
*(4 marks)*

**(i)** How are characters recognised by voice-based input devices ?
*(4 marks)*

### 2.
**(a)** Simplify the function :
*(5 marks)*
**[Original PDF rendering — math layout garbled in PDF text layer]**
```
A +B
A.B
f
        ( ) ( )
            ′ ′ ′
```
⚠ The expression is a Boolean simplification problem rendered in scattered math symbols in the PDF. Cross-check against the original PDF page 4. It approximates: f = [A′·(A·B)′ + B′] / (A+B) — verify visually.

**(b)** Define SOP and POS form of Boolean functions with the help of an example of each.
*(5 marks)*

**(c)** What is a flip-flop ? How is it different from a latch ? Also, explain the working of the following flip-flops along with necessary diagrams :
*(10 marks)*
  (i) Master-Slave flip-flop
  (ii) Edge-Triggered flip-flop

### 3.
**(a)** Assume that a computer system has the following memories :
*(6 marks)*
  (i) RAM 64 words with 16-bits word.
  (ii) Cache of 8 blocks (block size – 32 bits).
Find in which location of Cache memory a decimal address ‘21’ can be found if direct mapping is used.

**(b)** List the advantages and disadvantages of Associative Memory.
*(4 marks)*

**(c)** Explain how RAID technology enhances the performance and reliability of data storage. Also, summarize the characteristics of any three RAID-levels.
*(10 marks)*

### 4.
**(a)** Explain the role of the following types of registers :
*(6 marks)*
  (i) General purpose register
  (ii) Address register
  (iii) Data register

**(b)** With the help of a block diagram, explain the fixed-point arithmetic logic unit.
*(8 marks)*

**(c)** Explain the process of execution of a micro-program.
*(6 marks)*

### 5.
Write short notes on the following :
*(4×5=20 marks)*
  (a) Indirect Addressing Mode
  (b) COM Program
  (c) Dynamic Random Access Memory (DRAM)
  (d) Von Neumann Architecture

---

# December 2025

**MCS–202**
POST GRADUATE DIPLOMA IN COMPUTER APPLICATIONS (PGDCA–NEW)
Term-End Examination
**December, 2025**
**MCS-202 : COMPUTER ORGANIZATION**
Time : 3 Hours | Maximum Marks : 100 | Weightage : 70%

**Note :** Question No. 1 is compulsory and carries 40 marks. Attempt any three questions from Q. No. 2 to Q. No. 5.

### 1.
**(a)** Discuss the need of Control unit, Arithmetic logic unit memory and I/O devices in any computer system.
*(6 marks)*

**(b)** Differentiate between Multiprocessor and Multicore processor.
*(4 marks)*

**(c)** Add the following decimal numbers by converting them to 8-bit signed 2’s complement notation. Also indicate overflow, if any :
*(5 marks)*
  (i) + 50 and – 50
  (ii) + 120 and + 9

**(d)** Simplify the following function using K-map :
`F(A, B, C, D) = Σ (0, 3, 5, 7, 9, 10, 11, 12, 15)`
and draw the logic circuit of the function so obtained.
*(5 marks)*

**(e)** How many RAM chips of size 256 K × 4 bit are required to build 1 M byte of memory ?
*(5 marks)*

**(f)** Considering that a computer has Program Counter (PC), Instruction Register (IR), Data Register (DR) and a Memory Address Register (MAR), write the microoperations for fetch cycle of an instruction on this computer.
*(5 marks)*

**(g)** What is the role of flag register in 8086 microprocessor ? Can it be used as a general purpose register ? Give the uses of any four flags.
*(5 marks)*

**(h)** Explain the use of large register file in RISC architecture with the help of a diagram.
*(5 marks)*

### 2.
**(a)** A number using IEEE 754 (32 bit) is given. What is the equivalent decimal value ?
*(6 marks)*

| Sign bit (S) | Exponent of length 8 bits | Significant / Mantissa of length 23 bits (M) |
|---|---|---|
| 0 | 1000 1001 | 111 1000 0000 0000 0000 0000 |

**(b)** What is an excitation table ? Draw the characteristic table and excitation table for S-R and J-K flip-flops.
*(8 marks)*

**(c)** Write the differences between the following :
*(6 marks)*
  (i) LCD and LEDs
  (ii) Impact printers and Non-impact printers

### 3.
**(a)** What is an Interrupt ? Explain interrupt driven I/O technique with the help of a diagram.
*(6 marks)*

**(b)** Explain instruction pipelining with the help of a diagram.
*(6 marks)*

**(c)** Explain any four addressing modes of 8086 microprocessor with the help of an example of each.
*(8 marks)*

### 4.
**(a)** Explain the functioning of 3 × 8 decoder. Draw its truth table and explain its logic diagram.
*(8 marks)*

**(b)** Differentiate between .com programs and .exe programs.
*(6 marks)*

**(c)** How can interleaved memory be used to improve the speed of main memory access ? Explain with the help of an example/diagram.
*(6 marks)*

### 5.
**(a)** Write a program using 8086 assembly language that converts a binary value stored in a byte location (assume value between 0 to 9) to equivalent ASCII digit.
*(8 marks)*

**(b)** Why is memory hierarchy created in a computer system ? Explain memory hierarchy with the help of a diagram.
*(6 marks)*

**(c)** For the following values of various registers in an 8086 microprocessor, compute the physical memory address :
*(6 marks)*
  (i) CS : IP = 0FABh : 01FAh
  (ii) SS : SP = 1F0Ah : 0267h
  (iii) DS : Offset : A11Ah : 0565h

---

# June 2026

**MCS–202**
POST GRADUATE DIPLOMA IN COMPUTER APPLICATIONS (PGDCA-NEW)
Term-End Examination
**June, 2026**
**MCS-202 : COMPUTER ORGANISATION**
Time : 3 Hours | Maximum Marks : 100 | Weightage : 70%

**Note :**
(i) Question No. 1 is compulsory and carries 40 marks.
(ii) Attempt any three questions from the remaining Question No. 2 to Question No. 5.

### 1.
**(a)** Simplify the following :
`F(A, B, C, D) = Σ (0, 4, 8, 11, 12, 13)`
using K-map. Also draw the logic diagram of resultant function using AND, OR, NOT Gates.
*(6 marks)*

**(b)** Draw and explain the logic diagram of a RAM cell.
*(6 marks)*

**(c)** Explain the direct cache mapping scheme with the help of an example.
*(6 marks)*

**(d)** What is an interrupt ? List all the steps that are required to be performed by hardware or software to process an interrupt.
*(6 marks)*

**(e)** Explain the components of 8086 microprocessor with the help of a diagram.
*(6 marks)*

**(f)** Explain the FAR procedure call in the context of 8086 assembly language.
*(5 marks)*

**(g)** What is the role of Flag register in 8086 microprocessor ? Explain the role of any three flags in this register.
*(5 marks)*

### 2.
**(a)** Write an 8086 assembly language program to add five byte numbers stored in an array in the memory. The result should be stored in AX register.
*(8 marks)*

**(b)** Draw a general configuration of micro-programmed control unit and discuss its operation.
*(6 marks)*

**(c)** What are Adders ? Explain half adder and full adder with logic diagram and truth tables.
*(6 marks)*

### 3.
Explain the following by giving one example or diagram for each :
*(5×4=20 marks)*
  (i) CRT
  (ii) D-flip-flop
  (iii) Video cards
  (iv) Register file in RISC
  (v) The Interrupt Cycle

### 4.
**(a)** Explain the following addressing modes in assembly language programming with the help of an example for each :
*(10 marks)*
  (i) Indirect Addressing
  (ii) Relative Addressing
  (iii) Register Addressing
  (iv) Based Addressing
  (v) Immediate Addressing

**(b)** Differentiate the following :
*(10 marks)*
  (i) RISC vs. CISC
  (ii) Unencoded micro-instructions vs. Encoded micro-instructions

### 5.
**(a)** Explain the role of party bit *(typo preserved, = parity bit)* in error detection with the help of an example.
*(5 marks)*

**(b)** Explain the following instructions of 8086 microprocessor with the help of one example each :
*(10 marks)*
  (i) ROL
  (ii) SHL
  (iii) XCHG
  (iv) DEC
  (v) XOR

**(c)** What is the role of Interrupt Vector Table (IVT) in 8086 processor ? Explain.
*(5 marks)*

---

*Extracted from `MCS-202_Computer_Organisation/*.pdf` (official IGNOU TEE papers) — 2026-11-10.*
