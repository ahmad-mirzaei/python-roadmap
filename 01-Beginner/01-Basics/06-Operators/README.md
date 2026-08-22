# Part 1 — What Are Operators and Operands?

🌐 Language: **English** | [فارسی](fa/README.md)

In programming, we often need to perform actions such as:

* Adding numbers
* Subtracting values
* Comparing two pieces of information
* Combining data

To perform these actions, Python uses **operators**.

---

## A Real-World Example

Imagine a calculator.

If you type:

```text
5 + 3
```

The calculator performs an operation.

* `5` is a value.
* `3` is another value.
* `+` tells the calculator to add them.

Programming works in the same way.

---

## What Is an Operator?

An **operator** is a symbol that tells Python to perform an action.

Examples:

```python
+
-
*
/
=
```

Each operator has a specific meaning.

---

## What Is an Operand?

An **operand** is the value that the operator works with.

Example:

```python
5 + 3
```

Here:

* `5` → operand
* `3` → operand
* `+` → operator

---

## Another Example

```python
price = 100
discount = 20

final_price = price - discount
```

In the expression:

```python
price - discount
```

* `price` is an operand.
* `discount` is an operand.
* `-` is the operator.

Python subtracts the second operand from the first operand.

---

## Why Are Operators Important?

Without operators, programs could store information but could not work with it.

Operators allow programs to:

* Calculate totals
* Find differences
* Compare values
* Make decisions
* Update information

Almost every Python program uses operators.

---

## Part Summary

* An **operator** is a symbol that performs an action.
* An **operand** is the value used by the operator.
* Example:

```python
5 + 3
```

`+` is the operator, while `5` and `3` are operands.

In the next part, you will learn the most common arithmetic operators in Python.

---

# Part 2 — Arithmetic Operators

In the previous part, you learned what operators and operands are.

Now it's time to learn the operators you will use most often in Python.

These operators are called **Arithmetic Operators** because they perform mathematical calculations.

---

## A Real-World Example

Think about using a calculator.

When you calculate:

```
15 + 5
```

the calculator performs an addition.

When you calculate:

```
20 - 8
```

it performs a subtraction.

Python works exactly the same way.

It uses arithmetic operators to perform mathematical calculations.

---

## Addition (+)

The addition operator adds two values together.

Example:

```python
a = 10
b = 5

result = a + b

print(result)
```

Output:

```text
15
```

---

## Subtraction (-)

The subtraction operator subtracts one value from another.

Example:

```python
a = 20
b = 8

result = a - b

print(result)
```

Output:

```text
12
```

---

## Multiplication (*)

The multiplication operator multiplies two values.

Example:

```python
a = 6
b = 4

result = a * b

print(result)
```

Output:

```text
24
```

---

## Division (/)

The division operator divides one value by another.

Example:

```python
a = 20
b = 5

result = a / b

print(result)
```

Output:

```text
4.0
```

Notice that Python returns a floating-point number.

---

## Floor Division (//)

The floor division operator divides two numbers and keeps only the whole-number part.

Example:

```python
a = 20
b = 6

result = a // b

print(result)
```

Output:

```text
3
```

The decimal part is discarded.

---

## Modulus (%)

The modulus operator returns the remainder after division.

Example:

```python
a = 20
b = 6

result = a % b

print(result)
```

Output:

```text
2
```

Because:

```
20 = (6 × 3) + 2
```

The remainder is `2`.

---

## Exponent (**)

The exponent operator raises a number to a power.

Example:

```python
result = 2 ** 3

print(result)
```

Output:

```text
8
```

Because:

```
2 × 2 × 2 = 8
```

---

## Summary Table

| Operator | Meaning | Example |
|----------|---------|---------|
| `+` | Addition | `10 + 5` |
| `-` | Subtraction | `20 - 8` |
| `*` | Multiplication | `6 * 4` |
| `/` | Division | `20 / 5` |
| `//` | Floor Division | `20 // 6` |
| `%` | Modulus | `20 % 6` |
| `**` | Exponent | `2 ** 3` |

---

## Common Beginner Mistake

Many beginners confuse `/` and `//`.

```python
20 / 6
```

Result:

```text
3.3333333333333335
```

But:

```python
20 // 6
```

Result:

```text
3
```

The first returns the exact result.

The second returns only the whole-number part.

---

## Part Summary

- Arithmetic operators perform mathematical calculations.
- Python supports seven arithmetic operators.
- `/` and `//` are different operators.
- `%` returns the remainder.
- `**` calculates powers.

---

# Part 3 — Assignment Operators

In previous lessons, you have already used the assignment operator many times.

For example:

```python
age = 36
```

But what exactly is happening here?

The assignment operator stores a value inside a variable.

Python also provides several shortcut assignment operators that make your code shorter and easier to read.

---

## Assignment (=)

The `=` operator assigns a value to a variable.

Example:

```python
score = 100
```

Now the variable `score` stores the value `100`.

---

## Add and Assign (+=)

Instead of writing:

```python
score = score + 10
```

you can write:

```python
score += 10
```

Both statements produce the same result.

---

## Subtract and Assign (-=)

Example:

```python
score -= 5
```

This means:

```python
score = score - 5
```

---

## Multiply and Assign (*=)

Example:

```python
score *= 2
```

Equivalent to:

```python
score = score * 2
```

---

## Divide and Assign (/=)

Example:

```python
score /= 4
```

Equivalent to:

```python
score = score / 4
```

---

## Summary Table

| Operator | Equivalent Expression |
|----------|------------------------|
| `=` | Assign a value |
| `+=` | `x = x + value` |
| `-=` | `x = x - value` |
| `*=` | `x = x * value` |
| `/=` | `x = x / value` |

---

## Part Summary

Assignment operators update the value of a variable.

They help you write cleaner and shorter code.

---

# Part 4 — Comparison Operators

Programs often need to compare values before making decisions.

For example:

- Is the user old enough to register?
- Is the password correct?
- Is the score greater than 90?

Python uses **comparison operators** to compare two values.

A comparison always produces one of two results:

- `True`
- `False`

---

## Equal To (==)

The `==` operator checks whether two values are equal.

Example:

```python
print(10 == 10)
```

Output:

```text
True
```

Example:

```python
print(10 == 5)
```

Output:

```text
False
```

---

## Not Equal To (!=)

The `!=` operator checks whether two values are different.

Example:

```python
print(10 != 5)
```

Output:

```text
True
```

---

## Greater Than (>)

Checks whether the left value is greater than the right value.

Example:

```python
print(20 > 15)
```

Output:

```text
True
```

---

## Less Than (<)

Checks whether the left value is smaller than the right value.

Example:

```python
print(7 < 3)
```

Output:

```text
False
```

---

## Greater Than or Equal To (>=)

Example:

```python
print(18 >= 18)
```

Output:

```text
True
```

---

## Less Than or Equal To (<=)

Example:

```python
print(12 <= 20)
```

Output:

```text
True
```

---

## Summary Table

| Operator | Meaning |
|----------|---------|
| `==` | Equal to |
| `!=` | Not equal to |
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |

---

## Try It Yourself

### 🟢 Easy

Predict the output:

```python
print(5 == 5)
```

---

### 🟡 Medium

Predict the output:

```python
print(15 < 10)
```

---

### 🔴 Challenge

Write three comparison statements that produce:

- `True`
- `False`
- `True`

---

# Part 5 — Logical Operators

Sometimes comparing a single condition is not enough.

For example:

- Is the user over 18 **and** has a valid ID?
- Is today Saturday **or** Sunday?
- Is the password **not** empty?

Python uses **logical operators** to combine or modify conditions.

There are three logical operators:

- `and`
- `or`
- `not`

---

## The `and` Operator

The `and` operator returns `True` only when **both conditions** are `True`.

Example:

```python
age = 36
has_id = True

print(age >= 18 and has_id)
```

Output:

```text
True
```

If one condition becomes `False`, the entire expression becomes `False`.

---

## The `or` Operator

The `or` operator returns `True` when **at least one condition** is `True`.

Example:

```python
is_saturday = False
is_sunday = True

print(is_saturday or is_sunday)
```

Output:

```text
True
```

Only when both conditions are `False` does the result become `False`.

---

## The `not` Operator

The `not` operator reverses a Boolean value.

Example:

```python
is_logged_in = False

print(not is_logged_in)
```

Output:

```text
True
```

---

## Summary Table

| Operator | Meaning |
|----------|---------|
| `and` | Both conditions must be True |
| `or` | At least one condition must be True |
| `not` | Reverses the result |

---

## A Real-World Example

Imagine a website.

To log in, the user must:

- Enter the correct username.
- Enter the correct password.

Both conditions must be correct.

This is a perfect example of the `and` operator.

Another example:

A cinema offers discounts on **Saturday or Sunday**.

Only one of these days is enough.

This is a good example of the `or` operator.

---

## Try It Yourself

### 🟢 Easy

Predict the output:

```python
print(True and False)
```

---

### 🟡 Medium

Predict the output:

```python
print(False or True)
```

---

### 🔴 Challenge

Predict the output:

```python
print(not (10 > 5))
```

---

# Try It Yourself

Now it's time to practice what you have learned.

Try to solve these exercises before looking at the answers.

---

## 🟢 Easy

### Exercise 1

Create two variables:

```python
a = 15
b = 5
```

Print:

- Addition
- Subtraction
- Multiplication
- Division

---

### Exercise 2

Create a variable named `score` with the value `80`.

Increase it by `10` using an assignment operator.

Print the result.

---

### Exercise 3

Predict the output:

```python
print(20 > 15)
```

---

## 🟡 Medium

### Exercise 4

Create two variables:

```python
age = 36
height = 1.84
```

Print whether the age is greater than `18`.

---

### Exercise 5

Predict the output:

```python
print(25 % 4)
```

Explain why.

---

### Exercise 6

Predict the output:

```python
print((15 > 10) and (20 < 30))
```

---

## 🔴 Challenge

### Exercise 7

Without running the code, predict the output.

```python
number = 12

number += 8
number *= 2

print(number)
```

---

### Exercise 8

Predict the result.

```python
print((8 > 5) or (10 < 3))
```

---

### Exercise 9

Create two variables:

```python
age = 36
country = "Iran"
```

Write a comparison that returns `True`.

Then write another comparison that returns `False`.

---

# Mini Project — Simple Calculator

In this project, you will create a simple calculator.

The program will:

- Receive two numbers from the user.
- Perform mathematical operations.
- Display the results.

---

## Project Goal

Create a program that calculates:

- Addition
- Subtraction
- Multiplication
- Division

---

## Example Output

Input:

```text
10
5
```

Output:

```text
Addition: 15
Subtraction: 5
Multiplication: 50
Division: 2.0
```

---

## Challenge

Improve the calculator:

- Add floor division (`//`).
- Add modulus (`%`).
- Add exponent (`**`).

---

# Operators — Operator Precedence

In this part, we will learn about **Operator Precedence** in Python.

Operator precedence determines **which operation Python performs first** when an expression contains multiple operators.

Understanding precedence is important because an expression can produce a different result depending on the order in which its operations are evaluated.

---

## 1. What Is Operator Precedence?

Consider this expression:

```python
result = 2 + 3 * 4

print(result)
```

The result is:

```text
14
```

Why isn't the result `20`?

Because Python performs multiplication before addition:

```text
3 * 4 = 12
2 + 12 = 14
```

So Python effectively evaluates:

```python
2 + (3 * 4)
```

not:

```python
(2 + 3) * 4
```

---

## 2. Parentheses Have the Highest Priority

Parentheses can change the normal order of operations.

```python
result = (2 + 3) * 4

print(result)
```

Output:

```text
20
```

Without parentheses:

```python
result = 2 + 3 * 4

print(result)
```

Output:

```text
14
```

Therefore, parentheses are the easiest way to explicitly control the order of evaluation.

---

## 3. Basic Precedence Order

A simplified Python operator precedence order is:

| Priority | Operators                        | Description                                      |
| -------- | -------------------------------- | ------------------------------------------------ |
| 1        | `()`                             | Parentheses                                      |
| 2        | `**`                             | Exponentiation                                   |
| 3        | `+x`, `-x`                       | Unary plus and minus                             |
| 4        | `*`, `/`, `//`, `%`              | Multiplication, division, floor division, modulo |
| 5        | `+`, `-`                         | Addition and subtraction                         |
| 6        | `==`, `!=`, `<`, `<=`, `>`, `>=` | Comparisons                                      |
| 7        | `not`                            | Logical NOT                                      |
| 8        | `and`                            | Logical AND                                      |
| 9        | `or`                             | Logical OR                                       |

The higher an operator appears in the table, the earlier Python generally evaluates it.

---

## 4. Multiplication Before Addition

Consider:

```python
result = 10 + 5 * 2

print(result)
```

Python evaluates:

```text
5 * 2 = 10
10 + 10 = 20
```

Therefore:

```text
20
```

If we want addition first:

```python
result = (10 + 5) * 2

print(result)
```

Now:

```text
15 * 2 = 30
```

Output:

```text
30
```

---

## 5. Division and Multiplication

Multiplication, division, floor division, and modulo have the same precedence level.

For example:

```python
result = 20 / 5 * 2

print(result)
```

These operators are evaluated from **left to right**:

```text
20 / 5 = 4
4 * 2 = 8
```

Output:

```text
8.0
```

Similarly:

```python
result = 20 * 5 / 2

print(result)
```

is evaluated as:

```text
20 * 5 = 100
100 / 2 = 50
```

---

## 6. Addition and Subtraction

Addition and subtraction also have the same precedence.

Python evaluates them from left to right.

```python
result = 20 - 5 + 2

print(result)
```

Evaluation:

```text
20 - 5 = 15
15 + 2 = 17
```

Output:

```text
17
```

It is equivalent to:

```python
result = (20 - 5) + 2
```

---

## 7. Exponentiation

Exponentiation has a higher precedence than multiplication, division, addition, and subtraction.

```python
result = 2 + 3 ** 2

print(result)
```

Python first calculates:

```text
3 ** 2 = 9
```

Then:

```text
2 + 9 = 11
```

Output:

```text
11
```

This is equivalent to:

```python
result = 2 + (3 ** 2)
```

---

## 8. Exponentiation and Parentheses

Consider:

```python
result = (2 + 3) ** 2

print(result)
```

Python first calculates:

```text
2 + 3 = 5
```

Then:

```text
5 ** 2 = 25
```

Output:

```text
25
```

Compare it with:

```python
result = 2 + 3 ** 2

print(result)
```

Output:

```text
11
```

The parentheses completely change the result.

---

## 9. Unary Plus and Minus

Unary operators are operators that work with one value.

For example:

```python
x = -5
y = +5

print(x)
print(y)
```

Here:

```python
-5
+5
```

are unary operations.

They are different from binary subtraction and addition:

```python
5 - 3
```

and:

```python
5 + 3
```

---

## 10. The `**` and Unary Minus Example

Consider:

```python
result = -2 ** 2

print(result)
```

The result is:

```text
-4
```

Why?

Because exponentiation has higher precedence than the unary minus:

```text
2 ** 2 = 4
-4
```

If we want the negative number to be squared:

```python
result = (-2) ** 2

print(result)
```

Output:

```text
4
```

This is an important example of why parentheses matter.

---

## 11. Modulo and Floor Division

The following operators have the same precedence:

```text
*
/
//
%
```

For example:

```python
result = 17 % 5 + 2

print(result)
```

First:

```text
17 % 5 = 2
```

Then:

```text
2 + 2 = 4
```

Output:

```text
4
```

Another example:

```python
result = 17 // 5 * 2

print(result)
```

First:

```text
17 // 5 = 3
```

Then:

```text
3 * 2 = 6
```

---

## 12. Comparison Operators

Comparison operators have lower precedence than arithmetic operators.

For example:

```python
result = 10 + 5 > 12

print(result)
```

Python first performs:

```text
10 + 5 = 15
```

Then:

```text
15 > 12
```

Therefore:

```text
True
```

This is equivalent to:

```python
result = (10 + 5) > 12
```

---

## 13. Multiple Comparisons

Python allows chained comparisons.

For example:

```python
age = 20

result = 18 <= age < 30

print(result)
```

Output:

```text
True
```

This is effectively checking:

```python
18 <= age and age < 30
```

Chained comparisons are a useful Python feature.

---

## 14. `not`, `and`, and `or`

Logical operators have their own precedence.

The order is:

```text
not
and
or
```

So:

```python
result = True or False and False

print(result)
```

Python evaluates `and` first:

```text
False and False = False
```

Then:

```text
True or False = True
```

Output:

```text
True
```

This is equivalent to:

```python
result = True or (False and False)
```

---

## 15. Using Parentheses with Logical Operators

Consider:

```python
result = (True or False) and False

print(result)
```

First:

```text
True or False = True
```

Then:

```text
True and False = False
```

Output:

```text
False
```

Compare:

```python
True or False and False
```

with:

```python
(True or False) and False
```

The results are different because parentheses change the evaluation order.

---

## 16. A Complex Example

Consider:

```python
result = 10 + 2 * 3 ** 2

print(result)
```

Let's evaluate it step by step.

### Step 1 — Exponentiation

```text
3 ** 2 = 9
```

### Step 2 — Multiplication

```text
2 * 9 = 18
```

### Step 3 — Addition

```text
10 + 18 = 28
```

Therefore:

```text
28
```

---

## 17. Another Complex Example

```python
result = (10 + 2) * 3 ** 2

print(result)
```

First:

```text
10 + 2 = 12
```

Then:

```text
3 ** 2 = 9
```

Then:

```text
12 * 9 = 108
```

Output:

```text
108
```

---

## 18. A Boolean Example

Consider:

```python
age = 25
has_ticket = True

result = age >= 18 and has_ticket

print(result)
```

Python first evaluates the comparison:

```text
age >= 18
```

which becomes:

```text
True
```

Then:

```text
True and True
```

Therefore:

```text
True
```

---

## 19. A Mixed Arithmetic and Boolean Example

```python
x = 10

result = x + 5 > 12 and x * 2 == 20

print(result)
```

Python evaluates the arithmetic first:

```text
x + 5 = 15
x * 2 = 20
```

Then the comparisons:

```text
15 > 12
20 == 20
```

Both are `True`.

Finally:

```text
True and True
```

So:

```text
True
```

---

## 20. Parentheses as a Best Practice

Even when you know the precedence rules, parentheses can make code easier to understand.

Instead of:

```python
result = age >= 18 and score >= 60 or has_permission
```

we can write:

```python
result = (age >= 18 and score >= 60) or has_permission
```

The second version makes the intended logic much clearer.

Parentheses are especially useful when expressions become complicated.

---

# Practical Summary

The most important precedence rules to remember are:

```text
()
**
+x, -x
*, /, //, %
+, -
comparisons
not
and
or
```

A useful mental model is:

```text
Parentheses
    ↓
Power
    ↓
Multiply / Divide
    ↓
Add / Subtract
    ↓
Compare
    ↓
not
    ↓
and
    ↓
or
```

When you are unsure about an expression, use parentheses.

Clear code is usually better than code that depends on the reader remembering every precedence rule.

---

# Final Exercises

### Question 1

What is the result?

```python
result = 2 + 3 * 4
```

### Question 2

What is the result?

```python
result = (2 + 3) * 4
```

### Question 3

What is the result?

```python
result = 2 + 3 ** 2 * 2
```

### Question 4

What is the difference between:

```python
-2 ** 2
```

and:

```python
(-2) ** 2
```

### Question 5

What is the result?

```python
result = True or False and False
```

### Question 6

Rewrite this expression using parentheses so that the evaluation order is obvious:

```python
result = 10 + 5 * 2 > 15 and 20 % 3 == 2
```

---

# Comprehensive Question

Without running the code, determine the final value of each expression and explain the order in which Python evaluates the operators:

```python
a = 2 + 3 * 4
b = (2 + 3) * 4
c = 2 ** 3 * 2 + 1
d = -2 ** 2
e = (-2) ** 2
f = 20 / 5 * 2
g = 20 - 5 + 2
h = True or False and False
i = (True or False) and False
j = 10 + 2 * 3 ** 2 > 25 and 20 % 3 == 2
```

For each expression:

1. Identify the highest-precedence operator.
2. Evaluate the expression step by step.
3. Write the final result.
4. Explain whether parentheses could make the expression clearer.

---

