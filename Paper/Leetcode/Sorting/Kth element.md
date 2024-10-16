# Problem explaination
Find the Kth largest element in  a array

> [!NOTE] Notice
> It's conting from 0th largest element

# Solution
## Quick Select

>[!NOTE]program explaination
>1. initialize a piviot to index 0
>2. from index of piviot + 1, find the element which is larger than piviot, named as temp_start
>3. from end of array, find the element which is smaller than piviot, named as temp_end
>4. 
```Java
class Solution {

    public int findKthLargest(int[] nums, int k) {

        k = nums.length - k;

		// initialization, start => piviot
        int start = 0, end = nums.length - 1;

        while(start < end){

            int piviot = partition(nums, start, end);

  

            if(piviot == k){

                break;

            }else if(piviot < k){

                start = piviot + 1;

            }else{

                end = piviot - 1;

            }

        }

        return nums[k];

    }

  

    private int partition(int[] nums, int start, int end){

        int temp_start = start, temp_end = end + 1;

  

        // increasing order

        while(true){
			// find the element which is larger than piviot
            while(nums[++temp_start] < nums[start] && temp_start < end);
			// find the element which is smaller than piviot
            while(nums[--temp_end] > nums[start] && temp_end > start);

  
			// it means 
            if(temp_start >= temp_end){

                break;

            }

  

            swap(nums, temp_start, temp_end);

        }

        swap(nums, start, temp_end);

        return temp_end;

    }

  

    private void swap(int[] nums, int i, int j){

        int temp = nums[i];

        nums[i] = nums[j];

        nums[j] = temp;

    }

  

}
```
