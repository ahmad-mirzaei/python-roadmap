# Part 1 — What Is a List?

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

