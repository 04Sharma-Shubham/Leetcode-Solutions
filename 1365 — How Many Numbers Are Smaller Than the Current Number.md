
# 🔢 LeetCode 1365 — How Many Numbers Are Smaller Than the Current Number

## 💡 Problem Description

Given the array `nums`, for each `nums[i]`, find out how many numbers in the array are **smaller** than it.  
That is, for each `nums[i]` you have to count the number of valid `j`'s such that `j != i` and `nums[j] < nums[i]`.

Return the answer in a **new array**.

---

### 🔗 Problem Link
[LeetCode 1365 - How Many Numbers Are Smaller Than the Current Number](https://leetcode.com/problems/how-many-numbers-are-smaller-than-the-current-number/)

---

## ✅ Approach

This is a brute-force approach:
- For each element in the array, compare it with every other element.
- Count how many numbers are smaller than it.
- Store the count in a result array.

---

## 💻 Java Code
```
class Solution {
    public int[] smallerNumbersThanCurrent(int[] nums) {
        int n = nums.length;
        int[] res = new int[n];

        for (int i = 0; i < n; i++) {
            int count = 0;
            for (int j = 0; j < n; j++) {
                if (i != j && nums[j] < nums[i]) {
                    count++;
                }
            }
            res[i] = count;
        }

        return res;
    }
}
```
---

## 📊 Examples
```
Example 1:  
Input: nums = [8,1,2,2,3]  
Output: [4,0,1,1,3]  
Explanation:  
- 8 has 4 numbers smaller than it: [1,2,2,3]  
- 1 has 0 numbers smaller than it  
- 2 has 1 number smaller than it: [1] (and the second 2 is ignored due to `j != i`)  
- 3 has 3 numbers smaller than it: [1,2,2]
```
```
Example 2:  
Input: nums = [6,5,4,8]  
Output: [2,1,0,3]
```
---

## ⏱️ Time and Space Complexity
```
**Time Complexity:** O(n²)  
- We loop through the array twice for each element.

**Space Complexity:** O(n)  
- Result array stores `n` elements.
```
---

## 🏷️ Tags
```
Array, Brute Force, Counting
```
---
```
📌 Tip: A more optimized approach uses a counting array with prefix sums (O(n) + O(max value)), but brute-force is simple and acceptable for small arrays.
```
