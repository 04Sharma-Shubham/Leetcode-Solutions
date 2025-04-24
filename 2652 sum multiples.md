# ➕ LeetCode Problem 2652: Sum Multiples

## 📘 Problem Statement

Given a positive integer `n`, return **the sum of all integers in the range `[1, n]`** inclusive that are divisible by **3**, **5**, or **7**.

### 🧠 Example

Input: n = 7 Output: 21 Explanation: Numbers in the range [1, 7] divisible by 3, 5, or 7 are 3, 5, 6, 7. Their sum is 21.


---

## ✅ Constraints

- `1 <= n <= 1000`

---

## 🧩 Approach

This is a straightforward problem that can be solved using a simple loop. Iterate from `1` to `n`, and for each number, check if it is divisible by 3, 5, or 7. If so, add it to a running sum.

This brute-force approach is efficient enough given the constraint `n ≤ 1000`.

---

## 💻 Java Solution

```java
class Solution {
    public int sumOfMultiples(int n) {
        int sum = 0;
        for (int i = 1; i <= n; i++) {
            if (i % 3 == 0 || i % 5 == 0 || i % 7 == 0) {
                sum += i;
            }
        }
        return sum;
    }
}
```
🏁 Output Examples
```
Input	Output
7	21
10	40
15	86
```
🧮 Complexity Analysis
Time Complexity: O(n) – we check each number up to n.

Space Complexity: O(1) – constant space used for the sum variable.

📂 Related Topics
Brute Force

Arithmetic

🏷️ Tags
#LeetCode #Java #Loops #Easy #2652

🌟 If you liked this solution, give the repo a star and share it with others!



Let me know if you want a batch of these for a whole LeetCode series in your repo!







