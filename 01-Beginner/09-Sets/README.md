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

# Sets — Part 6: Set Length and Counting Elements

In the previous part, we learned how to check whether an element exists in a Set using `in` and `not in`.

Now we will learn how to **count the number of elements in a Set**.

The main function for this is:

```python
len()
```

---

## 1. Using `len()` with a Set

The `len()` function returns the number of elements in a Set.

```python
numbers = {10, 20, 30, 40}

print(len(numbers))
```

Output:

```text
4
```

The syntax is:

```python
len(set_name)
```

---

## 2. Sets Only Count Unique Elements

Because Sets do not store duplicate elements, `len()` counts only the unique elements.

```python
numbers = {1, 2, 2, 3, 3, 3}

print(len(numbers))
```

The Set is effectively:

```text
{1, 2, 3}
```

So the output is:

```text
3
```

This is one of the useful differences between Sets and Lists.

For example:

```python
numbers_list = [1, 2, 2, 3, 3, 3]
numbers_set = {1, 2, 2, 3, 3, 3}

print(len(numbers_list))
print(len(numbers_set))
```

Output:

```text
6
3
```

The List counts every element, while the Set counts only unique elements.

---

## 3. Counting Strings in a Set

`len()` works with Sets containing Strings as well.

```python
languages = {"Python", "Java", "C++", "Go"}

print(len(languages))
```

Output:

```text
4
```

Each unique String is one element.

---

## 4. Counting an Empty Set

An Empty Set has a length of zero.

```python
numbers = set()

print(len(numbers))
```

Output:

```text
0
```

This can be useful when checking whether a Set contains anything.

---

## 5. Using `len()` in an `if` Statement

We can use the result of `len()` in conditions.

```python
students = {"Ali", "Sara", "Reza"}

if len(students) > 0:
    print("The Set is not empty")
```

Output:

```text
The Set is not empty
```

We can also check whether the Set is empty:

```python
if len(students) == 0:
    print("The Set is empty")
```

---

## 6. A Simpler Way to Check Whether a Set Is Empty

Although `len()` works, Python provides a more common approach.

Instead of:

```python
if len(students) > 0:
    print("Not empty")
```

we can write:

```python
if students:
    print("Not empty")
```

And instead of:

```python
if len(students) == 0:
    print("Empty")
```

we can write:

```python
if not students:
    print("Empty")
```

This works because an Empty Set is considered **Falsy**.

A non-empty Set is considered **Truthy**.

Remember:

```text
Empty Set
→ False

Non-empty Set
→ True
```

---

## 7. Counting Elements After Adding

The length of a Set changes when new unique elements are added.

```python
numbers = {1, 2, 3}

print(len(numbers))

numbers.add(4)

print(len(numbers))
```

Output:

```text
3
4
```

But adding an existing element does not increase the length:

```python
numbers.add(4)

print(len(numbers))
```

The result is still:

```text
4
```

---

## 8. Counting Elements After Removing

Removing an existing element decreases the length.

```python
numbers = {1, 2, 3, 4}

numbers.remove(2)

print(len(numbers))
```

Output:

```text
3
```

But using `discard()` on an element that does not exist does not change the length:

```python
numbers.discard(10)

print(len(numbers))
```

The length remains:

```text
3
```

---

## 9. Using `len()` with User Input

We can build a Set from user input and then count its unique elements.

```python
names = set()

names.add(input("Enter a name: "))
names.add(input("Enter another name: "))
names.add(input("Enter another name: "))

print("Unique names:", len(names))
```

If the user enters:

```text
Ali
Sara
Ali
```

the Set contains:

```text
{"Ali", "Sara"}
```

So the output is:

```text
Unique names: 2
```

This demonstrates one of the most useful features of Sets: **counting unique values**.

---

## 10. Counting Unique Values from a List

A very common pattern is converting a List to a Set and then using `len()`.

```python
numbers = [1, 2, 2, 3, 3, 4, 4, 4]

unique_numbers = set(numbers)

print(len(unique_numbers))
```

Output:

```text
4
```

The unique values are:

```text
{1, 2, 3, 4}
```

This is a simple and powerful way to count unique values.

---

## 11. Comparing Total and Unique Counts

We can compare the length of a List with the length of a Set created from it.

```python
numbers = [1, 2, 2, 3, 3, 4]

unique_numbers = set(numbers)

print("Total:", len(numbers))
print("Unique:", len(unique_numbers))
```

Output:

```text
Total: 6
Unique: 4
```

The difference tells us that some values appeared more than once.

---

## 12. Detecting Duplicates

This technique can also help us determine whether a List contains duplicates.

```python
numbers = [1, 2, 3, 4]

if len(numbers) == len(set(numbers)):
    print("No duplicates")
else:
    print("Duplicates exist")
```

Output:

```text
No duplicates
```

Now consider:

```python
numbers = [1, 2, 2, 3, 4]

if len(numbers) == len(set(numbers)):
    print("No duplicates")
else:
    print("Duplicates exist")
```

Output:

```text
Duplicates exist
```

Why?

Because:

```text
len(numbers)
→ 5

len(set(numbers))
→ 4
```

The lengths are different, which means at least one duplicate existed.

---

## 13. Counting Elements in Different Types of Sets

A Set can contain different hashable types:

```python
data = {
    1,
    "Python",
    3.14,
    (10, 20)
}

print(len(data))
```

Output:

```text
4
```

Each item is one Set element:

```text
1
"Python"
3.14
(10, 20)
```

The contents of a Tuple do not get counted separately.

For example:

```python
data = {(10, 20)}

print(len(data))
```

Output:

```text
1
```

There is one Tuple as one Set element.

---

## 14. `len()` Does Not Count Characters Inside Strings

This is another important distinction.

Consider:

```python
languages = {"Python", "JavaScript"}

print(len(languages))
```

The result is:

```text
2
```

It does not count all the characters inside the Strings.

If you want the length of a String itself:

```python
language = "Python"

print(len(language))
```

Output:

```text
6
```

So:

```text
len(Set)
→ number of Set elements

len(String)
→ number of characters
```

The same function can have different meanings depending on the type of object.

---

## 15. `len()` and `in` Together

We can combine the concepts we have learned.

```python
students = {"Ali", "Sara", "Reza"}

if "Ali" in students and len(students) >= 3:
    print("Ali is registered and there are enough students")
```

Here:

* `in` checks membership.
* `len()` checks the number of elements.
* `and` combines the conditions.

This is an important step toward writing more realistic programs.

---

## 16. `len()` and `not in`

We can also combine `len()` with `not in`.

```python
students = {"Ali", "Sara", "Reza"}

if "Mina" not in students and len(students) < 5:
    print("Mina can be added")
```

Then:

```python
students.add("Mina")
```

This combines membership checking, counting, and modification.

---

## 17. Important Limitation: `len()` Does Not Tell You Which Elements Exist

Consider:

```python
numbers = {10, 20, 30}

print(len(numbers))
```

The result is:

```text
3
```

But `len()` does not tell us what the elements are.

For that, we need to work with:

* iteration
* membership checks
* printing the Set
* converting it to another data structure when appropriate

We will study iteration through Sets in a later part.

---

## Common Beginner Mistakes

### Mistake 1 — Thinking `len()` counts duplicates

```python
numbers = {1, 2, 2, 3}

print(len(numbers))
```

The result is:

```text
3
```

not `4`.

---

### Mistake 2 — Using `len()` to check membership

This is incorrect:

```python
if len(numbers) == 3:
    print("3 exists")
```

This checks whether the Set has exactly three elements.

It does **not** check whether the value `3` exists.

Use:

```python
if 3 in numbers:
    print("3 exists")
```

---

### Mistake 3 — Confusing an Empty Set with an Empty Dictionary

Remember:

```python
set()
```

creates an Empty Set.

But:

```python
{}
```

creates an Empty Dictionary.

This distinction will become especially important as we continue working with Python data structures.

---

## Key Takeaways

After this part, you should know:

1. `len(set_name)` returns the number of unique elements in a Set.
2. Duplicate values do not increase Set length.
3. An Empty Set has length `0`.
4. A non-empty Set can be checked directly with `if set_name`.
5. `not set_name` can be used to check whether a Set is empty.
6. `len(set)` and `len(list)` can produce different results when duplicates exist.
7. `len(set(list))` is a useful pattern for counting unique values.
8. Comparing `len(list)` and `len(set(list))` can help detect duplicates.
9. `len()` counts Set elements, not the characters inside String elements.
10. `len()` can be combined with `in`, `not in`, `and`, and other conditions.

---

## Exercises

### Question 1

What will this code print?

```python
numbers = {1, 2, 2, 3, 3, 3, 4}

print(len(numbers))
```

Explain why.

---

### Question 2

Write a program that takes this List:

```python
numbers = [1, 2, 2, 3, 4, 4, 5, 5, 5]
```

and prints:

```text
Total: ...
Unique: ...
```

using `len()` and `set()`.

---

### Question 3

What is the difference between these two conditions?

```python
if len(numbers) == 0:
```

and:

```python
if not numbers:
```

Are they checking the same thing when `numbers` is a Set?

---

## Comprehensive Set Question

Create a program that starts with:

```python
students = {"Ali", "Sara", "Reza"}
```

Then:

1. Print the number of students using `len()`.
2. Ask the user for a new student name.
3. Check whether that student is already in the Set using `in`.
4. If the student is not already present, add the student using `add()`.
5. Print the new number of unique students.
6. Ask for a student name to remove.
7. If the student exists, remove them.
8. Print the final Set and its length.
9. If the Set becomes empty, detect it using `if not students`.

Your solution should combine everything learned so far:

**Creating Sets → Adding Elements → Removing Elements → `in` → `not in` → `len()` → Empty Set Checks → Boolean Conditions**

---

# Sets — Part 7: Iterating Through Sets

In the previous part, we learned how to use `len()` to count the number of elements in a Set.

Now we will learn how to **iterate through the elements of a Set**.

Iteration means going through the elements of a collection one by one.

The main tool we will use is the `for` loop.

---

## 1. Basic `for` Loop with a Set

We can use a `for` loop to access each element of a Set:

```python
fruits = {"apple", "banana", "orange"}

for fruit in fruits:
    print(fruit)
```

The output may be:

```text
apple
orange
banana
```

The exact order is not guaranteed.

This is important because **Sets are unordered collections**.

---

## 2. Understanding the Loop

Consider:

```python
numbers = {10, 20, 30}

for number in numbers:
    print(number)
```

The loop works conceptually like this:

```text
Take an element
↓
Store it temporarily in `number`
↓
Run the code inside the loop
↓
Move to another element
↓
Repeat until all elements have been processed
```

The variable name can be anything:

```python
for number in numbers:
    print(number)
```

or:

```python
for item in numbers:
    print(item)
```

Both are valid.

---

## 3. Printing Each Element

A simple use of iteration is printing every element:

```python
languages = {"Python", "Java", "C++"}

for language in languages:
    print(language)
```

Each element is processed once during that iteration.

However, because a Set has no guaranteed order, you should not rely on the output order.

---

## 4. Performing an Operation on Each Element

Iteration is not only for printing.

We can perform an operation on every element.

For example:

```python
numbers = {1, 2, 3, 4}

for number in numbers:
    print(number * 2)
```

Possible output:

```text
2
4
6
8
```

The operation is performed separately for each element.

---

## 5. Using `if` Inside a Set Loop

We can combine iteration with conditions.

```python
numbers = {1, 2, 3, 4, 5, 6}

for number in numbers:
    if number % 2 == 0:
        print(number)
```

Output:

```text
2
4
6
```

The loop visits every element, while the `if` statement selects only the even numbers.

---

## 6. Finding Specific Elements

We can use iteration to search through a Set.

```python
names = {"Ali", "Sara", "Reza", "Mina"}

for name in names:
    if name.startswith("A"):
        print(name)
```

Possible output:

```text
Ali
```

For simple membership checks, `in` is usually easier:

```python
if "Ali" in names:
    print("Found")
```

But iteration is useful when we want to **inspect or process every element**.

---

## 7. Counting Elements During Iteration

We can create a counter:

```python
numbers = {10, 20, 30, 40}

count = 0

for number in numbers:
    count += 1

print(count)
```

Output:

```text
4
```

This works, although when we only need the number of elements, `len()` is simpler:

```python
print(len(numbers))
```

Iteration becomes useful when we need to count elements that satisfy a condition.

For example:

```python
numbers = {1, 2, 3, 4, 5, 6}

even_count = 0

for number in numbers:
    if number % 2 == 0:
        even_count += 1

print(even_count)
```

Output:

```text
3
```

---

## 8. Building a New Set While Iterating

We can create another Set based on the elements of the first Set.

```python
numbers = {1, 2, 3, 4, 5, 6}

even_numbers = set()

for number in numbers:
    if number % 2 == 0:
        even_numbers.add(number)

print(even_numbers)
```

Result:

```text
{2, 4, 6}
```

This is an important pattern:

```text
Original Set
↓
for loop
↓
condition
↓
New Set
```

---

## 9. Iterating Through a Set of Strings

Iteration also works naturally with Strings.

```python
languages = {"Python", "Java", "JavaScript"}

for language in languages:
    print("I know", language)
```

Possible output:

```text
I know Python
I know Java
I know JavaScript
```

Again, the order may differ.

---

## 10. Iterating Through a Set of Tuples

Tuples can be elements of a Set because tuples are hashable when their contents are hashable.

For example:

```python
points = {(1, 2), (3, 4), (5, 6)}

for point in points:
    print(point)
```

Possible output:

```text
(1, 2)
(3, 4)
(5, 6)
```

We can also unpack each Tuple:

```python
points = {(1, 2), (3, 4), (5, 6)}

for x, y in points:
    print("x =", x, "y =", y)
```

Possible output:

```text
x = 1 y = 2
x = 3 y = 4
x = 5 y = 6
```

---

## 11. Using `break`

We can stop a loop early with `break`.

```python
numbers = {1, 2, 3, 4, 5}

for number in numbers:
    if number == 3:
        break

    print(number)
```

The exact output order can vary because the Set is unordered.

The important idea is that once the condition becomes true, `break` immediately stops the loop.

---

## 12. Using `continue`

`continue` skips the current iteration and moves to the next one.

```python
numbers = {1, 2, 3, 4, 5}

for number in numbers:
    if number % 2 == 0:
        continue

    print(number)
```

The output contains only odd numbers:

```text
1
3
5
```

The exact order may differ.

---

## 13. Iterating and Checking Membership

We can combine iteration with `in`.

For example:

```python
numbers = {1, 2, 3, 4, 5}

for number in numbers:
    if number in {2, 4}:
        print(number)
```

Output:

```text
2
4
```

However, if the goal is simply to find whether a value exists, direct membership checking is usually better:

```python
if 2 in numbers:
    print("Found")
```

Iteration is most useful when we need to process multiple elements.

---

## 14. Do Not Modify a Set While Iterating Over It

One of the most important rules is:

> Do not change the size of a Set while iterating over that same Set.

For example, this can cause an error:

```python
numbers = {1, 2, 3, 4}

for number in numbers:
    if number % 2 == 0:
        numbers.remove(number)
```

Python can raise:

```text
RuntimeError: Set changed size during iteration
```

Why?

Because the loop is currently going through the Set while we are simultaneously removing elements from it.

---

## 15. Safe Way to Remove Elements While Iterating

If we need to remove elements based on a condition, we can iterate over a copy:

```python
numbers = {1, 2, 3, 4}

for number in numbers.copy():
    if number % 2 == 0:
        numbers.remove(number)

print(numbers)
```

Result:

```text
{1, 3}
```

Here:

```python
numbers.copy()
```

creates a separate Set for the loop.

The original Set can then be modified safely.

---

## 16. Another Safe Approach: Build a New Set

Often, an even cleaner approach is to build a new Set.

```python
numbers = {1, 2, 3, 4}

odd_numbers = set()

for number in numbers:
    if number % 2 != 0:
        odd_numbers.add(number)

print(odd_numbers)
```

Result:

```text
{1, 3}
```

This approach avoids modifying the original Set during iteration.

---

## 17. Iterating Through an Empty Set

If a Set is empty:

```python
numbers = set()

for number in numbers:
    print(number)
```

Nothing is printed.

The loop simply runs zero times.

This is one reason why `for` loops work naturally with collections.

---

## 18. Using `for` with `len()`

We can combine `len()` with iteration.

```python
students = {"Ali", "Sara", "Reza"}

print("Number of students:", len(students))

for student in students:
    print(student)
```

Possible output:

```text
Number of students: 3
Ali
Sara
Reza
```

The number is reliable, but the Set iteration order is not guaranteed.

---

## 19. Sorting a Set Before Iterating

If we need a predictable order, we can use `sorted()`.

```python
numbers = {5, 2, 8, 1, 3}

for number in sorted(numbers):
    print(number)
```

Output:

```text
1
2
3
5
8
```

Notice that `sorted()` does **not** turn the Set itself into an ordered Set.

Instead, it returns a sorted List that we iterate over.

Conceptually:

```text
Set
↓
sorted()
↓
List
↓
for loop
```

---

## 20. Iterating in Reverse Order

If the elements can be sorted, we can also iterate in reverse:

```python
numbers = {5, 2, 8, 1, 3}

for number in sorted(numbers, reverse=True):
    print(number)
```

Output:

```text
8
5
3
2
1
```

This is useful when we need a predictable descending order.

---

## Common Beginner Mistakes

### Mistake 1 — Assuming Set order

Do not write code that depends on:

```text
first element
second element
third element
```

because Sets do not provide a guaranteed ordering.

---

### Mistake 2 — Trying to access a Set by index

This does not work:

```python
numbers = {10, 20, 30}

print(numbers[0])
```

Sets do not support indexing.

Use iteration:

```python
for number in numbers:
    print(number)
```

---

### Mistake 3 — Modifying the Set During Iteration

Avoid:

```python
for number in numbers:
    numbers.remove(number)
```

Use a copy or create a new Set instead.

---

### Mistake 4 — Using iteration when `in` is enough

If you only want to know whether an element exists:

```python
if 10 in numbers:
    print("Found")
```

is simpler than looping through every element.

---

## Key Takeaways

After this part, you should know:

1. A `for` loop can iterate through a Set.
2. Each iteration processes one element.
3. Set iteration order is not guaranteed.
4. `if`, `break`, and `continue` can be used inside a Set loop.
5. We can create counters while iterating.
6. We can build new Sets while iterating.
7. We should not modify a Set's size while iterating over it.
8. `copy()` can be used when we need to modify the original Set during iteration.
9. `sorted()` can provide predictable iteration order.
10. `in` is usually better than iteration when we only need a membership check.

---

## Exercises

### Question 1

What does this code do?

```python
numbers = {1, 2, 3, 4, 5, 6}

for number in numbers:
    if number % 2 == 0:
        print(number)
```

Which elements can be printed?

---

### Question 2

Write a program that takes:

```python
numbers = {1, 2, 3, 4, 5, 6, 7, 8}
```

and creates a new Set containing only numbers greater than `5`.

---

### Question 3

Why can this code cause a `RuntimeError`?

```python
numbers = {1, 2, 3, 4}

for number in numbers:
    numbers.remove(number)
```

How can you modify the program so that the removal is safe?

---

## Comprehensive Set Question

Create a program that starts with:

```python
students = {"Ali", "Sara", "Reza", "Mina", "Hassan"}
```

Your program should:

1. Iterate through the Set.
2. Print only students whose names start with `"A"` or `"M"`.
3. Count how many such students exist.
4. Create a new Set containing those students.
5. Print the number of students using `len()`.
6. Check whether `"Ali"` exists using `in`.
7. Demonstrate why modifying the original Set directly during iteration is unsafe.
8. Use a safe approach to remove the selected students from the original Set.
9. Print the final Set.

Your solution should combine:

**Creating Sets → Adding Elements → Removing Elements → `in` → `not in` → `len()` → `for` → `if` → `break` / `continue` → Set Copy → New Sets**

---

# Sets — Part 8: Set Union

In the previous part, we learned how to iterate through Sets using `for`.

Now we will start learning one of the most important features of Sets: **Set Operations**.

The first operation is **Union**.

Union allows us to combine the elements of two or more Sets while automatically removing duplicates.

---

## 1. What Is Set Union?

The **Union** of two Sets contains all unique elements that exist in either Set.

For example:

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}
```

The Union is:

```text
{1, 2, 3, 4, 5}
```

Notice that `3` appears in both Sets, but it appears only once in the result.

Conceptually:

```text
Set A      Set B
  ↓          ↓
{1,2,3} + {3,4,5}
       ↓
{1,2,3,4,5}
```

---

## 2. Using the `|` Operator

Python provides the `|` operator for Set Union.

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}

result = set_a | set_b

print(result)
```

Output:

```text
{1, 2, 3, 4, 5}
```

The syntax is:

```python
set_a | set_b
```

This means:

> Return all unique elements from `set_a` and `set_b`.

---

## 3. Using the `union()` Method

We can also use the `union()` method.

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}

result = set_a.union(set_b)

print(result)
```

Output:

```text
{1, 2, 3, 4, 5}
```

So there are two common ways to perform Union:

```python
set_a | set_b
```

and:

```python
set_a.union(set_b)
```

Both produce the same Set.

---

## 4. Union Does Not Modify the Original Sets

When we create a Union, the original Sets remain unchanged.

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}

result = set_a.union(set_b)

print(set_a)
print(set_b)
print(result)
```

Output:

```text
{1, 2, 3}
{3, 4, 5}
{1, 2, 3, 4, 5}
```

The Union creates a new Set.

---

## 5. Union with No Common Elements

If two Sets have no common elements:

```python
set_a = {1, 2, 3}
set_b = {4, 5, 6}

print(set_a | set_b)
```

Output:

```text
{1, 2, 3, 4, 5, 6}
```

Since there are no duplicates, all elements are included.

---

## 6. Union with Identical Sets

If two Sets contain exactly the same elements:

```python
set_a = {1, 2, 3}
set_b = {1, 2, 3}

print(set_a | set_b)
```

Output:

```text
{1, 2, 3}
```

The result still contains each element only once.

---

## 7. Union of More Than Two Sets

The `union()` method can work with multiple Sets.

```python
set_a = {1, 2}
set_b = {2, 3}
set_c = {3, 4}

result = set_a.union(set_b, set_c)

print(result)
```

Output:

```text
{1, 2, 3, 4}
```

We can also chain the `|` operator:

```python
result = set_a | set_b | set_c

print(result)
```

The result is the same:

```text
{1, 2, 3, 4}
```

---

## 8. Union with Strings

Union is not limited to numbers.

```python
languages_a = {"Python", "Java", "C++"}
languages_b = {"Python", "Go", "Rust"}

all_languages = languages_a | languages_b

print(all_languages)
```

The result contains every unique language:

```text
{"Python", "Java", "C++", "Go", "Rust"}
```

`Python` appears in both Sets but only once in the Union.

---

## 9. A Real-World Example

Imagine two groups of students.

```python
morning_students = {"Ali", "Sara", "Reza"}
evening_students = {"Reza", "Mina", "Hassan"}
```

We want to know all students who attend either group.

```python
all_students = morning_students | evening_students

print(all_students)
```

Result:

```text
{"Ali", "Sara", "Reza", "Mina", "Hassan"}
```

This is a practical use of Union.

---

## 10. Union and `len()`

We can combine Union with `len()` to count the total number of unique elements.

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}

total_unique = len(set_a | set_b)

print(total_unique)
```

Output:

```text
5
```

This tells us there are five unique elements across both Sets.

---

## 11. Union and Iteration

We can also iterate through the result of a Union.

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}

for number in set_a | set_b:
    print(number)
```

Possible output:

```text
1
2
3
4
5
```

Remember that the order is not guaranteed.

If we need sorted output:

```python
for number in sorted(set_a | set_b):
    print(number)
```

Output:

```text
1
2
3
4
5
```

---

## 12. Union with an Empty Set

The Union of a Set with an Empty Set returns the original elements.

```python
numbers = {1, 2, 3}
empty = set()

print(numbers | empty)
```

Output:

```text
{1, 2, 3}
```

Conceptually:

```text
Set ∪ Empty Set = Set
```

---

## 13. Union Is Commutative

Union has an important mathematical property:

```text
A ∪ B = B ∪ A
```

In Python:

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}

print(set_a | set_b)
print(set_b | set_a)
```

Both results contain:

```text
{1, 2, 3, 4, 5}
```

So changing the order of the two Sets does not change the resulting Set.

---

## 14. Union Is Associative

Union is also associative:

```text
(A ∪ B) ∪ C = A ∪ (B ∪ C)
```

In Python:

```python
a = {1, 2}
b = {2, 3}
c = {3, 4}

result_1 = (a | b) | c
result_2 = a | (b | c)

print(result_1)
print(result_2)
```

Both produce:

```text
{1, 2, 3, 4}
```

This means we can group Union operations in different ways without changing the final Set.

---

## 15. Union with User Input

We can also use Sets created from user input.

For example:

```python
first = input("Enter names separated by spaces: ").split()
second = input("Enter more names separated by spaces: ").split()

set_a = set(first)
set_b = set(second)

all_names = set_a | set_b

print(all_names)
```

If the user enters:

```text
Ali Sara Reza
Reza Mina Hassan
```

the result contains:

```text
{"Ali", "Sara", "Reza", "Mina", "Hassan"}
```

The duplicate `Reza` is automatically removed.

---

## 16. Union with a List

The `|` operator requires Sets.

This works:

```python
a = {1, 2, 3}
b = {3, 4, 5}

print(a | b)
```

But this does not:

```python
a = {1, 2, 3}
b = [3, 4, 5]

print(a | b)
```

Python raises a `TypeError`.

If we want to use a List, convert it to a Set first:

```python
b = set([3, 4, 5])

print(a | b)
```

---

## 17. Union and the `union()` Method with Other Iterables

The `union()` method is more flexible.

For example:

```python
numbers = {1, 2, 3}

result = numbers.union([3, 4, 5])

print(result)
```

Output:

```text
{1, 2, 3, 4, 5}
```

It can also work with other iterable objects:

```python
numbers = {1, 2, 3}

result = numbers.union((3, 4, 5))

print(result)
```

Output:

```text
{1, 2, 3, 4, 5}
```

So remember:

```text
| operator
→ expects Set operands

union()
→ can accept other iterable objects
```

---

## 18. Common Beginner Mistakes

### Mistake 1 — Thinking Union keeps duplicates

```python
a = {1, 2, 3}
b = {3, 4}

print(a | b)
```

The result is:

```text
{1, 2, 3, 4}
```

not:

```text
{1, 2, 3, 3, 4}
```

Sets automatically eliminate duplicates.

---

### Mistake 2 — Confusing Union with Addition

This is not valid:

```python
a + b
```

Sets are not combined using `+`.

Use:

```python
a | b
```

or:

```python
a.union(b)
```

---

### Mistake 3 — Expecting the Original Set to Change

This:

```python
a | b
```

does not modify `a`.

If you want to store the result:

```python
result = a | b
```

If you want to update a Set in place, we will later learn about `update()`.

---

### Mistake 4 — Assuming Union Has a Fixed Order

Do not expect:

```python
{1, 2, 3, 4}
```

to always be displayed in that exact order.

If predictable ordering is needed:

```python
sorted(a | b)
```

---

## Key Takeaways

After this part, you should know:

1. Union combines all unique elements from two or more Sets.
2. The `|` operator performs Set Union.
3. The `union()` method also performs Union.
4. Union automatically removes duplicates.
5. Union does not modify the original Sets.
6. Union can be used with multiple Sets.
7. `len()` can count the unique elements in a Union.
8. We can iterate through a Union using `for`.
9. `sorted()` can provide predictable output order.
10. The `|` operator expects Set operands.
11. `union()` can accept other iterable objects.
12. Union is commutative and associative.

---

## Exercises

### Question 1

What will this code print?

```python
a = {1, 2, 3}
b = {3, 4, 5}

print(a | b)
```

Why does `3` appear only once?

---

### Question 2

Write a program that combines these two Sets:

```python
python_students = {"Ali", "Sara", "Reza"}
java_students = {"Reza", "Mina", "Hassan"}
```

Then print:

1. All unique students.
2. The number of unique students.

---

### Question 3

What is the difference between:

```python
a | b
```

and:

```python
a.union(b)
```

Also explain why this works:

```python
a.union([3, 4, 5])
```

but this does not:

```python
a | [3, 4, 5]
```

---

## Comprehensive Set Question

Create a program for two groups of students:

```python
morning_students = {"Ali", "Sara", "Reza", "Mina"}
evening_students = {"Reza", "Hassan", "Mina", "Nima"}
```

Your program should:

1. Create a Union containing all unique students.
2. Print the resulting Set.
3. Print the number of unique students using `len()`.
4. Iterate through the Union and print every student.
5. Print the students in alphabetical order using `sorted()`.
6. Ask the user for another student name.
7. Add that student to the appropriate Set.
8. Create the Union again.
9. Print the final unique student count.

This exercise should combine:

**Creating Sets → Adding Elements → `in` → `len()` → Iteration → `sorted()` → Set Union**

---

# Sets — Part 9: Set Intersection

In the previous part, we learned about **Set Union**, which combines all unique elements from two or more Sets.

Now we will learn another important Set operation:

**Set Intersection**

Intersection allows us to find the elements that are **common to two or more Sets**.

---

## 1. What Is Set Intersection?

The **Intersection** of two Sets contains only the elements that exist in **both Sets**.

For example:

```python
set_a = {1, 2, 3, 4}
set_b = {3, 4, 5, 6}

result = set_a & set_b

print(result)
```

Output:

```text
{3, 4}
```

Why?

Because:

```text
Set A → {1, 2, 3, 4}
Set B → {3, 4, 5, 6}
              ↑  ↑
            Common
```

Only `3` and `4` exist in both Sets.

---

## 2. Using the `&` Operator

Python provides the `&` operator for Set Intersection.

```python
set_a = {1, 2, 3}
set_b = {2, 3, 4}

result = set_a & set_b

print(result)
```

Output:

```text
{2, 3}
```

The syntax is:

```python
set_a & set_b
```

This means:

> Return the elements that exist in both Sets.

---

## 3. Using the `intersection()` Method

We can also use the `intersection()` method:

```python
set_a = {1, 2, 3}
set_b = {2, 3, 4}

result = set_a.intersection(set_b)

print(result)
```

Output:

```text
{2, 3}
```

So we have two common approaches:

```python
set_a & set_b
```

and:

```python
set_a.intersection(set_b)
```

Both return the common elements.

---

## 4. Intersection Does Not Modify the Original Sets

Just like Union, Intersection creates a new Set.

```python
set_a = {1, 2, 3}
set_b = {2, 3, 4}

result = set_a.intersection(set_b)

print(set_a)
print(set_b)
print(result)
```

Output:

```text
{1, 2, 3}
{2, 3, 4}
{2, 3}
```

The original Sets remain unchanged.

---

## 5. Sets With No Common Elements

If two Sets have no common elements:

```python
set_a = {1, 2, 3}
set_b = {4, 5, 6}

print(set_a & set_b)
```

Output:

```text
set()
```

The result is an **Empty Set**.

This means the Sets have no common elements.

---

## 6. Identical Sets

If two Sets are identical:

```python
set_a = {1, 2, 3}
set_b = {1, 2, 3}

print(set_a & set_b)
```

Output:

```text
{1, 2, 3}
```

Every element is common to both Sets.

---

## 7. Intersection With an Empty Set

The Intersection of any Set with an Empty Set is empty.

```python
numbers = {1, 2, 3}
empty = set()

print(numbers & empty)
```

Output:

```text
set()
```

Conceptually:

```text
Set ∩ Empty Set = Empty Set
```

---

## 8. Intersection of More Than Two Sets

We can find the common elements of multiple Sets.

```python
a = {1, 2, 3, 4}
b = {2, 3, 4, 5}
c = {3, 4, 5, 6}

result = a & b & c

print(result)
```

Output:

```text
{3, 4}
```

Only `3` and `4` exist in all three Sets.

We can also use the method:

```python
result = a.intersection(b, c)

print(result)
```

Output:

```text
{3, 4}
```

---

## 9. A Real-World Example

Suppose we have two groups of students.

```python
python_students = {"Ali", "Sara", "Reza", "Mina"}
java_students = {"Reza", "Mina", "Hassan", "Nima"}
```

We want to find students who study **both Python and Java**.

```python
both = python_students & java_students

print(both)
```

Output:

```text
{"Reza", "Mina"}
```

These students are common to both groups.

---

## 10. Finding Common Skills

Intersection is also useful for comparing skills.

```python
skills_a = {"Python", "Git", "SQL", "Linux"}
skills_b = {"Python", "Docker", "Linux", "Java"}

common_skills = skills_a & skills_b

print(common_skills)
```

Output:

```text
{"Python", "Linux"}
```

The Intersection tells us which skills are shared.

---

## 11. Intersection and `len()`

We can combine Intersection with `len()`.

```python
a = {1, 2, 3, 4}
b = {3, 4, 5, 6}

common_count = len(a & b)

print(common_count)
```

Output:

```text
2
```

There are two common elements.

This is useful when we care about the **number of shared elements**, not the elements themselves.

---

## 12. Intersection and Iteration

We can iterate through the Intersection:

```python
a = {1, 2, 3, 4}
b = {3, 4, 5, 6}

for number in a & b:
    print(number)
```

Possible output:

```text
3
4
```

Remember that Set order is not guaranteed.

For predictable output:

```python
for number in sorted(a & b):
    print(number)
```

Output:

```text
3
4
```

---

## 13. Intersection and Membership Checking

We can combine Intersection with `in`:

```python
a = {1, 2, 3}
b = {2, 3, 4}

common = a & b

if 2 in common:
    print("2 is common")
```

Output:

```text
2 is common
```

However, if we only want to check whether a particular element exists in both Sets, we can avoid creating another Set:

```python
if 2 in a and 2 in b:
    print("2 is common")
```

This can be simpler for a single value.

---

## 14. Intersection With Lists Using `intersection()`

The `&` operator requires Set operands.

For example, this does not work:

```python
a = {1, 2, 3}
b = [2, 3, 4]

print(a & b)
```

Python raises a `TypeError`.

But `intersection()` can accept an iterable:

```python
a = {1, 2, 3}

result = a.intersection([2, 3, 4])

print(result)
```

Output:

```text
{2, 3}
```

So remember:

```text
& operator
→ requires Set operands

intersection()
→ can accept iterable objects
```

---

## 15. Intersection and User Input

We can use Intersection with data entered by the user.

```python
first = input("Enter names: ").split()
second = input("Enter more names: ").split()

set_a = set(first)
set_b = set(second)

common_names = set_a & set_b

print("Common names:", common_names)
```

If the user enters:

```text
Ali Sara Reza Mina
```

and:

```text
Reza Mina Hassan
```

the result is:

```text
Common names: {'Reza', 'Mina'}
```

The Set automatically removes duplicate values.

---

## 16. Mathematical Properties of Intersection

Intersection has important mathematical properties.

### Commutative Property

```text
A ∩ B = B ∩ A
```

In Python:

```python
a = {1, 2, 3}
b = {2, 3, 4}

print(a & b)
print(b & a)
```

Both produce:

```text
{2, 3}
```

Changing the order does not change the result.

### Associative Property

Intersection is also associative:

```text
(A ∩ B) ∩ C = A ∩ (B ∩ C)
```

For example:

```python
a = {1, 2, 3}
b = {2, 3, 4}
c = {2, 3, 5}

result_1 = (a & b) & c
result_2 = a & (b & c)

print(result_1)
print(result_2)
```

Both produce:

```text
{2, 3}
```

---

## 17. Relationship Between Union and Intersection

Union and Intersection are complementary Set operations.

Consider:

```python
a = {1, 2, 3}
b = {3, 4, 5}
```

Union:

```python
a | b
```

gives:

```text
{1, 2, 3, 4, 5}
```

Intersection:

```python
a & b
```

gives:

```text
{3}
```

So:

```text
Union
→ Everything from both Sets

Intersection
→ Only what both Sets share
```

A useful way to remember them:

```text
A | B
→ "A OR B"

A & B
→ "A AND B"
```

---

## 18. Common Beginner Mistakes

### Mistake 1 — Confusing Intersection With Union

If:

```python
a = {1, 2, 3}
b = {3, 4, 5}
```

then:

```python
a | b
```

returns:

```text
{1, 2, 3, 4, 5}
```

while:

```python
a & b
```

returns:

```text
{3}
```

Remember:

```text
| → Union
& → Intersection
```

---

### Mistake 2 — Thinking Intersection Keeps All Elements

This:

```python
a & b
```

does not combine all elements.

It keeps only the elements shared by both Sets.

---

### Mistake 3 — Expecting the Original Set to Change

This:

```python
a & b
```

does not modify `a` or `b`.

If you want to save the result:

```python
common = a & b
```

---

### Mistake 4 — Using `&` With a List

This is invalid:

```python
a & [1, 2, 3]
```

Use:

```python
a.intersection([1, 2, 3])
```

instead.

---

### Mistake 5 — Forgetting That an Empty Result Is Still a Set

If there are no common elements:

```python
result = a & b
```

the result is:

```python
set()
```

not:

```python
{}
```

Remember:

```text
set()
→ Empty Set

{}
→ Empty Dictionary
```

---

## Key Takeaways

After this part, you should know:

1. Intersection returns elements common to two or more Sets.
2. The `&` operator performs Intersection.
3. The `intersection()` method also performs Intersection.
4. Intersection automatically removes duplicates.
5. Intersection does not modify the original Sets.
6. Two Sets with no common elements produce an Empty Set.
7. `len()` can count the number of common elements.
8. We can iterate through an Intersection using `for`.
9. `sorted()` can provide predictable output order.
10. `&` requires Set operands.
11. `intersection()` can accept iterable objects.
12. Intersection is commutative and associative.
13. `|` can be remembered as **OR**, while `&` can be remembered as **AND**.

---

## Exercises

### Question 1

What will this code print?

```python
a = {1, 2, 3, 4}
b = {3, 4, 5, 6}

print(a & b)
```

Why?

---

### Question 2

Write a program that finds the students who study both Python and Java:

```python
python_students = {"Ali", "Sara", "Reza", "Mina"}
java_students = {"Reza", "Mina", "Hassan", "Nima"}
```

Then print the number of students who study both languages.

---

### Question 3

Explain the difference between:

```python
a | b
```

and:

```python
a & b
```

Use your own example.

---

## Comprehensive Set Question

Create a program using:

```python
python_students = {"Ali", "Sara", "Reza", "Mina", "Hassan"}
java_students = {"Reza", "Mina", "Hassan", "Nima"}
web_students = {"Mina", "Hassan", "Nima", "Omid"}
```

Your program should:

1. Find all students using Union.
2. Find students who study both Python and Java.
3. Find students who study all three subjects.
4. Print the number of students in each result using `len()`.
5. Iterate through each result.
6. Print each result in sorted order.
7. Ask the user for a student name.
8. Check whether the student studies both Python and Java.
9. Explain the difference between the Union and Intersection results.

This exercise should combine:

**Creating Sets → `in` → `len()` → Iteration → `sorted()` → Union → Intersection**

---

# Sets — Part 10: Set Difference

In the previous part, we learned about **Set Intersection**, which finds the elements that two or more Sets have in common.

Now we will learn another important Set operation:

**Set Difference**

Set Difference allows us to find the elements that exist in one Set but **do not exist in another Set**.

---

## 1. What Is Set Difference?

Suppose we have:

```python
set_a = {1, 2, 3, 4}
set_b = {3, 4, 5, 6}
```

If we calculate the difference of `set_a` from `set_b`:

```python
result = set_a - set_b

print(result)
```

Output:

```text
{1, 2}
```

Why?

Because `1` and `2` exist in `set_a`, but they do not exist in `set_b`.

Conceptually:

```text
Set A → {1, 2, 3, 4}
Set B → {3, 4, 5, 6}

A - B → {1, 2}
```

---

## 2. Using the `-` Operator

Python provides the `-` operator for Set Difference.

```python
set_a = {1, 2, 3}
set_b = {2, 3, 4}

result = set_a - set_b

print(result)
```

Output:

```text
{1}
```

The syntax is:

```python
set_a - set_b
```

This means:

> Return the elements that are in `set_a` but not in `set_b`.

---

## 3. Difference Is Directional

This is one of the most important things to understand about Set Difference.

Consider:

```python
a = {1, 2, 3}
b = {2, 3, 4}
```

Then:

```python
print(a - b)
```

gives:

```text
{1}
```

But:

```python
print(b - a)
```

gives:

```text
{4}
```

So:

```text
A - B ≠ B - A
```

Unlike Union and Intersection, Difference is **not commutative**.

The order matters.

---

## 4. Using the `difference()` Method

We can also use the `difference()` method:

```python
a = {1, 2, 3}
b = {2, 3, 4}

result = a.difference(b)

print(result)
```

Output:

```text
{1}
```

So we have two common approaches:

```python
a - b
```

and:

```python
a.difference(b)
```

Both return the elements that are in `a` but not in `b`.

---

## 5. Difference Does Not Modify the Original Set

Set Difference creates a new Set.

```python
a = {1, 2, 3}
b = {2, 3, 4}

result = a - b

print(a)
print(b)
print(result)
```

Output:

```text
{1, 2, 3}
{2, 3, 4}
{1}
```

The original Sets remain unchanged.

---

## 6. Difference With No Common Elements

If the two Sets have no common elements:

```python
a = {1, 2, 3}
b = {4, 5, 6}

print(a - b)
```

Output:

```text
{1, 2, 3}
```

Since none of the elements in `a` exist in `b`, all elements of `a` remain.

But:

```python
print(b - a)
```

also gives:

```text
{4, 5, 6}
```

---

## 7. Difference Between Identical Sets

If two Sets are identical:

```python
a = {1, 2, 3}
b = {1, 2, 3}

print(a - b)
```

Output:

```text
set()
```

There are no elements in `a` that are missing from `b`.

The reverse is also empty:

```python
print(b - a)
```

Output:

```text
set()
```

---

## 8. Difference With an Empty Set

If we subtract an Empty Set from another Set:

```python
numbers = {1, 2, 3}
empty = set()

print(numbers - empty)
```

Output:

```text
{1, 2, 3}
```

Nothing is removed.

Conceptually:

```text
A - ∅ = A
```

But the reverse is different:

```python
print(empty - numbers)
```

Output:

```text
set()
```

---

## 9. Difference of Multiple Sets

We can apply Difference multiple times.

```python
a = {1, 2, 3, 4, 5}
b = {2, 3}
c = {4}

result = a - b - c

print(result)
```

Output:

```text
{1, 5}
```

The operation is evaluated from left to right:

```text
a - b
→ {1, 4, 5}

{1, 4, 5} - c
→ {1, 5}
```

---

## 10. Difference With `difference()`

The `difference()` method can also receive multiple Sets:

```python
a = {1, 2, 3, 4, 5}
b = {2, 3}
c = {4}

result = a.difference(b, c)

print(result)
```

Output:

```text
{1, 5}
```

This is equivalent to:

```python
a - b - c
```

---

## 11. A Real-World Example

Suppose we have students enrolled in Python and Java:

```python
python_students = {"Ali", "Sara", "Reza", "Mina"}
java_students = {"Reza", "Mina", "Hassan", "Nima"}
```

We want to find students who study **Python but not Java**:

```python
python_only = python_students - java_students

print(python_only)
```

Output:

```text
{"Ali", "Sara"}
```

We can also find students who study **Java but not Python**:

```python
java_only = java_students - python_students

print(java_only)
```

Output:

```text
{"Hassan", "Nima"}
```

This is a very common practical use of Set Difference.

---

## 12. Difference and `len()`

We can combine Difference with `len()`:

```python
a = {1, 2, 3, 4}
b = {3, 4, 5}

count = len(a - b)

print(count)
```

Output:

```text
2
```

There are two elements that belong to `a` but not to `b`.

---

## 13. Difference and Iteration

We can iterate through a Difference result:

```python
a = {1, 2, 3, 4}
b = {3, 4, 5}

for number in a - b:
    print(number)
```

Possible output:

```text
1
2
```

If we want predictable ordering:

```python
for number in sorted(a - b):
    print(number)
```

Output:

```text
1
2
```

---

## 14. Difference and Membership Checking

We can use `in` with Difference:

```python
a = {1, 2, 3}
b = {2, 3, 4}

difference = a - b

if 1 in difference:
    print("1 exists only in A")
```

Output:

```text
1 exists only in A
```

For a single value, we can also directly check:

```python
if 1 in a and 1 not in b:
    print("1 exists only in A")
```

This avoids creating another Set when we only need to check one element.

---

## 15. Difference With Lists

The `-` operator requires Set operands.

This does not work:

```python
a = {1, 2, 3}
b = [2, 3]

print(a - b)
```

Python raises a `TypeError`.

But `difference()` can accept an iterable:

```python
a = {1, 2, 3}

result = a.difference([2, 3])

print(result)
```

Output:

```text
{1}
```

So remember:

```text
- operator
→ requires Set operands

difference()
→ can accept iterable objects
```

---

## 16. Difference vs Intersection

It is important not to confuse Difference and Intersection.

Suppose:

```python
a = {1, 2, 3, 4}
b = {3, 4, 5, 6}
```

Intersection:

```python
a & b
```

returns:

```text
{3, 4}
```

These are the elements **shared by both Sets**.

Difference:

```python
a - b
```

returns:

```text
{1, 2}
```

These are the elements that exist in `a` but **not** in `b`.

Remember:

```text
A & B
→ Common elements

A - B
→ Elements only in A
```

---

## 17. Difference vs Union

Union gives us everything from both Sets:

```python
a | b
```

Difference gives us only what is unique to the left-hand Set:

```python
a - b
```

For example:

```python
a = {1, 2, 3}
b = {3, 4, 5}
```

Union:

```text
{1, 2, 3, 4, 5}
```

Difference:

```text
{1, 2}
```

So:

```text
| → Combine

& → Common

- → Only on the left
```

---

## 18. Common Beginner Mistakes

### Mistake 1 — Assuming Difference Is Commutative

This is incorrect:

```text
A - B = B - A
```

For example:

```python
a = {1, 2, 3}
b = {2, 3, 4}

print(a - b)
print(b - a)
```

Output:

```text
{1}
{4}
```

The results are different.

---

### Mistake 2 — Forgetting That the Left Set Matters

When you write:

```python
a - b
```

Python starts with `a` and removes elements that also exist in `b`.

It does **not** mean "find elements that are different between the Sets."

That operation is called **Symmetric Difference**, which we will learn separately.

---

### Mistake 3 — Expecting the Original Set to Change

This:

```python
a - b
```

does not modify `a`.

To store the result:

```python
result = a - b
```

---

### Mistake 4 — Confusing `{}` With `set()`

An empty Difference returns:

```python
set()
```

not:

```python
{}
```

Remember:

```text
set()
→ Empty Set

{}
→ Empty Dictionary
```

---

## Key Takeaways

After this part, you should know:

1. Set Difference finds elements in one Set that are not in another Set.
2. The `-` operator performs Difference.
3. The `difference()` method also performs Difference.
4. Difference is directional.
5. `A - B` is generally different from `B - A`.
6. Difference does not modify the original Sets.
7. Difference with an Empty Set returns the original Set.
8. Difference between identical Sets returns an Empty Set.
9. `len()` can count the elements in the Difference.
10. We can iterate through a Difference result.
11. `sorted()` can provide predictable ordering.
12. The `-` operator requires Set operands.
13. `difference()` can accept iterable objects.
14. Difference is different from Intersection and Union.

---

## Exercises

### Question 1

What will this code print?

```python
a = {1, 2, 3, 4}
b = {3, 4, 5, 6}

print(a - b)
print(b - a)
```

Why are the two results different?

---

### Question 2

Write a program that finds:

* students who study Python but not Java
* students who study Java but not Python

Use:

```python
python_students = {"Ali", "Sara", "Reza", "Mina"}
java_students = {"Reza", "Mina", "Hassan", "Nima"}
```

---

### Question 3

Explain the difference between:

```python
a | b
a & b
a - b
```

Give a simple example for each one.

---

## Comprehensive Set Question

Create a program using:

```python
python_students = {"Ali", "Sara", "Reza", "Mina", "Hassan"}
java_students = {"Reza", "Mina", "Hassan", "Nima"}
web_students = {"Mina", "Hassan", "Nima", "Omid"}
```

Your program should:

1. Find all students using Union.
2. Find students who study both Python and Java.
3. Find students who study Python but not Java.
4. Find students who study Java but not Python.
5. Find students who study Python but not Web.
6. Print the number of students in each result using `len()`.
7. Iterate through the Difference results.
8. Print the results using `sorted()`.
9. Ask the user for a student name.
10. Check whether that student belongs only to the Python group.

This exercise should combine:

**Creating Sets → `in` → `len()` → Iteration → `sorted()` → Union → Intersection → Difference**

---

# Sets — Part 11: Set Symmetric Difference

In the previous part, we learned about **Set Difference**, which finds the elements that exist in one Set but not another.

Now we will learn:

**Set Symmetric Difference**

Symmetric Difference finds the elements that belong to **either Set, but not to both Sets**.

---

## 1. What Is Symmetric Difference?

Suppose we have:

```python
a = {1, 2, 3, 4}
b = {3, 4, 5, 6}
```

The common elements are:

```text
{3, 4}
```

Symmetric Difference removes those common elements and keeps everything else:

```python
result = a ^ b

print(result)
```

Output:

```text
{1, 2, 5, 6}
```

So:

```text
A → {1, 2, 3, 4}
B → {3, 4, 5, 6}

Common → {3, 4}

Symmetric Difference → {1, 2, 5, 6}
```

A simple way to remember it:

```text
Symmetric Difference
→ Everything that belongs to only one of the Sets
```

---

## 2. Using the `^` Operator

Python provides the `^` operator for Symmetric Difference.

```python
a = {1, 2, 3}
b = {2, 3, 4}

result = a ^ b

print(result)
```

Output:

```text
{1, 4}
```

The syntax is:

```python
a ^ b
```

It means:

> Return elements that are in `a` or `b`, but not in both.

---

## 3. Using the `symmetric_difference()` Method

We can also use the `symmetric_difference()` method:

```python
a = {1, 2, 3}
b = {2, 3, 4}

result = a.symmetric_difference(b)

print(result)
```

Output:

```text
{1, 4}
```

So we have two common approaches:

```python
a ^ b
```

and:

```python
a.symmetric_difference(b)
```

Both return the same result.

---

## 4. Symmetric Difference Is Commutative

Unlike normal Difference, Symmetric Difference does **not** depend on the order of the Sets.

For example:

```python
a = {1, 2, 3}
b = {2, 3, 4}

print(a ^ b)
print(b ^ a)
```

Both produce:

```text
{1, 4}
```

Therefore:

```text
A △ B = B △ A
```

This is called the **Commutative Property**.

Remember the contrast:

```text
A - B ≠ B - A

A ^ B = B ^ A
```

---

## 5. Symmetric Difference Does Not Modify the Original Sets

Just like the other Set operations we have learned, Symmetric Difference normally creates a new Set.

```python
a = {1, 2, 3}
b = {2, 3, 4}

result = a ^ b

print(a)
print(b)
print(result)
```

Output:

```text
{1, 2, 3}
{2, 3, 4}
{1, 4}
```

The original Sets remain unchanged.

---

## 6. Symmetric Difference of Identical Sets

If two Sets are identical:

```python
a = {1, 2, 3}
b = {1, 2, 3}

print(a ^ b)
```

Output:

```text
set()
```

Why?

Because every element exists in both Sets.

Symmetric Difference keeps only elements that exist in exactly one Set.

Since there are none, the result is empty.

---

## 7. Symmetric Difference With an Empty Set

If one Set is empty:

```python
a = {1, 2, 3}
empty = set()

print(a ^ empty)
```

Output:

```text
{1, 2, 3}
```

The original Set is returned.

Conceptually:

```text
A △ ∅ = A
```

This makes sense because every element of `A` belongs to exactly one of the two Sets.

---

## 8. Symmetric Difference With No Common Elements

If two Sets have no common elements:

```python
a = {1, 2, 3}
b = {4, 5, 6}

print(a ^ b)
```

Output:

```text
{1, 2, 3, 4, 5, 6}
```

Because nothing is shared, every element belongs to exactly one Set.

Therefore:

```text
No overlap
→ Symmetric Difference = Union
```

---

## 9. Symmetric Difference vs Difference

This is one of the most important comparisons.

Suppose:

```python
a = {1, 2, 3}
b = {2, 3, 4}
```

Normal Difference:

```python
print(a - b)
```

Output:

```text
{1}
```

It keeps only elements that belong to `a` and not `b`.

But:

```python
print(a ^ b)
```

Output:

```text
{1, 4}
```

It keeps elements that belong to **either Set but not both**.

So:

```text
A - B
→ Only A

A ^ B
→ Only A + Only B
```

---

## 10. Symmetric Difference vs Union

Union keeps everything:

```python
a | b
```

Symmetric Difference removes the common elements:

```python
a ^ b
```

Example:

```python
a = {1, 2, 3}
b = {2, 3, 4}
```

Union:

```text
{1, 2, 3, 4}
```

Symmetric Difference:

```text
{1, 4}
```

So:

```text
| → Everything

^ → Everything except the common elements
```

---

## 11. Symmetric Difference vs Intersection

Intersection returns only common elements:

```python
a & b
```

Symmetric Difference returns only non-common elements:

```python
a ^ b
```

For:

```python
a = {1, 2, 3}
b = {2, 3, 4}
```

we get:

```text
Intersection
→ {2, 3}

Symmetric Difference
→ {1, 4}
```

These operations can be viewed as opposites in terms of overlap:

```text
& → Common

^ → Not common
```

---

## 12. Symmetric Difference Using Union and Intersection

Symmetric Difference can also be understood using Union and Intersection.

The mathematical relationship is:

```text
A △ B = (A ∪ B) - (A ∩ B)
```

In Python:

```python
a = {1, 2, 3}
b = {2, 3, 4}

result = (a | b) - (a & b)

print(result)
```

Output:

```text
{1, 4}
```

This is exactly the same as:

```python
a ^ b
```

This relationship is useful because it connects the Set operations we have already learned.

---

## 13. Using `len()` With Symmetric Difference

We can count the number of non-common elements:

```python
a = {1, 2, 3, 4}
b = {3, 4, 5, 6}

count = len(a ^ b)

print(count)
```

Output:

```text
4
```

The four non-common elements are:

```text
{1, 2, 5, 6}
```

---

## 14. Iterating Through Symmetric Difference

We can iterate through the result:

```python
a = {1, 2, 3}
b = {2, 3, 4}

for number in a ^ b:
    print(number)
```

Possible output:

```text
1
4
```

For predictable ordering:

```python
for number in sorted(a ^ b):
    print(number)
```

Output:

```text
1
4
```

---

## 15. A Real-World Example

Suppose two groups of students attend different courses:

```python
python_students = {"Ali", "Sara", "Reza", "Mina"}
java_students = {"Reza", "Mina", "Hassan", "Nima"}
```

We want students who study **only one of the two courses**.

```python
only_one_course = python_students ^ java_students

print(only_one_course)
```

Output:

```text
{"Ali", "Sara", "Hassan", "Nima"}
```

`Reza` and `Mina` are excluded because they study both courses.

---

## 16. Finding Changed Members

Symmetric Difference can be useful for comparing two versions of data.

For example:

```python
old_members = {"Ali", "Sara", "Reza"}
new_members = {"Ali", "Reza", "Mina"}

changed = old_members ^ new_members

print(changed)
```

Output:

```text
{"Sara", "Mina"}
```

This tells us which members are different between the two versions.

It does not directly tell us who was removed and who was added, but it identifies all members whose membership changed.

---

## 17. Finding Differences Between Two Permissions Sets

Suppose two users have different permissions:

```python
user_a_permissions = {"read", "write", "delete"}
user_b_permissions = {"read", "write", "share"}
```

We can find permissions that are not shared:

```python
different_permissions = user_a_permissions ^ user_b_permissions

print(different_permissions)
```

Output:

```text
{"delete", "share"}
```

This can be useful when comparing configurations or permissions.

---

## 18. Common Beginner Mistakes

### Mistake 1 — Confusing `^` With `-`

These are different:

```python
a - b
```

and:

```python
a ^ b
```

For:

```python
a = {1, 2, 3}
b = {2, 3, 4}
```

we get:

```text
a - b
→ {1}

a ^ b
→ {1, 4}
```

Difference only looks from the left Set.

Symmetric Difference considers both Sets.

---

### Mistake 2 — Thinking `^` Means Intersection

Intersection uses:

```python
a & b
```

Symmetric Difference uses:

```python
a ^ b
```

Remember:

```text
& → Common

^ → Only one side
```

---

### Mistake 3 — Thinking Symmetric Difference Is Directional

Unlike normal Difference:

```text
A - B ≠ B - A
```

Symmetric Difference is commutative:

```text
A ^ B = B ^ A
```

---

### Mistake 4 — Forgetting the Common Elements Are Removed

If:

```python
a = {1, 2, 3}
b = {2, 3, 4}
```

then:

```python
a ^ b
```

does not return:

```text
{1, 2, 3, 4}
```

It returns:

```text
{1, 4}
```

because `2` and `3` are common.

---

## Key Takeaways

After this part, you should know:

1. Symmetric Difference returns elements that belong to only one of the Sets.
2. The `^` operator performs Symmetric Difference.
3. The `symmetric_difference()` method performs the same operation.
4. Symmetric Difference is commutative.
5. `A ^ B` is equal to `B ^ A`.
6. Identical Sets produce an Empty Set.
7. Symmetric Difference with an Empty Set returns the original Set.
8. If two Sets have no common elements, Symmetric Difference equals Union.
9. `len()` can count the non-common elements.
10. We can iterate through Symmetric Difference.
11. `sorted()` can give predictable output.
12. Symmetric Difference can be expressed as `(A | B) - (A & B)`.
13. Difference is directional, but Symmetric Difference is not.
14. `&` means common elements, while `^` means elements belonging to only one side.

---

## Exercises

### Question 1

What will this code print?

```python
a = {1, 2, 3, 4}
b = {3, 4, 5, 6}

print(a ^ b)
```

Explain why `3` and `4` are not in the result.

---

### Question 2

Write a program that finds students who study **exactly one** of Python or Java:

```python
python_students = {"Ali", "Sara", "Reza", "Mina"}
java_students = {"Reza", "Mina", "Hassan", "Nima"}
```

Then print the number of those students.

---

### Question 3

Explain the difference between:

```python
a - b
a ^ b
```

Use:

```python
a = {1, 2, 3}
b = {2, 3, 4}
```

---

## Comprehensive Set Question

Create a program using:

```python
python_students = {"Ali", "Sara", "Reza", "Mina", "Hassan"}
java_students = {"Reza", "Mina", "Hassan", "Nima"}
web_students = {"Mina", "Hassan", "Nima", "Omid"}
```

Your program should:

1. Find all students using Union.
2. Find students who study both Python and Java.
3. Find students who study Python but not Java.
4. Find students who study Java but not Python.
5. Find students who study exactly one of Python and Java.
6. Find students who belong to Python or Java but not both.
7. Print the number of students in each result using `len()`.
8. Iterate through the Symmetric Difference result.
9. Print it using `sorted()`.
10. Calculate Symmetric Difference once with `^`.
11. Calculate it again using `(a | b) - (a & b)`.
12. Verify that both results are equal.
13. Ask the user for a student name.
14. Check whether the student studies exactly one of Python and Java.

This exercise should combine:

**Creating Sets → `in` → `len()` → Iteration → `sorted()` → Union → Intersection → Difference → Symmetric Difference**

---

# Sets — Part 12: Converting Between Sets and Other Data Structures

So far, we have learned how to create Sets and perform operations such as:

* Union
* Intersection
* Difference
* Symmetric Difference
* Checking membership
* Iterating through Sets
* Counting Elements

In this part, we will learn how to **convert Sets to other data structures and convert other data structures to Sets**.

This is important because Python programs often need to move data between different structures depending on what we want to do with that data.

---

## 1. Converting a List to a Set

We can convert a List into a Set using `set()`:

```python
numbers = [1, 2, 3, 2, 4, 1]

numbers_set = set(numbers)

print(numbers_set)
```

Output:

```text
{1, 2, 3, 4}
```

Notice that duplicate values have been removed.

This is one of the most useful reasons to convert a List into a Set.

```text
List
→ allows duplicates

Set
→ stores unique elements
```

---

## 2. Removing Duplicates From a List

A common pattern is:

```python
numbers = [1, 2, 3, 2, 4, 1, 5, 3]

unique_numbers = set(numbers)

print(unique_numbers)
```

Output:

```text
{1, 2, 3, 4, 5}
```

The Set automatically removes duplicates.

If we need the result to be a List again:

```python
numbers = [1, 2, 3, 2, 4, 1, 5, 3]

unique_numbers = list(set(numbers))

print(unique_numbers)
```

The result is a List containing unique values.

However, there is an important detail:

> Converting a List to a Set can change the order of the elements.

If preserving order matters, this approach should be used carefully.

---

## 3. Converting a Tuple to a Set

Tuples can also be converted into Sets:

```python
numbers = (1, 2, 3, 2, 4)

numbers_set = set(numbers)

print(numbers_set)
```

Output:

```text
{1, 2, 3, 4}
```

Again, duplicates are removed.

The general pattern is:

```python
set(tuple_value)
```

---

## 4. Converting a String to a Set

A String is an iterable, so we can convert it into a Set:

```python
word = "banana"

letters = set(word)

print(letters)
```

Possible output:

```text
{'b', 'a', 'n'}
```

The Set contains each unique character.

For example:

```python
word = "programming"

letters = set(word)

print(letters)
```

The result contains each different character only once.

This can be useful when we want to find:

> Which unique characters appear in a String?

---

## 5. Converting a Set to a List

We can convert a Set into a List with `list()`:

```python
numbers = {1, 2, 3, 4}

numbers_list = list(numbers)

print(numbers_list)
```

Possible output:

```text
[1, 2, 3, 4]
```

The general syntax is:

```python
list(set_value)
```

This is useful when we need List-specific operations.

For example, Lists support indexing:

```python
numbers = {10, 20, 30}

numbers_list = list(numbers)

print(numbers_list[0])
```

A Set itself does not support indexing:

```python
numbers = {10, 20, 30}

# numbers[0]  # Error
```

---

## 6. Converting a Set to a Tuple

We can also convert a Set into a Tuple:

```python
numbers = {1, 2, 3, 4}

numbers_tuple = tuple(numbers)

print(numbers_tuple)
```

Possible output:

```text
(1, 2, 3, 4)
```

The syntax is:

```python
tuple(set_value)
```

This can be useful when we need an immutable sequence.

---

## 7. Converting a Set to a Sorted List

Because Sets do not guarantee the type of ordering we usually want, we can use `sorted()`:

```python
numbers = {5, 2, 8, 1, 4}

numbers_list = sorted(numbers)

print(numbers_list)
```

Output:

```text
[1, 2, 4, 5, 8]
```

Notice that `sorted()` returns a **List**, not a Set.

This is an important difference:

```python
sorted(numbers)
```

returns:

```text
List
```

while:

```python
set(numbers)
```

returns:

```text
Set
```

---

## 8. Converting a Set to a String

We cannot simply use:

```python
str(my_set)
```

if our goal is to create a clean custom String representation.

For example:

```python
letters = {"a", "b", "c"}

text = "".join(sorted(letters))

print(text)
```

Output:

```text
abc
```

Here we:

1. Sort the Set.
2. Convert the elements into a sequence.
3. Join them together.

This is useful when Set elements are Strings.

---

## 9. Converting a Dictionary's Keys to a Set

A Dictionary's keys can be converted into a Set:

```python
student = {
    "name": "Ali",
    "age": 20,
    "course": "Python"
}

keys = set(student.keys())

print(keys)
```

Possible output:

```text
{'name', 'age', 'course'}
```

We can also simply write:

```python
keys = set(student)
```

because iterating over a Dictionary normally gives us its keys.

---

## 10. Converting Dictionary Values to a Set

Dictionary values can also be converted:

```python
student = {
    "student1": "Ali",
    "student2": "Sara",
    "student3": "Ali"
}

values = set(student.values())

print(values)
```

Output:

```text
{'Ali', 'Sara'}
```

Notice that the duplicate `"Ali"` disappears.

This is useful when we want to find unique values stored in a Dictionary.

---

## 11. Converting Dictionary Items to a Set

Dictionary Items are Key-Value pairs:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

We can get its Items:

```python
items = student.items()

print(items)
```

To convert them into a Set:

```python
items_set = set(student.items())

print(items_set)
```

Possible output:

```text
{('name', 'Ali'), ('age', 20)}
```

Each Item becomes a Tuple.

This works because Dictionary Items are represented as pairs.

---

## 12. Why Can't We Put a Dictionary Inside a Set?

A Set requires its elements to be **hashable**.

A normal Dictionary is mutable, so it cannot be an element of a Set:

```python
my_set = {
    {"name": "Ali"}
}
```

This causes an error.

Similarly, a List cannot be directly stored inside a Set:

```python
my_set = {
    [1, 2, 3]
}
```

This also causes an error.

But a Tuple containing hashable values can be stored:

```python
my_set = {
    (1, 2, 3)
}
```

This works.

The important idea is:

```text
List      → mutable → not hashable
Dictionary → mutable → not hashable
Tuple     → usually immutable → can be hashable
```

---

## 13. Converting a List of Tuples to a Set

Consider:

```python
data = [
    ("Ali", 20),
    ("Sara", 22),
    ("Ali", 20)
]

data_set = set(data)

print(data_set)
```

Output:

```text
{('Ali', 20), ('Sara', 22)}
```

The duplicate Tuple is removed.

This is useful when working with structured data where each record is represented as a Tuple.

---

## 14. Converting a Set Back to a List

Sometimes we first use a Set to remove duplicates and then convert the result back to a List:

```python
numbers = [1, 2, 2, 3, 4, 4, 5]

unique_numbers = list(set(numbers))

print(unique_numbers)
```

This pattern is very common:

```text
List
→ Set
→ List
```

It means:

```text
Original data
→ remove duplicates
→ return to List
```

But remember that the original order may not be preserved.

---

## 15. Removing Duplicates While Preserving Order

If we want to remove duplicates while keeping the original order, a Set can be combined with a loop:

```python
numbers = [3, 1, 3, 2, 1, 4]

seen = set()
result = []

for number in numbers:
    if number not in seen:
        seen.add(number)
        result.append(number)

print(result)
```

Output:

```text
[3, 1, 2, 4]
```

Here:

* `seen` keeps track of values we have already encountered.
* `result` keeps the original order.

This is a more controlled approach than:

```python
list(set(numbers))
```

---

## 16. Converting Between Sets and Other Data Structures

Here is a useful summary:

| From              | To          | Syntax                  |
| ----------------- | ----------- | ----------------------- |
| List              | Set         | `set(my_list)`          |
| Tuple             | Set         | `set(my_tuple)`         |
| String            | Set         | `set(my_string)`        |
| Set               | List        | `list(my_set)`          |
| Set               | Tuple       | `tuple(my_set)`         |
| Set               | Sorted List | `sorted(my_set)`        |
| Dictionary Keys   | Set         | `set(my_dict.keys())`   |
| Dictionary Values | Set         | `set(my_dict.values())` |
| Dictionary Items  | Set         | `set(my_dict.items())`  |

---

## 17. Choosing the Right Data Structure

Different data structures are useful for different tasks.

### List

Use a List when:

* Order matters.
* Duplicates are allowed.
* Indexing is important.

```python
numbers = [10, 20, 30]
```

### Tuple

Use a Tuple when:

* You need an immutable sequence.
* The data should not normally change.

```python
point = (10, 20)
```

### Set

Use a Set when:

* You need unique elements.
* Membership checking is important.
* Set operations are useful.

```python
unique_numbers = {1, 2, 3}
```

### Dictionary

Use a Dictionary when:

* You need Key-Value relationships.

```python
student = {
    "name": "Ali",
    "age": 20
}
```

Understanding when to convert between these structures is an important Python skill.

---

## 18. Real-World Example: Cleaning Data

Suppose we receive duplicate usernames:

```python
usernames = [
    "ali",
    "sara",
    "ali",
    "reza",
    "sara",
    "mina"
]
```

We can remove duplicates:

```python
unique_usernames = set(usernames)

print(unique_usernames)
```

If we need them sorted:

```python
unique_usernames = sorted(set(usernames))

print(unique_usernames)
```

Output:

```text
['ali', 'mina', 'reza', 'sara']
```

This is a very common data-cleaning pattern:

```python
sorted(set(usernames))
```

---

## 19. Real-World Example: Comparing Data From Two Sources

Suppose two systems provide user IDs:

```python
system_a = [101, 102, 103, 104]
system_b = [103, 104, 105, 106]
```

Convert them to Sets:

```python
a = set(system_a)
b = set(system_b)
```

Now we can easily compare them.

Common users:

```python
common = a & b
```

Users only in System A:

```python
only_a = a - b
```

Users only in System B:

```python
only_b = b - a
```

Users appearing in only one system:

```python
different = a ^ b
```

This demonstrates why converting Lists into Sets can be extremely useful.

---

## 20. Important Limitation: Sets Do Not Preserve List Indexing

Consider:

```python
numbers = [10, 20, 30]
```

We can write:

```python
print(numbers[0])
```

But with:

```python
numbers = {10, 20, 30}
```

we cannot use:

```python
numbers[0]
```

because Sets are not index-based.

If we really need indexing:

```python
numbers = {10, 20, 30}

numbers_list = list(numbers)

print(numbers_list[0])
```

However, the specific element at index `0` should not be relied upon unless we explicitly create an ordered List, for example with `sorted()`.

---

## 21. Important Limitation: Conversion Does Not Always Preserve Structure

When converting between data structures, we need to understand what information may be lost.

For example:

```python
numbers = [3, 1, 3, 2]
```

After:

```python
numbers_set = set(numbers)
```

we get the unique values, but the List's duplicate information and intended ordering are no longer available.

So conversion is not always just a change of syntax.

Sometimes it changes the properties of the data.

---

# Key Takeaways

After this part, you should know:

1. `set()` can convert Lists, Tuples, Strings, and other iterables into Sets.
2. Converting to a Set removes duplicate elements.
3. `list()` converts a Set into a List.
4. `tuple()` converts a Set into a Tuple.
5. `sorted()` converts a Set into a sorted List.
6. Dictionary Keys can be converted into Sets.
7. Dictionary Values can be converted into Sets.
8. Dictionary Items can be converted into Sets when the Items are hashable.
9. Lists and Dictionaries cannot normally be elements of a Set because they are mutable and unhashable.
10. Tuples can be Set elements when their contents are hashable.
11. Converting a List to a Set may lose the original ordering.
12. We can combine Sets with Lists to remove duplicates.
13. Sets are useful for comparing data from different sources.
14. Choosing the correct data structure depends on whether we need ordering, uniqueness, indexing, or Key-Value relationships.

---

## Exercises

### Question 1

Convert this List into a Set and remove its duplicates:

```python
numbers = [1, 2, 2, 3, 4, 3, 5, 1]
```

Then convert the result back into a List.

---

### Question 2

Given:

```python
users = [
    "Ali",
    "Sara",
    "Ali",
    "Reza",
    "Sara",
    "Mina"
]
```

Create a sorted List containing only unique usernames.

---

### Question 3

Given:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Tehran"
}
```

Create:

1. A Set containing the Dictionary Keys.
2. A Set containing the Dictionary Values.
3. A Set containing the Dictionary Items.

---

## Comprehensive Set Question

Create a program using:

```python
python_students = [
    "Ali",
    "Sara",
    "Reza",
    "Mina",
    "Ali"
]

java_students = [
    "Reza",
    "Mina",
    "Hassan",
    "Nima",
    "Reza"
]

web_students = [
    "Mina",
    "Hassan",
    "Nima",
    "Omid",
    "Mina"
]
```

Your program should:

1. Convert all three Lists into Sets.
2. Print the unique students in each course.
3. Find students who study both Python and Java.
4. Find students who study Python but not Java.
5. Find students who study Java but not Python.
6. Find students who study exactly one of Python and Java.
7. Find all students across the three courses.
8. Convert the final Set into a sorted List.
9. Print the number of unique students using `len()`.
10. Create a Dictionary containing the number of students in each course.
11. Convert the Dictionary Keys into a Set.
12. Convert the Dictionary Values into a Set.
13. Convert the Dictionary Items into a Set.
14. Explain which information may be lost when converting a List into a Set.
15. Explain why a Set is useful for comparing the three courses.

This exercise should combine:

**Lists → Sets → `set()` → `list()` → `tuple()` → `sorted()` → Dictionary Keys → Dictionary Values → Dictionary Items → Union → Intersection → Difference → Symmetric Difference → `len()`**

---

