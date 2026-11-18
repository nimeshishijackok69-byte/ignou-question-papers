BCS-042 : INTRODUCTION TO ALGORITHM DESIGN
TOPIC TEST 1 — ASYMPTOTIC NOTATION & COMPLEXITY ANALYSIS
====================================================================

Time : 1 Hour                                        Maximum Marks : 40

NOTE :
  (i)  Question No. 1 is COMPULSORY and carries 16 marks.
  (ii) Answer ANY THREE questions from Q2 - Q5 (8 marks each).
  (iii) For every proof, you must state the constants (c, c1, c2, n0)
        explicitly. A proof without stated constants gets no marks.
  (iv) Closed book. No calculator required.
  (v)  Write answers numbered exactly as asked, e.g. 1(c), 3(ii).

--------------------------------------------------------------------
Q1. (COMPULSORY)                                            16 marks
--------------------------------------------------------------------

(a) Write the name of each of the following symbols and state the
    type of bound it gives (upper / lower / tight) :          3
        (i)  O        (ii)  Omega        (iii)  Theta

(b) Arrange the following in increasing order of growth :     3
        O(n log n),  O(1),  O(2^n),  O(sqrt n),  O(n!),  O(n^2)

(c) Define O (big Oh) notation using its formal definition.
    Using that definition, show that :                        5
        6x^3 + 6x^2 + 1 = O(x^3)

(d) Explain the concept of space complexity. How is it different
    from time complexity ? Illustrate with the recursive factorial
    function (and its iterative version).                     5


--------------------------------------------------------------------
Q2.                                                         8 marks
--------------------------------------------------------------------

(a) Prove OR disprove, using the basic definition of O (big Oh):  4
        3n^3 + 5n^2 + 8 = O(n^2)

(b) Using the basic definition of Theta (big theta), show that:   4
        2n^2 + 5n + 2 = Theta(n^2)


--------------------------------------------------------------------
Q3.                                                         8 marks
--------------------------------------------------------------------

Analyse the following, giving the best case and the worst case
complexity in Big-Oh notation, with ONE line of reasoning each :

    (i)   Binary search on a sorted array of n elements.      2

    (ii)  Bubble sort on an array that is ALREADY sorted in
          ascending order (you may assume the standard early-exit
          / swapped-flag version).                            3

    (iii) Depth First Search (DFS) on a graph with V vertices
          and E edges, using an adjacency list.               3


--------------------------------------------------------------------
Q4.                                                         8 marks
--------------------------------------------------------------------

(a) State the Master Theorem.                              3

(b) Using the Master Theorem, give tight asymptotic bounds for
    each of the following. State which case applies.       5

        (i)   T(n) = 4T(n/2) + n
        (ii)  T(n) = 2T(n/2) + n
        (iii) T(n) = 9T(n/3) + n^2
        (iv)  T(n) = 3T(n/2) + n^2


--------------------------------------------------------------------
Q5.                                                         8 marks
--------------------------------------------------------------------

(a) Explain the terms upper bound and lower bound in the context
    of algorithm analysis. Give one example of each using binary
    search.                                                   4

(b) Write an algorithm to add two matrices of order m x n.
    Find its time complexity and justify your answer.         4


====================================================================
END OF PAPER
====================================================================
