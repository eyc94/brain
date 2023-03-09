# :heavy_check_mark: Bucket Sort
*Last Updated: 1/31/2023*

![Image of the bucket sort algorithm](../images/sorting/bucket-sort/bucket-sort.png)

## :round_pushpin: TLDR
`n` is the size of the input.
`k` is the number of buckets.

**Time Complexity:** `O(n + k)`

**Space Complexity:** `O(n + k)`

## :round_pushpin: Summary
- Buckets are created to put elements into them.
- Apply sorting algo (insertion sort) to sort elements in each bucket.
- Take out and join them to get sorted array.
- Useful when input is uniformly distributed over a range.
  - Sorting a large set of floating points in range 0.0 to 1.0 and are uniformly distributed.
- Simple way is comparison-based sorting.
- Can we sort in linear time?
  - Counting Sort cannot be applied as we use keys as index in counting sort.
  - The keys here are floats.
- Use Bucket Sort.

## :round_pushpin: Explanation
The algorithm:
1. Create `n` empty buckets (or lists).
  a. This is actually just 10 because there are only 10 digits.
2. Do the following for every array element `arr[i]`.
  a. Insert `arr[i]` into `bucket[n * arr[i]]`.
3. Sort buckets using insertion sort.
4. Concatenate all sorted buckets.

## :round_pushpin: Code
```java
import java.util.*;

/*
  Main function that uses bucket sort to sort an input array of size 'n'.
*/
public void bucketSort(float[] arr, int n) {
  if (n <= 0) {
    return;
  }

  // 1. Create empty buckets.
  Vector<Float>[] buckets = new Vector[n];
  for (int i = 0; i < n; i++) {
    buckets[i] = new Vector<Float>();
  }

  // 2. Put array elements in different buckets.
  for (int i = 0; i < n; i++) {
    float idx = arr[i] * n;
    buckets[(int) idx].add(arr[i]);
  }

  // 3. Sort individual buckets.
  for (int i = 0; i < n; i++) {
    Collections.sort(buckets[i]);
  }

  // 4. Concatenate all buckets into array.
  int index = 0;
  for (int i = 0; i < n; i++) {
    for (int j = 0; j < buckets[i].size(); j++) {
      arr[index++] = buckets[i].get(j);
    }
  }
}
```

## :round_pushpin: Analysis
`n` is the size of the input.
`k` is the number of buckets.

**Time Complexity:** `O(n + k)`

**Space Complexity:** `O(n + k)`
