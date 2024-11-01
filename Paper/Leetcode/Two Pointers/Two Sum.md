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
>If the sum of these positions is smaller than the target, the first pointer should shift right. 

# Solution
```java
class Solution {

    public int[] twoSum(int[] numbers, int target) {

        int[] result = new int[2];

        int index1 = 0, index2 = numbers.length - 1;

        while(index1 < index2){

            if(numbers[index1] + numbers[index2] == target){

                break;

            }else if(numbers[index1] + numbers[index2] < target){

                index1++;

            }else{

                index2--;

            }

        }

        result[0] = index1 + 1;

        result[1] = index2 + 1;

        return result;

    }

}
```