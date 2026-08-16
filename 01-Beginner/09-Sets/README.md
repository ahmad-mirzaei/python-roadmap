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

# Sets — Part 4: Removing Elements from a Set

In the previous part, we learned how to add elements to a Set using `add()`.

Now we will learn how to **remove elements from a Set**.

Python provides several methods for this:

* `remove()`
* `discard()`
* `pop()`
* `clear()`

Although they all modify a Set, they behave differently.

---

## 1. Using `remove()`

The `remove()` method removes a specific element from a Set.

```python
numbers = {1, 2, 3, 4}

numbers.remove(3)

print(numbers)
```

The result contains:

```text
{1, 2, 4}
```

The syntax is:

```python
set_name.remove(element)
```

---

## 2. What Happens If the Element Does Not Exist?

This is one of the most important differences between `remove()` and `discard()`.

If the element does not exist:

```python
numbers = {1, 2, 3}

numbers.remove(5)
```

Python raises a `KeyError`.

For example:

```text
KeyError: 5
```

So `remove()` should be used when you expect the element to exist.

---

## 3. Using `discard()`

The `discard()` method also removes a specific element:

```python
numbers = {1, 2, 3, 4}

numbers.discard(3)

print(numbers)
```

Result:

```text
{1, 2, 4}
```

But there is an important difference.

If the element does not exist:

```python
numbers = {1, 2, 3}

numbers.discard(5)

print(numbers)
```

Nothing happens.

No error is raised.

The Set remains:

```text
{1, 2, 3}
```

---

## 4. `remove()` vs `discard()`

This distinction is very important:

| Method      | Element exists | Element does not exist |
| ----------- | -------------- | ---------------------- |
| `remove()`  | Removes it     | Raises `KeyError`      |
| `discard()` | Removes it     | Does nothing           |

A simple way to remember:

```text
remove()
→ "I expect this element to exist."

discard()
→ "Remove it if it exists."
```

For beginner code, `discard()` is often useful when you do not want to handle an error for a missing element.

---

## 5. Using `pop()`

The `pop()` method removes and **returns an element** from the Set.

```python
numbers = {10, 20, 30, 40}

value = numbers.pop()

print(value)
print(numbers)
```

The removed value is stored in `value`.

An important point:

**Sets are unordered, so you should not expect `pop()` to remove a particular element.**

Do not write code that assumes it always removes the smallest, largest, first, or last element.

The exact element removed should be treated as unspecified.

---

## 6. `pop()` Returns the Removed Element

Unlike `remove()` and `discard()`, `pop()` gives us the removed element.

```python
numbers = {1, 2, 3}

removed = numbers.pop()

print(removed)
print(numbers)
```

The first `print()` displays the removed element.

The second displays the remaining Set.

Conceptually:

```text
Set
  ↓
pop()
  ↓
Remove one element
  ↓
Return that element
```

---

## 7. `pop()` on an Empty Set

If we call `pop()` on an Empty Set:

```python
numbers = set()

numbers.pop()
```

Python raises a `KeyError`.

So before using `pop()` on a Set that may be empty, you should consider checking whether it contains elements.

For example:

```python
if numbers:
    value = numbers.pop()
```

---

## 8. Using `clear()`

The `clear()` method removes **all elements** from a Set.

```python
numbers = {1, 2, 3, 4}

numbers.clear()

print(numbers)
```

Result:

```text
set()
```

The Set itself still exists, but it is now empty.

Compare:

```python
numbers = {1, 2, 3}

numbers.clear()

print(type(numbers))
```

The type is still:

```text
<class 'set'>
```

---

## 9. `clear()` vs Creating a New Set

There is a difference between clearing a Set and assigning a new Empty Set.

Using `clear()`:

```python
numbers = {1, 2, 3}

numbers.clear()
```

The existing Set object is emptied.

Using assignment:

```python
numbers = {1, 2, 3}

numbers = set()
```

the variable `numbers` is reassigned to another Set object.

At the beginner level, both leave `numbers` empty, but the underlying behavior is different.

For now, remember:

```text
clear()
→ Empty the existing Set

set()
→ Create a new Empty Set
```

---

## 10. Removing Elements While Checking Conditions

Sometimes we need to remove a known element only if it exists.

One approach is:

```python
numbers = {1, 2, 3, 4}

if 3 in numbers:
    numbers.remove(3)
```

Another simple approach is:

```python
numbers.discard(3)
```

This is one reason `discard()` can be convenient.

---

## 11. Removing Multiple Elements

You can call removal methods multiple times:

```python
numbers = {1, 2, 3, 4, 5}

numbers.remove(1)
numbers.remove(2)
numbers.discard(5)

print(numbers)
```

The remaining elements are:

```text
{3, 4}
```

Each call changes the Set.

---

## 12. Important: Don't Modify a Set During Iteration

A common mistake is trying to remove elements from a Set while directly iterating over that same Set:

```python
numbers = {1, 2, 3, 4, 5}

for number in numbers:
    if number % 2 == 0:
        numbers.remove(number)
```

This can raise:

```text
RuntimeError: Set changed size during iteration
```

For now, avoid modifying a Set directly while iterating over it.

Later, when we study more advanced techniques, we will learn safer ways to filter and transform collections.

---

## 13. Choosing the Right Method

A useful summary:

### Use `remove()` when:

You expect the element to exist and want Python to notify you if it does not.

```python
numbers.remove(3)
```

### Use `discard()` when:

You want to remove an element if it exists, without raising an error if it is missing.

```python
numbers.discard(3)
```

### Use `pop()` when:

You want to remove **one unspecified element** and receive that removed element.

```python
value = numbers.pop()
```

### Use `clear()` when:

You want to remove **all elements**.

```python
numbers.clear()
```

---

## Common Beginner Mistakes

### Mistake 1 — Assuming `remove()` ignores missing elements

```python
numbers = {1, 2, 3}

numbers.remove(10)
```

This raises a `KeyError`.

Use `discard()` if a missing element should not cause an error.

---

### Mistake 2 — Assuming `pop()` removes the first element

Sets do not have indexes or a meaningful first element.

So this assumption is incorrect:

```python
numbers = {10, 20, 30}

numbers.pop()  # Not necessarily 10
```

---

### Mistake 3 — Expecting `pop()` to return the remaining Set

`pop()` returns the **removed element**, not the Set.

```python
removed = numbers.pop()
```

---

### Mistake 4 — Confusing `clear()` with `discard()`

`discard()` removes one specified element:

```python
numbers.discard(3)
```

`clear()` removes everything:

```python
numbers.clear()
```

---

## Key Takeaways

After this part, you should know:

1. `remove()` removes a specific element.
2. `remove()` raises `KeyError` if the element does not exist.
3. `discard()` removes a specific element without raising an error if it is missing.
4. `pop()` removes one unspecified element and returns it.
5. `pop()` raises `KeyError` when the Set is empty.
6. `clear()` removes all elements from a Set.
7. Sets are unordered, so you should not depend on which element `pop()` removes.
8. You should avoid modifying a Set directly while iterating over it.

---

## Exercises

### Question 1

What happens when this code runs?

```python
numbers = {1, 2, 3}

numbers.remove(5)
```

How would you change the code if you wanted the program to continue without an error?

---

### Question 2

Explain the difference between these two:

```python
numbers.remove(10)
```

and:

```python
numbers.discard(10)
```

What happens when `10` is not inside the Set?

---

### Question 3

What does the following code guarantee about the final Set?

```python
numbers = {1, 2, 3, 4, 5}

removed = numbers.pop()

print(removed)
print(numbers)
```

Can you predict exactly which number will be stored in `removed`?

---

## Comprehensive Set Question

Write a program that starts with:

```python
students = {"Ali", "Sara", "Reza", "Mina", "Omid"}
```

Then perform these operations:

1. Remove `"Sara"` using `remove()`.
2. Try to remove `"Sara"` again, but this time make sure the program does not raise an error.
3. Remove one remaining student using `pop()` and store the removed name in a variable.
4. Print the removed name and the remaining Set.
5. Finally, remove all remaining students using `clear()`.
6. Print the final Set.

Your solution should demonstrate the difference between:

`remove()` → `discard()` → `pop()` → `clear()`

and explain when each method should be used.

---

# Sets — Part 5: Checking for an Element in a Set

In the previous part, we learned how to remove elements from a Set.

Now we will learn how to **check whether an element exists inside a Set**.

The main operator for this is:

```python
in
```

We will also learn:

* `in`
* `not in`
* using membership checks with `if`
* membership checks with user input
* why Set membership is useful
* the difference between checking a Set and checking a List

---

## 1. Using `in`

The `in` operator checks whether an element exists in a Set.

```python
numbers = {1, 2, 3, 4, 5}

print(3 in numbers)
```

Output:

```text
True
```

Because `3` exists in the Set.

If we check for an element that does not exist:

```python
print(10 in numbers)
```

Output:

```text
False
```

So:

```text
element in set
→ True or False
```

---

## 2. Using `not in`

We can also check whether an element **does not exist** in a Set.

```python
numbers = {1, 2, 3, 4, 5}

print(10 not in numbers)
```

Output:

```text
True
```

Because `10` is not inside the Set.

For an existing element:

```python
print(3 not in numbers)
```

Output:

```text
False
```

Remember:

```text
in
→ checks existence

not in
→ checks non-existence
```

---

## 3. Using Membership Checks with `if`

Membership checks become especially useful with `if`.

```python
students = {"Ali", "Sara", "Reza"}

if "Ali" in students:
    print("Ali is in the Set")
```

Output:

```text
Ali is in the Set
```

If the student does not exist:

```python
if "Mina" in students:
    print("Mina is in the Set")
```

Nothing is printed because the condition is `False`.

We can also use `else`:

```python
students = {"Ali", "Sara", "Reza"}

if "Mina" in students:
    print("Mina is in the Set")
else:
    print("Mina is not in the Set")
```

Output:

```text
Mina is not in the Set
```

---

## 4. Checking User Input

Membership checks are very useful when working with user input.

```python
allowed_users = {"Ali", "Sara", "Reza"}

username = input("Enter your username: ")

if username in allowed_users:
    print("Access granted")
else:
    print("Access denied")
```

Here, the Set acts like a collection of allowed values.

For example, if the user enters:

```text
Sara
```

the result is:

```text
Access granted
```

But if the user enters:

```text
Mina
```

the result is:

```text
Access denied
```

---

## 5. Checking Before Removing

Membership checking can also be combined with removal.

For example:

```python
numbers = {1, 2, 3, 4}

if 3 in numbers:
    numbers.remove(3)

print(numbers)
```

Output:

```text
{1, 2, 4}
```

This prevents `remove()` from raising a `KeyError` when the element does not exist.

We could also use `discard()`:

```python
numbers.discard(3)
```

But understanding membership checks is important because `in` can be used for many other decisions.

---

## 6. Checking Before Adding

We can also check whether an element already exists before adding it.

```python
numbers = {1, 2, 3}

if 4 not in numbers:
    numbers.add(4)

print(numbers)
```

Result:

```text
{1, 2, 3, 4}
```

For Sets, this check is often unnecessary because Sets automatically prevent duplicates.

For example:

```python
numbers.add(4)
```

is already safe if `4` exists.

Still, explicit membership checks are useful when the program needs to make a decision based on whether an element exists.

---

## 7. Membership Checks Return Boolean Values

The result of `in` and `not in` is always a Boolean:

```python
numbers = {1, 2, 3}

result = 2 in numbers

print(result)
print(type(result))
```

Output:

```text
True
<class 'bool'>
```

So:

```python
2 in numbers
```

is an expression that evaluates to either:

```text
True
```

or:

```text
False
```

This means it can be used anywhere a Boolean condition is expected.

---

## 8. Checking Strings

Membership checking works with Strings stored inside a Set.

```python
languages = {"Python", "Java", "C++"}

print("Python" in languages)
```

Output:

```text
True
```

But:

```python
print("python" in languages)
```

returns:

```text
False
```

because String comparison is case-sensitive.

These are different values:

```text
"Python"
"python"
```

So be careful when checking user input.

---

## 9. Checking Different Data Types

A Set can contain different hashable data types.

For example:

```python
data = {1, "Python", 3.14, (10, 20)}

print(1 in data)
print("Python" in data)
print(3.14 in data)
print((10, 20) in data)
```

The result of each check is:

```text
True
```

The type and value being checked must match an element in the Set.

For example:

```python
print("1" in data)
```

returns:

```text
False
```

because `"1"` is a String while `1` is an Integer.

---

## 10. Checking for `None`

`None` can also be stored in a Set and checked:

```python
data = {1, 2, None}

print(None in data)
```

Output:

```text
True
```

This can be useful when working with collections that may contain missing or optional values.

---

## 11. Membership Checking and `if / elif / else`

We can perform multiple membership checks:

```python
commands = {"start", "stop", "pause"}

command = input("Enter a command: ")

if command in commands:
    print("Valid command")
else:
    print("Unknown command")
```

This pattern is useful when the program has a fixed collection of accepted values.

For example:

```text
start
stop
pause
```

are accepted, while other commands are rejected.

---

## 12. Set Membership vs List Membership

The `in` operator works with both Sets and Lists:

```python
numbers_list = [1, 2, 3, 4, 5]
numbers_set = {1, 2, 3, 4, 5}

print(4 in numbers_list)
print(4 in numbers_set)
```

Both return:

```text
True
```

But there is an important performance difference.

For a List, Python generally searches through the elements one by one.

For a Set, Python is designed to perform membership checks efficiently using hashing.

Conceptually:

```text
List
→ search through elements

Set
→ hash-based lookup
```

At the beginner level, the important idea is:

> Sets are especially useful when the main goal is quickly checking whether a value exists.

You do not need to memorize the implementation details yet.

---

## 13. Membership Checking Does Not Modify the Set

The `in` operator only checks the Set.

It does not add, remove, or otherwise modify anything.

```python
numbers = {1, 2, 3}

print(2 in numbers)

print(numbers)
```

Output:

```text
True
{1, 2, 3}
```

The Set remains unchanged.

This is different from methods such as:

```python
numbers.add(4)
numbers.remove(2)
numbers.clear()
```

which modify the Set.

---

## 14. A Practical Example

Imagine we have a Set of registered users:

```python
registered_users = {
    "Ali",
    "Sara",
    "Reza",
    "Mina"
}
```

We can check whether a user is registered:

```python
username = input("Enter your username: ")

if username in registered_users:
    print("User is registered")
else:
    print("User is not registered")
```

This is a very common real-world pattern.

The same idea can be used for:

* allowed commands
* valid categories
* registered users
* blocked users
* available options
* unique IDs
* permissions
* supported values

---

## Common Beginner Mistakes

### Mistake 1 — Confusing `in` with `add()`

Incorrect:

```python
numbers.in(3)
```

`in` is an operator, not a method.

Correct:

```python
3 in numbers
```

---

### Mistake 2 — Using `in` as if it modifies the Set

This:

```python
3 in numbers
```

only checks whether `3` exists.

It does not add or remove anything.

---

### Mistake 3 — Forgetting Case Sensitivity

```python
languages = {"Python"}

print("python" in languages)
```

Output:

```text
False
```

because `"Python"` and `"python"` are different Strings.

---

### Mistake 4 — Confusing Value and String Representation

```python
numbers = {1, 2, 3}

print("1" in numbers)
```

Output:

```text
False
```

because:

```text
1
```

is an Integer, while:

```text
"1"
```

is a String.

---

## Key Takeaways

After this part, you should know:

1. `in` checks whether an element exists in a Set.
2. `not in` checks whether an element does not exist.
3. Both return a Boolean value: `True` or `False`.
4. Membership checks are commonly used with `if`.
5. Membership checks do not modify the Set.
6. Set membership is especially useful for checking whether a value belongs to a collection.
7. String membership checks are case-sensitive.
8. The type of the value matters when checking membership.
9. Set membership is generally designed to be efficient because Sets use hashing.

---

## Exercises

### Question 1

What will this code print?

```python
numbers = {10, 20, 30}

print(20 in numbers)
print(50 in numbers)
print(10 not in numbers)
```

---

### Question 2

Write a program that asks the user for a language and checks whether it is inside this Set:

```python
languages = {"Python", "Java", "C++"}
```

If it exists, print:

```text
Supported language
```

Otherwise print:

```text
Unsupported language
```

---

### Question 3

Why does this code print `False`?

```python
numbers = {1, 2, 3}

print("1" in numbers)
```

Explain the difference between `1` and `"1"`.

---

## Comprehensive Set Question

Create a small access-control program using this Set:

```python
allowed_users = {"Ali", "Sara", "Reza", "Mina"}
```

The program should:

1. Ask the user to enter a username.
2. Check whether the username exists in `allowed_users`.
3. Print `"Access granted"` if the user exists.
4. Print `"Access denied"` otherwise.
5. If access is granted, remove that username from the Set using `remove()`.
6. Print the updated Set.
7. Ask for another username and use `not in` to determine whether that username is no longer in the Set.

Your solution should demonstrate the concepts learned so far:

**Creating Sets → Adding Elements → Removing Elements → `in` → `not in` → Boolean Conditions**

---

