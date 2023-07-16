# Leftmost-Middle-Index-in-Array-leet3-


_**Problem Description**_
Given a 0-indexed integer array nums, you need to find the leftmost middle index (i.e., the smallest index amongst all the possible ones).

A middle index is defined as an index i where the sum of elements on the left side of i is equal to the sum of elements on the right side of i. The left side of index i includes nums[0] through nums[i-1], and the right side includes nums[i+1] through nums[nums.length-1].

If i == 0, the left side sum is considered to be 0. Similarly, if i == nums.length - 1, the right side sum is considered to be 0.

Your task is to return the leftmost middle index that satisfies the condition, or -1 if there is no such index.

_Example: _
Input: nums = [2, 3, -1, 8, 4]  
Output: 3


_**Explanation:**_

In this example, the middle index 3 is the leftmost index that satisfies the condition. The sum of elements on the left side is 2 + 3 + -1 = 4, and the sum of elements on the right side is 4.


_**Solution Approach**_
To solve this problem, we can iterate through the array and calculate the total sum of all elements. Then, we traverse the array again and keep track of the left sum as we move from left to right. At each index, we can calculate the right sum by subtracting the left sum and the current element from the total sum. If the left sum equals the right sum, we have found a middle index, and we return it.

_The algorithm follows these steps:_

Calculate the total sum of all elements in the array.
Initialize the left sum as 0.
Iterate through the array from left to right:
Calculate the right sum by subtracting the left sum and the current element from the total sum.
If the left sum equals the right sum, return the current index as the leftmost middle index.
Update the left sum by adding the current element to it.
If no middle index is found, return -1.


**Complexity Analysis**
The time complexity for this solution is O(N), where N is the length of the input array nums. We iterate through the array twice, once to calculate the total sum and once to find the middle index.

The space complexity is O(1) as we only use a constant amount of additional space to store variables.


**Summary**
The "Finding the Leftmost Middle Index in an Array" problem involves finding the leftmost index in an array where the sum of elements on the left side is equal to the sum of elements on the right side. By traversing the array and calculating the left and right sums, we can determine the leftmost middle index. The solution has a time complexity of O(N) and a space complexity of O(1).
