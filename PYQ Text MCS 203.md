# MCS-203 — Previous Year Question Papers (Full Text)

Complete text extracted from the 7 official TEE question papers in this repository (June 2023 – June 2026). Source PDFs are in `MCS-203_Operating_Systems/`.

> **Accuracy note:** Text extracted programmatically from the official PDFs (PyMuPDF). Printed-page artifacts like `P. T. O.`, `[ 2 ]`, and paper codes (`A–31/MCS–203`) were interleaved in the PDF text layer; they are not part of the questions and have been reduced to cleaner layout here. Where a sentence was split across printed-page boundaries, it is shown complete with no content dropped. The process/arrival/burst tables scattered across PDF lines are restored as tables. Source typos are preserved (marked). Only TWO genuinely garbled spots exist in the whole set and they are marked `⚠` — cross-check those against the original PDF.

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

**MCS-203**
POST GRADUATE DIPLOMA IN COMPUTER APPLICATIONS (PGDCA) (NEW)
Term-End Examination
**June, 2023**
**MCS-203 : OPERATING SYSTEMS**
Time : 3 Hours | Maximum Marks : 100 | Weightage : 70%

**Note :** (i) Question no. 1 is compulsory. (ii) Attempt any three questions from the rest.

### 1.
**(a)** Define a Semaphore. List and explain the two standard atomic operations of it. Also write the solution to producer-consumer problem using semaphores and explain.
*(10 marks)*

**(b)** Using SSTF and C-SCAN disk scheduling algorithms, calculate the total head movement for the following block sequence :
*(10 marks)*
`61, 141, 40, 160, 15, 63, 60, 125`
**Note :** Initially the head is at cylinder numbered 0.

**(c)** Define segmentation. Explain with the help of a diagram, the address mapping scheme used in segmentation.
*(10 marks)*

**(d)** With the help of a diagram, explain the fundamental architecture of LINUX operating system.
*(10 marks)*

### 2.
**(a)** For the reference string as shown below :
`0, 1, 3, 4, 6, 4, 3, 9, 6, 4` — and with 3 memory frames, calculate the number of page faults using OPT and FCFS page replacement algorithms.
*(10 marks)*

**(b)** Write and explain "Banker's algorithm" for Deadlock Avoidance proposed by Dijkstra.
*(10 marks)*

### 3.
**(a)** List and explain the design issues involved in distributed systems.
*(10 marks)*

**(b)** With the help of a diagram, explain "Distributed Shared Memory" application model.
*(10 marks)*

### 4.
**(a)** Describe multiprocessor OS functions and requirements. With respect to synchronization in multiprocessors, explain test-and-set, compare-and-swapes *(typo preserved from original, = compare-and-swaps)* and fetch-and-add techniques.
*(10 marks)*

**(b)** Write briefly about the following types of processors used in mobile devices :
*(10 marks)*
  (i) Qualcomm Snapdragon
  (ii) Intel Atom Processor

### 5.
Write short notes on any four of the following :
*(4×5=20 marks)*
  (a) Design issues in Mobile OS
  (b) File system management in Windows 10
  (c) Security features in LINUX
  (d) Memory management in Android
  (e) iOS directories and iCloud container of iOS

---

# December 2023

**MCS–203**
POST GRADUATE DIPLOMA IN COMPUTER APPLICATIONS (PGDCA) (NEW)
Term-End Examination
**December, 2023**
**MCS-203 : OPERATING SYSTEMS**
Time : 3 Hours | Maximum Marks : 100 | Weightage : 70%

**Note :** (i) Question No. 1 is compulsory. (ii) Attempt any three questions from the rest.

### 1.
**(a)** Consider the following set of processes (P1, P2, P3, P4, P5) with the length of the CPU burst time given in milliseconds along with the arrival time :

| Process | Arrival Time | CPU Burst Time |
|---|---|---|
| P1 | 1 | 6 |
| P2 | 2 | 4 |
| P3 | 4 | 1 |
| P4 | 3 | 2 |
| P5 | 5 | 3 |

Draw Gantt charts illustrating the execution of the processes using FCFS, SJF and RR (with quantum = 2) scheduling algorithms. Also find the average turn around time, average waiting time, processor utilization and throughput for all the algorithms.
*(10 marks)*

**(b)** Following is the sequence of page requests :
`1, 3, 2, 4, 3, 1, 4, 5, 2, 1, 3`
Assume that there are three frames. How many page faults will occur if the following algorithms are used to replace the pages ?
*(10 marks)*
  (i) Least Recently Used (LRU)
  (ii) First Come First Serve (FCFS)

**(c)** Define a semaphore. Using semaphores, write and explain the algorithm that solves the Reader's and Writer's problem.
*(10 marks)*

**(d)** Discuss the security features in LINUX with respect to the following :
*(10 marks)*
  (i) User Accounts
  (ii) File Permissions
  (iii) Encrypted Storage
  (iv) Remote Access

### 2.
**(a)** There are three main alternative ways to structure a distributed application as shown below :
*(10 marks)*
  (i) Client/Server (and RPC)
  (ii) Distributed objects
  (iii) Distributed shared memory
Explain all the three models with the help of block diagrams respectively.

**(b)** Discuss the following mechanisms/techniques suitable for synchronization in multiprocessors :
*(10 marks)*
  (i) Test-and-set
  (ii) Compare-and-swap

### 3.
**(a)** Describe the evolution of iOS. Also, discuss the features of iOS operating system.
*(10 marks)*

**(b)** Explain the process management and process scheduling in Windows-10.
*(10 marks)*

### 4.
**(a)** With reference to wireless communication, explain the following 'two-unit configuration' ways of device communication :
*(10 marks)*
  (i) Infrared connection
  (ii) Bluetooth connection
  (iii) Near Field Communication (NFC)
Also mention the drawbacks, if any, with the 'two-unit configuration' model/technique.

**(b)** Explain the memory management in Android Operating System.
*(10 marks)*

### 5.
Write short notes on the following :
*(4×5=20 marks)*
  (a) Demand segmentation
  (b) Deadlock avoidance
  (c) Windows vs. Linux operating system
  (d) Remote Procedure Call (RPC)

---

# June 2024

**MCS-203**
POST GRADUATE DIPLOMA IN COMPUTER APPLICATIONS (PGDCA–NEW)
Term-End Examination
**June, 2024**
**MCS-203 : OPERATING SYSTEMS**
Time : 3 Hours | Maximum Marks : 100 | Weightage : 70%

**Note :** (i) Question No. 1 is compulsory. (ii) Attempt any three questions from the rest.

### 1.
**(a)** Characterize a deadlock in a system. Using a resource allocation graph, illustrate a deadlock.
*(10 marks)*

**(b)** Discuss the design goals and design issues in a distributed system.
*(10 marks)*

**(c)** With the help of a block diagram, explain the iOS-layered architecture with a focus on essential functions of all the layers.
*(10 marks)*

**(d)** With reference to memory management in Windows-10 operating system, explain the following :
*(10 marks)*
  (i) Virtual Memory Organization
  (ii) Demand Paging

### 2.
**(a)** Discuss the file management and security features in Android operating system.
*(10 marks)*

**(b)** Elucidate the general design issues for a mobile operating system in detail.
*(10 marks)*

### 3.
**(a)** Write and explain Bakery's algorithm that handles critical section problem for 'n' processes.
*(10 marks)*

**(b)** Write and explain briefly, all the essential functions of an operating system.
*(10 marks)*

### 4.
**(a)** Explain Virtual Memory and its principle of operation, elaborating the virtual to physical address mapping.
*(10 marks)*

**(b)** With the help of a diagram, explain LINUX architecture with a special focus on 'Kernel' and its components.
*(10 marks)*

### 5.
Write short notes on the following :
*(4×5=20 marks)*
  (i) Types of Schedulers (Short-term, Long-term and Medium term)
  (ii) Demand Paging
  (iii) Mutual Exclusion in Distributed Systems
  (iv) Libraries and Application Framework Layers of Android Architecture

---

# December 2024

**MCS–203**
POST GRADUATE DIPLOMA IN COMPUTER APPLICATIONS (PGDCA–NEW)
Term-End Examination
**December, 2024**
**MCS-203 : OPERATING SYSTEMS**
Time : 3 Hours | Maximum Marks : 100 | Weightage : 70%
*(Paper code: B–1065/MCS–203)*

**Note :** (i) Question No. 1 is compulsory. (ii) Attempt any three questions from the rest.

### 1.
**(a)** Explain the significance of disk scheduling. Discuss the Shortest Seek Time First (SSTF) and SCAN scheduling algorithms. Trace the total head movement with SSTF and SCAN scheduling by representing them through a diagram for the following disk queue :
*(10 marks)*
`49, 90, 149, 41, 129, 17, 139, 69, 60`
Assume that the disk head is initially at 49.

**(b)** Define a deadlock. List and explain all the four conditions that are must to create the deadlock situation.
*(5 marks)*

**(c)** Define a mobile operating system and explain the features of iOS.
*(5 marks)*

**(d)** The following is the sequence of page-requests :
`1, 2, 5, 4, 2, 1, 3, 2, 6, 4`
Assume that there are four frames. How many page faults will occur if the following page replacement algorithms are used to replace the pages ?
*(10 marks)*
  (i) First Come First Serve (FCFS)
  (ii) Least Recently Used (LRU)
  (iii) Least Frequently Used (LFU)

**(e)** Write and explain producers-consumers problem. Also, provide the solution for the problem using semaphores.
*(10 marks)*

### 2.
**(a)** What is Interprocess communication ? Explain how it is performed in Windows-10.
*(5 marks)*

**(b)** With the help of a diagram, explain all the main components of LINUX operating system.
*(5 marks)*

**(c)** Discuss the layered architecture of Android OS, with the help of a diagram.
*(10 marks)*

### 3.
**(a)** List and explain the techniques available for synchronization in multiprocessors.
*(10 marks)*

**(b)** Write and explain Lamport's Bakery Algorithm for mutual exclusion in distributed systems.
*(10 marks)*

### 4.
**(a)** List and explain the design issues in mobile operating systems.
*(8 marks)*

**(b)** Define virutal memory *(typo preserved from original, = virtual)* and discuss its principle of operation with the help of a suitable diagram.
*(8 marks)*

**(c)** What is the difference between a loosely coupled system and a tightly coupled system ? Give examples for each.
*(4 marks)*

### 5.
Write short notes on the following :
*(4×5=20 marks)*
  (a) Memory management in LINUX
  (b) Segmentation (memory management scheme)
  (c) Locks (Process synchronization mechanism)
  (d) Some of the commonly used directories in iOS

---

# June 2025

**MCS–203**
POST GRADUATE DIPLOMA IN COMPUTER APPLICATIONS (PGDCA–NEW)
Term-End Examination
**June, 2025**
**MCS-203 : OPERATING SYSTEMS**
Time : 3 Hours | Maximum Marks : 100 | Weightage : 70%
*(Paper code: B–1087/MCS–203)*

**Note :** Question No. 1 compulsory. Attempt any three questions from the rest.

### 1.
**(a)** For the following given 5 processes arrived at the same time in the order with the length of their CPU time in milliseconds :

| Process | Processing Time |
|---|---|
| P1 | 7 |
| P2 | 6 |
| P3 | 9 |
| P4 | 4 |
| P5 | 3 |

calculate the turnaround time, average waiting time, throughput and processor utilization for FCFS, SJF and RR (quantum = 2) scheduling algorithms.
*(10 marks)*

**(b)** Define paging technique. With the help of a diagram, explain the principles of its operation. Also, discuss the hardware support required for paging.
*(10 marks)*

**(c)** Write and explain dining philosopher's problem. Also, provide the solution for the problem using semaphores.
*(10 marks)*

**(d)** With the help of a diagram, explain the layered architecture of iOS.
*(10 marks)*

### 2.
**(a)** Explain Batch processing, Time sharing Real-time and Distributed operating systems with suitable examples.
*(10 marks)*

**(b)** Describe the operating system's view of file management. In this context, explain two-level directory structure, acyclic-graph directory structure and general graph directory structure.
*(10 marks)*

### 3.
**(a)** Discuss the following processes in Android mobile operating system :
*(10 marks)*
  (i) Foreground process
  (ii) Visible process
  (iii) Service process
  (iv) Background process
  (v) Empty process

**(b)** Explain memory management in LINUX with the help of a diagram.
*(10 marks)*

### 4.
**(a)** Write and explain Ricart and Agrawal's mutual exclusion algorithm for distributed systems.
*(10 marks)*

**(b)** In context to multiprocessor operating systems, explain the following types :
*(10 marks)*
  (i) Separate supervisor
  (ii) Master-Slave

### 5.
Write short notes on the following :
*(4×5=20 marks)*
  (a) Demand segmentation
  (b) Deadlock detection and Recovery
  (c) Security features in LINUX
  (d) Rule-based access control and role-based access control security models

---

# December 2025

**MCS–203**
POST GRADUATE DIPLOMA IN COMPUTER APPLICATIONS (PGDCA–NEW)
Term-End Examination
**December, 2025**
**MCS-203 : OPERATING SYSTEMS**
Time : 3 Hours | Maximum Marks : 100 | Weightage : 70%
*(Paper code: A–31/MCS–203)*

**Note :** Question No. 1 compulsory. Attempt any three questions from the rest.

### 1.
**(a)** What do you understand by CPU bound programs and I/0 bound programs *(typo preserved, = I/O bound)* ? What are the various process management functions that are performed by the operating systems ?
*(10 marks)*

> ⚠ **Layout note:** In the PDF, this question's marks (10) and the second half of the sentence appear displaced across the page-2 header break (`[ 2 ] MCS–203 A–31/MCS–203`). Reconstructed above as one complete question — verify against the original PDF page 2.

**(b)** What are Semaphores ? How is the Dining Philosopher problem solved using semaphores ?
*(10 marks)*

**(c)** List and explain design issues involved in Distributed Systems.
*(10 marks)*

**(d)** Explain in detail the process management in WINDOWS 10.
*(10 marks)*

### 2.
**(a)** Consider the following page reference string :
`1, 2, 3, 4, 2, 1, 5, 6, 2, 1, 2, 3, 7, 6, 3, 2, 1, 2, 3, 6.`
How many page faults would occur for the following replacement algorithms, assuming four frames ? Remember all frames are initially empty, so your first unique pages will all cost one fault each :
*(10 marks)*
  (i) LRU replacement
  (ii) FIFO replacement

**(b)** Define a deadlock. How can the deadlock be prevented using Havender's algorithm ?
*(10 marks)*

### 3.
**(a)** Explain the abstract model of virtual address to physical address mapping. Also, explain the use of valid and invalid bits in page table.
*(10 marks)*

**(b)** Consider a disk queue with requests for I/O to blocks on cylinders `47, 38, 121, 191, 87, 11, 92, 10`. The SCAN scheduling algorithm is used. The head is initially at cylinder number 63, moving towards larger cylinder numbers on its servicing pass. The cylinders are numbered from 0 to 199. Find the total head movement (in number of cylinders) incurred while servicing these requests.
*(10 marks)*

### 4.
**(a)** What is Remote Procedure Call (RPC) ? How does it work ? What are the limitations of Remote Procedure Call ?
*(10 marks)*

**(b)** Give the complete layered architecture of iOS. Briefly explain about each layer and their significances.
*(10 marks)*

### 5.
Write short notes on any four of the following :
*(4×5=20 marks)*
  (a) Distributed Mutual Exclusion
  (b) Difference between Processes and Threads
  (c) Symbian Operating Systems
  (d) Memory Management in Linux
  (e) Features of WINDOWS 10 operating systems

---

# June 2026

**MCS–203**
POST GRADUATE DIPLOMA IN COMPUTER APPLICATIONS (PGDCA–NEW)
Term-End Examination
**June, 2026**
**MCS-203 : OPERATING SYSTEMS**
Time : 3 Hours | Maximum Marks : 100 | Weightage : 70%
*(Paper code: A–1040/MCS–203)*

**Note :** (i) Question No. 1 compulsory. (ii) Attempt any three questions from the rest.

### 1.
**(a)** Define the essential properties of the following types of operating systems :
*(10 marks)*
  (i) Batch
  (ii) Interactive
  (iii) Time-sharing
  (iv) Real-Time
  (v) Distributed

**(b)** Consider the following set of processes (P1, P2, P3, P4, P5) with the length of the CPU burst time given in milliseconds along with the arrival time :

| Process | Arrival Time | CPU Burst Time |
|---|---|---|
| P1 | 1 | 4 |
| P2 | 2 | 6 |
| P3 | 3 | 2 |
| P4 | 4 | 5 |
| P5 | 5 | 3 |

Draw Gantt charts illustrating the execution of the processes using FCFS, SRTN (Shortest Remaining Time Next) and RR (with quantum = 2) scheduling algorithms. Also, find the average turn around time, average waiting time, processor utilization and throughput for all the algorithms.
*(10 marks)*

**(c)** What is segmentation ? With the help of a diagram, explain the Address Translation Scheme in Segmentation. Also, explain protection and sharing in this context.
*(10 marks)*

**(d)** Explain Lamport's Distributed Mutual Exclusion Algorithm.
*(10 marks)*

### 2.
**(a)** What is the cause of thrashing ? How does the system detect thrashing ? Once it detects thrashing, what can the system do to eliminate this problem ?
*(10 marks)*

**(b)** Consider six memory partitions of size `200 kB, 400 kB, 600 kB, 500 kB, 300 kB and 250 kB`. These partitions need to be allocated to four processes of sizes `357 kB, 210 kB, 468 kB and 491 kB` in that order.
*(10 marks)*
Perform the allocation of processes using :
  (i) First-fit Algorithm
  (ii) Best-fit Algorithm
  (iii) Worst-fit Algorithm

### 3.
**(a)** There are four processes and two resources in the system. Each resource has two instances. Furthermore :
*(10 marks)*
  (i) P1 acquires an instance of R2, and requests an instance of R1.
  (ii) P2 acquires an instance of R1, and doesn't need any other resource.
  (iii) P3 acquires an instance of R1, and requires an instance of R2.
  (iv) P4 acquires an instance of R2, and doesn't need any other resource.

  (I) Draw the resource allocation graph.
  (II) Is there any cycle in the graph ? If yes, name it.
  (III) Whether the system is in deadlock ? If yes, explain why; if not, provide sequence of execution of processes.

**(b)** How to allocate space to files for effective disk space utilization and quick access using the following methods.
*(10 marks)*
  (i) Continuous allocation
  (ii) Non-continuous allocation

### 4.
**(a)** Briefly explain the Access Matrix Security Model that can possibly be implemented in operating systems with the help of an example.
*(10 marks)*

**(b)** If you have to choose any one between WINDOWS 10 and LINUX operating systems, for your work, then which OS will you go for ? Give five reasons for choosing the same.
*(10 marks)*

### 5.
Write short notes on any four of the following :
*(4×5=20 marks)*
  (a) Remote Procedure Call (RPC).
  (b) Android Libraries.
  (c) Design issues in mobile operating system.
  (d) Kernel Architecture of Linux.
  (e) Distributed Shared Memory.

---

*Extracted from `MCS-203_Operating_Systems/*.pdf` (official IGNOU TEE papers) — 2026-11-10.*
