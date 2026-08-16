# 🟢 سطح ۱ — مقدماتی (Beginner)

> 🌐 زبان: **فارسی** | [English](../README.md)

به سطح **مقدماتی** از نقشه راه پایتون خوش آمدید.

این سطح برای افرادی طراحی شده است که تجربه کمی در برنامه‌نویسی دارند یا می‌خواهند یادگیری پایتون را از صفر آغاز کنند.

در این بخش، پایه‌های اصلی زبان برنامه‌نویسی پایتون را یاد می‌گیرید و قدم‌به‌قدم با مفاهیمی آشنا می‌شوید که برای نوشتن برنامه‌های واقعی به آن‌ها نیاز خواهید داشت.

اگر در سطح قبلی، **تفکر الگوریتمی و حل مسئله** را یاد گرفته باشید، اکنون زمان آن رسیده است که آن مهارت‌ها را با استفاده از زبان پایتون به کد تبدیل کنید.

---

# 📚 در این سطح چه چیزهایی یاد می‌گیرید؟

در این سطح با موضوعات زیر آشنا خواهید شد:

- مبانی پایتون
- متغیرها
- انواع داده
- ورودی و خروجی
- عملگرها
- شرط‌ها
- حلقه‌ها
- توابع
- رشته‌ها
- لیست‌ها
- تاپل‌ها
- مجموعه‌ها
- دیکشنری‌ها

هر درس بر پایه درس قبل طراحی شده است؛ بنابراین توصیه می‌شود آن‌ها را به ترتیب مطالعه کنید.

---

# 🎯 اهداف یادگیری

پس از پایان این سطح، قادر خواهید بود:

- سینتکس پایه پایتون را درک کنید.
- برنامه‌های ساده با پایتون بنویسید.
- با استفاده از شرط‌ها تصمیم‌گیری کنید.
- با حلقه‌ها کارهای تکراری را انجام دهید.
- کدهای خود را با توابع سازمان‌دهی کنید.
- از ساختمان‌داده‌های داخلی پایتون استفاده کنید.
- کدهای ساده پایتون را بخوانید و درک کنید.
- مسائل پایه برنامه‌نویسی را با اطمینان حل کنید.

---

# 📋 پیش‌نیازها

پیش از شروع این سطح، پیشنهاد می‌شود ابتدا:

- ✅ سطح ۰ — حل مسئله

را به پایان رسانده باشید.

اگرچه می‌توانید مستقیماً این سطح را آغاز کنید، اما گذراندن سطح حل مسئله، یادگیری پایتون را بسیار ساده‌تر خواهد کرد.

---

# 🗂️ درس‌ها

| # | درس | وضعیت |
|---|------|--------|
| 1 | مبانی پایتون | ⏳ |
| 2 | متغیرها و انواع داده | ⏳ |
| 3 | ورودی و خروجی | ⏳ |
| 4 | عملگرها | ⏳ |
| 5 | شرط‌ها | ⏳ |
| 6 | حلقه‌ها | ⏳ |
| 7 | توابع | ⏳ |
| 8 | رشته‌ها | ⏳ |
| 9 | لیست‌ها | ⏳ |
| 10 | تاپل‌ها | ⏳ |
| 11 | مجموعه‌ها | ⏳ |
| 12 | دیکشنری‌ها | ⏳ |

---

# 💡 روش مطالعه

برای یادگیری بهتر:

- هر بار فقط یک درس را مطالعه کنید.
- توضیحات را با دقت بخوانید.
- تمام مثال‌های کد را خودتان اجرا کنید.
- همه تمرین‌ها را حل کنید.
- آزمون‌های پایان درس را از دست ندهید.
- به‌صورت منظم تمرین کنید.

برنامه‌نویسی یک مهارت عملی است.

هرچه بیشتر تمرین کنید، سریع‌تر پیشرفت خواهید کرد.

---

# 📈 میزان پیشرفت

وضعیت فعلی:

```text
□□□□□□□□□□□□
0%
```

درس‌های تکمیل‌شده:

**0 / 12**

---

# 🚀 مرحله بعد چیست؟

پس از پایان این سطح وارد:

> 🟡 **سطح ۲ — متوسط (Intermediate)**

خواهید شد.

در آنجا با مفاهیم پیشرفته‌تر پایتون آشنا می‌شوید، مهارت‌های برنامه‌نویسی خود را تقویت می‌کنید و پروژه‌های کاربردی‌تری خواهید ساخت.

---

موفق باشید و از مسیر یادگیری لذت ببرید! 🐍

---

# پارت ۹ — Key و Value در Dictionary

## مقدمه

Dictionary داده ها را به صورت **جفت های Key-Value** ذخیره می کند.

درک عمیق تفاوت بین Key و Value بسیار مهم است، چون تقریباً تمام کارهایی که با Dictionary انجام می دهیم بر اساس همین رابطه شکل می گیرند.

مثلاً:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

در این Dictionary:

* `"name"`، `"age"` و `"score"`، **Key** هستند.
* `"Ali"`، `20` و `18`، **Value** هستند.

می توانیم ساختار را این طور ببینیم:

```text
Key       → Value
"name"    → "Ali"
"age"     → 20
"score"   → 18
```

Key داده را **مشخص می کند** و Value داده ای است که به آن Key مربوط است.

---

## ۱. Key در Dictionary چیست؟

Key شناسه ای است که برای دسترسی به یک Value استفاده می شود.

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

در اینجا `"name"` یک Key و `"Ali"` Value مربوط به آن است.

بنابراین Key به Python می گوید:

> کدام Value را می خواهیم دریافت کنیم؟

---

## ۲. Value در Dictionary چیست؟

Value داده ای است که تحت یک Key ذخیره شده است.

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

Valueهای این Dictionary عبارت اند از:

```text
Ali
20
18
```

Valueها می توانند از نوع های مختلف باشند:

```python
data = {
    "name": "Ali",
    "age": 20,
    "active": True
}
```

در اینجا:

* `"Ali"` یک String است.
* `20` یک Integer است.
* `True` یک Boolean است.

لازم نیست تمام Valueهای یک Dictionary از یک نوع باشند.

---

## ۳. دسترسی به Value با استفاده از Key

رایج ترین رابطه بین Key و Value این است:

```python
dictionary[key]
```

مثلاً:

```python
student = {
    "name": "Ali",
    "age": 20
}

print(student["age"])
```

خروجی:

```text
20
```

ما Key را مشخص می کنیم و Python Value مربوط به آن را برمی گرداند.

---

## ۴. Keyها باید منحصر به فرد باشند

Keyهای Dictionary باید منحصر به فرد باشند.

مثلاً:

```python
student = {
    "name": "Ali",
    "age": 20
}
```

فقط یک Key به نام `"name"` داریم.

اگر یک Key را دوباره تعریف کنیم:

```python
student = {
    "name": "Ali",
    "name": "Sara"
}
```

Python دو ورودی جداگانه با Key یکسان نگه نمی دارد.

مقدار بعدی جای مقدار قبلی را می گیرد.

در نتیجه Dictionary به شکل زیر خواهد بود:

```python
{
    "name": "Sara"
}
```

پس یک قانون مهم داریم:

> **یک Dictionary نمی تواند دو ورودی مستقل با Key یکسان داشته باشد.**

---

## ۵. Valueها می توانند تکراری باشند

بر خلاف Keyها، Valueها لازم نیست منحصر به فرد باشند.

```python
scores = {
    "Ali": 18,
    "Sara": 18,
    "Reza": 15
}
```

در اینجا دو Key متفاوت، Value یکسان `18` دارند:

```text
Ali  → 18
Sara → 18
```

این کاملاً معتبر است.

پس:

```text
Keyها   → منحصر به فرد
Valueها → می توانند تکراری باشند
```

این تفاوت هنگام جستجو در Dictionary اهمیت زیادی پیدا می کند.

---

## ۶. دریافت تمام Keyها با `keys()`

Python متد `keys()` را در اختیار ما قرار می دهد:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

print(student.keys())
```

این متد یک View از Keyهای Dictionary در اختیار ما قرار می دهد.

می توانیم روی آن پیمایش کنیم:

```python
for key in student.keys():
    print(key)
```

خروجی:

```text
name
age
score
```

وقتی خود Keyها برای ما مهم هستند، `keys()` ابزار مناسبی است.

---

## ۷. دریافت تمام Valueها با `values()`

متد `values()` برای دسترسی به Valueها استفاده می شود:

```python
for value in student.values():
    print(value)
```

خروجی:

```text
Ali
20
18
```

این روش زمانی مناسب است که Keyها برای عملی که می خواهیم انجام دهیم اهمیتی نداشته باشند.

---

## ۸. دریافت Key و Value با هم با `items()`

اگر هم Key و هم Value را لازم داشته باشیم، از `items()` استفاده می کنیم:

```python
for key, value in student.items():
    print(key, value)
```

خروجی:

```text
name Ali
age 20
score 18
```

از نظر مفهومی، هر مرحله از پیمایش یک جفت به شکل زیر در اختیار ما قرار می دهد:

```text
(Key, Value)
```

مثلاً:

```text
"name" → "Ali"
"age" → 20
"score" → 18
```

این یکی از مهم ترین الگوهای کار با Dictionary است.

---

## ۹. بررسی وجود یک Key

عملگر `in` در حالت مستقیم روی Dictionary، وجود Key را بررسی می کند:

```python
student = {
    "name": "Ali",
    "age": 20
}

print("name" in student)
print("score" in student)
```

خروجی:

```text
True
False
```

چون `"name"` وجود دارد، اما `"score"` Key موجودی نیست.

---

## ۱۰. بررسی وجود یک Value

اگر بخواهیم Valueها را جستجو کنیم، از `values()` استفاده می کنیم:

```python
student = {
    "name": "Ali",
    "age": 20
}

print(20 in student.values())
```

خروجی:

```text
True
```

این دو عبارت را با هم مقایسه کنید:

```python
"age" in student
```

و:

```python
20 in student.values()
```

اولی یک **Key** را بررسی می کند.

دومی یک **Value** را بررسی می کند.

این تفاوت یکی از نکات پایه و بسیار مهم Dictionary است.

---

## ۱۱. نقش متفاوت Key و Value

Dictionary زیر را در نظر بگیرید:

```python
products = {
    "apple": 10,
    "banana": 5,
    "orange": 8
}
```

در اینجا Keyها نام محصولات هستند:

```text
apple
banana
orange
```

و Valueها تعداد موجودی هستند:

```text
10
5
8
```

اما می توانیم Dictionary مشابهی برای قیمت ها داشته باشیم:

```python
prices = {
    "apple": 2,
    "banana": 1,
    "orange": 3
}
```

ساختار Dictionary تغییری نکرده است؛ فقط معنای Valueها تغییر کرده است.

این موضوع یک مفهوم مهم در برنامه نویسی را نشان می دهد:

> **Dictionary ساختار داده را فراهم می کند؛ این برنامه نویس است که مشخص می کند Key و Value چه معنایی داشته باشند.**

---

## ۱۲. انتخاب Keyهای معنادار

بهتر است Keyها به شکلی انتخاب شوند که داده ای را که مشخص می کنند، واضح نشان دهند.

مثلاً:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

خواناتر از این است:

```python
student = {
    "a": "Ali",
    "b": 20,
    "c": 18
}
```

هر دو از نظر فنی می توانند کار کنند، اما Keyهای معنادار باعث می شوند کد راحت تر خوانده و نگهداری شود.

یک Key خوب باید تا حد امکان درباره Value مربوط به خودش اطلاعات بدهد.

---

## ۱۳. تفاوت Lookup و Search

بین **پیدا کردن Value با استفاده از Key** و **جستجوی یک Value** تفاوت مهمی وجود دارد.

### Lookup

```python
student["age"]
```

ما Key را از قبل می دانیم و Value مربوط به آن را می خواهیم.

به صورت مفهومی:

```text
Key → Value
```

### جستجوی Value

```python
20 in student.values()
```

ما Value را می دانیم و می خواهیم بررسی کنیم که آیا وجود دارد یا نه.

به صورت مفهومی:

```text
Value → آیا وجود دارد؟
```

این دو عملیات نباید با یکدیگر اشتباه گرفته شوند.

---

## ۱۴. پیدا کردن Key بر اساس Value

فرض کنید:

```python
scores = {
    "Ali": 18,
    "Sara": 15,
    "Reza": 18
}
```

می خواهیم تمام دانش آموزانی را پیدا کنیم که نمره `18` دارند.

می توانیم جفت های Key-Value را بررسی کنیم:

```python
for name, score in scores.items():
    if score == 18:
        print(name)
```

خروجی:

```text
Ali
Reza
```

دقت کنید که یک Value می تواند با چند Key مرتبط باشد.

این دقیقاً به دلیل منحصر به فرد نبودن Valueهاست.

---

## ۱۵. Valueها می توانند ساختارهای داده متفاوتی باشند

Value یک Dictionary فقط محدود به String، Integer یا Boolean نیست.

مثلاً:

```python
student = {
    "name": "Ali",
    "age": 20,
    "skills": ["Python", "HTML"],
    "active": True
}
```

در اینجا:

* `"name"` → String
* `"age"` → Integer
* `"skills"` → List
* `"active"` → Boolean

می توانیم از طریق Key به List دسترسی پیدا کنیم:

```python
print(student["skills"])
```

خروجی:

```text
['Python', 'HTML']
```

از آنجا که Value دریافت شده یک List است، می توانیم بعد از دریافت آن با قواعد List کار کنیم:

```python
print(student["skills"][0])
```

خروجی:

```text
Python
```

Dictionary مشخص می کند **کدام Value** را دریافت کنیم؛ سپس نوع خود Value مشخص می کند که بعد از آن چه کارهایی می توانیم انجام دهیم.

---

## ۱۶. Key بخشی از مدل داده است

Key صرفاً یک برچسب برای نمایش اطلاعات نیست.

Key در منطق برنامه نقش عملی دارد.

مثلاً:

```python
user = {
    "username": "ali123",
    "email": "ali@example.com"
}
```

می توانیم بنویسیم:

```python
user["email"]
```

تا ایمیل را دریافت کنیم.

بنابراین `"email"` بخشی از نحوه سازمان دهی و دسترسی به اطلاعات کاربر در برنامه است.

انتخاب Key مناسب باعث می شود کدهای بعدی بسیار واضح تر باشند.

---

## ۱۷. مثال کاربردی

یک موجودی ساده فروشگاه را در نظر بگیرید:

```python
inventory = {
    "apple": 10,
    "banana": 5,
    "orange": 8
}
```

اگر نام محصول را بدانیم، می توانیم مستقیماً تعداد آن را دریافت کنیم:

```python
print(inventory["apple"])
```

خروجی:

```text
10
```

اگر بخواهیم تمام محصولات را ببینیم:

```python
for product in inventory.keys():
    print(product)
```

اگر فقط تعداد موجودی ها را بخواهیم:

```python
for quantity in inventory.values():
    print(quantity)
```

و اگر هر دو را بخواهیم:

```python
for product, quantity in inventory.items():
    print(f"{product}: {quantity}")
```

خروجی:

```text
apple: 10
banana: 5
orange: 8
```

این سه روش، پایه ای ترین روش های کار با دو بخش اصلی Dictionary هستند.

---

## ۱۸. مدل ذهنی کامل

می توانیم Dictionary را مجموعه ای از رابطه ها در نظر بگیریم:

```text
             Dictionary
                 │
        ┌────────┴────────┐
        ↓                 ↓
       Key              Value
        │                 │
   مشخص کننده داده     نگهدارنده داده
        │                 │
        └───────┬─────────┘
                ↓
          Key → Value
```

مثلاً:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

یعنی:

```text
"name"  → "Ali"
"age"   → 20
"score" → 18
```

وقتی این رابطه به خوبی درک شود، متدهای `keys()`، `values()` و `items()` نیز بسیار ساده تر خواهند شد.

---

## نکات کلیدی

* Dictionary از **جفت های Key-Value** تشکیل شده است.
* Key یک بخش از داده را مشخص می کند.
* Value داده مربوط به آن Key است.
* Keyها باید منحصر به فرد باشند.
* Valueها می توانند تکراری باشند.
* `keys()` برای دسترسی به Keyها استفاده می شود.
* `values()` برای دسترسی به Valueها استفاده می شود.
* `items()` جفت های Key-Value را در اختیار ما قرار می دهد.
* استفاده مستقیم از `in` روی Dictionary، Keyها را بررسی می کند.
* `in dictionary.values()` برای بررسی Valueها استفاده می شود.
* Keyهای معنادار باعث خوانایی بیشتر برنامه می شوند.
* Valueها می توانند از نوع های مختلفی مانند List باشند.
* Lookup کردن یک Value با Key با جستجوی یک Value متفاوت است.
* برای پیدا کردن Keyها بر اساس Value معمولاً باید جفت های Key-Value را بررسی کنیم.

---

# سوال های بخش

## سوال ۱

تمام Keyها و تمام Valueهای Dictionary زیر را مشخص کنید:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

## سوال ۲

تفاوت این دو عبارت چیست؟

```python
"age" in student
```

و:

```python
20 in student.values()
```

## سوال ۳

Dictionary نهایی حاصل از کد زیر چه خواهد بود؟

```python
student = {
    "name": "Ali",
    "name": "Sara"
}
```

---

# سوال جامع

Dictionary زیر را در نظر بگیرید:

```python
students = {
    "Ali": 18,
    "Sara": 15,
    "Reza": 18,
    "Mina": 12
}
```

برنامه ای بنویسید که:

1. تمام Keyها را چاپ کند.
2. تمام Valueها را چاپ کند.
3. تمام جفت های Key-Value را چاپ کند.
4. بررسی کند که Value برابر `18` وجود دارد یا نه.
5. تمام Keyهایی را پیدا و چاپ کند که Value آن ها `18` است.

---

# پاسخ ها

## پاسخ سوال ۱

Keyها:

```text
name
age
score
```

Valueها:

```text
Ali
20
18
```

## پاسخ سوال ۲

```python
"age" in student
```

بررسی می کند که `"age"` به عنوان یک **Key** وجود دارد یا نه.

در مقابل:

```python
20 in student.values()
```

بررسی می کند که `20` به عنوان یک **Value** وجود دارد یا نه.

## پاسخ سوال ۳

Key تکراری دوم، مقدار قبلی را جایگزین می کند:

```python
{
    "name": "Sara"
}
```

## پاسخ سوال جامع

```python
students = {
    "Ali": 18,
    "Sara": 15,
    "Reza": 18,
    "Mina": 12
}

for key in students.keys():
    print(key)

for value in students.values():
    print(value)

for key, value in students.items():
    print(f"{key}: {value}")

if 18 in students.values():
    print("18 exists.")

for key, value in students.items():
    if value == 18:
        print(key)
```

خروجی بخش جستجوی نهایی:

```text
Ali
Reza
```

---

# پارت ۱۰ — Dictionary Items

## مقدمه

در پارت قبل یاد گرفتیم که Dictionary از **جفت های Key و Value** تشکیل می شود.

مثلاً:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

هر ورودی شامل دو بخش مرتبط است:

```text
"name"  → "Ali"
"age"   → 20
"score" → 18
```

گاهی فقط به Keyها نیاز داریم.

گاهی فقط Valueها برای ما مهم هستند.

اما در بسیاری از مواقع لازم است **Key و Value مربوط به آن را با هم** داشته باشیم.

اینجاست که متد `items()` اهمیت پیدا می کند.

---

## ۱. `items()` چه کاری انجام می دهد؟

متد `items()` امکان دسترسی به تمام **جفت های Key و Value** یک Dictionary را فراهم می کند.

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

print(student.items())
```

نتیجه، ورودی های Dictionary را به صورت جفت نمایش می دهد:

```text
("name", "Ali")
("age", 20)
("score", 18)
```

از نظر مفهومی:

```text
Dictionary
    ↓
items()
    ↓
(Key, Value)
(Key, Value)
(Key, Value)
```

بنابراین هدف اصلی `items()` این است:

> **این که بتوانیم با هر Key و Value مربوط به آن، هم زمان کار کنیم.**

---

## ۲. `items()` جفت ها را در اختیار ما قرار می دهد

هر عنصر حاصل از `items()` نشان دهنده یک ورودی کامل Dictionary است.

```python
student = {
    "name": "Ali",
    "age": 20
}

for item in student.items():
    print(item)
```

خروجی:

```text
('name', 'Ali')
('age', 20)
```

هر `item` یک ورودی کامل Dictionary را نشان می دهد.

این موضوع با:

```python
student.keys()
```

که Keyها را در اختیار ما قرار می دهد و:

```python
student.values()
```

که Valueها را در اختیار ما قرار می دهد، متفاوت است.

می توانیم این سه متد را این طور به خاطر بسپاریم:

```text
keys()   → Keyها
values() → Valueها
items()  → Key + Value
```

---

## ۳. پیمایش Dictionary با `items()`

رایج ترین استفاده از `items()` همراه با حلقه `for` است.

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}

for item in student.items():
    print(item)
```

خروجی:

```text
('name', 'Ali')
('age', 20)
('score', 18)
```

به این ترتیب تمام ورودی های Dictionary یکی یکی پردازش می شوند.

حلقه کل Dictionary را یک جا پردازش نمی کند؛ بلکه هر جفت Key-Value را به صورت جداگانه در اختیار ما قرار می دهد.

---

## ۴. باز کردن جفت Key و Value

Python اجازه می دهد هر جفت را مستقیماً داخل دو متغیر قرار دهیم:

```python
for key, value in student.items():
    print(key, value)
```

خروجی:

```text
name Ali
age 20
score 18
```

در اینجا:

```text
key   → Key
value → Value
```

در اولین مرحله:

```text
key   = "name"
value = "Ali"
```

در مرحله دوم:

```text
key   = "age"
value = 20
```

و به همین شکل ادامه پیدا می کند.

این الگو یکی از مهم ترین الگوهایی است که هنگام کار با Dictionary باید به آن مسلط شویم:

```python
for key, value in dictionary.items():
    ...
```

---

## ۵. چرا `items()` کاربردی است؟

فرض کنید می خواهیم نام هر دانش آموز را همراه با نمره او چاپ کنیم:

```python
scores = {
    "Ali": 18,
    "Sara": 15,
    "Reza": 19
}
```

ما هم به Key و هم به Value نیاز داریم:

```text
Student → Score
```

پس می توانیم بنویسیم:

```python
for name, score in scores.items():
    print(name, score)
```

خروجی:

```text
Ali 18
Sara 15
Reza 19
```

استفاده از `items()` رابطه بین دو بخش داده را به صورت مستقیم در اختیار ما قرار می دهد.

---

## ۶. استفاده از `items()` برای خروجی خوانا

می توانیم `items()` را با f-string ترکیب کنیم:

```python
scores = {
    "Ali": 18,
    "Sara": 15,
    "Reza": 19
}

for name, score in scores.items():
    print(f"{name}: {score}")
```

خروجی:

```text
Ali: 18
Sara: 15
Reza: 19
```

این روش برای نمایش خواناتر اطلاعات Dictionary بسیار کاربردی است.

---

## ۷. استفاده از `items()` همراه با شرط

از آنجا که هم Key و هم Value را داریم، می توانیم بر اساس Value تصمیم گیری کنیم.

مثلاً:

```python
scores = {
    "Ali": 18,
    "Sara": 12,
    "Reza": 19,
    "Mina": 10
}

for name, score in scores.items():
    if score >= 15:
        print(name)
```

خروجی:

```text
Ali
Reza
```

در اینجا Value تعیین کننده شرط است:

```python
score >= 15
```

و Key چاپ می شود.

این الگو برای پردازش داده های ساختار یافته بسیار مهم است.

---

## ۸. استفاده هم زمان از Key و Value در شرط

می توانیم از هر دو بخش در یک شرط استفاده کنیم:

```python
students = {
    "Ali": 18,
    "Sara": 12,
    "Reza": 19
}

for name, score in students.items():
    if name == "Ali" and score >= 15:
        print(f"{name} passed.")
```

خروجی:

```text
Ali passed.
```

نکته مهم این است که `items()` هر دو بخش اطلاعات را هم زمان در اختیار ما قرار می دهد.

بنابراین شرط می تواند فقط به Key، فقط به Value، یا به هر دو وابسته باشد.

---

## ۹. تفاوت `items()` با `keys()` و `values()`

Dictionary زیر را در نظر بگیرید:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

### `keys()`

```python
for key in student.keys():
    print(key)
```

خروجی:

```text
name
age
score
```

### `values()`

```python
for value in student.values():
    print(value)
```

خروجی:

```text
Ali
20
18
```

### `items()`

```python
for key, value in student.items():
    print(key, value)
```

خروجی:

```text
name Ali
age 20
score 18
```

مدل ذهنی:

```text
keys()   → چه چیزی داده را مشخص می کند؟

values() → چه داده ای ذخیره شده است؟

items()  → کدام داده به کدام شناسه مربوط است؟
```

---

## ۱۰. Dictionary به عنوان مجموعه ای از رابطه ها

یکی از مهم ترین مفاهیم `items()` این است که Dictionary فقط مجموعه ای از Valueهای جدا از هم نیست.

Dictionary **رابطه بین داده ها** را نشان می دهد.

مثلاً:

```python
prices = {
    "apple": 2,
    "banana": 1,
    "orange": 3
}
```

اطلاعات مهم فقط این ها نیستند:

```text
2
1
3
```

بلکه رابطه کامل این است:

```text
apple  → 2
banana → 1
orange → 3
```

`items()` اجازه می دهد همین رابطه ها را مستقیماً پردازش کنیم.

این مفهوم زمانی که Dictionaryهای پیچیده تر می سازیم اهمیت بیشتری پیدا می کند.

---

## ۱۱. تغییر Value هنگام پیمایش

می توانیم از Key دریافت شده از `items()` برای تغییر Dictionary استفاده کنیم.

مثلاً:

```python
scores = {
    "Ali": 10,
    "Sara": 12,
    "Reza": 15
}

for name, score in scores.items():
    scores[name] = score + 1

print(scores)
```

نتیجه:

```text
{'Ali': 11, 'Sara': 13, 'Reza': 16}
```

در اینجا:

```python
scores[name]
```

از Key برای دسترسی به ورودی مربوطه استفاده می کند.

سپس Value جدید جای Value قبلی قرار می گیرد.

رابطه را می توان این طور دید:

```text
Key
 ↓
ورودی Dictionary
 ↓
Value
```

---

## ۱۲. ساخت یک Dictionary جدید با استفاده از `items()`

می توانیم با استفاده از `items()` یک Dictionary جدید نیز بسازیم.

مثلاً:

```python
prices = {
    "apple": 2,
    "banana": 1,
    "orange": 3
}

expensive = {}

for product, price in prices.items():
    if price >= 2:
        expensive[product] = price
```

Dictionary جدید:

```python
{
    "apple": 2,
    "orange": 3
}
```

در اینجا اگر شرط برقرار باشد، Key و Value مربوط به آن با هم به Dictionary جدید منتقل می شوند.

---

## ۱۳. Valueهای مختلف با `items()`

Value الزاماً یک عدد یا String ساده نیست.

مثلاً:

```python
users = {
    "Ali": 20,
    "Sara": 25,
    "Reza": 22
}
```

می توانیم بنویسیم:

```python
for name, age in users.items():
    print(f"{name} is {age} years old.")
```

اما Value می تواند یک List نیز باشد:

```python
skills = {
    "Ali": ["Python", "HTML"],
    "Sara": ["CSS", "JavaScript"]
}
```

باز هم می توانیم از `items()` استفاده کنیم:

```python
for name, user_skills in skills.items():
    print(name, user_skills)
```

خروجی:

```text
Ali ['Python', 'HTML']
Sara ['CSS', 'JavaScript']
```

رابطه Key-Value تغییری نکرده است، حتی اگر خود Value پیچیده تر شده باشد.

---

## ۱۴. پردازش تو در تو

از آنجا که Value می تواند یک ساختار داده دیگر باشد، می توانیم `items()` را با عملیات دیگری ترکیب کنیم.

مثلاً:

```python
skills = {
    "Ali": ["Python", "HTML"],
    "Sara": ["CSS", "JavaScript"]
}

for name, user_skills in skills.items():
    print(name)

    for skill in user_skills:
        print(skill)
```

خروجی:

```text
Ali
Python
HTML
Sara
CSS
JavaScript
```

حلقه بیرونی با جفت های Key-Value Dictionary کار می کند.

حلقه داخلی با List ذخیره شده در Value کار می کند.

این مثال نشان می دهد که چگونه چند ساختار داده می توانند در کنار یکدیگر استفاده شوند.

---

## ۱۵. جستجوی داده با `items()`

فرض کنید می خواهیم افرادی را پیدا کنیم که نمره مشخصی دارند:

```python
scores = {
    "Ali": 18,
    "Sara": 15,
    "Reza": 18,
    "Mina": 12
}

for name, score in scores.items():
    if score == 18:
        print(name)
```

خروجی:

```text
Ali
Reza
```

Key به ما می گوید **چه کسی** این نمره را دارد.

Value به ما می گوید **نمره چیست**.

داشتن هر دو بخش در این نوع جستجو بسیار مهم است.

---

## ۱۶. نام متغیرها

نام های `key` و `value` کلمات رزرو شده Python نیستند.

مثلاً این کد:

```python
for key, value in student.items():
    print(key, value)
```

به این دلیل کار می کند که ما خودمان این نام ها را برای متغیرها انتخاب کرده ایم.

حتی این هم از نظر Python معتبر است:

```python
for x, y in student.items():
    print(x, y)
```

اما:

```python
for key, value in student.items():
```

خواناتر است، چون نام متغیرها نقش داده را مشخص می کنند.

نام گذاری مناسب باعث می شود کد Dictionary بسیار راحت تر خوانده شود.

---

## ۱۷. یک اشتباه رایج در شروع کار

یکی از اشتباهات رایج این است:

```python
for key, value in student:
    print(key, value)
```

این روش برای دریافت هم زمان Key و Value الگوی درستی نیست.

الگوی درست:

```python
for key, value in student.items():
    print(key, value)
```

چرا؟

چون وقتی مستقیماً روی Dictionary پیمایش می کنیم، به صورت معمول Keyها را پیمایش می کنیم.

اگر مشخصاً Key-Value pairها را بخواهیم، باید از:

```python
student.items()
```

استفاده کنیم.

---

## ۱۸. یک اشتباه رایج دیگر

ممکن است ترتیب Key و Value را اشتباه بگیریم:

```python
for value, key in student.items():
    print(key, value)
```

Python از نظر فنی دو مقدار را در دو متغیر قرار می دهد، اما نقش متغیرها برعکس شده است.

اگر جفت این باشد:

```text
"name", "Ali"
```

آنگاه:

```text
value = "name"
key   = "Ali"
```

این از نظر منطقی گمراه کننده است.

الگوی واضح تر این است:

```python
for key, value in student.items():
    ...
```

نام متغیرها باید با نقش داده هماهنگ باشند.

---

## ۱۹. مثال کاربردی: موجودی فروشگاه

فرض کنید:

```python
inventory = {
    "apple": 10,
    "banana": 5,
    "orange": 8
}
```

می توانیم موجودی را نمایش دهیم:

```python
for product, quantity in inventory.items():
    print(f"{product}: {quantity}")
```

می توانیم محصولاتی را که موجودی کمی دارند پیدا کنیم:

```python
for product, quantity in inventory.items():
    if quantity < 7:
        print(product)
```

خروجی:

```text
banana
```

همچنین می توانیم مقدار موجودی را تغییر دهیم:

```python
for product, quantity in inventory.items():
    inventory[product] = quantity + 2
```

در این حالت به موجودی تمام محصولات دو واحد اضافه می شود.

همان رابطه Key-Value به ما اجازه می دهد داده را بخوانیم، بررسی کنیم و تغییر دهیم.

---

## ۲۰. مدل ذهنی کامل

بهترین مدل ذهنی برای `items()` این است:

```text
Dictionary
    │
    ├── Key 1 → Value 1
    ├── Key 2 → Value 2
    └── Key 3 → Value 3
             │
           items()
             │
             ↓
      (Key, Value)
```

وقتی می نویسیم:

```python
for key, value in dictionary.items():
```

در واقع به Python می گوییم:

> «هر رابطه موجود در Dictionary را یکی یکی در اختیار من قرار بده تا بتوانم با هر دو طرف آن رابطه کار کنم.»

به همین دلیل `items()` یکی از مهم ترین ابزارها برای پردازش Dictionary است.

---

## نکات کلیدی

* `items()` امکان دسترسی به جفت های Key-Value را فراهم می کند.
* هر Item یک جفت `(Key, Value)` است.
* رایج ترین الگو این است:

```python
for key, value in dictionary.items():
```

* `keys()` فقط Keyها را در اختیار ما قرار می دهد.
* `values()` فقط Valueها را در اختیار ما قرار می دهد.
* `items()` هر دو را با هم در اختیار ما قرار می دهد.
* `items()` برای نمایش، مقایسه، جستجو، فیلتر و پردازش هم زمان Key و Value بسیار کاربردی است.
* Key می تواند برای دسترسی یا تغییر Value مربوط به خودش استفاده شود.
* Value می تواند ساختارهای پیچیده ای مانند List داشته باشد.
* نام گذاری مناسب متغیرهایی مانند `key` و `value` خوانایی کد را افزایش می دهد.
* پیمایش مستقیم Dictionary با پیمایش `dictionary.items()` یکسان نیست.

---

# سوال های بخش

## سوال ۱

متد `items()` چه چیزی را از یک Dictionary در اختیار ما قرار می دهد؟

## سوال ۲

تفاوت این دو حلقه چیست؟

```python
for key in student:
    print(key)
```

و:

```python
for key, value in student.items():
    print(key, value)
```

## سوال ۳

کد زیر چه چیزی چاپ می کند؟

```python
scores = {
    "Ali": 18,
    "Sara": 12,
    "Reza": 19
}

for name, score in scores.items():
    if score >= 18:
        print(name)
```

---

# سوال جامع

Dictionary زیر را در نظر بگیرید:

```python
inventory = {
    "apple": 10,
    "banana": 5,
    "orange": 8,
    "milk": 3
}
```

با استفاده از `items()` برنامه ای بنویسید که:

1. هر محصول و تعداد موجودی آن را چاپ کند.
2. محصولاتی را که تعداد موجودی آن ها کمتر از `6` است چاپ کند.
3. به تعداد موجودی تمام محصولات `2` واحد اضافه کند.
4. Dictionary به روز شده را چاپ کند.

---

# پاسخ ها

## پاسخ سوال ۱

`items()` جفت Key و Value مربوط به هر ورودی Dictionary را در اختیار ما قرار می دهد.

مثلاً:

```text
("name", "Ali")
("age", 20)
```

## پاسخ سوال ۲

حلقه اول روی Keyهای Dictionary پیمایش می کند:

```python
for key in student:
    print(key)
```

حلقه دوم به صورت مشخص روی جفت های Key-Value پیمایش می کند:

```python
for key, value in student.items():
    print(key, value)
```

## پاسخ سوال ۳

خروجی:

```text
Ali
Reza
```

چون نمره هر دو نفر حداقل `18` است.

## پاسخ سوال جامع

```python
inventory = {
    "apple": 10,
    "banana": 5,
    "orange": 8,
    "milk": 3
}

for product, quantity in inventory.items():
    print(f"{product}: {quantity}")

for product, quantity in inventory.items():
    if quantity < 6:
        print(product)

for product, quantity in inventory.items():
    inventory[product] = quantity + 2

print(inventory)
```

بعد از به روز رسانی:

```text
apple  → 12
banana → 7
orange → 10
milk   → 5
```

---

