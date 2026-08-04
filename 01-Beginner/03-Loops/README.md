# Part 1 — What Are Loops?

> 🌐 language: **English** | [فارسی](fa/README.md)


In programming, we often need to repeat the same action multiple times.

Writing the same code again and again is not efficient.

Loops allow us to repeat a block of code automatically.

---

## Why Do We Need Loops?

Imagine you want to print a message five times.

Without a loop:

```python
print("Hello")
print("Hello")
print("Hello")
print("Hello")
print("Hello")
```

This works, but it creates unnecessary repetition.

If we need to repeat the action 100 or 1000 times, writing the code manually becomes difficult.

Loops solve this problem.

---

## What Is a Loop?

A loop is a programming structure that repeats a block of code while a specific condition is true or for a specific number of times.

A loop has three main parts:

1. Starting point
2. Condition or repetition rule
3. Code that should be repeated

---

## How Loops Work

The general process of a loop:

```
Start

    Check the condition

        If condition is true:
            Run the code

        Repeat the process

    If condition is false:
        Stop

End
```

The program keeps repeating the instructions until the loop finishes.

---

## Real-world Example

Think about a daily alarm.

Every day:

1. Check the current time.
2. If it is the alarm time, ring the alarm.
3. Wait until the next day.
4. Repeat the process.

This repeated process is similar to how loops work in programming.

---

## First Look at Loops

A simple example of a loop:

```python
for i in range(5):
    print("Hello")
```

Output:

```text
Hello
Hello
Hello
Hello
Hello
```

We will learn how `for` and `range()` work in the next parts.

---

# Part 2 — The `while` Loop

## What Is a `while` Loop?

A `while` loop repeats a block of code as long as a specific condition is `True`.

The loop continues running until the condition becomes `False`.

---

## Basic Syntax

```python
while condition:
    statement
```

Python checks the condition before each repetition.

- If the condition is `True`, the code inside the loop runs.
- If the condition is `False`, the loop stops.

---

## Example

```python
count = 1

while count <= 5:
    print(count)
    count = count + 1
```

Output:

```text
1
2
3
4
5
```

---

## How Does This Code Work?

At the beginning, the variable has this value:

```python
count = 1
```

Python checks the condition:

```python
count <= 5
```

The result is:

```text
True
```

So the code inside the loop runs.

After printing the value, the variable increases:

```python
count = count + 1
```

The value changes:

```text
1 → 2 → 3 → 4 → 5 → 6
```

When `count` becomes `6`, the condition becomes:

```text
False
```

The loop stops.

---

## Real-world Example

Imagine filling a water tank.

The process is:

1. Check the water level.
2. If the tank is not full, add more water.
3. Check the level again.
4. Repeat until the tank is full.

This repeated process is similar to how a `while` loop works.

---

## Important Note

A `while` loop needs a condition that eventually becomes `False`.

If the condition never changes, the loop continues forever.

Example:

```python
while True:
    print("Running...")
```

This is called an **infinite loop**.

---

# Part 3 — The `for` Loop

## What Is a `for` Loop?

A `for` loop is used to repeat a block of code for a specific number of times or to go through a sequence of values.

Unlike a `while` loop, a `for` loop usually has a clear number of repetitions.

---

## Basic Syntax

```python
for variable in sequence:
    statement
```

Python takes each value from the sequence and runs the code block once for each value.

---

## Simple Example

```python
for number in range(5):
    print(number)
```

Output:

```text
0
1
2
3
4
```

The loop runs five times.

---

## How Does This Code Work?

The `range(5)` function creates a sequence of numbers:

```text
0, 1, 2, 3, 4
```

During each repetition:

First:

```python
number = 0
```

Then:

```python
number = 1
```

Then:

```python
number = 2
```

The process continues until all values are used.

---

## Looping Through a List

A `for` loop can also go through items inside a list.

Example:

```python
names = ["Ali", "Sara", "John"]

for name in names:
    print(name)
```

Output:

```text
Ali
Sara
John
```

The loop takes each item from the list and executes the code.

---

## `for` Loop vs `while` Loop

| `for` Loop | `while` Loop |
|---|---|
| Used when the number of repetitions is known | Used when repetition depends on a condition |
| Works with sequences | Works with conditions |
| Usually stops automatically | Needs a condition to become `False` |

Example:

Use `for` when you know the number of repetitions:

```python
for i in range(10):
    print(i)
```

Use `while` when you wait for a condition:

```python
while password != "1234":
    print("Try again")
```

---

## Important Note

A `for` loop does not need a manual counter update.

Python automatically moves to the next item in the sequence.

---

# Part 4 — The `range()` Function

## What Is `range()`?

The `range()` function is used to create a sequence of numbers.

It is commonly used with `for` loops when we need to repeat code a specific number of times.

---

## Basic Syntax

```python
range(stop)
```

The sequence starts from `0` and stops before the specified number.

Example:

```python
for number in range(5):
    print(number)
```

Output:

```text
0
1
2
3
4
```

Notice that `5` is not included.

---

## Using `range()` With Start and Stop

We can define where the sequence starts and where it stops.

Syntax:

```python
range(start, stop)
```

Example:

```python
for number in range(2, 6):
    print(number)
```

Output:

```text
2
3
4
5
```

The starting value is included, but the stopping value is not included.

---

## Using `range()` With Step

We can also control the difference between numbers.

Syntax:

```python
range(start, stop, step)
```

Example:

```python
for number in range(0, 10, 2):
    print(number)
```

Output:

```text
0
2
4
6
8
```

The `step` value determines how much the number changes after each repetition.

---

## Counting Backwards

The `step` value can also be negative.

Example:

```python
for number in range(5, 0, -1):
    print(number)
```

Output:

```text
5
4
3
2
1
```

---

## Common Mistake

A common mistake is forgetting that the stop value is not included.

Example:

```python
range(1, 5)
```

Creates:

```text
1, 2, 3, 4
```

Not:

```text
1, 2, 3, 4, 5
```

---

## Summary

The `range()` function has three common forms:

```python
range(stop)

range(start, stop)

range(start, stop, step)
```

It is one of the most useful tools when working with `for` loops.

---

# Part 5 — Nested Loops

Sometimes, one loop is not enough.

There are situations where we need a loop inside another loop.

This is called a **nested loop**.

A nested loop simply means:

> A loop that runs inside another loop.

---

## A Real-World Example

Imagine a school with several classrooms.

Each classroom contains multiple students.

To visit every student, you would:

1. Enter a classroom.
2. Visit every student in that classroom.
3. Move to the next classroom.
4. Repeat the process.

This is exactly how nested loops work.

The outer loop moves between classrooms.

The inner loop visits every student inside each classroom.

---

## Basic Syntax

```python
for item1 in sequence1:
    for item2 in sequence2:
        statement
```

The inner loop finishes completely before the outer loop continues.

---

## Example

```python
for row in range(3):
    for column in range(3):
        print(row, column)
```

Output:

```text
0 0
0 1
0 2
1 0
1 1
1 2
2 0
2 1
2 2
```

For every value of `row`, Python executes the entire inner loop.

---

## Important Note

The outer loop controls how many times the inner loop starts.

The inner loop always completes before the next iteration of the outer loop begins.

---

# Part 6 — The `break` Statement

Normally, a loop continues until it finishes all of its iterations.

However, sometimes we want to stop the loop immediately.

Python provides the `break` statement for this purpose.

The word **break** means:

> "Exit the loop immediately."

---

## A Real-World Example

Imagine you are searching for a book on a bookshelf.

You check the books one by one.

As soon as you find the book you want, you stop searching.

There is no reason to continue checking the remaining books.

The `break` statement works exactly like this.

---

## Basic Syntax

```python
for item in sequence:
    if condition:
        break
```

When Python reaches `break`, the loop ends immediately.

---

## Example

```python
for number in range(1, 11):
    if number == 6:
        break

    print(number)
```

Output:

```text
1
2
3
4
5
```

When `number` becomes `6`, Python exits the loop.

The remaining numbers are never processed.

---

## Another Example

```python
password = ""

while True:
    password = input("Enter the password: ")

    if password == "python":
        print("Access granted.")
        break
```

The loop continues until the correct password is entered.

---

## Important Note

`break` stops only the loop that it belongs to.

If it is inside a nested loop, only the inner loop will stop.

---

<p align="center">
  <img src="images/break-flowchart.png" width="800" alt="break-flowchart">
</p>

<p align="center">
  <em>Figure 6. Immediate termination of a loop using the <code>break</code> statement.</em>
</p>

---

# Part 7 — The `continue` Statement

In the previous part, you learned that the `break` statement stops a loop immediately.

But sometimes we do not want to stop the loop.

Instead, we simply want to skip the current iteration and continue with the next one.

Python uses the `continue` statement for this purpose.

The word **continue** means:

> "Skip the rest of the current iteration and continue with the next one."

---

## A Real-World Example

Imagine a teacher is checking students' homework.

One student is absent.

Instead of stopping the attendance process, the teacher simply skips that student and continues checking the remaining students.

The `continue` statement works exactly the same way.

---

## Basic Syntax

```python
for item in sequence:
    if condition:
        continue

    statement
```

When Python reaches `continue`, it skips the remaining code in the current iteration and immediately starts the next iteration.

---

## Example

```python
for number in range(1, 11):

    if number == 6:
        continue

    print(number)
```

Output:

```text
1
2
3
4
5
7
8
9
10
```

The number `6` is skipped, but the loop continues normally.

---

## Another Example

```python
for letter in "PYTHON":

    if letter == "H":
        continue

    print(letter)
```

Output:

```text
P
Y
T
O
N
```

Python skips the letter `H` and continues with the remaining letters.

---

## Important Note

Unlike `break`, the `continue` statement does **not** stop the loop.

It only skips the current iteration.

---

<p align="center">
  <img src="images/continue-flowchart.png" width="800" alt="continue-flowchart">
</p>

<p align="center">
  <em>Figure 7. Skipping the current iteration using the <code>continue</code> statement.</em>
</p>

---

# Part 8 — Comparing `break` and `continue`

Both `break` and `continue` are used inside loops.

However, they behave differently.

---

## `break`

The `break` statement stops the entire loop immediately.

Python exits the loop and continues with the first statement after the loop.

Example:

```python
for number in range(1, 6):
    if number == 3:
        break

    print(number)
```

Output:

```text
1
2
```

---

## `continue`

The `continue` statement does **not** stop the loop.

Instead, it skips the current iteration and continues with the next one.

Example:

```python
for number in range(1, 6):
    if number == 3:
        continue

    print(number)
```

Output:

```text
1
2
4
5
```

---

## Comparison Table

| Statement | What it does |
|-----------|--------------|
| `break` | Stops the entire loop immediately. |
| `continue` | Skips the current iteration and continues with the next one. |

---

## Important Note

If you want to end the loop completely, use `break`.

If you only want to ignore one iteration, use `continue`.

---

