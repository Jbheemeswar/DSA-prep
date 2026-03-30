# Arrays and Strings

---

## 🔹 Arrays (List in Python)

### 📌 Definition

Array is a collection of elements stored in contiguous memory locations and accessed using index.

(In Python → implemented using lists)

---

## 🔹 Four Fundamental Array Operations

1. **Access**

   * Get element using index
   * O(1)

2. **Insertion**

   * Add element
   * End → O(1)
   * Middle → O(n)

3. **Deletion**

   * Remove element
   * O(n) (shifting required)

4. **Traversal**

   * Visit all elements
   * O(n)

---

## 🔹 Key Insight

* Arrays give fast access
* But insertion/deletion (middle) is costly

---

## 🔹 Strings

### 📌 Definition

String is a sequence of characters.

---

## 🔹 Important Properties

### 1. Strings are Immutable

* Cannot change characters directly
* New string is created

```python id="2x0y1z"
s = "abc"
s = s + "d"
```

---

### 2. Length

```python id="l7pz6m"
len(s)
```

---

### 3. Indexing

```python id="9z9n6y"
s[0], s[-1]
```

---

### 4. Slicing

```python id="p7u2qv"
s[1:4]
```

---

### 5. Traversal

```python id="l2y1nm"
for ch in s:
    print(ch)
```

---

### 6. Comparison

```python id="6q8q3n"
"abc" == "abc"
"abc" < "abd"
```

---

### 7. Reverse String

```python id="m3h8zt"
s[::-1]
```

---

### 8. Convert String to List

```python id="n4x5po"
list(s)
```

---

## ⚠️ Mistakes I Made

* Tried modifying string directly
* Forgot slicing creates new string
* Used string instead of list for modifications

---

## 🎯 Key Insight

* Use list when you need modification
* Use string when immutability is fine
