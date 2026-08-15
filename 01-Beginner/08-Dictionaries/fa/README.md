# بخش ۱ — مقدمه ای بر Dictionaryها

> 🌐 Language: **فارسی** | [English](../README.md)

---

| بخش | موضوع                                   |
| --: | --------------------------------------- |
|   ۱ | مقدمه ای بر Dictionaryها                |
|   ۲ | ساخت Dictionary                         |
|   ۳ | دسترسی به Valueهای Dictionary           |
|   ۴ | اضافه کردن و به روز رسانی عناصر         |
|   ۵ | حذف عناصر                               |
|   ۶ | بررسی وجود Key                          |
|   ۷ | طول Dictionary                          |
|   ۸ | پیمایش Dictionaryها                     |
|   ۹ | Keyها و Valueهای Dictionary             |
|  ۱۰ | جفت های Key-Value                       |
|  ۱۱ | Dictionaryهای تو در تو                  |
|  ۱۲ | کپی کردن Dictionary                     |
|  ۱۳ | تبدیل Dictionary به ساختارهای داده دیگر |
|  ۱۴ | مرور نهایی Dictionaryها                 |
|  ۱۵ | پروژه کوچک Dictionaryها                 |

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

