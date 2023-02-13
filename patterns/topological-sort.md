# :heavy_check_mark: Topological Sort
*Last Updated: 2/13/2023*

![Image of topological sort](../images/patterns/topological-sort/topological-sort.png)

## :round_pushpin: Introduction
- Topological Sort pattern is used to find valid orderings of elements that have dependencies on, or priority over each other.
- Scheduling and grouping problems that have prerequisites or dependencies fall under this pattern.
- Partial order.
- Offers more flexibility because there can be multiple correct answers.
- Convert a problem to a directed graph first.
- Elements to consider are the graph vertices and the dependency relationships form the edges.
- Graph needs to be `acyclic`.

## :round_pushpin: Partial Order vs. Complete/Total Order
Complete/Total Order:
- Consider we are asked to sort an array `[5,2,1]`.
- The answer is `[1,2,5]`, and this is the only answer.

Partial Order:
- Consider a course prerequisite where English I has to be taken before English II, and Mathematics can be taken whenever.
- There is no obligation to take Mathematics, so we can take it in any order as long as the dependency is respected.
- This is a partial order.
- There are three valid orders:
  1. English I, English II, Mathematics
  2. Mathematics, English I, English II
  3. English I, Mathematics, English II

## :round_pushpin: Requirements
Use topological sorting if:
- Partial ordering of the given elements.
- Asks you to find ordering of elements based on some dependency rules between them.

**Do not** use topological sorting if:
- It asks for total ordering.
- The relationships cannot be converted to a graph.
- The graph is not a tree.

## :round_pushpin: Leetcode Problems ![0/7 = 0%](https://progress-bar.dev/0)

- [ ] 207. [Course Schedule (Medium)](https://leetcode.com/problems/course-schedule/)
- [ ] 210. [Course Schedule II (Medium)](https://leetcode.com/problems/course-schedule-ii/)
- [ ] 269. [Alien Dictionary (Hard)](https://leetcode.com/problems/alien-dictionary/)
- [ ] 310. [Minimum Height Trees (Medium)](https://leetcode.com/problems/minimum-height-trees/)
- [ ] 444. [Sequence Reconstruction (Medium)](https://leetcode.com/problems/sequence-reconstruction/)
- [ ] 953. [Verifying an Alien Dictionary (Easy)](https://leetcode.com/problems/verifying-an-alien-dictionary/)
- [ ] 2115. [Find All Possible Recipes from Given Supplies (Medium)](https://leetcode.com/problems/find-all-possible-recipes-from-given-supplies/)

## :round_pushpin: Sources
*List to be updated...*
