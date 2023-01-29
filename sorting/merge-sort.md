# :heavy_check_mark: Merge Sort
*Last Updated: 1/29/2023*

![Image of the merge sort algorithm](../images/sorting/merge-sort/merge-sort.png)

## :round_pushpin: TLDR
**Time Complexity:** <code>O(N log N)</code>

**Space Complexity:** `O(N)`

## :round_pushpin: Summary
- Usually done recursively.
- Think of `Divide & Conquer`.
- Works by dividing an array into smaller subarrays, sorting each subarray, and then merging the sorted subarrays back together to form the final sorted array.
- It can sort large arrays relatively quickly.
- It is a stable sort.
- Often used with quicksort.


## :round_pushpin: Explanation
Simple explanation:
- Think of having a recursive algorithm that constantly splits the array in half until it cannot be divided further.
- If the array becomes empty or has 1 element left, dividing stops (base case).
- Once the halves are sorted, we start the merge operation

## :round_pushpin: Code
The code below can be used to sort in descending order as well. Just change the condition.
```java
// Merges two subarrays of arr[].
// First subarray: arr[left...mid].
// Second subarray: arr[mid + 1...right].
public void merge(int[] arr, int left, int mid, int right) {
  /*
    Basically, we are creating two temp arrays.
    1. Left temp array holds the left half.
    2. Right temp array holds the right half.
  */
  // Find sizes of two subarrays to be merged.
  int sizeOne = mid - left + 1;
  int sizeTwo = right - mid;

  // Create temporary arrays.
  int[] leftArr = new int[sizeOne];
  int[] rightArr = new int[sizeTwo];

  // Copy data to temporary arrays.
  for (int i = 0; i < sizeOne; i++) {
    leftArr[i] = arr[left + i];
  }

  for (int j = 0; j < sizeTwo; j++) {
    rightArr[j] = arr[mid + 1 + j];
  }

  /*
    Start merging the temp arrays (like merging two sorted lists).
    1. Compare values of left vs right.
    2. Whichever is lowest gets added first to the real array's 'k'th position.
    This works because we created temp arrays so we can override the original array values.
  */
  // Initial indices of first and second subarrays.
  int i = 0;
  int j = 0;

  // Initial index of merged subarray array.
  int k = left;
  while (i < sizeOne && j < sizeTwo) {
    if (leftArr[i] <= rightArr[j]) {
      arr[k] = leftArr[i];
      i++;
    } else {
      arr[k] = rightArr[j];
      j++;
    }
    k++;
  }

  // Copy remaining elements of leftArr[] if any.
  while (i < sizeOne) {
    arr[k] = leftArr[i];
    i++;
    k++;
  }

  // Copy remaining elements of rightArr[] if any.
  while (j < sizeTwo) {
    arr[k] rightArr[j];
    j++;
    k++;
  }
}

// Main sort function that is called on arr[left...right].
public void sort(int[] arr, int left, int right) {
  // Check if left and right had not crossed.
  if (left < right) {
    // Get the middle index.
    int mid = left + (right - left) / 2;

    // Sort the first and second halves.
    sort(arr, left, mid);
    sort(arr, mid + 1, right);

    // Merge the sorted halves.
    merge(arr, left, mid, right);
  }
}
```

## :round_pushpin: Advantages
- Merge sort has good complexity.
- Stable sort.
- Easy to implement.
- Useful for external sorting.
- Can be easily parallelized.
- Requires few resources to sort.

## :round_pushpin: Disadvantages
- Slower compared to other sort algorithms (not best for small datasets).
- Requires an additional `O(N)` memory.
  - For the temporary array.
  - Store subarray that are used during the sorting process.
- It goes through the whole process even if array is sorted.
- Requires more code.
  - This is because we are dividing *and* merging.

## :round_pushpin: Analysis
**Time Complexity:** <code>O(N log N)</code>

**Space Complexity:** `O(N)`
