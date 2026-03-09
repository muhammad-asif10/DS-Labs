# 📚 DS Lab 3 – Stacks

### Stack Implementations Using Static Arrays & Linked Lists in C++

This lab implements the **Stack** abstract data type (ADT) using two different underlying structures — a fixed-size array and a singly linked list — and compares their trade-offs.

---

## 📁 Files

| File | Description |
|------|-------------|
| `Task1.cpp` | Dynamic `ArrayWrapper` class with constructor/destructor and safe memory management |
| `Task2.cpp` | Stack implemented using a **static array** (`MAX_SIZE = 5`) with overflow/underflow detection |
| `Task3.cpp` | Stack implemented using a **singly linked list** (unbounded, no overflow) |
| `Task4.cpp` | Side-by-side comparison of `StackArray` vs `StackList` |
| `Task5.cpp` | Full stack demo with comprehensive overflow and underflow test cases |

---

## 🧠 Concepts Covered

- **ArrayWrapper** – Demonstrates RAII: constructor allocates heap array; destructor frees it
- **Stack ADT** – LIFO (Last In, First Out) principle
- **StackArray** – `push`, `pop`, `peek`, and `print` on a fixed-size array; detects stack overflow
- **StackList** – Node-based stack with dynamic growth; proper destructor cleans all nodes
- **Stack Overflow** – Attempting to push onto a full array stack
- **Stack Underflow** – Attempting to pop from an empty stack

---

## 🔍 Sample Output

### Task2 – Array Stack (MAX_SIZE = 5)
```
Pushed: 10
Pushed: 20
Pushed: 30
Pushed: 40
Pushed: 50
ERROR: STACK OVERFLOW! Cannot push 60 (Array is full).
StackArray (TOP->BOT): [ 50, 40, 30, 20, 10 ]
Popped value: 50
StackArray (TOP->BOT): [ 40, 30, 20, 10 ]
```

### Task3 – Linked List Stack
```
Pushed: 100
Pushed: 200
Pushed: 300
StackList (TOP->BOT): [ 300, 200, 100 ]
Popped value: 300
Pushed: 400
StackList (TOP->BOT): [ 400, 200, 100 ]
```

---

## 🚀 How to Compile & Run

```bash
g++ Task1.cpp -o task1 && ./task1
g++ Task2.cpp -o task2 && ./task2
g++ Task3.cpp -o task3 && ./task3
g++ Task4.cpp -o task4 && ./task4
g++ Task5.cpp -o task5 && ./task5
```

---

## 📈 Time Complexity

| Operation | StackArray | StackList |
|-----------|------------|-----------|
| `push` | O(1) | O(1) |
| `pop` | O(1) | O(1) |
| `peek` | O(1) | O(1) |
| Space | O(MAX_SIZE) fixed | O(n) dynamic |
| Overflow risk | Yes (bounded) | No (heap limited) |

---

## 🔄 Trade-offs

| Feature | Array Stack | Linked List Stack |
|---------|-------------|-------------------|
| Memory allocation | Static / upfront | Dynamic / on demand |
| Overflow possible? | Yes | No |
| Cache performance | Better (contiguous) | Worse (scattered) |
| Implementation complexity | Simple | Slightly more complex |

---

## 👤 Author

**Muhammad Asif**
