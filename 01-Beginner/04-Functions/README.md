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

# Part 3 — Parameters

A function can receive information from outside.

This information allows the function to work with different values each time it is called.

The variables that receive these values inside the function are called **parameters**.

---

## A Real-World Example

Imagine an ATM machine.

The ATM itself is the same machine every time.

But the amount of money you request can be different.

One person may request:

```
100 Toman
```

Another person may request:

```
500 Toman
```

The ATM uses the given amount to perform the operation.

In Python, parameters work in the same way.

They allow a function to receive different values.

---

## Basic Syntax

```python
def function_name(parameter):
    # function body
```

The parameter is a variable that receives a value when the function is called.

---

## Example

```python
def greet(name):
    print("Hello", name)
```

The function has one parameter called `name`.

Now we can provide different values:

```python
greet("Ahmad")
```

Output:

```text
Hello Ahmad
```

Another call:

```python
greet("Sara")
```

Output:

```text
Hello Sara
```

---

## Multiple Parameters

A function can have more than one parameter.

Example:

```python
def introduce(name, age):
    print(name)
    print(age)
```

Calling the function:

```python
introduce("Ahmad", 36)
```

Output:

```text
Ahmad
36
```

---

## Important Note

Parameters are created when we define a function.

The actual values are provided when we call the function.

The next part will explain these values in detail: **Arguments**.

---

# Part 4 — Arguments

In the previous part, you learned about **parameters**.

Now we need to understand another important concept: **arguments**.

A parameter and an argument are related, but they are not the same thing.

---

## What Is an Argument?

An **argument** is the actual value that we provide when we call a function.

For example:

```python
def greet(name):
    print("Hello", name)
```

Here, `name` is a **parameter**.

When we call the function:

```python
greet("Ahmad")
```

`"Ahmad"` is an **argument**.

---

## Parameter vs Argument

Think about it this way:

```python
def greet(name):
```

`name` is a placeholder.

It tells the function:

> "I will receive a value here."

But when we write:

```python
greet("Ahmad")
```

we provide the actual value.

So:

| Term      | Meaning                                                    |
| --------- | ---------------------------------------------------------- |
| Parameter | A variable defined in the function definition.             |
| Argument  | The actual value passed to the function when it is called. |

---

## Multiple Arguments

A function can receive multiple arguments.

```python
def introduce(name, age):
    print("Name:", name)
    print("Age:", age)
```

Now we can call the function:

```python
introduce("Ahmad", 36)
```

Output:

```text
Name: Ahmad
Age: 36
```

Here:

* `name` is a parameter.
* `age` is a parameter.
* `"Ahmad"` is an argument.
* `36` is an argument.

---

## A Simple Way to Remember

You can think of a parameter as an **empty box**.

The argument is the **value that you put inside the box**.

```text
Parameter → Empty box
Argument  → Value inside the box
```

This distinction becomes especially useful when you start working with functions that have many parameters.

---

# Part 5 — The `return` Statement

Until now, our functions have performed actions such as printing messages.

But sometimes we want a function to **calculate something and give the result back to us**.

This is where the `return` statement becomes useful.

---

## What Does `return` Do?

The `return` statement sends a value from a function back to the place where the function was called.

For example:

```python
def add(a, b):
    return a + b
```

When we call the function:

```python
result = add(5, 3)
```

The function calculates:

```text
5 + 3 = 8
```

and returns `8`.

The value is then stored in the `result` variable.

```python
print(result)
```

Output:

```text
8
```

---

## `print()` vs `return`

One of the most important things to understand is the difference between `print()` and `return`.

Consider this function:

```python
def add(a, b):
    print(a + b)
```

Calling it:

```python
result = add(5, 3)
```

The function prints:

```text
8
```

But `result` does not contain `8`.

Now look at this version:

```python
def add(a, b):
    return a + b
```

Calling it:

```python
result = add(5, 3)
```

Now `result` contains `8`.

So:

| `print()`                          | `return`                                   |
| ---------------------------------- | ------------------------------------------ |
| Displays a value on the screen.    | Sends a value back from the function.      |
| Mainly used to show information.   | Used when we need to use the result later. |
| Does not return the printed value. | Returns a value to the caller.             |

---

## A Real-World Example

Imagine using a calculator.

You enter:

```text
36 + 14
```

The calculator performs the calculation and gives you:

```text
50
```

You can then use that result in another calculation.

For example:

```text
50 × 2 = 100
```

A function with `return` works in a similar way.

It performs a task and **gives the result back**, so we can use that result somewhere else.

---

## Using the Returned Value

A returned value does not have to be printed immediately.

We can store it in a variable:

```python
def multiply(a, b):
    return a * b

result = multiply(6, 4)

print(result)
```

Output:

```text
24
```

We can also use the returned value directly:

```python
print(multiply(6, 4))
```

Output:

```text
24
```

Or use it in another calculation:

```python
result = multiply(6, 4)

final_result = result + 10

print(final_result)
```

Output:

```text
34
```

---

## `return` Ends the Function

When Python reaches a `return` statement, the function immediately stops executing.

For example:

```python
def test():
    print("Start")
    return
    print("End")
```

Calling the function:

```python
test()
```

Output:

```text
Start
```

The `"End"` message is never printed because the function stopped when it reached `return`.

---

## Returning Multiple Values

A function can also return more than one value.

For example:

```python
def calculate(a, b):
    return a + b, a * b
```

We can store both results:

```python
sum_result, multiply_result = calculate(5, 3)
```

Now:

```python
print(sum_result)
print(multiply_result)
```

Output:

```text
8
15
```

---

## Important Note

Remember this simple rule:

> `print()` shows a value.
> `return` gives a value back.

This difference is extremely important because returned values can be stored, reused, compared, or used in other calculations.

<p align="center">
  <img src="images/return-flowchart.png" width="800" alt="return-flowchart">
</p>

<p align="center">
  <em>Figure 2. The flow of receiving input, executing a function, and returning a result with the <code>return</code> statement.</em>
</p>

---

