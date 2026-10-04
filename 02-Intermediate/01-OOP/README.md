# Object-Oriented Programming

🌐 Language: **فارسی** | [English](../01-OOP/fa/README.md)

## Table of Contents

| Part | Topic |
|---|---|
| 1 | Introduction to Object-Oriented Programming |
| 2 | Classes |
| 3 | Objects |
| 4 | The `__init__()` Method |
| 5 | Instance Attributes |
| 6 | Instance Methods |
| 7 | The `self` Parameter |
| 8 | Class Attributes |
| 9 | Class Methods |
| 10 | Static Methods |
| 11 | Object Interaction |
| 12 | Inheritance |
| 13 | Method Overriding |
| 14 | `super()` |
| 15 | Encapsulation |
| 16 | Properties |
| 17 | `__str__()` and `__repr__()` |
| 18 | Special Methods |
| 19 | Common Mistakes and Best Practices |
| 20 | Final Review: OOP |
| 21 | OOP Mini Project |

---

# Part 1: Introduction to OOP

## 1. What Is Object-Oriented Programming?

**Object-Oriented Programming**, usually called **OOP**, is a programming style where we organize code around **objects**.

An object can represent something such as:

- a user
- a product
- a bank account
- a student
- a car
- a book
- a game character

Each object can have:

- **data** — information about the object
- **behavior** — actions that the object can perform

For example, a `Car` object might have:

```python
brand = "Toyota"
color = "Red"
speed = 80
```

and it might be able to perform actions such as:

```python
start()
stop()
accelerate()
brake()
```

So we can think about an object as a combination of **data and behavior**.

---

## 2. Why Do We Need OOP?

As programs become larger, managing everything with simple variables and functions can become difficult.

Imagine a program that manages students.

Without OOP, we might have:

```python
student1_name = "Ali"
student1_age = 20
student1_grade = 18.5

student2_name = "Sara"
student2_age = 21
student2_grade = 19.0
```

As the number of students increases, the code becomes harder to organize.

We might also create separate functions:

```python
def print_student(name, age, grade):
    print(name)
    print(age)
    print(grade)
```

This works, but the data belonging to each student is spread across separate variables.

With OOP, we can represent each student as an object.

Conceptually:

```text
Student
│
├── name
├── age
├── grade
│
├── study()
└── introduce()
```

Now the information and behavior related to a student can live together.

---

## 3. Objects as Real-World Models

One of the most useful ways to understand OOP is to think about **real-world objects**.

Suppose we want to create a program for a library.

A library may contain many books.

Each book can have information such as:

```text
Book
├── title
├── author
├── year
└── price
```

A book might also have behaviors such as:

```text
borrow()
return_book()
display_info()
```

Instead of creating unrelated variables and functions, OOP allows us to create a structure that represents the concept of a book.

This is called **modeling**.

We are modeling a real-world concept inside our program.

---

## 4. Class vs Object

Two important concepts in OOP are:

- **Class**
- **Object**

They are related, but they are not the same thing.

A **class** is a blueprint or template.

An **object** is an actual instance created from that class.

A simple analogy is a house.

The architectural plan is similar to a class:

```text
House Blueprint
├── number of rooms
├── color
├── doors
└── windows
```

An actual house is similar to an object:

```text
House #1
├── 3 rooms
├── white
├── 2 doors
└── 6 windows
```

Another house can use the same blueprint:

```text
House #2
├── 4 rooms
├── blue
├── 3 doors
└── 8 windows
```

Both houses follow the same general structure, but they contain different data.

In Python:

```text
Class
  ↓
Blueprint

Object
  ↓
Actual instance
```

We will learn how to create classes and objects in the next Parts.

---

## 5. Data and Behavior

Objects usually contain two important categories of information.

### Data

Data describes the object.

For example, a `Student` could have:

```text
name
age
grade
```

A `Car` could have:

```text
brand
model
color
speed
```

A `BankAccount` could have:

```text
owner
balance
account_number
```

### Behavior

Behavior describes what the object can do.

A `Student` might:

```text
study()
take_exam()
introduce()
```

A `Car` might:

```text
start()
accelerate()
brake()
stop()
```

A `BankAccount` might:

```text
deposit()
withdraw()
check_balance()
```

In Python, behaviors are usually represented using **methods**.

A method is a function that belongs to a class or object.

We will study methods in detail later.

---

## 6. A Simple OOP Mental Model

A useful mental model is:

```text
Class
  │
  ├── Data
  │
  └── Behavior
        │
        ↓
     Objects
```

For example:

```text
Class: Student

Data:
    name
    age
    grade

Behavior:
    study()
    introduce()
    take_exam()
```

From this class, we could create several objects:

```text
student1 → Ali
student2 → Sara
student3 → Reza
```

All three objects follow the same general structure, but their data can be different.

---

## 7. OOP Does Not Mean Everything Must Be an Object

A common beginner misunderstanding is thinking:

> "If Python supports OOP, I must use classes for everything."

That is not true.

Python supports multiple programming styles.

For example, a simple calculation does not necessarily need a class:

```python
def calculate_total(price, quantity):
    return price * quantity
```

Creating a class for this simple function might make the code unnecessarily complicated.

OOP becomes especially useful when:

- the program has many related entities
- each entity has its own data
- each entity has its own behavior
- objects interact with each other
- the program is becoming difficult to organize
- we want reusable structures

The goal is not to use classes everywhere.

The goal is to use them when they make the program clearer and easier to maintain.

---

## 8. OOP and Code Organization

One of the major advantages of OOP is better organization.

Imagine a game.

Without OOP, we might have:

```text
player_name
player_health
player_score

enemy_name
enemy_health
enemy_damage

move_player()
attack_enemy()
take_damage()
```

As the game becomes larger, the number of variables and functions can grow quickly.

With OOP, we can model the concepts separately:

```text
Player
├── name
├── health
├── score
├── move()
└── attack()

Enemy
├── name
├── health
├── damage
└── attack()
```

This makes the structure of the program easier to understand.

---

## 9. Reusability

Another important advantage of OOP is **reusability**.

Suppose we create a `Student` class once.

We can then create many student objects from it:

```text
Student class
     │
     ├── student1
     ├── student2
     ├── student3
     └── student4
```

We do not need to rewrite the entire structure for every student.

The same idea applies to:

- users
- products
- employees
- customers
- vehicles
- books
- game characters

This is one of the main reasons classes are useful in larger programs.

---

## 10. OOP and Encapsulation

OOP also gives us tools for keeping related data and behavior together.

For example, a bank account has a balance.

Instead of having:

```python
balance = 1000
```

and many unrelated functions manipulating that variable, we can eventually create something conceptually like:

```text
BankAccount
├── balance
├── deposit()
└── withdraw()
```

Now the operations related to the account are grouped with the account itself.

This idea leads to a major OOP concept called **encapsulation**.

We will study encapsulation later in this lesson.

---

## 11. OOP and Abstraction

Another important OOP concept is **abstraction**.

Abstraction means that we can work with a concept without needing to know all of its internal implementation details.

For example, when we use:

```python
numbers.append(10)
```

we do not need to know exactly how Python internally changes the list's memory.

We simply use the operation we need.

In larger OOP systems, classes can provide a simple interface while hiding unnecessary implementation details.

We will study abstraction more deeply later.

---

## 12. OOP and Inheritance

OOP also allows one class to build upon another class.

For example:

```text
Animal
  │
  ├── Dog
  └── Cat
```

A `Dog` can inherit common characteristics from `Animal`.

Conceptually:

```text
Animal
├── name
├── eat()
└── sleep()

Dog
├── bark()
└── inherited eat()
└── inherited sleep()
```

This is called **inheritance**.

Inheritance can help us avoid repeating common code.

However, inheritance should be used carefully. It is not always the best solution for every relationship.

We will study it in detail later.

---

## 13. OOP and Polymorphism

Another important concept is **polymorphism**.

The word comes from Greek roots meaning "many forms."

In programming, polymorphism allows different objects to respond to the same operation in different ways.

For example:

```text
Animal
   │
   ├── Dog → speak() → "Woof"
   └── Cat → speak() → "Meow"
```

Both objects have a `speak()` behavior, but each provides its own implementation.

This allows code to work with different object types through a common interface.

We will study this concept after learning the foundations of classes and objects.

---

## 14. A Small Preview

We are not going to build the complete class yet, but the following example gives us a preview of where this lesson is going:

```python
class Student:
    pass
```

Here we have created a class named `Student`.

We can later create objects from it:

```python
student1 = Student()
student2 = Student()
```

Now:

```text
Student
   │
   ├── student1
   └── student2
```

These are two different objects created from the same class.

We will gradually learn how to give these objects data and behavior.

---

## 15. When Should You Use OOP?

OOP is often useful when your program contains multiple entities with their own data and behavior.

Good examples include:

- banking applications
- e-commerce systems
- school management systems
- games
- inventory systems
- employee management systems
- reservation systems
- larger APIs and applications

For example, an e-commerce application might contain:

```text
User
Product
ShoppingCart
Order
Payment
Address
```

Each of these concepts can have its own data and behavior.

OOP gives us a way to model these concepts in a structured way.

---

## 16. When Should You Avoid OOP?

Not every program needs classes.

For example, this program is simple:

```python
numbers = [10, 20, 30, 40]

total = sum(numbers)

print(total)
```

There is no strong reason to create a class just to calculate the sum.

Similarly:

```python
def greet(name):
    return f"Hello, {name}!"
```

does not need a class.

A useful rule is:

> Use the simplest structure that clearly solves the problem.

OOP is a tool, not a requirement.

---

## 17. Common Beginner Mistakes

### Mistake 1: Thinking Class and Object Are the Same

A class is the blueprint.

An object is an instance created from that blueprint.

```text
Class → Blueprint
Object → Instance
```

---

### Mistake 2: Creating Classes for Everything

A class is not automatically better than a function.

If a simple function solves the problem clearly, use the function.

---

### Mistake 3: Learning Syntax Without Understanding the Model

It is possible to memorize:

```python
class Student:
    pass
```

without understanding what a class actually represents.

Focus first on the concepts:

```text
Class
   ↓
Blueprint

Object
   ↓
Instance

Attributes
   ↓
Data

Methods
   ↓
Behavior
```

Once this mental model is clear, the syntax becomes much easier.

---

### Mistake 4: Thinking OOP Is Only About Inheritance

Inheritance is only one part of OOP.

Important OOP concepts include:

- classes
- objects
- attributes
- methods
- encapsulation
- abstraction
- inheritance
- polymorphism

We will study these concepts step by step.

---

## 18. Final Review

In this Part, we learned that:

- OOP stands for **Object-Oriented Programming**.
- OOP organizes programs around objects.
- Objects can contain data and behavior.
- A **class** is a blueprint or template.
- An **object** is an instance of a class.
- Methods represent behavior.
- Attributes represent data.
- OOP can improve organization and reusability.
- OOP is useful for larger and more structured programs.
- Not every problem needs a class.
- Encapsulation, abstraction, inheritance, and polymorphism are important OOP concepts that we will study later.

The most important mental model to remember is:

```text
Class
  ↓
Blueprint

Object
  ↓
Instance

Attributes
  ↓
Data

Methods
  ↓
Behavior
```

---

## Questions

### Question 1

What is the main difference between a class and an object?

### Question 2

Why can OOP make a large program easier to organize?

### Question 3

Should every Python program use classes? Explain why or why not.

---

## Comprehensive Question

Imagine you are going to build a **library management system**.

The system needs to manage books.

Each book has:

- a title
- an author
- a publication year
- a price

Each book should eventually be able to perform actions such as:

- displaying its information
- being borrowed
- being returned

Answer the following:

1. What could the class represent?
2. What could the objects represent?
3. Which items would be attributes?
4. Which items would be methods?
5. Why would using OOP be more suitable here than keeping everything in unrelated variables and functions?

Do not worry about writing the complete class yet. The goal is to design the structure conceptually.