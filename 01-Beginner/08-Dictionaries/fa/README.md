# بخش ۱ — مقدمه ای بر Dictionaryها

> 🌐 Language: **فارسی** | [English](../README.md)

---

| بخش | موضوع                                   |
| --: | --------------------------------------- |
|   ۱ | مقدمه ای بر دیکشنری ها                |
|   ۲ | ساخت دیکشنری                         |
|   ۳ | دسترسی به مقادیر دیکشنری           |
|   ۴ | اضافه کردن و به روز رسانی عناصر         |
|   ۵ |  حذف عناصر دیکشنری                     |
|   ۶ | بررسی وجود کلید و مقدار                 |
|   ۷ | طول دیکشنری                          |
|   ۸ | پیمایش دیکشنری ها                     |
|   ۹ | کلید ها و مقادیر دیکشنری             |
|  ۱۰ | جفت های کلید-مقدار                       |
|  ۱۱ | دیکشنری های تو در تو                  |
|  ۱۲ | کپی کردن دیکشنری                     |
|  ۱۳ | تبدیل دیکشنری به ساختارهای داده دیگر |
|  ۱۴ | مرور نهایی دیکشنری ها                 |
|  ۱۵ | پروژه کوچک دیکشنری                  |

---

## مقدمه

تا اینجا با **List** و **Tuple** آشنا شدیم. هر دو ساختار برای نگهداری چند مقدار استفاده می شوند، اما سازمان دهی اطلاعات در آن ها بیشتر بر اساس **موقعیت** یا **Index** انجام می شود.

Dictionary از یک مدل متفاوت استفاده می کند.

Dictionary اطلاعات را به صورت **جفت های Key-Value** ذخیره می کند؛ یعنی هر Value با یک Key معنادار مرتبط است.

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

در این مثال:

```text
"name"  → "Ali"
"age"   → 20
"score" → 18
```

Key مشخص می کند که Value چه چیزی را نشان می دهد.

---

## ۱. Dictionary چیست؟

Dictionary یک ساختار داده **تغییر پذیر** است که برای ذخیره رابطه بین Keyها و Valueها طراحی شده است.

ساختار کلی آن:

```python
{
    key: value,
    key: value,
    key: value
}
```

برای مثال:

```python
car = {
    "brand": "BMW",
    "model": "M4",
    "year": 2025
}
```

این Dictionary شامل سه جفت Key-Value است:

```text
brand → BMW
model → M4
year  → 2025
```

این ساختار زمانی بسیار مفید است که هر بخش از اطلاعات یک **نام یا شناسه مشخص** داشته باشد.

---

## ۲. تفاوت Dictionary و List

فرض کنید اطلاعات یک دانش آموز را در یک List ذخیره کنیم:

```python
student = ["Ali", 20, 18]
```

برای درک این اطلاعات باید از قبل بدانیم:

```text
Index 0 → name
Index 1 → age
Index 2 → score
```

برای مثال:

```python
print(student[0])
```

خروجی:

```text
Ali
```

اما `student[0]` به خودی خود نشان نمی دهد که چرا Index صفر مربوط به نام دانش آموز است.

همان اطلاعات را می توان با Dictionary نمایش داد:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

حالا:

```python
print(student["name"])
```

خروجی:

```text
Ali
```

در این حالت خود کد معنای داده را مشخص می کند.

تفاوت اصلی:

```text
List:
Index → Value

Dictionary:
Key → Value
```

---

## ۳. تفاوت Dictionary و Tuple

Tuple نیز از Index استفاده می کند:

```python
point = (10, 20)
```

دسترسی به عنصر:

```python
print(point[0])
```

خروجی:

```text
10
```

اما Tuple **تغییر ناپذیر** است.

در مقابل، Dictionary:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

**تغییر پذیر** است و اطلاعات را با استفاده از Keyهای معنادار سازمان دهی می کند.

| ساختار     | روش دسترسی | تغییر پذیر |
| ---------- | ---------- | ---------- |
| List       | Index      | بله        |
| Tuple      | Index      | خیر        |
| Dictionary | Key        | بله        |

---

## ۴. Key و Value

هر ورودی Dictionary از یک رابطه Key-Value تشکیل شده است:

```python
"name": "Ali"
```

در اینجا:

* `"name"` یک **Key** است.
* `"Ali"` یک **Value** است.

برای مثال:

```python
user = {
    "username": "ali123",
    "age": 20,
    "active": True
}
```

می توانیم ساختار آن را به این صورت ببینیم:

```text
Key        Value
----------------
username   ali123
age        20
active     True
```

Key معمولاً نقش یک **شناسه** را دارد و Value اطلاعات مرتبط با آن شناسه را نگهداری می کند.

---

## ۵. چرا Keyها مهم هستند؟

این List را در نظر بگیرید:

```python
product = ["Laptop", 2500, "Black", 15]
```

باید معنی هر موقعیت را به خاطر داشته باشیم:

```text
0 → name
1 → price
2 → color
3 → stock
```

اما در Dictionary:

```python
product = {
    "name": "Laptop",
    "price": 2500,
    "color": "Black",
    "stock": 15
}
```

هر Value نام مشخص خودش را دارد.

در نتیجه ساختار خواناتر می شود و وابستگی ما به حفظ کردن Indexها کاهش پیدا می کند.

---

## ۶. Dictionaryها تغییر پذیر هستند

یکی از ویژگی های مهم Dictionary این است که **تغییر پذیر** است.

یعنی بعد از ساخت Dictionary می توانیم محتوای آن را تغییر دهیم.

برای مثال:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

می توانیم سن را تغییر دهیم:

```python
student["age"] = 21
```

حالا:

```python
print(student)
```

خروجی:

```text
{'name': 'Ali', 'age': 21}
```

این موضوع با Tuple متفاوت است:

```python
point = (10, 20)
```

نمی توانیم یکی از عناصر Tuple را مستقیماً جایگزین کنیم.

---

## ۷. Valueها می توانند از نوع های مختلف باشند

Valueهای Dictionary محدود به یک نوع داده نیستند.

برای مثال:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18.5,
    "active": True
}
```

در این مثال Valueها شامل موارد زیر هستند:

* `str`
* `int`
* `float`
* `bool`

حتی یک Value می تواند خودش یک ساختار داده دیگر باشد:

```python
student = {
    "name": "Ali",
    "scores": [18, 20, 17]
}
```

یا حتی یک Dictionary دیگر:

```python
student = {
    "name": "Ali",
    "address": {
        "city": "Tehran",
        "country": "Iran"
    }
}
```

ساختارهای تو در تو را در بخش **Dictionaryهای تو در تو** با جزئیات بیشتری بررسی خواهیم کرد.

---

## ۸. چه زمانی از Dictionary استفاده کنیم؟

Dictionary زمانی انتخاب مناسبی است که بین یک شناسه مشخص و اطلاعات مرتبط با آن رابطه وجود داشته باشد.

برای مثال:

```python
user = {
    "username": "ali123",
    "email": "ali@example.com",
    "age": 20
}
```

یا:

```python
car = {
    "brand": "BMW",
    "model": "M4",
    "year": 2025
}
```

یا:

```python
book = {
    "title": "Python",
    "author": "John",
    "pages": 350
}
```

در تمام این مثال ها Keyها به Valueها معنا می دهند.

---

## ۹. Dictionary فقط یک Syntax متفاوت نیست

نباید Dictionary را صرفاً یک List با Syntax متفاوت در نظر بگیریم.

List زمانی مناسب است که مجموعه ای از مقادیر را بر اساس موقعیت آن ها مدیریت کنیم:

```python
numbers = [10, 20, 30]
```

Tuple زمانی مناسب است که به یک مجموعه مرتب و تغییر ناپذیر نیاز داشته باشیم:

```python
point = (10, 20)
```

اما Dictionary زمانی مناسب است که رابطه بین **Key و Value** بخش اصلی داده باشد:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

مقایسه کنید:

```python
student[0]
```

با:

```python
student["name"]
```

اولی یک موقعیت را توصیف می کند.

دومی معنای داده ای را که می خواهیم دریافت کنیم مشخص می کند.

این تفاوت برای انتخاب درست ساختارهای داده در پایتون بسیار مهم است.

---

## نکات کلیدی

تا پایان این بخش باید بدانید:

* Dictionary داده ها را به صورت **جفت های Key-Value** ذخیره می کند.
* Key یک Value را شناسایی یا توصیف می کند.
* دسترسی به Dictionary بر اساس Key انجام می شود، نه Index عددی.
* Dictionaryها **تغییر پذیر** هستند.
* Valueها می توانند از نوع های مختلف باشند.
* یک Value می تواند خودش شامل یک ساختار داده دیگر باشد.
* Dictionary برای نمایش اطلاعات ساختار یافته بسیار مناسب است.
* انتخاب Dictionary معمولاً زمانی منطقی است که **رابطه بین یک نام و یک مقدار** بخش اصلی داده باشد.

---

# سوال های بخش

## سوال ۱

تفاوت اصلی دسترسی به داده در List و Dictionary چیست؟

برای هر کدام یک مثال بنویسید.

## سوال ۲

Keyها و Valueهای Dictionary زیر را مشخص کنید:

```python
student = {
    "name": "Sara",
    "age": 19,
    "score": 20
}
```

## سوال ۳

چرا Dictionary می تواند برای نمایش اطلاعات یک User نسبت به یک List انتخاب مناسب تری باشد؟

دو ساختار زیر را با هم مقایسه کنید:

```python
user = ["Ali", 20, True]
```

و:

```python
user = {
    "name": "Ali",
    "age": 20,
    "active": True
}
```

---

# سوال جامع

با توجه به مباحثی که تاکنون درباره **List، Tuple و Dictionary** یاد گرفته اید، برای هر مورد ساختار مناسب را انتخاب کنید و دلیل خود را توضیح دهید:

1. نگهداری چند Score که ترتیب آن ها مهم است و ممکن است تغییر کنند.
2. نگهداری مختصات ثابت `x` و `y` یک نقطه.
3. نگهداری اطلاعات یک User مانند نام، سن و وضعیت فعال بودن.

---

# پاسخ ها

## پاسخ سوال ۱

List معمولاً از Index عددی استفاده می کند:

```python
numbers = [10, 20, 30]

print(numbers[1])
```

Dictionary از Key استفاده می کند:

```python
student = {
    "name": "Ali",
    "age": 20
}

print(student["name"])
```

بنابراین:

```text
List       → Index → Value
Dictionary → Key   → Value
```

## پاسخ سوال ۲

Keyها:

```text
"name"
"age"
"score"
```

Valueها:

```text
"Sara"
19
20
```

## پاسخ سوال ۳

Dictionary به هر Value یک شناسه معنادار می دهد.

در List:

```python
user = ["Ali", 20, True]
```

باید به خاطر داشته باشیم هر Index چه معنایی دارد.

در Dictionary:

```python
user = {
    "name": "Ali",
    "age": 20,
    "active": True
}
```

معنای هر Value به صورت واضح مشخص است.

## پاسخ سوال جامع

### ۱. List

```python
scores = [18, 20, 17, 19]
```

List مناسب است چون ترتیب اهمیت دارد و Valueها می توانند تغییر کنند.

### ۲. Tuple

```python
point = (10, 20)
```

Tuple مناسب است چون دو مقدار مختصات یک مجموعه مرتب و تغییر ناپذیر را تشکیل می دهند.

### ۳. Dictionary

```python
user = {
    "name": "Ali",
    "age": 20,
    "active": True
}
```

Dictionary مناسب است چون هر Value یک نام مشخص دارد و می توان آن را از طریق همان شناسه دریافت کرد.

---

# بخش ۲ — ساخت Dictionary

## مقدمه

حالا که با مفهوم Dictionary و دلیل استفاده از آن آشنا شدیم، قدم بعدی یادگیری **روش های مختلف ساخت Dictionary** است.

رایج ترین روش استفاده از آکولاد `{}` و جفت های Key-Value است:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

الگوی اصلی:

```python
dictionary = {
    key: value,
    key: value
}
```

روش های مختلف ساخت Dictionary زمانی اهمیت پیدا می کنند که داده های ما از شکل های متفاوتی در اختیارمان باشند.

---

## ۱. ساخت Dictionary خالی

می توانیم با `{}` یک Dictionary خالی بسازیم:

```python
student = {}
```

در این لحظه Dictionary هیچ عضوی ندارد.

بعداً می توانیم اطلاعات را به آن اضافه کنیم:

```python
student["name"] = "Ali"
student["age"] = 20
```

حالا:

```python
print(student)
```

خروجی:

```text
{'name': 'Ali', 'age': 20}
```

این روش زمانی مفید است که اطلاعات از ابتدا به صورت کامل در اختیار برنامه نباشد.

---

## ۲. ساخت Dictionary همراه با داده های اولیه

اگر از ابتدا داده ها را داشته باشیم، می توانیم آن ها را هنگام ساخت Dictionary قرار دهیم:

```python
student = {
    "name": "Ali",
    "age": 20,
    "major": "Computer Science"
}
```

هر ورودی از ساختار زیر پیروی می کند:

```text
Key: Value
```

و جفت های مختلف با کاما از هم جدا می شوند.

برای مثال:

```text
"name": "Ali"
```

یعنی:

```text
Key   → "name"
Value → "Ali"
```

---

## ۳. ساخت Dictionary با `dict()`

پایتون Constructorای به نام `dict()` نیز دارد:

```python
student = dict()
```

این دستور یک Dictionary خالی ایجاد می کند.

از نظر نتیجه با این کد یکسان است:

```python
student = {}
```

برای حالت های ساده، `{}` معمولاً کوتاه تر و مستقیم تر است.

اما `dict()` زمانی اهمیت بیشتری پیدا می کند که بخواهیم Dictionary را از داده های موجود بسازیم.

---

## ۴. استفاده از Keyword Argumentها در `dict()`

می توانیم هنگام استفاده از `dict()` از Keyword Argument استفاده کنیم:

```python
student = dict(
    name="Ali",
    age=20,
    major="Computer Science"
)
```

نتیجه:

```python
{
    "name": "Ali",
    "age": 20,
    "major": "Computer Science"
}
```

نام Keywordها به عنوان Key استفاده می شود.

این روش زمانی مناسب است که Keyها شناسه های معتبر پایتون باشند.

مثلاً:

```python
user = dict(
    username="ali123",
    active=True
)
```

اما نمی توانیم مستقیماً Keyهایی مانند:

```text
"first-name"
```

را با این روش بنویسیم، چون `first-name` یک Python Identifier معتبر نیست.

در چنین شرایطی استفاده از `{}` انعطاف بیشتری دارد:

```python
user = {
    "first-name": "Ali"
}
```

---

## ۵. ساخت Dictionary از جفت های Key-Value

اگر داده های ما از قبل به صورت جفت وجود داشته باشند، می توانیم از `dict()` استفاده کنیم:

```python
student = dict([
    ("name", "Ali"),
    ("age", 20),
    ("score", 18)
])
```

هر Tuple داخلی شامل:

```text
(Key, Value)
```

است.

پایتون این جفت ها را به ورودی های Dictionary تبدیل می کند.

نتیجه:

```python
{
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

این روش زمانی مفید است که داده های ما از قبل به صورت مجموعه ای از جفت ها در اختیارمان باشند.

---

## ۶. ساخت Dictionary از دو Sequence با `zip()`

یکی از روش های مهم دیگر استفاده از `zip()` است.

فرض کنید Keyها و Valueها در دو Sequence جداگانه قرار دارند:

```python
keys = ["name", "age", "score"]
values = ["Ali", 20, 18]

student = dict(zip(keys, values))
```

نتیجه:

```python
{
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

در واقع `zip()` عناصر متناظر را به هم متصل می کند:

```text
"name"  → "Ali"
"age"   → 20
"score" → 18
```

این روش زمانی بسیار کاربردی است که Keyها و Valueها از قبل جدا از یکدیگر ذخیره شده باشند.

---

## ۷. ساخت Dictionary از یک Dictionary موجود

می توانیم بر اساس یک Dictionary موجود، Dictionary دیگری بسازیم:

```python
student = {
    "name": "Ali",
    "age": 20
}

copy_student = dict(student)
```

حالا `copy_student` همان جفت های Key-Value را دارد:

```python
print(copy_student)
```

خروجی:

```text
{'name': 'Ali', 'age': 20}
```

در این حالت یک Dictionary جدید ایجاد می شود که ورودی های سطح اول Dictionary قبلی را دارد.

این موضوع با صرفاً اختصاص دادن یک Variable دیگر به همان Dictionary متفاوت است:

```python
student = {
    "name": "Ali"
}

other = student
```

در این حالت `student` و `other` به یک شیء Dictionary اشاره می کنند.

موضوع Copy کردن را در بخش مربوط به خودش با جزئیات بیشتری بررسی خواهیم کرد.

---

## ۸. Keyهای تکراری

Keyهای Dictionary یکتا هستند.

مثلاً:

```python
student = {
    "name": "Ali",
    "name": "Sara"
}
```

Value دوم جای Value اول را می گیرد.

در نتیجه:

```python
{
    "name": "Sara"
}
```

بنابراین تکرار یک Key باعث ایجاد چند ورودی مستقل نمی شود.

این ویژگی به دلیل نقش Key در شناسایی یک Value اهمیت زیادی دارد.

---

## ۹. اضافه کردن اطلاعات بعد از ساخت

لازم نیست Dictionary از همان ابتدا کامل باشد.

می توانیم ابتدا این Dictionary را بسازیم:

```python
student = {
    "name": "Ali"
}
```

و بعد اطلاعات بیشتری به آن اضافه کنیم:

```python
student["age"] = 20
student["score"] = 18
```

در نهایت:

```python
{
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

این رفتار یکی از نتایج تغییر پذیر بودن Dictionary است.

---

## ۱۰. انتخاب روش مناسب برای ساخت Dictionary

هر روش ساخت در موقعیت خاصی مناسب تر است.

### زمانی که داده از قبل مشخص است

از `{}` استفاده می کنیم:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

### زمانی که Keyها Identifierهای ساده هستند

می توانیم از `dict()` استفاده کنیم:

```python
student = dict(name="Ali", age=20)
```

### زمانی که داده به صورت جفت در اختیارمان است

می توانیم از `dict()` استفاده کنیم:

```python
pairs = [
    ("name", "Ali"),
    ("age", 20)
]

student = dict(pairs)
```

### زمانی که Keyها و Valueها جدا هستند

می توانیم از `zip()` استفاده کنیم:

```python
keys = ["name", "age"]
values = ["Ali", 20]

student = dict(zip(keys, values))
```

نکته مهم این نیست که تمام Syntaxها را حفظ کنیم؛ مهم این است که بدانیم **داده فعلی ما چه شکلی دارد** و مناسب ترین روش ساخت را بر اساس همان انتخاب کنیم.

---

## نکات کلیدی

* `{}` مستقیم ترین روش ساخت Dictionary است.
* `dict()` می تواند Dictionary خالی بسازد یا از داده های موجود یک Dictionary ایجاد کند.
* می توان از Keyword Argumentها در `dict()` استفاده کرد.
* Dictionary را می توان از مجموعه ای از جفت های `(Key, Value)` ساخت.
* `zip()` برای ترکیب Sequenceهای جداگانه Key و Value بسیار مفید است.
* Keyهای تکراری باعث ایجاد ورودی های جداگانه نمی شوند.
* در صورت تکرار Key، Value بعدی جای Value قبلی را می گیرد.
* می توان Dictionary را خالی ساخت و بعداً آن را تکمیل کرد.
* انتخاب روش ساخت باید بر اساس شکل داده های موجود انجام شود.

---

# سوال های بخش

## سوال ۱

با استفاده از `{}` یک Dictionary به نام `book` بسازید که شامل اطلاعات زیر باشد:

```text
title  → "Python"
author → "Ali"
pages  → 300
```

## سوال ۲

Dictionary زیر را با استفاده از `dict()` و Keyword Argumentها بسازید:

```text
name → "Sara"
age  → 21
```

## سوال ۳

با توجه به کد زیر، با استفاده از `zip()` یک Dictionary بسازید:

```python
keys = ["name", "age", "city"]
values = ["Ali", 20, "Tehran"]
```

---

# سوال جامع

داده های زیر را دریافت کرده اید:

```python
keys = ["username", "age", "active"]
values = ["ali123", 20, True]
```

با استفاده از این داده ها یک Dictionary بسازید و توضیح دهید چرا در این شرایط استفاده از `zip()` نسبت به نوشتن دستی تمام جفت های Key-Value مناسب تر است.

---

# پاسخ ها

## پاسخ سوال ۱

```python
book = {
    "title": "Python",
    "author": "Ali",
    "pages": 300
}
```

## پاسخ سوال ۲

```python
student = dict(
    name="Sara",
    age=21
)
```

## پاسخ سوال ۳

```python
keys = ["name", "age", "city"]
values = ["Ali", 20, "Tehran"]

data = dict(zip(keys, values))
```

نتیجه:

```python
{
    "name": "Ali",
    "age": 20,
    "city": "Tehran"
}
```

## پاسخ سوال جامع

```python
keys = ["username", "age", "active"]
values = ["ali123", 20, True]

user = dict(zip(keys, values))
```

نتیجه:

```python
{
    "username": "ali123",
    "age": 20,
    "active": True
}
```

استفاده از `zip()` مناسب است چون Keyها و Valueها از قبل در دو Sequence جداگانه قرار دارند. `zip()` عناصر متناظر را به صورت خودکار به یکدیگر متصل می کند و نیاز به نوشتن دستی هر جفت را از بین می برد.

---

# بخش ۳ — دسترسی به Valueهای Dictionary

## مقدمه

ساخت Dictionary فقط نقطه شروع کار است. مهارت مهم بعدی این است که یاد بگیریم چگونه **Valueهای ذخیره شده در Dictionary را دریافت کنیم**.

بر خلاف List و Tuple که معمولاً با Index عددی به عناصر آن ها دسترسی پیدا می کنیم، در Dictionary از **Key** برای دسترسی به Value مربوط به آن استفاده می کنیم.

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

برای دریافت نام:

```python
print(student["name"])
```

خروجی:

```text
Ali
```

Key یعنی `"name"` دقیقاً مشخص می کند که کدام Value را می خواهیم.

---

## ۱. دسترسی به Value با براکت

مستقیم ترین روش دسترسی به Value یک Dictionary استفاده از Key داخل `[]` است:

```python
student = {
    "name": "Ali",
    "age": 20
}

print(student["name"])
```

خروجی:

```text
Ali
```

برای Valueهای دیگر نیز همین روش را داریم:

```python
print(student["age"])
```

خروجی:

```text
20
```

الگوی کلی:

```python
dictionary[key]
```

این موضوع با:

```python
list[index]
```

تفاوت اساسی دارد، چون Dictionary به جای موقعیت عددی، از **شناسه داده** برای دسترسی استفاده می کند.

---

## ۲. دسترسی به Valueهای انواع مختلف

Value مربوط به یک Key می تواند از انواع مختلف داده باشد.

```python
user = {
    "name": "Ali",
    "age": 20,
    "active": True
}
```

می توانیم هر کدام را جداگانه دریافت کنیم:

```python
print(user["name"])
print(user["age"])
print(user["active"])
```

خروجی:

```text
Ali
20
True
```

Key مشخص می کند کدام Value برگردانده شود.

---

## ۳. استفاده از Variable به عنوان Key

Key لازم نیست حتماً مستقیماً داخل براکت نوشته شود.

می توانیم آن را داخل یک Variable قرار دهیم:

```python
student = {
    "name": "Ali",
    "age": 20
}

field = "name"

print(student[field])
```

خروجی:

```text
Ali
```

پایتون ابتدا مقدار `field` را به دست می آورد که `"name"` است و سپس از آن به عنوان Key استفاده می کند.

این قابلیت زمانی مهم می شود که Key مورد نظر در زمان اجرای برنامه مشخص شود.

مثلاً:

```python
field = input("Enter a field: ")

print(student[field])
```

اگر کاربر وارد کند:

```text
age
```

پایتون عملاً این دسترسی را انجام می دهد:

```python
student["age"]
```

---

## ۴. اگر Key وجود نداشته باشد چه اتفاقی می افتد؟

فرض کنید Dictionary ما این باشد:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

حالا:

```python
print(student["score"])
```

Key به نام `"score"` وجود ندارد.

در نتیجه پایتون خطای `KeyError` ایجاد می کند:

```text
KeyError: 'score'
```

این رفتار مهم است.

وقتی از براکت استفاده می کنیم، انتظار داریم Key مورد نظر واقعاً وجود داشته باشد.

بنابراین:

```python
dictionary[key]
```

زمانی مناسب است که وجود Key را انتظار داریم.

---

## ۵. دسترسی با `.get()`

پایتون روش دیگری برای دریافت Value در اختیارمان قرار می دهد:

```python
student = {
    "name": "Ali",
    "age": 20
}

print(student.get("name"))
```

خروجی:

```text
Ali
```

تفاوت مهم زمانی مشخص می شود که Key وجود نداشته باشد:

```python
print(student.get("score"))
```

در این حالت به جای `KeyError` مقدار:

```text
None
```

برگردانده می شود.

به همین دلیل `.get()` زمانی مفید است که احتمال دارد Key مورد نظر وجود نداشته باشد.

---

## ۶. تعیین مقدار پیش فرض با `.get()`

متد `.get()` می تواند یک آرگومان دوم نیز دریافت کند:

```python
student = {
    "name": "Ali",
    "age": 20
}

print(student.get("score", 0))
```

خروجی:

```text
0
```

ساختار کلی:

```python
dictionary.get(key, default)
```

اگر Key وجود داشته باشد، Value آن برگردانده می شود.

اگر Key وجود نداشته باشد، مقدار پیش فرض برگردانده می شود.

مثلاً:

```python
print(student.get("age", 0))
```

خروجی:

```text
20
```

چون `"age"` وجود دارد، مقدار پیش فرض `0` نادیده گرفته می شود.

---

## ۷. مقایسه `[]` و `.get()`

این دو روش برای شرایط متفاوتی مناسب هستند.

### براکت

```python
student["score"]
```

وقتی استفاده می کنیم که انتظار داریم Key وجود داشته باشد.

اگر وجود نداشته باشد:

```text
KeyError
```

ایجاد می شود.

### `.get()`

```python
student.get("score")
```

زمانی مناسب است که احتمال می دهیم Key وجود نداشته باشد.

در صورت نبودن Key:

```text
None
```

برگردانده می شود.

یا می توانیم مقدار پیش فرض تعیین کنیم:

```python
student.get("score", 0)
```

یک مدل ذهنی مفید:

```text
[]     → «انتظار دارم این Key وجود داشته باشد.»

.get() → «ممکن است این Key وجود نداشته باشد.»
```

---

## ۸. دسترسی به Valueهای تو در تو

Value یک Dictionary می تواند خودش یک Dictionary دیگر باشد.

برای مثال:

```python
student = {
    "name": "Ali",
    "address": {
        "city": "Tehran",
        "country": "Iran"
    }
}
```

برای دسترسی به `"city"`:

```python
print(student["address"]["city"])
```

خروجی:

```text
Tehran
```

دسترسی در دو مرحله انجام می شود:

```text
student
   ↓
"address"
   ↓
"city"
```

ابتدا Dictionary مربوط به `"address"` را دریافت می کنیم و سپس از داخل آن به `"city"` دسترسی پیدا می کنیم.

---

## ۹. دسترسی به Valueهایی که ساختار داده دیگری هستند

یک Value می تواند یک List باشد:

```python
student = {
    "name": "Ali",
    "scores": [18, 20, 17]
}
```

ابتدا می توانیم خود List را دریافت کنیم:

```python
print(student["scores"])
```

خروجی:

```text
[18, 20, 17]
```

سپس می توانیم با استفاده از Index به یکی از عناصر آن دسترسی پیدا کنیم:

```python
print(student["scores"][0])
```

خروجی:

```text
18
```

این مثال یک اصل مهم را نشان می دهد:

> هر ساختار داده از روش دسترسی مخصوص خودش استفاده می کند.

Dictionary با Key:

```python
student["scores"]
```

و List با Index:

```python
student["scores"][0]
```

---

## ۱۰. دریافت Value بدون تغییر Dictionary

صرفاً دسترسی به یک Value باعث تغییر Dictionary نمی شود:

```python
student = {
    "name": "Ali",
    "age": 20
}

age = student["age"]

print(age)
print(student)
```

خروجی:

```text
20
{'name': 'Ali', 'age': 20}
```

Dictionary بدون تغییر باقی می ماند.

این موضوع با:

```python
student["age"] = 21
```

متفاوت است.

در این حالت دیگر فقط در حال دسترسی نیستیم؛ بلکه Dictionary را تغییر می دهیم.

---

## ۱۱. استفاده از Valueهای دریافت شده در Expressionها

Value دریافت شده از Dictionary می تواند مستقیماً در محاسبات و شرط ها استفاده شود.

برای مثال:

```python
student = {
    "name": "Ali",
    "score": 18
}

if student["score"] >= 10:
    print("Passed")
```

خروجی:

```text
Passed
```

یا:

```python
total = student["score"] + 2

print(total)
```

خروجی:

```text
20
```

Value دریافت شده مانند همان داده ای رفتار می کند که در Dictionary ذخیره شده است.

---

## ۱۲. دسترسی به Keyهایی با کاراکترهای خاص

Keyها الزاماً نباید کلمات ساده باشند.

برای مثال:

```python
data = {
    "first-name": "Ali",
    "email.address": "ali@example.com"
}
```

می توانیم این Valueها را با براکت دریافت کنیم:

```python
print(data["first-name"])
print(data["email.address"])
```

خروجی:

```text
Ali
ali@example.com
```

این موضوع یکی دیگر از دلایل اهمیت روش براکتی است؛ چون با Keyهای مختلف Dictionary کار می کند.

---

## نکات کلیدی

* Valueهای Dictionary معمولاً با استفاده از Key دریافت می شوند.
* ساختار دسترسی با براکت به صورت `dictionary[key]` است.
* اگر Key وجود نداشته باشد، دسترسی براکتی `KeyError` ایجاد می کند.
* `.get()` زمانی مناسب است که احتمال می دهیم Key وجود نداشته باشد.
* `.get(key, default)` امکان تعیین مقدار پیش فرض را فراهم می کند.
* می توان از Variable به عنوان Key استفاده کرد.
* Valueهای Dictionary می توانند خودشان شامل ساختارهای داده دیگر باشند.
* برای ساختارهای تو در تو باید روش دسترسی هر ساختار را به ترتیب استفاده کنیم.
* خواندن یک Value به تنهایی Dictionary را تغییر نمی دهد.
* Value دریافت شده می تواند مستقیماً در محاسبات و شرط ها استفاده شود.

---

# سوال های بخش

## سوال ۱

با توجه به Dictionary زیر، کدی بنویسید که `name` و `score` دانش آموز را چاپ کند:

```python
student = {
    "name": "Sara",
    "age": 19,
    "score": 20
}
```

## سوال ۲

تفاوت دو عبارت زیر چیست؟

```python
student["score"]
```

و:

```python
student.get("score")
```

اگر `"score"` وجود نداشته باشد، هر کدام چه رفتاری دارند؟

## سوال ۳

با توجه به Dictionary زیر، کدی بنویسید که مقدار `"city"` را چاپ کند:

```python
student = {
    "name": "Ali",
    "address": {
        "city": "Tehran",
        "country": "Iran"
    }
}
```

---

# سوال جامع

Dictionary زیر را در نظر بگیرید:

```python
user = {
    "name": "Ali",
    "age": 20,
    "profile": {
        "city": "Tehran",
        "active": True
    },
    "scores": [18, 20, 17]
}
```

کدی بنویسید که:

1. نام User را دریافت کند.
2. شهر User را دریافت کند.
3. اولین Score را دریافت کند.
4. Keyای به نام `"email"` را به صورت امن دریافت کند و اگر وجود نداشت، `"Not provided"` را برگرداند.

در هر مورد توضیح دهید از چه روش دسترسی استفاده کرده اید و چرا.

---

# پاسخ ها

## پاسخ سوال ۱

```python
print(student["name"])
print(student["score"])
```

## پاسخ سوال ۲

هر دو عبارت در صورتی که Key وجود داشته باشد، Value مربوط به `"score"` را دریافت می کنند.

اما:

```python
student["score"]
```

اگر `"score"` وجود نداشته باشد، `KeyError` ایجاد می کند.

در مقابل:

```python
student.get("score")
```

اگر Key وجود نداشته باشد، `None` برمی گرداند.

همچنین می توان مقدار پیش فرض تعیین کرد:

```python
student.get("score", 0)
```

## پاسخ سوال ۳

```python
print(student["address"]["city"])
```

ابتدا Value مربوط به `"address"` دریافت می شود و سپس از Dictionary داخلی، Value مربوط به `"city"` دریافت می شود.

## پاسخ سوال جامع

```python
user = {
    "name": "Ali",
    "age": 20,
    "profile": {
        "city": "Tehran",
        "active": True
    },
    "scores": [18, 20, 17]
}

print(user["name"])
print(user["profile"]["city"])
print(user["scores"][0])
print(user.get("email", "Not provided"))
```

برای `"name"` از دسترسی مستقیم استفاده شده، چون می دانیم این Key وجود دارد.

برای `"city"` دو بار از دسترسی Dictionary استفاده شده، چون `"city"` داخل Dictionary مربوط به `"profile"` قرار دارد.

برای اولین Score ابتدا به `"scores"` دسترسی پیدا کرده ایم و سپس از Index صفر List استفاده کرده ایم.

برای `"email"` از `.get()` استفاده شده، چون ممکن است این Key وجود نداشته باشد و می خواهیم به جای `KeyError` یک مقدار پیش فرض داشته باشیم.

---

# بخش ۴ — اضافه کردن و به روز رسانی آیتم های Dictionary

## مقدمه

تا اینجا یاد گرفتیم چگونه یک Dictionary بسازیم و چگونه Valueهای ذخیره شده در آن را دریافت کنیم.

حالا باید یاد بگیریم چگونه **Dictionary را بعد از ساخته شدن تغییر دهیم**.

Dictionaryها **تغییر پذیر** هستند؛ یعنی بعد از ساخته شدن می توان محتویات آن ها را تغییر داد.

در این بخش با دو عملیات مهم آشنا می شویم:

* **اضافه کردن** یک جفت Key-Value جدید
* **به روز رسانی** Value مربوط به یک Key موجود

درک تفاوت این دو عملیات برای کار با داده های واقعی بسیار مهم است.

---

## ۱. اضافه کردن یک آیتم جدید

اگر Key مورد نظر در Dictionary وجود نداشته باشد، می توانیم با انتساب یک Value به آن، یک آیتم جدید ایجاد کنیم:

```python
student = {
    "name": "Ali",
    "age": 20
}

student["score"] = 18
```

حالا Dictionary شامل این موارد است:

```python
{
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

الگوی کلی:

```python
dictionary[key] = value
```

اگر `key` وجود نداشته باشد، Python یک ورودی جدید ایجاد می کند.

---

## ۲. به روز رسانی یک آیتم موجود

همین Syntax برای تغییر Value یک Key موجود نیز استفاده می شود:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

student["score"] = 20
```

حالا:

```python
print(student)
```

نتیجه:

```text
{'name': 'Ali', 'age': 20, 'score': 20}
```

Python یک `"score"` جدید ایجاد نمی کند.

بلکه Value مربوط به Key موجود را جایگزین می کند.

بنابراین:

```python
dictionary[key] = value
```

می تواند دو معنی داشته باشد:

```text
Key جدید       → اضافه کردن آیتم
Key موجود      → به روز رسانی Value
```

این رفتار یکی از مهم ترین ویژگی های انتساب در Dictionary است.

---

## ۳. اضافه کردن چند آیتم

می توانیم چند آیتم را یکی پس از دیگری اضافه کنیم:

```python
student = {}

student["name"] = "Ali"
student["age"] = 20
student["score"] = 18
```

نتیجه:

```python
{
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

این روش زمانی مناسب است که اطلاعات به صورت تدریجی در اختیار برنامه قرار می گیرند.

برای مثال، ممکن است داده ها از ورودی کاربر دریافت شوند:

```python
student = {}

student["name"] = input("Name: ")
student["age"] = int(input("Age: "))
```

در این حالت Dictionary هم زمان با دریافت اطلاعات تکمیل می شود.

---

## ۴. به روز رسانی چند آیتم با `update()`

اگر بخواهیم چند Key-Value را هم زمان اضافه یا به روز رسانی کنیم، متد `update()` بسیار کاربردی است.

```python
student = {
    "name": "Ali",
    "age": 20
}

student.update({
    "age": 21,
    "score": 19
})
```

بعد از اجرای `update()`:

```python
{
    "name": "Ali",
    "age": 21,
    "score": 19
}
```

دقت کنید چه اتفاقی افتاده است:

* `"age"` از قبل وجود داشته، پس Value آن به روز رسانی شده است.
* `"score"` وجود نداشته، پس یک آیتم جدید ایجاد شده است.

بنابراین `update()` می تواند هر دو عملیات را هم زمان انجام دهد.

---

## ۵. استفاده از Keyword Argument در `update()`

برای Keyهای مناسب، `update()` می تواند Keyword Argument نیز دریافت کند:

```python
student.update(
    age=21,
    score=19
)
```

این روش زمانی مناسب است که Keyها Identifierهای معتبر Python باشند.

اما اگر Key شامل کاراکترهایی مانند `-` یا `.` باشد، بهتر است از Dictionary استفاده کنیم:

```python
student.update({
    "first-name": "Ali",
    "email.address": "ali@example.com"
})
```

---

## ۶. به روز رسانی از یک Dictionary دیگر

یکی از کاربردهای رایج این است که اطلاعات یک Dictionary دیگر را وارد Dictionary فعلی کنیم:

```python
student = {
    "name": "Ali",
    "age": 20
}

extra_data = {
    "age": 21,
    "score": 19
}

student.update(extra_data)
```

نتیجه:

```python
{
    "name": "Ali",
    "age": 21,
    "score": 19
}
```

Keyهای موجود به روز رسانی می شوند و Keyهای جدید اضافه می شوند.

---

## ۷. به روز رسانی از یک Iterable از جفت ها

`update()` می تواند یک Iterable شامل جفت های Key-Value نیز دریافت کند:

```python
student = {
    "name": "Ali"
}

student.update([
    ("age", 20),
    ("score", 18)
])
```

نتیجه:

```python
{
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

این روش زمانی مفید است که داده ورودی از قبل به صورت جفت ها در اختیارمان باشد.

---

## ۸. `update()` Dictionary اصلی را تغییر می دهد

یک نکته مهم درباره `update()` این است که خود Dictionary موجود را تغییر می دهد.

```python
student = {
    "name": "Ali"
}

result = student.update({
    "age": 20
})
```

Dictionary تغییر کرده است:

```python
print(student)
```

خروجی:

```text
{'name': 'Ali', 'age': 20}
```

اما:

```python
print(result)
```

خروجی:

```text
None
```

دلیلش این است که `update()` یک عملیات **in-place** انجام می دهد؛ یعنی همان Dictionary را تغییر می دهد و Dictionary جدیدی به عنوان نتیجه برنمی گرداند.

این تفاوت در برنامه های بزرگ تر اهمیت بیشتری پیدا می کند.

---

## ۹. مقایسه انتساب مستقیم و `update()`

هر دو روش می توانند Dictionary را تغییر دهند:

```python
student["age"] = 21
```

و:

```python
student.update({
    "age": 21
})
```

برای یک Key-Value، انتساب مستقیم معمولاً ساده تر است.

اما وقتی چند مورد را هم زمان تغییر می دهیم:

```python
student.update({
    "age": 21,
    "score": 19,
    "active": True
})
```

استفاده از `update()` معمولاً خواناتر است.

بنابراین انتخاب روش به ساختار و تعداد داده هایی که قرار است تغییر کنند بستگی دارد.

---

## ۱۰. به روز رسانی Value بر اساس مقدار فعلی آن

می توانیم ابتدا Value فعلی را بخوانیم، آن را تغییر دهیم و دوباره در Dictionary قرار دهیم.

مثلاً:

```python
student = {
    "name": "Ali",
    "score": 18
}

student["score"] = student["score"] + 1
```

حالا:

```python
print(student["score"])
```

خروجی:

```text
19
```

می توان این کار را کوتاه تر نوشت:

```python
student["score"] += 1
```

همچنین:

```python
student["score"] -= 1
```

Value را یک واحد کاهش می دهد.

این الگو برای Counterها و داده هایی که به صورت تجمعی تغییر می کنند بسیار کاربردی است.

---

## ۱۱. ساخت تدریجی یک Dictionary

در بسیاری از برنامه ها Dictionary به صورت پویا ساخته می شود.

مثلاً برای شمارش:

```python
counts = {}

counts["Python"] = 1
counts["Java"] = 1
counts["Python"] += 1
```

نتیجه:

```python
{
    "Python": 2,
    "Java": 1
}
```

در اینجا ابتدا Key `"Python"` را ایجاد کردیم و سپس Value آن را به روز رسانی کردیم.

این مثال نشان می دهد که چرا درک تفاوت بین **ایجاد یک ورودی** و **تغییر یک ورودی موجود** مهم است.

---

## ۱۲. Keyهای وجود نداشته و عملیات به روز رسانی

این کد کاملاً درست است:

```python
student = {}

student["score"] = 18
```

چون انتساب به یک Key جدید باعث ایجاد آن می شود.

اما این کد:

```python
student = {}

student["score"] += 1
```

کار نمی کند.

دلیل این است که Python برای اجرای `+=` ابتدا باید مقدار فعلی `student["score"]` را بخواند، اما چنین Keyای وجود ندارد.

نتیجه:

```text
KeyError: 'score'
```

راه حل این است که ابتدا مقدار اولیه تعیین کنیم:

```python
student["score"] = 0
student["score"] += 1
```

حالا:

```python
{
    "score": 1
}
```

خواهیم داشت.

این نکته هنگام ساخت Counterها بسیار مهم است.

---

## نکات کلیدی

* Dictionaryها تغییر پذیر هستند.
* `dictionary[key] = value` در صورت نبودن Key، آیتم جدید اضافه می کند.
* همین Syntax در صورت وجود Key، Value آن را به روز رسانی می کند.
* `update()` می تواند چند آیتم را هم زمان اضافه یا به روز رسانی کند.
* `update()` می تواند Dictionary، Keyword Argument یا Iterableای از جفت های Key-Value دریافت کند.
* `update()` خود Dictionary اصلی را تغییر می دهد.
* `update()` مقدار `None` برمی گرداند.
* می توان Value را بر اساس مقدار فعلی آن به روز رسانی کرد.
* عملگرهایی مانند `+=` و `-=` برای تغییر عددی Valueها کاربرد زیادی دارند.
* قبل از استفاده از عملیاتی مانند `+=` روی یک Key، باید مقدار اولیه آن Key وجود داشته باشد.

---

# سوال های بخش

## سوال ۱

با توجه به کد زیر، یک Key جدید به نام `"score"` با مقدار `18` اضافه کنید:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

## سوال ۲

با توجه به Dictionary زیر، سن دانش آموز را به `21` و Score او را به `20` تغییر دهید:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

## سوال ۳

با استفاده از `update()` موارد زیر را انجام دهید:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

* مقدار `"age"` را به `21` تغییر دهید.
* `"score"` را با مقدار `19` اضافه کنید.
* `"active"` را با مقدار `True` اضافه کنید.

---

# سوال جامع

کد زیر را در نظر بگیرید:

```python
counts = {}

counts["Python"] = 1
counts["Java"] = 1
```

حالا فرض کنید یک مورد دیگر از Python پیدا شده است.

کدی بنویسید که Counter مربوط به `"Python"` را یک واحد افزایش دهد.

سپس توضیح دهید چرا این کد:

```python
counts["Python"] += 1
```

در این شرایط درست کار می کند، اما اگر `"Python"` از قبل اضافه نشده باشد، همین عملیات باعث خطا می شود.

---

# پاسخ ها

## پاسخ سوال ۱

```python
student["score"] = 18
```

## پاسخ سوال ۲

```python
student["age"] = 21
student["score"] = 20
```

## پاسخ سوال ۳

```python
student.update({
    "age": 21,
    "score": 19,
    "active": True
})
```

## پاسخ سوال جامع

بعد از اینکه `"Python"` مقدار اولیه گرفت:

```python
counts["Python"] += 1
```

درست کار می کند، چون Python ابتدا مقدار فعلی را دریافت می کند:

```python
counts["Python"]
```

و سپس `1` را به آن اضافه می کند.

اما اگر Key وجود نداشته باشد، Python نمی تواند مقدار فعلی آن را دریافت کند. در نتیجه:

```python
counts["Python"] += 1
```

خطای زیر را ایجاد می کند:

```text
KeyError: 'Python'
```

راه حل این است که ابتدا مقدار اولیه را تعیین کنیم:

```python
counts["Python"] = 0
counts["Python"] += 1
```

در نتیجه Dictionary به این شکل خواهد بود:

```python
{
    "Python": 1
}
```

---

# بخش ۵ — حذف آیتم های Dictionary

## مقدمه

تا اینجا یاد گرفتیم چگونه یک Dictionary بسازیم، Valueهای آن را دریافت کنیم و آیتم های جدید اضافه یا آیتم های موجود را به روز رسانی کنیم.

حالا باید یاد بگیریم چگونه **داده ها را از Dictionary حذف کنیم**.

Python چند روش مختلف برای حذف آیتم های Dictionary در اختیار ما قرار می دهد:

* `del`
* `pop()`
* `popitem()`
* `clear()`

هر کدام کاربرد متفاوتی دارند و در مقدار بازگشتی، نوع حذف و رفتار در شرایط خاص با یک دیگر تفاوت دارند.

---

## ۱. حذف یک آیتم با `del`

با `del` می توانیم یک آیتم مشخص را بر اساس Key آن حذف کنیم:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

del student["score"]
```

حالا:

```python
print(student)
```

نتیجه:

```text
{'name': 'Ali', 'age': 20}
```

ساختار کلی:

```python
del dictionary[key]
```

`del` جفت Key-Value مربوط به آن Key را مستقیماً حذف می کند.

---

## ۲. اگر Key وجود نداشته باشد چه می شود؟

فرض کنید:

```python
student = {
    "name": "Ali",
    "age": 20
}

del student["score"]
```

چون `"score"` وجود ندارد، Python خطای `KeyError` ایجاد می کند:

```text
KeyError: 'score'
```

بنابراین `del` زمانی مناسب است که بدانیم Key مورد نظر وجود دارد.

---

## ۳. حذف آیتم با `pop()`

متد `pop()` یک Key مشخص را حذف می کند و **Value آن را برمی گرداند**:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

score = student.pop("score")
```

حالا:

```python
print(score)
print(student)
```

نتیجه:

```text
18
{'name': 'Ali', 'age': 20}
```

این تفاوت بسیار مهم است:

```text
del    → آیتم را حذف می کند.
pop()  → آیتم را حذف می کند و Value آن را برمی گرداند.
```

---

## ۴. استفاده از مقدار پیش فرض در `pop()`

مانند `.get()`، متد `pop()` نیز می تواند یک مقدار پیش فرض دریافت کند:

```python
student = {
    "name": "Ali",
    "age": 20
}

score = student.pop("score", None)
```

چون `"score"` وجود ندارد، `KeyError` ایجاد نمی شود.

در عوض:

```python
print(score)
```

نتیجه:

```text
None
```

می شود.

می توانیم مقدار پیش فرض دیگری نیز تعیین کنیم:

```python
score = student.pop("score", 0)
```

در این حالت مقدار `score` برابر `0` خواهد بود.

این قابلیت زمانی مفید است که احتمال دارد Key مورد نظر وجود نداشته باشد.

---

## ۵. حذف آخرین آیتم با `popitem()`

متد `popitem()` **آخرین جفت Key-Value اضافه شده** را حذف و همان جفت را برمی گرداند:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

item = student.popitem()
```

حالا:

```python
print(item)
print(student)
```

نتیجه:

```text
('score', 18)
{'name': 'Ali', 'age': 20}
```

مقدار بازگشتی یک Tuple شامل:

```text
(Key, Value)
```

است.

بنابراین می توانیم آن را Unpack کنیم:

```python
key, value = student.popitem()
```

---

## ۶. ارتباط `popitem()` با ترتیب Dictionary

در نسخه های امروزی Python، Dictionary ترتیب اضافه شدن آیتم ها را حفظ می کند.

بنابراین `popitem()` آخرین آیتم اضافه شده را حذف می کند.

مثلاً:

```python
data = {}

data["a"] = 10
data["b"] = 20
data["c"] = 30

print(data.popitem())
```

خروجی:

```text
('c', 30)
```

سپس:

```python
print(data)
```

خروجی:

```text
{'a': 10, 'b': 20}
```

است.

---

## ۷. اگر `popitem()` روی Dictionary خالی اجرا شود

اگر Dictionary خالی باشد:

```python
data = {}

data.popitem()
```

هیچ آیتمی برای حذف وجود ندارد.

در نتیجه Python یک `KeyError` ایجاد می کند:

```text
KeyError: 'popitem(): dictionary is empty'
```

پس باید مطمئن باشیم Dictionary حداقل یک آیتم دارد یا احتمال خالی بودن آن را مدیریت کنیم.

---

## ۸. حذف تمام آیتم ها با `clear()`

اگر بخواهیم تمام آیتم های Dictionary را حذف کنیم، از `clear()` استفاده می کنیم:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

student.clear()
```

حالا:

```python
print(student)
```

خروجی:

```text
{}
```

است.

Dictionary همچنان وجود دارد، اما دیگر هیچ آیتمی داخل آن نیست.

---

## ۹. تفاوت `clear()` و `del`

نباید این دو عملیات را با یک دیگر اشتباه بگیریم.

### `clear()`

```python
student.clear()
```

تمام آیتم ها را حذف می کند، اما خود Dictionary باقی می ماند.

بعد از آن:

```python
student
```

هنوز یک Dictionary معتبر است:

```python
{}
```

### `del`

```python
del student
```

خود Variable مربوط به Dictionary را حذف می کند.

بعد از آن:

```python
print(student)
```

با `NameError` مواجه می شود.

پس:

```text
clear() → Dictionary را خالی می کند.
del      → Variable مربوط به Dictionary را حذف می کند.
```

---

## ۱۰. انتخاب روش مناسب برای حذف

چهار روش اصلی کاربردهای متفاوتی دارند:

| روش                 | چه چیزی را حذف می کند؟ | چه چیزی برمی گرداند؟   | اگر Key وجود نداشته باشد      |
| ------------------- | ---------------------- | ---------------------- | ----------------------------- |
| `del`               | یک Key-Value مشخص      | چیزی برنمی گرداند      | `KeyError`                    |
| `pop(key)`          | یک Key-Value مشخص      | Value                  | `KeyError`                    |
| `pop(key, default)` | Key مشخص در صورت وجود  | Value یا مقدار پیش فرض | خطا نمی دهد                   |
| `popitem()`         | آخرین جفت اضافه شده    | `(Key, Value)`         | در Dictionary خالی `KeyError` |
| `clear()`           | همه آیتم ها            | `None`                 | کاربرد ندارد                  |

یک مدل ذهنی مفید:

```text
del       → «این Key را حذف کن.»

pop()     → «این Key را حذف کن و Value آن را به من بده.»

popitem() → «آخرین آیتم را حذف کن و جفت Key-Value آن را بده.»

clear()   → «همه چیز را حذف کن.»
```

---

## ۱۱. حذف آیتم و نگه داشتن Value آن

یکی از مهم ترین مزیت های `pop()` این است که می توانیم آیتم را حذف کنیم و هم زمان Value آن را نگه داریم.

```python
cart = {
    "product": "Keyboard",
    "price": 50,
    "quantity": 2
}

price = cart.pop("price")

print(price)
print(cart)
```

خروجی:

```text
50
{'product': 'Keyboard', 'quantity': 2}
```

این قابلیت زمانی مفید است که بعد از حذف یک داده، هنوز بخواهیم با Value آن کار کنیم.

---

## ۱۲. استفاده از `popitem()` در Loop

چون `popitem()` در هر بار اجرا یک آیتم را حذف می کند، می توان از آن برای پردازش تدریجی Dictionary استفاده کرد:

```python
data = {
    "a": 10,
    "b": 20,
    "c": 30
}

while data:
    key, value = data.popitem()
    print(key, value)
```

خروجی:

```text
c 30
b 20
a 10
```

Dictionary در هر مرحله کوچک تر می شود تا در نهایت خالی شود.

این الگو زمانی مفید است که عمداً بخواهیم آیتم ها را پردازش و سپس حذف کنیم.

---

## ۱۳. حذف داده بدون ساخت مجدد Dictionary

یک اشتباه رایج در شروع کار این است که برای حذف یک آیتم، Dictionary جدیدی بسازیم.

مثلاً:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

student = {
    "name": student["name"],
    "age": student["age"]
}
```

در حالی که می توانیم مستقیماً بنویسیم:

```python
del student["score"]
```

روش دوم واضح تر است و دقیقاً نیت ما، یعنی حذف یک آیتم، را بیان می کند.

---

## ۱۴. تفاوت `del`، `pop()` و `clear()`

فرض کنید:

```python
data = {
    "a": 10,
    "b": 20,
    "c": 30
}
```

### حذف `"b"`

```python
del data["b"]
```

نتیجه:

```python
{'a': 10, 'c': 30}
```

### حذف `"b"` و دریافت Value آن

```python
value = data.pop("b")
```

در این حالت Value در Variable `value` ذخیره می شود.

### حذف آخرین آیتم اضافه شده

```python
item = data.popitem()
```

نتیجه یک جفت `(Key, Value)` است.

### حذف تمام آیتم ها

```python
data.clear()
```

نتیجه:

```python
{}
```

بنابراین روش مناسب به این بستگی دارد که **چه چیزی می خواهیم حذف کنیم و آیا بعد از حذف به داده حذف شده نیاز داریم یا نه**.

---

## نکات کلیدی

* `del` یک Key-Value مشخص را حذف می کند.
* `pop()` یک Key مشخص را حذف کرده و Value آن را برمی گرداند.
* `pop(key, default)` در صورت نبودن Key از `KeyError` جلوگیری می کند.
* `popitem()` آخرین جفت Key-Value اضافه شده را حذف و برمی گرداند.
* `clear()` تمام آیتم ها را حذف می کند اما خود Dictionary را نگه می دارد.
* `del dictionary` خود Dictionary Variable را حذف می کند.
* `pop()` زمانی مفید است که بعد از حذف، هنوز به Value آن نیاز داریم.
* `popitem()` می تواند برای پردازش آیتم های Dictionary به صورت تدریجی استفاده شود.
* انتخاب روش حذف باید بر اساس نوع حذف مورد نیاز و نیاز یا عدم نیاز به داده حذف شده انجام شود.

---

# سوال های بخش

## سوال ۱

با توجه به Dictionary زیر، آیتم `"score"` را با استفاده از `del` حذف کنید:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

## سوال ۲

با توجه به Dictionary زیر، `"score"` را با استفاده از `pop()` حذف کنید و Value آن را داخل یک Variable ذخیره کنید:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

## سوال ۳

تفاوت این دو عبارت چیست؟

```python
student.clear()
```

و:

```python
del student
```

---

# سوال جامع

Dictionary زیر را در نظر بگیرید:

```python
data = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

کدی بنویسید که:

1. `"score"` را حذف کند و Value آن را نگه دارد.
2. آخرین آیتم اضافه شده را حذف کند.
3. تمام آیتم های باقی مانده را حذف کند.

توضیح دهید چرا برای هر عملیات به ترتیب از `pop()`، `popitem()` و `clear()` استفاده کرده اید.

---

# پاسخ ها

## پاسخ سوال ۱

```python
del student["score"]
```

## پاسخ سوال ۲

```python
score = student.pop("score")
```

حالا مقدار `score` برابر است با:

```text
18
```

## پاسخ سوال ۳

```python
student.clear()
```

تمام آیتم ها را حذف می کند، اما خود Dictionary را نگه می دارد.

در مقابل:

```python
del student
```

خود Variable مربوط به Dictionary را حذف می کند.

## پاسخ سوال جامع

```python
data = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

score = data.pop("score")

key, value = data.popitem()

data.clear()
```

ابتدا از `pop()` استفاده کردیم، چون لازم بود Value مربوط به `"score"` را نگه داریم.

سپس از `popitem()` استفاده کردیم تا آخرین آیتم باقی مانده را حذف کرده و Key و Value آن را دریافت کنیم.

در نهایت `clear()` را به کار بردیم تا تمام آیتم های باقی مانده حذف شوند و خود Dictionary به صورت یک Dictionary خالی باقی بماند.

---

# بخش ۶ — بررسی وجود Key و Value در Dictionary

## مقدمه

Dictionary داده ها را به صورت **جفت های Key-Value** نگه داری می کند. در برنامه های واقعی، خیلی وقت ها لازم است قبل از انجام یک عملیات بررسی کنیم که یک Key یا Value خاص وجود دارد یا نه.

برای مثال ممکن است بخواهیم بدانیم:

* آیا Keyای به نام `"name"` وجود دارد؟
* آیا Keyای به نام `"score"` وجود دارد؟
* آیا Value برابر `20` در Dictionary وجود دارد؟
* اگر یک Key وجود نداشت، برنامه چه کاری باید انجام دهد؟

Python ابزارهای مختلفی برای پاسخ دادن به این سوال ها دارد.

مهم ترین آن ها عملگر `in` است.

---

## ۱. بررسی وجود یک Key

عملگر `in` بررسی می کند که آیا یک Key در Dictionary وجود دارد یا نه:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

print("name" in student)
```

خروجی:

```text
True
```

چون `"name"` یکی از Keyهای Dictionary است.

اگر Key وجود نداشته باشد:

```python
print("email" in student)
```

خروجی:

```text
False
```

خواهد بود.

الگوی کلی:

```python
key in dictionary
```

و نتیجه همیشه یک مقدار Boolean است:

```text
True
False
```

---

## ۲. چرا `in`، Keyها را بررسی می کند؟

این یک قانون مهم در Dictionary است:

```python
"name" in student
```

**Keyها** را بررسی می کند، نه Valueها را.

مثلاً:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

در این حالت:

```python
print("name" in student)
```

برابر است با:

```text
True
```

اما:

```python
print("Ali" in student)
```

برابر است با:

```text
False
```

با اینکه `"Ali"` داخل Dictionary وجود دارد، اما `"Ali"` یک Value است، نه یک Key.

این رفتار با List متفاوت است؛ در List، `in` عناصر خود List را بررسی می کند.

---

## ۳. بررسی نبودن یک Key با `not in`

اگر بخواهیم بررسی کنیم که یک Key **وجود ندارد**، می توانیم از `not in` استفاده کنیم:

```python
if "email" not in student:
    print("Email is not available.")
```

این روش هنگام اضافه کردن اطلاعات نیز کاربردی است:

```python
if "email" not in student:
    student["email"] = "ali@example.com"
```

در این حالت فقط زمانی `"email"` اضافه می شود که از قبل وجود نداشته باشد.

این الگو می تواند از تغییر ناخواسته یک Value موجود جلوگیری کند.

---

## ۴. استفاده از بررسی وجود Key در شرط

بررسی وجود Key وقتی با `if` ترکیب شود، بسیار کاربردی می شود:

```python
student = {
    "name": "Ali",
    "age": 20
}

if "age" in student:
    print("Age exists.")
```

خروجی:

```text
Age exists.
```

همچنین می توانیم حالت دیگر را نیز مدیریت کنیم:

```python
if "email" in student:
    print("Email exists.")
else:
    print("Email does not exist.")
```

در این حالت برنامه بر اساس ساختار Dictionary تصمیم می گیرد.

---

## ۵. بررسی وجود یک Value

همان طور که گفتیم، `in` وقتی مستقیماً روی Dictionary استفاده شود، Keyها را بررسی می کند.

اگر بخواهیم Valueها را بررسی کنیم، باید از متد `values()` استفاده کنیم:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

print(20 in student.values())
```

خروجی:

```text
True
```

چون `20` یکی از Valueهای Dictionary است.

برای Valueای که وجود ندارد:

```python
print(25 in student.values())
```

خروجی:

```text
False
```

بنابراین تفاوت مهم این است:

```python
key in dictionary
```

Keyها را بررسی می کند.

اما:

```python
value in dictionary.values()
```

Valueها را بررسی می کند.

---

## ۶. بررسی هم زمان Key و Value

فرض کنید:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

برای بررسی Key:

```python
print("name" in student)
```

و برای بررسی Value:

```python
print("Ali" in student.values())
```

استفاده می کنیم.

این دو عملیات سوال های متفاوتی را پاسخ می دهند.

یک روش ساده برای به خاطر سپردن:

```text
dictionary
    ↓
Keys   →  key in dictionary
Values →  value in dictionary.values()
```

---

## ۷. استفاده از `values()` برای بررسی عضویت

متد `values()` یک View از Valueهای Dictionary در اختیارمان قرار می دهد:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

values = student.values()

print(values)
```

مقدار `values` یک Dictionary Values View خواهد بود.

مهم تر از نحوه نمایش آن این است که می توانیم مستقیماً از آن برای بررسی وجود Value استفاده کنیم:

```python
print(18 in student.values())
```

خروجی:

```text
True
```

لازم نیست فقط برای بررسی وجود یک Value، آن را به List تبدیل کنیم.

مثلاً این کار معمولاً غیر ضروری است:

```python
print(18 in list(student.values()))
```

شکل مستقیم و واضح تر این است:

```python
print(18 in student.values())
```

---

## ۸. استفاده از `get()` وقتی Value را لازم داریم

گاهی فقط نمی خواهیم بدانیم یک Key وجود دارد یا نه.

بلکه واقعاً Value مربوط به آن Key را لازم داریم.

در چنین شرایطی `get()` کاربرد زیادی دارد:

```python
student = {
    "name": "Ali",
    "age": 20
}

age = student.get("age")

print(age)
```

خروجی:

```text
20
```

اگر Key وجود نداشته باشد:

```python
email = student.get("email")
print(email)
```

نتیجه:

```text
None
```

خواهد بود.

در حالی که استفاده مستقیم از:

```python
student["email"]
```

باعث ایجاد خطای:

```text
KeyError: 'email'
```

می شود.

بنابراین `get()` زمانی بسیار مناسب است که ممکن است Key وجود نداشته باشد و بخواهیم بدون ایجاد Exception این حالت را مدیریت کنیم.

---

## ۹. تعیین مقدار پیش فرض در `get()`

می توانیم برای `get()` یک مقدار پیش فرض نیز مشخص کنیم:

```python
email = student.get("email", "Not provided")
```

حالا:

```python
print(email)
```

خروجی:

```text
Not provided
```

است.

ساختار کلی:

```python
dictionary.get(key, default)
```

این قابلیت زمانی کاربردی است که برنامه برای نبودن Key یک مقدار جایگزین نیاز دارد.

مثلاً:

```python
score = student.get("score", 0)
```

اگر `"score"` وجود داشته باشد، Value آن برگردانده می شود.

اگر وجود نداشته باشد، `0` برگردانده می شود.

---

## ۱۰. تفاوت `in` و `get()`

این دو عملیات سوال های متفاوتی را پاسخ می دهند.

### `in`

زمانی از `in` استفاده می کنیم که سوال اصلی این باشد:

> آیا این Key وجود دارد؟

```python
if "score" in student:
    print("Score exists.")
```

### `get()`

زمانی از `get()` استفاده می کنیم که سوال اصلی این باشد:

> Value مربوط به این Key چیست و اگر Key وجود نداشت، چه مقداری استفاده کنیم؟

```python
score = student.get("score", 0)
```

این تفاوت باعث می شود کد هدف خود را واضح تر بیان کند.

---

## ۱۱. تفاوت `in` و دسترسی مستقیم

فرض کنید:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

این کد ایمن است:

```python
if "email" in student:
    print(student["email"])
```

چون فقط بعد از اطمینان از وجود Key، به Value آن دسترسی پیدا می کنیم.

اما:

```python
print(student["email"])
```

مستقیماً تلاش می کند به یک Key موجود نباشد دسترسی پیدا کند و در نتیجه:

```text
KeyError: 'email'
```

ایجاد می شود.

بنابراین می توان از بررسی عضویت به عنوان یک Guard قبل از دسترسی به Keyهای احتمالی استفاده کرد.

---

## ۱۲. یک الگوی رایج: بررسی قبل از به روز رسانی

فرض کنید می خواهیم Score را فقط زمانی تغییر دهیم که Key آن از قبل وجود داشته باشد:

```python
if "score" in student:
    student["score"] = 20
```

اگر `"score"` وجود نداشته باشد، عملیات به روز رسانی انجام نمی شود.

حالت دیگر این است که بخواهیم اگر Key وجود نداشت، آن را ایجاد کنیم:

```python
if "score" not in student:
    student["score"] = 0
```

و بعد:

```python
student["score"] += 1
```

این الگو برای Counterها و داده هایی که به صورت تدریجی ساخته می شوند بسیار کاربردی است.

---

## ۱۳. بررسی Value قبل از انجام عملیات

می توانیم وجود یک Value را نیز بررسی کنیم:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

if 18 in student.values():
    print("A score of 18 exists.")
```

خروجی:

```text
A score of 18 exists.
```

اما باید توجه کنیم که Valueها الزاماً Unique نیستند.

مثلاً:

```python
data = {
    "first": 10,
    "second": 10
}
```

در این حالت:

```python
10 in data.values()
```

برابر با `True` است، اما مقدار `10` به دو Key مختلف مربوط است.

---

## ۱۴. Key و Value مفاهیم متفاوتی هستند

فرض کنید:

```python
data = {
    "name": "Ali",
    "city": "Tehran"
}
```

Key `"name"` و Value `"Ali"` قابل جایگزینی با یک دیگر نیستند.

بنابراین:

```python
"name" in data
```

نتیجه:

```text
True
```

اما:

```python
"Ali" in data
```

نتیجه:

```text
False
```

است.

برای جست و جوی `"Ali"` در Valueها باید بنویسیم:

```python
"Ali" in data.values()
```

که نتیجه آن:

```text
True
```

خواهد بود.

این تفاوت در زمان کار با Dictionaryهای پیچیده اهمیت بیشتری پیدا می کند.

---

## ۱۵. مثال کاربردی: اطلاعات کاربر

فرض کنید:

```python
user = {
    "username": "ali123",
    "age": 22,
    "country": "Iran"
}
```

می توانیم بررسی کنیم که اطلاعات کشور وجود دارد:

```python
if "country" in user:
    print("Country information exists.")
```

می توانیم آن را به صورت ایمن دریافت کنیم:

```python
country = user.get("country", "Unknown")
```

و می توانیم بررسی کنیم که کشور `"Iran"` به عنوان یک Value در Dictionary وجود دارد:

```python
if "Iran" in user.values():
    print("Iran is stored as a Value.")
```

هر یک از این عملیات یک سوال متفاوت را پاسخ می دهد.

---

## ۱۶. مثال کاربردی: بررسی Keyهای ضروری

فرض کنید برنامه ما انتظار دارد یک Dictionary شامل اطلاعات مشخصی باشد:

```python
user = {
    "username": "ali123",
    "email": "ali@example.com",
    "age": 22
}
```

می توانیم بررسی کنیم که Keyهای ضروری وجود دارند:

```python
required_keys = ["username", "email", "age"]

for key in required_keys:
    if key not in user:
        print(f"Missing key: {key}")
```

اگر همه Keyهای ضروری وجود داشته باشند، چیزی چاپ نمی شود.

این الگو برای **اعتبار سنجی داده های ساخت یافته** قبل از پردازش آن ها بسیار کاربردی است.

---

## ۱۷. نگاه دقیق تر به عملکرد

در Dictionaryهای معمول Python، بررسی وجود یک Key با `in` برای Lookup بسیار بهینه طراحی شده است.

بنابراین روش استاندارد برای بررسی یک Key این است:

```python
if "username" in user:
    ...
```

معمولاً نباید برای جست و جوی یک Key، ابتدا Keyها را به List تبدیل کنیم:

```python
if "username" in list(user.keys()):
    ...
```

این تبدیل کار اضافی ایجاد می کند و هدف کد را نیز کمتر واضح می کند.

روش بهتر:

```python
if "username" in user:
    ...
```

برای Valueها وضعیت متفاوت است. بررسی:

```python
value in dictionary.values()
```

باید Valueها را تا پیدا شدن نتیجه بررسی کند؛ بنابراین از نظر هدف و ویژگی عملکردی با بررسی Key متفاوت است.

---

## نکات کلیدی

* `in` بررسی می کند که یک Key در Dictionary وجود دارد یا نه.
* `not in` بررسی می کند که یک Key وجود ندارد.
* استفاده مستقیم از `in` روی Dictionary، Valueها را جست و جو نمی کند.
* برای جست و جوی Valueها از `dictionary.values()` استفاده می کنیم.
* `get()` زمانی کاربردی است که Value یک Key را لازم داریم و ممکن است Key وجود نداشته باشد.
* `get(key, default)` یک مقدار جایگزین برای Keyهای موجود نباشد فراهم می کند.
* `in` می تواند قبل از دسترسی به Key احتمالی به عنوان Guard استفاده شود.
* بررسی وجود Key و بررسی وجود Value دو سوال متفاوت هستند.
* برای بررسی معمول Key نیازی به تبدیل `dictionary.keys()` به List نیست.
* بررسی عضویت در Dictionary برای اعتبار سنجی، منطق شرطی و به روز رسانی ایمن داده ها بسیار مهم است.

---

# سوال های بخش

## سوال ۱

Dictionary زیر را در نظر بگیرید:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

کدی بنویسید که بررسی کند آیا Key `"score"` وجود دارد یا نه.

## سوال ۲

با استفاده از همین Dictionary، کدی بنویسید که بررسی کند آیا Value برابر `20` وجود دارد یا نه.

## سوال ۳

با استفاده از `get()` مقدار مربوط به Key `"email"` را دریافت کنید و اگر Key وجود نداشت، مقدار `"Not provided"` را برگردانید.

---

# سوال جامع

Dictionary زیر را در نظر بگیرید:

```python
user = {
    "username": "ali123",
    "age": 22
}
```

کدی بنویسید که:

1. بررسی کند آیا `"email"` وجود دارد یا نه.
2. اگر وجود نداشت، آن را با استفاده از `get()` و مقدار پیش فرض `"Not provided"` دریافت کند.
3. بررسی کند آیا Value برابر `22` در Dictionary وجود دارد یا نه.
4. توضیح دهید چرا `"email" in user` و `"Not provided" in user` دو سوال کاملاً متفاوت را بررسی می کنند.

---

# پاسخ ها

## پاسخ سوال ۱

```python
"score" in student
```

یا:

```python
if "score" in student:
    print("Score exists.")
```

## پاسخ سوال ۲

```python
20 in student.values()
```

## پاسخ سوال ۳

```python
email = student.get("email", "Not provided")
```

## پاسخ سوال جامع

```python
user = {
    "username": "ali123",
    "age": 22
}

if "email" in user:
    print("Email exists.")

email = user.get("email", "Not provided")

if 22 in user.values():
    print("Age value exists.")
```

عبارت:

```python
"email" in user
```

بررسی می کند که `"email"` به عنوان یک **Key** وجود دارد یا نه.

اما:

```python
"Not provided" in user
```

نیز Keyها را بررسی می کند، نه Valueها؛ چون `in` وقتی مستقیماً روی Dictionary استفاده شود، Keyها را جست و جو می کند.

برای جست و جوی Valueها باید بنویسیم:

```python
"Not provided" in user.values()
```

این تفاوت یکی از مفاهیم پایه ای و مهم در کار با Dictionary است.

---

