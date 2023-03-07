# :heavy_check_mark: 63. :orange_book: Unique Paths II
*Last Updated: 3/7/2023*

![Image of the unique paths ii problem](../../images/lc-solutions/dynamic-programming/unique-paths-ii.png)

## :round_pushpin: Background
This problem is an extension of the `Unique Paths` problem.

The `Unique Paths` problem is a classic Dynamic Programming (DP) problem. This involves finding the number of unique paths in a grid from the top-left to the bottom-right corner.

You can only move right or down at each step.

However, the `Unique Paths II` problem becomes more complicated. Obstacles are introduced into the grid. Certain cells are marked as obstacles and cannot be passed through. The goal is still to find the number of unique paths from the top-left to the bottom-right.

## :round_pushpin: Problem
Leetcode problem [reference](https://leetcode.com/problems/unique-paths-ii/)

You are given an `m x n` integer array `grid`. There is a robot initially located at the **top-left corner** (i.e., `grid[0][0]`). The robot tries to move to the **bottom-right corner** (i.e. `grid[m - 1][n - 1]`). The robot can only move either down or right at any point in time.

An obstacle and space are marked as `1` or `0` respectively in `grid`. A path that the robot takes cannot include **any** square that is an obstacle.

Return *the number of possible unique paths that the robot can take to reach the bottom-right corner*.

The test cases are generated so that the answer will be less than or equal to <code>2 * 10<sup>9</sup></code>.

## :round_pushpin: Examples
```
Input:        obstacleGrid = [
                [0,0,0],
                [0,1,0],
                [0,0,0]
              ]
Output:       2
Explanation:  There is one obstacle in the middle of the 3x3 grid
              above. There are two ways to reach the bottom-right
              corner:
              1. Right -> Right -> Down -> Down
              2. Down -> Down -> Right -> Right
```

```
Input:        obstacleGrid = [
                [0,1],
                [0,0]
              ]
Output:       1
```

## :round_pushpin: DP Characteristics For Unique Paths II
The brute force algorithm is very inefficient. So, we have to use `Dynamic Programming (DP)`.

The LCS problem has the properties of a DP problem:
1. **Optimal Substructure:** The problem can be broken down into smaller, simpler subproblems, which can, in turn, be broken down into simpler subproblems, and so on, until, finally the solution becomes trivial.
2. **Overlapping Subproblems:** The solutions to high-level subproblems often reuse solutions to lower level subproblems.

Subproblem solutions are `memoized` for faster access/calculations/reuse.

## :round_pushpin: Unique Paths II Properties
When dealing with unique paths with obstacles, a brute-force idea is to traverse *every* possible path with only right and down movements.

However, it will soon become obvious that this approach is not realistic, and it will take too long to complete.

There are a few important things to note:
1. Every cell comes from another cell (unless it is the origin).
2. Every cell has a path coming from the top *and* left. This applies to every cell but the cells on the first row and first column.
3. Every cell that is an obstacle will no longer contribute to a growing path to cells further down.

Basically, every cell's incoming path should be added together to get the total number of paths to that particular cell.

To do this, we can create a table to record the number of unique paths at each cell *so far*.

***Explanation from ChatGPT:***

## :round_pushpin: DP Table
The Dynamic Programming (DP) table for the unique paths problem can be seen as the same as the field the robot is traveling.

Basically, every cell of the dp table records the number of unique paths **to** that cell. To calculate the number of unique paths to that cell, we have to add up all the **incoming** paths to that cell.

We know paths can only come from the top or the left. So, we just add the values from the **top** and the **left**.

However, we have to keep in mind that there are obstacles present. Their locations are given in the `obstacleGrid` matrix.

Here is an example:
```css
Example:

obstacleGrid:
      0   1   2
    +---+---+---+
0   | 0 | 0 | 0 |
    +---+---+---+
1   | 0 | 1 | 0 |
    +---+---+---+
2   | 0 | 0 | 0 |
    +---+---+---+

dp:
      0   1   2
    +---+---+---+
0   | 0 | 1 | 1 |
    +---+---+---+
1   | 1 | 0 | 1 |
    +---+---+---+
2   | 1 | 1 | 2 |
    +---+---+---+
```

Notice that the obstacle is present in the middle of the `3x3` matrix. Because of this obstacle, the value inside the corresponding cell in `dp` will be 0. This is because we can *no longer* create paths from this cell.

We will still be adding the top and left cells for every cell. In order to denote that there can be no more paths from an obstacle, we must put a `0` in the location of the `dp` array. This means that cells that have paths "incoming" from an obstacle, will not count the path with the obstacle. This is exactly what we want.

So, get the number of unique paths for the top and left cells and add them together for the answer for the current cell.

The bottom-right position (final robot position) will hold the value for the unique paths from origin to destination.

The example below shows a grid with **more than one** obstacle:
```css
obstacleGrid:
      0   1   2
    +---+---+---+
0   | 0 | 0 | 0 |
    +---+---+---+
1   | 1 | 1 | 0 |
    +---+---+---+
2   | 0 | 0 | 0 |
    +---+---+---+

dp:
      0   1   2
    +---+---+---+
0   | 0 | 1 | 1 |
    +---+---+---+
1   | 0 | 0 | 1 |
    +---+---+---+
2   | 0 | 0 | 1 |
    +---+---+---+
```
Notice here that the cell at `[1,0]` has an obstacle. So the `dp` matrix has the value `0` in the `dp` array. Any cell that extends from this obstacle cell will have a path count of 0 *plus* the path to its left.

The path to its left is **outside** the boundaries of the matrix.

## :round_pushpin: Complexity Analysis
`M` is the number of rows in the grid.
`N` is the number of columns in the grid.

Time Complexity: `O(N * M)`
Space Complexity: `O(N * M)`

## :round_pushpin: Variations
- Unique Paths with Limited Moves.
- Unique Paths with Obstacles and Weights.
- Unique Paths with Multiple Destinations.
- Unique Paths on a Hexagonal Grid.
- Unique Paths on a Weighted Graph.

## :round_pushpin: Applications
Here are some applications in the real-world:
- Robotics.
- Logistics.
- Map Navigation.
- Network Routing.
- Game Design.
- Supply Chain Management.
- Disaster Response.

## :round_pushpin: Supplemental Sources
1. [YouTube - Neetcode](https://www.youtube.com/watch?v=d3UOz7zdE4I)
2. [YouTube - TECH DOSE](https://www.youtube.com/watch?v=z6kelCB0ww4)
