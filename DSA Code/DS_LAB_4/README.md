# 📚 DS Lab 4 – Stack Applications

### Bracket Checking, Infix-to-Postfix Conversion & Postfix Evaluation in Python

This lab applies the **Stack** data structure to solve real-world expression parsing problems, using Python and Jupyter Notebooks.

---

## 📁 Files

| File | Description |
|------|-------------|
| `DS_Lab_4.ipynb` | Main lab notebook — stack implementation and all tasks |
| `DS_Lab_4_Asif.ipynb` | Personal solution notebook with extended analysis |
| `Operator Precedence.png` | Reference chart showing operator precedence rules |

---

## 🧠 Concepts Covered

### Task 1 – Stack Class
Custom Python `Stack` class built on top of a list with:
- `push(item)` – add to top
- `pop()` – remove from top
- `peek()` – inspect top without removing
- `is_empty()` – check if stack is empty

### Task 2 – Bracket Checker
Validates whether an expression has **balanced parentheses/brackets**:
- Pushes opening brackets `(`, `[`, `{` onto the stack
- Pops and verifies matching closing bracket
- Catches mismatches and unmatched opens/closes

**Examples:**
```
"(a+b)*[c-d]"  → Balanced ✅
"((a+b)"        → Unbalanced ❌
"{[}]"          → Unbalanced ❌
```

### Task 3 – Infix to Postfix Converter
Converts a standard infix expression to postfix (Reverse Polish Notation) using the **Shunting Yard algorithm**:
- Respects operator precedence: `^` > `*` `/` > `+` `-`
- Handles parentheses correctly

**Example:**
```
Infix:   A + B * C
Postfix: A B C * +
```

### Task 4 – Postfix Evaluator
Evaluates a postfix expression using a stack:
- Operands are pushed onto the stack
- On encountering an operator, two operands are popped, the operation applied, and the result pushed back

**Example:**
```
Postfix: 3 4 2 * +
Result:  11
```

### Task 5 – Linear Search
Bonus task demonstrating linear (sequential) search through a list.

---

## 🚀 How to Run

Open the notebooks in **Jupyter Notebook** or **VS Code**:

```bash
jupyter notebook DS_Lab_4.ipynb
```

Or run interactively in any Python environment (Python 3.x required).

---

## 📈 Time Complexity

| Algorithm | Time Complexity |
|-----------|----------------|
| Bracket Checker | O(n) |
| Infix → Postfix | O(n) |
| Postfix Evaluation | O(n) |

---

## 📖 Reference

See `Operator Precedence.png` for the precedence table used when parsing infix expressions.

---

## 👤 Author

**Muhammad Asif**
