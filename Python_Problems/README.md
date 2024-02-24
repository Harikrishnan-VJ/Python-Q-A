# Increment Large Integer by One

Given a large integer represented as an integer array `digits`, where each `digits[i]` is the ith digit of the integer. The digits are ordered from most significant to least significant in left-to-right order. The large integer does not contain any leading 0's.

## Problem Description

You are tasked with incrementing the large integer by one and returning the resulting array of digits.

### Examples:

#### Example 1:
Input: `digits = [1,2,3]`  
Output: `[1,2,4]`  
Explanation: The array represents the integer 123. Incrementing by one gives 123 + 1 = 124. Thus, the result should be [1,2,4].

#### Example 2:
Input: `digits = [4,3,2,1]`  
Output: `[4,3,2,2]`  
Explanation: The array represents the integer 4321. Incrementing by one gives 4321 + 1 = 4322. Thus, the result should be [4,3,2,2].

#### Example 3:
Input: `digits = [9]`  
Output: `[1,0]`  
Explanation: The array represents the integer 9. Incrementing by one gives 9 + 1 = 10. Thus, the result should be [1,0].

## Approach

The intuition behind this approach is to iterate through the digits of the input integer from right to left. We start from the least significant digit and move towards the most significant digit. Whenever we encounter a digit less than 9, we can simply increment it by 1 and return the updated array. If we encounter a 9, we set the digit to 0 and continue the iteration. If we reach the end of the loop without returning, it means all digits were 9, so we prepend 1 to the array to handle the carry.

1. Iterate through the digits of the input integer from right to left.
2. If the current digit is less than 9, increment it by 1 and return the updated array.
3. If the current digit is 9, set it to 0 and continue to the next iteration.
4. If we reach the end of the loop without returning, prepend 1 to the array to handle the carry.

## Complexity Analysis

- **Time complexity:** O(n), where n is the number of digits in the input integer. The algorithm iterates through the digits array once.
- **Space complexity:** O(n). The space used is proportional to the size of the input array `digits`. In the worst case, when there is a carry from the least significant digit to the most significant digit, the algorithm creates a new array of size n+1 to hold the incremented number. Otherwise, it modifies the input array in place, so no additional space is used.

