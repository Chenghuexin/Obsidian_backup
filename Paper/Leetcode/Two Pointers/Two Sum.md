---
Leetcode: https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/description/
tags:
  - TwoPoints
---
# Problem explaination
Given a **1-indexed** array of integers `numbers` that is already **_sorted in non-decreasing order_**, find two numbers such that they add up to a specific `target` number.

>[!NOTE] Notice
>Using two pointers, initially, one pointer is at index 0, and another is at the end of the array.
>If the sum of these positions is bigger than the target, the second pointer should shift left.
>