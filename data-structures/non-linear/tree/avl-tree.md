# :heavy_check_mark: AVL Tree
*Last Updated: 1/25/2023*

![Image of an AVL Tree](../../../images/data-structures/non-linear/tree/avl-tree.png)

## :round_pushpin: Summary
- Self-balancing Binary Search Tree (BST).
- Difference between heights of left and right subtrees for any node cannot be more than one.

## :round_pushpin: Properties
### Left Rotation
![Image of a left rotation of an AVL tree](../../../images/data-structures/non-linear/tree/avl-tree-left-rotation.png)
- When node is added into the right subtree of the right subtree.
  - If tree is not balanced, do a left rotation.

### Right Rotation
![Image of a right rotation of an AVL tree](../../../images/data-structures/non-linear/tree/avl-tree-right-rotation.png)
- When node is added into the left subtree of the left subtree.
  - If tree is not balanced, do a right rotation.

### Left-Right Rotation
![Image of a left rotation of an AVL tree](../../../images/data-structures/non-linear/tree/avl-tree-left-right-rotation.png)
- First left rotation takes place after that right rotation executes.

### Right-Left Rotation
![Image of a left rotation of an AVL tree](../../../images/data-structures/non-linear/tree/avl-tree-right-left-rotation.png)
- First right rotation takes place after that left rotation executes.
