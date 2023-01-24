# :heavy_check_mark: Array
*Last Updated: 1/23/2023*

![Image of an array](../../images/data-structures/linear/array/array.png)

## :round_pushpin: Summary
- Linear data structure.
- Collection of items.
- Stored at contiguous memory locations.
- Usually holds the same data types.
- Usually indexed starting at 0.

## :round_pushpin: Characteristics
- Index-based data structure.
- Can handle complex data structures by storing data in a two-dimensional array.
- Used to implement other data structures (i.e. stack, queue, heap, hash tables, etc).

## :round_pushpin: Operations
Operations on an array, `A`, at index, `i`, uses the bracket notation: `A[i]`.
### Read/Access
- Constant time operation: `O(1)`.

### Update
- Constant time operation: `O(1)`.

### Insert/Create
- Inserting elements in the end: Constant time operation - `O(1)`.
  - Resizing is necessary when the array is full.
  - There is a resize factor, `k`.
  - Create a new array with a new size, and copy over the old values into the new array.
  - This increases time complexity to be linear in the worst case.
  - However, resizing is infrequent, so it's still constant.
- Inserting elements in the middle: Linear time operation - `O(n)` where `n` is the length of the array.
  - Inserting elements in the middle require every element to its right to shift right by one cell.

### Delete
- Deleting elements in the end: Constant time operation - `O(1)`.
- Deleting elements in the middle: Linear time operation - `O(n)` where `n` is the length of the array.
  - Deleting elements in the middle require every element to its left to shift left by one cell.

## :round_pushpin: Java Syntax/Libraries
- Basic arrays in Java are fixed-size.
- Java `Arrays` class: [Reference](https://docs.oracle.com/javase/7/docs/api/java/util/Arrays.html)
  - Some static utility methods: `asList`, `fill`, `sort`, and `toString`.
- The `ArrayList` type is a dynamically-resizing array.
  - [Documentation](https://docs.oracle.com/javase/8/docs/api/java/util/ArrayList.html)
  - [ArrayList Notes](./arraylist.md)
  - Better replacement than the basic array (more API methods).
- Allocating and initializing an array: `new int[] { 1, 2, 3 }`.
- Instantiate a 2D array: `new Integer[3][]`.
  - Holds 3 rows.
- Get the length of an array by accessing the `length` field.
  - `Collections` use the `size()` method, and the `String` uses the `length()` method.

## :round_pushpin: Misc
- Add misc notes here...
