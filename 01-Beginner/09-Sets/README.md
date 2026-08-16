## Course Outline

1. Introduction to Sets
2. Creating Sets
3. Adding Elements to a Set
4. Removing Elements from a Set
5. Checking for an Element in a Set
6. Set Length and Counting Elements
7. Iterating Through Sets
8. Set Union
9. Set Intersection
10. Set Difference
11. Set Symmetric Difference
12. Converting Between Sets and Other Data Structures
13. Set Immutability and `frozenset`
14. Final Review: Sets
15. Sets Mini Project

---

# Sets — Part 1: Introduction to Sets

> 🌐 Language: **English** | [فارسی](fa/README.md)

## What Is a Set?

A **Set** is a built-in Python data structure used to store a collection of **unique elements**.

The most important characteristic of a Set is that it does **not allow duplicate elements**.

For example:

```python
numbers = {1, 2, 3, 4}
```

Here, `numbers` is a Set containing four elements.

Unlike a List:

```python
numbers = [1, 2, 3, 4]
```

a Set does not use positions or indexes to organize its elements.

---

## Sets Do Not Contain Duplicate Elements

Consider this Set:

```python
numbers = {1, 2, 2, 3, 3, 3}
```

Python automatically removes the duplicates.

If you display it:

```python
print(numbers)
```

you will get a Set containing only the unique values:

```text
{1, 2, 3}
```

This makes Sets especially useful when you need to work with unique values.

For example:

```python
names = {"Ali", "Sara", "Ali", "Reza", "Sara"}

print(names)
```

The result contains each name only once.

---

## Sets Are Unordered

Sets do not provide index-based ordering like Lists or Tuples.

For example, with a List:

```python
numbers = [10, 20, 30]

print(numbers[0])
```

we can access the first element.

But this does **not** work with a Set:

```python
numbers = {10, 20, 30}

print(numbers[0])
```

You will get an error because Sets do not support indexing.

So you should think about Sets differently:

```text
List / Tuple
    ↓
Ordered collection
    ↓
Index-based access

Set
    ↓
Collection of unique elements
    ↓
No index-based access
```

The main purpose of a Set is not to preserve positions.

---

## Creating an Empty Set

There is an important detail when creating an empty Set.

This:

```python
empty = {}
```

does **not** create an empty Set.

It creates an empty Dictionary.

To create an empty Set, use:

```python
empty = set()
```

You can verify this:

```python
print(type(empty))
```

The result will be:

```text
<class 'set'>
```

Compare that with:

```python
empty = {}

print(type(empty))
```

which produces:

```text
<class 'dict'>
```

This is a very common beginner mistake.

---

## Sets Can Contain Different Data Types

A Set can contain multiple types of hashable values:

```python
data = {10, "Python", 3.14, True}
```

However, the elements of a Set must be **hashable**.

For now, you can think of hashable values as values that Python can safely use as unique Set elements.

Common examples include:

* integers;
* floats;
* strings;
* booleans;
* tuples containing hashable elements.

Lists cannot be Set elements:

```python
numbers = {[1, 2], [3, 4]}
```

because Lists are mutable and therefore unhashable.

We will study this concept more carefully later when we discuss `frozenset` and Set behavior.

---

## Why Use Sets?

Sets are particularly useful when you need to:

### Remove duplicates

```python
numbers = [1, 2, 2, 3, 3, 4]

unique_numbers = set(numbers)

print(unique_numbers)
```

### Check membership

```python
languages = {"Python", "Java", "C++"}

print("Python" in languages)
```

The result is:

```text
True
```

### Compare collections

Sets provide operations such as:

* Union
* Intersection
* Difference
* Symmetric Difference

These operations become especially useful when comparing groups of data.

For example:

```text
Students who study Python
        ∩
Students who study Java
```

can represent:

> Students who study both Python and Java.

We will explore these operations in later parts.

---

## Set vs List vs Tuple

It is important to understand the difference between the three structures we have studied so far.

| Feature      | List               | Tuple            | Set             |
| ------------ | ------------------ | ---------------- | --------------- |
| Ordered      | Yes                | Yes              | No              |
| Indexing     | Yes                | Yes              | No              |
| Duplicates   | Allowed            | Allowed          | Not allowed     |
| Mutable      | Yes                | No               | Yes             |
| Main purpose | General collection | Fixed collection | Unique elements |

For example:

```python
numbers_list = [1, 2, 2, 3]
numbers_tuple = (1, 2, 2, 3)
numbers_set = {1, 2, 2, 3}
```

The List and Tuple keep the duplicate `2`.

The Set automatically keeps only one `2`.

---

## A Practical Example

Imagine that you collect the names of students who attended several classes.

For the first class:

```python
python_students = {"Ali", "Sara", "Reza"}
```

For the second class:

```python
java_students = {"Sara", "Reza", "Mina"}
```

Later, we may want to answer questions such as:

* Who attended at least one class?
* Who attended both classes?
* Who attended Python but not Java?
* Which students are unique to each class?

Sets are designed specifically for this type of problem.

The answers can be found using Set Operations, which we will study in the upcoming parts.

---

## Key Takeaways

At this point, remember these core ideas:

1. A Set stores **unique elements**.
2. Duplicate elements are automatically removed.
3. Sets do not support index-based access.
4. `{}` creates an empty Dictionary, not an empty Set.
5. Use `set()` to create an empty Set.
6. Sets are especially useful for membership checking and comparing collections.
7. Set elements must be hashable.
8. Set Operations such as Union and Intersection are important tools for working with collections of unique data.

In the next part, we will learn the different ways to **create Sets** in Python.
