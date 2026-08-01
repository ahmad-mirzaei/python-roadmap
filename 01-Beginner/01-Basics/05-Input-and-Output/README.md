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

# Part 3 — Storing User Input in Variables

In the previous part, you learned that the `input()` function receives information from users.

But receiving information is only the first step.

A program also needs a way to remember that information.

Python stores user input inside variables.

---

## A Real-World Example

Imagine filling out a registration form.

You type your name:

```
Ahmad
```

The website does not just read your name and forget it.

It stores your information so it can use it later.

Python programs work in a similar way.

They store the user's answers inside variables.

---

## Storing Input

Look at this example:

```python
name = input("Enter your name: ")
```

When the user enters:

```text
Ahmad
```

Python stores that value inside the variable:

```python
name
```

Now the program remembers the user's name.

---

## Using Stored Information

After storing information, the program can use it later.

Example:

```python
name = input("Enter your name: ")

print(name)
```

If the user enters:

```text
Ahmad
```

The output will be:

```text
Ahmad
```

The program displays the value stored inside the variable.

---

## Multiple Inputs

A program can store different pieces of information in different variables.

Example:

```python
name = input("Enter your name: ")
country = input("Enter your country: ")
```

Now the program has two separate pieces of information:

- The user's name
- The user's country

Each value has its own variable.

---

## Why Store User Input?

Storing information allows programs to:

- Use data later.
- Create personalized messages.
- Make decisions based on user information.

Without storing input, the program would receive information and immediately lose it.

---

## Part Summary

- User input can be stored inside variables.
- Each variable can store a different piece of information.
- Stored information can be used later in the program.

# Part 4 — Working with User Input

In the previous parts, you learned how to receive information from users and store it in variables.

Now let's look at how Python handles that information.

---

## Input Is Stored as Text

When Python receives information using `input()`, it stores the result as text.

For example:

```python
age = input("Enter your age: ")
```

If the user enters:

```text
25
```

Python stores it as:

```text
"25"
```

It looks like a number, but Python sees it as text.

---

## A Real-World Example

Imagine receiving a phone number.

A phone number contains digits:

```
09121234567
```

But it is not a number that you calculate with.

You do not add two phone numbers together.

It is information represented using digits.

This is why some values that contain numbers are still treated as text.

---

## Why Does This Matter?

Imagine this code:

```python
age = input("Enter your age: ")

next_year = age + 1
```

A beginner may expect:

```
25 + 1 = 26
```

But Python does not see `age` as a number.

It sees:

```
"25" + 1
```

These are different types of information.

Python needs to know that we want to perform a mathematical operation.

---

## Working with Different Types

Programs often need to convert information from one type to another.

For example:

- Text to a number
- Number to text

This process is called **type conversion**.

We will learn how to do this in the next part.

---

## Part Summary

- `input()` receives information as text.
- Numbers entered by users are still stored as text.
- Different data types may need to be converted before use.

