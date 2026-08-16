# 🟢 Level 1 — Beginner

> 🌐 Language: **English** | [فارسی](fa/README.md)

Welcome to the **Beginner** level of the Python Roadmap.

This level is designed for learners who have little or no programming experience. Here, you will build the fundamental knowledge required to write Python programs confidently.

Unlike the previous level, which focused on **problem-solving and algorithmic thinking**, this level introduces the Python language itself.

By the end of this level, you will be able to write, read, and understand Python programs while applying good programming practices from the very beginning.

---

# 📚 What You'll Learn

During this level, you will learn:

- Python basics
- Variables
- Data types
- User input
- Operators
- Conditional statements
- Loops
- Functions
- Strings
- Lists
- Tuples
- Sets
- Dictionaries

Each lesson builds upon the previous one, so it is highly recommended to complete them in order.

---

# 🎯 Learning Goals

After completing this level, you will be able to:

- Understand Python syntax.
- Write simple Python programs.
- Make decisions using conditions.
- Repeat tasks using loops.
- Organize code with functions.
- Work with Python's built-in data structures.
- Read and understand beginner-level Python code.
- Solve basic programming problems confidently.

---

# 📋 Prerequisites

Before starting this level, you should complete:

- ✅ Level 0 — Problem Solving

Although it is technically possible to skip it, completing the previous level will make learning Python significantly easier.

---

# 🗂️ Lessons

| # | Lesson | Status |
|---|--------|--------|
| 1 | Python Basics | ⏳ |
| 2 | Variables & Data Types | ⏳ |
| 3 | User Input & Output | ⏳ |
| 4 | Operators | ⏳ |
| 5 | Conditional Statements | ⏳ |
| 6 | Loops | ⏳ |
| 7 | Functions | ⏳ |
| 8 | Strings | ⏳ |
| 9 | Lists | ⏳ |
| 10 | Tuples | ⏳ |
| 11 | Sets | ⏳ |
| 12 | Dictionaries | ⏳ |

---

# 💡 How to Study

To get the most out of this level:

- Study one lesson at a time.
- Read the explanations carefully.
- Run every code example yourself.
- Complete all exercises.
- Don't skip the quizzes.
- Practice regularly.

Programming is a practical skill.

The more you practice, the faster you improve.

---

# 📈 Progress

Current Progress:

```text
□□□□□□□□□□□□
0%
```

Lessons Completed:

**0 / 12**

---

# 🚀 What's Next?

After completing this level, you'll move on to:

> 🟡 **Level 2 — Intermediate**

There, you'll learn more advanced Python concepts, improve your coding skills, and begin building larger and more practical applications.

---

Happy coding! 🐍

---

# Part 9 — Dictionary Keys and Values

## Introduction

A Dictionary stores data as **Key-Value pairs**.

Understanding the difference between Keys and Values is essential because almost every Dictionary operation is based on this relationship.

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

Here:

* `"name"`, `"age"`, and `"score"` are **Keys**.
* `"Ali"`, `20`, and `18` are **Values**.

We can visualize the Dictionary as:

```text
Key       → Value
"name"    → "Ali"
"age"     → 20
"score"   → 18
```

The **Key identifies the data**, while the **Value contains the data** associated with that Key.

---

## 1. Dictionary Keys

A Key is the identifier used to access a Value.

```python
student = {
    "name": "Ali",
    "age": 20
}

print(student["name"])
```

Output:

```text
Ali
```

Here, `"name"` is the Key and `"Ali"` is its associated Value.

The Key tells Python **which Value we want to retrieve**.

---

## 2. Dictionary Values

A Value is the actual data stored under a Key.

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

The Values are:

```text
Ali
20
18
```

Values can have different data types:

```python
data = {
    "name": "Ali",
    "age": 20,
    "active": True
}
```

Here:

* `"Ali"` is a String.
* `20` is an Integer.
* `True` is a Boolean.

A Dictionary does not require all Values to have the same type.

---

## 3. Accessing a Value Through Its Key

The most common operation between a Key and a Value is:

```python
dictionary[key]
```

For example:

```python
student = {
    "name": "Ali",
    "age": 20
}

print(student["age"])
```

Output:

```text
20
```

We provide the Key, and Python returns the Value associated with it.

---

## 4. Keys Must Be Unique

Dictionary Keys must be unique.

For example:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

There is only one `"name"` Key.

If the same Key is written more than once:

```python
student = {
    "name": "Ali",
    "name": "Sara"
}
```

Python does not keep two separate `"name"` entries.

The later entry replaces the earlier one.

The resulting Dictionary behaves as:

```python
{
    "name": "Sara"
}
```

Therefore:

> **A Dictionary cannot contain two distinct entries with the same Key.**

---

## 5. Values Can Be Repeated

Values do not have to be unique.

```python
scores = {
    "Ali": 18,
    "Sara": 18,
    "Reza": 15
}
```

Both `"Ali"` and `"Sara"` have the Value `18`.

This is completely valid.

The important distinction is:

```text
Keys   → unique
Values → may repeat
```

---

## 6. Getting All Keys with `keys()`

Python provides the `keys()` method:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

print(student.keys())
```

The result is a view containing the Dictionary's Keys.

We can iterate through it:

```python
for key in student.keys():
    print(key)
```

Output:

```text
name
age
score
```

Use `keys()` when the Keys themselves are what we need to work with.

---

## 7. Getting All Values with `values()`

The `values()` method provides access to the Values:

```python
for value in student.values():
    print(value)
```

Output:

```text
Ali
20
18
```

This is useful when the Keys are not relevant to the operation.

---

## 8. Getting Keys and Values Together with `items()`

When we need both parts of every Dictionary entry, we can use `items()`:

```python
for key, value in student.items():
    print(key, value)
```

Output:

```text
name Ali
age 20
score 18
```

Conceptually, each iteration gives us:

```text
(Key, Value)
```

For example:

```text
"name" → "Ali"
"age" → 20
"score" → 18
```

This is one of the most important Dictionary patterns.

---

## 9. Checking Whether a Key Exists

The `in` operator checks Dictionary Keys:

```python
student = {
    "name": "Ali",
    "age": 20
}

print("name" in student)
print("score" in student)
```

Output:

```text
True
False
```

Because `"name"` exists as a Key while `"score"` does not.

---

## 10. Checking Whether a Value Exists

To search Values, use `values()`:

```python
student = {
    "name": "Ali",
    "age": 20
}

print(20 in student.values())
```

Output:

```text
True
```

Compare:

```python
"age" in student
```

with:

```python
20 in student.values()
```

The first checks a **Key**.

The second checks a **Value**.

This distinction is fundamental when working with Dictionaries.

---

## 11. Keys and Values Have Different Roles

Consider:

```python
products = {
    "apple": 10,
    "banana": 5,
    "orange": 8
}
```

Here, the Keys identify products:

```text
apple
banana
orange
```

The Values represent quantities:

```text
10
5
8
```

We could use exactly the same Dictionary structure for prices:

```python
prices = {
    "apple": 2,
    "banana": 1,
    "orange": 3
}
```

The structure remains the same, but the meaning of the Values changes.

This illustrates an important programming idea:

> **A Dictionary provides the structure; the programmer defines what the Keys and Values represent.**

---

## 12. Choosing Meaningful Keys

Keys should clearly describe the data they identify.

For example:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

is easier to understand than:

```python
student = {
    "a": "Ali",
    "b": 20,
    "c": 18
}
```

Both are technically possible, but meaningful Keys make code easier to read, understand, and maintain.

A good Key gives us useful information about the Value it identifies.

---

## 13. Lookup vs. Search

There is an important difference between **looking up a Value using a Key** and **searching for a Value**.

### Lookup

```python
student["age"]
```

We already know the Key and want its Value.

Conceptually:

```text
Key → Value
```

### Value Search

```python
20 in student.values()
```

We know a Value and want to know whether it exists.

Conceptually:

```text
Value → Does it exist?
```

These are different operations and should not be confused.

---

## 14. Finding Keys Based on Their Values

Suppose:

```python
scores = {
    "Ali": 18,
    "Sara": 15,
    "Reza": 18
}
```

We want to find all students whose score is `18`.

We can examine Key-Value pairs:

```python
for name, score in scores.items():
    if score == 18:
        print(name)
```

Output:

```text
Ali
Reza
```

Notice that one Value can correspond to multiple Keys.

This is possible because Values do not need to be unique.

---

## 15. Values Can Contain Different Data Structures

Dictionary Values can be more complex than simple numbers or strings.

For example:

```python
student = {
    "name": "Ali",
    "age": 20,
    "skills": ["Python", "HTML"],
    "active": True
}
```

Here:

* `"name"` → String
* `"age"` → Integer
* `"skills"` → List
* `"active"` → Boolean

We can access the List through its Key:

```python
print(student["skills"])
```

Output:

```text
['Python', 'HTML']
```

Because the resulting Value is a List, we can then use List operations:

```python
print(student["skills"][0])
```

Output:

```text
Python
```

The Dictionary determines **which Value** we retrieve; the Value's own data type determines what we can do with it afterward.

---

## 16. Keys Are Part of the Data Model

A Key is not merely a label displayed to the user.

It plays an operational role in the program.

For example:

```python
user = {
    "username": "ali123",
    "email": "ali@example.com"
}
```

We can write:

```python
user["email"]
```

to retrieve the email.

Therefore, `"email"` is part of the way the program organizes and accesses the user's data.

Good Key names make later code much easier to understand.

---

## 17. A Practical Example

Consider a small inventory:

```python
inventory = {
    "apple": 10,
    "banana": 5,
    "orange": 8
}
```

If we know the product name, we can directly retrieve its quantity:

```python
print(inventory["apple"])
```

Output:

```text
10
```

If we want all product names:

```python
for product in inventory.keys():
    print(product)
```

If we want all quantities:

```python
for quantity in inventory.values():
    print(quantity)
```

If we want both:

```python
for product, quantity in inventory.items():
    print(f"{product}: {quantity}")
```

Output:

```text
apple: 10
banana: 5
orange: 8
```

These three methods provide the basic ways to work with the two sides of a Dictionary.

---

## 18. Complete Mental Model

A Dictionary can be understood as a collection of relationships:

```text
             Dictionary
                 │
        ┌────────┴────────┐
        ↓                 ↓
      Keys             Values
        │                 │
   identify data      store data
        │                 │
        └───────┬─────────┘
                ↓
          Key → Value
```

For:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

we have:

```text
"name"  → "Ali"
"age"   → 20
"score" → 18
```

Once this relationship is clear, `keys()`, `values()`, and `items()` become much easier to understand.

---

## Key Takeaways

* A Dictionary consists of **Key-Value pairs**.
* A Key identifies a piece of data.
* A Value contains the data associated with a Key.
* Keys must be unique.
* Values can be repeated.
* `keys()` provides access to Keys.
* `values()` provides access to Values.
* `items()` provides Key-Value pairs.
* `in` used directly on a Dictionary checks Keys.
* `in dictionary.values()` checks Values.
* Meaningful Keys make programs easier to understand.
* Values can contain different data types, including Lists.
* Looking up a Value by Key is different from searching for a Value.
* Finding Keys based on Values generally requires examining Key-Value pairs.

---

# Section Questions

## Question 1

Identify all Keys and all Values in:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

## Question 2

What is the difference between:

```python
"age" in student
```

and:

```python
20 in student.values()
```

## Question 3

What will the resulting Dictionary contain?

```python
student = {
    "name": "Ali",
    "name": "Sara"
}
```

---

# Comprehensive Question

Given:

```python
students = {
    "Ali": 18,
    "Sara": 15,
    "Reza": 18,
    "Mina": 12
}
```

Write a program that:

1. Prints all Keys.
2. Prints all Values.
3. Prints every Key-Value pair.
4. Checks whether the Value `18` exists.
5. Finds and prints all Keys whose Value is `18`.

---

# Answers

## Answer 1

Keys:

```text
name
age
score
```

Values:

```text
Ali
20
18
```

## Answer 2

```python
"age" in student
```

checks whether `"age"` exists as a **Key**.

```python
20 in student.values()
```

checks whether `20` exists as a **Value**.

## Answer 3

The later `"name"` entry replaces the earlier one:

```python
{
    "name": "Sara"
}
```

## Comprehensive Answer

```python
students = {
    "Ali": 18,
    "Sara": 15,
    "Reza": 18,
    "Mina": 12
}

for key in students.keys():
    print(key)

for value in students.values():
    print(value)

for key, value in students.items():
    print(f"{key}: {value}")

if 18 in students.values():
    print("18 exists.")

for key, value in students.items():
    if value == 18:
        print(key)
```

The final search prints:

```text
Ali
Reza
```

---

