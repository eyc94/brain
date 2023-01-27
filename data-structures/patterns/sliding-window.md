# :heavy_check_mark: Two Pointers
*Last Updated: 1/26/2023*

## :round_pushpin: Introduction
In problems with an array or linked list, we are often asked to find or calculate something among all the contiguous subarrays (or sublists) of a given size.

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

Visualize each contiguous subarray as a sliding window