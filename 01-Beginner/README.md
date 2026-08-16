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

# Part 10 — Dictionary Items

## Introduction

In the previous part, we learned that a Dictionary is made of **Key-Value pairs**.

For example:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

Each entry contains two related pieces of information:

```text
"name"  → "Ali"
"age"   → 20
"score" → 18
```

Sometimes we need only the Keys.

Sometimes we need only the Values.

But very often, we need **both the Key and its Value together**.

This is where the `items()` method becomes important.

---

## 1. What Does `items()` Do?

The `items()` method gives us access to all **Key-Value pairs** in a Dictionary.

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

print(student.items())
```

The result represents the Dictionary entries as pairs:

```text
("name", "Ali")
("age", 20)
("score", 18)
```

Conceptually:

```text
Dictionary
    ↓
items()
    ↓
(Key, Value)
(Key, Value)
(Key, Value)
```

So the purpose of `items()` is:

> **To work with each Key and its corresponding Value together.**

---

## 2. `items()` Returns Pairs

Each element produced by `items()` represents one Key-Value pair.

For example:

```python
student = {
    "name": "Ali",
    "age": 20
}

for item in student.items():
    print(item)
```

Output:

```text
('name', 'Ali')
('age', 20)
```

Each `item` represents one complete Dictionary entry.

This is different from:

```python
student.keys()
```

which gives Keys, and:

```python
student.values()
```

which gives Values.

We can think of the three methods as:

```text
keys()   → Keys
values() → Values
items()  → Keys + Values
```

---

## 3. Iterating Through `items()`

The most common use of `items()` is with a `for` loop.

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

for item in student.items():
    print(item)
```

Output:

```text
('name', 'Ali')
('age', 20)
('score', 18)
```

This gives us every Dictionary entry one by one.

The loop does not give us the entire Dictionary at once. Instead, it processes each Key-Value pair separately.

---

## 4. Unpacking Key and Value

Python allows us to unpack each pair directly into two variables:

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

Here:

```text
key   → Key
value → Value
```

For the first iteration:

```text
key   = "name"
value = "Ali"
```

For the second:

```text
key   = "age"
value = 20
```

And so on.

This pattern is extremely common in Python:

```python
for key, value in dictionary.items():
    ...
```

It is one of the main patterns you should become comfortable reading.

---

## 5. Why `items()` Is Useful

Suppose we want to print the name of each student together with their score:

```python
scores = {
    "Ali": 18,
    "Sara": 15,
    "Reza": 19
}
```

We need both parts:

```text
Student → Score
```

So:

```python
for name, score in scores.items():
    print(name, score)
```

Output:

```text
Ali 18
Sara 15
Reza 19
```

Using `items()` makes the relationship between the two pieces of information explicit.

---

## 6. Using `items()` to Create Formatted Output

We can combine `items()` with f-strings:

```python
scores = {
    "Ali": 18,
    "Sara": 15,
    "Reza": 19
}

for name, score in scores.items():
    print(f"{name}: {score}")
```

Output:

```text
Ali: 18
Sara: 15
Reza: 19
```

This is useful when displaying Dictionary data in a readable format.

---

## 7. Using `items()` with Conditions

Because we have both the Key and Value, we can make decisions based on either one.

For example:

```python
scores = {
    "Ali": 18,
    "Sara": 12,
    "Reza": 19,
    "Mina": 10
}

for name, score in scores.items():
    if score >= 15:
        print(name)
```

Output:

```text
Ali
Reza
```

Here the Value controls the condition:

```python
score >= 15
```

while the Key is printed.

This pattern is very useful when processing structured data.

---

## 8. Using Both Key and Value in a Condition

We can also use both:

```python
students = {
    "Ali": 18,
    "Sara": 12,
    "Reza": 19
}

for name, score in students.items():
    if name == "Ali" and score >= 15:
        print(f"{name} passed.")
```

Output:

```text
Ali passed.
```

The important point is that `items()` gives us both pieces of information at the same time, allowing the condition to use either or both.

---

## 9. `items()` vs `keys()` vs `values()`

These methods serve different purposes.

Given:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

### `keys()`

```python
for key in student.keys():
    print(key)
```

Gives:

```text
name
age
score
```

### `values()`

```python
for value in student.values():
    print(value)
```

Gives:

```text
Ali
20
18
```

### `items()`

```python
for key, value in student.items():
    print(key, value)
```

Gives:

```text
name Ali
age 20
score 18
```

The mental model is:

```text
keys()   → What identifies the data?
values() → What data is stored?
items()  → Which data belongs to which identifier?
```

---

## 10. A Dictionary Entry as a Relationship

One of the most important ideas behind `items()` is that a Dictionary is not simply a collection of unrelated values.

It represents **relationships**.

For example:

```python
prices = {
    "apple": 2,
    "banana": 1,
    "orange": 3
}
```

The important information is not only:

```text
2
1
3
```

It is:

```text
apple  → 2
banana → 1
orange → 3
```

`items()` allows us to process these relationships directly.

This becomes increasingly important as Dictionaries become more complex.

---

## 11. Changing the Value While Iterating

We can use a Key obtained from `items()` to modify the Dictionary.

For example:

```python
scores = {
    "Ali": 10,
    "Sara": 12,
    "Reza": 15
}

for name, score in scores.items():
    scores[name] = score + 1

print(scores)
```

Result:

```text
{'Ali': 11, 'Sara': 13, 'Reza': 16}
```

Here:

```python
scores[name]
```

uses the Key to access the corresponding entry.

The Value is then replaced with an updated Value.

This shows an important relationship:

```text
Key
 ↓
Dictionary entry
 ↓
Value
```

---

## 12. Building a New Dictionary from `items()`

We can also use `items()` to create another Dictionary.

For example:

```python
prices = {
    "apple": 2,
    "banana": 1,
    "orange": 3
}

expensive = {}

for product, price in prices.items():
    if price >= 2:
        expensive[product] = price
```

The new Dictionary becomes:

```python
{
    "apple": 2,
    "orange": 3
}
```

The Key and Value are kept together when the condition is satisfied.

---

## 13. Using `items()` with Different Value Types

The Value does not have to be a simple number.

For example:

```python
users = {
    "Ali": 20,
    "Sara": 25,
    "Reza": 22
}
```

works naturally with:

```python
for name, age in users.items():
    print(f"{name} is {age} years old.")
```

But Values can also be Lists:

```python
skills = {
    "Ali": ["Python", "HTML"],
    "Sara": ["CSS", "JavaScript"]
}
```

We can still use:

```python
for name, user_skills in skills.items():
    print(name, user_skills)
```

Output:

```text
Ali ['Python', 'HTML']
Sara ['CSS', 'JavaScript']
```

The Key-Value relationship remains the same even when the Value itself is more complex.

---

## 14. Nested Processing

Because Values can contain other data structures, `items()` can be combined with additional operations.

For example:

```python
skills = {
    "Ali": ["Python", "HTML"],
    "Sara": ["CSS", "JavaScript"]
}

for name, user_skills in skills.items():
    print(name)

    for skill in user_skills:
        print(skill)
```

Output:

```text
Ali
Python
HTML
Sara
CSS
JavaScript
```

The outer loop works with Dictionary Key-Value pairs.

The inner loop works with the List stored as the Value.

This demonstrates how different data structures can work together.

---

## 15. Using `items()` to Search for Data

Suppose we want to find the person with a particular score:

```python
scores = {
    "Ali": 18,
    "Sara": 15,
    "Reza": 18,
    "Mina": 12
}

for name, score in scores.items():
    if score == 18:
        print(name)
```

Output:

```text
Ali
Reza
```

The Key tells us **who** has the score.

The Value tells us **what the score is**.

Without both pieces of information, this type of search would be less useful.

---

## 16. Understanding the Variable Names

The names `key` and `value` are not special Python keywords.

For example:

```python
for key, value in student.items():
    print(key, value)
```

works because of the meaning we give those variables.

We could technically write:

```python
for x, y in student.items():
    print(x, y)
```

This also works.

But:

```python
for key, value in student.items():
```

is clearer because the variable names describe what they contain.

Good variable names make Dictionary code easier to understand.

---

## 17. Common Beginner Mistake

A common mistake is to write:

```python
for key, value in student:
    print(key, value)
```

This is not the correct pattern for iterating over both Keys and Values.

The correct form is:

```python
for key, value in student.items():
    print(key, value)
```

Why?

Because iterating over a Dictionary directly normally iterates over its Keys.

When we specifically want Key-Value pairs, we use:

```python
student.items()
```

---

## 18. Another Common Mistake

Another mistake is confusing the Value with the Key:

```python
for value, key in student.items():
    print(key, value)
```

Technically, Python will still unpack two values, but the variable meanings are reversed.

If the pair is:

```text
"name", "Ali"
```

then:

```text
value = "name"
key   = "Ali"
```

This is logically misleading.

A clearer pattern is:

```python
for key, value in student.items():
    ...
```

Variable names should match the role of the data.

---

## 19. Practical Example: Product Inventory

Consider:

```python
inventory = {
    "apple": 10,
    "banana": 5,
    "orange": 8
}
```

We can display the inventory:

```python
for product, quantity in inventory.items():
    print(f"{product}: {quantity}")
```

We can find products with low inventory:

```python
for product, quantity in inventory.items():
    if quantity < 7:
        print(product)
```

Output:

```text
banana
```

We can also update quantities:

```python
for product, quantity in inventory.items():
    inventory[product] = quantity + 2
```

Now every product has two additional units.

The same Key-Value relationship supports reading, checking, and updating data.

---

## 20. Complete Mental Model

The most useful mental model is:

```text
Dictionary
    │
    ├── Key 1 → Value 1
    ├── Key 2 → Value 2
    └── Key 3 → Value 3
             │
           items()
             │
             ↓
      (Key, Value)
```

When we write:

```python
for key, value in dictionary.items():
```

we are saying:

> "Give me each relationship in the Dictionary, one at a time, and let me work with both sides of that relationship."

This is why `items()` is especially useful when processing Dictionary data.

---

## Key Takeaways

* `items()` provides access to Dictionary Key-Value pairs.
* Each item represents one `(Key, Value)` pair.
* The most common pattern is:

```python
for key, value in dictionary.items():
```

* `keys()` gives Keys.
* `values()` gives Values.
* `items()` gives both together.
* `items()` is especially useful when a program needs to compare, display, search, filter, or process Keys and Values together.
* The Key can be used to access or update its corresponding Value.
* Values can contain complex structures such as Lists.
* Meaningful variable names such as `key` and `value` make code easier to understand.
* Iterating over a Dictionary directly is different from iterating over `dictionary.items()`.

---

# Section Questions

## Question 1

What does `items()` provide when used with a Dictionary?

## Question 2

What is the difference between these two loops?

```python
for key in student:
    print(key)
```

and:

```python
for key, value in student.items():
    print(key, value)
```

## Question 3

What will the following code print?

```python
scores = {
    "Ali": 18,
    "Sara": 12,
    "Reza": 19
}

for name, score in scores.items():
    if score >= 18:
        print(name)
```

---

# Comprehensive Question

Given:

```python
inventory = {
    "apple": 10,
    "banana": 5,
    "orange": 8,
    "milk": 3
}
```

Write a program using `items()` that:

1. Prints every product and its quantity.
2. Prints products whose quantity is less than `6`.
3. Adds `2` to the quantity of every product.
4. Prints the updated Dictionary.

---

# Answers

## Answer 1

`items()` provides the Key and its corresponding Value together as pairs.

For example:

```text
("name", "Ali")
("age", 20)
```

## Answer 2

The first loop iterates through the Dictionary's Keys:

```python
for key in student:
    print(key)
```

The second loop explicitly iterates through Key-Value pairs:

```python
for key, value in student.items():
    print(key, value)
```

## Answer 3

The output is:

```text
Ali
Reza
```

because their scores are at least `18`.

## Comprehensive Answer

```python
inventory = {
    "apple": 10,
    "banana": 5,
    "orange": 8,
    "milk": 3
}

for product, quantity in inventory.items():
    print(f"{product}: {quantity}")

for product, quantity in inventory.items():
    if quantity < 6:
        print(product)

for product, quantity in inventory.items():
    inventory[product] = quantity + 2

print(inventory)
```

After the update, the quantities become:

```text
apple  → 12
banana → 7
orange → 10
milk   → 5
```

---

# Part 11 — Nested Dictionaries

## Introduction

So far, we have worked with Dictionaries whose Values were mostly simple pieces of data:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

But real-world data is often more structured.

A student may have:

* personal information
* academic information
* contact information
* multiple scores
* a list of skills

Putting all of this into one flat Dictionary can quickly become difficult to organize.

Python solves this naturally by allowing a **Dictionary to contain another Dictionary as a Value**.

This structure is called a **Nested Dictionary**.

---

## 1. What Is a Nested Dictionary?

A Nested Dictionary is a Dictionary that contains another Dictionary inside it.

For example:

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20,
        "city": "Baku"
    }
}
```

Here:

```text
student
│
├── name   → "Ali"
│
└── details
      │
      ├── age  → 20
      └── city → "Baku"
```

The outer Dictionary contains the Key `"details"`.

The Value associated with `"details"` is itself another Dictionary.

That inner Dictionary has its own Keys and Values.

---

## 2. Why Do We Need Nested Dictionaries?

Nested Dictionaries allow us to represent **hierarchical data**.

Instead of putting everything at the same level:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku",
    "math": 18,
    "python": 20
}
```

we can organize related information:

```python
student = {
    "name": "Ali",
    "personal": {
        "age": 20,
        "city": "Baku"
    },
    "scores": {
        "math": 18,
        "python": 20
    }
}
```

Now the structure itself tells us what each piece of data means.

```text
student
│
├── name
├── personal
│    ├── age
│    └── city
│
└── scores
     ├── math
     └── python
```

This organization becomes especially valuable when working with larger datasets.

---

## 3. Accessing a Value in a Nested Dictionary

To access data inside the inner Dictionary, we use multiple Key lookups.

For example:

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20,
        "city": "Baku"
    }
}
```

To access the age:

```python
print(student["details"]["age"])
```

Output:

```text
20
```

The lookup happens in two steps:

```text
student
   ↓
["details"]
   ↓
inner Dictionary
   ↓
["age"]
   ↓
20
```

This is one of the most important patterns for working with nested data.

---

## 4. Accessing Different Levels

Suppose we have:

```python
student = {
    "name": "Ali",
    "personal": {
        "age": 20,
        "address": {
            "city": "Baku",
            "country": "Azerbaijan"
        }
    }
}
```

We can access:

```python
student["name"]
```

which gives:

```text
Ali
```

We can access:

```python
student["personal"]["age"]
```

which gives:

```text
20
```

And we can go deeper:

```python
student["personal"]["address"]["city"]
```

which gives:

```text
Baku
```

Each additional Key moves one level deeper into the structure.

---

## 5. Nested Dictionaries Can Have Multiple Levels

There is no requirement that nesting stops after one level.

For example:

```python
company = {
    "employee": {
        "contact": {
            "address": {
                "city": "Baku"
            }
        }
    }
}
```

We can access the city with:

```python
print(
    company["employee"]["contact"]["address"]["city"]
)
```

Output:

```text
Baku
```

Although Python allows deep nesting, excessive nesting can make code difficult to read.

So nesting should be used when it makes the data structure clearer, not simply because it is possible.

---

## 6. Updating a Nested Value

Nested Values can be changed just like ordinary Dictionary Values.

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20,
        "city": "Baku"
    }
}

student["details"]["age"] = 21
```

Now:

```python
print(student["details"]["age"])
```

produces:

```text
21
```

The important idea is that we navigate to the desired Value and then assign a new Value.

---

## 7. Adding a New Value to an Inner Dictionary

We can also add new entries.

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20,
        "city": "Baku"
    }
}

student["details"]["country"] = "Azerbaijan"
```

Now the inner Dictionary contains:

```python
{
    "age": 20,
    "city": "Baku",
    "country": "Azerbaijan"
}
```

The outer Dictionary itself has not changed structurally; we modified the Dictionary stored inside `"details"`.

---

## 8. Adding a Completely New Nested Dictionary

We can create a new nested section as well:

```python
student = {
    "name": "Ali"
}

student["scores"] = {
    "math": 18,
    "python": 20
}
```

Now:

```python
print(student)
```

represents:

```text
name
   → Ali

scores
   → math   → 18
   → python → 20
```

This is useful when the structure needs to grow dynamically.

---

## 9. Deleting Nested Data

We can delete an entry from an inner Dictionary:

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20,
        "city": "Baku"
    }
}

del student["details"]["city"]
```

Now `"city"` no longer exists inside `"details"`.

We can also delete the entire nested Dictionary:

```python
del student["details"]
```

This removes the `"details"` Key and its associated Dictionary from the outer Dictionary.

---

## 10. Nested Dictionaries and `items()`

The `items()` method we learned in the previous part also works with Nested Dictionaries.

For example:

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20,
        "city": "Baku"
    }
}

for key, value in student.items():
    print(key, value)
```

Output:

```text
name Ali
details {'age': 20, 'city': 'Baku'}
```

Notice something important:

The outer loop sees the entire inner Dictionary as one Value.

It does not automatically enter the inner Dictionary.

---

## 11. Iterating Through the Inner Dictionary

If we want to process the inner Dictionary, we need another loop:

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20,
        "city": "Baku"
    }
}

for key, value in student["details"].items():
    print(key, value)
```

Output:

```text
age 20
city Baku
```

Here we explicitly tell Python:

> "Take the Dictionary stored under `details`, then iterate through its items."

---

## 12. Nested `for` Loops

For multiple nested Dictionaries, we can use nested loops.

```python
students = {
    "student1": {
        "name": "Ali",
        "score": 18
    },
    "student2": {
        "name": "Sara",
        "score": 15
    }
}

for student_id, student_info in students.items():
    print(student_id)

    for key, value in student_info.items():
        print(key, value)
```

Output:

```text
student1
name Ali
score 18
student2
name Sara
score 15
```

The outer loop processes each student.

The inner loop processes the information belonging to that student.

---

## 13. A More Realistic Structure

Nested Dictionaries become particularly useful when representing multiple objects.

For example:

```python
students = {
    "ali": {
        "age": 20,
        "city": "Baku",
        "scores": {
            "math": 18,
            "python": 20
        }
    },
    "sara": {
        "age": 19,
        "city": "Ganja",
        "scores": {
            "math": 17,
            "python": 19
        }
    }
}
```

The structure is:

```text
students
│
├── ali
│    ├── age
│    ├── city
│    └── scores
│         ├── math
│         └── python
│
└── sara
     ├── age
     ├── city
     └── scores
          ├── math
          └── python
```

Now each student has their own structured set of information.

---

## 14. Accessing Deeply Nested Data

Using the structure above:

```python
print(students["ali"]["scores"]["python"])
```

Output:

```text
20
```

The lookup follows this path:

```text
students
   ↓
ali
   ↓
scores
   ↓
python
   ↓
20
```

Understanding this path is more important than memorizing the syntax.

Whenever you see:

```python
data["a"]["b"]["c"]
```

you should mentally read it as:

> Enter `a`, then enter `b`, then retrieve `c`.

---

## 15. Updating Deeply Nested Data

We can also modify a deeply nested Value:

```python
students["ali"]["scores"]["python"] = 21
```

Now:

```python
print(students["ali"]["scores"]["python"])
```

produces:

```text
21
```

The same assignment principle used with ordinary Dictionaries applies here.

The only difference is that we have to navigate through more levels.

---

## 16. Checking for a Key at Different Levels

The `in` operator can be used at each Dictionary level.

For example:

```python
if "ali" in students:
    print("Ali exists.")
```

We can also check an inner Dictionary:

```python
if "scores" in students["ali"]:
    print("Scores exist.")
```

And even deeper:

```python
if "python" in students["ali"]["scores"]:
    print("Python score exists.")
```

The important point is that the `in` operator checks the Dictionary at the level where it is applied.

---

## 17. Avoiding Key Errors

A nested lookup can fail if one of the required Keys does not exist.

For example:

```python
print(students["ali"]["grades"]["python"])
```

If `"grades"` does not exist, Python raises:

```text
KeyError
```

With nested data, every step of the lookup path must be valid.

For example:

```text
students
  ↓
"ali"       must exist
  ↓
"grades"    must exist
  ↓
"python"    must exist
```

This is an important reason to understand the structure of the data before accessing deeply nested Values.

---

## 18. Using `get()` with Nested Dictionaries

We can sometimes make access safer with `get()`.

For example:

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20
    }
}

details = student.get("details", {})
age = details.get("age")
```

Now, if `"details"` does not exist, `details` becomes an empty Dictionary instead of immediately raising a `KeyError`.

This is useful when working with data where some fields may be missing.

However, `get()` does not automatically make every level safe. We still need to handle the structure carefully.

---

## 19. Nested Dictionaries and Data Organization

A major advantage of Nested Dictionaries is **organization**.

Compare:

```python
data = {
    "name": "Ali",
    "age": 20,
    "city": "Baku",
    "math_score": 18,
    "python_score": 20
}
```

with:

```python
data = {
    "name": "Ali",
    "personal": {
        "age": 20,
        "city": "Baku"
    },
    "scores": {
        "math": 18,
        "python": 20
    }
}
```

The second structure makes relationships much clearer.

If more information is added later, the structure can remain organized:

```python
data = {
    "name": "Ali",
    "personal": {
        "age": 20,
        "city": "Baku"
    },
    "scores": {
        "math": 18,
        "python": 20
    },
    "contact": {
        "email": "ali@example.com"
    }
}
```

Each category has its own place.

---

## 20. Nested Dictionaries Are Not a Different Data Type

A Nested Dictionary is not a special Python data type.

It is simply a normal Dictionary whose Value happens to be another Dictionary.

For example:

```python
data = {
    "person": {
        "name": "Ali"
    }
}
```

The outer structure is a Dictionary.

The inner structure is also a Dictionary.

This distinction is important because all normal Dictionary operations still apply to the inner Dictionary.

---

## 21. Combining Nested Dictionaries with Lists

Nested data does not have to contain only Dictionaries.

We can combine Dictionaries and Lists:

```python
student = {
    "name": "Ali",
    "skills": [
        "Python",
        "HTML",
        "CSS"
    ],
    "scores": {
        "math": 18,
        "python": 20
    }
}
```

Here:

```text
student
│
├── name   → String
├── skills → List
└── scores → Dictionary
```

We can access the List:

```python
print(student["skills"][0])
```

Output:

```text
Python
```

And the nested Dictionary:

```python
print(student["scores"]["python"])
```

Output:

```text
20
```

This demonstrates an important idea:

> Python data structures can be combined to model increasingly complex data.

---

## 22. Practical Example: Product Catalog

Consider an online store:

```python
products = {
    "laptop": {
        "price": 1200,
        "stock": 5,
        "brand": "Lenovo"
    },
    "phone": {
        "price": 800,
        "stock": 10,
        "brand": "Samsung"
    }
}
```

We can access the laptop price:

```python
print(products["laptop"]["price"])
```

Output:

```text
1200
```

We can check its stock:

```python
print(products["laptop"]["stock"])
```

And we can update it:

```python
products["laptop"]["stock"] = 4
```

This is a realistic example of how Nested Dictionaries can represent structured entities.

---

## 23. Practical Example: Multiple Products

We can process every product:

```python
for product_name, product_info in products.items():
    print(product_name)

    for key, value in product_info.items():
        print(f"{key}: {value}")
```

Output:

```text
laptop
price: 1200
stock: 5
brand: Lenovo

phone
price: 800
stock: 10
brand: Samsung
```

This pattern is important:

```python
for outer_key, inner_dictionary in data.items():
    for inner_key, value in inner_dictionary.items():
        ...
```

It allows us to move through multiple levels of structured Dictionary data.

---

## 24. The Important Mental Model

When working with Nested Dictionaries, do not think of the structure as one giant block of syntax.

Think of it as a tree.

For example:

```text
products
│
├── laptop
│    ├── price
│    ├── stock
│    └── brand
│
└── phone
     ├── price
     ├── stock
     └── brand
```

Then a lookup such as:

```python
products["laptop"]["price"]
```

simply means:

```text
products
   ↓
laptop
   ↓
price
   ↓
1200
```

Once this mental model becomes natural, Nested Dictionaries become much easier to understand.

---

## Key Takeaways

* A Nested Dictionary is a Dictionary containing another Dictionary as a Value.
* Nested Dictionaries are useful for representing hierarchical and structured data.
* Accessing nested data requires multiple Key lookups.
* Values can be updated or added at any nesting level.
* `items()` works with nested Dictionaries as well.
* Nested `for` loops can be used to process multiple Dictionary levels.
* `in` checks Keys at the specific Dictionary level where it is used.
* Missing Keys at any level can cause a `KeyError`.
* `get()` can help handle potentially missing data.
* Dictionaries can be combined with Lists and other data structures.
* A Nested Dictionary is still made from ordinary Python Dictionaries.
* The most useful way to understand complex nested data is as a tree of relationships.

---

# Section Questions

## Question 1

What makes a Dictionary a Nested Dictionary?

## Question 2

What will this code print?

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20,
        "city": "Baku"
    }
}

print(student["details"]["city"])
```

## Question 3

How would you change Ali's age to `21`?

## Question 4

Why might Nested Dictionaries be better than putting all information into one flat Dictionary?

---

# Comprehensive Question

Given:

```python
students = {
    "ali": {
        "age": 20,
        "scores": {
            "math": 18,
            "python": 20
        }
    },
    "sara": {
        "age": 19,
        "scores": {
            "math": 17,
            "python": 19
        }
    }
}
```

Write a program that:

1. Prints each student's name.
2. Prints their age.
3. Prints their Python score.
4. Prints students whose Python score is at least `20`.
5. Changes Ali's Python score to `21`.

---

# Answers

## Answer 1

A Dictionary becomes Nested when one of its Values is another Dictionary.

Example:

```python
data = {
    "person": {
        "name": "Ali"
    }
}
```

The Value of `"person"` is itself a Dictionary.

## Answer 2

```text
Baku
```

because:

```python
student["details"]
```

accesses the inner Dictionary, and:

```python
["city"]
```

retrieves its `"city"` Value.

## Answer 3

```python
student["details"]["age"] = 21
```

## Answer 4

Nested Dictionaries organize related information into logical groups and make hierarchical relationships explicit.

Instead of having:

```text
age
city
math_score
python_score
```

at the same level, we can organize them:

```text
personal
    age
    city

scores
    math
    python
```

This becomes much more valuable as the amount and complexity of data increase.

## Comprehensive Answer

```python
students = {
    "ali": {
        "age": 20,
        "scores": {
            "math": 18,
            "python": 20
        }
    },
    "sara": {
        "age": 19,
        "scores": {
            "math": 17,
            "python": 19
        }
    }
}

for name, info in students.items():
    print(name)
    print(f"Age: {info['age']}")
    print(f"Python: {info['scores']['python']}")

for name, info in students.items():
    if info["scores"]["python"] >= 20:
        print(name)

students["ali"]["scores"]["python"] = 21
```

---

# Part 12 — Copying Dictionaries

## Introduction

When working with Dictionaries, one of the most important concepts is understanding the difference between **assigning a Dictionary** and **copying a Dictionary**.

At first, these two operations may look similar:

```python
first = {"name": "Ali", "age": 20}

second = first
```

and:

```python
first = {"name": "Ali", "age": 20}

second = first.copy()
```

But they do **not** create the same relationship.

This difference becomes especially important when we modify data.

---

## 1. Assigning a Dictionary Does Not Create a Copy

Consider:

```python
student = {
    "name": "Ali",
    "age": 20
}

another_student = student
```

It may look like we now have two Dictionaries.

But `another_student` is not an independent copy.

Both variables refer to the **same Dictionary object**.

Conceptually:

```text
student ─────────┐
                 ↓
          ┌──────────────┐
          │  Dictionary  │
          │ name → Ali   │
          │ age  → 20    │
          └──────────────┘
                 ↑
another_student ─┘
```

There is only one Dictionary.

There are simply two names referring to it.

---

## 2. Modifying One Variable Affects the Other

Because both variables refer to the same Dictionary:

```python
student = {
    "name": "Ali",
    "age": 20
}

another_student = student

another_student["age"] = 21

print(student)
```

Output:

```text
{'name': 'Ali', 'age': 21}
```

Even though we changed `another_student`, `student` changed as well.

Why?

Because there was never a second Dictionary.

Both variables point to the same object.

---

## 3. Understanding Object Identity

Python allows us to examine whether two variables refer to the same object using the `is` operator.

```python
student = {
    "name": "Ali"
}

another_student = student

print(student is another_student)
```

Output:

```text
True
```

This means both variables refer to the exact same object.

This is different from simply checking whether two Dictionaries contain equal data.

---

## 4. Equality vs Identity

Consider:

```python
first = {"name": "Ali"}
second = {"name": "Ali"}
```

These Dictionaries contain the same data.

Therefore:

```python
print(first == second)
```

returns:

```text
True
```

But:

```python
print(first is second)
```

returns:

```text
False
```

The distinction is:

```text
==  → Do these objects contain equal values?

is  → Are these the exact same object?
```

This distinction is fundamental when working with mutable objects such as Dictionaries and Lists.

---

## 5. Creating an Independent Dictionary with `copy()`

If we want a separate Dictionary, we can use the `copy()` method:

```python
student = {
    "name": "Ali",
    "age": 20
}

another_student = student.copy()
```

Now there are two Dictionary objects:

```text
student
   ↓
Dictionary A

another_student
   ↓
Dictionary B
```

The contents are initially the same, but the objects are separate.

---

## 6. Modifying a Copied Dictionary

Now consider:

```python
student = {
    "name": "Ali",
    "age": 20
}

another_student = student.copy()

another_student["age"] = 21
```

If we print both:

```python
print(student)
print(another_student)
```

we get:

```text
{'name': 'Ali', 'age': 20}
{'name': 'Ali', 'age': 21}
```

The original Dictionary remains unchanged.

This is the main purpose of copying:

> Create another Dictionary that can be modified independently at the outer level.

---

## 7. `copy()` and `is`

We can verify that the copied Dictionary is a different object:

```python
student = {
    "name": "Ali"
}

another_student = student.copy()

print(student == another_student)
print(student is another_student)
```

Output:

```text
True
False
```

The data is equal.

The objects are different.

This is exactly what we normally want from a copy.

---

## 8. Another Way to Copy a Dictionary

The `dict()` constructor can also create a copy of a Dictionary:

```python
student = {
    "name": "Ali",
    "age": 20
}

another_student = dict(student)
```

This produces a separate Dictionary.

For example:

```python
another_student["age"] = 21

print(student["age"])
```

Output:

```text
20
```

Both `copy()` and `dict()` are useful for creating a new outer Dictionary.

---

## 9. Copying with a Dictionary Comprehension

A Dictionary can also be copied using a Dictionary comprehension:

```python
student = {
    "name": "Ali",
    "age": 20
}

another_student = {
    key: value
    for key, value in student.items()
}
```

This creates a new outer Dictionary.

However, for a simple copy, `copy()` is usually clearer:

```python
another_student = student.copy()
```

A comprehension becomes more useful when we also want to transform or filter the data.

---

## 10. Shallow Copy

The `copy()` method creates what is called a **shallow copy**.

This means:

* the outer Dictionary is copied;
* its immediate entries are copied into the new Dictionary;
* but nested mutable objects inside it may still be shared.

Consider:

```python
student = {
    "name": "Ali",
    "scores": {
        "math": 18,
        "python": 20
    }
}

another_student = student.copy()
```

The outer Dictionaries are different.

But the nested `"scores"` Dictionary is still shared.

Conceptually:

```text
student
   ↓
Outer Dictionary A
   │
   └── scores ─────┐
                   ↓
              Inner Dictionary
              math → 18
              python → 20
                   ↑
   ┌── scores ─────┘
   │
Outer Dictionary B
   ↑
another_student
```

This is one of the most important concepts in copying nested data.

---

## 11. The Shallow Copy Problem

Now:

```python
another_student["scores"]["python"] = 21
```

What happens to the original?

```python
print(student["scores"]["python"])
```

Output:

```text
21
```

This may initially seem surprising.

We used `copy()`.

Why did the original change?

Because `copy()` only copied the **outer Dictionary**.

The nested `"scores"` Dictionary was not duplicated.

Both outer Dictionaries still refer to the same inner Dictionary.

---

## 12. What `copy()` Actually Copies

Consider:

```python
student = {
    "name": "Ali",
    "scores": {
        "python": 20
    }
}

another_student = student.copy()
```

The relationship is approximately:

```text
student ───────────────→ Outer Dictionary A
                           │
                           ├── name → "Ali"
                           │
                           └── scores ─────┐
                                          ↓
                                      Inner Dictionary
                                      python → 20
                                          ↑
another_student ───────→ Outer Dictionary B
                           │
                           └── scores ─────┘
```

The outer objects are different.

The nested object is shared.

This is the meaning of a shallow copy.

---

## 13. Checking the Nested Object with `is`

We can verify this:

```python
student = {
    "scores": {
        "python": 20
    }
}

another_student = student.copy()

print(student is another_student)
print(student["scores"] is another_student["scores"])
```

Output:

```text
False
True
```

The first result tells us that the outer Dictionaries are different.

The second result tells us that the nested Dictionaries are the same object.

---

## 14. Why This Matters

This distinction matters whenever Dictionaries contain mutable objects such as:

* Dictionaries
* Lists
* Sets
* other mutable structures

For example:

```python
data = {
    "name": "Ali",
    "skills": ["Python", "HTML"]
}
```

If we shallow-copy this Dictionary:

```python
new_data = data.copy()
```

the outer Dictionary is new, but the List stored under `"skills"` can still be shared.

Therefore:

```python
new_data["skills"].append("CSS")
```

can also affect:

```python
data["skills"]
```

Understanding this behavior prevents many difficult-to-find bugs.

---

## 15. Deep Copy

When we need an entirely independent copy, including nested mutable objects, we can use a **deep copy**.

Python provides this through the `copy` module:

```python
import copy
```

Then:

```python
another_student = copy.deepcopy(student)
```

A deep copy recursively creates copies of nested objects.

---

## 16. Shallow Copy vs Deep Copy

Consider:

```python
student = {
    "name": "Ali",
    "scores": {
        "math": 18,
        "python": 20
    }
}
```

### Shallow copy

```python
another_student = student.copy()
```

Result:

```text
Outer Dictionary → copied
Inner Dictionary → shared
```

### Deep copy

```python
import copy

another_student = copy.deepcopy(student)
```

Result:

```text
Outer Dictionary → copied
Inner Dictionary → copied
```

So:

```python
another_student["scores"]["python"] = 21
```

after a deep copy does not modify:

```python
student["scores"]["python"]
```

---

## 17. Demonstrating `deepcopy()`

```python
import copy

student = {
    "name": "Ali",
    "scores": {
        "math": 18,
        "python": 20
    }
}

another_student = copy.deepcopy(student)

another_student["scores"]["python"] = 21

print(student["scores"]["python"])
print(another_student["scores"]["python"])
```

Output:

```text
20
21
```

The nested Dictionary is independent.

---

## 18. Deep Copy and Identity

We can verify the difference:

```python
import copy

student = {
    "scores": {
        "python": 20
    }
}

another_student = copy.deepcopy(student)

print(student is another_student)
print(student["scores"] is another_student["scores"])
```

Output:

```text
False
False
```

Both the outer Dictionary and the nested Dictionary are separate objects.

---

## 19. Choosing Between Assignment, Shallow Copy, and Deep Copy

These three operations have different purposes.

### Assignment

```python
second = first
```

Use this when you intentionally want another reference to the same object.

```text
first ─────┐
           ↓
        Object
           ↑
second ────┘
```

### Shallow Copy

```python
second = first.copy()
```

Use this when you want a new outer Dictionary but do not necessarily need nested mutable objects to be independent.

```text
first  → Outer A → Inner
second → Outer B ──↑
```

### Deep Copy

```python
second = copy.deepcopy(first)
```

Use this when the entire nested structure needs to become independent.

```text
first  → Outer A → Inner A
second → Outer B → Inner B
```

---

## 20. Copying Before Modification

A common practical reason to copy a Dictionary is to preserve the original data while creating a modified version.

For example:

```python
original = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}

updated = original.copy()

updated["age"] = 21
```

Now we have:

```text
original → original information

updated  → modified information
```

This pattern is useful when the original data should remain available.

---

## 21. Copying for Independent Records

Suppose we want to create several records based on a template:

```python
template = {
    "name": "",
    "age": 0,
    "city": ""
}
```

We can create separate Dictionaries:

```python
student1 = template.copy()
student2 = template.copy()
```

Then:

```python
student1["name"] = "Ali"
student2["name"] = "Sara"
```

The two outer Dictionaries are independent:

```python
print(student1)
print(student2)
```

Output:

```text
{'name': 'Ali', 'age': 0, 'city': ''}
{'name': 'Sara', 'age': 0, 'city': ''}
```

This pattern becomes useful when creating multiple records from a common structure.

---

## 22. The Mutable Object Problem

The deeper concept behind Dictionary copying is **mutability**.

Dictionaries are mutable.

That means their contents can be changed after the Dictionary has been created.

When we write:

```python
second = first
```

Python does not duplicate the mutable object.

It simply creates another reference to it.

When we write:

```python
second = first.copy()
```

Python creates a new outer Dictionary.

Understanding this relationship is much more important than simply memorizing the `copy()` method.

---

## 23. A Practical Example

Suppose we have:

```python
product = {
    "name": "Laptop",
    "price": 1200,
    "specs": {
        "ram": 16,
        "storage": 512
    }
}
```

We want to create a cheaper version.

A shallow copy is enough if we only change an outer Value:

```python
discounted = product.copy()

discounted["price"] = 1000
```

The original price remains:

```python
print(product["price"])
```

Output:

```text
1200
```

But if we also modify nested specifications:

```python
discounted["specs"]["ram"] = 32
```

the original product's RAM can also change because `"specs"` is shared.

If complete independence is required, use:

```python
import copy

discounted = copy.deepcopy(product)
```

---

## 24. Common Mistake

A common beginner assumption is:

```python
second = first
```

means:

> "Make a copy of `first`."

It does not.

It means:

> "Make `second` refer to the same object as `first`."

This distinction becomes increasingly important as programs become larger.

---

## 25. A Useful Rule

A practical rule to remember is:

```text
=          → assignment/reference

.copy()    → shallow copy

deepcopy() → independent recursive copy
```

For simple flat Dictionaries:

```python
second = first.copy()
```

is usually enough.

For deeply nested mutable structures:

```python
second = copy.deepcopy(first)
```

may be necessary.

---

## Key Takeaways

* `second = first` does not create a new Dictionary.
* Assignment creates another reference to the same object.
* `is` checks whether two variables refer to the same object.
* `==` checks whether two objects contain equal values.
* `Dictionary.copy()` creates a new outer Dictionary.
* `copy()` creates a **shallow copy**.
* Nested mutable objects can remain shared after a shallow copy.
* `copy.deepcopy()` recursively copies nested objects.
* Deep copying is useful when complete independence is required.
* `dict(first)` can also create a new outer Dictionary.
* Dictionary comprehensions can create copies while also transforming data.
* Understanding mutability and object references is more important than memorizing copying syntax.

---

# Section Questions

## Question 1

What is the difference between:

```python
second = first
```

and:

```python
second = first.copy()
```

## Question 2

What will this code print?

```python
first = {"age": 20}
second = first

second["age"] = 21

print(first["age"])
```

## Question 3

What is the difference between `==` and `is`?

## Question 4

Why can modifying a nested Dictionary after `copy()` affect the original Dictionary?

## Question 5

When would you use `copy.deepcopy()`?

---

# Comprehensive Question

Consider:

```python
student = {
    "name": "Ali",
    "scores": {
        "math": 18,
        "python": 20
    }
}
```

Write a program that:

1. Creates a shallow copy.
2. Creates a deep copy.
3. Changes the Python score in the shallow copy.
4. Changes the Python score in the deep copy.
5. Prints the original and both copies.
6. Uses `is` to demonstrate which nested Dictionary objects are shared.

---

# Answers

## Answer 1

```python
second = first
```

creates another reference to the same Dictionary.

```python
second = first.copy()
```

creates a new outer Dictionary.

## Answer 2

```text
21
```

Both variables refer to the same Dictionary.

## Answer 3

`==` compares values.

`is` checks object identity.

For example:

```python
first = {"name": "Ali"}
second = {"name": "Ali"}

print(first == second)  # True
print(first is second)  # False
```

## Answer 4

Because `copy()` creates a shallow copy.

The outer Dictionary is copied, but nested mutable objects such as Lists and Dictionaries can still be shared.

## Answer 5

Use `copy.deepcopy()` when the entire nested structure must be independent from the original.

## Comprehensive Answer

```python
import copy

student = {
    "name": "Ali",
    "scores": {
        "math": 18,
        "python": 20
    }
}

shallow = student.copy()
deep = copy.deepcopy(student)

shallow["scores"]["python"] = 21
deep["scores"]["python"] = 22

print("Original:", student)
print("Shallow:", shallow)
print("Deep:", deep)

print(student is shallow)
print(student["scores"] is shallow["scores"])

print(student is deep)
print(student["scores"] is deep["scores"])
```

The important result is:

```text
student is shallow
→ False

student["scores"] is shallow["scores"]
→ True

student is deep
→ False

student["scores"] is deep["scores"]
→ False
```

This demonstrates the central difference between shallow and deep copying.

---

