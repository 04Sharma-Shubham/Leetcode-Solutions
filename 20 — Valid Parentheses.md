# 🔒 LeetCode 20 — Valid Parentheses

## 💡 Problem Description

Given a string `s` containing just the characters `'('`, `')'`, `'{'`, `'}'`, `'['` and `']'`, determine if the input string is **valid**.

### A string is valid if:
- Open brackets must be closed by the same type of brackets.
- Open brackets must be closed in the correct order.
- Every close bracket has a corresponding open bracket of the same type.

---

### 🔗 Problem Link

[LeetCode 20 - Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)

---

## ✅ Approach

- Use a **stack** to keep track of expected closing brackets.
- For every opening bracket, push the corresponding closing bracket to the stack.
- For every closing bracket, check if it matches the top of the stack.
- If not, or if the stack is empty before a match is found, return `false`.
- If the stack is empty at the end, the string is valid.

---

## 💻 Java Code

```java
class Solution {
    public boolean isValid(String s) {
        Deque<Character> stack = new ArrayDeque<>();

        for (final char c : s.toCharArray())
            if (c == '(')
                stack.push(')');
            else if (c == '{')
                stack.push('}');
            else if (c == '[')
                stack.push(']');
            else if (stack.isEmpty() || stack.pop() != c)
                return false;

        return stack.isEmpty();
    }
}
```

---

## 📊 Examples

### Example 1:

**Input:**  
`s = "()"`  
**Output:**  
`true`

---

### Example 2:

**Input:**  
`s = "()[]{}"`  
**Output:**  
`true`

---

### Example 3:

**Input:**  
`s = "(]"`  
**Output:**  
`false`

---

### Example 4:

**Input:**  
`s = "([])"`  
**Output:**  
`true`

---

## ⏱️ Time and Space Complexity

**Time Complexity:** O(n) — Each character is processed once.  
**Space Complexity:** O(n) — In the worst case, the stack stores all characters.

---

## 🏷️ Tags

Stack, String, Data Structures

---

📌 This is a classic stack problem used to validate sequences of brackets in compilers and interpreters.
