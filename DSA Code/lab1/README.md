# 📚 Lab 1 (lab1) – Pointers & Dynamic Memory Management

### Pointers, Double Pointers, and Heap Memory in C++

This lab dives deep into **pointer mechanics** in C++, covering pointer-to-pointer, dynamic arrays, safe deletion, and identifying memory leaks.

---

## 📁 Files

| File | Description |
|------|-------------|
| `task1.cpp` | Pointer-to-pointer (`**`) – accessing and modifying a variable through double indirection |
| `task2.cpp` | Modifying a variable through a pointer (`*p += 5`) |
| `task3.cpp` | Array of `const char*` pointers to string literals; runtime replacement |
| `task4.cpp` | Dynamic array of scores using `new`; user input; average calculation |
| `task5.cpp` | Safe pointer deletion and setting pointer to `nullptr` |
| `task6.cpp` | Memory leak demonstration vs. a fixed version using `delete[]` |

---

## 🧠 Concepts Covered

- **Pointer Basics** – Declaring, assigning, and dereferencing pointers
- **Double Pointers (`**`)** – Pointer to a pointer; modifying through two levels of indirection
- **Array of Pointers** – `const char*` arrays pointing to string literals
- **Dynamic Memory Allocation** – `new` / `delete` / `delete[]`
- **Null Safety** – Setting pointers to `nullptr` after deletion
- **Memory Leaks** – What they are, how to cause them, and how to fix them

---

## 🔍 Task Walkthrough

### `task1.cpp` – Double Pointer
```
x: 42
*p: 42
**q: 42
after **q=100, x: 100
```
Demonstrates that modifying `**q` changes the original variable `x`.

### `task2.cpp` – Pointer Arithmetic
```
a before: 20
a after:  25
```
Adds 5 to `a` indirectly through pointer `p`.

### `task3.cpp` – Array of String Pointers
Prints all 5 names, then replaces `"Azeem"` with `"Fatima"` by updating the pointer at index 2.

### `task4.cpp` – Dynamic Score Array
User enters `n` scores; program allocates a heap array, reads values, computes the average, then frees memory.

### `task5.cpp` – Safe Deletion
Allocates a single `int` on the heap, prints it, deletes it, and sets the pointer to `nullptr` to prevent dangling pointer access.

### `task6.cpp` – Memory Leak vs Fix
- `leaky()` – allocates 100 ints but **never** frees them (×10,000 iterations → leak)
- `fixed()` – allocates and immediately `delete[]`s (no leak)

---

## 🚀 How to Compile & Run

```bash
g++ task1.cpp -o task1 && ./task1
g++ task2.cpp -o task2 && ./task2
g++ task3.cpp -o task3 && ./task3
g++ task4.cpp -o task4 && ./task4
g++ task5.cpp -o task5 && ./task5
g++ task6.cpp -o task6 && ./task6
```

---

## 📈 Key Concepts Summary

| Concept | Key Rule |
|---------|----------|
| Pointer dereference | `*p` reads/writes the value at the address stored in `p` |
| Double pointer | `**q` follows two levels of indirection |
| Dynamic allocation | `new T` allocates on heap; must be paired with `delete` |
| Array allocation | `new T[n]` must be freed with `delete[]` (not `delete`) |
| Null safety | Always set pointer to `nullptr` after deletion |

---

## 👤 Author

**Muhammad Asif**
