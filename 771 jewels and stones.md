# 💎 LeetCode Problem 771: Jewels and Stones

## 📘 Problem Statement

You're given strings `jewels` representing the types of stones that are jewels, and `stones` representing the stones you have. Each character in `stones` is a type of stone you have. You want to know how many of the stones you have are also jewels.

Letters are case sensitive, so `"a"` is considered a different type of stone from `"A"`.

### 🧠 Example

Input: jewels = "aA", stones = "aAAbbbb" Output: 3

Copy
Edit
Input: jewels = "z", stones = "ZZ" Output: 0

yaml
Copy
Edit

---

## ✅ Constraints

- `1 <= jewels.length, stones.length <= 50`
- `jewels` and `stones` consist of only English letters.
- All the characters of `jewels` are **unique**.

---

## 🧩 Approach

We use a simple frequency array of size 128 (for all ASCII characters) to mark the characters that are jewels. Then, we iterate through the `stones` string and check how many of those are marked as jewels.

This approach is both time and space efficient.

---

## 💻 Java Solution

```java
class Solution {
    public int numJewelsInStones(String jewels, String stones) {
        int[] s = new int[128]; // ASCII table size
        for (char c : jewels.toCharArray()) {
            s[c] = 1; // Mark character as a jewel
        }
        int ans = 0;
        for (char c : stones.toCharArray()) {
            ans += s[c]; // Count jewels in stones
        }
        return ans;
    }
}
🏁 Output

Input	Output
jewels = "aA"
stones = "aAAbbbb"	3
jewels = "z"
stones = "ZZ"	0
🧮 Complexity Analysis
Time Complexity: O(n + m), where n is the length of jewels and m is the length of stones.

Space Complexity: O(1) – fixed size array used for ASCII characters.

📂 Related Topics
Hash Table

String

🏷️ Tags
#LeetCode #Java #HashMap #String #Easy #771

🌟 Star this repository if you found the solution helpful!

yaml
Copy
Edit

---

Let me know if you'd like the same format for other LeetCode problems too!






