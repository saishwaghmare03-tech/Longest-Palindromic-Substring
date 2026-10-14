# Longest Palindromic Substring 🧩

[![LeetCode](https://img.shields.io/badge/LeetCode-Medium-orange.svg)](https://leetcode.com/problems/longest-palindromic-substring/)
[![Java](https://img.shields.io/badge/Language-Java-blue.svg)](https://www.java.com/)

A clean, optimal, and well-documented Java solution for the classic **Longest Palindromic Substring** problem using the **Expand Around Center** approach.

---

## 📖 Problem Statement

Given a string `s`, return the longest palindromic substring in `s`.

### Examples

* **Example 1:**
  * **Input:** `s = "babad"`
  * **Output:** `"bab"` *(Note: `"aba"` is also a valid answer.)*

* **Example 2:**
  * **Input:** `s = "cbbd"`
  * **Output:** `"bb"`

### Constraints
* $1 \le \text{s.length} \le 1000$
* `s` consists of only digits and English letters.

---

## 💡 Approach: Expand Around Center

Instead of checking every possible substring ($O(n^3)$ time) or using extra space for Dynamic Programming ($O(n^2)$ space), this solution treats every character and the gap between characters as a potential **center** of a palindrome:
1. **Odd-length palindromes:** Centered at a single character (e.g., `"aba"` centered at index `i`).
2. **Even-length palindromes:** Centered between two characters (e.g., `"abba"` centered between index `i` and `i + 1`).

We expand outwards from each center as long as the characters match, keeping track of the maximum length and start/end pointers.

---

## ⏱️ Complexity Analysis

* **Time Complexity:** $O(n^2)$, where $n$ is the length of the string. There are $2n - 1$ possible centers, and expanding around each takes up to $O(n)$ time.
* **Space Complexity:** $O(1)$, as it only uses a few pointer variables without allocating any extra data structures.

---

## 🚀 Getting Started

### Prerequisites
Make sure you have Java installed on your machine. You can check via your terminal:
```bash
java -version
