# 🔢 LeetCode 268 — Missing Number

## 💡 Problem Description

You are given an array `nums` containing `n` **distinct** numbers in the range `[0, n]`.  
Return the only number in the range that is **missing** from the array.

---

### 🔗 Problem Link

[LeetCode 268 - Missing Number](https://leetcode.com/problems/missing-number/)

---

## ✅ Approach

The sum of the first `n` natural numbers is:  
📌 `total = n * (n + 1) / 2`

If we subtract the sum of the actual array elements from this total, we get the missing number.

---

## 💻 Java Code

```java
class Solution {
    public int missingNumber(int[] nums) {
        int n = nums.length;
        int total = n * (n + 1) / 2;
        int sum = 0;
        
        for (int num : nums) {
            sum += num;
        }
        
        return total - sum;
    }
}
```

---

## 📊 Examples

### Example 1:

**Input:**  
`nums = [3, 0, 1]`

**Output:**  
`2`

**Explanation:**  
The expected sum is `3 * (3 + 1) / 2 = 6`, and the sum of array elements is `3 + 0 + 1 = 4`, so the missing number is `6 - 4 = 2`.

---

### Example 2:

**Input:**  
`nums = [0, 1]`

**Output:**  
`2`

---

### Example 3:

**Input:**  
`nums = [9,6,4,2,3,5,7,0,1]`

**Output:**  
`8`

---

## ⏱️ Time and Space Complexity

**Time Complexity:** O(n)  
- Single pass through the array to compute the sum.

**Space Complexity:** O(1)  
- Constant extra space used.

---

## 🏷️ Tags

Array, Math, Bit Manipulation

---

📌 This is a classic application of the **Gauss Formula** for the sum of the first `n` natural numbers.
