# Part 1 — Introduction to Tuples

> 🌐 Language: **English** | [فارسی](fa/README.md)

## Tuples Roadmap

| Part | Topic |
|---:|---|
| 1 | Introduction to Tuples |
| 2 | Creating Tuples |
| 3 | Accessing Tuple Elements |
| 4 | Tuple Slicing |
| 5 | Tuple Immutability |
| 6 | Checking for an Element in a Tuple |
| 7 | Tuple Length and Counting Elements |
| 8 | Finding the Position of an Element |
| 9 | Iterating Through Tuples |
| 10 | Combining and Repeating Tuples |
| 11 | Converting Between Lists and Tuples |
| 12 | Tuple Unpacking |
| 13 | Nested Tuples |
| 14 | Final Review: Tuples |
| 15 | Tuples Mini Project |

## 1. What Is a Tuple?

A **tuple** is a Python data type that can store multiple values together.

A tuple is similar to a list, but there is an important difference:

```text
List  → can be changed
Tuple → cannot be changed after creation
```

For example:

```python
fruits = ("Apple", "Banana", "Orange")

print(fruits)
```

Output:

```text
('Apple', 'Banana', 'Orange')
```

The values are stored together inside one tuple.

## 2. Creating a Tuple

We create a tuple by placing elements inside parentheses `()`.

```python
numbers = (10, 20, 30, 40)

print(numbers)
```

Output:

```text
(10, 20, 30, 40)
```

A tuple can contain different types of values:

```python
student = ("Ali", 20, 18.5)

print(student)
```

Output:

```text
('Ali', 20, 18.5)
```

## 3. Tuple vs List

A list uses square brackets:

```python
fruits = ["Apple", "Banana", "Orange"]
```

A tuple usually uses parentheses:

```python
fruits = ("Apple", "Banana", "Orange")
```

The important difference is that lists are mutable, while tuples are immutable.

For example, this works with a list:

```python
fruits = ["Apple", "Banana", "Orange"]

fruits[0] = "Mango"

print(fruits)
```

Output:

```text
['Mango', 'Banana', 'Orange']
```

But a tuple cannot be changed this way:

```python
fruits = ("Apple", "Banana", "Orange")

fruits[0] = "Mango"
```

Python will raise an error because tuple elements cannot be changed after the tuple is created.

## 4. When Can We Use a Tuple?

Tuples are useful when we have a group of values that should stay unchanged.

For example:

```python
location = (51.5074, -0.1278)

print(location)
```

Output:

```text
(51.5074, -0.1278)
```

The tuple can represent a fixed pair of values.

Another example:

```python
birthday = (15, 8, 2005)

print(birthday)
```

Output:

```text
(15, 8, 2005)
```

## 5. An Important Beginner Point

A tuple is not simply "a list with parentheses".

The main idea is that a tuple is **immutable**.

That means after creating it, we cannot directly change, add, or remove its elements.

We will study this concept more carefully in a later section.

For now, remember:

```text
List  → mutable
Tuple → immutable
```

# Questions

## Question 1

What is a tuple?

## Question 2

What is the main difference between a list and a tuple?

## Question 3

Is this code valid? Why or why not?

```python
numbers = (10, 20, 30)

numbers[0] = 100
```

## Review Question

What is the difference between a mutable data type and an immutable data type, based on what we have learned so far?

# Answers

## Answer 1

A tuple is a Python data type that can store multiple values together.

## Answer 2

A list can be changed after creation, while a tuple cannot be directly changed after creation.

## Answer 3

No. The code is not valid because tuple elements cannot be changed after the tuple is created.

## Review Answer

A mutable data type can be changed after creation, while an immutable data type cannot be directly changed after creation.

---

# Part 2 — Creating Tuples

## 1. Creating a Tuple

A tuple is usually created by placing multiple values inside parentheses `()` and separating them with commas.

```python
fruits = ("Apple", "Banana", "Orange")

print(fruits)
```

Output:

```text
('Apple', 'Banana', 'Orange')
```

The commas are important because they separate the elements of the tuple.

## 2. Creating a Tuple of Numbers

A tuple can contain numbers:

```python
numbers = (10, 20, 30, 40)

print(numbers)
```

Output:

```text
(10, 20, 30, 40)
```

## 3. Creating a Tuple with Different Data Types

A tuple can contain different types of values.

```python
student = ("Ali", 20, 18.5, True)

print(student)
```

Output:

```text
('Ali', 20, 18.5, True)
```

## 4. Creating an Empty Tuple

We can create an empty tuple using empty parentheses:

```python
empty_tuple = ()

print(empty_tuple)
```

Output:

```text
()
```

An empty tuple contains no elements.

## 5. Creating a Tuple with One Element

A very important point is that a single-element tuple needs a comma.

This is not a tuple:

```python
number = (10)

print(type(number))
```

Output:

```text
<class 'int'>
```

Python treats `(10)` as a normal integer expression.

To create a tuple with one element, we need a comma:

```python
number = (10,)

print(type(number))
```

Output:

```text
<class 'tuple'>
```

This comma is important.

## 6. Tuple Creation Without Parentheses

Python also allows us to create a tuple without explicitly writing parentheses.

```python
fruits = "Apple", "Banana", "Orange"

print(fruits)
```

Output:

```text
('Apple', 'Banana', 'Orange')
```

Python recognizes the comma-separated values as a tuple.

However, using parentheses is often clearer for beginners:

```python
fruits = ("Apple", "Banana", "Orange")
```

## 7. Creating a Tuple from a List

We can use `tuple()` to convert a list into a tuple.

```python
fruits = ["Apple", "Banana", "Orange"]

fruits_tuple = tuple(fruits)

print(fruits_tuple)
```

Output:

```text
('Apple', 'Banana', 'Orange')
```

We will study conversions between Lists and Tuples in more detail later.

## 8. Checking the Type

We can use `type()` to check whether a value is a tuple.

```python
colors = ("Red", "Green", "Blue")

print(type(colors))
```

Output:

```text
<class 'tuple'>
```

## 9. Important Rule

When creating a tuple, remember:

```text
Multiple elements → commas separate the elements
One element       → a comma is required
Empty tuple       → ()
```

For example:

```python
a = ()
b = (10,)
c = (10, 20, 30)
```

# Questions

## Question 1

How do we normally create a tuple?

## Question 2

What is the difference between these two?

```python
a = (10)
b = (10,)
```

## Question 3

What will this program print?

```python
numbers = 10, 20, 30

print(numbers)
print(type(numbers))
```

## Review Question

What is the main difference between a List and a Tuple, and how do we create a tuple with only one element?

# Answers

## Answer 1

A tuple is normally created by placing comma-separated values inside parentheses `()`.

## Answer 2

`(10)` is an integer expression, while `(10,)` is a tuple containing one element.

## Answer 3

It prints:

```text
(10, 20, 30)
<class 'tuple'>
```

## Review Answer

A List is mutable, while a Tuple is immutable. To create a tuple with one element, a comma is required, such as `(10,)`.

---

# Part 3 — Accessing Tuple Elements

## 1. Accessing Elements with Indexing

Just like Lists, we can access Tuple elements using their index.

Python starts counting indexes from `0`.

```python
fruits = ("Apple", "Banana", "Orange")

print(fruits[0])
print(fruits[1])
print(fruits[2])
```

Output:

```text
Apple
Banana
Orange
```

## 2. Using Negative Indexes

We can also use negative indexes.

`-1` refers to the last element, `-2` to the second-to-last element, and so on.

```python
fruits = ("Apple", "Banana", "Orange")

print(fruits[-1])
print(fruits[-2])
print(fruits[-3])
```

Output:

```text
Orange
Banana
Apple
```

## 3. Accessing a Specific Element

We can use an index to access any element we need.

```python
numbers = (10, 20, 30, 40, 50)

print(numbers[3])
```

Output:

```text
40
```

The index `3` refers to the fourth element because indexing starts from `0`.

## 4. Using Indexing with Different Data Types

Indexing works regardless of the type of values stored in the Tuple.

```python
student = ("Ali", 20, 18.5, True)

print(student[0])
print(student[1])
print(student[2])
print(student[3])
```

Output:

```text
Ali
20
18.5
True
```

## 5. Indexing a Nested Tuple

A Tuple can contain another Tuple.

We can use multiple indexes to access an element inside the nested Tuple.

```python
student = ("Ali", (18, 20, 17))

print(student[1])
print(student[1][0])
```

Output:

```text
(18, 20, 17)
18
```

Here:

```text
student[1]
```

accesses the inner Tuple.

Then:

```text
student[1][0]
```

accesses the first element of that inner Tuple.

We will study nested Tuples in more detail later.

## 6. Index Out of Range

The index must exist in the Tuple.

For example:

```python
fruits = ("Apple", "Banana", "Orange")

print(fruits[3])
```

This causes an error because the available indexes are:

```text
0
1
2
```

The index `3` does not exist.

## 7. Important Point

Tuple indexing works in the same basic way as List indexing.

For example:

```python
fruits = ("Apple", "Banana", "Orange")

print(fruits[0])
print(fruits[-1])
```

Output:

```text
Apple
Orange
```

The important difference is not how we access the elements.

The important difference is that Tuple elements cannot be changed after the Tuple is created.

# Questions

## Question 1

What is the index of `"Orange"`?

```python
fruits = ("Apple", "Banana", "Orange")
```

## Question 2

What will this program print?

```python
numbers = (10, 20, 30, 40)

print(numbers[-1])
print(numbers[-3])
```

## Question 3

Why does this code cause an error?

```python
colors = ("Red", "Green", "Blue")

print(colors[3])
```

## Review Question

What are the main differences between accessing elements in a List and a Tuple, and what happens if we try to change a Tuple element?

# Answers

## Answer 1

The index of `"Orange"` is `2`.

## Answer 2

Output:

```text
40
20
```

## Answer 3

The Tuple has only three elements, so its valid indexes are `0`, `1`, and `2`. Index `3` does not exist.

## Review Answer

The basic indexing method is the same for Lists and Tuples. Both support positive and negative indexes. However, Tuple elements cannot be changed after the Tuple is created.

---

# Part 4 — Tuple Slicing

## 1. What Is Tuple Slicing?

Just like Lists, we can use slicing to select a part of a Tuple.

The basic syntax is:

```python
tuple[start:stop]
```

The `start` index is included, but the `stop` index is not included.

For example:

```python
fruits = ("Apple", "Banana", "Orange", "Mango", "Grape")

print(fruits[1:4])
```

Output:

```text
('Banana', 'Orange', 'Mango')
```

Indexes `1`, `2`, and `3` are included, but index `4` is not.

## 2. Slicing from the Beginning

We can leave the `start` index empty.

```python
numbers = (10, 20, 30, 40, 50)

print(numbers[:3])
```

Output:

```text
(10, 20, 30)
```

This means:

```text
Start from the beginning
Stop before index 3
```

## 3. Slicing to the End

We can also leave the `stop` index empty.

```python
numbers = (10, 20, 30, 40, 50)

print(numbers[2:])
```

Output:

```text
(30, 40, 50)
```

This means:

```text
Start from index 2
Continue to the end
```

## 4. Copying a Tuple with Slicing

We can use slicing to create a Tuple containing all elements.

```python
fruits = ("Apple", "Banana", "Orange")

new_fruits = fruits[:]

print(new_fruits)
```

Output:

```text
('Apple', 'Banana', 'Orange')
```

## 5. Using a Step

We can provide a third value in the slice:

```python
tuple[start:stop:step]
```

For example:

```python
numbers = (10, 20, 30, 40, 50, 60)

print(numbers[0:6:2])
```

Output:

```text
(10, 30, 50)
```

The step `2` means that Python selects every second element.

## 6. Reversing a Tuple

A negative step allows us to move backward.

The simplest way to reverse a Tuple is:

```python
numbers = (10, 20, 30, 40, 50)

reversed_numbers = numbers[::-1]

print(reversed_numbers)
```

Output:

```text
(50, 40, 30, 20, 10)
```

Here:

```text
start → omitted
stop  → omitted
step  → -1
```

So Python moves through the Tuple from the end to the beginning.

## 7. Negative Indexes in Slicing

We can also use negative indexes when slicing.

```python
fruits = ("Apple", "Banana", "Orange", "Mango", "Grape")

print(fruits[-4:-1])
```

Output:

```text
('Banana', 'Orange', 'Mango')
```

The same slicing rules apply. The `stop` index is still excluded.

## 8. Important Rule

Remember:

```text
tuple[start:stop]
```

means:

```text
start → included
stop  → excluded
```

And:

```python
tuple[::-1]
```

is a common way to reverse a Tuple.

# Questions

## Question 1

What will this code print?

```python
numbers = (10, 20, 30, 40, 50)

print(numbers[1:4])
```

## Question 2

What is the difference between these two?

```python
numbers[:3]
numbers[3:]
```

## Question 3

What will this code print?

```python
numbers = (10, 20, 30, 40, 50)

print(numbers[::-1])
```

## Review Question

How can we access a specific element of a Tuple, select a range of elements, and reverse the entire Tuple?

# Answers

## Answer 1

```text
(20, 30, 40)
```

## Answer 2

`numbers[:3]` selects elements from the beginning up to, but not including, index `3`.

`numbers[3:]` selects elements starting at index `3` and continues to the end.

## Answer 3

```text
(50, 40, 30, 20, 10)
```

## Review Answer

We use indexing such as `tuple[2]` to access one element, slicing such as `tuple[1:4]` to select a range, and `tuple[::-1]` to reverse the Tuple.

---

# Part 5 — Tuple Immutability

## 1. The Core Idea of Tuples

One of the most important characteristics of a Tuple is **immutability**.

When we create a Tuple, its structure cannot be changed afterward.

For example:

```python
student = ("Ali", 20, 18.5)

print(student)
```

The Tuple has three elements. After it is created, we cannot directly replace one of those elements.

```python
student = ("Ali", 20, 18.5)

student[1] = 21
```

This produces an error because the Tuple is immutable.

The important idea is not that the values are somehow "permanently frozen" in every possible sense. Rather, the **Tuple itself does not provide operations for changing its existing elements**.

## 2. Comparing Tuple Immutability with List Mutability

To understand immutability properly, it helps to compare a Tuple with a List.

A List allows us to change an existing element:

```python
student = ["Ali", 20, 18.5]

student[1] = 21

print(student)
```

Output:

```text
['Ali', 21, 18.5]
```

The same operation does not work with a Tuple:

```python
student = ("Ali", 20, 18.5)

student[1] = 21
```

The difference is fundamental:

```text
List  → elements can be changed
Tuple → elements cannot be changed
```

This is one of the main reasons Python has both Lists and Tuples.

## 3. Why Does Immutability Matter?

Immutability can be useful when we want to represent data that should remain stable.

For example, suppose we have a fixed coordinate:

```python
point = (10, 20)
```

If this Tuple represents a specific point, allowing arbitrary changes to its elements may not be desirable.

Another example could be a date:

```python
birthday = (15, 8, 2005)
```

The three values belong together as one fixed group of information.

The Tuple communicates an important idea:

> These values belong together, and the structure itself should not be modified.

## 4. You Can Still Create a New Tuple

Immutability does not mean that we can never have a different Tuple.

It means that we cannot modify the existing Tuple in place.

We can create another Tuple instead:

```python
numbers = (10, 20, 30)

new_numbers = (100, 20, 30)

print(numbers)
print(new_numbers)
```

Output:

```text
(10, 20, 30)
(100, 20, 30)
```

The original Tuple remains unchanged.

This distinction is important:

```text
Changing an existing Tuple → not allowed
Creating another Tuple     → allowed
```

## 5. Operations That Do Not Change the Tuple

Many operations can read or use a Tuple without modifying it.

For example:

```python
numbers = (10, 20, 30, 40)

print(numbers[1])
print(len(numbers))
print(20 in numbers)
```

Output:

```text
20
4
True
```

None of these operations changes the Tuple.

This is an important distinction between **reading data** and **modifying data**.

## 6. Methods That Change a List Are Not Available for Tuples

Lists provide methods such as:

```python
append()
remove()
sort()
```

These methods can modify a List.

Tuples do not provide these modification methods.

For example:

```python
numbers = (10, 20, 30)

numbers.append(40)
```

This produces an error because a Tuple has no `append()` method.

Likewise:

```python
numbers = (10, 20, 30)

numbers.remove(20)
```

This also produces an error.

The absence of these methods is directly related to the immutable nature of Tuples.

## 7. Immutability and Slicing

Slicing does not modify the original Tuple.

Instead, it creates a new Tuple containing the selected elements.

```python
numbers = (10, 20, 30, 40, 50)

part = numbers[1:4]

print(numbers)
print(part)
```

Output:

```text
(10, 20, 30, 40, 50)
(20, 30, 40)
```

The original Tuple remains unchanged.

This is another example of the difference between **creating a new value** and **modifying an existing value**.

## 8. An Important Exception: Mutable Objects Inside a Tuple

There is a deeper point worth understanding.

A Tuple itself is immutable, but an element inside a Tuple can be a mutable object such as a List.

For example:

```python
data = ("Ali", [10, 20, 30])

data[1].append(40)

print(data)
```

Output:

```text
('Ali', [10, 20, 30, 40])
```

We did not replace the second element of the Tuple.

The second element is still the same List object.

We changed the **contents of that List**.

This leads to an important distinction:

```text
The Tuple structure is immutable.
An object stored inside the Tuple may still be mutable.
```

For beginner Python programming, this distinction is extremely useful because it prevents a common misunderstanding:

> "If a Tuple is immutable, absolutely nothing inside it can ever change."

That statement is not always correct.

## 9. The Mental Model

A useful way to think about Tuple immutability is:

```text
Tuple
 ├── element 1
 ├── element 2
 └── element 3
```

The Tuple does not allow us to replace, add, or remove its element references.

But if one of those elements refers to a mutable object:

```text
Tuple
 ├── "Ali"
 └── List → [10, 20, 30]
```

the List itself may still be changed.

Understanding this now will make more advanced Python concepts much easier later.

# Questions

## Question 1

Why does this code produce an error?

```python
numbers = (10, 20, 30)

numbers[0] = 100
```

## Question 2

What is the difference between modifying an existing Tuple and creating a new Tuple?

## Question 3

Will the following code change the Tuple itself?

```python
data = ("Ali", [10, 20])

data[1].append(30)

print(data)
```

Explain your answer.

## Review Question

Compare Lists and Tuples based on everything learned so far. Explain when you would choose a List and when you would choose a Tuple, and include the role of immutability in your explanation.

# Answers

## Answer 1

The code produces an error because Tuple elements cannot be replaced after the Tuple has been created.

## Answer 2

An existing Tuple cannot be modified in place, but we can create another Tuple with different values.

## Answer 3

The Tuple structure itself is not changed. The second element refers to a mutable List, and the contents of that List are changed.

The result is:

```text
('Ali', [10, 20, 30])
```

## Review Answer

A List is appropriate when the collection needs to be modified, while a Tuple is useful when the group of values should remain structurally unchanged. Immutability is the key characteristic that distinguishes the two.

---

# Part 6 — Checking for an Element in a Tuple

## 1. Checking Whether an Element Exists

After learning how to access Tuple elements, the next important step is learning how to determine whether a specific value exists in a Tuple.

Python provides the `in` operator for this purpose.

```python
fruits = ("Apple", "Banana", "Orange")

print("Banana" in fruits)
```

Output:

```text
True
```

Because `"Banana"` exists in the Tuple, the expression returns `True`.

If the value does not exist:

```python
fruits = ("Apple", "Banana", "Orange")

print("Mango" in fruits)
```

Output:

```text
False
```

The `in` operator does not return the element itself. It checks membership and returns a Boolean value:

```text
True  → the element exists
False → the element does not exist
```

## 2. Using `not in`

We can also check that an element does **not** exist in a Tuple by using `not in`.

```python
fruits = ("Apple", "Banana", "Orange")

print("Mango" not in fruits)
```

Output:

```text
True
```

This is `True` because `"Mango"` is not inside the Tuple.

If the element does exist:

```python
print("Apple" not in fruits)
```

Output:

```text
False
```

## 3. Membership Is Based on Value

When we use `in`, Python checks whether the specified value exists among the elements.

For example:

```python
numbers = (10, 20, 30, 40)

print(20 in numbers)
print(25 in numbers)
```

Output:

```text
True
False
```

The position of the element does not matter for this check.

We are asking:

> Is this value a member of the Tuple?

not:

> What is the position of this value?

If we need the position, we will use `index()` in a later section.

## 4. Using Membership Checks in Conditions

Membership checks become especially useful when combined with `if`.

```python
fruits = ("Apple", "Banana", "Orange")

if "Banana" in fruits:
    print("Banana is available.")
```

Output:

```text
Banana is available.
```

We can also handle the case where an element is missing:

```python
fruits = ("Apple", "Banana", "Orange")

if "Mango" not in fruits:
    print("Mango is not available.")
```

Output:

```text
Mango is not available.
```

This makes membership checks useful in real programs where the program needs to make a decision based on whether some data exists.

## 5. Membership Checks and Strings

The `in` operator is not limited to numbers.

It can be used with strings and other data types as long as Python can compare the values.

```python
names = ("Ali", "Sara", "Reza")

print("Sara" in names)
print("sara" in names)
```

Output:

```text
True
False
```

The comparison is case-sensitive.

`"Sara"` and `"sara"` are different strings.

## 6. Membership Checks and Nested Tuples

When a Tuple contains another Tuple, `in` checks the elements at the current level.

```python
data = ("Ali", (10, 20, 30))

print(10 in data)
print((10, 20, 30) in data)
```

Output:

```text
False
True
```

Why is `10 in data` false?

Because the elements of `data` are:

```text
"Ali"
(10, 20, 30)
```

The number `10` is inside the nested Tuple, not directly inside `data`.

To check inside the nested Tuple, we need to access it first:

```python
data = ("Ali", (10, 20, 30))

print(10 in data[1])
```

Output:

```text
True
```

This distinction becomes important when working with nested data structures.

## 7. Membership Checking vs Indexing

Indexing and membership checking answer different questions.

Indexing:

```python
fruits = ("Apple", "Banana", "Orange")

print(fruits[1])
```

Output:

```text
Banana
```

Here we already know the position and want the value.

Membership checking:

```python
print("Banana" in fruits)
```

Output:

```text
True
```

Here we have a value and want to know whether it exists.

A useful mental model is:

```text
Indexing    → "What value is at this position?"
Membership  → "Does this value exist?"
```

Understanding this difference helps us choose the correct operation instead of trying to solve every problem with indexing.

# Questions

## Question 1

What will this code print?

```python
colors = ("Red", "Green", "Blue")

print("Green" in colors)
print("Yellow" in colors)
```

## Question 2

What is the difference between `in` and `not in`?

## Question 3

Why does this code print `False`?

```python
data = ("Ali", (10, 20, 30))

print(10 in data)
```

## Review Question

What is the difference between indexing and membership checking, and how can membership checking be used with an `if` statement?

# Answers

## Answer 1

```text
True
False
```

## Answer 2

`in` checks whether a value exists in a Tuple, while `not in` checks whether a value does not exist in a Tuple.

## Answer 3

Because `10` is not a direct element of `data`. It is inside the nested Tuple `(10, 20, 30)`.

## Review Answer

Indexing is used to access a value at a known position, while membership checking is used to determine whether a specific value exists. Membership checks can be combined with `if` to make decisions based on whether a value exists in the Tuple.

---

# Part 7 — Tuple Length and Counting Elements

## 1. Understanding the Size of a Tuple

A Tuple can contain any number of elements, from zero elements to many elements.

To find out how many elements a Tuple contains, we use the `len()` function.

```python
fruits = ("Apple", "Banana", "Orange")

print(len(fruits))
```

Output:

```text
3
```

The result is `3` because the Tuple contains three elements.

The important point is that `len()` counts the **elements of the Tuple**, not the number of characters inside those elements.

For example:

```python
fruits = ("Apple", "Banana", "Orange")

print(len(fruits))
```

Output:

```text
3
```

It does not count all the letters in the words.

## 2. Empty and Single-Element Tuples

`len()` also works with empty and single-element Tuples.

```python
empty = ()

single = (10,)

print(len(empty))
print(len(single))
```

Output:

```text
0
1
```

This is especially useful for understanding why `(10,)` is a Tuple while `(10)` is simply the number `10`.

## 3. Length and Indexes

There is an important relationship between the length of a Tuple and its indexes.

Consider:

```python
numbers = (10, 20, 30, 40, 50)

print(len(numbers))
```

Output:

```text
5
```

There are five elements, but the indexes are:

```text
0
1
2
3
4
```

Therefore:

```text
last index = length - 1
```

So for this Tuple:

```text
length = 5
last index = 4
```

This relationship is fundamental when working with indexed collections.

## 4. Counting Repeated Elements

`len()` tells us how many elements the entire Tuple contains.

But sometimes we want to know how many times a **specific value** appears.

For this, Tuples provide the `count()` method.

```python
numbers = (10, 20, 10, 30, 10)

print(numbers.count(10))
```

Output:

```text
3
```

The number `10` appears three times.

If the value does not appear:

```python
numbers = (10, 20, 30)

print(numbers.count(50))
```

Output:

```text
0
```

## 5. `len()` vs `count()`

These two operations answer different questions.

```python
numbers = (10, 20, 10, 30, 10)

print(len(numbers))
print(numbers.count(10))
```

Output:

```text
5
3
```

The difference is:

```text
len(tuple)       → How many elements are there in total?
tuple.count(x)   → How many times does x appear?
```

This distinction is important.

For example, if we have:

```python
colors = ("Red", "Blue", "Red", "Green", "Red")
```

then:

```python
len(colors)
```

asks:

> How many elements are in the Tuple?

while:

```python
colors.count("Red")
```

asks:

> How many times does `"Red"` occur?

## 6. Counting Elements in Real Data

Suppose we store the results of several tests:

```python
results = ("Pass", "Fail", "Pass", "Pass", "Fail")

print("Total results:", len(results))
print("Pass results:", results.count("Pass"))
print("Fail results:", results.count("Fail"))
```

Output:

```text
Total results: 5
Pass results: 3
Fail results: 2
```

This gives us useful information without changing the Tuple.

## 7. Case Sensitivity

`count()` compares values according to Python's normal equality rules.

For Strings, uppercase and lowercase letters are different.

```python
fruits = ("Apple", "apple", "Apple")

print(fruits.count("Apple"))
print(fruits.count("apple"))
```

Output:

```text
2
1
```

`"Apple"` and `"apple"` are different Strings.

## 8. Counting Does Not Modify the Tuple

Both `len()` and `count()` are operations that read information from the Tuple.

They do not change it.

```python
numbers = (10, 20, 10, 30)

print(len(numbers))
print(numbers.count(10))

print(numbers)
```

Output:

```text
4
2
(10, 20, 10, 30)
```

The Tuple remains exactly the same.

This connects directly to what we learned about Tuple immutability.

## 9. A Useful Mental Model

Think of these operations as answering different questions about the same Tuple:

```text
Tuple
(10, 20, 10, 30, 10)
```

```text
len(tuple)
      ↓
How many elements are there?
      ↓
5
```

and:

```text
tuple.count(10)
      ↓
How many times does 10 appear?
      ↓
3
```

Once this distinction is clear, `len()` and `count()` become simple but powerful tools for inspecting Tuple data.

# Questions

## Question 1

What will this code print?

```python
numbers = (10, 20, 30, 40)

print(len(numbers))
```

## Question 2

What will this code print?

```python
numbers = (10, 20, 10, 30, 10)

print(numbers.count(10))
```

## Question 3

What is the difference between `len(numbers)` and `numbers.count(10)`?

## Review Question

Explain how indexing, membership checking, `len()`, and `count()` answer four different questions about a Tuple.

# Answers

## Answer 1

```text
4
```

## Answer 2

```text
3
```

## Answer 3

`len(numbers)` returns the total number of elements, while `numbers.count(10)` returns the number of times `10` appears.

## Review Answer

Indexing asks which value is located at a specific position. Membership checking asks whether a value exists. `len()` asks how many elements the Tuple contains in total. `count()` asks how many times a specific value occurs.

---

# Part 8 — Finding the Position of an Element

## 1. Why Do We Need the Position?

In the previous section, we learned how to check whether an element exists in a Tuple using `in`.

For example:

```python
fruits = ("Apple", "Banana", "Orange", "Mango")

print("Orange" in fruits)
```

Output:

```text
True
```

But sometimes knowing that an element exists is not enough.

We may need to know **where that element is located**.

For this purpose, Python provides the `index()` method.

## 2. Using `index()`

The basic syntax is:

```python
tuple.index(value)
```

For example:

```python
fruits = ("Apple", "Banana", "Orange", "Mango")

print(fruits.index("Orange"))
```

Output:

```text
2
```

The result is `2` because `"Orange"` is located at index `2`.

Remember that Tuple indexes start from `0`:

```text
Apple   → 0
Banana  → 1
Orange  → 2
Mango   → 3
```

## 3. `index()` Returns the First Occurrence

A Tuple can contain repeated values.

For example:

```python
fruits = ("Apple", "Banana", "Apple", "Orange", "Apple")

print(fruits.index("Apple"))
```

Output:

```text
0
```

There are three `"Apple"` values, but `index()` returns only the position of the **first occurrence**.

This is important:

```text
index()
↓
first matching position
```

It does not return all positions where the value appears.

## 4. `in` vs `index()`

The `in` operator and `index()` method are related, but they have different purposes.

```python
fruits = ("Apple", "Banana", "Orange")

print("Banana" in fruits)
print(fruits.index("Banana"))
```

Output:

```text
True
1
```

The first expression asks:

```text
Does "Banana" exist?
```

The second asks:

```text
Where is "Banana"?
```

So:

```text
in       → checks existence
index()  → finds position
```

If we only need a Boolean answer, `in` is enough.

If we need the position, we use `index()`.

## 5. What Happens When the Element Does Not Exist?

If the requested value does not exist, `index()` raises a `ValueError`.

For example:

```python
fruits = ("Apple", "Banana", "Orange")

print(fruits.index("Mango"))
```

Output:

```text
ValueError: tuple.index(x): x not in tuple
```

This is different from `in`.

With `in`:

```python
print("Mango" in fruits)
```

Output:

```text
False
```

With `index()`:

```python
print(fruits.index("Mango"))
```

Python cannot provide a valid position, so it raises an error.

Therefore, if we are not sure that the element exists, checking membership first can be useful.

## 6. Combining `in` and `index()`

We can safely combine these two operations:

```python
fruits = ("Apple", "Banana", "Orange")

if "Banana" in fruits:
    print(fruits.index("Banana"))
```

Output:

```text
1
```

The logic is:

```text
Check whether the value exists
            ↓
          True
            ↓
Find its position
```

This pattern is useful when the data may or may not contain the requested value.

## 7. Searching from a Specific Position

`index()` can also receive a `start` argument.

```python
tuple.index(value, start)
```

For example:

```python
fruits = ("Apple", "Banana", "Apple", "Orange", "Apple")

print(fruits.index("Apple", 1))
```

Output:

```text
2
```

Why `2`?

Because Python starts searching from index `1`.

The first `"Apple"` is at index `0`, so it is ignored.

The next `"Apple"` is at index `2`.

We can also specify both `start` and `stop`:

```python
tuple.index(value, start, stop)
```

For example:

```python
fruits = ("Apple", "Banana", "Apple", "Orange", "Apple")

print(fruits.index("Apple", 1, 4))
```

Output:

```text
2
```

The search begins at index `1` and stops before index `4`.

The same rule used in slicing applies here:

```text
start → included
stop  → excluded
```

## 8. Finding the Position of a Nested Tuple

`index()` searches the elements of the Tuple on which it is called.

Consider:

```python
data = ("Ali", (10, 20, 30))

print(data.index((10, 20, 30)))
```

Output:

```text
1
```

The nested Tuple `(10, 20, 30)` is itself an element of `data`, so `index()` can find it.

However:

```python
print(data.index(10))
```

raises a `ValueError`.

Why?

Because `10` is not a direct element of `data`.

The structure is:

```text
data
├── "Ali"
└── (10, 20, 30)
      ├── 10
      ├── 20
      └── 30
```

To search inside the nested Tuple, we first access it:

```python
data = ("Ali", (10, 20, 30))

print(data[1].index(10))
```

Output:

```text
0
```

This leads to an important principle:

> A search operation works on the collection on which it is called.

## 9. `index()` Does Not Modify the Tuple

`index()` only searches for information.

It does not modify the Tuple.

```python
numbers = (10, 20, 30)

position = numbers.index(20)

print(position)
print(numbers)
```

Output:

```text
1
(10, 20, 30)
```

The Tuple remains unchanged.

This is consistent with the immutability of Tuples.

## 10. Connecting `index()` with Previous Concepts

At this point, we have several tools for inspecting Tuple data:

```text
tuple[index]
    ↓
Access a value at a known position

value in tuple
    ↓
Check whether a value exists

len(tuple)
    ↓
Find the total number of elements

tuple.count(value)
    ↓
Count occurrences of a value

tuple.index(value)
    ↓
Find the position of the first occurrence
```

These operations answer different questions.

A good programmer does not simply memorize the syntax. The important skill is recognizing which question the program needs to answer.

# Questions

## Question 1

What will this code print?

```python
fruits = ("Apple", "Banana", "Orange")

print(fruits.index("Orange"))
```

## Question 2

What is the difference between these two expressions?

```python
"Banana" in fruits
fruits.index("Banana")
```

## Question 3

What will this code print?

```python
numbers = (10, 20, 10, 30, 10)

print(numbers.index(10))
```

## Review Question

Explain the difference between `in`, `count()`, and `index()` and describe what each one tells us about a Tuple.

# Answers

## Answer 1

```text
2
```

## Answer 2

`in` checks whether `"Banana"` exists and returns a Boolean value.

`index()` searches for `"Banana"` and returns the position of its first occurrence.

## Answer 3

```text
0
```

`index()` returns the position of the first occurrence.

## Review Answer

`in` checks whether a value exists, `count()` tells us how many times a value occurs, and `index()` tells us the position of the first occurrence.

---

# Part 9 — Iterating Through Tuples

## 1. What Does Iterating Mean?

In the previous section, we learned how to find the position of an element using `index()`.

However, many problems require us to work with **every element of a Tuple**, not just one specific element.

For example:

```python
fruits = ("Apple", "Banana", "Orange", "Mango")
```

If we want to process every fruit, manually accessing each index would be repetitive:

```python
print(fruits[0])
print(fruits[1])
print(fruits[2])
print(fruits[3])
```

Instead, we can **iterate through the Tuple**.

Iteration means going through the elements of a collection one by one and performing an operation on each element.

In Python, the most common way to iterate through a Tuple is with a `for` loop.

## 2. Iterating with `for`

The basic structure is:

```python
for element in tuple:
    # code
```

For example:

```python
fruits = ("Apple", "Banana", "Orange", "Mango")

for fruit in fruits:
    print(fruit)
```

Output:

```text
Apple
Banana
Orange
Mango
```

Python automatically gives `fruit` the value of the current element during each iteration.

Conceptually:

```text
Iteration 1 → Apple
Iteration 2 → Banana
Iteration 3 → Orange
Iteration 4 → Mango
```

The loop continues until all elements have been processed.

## 3. The Loop Variable

The variable after `for` represents the current element.

For example:

```python
numbers = (10, 20, 30)

for number in numbers:
    print(number)
```

Output:

```text
10
20
30
```

During each iteration:

```text
number = 10
number = 20
number = 30
```

The variable name itself is not special.

This also works:

```python
for x in numbers:
    print(x)
```

However, meaningful names are usually better:

```python
for number in numbers:
```

is easier to understand than:

```python
for x in numbers:
```

when the Tuple contains numbers.

## 4. Performing Operations During Iteration

Iteration allows us to process each value.

For example:

```python
numbers = (10, 20, 30, 40)

for number in numbers:
    print(number * 2)
```

Output:

```text
20
40
60
80
```

The original Tuple remains unchanged.

We are reading each value and performing an operation on it.

This is especially important with Tuples because their elements cannot be replaced directly.

## 5. Iteration with Conditions

We can combine `for` with `if`.

For example, suppose we only want numbers greater than `20`:

```python
numbers = (10, 25, 15, 40, 30)

for number in numbers:
    if number > 20:
        print(number)
```

Output:

```text
25
40
30
```

The general pattern is:

```text
iterate
   ↓
inspect current element
   ↓
check condition
   ↓
perform action when condition is true
```

This pattern appears throughout Python programming.

## 6. Iteration for Counting

We can also count elements that satisfy a condition.

```python
numbers = (10, 25, 15, 40, 30)

count = 0

for number in numbers:
    if number > 20:
        count += 1

print(count)
```

Output:

```text
3
```

The Tuple is traversed once.

Each time a number greater than `20` is found, `count` increases by one.

Notice that this is different from `count()`:

```python
numbers.count(10)
```

`count()` counts occurrences of a **specific value**.

The loop allows us to count elements based on a **condition**.

## 7. Iterating with Indexes Using `enumerate()`

Sometimes we need both the element and its index.

Python provides `enumerate()` for this purpose.

```python
fruits = ("Apple", "Banana", "Orange")

for index, fruit in enumerate(fruits):
    print(index, fruit)
```

Output:

```text
0 Apple
1 Banana
2 Orange
```

Each iteration provides two values:

```text
index → position
fruit → value
```

This is usually cleaner than manually creating and updating an index variable.

For example, instead of:

```python
index = 0

for fruit in fruits:
    print(index, fruit)
    index += 1
```

we can use:

```python
for index, fruit in enumerate(fruits):
    print(index, fruit)
```

## 8. Starting `enumerate()` from Another Number

By default, `enumerate()` starts counting from `0`.

We can change the starting number with `start`:

```python
fruits = ("Apple", "Banana", "Orange")

for index, fruit in enumerate(fruits, start=1):
    print(index, fruit)
```

Output:

```text
1 Apple
2 Banana
3 Orange
```

This changes only the displayed counter.

It does **not** change the actual Tuple indexes.

The real indexes are still:

```text
Apple   → 0
Banana  → 1
Orange  → 2
```

## 9. Iterating in Reverse

Sometimes we need to process the elements from the last one to the first one.

We can use `reversed()`:

```python
numbers = (10, 20, 30, 40)

for number in reversed(numbers):
    print(number)
```

Output:

```text
40
30
20
10
```

This allows us to reverse the traversal order without changing the original Tuple.

The Tuple remains:

```python
(10, 20, 30, 40)
```

## 10. Iterating Through Nested Tuples

A Tuple can contain other Tuples.

For example:

```python
students = (
    ("Ali", 18),
    ("Sara", 20),
    ("Reza", 17)
)
```

We can iterate through the outer Tuple:

```python
for student in students:
    print(student)
```

Output:

```text
('Ali', 18)
('Sara', 20)
('Reza', 17)
```

But because each element is itself a Tuple, we can unpack it during iteration:

```python
for name, score in students:
    print(name, score)
```

Output:

```text
Ali 18
Sara 20
Reza 17
```

This is especially useful when a Tuple represents a structured piece of information.

## 11. Iteration Does Not Modify the Tuple

A common misunderstanding is thinking that changing the loop variable changes the Tuple.

For example:

```python
numbers = (10, 20, 30)

for number in numbers:
    number = number * 2

print(numbers)
```

Output:

```text
(10, 20, 30)
```

The assignment:

```python
number = number * 2
```

changes only the loop variable.

It does not replace the corresponding element inside the Tuple.

This is consistent with Tuple immutability.

## 12. Why Iteration Matters

Iteration is more than a convenient way to print values.

It allows us to build algorithms that operate on collections.

For example, we can:

```text
Read every element
      ↓
Analyze its value
      ↓
Compare it with a condition
      ↓
Count or process it
      ↓
Produce a result
```

This makes iteration one of the fundamental mechanisms for processing collections in Python.

The important question is not:

> "How do I loop through this Tuple?"

but rather:

> "What should my program do with each element as it visits it?"

That shift in thinking is what turns a loop from simple syntax into an algorithmic tool.

# Questions

## Question 1

What will this code print?

```python
numbers = (5, 10, 15, 20)

for number in numbers:
    if number >= 15:
        print(number)
```

## Question 2

What is the purpose of `enumerate()` when iterating through a Tuple?

## Question 3

What will this code print?

```python
numbers = (10, 20, 30)

for number in reversed(numbers):
    print(number)
```

## Review Question

Explain how you would iterate through a Tuple when you need only its values, when you need both the index and value, and when the Tuple contains nested structured data.

# Answers

## Answer 1

```text
15
20
```

## Answer 2

`enumerate()` allows us to receive both the index and the current element during each iteration.

## Answer 3

```text
30
20
10
```

## Review Answer

For values only:

```python
for element in tuple:
```

For both index and value:

```python
for index, element in enumerate(tuple):
```

For nested structured Tuples, we can unpack the elements directly:

```python
for value1, value2 in tuple:
```

---

