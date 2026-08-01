# Part 1 — Variables

🌐 Language: **English** | [فارسی](fa/README.md)

Every day, we store things in containers.

For example, imagine you have a box on your desk.

You write the word **Books** on the box.

Whenever you buy a new book, you put it inside that box.

Later, if someone asks where your books are, you simply answer:

> "They're in the **Books** box."

The label helps you identify what is stored inside without opening the box.

Programming works in a very similar way.

Instead of storing books, we store information.

Instead of using a physical label, we use a **variable name**.

---

## What Is a Variable?

A **variable** is a name used to store a value.

You can think of a variable as a labeled box.

- The label is the variable's name.
- The content inside the box is the value.

For example:

```python
name = "Ahmad"
```

Here:

- `name` is the label on the box.
- `"Ahmad"` is the value stored inside the box.
- The `=` operator places the value into the variable.

---

Let's look at another example.

```python
age = 25
```

Now imagine another box.

Its label is **age**, and inside it is the number **25**.

Every variable has a name and stores a value.

---

## Why Do We Need Variables?

Imagine writing a program without variables.

Every time you needed a person's name, age, or country, you would have to write the actual value again and again.

Variables allow us to store information once and reuse it whenever we need it.

This makes our programs easier to read, easier to maintain, and much more flexible.

---

## Part Summary

- A variable stores information.
- A variable has a name and a value.
- Think of a variable as a labeled box.
- The `=` operator assigns a value to a variable.

# Part 2 — Naming Variables

Choosing good variable names is an important programming skill.

A clear variable name makes your code easier to read and understand.

Imagine opening a program that contains variables like this:

```python
a = "Ahmad"
b = 25
c = "Canada"
```

Can you tell what `a`, `b`, or `c` represent?

Probably not.

Now compare it with:

```python
name = "Ahmad"
age = 25
country = "Canada"
```

Even without any explanation, the purpose of each variable is immediately clear.

This is why choosing meaningful names is important.

---

## Rules for Naming Variables

Python has a few simple rules for variable names.

### Rule 1 — A variable name must start with a letter or an underscore.

✔ Valid

```python
name = "Ahmad"
_age = 25
```

✘ Invalid

```python
2name = "Ahmad"
```

---

### Rule 2 — A variable name can contain letters, numbers, and underscores.

✔ Valid

```python
student_name = "Ahmad"
score1 = 95
```

✘ Invalid

```python
student-name = "Ahmad"
```

The hyphen (`-`) is treated as the subtraction operator.

---

### Rule 3 — Variable names are case-sensitive.

These are three different variables:

```python
name = "Ahmad"
Name = "Bob"
NAME = "Charlie"
```

Python treats each one as a separate variable.

---

## Best Practices

Good variable names describe the data they store.

Good examples:

```python
first_name
last_name
email
phone_number
price
```

Avoid names like:

```python
a
x
temp1
abc
```

unless they are used for short examples or temporary values.

---

## Part Summary

- Choose meaningful variable names.
- Follow Python's naming rules.
- Variable names are case-sensitive.
- Good names make programs easier to read.

# Part 3 — String Data Type

Not all information is made of numbers.

Sometimes we want to store text, such as a person's name, country, or email address.

In Python, text is stored using the **String** data type.

---

## What Is a String?

A **string** is a sequence of characters enclosed in quotation marks.

For example:

```python
name = "Ahmad"
```

Here, `"Ahmad"` is a string.

Python knows it is text because it is enclosed in quotation marks.

---

## More Examples

```python
country = "Iran"
```

```python
city = "Shiraz"
```

```python
email = "Ahmad@example.com"
```

All of these values are strings because they represent text.

---

## Quotation Marks

Python allows you to use either double quotation marks (`" "`) or single quotation marks (`' '`).

Both examples below are valid:

```python
language = "Python"
```

```python
language = 'Python'
```

Choose one style and use it consistently throughout your code.

---

## When Should You Use Strings?

Use strings whenever you need to store text.

Examples include:

- Names
- Cities
- Countries
- Email addresses
- Messages

---

> 💡 **Tip**
>
> Even if a value contains numbers, it is still a string if it is enclosed in quotation marks.
>
> Example:
>
> ```python
> code = "12345"
> ```
>
> This is text, not a number.

---

## Common Beginner Mistake

Beginners sometimes forget to place text inside quotation marks.

Incorrect:

```python
name = Ahmad
```

Correct:

```python
name = "Ahmad"
```

Without quotation marks, Python thinks `Ahmad` is the name of another variable.

---

## Part Summary

- A string stores text.
- Strings must be enclosed in quotation marks.
- Python accepts both single and double quotation marks.
- Text without quotation marks is not treated as a string.