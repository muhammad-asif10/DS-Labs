# 📚 DS Lab 7 – Queue Applications & Priority Queue

### Bank Queue Simulation, Priority Queues & Mixed Queue Challenge in Python

This lab applies **Queue** variants to real-world scenarios, including a bank service simulation, numeric priority queues, and signed-priority queues.

---

## 📁 Files

| File | Description |
|------|-------------|
| `DS_LAB7.ipynb` | Complete lab notebook covering all four tasks |

---

## 🧠 Concepts Covered

### Task 1 – Bank Queue Simulation (FIFO)
Simulates a standard **First-Come-First-Served** bank queue:
- Customers arrive and are enqueued with their names and service times
- Teller serves customers one at a time in arrival order
- Tracks total wait time and service completion

### Task 2 – Priority Queue (Numeric Priority)
Implements a **min-priority queue** where lower numbers indicate higher priority:
- Patients/customers assigned a numeric priority (e.g., 1 = highest)
- Queue always serves the highest-priority element first, regardless of arrival order
- Built using a sorted list or linear scan for minimum

**Example:**
```
Enqueue: (priority=3, "Alice"), (priority=1, "Bob"), (priority=2, "Carol")
Dequeue order: Bob (1) → Carol (2) → Alice (3)
```

### Task 3 – Priority Queue with +/- Signs
Extends the priority queue to support **signed priorities**:
- Positive sign = standard priority
- Negative sign = special/emergency handling
- Demonstrates how priority definitions can be customized

### Task 4 – Mixed Queue Challenge (Bonus)
Combines FIFO and priority-based behavior in a single queue:
- Regular items are processed in FIFO order
- Priority-flagged items jump ahead in the queue
- Tests edge cases including empty queue and tie-breaking

---

## 🔍 Priority Queue vs Regular Queue

| Feature | Regular Queue | Priority Queue |
|---------|--------------|----------------|
| Order | Arrival order (FIFO) | Priority order |
| Dequeue | Always from front | Highest-priority element |
| Use case | Print queue, bank line | OS scheduling, ER triage |

---

## 🚀 How to Run

```bash
jupyter notebook DS_LAB7.ipynb
```

Python 3.x is required.

---

## 📈 Time Complexity

| Operation | Simple List Priority Queue | Heap-Based Priority Queue |
|-----------|---------------------------|--------------------------|
| Enqueue | O(1) | O(log n) |
| Dequeue (highest priority) | O(n) – linear scan | O(log n) |
| Peek | O(n) | O(1) |

> Python's `heapq` module provides an efficient O(log n) heap-based priority queue.

---

## 👤 Author

**Muhammad Asif**
