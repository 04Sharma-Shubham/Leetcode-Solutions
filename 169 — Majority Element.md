# 🔢 LeetCode 169 — Majority Element

## 💡 Problem Description

Given an array `nums` of size `n`, return the **majority element**.

The majority element is the element that appears **more than** `⌊n / 2⌋` times.  
You may assume that the majority element **always exists** in the array.

---

### 🔗 Problem Link

[LeetCode 169 - Majority Element](https://leetcode.com/problems/majority-element/)

---

## ✅ Approach

We sort the array using `Arrays.sort()` and return the element at index `n / 2`.

- Since the majority element appears more than `n / 2` times, it must occupy the middle position in a sorted array.

---

## 💻 Java Code

```java
class Solution {
    public int majorityElement(int[] nums) {
        Arrays.sort(nums);
        return nums[nums.length / 2];
    }
}
```

---

## 📊 Examples

### Example 1:

**Input:** `nums = [3,2,3]`  
**Output:** `3`

---

### Example 2:

**Input:** `nums = [2,2,1,1,1,2,2]`  
**Output:** `2`

---

## ⏱️ Time and Space Complexity

**Time Complexity:** O(n log n) – due to sorting  
**Space Complexity:** O(1) – ignoring sorting space

---

## 🏷️ Tags

Array, Sorting, Counting
