# 🧗 LeetCode 70 — Climbing Stairs

## 💡 Problem Description

You are climbing a staircase. It takes `n` steps to reach the top.

Each time you can either climb **1** or **2** steps. In how many distinct ways can you climb to the top?

---

### 🔗 Problem Link

[LeetCode 70 - Climbing Stairs](https://leetcode.com/problems/climbing-stairs/)

---

## ✅ Approach

This is a classic **dynamic programming / Fibonacci** problem.

- Base cases:  
  - `n = 1` → 1 way  
  - `n = 2` → 2 ways  
- For each additional step, the number of ways to reach it is the sum of the ways to reach the previous two steps.

We use two variables (`first` and `second`) to keep track of the previous two results, optimizing space usage.

---

## 💻 Java Code

```java
class Solution {
    public int climbStairs(int n) {
        if (n <= 1) {
            return 1;
        }

        int first = 1, second = 1;
        for (int i = 2; i <= n; i++) {
            int temp = second;
            second = first + second;
            first = temp;
        }

        return second;
    }
}
```

---

## 📊 Examples

### Example 1:

**Input:** `n = 2`  
**Output:** `2`  
**Explanation:**  
1. 1 step + 1 step  
2. 2 steps

---

### Example 2:

**Input:** `n = 3`  
**Output:** `3`  
**Explanation:**  
1. 1 step + 1 step + 1 step  
2. 1 step + 2 steps  
3. 2 steps + 1 step

---

## ⏱️ Time and Space Complexity

**Time Complexity:** O(n)  
**Space Complexity:** O(1)

---

## 🏷️ Tags

Dynamic Programming, Recursion, Fibonacci
