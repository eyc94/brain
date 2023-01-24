# :heavy_check_mark: Singly Linked List
*Last Updated: 1/24/2023*

![Image of a singly linked list](../../images/data-structures/linear/linked-list/singly-linked-list.png)

## :round_pushpin: Summary
- Sometimes abbreviated to SLL.
- Traversal of items in the forward direction only.
- This is basically the basic linked list.
  - See [Linked List](linked-list.md) section for more information.

## :round_pushpin: Representation
- Basic representation
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
- Exact same operations as the basic [Linked List](linked-list.md).
- `n` is the length of the list.
### Read/Access
- Reading elements at the head: Constant time operation - `O(1)`.
- Reading elements at the tail: Linear time operation - `O(n)`.
- Reading elements in the middle: Linear time operation - `O(n)`.

### Update
- Updating elements at the head: Constant time operation - `O(1)`.
- Updating elements at the tail: Linear time operation - `O(n)`.
- Updating elements in the middle: Linear time operation - `O(n)`.

### Insert/Create
- Inserting elements at the head: Constant time operation - `O(1)`.
- Inserting elements at the tail: Linear time operation - `O(n)`.
- Inserting elements in the middle: Linear time operation - `O(n)`.

### Delete
- Deleting elements at the head: Constant time operation - `O(1)`.
- Deleting elements at the tail: Linear time operation - `O(n)`.
- Deleting elements in the middle: Linear time operation - `O(n)`.
