# Single Number

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

Given a  **non-empty**  array of integers `nums`, every element appears  *twice*  except for one. Find that single one.

You must implement a solution with a linear runtime complexity and use only constant extra space.

 

 **Example 1:** 

 **Input:**  nums = [2,2,1]

 **Output:**  1

 **Example 2:** 

 **Input:**  nums = [4,1,2,1,2]

 **Output:**  4

 **Example 3:** 

 **Input:**  nums = [1]

 **Output:**  1

 

 **Constraints:** 

- 1 <= nums.length <= 3 * 104
- -3  *104 <= nums[i] <= 3*  104
- Each element in the array appears twice except for one element which appears only once.

## Solution

**Language:** Java  
**Runtime:** 13 ms (beats 18.97%)  
**Memory:** 46.3 MB (beats 99.22%)  
**Submitted:** 2026-10-16T17:13:52.934Z  

```java
import java.util.HashMap;
    class Solution {
    public int singleNumber(int[] nums) {

        HashMap<Integer,Integer> map = new HashMap<>();

        for(int i=0;i<nums.length;i++){
            map.put(nums[i],map.getOrDefault(nums[i],0)+1);
        }

        for(int i=0;i<nums.length;i++){
            if(map.get(nums[i])==1){
                return nums[i];
            }
        }

        return 0;
        
    }
}
```

---

[View on LeetCode](https://leetcode.com/problems/single-number/)