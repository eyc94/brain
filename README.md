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

### Array ![3/16 = 19%](https://progress-bar.dev/19)
- [x] 1. [Two Sum (Easy)](https://leetcode.com/problems/two-sum/description/)
- [ ] 11. [Container With Most Water (Medium)](https://leetcode.com/problems/container-with-most-water/description/)
- [x] 15. [3Sum (Medium)](https://leetcode.com/problems/3sum/description/)
- [ ] 33. [Search in Rotated Sorted Array (Medium)](https://leetcode.com/problems/search-in-rotated-sorted-array/description/)
- [ ] 36. [Valid Sudoku (Medium)](https://leetcode.com/problems/valid-sudoku/description/)
- [ ] 49. [Group Anagrams (Medium)](https://leetcode.com/problems/group-anagrams/description/)
- [x] 53. [Maximum Subarray (Medium)](https://leetcode.com/problems/maximum-subarray/description/)
- [ ] 121. [Best Time to Buy and Sell Stock (Easy)](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/description/)
- [ ] 128. [Longest Consecutive Sequence (Medium)](https://leetcode.com/problems/longest-consecutive-sequence/description/)
- [ ] 152. [Maximum Product Subarray (Medium)](https://leetcode.com/problems/maximum-product-subarray/description/)
- [ ] 153. [Find Minimum in Rotated Sorted Array (Medium)](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/description/)
- [ ] 217. [Contains Duplicate (Easy)](https://leetcode.com/problems/contains-duplicate/description/)
- [ ] 238. [Product of Array Except Self (Medium)](https://leetcode.com/problems/product-of-array-except-self/description/)
- [ ] 242. [Valid Anagram (Easy)](https://leetcode.com/problems/valid-anagram/description/)
- [ ] 271. [Encode and Decode Strings (Medium)](https://leetcode.com/problems/encode-and-decode-strings/description/)
- [ ] 347. [Top K Frequent Elements (Medium)](https://leetcode.com/problems/top-k-frequent-elements/description/)

### Binary ![0/6 = 0%](https://progress-bar.dev/0)
- [ ] 136. [Single Number (Easy)](https://leetcode.com/problems/single-number/description/)
- [ ] 190. [Reverse Bits (Easy)](https://leetcode.com/problems/reverse-bits/)
- [ ] 191. [Number of 1 Bits (Easy)](https://leetcode.com/problems/number-of-1-bits/description/)
- [ ] 268. [Missing Number (Easy)](https://leetcode.com/problems/missing-number/description/)
- [ ] 338. [Counting Bits (Easy)](https://leetcode.com/problems/counting-bits/)
- [ ] 371. [Sum of Two Integers (Medium)](https://leetcode.com/problems/sum-of-two-integers/description/)

### Interval ![4/6 = 66%](https://progress-bar.dev/66)
- [x] 56. [Merge Intervals (Medium)](https://leetcode.com/problems/merge-intervals/)
- [x] 57. [Insert Interval (Medium)](https://leetcode.com/problems/insert-interval/)
- [ ] 252. [Meeting Rooms (Medium)](https://leetcode.com/problems/meeting-rooms/description/)
- [x] 253. [Meeting Rooms II (Medium)](https://leetcode.com/problems/meeting-rooms-ii/description/)
- [x] 435. [Non-overlapping Intervals (Medium)](https://leetcode.com/problems/non-overlapping-intervals/)
- [ ] 1851. [Minimum Interval to Include Each Query (Hard)](https://leetcode.com/problems/minimum-interval-to-include-each-query/)

### Linked List ![6/11 = 55%](https://progress-bar.dev/55)
- [ ] 2. [Add Two Numbers (Medium)](https://leetcode.com/problems/add-two-numbers/description/)
- [x] 19. [Remove Nth Node From End of List (Medium)](https://leetcode.com/problems/remove-nth-node-from-end-of-list/description/)
- [ ] 21. [Merge Two Sorted Lists (Easy)](https://leetcode.com/problems/merge-two-sorted-lists/description/)
- [x] 25. [Reverse Node in k-Group (Hard)](https://leetcode.com/problems/reverse-nodes-in-k-group/)
- [x] 23. [Merge k Sorted Lists (Hard)](https://leetcode.com/problems/merge-k-sorted-lists/description/)
- [ ] 138. [Copy List with Random Pointer (Medium)](https://leetcode.com/problems/copy-list-with-random-pointer/description/)
- [x] 141. [Linked List Cycle (Easy)](https://leetcode.com/problems/linked-list-cycle/description/)
- [x] 143. [Reorder List (Medium)](https://leetcode.com/problems/reorder-list/description/)
- [ ] 146. [LRU Cache (Medium)](https://leetcode.com/problems/lru-cache/description/)
- [x] 206. [Reverse Linked List (Easy)](https://leetcode.com/problems/reverse-linked-list/description/)
- [ ] 287. [Find the Duplicate Number (Medium)](https://leetcode.com/problems/find-the-duplicate-number/description/)

### Matrix ![0/4 = 0%](https://progress-bar.dev/0)
- [ ] 48. [Rotate Image (Medium)](https://leetcode.com/problems/rotate-image/description/)
- [ ] 54. [Spiral Matrix (Medium)](https://leetcode.com/problems/spiral-matrix/description/)
- [ ] 73. [Set Matrix Zeroes (Medium)](https://leetcode.com/problems/set-matrix-zeroes/description/)
- [ ] 79. [Word Search (Medium)](https://leetcode.com/problems/word-search/description/)

### String ![3/10 = 30%](https://progress-bar.dev/30)
- [x] 3. [Longest Substring Without Repeating Characters (Medium)](https://leetcode.com/problems/longest-substring-without-repeating-characters/description/)
- [ ] 5. [Longest Palindromic Substring (Medium)](https://leetcode.com/problems/longest-palindromic-substring/description/)
- [ ] 20. [Valid Parentheses (Easy)](https://leetcode.com/problems/valid-parentheses/description/)
- [ ] 49. [Group Anagrams (Medium)](https://leetcode.com/problems/group-anagrams/description/)
- [x] 76. [Minimum Window Substring (Hard)](https://leetcode.com/problems/minimum-window-substring/description/)
- [ ] 125. [Valid Palindrome (Easy)](https://leetcode.com/problems/valid-palindrome/description/)
- [ ] 242. [Valid Anagram (Easy)](https://leetcode.com/problems/valid-anagram/description/)
- [ ] 271. [Encode and Decode Strings (Medium)](https://leetcode.com/problems/encode-and-decode-strings/description/)
- [x] 424. [Longest Repeating Character Replacement (Medium)](https://leetcode.com/problems/longest-repeating-character-replacement/description/)
- [ ] 647. [Palindromic Substrings (Medium)](https://leetcode.com/problems/palindromic-substrings/description/)

### Tree ![6/18 = 33%](https://progress-bar.dev/33)
- [ ] 98. [Validate Binary Search Tree (Medium)](https://leetcode.com/problems/validate-binary-search-tree/description/)
- [ ] 100. [Same Tree (Easy)](https://leetcode.com/problems/same-tree/description/)
- [x] 102. [Binary Tree Level Order Traversal (Medium)](https://leetcode.com/problems/binary-tree-level-order-traversal/description/)
- [x] 104. [Maximum Depth of Binary Tree (Easy)](https://leetcode.com/problems/maximum-depth-of-binary-tree/description/)
- [ ] 105. [Construct Binary Tree from Preorder and Inorder Traversal (Medium)](https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/description/)
- [ ] 110. [Balanced Binary Tree (Easy)](https://leetcode.com/problems/balanced-binary-tree/description/)
- [x] 124. [Binary Tree Maximum Path Sum (Hard)](https://leetcode.com/problems/binary-tree-maximum-path-sum/description/)
- [x] 199. [Binary Tree Righ Side View (Easy)](https://leetcode.com/problems/binary-tree-right-side-view/description/)
- [ ] 208. [Implement Trie (Prefix Tree) (Medium)](https://leetcode.com/problems/implement-trie-prefix-tree/description/)
- [ ] 211. [Design Add and Search Words Data Structure (Medium)](https://leetcode.com/problems/design-add-and-search-words-data-structure/description/)
- [ ] 212. [Word Search II (Hard)](https://leetcode.com/problems/word-search-ii/description/)
- [x] 226. [Invert Binary Tree (Easy)](https://leetcode.com/problems/invert-binary-tree/description/)
- [ ] 230. [Kth Smallest Element in a BST (Medium)](https://leetcode.com/problems/kth-smallest-element-in-a-bst/description/)
- [ ] 235. [Lowest Common Ancestor of a Binary Search Tree (Medium)](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/description/)
- [ ] 297. [Serialize and Deserialize Binary Tree (Hard)](https://leetcode.com/problems/serialize-and-deserialize-binary-tree/description/)
- [x] 543. [Diameter of Binary Tree (Easy)](https://leetcode.com/problems/diameter-of-binary-tree/)
- [ ] 572. [Subtree of Another Tree (Easy)](https://leetcode.com/problems/subtree-of-another-tree/description/)
- [ ] 1448. [Count Good Nodes in Binary Tree (Medium)](https://leetcode.com/problems/count-good-nodes-in-binary-tree/description/)

### Graph ![0/20 = 0%](https://progress-bar.dev/0)
- [ ] 127. [Word Ladder (Hard)](https://leetcode.com/problems/word-ladder/)
- [ ] 128. [Longest Consecutive Sequence (Medium)](https://leetcode.com/problems/longest-consecutive-sequence/description/)
- [ ] 130. [Surrounded Regions (Medium)](https://leetcode.com/problems/surrounded-regions/description/)
- [ ] 133. [Clone Graph (Medium)](https://leetcode.com/problems/clone-graph/description/)
- [ ] 200. [Number of Islands (Medium)](https://leetcode.com/problems/number-of-islands/description/)
- [ ] 207. [Course Schedule (Medium)](https://leetcode.com/problems/course-schedule/)
- [ ] 210. [Course Schedule II (Medium)](https://leetcode.com/problems/course-schedule-ii/description/)
- [ ] 261. [Graph Valid Tree (Medium)](https://leetcode.com/problems/graph-valid-tree/description/)
- [ ] 269. [Alien Dictionary (Hard)](https://leetcode.com/problems/alien-dictionary/)
- [ ] 286. [Walls and Gates (Medium)](https://leetcode.com/problems/walls-and-gates/)
- [ ] 323. [Number of Connected Components in an Undirected Graph (Medium)](https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/description/)
- [ ] 332. [Reconstruct Itinerary (Hard)](https://leetcode.com/problems/reconstruct-itinerary/description/)
- [ ] 417. [Pacific Atlantic Water Flow (Medium)](https://leetcode.com/problems/pacific-atlantic-water-flow/description/)
- [ ] 684. [Redundant Connection (Medium)](https://leetcode.com/problems/redundant-connection/)
- [ ] 695. [Max Area of Island (Medium)](https://leetcode.com/problems/max-area-of-island/description/)
- [ ] 743. [Network Delay Time (Medium)](https://leetcode.com/problems/network-delay-time/)
- [ ] 778. [Swim in Rising Water (Hard)](https://leetcode.com/problems/swim-in-rising-water/)
- [ ] 787. [Cheapest Flights Within K Stops (Medium)](https://leetcode.com/problems/cheapest-flights-within-k-stops/description/)
- [ ] 994. [Rotting Oranges (Medium)](https://leetcode.com/problems/rotting-oranges/description/)
- [ ] 1584. [Min Cost to Connect All Points (Medium)](https://leetcode.com/problems/min-cost-to-connect-all-points/)

### Heap

### Dynamic Programming ![0/25 = 0%](https://progress-bar.dev/0)
- [ ] 5. [Longest Palindromic Substring (Medium)](https://leetcode.com/problems/longest-palindromic-substring/description/)
- [ ] 10. [Regular Expression Matching (Hard)](https://leetcode.com/problems/regular-expression-matching/)
- [ ] 55. [Jump Game (Medium)](https://leetcode.com/problems/jump-game/description/)
- [ ] 62. [Unique Paths (Medium)](https://leetcode.com/problems/unique-paths/description/)
- [ ] 70. [Climbing Stairs (Easy)](https://leetcode.com/problems/climbing-stairs/description/)
- [ ] 72. [Edit Distance (Hard)](https://leetcode.com/problems/edit-distance/)
- [ ] 91. [Decode Ways (Medium)](https://leetcode.com/problems/decode-ways/)
- [ ] 97. [Interleaving String (Medium)](https://leetcode.com/problems/interleaving-string/)
- [ ] 115. [Distinct Subsequences (Hard)](https://leetcode.com/problems/distinct-subsequences/)
- [ ] 139. [Word Break (Medium)](https://leetcode.com/problems/word-break/description/)
- [ ] 152. [Maximum Product Subarray (Medium)](https://leetcode.com/problems/maximum-product-subarray/description/)
- [ ] 198. [House Robber (Medium)](https://leetcode.com/problems/house-robber/)
- [ ] 213. [House Robber II (Medium)](https://leetcode.com/problems/house-robber-ii/)
- [ ] 300. [Longest Increasing Subsequence (Medium)](https://leetcode.com/problems/longest-increasing-subsequence/description/)
- [ ] 309. [Best Time to Buy and Sell Stock with Cooldown (Medium)](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-cooldown/)
- [ ] 312. [Burst Balloons (Hard)](https://leetcode.com/problems/burst-balloons/description/)
- [ ] 322. [Coin Change (Medium)](https://leetcode.com/problems/coin-change/description/)
- [ ] 329. [Longest Increasing Path in a Matrix (Hard)](https://leetcode.com/problems/longest-increasing-path-in-a-matrix/)
- [ ] 377. [Combination Sum IV (Medium)](https://leetcode.com/problems/combination-sum-iv/)
- [ ] 416. [Partition Equal Subset Sum (Medium)](https://leetcode.com/problems/partition-equal-subset-sum/description/)
- [ ] 494. [Target Sum (Medium)](https://leetcode.com/problems/target-sum/description/)
- [ ] 518. [Coin Change II (Medium)](https://leetcode.com/problems/coin-change-ii/)
- [ ] 647. [Palindromic Substrings (Medium)](https://leetcode.com/problems/palindromic-substrings/description/)
- [ ] 746. [Min Cost Climbing Stairs (Easy)](https://leetcode.com/problems/min-cost-climbing-stairs/)
- [ ] 1143. [Longest Common Subsequence (Medium)](https://leetcode.com/problems/longest-common-subsequence/)

## :round_pushpin: Java Utilities
- Java `Arrays` class.
- Java `Collections` class.
- Java `Math` class.
