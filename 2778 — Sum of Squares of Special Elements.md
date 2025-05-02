# 🧮 LeetCode 2778 — Sum of Squares of Special Elements

## 💡 Problem Description

You are given a **1-indexed** integer array `nums` of length `n`.

An element `nums[i]` of `nums` is called **special** if `i` divides `n`, i.e. `n % i == 0`.

Return the **sum of the squares** of all special elements of `nums`.

---

### 🔗 Problem Link

[LeetCode 2778 - Sum of Squares of Special Elements](https://leetcode.com/problems/sum-of-squares-of-special-elements/)

---

## ✅ Approach

- Since the array is **1-indexed**, we simulate that by iterating through the 0-indexed array.
- For each index `i`, check if `n % (i + 1) == 0`.
- If it is, it's a "special" index, so we add `nums[i] * nums[i]` to the result.

---

## 💻 Java Code

```java
class Solution {
    public int sumOfSquares(int[] nums) {
        int n = nums.length;
        int sum = 0;
        for (int i = 0; i < n; i++) {
            if (n % (i + 1) == 0) {
                sum += nums[i] * nums[i];
            }
        }
        return sum;
    }
}
```

---

## 📊 Examples

### Example 1:

**Input:**  
`nums = [1,2,3,4]`  
**Output:**  
`21`  

**Explanation:**  
Special indices are 1, 2, and 4 (1-based).  
Sum of squares: `1² + 2² + 4² = 1 + 4 + 16 = 21`.

---

### Example 2:

**Input:**  
`nums = [2,7,1,19,18,3]`  
**Output:**  
`63`  
