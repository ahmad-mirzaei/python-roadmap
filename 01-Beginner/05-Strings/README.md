# Lesson — Strings & Sequences

> 🌐 language: **English** | [فارسی](fa/README.md)

# Part 1 — What Is a String?

Until now, we have learned about variables, data types, user input, conditions, loops, and functions.

Now we will learn about one of the most important data types in Python:

**String**

Strings are everywhere in real programs.

Examples:

* User names
* Passwords
* Email addresses
* Messages
* File names
* Text documents
* Information entered through forms

Understanding strings is not just about learning a few commands. It is about understanding how Python stores and works with text.

---

# 1. What Is a String?

A **string** is a sequence of characters.

A character can be:

* A letter
* A number
* A space
* A symbol

In Python, strings are created by placing text inside quotation marks.

Example:

```python
name = "Python"
```

Here:

```text
Python
```

is a string.

Python stores the characters in a specific order.

---

# 2. What Is a Character?

A string is made of smaller parts called **characters**.

Example:

```python
word = "Python"
```

This string contains six characters:

```text
P   y   t   h   o   n
```

Each character is a separate value inside the string.

Spaces are also characters.

Example:

```python
message = "Hello World"
```

The space between `Hello` and `World` is also a character.

So this string contains:

```text
H e l l o _ W o r l d
```

The `_` represents the space character.

---

# 3. Strings Can Contain Different Types of Characters

A string is not limited to letters.

## Letters

```python
language = "Python"
```

## Numbers

```python
number_text = "12345"
```

Important:

`"12345"` is not a number.

It is text containing number characters.

Compare:

```python
a = 12345
b = "12345"
```

The first value is an integer.

The second value is a string.

Python treats them differently.

---

# 4. Difference Between `"123"` and `123`

This is one of the most important concepts when working with strings.

Example:

```python
a = 123
b = "123"
```

Although they look similar, they have different data types.

Check their types:

```python
print(type(a))
print(type(b))
```

Output:

```text
<class 'int'>
<class 'str'>
```

The first value is a number.

The second value is text.

---

## Working With Numbers

A number can be used in calculations:

```python
age = 20

print(age + 5)
```

Output:

```text
25
```

Because Python understands that `age` is a number.

---

## Working With Strings

A string behaves differently:

```python
age = "20"

print(age + "5")
```

Output:

```text
205
```

Python joins the two strings together.

This process is called **concatenation**.

---

But this causes an error:

```python
age = "20"

print(age + 5)
```

Why?

Because Python cannot add:

```text
"20" + 5
```

A string and a number are different types.

---

# 5. Checking Data Types With `type()`

Python provides a built-in function called:

```python
type()
```

This function tells us the data type of a value.

Example:

```python
print(type(10))
```

Output:

```text
<class 'int'>
```

---

Example with a decimal number:

```python
print(type(10.5))
```

Output:

```text
<class 'float'>
```

---

Example with a string:

```python
print(type("Python"))
```

Output:

```text
<class 'str'>
```

---

Example with a boolean:

```python
print(type(True))
```

Output:

```text
<class 'bool'>
```

---

# 6. Why Is `type()` Important?

Sometimes a value looks like one thing but actually has another type.

For example:

```python
age = input("Enter your age: ")

print(type(age))
```

The user enters:

```text
20
```

But the output is:

```text
<class 'str'>
```

Why?

Because the `input()` function always returns a string.

Python receives:

```python
age = "20"
```

not:

```python
age = 20
```

---

# 7. Converting Input Values

Because `input()` returns a string, we often need to convert the value.

Example:

Wrong:

```python
age = input("Enter your age: ")

print(age + 5)
```

The program fails.

Correct:

```python
age = int(input("Enter your age: "))

print(age + 5)
```

Now Python converts:

```text
"20"
```

into:

```text
20
```

and calculations work correctly.

---

Common conversions:

```python
int("100")
```

Converts string to integer.

---

```python
float("10.5")
```

Converts string to decimal number.

---

```python
str(100)
```

Converts a value into a string.

---

# 8. Empty Strings

A string can contain no characters.

Example:

```python
text = ""
```

This is called an **empty string**.

Its length is zero.

However:

```python
text = " "
```

is different.

This contains one character:

a space.

---

# 9. Strings Are Sequences

A string is a sequence because its characters have an order.

Example:

```python
word = "Python"
```

Conceptually:

```text
P   y   t   h   o   n
```

The order matters.

These are different strings:

```python
"Python"

"nohtyP"
```

They contain the same characters, but the order is different.

Because strings are sequences, we can:

* Access individual characters
* Slice parts of strings
* Loop through characters
* Find the length of strings

We will learn these concepts in the next sections.

---

# 10. Index Concept

Because strings are sequences, every character has a position.

Example:

```python
word = "Python"
```

Positions:

```text
Character:  P   y   t   h   o   n
Index:      0   1   2   3   4   5
```

Important:

Python indexes start from zero.

The first character is index `0`.

The last character is index `5`.

We will study indexing deeply in the next section.

---

# 11. Strings Are Immutable

Strings in Python are **immutable**.

Immutable means:

> After a string is created, its characters cannot be changed directly.

Example:

```python
word = "Python"

word[0] = "J"
```

This produces an error.

Python does not allow changing a single character inside an existing string.

---

Instead, we create a new string:

```python
word = "Python"

word = "J" + word[1:]

print(word)
```

Output:

```text
Jython
```

The original string was not modified.

A new string was created.

This concept becomes very important when we learn slicing and string methods.

---

# Short Exercises

## Exercise 1

Predict the type of each variable:

```python
a = "100"
b = 100
c = 10.5
d = True
e = "True"
```

---

## Exercise 2

Predict the output:

```python
x = "10"
y = "20"

print(x + y)
```

Then compare it with:

```python
x = 10
y = 20

print(x + y)
```

Explain the difference.

---

## Exercise 3

Write a program that receives a user's name and displays:

```text
Name:
Type:
```

---

## Exercise 4

Write a program that receives a user's age and displays their age after five years.

---

# End of Section Challenge

Create a program that receives:

* Name
* Age
* City

The program should:

1. Receive the user's name.
2. Receive the user's age.
3. Convert the age into the correct data type.
4. Receive the user's city.
5. Display the user's information.
6. Check whether the user is an adult.
7. Put the process inside a function.
8. Ask if another user should be added.

Example:

```text
Enter your name: Ali
Enter your age: 22
Enter your city: Tehran

Name: Ali
Age: 22
City: Tehran

You are an adult.

Add another user? yes
```

Before writing code:

**Analyze the problem and write the algorithm first.**
