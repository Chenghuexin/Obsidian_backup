---
Leetcode: https://leetcode.com/problems/sort-colors/description/
tags:
  - Sorting
  - TwoPoints
---
# Problem explaination
sort the objects so that objects of the same frequency or color are adjacent

>[!NOTE] Notice
>Sorting by using multiple pointers

# Solution
```java
class Solution {

    public void sortColors(int[] nums) {

        int zero = -1, one = 0, two = nums.length;

        while (one < two) {

            if (nums[one] == 0) {

                // zero must be smaller than or equal one, switch position zero and

                // one means change position 1 and 0

                swap(nums, ++zero, one++);

            } else if (nums[one] == 2) {

                // because 2 must put in the right side of the array

                swap(nums, --two, one);

            } else {

                ++one;

            }

        }

    }

  

    private void swap(int[] nums, int i, int j) {

    int t = nums[i];

    nums[i] = nums[j];

    nums[j] = t;

	}

}

```