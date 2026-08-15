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

