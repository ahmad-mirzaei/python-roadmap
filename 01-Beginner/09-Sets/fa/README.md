## فهرست مطالب

1. Introduction to Sets
2. Creating Sets
3. Adding Elements to a Set
4. Removing Elements from a Set
5. Checking for an Element in a Set
6. Set Length and Counting Elements
7. Iterating Through Sets
8. Set Union
9. Set Intersection
10. Set Difference
11. Set Symmetric Difference
12. Converting Between Sets and Other Data Structures
13. Set Immutability and `frozenset`
14. Final Review: Sets
15. Sets Mini Project

---

# Sets — پارت ۱: مقدمه ای بر ست ها

> 🌐 Language: **فارسی** | [English](../README.md)

## Set چیست؟

**Set** یکی از Data Structure های داخلی Python است که برای نگه داری یک مجموعه از **عناصر یکتا (Unique)** استفاده می شود.

مهم ترین ویژگی Set این است که **Duplicate**ها را نگه نمی دارد.

مثلا:

```python
numbers = {1, 2, 3, 4}
```

در اینجا `numbers` یک Set است که چهار عنصر دارد.

در مقایسه با List:

```python
numbers = [1, 2, 3, 4]
```

Set از Position و Index برای سازمان دهی عناصر استفاده نمی کند.

---

## Set عناصر تکراری ندارد

به این Set دقت کنید:

```python
numbers = {1, 2, 2, 3, 3, 3}
```

Python به صورت خودکار Duplicateها را حذف می کند.

اگر آن را نمایش دهیم:

```python
print(numbers)
```

نتیجه فقط شامل مقادیر Unique خواهد بود:

```text
{1, 2, 3}
```

این ویژگی باعث می شود Set برای زمانی که فقط به مقادیر یکتا نیاز داریم بسیار مفید باشد.

مثلا:

```python
names = {"Ali", "Sara", "Ali", "Reza", "Sara"}

print(names)
```

هر نام فقط یک بار در Set باقی می ماند.

---

## Setها Index ندارند

Set برخلاف List و Tuple، برای دسترسی به عناصر از Index استفاده نمی کند.

مثلا در List:

```python
numbers = [10, 20, 30]

print(numbers[0])
```

می توانیم عنصر اول را دریافت کنیم.

اما این کار با Set امکان پذیر نیست:

```python
numbers = {10, 20, 30}

print(numbers[0])
```

چون Set از Indexing پشتیبانی نمی کند، این کد باعث Error می شود.

پس بهتر است تفاوت را این طور در ذهن داشته باشید:

```text
List / Tuple
    ↓
Ordered Collection
    ↓
Index-based Access

Set
    ↓
Collection of Unique Elements
    ↓
No Index-based Access
```

هدف اصلی Set نگه داری عناصر Unique و انجام عملیات روی مجموعه هاست، نه دسترسی به عناصر بر اساس Position.

---

## ساخت یک Set خالی

هنگام ساخت Empty Set یک نکته بسیار مهم وجود دارد.

این کد:

```python
empty = {}
```

یک Set خالی ایجاد نمی کند.

بلکه یک **Dictionary خالی** ایجاد می کند.

برای ساخت Empty Set باید از `set()` استفاده کنیم:

```python
empty = set()
```

می توانیم Type آن را بررسی کنیم:

```python
print(type(empty))
```

خروجی:

```text
<class 'set'>
```

اما:

```python
empty = {}

print(type(empty))
```

خروجی:

```text
<class 'dict'>
```

این یکی از اشتباهات بسیار رایج در ابتدای یادگیری Python است.

---

## Set می تواند چند نوع داده داشته باشد

Set می تواند چند نوع مقدار مختلف را در خود نگه دارد، به شرطی که آن مقادیر **Hashable** باشند.

مثلا:

```python
data = {10, "Python", 3.14, True}
```

نمونه هایی از مقادیر معمول Hashable:

* Integer
* Float
* String
* Boolean
* Tupleهایی که خودشان شامل عناصر Hashable باشند

اما List را نمی توان مستقیما داخل Set قرار داد:

```python
numbers = {[1, 2], [3, 4]}
```

چون List یک Data Structure قابل تغییر (**Mutable**) و در نتیجه Unhashable است.

فعلا لازم نیست مفهوم Hashing را به صورت عمیق یاد بگیریم. بعدا هنگام بررسی `frozenset` و رفتار Setها بیشتر با این موضوع آشنا می شویم.

---

## چرا از Set استفاده می کنیم؟

Setها در چند موقعیت بسیار کاربردی هستند.

### حذف Duplicateها

مثلا:

```python
numbers = [1, 2, 2, 3, 3, 4]

unique_numbers = set(numbers)

print(unique_numbers)
```

در اینجا List به Set تبدیل شده و Duplicateها حذف می شوند.

---

### بررسی وجود یک عنصر

مثلا:

```python
languages = {"Python", "Java", "C++"}

print("Python" in languages)
```

نتیجه:

```text
True
```

این نوع Membership Checking یکی از کاربردهای مهم Setهاست.

---

### مقایسه مجموعه های مختلف

Setها عملیات مهمی برای مقایسه مجموعه ها دارند، از جمله:

* Union
* Intersection
* Difference
* Symmetric Difference

مثلا می توانیم دو گروه از دانش آموزان را با هم مقایسه کنیم و بفهمیم چه کسانی در هر دو گروه حضور دارند.

---

## Set در مقابل List و Tuple

حالا که List و Tuple و Dictionary را یاد گرفته ایم، باید جایگاه Set را هم به خوبی بشناسیم.

| ویژگی       | List                 | Tuple               | Set                   |
| ----------- | -------------------- | ------------------- | --------------------- |
| Ordered     | بله                  | بله                 | خیر                   |
| Indexing    | دارد                 | دارد                | ندارد                 |
| Duplicate   | مجاز                 | مجاز                | مجاز نیست             |
| Mutable     | بله                  | خیر                 | بله                   |
| کاربرد اصلی | مجموعه عمومی داده ها | مجموعه ثابت داده ها | نگه داری عناصر Unique |

مثلا:

```python
numbers_list = [1, 2, 2, 3]
numbers_tuple = (1, 2, 2, 3)
numbers_set = {1, 2, 2, 3}
```

List و Tuple مقدار `2` را دو بار نگه می دارند.

اما Set فقط یک `2` خواهد داشت.

---

## یک مثال کاربردی

فرض کنید نام دانش آموزانی را که در دو کلاس مختلف شرکت کرده اند ذخیره می کنیم.

دانش آموزان کلاس Python:

```python
python_students = {"Ali", "Sara", "Reza"}
```

دانش آموزان کلاس Java:

```python
java_students = {"Sara", "Reza", "Mina"}
```

حالا ممکن است بخواهیم جواب سوال هایی مثل این را پیدا کنیم:

* چه کسانی حداقل در یکی از کلاس ها شرکت کرده اند؟
* چه کسانی در هر دو کلاس شرکت کرده اند؟
* چه کسانی در Python بوده اند ولی در Java نبوده اند؟
* چه کسانی فقط در یکی از کلاس ها حضور داشته اند؟

Set دقیقا برای چنین مسئله هایی طراحی شده است.

در پارت های بعدی با **Set Operations** یاد می گیریم چگونه به این سوال ها پاسخ دهیم.

---

## نکات مهم

در این پارت این موارد را به خاطر بسپار:

1. Set برای نگه داری **عناصر Unique** استفاده می شود.
2. Duplicateها به صورت خودکار حذف می شوند.
3. Set از Indexing پشتیبانی نمی کند.
4. `{}` یک Empty Dictionary ایجاد می کند، نه Empty Set.
5. برای ساخت Empty Set باید از `set()` استفاده کنیم.
6. Set برای Membership Checking بسیار کاربردی است.
7. Set برای مقایسه و پردازش مجموعه های مختلف داده مناسب است.
8. عناصر Set باید **Hashable** باشند.
9. Union، Intersection، Difference و Symmetric Difference از مهم ترین عملیات Set هستند.

در پارت بعدی می رویم سراغ روش های مختلف **Creating Sets** در Python.
