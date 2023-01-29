# :heavy_check_mark: Insertion Sort
*Last Updated: 1/29/2023*

![Image of the insertion sort algorithm](../images/sorting/insertion-sort/insertion-sort.png)

## :round_pushpin: TLDR
**Time Complexity:** <code>O(N<sup>2</sup>)</code>

**Space Complexity:** `O(1)`

## :round_pushpin: Summary
- In-place sorting algorithm.
- Simple and straightforward.
- Similar to selection sort.
  - Similar in that in selection sort, you're looking for the smallest value in each iteration.
  - In insertion sort, you're looking to place the current number in the correct spot.
- There are two partitions: Left is sorted and right is unsorted.
- Iterate through the unsorted values and keep swapping them into the sorted portion is the value of it is less than the value to be swapped.

## :round_pushpin: Explanation
Simple explanation:
- This is like having a hand of cards.
- When sorting the cards, you pick a card and place it in the correct order/position on the left side.
- Basically, you grab a card, and you *insert* this card in the sorted partition in the correct spot.

## :round_pushpin: Code
The code below can be used to sort in descending order as well. Just change the condition.
```java
public void insertionSort(int[] arr) {
  // Grab the array length.
  int n = arr.length;

  // Iterate through the unsorted portion. The far left is automatically considered sorted.
  for (int i = 1; i < n; i++) {
    // Grab the value.
    int key = arr[i];

    // Grab the index to the left of the current 'i' position.
    int j = i - 1;
    // Iterate while 'j' hasn't passed the left boundary AND the value of 'j' is greater than the value of 'i'.
    while (j >= 0 && arr[j] > key) {
      // Move the left value to the current position of 'i'.
      arr[j + 1] = arr[j];
      // Decrement 'j'.
      j = j - 1;
    }

    // Once all the values are moved to the right, 'j + 1' will point at the correct location for the key (value at 'i').
    arr[j + 1] = key;
  }
}
```
- We iterate through every number.
- For every number, we place this number in the correct spot to its *left*.
- To do this, we swap the current number with the number to its left *IFF* the left value is greater than the current number.
  - Basically, we are moving all values to the right until we find the correct spot for the current number.
- Then we place that number in the correct spot.
- Rinse and repeat.

## :round_pushpin: Analysis
**Time Complexity:** <code>O(N<sup>2</sup>)</code>

**Space Complexity:** `O(1)`
