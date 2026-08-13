# Part 1 — What Is a List?

> 🌐 Language: **English** | [فارسی](fa/README.md)

A **List** is one of Python's most important built-in data structures.

It allows us to store multiple values inside a single variable and work with those values as one collection.

Before learning Lists, we often stored values separately:

```python
student1 = "Ahmad"
student2 = "Sara"
student3 = "Alex"
student4 = "John"
```

This approach becomes inconvenient as the amount of data grows.

If we have 100 students, creating 100 separate variables is not a practical solution.

A List allows us to represent the same data as one collection:

```python
students = ["Ahmad", "Sara", "Alex", "John"]
```

Now `students` represents the entire collection.

---

## What Is a List?

A List is an **ordered collection of elements**.

For example:

```python
students = ["Ahmad", "Sara", "Alex", "John"]
```

This List contains four elements:

```text
Ahmad
Sara
Alex
John
```

Each element is stored at a specific position.

These positions are called **indexes**, which we will study in detail in the next part.

For now, the important idea is:

```text
List
 ├── Element
 ├── Element
 ├── Element
 └── Element
```

A List lets us treat multiple related values as one collection.

---

## Creating a List

Lists are created using **square brackets** `[]`.

The general structure is:

```python
list_name = [value1, value2, value3]
```

For example:

```python
numbers = [10, 20, 30, 40, 50]
```

Another example:

```python
colors = ["red", "green", "blue"]
```

And another:

```python
cities = ["Tehran", "Shiraz", "Tabriz", "Mashhad"]
```

The elements are separated by commas.

---

## Lists Can Store Strings

A List can contain multiple Strings:

```python
programming_languages = ["Python", "Java", "C++", "JavaScript"]
```

This is useful when we have a collection of related textual data.

For example:

```python
favorite_foods = ["Pizza", "Burger", "Pasta", "Rice", "Sushi"]
```

The variable `favorite_foods` now represents an entire collection instead of one food.

---

## Lists Can Store Numbers

Lists can also contain integers:

```python
scores = [18, 15, 20, 17, 19]
```

Or floating-point numbers:

```python
prices = [12.5, 20.75, 8.99, 15.25]
```

This makes Lists particularly useful for processing numerical data.

For example:

```python
temperatures = [22, 24, 27, 25, 21]
```

Later, we can use Python's built-in functions and List methods to process this data.

---

## Lists Can Contain Different Data Types

Python Lists are not restricted to one data type.

For example:

```python
person = ["Ahmad", 25, 175.5, True]
```

This List contains:

```text
"Ahmad" → String
25      → Integer
175.5   → Float
True    → Boolean
```

Python allows this because a List is a general-purpose collection.

However, in well-designed programs, Lists often contain values that have a logical relationship.

For example:

```python
ages = [18, 21, 25, 30]
```

is a natural collection because all elements represent ages.

Compare that with:

```python
data = ["Ahmad", 25, True, 175.5]
```

This is valid Python, but the elements represent completely different kinds of information.

Whether a mixed List is appropriate depends on the problem being solved.

---

## Lists Are Ordered

One of the fundamental characteristics of a List is that the elements have an order.

Consider:

```python
numbers = [10, 20, 30, 40]
```

The order is:

```text
10 → 20 → 30 → 40
```

If we create another List:

```python
numbers = [40, 30, 20, 10]
```

the collection contains the same values but in a different order.

This difference matters because the position of an element is part of the List's structure.

---

## An Empty List

A List does not have to contain elements when it is created.

We can create an empty List:

```python
students = []
```

At this point, the List contains zero elements.

Empty Lists are especially useful when we want to build a collection during program execution.

For example:

```python
students = []

print(students)
```

Output:

```text
[]
```

Later, elements can be added to the List.

We will study adding elements in the List methods section.

---

## Finding the Number of Elements

Python provides the built-in `len()` function for finding the number of elements in a List.

For example:

```python
students = ["Ahmad", "Sara", "Alex"]

print(len(students))
```

Output:

```text
3
```

There are three elements in the List.

Another example:

```python
numbers = [10, 20, 30, 40, 50]

print(len(numbers))
```

Output:

```text
5
```

For an empty List:

```python
students = []

print(len(students))
```

Output:

```text
0
```

So we can think of:

```text
len(list) → number of elements
```

This function will become extremely useful when working with Lists.

---

## Lists and Variables

A List does not replace variables.

Instead, it gives a variable the ability to represent a collection.

For example:

```python
name = "Ahmad"
```

The variable `name` represents one value.

But:

```python
names = ["Ahmad", "Sara", "Alex"]
```

The variable `names` represents a collection of values.

This distinction is important:

```text
Variable → one value

List variable → collection of values
```

---

## Why Lists Are Important

Lists become important when programs need to work with collections of data.

Common examples include:

```text
Student names
Student scores
Products
Prices
Temperatures
Usernames
Questions
Answers
Tasks
Messages
Files
```

For example, a Todo application could store tasks in a List:

```python
tasks = [
    "Study Python",
    "Practice Lists",
    "Read a book",
    "Exercise"
]
```

A shopping application could store products:

```python
cart = [
    "Laptop",
    "Mouse",
    "Keyboard"
]
```

A quiz application could store questions:

```python
questions = [
    "What is Python?",
    "What is a variable?",
    "What is a List?"
]
```

The same basic structure can be used in many different types of applications.

---

## Lists and Loops

Lists become much more powerful when combined with loops.

We already learned about loops in the previous lesson.

For example:

```python
students = ["Ahmad", "Sara", "Alex"]

for student in students:
    print(student)
```

Output:

```text
Ahmad
Sara
Alex
```

The loop processes each element in the List.

This is one of the most important patterns we will use throughout the List lesson.

Instead of writing:

```python
print(students[0])
print(students[1])
print(students[2])
```

we can use a loop to process the collection.

This becomes particularly important when the number of elements is unknown.

---

## Lists and Data Processing

Consider a List of student scores:

```python
scores = [18, 8, 15, 7, 20]
```

We can process every score using a loop:

```python
scores = [18, 8, 15, 7, 20]

for score in scores:
    print(score)
```

Output:

```text
18
8
15
7
20
```

Now imagine that instead of five scores, we have 500 scores.

The same loop can still process the entire collection.

This is one of the major advantages of using data structures.

We write a general solution that works with a collection rather than creating separate code for every individual value.

---

## A Practical Example — Student Scores

Let's build a small example using concepts we already know.

```python
scores = [18, 8, 15, 7, 20]

print("----- Student Scores -----")
print()

print(f"Scores: {scores}")

number_of_scores = len(scores)
total = sum(scores)
average = total / number_of_scores

print(f"Number of scores: {number_of_scores}")
print(f"Total: {total}")
print(f"Average: {average}")
print()

for score in scores:
    if score >= 10:
        print(f"{score} → Passing")
    else:
        print(f"{score} → Failing")
```

This example combines several concepts we have already learned:

```text
List
Variables
len()
sum()
Arithmetic
f-strings
for loops
if/else
```

This is an important transition.

We are no longer working only with individual values.

We are now working with **collections of data**.

---

## Lists as a Foundation for Algorithms

Lists are not only useful for storing data.

They also provide a foundation for solving more complex problems.

Suppose the problem is:

> Find the highest score among several students.

Instead of thinking about five independent variables, we can represent the problem as:

```text
Input
  ↓
List of scores
  ↓
Process the elements
  ↓
Compare values
  ↓
Find the highest value
  ↓
Output
```

The important idea is that the algorithm can operate on the collection.

Whether the List contains five values or five thousand values, the general problem remains the same.

This is one of the first steps toward thinking algorithmically about data structures.

---

## Lists vs Separate Variables

Consider this approach:

```python
student1 = "Ahmad"
student2 = "Sara"
student3 = "Alex"
student4 = "John"
student5 = "Mary"
```

Now compare it with:

```python
students = ["Ahmad", "Sara", "Alex", "John", "Mary"]
```

The List-based approach gives us one collection that can be processed systematically.

For example:

```python
students = ["Ahmad", "Sara", "Alex", "John", "Mary"]

for student in students:
    print(student)
```

If the number of students changes, the loop does not need to change.

This is a major improvement in scalability and maintainability.

---

## What We Will Learn About Lists

The concept of a List is much larger than simply creating one with square brackets.

Throughout this lesson, we will learn how to:

1. Create Lists
2. Access elements
3. Use positive indexes
4. Use negative indexes
5. Modify elements
6. Add elements
7. Remove elements
8. Search Lists
9. Check whether an element exists
10. Find the length of a List
11. Iterate over Lists
12. Slice Lists
13. Copy Lists
14. Sort Lists
15. Reverse Lists
16. Work with nested Lists
17. Use important List methods
18. Combine Lists with conditions and loops
19. Solve practical data-processing problems

We will also connect Lists to concepts learned previously, especially:

```text
Variables
Data Types
Conditions
Loops
Functions
Strings
```

This connection is important because real Python programs rarely use one concept in isolation.

---

# Key Takeaways

A List is an ordered collection of elements.

Lists are created using square brackets:

```python
numbers = [10, 20, 30]
```

A List can contain Strings:

```python
names = ["Ahmad", "Sara", "Alex"]
```

A List can contain numbers:

```python
scores = [18, 15, 20]
```

A List can contain different data types:

```python
person = ["Ahmad", 25, True]
```

An empty List is created with:

```python
items = []
```

The `len()` function returns the number of elements:

```python
items = ["A", "B", "C"]

print(len(items))
```

Output:

```text
3
```

Lists can be processed naturally with loops:

```python
items = ["A", "B", "C"]

for item in items:
    print(item)
```

The most important idea of this Part is:

> **A List allows us to represent and process a collection of related values as one data structure.**

---

# Practice

## Exercise 1 — Favorite Foods

Create a List called `favorite_foods` containing at least five foods.

Print the List.

```python
favorite_foods = ["Pizza", "Burger", "Pasta", "Rice", "Sushi"]

print(favorite_foods)
```

---

## Exercise 2 — Programming Languages

Create a List containing at least five programming languages.

Print the List and its length.

---

## Exercise 3 — Student Scores

Create a List containing the scores of five students.

Calculate:

- Number of scores
- Total score
- Average score

Use `len()` and `sum()`.

---

## Exercise 4 — Shopping Cart

Create a List called `cart` containing several products.

Use a `for` loop to display every product.

---

## Exercise 5 — Mixed Data

Create a List containing:

- Your name
- Your age
- Your height
- A Boolean value representing whether you are learning Python

Then inspect the type of each value.

---

## Exercise 6 — Conceptual Question

Explain why this approach:

```python
student1 = "Ahmad"
student2 = "Sara"
student3 = "Alex"
student4 = "John"
```

is generally less practical than:

```python
students = ["Ahmad", "Sara", "Alex", "John"]
```

Your answer should focus on how collections make data easier to process.

---

# Section Challenge — Student Score Analyzer

Create a program that stores several student scores in a List.

Your program should:

1. Create a List containing at least five scores.
2. Display the List.
3. Display the number of scores.
4. Calculate and display the total.
5. Calculate and display the average.
6. Use a loop to examine every score.
7. Display whether each score is `Passing` or `Failing`.
8. Use concepts from previous lessons such as Lists, Variables, `len()`, `sum()`, Loops, Conditions, and f-strings.

Example structure:

```python
scores = [18, 8, 15, 7, 20]

print("----- Student Score Analyzer -----")
print()

print(f"Scores: {scores}")

number_of_scores = len(scores)
total = sum(scores)
average = total / number_of_scores

print(f"Number of scores: {number_of_scores}")
print(f"Total: {total}")
print(f"Average: {average}")
print()

for score in scores:
    if score >= 10:
        print(f"{score} → Passing")
    else:
        print(f"{score} → Failing")
```

Try to build your own version before comparing it with the example.

The goal of this challenge is not merely to create a List.

The goal is to understand why Lists are useful when a program needs to work with a **collection of data**.

---

# Part 2 — List Indexing and Accessing Elements

In the previous Part, we learned that a List is an ordered collection of elements.

For example:

```python
students = ["Ahmad", "Sara", "Alex", "John"]
```

The List contains four elements, and each element has a specific position.

In Python, we use **indexing** to access an individual element of a List.

Understanding indexing is one of the most important skills when working with Lists because it allows us to select, inspect, and later modify specific elements.

---

## What Is an Index?

An **index** is the position of an element inside a List.

Python uses **zero-based indexing**.

This means that the first element has index `0`, not `1`.

Consider this List:

```python
students = ["Ahmad", "Sara", "Alex", "John"]
```

The indexes are:

```text
Element    Index

Ahmad      0
Sara       1
Alex       2
John       3
```

So:

```text
First element  → index 0
Second element → index 1
Third element  → index 2
Fourth element → index 3
```

This is a fundamental rule in Python.

---

## Accessing the First Element

To access an element, we place its index inside square brackets after the List name.

For example:

```python
students = ["Ahmad", "Sara", "Alex", "John"]

print(students[0])
```

Output:

```text
Ahmad
```

Because `Ahmad` is the first element, its index is `0`.

---

## Accessing Other Elements

We can use different indexes to access different elements.

```python
students = ["Ahmad", "Sara", "Alex", "John"]

print(students[0])
print(students[1])
print(students[2])
print(students[3])
```

Output:

```text
Ahmad
Sara
Alex
John
```

Each index points to one specific element.

---

## Visualizing List Indexes

It is useful to visualize the List like this:

```text
Index:      0        1        2        3
            ↓        ↓        ↓        ↓
List:    ["Ahmad",  "Sara",  "Alex",  "John"]
```

The index tells Python which element we want.

For example:

```python
students[0]
```

means:

```text
Give me the element at index 0.
```

And:

```python
students[2]
```

means:

```text
Give me the element at index 2.
```

---

## Indexing Numbers

Indexing is not limited to Strings.

For example:

```python
scores = [18, 8, 15, 7, 20]

print(scores[0])
print(scores[2])
print(scores[4])
```

Output:

```text
18
15
20
```

The List is:

```text
Index:     0    1    2    3    4
           ↓    ↓    ↓    ↓    ↓
Scores:   18    8   15    7   20
```

Therefore:

```python
scores[0]  # 18
scores[2]  # 15
scores[4]  # 20
```

---

## Why Does Python Start from Zero?

Zero-based indexing may initially feel strange.

If a List contains five elements, you might expect the positions to be:

```text
1  2  3  4  5
```

But Python uses:

```text
0  1  2  3  4
```

The reason is that indexing represents the **offset from the beginning** of the collection.

The first element is zero positions away from the beginning.

The second element is one position away.

The third element is two positions away.

And so on.

You do not need to memorize the historical reasons behind zero-based indexing.

The practical rule is enough:

> **In Python, the first element of a List has index 0.**

---

## The Last Index

A very important rule is:

```text
Last index = length - 1
```

For example:

```python
numbers = [10, 20, 30, 40, 50]
```

The List has five elements:

```python
len(numbers)
```

returns:

```text
5
```

But the indexes are:

```text
0  1  2  3  4
```

Therefore the last index is:

```text
5 - 1 = 4
```

So:

```python
numbers[4]
```

returns:

```text
50
```

This relationship is extremely important:

```text
Last index = len(list) - 1
```

---

## Accessing the Last Element

We can access the last element using its positive index.

For example:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[4])
```

Output:

```text
50
```

However, Python provides an even more convenient way to access the last element.

We can use **negative indexing**.

---

## Negative Indexing

Python allows us to count from the end of a List using negative indexes.

For example:

```python
numbers = [10, 20, 30, 40, 50]
```

The indexes can be viewed like this:

```text
Positive Index:

Index:      0    1    2    3    4
            ↓    ↓    ↓    ↓    ↓
List:      10   20   30   40   50


Negative Index:

Index:     -5   -4   -3   -2   -1
            ↓    ↓    ↓    ↓    ↓
List:      10   20   30   40   50
```

The negative indexes start from `-1`.

So:

```text
-1 → Last element
-2 → Second-to-last element
-3 → Third-to-last element
```

---

## Accessing the Last Element with -1

For example:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[-1])
```

Output:

```text
50
```

This is one of the most commonly used indexing techniques in Python.

Instead of calculating the last positive index:

```python
print(numbers[len(numbers) - 1])
```

we can simply write:

```python
print(numbers[-1])
```

The second version is shorter and clearer.

---

## Accessing Elements from the End

We can use other negative indexes as well.

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[-1])
print(numbers[-2])
print(numbers[-3])
```

Output:

```text
50
40
30
```

So:

```text
-1 → 50
-2 → 40
-3 → 30
```

Negative indexing is especially useful when we care about elements near the end of a List.

---

## Positive and Negative Indexes Refer to the Same Elements

Positive and negative indexes can refer to the same element.

For example:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[0])
print(numbers[-5])
```

Both produce:

```text
10
```

Similarly:

```python
print(numbers[1])
print(numbers[-4])
```

Both produce:

```text
20
```

And:

```python
print(numbers[4])
print(numbers[-1])
```

Both produce:

```text
50
```

We can think of the List like this:

```text
Positive:   0    1    2    3    4
            ↓    ↓    ↓    ↓    ↓
Values:    10   20   30   40   50
            ↑    ↑    ↑    ↑    ↑
Negative:  -5   -4   -3   -2   -1
```

---

## Indexing Strings Inside Lists

A List can contain Strings, and each String can itself be indexed.

For example:

```python
names = ["Ahmad", "Sara", "Alex"]

print(names[0])
```

Output:

```text
Ahmad
```

Here:

```python
names[0]
```

returns the first String.

We can then index the String itself:

```python
print(names[0][0])
```

Output:

```text
A
```

This happens because:

```text
names[0]     → "Ahmad"
names[0][0]  → "A"
```

This introduces an important idea:

> **Python allows us to combine indexing operations when working with nested sequences.**

We will explore this idea more deeply later.

---

## Indexing with Variables

The index does not have to be written directly as a number.

We can store the index in a variable.

For example:

```python
students = ["Ahmad", "Sara", "Alex", "John"]

index = 2

print(students[index])
```

Output:

```text
Alex
```

Here:

```python
index = 2
```

and:

```python
students[index]
```

is equivalent to:

```python
students[2]
```

This becomes useful when the index is determined dynamically by the program.

---

## Using Input as an Index

Because an index can come from a variable, it can also come from user input.

For example:

```python
students = ["Ahmad", "Sara", "Alex", "John"]

index = int(input("Enter an index: "))

print(students[index])
```

If the user enters:

```text
2
```

the program prints:

```text
Alex
```

This demonstrates an important connection between concepts we have already learned:

```text
Input
  ↓
Type Casting
  ↓
Variable
  ↓
List Indexing
  ↓
Output
```

---

## IndexError

What happens if we try to access an index that does not exist?

Consider:

```python
students = ["Ahmad", "Sara", "Alex"]

print(students[5])
```

This List contains only three elements.

Its valid positive indexes are:

```text
0
1
2
```

Index `5` does not exist.

Python therefore raises an error:

```text
IndexError: list index out of range
```

This error is called an **IndexError**.

---

## Understanding "List Index Out of Range"

The phrase:

```text
list index out of range
```

means:

> The requested index is outside the valid range of indexes for that List.

For example:

```python
numbers = [10, 20, 30]
```

Valid indexes:

```text
0
1
2
```

Invalid indexes:

```text
3
4
5
...
```

Some negative indexes are also invalid.

For example:

```python
numbers[-4]
```

is invalid because the List contains only three elements.

---

## How to Avoid Index Errors

Before using an index, we need to understand the size of the List.

For example:

```python
numbers = [10, 20, 30, 40, 50]

print(len(numbers))
```

Output:

```text
5
```

Therefore the valid positive indexes are:

```text
0 through 4
```

A useful relationship is:

```text
0 <= index < len(list)
```

For a List with five elements:

```text
0 <= index < 5
```

Therefore:

```text
0
1
2
3
4
```

are valid indexes.

---

## Checking an Index with a Condition

We can use a condition to make sure an index is valid before accessing the List.

For example:

```python
students = ["Ahmad", "Sara", "Alex"]

index = 2

if 0 <= index < len(students):
    print(students[index])
else:
    print("Invalid index")
```

Output:

```text
Alex
```

If the index were:

```python
index = 5
```

the program would print:

```text
Invalid index
```

This combines several concepts:

```text
List
len()
Variable
Condition
Indexing
```

---

## Indexing and Loops

We can combine indexing with loops.

For example:

```python
students = ["Ahmad", "Sara", "Alex", "John"]

for index in range(len(students)):
    print(index, students[index])
```

Output:

```text
0 Ahmad
1 Sara
2 Alex
3 John
```

Here:

```python
range(len(students))
```

generates the valid positive indexes.

Then:

```python
students[index]
```

accesses the element at that index.

This is an important pattern.

However, when we only need the values and do not need their indexes, Python provides a simpler approach:

```python
for student in students:
    print(student)
```

We will compare these approaches more deeply when we study List iteration.

---

## A Practical Example — Student Scores

Let's use indexing in a realistic example.

```python
scores = [18, 8, 15, 7, 20]

print("----- Student Scores -----")
print()

print(f"First score: {scores[0]}")
print(f"Second score: {scores[1]}")
print(f"Last score: {scores[-1]}")
```

Output:

```text
----- Student Scores -----

First score: 18
Second score: 8
Last score: 20
```

This example demonstrates both positive and negative indexing.

---

## Another Practical Example — Accessing Product Information

Suppose an online store has a List of products:

```python
products = ["Laptop", "Mouse", "Keyboard", "Monitor"]
```

We can access specific products:

```python
print(f"First product: {products[0]}")
print(f"Last product: {products[-1]}")
```

Output:

```text
First product: Laptop
Last product: Monitor
```

This pattern appears frequently in real programs.

---

## A Practical Example — Selecting a Menu Item

Imagine a simple menu:

```python
menu = ["Pizza", "Burger", "Pasta", "Salad"]
```

We can select a specific item:

```python
choice = 2

print(f"You selected: {menu[choice]}")
```

Output:

```text
You selected: Pasta
```

The important idea is that the index can come from the program rather than being hard-coded.

---

## Indexing Is Not Slicing

It is important to distinguish between **indexing** and **slicing**.

Indexing selects one element:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[2])
```

Output:

```text
30
```

Slicing selects a range of elements:

```python
print(numbers[1:4])
```

Output:

```text
[20, 30, 40]
```

We will study slicing separately because it has its own rules.

For now:

```text
Indexing → one element

Slicing → a range of elements
```

---

## The Most Important Indexing Rules

There are several rules you should remember.

### Rule 1 — Indexing Starts at Zero

```python
numbers = [10, 20, 30]

print(numbers[0])
```

Output:

```text
10
```

---

### Rule 2 — The Last Positive Index Is Length Minus One

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[len(numbers) - 1])
```

Output:

```text
50
```

---

### Rule 3 — -1 Means the Last Element

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[-1])
```

Output:

```text
50
```

---

### Rule 4 — Negative Indexes Count from the End

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[-2])
```

Output:

```text
40
```

---

### Rule 5 — Invalid Indexes Cause IndexError

```python
numbers = [10, 20, 30]

print(numbers[5])
```

This causes:

```text
IndexError: list index out of range
```

---

# Key Takeaways

Indexing allows us to access individual elements of a List.

Python uses zero-based indexing.

For example:

```python
students = ["Ahmad", "Sara", "Alex", "John"]
```

The indexes are:

```text
Index:      0        1        2        3
            ↓        ↓        ↓        ↓
List:    ["Ahmad",  "Sara",  "Alex",  "John"]
```

The first element is accessed with:

```python
students[0]
```

The last element can be accessed with:

```python
students[-1]
```

The second-to-last element can be accessed with:

```python
students[-2]
```

The last positive index is:

```text
len(list) - 1
```

A valid positive index follows:

```text
0 <= index < len(list)
```

An invalid index produces:

```text
IndexError
```

The most important idea of this Part is:

> **Indexing gives us precise control over individual elements inside a List.**

---

# Practice

## Exercise 1 — Basic Indexing

Create the following List:

```python
fruits = ["Apple", "Banana", "Orange", "Mango", "Grape"]
```

Print:

- The first element
- The second element
- The third element
- The last element

Use both positive and negative indexes where appropriate.

---

## Exercise 2 — Student Scores

Create:

```python
scores = [18, 8, 15, 7, 20]
```

Print:

- First score
- Third score
- Last score
- Second-to-last score

---

## Exercise 3 — Index Mapping

Create a List containing at least six elements.

Write down the positive and negative index of every element.

For example:

```text
Positive Index    Value    Negative Index
0                 A        -6
1                 B        -5
...
```

---

## Exercise 4 — Dynamic Index

Create a List of several cities.

Store an index inside a variable and use that variable to access an element.

For example:

```python
cities = ["Tehran", "Shiraz", "Tabriz", "Mashhad"]

index = 2

print(cities[index])
```

Then change the value of `index` and observe the result.

---

## Exercise 5 — User Selected Element

Create a List of several favorite foods.

Ask the user for an index and display the corresponding food.

Use `input()` and type casting.

Make sure the index is valid before accessing the List.

---

## Exercise 6 — Avoid IndexError

Create a List and ask the user for an index.

Use a condition to check whether the index is valid.

If the index is valid, print the element.

Otherwise, print:

```text
Invalid index
```

---

# Section Challenge — Student Score Selector

Create a program that stores several student scores in a List.

The program should:

1. Display the List.
2. Display the number of scores.
3. Ask the user to enter an index.
4. Check whether the index is valid.
5. If valid, display the selected score.
6. If invalid, display an appropriate message.
7. Also display the first and last scores.

Example structure:

```python
scores = [18, 8, 15, 7, 20]

print("----- Student Score Selector -----")
print()

print(f"Scores: {scores}")
print(f"Number of scores: {len(scores)}")
print(f"First score: {scores[0]}")
print(f"Last score: {scores[-1]}")
print()

index = int(input("Enter an index: "))

if 0 <= index < len(scores):
    print(f"Selected score: {scores[index]}")
else:
    print("Invalid index")
```

Before looking at the example, try to build your own solution.

The goal of this challenge is to connect concepts from previous lessons:

```text
Lists
Variables
Input
Type Casting
len()
Conditions
Indexing
Output
```

The next step is to learn how indexing can be used not only to read elements, but also to **modify elements inside a List**.

---

# Part 3 — Modifying List Elements

In this section, we learn how to modify existing elements inside a Python List.

## What We Will Learn

- Modifying a List element using its index
- Replacing the first and last elements
- Using positive and negative indexes
- Using variables as indexes
- Updating values based on their current values
- Using augmented assignment operators
- Modifying List elements with conditions
- Modifying List elements inside loops
- Understanding List mutability
- Common mistakes
- Practical examples
- Exercises
- Section Challenge

---

## 1. Modifying a List Element

In the previous section, we learned how to access an element:

```python
fruits = ["Apple", "Banana", "Orange"]

print(fruits[1])
```

Output:

```text
Banana
```

The same index can be used to replace the element:

```python
fruits = ["Apple", "Banana", "Orange"]

fruits[1] = "Mango"

print(fruits)
```

Output:

```text
['Apple', 'Mango', 'Orange']
```

The general syntax is:

```python
list_name[index] = new_value
```

The value at that index is replaced with the new value.

---

## 2. Modifying the First Element

Because the first element has index `0`, we can modify it like this:

```python
colors = ["Red", "Blue", "Green"]

colors[0] = "Yellow"

print(colors)
```

Output:

```text
['Yellow', 'Blue', 'Green']
```

---

## 3. Modifying the Last Element

Negative indexing can also be used when modifying elements.

```python
colors = ["Red", "Blue", "Green"]

colors[-1] = "Purple"

print(colors)
```

Output:

```text
['Red', 'Blue', 'Purple']
```

Remember:

```text
-1 → Last element
-2 → Second-to-last element
```

---

## 4. Modifying Numeric Elements

List elements can contain numbers as well as Strings.

```python
scores = [18, 8, 15, 7, 20]

scores[1] = 12

print(scores)
```

Output:

```text
[18, 12, 15, 7, 20]
```

Only the element at index `1` was changed.

---

## 5. Modifying Multiple Elements

Several elements can be modified through separate assignments.

```python
scores = [18, 8, 15, 7, 20]

scores[1] = 12
scores[3] = 14

print(scores)
```

Output:

```text
[18, 12, 15, 14, 20]
```

Each assignment modifies the element at its specified index.

---

## 6. Using a Variable as the Index

The index does not have to be written directly inside the brackets.

It can be stored in a variable:

```python
students = ["Ahmad", "Sara", "Alex", "John"]

index = 2

students[index] = "Michael"

print(students)
```

Output:

```text
['Ahmad', 'Sara', 'Michael', 'John']
```

This becomes particularly useful when the position is determined dynamically.

---

## 7. Using a Variable as the New Value

The replacement value can also be stored in a variable:

```python
students = ["Ahmad", "Sara", "Alex", "John"]

new_name = "Michael"

students[2] = new_name

print(students)
```

Output:

```text
['Ahmad', 'Sara', 'Michael', 'John']
```

Both the index and the replacement value can therefore be dynamic:

```python
index = 2
new_name = "Michael"

students[index] = new_name
```

---

## 8. Updating an Element Using Its Current Value

We can read the current value, modify it, and assign the result back to the same position.

```python
scores = [18, 8, 15, 7, 20]

scores[1] = scores[1] + 2

print(scores)
```

Output:

```text
[18, 10, 15, 7, 20]
```

The expression:

```python
scores[1] + 2
```

first reads the current value and then adds `2`.

The result is assigned back to:

```python
scores[1]
```

---

## 9. Augmented Assignment

Python provides shorter ways to update numeric values.

Instead of:

```python
scores[1] = scores[1] + 2
```

we can write:

```python
scores[1] += 2
```

Example:

```python
scores = [18, 8, 15, 7, 20]

scores[1] += 2

print(scores)
```

Output:

```text
[18, 10, 15, 7, 20]
```

Other augmented assignment operators include:

```python
scores[1] -= 2
scores[1] *= 2
scores[1] /= 2
```

These are especially useful when working with numeric Lists.

---

## 10. Modifying Elements with Negative Indexing

Negative indexes can also be used with calculations:

```python
numbers = [10, 20, 30, 40, 50]

numbers[-1] += 10

print(numbers)
```

Output:

```text
[10, 20, 30, 40, 60]
```

The last element was increased by `10`.

---

## 11. Modifying an Element with a Condition

We can combine List modification with conditions.

```python
scores = [18, 8, 15, 7, 20]

if scores[1] < 10:
    scores[1] = 10

print(scores)
```

Output:

```text
[18, 10, 15, 7, 20]
```

The value is changed only when the condition is true.

This gives us an important pattern:

```text
Read element
    ↓
Check condition
    ↓
Modify element
```

---

## 12. Modifying List Elements Inside a Loop

We can use a loop and an index to examine and modify every element.

```python
scores = [8, 12, 7, 18, 9]

for index in range(len(scores)):
    if scores[index] < 10:
        scores[index] = 10

print(scores)
```

Output:

```text
[10, 12, 10, 18, 10]
```

The program examines every position.

If the score is below `10`, it replaces that score with `10`.

This pattern is extremely useful when processing List data.

---

## 13. Practical Example — Correcting Scores

Suppose some student scores were entered incorrectly.

```python
scores = [18, 8, 15, 7, 20]

print("----- Score Correction -----")
print()

print(f"Original scores: {scores}")

scores[1] = 13

print(f"Updated scores: {scores}")
```

Output:

```text
----- Score Correction -----

Original scores: [18, 8, 15, 7, 20]
Updated scores: [18, 13, 15, 7, 20]
```

Only one existing element was replaced.

---

## 14. Practical Example — Updating a Menu

A restaurant menu can also be modified:

```python
menu = ["Pizza", "Burger", "Pasta", "Salad"]

menu[3] = "Steak"

print(menu)
```

Output:

```text
['Pizza', 'Burger', 'Pasta', 'Steak']
```

The List itself remains the same List; only one of its existing elements changes.

---

## 15. Practical Example — Updating Inventory

Suppose we store the quantity of products:

```python
stock = [15, 8, 20, 5]

stock[1] = 12

print(stock)
```

Output:

```text
[15, 12, 20, 5]
```

The quantity at index `1` has been updated.

---

## 16. What Does Mutable Mean?

A List is a **mutable** data type.

Mutable means that the contents of the List can be changed after the List has been created.

For example:

```python
numbers = [10, 20, 30]

numbers[0] = 100

print(numbers)
```

Output:

```text
[100, 20, 30]
```

The List was created first and then one of its existing elements was modified.

This concept will become important later when we compare Lists with **Tuples**, because Tuples are immutable.

---

## 17. Modifying a List Does Not Change Its Length

Replacing an existing element does not change the number of elements.

```python
numbers = [10, 20, 30]

print(len(numbers))

numbers[1] = 200

print(numbers)
print(len(numbers))
```

Output:

```text
3
[10, 200, 30]
3
```

The value changed, but the number of elements remained `3`.

Adding and removing elements are different operations and will be covered in later sections.

---

## 18. Invalid Indexes Cannot Be Used for Modification

The index must already exist.

This is invalid:

```python
numbers = [10, 20, 30]

numbers[5] = 100
```

Python raises:

```text
IndexError: list assignment index out of range
```

An assignment through indexing replaces an existing element.

It does not automatically create missing positions.

For example:

```python
numbers = [10, 20, 30]

numbers[5] = 100
```

does not create indexes `3` and `4`.

When we want to add new elements, we will use List methods such as `append()` and `insert()`.

---

## 19. Reading vs Modifying

These two operations should not be confused.

Reading:

```python
numbers = [10, 20, 30]

print(numbers[2])
```

Output:

```text
30
```

Modifying:

```python
numbers[2] = 100
```

Now the List becomes:

```text
[10, 20, 100]
```

Complete example:

```python
numbers = [10, 20, 30]

print(numbers[2])

numbers[2] = 100

print(numbers)
```

Output:

```text
30
[10, 20, 100]
```

---

## 20. A Complete Practical Example

Let's create a small score correction system:

```python
scores = [18, 8, 15, 7, 20]

print("----- Score Correction -----")
print()

print(f"Original scores: {scores}")

for index in range(len(scores)):
    if scores[index] < 10:
        scores[index] = 10

print(f"Updated scores: {scores}")
```

Output:

```text
----- Score Correction -----

Original scores: [18, 8, 15, 7, 20]
Updated scores: [18, 10, 15, 10, 20]
```

This example combines several concepts from previous lessons:

```text
Lists
Variables
Indexing
len()
range()
for loops
Conditions
Assignment
```

---

# Common Mistakes

## Mistake 1 — Forgetting Zero-Based Indexing

The first element is at index `0`:

```python
numbers = [10, 20, 30]

numbers[0] = 100

print(numbers)
```

Output:

```text
[100, 20, 30]
```

---

## Mistake 2 — Using an Index That Does Not Exist

This causes an error:

```python
numbers = [10, 20, 30]

numbers[3] = 100
```

The valid positive indexes are:

```text
0
1
2
```

---

## Mistake 3 — Confusing Replacement with Adding

This:

```python
numbers[1] = 100
```

replaces the existing element at index `1`.

It does not add another element.

```python
numbers = [10, 20, 30]

numbers[1] = 100

print(numbers)
```

Output:

```text
[10, 100, 30]
```

The List still contains three elements.

---

## Mistake 4 — Expecting Missing Positions to Be Created

This is invalid:

```python
numbers = [10, 20, 30]

numbers[5] = 100
```

The List does not automatically create missing positions.

Adding new elements requires List methods such as `append()` or `insert()`.

---

# Key Takeaways

The main syntax for modifying an existing List element is:

```python
list_name[index] = new_value
```

Lists are mutable:

```python
numbers = [10, 20, 30]

numbers[1] = 100

print(numbers)
```

Output:

```text
[10, 100, 30]
```

Negative indexing can also be used:

```python
numbers[-1] = 500
```

An element can be updated based on its current value:

```python
numbers[1] += 10
```

A variable can be used as the index:

```python
index = 1

numbers[index] = 100
```

Conditions and loops can be combined with indexing:

```python
for index in range(len(scores)):
    if scores[index] < 10:
        scores[index] = 10
```

The central idea of this section is:

> **A List is mutable, so existing elements can be changed by assigning a new value to their indexes.**

---

# Exercises

## Exercise 1 — Replace an Element

Create:

```python
fruits = ["Apple", "Banana", "Orange", "Mango"]
```

Replace `"Banana"` with `"Strawberry"`.

Print the final List.

---

## Exercise 2 — Replace the Last Element

Create:

```python
colors = ["Red", "Blue", "Green", "Yellow"]
```

Replace the last element with `"Purple"`.

Use negative indexing.

---

## Exercise 3 — Update a Score

Create:

```python
scores = [18, 8, 15, 7, 20]
```

Increase the second score by `2`.

Try using:

```python
+=
```

---

## Exercise 4 — Dynamic Modification

Create a List of several cities.

Store an Index in a variable and replace the corresponding city with another city.

Example:

```python
cities = ["Tehran", "Shiraz", "Tabriz", "Mashhad"]

index = 2
cities[index] = "Isfahan"

print(cities)
```

---

## Exercise 5 — Minimum Passing Score

Create:

```python
scores = [18, 8, 15, 7, 20, 9, 17]
```

Use a loop and indexing to replace every score below `10` with `10`.

The final List should contain no score below `10`.

---

## Exercise 6 — Increase Every Score

Create:

```python
scores = [10, 12, 15, 18, 20]
```

Use a loop and indexing to increase every score by `1`.

Expected result:

```text
[11, 13, 16, 19, 21]
```

---

# Section Challenge — Student Score Correction System

Create a program that stores several student scores in a List.

The program should:

1. Display the original scores.
2. Go through every score using its Index.
3. Replace every score below `10` with `10`.
4. Increase every passing score by `1`.
5. Display the updated scores.
6. Display the number of scores.
7. Display the first score.
8. Display the last score.

Example structure:

```python
scores = [18, 8, 15, 7, 20, 9, 17]

print("----- Student Score Correction -----")
print()

print(f"Original scores: {scores}")
print()

for index in range(len(scores)):
    if scores[index] < 10:
        scores[index] = 10
    else:
        scores[index] += 1

print(f"Updated scores: {scores}")
print(f"Number of scores: {len(scores)}")
print(f"First score: {scores[0]}")
print(f"Last score: {scores[-1]}")
```

Before looking at the example, try to design the solution yourself.

This challenge combines concepts from previous lessons:

```text
Lists
Variables
Indexing
Negative Indexing
len()
Conditions
for loops
Assignment
Augmented Assignment
```

In the next section, we will learn **List Slicing** and how to select a range of elements instead of only one element.

---

# Part 4 — List Slicing

In this section, we learn how to select a range of elements from a Python List using **Slicing**.

## What We Will Learn

- What List Slicing is
- Basic Slicing Syntax
- Start and Stop
- Understanding the exclusive Stop index
- Slicing from the beginning
- Slicing to the end
- Slicing the entire List
- Using Negative Indexes
- Using a Step
- Reversing a List with Slicing
- Copying a List with Slicing
- Common Slicing Mistakes
- Practical Examples
- Exercises
- Section Challenge

---

## 1. What Is List Slicing?

Indexing allows us to access **one element**:

```python
fruits = ["Apple", "Banana", "Orange", "Mango", "Sushi"]

print(fruits[1])
```

Output:

```text
Banana
```

Slicing allows us to select **multiple consecutive elements**:

```python
fruits = ["Apple", "Banana", "Orange", "Mango", "Sushi"]

print(fruits[1:4])
```

Output:

```text
['Banana', 'Orange', 'Mango']
```

Instead of selecting one position, Slicing selects a range of positions.

---

## 2. Basic Slicing Syntax

The basic syntax is:

```python
list_name[start:stop]
```

For example:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[1:4])
```

Output:

```text
[20, 30, 40]
```

The Slice starts at Index `1` and stops **before** Index `4`.

Therefore:

```text
Index 1 → included
Index 2 → included
Index 3 → included
Index 4 → excluded
```

This is one of the most important rules of Python Slicing.

---

## 3. Start and Stop

Consider this List:

```python
numbers = [10, 20, 30, 40, 50]
```

Indexes:

```text
0 → 10
1 → 20
2 → 30
3 → 40
4 → 50
```

Now:

```python
print(numbers[1:4])
```

means:

```text
Start at Index 1
Take Index 1
Take Index 2
Take Index 3
Stop before Index 4
```

Result:

```text
[20, 30, 40]
```

---

## 4. The Stop Index Is Exclusive

The Stop index is **not included** in the result.

For example:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[0:3])
```

Output:

```text
[10, 20, 30]
```

Index `3` contains `40`, but `40` is not included.

So:

```python
numbers[0:3]
```

means:

```text
Index 0
Index 1
Index 2
```

but not:

```text
Index 3
```

A useful way to remember this is:

> **Start is included, Stop is excluded.**

---

## 5. Slicing from the Beginning

If we want to start from the beginning of a List, we can omit the Start index.

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[:3])
```

Output:

```text
[10, 20, 30]
```

This is equivalent to:

```python
numbers[0:3]
```

Python automatically assumes the beginning of the List when Start is omitted.

---

## 6. Slicing to the End

If we want everything from a specific position to the end, we can omit the Stop index.

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[2:])
```

Output:

```text
[30, 40, 50]
```

This means:

```text
Start at Index 2
Continue until the end
```

---

## 7. Slicing the Entire List

We can omit both Start and Stop:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[:])
```

Output:

```text
[10, 20, 30, 40, 50]
```

This selects the entire List.

One important use of this form is creating a shallow copy of a List.

```python
numbers = [10, 20, 30, 40, 50]

numbers_copy = numbers[:]

print(numbers_copy)
```

Output:

```text
[10, 20, 30, 40, 50]
```

The new List contains the same elements.

---

## 8. Slicing with Negative Indexes

Slicing can also use Negative Indexing.

Consider:

```python
numbers = [10, 20, 30, 40, 50]
```

Negative indexes:

```text
-5 → 10
-4 → 20
-3 → 30
-2 → 40
-1 → 50
```

Now:

```python
print(numbers[-3:])
```

Output:

```text
[30, 40, 50]
```

This means:

```text
Start at Index -3
Continue to the end
```

---

## 9. Selecting the Last Few Elements

Negative Slicing is especially useful for selecting the last few elements.

```python
students = ["Ahmad", "Sara", "Alex", "John", "Michael"]

print(students[-2:])
```

Output:

```text
['John', 'Michael']
```

This selects the last two elements.

---

## 10. Selecting Everything Except the Last Element

We can also use:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[:-1])
```

Output:

```text
[10, 20, 30, 40]
```

The Stop index `-1` refers to the last element, but because Stop is exclusive, that element is not included.

---

## 11. Using a Step

Slicing supports a third value called **Step**.

The complete syntax is:

```python
list_name[start:stop:step]
```

For example:

```python
numbers = [10, 20, 30, 40, 50, 60]

print(numbers[0:6:2])
```

Output:

```text
[10, 30, 50]
```

The Slice moves through the List two positions at a time.

The selected indexes are:

```text
0 → 10
2 → 30
4 → 50
```

---

## 12. Slicing with a Step of 3

```python
numbers = [10, 20, 30, 40, 50, 60, 70, 80]

print(numbers[0:8:3])
```

Output:

```text
[10, 40, 70]
```

The selected indexes are:

```text
0
3
6
```

---

## 13. Omitting Start with a Step

We can combine omitted Start with Step:

```python
numbers = [10, 20, 30, 40, 50, 60]

print(numbers[:6:2])
```

Output:

```text
[10, 30, 50]
```

This means:

```text
Start from the beginning
Stop before Index 6
Move by 2
```

---

## 14. Omitting Stop with a Step

We can also omit Stop:

```python
numbers = [10, 20, 30, 40, 50, 60]

print(numbers[1::2])
```

Output:

```text
[20, 40, 60]
```

This means:

```text
Start at Index 1
Continue to the end
Move by 2
```

---

## 15. Reversing a List

One of the most useful Slicing techniques is:

```python
list_name[::-1]
```

The negative Step tells Python to move backward.

Example:

```python
numbers = [10, 20, 30, 40, 50]

reversed_numbers = numbers[::-1]

print(reversed_numbers)
```

Output:

```text
[50, 40, 30, 20, 10]
```

The original List remains unchanged:

```python
print(numbers)
```

Output:

```text
[10, 20, 30, 40, 50]
```

---

## 16. Copying and Reversing at the Same Time

Because Slicing creates a new List, we can create a reversed copy:

```python
numbers = [10, 20, 30, 40, 50]

reversed_numbers = numbers[::-1]

print("Original:", numbers)
print("Reversed:", reversed_numbers)
```

Output:

```text
Original: [10, 20, 30, 40, 50]
Reversed: [50, 40, 30, 20, 10]
```

---

## 17. Slicing Strings and Lists

Slicing is not limited to Lists.

Strings also support Slicing:

```python
name = "Python"

print(name[0:3])
```

Output:

```text
Pyt
```

The same general concept applies:

```text
[start:stop:step]
```

We learned String Slicing earlier, and now we can apply the same idea to Lists.

This is an important example of Python's consistent syntax.

---

## 18. Slicing a List of Strings

We can select a range from a List containing Strings:

```python
languages = ["Python", "Java", "C++", "JavaScript", "Go"]

print(languages[1:4])
```

Output:

```text
['Java', 'C++', 'JavaScript']
```

---

## 19. Slicing a List of Scores

Suppose we have student scores:

```python
scores = [18, 8, 15, 7, 20, 17, 19]

print(scores[1:5])
```

Output:

```text
[8, 15, 7, 20]
```

We selected the scores from Index `1` through Index `4`.

---

## 20. Practical Example — Recent Scores

Suppose a system stores the scores of several recent exams:

```python
scores = [15, 17, 18, 14, 20, 19, 16]

recent_scores = scores[-3:]

print(f"Recent scores: {recent_scores}")
```

Output:

```text
Recent scores: [20, 19, 16]
```

Negative Slicing makes this operation simple and readable.

---

## 21. Practical Example — First Five Items

Suppose an online store contains products:

```python
products = [
    "Laptop",
    "Phone",
    "Tablet",
    "Keyboard",
    "Mouse",
    "Monitor",
    "Headphones"
]

first_five = products[:5]

print(first_five)
```

Output:

```text
['Laptop', 'Phone', 'Tablet', 'Keyboard', 'Mouse']
```

---

## 22. Practical Example — Every Second Item

We can select every second element:

```python
products = [
    "Laptop",
    "Phone",
    "Tablet",
    "Keyboard",
    "Mouse",
    "Monitor"
]

selected_products = products[::2]

print(selected_products)
```

Output:

```text
['Laptop', 'Tablet', 'Mouse']
```

---

## 23. Slicing Does Not Modify the Original List

Slicing normally creates a new List.

```python
numbers = [10, 20, 30, 40, 50]

part = numbers[1:4]

print("Original:", numbers)
print("Part:", part)
```

Output:

```text
Original: [10, 20, 30, 40, 50]
Part: [20, 30, 40]
```

The original List is unchanged.

This is different from directly modifying an element:

```python
numbers[1] = 100
```

which changes the original List.

---

## 24. Important Difference Between Indexing and Slicing

Indexing:

```python
numbers = [10, 20, 30]

print(numbers[1])
```

returns one element:

```text
20
```

Slicing:

```python
print(numbers[1:2])
```

returns a new List:

```text
[20]
```

This difference is important:

```text
numbers[1]   → one element
numbers[1:2] → a List containing one element
```

---

# Common Mistakes

## Mistake 1 — Expecting the Stop Index to Be Included

This:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[1:4])
```

does not include Index `4`.

Output:

```text
[20, 30, 40]
```

Remember:

```text
Start → included
Stop  → excluded
```

---

## Mistake 2 — Confusing Indexing with Slicing

This:

```python
numbers[2]
```

returns one element.

But:

```python
numbers[2:3]
```

returns a List.

---

## Mistake 3 — Using a Step of Zero

A Step of `0` is invalid:

```python
numbers = [10, 20, 30, 40]

print(numbers[::0])
```

Python raises:

```text
ValueError: slice step cannot be zero
```

The Step must not be zero.

---

## Mistake 4 — Forgetting That Negative Step Changes Direction

For example:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[::-1])
```

returns:

```text
[50, 40, 30, 20, 10]
```

A negative Step moves through the List from right to left.

---

# Key Takeaways

The basic Slicing syntax is:

```python
list_name[start:stop]
```

The complete syntax is:

```python
list_name[start:stop:step]
```

The most important rule:

```text
Start is included.
Stop is excluded.
```

Examples:

```python
numbers[:3]
numbers[2:]
numbers[:]
numbers[-3:]
numbers[::2]
numbers[::-1]
```

Slicing can be used to:

- Select a range of elements
- Select the first elements
- Select the last elements
- Select every Nth element
- Reverse a List
- Create a shallow copy

The central idea of this section is:

> **List Slicing allows us to select a range of elements using a compact and powerful syntax.**

---

# Exercises

## Exercise 1 — Basic Slice

Create:

```python
numbers = [10, 20, 30, 40, 50, 60]
```

Select:

```text
20, 30, 40
```

---

## Exercise 2 — First Elements

Create:

```python
fruits = ["Apple", "Banana", "Orange", "Mango", "Sushi"]
```

Select the first three elements.

---

## Exercise 3 — Last Elements

Create:

```python
students = ["Ahmad", "Sara", "Alex", "John", "Michael"]
```

Select the last two students using Negative Slicing.

---

## Exercise 4 — Every Second Element

Create:

```python
numbers = [10, 20, 30, 40, 50, 60, 70, 80]
```

Select every second element.

Expected result:

```text
[10, 30, 50, 70]
```

---

## Exercise 5 — Reverse the List

Create:

```python
numbers = [1, 2, 3, 4, 5]
```

Create a reversed copy using Slicing.

Expected result:

```text
[5, 4, 3, 2, 1]
```

---

## Exercise 6 — Copy a List

Create:

```python
languages = ["Python", "Java", "C++", "Go"]
```

Create a copy using:

```python
[:]
```

Then print both Lists.

---

# Section Challenge — List Data Analyzer

Create a program that works with a List of scores:

```python
scores = [18, 12, 15, 9, 20, 17, 14, 19, 11, 16]
```

The program should:

1. Display the complete List.
2. Display the first three scores.
3. Display the last three scores.
4. Display the middle portion of the List.
5. Display every second score.
6. Display the reversed List.
7. Create a copy of the List using Slicing.
8. Display both the original List and the copied List.

Try to solve the Challenge using Slicing as much as possible.

Example structure:

```python
scores = [18, 12, 15, 9, 20, 17, 14, 19, 11, 16]

first_three = scores[:3]
last_three = scores[-3:]
middle = scores[3:7]
every_second = scores[::2]
reversed_scores = scores[::-1]
scores_copy = scores[:]

print("----- Score Analyzer -----")
print()

print(f"All scores: {scores}")
print(f"First three: {first_three}")
print(f"Last three: {last_three}")
print(f"Middle: {middle}")
print(f"Every second score: {every_second}")
print(f"Reversed: {reversed_scores}")
print(f"Copy: {scores_copy}")
```

This Challenge combines several concepts:

```text
Lists
Indexing
Negative Indexing
Slicing
Variables
String Formatting
```

In the next section, we will move on to **List Methods** and work with methods such as `append()`, `insert()`, `remove()`, and `pop()`.

---

# Part 5 — List Methods

In this section, we learn how to work with Python Lists using their built-in methods.

List Methods allow us to add, remove, search, reorder, and manage elements without manually implementing these operations ourselves.

## What We Will Learn

- What List Methods are
- `append()`
- `insert()`
- `extend()`
- `remove()`
- `pop()`
- `clear()`
- `index()`
- `count()`
- `sort()`
- `reverse()`
- The difference between `sort()` and `sorted()`
- The difference between `reverse()` and `[::-1]`
- Return Values of List Methods
- Common List Method mistakes
- Practical examples
- Combined exercises
- Section Challenge

---

## 1. What Is a List Method?

A List Method is a built-in operation that belongs to a List object.

For example:

```python
numbers = [10, 20, 30]

numbers.append(40)

print(numbers)
```

Output:

```text
[10, 20, 30, 40]
```

The method:

```python
append()
```

changes the List by adding a new element.

List Methods are called using Dot Notation:

```python
list_name.method_name()
```

Some methods also accept arguments:

```python
list_name.method_name(argument)
```

For example:

```python
numbers.append(40)
```

Here:

- `numbers` is the List.
- `append` is the method.
- `40` is the argument.

---

# 2. `append()`

The `append()` method adds **one element to the end of a List**.

Example:

```python
numbers = [10, 20, 30]

numbers.append(40)

print(numbers)
```

Output:

```text
[10, 20, 30, 40]
```

The new element is always added to the end.

---

## 2.1 Appending a String

`append()` can add values of different data types:

```python
languages = ["Python", "Java", "C++"]

languages.append("Go")

print(languages)
```

Output:

```text
['Python', 'Java', 'C++', 'Go']
```

---

## 2.2 Appending Multiple Times

We can call `append()` multiple times:

```python
numbers = []

numbers.append(10)
numbers.append(20)
numbers.append(30)
numbers.append(40)

print(numbers)
```

Output:

```text
[10, 20, 30, 40]
```

This is useful when we gradually build a List.

---

## 2.3 `append()` Adds One Object

An important detail is that `append()` adds its argument as **one element**.

For example:

```python
numbers = [1, 2, 3]

numbers.append([4, 5])

print(numbers)
```

Output:

```text
[1, 2, 3, [4, 5]]
```

The List `[4, 5]` becomes one element inside `numbers`.

The resulting structure is:

```text
1
2
3
[4, 5]
```

This behavior is important when working with nested Lists.

---

# 3. `insert()`

The `insert()` method adds an element at a specific Index.

Syntax:

```python
list_name.insert(index, value)
```

Example:

```python
numbers = [10, 20, 40]

numbers.insert(2, 30)

print(numbers)
```

Output:

```text
[10, 20, 30, 40]
```

The value `30` was inserted at Index `2`.

---

## 3.1 Understanding the Index

Before insertion:

```text
Index 0 → 10
Index 1 → 20
Index 2 → 40
```

After:

```python
numbers.insert(2, 30)
```

we have:

```text
Index 0 → 10
Index 1 → 20
Index 2 → 30
Index 3 → 40
```

The existing elements are shifted to the right.

---

## 3.2 Insert at the Beginning

We can insert an element at Index `0`:

```python
names = ["Sara", "Alex", "John"]

names.insert(0, "Ahmad")

print(names)
```

Output:

```text
['Ahmad', 'Sara', 'Alex', 'John']
```

---

## 3.3 Insert at the End

Although `insert()` can be used to add an element near the end, `append()` is usually clearer when we simply want to add an element to the end.

```python
numbers = [10, 20, 30]

numbers.insert(len(numbers), 40)

print(numbers)
```

Output:

```text
[10, 20, 30, 40]
```

For this situation, the simpler approach is:

```python
numbers.append(40)
```

Use the method that best communicates your intention.

---

# 4. `extend()`

The `extend()` method adds multiple elements from another Iterable to the end of a List.

Example:

```python
numbers = [1, 2, 3]

numbers.extend([4, 5, 6])

print(numbers)
```

Output:

```text
[1, 2, 3, 4, 5, 6]
```

Unlike `append()`, `extend()` adds the elements individually.

---

## 4.1 `append()` vs `extend()`

This difference is extremely important.

Using `append()`:

```python
numbers = [1, 2, 3]

numbers.append([4, 5])

print(numbers)
```

Output:

```text
[1, 2, 3, [4, 5]]
```

Using `extend()`:

```python
numbers = [1, 2, 3]

numbers.extend([4, 5])

print(numbers)
```

Output:

```text
[1, 2, 3, 4, 5]
```

The difference can be summarized as:

```text
append()  → adds one object
extend()  → adds elements from an Iterable
```

---

## 4.2 Extending with Another List

```python
first_group = ["Ahmad", "Sara"]
second_group = ["Alex", "John"]

first_group.extend(second_group)

print(first_group)
```

Output:

```text
['Ahmad', 'Sara', 'Alex', 'John']
```

The elements from `second_group` are added to `first_group`.

---

## 4.3 Extending with a String

Because Strings are Iterables, `extend()` can add their characters individually:

```python
letters = ["A", "B"]

letters.extend("CD")

print(letters)
```

Output:

```text
['A', 'B', 'C', 'D']
```

This is a good example of why understanding Iterables becomes important later in Python.

---

# 5. `remove()`

The `remove()` method removes the **first occurrence** of a specific value.

Example:

```python
numbers = [10, 20, 30, 20, 40]

numbers.remove(20)

print(numbers)
```

Output:

```text
[10, 30, 20, 40]
```

Only the first `20` was removed.

---

## 5.1 `remove()` Uses a Value, Not an Index

This:

```python
numbers.remove(30)
```

means:

> Find the first element whose value is `30` and remove it.

It does not mean:

> Remove the element at Index `30`.

For removing an element by Index, we use `pop()`.

---

## 5.2 Removing a String

```python
fruits = ["Apple", "Banana", "Orange", "Mango"]

fruits.remove("Orange")

print(fruits)
```

Output:

```text
['Apple', 'Banana', 'Mango']
```

---

## 5.3 What Happens If the Value Does Not Exist?

If the value is not present, Python raises a `ValueError`.

```python
numbers = [10, 20, 30]

numbers.remove(50)
```

This produces an error similar to:

```text
ValueError: list.remove(x): x not in list
```

Therefore, if the existence of the value is uncertain, we can check first:

```python
numbers = [10, 20, 30]

if 50 in numbers:
    numbers.remove(50)

print(numbers)
```

Output:

```text
[10, 20, 30]
```

---

# 6. `pop()`

The `pop()` method removes an element by Index and **returns the removed element**.

Example:

```python
numbers = [10, 20, 30, 40]

removed_number = numbers.pop(2)

print("Removed:", removed_number)
print("Numbers:", numbers)
```

Output:

```text
Removed: 30
Numbers: [10, 20, 40]
```

This makes `pop()` different from `remove()`.

---

## 6.1 `pop()` Without an Index

If we do not provide an Index, `pop()` removes the last element:

```python
numbers = [10, 20, 30, 40]

removed_number = numbers.pop()

print("Removed:", removed_number)
print("Numbers:", numbers)
```

Output:

```text
Removed: 40
Numbers: [10, 20, 30]
```

This is a very common use of `pop()`.

---

## 6.2 `pop()` with a Specific Index

```python
numbers = [10, 20, 30, 40, 50]

removed_number = numbers.pop(1)

print("Removed:", removed_number)
print("Numbers:", numbers)
```

Output:

```text
Removed: 20
Numbers: [10, 30, 40, 50]
```

The element at Index `1` was removed.

---

## 6.3 Negative Index with `pop()`

`pop()` also supports Negative Indexing:

```python
numbers = [10, 20, 30, 40, 50]

removed_number = numbers.pop(-2)

print("Removed:", removed_number)
print("Numbers:", numbers)
```

Output:

```text
Removed: 40
Numbers: [10, 20, 30, 50]
```

---

# 7. `clear()`

The `clear()` method removes all elements from a List.

Example:

```python
numbers = [10, 20, 30, 40]

numbers.clear()

print(numbers)
```

Output:

```text
[]
```

The List still exists, but it is now empty.

---

## 7.1 `clear()` vs Creating a New List

These two operations are not always conceptually identical.

Using:

```python
numbers.clear()
```

we empty the existing List.

Using:

```python
numbers = []
```

we make the variable refer to a new empty List.

For beginners, the important distinction is:

```text
clear() → empties the existing List
[]      → creates a new empty List
```

---

# 8. `index()`

The `index()` method returns the Index of the **first occurrence** of a value.

Example:

```python
fruits = ["Apple", "Banana", "Orange", "Banana"]

position = fruits.index("Banana")

print(position)
```

Output:

```text
1
```

The first `"Banana"` is at Index `1`.

---

## 8.1 `index()` with Duplicate Values

If a value appears multiple times, `index()` returns the first matching Index:

```python
numbers = [10, 20, 30, 20, 40]

position = numbers.index(20)

print(position)
```

Output:

```text
1
```

It does not return Index `3`, because Index `1` is the first occurrence.

---

## 8.2 Searching from a Specific Position

`index()` can also accept optional Start and Stop positions:

```python
numbers = [10, 20, 30, 20, 40]

position = numbers.index(20, 2)

print(position)
```

Output:

```text
3
```

Python starts searching from Index `2`, so it finds the second `20`.

---

# 9. `count()`

The `count()` method returns how many times a value appears in a List.

Example:

```python
numbers = [10, 20, 20, 30, 20, 40]

number_of_twenty = numbers.count(20)

print(number_of_twenty)
```

Output:

```text
3
```

The value `20` appears three times.

---

## 9.1 Counting Strings

```python
fruits = ["Apple", "Banana", "Apple", "Orange", "Apple"]

apple_count = fruits.count("Apple")

print(apple_count)
```

Output:

```text
3
```

---

# 10. `sort()`

The `sort()` method sorts a List **in place**.

For numbers:

```python
numbers = [40, 10, 30, 20, 50]

numbers.sort()

print(numbers)
```

Output:

```text
[10, 20, 30, 40, 50]
```

The original List has been changed.

---

## 10.1 Sorting in Descending Order

We can use the `reverse` parameter:

```python
numbers = [40, 10, 30, 20, 50]

numbers.sort(reverse=True)

print(numbers)
```

Output:

```text
[50, 40, 30, 20, 10]
```

---

## 10.2 Sorting Strings

Strings can also be sorted:

```python
names = ["Sara", "Ahmad", "John", "Alex"]

names.sort()

print(names)
```

Output:

```text
['Ahmad', 'Alex', 'John', 'Sara']
```

The strings are sorted according to their ordering rules.

---

# 11. `reverse()`

The `reverse()` method reverses the order of the elements **in place**.

Example:

```python
numbers = [10, 20, 30, 40, 50]

numbers.reverse()

print(numbers)
```

Output:

```text
[50, 40, 30, 20, 10]
```

The original List is changed.

---

## 11.1 `reverse()` Does Not Sort

This is an important distinction.

`reverse()` only changes the direction of the existing order.

```python
numbers = [30, 10, 50, 20, 40]

numbers.reverse()

print(numbers)
```

Output:

```text
[40, 20, 50, 10, 30]
```

The values were not sorted.

They were simply reversed.

---

# 12. `sort()` vs `sorted()`

This is an important concept.

`sort()` is a List Method:

```python
numbers.sort()
```

It modifies the original List.

`sorted()` is a built-in Python function:

```python
sorted(numbers)
```

It returns a new sorted List.

Example:

```python
numbers = [40, 10, 30, 20, 50]

sorted_numbers = sorted(numbers)

print("Original:", numbers)
print("Sorted:", sorted_numbers)
```

Output:

```text
Original: [40, 10, 30, 20, 50]
Sorted: [10, 20, 30, 40, 50]
```

The original List remains unchanged.

Compare this with:

```python
numbers = [40, 10, 30, 20, 50]

numbers.sort()

print(numbers)
```

Output:

```text
[10, 20, 30, 40, 50]
```

The original List has changed.

---

# 13. `reverse()` vs `[::-1]`

These two approaches can both reverse a List, but they behave differently.

Using `reverse()`:

```python
numbers = [10, 20, 30, 40]

numbers.reverse()

print(numbers)
```

The original List is modified.

Using Slicing:

```python
numbers = [10, 20, 30, 40]

reversed_numbers = numbers[::-1]

print("Original:", numbers)
print("Reversed:", reversed_numbers)
```

Output:

```text
Original: [10, 20, 30, 40]
Reversed: [40, 30, 20, 10]
```

The original List remains unchanged.

Therefore:

```text
reverse() → modifies the original List
[::-1]    → creates a reversed List
```

---

# 14. Return Values of List Methods

One of the most common beginner mistakes is assuming that List Methods always return the modified List.

They do not.

For example:

```python
numbers = [10, 20, 30]

result = numbers.append(40)

print(result)
```

Output:

```text
None
```

The List itself was modified:

```python
print(numbers)
```

Output:

```text
[10, 20, 30, 40]
```

This means:

```text
append() → modifies the List
append() → returns None
```

---

## 14.1 Another Example with `sort()`

```python
numbers = [30, 10, 20]

result = numbers.sort()

print(result)
print(numbers)
```

Output:

```text
None
[10, 20, 30]
```

Again, `sort()` modifies the original List but returns `None`.

---

## 14.2 Methods That Return a Useful Value

Some List Methods do return information.

For example:

```python
numbers = [10, 20, 30]

removed = numbers.pop()

print(removed)
```

Output:

```text
30
```

And:

```python
numbers = [10, 20, 30]

position = numbers.index(20)

print(position)
```

Output:

```text
1
```

And:

```python
numbers = [10, 20, 20, 30]

total = numbers.count(20)

print(total)
```

Output:

```text
2
```

Understanding the Return Value of a Method is important when writing larger programs.

---

# 15. Quick Comparison of Common List Methods

| Method | Purpose | Modifies List? | Returns |
|---|---|---:|---|
| `append()` | Add one element to the end | Yes | `None` |
| `insert()` | Add one element at an Index | Yes | `None` |
| `extend()` | Add elements from an Iterable | Yes | `None` |
| `remove()` | Remove the first matching value | Yes | `None` |
| `pop()` | Remove and return an element | Yes | Removed element |
| `clear()` | Remove all elements | Yes | `None` |
| `index()` | Find the first matching Index | No | Index |
| `count()` | Count occurrences | No | Number |
| `sort()` | Sort the List in place | Yes | `None` |
| `reverse()` | Reverse the List in place | Yes | `None` |

This table is useful as a quick reference, but understanding the behavior of each method is more important than memorizing the table.

---

# 16. Practical Example — Managing a Shopping List

We can combine several List Methods in a practical program:

```python
shopping_list = ["Milk", "Bread", "Eggs"]

shopping_list.append("Cheese")
shopping_list.insert(1, "Butter")
shopping_list.remove("Bread")

print("Shopping List:")
print(shopping_list)
```

Output:

```text
Shopping List:
['Milk', 'Butter', 'Eggs', 'Cheese']
```

The program demonstrates:

```text
append()
insert()
remove()
```

---

# 17. Practical Example — Processing Student Scores

Suppose we receive additional scores:

```python
scores = [18, 12, 15, 9]

new_scores = [20, 17, 14]

scores.extend(new_scores)

scores.sort()

print(scores)
```

Output:

```text
[9, 12, 14, 15, 17, 18, 20]
```

Several List operations were combined:

```text
extend()
sort()
```

---

# 18. Practical Example — Removing and Saving an Item

Suppose we have a queue of tasks:

```python
tasks = [
    "Study Python",
    "Practice Lists",
    "Read a Book",
    "Exercise"
]

completed_task = tasks.pop(1)

print(f"Completed: {completed_task}")
print(f"Remaining tasks: {tasks}")
```

Output:

```text
Completed: Practice Lists
Remaining tasks: ['Study Python', 'Read a Book', 'Exercise']
```

Because `pop()` returns the removed element, we can save it and use it later.

---

# 19. Practical Example — Checking Duplicate Data

Suppose we want to know how many times a score appears:

```python
scores = [18, 15, 20, 15, 17, 15, 19]

count_of_fifteen = scores.count(15)

print(f"Score 15 appears {count_of_fifteen} times.")
```

Output:

```text
Score 15 appears 3 times.
```

---

# 20. Practical Example — Finding an Item

```python
languages = ["Python", "Java", "C++", "JavaScript"]

language = "C++"

if language in languages:
    position = languages.index(language)
    print(f"{language} found at Index {position}.")
else:
    print(f"{language} was not found.")
```

Output:

```text
C++ found at Index 2.
```

Using `in` before `index()` prevents an error when the value does not exist.

---

# Common Mistakes

## Mistake 1 — Assigning the Result of `append()`

Incorrect:

```python
numbers = [10, 20, 30]

numbers = numbers.append(40)

print(numbers)
```

Result:

```text
None
```

Why?

Because `append()` modifies the List and returns `None`.

Correct:

```python
numbers = [10, 20, 30]

numbers.append(40)

print(numbers)
```

---

## Mistake 2 — Using `append()` When You Need `extend()`

This:

```python
numbers = [1, 2, 3]

numbers.append([4, 5])

print(numbers)
```

produces:

```text
[1, 2, 3, [4, 5]]
```

If the goal is to add `4` and `5` as separate elements, use:

```python
numbers = [1, 2, 3]

numbers.extend([4, 5])

print(numbers)
```

Output:

```text
[1, 2, 3, 4, 5]
```

---

## Mistake 3 — Confusing `remove()` and `pop()`

`remove()` works with a value:

```python
numbers.remove(30)
```

`pop()` works with an Index:

```python
numbers.pop(2)
```

A useful rule:

```text
remove(value)
pop(index)
```

---

## Mistake 4 — Calling `remove()` on a Missing Value

This can raise an error:

```python
numbers = [10, 20, 30]

numbers.remove(50)
```

Safer approach:

```python
numbers = [10, 20, 30]

if 50 in numbers:
    numbers.remove(50)
```

---

## Mistake 5 — Assuming `reverse()` Sorts the List

This:

```python
numbers = [30, 10, 20]

numbers.reverse()

print(numbers)
```

produces:

```text
[20, 10, 30]
```

It does not produce:

```text
[10, 20, 30]
```

`reverse()` changes direction.

`sort()` changes ordering according to sorting rules.

---

## Mistake 6 — Forgetting That `sort()` Changes the Original List

```python
numbers = [30, 10, 20]

numbers.sort()

print(numbers)
```

The original List is now:

```text
[10, 20, 30]
```

If you need to preserve the original List, use:

```python
numbers = [30, 10, 20]

sorted_numbers = sorted(numbers)

print("Original:", numbers)
print("Sorted:", sorted_numbers)
```

---

# Key Takeaways

List Methods provide convenient ways to manage List data.

The most important methods from this section are:

```python
append()
insert()
extend()
remove()
pop()
clear()
index()
count()
sort()
reverse()
```

Remember these core differences:

```text
append(value)
→ Add one object to the end

insert(index, value)
→ Add one object at a specific position

extend(iterable)
→ Add elements from another Iterable

remove(value)
→ Remove the first matching value

pop(index)
→ Remove and return an element by Index

pop()
→ Remove and return the last element

clear()
→ Empty the List

index(value)
→ Find the first matching Index

count(value)
→ Count occurrences

sort()
→ Sort the original List

reverse()
→ Reverse the original List
```

Also remember:

```text
sort()     → modifies the List
sorted()   → returns a new sorted List

reverse()  → modifies the List
[::-1]     → creates a reversed List
```

And one of the most important concepts:

> **Many List Methods modify the original List and return `None`.**

Understanding this behavior prevents many beginner mistakes.

---

# Exercises

## Exercise 1 — Building a List

Start with an empty List:

```python
numbers = []
```

Use `append()` to add:

```text
10
20
30
40
50
```

Then print the List.

---

## Exercise 2 — Inserting a Value

Start with:

```python
numbers = [10, 20, 40, 50]
```

Use `insert()` to add `30` between `20` and `40`.

Expected result:

```text
[10, 20, 30, 40, 50]
```

---

## Exercise 3 — Append vs Extend

Create:

```python
numbers = [1, 2, 3]
```

First use `append()` with:

```python
[4, 5]
```

Then create another List and use `extend()` with:

```python
[4, 5]
```

Compare the results.

---

## Exercise 4 — Remove a Value

Create:

```python
fruits = ["Apple", "Banana", "Orange", "Mango", "Banana"]
```

Remove the first `"Banana"`.

What happens to the second `"Banana"`?

---

## Exercise 5 — Pop and Save

Create:

```python
tasks = ["Study", "Exercise", "Read", "Sleep"]
```

Use `pop()` to remove the last task.

Save the removed task in a variable and print it.

---

## Exercise 6 — Count Occurrences

Create:

```python
numbers = [10, 20, 10, 30, 10, 40, 20]
```

Use `count()` to find how many times `10` appears.

---

## Exercise 7 — Find an Index

Create:

```python
languages = ["Python", "Java", "C++", "Go"]
```

Use `index()` to find the position of `"C++"`.

---

## Exercise 8 — Sort a List

Create:

```python
scores = [15, 8, 19, 12, 20, 10]
```

Sort the List in ascending order.

Then sort another copy in descending order.

---

## Exercise 9 — Reverse Without Modifying

Create:

```python
numbers = [1, 2, 3, 4, 5]
```

Create a reversed copy without changing the original List.

---

# Section Challenge — Student Score Manager

Create a program that manages student scores.

Start with:

```python
scores = [18, 12, 15, 9, 20]
```

The program should:

1. Add a new score using `append()`.
2. Insert a score at a specific position using `insert()`.
3. Add several scores using `extend()`.
4. Remove one specific score using `remove()`.
5. Remove the last score using `pop()` and save it.
6. Count how many times a specific score appears.
7. Find the Index of a specific score.
8. Create a sorted copy using `sorted()`.
9. Sort the original List in place using `sort()`.
10. Create a reversed copy using Slicing.
11. Display the original and modified data clearly.

Example structure:

```python
scores = [18, 12, 15, 9, 20]

scores.append(17)
scores.insert(2, 14)
scores.extend([16, 19])

if 9 in scores:
    scores.remove(9)

removed_score = scores.pop()

score_count = scores.count(15)

if 20 in scores:
    score_position = scores.index(20)
else:
    score_position = None

sorted_scores = sorted(scores)

scores.sort()

reversed_scores = scores[::-1]

print("----- Student Score Manager -----")
print()

print(f"Current scores: {scores}")
print(f"Removed score: {removed_score}")
print(f"Score 15 count: {score_count}")
print(f"Score 20 position: {score_position}")
print(f"Sorted copy: {sorted_scores}")
print(f"Reversed copy: {reversed_scores}")
```

This Challenge combines several concepts from the Lists lessons:

```text
Lists
Indexing
Negative Indexing
Slicing
List Methods
Variables
Conditional Statements
Membership Testing
String Formatting
```

In the next section, we will explore more advanced List operations and learn how Lists can be used with other Python concepts to process and transform data.

---

# Part 6 — Nested Lists

A nested list is a list that contains one or more other lists as its elements.

Nested lists are useful when data naturally has multiple levels.

For example, a list of students can contain a list of scores for each student:

```python
student_scores = [
    ["Ali", 18, 15, 20],
    ["Sara", 17, 19, 16],
    ["Reza", 12, 14, 10]
]

print(student_scores)
```

Output:

```text
[['Ali', 18, 15, 20], ['Sara', 17, 19, 16], ['Reza', 12, 14, 10]]
```

In this example, the outer list contains three inner lists.

---

## 1. What Are Nested Lists?

A normal list can contain simple values:

```python
numbers = [10, 20, 30]
```

A nested list can contain other lists:

```python
numbers = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
```

We can think of this structure as rows and columns:

```text
Row 1 → [1, 2, 3]
Row 2 → [4, 5, 6]
Row 3 → [7, 8, 9]
```

Each inner list is an element of the outer list.

---

## 2. Creating Nested Lists

A nested list is created by placing lists inside another list.

```python
numbers = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

print(numbers)
```

Output:

```text
[[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

Another example:

```python
students = [
    ["Ali", 18],
    ["Sara", 17],
    ["Reza", 15]
]

print(students)
```

Output:

```text
[['Ali', 18], ['Sara', 17], ['Reza', 15]]
```

Here each inner list contains a student's name and score.

---

## 3. Accessing Elements in Nested Lists

The first index selects an element from the outer list.

```python
numbers = [
    [10, 20, 30],
    [40, 50, 60],
    [70, 80, 90]
]

print(numbers[0])
```

Output:

```text
[10, 20, 30]
```

`numbers[0]` gives us the first inner list.

Similarly:

```python
print(numbers[1])
```

Output:

```text
[40, 50, 60]
```

And:

```python
print(numbers[2])
```

Output:

```text
[70, 80, 90]
```

---

## 4. Using Multiple Indexes

To access an individual value inside a nested list, we use two indexes.

The first index selects the inner list.

The second index selects an element inside that inner list.

```python
numbers = [
    [10, 20, 30],
    [40, 50, 60],
    [70, 80, 90]
]

print(numbers[0][1])
```

Output:

```text
20
```

Let's understand the two steps:

```python
numbers[0]
```

gives:

```text
[10, 20, 30]
```

Then:

```python
numbers[0][1]
```

selects index `1` from that inner list:

```text
20
```

Another example:

```python
print(numbers[2][0])
```

Output:

```text
70
```

The first `2` selects:

```text
[70, 80, 90]
```

The second `0` selects:

```text
70
```

---

## 5. Accessing Nested Lists with Negative Indexes

Negative indexes work with nested lists just like normal lists.

```python
numbers = [
    [10, 20, 30],
    [40, 50, 60],
    [70, 80, 90]
]

print(numbers[-1])
```

Output:

```text
[70, 80, 90]
```

We can also use a negative index for the inner list:

```python
print(numbers[-1][-1])
```

Output:

```text
90
```

The first `-1` selects the last inner list.

The second `-1` selects the last element of that inner list.

---

## 6. Changing Elements in Nested Lists

Nested lists are mutable, so their elements can be changed.

```python
numbers = [
    [10, 20, 30],
    [40, 50, 60],
    [70, 80, 90]
]

numbers[0][1] = 25

print(numbers)
```

Output:

```text
[[10, 25, 30], [40, 50, 60], [70, 80, 90]]
```

The value `20` was changed to `25`.

Another example:

```python
students = [
    ["Ali", 18],
    ["Sara", 17],
    ["Reza", 15]
]

students[1][1] = 19

print(students)
```

Output:

```text
[['Ali', 18], ['Sara', 19], ['Reza', 15]]
```

The score of `"Sara"` was changed from `17` to `19`.

---

## 7. Changing an Entire Inner List

We can also replace an entire inner list.

```python
numbers = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

numbers[1] = [40, 50, 60]

print(numbers)
```

Output:

```text
[[1, 2, 3], [40, 50, 60], [7, 8, 9]]
```

The entire second inner list was replaced.

---

## 8. Nested Lists with Loops

We can use loops to process the elements of a nested list.

First, we can use one loop to access each inner list:

```python
numbers = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for row in numbers:
    print(row)
```

Output:

```text
[1, 2, 3]
[4, 5, 6]
[7, 8, 9]
```

The variable `row` represents one inner list at a time.

---

## 9. Nested Loops

If we want to access every individual element, we can use a loop inside another loop.

```python
numbers = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for row in numbers:
    for number in row:
        print(number)
```

Output:

```text
1
2
3
4
5
6
7
8
9
```

The outer loop processes each inner list.

The inner loop processes each element inside that inner list.

This is called a **nested loop**.

---

## 10. Printing a Nested List as Rows

Nested lists are often easier to understand when printed row by row.

```python
numbers = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for row in numbers:
    print(row)
```

Output:

```text
[1, 2, 3]
[4, 5, 6]
[7, 8, 9]
```

We can also print the individual values:

```python
for row in numbers:
    for number in row:
        print(number, end=" ")

    print()
```

Output:

```text
1 2 3
4 5 6
7 8 9
```

The `print()` after the inner loop moves to the next line.

---

## 11. A Practical Example — Student Scores

Suppose we have several students and their scores:

```python
students = [
    ["Ali", 18, 15, 20],
    ["Sara", 17, 19, 16],
    ["Reza", 12, 14, 10]
]

for student in students:
    print(student)
```

Output:

```text
['Ali', 18, 15, 20]
['Sara', 17, 19, 16]
['Reza', 12, 14, 10]
```

We can access each student's information separately:

```python
students = [
    ["Ali", 18, 15, 20],
    ["Sara", 17, 19, 16],
    ["Reza", 12, 14, 10]
]

for student in students:
    name = student[0]

    print(f"Student: {name}")
```

Output:

```text
Student: Ali
Student: Sara
Student: Reza
```

---

## 12. Calculating Scores

We can combine nested lists with functions and loops learned earlier.

```python
students = [
    ["Ali", 18, 15, 20],
    ["Sara", 17, 19, 16],
    ["Reza", 12, 14, 10]
]

for student in students:
    name = student[0]
    scores = student[1:]

    total = sum(scores)
    average = total / len(scores)

    print(f"{name}: {average}")
```

Output:

```text
Ali: 17.666666666666668
Sara: 17.333333333333332
Reza: 12.0
```

We are combining several concepts we have already learned:

- Lists
- Indexing
- Slicing
- Variables
- Loops
- Functions
- Arithmetic
- Formatted strings

---

## 13. Nested Lists and Conditions

We can also use conditions while processing nested lists.

```python
students = [
    ["Ali", 18],
    ["Sara", 9],
    ["Reza", 15]
]

for student in students:
    name = student[0]
    score = student[1]

    if score >= 10:
        print(f"{name} → Passing")
    else:
        print(f"{name} → Failing")
```

Output:

```text
Ali → Passing
Sara → Failing
Reza → Passing
```

This is a good example of combining lists with conditions and loops.

---

## 14. Common Beginner Mistakes

### Mistake 1 — Forgetting the second index

Suppose we have:

```python
numbers = [
    [10, 20],
    [30, 40]
]
```

This:

```python
print(numbers[0])
```

prints:

```text
[10, 20]
```

If we want `20`, we need:

```python
print(numbers[0][1])
```

---

### Mistake 2 — Mixing Up the Indexes

For:

```python
numbers = [
    [10, 20],
    [30, 40]
]
```

This:

```python
numbers[1][0]
```

means:

1. Select the second inner list.
2. Select the first element.

The result is:

```text
30
```

---

### Mistake 3 — Using the Wrong Level of Loop

If we only need each inner list:

```python
for row in numbers:
    print(row)
```

If we need every individual number:

```python
for row in numbers:
    for number in row:
        print(number)
```

The second loop is necessary because each `row` is itself a list.

---

### Mistake 4 — Assuming Every Inner List Has the Same Size

For example:

```python
students = [
    ["Ali", 18, 15],
    ["Sara", 17],
    ["Reza", 12, 14, 10]
]
```

The inner lists do not have the same number of elements.

We should be careful when accessing indexes that may not exist.

---

# 15. Important Summary

A nested list is a list that contains other lists.

Example:

```python
numbers = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
```

The first index selects an inner list:

```python
numbers[1]
```

Result:

```text
[4, 5, 6]
```

The second index selects an element from that inner list:

```python
numbers[1][2]
```

Result:

```text
6
```

We can change individual elements:

```python
numbers[0][1] = 20
```

And we can use nested loops to process all elements:

```python
for row in numbers:
    for number in row:
        print(number)
```

The most important idea in this section is:

```text
First index  → choose the inner list
Second index → choose an element inside that list
```

---

# Exercises

## Exercise 1 — Create a Nested List

Create a nested list containing three rows of numbers.

Each row should contain three numbers.

Print the nested list.

---

## Exercise 2 — Access Elements

Using this list:

```python
numbers = [
    [10, 20, 30],
    [40, 50, 60],
    [70, 80, 90]
]
```

Print:

1. `10`
2. `50`
3. `90`

---

## Exercise 3 — Change Elements

Using the same list, change:

- `20` to `25`
- `60` to `65`
- `80` to `85`

Print the final list.

---

## Exercise 4 — Print Rows

Create a nested list containing three rows.

Use a loop to print each row separately.

---

## Exercise 5 — Print Every Element

Create a nested list containing numbers from `1` to `9`.

Use nested loops to print every number separately.

---

## Exercise 6 — Student Scores

Create a nested list like this:

```python
students = [
    ["Ali", 18],
    ["Sara", 12],
    ["Reza", 9]
]
```

Use a loop to print each student's name and score.

---

## Exercise 7 — Passing and Failing

Using the same student list, use a condition to print:

```text
Ali → Passing
Sara → Passing
Reza → Failing
```

A score of `10` or higher should be considered passing.

---

## Exercise 8 — Student Averages

Create a nested list containing student names and three scores for each student.

Calculate and print the average score of every student.

---

# Comprehensive Challenge

Create a simple **Student Score Manager** using a nested list.

Start with:

```python
students = [
    ["Ali", 18, 15, 20],
    ["Sara", 17, 9, 16],
    ["Reza", 12, 14, 10],
    ["Mina", 20, 19, 18]
]
```

Your program should:

1. Print every student's name.
2. Print every student's scores.
3. Calculate the total score for each student.
4. Calculate the average score for each student.
5. Determine whether each student is passing or failing.
6. Print the results in a readable format.
7. Use concepts learned in previous sections such as variables, lists, indexing, slicing, loops, conditions, functions, and formatted strings.

The goal is to understand how a nested list can represent a simple structured collection of data without introducing more advanced data structures.

---

# Final Challenge

Create a small **Classroom Table** using a nested list.

Use this starting data:

```python
classroom = [
    ["Ali", 18],
    ["Sara", 15],
    ["Reza", 9],
    ["Mina", 20]
]
```

Your program should:

1. Print all students.
2. Print each student's score.
3. Determine whether each student passed or failed.
4. Calculate the total of all scores.
5. Calculate the average score of the class.
6. Use loops and conditions to produce a clean report.

Example output:

```text
----- Classroom Report -----

Ali → 18 → Passing
Sara → 15 → Passing
Reza → 9 → Failing
Mina → 20 → Passing

Total: 62
Average: 15.5
```

The main goal is to practice **nested lists together with the beginner concepts learned in previous lessons**.

---

# Part 7 — Copying Lists

## 1. Why Do We Need to Copy a List?

Sometimes we want to create another list based on an existing list.

For example:

```python
numbers = [10, 20, 30]

numbers_copy = numbers.copy()

print(numbers)
print(numbers_copy)
```

Output:

```text
[10, 20, 30]
[10, 20, 30]
```

At first glance, both lists look exactly the same.

However, an important question is:

> Are they actually two separate lists?

To answer this, we need to understand the difference between **assigning a list** and **copying a list**.

---

## 2. Assigning One List to Another Variable

Consider this example:

```python
numbers = [10, 20, 30]

numbers_copy = numbers

print(numbers_copy)
```

Output:

```text
[10, 20, 30]
```

It may look like we created a new list.

But we did not create a new list.

Both variables refer to the same list.

We can see this by changing the second variable:

```python
numbers = [10, 20, 30]

numbers_copy = numbers

numbers_copy[0] = 100

print(numbers)
print(numbers_copy)
```

Output:

```text
[100, 20, 30]
[100, 20, 30]
```

Changing `numbers_copy` also changed `numbers`.

This happens because both variables refer to the same list.

---

## 3. The Difference Between Assignment and Copying

Assignment:

```python
numbers = [10, 20, 30]

numbers_copy = numbers
```

does not create a new list.

Instead, both variables refer to the same list.

Copying:

```python
numbers = [10, 20, 30]

numbers_copy = numbers.copy()
```

creates a separate list.

Now changing one list does not change the other.

```python
numbers = [10, 20, 30]

numbers_copy = numbers.copy()

numbers_copy[0] = 100

print(numbers)
print(numbers_copy)
```

Output:

```text
[10, 20, 30]
[100, 20, 30]
```

The original list remains unchanged.

---

## 4. Copying a List with `copy()`

The `copy()` method is one of the simplest ways to create a copy of a list.

```python
numbers = [10, 20, 30, 40]

numbers_copy = numbers.copy()

print(numbers_copy)
```

Output:

```text
[10, 20, 30, 40]
```

The two lists contain the same values, but they are separate lists.

For beginner-level Python, this is usually the clearest way to communicate that we intentionally want a copy.

---

## 5. Copying a List with Slicing

We can also create a copy using list slicing.

```python
numbers = [10, 20, 30, 40]

numbers_copy = numbers[:]

print(numbers_copy)
```

Output:

```text
[10, 20, 30, 40]
```

The `[:]` slice selects all elements of the list and creates a new list.

For example:

```python
numbers = [10, 20, 30]

numbers_copy = numbers[:]

numbers_copy[1] = 200

print(numbers)
print(numbers_copy)
```

Output:

```text
[10, 20, 30]
[10, 200, 30]
```

The original list is not changed.

---

## 6. Copying a List with `list()`

Another simple way to create a copy is to use the `list()` function.

```python
numbers = [10, 20, 30]

numbers_copy = list(numbers)

print(numbers_copy)
```

Output:

```text
[10, 20, 30]
```

We can also verify that changing the copy does not change the original:

```python
numbers = [10, 20, 30]

numbers_copy = list(numbers)

numbers_copy.append(40)

print(numbers)
print(numbers_copy)
```

Output:

```text
[10, 20, 30]
[10, 20, 30, 40]
```

---

## 7. Comparing the Three Simple Copying Methods

There are several beginner-friendly ways to copy a list.

### Using `copy()`

```python
numbers_copy = numbers.copy()
```

### Using slicing

```python
numbers_copy = numbers[:]
```

### Using `list()`

```python
numbers_copy = list(numbers)
```

All three create a separate list for a normal list of simple values.

For readability, `copy()` is often the easiest choice when the intention is clearly to copy a list:

```python
numbers_copy = numbers.copy()
```

---

## 8. Changing the Original and Copied List

Once we have a real copy, we can change either list independently.

```python
numbers = [10, 20, 30]

numbers_copy = numbers.copy()

numbers[0] = 100

print(numbers)
print(numbers_copy)
```

Output:

```text
[100, 20, 30]
[10, 20, 30]
```

Changing the original did not change the copy.

We can also change the copy:

```python
numbers = [10, 20, 30]

numbers_copy = numbers.copy()

numbers_copy[2] = 300

print(numbers)
print(numbers_copy)
```

Output:

```text
[10, 20, 30]
[10, 20, 300]
```

The two lists are independent.

---

## 9. A Practical Example

Suppose we have a list of student scores.

```python
scores = [18, 15, 20, 12, 17]

original_scores = scores.copy()

scores[0] = 10

print(f"Original scores: {original_scores}")
print(f"Updated scores: {scores}")
```

Output:

```text
Original scores: [18, 15, 20, 12, 17]
Updated scores: [10, 15, 20, 12, 17]
```

The copied list preserves the original values.

This can be useful when we want to keep the original data while working with a modified version.

---

## 10. Copying Before Making Changes

A common practical pattern is:

```python
scores = [18, 15, 20, 12, 17]

updated_scores = scores.copy()

updated_scores.append(19)

print(f"Original: {scores}")
print(f"Updated: {updated_scores}")
```

Output:

```text
Original: [18, 15, 20, 12, 17]
Updated: [18, 15, 20, 12, 17, 19]
```

This allows us to keep the original list unchanged.

---

## 11. Common Beginner Mistakes

### Mistake 1 — Thinking Assignment Creates a Copy

This does not create a separate list:

```python
numbers = [1, 2, 3]

numbers_copy = numbers
```

If we change one:

```python
numbers_copy[0] = 100
```

the other one changes too.

---

### Mistake 2 — Forgetting to Copy Before Modification

Suppose we want to preserve the original list.

This is not enough:

```python
numbers = [1, 2, 3]

new_numbers = numbers

new_numbers.append(4)
```

Now both variables refer to:

```text
[1, 2, 3, 4]
```

Instead, create a copy:

```python
numbers = [1, 2, 3]

new_numbers = numbers.copy()

new_numbers.append(4)
```

Now:

```text
numbers     → [1, 2, 3]
new_numbers → [1, 2, 3, 4]
```

---

### Mistake 3 — Confusing Equal Values with the Same List

Two lists can contain the same values while still being separate lists.

```python
numbers = [1, 2, 3]

numbers_copy = numbers.copy()
```

Both contain:

```text
[1, 2, 3]
```

But changing one does not change the other.

---

# 12. Important Summary

When we write:

```python
numbers_copy = numbers
```

we do not create a new list.

Both variables refer to the same list.

When we write:

```python
numbers_copy = numbers.copy()
```

we create a separate list.

Other beginner-friendly ways to copy a list include:

```python
numbers_copy = numbers[:]
```

and:

```python
numbers_copy = list(numbers)
```

The most important distinction is:

```text
Assignment → same list
Copying    → separate list
```

---

# Exercises

## Exercise 1 — Assignment or Copy?

Predict the output before running this code:

```python
numbers = [10, 20, 30]

numbers_copy = numbers

numbers_copy[0] = 100

print(numbers)
print(numbers_copy)
```

Explain why both outputs are the same.

---

## Exercise 2 — Using `copy()`

Create a list of five numbers.

Create a copy using `copy()`.

Change one element in the copied list.

Print both lists and verify that the original list has not changed.

---

## Exercise 3 — Using Slicing

Create a list of names.

Create a copy using:

```python
names_copy = names[:]
```

Add a new name to the copied list.

Print both lists.

---

## Exercise 4 — Using `list()`

Create a list of numbers.

Create a copy using:

```python
numbers_copy = list(numbers)
```

Remove one element from the copied list.

Print both lists.

---

## Exercise 5 — Original and Updated Scores

Create a list of student scores.

Make a copy called `updated_scores`.

Change some scores in `updated_scores`.

Print:

```text
Original scores:
Updated scores:
```

Verify that the original list remains unchanged.

---

## Exercise 6 — Three Lists

Create an original list:

```python
numbers = [1, 2, 3, 4, 5]
```

Create three separate copies using:

1. `copy()`
2. slicing
3. `list()`

Change an element in each copy.

Print all four lists.

---

# Comprehensive Challenge

Create a simple **Score Update System**.

Start with:

```python
scores = [18, 15, 20, 12, 17]
```

Your program should:

1. Preserve the original scores.
2. Create a separate copy called `updated_scores`.
3. Change at least two scores in `updated_scores`.
4. Add a new score.
5. Print the original scores.
6. Print the updated scores.
7. Make sure changing `updated_scores` does not change `scores`.

Example output:

```text
----- Score Update System -----

Original scores:
[18, 15, 20, 12, 17]

Updated scores:
[18, 19, 20, 14, 17, 16]
```

The main goal is to understand the difference between **referring to the same list** and **creating a separate copy of a list**.

---

# Part 8 — List Iteration

## 1. Introduction to List Iteration

One of the most common things we do with a list is to go through its elements one by one.

This process is called **iteration**.

For example:

    fruits = ["Apple", "Banana", "Orange"]

We can use a `for` loop to visit each element:

    fruits = ["Apple", "Banana", "Orange"]

    for fruit in fruits:
        print(fruit)

Output:

    Apple
    Banana
    Orange

The variable `fruit` represents the current element during each iteration.

---

## 2. Basic List Iteration

The simplest way to iterate over a list is with a `for` loop.

    numbers = [10, 20, 30, 40, 50]

    for number in numbers:
        print(number)

Output:

    10
    20
    30
    40
    50

Python automatically moves from one element to the next.

---

## 3. Iterating Over Strings in a List

A list can contain strings, and we can process each string individually.

    names = ["Ali", "Sara", "Reza", "Mina"]

    for name in names:
        print(f"Hello, {name}!")

Output:

    Hello, Ali!
    Hello, Sara!
    Hello, Reza!
    Hello, Mina!

This is useful when we want to perform the same operation on every item.

---

## 4. Performing Calculations During Iteration

We can perform calculations for every element.

    numbers = [2, 4, 6, 8]

    for number in numbers:
        square = number ** 2
        print(f"{number} squared = {square}")

Output:

    2 squared = 4
    4 squared = 16
    6 squared = 36
    8 squared = 64

Each element is processed separately.

---

## 5. Using Conditions While Iterating

We can combine a `for` loop with an `if` statement.

    scores = [18, 8, 15, 7, 20]

    for score in scores:
        if score >= 10:
            print(f"{score} → Passing")
        else:
            print(f"{score} → Failing")

Output:

    18 → Passing
    8 → Failing
    15 → Passing
    7 → Failing
    20 → Passing

This is one of the most useful patterns when working with lists.

---

## 6. Finding Specific Elements

We can use iteration to find elements that satisfy a condition.

    numbers = [5, 12, 8, 20, 3, 15]

    for number in numbers:
        if number > 10:
            print(number)

Output:

    12
    20
    15

Only numbers greater than `10` are printed.

---

## 7. Counting Elements During Iteration

We can create a counter and increase it while iterating.

    numbers = [5, 12, 8, 20, 3, 15]

    count = 0

    for number in numbers:
        if number > 10:
            count += 1

    print(f"Numbers greater than 10: {count}")

Output:

    Numbers greater than 10: 3

This pattern is useful when we want to count elements that meet a condition.

---

## 8. Calculating a Total During Iteration

We can use a variable to keep track of a running total.

    numbers = [10, 20, 30, 40]

    total = 0

    for number in numbers:
        total += number

    print(f"Total: {total}")

Output:

    Total: 100

The value of `total` changes during each iteration.

---

## 9. Finding the Largest Value

We can use a loop to find the largest value in a list.

    numbers = [12, 45, 7, 32, 18]

    largest = numbers[0]

    for number in numbers:
        if number > largest:
            largest = number

    print(f"Largest number: {largest}")

Output:

    Largest number: 45

The variable `largest` stores the largest value found so far.

---

## 10. Finding the Smallest Value

The same idea can be used to find the smallest value.

    numbers = [12, 45, 7, 32, 18]

    smallest = numbers[0]

    for number in numbers:
        if number < smallest:
            smallest = number

    print(f"Smallest number: {smallest}")

Output:

    Smallest number: 7

We start with the first element and compare every other element with it.

---

## 11. Creating a New List During Iteration

We can create a new list and add selected elements to it.

For example, we can create a list containing only passing scores.

    scores = [18, 8, 15, 7, 20]

    passing_scores = []

    for score in scores:
        if score >= 10:
            passing_scores.append(score)

    print(f"Passing scores: {passing_scores}")

Output:

    Passing scores: [18, 15, 20]

This is an important beginner pattern:

1. Create an empty list.
2. Iterate over the original list.
3. Check a condition.
4. Add matching elements to the new list.

---

## 12. Iterating Over a List and Creating Another List

We can use one list as the source and another list as the result.

    numbers = [1, 2, 3, 4, 5]

    doubled_numbers = []

    for number in numbers:
        doubled = number * 2
        doubled_numbers.append(doubled)

    print(f"Original: {numbers}")
    print(f"Doubled: {doubled_numbers}")

Output:

    Original: [1, 2, 3, 4, 5]
    Doubled: [2, 4, 6, 8, 10]

The original list remains unchanged.

---

## 13. Using `range()` with a List

Sometimes we want to work with the indexes of a list.

We can use `range()` together with `len()`.

    fruits = ["Apple", "Banana", "Orange"]

    for index in range(len(fruits)):
        print(f"Index: {index} → {fruits[index]}")

Output:

    Index: 0 → Apple
    Index: 1 → Banana
    Index: 2 → Orange

Here:

    len(fruits)

gives the number of elements in the list.

And:

    range(len(fruits))

creates the indexes we need.

For beginner-level list work, direct iteration is usually simpler when we do not need the index.

---

## 14. Direct Iteration vs Index-Based Iteration

### Direct iteration

Use this when you only need the values.

    fruits = ["Apple", "Banana", "Orange"]

    for fruit in fruits:
        print(fruit)

### Index-based iteration

Use this when you need the indexes.

    fruits = ["Apple", "Banana", "Orange"]

    for index in range(len(fruits)):
        print(f"{index}: {fruits[index]}")

The first approach is usually cleaner when the index is not needed.

---

## 15. Using `break` While Iterating

The `break` statement stops the loop completely.

For example, we can stop when we find a specific number.

    numbers = [10, 20, 30, 40, 50]

    for number in numbers:
        if number == 30:
            print("Number found!")
            break

        print(number)

Output:

    10
    20
    Number found!

When Python reaches `break`, the loop stops.

---

## 16. Using `continue` While Iterating

The `continue` statement skips the current iteration and moves to the next one.

For example, we can skip failing scores.

    scores = [18, 8, 15, 7, 20]

    for score in scores:
        if score < 10:
            continue

        print(f"Passing score: {score}")

Output:

    Passing score: 18
    Passing score: 15
    Passing score: 20

When `score < 10` is true, `continue` skips the remaining code for that iteration.

---

## 17. Practical Example — Student Scores

We can combine list iteration, conditions, counting, and calculations.

    scores = [18, 8, 15, 7, 20]

    print("----- Student Scores -----")
    print()

    print(f"Scores: {scores}")

    number_of_scores = len(scores)
    total = 0
    passing_count = 0

    for score in scores:
        total += score

        if score >= 10:
            passing_count += 1
            print(f"{score} → Passing")
        else:
            print(f"{score} → Failing")

    average = total / number_of_scores

    print()
    print(f"Number of scores: {number_of_scores}")
    print(f"Total: {total}")
    print(f"Average: {average}")
    print(f"Passing students: {passing_count}")

Output:

    ----- Student Scores -----

    Scores: [18, 8, 15, 7, 20]
    18 → Passing
    8 → Failing
    15 → Passing
    7 → Failing
    20 → Passing

    Number of scores: 5
    Total: 68
    Average: 13.6
    Passing students: 3

---

## 18. Practical Example — Finding a Product

We can search through a list of products.

    products = ["Laptop", "Mouse", "Keyboard", "Monitor"]

    search_item = "Keyboard"

    found = False

    for product in products:
        if product == search_item:
            found = True
            break

    if found:
        print(f"{search_item} was found.")
    else:
        print(f"{search_item} was not found.")

Output:

    Keyboard was found.

This example combines a list, a `for` loop, an `if` statement, a Boolean variable, and `break`.

---

## 19. Common Beginner Mistakes

### Mistake 1 — Forgetting indentation

Correct:

    numbers = [1, 2, 3]

    for number in numbers:
        print(number)

The `print()` statement belongs to the loop because it is indented.

### Mistake 2 — Changing the list while iterating over it

Avoid changing the same list while directly iterating over it.

For example:

    numbers = [1, 2, 3, 4, 5]

    for number in numbers:
        if number % 2 == 0:
            numbers.remove(number)

At the Beginner level, prefer creating a new list instead:

    numbers = [1, 2, 3, 4, 5]

    odd_numbers = []

    for number in numbers:
        if number % 2 != 0:
            odd_numbers.append(number)

    print(odd_numbers)

Output:

    [1, 3, 5]

### Mistake 3 — Using an unnecessary index

If we only need the values, this is simpler:

    fruits = ["Apple", "Banana", "Orange"]

    for fruit in fruits:
        print(fruit)

There is usually no need to write:

    for index in range(len(fruits)):
        print(fruits[index])

Use the index-based approach when you actually need the index.

---

## 20. Important Summary

List iteration means visiting the elements of a list one by one.

The most common pattern is:

    for item in my_list:
        print(item)

We can combine iteration with conditions:

    for item in my_list:
        if condition:
            print(item)

We can count matching elements:

    count = 0

    for item in my_list:
        if condition:
            count += 1

We can calculate a total:

    total = 0

    for number in numbers:
        total += number

We can create a new list:

    result = []

    for item in my_list:
        if condition:
            result.append(item)

We can stop a loop with:

    break

And skip one iteration with:

    continue

---

# Exercises

## Exercise 1 — Print All Elements

Create a list containing five favorite foods.

Use a `for` loop to print each food.

## Exercise 2 — Print Numbers

Create a list containing several numbers.

Use a loop to print each number.

## Exercise 3 — Print Even Numbers

Create a list of numbers.

Use iteration and an `if` statement to print only even numbers.

## Exercise 4 — Count Passing Scores

Create a list of student scores.

Use a loop to count how many scores are greater than or equal to `10`.

## Exercise 5 — Calculate the Total

Create a list of numbers.

Use iteration to calculate the total without using `sum()`.

## Exercise 6 — Find the Largest Number

Create a list of numbers.

Use a loop to find the largest number without using `max()`.

## Exercise 7 — Find the Smallest Number

Create a list of numbers.

Use a loop to find the smallest number without using `min()`.

## Exercise 8 — Create a New List

Create a list of numbers.

Create a second list containing only numbers greater than `10`.

## Exercise 9 — Double the Numbers

Create a list of numbers.

Create a new list where every number is multiplied by `2`.

## Exercise 10 — Search a List

Create a list of names.

Ask the user for a name.

Search through the list and print whether the name exists.

---

# Comprehensive Challenge

Create a **Student Score Analyzer**.

Start with:

    scores = [18, 8, 15, 7, 20, 12, 9]

Your program should:

1. Print all scores.
2. Count the number of scores.
3. Calculate the total without using `sum()`.
4. Calculate the average.
5. Count passing scores.
6. Count failing scores.
7. Find the highest score without using `max()`.
8. Find the lowest score without using `min()`.
9. Print whether each score is passing or failing.

Example output:

    ----- Student Score Analyzer -----

    Scores: [18, 8, 15, 7, 20, 12, 9]

    18 → Passing
    8 → Failing
    15 → Passing
    7 → Failing
    20 → Passing
    12 → Passing
    9 → Failing

    Number of scores: 7
    Total: 89
    Average: 12.71
    Passing scores: 4
    Failing scores: 3
    Highest score: 20
    Lowest score: 7

The goal is to practice list iteration together with the `for` loop, conditions, variables, counters, and basic calculations learned in previous sections.

---

# Part 9 — Checking Whether an Element Exists in a List

## 1. Introduction

Sometimes we need to check whether a specific value exists inside a list.

For example:

    fruits = ["Apple", "Banana", "Orange", "Mango"]

We may want to know whether `"Banana"` is in the list.

Python provides the `in` operator for this purpose.

    fruits = ["Apple", "Banana", "Orange", "Mango"]

    print("Banana" in fruits)

Output:

    True

The result is a Boolean value:

    True

or:

    False

---

## 2. Using `in`

The `in` operator checks whether a value exists in a list.

    numbers = [10, 20, 30, 40, 50]

    print(30 in numbers)
    print(100 in numbers)

Output:

    True
    False

The first check succeeds because `30` exists in the list.

The second check fails because `100` does not exist in the list.

---

## 3. Using `not in`

We can also check whether a value does not exist in a list.

For this, we use `not in`.

    fruits = ["Apple", "Banana", "Orange"]

    print("Apple" not in fruits)
    print("Mango" not in fruits)

Output:

    False
    True

`"Apple"` exists in the list, so `"Apple" not in fruits` is `False`.

`"Mango"` does not exist in the list, so `"Mango" not in fruits` is `True`.

---

## 4. Using `in` with `if`

The `in` operator is often used together with `if`.

    fruits = ["Apple", "Banana", "Orange"]

    if "Banana" in fruits:
        print("Banana is available.")

Output:

    Banana is available.

This allows our program to make a decision based on whether an element exists.

---

## 5. Using `else`

We can also handle the case where the element does not exist.

    fruits = ["Apple", "Banana", "Orange"]

    if "Mango" in fruits:
        print("Mango is available.")
    else:
        print("Mango is not available.")

Output:

    Mango is not available.

---

## 6. Checking User Input

We can use `in` to check a value entered by the user.

    fruits = ["Apple", "Banana", "Orange"]

    favorite = input("Enter a fruit: ")

    if favorite in fruits:
        print("This fruit is in the list.")
    else:
        print("This fruit is not in the list.")

If the user enters:

    Banana

The output will be:

    This fruit is in the list.

---

## 7. Checking Numbers

The same idea works with numbers.

    numbers = [10, 20, 30, 40, 50]

    number = int(input("Enter a number: "))

    if number in numbers:
        print("Number found.")
    else:
        print("Number not found.")

If the user enters:

    30

The output will be:

    Number found.

---

## 8. Checking Multiple Allowed Values

We can use `in` when several values are acceptable.

For example:

    allowed_colors = ["red", "green", "blue"]

    color = input("Enter a color: ")

    if color in allowed_colors:
        print("This color is allowed.")
    else:
        print("This color is not allowed.")

This is cleaner than writing several separate comparisons.

---

## 9. Checking Multiple Values with `not in`

We can also use `not in` when we want to reject certain values.

    blocked_users = ["admin", "root", "guest"]

    username = input("Enter a username: ")

    if username not in blocked_users:
        print("Username is available.")
    else:
        print("This username is blocked.")

---

## 10. Case Sensitivity

String comparisons are case-sensitive.

For example:

    fruits = ["Apple", "Banana", "Orange"]

    print("Apple" in fruits)
    print("apple" in fruits)

Output:

    True
    False

`"Apple"` and `"apple"` are different strings.

If we want to accept different letter cases, we can convert the input first.

    fruits = ["apple", "banana", "orange"]

    fruit = input("Enter a fruit: ").lower()

    if fruit in fruits:
        print("Fruit found.")
    else:
        print("Fruit not found.")

Now entering:

    APPLE

will also work because `.lower()` converts it to:

    apple

---

## 11. Checking Before Adding an Element

We can use `in` to prevent duplicate values.

    fruits = ["Apple", "Banana", "Orange"]

    new_fruit = "Banana"

    if new_fruit not in fruits:
        fruits.append(new_fruit)

    print(fruits)

Output:

    ['Apple', 'Banana', 'Orange']

Because `"Banana"` already exists, it is not added again.

If we use:

    new_fruit = "Mango"

The result becomes:

    ['Apple', 'Banana', 'Orange', 'Mango']

---

## 12. Checking Before Removing an Element

We can also check whether an element exists before using `remove()`.

    fruits = ["Apple", "Banana", "Orange"]

    fruit = "Banana"

    if fruit in fruits:
        fruits.remove(fruit)

    print(fruits)

Output:

    ['Apple', 'Orange']

This prevents an error that could happen if we tried to remove a value that does not exist.

---

## 13. Checking a List of Names

Here is a simple practical example.

    students = ["Ali", "Sara", "Reza", "Mina"]

    name = input("Enter a student name: ")

    if name in students:
        print(f"{name} is a student.")
    else:
        print(f"{name} is not in the student list.")

---

## 14. Combining `in` with Conditions

We can combine membership checking with other conditions.

    scores = [18, 15, 20, 12, 9]

    score = 20

    if score in scores and score >= 10:
        print("This is a passing score and it exists in the list.")

Output:

    This is a passing score and it exists in the list.

This allows us to check more than one condition at the same time.

---

## 15. `in` vs `index()`

The `in` operator answers a simple question:

    Does this value exist in the list?

For example:

    fruits = ["Apple", "Banana", "Orange"]

    print("Banana" in fruits)

Output:

    True

The `index()` method answers a different question:

    Where is this value located?

For example:

    fruits = ["Apple", "Banana", "Orange"]

    print(fruits.index("Banana"))

Output:

    1

At the Beginner level, use `in` when you only need to know whether an element exists.

Use `index()` when you actually need its position.

---

## 16. Practical Example — Shopping List

We can check whether an item is already in a shopping list.

    shopping_list = ["Milk", "Bread", "Eggs"]

    item = input("Enter an item: ")

    if item in shopping_list:
        print(f"{item} is already in the shopping list.")
    else:
        shopping_list.append(item)
        print(f"{item} was added to the shopping list.")

    print(f"Shopping list: {shopping_list}")

This simple pattern is useful for preventing duplicate items.

---

## 17. Practical Example — Allowed Subjects

We can use a list to store allowed subjects.

    subjects = ["Python", "Math", "English", "Science"]

    subject = input("Enter a subject: ")

    if subject in subjects:
        print("This subject is available.")
    else:
        print("This subject is not available.")

---

## 18. Practical Example — Simple Login Check

We can use a list to store allowed usernames.

    usernames = ["ali", "sara", "reza"]

    username = input("Enter your username: ")

    if username in usernames:
        print("Welcome!")
    else:
        print("Username not found.")

This is only a simple example of list membership. It is not a real authentication system.

---

## 19. Common Beginner Mistakes

### Mistake 1 — Forgetting that strings are case-sensitive

This:

    "Ali" in ["Ali", "Sara"]

is `True`.

But this:

    "ali" in ["Ali", "Sara"]

is `False`.

### Mistake 2 — Removing without checking

This can cause an error:

    fruits = ["Apple", "Banana"]

    fruits.remove("Mango")

A safer beginner approach is:

    fruits = ["Apple", "Banana"]

    if "Mango" in fruits:
        fruits.remove("Mango")

### Mistake 3 — Using `index()` when `in` is enough

If you only want to know whether an element exists, this is simpler:

    if "Banana" in fruits:
        print("Found.")

There is no need to find its index first.

---

## 20. Important Summary

The `in` operator checks whether an element exists in a list:

    "Apple" in fruits

The result is either:

    True

or:

    False

The `not in` operator checks whether an element does not exist:

    "Mango" not in fruits

We can use membership checking with `if`:

    if item in my_list:
        print("Found.")

We can prevent duplicates:

    if item not in my_list:
        my_list.append(item)

We can safely remove an element:

    if item in my_list:
        my_list.remove(item)

Remember that string comparisons are case-sensitive.

At the Beginner level, `in` and `not in` are simple and useful tools for working with lists.

---

# Part 10 — List Length and Counting Elements

## 1. Introduction

Sometimes we need to know how many elements a list contains.

For example:

```python
fruits = ["Apple", "Banana", "Orange"]

print(len(fruits))
```

Output:

```text
3
```

The `len()` function returns the number of elements in a list.

## 2. Using `len()`

The basic syntax is:

```python
len(list_name)
```

For example:

```python
numbers = [10, 20, 30, 40, 50]

print(len(numbers))
```

Output:

```text
5
```

## 3. Using `count()`

The `count()` method tells us how many times a specific value appears in a list.

```python
fruits = ["Apple", "Banana", "Apple", "Orange", "Apple"]

print(fruits.count("Apple"))
```

Output:

```text
3
```

## 4. `len()` vs `count()`

`len()` counts all elements:

```python
fruits = ["Apple", "Banana", "Apple", "Orange"]

print(len(fruits))
```

Output:

```text
4
```

`count()` counts a specific value:

```python
print(fruits.count("Apple"))
```

Output:

```text
2
```

So:

```python
len(fruits)
```

means:

How many elements are in the list?

While:

```python
fruits.count("Apple")
```

means:

How many times does `"Apple"` appear?

## 5. Important Summary

Use `len()` to find the number of elements:

```python
len(my_list)
```

Use `count()` to count a specific value:

```python
my_list.count(value)
```

An empty list has a length of:

```text
0
```

The last element can be accessed with:

```python
my_list[-1]
```

## Exercises

### Exercise 1

Create a list containing five favorite foods and print its length.

### Exercise 2

Create a list containing repeated numbers and use `count()` to count one of the numbers.

### Exercise 3

Create a list of student scores and count how many scores are greater than or equal to `10`.

### Exercise 4

Create an empty list and check whether it is empty.

---

