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

