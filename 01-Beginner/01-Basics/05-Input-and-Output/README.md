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