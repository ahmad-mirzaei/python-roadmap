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

