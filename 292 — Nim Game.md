# 🎮 LeetCode 292 — Nim Game

## 💡 Problem Description

You are playing the following Nim Game with your friend:

- There is a heap of stones on the table.
- You and your friend take turns, and **you go first**.
- On each turn, a player removes **1 to 3 stones**.
- The player who removes the **last stone wins**.

Given `n`, the number of stones in the heap, return `true` if you can win the game assuming both you and your friend play optimally, otherwise return `false`.

---

### 🔗 Problem Link

[LeetCode 292 - Nim Game](https://leetcode.com/problems/nim-game/)

---

## ✅ Approach

The **key observation** is:
- If `n % 4 == 0`, you will always lose **if your opponent plays optimally**.
- Otherwise, you can win by making sure your opponent always faces a multiple of 4.

### Why?
If the number of stones is a multiple of 4, whatever number of stones you remove (1, 2, or 3), the opponent can always return the count to another multiple of 4 — eventually making you take the last stone.

---

## 💻 Java Code

```java
class Solution {
    public boolean canWinNim(int n) {
        return n % 4 != 0;
    }
}
```

---

## 📊 Examples

### Example 1:

**Input:**  
`n = 4`  
**Output:**  
`false`  
**Explanation:**  
No matter what you do, your friend will win.

---

### Example 2:

**Input:**  
`n = 1`  
**Output:**  
`true`

---

### Example 3:

**Input:**  
`n = 2`  
**Output:**  
`true`

---

## ⏱️ Time and Space Complexity

**Time Complexity:** O(1)  
**Space Complexity:** O(1)  

Just a simple modulo check.

---

## 🏷️ Tags

Math, Game Theory

---

📌 This problem is a classic case of mathematical pattern recognition in game theory — often asked in interviews for its simplicity and depth.
