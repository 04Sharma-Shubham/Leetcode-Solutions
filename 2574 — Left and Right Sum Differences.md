
# 🔄 LeetCode 2574 — Left and Right Sum Differences

## 💡 Problem Description

You are given a **0-indexed** integer array `nums` of size `n`.

Define two arrays `leftSum` and `rightSum` where:

- `leftSum[i]` is the sum of elements to the **left** of the index `i` in the array `nums`.  
  If there is no such element, `leftSum[i] = 0`.
- `rightSum[i]` is the sum of elements to the **right** of the index `i` in the array `nums`.  
  If there is no such element, `rightSum[i] = 0`.

Return an integer array `answer` of size `n` where:  
`answer[i] = |leftSum[i] - rightSum[i]|`

---

### 🔗 Problem Link

[LeetCode 2574 - Left and Right Sum Differences](https://leetcode.com/problems/left-and-right-sum-differences/)

---

## ✅ Approach

1. Initialize two arrays: `leftSum` and `rightSum` of the same length as `nums`.
2. Compute prefix sum in `leftSum`:
   - `leftSum[i] = leftSum[i-1] + nums[i-1]`
3. Compute suffix sum in `rightSum`:
   - `rightSum[i] = rightSum[i+1] + nums[i+1]`
4. For each index `i`, calculate `answer[i] = |leftSum[i] - rightSum[i]|`

---

## 💻 Java Code

```java
class Solution {
    public int[] leftRightDifference(int[] nums) {
        int n = nums.length;
        int[] leftSum = new int[n];
        int[] rightSum = new int[n];
        int[] answer = new int[n];

        // Compute leftSum
        for (int i = 1; i < n; i++) {
            leftSum[i] = leftSum[i - 1] + nums[i - 1];
        }

        // Compute rightSum
        for (int i = n - 2; i >= 0; i--) {
            rightSum[i] = rightSum[i + 1] + nums[i + 1];
        }

        // Compute absolute differences
        for (int i = 0; i < n; i++) {
            answer[i] = Math.abs(leftSum[i] - rightSum[i]);
        }

        return answer;
    }
}
```

---

## 📊 Examples
```
### Example 1:

**Input:**  
`nums = [10,4,8,3]`  

**Explanation:**  
- `leftSum = [0,10,14,22]`  
- `rightSum = [15,11,3,0]`  
- `answer = [15,1,11,22]`  

**Output:** `[15,1,11,22]`
```
---
```
### Example 2:

**Input:**  
`nums = [1]`  

**Explanation:**  
- `leftSum = [0]`  
- `rightSum = [0]`  
- `answer = [0]`  

**Output:** `[0]`
```
---

## ⏱️ Time and Space Complexity
```
**Time Complexity:** O(n)  
- We pass over the array 3 times: once for `leftSum`, once for `rightSum`, and once for `answer`.

**Space Complexity:** O(n)  
- We use three arrays of size `n` for `leftSum`, `rightSum`, and `answer`.
```
---

## 🏷️ Tags

Array, Prefix Sum, Math

---

📌 Tip: This pattern of prefix and suffix sums is useful in many range sum problems!
```
