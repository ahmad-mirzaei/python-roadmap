# Part 1 — Introduction to Dictionaries

> 🌐 Language: **English** | [فارسی](fa/README.md)

---

| Part | Topic                                                     |
| ---: | --------------------------------------------------------- |
|    1 | Introduction to Dictionaries                              |
|    2 | Creating Dictionaries                                     |
|    3 | Accessing Dictionary Values                               |
|    4 | Adding and Updating Items                                 |
|    5 | Removing Dictionary Items                                 |
|    6 | Checking for Keys and Values                              |
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

# Part 2 — Creating Dictionaries

## Introduction

Now that we understand what a Dictionary is and why it is useful, the next step is learning how to **create Dictionaries in different ways**.

The most common approach uses curly braces `{}` and Key-Value pairs:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

The basic pattern is:

```python
dictionary = {
    key: value,
    key: value
}
```

Understanding the different ways to construct a Dictionary is important because different situations call for different approaches.

---

## 1. Creating an Empty Dictionary

We can create an empty Dictionary using `{}`:

```python
student = {}
```

At this point, the Dictionary contains no items.

We can populate it later:

```python
student["name"] = "Ali"
student["age"] = 20
```

Now:

```python
print(student)
```

produces:

```text
{'name': 'Ali', 'age': 20}
```

This approach is useful when the information is not available all at once.

---

## 2. Creating a Dictionary with Initial Data

When we already know the data, we can provide the Key-Value pairs immediately:

```python
student = {
    "name": "Ali",
    "age": 20,
    "major": "Computer Science"
}
```

Each pair follows:

```text
Key: Value
```

and pairs are separated by commas.

For example:

```text
"name": "Ali"
```

means:

```text
Key   → "name"
Value → "Ali"
```

---

## 3. Creating a Dictionary with `dict()`

Python provides the `dict()` constructor as another way to create a Dictionary.

An empty Dictionary can be created with:

```python
student = dict()
```

This is equivalent to:

```python
student = {}
```

For simple cases, `{}` is often more concise.

However, `dict()` becomes particularly useful when we are constructing a Dictionary from existing data.

---

## 4. Using Keyword Arguments with `dict()`

We can pass keyword arguments to `dict()`:

```python
student = dict(
    name="Ali",
    age=20,
    major="Computer Science"
)
```

The result is:

```python
{
    "name": "Ali",
    "age": 20,
    "major": "Computer Science"
}
```

The keyword names become the Dictionary Keys.

This syntax is convenient when the Keys are valid Python identifiers.

For example:

```python
user = dict(
    username="ali123",
    active=True
)
```

But this approach cannot directly express a Key such as:

```python
"first-name"
```

because `"first-name"` is not a valid Python identifier.

For such Keys, the `{}` syntax is more flexible:

```python
user = {
    "first-name": "Ali"
}
```

---

## 5. Creating a Dictionary from Key-Value Pairs

We can create a Dictionary from a sequence of pairs:

```python
student = dict([
    ("name", "Ali"),
    ("age", 20),
    ("score", 18)
])
```

Each inner Tuple contains:

```text
(Key, Value)
```

Python converts those pairs into Dictionary entries.

The result is:

```python
{
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

This technique becomes useful when our data already exists in a sequence of pairs.

---

## 6. Creating a Dictionary from Two Sequences with `zip()`

Another powerful approach is combining two sequences with `zip()`.

For example:

```python
keys = ["name", "age", "score"]
values = ["Ali", 20, 18]

student = dict(zip(keys, values))
```

The result is:

```python
{
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

Conceptually, `zip()` pairs the corresponding elements:

```text
"name"  → "Ali"
"age"   → 20
"score" → 18
```

This is especially useful when Keys and Values are stored separately.

---

## 7. Creating Dictionaries from Existing Dictionaries

We can create a new Dictionary based on an existing one using `dict()`:

```python
student = {
    "name": "Ali",
    "age": 20
}

copy_student = dict(student)
```

Now `copy_student` contains the same Key-Value pairs.

```python
print(copy_student)
```

Output:

```text
{'name': 'Ali', 'age': 20}
```

This creates a new Dictionary object containing the same top-level entries.

It is important to distinguish this from simply assigning the same Dictionary to another variable:

```python
student = {
    "name": "Ali"
}

other = student
```

Here, `student` and `other` refer to the same Dictionary object.

We will examine copying in more depth later.

---

## 8. Duplicate Keys

Dictionary Keys are unique.

Consider:

```python
student = {
    "name": "Ali",
    "name": "Sara"
}
```

The second assignment replaces the first one.

The resulting Dictionary is:

```python
{
    "name": "Sara"
}
```

Therefore, writing the same Key more than once does not create multiple entries.

This is an important property because a Dictionary uses the Key to identify a particular Value.

---

## 9. Adding Items After Creation

A Dictionary does not have to be completed when it is created.

We can start with:

```python
student = {
    "name": "Ali"
}
```

and add more information later:

```python
student["age"] = 20
student["score"] = 18
```

The final Dictionary becomes:

```python
{
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

This is one of the practical consequences of Dictionary mutability.

---

## 10. Choosing the Appropriate Construction Method

Different construction methods are useful in different situations.

### Direct data

Use `{}` when the structure is known clearly:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

### Keyword-style construction

Use `dict()` when the Keys are simple identifiers:

```python
student = dict(name="Ali", age=20)
```

### Existing pairs

Use `dict()` when data already exists as pairs:

```python
pairs = [
    ("name", "Ali"),
    ("age", 20)
]

student = dict(pairs)
```

### Separate Keys and Values

Use `zip()` when Keys and Values are stored separately:

```python
keys = ["name", "age"]
values = ["Ali", 20]

student = dict(zip(keys, values))
```

The important skill is not memorizing every syntax variation. It is understanding **what form your data already has** and choosing a construction method that matches it.

---

## Key Takeaways

* `{}` is the most direct syntax for creating a Dictionary.
* `dict()` can create empty Dictionaries or construct them from existing data.
* Keyword arguments can be used with `dict()`.
* A Dictionary can be built from a sequence of `(Key, Value)` pairs.
* `zip()` can combine separate Key and Value sequences into a Dictionary.
* Duplicate Keys do not produce duplicate entries; the later Value replaces the earlier one.
* Dictionaries can be created partially and populated later.
* Choosing a construction method should depend on the form of the data you already have.

---

# Section Questions

## Question 1

Create a Dictionary named `book` using `{}` with the following information:

```text
title  → "Python"
author → "Ali"
pages  → 300
```

## Question 2

Create the following Dictionary using `dict()` and keyword arguments:

```text
name → "Sara"
age  → 21
```

## Question 3

Given:

```python
keys = ["name", "age", "city"]
values = ["Ali", 20, "Tehran"]
```

Create a Dictionary using `zip()`.

---

# Comprehensive Question

You receive the following data:

```python
keys = ["username", "age", "active"]
values = ["ali123", 20, True]
```

Create a Dictionary from this data and explain why using `zip()` is more appropriate here than manually writing every Key-Value pair.

---

# Answers

## Answer 1

```python
book = {
    "title": "Python",
    "author": "Ali",
    "pages": 300
}
```

## Answer 2

```python
student = dict(
    name="Sara",
    age=21
)
```

## Answer 3

```python
keys = ["name", "age", "city"]
values = ["Ali", 20, "Tehran"]

data = dict(zip(keys, values))
```

The result is:

```python
{
    "name": "Ali",
    "age": 20,
    "city": "Tehran"
}
```

## Comprehensive Answer

```python
keys = ["username", "age", "active"]
values = ["ali123", 20, True]

user = dict(zip(keys, values))
```

The result is:

```python
{
    "username": "ali123",
    "age": 20,
    "active": True
}
```

`zip()` is appropriate because the Keys and Values already exist as two separate sequences. It pairs the corresponding elements automatically, avoiding repetitive manual construction.

---

# Part 3 — Accessing Dictionary Values

## Introduction

Creating a Dictionary is only the beginning. The next essential skill is learning how to **retrieve the values stored inside it**.

Unlike Lists and Tuples, which normally use numeric indexes, Dictionaries use **Keys** to access their corresponding Values.

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

To retrieve the student's name:

```python
print(student["name"])
```

Output:

```text
Ali
```

The Key `"name"` tells Python exactly which Value we want.

---

## 1. Accessing a Value with Square Brackets

The most direct way to access a Dictionary Value is to place its Key inside square brackets:

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

We can access other Values in the same way:

```python
print(student["age"])
```

Output:

```text
20
```

The general pattern is:

```python
dictionary[key]
```

This is fundamentally different from:

```python
list[index]
```

because the Dictionary uses the **identity of the data**, rather than its numeric position.

---

## 2. Accessing Different Types of Values

The Value associated with a Key can have any appropriate data type.

```python
user = {
    "name": "Ali",
    "age": 20,
    "active": True
}
```

We can retrieve each Value:

```python
print(user["name"])
print(user["age"])
print(user["active"])
```

Output:

```text
Ali
20
True
```

The Key determines which Value is returned.

---

## 3. Using Variables as Keys

The Key used for access does not have to be written directly.

We can store it in a Variable:

```python
student = {
    "name": "Ali",
    "age": 20
}

field = "name"

print(student[field])
```

Output:

```text
Ali
```

Python evaluates `field`, obtains `"name"`, and then uses that value as the Key.

This becomes useful when the Key we want to access is determined dynamically.

For example:

```python
field = input("Enter a field: ")

print(student[field])
```

If the user enters:

```text
age
```

Python effectively evaluates:

```python
student["age"]
```

---

## 4. What Happens When a Key Does Not Exist?

Suppose our Dictionary is:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

Now consider:

```python
print(student["score"])
```

There is no `"score"` Key.

Python raises a `KeyError`:

```text
KeyError: 'score'
```

This is an important behavior to understand.

When using square brackets, Python expects the requested Key to exist.

Therefore, this form:

```python
dictionary[key]
```

is appropriate when the Key is expected to exist.

---

## 5. Accessing Values with `.get()`

Python provides another way to retrieve Dictionary Values:

```python
student = {
    "name": "Ali",
    "age": 20
}

print(student.get("name"))
```

Output:

```text
Ali
```

The major difference appears when the Key does not exist.

```python
print(student.get("score"))
```

Instead of raising `KeyError`, this returns:

```text
None
```

This makes `.get()` useful when a Key may or may not exist.

---

## 6. Providing a Default Value to `.get()`

`.get()` can also receive a second argument.

```python
student = {
    "name": "Ali",
    "age": 20
}

print(student.get("score", 0))
```

Output:

```text
0
```

The general form is:

```python
dictionary.get(key, default)
```

If the Key exists, its Value is returned.

If the Key does not exist, the default Value is returned.

For example:

```python
print(student.get("age", 0))
```

Output:

```text
20
```

Because `"age"` exists, the default `0` is ignored.

---

## 7. `[]` vs `.get()`

These two approaches serve different purposes.

### Square brackets

```python
student["score"]
```

Use this when the Key is expected to exist.

If it does not exist:

```text
KeyError
```

### `.get()`

```python
student.get("score")
```

Use this when the Key may not exist.

If it does not exist:

```text
None
```

Or:

```python
student.get("score", 0)
```

which returns:

```text
0
```

A useful mental model is:

```text
[]     → "I expect this Key to exist."

.get() → "This Key might not exist."
```

---

## 8. Accessing Nested Values

Dictionary Values can themselves be Dictionaries.

For example:

```python
student = {
    "name": "Ali",
    "address": {
        "city": "Tehran",
        "country": "Iran"
    }
}
```

To access `"city"`:

```python
print(student["address"]["city"])
```

Output:

```text
Tehran
```

The access happens in two stages:

```text
student
   ↓
"address"
   ↓
"city"
```

We first retrieve the `"address"` Dictionary, then retrieve `"city"` from that Dictionary.

Nested Dictionaries will be studied more deeply later.

---

## 9. Accessing Values Inside Other Data Structures

A Dictionary Value can also be a List:

```python
student = {
    "name": "Ali",
    "scores": [18, 20, 17]
}
```

We can first access the List:

```python
print(student["scores"])
```

Output:

```text
[18, 20, 17]
```

Then we can access an element of that List:

```python
print(student["scores"][0])
```

Output:

```text
18
```

This demonstrates an important principle:

> Each data structure uses its own access mechanism.

The Dictionary uses a Key:

```python
student["scores"]
```

The List then uses an Index:

```python
student["scores"][0]
```

---

## 10. Reading Values Without Changing the Dictionary

Accessing a Value does not modify the Dictionary.

```python
student = {
    "name": "Ali",
    "age": 20
}

age = student["age"]

print(age)
print(student)
```

Output:

```text
20
{'name': 'Ali', 'age': 20}
```

The Dictionary remains unchanged.

This is different from assigning a new Value:

```python
student["age"] = 21
```

Here we are no longer just accessing a Value; we are modifying the Dictionary.

---

## 11. Using Dictionary Access in Expressions

Retrieved Values can be used directly in calculations and conditions.

For example:

```python
student = {
    "name": "Ali",
    "score": 18
}

if student["score"] >= 10:
    print("Passed")
```

Output:

```text
Passed
```

Or:

```python
total = student["score"] + 2

print(total)
```

Output:

```text
20
```

The retrieved Value behaves like the original data stored in the Dictionary.

---

## 12. Accessing a Key with Special Characters

Keys do not have to be simple words.

For example:

```python
data = {
    "first-name": "Ali",
    "email.address": "ali@example.com"
}
```

These Values can still be accessed with square brackets:

```python
print(data["first-name"])
print(data["email.address"])
```

Output:

```text
Ali
ali@example.com
```

This is another reason square-bracket access is important: it works with arbitrary valid Dictionary Keys.

---

## Key Takeaways

* Dictionary Values are normally accessed through their Keys.
* Square brackets use the form `dictionary[key]`.
* If the Key does not exist, square-bracket access raises `KeyError`.
* `.get()` provides a safer alternative when a Key may be missing.
* `.get(key, default)` lets us specify a fallback Value.
* Variables can be used as Keys during access.
* Dictionary Values can contain other data structures.
* Nested structures can be accessed one level at a time.
* Reading a Value does not modify the Dictionary.
* Retrieved Values can be used directly in expressions and conditions.

---

# Section Questions

## Question 1

Given:

```python
student = {
    "name": "Sara",
    "age": 19,
    "score": 20
}
```

Write code to print the student's `name` and `score`.

## Question 2

What is the difference between these two expressions?

```python
student["score"]
```

and:

```python
student.get("score")
```

What happens if `"score"` does not exist?

## Question 3

Given:

```python
student = {
    "name": "Ali",
    "address": {
        "city": "Tehran",
        "country": "Iran"
    }
}
```

Write code to print the value of `"city"`.

---

# Comprehensive Question

Consider:

```python
user = {
    "name": "Ali",
    "age": 20,
    "profile": {
        "city": "Tehran",
        "active": True
    },
    "scores": [18, 20, 17]
}
```

Write code to:

1. Access the user's name.
2. Access the city.
3. Access the first score.
4. Safely access a Key named `"email"` and return `"Not provided"` if it does not exist.

Explain which access mechanism you used in each case and why.

---

# Answers

## Answer 1

```python
print(student["name"])
print(student["score"])
```

## Answer 2

Both can retrieve the Value associated with `"score"` when that Key exists.

```python
student["score"]
```

raises `KeyError` if `"score"` does not exist.

```python
student.get("score")
```

returns `None` if `"score"` does not exist.

A default can also be provided:

```python
student.get("score", 0)
```

## Answer 3

```python
print(student["address"]["city"])
```

First `"address"` is retrieved, then `"city"` is retrieved from the nested Dictionary.

## Comprehensive Answer

```python
user = {
    "name": "Ali",
    "age": 20,
    "profile": {
        "city": "Tehran",
        "active": True
    },
    "scores": [18, 20, 17]
}

print(user["name"])
print(user["profile"]["city"])
print(user["scores"][0])
print(user.get("email", "Not provided"))
```

The first access uses a Key directly because `"name"` is known to exist.

The second combines two Dictionary Key accesses because `"city"` is inside the nested `"profile"` Dictionary.

The third combines Dictionary access with List indexing because `"scores"` contains a List.

The fourth uses `.get()` because `"email"` may not exist, and we want a meaningful fallback instead of a `KeyError`.

---

# Part 4 — Adding and Updating Dictionary Items

## Introduction

So far, we have learned how to create a Dictionary and access the Values stored inside it.

The next important skill is learning how to **change a Dictionary after it has been created**.

Dictionaries are **mutable**, which means their contents can be changed after creation.

There are two closely related operations:

* **Adding** a new Key-Value pair
* **Updating** the Value of an existing Key

Understanding the difference between these two operations is essential for working with real data.

---

## 1. Adding a New Item

We can add a new Key-Value pair by assigning a Value to a Key that does not currently exist:

```python
student = {
    "name": "Ali",
    "age": 20
}

student["score"] = 18
```

Now the Dictionary contains:

```python
{
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

The general pattern is:

```python
dictionary[key] = value
```

If `key` does not already exist, Python creates a new entry.

---

## 2. Updating an Existing Item

The same syntax is used to update an existing Value.

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

student["score"] = 20
```

Now:

```python
print(student)
```

produces:

```text
{'name': 'Ali', 'age': 20, 'score': 20}
```

Python does not create another `"score"` entry.

Instead, the existing Value is replaced.

Therefore:

```python
dictionary[key] = value
```

can mean either:

```text
New Key     → Add a new item
Existing Key → Update its Value
```

This dual behavior is one of the most important things to understand about Dictionary assignment.

---

## 3. Adding Several Items

We can add several items one by one:

```python
student = {}

student["name"] = "Ali"
student["age"] = 20
student["score"] = 18
```

The final result is:

```python
{
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

This approach is useful when the information becomes available gradually.

For example, data may arrive from user input:

```python
student = {}

student["name"] = input("Name: ")
student["age"] = int(input("Age: "))
```

The Dictionary can then be completed as more information becomes available.

---

## 4. Updating Several Items with `update()`

When we need to add or update multiple Key-Value pairs at once, the `update()` method is useful.

```python
student = {
    "name": "Ali",
    "age": 20
}

student.update({
    "age": 21,
    "score": 19
})
```

After the operation:

```python
{
    "name": "Ali",
    "age": 21,
    "score": 19
}
```

Notice what happened:

* `"age"` already existed, so its Value was updated.
* `"score"` did not exist, so a new item was added.

Therefore, `update()` can perform both operations simultaneously.

---

## 5. Updating with Keyword Arguments

For suitable Key names, `update()` can also receive Keyword Arguments:

```python
student.update(
    age=21,
    score=19
)
```

This is convenient when the Keys are valid Python identifiers.

However, if a Key contains characters such as `-` or `.`, use a Dictionary:

```python
student.update({
    "first-name": "Ali",
    "email.address": "ali@example.com"
})
```

---

## 6. Updating from Another Dictionary

A common situation is merging information from another Dictionary into an existing one.

```python
student = {
    "name": "Ali",
    "age": 20
}

extra_data = {
    "age": 21,
    "score": 19
}

student.update(extra_data)
```

The result is:

```python
{
    "name": "Ali",
    "age": 21,
    "score": 19
}
```

Existing Keys are updated, while new Keys are added.

---

## 7. Updating from an Iterable of Pairs

`update()` can also receive an iterable containing Key-Value pairs:

```python
student = {
    "name": "Ali"
}

student.update([
    ("age", 20),
    ("score", 18)
])
```

The result is:

```python
{
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

This is useful when the incoming data already has the form of pairs.

---

## 8. `update()` Changes the Original Dictionary

An important property of `update()` is that it modifies the existing Dictionary.

```python
student = {
    "name": "Ali"
}

result = student.update({
    "age": 20
})
```

The Dictionary is changed:

```python
print(student)
```

Output:

```text
{'name': 'Ali', 'age': 20}
```

But:

```python
print(result)
```

outputs:

```text
None
```

This is because `update()` performs an in-place modification rather than returning a new Dictionary.

This distinction becomes important when writing larger programs.

---

## 9. Assignment vs `update()`

Both approaches can modify a Dictionary:

```python
student["age"] = 21
```

and:

```python
student.update({
    "age": 21
})
```

For a single Key-Value pair, direct assignment is usually simpler.

For multiple updates:

```python
student.update({
    "age": 21,
    "score": 19,
    "active": True
})
```

is often clearer.

The choice should depend on how the data is structured and how many entries need to be changed.

---

## 10. Updating a Value Based on Its Current Value

We can read a Value, modify it, and assign it back.

For example:

```python
student = {
    "name": "Ali",
    "score": 18
}

student["score"] = student["score"] + 1
```

Now:

```python
print(student["score"])
```

outputs:

```text
19
```

This can be shortened with an augmented assignment:

```python
student["score"] += 1
```

Similarly:

```python
student["score"] -= 1
```

can decrease the Value.

This pattern is especially useful for counters and accumulated values.

---

## 11. Building a Dictionary Gradually

Dictionaries are often constructed dynamically.

For example, suppose we want to count something:

```python
counts = {}

counts["Python"] = 1
counts["Java"] = 1
counts["Python"] += 1
```

The final Dictionary is:

```python
{
    "Python": 2,
    "Java": 1
}
```

Here we first create the `"Python"` Key and then update its Value.

This illustrates why it is important to understand the difference between **creating an entry** and **modifying an existing entry**.

---

## 12. Important Difference: Missing Keys and Updates

This code works:

```python
student = {}

student["score"] = 18
```

because assigning to a missing Key creates it.

But this does not work:

```python
student = {}

student["score"] += 1
```

because Python first needs to read `student["score"]`, and that Key does not exist yet.

The result is:

```text
KeyError: 'score'
```

A common solution is to provide an initial value first:

```python
student["score"] = 0
student["score"] += 1
```

Now the result is:

```python
{
    "score": 1
}
```

This distinction is extremely important when working with counters.

---

## Key Takeaways

* Dictionaries are mutable.
* `dictionary[key] = value` adds a new item when the Key does not exist.
* The same syntax updates the Value when the Key already exists.
* `update()` can add and update multiple items at once.
* `update()` can receive a Dictionary, Keyword Arguments, or an iterable of Key-Value pairs.
* `update()` modifies the original Dictionary.
* `update()` returns `None`.
* Values can be updated based on their current Values.
* Augmented assignments such as `+=` and `-=` are useful for modifying numeric Values.
* A missing Key must be initialized before using an expression such as `+=`.

---

# Section Questions

## Question 1

Given:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

Add a new Key named `"score"` with the Value `18`.

## Question 2

Given:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

Change the student's age to `21` and score to `20`.

## Question 3

Given:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

Use `update()` to:

* change `"age"` to `21`
* add `"score"` with the Value `19`
* add `"active"` with the Value `True`

---

# Comprehensive Question

Consider:

```python
counts = {}

counts["Python"] = 1
counts["Java"] = 1
```

Now suppose another Python item is encountered.

Write the code needed to increase the `"Python"` counter by one.

Then explain why this works:

```python
counts["Python"] += 1
```

but the following code fails when `"Python"` has never been added:

```python
counts["Python"] += 1
```

---

# Answers

## Answer 1

```python
student["score"] = 18
```

## Answer 2

```python
student["age"] = 21
student["score"] = 20
```

## Answer 3

```python
student.update({
    "age": 21,
    "score": 19,
    "active": True
})
```

## Comprehensive Answer

After `"Python"` has already been initialized:

```python
counts["Python"] += 1
```

works because Python can first retrieve the existing Value:

```python
counts["Python"]
```

and then add `1`.

If the Key does not exist, Python cannot retrieve its current Value, so:

```python
counts["Python"] += 1
```

raises:

```text
KeyError: 'Python'
```

A safe initialization is:

```python
counts["Python"] = 0
counts["Python"] += 1
```

After that, the Dictionary contains:

```python
{
    "Python": 1
}
```

---

# Part 5 — Removing Dictionary Items

## Introduction

So far, we have learned how to create a Dictionary, access its Values, and add or update Key-Value pairs.

The next step is learning how to **remove data from a Dictionary**.

Python provides several ways to remove Dictionary items, and each one has a different purpose:

* `del`
* `pop()`
* `popitem()`
* `clear()`

Choosing the correct method matters because these operations differ in what they remove, what they return, and what happens when the requested Key does not exist.

---

## 1. Removing an Item with `del`

The `del` statement can remove a specific Dictionary item by its Key:

```python id="7m2qd1"
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

del student["score"]
```

Now:

```python id="4q8n1v"
print(student)
```

produces:

```text id="r7k3ps"
{'name': 'Ali', 'age': 20}
```

The general form is:

```python id="4v7xq0"
del dictionary[key]
```

`del` removes the Key-Value pair directly.

---

## 2. What Happens if the Key Does Not Exist?

Consider:

```python id="x5k9tr"
student = {
    "name": "Ali",
    "age": 20
}

del student["score"]
```

Because `"score"` does not exist, Python raises:

```text id="p5j8r2"
KeyError: 'score'
```

Therefore, `del` is appropriate when we know that the Key exists.

---

## 3. Removing an Item with `pop()`

The `pop()` method removes a specific Key and **returns its Value**.

```python id="3c7n5k"
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

score = student.pop("score")
```

Now:

```python id="h6s4x1"
print(score)
print(student)
```

produces:

```text id="m4t8q2"
18
{'name': 'Ali', 'age': 20}
```

This is an important difference:

```text id="z1k6pd"
del       → removes the item
pop()     → removes the item and returns its Value
```

---

## 4. Using `pop()` with a Default Value

Like `.get()`, `pop()` can receive a default Value.

```python id="v9x2ka"
student = {
    "name": "Ali",
    "age": 20
}

score = student.pop("score", None)
```

Because `"score"` does not exist, no `KeyError` occurs.

Instead:

```python id="1f5q8z"
print(score)
```

outputs:

```text id="e7m3ax"
None
```

We can choose another default:

```python id="9s4h2c"
score = student.pop("score", 0)
```

Now `score` becomes `0`.

This is useful when a Key may or may not exist.

---

## 5. Removing the Last Inserted Item with `popitem()`

`popitem()` removes and returns the **last inserted Key-Value pair**.

```python id="k8r4wp"
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

item = student.popitem()
```

Now:

```python id="4m2z8n"
print(item)
print(student)
```

produces:

```text id="n6x3qd"
('score', 18)
{'name': 'Ali', 'age': 20}
```

The returned result is a Tuple containing:

```text id="2s7w9p"
(Key, Value)
```

For example:

```python id="h1d6qa"
key, value = student.popitem()
```

can unpack the returned pair.

---

## 6. `popitem()` and Dictionary Order

In modern Python versions, Dictionaries preserve insertion order.

Therefore, `popitem()` removes the **last inserted item**.

For example:

```python id="u3f8rm"
data = {}

data["a"] = 10
data["b"] = 20
data["c"] = 30

print(data.popitem())
```

Output:

```text id="w9n4qs"
('c', 30)
```

Then:

```python id="p6h2xd"
print(data)
```

gives:

```text id="b5m1vk"
{'a': 10, 'b': 20}
```

---

## 7. What Happens if `popitem()` Is Used on an Empty Dictionary?

Consider:

```python id="v8k3zr"
data = {}

data.popitem()
```

There is no item to remove.

Python raises:

```text id="f4x2nm"
KeyError: 'popitem(): dictionary is empty'
```

So `popitem()` should only be used when we know that the Dictionary contains at least one item, or when we deliberately handle the possibility of an empty Dictionary.

---

## 8. Removing Everything with `clear()`

If we want to remove all items from a Dictionary, we can use `clear()`:

```python id="q7d3ka"
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

student.clear()
```

Now:

```python id="v2h8ms"
print(student)
```

outputs:

```text id="a6j3pw"
{}
```

The Dictionary still exists, but it contains no items.

This is different from deleting the Dictionary itself.

---

## 9. `clear()` vs `del`

These two operations should not be confused.

### `clear()`

```python id="b8k5r1"
student.clear()
```

removes all items but keeps the Dictionary.

Afterwards:

```python id="8p2m4x"
student
```

is still a valid Dictionary:

```python id="0n7x5q"
{}
```

### `del`

```python id="1v6k3c"
del student
```

removes the Dictionary variable itself.

After that:

```python id="w4p9sj"
print(student)
```

causes:

```text
NameError
```

So:

```text id="m3f8kd"
clear() → empty the Dictionary
del      → delete the Dictionary variable
```

---

## 10. Choosing the Right Removal Method

The four main methods have different purposes:

| Method              | Removes                 | Returns          | Missing Key Behavior |
| ------------------- | ----------------------- | ---------------- | -------------------- |
| `del`               | Specific Key-Value pair | Nothing          | `KeyError`           |
| `pop(key)`          | Specific Key-Value pair | Value            | `KeyError`           |
| `pop(key, default)` | Specific Key if present | Value or default | No error             |
| `popitem()`         | Last inserted pair      | `(Key, Value)`   | `KeyError` if empty  |
| `clear()`           | All items               | `None`           | Not applicable       |

A useful mental model:

```text
del              → "Remove this Key."
pop()            → "Remove this Key and give me its Value."
popitem()        → "Remove the last item and give me the pair."
clear()          → "Remove everything."
```

---

## 11. Removing an Item While Keeping Its Value

One of the biggest practical advantages of `pop()` is that it lets us remove data and use it at the same time.

```python id="x7m2pc"
cart = {
    "product": "Keyboard",
    "price": 50,
    "quantity": 2
}

price = cart.pop("price")

print(price)
print(cart)
```

Output:

```text id="s4n8qk"
50
{'product': 'Keyboard', 'quantity': 2}
```

This is useful when an item needs to be processed before or after being removed.

---

## 12. Using `popitem()` in a Loop

Because `popitem()` removes one item at a time, it can be used to consume a Dictionary.

```python id="r2j6wb"
data = {
    "a": 10,
    "b": 20,
    "c": 30
}

while data:
    key, value = data.popitem()
    print(key, value)
```

Output:

```text id="p7d3xm"
c 30
b 20
a 10
```

The Dictionary gradually becomes empty.

This pattern is useful when we intentionally want to process and remove items until nothing remains.

---

## 13. Removing Data Does Not Require Rebuilding the Dictionary

A common beginner mistake is creating a new Dictionary without the unwanted item.

For example, instead of manually rebuilding:

```python id="w3f5ka"
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

student = {
    "name": student["name"],
    "age": student["age"]
}
```

we can simply write:

```python id="g8p1zr"
del student["score"]
```

The direct operation is clearer and expresses the actual intention: remove one item.

---

## 14. Important Difference Between `del`, `pop()`, and `clear()`

Consider this Dictionary:

```python id="t5n2yx"
data = {
    "a": 10,
    "b": 20,
    "c": 30
}
```

### Remove `"b"`

```python id="q8m4ds"
del data["b"]
```

Result:

```python id="7j3x9f"
{'a': 10, 'c': 30}
```

### Remove `"b"` and receive its Value

```python id="z6p1vc"
value = data.pop("b")
```

The Value is stored in `value`.

### Remove the last inserted item

```python id="c4x8mk"
item = data.popitem()
```

The result is a `(Key, Value)` pair.

### Remove all items

```python id="m7q2la"
data.clear()
```

Result:

```python id="e5h9sw"
{}
```

The correct method depends on what information we need after the removal.

---

## Key Takeaways

* `del` removes a specific Key-Value pair.
* `pop()` removes a specific Key and returns its Value.
* `pop(key, default)` avoids `KeyError` when a Key may be missing.
* `popitem()` removes and returns the last inserted Key-Value pair.
* `clear()` removes every item but keeps the Dictionary itself.
* `del dictionary` removes the Dictionary variable itself.
* `pop()` is useful when the removed Value is still needed.
* `popitem()` can be used to process a Dictionary item by item.
* Choosing the removal method should depend on what needs to be removed and whether the removed data is needed afterward.

---

# Section Questions

## Question 1

Given:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

Remove the `"score"` item using `del`.

## Question 2

Given:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

Remove `"score"` using `pop()` and store its Value in a Variable.

## Question 3

What is the difference between:

```python
student.clear()
```

and:

```python
del student
```

---

# Comprehensive Question

Consider:

```python
data = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

Write code that:

1. Removes `"score"` while keeping its Value.
2. Removes the last inserted item.
3. Removes all remaining items from the Dictionary.

Explain why you chose `pop()`, `popitem()`, and `clear()` for the three operations.

---

# Answers

## Answer 1

```python
del student["score"]
```

## Answer 2

```python
score = student.pop("score")
```

Now `score` contains:

```text
18
```

## Answer 3

```python
student.clear()
```

removes all items but keeps the Dictionary.

```python
del student
```

removes the Dictionary variable itself.

## Comprehensive Answer

```python
data = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

score = data.pop("score")

key, value = data.popitem()

data.clear()
```

`pop()` is used first because we need the removed Value.

`popitem()` is then used to remove the last inserted remaining item and retrieve its Key and Value.

Finally, `clear()` removes everything that remains while keeping `data` as an empty Dictionary.

---

# Part 6 — Checking for Keys and Values

## Introduction

A Dictionary stores data as **Key-Value pairs**. In real programs, we often need to determine whether a particular Key or Value exists before performing an operation.

For example, we may need to ask:

* Does this Dictionary contain the Key `"name"`?
* Does it contain the Key `"score"`?
* Is the Value `20` present?
* What should the program do if a Key does not exist?

Python provides several tools for answering these questions.

The most important one is the `in` operator.

---

## 1. Checking Whether a Key Exists

The `in` operator checks whether a Key exists in a Dictionary:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

print("name" in student)
```

Output:

```text
True
```

Because `"name"` is one of the Dictionary's Keys.

We can also check a Key that does not exist:

```python
print("email" in student)
```

Output:

```text
False
```

The general pattern is:

```python
key in dictionary
```

The result is always a Boolean:

```text
True
False
```

---

## 2. Why `in` Checks Keys

This is an important Dictionary rule:

```python
"name" in student
```

checks the **Keys**, not the Values.

Consider:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

Then:

```python
print("name" in student)
```

returns:

```text
True
```

But:

```python
print("Ali" in student)
```

returns:

```text
False
```

Even though `"Ali"` is stored in the Dictionary, it is a Value, not a Key.

This behavior is different from checking membership in a List, where `in` searches through the elements themselves.

---

## 3. Checking for a Missing Key with `not in`

We can use `not in` when we want to check that a Key does **not** exist:

```python
if "email" not in student:
    print("Email is not available.")
```

This is especially useful before adding data:

```python
if "email" not in student:
    student["email"] = "ali@example.com"
```

The program adds the Key only if it is not already present.

This can prevent an existing Value from being accidentally overwritten.

---

## 4. Using Membership Checks in Conditional Statements

Membership checks become especially useful when combined with `if`.

```python
student = {
    "name": "Ali",
    "age": 20
}

if "age" in student:
    print("Age exists.")
```

Output:

```text
Age exists.
```

We can create an alternative branch:

```python
if "email" in student:
    print("Email exists.")
else:
    print("Email does not exist.")
```

This allows the program to make decisions based on the structure of the Dictionary.

---

## 5. Checking Whether a Value Exists

The `in` operator checks Keys by default.

If we specifically want to check Values, we can use the `values()` method:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

print(20 in student.values())
```

Output:

```text
True
```

Because `20` is one of the Values.

For a Value that does not exist:

```python
print(25 in student.values())
```

Output:

```text
False
```

The distinction is:

```python
key in dictionary
```

checks Keys.

While:

```python
value in dictionary.values()
```

checks Values.

---

## 6. Checking Both Keys and Values

Suppose:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

Then:

```python
print("name" in student)
```

checks for the Key.

And:

```python
print("Ali" in student.values())
```

checks for the Value.

These are different questions.

A useful way to remember them is:

```text
dictionary
    ↓
Keys   →  key in dictionary
Values →  value in dictionary.values()
```

---

## 7. Using `values()` for Membership Tests

`values()` provides a view containing the Dictionary's Values:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

values = student.values()

print(values)
```

The exact representation is a Dictionary Values view.

More importantly, we can use it for membership testing:

```python
print(18 in student.values())
```

Output:

```text
True
```

We do not need to convert the Values into a List just to perform this check.

For example, this is unnecessary:

```python
print(18 in list(student.values()))
```

The direct form is clearer:

```python
print(18 in student.values())
```

---

## 8. Using `get()` When You Need the Value

Sometimes we do not only want to know whether a Key exists.

We actually need the Value associated with it.

For that situation, `get()` can be useful:

```python
student = {
    "name": "Ali",
    "age": 20
}

age = student.get("age")

print(age)
```

Output:

```text
20
```

If the Key does not exist:

```python
email = student.get("email")
print(email)
```

The result is:

```text
None
```

Unlike direct indexing:

```python
student["email"]
```

which would raise:

```text
KeyError: 'email'
```

Therefore, `get()` is useful when a Key may be missing and we want to handle that situation without an exception.

---

## 9. Providing a Default Value with `get()`

We can provide a default Value:

```python
email = student.get("email", "Not provided")
```

Now:

```python
print(email)
```

outputs:

```text
Not provided
```

The general form is:

```python
dictionary.get(key, default)
```

This is useful when the program needs a fallback Value.

For example:

```python
score = student.get("score", 0)
```

If `"score"` exists, its Value is returned.

If it does not exist, `0` is returned.

---

## 10. `in` vs `get()`

These two operations answer different questions.

### `in`

Use `in` when the main question is:

> Does this Key exist?

```python
if "score" in student:
    print("Score exists.")
```

### `get()`

Use `get()` when the main question is:

> What Value is associated with this Key, and what should I use if it is missing?

```python
score = student.get("score", 0)
```

This distinction helps make code more expressive.

---

## 11. `in` vs Direct Indexing

Consider:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

This:

```python
if "email" in student:
    print(student["email"])
```

is safe because the Value is accessed only after confirming that the Key exists.

But this:

```python
print(student["email"])
```

immediately attempts to access the missing Key and raises:

```text
KeyError: 'email'
```

So membership checking can be used as a guard before accessing a potentially missing Key.

---

## 12. A Common Pattern: Check Before Updating

Suppose we want to update a score only if the Key already exists:

```python
if "score" in student:
    student["score"] = 20
```

If `"score"` is missing, the update does not happen.

Alternatively, if we want to create it when missing:

```python
if "score" not in student:
    student["score"] = 0
```

Then later:

```python
student["score"] += 1
```

This pattern is especially useful for counters and progressively built data.

---

## 13. Checking for a Value Before Adding Data

Membership checks can also be used with Values.

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

if 18 in student.values():
    print("A score of 18 exists.")
```

Output:

```text
A score of 18 exists.
```

However, remember that Values do not have to be unique.

For example:

```python
data = {
    "first": 10,
    "second": 10
}
```

Here:

```python
10 in data.values()
```

is `True`, but the Value `10` belongs to two different Keys.

---

## 14. Keys and Values Are Different Concepts

Consider:

```python
data = {
    "name": "Ali",
    "city": "Tehran"
}
```

The Key `"name"` and the Value `"Ali"` are not interchangeable.

Therefore:

```python
"name" in data
```

returns:

```text
True
```

while:

```python
"Ali" in data
```

returns:

```text
False
```

To search for `"Ali"`:

```python
"Ali" in data.values()
```

returns:

```text
True
```

This distinction becomes increasingly important when Dictionaries contain complex data.

---

## 15. Practical Example: User Information

Suppose we have:

```python
user = {
    "username": "ali123",
    "age": 22,
    "country": "Iran"
}
```

We can check whether the country information exists:

```python
if "country" in user:
    print("Country information exists.")
```

We can safely retrieve it:

```python
country = user.get("country", "Unknown")
```

And we can check whether a particular country appears among the Values:

```python
if "Iran" in user.values():
    print("Iran is stored as a Value.")
```

Each operation answers a different question.

---

## 16. Practical Example: Validating Required Keys

Imagine a program that expects a Dictionary containing certain information:

```python
user = {
    "username": "ali123",
    "email": "ali@example.com",
    "age": 22
}
```

We can verify that required Keys exist:

```python
required_keys = ["username", "email", "age"]

for key in required_keys:
    if key not in user:
        print(f"Missing key: {key}")
```

If all required Keys exist, nothing is printed.

This pattern is useful for validating structured data before processing it.

---

## 17. Important Performance Perspective

For normal Python Dictionaries, Key lookup with `in` is designed to be very efficient.

For example:

```python
if "username" in user:
    ...
```

is the standard way to check whether a Key exists.

We should not normally convert the Keys to a List just to search:

```python
if "username" in list(user.keys()):
    ...
```

The conversion creates unnecessary work and makes the intention less clear.

Prefer:

```python
if "username" in user:
    ...
```

For Values, however, searching with:

```python
value in dictionary.values()
```

requires checking the Values until a match is found, so Value membership is generally different from Key membership in both purpose and performance characteristics.

---

## Key Takeaways

* `in` checks whether a Key exists in a Dictionary.
* `not in` checks whether a Key does not exist.
* `in` on a Dictionary does **not** search its Values.
* Use `dictionary.values()` when you need to search Values.
* `get()` is useful when you need a Value and the Key may be missing.
* `get(key, default)` provides a fallback Value.
* `in` is useful for guarding access to potentially missing Keys.
* Key membership and Value membership answer different questions.
* Avoid unnecessary conversions such as `list(dictionary.keys())` for normal membership checks.
* Dictionary membership checks are especially useful for validation, conditional logic, and safely updating data.

---

# Section Questions

## Question 1

Given:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

Write code that checks whether the Key `"score"` exists.

## Question 2

Using the same Dictionary, write code that checks whether the Value `20` exists.

## Question 3

Use `get()` to retrieve the `"email"` Key while returning `"Not provided"` if the Key does not exist.

---

# Comprehensive Question

Consider:

```python
user = {
    "username": "ali123",
    "age": 22
}
```

Write code that:

1. Checks whether `"email"` exists.
2. If it does not exist, safely retrieves it with a default Value of `"Not provided"`.
3. Checks whether the Value `22` exists in the Dictionary.
4. Explain why `"email" in user` and `"Not provided" in user` answer completely different questions.

---

# Answers

## Answer 1

```python
"score" in student
```

Or:

```python
if "score" in student:
    print("Score exists.")
```

## Answer 2

```python
20 in student.values()
```

## Answer 3

```python
email = student.get("email", "Not provided")
```

## Comprehensive Answer

```python
user = {
    "username": "ali123",
    "age": 22
}

if "email" in user:
    print("Email exists.")

email = user.get("email", "Not provided")

if 22 in user.values():
    print("Age value exists.")
```

`"email" in user` checks whether `"email"` is a **Key**.

`"Not provided" in user` would also check Keys, not Values, because the `in` operator applied directly to a Dictionary searches its Keys.

To search Values, we need:

```python
"Not provided" in user.values()
```

This distinction is fundamental when working with Dictionary membership.

---

# Part 7 — Dictionary Length and Counting Elements

## Introduction

A Dictionary can contain zero, one, or many Key-Value pairs. As programs become more dynamic, we often need to know **how many items a Dictionary currently contains**.

Python provides the built-in `len()` function for this purpose.

Although the operation itself is simple, understanding exactly **what `len()` counts**, how it behaves with empty Dictionaries, and how it differs from counting Keys or Values individually is important for writing reliable programs.

---

## 1. Getting the Number of Items

Consider:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

print(len(student))
```

Output:

```text
3
```

The Dictionary contains three Key-Value pairs, so its length is `3`.

The general form is:

```python
len(dictionary)
```

For a Dictionary, `len()` returns the number of **Key-Value pairs**.

---

## 2. What Exactly Does `len()` Count?

Suppose we have:

```python
data = {
    "a": 10,
    "b": 20,
    "c": 30
}
```

There are:

* 3 Keys
* 3 Values
* 3 Key-Value pairs

Therefore:

```python
len(data)
```

returns:

```text
3
```

This is because every Dictionary item consists of one Key and its corresponding Value.

---

## 3. An Empty Dictionary

An empty Dictionary has no Key-Value pairs:

```python
data = {}

print(len(data))
```

Output:

```text
0
```

This makes `len()` useful when we need to determine whether a Dictionary contains any items.

For example:

```python
if len(data) == 0:
    print("Dictionary is empty.")
```

---

## 4. A More Pythonic Empty Check

Although this works:

```python
if len(data) == 0:
    print("Empty")
```

Python allows a simpler form:

```python
if not data:
    print("Empty")
```

An empty Dictionary is considered **Falsy**, while a non-empty Dictionary is considered **Truthy**.

For example:

```python
data = {}

print(bool(data))
```

Output:

```text
False
```

After adding an item:

```python
data["name"] = "Ali"

print(bool(data))
```

Output:

```text
True
```

This gives us two common approaches:

```python
len(data) == 0
```

and:

```python
not data
```

The second form is usually preferred when the only question is whether the Dictionary is empty.

---

## 5. Checking Whether a Dictionary Contains Items

We can also write:

```python
if data:
    print("Dictionary contains items.")
```

This executes only when the Dictionary is non-empty.

For example:

```python
data = {
    "name": "Ali"
}

if data:
    print("There is data.")
```

Output:

```text
There is data.
```

This pattern is very common in Python programs.

---

## 6. Length Changes When Items Are Added

Dictionary length is dynamic.

Consider:

```python
data = {}

print(len(data))
```

Output:

```text
0
```

Add an item:

```python
data["name"] = "Ali"

print(len(data))
```

Output:

```text
1
```

Add another:

```python
data["age"] = 20

print(len(data))
```

Output:

```text
2
```

The length changes as the Dictionary structure changes.

---

## 7. Updating a Value Does Not Change the Length

This distinction is important.

Consider:

```python
student = {
    "name": "Ali",
    "score": 18
}

print(len(student))
```

Output:

```text
2
```

Now update the existing Value:

```python
student["score"] = 20

print(len(student))
```

The result is still:

```text
2
```

Why?

Because we did not create a new Key. We only changed the Value associated with an existing Key.

Therefore:

```text
New Key      → length increases
Existing Key → length stays the same
```

---

## 8. Adding a New Key Changes the Length

Compare that with:

```python
student["age"] = 20
```

Now the Dictionary contains:

```python
{
    "name": "Ali",
    "score": 20,
    "age": 20
}
```

Therefore:

```python
len(student)
```

returns:

```text
3
```

The important point is that Dictionary length depends on the number of **unique Keys**.

---

## 9. Removing an Item Changes the Length

If we remove an item:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

del student["score"]

print(len(student))
```

Output:

```text
2
```

Likewise, using `pop()` changes the length:

```python
student.pop("age")

print(len(student))
```

Now the length is:

```text
1
```

So the relationship is:

```text
Add new Key     → length + 1
Remove Key      → length - 1
Update Value    → length unchanged
```

---

## 10. `clear()` and Dictionary Length

The `clear()` method removes all items:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

student.clear()

print(len(student))
```

Output:

```text
0
```

The Dictionary still exists, but it contains no items.

---

## 11. Counting Keys Explicitly

Because Dictionary length represents the number of Key-Value pairs, it is also equal to the number of Keys.

For example:

```python
data = {
    "a": 10,
    "b": 20,
    "c": 30
}
```

These produce the same count:

```python
len(data)
```

and:

```python
len(data.keys())
```

Both return:

```text
3
```

However, for simply getting the Dictionary's size, this is usually preferable:

```python
len(data)
```

There is no need to explicitly create the Keys view first.

---

## 12. Counting Values

The same idea applies to Values:

```python
len(data.values())
```

also returns:

```text
3
```

because every Key has one corresponding Value.

So for a normal Dictionary:

```python
len(data)
len(data.keys())
len(data.values())
```

all produce the same number.

However, they represent different concepts:

* `len(data)` → number of Dictionary items
* `len(data.keys())` → number of Keys
* `len(data.values())` → number of Values

---

## 13. Counting Unique Values

Here we encounter an important distinction.

Dictionary Keys must be unique, but Values do not.

Consider:

```python
data = {
    "first": 10,
    "second": 10,
    "third": 20
}
```

Then:

```python
len(data)
```

returns:

```text
3
```

There are three Key-Value pairs.

But there are only two **unique Values**:

```text
10
20
```

We can count them with a Set:

```python
print(len(set(data.values())))
```

Output:

```text
2
```

This is a useful example of the difference between:

```text
number of Values
```

and:

```text
number of unique Values
```

---

## 14. Counting Items That Match a Condition

Sometimes we do not want the total number of items.

We want to count only the items satisfying a condition.

For example:

```python
scores = {
    "Ali": 18,
    "Sara": 15,
    "Reza": 19,
    "Mina": 12
}
```

Suppose we want to count students whose score is at least `18`.

We can write:

```python
count = 0

for score in scores.values():
    if score >= 18:
        count += 1

print(count)
```

Output:

```text
2
```

Here, `len(scores)` would tell us that there are four students, but our loop counts only the Values satisfying the condition.

---

## 15. Counting Matching Items with `sum()`

Python also allows a compact approach:

```python
count = sum(score >= 18 for score in scores.values())
```

Then:

```python
print(count)
```

outputs:

```text
2
```

The expression:

```python
score >= 18
```

produces Boolean values:

```text
True
False
True
False
```

Python treats:

```text
True  → 1
False → 0
```

when used in this numerical context.

Therefore:

```text
1 + 0 + 1 + 0 = 2
```

This technique is useful once you are comfortable with Boolean expressions and iteration.

---

## 16. Counting Keys That Match a Condition

We can also count Keys based on a condition.

For example:

```python
data = {
    "name": "Ali",
    "age": 20,
    "score": 18,
    "city": "Tehran"
}
```

Suppose we want to count Keys whose names contain the letter `"a"`:

```python
count = 0

for key in data:
    if "a" in key:
        count += 1
```

Then:

```python
print(count)
```

The important concept is that iterating directly over a Dictionary gives us its Keys.

---

## 17. Dictionary Length in Loops

The length of a Dictionary can be useful when controlling or validating program behavior.

For example:

```python
data = {
    "a": 10,
    "b": 20,
    "c": 30
}

print(f"Number of items: {len(data)}")
```

Output:

```text
Number of items: 3
```

This can be useful when reporting the current state of dynamically changing data.

---

## 18. A Dictionary Can Grow and Shrink

Consider a Dictionary that changes throughout a program:

```python
data = {}

data["a"] = 10
data["b"] = 20

print(len(data))
```

Output:

```text
2
```

Then:

```python
data["c"] = 30

print(len(data))
```

Output:

```text
3
```

Then:

```python
data.pop("a")

print(len(data))
```

Output:

```text
2
```

The length always reflects the Dictionary's **current state**.

---

## 19. Why Length Matters in Real Programs

Dictionary length is useful in many situations:

### Validation

```python
if len(user_data) < 3:
    print("Some information is missing.")
```

### Empty-state handling

```python
if not cache:
    print("Cache is empty.")
```

### Reporting

```python
print(f"Loaded {len(records)} records.")
```

### Controlling logic

```python
if len(settings) == 5:
    print("All settings are configured.")
```

The important idea is that `len()` is not just a way to display a number. It can become part of the program's decision-making logic.

---

## 20. Important Concept: Length Is Not the Same as Data Size

A Dictionary's `len()` tells us the number of Key-Value pairs.

It does **not** tell us:

* how many characters are inside its Strings,
* how many elements are inside a nested List,
* how much memory the Dictionary uses,
* how many unique Values it contains.

For example:

```python
data = {
    "name": "Alexander",
    "scores": [18, 19, 20]
}
```

Then:

```python
len(data)
```

is:

```text
2
```

because there are only two top-level Keys:

```text
"name"
"scores"
```

The List inside `"scores"` does not affect the Dictionary's length.

---

## Key Takeaways

* `len(dictionary)` returns the number of Key-Value pairs.
* An empty Dictionary has length `0`.
* Updating an existing Value does not change the length.
* Adding a new Key increases the length.
* Removing a Key decreases the length.
* `clear()` makes the Dictionary's length `0`.
* `len(dictionary.keys())` and `len(dictionary.values())` normally produce the same count as `len(dictionary)`.
* Values can repeat, while Keys must be unique.
* `len(set(dictionary.values()))` can be used to count unique Values.
* `len()` counts only top-level Dictionary items; it does not recursively count nested data.
* `not dictionary` is a concise way to check whether a Dictionary is empty.
* Length can be used for validation, reporting, and program logic.

---

# Section Questions

## Question 1

Given:

```python
data = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

What is the result of:

```python
len(data)
```

## Question 2

Given:

```python
data = {
    "a": 10,
    "b": 20
}

data["a"] = 100
```

Does the length of `data` change? Explain why.

## Question 3

Write two different ways to check whether a Dictionary is empty.

---

# Comprehensive Question

Consider:

```python
scores = {
    "Ali": 18,
    "Sara": 15,
    "Reza": 19,
    "Mina": 12
}
```

Write code that:

1. Finds the total number of students.
2. Counts how many students have a score of at least `18`.
3. Checks whether the Dictionary is empty.
4. Explain why `len(scores)` and the number of students with scores of at least `18` are different concepts.

---

# Answers

## Answer 1

```python
len(data)
```

returns:

```text
3
```

## Answer 2

No.

The length remains `2` because the existing Key `"a"` was updated. No new Key was added.

## Answer 3

Using `len()`:

```python
len(data) == 0
```

Or the more Pythonic form:

```python
not data
```

## Comprehensive Answer

```python
scores = {
    "Ali": 18,
    "Sara": 15,
    "Reza": 19,
    "Mina": 12
}

total_students = len(scores)

high_scores = sum(score >= 18 for score in scores.values())

is_empty = not scores
```

The total number of students is `4`, while the number of students with a score of at least `18` is `2`.

`len(scores)` counts all Key-Value pairs.

The conditional count only counts Values that satisfy the condition `score >= 18`.

---

