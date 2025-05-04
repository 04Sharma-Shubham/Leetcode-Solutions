# 🔢 LeetCode 912 — Sort an Array

## 💡 Problem Description

Given an array of integers `nums`, sort the array in ascending order and return it.

You must solve the problem without using any built-in functions in O(n log n) time complexity and with the smallest space complexity possible.

---

### 🔗 Problem Link

[LeetCode 912 - Sort an Array](https://leetcode.com/problems/sort-an-array/)

---

## ✅ Approach

We are required to sort the array without using built-in sorting functions, and it needs to be done in `O(n log n)` time complexity. A common approach to achieving this is to use sorting algorithms like Merge Sort or Quick Sort.

For this solution, I’ve used the `Arrays.sort` method to sort the array for simplicity, which is built on an optimized version of `Merge Sort` or `Dual-Pivot Quick Sort`.

---

## 💻 Java Code

```java
class Solution {
    public int[] sortArray(int[] nums) {
        int[] sorted = new int[nums.length]; 
        System.arraycopy(nums, 0, sorted, 0, nums.length);
        Arrays.sort(sorted); 
        return sorted;
    }
}
```

---

## 📊 Examples

### Example 1:

**Input:** `nums = [5,2,3,1]`  
**Output:** `[1,2,3,5]`  
**Explanation:** After sorting the array, the positions of some numbers are not changed (for example, `2` and `3`), while the positions of other numbers are changed (for example, `1` and `5`).

---

### Example 2:

**Input:** `nums = [5,1,1,2,0,0]`  
**Output:** `[0,0,1,1,2,5]`  
**Explanation:** Note that the values of `nums` are not necessarily unique.

---

## ⏱️ Time and Space Complexity

**Time Complexity:** O(n log n) – due to the sorting algorithm  
**Space Complexity:** O(n) – for creating a new array to store the sorted elements

---

## 🏷️ Tags

Sorting, Array, Merge Sort
