## فهرست مطالب

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

---

# Sets — پارت ۲: ساخت Setها

## ساخت Setها

در پارت قبلی یاد گرفتیم Set چیست و چرا از آن استفاده می کنیم.

حالا می خواهیم روش های مختلف **Creating Sets** در Python را یاد بگیریم.

---

## 1. ساخت Set با آکولاد

ساده ترین روش برای ساخت Set این است که عناصر را داخل `{}` قرار دهیم:

```python
numbers = {1, 2, 3, 4}
```

Python این ساختار را به عنوان Set در نظر می گیرد.

می توانیم Type آن را بررسی کنیم:

```python
print(type(numbers))
```

خروجی:

```text
<class 'set'>
```

---

## 2. ساخت Set از Stringها

Set می تواند شامل String باشد:

```python
languages = {"Python", "Java", "C++"}
```

یا می توانیم نام چند نفر را در یک Set قرار دهیم:

```python
names = {"Ali", "Sara", "Reza"}
```

هر عنصر فقط یک بار در Set نگه داری می شود.

---

## 3. ساخت Set با چند نوع داده مختلف

یک Set می تواند شامل چند نوع داده Hashable باشد:

```python
data = {10, "Python", 3.14, True}
```

اما باید به خاطر داشته باشیم که عناصر Set باید Hashable باشند.

مثلا این کد معتبر نیست:

```python
data = {[1, 2], [3, 4]}
```

چون Listها Mutable و در نتیجه Unhashable هستند.

---

## 4. حذف خودکار Duplicateها

هنگام ساخت Set، مقادیر تکراری به صورت خودکار حذف می شوند:

```python
numbers = {1, 2, 2, 3, 3, 4}
```

Set نهایی شامل:

```text
{1, 2, 3, 4}
```

خواهد بود.

این عملیات همان لحظه ای که Python Set را ایجاد می کند انجام می شود.

بنابراین Set زمانی که فقط به مقادیر Unique نیاز داریم بسیار کاربردی است.

---

## 5. ساخت Empty Set

همان طور که در پارت قبلی دیدیم، `{}` یک Empty Set ایجاد نمی کند.

این کد:

```python
empty = {}
```

یک Dictionary خالی می سازد.

برای ساخت Empty Set باید از:

```python
empty = set()
```

استفاده کنیم.

Type آن را بررسی کنیم:

```python
print(type(empty))
```

خروجی:

```text
<class 'set'>
```

پس این تفاوت را حتما به خاطر بسپار:

```python
{}
```

یعنی:

```text
Empty Dictionary
```

اما:

```python
set()
```

یعنی:

```text
Empty Set
```

---

## 6. ساخت Set از List

می توانیم یک Set را از یک List موجود با استفاده از Constructor به نام `set()` ایجاد کنیم:

```python
numbers = [1, 2, 2, 3, 4, 4]

unique_numbers = set(numbers)

print(unique_numbers)
```

مقادیر Duplicate حذف می شوند.

به صورت مفهومی:

```text
List
    ↓
set()
    ↓
Set of Unique Elements
```

این یکی از رایج ترین کاربردهای `set()` است.

---

## 7. ساخت Set از Tuple

همین روش برای Tuple نیز کار می کند:

```python
numbers = (1, 2, 2, 3, 4)

unique_numbers = set(numbers)
```

حالا `unique_numbers` یک Set است که فقط مقادیر Unique را نگه می دارد.

---

## 8. ساخت Set از String

می توانیم یک String را نیز به `set()` بدهیم:

```python
letters = set("hello")

print(letters)
```

Set شامل کاراکترهای Unique موجود در String خواهد بود.

مثلا ممکن است نتیجه به شکل زیر باشد:

```text
{'h', 'e', 'l', 'o'}
```

دقت کنید که `l` دوم دوباره در Set قرار نگرفته است.

چون هر Character به عنوان یک عنصر جداگانه در نظر گرفته می شود و Set فقط عناصر Unique را نگه می دارد.

---

## 9. ساخت Set از Dictionary

وقتی یک Dictionary را به `set()` می دهیم، Python از **Keyهای Dictionary** استفاده می کند:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}

keys = set(student)

print(keys)
```

Set حاصل شامل:

```text
{'name', 'age', 'city'}
```

خواهد بود.

این نکته مهم است:

```python
set(dictionary)
```

با Keyهای Dictionary کار می کند، نه Valueها.

اگر بخواهیم از Valueها Set بسازیم، باید به صورت مشخص از `values()` استفاده کنیم:

```python
values = set(student.values())
```

---

## 10. ساخت Set از Dictionary Items

می توانیم با Itemهای Dictionary نیز کار کنیم:

```python
student = {
    "name": "Ali",
    "age": 20
}

items = set(student.items())
```

این کار یک Set شامل Tupleها ایجاد می کند:

```text
{
    ('name', 'Ali'),
    ('age', 20)
}
```

این کار زمانی امکان پذیر است که عناصر موجود در Tupleها Hashable باشند.

---

## 11. استفاده از `set()`

Constructor مربوط به `set()` زمانی بسیار کاربردی است که داده اولیه از قبل وجود داشته باشد:

```python
numbers = [1, 2, 3, 3, 4]

numbers_set = set(numbers)
```

همین الگو را می توانیم با چند نوع Iterable دیگر نیز استفاده کنیم:

```python
set(list_data)
set(tuple_data)
set(string_data)
set(dictionary_data)
```

نتیجه دقیق به عناصر موجود در Object اولیه بستگی دارد.

---

## 12. Set Comprehension

Python از **Set Comprehension** نیز پشتیبانی می کند.

ساختار کلی آن:

```python
{expression for item in iterable}
```

مثلا:

```python
numbers = {x for x in range(5)}
```

یک Set شامل:

```text
{0, 1, 2, 3, 4}
```

ایجاد می کند.

می توانیم شرط نیز قرار دهیم:

```python
even_numbers = {x for x in range(10) if x % 2 == 0}
```

نتیجه شامل اعداد زوج Unique خواهد بود.

فعلا روی مفهوم اصلی تمرکز کن:

```text
Iterable
    ↓
پردازش هر عنصر
    ↓
تولید یک مقدار
    ↓
قرار دادن مقدارها در Set
```

با پیش رفتن در مباحث Python استفاده از Comprehensionها برایمان راحت تر می شود.

---

## 13. تفاوت Set Comprehension و List Comprehension

Syntax این دو بسیار شبیه است.

List Comprehension:

```python
numbers = [x for x in range(5)]
```

Set Comprehension:

```python
numbers = {x for x in range(5)}
```

تفاوت ظاهری اصلی:

```text
[ ] → List
{ } → Set
```

اما یک نکته مهم را فراموش نکن:

```python
{}
```

به تنهایی یک Dictionary ایجاد می کند، نه Set.

وقتی داخل آکولاد یک Expression و ساختار Comprehension داشته باشیم، Python می تواند آن را به عنوان Set Comprehension تشخیص دهد.

---

## 14. انتخاب روش مناسب برای ساخت Set

بسته به شرایط، روش مناسب متفاوت است.

### اگر مقدارها را از قبل می دانیم

از این روش استفاده کن:

```python
numbers = {1, 2, 3, 4}
```

### اگر یک List داریم

```python
numbers = set(my_list)
```

### اگر یک Tuple داریم

```python
numbers = set(my_tuple)
```

### اگر یک String داریم

```python
letters = set("hello")
```

### اگر یک Empty Set می خواهیم

```python
numbers = set()
```

### اگر می خواهیم مقدارها را به صورت Dynamic تولید کنیم

از Set Comprehension استفاده می کنیم:

```python
numbers = {x for x in range(10)}
```

---

## اشتباهات رایج مبتدی ها

### اشتباه ۱ — استفاده از `{}` برای Empty Set

اشتباه:

```python
numbers = {}
```

درست:

```python
numbers = set()
```

---

### اشتباه ۲ — انتظار داشتن Duplicateها

```python
numbers = {1, 1, 2, 2, 3}
```

این کد پنج عنصر ایجاد نمی کند.

Set فقط سه عنصر Unique خواهد داشت.

---

### اشتباه ۳ — قرار دادن List داخل Set

این کد معتبر نیست:

```python
numbers = {[1, 2], [3, 4]}
```

چون Listها Unhashable هستند.

---

### اشتباه ۴ — فرض کردن ترتیب مشخص برای Set

نباید کدی بنویسیم که به یک ترتیب خاص در Set وابسته باشد:

```python
numbers = {10, 20, 30}
```

هدف Set نگه داری عناصر Unique و انجام Set Operations است، نه دسترسی Position-based.

---

## نکات مهم

بعد از این پارت باید این موارد را بلد باشی:

1. می توانیم Set را با `{}` و قرار دادن عناصر داخل آن بسازیم.
2. Empty Set باید با `set()` ساخته شود.
3. `set()` می تواند List، Tuple، String و سایر Iterableها را به Set تبدیل کند.
4. Duplicateها به صورت خودکار حذف می شوند.
5. اگر Dictionary را به `set()` بدهیم، Keyهای آن به Set تبدیل می شوند.
6. برای ساخت Set از Valueهای Dictionary می توانیم از `set(dictionary.values())` استفاده کنیم.
7. Dictionary Items نیز در صورتی که Hashable باشند می توانند به Set تبدیل شوند.
8. Set Comprehension روش کوتاهی برای تولید Set است.
9. عناصر Set باید Hashable باشند.
10. روش ساخت Set را باید بر اساس نوع و هدف داده اولیه انتخاب کنیم.

در پارت بعدی یاد می گیریم چطور بعد از ساخت Set، **Element جدید به آن اضافه کنیم**.

---

# Sets — پارت ۳: اضافه کردن عناصر به Set

## اضافه کردن عناصر به Set

در پارت قبلی روش های مختلف ساخت Set در Python را یاد گرفتیم.

حالا می خواهیم یاد بگیریم چطور **Element جدید به یک Set موجود اضافه کنیم**.

مهم ترین متدی که برای این کار استفاده می کنیم:

```python
set.add()
```

---

## 1. استفاده از `add()`

متد `add()` یک Element را به Set اضافه می کند.

```python
numbers = {1, 2, 3}

numbers.add(4)

print(numbers)
```

حالا Set شامل `4` نیز می شود:

```text
{1, 2, 3, 4}
```

Syntax آن:

```python
set_name.add(element)
```

مثلا:

```python
languages = {"Python", "Java"}

languages.add("C++")
```

حالا Set شامل این موارد است:

```text
{"Python", "Java", "C++"}
```

---

## 2. اضافه کردن یک Element موجود

اگر Elementی که می خواهیم اضافه کنیم از قبل در Set وجود داشته باشد چه اتفاقی می افتد؟

```python
numbers = {1, 2, 3}

numbers.add(2)

print(numbers)
```

هیچ تغییری ایجاد نمی شود.

Set همچنان:

```text
{1, 2, 3}
```

خواهد بود.

دلیلش این است که Set فقط **Elementهای Unique** را نگه داری می کند.

پس `add()` باعث ایجاد Duplicate نمی شود.

---

## 3. اضافه کردن Elementها به صورت جداگانه

`add()` در هر بار اجرا فقط **یک Element** اضافه می کند.

```python
numbers = {1, 2}

numbers.add(3)
numbers.add(4)
numbers.add(5)

print(numbers)
```

Set نهایی شامل:

```text
{1, 2, 3, 4, 5}
```

خواهد بود.

هر بار اجرای `add()` یک Element اضافه می کند.

---

## 4. اضافه کردن String

می توانیم یک String را به عنوان یک Element اضافه کنیم:

```python
languages = {"Python", "Java"}

languages.add("JavaScript")
```

کل String `"JavaScript"` یک Element در Set است.

یعنی کاراکترهای آن به صورت جداگانه اضافه نمی شوند.

مثلا:

```python
languages.add("Go")
```

حالا `"Go"` نیز یک Element جداگانه است.

---

## 5. اضافه کردن Tuple

چون Tuple می تواند Hashable باشد، می توانیم یک Tuple را به Set اضافه کنیم:

```python
data = {1, 2, 3}

data.add((4, 5))

print(data)
```

در اینجا Tuple `(4, 5)` به عنوان **یک Element** در Set قرار می گیرد.

به صورت مفهومی:

```text
Set
 ├── 1
 ├── 2
 ├── 3
 └── (4, 5)
```

---

## 6. تلاش برای اضافه کردن List

نمی توانیم یک List را مستقیما به Set اضافه کنیم:

```python
numbers = {1, 2, 3}

numbers.add([4, 5])
```

این کد باعث Error می شود، چون Listها **Unhashable** هستند.

معمولا خطایی شبیه این دریافت می کنیم:

```text
TypeError: unhashable type: 'list'
```

این موضوع مستقیما به مفهوم Hashable که در پارت قبلی معرفی کردیم مربوط است.

---

## 7. `add()` Set جدید را بر نمی گرداند

یک نکته بسیار مهم درباره `add()` این است که این متد Set موجود را **در همان Object تغییر می دهد**.

یعنی Set را درجا تغییر می دهد.

اما Set تغییر یافته را به عنوان Return Value بر نمی گرداند.

مثلا:

```python
numbers = {1, 2, 3}

result = numbers.add(4)

print(result)
```

خروجی:

```text
None
```

اما خود Set تغییر کرده است:

```python
print(numbers)
```

خروجی:

```text
{1, 2, 3, 4}
```

پس این نکته را به خاطر بسپار:

```text
add()
  ↓
Set را تغییر می دهد
  ↓
None بر می گرداند
```

این موضوع یکی از مواردی است که ممکن است در ابتدای کار باعث سردرگمی شود.

---

## 8. اضافه کردن User Input

می توانیم مقدار وارد شده توسط کاربر را نیز به Set اضافه کنیم:

```python
names = set()

name = input("Enter your name: ")

names.add(name)

print(names)
```

نام وارد شده به Set اضافه می شود.

چون Set فقط مقادیر Unique را نگه داری می کند، اگر همان نام دوباره وارد شود Duplicate ایجاد نمی شود.

مثلا اگر این نام ها را اضافه کنیم:

```text
Ali
Sara
Ali
Reza
```

Set فقط شامل:

```text
{"Ali", "Sara", "Reza"}
```

خواهد بود.

---

## 9. استفاده از `add()` در Loop

می توانیم `add()` را داخل Loop نیز استفاده کنیم:

```python
numbers = set()

for number in range(1, 6):
    numbers.add(number)

print(numbers)
```

نتیجه شامل:

```text
{1, 2, 3, 4, 5}
```

خواهد بود.

این روش زمانی کاربردی است که مقدارها به صورت Dynamic تولید می شوند.

---

## 10. تفاوت `add()` و `set()`

این دو کاربرد کاملا متفاوتی دارند.

`set()` معمولا برای **ساختن یا تبدیل داده به Set** استفاده می شود:

```python
numbers = set([1, 2, 3])
```

اما `add()` برای **اضافه کردن یک Element به Set موجود** استفاده می شود:

```python
numbers.add(4)
```

به این شکل به خاطر بسپار:

```text
set()
  ↓
Create / Convert

add()
  ↓
Add one element
```

---

## 11. تفاوت `add()` و `update()`

در ادامه با `update()` نیز کار خواهیم کرد، پس بهتر است از همین حالا تفاوت آن را بدانیم.

`add()` یک Element اضافه می کند:

```python
numbers = {1, 2}

numbers.add(3)
```

اما `update()` می تواند چند Element را از یک Iterable اضافه کند:

```python
numbers = {1, 2}

numbers.update([3, 4, 5])
```

نتیجه:

```text
{1, 2, 3, 4, 5}
```

فعلا این تفاوت را به خاطر بسپار:

```text
add()
→ یک Element

update()
→ چند Element
```

در ادامه هنگام کار با تغییر Setها، `update()` را دقیق تر بررسی می کنیم.

---

## اشتباهات رایج مبتدی ها

### اشتباه ۱ — انتظار داشتن Return شدن Set از `add()`

اشتباه:

```python
numbers = {1, 2, 3}

numbers = numbers.add(4)
```

بعد از این Assignment، مقدار `numbers` برابر `None` می شود.

روش درست:

```python
numbers = {1, 2, 3}

numbers.add(4)
```

---

### اشتباه ۲ — اضافه کردن List

این کد اشتباه است:

```python
numbers.add([4, 5])
```

چون Listها Unhashable هستند.

اگر می خواهی `(4, 5)` به عنوان یک Element اضافه شود، می توانی از Tuple استفاده کنی:

```python
numbers.add((4, 5))
```

---

### اشتباه ۳ — انتظار داشتن Duplicate

```python
numbers = {1, 2, 3}

numbers.add(3)
numbers.add(3)
```

Set همچنان فقط یک `3` خواهد داشت.

---

## نکات مهم

بعد از این پارت باید این موارد را بلد باشی:

1. `add()` یک Element را به Set موجود اضافه می کند.
2. اگر Element از قبل وجود داشته باشد، Duplicate ایجاد نمی شود.
3. `add()` Set را درجا تغییر می دهد.
4. `add()` مقدار `None` را بر می گرداند.
5. Objectهای Hashable مثل Tuple می توانند به Set اضافه شوند.
6. Listها را نمی توان مستقیما به Set اضافه کرد، چون Unhashable هستند.
7. می توان از `add()` در Loop و همراه User Input استفاده کرد.
8. `set()` بیشتر برای ساخت یا تبدیل Set استفاده می شود، در حالی که `add()` برای اضافه کردن یک Element است.
9. `add()` و `update()` کاربرد متفاوتی دارند.

---

## تمرین ها

### سوال ۱

Set نهایی `numbers` چه مقادیری خواهد داشت؟

```python
numbers = {1, 2, 3}

numbers.add(3)
numbers.add(4)
numbers.add(4)
numbers.add(5)
```

---

### سوال ۲

کد زیر را اصلاح کن تا `(10, 20)` به عنوان **یک Element** به Set اضافه شود:

```python
data = {1, 2, 3}

data.add([10, 20])
```

---

### سوال ۳

چه چیزی چاپ می شود؟

```python
numbers = {1, 2}

result = numbers.add(3)

print(result)
print(numbers)
```

توضیح بده چرا دو خروجی با هم متفاوت هستند.

---

## سوال جامع Setها

یک برنامه بنویس که با این Set شروع شود:

```python
students = {"Ali", "Sara", "Reza"}
```

سپس:

1. `"Mina"` را به Set اضافه کن.
2. دوباره `"Ali"` را اضافه کن.
3. نام های `"Omid"` و `"Nima"` را یکی یکی با `add()` اضافه کن.
4. Set نهایی را چاپ کن.
5. توضیح بده چرا `"Ali"` فقط یک بار در Set وجود دارد.
6. مقدار Return شده از یکی از اجرای `add()` را داخل یک متغیر ذخیره کن و توضیح بده این مقدار چیست.

هدف این سوال این است که مفاهیمی را که تا اینجا یاد گرفته ایم با هم استفاده کنی:

**Creating Sets + Unique Elements + Hashable Elements + Adding Elements**

---

# Sets — پارت ۴: حذف عناصر از Set

در پارت قبلی یاد گرفتیم چطور با استفاده از `add()` عناصر جدید به Set اضافه کنیم.

حالا می خواهیم روش های مختلف **حذف عناصر از Set** را یاد بگیریم.

Python چند متد مختلف برای این کار دارد:

* `remove()`
* `discard()`
* `pop()`
* `clear()`

با اینکه همه این متدها Set را تغییر می دهند، رفتارشان با یکدیگر متفاوت است.

---

## 1. استفاده از `remove()`

متد `remove()` یک Element مشخص را از Set حذف می کند.

```python
numbers = {1, 2, 3, 4}

numbers.remove(3)

print(numbers)
```

نتیجه:

```text
{1, 2, 4}
```

Syntax:

```python
set_name.remove(element)
```

---

## 2. اگر Element وجود نداشته باشد چه می شود؟

این یکی از مهم ترین تفاوت های `remove()` و `discard()` است.

اگر Element مورد نظر در Set وجود نداشته باشد:

```python
numbers = {1, 2, 3}

numbers.remove(5)
```

Python یک `KeyError` ایجاد می کند.

مثلا:

```text
KeyError: 5
```

پس بهتر است زمانی از `remove()` استفاده کنیم که انتظار داریم Element مورد نظر واقعا در Set وجود داشته باشد.

---

## 3. استفاده از `discard()`

متد `discard()` نیز یک Element مشخص را حذف می کند:

```python
numbers = {1, 2, 3, 4}

numbers.discard(3)

print(numbers)
```

نتیجه:

```text
{1, 2, 4}
```

اما یک تفاوت مهم دارد.

اگر Element وجود نداشته باشد:

```python
numbers = {1, 2, 3}

numbers.discard(5)

print(numbers)
```

هیچ اتفاقی نمی افتد.

Error ایجاد نمی شود و Set همچنان:

```text
{1, 2, 3}
```

خواهد بود.

---

## 4. تفاوت `remove()` و `discard()`

این تفاوت را حتما به خاطر بسپار:

| متد         | Element وجود دارد | Element وجود ندارد      |
| ----------- | ----------------- | ----------------------- |
| `remove()`  | حذف می شود        | `KeyError` ایجاد می شود |
| `discard()` | حذف می شود        | هیچ کاری انجام نمی شود  |

به صورت ساده:

```text
remove()
→ "انتظار دارم این Element وجود داشته باشد."

discard()
→ "اگر وجود داشت حذفش کن."
```

برای کدهای مبتدی، `discard()` زمانی مفید است که نمی خواهیم نبودن یک Element باعث Error شود.

---

## 5. استفاده از `pop()`

متد `pop()` یک Element را از Set حذف می کند و **همان Element حذف شده را بر می گرداند**.

```python
numbers = {10, 20, 30, 40}

value = numbers.pop()

print(value)
print(numbers)
```

Element حذف شده داخل `value` ذخیره می شود.

یک نکته بسیار مهم:

**Setها Unordered هستند، بنابراین نباید انتظار داشته باشیم `pop()` یک Element مشخص را حذف کند.**

نباید فرض کنیم که `pop()` همیشه کوچک ترین، بزرگ ترین، اولی یا آخری را حذف می کند.

Element حذف شده را باید به عنوان یک Element نامشخص در نظر بگیریم.

---

## 6. `pop()` Element حذف شده را بر می گرداند

برخلاف `remove()` و `discard()`، متد `pop()` Element حذف شده را به ما می دهد.

```python
numbers = {1, 2, 3}

removed = numbers.pop()

print(removed)
print(numbers)
```

`print()` اول Element حذف شده را نمایش می دهد.

`print()` دوم Set باقی مانده را نمایش می دهد.

به صورت مفهومی:

```text
Set
  ↓
pop()
  ↓
حذف یک Element
  ↓
برگرداندن همان Element
```

---

## 7. `pop()` روی Empty Set

اگر روی یک Empty Set از `pop()` استفاده کنیم:

```python
numbers = set()

numbers.pop()
```

Python یک `KeyError` ایجاد می کند.

پس اگر احتمال می دهیم Set خالی باشد، بهتر است قبل از `pop()` بررسی کنیم که Set شامل Element هست یا نه.

مثلا:

```python
if numbers:
    value = numbers.pop()
```

---

## 8. استفاده از `clear()`

متد `clear()` **تمام عناصر Set** را حذف می کند.

```python
numbers = {1, 2, 3, 4}

numbers.clear()

print(numbers)
```

نتیجه:

```text
set()
```

خود Set همچنان وجود دارد، اما دیگر هیچ Elementی داخل آن نیست.

مثلا:

```python
numbers = {1, 2, 3}

numbers.clear()

print(type(numbers))
```

Type همچنان:

```text
<class 'set'>
```

است.

---

## 9. تفاوت `clear()` و ساخت Set جدید

بین خالی کردن یک Set و ساختن یک Empty Set جدید تفاوت وجود دارد.

با `clear()`:

```python
numbers = {1, 2, 3}

numbers.clear()
```

همان Set موجود خالی می شود.

اما با Assignment:

```python
numbers = {1, 2, 3}

numbers = set()
```

متغیر `numbers` به یک Set جدید اشاره می کند.

در سطح مقدماتی هر دو در نهایت باعث می شوند `numbers` خالی باشد، اما رفتار داخلی آن ها متفاوت است.

فعلا این تفاوت را به خاطر بسپار:

```text
clear()
→ خالی کردن Set موجود

set()
→ ساخت یک Empty Set جدید
```

---

## 10. حذف Element همراه با بررسی وجود آن

گاهی می خواهیم یک Element مشخص را فقط در صورتی حذف کنیم که در Set وجود داشته باشد.

یک روش:

```python
numbers = {1, 2, 3, 4}

if 3 in numbers:
    numbers.remove(3)
```

روش ساده تر:

```python
numbers.discard(3)
```

به همین دلیل `discard()` در بعضی موقعیت ها بسیار کاربردی است.

---

## 11. حذف چند Element

می توانیم متدهای حذف را چند بار اجرا کنیم:

```python
numbers = {1, 2, 3, 4, 5}

numbers.remove(1)
numbers.remove(2)
numbers.discard(5)

print(numbers)
```

عناصر باقی مانده:

```text
{3, 4}
```

هر بار اجرای متد Set را تغییر می دهد.

---

## 12. نکته مهم: هنگام Iteration، Set را تغییر نده

یک اشتباه رایج این است که بخواهیم هنگام Iteration روی همان Set، عناصر آن را حذف کنیم:

```python
numbers = {1, 2, 3, 4, 5}

for number in numbers:
    if number % 2 == 0:
        numbers.remove(number)
```

این کار می تواند باعث Error زیر شود:

```text
RuntimeError: Set changed size during iteration
```

فعلا از تغییر مستقیم Set در هنگام Iteration خود داری کن.

در مباحث پیشرفته تر روش های امن تر برای Filter و Transform کردن Collectionها را یاد می گیریم.

---

## 13. انتخاب متد مناسب

یک خلاصه کاربردی:

### زمانی از `remove()` استفاده کن که:

انتظار داری Element وجود داشته باشد و اگر وجود نداشت می خواهی Python به تو اطلاع دهد.

```python
numbers.remove(3)
```

### زمانی از `discard()` استفاده کن که:

می خواهی Element را در صورت وجود حذف کنی و اگر وجود نداشت Error ایجاد نشود.

```python
numbers.discard(3)
```

### زمانی از `pop()` استفاده کن که:

می خواهی یک Element نامشخص را حذف کنی و خود Element حذف شده را دریافت کنی.

```python
value = numbers.pop()
```

### زمانی از `clear()` استفاده کن که:

می خواهی **تمام عناصر** را حذف کنی.

```python
numbers.clear()
```

---

## اشتباهات رایج مبتدی ها

### اشتباه ۱ — فرض کردن اینکه `remove()` برای Elementهای غیر موجود Error نمی دهد

```python
numbers = {1, 2, 3}

numbers.remove(10)
```

این کد `KeyError` ایجاد می کند.

اگر نبودن Element نباید باعث Error شود، می توانیم از `discard()` استفاده کنیم.

---

### اشتباه ۲ — فرض کردن اینکه `pop()` اولین Element را حذف می کند

Setها Index ندارند و یک First Element مشخص برای آن ها تعریف نشده است.

پس این فرض اشتباه است:

```python
numbers = {10, 20, 30}

numbers.pop()
```

نباید فرض کنیم `10` حذف می شود.

---

### اشتباه ۳ — انتظار داشتن Set باقی مانده از `pop()`

`pop()` خود Element حذف شده را بر می گرداند، نه Set باقی مانده را.

```python
removed = numbers.pop()
```

---

### اشتباه ۴ — اشتباه گرفتن `clear()` و `discard()`

`discard()` یک Element مشخص را حذف می کند:

```python
numbers.discard(3)
```

اما `clear()` همه چیز را حذف می کند:

```python
numbers.clear()
```

---

## نکات مهم

بعد از این پارت باید این موارد را بلد باشی:

1. `remove()` یک Element مشخص را حذف می کند.
2. اگر Element وجود نداشته باشد، `remove()` باعث `KeyError` می شود.
3. `discard()` یک Element مشخص را حذف می کند و اگر Element وجود نداشته باشد Error ایجاد نمی کند.
4. `pop()` یک Element نامشخص را حذف می کند و همان Element را بر می گرداند.
5. `pop()` روی Empty Set باعث `KeyError` می شود.
6. `clear()` تمام عناصر Set را حذف می کند.
7. چون Setها Unordered هستند، نباید روی Element حذف شده توسط `pop()` حساب خاصی باز کنیم.
8. نباید هنگام Iteration، Set را مستقیما تغییر دهیم.

---

## تمرین ها

### سوال ۱

وقتی این کد اجرا شود چه اتفاقی می افتد؟

```python
numbers = {1, 2, 3}

numbers.remove(5)
```

اگر بخواهی برنامه بدون Error ادامه پیدا کند، کد را چطور تغییر می دهی؟

---

### سوال ۲

تفاوت این دو را توضیح بده:

```python
numbers.remove(10)
```

و:

```python
numbers.discard(10)
```

اگر `10` داخل Set وجود نداشته باشد، هر کدام چه رفتاری دارند؟

---

### سوال ۳

کد زیر چه چیزی را تضمین می کند؟

```python
numbers = {1, 2, 3, 4, 5}

removed = numbers.pop()

print(removed)
print(numbers)
```

آیا می توانی دقیقا پیش بینی کنی چه عددی داخل `removed` قرار می گیرد؟

---

## سوال جامع Setها

برنامه ای بنویس که با Set زیر شروع شود:

```python
students = {"Ali", "Sara", "Reza", "Mina", "Omid"}
```

سپس این کارها را انجام بده:

1. `"Sara"` را با استفاده از `remove()` حذف کن.
2. دوباره `"Sara"` را حذف کن، اما این بار مطمئن شو که برنامه Error ندهد.
3. با استفاده از `pop()` یکی از دانش آموزان باقی مانده را حذف کن و نام حذف شده را داخل یک متغیر قرار بده.
4. نام حذف شده و Set باقی مانده را چاپ کن.
5. در نهایت تمام دانش آموزان باقی مانده را با `clear()` حذف کن.
6. Set نهایی را چاپ کن.

در راه حل خود تفاوت این چهار متد را توضیح بده:

`remove()` → `discard()` → `pop()` → `clear()`

همچنین توضیح بده هر کدام در چه شرایطی مناسب تر هستند.

---

# Sets — پارت ۵: بررسی وجود یک Element در Set

در پارت قبلی یاد گرفتیم چطور عناصر را از Set حذف کنیم.

حالا می خواهیم یاد بگیریم چطور **بررسی کنیم که آیا یک Element داخل Set وجود دارد یا نه**.

مهم ترین چیزی که برای این کار استفاده می کنیم:

```python
in
```

همچنین با این موارد کار می کنیم:

* `in`
* `not in`
* استفاده از Membership Check همراه `if`
* بررسی User Input
* کاربرد Membership Check در Set
* تفاوت بررسی وجود Element در Set و List

---

## 1. استفاده از `in`

عملگر `in` بررسی می کند که آیا یک Element داخل Set وجود دارد یا نه.

```python
numbers = {1, 2, 3, 4, 5}

print(3 in numbers)
```

خروجی:

```text
True
```

چون `3` داخل Set وجود دارد.

اگر Elementی را بررسی کنیم که وجود ندارد:

```python
print(10 in numbers)
```

خروجی:

```text
False
```

پس:

```text
element in set
→ True یا False
```

---

## 2. استفاده از `not in`

با `not in` بررسی می کنیم که یک Element **داخل Set وجود ندارد**.

```python
numbers = {1, 2, 3, 4, 5}

print(10 not in numbers)
```

خروجی:

```text
True
```

چون `10` داخل Set وجود ندارد.

برای Element موجود:

```python
print(3 not in numbers)
```

خروجی:

```text
False
```

به خاطر بسپار:

```text
in
→ بررسی وجود

not in
→ بررسی عدم وجود
```

---

## 3. استفاده از Membership Check با `if`

Membership Check در کنار `if` بسیار کاربردی است.

```python
students = {"Ali", "Sara", "Reza"}

if "Ali" in students:
    print("Ali is in the Set")
```

خروجی:

```text
Ali is in the Set
```

اگر دانش آموز وجود نداشته باشد:

```python
if "Mina" in students:
    print("Mina is in the Set")
```

چون شرط `False` است، چیزی چاپ نمی شود.

می توانیم از `else` نیز استفاده کنیم:

```python
students = {"Ali", "Sara", "Reza"}

if "Mina" in students:
    print("Mina is in the Set")
else:
    print("Mina is not in the Set")
```

خروجی:

```text
Mina is not in the Set
```

---

## 4. بررسی User Input

Membership Check هنگام کار با User Input بسیار کاربردی است.

```python
allowed_users = {"Ali", "Sara", "Reza"}

username = input("Enter your username: ")

if username in allowed_users:
    print("Access granted")
else:
    print("Access denied")
```

در اینجا Set مانند یک مجموعه از مقدارهای مجاز عمل می کند.

اگر کاربر وارد کند:

```text
Sara
```

نتیجه:

```text
Access granted
```

اما اگر وارد کند:

```text
Mina
```

نتیجه:

```text
Access denied
```

---

## 5. بررسی قبل از حذف

می توانیم Membership Check را با حذف نیز ترکیب کنیم.

مثلا:

```python
numbers = {1, 2, 3, 4}

if 3 in numbers:
    numbers.remove(3)

print(numbers)
```

خروجی:

```text
{1, 2, 4}
```

این روش باعث می شود `remove()` زمانی اجرا شود که Element مورد نظر واقعا وجود دارد.

البته می توانستیم از `discard()` نیز استفاده کنیم:

```python
numbers.discard(3)
```

اما یادگیری Membership Check مهم است، چون `in` فقط برای حذف کردن کاربرد ندارد و در تصمیم گیری های مختلف استفاده می شود.

---

## 6. بررسی قبل از اضافه کردن

می توانیم قبل از اضافه کردن نیز وجود Element را بررسی کنیم:

```python
numbers = {1, 2, 3}

if 4 not in numbers:
    numbers.add(4)

print(numbers)
```

نتیجه:

```text
{1, 2, 3, 4}
```

در Setها این بررسی معمولا برای جلوگیری از Duplicate لازم نیست، چون Set به صورت خود کار Duplicateها را حذف می کند.

مثلا:

```python
numbers.add(4)
```

حتی اگر `4` از قبل وجود داشته باشد، مشکلی ایجاد نمی کند.

با این حال Membership Check زمانی مهم است که برنامه باید بر اساس وجود یا عدم وجود یک Element تصمیم بگیرد.

---

## 7. Membership Check مقدار Boolean بر می گرداند

نتیجه `in` و `not in` همیشه یک Boolean است:

```python
numbers = {1, 2, 3}

result = 2 in numbers

print(result)
print(type(result))
```

خروجی:

```text
True
<class 'bool'>
```

پس:

```python
2 in numbers
```

یک Expression است که در نهایت یکی از این دو مقدار را تولید می کند:

```text
True
```

یا:

```text
False
```

بنابراین می توانیم از آن هر جایی که یک Boolean Condition لازم است استفاده کنیم.

---

## 8. بررسی Stringها

Membership Check برای Stringهایی که داخل Set هستند نیز کار می کند.

```python
languages = {"Python", "Java", "C++"}

print("Python" in languages)
```

خروجی:

```text
True
```

اما:

```python
print("python" in languages)
```

خروجی:

```text
False
```

چون مقایسه Stringها به حروف بزرگ و کوچک حساس است.

این دو مقدار متفاوت هستند:

```text
"Python"
"python"
```

پس هنگام بررسی User Input باید به این موضوع دقت کنیم.

---

## 9. بررسی Data Typeهای مختلف

یک Set می تواند شامل Data Typeهای مختلف Hashable باشد.

مثلا:

```python
data = {1, "Python", 3.14, (10, 20)}

print(1 in data)
print("Python" in data)
print(3.14 in data)
print((10, 20) in data)
```

نتیجه هر بررسی:

```text
True
```

خواهد بود.

Valueای که بررسی می کنیم باید با یک Element موجود در Set مطابقت داشته باشد.

مثلا:

```python
print("1" in data)
```

نتیجه:

```text
False
```

است.

چون `"1"` یک String است، در حالی که `1` یک Integer است.

---

## 10. بررسی `None`

مقدار `None` نیز می تواند داخل Set قرار بگیرد و بررسی شود:

```python
data = {1, 2, None}

print(None in data)
```

خروجی:

```text
True
```

این موضوع هنگام کار با Collectionهایی که ممکن است مقدار خالی یا Optional داشته باشند کاربردی است.

---

## 11. Membership Check با `if / elif / else`

می توانیم چند Membership Check انجام دهیم:

```python
commands = {"start", "stop", "pause"}

command = input("Enter a command: ")

if command in commands:
    print("Valid command")
else:
    print("Unknown command")
```

این الگو زمانی کاربرد دارد که برنامه یک مجموعه مشخص از مقدارهای مجاز داشته باشد.

مثلا:

```text
start
stop
pause
```

مجاز هستند و Commandهای دیگر رد می شوند.

---

## 12. تفاوت Membership در Set و List

عملگر `in` هم برای Set و هم برای List کار می کند:

```python
numbers_list = [1, 2, 3, 4, 5]
numbers_set = {1, 2, 3, 4, 5}

print(4 in numbers_list)
print(4 in numbers_set)
```

هر دو خروجی:

```text
True
```

خواهند داشت.

اما از نظر Performance یک تفاوت مهم وجود دارد.

در List، Python معمولا عناصر را یکی یکی بررسی می کند.

اما Set برای Membership Check از Hashing استفاده می کند و برای این نوع بررسی بسیار مناسب است.

به صورت مفهومی:

```text
List
→ جست و جو بین عناصر

Set
→ جست و جوی مبتنی بر Hash
```

در سطح مقدماتی مهم ترین نکته این است:

> Set زمانی بسیار کاربردی است که هدف اصلی ما بررسی سریع وجود یک مقدار در یک Collection باشد.

فعلا لازم نیست جزئیات پیاده سازی آن را حفظ کنی.

---

## 13. Membership Check، Set را تغییر نمی دهد

عملگر `in` فقط Set را بررسی می کند.

هیچ Elementی را اضافه یا حذف نمی کند.

```python
numbers = {1, 2, 3}

print(2 in numbers)

print(numbers)
```

خروجی:

```text
True
{1, 2, 3}
```

Set بدون تغییر باقی می ماند.

این رفتار با متدهایی مثل:

```python
numbers.add(4)
numbers.remove(2)
numbers.clear()
```

متفاوت است، چون آن ها Set را تغییر می دهند.

---

## 14. یک مثال کاربردی

فرض کن یک Set از Userهای ثبت نام شده داریم:

```python
registered_users = {
    "Ali",
    "Sara",
    "Reza",
    "Mina"
}
```

می توانیم بررسی کنیم که آیا یک User ثبت نام شده است یا نه:

```python
username = input("Enter your username: ")

if username in registered_users:
    print("User is registered")
else:
    print("User is not registered")
```

این یک الگوی بسیار رایج در برنامه های واقعی است.

از همین ایده می توان برای این موارد استفاده کرد:

* Commandهای مجاز
* Categoryهای معتبر
* Userهای ثبت نام شده
* Userهای Block شده
* Optionهای قابل انتخاب
* IDهای Unique
* Permissionها
* Valueهای پشتیبانی شده

---

## اشتباهات رایج مبتدی ها

### اشتباه ۱ — اشتباه گرفتن `in` با `add()`

اشتباه:

```python
numbers.in(3)
```

`in` یک Operator است، نه Method.

روش درست:

```python
3 in numbers
```

---

### اشتباه ۲ — تصور کردن اینکه `in` Set را تغییر می دهد

این:

```python
3 in numbers
```

فقط بررسی می کند که `3` وجود دارد یا نه.

هیچ Elementی اضافه یا حذف نمی شود.

---

### اشتباه ۳ — فراموش کردن Case Sensitivity

```python
languages = {"Python"}

print("python" in languages)
```

خروجی:

```text
False
```

چون `"Python"` و `"python"` متفاوت هستند.

---

### اشتباه ۴ — اشتباه گرفتن Value و String Representation

```python
numbers = {1, 2, 3}

print("1" in numbers)
```

خروجی:

```text
False
```

چون:

```text
1
```

یک Integer است، در حالی که:

```text
"1"
```

یک String است.

---

## نکات مهم

بعد از این پارت باید این موارد را بلد باشی:

1. `in` بررسی می کند که یک Element داخل Set وجود دارد یا نه.
2. `not in` بررسی می کند که یک Element داخل Set وجود ندارد.
3. هر دو مقدار Boolean یعنی `True` یا `False` بر می گردانند.
4. Membership Check معمولا همراه `if` استفاده می شود.
5. Membership Check خود Set را تغییر نمی دهد.
6. بررسی Membership برای تشخیص وجود یک مقدار در Collection بسیار کاربردی است.
7. بررسی Stringها به حروف بزرگ و کوچک حساس است.
8. Type مقدار در Membership Check اهمیت دارد.
9. Setها به دلیل استفاده از Hashing برای Membership Check بسیار مناسب هستند.

---

## تمرین ها

### سوال ۱

این کد چه چیزی چاپ می کند؟

```python
numbers = {10, 20, 30}

print(20 in numbers)
print(50 in numbers)
print(10 not in numbers)
```

---

### سوال ۲

برنامه ای بنویس که از کاربر یک Language دریافت کند و بررسی کند آیا داخل این Set وجود دارد یا نه:

```python
languages = {"Python", "Java", "C++"}
```

اگر وجود داشت:

```text
Supported language
```

و اگر وجود نداشت:

```text
Unsupported language
```

را چاپ کن.

---

### سوال ۳

چرا کد زیر `False` چاپ می کند؟

```python
numbers = {1, 2, 3}

print("1" in numbers)
```

تفاوت `1` و `"1"` را توضیح بده.

---

## سوال جامع Setها

یک برنامه کوچک برای کنترل دسترسی بنویس که از Set زیر استفاده کند:

```python
allowed_users = {"Ali", "Sara", "Reza", "Mina"}
```

برنامه باید:

1. از کاربر یک Username دریافت کند.
2. بررسی کند Username داخل `allowed_users` وجود دارد یا نه.
3. اگر وجود داشت `"Access granted"` را چاپ کند.
4. در غیر این صورت `"Access denied"` را چاپ کند.
5. اگر دسترسی داده شد، همان Username را با `remove()` از Set حذف کند.
6. Set به روز شده را چاپ کند.
7. دوباره یک Username دریافت کند و با استفاده از `not in` بررسی کند که آیا آن Username دیگر داخل Set نیست.

در راه حل خود مفاهیم زیر را با هم استفاده کن:

**Creating Sets → Adding Elements → Removing Elements → `in` → `not in` → Boolean Conditions**

---

# Sets — پارت ۶: طول Set و شمارش عناصر

در پارت قبلی یاد گرفتیم چطور با استفاده از `in` و `not in` بررسی کنیم که یک Element داخل Set وجود دارد یا نه.

حالا می خواهیم یاد بگیریم چطور **تعداد عناصر یک Set را بشماریم**.

تابع اصلی برای این کار:

```python
len()
```

است.

---

## 1. استفاده از `len()` با Set

تابع `len()` تعداد عناصر موجود در Set را بر می گرداند.

```python
numbers = {10, 20, 30, 40}

print(len(numbers))
```

خروجی:

```text
4
```

Syntax:

```python
len(set_name)
```

---

## 2. Set فقط عناصر Unique را می شمارد

چون Setها Duplicateها را نگه داری نمی کنند، `len()` فقط تعداد عناصر Unique را حساب می کند.

```python
numbers = {1, 2, 2, 3, 3, 3}

print(len(numbers))
```

Set در عمل:

```text
{1, 2, 3}
```

است.

پس خروجی:

```text
3
```

خواهد بود.

این یکی از تفاوت های مهم Set و List است.

مثلا:

```python
numbers_list = [1, 2, 2, 3, 3, 3]
numbers_set = {1, 2, 2, 3, 3, 3}

print(len(numbers_list))
print(len(numbers_set))
```

خروجی:

```text
6
3
```

در List تمام عناصر شمارش می شوند، اما در Set فقط عناصر Unique شمارش می شوند.

---

## 3. شمارش Stringها در Set

`len()` روی Setهایی که شامل String هستند نیز کار می کند.

```python
languages = {"Python", "Java", "C++", "Go"}

print(len(languages))
```

خروجی:

```text
4
```

هر String Unique یک Element محسوب می شود.

---

## 4. شمارش Empty Set

یک Empty Set دارای طول صفر است.

```python
numbers = set()

print(len(numbers))
```

خروجی:

```text
0
```

این موضوع برای بررسی اینکه آیا Set شامل چیزی هست یا نه بسیار کاربردی است.

---

## 5. استفاده از `len()` در `if`

می توانیم نتیجه `len()` را داخل شرط استفاده کنیم.

```python
students = {"Ali", "Sara", "Reza"}

if len(students) > 0:
    print("The Set is not empty")
```

خروجی:

```text
The Set is not empty
```

برای بررسی خالی بودن نیز می توانیم بنویسیم:

```python
if len(students) == 0:
    print("The Set is empty")
```

---

## 6. یک روش ساده تر برای بررسی Empty بودن Set

با اینکه `len()` کار می کند، در Python یک روش رایج تر نیز وجود دارد.

به جای:

```python
if len(students) > 0:
    print("Not empty")
```

می توانیم بنویسیم:

```python
if students:
    print("Not empty")
```

و به جای:

```python
if len(students) == 0:
    print("Empty")
```

می توانیم بنویسیم:

```python
if not students:
    print("Empty")
```

این به این دلیل است که Empty Set یک مقدار **Falsy** است.

Set غیر خالی **Truthy** است.

به خاطر بسپار:

```text
Empty Set
→ False

Non-empty Set
→ True
```

---

## 7. شمارش عناصر بعد از `add()`

طول Set وقتی Elementهای جدید و Unique اضافه می شوند تغییر می کند.

```python
numbers = {1, 2, 3}

print(len(numbers))

numbers.add(4)

print(len(numbers))
```

خروجی:

```text
3
4
```

اما اگر یک Element موجود را دوباره اضافه کنیم، طول افزایش پیدا نمی کند:

```python
numbers.add(4)

print(len(numbers))
```

نتیجه همچنان:

```text
4
```

است.

---

## 8. شمارش عناصر بعد از حذف

حذف یک Element موجود باعث کاهش طول Set می شود.

```python
numbers = {1, 2, 3, 4}

numbers.remove(2)

print(len(numbers))
```

خروجی:

```text
3
```

اما اگر با `discard()` یک Element غیر موجود را حذف کنیم، طول تغییری نمی کند:

```python
numbers.discard(10)

print(len(numbers))
```

طول همچنان:

```text
3
```

خواهد بود.

---

## 9. استفاده از `len()` همراه User Input

می توانیم از User Input یک Set بسازیم و سپس تعداد عناصر Unique آن را بشماریم.

```python
names = set()

names.add(input("Enter a name: "))
names.add(input("Enter another name: "))
names.add(input("Enter another name: "))

print("Unique names:", len(names))
```

اگر کاربر این موارد را وارد کند:

```text
Ali
Sara
Ali
```

Set شامل:

```text
{"Ali", "Sara"}
```

خواهد بود.

پس خروجی:

```text
Unique names: 2
```

است.

این یکی از کاربردهای مهم Setها است: **شمارش مقدارهای Unique**.

---

## 10. شمارش Unique Valueها از یک List

یک الگوی بسیار رایج این است که یک List را به Set تبدیل کنیم و سپس `len()` را روی آن اجرا کنیم.

```python
numbers = [1, 2, 2, 3, 3, 4, 4, 4]

unique_numbers = set(numbers)

print(len(unique_numbers))
```

خروجی:

```text
4
```

مقادیر Unique:

```text
{1, 2, 3, 4}
```

هستند.

این یک روش ساده و قدرتمند برای شمارش مقدارهای Unique است.

---

## 11. مقایسه تعداد کل و تعداد Unique

می توانیم طول List را با طول Set ساخته شده از آن مقایسه کنیم.

```python
numbers = [1, 2, 2, 3, 3, 4]

unique_numbers = set(numbers)

print("Total:", len(numbers))
print("Unique:", len(unique_numbers))
```

خروجی:

```text
Total: 6
Unique: 4
```

این تفاوت نشان می دهد که بعضی مقدارها بیشتر از یک بار تکرار شده اند.

---

## 12. تشخیص Duplicateها

از همین تکنیک می توانیم برای تشخیص وجود Duplicate در یک List استفاده کنیم.

```python
numbers = [1, 2, 3, 4]

if len(numbers) == len(set(numbers)):
    print("No duplicates")
else:
    print("Duplicates exist")
```

خروجی:

```text
No duplicates
```

حالا:

```python
numbers = [1, 2, 2, 3, 4]

if len(numbers) == len(set(numbers)):
    print("No duplicates")
else:
    print("Duplicates exist")
```

خروجی:

```text
Duplicates exist
```

چرا؟

چون:

```text
len(numbers)
→ 5

len(set(numbers))
→ 4
```

طول ها متفاوت هستند، پس حداقل یک Duplicate وجود داشته است.

---

## 13. شمارش عناصر در Setهای دارای Typeهای مختلف

یک Set می تواند شامل Typeهای مختلف Hashable باشد:

```python
data = {
    1,
    "Python",
    3.14,
    (10, 20)
}

print(len(data))
```

خروجی:

```text
4
```

هر مورد یک Element محسوب می شود:

```text
1
"Python"
3.14
(10, 20)
```

محتوای Tuple به صورت جداگانه شمارش نمی شود.

مثلا:

```python
data = {(10, 20)}

print(len(data))
```

خروجی:

```text
1
```

است.

چون فقط یک Tuple به عنوان یک Element در Set داریم.

---

## 14. `len()` تعداد کاراکترهای داخل String را نمی شمارد

این نکته نیز مهم است.

مثلا:

```python
languages = {"Python", "JavaScript"}

print(len(languages))
```

نتیجه:

```text
2
```

است.

`len()` تعداد تمام کاراکترهای داخل Stringها را نمی شمارد.

اگر بخواهیم طول خود String را حساب کنیم:

```python
language = "Python"

print(len(language))
```

خروجی:

```text
6
```

است.

پس:

```text
len(Set)
→ تعداد عناصر Set

len(String)
→ تعداد کاراکترها
```

یک تابع می تواند با توجه به Type Object، معنی متفاوتی داشته باشد.

---

## 15. ترکیب `len()` و `in`

می توانیم مفاهیمی که تا اینجا یاد گرفته ایم را با هم ترکیب کنیم.

```python
students = {"Ali", "Sara", "Reza"}

if "Ali" in students and len(students) >= 3:
    print("Ali is registered and there are enough students")
```

اینجا:

* `in` وجود Element را بررسی می کند.
* `len()` تعداد عناصر را بررسی می کند.
* `and` دو شرط را با هم ترکیب می کند.

این یک قدم مهم برای نوشتن برنامه های واقعی تر است.

---

## 16. ترکیب `len()` و `not in`

می توانیم `len()` را با `not in` نیز ترکیب کنیم.

```python
students = {"Ali", "Sara", "Reza"}

if "Mina" not in students and len(students) < 5:
    print("Mina can be added")
```

سپس:

```python
students.add("Mina")
```

این مثال Membership Check، Counting و Modification را با هم ترکیب می کند.

---

## 17. محدودیت مهم: `len()` نمی گوید چه Elementهایی وجود دارند

مثلا:

```python
numbers = {10, 20, 30}

print(len(numbers))
```

نتیجه:

```text
3
```

است.

اما `len()` به ما نمی گوید این سه Element دقیقا چه هستند.

برای این کار باید از مواردی مثل این ها استفاده کنیم:

* Iteration
* Membership Check
* چاپ کردن Set
* تبدیل Set به Data Structure دیگر در صورت نیاز

در پارت های بعدی Iteration روی Setها را یاد می گیریم.

---

## اشتباهات رایج مبتدی ها

### اشتباه ۱ — تصور کردن اینکه `len()` Duplicateها را می شمارد

```python
numbers = {1, 2, 2, 3}

print(len(numbers))
```

نتیجه:

```text
3
```

است، نه `4`.

---

### اشتباه ۲ — استفاده از `len()` برای Membership Check

این کد اشتباه است:

```python
if len(numbers) == 3:
    print("3 exists")
```

این فقط بررسی می کند که Set دقیقا سه Element دارد.

بررسی نمی کند که مقدار `3` داخل Set وجود دارد یا نه.

برای این کار باید بنویسیم:

```python
if 3 in numbers:
    print("3 exists")
```

---

### اشتباه ۳ — اشتباه گرفتن Empty Set و Empty Dictionary

به خاطر داشته باش:

```python
set()
```

یک Empty Set می سازد.

اما:

```python
{}
```

یک Empty Dictionary می سازد.

این تفاوت در ادامه و هنگام کار با Data Structureهای مختلف Python بسیار مهم خواهد بود.

---

## نکات مهم

بعد از این پارت باید این موارد را بلد باشی:

1. `len(set_name)` تعداد عناصر Unique داخل Set را بر می گرداند.
2. Duplicateها باعث افزایش طول Set نمی شوند.
3. Empty Set دارای طول `0` است.
4. می توان Set غیر خالی را مستقیما با `if set_name` بررسی کرد.
5. با `not set_name` می توان Empty بودن Set را بررسی کرد.
6. `len(set)` و `len(list)` وقتی Duplicate وجود دارد می توانند نتایج متفاوتی داشته باشند.
7. `len(set(list))` یک الگوی مفید برای شمارش مقدارهای Unique است.
8. مقایسه `len(list)` و `len(set(list))` می تواند برای تشخیص Duplicateها استفاده شود.
9. `len()` تعداد عناصر Set را می شمارد، نه تعداد کاراکترهای Stringهای داخل آن را.
10. می توان `len()` را با `in`، `not in`، `and` و شرط های دیگر ترکیب کرد.

---

## تمرین ها

### سوال ۱

این کد چه چیزی چاپ می کند؟

```python
numbers = {1, 2, 2, 3, 3, 3, 4}

print(len(numbers))
```

توضیح بده چرا.

---

### سوال ۲

برنامه ای بنویس که List زیر را داشته باشد:

```python
numbers = [1, 2, 2, 3, 4, 4, 5, 5, 5]
```

و خروجی زیر را چاپ کند:

```text
Total: ...
Unique: ...
```

برای این کار از `len()` و `set()` استفاده کن.

---

### سوال ۳

تفاوت این دو شرط چیست؟

```python
if len(numbers) == 0:
```

و:

```python
if not numbers:
```

وقتی `numbers` یک Set باشد، آیا هر دو یک چیز را بررسی می کنند؟

---

## سوال جامع Setها

برنامه ای بنویس که با این Set شروع شود:

```python
students = {"Ali", "Sara", "Reza"}
```

سپس:

1. تعداد دانش آموزان را با `len()` چاپ کن.
2. از کاربر نام یک دانش آموز جدید را دریافت کن.
3. با استفاده از `in` بررسی کن که آیا این دانش آموز از قبل در Set وجود دارد یا نه.
4. اگر وجود نداشت، با `add()` او را به Set اضافه کن.
5. تعداد جدید دانش آموزان Unique را چاپ کن.
6. از کاربر نام دانش آموزی را که باید حذف شود دریافت کن.
7. اگر دانش آموز وجود داشت، او را حذف کن.
8. Set نهایی و طول آن را چاپ کن.
9. اگر Set خالی شد، با `if not students` آن را تشخیص بده.

در این سوال باید تمام مفاهیم یاد گرفته شده تا اینجا را با هم ترکیب کنی:

**Creating Sets → Adding Elements → Removing Elements → `in` → `not in` → `len()` → Empty Set Checks → Boolean Conditions**

---

# Sets — پارت ۷: پیمایش Setها

در پارت قبلی یاد گرفتیم چطور با `len()` تعداد عناصر یک Set را بشماریم.

حالا می خواهیم یاد بگیریم چطور **روی عناصر یک Set پیمایش انجام دهیم**.

Iteration یعنی اینکه عناصر یک Collection را یکی یکی بررسی یا پردازش کنیم.

ابزار اصلی که در این بخش استفاده می کنیم، حلقه `for` است.

---

## 1. حلقه `for` ساده با Set

می توانیم با یک حلقه `for` به عناصر Set دسترسی پیدا کنیم:

```python
fruits = {"apple", "banana", "orange"}

for fruit in fruits:
    print(fruit)
```

ممکن است خروجی این باشد:

```text
apple
orange
banana
```

اما ترتیب دقیق تضمین شده نیست.

این نکته مهم است، چون **Setها Collectionهای بدون ترتیب مشخص هستند**.

---

## 2. درک عملکرد Loop

این کد را در نظر بگیر:

```python
numbers = {10, 20, 30}

for number in numbers:
    print(number)
```

Loop به صورت مفهومی این مراحل را انجام می دهد:

```text
یک Element را می گیرد
↓
آن را موقتا داخل `number` قرار می دهد
↓
کد داخل Loop را اجرا می کند
↓
به Element بعدی می رود
↓
تا زمانی که همه Elementها بررسی شوند ادامه می دهد
```

نام Variable می تواند هر چیزی باشد:

```python
for number in numbers:
    print(number)
```

یا:

```python
for item in numbers:
    print(item)
```

هر دو صحیح هستند.

---

## 3. چاپ هر Element

یکی از ساده ترین کاربردهای Iteration، چاپ تمام Elementها است:

```python
languages = {"Python", "Java", "C++"}

for language in languages:
    print(language)
```

هر Element در طول Iteration پردازش می شود.

اما چون Set ترتیب تضمین شده ای ندارد، نباید روی ترتیب خروجی حساب کنیم.

---

## 4. انجام یک Operation روی هر Element

Iteration فقط برای چاپ کردن نیست.

می توانیم روی هر Element یک Operation انجام دهیم.

مثلا:

```python
numbers = {1, 2, 3, 4}

for number in numbers:
    print(number * 2)
```

خروجی ممکن:

```text
2
4
6
8
```

Operation برای هر Element به صورت جداگانه انجام می شود.

---

## 5. استفاده از `if` داخل Loop

می توانیم Iteration را با شرط ترکیب کنیم.

```python
numbers = {1, 2, 3, 4, 5, 6}

for number in numbers:
    if number % 2 == 0:
        print(number)
```

خروجی:

```text
2
4
6
```

Loop تمام Elementها را بررسی می کند و `if` فقط عددهای زوج را انتخاب می کند.

---

## 6. پیدا کردن Elementهای خاص

می توانیم از Iteration برای جست و جو در Set استفاده کنیم.

```python
names = {"Ali", "Sara", "Reza", "Mina"}

for name in names:
    if name.startswith("A"):
        print(name)
```

خروجی ممکن:

```text
Ali
```

برای Membership Check ساده، استفاده از `in` معمولا راحت تر است:

```python
if "Ali" in names:
    print("Found")
```

اما Iteration زمانی کاربردی است که بخواهیم **تمام Elementها را بررسی یا پردازش کنیم**.

---

## 7. شمارش Elementها هنگام Iteration

می توانیم یک Counter بسازیم:

```python
numbers = {10, 20, 30, 40}

count = 0

for number in numbers:
    count += 1

print(count)
```

خروجی:

```text
4
```

البته اگر فقط تعداد Elementها را بخواهیم، `len()` ساده تر است:

```python
print(len(numbers))
```

Iteration زمانی مفیدتر می شود که بخواهیم تعداد Elementهایی را بشماریم که یک شرط خاص دارند.

مثلا:

```python
numbers = {1, 2, 3, 4, 5, 6}

even_count = 0

for number in numbers:
    if number % 2 == 0:
        even_count += 1

print(even_count)
```

خروجی:

```text
3
```

---

## 8. ساخت یک Set جدید هنگام Iteration

می توانیم بر اساس عناصر یک Set، یک Set جدید بسازیم.

```python
numbers = {1, 2, 3, 4, 5, 6}

even_numbers = set()

for number in numbers:
    if number % 2 == 0:
        even_numbers.add(number)

print(even_numbers)
```

نتیجه:

```text
{2, 4, 6}
```

این یک الگوی مهم است:

```text
Set اصلی
↓
for loop
↓
condition
↓
Set جدید
```

---

## 9. Iteration روی Set دارای String

Iteration برای Stringها نیز کاملا طبیعی است.

```python
languages = {"Python", "Java", "JavaScript"}

for language in languages:
    print("I know", language)
```

خروجی ممکن:

```text
I know Python
I know Java
I know JavaScript
```

دوباره ترتیب ممکن است متفاوت باشد.

---

## 10. Iteration روی Set دارای Tuple

Tupleها می توانند Element یک Set باشند، چون اگر محتویات آن ها Hashable باشند، خود Tuple نیز Hashable است.

مثلا:

```python
points = {(1, 2), (3, 4), (5, 6)}

for point in points:
    print(point)
```

خروجی ممکن:

```text
(1, 2)
(3, 4)
(5, 6)
```

حتی می توانیم هر Tuple را Unpack کنیم:

```python
points = {(1, 2), (3, 4), (5, 6)}

for x, y in points:
    print("x =", x, "y =", y)
```

خروجی ممکن:

```text
x = 1 y = 2
x = 3 y = 4
x = 5 y = 6
```

---

## 11. استفاده از `break`

با `break` می توانیم Loop را زودتر متوقف کنیم.

```python
numbers = {1, 2, 3, 4, 5}

for number in numbers:
    if number == 3:
        break

    print(number)
```

ترتیب دقیق خروجی ممکن است متفاوت باشد، چون Set ترتیب مشخصی ندارد.

نکته مهم این است که وقتی شرط برقرار شود، `break` بلافاصله Loop را متوقف می کند.

---

## 12. استفاده از `continue`

`continue` Iteration فعلی را رد می کند و به Iteration بعدی می رود.

```python
numbers = {1, 2, 3, 4, 5}

for number in numbers:
    if number % 2 == 0:
        continue

    print(number)
```

خروجی شامل عددهای فرد است:

```text
1
3
5
```

ترتیب ممکن است متفاوت باشد.

---

## 13. ترکیب Iteration و Membership Check

می توانیم Iteration را با `in` ترکیب کنیم.

مثلا:

```python
numbers = {1, 2, 3, 4, 5}

for number in numbers:
    if number in {2, 4}:
        print(number)
```

خروجی:

```text
2
4
```

البته اگر هدف فقط این باشد که بفهمیم یک مقدار وجود دارد یا نه، Membership Check مستقیم بهتر است:

```python
if 2 in numbers:
    print("Found")
```

Iteration زمانی کاربردی تر است که بخواهیم چند Element را پردازش کنیم.

---

## 14. Set را هنگام Iteration تغییر نده

یکی از مهم ترین قوانین این است:

> هنگام Iteration روی یک Set، اندازه همان Set را تغییر نده.

مثلا این کد می تواند خطا ایجاد کند:

```python
numbers = {1, 2, 3, 4}

for number in numbers:
    if number % 2 == 0:
        numbers.remove(number)
```

Python می تواند این خطا را ایجاد کند:

```text
RuntimeError: Set changed size during iteration
```

چرا؟

چون Loop در حال پیمایش Set است و هم زمان ما داریم Elementهای آن را حذف می کنیم.

---

## 15. روش امن برای حذف هنگام Iteration

اگر لازم باشد هنگام Iteration بر اساس یک شرط Elementهایی را حذف کنیم، می توانیم روی یک Copy پیمایش کنیم:

```python
numbers = {1, 2, 3, 4}

for number in numbers.copy():
    if number % 2 == 0:
        numbers.remove(number)

print(numbers)
```

نتیجه:

```text
{1, 3}
```

اینجا:

```python
numbers.copy()
```

یک Set جداگانه برای Loop ایجاد می کند.

در نتیجه Set اصلی را می توانیم با خیال راحت تغییر دهیم.

---

## 16. یک روش امن دیگر: ساخت Set جدید

گاهی حتی روش تمیزتر این است که یک Set جدید بسازیم.

```python
numbers = {1, 2, 3, 4}

odd_numbers = set()

for number in numbers:
    if number % 2 != 0:
        odd_numbers.add(number)

print(odd_numbers)
```

نتیجه:

```text
{1, 3}
```

در این روش Set اصلی را هنگام Iteration تغییر نمی دهیم.

---

## 17. Iteration روی Empty Set

اگر Set خالی باشد:

```python
numbers = set()

for number in numbers:
    print(number)
```

هیچ چیزی چاپ نمی شود.

Loop فقط صفر بار اجرا می شود.

این یکی از دلایلی است که `for` به صورت طبیعی با Collectionها کار می کند.

---

## 18. استفاده از `for` همراه `len()`

می توانیم `len()` را با Iteration ترکیب کنیم.

```python
students = {"Ali", "Sara", "Reza"}

print("Number of students:", len(students))

for student in students:
    print(student)
```

خروجی ممکن:

```text
Number of students: 3
Ali
Sara
Reza
```

تعداد قابل اعتماد است، اما ترتیب Iteration روی Set تضمین نشده است.

---

## 19. مرتب کردن Set قبل از Iteration

اگر به ترتیب قابل پیش بینی نیاز داشته باشیم، می توانیم از `sorted()` استفاده کنیم.

```python
numbers = {5, 2, 8, 1, 3}

for number in sorted(numbers):
    print(number)
```

خروجی:

```text
1
2
3
5
8
```

دقت کن که `sorted()` خود Set را به یک Set مرتب تبدیل نمی کند.

بلکه یک List مرتب شده بر می گرداند که ما روی آن Iteration انجام می دهیم.

به صورت مفهومی:

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

## 20. Iteration به صورت Reverse

اگر عناصر قابلیت Sort شدن داشته باشند، می توانیم به صورت نزولی نیز روی آن ها Iteration انجام دهیم:

```python
numbers = {5, 2, 8, 1, 3}

for number in sorted(numbers, reverse=True):
    print(number)
```

خروجی:

```text
8
5
3
2
1
```

این روش زمانی مفید است که به ترتیب نزولی قابل پیش بینی نیاز داشته باشیم.

---

## اشتباهات رایج مبتدی ها

### اشتباه ۱ — فرض کردن ترتیب Set

نباید کدی بنویسیم که به مواردی مثل:

```text
Element اول
Element دوم
Element سوم
```

وابسته باشد، چون Set ترتیب تضمین شده ای ندارد.

---

### اشتباه ۲ — تلاش برای دسترسی با Index

این کار امکان پذیر نیست:

```python
numbers = {10, 20, 30}

print(numbers[0])
```

Set از Indexing پشتیبانی نمی کند.

از Iteration استفاده کن:

```python
for number in numbers:
    print(number)
```

---

### اشتباه ۳ — تغییر دادن Set هنگام Iteration

از این کار اجتناب کن:

```python
for number in numbers:
    numbers.remove(number)
```

در صورت نیاز از Copy یا یک Set جدید استفاده کن.

---

### اشتباه ۴ — استفاده از Iteration وقتی `in` کافی است

اگر فقط می خواهی بدانی یک Element وجود دارد یا نه:

```python
if 10 in numbers:
    print("Found")
```

ساده تر از این است که تمام Elementها را با Loop بررسی کنی.

---

## نکات مهم

بعد از این پارت باید این موارد را بلد باشی:

1. با `for` می توان روی عناصر Set پیمایش کرد.
2. هر Iteration یک Element را پردازش می کند.
3. ترتیب Iteration روی Set تضمین شده نیست.
4. می توان از `if`، `break` و `continue` داخل Loop استفاده کرد.
5. می توان هنگام Iteration Counter ساخت.
6. می توان هنگام Iteration یک Set جدید ساخت.
7. نباید اندازه Set را هنگام Iteration روی همان Set تغییر دهیم.
8. وقتی لازم است Set اصلی را هنگام Iteration تغییر دهیم، می توانیم از `copy()` استفاده کنیم.
9. با `sorted()` می توان ترتیب قابل پیش بینی برای Iteration ایجاد کرد.
10. وقتی فقط Membership Check لازم داریم، `in` معمولا انتخاب ساده تری از Iteration است.

---

## تمرین ها

### سوال ۱

این کد چه کاری انجام می دهد؟

```python
numbers = {1, 2, 3, 4, 5, 6}

for number in numbers:
    if number % 2 == 0:
        print(number)
```

چه Elementهایی می توانند چاپ شوند؟

---

### سوال ۲

برنامه ای بنویس که Set زیر را داشته باشد:

```python
numbers = {1, 2, 3, 4, 5, 6, 7, 8}
```

و یک Set جدید بسازد که فقط شامل عددهای بزرگ تر از `5` باشد.

---

### سوال ۳

چرا کد زیر می تواند باعث `RuntimeError` شود؟

```python
numbers = {1, 2, 3, 4}

for number in numbers:
    numbers.remove(number)
```

چطور می توان این برنامه را طوری تغییر داد که حذف کردن به صورت امن انجام شود؟

---

## سوال جامع Setها

برنامه ای بنویس که با این Set شروع شود:

```python
students = {"Ali", "Sara", "Reza", "Mina", "Hassan"}
```

برنامه باید:

1. روی Set پیمایش انجام دهد.
2. فقط دانش آموزانی را چاپ کند که نامشان با `"A"` یا `"M"` شروع می شود.
3. تعداد این دانش آموزان را بشمارد.
4. یک Set جدید شامل این دانش آموزان بسازد.
5. تعداد دانش آموزان را با `len()` چاپ کند.
6. با استفاده از `in` بررسی کند که `"Ali"` وجود دارد یا نه.
7. نشان دهد که چرا تغییر مستقیم Set اصلی هنگام Iteration کار امنی نیست.
8. با استفاده از یک روش امن، دانش آموزان انتخاب شده را از Set اصلی حذف کند.
9. Set نهایی را چاپ کند.

در این سوال باید این مفاهیم را با هم ترکیب کنی:

**Creating Sets → Adding Elements → Removing Elements → `in` → `not in` → `len()` → `for` → `if` → `break` / `continue` → Set Copy → New Sets**

---

# Sets — پارت ۸: اجتماع Setها (Set Union)

در پارت قبلی یاد گرفتیم چطور با استفاده از `for` روی عناصر Set پیمایش انجام دهیم.

حالا وارد یکی از مهم ترین قابلیت های Setها می شویم: **Set Operations**.

اولین Operation، مفهوم **Union** است.

Union به ما اجازه می دهد عناصر دو یا چند Set را با هم ترکیب کنیم و Duplicateها را به صورت خودکار حذف کنیم.

---

## 1. Set Union چیست؟

**Union** دو Set شامل تمام Elementهای Unique است که در یکی از دو Set وجود دارند.

مثلا:

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}
```

Union آن ها:

```text
{1, 2, 3, 4, 5}
```

است.

دقت کن که `3` در هر دو Set وجود دارد، اما در نتیجه فقط یک بار قرار می گیرد.

به صورت مفهومی:

```text
Set A      Set B
  ↓          ↓
{1,2,3} + {3,4,5}
       ↓
{1,2,3,4,5}
```

---

## 2. استفاده از Operator `|`

Python برای Union از Operator `|` پشتیبانی می کند.

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}

result = set_a | set_b

print(result)
```

خروجی:

```text
{1, 2, 3, 4, 5}
```

Syntax:

```python
set_a | set_b
```

یعنی:

> تمام Elementهای Unique موجود در `set_a` و `set_b` را بر گردان.

---

## 3. استفاده از متد `union()`

روش دیگر استفاده از متد `union()` است.

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}

result = set_a.union(set_b)

print(result)
```

خروجی:

```text
{1, 2, 3, 4, 5}
```

پس دو روش رایج برای Union داریم:

```python
set_a | set_b
```

و:

```python
set_a.union(set_b)
```

هر دو یک Set یکسان ایجاد می کنند.

---

## 4. Union، Setهای اصلی را تغییر نمی دهد

وقتی Union ایجاد می کنیم، Setهای اصلی بدون تغییر باقی می مانند.

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}

result = set_a.union(set_b)

print(set_a)
print(set_b)
print(result)
```

خروجی:

```text
{1, 2, 3}
{3, 4, 5}
{1, 2, 3, 4, 5}
```

Union یک Set جدید ایجاد می کند.

---

## 5. Union بدون Element مشترک

اگر دو Set هیچ Element مشترکی نداشته باشند:

```python
set_a = {1, 2, 3}
set_b = {4, 5, 6}

print(set_a | set_b)
```

خروجی:

```text
{1, 2, 3, 4, 5, 6}
```

چون Duplicateای وجود ندارد، تمام Elementها وارد نتیجه می شوند.

---

## 6. Union دو Set یکسان

اگر دو Set دقیقا Elementهای یکسانی داشته باشند:

```python
set_a = {1, 2, 3}
set_b = {1, 2, 3}

print(set_a | set_b)
```

خروجی:

```text
{1, 2, 3}
```

هر Element همچنان فقط یک بار در نتیجه وجود دارد.

---

## 7. Union بیشتر از دو Set

متد `union()` می تواند با چند Set کار کند.

```python
set_a = {1, 2}
set_b = {2, 3}
set_c = {3, 4}

result = set_a.union(set_b, set_c)

print(result)
```

خروجی:

```text
{1, 2, 3, 4}
```

می توانیم Operator `|` را نیز چند بار استفاده کنیم:

```python
result = set_a | set_b | set_c

print(result)
```

نتیجه همان است:

```text
{1, 2, 3, 4}
```

---

## 8. Union با String

Union فقط برای اعداد نیست.

```python
languages_a = {"Python", "Java", "C++"}
languages_b = {"Python", "Go", "Rust"}

all_languages = languages_a | languages_b

print(all_languages)
```

نتیجه شامل تمام Languageهای Unique است:

```text
{"Python", "Java", "C++", "Go", "Rust"}
```

`Python` در هر دو Set وجود دارد، اما در Union فقط یک بار قرار می گیرد.

---

## 9. یک مثال واقعی

فرض کن دو گروه دانش آموز داریم:

```python
morning_students = {"Ali", "Sara", "Reza"}
evening_students = {"Reza", "Mina", "Hassan"}
```

می خواهیم تمام دانش آموزانی را پیدا کنیم که در یکی از این دو گروه حضور دارند.

```python
all_students = morning_students | evening_students

print(all_students)
```

نتیجه:

```text
{"Ali", "Sara", "Reza", "Mina", "Hassan"}
```

این یک کاربرد واقعی Union است.

---

## 10. ترکیب Union و `len()`

می توانیم Union را با `len()` ترکیب کنیم تا تعداد کل Elementهای Unique را به دست آوریم.

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}

total_unique = len(set_a | set_b)

print(total_unique)
```

خروجی:

```text
5
```

یعنی در مجموع پنج Element Unique در هر دو Set وجود دارد.

---

## 11. ترکیب Union و Iteration

می توانیم روی نتیجه Union نیز Iteration انجام دهیم.

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}

for number in set_a | set_b:
    print(number)
```

خروجی ممکن:

```text
1
2
3
4
5
```

اما دوباره یادمان باشد که ترتیب تضمین شده نیست.

اگر خروجی مرتب می خواهیم:

```python
for number in sorted(set_a | set_b):
    print(number)
```

خروجی:

```text
1
2
3
4
5
```

---

## 12. Union با Empty Set

Union یک Set با Empty Set، همان Elementهای Set اصلی را بر می گرداند.

```python
numbers = {1, 2, 3}
empty = set()

print(numbers | empty)
```

خروجی:

```text
{1, 2, 3}
```

به صورت مفهومی:

```text
Set ∪ Empty Set = Set
```

---

## 13. خاصیت جابجایی Union

Union یک خاصیت مهم ریاضی دارد:

```text
A ∪ B = B ∪ A
```

در Python:

```python
set_a = {1, 2, 3}
set_b = {3, 4, 5}

print(set_a | set_b)
print(set_b | set_a)
```

هر دو نتیجه شامل:

```text
{1, 2, 3, 4, 5}
```

هستند.

پس تغییر ترتیب دو Set نتیجه Union را تغییر نمی دهد.

---

## 14. خاصیت شرکت پذیری Union

Union خاصیت شرکت پذیری نیز دارد:

```text
(A ∪ B) ∪ C = A ∪ (B ∪ C)
```

در Python:

```python
a = {1, 2}
b = {2, 3}
c = {3, 4}

result_1 = (a | b) | c
result_2 = a | (b | c)

print(result_1)
print(result_2)
```

هر دو نتیجه:

```text
{1, 2, 3, 4}
```

هستند.

یعنی می توانیم نحوه گروه بندی عملیات Union را تغییر دهیم، بدون اینکه نتیجه نهایی تغییر کند.

---

## 15. Union با User Input

می توانیم از User Input نیز Set بسازیم و Union بگیریم.

مثلا:

```python
first = input("Enter names separated by spaces: ").split()
second = input("Enter more names separated by spaces: ").split()

set_a = set(first)
set_b = set(second)

all_names = set_a | set_b

print(all_names)
```

اگر کاربر وارد کند:

```text
Ali Sara Reza
Reza Mina Hassan
```

نتیجه شامل:

```text
{"Ali", "Sara", "Reza", "Mina", "Hassan"}
```

خواهد بود.

Duplicate مربوط به `Reza` به صورت خودکار حذف می شود.

---

## 16. Union با List

Operator `|` به Operandهای از نوع Set نیاز دارد.

این کد درست است:

```python
a = {1, 2, 3}
b = {3, 4, 5}

print(a | b)
```

اما این کد درست نیست:

```python
a = {1, 2, 3}
b = [3, 4, 5]

print(a | b)
```

Python یک `TypeError` ایجاد می کند.

اگر بخواهیم از List استفاده کنیم، ابتدا آن را به Set تبدیل می کنیم:

```python
b = set([3, 4, 5])

print(a | b)
```

---

## 17. Union با `union()` و سایر Iterableها

متد `union()` انعطاف بیشتری دارد.

مثلا:

```python
numbers = {1, 2, 3}

result = numbers.union([3, 4, 5])

print(result)
```

خروجی:

```text
{1, 2, 3, 4, 5}
```

حتی می تواند با سایر Iterableها نیز کار کند:

```python
numbers = {1, 2, 3}

result = numbers.union((3, 4, 5))

print(result)
```

خروجی:

```text
{1, 2, 3, 4, 5}
```

پس به خاطر بسپار:

```text
| Operator
→ به Operandهای Set نیاز دارد

union()
→ می تواند Iterableهای دیگر را نیز دریافت کند
```

---

## اشتباهات رایج مبتدی ها

### اشتباه ۱ — تصور اینکه Union Duplicateها را نگه می دارد

```python
a = {1, 2, 3}
b = {3, 4}

print(a | b)
```

نتیجه:

```text
{1, 2, 3, 4}
```

است، نه:

```text
{1, 2, 3, 3, 4}
```

Setها به صورت خودکار Duplicateها را حذف می کنند.

---

### اشتباه ۲ — اشتباه گرفتن Union با Addition

این کار صحیح نیست:

```python
a + b
```

Setها با `+` ترکیب نمی شوند.

از این استفاده کن:

```python
a | b
```

یا:

```python
a.union(b)
```

---

### اشتباه ۳ — انتظار تغییر Set اصلی

این:

```python
a | b
```

باعث تغییر `a` نمی شود.

اگر می خواهی نتیجه را نگه داری:

```python
result = a | b
```

اگر بخواهی یک Set را مستقیما تغییر دهی، در پارت های بعدی با `update()` آشنا می شویم.

---

### اشتباه ۴ — فرض کردن ترتیب ثابت برای Union

نباید انتظار داشته باشی:

```text
{1, 2, 3, 4}
```

همیشه دقیقا با همین ترتیب نمایش داده شود.

اگر ترتیب قابل پیش بینی لازم داری:

```python
sorted(a | b)
```

---

## نکات مهم

بعد از این پارت باید این موارد را بلد باشی:

1. Union تمام Elementهای Unique دو یا چند Set را با هم ترکیب می کند.
2. Operator `|` برای Union استفاده می شود.
3. متد `union()` نیز Union را انجام می دهد.
4. Union به صورت خودکار Duplicateها را حذف می کند.
5. Union Setهای اصلی را تغییر نمی دهد.
6. می توان Union را روی چند Set انجام داد.
7. با `len()` می توان تعداد Elementهای Unique در Union را حساب کرد.
8. می توان با `for` روی نتیجه Union پیمایش کرد.
9. `sorted()` می تواند ترتیب قابل پیش بینی برای خروجی ایجاد کند.
10. Operator `|` به Operandهای Set نیاز دارد.
11. `union()` می تواند Iterableهای دیگر را نیز دریافت کند.
12. Union خاصیت جابجایی و شرکت پذیری دارد.

---

## تمرین ها

### سوال ۱

این کد چه چیزی چاپ می کند؟

```python
a = {1, 2, 3}
b = {3, 4, 5}

print(a | b)
```

چرا `3` فقط یک بار ظاهر می شود؟

---

### سوال ۲

برنامه ای بنویس که این دو Set را با هم ترکیب کند:

```python
python_students = {"Ali", "Sara", "Reza"}
java_students = {"Reza", "Mina", "Hassan"}
```

سپس:

1. تمام دانش آموزان Unique را چاپ کند.
2. تعداد دانش آموزان Unique را چاپ کند.

---

### سوال ۳

تفاوت این دو چیست؟

```python
a | b
```

و:

```python
a.union(b)
```

همچنین توضیح بده چرا این کد درست است:

```python
a.union([3, 4, 5])
```

اما این کد درست نیست:

```python
a | [3, 4, 5]
```

---

## سوال جامع Setها

برای دو گروه دانش آموز این Setها را داریم:

```python
morning_students = {"Ali", "Sara", "Reza", "Mina"}
evening_students = {"Reza", "Hassan", "Mina", "Nima"}
```

برنامه باید:

1. یک Union شامل تمام دانش آموزان Unique ایجاد کند.
2. Set حاصل را چاپ کند.
3. تعداد دانش آموزان Unique را با `len()` چاپ کند.
4. با `for` روی Union پیمایش کند و تمام دانش آموزان را چاپ کند.
5. دانش آموزان را با استفاده از `sorted()` به صورت الفبایی چاپ کند.
6. از کاربر نام یک دانش آموز دیگر را دریافت کند.
7. آن دانش آموز را به Set مناسب اضافه کند.
8. Union را دوباره ایجاد کند.
9. تعداد نهایی دانش آموزان Unique را چاپ کند.

این تمرین باید این مفاهیم را با هم ترکیب کند:

**Creating Sets → Adding Elements → `in` → `len()` → Iteration → `sorted()` → Set Union**

---

