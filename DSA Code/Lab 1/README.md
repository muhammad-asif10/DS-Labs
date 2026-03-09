# 📚 Lab 1 – Arrays: Basics, Insertion & Deletion

### Static Arrays, Dynamic Arrays, and Core Array Operations in C++

This lab introduces **fundamental array operations** in C++, covering static arrays, dynamic memory allocation, element insertion, and deletion.

---

## 📁 Files

| File | Description |
|------|-------------|
| `Part1.cpp` | Hello World – lab environment verification |
| `Static_Array.cpp` | Static array declaration and traversal |
| `Array_input.cpp` | Dynamic array allocation with user-defined size |
| `Inserted_Array.cpp` | Inserting an element at the end of an array |
| `Array_Delete.cpp` | Deleting an element at a specific position |

---

## 🧠 Concepts Covered

- **Static Arrays** – Stack-allocated fixed-size arrays
- **Dynamic Arrays** – Heap-allocated arrays using `new` and `delete[]`
- **Array Insertion** – Appending a new element and updating the logical size
- **Array Deletion** – Removing an element by shifting subsequent elements left
- **Memory Management** – Proper deallocation with `delete[]`

---

## 🔍 Example Walkthrough

### `Static_Array.cpp`
Declares `int x[6]`, fills each position with `2*j`, and prints: `0 2 4 6 8 10`.

### `Array_input.cpp`
Prompts the user for array size, allocates memory dynamically, fills with multiples of 5, prints the array, and frees memory.

### `Inserted_Array.cpp`
Starts with a 5-element array and appends the value `99` at index `n`, incrementing the logical size.

**Before:** `0 2 4 6 8`  
**After insertion:** `0 2 4 6 8 99`

### `Array_Delete.cpp`
Deletes the element at index `pos = 2` by shifting all elements after it one position to the left, then decrementing size.

**Before:** `10 20 30 40 50 60`  
**After deletion at index 2:** `10 20 40 50 60`

---

## 🚀 How to Compile & Run

```bash
g++ Part1.cpp -o part1 && ./part1
g++ Static_Array.cpp -o static_arr && ./static_arr
g++ Array_input.cpp -o arr_input && ./arr_input
g++ Inserted_Array.cpp -o insert && ./insert
g++ Array_Delete.cpp -o delete_arr && ./delete_arr
```

---

## 📈 Time Complexity

| Operation | Complexity |
|-----------|------------|
| Access by index | O(1) |
| Insertion at end | O(1) |
| Deletion at position `i` | O(n) – requires shifting |
| Array traversal | O(n) |

---

## 👤 Author

**Muhammad Asif**
