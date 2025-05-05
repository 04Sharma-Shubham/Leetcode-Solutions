# 📐 LeetCode 492 — Construct the Rectangle

## 💡 Problem Description

A web developer needs to know how to design a web page's size. Given a specific rectangular web page’s `area`, your job is to design a rectangular page where:

- The area equals the given target.
- The **length `L`** is **greater than or equal to the width `W`** (i.e., `L ≥ W`).
- The **difference** between `L` and `W` is as **small as possible**.

Return an array `[L, W]` representing the dimensions of the web page.

---

### 🔗 Problem Link

[LeetCode 492 - Construct the Rectangle](https://leetcode.com/problems/construct-the-rectangle/)

---

## ✅ Approach

- Start checking from the integer square root of the area (i.e., the closest possible width to make `L - W` minimal).
- Decrease `W` until it evenly divides the area.
- Return `[L, W]` where `L = area / W`.

This guarantees:
- `L * W == area`
- `L ≥ W`
- `L - W` is minimized

---

## 💻 Java Code

```java
class Solution {
    public int[] constructRectangle(int area) {
        int w = (int) Math.sqrt(area);
        while (area % w != 0) {
            --w;
        }
        return new int[] {area / w, w};
    }
}
```

---

## 📊 Examples

### Example 1:

**Input:** `area = 4`  
**Output:** `[2, 2]`  
**Explanation:** Possible pairs: `[1, 4]`, `[2, 2]`, `[4, 1]`. Only `[2, 2]` meets all conditions.

---

### Example 2:

**Input:** `area = 37`  
**Output:** `[37, 1]`  
**Explanation:** 37 is a prime number, so only possible dimensions are `[37, 1]`.

---

### Example 3:

**Input:** `area = 122122`  
**Output:** `[427, 286]`

---

## ⏱️ Time and Space Complexity

**Time Complexity:** O(√n) — In the worst case, we scan backward from √area to 1.  
**Space Complexity:** O(1) — Only constant extra space is used.

---

## 🏷️ Tags

Math, Geometry, Simulation, Brute Force
