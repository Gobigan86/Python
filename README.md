# 🐍 Python Fundamentals: Operators and Control Flow

A concise, well-structured reference covering the essential building blocks of Python programming—**syntax, data types, operators, and conditional logic**—to help you write robust and readable code from day one.

---

## 💡 Core Python Foundations

This guide outlines the foundational concepts necessary to write any functional Python script, with a focus on clarity, correctness, and best practices.

---

## ✨ 1. Syntax, Comments, and Variables

| Concept     | Description                                  | Example                     |
|-----------|----------------------------------------------|-----------------------------|
| **Syntax**  | Basic executable statement.                  | `print('Hello')`            |
| **Comments**| Notes ignored by the interpreter.            | `# This is a comment`       |
| **Variables**| Named storage for values (case-sensitive).   | `name = "Alice"`            |

> 🔹 Python uses **dynamic typing**: variable types are inferred at runtime.

---

## ✨ 2. Data Types and Typecasting

All user input is initially a **string** (`str`) and often requires explicit conversion for other uses.

| Type Category | Python Type          | Description                        | Casting Function |
|---------------|----------------------|------------------------------------|------------------|
| **Text**      | `str`                | Sequence of characters             | `str()`          |
| **Numeric**   | `int`, `float`       | Whole numbers and decimals         | `int()`, `float()`|
| **Sequence**  | `list`, `tuple`      | Ordered, mutable/immutable collections | `list()`, `tuple()` |
| **Mapping**   | `dict`               | Key-value pairs                    | `dict()`         |
| **Boolean**   | `bool`               | `True` or `False`                  | `bool()`         |

> 🔹 **Always typecast user input** (e.g., `age = int(input("Age: "))`) before performing arithmetic.

---

## 📊 Summary of All Operator Types

Operators are symbols or keywords that perform operations on values and variables.

---

### 🔢 1. Arithmetic Operators (Math)

| Operator | Name              | Purpose                                 | Example (`x=10, y=3`) | Result     |
|--------|-------------------|-----------------------------------------|------------------------|------------|
| `+`    | Addition          | Sum of operands                         | `x + y`                | `13`       |
| `/`    | Division          | Floating-point result                   | `x / y`                | `3.333...` |
| `//`   | Floor Division    | Integer part of quotient                | `x // y`               | `3`        |
| `%`    | Modulus           | Remainder of division                   | `x % y`                | `1`        |
| `**`   | Exponentiation    | Left raised to power of right           | `x ** 2`               | `100`      |

---

### 🔍 2. Comparison & Logical Operators

These return **Boolean** values (`True`/`False`) and drive control flow.

#### Comparison (Relational) Operators

| Operator | Name             | Condition                          | Example (`x=10, y=20`) | Result |
|--------|------------------|------------------------------------|-------------------------|--------|
| `==`   | Equal To         | True if values are equal           | `x == y`                | `False`|
| `!=`   | Not Equal To     | True if values differ              | `x != y`                | `True` |
| `>`    | Greater Than     | True if left > right               | `x > y`                 | `False`|
| `<=`   | Less Than or Eq. | True if left ≤ right               | `y <= 15`               | `False`|

#### Logical (Boolean) Operators

| Operator | Description                              | Example (`a=True, b=False`) | Result |
|--------|------------------------------------------|------------------------------|--------|
| `and`  | True if **both** operands are `True`     | `a and b`                    | `False`|
| `or`   | True if **at least one** is `True`       | `a or b`                     | `True` |
| `not`  | Reverses the Boolean value               | `not a`                      | `False`|

---

### 🎯 3. Specialized Operators

| Operator Type | Operator     | Purpose                                      | Key Distinction |
|---------------|--------------|----------------------------------------------|-----------------|
| **Identity**  | `is`, `is not` | Checks if two variables refer to the **same object in memory** | Compares **identity**, not value |
| **Membership**| `in`, `not in`| Checks if a value exists in a sequence (e.g., list, string) | Essential for iteration & validation |

> Example:  
> ```python
> a = [1, 2]; b = a
> print(a is b)  # True (same object)
> print(2 in a)  # True (2 is in the list)
> ```

---

## ⚙️ Control Flow: Conditional Statements

Conditional logic (`if`/`elif`/`else`) uses **Boolean expressions** to determine program execution paths.

### The `if`/`elif`/`else` Structure

Python uses **indentation (4 spaces)**—not braces—to define code blocks.

```python
score = 85

if score >= 90:
    print("A Grade")
elif score >= 80:
    print("B Grade")  # ✅ This block executes
else:
    print("Lower Grade")
