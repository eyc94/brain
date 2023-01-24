# :heavy_check_mark: Java LinkedList
*Last Updated: 1/24/2023*

## :round_pushpin: Summary
- Part of Collection framework in `java.util` package.
- Implementation of the Linked List data structure.

## :round_pushpin: Features
![Image of how an extended LinkedList diagram](../../images/data-structures/linear/linked-list/linked-list-diagram-extended.png)

## :round_pushpin: Operations (API)
- [Documentation](https://docs.oracle.com/javase/7/docs/api/java/util/LinkedList.html)
- Common operations:
  - `add`
  - `addAll`
  - `contains`
  - `get`
  - `isEmpty`
  - `size`

## :round_pushpin: Examples
- Instantiate an empty linked list:
```java
LinkedList<Integer> list = new LinkedList<>();
```

- Instantiate with another collection, `c`:
```java
LinkedList<Integer> list = new LinkedList<>(c);
```

- Common operations:
```java
LinkedList<Integer> list = new LinkedList<>();
list.add(1); // [1]
list.add(2); // [2]
list.addLast(100); // [1, 2, 100]
list.addFirst(101); // [101, 1, 2, 100]
list.add(1); // [101, 1, 2, 100, 1]

list.remove(1); // [101, 2, 100, 1]
list.removeFirst(); // [2, 100, 1]
list.removeLast(); // [2, 100]
```

## :round_pushpin: Misc
- Can be used to implement the `List` interface of Java.
  - Implemented as a doubly linked list.
