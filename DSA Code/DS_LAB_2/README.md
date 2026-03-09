# 📚 DS Lab 2 – Arrays & Linked Lists

### Array Operations, Singly Linked Lists, Doubly Linked Lists & Circular Linked Lists in C++

This lab covers **fundamental array manipulation** and introduces **linked list data structures** — singly, doubly, and circular — with insertion, deletion, and traversal operations.

---

## 📁 Files

| File | Description |
|------|-------------|
| `TaskA1.cpp` | Array insertion – shifting elements right to insert at a given position |
| `TaskA2.cpp` | Array deletion – shifting elements left to remove at a given position |
| `TaskB1.cpp` | Singly linked list – manual node creation and traversal |
| `TaskB2.cpp` | Singly linked list – `insertAtHead` and `deleteHead` operations |
| `TaskC1.cpp` | Doubly linked list – forward and backward traversal |
| `TaskD1.cpp` | Circular linked list – creation and single-round traversal |
| `TaskD2.cpp` | Josephus Problem – circular list elimination (every 3rd person) |

---

## 🧠 Concepts Covered

### Part A – Arrays
- **Insertion at position** – shift elements right from the end, then place the new value
- **Deletion at position** – shift elements left to overwrite the deleted slot; decrement size

### Part B – Singly Linked List
- Node structure with `data` and `next` pointer
- Manual linking of nodes
- `insertAtHead` – O(1) prepend
- `deleteHead` – O(1) remove from front
- List traversal using a `temp` pointer

### Part C – Doubly Linked List
- Node structure with `data`, `next`, and `prev` pointers
- **Forward traversal** (head → tail)
- **Backward traversal** (tail → head)

### Part D – Circular Linked List & Josephus Problem
- Circular list where the last node points back to `head`
- Traversal stops after `n` iterations to avoid infinite loop
- **Josephus Problem** – simulation of `N=10` people, eliminating every `M=3`rd

---

## 🔍 Sample Output

### TaskA1 – Array Insertion (value 9 at index 3)
```
After insertion: 2  6  8  9  7  1
```

### TaskA2 – Array Deletion (index 2)
```
After deletion: 2  6  7  1
```

### TaskB1 – Linked List Traversal
```
Linked List: 10  20  30
```

### TaskB2 – Insert & Delete Head
```
List: 10 20 30
List: 20 30
```

### TaskD2 – Josephus Elimination Order
```
Removing: 3
Removing: 6
Removing: 9
...
Leader is: <last remaining node>
```

---

## 🚀 How to Compile & Run

```bash
g++ TaskA1.cpp -o taskA1 && ./taskA1
g++ TaskA2.cpp -o taskA2 && ./taskA2
g++ TaskB1.cpp -o taskB1 && ./taskB1
g++ TaskB2.cpp -o taskB2 && ./taskB2
g++ TaskC1.cpp -o taskC1 && ./taskC1
g++ TaskD1.cpp -o taskD1 && ./taskD1
g++ TaskD2.cpp -o taskD2 && ./taskD2
```

---

## 📈 Time Complexity

| Operation | Array | Linked List |
|-----------|-------|-------------|
| Access by index | O(1) | O(n) |
| Insert at head | O(n) – shift | O(1) |
| Delete at head | O(n) – shift | O(1) |
| Insert at position | O(n) | O(n) – traversal |
| Traversal | O(n) | O(n) |

---

## 👤 Author

**Muhammad Asif**
