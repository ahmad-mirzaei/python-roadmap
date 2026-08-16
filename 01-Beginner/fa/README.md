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

