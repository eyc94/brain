# :heavy_check_mark: Linked List
*Last Updated: 1/24/2023*

![Image of a linked list](../../images/data-structures/linear/linked-list/linked-list.png)

## :round_pushpin: Summary
- Linear data structure.
- Not stored in contiguous memory.
- Ordered collection of values.
- Elements of a list are linked using pointers to the next element.
  - Consists of nodes that have references (links) to the next node in the list.
- There is a `head` pointer pointing to the first element.
  - Empty list has this pointer pointing to `null`.

## :round_pushpin: Linked List vs Array
### Advantages
- Arrays need to declare size and resize accordingly.
  - Expensive when adding/removing elements.
- In linked lists, you just need to know the position and traverse to it and re-link nodes.

### Disadvantages
- We have to access nodes sequentially.
- Extra memory for a pointer is needed for each element.
- Not cache-friendly.
- Reverse traversing not possible in singly-linked lists.
- Pointers are confusing.
- Reading/Searching for an element is expensive (not constant).
- Sorting is complicated.

## :round_pushpin: Types
- [Singly-Linked List](singly-linked-list.md)
- [Doubly-Linked List](doubly-linked-list.md)
- Circularly-Linked List
- Doubly Circular Linked List

## :round_pushpin: Characteristics
- Uses extra memory to store links.
- Initial size not needed for initialization (like arrays do).
- Implements stack, queue, graphs, etc.
- First node is called the head.
- Last node is called the tail and always points to `null`.
- Insertion and deletion on the ends is easy.
- Each node contains a next pointer to the next node.

## :round_pushpin: Operations
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

## :round_pushpin: Java Syntax/Libraries
- Java has a standard linked list library called `LinkedList`: [Documentation](https://docs.oracle.com/javase/7/docs/api/java/util/LinkedList.html)
- [`LinkedList` notes](./java-linkedlist.md)
