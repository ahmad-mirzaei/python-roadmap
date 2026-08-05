# Part 1 — What Is a Function?

> 🌐 language: **English** | [فارسی](fa/README.md)

As programs become larger, writing everything in one place becomes difficult.

Some pieces of code perform the same task many times.

Instead of writing the same code again and again, we can place it inside a **function**.

A function is a reusable block of code that performs a specific task.

Once a function is created, it can be used whenever it is needed.

---

## A Real-World Example

Imagine a coffee machine.

You press the **Coffee** button.

The machine performs several steps automatically:

- Boil water.
- Grind coffee beans.
- Prepare the coffee.
- Pour it into the cup.

You only press one button.

You do not perform every step yourself.

A Python function works in the same way.

You call the function once, and Python executes all of the instructions inside it.

---

## Why Do We Use Functions?

Functions help us:

- Avoid writing the same code repeatedly.
- Make programs easier to read.
- Organize code into smaller parts.
- Make programs easier to maintain.

---

## A Simple Example

```python
def say_hello():
    print("Hello!")
```

Nothing happens yet.

The function has only been created.

To use it, we must call it.

```python
say_hello()
```

Output:

```text
Hello!
```

---

## Important Note

Creating a function and calling a function are two different things.

Creating defines what the function should do.

Calling tells Python to execute it.

---

<p align="center">
  <img src="images/function-concept.png" width="800" alt="function-concept">
</p>

<p align="center">
  <em>Figure 1. A function performs a specific task when it is called.</em>
</p>

---

# Part 2 — Defining a Function (`def`)

In Python, every function starts with the `def` keyword.

The word `def` is short for **define**, which means "to create" or "to define."

When Python sees the `def` keyword, it knows that a new function is being created.

---

## Basic Syntax

```python
def function_name():
    # function body
```

Every function has two main parts:

- **Function Header** → The line that starts with `def`.
- **Function Body** → The code that runs when the function is called.

---

## Your First Function

```python
def say_hello():
    print("Hello!")
```

This code only defines the function.

It does **not** execute it.

To run the function, you must call it.

```python
say_hello()
```

Output:

```text
Hello!
```

---

## Another Example

```python
def welcome():
    print("Welcome to Python!")
```

Calling the function:

```python
welcome()
```

Output:

```text
Welcome to Python!
```

---

## Important Note

Defining a function does not execute it.

A function runs only when it is called.

---

