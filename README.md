![Last Commit](https://img.shields.io/github/last-commit/eyc94/dsna?label=Updated)
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
- [ ] [Subsets](patterns/subsets.md) ![4/10 = 40%](https://progress-bar.dev/40)
- [ ] [K-Way Merge](patterns/k-way-merge.md) ![3/7 = 43%](https://progress-bar.dev/43)
- [ ] [Top K Elements](patterns/top-k-elements.md) ![4/15 = 27%](https://progress-bar.dev/27)
- [ ] [Modified Binary Search](patterns/modified-binary-search.md) ![1/18 = 6%](https://progress-bar.dev/6)
- [ ] [Greedy](patterns/greedy.md) ![1/10 = 10%](https://progress-bar.dev/10)
- [ ] [Backtracking](patterns/backtracking.md) ![0/10 = 0%](https://progress-bar.dev/0)
- [ ] [Dynamic Programming](patterns/dynamic-programming.md) ![0/8 = 0%](https://progress-bar.dev/0)
- [ ] [Cyclic Sort](patterns/cyclic-sort.md) ![0/5 = 0%](https://progress-bar.dev/0)
- [ ] [Topological Sort](patterns/topological-sort.md) ![0/7 = 0%](https://progress-bar.dev/0)
- [ ] [Stacks](patterns/stacks.md) ![0/12 = 0%](https://progress-bar.dev/0)
- [ ] [Trie](patterns/trie.md) ![0/6 = 0%](https://progress-bar.dev/0)
- [ ] [Hash Maps](patterns/hash-maps.md) ![0/6 = 0%](https://progress-bar.dev/0)
- [ ] [Union Find](patterns/union-find.md) ![0/6 = 0%](https://progress-bar.dev/0)
- [ ] [Bitwise Manipulation](patterns/bitwise-manipulation.md) ![0/7 = 0%](https://progress-bar.dev/0)
- [ ] [Custom Data Structures](patterns/custom-data-structures.md) ![0/6 = 0%](https://progress-bar.dev/0)

## :round_pushpin: Top Leetcode Questions
Adopted from the popular [Blind](https://www.teamblind.com/post/New-Year-Gift---Curated-List-of-Top-75-LeetCode-Questions-to-Save-Your-Time-OaM1orEU) post and Needcode's curated [list](https://neetcode.io/roadmap).
- ***NOTE:*** Some questions are in the `Patterns & Techniques` section above.
- See [this](https://leetcode.com/discuss/general-discussion/460599/blind-75-leetcode-questions) for a fast Leetcode link to curated list.

### Legend
- :green_book: Easy
- :orange_book: Medium
- :closed_book: Hard
- :lock: LC Premium

### Array ![4/18 = 22%](https://progress-bar.dev/22)
- [x] 1. [:green_book: Two Sum](https://leetcode.com/problems/two-sum/description/) 
- [ ] 11. [:orange_book: Container With Most Water](https://leetcode.com/problems/container-with-most-water/description/)
- [x] 15. [:orange_book: 3Sum](https://leetcode.com/problems/3sum/description/)
- [ ] 33. [:orange_book: Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/description/)
- [ ] 36. [:orange_book: Valid Sudoku](https://leetcode.com/problems/valid-sudoku/description/)
- [ ] 42. [:closed_book: Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/description/)
- [ ] 49. [:orange_book: Group Anagrams](https://leetcode.com/problems/group-anagrams/description/)
- [x] 53. [:orange_book: Maximum Subarray](https://leetcode.com/problems/maximum-subarray/description/)
- [ ] 121. [:green_book: Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/description/)
- [ ] 128. [:orange_book: Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/description/)
- [ ] 152. [:orange_book: Maximum Product Subarray](https://leetcode.com/problems/maximum-product-subarray/description/)
- [ ] 217. [:green_book: Contains Duplicate](https://leetcode.com/problems/contains-duplicate/description/)
- [ ] 238. [:orange_book: Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/description/)
- [ ] 242. [:green_book: Valid Anagram](https://leetcode.com/problems/valid-anagram/description/)
- [ ] 271. [:orange_book: Encode and Decode Strings](https://leetcode.com/problems/encode-and-decode-strings/description/) :lock:
- [ ] 347. [:orange_book: Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/description/)

### String ![3/10 = 30%](https://progress-bar.dev/30)
- [x] 3. [:orange_book: Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/description/)
- [ ] 5. [:orange_book: Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/description/)
- [ ] 20. [:green_book: Valid Parentheses](https://leetcode.com/problems/valid-parentheses/description/)
- [ ] 49. [:orange_book: Group Anagrams](https://leetcode.com/problems/group-anagrams/description/)
- [x] 76. [:closed_book: Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/description/)
- [ ] 125. [:green_book: Valid Palindrome](https://leetcode.com/problems/valid-palindrome/description/)
- [ ] 242. [:green_book: Valid Anagram](https://leetcode.com/problems/valid-anagram/description/)
- [ ] 271. [:orange_book: Encode and Decode Strings](https://leetcode.com/problems/encode-and-decode-strings/description/) :lock:
- [x] 424. [:orange_book: Longest Repeating Character Replacement](https://leetcode.com/problems/longest-repeating-character-replacement/description/)
- [ ] 647. [:orange_book: Palindromic Substrings](https://leetcode.com/problems/palindromic-substrings/description/)

### Binary ![0/6 = 0%](https://progress-bar.dev/0)
- [ ] 136. [:green_book: Single Number](https://leetcode.com/problems/single-number/description/)
- [ ] 190. [:green_book: Reverse Bits](https://leetcode.com/problems/reverse-bits/)
- [ ] 191. [:green_book: Number of 1 Bits](https://leetcode.com/problems/number-of-1-bits/description/)
- [ ] 268. [:green_book: Missing Number](https://leetcode.com/problems/missing-number/description/)
- [ ] 338. [:green_book: Counting Bits](https://leetcode.com/problems/counting-bits/)
- [ ] 371. [:orange_book: Sum of Two Integers](https://leetcode.com/problems/sum-of-two-integers/description/)

### Interval ![4/6 = 66%](https://progress-bar.dev/66)
- [x] 56. [:orange_book: Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- [x] 57. [:orange_book: Insert Interval](https://leetcode.com/problems/insert-interval/)
- [ ] 252. [:orange_book: Meeting Rooms](https://leetcode.com/problems/meeting-rooms/description/) :lock:
- [x] 253. [:orange_book: Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/description/) :lock:
- [x] 435. [:orange_book: Non-overlapping Intervals](https://leetcode.com/problems/non-overlapping-intervals/)
- [ ] 1851. [:closed_book: Minimum Interval to Include Each Query](https://leetcode.com/problems/minimum-interval-to-include-each-query/)

### Linked List ![6/11 = 55%](https://progress-bar.dev/55)
- [ ] 2. [:orange_book: Add Two Numbers](https://leetcode.com/problems/add-two-numbers/description/)
- [x] 19. [:orange_book: Remove Nth Node From End of List](https://leetcode.com/problems/remove-nth-node-from-end-of-list/description/)
- [ ] 21. [:green_book: Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/description/)
- [x] 25. [:closed_book: Reverse Node in k-Group](https://leetcode.com/problems/reverse-nodes-in-k-group/)
- [x] 23. [:closed_book: Merge k Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/description/)
- [ ] 138. [:orange_book: Copy List with Random Pointer](https://leetcode.com/problems/copy-list-with-random-pointer/description/)
- [x] 141. [:green_book: Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/description/)
- [x] 143. [:orange_book: Reorder List](https://leetcode.com/problems/reorder-list/description/)
- [ ] 146. [:orange_book: LRU Cache](https://leetcode.com/problems/lru-cache/description/)
- [x] 206. [:green_book: Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/description/)
- [ ] 287. [:orange_book: Find the Duplicate Number](https://leetcode.com/problems/find-the-duplicate-number/description/)

### Matrix ![0/4 = 0%](https://progress-bar.dev/0)
- [ ] 48. [:orange_book: Rotate Image](https://leetcode.com/problems/rotate-image/description/)
- [ ] 54. [:orange_book: Spiral Matrix](https://leetcode.com/problems/spiral-matrix/description/)
- [ ] 73. [:orange_book: Set Matrix Zeroes](https://leetcode.com/problems/set-matrix-zeroes/description/)
- [ ] 79. [:orange_book: Word Search](https://leetcode.com/problems/word-search/description/)

### Tree ![6/18 = 33%](https://progress-bar.dev/33)
- [ ] 98. [:orange_book: Validate Binary Search Tree](https://leetcode.com/problems/validate-binary-search-tree/description/)
- [ ] 100. [:green_book: Same Tree](https://leetcode.com/problems/same-tree/description/)
- [x] 102. [:orange_book: Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/description/)
- [x] 104. [:green_book: Maximum Depth of Binary Tree](https://leetcode.com/problems/maximum-depth-of-binary-tree/description/)
- [ ] 105. [:orange_book: Construct Binary Tree from Preorder and Inorder Traversal](https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/description/)
- [ ] 110. [:green_book: Balanced Binary Tree](https://leetcode.com/problems/balanced-binary-tree/description/)
- [x] 124. [:closed_book: Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/description/)
- [x] 199. [:green_book: Binary Tree Righ Side View](https://leetcode.com/problems/binary-tree-right-side-view/description/)
- [ ] 208. [:orange_book: Implement Trie (Prefix Tree)](https://leetcode.com/problems/implement-trie-prefix-tree/description/)
- [ ] 211. [:orange_book: Design Add and Search Words Data Structure](https://leetcode.com/problems/design-add-and-search-words-data-structure/description/)
- [ ] 212. [:closed_book: Word Search II](https://leetcode.com/problems/word-search-ii/description/)
- [x] 226. [:green_book: Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree/description/)
- [ ] 230. [:orange_book: Kth Smallest Element in a BST](https://leetcode.com/problems/kth-smallest-element-in-a-bst/description/)
- [ ] 235. [:orange_book: Lowest Common Ancestor of a Binary Search Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/description/)
- [ ] 297. [:closed_book: Serialize and Deserialize Binary Tree](https://leetcode.com/problems/serialize-and-deserialize-binary-tree/description/)
- [x] 543. [:green_book: Diameter of Binary Tree](https://leetcode.com/problems/diameter-of-binary-tree/)
- [ ] 572. [:green_book: Subtree of Another Tree](https://leetcode.com/problems/subtree-of-another-tree/description/)
- [ ] 1448. [:orange_book: Count Good Nodes in Binary Tree](https://leetcode.com/problems/count-good-nodes-in-binary-tree/description/)

### Graph ![0/20 = 0%](https://progress-bar.dev/0)
- [ ] 127. [:closed_book: Word Ladder](https://leetcode.com/problems/word-ladder/)
- [ ] 128. [:orange_book: Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/description/)
- [ ] 130. [:orange_book: Surrounded Regions](https://leetcode.com/problems/surrounded-regions/description/)
- [ ] 133. [:orange_book: Clone Graph](https://leetcode.com/problems/clone-graph/description/)
- [ ] 200. [:orange_book: Number of Islands](https://leetcode.com/problems/number-of-islands/description/)
- [ ] 207. [:orange_book: Course Schedule](https://leetcode.com/problems/course-schedule/)
- [ ] 210. [:orange_book: Course Schedule II](https://leetcode.com/problems/course-schedule-ii/description/)
- [ ] 261. [:orange_book: Graph Valid Tree](https://leetcode.com/problems/graph-valid-tree/description/) :lock:
- [ ] 269. [:closed_book: Alien Dictionary](https://leetcode.com/problems/alien-dictionary/) :lock:
- [ ] 286. [:orange_book: Walls and Gates](https://leetcode.com/problems/walls-and-gates/) :lock:
- [ ] 323. [:orange_book: Number of Connected Components in an Undirected Graph](https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/description/) :lock:
- [ ] 332. [:closed_book: Reconstruct Itinerary](https://leetcode.com/problems/reconstruct-itinerary/description/)
- [ ] 417. [:orange_book: Pacific Atlantic Water Flow](https://leetcode.com/problems/pacific-atlantic-water-flow/description/)
- [ ] 684. [:orange_book: Redundant Connection](https://leetcode.com/problems/redundant-connection/)
- [ ] 695. [:orange_book: Max Area of Island](https://leetcode.com/problems/max-area-of-island/description/)
- [ ] 743. [:orange_book: Network Delay Time](https://leetcode.com/problems/network-delay-time/)
- [ ] 778. [:closed_book: Swim in Rising Water](https://leetcode.com/problems/swim-in-rising-water/)
- [ ] 787. [:orange_book: Cheapest Flights Within K Stops](https://leetcode.com/problems/cheapest-flights-within-k-stops/description/)
- [ ] 994. [:orange_book: Rotting Oranges](https://leetcode.com/problems/rotting-oranges/description/)
- [ ] 1584. [:orange_book: Min Cost to Connect All Points](https://leetcode.com/problems/min-cost-to-connect-all-points/)

### Heap ![0/9 = 0%](https://progress-bar.dev/0)
- [ ] 23. [:closed_book: Merge k Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/description/)
- [ ] 215. [:orange_book: Kth Largest Element in an Array](https://leetcode.com/problems/kth-largest-element-in-an-array/)
- [ ] 295. [:closed_book: Find Median from Data Stream](https://leetcode.com/problems/find-median-from-data-stream/description/)
- [ ] 347. [:orange_book: Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/description/)
- [ ] 355. [:orange_book: Design Twitter](https://leetcode.com/problems/design-twitter/)
- [ ] 621. [:orange_book: Task Scheduler](https://leetcode.com/problems/task-scheduler/)
- [ ] 703. [:green_book: Kth Largest Element in a Stream](https://leetcode.com/problems/kth-largest-element-in-a-stream/)
- [ ] 973. [:orange_book: K Closest Points to Origin](https://leetcode.com/problems/k-closest-points-to-origin/description/)
- [ ] 1046. [:green_book: Last Stone Weight](https://leetcode.com/problems/last-stone-weight/description/)

### Dynamic Programming ![0/25 = 0%](https://progress-bar.dev/0)
- [ ] 5. [:orange_book: Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/description/)
- [ ] 10. [:closed_book: Regular Expression Matching](https://leetcode.com/problems/regular-expression-matching/)
- [ ] 55. [:orange_book: Jump Game](https://leetcode.com/problems/jump-game/description/)
- [ ] 62. [:orange_book: Unique Paths](https://leetcode.com/problems/unique-paths/description/)
- [ ] 70. [:green_book: Climbing Stairs](https://leetcode.com/problems/climbing-stairs/description/)
- [ ] 72. [:closed_book: Edit Distance](https://leetcode.com/problems/edit-distance/)
- [ ] 91. [:orange_book: Decode Ways](https://leetcode.com/problems/decode-ways/)
- [ ] 97. [:orange_book: Interleaving String](https://leetcode.com/problems/interleaving-string/)
- [ ] 115. [:closed_book: Distinct Subsequences](https://leetcode.com/problems/distinct-subsequences/)
- [ ] 139. [:orange_book: Word Break](https://leetcode.com/problems/word-break/description/)
- [ ] 152. [:orange_book: Maximum Product Subarray](https://leetcode.com/problems/maximum-product-subarray/description/)
- [ ] 198. [:orange_book: House Robber](https://leetcode.com/problems/house-robber/)
- [ ] 213. [:orange_book: House Robber II](https://leetcode.com/problems/house-robber-ii/)
- [ ] 300. [:orange_book: Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/description/)
- [ ] 309. [:orange_book: Best Time to Buy and Sell Stock with Cooldown (Medium)](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-cooldown/)
- [ ] 312. [:closed_book: Burst Balloons](https://leetcode.com/problems/burst-balloons/description/)
- [ ] 322. [:orange_book: Coin Change](https://leetcode.com/problems/coin-change/description/)
- [ ] 329. [:closed_book: Longest Increasing Path in a Matrix](https://leetcode.com/problems/longest-increasing-path-in-a-matrix/)
- [ ] 377. [:orange_book: Combination Sum IV](https://leetcode.com/problems/combination-sum-iv/)
- [ ] 416. [:orange_book: Partition Equal Subset Sum](https://leetcode.com/problems/partition-equal-subset-sum/description/)
- [ ] 494. [:orange_book: Target Sum](https://leetcode.com/problems/target-sum/description/)
- [ ] 518. [:orange_book: Coin Change II](https://leetcode.com/problems/coin-change-ii/)
- [ ] 647. [:orange_book: Palindromic Substrings](https://leetcode.com/problems/palindromic-substrings/description/)
- [ ] 746. [:green_book: Min Cost Climbing Stairs](https://leetcode.com/problems/min-cost-climbing-stairs/)
- [ ] 1143. [:orange_book: Longest Common Subsequence](https://leetcode.com/problems/longest-common-subsequence/)

### Math & Geometry ![1/5 = 20%](https://progress-bar.dev/20)
- [ ] 43. [:orange_book: Multiple Strings](https://leetcode.com/problems/multiply-strings/)
- [ ] 50. [:orange_book: Pow(x,n)](https://leetcode.com/problems/powx-n/)
- [ ] 66. [:green_book: Plus One](https://leetcode.com/problems/plus-one/)
- [x] 202. [:green_book: Happy Number](https://leetcode.com/problems/happy-number/)
- [ ] 2013. [:orange_book: Detect Squares](https://leetcode.com/problems/detect-squares/)

## :round_pushpin: Java Utilities
- Java `Arrays` class.
- Java `Collections` class.
- Java `Math` class.
