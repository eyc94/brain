# :heavy_check_mark: Binary Search
*Last Updated: 1/31/2023*

![Image of the binary search algorithm](../images/searching/binary-search/binary-search.png)

## :round_pushpin: TLDR
**Time Complexity:** `O(log N)`

**Space Complexity:** `O(1)`

## :round_pushpin: Summary
- Repeatedly divides the search interval in half.
- You have to be given a sorted array.
- Finding an element in the array based on the midpoint's value.
- Cut the input in half depending on this value.

## :round_pushpin: Explanation
Algorithm:
1. Sort the array in ascending order.
2. Set low index as the first element of the array and high index as the last element.
3. Set the middle as the average of low and high.
4. If the middle is the target, return middle index.
5. If the target is less than middle element, search left half.
6. If the target is greater than element at middle, search right half.
7. Repeat 3-6 until element is found *or* there is no target in the array.

## :round_pushpin: Code
```java
public int binarySearch(int[] arr, int low, int high, int target) {
  while (low <= high) {
    int mid = low + (high - low) / 2;

    if (arr[mid] == target) {
      return mid;
    } else if (arr[mid] < target) {
      low = mid + 1;
    } else {
      high = mid - 1;
    }
  }

  return -1;
}
```
- Note that we return -1 if the target is not found.

## :round_pushpin: Finding the Average
- Note that we use `int mid = low + (high - low) / 2` as opposed to `int mid = (low + high) / 2`.
- Why?
  - This is because it fails for larger values of low and high.
  - It fails if the sum of low and high is greater than the max possible integer <code>2<sup>31</sup> - 1</code>.
  - The sum overflows to a negative value.

## :round_pushpin: Advantages
- Faster than linear search.
- More efficient than other searching algorithms (interpolation search or exponential search).
- Simple to implement and easy to understand.
- Can be used for sorted arrays and sorted linked lists.
- Well suited for large datasets.
- Building block for more complex algorithms.

## :round_pushpin: Disadvantages
- Requires array to be sorted.
- If the array is not sorted, this adds additional `O(N log N)` complexity.
- Array elements must be comparable.
- Might be less efficient than hash tables.

## :round_pushpin: Analysis
**Time Complexity:** `O(log N)`

**Space Complexity:** `O(1)`
