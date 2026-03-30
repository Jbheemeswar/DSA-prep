# Two Pointers

## 📌 Definition

Two Pointers is a technique where two indices move through the data (usually from opposite ends or same direction) to reduce time complexity, often from O(n²) → O(n).

---

## 🔹 When to Use

* Sorted arrays
* Pairs / triplets problems
* Removing duplicates
* Partitioning / rearranging

---

## 🔹 Types of Two Pointers

### 1. Opposite Direction

* One pointer at start, one at end

Example:

```python
left = 0
right = len(arr) - 1
```

Used in:

* Pair sum in sorted array
* Container with most water

---

### 2. Same Direction (Fast & Slow)

* Both move forward
* One moves faster

Example:

```python
slow = 0
for fast in range(len(arr)):
    if condition:
        arr[slow] = arr[fast]
        slow += 1
```

Used in:

* Remove duplicates
* Move zeroes

---

## 🔹 Key Logic

* Decide condition
* Move pointers based on condition
* Avoid nested loops

---

## 🔹 Example (Sorted Pair Sum)

```python
arr = [1,2,3,4,6]
target = 6

left = 0
right = len(arr) - 1

while left < right:
    s = arr[left] + arr[right]
    
    if s == target:
        print(left, right)
        break
    elif s < target:
        left += 1
    else:
        right -= 1
```

---

## 🔹 Time Complexity

* O(n) (each element visited at most once)

---

## ⚠️ Mistakes I Made

* Used nested loops instead of two pointers
* Forgot array must be sorted
* Moved wrong pointer
* Didn’t handle duplicates properly

---

## 🎯 Key Insight

Two pointers reduce unnecessary comparisons by using structure (sorted data or constraints).

---

## 🔹 Practice Problems

* Reverse a String (344)
* Valid Palindrome (125)
* Remove Duplicates from Sorted Array (26)
* Two Sum II - Input Array is Sorted (167)
* Container With Most Water (11)

---

## 🎯 Why These Matter

* Reverse String → basic pointer movement
* Valid Palindrome → skip + compare logic
* Remove Duplicates → fast & slow pointers
* Two Sum II → classic opposite pointers
* Container → decision-based pointer movement
