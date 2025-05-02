# 🔁 LeetCode 283 — Move Zeroes

## 💡 Problem Description

Given an integer array `nums`, move all `0`'s to the end of it while maintaining the **relative order** of the non-zero elements.

📌 Note: You must do this **in-place** without making a copy of the array.

---

### 🔗 Problem Link

[LeetCode 283 - Move Zeroes](https://leetcode.com/problems/move-zeroes/)

---

## ✅ Approach

We use two pointers:

- `i` iterates through the array.
- `index` keeps track of where the next non-zero number should go.

After placing all non-zero numbers at the start, fill the rest of the array with zeroes.

---

## 💻 Java Code

```java
class Solution {
    public void moveZeroes(int[] nums) {
        int n = nums.length;
        int index = 0;

        // Move all non-zero elements to the front
        for (int i = 0; i < n; i++) {
            if (nums[i] != 0) {
                nums[index++] = nums[i];
            }
        }

        // Fill the rest of the array with zeros
        for (int i = index; i < n; i++) {
            nums[i] = 0;
        }
    }
}
```

---

## 📊 Examples

### Example 1:

**Input:**  
`nums = [0,1,0,3,12]`  
**Output:**  
`[1,3,12,0,0]`

### Example 2:

**Input:**  
`nums = [0]`  
**Output:**  
`[0]`

---

## ⏱️ Time and Space Complexity

**Time Complexity:** O(n)  
- We traverse the array twice (once to move non-zeroes, once to fill zeroes).

**Space Complexity:** O(1)  
- No extra space used beyond variables.

---

## 🏷️ Tags

Array, Two Pointers, In-Place Operation

---

📌 This is a great example of solving array manipulation **in-place** using a two-pointer strategy.
