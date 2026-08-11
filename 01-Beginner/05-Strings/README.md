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
