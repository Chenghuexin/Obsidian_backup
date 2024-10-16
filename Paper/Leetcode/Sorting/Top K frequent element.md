---
Leetcode: https://leetcode.com/problems/top-k-frequent-elements/description/
tags:
  - Sorting
  - DivideAndConquer
---
# Problem explaination
find the k most frequent elements

>[!NOTE]Notice
>using array to store the elements of different frequence. 
>e.g. array[3] sotre the elements whose frequency are 3
>Don't use sorting!!
# Solution
```Java
class Solution {

    public int[] topKFrequent(int[] nums, int k) {

        // record the frquency of each element

        HashMap<Integer, Integer> Freq = new HashMap<>();

        for (int i : nums) {

            Freq.put(i, Freq.getOrDefault(i, 0) + 1);

        }

  

        // one bucket store the element(key) having the same frequency(index)

        List<Integer>[] buckets = new ArrayList[nums.length + 1];

        for (int key : Freq.keySet()) {

            int f = Freq.get(key);

            if(buckets[f] == null){

                buckets[f] = new ArrayList<>();

            }

            buckets[f].add(key);

        }

  

        // find top K

        List<Integer> topK = new ArrayList<>();

        for (int i = buckets.length - 1; i >= 0 && topK.size() < k ; i--) {

            if(buckets[i] == null){

                continue;

            }

  

            if(buckets[i].size() <= (k - topK.size())) {

                topK.addAll(buckets[i]);

            } else {

                topK.addAll(buckets[i].subList(0, k - topK.size()));

            }

        }

  

        int[] result = new int[k];

        for (int i = 0; i < k; i++){

            result[i] = topK.get(i);

        }

        return result;

    }

}

```