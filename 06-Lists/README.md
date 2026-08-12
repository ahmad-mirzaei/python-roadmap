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

