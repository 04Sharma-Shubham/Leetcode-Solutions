# 📝 LeetCode 58 — Length of Last Word

## 💡 Problem Description

Given a string `s` consisting of words and spaces, return the **length of the last word** in the string.

A **word** is defined as a maximal substring consisting of non-space characters only.

---

### 🔗 Problem Link

[LeetCode 58 - Length of Last Word](https://leetcode.com/problems/length-of-last-word/)

---

## ✅ Approach

- First, trim the string to remove any trailing spaces.
- Split the string by spaces to isolate words.
- The last word will be the last element in the resulting array.
- Return the length of that word.

---

## 💻 Java Code

```java
class Solution {
    public int lengthOfLastWord(String s) {
        s = s.trim();
        String[] word = s.split(" ");
        String lastWord = word[word.length - 1];
        return lastWord.length();
    }
}
```

---

## 📊 Examples

### Example 1:

**Input:**  
`s = "Hello World"`  
**Output:**  
`5`  
**Explanation:** The last word is `"World"`.

---

### Example 2:

**Input:**  
`s = "   fly me   to   the moon  "`  
**Output:**  
`4`  
**Explanation:** The last word is `"moon"`.

---

### Example 3:

**Input:**  
`s = "luffy is still joyboy"`  
**Output:**  
`6`  
**Explanation:** The last word is `"joyboy"`.

---

## ⏱️ Time and Space Complexity

**Time Complexity:** O(n)  
**Space Complexity:** O(n), due to the array created by `split`.

---

## 🏷️ Tags

String, Parsing, Basic Manipulation
