# Part 1 — Introduction to Dictionaries

> 🌐 Language: **English** | [فارسی](fa/README.md)

---

| Part | Topic                                                     |
| ---: | --------------------------------------------------------- |
|    1 | Introduction to Dictionaries                              |
|    2 | Creating Dictionaries                                     |
|    3 | Accessing Dictionary Values                               |
|    4 | Adding and Updating Items                                 |
|    5 | Removing Items                                            |
|    6 | Checking for Keys                                         |
|    7 | Dictionary Length                                         |
|    8 | Iterating Through Dictionaries                            |
|    9 | Dictionary Keys and Values                                |
|   10 | Dictionary Items                                          |
|   11 | Nested Dictionaries                                       |
|   12 | Copying Dictionaries                                      |
|   13 | Converting Between Dictionaries and Other Data Structures |
|   14 | Final Review: Dictionaries                                |
|   15 | Dictionaries Mini Project                                 |

---

## Introduction

Until now, we have worked with **Lists** and **Tuples**. Both structures allow us to store multiple values, but they primarily organize those values by their **position** or **index**.

A Dictionary uses a different model.

A Dictionary stores data as **Key-Value pairs**, where each value is associated with a meaningful key.

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

Here:

```text
"name"  → "Ali"
"age"   → 20
"score" → 18
```

The Key tells us what the Value represents.

---

## 1. What Is a Dictionary?

A Dictionary is a **mutable data structure** designed to store relationships between Keys and Values.

Its general structure is:

```python
{
    key: value,
    key: value,
    key: value
}
```

For example:

```python
car = {
    "brand": "BMW",
    "model": "M4",
    "year": 2025
}
```

This Dictionary contains three Key-Value pairs:

```text
brand → BMW
model → M4
year  → 2025
```

This structure is especially useful when each piece of information has a clear **name or identifier**.

---

## 2. Dictionary vs. List

Consider storing student information in a List:

```python
student = ["Ali", 20, 18]
```

To understand this data, we need to already know that:

```text
Index 0 → name
Index 1 → age
Index 2 → score
```

For example:

```python
print(student[0])
```

Output:

```text
Ali
```

The problem is that `student[0]` does not communicate why index `0` represents the student's name.

The same information can be represented with a Dictionary:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

Now:

```python
print(student["name"])
```

Output:

```text
Ali
```

The code itself communicates the meaning of the data.

The fundamental difference is:

```text
List:
Index → Value

Dictionary:
Key → Value
```

---

## 3. Dictionary vs. Tuple

A Tuple also uses indexes:

```python
point = (10, 20)
```

We can access its elements using:

```python
print(point[0])
```

Output:

```text
10
```

However, a Tuple is **immutable**.

A Dictionary, on the other hand:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

is **mutable**, and its values are organized through meaningful Keys.

| Structure  | Access Method | Mutable |
| ---------- | ------------- | ------- |
| List       | Index         | Yes     |
| Tuple      | Index         | No      |
| Dictionary | Key           | Yes     |

---

## 4. Keys and Values

Every Dictionary entry consists of a Key-Value relationship:

```python
"name": "Ali"
```

Here:

* `"name"` is the **Key**.
* `"Ali"` is the **Value**.

For example:

```python
user = {
    "username": "ali123",
    "age": 20,
    "active": True
}
```

The structure can be viewed as:

```text
Key        Value
----------------
username   ali123
age        20
active     True
```

A Key usually acts as an **identifier**, while the Value contains the information associated with that identifier.

---

## 5. Why Are Keys Important?

Consider this List:

```python
product = ["Laptop", 2500, "Black", 15]
```

We need to remember the meaning of every position:

```text
0 → name
1 → price
2 → color
3 → stock
```

With a Dictionary:

```python
product = {
    "name": "Laptop",
    "price": 2500,
    "color": "Black",
    "stock": 15
}
```

Each Value has an explicit name.

This makes the structure easier to understand and reduces our dependence on remembering what each index represents.

---

## 6. Dictionaries Are Mutable

One important property of Dictionaries is that they are **mutable**.

This means that after creating a Dictionary, we can change its contents.

For example:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

We can update the age:

```python
student["age"] = 21
```

Now:

```python
print(student)
```

Output:

```text
{'name': 'Ali', 'age': 21}
```

This is different from a Tuple:

```python
point = (10, 20)
```

We cannot directly replace one of its elements.

---

## 7. Values Can Have Different Data Types

Dictionary Values are not restricted to one data type.

For example:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18.5,
    "active": True
}
```

The Values include:

* `str`
* `int`
* `float`
* `bool`

A Value can also contain another data structure:

```python
student = {
    "name": "Ali",
    "scores": [18, 20, 17]
}
```

Or even another Dictionary:

```python
student = {
    "name": "Ali",
    "address": {
        "city": "Tehran",
        "country": "Iran"
    }
}
```

We will study this structure more deeply when we reach **Nested Dictionaries**.

---

## 8. When Should We Use a Dictionary?

A Dictionary is a good choice when we have a relationship between an identifiable piece of information and its corresponding Value.

For example:

```python
user = {
    "username": "ali123",
    "email": "ali@example.com",
    "age": 20
}
```

Or:

```python
car = {
    "brand": "BMW",
    "model": "M4",
    "year": 2025
}
```

Or:

```python
book = {
    "title": "Python",
    "author": "John",
    "pages": 350
}
```

In each case, the Keys give meaning to the Values.

---

## 9. A Dictionary Is More Than a Different Syntax

It is important not to think of a Dictionary as simply a List with different syntax.

A List is generally useful when we care about a collection of values organized by position:

```python
numbers = [10, 20, 30]
```

A Tuple is useful when we need an ordered collection that should not be modified:

```python
point = (10, 20)
```

A Dictionary is useful when the relationship between a **Key and a Value** is the central idea:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

Compare:

```python
student[0]
```

with:

```python
student["name"]
```

The first describes a position.

The second describes the meaning of the data we want.

This distinction is fundamental to choosing the appropriate Python data structure.

---

## Key Takeaways

By the end of this section, you should understand that:

* A Dictionary stores data as **Key-Value pairs**.
* A Key identifies or describes a Value.
* Dictionary access is based on Keys rather than numeric indexes.
* Dictionaries are **mutable**.
* Dictionary Values can have different data types.
* A Value can itself contain another data structure.
* Dictionaries are especially useful for representing structured information.
* Choosing a Dictionary is often about expressing the **relationship between a name and a value**, rather than simply storing a sequence of values.

---

# Section Questions

## Question 1

What is the fundamental difference between accessing data in a List and accessing data in a Dictionary?

Give one example of each.

## Question 2

Identify the Keys and Values in the following Dictionary:

```python
student = {
    "name": "Sara",
    "age": 19,
    "score": 20
}
```

## Question 3

Why can a Dictionary be a better choice than a simple List for representing information about a user?

Compare:

```python
user = ["Ali", 20, True]
```

with:

```python
user = {
    "name": "Ali",
    "age": 20,
    "active": True
}
```

---

# Comprehensive Question

Considering what you have learned so far about **Lists, Tuples, and Dictionaries**, choose the most appropriate structure for each situation and explain why:

1. Storing several scores where their order matters and the values may change.
2. Storing the fixed `x` and `y` coordinates of a point.
3. Storing information about a user such as name, age, and active status.

---

# Answers

## Answer 1

A List normally uses a numeric Index:

```python
numbers = [10, 20, 30]

print(numbers[1])
```

A Dictionary uses a Key:

```python
student = {
    "name": "Ali",
    "age": 20
}

print(student["name"])
```

Therefore:

```text
List       → Index → Value
Dictionary → Key   → Value
```

## Answer 2

Keys:

```text
"name"
"age"
"score"
```

Values:

```text
"Sara"
19
20
```

## Answer 3

The Dictionary gives every Value a meaningful identifier.

With the List:

```python
user = ["Ali", 20, True]
```

we need to remember what each index represents.

With the Dictionary:

```python
user = {
    "name": "Ali",
    "age": 20,
    "active": True
}
```

the meaning of each Value is explicit.

## Comprehensive Answer

1. **List**

```python
scores = [18, 20, 17, 19]
```

A List is appropriate because the order matters and the Values can be changed.

2. **Tuple**

```python
point = (10, 20)
```

A Tuple is appropriate because the two coordinate values form a small ordered collection that does not need to be modified.

3. **Dictionary**

```python
user = {
    "name": "Ali",
    "age": 20,
    "active": True
}
```

A Dictionary is appropriate because each Value has a meaningful field name and can be accessed through that identifier.

---

