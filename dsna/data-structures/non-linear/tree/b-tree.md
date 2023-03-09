# :heavy_check_mark: B-Tree
*Last Updated: 1/25/2023*

<!-- ![Image of a b-tree]() -->

## :round_pushpin: Summary
- Self-balancing Binary Search Tree (BST).
- Assumed everything is in main memory.
- Think of the huge amount of data that cannot fit in main memory.
  - When number of keys is high, data is read from the disk in blocks.
  - Disk access time is higher compared to main memory access time.
- Reduce number of disk accesses.
- B-Tree is a fat tree.
  - Height is kept low by putting max possible keys in a node.
  - Node size is kept equal to disk block size.
- Also known as "large key" trees.
- Shallow height leads to less disk I/O.
- Suited for storage systems that have slow, bulky data access like HDD, flash memory, and CDs.

## :round_pushpin: Operations
- `N` is the number of elements in a B-Tree.
### Search
- Time Complexity: `O(log N)`

### Insert
- Time Complexity: `O(log N)`

### Delete
- Time Complexity: `O(log N)`

## :round_pushpin: Properties
- Leaves are at the same level.
- Defined by term minimum degree `t`.
  - Depends on the disk block size.
- All nodes except the root must contain `t - 1` keys.
  - Root may have minimum of 1 key.
- All nodes (including root) may contain at most `2 * (t - 1)` keys.
- Number of children in a node equals number of keys in it plus 1.
- All keys of node are sorted in increasing order.
  - Child between two keys `k1` and `k2` contains all keys in the range from `k1` and `k2`.
- Insertion happens only at the leaf node.
