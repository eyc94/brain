# :heavy_check_mark: Java Deque Interface
*Last Updated: 1/24/2023*

![Image of Deque interface diagram](../../../images/data-structures/linear/stack/deque-interface-diagram.png)

## :round_pushpin: Summary
- Subtype of `queue` interface.
- Deque is related to the double-ended queue.
- Supports addition and removal on both ends.
- Can either be a stack or queue.

## :round_pushpin: Operations (API)
- [Documentation](https://docs.oracle.com/javase/7/docs/api/java/util/Deque.html)
- Common operations:
  - `add`
  - `addFirst`
  - `addLast`
  - `getFirst`
  - `getLast`
  - `removeFirst`
  - `removeLast`

## :round_pushpin: Examples
- Deque is an interface.
  - Cannot be created with type deque.
  - Need a class that extends this list to create an object.
- Instantiate:
```java
Deque<Integer> deque = new LinkedList<>();
```

- Common operations:
```java
Deque<Integer> deque = new LinkedList<>();
deque.add(1); // [1]
deque.add(2); // [1, 2]
deque.add(3); // [1, 2, 3]
System.out.println(deque.getFirst()) // 1
deque.addFirst(-1); // [-1, 1, 2, 3]
deque.removeLast(); // [-1, 1, 2]
```
