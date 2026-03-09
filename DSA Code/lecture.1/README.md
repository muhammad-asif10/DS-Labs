# 📚 Lecture 1 – Introduction to Arrays

### Static & Dynamic Memory Allocation in C++

This folder covers the introductory lecture on **arrays** in C++, demonstrating the difference between **static arrays** (compile-time size) and **dynamic arrays** (runtime heap allocation).

---

## 📁 Files

| File | Description |
|------|-------------|
| `example1.cpp` | Static array declaration, initialization and traversal |
| `example2.cpp` | Dynamic array allocation using `new`, input from user, and `delete[]` cleanup |

---

## 🧠 Concepts Covered

- **Static Arrays** – Fixed-size arrays declared on the stack
- **Dynamic Arrays** – Heap-allocated arrays using `new int[n]`
- **Memory Deallocation** – Using `delete[]` to avoid memory leaks
- **Array Traversal** – Using `for` loops to read and print elements

---

## 🔍 Example Walkthrough

### `example1.cpp` – Static Array
Declares an integer array of size 6, fills it with multiples of 2 (`0, 2, 4, 6, 8, 10`), and prints the elements.

### `example2.cpp` – Dynamic Array
Asks the user for a size `n`, allocates memory on the heap, fills the array with values `1` through `n`, prints them, and then frees the memory.

---

## 🚀 How to Compile & Run

```bash
g++ example1.cpp -o example1
./example1

g++ example2.cpp -o example2
./example2
```

---

## 📈 Time Complexity

| Operation | Complexity |
|-----------|------------|
| Array traversal | O(n) |
| Element access by index | O(1) |

---

## 👤 Author

**Muhammad Asif**
