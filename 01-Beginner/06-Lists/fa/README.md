# بخش ۱ — لیست چیست؟

> 🌐 Language: **فارسی** | [English](../README.md)

تا اینجا بیشتر با مقادیر تکی که داخل متغیرها ذخیره می‌شوند کار کرده‌ایم.

برای مثال:

```python
name = "Ahmad"
age = 25
city = "Tehran"
```

هر متغیر یک مقدار را نگهداری می‌کند.

این روش زمانی مناسب است که فقط با مقدار کمی داده سر و کار داشته باشیم.

اما فرض کن بخواهیم نام ۱۰۰ دانش‌آموز را در برنامه ذخیره کنیم.

می‌توانیم بنویسیم:

```python
student1 = "Ahmad"
student2 = "Sara"
student3 = "Alex"
student4 = "John"
```

اما با افزایش تعداد داده‌ها، این روش خیلی زود غیرعملی می‌شود.

Python یک ساختار داده به نام **List** در اختیار ما قرار می‌دهد که اجازه می‌دهد چندین مقدار را داخل یک متغیر ذخیره کنیم.

---

## لیست چیست؟

List یک **مجموعه مرتب از عناصر** است.

برای مثال:

```python
students = ["Ahmad", "Sara", "Alex", "John"]
```

به جای اینکه چهار متغیر جداگانه داشته باشیم، هر چهار نام را داخل یک List قرار داده‌ایم.

این List شامل چهار عنصر است:

```text
Ahmad
Sara
Alex
John
```

هر عنصر در یک موقعیت مشخص قرار دارد.

این موقعیت با مفهومی به نام **Index** مشخص می‌شود که در بخش بعدی به صورت کامل بررسی خواهیم کرد.

فعلاً مهم‌ترین ایده این است:

```text
List
 ├── Element
 ├── Element
 ├── Element
 └── Element
```

List به ما اجازه می‌دهد چند مقدار مرتبط را به عنوان یک مجموعه مدیریت کنیم.

---

## ساختن یک List

برای ساختن List از **براکت‌های مربعی** `[]` استفاده می‌کنیم.

ساختار کلی:

```python
list_name = [value1, value2, value3]
```

برای مثال:

```python
numbers = [10, 20, 30, 40, 50]
```

مثال دیگر:

```python
colors = ["red", "green", "blue"]
```

و یک مثال دیگر:

```python
cities = ["Tehran", "Shiraz", "Tabriz", "Mashhad"]
```

عناصر List با کاما از یکدیگر جدا می‌شوند.

---

## List می‌تواند شامل String باشد

یک List می‌تواند چندین String را در خود نگهداری کند:

```python
programming_languages = ["Python", "Java", "C++", "JavaScript"]
```

این قابلیت زمانی مفید است که با مجموعه‌ای از داده‌های متنی مرتبط کار می‌کنیم.

برای مثال:

```python
favorite_foods = ["Pizza", "Burger", "Pasta", "Rice", "Sushi"]
```

حالا متغیر `favorite_foods` نماینده یک مجموعه کامل از غذاهاست، نه فقط یک غذا.

---

## List می‌تواند شامل اعداد باشد

List می‌تواند شامل اعداد صحیح باشد:

```python
scores = [18, 15, 20, 17, 19]
```

یا شامل اعداد اعشاری باشد:

```python
prices = [12.5, 20.75, 8.99, 15.25]
```

این ویژگی باعث می‌شود List برای پردازش داده‌های عددی بسیار کاربردی باشد.

برای مثال:

```python
temperatures = [22, 24, 27, 25, 21]
```

بعداً می‌توانیم با استفاده از توابع داخلی Python و متدهای List روی این داده‌ها عملیات مختلفی انجام دهیم.

---

## List می‌تواند شامل انواع داده مختلف باشد

List در Python محدود به یک نوع داده نیست.

برای مثال:

```python
person = ["Ahmad", 25, 175.5, True]
```

این List شامل موارد زیر است:

```text
"Ahmad" → String
25      → Integer
175.5   → Float
True    → Boolean
```

Python اجازه چنین کاری را می‌دهد چون List یک مجموعه عمومی از داده‌هاست.

با این حال، در برنامه‌های خوب طراحی شده معمولاً عناصر یک List از نظر منطقی با یکدیگر ارتباط دارند.

برای مثال:

```python
ages = [18, 21, 25, 30]
```

یک مجموعه طبیعی است، چون تمام عناصر نشان‌دهنده سن هستند.

در مقابل:

```python
data = ["Ahmad", 25, True, 175.5]
```

مقادیر کاملاً متفاوتی را در خود نگه می‌دارد.

این List از نظر Python کاملاً معتبر است، اما مناسب بودن آن به مسئله‌ای که در حال حل آن هستیم بستگی دارد.

---

## Listها مرتب هستند

یکی از ویژگی‌های اساسی List این است که عناصر آن دارای ترتیب هستند.

برای مثال:

```python
numbers = [10, 20, 30, 40]
```

ترتیب عناصر:

```text
10 → 20 → 30 → 40
```

اگر List زیر را بسازیم:

```python
numbers = [40, 30, 20, 10]
```

همان مقادیر را داریم، اما ترتیب آن‌ها متفاوت است.

این تفاوت اهمیت دارد، زیرا موقعیت هر عنصر بخشی از ساختار List است.

---

## List خالی

هنگام ساخت List مجبور نیستیم از ابتدا مقداری داخل آن قرار دهیم.

می‌توانیم یک List خالی بسازیم:

```python
students = []
```

در این لحظه List هیچ عنصری ندارد.

Listهای خالی زمانی بسیار کاربردی هستند که بخواهیم مجموعه‌ای از داده‌ها را به مرور زمان بسازیم.

برای مثال:

```python
students = []

print(students)
```

خروجی:

```text
[]
```

بعداً می‌توانیم عناصر جدیدی به آن اضافه کنیم.

روش اضافه کردن عناصر را در بخش متدهای List بررسی خواهیم کرد.

---

## پیدا کردن تعداد عناصر List

برای پیدا کردن تعداد عناصر یک List می‌توانیم از تابع داخلی `len()` استفاده کنیم.

برای مثال:

```python
students = ["Ahmad", "Sara", "Alex"]

print(len(students))
```

خروجی:

```text
3
```

یعنی List شامل سه عنصر است.

مثال دیگر:

```python
numbers = [10, 20, 30, 40, 50]

print(len(numbers))
```

خروجی:

```text
5
```

برای یک List خالی:

```python
students = []

print(len(students))
```

خروجی:

```text
0
```

بنابراین می‌توانیم این رابطه را در ذهن داشته باشیم:

```text
len(list) → تعداد عناصر
```

این تابع در ادامه کار با Listها بسیار مهم خواهد بود.

---

## List و متغیرها

List جایگزین متغیرها نیست.

بلکه به یک متغیر اجازه می‌دهد یک مجموعه را نمایش دهد.

برای مثال:

```python
name = "Ahmad"
```

متغیر `name` یک مقدار را نمایش می‌دهد.

اما:

```python
names = ["Ahmad", "Sara", "Alex"]
```

متغیر `names` یک مجموعه از مقادیر را نمایش می‌دهد.

این تفاوت را به خاطر بسپار:

```text
Variable → یک مقدار

List variable → مجموعه‌ای از مقادیر
```

---

## چرا Listها مهم هستند؟

List زمانی اهمیت پیدا می‌کند که برنامه نیاز داشته باشد با مجموعه‌ای از داده‌ها کار کند.

نمونه‌های رایج:

```text
نام دانش‌آموزان
نمره‌های دانش‌آموزان
محصولات
قیمت‌ها
دماها
نام کاربران
سؤال‌ها
پاسخ‌ها
کارها
پیام‌ها
فایل‌ها
```

برای مثال، یک برنامه Todo می‌تواند کارها را داخل یک List ذخیره کند:

```python
tasks = [
    "Study Python",
    "Practice Lists",
    "Read a book",
    "Exercise"
]
```

یک فروشگاه اینترنتی می‌تواند محصولات سبد خرید را ذخیره کند:

```python
cart = [
    "Laptop",
    "Mouse",
    "Keyboard"
]
```

یک برنامه Quiz می‌تواند سؤال‌ها را ذخیره کند:

```python
questions = [
    "What is Python?",
    "What is a variable?",
    "What is a List?"
]
```

همین ساختار ساده می‌تواند در انواع مختلف برنامه‌ها استفاده شود.

---

## List و حلقه‌ها

Listها زمانی بسیار قدرتمندتر می‌شوند که آن‌ها را با حلقه‌ها ترکیب کنیم.

ما در درس قبلی حلقه‌ها را یاد گرفتیم.

برای مثال:

```python
students = ["Ahmad", "Sara", "Alex"]

for student in students:
    print(student)
```

خروجی:

```text
Ahmad
Sara
Alex
```

حلقه هر عنصر List را پردازش می‌کند.

این یکی از مهم‌ترین الگوهایی است که در تمام درس Listها استفاده خواهیم کرد.

به جای اینکه برای هر عنصر کد جداگانه بنویسیم:

```python
print(students[0])
print(students[1])
print(students[2])
```

می‌توانیم با یک حلقه کل مجموعه را پردازش کنیم.

این موضوع زمانی اهمیت بیشتری پیدا می‌کند که تعداد عناصر مشخص نباشد.

---

## List و پردازش داده

فرض کن یک List از نمره‌های دانش‌آموزان داریم:

```python
scores = [18, 8, 15, 7, 20]
```

می‌توانیم با یک حلقه تمام نمره‌ها را پردازش کنیم:

```python
scores = [18, 8, 15, 7, 20]

for score in scores:
    print(score)
```

خروجی:

```text
18
8
15
7
20
```

حالا فرض کن به جای پنج نمره، ۵۰۰ نمره داشته باشیم.

همان حلقه همچنان می‌تواند تمام مجموعه را پردازش کند.

این یکی از مهم‌ترین مزایای استفاده از ساختارهای داده است.

ما یک راه‌حل عمومی می‌نویسیم که روی یک مجموعه داده کار می‌کند، نه اینکه برای تک‌تک مقادیر کد جداگانه بنویسیم.

---

## یک مثال کاربردی — نمره‌های دانش‌آموزان

بیایید با استفاده از مفاهیمی که تا اینجا یاد گرفته‌ایم یک مثال کوچک بسازیم.

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

این مثال چند مفهوم قبلی را با یکدیگر ترکیب می‌کند:

```text
List
Variables
len()
sum()
Arithmetic
f-strings
for loop
if/else
```

این نقطه انتقال مهمی است.

دیگر فقط با مقادیر تکی کار نمی‌کنیم.

اکنون با **مجموعه‌ای از داده‌ها** کار می‌کنیم.

---

## List به عنوان پایه پردازش داده

List فقط برای ذخیره داده نیست.

List پایه بسیاری از مسائل پردازش داده و الگوریتم‌هاست.

فرض کن مسئله این باشد:

> بالاترین نمره را بین چند دانش‌آموز پیدا کن.

به جای اینکه پنج متغیر مستقل داشته باشیم، مسئله را این‌گونه می‌بینیم:

```text
Input
  ↓
مجموعه‌ای از نمره‌ها
  ↓
پردازش عناصر
  ↓
مقایسه مقادیر
  ↓
پیدا کردن بیشترین مقدار
  ↓
Output
```

نکته مهم این است که الگوریتم می‌تواند روی کل مجموعه کار کند.

فرقی نمی‌کند List شامل پنج مقدار باشد یا پنج هزار مقدار.

ایده کلی مسئله همچنان یکسان است.

این یکی از اولین قدم‌ها برای فکر کردن الگوریتمی درباره ساختارهای داده است.

---

## مقایسه List با متغیرهای جداگانه

این روش را در نظر بگیر:

```python
student1 = "Ahmad"
student2 = "Sara"
student3 = "Alex"
student4 = "John"
student5 = "Mary"
```

حالا آن را با این روش مقایسه کن:

```python
students = ["Ahmad", "Sara", "Alex", "John", "Mary"]
```

روش دوم به ما یک مجموعه می‌دهد که می‌توانیم آن را به صورت سیستماتیک پردازش کنیم.

برای مثال:

```python
students = ["Ahmad", "Sara", "Alex", "John", "Mary"]

for student in students:
    print(student)
```

اگر تعداد دانش‌آموزان تغییر کند، حلقه ما نیازی به تغییر ندارد.

این موضوع باعث می‌شود برنامه مقیاس‌پذیرتر و نگهداری آن ساده‌تر شود.

---

## در درس Listها چه چیزهایی یاد می‌گیریم؟

مفهوم List بسیار بزرگ‌تر از ساختن یک List با براکت‌های مربعی است.

در ادامه این درس یاد می‌گیریم:

1. ساخت List
2. دسترسی به عناصر
3. Index مثبت
4. Index منفی
5. تغییر عناصر
6. اضافه کردن عناصر
7. حذف عناصر
8. جستجو در List
9. بررسی وجود یک عنصر
10. پیدا کردن طول List
11. پیمایش List
12. Slicing
13. کپی کردن List
14. مرتب‌ سازی List
15. برعکس کردن List
16. Listهای تو در تو
17. متدهای مهم List
18. ترکیب List با شرط‌ها و حلقه‌ها
19. حل مسائل کاربردی مرتبط با پردازش داده

همچنین List را به مفاهیمی که در درس‌های قبلی یاد گرفته‌ایم متصل خواهیم کرد:

```text
Variables
Data Types
Conditions
Loops
Functions
Strings
```

این ارتباط مهم است، چون در برنامه‌های واقعی معمولاً یک مفهوم را به تنهایی استفاده نمی‌کنیم.

---

# نکات کلیدی

List یک مجموعه مرتب از عناصر است.

List با براکت‌های مربعی ساخته می‌شود:

```python
numbers = [10, 20, 30]
```

List می‌تواند شامل String باشد:

```python
names = ["Ahmad", "Sara", "Alex"]
```

List می‌تواند شامل اعداد باشد:

```python
scores = [18, 15, 20]
```

List می‌تواند شامل انواع مختلف داده باشد:

```python
person = ["Ahmad", 25, True]
```

List خالی به این شکل ساخته می‌شود:

```python
items = []
```

تابع `len()` تعداد عناصر را برمی‌گرداند:

```python
items = ["A", "B", "C"]

print(len(items))
```

خروجی:

```text
3
```

List را می‌توان با حلقه پیمایش کرد:

```python
items = ["A", "B", "C"]

for item in items:
    print(item)
```

مهم‌ترین مفهوم این بخش:

> **List به ما اجازه می‌دهد مجموعه‌ای از مقادیر مرتبط را در یک ساختار داده ذخیره و پردازش کنیم.**

---

# تمرین‌ها

## تمرین ۱ — غذاهای مورد علاقه

یک List به نام `favorite_foods` بساز که حداقل پنج غذا داشته باشد.

سپس List را چاپ کن.

```python
favorite_foods = ["Pizza", "Burger", "Pasta", "Rice", "Sushi"]

print(favorite_foods)
```

---

## تمرین ۲ — زبان‌های برنامه‌ نویسی

یک List شامل حداقل پنج زبان برنامه‌ نویسی بساز.

سپس خود List و تعداد عناصر آن را نمایش بده.

---

## تمرین ۳ — نمره‌های دانش‌آموزان

یک List شامل نمره پنج دانش‌آموز بساز.

موارد زیر را محاسبه کن:

- تعداد نمره‌ها
- مجموع نمره‌ها
- میانگین نمره‌ها

برای حل مسئله از `len()` و `sum()` استفاده کن.

---

## تمرین ۴ — سبد خرید

یک List به نام `cart` بساز که شامل چند محصول باشد.

با استفاده از حلقه `for` تمام محصولات را نمایش بده.

---

## تمرین ۵ — داده‌های مختلف

یک List بساز که شامل موارد زیر باشد:

- نام خودت
- سن خودت
- قد خودت
- یک مقدار Boolean که نشان دهد در حال یادگیری Python هستی یا نه

سپس نوع هر مقدار را بررسی کن.

---

## تمرین ۶ — سؤال مفهومی

توضیح بده چرا این روش:

```python
student1 = "Ahmad"
student2 = "Sara"
student3 = "Alex"
student4 = "John"
```

معمولاً از این روش:

```python
students = ["Ahmad", "Sara", "Alex", "John"]
```

کم‌ کاربردتر است.

در پاسخ خود روی این موضوع تمرکز کن که چرا مجموعه‌ها پردازش داده را ساده‌تر می‌کنند.

---

# چالش بخش — تحلیل‌ گر نمره‌های دانش‌آموزان

یک برنامه بنویس که چند نمره دانش‌آموزان را داخل یک List ذخیره کند.

برنامه باید:

1. یک List شامل حداقل پنج نمره بسازد.
2. List را نمایش دهد.
3. تعداد نمره‌ها را نمایش دهد.
4. مجموع نمره‌ها را محاسبه و نمایش دهد.
5. میانگین را محاسبه و نمایش دهد.
6. با استفاده از حلقه هر نمره را بررسی کند.
7. مشخص کند هر نمره `Passing` است یا `Failing`.
8. از مفاهیم درس‌های قبلی مانند List، Variable، `len()`، `sum()`، Loop، Condition و f-string استفاده کند.

یک نمونه ساختار:

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

قبل از مقایسه با نمونه، سعی کن خودت مسئله را حل کنی.

هدف این چالش فقط ساختن یک List نیست.

هدف این است که درک کنی چرا List زمانی که یک برنامه باید با **مجموعه‌ای از داده‌ها** کار کند، اهمیت زیادی پیدا می‌کند.

---

# بخش ۲ — Indexing و دسترسی به عناصر List

در بخش قبلی یاد گرفتیم که List یک مجموعه مرتب از عناصر است.

برای مثال:

```python
students = ["Ahmad", "Sara", "Alex", "John"]
```

این List شامل چهار عنصر است و هر عنصر در یک موقعیت مشخص قرار دارد.

در Python برای دسترسی به یک عنصر مشخص از مفهوم **Indexing** استفاده می‌کنیم.

یادگیری Indexing یکی از مهم‌ترین مهارت‌ها در کار با Listهاست، چون به ما اجازه می‌دهد عناصر مشخصی را انتخاب، بررسی و در ادامه تغییر دهیم.

---

## Index چیست؟

**Index** موقعیت یک عنصر درون List است.

Python از **Zero-Based Indexing** استفاده می‌کند.

یعنی اولین عنصر List دارای Index برابر با `0` است، نه `1`.

برای مثال:

```python
students = ["Ahmad", "Sara", "Alex", "John"]
```

Indexها به این صورت هستند:

```text
Element    Index

Ahmad      0
Sara       1
Alex       2
John       3
```

بنابراین:

```text
First element  → index 0
Second element → index 1
Third element  → index 2
Fourth element → index 3
```

این یکی از قوانین بنیادی Python است.

---

## دسترسی به اولین عنصر

برای دسترسی به یک عنصر، Index آن را داخل براکت‌های مربعی بعد از نام List قرار می‌دهیم.

برای مثال:

```python
students = ["Ahmad", "Sara", "Alex", "John"]

print(students[0])
```

خروجی:

```text
Ahmad
```

چون `Ahmad` اولین عنصر List است، Index آن `0` است.

---

## دسترسی به عناصر دیگر

می‌توانیم با استفاده از Indexهای مختلف به عناصر مختلف دسترسی پیدا کنیم.

```python
students = ["Ahmad", "Sara", "Alex", "John"]

print(students[0])
print(students[1])
print(students[2])
print(students[3])
```

خروجی:

```text
Ahmad
Sara
Alex
John
```

هر Index به یک عنصر مشخص اشاره می‌کند.

---

## نمایش تصویری Indexهای List

برای درک بهتر می‌توانیم List را این‌گونه تصور کنیم:

```text
Index:      0        1        2        3
            ↓        ↓        ↓        ↓
List:    ["Ahmad",  "Sara",  "Alex",  "John"]
```

Index به Python می‌گوید که کدام عنصر را می‌خواهیم.

برای مثال:

```python
students[0]
```

یعنی:

```text
عنصر موجود در Index شماره 0 را به من بده.
```

و:

```python
students[2]
```

یعنی:

```text
عنصر موجود در Index شماره 2 را به من بده.
```

---

## Indexing برای اعداد

Indexing فقط مخصوص Stringها نیست.

برای مثال:

```python
scores = [18, 8, 15, 7, 20]

print(scores[0])
print(scores[2])
print(scores[4])
```

خروجی:

```text
18
15
20
```

ساختار List:

```text
Index:     0    1    2    3    4
           ↓    ↓    ↓    ↓    ↓
Scores:   18    8   15    7   20
```

بنابراین:

```python
scores[0]  # 18
scores[2]  # 15
scores[4]  # 20
```

---

## چرا Python از صفر شروع می‌کند؟

Zero-Based Indexing ممکن است در ابتدا کمی عجیب به نظر برسد.

اگر یک List پنج عنصر داشته باشد، شاید انتظار داشته باشیم موقعیت‌ها این‌گونه باشند:

```text
1  2  3  4  5
```

اما Python از این ساختار استفاده می‌کند:

```text
0  1  2  3  4
```

یکی از دلایل مهم این نوع شماره‌گذاری این است که Index را می‌توان به عنوان **فاصله از ابتدای مجموعه** در نظر گرفت.

عنصر اول صفر موقعیت از ابتدای مجموعه فاصله دارد.

عنصر دوم یک موقعیت فاصله دارد.

عنصر سوم دو موقعیت فاصله دارد.

و به همین ترتیب ادامه پیدا می‌کند.

لازم نیست در این مرحله وارد جزئیات تاریخی Zero-Based Indexing شویم.

برای کار عملی فقط این قانون را به خاطر بسپار:

> **در Python، اولین عنصر List دارای Index برابر با 0 است.**

---

## آخرین Index

یک قانون بسیار مهم این است:

```text
Last index = length - 1
```

برای مثال:

```python
numbers = [10, 20, 30, 40, 50]
```

این List دارای پنج عنصر است.

بنابراین:

```python
len(numbers)
```

مقدار زیر را برمی‌گرداند:

```text
5
```

اما Indexها این‌ها هستند:

```text
0  1  2  3  4
```

پس آخرین Index برابر است با:

```text
5 - 1 = 4
```

بنابراین:

```python
numbers[4]
```

مقدار زیر را برمی‌گرداند:

```text
50
```

این رابطه بسیار مهم است:

```text
Last index = len(list) - 1
```

---

## دسترسی به آخرین عنصر

می‌توانیم با استفاده از Index مثبت به آخرین عنصر دسترسی پیدا کنیم.

برای مثال:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[4])
```

خروجی:

```text
50
```

اما Python روش راحت‌تری برای دسترسی به آخرین عنصر در اختیار ما قرار می‌دهد.

می‌توانیم از **Negative Indexing** استفاده کنیم.

---

## Negative Indexing

Python اجازه می‌دهد از انتهای List نیز Indexگذاری کنیم.

برای مثال:

```python
numbers = [10, 20, 30, 40, 50]
```

Indexها را می‌توانیم این‌گونه ببینیم:

```text
Positive Index:

Index:      0    1    2    3    4
            ↓    ↓    ↓    ↓    ↓
List:      10   20   30   40   50


Negative Index:

Index:     -5   -4   -3   -2   -1
            ↓    ↓    ↓    ↓    ↓
List:      10   20   30   40   50
```

Indexهای منفی از `-1` شروع می‌شوند.

بنابراین:

```text
-1 → آخرین عنصر
-2 → عنصر یکی مانده به آخر
-3 → عنصر دو تا مانده به آخر
```

---

## دسترسی به آخرین عنصر با -1

برای مثال:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[-1])
```

خروجی:

```text
50
```

این یکی از رایج‌ترین روش‌های Indexing در Python است.

به جای اینکه آخرین Index مثبت را محاسبه کنیم:

```python
print(numbers[len(numbers) - 1])
```

می‌توانیم به سادگی بنویسیم:

```python
print(numbers[-1])
```

روش دوم کوتاه‌تر و خواناتر است.

---

## دسترسی به عناصر از انتهای List

می‌توانیم از Indexهای منفی دیگر نیز استفاده کنیم.

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[-1])
print(numbers[-2])
print(numbers[-3])
```

خروجی:

```text
50
40
30
```

بنابراین:

```text
-1 → 50
-2 → 40
-3 → 30
```

Negative Indexing زمانی بسیار مفید است که به عناصر نزدیک انتهای List نیاز داشته باشیم.

---

## Index مثبت و منفی به یک عنصر اشاره می‌کنند

Indexهای مثبت و منفی می‌توانند به یک عنصر یکسان اشاره کنند.

برای مثال:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[0])
print(numbers[-5])
```

هر دو خروجی زیر را تولید می‌کنند:

```text
10
```

مثال دیگر:

```python
print(numbers[1])
print(numbers[-4])
```

هر دو مقدار زیر را نشان می‌دهند:

```text
20
```

و:

```python
print(numbers[4])
print(numbers[-1])
```

هر دو مقدار زیر را نشان می‌دهند:

```text
50
```

ساختار کامل List:

```text
Positive:   0    1    2    3    4
            ↓    ↓    ↓    ↓    ↓
Values:    10   20   30   40   50
            ↑    ↑    ↑    ↑    ↑
Negative:  -5   -4   -3   -2   -1
```

---

## Indexing روی Stringهای داخل List

یک List می‌تواند شامل String باشد و خود String نیز قابل Indexing است.

برای مثال:

```python
names = ["Ahmad", "Sara", "Alex"]

print(names[0])
```

خروجی:

```text
Ahmad
```

اینجا:

```python
names[0]
```

اولین String را برمی‌گرداند.

حالا می‌توانیم روی خود String نیز Indexing انجام دهیم:

```python
print(names[0][0])
```

خروجی:

```text
A
```

این اتفاق به این دلیل است که:

```text
names[0]     → "Ahmad"
names[0][0]  → "A"
```

این موضوع یک ایده مهم را معرفی می‌کند:

> **در Python می‌توانیم عملیات Indexing را هنگام کار با Sequenceهای تو در تو با یکدیگر ترکیب کنیم.**

در ادامه مباحث List و ساختارهای تو در تو، این مفهوم را بیشتر بررسی خواهیم کرد.

---

## استفاده از Variable به عنوان Index

Index الزاماً نباید مستقیماً یک عدد نوشته شده در کد باشد.

می‌توانیم Index را داخل یک متغیر ذخیره کنیم.

برای مثال:

```python
students = ["Ahmad", "Sara", "Alex", "John"]

index = 2

print(students[index])
```

خروجی:

```text
Alex
```

اینجا:

```python
index = 2
```

و:

```python
students[index]
```

از نظر نتیجه معادل:

```python
students[2]
```

است.

این روش زمانی بسیار مفید می‌شود که Index در زمان اجرای برنامه تعیین شود.

---

## استفاده از Input به عنوان Index

از آنجا که Index می‌تواند داخل یک Variable قرار داشته باشد، می‌توانیم آن را از کاربر نیز دریافت کنیم.

برای مثال:

```python
students = ["Ahmad", "Sara", "Alex", "John"]

index = int(input("Enter an index: "))

print(students[index])
```

اگر کاربر مقدار زیر را وارد کند:

```text
2
```

برنامه خروجی زیر را نمایش می‌دهد:

```text
Alex
```

اینجا چند مفهوم قبلی با یکدیگر ترکیب شده‌اند:

```text
Input
  ↓
Type Casting
  ↓
Variable
  ↓
List Indexing
  ↓
Output
```

---

## خطای IndexError

اگر بخواهیم به Indexای دسترسی پیدا کنیم که وجود ندارد، چه اتفاقی می‌افتد؟

مثال زیر را ببین:

```python
students = ["Ahmad", "Sara", "Alex"]

print(students[5])
```

این List فقط سه عنصر دارد.

Indexهای مثبت معتبر آن:

```text
0
1
2
```

Index شماره `5` وجود ندارد.

در نتیجه Python خطایی ایجاد می‌کند:

```text
IndexError: list index out of range
```

این خطا **IndexError** نام دارد.

---

## مفهوم "List Index Out of Range"

عبارت:

```text
list index out of range
```

یعنی:

> Index درخواست شده خارج از محدوده Indexهای معتبر آن List است.

برای مثال:

```python
numbers = [10, 20, 30]
```

Indexهای معتبر:

```text
0
1
2
```

Indexهای نامعتبر:

```text
3
4
5
...
```

برخی Indexهای منفی نیز می‌توانند نامعتبر باشند.

برای مثال:

```python
numbers[-4]
```

نامعتبر است، چون List فقط سه عنصر دارد.

---

## جلوگیری از IndexError

قبل از استفاده از یک Index باید اندازه List را در نظر بگیریم.

برای مثال:

```python
numbers = [10, 20, 30, 40, 50]

print(len(numbers))
```

خروجی:

```text
5
```

بنابراین Indexهای مثبت معتبر:

```text
0 تا 4
```

هستند.

یک رابطه بسیار مهم:

```text
0 <= index < len(list)
```

برای Listای که پنج عنصر دارد:

```text
0 <= index < 5
```

بنابراین Indexهای زیر معتبر هستند:

```text
0
1
2
3
4
```

---

## بررسی Index با Condition

می‌توانیم قبل از دسترسی به List با استفاده از شرط بررسی کنیم که آیا Index معتبر است یا نه.

برای مثال:

```python
students = ["Ahmad", "Sara", "Alex"]

index = 2

if 0 <= index < len(students):
    print(students[index])
else:
    print("Invalid index")
```

خروجی:

```text
Alex
```

اگر Index برابر با:

```python
index = 5
```

باشد، برنامه خروجی زیر را نمایش می‌دهد:

```text
Invalid index
```

این مثال چند مفهوم را با یکدیگر ترکیب می‌کند:

```text
List
len()
Variable
Condition
Indexing
```

---

## Indexing و Loop

می‌توانیم Indexing را با حلقه‌ها نیز ترکیب کنیم.

برای مثال:

```python
students = ["Ahmad", "Sara", "Alex", "John"]

for index in range(len(students)):
    print(index, students[index])
```

خروجی:

```text
0 Ahmad
1 Sara
2 Alex
3 John
```

اینجا:

```python
range(len(students))
```

Indexهای معتبر را تولید می‌کند.

سپس:

```python
students[index]
```

عنصر موجود در آن Index را دریافت می‌کند.

این یک الگوی مهم است.

با این حال، اگر فقط به خود مقادیر نیاز داشته باشیم و Index برایمان مهم نباشد، Python روش ساده‌تری در اختیارمان قرار می‌دهد:

```python
for student in students:
    print(student)
```

این دو روش را هنگام بررسی Iteration روی Listها با جزئیات بیشتری مقایسه خواهیم کرد.

---

## یک مثال کاربردی — نمره‌های دانش‌آموزان

بیایید از Indexing در یک مثال واقعی استفاده کنیم.

```python
scores = [18, 8, 15, 7, 20]

print("----- Student Scores -----")
print()

print(f"First score: {scores[0]}")
print(f"Second score: {scores[1]}")
print(f"Last score: {scores[-1]}")
```

خروجی:

```text
----- Student Scores -----

First score: 18
Second score: 8
Last score: 20
```

این مثال هم Index مثبت و هم Index منفی را نشان می‌دهد.

---

## یک مثال کاربردی دیگر — دسترسی به محصولات

فرض کن یک فروشگاه اینترنتی List زیر را برای محصولات خود داشته باشد:

```python
products = ["Laptop", "Mouse", "Keyboard", "Monitor"]
```

می‌توانیم به محصولات مشخص دسترسی پیدا کنیم:

```python
print(f"First product: {products[0]}")
print(f"Last product: {products[-1]}")
```

خروجی:

```text
First product: Laptop
Last product: Monitor
```

این الگو در برنامه‌های واقعی بسیار رایج است.

---

## یک مثال کاربردی — انتخاب از منو

فرض کن یک منوی ساده داریم:

```python
menu = ["Pizza", "Burger", "Pasta", "Salad"]
```

می‌توانیم یک گزینه مشخص را انتخاب کنیم:

```python
choice = 2

print(f"You selected: {menu[choice]}")
```

خروجی:

```text
You selected: Pasta
```

نکته مهم این است که Index می‌تواند توسط خود برنامه تعیین شود و الزاماً یک مقدار ثابت در کد نباشد.

---

## Indexing با Slicing متفاوت است

باید بین **Indexing** و **Slicing** تفاوت قائل شویم.

Indexing یک عنصر را انتخاب می‌کند:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[2])
```

خروجی:

```text
30
```

اما Slicing یک محدوده از عناصر را انتخاب می‌کند:

```python
print(numbers[1:4])
```

خروجی:

```text
[20, 30, 40]
```

Slicing قوانین خاص خودش را دارد و در یک بخش جداگانه آن را بررسی خواهیم کرد.

فعلاً این تفاوت را به خاطر بسپار:

```text
Indexing → یک عنصر

Slicing → یک محدوده از عناصر
```

---

# مهم‌ترین قوانین Indexing

چند قانون مهم وجود دارد که باید به خاطر بسپاری.

## قانون ۱ — Indexing از صفر شروع می‌شود

```python
numbers = [10, 20, 30]

print(numbers[0])
```

خروجی:

```text
10
```

---

## قانون ۲ — آخرین Index مثبت برابر Length منهای یک است

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[len(numbers) - 1])
```

خروجی:

```text
50
```

---

## قانون ۳ — مقدار -1 به آخرین عنصر اشاره می‌کند

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[-1])
```

خروجی:

```text
50
```

---

## قانون ۴ — Indexهای منفی از انتها شمارش می‌شوند

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[-2])
```

خروجی:

```text
40
```

---

## قانون ۵ — Index نامعتبر باعث IndexError می‌شود

```python
numbers = [10, 20, 30]

print(numbers[5])
```

این کد باعث ایجاد خطای زیر می‌شود:

```text
IndexError: list index out of range
```

---

# نکات کلیدی

Indexing به ما اجازه می‌دهد به عناصر تکی یک List دسترسی داشته باشیم.

Python از Zero-Based Indexing استفاده می‌کند.

برای مثال:

```python
students = ["Ahmad", "Sara", "Alex", "John"]
```

Indexها:

```text
Index:      0        1        2        3
            ↓        ↓        ↓        ↓
List:    ["Ahmad",  "Sara",  "Alex",  "John"]
```

اولین عنصر با این دستور قابل دسترسی است:

```python
students[0]
```

آخرین عنصر را می‌توان با این روش دریافت کرد:

```python
students[-1]
```

عنصر یکی مانده به آخر:

```python
students[-2]
```

آخرین Index مثبت:

```text
len(list) - 1
```

یک Index مثبت معتبر باید این شرط را داشته باشد:

```text
0 <= index < len(list)
```

Index نامعتبر باعث ایجاد:

```text
IndexError
```

می‌شود.

مهم‌ترین مفهوم این بخش:

> **Indexing به ما کنترل دقیق روی عناصر تکی یک List می‌دهد.**

---

# تمرین‌ها

## تمرین ۱ — Indexing پایه

List زیر را بساز:

```python
fruits = ["Apple", "Banana", "Orange", "Mango", "Grape"]
```

موارد زیر را چاپ کن:

- اولین عنصر
- دومین عنصر
- سومین عنصر
- آخرین عنصر

در صورت امکان از Indexهای مثبت و منفی استفاده کن.

---

## تمرین ۲ — نمره‌های دانش‌آموزان

List زیر را بساز:

```python
scores = [18, 8, 15, 7, 20]
```

موارد زیر را چاپ کن:

- اولین نمره
- سومین نمره
- آخرین نمره
- نمره یکی مانده به آخر

---

## تمرین ۳ — جدول Indexها

یک List با حداقل شش عنصر بساز.

سپس Index مثبت و منفی هر عنصر را مشخص کن.

برای مثال:

```text
Positive Index    Value    Negative Index
0                 A        -6
1                 B        -5
...
```

---

## تمرین ۴ — Index پویا

یک List از چند شهر بساز.

یک Index را داخل یک Variable ذخیره کن و با استفاده از آن Variable به یک عنصر دسترسی پیدا کن.

برای مثال:

```python
cities = ["Tehran", "Shiraz", "Tabriz", "Mashhad"]

index = 2

print(cities[index])
```

سپس مقدار `index` را تغییر بده و نتیجه را مشاهده کن.

---

## تمرین ۵ — انتخاب عنصر توسط کاربر

یک List از چند غذای مورد علاقه بساز.

از کاربر یک Index دریافت کن و غذای مربوط به آن Index را نمایش بده.

برای دریافت ورودی از `input()` و برای تبدیل نوع داده از Type Casting استفاده کن.

قبل از دسترسی به List مطمئن شو که Index معتبر است.

---

## تمرین ۶ — جلوگیری از IndexError

یک List بساز و از کاربر یک Index دریافت کن.

با استفاده از Condition بررسی کن که آیا Index معتبر است یا نه.

اگر Index معتبر بود، عنصر مربوطه را چاپ کن.

در غیر این صورت پیام زیر را نمایش بده:

```text
Invalid index
```

---

# چالش بخش — انتخاب نمره دانش‌آموز

برنامه‌ای بنویس که چند نمره دانش‌آموز را داخل یک List ذخیره کند.

برنامه باید:

1. List را نمایش دهد.
2. تعداد نمره‌ها را نمایش دهد.
3. از کاربر یک Index دریافت کند.
4. معتبر بودن Index را بررسی کند.
5. اگر Index معتبر بود، نمره انتخاب شده را نمایش دهد.
6. اگر Index نامعتبر بود، پیام مناسب نمایش دهد.
7. اولین و آخرین نمره را نیز نمایش دهد.

یک ساختار نمونه:

```python
scores = [18, 8, 15, 7, 20]

print("----- Student Score Selector -----")
print()

print(f"Scores: {scores}")
print(f"Number of scores: {len(scores)}")
print(f"First score: {scores[0]}")
print(f"Last score: {scores[-1]}")
print()

index = int(input("Enter an index: "))

if 0 <= index < len(scores):
    print(f"Selected score: {scores[index]}")
else:
    print("Invalid index")
```

قبل از نگاه کردن به نمونه، سعی کن خودت مسئله را حل کنی.

هدف این چالش این است که چند مفهوم از درس‌های قبلی را با یکدیگر ترکیب کنی:

```text
Lists
Variables
Input
Type Casting
len()
Conditions
Indexing
Output
```

در بخش بعدی یاد می‌گیریم که چگونه از Indexing فقط برای خواندن عناصر استفاده نکنیم، بلکه **عناصر موجود در یک List را نیز تغییر دهیم**.

---

# بخش ۳ — تغییر عناصر List

در این بخش یاد می‌گیریم چگونه عناصر موجود در یک List را با استفاده از Index تغییر دهیم.

## چیزهایی که یاد می‌گیریم

- تغییر یک عنصر List با استفاده از Index
- جایگزین کردن عنصر اول و آخر
- استفاده از Index مثبت و منفی
- استفاده از Variable به عنوان Index
- تغییر مقدار بر اساس مقدار فعلی آن
- استفاده از عملگرهای Augmented Assignment
- تغییر عناصر List با شرط
- تغییر عناصر List داخل Loop
- مفهوم Mutable بودن List
- خطاهای رایج
- مثال‌های کاربردی
- تمرین‌ها
- چالش بخش

---

## ۱. تغییر یک عنصر List

در بخش قبلی یاد گرفتیم چگونه به یک عنصر دسترسی پیدا کنیم:

```python
fruits = ["Apple", "Banana", "Orange"]

print(fruits[1])
```

خروجی:

```text
Banana
```

حالا می‌توانیم با استفاده از همان Index، مقدار عنصر را تغییر دهیم:

```python
fruits = ["Apple", "Banana", "Orange"]

fruits[1] = "Mango"

print(fruits)
```

خروجی:

```text
['Apple', 'Mango', 'Orange']
```

قالب کلی:

```python
list_name[index] = new_value
```

مقدار موجود در آن Index با مقدار جدید جایگزین می‌شود.

---

## ۲. تغییر اولین عنصر

چون اولین عنصر Index برابر با `0` دارد:

```python
colors = ["Red", "Blue", "Green"]

colors[0] = "Yellow"

print(colors)
```

خروجی:

```text
['Yellow', 'Blue', 'Green']
```

---

## ۳. تغییر آخرین عنصر

در هنگام تغییر عناصر نیز می‌توانیم از Negative Indexing استفاده کنیم:

```python
colors = ["Red", "Blue", "Green"]

colors[-1] = "Purple"

print(colors)
```

خروجی:

```text
['Red', 'Blue', 'Purple']
```

به یاد داشته باش:

```text
-1 → آخرین عنصر
-2 → یکی مانده به آخر
```

---

## ۴. تغییر عناصر عددی

تغییر عناصر فقط مخصوص String نیست.

```python
scores = [18, 8, 15, 7, 20]

scores[1] = 12

print(scores)
```

خروجی:

```text
[18, 12, 15, 7, 20]
```

فقط عنصر موجود در Index شماره `1` تغییر کرده است.

---

## ۵. تغییر چند عنصر

می‌توانیم چند عنصر را با Assignmentهای جداگانه تغییر دهیم:

```python
scores = [18, 8, 15, 7, 20]

scores[1] = 12
scores[3] = 14

print(scores)
```

خروجی:

```text
[18, 12, 15, 14, 20]
```

هر Assignment عنصر موجود در Index مشخص شده را تغییر می‌دهد.

---

## ۶. استفاده از Variable به عنوان Index

Index لازم نیست مستقیماً داخل براکت نوشته شود.

می‌توانیم آن را داخل یک Variable قرار دهیم:

```python
students = ["Ahmad", "Sara", "Alex", "John"]

index = 2

students[index] = "Michael"

print(students)
```

خروجی:

```text
['Ahmad', 'Sara', 'Michael', 'John']
```

این روش زمانی اهمیت بیشتری پیدا می‌کند که موقعیت مورد نظر در زمان اجرای برنامه مشخص شود.

---

## ۷. استفاده از Variable برای مقدار جدید

مقدار جدید نیز می‌تواند داخل یک Variable قرار داشته باشد:

```python
students = ["Ahmad", "Sara", "Alex", "John"]

new_name = "Michael"

students[2] = new_name

print(students)
```

خروجی:

```text
['Ahmad', 'Sara', 'Michael', 'John']
```

بنابراین هم Index و هم مقدار جدید می‌توانند Dynamic باشند:

```python
index = 2
new_name = "Michael"

students[index] = new_name
```

---

## ۸. تغییر عنصر بر اساس مقدار فعلی آن

می‌توانیم مقدار فعلی یک عنصر را بخوانیم، روی آن عملیات انجام دهیم و نتیجه را دوباره در همان موقعیت قرار دهیم.

```python
scores = [18, 8, 15, 7, 20]

scores[1] = scores[1] + 2

print(scores)
```

خروجی:

```text
[18, 10, 15, 7, 20]
```

ابتدا مقدار:

```python
scores[1]
```

خوانده می‌شود.

سپس `2` به آن اضافه می‌شود.

در نهایت نتیجه دوباره در همان Index قرار می‌گیرد.

---

## ۹. Augmented Assignment

Python روش کوتاه‌تری برای این نوع تغییرات در اختیارمان قرار می‌دهد.

به جای:

```python
scores[1] = scores[1] + 2
```

می‌توانیم بنویسیم:

```python
scores[1] += 2
```

مثال:

```python
scores = [18, 8, 15, 7, 20]

scores[1] += 2

print(scores)
```

خروجی:

```text
[18, 10, 15, 7, 20]
```

عملگرهای دیگری نیز وجود دارند:

```python
scores[1] -= 2
scores[1] *= 2
scores[1] /= 2
```

این عملگرها در هنگام تغییر داده‌های عددی بسیار کاربردی هستند.

---

## ۱۰. تغییر عنصر با Negative Indexing

Negative Indexing را می‌توان با محاسبات نیز ترکیب کرد:

```python
numbers = [10, 20, 30, 40, 50]

numbers[-1] += 10

print(numbers)
```

خروجی:

```text
[10, 20, 30, 40, 60]
```

آخرین عنصر `10` واحد افزایش پیدا کرده است.

---

## ۱۱. تغییر عنصر با Condition

می‌توانیم تغییر List را با Condition ترکیب کنیم:

```python
scores = [18, 8, 15, 7, 20]

if scores[1] < 10:
    scores[1] = 10

print(scores)
```

خروجی:

```text
[18, 10, 15, 7, 20]
```

در اینجا مقدار فقط زمانی تغییر می‌کند که شرط برقرار باشد.

الگوی مهم این قسمت:

```text
خواندن عنصر
    ↓
بررسی شرط
    ↓
تغییر عنصر
```

---

## ۱۲. تغییر عناصر List داخل Loop

می‌توانیم با استفاده از Loop و Index تمام عناصر را بررسی و در صورت نیاز تغییر دهیم:

```python
scores = [8, 12, 7, 18, 9]

for index in range(len(scores)):
    if scores[index] < 10:
        scores[index] = 10

print(scores)
```

خروجی:

```text
[10, 12, 10, 18, 10]
```

برنامه هر موقعیت را بررسی می‌کند.

اگر نمره کمتر از `10` باشد، مقدار آن را با `10` جایگزین می‌کند.

این الگو در پردازش داده‌های داخل List بسیار مهم است.

---

## ۱۳. مثال کاربردی — اصلاح نمره‌ها

فرض کنیم بعضی از نمره‌های دانش‌ آموز اشتباه وارد شده‌اند:

```python
scores = [18, 8, 15, 7, 20]

print("----- Score Correction -----")
print()

print(f"Original scores: {scores}")

scores[1] = 13

print(f"Updated scores: {scores}")
```

خروجی:

```text
----- Score Correction -----

Original scores: [18, 8, 15, 7, 20]
Updated scores: [18, 13, 15, 7, 20]
```

در این مثال فقط یک عنصر موجود جایگزین شده است.

---

## ۱۴. مثال کاربردی — تغییر منو

یک منوی رستوران نیز می‌تواند تغییر کند:

```python
menu = ["Pizza", "Burger", "Pasta", "Salad"]

menu[3] = "Steak"

print(menu)
```

خروجی:

```text
['Pizza', 'Burger', 'Pasta', 'Steak']
```

خود List باقی می‌ماند و فقط یکی از عناصر آن تغییر می‌کند.

---

## ۱۵. مثال کاربردی — تغییر موجودی

فرض کنیم تعداد موجودی چند محصول را نگهداری می‌کنیم:

```python
stock = [15, 8, 20, 5]

stock[1] = 12

print(stock)
```

خروجی:

```text
[15, 12, 20, 5]
```

موجودی عنصر موجود در Index شماره `1` تغییر کرده است.

---

## ۱۶. Mutable یعنی چه؟

List یک Data Type **Mutable** است.

Mutable یعنی بعد از ساخته شدن List، می‌توانیم محتوای آن را تغییر دهیم.

برای مثال:

```python
numbers = [10, 20, 30]

numbers[0] = 100

print(numbers)
```

خروجی:

```text
[100, 20, 30]
```

List ابتدا ساخته شده و سپس یکی از عناصر موجود در آن تغییر کرده است.

این مفهوم در ادامه، هنگام مقایسه List با **Tuple** بسیار مهم خواهد بود، چون Tuple یک Data Type **Immutable** است.

---

## ۱۷. تغییر List باعث تغییر طول آن نمی‌شود

وقتی یک عنصر موجود را جایگزین می‌کنیم، تعداد عناصر List تغییر نمی‌کند:

```python
numbers = [10, 20, 30]

print(len(numbers))

numbers[1] = 200

print(numbers)
print(len(numbers))
```

خروجی:

```text
3
[10, 200, 30]
3
```

مقدار تغییر کرده است، اما تعداد عناصر همچنان `3` است.

عملیات اضافه کردن و حذف کردن عنصر با این موضوع متفاوت است و در بخش‌های بعدی بررسی خواهد شد.

---

## ۱۸. Index نامعتبر در Modification

Index باید از قبل در List وجود داشته باشد.

مثال زیر اشتباه است:

```python
numbers = [10, 20, 30]

numbers[5] = 100
```

Python خطای زیر را ایجاد می‌کند:

```text
IndexError: list assignment index out of range
```

Assignment با Index برای جایگزین کردن یک عنصر موجود استفاده می‌شود.

این کار باعث ایجاد موقعیت‌های خالی نمی‌شود.

برای مثال:

```python
numbers = [10, 20, 30]

numbers[5] = 100
```

باعث ایجاد Indexهای `3` و `4` نمی‌شود.

برای اضافه کردن عناصر جدید، بعداً از متدهایی مانند `append()` و `insert()` استفاده خواهیم کرد.

---

## ۱۹. تفاوت Reading و Modifying

این دو عملیات را نباید با یکدیگر اشتباه بگیریم.

Reading:

```python
numbers = [10, 20, 30]

print(numbers[2])
```

خروجی:

```text
30
```

Modifying:

```python
numbers[2] = 100
```

حالا List به این شکل است:

```text
[10, 20, 100]
```

مثال کامل:

```python
numbers = [10, 20, 30]

print(numbers[2])

numbers[2] = 100

print(numbers)
```

خروجی:

```text
30
[10, 20, 100]
```

---

## ۲۰. یک مثال کامل کاربردی

یک سیستم کوچک برای اصلاح نمره‌ها ایجاد کنیم:

```python
scores = [18, 8, 15, 7, 20]

print("----- Score Correction -----")
print()

print(f"Original scores: {scores}")

for index in range(len(scores)):
    if scores[index] < 10:
        scores[index] = 10

print(f"Updated scores: {scores}")
```

خروجی:

```text
----- Score Correction -----

Original scores: [18, 8, 15, 7, 20]
Updated scores: [18, 10, 15, 10, 20]
```

این مثال چند مفهوم قبلی را با هم ترکیب می‌کند:

```text
Lists
Variables
Indexing
len()
range()
for loops
Conditions
Assignment
```

---

# اشتباهات رایج

## اشتباه ۱ — فراموش کردن Zero-Based Indexing

اولین عنصر Index برابر با `0` دارد:

```python
numbers = [10, 20, 30]

numbers[0] = 100

print(numbers)
```

خروجی:

```text
[100, 20, 30]
```

---

## اشتباه ۲ — استفاده از Index ناموجود

کد زیر باعث خطا می‌شود:

```python
numbers = [10, 20, 30]

numbers[3] = 100
```

Indexهای معتبر:

```text
0
1
2
```

هستند.

---

## اشتباه ۳ — اشتباه گرفتن Replacement با Adding

این دستور:

```python
numbers[1] = 100
```

عنصر موجود در Index شماره `1` را جایگزین می‌کند.

عنصر جدیدی اضافه نمی‌کند.

```python
numbers = [10, 20, 30]

numbers[1] = 100

print(numbers)
```

خروجی:

```text
[10, 100, 30]
```

تعداد عناصر همچنان `3` است.

---

## اشتباه ۴ — انتظار ایجاد موقعیت‌های خالی

کد زیر معتبر نیست:

```python
numbers = [10, 20, 30]

numbers[5] = 100
```

List موقعیت‌های خالی را به صورت خودکار ایجاد نمی‌کند.

برای اضافه کردن عنصر جدید، از متدهایی مانند `append()` و `insert()` استفاده خواهیم کرد.

---

# نکات کلیدی

قالب اصلی تغییر یک عنصر List:

```python
list_name[index] = new_value
```

Listها Mutable هستند:

```python
numbers = [10, 20, 30]

numbers[1] = 100

print(numbers)
```

خروجی:

```text
[10, 100, 30]
```

از Negative Indexing نیز می‌توان استفاده کرد:

```python
numbers[-1] = 500
```

می‌توان مقدار یک عنصر را بر اساس مقدار فعلی آن تغییر داد:

```python
numbers[1] += 10
```

می‌توان از Variable به عنوان Index استفاده کرد:

```python
index = 1

numbers[index] = 100
```

همچنین می‌توان Indexing را با Condition و Loop ترکیب کرد:

```python
for index in range(len(scores)):
    if scores[index] < 10:
        scores[index] = 10
```

مهم‌ترین مفهوم این بخش:

> **List یک ساختار Mutable است و می‌توان عناصر موجود آن را با استفاده از Index تغییر داد.**

---

# تمرین‌ها

## تمرین ۱ — جایگزین کردن یک عنصر

List زیر را بساز:

```python
fruits = ["Apple", "Banana", "Orange", "Mango"]
```

`"Banana"` را با `"Strawberry"` جایگزین کن.

در نهایت List را چاپ کن.

---

## تمرین ۲ — تغییر آخرین عنصر

List زیر را بساز:

```python
colors = ["Red", "Blue", "Green", "Yellow"]
```

آخرین عنصر را با `"Purple"` جایگزین کن.

برای این تمرین از Negative Indexing استفاده کن.

---

## تمرین ۳ — تغییر نمره

List زیر را بساز:

```python
scores = [18, 8, 15, 7, 20]
```

نمره دوم را `2` واحد افزایش بده.

سعی کن از این عملگر استفاده کنی:

```python
+=
```

---

## تمرین ۴ — تغییر Dynamic

یک List از چند شهر بساز.

یک Index را داخل یک Variable قرار بده و شهر موجود در آن موقعیت را با شهر دیگری جایگزین کن.

مثال:

```python
cities = ["Tehran", "Shiraz", "Tabriz", "Mashhad"]

index = 2
cities[index] = "Isfahan"

print(cities)
```

---

## تمرین ۵ — حداقل نمره قبولی

List زیر را بساز:

```python
scores = [18, 8, 15, 7, 20, 9, 17]
```

با استفاده از Loop و Indexing، هر نمره‌ای که کمتر از `10` است را با `10` جایگزین کن.

در List نهایی نباید هیچ نمره‌ای کمتر از `10` وجود داشته باشد.

---

## تمرین ۶ — افزایش تمام نمره‌ها

List زیر را بساز:

```python
scores = [10, 12, 15, 18, 20]
```

با استفاده از Loop و Indexing، تمام نمره‌ها را `1` واحد افزایش بده.

نتیجه مورد انتظار:

```text
[11, 13, 16, 19, 21]
```

---

# چالش بخش — سیستم اصلاح نمره دانش‌ آموز

برنامه‌ای بنویس که چند نمره دانش‌ آموز را داخل یک List ذخیره کند.

برنامه باید:

1. نمره‌های اولیه را نمایش دهد.
2. با استفاده از Index تمام نمره‌ها را بررسی کند.
3. هر نمره کمتر از `10` را به `10` تغییر دهد.
4. هر نمره قبولی را `1` واحد افزایش دهد.
5. نمره‌های نهایی را نمایش دهد.
6. تعداد نمره‌ها را نمایش دهد.
7. اولین نمره را نمایش دهد.
8. آخرین نمره را نمایش دهد.

ساختار نمونه:

```python
scores = [18, 8, 15, 7, 20, 9, 17]

print("----- Student Score Correction -----")
print()

print(f"Original scores: {scores}")
print()

for index in range(len(scores)):
    if scores[index] < 10:
        scores[index] = 10
    else:
        scores[index] += 1

print(f"Updated scores: {scores}")
print(f"Number of scores: {len(scores)}")
print(f"First score: {scores[0]}")
print(f"Last score: {scores[-1]}")
```

قبل از نگاه کردن به نمونه، ابتدا خودت راه‌ حل را طراحی کن.

در این Challenge چند مفهوم از درس‌های قبلی را با هم ترکیب می‌کنیم:

```text
Lists
Variables
Indexing
Negative Indexing
len()
Conditions
for loops
Assignment
Augmented Assignment
```

در بخش بعدی سراغ **List Slicing** می‌رویم و یاد می‌گیریم چگونه به جای یک عنصر، یک محدوده از عناصر List را انتخاب کنیم.

---

# بخش ۴ — برش‌ زدن List ها (List Slicing)

در این بخش یاد می‌ گیریم چگونه با استفاده از **Slicing** یک محدوده از عناصر یک List پایتون را انتخاب کنیم.

## چیزهایی که یاد می‌ گیریم

- مفهوم List Slicing
- Syntax اصلی Slicing
- Start و Stop
- مفهوم Exclusive بودن Stop
- برش‌ زدن از ابتدای List
- برش‌ زدن تا انتهای List
- انتخاب کل List
- استفاده از Index های منفی
- استفاده از Step
- برعکس کردن List با Slicing
- کپی کردن List با Slicing
- تفاوت Indexing و Slicing
- اشتباهات رایج در Slicing
- مثال‌ های کاربردی
- تمرین‌ ها
- چالش بخش

---

## ۱. List Slicing چیست؟

در بخش‌ های قبلی یاد گرفتیم که با استفاده از Indexing می‌ توانیم به **یک عنصر** دسترسی داشته باشیم:

```python
fruits = ["Apple", "Banana", "Orange", "Mango", "Sushi"]

print(fruits[1])
```

خروجی:

```text
Banana
```

اما با Slicing می‌ توانیم **چند عنصر پشت سر هم** را انتخاب کنیم:

```python
fruits = ["Apple", "Banana", "Orange", "Mango", "Sushi"]

print(fruits[1:4])
```

خروجی:

```text
['Banana', 'Orange', 'Mango']
```

بنابراین به جای انتخاب یک موقعیت، می‌ توانیم یک محدوده از موقعیت‌ های List را انتخاب کنیم.

---

## ۲. Syntax اصلی Slicing

Syntax اصلی Slicing به شکل زیر است:

```python
list_name[start:stop]
```

برای مثال:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[1:4])
```

خروجی:

```text
[20, 30, 40]
```

برش از Index شماره `1` شروع می‌ شود و قبل از Index شماره `4` متوقف می‌ شود.

بنابراین:

```text
Index 1 → شامل می‌ شود
Index 2 → شامل می‌ شود
Index 3 → شامل می‌ شود
Index 4 → شامل نمی‌ شود
```

این یکی از مهم‌ ترین قوانین Slicing در پایتون است.

---

## ۳. Start و Stop

List زیر را در نظر بگیر:

```python
numbers = [10, 20, 30, 40, 50]
```

Index ها:

```text
0 → 10
1 → 20
2 → 30
3 → 40
4 → 50
```

حالا:

```python
print(numbers[1:4])
```

یعنی:

```text
شروع از Index 1
انتخاب Index 1
انتخاب Index 2
انتخاب Index 3
توقف قبل از Index 4
```

نتیجه:

```text
[20, 30, 40]
```

---

## ۴. Stop شامل نتیجه نمی‌ شود

Index مربوط به Stop در نتیجه قرار نمی‌ گیرد.

برای مثال:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[0:3])
```

خروجی:

```text
[10, 20, 30]
```

Index شماره `3` شامل مقدار `40` است، اما این مقدار در نتیجه قرار نمی‌ گیرد.

بنابراین:

```python
numbers[0:3]
```

یعنی:

```text
Index 0
Index 1
Index 2
```

اما نه:

```text
Index 3
```

یک قانون بسیار مهم:

> **Start شامل می‌ شود، اما Stop شامل نمی‌ شود.**

---

## ۵. برش‌ زدن از ابتدای List

اگر بخواهیم Slicing را از ابتدای List شروع کنیم، می‌ توانیم Start را حذف کنیم:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[:3])
```

خروجی:

```text
[10, 20, 30]
```

این دستور معادل عبارت زیر است:

```python
numbers[0:3]
```

وقتی Start را مشخص نمی‌ کنیم، پایتون به صورت خودکار ابتدای List را در نظر می‌ گیرد.

---

## ۶. برش‌ زدن تا انتهای List

اگر بخواهیم از یک Index مشخص تا انتهای List را انتخاب کنیم، می‌ توانیم Stop را حذف کنیم:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[2:])
```

خروجی:

```text
[30, 40, 50]
```

یعنی:

```text
شروع از Index 2
ادامه تا انتهای List
```

---

## ۷. انتخاب کل List

می‌ توانیم هم Start و هم Stop را حذف کنیم:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[:])
```

خروجی:

```text
[10, 20, 30, 40, 50]
```

این دستور تمام عناصر List را انتخاب می‌ کند.

یکی از کاربرد های مهم این روش، ساختن یک **Shallow Copy** از List است:

```python
numbers = [10, 20, 30, 40, 50]

numbers_copy = numbers[:]

print(numbers_copy)
```

خروجی:

```text
[10, 20, 30, 40, 50]
```

List جدید شامل همان عناصر List اصلی است.

---

## ۸. استفاده از Index های منفی در Slicing

Slicing می‌ تواند با Negative Indexing نیز استفاده شود.

List زیر را در نظر بگیر:

```python
numbers = [10, 20, 30, 40, 50]
```

Index های منفی:

```text
-5 → 10
-4 → 20
-3 → 30
-2 → 40
-1 → 50
```

حالا:

```python
print(numbers[-3:])
```

خروجی:

```text
[30, 40, 50]
```

یعنی:

```text
شروع از Index -3
ادامه تا انتهای List
```

---

## ۹. انتخاب چند عنصر آخر List

Negative Slicing برای انتخاب چند عنصر آخر بسیار کاربردی است:

```python
students = ["Ahmad", "Sara", "Alex", "John", "Michael"]

print(students[-2:])
```

خروجی:

```text
['John', 'Michael']
```

در این مثال دو عنصر آخر انتخاب شده‌ اند.

---

## ۱۰. انتخاب همه عناصر به جز آخرین عنصر

می‌ توانیم از `-1` به عنوان Stop استفاده کنیم:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[:-1])
```

خروجی:

```text
[10, 20, 30, 40]
```

Index `-1` به آخرین عنصر اشاره می‌ کند، اما چون Stop شامل نتیجه نمی‌ شود، آخرین عنصر در خروجی قرار نمی‌ گیرد.

---

## ۱۱. استفاده از Step

Slicing یک مقدار سوم نیز دارد که به آن **Step** می‌ گوییم.

Syntax کامل:

```python
list_name[start:stop:step]
```

برای مثال:

```python
numbers = [10, 20, 30, 40, 50, 60]

print(numbers[0:6:2])
```

خروجی:

```text
[10, 30, 50]
```

در اینجا Step برابر `2` است؛ بنابراین پایتون هر دو موقعیت یک بار حرکت می‌ کند.

Index های انتخاب شده:

```text
0 → 10
2 → 30
4 → 50
```

---

## ۱۲. Slicing با Step برابر ۳

```python
numbers = [10, 20, 30, 40, 50, 60, 70, 80]

print(numbers[0:8:3])
```

خروجی:

```text
[10, 40, 70]
```

Index های انتخاب شده:

```text
0
3
6
```

---

## ۱۳. حذف Start و استفاده از Step

می‌ توانیم Start را حذف کنیم و فقط Stop و Step را مشخص کنیم:

```python
numbers = [10, 20, 30, 40, 50, 60]

print(numbers[:6:2])
```

خروجی:

```text
[10, 30, 50]
```

یعنی:

```text
شروع از ابتدای List
توقف قبل از Index 6
حرکت با Step برابر 2
```

---

## ۱۴. حذف Stop و استفاده از Step

می‌ توانیم Stop را نیز حذف کنیم:

```python
numbers = [10, 20, 30, 40, 50, 60]

print(numbers[1::2])
```

خروجی:

```text
[20, 40, 60]
```

یعنی:

```text
شروع از Index 1
ادامه تا انتهای List
حرکت با Step برابر 2
```

---

## ۱۵. برعکس کردن List

یکی از کاربردی‌ ترین روش‌ های Slicing استفاده از:

```python
list_name[::-1]
```

است.

Step منفی باعث می‌ شود پایتون از انتهای List به سمت ابتدای آن حرکت کند.

مثال:

```python
numbers = [10, 20, 30, 40, 50]

reversed_numbers = numbers[::-1]

print(reversed_numbers)
```

خروجی:

```text
[50, 40, 30, 20, 10]
```

List اصلی تغییری نمی‌ کند:

```python
print(numbers)
```

خروجی:

```text
[10, 20, 30, 40, 50]
```

---

## ۱۶. کپی کردن و برعکس کردن List به صورت هم‌ زمان

چون Slicing یک List جدید ایجاد می‌ کند، می‌ توانیم با استفاده از `[::-1]` یک نسخه برعکس شده بسازیم:

```python
numbers = [10, 20, 30, 40, 50]

reversed_numbers = numbers[::-1]

print("Original:", numbers)
print("Reversed:", reversed_numbers)
```

خروجی:

```text
Original: [10, 20, 30, 40, 50]
Reversed: [50, 40, 30, 20, 10]
```

---

## ۱۷. Slicing در String و List

Slicing فقط مخصوص List نیست.

String ها نیز از Slicing پشتیبانی می‌ کنند:

```python
name = "Python"

print(name[0:3])
```

خروجی:

```text
Pyt
```

Syntax کلی در هر دو مورد یکسان است:

```text
[start:stop:step]
```

در درس String ها نیز با Slicing آشنا شدیم و حالا همان مفهوم را روی List ها اعمال می‌ کنیم.

این موضوع یکی از نمونه‌ های مهم سازگاری Syntax در پایتون است.

---

## ۱۸. Slicing یک List از String ها

می‌ توانیم یک محدوده از List ای که شامل String است انتخاب کنیم:

```python
languages = ["Python", "Java", "C++", "JavaScript", "Go"]

print(languages[1:4])
```

خروجی:

```text
['Java', 'C++', 'JavaScript']
```

---

## ۱۹. Slicing یک List از نمره ها

فرض کنیم نمره های یک دانش‌ آموز را داریم:

```python
scores = [18, 8, 15, 7, 20, 17, 19]

print(scores[1:5])
```

خروجی:

```text
[8, 15, 7, 20]
```

در این مثال نمره های موجود از Index `1` تا قبل از Index `5` انتخاب شده‌ اند.

---

## ۲۰. مثال کاربردی — نمره های اخیر

فرض کنیم یک سیستم، نمره چند آزمون اخیر را ذخیره می‌ کند:

```python
scores = [15, 17, 18, 14, 20, 19, 16]

recent_scores = scores[-3:]

print(f"Recent scores: {recent_scores}")
```

خروجی:

```text
Recent scores: [20, 19, 16]
```

Negative Slicing باعث می‌ شود انتخاب چند داده آخر ساده و خوانا باشد.

---

## ۲۱. مثال کاربردی — پنج محصول اول

فرض کنیم یک فروشگاه آنلاین چند محصول دارد:

```python
products = [
    "Laptop",
    "Phone",
    "Tablet",
    "Keyboard",
    "Mouse",
    "Monitor",
    "Headphones"
]

first_five = products[:5]

print(first_five)
```

خروجی:

```text
['Laptop', 'Phone', 'Tablet', 'Keyboard', 'Mouse']
```

---

## ۲۲. مثال کاربردی — انتخاب هر دومین محصول

می‌ توانیم هر دومین عنصر را انتخاب کنیم:

```python
products = [
    "Laptop",
    "Phone",
    "Tablet",
    "Keyboard",
    "Mouse",
    "Monitor"
]

selected_products = products[::2]

print(selected_products)
```

خروجی:

```text
['Laptop', 'Tablet', 'Mouse']
```

---

## ۲۳. Slicing، List اصلی را تغییر نمی‌ دهد

Slicing به طور معمول یک List جدید ایجاد می‌ کند:

```python
numbers = [10, 20, 30, 40, 50]

part = numbers[1:4]

print("Original:", numbers)
print("Part:", part)
```

خروجی:

```text
Original: [10, 20, 30, 40, 50]
Part: [20, 30, 40]
```

List اصلی تغییری نکرده است.

این رفتار با تغییر مستقیم یک عنصر متفاوت است:

```python
numbers[1] = 100
```

این دستور List اصلی را تغییر می‌ دهد.

---

## ۲۴. تفاوت Indexing و Slicing

Indexing:

```python
numbers = [10, 20, 30]

print(numbers[1])
```

یک عنصر را برمی‌ گرداند:

```text
20
```

اما Slicing:

```python
print(numbers[1:2])
```

یک List جدید برمی‌ گرداند:

```text
[20]
```

این تفاوت بسیار مهم است:

```text
numbers[1]   → یک عنصر
numbers[1:2] → یک List شامل یک عنصر
```

---

# اشتباهات رایج

## اشتباه ۱ — انتظار داشتن Stop در نتیجه

کد زیر:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[1:4])
```

Index شماره `4` را در نتیجه قرار نمی‌ دهد.

خروجی:

```text
[20, 30, 40]
```

همیشه به خاطر داشته باش:

```text
Start → شامل
Stop  → غیر شامل
```

---

## اشتباه ۲ — اشتباه گرفتن Indexing با Slicing

این:

```python
numbers[2]
```

یک عنصر را برمی‌ گرداند.

اما این:

```python
numbers[2:3]
```

یک List برمی‌ گرداند.

---

## اشتباه ۳ — استفاده از Step برابر صفر

Step برابر `0` معتبر نیست:

```python
numbers = [10, 20, 30, 40]

print(numbers[::0])
```

پایتون خطای زیر را ایجاد می‌ کند:

```text
ValueError: slice step cannot be zero
```

بنابراین Step نباید صفر باشد.

---

## اشتباه ۴ — فراموش کردن تأثیر Step منفی

برای مثال:

```python
numbers = [10, 20, 30, 40, 50]

print(numbers[::-1])
```

نتیجه:

```text
[50, 40, 30, 20, 10]
```

Step منفی باعث می‌ شود حرکت در List از سمت راست به چپ انجام شود.

---

# نکات کلیدی

Syntax اصلی Slicing:

```python
list_name[start:stop]
```

Syntax کامل:

```python
list_name[start:stop:step]
```

مهم‌ ترین قانون:

```text
Start شامل می‌ شود.
Stop شامل نمی‌ شود.
```

مثال‌ های مهم:

```python
numbers[:3]
numbers[2:]
numbers[:]
numbers[-3:]
numbers[::2]
numbers[::-1]
```

Slicing می‌ تواند برای موارد زیر استفاده شود:

- انتخاب یک محدوده از عناصر
- انتخاب چند عنصر ابتدایی
- انتخاب چند عنصر انتهایی
- انتخاب هر N امین عنصر
- برعکس کردن List
- ساختن یک Shallow Copy

ایده اصلی این بخش:

> **List Slicing به ما اجازه می‌ دهد با استفاده از یک Syntax کوتاه و قدرتمند، محدوده ای از عناصر List را انتخاب کنیم.**

---

# تمرین ها

## تمرین ۱ — برش ساده

List زیر را بساز:

```python
numbers = [10, 20, 30, 40, 50, 60]
```

عناصر زیر را انتخاب کن:

```text
20, 30, 40
```

---

## تمرین ۲ — انتخاب عناصر اول

List زیر را بساز:

```python
fruits = ["Apple", "Banana", "Orange", "Mango", "Sushi"]
```

سه عنصر اول را انتخاب کن.

---

## تمرین ۳ — انتخاب عناصر آخر

List زیر را بساز:

```python
students = ["Ahmad", "Sara", "Alex", "John", "Michael"]
```

دو دانش‌ آموز آخر را با استفاده از Negative Slicing انتخاب کن.

---

## تمرین ۴ — انتخاب هر دومین عنصر

List زیر را بساز:

```python
numbers = [10, 20, 30, 40, 50, 60, 70, 80]
```

هر دومین عنصر را انتخاب کن.

نتیجه مورد انتظار:

```text
[10, 30, 50, 70]
```

---

## تمرین ۵ — برعکس کردن List

List زیر را بساز:

```python
numbers = [1, 2, 3, 4, 5]
```

با استفاده از Slicing یک نسخه برعکس شده ایجاد کن.

نتیجه مورد انتظار:

```text
[5, 4, 3, 2, 1]
```

---

## تمرین ۶ — کپی کردن List

List زیر را بساز:

```python
languages = ["Python", "Java", "C++", "Go"]
```

با استفاده از:

```python
[:]
```

یک کپی از List ایجاد کن.

سپس هر دو List را چاپ کن.

---

# چالش بخش — تحلیل داده های List

برنامه ای بنویس که با List زیر کار کند:

```python
scores = [18, 12, 15, 9, 20, 17, 14, 19, 11, 16]
```

برنامه باید:

1. کل List را نمایش دهد.
2. سه نمره اول را نمایش دهد.
3. سه نمره آخر را نمایش دهد.
4. بخش میانی List را نمایش دهد.
5. هر دومین نمره را نمایش دهد.
6. List برعکس شده را نمایش دهد.
7. با استفاده از Slicing یک کپی از List ایجاد کند.
8. List اصلی و List کپی شده را نمایش دهد.

تا جای ممکن سعی کن Challenge را فقط با استفاده از قابلیت های Slicing حل کنی.

ساختار نمونه:

```python
scores = [18, 12, 15, 9, 20, 17, 14, 19, 11, 16]

first_three = scores[:3]
last_three = scores[-3:]
middle = scores[3:7]
every_second = scores[::2]
reversed_scores = scores[::-1]
scores_copy = scores[:]

print("----- Score Analyzer -----")
print()

print(f"All scores: {scores}")
print(f"First three: {first_three}")
print(f"Last three: {last_three}")
print(f"Middle: {middle}")
print(f"Every second score: {every_second}")
print(f"Reversed: {reversed_scores}")
print(f"Copy: {scores_copy}")
```

این Challenge چند مفهوم را با یکدیگر ترکیب می‌ کند:

```text
Lists
Indexing
Negative Indexing
Slicing
Variables
String Formatting
```

در بخش بعدی سراغ **List Methods** می‌ رویم و با متدهایی مانند `append()`، `insert()`، `remove()` و `pop()` کار خواهیم کرد.

---

# بخش ۵ — متد های List

در این بخش یاد می‌ گیریم چگونه با استفاده از متد های داخلی Python، روی List ها عملیات مختلف انجام دهیم.

متد های List به ما اجازه می‌ دهند بدون پیاده‌ سازی دستی عملیات، عناصر را اضافه کنیم، حذف کنیم، جست‌ و جو کنیم، مرتب کنیم و ساختار List را مدیریت کنیم.

## چیزهایی که یاد می‌ گیریم

- مفهوم List Methods
- متد `append()`
- متد `insert()`
- متد `extend()`
- متد `remove()`
- متد `pop()`
- متد `clear()`
- متد `index()`
- متد `count()`
- متد `sort()`
- متد `reverse()`
- تفاوت `sort()` و `sorted()`
- تفاوت `reverse()` و `[::-1]`
- Return Value متد های List
- اشتباهات رایج در استفاده از List Methods
- مثال‌ های کاربردی
- تمرین‌ های ترکیبی
- چالش نهایی بخش

---

## ۱. List Method چیست؟

List Method یک عملیات داخلی است که به یک List تعلق دارد.

برای مثال:

```python
numbers = [10, 20, 30]

numbers.append(40)

print(numbers)
```

خروجی:

```text
[10, 20, 30, 40]
```

متد:

```python
append()
```

با اضافه کردن یک عنصر جدید، List را تغییر می‌ دهد.

متد های List با استفاده از **Dot Notation** فراخوانی می‌ شوند:

```python
list_name.method_name()
```

برخی متد ها نیز Argument دریافت می‌ کنند:

```python
list_name.method_name(argument)
```

برای مثال:

```python
numbers.append(40)
```

در این مثال:

- `numbers` همان List است.
- `append` نام متد است.
- `40` همان Argument است.

---

# ۲. متد `append()`

متد `append()` **یک عنصر را به انتهای List اضافه می‌ کند.**

مثال:

```python
numbers = [10, 20, 30]

numbers.append(40)

print(numbers)
```

خروجی:

```text
[10, 20, 30, 40]
```

عنصر جدید همیشه به انتهای List اضافه می‌ شود.

---

## ۲.۱ اضافه کردن String با `append()`

`append()` می‌ تواند مقادیر با Data Type های مختلف را اضافه کند:

```python
languages = ["Python", "Java", "C++"]

languages.append("Go")

print(languages)
```

خروجی:

```text
['Python', 'Java', 'C++', 'Go']
```

---

## ۲.۲ استفاده چند باره از `append()`

می‌ توانیم `append()` را چند بار اجرا کنیم:

```python
numbers = []

numbers.append(10)
numbers.append(20)
numbers.append(30)
numbers.append(40)

print(numbers)
```

خروجی:

```text
[10, 20, 30, 40]
```

این روش زمانی کاربرد دارد که List را به صورت تدریجی بسازیم.

---

## ۲.۳ `append()` یک Object را اضافه می‌ کند

نکته مهم این است که `append()` مقدار دریافت شده را به عنوان **یک عنصر** اضافه می‌ کند.

برای مثال:

```python
numbers = [1, 2, 3]

numbers.append([4, 5])

print(numbers)
```

خروجی:

```text
[1, 2, 3, [4, 5]]
```

در اینجا List `[4, 5]` به عنوان یک عنصر داخل `numbers` قرار گرفته است.

ساختار نهایی:

```text
1
2
3
[4, 5]
```

این رفتار هنگام کار با Nested Lists بسیار مهم است.

---

# ۳. متد `insert()`

متد `insert()` یک عنصر را در یک Index مشخص اضافه می‌ کند.

Syntax:

```python
list_name.insert(index, value)
```

مثال:

```python
numbers = [10, 20, 40]

numbers.insert(2, 30)

print(numbers)
```

خروجی:

```text
[10, 20, 30, 40]
```

مقدار `30` در Index شماره `2` قرار گرفته است.

---

## ۳.۱ درک Index هنگام `insert()`

قبل از Insert:

```text
Index 0 → 10
Index 1 → 20
Index 2 → 40
```

بعد از:

```python
numbers.insert(2, 30)
```

ساختار List به این صورت می‌ شود:

```text
Index 0 → 10
Index 1 → 20
Index 2 → 30
Index 3 → 40
```

عناصر قبلی از محل درج به بعد، یک موقعیت به سمت راست منتقل می‌ شوند.

---

## ۳.۲ اضافه کردن عنصر در ابتدای List

می‌ توانیم یک عنصر را در Index `0` قرار دهیم:

```python
names = ["Sara", "Alex", "John"]

names.insert(0, "Ahmad")

print(names)
```

خروجی:

```text
['Ahmad', 'Sara', 'Alex', 'John']
```

---

## ۳.۳ اضافه کردن عنصر در انتهای List با `insert()`

می‌ توانیم از `insert()` برای اضافه کردن یک عنصر در انتها نیز استفاده کنیم:

```python
numbers = [10, 20, 30]

numbers.insert(len(numbers), 40)

print(numbers)
```

خروجی:

```text
[10, 20, 30, 40]
```

اما اگر هدف فقط اضافه کردن عنصر به انتهای List باشد، استفاده از `append()` واضح‌ تر و خواناتر است:

```python
numbers.append(40)
```

بهتر است متدی را انتخاب کنیم که Intent کد را بهتر نشان دهد.

---

# ۴. متد `extend()`

متد `extend()` چندین عنصر را از یک Iterable گرفته و به انتهای List اضافه می‌ کند.

مثال:

```python
numbers = [1, 2, 3]

numbers.extend([4, 5, 6])

print(numbers)
```

خروجی:

```text
[1, 2, 3, 4, 5, 6]
```

برخلاف `append()`، متد `extend()` عناصر را به صورت جداگانه اضافه می‌ کند.

---

## ۴.۱ تفاوت `append()` و `extend()`

این تفاوت بسیار مهم است.

با `append()`:

```python
numbers = [1, 2, 3]

numbers.append([4, 5])

print(numbers)
```

خروجی:

```text
[1, 2, 3, [4, 5]]
```

اما با `extend()`:

```python
numbers = [1, 2, 3]

numbers.extend([4, 5])

print(numbers)
```

خروجی:

```text
[1, 2, 3, 4, 5]
```

خلاصه:

```text
append()  → یک Object را اضافه می‌ کند
extend()  → عناصر یک Iterable را اضافه می‌ کند
```

---

## ۴.۲ استفاده از `extend()` با یک List دیگر

```python
first_group = ["Ahmad", "Sara"]
second_group = ["Alex", "John"]

first_group.extend(second_group)

print(first_group)
```

خروجی:

```text
['Ahmad', 'Sara', 'Alex', 'John']
```

عناصر `second_group` به `first_group` اضافه شده‌ اند.

---

## ۴.۳ استفاده از `extend()` با String

از آنجا که String ها Iterable هستند، `extend()` می‌ تواند حروف آن ها را به صورت جداگانه اضافه کند:

```python
letters = ["A", "B"]

letters.extend("CD")

print(letters)
```

خروجی:

```text
['A', 'B', 'C', 'D']
```

این مثال نشان می‌ دهد که درک مفهوم Iterable در پایتون اهمیت زیادی دارد.

---

# ۵. متد `remove()`

متد `remove()` **اولین وقوع یک مقدار مشخص** را از List حذف می‌ کند.

مثال:

```python
numbers = [10, 20, 30, 20, 40]

numbers.remove(20)

print(numbers)
```

خروجی:

```text
[10, 30, 20, 40]
```

فقط اولین `20` حذف شده است.

---

## ۵.۱ `remove()` با Value کار می‌ کند، نه Index

این:

```python
numbers.remove(30)
```

یعنی:

> اولین عنصری را که مقدار آن `30` است پیدا کن و حذف کن.

این دستور به معنی:

> عنصر موجود در Index شماره `30` را حذف کن.

نیست.

برای حذف عنصر بر اساس Index از `pop()` استفاده می‌ کنیم.

---

## ۵.۲ حذف یک String

```python
fruits = ["Apple", "Banana", "Orange", "Mango"]

fruits.remove("Orange")

print(fruits)
```

خروجی:

```text
['Apple', 'Banana', 'Mango']
```

---

## ۵.۳ اگر مقدار مورد نظر وجود نداشته باشد چه می‌ شود؟

اگر مقدار مورد نظر در List وجود نداشته باشد، پایتون یک `ValueError` ایجاد می‌ کند:

```python
numbers = [10, 20, 30]

numbers.remove(50)
```

خطایی مشابه زیر ایجاد می‌ شود:

```text
ValueError: list.remove(x): x not in list
```

بنابراین اگر مطمئن نیستیم مقدار وجود دارد یا نه، بهتر است ابتدا آن را بررسی کنیم:

```python
numbers = [10, 20, 30]

if 50 in numbers:
    numbers.remove(50)

print(numbers)
```

خروجی:

```text
[10, 20, 30]
```

---

# ۶. متد `pop()`

متد `pop()` یک عنصر را بر اساس Index حذف می‌ کند و **عنصر حذف شده را برمی‌ گرداند.**

مثال:

```python
numbers = [10, 20, 30, 40]

removed_number = numbers.pop(2)

print("Removed:", removed_number)
print("Numbers:", numbers)
```

خروجی:

```text
Removed: 30
Numbers: [10, 20, 40]
```

این ویژگی باعث می‌ شود `pop()` با `remove()` تفاوت مهمی داشته باشد.

---

## ۶.۱ استفاده از `pop()` بدون Index

اگر Index مشخص نکنیم، `pop()` آخرین عنصر List را حذف می‌ کند:

```python
numbers = [10, 20, 30, 40]

removed_number = numbers.pop()

print("Removed:", removed_number)
print("Numbers:", numbers)
```

خروجی:

```text
Removed: 40
Numbers: [10, 20, 30]
```

این یکی از رایج‌ ترین کاربرد های `pop()` است.

---

## ۶.۲ استفاده از `pop()` با Index مشخص

```python
numbers = [10, 20, 30, 40, 50]

removed_number = numbers.pop(1)

print("Removed:", removed_number)
print("Numbers:", numbers)
```

خروجی:

```text
Removed: 20
Numbers: [10, 30, 40, 50]
```

عنصر موجود در Index `1` حذف شده است.

---

## ۶.۳ استفاده از Index منفی با `pop()`

`pop()` از Negative Indexing نیز پشتیبانی می‌ کند:

```python
numbers = [10, 20, 30, 40, 50]

removed_number = numbers.pop(-2)

print("Removed:", removed_number)
print("Numbers:", numbers)
```

خروجی:

```text
Removed: 40
Numbers: [10, 20, 30, 50]
```

---

# ۷. متد `clear()`

متد `clear()` تمام عناصر موجود در List را حذف می‌ کند.

مثال:

```python
numbers = [10, 20, 30, 40]

numbers.clear()

print(numbers)
```

خروجی:

```text
[]
```

خود List همچنان وجود دارد، اما دیگر عنصری داخل آن نیست.

---

## ۷.۱ تفاوت `clear()` و ساختن یک List جدید

این دو عملیات از نظر مفهومی همیشه یکسان نیستند.

با:

```python
numbers.clear()
```

List موجود را خالی می‌ کنیم.

اما با:

```python
numbers = []
```

متغیر را به یک List جدید و خالی متصل می‌ کنیم.

برای این بخش فعلاً این تفاوت را به خاطر بسپار:

```text
clear() → List موجود را خالی می‌ کند
[]      → یک List جدید ایجاد می‌ کند
```

---

# ۸. متد `index()`

متد `index()` Index مربوط به **اولین وقوع** یک مقدار را برمی‌ گرداند.

مثال:

```python
fruits = ["Apple", "Banana", "Orange", "Banana"]

position = fruits.index("Banana")

print(position)
```

خروجی:

```text
1
```

اولین `"Banana"` در Index شماره `1` قرار دارد.

---

## ۸.۱ `index()` و مقادیر تکراری

اگر یک مقدار چند بار در List وجود داشته باشد، `index()` اولین مورد را برمی‌ گرداند:

```python
numbers = [10, 20, 30, 20, 40]

position = numbers.index(20)

print(position)
```

خروجی:

```text
1
```

Index شماره `3` برگردانده نمی‌ شود، چون Index شماره `1` اولین وقوع `20` است.

---

## ۸.۲ جست‌ و جو از یک Index مشخص

`index()` می‌ تواند Start و Stop اختیاری نیز دریافت کند:

```python
numbers = [10, 20, 30, 20, 40]

position = numbers.index(20, 2)

print(position)
```

خروجی:

```text
3
```

جست‌ و جو از Index شماره `2` شروع شده است؛ بنابراین دومین `20` پیدا می‌ شود.

---

# ۹. متد `count()`

متد `count()` تعداد دفعاتی را که یک مقدار در List ظاهر شده است، برمی‌ گرداند.

مثال:

```python
numbers = [10, 20, 20, 30, 20, 40]

number_of_twenty = numbers.count(20)

print(number_of_twenty)
```

خروجی:

```text
3
```

مقدار `20` سه بار در List وجود دارد.

---

## ۹.۱ شمارش String ها

```python
fruits = ["Apple", "Banana", "Apple", "Orange", "Apple"]

apple_count = fruits.count("Apple")

print(apple_count)
```

خروجی:

```text
3
```

---

# ۱۰. متد `sort()`

متد `sort()` یک List را **در همان List و به صورت In-Place** مرتب می‌ کند.

برای اعداد:

```python
numbers = [40, 10, 30, 20, 50]

numbers.sort()

print(numbers)
```

خروجی:

```text
[10, 20, 30, 40, 50]
```

List اصلی تغییر کرده است.

---

## ۱۰.۱ مرتب‌ سازی نزولی

می‌ توانیم از Argument به نام `reverse` استفاده کنیم:

```python
numbers = [40, 10, 30, 20, 50]

numbers.sort(reverse=True)

print(numbers)
```

خروجی:

```text
[50, 40, 30, 20, 10]
```

---

## ۱۰.۲ مرتب‌ سازی String ها

String ها نیز می‌ توانند مرتب شوند:

```python
names = ["Sara", "Ahmad", "John", "Alex"]

names.sort()

print(names)
```

خروجی:

```text
['Ahmad', 'Alex', 'John', 'Sara']
```

ترتیب بر اساس قوانین Ordering مربوط به مقادیر انجام می‌ شود.

---

# ۱۱. متد `reverse()`

متد `reverse()` ترتیب عناصر List را **در همان List** معکوس می‌ کند.

مثال:

```python
numbers = [10, 20, 30, 40, 50]

numbers.reverse()

print(numbers)
```

خروجی:

```text
[50, 40, 30, 20, 10]
```

List اصلی تغییر کرده است.

---

## ۱۱.۱ `reverse()` مرتب‌ سازی نمی‌ کند

این تفاوت بسیار مهم است.

متد `reverse()` فقط جهت ترتیب موجود را عوض می‌ کند.

```python
numbers = [30, 10, 50, 20, 40]

numbers.reverse()

print(numbers)
```

خروجی:

```text
[40, 20, 50, 10, 30]
```

مقادیر مرتب نشده‌ اند.

فقط ترتیب قبلی برعکس شده است.

---

# ۱۲. تفاوت `sort()` و `sorted()`

این موضوع یکی از نکات مهم در کار با List ها است.

`sort()` یک List Method است:

```python
numbers.sort()
```

و List اصلی را تغییر می‌ دهد.

اما `sorted()` یک Built-in Function در پایتون است:

```python
sorted(numbers)
```

و یک List جدید و مرتب شده برمی‌ گرداند.

مثال:

```python
numbers = [40, 10, 30, 20, 50]

sorted_numbers = sorted(numbers)

print("Original:", numbers)
print("Sorted:", sorted_numbers)
```

خروجی:

```text
Original: [40, 10, 30, 20, 50]
Sorted: [10, 20, 30, 40, 50]
```

List اصلی تغییری نکرده است.

در مقابل:

```python
numbers = [40, 10, 30, 20, 50]

numbers.sort()

print(numbers)
```

خروجی:

```text
[10, 20, 30, 40, 50]
```

در این حالت List اصلی تغییر کرده است.

---

# ۱۳. تفاوت `reverse()` و `[::-1]`

هر دو روش می‌ توانند ترتیب یک List را معکوس کنند، اما رفتار آن ها یکسان نیست.

با `reverse()`:

```python
numbers = [10, 20, 30, 40]

numbers.reverse()

print(numbers)
```

List اصلی تغییر می‌ کند.

با Slicing:

```python
numbers = [10, 20, 30, 40]

reversed_numbers = numbers[::-1]

print("Original:", numbers)
print("Reversed:", reversed_numbers)
```

خروجی:

```text
Original: [10, 20, 30, 40]
Reversed: [40, 30, 20, 10]
```

List اصلی بدون تغییر باقی می‌ ماند.

بنابراین:

```text
reverse() → List اصلی را تغییر می‌ دهد
[::-1]    → یک List برعکس شده جدید ایجاد می‌ کند
```

---

# ۱۴. Return Value متد های List

یکی از اشتباهات رایج مبتدیان این است که تصور کنند متد های List همیشه List تغییر یافته را برمی‌ گردانند.

این تصور درست نیست.

برای مثال:

```python
numbers = [10, 20, 30]

result = numbers.append(40)

print(result)
```

خروجی:

```text
None
```

اما خود List تغییر کرده است:

```python
print(numbers)
```

خروجی:

```text
[10, 20, 30, 40]
```

بنابراین:

```text
append() → List را تغییر می‌ دهد
append() → مقدار None را برمی‌ گرداند
```

---

## ۱۴.۱ مثال دیگر با `sort()`

```python
numbers = [30, 10, 20]

result = numbers.sort()

print(result)
print(numbers)
```

خروجی:

```text
None
[10, 20, 30]
```

دوباره می‌ بینیم که `sort()` List اصلی را تغییر می‌ دهد، اما `None` برمی‌ گرداند.

---

## ۱۴.۲ متد هایی که مقدار مفید برمی‌ گردانند

برخی متد ها اطلاعاتی را برمی‌ گردانند.

برای مثال:

```python
numbers = [10, 20, 30]

removed = numbers.pop()

print(removed)
```

خروجی:

```text
30
```

یا:

```python
numbers = [10, 20, 30]

position = numbers.index(20)

print(position)
```

خروجی:

```text
1
```

و:

```python
numbers = [10, 20, 20, 30]

total = numbers.count(20)

print(total)
```

خروجی:

```text
2
```

درک Return Value متد ها برای نوشتن برنامه‌ های بزرگ‌ تر اهمیت زیادی دارد.

---

# ۱۵. مقایسه سریع متد های مهم List

| متد | کاربرد | List را تغییر می‌ دهد؟ | Return Value |
|---|---|---:|---|
| `append()` | اضافه کردن یک عنصر به انتها | بله | `None` |
| `insert()` | اضافه کردن یک عنصر در Index مشخص | بله | `None` |
| `extend()` | اضافه کردن عناصر یک Iterable | بله | `None` |
| `remove()` | حذف اولین Value مشابه | بله | `None` |
| `pop()` | حذف و برگرداندن یک عنصر | بله | عنصر حذف شده |
| `clear()` | حذف تمام عناصر | بله | `None` |
| `index()` | پیدا کردن اولین Index مشابه | خیر | Index |
| `count()` | شمارش تعداد وقوع | خیر | Number |
| `sort()` | مرتب‌ سازی In-Place | بله | `None` |
| `reverse()` | معکوس کردن In-Place | بله | `None` |

این جدول برای مرور سریع مفید است، اما درک رفتار هر متد از حفظ کردن جدول مهم‌ تر است.

---

# ۱۶. مثال کاربردی — مدیریت Shopping List

می‌ توانیم چند List Method را در یک برنامه واقعی ترکیب کنیم:

```python
shopping_list = ["Milk", "Bread", "Eggs"]

shopping_list.append("Cheese")
shopping_list.insert(1, "Butter")
shopping_list.remove("Bread")

print("Shopping List:")
print(shopping_list)
```

خروجی:

```text
Shopping List:
['Milk', 'Butter', 'Eggs', 'Cheese']
```

در این مثال از موارد زیر استفاده کردیم:

```text
append()
insert()
remove()
```

---

# ۱۷. مثال کاربردی — پردازش نمره های دانش‌ آموزان

فرض کنیم نمره های جدیدی دریافت کرده‌ ایم:

```python
scores = [18, 12, 15, 9]

new_scores = [20, 17, 14]

scores.extend(new_scores)

scores.sort()

print(scores)
```

خروجی:

```text
[9, 12, 14, 15, 17, 18, 20]
```

در این مثال چند عملیات List را ترکیب کرده‌ ایم:

```text
extend()
sort()
```

---

# ۱۸. مثال کاربردی — حذف و ذخیره یک Task

فرض کنیم یک Queue از Task ها داریم:

```python
tasks = [
    "Study Python",
    "Practice Lists",
    "Read a Book",
    "Exercise"
]

completed_task = tasks.pop(1)

print(f"Completed: {completed_task}")
print(f"Remaining tasks: {tasks}")
```

خروجی:

```text
Completed: Practice Lists
Remaining tasks: ['Study Python', 'Read a Book', 'Exercise']
```

چون `pop()` عنصر حذف شده را برمی‌ گرداند، می‌ توانیم آن را ذخیره کنیم و بعداً استفاده کنیم.

---

# ۱۹. مثال کاربردی — بررسی داده های تکراری

فرض کنیم می‌ خواهیم بدانیم یک نمره چند بار تکرار شده است:

```python
scores = [18, 15, 20, 15, 17, 15, 19]

count_of_fifteen = scores.count(15)

print(f"Score 15 appears {count_of_fifteen} times.")
```

خروجی:

```text
Score 15 appears 3 times.
```

---

# ۲۰. مثال کاربردی — پیدا کردن یک عنصر

```python
languages = ["Python", "Java", "C++", "JavaScript"]

language = "C++"

if language in languages:
    position = languages.index(language)
    print(f"{language} found at Index {position}.")
else:
    print(f"{language} was not found.")
```

خروجی:

```text
C++ found at Index 2.
```

استفاده از `in` قبل از `index()` باعث می‌ شود اگر مقدار وجود نداشت، خطا دریافت نکنیم.

---

# اشتباهات رایج

## اشتباه ۱ — قرار دادن نتیجه `append()` داخل List

روش اشتباه:

```python
numbers = [10, 20, 30]

numbers = numbers.append(40)

print(numbers)
```

نتیجه:

```text
None
```

چرا؟

چون `append()` List را تغییر می‌ دهد و `None` برمی‌ گرداند.

روش صحیح:

```python
numbers = [10, 20, 30]

numbers.append(40)

print(numbers)
```

---

## اشتباه ۲ — استفاده از `append()` به جای `extend()`

این:

```python
numbers = [1, 2, 3]

numbers.append([4, 5])

print(numbers)
```

نتیجه:

```text
[1, 2, 3, [4, 5]]
```

اگر هدف اضافه کردن `4` و `5` به عنوان دو عنصر جداگانه باشد، باید از `extend()` استفاده کنیم:

```python
numbers = [1, 2, 3]

numbers.extend([4, 5])

print(numbers)
```

خروجی:

```text
[1, 2, 3, 4, 5]
```

---

## اشتباه ۳ — اشتباه گرفتن `remove()` و `pop()`

`remove()` با Value کار می‌ کند:

```python
numbers.remove(30)
```

اما `pop()` با Index کار می‌ کند:

```python
numbers.pop(2)
```

یک قانون ساده:

```text
remove(value)
pop(index)
```

---

## اشتباه ۴ — استفاده از `remove()` برای مقدار غیر موجود

کد زیر می‌ تواند خطا ایجاد کند:

```python
numbers = [10, 20, 30]

numbers.remove(50)
```

روش امن‌ تر:

```python
numbers = [10, 20, 30]

if 50 in numbers:
    numbers.remove(50)
```

---

## اشتباه ۵ — تصور اینکه `reverse()` List را مرتب می‌ کند

این:

```python
numbers = [30, 10, 20]

numbers.reverse()

print(numbers)
```

نتیجه:

```text
[20, 10, 30]
```

و نه:

```text
[10, 20, 30]
```

`reverse()` جهت ترتیب را تغییر می‌ دهد.

`sort()` ترتیب عناصر را بر اساس قوانین مرتب‌ سازی تغییر می‌ دهد.

---

## اشتباه ۶ — فراموش کردن اینکه `sort()` List اصلی را تغییر می‌ دهد

```python
numbers = [30, 10, 20]

numbers.sort()

print(numbers)
```

List اصلی اکنون:

```text
[10, 20, 30]
```

است.

اگر می‌ خواهیم List اصلی حفظ شود، می‌ توانیم از `sorted()` استفاده کنیم:

```python
numbers = [30, 10, 20]

sorted_numbers = sorted(numbers)

print("Original:", numbers)
print("Sorted:", sorted_numbers)
```

---

# نکات کلیدی

List Methods روش‌ های آماده و قدرتمندی برای مدیریت داده های موجود در List هستند.

مهم‌ ترین متد های این بخش:

```python
append()
insert()
extend()
remove()
pop()
clear()
index()
count()
sort()
reverse()
```

تفاوت های مهم را به خاطر بسپار:

```text
append(value)
→ اضافه کردن یک Object به انتهای List

insert(index, value)
→ اضافه کردن یک Object در یک موقعیت مشخص

extend(iterable)
→ اضافه کردن عناصر یک Iterable

remove(value)
→ حذف اولین مقدار مشابه

pop(index)
→ حذف و برگرداندن یک عنصر بر اساس Index

pop()
→ حذف و برگرداندن آخرین عنصر

clear()
→ خالی کردن List

index(value)
→ پیدا کردن اولین Index مشابه

count(value)
→ شمارش تعداد وقوع یک مقدار

sort()
→ مرتب کردن List اصلی

reverse()
→ معکوس کردن List اصلی
```

همچنین:

```text
sort()     → List را تغییر می‌ دهد
sorted()   → یک List مرتب شده جدید برمی‌ گرداند

reverse()  → List را تغییر می‌ دهد
[::-1]     → یک List برعکس شده جدید ایجاد می‌ کند
```

یکی از مهم‌ ترین مفاهیم این بخش:

> **بسیاری از List Methods، List اصلی را تغییر می‌ دهند و `None` برمی‌ گردانند.**

درک این رفتار از بسیاری از اشتباهات رایج در ابتدای مسیر جلوگیری می‌ کند.

---

# تمرین ها

## تمرین ۱ — ساختن یک List

از یک List خالی شروع کن:

```python
numbers = []
```

با استفاده از `append()` مقادیر زیر را اضافه کن:

```text
10
20
30
40
50
```

سپس List را چاپ کن.

---

## تمرین ۲ — درج یک مقدار

از List زیر شروع کن:

```python
numbers = [10, 20, 40, 50]
```

با استفاده از `insert()` مقدار `30` را بین `20` و `40` قرار بده.

نتیجه مورد انتظار:

```text
[10, 20, 30, 40, 50]
```

---

## تمرین ۳ — مقایسه `append()` و `extend()`

List زیر را ایجاد کن:

```python
numbers = [1, 2, 3]
```

ابتدا با `append()` مقدار:

```python
[4, 5]
```

را اضافه کن.

سپس یک List دیگر ایجاد کن و با `extend()` همان:

```python
[4, 5]
```

را اضافه کن.

نتیجه ها را با یکدیگر مقایسه کن.

---

## تمرین ۴ — حذف یک Value

List زیر را ایجاد کن:

```python
fruits = ["Apple", "Banana", "Orange", "Mango", "Banana"]
```

اولین `"Banana"` را حذف کن.

چه اتفاقی برای `"Banana"` دوم می‌ افتد؟

---

## تمرین ۵ — استفاده از `pop()` و ذخیره مقدار

List زیر را ایجاد کن:

```python
tasks = ["Study", "Exercise", "Read", "Sleep"]
```

با استفاده از `pop()` آخرین Task را حذف کن.

مقدار حذف شده را داخل یک متغیر ذخیره کن و آن را چاپ کن.

---

## تمرین ۶ — شمارش وقوع

List زیر را ایجاد کن:

```python
numbers = [10, 20, 10, 30, 10, 40, 20]
```

با استفاده از `count()` مشخص کن مقدار `10` چند بار ظاهر شده است.

---

## تمرین ۷ — پیدا کردن Index

List زیر را ایجاد کن:

```python
languages = ["Python", "Java", "C++", "Go"]
```

با استفاده از `index()` موقعیت `"C++"` را پیدا کن.

---

## تمرین ۸ — مرتب‌ سازی List

List زیر را ایجاد کن:

```python
scores = [15, 8, 19, 12, 20, 10]
```

List را به صورت صعودی مرتب کن.

سپس یک کپی دیگر را به صورت نزولی مرتب کن.

---

## تمرین ۹ — برعکس کردن بدون تغییر List اصلی

List زیر را ایجاد کن:

```python
numbers = [1, 2, 3, 4, 5]
```

بدون تغییر دادن List اصلی، یک نسخه برعکس شده ایجاد کن.

---

# چالش بخش — Student Score Manager

برنامه‌ ای بنویس که نمره های یک دانش‌ آموز را مدیریت کند.

با List زیر شروع کن:

```python
scores = [18, 12, 15, 9, 20]
```

برنامه باید:

1. با استفاده از `append()` یک نمره جدید اضافه کند.
2. با استفاده از `insert()` یک نمره را در موقعیت مشخص قرار دهد.
3. با استفاده از `extend()` چند نمره جدید اضافه کند.
4. با استفاده از `remove()` یک نمره مشخص را حذف کند.
5. با استفاده از `pop()` آخرین نمره را حذف کرده و آن را ذخیره کند.
6. تعداد وقوع یک نمره مشخص را با `count()` پیدا کند.
7. Index یک نمره مشخص را با `index()` پیدا کند.
8. با استفاده از `sorted()` یک نسخه مرتب شده ایجاد کند.
9. List اصلی را با `sort()` به صورت In-Place مرتب کند.
10. با استفاده از Slicing یک نسخه برعکس شده ایجاد کند.
11. List اصلی و داده های پردازش شده را به شکل واضح نمایش دهد.

ساختار نمونه:

```python
scores = [18, 12, 15, 9, 20]

scores.append(17)
scores.insert(2, 14)
scores.extend([16, 19])

if 9 in scores:
    scores.remove(9)

removed_score = scores.pop()

score_count = scores.count(15)

if 20 in scores:
    score_position = scores.index(20)
else:
    score_position = None

sorted_scores = sorted(scores)

scores.sort()

reversed_scores = scores[::-1]

print("----- Student Score Manager -----")
print()

print(f"Current scores: {scores}")
print(f"Removed score: {removed_score}")
print(f"Score 15 count: {score_count}")
print(f"Score 20 position: {score_position}")
print(f"Sorted copy: {sorted_scores}")
print(f"Reversed copy: {reversed_scores}")
```

این Challenge چند مفهوم مختلف از درس Lists را با یکدیگر ترکیب می‌ کند:

```text
Lists
Indexing
Negative Indexing
Slicing
List Methods
Variables
Conditional Statements
Membership Testing
String Formatting
```

در بخش بعدی سراغ عملیات پیشرفته‌ تر روی List ها می‌ رویم و بررسی می‌ کنیم که چگونه می‌ توانیم List ها را در کنار سایر مفاهیم پایتون برای پردازش و تبدیل داده ها استفاده کنیم.

---

# بخش ششم — لیست های تو در تو

یک لیست تو در تو، لیستی است که یک یا چند لیست دیگر را به عنوان عناصر خود در بر می گیرد.

لیست های تو در تو زمانی کاربرد دارند که داده ها به صورت چند سطحی و دسته بندی شده باشند.

برای مثال، می توانیم یک لیست از دانش آموزان داشته باشیم که برای هر دانش آموز یک لیست از نمرات او را نگهداری کند:

```python
student_scores = [
    ["Ali", 18, 15, 20],
    ["Sara", 17, 19, 16],
    ["Reza", 12, 14, 10]
]

print(student_scores)
```

خروجی:

```text
[['Ali', 18, 15, 20], ['Sara', 17, 19, 16], ['Reza', 12, 14, 10]]
```

در این مثال، لیست بیرونی شامل سه لیست داخلی است.

---

## ۱. لیست تو در تو چیست؟

یک لیست معمولی می تواند شامل مقادیر ساده باشد:

```python
numbers = [10, 20, 30]
```

اما یک لیست تو در تو می تواند شامل لیست های دیگری باشد:

```python
numbers = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
```

می توانیم این ساختار را به صورت سطر و ستون تصور کنیم:

```text
سطر اول → [1, 2, 3]
سطر دوم → [4, 5, 6]
سطر سوم → [7, 8, 9]
```

هر لیست داخلی، یک عنصر از لیست بیرونی است.

---

## ۲. ساخت لیست های تو در تو

برای ساخت یک لیست تو در تو، لیست های داخلی را داخل یک لیست بیرونی قرار می دهیم.

```python
numbers = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

print(numbers)
```

خروجی:

```text
[[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

یک مثال دیگر:

```python
students = [
    ["Ali", 18],
    ["Sara", 17],
    ["Reza", 15]
]

print(students)
```

خروجی:

```text
[['Ali', 18], ['Sara', 17], ['Reza', 15]]
```

در اینجا هر لیست داخلی شامل نام و نمره یک دانش آموز است.

---

## ۳. دسترسی به عناصر لیست تو در تو

اولین اندیس یک عنصر از لیست بیرونی را انتخاب می کند.

```python
numbers = [
    [10, 20, 30],
    [40, 50, 60],
    [70, 80, 90]
]

print(numbers[0])
```

خروجی:

```text
[10, 20, 30]
```

`numbers[0]` اولین لیست داخلی را بر می گرداند.

به همین شکل:

```python
print(numbers[1])
```

خروجی:

```text
[40, 50, 60]
```

و:

```python
print(numbers[2])
```

خروجی:

```text
[70, 80, 90]
```

---

## ۴. استفاده از چند اندیس

برای دسترسی به یک مقدار مشخص در یک لیست تو در تو، از دو اندیس استفاده می کنیم.

اندیس اول، لیست داخلی را انتخاب می کند.

اندیس دوم، یک عنصر از آن لیست داخلی را انتخاب می کند.

```python
numbers = [
    [10, 20, 30],
    [40, 50, 60],
    [70, 80, 90]
]

print(numbers[0][1])
```

خروجی:

```text
20
```

بیایید این عملیات را مرحله به مرحله بررسی کنیم:

```python
numbers[0]
```

نتیجه:

```text
[10, 20, 30]
```

سپس:

```python
numbers[0][1]
```

اندیس `1` را از لیست داخلی انتخاب می کند:

```text
20
```

یک مثال دیگر:

```python
print(numbers[2][0])
```

خروجی:

```text
70
```

عدد `2` لیست داخلی سوم را انتخاب می کند:

```text
[70, 80, 90]
```

و عدد `0` اولین عنصر آن را انتخاب می کند:

```text
70
```

---

## ۵. استفاده از اندیس های منفی

اندیس های منفی در لیست های تو در تو نیز مانند لیست های معمولی کار می کنند.

```python
numbers = [
    [10, 20, 30],
    [40, 50, 60],
    [70, 80, 90]
]

print(numbers[-1])
```

خروجی:

```text
[70, 80, 90]
```

همچنین می توانیم برای لیست داخلی نیز از اندیس منفی استفاده کنیم:

```python
print(numbers[-1][-1])
```

خروجی:

```text
90
```

اولین `-1` آخرین لیست داخلی را انتخاب می کند.

دومین `-1` آخرین عنصر آن لیست داخلی را انتخاب می کند.

---

## ۶. تغییر عناصر لیست تو در تو

لیست های تو در تو قابل تغییر هستند، بنابراین می توانیم عناصر آن ها را تغییر دهیم.

```python
numbers = [
    [10, 20, 30],
    [40, 50, 60],
    [70, 80, 90]
]

numbers[0][1] = 25

print(numbers)
```

خروجی:

```text
[[10, 25, 30], [40, 50, 60], [70, 80, 90]]
```

مقدار `20` به `25` تغییر کرده است.

یک مثال دیگر:

```python
students = [
    ["Ali", 18],
    ["Sara", 17],
    ["Reza", 15]
]

students[1][1] = 19

print(students)
```

خروجی:

```text
[['Ali', 18], ['Sara', 19], ['Reza', 15]]
```

نمره `"Sara"` از `17` به `19` تغییر کرده است.

---

## ۷. تغییر یک لیست داخلی کامل

می توانیم یک لیست داخلی کامل را نیز با یک لیست جدید جایگزین کنیم.

```python
numbers = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

numbers[1] = [40, 50, 60]

print(numbers)
```

خروجی:

```text
[[1, 2, 3], [40, 50, 60], [7, 8, 9]]
```

لیست داخلی دوم به طور کامل جایگزین شده است.

---

## ۸. لیست های تو در تو و حلقه ها

می توانیم برای پردازش عناصر یک لیست تو در تو از حلقه ها استفاده کنیم.

ابتدا می توانیم با یک حلقه، هر لیست داخلی را دریافت کنیم:

```python
numbers = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for row in numbers:
    print(row)
```

خروجی:

```text
[1, 2, 3]
[4, 5, 6]
[7, 8, 9]
```

متغیر `row` در هر مرحله نماینده یک لیست داخلی است.

---

## ۹. حلقه های تو در تو

اگر بخواهیم به تک تک عناصر دسترسی داشته باشیم، می توانیم از یک حلقه درون یک حلقه دیگر استفاده کنیم.

```python
numbers = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for row in numbers:
    for number in row:
        print(number)
```

خروجی:

```text
1
2
3
4
5
6
7
8
9
```

حلقه بیرونی هر لیست داخلی را پردازش می کند.

حلقه داخلی هر عنصر داخل آن لیست را پردازش می کند.

به این ساختار **حلقه تو در تو** گفته می شود.

---

## ۱۰. چاپ لیست تو در تو به صورت سطر به سطر

لیست های تو در تو معمولاً وقتی سطر به سطر چاپ شوند، خواناتر هستند.

```python
numbers = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for row in numbers:
    print(row)
```

خروجی:

```text
[1, 2, 3]
[4, 5, 6]
[7, 8, 9]
```

می توانیم عناصر را نیز به صورت جداگانه چاپ کنیم:

```python
for row in numbers:
    for number in row:
        print(number, end=" ")

    print()
```

خروجی:

```text
1 2 3
4 5 6
7 8 9
```

`print()` بعد از حلقه داخلی باعث می شود به خط بعد برویم.

---

## ۱۱. مثال کاربردی — نمرات دانش آموزان

فرض کنید چند دانش آموز و نمرات آن ها را داریم:

```python
students = [
    ["Ali", 18, 15, 20],
    ["Sara", 17, 19, 16],
    ["Reza", 12, 14, 10]
]

for student in students:
    print(student)
```

خروجی:

```text
['Ali', 18, 15, 20]
['Sara', 17, 19, 16]
['Reza', 12, 14, 10]
```

می توانیم اطلاعات هر دانش آموز را جداگانه دریافت کنیم:

```python
students = [
    ["Ali", 18, 15, 20],
    ["Sara", 17, 19, 16],
    ["Reza", 12, 14, 10]
]

for student in students:
    name = student[0]

    print(f"Student: {name}")
```

خروجی:

```text
Student: Ali
Student: Sara
Student: Reza
```

---

## ۱۲. محاسبه نمرات

می توانیم لیست های تو در تو را با توابع و حلقه هایی که قبلاً یاد گرفته ایم ترکیب کنیم.

```python
students = [
    ["Ali", 18, 15, 20],
    ["Sara", 17, 19, 16],
    ["Reza", 12, 14, 10]
]

for student in students:
    name = student[0]
    scores = student[1:]

    total = sum(scores)
    average = total / len(scores)

    print(f"{name}: {average}")
```

خروجی:

```text
Ali: 17.666666666666668
Sara: 17.333333333333332
Reza: 12.0
```

در این مثال چند مفهوم قبلی را با هم ترکیب کرده ایم:

- لیست ها
- اندیس گذاری
- برش لیست
- متغیر ها
- حلقه ها
- توابع
- محاسبات
- رشته های قالب بندی شده

---

## ۱۳. لیست های تو در تو و شرط ها

هنگام پردازش لیست های تو در تو می توانیم از شرط ها نیز استفاده کنیم.

```python
students = [
    ["Ali", 18],
    ["Sara", 9],
    ["Reza", 15]
]

for student in students:
    name = student[0]
    score = student[1]

    if score >= 10:
        print(f"{name} → Passing")
    else:
        print(f"{name} → Failing")
```

خروجی:

```text
Ali → Passing
Sara → Failing
Reza → Passing
```

این مثال ترکیبی خوبی از لیست ها، شرط ها و حلقه ها است.

---

## ۱۴. اشتباهات رایج مبتدی ها

### اشتباه اول — فراموش کردن اندیس دوم

فرض کنید:

```python
numbers = [
    [10, 20],
    [30, 40]
]
```

این دستور:

```python
print(numbers[0])
```

خروجی زیر را تولید می کند:

```text
[10, 20]
```

اگر بخواهیم `20` را دریافت کنیم، باید بنویسیم:

```python
print(numbers[0][1])
```

---

### اشتباه دوم — جابه جا کردن اندیس ها

برای:

```python
numbers = [
    [10, 20],
    [30, 40]
]
```

این:

```python
numbers[1][0]
```

یعنی:

1. لیست داخلی دوم را انتخاب کن.
2. اولین عنصر آن را انتخاب کن.

نتیجه:

```text
30
```

---

### اشتباه سوم — استفاده از سطح اشتباه حلقه

اگر فقط هر لیست داخلی را نیاز داریم:

```python
for row in numbers:
    print(row)
```

اگر تک تک عناصر را نیاز داریم:

```python
for row in numbers:
    for number in row:
        print(number)
```

در حالت دوم، حلقه داخلی لازم است چون هر `row` خودش یک لیست است.

---

### اشتباه چهارم — فرض اینکه همه لیست های داخلی اندازه یکسان دارند

برای مثال:

```python
students = [
    ["Ali", 18, 15],
    ["Sara", 17],
    ["Reza", 12, 14, 10]
]
```

لیست های داخلی تعداد عناصر یکسانی ندارند.

بنابراین هنگام دسترسی به اندیس ها باید مراقب باشیم اندیسی که وجود ندارد را درخواست نکنیم.

---

# ۱۵. جمع بندی مهم

یک لیست تو در تو، لیستی است که شامل لیست های دیگری است.

مثال:

```python
numbers = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
```

اندیس اول یک لیست داخلی را انتخاب می کند:

```python
numbers[1]
```

نتیجه:

```text
[4, 5, 6]
```

اندیس دوم یک عنصر از آن لیست داخلی را انتخاب می کند:

```python
numbers[1][2]
```

نتیجه:

```text
6
```

می توانیم عناصر را تغییر دهیم:

```python
numbers[0][1] = 20
```

و برای پردازش تمام عناصر می توانیم از حلقه های تو در تو استفاده کنیم:

```python
for row in numbers:
    for number in row:
        print(number)
```

مهم ترین نکته این بخش:

```text
اندیس اول  → انتخاب لیست داخلی
اندیس دوم  → انتخاب عنصر داخل آن لیست
```

---

# تمرین ها

## تمرین ۱ — ساخت لیست تو در تو

یک لیست تو در تو شامل سه سطر از اعداد ایجاد کنید.

هر سطر باید شامل سه عدد باشد.

لیست تو در تو را چاپ کنید.

---

## تمرین ۲ — دسترسی به عناصر

با استفاده از لیست زیر:

```python
numbers = [
    [10, 20, 30],
    [40, 50, 60],
    [70, 80, 90]
]
```

موارد زیر را چاپ کنید:

1. `10`
2. `50`
3. `90`

---

## تمرین ۳ — تغییر عناصر

با استفاده از همان لیست، موارد زیر را تغییر دهید:

- `20` به `25`
- `60` به `65`
- `80` به `85`

در پایان لیست را چاپ کنید.

---

## تمرین ۴ — چاپ سطر ها

یک لیست تو در تو شامل سه سطر ایجاد کنید.

با استفاده از یک حلقه، هر سطر را به صورت جداگانه چاپ کنید.

---

## تمرین ۵ — چاپ تمام عناصر

یک لیست تو در تو شامل اعداد `1` تا `9` ایجاد کنید.

با استفاده از حلقه های تو در تو، تمام اعداد را به صورت جداگانه چاپ کنید.

---

## تمرین ۶ — نمرات دانش آموزان

یک لیست تو در تو مانند نمونه زیر ایجاد کنید:

```python
students = [
    ["Ali", 18],
    ["Sara", 12],
    ["Reza", 9]
]
```

با استفاده از یک حلقه، نام و نمره هر دانش آموز را چاپ کنید.

---

## تمرین ۷ — قبول و مردود

با استفاده از همان لیست دانش آموزان، از یک شرط استفاده کنید تا خروجی زیر تولید شود:

```text
Ali → Passing
Sara → Passing
Reza → Failing
```

نمره `10` یا بیشتر باید قبول در نظر گرفته شود.

---

## تمرین ۸ — میانگین نمرات

یک لیست تو در تو شامل نام دانش آموزان و سه نمره برای هر دانش آموز ایجاد کنید.

میانگین نمره هر دانش آموز را محاسبه و چاپ کنید.

---

# تمرین جامع

یک **مدیریت کننده نمرات دانش آموزان** با استفاده از لیست تو در تو ایجاد کنید.

برنامه را با داده های زیر شروع کنید:

```python
students = [
    ["Ali", 18, 15, 20],
    ["Sara", 17, 9, 16],
    ["Reza", 12, 14, 10],
    ["Mina", 20, 19, 18]
]
```

برنامه باید:

1. نام تمام دانش آموزان را چاپ کند.
2. نمرات هر دانش آموز را چاپ کند.
3. مجموع نمرات هر دانش آموز را محاسبه کند.
4. میانگین نمرات هر دانش آموز را محاسبه کند.
5. مشخص کند هر دانش آموز قبول یا مردود است.
6. نتایج را به شکل خوانا چاپ کند.
7. از مفاهیم قبلی مانند متغیر ها، لیست ها، اندیس گذاری، برش، حلقه ها، شرط ها، توابع و رشته های قالب بندی شده استفاده کند.

هدف این تمرین درک نحوه استفاده از لیست های تو در تو برای نگهداری یک مجموعه ساده از داده ها است، بدون اینکه وارد ساختارهای داده پیشرفته تر شویم.

---

# چالش نهایی

یک **جدول کلاس** با استفاده از لیست تو در تو ایجاد کنید.

از داده های زیر شروع کنید:

```python
classroom = [
    ["Ali", 18],
    ["Sara", 15],
    ["Reza", 9],
    ["Mina", 20]
]
```

برنامه باید:

1. تمام دانش آموزان را چاپ کند.
2. نمره هر دانش آموز را چاپ کند.
3. مشخص کند هر دانش آموز قبول یا مردود است.
4. مجموع تمام نمرات را محاسبه کند.
5. میانگین نمره کلاس را محاسبه کند.
6. برای تولید گزارش مرتب از حلقه ها و شرط ها استفاده کند.

نمونه خروجی:

```text
----- Classroom Report -----

Ali → 18 → Passing
Sara → 15 → Passing
Reza → 9 → Failing
Mina → 20 → Passing

Total: 62
Average: 15.5
```

هدف اصلی این تمرین، تمرین کردن **لیست های تو در تو در کنار مفاهیم مقدماتی درس های قبلی** است.

---

# بخش هفتم — کپی کردن لیست ها

## ۱. چرا به کپی کردن لیست نیاز داریم؟

گاهی اوقات می خواهیم یک لیست جدید بر اساس یک لیست موجود ایجاد کنیم.

برای مثال:

```python
numbers = [10, 20, 30]

numbers_copy = numbers.copy()

print(numbers)
print(numbers_copy)
```

خروجی:

```text
[10, 20, 30]
[10, 20, 30]
```

در نگاه اول، هر دو لیست کاملاً یکسان به نظر می رسند.

اما یک سؤال مهم وجود دارد:

> آیا این دو واقعاً دو لیست جدا هستند؟

برای پاسخ به این سؤال باید تفاوت بین **انتساب یک لیست** و **کپی کردن یک لیست** را یاد بگیریم.

---

## ۲. انتساب یک لیست به یک متغیر دیگر

مثال زیر را در نظر بگیرید:

```python
numbers = [10, 20, 30]

numbers_copy = numbers

print(numbers_copy)
```

خروجی:

```text
[10, 20, 30]
```

ممکن است به نظر برسد که یک لیست جدید ساخته ایم.

اما این اتفاق نیفتاده است.

هر دو متغیر به یک لیست اشاره می کنند.

این موضوع را با تغییر متغیر دوم می توانیم مشاهده کنیم:

```python
numbers = [10, 20, 30]

numbers_copy = numbers

numbers_copy[0] = 100

print(numbers)
print(numbers_copy)
```

خروجی:

```text
[100, 20, 30]
[100, 20, 30]
```

تغییر `numbers_copy` باعث تغییر `numbers` نیز شده است.

دلیل این اتفاق این است که هر دو متغیر به همان لیست اشاره می کنند.

---

## ۳. تفاوت انتساب و کپی کردن

انتساب:

```python
numbers = [10, 20, 30]

numbers_copy = numbers
```

یک لیست جدید ایجاد نمی کند.

هر دو متغیر به همان لیست اشاره می کنند.

اما در کپی کردن:

```python
numbers = [10, 20, 30]

numbers_copy = numbers.copy()
```

یک لیست جدا ایجاد می شود.

حالا تغییر یک لیست، لیست دیگر را تغییر نمی دهد.

```python
numbers = [10, 20, 30]

numbers_copy = numbers.copy()

numbers_copy[0] = 100

print(numbers)
print(numbers_copy)
```

خروجی:

```text
[10, 20, 30]
[100, 20, 30]
```

لیست اصلی بدون تغییر باقی مانده است.

---

## ۴. کپی کردن لیست با `copy()`

متد `copy()` یکی از ساده ترین روش ها برای ایجاد یک کپی از لیست است.

```python
numbers = [10, 20, 30, 40]

numbers_copy = numbers.copy()

print(numbers_copy)
```

خروجی:

```text
[10, 20, 30, 40]
```

دو لیست مقادیر یکسانی دارند، اما دو لیست جدا هستند.

در سطح مقدماتی، این روش معمولاً واضح ترین روش برای نشان دادن این است که می خواهیم یک لیست را کپی کنیم.

---

## ۵. کپی کردن لیست با برش

می توانیم با استفاده از برش لیست نیز یک کپی ایجاد کنیم.

```python
numbers = [10, 20, 30, 40]

numbers_copy = numbers[:]

print(numbers_copy)
```

خروجی:

```text
[10, 20, 30, 40]
```

برش `[:]` تمام عناصر لیست را انتخاب می کند و یک لیست جدید ایجاد می کند.

برای مثال:

```python
numbers = [10, 20, 30]

numbers_copy = numbers[:]

numbers_copy[1] = 200

print(numbers)
print(numbers_copy)
```

خروجی:

```text
[10, 20, 30]
[10, 200, 30]
```

لیست اصلی تغییر نکرده است.

---

## ۶. کپی کردن لیست با `list()`

روش ساده دیگر برای ایجاد یک کپی، استفاده از تابع `list()` است.

```python
numbers = [10, 20, 30]

numbers_copy = list(numbers)

print(numbers_copy)
```

خروجی:

```text
[10, 20, 30]
```

می توانیم بررسی کنیم که تغییر کپی باعث تغییر لیست اصلی نمی شود:

```python
numbers = [10, 20, 30]

numbers_copy = list(numbers)

numbers_copy.append(40)

print(numbers)
print(numbers_copy)
```

خروجی:

```text
[10, 20, 30]
[10, 20, 30, 40]
```

---

## ۷. مقایسه سه روش ساده کپی کردن

چند روش مقدماتی برای کپی کردن لیست وجود دارد.

### استفاده از `copy()`

```python
numbers_copy = numbers.copy()
```

### استفاده از برش

```python
numbers_copy = numbers[:]
```

### استفاده از `list()`

```python
numbers_copy = list(numbers)
```

هر سه روش برای یک لیست معمولی از مقادیر ساده، یک لیست جدا ایجاد می کنند.

برای خوانایی، `copy()` معمولاً انتخاب ساده تری است، زیرا هدف کد را به شکل واضح نشان می دهد:

```python
numbers_copy = numbers.copy()
```

---

## ۸. تغییر لیست اصلی و لیست کپی شده

وقتی یک کپی واقعی داشته باشیم، می توانیم هر یک از دو لیست را به صورت مستقل تغییر دهیم.

```python
numbers = [10, 20, 30]

numbers_copy = numbers.copy()

numbers[0] = 100

print(numbers)
print(numbers_copy)
```

خروجی:

```text
[100, 20, 30]
[10, 20, 30]
```

تغییر لیست اصلی باعث تغییر کپی نشده است.

می توانیم کپی را نیز تغییر دهیم:

```python
numbers = [10, 20, 30]

numbers_copy = numbers.copy()

numbers_copy[2] = 300

print(numbers)
print(numbers_copy)
```

خروجی:

```text
[10, 20, 30]
[10, 20, 300]
```

دو لیست مستقل از یکدیگر هستند.

---

## ۹. یک مثال کاربردی

فرض کنید یک لیست از نمرات دانش آموزان داریم.

```python
scores = [18, 15, 20, 12, 17]

original_scores = scores.copy()

scores[0] = 10

print(f"Original scores: {original_scores}")
print(f"Updated scores: {scores}")
```

خروجی:

```text
Original scores: [18, 15, 20, 12, 17]
Updated scores: [10, 15, 20, 12, 17]
```

لیست کپی شده، مقادیر اصلی را حفظ کرده است.

این کار زمانی مفید است که بخواهیم داده اصلی را نگه داریم و روی یک نسخه تغییر یافته کار کنیم.

---

## ۱۰. کپی کردن قبل از ایجاد تغییر

یک الگوی کاربردی می تواند به این شکل باشد:

```python
scores = [18, 15, 20, 12, 17]

updated_scores = scores.copy()

updated_scores.append(19)

print(f"Original: {scores}")
print(f"Updated: {updated_scores}")
```

خروجی:

```text
Original: [18, 15, 20, 12, 17]
Updated: [18, 15, 20, 12, 17, 19]
```

به این شکل می توانیم لیست اصلی را بدون تغییر نگه داریم.

---

## ۱۱. اشتباهات رایج مبتدی ها

### اشتباه اول — تصور اینکه انتساب باعث ایجاد کپی می شود

این کار یک لیست جدا ایجاد نمی کند:

```python
numbers = [1, 2, 3]

numbers_copy = numbers
```

اگر یکی را تغییر دهیم:

```python
numbers_copy[0] = 100
```

لیست دیگر نیز تغییر می کند.

---

### اشتباه دوم — کپی نکردن قبل از تغییر

فرض کنید می خواهیم لیست اصلی را حفظ کنیم.

این کار کافی نیست:

```python
numbers = [1, 2, 3]

new_numbers = numbers

new_numbers.append(4)
```

حالا هر دو متغیر به این لیست اشاره می کنند:

```text
[1, 2, 3, 4]
```

به جای آن باید یک کپی ایجاد کنیم:

```python
numbers = [1, 2, 3]

new_numbers = numbers.copy()

new_numbers.append(4)
```

حالا:

```text
numbers     → [1, 2, 3]
new_numbers → [1, 2, 3, 4]
```

---

### اشتباه سوم — اشتباه گرفتن مقادیر برابر با یک لیست یکسان

دو لیست می توانند مقادیر یکسانی داشته باشند، اما همچنان دو لیست جدا باشند.

```python
numbers = [1, 2, 3]

numbers_copy = numbers.copy()
```

هر دو شامل این مقادیر هستند:

```text
[1, 2, 3]
```

اما تغییر یکی باعث تغییر دیگری نمی شود.

---

# ۱۲. جمع بندی مهم

وقتی می نویسیم:

```python
numbers_copy = numbers
```

یک لیست جدید ایجاد نمی کنیم.

هر دو متغیر به همان لیست اشاره می کنند.

وقتی می نویسیم:

```python
numbers_copy = numbers.copy()
```

یک لیست جدا ایجاد می کنیم.

روش های مقدماتی دیگر برای کپی کردن لیست عبارتند از:

```python
numbers_copy = numbers[:]
```

و:

```python
numbers_copy = list(numbers)
```

مهم ترین تفاوت:

```text
انتساب → همان لیست
کپی کردن → لیست جدا
```

---

# تمرین ها

## تمرین ۱ — انتساب یا کپی؟

قبل از اجرای کد زیر، خروجی آن را حدس بزنید:

```python
numbers = [10, 20, 30]

numbers_copy = numbers

numbers_copy[0] = 100

print(numbers)
print(numbers_copy)
```

توضیح دهید چرا هر دو خروجی یکسان هستند.

---

## تمرین ۲ — استفاده از `copy()`

یک لیست شامل پنج عدد ایجاد کنید.

با استفاده از `copy()` یک کپی از آن ایجاد کنید.

یکی از عناصر لیست کپی شده را تغییر دهید.

هر دو لیست را چاپ کنید و بررسی کنید که لیست اصلی تغییر نکرده باشد.

---

## تمرین ۳ — استفاده از برش

یک لیست از نام ها ایجاد کنید.

با استفاده از دستور زیر یک کپی ایجاد کنید:

```python
names_copy = names[:]
```

یک نام جدید به لیست کپی شده اضافه کنید.

هر دو لیست را چاپ کنید.

---

## تمرین ۴ — استفاده از `list()`

یک لیست از اعداد ایجاد کنید.

با استفاده از دستور زیر یک کپی ایجاد کنید:

```python
numbers_copy = list(numbers)
```

یکی از عناصر لیست کپی شده را حذف کنید.

هر دو لیست را چاپ کنید.

---

## تمرین ۵ — نمرات اصلی و به روز شده

یک لیست از نمرات دانش آموزان ایجاد کنید.

یک کپی با نام `updated_scores` بسازید.

چند نمره را در `updated_scores` تغییر دهید.

چاپ کنید:

```text
Original scores:
Updated scores:
```

بررسی کنید که لیست اصلی بدون تغییر باقی مانده باشد.

---

## تمرین ۶ — سه لیست کپی شده

لیست اصلی زیر را ایجاد کنید:

```python
numbers = [1, 2, 3, 4, 5]
```

سه کپی جداگانه با استفاده از موارد زیر ایجاد کنید:

1. `copy()`
2. برش
3. `list()`

در هر کپی یک عنصر را تغییر دهید.

هر چهار لیست را چاپ کنید.

---

# تمرین جامع

یک **سیستم به روز رسانی نمرات** ایجاد کنید.

برنامه را با این لیست شروع کنید:

```python
scores = [18, 15, 20, 12, 17]
```

برنامه باید:

1. نمرات اصلی را حفظ کند.
2. یک کپی با نام `updated_scores` ایجاد کند.
3. حداقل دو نمره را در `updated_scores` تغییر دهد.
4. یک نمره جدید اضافه کند.
5. نمرات اصلی را چاپ کند.
6. نمرات به روز شده را چاپ کند.
7. اطمینان حاصل کند که تغییر `updated_scores` باعث تغییر `scores` نشود.

نمونه خروجی:

```text
----- Score Update System -----

Original scores:
[18, 15, 20, 12, 17]

Updated scores:
[18, 19, 20, 14, 17, 16]
```

هدف اصلی این تمرین درک تفاوت بین **اشاره کردن به یک لیست یکسان** و **ایجاد یک کپی جدا از لیست** است.

---

# بخش ۸ — پیمایش لیست ها

## ۱. مقدمه ای بر پیمایش لیست ها

یکی از رایج ترین کارهایی که با یک لیست انجام می دهیم، عبور از عناصر آن به صورت یکی یکی است.

به این فرایند **Iteration** یا پیمایش گفته می شود.

برای مثال:

    fruits = ["Apple", "Banana", "Orange"]

می توانیم با استفاده از حلقه `for` هر عنصر را بررسی کنیم:

    fruits = ["Apple", "Banana", "Orange"]

    for fruit in fruits:
        print(fruit)

خروجی:

    Apple
    Banana
    Orange

متغیر `fruit` در هر بار اجرای حلقه، عنصر فعلی لیست را نشان می دهد.

---

## ۲. پیمایش ساده یک لیست

ساده ترین روش برای پیمایش یک لیست، استفاده از حلقه `for` است.

    numbers = [10, 20, 30, 40, 50]

    for number in numbers:
        print(number)

خروجی:

    10
    20
    30
    40
    50

پایتون به صورت خودکار از یک عنصر به عنصر بعدی حرکت می کند.

---

## ۳. پیمایش لیست شامل رشته ها

یک لیست می تواند شامل رشته ها باشد و می توانیم هر رشته را به صورت جداگانه پردازش کنیم.

    names = ["Ali", "Sara", "Reza", "Mina"]

    for name in names:
        print(f"Hello, {name}!")

خروجی:

    Hello, Ali!
    Hello, Sara!
    Hello, Reza!
    Hello, Mina!

این روش زمانی کاربرد دارد که بخواهیم یک عملیات مشابه را روی تمام عناصر انجام دهیم.

---

## ۴. انجام محاسبات هنگام پیمایش

می توانیم برای هر عنصر یک محاسبه انجام دهیم.

    numbers = [2, 4, 6, 8]

    for number in numbers:
        square = number ** 2
        print(f"{number} squared = {square}")

خروجی:

    2 squared = 4
    4 squared = 16
    6 squared = 36
    8 squared = 64

هر عنصر به صورت جداگانه پردازش می شود.

---

## ۵. استفاده از شرط هنگام پیمایش

می توانیم حلقه `for` را با دستور `if` ترکیب کنیم.

    scores = [18, 8, 15, 7, 20]

    for score in scores:
        if score >= 10:
            print(f"{score} → Passing")
        else:
            print(f"{score} → Failing")

خروجی:

    18 → Passing
    8 → Failing
    15 → Passing
    7 → Failing
    20 → Passing

این یکی از کاربردی ترین الگوها هنگام کار با لیست هاست.

---

## ۶. پیدا کردن عناصر خاص

می توانیم با استفاده از پیمایش، عناصری را پیدا کنیم که یک شرط مشخص را دارند.

    numbers = [5, 12, 8, 20, 3, 15]

    for number in numbers:
        if number > 10:
            print(number)

خروجی:

    12
    20
    15

فقط اعدادی که بزرگ تر از `10` هستند چاپ می شوند.

---

## ۷. شمارش عناصر هنگام پیمایش

می توانیم یک متغیر شمارنده ایجاد کنیم و هنگام پیمایش آن را افزایش دهیم.

    numbers = [5, 12, 8, 20, 3, 15]

    count = 0

    for number in numbers:
        if number > 10:
            count += 1

    print(f"Numbers greater than 10: {count}")

خروجی:

    Numbers greater than 10: 3

این الگو زمانی مفید است که بخواهیم تعداد عناصری را که یک شرط مشخص دارند محاسبه کنیم.

---

## ۸. محاسبه مجموع هنگام پیمایش

می توانیم از یک متغیر برای نگهداری مجموع استفاده کنیم.

    numbers = [10, 20, 30, 40]

    total = 0

    for number in numbers:
        total += number

    print(f"Total: {total}")

خروجی:

    Total: 100

مقدار `total` در هر بار اجرای حلقه تغییر می کند.

---

## ۹. پیدا کردن بزرگ ترین مقدار

می توانیم با استفاده از یک حلقه بزرگ ترین مقدار موجود در لیست را پیدا کنیم.

    numbers = [12, 45, 7, 32, 18]

    largest = numbers[0]

    for number in numbers:
        if number > largest:
            largest = number

    print(f"Largest number: {largest}")

خروجی:

    Largest number: 45

متغیر `largest` بزرگ ترین مقداری را که تا آن لحظه پیدا شده نگه می دارد.

---

## ۱۰. پیدا کردن کوچک ترین مقدار

همین ایده را می توانیم برای پیدا کردن کوچک ترین مقدار استفاده کنیم.

    numbers = [12, 45, 7, 32, 18]

    smallest = numbers[0]

    for number in numbers:
        if number < smallest:
            smallest = number

    print(f"Smallest number: {smallest}")

خروجی:

    Smallest number: 7

ابتدا عنصر اول را به عنوان کوچک ترین مقدار در نظر می گیریم و سپس سایر عناصر را با آن مقایسه می کنیم.

---

## ۱۱. ساخت یک لیست جدید هنگام پیمایش

می توانیم یک لیست جدید بسازیم و عناصر مورد نظر را داخل آن قرار دهیم.

برای مثال، می توانیم لیستی شامل نمرات قبولی بسازیم.

    scores = [18, 8, 15, 7, 20]

    passing_scores = []

    for score in scores:
        if score >= 10:
            passing_scores.append(score)

    print(f"Passing scores: {passing_scores}")

خروجی:

    Passing scores: [18, 15, 20]

این یک الگوی مهم در سطح مقدماتی است:

1. یک لیست خالی ایجاد می کنیم.
2. لیست اصلی را پیمایش می کنیم.
3. یک شرط را بررسی می کنیم.
4. عناصر مناسب را به لیست جدید اضافه می کنیم.

---

## ۱۲. پیمایش یک لیست و ساخت یک لیست دیگر

می توانیم یک لیست را به عنوان منبع و یک لیست دیگر را به عنوان نتیجه استفاده کنیم.

    numbers = [1, 2, 3, 4, 5]

    doubled_numbers = []

    for number in numbers:
        doubled = number * 2
        doubled_numbers.append(doubled)

    print(f"Original: {numbers}")
    print(f"Doubled: {doubled_numbers}")

خروجی:

    Original: [1, 2, 3, 4, 5]
    Doubled: [2, 4, 6, 8, 10]

لیست اصلی بدون تغییر باقی می ماند.

---

## ۱۳. استفاده از `range()` همراه با لیست

گاهی اوقات می خواهیم با اندیس های یک لیست کار کنیم.

می توانیم از `range()` و `len()` استفاده کنیم.

    fruits = ["Apple", "Banana", "Orange"]

    for index in range(len(fruits)):
        print(f"Index: {index} → {fruits[index]}")

خروجی:

    Index: 0 → Apple
    Index: 1 → Banana
    Index: 2 → Orange

در اینجا:

    len(fruits)

تعداد عناصر لیست را مشخص می کند.

و:

    range(len(fruits))

اندیس های مورد نیاز را ایجاد می کند.

در سطح مقدماتی، زمانی که به اندیس نیاز نداریم، پیمایش مستقیم معمولا ساده تر است.

---

## ۱۴. پیمایش مستقیم در مقابل پیمایش بر اساس اندیس

### پیمایش مستقیم

زمانی از این روش استفاده می کنیم که فقط به مقدار عناصر نیاز داریم.

    fruits = ["Apple", "Banana", "Orange"]

    for fruit in fruits:
        print(fruit)

### پیمایش بر اساس اندیس

زمانی از این روش استفاده می کنیم که به اندیس نیز نیاز داریم.

    fruits = ["Apple", "Banana", "Orange"]

    for index in range(len(fruits)):
        print(f"{index}: {fruits[index]}")

روش اول زمانی که به اندیس نیاز نداریم، ساده تر و خواناتر است.

---

## ۱۵. استفاده از `break` هنگام پیمایش

دستور `break` حلقه را به طور کامل متوقف می کند.

برای مثال، می توانیم وقتی یک عدد مشخص را پیدا کردیم، حلقه را متوقف کنیم.

    numbers = [10, 20, 30, 40, 50]

    for number in numbers:
        if number == 30:
            print("Number found!")
            break

        print(number)

خروجی:

    10
    20
    Number found!

وقتی پایتون به `break` می رسد، حلقه متوقف می شود.

---

## ۱۶. استفاده از `continue` هنگام پیمایش

دستور `continue` اجرای فعلی حلقه را رد می کند و به تکرار بعدی می رود.

برای مثال، می توانیم نمرات مردودی را نادیده بگیریم.

    scores = [18, 8, 15, 7, 20]

    for score in scores:
        if score < 10:
            continue

        print(f"Passing score: {score}")

خروجی:

    Passing score: 18
    Passing score: 15
    Passing score: 20

وقتی `score < 10` درست باشد، `continue` باعث می شود ادامه کد در آن تکرار اجرا نشود.

---

## ۱۷. مثال کاربردی — نمرات دانش آموزان

می توانیم پیمایش لیست، شرط، شمارنده و محاسبات را با هم ترکیب کنیم.

    scores = [18, 8, 15, 7, 20]

    print("----- Student Scores -----")
    print()

    print(f"Scores: {scores}")

    number_of_scores = len(scores)
    total = 0
    passing_count = 0

    for score in scores:
        total += score

        if score >= 10:
            passing_count += 1
            print(f"{score} → Passing")
        else:
            print(f"{score} → Failing")

    average = total / number_of_scores

    print()
    print(f"Number of scores: {number_of_scores}")
    print(f"Total: {total}")
    print(f"Average: {average}")
    print(f"Passing students: {passing_count}")

خروجی:

    ----- Student Scores -----

    Scores: [18, 8, 15, 7, 20]
    18 → Passing
    8 → Failing
    15 → Passing
    7 → Failing
    20 → Passing

    Number of scores: 5
    Total: 68
    Average: 13.6
    Passing students: 3

---

## ۱۸. مثال کاربردی — پیدا کردن یک محصول

می توانیم در یک لیست از محصولات جستجو کنیم.

    products = ["Laptop", "Mouse", "Keyboard", "Monitor"]

    search_item = "Keyboard"

    found = False

    for product in products:
        if product == search_item:
            found = True
            break

    if found:
        print(f"{search_item} was found.")
    else:
        print(f"{search_item} was not found.")

خروجی:

    Keyboard was found.

در این مثال مفاهیم زیر را با هم استفاده کرده ایم:

- لیست
- حلقه `for`
- دستور `if`
- متغیر Boolean
- دستور `break`

---

## ۱۹. اشتباهات رایج مبتدی ها

### اشتباه اول — فراموش کردن تورفتگی

درست:

    numbers = [1, 2, 3]

    for number in numbers:
        print(number)

دستور `print()` بخشی از حلقه است، چون داخل آن تورفتگی دارد.

### اشتباه دوم — تغییر دادن لیست هنگام پیمایش

بهتر است هنگام پیمایش مستقیم یک لیست، همان لیست را تغییر ندهیم.

برای مثال:

    numbers = [1, 2, 3, 4, 5]

    for number in numbers:
        if number % 2 == 0:
            numbers.remove(number)

در سطح مقدماتی بهتر است یک لیست جدید بسازیم:

    numbers = [1, 2, 3, 4, 5]

    odd_numbers = []

    for number in numbers:
        if number % 2 != 0:
            odd_numbers.append(number)

    print(odd_numbers)

خروجی:

    [1, 3, 5]

### اشتباه سوم — استفاده غیرضروری از اندیس

اگر فقط به مقدار عناصر نیاز داریم، این روش ساده تر است:

    fruits = ["Apple", "Banana", "Orange"]

    for fruit in fruits:
        print(fruit)

معمولا نیازی نیست بنویسیم:

    for index in range(len(fruits)):
        print(fruits[index])

زمانی از روش مبتنی بر اندیس استفاده کنید که واقعا به اندیس نیاز دارید.

---

## ۲۰. جمع بندی مهم

پیمایش لیست یعنی بررسی عناصر یک لیست به صورت یکی یکی.

رایج ترین الگو:

    for item in my_list:
        print(item)

می توانیم پیمایش را با شرط ترکیب کنیم:

    for item in my_list:
        if condition:
            print(item)

می توانیم عناصر مطابق شرط را بشماریم:

    count = 0

    for item in my_list:
        if condition:
            count += 1

می توانیم مجموع را محاسبه کنیم:

    total = 0

    for number in numbers:
        total += number

می توانیم یک لیست جدید بسازیم:

    result = []

    for item in my_list:
        if condition:
            result.append(item)

برای توقف کامل حلقه از:

    break

و برای رد کردن یک تکرار از:

    continue

استفاده می کنیم.

---

# تمرین ها

## تمرین ۱ — چاپ تمام عناصر

یک لیست شامل پنج غذای مورد علاقه خود ایجاد کنید.

با استفاده از حلقه `for` هر غذا را چاپ کنید.

## تمرین ۲ — چاپ اعداد

یک لیست شامل چند عدد ایجاد کنید.

با استفاده از یک حلقه هر عدد را چاپ کنید.

## تمرین ۳ — چاپ اعداد زوج

یک لیست از اعداد ایجاد کنید.

با استفاده از پیمایش و دستور `if` فقط اعداد زوج را چاپ کنید.

## تمرین ۴ — شمارش نمرات قبولی

یک لیست از نمرات دانش آموزان ایجاد کنید.

با استفاده از حلقه تعداد نمراتی را که بزرگ تر یا مساوی `10` هستند بشمارید.

## تمرین ۵ — محاسبه مجموع

یک لیست از اعداد ایجاد کنید.

با استفاده از پیمایش مجموع اعداد را بدون استفاده از `sum()` محاسبه کنید.

## تمرین ۶ — پیدا کردن بزرگ ترین عدد

یک لیست از اعداد ایجاد کنید.

با استفاده از حلقه بزرگ ترین عدد را بدون استفاده از `max()` پیدا کنید.

## تمرین ۷ — پیدا کردن کوچک ترین عدد

یک لیست از اعداد ایجاد کنید.

با استفاده از حلقه کوچک ترین عدد را بدون استفاده از `min()` پیدا کنید.

## تمرین ۸ — ساخت یک لیست جدید

یک لیست از اعداد ایجاد کنید.

یک لیست دوم بسازید که فقط شامل اعداد بزرگ تر از `10` باشد.

## تمرین ۹ — دو برابر کردن اعداد

یک لیست از اعداد ایجاد کنید.

یک لیست جدید بسازید که هر عدد آن دو برابر عدد متناظر در لیست اصلی باشد.

## تمرین ۱۰ — جستجو در لیست

یک لیست از نام ها ایجاد کنید.

از کاربر یک نام دریافت کنید.

در لیست جستجو کنید و مشخص کنید که آیا آن نام وجود دارد یا خیر.

---

# چالش جامع

یک **تحلیل گر نمرات دانش آموزان** ایجاد کنید.

با این داده شروع کنید:

    scores = [18, 8, 15, 7, 20, 12, 9]

برنامه باید:

1. تمام نمرات را چاپ کند.
2. تعداد نمرات را چاپ کند.
3. مجموع نمرات را بدون استفاده از `sum()` محاسبه کند.
4. میانگین را محاسبه کند.
5. تعداد نمرات قبولی را محاسبه کند.
6. تعداد نمرات مردودی را محاسبه کند.
7. بالاترین نمره را بدون استفاده از `max()` پیدا کند.
8. پایین ترین نمره را بدون استفاده از `min()` پیدا کند.
9. مشخص کند که هر نمره قبولی است یا مردودی.

نمونه خروجی:

    ----- Student Score Analyzer -----

    Scores: [18, 8, 15, 7, 20, 12, 9]

    18 → Passing
    8 → Failing
    15 → Passing
    7 → Failing
    20 → Passing
    12 → Passing
    9 → Failing

    Number of scores: 7
    Total: 89
    Average: 12.71
    Passing scores: 4
    Failing scores: 3
    Highest score: 20
    Lowest score: 7

هدف این چالش، تمرین پیمایش لیست در کنار حلقه `for`، شرط ها، متغیرها، شمارنده ها و محاسبات پایه ای است که در بخش های قبلی یاد گرفته ایم.

---

# بخش ۹ — بررسی وجود یک عنصر در لیست

## ۱. مقدمه

گاهی لازم است بررسی کنیم که آیا یک مقدار مشخص در یک لیست وجود دارد یا نه.

برای مثال:

    fruits = ["Apple", "Banana", "Orange", "Mango"]

ممکن است بخواهیم بدانیم آیا `"Banana"` در لیست وجود دارد یا خیر.

پایتون برای این کار عملگر `in` را در اختیار ما قرار می دهد.

    fruits = ["Apple", "Banana", "Orange", "Mango"]

    print("Banana" in fruits)

خروجی:

    True

نتیجه یک مقدار Boolean است:

    True

یا:

    False

---

## ۲. استفاده از `in`

عملگر `in` بررسی می کند که آیا یک مقدار در لیست وجود دارد یا خیر.

    numbers = [10, 20, 30, 40, 50]

    print(30 in numbers)
    print(100 in numbers)

خروجی:

    True
    False

بررسی اول درست است، چون `30` در لیست وجود دارد.

بررسی دوم نادرست است، چون `100` در لیست وجود ندارد.

---

## ۳. استفاده از `not in`

می توانیم بررسی کنیم که یک مقدار در لیست وجود ندارد.

برای این کار از `not in` استفاده می کنیم.

    fruits = ["Apple", "Banana", "Orange"]

    print("Apple" not in fruits)
    print("Mango" not in fruits)

خروجی:

    False
    True

`"Apple"` در لیست وجود دارد، بنابراین `"Apple" not in fruits` برابر `False` است.

`"Mango"` در لیست وجود ندارد، بنابراین `"Mango" not in fruits` برابر `True` است.

---

## ۴. استفاده از `in` با `if`

عملگر `in` معمولا همراه با `if` استفاده می شود.

    fruits = ["Apple", "Banana", "Orange"]

    if "Banana" in fruits:
        print("Banana is available.")

خروجی:

    Banana is available.

به این شکل برنامه می تواند بر اساس وجود یا عدم وجود یک عنصر تصمیم گیری کند.

---

## ۵. استفاده از `else`

می توانیم حالت وجود نداشتن عنصر را نیز مدیریت کنیم.

    fruits = ["Apple", "Banana", "Orange"]

    if "Mango" in fruits:
        print("Mango is available.")
    else:
        print("Mango is not available.")

خروجی:

    Mango is not available.

---

## ۶. بررسی ورودی کاربر

می توانیم از `in` برای بررسی مقداری که کاربر وارد کرده است استفاده کنیم.

    fruits = ["Apple", "Banana", "Orange"]

    favorite = input("Enter a fruit: ")

    if favorite in fruits:
        print("This fruit is in the list.")
    else:
        print("This fruit is not in the list.")

اگر کاربر وارد کند:

    Banana

خروجی خواهد بود:

    This fruit is in the list.

---

## ۷. بررسی اعداد

همین روش برای اعداد نیز کاربرد دارد.

    numbers = [10, 20, 30, 40, 50]

    number = int(input("Enter a number: "))

    if number in numbers:
        print("Number found.")
    else:
        print("Number not found.")

اگر کاربر وارد کند:

    30

خروجی:

    Number found.

---

## ۸. بررسی چند مقدار مجاز

می توانیم زمانی که چند مقدار قابل قبول داریم از `in` استفاده کنیم.

برای مثال:

    allowed_colors = ["red", "green", "blue"]

    color = input("Enter a color: ")

    if color in allowed_colors:
        print("This color is allowed.")
    else:
        print("This color is not allowed.")

این روش نسبت به نوشتن چند مقایسه جداگانه ساده تر و خواناتر است.

---

## ۹. بررسی چند مقدار غیر مجاز با `not in`

می توانیم زمانی که می خواهیم بعضی مقادیر را رد کنیم از `not in` استفاده کنیم.

    blocked_users = ["admin", "root", "guest"]

    username = input("Enter a username: ")

    if username not in blocked_users:
        print("Username is available.")
    else:
        print("This username is blocked.")

---

## ۱۰. حساس بودن حروف به بزرگی و کوچکی

مقایسه رشته ها به بزرگی و کوچکی حروف حساس است.

برای مثال:

    fruits = ["Apple", "Banana", "Orange"]

    print("Apple" in fruits)
    print("apple" in fruits)

خروجی:

    True
    False

`"Apple"` و `"apple"` دو رشته متفاوت هستند.

اگر بخواهیم حروف بزرگ و کوچک تفاوتی نداشته باشند، می توانیم ابتدا ورودی را تبدیل کنیم.

    fruits = ["apple", "banana", "orange"]

    fruit = input("Enter a fruit: ").lower()

    if fruit in fruits:
        print("Fruit found.")
    else:
        print("Fruit not found.")

حالا اگر کاربر وارد کند:

    APPLE

این ورودی نیز کار خواهد کرد، چون `.lower()` آن را به:

    apple

تبدیل می کند.

---

## ۱۱. بررسی قبل از اضافه کردن یک عنصر

می توانیم از `in` استفاده کنیم تا از ایجاد عناصر تکراری جلوگیری کنیم.

    fruits = ["Apple", "Banana", "Orange"]

    new_fruit = "Banana"

    if new_fruit not in fruits:
        fruits.append(new_fruit)

    print(fruits)

خروجی:

    ['Apple', 'Banana', 'Orange']

چون `"Banana"` از قبل وجود دارد، دوباره به لیست اضافه نمی شود.

اگر از:

    new_fruit = "Mango"

استفاده کنیم، نتیجه می شود:

    ['Apple', 'Banana', 'Orange', 'Mango']

---

## ۱۲. بررسی قبل از حذف یک عنصر

می توانیم قبل از استفاده از `remove()` بررسی کنیم که عنصر مورد نظر وجود دارد یا نه.

    fruits = ["Apple", "Banana", "Orange"]

    fruit = "Banana"

    if fruit in fruits:
        fruits.remove(fruit)

    print(fruits)

خروجی:

    ['Apple', 'Orange']

این روش از خطایی که ممکن است هنگام حذف مقداری که در لیست وجود ندارد ایجاد شود جلوگیری می کند.

---

## ۱۳. بررسی یک لیست از نام ها

یک مثال ساده و کاربردی:

    students = ["Ali", "Sara", "Reza", "Mina"]

    name = input("Enter a student name: ")

    if name in students:
        print(f"{name} is a student.")
    else:
        print(f"{name} is not in the student list.")

---

## ۱۴. ترکیب `in` با شرط های دیگر

می توانیم بررسی وجود یک عنصر را با شرط های دیگر ترکیب کنیم.

    scores = [18, 15, 20, 12, 9]

    score = 20

    if score in scores and score >= 10:
        print("This is a passing score and it exists in the list.")

خروجی:

    This is a passing score and it exists in the list.

به این شکل می توانیم چند شرط را هم زمان بررسی کنیم.

---

## ۱۵. تفاوت `in` و `index()`

عملگر `in` به یک سوال ساده پاسخ می دهد:

    آیا این مقدار در لیست وجود دارد؟

برای مثال:

    fruits = ["Apple", "Banana", "Orange"]

    print("Banana" in fruits)

خروجی:

    True

اما متد `index()` به سوال دیگری پاسخ می دهد:

    این مقدار در چه موقعیتی قرار دارد؟

برای مثال:

    fruits = ["Apple", "Banana", "Orange"]

    print(fruits.index("Banana"))

خروجی:

    1

در سطح مقدماتی، اگر فقط می خواهیم بدانیم یک عنصر وجود دارد یا نه، از `in` استفاده می کنیم.

اگر به موقعیت عنصر نیاز داشته باشیم، از `index()` استفاده می کنیم.

---

## ۱۶. مثال کاربردی — لیست خرید

می توانیم بررسی کنیم که آیا یک کالا از قبل در لیست خرید وجود دارد یا نه.

    shopping_list = ["Milk", "Bread", "Eggs"]

    item = input("Enter an item: ")

    if item in shopping_list:
        print(f"{item} is already in the shopping list.")
    else:
        shopping_list.append(item)
        print(f"{item} was added to the shopping list.")

    print(f"Shopping list: {shopping_list}")

این الگوی ساده برای جلوگیری از اضافه شدن کالاهای تکراری کاربرد دارد.

---

## ۱۷. مثال کاربردی — درس های مجاز

می توانیم از یک لیست برای نگهداری درس های مجاز استفاده کنیم.

    subjects = ["Python", "Math", "English", "Science"]

    subject = input("Enter a subject: ")

    if subject in subjects:
        print("This subject is available.")
    else:
        print("This subject is not available.")

---

## ۱۸. مثال کاربردی — بررسی ساده نام کاربری

می توانیم از یک لیست برای نگهداری نام های کاربری مجاز استفاده کنیم.

    usernames = ["ali", "sara", "reza"]

    username = input("Enter your username: ")

    if username in usernames:
        print("Welcome!")
    else:
        print("Username not found.")

این فقط یک مثال ساده برای بررسی وجود یک مقدار در لیست است و یک سیستم احراز هویت واقعی نیست.

---

## ۱۹. اشتباهات رایج مبتدی ها

### اشتباه اول — فراموش کردن حساس بودن حروف

این عبارت:

    "Ali" in ["Ali", "Sara"]

برابر `True` است.

اما این عبارت:

    "ali" in ["Ali", "Sara"]

برابر `False` است.

### اشتباه دوم — حذف کردن بدون بررسی

این کد می تواند باعث خطا شود:

    fruits = ["Apple", "Banana"]

    fruits.remove("Mango")

روش امن تر در سطح مقدماتی:

    fruits = ["Apple", "Banana"]

    if "Mango" in fruits:
        fruits.remove("Mango")

### اشتباه سوم — استفاده از `index()` وقتی فقط به `in` نیاز داریم

اگر فقط می خواهیم بدانیم یک عنصر وجود دارد یا نه، این روش ساده تر است:

    if "Banana" in fruits:
        print("Found.")

نیازی نیست ابتدا موقعیت عنصر را پیدا کنیم.

---

## ۲۰. جمع بندی مهم

عملگر `in` بررسی می کند که آیا یک عنصر در لیست وجود دارد یا خیر:

    "Apple" in fruits

نتیجه یکی از این دو مقدار است:

    True

یا:

    False

عملگر `not in` بررسی می کند که یک عنصر در لیست وجود ندارد:

    "Mango" not in fruits

می توانیم بررسی وجود عنصر را با `if` ترکیب کنیم:

    if item in my_list:
        print("Found.")

می توانیم از ایجاد عناصر تکراری جلوگیری کنیم:

    if item not in my_list:
        my_list.append(item)

می توانیم قبل از حذف یک عنصر وجود آن را بررسی کنیم:

    if item in my_list:
        my_list.remove(item)

به یاد داشته باشید که مقایسه رشته ها به بزرگی و کوچکی حروف حساس است.

در سطح مقدماتی، `in` و `not in` ابزارهای ساده و کاربردی برای کار با لیست ها هستند.

---

# بخش ۱۰ — طول لیست ها و شمارش عناصر

## ۱. مقدمه

گاهی لازم است بدانیم یک لیست چند عنصر دارد.

برای این کار از تابع `len()` استفاده می کنیم.

برای مثال:

```python
fruits = ["Apple", "Banana", "Orange"]

print(len(fruits))
```

خروجی:

```text
3
```

تابع `len()` تعداد عناصر موجود در لیست را برمی گرداند.

## ۲. استفاده از `len()`

ساختار اصلی:

```python
len(list_name)
```

برای مثال:

```python
numbers = [10, 20, 30, 40, 50]

print(len(numbers))
```

خروجی:

```text
5
```

## ۳. استفاده از `count()`

متد `count()` مشخص می کند یک مقدار مشخص چند بار در لیست وجود دارد.

```python
fruits = ["Apple", "Banana", "Apple", "Orange", "Apple"]

print(fruits.count("Apple"))
```

خروجی:

```text
3
```

## ۴. تفاوت `len()` و `count()`

`len()` تعداد تمام عناصر را می شمارد:

```python
fruits = ["Apple", "Banana", "Apple", "Orange"]

print(len(fruits))
```

خروجی:

```text
4
```

اما `count()` تعداد تکرار یک مقدار مشخص را می شمارد:

```python
print(fruits.count("Apple"))
```

خروجی:

```text
2
```

بنابراین:

```python
len(fruits)
```

یعنی:

تعداد عناصر موجود در لیست چقدر است؟

و:

```python
fruits.count("Apple")
```

یعنی:

`"Apple"` چند بار در لیست وجود دارد؟

## ۵. جمع بندی

برای پیدا کردن تعداد عناصر از `len()` استفاده می کنیم:

```python
len(my_list)
```

برای شمارش یک مقدار مشخص از `count()` استفاده می کنیم:

```python
my_list.count(value)
```

طول یک لیست خالی برابر است با:

```text
0
```

برای دسترسی به آخرین عنصر می توانیم از این روش استفاده کنیم:

```python
my_list[-1]
```

## تمرین ها

### تمرین ۱

یک لیست شامل پنج غذای مورد علاقه خود بسازید و طول آن را چاپ کنید.

### تمرین ۲

یک لیست شامل چند عدد تکراری بسازید و تعداد تکرار یکی از اعداد را با `count()` پیدا کنید.

### تمرین ۳

یک لیست از نمره های دانش آموزان بسازید و تعداد نمره های بزرگ تر یا مساوی `10` را بشمارید.

### تمرین ۴

یک لیست خالی بسازید و بررسی کنید که آیا خالی است یا نه.

---

# بخش ۱۱ — حذف عناصر از لیست

## ۱. مقدمه

گاهی لازم است یک یا چند عنصر را از لیست حذف کنیم.

پایتون روش های مختلفی برای حذف عناصر از لیست در اختیار ما قرار می دهد.

در این بخش با موارد زیر آشنا می شویم:

- `remove()`
- `pop()`
- `del`
- `clear()`

هر کدام کاربرد متفاوتی دارند.

## ۲. استفاده از `remove()`

متد `remove()` اولین تکرار یک مقدار مشخص را از لیست حذف می کند.

```python
fruits = ["Apple", "Banana", "Orange", "Banana"]

fruits.remove("Banana")

print(fruits)
```

خروجی:

```text
['Apple', 'Orange', 'Banana']
```

فقط اولین `"Banana"` حذف شد.

## ۳. حذف مقداری که وجود ندارد

اگر مقدار مورد نظر در لیست وجود نداشته باشد، `remove()` باعث ایجاد خطا می شود.

برای مثال:

```python
fruits = ["Apple", "Banana", "Orange"]

fruits.remove("Mango")
```

این کد باعث ایجاد `ValueError` می شود.

قبل از استفاده از `remove()` می توانیم بررسی کنیم که مقدار مورد نظر وجود دارد یا نه.

```python
fruits = ["Apple", "Banana", "Orange"]

if "Mango" in fruits:
    fruits.remove("Mango")

print(fruits)
```

خروجی:

```text
['Apple', 'Banana', 'Orange']
```

## ۴. استفاده از `pop()`

متد `pop()` یک عنصر را با استفاده از اندیس آن حذف می کند.

```python
fruits = ["Apple", "Banana", "Orange"]

fruits.pop(1)

print(fruits)
```

خروجی:

```text
['Apple', 'Orange']
```

اندیس `1` مربوط به `"Banana"` بود، بنابراین این عنصر حذف شد.

## ۵. استفاده از `pop()` بدون اندیس

اگر اندیس مشخص نکنیم، `pop()` آخرین عنصر را حذف می کند.

```python
fruits = ["Apple", "Banana", "Orange"]

fruits.pop()

print(fruits)
```

خروجی:

```text
['Apple', 'Banana']
```

## ۶. دریافت عنصر حذف شده

یکی از ویژگی های مفید `pop()` این است که عنصر حذف شده را برمی گرداند.

```python
fruits = ["Apple", "Banana", "Orange"]

removed_fruit = fruits.pop(1)

print(removed_fruit)
print(fruits)
```

خروجی:

```text
Banana
['Apple', 'Orange']
```

این ویژگی یکی از تفاوت های مهم `pop()` و `remove()` است.

## ۷. استفاده از `del`

دستور `del` می تواند یک عنصر را با استفاده از اندیس حذف کند.

```python
fruits = ["Apple", "Banana", "Orange"]

del fruits[1]

print(fruits)
```

خروجی:

```text
['Apple', 'Orange']
```

عنصر موجود در اندیس `1` حذف شد.

## ۸. استفاده از `del` برای چند عنصر

می توانیم از `del` همراه با برش نیز استفاده کنیم.

```python
numbers = [10, 20, 30, 40, 50]

del numbers[1:4]

print(numbers)
```

خروجی:

```text
[10, 50]
```

عناصر موجود در اندیس های `1`، `2` و `3` حذف شدند.

## ۹. استفاده از `clear()`

متد `clear()` تمام عناصر لیست را حذف می کند.

```python
fruits = ["Apple", "Banana", "Orange"]

fruits.clear()

print(fruits)
```

خروجی:

```text
[]
```

خود لیست همچنان وجود دارد، اما دیگر هیچ عنصری ندارد.

## ۱۰. تفاوت `remove()` و `pop()`

تفاوت اصلی این است که هر کدام عنصر مورد نظر را چگونه مشخص می کنند.

`remove()` با مقدار کار می کند:

```python
fruits.remove("Apple")
```

`pop()` با اندیس کار می کند:

```python
fruits.pop(0)
```

برای مثال:

```python
fruits = ["Apple", "Banana", "Orange"]

fruits.remove("Banana")

print(fruits)
```

خروجی:

```text
['Apple', 'Orange']
```

اما:

```python
fruits = ["Apple", "Banana", "Orange"]

fruits.pop(1)

print(fruits)
```

خروجی:

```text
['Apple', 'Orange']
```

هر دو `"Banana"` را حذف می کنند، اما روش پیدا کردن عنصر متفاوت است.

## ۱۱. تفاوت `pop()` و `del`

هر دو می توانند یک عنصر را با استفاده از اندیس حذف کنند.

تفاوت مهم این است که `pop()` عنصر حذف شده را برمی گرداند.

```python
fruits = ["Apple", "Banana", "Orange"]

removed = fruits.pop(1)

print(removed)
```

خروجی:

```text
Banana
```

اما `del` عنصر حذف شده را برنمی گرداند.

```python
fruits = ["Apple", "Banana", "Orange"]

del fruits[1]

print(fruits)
```

خروجی:

```text
['Apple', 'Orange']
```

## ۱۲. انتخاب روش مناسب

وقتی مقدار را می دانیم، از `remove()` استفاده می کنیم:

```python
fruits.remove("Banana")
```

وقتی اندیس را می دانیم و می خواهیم عنصر حذف شده را دریافت کنیم، از `pop()` استفاده می کنیم:

```python
removed = fruits.pop(1)
```

برای حذف یک عنصر یا یک بازه بر اساس اندیس از `del` استفاده می کنیم:

```python
del fruits[1]
```

برای حذف تمام عناصر از `clear()` استفاده می کنیم:

```python
fruits.clear()
```

## ۱۳. حذف انتخاب کاربر

می توانیم `input()`، `in` و `remove()` را با هم ترکیب کنیم.

```python
fruits = ["Apple", "Banana", "Orange"]

fruit = input("Enter a fruit to remove: ")

if fruit in fruits:
    fruits.remove(fruit)
    print(f"{fruit} was removed.")
else:
    print(f"{fruit} was not found.")

print(fruits)
```

نمونه خروجی:

```text
Enter a fruit to remove: Banana
Banana was removed.
['Apple', 'Orange']
```

## ۱۴. حذف آخرین عنصر

برای حذف آخرین عنصر می توانیم از `pop()` استفاده کنیم.

```python
tasks = ["Study", "Exercise", "Read"]

last_task = tasks.pop()

print(f"Removed task: {last_task}")
print(tasks)
```

خروجی:

```text
Removed task: Read
['Study', 'Exercise']
```

## ۱۵. حذف تمام تکرارهای یک مقدار

متد `remove()` فقط اولین تکرار را حذف می کند.

اگر بخواهیم تمام تکرارهای یک مقدار را حذف کنیم، می توانیم از حلقه استفاده کنیم.

```python
fruits = ["Apple", "Banana", "Apple", "Orange", "Apple"]

while "Apple" in fruits:
    fruits.remove("Apple")

print(fruits)
```

خروجی:

```text
['Banana', 'Orange']
```

حلقه تا زمانی ادامه پیدا می کند که `"Apple"` در لیست وجود داشته باشد.

## ۱۶. اشتباه های رایج

### اشتباه ۱ — اشتباه گرفتن مقدار و اندیس

این کد:

```python
fruits.remove(1)
```

می خواهد مقدار `1` را حذف کند.

این کد به معنی «حذف عنصر موجود در اندیس 1» نیست.

برای حذف عنصر اندیس `1` می توانیم از این روش استفاده کنیم:

```python
fruits.pop(1)
```

یا:

```python
del fruits[1]
```

### اشتباه ۲ — حذف مقدار موجود نبودن

این کد ممکن است خطا ایجاد کند:

```python
fruits = ["Apple", "Banana"]

fruits.remove("Mango")
```

روش امن تر:

```python
if "Mango" in fruits:
    fruits.remove("Mango")
```

### اشتباه ۳ — فراموش کردن مقدار برگشتی `pop()`

در این کد:

```python
removed = fruits.pop(1)
```

عنصر حذف شده داخل متغیر `removed` قرار می گیرد.

این ویژگی زمانی مفید است که بعد از حذف بخواهیم با آن عنصر کار کنیم.

## ۱۷. جمع بندی

برای حذف اولین مقدار مشخص از `remove()` استفاده می کنیم:

```python
my_list.remove(value)
```

برای حذف یک عنصر با اندیس از `pop()` استفاده می کنیم:

```python
my_list.pop(index)
```

برای حذف آخرین عنصر بدون مشخص کردن اندیس:

```python
my_list.pop()
```

برای حذف یک عنصر یا یک بازه بر اساس اندیس از `del` استفاده می کنیم:

```python
del my_list[index]
```

برای حذف تمام عناصر:

```python
my_list.clear()
```

به صورت خلاصه:

```text
remove() → مقدار
pop()    → اندیس
del      → اندیس یا برش
clear()  → همه عناصر
```

# تمرین ها

## تمرین ۱ — حذف یک میوه

یک لیست از میوه ها بسازید و `"Banana"` را با استفاده از `remove()` حذف کنید.

## تمرین ۲ — حذف با اندیس

یک لیست از اعداد بسازید و عنصر موجود در اندیس `2` را با استفاده از `pop()` حذف کنید.

## تمرین ۳ — ذخیره عنصر حذف شده

یک لیست از نام ها بسازید.

یک نام را با `pop()` حذف کنید و نام حذف شده را چاپ کنید.

## تمرین ۴ — حذف آخرین عنصر

یک لیست از کارها بسازید و آخرین کار را با استفاده از `pop()` حذف کنید.

## تمرین ۵ — خالی کردن لیست

یک لیست شامل چند عنصر بسازید و با استفاده از `clear()` آن را خالی کنید.

# مرور جامع

## سوال ۱

تفاوت `remove()` و `pop()` چیست؟

## سوال ۲

این برنامه چه چیزی چاپ می کند؟

```python
fruits = ["Apple", "Banana", "Orange", "Banana"]

fruits.remove("Banana")

print(fruits)
```

## سوال ۳

تفاوت این دو چیست؟

```python
fruits.pop(1)
```

و:

```python
del fruits[1]
```

## سوال ۴

برنامه ای بنویسید که یک میوه از کاربر دریافت کند و فقط در صورتی آن را از لیست حذف کند که در لیست وجود داشته باشد.

## سوال ۵

یک لیست از اعداد بسازید و تمام تکرارهای یک عدد مشخص را حذف کنید.

# چالش

## چالش Python Roadmap

یک برنامه ساده با نام **Task Manager** بسازید و از مفاهیمی که تا اینجا یاد گرفته اید استفاده کنید.

برنامه را با این لیست شروع کنید:

```python
tasks = ["Study Python", "Exercise", "Read", "Practice Lists"]
```

برنامه باید:

1. لیست کارها را چاپ کند.
2. تعداد کارها را چاپ کند.
3. از کاربر نام کاری را که می خواهد حذف کند دریافت کند.
4. با استفاده از `in` بررسی کند که آن کار وجود دارد یا نه.
5. در صورت وجود، آن کار را حذف کند.
6. نام کار حذف شده را چاپ کند.
7. لیست به روز شده را چاپ کند.
8. تعداد کارهای باقی مانده را چاپ کند.
9. در صورت پیدا نشدن کار، پیام مناسب نمایش دهد.

در این برنامه از متغیرها، `input`، تبدیل نوع در صورت نیاز، شرط ها، لیست ها، `len()`، `in`، `not in`، `remove()` و در صورت مناسب بودن `pop()` استفاده کنید.

---

# بخش ۱۲ — کپی کردن یک لیست

## ۱. مقدمه

گاهی لازم است یک کپی از یک لیست ایجاد کنیم تا بتوانیم کپی را تغییر دهیم بدون اینکه لیست اصلی تغییر کند.

این موضوع مهم است، چون قرار دادن یک لیست در یک متغیر دیگر با استفاده از انتساب ساده، یک کپی مستقل ایجاد نمی کند.

## ۲. مشکل انتساب ساده

این مثال را در نظر بگیرید:

```python
fruits = ["Apple", "Banana", "Orange"]

new_fruits = fruits

new_fruits.append("Mango")

print(fruits)
print(new_fruits)
```

خروجی:

```text
['Apple', 'Banana', 'Orange', 'Mango']
['Apple', 'Banana', 'Orange', 'Mango']
```

هر دو متغیر به یک لیست اشاره می کنند.

بنابراین تغییر `new_fruits` باعث تغییر `fruits` نیز می شود.

## ۳. کپی کردن با `copy()`

لیست ها یک متد به نام `copy()` دارند که یک کپی جداگانه ایجاد می کند.

```python
fruits = ["Apple", "Banana", "Orange"]

new_fruits = fruits.copy()

new_fruits.append("Mango")

print(fruits)
print(new_fruits)
```

خروجی:

```text
['Apple', 'Banana', 'Orange']
['Apple', 'Banana', 'Orange', 'Mango']
```

حالا دو لیست از هم جدا هستند.

تغییر `new_fruits` باعث تغییر `fruits` نمی شود.

## ۴. کپی کردن با برش

می توانیم با استفاده از برش نیز یک کپی ایجاد کنیم.

```python
fruits = ["Apple", "Banana", "Orange"]

new_fruits = fruits[:]

new_fruits.append("Mango")

print(fruits)
print(new_fruits)
```

خروجی:

```text
['Apple', 'Banana', 'Orange']
['Apple', 'Banana', 'Orange', 'Mango']
```

عبارت:

```python
fruits[:]
```

یک لیست جدید شامل تمام عناصر `fruits` ایجاد می کند.

## ۵. مقایسه روش ها

این دو روش یک لیست جداگانه ایجاد می کنند:

```python
new_fruits = fruits.copy()
```

و:

```python
new_fruits = fruits[:]
```

اما این روش یک لیست جداگانه ایجاد نمی کند:

```python
new_fruits = fruits
```

تفاوت اصلی در این است که آیا یک لیست جدید ساخته می شود یا نه.

## ۶. تغییر کپی

بعد از ایجاد کپی می توانیم آن را به صورت مستقل تغییر دهیم.

```python
numbers = [10, 20, 30]

copied_numbers = numbers.copy()

copied_numbers[0] = 100

print(numbers)
print(copied_numbers)
```

خروجی:

```text
[10, 20, 30]
[100, 20, 30]
```

فقط لیست کپی شده تغییر کرده است.

## ۷. حذف یک عنصر از کپی

می توانیم از متدهای لیست برای کپی نیز استفاده کنیم.

```python
fruits = ["Apple", "Banana", "Orange"]

copied_fruits = fruits.copy()

copied_fruits.remove("Banana")

print(fruits)
print(copied_fruits)
```

خروجی:

```text
['Apple', 'Banana', 'Orange']
['Apple', 'Orange']
```

لیست اصلی بدون تغییر باقی می ماند.

## ۸. اضافه کردن عناصر به کپی

می توانیم عناصر جدیدی به کپی اضافه کنیم.

```python
fruits = ["Apple", "Banana", "Orange"]

copied_fruits = fruits.copy()

copied_fruits.append("Mango")

print(fruits)
print(copied_fruits)
```

خروجی:

```text
['Apple', 'Banana', 'Orange']
['Apple', 'Banana', 'Orange', 'Mango']
```

## ۹. استفاده از کپی برای تغییرات امن

کپی کردن زمانی مفید است که بخواهیم داده اصلی را حفظ کنیم.

برای مثال:

```python
scores = [18, 15, 12, 9, 20]

updated_scores = scores.copy()

updated_scores.remove(9)

print("Original:", scores)
print("Updated:", updated_scores)
```

خروجی:

```text
Original: [18, 15, 12, 9, 20]
Updated: [18, 15, 12, 20]
```

نمره های اصلی همچنان در دسترس هستند.

## ۱۰. اشتباه های رایج

### اشتباه ۱ — تصور اینکه انتساب یک کپی ایجاد می کند

این کد یک لیست مستقل ایجاد نمی کند:

```python
new_list = old_list
```

هر دو متغیر به یک لیست اشاره می کنند.

### اشتباه ۲ — تغییر دادن لیست اشتباه

بعد از ایجاد کپی باید دقت کنیم کدام متغیر را تغییر می دهیم.

```python
fruits = ["Apple", "Banana"]

copied_fruits = fruits.copy()

copied_fruits.append("Orange")
```

در این حالت فقط `copied_fruits` تغییر می کند.

## ۱۱. جمع بندی

برای ایجاد یک کپی مستقل از لیست از `copy()` استفاده می کنیم:

```python
new_list = old_list.copy()
```

همچنین می توانیم با برش یک کپی ایجاد کنیم:

```python
new_list = old_list[:]
```

اگر به یک لیست مستقل نیاز داریم، نباید فقط از انتساب ساده استفاده کنیم:

```python
new_list = old_list
```

به یاد داشته باشید:

```text
copy() → یک لیست جدید ایجاد می کند
[:]    → یک لیست جدید ایجاد می کند
=      → به همان لیست اشاره می کند
```

# تمرین ها

## تمرین ۱ — ایجاد کپی

یک لیست شامل پنج میوه بسازید و با استفاده از `copy()` یک کپی از آن ایجاد کنید.

یک میوه جدید به کپی اضافه کنید و هر دو لیست را چاپ کنید.

## تمرین ۲ — کپی با برش

یک لیست از اعداد بسازید و با استفاده از `[:]` یک کپی ایجاد کنید.

یکی از عناصر کپی را تغییر دهید و هر دو لیست را چاپ کنید.

## تمرین ۳ — مقایسه انتساب و کپی

یک لیست بسازید و آن را با استفاده از `=` به یک متغیر دیگر نسبت دهید.

متغیر دوم را تغییر دهید و مشاهده کنید چه اتفاقی برای لیست اصلی می افتد.

سپس همین مثال را با `copy()` انجام دهید.

## تمرین ۴ — کپی و حذف

یک لیست از نام ها بسازید.

یک کپی از آن ایجاد کنید و یک نام را از کپی حذف کنید.

هر دو لیست را چاپ کنید.

## تمرین ۵ — کپی و به روز رسانی

یک لیست از نمره ها بسازید.

یک کپی ایجاد کنید، یک نمره را حذف کنید و یک نمره جدید به کپی اضافه کنید.

لیست اصلی و لیست به روز شده را چاپ کنید.

# مرور جامع

## سوال ۱

تفاوت این دو چیست؟

```python
new_list = old_list
```

و:

```python
new_list = old_list.copy()
```

## سوال ۲

این برنامه چه چیزی چاپ می کند؟

```python
numbers = [10, 20, 30]

copied_numbers = numbers.copy()

copied_numbers.append(40)

print(numbers)
print(copied_numbers)
```

## سوال ۳

برنامه ای بنویسید که با استفاده از برش یک کپی از یک لیست ایجاد کند.

## سوال ۴

یک لیست از میوه ها بسازید، یک کپی از آن ایجاد کنید، یک میوه را از کپی حذف کنید و هر دو لیست را چاپ کنید.

## سوال ۵

چرا وقتی می خواهیم داده اصلی بدون تغییر باقی بماند، کپی کردن لیست می تواند مفید باشد؟

# چالش

## چالش Python Roadmap

یک برنامه ساده با نام **Shopping List Manager** بسازید.

برنامه را با این لیست شروع کنید:

```python
shopping_list = ["Milk", "Bread", "Eggs", "Apples"]
```

برنامه باید:

1. لیست خرید اصلی را چاپ کند.
2. یک کپی از لیست ایجاد کند.
3. یک آیتم جدید از کاربر دریافت کند.
4. فقط در صورتی آیتم جدید را به لیست کپی شده اضافه کند که از قبل در آن وجود نداشته باشد.
5. یک آیتم برای حذف از کاربر دریافت کند.
6. فقط در صورتی آن آیتم را از لیست کپی شده حذف کند که وجود داشته باشد.
7. لیست اصلی را چاپ کند.
8. لیست کپی شده و به روز شده را چاپ کند.
9. تعداد آیتم های لیست به روز شده را چاپ کند.

در این برنامه از مفاهیمی که تا اینجا یاد گرفته اید استفاده کنید، از جمله متغیرها، ورودی، شرط ها، لیست ها، `len()`، `in`، `not in`، `append()`، `remove()` و `copy()`.
````

---

