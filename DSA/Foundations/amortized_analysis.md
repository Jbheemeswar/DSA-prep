# Amortized Analysis

## 📌 Definition

Amortized analysis calculates the average time per operation over a sequence of operations, where some operations are expensive but occur rarely.

It is NOT simple averaging. It distributes the cost of expensive operations across many cheap operations.

---

## 🔹 Key Idea

* Most operations are cheap → O(1)
* Few operations are expensive → O(n)
* Expensive operations happen rarely
* Overall average per operation becomes small

---

## 🔹 Example: Dynamic Array (Python List)

```python
arr = []
for i in range(n):
    arr.append(i)
```

### What happens:

* Most `append()` → O(1)
* Occasionally resize → O(n)

### Final:

Amortized time per append = **O(1)**

---

## 🔹 Why?

* Array capacity doubles when full
* Resizing doesn’t happen every time
* Total cost spreads across many operations

---

## 🔹 Types of Amortized Analysis

### 1. Aggregate Method

Total cost of all operations ÷ number of operations

---

### 2. Accounting Method

Assign extra cost to cheap operations to pay for expensive ones later

---

### 3. Potential Method

Use stored "potential energy" to balance operation costs

---

## 🔹 Key Observation

Even though one operation can be O(n),
overall sequence behaves like O(1) per operation

---

## ⚠️ Mistakes I Made

* Thought amortized = simple average
* Ignored sequence of operations
* Didn’t understand why append is O(1)
* Focused only on worst-case per operation

---

## 🎯 Key Insight

Amortized analysis focuses on overall efficiency across multiple operations, not the cost of a single operation.
