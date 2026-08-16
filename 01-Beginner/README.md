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

# Part 13 — Converting Between Dictionaries and Other Data Structures

## Introduction

A Dictionary is one of Python's most important data structures because it connects **keys** with **values**.

But real programs rarely keep data in one structure forever.

You may receive data as:

* a List,
* a Tuple,
* a Set,
* a sequence of key-value pairs,
* or another Dictionary,

and need to transform it into the structure that best fits the next operation.

Understanding these conversions is therefore not just about memorizing syntax. It is about understanding **what information is preserved, what information is lost, and how Python interprets the data during conversion**.

---

## 1. Converting a Dictionary to a List

When a Dictionary is passed to `list()`, Python converts it to a List containing its **keys**.

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}

keys = list(student)

print(keys)
```

Output:

```text
['name', 'age', 'city']
```

This is equivalent to:

```python
keys = list(student.keys())
```

The important point is that:

```python
list(dictionary)
```

means:

> Convert the Dictionary's keys into a List.

It does **not** convert the complete key-value pairs into a List.

---

## 2. Converting Dictionary Keys to a List

If the intention is specifically to obtain the keys, using `.keys()` makes the intention clearer:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}

keys = list(student.keys())

print(keys)
```

Output:

```text
['name', 'age', 'city']
```

This is useful when we need to process the keys as an actual List.

For example:

```python
for key in keys:
    print(key)
```

---

## 3. Converting Dictionary Values to a List

We can similarly convert the values:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}

values = list(student.values())

print(values)
```

Output:

```text
['Ali', 20, 'Baku']
```

Unlike `list(student)`, this gives us the Values rather than the Keys.

---

## 4. Converting Dictionary Items to a List

Sometimes we need both keys and values.

The `.items()` method provides key-value pairs:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}

items = list(student.items())

print(items)
```

Output:

```text
[('name', 'Ali'), ('age', 20), ('city', 'Baku')]
```

Each item is represented as a Tuple:

```text
(key, value)
```

So the result is a List of Tuples.

Conceptually:

```text
Dictionary
    ↓
.items()
    ↓
dict_items
    ↓
list()
    ↓
List of Tuples
```

---

## 5. Dictionary → List of Tuples

This conversion is especially important because it creates a structure that can easily be processed as a sequence:

```python
data = {
    "name": "Ali",
    "age": 20
}

pairs = list(data.items())
```

Result:

```python
[
    ("name", "Ali"),
    ("age", 20)
]
```

Each Tuple represents one key-value relationship.

This representation is often useful when:

* sorting Dictionary entries,
* iterating over pairs,
* passing key-value data to functions,
* or transforming the structure.

---

## 6. Dictionary → Tuple

We can also convert the Dictionary's keys into a Tuple:

```python
student = {
    "name": "Ali",
    "age": 20
}

keys = tuple(student)
```

Result:

```python
('name', 'age')
```

Similarly:

```python
values = tuple(student.values())
```

produces:

```python
('Ali', 20)
```

And:

```python
items = tuple(student.items())
```

produces:

```python
(('name', 'Ali'), ('age', 20))
```

---

## 7. Dictionary → Set

A Dictionary can also be converted into a Set:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}

keys = set(student)
```

Result:

```python
{'name', 'age', 'city'}
```

Again, the conversion uses the Dictionary's keys.

If we want the values:

```python
values = set(student.values())
```

The result contains the unique values.

This is particularly useful when we care about **membership and uniqueness** rather than key-value relationships.

---

## 8. Converting a List of Pairs into a Dictionary

The reverse operation is equally important.

Suppose we have:

```python
pairs = [
    ("name", "Ali"),
    ("age", 20),
    ("city", "Baku")
]
```

We can convert it into a Dictionary:

```python
student = dict(pairs)

print(student)
```

Output:

```text
{'name': 'Ali', 'age': 20, 'city': 'Baku'}
```

Python expects each element to contain exactly two parts:

```text
(key, value)
```

This is why a List of two-element Tuples is a natural source for `dict()`.

---

## 9. List of Lists → Dictionary

The elements do not have to be Tuples.

A List of two-element Lists also works:

```python
pairs = [
    ["name", "Ali"],
    ["age", 20],
    ["city", "Baku"]
]

student = dict(pairs)
```

Result:

```python
{
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}
```

The important requirement is not whether the elements are Lists or Tuples.

The important requirement is that each element provides **two values**:

```text
key + value
```

---

## 10. Tuple of Pairs → Dictionary

A Tuple containing key-value pairs can also be converted:

```python
pairs = (
    ("name", "Ali"),
    ("age", 20)
)

student = dict(pairs)

print(student)
```

Output:

```text
{'name': 'Ali', 'age': 20}
```

So `dict()` can consume many iterable structures as long as each element can provide a key and a value.

---

## 11. Dictionary → Dictionary

Passing a Dictionary to `dict()` creates a new outer Dictionary:

```python
original = {
    "name": "Ali",
    "age": 20
}

new_dictionary = dict(original)
```

The result contains the same key-value pairs.

```python
print(new_dictionary)
```

Output:

```text
{'name': 'Ali', 'age': 20}
```

At the outer level:

```python
print(original is new_dictionary)
```

returns:

```text
False
```

However, just like `.copy()`, this should be understood as an **outer/shallow copy**, not a recursive deep copy.

---

## 12. Converting Dictionary Keys and Values Together

A useful transformation is to turn a Dictionary into a List of pairs:

```python
data = {
    "Python": 90,
    "HTML": 80,
    "CSS": 75
}

pairs = list(data.items())
```

Result:

```python
[
    ("Python", 90),
    ("HTML", 80),
    ("CSS", 75)
]
```

Now the data can be handled as a sequence.

For example:

```python
for subject, score in pairs:
    print(subject, score)
```

This demonstrates why conversion is useful: we are not simply changing syntax; we are changing the **way the data can be processed**.

---

## 13. Converting a Dictionary into a List for Sorting

Dictionary entries can be converted into a List of Tuples before sorting.

```python
scores = {
    "Ali": 85,
    "Sara": 95,
    "Reza": 78
}

items = list(scores.items())

items.sort(key=lambda item: item[1])

print(items)
```

Output:

```text
[('Reza', 78), ('Ali', 85), ('Sara', 95)]
```

The Dictionary has been transformed into a sequence of pairs so that we can sort the entries according to their values.

This is a practical example of choosing a data structure based on the operation we want to perform.

---

## 14. Converting a Dictionary to JSON

Another important conversion in real programs is between Python Dictionaries and JSON.

Python provides the `json` module:

```python
import json
```

A Dictionary can be converted into a JSON string with `json.dumps()`:

```python
student = {
    "name": "Ali",
    "age": 20
}

json_data = json.dumps(student)

print(json_data)
```

Output:

```text
{"name": "Ali", "age": 20}
```

This is not the same as simply converting the Dictionary to a String with `str()`.

JSON is a structured data format designed for exchanging data between systems.

---

## 15. JSON → Dictionary

The reverse conversion uses `json.loads()`:

```python
import json

json_data = '{"name": "Ali", "age": 20}'

student = json.loads(json_data)

print(student)
```

Output:

```text
{'name': 'Ali', 'age': 20}
```

Now the JSON string has become a Python Dictionary.

The general relationship is:

```text
Python Dictionary
       ↓
   json.dumps()
       ↓
    JSON string
       ↓
   json.loads()
       ↓
Python Dictionary
```

---

## 16. Dictionary → List → Dictionary

Conversions can be chained.

For example:

```python
student = {
    "name": "Ali",
    "age": 20
}

pairs = list(student.items())

new_student = dict(pairs)
```

The final Dictionary contains the same key-value relationships.

```python
print(new_student)
```

Output:

```text
{'name': 'Ali', 'age': 20}
```

This pattern demonstrates an important idea:

> A conversion can change the representation of data without necessarily changing the information it represents.

---

## 17. What Can Be Lost During Conversion?

Not every conversion preserves every property.

For example, converting Dictionary values to a Set:

```python
data = {
    "a": 10,
    "b": 10,
    "c": 20
}

values = set(data.values())

print(values)
```

produces:

```text
{10, 20}
```

The duplicate `10` disappears.

Why?

Because a Set stores unique elements.

So:

```text
Dictionary → Set
```

can result in information loss when duplicate values exist.

This is why conversion should always be intentional.

---

## 18. Dictionary → Set vs Dictionary → List

Suppose:

```python
data = {
    "a": 10,
    "b": 10,
    "c": 20
}
```

Then:

```python
list(data.values())
```

produces:

```text
[10, 10, 20]
```

while:

```python
set(data.values())
```

produces:

```text
{10, 20}
```

The List preserves repeated values.

The Set removes duplicates.

Choosing between them depends on what the program needs.

---

## 19. Converting Keys to Different Structures

For a Dictionary:

```python
data = {
    "a": 10,
    "b": 20,
    "c": 30
}
```

we can obtain:

```python
list(data.keys())
```

```text
['a', 'b', 'c']
```

or:

```python
tuple(data.keys())
```

```text
('a', 'b', 'c')
```

or:

```python
set(data.keys())
```

```text
{'a', 'b', 'c'}
```

The same source data can therefore be represented in several different ways.

---

## 20. Choosing the Right Conversion

The most important question is not:

> "How do I convert this Dictionary?"

The better question is:

> "What structure does the next operation require?"

For example:

| Goal                              | Useful representation |
| --------------------------------- | --------------------- |
| Access by key                     | Dictionary            |
| Process keys as a sequence        | List/Tuple of keys    |
| Process key-value pairs           | List/Tuple of items   |
| Remove duplicate values           | Set                   |
| Sort entries                      | List of pairs         |
| Exchange data with another system | JSON                  |
| Build a Dictionary from pairs     | `dict()`              |

The conversion should serve the operation.

---

## 21. A Practical Example

Imagine receiving user information as a List of pairs:

```python
user_data = [
    ("username", "ali"),
    ("age", 20),
    ("country", "Azerbaijan")
]
```

We can convert it:

```python
user = dict(user_data)
```

Now accessing data becomes much easier:

```python
print(user["username"])
print(user["age"])
```

Output:

```text
ali
20
```

The original structure was useful for representing a sequence of pairs.

The Dictionary is better for accessing information by key.

---

## 22. Another Practical Example

Suppose we have:

```python
scores = {
    "Ali": 85,
    "Sara": 95,
    "Reza": 85
}
```

If we need all scores:

```python
scores_list = list(scores.values())
```

Result:

```text
[85, 95, 85]
```

If we only need the unique scores:

```python
unique_scores = set(scores.values())
```

Result:

```text
{85, 95}
```

The same Dictionary can therefore produce different structures depending on the problem.

---

## 23. Common Mistakes

### Mistake 1: Expecting `list(dictionary)` to contain values

```python
data = {"a": 10, "b": 20}

print(list(data))
```

Result:

```text
['a', 'b']
```

It produces keys.

For values, use:

```python
list(data.values())
```

---

### Mistake 2: Forgetting `.items()`

If we want key-value pairs:

```python
list(data.items())
```

not:

```python
list(data)
```

---

### Mistake 3: Passing invalid data to `dict()`

This works:

```python
dict([
    ("a", 1),
    ("b", 2)
])
```

But this does not represent valid key-value pairs:

```python
dict([
    ("a", 1, 2),
    ("b", 3, 4)
])
```

Each element must provide exactly two parts.

---

### Mistake 4: Assuming Set conversion preserves duplicates

It does not.

```python
set([10, 10, 20])
```

becomes:

```text
{10, 20}
```

---

## 24. The Deeper Concept

The deeper lesson of conversion is that **data structures represent different ways of organizing information**.

A Dictionary emphasizes:

```text
key → value
```

A List emphasizes:

```text
ordered sequence
```

A Tuple emphasizes:

```text
fixed sequence
```

A Set emphasizes:

```text
unique membership
```

JSON emphasizes:

```text
data exchange
```

Converting between them means choosing a representation that better matches the next operation.

This is why understanding conversion is more important than memorizing individual conversion commands.

---

## Key Takeaways

* `list(dictionary)` produces the Dictionary's keys.
* `list(dictionary.keys())` explicitly produces a List of keys.
* `list(dictionary.values())` produces a List of values.
* `list(dictionary.items())` produces a List of `(key, value)` Tuples.
* `tuple()` can be used similarly for keys, values, or items.
* `set()` is useful when unique elements are needed.
* `dict()` can build a Dictionary from iterable key-value pairs.
* Lists of Tuples and Lists of Lists can be converted into Dictionaries.
* `dict(existing_dictionary)` creates a new outer Dictionary.
* `json.dumps()` converts a Python Dictionary into JSON text.
* `json.loads()` converts JSON text into a Python Dictionary.
* Conversions can change how data is processed.
* Some conversions can lose information, especially when moving to a Set.
* The correct conversion depends on the operation that comes next.

---

# Section Questions

## Question 1

What does this produce?

```python
data = {
    "name": "Ali",
    "age": 20
}

print(list(data))
```

## Question 2

How do you create a List containing all Dictionary values?

## Question 3

What does `list(data.items())` produce?

## Question 4

How can this structure be converted into a Dictionary?

```python
pairs = [
    ("name", "Ali"),
    ("age", 20)
]
```

## Question 5

What information can be lost when Dictionary values are converted to a Set?

## Question 6

What is the difference between `json.dumps()` and `json.loads()`?

---

# Comprehensive Question

Given:

```python
scores = {
    "Ali": 85,
    "Sara": 95,
    "Reza": 85
}
```

Write a program that:

1. Converts the keys into a List.
2. Converts the values into a List.
3. Converts the values into a Set.
4. Converts the items into a List of Tuples.
5. Converts that List of Tuples back into a Dictionary.
6. Converts the Dictionary into JSON.
7. Converts the JSON back into a Python Dictionary.
8. Prints each resulting structure.

The goal is to observe not only the syntax of each conversion, but also how the representation and information characteristics change.

---

# Final Review: Dictionaries

This review is not meant to repeat every Dictionary method one more time.

The goal is to connect the topics together and build a **mental model of Dictionaries** that you can use when solving new problems.

---

## 1. The Core Idea of a Dictionary

A Dictionary stores data as a relationship between a **key** and a **value**:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}
```

The important mental model is:

```text
"name" → "Ali"
"age"  → 20
"city" → "Baku"
```

A Dictionary is therefore useful when the program needs to answer questions such as:

> "Given this identifier, what information belongs to it?"

For example:

```python
student["age"]
```

does not mean:

> "Give me the second element."

It means:

> "Give me the value associated with the key `age`."

This distinction is fundamental.

---

# 2. Dictionary vs List

Consider:

```python
students = ["Ali", "Sara", "Reza"]
```

and:

```python
students = {
    "first": "Ali",
    "second": "Sara",
    "third": "Reza"
}
```

The List is naturally accessed by position:

```python
students[0]
```

The Dictionary is naturally accessed by meaning:

```python
students["first"]
```

So the important difference is not simply:

> List uses numbers, Dictionary uses strings.

The deeper difference is:

* List → **position-oriented**
* Dictionary → **key-oriented**

A key gives the data semantic meaning.

---

# 3. Creating Dictionaries

A Dictionary can be created with `{}`:

```python
person = {
    "name": "Ali",
    "age": 20
}
```

An empty Dictionary:

```python
person = {}
```

can later receive data:

```python
person["name"] = "Ali"
person["age"] = 20
```

Python also provides `dict()`:

```python
person = dict(name="Ali", age=20)
```

The important idea is that different creation techniques ultimately produce the same type:

```python
type(person)
```

```text
<class 'dict'>
```

---

# 4. Keys and Values Have Different Roles

Consider:

```python
product = {
    "name": "Laptop",
    "price": 1200,
    "stock": 15
}
```

Here:

```text
Keys:
"name"
"price"
"stock"

Values:
"Laptop"
1200
15
```

The key identifies the information.

The value is the information itself.

This is why keys must satisfy different requirements from values.

A Dictionary's keys must be **hashable**, while values do not have this restriction.

For example, these can be values:

```python
data = {
    "numbers": [1, 2, 3],
    "settings": {"theme": "dark"},
    "tags": {"python", "programming"}
}
```

But mutable structures such as Lists and Sets cannot normally be Dictionary keys.

---

# 5. Accessing Data

The most direct form is:

```python
student["name"]
```

If the key does not exist:

```python
student["email"]
```

Python raises:

```text
KeyError
```

When the key may not exist, `.get()` is often safer:

```python
student.get("email")
```

which returns:

```text
None
```

We can also provide a default:

```python
student.get("email", "Not provided")
```

This gives:

```text
Not provided
```

The important conceptual difference is:

```text
dictionary[key]
```

means:

> This key is expected to exist.

while:

```text
dictionary.get(key)
```

means:

> This key may or may not exist.

---

# 6. Adding and Updating Data

These two operations use the same syntax:

```python
student["age"] = 21
```

If `"age"` already exists, its value is updated.

If it does not exist, a new key-value pair is created.

Therefore:

```python
dictionary[key] = value
```

can mean either:

```text
Add
```

or:

```text
Update
```

depending on whether the key already exists.

This is one of the most important behaviors to remember.

---

# 7. Removing Data

Python provides several ways to remove Dictionary data.

```python
del student["age"]
```

removes a specific key.

```python
student.pop("age")
```

removes the key and returns its value.

```python
student.clear()
```

removes all entries.

The choice depends on what the program needs.

If the removed value is needed:

```python
age = student.pop("age")
```

is more useful than `del`.

---

# 8. Checking Membership

When we write:

```python
"name" in student
```

Python checks whether `"name"` is a **key** in the Dictionary.

This is important:

```python
20 in student
```

does not normally ask whether `20` is one of the values.

To search values:

```python
20 in student.values()
```

To search key-value pairs:

```python
("age", 20) in student.items()
```

Therefore, membership testing depends on **which view of the Dictionary we are searching**.

---

# 9. Dictionary Length

```python
len(student)
```

returns the number of key-value pairs.

For:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}
```

we get:

```text
3
```

It does not count individual characters inside strings or individual elements inside nested Lists.

It counts the number of top-level entries.

---

# 10. Iterating Through a Dictionary

The simplest loop:

```python
for key in student:
    print(key)
```

iterates over keys.

To get values:

```python
for value in student.values():
    print(value)
```

To get both:

```python
for key, value in student.items():
    print(key, value)
```

This last form is particularly important because it matches the fundamental structure:

```text
key → value
```

---

# 11. Keys, Values, and Items

The three main views are:

```python
student.keys()
student.values()
student.items()
```

They represent three different perspectives on the same Dictionary.

```text
Dictionary
   │
   ├── keys()   → keys
   │
   ├── values() → values
   │
   └── items()  → key-value pairs
```

This becomes especially useful when we need to process only one part of the data.

---

# 12. Combining and Updating Dictionaries

Suppose:

```python
a = {
    "name": "Ali",
    "age": 20
}

b = {
    "city": "Baku",
    "age": 21
}
```

We can update one Dictionary with another:

```python
a.update(b)
```

Now:

```python
{
    "name": "Ali",
    "age": 21,
    "city": "Baku"
}
```

Notice that `"age"` was replaced.

When two Dictionaries contain the same key, the later value wins.

This is a general rule worth remembering whenever Dictionaries are merged.

---

# 13. Combining Dictionaries with `|`

Modern Python also supports Dictionary union:

```python
a = {"name": "Ali"}
b = {"age": 20}

result = a | b
```

Result:

```python
{
    "name": "Ali",
    "age": 20
}
```

Unlike `.update()`, this creates a new Dictionary rather than modifying `a`.

So there is an important distinction:

```python
a.update(b)
```

modifies `a`.

While:

```python
result = a | b
```

creates a new result.

---

# 14. Nested Dictionaries

A Dictionary can contain another Dictionary:

```python
students = {
    "ali": {
        "age": 20,
        "city": "Baku"
    },
    "sara": {
        "age": 22,
        "city": "Ganja"
    }
}
```

Now accessing data happens in stages:

```python
students["ali"]["age"]
```

The first lookup:

```python
students["ali"]
```

returns another Dictionary.

Then:

```python
["age"]
```

accesses data inside that nested Dictionary.

This gives us a powerful model:

```text
students
   ↓
"ali"
   ↓
inner Dictionary
   ↓
"age"
   ↓
20
```

Nested Dictionaries are useful for representing structured real-world data.

---

# 15. Copying Dictionaries

This is a common source of mistakes.

Consider:

```python
original = {
    "numbers": [1, 2, 3]
}

copy = original.copy()
```

The outer Dictionary is copied, but the nested List is still shared.

Therefore:

```python
copy["numbers"].append(4)
```

also affects:

```python
original["numbers"]
```

For a completely independent nested structure, `deepcopy()` is required:

```python
from copy import deepcopy

copy = deepcopy(original)
```

The important distinction is:

```text
copy()
```

→ shallow copy

```text
deepcopy()
```

→ recursive independent copy

---

# 16. Converting Dictionaries

A Dictionary can be viewed in different forms.

Keys:

```python
list(data.keys())
```

Values:

```python
list(data.values())
```

Items:

```python
list(data.items())
```

A List of pairs can become a Dictionary:

```python
pairs = [
    ("name", "Ali"),
    ("age", 20)
]

data = dict(pairs)
```

This is useful because different operations favor different representations.

For example:

```text
Dictionary → List of pairs → sorting
```

while:

```text
List of pairs → Dictionary → key-based lookup
```

---

# 17. Dictionary and JSON

A Dictionary is a Python object.

JSON is a data-exchange format.

They are related but not identical.

Python Dictionary → JSON:

```python
import json

json_data = json.dumps(data)
```

JSON → Python Dictionary:

```python
data = json.loads(json_data)
```

This is extremely important in real programming because APIs frequently exchange structured data using JSON.

---

# 18. The Most Important Dictionary Questions

When working with a Dictionary, ask yourself:

### What does the key represent?

For example:

```python
users["ali"]
```

Does `"ali"` represent:

* an ID?
* a username?
* a category?
* a database identifier?

Understanding the meaning of the key makes the structure easier to reason about.

### What does the value represent?

Is it:

* a number?
* a string?
* a List?
* another Dictionary?
* an object?

### Can the key be missing?

If yes, consider:

```python
.get()
```

or an explicit membership check.

### Do I need keys, values, or both?

Choose:

```python
.keys()
.values()
.items()
```

### Am I modifying the original Dictionary?

This matters when using:

```python
update()
```

versus:

```python
|
```

### Is nested data involved?

If yes, consider whether a shallow copy is enough.

---

# 19. Dictionary Problem-Solving Pattern

A large number of Dictionary problems can be approached with the following process:

```text
1. Identify what uniquely identifies the data.
             ↓
2. Choose that information as the key.
             ↓
3. Store the associated information as the value.
             ↓
4. Decide whether the key may be missing.
             ↓
5. Choose lookup, iteration, update, or removal.
             ↓
6. Choose the appropriate representation for the next operation.
```

For example, if we are storing student scores:

```python
scores = {
    "Ali": 85,
    "Sara": 95,
    "Reza": 78
}
```

The student name is the identifier.

The score is the associated value.

That makes:

```python
scores["Sara"]
```

a natural operation.

---

# 20. Common Mistakes

## Mistake 1 — Confusing Keys with Positions

This:

```python
student[0]
```

does not mean:

> Give me the first item.

It searches for a key literally equal to `0`.

If `0` is not a key, Python raises `KeyError`.

---

## Mistake 2 — Assuming `in` Searches Values

```python
20 in student
```

checks keys.

For values:

```python
20 in student.values()
```

---

## Mistake 3 — Modifying a Dictionary While Iterating

Code like this can cause problems:

```python
for key in student:
    del student[key]
```

Changing the Dictionary's size during iteration is unsafe.

A safer approach is to iterate over a separate collection of keys:

```python
for key in list(student):
    del student[key]
```

The important principle is:

> Do not structurally modify the collection you are currently traversing unless the operation is explicitly designed for it.

---

## Mistake 4 — Forgetting Shallow Copy Behavior

```python
copy = original.copy()
```

does not recursively copy nested mutable objects.

This matters whenever Dictionaries contain Lists, Sets, or other mutable structures.

---

## Mistake 5 — Accidentally Overwriting a Key

Consider:

```python
data = {
    "score": 80
}

data["score"] = 100
```

The original `80` is replaced.

Dictionary keys are unique.

Assigning a value to an existing key updates that key.

---

# 21. Dictionary as a Lookup Structure

One of the strongest uses of a Dictionary is replacing repeated searching with direct lookup.

Imagine:

```python
names = ["Ali", "Sara", "Reza"]
scores = [85, 95, 78]
```

To find Sara's score, we need to relate positions between two Lists.

A Dictionary makes that relationship explicit:

```python
scores = {
    "Ali": 85,
    "Sara": 95,
    "Reza": 78
}
```

Now:

```python
scores["Sara"]
```

directly represents:

```text
Sara → 95
```

This is the deeper reason Dictionaries are so useful.

They do not merely store data.

They encode **relationships between identifiers and information**.

---

# 22. Dictionary as a Data Modeling Tool

A Dictionary can model real-world concepts:

```python
user = {
    "username": "ali",
    "age": 20,
    "active": True
}
```

It can represent a product:

```python
product = {
    "name": "Laptop",
    "price": 1200,
    "stock": 15
}
```

It can represent configuration:

```python
config = {
    "debug": True,
    "port": 8000,
    "host": "localhost"
}
```

It can represent relationships:

```python
grades = {
    "math": 90,
    "python": 95,
    "english": 82
}
```

So Dictionary knowledge is not only about Python syntax.

It is also an introduction to **data modeling**.

---

# 23. The Bigger Picture

By now, the main Python data structures can be understood through the kind of problem they solve:

| Structure  | Main idea                     |
| ---------- | ----------------------------- |
| List       | Ordered collection            |
| Tuple      | Ordered, immutable collection |
| Set        | Unique collection             |
| Dictionary | Key-value relationship        |

The important skill is not memorizing every method.

The important skill is asking:

> What relationship does my data have, and which structure expresses that relationship naturally?

If the answer is:

> "I need to find information using an identifier."

A Dictionary is often the natural choice.

---

# Final Mental Model

Think of a Dictionary as a system of labeled relationships:

```text
                 Dictionary
                     │
          ┌──────────┼──────────┐
          ↓          ↓          ↓
        Key        Key        Key
          ↓          ↓          ↓
       Value      Value      Value
```

Then connect that model to the operations:

```text
Create
  ↓
Access
  ↓
Add / Update
  ↓
Check
  ↓
Iterate
  ↓
Remove
  ↓
Combine
  ↓
Nest
  ↓
Copy
  ↓
Convert
```

Once this model is clear, individual methods stop looking like isolated commands.

They become different operations on the same underlying idea:

> **A Dictionary connects keys to values and gives the program a meaningful way to organize, find, modify, and transform related data.**

---

# Final Review Questions

## Question 1

What is the fundamental difference between accessing a List and accessing a Dictionary?

## Question 2

Why is this:

```python
data[0]
```

not necessarily the first element of a Dictionary?

## Question 3

What is the difference between:

```python
data[key]
```

and:

```python
data.get(key)
```

?

## Question 4

What happens when we assign a value to a key that already exists?

## Question 5

What does:

```python
key in data
```

actually check?

## Question 6

What is the difference between:

```python
data.keys()
data.values()
data.items()
```

?

## Question 7

When would you choose a Dictionary instead of a List?

## Question 8

What is the difference between:

```python
data.update(other)
```

and:

```python
result = data | other
```

?

## Question 9

Why can `copy()` be insufficient when a Dictionary contains nested mutable objects?

## Question 10

What is the difference between a shallow copy and a deep copy?

## Question 11

What happens when Dictionary values are converted to a Set?

## Question 12

Why can a List of `(key, value)` pairs be converted into a Dictionary?

---

# Comprehensive Challenge

Consider the following data:

```python
students = {
    "ali": {
        "age": 20,
        "scores": [85, 90, 95]
    },
    "sara": {
        "age": 22,
        "scores": [92, 88, 96]
    }
}
```

Write a program that:

1. Accesses Ali's age.
2. Adds a new student.
3. Updates Sara's age.
4. Adds another score for Ali.
5. Checks whether `"reza"` exists.
6. Iterates through all students.
7. Prints each student's name and scores.
8. Creates a shallow copy of the Dictionary.
9. Demonstrates why modifying a nested List can affect the original.
10. Creates a deep copy.
11. Converts the top-level items into a List of Tuples.
12. Converts that List back into a Dictionary.
13. Converts the Dictionary into JSON.
14. Converts the JSON back into a Python Dictionary.

The goal is not merely to complete the operations.

You should be able to explain **why Dictionary is the appropriate structure, what each operation does to the data model, and where copying or conversion can change the behavior of the data.**

---

