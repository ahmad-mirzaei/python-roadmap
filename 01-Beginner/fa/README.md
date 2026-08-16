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

# پارت ۱۱ — Nested Dictionaries

## مقدمه

تا اینجا با Dictionaryهایی کار کردیم که Valueهای آن ها معمولاً داده های ساده بودند:

```python
student = {
    "name": "Ali",
    "age": 20,
    "score": 18
}
```

اما داده های واقعی معمولاً ساختار پیچیده تری دارند.

برای مثال اطلاعات یک دانش آموز ممکن است شامل موارد زیر باشد:

* اطلاعات شخصی
* اطلاعات تحصیلی
* اطلاعات تماس
* چندین نمره
* فهرستی از مهارت ها

اگر همه این اطلاعات را در یک Dictionary ساده قرار دهیم، با زیاد شدن داده ها ساختار خیلی سریع شلوغ می شود.

Python با اجازه دادن به قرار گرفتن یک Dictionary به عنوان Value یک Dictionary دیگر، امکان ساخت ساختارهای منظم تر را فراهم می کند.

به چنین ساختاری **Nested Dictionary** یا **Dictionary تو در تو** می گوییم.

---

## ۱. Nested Dictionary چیست؟

Nested Dictionary دیکشنری ای است که یکی از Valueهای آن خودش یک Dictionary دیگر است.

مثلاً:

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20,
        "city": "Baku"
    }
}
```

ساختار:

```text
student
│
├── name   → "Ali"
│
└── details
      │
      ├── age  → 20
      └── city → "Baku"
```

Dictionary بیرونی دارای Key به نام `"details"` است.

Value مربوط به `"details"` خودش یک Dictionary است.

آن Dictionary داخلی نیز Keyها و Valueهای خودش را دارد.

---

## ۲. چرا به Nested Dictionaries نیاز داریم؟

Nested Dictionary به ما اجازه می دهد **داده های سلسله مراتبی** را نمایش دهیم.

به جای این:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku",
    "math": 18,
    "python": 20
}
```

می توانیم داده ها را بر اساس ارتباطشان گروه بندی کنیم:

```python
student = {
    "name": "Ali",
    "personal": {
        "age": 20,
        "city": "Baku"
    },
    "scores": {
        "math": 18,
        "python": 20
    }
}
```

حالا خود ساختار مشخص می کند هر داده متعلق به چه بخشی است:

```text
student
│
├── name
├── personal
│    ├── age
│    └── city
│
└── scores
     ├── math
     └── python
```

این نوع سازمان دهی زمانی که با داده های بزرگ تر کار می کنیم اهمیت بسیار بیشتری پیدا می کند.

---

## ۳. دسترسی به Value داخل Dictionary تو در تو

برای دسترسی به داده داخل Dictionary داخلی، باید چند Key را پشت سر هم استفاده کنیم.

مثلاً:

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20,
        "city": "Baku"
    }
}
```

برای دسترسی به سن:

```python
print(student["details"]["age"])
```

خروجی:

```text
20
```

این دسترسی به صورت مفهومی چنین اتفاقی می افتد:

```text
student
   ↓
["details"]
   ↓
Dictionary داخلی
   ↓
["age"]
   ↓
20
```

این یکی از مهم ترین الگوها در کار با داده های تو در تو است.

---

## ۴. دسترسی به سطوح مختلف

فرض کنید:

```python
student = {
    "name": "Ali",
    "personal": {
        "age": 20,
        "address": {
            "city": "Baku",
            "country": "Azerbaijan"
        }
    }
}
```

می توانیم بنویسیم:

```python
student["name"]
```

که نتیجه آن:

```text
Ali
```

است.

یا:

```python
student["personal"]["age"]
```

که نتیجه:

```text
20
```

است.

و حتی عمیق تر:

```python
student["personal"]["address"]["city"]
```

که نتیجه:

```text
Baku
```

است.

هر Key اضافی ما را یک سطح بیشتر در ساختار وارد می کند.

---

## ۵. Nested Dictionary می تواند چندین سطح داشته باشد

محدودیتی وجود ندارد که Nested Dictionary فقط یک سطح عمق داشته باشد.

مثلاً:

```python
company = {
    "employee": {
        "contact": {
            "address": {
                "city": "Baku"
            }
        }
    }
}
```

می توانیم شهر را این گونه دریافت کنیم:

```python
print(
    company["employee"]["contact"]["address"]["city"]
)
```

خروجی:

```text
Baku
```

البته Python اجازه چنین ساختاری را می دهد، اما این به معنی آن نیست که همیشه باید Dictionaryها را بسیار عمیق کنیم.

اگر عمق بیش از حد زیاد شود، خواندن و نگهداری کد دشوار می شود.

پس Nested کردن باید زمانی انجام شود که واقعاً باعث واضح تر شدن ساختار داده شود.

---

## ۶. تغییر یک Value داخلی

Valueهای داخل Dictionaryهای تو در تو نیز قابل تغییر هستند.

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20,
        "city": "Baku"
    }
}

student["details"]["age"] = 21
```

حالا:

```python
print(student["details"]["age"])
```

نتیجه:

```text
21
```

اصل کار همان Assignment معمولی Dictionary است.

فقط قبل از رسیدن به Value باید مسیر داخل ساختار را مشخص کنیم.

---

## ۷. اضافه کردن Value به Dictionary داخلی

می توانیم یک ورودی جدید نیز به Dictionary داخلی اضافه کنیم:

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20,
        "city": "Baku"
    }
}

student["details"]["country"] = "Azerbaijan"
```

حالا Dictionary داخلی:

```python
{
    "age": 20,
    "city": "Baku",
    "country": "Azerbaijan"
}
```

است.

در واقع ما به جای Dictionary بیرونی، Dictionary ذخیره شده در `"details"` را تغییر داده ایم.

---

## ۸. اضافه کردن یک Dictionary تو در توی جدید

می توانیم یک بخش کاملاً جدید نیز ایجاد کنیم:

```python
student = {
    "name": "Ali"
}

student["scores"] = {
    "math": 18,
    "python": 20
}
```

حالا ساختار چنین چیزی است:

```text
name
   → Ali

scores
   → math   → 18
   → python → 20
```

این قابلیت برای زمانی که ساختار داده در طول اجرای برنامه رشد می کند بسیار کاربردی است.

---

## ۹. حذف داده های تو در تو

می توانیم یک ورودی را از Dictionary داخلی حذف کنیم:

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20,
        "city": "Baku"
    }
}

del student["details"]["city"]
```

در این حالت `"city"` از Dictionary داخلی حذف می شود.

همچنین می توانیم کل Dictionary داخلی را حذف کنیم:

```python
del student["details"]
```

در این حالت Key `"details"` و Dictionary مربوط به آن از Dictionary بیرونی حذف می شوند.

---

## ۱۰. استفاده از `items()` در Nested Dictionaries

متد `items()` که در پارت قبل یاد گرفتیم، برای Nested Dictionary نیز کاربرد دارد.

مثلاً:

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20,
        "city": "Baku"
    }
}

for key, value in student.items():
    print(key, value)
```

خروجی:

```text
name Ali
details {'age': 20, 'city': 'Baku'}
```

یک نکته مهم وجود دارد:

حلقه بیرونی کل Dictionary داخلی را به عنوان **یک Value** می بیند.

خودش به صورت خودکار وارد Dictionary داخلی نمی شود.

---

## ۱۱. پیمایش Dictionary داخلی

اگر بخواهیم Dictionary داخلی را پردازش کنیم، باید مشخصاً وارد آن شویم:

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20,
        "city": "Baku"
    }
}

for key, value in student["details"].items():
    print(key, value)
```

خروجی:

```text
age 20
city Baku
```

اینجا به Python گفته ایم:

> «Dictionary ذخیره شده در `details` را بگیر و روی Itemهای آن پیمایش کن.»

---

## ۱۲. حلقه های `for` تو در تو

برای چند Dictionary تو در تو می توانیم از چند حلقه استفاده کنیم.

```python
students = {
    "student1": {
        "name": "Ali",
        "score": 18
    },
    "student2": {
        "name": "Sara",
        "score": 15
    }
}

for student_id, student_info in students.items():
    print(student_id)

    for key, value in student_info.items():
        print(key, value)
```

خروجی:

```text
student1
name Ali
score 18
student2
name Sara
score 15
```

حلقه بیرونی هر دانش آموز را پردازش می کند.

حلقه داخلی اطلاعات مربوط به همان دانش آموز را پردازش می کند.

---

## ۱۳. یک ساختار واقعی تر

Nested Dictionaries زمانی که چند موجودیت مشابه داریم، بسیار مفید می شوند.

مثلاً:

```python
students = {
    "ali": {
        "age": 20,
        "city": "Baku",
        "scores": {
            "math": 18,
            "python": 20
        }
    },
    "sara": {
        "age": 19,
        "city": "Ganja",
        "scores": {
            "math": 17,
            "python": 19
        }
    }
}
```

ساختار:

```text
students
│
├── ali
│    ├── age
│    ├── city
│    └── scores
│         ├── math
│         └── python
│
└── sara
     ├── age
     ├── city
     └── scores
          ├── math
          └── python
```

حالا هر دانش آموز مجموعه اطلاعات ساختاریافته خودش را دارد.

---

## ۱۴. دسترسی به داده عمیقاً تو در تو

با ساختار بالا:

```python
print(students["ali"]["scores"]["python"])
```

خروجی:

```text
20
```

مسیر دسترسی:

```text
students
   ↓
ali
   ↓
scores
   ↓
python
   ↓
20
```

درک این مسیر از حفظ کردن Syntax مهم تر است.

هر زمان چیزی شبیه این دیدید:

```python
data["a"]["b"]["c"]
```

باید آن را ذهنی این گونه بخوانید:

> وارد `a` شو، سپس وارد `b` شو، سپس `c` را دریافت کن.

---

## ۱۵. تغییر داده عمیقاً تو در تو

می توانیم یک Value در سطح عمیق تر را نیز تغییر دهیم:

```python
students["ali"]["scores"]["python"] = 21
```

حالا:

```python
print(students["ali"]["scores"]["python"])
```

نتیجه:

```text
21
```

اصل Assignment همان است.

تنها تفاوت این است که برای رسیدن به Value باید از چند سطح عبور کنیم.

---

## ۱۶. بررسی وجود Key در سطوح مختلف

عملگر `in` را می توان در هر سطح از Dictionary استفاده کرد.

مثلاً:

```python
if "ali" in students:
    print("Ali exists.")
```

می توانیم Dictionary داخلی را بررسی کنیم:

```python
if "scores" in students["ali"]:
    print("Scores exist.")
```

و حتی سطح عمیق تر:

```python
if "python" in students["ali"]["scores"]:
    print("Python score exists.")
```

نکته مهم این است که `in` در همان Dictionaryای که روی آن اعمال شده، وجود Key را بررسی می کند.

---

## ۱۷. جلوگیری از `KeyError`

دسترسی تو در تو در صورتی که یکی از Keyهای مسیر وجود نداشته باشد، می تواند باعث خطا شود.

مثلاً:

```python
print(students["ali"]["grades"]["python"])
```

اگر `"grades"` وجود نداشته باشد، Python خطای:

```text
KeyError
```

ایجاد می کند.

در داده های تو در تو تمام مراحل مسیر باید معتبر باشند:

```text
students
  ↓
"ali"       باید وجود داشته باشد
  ↓
"grades"    باید وجود داشته باشد
  ↓
"python"    باید وجود داشته باشد
```

به همین دلیل قبل از دسترسی به داده های عمیق، باید ساختار داده را به خوبی بشناسیم.

---

## ۱۸. استفاده از `get()` در Nested Dictionaries

گاهی می توانیم برای دسترسی امن تر از `get()` استفاده کنیم.

مثلاً:

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20
    }
}

details = student.get("details", {})
age = details.get("age")
```

اگر `"details"` وجود نداشته باشد، مقدار `details` به جای ایجاد فوری `KeyError` برابر یک Dictionary خالی می شود.

این روش زمانی مفید است که بعضی قسمت های داده ممکن است وجود نداشته باشند.

البته `get()` به صورت خودکار تمام سطوح را امن نمی کند؛ هنوز باید ساختار داده را به شکل صحیح مدیریت کنیم.

---

## ۱۹. Nested Dictionaries و سازمان دهی داده

یکی از مهم ترین مزیت های Nested Dictionary، **سازمان دهی اطلاعات** است.

این ساختار را ببینید:

```python
data = {
    "name": "Ali",
    "age": 20,
    "city": "Baku",
    "math_score": 18,
    "python_score": 20
}
```

در مقابل:

```python
data = {
    "name": "Ali",
    "personal": {
        "age": 20,
        "city": "Baku"
    },
    "scores": {
        "math": 18,
        "python": 20
    }
}
```

ساختار دوم رابطه بین داده ها را بسیار واضح تر می کند.

اگر اطلاعات بیشتری اضافه کنیم:

```python
data = {
    "name": "Ali",
    "personal": {
        "age": 20,
        "city": "Baku"
    },
    "scores": {
        "math": 18,
        "python": 20
    },
    "contact": {
        "email": "ali@example.com"
    }
}
```

هر دسته اطلاعات جای مشخص خودش را دارد.

---

## ۲۰. Nested Dictionary یک نوع داده جدید نیست

Nested Dictionary یک Data Type خاص و جداگانه در Python نیست.

این فقط یک Dictionary معمولی است که یکی از Valueهای آن یک Dictionary دیگر است.

مثلاً:

```python
data = {
    "person": {
        "name": "Ali"
    }
}
```

Dictionary بیرونی یک Dictionary است.

Dictionary داخلی نیز یک Dictionary است.

این نکته مهم است، چون تمام عملیات معمول Dictionary روی Dictionary داخلی نیز قابل استفاده هستند.

---

## ۲۱. ترکیب Nested Dictionary با List

داده های تو در تو فقط شامل Dictionary نیستند.

می توانیم Dictionary و List را با هم ترکیب کنیم:

```python
student = {
    "name": "Ali",
    "skills": [
        "Python",
        "HTML",
        "CSS"
    ],
    "scores": {
        "math": 18,
        "python": 20
    }
}
```

ساختار:

```text
student
│
├── name   → String
├── skills → List
└── scores → Dictionary
```

می توانیم به List دسترسی داشته باشیم:

```python
print(student["skills"][0])
```

خروجی:

```text
Python
```

و به Dictionary داخلی:

```python
print(student["scores"]["python"])
```

خروجی:

```text
20
```

این مثال نشان می دهد که ساختارهای داده Python می توانند در کنار یکدیگر برای مدل کردن داده های پیچیده تر استفاده شوند.

---

## ۲۲. مثال کاربردی: کاتالوگ محصولات

یک فروشگاه آنلاین را در نظر بگیرید:

```python
products = {
    "laptop": {
        "price": 1200,
        "stock": 5,
        "brand": "Lenovo"
    },
    "phone": {
        "price": 800,
        "stock": 10,
        "brand": "Samsung"
    }
}
```

قیمت لپ تاپ:

```python
print(products["laptop"]["price"])
```

خروجی:

```text
1200
```

موجودی:

```python
print(products["laptop"]["stock"])
```

و تغییر آن:

```python
products["laptop"]["stock"] = 4
```

این یک نمونه واقعی از استفاده Nested Dictionary برای نمایش یک موجودیت ساختاریافته است.

---

## ۲۳. پردازش چند محصول

می توانیم تمام محصولات را پردازش کنیم:

```python
for product_name, product_info in products.items():
    print(product_name)

    for key, value in product_info.items():
        print(f"{key}: {value}")
```

خروجی:

```text
laptop
price: 1200
stock: 5
brand: Lenovo

phone
price: 800
stock: 10
brand: Samsung
```

الگوی مهم اینجا:

```python
for outer_key, inner_dictionary in data.items():
    for inner_key, value in inner_dictionary.items():
        ...
```

است.

این الگو اجازه می دهد چند سطح از داده های Dictionary را پردازش کنیم.

---

## ۲۴. مدل ذهنی مهم

وقتی با Nested Dictionary کار می کنیم، بهتر است ساختار را یک تکه بزرگ از Syntax نبینیم.

آن را مثل یک **درخت** تصور کنیم.

مثلاً:

```text
products
│
├── laptop
│    ├── price
│    ├── stock
│    └── brand
│
└── phone
     ├── price
     ├── stock
     └── brand
```

پس:

```python
products["laptop"]["price"]
```

فقط یک مسیر در این درخت است:

```text
products
   ↓
laptop
   ↓
price
   ↓
1200
```

وقتی این مدل ذهنی برایمان طبیعی شود، Nested Dictionaries بسیار ساده تر خواهند شد.

---

## نکات کلیدی

* Nested Dictionary یعنی Dictionaryای که یکی از Valueهای آن یک Dictionary دیگر است.
* برای نمایش داده های سلسله مراتبی و ساختاریافته بسیار مفید است.
* برای دسترسی به داده های تو در تو از چند Key پشت سر هم استفاده می کنیم.
* می توان Valueها را در هر سطح تغییر داد یا Value جدید اضافه کرد.
* `items()` با Dictionaryهای داخلی نیز قابل استفاده است.
* برای پیمایش چند سطح می توان از حلقه های `for` تو در تو استفاده کرد.
* `in` در سطح مشخصی که روی آن اجرا می شود، وجود Key را بررسی می کند.
* نبودن یکی از Keyهای مسیر می تواند باعث `KeyError` شود.
* `get()` در شرایطی که بعضی داده ها ممکن است وجود نداشته باشند، می تواند مفید باشد.
* Dictionary می تواند با List و سایر ساختارهای داده ترکیب شود.
* Nested Dictionary یک Data Type جدید نیست؛ همچنان از Dictionaryهای معمولی ساخته شده است.
* بهترین مدل ذهنی برای ساختارهای پیچیده، تصور کردن آن ها به شکل یک درخت از رابطه هاست.

---

# سوال های بخش

## سوال ۱

چه چیزی باعث می شود یک Dictionary به Nested Dictionary تبدیل شود؟

## سوال ۲

کد زیر چه چیزی چاپ می کند؟

```python
student = {
    "name": "Ali",
    "details": {
        "age": 20,
        "city": "Baku"
    }
}

print(student["details"]["city"])
```

## سوال ۳

چگونه سن Ali را به `21` تغییر می دهید؟

## سوال ۴

چرا ممکن است Nested Dictionary نسبت به قرار دادن تمام اطلاعات در یک Dictionary ساده انتخاب بهتری باشد؟

---

# سوال جامع

Dictionary زیر را در نظر بگیرید:

```python
students = {
    "ali": {
        "age": 20,
        "scores": {
            "math": 18,
            "python": 20
        }
    },
    "sara": {
        "age": 19,
        "scores": {
            "math": 17,
            "python": 19
        }
    }
}
```

برنامه ای بنویسید که:

1. نام هر دانش آموز را چاپ کند.
2. سن او را چاپ کند.
3. نمره Python او را چاپ کند.
4. دانش آموزانی را که نمره Python آن ها حداقل `20` است چاپ کند.
5. نمره Python مربوط به Ali را به `21` تغییر دهد.

---

# پاسخ ها

## پاسخ سوال ۱

زمانی که یکی از Valueهای Dictionary خودش یک Dictionary باشد، با Nested Dictionary روبه رو هستیم.

مثلاً:

```python
data = {
    "person": {
        "name": "Ali"
    }
}
```

Value مربوط به `"person"` خودش یک Dictionary است.

## پاسخ سوال ۲

```text
Baku
```

زیرا:

```python
student["details"]
```

Dictionary داخلی را دریافت می کند و:

```python
["city"]
```

Value مربوط به `"city"` را دریافت می کند.

## پاسخ سوال ۳

```python
student["details"]["age"] = 21
```

## پاسخ سوال ۴

Nested Dictionary اطلاعات مرتبط را در گروه های منطقی سازمان دهی می کند و رابطه سلسله مراتبی بین داده ها را واضح تر نشان می دهد.

به جای اینکه همه چیز در یک سطح قرار بگیرد:

```text
age
city
math_score
python_score
```

می توانیم ساختار را این گونه سازمان دهی کنیم:

```text
personal
    age
    city

scores
    math
    python
```

هرچه داده ها پیچیده تر شوند، این نوع سازمان دهی ارزش بیشتری پیدا می کند.

## پاسخ سوال جامع

```python
students = {
    "ali": {
        "age": 20,
        "scores": {
            "math": 18,
            "python": 20
        }
    },
    "sara": {
        "age": 19,
        "scores": {
            "math": 17,
            "python": 19
        }
    }
}

for name, info in students.items():
    print(name)
    print(f"Age: {info['age']}")
    print(f"Python: {info['scores']['python']}")

for name, info in students.items():
    if info["scores"]["python"] >= 20:
        print(name)

students["ali"]["scores"]["python"] = 21
```

---

# پارت ۱۲ — Copying Dictionaries

## مقدمه

یکی از مهم ترین مفاهیم هنگام کار با Dictionary این است که تفاوت بین **Assignment** و **Copy کردن Dictionary** را به خوبی درک کنیم.

در نگاه اول ممکن است این دو کد شبیه به هم به نظر برسند:

```python
first = {"name": "Ali", "age": 20}

second = first
```

و:

```python
first = {"name": "Ali", "age": 20}

second = first.copy()
```

اما این دو یک رابطه کاملاً متفاوت ایجاد می کنند.

این تفاوت زمانی اهمیت زیادی پیدا می کند که بخواهیم داده ها را تغییر دهیم.

---

## ۱. Assignment باعث ساخت Copy نمی شود

فرض کنید:

```python
student = {
    "name": "Ali",
    "age": 20
}

another_student = student
```

ممکن است تصور کنیم حالا دو Dictionary داریم.

اما `another_student` یک Copy مستقل نیست.

هر دو متغیر به **همان Object** اشاره می کنند.

از نظر مفهومی:

```text
student ─────────┐
                 ↓
          ┌──────────────┐
          │  Dictionary  │
          │ name → Ali   │
          │ age  → 20    │
          └──────────────┘
                 ↑
another_student ─┘
```

فقط یک Dictionary وجود دارد.

دو نام به همان Object اشاره می کنند.

---

## ۲. تغییر یک متغیر روی دیگری هم اثر می گذارد

مثلاً:

```python
student = {
    "name": "Ali",
    "age": 20
}

another_student = student

another_student["age"] = 21

print(student)
```

خروجی:

```text
{'name': 'Ali', 'age': 21}
```

ما `another_student` را تغییر دادیم، اما `student` نیز تغییر کرد.

دلیل آن این است که Dictionary جدیدی ساخته نشده بود.

هر دو متغیر به یک Object اشاره می کردند.

---

## ۳. مفهوم Object Identity

Python با عملگر `is` به ما اجازه می دهد بررسی کنیم آیا دو متغیر به یک Object یکسان اشاره می کنند یا نه.

```python
student = {
    "name": "Ali"
}

another_student = student

print(student is another_student)
```

خروجی:

```text
True
```

یعنی هر دو متغیر دقیقاً به یک Object اشاره دارند.

این موضوع با بررسی برابر بودن داده ها متفاوت است.

---

## ۴. تفاوت `==` و `is`

فرض کنید:

```python
first = {"name": "Ali"}
second = {"name": "Ali"}
```

این دو Dictionary داده یکسانی دارند.

بنابراین:

```python
print(first == second)
```

نتیجه:

```text
True
```

اما:

```python
print(first is second)
```

نتیجه:

```text
False
```

تفاوت اصلی:

```text
==  → آیا مقدارهای دو Object برابر هستند؟

is  → آیا دقیقاً همان Object هستند؟
```

این تفاوت هنگام کار با Objectهای Mutable مثل Dictionary و List بسیار مهم است.

---

## ۵. ساخت Dictionary مستقل با `copy()`

اگر بخواهیم یک Dictionary جداگانه ایجاد کنیم، می توانیم از `copy()` استفاده کنیم:

```python
student = {
    "name": "Ali",
    "age": 20
}

another_student = student.copy()
```

حالا دو Object جدا داریم:

```text
student
   ↓
Dictionary A

another_student
   ↓
Dictionary B
```

محتوای آن ها در ابتدا یکسان است، اما خود Objectها جدا هستند.

---

## ۶. تغییر Dictionary کپی شده

حالا:

```python
student = {
    "name": "Ali",
    "age": 20
}

another_student = student.copy()

another_student["age"] = 21
```

اگر هر دو را چاپ کنیم:

```python
print(student)
print(another_student)
```

خروجی:

```text
{'name': 'Ali', 'age': 20}
{'name': 'Ali', 'age': 21}
```

Dictionary اصلی تغییر نکرده است.

این هدف اصلی Copy کردن است:

> ایجاد یک Dictionary جدید که حداقل در سطح بیرونی بتواند مستقل از Dictionary اصلی تغییر کند.

---

## ۷. بررسی Copy با `is`

می توانیم این موضوع را بررسی کنیم:

```python
student = {
    "name": "Ali"
}

another_student = student.copy()

print(student == another_student)
print(student is another_student)
```

خروجی:

```text
True
False
```

داده ها برابر هستند.

اما Objectها متفاوت هستند.

این دقیقاً همان رفتاری است که معمولاً از یک Copy انتظار داریم.

---

## ۸. یک روش دیگر برای Copy کردن Dictionary

می توانیم از Constructor به نام `dict()` نیز استفاده کنیم:

```python
student = {
    "name": "Ali",
    "age": 20
}

another_student = dict(student)
```

این روش نیز یک Dictionary بیرونی جدید ایجاد می کند.

مثلاً:

```python
another_student["age"] = 21

print(student["age"])
```

خروجی:

```text
20
```

هم `copy()` و هم `dict()` برای ساخت یک Dictionary بیرونی جدید کاربرد دارند.

---

## ۹. Copy با Dictionary Comprehension

یک Dictionary را می توان با Dictionary Comprehension نیز کپی کرد:

```python
student = {
    "name": "Ali",
    "age": 20
}

another_student = {
    key: value
    for key, value in student.items()
}
```

این روش نیز یک Dictionary بیرونی جدید می سازد.

اما برای یک Copy ساده، معمولاً این روش خواناتر است:

```python
another_student = student.copy()
```

Comprehension زمانی ارزش بیشتری دارد که همزمان بخواهیم داده ها را فیلتر یا تغییر دهیم.

---

## ۱۰. Shallow Copy چیست؟

متد `copy()` یک **Shallow Copy** ایجاد می کند.

یعنی:

* Dictionary بیرونی Copy می شود؛
* Entryهای سطح اول در Dictionary جدید قرار می گیرند؛
* اما Objectهای Mutable تو در تو ممکن است همچنان مشترک باشند.

مثلاً:

```python
student = {
    "name": "Ali",
    "scores": {
        "math": 18,
        "python": 20
    }
}

another_student = student.copy()
```

Dictionaryهای بیرونی متفاوت هستند.

اما Dictionary مربوط به `"scores"` همچنان مشترک است.

به صورت مفهومی:

```text
student
   ↓
Outer Dictionary A
   │
   └── scores ─────┐
                   ↓
              Inner Dictionary
              math → 18
              python → 20
                   ↑
   ┌── scores ─────┘
   │
Outer Dictionary B
   ↑
another_student
```

این یکی از مهم ترین مفاهیم هنگام Copy کردن داده های Nested است.

---

## ۱۱. مشکل Shallow Copy

حالا:

```python
another_student["scores"]["python"] = 21
```

چه اتفاقی برای Dictionary اصلی می افتد؟

```python
print(student["scores"]["python"])
```

خروجی:

```text
21
```

ممکن است این رفتار عجیب به نظر برسد.

ما `copy()` کردیم، پس چرا Original هم تغییر کرد؟

چون `copy()` فقط **Dictionary بیرونی** را Copy کرده است.

Dictionary داخلی `"scores"` کپی نشده است.

هر دو Dictionary بیرونی هنوز به همان Dictionary داخلی اشاره می کنند.

---

## ۱۲. دقیقاً چه چیزی با `copy()` کپی می شود؟

فرض کنید:

```python
student = {
    "name": "Ali",
    "scores": {
        "python": 20
    }
}

another_student = student.copy()
```

رابطه تقریباً چنین است:

```text
student ───────────────→ Outer Dictionary A
                           │
                           ├── name → "Ali"
                           │
                           └── scores ─────┐
                                          ↓
                                      Inner Dictionary
                                      python → 20
                                          ↑
another_student ───────→ Outer Dictionary B
                           │
                           └── scores ─────┘
```

Objectهای بیرونی متفاوت هستند.

Object داخلی مشترک است.

این دقیقاً معنی Shallow Copy است.

---

## ۱۳. بررسی Object داخلی با `is`

می توانیم این موضوع را ثابت کنیم:

```python
student = {
    "scores": {
        "python": 20
    }
}

another_student = student.copy()

print(student is another_student)
print(student["scores"] is another_student["scores"])
```

خروجی:

```text
False
True
```

نتیجه اول نشان می دهد Dictionaryهای بیرونی متفاوت هستند.

نتیجه دوم نشان می دهد Dictionaryهای داخلی همان Object هستند.

---

## ۱۴. چرا این موضوع مهم است؟

این تفاوت زمانی اهمیت پیدا می کند که Dictionary شامل Objectهای Mutable دیگری مانند این موارد باشد:

* Dictionary
* List
* Set
* ساختارهای Mutable دیگر

مثلاً:

```python
data = {
    "name": "Ali",
    "skills": ["Python", "HTML"]
}
```

اگر این Dictionary را Shallow Copy کنیم:

```python
new_data = data.copy()
```

Dictionary بیرونی جدید است، اما List مربوط به `"skills"` می تواند همچنان مشترک باشد.

بنابراین:

```python
new_data["skills"].append("CSS")
```

ممکن است روی:

```python
data["skills"]
```

نیز اثر بگذارد.

درک این رفتار از ایجاد بسیاری از Bugهای دشوار جلوگیری می کند.

---

## ۱۵. Deep Copy

اگر بخواهیم یک Copy کاملاً مستقل داشته باشیم، حتی برای Objectهای تو در تو، می توانیم از **Deep Copy** استفاده کنیم.

Python این قابلیت را در Module به نام `copy` ارائه می دهد:

```python
import copy
```

سپس:

```python
another_student = copy.deepcopy(student)
```

Deep Copy به صورت بازگشتی Objectهای داخلی را نیز Copy می کند.

---

## ۱۶. تفاوت Shallow Copy و Deep Copy

فرض کنید:

```python
student = {
    "name": "Ali",
    "scores": {
        "math": 18,
        "python": 20
    }
}
```

### Shallow Copy

```python
another_student = student.copy()
```

نتیجه:

```text
Outer Dictionary → کپی شده
Inner Dictionary → مشترک
```

### Deep Copy

```python
import copy

another_student = copy.deepcopy(student)
```

نتیجه:

```text
Outer Dictionary → کپی شده
Inner Dictionary → کپی شده
```

بنابراین:

```python
another_student["scores"]["python"] = 21
```

بعد از Deep Copy، روی:

```python
student["scores"]["python"]
```

اثری ندارد.

---

## ۱۷. نمایش عملی `deepcopy()`

```python
import copy

student = {
    "name": "Ali",
    "scores": {
        "math": 18,
        "python": 20
    }
}

another_student = copy.deepcopy(student)

another_student["scores"]["python"] = 21

print(student["scores"]["python"])
print(another_student["scores"]["python"])
```

خروجی:

```text
20
21
```

Dictionary داخلی کاملاً مستقل است.

---

## ۱۸. Deep Copy و Identity

می توانیم تفاوت را با `is` بررسی کنیم:

```python
import copy

student = {
    "scores": {
        "python": 20
    }
}

another_student = copy.deepcopy(student)

print(student is another_student)
print(student["scores"] is another_student["scores"])
```

خروجی:

```text
False
False
```

هم Dictionary بیرونی و هم Dictionary داخلی Objectهای جداگانه هستند.

---

## ۱۹. انتخاب بین Assignment، Shallow Copy و Deep Copy

این سه عملیات کاربردهای متفاوتی دارند.

### Assignment

```python
second = first
```

زمانی استفاده می شود که عمداً بخواهیم Variable جدید به همان Object اشاره کند.

```text
first ─────┐
           ↓
        Object
           ↑
second ────┘
```

### Shallow Copy

```python
second = first.copy()
```

زمانی مناسب است که یک Dictionary بیرونی جدید بخواهیم، اما لزوماً نیازی نداشته باشیم Objectهای Mutable داخلی نیز مستقل باشند.

```text
first  → Outer A → Inner
second → Outer B ──↑
```

### Deep Copy

```python
second = copy.deepcopy(first)
```

زمانی استفاده می شود که کل ساختار Nested باید کاملاً مستقل باشد.

```text
first  → Outer A → Inner A
second → Outer B → Inner B
```

---

## ۲۰. Copy قبل از تغییر

یکی از کاربردهای رایج Copy این است که داده اصلی را نگه داریم و یک نسخه تغییر یافته بسازیم.

مثلاً:

```python
original = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}

updated = original.copy()

updated["age"] = 21
```

حالا دو نسخه داریم:

```text
original → اطلاعات اصلی

updated  → اطلاعات تغییر یافته
```

این الگو زمانی کاربردی است که بخواهیم نسخه اصلی داده همچنان در دسترس باشد.

---

## ۲۱. ساخت چند Record مستقل

فرض کنید می خواهیم چند Record را بر اساس یک Template ایجاد کنیم:

```python
template = {
    "name": "",
    "age": 0,
    "city": ""
}
```

می توانیم:

```python
student1 = template.copy()
student2 = template.copy()
```

سپس:

```python
student1["name"] = "Ali"
student2["name"] = "Sara"
```

در این حالت Dictionaryهای بیرونی مستقل هستند:

```python
print(student1)
print(student2)
```

خروجی:

```text
{'name': 'Ali', 'age': 0, 'city': ''}
{'name': 'Sara', 'age': 0, 'city': ''}
```

این الگو برای ساخت چند Record بر اساس یک ساختار مشترک بسیار مفید است.

---

## ۲۲. مشکل Objectهای Mutable

مفهوم عمیق تر پشت Copy کردن Dictionary، مفهوم **Mutability** است.

Dictionary یک Object Mutable است.

یعنی بعد از ایجاد آن می توان محتوایش را تغییر داد.

وقتی می نویسیم:

```python
second = first
```

Python Object Mutable را Duplicate نمی کند.

فقط یک Reference دیگر به همان Object ایجاد می کند.

وقتی می نویسیم:

```python
second = first.copy()
```

Python یک Dictionary بیرونی جدید ایجاد می کند.

درک این رابطه بسیار مهم تر از حفظ کردن صرف Syntax مربوط به `copy()` است.

---

## ۲۳. مثال کاربردی

فرض کنید:

```python
product = {
    "name": "Laptop",
    "price": 1200,
    "specs": {
        "ram": 16,
        "storage": 512
    }
}
```

می خواهیم یک نسخه ارزان تر ایجاد کنیم.

اگر فقط یک Value بیرونی را تغییر دهیم، Shallow Copy کافی است:

```python
discounted = product.copy()

discounted["price"] = 1000
```

قیمت Original همچنان:

```python
print(product["price"])
```

خروجی:

```text
1200
```

اما اگر مشخصات داخلی را نیز تغییر دهیم:

```python
discounted["specs"]["ram"] = 32
```

ممکن است RAM محصول اصلی نیز تغییر کند، چون `"specs"` مشترک است.

اگر استقلال کامل لازم باشد:

```python
import copy

discounted = copy.deepcopy(product)
```

راه مناسب تری است.

---

## ۲۴. اشتباه رایج

یک تصور رایج در میان افراد مبتدی این است:

```python
second = first
```

یعنی:

> «از `first` یک Copy بساز.»

اما چنین نیست.

معنی آن این است:

> «کاری کن `second` به همان Objectی اشاره کند که `first` به آن اشاره می کند.»

این تفاوت هرچه برنامه بزرگ تر و ساختار داده پیچیده تر شود، اهمیت بیشتری پیدا می کند.

---

## ۲۵. یک قانون کاربردی

یک قانون ساده برای به خاطر سپردن:

```text
=          → Assignment / Reference

.copy()    → Shallow Copy

deepcopy() → Copy بازگشتی و مستقل
```

برای Dictionaryهای ساده و بدون ساختار تو در تو:

```python
second = first.copy()
```

معمولاً کافی است.

برای ساختارهای Nested و Mutable:

```python
second = copy.deepcopy(first)
```

ممکن است لازم باشد.

---

## نکات کلیدی

* `second = first` یک Dictionary جدید ایجاد نمی کند.
* Assignment فقط یک Reference دیگر به همان Object می سازد.
* `is` بررسی می کند که دو Variable به یک Object اشاره می کنند یا نه.
* `==` بررسی می کند که Valueهای دو Object برابر هستند یا نه.
* `Dictionary.copy()` یک Dictionary بیرونی جدید ایجاد می کند.
* `copy()` یک **Shallow Copy** ایجاد می کند.
* Objectهای Mutable تو در تو ممکن است بعد از Shallow Copy همچنان مشترک باشند.
* `copy.deepcopy()` Objectهای داخلی را نیز به صورت بازگشتی Copy می کند.
* Deep Copy زمانی کاربرد دارد که استقلال کامل ساختار Nested لازم باشد.
* `dict(first)` نیز می تواند یک Dictionary بیرونی جدید ایجاد کند.
* Dictionary Comprehension می تواند برای Copy کردن همراه با Transform کردن داده ها استفاده شود.
* درک Mutability و Referenceها از حفظ کردن Syntax مربوط به Copy مهم تر است.

---

# سوال های بخش

## سوال ۱

تفاوت این دو چیست؟

```python
second = first
```

و:

```python
second = first.copy()
```

## سوال ۲

کد زیر چه چیزی چاپ می کند؟

```python
first = {"age": 20}
second = first

second["age"] = 21

print(first["age"])
```

## سوال ۳

تفاوت `==` و `is` چیست؟

## سوال ۴

چرا تغییر یک Dictionary داخلی بعد از `copy()` می تواند روی Dictionary اصلی نیز اثر بگذارد؟

## سوال ۵

چه زمانی از `copy.deepcopy()` استفاده می کنیم؟

---

# سوال جامع

Dictionary زیر را در نظر بگیرید:

```python
student = {
    "name": "Ali",
    "scores": {
        "math": 18,
        "python": 20
    }
}
```

برنامه ای بنویسید که:

1. یک Shallow Copy ایجاد کند.
2. یک Deep Copy ایجاد کند.
3. نمره Python را در Shallow Copy تغییر دهد.
4. نمره Python را در Deep Copy تغییر دهد.
5. Original و هر دو Copy را چاپ کند.
6. با استفاده از `is` نشان دهد کدام Dictionaryهای داخلی مشترک هستند.

---

# پاسخ ها

## پاسخ سوال ۱

```python
second = first
```

یک Reference دیگر به همان Dictionary ایجاد می کند.

اما:

```python
second = first.copy()
```

یک Dictionary بیرونی جدید ایجاد می کند.

## پاسخ سوال ۲

```text
21
```

زیرا هر دو Variable به یک Dictionary اشاره می کنند.

## پاسخ سوال ۳

`==` مقدارها را مقایسه می کند.

`is` هویت Object را بررسی می کند.

مثلاً:

```python
first = {"name": "Ali"}
second = {"name": "Ali"}

print(first == second)  # True
print(first is second)  # False
```

## پاسخ سوال ۴

چون `copy()` یک Shallow Copy ایجاد می کند.

Dictionary بیرونی Copy می شود، اما Objectهای Mutable داخلی مانند List و Dictionary می توانند همچنان مشترک باشند.

## پاسخ سوال ۵

زمانی از `copy.deepcopy()` استفاده می کنیم که بخواهیم کل ساختار Nested از جمله Objectهای داخلی آن کاملاً مستقل باشد.

## پاسخ سوال جامع

```python
import copy

student = {
    "name": "Ali",
    "scores": {
        "math": 18,
        "python": 20
    }
}

shallow = student.copy()
deep = copy.deepcopy(student)

shallow["scores"]["python"] = 21
deep["scores"]["python"] = 22

print("Original:", student)
print("Shallow:", shallow)
print("Deep:", deep)

print(student is shallow)
print(student["scores"] is shallow["scores"])

print(student is deep)
print(student["scores"] is deep["scores"])
```

نتیجه مهم:

```text
student is shallow
→ False

student["scores"] is shallow["scores"]
→ True

student is deep
→ False

student["scores"] is deep["scores"]
→ False
```

این نتیجه تفاوت اصلی بین Shallow Copy و Deep Copy را نشان می دهد.

---

# پارت ۱۳ — Converting Between Dictionaries and Other Data Structures

## مقدمه

Dictionary یکی از مهم ترین Data Structureهای Python است، چون رابطه ای بین **Key** و **Value** ایجاد می کند.

اما در برنامه های واقعی، داده ها معمولاً برای همیشه در یک ساختار باقی نمی مانند.

ممکن است داده را به شکل:

* List
* Tuple
* Set
* مجموعه ای از Pairهای Key-Value
* یا یک Dictionary دیگر

دریافت کنیم و لازم باشد آن را به ساختاری تبدیل کنیم که برای عملیات بعدی مناسب تر است.

بنابراین هدف این بخش فقط حفظ کردن Syntax تبدیل نیست.

باید بفهمیم:

* چه چیزی در تبدیل حفظ می شود؟
* چه چیزی از بین می رود؟
* Python داده را چگونه تفسیر می کند؟
* و چه زمانی هر ساختار انتخاب بهتری است؟

---

## ۱. تبدیل Dictionary به List

وقتی یک Dictionary را به `list()` می دهیم، Python آن را به Listای از **Keyها** تبدیل می کند.

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}

keys = list(student)

print(keys)
```

خروجی:

```text
['name', 'age', 'city']
```

این تقریباً معادل این است:

```python
keys = list(student.keys())
```

نکته مهم این است که:

```python
list(dictionary)
```

یعنی:

> Keyهای Dictionary را به یک List تبدیل کن.

این دستور کل Key-Valueها را به List تبدیل نمی کند.

---

## ۲. تبدیل Keyهای Dictionary به List

اگر هدف ما مشخصاً گرفتن Keyها باشد، استفاده از `.keys()` مفهوم کد را واضح تر می کند:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}

keys = list(student.keys())

print(keys)
```

خروجی:

```text
['name', 'age', 'city']
```

این کار زمانی مفید است که بخواهیم Keyها را به عنوان یک List واقعی پردازش کنیم.

مثلاً:

```python
for key in keys:
    print(key)
```

---

## ۳. تبدیل Valueهای Dictionary به List

برای Valueها می توانیم از `.values()` استفاده کنیم:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}

values = list(student.values())

print(values)
```

خروجی:

```text
['Ali', 20, 'Baku']
```

بنابراین:

```python
list(student)
```

Keyها را می دهد، در حالی که:

```python
list(student.values())
```

Valueها را می دهد.

---

## ۴. تبدیل Items به List

گاهی همزمان به Key و Value نیاز داریم.

متد `.items()` Pairهای Key-Value را در اختیارمان قرار می دهد:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}

items = list(student.items())

print(items)
```

خروجی:

```text
[('name', 'Ali'), ('age', 20), ('city', 'Baku')]
```

هر Item یک Tuple به شکل زیر است:

```text
(key, value)
```

پس نتیجه نهایی یک **List از Tupleها** است.

---

## ۵. Dictionary → List of Tuples

این تبدیل اهمیت زیادی دارد:

```python
data = {
    "name": "Ali",
    "age": 20
}

pairs = list(data.items())
```

نتیجه:

```python
[
    ("name", "Ali"),
    ("age", 20)
]
```

هر Tuple یک رابطه Key-Value را نمایش می دهد.

این ساختار زمانی مفید است که بخواهیم:

* Entryهای Dictionary را Sort کنیم؛
* روی Pairها Iteration انجام دهیم؛
* داده را به یک Function منتقل کنیم؛
* یا ساختار را Transform کنیم.

---

## ۶. تبدیل Dictionary به Tuple

می توانیم Keyهای Dictionary را به Tuple تبدیل کنیم:

```python
student = {
    "name": "Ali",
    "age": 20
}

keys = tuple(student)
```

نتیجه:

```python
('name', 'age')
```

برای Valueها:

```python
values = tuple(student.values())
```

نتیجه:

```python
('Ali', 20)
```

و برای Items:

```python
items = tuple(student.items())
```

نتیجه:

```python
(('name', 'Ali'), ('age', 20))
```

---

## ۷. تبدیل Dictionary به Set

Dictionary را می توان به Set نیز تبدیل کرد:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}

keys = set(student)
```

نتیجه:

```python
{'name', 'age', 'city'}
```

در اینجا نیز Keyهای Dictionary استفاده می شوند.

اگر Valueها را بخواهیم:

```python
values = set(student.values())
```

این تبدیل زمانی مفید است که برای ما **Unique بودن و Membership** مهم باشد، نه رابطه Key-Value.

---

## ۸. تبدیل List از Pairها به Dictionary

جهت برعکس نیز بسیار مهم است.

فرض کنید:

```python
pairs = [
    ("name", "Ali"),
    ("age", 20),
    ("city", "Baku")
]
```

می توانیم آن را به Dictionary تبدیل کنیم:

```python
student = dict(pairs)

print(student)
```

خروجی:

```text
{'name': 'Ali', 'age': 20, 'city': 'Baku'}
```

Python انتظار دارد هر Element دقیقاً دو بخش داشته باشد:

```text
(key, value)
```

به همین دلیل Listای از Tupleهای دو عضوی یک ورودی طبیعی برای `dict()` است.

---

## ۹. List از Listها → Dictionary

Elementها الزاماً Tuple نیستند.

Listهای دو عضوی نیز قابل استفاده هستند:

```python
pairs = [
    ["name", "Ali"],
    ["age", 20],
    ["city", "Baku"]
]

student = dict(pairs)
```

نتیجه:

```python
{
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}
```

بنابراین مسئله اصلی List یا Tuple بودن نیست.

مهم این است که هر Element دو مقدار در اختیار `dict()` قرار دهد:

```text
key + value
```

---

## ۱۰. Tuple از Pairها → Dictionary

Tupleای که شامل Pairهای Key-Value باشد نیز قابل تبدیل است:

```python
pairs = (
    ("name", "Ali"),
    ("age", 20)
)

student = dict(pairs)

print(student)
```

خروجی:

```text
{'name': 'Ali', 'age': 20}
```

در نتیجه `dict()` می تواند ساختارهای Iterable مختلفی را دریافت کند، به شرطی که هر Element بتواند یک Key و یک Value ارائه کند.

---

## ۱۱. Dictionary → Dictionary

اگر یک Dictionary را به `dict()` بدهیم، یک Dictionary بیرونی جدید ایجاد می شود:

```python
original = {
    "name": "Ali",
    "age": 20
}

new_dictionary = dict(original)
```

محتوای آن یکسان است:

```python
print(new_dictionary)
```

خروجی:

```text
{'name': 'Ali', 'age': 20}
```

اما:

```python
print(original is new_dictionary)
```

نتیجه:

```text
False
```

یعنی Dictionary بیرونی جدید است.

البته این را باید مانند `copy()` یک **Shallow Copy** در نظر گرفت، نه یک Deep Copy بازگشتی.

---

## ۱۲. تبدیل همزمان Key و Value

یکی از تبدیل های کاربردی این است که Dictionary را به Listای از Pairها تبدیل کنیم:

```python
data = {
    "Python": 90,
    "HTML": 80,
    "CSS": 75
}

pairs = list(data.items())
```

نتیجه:

```python
[
    ("Python", 90),
    ("HTML", 80),
    ("CSS", 75)
]
```

حالا داده به شکل یک Sequence درآمده است.

مثلاً:

```python
for subject, score in pairs:
    print(subject, score)
```

این مثال نشان می دهد چرا Conversion مفید است.

ما فقط Syntax را تغییر نداده ایم؛ بلکه **نحوه پردازش داده** را تغییر داده ایم.

---

## ۱۳. تبدیل Dictionary به List برای Sorting

می توانیم Entryهای Dictionary را قبل از Sorting به List از Tupleها تبدیل کنیم:

```python
scores = {
    "Ali": 85,
    "Sara": 95,
    "Reza": 78
}

items = list(scores.items())

items.sort(key=lambda item: item[1])

print(items)
```

خروجی:

```text
[('Reza', 78), ('Ali', 85), ('Sara', 95)]
```

Dictionary به Sequenceای از Pairها تبدیل شده تا بتوانیم Entryها را بر اساس Value مرتب کنیم.

این یک مثال عملی از انتخاب Data Structure بر اساس عملیاتی است که می خواهیم انجام دهیم.

---

## ۱۴. تبدیل Dictionary به JSON

یکی دیگر از Conversionهای مهم در برنامه های واقعی، تبدیل Dictionary به JSON است.

Python برای این کار Moduleای به نام `json` دارد:

```python
import json
```

با `json.dumps()` می توان Dictionary را به JSON String تبدیل کرد:

```python
student = {
    "name": "Ali",
    "age": 20
}

json_data = json.dumps(student)

print(json_data)
```

خروجی:

```text
{"name": "Ali", "age": 20}
```

این با تبدیل ساده Dictionary به String با `str()` متفاوت است.

JSON یک Data Format ساختاریافته برای تبادل داده بین سیستم های مختلف است.

---

## ۱۵. JSON → Dictionary

تبدیل برعکس با `json.loads()` انجام می شود:

```python
import json

json_data = '{"name": "Ali", "age": 20}'

student = json.loads(json_data)

print(student)
```

خروجی:

```text
{'name': 'Ali', 'age': 20}
```

اکنون JSON String دوباره به Python Dictionary تبدیل شده است.

رابطه کلی:

```text
Python Dictionary
       ↓
   json.dumps()
       ↓
    JSON String
       ↓
   json.loads()
       ↓
Python Dictionary
```

---

## ۱۶. Dictionary → List → Dictionary

Conversionها را می توان پشت سر هم نیز انجام داد.

مثلاً:

```python
student = {
    "name": "Ali",
    "age": 20
}

pairs = list(student.items())

new_student = dict(pairs)
```

Dictionary نهایی همان رابطه های Key-Value را دارد:

```python
print(new_student)
```

خروجی:

```text
{'name': 'Ali', 'age': 20}
```

این مثال یک مفهوم مهم را نشان می دهد:

> Conversion می تواند Representation داده را تغییر دهد، بدون اینکه الزاماً اطلاعاتی که داده نمایش می دهد تغییر کند.

---

## ۱۷. چه چیزی ممکن است هنگام Conversion از بین برود؟

همه Conversionها تمام ویژگی های ساختار قبلی را حفظ نمی کنند.

مثلاً:

```python
data = {
    "a": 10,
    "b": 10,
    "c": 20
}

values = set(data.values())

print(values)
```

نتیجه:

```text
{10, 20}
```

یکی از `10`ها از بین رفته است.

چرا؟

چون Set فقط Elementهای Unique را نگه می دارد.

پس:

```text
Dictionary → Set
```

در صورت وجود Valueهای تکراری می تواند باعث **از دست رفتن اطلاعات** شود.

بنابراین Conversion باید آگاهانه انجام شود.

---

## ۱۸. Dictionary → Set در برابر Dictionary → List

فرض کنید:

```python
data = {
    "a": 10,
    "b": 10,
    "c": 20
}
```

این:

```python
list(data.values())
```

نتیجه می دهد:

```text
[10, 10, 20]
```

اما:

```python
set(data.values())
```

نتیجه می دهد:

```text
{10, 20}
```

List مقدارهای تکراری را حفظ می کند.

Set تکراری ها را حذف می کند.

بنابراین انتخاب بین آن ها به نیاز برنامه بستگی دارد.

---

## ۱۹. تبدیل Keyها به ساختارهای مختلف

برای Dictionary زیر:

```python
data = {
    "a": 10,
    "b": 20,
    "c": 30
}
```

می توانیم داشته باشیم:

```python
list(data.keys())
```

```text
['a', 'b', 'c']
```

یا:

```python
tuple(data.keys())
```

```text
('a', 'b', 'c')
```

یا:

```python
set(data.keys())
```

```text
{'a', 'b', 'c'}
```

بنابراین یک منبع داده می تواند بر اساس نیاز برنامه با چند Representation مختلف نمایش داده شود.

---

## ۲۰. انتخاب Conversion مناسب

مهم ترین سؤال این نیست:

> «چطور این Dictionary را تبدیل کنم؟»

سؤال بهتر این است:

> «عملیات بعدی به چه Data Structureای نیاز دارد؟»

مثلاً:

| هدف                           | Representation مناسب |
| ----------------------------- | -------------------- |
| دسترسی با Key                 | Dictionary           |
| پردازش Keyها به صورت Sequence | List/Tuple از Keyها  |
| پردازش Key-Value Pairها       | List/Tuple از Items  |
| حذف Valueهای تکراری           | Set                  |
| Sort کردن Entryها             | List از Pairها       |
| تبادل داده با سیستم دیگر      | JSON                 |
| ساخت Dictionary از Pairها     | `dict()`             |

پس Conversion باید در خدمت عملیاتی باشد که بعد از آن انجام می دهیم.

---

## ۲۱. مثال کاربردی

فرض کنید اطلاعات کاربر را به شکل List از Pairها دریافت کرده ایم:

```python
user_data = [
    ("username", "ali"),
    ("age", 20),
    ("country", "Azerbaijan")
]
```

می توانیم آن را تبدیل کنیم:

```python
user = dict(user_data)
```

حالا دسترسی به داده بسیار ساده تر است:

```python
print(user["username"])
print(user["age"])
```

خروجی:

```text
ali
20
```

ساختار اولیه برای نمایش Sequenceای از Pairها مناسب بود.

اما Dictionary برای دسترسی به اطلاعات با Key مناسب تر است.

---

## ۲۲. یک مثال کاربردی دیگر

فرض کنید:

```python
scores = {
    "Ali": 85,
    "Sara": 95,
    "Reza": 85
}
```

اگر همه Scoreها را بخواهیم:

```python
scores_list = list(scores.values())
```

نتیجه:

```text
[85, 95, 85]
```

اگر فقط Scoreهای Unique را بخواهیم:

```python
unique_scores = set(scores.values())
```

نتیجه:

```text
{85, 95}
```

یک Dictionary واحد می تواند بر اساس مسئله به ساختارهای متفاوتی تبدیل شود.

---

## ۲۳. اشتباهات رایج

### اشتباه ۱: انتظار داشتن Valueها از `list(dictionary)`

```python
data = {"a": 10, "b": 20}

print(list(data))
```

نتیجه:

```text
['a', 'b']
```

این دستور Keyها را تولید می کند.

برای Valueها:

```python
list(data.values())
```

را استفاده کنید.

---

### اشتباه ۲: فراموش کردن `.items()`

اگر Key و Value را با هم می خواهیم:

```python
list(data.items())
```

مناسب است، نه:

```python
list(data)
```

---

### اشتباه ۳: دادن داده نامعتبر به `dict()`

این درست است:

```python
dict([
    ("a", 1),
    ("b", 2)
])
```

اما این ساختار Pairهای معتبر Key-Value ایجاد نمی کند:

```python
dict([
    ("a", 1, 2),
    ("b", 3, 4)
])
```

هر Element باید دقیقاً دو بخش داشته باشد.

---

### اشتباه ۴: تصور اینکه Set تکراری ها را نگه می دارد

این:

```python
set([10, 10, 20])
```

تبدیل می شود به:

```text
{10, 20}
```

---

## ۲۴. مفهوم عمیق تر

درس اصلی Conversion این است که **Data Structureهای مختلف، روش های مختلفی برای سازمان دهی اطلاعات هستند.**

Dictionary روی این رابطه تأکید دارد:

```text
key → value
```

List روی این مفهوم تأکید دارد:

```text
ordered sequence
```

Tuple یک Sequence ثابت تر را نمایش می دهد:

```text
fixed sequence
```

Set روی این مفهوم تمرکز دارد:

```text
unique membership
```

و JSON بیشتر برای این هدف طراحی شده است:

```text
data exchange
```

پس تبدیل بین آن ها یعنی انتخاب Representationای که با عملیات بعدی برنامه بهتر سازگار باشد.

به همین دلیل درک Conversionها از حفظ کردن چند دستور جداگانه مهم تر است.

---

## نکات کلیدی

* `list(dictionary)` Keyهای Dictionary را تولید می کند.
* `list(dictionary.keys())` به صورت واضح Listای از Keyها می سازد.
* `list(dictionary.values())` Listای از Valueها می سازد.
* `list(dictionary.items())` Listای از Tupleهای `(key, value)` می سازد.
* `tuple()` نیز برای تبدیل Keyها، Valueها یا Items قابل استفاده است.
* `set()` زمانی مفید است که Elementهای Unique نیاز داشته باشیم.
* `dict()` می تواند از Pairهای Key-Value یک Dictionary بسازد.
* List از Tupleها و List از Listها می توانند به Dictionary تبدیل شوند.
* `dict(existing_dictionary)` یک Dictionary بیرونی جدید ایجاد می کند.
* `json.dumps()` Dictionary را به JSON تبدیل می کند.
* `json.loads()` JSON را به Python Dictionary تبدیل می کند.
* Conversion می تواند نحوه پردازش داده را تغییر دهد.
* بعضی Conversionها ممکن است باعث از دست رفتن اطلاعات شوند، مخصوصاً هنگام تبدیل به Set.
* Conversion مناسب به عملیاتی بستگی دارد که قرار است بعد از آن انجام شود.

---

# سوال های بخش

## سوال ۱

کد زیر چه چیزی تولید می کند؟

```python
data = {
    "name": "Ali",
    "age": 20
}

print(list(data))
```

## سوال ۲

چطور یک List شامل تمام Valueهای Dictionary ایجاد می کنیم؟

## سوال ۳

`list(data.items())` چه ساختاری تولید می کند؟

## سوال ۴

چطور ساختار زیر را به Dictionary تبدیل می کنیم؟

```python
pairs = [
    ("name", "Ali"),
    ("age", 20)
]
```

## سوال ۵

هنگام تبدیل Valueهای Dictionary به Set چه اطلاعاتی ممکن است از بین برود؟

## سوال ۶

تفاوت `json.dumps()` و `json.loads()` چیست؟

---

# سوال جامع

Dictionary زیر را در نظر بگیرید:

```python
scores = {
    "Ali": 85,
    "Sara": 95,
    "Reza": 85
}
```

برنامه ای بنویسید که:

1. Keyها را به List تبدیل کند.
2. Valueها را به List تبدیل کند.
3. Valueها را به Set تبدیل کند.
4. Items را به Listای از Tupleها تبدیل کند.
5. همان List از Tupleها را دوباره به Dictionary تبدیل کند.
6. Dictionary را به JSON تبدیل کند.
7. JSON را دوباره به Python Dictionary تبدیل کند.
8. هر ساختار حاصل را چاپ کند.

هدف فقط یادگیری Syntax نیست؛ باید مشاهده کنید که با هر Conversion، **Representation و ویژگی های داده** چگونه تغییر می کنند.

---

# مرور نهایی: Dictionaries

این بخش قرار نیست دوباره تمام متدهای Dictionary را به شکل جداگانه تکرار کند.

هدف این مرور، ساختن یک **مدل ذهنی کامل از Dictionary** است؛ مدلی که بتوانید هنگام مواجه شدن با یک مسئله جدید، بدون حفظ کردن Syntaxهای پراکنده، تصمیم درست بگیرید.

---

## ۱. ایده اصلی Dictionary

Dictionary داده ها را به شکل رابطه بین **Key** و **Value** نگه می دارد:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}
```

مدل ذهنی اصلی:

```text
"name" → "Ali"
"age"  → 20
"city" → "Baku"
```

بنابراین Dictionary زمانی مناسب است که برنامه بخواهد به این سؤال پاسخ دهد:

> «با داشتن این شناسه، چه اطلاعاتی متعلق به آن است؟»

مثلاً:

```python
student["age"]
```

به این معنا نیست که:

> «عنصر دوم را بده.»

بلکه یعنی:

> «مقدار مربوط به Keyای به نام `age` را بده.»

این تفاوت یکی از بنیادی ترین مفاهیم Dictionary است.

---

# ۲. Dictionary در برابر List

این دو ساختار را مقایسه کنید:

```python
students = ["Ali", "Sara", "Reza"]
```

و:

```python
students = {
    "first": "Ali",
    "second": "Sara",
    "third": "Reza"
}
```

List به طور طبیعی با Position کار می کند:

```python
students[0]
```

اما Dictionary با Meaning یا Key کار می کند:

```python
students["first"]
```

پس تفاوت عمیق این نیست که:

> List با عدد کار می کند و Dictionary با String.

بلکه:

* List → **Position-oriented**
* Dictionary → **Key-oriented**

Key به داده یک معنای مشخص می دهد.

---

# ۳. ساخت Dictionary

Dictionary را می توان با `{}` ساخت:

```python
person = {
    "name": "Ali",
    "age": 20
}
```

Dictionary خالی:

```python
person = {}
```

و سپس می توان داده به آن اضافه کرد:

```python
person["name"] = "Ali"
person["age"] = 20
```

همچنین `dict()` وجود دارد:

```python
person = dict(name="Ali", age=20)
```

تمام این روش ها در نهایت یک نوع داده ایجاد می کنند:

```python
type(person)
```

```text
<class 'dict'>
```

---

# ۴. Key و Value نقش یکسانی ندارند

Dictionary زیر را در نظر بگیرید:

```python
product = {
    "name": "Laptop",
    "price": 1200,
    "stock": 15
}
```

در اینجا:

```text
Keys:
"name"
"price"
"stock"

Values:
"Laptop"
1200
15
```

Key مشخص می کند اطلاعات مربوط به چه چیزی است.

Value خود اطلاعات است.

به همین دلیل Keyها محدودیت های متفاوتی نسبت به Valueها دارند.

Key باید **Hashable** باشد، در حالی که Value چنین محدودیتی ندارد.

مثلاً این کاملاً معتبر است:

```python
data = {
    "numbers": [1, 2, 3],
    "settings": {"theme": "dark"},
    "tags": {"python", "programming"}
}
```

اما ساختارهای Mutable مانند List و Set را نمی توان معمولاً به عنوان Key استفاده کرد.

---

# ۵. دسترسی به داده

مستقیم ترین روش:

```python
student["name"]
```

اگر Key وجود نداشته باشد:

```python
student["email"]
```

Python خطای:

```text
KeyError
```

می دهد.

اگر احتمال می دهیم Key وجود نداشته باشد، `.get()` مناسب تر است:

```python
student.get("email")
```

که:

```text
None
```

برمی گرداند.

می توانیم مقدار پیش فرض نیز تعیین کنیم:

```python
student.get("email", "Not provided")
```

نتیجه:

```text
Not provided
```

تفاوت مفهومی مهم:

```text
dictionary[key]
```

یعنی:

> انتظار داریم این Key وجود داشته باشد.

اما:

```text
dictionary.get(key)
```

یعنی:

> ممکن است این Key وجود داشته باشد یا نداشته باشد.

---

# ۶. اضافه کردن و به روزرسانی

این دستور:

```python
student["age"] = 21
```

دو رفتار ممکن دارد.

اگر `"age"` از قبل وجود داشته باشد، مقدار آن تغییر می کند.

اگر وجود نداشته باشد، یک Entry جدید ساخته می شود.

پس:

```python
dictionary[key] = value
```

می تواند هم به معنای:

```text
Add
```

و هم:

```text
Update
```

باشد.

تشخیص این دو رفتار بر اساس وجود یا عدم وجود Key انجام می شود.

---

# ۷. حذف داده

چند روش مهم برای حذف وجود دارد:

```python
del student["age"]
```

یک Key مشخص را حذف می کند.

```python
student.pop("age")
```

Key را حذف می کند و Value آن را نیز برمی گرداند.

```python
student.clear()
```

تمام Entryها را حذف می کند.

انتخاب روش به هدف برنامه بستگی دارد.

اگر Value حذف شده را لازم داریم:

```python
age = student.pop("age")
```

از `del` مناسب تر است.

---

# ۸. بررسی Membership

وقتی می نویسیم:

```python
"name" in student
```

Python بررسی می کند که `"name"` یک **Key** در Dictionary هست یا نه.

این نکته بسیار مهم است:

```python
20 in student
```

معمولاً نمی پرسد که آیا `20` یکی از Valueهاست.

برای Valueها:

```python
20 in student.values()
```

و برای Pairهای کامل:

```python
("age", 20) in student.items()
```

بنابراین Membership به این بستگی دارد که **کدام View از Dictionary** را بررسی می کنیم.

---

# ۹. طول Dictionary

```python
len(student)
```

تعداد Key-Value Pairها را برمی گرداند.

برای:

```python
student = {
    "name": "Ali",
    "age": 20,
    "city": "Baku"
}
```

نتیجه:

```text
3
```

این دستور تعداد Characterهای String یا تعداد Elementهای ساختارهای Nested را نمی شمارد.

تعداد Entryهای سطح اصلی Dictionary را برمی گرداند.

---

# ۱۰. پیمایش Dictionary

ساده ترین Loop:

```python
for key in student:
    print(key)
```

روی Keyها Iteration می کند.

برای Valueها:

```python
for value in student.values():
    print(value)
```

برای هر دو:

```python
for key, value in student.items():
    print(key, value)
```

این حالت بسیار مهم است، چون دقیقاً با ساختار اصلی Dictionary هماهنگ است:

```text
key → value
```

---

# ۱۱. Keys، Values و Items

سه View اصلی Dictionary:

```python
student.keys()
student.values()
student.items()
```

سه دیدگاه متفاوت نسبت به یک Dictionary هستند:

```text
Dictionary
   │
   ├── keys()   → Keyها
   │
   ├── values() → Valueها
   │
   └── items()  → Key-Value Pairها
```

این Viewها زمانی مهم می شوند که فقط بخشی از اطلاعات Dictionary را نیاز داشته باشیم.

---

# ۱۲. ترکیب و Update کردن Dictionaryها

فرض کنید:

```python
a = {
    "name": "Ali",
    "age": 20
}

b = {
    "city": "Baku",
    "age": 21
}
```

می توانیم:

```python
a.update(b)
```

را اجرا کنیم.

نتیجه:

```python
{
    "name": "Ali",
    "age": 21,
    "city": "Baku"
}
```

دقت کنید که `"age"` تغییر کرد.

وقتی دو Dictionary یک Key مشترک دارند، Value جدید جای Value قبلی را می گیرد.

این یک قانون مهم هنگام Merge کردن Dictionaryهاست.

---

# ۱۳. ترکیب Dictionaryها با `|`

در نسخه های جدید Python می توان از Union Operator استفاده کرد:

```python
a = {"name": "Ali"}
b = {"age": 20}

result = a | b
```

نتیجه:

```python
{
    "name": "Ali",
    "age": 20
}
```

تفاوت مهم با `update()`:

```python
a.update(b)
```

خود `a` را تغییر می دهد.

اما:

```python
result = a | b
```

یک Dictionary جدید ایجاد می کند.

---

# ۱۴. Nested Dictionaries

Dictionary می تواند Valueای داشته باشد که خودش یک Dictionary است:

```python
students = {
    "ali": {
        "age": 20,
        "city": "Baku"
    },
    "sara": {
        "age": 22,
        "city": "Ganja"
    }
}
```

در اینجا دسترسی مرحله ای است:

```python
students["ali"]["age"]
```

ابتدا:

```python
students["ali"]
```

یک Dictionary داخلی برمی گرداند.

سپس:

```python
["age"]
```

داده داخل آن Dictionary را انتخاب می کند.

مدل ذهنی:

```text
students
   ↓
"ali"
   ↓
Dictionary داخلی
   ↓
"age"
   ↓
20
```

این ساختار برای مدل کردن داده های واقعی و ساختاریافته بسیار قدرتمند است.

---

# ۱۵. Copy کردن Dictionary

این قسمت یکی از منابع رایج خطاست.

فرض کنید:

```python
original = {
    "numbers": [1, 2, 3]
}

copy = original.copy()
```

Dictionary بیرونی Copy شده است، اما List داخلی همچنان Shared است.

بنابراین:

```python
copy["numbers"].append(4)
```

می تواند روی:

```python
original["numbers"]
```

نیز اثر بگذارد.

اگر ساختار Nested کاملاً مستقل می خواهیم:

```python
from copy import deepcopy

copy = deepcopy(original)
```

تفاوت اصلی:

```text
copy()
```

→ Shallow Copy

```text
deepcopy()
```

→ Deep Copy

---

# ۱۶. تبدیل Dictionary

Dictionary را می توان به Representationهای مختلف تبدیل کرد.

Keyها:

```python
list(data.keys())
```

Valueها:

```python
list(data.values())
```

Items:

```python
list(data.items())
```

و Listای از Pairها می تواند دوباره Dictionary شود:

```python
pairs = [
    ("name", "Ali"),
    ("age", 20)
]

data = dict(pairs)
```

این تبدیل ها به ما اجازه می دهند Representation داده را با عملیات مورد نظر هماهنگ کنیم.

مثلاً:

```text
Dictionary → List of pairs → Sorting
```

در حالی که:

```text
List of pairs → Dictionary → Key-based lookup
```

---

# ۱۷. Dictionary و JSON

Dictionary یک Object در Python است.

JSON یک Data Format برای تبادل داده است.

این دو مرتبط هستند اما یکی نیستند.

Python Dictionary → JSON:

```python
import json

json_data = json.dumps(data)
```

JSON → Python Dictionary:

```python
data = json.loads(json_data)
```

این مفهوم در برنامه های واقعی بسیار مهم است، چون APIها معمولاً داده های ساختاریافته را با JSON منتقل می کنند.

---

# ۱۸. مهم ترین سؤال ها هنگام کار با Dictionary

وقتی با یک Dictionary مواجه می شوید، از خودتان بپرسید:

### Key چه چیزی را نمایندگی می کند؟

مثلاً:

```python
users["ali"]
```

آیا `"ali"` یک:

* ID است؟
* Username است؟
* Category است؟
* Database Identifier است؟

وقتی معنای Key مشخص باشد، ساختار راحت تر قابل درک است.

### Value چه چیزی را نمایش می دهد؟

آیا:

* Number است؟
* String است؟
* List است؟
* Dictionary دیگری است؟
* Object است؟

### آیا ممکن است Key وجود نداشته باشد؟

اگر بله، ممکن است:

```python
.get()
```

یا Membership Check مناسب باشد.

### آیا Keyها، Valueها یا هر دو را نیاز داریم؟

انتخاب کنید:

```python
.keys()
.values()
.items()
```

### آیا Dictionary اصلی را تغییر می دهیم؟

این موضوع هنگام انتخاب بین:

```python
update()
```

و:

```python
|
```

مهم است.

### آیا داده Nested است؟

اگر بله، باید بررسی کنیم آیا Shallow Copy کافی است یا به Deep Copy نیاز داریم.

---

# ۱۹. الگوی حل مسئله با Dictionary

بخش بزرگی از مسائل Dictionary را می توان با این فرآیند حل کرد:

```text
۱. مشخص کن چه چیزی داده را به صورت Unique شناسایی می کند.
                    ↓
۲. آن را به عنوان Key انتخاب کن.
                    ↓
۳. اطلاعات مرتبط را به عنوان Value ذخیره کن.
                    ↓
۴. بررسی کن آیا Key ممکن است وجود نداشته باشد.
                    ↓
۵. Lookup، Iteration، Update یا Removal مناسب را انتخاب کن.
                    ↓
۶. Representation مناسب برای عملیات بعدی را انتخاب کن.
```

مثلاً برای ذخیره Score دانش آموزان:

```python
scores = {
    "Ali": 85,
    "Sara": 95,
    "Reza": 78
}
```

نام دانش آموز Identifier است.

Score Value مربوط به آن Identifier است.

بنابراین:

```python
scores["Sara"]
```

یک عملیات طبیعی است.

---

# ۲۰. Dictionary به عنوان Lookup Structure

یکی از قدرتمندترین کاربردهای Dictionary، تبدیل جستجوهای تکراری به Lookup مستقیم است.

فرض کنید:

```python
names = ["Ali", "Sara", "Reza"]
scores = [85, 95, 78]
```

برای پیدا کردن Score مربوط به Sara باید رابطه بین Positionهای دو List را حفظ کنیم.

اما Dictionary این رابطه را مستقیم بیان می کند:

```python
scores = {
    "Ali": 85,
    "Sara": 95,
    "Reza": 78
}
```

حالا:

```python
scores["Sara"]
```

مستقیماً این رابطه را بیان می کند:

```text
Sara → 95
```

این دلیل عمیق اهمیت Dictionary است.

Dictionary فقط داده ذخیره نمی کند.

بلکه **رابطه بین Identifier و Information** را مدل می کند.

---

# ۲۱. Dictionary به عنوان ابزار Data Modeling

Dictionary می تواند یک مفهوم واقعی را مدل کند:

```python
user = {
    "username": "ali",
    "age": 20,
    "active": True
}
```

یک Product:

```python
product = {
    "name": "Laptop",
    "price": 1200,
    "stock": 15
}
```

یک Configuration:

```python
config = {
    "debug": True,
    "port": 8000,
    "host": "localhost"
}
```

یک رابطه:

```python
grades = {
    "math": 90,
    "python": 95,
    "english": 82
}
```

پس یادگیری Dictionary فقط یادگیری Syntax نیست.

این بخش در واقع مقدمه ای برای **Data Modeling** نیز محسوب می شود.

---

# ۲۲. تصویر بزرگ تر

Data Structureهای اصلی Python را می توان بر اساس مسئله ای که حل می کنند دید:

| Structure  | ایده اصلی               |
| ---------- | ----------------------- |
| List       | مجموعه مرتب             |
| Tuple      | مجموعه مرتب و Immutable |
| Set        | مجموعه Unique           |
| Dictionary | رابطه Key-Value         |

مهارت اصلی حفظ کردن همه متدها نیست.

سؤال مهم این است:

> داده من چه رابطه ای دارد و کدام Structure این رابطه را طبیعی تر نمایش می دهد؟

اگر جواب این باشد:

> «می خواهم اطلاعات را با یک Identifier پیدا کنم.»

Dictionary معمولاً انتخاب طبیعی است.

---

# مدل ذهنی نهایی

Dictionary را مانند یک سیستم از روابط دارای Label در نظر بگیرید:

```text
                 Dictionary
                     │
          ┌──────────┼──────────┐
          ↓          ↓          ↓
         Key        Key        Key
          ↓          ↓          ↓
       Value      Value      Value
```

حالا این مدل را به عملیات مختلف وصل کنید:

```text
Create
  ↓
Access
  ↓
Add / Update
  ↓
Check
  ↓
Iterate
  ↓
Remove
  ↓
Combine
  ↓
Nest
  ↓
Copy
  ↓
Convert
```

وقتی این مدل ذهنی را درک کنید، متدهای مختلف دیگر دستورات جدا از هم به نظر نمی رسند.

همه آن ها عملیات متفاوتی روی یک ایده واحد هستند:

> **Dictionary Keyها را به Valueها متصل می کند و به برنامه اجازه می دهد داده های مرتبط را به شکلی معنادار سازمان دهی، پیدا، تغییر و تبدیل کند.**

---

# سوالات مرور نهایی

## سوال ۱

تفاوت بنیادی دسترسی به یک List و یک Dictionary چیست؟

## سوال ۲

چرا:

```python
data[0]
```

لزوماً به معنی اولین Element یک Dictionary نیست؟

## سوال ۳

تفاوت:

```python
data[key]
```

و:

```python
data.get(key)
```

چیست؟

## سوال ۴

اگر مقداری را به Keyای که از قبل وجود دارد Assign کنیم چه اتفاقی می افتد؟

## سوال ۵

عبارت:

```python
key in data
```

دقیقاً چه چیزی را بررسی می کند؟

## سوال ۶

تفاوت این سه چیست؟

```python
data.keys()
data.values()
data.items()
```

## سوال ۷

چه زمانی Dictionary را به جای List انتخاب می کنیم؟

## سوال ۸

تفاوت:

```python
data.update(other)
```

و:

```python
result = data | other
```

چیست؟

## سوال ۹

چرا وقتی Dictionary شامل Mutable Objectهای Nested است، `copy()` ممکن است کافی نباشد؟

## سوال ۱۰

تفاوت Shallow Copy و Deep Copy چیست؟

## سوال ۱۱

هنگام تبدیل Valueهای Dictionary به Set چه اتفاقی برای Valueهای تکراری می افتد؟

## سوال ۱۲

چرا Listای از `(key, value)` Pairها می تواند به Dictionary تبدیل شود؟

---

# چالش جامع

داده زیر را در نظر بگیرید:

```python
students = {
    "ali": {
        "age": 20,
        "scores": [85, 90, 95]
    },
    "sara": {
        "age": 22,
        "scores": [92, 88, 96]
    }
}
```

برنامه ای بنویسید که:

1. سن Ali را استخراج کند.
2. یک دانش آموز جدید اضافه کند.
3. سن Sara را Update کند.
4. یک Score جدید به Ali اضافه کند.
5. بررسی کند آیا `"reza"` وجود دارد یا نه.
6. روی تمام دانش آموزان Iteration انجام دهد.
7. نام و Scoreهای هر دانش آموز را چاپ کند.
8. یک Shallow Copy از Dictionary ایجاد کند.
9. نشان دهد چرا تغییر یک List داخلی می تواند روی Dictionary اصلی اثر بگذارد.
10. یک Deep Copy ایجاد کند.
11. Entryهای سطح اصلی را به Listای از Tupleها تبدیل کند.
12. آن List را دوباره به Dictionary تبدیل کند.
13. Dictionary را به JSON تبدیل کند.
14. JSON را دوباره به Python Dictionary تبدیل کند.

هدف این تمرین فقط اجرای عملیات نیست.

باید بتوانید توضیح دهید:

* چرا Dictionary برای این داده مناسب است؛
* هر عملیات چه تغییری در Data Model ایجاد می کند؛
* و در چه شرایطی Copy یا Conversion می تواند رفتار یا ویژگی های داده را تغییر دهد.

---

# پروژه کوچک Dictionaries

## سیستم مدیریت دانش آموزان

در این پروژه کوچک، مفاهیمی که در بخش Dictionary یاد گرفتیم را در قالب یک برنامه کاربردی کنار هم قرار می دهیم.

هدف پروژه ساخت یک نرم افزار بزرگ یا پیچیده نیست.

هدف این است که یاد بگیریم چگونه با **منطق رابطه بین داده ها** فکر کنیم و Dictionary را به عنوان ساختار اصلی برای سازمان دهی و دسترسی به اطلاعات به کار ببریم.

---

## هدف پروژه

یک **Student Management System** ساده بسازید که اطلاعات چند دانش آموز را ذخیره کند.

هر دانش آموز باید دارای موارد زیر باشد:

* یک شناسه؛
* نام؛
* سن؛
* شهر؛
* مجموعه ای از نمرات.

ساختار اولیه می تواند به این شکل باشد:

```python
students = {
    "ali": {
        "name": "Ali",
        "age": 20,
        "city": "Baku",
        "scores": [85, 90, 95]
    },
    "sara": {
        "name": "Sara",
        "age": 22,
        "city": "Ganja",
        "scores": [92, 88, 96]
    }
}
```

به ساختار دقت کنید.

Dictionary بیرونی از شناسه دانش آموز به عنوان Key استفاده می کند:

```text
"ali"
"sara"
```

و Value مربوط به هر دانش آموز، خودش یک Dictionary دیگر است.

در Dictionary داخلی نیز اطلاعات دانش آموز ذخیره شده است.

Value مربوط به `"scores"` هم یک List است.

پس با یک ساختار چندلایه روبه رو هستیم:

```text
Dictionary
   │
   ├── Student ID
   │      │
   │      └── Student Dictionary
   │              │
   │              ├── name → String
   │              ├── age → Integer
   │              ├── city → String
   │              └── scores → List
   │
   └── Student ID
          │
          └── Student Dictionary
```

در نتیجه این پروژه چند Data Structure را به جای اینکه جدا از هم ببینیم، در یک مسئله واقعی با هم ترکیب می کند.

---

# بخش ۱ — نمایش اطلاعات دانش آموز

تابعی به شکل زیر ایجاد کنید:

```python
def show_student(student_id):
    pass
```

این تابع باید یک Student ID دریافت کند و اطلاعات آن دانش آموز را نمایش دهد.

مثلاً:

```python
show_student("ali")
```

می تواند چنین خروجی ای داشته باشد:

```text
Name: Ali
Age: 20
City: Baku
Scores: [85, 90, 95]
```

تابع باید حالتی را نیز مدیریت کند که دانش آموز مورد نظر وجود نداشته باشد.

---

# بخش ۲ — اضافه کردن دانش آموز

تابع زیر را ایجاد کنید:

```python
def add_student(student_id, name, age, city):
    pass
```

این تابع باید یک دانش آموز جدید به Dictionary اصلی اضافه کند.

مثلاً:

```python
add_student(
    "reza",
    "Reza",
    21,
    "Shaki"
)
```

بعد از اجرای این عملیات، `"reza"` باید به یک Key جدید در `students` تبدیل شود.

دانش آموز جدید باید در ابتدا دارای Score خالی باشد:

```python
"scores": []
```

حالا به این موضوع فکر کنید:

اگر Student ID از قبل وجود داشته باشد چه اتفاقی باید بیفتد؟

یک برنامه خوب نباید بدون اطلاع، اطلاعات دانش آموز قبلی را Overwrite کند.

---

# بخش ۳ — به روزرسانی اطلاعات دانش آموز

تابعی به شکل زیر ایجاد کنید:

```python
def update_student(student_id, age=None, city=None):
    pass
```

این تابع باید فقط اطلاعاتی را که کاربر ارائه کرده Update کند.

مثلاً:

```python
update_student("ali", city="Sumqayit")
```

باید شهر Ali را تغییر دهد، بدون اینکه سن یا Scoreهای او را تغییر دهد.

در این قسمت باید با دقت اطلاعات داخل Dictionary تو در تو را تغییر دهیم، بدون اینکه کل Record دانش آموز را ناخواسته جایگزین کنیم.

---

# بخش ۴ — اضافه کردن Score

تابع:

```python
def add_score(student_id, score):
    pass
```

را ایجاد کنید.

مثلاً:

```python
add_score("ali", 98)
```

باید:

```python
"scores": [85, 90, 95]
```

را به:

```python
"scores": [85, 90, 95, 98]
```

تبدیل کند.

این تابع نیز باید ابتدا بررسی کند که دانش آموز مورد نظر وجود دارد یا نه.

---

# بخش ۵ — محاسبه میانگین

تابع:

```python
def calculate_average(student_id):
    pass
```

را ایجاد کنید.

این تابع باید میانگین Scoreهای دانش آموز را محاسبه کند.

برای:

```python
[85, 90, 95]
```

میانگین برابر است با:

```text
90
```

اما یک حالت مهم وجود دارد:

اگر دانش آموز هنوز هیچ Scoreای نداشته باشد چه؟

برنامه باید این حالت را آگاهانه مدیریت کند، نه اینکه به یک خطای غیرمنتظره برسد.

---

# بخش ۶ — پیدا کردن بهترین دانش آموز

تابع:

```python
def find_top_student():
    pass
```

باید دانش آموزی را پیدا کند که بالاترین Average Score را دارد.

مثلاً اگر:

```text
Ali  → 90
Sara → 92
Reza → 88
```

تابع باید Sara را شناسایی کند.

این بخش مهم است، چون چند مفهوم را همزمان ترکیب می کند:

* Iteration روی Dictionary؛
* دسترسی به Dictionary داخلی؛
* پردازش List؛
* محاسبه؛
* مقایسه.

راه حل نباید به نام دانش آموزان خاص وابسته باشد.

---

# بخش ۷ — نمایش تمام دانش آموزان

تابع:

```python
def show_all_students():
    pass
```

را ایجاد کنید.

روی Dictionary اصلی Iteration انجام دهید و اطلاعات تمام دانش آموزان را نمایش دهید.

مثلاً:

```text
--- Ali ---
Age: 20
City: Baku
Scores: [85, 90, 95]

--- Sara ---
Age: 22
City: Ganja
Scores: [92, 88, 96]
```

این بخش فرصت خوبی برای تمرین:

```python
for student_id, student in students.items():
    ...
```

است.

به جای اینکه هر دانش آموز را به صورت دستی دسترسی بزنیم، باید ساختار را پیمایش کنیم.

---

# بخش ۸ — جستجوی دانش آموزان بر اساس شهر

تابع:

```python
def find_students_by_city(city):
    pass
```

را ایجاد کنید.

مثلاً:

```python
find_students_by_city("Baku")
```

باید تمام دانش آموزانی را که در Baku زندگی می کنند پیدا یا نمایش دهد.

این بخش نشان می دهد Dictionary فقط برای Direct Lookup استفاده نمی شود.

Dictionary ساختار اصلی داده را فراهم می کند و Iteration اجازه می دهد در میان Valueها جستجو کنیم.

---

# بخش ۹ — پیدا کردن دانش آموزان بالاتر از یک میانگین مشخص

تابع:

```python
def students_above_average(minimum):
    pass
```

را ایجاد کنید.

مثلاً:

```python
students_above_average(90)
```

باید دانش آموزانی را پیدا کند که Average Score آنها بزرگ تر یا مساوی `90` است.

در این بخش چند مفهوم به هم متصل می شوند:

```text
Dictionary Iteration
        ↓
Nested Data Access
        ↓
List Calculation
        ↓
Comparison
        ↓
Result Collection
```

---

# بخش ۱۰ — Copy کردن داده ها

یک Copy از Database دانش آموزان ایجاد کنید:

```python
students_copy = students.copy()
```

سپس یک Score داخل List تو در تو را تغییر دهید.

بررسی کنید آیا تغییر:

```python
students_copy["ali"]["scores"]
```

روی:

```python
students["ali"]["scores"]
```

نیز اثر می گذارد یا خیر.

سپس یک Copy کاملاً مستقل ایجاد کنید:

```python
from copy import deepcopy

students_copy = deepcopy(students)
```

و دوباره آزمایش را انجام دهید.

هدف این قسمت این است که تفاوت **Shallow Copy** و **Deep Copy** را به صورت عملی درک کنید، نه فقط به صورت تئوری.

---

# بخش ۱۱ — تبدیل داده ها

یک List ایجاد کنید که شامل Student ID و Name دانش آموزان باشد.

مثلاً:

```python
[
    ("ali", "Ali"),
    ("sara", "Sara"),
    ("reza", "Reza")
]
```

سپس این List را دوباره به Dictionary تبدیل کنید.

این بخش مفهوم Representationهای مختلف داده را تقویت می کند.

یک داده ممکن است بسته به عملیاتی که قرار است روی آن انجام دهیم، در شکل های مختلف مفید باشد.

---

# بخش ۱۲ — Export کردن به JSON

از ماژول `json` استفاده کنید:

```python
import json
```

Database دانش آموزان را به JSON تبدیل کنید:

```python
json_data = json.dumps(students, indent=4)
```

JSON تولید شده را نمایش دهید.

سپس آن را دوباره به Python Dictionary تبدیل کنید:

```python
restored_students = json.loads(json_data)
```

بررسی کنید که داده بازیابی شده همچنان قابل دسترسی باشد.

مثلاً:

```python
restored_students["ali"]["age"]
```

---

# بخش ۱۳ — ساخت Menu ساده

نسخه نهایی برنامه باید یک Menu متنی ساده داشته باشد:

```text
==============================
 Student Management System
==============================

1. Show student
2. Add student
3. Update student
4. Add score
5. Calculate average
6. Find top student
7. Show all students
8. Search by city
9. Find students above average
10. Export to JSON
0. Exit
```

کاربر باید بتواند چندین بار یک عملیات را انتخاب کند تا زمانی که گزینه `0` را انتخاب کند.

جریان کلی برنامه:

```text
Start
  ↓
Display menu
  ↓
Read choice
  ↓
Perform operation
  ↓
Display result
  ↓
Return to menu
  ↓
Exit when choice == 0
```

---

# الزامات پروژه

برنامه نهایی باید:

* از Dictionary به عنوان ساختار اصلی داده استفاده کند؛
* برای Record دانش آموزان از Nested Dictionary استفاده کند؛
* Scoreها را داخل List نگه دارد؛
* امکان اضافه کردن دانش آموز داشته باشد؛
* امکان Update اطلاعات دانش آموز داشته باشد؛
* امکان اضافه کردن Score داشته باشد؛
* Average Score را محاسبه کند؛
* بهترین دانش آموز را پیدا کند؛
* تمام دانش آموزان را نمایش دهد؛
* بر اساس شهر جستجو کند؛
* بر اساس Average Score فیلتر کند؛
* Shallow و Deep Copy را به صورت عملی نشان دهد؛
* بین Dictionary و List Representation تبدیل انجام دهد؛
* JSON را Serialize و Deserialize کند؛
* یک Menu تعاملی ساده داشته باشد؛
* Student IDهای ناموجود را به شکل مناسب مدیریت کند؛
* با استفاده از Functionها از تکرار غیرضروری جلوگیری کند.

---

# اصل مهم طراحی

سعی نکنید کل پروژه را داخل یک Block بزرگ از کد بنویسید.

برنامه را به مسئولیت های کوچک تقسیم کنید:

```text
show_student()
add_student()
update_student()
add_score()
calculate_average()
find_top_student()
show_all_students()
find_students_by_city()
students_above_average()
```

هر Function باید یک مسئولیت مشخص داشته باشد.

Dictionary نیز به عنوان Data Model مشترک عمل می کند که Functionها روی آن عملیات انجام می دهند.

درس مهم این پروژه این است:

> **یک Data Structure زمانی واقعاً قدرتمند می شود که طراحی برنامه بر اساس روابطی انجام شود که آن Structure نمایندگی می کند.**

---

# چالش های توسعه پروژه

بعد از اینکه نسخه اصلی پروژه را کامل کردید، سعی کنید آن را توسعه دهید.

### چالش ۱ — حذف دانش آموز

تابع:

```python
def remove_student(student_id):
    pass
```

را اضافه کنید.

حالت Student ID ناموجود را نیز مدیریت کنید.

### چالش ۲ — حذف Score

امکان حذف یک Score مشخص از List مربوط به دانش آموز را اضافه کنید.

### چالش ۳ — پیدا کردن بالاترین Score

بالاترین Score فردی را در میان تمام دانش آموزان پیدا کنید.

### چالش ۴ — مرتب سازی دانش آموزان

دانش آموزان را بر اساس Average Score مرتب نمایش دهید.

### چالش ۵ — پیدا کردن جوان ترین دانش آموز

دانش آموزی را پیدا کنید که کمترین سن را دارد.

### چالش ۶ — شمارش دانش آموزان بر اساس شهر

ساختاری مانند زیر تولید کنید:

```python
{
    "Baku": 3,
    "Ganja": 2,
    "Shaki": 1
}
```

این تمرین مهم است، چون ایده استفاده از Dictionary برای **Counting Occurrences** را تقویت می کند.

### چالش ۷ — ذخیره در فایل

JSON را داخل یک فایل ذخیره کنید و هنگام اجرای برنامه دوباره آن را Load کنید.

---

# بعد از این پروژه باید چه چیزی را بفهمید؟

بعد از تکمیل پروژه، باید بتوانید هنگام مواجه شدن با یک مسئله این سؤال ها را از خودتان بپرسید:

1. چه اطلاعاتی باید ذخیره شود؟
2. چه چیزی هر بخش از اطلاعات را به صورت Unique شناسایی می کند؟
3. کدام داده باید Key باشد؟
4. کدام داده باید Value باشد؟
5. کدام Value به ساختار Nested نیاز دارد؟
6. چه زمانی باید داخل Dictionary از List استفاده کنیم؟
7. چه زمانی Direct Lookup مناسب است؟
8. چه زمانی باید Iteration انجام دهیم؟
9. چه زمانی باید داده را Copy کنیم؟
10. چه زمانی باید Representation داده را تغییر دهیم؟

اگر بتوانید به این سؤال ها پاسخ دهید، دیگر فقط Syntax مربوط به Dictionary را حفظ نکرده اید.

شما در حال یادگیری استفاده از Dictionary به عنوان یک **ابزار Data Modeling و Problem Solving** هستید.

---

