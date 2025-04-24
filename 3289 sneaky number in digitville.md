# 🕵️‍♂️ LeetCode Problem 389: Sneaky Numbers in Digitville

## 📘 Problem Statement

In the quirky town of **Digitville**, numbers love to show up in mysterious ways. You're given an array of integers where numbers from `0` to `99` may appear. Your task is to identify the **first two numbers** that sneak into the list **twice**.

### 🧠 Example

Input: [1, 3, 2, 3, 5, 1, 7, 8] Output: [3, 1] Explanation:

The number 3 appears twice (first duplicate).

The number 1 appears twice (second duplicate).


---

## ✅ Constraints

- The integers are in the range `0` to `99`.
- The array contains **at least two duplicated numbers**.
- You must return exactly **two integers** — the first two to appear twice.

---

## 🧩 Approach

We use a frequency counter array of size `100` (matching the valid range of inputs) to track how many times each number has been seen.

As soon as a number’s count reaches **2**, it’s added to the result array. The loop continues until the first **two** such numbers are found.

---

## 💻 Java Solution

```java
class Solution {
    public int[] getSneakyNumbers(int[] nums) {
        int[] ans = new int[2];
        int[] cnt = new int[100];
        int k = 0;
        for (int x : nums) {
            if (++cnt[x] == 2) {
                ans[k++] = x;
            }
        }
        return ans;
    }
}
```
🏁 Output Examples
```
Input	Output
[4, 6, 1, 6, 2, 4]	[6, 4]
[9, 8, 9, 3, 8, 7, 2, 1]	[9, 8]
[10, 20, 30, 20, 10, 40, 50]	[20, 10]
```
🧮 Complexity Analysis
Time Complexity: O(n) — We iterate once over the array.

Space Complexity: O(1) — Fixed-size count array of 100 elements.

📂 Related Topics
Hashing

Arrays

Frequency Counting

🏷️ Tags
#LeetCodeStyle #Java #HashMap #Duplicates #389

🎯 Keep an eye out — some numbers are sneakier than others!

⭐ Star this repo if you found the solution useful or interesting!

```
Let me know if you'd like to turn this into a template you can reuse for all your custom LeetCode-style problems!

```


