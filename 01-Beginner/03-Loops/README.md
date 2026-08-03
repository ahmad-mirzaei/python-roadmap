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

