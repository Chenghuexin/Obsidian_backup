---
Leetcode: https://leetcode.com/problems/reverse-vowels-of-a-string/description/
tags:
  - TwoPoints
---
# Problem explaination
Given a string `s`, reverse only all the vowels in the string and return it.

>[!NOTE] Notice
>Don't swap; create a new array to put the result.

# Solution
```java
class Solution {

    public String reverseVowels(String s) {

        String vowels = "AEIOUaeiou";

        int head = 0, tail = s.length() - 1;

        char[] result = new char[s.length()];

        while(head <= tail){

            char c_head = s.charAt(head);

            char c_tail = s.charAt(tail);

            int pos_head = vowels.indexOf(c_head);

            int pos_tail = vowels.indexOf(c_tail);

  

            if(pos_head != -1 && pos_tail != -1){

                result[tail--] = c_head;

                result[head++] = c_tail;

            }

  

            if(pos_head == -1){

                result[head++] = c_head;

            }

  

            if(pos_tail == -1){

                result[tail--] = c_tail;

            }

        }

        return new String(result);

  

    }

}
```