# Space Complexity

## 📌 Definition

Space complexity measures how much extra memory an algorithm uses relative to input size (n).

---

## 🔹 Types of Space

### 1. Input Space

* Memory required to store input
* Not counted in most interview problems

---

### 2. Auxiliary Space (Important)

* Extra space used by algorithm
* This is what interviewers care about

---

## 📊 Common Complexities

* O(1): Constant space (no extra memory)
* O(n): Linear space (extra array/list)
* O(n²): 2D structures

---

## 🔹 Examples

### O(1)

```python
sum = 0
for i in arr:
    sum += i
```

### O(n)

```python
new_arr = [x*2 for x in arr]
```

### O(n) (Recursion stack)

```python
def func(n):
    if n == 0:
        return
    func(n-1)
```

---

## 🔹 Important Cases

* Recursion uses stack space → O(n)
* Iteration usually → O(1)
* Using extra arrays → increases space

---

## 🔹 In-place Algorithms

* Modify input directly
* Use O(1) space

Example:
Two pointers, swapping elements

---

## ⚠️ Mistakes I Made

* Thought input array counts in space complexity
* Ignored recursion stack space
* Confused in-place vs extra space

---

## 🎯 Key Insight

Space complexity is about extra memory used, not input size.
