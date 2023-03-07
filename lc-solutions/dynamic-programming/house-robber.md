# :heavy_check_mark: 198. :orange_book: House Robber
*Last Updated: 3/7/2023*

![Image of the house robber problem](../../images/lc-solutions/dynamic-programming/house-robber.png)

## :round_pushpin: Background
The `House Robber` problem is a Dynamic Programming (DP) problem that involves a robber trying to maximize the amount of money they can steal from a row of houses.

The idea is to rob houses that *are not* adjacent to each other because a security alarm will get triggered.

This problem resembles the classic `Fibonacci Sequence` problem where the numbers in the sequence are derived from the previous two numbers.

Basically, if we were to rob a house, we have to calculatet the maximum of the rest of the houses starting from two houses to the right. We then calculate the max for that subproblem. So, this means that we have subproblems and we should record the values somewhere.

## :round_pushpin: Problem
Leetcode problem [reference](https://leetcode.com/problems/unique-paths-ii/)

You are a professional robber planning to rob houses along a street. Each house has a certain amount of money stashed, the only constraint stopping you from robbing each of them is that adjacent houses have security systems connected and **it will automatically contact the police if two adjacent houses were broken into on the same night**.

Given an integer array `nums` representing the amount of money of each house, return *the maximum amount of money you can rob tonight **without alerting the police***.

## :round_pushpin: Examples
```
Input:        nums = [1,2,3,1]
Output:       4
Explanation:  Rob house 1 (money = 1) and then rob house 3 (money = 3).
              Total amount you can rob = 1 + 3 = 4.
```

```
Input:        nums = [2,7,9,3,1]
Output:       12
Explanation:  Rob house 1 (money = 2), rob house 3 (money = 9), and rob
              house 5 (money = 1).
              Total amount you can rob = 2 + 9 + 1 = 12.
```

## :round_pushpin: DP Characteristics For House Robber
The brute force algorithm is very inefficient. So, we have to use `Dynamic Programming (DP)`.

The LCS problem has the properties of a DP problem:
1. **Optimal Substructure:** The problem can be broken down into smaller, simpler subproblems, which can, in turn, be broken down into simpler subproblems, and so on, until, finally the solution becomes trivial.
2. **Overlapping Subproblems:** The solutions to high-level subproblems often reuse solutions to lower level subproblems.

Subproblem solutions are `memoized` for faster access/calculations/reuse.

## :round_pushpin: House Robber Properties
So, we have to understand the restriction that we *cannot* rob adjacent houses. We also can only steal from one house at a time.

So, we must consider two cases for each house:
1. The robber **does not** steal from the current house. In this case, the robber will move on to the next house and try to steal from it. Since the robber cannot steal from two adjacent houses, we do not have to worry about the next house behind adjacent to the current house.
2. The robber steals from the current house. In this case, the robber will skip the next house and move on to the house after that to try to steal from it. Again, we don't have to worry about the next house being adjacent to the current house since the robber is skipping the next house.

To explain it in simpler terms:

We start by figuring out the max amount of money the robber can steal from the first house in the row. Then, we move on to the second house and figure out the max money the robber can steal from the first two houses. We continue this until we reach the end.

At each house, we have two choices:
1. Skip the current house. Here, the robber skips the current house to move to the next house. In which case, the max amount of money they can steal at the **current** house is the same as the max of the **previous** house.
2. Rob the current house. Here, the max money they can steal from the current house is the amount of money in the current house **plus** the max amount of money from two houses back (because they cannot be adjacent).

Basically, in `scenario 1`, we are setting up the current house value for the next iteration (house) because we decided **not** to rob the current house (in case this is confusing).

## :round_pushpin: DP Table
The Dynamic Programming (DP) table for this problem uses a 1D array that records the max amount we can rob at any given house. So, the idea is to record these values in this table. The right-most value will hold the max amount of money we can rob in the row of houses.

The idea is, that at every cell, we follow the two conditions in the previous section. We take the max of scenario 1 and 2 and use that to place in the current cell in our `dp` array.

```java
dp[i] = Math.max(dp[i - 1], dp[i - 2] + nums[i]);
```

Here is an example:
```css
       0   1   2    3    4    5    6    7    8    9    10
     +---+---+----+----+----+----+----+----+----+----+----+
nums | 2 | 3 |  9 | 10 |  1 |  2 | 11 |  7 |  4 |  8 |  1 |
     +---+---+----+----+----+----+----+----+----+----+----+

       0   1   2    3    4    5    6    7    8    9    10
     +---+---+----+----+----+----+----+----+----+----+----+
dp   | 2 | 3 | 11 | 13 | 13 | 15 | 24 | 24 | 28 | 32 | 32 |
     +---+---+----+----+----+----+----+----+----+----+----+
```

Basically, at every cell, we either **rob it** or **leave it**. If we chose to leave it alone, we just take the value to the *left* of the current cell and place it into the current cell. We are essentially setting up for the next house we *may* or *may not* rob.

If we rob it, we see what is more worth:
1. Start robbing from this house.
2. Or, continue robbing from the previous houses (at least two away).

Also, we must notice the base cases. The first two houses will always equal the value (amount of money) at those two houses. This is because we start from these two, and they cannot be adjacent.

## :round_pushpin: Complexity Analysis
`N` is the number of houses in the row.

Time Complexity: `O(N)`
Space Complexity: `O(N)`

## :round_pushpin: Variations
- Circular Row.
- K Houses Apart.
- Multiplayer Game.
- Weighted Houses.
- Subset Robbery.

## :round_pushpin: Applications
Here are some applications in the real-world:
- Financial Planning.
- Resource Allocation.
- Network Security.
- Gaming.

## :round_pushpin: Supplemental Sources
*Note:* The sources below do not really explain the *why* in the DP approach.
1. [YouTube - Neetcode](https://www.youtube.com/watch?v=73r3KWiEvyk)
2. [YouTube - Nick White](https://www.youtube.com/watch?v=ZwDDLAeeBM0)
3. [YouTube - Kevin Naughton Jr.](https://www.youtube.com/watch?v=xlvhyfcoQa4)
