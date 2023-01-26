# :heavy_check_mark: Binary Tree
*Last Updated: 1/25/2023*

![Image of a Binary Tree](../../../images/data-structures/non-linear/tree/binary-tree.png)

## :round_pushpin: Summary
- Type of tree data structure.
- Composed of nodes.
  - Each node has at most two children (left and right).
- Tree begins from the root node.

## :round_pushpin: Representation
- Node representation:
```java
class Node {
  int key;
  Node left;
  Node right;

  public Node(int item) {
    key = item;
    left = null;
    right = null;
  }
}
```
## :round_pushpin: Properties
1. Max number of nodes at level, `l`, of a binary tree is 2<sup>l</sup>.
  a. Level is the number of nodes from root to node.
  b. Level of the root is 0.
2. Max number of nodes in a binary tree of height `h` is 2<sup>h</sup> - 1.
  a. Height of a tree is max number of nodes on root-to-leaf path.
  b. height of tree with 1 node is 1.
3. In a Binary Tree with `N` nodes, the minimum possible height (minimum number of levels) is log<sub>2</sub>N + 1.
  a. Each level should have at least 1 element, so height cannot be more than `N`.
4. A Binary Tree with `L` leaves has at least |log<sub>2</sub>L| + 1 levels.
  a. Binary Tree has max leaves when all levels are filled.
5. In a Binary Tree, if every node has 0 or 2 children, the number of leaf nodes is always one more than nodes with two children.
6. In a non-empty Binary Tree, if `N` is the total number of nodes and `E` is the total number of edges, `E = N - 1`.

## :round_pushpin: Types
- Types based on number of children:
  - [Full Binary Tree](full-binary-tree.md)
  - [Degenerate Binary Tree](degenerate-binary-tree.md)
  - [Skewed Binary Tree](skewed-binary-tree.md)
- Types based on completion of levels:
  - [Complete Binary Tree](complete-binary-tree.md)
  - [Perfect Binary Tree](perfect-binary-tree.md)
  - [Balanced Binary Tree](balanced-binary-tree.md)
- Other types:
  - [Binary Search Tree](binary-search-tree.md)
  - [AVL Tree](avl-tree.md)
  - [Red-Black Tree](red-black-tree.md)
  - B Tree
  - B+ Tree
  - Segment Tree

## :round_pushpin: Operations
- Insertion
- Removal
- Search
- Traversal

## :round_pushpin: Traversals
- See general tree for tree traversals: [Here](tree.md).
- Depth First Search (DFS)
  - Preorder
  - Inorder
  - Postorder
- Breadth First Search (BFS)
  - Level Order
