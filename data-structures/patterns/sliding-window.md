# :heavy_check_mark: Sliding Window
*Last Updated: 1/26/2023*

![Image of a sliding window](../../images/patterns/sliding-window/sliding-window.png)

## :round_pushpin: Introduction
In problems with an array or linked list, we are often asked to find or calculate something among all the contiguous subarrays (or sublists) of a given size.

It is a computational technique which aims to reduce the use of nested loops and replace it with a single loop, reducing the time complexity.

## :round_pushpin: Requirements
The size of the sliding window *must* be fixed throughout the complete nested loop.

## :round_pushpin: Types
There are two types:
1. Static/Fixed Sliding Window
  a. Usually, the size of the window will be given.
  b. Expand the window until this size is met.
  c. Slide accordingly.
2. Dynamic Sliding Window
  a. Usually, the size of the window will ***not*** be given.
  b. Instead, another constraint will be given (e.g. finding the longest/shortest subarray with a given, required sum).
  c. Expand the window until this constraint is met.
  d. See if the window can be shrunken down or expanded more while ***adhering*** to this constraint.
  e. For example, expand the subarray until the sum is at least 7. Shrink the window from here to see what the shortest subarray is with a sum of at least 7.

## :round_pushpin: Example
Take a look at this problem:
```
Given an array, find the average of all contiguous subarrays of size 'K' in it.

Example:
Array: [1, 3, 2, 6, -1, 4, 1, 8, 2], K = 5
```

We are asked to find the average of all coniguous subarrays of size 5 in the given array.

To solve it:
1. For the first 5 numbers (index 0 - 4), the average is: (1 + 3 + 2 + 6 - 1) / 5 = 2.2.
2. The next 5 numbers (index 1 - 5), the average is: (3 + 2 + 6 - 1 + 4) / 5 = 2.8.
3. The next 5 numbers (index 2 - 6), the average is: (2 + 6 - 1 + 4 + 1) / 5 = 2.4.

The final output is:
```
Output: [2.2, 2.8, 2.4, 3.6, 2.8]
```

### Brute-Force Approach
A brute-force approach is to calculate the sum of every 5-element contiguous subarray of the given array and divide the sum by 5 to find the average:
```java
class AverageOfSubarrayOfSizeK {
  public static double[] findAverages(int K, int[] arr) {
    double[] result = new double[arr.length - K + 1];
    for (int i = 0; i <= arr.length - K; i++) {
      // Find sum of next 'K' elements.
      double sum = 0;
      for (int j = i; j < i + K; j++) {
        sum += arr[j];
      }
      result[i] = sum / K;
    }
    return result;
  }
}
```
**Time Complexity:** For every element, we are calculating the sum of its next 'K' elements. The time complexity will be `O(N * K)` where `N` is the number of elements in the input array.

### Efficient Approach
There is an inefficiency with the brute-force approach.

For any two consecutive subarrays of size 5, the overlapping part (contains 4 elements) will be evaluated twice.

![Image of overlapping portion of the method](../../images/patterns/sliding-window/sliding-window-overlapping.png)

There are four overlapping elements. Can we reuse the `sum` from the previous subarray?

![Image of the sliding window method](../../images/patterns/sliding-window/sliding-window-example.png)

Visualize each contiguous subarray as a sliding window of 5 elements. When we move to the next subarray:
- Slide window by one element.
- Reuse the sum from the previous window.
- Subtract the element leaving the window (left).
- Add the element entering the window (right).

This algorithm saves us from going through the subarray again to find the `sum`.

**Time Complexity:** `O(N)`.
```java
class AverageOfSubarrayOfSizeK {
  public static double[] findAverages(int K, int[] arr) {
    double[] result = new double[arr.length - K + 1];
    double windowSum = 0;
    int windowStart = 0;
    for (int windowEnd = 0; windowEnd < arr.length; windowEnd++) {
      windowSum += arr[windowEnd]; // Add the next element.
      // Slide the window. We don't need to slide if we have not hit the required window size of 'k'.
      if (windowEnd >= K - 1) {
        result[windowStart] = windowSum / K; // Calculate the average.
        windowSum -= arr[windowStart]; // Subtract the element going out.
        windowStart++; // Slide the window ahead.
      }
    }

    return result;
  }
}
```

***NOTE:*** In some cases, the sliding window is not of fixed size. We have to expand/shrink the window based on the problem constraints.

## :round_pushpin: Leetcode Problems
*List to be updated...*


## :round_pushpin: Sources
*List to be updated...*
