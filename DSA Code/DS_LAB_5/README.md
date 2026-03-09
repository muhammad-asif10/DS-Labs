# 📚 DS Lab 5 – Queues

### Linear Queue, Fixed-Size Array Queue, Circular Queue & Printer Job Simulation in Python

This lab explores the **Queue** data structure — a First In, First Out (FIFO) collection — through multiple implementations and a real-world simulation.

---

## 📁 Files

| File | Description |
|------|-------------|
| `DS_Lab5.ipynb` | Complete lab notebook covering all queue variants and the mini-project |

---

## 🧠 Concepts Covered

### Warm-Up – Basic FIFO Queue
Simple queue using Python's built-in list with `append()` (enqueue) and `pop(0)` (dequeue) to demonstrate FIFO behavior.

### Teaching Queue (List-Backed)
A Python class wrapping a list:
- `enqueue(item)` – add to rear
- `dequeue()` – remove from front
- `peek()` – inspect front element
- `is_empty()` – check emptiness
- `size()` – return current length

### Fixed-Size Array Queue
Array-backed queue with a maximum capacity:
- Tracks `front` and `rear` indices
- Raises an error on overflow (queue full) or underflow (queue empty)
- Illustrates the limitations of a simple array queue (wasted space after dequeues)

### Circular Queue
Solves the wasted-space problem using **modular arithmetic**:
- `rear = (rear + 1) % capacity`
- `front = (front + 1) % capacity`
- Efficiently reuses freed slots at the beginning of the array
- Distinguishes between full and empty states

### Mini-Project – Printer Job Simulation (FCFS)
Simulates a **First-Come-First-Served** print queue:
- Jobs are enqueued with a name and number of pages
- The printer dequeues and processes one job at a time
- Tracks total pages printed and job completion order

---

## 🔍 Circular Queue – How It Works

```
Initial (capacity=5):  [ _, _, _, _, _ ]
Enqueue A, B, C:       [ A, B, C, _, _ ]   front=0, rear=3
Dequeue A:             [ _, B, C, _, _ ]   front=1, rear=3
Enqueue D, E, F:       [ F, B, C, D, E ]   front=1, rear=1  (wraps around)
```

---

## 🚀 How to Run

```bash
jupyter notebook DS_Lab5.ipynb
```

Python 3.x is required.

---

## 📈 Time Complexity

| Operation | List Queue | Array Queue | Circular Queue |
|-----------|-----------|-------------|----------------|
| Enqueue | O(1) amortized | O(1) | O(1) |
| Dequeue | O(n) – `pop(0)` | O(1) | O(1) |
| Peek | O(1) | O(1) | O(1) |
| Space | O(n) | O(capacity) fixed | O(capacity) fixed |

> **Note:** `list.pop(0)` is O(n) due to shifting. Use `collections.deque` for O(1) dequeue on both ends.

---

## 👤 Author

**Muhammad Asif**
