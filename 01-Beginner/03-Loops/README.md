# Part 1 — What Are Loops?

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

