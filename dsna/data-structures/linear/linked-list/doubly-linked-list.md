# :heavy_check_mark: Doubly Linked List
*Last Updated: 1/24/2023*

![Image of a doubly linked list](../../../images/data-structures/linear/linked-list/doubly-linked-list.png)

## :round_pushpin: Summary
- Sometimes abbreviated to DLL.
- Traversal can be done in forward and backward directions.
- Every node contains a `prev` pointer pointing to the previous node.

## :round_pushpin: Singly vs Doubly
### Advantages
- Can traverse in both directions.
- Deleting is more efficient if given the node.
- Can insert nodes before a given node.

### Disadvantages
- Every node requires extra space for a previous pointer.

## :round_pushpin: Representation
- Basic representation
```java
// Doubly Linked List Class
class DoublyLinkedList {
  Node head; // Head of list.

  // Doubly Linked List Node.
  class Node {
    int data;
    Node prev;
    Node next;

    // Constructor to create a new node.
    // The next and prev is null by default.
    Node(int d) {
      data = d;
    }
  }
}
```

## :round_pushpin: Operations
- Can now add/delete a node before and after a given node.
- `n` is the length of the list.
### Read/Access
- Reading elements at the head: Constant time operation - `O(1)`.
- Reading elements at the tail: Constant time operation - `O(1)`.
- Reading elements in the middle: Linear time operation - `O(n)`.

### Update
- Updating elements at the head: Constant time operation - `O(1)`.
- Updating elements at the tail: Constant time operation - `O(1)`.
- Updating elements in the middle: Linear time operation - `O(n)`.

### Insert/Create
- Inserting elements at the head: Constant time operation - `O(1)`.
- Inserting elements at the tail: Constant time operation - `O(1)`.
- Inserting elements in the middle: Linear time operation - `O(n)`.

### Delete
- Deleting elements at the head: Constant time operation - `O(1)`.
- Deleting elements at the tail: Constant time operation - `O(1)`.
- Deleting elements in the middle: Linear time operation - `O(n)`.

## :round_pushpin: Misc
- There is no Java doubly-linked list class.
