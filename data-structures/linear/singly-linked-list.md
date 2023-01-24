# :heavy_check_mark: Singly Linked List
*Last Updated: 1/24/2023*

![Image of a linked list](../../images/data-structures/linear/linked-list/singly-linked-list.png)

## :round_pushpin: Summary
- Traversal of items in the forward direction only.

## :round_pushpin: Representation
```java
// Linked List Class
class LinkedList {
  Node head; // Head of list.

  class Node {
    int data;
    Node next;

    // Constructor to create a new node.
    Node(int d) {
      data = d;
      next = null;
    }
  }
}
```

## :round_pushpin: Operations

