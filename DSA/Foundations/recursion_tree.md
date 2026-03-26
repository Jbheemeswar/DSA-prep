# Recursion Tree Method

## 📌 Definition

The recursion tree method is used to solve recurrence relations by expanding them into a tree and calculating the total work done at each level.

---

## 🔹 Key Idea

* Break recurrence into levels
* Each level represents recursive calls
* Calculate work at each level
* Add all levels to get total time

---

## 🔹 Example

Solve:
T(n) = 2T(n/2) + n

---

## 🔹 Step 1: Build Tree

Level 0:
Cost = n

Level 1:
2 calls → each does work n/2
Total = n

Level 2:
4 calls → each does work n/4
Total = n

...

---

## 🔹 Step 2: Find Number of Levels

n → n/2 → n/4 → ... → 1

Number of levels = log n

---

## 🔹 Step 3: Total Cost

Each level cost = n
Number of levels = log n

Total:
T(n) = n * log n

---

## 🔹 General Pattern

If each level does same work:
T(n) = (work per level) × (number of levels)

---

## 🔹 Another Example

T(n) = T(n/2) + n

Level 0 → n
Level 1 → n/2
Level 2 → n/4
...

Total:
n + n/2 + n/4 + ... = 2n = O(n)

---

## ⚠️ Mistakes I Made

* Didn’t calculate cost per level properly
* Ignored number of levels
* Confused decreasing vs constant work
* Stopped tree expansion too early

---

## 🎯 Key Insight

Recursion tree helps visualize how total work is distributed across levels.
