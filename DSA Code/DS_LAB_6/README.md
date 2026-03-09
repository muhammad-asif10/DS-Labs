# 📚 DS Lab 6 – Deque (Double-Ended Queue)

### Deque Operations, Doorway Traffic Simulation & Palindrome Checker in Python

This lab implements the **Deque** (Double-Ended Queue) data structure, which allows insertion and removal from **both ends**, and applies it to two practical problems.

---

## 📁 Files

| File | Description |
|------|-------------|
| `DUQUE_LAB6_DS.ipynb` | Main lab notebook — Deque implementation and both problem tasks |
| `DS_LAB_8/Queue.py` | Supporting Python file with queue/priority queue utilities |

---

## 🧠 Concepts Covered

### Core Deque Operations
A custom `Deque` class built on a Python list:

| Method | Description |
|--------|-------------|
| `add_front(item)` | Insert element at the front |
| `add_rear(item)` | Insert element at the rear |
| `remove_front()` | Remove and return element from front |
| `remove_rear()` | Remove and return element from rear |
| `peek_front()` | View front element without removing |
| `peek_rear()` | View rear element without removing |
| `is_empty()` | Check if deque has no elements |
| `size()` | Return number of elements |

### Problem 1 – Doorway Traffic Simulation
Models two streams of people entering/exiting through a doorway:
- **Entering** people are added to the rear of the deque
- **Exiting** people are removed from the front
- Demonstrates how a deque models bidirectional flow

### Problem 2 – Palindrome Checker Using Deque
Checks whether a string is a palindrome:
- Characters are added to the deque
- Characters are simultaneously removed from both front and rear and compared
- If all pairs match, the string is a palindrome

**Examples:**
```
"racecar"  → Palindrome ✅
"radar"    → Palindrome ✅
"hello"    → Not a palindrome ❌
```

---

## 🔍 Deque vs Queue vs Stack

| Feature | Stack | Queue | Deque |
|---------|-------|-------|-------|
| Insert front | ✅ (push) | ❌ | ✅ |
| Insert rear | ❌ | ✅ (enqueue) | ✅ |
| Remove front | ✅ (pop) | ✅ (dequeue) | ✅ |
| Remove rear | ❌ | ❌ | ✅ |

---

## 🚀 How to Run

```bash
jupyter notebook DUQUE_LAB6_DS.ipynb
```

Python 3.x is required.

---

## 📈 Time Complexity

| Operation | Time Complexity |
|-----------|----------------|
| `add_front` | O(n) – list insert at index 0 |
| `add_rear` | O(1) – list append |
| `remove_front` | O(n) – list `pop(0)` |
| `remove_rear` | O(1) – list `pop()` |
| Palindrome check | O(n) |

> For O(1) on both ends, use Python's `collections.deque`.

---

## 👤 Author

**Muhammad Asif**
