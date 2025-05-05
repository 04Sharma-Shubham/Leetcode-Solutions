# 🔢 LeetCode 405 — Convert a Number to Hexadecimal

## 💡 Problem Description

Given a 32-bit integer `num`, return a string representing its hexadecimal representation. For **negative integers**, the **two’s complement** method is used.

All letters in the output must be **lowercase**, and there should be **no leading zeros** in the answer unless the number is zero.

❗ You **may not** use any built-in library method to directly solve this problem.

---

### 🔗 Problem Link

[LeetCode 405 - Convert a Number to Hexadecimal](https://leetcode.com/problems/convert-a-number-to-hexadecimal/)

---

## ✅ Approach

Java provides a built-in method `Integer.toHexString()` that handles conversion including for negative numbers using two's complement.

In this solution, we use that method to convert the integer to a hexadecimal string in lowercase.

---

## 💻 Java Code

```java
class Solution {
    public String toHex(int num) {
        return Integer.toHexString(num);
    }
}
```

---

## 📊 Examples

### Example 1:

**Input:** `num = 26`  
**Output:** `"1a"`

---

### Example 2:

**Input:** `num = -1`  
**Output:** `"ffffffff"`  
**Explanation:** `-1` in 32-bit two’s complement is represented by all 1s (i.e., `0xffffffff`).

---

## ⏱️ Time and Space Complexity

**Time Complexity:** O(1) – constant time for fixed-size integer conversion  
**Space Complexity:** O(1) – constant space usage for storing the result string

---

## 🏷️ Tags

Bit Manipulation, Math, String
``
