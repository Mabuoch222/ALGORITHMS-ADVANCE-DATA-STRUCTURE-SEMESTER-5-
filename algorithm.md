# Algorithm Implementation: Find Maximum Number

This repository contains C++ implementations of an algorithm to find the maximum number in a list (array). The algorithm demonstrates fundamental programming concepts including loops, conditionals, function usage, and working with different data structures.

## Overview

The algorithm follows these steps:
1.  **Input:** Accepts a list of numbers.
2.  **Process:** Iterates through the list, comparing each element to the current maximum.
3.  **Output:** Returns the largest number found.
4.  **Properties:** Exhibits `O(n)` time complexity and `O(1)` space complexity.

## Code Implementations

### 1. Basic Function with C-Style Array

This implementation uses a standard C-style array and requires the size to be passed as a parameter.

```cpp
#include <iostream>

/**
 * Finds the maximum integer in a C-style array.
 * @param arr The array of integers.
 * @param n The size of the array.
 * @return The maximum value in the array. Returns -1 if the array is empty.
 */
int findMax(int arr[], int n) {
    // Check for empty array
    if (n <= 0) {
        std::cerr << "Error: Array is empty." << std::endl;
        return -1;
    }
    
    int max_num = arr[0]; // Initialize max to the first element
    
    // Iterate through the remaining elements
    for (int i = 1; i < n; ++i) {
        if (arr[i] > max_num) {
            max_num = arr[i]; // Update max if current element is larger
        }
    }
    return max_num;
}

// Example usage in main()
int main() {
    int numbers[] = {45, 12, 67, 23, 89, 34, 11, 90, 56};
    int size = sizeof(numbers) / sizeof(numbers[0]); // Calculate array size
    
    int result = findMax(numbers, size);
    std::cout << "The largest number is: " << result << std::endl; // Output: 90
    
    return 0;
}
