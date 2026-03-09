# 📚 DS Lab 10 – Searching Algorithms (Extended)

### Sequential Search & Binary Search with Step Counting & Performance Analysis in Python

This lab provides an in-depth study of **searching algorithms**, building on Lab 9 with extended experiments, larger datasets, and detailed complexity discussion.

---

## 📁 Files

| File | Description |
|------|-------------|
| `DS_Lab_9.ipynb` | Lab notebook with sequential and binary search implementations, step-count experiments, and analysis |

---

## 🧠 Concepts Covered

### Sequential Search (Linear Search)
Iterates through each element of the list from the beginning:
- No preprocessing required — works on **unsorted** data
- Returns the index of the found element or signals "not found"
- Step counter incremented for every comparison

### Binary Search
Efficient search on a **sorted** list using divide-and-conquer:
- Compares target to the midpoint element
- Eliminates half of the remaining search space each iteration
- Step counter shows the logarithmic growth

### Step-Count Comparison
Both algorithms are instrumented with counters to directly measure the number of comparisons performed per search, making the O(n) vs O(log n) difference concrete and observable.

### Large-Scale Experiment
Runs searches on a list of **100,000 elements** to demonstrate:
- Sequential search may require up to 100,000 comparisons
- Binary search requires at most 17 comparisons on the same list

---

## 🔍 Algorithm Comparison

| Property | Sequential Search | Binary Search |
|----------|------------------|---------------|
| Prerequisite | None | List must be sorted |
| Best Case | O(1) – element at index 0 | O(1) – element at midpoint |
| Worst Case | O(n) – element at end or absent | O(log n) |
| Average Case | O(n/2) ≈ O(n) | O(log n) |
| Data requirement | Any | Sorted only |

---

## 🚀 How to Run

```bash
jupyter notebook DS_Lab_9.ipynb
```

Python 3.x is required.

---

## 📈 Practical Performance (Steps Comparison)

```
List size: 100,000
Target: last element

Sequential Search steps: 100,000
Binary Search steps:          17
```

---

## 📖 Key Takeaways

- **Binary Search is dramatically faster** for large sorted datasets
- **Sequential Search** is appropriate when data is unsorted or the list is small
- The cost of **sorting** (O(n log n)) is worth it when many searches will be performed
- Step counting is a practical way to verify theoretical time complexity

---

## 👤 Author

**Muhammad Asif**
