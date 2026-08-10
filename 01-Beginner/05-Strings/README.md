# Lesson — Strings & Sequences

> 🌐 language: **English** | [فارسی](fa/README.md)

## Part 1 — What Is a String?

A **string** is a sequence of characters.

Characters can be:

* Letters
* Numbers
* Spaces
* Symbols

In Python, strings are written inside quotation marks.

For example:

```python
name = "Python"
language = 'Python'
```

Both forms create a string.

---

## Creating a String

We can use either single quotes or double quotes:

```python
message = "Hello, Python!"
```

or:

```python
message = 'Hello, Python!'
```

Python treats both as strings.

---

## Strings Can Contain Different Characters

A string is not limited to letters.

For example:

```python
text = "Hello123"
```

This is a string containing letters and numbers.

We can also have spaces:

```python
text = "Hello World"
```

And symbols:

```python
text = "Python @ 2026!"
```

All of these are strings.

---

## Empty Strings

A string can also contain no characters.

```python
empty = ""
```

This is called an **empty string**.

Its length is zero.

---

## Strings Are Sequences

A string is an ordered sequence of characters.

For example:

```python
word = "Python"
```

Conceptually:

```text
P  y  t  h  o  n
```

Each character has a position.

This position is called an **index**.

We will learn how to use indexes in the next sections.

---

## Checking the Type

We can use `type()` to see what kind of value we have:

```python
name = "Python"

print(type(name))
```

Output:

```text
<class 'str'>
```

`str` is Python's built-in type for strings.

---

## Important

Strings are **immutable** in Python.

That means once a string has been created, its individual characters cannot be changed directly.

For example, this is not allowed:

```python
word = "Python"

word[0] = "J"
```

Python will raise an error.

Instead, we create a new string:

```python
word = "Python"

word = "J" + word[1:]

print(word)
```

Output:

```text
Jython
```

We will explore this idea more when we learn indexing and slicing.

---

## Algorithmic Thinking

Before moving on, think about this:

Suppose you have a user's name:

```python
name = "Ahmad"
```

How could you determine:

1. How many characters the name contains?
2. What the first character is?
3. What the last character is?
4. Whether a specific character exists in the name?

We will answer these questions step by step throughout this Lesson.

---

## Summary

A string:

* Is a sequence of characters.
* Is written inside quotes.
* Can contain letters, numbers, spaces, and symbols.
* Can be empty.
* Has an order.
* Has indexes.
* Uses the `str` type.
* Is immutable.

In the next section, we will learn how to **access individual characters using indexes**.

---

