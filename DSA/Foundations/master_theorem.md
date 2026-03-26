# Master Theorem

## 📌 Definition

Master Theorem is used to solve recurrence relations of the form:

T(n) = aT(n/b) + f(n)

Where:

* a → number of subproblems
* b → factor by which input is divided
* f(n) → work done outside recursion

---

## 🔹 Key Idea

Compare:
f(n)  vs  n^(log_b a)

This comparison decides the final complexity.

---

## 🔹 Case 1 (Leaf Dominates)

If:
f(n) = O(n^(log_b a - ε))

Then:
T(n) = Θ(n^(log_b a))

---

## 🔹 Case 2 (Balanced)

If:
f(n) = Θ(n^(log_b a))

Then:
T(n) = Θ(n^(log_b a) * log n)

---

## 🔹 Case 3 (Root Dominates)

If:
f(n) = Ω(n^(log_b a + ε))

Then:
T(n) = Θ(f(n))

(Regularity condition must hold)

---

## 🔹 Examples

### Example 1

T(n) = 2T(n/2) + n

* a = 2, b = 2
* n^(log_b a) = n

→ Case 2

T(n) = Θ(n log n)

---

### Example 2

T(n) = T(n/2) + n

* a = 1, b = 2
* n^(log_b a) = 1

→ Case 3

T(n) = Θ(n)

---

### Example 3

T(n) = 4T(n/2) + n

* a = 4, b = 2
* n^(log_b a) = n²

→ Case 1

T(n) = Θ(n²)

---

## ⚠️ When NOT to use

* If subproblem sizes are not equal
* If recurrence is not in form aT(n/b) + f(n)
* Example:
  T(n) = T(n/2) + T(n/3) + n ❌

---

## ⚠️ Mistakes I Made

* Didn’t compare f(n) with n^(log_b a)
* Forgot which case applies
* Tried to memorize instead of understanding
* Applied theorem to invalid recurrences

---

## 🎯 Key Insight

Master Theorem is a shortcut for recursion tree analysis, not a replacement for understanding.
