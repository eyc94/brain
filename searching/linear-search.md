# :heavy_check_mark: Linear Search
*Last Updated: 1/31/2023*

![Image of the linear search algorithm](../images/searching/linear-search/linear-search.png)

## :round_pushpin: TLDR
**Time Complexity:** `O(N)`

**Space Complexity:** `O(1)`

## :round_pushpin: Summary
- We just sequentially iterate through the array and look for the target.

## :round_pushpin: Code
```java
public int linearSearch(int[] arr, int target) {
  int N = arr.length;
  for (int i = 0; i < N; i++) {
    if (arr[i] == target) {
      return i;
    }
  }
  return -1;
}
```
- Note that we return -1 if the target is not found.

## :round_pushpin: Advantages
- Simple to implement and easy to understand.
- Can be used irrespective to whether array is sorted or not.
- Can be used on any data type.
- Does not require additional memory.

## :round_pushpin: Disadvantages
- Complexity is linear.
- Not suitable for large arrays.
- Can be less efficient.

## :round_pushpin: Analysis
**Time Complexity:** `O(N)`

**Space Complexity:** `O(1)`
