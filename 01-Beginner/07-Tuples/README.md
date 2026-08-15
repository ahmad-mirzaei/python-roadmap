# Part 1 — Introduction to Tuples

> 🌐 Language: **English** | [فارسی](fa/README.md)

## Tuples Roadmap

| Part | Topic |
|---:|---|
| 1 | Introduction to Tuples |
| 2 | Creating Tuples |
| 3 | Accessing Tuple Elements |
| 4 | Tuple Slicing |
| 5 | Tuple Immutability |
| 6 | Checking for an Element in a Tuple |
| 7 | Tuple Length and Counting Elements |
| 8 | Finding the Position of an Element |
| 9 | Iterating Through Tuples |
| 10 | Combining and Repeating Tuples |
| 11 | Converting Between Lists and Tuples |
| 12 | Tuple Unpacking |
| 13 | Nested Tuples |
| 14 | Final Review: Tuples |
| 15 | Tuples Mini Project |

## 1. What Is a Tuple?

A **tuple** is a Python data type that can store multiple values together.

A tuple is similar to a list, but there is an important difference:

```text
List  → can be changed
Tuple → cannot be changed after creation
```

For example:

```python
fruits = ("Apple", "Banana", "Orange")

print(fruits)
```

Output:

```text
('Apple', 'Banana', 'Orange')
```

The values are stored together inside one tuple.

## 2. Creating a Tuple

We create a tuple by placing elements inside parentheses `()`.

```python
numbers = (10, 20, 30, 40)

print(numbers)
```

Output:

```text
(10, 20, 30, 40)
```

A tuple can contain different types of values:

```python
student = ("Ali", 20, 18.5)

print(student)
```

Output:

```text
('Ali', 20, 18.5)
```

## 3. Tuple vs List

A list uses square brackets:

```python
fruits = ["Apple", "Banana", "Orange"]
```

A tuple usually uses parentheses:

```python
fruits = ("Apple", "Banana", "Orange")
```

The important difference is that lists are mutable, while tuples are immutable.

For example, this works with a list:

```python
fruits = ["Apple", "Banana", "Orange"]

fruits[0] = "Mango"

print(fruits)
```

Output:

```text
['Mango', 'Banana', 'Orange']
```

But a tuple cannot be changed this way:

```python
fruits = ("Apple", "Banana", "Orange")

fruits[0] = "Mango"
```

Python will raise an error because tuple elements cannot be changed after the tuple is created.

## 4. When Can We Use a Tuple?

Tuples are useful when we have a group of values that should stay unchanged.

For example:

```python
location = (51.5074, -0.1278)

print(location)
```

Output:

```text
(51.5074, -0.1278)
```

The tuple can represent a fixed pair of values.

Another example:

```python
birthday = (15, 8, 2005)

print(birthday)
```

Output:

```text
(15, 8, 2005)
```

## 5. An Important Beginner Point

A tuple is not simply "a list with parentheses".

The main idea is that a tuple is **immutable**.

That means after creating it, we cannot directly change, add, or remove its elements.

We will study this concept more carefully in a later section.

For now, remember:

```text
List  → mutable
Tuple → immutable
```

# Questions

## Question 1

What is a tuple?

## Question 2

What is the main difference between a list and a tuple?

## Question 3

Is this code valid? Why or why not?

```python
numbers = (10, 20, 30)

numbers[0] = 100
```

## Review Question

What is the difference between a mutable data type and an immutable data type, based on what we have learned so far?

# Answers

## Answer 1

A tuple is a Python data type that can store multiple values together.

## Answer 2

A list can be changed after creation, while a tuple cannot be directly changed after creation.

## Answer 3

No. The code is not valid because tuple elements cannot be changed after the tuple is created.

## Review Answer

A mutable data type can be changed after creation, while an immutable data type cannot be directly changed after creation.

---

# Part 2 — Creating Tuples

## 1. Creating a Tuple

A tuple is usually created by placing multiple values inside parentheses `()` and separating them with commas.

```python
fruits = ("Apple", "Banana", "Orange")

print(fruits)
```

Output:

```text
('Apple', 'Banana', 'Orange')
```

The commas are important because they separate the elements of the tuple.

## 2. Creating a Tuple of Numbers

A tuple can contain numbers:

```python
numbers = (10, 20, 30, 40)

print(numbers)
```

Output:

```text
(10, 20, 30, 40)
```

## 3. Creating a Tuple with Different Data Types

A tuple can contain different types of values.

```python
student = ("Ali", 20, 18.5, True)

print(student)
```

Output:

```text
('Ali', 20, 18.5, True)
```

## 4. Creating an Empty Tuple

We can create an empty tuple using empty parentheses:

```python
empty_tuple = ()

print(empty_tuple)
```

Output:

```text
()
```

An empty tuple contains no elements.

## 5. Creating a Tuple with One Element

A very important point is that a single-element tuple needs a comma.

This is not a tuple:

```python
number = (10)

print(type(number))
```

Output:

```text
<class 'int'>
```

Python treats `(10)` as a normal integer expression.

To create a tuple with one element, we need a comma:

```python
number = (10,)

print(type(number))
```

Output:

```text
<class 'tuple'>
```

This comma is important.

## 6. Tuple Creation Without Parentheses

Python also allows us to create a tuple without explicitly writing parentheses.

```python
fruits = "Apple", "Banana", "Orange"

print(fruits)
```

Output:

```text
('Apple', 'Banana', 'Orange')
```

Python recognizes the comma-separated values as a tuple.

However, using parentheses is often clearer for beginners:

```python
fruits = ("Apple", "Banana", "Orange")
```

## 7. Creating a Tuple from a List

We can use `tuple()` to convert a list into a tuple.

```python
fruits = ["Apple", "Banana", "Orange"]

fruits_tuple = tuple(fruits)

print(fruits_tuple)
```

Output:

```text
('Apple', 'Banana', 'Orange')
```

We will study conversions between Lists and Tuples in more detail later.

## 8. Checking the Type

We can use `type()` to check whether a value is a tuple.

```python
colors = ("Red", "Green", "Blue")

print(type(colors))
```

Output:

```text
<class 'tuple'>
```

## 9. Important Rule

When creating a tuple, remember:

```text
Multiple elements → commas separate the elements
One element       → a comma is required
Empty tuple       → ()
```

For example:

```python
a = ()
b = (10,)
c = (10, 20, 30)
```

# Questions

## Question 1

How do we normally create a tuple?

## Question 2

What is the difference between these two?

```python
a = (10)
b = (10,)
```

## Question 3

What will this program print?

```python
numbers = 10, 20, 30

print(numbers)
print(type(numbers))
```

## Review Question

What is the main difference between a List and a Tuple, and how do we create a tuple with only one element?

# Answers

## Answer 1

A tuple is normally created by placing comma-separated values inside parentheses `()`.

## Answer 2

`(10)` is an integer expression, while `(10,)` is a tuple containing one element.

## Answer 3

It prints:

```text
(10, 20, 30)
<class 'tuple'>
```

## Review Answer

A List is mutable, while a Tuple is immutable. To create a tuple with one element, a comma is required, such as `(10,)`.

---

