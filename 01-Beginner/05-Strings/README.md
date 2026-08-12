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

# Part 3 — String Indexing

In the previous sections, we learned what strings are and how to create them using different types of quotation marks.

We also learned about escape characters such as `\n`, `\t`, `\\`, `\"`, and `\'`.

Now we are going to work with one of the most important features of strings:

**Indexing**

Indexing allows us to access individual characters inside a string.

---

## 1. What Is Indexing?

A string is a sequence of characters.

For example:

```python
word = "Python"
```

We can imagine the string like this:

```text
P   y   t   h   o   n
```

Each character has a position.

In Python, these positions are called **indexes**.

The important rule is:

> Python starts counting indexes from `0`.

So the string looks like this:

```text
Character:  P   y   t   h   o   n
Index:      0   1   2   3   4   5
```

The first character is at index `0`, not `1`.

---

# 2. Accessing a Character

To access a specific character, we use square brackets:

```python
word[index]
```

For example:

```python
word = "Python"

print(word[0])
```

Output:

```text
P
```

We can access the second character:

```python
print(word[1])
```

Output:

```text
y
```

The third:

```python
print(word[2])
```

Output:

```text
t
```

And so on.

---

# 3. Why Does Python Start From Zero?

This can seem strange at first.

Why isn't the first character index `1`?

Because Python follows the common convention used by many programming languages and computer systems where sequence positions are represented as offsets from the beginning.

Think of the index as:

> How many steps do we move from the beginning?

The first character requires zero steps.

The second character requires one step.

The third character requires two steps.

So:

```text
Index:      0   1   2   3   4   5
Character:  P   y   t   h   o   n
            ↑
         start
```

This is why the first character is at index `0`.

---

# 4. Accessing the First Character

Because indexing starts at zero:

```python
word = "Python"

print(word[0])
```

gives:

```text
P
```

This pattern is extremely common.

Whenever you need the first character of a string:

```python
text[0]
```

---

# 5. Accessing the Last Character

There are two ways to access the last character.

We could calculate its index.

For `"Python"`:

```text
P   y   t   h   o   n
0   1   2   3   4   5
```

So:

```python
print(word[5])
```

prints:

```text
n
```

But this approach is not very practical.

What if the string changes?

```python
word = "Programming"
```

We would need to calculate the new last index.

Python provides a much better solution:

**Negative indexing.**

---

# 6. Negative Indexing

Python allows us to count from the end of a string using negative indexes.

Example:

```text
Character:  P   y   t   h   o   n
Positive:   0   1   2   3   4   5
Negative:  -6  -5  -4  -3  -2  -1
```

The last character always has index:

```python
-1
```

Therefore:

```python
word = "Python"

print(word[-1])
```

Output:

```text
n
```

The character before it:

```python
print(word[-2])
```

Output:

```text
o
```

And:

```python
print(word[-3])
```

Output:

```text
h
```

Negative indexing is extremely useful when we need characters near the end of a string.

---

# 7. Positive and Negative Indexing Together

Consider:

```python
word = "Python"
```

We can visualize all indexes:

```text
             P    y    t    h    o    n
Positive:    0    1    2    3    4    5
Negative:   -6   -5   -4   -3   -2   -1
```

Notice:

```python
word[0] == word[-6]
```

and:

```python
word[5] == word[-1]
```

Both refer to the same character.

---

# 8. The `len()` Function

Sometimes we don't know how many characters a string contains.

Python provides:

```python
len()
```

to find the length of a string.

Example:

```python
word = "Python"

print(len(word))
```

Output:

```text
6
```

There are six characters in `"Python"`.

---

# 9. `len()` and Indexing Are Different

This is a very important distinction.

For:

```python
word = "Python"
```

we have:

```python
len(word)
```

which gives:

```text
6
```

But the last index is:

```text
5
```

Why?

Because the length counts the number of characters:

```text
6 characters
```

while indexes start at zero:

```text
0 1 2 3 4 5
```

Therefore:

> Last index = `len(string) - 1`

For example:

```python
word = "Python"

print(word[len(word) - 1])
```

Output:

```text
n
```

This is one of the most useful patterns when working with strings.

---

# 10. Getting the Last Character With `len()`

Instead of writing:

```python
word[5]
```

we can write:

```python
word[len(word) - 1]
```

This works even if the string changes.

For example:

```python
word = "Programming"

print(word[len(word) - 1])
```

Output:

```text
g
```

We do not need to know the length beforehand.

---

# 11. Indexing User Input

Indexing becomes much more useful when working with user input.

Example:

```python
name = input("Enter your name: ")

print(name[0])
```

If the user enters:

```text
Ali
```

the output is:

```text
A
```

We can also get the last character:

```python
print(name[-1])
```

Output:

```text
i
```

Now the program can work with information that the user provides.

---

# 12. Indexing Does Not Change the String

When we access a character:

```python
word = "Python"

letter = word[0]
```

we are only reading the character.

The original string remains unchanged.

```python
print(word)
```

still produces:

```text
Python
```

This is consistent with what we learned earlier about strings being **immutable**.

---

# 13. You Cannot Assign to an Index

Because strings are immutable, this is not allowed:

```python
word = "Python"

word[0] = "J"
```

Python raises an error.

You cannot directly replace one character inside an existing string.

Instead, you create a new string.

For example:

```python
word = "Python"

word = "J" + word[1:]

print(word)
```

Output:

```text
Jython
```

We will study this technique more deeply when we learn slicing.

---

# 14. IndexError

What happens if we try to access an index that does not exist?

Example:

```python
word = "Python"

print(word[10])
```

The string only has indexes:

```text
0 1 2 3 4 5
```

Index `10` does not exist.

Python raises:

```text
IndexError
```

This is called an **IndexError**.

---

# 15. Understanding the Error

Suppose:

```python
name = "Ali"
```

The valid indexes are:

```text
Character:  A   l   i
Index:      0   1   2
```

This works:

```python
print(name[0])
print(name[1])
print(name[2])
```

But this does not:

```python
print(name[3])
```

because index `3` is outside the valid range.

Remember:

```text
Valid indexes:
0 → first character
1 → second character
2 → third character
```

The length is `3`, but the last index is `2`.

---

# 16. A Useful Rule

For a string:

```python
text
```

the valid positive indexes are:

```text
0
through
len(text) - 1
```

The valid negative indexes are:

```text
-1
through
-len(text)
```

This rule helps us understand why an `IndexError` happens.

---

# 17. Checking Before Accessing

Suppose we want to access the first character of user input:

```python
name = input("Enter your name: ")

print(name[0])
```

What if the user enters nothing?

Then:

```python
name = ""
```

The string has no characters.

Trying:

```python
name[0]
```

will cause an `IndexError`.

We can prevent this by checking first:

```python
name = input("Enter your name: ")

if len(name) > 0:
    print(name[0])
else:
    print("You entered an empty string.")
```

This is a good example of combining:

* Strings
* `len()`
* Conditions
* Indexing

---

# 18. Indexing and Loops

Because strings are sequences, we can combine indexing with loops.

For example:

```python
word = "Python"

for i in range(len(word)):
    print(word[i])
```

Output:

```text
P
y
t
h
o
n
```

Here:

```python
range(len(word))
```

generates the indexes:

```text
0 1 2 3 4 5
```

and:

```python
word[i]
```

accesses the character at each index.

This connects the current lesson with the loops and `range()` concepts we learned earlier.

---

# 19. A More Practical Example

Let's ask the user for a word and display its first and last characters:

```python
word = input("Enter a word: ")

if len(word) > 0:
    print("First character:", word[0])
    print("Last character:", word[-1])
else:
    print("The string is empty.")
```

If the user enters:

```text
Python
```

the output is:

```text
First character: P
Last character: n
```

This is a small but realistic example of how indexing can be used in a program.

---

# Short Exercises

## Exercise 1

What is the output?

```python
word = "Python"

print(word[0])
print(word[3])
print(word[-1])
```

---

## Exercise 2

Find the last character without using a negative index:

```python
word = "Programming"
```

Use `len()`.

---

## Exercise 3

What is the output?

```python
text = "Hello"

print(text[-2])
print(text[-5])
```

---

## Exercise 4

How many characters does this string contain?

```python
text = "Hello World"
```

Remember that the space is also a character.

---

## Exercise 5

Predict whether each line works or raises an error:

```python
text = "Python"

print(text[0])
print(text[5])
print(text[6])
print(text[-1])
print(text[-6])
print(text[-7])
```

---

## Exercise 6

Write a program that receives a user's name and displays:

```text
First character: A
Last character: i
```

For example, if the user enters:

```text
Ali
```

---

## Exercise 7

Write a program that receives a word and displays every character on a separate line.

Do not use a direct `for character in word` loop.

Use indexing and `range()`.

---

## Exercise 8

Write a program that receives a word and prints its first character only if the user entered something.

If the input is empty, display:

```text
The string is empty.
```

---

# End of Section Challenge

Now combine the concepts from the previous lessons with indexing.

Create a program that:

1. Is placed inside a function.
2. Receives a user's name.
3. Receives the user's age.
4. Converts the age to an integer.
5. Receives the user's city.
6. Checks whether the user is an adult.
7. Displays the first character of the user's name.
8. Displays the last character of the user's name.
9. Displays the length of the user's name.
10. Handles an empty name without causing an error.
11. Asks whether another user should be entered.
12. Continues until the user chooses to stop.

Example:

```text
Name:   Ali
Age:    22
City:   Tehran

First character: A
Last character: i
Name length: 3

Status: Adult

Add another user? yes
```

### Algorithmic Thinking

Before writing the code, think about the problem step by step:

```text
Start
↓
Get user information
↓
Check whether the name is empty
↓
If it is not empty:
    Find first character
    Find last character
    Find length
↓
Check age
↓
Display information
↓
Ask whether another user should be added
↓
If yes → repeat
If no → finish
```

Do not copy this algorithm directly into code.

First understand each step, then decide which Python tools you need.

You should recognize several concepts from previous lessons:

* Variables
* `input()`
* `int()`
* Strings
* `type()`
* `len()`
* Indexing
* `if`
* `for`
* `range()`
* Functions
* Loops

This is exactly the kind of combination we will continue building throughout the book.

---

# What We Learned

In this section, we learned:

* What indexing means
* Why Python indexes start from `0`
* How to access characters with `[]`
* Positive indexing
* Negative indexing
* How to access the first character
* How to access the last character
* The `len()` function
* The relationship between length and the last index
* `IndexError`
* How to prevent indexing errors
* Indexing user input
* Indexing inside loops
* Combining indexing with `range()`
* Why indexing does not modify a string
* How indexing connects to string immutability

In the next section, we will move from accessing individual characters to accessing **multiple characters at once**.

That brings us to:

---

# Part 4 — String Slicing

In the previous section, we learned how to access a single character using indexing.

For example:

```python
word = "Python"

print(word[0])
```

Output:

```text
P
```

But what if we want to access **several characters at once**?

For example, suppose we have:

```text
Python
```

and we want:

```text
Pyt
```

or:

```text
hon
```

or even:

```text
nohtyP
```

This is where **slicing** becomes useful.

---

# 1. What Is Slicing?

Slicing means extracting a portion of a sequence.

Because strings are sequences, we can slice them.

The basic syntax is:

```python
text[start:stop]
```

For example:

```python
word = "Python"

print(word[0:3])
```

Output:

```text
Pyt
```

We started at index `0` and stopped **before** index `3`.

This leads to one of the most important rules in Python:

> The `start` index is included, but the `stop` index is excluded.

---

# 2. Understanding `start` and `stop`

Consider:

```python
word = "Python"
```

Indexes:

```text
Character:  P   y   t   h   o   n
Index:      0   1   2   3   4   5
```

Now:

```python
word[1:4]
```

means:

```text
Start at 1
Take 1
Take 2
Take 3
Stop before 4
```

So the result is:

```text
yth
```

Example:

```python
print(word[1:4])
```

Output:

```text
yth
```

---

# 3. Why Is `stop` Excluded?

At first, this rule can feel strange.

Why does:

```python
word[0:3]
```

give:

```text
Pyt
```

instead of:

```text
Pyth
```

Because slicing is designed around a very useful boundary system.

Think of the indexes as positions between characters:

```text
    0   1   2   3   4   5   6
    |   |   |   |   |   |   |
    P   y   t   h   o   n
```

The slice:

```python
word[0:3]
```

takes everything from boundary `0` up to boundary `3`.

That gives:

```text
P y t
```

This design makes calculating the size of a slice very convenient:

```text
number of characters = stop - start
```

For:

```python
word[1:4]
```

we get:

```text
4 - 1 = 3 characters
```

and indeed:

```text
yth
```

contains three characters.

---

# 4. Basic Slicing Examples

```python
word = "Python"

print(word[0:2])
print(word[1:4])
print(word[2:6])
```

Output:

```text
Py
yth
thon
```

Let's break them down:

```python
word[0:2]
```

gives:

```text
Py
```

```python
word[1:4]
```

gives:

```text
yth
```

```python
word[2:6]
```

gives:

```text
thon
```

---

# 5. Omitting `start`

We don't always need to write the `start` value.

For example:

```python
word = "Python"

print(word[:3])
```

Output:

```text
Pyt
```

When `start` is omitted, Python assumes:

```text
start = beginning of the string
```

So:

```python
word[:3]
```

is equivalent to:

```python
word[0:3]
```

---

# 6. Omitting `stop`

We can also omit `stop`.

Example:

```python
word = "Python"

print(word[3:])
```

Output:

```text
hon
```

When `stop` is omitted, Python continues to the end of the string.

So:

```python
word[3:]
```

means:

> Start at index `3` and continue until the end.

---

# 7. Omitting Both

What happens if we write:

```python
word[:]
```

?

It returns the entire string.

Example:

```python
word = "Python"

print(word[:])
```

Output:

```text
Python
```

This is sometimes useful when working with sequences or creating a copy of a sequence.

---

# 8. Slicing With Negative Indexes

Slicing also works with negative indexes.

Remember:

```text
Character:  P    y    t    h    o    n
Positive:   0    1    2    3    4    5
Negative:  -6   -5   -4   -3   -2   -1
```

Example:

```python
word = "Python"

print(word[-3:])
```

Output:

```text
hon
```

This means:

> Start at the third character from the end and continue to the end.

---

# 9. Negative `stop`

We can also use a negative stop value.

Example:

```python
word = "Python"

print(word[:-2])
```

Output:

```text
Pyth
```

Why?

The last two characters are:

```text
o
n
```

`[:-2]` means:

> Start from the beginning and stop before the second-to-last position.

---

# 10. Combining Positive and Negative Indexes

We can combine them.

Example:

```python
word = "Python"

print(word[1:-1])
```

Output:

```text
ytho
```

Let's visualize it:

```text
Character:  P    y    t    h    o    n
Index:      0    1    2    3    4    5
Negative:  -6   -5   -4   -3   -2   -1
```

Start:

```text
1 → y
```

Stop:

```text
-1 → n
```

But `stop` is excluded.

Therefore:

```text
y t h o
```

---

# 11. The Third Part: `step`

So far we have used:

```python
text[start:stop]
```

But slicing has another optional value:

```python
text[start:stop:step]
```

The `step` controls how many positions Python moves at a time.

Example:

```python
word = "Python"

print(word[0:6:1])
```

Output:

```text
Python
```

A step of `1` means:

> Move one character at a time.

---

# 12. Step of 2

Now:

```python
word = "Python"

print(word[0:6:2])
```

Output:

```text
Pto
```

Why?

Indexes visited:

```text
0 → P
2 → t
4 → o
```

So:

```text
P t o
```

---

# 13. Step of 3

Example:

```python
word = "Python"

print(word[0:6:3])
```

Output:

```text
Ph
```

Indexes:

```text
0 → P
3 → h
```

So the result is:

```text
Ph
```

---

# 14. A Simple Way to Understand `step`

Think of `step` as the size of the jump.

```text
step = 1
→ take every character

step = 2
→ take every second character

step = 3
→ take every third character
```

For:

```text
Python
```

we have:

```text
Index:  0  1  2  3  4  5
        P  y  t  h  o  n
```

With:

```python
word[::2]
```

we get:

```text
P t o
```

---

# 15. Omitting `start` and `stop` With `step`

We can omit both:

```python
word[::2]
```

This means:

> Start at the beginning, go to the end, and move by 2.

Example:

```python
word = "Python"

print(word[::2])
```

Output:

```text
Pto
```

---

# 16. Reverse a String With `[::-1]`

One of the most useful slicing techniques is:

```python
[::-1]
```

Example:

```python
word = "Python"

print(word[::-1])
```

Output:

```text
nohtyP
```

Why?

Because the step is:

```text
-1
```

A negative step tells Python to move backward.

So:

```python
[::-1]
```

means:

> Start from the end and move backward one character at a time.

---

# 17. Understanding `[::-1]`

The original:

```text
P y t h o n
```

is traversed in reverse:

```text
n o h t y P
```

So:

```python
word[::-1]
```

returns:

```text
nohtyP
```

This is one of the most common Python slicing patterns.

---

# 18. Other Negative Steps

The negative step doesn't have to be `-1`.

Example:

```python
word = "Python"

print(word[::-2])
```

Output:

```text
nhy
```

The indexes are traversed backward:

```text
5 → n
3 → h
1 → y
```

Result:

```text
nhy
```

---

# 19. Important: A Negative Step Changes the Direction

Compare:

```python
word[::2]
```

and:

```python
word[::-2]
```

The first moves forward:

```text
0 → 2 → 4
```

The second moves backward:

```text
5 → 3 → 1
```

So:

```python
word[::2]
```

and:

```python
word[::-2]
```

are not simply "the same thing with a negative number".

They traverse the sequence in opposite directions.

---

# 20. Slicing Does Not Modify the Original String

Just like indexing, slicing does not modify the original string.

Example:

```python
word = "Python"

part = word[0:3]

print(part)
print(word)
```

Output:

```text
Pyt
Python
```

The original string remains unchanged.

This is another consequence of strings being immutable.

---

# 21. Slicing and Assignment

We can assign the result of a slice to another variable:

```python
word = "Python"

first_part = word[:3]
second_part = word[3:]

print(first_part)
print(second_part)
```

Output:

```text
Pyt
hon
```

We have effectively divided the string into two parts.

---

# 22. Rebuilding a String With Slicing

Because strings cannot be modified directly, slicing can help us create a new version.

Suppose:

```python
word = "Python"
```

and we want:

```text
Jython
```

We cannot do:

```python
word[0] = "J"
```

Instead:

```python
word = "J" + word[1:]
```

Now:

```python
print(word)
```

produces:

```text
Jython
```

We created a new string from:

```text
"J"
```

plus:

```text
"ython"
```

---

# 23. Extracting Parts of User Input

Slicing becomes especially useful with user input.

Example:

```python
name = input("Enter your name: ")

print("First three characters:", name[:3])
```

If the user enters:

```text
Alexander
```

the output is:

```text
First three characters: Ale
```

This can be useful when processing real text.

---

# 24. Slicing and `len()`

We can combine slicing with `len()`.

For example:

```python
word = "Python"

middle = word[1:len(word)-1]

print(middle)
```

Output:

```text
ytho
```

We removed the first and last characters.

A simpler version is:

```python
word[1:-1]
```

Both approaches demonstrate the same idea.

---

# 25. Slicing With Loops

Slicing can also be used together with loops.

Example:

```python
word = "Python"

for i in range(len(word)):
    print(word[i:])
```

Output:

```text
Python
ython
thon
hon
on
n
```

Here each iteration starts the slice at a different index.

This is a good example of how concepts from different sections can work together.

---

# 26. Common Slicing Mistakes

### Mistake 1 — Expecting `stop` to be included

```python
word = "Python"

print(word[0:3])
```

Some beginners expect:

```text
Pyth
```

But the result is:

```text
Pyt
```

Remember:

> `start` is included. `stop` is excluded.

---

### Mistake 2 — Confusing length with last index

For:

```python
word = "Python"
```

we have:

```text
len(word) = 6
```

but:

```text
last index = 5
```

---

### Mistake 3 — Forgetting that `step` can change direction

```python
word[::2]
```

moves forward.

```python
word[::-2]
```

moves backward.

---

### Mistake 4 — Thinking slicing changes the original string

It does not.

```python
part = word[:3]
```

creates another string value.

The original remains unchanged.

---

# Short Exercises

## Exercise 1

What is the output?

```python
word = "Python"

print(word[1:4])
```

---

## Exercise 2

What is the output?

```python
word = "Programming"

print(word[:4])
print(word[4:])
```

---

## Exercise 3

What is the output?

```python
word = "Python"

print(word[-3:])
print(word[:-3])
```

---

## Exercise 4

What is the output?

```python
word = "Python"

print(word[::2])
```

---

## Exercise 5

What is the output?

```python
word = "Python"

print(word[::-1])
```

---

## Exercise 6

Without running the code, predict:

```python
word = "Programming"

print(word[1:-1])
```

---

## Exercise 7

Create a program that receives a word and prints:

* The first half
* The second half

Hint:

Use `len()` and slicing.

---

## Exercise 8

Create a program that receives a word and prints it in reverse.

Do not use a loop.

Use slicing.

---

## Exercise 9

Create a program that receives a word and prints every second character.

For example:

```text
Input:
Python

Output:
Pto
```

---

## Exercise 10

Create a program that receives a username and displays:

```text
First 3 characters:
Last 3 characters:
Reversed:
```

Use slicing for all three.

---

# End of Section Challenge

Now combine everything we have learned so far.

Create a program that:

1. Is placed inside a function.
2. Receives a user's name.
3. Receives the user's age.
4. Converts the age to an integer.
5. Receives the user's city.
6. Checks whether the user is an adult.
7. Displays the length of the name.
8. Displays the first character.
9. Displays the last character.
10. Displays the first three characters.
11. Displays the last three characters.
12. Displays the name reversed.
13. Handles an empty name safely.
14. Asks whether another user should be entered.
15. Continues until the user chooses to stop.

Example:

```text
Name:   Alexander
Age:    22
City:   Tehran

Name length: 9
First character: A
Last character: r
First 3 characters: Ale
Last 3 characters: der
Reversed: rednaxelA

Status: Adult

Add another user? yes
```

### Algorithmic Thinking

Before writing the code, break the problem into smaller steps.

Ask yourself:

1. What information do I need?
2. Which values should be converted to numbers?
3. What should happen if the name is empty?
4. How can I find the first character?
5. How can I find the last character?
6. How can I get the first three characters?
7. How can I get the last three characters?
8. How can I reverse the name?
9. Where should the condition go?
10. Where should the loop go?
11. Where should the function go?

The goal is not to memorize:

```python
[::-1]
```

The goal is to understand **why** we use it.

---

# What We Learned

In this section, we learned:

* What String Slicing is
* `start`
* `stop`
* Why `stop` is excluded
* `text[start:stop]`
* Omitting `start`
* Omitting `stop`
* Omitting both
* Positive indexes in slicing
* Negative indexes in slicing
* `step`
* Positive steps
* Negative steps
* `[::-1]`
* Reversing strings
* Using `len()` with slicing
* Combining slicing with loops
* Rebuilding strings using slicing
* Common slicing mistakes
* Using slicing with user input

The next section will move from extracting characters to **working with the content of strings**.

---

# Part 5 — String Methods

> 🌐 Language: **English** | [فارسی](fa/README.md)

## 1. What Is a String Method?

In the previous sections, we learned how to create strings, access characters using indexing, and extract parts of strings using slicing.

Now we will learn how to **process strings** using string methods.

A string method is an operation that belongs to a string object.

```python
text = "python"

print(text.upper())
```

Output:

```text
PYTHON
```

Here:

* `text` is the string object.
* `upper()` is a string method.
* `.` connects the object to its method.

The general structure is:

```python
string.method()
```

Some methods also accept arguments:

```python
string.method(argument)
```

For example:

```python
text = "hello world"

print(text.replace("world", "Python"))
```

Output:

```text
hello Python
```

---

## 2. Function vs Method

We have already used functions such as:

```python
len(text)
```

`len()` is a **function**.

But:

```python
text.upper()
```

uses a **method**.

The important difference is where the operation is called.

```python
# Function
len(text)

# Method
text.upper()
```

A function receives the object as an argument.

A method is called directly on the object.

You will see this distinction frequently in Python.

---

## 3. `upper()`

The `upper()` method converts letters to uppercase.

```python
text = "hello"

print(text.upper())
```

Output:

```text
HELLO
```

Another example:

```python
name = "alexander"

print(name.upper())
```

Output:

```text
ALEXANDER
```

### Does `upper()` change the original string?

No.

```python
text = "hello"

print(text.upper())
print(text)
```

Output:

```text
HELLO
hello
```

Strings are immutable, so `upper()` creates a new string.

If we want to save the result:

```python
text = text.upper()
```

Now `text` contains:

```text
HELLO
```

---

## 4. `lower()`

`lower()` converts letters to lowercase.

```python
text = "PYTHON"

print(text.lower())
```

Output:

```text
python
```

This is particularly useful when we want to compare text without worrying about uppercase and lowercase differences.

```python
answer = input("Continue? ")

if answer.lower() == "yes":
    print("Continuing...")
```

Now all of these inputs work:

```text
yes
YES
Yes
YeS
```

because they are converted to lowercase before comparison.

---

## 5. `capitalize()`

`capitalize()` makes the first character uppercase and converts the remaining characters to lowercase.

```python
text = "pYTHON"

print(text.capitalize())
```

Output:

```text
Python
```

Compare:

```python
text.upper()
```

with:

```python
text.capitalize()
```

For:

```text
python
```

`upper()` produces:

```text
PYTHON
```

while `capitalize()` produces:

```text
Python
```

---

## 6. `title()`

`title()` capitalizes the first character of each word.

```python
text = "hello world"

print(text.title())
```

Output:

```text
Hello World
```

For example:

```python
name = input("Enter your name: ")

print(name.title())
```

If the user enters:

```text
aLEXANDER hAMILTON
```

the result is:

```text
Alexander Hamilton
```

---

## 7. Comparing `upper()`, `lower()`, `capitalize()`, and `title()`

Suppose:

```python
text = "hello WORLD"
```

Then:

```python
text.upper()
```

produces:

```text
HELLO WORLD
```

```python
text.lower()
```

produces:

```text
hello world
```

```python
text.capitalize()
```

produces:

```text
Hello world
```

```python
text.title()
```

produces:

```text
Hello World
```

| Method         | Result                                 |
| -------------- | -------------------------------------- |
| `upper()`      | All uppercase                          |
| `lower()`      | All lowercase                          |
| `capitalize()` | First character uppercase              |
| `title()`      | First character of each word uppercase |

---

## 8. `strip()`

User input may contain unnecessary spaces.

For example:

```python
name = "   Alice   "
```

We can remove the spaces at the beginning and end with:

```python
name.strip()
```

Example:

```python
name = "   Alice   "

print(name.strip())
```

Output:

```text
Alice
```

This is very useful with `input()`:

```python
name = input("Enter your name: ").strip()
```

Now accidental spaces around the input are removed.

---

## 9. `lstrip()` and `rstrip()`

Sometimes we only want to remove spaces from one side.

`lstrip()` removes whitespace from the left side:

```python
text = "   Python   "

print(text.lstrip())
```

Result:

```text
Python   
```

`rstrip()` removes whitespace from the right side:

```python
text = "   Python   "

print(text.rstrip())
```

Result:

```text
   Python
```

Remember:

```text
strip()   → both sides
lstrip()  → left side
rstrip()  → right side
```

---

## 10. `replace()`

`replace()` replaces one piece of text with another.

Syntax:

```python
text.replace(old, new)
```

Example:

```python
text = "I like Java"

print(text.replace("Java", "Python"))
```

Output:

```text
I like Python
```

It can also replace individual characters:

```python
text = "banana"

print(text.replace("a", "o"))
```

Output:

```text
bonono
```

Every matching `a` is replaced.

---

## 11. `replace()` Does Not Modify the Original String

Just like `upper()`, `replace()` creates a new string.

```python
text = "I like Java"

text.replace("Java", "Python")

print(text)
```

The output is still:

```text
I like Java
```

If we want to keep the new value:

```python
text = text.replace("Java", "Python")
```

Now:

```text
I like Python
```

---

## 12. Limiting `replace()`

We can specify how many replacements should happen.

```python
text = "banana"

print(text.replace("a", "o", 1))
```

Output:

```text
bonana
```

Only the first matching `a` was replaced.

For example:

```python
text.replace("a", "o", 2)
```

produces:

```text
bonona
```

The third argument is the maximum number of replacements.

---

## 13. `find()`

`find()` searches for a substring and returns its index.

```python
text = "Python programming"

print(text.find("programming"))
```

Output:

```text
7
```

Why `7`?

Because `"programming"` starts at index `7`.

```text
P y t h o n   p r o g r a m m i n g
0 1 2 3 4 5 6 7 ...
```

---

## 14. What Happens When `find()` Finds Nothing?

If the substring does not exist, `find()` returns `-1`.

```python
text = "Python"

print(text.find("Java"))
```

Output:

```text
-1
```

This does not cause an error.

We can use it in a condition:

```python
text = "Python"

position = text.find("Java")

if position == -1:
    print("Java was not found")
```

Output:

```text
Java was not found
```

---

## 15. Combining `find()` and Slicing

We can combine concepts we have already learned.

```python
text = "Python programming"

position = text.find("programming")

print(text[position:])
```

Output:

```text
programming
```

Here we are combining:

1. `find()`
2. indexing
3. slicing

This is an important step toward algorithmic thinking: different tools can be combined to solve one problem.

---

## 16. `count()`

`count()` tells us how many times a substring occurs.

```python
text = "banana"

print(text.count("a"))
```

Output:

```text
3
```

Another example:

```python
text = "hello hello"

print(text.count("hello"))
```

Output:

```text
2
```

---

## 17. `startswith()`

`startswith()` checks whether a string begins with a specific value.

```python
text = "Python programming"

print(text.startswith("Python"))
```

Output:

```text
True
```

But:

```python
print(text.startswith("Java"))
```

produces:

```text
False
```

Because this method returns a Boolean value, it works naturally with `if`:

```python
username = input("Username: ")

if username.startswith("admin"):
    print("Administrative account")
```

---

## 18. `endswith()`

`endswith()` checks whether a string ends with a specific value.

```python
filename = "report.pdf"

print(filename.endswith(".pdf"))
```

Output:

```text
True
```

This is useful for checking file extensions:

```python
filename = input("Filename: ")

if filename.endswith(".pdf"):
    print("PDF file")
```

---

## 19. `isdigit()`

`isdigit()` checks whether all characters in a string are digits.

```python
text = "12345"

print(text.isdigit())
```

Output:

```text
True
```

But:

```python
text = "123a"

print(text.isdigit())
```

Output:

```text
False
```

This is useful when validating user input:

```python
age = input("Enter your age: ")

if age.isdigit():
    age = int(age)
    print("Age:", age)
else:
    print("Invalid age")
```

Notice that `input()` gives us a string, so we can use a string method before converting it to an integer.

---

## 20. `isalpha()`

`isalpha()` checks whether all characters are alphabetic.

```python
text = "Python"

print(text.isalpha())
```

Output:

```text
True
```

But:

```python
text = "Python3"

print(text.isalpha())
```

produces:

```text
False
```

because `3` is not a letter.

---

## 21. `isalnum()`

`isalnum()` returns `True` when all characters are letters or numbers.

```python
print("Python123".isalnum())
```

Output:

```text
True
```

But:

```python
print("Python 123".isalnum())
```

returns:

```text
False
```

because the space is neither a letter nor a number.

---

## 22. `isspace()`

`isspace()` checks whether all characters are whitespace.

```python
text = "   "

print(text.isspace())
```

Output:

```text
True
```

But:

```python
text = " Python "

print(text.isspace())
```

returns:

```text
False
```

This can help us detect input that contains only spaces.

---

## 23. `isupper()` and `islower()`

These methods check the case of a string.

```python
text = "PYTHON"

print(text.isupper())
```

Output:

```text
True
```

And:

```python
text = "python"

print(text.islower())
```

Output:

```text
True
```

For mixed case:

```python
text = "Python"

print(text.isupper())
print(text.islower())
```

Both results are:

```text
False
```

---

## 24. Converting vs Checking

This distinction is important.

These methods **convert** text:

```text
upper()
lower()
capitalize()
title()
```

These methods **check** text:

```text
isdigit()
isalpha()
isalnum()
isspace()
isupper()
islower()
```

The checking methods return a Boolean:

```text
True
```

or:

```text
False
```

---

## 25. Method Chaining

Methods can be chained together.

For example:

```python
name = "   aLEXANDER   "

print(name.strip().lower())
```

The operations happen from left to right:

```text
"   aLEXANDER   "
        ↓
strip()
        ↓
"aLEXANDER"
        ↓
lower()
        ↓
"alexander"
```

We can continue chaining:

```python
name.strip().lower().title()
```

Result:

```text
Alexander
```

This is called **method chaining**.

---

## 26. How to Read a Chained Expression

Consider:

```python
text.strip().lower().replace("python", "java")
```

Do not try to understand everything at once.

Read it from left to right:

```text
1. strip()
2. lower()
3. replace()
```

Each operation produces a new string.

That new string becomes the input for the next method.

---

## 27. Practical Example — Username Validation

We can combine several concepts to validate a username:

```python
username = input("Enter username: ").strip()

if username == "":
    print("Username cannot be empty")
elif not username.isalnum():
    print("Username can contain only letters and numbers")
else:
    print("Username accepted")
```

The process is:

```text
input
  ↓
strip
  ↓
check empty
  ↓
check characters
  ↓
display result
```

This is much closer to real programming than using each method in isolation.

---

## 28. Practical Example — Validating a Number

Because `input()` always returns a string, we can validate it before converting it:

```python
age = input("Enter your age: ").strip()

if age.isdigit():
    age = int(age)
    print("Your age is", age)
else:
    print("Please enter a valid number")
```

We are now combining:

* `input()`
* `strip()`
* `isdigit()`
* `if`
* `int()`

---

## 29. Practical Example — Searching Text

```python
message = input("Enter a message: ")

if message.lower().find("python") != -1:
    print("The message contains Python")
else:
    print("Python was not found")
```

Because we convert the message to lowercase first, the program can recognise:

```text
Python
python
PYTHON
PyThOn
```

as the same word for this search.

---

# Exercises

## Exercise 1 — Predict the Output

What will this program print?

```python
text = "python"

print(text.upper())
print(text.capitalize())
print(text.title())
```

---

## Exercise 2 — Whitespace

What will each line print?

```python
text = "   Hello World   "

print(text.strip())
print(text.lstrip())
print(text.rstrip())
```

---

## Exercise 3 — Searching and Counting

What is the output?

```python
text = "banana"

print(text.count("a"))
print(text.find("n"))
```

---

## Exercise 4 — Combining Methods

What will this print?

```python
text = "Python Programming"

print(text.lower().startswith("python"))
```

---

## Exercise 5 — Validation

Predict the output:

```python
text = "12345"

print(text.isdigit())
print(text.isalpha())
print(text.isalnum())
```

---

## Exercise 6 — Name Formatter

Write a program that:

1. asks the user for a name
2. removes unnecessary spaces
3. converts it to lowercase
4. converts it to title case
5. prints the final name

---

## Exercise 7 — Number Validation

Ask the user for a number as a string.

If it contains only digits, convert it to an integer.

Otherwise print:

```text
Invalid number
```

---

## Exercise 8 — Character Counter

Ask the user for a sentence and count:

* spaces
* `a`
* `e`
* `i`

---

## Exercise 9 — File Extension

Ask the user for a filename.

If it ends with:

```text
.py
```

print:

```text
Python file
```

Otherwise print:

```text
Not a Python file
```

---

## Exercise 10 — Username Validation

Write a program that asks for a username.

The username is valid only if:

* it is not empty
* it contains only letters and numbers
* it contains at least 5 characters

Display:

```text
Valid username
```

or:

```text
Invalid username
```

---

# Section Challenge — Text Analyzer

Create a program that receives a sentence and performs a small text analysis.

The program should:

1. receive a sentence using `input()`
2. remove unnecessary spaces from the beginning and end
3. check whether the sentence is empty
4. display the sentence in lowercase
5. display the sentence in uppercase
6. display the sentence in title case
7. display its length
8. count the number of spaces
9. count the number of occurrences of `a`
10. check whether it starts with `"I"`
11. check whether it ends with `"."`
12. ask the user for a word
13. search for that word
14. report whether the word was found
15. ask whether the user wants to analyse another sentence

### Important

Do **not** write the final solution immediately.

First design the algorithm.

For example:

```text
START
  ↓
Receive sentence
  ↓
Clean sentence
  ↓
Check whether it is empty
  ↓
Analyse sentence
  ↓
Display results
  ↓
Ask for search word
  ↓
Search for word
  ↓
Display result
  ↓
Ask whether to continue
  ↓
Repeat or STOP
```

The goal is not simply to memorise string methods.

The goal is to learn how to **combine methods and control structures to solve a problem**.

---

# Part 5 — Final Algorithmic Question

Before moving to the exercises section, solve this problem conceptually:

> Write a program that receives a sentence and determines whether it is a valid username-like text according to a set of rules.

The program should decide whether:

* the input is empty
* unnecessary spaces exist
* the input contains only letters and numbers
* the input has at least 5 characters
* the input starts with a specific prefix

### Your Task

Do not write the code yet.

First write the algorithm in plain language.

Then convert the algorithm into Python.

The important part is to show the transition:

```text
Problem
   ↓
Rules
   ↓
Algorithm
   ↓
Python code
```

We will implement and solve the final challenge in the next stage, **after the learner has had the opportunity to solve it independently**.

---

# Part 6 — String Formatting

So far, we have learned how to create Strings, access individual characters, extract parts of a String, and work with String Methods.

But there is another important question:

How can we create clean, readable, and professional output?

For example, imagine that our program stores:

name = "Ahmad"
age = 25
score = 92.5

We may want to display:

Name: Ahmad
Age: 25
Score: 92.5

This is where String Formatting becomes important.

---

## Why Do We Need String Formatting?

Programs constantly need to combine text with data.

For example:

- A game displays the player's score.
- A banking program displays the account balance.
- A registration program displays the user's name.
- A shopping program displays the product price.
- A school program displays student information.

We need a way to place values inside text in a clean and readable way.

Python provides several approaches for this.

The most important modern approach is:

f-string

---

# String Concatenation

The simplest way to combine Strings is using `+`.

For example:

first_name = "Ahmad"
last_name = "Ahmadi"

full_name = first_name + " " + last_name

print(full_name)

Output:

Ahmad Ahmadi

The `+` operator joins Strings together.

---

## Concatenating More Values

We can combine several Strings:

first_name = "Ahmad"
last_name = "Ahmadi"
city = "Tehran"

message = first_name + " " + last_name + " lives in " + city

print(message)

Output:

Ahmad Ahmadi lives in Tehran

This works, but the code can become difficult to read when there are many values.

---

# The Problem with Different Data Types

Consider:

age = 25

print("I am " + age + " years old.")

This produces an error.

Why?

Because:

"I am "

is a String, while:

age

is an Integer.

Python does not automatically combine an Integer with a String using `+`.

We need to convert the Integer:

age = 25

print("I am " + str(age) + " years old.")

Output:

I am 25 years old.

---

# The `str()` Function

The `str()` function converts a value into a String.

For example:

age = 25

text = str(age)

print(text)
print(type(text))

Output:

25
<class 'str'>

Before conversion:

age

was an Integer.

After:

str(age)

we have a String.

The same thing works with Floating-Point numbers:

score = 92.5

print("My score is " + str(score))

Output:

My score is 92.5

---

# Why Concatenation Can Become Difficult

Consider this:

name = "Ahmad"
age = 25
city = "Tehran"
score = 92.5

print(
    "My name is " + name +
    ", I am " + str(age) +
    " years old, I live in " + city +
    ", and my score is " + str(score) + "."
)

The program works, but the expression is long and difficult to maintain.

Python provides a cleaner solution.

---

# f-Strings

An f-string allows us to insert values directly inside a String.

The basic syntax is:

f"text {variable}"

For example:

name = "Ahmad"
age = 25

print(f"My name is {name} and I am {age} years old.")

Output:

My name is Ahmad and I am 25 years old.

Notice the `f` before the quotation mark:

f"..."

The variable goes inside curly braces:

{name}

and:

{age}

---

# Multiple Variables in an f-String

We can insert many variables:

name = "Ahmad"
age = 25
city = "Tehran"

print(f"My name is {name}, I am {age} years old, and I live in {city}.")

Output:

My name is Ahmad, I am 25 years old, and I live in Tehran.

---

# Expressions Inside `{}`

The content inside `{}` does not have to be only a variable.

We can put expressions there.

For example:

age = 25

print(f"Next year I will be {age + 1}.")

Output:

Next year I will be 26.

Another example:

a = 10
b = 20

print(f"The sum is {a + b}.")

Output:

The sum is 30.

We can also use functions:

name = "ahmad"

print(f"Hello {name.title()}!")

Output:

Hello Ahmad!

We can even use methods:

text = "python programming"

print(f"Uppercase: {text.upper()}")

Output:

Uppercase: PYTHON PROGRAMMING

This is an important idea:

The expression inside `{}` is evaluated by Python.

---

# Combining Previous Lessons with f-Strings

Now we can combine what we learned in previous sections.

Suppose:

text = "Python Programming"

We can use Indexing:

print(f"First character: {text[0]}")

Output:

First character: P

We can use Slicing:

print(f"First three characters: {text[:3]}")

Output:

First three characters: Pyt

We can use String Methods:

print(f"Lowercase: {text.lower()}")

Output:

Lowercase: python programming

We can use `len()`:

print(f"Length: {len(text)}")

Output:

Length: 18

This is exactly how different concepts start working together.

---

# Formatting Numbers

String Formatting becomes especially useful when working with numbers.

Suppose:

price = 19.987654

If we write:

print(f"Price: {price}")

Output:

Price: 19.987654

Maybe we only want two decimal places.

We can write:

print(f"Price: {price:.2f}")

Output:

Price: 19.99

The general structure is:

{value:.2f}

Here:

- `:` starts the formatting instructions.
- `.2` means two decimal places.
- `f` means fixed-point notation.

---

# More Examples with `.2f`

number = 10

print(f"{number:.2f}")

Output:

10.00

Another example:

number = 3.14159265

print(f"{number:.2f}")

Output:

3.14

And:

print(f"{number:.4f}")

Output:

3.1416

---

# Rounding and Formatting

Formatting a number to two decimal places changes how it is displayed.

For example:

number = 7.456

print(f"{number:.2f}")

Output:

7.46

The original variable is not changed:

number = 7.456

print(f"{number:.2f}")
print(number)

Output:

7.46
7.456

Formatting controls the representation shown in the output.

---

# Thousands Separator

Large numbers can be difficult to read.

For example:

population = 12500000

print(f"{population:,}")

Output:

12,500,000

We can combine the comma separator with decimal formatting:

number = 1234567.891

print(f"{number:,.2f}")

Output:

1,234,567.89

This is useful for:

- money
- population
- statistics
- large quantities
- financial data

---

# Percentage Formatting

Suppose:

rate = 0.875

If we write:

print(f"{rate}")

Output:

0.875

But perhaps we want:

87.5%

We can use `%` formatting:

print(f"{rate:.1%}")

Output:

87.5%

Python converts the value into a percentage and adds `%`.

Another example:

success_rate = 0.9234

print(f"Success rate: {success_rate:.2%}")

Output:

Success rate: 92.34%

---

# `.2f` vs `.2%`

These two formats are different.

For:

rate = 0.92

Using:

print(f"{rate:.2f}")

produces:

0.92

But:

print(f"{rate:.2%}")

produces:

92.00%

So:

`.2f`

means two decimal places.

`.2%`

means percentage with two decimal places.

---

# Formatting Positive and Negative Numbers

We can control how numbers appear.

For example:

profit = 2500

print(f"Profit: {profit:+}")

Output:

Profit: +2500

And:

loss = -500

print(f"Loss: {loss:+}")

Output:

Loss: -500

The `+` formatting option explicitly shows the sign.

---

# Width

Sometimes we want a value to occupy a certain amount of space.

For example:

name = "Ahmad"

print(f"{name:10}")

The String is placed inside a field with a width of 10 characters.

This becomes useful when creating tables.

---

# Left Alignment

Use `<` for left alignment.

name = "Ahmad"

print(f"{name:<10}")

The text is aligned to the left side of the field.

Conceptually:

Ahmad     

---

# Right Alignment

Use `>` for right alignment.

name = "Ahmad"

print(f"{name:>10}")

Conceptually:

     Ahmad

The text is aligned to the right.

---

# Center Alignment

Use `^` for center alignment.

name = "Ahmad"

print(f"{name:^10}")

The text is centered inside the field.

---

# Custom Fill Characters

We can choose what character fills the empty space.

For example:

name = "Ahmad"

print(f"{name:*<10}")

Output:

Ahmad*****

The `*` is the fill character.

We can also combine fill characters with alignment.

Right alignment:

print(f"{name:*>10}")

Output:

*****Ahmad

Center alignment:

print(f"{name:*^10}")

Output:

**Ahmad***

This can be useful for creating simple console interfaces.

---

# Formatting Numbers with Width

Width can also be used with numbers.

score = 95

print(f"{score:>10}")

The number is aligned to the right inside a field of width 10.

This is useful when displaying columns of numbers.

---

# Creating a Simple Table

Suppose:

name1 = "Ahmad"
score1 = 95

name2 = "Sara"
score2 = 88

We can write:

print(f"{'Name':<10}{'Score':>10}")
print(f"{name1:<10}{score1:>10}")
print(f"{name2:<10}{score2:>10}")

Output:

Name           Score
Ahmad             95
Sara              88

Now our output looks much more organized.

---

# Combining Width and Decimal Formatting

We can combine multiple formatting rules.

For example:

price = 1234.5678

print(f"{price:>15,.2f}")

Output:

       1,234.57

Here we have:

`>` → right alignment

`15` → field width

`,` → thousands separator

`.2f` → two decimal places

This is a good example of how multiple formatting instructions can work together.

---

# The General Structure of a Format Specifier

A simplified way to think about formatting is:

{value:[fill][align][width][,][.precision][type]}

Not every part is required.

For example:

{price:.2f}

Only precision and type are used.

Or:

{name:<10}

Alignment and width are used.

Or:

{number:,.2f}

Thousands separator and decimal precision are used.

Understanding the pieces makes more complicated formatting much easier.

---

# Formatting Strings with `format()`

Before f-strings became the preferred approach, Python programmers often used the `format()` method.

For example:

name = "Ahmad"
age = 25

print("My name is {} and I am {} years old.".format(name, age))

Output:

My name is Ahmad and I am 25 years old.

The `{}` symbols are placeholders.

The values are supplied to:

format()

---

# Positional Arguments in `format()`

We can explicitly specify the position.

name = "Ahmad"
age = 25

print("Name: {0}, Age: {1}".format(name, age))

Output:

Name: Ahmad, Age: 25

We can also change the order:

print("Age: {1}, Name: {0}".format(name, age))

Output:

Age: 25, Name: Ahmad

---

# Named Arguments in `format()`

We can also use named arguments.

print(
    "Name: {name}, Age: {age}".format(
        name="Ahmad",
        age=25
    )
)

Output:

Name: Ahmad, Age: 25

This can make complex formatting easier to understand.

---

# Formatting Numbers with `format()`

We can use the same formatting ideas.

price = 19.987654

print("Price: {:.2f}".format(price))

Output:

Price: 19.99

Thousands separator:

number = 1234567

print("{:,}".format(number))

Output:

1,234,567

Percentage:

rate = 0.875

print("{:.1%}".format(rate))

Output:

87.5%

---

# f-String vs `format()`

Compare:

### f-string

name = "Ahmad"
age = 25

print(f"My name is {name} and I am {age} years old.")

### `format()`

name = "Ahmad"
age = 25

print("My name is {} and I am {} years old.".format(name, age))

Both work.

However, modern Python code generally prefers f-strings because they are concise and readable.

---

# Formatting Expressions

With f-strings, we can format the result of an expression.

a = 10
b = 3

print(f"Result: {a / b:.2f}")

Output:

Result: 3.33

Notice that:

a / b

is calculated first.

Then the result is formatted to two decimal places.

---

# Formatting a Calculation

We can combine calculations and formatting.

price = 100
discount = 0.15

final_price = price * (1 - discount)

print(f"Final price: ${final_price:.2f}")

Output:

Final price: $85.00

This is much more realistic than simply formatting a variable.

---

# Formatting User Input

Remember that `input()` always returns a String.

Suppose:

age = input("Enter your age: ")

If the user enters:

25

then:

age

is a String.

If we need an Integer:

age = int(input("Enter your age: "))

Now we can use it in calculations:

age = int(input("Enter your age: "))

print(f"Next year you will be {age + 1}.")

---

# A Practical Example — Student Report

Suppose:

name = "Ahmad"
math = 18.5
physics = 17.75
programming = 19.25

average = (math + physics + programming) / 3

print(f"Student: {name}")
print(f"Math: {math:.2f}")
print(f"Physics: {physics:.2f}")
print(f"Programming: {programming:.2f}")
print(f"Average: {average:.2f}")

Output:

Student: Ahmad
Math: 18.50
Physics: 17.75
Programming: 19.25
Average: 18.50

---

# A Practical Example — Shopping Receipt

product = "Keyboard"
price = 49.987
quantity = 2

total = price * quantity

print("----- Receipt -----")
print(f"Product: {product}")
print(f"Price: ${price:.2f}")
print(f"Quantity: {quantity}")
print(f"Total: ${total:.2f}")

Output:

----- Receipt -----
Product: Keyboard
Price: $49.99
Quantity: 2
Total: $99.97

---

# A Practical Example — Game Score

player = "Ahmad"
score = 12500
accuracy = 0.9345

print(f"Player: {player}")
print(f"Score: {score:,}")
print(f"Accuracy: {accuracy:.1%}")

Output:

Player: Ahmad
Score: 12,500
Accuracy: 93.5%

---

# A Practical Example — Countdown

seconds = 125

minutes = seconds // 60
remaining_seconds = seconds % 60

print(f"Time remaining: {minutes}:{remaining_seconds:02d}")

Output:

Time remaining: 2:05

The important part is:

`02d`

It means that the number should occupy at least two digits.

So:

5

becomes:

05

This is extremely useful for:

- timers
- clocks
- dates
- scores
- counters

---

# Zero Padding

Suppose:

number = 7

print(f"{number:02d}")

Output:

07

For three digits:

print(f"{number:03d}")

Output:

007

Another example:

hour = 9
minute = 5
second = 3

print(f"{hour:02d}:{minute:02d}:{second:02d}")

Output:

09:05:03

This is a very common formatting technique.

---

# Escaping Curly Braces

Curly braces have a special meaning inside f-strings.

For example:

name = "Ahmad"

print(f"Hello {name}")

Here:

{name}

means "insert the value of name".

But what if we actually want to display curly braces?

We use double braces:

print(f"{{name}}")

Output:

{name}

So:

`{{`

produces:

{

and:

`}}`

produces:

}

---

# Formatting Boolean Values

We can also place Boolean values inside f-strings.

is_logged_in = True

print(f"Logged in: {is_logged_in}")

Output:

Logged in: True

We can also use expressions:

age = 20

print(f"Adult: {age >= 18}")

Output:

Adult: True

This demonstrates that expressions inside `{}` can return Boolean values too.

---

# Formatting with Conditional Expressions

Python allows a conditional expression inside an f-string.

age = 20

print(f"Status: {'Adult' if age >= 18 else 'Minor'}")

Output:

Status: Adult

This is powerful, but beginners should first understand the simpler forms of f-strings before using complex expressions.

---

# Formatting and Readability

String Formatting is not only about making output look nice.

It also improves the readability of the program.

Compare:

name = "Ahmad"
score = 95

print("Student " + name + " has a score of " + str(score) + ".")

with:

print(f"Student {name} has a score of {score}.")

The second version is easier to understand.

Good formatting helps us write code that other people can read and maintain.

---

# A Complete Example

Let's combine several concepts from previous sections.

The program asks for:

- name
- age
- score

Then it creates a formatted report.

name = input("Enter your name: ").strip().title()
age = int(input("Enter your age: "))
score = float(input("Enter your score: "))

print()
print("----- Student Report -----")
print(f"Name: {name}")
print(f"Age: {age}")
print(f"Score: {score:.2f}")

Output could be:

----- Student Report -----
Name: Ahmad
Age: 25
Score: 92.50

Notice how this one example combines:

- `input()`
- `strip()`
- `title()`
- `int()`
- `float()`
- f-strings
- number formatting

This is the kind of combination we want to practice throughout the project.

---

# Exercises

## Exercise 1 — Basic f-String

Create:

name = "Ali"
age = 20

Use an f-string to display:

My name is Ali and I am 20 years old.

---

## Exercise 2 — Multiple Variables

Create:

name = "Sara"
city = "Shiraz"
age = 22

Display all three values in one sentence using an f-string.

---

## Exercise 3 — Expression Inside `{}`

Create:

a = 15
b = 7

Display:

The sum is 22.

Use an expression directly inside the f-string.

---

## Exercise 4 — String Method Inside an f-String

Create:

name = "aHMAD"

Use `title()` inside an f-string to display:

Hello Ahmad!

---

## Exercise 5 — Indexing and Formatting

Create:

text = "Python"

Use an f-string to display:

First character: P
Last character: n

Use String Indexing.

---

## Exercise 6 — Slicing and Formatting

Create:

text = "Programming"

Display:

First four characters: Prog

Use Slicing inside the f-string.

---

## Exercise 7 — Decimal Formatting

Create:

price = 19.98765

Display the price with exactly two decimal places.

Expected:

19.99

---

## Exercise 8 — Percentage

Create:

success_rate = 0.8765

Display:

87.65%

Use percentage formatting.

---

## Exercise 9 — Thousands Separator

Create:

population = 12500000

Display:

12,500,000

---

## Exercise 10 — Combine Number Formats

Create:

price = 1234567.8912

Display:

1,234,567.89

Use both:

- thousands separator
- two decimal places

---

## Exercise 11 — Alignment

Create:

name = "Ahmad"

Print the name:

- left aligned in a field of 15 characters
- right aligned in a field of 15 characters
- centered in a field of 15 characters

---

## Exercise 12 — Custom Fill

Create:

name = "Python"

Create outputs using `*` as the fill character:

Python*********
*********Python
****Python*****

Try to understand how width and alignment work.

---

## Exercise 13 — Student Average

Create:

math = 18.5
physics = 17.25
programming = 19.75

Calculate the average and display it with two decimal places.

---

## Exercise 14 — Shopping Receipt

Create:

product = "Mouse"
price = 25.987
quantity = 3

Calculate the total.

Display:

----- Receipt -----
Product: Mouse
Price: $25.99
Quantity: 3
Total: $77.96

---

## Exercise 15 — User Input

Ask the user for:

- name
- age
- city

Then display all information using f-strings.

Make sure the name is cleaned with `strip()`.

---

## Exercise 16 — Age Calculator

Ask the user for their age.

Display:

Current age: 25
Next year: 26
In five years: 30

The numbers must be calculated rather than manually written.

---

## Exercise 17 — Timer Formatting

Ask the user for a number of seconds.

Convert it to:

minutes
seconds

Then display it in this format:

02:05

Use zero padding.

---

## Exercise 18 — Game Score

Create:

player = "Ahmad"
score = 12500
accuracy = 0.9345

Display:

Player: Ahmad
Score: 12,500
Accuracy: 93.45%

---

# Final Algorithmic Challenge

Create a program called:

Student Report Generator

The program should ask the user for:

1. Student name
2. Student age
3. Math score
4. Physics score
5. Programming score

The program should then:

1. Clean the student's name using `strip()`.
2. Format the student's name using `title()`.
3. Convert the age to an Integer.
4. Convert the scores to Floating-Point numbers.
5. Calculate the average score.
6. Calculate the percentage of the average relative to 20.
7. Determine whether the student passed.
8. Display a clean formatted report.

The output should look similar to:

----- Student Report -----

Name: Ahmad Ahmadi
Age: 20

Math:         18.50
Physics:      17.75
Programming:  19.25

Average:      18.50
Percentage:   92.50%
Status:       Passed

Your program should calculate all values dynamically.

Do not manually write the final numbers into the output.

---

# Think Algorithmically

Before writing code, break the problem into steps.

Think about:

Receive name
↓
Clean name
↓
Format name
↓
Receive age
↓
Convert age to Integer
↓
Receive Math score
↓
Convert to Float
↓
Receive Physics score
↓
Convert to Float
↓
Receive Programming score
↓
Calculate average
↓
Calculate percentage
↓
Check pass condition
↓
Format numbers
↓
Display report

Now identify which concepts from previous sections are needed.

You should notice that this challenge combines:

- input
- Strings
- String Methods
- `strip()`
- `title()`
- Type Conversion
- Integers
- Floats
- Arithmetic
- Conditions
- f-Strings
- Number Formatting

This is intentional.

The goal is not only to learn String Formatting.

The goal is to learn how to combine several programming concepts to solve a problem.

---

# Final Challenge — Answer

Try to solve the challenge yourself before looking at the solution.

A possible solution is:

name = input("Enter student name: ").strip().title()
age = int(input("Enter student age: "))

math = float(input("Enter Math score: "))
physics = float(input("Enter Physics score: "))
programming = float(input("Enter Programming score: "))

average = (math + physics + programming) / 3
percentage = (average / 20) * 100

if average >= 10:
    status = "Passed"
else:
    status = "Failed"

print()
print("----- Student Report -----")
print()
print(f"Name: {name}")
print(f"Age: {age}")
print()
print(f"Math:         {math:.2f}")
print(f"Physics:      {physics:.2f}")
print(f"Programming:  {programming:.2f}")
print()
print(f"Average:      {average:.2f}")
print(f"Percentage:   {percentage:.2f}%")
print(f"Status:       {status}")

The important part is not memorizing this solution.

The important part is understanding how the algorithm was converted into code.

---

