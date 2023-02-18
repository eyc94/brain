# :heavy_check_mark: Data Structures & Algorithms

## :round_pushpin: Data Structures
A data structure is a storage that is used to store and organize data. It is a way of arranging data on a computer so that it can be accessed and updated efficiently. An efficient data structure utilizes minimum memory space and execution time.

There are two classifications of data structures:

### Linear
Elements are arranged in one dimension.
- [Array](./data-structures/linear/array/array.md)
  - [Java ArrayList class](./data-structures/linear/array/java-arraylist.md)
- [Linked List](./data-structures/linear/linked-list/linked-list.md)
  - [Java LinkedList class](./data-structures/linear/linked-list/java-linkedlist.md)
  - Types:
    - [Singly Linked List](./data-structures/linear/linked-list/singly-linked-list.md)
    - [Doubly Linked List](./data-structures/linear/linked-list/doubly-linked-list.md)
    - [Circularly Linked List](./data-structures/linear/linked-list/circularly-linked-list.md)
    - [Doubly Circular Linked List](./data-structures/linear/linked-list/doubly-circular-linked-list.md)
- [Stack](./data-structures/linear/stack/stack.md)
  - [Java Stack](./data-structures/linear/stack/java-stack.md)
  - [Java Deque](./data-structures/linear/stack/java-deque.md)
  - [Java ArrayDeque](./data-structures/linear/stack/java-arraydeque.md)
- [Queue](./data-structures/linear/queue/queue.md)
  - [Java Queue Class](./data-structures/linear/queue/java-queue.md)
  - [Java PriorityQueue Class](./data-structures/linear/queue/java-priorityqueue.md)
  - Types:
    - [Priority Queue](./data-structures/linear/queue/priority-queue.md)

### Non-Linear
Elements are arranged in one-to-many, many-to-one, and many-to-many dimensions.
- [Tree](./data-structures/non-linear/tree/tree.md)
  - [Binary Tree](./data-structures/non-linear/tree/binary-tree.md)
    - [Full Binary Tree](./data-structures/non-linear/tree/full-binary-tree.md)
    - [Complete Binary Tree](./data-structures/non-linear/tree/complete-binary-tree.md)
    - [Perfect Binary Tree](./data-structures/non-linear/tree/perfect-binary-tree.md)
    - [Balanced Binary Tree](./data-structures/non-linear/tree/balanced-binary-tree.md)
    - [Degenerate Binary Tree](./data-structures/non-linear/tree/degenerate-binary-tree.md)
    - [Skewed Binary Tree](./data-structures/non-linear/tree/skewed-binary-tree.md)
    - Strictly Binary Tree
    - Extended Binary Tree
    - [Binary Search Tree (BST)](./data-structures/non-linear/tree/binary-search-tree.md)
      - [AVL Tree](./data-structures/non-linear/tree/avl-tree.md)
      - [Red-Black Tree](./data-structures/non-linear/tree/red-black-tree.md)
    - [Binary Heap](./data-structures/non-linear/tree/binary-heap.md)
  - [Trie](./data-structures/non-linear/tree/trie.md)
  - [B-Tree](./data-structures/non-linear/tree/b-tree.md)
  - [B+ Tree](./data-structures/non-linear/tree/b-plus-tree.md)
- [Graph](./data-structures/non-linear/graph/graph.md)

## :round_pushpin: Algorithms
Algorithm is defined as a process or set of well-defined instructions that are typically used to solve a group of problems or perform a specific type of calculation.

It is a set of operations performed in a step-by-step manner to execute a task.

### Complexities
We need a way to determine how efficient and effective an algorithm is. A way to measure this is with complexities. There are two types:

1. **Time Complexity**
  a. Measures the amount of time required to execute the code.
2. **Space Complexity**
  a. Amount of space required to execute the code successfully.
  b. **Auxiliary Space** is a common term. This refers to the extra space used in the program other than the input data structure.

Both are measured with respect to the input parameters.

The time required for running a program depends on several things:
- The number of operations performed.
- The speed of the device.
- The speed of data transfer if being executed on an online platform.

We use **asymptotic notation**: A mathematical tool that calculates the required time in terms of input size and does not require the execution of code.

It only looks at modular operations being performed in the whole program.

There are three asymptotic notations to represent complexity:
1. **Big-O Notation (O):** Describes worst-case scenario.
  a. This is the most used notation because it represents an upper bound.
2. **Omega Notation ($\Omega$):** Describes best-case scenario.
3. **Theta Notation ($\Theta$):** Describes average complexity of an algorithm.

![Image of big-oh chart](images/algorithms/big-oh-chart.png)

From worst to best (there may be more to this):
- `O(n!)`, `O(c^n)`, `O(n^c)` - Worst
- `O(n log n)` - Bad
- `O(n)` - Fair
- `O(log n)` - good
- `O(1)` - Best

***NOTE:*** When dealing with constants, we remove them as they don't provide much value over time.

## :round_pushpin: Searching
Searching algorithms are designed to check for an element or retrieve an element from any data structure where it is stored.

***NOTE:*** There are more searching algorithms, but those below are the common and important ones.

- [Sequential/Linear Search](searching/linear-search.md)
- [Binary Search](searching/binary-search.md)


## :round_pushpin: Sorting
A sorting algorithm is used to rearrange a given array or list of elements according to a comparison operator on the elements.

The comparison operator is used to decide the new order of elements in the respective data structure.

![Image of sorting example](images/sorting/sorting-example.png)

There are many types of sorting algorithms:
- [Selection Sort](sorting/selection-sort.md)
- [Bubble Sort](sorting/bubble-sort.md)
- [Insertion Sort](sorting/insertion-sort.md)
- [Merge Sort](sorting/merge-sort.md)
- [Quick Sort](sorting/quick-sort.md)
- [Heap Sort](sorting/heap-sort.md)
- [Counting Sort](sorting/counting-sort.md)
- [Radix Sort](sorting/radix-sort.md)
- [Bucket Sort](sorting/bucket-sort.md)
- [Shell Sort](sorting/shell-sort.md)
- Comb Sort
- Pigeonhole Sort

***NOTE:*** There are more sorting algorithms, but those above are the common and important ones.

### Quick Complexity Reference
`n` represents the input size.

|Name|Best Case|Average Case|Worst Case|Memory|Stable|Method Used|
|----|---------|------------|----------|------|------|-----------|
|Quick Sort|`n log n`|`n log n`|<code>n<sup>2</sup></code>|`1`|No|Partitioning|
|Merge Sort|`n log n`|`n log n`|`n log n`|`n`|Yes|Merging|
|Heap Sort|`n log n`|`n log n`|`n log n`|`1`|No|Selection|
|Insertion Sort|`n`|<code>n<sup>2</sup></code>|<code>n<sup>2</sup></code>|`1`|Yes|Insertion|
|Shell Sort|`n log n`|<code>n<sup>4/3</sup></code>|<code>n<sup>3/2</sup></code>|`1`|No|Insertion|
|Bubble Sort|`n`|<code>n<sup>2</sup></code>|<code>n<sup>2</sup></code>|`1`|Yes|Exchanging|

***NOTE:*** There are more sorting algorithms, but those below are the common and important ones.

## :round_pushpin: Patterns & Techniques
Patterns are a tool to solve specific categories of problems.

- [ ] [Sliding Window](patterns/sliding-window.md) ![23/26 = 88%](https://progress-bar.dev/88)
- [ ] [Two Pointers](patterns/two-pointers.md) ![26/28 = 93%](https://progress-bar.dev/93)
- [x] [Fast and Slow Pointers](patterns/fast-and-slow-pointers.md) ![7/7 = 100%](https://progress-bar.dev/100)
- [ ] [Intervals](patterns/intervals.md) ![6/7 = 86%](https://progress-bar.dev/86)
- [ ] [Linked Lists Reversals](patterns/linked-list-reversals.md) ![9/11 = 82%](https://progress-bar.dev/82)
- [ ] [Two Heaps](patterns/two-heaps.md) ![0/4 = 0%](https://progress-bar.dev/0)
- [ ] [Tree Breadth First Search (BFS)](patterns/tree-breadth-first-search.md) ![9/10 = 90%](https://progress-bar.dev/90)
- [ ] [Tree Depth First Search (DFS)](patterns/tree-depth-first-search.md) ![10/12 = 83%](https://progress-bar.dev/83)
- [ ] [Subsets](patterns/subsets.md) ![3/7 = 43%](https://progress-bar.dev/43)
- [ ] [K-Way Merge](patterns/k-way-merge.md) ![3/7 = 43%](https://progress-bar.dev/43)
- [ ] [Top K Elements](patterns/top-k-elements.md) ![0/14 = 0%](https://progress-bar.dev/0)
- [ ] [Modified Binary Search](patterns/modified-binary-search.md) ![0/14 = 0%](https://progress-bar.dev/0)
- [ ] [Greedy](patterns/greedy.md) ![0/6 = 0%](https://progress-bar.dev/0)
- [ ] [Backtracking](patterns/backtracking.md) ![0/5 = 0%](https://progress-bar.dev/0)
- [ ] [Dynamic Programming](patterns/dynamic-programming.md) ![0/8 = 0%](https://progress-bar.dev/0)
- [ ] [Cyclic Sort](patterns/cyclic-sort.md) ![0/5 = 0%](https://progress-bar.dev/0)
- [ ] [Topological Sort](patterns/topological-sort.md) ![0/7 = 0%](https://progress-bar.dev/0)
- [ ] [Stacks](patterns/stacks.md) ![0/6 = 0%](https://progress-bar.dev/0)
- [ ] [Trie](patterns/trie.md) ![0/6 = 0%](https://progress-bar.dev/0)
- [ ] [Hash Maps](patterns/hash-maps.md) ![0/6 = 0%](https://progress-bar.dev/0)
- [ ] [Union Find](patterns/union-find.md) ![0/6 = 0%](https://progress-bar.dev/0)
- [ ] [Bitwise Manipulation](patterns/bitwise-manipulation.md) ![0/7 = 0%](https://progress-bar.dev/0)
- [ ] [Custom Data Structures](patterns/custom-data-structures.md) ![0/6 = 0%](https://progress-bar.dev/0)

## :round_pushpin: Top Leetcode Questions
Adopted from the popular [Blind](https://www.teamblind.com/post/New-Year-Gift---Curated-List-of-Top-75-LeetCode-Questions-to-Save-Your-Time-OaM1orEU) post and Needcode's curated [list](https://neetcode.io/roadmap).
- ***NOTE:*** Some questions are in the `Patterns & Techniques` section above.
- See [this](https://leetcode.com/discuss/general-discussion/460599/blind-75-leetcode-questions) for a fast Leetcode link to curated list.

### Array ![1/9 = 11%](https://progress-bar.dev/11)
- [x] 1. [Two Sum (Easy)](https://leetcode.com/problems/two-sum/description/)
- [ ] 36. [Valid Sudoku (Medium)](https://leetcode.com/problems/valid-sudoku/description/)
- [ ] 49. [Group Anagrams (Medium)](https://leetcode.com/problems/group-anagrams/description/)
- [ ] 128. [Longest Consecutive Sequence (Medium)](https://leetcode.com/problems/longest-consecutive-sequence/description/)
- [ ] 217. [Contains Duplicate (Easy)](https://leetcode.com/problems/contains-duplicate/description/)
- [ ] 238. [Product of Array Except Self (Medium)](https://leetcode.com/problems/product-of-array-except-self/description/)
- [ ] 242. [Valid Anagram (Easy)](https://leetcode.com/problems/valid-anagram/description/)
- [ ] 271. [Encode and Decode Strings (Medium)](https://leetcode.com/problems/encode-and-decode-strings/description/)
- [ ] 347. [Top K Frequent Elements (Medium)](https://leetcode.com/problems/top-k-frequent-elements/description/)

### Binary

### Interval

### Linked List

### Matrix

### String

### Tree

### Graph

### Heap

### Dynamic Programming

## :round_pushpin: Java Utilities
- Java `Arrays` class.
- Java `Collections` class.
- Java `Math` class.
