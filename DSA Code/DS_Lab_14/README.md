# 📚 DS Lab 14 – Sorting Algorithms

### Selection Sort, Insertion Sort, Merge Sort & Heap Sort with Visual Step-by-Step Diagrams

This lab provides a comprehensive study of **comparison-based sorting algorithms**, covering their mechanics, implementation, stability, and performance, with SVG step-by-step diagrams.

---

## 📁 Files

| File | Description |
|------|-------------|
| `DS_Week14_Sorting_UVAS_Lab.html` | Full interactive HTML document — lecture notes, code examples, SVG diagrams, and lab tasks |

---

## 🧠 Concepts Covered

### Lecture 1 – Selection Sort
- Repeatedly finds the **minimum element** from the unsorted portion and swaps it into place
- Simple but not adaptive (always O(n²) regardless of input order)
- **In-place**, **not stable**

**Pseudocode:**
```
for i from 0 to n-1:
    min_idx = i
    for j from i+1 to n:
        if A[j] < A[min_idx]: min_idx = j
    swap(A[i], A[min_idx])
```

### Lecture 2 – Insertion Sort
- Builds the sorted portion one element at a time by **inserting** each new element into its correct position
- **Adaptive** (fast on nearly sorted data), **stable**

**Pseudocode:**
```
for i from 1 to n-1:
    key = A[i]
    j = i - 1
    while j >= 0 and A[j] > key:
        A[j+1] = A[j]
        j -= 1
    A[j+1] = key
```

### Lecture 3 – Merge Sort
- **Divide and Conquer**: recursively splits the array in half, sorts each half, then merges
- **Stable**, **not in-place** (requires O(n) extra space)
- Consistent O(n log n) performance

### Heap Sort
- Builds a **Max Heap** from the array, then repeatedly extracts the maximum
- **In-place**, **not stable**, O(n log n)
- Uses `heapify` to maintain the heap property

---

## 🔍 Algorithm Comparison Table

| Algorithm | Best Case | Average Case | Worst Case | Space | Stable |
|-----------|-----------|--------------|------------|-------|--------|
| Selection Sort | O(n²) | O(n²) | O(n²) | O(1) | ❌ |
| Insertion Sort | O(n) | O(n²) | O(n²) | O(1) | ✅ |
| Merge Sort | O(n log n) | O(n log n) | O(n log n) | O(n) | ✅ |
| Heap Sort | O(n log n) | O(n log n) | O(n log n) | O(1) | ❌ |

---

## 🖥️ How to View

Open the HTML file in any web browser:

```bash
open DS_Week14_Sorting_UVAS_Lab.html
# or
xdg-open DS_Week14_Sorting_UVAS_Lab.html
```

The file contains:
- **Interactive SVG diagrams** showing each sort step-by-step
- **Code examples** with comparison counters
- **Mini lab tasks** with evaluation criteria

---

## 📖 Key Concepts

- **Stability** – A sorting algorithm is stable if equal elements maintain their relative order
- **In-place** – Requires O(1) extra space (no auxiliary array)
- **Adaptive** – Performs better on partially sorted input (Insertion Sort is adaptive)
- **Divide and Conquer** – Merge Sort's approach: split → sort → merge

---

## 👤 Author

**Muhammad Asif**
