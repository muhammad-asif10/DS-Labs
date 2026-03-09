# 📚 Hashing – Hash Table with Chaining

### Hash Table Implementation Using Separate Chaining for Collision Resolution in Python

This module implements a **Hash Table** that handles collisions using the **Separate Chaining** technique, where each bucket holds a linked list of entries that hash to the same index.

---

## 📁 Files

| File | Description |
|------|-------------|
| `Chaning.py` | Full implementation of a hash table with separate chaining — insert, search, and delete |

---

## 🧠 Concepts Covered

### Hash Function
Converts a string key into a table index:
```python
def hash_function(self, key):
    total = 0
    for ch in key:
        total += ord(ch)    # sum of ASCII values
    return total % self.size
```

### Separate Chaining (Collision Resolution)
- Each slot in the table holds a **linked list** of `Node` objects
- When two keys hash to the same index, the new node is **prepended** to the chain
- Lookup and deletion scan the chain at the target index

### Node Structure
```python
class Node:
    def __init__(self, key, value):
        self.key = key
        self.value = value
        self.next = None
```

### Operations

| Method | Description |
|--------|-------------|
| `insert(key, value)` | Hash the key and prepend a new node at the computed index |
| `search(key)` | Hash the key, traverse the chain, return `value` or `None` |
| `delete(key)` | Hash the key, find the node in the chain, and unlink it |

---

## 🔍 Example Usage

```python
ht = HashTableChaining(size=10)
ht.insert("name", "Alice")
ht.insert("age", "22")
ht.insert("city", "Lahore")

print(ht.search("name"))   # → "Alice"
print(ht.search("age"))    # → "22"

ht.delete("age")
print(ht.search("age"))    # → None
```

**Sample insert output:**
```
Inserted 'name' at index 3
Inserted 'age' at index 7
Inserted 'city' at index 2
```

---

## 🔄 How Collision Chaining Works

```
Index 5 → [Node("apple","red")] → [Node("mango","yellow")] → None
          ↑ both hashed to index 5; chained as a linked list
```

---

## 🚀 How to Run

```bash
python Chaning.py
```

Python 3.x is required.

---

## 📈 Time Complexity

| Operation | Average Case | Worst Case (all keys in one chain) |
|-----------|-------------|-------------------------------------|
| Insert | O(1) | O(n) |
| Search | O(1 + α) | O(n) |
| Delete | O(1 + α) | O(n) |

Where **α = n / m** is the **load factor** (n = number of entries, m = table size).

> Keeping α ≤ 1 (resizing the table when needed) maintains O(1) average performance.

---

## 📖 Key Concepts

- **Hash collision** – Two different keys mapping to the same index
- **Separate chaining** – Each bucket is a linked list; collisions are chained
- **Open addressing** – An alternative where collisions are resolved by probing for the next empty slot
- **Load factor** – Ratio of entries to buckets; high load → more collisions

---

## 👤 Author

**Muhammad Asif**
