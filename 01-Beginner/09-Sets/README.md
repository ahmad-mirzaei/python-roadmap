## Course Outline

| #  | Topic                                             |
| -- | ------------------------------------------------- |
| 1  | Introduction to Sets                              |
| 2  | Creating Sets                                     |
| 3  | Adding Elements to a Set                          |
| 4  | Removing Elements from a Set                      |
| 5  | Checking for an Element in a Set                  |
| 6  | Set Length and Counting Elements                  |
| 7  | Iterating Through Sets                            |
| 8  | Set Union                                         |
| 9  | Set Intersection                                  |
| 10 | Set Difference                                    |
| 11 | Set Symmetric Difference                          |
| 12 | Converting Between Sets and Other Data Structures |
| 13 | Set Immutability and `frozenset`                  |
| 14 | Final Review: Sets                                |
| 15 | Sets Mini Project                                 |

---

# Sets — Part 1: Introduction to Sets

> 🌐 Language: **English** | [فارسی](fa/README.md)

## What Is a Set?

A **Set** is a built-in Python data structure used to store a collection of **unique elements**.

The most important characteristic of a Set is that it does **not allow duplicate elements**.

For example:

```python
numbers = {1, 2, 3, 4}
```

Here, `numbers` is a Set containing four elements.

Unlike a List:

```python
numbers = [1, 2, 3, 4]
```

a Set does not use positions or indexes to organize its elements.

---

## Sets Do Not Contain Duplicate Elements

Consider this Set:

```python
numbers = {1, 2, 2, 3, 3, 3}
```

Python automatically removes the duplicates.

If you display it:

```python
print(numbers)
```

you will get a Set containing only the unique values:

```text
{1, 2, 3}
```

This makes Sets especially useful when you need to work with unique values.

For example:

```python
names = {"Ali", "Sara", "Ali", "Reza", "Sara"}

print(names)
```

The result contains each name only once.

---

## Sets Are Unordered

Sets do not provide index-based ordering like Lists or Tuples.

For example, with a List:

```python
numbers = [10, 20, 30]

print(numbers[0])
```

we can access the first element.

But this does **not** work with a Set:

```python
numbers = {10, 20, 30}

print(numbers[0])
```

You will get an error because Sets do not support indexing.

So you should think about Sets differently:

```text
List / Tuple
    ↓
Ordered collection
    ↓
Index-based access

Set
    ↓
Collection of unique elements
    ↓
No index-based access
```

The main purpose of a Set is not to preserve positions.

---

## Creating an Empty Set

There is an important detail when creating an empty Set.

This:

```python
empty = {}
```

does **not** create an empty Set.

It creates an empty Dictionary.

To create an empty Set, use:

```python
empty = set()
```

You can verify this:

```python
print(type(empty))
```

The result will be:

```text
<class 'set'>
```

Compare that with:

```python
empty = {}

print(type(empty))
```

which produces:

```text
<class 'dict'>
```

This is a very common beginner mistake.

---

## Sets Can Contain Different Data Types

A Set can contain multiple types of hashable values:

```python
data = {10, "Python", 3.14, True}
```

However, the elements of a Set must be **hashable**.

For now, you can think of hashable values as values that Python can safely use as unique Set elements.

Common examples include:

* integers;
* floats;
* strings;
* booleans;
* tuples containing hashable elements.

Lists cannot be Set elements:

```python
numbers = {[1, 2], [3, 4]}
```

because Lists are mutable and therefore unhashable.

We will study this concept more carefully later when we discuss `frozenset` and Set behavior.

---

## Why Use Sets?

Sets are particularly useful when you need to:

### Remove duplicates

```python
numbers = [1, 2, 2, 3, 3, 4]

unique_numbers = set(numbers)

print(unique_numbers)
```

### Check membership

```python
languages = {"Python", "Java", "C++"}

print("Python" in languages)
```

The result is:

```text
True
```

### Compare collections

Sets provide operations such as:

* Union
* Intersection
* Difference
* Symmetric Difference

These operations become especially useful when comparing groups of data.

For example:

```text
Students who study Python
        ∩
Students who study Java
```

can represent:

> Students who study both Python and Java.

We will explore these operations in later parts.

---

## Set vs List vs Tuple

It is important to understand the difference between the three structures we have studied so far.

| Feature      | List               | Tuple            | Set             |
| ------------ | ------------------ | ---------------- | --------------- |
| Ordered      | Yes                | Yes              | No              |
| Indexing     | Yes                | Yes              | No              |
| Duplicates   | Allowed            | Allowed          | Not allowed     |
| Mutable      | Yes                | No               | Yes             |
| Main purpose | General collection | Fixed collection | Unique elements |

For example:

```python
numbers_list = [1, 2, 2, 3]
numbers_tuple = (1, 2, 2, 3)
numbers_set = {1, 2, 2, 3}
```

The List and Tuple keep the duplicate `2`.

The Set automatically keeps only one `2`.

---

## A Practical Example

Imagine that you collect the names of students who attended several classes.

For the first class:

```python
python_students = {"Ali", "Sara", "Reza"}
```

For the second class:

```python
java_students = {"Sara", "Reza", "Mina"}
```

Later, we may want to answer questions such as:

* Who attended at least one class?
* Who attended both classes?
* Who attended Python but not Java?
* Which students are unique to each class?

Sets are designed specifically for this type of problem.

The answers can be found using Set Operations, which we will study in the upcoming parts.

---

## Key Takeaways

At this point, remember these core ideas:

1. A Set stores **unique elements**.
2. Duplicate elements are automatically removed.
3. Sets do not support index-based access.
4. `{}` creates an empty Dictionary, not an empty Set.
5. Use `set()` to create an empty Set.
6. Sets are especially useful for membership checking and comparing collections.
7. Set elements must be hashable.
8. Set Operations such as Union and Intersection are important tools for working with collections of unique data.

In the next part, we will learn the different ways to **create Sets** in Python.

---

# Sets — Part 2: Creating Sets

## Creating Sets

In the previous part, we learned what a Set is and why it is useful.

Now we will learn the different ways to **create Sets in Python**.

---

## 1. Creating a Set with Curly Braces

The simplest way to create a Set is to place elements inside `{}`:

```python
numbers = {1, 2, 3, 4}
```

Python recognizes this as a Set because it contains elements separated by commas.

You can check its type:

```python
print(type(numbers))
```

Output:

```text
<class 'set'>
```

---

## 2. Creating a Set of Strings

Sets can contain Strings:

```python
languages = {"Python", "Java", "C++"}
```

You can also create a Set of names:

```python
names = {"Ali", "Sara", "Reza"}
```

Each element is stored only once.

---

## 3. Creating a Set with Different Data Types

A Set can contain different hashable data types:

```python
data = {10, "Python", 3.14, True}
```

However, remember that Set elements must be hashable.

For example, this is invalid:

```python
data = {[1, 2], [3, 4]}
```

because Lists are mutable and unhashable.

---

## 4. Duplicate Values Are Automatically Removed

When creating a Set, duplicate values are automatically eliminated:

```python
numbers = {1, 2, 2, 3, 3, 4}
```

The resulting Set contains:

```text
{1, 2, 3, 4}
```

This happens immediately when Python creates the Set.

So a Set can be useful when you want to represent only unique values.

---

## 5. Creating an Empty Set

As we saw in the previous part, `{}` does not create an Empty Set.

This:

```python
empty = {}
```

creates a Dictionary.

To create an Empty Set, use:

```python
empty = set()
```

Check the type:

```python
print(type(empty))
```

Output:

```text
<class 'set'>
```

This distinction is very important.

```python
{}
```

means:

```text
Empty Dictionary
```

while:

```python
set()
```

means:

```text
Empty Set
```

---

## 6. Creating a Set from a List

You can create a Set from an existing List using the `set()` constructor:

```python
numbers = [1, 2, 2, 3, 4, 4]

unique_numbers = set(numbers)

print(unique_numbers)
```

The duplicate values are removed.

Conceptually:

```text
List
    ↓
set()
    ↓
Set of unique elements
```

This is one of the most common ways to use `set()`.

---

## 7. Creating a Set from a Tuple

The same idea works with Tuples:

```python
numbers = (1, 2, 2, 3, 4)

unique_numbers = set(numbers)
```

Now `unique_numbers` is a Set containing only the unique values.

---

## 8. Creating a Set from a String

You can also pass a String to `set()`:

```python
letters = set("hello")

print(letters)
```

The Set contains the unique characters from the String.

For example, the characters may be represented as:

```text
{'h', 'e', 'l', 'o'}
```

Notice that the second `l` does not appear twice.

This happens because each character is treated as an individual element and Sets only keep unique elements.

---

## 9. Creating a Set from a Dictionary

When you pass a Dictionary to `set()`, Python uses the Dictionary's **Keys**:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}

keys = set(student)

print(keys)
```

The resulting Set contains:

```text
{'name', 'age', 'city'}
```

This is important because:

```python
set(dictionary)
```

works with the Keys, not the Values.

If you want to create a Set from the Values, you can explicitly use:

```python
values = set(student.values())
```

---

## 10. Creating a Set from Dictionary Items

You can also work with the Dictionary's Items:

```python
student = {
    "name": "Ali",
    "age": 20
}

items = set(student.items())
```

This creates a Set containing Tuples:

```text
{
    ('name', 'Ali'),
    ('age', 20)
}
```

This works because the Keys and Values in these Tuples are hashable.

---

## 11. Creating a Set with `set()`

The `set()` constructor is especially useful when the source data already exists:

```python
numbers = [1, 2, 3, 3, 4]

numbers_set = set(numbers)
```

You can use the same pattern with many iterable objects:

```python
set(list_data)
set(tuple_data)
set(string_data)
set(dictionary_data)
```

The exact result depends on the elements contained in the source object.

---

## 12. Set Comprehension

Python also supports **Set Comprehension**.

The basic structure is:

```python
{expression for item in iterable}
```

For example:

```python
numbers = {x for x in range(5)}
```

This produces a Set containing:

```text
{0, 1, 2, 3, 4}
```

You can also apply a condition:

```python
even_numbers = {x for x in range(10) if x % 2 == 0}
```

The result contains the unique even numbers.

Set Comprehension is useful, but for now focus on understanding the basic idea:

```text
Iterable
    ↓
Process each element
    ↓
Generate a value
    ↓
Store the values in a Set
```

We will use Comprehensions more comfortably as we progress.

---

## 13. Set Comprehension vs List Comprehension

The syntax is very similar.

List Comprehension:

```python
numbers = [x for x in range(5)]
```

Set Comprehension:

```python
numbers = {x for x in range(5)}
```

The main visual difference is:

```text
[ ] → List
{ } → Set
```

However, remember that `{}` by itself creates a Dictionary, not a Set.

The presence of an expression inside the braces allows Python to recognize a Set Comprehension.

---

## 14. Choosing the Right Creation Method

Different situations call for different approaches.

### You already know the values

Use:

```python
numbers = {1, 2, 3, 4}
```

### You have a List

Use:

```python
numbers = set(my_list)
```

### You have a Tuple

Use:

```python
numbers = set(my_tuple)
```

### You have a String

Use:

```python
letters = set("hello")
```

### You need to create an Empty Set

Use:

```python
numbers = set()
```

### You want to generate values dynamically

Use Set Comprehension:

```python
numbers = {x for x in range(10)}
```

---

## Common Beginner Mistakes

### Mistake 1 — Using `{}` for an Empty Set

Incorrect:

```python
numbers = {}
```

Correct:

```python
numbers = set()
```

---

### Mistake 2 — Expecting Duplicates to remain

```python
numbers = {1, 1, 2, 2, 3}
```

This does not create five elements.

It creates a Set containing three unique elements.

---

### Mistake 3 — Putting a List inside a Set

This is invalid:

```python
numbers = {[1, 2], [3, 4]}
```

because Lists are unhashable.

---

### Mistake 4 — Assuming Set order

Do not write code that depends on a particular displayed order:

```python
numbers = {10, 20, 30}
```

The purpose of a Set is uniqueness and Set Operations, not positional access.

---

## Key Takeaways

After this part, you should know:

1. Sets can be created using `{}` with elements.
2. Empty Sets must be created with `set()`.
3. `set()` can convert Lists, Tuples, Strings, and other iterable objects into Sets.
4. Duplicate values are automatically removed.
5. A Dictionary passed to `set()` produces a Set of its Keys.
6. `set(dictionary.values())` can be used to create a Set from Values.
7. Dictionary Items can be converted into a Set when the resulting Tuples are hashable.
8. Set Comprehension provides a concise way to generate Sets.
9. Set elements must be hashable.
10. Set creation should be chosen based on the type and purpose of the source data.

In the next part, we will learn how to **add elements to a Set** after it has been created.

---

# Sets — Part 3: Adding Elements to a Set

## Adding Elements to a Set

In the previous part, we learned how to create Sets in Python.

Now we will learn how to **add new elements to an existing Set**.

The main method for this is:

```python
set.add()
```

---

## 1. Using `add()`

The `add()` method adds one element to a Set.

```python
numbers = {1, 2, 3}

numbers.add(4)

print(numbers)
```

The Set now contains `4` as well:

```text
{1, 2, 3, 4}
```

The syntax is:

```python
set_name.add(element)
```

For example:

```python
languages = {"Python", "Java"}

languages.add("C++")
```

Now:

```text
{"Python", "Java", "C++"}
```

---

## 2. Adding an Existing Element

What happens if we add an element that already exists?

```python
numbers = {1, 2, 3}

numbers.add(2)

print(numbers)
```

Nothing changes.

The Set remains:

```text
{1, 2, 3}
```

This is because Sets only store **unique elements**.

So `add()` does not create duplicates.

---

## 3. Adding Elements One at a Time

`add()` adds **one element at a time**.

```python
numbers = {1, 2}

numbers.add(3)
numbers.add(4)
numbers.add(5)

print(numbers)
```

The final Set contains:

```text
{1, 2, 3, 4, 5}
```

Each call to `add()` adds one element.

---

## 4. Adding a String

You can add a String as one element:

```python
languages = {"Python", "Java"}

languages.add("JavaScript")
```

The entire String `"JavaScript"` is one Set element.

It does **not** add each character separately.

```python
languages.add("Go")
```

Now `"Go"` is another single element.

---

## 5. Adding a Tuple

Because Tuples can be hashable, a Tuple can be added to a Set:

```python
data = {1, 2, 3}

data.add((4, 5))

print(data)
```

The Tuple `(4, 5)` is treated as one element.

Conceptually:

```text
Set
 ├── 1
 ├── 2
 ├── 3
 └── (4, 5)
```

---

## 6. Trying to Add a List

A List cannot be added directly to a Set:

```python
numbers = {1, 2, 3}

numbers.add([4, 5])
```

This produces an error because Lists are **unhashable**.

You will typically see:

```text
TypeError: unhashable type: 'list'
```

This connects directly to the Hashable concept we introduced earlier.

---

## 7. `add()` Does Not Return the Updated Set

One important detail about `add()` is that it modifies the existing Set **in place**.

It does not return the modified Set.

For example:

```python
numbers = {1, 2, 3}

result = numbers.add(4)

print(result)
```

The output is:

```text
None
```

But the Set itself has changed:

```python
print(numbers)
```

Output:

```text
{1, 2, 3, 4}
```

So remember:

```text
add()
  ↓
modifies the Set
  ↓
returns None
```

This is a common source of confusion for beginners.

---

## 8. Adding User Input

We can also add values entered by the user.

```python
names = set()

name = input("Enter your name: ")

names.add(name)

print(names)
```

The entered name is added to the Set.

Because this is a Set, entering the same name again will not create a duplicate.

For example, if we repeatedly add:

```text
Ali
Sara
Ali
Reza
```

the Set will contain only:

```text
{"Ali", "Sara", "Reza"}
```

---

## 9. Adding Values in a Loop

We can use `add()` inside a loop:

```python
numbers = set()

for number in range(1, 6):
    numbers.add(number)

print(numbers)
```

The result contains:

```text
{1, 2, 3, 4, 5}
```

This is useful when values are generated dynamically.

---

## 10. `add()` vs `set()`

These two have completely different purposes.

`set()` is commonly used to **create or convert data into a Set**:

```python
numbers = set([1, 2, 3])
```

`add()` is used to **add one new element to an existing Set**:

```python
numbers.add(4)
```

Think of them like this:

```text
set()
  ↓
Create / Convert

add()
  ↓
Add one element
```

---

## 11. `add()` vs `update()`

You will encounter `update()` soon, so it is important to understand the difference.

`add()` adds **one element**:

```python
numbers = {1, 2}

numbers.add(3)
```

`update()` can add **multiple elements from an iterable**:

```python
numbers = {1, 2}

numbers.update([3, 4, 5])
```

Result:

```text
{1, 2, 3, 4, 5}
```

For now, remember:

```text
add()
→ one element

update()
→ multiple elements
```

We will study `update()` more carefully when we work with Set modification.

---

## Common Beginner Mistakes

### Mistake 1 — Expecting `add()` to return the Set

Incorrect:

```python
numbers = {1, 2, 3}

numbers = numbers.add(4)
```

After this assignment, `numbers` becomes `None`.

Correct:

```python
numbers = {1, 2, 3}

numbers.add(4)
```

---

### Mistake 2 — Adding a List

Incorrect:

```python
numbers.add([4, 5])
```

Lists are unhashable.

If you want `(4, 5)` to be one element, you can use a Tuple:

```python
numbers.add((4, 5))
```

---

### Mistake 3 — Expecting Duplicates

```python
numbers = {1, 2, 3}

numbers.add(3)
numbers.add(3)
```

The Set still contains only one `3`.

---

## Key Takeaways

After this part, you should know:

1. `add()` adds one element to an existing Set.
2. Adding an existing element does not create a duplicate.
3. `add()` modifies the Set in place.
4. `add()` returns `None`.
5. Hashable objects such as Tuples can be added to a Set.
6. Lists cannot be added directly because they are unhashable.
7. `add()` can be used inside loops and with user input.
8. `set()` is mainly used to create or convert Sets, while `add()` adds one element.
9. `add()` and `update()` have different purposes.

---

## Exercises

### Question 1

What will the final value of `numbers` contain?

```python
numbers = {1, 2, 3}

numbers.add(3)
numbers.add(4)
numbers.add(4)
numbers.add(5)
```

---

### Question 2

Fix the following code so that `(10, 20)` is added as one element to the Set:

```python
data = {1, 2, 3}

data.add([10, 20])
```

---

### Question 3

What will be printed?

```python
numbers = {1, 2}

result = numbers.add(3)

print(result)
print(numbers)
```

Explain why the two outputs are different.

---

## Comprehensive Set Question

Create a program that starts with this Set:

```python
students = {"Ali", "Sara", "Reza"}
```

Then:

1. Add `"Mina"` to the Set.
2. Try to add `"Ali"` again.
3. Add the names `"Omid"` and `"Nima"` one at a time using `add()`.
4. Print the final Set.
5. Explain why `"Ali"` appears only once.
6. Store the return value of one `add()` call in a variable and explain what that value is.

Your goal is to demonstrate everything we have learned so far about **creating Sets, uniqueness, hashable elements, and adding elements**.

---

