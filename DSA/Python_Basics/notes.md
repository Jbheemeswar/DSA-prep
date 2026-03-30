# Python Basics for DSA

## 🔹 Lists

* Dynamic array
* Use for ordered data

Key:
arr = [1,2,3]
arr.append(x)
arr.pop()

---

## 🔹 Tuples

* Immutable list
* Faster than list

Key:
t = (1,2,3)

---

## 🔹 Sets

* Unique elements
* Fast lookup O(1)

Key:
s = set()
s.add(x)
x in s

---

## 🔹 Dictionaries (HashMap)

* Key-value storage
* O(1) lookup

Key:
d = {}
d[key] = value
d.get(key, 0)

---

## 🔹 List Comprehension

* Compact way to build lists

Key:
[x for x in arr if x > 0]

---

## 🔹 Collections

### defaultdict

### defaultdict

* Automatically assigns a default value if key is missing
* Avoids KeyError and manual checks

```python
from collections import defaultdict
d = defaultdict(int)
```

## 🔹 Use Cases

### 1. Frequency Counting (MOST COMMON)

```python
arr = [1,2,2,3]

d = defaultdict(int)
for x in arr:
    d[x] += 1

# Result: {1:1, 2:2, 3:1}
```

---

### 2. Grouping Elements

```python
pairs = [("a",1), ("b",2), ("a",3)]

d = defaultdict(list)
for key, val in pairs:
    d[key].append(val)

# Result: {'a': [1,3], 'b': [2]}
```

---

## ⚠️ Why use defaultdict?

Without it:

```python
if key not in d:
    d[key] = 0
d[key] += 1
```

With defaultdict:

```python
d[key] += 1
```

---

## 🎯 Key Insight

Use defaultdict when:

* you are counting
* grouping values
* avoiding manual initialization
Example:
  
from collections import defaultdict

ar = [1,2]
dicit = defaultdict(int)

for i in ar:
    dicit[i] += 1

print(dicit)
Execution:
i = 1 → dicit[1] = 0 → +1 → 1
i = 2 → dicit[2] = 0 → +1 → 1

👉 Final:

{1:1, 2:1}
---

### Counter

* Count frequency

from collections import Counter
c = Counter(arr)

---

### deque

* Fast insert/delete both ends

from collections import deque
dq = deque()
dq.append()
dq.popleft()

---

## 🔹 heapq

* Min heap

import heapq
heapq.heappush(heap, x)
heapq.heappop(heap)

---

## 🔹 bisect

* Binary search in sorted list

import bisect
bisect.bisect_left(arr, x)

---

## 🔹 Custom Sorting

* Sort with key

arr.sort(key=lambda x: x[1])

---

## ⚠️ Mistakes I Made

* Used list instead of set → slow lookup
* Forgot defaultdict → wrote extra checks
* Confused heap (min vs max)

---

## 🎯 Key Insight

Choose data structure based on operation:

* lookup → set/dict
* order → list
* frequency → Counter
