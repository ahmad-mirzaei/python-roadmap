# بخش ۱ — لیست چیست؟

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

