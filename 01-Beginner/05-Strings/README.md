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

---

# Lesson — Strings & Sequences

# Part 2 — Creating Strings and Working with Quotes

In Part 1, we learned what strings are, how Python identifies them with the `str` type, how `input()` returns strings, and why strings are sequences.

Now we will learn how to create strings correctly and how quotation marks and escape characters work.

---

## 1. Creating Strings

The simplest way to create a string is to place text inside quotation marks.

Python allows us to use single quotes:

```python
name = 'Ali'
```

or double quotes:

```python
name = "Ali"
```

Both values are strings:

```python
print(type(name))
```

Output:

```text
<class 'str'>
```

The choice between single and double quotes usually depends on which one makes the text easier to write and read.

---

## 2. Single Quotes and Double Quotes

These two strings contain exactly the same text:

```python
a = "Python"
b = 'Python'
```

We can check:

```python
print(a == b)
```

Output:

```text
True
```

So Python does not consider one form more "string-like" than the other.

The important thing is that the opening and closing quotation marks match.

Correct:

```python
name = "Ali"
```

Correct:

```python
name = 'Ali'
```

Incorrect:

```python
name = "Ali'
```

The quotation marks must be properly paired.

---

## 3. Why Do We Have Two Types of Quotes?

The real advantage becomes clear when quotation marks themselves are part of our text.

Imagine we want to store:

```text
Python is "easy" to learn.
```

We can use single quotes around the entire string:

```python
message = 'Python is "easy" to learn.'
```

This works because Python sees the outer single quotes as the boundaries of the string.

We can also do the opposite:

```python
message = "Python is 'easy' to learn."
```

This is one of the simplest ways to avoid unnecessary escaping.

---

## 4. Quotes Inside Quotes

Consider this sentence:

```text
Ali said "Hello".
```

We can write:

```python
message = 'Ali said "Hello".'
```

Or:

```python
message = "Ali said \"Hello\"."
```

Both produce:

```text
Ali said "Hello".
```

The second example introduces an important concept: **escape characters**.

---

# 5. Escape Characters

An escape character allows us to represent characters or special behaviors that would otherwise be difficult to write inside a string.

The escape character in Python is:

```text
\
```

A backslash followed by another character creates a special sequence.

Some of the most useful ones are:

| Escape sequence | Meaning      |
| --------------- | ------------ |
| `\n`            | New line     |
| `\t`            | Tab          |
| `\\`            | Backslash    |
| `\"`            | Double quote |
| `\'`            | Single quote |

Let's look at them one by one.

---

# 6. New Line — `\n`

Normally:

```python
print("Hello Python")
```

produces:

```text
Hello Python
```

But `\n` tells Python to continue on a new line:

```python
print("Hello\nPython")
```

Output:

```text
Hello
Python
```

Notice that `\n` does not appear in the output.

It represents an instruction to move to the next line.

---

## A More Useful Example

```python
print("Name: Ali\nAge: 20\nCity: Tehran")
```

Output:

```text
Name: Ali
Age: 20
City: Tehran
```

This is useful when we want to format information without writing several separate `print()` statements.

---

# 7. Tab — `\t`

The `\t` escape sequence inserts a tab.

Example:

```python
print("Name:\tAli")
```

Output:

```text
Name:   Ali
```

A common use is creating simple columns:

```python
print("Name\tAge")
print("Ali\t20")
print("Sara\t22")
```

Output:

```text
Name    Age
Ali     20
Sara    22
```

The exact visual width of a tab can depend on the environment, but conceptually it moves the text to the next tab position.

---

# 8. Double Quote — `\"`

Suppose we want to use double quotes inside a string that is already surrounded by double quotes.

This would cause a problem:

```python
message = "Python is "easy" to learn."
```

Python interprets the second `"` as the end of the string.

Instead, escape the inner quotes:

```python
message = "Python is \"easy\" to learn."
```

Now the quotation marks become part of the text.

Output:

```text
Python is "easy" to learn.
```

---

# 9. Single Quote — `\'`

The same idea works with single quotes.

This causes a problem:

```python
message = 'Python's syntax is simple.'
```

Python thinks the string ends after `Python`.

We can escape the apostrophe:

```python
message = 'Python\'s syntax is simple.'
```

Output:

```text
Python's syntax is simple.
```

However, there is an easier option:

```python
message = "Python's syntax is simple."
```

This is another reason having both single and double quotes is useful.

---

# 10. Backslash — `\\`

Because `\` has a special meaning, we cannot always write it directly when we want an actual backslash in the output.

For example, suppose we want to display a Windows-style path:

```text
C:\Users\Ali
```

We can write:

```python
path = "C:\\Users\\Ali"

print(path)
```

Output:

```text
C:\Users\Ali
```

Each `\\` represents one actual backslash.

---

# 11. Why Does Python Need Escape Characters?

Python needs a way to distinguish between:

**characters that belong to the text**

and

**characters that control how the text is interpreted.**

For example:

```python
"\n"
```

does not mean the two visible characters `\` and `n`.

It represents a new-line character.

Likewise:

```python
"\""
```

represents a double-quote character inside a string.

Understanding this distinction will become important later when working with files, paths, formatted text, and regular expressions.

---

# 12. Multi-line Strings

Sometimes we want a string to contain several lines.

Python allows triple quotes:

```python
message = """
Hello
Welcome to Python
Have a great day!
"""
```

The string can span multiple lines.

This is useful for:

* Long messages
* Multi-line text
* Documentation
* Large blocks of text

We can use either triple double quotes:

```python
message = """
Hello
Python
"""
```

or triple single quotes:

```python
message = '''
Hello
Python
'''
```

Both are valid.

---

# 13. A Common Source of Confusion

Look at this:

```python
text = "Hello\nWorld"
```

The string contains a special new-line character.

But look at:

```python
text = "Hello\\nWorld"
```

Here we escaped the backslash.

The output is:

```text
Hello\nWorld
```

The difference is important:

### First:

```python
"Hello\nWorld"
```

means:

```text
Hello
World
```

### Second:

```python
"Hello\\nWorld"
```

means the text:

```text
Hello\nWorld
```

So `\\` changes the meaning of the backslash itself.

---

# 14. Combining Everything

We can combine variables, strings, escape characters, and `print()`.

Example:

```python
name = "Ali"
age = 20
city = "Tehran"

print("Name:\t" + name)
print("Age:\t" + str(age))
print("City:\t" + city)
```

Output:

```text
Name:   Ali
Age:    20
City:   Tehran
```

Notice something important:

`age` is an integer.

Therefore, before using it with string concatenation, we convert it:

```python
str(age)
```

This connects directly to what we learned in Part 1 about data types.

---

# Short Exercises

## Exercise 1 — Predict the Output

Without running the code, predict the output:

```python
print("Python\nStrings")
```

---

## Exercise 2 — Fix the String

Fix this code:

```python
message = "Python is "easy" to learn."
```

The output should be:

```text
Python is "easy" to learn.
```

---

## Exercise 3 — Apostrophe

Fix this code:

```python
message = 'I don't like bugs.'
```

Make the program print:

```text
I don't like bugs.
```

---

## Exercise 4 — Formatting

Create a program that prints:

```text
Name:   Ali
Age:    20
City:   Tehran
```

Use `\t`.

---

## Exercise 5 — Multi-line String

Create one string that produces:

```text
Welcome to Python!

Today we are learning Strings.
```

Use `\n`.

---

## Exercise 6 — Path

Create a string that prints:

```text
C:\Python\Projects\Lesson1
```

Make sure the backslashes appear correctly.

---

# End of Section Challenge

Now combine the concepts from previous lessons with what you learned in this section.

Write a program that:

1. Is placed inside a function.
2. Receives the user's name.
3. Receives the user's age.
4. Receives the user's city.
5. Converts the age to an integer.
6. Checks whether the user is an adult.
7. Creates a formatted multi-line message.
8. Uses `\n` and `\t` somewhere in the output.
9. Asks whether the user wants to enter another user.
10. Continues until the user chooses to stop.

Example output:

```text
Name:   Ali
Age:    22
City:   Tehran

Status: Adult

Add another user? yes
```

### Important

Do **not** copy the example directly into your program.

First break the problem into smaller steps and write the algorithm.

The goal of this challenge is not simply to practice strings.

It is to combine:

* Variables
* `input()`
* Type conversion
* Strings
* `print()`
* Conditions
* Loops
* Functions

into one small program.

---

## What We Learned

In this section, we learned:

* How to create strings
* Single vs double quotes
* Quotes inside strings
* Escape characters
* `\n`
* `\t`
* `\\`
* `\"`
* `\'`
* Multi-line strings
* Formatting text with escape sequences
* Combining strings with variables
* Converting values with `str()`

In the next section, we will learn how to access individual characters using **Indexing**.

---

