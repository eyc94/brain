# :heavy_check_mark: Quick Sort
*Last Updated: 1/30/2023*

![Image of the quick sort algorithm](../images/sorting/quick-sort/quick-sort.png)

## :round_pushpin: TLDR
**Time Complexity [Worst]:** <code>O(N<sup>2</sup>)</code>
**Time Complexity [Average]:** <code>O(N log N)</code>

**Space Complexity:** `O(1)`

## :round_pushpin: Summary
- In place sorting algorithm.
- Done recursively.
- `Divide & Conquer` paradigm.
- Think of the word `pivot`. Pivot means one of the 3:
  - Pivot is in the final, sorted array (correct position).
  - Items to the left are smaller.
  - Items to the right are larger.
- It picks an element as a pivot and partitions the array around the picked pivot.
- Many different versions of quick sort that pick the pivot in different ways.
  - `Median-of-three` method: Get the first, middle, and last item of the array. We sort them, and get the median. The median is our pivot.
  - Always picking the first element.
  - Always picking the last element.
  - Picking a random element.

## :round_pushpin: Explanation
- Basically, you pick a pivot.
- You place that pivot at its correct spot by recurively placing elements smaller than the pivot to its left and elements larger than the pivot to its right.
- Simple explanation:
  - Allowing students to sort themselves by height.
  - They do this be referencing their own height with a reference height (pivot).

## :round_pushpin: Code
The code below uses the last element as the pivot. This is also called the `Lomuto Partition`. You can change this to choose any other element as the pivot.

A more optimized implementation is `Hoare's Partition` because it does three times less swaps on average.
```java
// Utility function to swap two elements in an array.
public void swap(int[] arr, int i, int j) {
  int temp = arr[i];
  arr[i] = arr[j];
  arr[j] = temp;
}

/*
  This function takes the last element as a pivot.
  It places all smaller (smaller than pivot) to the left of the pivot.
  It places the pivot element at its correct position in sorted array.
*/
public int partition(int[] arr, int low, int high) {
  // Grab the pivot.
  int pivot = arr[high];

  // Index that represents the swappable position.
  // Initially out of bounds in the array bounds.
  int i = (low - 1);
  // Iterate bounds until the far-right boundary (stop before processing pivot).
  for (int j = low; j <= high - 1; j++) {
    // If current element < pivot.
    if (arr[j] < pivot) {
      // Increment index to prepare to swap.
      i++;
      swap(arr, i, j);
    }
  }

  // Swap the pivot with the position i + 1.
  // This position is where the pivot is supposed to go into.
  swap(arr, i + 1, high);

  // Return i + 1 as the partition index (i.e. the index where the pivot should be)
  return (i + 1);
}

/*
  Main function that implements Quick Sort.
  arr[]:  Array to be sorted.
  low:    Starting index.
  high:   Ending index.
*/
public void quickSort(int[] arr, int low, int high) {
  // If the low crosses the high, we are at the base case.
  if (low < high) {
    // Find the partition index (i.e. where we should split array in half).
    int partitionIndex = partition(arr, low, high);

    // Sort the left half.
    quickSort(arr, low, partitionIndex - 1);
    // Sort the right half.
    quickSort(arr, partitionIndex + 1, high);
  }
}
```

## :round_pushpin: Quick Sort vs. Merge Sort
### Array Implementation
- Quick sort is an in-place algorithm and merge sort isn't.
- Quick sort is tail-recursive, so tail call optimizations is done.

### Linked List Implementation
- Linked list nodes may not be adjacent in memory (like arrays are).
- Merge sort can be implemented without extra space for linked lists.
- We cannot do random access for linked lists (and quick sort requires this).

## :round_pushpin: Advantages
- It is a divide and conquer algorithm.
- Efficient on large datasets.
- Stable sort.
- Low overhead.

## :round_pushpin: Disadvantages
- Worst-case complexity of <code>O(N<sup>2</sup>)</code>.
- Not a good choice for small datasets.
- Sensitive to the choice of a pivot.
- Not cache-efficient.

## :round_pushpin: Analysis
**Time Complexity [Worst]:** <code>O(N<sup>2</sup>)</code>
**Time Complexity [Average]:** <code>O(N log N)</code>
- Although, quadratic is slower than Merge Sort or Heap Sort, Quick Sort is still faster in practice.
- This is because the worst case can barely occur if you choose a good pivot.
- However, Merge Sort is still considered better when data is huge and stored in external storage.

**Space Complexity:** `O(1)`
