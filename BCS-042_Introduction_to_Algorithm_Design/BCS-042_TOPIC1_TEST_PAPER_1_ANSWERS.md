BCS-042 TOPIC TEST 1 — ANSWER SHEET
Asymptotic Notation & Complexity Analysis
====================================================================

Q1(a)  3
  O      = Big Oh      -> upper bound
  Omega  = Big Omega   -> lower bound
  Theta  = Big Theta   -> tight bound (both upper and lower)


Q1(b)  3
  O(1)  <  O(sqrt n)  <  O(n log n)  <  O(n^2)  <  O(2^n)  <  O(n!)
  (if present: n log n always sits between n and n^2;
   2^n beats every polynomial; n! beats everything)


Q1(c)  5
  Definition:
    f(x) = O(g(x)) if there exist constants c > 0 and n0 > 0 such
    that  0 <= f(x) <= c.g(x)  for all x >= n0.

  Proof:
    Let f(x) = 6x^3 + 6x^2 + 1  and  g(x) = x^3.
    For x >= 1 :   6x^2 <= 6x^3   and   1 <= x^3
    Therefore
        6x^3 + 6x^2 + 1 <= 6x^3 + 6x^3 + x^3 = 13x^3
    So  f(x) <= 13.x^3  for all x >= 1.
    Taking  c = 13  and  n0 = 1,  we get  6x^3 + 6x^2 + 1 = O(x^3).


Q1(d)  5
  Time complexity  = number of basic operations performed, as a
                     function of input size n.
  Space complexity  = extra memory used (beyond the input itself),
                     as a function of n. Has two parts: fixed
                     (code, constants) + variable (depends on n).

  Example - factorial:

    Recursive:  fact(n) = n * fact(n-1)
                Time = O(n)   (n multiplications)
                Space = O(n)  (n stack frames kept alive)

    Iterative:  loop from 1 to n multiplying into a variable
                Time = O(n)
                Space = O(1)  (only one extra variable)

  Conclusion: same time, different space. Recursion costs stack
  memory; that difference IS space complexity.


Q2(a)  4
  Claim: 3n^3 + 5n^2 + 8 = O(n^2) is FALSE.

  Assume true. Then exists c such that
        3n^3 + 5n^2 + 8 <= c.n^2   for all n >= n0.
  Divide by n^2 (n > 0):
        3n + 5 + 8/n^2 <= c.
  But 3n grows without bound, so no fixed c can stay above it.
  Formally, take n > max(n0, c). Then 3n > c, so
        3n + 5 + 8/n^2 > c   - a contradiction.
  Hence no such c, n0 exist. The statement is false.

  Correct bound: 3n^3 + 5n^2 + 8 = O(n^3)  with c = 16, n0 = 1
  (since 5n^2 <= 5n^3 and 8 <= 8n^3 for n >= 1).


Q2(b)  4
  Definition: f(n) = Theta(g(n)) if there exist c1, c2, n0 > 0 with
        0 <= c1.g(n) <= f(n) <= c2.g(n)  for all n >= n0.

  For n >= 1 :
        Lower:  2n^2 <= 2n^2 + 5n + 2        (since 5n + 2 > 0)
        Upper:  2n^2 + 5n + 2 <= 2n^2 + 5n^2 + 2n^2 = 9n^2
                 (5n <= 5n^2 and 2 <= 2n^2 for n >= 1)

  So  2n^2 <= f(n) <= 9n^2  for all n >= 1, giving
        c1 = 2,  c2 = 9,  n0 = 1.
  Hence 2n^2 + 5n + 2 = Theta(n^2).


Q3(i)  2
  Binary search:  best O(1),  worst O(log n).
  Best : the middle element is the target -> found in 1 comparison.
  Worst: each comparison halves the array, n/2, n/4, ... -> log n.


Q3(ii)  3
  Bubble sort on an ALREADY sorted array (early-exit version):
        best = O(n),  worst = O(n^2).
  Best (already sorted): one full pass of n-1 comparisons, flag
        never set -> loop exits. O(n).
  Worst (reverse sorted): n-1 passes, ~n^2/2 swaps. O(n^2).


Q3(iii)  3
  DFS with adjacency list:  O(V + E).
  Every vertex is visited once: O(V).
  Every edge is examined at most twice (once from each end):
        O(E).
  Total = O(V + E).


Q4(a)  3
  Master Theorem:
  For  T(n) = a.T(n/b) + f(n),  with a >= 1, b > 1,
  compare f(n) with n^(log_b a) :

    Case 1: f(n) = O(n^(log_b a - e))  ->  T(n) = Theta(n^(log_b a))
    Case 2: f(n) = Theta(n^(log_b a))  ->  T(n) = Theta(n^(log_b a).log n)
    Case 3: f(n) = Omega(n^(log_b a + e)) and a.f(n/b) <= c.f(n)
            ->  T(n) = Theta(f(n))


Q4(b)  5

  (i)  T(n) = 4T(n/2) + n
       a = 4, b = 2 -> n^(log_2 4) = n^2 ;  f(n) = n
       n is smaller than n^2  ->  CASE 1
       T(n) = Theta(n^2)

  (ii) T(n) = 2T(n/2) + n
       a = 2, b = 2 -> n^(log_2 2) = n ;  f(n) = n
       n equals n  ->  CASE 2
       T(n) = Theta(n log n)

  (iii) T(n) = 9T(n/3) + n^2
       a = 9, b = 3 -> n^(log_3 9) = n^2 ;  f(n) = n^2
       equal  ->  CASE 2
       T(n) = Theta(n^2 log n)

  (iv) T(n) = 3T(n/2) + n^2
       a = 3, b = 2 -> n^(log_2 3) = n^1.585 ;  f(n) = n^2
       n^2 is larger  ->  CASE 3
       Check: 3.(n/2)^2 = 0.75 n^2 <= c.n^2 with c = 0.75 < 1  OK
       T(n) = Theta(n^2)


Q5(a)  4
  Upper bound: a guarantee that the running time will NOT exceed
      a certain growth. Formally f(n) <= c.g(n) -> Big Oh.
      Relates to the worst case.
      Example: binary search is O(log n) - it will never do more
      than about log n comparisons.

  Lower bound: a guarantee that the running time CANNOT be less
      than a certain growth. Formally f(n) >= c.g(n) -> Big Omega.
      Relates to the best case.
      Example: binary search is Omega(1) - at least one comparison
      must always be made.

  Binary search is therefore Theta(log n) overall.


Q5(b)  4
  Algorithm:
      for i = 1 to m:
          for j = 1 to n:
              C[i][j] = A[i][j] + B[i][j]

  Time complexity: O(m x n).
  Justification: the outer loop runs m times and, for each i, the
  inner loop runs n times. Each iteration performs one addition and
  one assignment - a constant number of operations. Hence the total
  number of operations is m x n, so the time complexity is O(m x n).
  (Space: O(m x n) for the result matrix C.)


====================================================================
MARKING NOTES FOR YOUR ATTEMPT
====================================================================
Q2(a) - verdict correct. Full marks need: the definition, the
        division step, and an explicit "for large n, 3n > any
        constant c" argument. Also state the correct bound O(n^3).

Q2(b) - your inequality chain is correct. Add these three lines to
        make it a full-mark answer:
            c1 = 2, c2 = 9, n0 = 1   (for n >= 1)
            since 5n + 2 > 0 gives the lower bound, and
            5n <= 5n^2, 2 <= 2n^2 give the upper bound.

Q4    - the only thing to memorise is "compare f(n) with n^(log_b a)".
        Every case question reduces to that one comparison.
====================================================================
