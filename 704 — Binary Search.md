# 🧮 LeetCode 704 — Binary Search

## 💡 Problem Description

Given an array of integers `nums` which is sorted in ascending order, and an integer `target`, write a function to search for `target` in `nums`.

If `target` exists, return its index. Otherwise, return -1.

You must implement an algorithm with **O(log n)** runtime complexity.

---

### 🔗 Problem Link

[LeetCode 704 - Binary Search](https://leetcode.com/problems/binary-search/)

---

## ✅ Approach

- This problem is a classic **binary search**.
- The function uses recursion to perform binary search on the sorted array.
- It compares the target with the middle element and adjusts the search range accordingly.

---

## 💻 Java Code

```java
class Solution {
    public int search(int[] nums, int target) {
        int start = 0;
        int end = nums.length - 1;

        if (nums == null || nums.length == 0) {
            return -1;
        }

        return bs(nums, start, end, target);
    }

    public static int bs(int[] nums, int start, int end, int target) {
        if (start > end) {
            return -1;
        }

        int mid = start + (end - start) / 2;

        if (nums[mid] == target) {
            return mid;
        } else if (nums[mid] > target) {
            return bs(nums, start, mid - 1, target);
        } else {
            return bs(nums, mid + 1, end, target);
        }
    }
}
```

---

## 📊 Examples

### Example 1:

**Input:**  
`nums = [-1,0,3,5,9,12], target = 9`  
**Output:**  
`4`  
**Explanation:** 9 is at index 4.

---

### Example 2:

**Input:**  
`nums = [-1,0,3,5,9,12], target = 2`  
**Output:**  
`-1`  
**Explanation:** 2 is not in the array.

---

## ⏱️ Time and Space Complexity

**Time Complexity:** O(log n)  
**Space Complexity:** O(log n) due to recursive stack (can be O(1) with iterative version)

---

## 🏷️ Tags

Binary Search, Divide and Conquer, Recursion
