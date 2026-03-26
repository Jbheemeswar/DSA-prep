# Time Complexity

## 📌 Definition

Time complexity describes how the runtime of an algorithm grows with input size (n), not actual execution time.

---

## 📊 Order of Growth (Important)

O(1) < O(log n) < O(n) < O(n log n) < O(n²) < O(2ⁿ) < O(n!)

---

## 🔹 Common Examples

* O(1): Access array element
* O(n): Single loop
* O(n²): Nested loops
* O(log n): Binary search

---

## 🔹 Rules to Calculate

1. Drop constants
   O(2n) → O(n)

2. Keep highest order term
   O(n² + n) → O(n²)

3. Nested loops → multiply
   Example:
   for i in range(n):
   for j in range(n):
   → O(n²)

4. Sequential loops → add
   O(n) + O(n) → O(n)

---

## 🔹 Special Case (Important)

Not all nested loops are O(n²)

Example:
left = 0
for right in range(n):
while left < right:
left += 1

→ Overall complexity = O(n), not O(n²)

---

## 🔹 Best / Average / Worst Case

* Best → minimum time
* Average → expected
* Worst → maximum (focus in interviews)

---

## 🔹 Pattern Mapping

* Two Pointers → O(n)
* Sliding Window → O(n)
* Binary Search → O(log n)

---

## ⚠️ Mistakes I Made

* Thought every nested loop = O(n²)
* Ignored worst-case analysis
* Misunderstood while loops in sliding window

---

## 🎯 Key Insight

Time complexity is about growth trend, not exact runtime.
