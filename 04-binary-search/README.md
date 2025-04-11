# Binary Search Pattern

## 🔍 Pattern Overview

Binary Search cuts the search space in half each time. Ideal for sorted data or problems where a decision can be made at each step.

## 📘 When to Use

- Searching in sorted arrays or conditions with a monotonic behavior
- Finding the first/last occurrence of an element
- Optimizing for min/max in a numeric range

## 🧠 Strategy

- Use left/right pointers
- Midpoint check determines which side to discard
- Narrow the search window until you find the result

## 📌 Example Problems

- [ ] [Binary Search](https://leetcode.com/problems/binary-search/)
- [ ] [Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- [ ] [Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/)
- [ ] [Koko Eating Bananas](https://leetcode.com/problems/koko-eating-bananas/)
- [ ] [Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/)

## 🧵 Time & Space Complexity

- **Time:** O(log n)
- **Space:** O(1) (iterative), O(log n) (recursive)
