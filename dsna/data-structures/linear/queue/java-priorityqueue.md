# :heavy_check_mark: Java PriorityQueue Class
*Last Updated: 1/24/2023*

![Image of the Java PriorityQueue class](../../../images/data-structures/linear/queue/java-priorityqueue-class-diagram.png)

## :round_pushpin: Summary
- Objects are based on priority.
- Based on priority heap.
- Ordered naturally or by a Comparator provided at queue construction time.

## :round_pushpin: Characteristics
- Does not permit `null`.
- Cannot create PriorityQueue of objects that are non-comparable.
- Unbounded
- Head of the queue is the "least" element.
- Not thread-safe (`PriorityBlockingQueue` class is thread-safe).

## :round_pushpin: Operations (API)
- [Documentation](https://docs.oracle.com/javase/7/docs/api/java/util/PriorityQueue.html)
- Adding and removing methods are `O(log n)` time complexity where `n` is the size of the queue.
- Common operations:
  - `offer`
  - `poll`
  - `peek`

## :round_pushpin: Examples
PriorityQueue is an class (i.e. implementation).
- Instantiate with default capacity of 11:
```java
Queue<Integer> queue = new PriorityQueue<>();
```

- Instantiate with another collection, `c`:
```java
Queue<Integer> queue = new PriorityQueue<>(c);
```

- Instantiate with initial capacity:
```java
Queue<Integer> queue = new PriorityQueue<>(5);
```

- Instantiate with comparator, `comparator`, and initial capacity:
```java
Queue<Integer> queue = new PriorityQueue<>(5, comparator);
```

- Common operations:
```java
Queue<Integer> pq = new PriorityQueue<>();
pq.offer(5); // [5]
pq.offer(1); // [1, 5]
pq.offer(3); // [1, 3, 5]
System.out.println(pq.peek()) // 1
pq.poll(); // [3, 5]
System.out.println(pq.peek()) // 3
```
