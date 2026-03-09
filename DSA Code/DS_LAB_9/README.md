# 📚 DS Lab 9 – Searching Algorithms

### Sequential Search & Binary Search with Complexity Analysis in Python

This lab implements and compares two fundamental **searching algorithms** — Sequential (Linear) Search and Binary Search — with step counting and performance analysis.

---

## 📁 Files

| File | Description |
|------|-------------|
| `DS_Lab_9.ipynb` | Complete lab notebook with implementations, experiments, and analysis |

---

## 🧠 Concepts Covered

### Sequential Search (Linear Search)
Scans through the list one element at a time until the target is found or the list is exhausted:
- Works on **unsorted** or sorted lists
- Returns the index of the target or `-1` if not found
- Counts comparisons to measure performance

**Algorithm:**
```python
for i in range(len(data)):
    if data[i] == target:
        return i
return -1
```

### Binary Search
Exploits a **sorted** list by repeatedly halving the search space:
- Compare the target with the middle element
- If equal → found; if less → search left half; if greater → search right half
- Counts comparisons at each step

**Algorithm:**
```python
low, high = 0, len(data) - 1
while low <= high:
    mid = (low + high) // 2
    if data[mid] == target: return mid
    elif data[mid] < target: low = mid + 1
    else: high = mid - 1
return -1
```

### Comparison Analysis
- Runs both algorithms on the same datasets
- Records the number of comparisons (steps) for each search
- Demonstrates O(n) vs O(log n) growth through experiments

### Large List Experiment
Tests both algorithms on a list of **100,000 elements** to make the performance gap clearly visible.

---

## 🔍 Example Results

| List Size | Sequential (worst) | Binary (worst) |
|-----------|-------------------|----------------|
| 10 | 10 comparisons | 4 comparisons |
| 100 | 100 comparisons | 7 comparisons |
| 1,000 | 1,000 comparisons | 10 comparisons |
| 100,000 | 100,000 comparisons | 17 comparisons |

---

## 🚀 How to Run

```bash
jupyter notebook DS_Lab_9.ipynb
```

Python 3.x is required.

---

## 📈 Time Complexity

| Algorithm | Best Case | Average Case | Worst Case | Requires Sorted? |
|-----------|-----------|--------------|------------|-----------------|
| Sequential Search | O(1) | O(n) | O(n) | No |
| Binary Search | O(1) | O(log n) | O(log n) | **Yes** |

---

## 📖 Short Answer Questions

1. **Why does Binary Search require a sorted list?**  
   It relies on comparing the target with the midpoint to discard half the remaining elements. Without sorted order, the direction of the next search would be undefined.

2. **When should you prefer Sequential over Binary Search?**  
   When the list is unsorted (or small), and the cost of sorting would exceed the savings from faster searching.

---

## 👤 Author

**Muhammad Asif**
