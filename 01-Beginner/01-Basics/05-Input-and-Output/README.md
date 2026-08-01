# Part 1 — Getting Information from Users

So far, you have created programs that use information already written inside the code.

For example:

```python
name = "Ahmad"
age = 25
```

The values are fixed.

If another person wants to use the program, the code needs to be changed manually.

Real programs usually need to receive information from users.

---

## A Real-World Example

Imagine a registration form on a website.

The website does not already know:

- Your name
- Your email
- Your age

Instead, it asks you to enter this information.

The website then uses your answers to create your account.

Python programs work in a similar way.

They can ask users for information and use that information while the program is running.

---

## Static vs Dynamic Information

Compare these two approaches.

### Static information:

```python
name = "Ahmad"
```

The value is already written in the program.

### Dynamic information:

```python
name = get_information_from_user()
```

The program receives the value from the user.

Dynamic programs are more flexible because they can work with different users.

---

## Why Do We Need User Input?

User input allows programs to:

- Ask questions
- Personalize responses
- Work with different users
- React to user choices

Examples:

- A login system asks for a username.
- A calculator asks for numbers.
- A game asks for player choices.

---

## Part Summary

- Programs can use fixed information or user information.
- Real applications usually receive data from users.
- User input makes programs more flexible.

# Part 2 — The input() Function

In the previous part, you learned why programs need information from users.

Now we will learn how Python receives that information.

Python uses the `input()` function to ask the user for data.

---

## What Is input()?

The `input()` function pauses the program and waits for the user to type something.

For example:

```python
name = input("Enter your name: ")
```

When Python runs this code, it displays:

```text
Enter your name:
```

The program waits until the user enters a value.

---

## A Real-World Example

Think about an ATM machine.

An ATM does not already know your password.

It asks:

> "Please enter your password."

The machine waits for your answer and then uses that information.

The `input()` function works in a similar way.

It asks the user a question and receives the answer.

---

## Understanding the Code

Look at this example:

```python
name = input("Enter your name: ")
```

There are two parts:

### The message

```python
"Enter your name: "
```

This is the question shown to the user.

### The input value

The answer typed by the user is stored inside:

```python
name
```

The variable keeps the information so the program can use it later.

---

## Another Example

```python
country = input("Where do you live? ")
```

The program asks a question.

The user's answer is stored in the variable:

```python
country
```

---

## Important Note

For now, remember this:

The `input()` function receives information from the user.

Later, you will learn how to work with different types of input, such as numbers.

---

## Part Summary

- `input()` receives information from the user.
- The program waits until the user enters a value.
- The result can be stored inside a variable.
- User input makes programs interactive.

