# :heavy_check_mark: Java Queue Interface
*Last Updated: 1/24/2023*

![Image of the Java Queue interface](../../../images/data-structures/linear/queue/java-queue-interface-diagram.png)

## :round_pushpin: Summary
- `Queue` interface present in `java.util` package.
- Extends `Collection` interface.
- This interface needs a class for declaration.
  - Two are `PriorityQueue` and `LinkedList` classes in Java.
  - Note that the `PriorityQueue` provides us a way to process objects based on priority.
    - See more of `PriorityQueue` [here](java-priorityqueue.md).

## :round_pushpin: Operations (API)
- [Documentation](https://docs.oracle.com/javase/8/docs/api/java/util/Queue.html)
- Common operations:
  - `offer`
  - `poll`
  - `peek`
  - `add`
  - `remove`

## :round_pushpin: Examples
- Queue is an interface.
  - Cannot be created with type queue.
  - Need a class that extends this list to create an object.
- Instantiate with `LinkedList` implementation:
```java
Queue<Integer> queue = new LinkedList<>();
```

- Instantiate with `PriorityQueue` implementation:
```java
Queue<Integer> queue = new PriorityQueue<>();
```

- Common operations:
```java
Queue<Integer> queue = new LinkedList<>();
queue.offer(1); // [1]
queue.offer(2); // [1, 2]
queue.offer(3); // [1, 2, 3]
System.out.println(queue.peek()) // 1
queue.poll(); // [2, 3]
System.out.println(queue.peek()) // 2

Queue<Integer> pq = new PriorityQueue<>();
pq.offer(5); // [5]
pq.offer(1); // [1, 5]
pq.offer(3); // [1, 3, 5]
System.out.println(pq.peek()) // 1
pq.poll(); // [3, 5]
System.out.println(pq.peek()) // 3
```
