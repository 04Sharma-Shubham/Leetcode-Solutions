# 🔢 LeetCode 217 — Contains Duplicate

## 💡 Problem Description

Given an integer array `nums`, return `true` if any value appears at least twice in the array, and return `false` if every element is distinct.

---

### 🔗 Problem Link

[LeetCode 217 - Contains Duplicate](https://leetcode.com/problems/contains-duplicate/)

---

## ✅ Approach

The idea is to sort the array and check if any two consecutive elements are the same.

- If the array is sorted, duplicates will appear next to each other, making it easier to check for any repeated values.

---

## 💻 Java Code

```java
class Solution {
    public boolean containsDuplicate(int[] nums) {
        Arrays.sort(nums);
        for (int i = 1; i < nums.length; i++) {
            if (nums[i] == nums[i - 1]) {
                return true;
            }
        }
        return false;
    }
}
```

---

## 📊 Examples

### Example 1:

**Input:** `nums = [1,2,3,1]`  
**Output:** `true`  
**Explanation:** The element `1` occurs at the indices `0` and `3`.

---

### Example 2:

**Input:** `nums = [1,2,3,4]`  
**Output:** `false`  
**Explanation:** All elements are distinct.

---

### Example 3:

**Input:** `nums = [1,1,1,3,3,4,3,2,4,2]`  
**Output:** `true`  
**Explanation:** There are several duplicates in the array.

---

## ⏱️ Time and Space Complexity

**Time Complexity:** O(n log n) – due to sorting the array  
**Space Complexity:** O(1) – ignoring the sorting space

---

## 🏷️ Tags

Array, Sorting
