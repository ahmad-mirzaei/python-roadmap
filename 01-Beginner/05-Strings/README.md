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

In the previous parts, we learned how to create strings, access individual characters, slice strings, and use string methods.

Now we are going to learn how to make strings more useful and readable by **putting values inside them**.

This is called **string formatting**.

String formatting is extremely common in real programs because programs usually need to display information that comes from variables.

For example, instead of writing:

```python
name = "Ahmad"
age = 25

print("My name is Ahmad and I am 25 years old.")
```

we want the program to use the variables:

```python
name = "Ahmad"
age = 25

print(f"My name is {name} and I am {age} years old.")
```

The second approach is much more useful because the values can change.

---

## Why Do We Need String Formatting?

Imagine a program that displays a student's information.

We might have:

```python
name = "Sara"
age = 20
score = 18.75
```

We could print every value separately:

```python
print("Name:", name)
print("Age:", age)
print("Score:", score)
```

This works, but sometimes we want to build a complete sentence:

```python
print(f"{name} is {age} years old and scored {score}.")
```

Output:

```text
Sara is 20 years old and scored 18.75.
```

String formatting allows us to combine:

- Text
- Variables
- Calculated values
- Numbers
- Expressions

inside one formatted string.

---

# f-Strings

The most common and recommended way to format strings in modern Python is the **f-string**.

The `f` is written before the opening quotation mark.

For example:

```python
name = "Ahmad"

print(f"Hello, {name}!")
```

Output:

```text
Hello, Ahmad!
```

Without the `f`, Python does not treat `{name}` as a variable:

```python
name = "Ahmad"

print("Hello, {name}!")
```

Output:

```text
Hello, {name}!
```

So remember:

```python
f"Hello, {name}!"
```

not:

```python
"Hello, {name}!"
```

---

## How Does an f-String Work?

Consider:

```python
name = "Ahmad"
age = 25

message = f"My name is {name} and I am {age} years old."

print(message)
```

Python sees:

```python
f"My name is {name} and I am {age} years old."
```

The parts inside `{}` are evaluated and replaced with their values.

So:

```python
{name}
```

becomes:

```text
Ahmad
```

and:

```python
{age}
```

becomes:

```text
25
```

The final string becomes:

```text
My name is Ahmad and I am 25 years old.
```

---

# Putting Multiple Variables Inside a String

You can use as many variables as you need.

```python
first_name = "Ali"
last_name = "Ahmadi"
age = 22

print(f"Name: {first_name} {last_name}")
print(f"Age: {age}")
```

Output:

```text
Name: Ali Ahmadi
Age: 22
```

Another example:

```python
product = "Keyboard"
price = 49.99
quantity = 2

print(f"Product: {product}")
print(f"Price: {price}")
print(f"Quantity: {quantity}")
```

Output:

```text
Product: Keyboard
Price: 49.99
Quantity: 2
```

---

# Expressions Inside f-Strings

One of the most useful features of f-strings is that we can put **expressions** inside `{}`.

For example:

```python
a = 10
b = 5

print(f"Sum: {a + b}")
```

Output:

```text
Sum: 15
```

We can also multiply:

```python
price = 20
quantity = 3

print(f"Total: {price * quantity}")
```

Output:

```text
Total: 60
```

We can use more complicated expressions:

```python
math = 18
physics = 16
programming = 20

average = (math + physics + programming) / 3

print(f"Average: {average}")
```

Output:

```text
Average: 18.0
```

The important idea is:

> Anything inside `{}` in an f-string is evaluated as a Python expression.

For example:

```python
name = "Ahmad"
age = 25

print(f"{name} will be {age + 1} next year.")
```

Output:

```text
Ahmad will be 26 next year.
```

---

# Using String Methods Inside f-Strings

We can even use methods inside `{}`.

For example:

```python
name = "ahmad"

print(f"Hello, {name.title()}!")
```

Output:

```text
Hello, Ahmad!
```

Another example:

```python
name = "  ahmad  "

print(f"Hello, {name.strip().title()}!")
```

Output:

```text
Hello, Ahmad!
```

This is useful when the original input may contain unnecessary spaces or inconsistent capitalization.

For example:

```python
name = input("Enter your name: ").strip().title()

print(f"Welcome, {name}!")
```

If the user enters:

```text
   ahmad
```

the output becomes:

```text
Welcome, Ahmad!
```

---

# Formatting Numbers

String formatting becomes especially useful when working with numbers.

Suppose we have:

```python
price = 49.99
```

We can display it directly:

```python
print(f"Price: {price}")
```

Output:

```text
Price: 49.99
```

But sometimes we want to control how many decimal places are displayed.

For example:

```python
price = 49.999999

print(f"Price: {price:.2f}")
```

Output:

```text
Price: 50.00
```

The important part is:

```python
:.2f
```

Let's break it down.

---

## Understanding `:.2f`

Consider:

```python
f"{price:.2f}"
```

The structure is:

```text
{value:format}
```

Here:

- `price` is the value.
- `:` starts the formatting instructions.
- `.2` means two digits after the decimal point.
- `f` means fixed-point decimal formatting.

For example:

```python
number = 12.34567

print(f"{number:.1f}")
print(f"{number:.2f}")
print(f"{number:.3f}")
```

Output:

```text
12.3
12.35
12.346
```

Python also rounds the number when necessary.

For example:

```python
score = 17.876

print(f"Score: {score:.2f}")
```

Output:

```text
Score: 17.88
```

---

# Formatting Percentages

Suppose a score is stored as a decimal:

```python
score = 0.875
```

If we print it normally:

```python
print(score)
```

we get:

```text
0.875
```

But maybe we want:

```text
87.50%
```

We can use `%` formatting:

```python
print(f"{score:.2%}")
```

Output:

```text
87.50%
```

Notice that:

```python
.2%
```

does two things:

1. Converts the decimal to a percentage.
2. Displays two decimal places.

For example:

```python
value = 0.5

print(f"{value:.2%}")
```

Output:

```text
50.00%
```

Another example:

```python
value = 0.875

print(f"{value:.1%}")
```

Output:

```text
87.5%
```

---

# Formatting Money

A common real-world situation is displaying prices.

For example:

```python
price = 1499.5

print(f"${price:.2f}")
```

Output:

```text
$1499.50
```

We can combine formatting with calculations:

```python
price = 49.99
quantity = 3

total = price * quantity

print(f"Total: ${total:.2f}")
```

Output:

```text
Total: $149.97
```

---

# Thousands Separators

Large numbers can be difficult to read.

For example:

```python
population = 12500000

print(population)
```

Output:

```text
12500000
```

We can use a comma separator:

```python
print(f"{population:,}")
```

Output:

```text
12,500,000
```

This is useful for:

- Population
- Money
- Large measurements
- Statistics
- Scores
- File sizes

Another example:

```python
salary = 125000

print(f"Salary: ${salary:,}")
```

Output:

```text
Salary: $125,000
```

---

# Combining Number Formatting

Formatting instructions can be combined.

For example:

```python
price = 1234567.89123

print(f"${price:,.2f}")
```

Output:

```text
$1,234,567.89
```

Here:

```text
,
```

adds thousands separators.

And:

```text
.2f
```

keeps two decimal places.

This pattern is extremely useful when displaying financial information.

---

# Alignment

Sometimes we want information to line up neatly.

Python allows us to control the width of a formatted value.

For example:

```python
name = "Ali"

print(f"{name:10}")
```

This reserves a width of 10 characters.

We can also align text to the left:

```python
name = "Ali"

print(f"{name:<10}")
```

Right alignment:

```python
name = "Ali"

print(f"{name:>10}")
```

Center alignment:

```python
name = "Ali"

print(f"{name:^10}")
```

These are especially useful when creating simple tables.

---

# Creating a Simple Table

For example:

```python
name1 = "Ali"
score1 = 18

name2 = "Sara"
score2 = 19

print(f"{'Name':<10}{'Score':>10}")
print(f"{name1:<10}{score1:>10}")
print(f"{name2:<10}{score2:>10}")
```

Output:

```text
Name           Score
Ali               18
Sara              19
```

The formatting makes the output easier to read.

---

# Formatting Boolean Values

Boolean values can also be placed inside f-strings.

```python
is_student = True

print(f"Student: {is_student}")
```

Output:

```text
Student: True
```

Another example:

```python
age = 20
is_adult = age >= 18

print(f"Age: {age}")
print(f"Adult: {is_adult}")
```

Output:

```text
Age: 20
Adult: True
```

---

# Formatting Results of Conditions

We can calculate a value and immediately display it.

```python
age = 20

print(f"Can vote: {age >= 18}")
```

Output:

```text
Can vote: True
```

This is useful when debugging programs or displaying the result of a logical operation.

---

# Using Conditional Expressions

Python also allows a conditional expression inside an f-string.

For example:

```python
age = 20

print(f"Status: {'Adult' if age >= 18 else 'Minor'}")
```

Output:

```text
Status: Adult
```

Another example:

```python
score = 17

print(f"Result: {'Passed' if score >= 10 else 'Failed'}")
```

Output:

```text
Result: Passed
```

This is compact, but for complicated logic it is usually better to calculate the result first.

For example:

```python
score = 17

if score >= 10:
    result = "Passed"
else:
    result = "Failed"

print(f"Result: {result}")
```

This version is often easier to read.

---

# Building Multi-Line Output

f-strings are not limited to one line.

We can use `\n`:

```python
name = "Ahmad"
age = 25
score = 18.5

print(f"Name: {name}\nAge: {age}\nScore: {score}")
```

Output:

```text
Name: Ahmad
Age: 25
Score: 18.5
```

We can also use triple quotes for larger blocks of text:

```python
name = "Ahmad"
age = 25

message = f"""
----- Student Profile -----
Name: {name}
Age: {age}
---------------------------
"""

print(message)
```

Output:

```text
----- Student Profile -----
Name: Ahmad
Age: 25
---------------------------
```

This is useful for reports and formatted output.

---

# Formatting User Input

String formatting becomes much more useful when combined with `input()`.

For example:

```python
name = input("Enter your name: ").strip().title()
age = int(input("Enter your age: "))

print(f"Hello, {name}!")
print(f"You are {age} years old.")
```

If the user enters:

```text
ahmad
25
```

the output is:

```text
Hello, Ahmad!
You are 25 years old.
```

Notice how several concepts from previous parts are working together:

- `input()` receives data.
- `.strip()` removes unnecessary spaces.
- `.title()` changes capitalization.
- `int()` converts the age to an integer.
- f-strings format the final output.

This is an important example of how Python concepts build on each other.

---

# Formatting Calculated Values

Suppose a user enters three scores.

```python
math = float(input("Enter Math score: "))
physics = float(input("Enter Physics score: "))
programming = float(input("Enter Programming score: "))

average = (math + physics + programming) / 3

print(f"Average: {average:.2f}")
```

If the user enters:

```text
18
16
19
```

the output is:

```text
Average: 17.67
```

We can also calculate a percentage:

```python
percentage = (average / 20) * 100

print(f"Percentage: {percentage:.2f}%")
```

Output:

```text
Percentage: 88.33%
```

---

# A Complete Student Report

Now let's combine everything we have learned.

```python
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
print(f"Name: {name}")
print(f"Age: {age}")
print(f"Math: {math:.2f}")
print(f"Physics: {physics:.2f}")
print(f"Programming: {programming:.2f}")
print(f"Average: {average:.2f}")
print(f"Percentage: {percentage:.2f}%")
print(f"Status: {status}")
```

Example input:

```text
Enter student name:   alex
Enter student age: 20
Enter Math score: 18
Enter Physics score: 17
Enter Programming score: 18.5
```

Output:

```text
----- Student Report -----
Name: Alex
Age: 20
Math: 18.00
Physics: 17.00
Programming: 18.50
Average: 17.83
Percentage: 89.17%
Status: Passed
```

This small program combines many concepts:

- Variables
- Strings
- `input()`
- `int()`
- `float()`
- `.strip()`
- `.title()`
- Arithmetic
- Comparison
- `if / else`
- f-strings
- Number formatting

This is exactly how programming concepts start working together to create useful programs.

---

# Common Mistake — Forgetting the `f`

Wrong:

```python
name = "Ahmad"

print("Hello, {name}!")
```

Output:

```text
Hello, {name}!
```

Correct:

```python
print(f"Hello, {name}!")
```

Output:

```text
Hello, Ahmad!
```

---

# Common Mistake — Putting Quotes Inside the Braces

Wrong:

```python
name = "Ahmad"

print(f"Hello, {"name"}!")
```

This creates a syntax problem.

Correct:

```python
print(f"Hello, {name}!")
```

The variable name does not need quotes.

---

# Common Mistake — Confusing the Value with Its Formatting

Consider:

```python
score = 0.875

print(f"{score:.2f}")
```

This gives:

```text
0.88
```

But:

```python
print(f"{score:.2%}")
```

gives:

```text
87.50%
```

The difference is important.

`.2f` means:

> Show the number with two decimal places.

`.2%` means:

> Convert the decimal to a percentage and show two decimal places.

---

# Common Mistake — Formatting Does Not Change the Original Variable

Consider:

```python
price = 12.3456

print(f"{price:.2f}")
print(price)
```

Output:

```text
12.35
12.3456
```

The formatting only changes how the value is displayed.

It does not permanently change `price`.

If we actually want a rounded value, we can use:

```python
price = 12.3456

price = round(price, 2)

print(price)
```

Output:

```text
12.35
```

This distinction is important:

- Formatting controls **display**.
- `round()` changes the value stored in the variable.

---

# Exercises

## Exercise 1 — Personal Introduction

Create these variables:

```python
name = "Ali"
age = 21
city = "Tehran"
```

Print:

```text
My name is Ali.
I am 21 years old.
I live in Tehran.
```

Use an f-string.

---

## Exercise 2 — Product Information

Create:

```python
product = "Keyboard"
price = 49.99
quantity = 2
```

Display:

```text
Product: Keyboard
Price: $49.99
Quantity: 2
```

Use f-strings.

---

## Exercise 3 — Calculate Total

Using:

```python
price = 49.99
quantity = 2
```

calculate the total price and display:

```text
Total: $99.98
```

The price must have exactly two decimal places.

---

## Exercise 4 — Average Score

Create three scores:

```python
math = 18
physics = 16
programming = 19
```

Calculate the average and display it with two decimal places.

Expected output:

```text
Average: 17.67
```

---

## Exercise 5 — Percentage

Given:

```python
score = 0.875
```

display:

```text
Score: 87.50%
```

Use percentage formatting.

---

## Exercise 6 — User Profile

Ask the user for:

- Name
- Age
- City

Then display:

```text
----- User Profile -----
Name: Alex
Age: 25
City: Tehran
```

The name should be cleaned using `.strip().title()`.

---

## Exercise 7 — Rectangle Report

Create:

```python
width = 12.5
height = 8.2
```

Calculate:

- Area
- Perimeter

Display both with two decimal places.

Expected format:

```text
Width: 12.50
Height: 8.20
Area: 102.50
Perimeter: 41.40
```

---

## Exercise 8 — Shopping Receipt

Ask the user for:

- Product name
- Price
- Quantity

Calculate the total and display:

```text
----- Receipt -----
Product: Keyboard
Price: $49.99
Quantity: 2
Total: $99.98
```

Use proper number formatting.

---

## Exercise 9 — Temperature Converter

Ask the user for a temperature in Celsius.

Convert it to Fahrenheit using:

```text
F = C × 9 / 5 + 32
```

Display:

```text
Celsius: 25.00°C
Fahrenheit: 77.00°F
```

---

## Exercise 10 — Student Profile

Ask the user for:

- Name
- Age
- Score

Then display:

```text
----- Student Profile -----
Name: Alex
Age: 20
Score: 87.50%
```

The score should be entered as a decimal such as:

```text
0.875
```

and displayed as:

```text
87.50%
```

---

## Exercise 11 — Simple Table

Create three students:

```python
name1 = "Ali"
score1 = 18

name2 = "Sara"
score2 = 19

name3 = "Reza"
score3 = 17
```

Display them in an aligned table:

```text
Name           Score
Ali               18
Sara              19
Reza              17
```

Use alignment formatting.

---

## Exercise 12 — Bank Account

Create:

```python
name = "Ahmad"
balance = 1250000.5
```

Display:

```text
----- Bank Account -----
Name: Ahmad
Balance: $1,250,000.50
```

Use thousands separators and two decimal places.

---

# Final Challenge — Student Report System

Before looking at the solution, try to solve the problem yourself.

Create a program that asks the user for:

- Student name
- Student age
- Math score
- Physics score
- Programming score

The name must be cleaned using:

```python
.strip().title()
```

The scores should be entered as numbers between `0` and `20`.

Calculate:

- Average score
- Percentage

The percentage should be calculated relative to a maximum score of `20`.

Then determine whether the student passed.

A student passes if the average is at least `10`.

Finally, display a formatted report similar to:

```text
----- Student Report -----
Name: Alex
Age: 20
Math: 18.00
Physics: 17.00
Programming: 18.50
Average: 17.83
Percentage: 89.17%
Status: Passed
```

### Requirements

Your program must use:

- `input()`
- `int()`
- `float()`
- `.strip()`
- `.title()`
- Variables
- Arithmetic operators
- `if / else`
- f-strings
- Number formatting with `.2f`
- Percentage formatting or a calculated percentage

Try to solve it without looking at the answer.

---

# Final Challenge — Solution

One possible solution is:

```python
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
print(f"Name: {name}")
print(f"Age: {age}")
print(f"Math: {math:.2f}")
print(f"Physics: {physics:.2f}")
print(f"Programming: {programming:.2f}")
print(f"Average: {average:.2f}")
print(f"Percentage: {percentage:.2f}%")
print(f"Status: {status}")
```

The important part is not memorizing this exact program.

The goal is to understand how the different pieces work together:

```text
input
  ↓
clean / convert data
  ↓
store values in variables
  ↓
calculate results
  ↓
make a decision
  ↓
format the final output
```

This is the beginning of **algorithmic thinking**: taking raw information, transforming it step by step, making decisions, and producing a useful result.

---

# Part 8 — Strings and User Input

In the previous parts, you learned how to:

- Create strings
- Use quotation marks
- Access characters with indexing
- Extract parts of strings with slicing
- Use string methods
- Format strings with f-strings

Now we will combine these concepts with user input.

A program becomes much more useful when it can receive text from the user, process that text, and produce a meaningful result.

A common pattern in real programs is:

    Input
    ↓
    Clean
    ↓
    Process
    ↓
    Format
    ↓
    Output

The exercises in this section gradually combine the concepts you have learned so far.

---

## Exercise 1 — Ask for a Name

Ask the user to enter their name.

Then display:

    Hello, Ahmad!

Replace `Ahmad` with the user's input.

Use an f-string.

---

## Exercise 2 — Clean the Name

Ask the user to enter their name.

The user might accidentally type spaces before or after the name.

For example:

    "   Ahmad   "

Remove the unnecessary spaces and display:

    Hello, Ahmad!

Use `.strip()`.

---

## Exercise 3 — Format the Name

Ask the user to enter their name in lowercase.

Example:

    Enter your name: ahmad

Display:

    Name: Ahmad

Use an appropriate string method.

---

## Exercise 4 — Analyze the Name

Ask the user to enter their name.

Display:

    Name: Ahmad
    Length: 5
    First character: A
    Last character: d

Use:

- `.strip()`
- `.title()`
- `len()`
- Indexing
- f-strings

---

## Exercise 5 — Username Generator

Ask the user for:

- First name
- Last name

Create a username using this format:

    first.last

Example:

    First name: Ahmad
    Last name: Rezaei

    Username: ahmad.rezaei

The username must be lowercase.

Clean the input before creating the username.

---

## Exercise 6 — Email Generator

Ask the user for:

- First name
- Last name

Create an email address using:

    first.last@example.com

Example:

    First name: Ahmad
    Last name: Rezaei

    Email: ahmad.rezaei@example.com

Clean and format the names before creating the email.

---

## Exercise 7 — Extract Username from Email

Ask the user for an email address.

Example:

    Enter email: ahmad@example.com

Display:

    Username: ahmad

Use string methods or slicing.

Do not manually type the username.

---

## Exercise 8 — Extract Domain

Ask the user for an email address.

Example:

    Enter email: ahmad@example.com

Display:

    Domain: example.com

Think about the position of `@` and how slicing can help you.

---

## Exercise 9 — Email Analyzer

Ask the user for an email address.

Example:

    Enter email: ahmad@example.com

Display:

    Email: ahmad@example.com
    Username: ahmad
    Domain: example.com
    Length: 17

Combine:

- String methods
- Indexing or slicing
- `len()`
- f-strings

---

## Exercise 10 — Sentence Cleaner

Ask the user to enter a sentence.

The program should:

1. Remove unnecessary spaces.
2. Convert the sentence to lowercase.
3. Display the cleaned sentence.

Example:

    Input:
       PYTHON IS FUN

    Output:
    python is fun

---

## Exercise 11 — Sentence Information

Ask the user to enter a sentence.

Display:

    Sentence: Python is easy.
    Length: 16
    Uppercase: PYTHON IS EASY.
    Lowercase: python is easy.

Use string methods.

---

## Exercise 12 — Search in a Sentence

Ask the user for:

- A sentence
- A word to search for

Example:

    Sentence: Python is easy to learn.
    Search: easy

Display:

    Found: True
    Position: 10

Use `.find()`.

Do not manually count the position.

---

## Exercise 13 — Count a Character

Ask the user for:

- A sentence
- A character

Example:

    Sentence: programming
    Character: m

Display:

    Character: m
    Count: 2

Use `.count()`.

---

## Exercise 14 — Replace a Word

Ask the user for:

- A sentence
- A word to replace
- A replacement word

Example:

    Sentence: I like Java
    Word to replace: Java
    Replacement: Python

Display:

    Result: I like Python

Use `.replace()`.

---

## Exercise 15 — Check an Email

Ask the user to enter an email address.

Check whether it:

- Contains `@`
- Ends with `.com`

Example:

    Email: ahmad@example.com

    Contains @: True
    Ends with .com: True

Use appropriate string methods.

---

## Exercise 16 — Check a File Name

Ask the user for a filename.

Determine whether it is a Python file.

Example:

    Filename: calculator.py

    Python file: True

Use `.endswith()`.

---

## Exercise 17 — Generate Initials

Ask the user for:

- First name
- Last name

Example:

    First name: Ahmad
    Last name: Rezaei

Display:

    Full name: Ahmad Rezaei
    Initials: AR

Use indexing.

---

## Exercise 18 — Generate a Short ID

Ask the user for:

- First name
- Last name
- Birth year

Create an ID using:

    first three letters of first name
    +
    first three letters of last name
    +
    birth year

Example:

    First name: Ahmad
    Last name: Rezaei
    Birth year: 2001

    ID: ahmrez2001

Requirements:

- Convert names to lowercase.
- Use slicing.
- Combine the values with an f-string.

---

## Exercise 19 — Password Mask

Ask the user to enter a password.

Do not display the actual password.

Instead, display a number of `*` characters equal to the password length.

Example:

    Enter password: python123

    Password: *********
    Length: 9

Use:

- `len()`
- String multiplication

---

## Exercise 20 — Password Analyzer

Ask the user to enter a password.

Display:

    Password length: 10
    Contains @: True
    Starts with P: True
    Ends with 123: False

Use appropriate string methods.

Do not display the actual password.

---

## Exercise 21 — Product Information

Ask the user for:

- Product name
- Price
- Quantity

Example:

    Product: Keyboard
    Price: 49.99
    Quantity: 2

Display:

    ----- Product Information -----

    Product: Keyboard
    Price: $49.99
    Quantity: 2
    Total: $99.98

Requirements:

- Clean the product name.
- Convert price to `float`.
- Convert quantity to `int`.
- Calculate the total.
- Format monetary values with two decimal places.
- Use f-strings.

---

## Exercise 22 — Student Profile

Ask the user for:

- Name
- Age
- Score

Example:

    Name:   alex
    Age: 20
    Score: 0.875

Display:

    ----- Student Profile -----

    Name: Alex
    Age: 20
    Score: 87.50%

Requirements:

- Remove unnecessary spaces.
- Format the name.
- Convert age to `int`.
- Convert score to `float`.
- Display the score as a percentage.
- Use an f-string.

---

## Exercise 23 — Username and Email Generator

Ask the user for:

- First name
- Last name

Generate both:

    Username: ahmad.rezaei
    Email: ahmad.rezaei@example.com

Requirements:

- Remove unnecessary spaces.
- Convert names to lowercase.
- Use f-strings.

---

## Exercise 24 — Text Cleaner

Ask the user to enter a sentence.

The program should:

1. Remove spaces from the beginning and end.
2. Convert the sentence to lowercase.
3. Replace `python` with `Python`.
4. Display the result.

Example:

    Input:
       I LOVE PYTHON PROGRAMMING

    Output:
    i love Python programming

Think carefully about the order of the operations.

---

## Exercise 25 — Word Reverser

Ask the user for a word.

Display:

    Original: Python
    Reversed: nohtyP

Use slicing.

Do not use a loop.

---

## Exercise 26 — First and Last Three Characters

Ask the user for a word.

Display its first three and last three characters.

Example:

    Word: Programming

    First three: Pro
    Last three: ing

Use slicing.

---

## Exercise 27 — Word Analyzer

Ask the user for a word.

Display:

    Word: Python
    Length: 6
    First character: P
    Last character: n
    First three: Pyt
    Last three: hon
    Reversed: nohtyP
    Uppercase: PYTHON
    Lowercase: python

You should combine:

- `len()`
- Indexing
- Slicing
- String methods
- f-strings

---

## Exercise 28 — Sentence Analyzer

Ask the user for a sentence.

Display:

    Sentence: Python is easy to learn.
    Length: 25
    Uppercase: PYTHON IS EASY TO LEARN.
    Lowercase: python is easy to learn.
    Starts with Python: True
    Ends with learn.: True

Use string methods wherever appropriate.

---

## Exercise 29 — Simple Receipt

Ask the user for:

- Product name
- Price
- Quantity

Example:

    Product: Mouse
    Price: 25.5
    Quantity: 3

Display:

    ----- Receipt -----

    Product: Mouse
    Price: $25.50
    Quantity: 3
    Total: $76.50

Requirements:

- Clean the product name.
- Convert the price to a float.
- Convert the quantity to an integer.
- Calculate the total.
- Format the price and total to two decimal places.
- Use an f-string.

---

## Exercise 30 — Student Report

Ask the user for:

- Student name
- Age
- Math score
- Physics score
- Programming score

Each score is out of 20.

Calculate the average and percentage.

Example:

    ----- Student Report -----

    Name: Alex
    Age: 20

    Math: 18.00
    Physics: 17.50
    Programming: 19.00

    Average: 18.17
    Percentage: 90.83%

Requirements:

- Clean and format the student's name.
- Convert numeric input to the correct types.
- Calculate the average.
- Convert the average to a percentage.
- Format decimal values with two decimal places.
- Use f-strings.

---

# Final Challenge — User Information Card

Do not look at the answer before trying to solve the problem.

Build a program that creates a formatted user information card.

The program should ask the user for:

- First name
- Last name
- Email
- Age
- City

The program must then:

1. Remove unnecessary spaces from all text inputs.
2. Format the first and last names correctly.
3. Create the full name.
4. Extract the username from the email.
5. Extract the domain from the email.
6. Convert the age to an integer.
7. Create a username using the person's first and last name.
8. Display all information in a clean format.

For example:

    First name:   alex
    Last name: johnson
    Email: alex.johnson@example.com
    Age: 20
    City:   London

The output should look like:

    ----- User Information -----

    Full name: Alex Johnson
    Age: 20
    City: London

    Email: alex.johnson@example.com
    Email username: alex.johnson
    Email domain: example.com

    Generated username: alex.johnson

Concepts you should combine:

- `input()`
- Variables
- Strings
- `.strip()`
- `.lower()`
- `.title()`
- Indexing
- Slicing
- `.find()`
- `len()`
- f-strings
- `int()`

Think about the problem as an algorithm:

    Input
    ↓
    Clean
    ↓
    Format
    ↓
    Extract
    ↓
    Convert
    ↓
    Generate
    ↓
    Display

The goal is not simply to make the program work.

The goal is to practice breaking a larger problem into smaller, logical steps.

---

# Final Challenge — Answer

Try to solve the challenge yourself first.

One possible solution is:

    first_name = input("First name: ").strip().title()
    last_name = input("Last name: ").strip().title()
    email = input("Email: ").strip().lower()
    age = int(input("Age: "))
    city = input("City: ").strip().title()

    full_name = f"{first_name} {last_name}"

    at_position = email.find("@")

    email_username = email[:at_position]
    email_domain = email[at_position + 1:]

    generated_username = f"{first_name.lower()}.{last_name.lower()}"

    print()
    print("----- User Information -----")
    print()
    print(f"Full name: {full_name}")
    print(f"Age: {age}")
    print(f"City: {city}")
    print()
    print(f"Email: {email}")
    print(f"Email username: {email_username}")
    print(f"Email domain: {email_domain}")
    print()
    print(f"Generated username: {generated_username}")

The important part is not memorizing the solution.

Focus on the sequence of operations:

    Input
    ↓
    Clean
    ↓
    Format
    ↓
    Find
    ↓
    Slice
    ↓
    Convert
    ↓
    Generate
    ↓
    Format output

This way of thinking will become increasingly important as your programs become larger and more complex.

---

# Part 9 — Advanced String Operations

By now, strings should no longer feel like simple pieces of text.

You have learned how to:

- Create strings
- Store strings in variables
- Access individual characters
- Extract sections with slicing
- Change text with string methods
- Format values with f-strings
- Receive text from users
- Clean and process user input

In this section, we will go one step further.

The goal is to start treating strings as **structured data**.

A string may look like ordinary text, but it often contains information with a structure that a program can analyze.

For example:

    alex.johnson@example.com

This is one string, but it contains several meaningful parts:

    username → alex.johnson
    domain   → example.com

Another example:

    Python,Java,C++,JavaScript

This is also one string, but it contains four separate values.

To work effectively with this kind of data, we need to learn how to split strings, combine strings, inspect their contents, and process them systematically.

---

## 1. Splitting a String

One of the most useful string operations is `.split()`.

It separates a string into multiple pieces.

For example:

    text = "Python is easy"

    words = text.split()

After splitting, the result contains:

    Python
    is
    easy

By default, `.split()` separates the string wherever whitespace appears.

You can also specify a separator.

For example:

    fruits = "apple,banana,orange"

    result = fruits.split(",")

The result is conceptually:

    apple
    banana
    orange

The important idea is that `.split()` transforms one string into multiple pieces.

---

## 2. Splitting User Input

Suppose the user enters several names separated by commas:

    Enter names: Ahmad, Sara, Alex

We can process the input:

    names = input("Enter names: ").split(",")

Now the program can work with each name separately.

However, notice something important.

The values may contain unnecessary spaces:

    "Ahmad"
    " Sara"
    " Alex"

A good program should clean those values.

For example:

    names = input("Enter names: ").split(",")

    first_name = names[0].strip()
    second_name = names[1].strip()
    third_name = names[2].strip()

This is an early example of a very important programming pattern:

    Receive data
    ↓
    Split data
    ↓
    Clean data
    ↓
    Process data

---

## 3. Splitting with a Specific Separator

You are not limited to commas.

For example:

    date = "2026-08-05"

    parts = date.split("-")

The resulting pieces are:

    2026
    08
    05

This allows the program to extract structured information from a simple string.

---

## 4. Joining Strings

The opposite of `split()` is often `join()`.

Suppose we have:

    words = ["Python", "is", "powerful"]

We can combine them into one string:

    sentence = " ".join(words)

The result is:

    Python is powerful

The string before `.join()` determines what is placed between the items.

For example:

    "-".join(["2026", "08", "05"])

produces:

    2026-08-05

And:

    ", ".join(["Python", "Java", "C++"])

produces:

    Python, Java, C++

This is a fundamental distinction:

    split()
    string → multiple pieces

    join()
    multiple pieces → string

---

## 5. Split and Join Together

A powerful technique is to split a string, modify its pieces, and then join them again.

For example:

    text = "python programming language"

    words = text.split()

    words = [word.title() for word in words]

    result = " ".join(words)

The final result is:

    Python Programming Language

The important idea is not the exact syntax.

The important idea is the transformation:

    Original string
          ↓
        split
          ↓
      individual words
          ↓
       process
          ↓
        join
          ↓
    new string

This pattern appears frequently in real applications.

---

## 6. Checking Whether Text Exists

You can check whether a smaller string exists inside another string with `in`.

For example:

    text = "Python is powerful"

    print("Python" in text)

The result is:

    True

You can also use:

    print("Java" in text)

which produces:

    False

This is useful when the program needs to search for specific text.

---

## 7. Using `not in`

The opposite operation is:

    not in

For example:

    text = "Python is powerful"

    print("Java" not in text)

The result is:

    True

This can make conditions easier to read.

---

## 8. Checking Individual Characters

The `in` operator also works with characters.

For example:

    text = "Python"

    print("P" in text)

Result:

    True

And:

    print("z" in text)

Result:

    False

This can be useful when validating user input.

---

## 9. Checking for Digits

Python provides methods for checking the contents of a string.

For example:

    text = "12345"

    print(text.isdigit())

Result:

    True

But:

    text = "123abc"

    print(text.isdigit())

Result:

    False

This is useful when the program expects a string containing only digits.

---

## 10. Checking for Alphabetic Characters

You can use `.isalpha()` to determine whether all characters are alphabetic.

For example:

    text = "Python"

    print(text.isalpha())

Result:

    True

But:

    text = "Python3"

    print(text.isalpha())

Result:

    False

Spaces also cause `.isalpha()` to return `False`.

For example:

    text = "Python Programming"

    print(text.isalpha())

Result:

    False

---

## 11. Checking for Alphanumeric Characters

`.isalnum()` checks whether all characters are letters or numbers.

For example:

    print("Python123".isalnum())

Result:

    True

But:

    print("Python 123".isalnum())

Result:

    False

The space is not an alphanumeric character.

---

## 12. Checking for Whitespace

`.isspace()` checks whether a string contains only whitespace characters.

For example:

    text = "   "

    print(text.isspace())

Result:

    True

But:

    text = " Python "

    print(text.isspace())

Result:

    False

This can be useful when validating empty-looking input.

---

## 13. Empty Strings

An empty string contains no characters.

You can create one with:

    text = ""

Its length is:

    len(text)

which gives:

    0

An empty string is different from a string containing spaces.

Compare:

    text1 = ""

    text2 = "   "

The first string has length `0`.

The second string has length `3`.

This distinction is important when validating user input.

---

## 14. Checking Empty User Input

Suppose you ask the user for their name:

    name = input("Enter your name: ").strip()

The user might simply press Enter.

Then:

    name == ""

will be `True`.

You can check this with:

    if name == "":
        print("Name cannot be empty.")

This is much better than allowing an empty value to continue through the program.

---

## 15. A Shorter Empty-String Check

Python also allows:

    if not name:
        print("Name cannot be empty.")

For an empty string, Python treats the value as false in a condition.

This is called **truthiness**.

For now, the important rule is:

    "" → False

while a non-empty string behaves as true in a condition.

For example:

    name = "Ahmad"

    if name:
        print("Name was entered.")

---

## 16. Counting Words

Suppose the user enters a sentence:

    Python is easy to learn

We can count the words:

    sentence = "Python is easy to learn"

    words = sentence.split()

    count = len(words)

The result is:

    5

This is a powerful example because we are combining several concepts:

    String
    ↓
    split()
    ↓
    multiple words
    ↓
    len()
    ↓
    number of words

---

## 17. Counting Words from User Input

Ask the user for a sentence and count its words.

A possible approach:

    sentence = input("Enter a sentence: ").strip()

    words = sentence.split()

    word_count = len(words)

    print(f"Word count: {word_count}")

If the user enters:

    Python is easy to learn

the output is:

    Word count: 5

Notice that `.split()` handles multiple spaces better than manually searching for spaces.

---

## 18. Creating a Clean Sentence

Suppose the user enters:

    Python    is     very     powerful

There are many unnecessary spaces.

Using:

    words = text.split()

removes the extra whitespace between words.

Then:

    clean_text = " ".join(words)

produces:

    Python is very powerful

This is an important text-cleaning technique.

The transformation is:

    "Python    is     very     powerful"
                    ↓
                split()
                    ↓
        ["Python", "is", "very", "powerful"]
                    ↓
                join()
                    ↓
        "Python is very powerful"

---

## 19. Extracting Parts of a Name

Suppose we have:

    full_name = "Alex Johnson"

We can split it:

    parts = full_name.split()

Then:

    first_name = parts[0]
    last_name = parts[1]

Now we can use the individual values separately.

For example:

    print(f"First name: {first_name}")
    print(f"Last name: {last_name}")

Output:

    First name: Alex
    Last name: Johnson

This is useful, but there is an important limitation.

What happens with:

    Alex Michael Johnson

There are now three pieces.

Therefore, real programs must think carefully about the structure of the input they expect.

---

## 20. Splitting Only Once

Sometimes you do not want to split a string into every possible piece.

For example:

    text = "name@example.com"

You might want to separate it at `@`.

You can use:

    username, domain = text.split("@", 1)

The `1` means that the split should happen at most once.

The result is:

    username → name
    domain   → example.com

This is especially useful when working with structured text.

---

## 21. Cleaning a List of Names

Suppose the user enters:

    Ahmad, Sara, Alex

We can create clean names:

    names = input("Enter names: ").split(",")

    clean_names = [name.strip().title() for name in names]

Now the program has:

    Ahmad
    Sara
    Alex

The list comprehension may look unfamiliar at first.

Do not worry about memorizing it immediately.

The underlying process is:

    Split
    ↓
    Take each name
    ↓
    Strip spaces
    ↓
    Format the name
    ↓
    Store the cleaned result

---

## 22. A More Explicit Version

The previous example can also be written using a normal loop:

    names = input("Enter names: ").split(",")

    clean_names = []

    for name in names:
        clean_name = name.strip().title()
        clean_names.append(clean_name)

This version is longer, but it makes the algorithm easier to see.

Understanding the explicit version first is often useful before learning the shorter version.

---

## 23. Joining Cleaned Names

After cleaning the names, we can turn them back into one string:

    names = ["Ahmad", "Sara", "Alex"]

    result = ", ".join(names)

The result is:

    Ahmad, Sara, Alex

This gives us a complete data transformation:

    User input
        ↓
    Split
        ↓
    Clean
        ↓
    Format
        ↓
    Join
        ↓
    Final text

---

## 24. Building a Search Program

Ask the user for a sentence and a word.

Then determine whether the word exists.

For example:

    sentence = input("Enter a sentence: ")
    search_word = input("Search for: ")

    if search_word in sentence:
        print("Word found.")
    else:
        print("Word not found.")

This is a simple example of a program that reacts to text.

---

## 25. Case-Insensitive Searching

The previous program has a problem.

Suppose the sentence is:

    Python is powerful

and the user searches for:

    python

The exact search may fail because:

    Python

and:

    python

are different strings.

A common solution is to normalize both values:

    sentence = input("Enter a sentence: ").lower()
    search_word = input("Search for: ").lower()

    if search_word in sentence:
        print("Word found.")
    else:
        print("Word not found.")

Now capitalization does not affect the basic search.

---

## 26. Building a Text Normalizer

A text normalizer prepares user input for consistent processing.

For example:

    text = input("Enter text: ")

    text = text.strip()
    text = text.lower()

Now different forms such as:

    " PYTHON "
    "Python"
    "PYTHON"

can all become:

    "python"

This is especially useful before:

- Searching
- Comparing
- Validating
- Storing user input

---

## 27. Important Idea: Normalize Before Comparing

Suppose you want to compare two names.

The user enters:

    first_name = " Ahmad "
    second_name = "ahmad"

If you compare them directly:

    first_name == second_name

the result is:

    False

But if you normalize them:

    first_name = first_name.strip().lower()
    second_name = second_name.strip().lower()

then:

    first_name == second_name

becomes:

    True

This teaches an important programming principle:

**Before comparing user-provided text, make sure the text is in a consistent form.**

---

## 28. Common Mistake — Forgetting `strip()`

Consider:

    name = input("Name: ")

The user enters:

    Ahmad

This may look correct.

But the user could enter:

    "   Ahmad   "

If the program stores the value without cleaning it, those spaces remain part of the string.

A safer pattern is:

    name = input("Name: ").strip()

Clean data early when possible.

---

## 29. Common Mistake — Assuming Input Has the Expected Structure

Suppose your program expects:

    first_name,last_name

and the user enters:

    Ahmad,Rezaei

Splitting works:

    parts = text.split(",")

But what if the user enters:

    Ahmad

Now there is no second value.

A program should not blindly assume that user input is always valid.

This leads to a broader programming idea:

**Input should be validated before it is processed.**

You will study validation and error handling more deeply later.

---

# Practice Challenge 1 — Word Counter

Write a program that asks the user for a sentence.

The program should display:

    ----- Text Analysis -----

    Sentence: Python is easy to learn.
    Word count: 5

Requirements:

- Remove unnecessary spaces.
- Split the sentence into words.
- Count the words.
- Use an f-string.

---

# Practice Challenge 2 — Clean Name List

Ask the user to enter several names separated by commas.

Example:

    Enter names:   ahmad, sara , ALEX, john

The program should produce:

    ----- Names -----

    Ahmad
    Sara
    Alex
    John

Requirements:

- Split the input using `,`.
- Remove unnecessary spaces.
- Format each name correctly.
- Display the cleaned names.

---

# Practice Challenge 3 — Email Analyzer

Ask the user for an email address.

The program should display:

    ----- Email Analysis -----

    Email: ahmad@example.com
    Username: ahmad
    Domain: example.com

Requirements:

- Clean the input.
- Convert it to lowercase.
- Separate the username and domain.
- Use string operations rather than manually typing the result.

---

# Practice Challenge 4 — Text Normalizer

Ask the user for a sentence.

The sentence may contain:

- Extra spaces
- Uppercase letters
- Lowercase letters

Convert it into a clean sentence with:

- One space between words
- Lowercase letters

Example:

    Input:
       PYTHON     IS       VERY     POWERFUL

    Output:
    python is very powerful

Think about why `split()` followed by `join()` is useful here.

---

# Practice Challenge 5 — Simple Search Engine

Ask the user for:

- A sentence
- A search word

The program should perform a case-insensitive search.

Example:

    Sentence: Python is a powerful programming language.
    Search: PYTHON

Output:

    Result: Found

If the word does not exist:

    Result: Not found

---

# Final Challenge — Contact List Processor

Do not look at the answer before trying to solve the problem.

Build a program that receives several contacts from the user.

The user enters contacts using this format:

    Ahmad Rezaei:ahmad@example.com,Sara Smith:sara@example.com,Alex Johnson:alex@example.com

The program should process the input and produce:

    ----- Contact List -----

    1. Ahmad Rezaei
       Email: ahmad@example.com

    2. Sara Smith
       Email: sara@example.com

    3. Alex Johnson
       Email: alex@example.com

The program should:

1. Receive the complete string from the user.
2. Split the contacts using `,`.
3. Process each contact separately.
4. Separate the name from the email using `:`.
5. Clean unnecessary spaces.
6. Format the name correctly.
7. Convert the email to lowercase.
8. Display the contacts in a readable format.

Think about the problem as a sequence of transformations:

    Raw input
        ↓
    Split contacts
        ↓
    Process one contact
        ↓
    Split name and email
        ↓
    Clean values
        ↓
    Format values
        ↓
    Display result

The challenge is not mainly about syntax.

It is about learning how to take a large string containing structured information and gradually transform it into useful pieces of data.

---

# Final Challenge — Answer

Try to solve the challenge yourself first.

One possible solution is:

    contacts_text = input("Enter contacts: ").strip()

    contacts = contacts_text.split(",")

    print()
    print("----- Contact List -----")
    print()

    number = 1

    for contact in contacts:
        name, email = contact.split(":", 1)

        name = name.strip().title()
        email = email.strip().lower()

        print(f"{number}. {name}")
        print(f"   Email: {email}")
        print()

        number += 1

Notice how the solution follows the same algorithm:

    Input
        ↓
    Split contacts
        ↓
    Loop through contacts
        ↓
    Split each contact
        ↓
    Clean values
        ↓
    Format values
        ↓
    Display

The important lesson is that strings can contain structured information.

Once you learn how to split, clean, search, normalize, and join strings, you can begin turning raw text into data that a program can actually work with.

---

