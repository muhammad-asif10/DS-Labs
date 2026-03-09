# 📚 Mini Project – Student Marks Statistics System

### Dynamic Array-Based Student Marks Manager in C++

This mini-project is a C++ console application that reads student marks at runtime, stores them in a **dynamically allocated array**, and computes basic statistics: average, highest, and lowest marks.

---

## 📁 Files

| File | Description |
|------|-------------|
| `SMM.cpp` | Full C++ source — dynamic array allocation, marks input, statistics computation |

---

## 🧠 Concepts Covered

- **Dynamic Memory Allocation** – `new int[n]` for a runtime-sized marks array
- **User Input Loop** – Reading each student's marks using `cin`
- **Aggregate Statistics** – Sum, average, maximum, and minimum
- **Memory Cleanup** – `delete[] marks` to free heap memory after use

---

## 🔍 Program Flow

```
1. Prompt user: "Enter Number of Students"
2. Allocate: int* marks = new int[n]
3. Loop n times: read marks[i] from user
4. Compute: sum, maxMark, minMark
5. Print: Average, Highest, Lowest
6. Free: delete[] marks
```

---

## 🚀 How to Compile & Run

```bash
g++ SMM.cpp -o smm
./smm
```

**Sample Session:**
```
Enter Number of Students: 4
Enter Marks of Students: 1 : 85
Enter Marks of Students: 2 : 92
Enter Marks of Students: 3 : 78
Enter Marks of Students: 4 : 88

Marks Entered: 85 92 78 88
Average = 85.75
Highest = 92
Lowest  = 78
```

---

## 📈 Complexity

| Operation | Time Complexity |
|-----------|----------------|
| Input loop | O(n) |
| Statistics loop | O(n) |
| Overall | O(n) |
| Space | O(n) – dynamic array |

---

## 👤 Author

**Muhammad Asif**
