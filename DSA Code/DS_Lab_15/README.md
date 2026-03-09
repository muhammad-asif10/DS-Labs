# 📚 DS Lab 15 – Binary Search Trees (BST)

### BST Insert, Search, Delete, Traversal & Min/Max Operations in Python

This lab implements a complete **Binary Search Tree (BST)** with all fundamental operations, accompanied by lecture notes and an interactive HTML reference.

---

## 📁 Files

| File | Description |
|------|-------------|
| `DS_LAB15.ipynb` | Full lab notebook — BST implementation, all operations, and test demonstrations |
| `DS_Week15_BST_Lecture_Lab.html` | Lecture notes and lab manual in HTML format |

---

## 🧠 Concepts Covered

### BST Property
For every node `N`:
- All values in the **left subtree** are **less than** `N.data`
- All values in the **right subtree** are **greater than** `N.data`

### Node Structure
```python
class Node:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None
```

### Operations Implemented

| Operation | Description |
|-----------|-------------|
| `insert(value)` | Insert a new value maintaining BST property |
| `search(value)` | Return the node if found, else `None` |
| `find_min()` | Traverse left until no left child remains |
| `find_max()` | Traverse right until no right child remains |
| `count_nodes()` | Recursively count all nodes |
| `inorder()` | Left → Root → Right (produces **sorted** output) |
| `delete(value)` | Remove a node (handles all 3 cases) |

### Delete – Three Cases
1. **Leaf node** – simply remove it
2. **One child** – replace node with its single child
3. **Two children** – replace with **inorder successor** (smallest in right subtree), then delete the successor

---

## 🔍 Sample Output

```
Insert: 50, 30, 70, 20, 40, 60, 80

BST Structure (conceptual):
        50
       /  \
      30   70
     / \   / \
    20  40 60  80

Inorder traversal: 20 30 40 50 60 70 80   ← sorted!
Min: 20    Max: 80
Node count: 7

Delete 30 (two children):
Inorder after delete: 20 40 50 60 70 80
```

---

## 🚀 How to Run

```bash
jupyter notebook DS_LAB15.ipynb
```

To view the lecture notes:
```bash
open DS_Week15_BST_Lecture_Lab.html
```

Python 3.x is required.

---

## 📈 Time Complexity

| Operation | Average Case | Worst Case (Skewed Tree) |
|-----------|-------------|--------------------------|
| Insert | O(log n) | O(n) |
| Search | O(log n) | O(n) |
| Delete | O(log n) | O(n) |
| Find Min/Max | O(log n) | O(n) |
| Inorder Traversal | O(n) | O(n) |

> A **balanced BST** (e.g., AVL Tree, Red-Black Tree) guarantees O(log n) height and avoids the O(n) worst case of a skewed tree.

---

## 📖 Key Concepts

- **Inorder traversal** of a BST always produces a **sorted sequence**
- **BST search** is similar to Binary Search on a sorted array, but without random access
- **Balancing** is critical for maintaining efficient O(log n) operations

---

## 👤 Author

**Muhammad Asif**
