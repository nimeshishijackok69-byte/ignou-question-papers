BCS-042 : TOPIC 1 — ASYMPTOTIC NOTATION & COMPLEXITY ANALYSIS
All past-year questions, Dec 2021 - Jun 2026 (11 papers)
Source: BCS-042_all_papers.txt (extracted from official IGNOU TEE papers)
====================================================================

Frequency: 11/11 papers. Always appears in Q1 (compulsory, 20 marks),
usually as Q1(a) — so it is the FIRST thing you write in the exam.

Total questions found: 40 (2-7 marks each, ~6-10 marks of every paper)


====================================================================
PART A — EVERY QUESTION, PAPER BY PAPER (verbatim where legible)
====================================================================

--- JUNE 2021 -------------------------------------------------------
Q1(a) Arrange the following classes of algorithms in increasing
      order of growth :  [3]
      (i) O(n^3)  (ii) O(n log n)  (iii) O(n^2)  (iv) O(sqrt n)

Q2(a) Write the pseudocode for computing GCD(m, n) and find its
      time complexity.  [4]


--- DECEMBER 2021 ---------------------------------------------------
Q1(a) State True or False :  [2]
      O(log n) is better than O(n^2) but not as good as O(n).

Q1(b) Write the names of the following symbols :  [2]
      (Theta), (Omega), O

Q1(c) Define O (big Oh) notation. By using the basic definition of
      O (big Oh), show that :  [4]
            6x^3 + 6x^2 + 1 = O(x^3)

Q2(a) Arrange the following growth rate in increasing order :  [2]
      O(2^n), O(n^3), n!, n

Q2(b)(ii) Perform the complexity analysis of the BFS algorithm
      (the one you just traced).  [4]


--- JUNE 2022 -------------------------------------------------------
Q1(a) Define basic efficiency classes in context of running time.  [3]

Q2(a) Arrange the following functions in increasing order :  [2]
      n^2 , log n , n log n , 5n + 7
      [exact list partly garbled in the source PDF extraction]

Q3(a) For the function defined by  f(n) = 6n^2 + 8n + 6,
      show that f(n) = O(n^2).  [4]

Q5(a) Write any two cases of the Master method with formal
      notations.  [4]


--- DECEMBER 2022 ---------------------------------------------------
Q1(a) Define Theta (big theta) notation. By using a basic
      definition, show that :  [4]
            7n^2 + 8n - 9 = Theta(n^2)

Q2(a) Give an example for each complexity class :  [3]
      O(n),   O(n^2),   O(n log n)

Q2(b)(ii) Perform the complexity analysis of the Euclid algorithm
      (used to find GCD(325, 95)).  [3]


--- JUNE 2023 -------------------------------------------------------
Q1(a) What is complexity of algorithm ? Explain space complexity
      and time complexity of algorithms with the help of an
      example.  [5]

Q3(b) Explain use of Big oh (O) notation in the analysis of
      algorithms with example.  [2]

Q4(b)(i) Explain Upper Bound (with an example of each).  [2]

Q5(b) Write algorithm for adding two matrices of order m x n and
      find its time complexity.  [4]


--- DECEMBER 2023 ---------------------------------------------------
Q1(a) Show that :  [2]
            2n^2 + 5n + 2 = Theta(n^2)
      [symbols garbled in extraction; this is the standard pair
       for this slot — verify against the original paper]

Q1(c) Write binary search algorithm and explain its best case and
      worst case complexity.  [5]

Q2(b) Write Prim's algorithm for finding minimum spanning tree and
      find the complexity of this algorithm.  [5]


--- JUNE 2024 -------------------------------------------------------
Q1(a) Arrange the following time complexities in the increasing
      order :  [2]
      O(log n), O(n^2), O(3^n), O(n!)

Q1(b) Write the names of the following symbols :  [3]
      (i) Theta   (ii) Omega   (iii) O

Q1(d) What is linear search method ? Apply linear search to search
      the number 9 in the following list. Show the searching
      steps :  8, 4, 10, 6, 9, 2
      Also, analyse the worst case complexity of the linear
      search method.  [6]

Q2(a) Explain the following terms :  [3]
      (i) Space complexity  (ii) Cycle in a graph  (iii) Lower bound

Q2(b) Traverse the graph using DFS from A ... Also, write the time
      complexity of DFS method.  [7]

Q3(a) Write and explain binary search algorithm. Explain its time
      complexity for best and worst cases.  [5]

Q4(b) Write an algorithm for multiplying two matrices. Also find
      the time complexity of this algorithm.  [6]


--- DECEMBER 2024 ---------------------------------------------------
Q1(a) Define O (big oh) notation and prove or disprove the
      following using the basic definition of O (big oh) :  [4]
            3n^3 + 5n^2 + 8 = O(n^3)
      [digits garbled in extraction — check the original; if the
       paper says = O(n^2) then the answer is "disprove"]

Q1(b) Write bubble sort algorithm and find its worst case time
      complexity.  [5]

Q3(c) Explain the use of lower bound and upper bound concepts
      with the help of example.  [5]


--- JUNE 2025 -------------------------------------------------------
Q1(b) What is the time complexity of linear search algorithm ?
      Explain with the help of an example.  [5]

Q2    (Master-method / asymptotics question, text garbled)
      "What is the largest integer value for ... such that
      A^? is asymptotically faster than A ?"  [5]

Q3(a) Given an array of size(n), analyze the time complexity of
      the bubble sort algorithm. If array is already sorted in
      ascending order, what would be the best time complexity ?
      Provide the Big-O notation for both the best case and
      worst case scenarios.  [5]


--- DECEMBER 2025 ---------------------------------------------------
Q1(a) Explain the concept of the space complexity in context of
      algorithm analysis. How is it different from time
      complexity ? Provide an example to illustrate the
      calculation of space complexity.  [5]

Q1(c) Describe any three of the following :  [3 x 2 = 6]
      (i) Greedy technique   (ii) Cycle in a Directed Graph
      (iii) Upper Bound      (iv) Branch and Bound

Q1(d) Use Master Theorem to give tight asymptotic bounds of the
      following :  [2 x 2 = 4]
      (i)  T(n) = 4T(n/2) + n
      (ii) T(n) = 2T(n/2) + n


--- JUNE 2026 -------------------------------------------------------
Q1(c) Why is analysis of an algorithm important ? Justify your
      answer with example.  [5]

Q1(d) Explain asymptotic notations. Also, discuss what is upper
      and lower bound in asymptotic notations.  [5]

Q3(a) Write basic algorithm to evaluate a polynomial and find its
      complexity.  [5]


====================================================================
PART B — THE 7 SHAPES (prep these, cover every paper)
====================================================================

SHAPE 1 — Arrange growth rates in increasing order
  Papers: Jun21, Dec21, Jun22, Jun24          Marks: 2-3
  Method: memorise the ladder, then slot each term in.
      1 < log log n < log n < sqrt(n) < n < n log n
        < n^2 < n^3 < 2^n < n! < n^n
  Traps: n log n sits BETWEEN n and n^2 (not after n^2).
         2^n beats n^3 and any polynomial; n! beats everything.

SHAPE 2 — Define O / Theta and prove by definition
  Papers: Dec21, Jun22, Dec22, Dec23, Dec24    Marks: 2-4
  Definition to write first:
      f(n) = O(g(n)) if there exist positive constants c and n0
      such that 0 <= f(n) <= c.g(n)  for all n >= n0.
      f(n) = Theta(g(n)) if there exist c1, c2, n0 > 0 with
      0 <= c1.g(n) <= f(n) <= c2.g(n)  for all n >= n0.
  Then find the constants (always work from n >= 1 or n >= 2):

  (a) 6x^3 + 6x^2 + 1 = O(x^3)
      For x >= 1: 6x^2 <= 6x^3 and 1 <= x^3
      => 6x^3 + 6x^2 + 1 <= 6x^3 + 6x^3 + x^3 = 13x^3
      So c = 13, n0 = 1.                                   DONE

  (b) 6n^2 + 8n + 6 = O(n^2)
      For n >= 1: 8n <= 8n^2 and 6 <= 6n^2
      => <= 6n^2 + 8n^2 + 6n^2 = 20n^2
      So c = 20, n0 = 1.                                   DONE

  (c) 7n^2 + 8n - 9 = Theta(n^2)      <-- the one in your notes
      Upper: for n >= 1, 8n <= 8n^2 and -9 <= 0
             => 7n^2 + 8n - 9 <= 15n^2      so c2 = 15
      Lower: for n >= 2, 8n - 9 > 0
             => 7n^2 + 8n - 9 >= 7n^2       so c1 = 7
      So c1 = 7, c2 = 15, n0 = 2.                          DONE

  (d) 2n^2 + 5n + 2 = Theta(n^2)   (Dec 2023)
      Upper: n >= 1 -> 5n <= 5n^2, 2 <= 2n^2 => <= 9n^2, c2 = 9
      Lower: n >= 1 -> 5n + 2 > 0 => >= 2n^2, c1 = 2, n0 = 1

  (e) 3n^3 + 5n^2 + 8 = O(n^3)     (Dec 2024)
      n >= 1 -> 5n^2 <= 5n^3, 8 <= 8n^3 => <= 16n^3, c = 16, n0 = 1

  NOTE: IGNOU alternates between O(...) and Theta(...) for the same
  kind of function. If asked for Theta and you only give the upper
  bound, you lose the lower-bound marks. Always give both.

SHAPE 3 — Name the symbols (cheapest marks in the whole paper)
  Papers: Dec21, Jun24                         Marks: 2-3
      O     = Big Oh     -> upper bound
      Omega = Big Omega  -> lower bound
      Theta = Big Theta  -> tight bound (both)

SHAPE 4 — Space vs time complexity, with an example
  Papers: Jun23, Dec25, Jun26                  Marks: 5
  Answer skeleton:
      - Time complexity = number of basic operations as a function
        of input size n (how long it runs).
      - Space complexity = extra memory beyond the input, again as
        a function of n. Two parts: fixed + variable.
      - Give the SAME algorithm both ways, e.g. iterative vs
        recursive factorial:
            iterative: time O(n), space O(1)
            recursive: time O(n), space O(n)  (call stack)
        That single example wins the "illustrate" marks.

SHAPE 5 — Upper bound / lower bound explained
  Papers: Jun23, Jun24, Dec24, Dec25, Jun26    Marks: 2-6
  Appears in 5 of the last 6 papers — do not skip.
      - Upper bound = a guarantee it will not get slower than
        this: f(n) <= c.g(n)  -> Big Oh (worst case).
      - Lower bound = a guarantee it cannot be faster than this:
        f(n) >= c.g(n)  -> Big Omega (best case).
      - Tight bound = both at once -> Theta.
      - Example: binary search is Omega(1) best case,
        O(log n) worst case, Theta(log n) in general.

SHAPE 6 — Complexity of a named algorithm
  Papers: almost every paper                 Marks: 4-7
  Table worth memorising:
      linear search   : best O(1),        worst O(n)
      binary search   : best O(1),        worst O(log n)
      bubble sort     : best O(n) (already sorted, with flag),
                        worst O(n^2)
      selection sort  : always O(n^2)
      merge sort      : O(n log n) always
      quick sort      : best/avg O(n log n), worst O(n^2)
      insertion sort  : best O(n),        worst O(n^2)
      DFS / BFS       : O(V + E)
      Prim (matrix)   : O(V^2)
      Kruskal         : O(E log E)
      matrix add      : O(m x n)
      matrix multiply : O(n^3); Strassen O(n^2.81)
      Euclid GCD      : O(log(min(a,b)))
      polynomial eval : O(n^2) naive, O(n) with Horner

SHAPE 7 — Master theorem
  Papers: Jun22, Dec25                         Marks: 4-5
  For T(n) = aT(n/b) + f(n), compare f(n) with n^(log_b a):
      Case 1: f(n) smaller  -> T(n) = Theta(n^(log_b a))
      Case 2: equal         -> T(n) = Theta(n^(log_b a) . log n)
      Case 3: f(n) larger   -> T(n) = Theta(f(n))
  Worked Dec 2025 answers:
      T(n) = 4T(n/2) + n : a=4, b=2, n^2 vs n  -> Case 1
                           => Theta(n^2)
      T(n) = 2T(n/2) + n : a=2, b=2, n^1 vs n  -> Case 2
                           => Theta(n log n)


====================================================================
30-MINUTE DRILL (do this before reading anything else)
====================================================================
1. Write the ladder of growth rates from memory.          (Shape 1)
2. Write the formal definitions of O, Omega, Theta.       (Shape 3)
3. Prove 7n^2 + 8n - 9 = Theta(n^2) with constants.       (Shape 2c)
4. Prove 6n^2 + 8n + 6 = O(n^2).                          (Shape 2b)
5. Recite: binary search best/worst, bubble best/worst,
   merge sort, DFS.                                       (Shape 6)
6. Master theorem 3 cases + the two Dec 2025 recurrences. (Shape 7)

That set has appeared, in some form, in all 11 papers.

--------------------------------------------------------------------
NOTE ON ACCURACY: questions are taken from the PDF text extraction
in BCS-042_all_papers.txt. A few mathematical expressions were
scrambled by the extraction (marked "garbled"); check those 4 items
against the original question papers before memorising the exact
constants.
--------------------------------------------------------------------
