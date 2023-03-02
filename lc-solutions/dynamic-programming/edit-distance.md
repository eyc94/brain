# :heavy_check_mark: 72. Edit Distance
*Last Updated: 3/2/2023*

![Image of edit distance problem]()

## :round_pushpin: Problem
Leetcode problem [reference](https://leetcode.com/problems/edit-distance/)

## :round_pushpin: Examples
```
```

```
```

```
```

## :round_pushpin: DP Characteristics For Edit Distance
The brute force algorithm is very inefficient. So, we have to use `Dynamic Programming (DP)`.

The LCS problem has the properties of a DP problem:
1. **Optimal Substructure:** The problem can be broken down into smaller, simpler subproblems, which can, in turn, be broken down into simpler subproblems, and so on, until, finally the solution becomes trivial.
2. **Overlapping Subproblems:** The solutions to high-level subproblems often reuse solutions to lower level subproblems.

Subproblem solutions are `memoized` for faster access/calculations/reuse.

## :round_pushpin: Edit Distance Properties

***Explanation from ChatGPT:***

## :round_pushpin: DP Table

![Image of edit distance dp table]()

### What About The Letters?

## :round_pushpin: Complexity Analysis
`M` and `N` are the lengths of both strings.

Time Complexity: `O(M * N)`
Space Complexity: `O(M * N)`

## :round_pushpin: Applications
Here are some current applications that uses edit distance:

## :round_pushpin: Sources
2. [YouTube - Neetcode](https://www.youtube.com/watch?v=XYi2-LPrwm4)
3. [YouTube - Back to Back SWE](https://www.youtube.com/watch?v=MiqoA-yF-0M)
4. [YouTube - TECH DOSE](https://www.youtube.com/watch?v=AuYujVj646Q)
5. [YouTube - TECH DOSE](https://www.youtube.com/watch?v=5RlPzxWv9p4)
