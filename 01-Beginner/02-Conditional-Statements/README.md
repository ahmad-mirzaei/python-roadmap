# Part 1 — What Is a Conditional Statement?

🌐 Language: **English** | [فارسی](fa/README.md)

Not every program should perform the same actions every time it runs.

Sometimes, a program needs to make a decision.

For example:

- Should a user be allowed to log in?
- Should a student pass an exam?
- Should a customer receive a discount?
- Should a game continue or end?

Before making a decision, a program must check one or more conditions.

This is called a **conditional statement**.

---

## A Real-World Example

Imagine you are standing at the entrance of a movie theater.

The theater has a simple rule:

> Only people who are **18 years old or older** can enter.

Before allowing someone to enter, the staff checks the person's age.

If the person is 18 or older, they may enter.

Otherwise, they cannot.

Programs work in exactly the same way.

They first check a condition, then decide what to do.

<p align="center">
  <img src="images/Cinema-Age-Check-Flowchart.png" width="800" alt="Cinema-Age-Check-Flowchart">
</p>

<p align="center">
  <em>A real-world example of a conditional decision.</em>
</p>

---

## What Is a Condition?

A condition is simply a question that has only two possible answers:

- Yes
- No

In Python, these answers are represented as:

- `True`
- `False`

Example:

```
Is 20 greater than 18?
```

Answer:

```
True
```

Another example:

```
Is 10 greater than 50?
```

Answer:

```
False
```

Python uses these answers to decide which code should run.

---

## Where Are Conditional Statements Used?

Conditional statements are everywhere.

For example:

- Login systems
- ATM machines
- Online stores
- Mobile applications
- Video games

Almost every real-world application uses conditions.

---

## In the Next Part

In the next part, you will learn the first conditional statement in Python:

```python
if
```

---

# Part 2 — The `if` Statement

Now that you know what a conditional statement is, it's time to write one in Python.

Python uses the `if` statement to make decisions.

The word `if` simply means:

> "If this condition is true, do something."

---

## Basic Syntax

```python
if condition:
    statement
```

There are two important things to notice:

- A colon (`:`) appears at the end of the first line.
- The code inside the `if` statement is indented.

Both are required in Python.

---

## How the `if` Statement Works

Python follows these steps:

1. Read the condition.
2. Check whether it is `True` or `False`.
3. If it is `True`, execute the indented code.
4. If it is `False`, skip the indented code.

---

## Example

Imagine the movie theater from the previous section.

The rule is:

> People who are 18 or older may enter.

In Python:

```python
age = 36

if age >= 18:
    print("You can enter the movie theater.")
```

Output:

```text
You can enter the movie theater.
```

Since the condition is `True`, Python executes the `print()` statement.

---

## Another Example

```python
age = 15

if age >= 18:
    print("You can enter the movie theater.")
```

Output:

```text
```

Nothing is printed because the condition is `False`.

Python simply skips the code inside the `if` statement.

---

## Important Note

An `if` statement only performs an action when the condition is `True`.

If the condition is `False`, nothing happens.

In the next part, you will learn how to tell Python what to do when the condition is `False`.

---

