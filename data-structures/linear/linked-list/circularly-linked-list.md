# :heavy_check_mark: Circularly Linked List
*Last Updated: 1/24/2023*

![Image of a doubly linked list](../../../images/data-structures/linear/linked-list/doubly-linked-list.png)

## :round_pushpin: Summary
- First and last nodes are connected to form a circle/cycle.
- There is no `null` end.
- There should be a reference to the `tail`.

## :round_pushpin: Representation
- Basic representation
- Uses the same node as a singly linked list.
- Just connect the last node to the `head`.
```java
// Singly Linked List Class
class SinglyLinkedList {
  Node head; // Head of list.

  // Singly Linked List Node.
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
- There is no Java circularly-linked list class.
