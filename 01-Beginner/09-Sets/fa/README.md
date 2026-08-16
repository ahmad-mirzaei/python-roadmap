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

