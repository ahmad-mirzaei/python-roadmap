# Lesson — Strings & Sequences

> 🌐 language: **فارسی** | [English](../README.md)

# بخش ۱ — رشته چیست؟ (`Strings`)

تا اینجا با متغیرها، انواع داده، ورودی گرفتن، شرط ها، حلقه ها و تابع ها آشنا شده ایم.

حالا می خواهیم با یکی از پرکاربردترین انواع داده در پایتون آشنا شویم:

**String**

تقریباً هر برنامه واقعی با متن سر و کار دارد:

* نام کاربر
* نام شهر
* ایمیل
* رمز عبور
* پیام
* فایل متنی
* اطلاعات فرم ها
* خروجی برنامه

بنابراین یادگیری String فقط یادگیری چند دستور نیست؛ بلکه یکی از پایه های اصلی کار با داده در پایتون است.

---

## 1. String چیست؟

یک `String` یا **رشته** دنباله ای مرتب از کاراکترهاست.

برای مثال:

```python
name = "Python"
```

در اینجا:

```text
Python
```

یک String است.

هر چیزی که داخل `' '` یا `" "` قرار بگیرد، می تواند یک String باشد.

مثلاً:

```python
language = "Python"
country = "Iran"
message = "Hello World!"
```

---

## 2. Character چیست؟

هر String از واحدهای کوچک تری به نام **Character** ساخته شده است.

مثلاً:

```python
word = "Python"
```

این String شامل این کاراکترهاست:

```text
P   y   t   h   o   n
```

یعنی:

* `P` یک Character است.
* `y` یک Character است.
* `t` یک Character است.
* و به همین شکل ادامه دارد.

فاصله هم یک Character محسوب می شود.

مثلاً:

```python
text = "Hello World"
```

بین `Hello` و `World` یک فاصله وجود دارد و آن فاصله نیز بخشی از String است.

---

## 3. String فقط شامل حروف نیست

String می تواند تقریباً هر نوع Character متنی را در خود داشته باشد.

### حروف

```python
text = "Python"
```

### اعداد

```python
text = "12345"
```

نکته مهم:

`"12345"` یک String است، نه یک عدد.

در مقابل:

```python
number = 12345
```

یک عدد صحیح است.

### ترکیب حروف و اعداد

```python
code = "A123"
```

### فاصله

```python
message = "Hello World"
```

### نمادها

```python
symbol = "@#$%"
```

حتی می توان همه این ها را ترکیب کرد:

```python
text = "User_123 @ Python!"
```

---

# 4. تفاوت `"123"` و `123`

این یکی از مهم ترین نکات این بخش است.

به این دو مقدار نگاه کنید:

```python
a = 123
b = "123"
```

ممکن است از نظر ظاهری شبیه باشند، اما از نظر پایتون کاملاً متفاوت هستند.

`a` یک عدد است:

```python
123
```

اما `b` یک String است:

```python
"123"
```

به همین دلیل:

```python
print(a + 10)
```

نتیجه:

```text
133
```

اما:

```python
print(b + "10")
```

نتیجه:

```text
12310
```

چون در حالت دوم پایتون دو String را به هم متصل می کند.

اما این کار مجاز نیست:

```python
print(b + 10)
```

چون یک طرف String و طرف دیگر عدد است.

اگر بخواهیم `"123"` را به عدد تبدیل کنیم، می توانیم از `int()` استفاده کنیم:

```python
b = "123"

number = int(b)

print(number + 10)
```

خروجی:

```text
133
```

پس همیشه به این سؤال توجه کنید:

> آیا این مقدار واقعاً عدد است یا فقط متنی است که از کاراکترهای عددی ساخته شده؟

---

# 5. نوع داده String

پایتون برای String یک نوع داده مخصوص دارد:

```text
str
```

مثلاً:

```python
name = "Python"

print(type(name))
```

خروجی:

```text
<class 'str'>
```

اینجا `type()` بسیار مهم است.

---

# 6. `type()` دقیقاً چه کاری انجام می دهد؟

تابع `type()` به ما می گوید یک مقدار از چه **نوع داده ای** است.

مثلاً:

```python
print(type(10))
```

خروجی:

```text
<class 'int'>
```

عدد اعشاری:

```python
print(type(10.5))
```

خروجی:

```text
<class 'float'>
```

رشته:

```python
print(type("10"))
```

خروجی:

```text
<class 'str'>
```

مقدار منطقی:

```python
print(type(True))
```

خروجی:

```text
<class 'bool'>
```

---

## چرا `type()` مهم است؟

گاهی برنامه دقیقاً آن چیزی را که ما فکر می کنیم دریافت نمی کند.

مثلاً:

```python
age = input("Enter your age: ")

print(type(age))
```

حتی اگر کاربر وارد کند:

```text
20
```

خروجی این است:

```text
<class 'str'>
```

چرا؟

چون `input()` ورودی کاربر را به صورت String برمی گرداند.

یعنی:

```python
age = input(...)
```

در واقع چیزی شبیه این داریم:

```python
age = "20"
```

نه:

```python
age = 20
```

این تفاوت بسیار مهم است.

---

## یک مثال مهم

فرض کنید می خواهیم سن کاربر را بگیریم:

```python
age = input("Enter your age: ")

print(age + 5)
```

این کد خطا می دهد.

چون:

```text
"20" + 5
```

معنای مشخصی برای پایتون ندارد.

باید String را به عدد تبدیل کنیم:

```python
age = int(input("Enter your age: "))

print(age + 5)
```

حالا اگر کاربر `20` وارد کند:

```text
25
```

پس یک الگوی بسیار مهم داریم:

```python
int(input(...))
```

یعنی:

1. ورودی را دریافت کن.
2. آن را به عدد صحیح تبدیل کن.
3. در متغیر ذخیره کن.

---

# 7. String خالی

یک String می تواند هیچ Character نداشته باشد:

```python
text = ""
```

این یک **Empty String** است.

دقت کنید:

```python
text = ""
```

با:

```python
text = " "
```

یکی نیست.

اولی هیچ Character ندارد.

دومی یک Character دارد و آن Character یک فاصله است.

---

# 8. String یک Sequence است

یکی از مهم ترین ویژگی های String این است که یک **Sequence** است.

یعنی Characterها ترتیب مشخصی دارند.

مثلاً:

```python
word = "Python"
```

از نظر مفهومی:

```text
P   y   t   h   o   n
```

ترتیب مهم است.

این دو String با هم برابر نیستند:

```python
"Python"
"nohtyP"
```

هر دو از همان Characterها ساخته شده اند، اما ترتیبشان متفاوت است.

همین ویژگی Sequence بودن باعث می شود بتوانیم:

* به Character خاصی دسترسی پیدا کنیم.
* String را برش بزنیم.
* روی آن حلقه اجرا کنیم.
* طول آن را پیدا کنیم.

این مفاهیم را در بخش های بعدی یاد می گیریم.

---

# 9. Index چیست؟

چون String یک Sequence است، هر Character یک موقعیت دارد.

مثلاً:

```python
word = "Python"
```

می توانیم موقعیت ها را این طور تصور کنیم:

```text
Character:  P   y   t   h   o   n
Index:      0   1   2   3   4   5
```

دقت کنید:

**Index از صفر شروع می شود.**

پس اولین Character در Index شماره `0` قرار دارد.

دومین Character در Index شماره `1`.

و آخرین Character در Index شماره `5`.

در بخش بعدی به صورت کامل با Indexing کار خواهیم کرد.

---

# 10. Stringها Immutable هستند

یک ویژگی مهم دیگر Stringها این است که در پایتون **Immutable** هستند.

Immutable یعنی:

> بعد از ساخته شدن String، نمی توانیم Characterهای آن را مستقیماً تغییر دهیم.

مثلاً:

```python
word = "Python"

word[0] = "J"
```

این کار خطا ایجاد می کند.

دلیلش این است که String قابل تغییر مستقیم نیست.

اما می توانیم یک String جدید بسازیم:

```python
word = "J" + word[1:]

print(word)
```

خروجی:

```text
Jython
```

در این حالت String قبلی را تغییر نداده ایم.

یک String جدید ساخته ایم.

این مفهوم در زمان کار با Slicing و متدهای String بسیار مهم خواهد بود.

---

# 11. یک مثال واقعی

فرض کنید می خواهیم اطلاعات ساده یک کاربر را نگه داریم:

```python
name = "Ali"
city = "Tehran"
username = "ali123"
```

هر سه مقدار String هستند.

حالا:

```python
print(type(name))
print(type(city))
print(type(username))
```

خروجی:

```text
<class 'str'>
<class 'str'>
<class 'str'>
```

اما اگر داشته باشیم:

```python
age = 25
```

نوع آن:

```text
<class 'int'>
```

پس در یک برنامه واقعی، ممکن است چند نوع داده مختلف کنار هم داشته باشیم.

---

# تمرین های کوتاه

### تمرین ۱

نوع داده هر کدام را حدس بزنید:

```python
a = "100"
b = 100
c = 10.5
d = True
e = "True"
```

قبل از اجرای کد، نوع هر متغیر را حدس بزنید.

---

### تمرین ۲

بدون اجرای کد، نتیجه را حدس بزنید:

```python
x = "10"
y = "20"

print(x + y)
```

سپس همین کار را با:

```python
x = 10
y = 20
```

انجام دهید.

تفاوت را توضیح دهید.

---

### تمرین ۳

برنامه ای بنویسید که نام کاربر را دریافت کند و این موارد را چاپ کند:

```text
Name:
Type:
```

---

### تمرین ۴

برنامه ای بنویسید که سن کاربر را دریافت کند و سن او را در ۵ سال آینده نمایش دهد.

---

# سؤال ترکیبی پایان بخش

حالا یک مسئله داریم که فقط درباره String نیست.

برنامه ای بنویسید که اطلاعات زیر را از کاربر دریافت کند:

* نام
* سن
* شهر

سپس برنامه باید:

1. نام را دریافت کند.
2. سن را به شکل مناسب دریافت کند.
3. شهر را دریافت کند.
4. نوع داده هر سه مقدار را بررسی کند.
5. یک پیام معرفی برای کاربر نمایش دهد.
6. مشخص کند آیا کاربر بزرگسال است یا خیر.
7. برنامه این کار را داخل یک **تابع** انجام دهد.
8. در پایان از کاربر بپرسد آیا می خواهد اطلاعات کاربر دیگری را وارد کند یا نه.

### نمونه اجرا

```text
Enter your name: Ali
Enter your age: 22
Enter your city: Tehran

Name: Ali
Age: 22
City: Tehran

You are an adult.

Add another user? yes
```

### هدف

در این سؤال هنوز با Indexing یا Slicing کاری نداریم.

هدف این است که مفاهیم قبلی را با مفهوم جدید **String و `type()`** ترکیب کنید.

قبل از نوشتن کد، ابتدا مسئله را به چند مرحله تقسیم کنید و الگوریتم خودتان را بنویسید.

---

# بخش ۲ — ساخت رشته ها و کار با علامت های نقل قول

در بخش ۱ یاد گرفتیم String چیست، پایتون چگونه آن را با نوع `str` می شناسد، چرا `input()` مقدار String برمی گرداند و چرا Stringها یک Sequence هستند.

حالا می خواهیم یاد بگیریم چگونه Stringها را درست بسازیم و علامت های نقل قول و Escape Characterها چگونه کار می کنند.

---

## ۱. ساخت یک String

ساده ترین روش ساخت String این است که متن را داخل علامت نقل قول قرار دهیم.

در پایتون می توانیم از نقل قول تکی استفاده کنیم:

```python
name = 'Ali'
```

یا از نقل قول دوتایی:

```python
name = "Ali"
```

هر دو یک String می سازند:

```python
print(type(name))
```

خروجی:

```text
<class 'str'>
```

انتخاب بین نقل قول تکی و دوتایی معمولاً به این بستگی دارد که کدام روش خوانایی کد را بیشتر کند.

---

## ۲. نقل قول تکی و دوتایی

این دو String دقیقاً یک متن دارند:

```python
a = "Python"
b = 'Python'
```

می توانیم این موضوع را بررسی کنیم:

```python
print(a == b)
```

خروجی:

```text
True
```

پس پایتون یکی را بیشتر از دیگری String نمی داند.

نکته مهم این است که علامت شروع و پایان String باید با هم هماهنگ باشند.

درست:

```python
name = "Ali"
```

درست:

```python
name = 'Ali'
```

اما این اشتباه است:

```python
name = "Ali'
```

علامت های نقل قول به درستی جفت نشده اند.

---

## ۳. چرا دو نوع نقل قول داریم؟

مزیت واقعی این دو روش زمانی مشخص می شود که خود علامت نقل قول بخشی از متن باشد.

فرض کنید می خواهیم این جمله را ذخیره کنیم:

```text
Python is "easy" to learn.
```

می توانیم از نقل قول تکی در بیرون استفاده کنیم:

```python
message = 'Python is "easy" to learn.'
```

این کار درست است، چون پایتون نقل قول های تکی بیرونی را مرز String در نظر می گیرد.

می توانیم برعکس هم عمل کنیم:

```python
message = "Python is 'easy' to learn."
```

این یکی از ساده ترین روش ها برای جلوگیری از Escape کردن غیر ضروری است.

---

## ۴. قرار دادن نقل قول داخل String

فرض کنید می خواهیم این جمله را ذخیره کنیم:

```text
Ali said "Hello".
```

می توانیم بنویسیم:

```python
message = 'Ali said "Hello".'
```

یا:

```python
message = "Ali said \"Hello\"."
```

هر دو این خروجی را ایجاد می کنند:

```text
Ali said "Hello".
```

در مثال دوم با مفهوم مهمی به نام **Escape Character** روبرو می شویم.

---

# ۵. Escape Character چیست؟

Escape Character به ما اجازه می دهد کاراکترهایی را داخل String قرار دهیم که ممکن است در حالت عادی برای پایتون معنای خاصی داشته باشند.

Escape Character در پایتون:

```text
\
```

است.

یک Backslash در کنار کاراکتر بعد از خودش می تواند یک Escape Sequence ایجاد کند.

چند مورد پرکاربرد:

| Escape Sequence | معنی                 |
| --------------- | -------------------- |
| `\n`            | رفتن به خط بعد       |
| `\t`            | ایجاد فاصله Tab      |
| `\\`            | نمایش Backslash      |
| `\"`            | نمایش نقل قول دوتایی |
| `\'`            | نمایش نقل قول تکی    |

حالا هر کدام را جداگانه بررسی کنیم.

---

# ۶. رفتن به خط بعد — `\n`

در حالت عادی:

```python
print("Hello Python")
```

خروجی:

```text
Hello Python
```

اما `\n` به پایتون می گوید از خط جدید ادامه بدهد:

```python
print("Hello\nPython")
```

خروجی:

```text
Hello
Python
```

توجه کنید که `\n` خودش در خروجی نمایش داده نمی شود.

این عبارت در واقع یک دستور برای ایجاد خط جدید است.

---

## یک مثال کاربردی تر

```python
print("Name: Ali\nAge: 20\nCity: Tehran")
```

خروجی:

```text
Name: Ali
Age: 20
City: Tehran
```

این روش زمانی مفید است که بخواهیم اطلاعات را بدون استفاده از چند `print()` جداگانه، در چند خط نمایش دهیم.

---

# ۷. فاصله Tab — `\t`

Escape Sequence دیگری که زیاد استفاده می شود:

```text
\t
```

است.

این دستور یک فاصله Tab ایجاد می کند.

مثلاً:

```python
print("Name:\tAli")
```

خروجی چیزی شبیه این خواهد بود:

```text
Name:   Ali
```

یکی از کاربردهای خوب آن ساختن ستون های ساده است:

```python
print("Name\tAge")
print("Ali\t20")
print("Sara\t22")
```

خروجی:

```text
Name    Age
Ali     20
Sara    22
```

اندازه دقیق فاصله Tab می تواند به محیط اجرای برنامه بستگی داشته باشد، اما مفهوم آن این است که متن را به موقعیت Tab بعدی منتقل می کند.

---

# ۸. نقل قول دوتایی — `\"`

فرض کنید String ما خودش با نقل قول دوتایی ساخته شده است و می خواهیم داخل آن هم از نقل قول دوتایی استفاده کنیم.

این کد مشکل دارد:

```python
message = "Python is "easy" to learn."
```

پایتون نقل قول دوم را به عنوان پایان String در نظر می گیرد.

راه حل:

```python
message = "Python is \"easy\" to learn."
```

حالا علامت های نقل قول داخلی بخشی از متن هستند.

خروجی:

```text
Python is "easy" to learn.
```

---

# ۹. نقل قول تکی — `\'`

همین موضوع برای نقل قول تکی هم وجود دارد.

این کد مشکل دارد:

```python
message = 'Python's syntax is simple.'
```

پایتون تصور می کند String بعد از `Python` تمام شده است.

می توانیم علامت `'` را Escape کنیم:

```python
message = 'Python\'s syntax is simple.'
```

خروجی:

```text
Python's syntax is simple.
```

اما یک راه ساده تر هم وجود دارد:

```python
message = "Python's syntax is simple."
```

اینجا چون String با نقل قول دوتایی شروع شده است، نقل قول تکی داخل آن مشکلی ایجاد نمی کند.

---

# ۱۰. نمایش Backslash — `\\`

چون Backslash در پایتون معنای خاص دارد، وقتی بخواهیم خود Backslash را نمایش دهیم، باید آن را Escape کنیم.

فرض کنید می خواهیم این مسیر را نمایش دهیم:

```text
C:\Users\Ali
```

می توانیم بنویسیم:

```python
path = "C:\\Users\\Ali"

print(path)
```

خروجی:

```text
C:\Users\Ali
```

هر `\\` در خروجی به یک Backslash تبدیل می شود.

---

# ۱۱. چرا پایتون به Escape Character نیاز دارد؟

پایتون باید بتواند بین دو حالت تفاوت بگذارد:

**کاراکترهایی که واقعاً بخشی از متن هستند**

و

**کاراکترهایی که دستور یا رفتار خاصی ایجاد می کنند.**

مثلاً:

```python
"\n"
```

به معنی دو کاراکتر قابل مشاهده `\` و `n` نیست.

این عبارت نمایانگر یک کاراکتر خط جدید است.

همین طور:

```python
"\""
```

نمایانگر یک علامت نقل قول دوتایی داخل String است.

درک این تفاوت بعدها هنگام کار با فایل ها، مسیر فایل ها، متن های قالب بندی شده و Regular Expressionها بسیار مهم خواهد شد.

---

# ۱۲. String چند خطی

گاهی لازم است یک String شامل چند خط باشد.

پایتون برای این کار امکان استفاده از سه نقل قول را فراهم می کند:

```python
message = """
Hello
Welcome to Python
Have a great day!
"""
```

در این حالت String می تواند در چند خط ادامه پیدا کند.

این روش برای مواردی مثل موارد زیر کاربرد دارد:

* پیام های طولانی
* متن های چند خطی
* Documentation
* بخش های بزرگ متن

می توانیم از سه نقل قول دوتایی استفاده کنیم:

```python
message = """
Hello
Python
"""
```

یا سه نقل قول تکی:

```python
message = '''
Hello
Python
'''
```

هر دو روش معتبر هستند.

---

# ۱۳. یک اشتباه رایج

به این دو مثال دقت کنید:

```python
text = "Hello\nWorld"
```

در اینجا `\n` یک دستور برای رفتن به خط بعد است.

اما:

```python
text = "Hello\\nWorld"
```

در اینجا Backslash را Escape کرده ایم.

بنابراین خروجی:

```text
Hello\nWorld
```

خواهد بود.

تفاوت را به شکل ساده ببینیم.

### حالت اول:

```python
"Hello\nWorld"
```

یعنی:

```text
Hello
World
```

### حالت دوم:

```python
"Hello\\nWorld"
```

یعنی متن:

```text
Hello\nWorld
```

پس `\\` باعث می شود خود Backslash را داشته باشیم، نه اینکه آن Backslash بخشی از یک Escape Sequence باشد.

---

# ۱۴. ترکیب چند مفهوم

می توانیم متغیرها، Stringها، Escape Characterها و `print()` را با هم ترکیب کنیم.

مثلاً:

```python
name = "Ali"
age = 20
city = "Tehran"

print("Name:\t" + name)
print("Age:\t" + str(age))
print("City:\t" + city)
```

خروجی:

```text
Name:   Ali
Age:    20
City:   Tehran
```

اینجا یک نکته مهم وجود دارد.

`age` یک عدد صحیح است.

بنابراین اگر بخواهیم آن را با یک String با استفاده از `+` ترکیب کنیم، باید آن را به String تبدیل کنیم:

```python
str(age)
```

این دقیقاً به بحث انواع داده در بخش ۱ مربوط می شود.

---

# تمرین های کوتاه

## تمرین ۱ — خروجی را حدس بزنید

بدون اجرای کد، خروجی را حدس بزنید:

```python
print("Python\nStrings")
```

---

## تمرین ۲ — String را اصلاح کنید

کد زیر را اصلاح کنید:

```python
message = "Python is "easy" to learn."
```

خروجی باید این باشد:

```text
Python is "easy" to learn.
```

---

## تمرین ۳ — Apostrophe

کد زیر را اصلاح کنید:

```python
message = 'I don't like bugs.'
```

برنامه باید این خروجی را چاپ کند:

```text
I don't like bugs.
```

---

## تمرین ۴ — قالب بندی

برنامه ای بنویسید که این خروجی را تولید کند:

```text
Name:   Ali
Age:    20
City:   Tehran
```

از `\t` استفاده کنید.

---

## تمرین ۵ — String چند خطی

یک String بسازید که خروجی زیر را تولید کند:

```text
Welcome to Python!

Today we are learning Strings.
```

از `\n` استفاده کنید.

---

## تمرین ۶ — مسیر فایل

یک String بسازید که این متن را چاپ کند:

```text
C:\Python\Projects\Lesson1
```

دقت کنید که Backslashها به درستی نمایش داده شوند.

---

# سؤال ترکیبی پایان بخش

حالا مفاهیم درس های قبلی را با مطالب این بخش ترکیب کنید.

برنامه ای بنویسید که:

1. داخل یک تابع قرار داشته باشد.
2. نام کاربر را دریافت کند.
3. سن کاربر را دریافت کند.
4. سن را به نوع داده مناسب تبدیل کند.
5. شهر کاربر را دریافت کند.
6. بررسی کند که آیا کاربر بزرگسال است یا نه.
7. یک پیام چند خطی و مرتب برای کاربر بسازد.
8. در خروجی از `\n` و `\t` استفاده کند.
9. از کاربر بپرسد آیا می خواهد کاربر دیگری را وارد کند یا نه.
10. تا زمانی که کاربر تصمیم به توقف نگرفته است، ادامه پیدا کند.

نمونه خروجی:

```text
Name:   Ali
Age:    22
City:   Tehran

Status: Adult

Add another user? yes
```

### نکته مهم

کد نمونه را مستقیماً کپی نکنید.

ابتدا مسئله را به مراحل کوچک تر تقسیم کنید و **الگوریتم خودتان را بنویسید**.

هدف این تمرین فقط کار با String نیست.

در این مسئله باید چند مفهوم را با هم ترکیب کنید:

* متغیرها
* `input()`
* تبدیل نوع داده
* String
* `print()`
* شرط ها
* حلقه ها
* تابع ها

این دقیقاً همان نوع تفکری است که در ادامه کتاب برای حل مسئله های بزرگ تر به آن نیاز خواهید داشت.

---

# آنچه در این بخش یاد گرفتیم

در این بخش یاد گرفتیم:

* چگونه String بسازیم
* تفاوت نقل قول تکی و دوتایی
* قرار دادن نقل قول داخل String
* Escape Character
* `\n`
* `\t`
* `\\`
* `\"`
* `\'`
* Stringهای چند خطی
* قالب بندی متن با Escape Sequenceها
* ترکیب String با متغیرها
* تبدیل مقدار به String با `str()`

در بخش بعدی، سراغ **Indexing** می رویم و یاد می گیریم چگونه به یک Character مشخص داخل String دسترسی پیدا کنیم.

---

# بخش ۳ — Indexing در String

در بخش های قبلی یاد گرفتیم String چیست و چگونه با استفاده از انواع مختلف علامت های نقل قول آن را ایجاد کنیم.

همچنین با Escape Characterهایی مانند `\n`، `\t`، `\\`، `\"` و `\'` آشنا شدیم.

حالا می خواهیم یکی از مهم ترین قابلیت های String را یاد بگیریم:

**Indexing**

Indexing به ما اجازه می دهد به Characterهای جداگانه داخل یک String دسترسی پیدا کنیم.

---

## ۱. Indexing چیست؟

یک String مجموعه ای مرتب از Characterهاست.

برای مثال:

```python
word = "Python"
```

می توانیم آن را این طور تصور کنیم:

```text
P   y   t   h   o   n
```

هر Character یک موقعیت مشخص دارد.

در پایتون به این موقعیت ها **Index** گفته می شود.

قانون بسیار مهم:

> پایتون شمارش Indexها را از `0` شروع می کند.

بنابراین:

```text
Character:  P   y   t   h   o   n
Index:      0   1   2   3   4   5
```

اولین Character در Index شماره `0` قرار دارد، نه `1`.

---

## ۲. دسترسی به یک Character

برای دسترسی به یک Character مشخص، از براکت استفاده می کنیم:

```python
word[index]
```

مثلاً:

```python
word = "Python"

print(word[0])
```

خروجی:

```text
P
```

Character دوم:

```python
print(word[1])
```

خروجی:

```text
y
```

Character سوم:

```python
print(word[2])
```

خروجی:

```text
t
```

و به همین ترتیب می توانیم به Characterهای دیگر دسترسی داشته باشیم.

---

## ۳. چرا Index از صفر شروع می شود؟

ممکن است در ابتدا این سؤال پیش بیاید:

چرا اولین Character شماره `1` نیست؟

یکی از راه های ساده برای درک این موضوع این است که Index را به عنوان **تعداد قدم هایی که از ابتدای String حرکت کرده ایم** در نظر بگیریم.

برای رسیدن به اولین Character، هنوز هیچ قدمی برنداشته ایم.

پس:

```text
اولین Character → 0 قدم
دومین Character → 1 قدم
سومین Character → 2 قدم
```

بنابراین:

```text
Index:      0   1   2   3   4   5
Character:  P   y   t   h   o   n
```

این نوع شمارش در بسیاری از زبان های برنامه نویسی و ساختارهای داده رایج است.

---

## ۴. دسترسی به اولین Character

چون Index از صفر شروع می شود، برای گرفتن اولین Character کافی است بنویسیم:

```python
word = "Python"

print(word[0])
```

خروجی:

```text
P
```

بنابراین یک الگوی بسیار مهم داریم:

```python
text[0]
```

یعنی:

> اولین Character از `text`

---

## ۵. دسترسی به آخرین Character

می توانیم Index آخرین Character را به صورت دستی پیدا کنیم.

برای `"Python"`:

```text
P   y   t   h   o   n
0   1   2   3   4   5
```

پس:

```python
print(word[5])
```

خروجی:

```text
n
```

اما این روش چندان کاربردی نیست.

فرض کنید String تغییر کند:

```python
word = "Programming"
```

حالا باید دوباره Index آخرین Character را حساب کنیم.

پایتون راه بهتری برای این کار دارد:

**Negative Indexing**

---

## ۶. Negative Indexing

پایتون اجازه می دهد از انتهای String نیز شمارش کنیم.

برای مثال:

```text
Character:  P    y    t    h    o    n
Positive:   0    1    2    3    4    5
Negative:  -6   -5   -4   -3   -2   -1
```

آخرین Character همیشه Index زیر را دارد:

```python
-1
```

بنابراین:

```python
word = "Python"

print(word[-1])
```

خروجی:

```text
n
```

Character قبل از آن:

```python
print(word[-2])
```

خروجی:

```text
o
```

و:

```python
print(word[-3])
```

خروجی:

```text
h
```

Negative Indexing زمانی بسیار کاربردی است که بخواهیم به Characterهای انتهای String دسترسی داشته باشیم.

---

## ۷. استفاده همزمان از Positive و Negative Indexing

برای String زیر:

```python
word = "Python"
```

می توانیم تمام Indexها را این طور نمایش دهیم:

```text
             P    y    t    h    o    n
Positive:    0    1    2    3    4    5
Negative:   -6   -5   -4   -3   -2   -1
```

بنابراین:

```python
word[0] == word[-6]
```

هر دو به `P` اشاره می کنند.

همچنین:

```python
word[5] == word[-1]
```

هر دو به `n` اشاره می کنند.

---

## ۸. تابع `len()`

گاهی نمی دانیم یک String چند Character دارد.

برای پیدا کردن طول String از تابع:

```python
len()
```

استفاده می کنیم.

مثلاً:

```python
word = "Python"

print(len(word))
```

خروجی:

```text
6
```

چون `"Python"` شامل شش Character است.

---

## ۹. تفاوت `len()` و Index

این تفاوت بسیار مهم است.

برای:

```python
word = "Python"
```

عبارت:

```python
len(word)
```

مقدار:

```text
6
```

را برمی گرداند.

اما آخرین Index برابر است با:

```text
5
```

چرا؟

چون `len()` تعداد Characterها را می شمارد:

```text
6 Character
```

اما Indexها از صفر شروع می شوند:

```text
0 1 2 3 4 5
```

بنابراین یک قانون مهم داریم:

> آخرین Index برابر است با `len(string) - 1`

مثلاً:

```python
word = "Python"

print(word[len(word) - 1])
```

خروجی:

```text
n
```

این الگو در کار با Stringها بسیار مهم است.

---

## ۱۰. پیدا کردن آخرین Character با `len()`

به جای اینکه بنویسیم:

```python
word[5]
```

می توانیم بنویسیم:

```python
word[len(word) - 1]
```

مزیت این روش این است که به طول مشخصی وابسته نیست.

مثلاً:

```python
word = "Programming"

print(word[len(word) - 1])
```

خروجی:

```text
g
```

بدون اینکه از قبل بدانیم String چند Character دارد.

---

## ۱۱. Indexing روی ورودی کاربر

Indexing زمانی کاربردی تر می شود که با اطلاعاتی کار کنیم که کاربر وارد می کند.

مثلاً:

```python
name = input("Enter your name: ")

print(name[0])
```

اگر کاربر وارد کند:

```text
Ali
```

خروجی:

```text
A
```

می توانیم آخرین Character را هم بگیریم:

```python
print(name[-1])
```

خروجی:

```text
i
```

حالا برنامه می تواند روی اطلاعات واقعی که کاربر وارد کرده است کار کند.

---

## ۱۲. Indexing باعث تغییر String نمی شود

وقتی می نویسیم:

```python
word = "Python"

letter = word[0]
```

فقط Character را می خوانیم.

String اصلی تغییر نمی کند.

اگر بنویسیم:

```python
print(word)
```

همچنان خواهیم داشت:

```text
Python
```

این موضوع با چیزی که در بخش قبلی درباره **Immutable بودن String** یاد گرفتیم ارتباط مستقیم دارد.

---

## ۱۳. نمی توانیم یک Index را مستقیماً تغییر دهیم

چون Stringها Immutable هستند، این کار مجاز نیست:

```python
word = "Python"

word[0] = "J"
```

پایتون خطا می دهد.

ما نمی توانیم یک Character را مستقیماً داخل String موجود جایگزین کنیم.

در عوض باید یک String جدید بسازیم.

مثلاً:

```python
word = "Python"

word = "J" + word[1:]

print(word)
```

خروجی:

```text
Jython
```

در ادامه و هنگام یادگیری **Slicing** این روش را دقیق تر بررسی خواهیم کرد.

---

## ۱۴. خطای `IndexError`

اگر بخواهیم به Indexای دسترسی پیدا کنیم که وجود ندارد، چه اتفاقی می افتد؟

مثلاً:

```python
word = "Python"

print(word[10])
```

این String فقط Indexهای زیر را دارد:

```text
0 1 2 3 4 5
```

Index شماره `10` وجود ندارد.

در نتیجه پایتون خطای زیر را ایجاد می کند:

```text
IndexError
```

به این خطا **IndexError** گفته می شود.

---

## ۱۵. درک بهتر `IndexError`

فرض کنید:

```python
name = "Ali"
```

Indexهای معتبر:

```text
Character:  A   l   i
Index:      0   1   2
```

این موارد درست هستند:

```python
print(name[0])
print(name[1])
print(name[2])
```

اما این مورد اشتباه است:

```python
print(name[3])
```

چون Index شماره `3` خارج از محدوده String است.

به یاد داشته باشید:

```text
0 → اولین Character
1 → دومین Character
2 → سومین Character
```

طول String برابر `3` است، اما آخرین Index برابر `2` است.

---

## ۱۶. یک قانون کاربردی

برای یک String به نام:

```python
text
```

Indexهای مثبت معتبر از:

```text
0
```

تا:

```text
len(text) - 1
```

هستند.

Indexهای منفی معتبر از:

```text
-1
```

تا:

```text
-len(text)
```

هستند.

دانستن این قانون به ما کمک می کند دلیل ایجاد `IndexError` را بهتر متوجه شویم.

---

## ۱۷. بررسی قبل از Indexing

فرض کنید می خواهیم اولین Character نام کاربر را دریافت کنیم:

```python
name = input("Enter your name: ")

print(name[0])
```

اگر کاربر هیچ چیزی وارد نکند:

```python
name = ""
```

در این حالت String هیچ Characterای ندارد.

پس:

```python
name[0]
```

باعث `IndexError` می شود.

می توانیم قبل از دسترسی، String را بررسی کنیم:

```python
name = input("Enter your name: ")

if len(name) > 0:
    print(name[0])
else:
    print("You entered an empty string.")
```

اینجا چند مفهوم را با هم ترکیب کرده ایم:

* String
* `len()`
* شرط `if`
* Indexing

---

## ۱۸. Indexing و حلقه ها

چون String یک Sequence است، می توانیم Indexing را با حلقه ها ترکیب کنیم.

مثلاً:

```python
word = "Python"

for i in range(len(word)):
    print(word[i])
```

خروجی:

```text
P
y
t
h
o
n
```

در اینجا:

```python
range(len(word))
```

Indexهای زیر را تولید می کند:

```text
0 1 2 3 4 5
```

و:

```python
word[i]
```

Character مربوط به هر Index را برمی گرداند.

این مثال ارتباط مستقیمی با مباحث **حلقه ها** و تابع `range()` که قبلاً یاد گرفتیم دارد.

---

## ۱۹. یک مثال کاربردی

برنامه ای بنویسیم که یک کلمه از کاربر بگیرد و اولین و آخرین Character آن را نمایش دهد:

```python
word = input("Enter a word: ")

if len(word) > 0:
    print("First character:", word[0])
    print("Last character:", word[-1])
else:
    print("The string is empty.")
```

اگر کاربر وارد کند:

```text
Python
```

خروجی:

```text
First character: P
Last character: n
```

این یک مثال ساده اما واقعی از کاربرد Indexing در برنامه است.

---

# تمرین های کوتاه

## تمرین ۱

خروجی را حدس بزنید:

```python
word = "Python"

print(word[0])
print(word[3])
print(word[-1])
```

---

## تمرین ۲

آخرین Character String زیر را بدون استفاده از Negative Indexing پیدا کنید:

```python
word = "Programming"
```

از `len()` استفاده کنید.

---

## تمرین ۳

خروجی را حدس بزنید:

```python
text = "Hello"

print(text[-2])
print(text[-5])
```

---

## تمرین ۴

این String چند Character دارد؟

```python
text = "Hello World"
```

به یاد داشته باشید که فاصله بین `Hello` و `World` نیز یک Character است.

---

## تمرین ۵

مشخص کنید هر خط زیر درست اجرا می شود یا خطا ایجاد می کند:

```python
text = "Python"

print(text[0])
print(text[5])
print(text[6])
print(text[-1])
print(text[-6])
print(text[-7])
```

---

## تمرین ۶

برنامه ای بنویسید که نام کاربر را دریافت کند و این خروجی را نمایش دهد:

```text
First character: A
Last character: i
```

مثلاً اگر کاربر وارد کند:

```text
Ali
```

---

## تمرین ۷

برنامه ای بنویسید که یک کلمه از کاربر دریافت کند و هر Character را در یک خط جداگانه چاپ کند.

در این تمرین مستقیماً از:

```python
for character in word
```

استفاده نکنید.

از Indexing و `range()` استفاده کنید.

---

## تمرین ۸

برنامه ای بنویسید که یک کلمه از کاربر دریافت کند و فقط در صورتی اولین Character را چاپ کند که کاربر چیزی وارد کرده باشد.

اگر ورودی خالی بود، این پیام نمایش داده شود:

```text
The string is empty.
```

---

# سؤال ترکیبی پایان بخش

حالا مطالب بخش های قبلی را با Indexing ترکیب کنید.

برنامه ای بنویسید که:

1. داخل یک تابع قرار داشته باشد.
2. نام کاربر را دریافت کند.
3. سن کاربر را دریافت کند.
4. سن را به `int` تبدیل کند.
5. شهر کاربر را دریافت کند.
6. بررسی کند که آیا کاربر بزرگسال است یا نه.
7. اولین Character نام کاربر را نمایش دهد.
8. آخرین Character نام کاربر را نمایش دهد.
9. طول نام کاربر را نمایش دهد.
10. اگر نام خالی بود، بدون ایجاد خطا آن را مدیریت کند.
11. از کاربر بپرسد آیا می خواهد کاربر دیگری وارد کند یا نه.
12. تا زمانی که کاربر تصمیم به توقف نگرفته است، برنامه ادامه پیدا کند.

نمونه خروجی:

```text
Name:   Ali
Age:    22
City:   Tehran

First character: A
Last character: i
Name length: 3

Status: Adult

Add another user? yes
```

### تفکر الگوریتمی

قبل از نوشتن کد، مسئله را مرحله به مرحله بررسی کنید:

```text
شروع
↓
دریافت اطلاعات کاربر
↓
بررسی خالی بودن نام
↓
اگر نام خالی نیست:
    پیدا کردن اولین Character
    پیدا کردن آخرین Character
    پیدا کردن طول نام
↓
بررسی سن
↓
نمایش اطلاعات
↓
پرسیدن درباره ورود کاربر بعدی
↓
اگر yes → تکرار
اگر no → پایان
```

این الگوریتم را مستقیماً به کد تبدیل نکنید.

ابتدا هر مرحله را درک کنید و سپس تصمیم بگیرید برای اجرای آن به کدام ابزارهای پایتون نیاز دارید.

در این مسئله باید چند مفهوم قبلی را تشخیص دهید:

* متغیرها
* `input()`
* `int()`
* String
* `type()`
* `len()`
* Indexing
* `if`
* `for`
* `range()`
* تابع ها
* حلقه ها

هدف ما دقیقاً همین است: به تدریج یاد بگیریم چند مفهوم ساده را برای حل یک مسئله واقعی با هم ترکیب کنیم.

---

# آنچه در این بخش یاد گرفتیم

در این بخش یاد گرفتیم:

* Indexing چیست
* چرا Index در پایتون از `0` شروع می شود
* چگونه با `[]` به Characterها دسترسی پیدا کنیم
* Positive Indexing
* Negative Indexing
* چگونه اولین Character را پیدا کنیم
* چگونه آخرین Character را پیدا کنیم
* تابع `len()`
* رابطه بین طول String و آخرین Index
* خطای `IndexError`
* جلوگیری از خطاهای Indexing
* Indexing روی ورودی کاربر
* استفاده از Indexing داخل حلقه ها
* ترکیب Indexing با `range()`
* چرا Indexing باعث تغییر String نمی شود
* ارتباط Indexing با Immutable بودن String

در بخش بعدی از دسترسی به یک Character عبور می کنیم و یاد می گیریم چگونه **چند Character را به صورت همزمان از داخل String استخراج کنیم**.

---

# بخش ۴ — Slicing در String

در بخش قبلی یاد گرفتیم چگونه با استفاده از Indexing به یک Character مشخص داخل String دسترسی پیدا کنیم.

مثلاً:

```python
word = "Python"

print(word[0])
```

خروجی:

```text
P
```

اما اگر بخواهیم **چند Character را همزمان** از داخل String برداریم چه؟

مثلاً فرض کنید String ما این باشد:

```text
Python
```

و بخواهیم به این قسمت برسیم:

```text
Pyt
```

یا:

```text
hon
```

یا حتی:

```text
nohtyP
```

اینجاست که مفهوم **Slicing** اهمیت پیدا می کند.

---

# ۱. Slicing چیست؟

Slicing یعنی استخراج بخشی از یک Sequence.

چون Stringها Sequence هستند، می توانیم آن ها را Slice کنیم.

ساختار پایه:

```python
text[start:stop]
```

مثلاً:

```python
word = "Python"

print(word[0:3])
```

خروجی:

```text
Pyt
```

از Index شماره `0` شروع کردیم و قبل از Index شماره `3` متوقف شدیم.

پس یکی از مهم ترین قوانین Python این است:

> `start` در Slicing شامل می شود، اما `stop` شامل نمی شود.

---

# ۲. درک `start` و `stop`

String زیر را در نظر بگیرید:

```python
word = "Python"
```

Indexها:

```text
Character:  P   y   t   h   o   n
Index:      0   1   2   3   4   5
```

حالا:

```python
word[1:4]
```

یعنی:

```text
از 1 شروع کن
1 را بردار
2 را بردار
3 را بردار
قبل از 4 متوقف شو
```

پس نتیجه:

```text
yth
```

مثلاً:

```python
print(word[1:4])
```

خروجی:

```text
yth
```

---

# ۳. چرا `stop` شامل نمی شود؟

ممکن است در ابتدا این قانون کمی عجیب به نظر برسد.

چرا:

```python
word[0:3]
```

نتیجه:

```text
Pyt
```

می دهد و نه:

```text
Pyth
```

؟

چون Slicing بر اساس مرزهای بین Characterها طراحی شده است.

می توانیم آن را این طور تصور کنیم:

```text
    0   1   2   3   4   5   6
    |   |   |   |   |   |   |
    P   y   t   h   o   n
```

عبارت:

```python
word[0:3]
```

از مرز `0` شروع می شود و تا مرز `3` ادامه پیدا می کند.

بنابراین:

```text
P y t
```

را می گیرد.

این طراحی یک مزیت مهم دارد:

> تعداد Characterهای یک Slice برابر است با `stop - start`

مثلاً:

```python
word[1:4]
```

داریم:

```text
4 - 1 = 3
```

و واقعاً نتیجه:

```text
yth
```

سه Character دارد.

---

# ۴. مثال های ساده Slicing

```python
word = "Python"

print(word[0:2])
print(word[1:4])
print(word[2:6])
```

خروجی:

```text
Py
yth
thon
```

تجزیه کنیم:

```python
word[0:2]
```

نتیجه:

```text
Py
```

```python
word[1:4]
```

نتیجه:

```text
yth
```

```python
word[2:6]
```

نتیجه:

```text
thon
```

---

# ۵. حذف `start`

لازم نیست همیشه `start` را بنویسیم.

مثلاً:

```python
word = "Python"

print(word[:3])
```

خروجی:

```text
Pyt
```

وقتی `start` را ننویسیم، پایتون فرض می کند از ابتدای String شروع کنیم.

بنابراین:

```python
word[:3]
```

معادل است با:

```python
word[0:3]
```

---

# ۶. حذف `stop`

می توانیم `stop` را هم حذف کنیم.

مثلاً:

```python
word = "Python"

print(word[3:])
```

خروجی:

```text
hon
```

وقتی `stop` مشخص نشده باشد، پایتون تا انتهای String ادامه می دهد.

بنابراین:

```python
word[3:]
```

یعنی:

> از Index شماره ۳ شروع کن و تا انتهای String ادامه بده.

---

# ۷. حذف هر دو

اگر بنویسیم:

```python
word[:]
```

کل String را دریافت می کنیم.

مثلاً:

```python
word = "Python"

print(word[:])
```

خروجی:

```text
Python
```

این روش گاهی برای کار با Sequenceها و ایجاد یک Copy از آن ها کاربرد دارد.

---

# ۸. Slicing با Negative Index

Slicing با Negative Index هم کار می کند.

به یاد داشته باشید:

```text
Character:  P    y    t    h    o    n
Positive:   0    1    2    3    4    5
Negative:  -6   -5   -4   -3   -2   -1
```

مثلاً:

```python
word = "Python"

print(word[-3:])
```

خروجی:

```text
hon
```

یعنی:

> از سومین Character از سمت انتها شروع کن و تا انتها ادامه بده.

---

# ۹. `stop` منفی

می توانیم مقدار `stop` را هم منفی قرار دهیم.

مثلاً:

```python
word = "Python"

print(word[:-2])
```

خروجی:

```text
Pyth
```

چرا؟

چون دو Character آخر:

```text
o
n
```

هستند.

عبارت:

```python
[:-2]
```

یعنی:

> از ابتدای String شروع کن و قبل از دومین Character از انتها متوقف شو.

---

# ۱۰. ترکیب Index مثبت و منفی

می توانیم Index مثبت و منفی را با هم ترکیب کنیم.

مثلاً:

```python
word = "Python"

print(word[1:-1])
```

خروجی:

```text
ytho
```

به شکل زیر نگاه کنیم:

```text
Character:  P    y    t    h    o    n
Index:      0    1    2    3    4    5
Negative:  -6   -5   -4   -3   -2   -1
```

شروع:

```text
1 → y
```

پایان:

```text
-1 → n
```

اما چون `stop` شامل نمی شود، `n` وارد نتیجه نمی شود.

پس نتیجه:

```text
y t h o
```

خواهد بود.

---

# ۱۱. قسمت سوم Slicing: `step`

تا اینجا از این ساختار استفاده کردیم:

```python
text[start:stop]
```

اما Slicing یک قسمت اختیاری دیگر هم دارد:

```python
text[start:stop:step]
```

`step` مشخص می کند پایتون با چه فاصله ای بین Indexها حرکت کند.

مثلاً:

```python
word = "Python"

print(word[0:6:1])
```

خروجی:

```text
Python
```

چون `step` برابر `1` است، پایتون یکی یکی جلو می رود.

---

# ۱۲. `step` برابر ۲

حالا:

```python
word = "Python"

print(word[0:6:2])
```

خروجی:

```text
Pto
```

چرا؟

Indexهای انتخاب شده:

```text
0 → P
2 → t
4 → o
```

پس:

```text
P t o
```

---

# ۱۳. `step` برابر ۳

مثلاً:

```python
word = "Python"

print(word[0:6:3])
```

خروجی:

```text
Ph
```

Indexها:

```text
0 → P
3 → h
```

پس نتیجه:

```text
Ph
```

---

# ۱۴. درک ساده `step`

می توانیم `step` را به عنوان **اندازه پرش** در نظر بگیریم.

```text
step = 1
→ هر Character

step = 2
→ یک Character در میان

step = 3
→ هر سه Character یک بار
```

برای:

```text
Python
```

داریم:

```text
Index:  0  1  2  3  4  5
        P  y  t  h  o  n
```

پس:

```python
word[::2]
```

نتیجه:

```text
Pto
```

خواهد بود.

---

# ۱۵. حذف `start` و `stop` همراه با `step`

می توانیم هر دو را حذف کنیم:

```python
word[::2]
```

یعنی:

> از ابتدا شروع کن، تا انتها برو و با پرش ۲ حرکت کن.

مثلاً:

```python
word = "Python"

print(word[::2])
```

خروجی:

```text
Pto
```

---

# ۱۶. برعکس کردن String با `[::-1]`

یکی از کاربردی ترین تکنیک های Slicing عبارت زیر است:

```python
[::-1]
```

مثلاً:

```python
word = "Python"

print(word[::-1])
```

خروجی:

```text
nohtyP
```

چرا؟

چون `step` برابر:

```text
-1
```

است.

Step منفی به پایتون می گوید به سمت عقب حرکت کند.

پس:

```python
[::-1]
```

یعنی:

> از انتهای String شروع کن و هر بار یک Character به سمت عقب حرکت کن.

---

# ۱۷. درک دقیق `[::-1]`

String اصلی:

```text
P y t h o n
```

به صورت برعکس پیمایش می شود:

```text
n o h t y P
```

بنابراین:

```python
word[::-1]
```

نتیجه:

```text
nohtyP
```

خواهد بود.

این یکی از رایج ترین الگوهای Slicing در پایتون است.

---

# ۱۸. Step منفی دیگر

Step منفی فقط `-1` نیست.

مثلاً:

```python
word = "Python"

print(word[::-2])
```

خروجی:

```text
nhy
```

Indexها به صورت معکوس پیمایش می شوند:

```text
5 → n
3 → h
1 → y
```

پس نتیجه:

```text
nhy
```

است.

---

# ۱۹. Step منفی جهت حرکت را تغییر می دهد

این دو را مقایسه کنید:

```python
word[::2]
```

و:

```python
word[::-2]
```

اولی به سمت جلو حرکت می کند:

```text
0 → 2 → 4
```

دومی به سمت عقب حرکت می کند:

```text
5 → 3 → 1
```

پس:

```python
word[::2]
```

و:

```python
word[::-2]
```

فقط دو حالت مشابه با علامت متفاوت نیستند؛ آن ها Sequence را در دو جهت متفاوت پیمایش می کنند.

---

# ۲۰. Slicing String اصلی را تغییر نمی دهد

مثل Indexing، Slicing نیز String اصلی را تغییر نمی دهد.

مثلاً:

```python
word = "Python"

part = word[0:3]

print(part)
print(word)
```

خروجی:

```text
Pyt
Python
```

String اصلی همچنان:

```text
Python
```

است.

این موضوع یکی دیگر از نتایج **Immutable بودن Stringها** است.

---

# ۲۱. ذخیره نتیجه Slicing در متغیر

می توانیم نتیجه Slice را داخل یک متغیر جدید ذخیره کنیم:

```python
word = "Python"

first_part = word[:3]
second_part = word[3:]

print(first_part)
print(second_part)
```

خروجی:

```text
Pyt
hon
```

در واقع String را به دو قسمت تقسیم کرده ایم.

---

# ۲۲. ساخت String جدید با Slicing

چون نمی توانیم String را مستقیماً تغییر دهیم، Slicing می تواند برای ساخت نسخه جدید کمکمان کند.

فرض کنید:

```python
word = "Python"
```

و می خواهیم:

```text
Jython
```

را بسازیم.

نمی توانیم بنویسیم:

```python
word[0] = "J"
```

در عوض:

```python
word = "J" + word[1:]
```

حالا:

```python
print(word)
```

خروجی:

```text
Jython
```

ما یک String جدید از دو قسمت ساخته ایم:

```text
"J"
```

و:

```text
"ython"
```

---

# ۲۳. استخراج بخش هایی از ورودی کاربر

Slicing هنگام کار با `input()` کاربرد بسیار زیادی دارد.

مثلاً:

```python
name = input("Enter your name: ")

print("First three characters:", name[:3])
```

اگر کاربر بنویسد:

```text
Alexander
```

خروجی:

```text
First three characters: Ale
```

این نوع عملیات در پردازش واقعی متن بسیار کاربردی است.

---

# ۲۴. ترکیب Slicing و `len()`

می توانیم Slicing را با `len()` ترکیب کنیم.

مثلاً:

```python
word = "Python"

middle = word[1:len(word)-1]

print(middle)
```

خروجی:

```text
ytho
```

ما اولین و آخرین Character را حذف کردیم.

نسخه ساده تر همین کار:

```python
word[1:-1]
```

است.

هر دو روش یک مفهوم را نشان می دهند.

---

# ۲۵. Slicing و حلقه ها

Slicing را می توانیم با حلقه ها نیز ترکیب کنیم.

مثلاً:

```python
word = "Python"

for i in range(len(word)):
    print(word[i:])
```

خروجی:

```text
Python
ython
thon
hon
on
n
```

در هر تکرار، شروع Slice یک Index جلوتر می رود.

این مثال نشان می دهد که چگونه چند مفهوم مختلف که قبلاً یاد گرفته ایم می توانند با هم کار کنند.

---

# ۲۶. اشتباهات رایج در Slicing

### اشتباه اول — انتظار داشته باشیم `stop` شامل شود

```python
word = "Python"

print(word[0:3])
```

ممکن است انتظار داشته باشید:

```text
Pyth
```

اما نتیجه:

```text
Pyt
```

است.

قانون را به یاد داشته باشید:

> `start` شامل می شود، `stop` شامل نمی شود.

---

### اشتباه دوم — اشتباه گرفتن Length و آخرین Index

برای:

```python
word = "Python"
```

داریم:

```text
len(word) = 6
```

اما:

```text
last index = 5
```

---

### اشتباه سوم — فراموش کردن جهت حرکت Step

```python
word[::2]
```

به سمت جلو حرکت می کند.

اما:

```python
word[::-2]
```

به سمت عقب حرکت می کند.

---

### اشتباه چهارم — تصور اینکه Slicing String اصلی را تغییر می دهد

این کد:

```python
part = word[:3]
```

یک مقدار جدید تولید می کند.

String اصلی تغییر نمی کند.

---

# تمرین های کوتاه

## تمرین ۱

خروجی را حدس بزنید:

```python
word = "Python"

print(word[1:4])
```

---

## تمرین ۲

خروجی را حدس بزنید:

```python
word = "Programming"

print(word[:4])
print(word[4:])
```

---

## تمرین ۳

خروجی را حدس بزنید:

```python
word = "Python"

print(word[-3:])
print(word[:-3])
```

---

## تمرین ۴

خروجی را حدس بزنید:

```python
word = "Python"

print(word[::2])
```

---

## تمرین ۵

خروجی را حدس بزنید:

```python
word = "Python"

print(word[::-1])
```

---

## تمرین ۶

بدون اجرای برنامه، خروجی را حدس بزنید:

```python
word = "Programming"

print(word[1:-1])
```

---

## تمرین ۷

برنامه ای بنویسید که یک کلمه از کاربر دریافت کند و:

* نیمه اول آن
* نیمه دوم آن

را نمایش دهد.

راهنما:

از `len()` و Slicing استفاده کنید.

---

## تمرین ۸

برنامه ای بنویسید که یک کلمه از کاربر دریافت کند و آن را برعکس چاپ کند.

از حلقه استفاده نکنید.

از Slicing استفاده کنید.

---

## تمرین ۹

برنامه ای بنویسید که یک کلمه از کاربر دریافت کند و یک Character در میان را چاپ کند.

مثلاً:

```text
Input:
Python

Output:
Pto
```

---

## تمرین ۱۰

برنامه ای بنویسید که یک Username دریافت کند و خروجی زیر را نمایش دهد:

```text
First 3 characters:
Last 3 characters:
Reversed:
```

برای هر سه مورد از Slicing استفاده کنید.

---

# سؤال ترکیبی پایان بخش

حالا تمام مطالبی را که تا اینجا یاد گرفته ایم با هم ترکیب کنید.

برنامه ای بنویسید که:

1. داخل یک تابع قرار داشته باشد.
2. نام کاربر را دریافت کند.
3. سن کاربر را دریافت کند.
4. سن را به `int` تبدیل کند.
5. شهر کاربر را دریافت کند.
6. بررسی کند که آیا کاربر بزرگسال است یا نه.
7. طول نام را نمایش دهد.
8. اولین Character نام را نمایش دهد.
9. آخرین Character نام را نمایش دهد.
10. سه Character اول نام را نمایش دهد.
11. سه Character آخر نام را نمایش دهد.
12. نام را برعکس نمایش دهد.
13. اگر نام خالی بود، بدون ایجاد خطا آن را مدیریت کند.
14. از کاربر بپرسد آیا می خواهد کاربر دیگری وارد کند یا نه.
15. تا زمانی که کاربر تصمیم به توقف نگرفته است، برنامه ادامه پیدا کند.

نمونه خروجی:

```text
Name:   Alexander
Age:    22
City:   Tehran

Name length: 9
First character: A
Last character: r
First 3 characters: Ale
Last 3 characters: der
Reversed: rednaxelA

Status: Adult

Add another user? yes
```

## تفکر الگوریتمی

قبل از نوشتن کد، مسئله را به قسمت های کوچک تر تقسیم کنید.

از خودتان بپرسید:

1. چه اطلاعاتی لازم دارم؟
2. کدام مقدار باید به عدد تبدیل شود؟
3. اگر نام خالی باشد چه اتفاقی باید بیفتد؟
4. چگونه اولین Character را پیدا کنم؟
5. چگونه آخرین Character را پیدا کنم؟
6. چگونه سه Character اول را بگیرم؟
7. چگونه سه Character آخر را بگیرم؟
8. چگونه نام را Reverse کنم؟
9. شرط `if` را کجا قرار دهم؟
10. حلقه را کجا قرار دهم؟
11. تابع را کجا قرار دهم؟

هدف این نیست که فقط عبارت زیر را حفظ کنید:

```python
[::-1]
```

هدف این است که **دلیل استفاده از آن را بفهمید.**

---

# آنچه در این بخش یاد گرفتیم

در این بخش یاد گرفتیم:

* Slicing در String چیست
* `start`
* `stop`
* چرا `stop` شامل نمی شود
* ساختار `text[start:stop]`
* حذف `start`
* حذف `stop`
* حذف هر دو
* استفاده از Indexهای مثبت در Slicing
* استفاده از Indexهای منفی در Slicing
* `step`
* Step مثبت
* Step منفی
* `[::-1]`
* Reverse کردن String
* ترکیب `len()` و Slicing
* ترکیب Slicing و حلقه ها
* ساخت String جدید با استفاده از Slicing
* اشتباهات رایج در Slicing
* استفاده از Slicing روی ورودی کاربر

در بخش بعدی از استخراج Characterها عبور می کنیم و وارد **کار با محتوای Stringها و متدهای آن ها** می شویم.

---

# بخش ۵ — متدهای رشته

> 🌐 زبان: **فارسی** | [English](../README.md)

## ۱. متد رشته چیست؟

در بخش های قبلی یاد گرفتیم چگونه رشته بسازیم، با استفاده از Indexing به کاراکترها دسترسی پیدا کنیم و با Slicing قسمت هایی از یک رشته را استخراج کنیم.

حالا می خواهیم یاد بگیریم چگونه خود رشته را **پردازش کنیم**.

برای مثال:

```python
text = "python"
```

اگر بخواهیم آن را به شکل زیر تبدیل کنیم:

```text
PYTHON
```

می توانیم از متد `upper()` استفاده کنیم:

```python
print(text.upper())
```

خروجی:

```text
PYTHON
```

در اینجا:

* `text` یک String Object است.
* `upper()` یک String Method است.
* `.` برای دسترسی به متد شیء استفاده می شود.

ساختار کلی یک متد به این شکل است:

```python
string.method()
```

بعضی متدها نیز ورودی دریافت می کنند:

```python
string.method(argument)
```

مثلاً:

```python
text = "hello world"

print(text.replace("world", "Python"))
```

خروجی:

```text
hello Python
```

---

## ۲. تفاوت Function و Method

تا اینجا از توابعی مثل `len()` استفاده کرده ایم:

```python
len(text)
```

`len()` یک **Function** است.

اما:

```python
text.upper()
```

از یک **Method** استفاده می کند.

به صورت ساده:

```python
# Function
len(text)

# Method
text.upper()
```

تابع، شیء را به عنوان ورودی دریافت می کند.

اما متد مستقیماً روی خود شیء فراخوانی می شود.

این تفاوت در ادامه مسیر پایتون بسیار مهم خواهد بود.

---

## ۳. متد `upper()`

متد `upper()` حروف را به حروف بزرگ تبدیل می کند.

```python
text = "hello"

print(text.upper())
```

خروجی:

```text
HELLO
```

مثال دیگر:

```python
name = "alexander"

print(name.upper())
```

خروجی:

```text
ALEXANDER
```

### آیا `upper()` رشته اصلی را تغییر می دهد؟

خیر.

```python
text = "hello"

print(text.upper())
print(text)
```

خروجی:

```text
HELLO
hello
```

رشته ها Immutable هستند، بنابراین `upper()` یک String جدید ایجاد می کند.

اگر بخواهیم نتیجه را ذخیره کنیم:

```python
text = text.upper()
```

حالا مقدار `text` برابر است با:

```text
HELLO
```

---

## ۴. متد `lower()`

متد `lower()` حروف را به حروف کوچک تبدیل می کند.

```python
text = "PYTHON"

print(text.lower())
```

خروجی:

```text
python
```

این متد زمانی بسیار کاربردی است که نخواهیم تفاوت حروف بزرگ و کوچک روی مقایسه تأثیر بگذارد.

مثلاً:

```python
answer = input("Continue? ")

if answer.lower() == "yes":
    print("Continuing...")
```

حالا ورودی های زیر همگی قابل قبول هستند:

```text
yes
YES
Yes
YeS
```

چون قبل از مقایسه به حروف کوچک تبدیل شده اند.

---

## ۵. متد `capitalize()`

متد `capitalize()` اولین کاراکتر را بزرگ و باقی حروف را کوچک می کند.

```python
text = "pYTHON"

print(text.capitalize())
```

خروجی:

```text
Python
```

تفاوت آن با `upper()` را دقت کنید.

برای:

```text
python
```

متد `upper()` نتیجه زیر را می دهد:

```text
PYTHON
```

اما `capitalize()` نتیجه زیر را می دهد:

```text
Python
```

---

## ۶. متد `title()`

متد `title()` اولین حرف هر کلمه را بزرگ می کند.

```python
text = "hello world"

print(text.title())
```

خروجی:

```text
Hello World
```

مثلاً:

```python
name = input("Enter your name: ")

print(name.title())
```

اگر کاربر وارد کند:

```text
aLEXANDER hAMILTON
```

نتیجه:

```text
Alexander Hamilton
```

خواهد بود.

---

## ۷. مقایسه `upper()`، `lower()`، `capitalize()` و `title()`

فرض کنید:

```python
text = "hello WORLD"
```

نتیجه:

```python
text.upper()
```

برابر است با:

```text
HELLO WORLD
```

نتیجه:

```python
text.lower()
```

برابر است با:

```text
hello world
```

نتیجه:

```python
text.capitalize()
```

برابر است با:

```text
Hello world
```

و:

```python
text.title()
```

برابر است با:

```text
Hello World
```

| متد            | نتیجه                  |
| -------------- | ---------------------- |
| `upper()`      | تمام حروف بزرگ         |
| `lower()`      | تمام حروف کوچک         |
| `capitalize()` | اولین کاراکتر بزرگ     |
| `title()`      | اولین حرف هر کلمه بزرگ |

---

## ۸. متد `strip()`

گاهی در ابتدای یا انتهای String فاصله های اضافی وجود دارد.

مثلاً:

```python
name = "   Alice   "
```

می توانیم این فاصله ها را با `strip()` حذف کنیم:

```python
print(name.strip())
```

خروجی:

```text
Alice
```

این متد هنگام دریافت ورودی از کاربر بسیار کاربردی است:

```python
name = input("Enter your name: ").strip()
```

---

## ۹. متدهای `lstrip()` و `rstrip()`

گاهی نمی خواهیم فاصله های دو طرف را همزمان حذف کنیم.

`lstrip()` فاصله های سمت چپ را حذف می کند:

```python
text = "   Python   "

print(text.lstrip())
```

نتیجه:

```text
Python   
```

`rstrip()` فاصله های سمت راست را حذف می کند:

```python
text = "   Python   "

print(text.rstrip())
```

نتیجه:

```text
   Python
```

پس:

```text
strip()   → هر دو طرف
lstrip()  → سمت چپ
rstrip()  → سمت راست
```

---

## ۱۰. متد `replace()`

متد `replace()` یک قسمت از متن را با قسمت دیگری جایگزین می کند.

ساختار:

```python
text.replace(old, new)
```

مثال:

```python
text = "I like Java"

print(text.replace("Java", "Python"))
```

خروجی:

```text
I like Python
```

حتی می توانیم یک کاراکتر را جایگزین کنیم:

```python
text = "banana"

print(text.replace("a", "o"))
```

خروجی:

```text
bonono
```

تمام `a`های موجود جایگزین می شوند.

---

## ۱۱. `replace()` رشته اصلی را تغییر نمی دهد

مانند `upper()`، متد `replace()` نیز یک String جدید ایجاد می کند.

```python
text = "I like Java"

text.replace("Java", "Python")

print(text)
```

خروجی همچنان:

```text
I like Java
```

است.

اگر بخواهیم نتیجه را ذخیره کنیم:

```python
text = text.replace("Java", "Python")
```

اکنون:

```text
I like Python
```

---

## ۱۲. محدود کردن تعداد جایگزینی ها

می توانیم مشخص کنیم چند بار جایگزینی انجام شود.

```python
text = "banana"

print(text.replace("a", "o", 1))
```

خروجی:

```text
bonana
```

فقط اولین `a` جایگزین شده است.

مثلاً:

```python
text.replace("a", "o", 2)
```

نتیجه:

```text
bonona
```

آرگومان سوم، حداکثر تعداد جایگزینی ها را مشخص می کند.

---

## ۱۳. متد `find()`

متد `find()` به دنبال یک Substring می گردد و Index آن را برمی گرداند.

```python
text = "Python programming"

print(text.find("programming"))
```

خروجی:

```text
7
```

چرا `7`؟

چون کلمه `programming` از Index شماره ۷ شروع می شود.

```text
P y t h o n   p r o g r a m m i n g
0 1 2 3 4 5 6 7 ...
```

---

## ۱۴. اگر `find()` چیزی پیدا نکند چه می شود؟

اگر Substring مورد نظر وجود نداشته باشد، `find()` مقدار `-1` را برمی گرداند.

```python
text = "Python"

print(text.find("Java"))
```

خروجی:

```text
-1
```

این یک Error نیست.

می توانیم از آن در شرط استفاده کنیم:

```python
text = "Python"

position = text.find("Java")

if position == -1:
    print("Java was not found")
```

خروجی:

```text
Java was not found
```

---

## ۱۵. ترکیب `find()` با Slicing

می توانیم مفاهیم قبلی را با متدهای جدید ترکیب کنیم.

```python
text = "Python programming"

position = text.find("programming")

print(text[position:])
```

خروجی:

```text
programming
```

اینجا سه مفهوم را ترکیب کرده ایم:

1. `find()`
2. Indexing
3. Slicing

این دقیقاً همان مسیری است که ما را به سمت تفکر الگوریتمی می برد.

---

## ۱۶. متد `count()`

متد `count()` مشخص می کند یک Substring چند بار در String ظاهر شده است.

```python
text = "banana"

print(text.count("a"))
```

خروجی:

```text
3
```

مثال دیگر:

```python
text = "hello hello"

print(text.count("hello"))
```

خروجی:

```text
2
```

---

## ۱۷. متد `startswith()`

این متد بررسی می کند که آیا String با مقدار مشخصی شروع می شود یا نه.

```python
text = "Python programming"

print(text.startswith("Python"))
```

خروجی:

```text
True
```

اما:

```python
print(text.startswith("Java"))
```

نتیجه:

```text
False
```

چون این متد یک مقدار Boolean برمی گرداند، می توانیم آن را مستقیماً در `if` استفاده کنیم:

```python
username = input("Username: ")

if username.startswith("admin"):
    print("Administrative account")
```

---

## ۱۸. متد `endswith()`

این متد بررسی می کند که String با مقدار مشخصی تمام می شود یا نه.

```python
filename = "report.pdf"

print(filename.endswith(".pdf"))
```

خروجی:

```text
True
```

برای بررسی پسوند فایل نیز بسیار کاربردی است:

```python
filename = input("Filename: ")

if filename.endswith(".pdf"):
    print("PDF file")
```

---

## ۱۹. متد `isdigit()`

این متد بررسی می کند که تمام کاراکترهای String رقم هستند یا نه.

```python
text = "12345"

print(text.isdigit())
```

خروجی:

```text
True
```

اما:

```python
text = "123a"

print(text.isdigit())
```

نتیجه:

```text
False
```

این متد برای اعتبارسنجی ورودی کاربر بسیار کاربردی است:

```python
age = input("Enter your age: ")

if age.isdigit():
    age = int(age)
    print("Age:", age)
else:
    print("Invalid age")
```

دقت کنید که `input()` همیشه یک String برمی گرداند، بنابراین می توانیم قبل از تبدیل آن به عدد، String را بررسی کنیم.

---

## ۲۰. متد `isalpha()`

`isalpha()` بررسی می کند که تمام کاراکترهای String حروف الفبا باشند.

```python
text = "Python"

print(text.isalpha())
```

خروجی:

```text
True
```

اما:

```python
text = "Python3"

print(text.isalpha())
```

نتیجه:

```text
False
```

چون `3` حرف نیست.

---

## ۲۱. متد `isalnum()`

`isalnum()` زمانی `True` برمی گرداند که تمام کاراکترها حرف یا عدد باشند.

```python
print("Python123".isalnum())
```

خروجی:

```text
True
```

اما:

```python
print("Python 123".isalnum())
```

نتیجه:

```text
False
```

چون فاصله نه حرف است و نه عدد.

---

## ۲۲. متد `isspace()`

`isspace()` بررسی می کند که تمام کاراکترهای String از نوع Whitespace باشند.

```python
text = "   "

print(text.isspace())
```

خروجی:

```text
True
```

اما:

```python
text = " Python "

print(text.isspace())
```

نتیجه:

```text
False
```

این متد می تواند برای تشخیص ورودی هایی که فقط شامل فاصله هستند استفاده شود.

---

## ۲۳. متدهای `isupper()` و `islower()`

این متدها وضعیت حروف بزرگ و کوچک را بررسی می کنند.

```python
text = "PYTHON"

print(text.isupper())
```

خروجی:

```text
True
```

و:

```python
text = "python"

print(text.islower())
```

خروجی:

```text
True
```

برای یک String با حروف ترکیبی:

```python
text = "Python"

print(text.isupper())
print(text.islower())
```

هر دو:

```text
False
```

خواهند بود.

---

## ۲۴. تفاوت متدهای تبدیل و بررسی

این تفاوت را حتماً به خاطر بسپارید.

متدهای **تبدیل کننده**:

```text
upper()
lower()
capitalize()
title()
```

متدهای **بررسی کننده**:

```text
isdigit()
isalpha()
isalnum()
isspace()
isupper()
islower()
```

متدهای بررسی کننده معمولاً مقدار Boolean برمی گردانند:

```text
True
```

یا:

```text
False
```

---

## ۲۵. Method Chaining

می توانیم چند متد را پشت سر هم اجرا کنیم.

مثلاً:

```python
name = "   aLEXANDER   "

print(name.strip().lower())
```

عملیات از چپ به راست انجام می شوند:

```text
"   aLEXANDER   "
        ↓
strip()
        ↓
"aLEXANDER"
        ↓
lower()
        ↓
"alexander"
```

حتی می توانیم یک مرحله دیگر اضافه کنیم:

```python
name.strip().lower().title()
```

نتیجه:

```text
Alexander
```

به این کار **Method Chaining** گفته می شود.

---

## ۲۶. چگونه یک عبارت زنجیره ای را بخوانیم؟

فرض کنید این عبارت را می بینید:

```python
text.strip().lower().replace("python", "java")
```

لازم نیست همه چیز را همزمان بفهمید.

از چپ به راست بخوانید:

```text
1. strip()
2. lower()
3. replace()
```

هر عملیات یک String جدید تولید می کند و آن String ورودی عملیات بعدی می شود.

---

## ۲۷. مثال کاربردی — اعتبارسنجی Username

می توانیم چند مفهوم را برای ساخت یک اعتبارسنجی ساده ترکیب کنیم:

```python
username = input("Enter username: ").strip()

if username == "":
    print("Username cannot be empty")
elif not username.isalnum():
    print("Username can contain only letters and numbers")
else:
    print("Username accepted")
```

فرآیند برنامه:

```text
input
  ↓
strip
  ↓
بررسی خالی بودن
  ↓
بررسی کاراکترها
  ↓
نمایش نتیجه
```

این بسیار به برنامه نویسی واقعی نزدیک تر از استفاده جداگانه از هر متد است.

---

## ۲۸. مثال کاربردی — اعتبارسنجی عدد

چون `input()` همیشه یک String برمی گرداند، می توانیم قبل از تبدیل آن را بررسی کنیم:

```python
age = input("Enter your age: ").strip()

if age.isdigit():
    age = int(age)
    print("Your age is", age)
else:
    print("Please enter a valid number")
```

اینجا چند مفهوم را با هم ترکیب کرده ایم:

* `input()`
* `strip()`
* `isdigit()`
* `if`
* `int()`

---

## ۲۹. مثال کاربردی — جستجو در متن

```python
message = input("Enter a message: ")

if message.lower().find("python") != -1:
    print("The message contains Python")
else:
    print("Python was not found")
```

چون ابتدا متن را به حروف کوچک تبدیل کرده ایم، برنامه می تواند شکل های مختلف کلمه را به صورت یکسان بررسی کند:

```text
Python
python
PYTHON
PyThOn
```

---

# تمرین ها

## تمرین ۱ — پیش بینی خروجی

خروجی برنامه زیر چیست؟

```python
text = "python"

print(text.upper())
print(text.capitalize())
print(text.title())
```

---

## تمرین ۲ — فاصله ها

خروجی هر خط را مشخص کنید:

```python
text = "   Hello World   "

print(text.strip())
print(text.lstrip())
print(text.rstrip())
```

---

## تمرین ۳ — جستجو و شمارش

خروجی برنامه چیست؟

```python
text = "banana"

print(text.count("a"))
print(text.find("n"))
```

---

## تمرین ۴ — ترکیب متدها

خروجی برنامه زیر چیست؟

```python
text = "Python Programming"

print(text.lower().startswith("python"))
```

---

## تمرین ۵ — اعتبارسنجی

خروجی را پیش بینی کنید:

```python
text = "12345"

print(text.isdigit())
print(text.isalpha())
print(text.isalnum())
```

---

## تمرین ۶ — قالب بندی نام

برنامه ای بنویسید که:

1. نام کاربر را دریافت کند.
2. فاصله های اضافی ابتدا و انتها را حذف کند.
3. تمام حروف را کوچک کند.
4. نام را به حالت Title Case تبدیل کند.
5. نتیجه نهایی را چاپ کند.

---

## تمرین ۷ — اعتبارسنجی عدد

یک عدد را به صورت String از کاربر دریافت کنید.

اگر فقط شامل رقم بود، آن را به `int` تبدیل کنید.

در غیر این صورت:

```text
Invalid number
```

را چاپ کنید.

---

## تمرین ۸ — شمارش کاراکترها

یک جمله از کاربر دریافت کنید و تعداد موارد زیر را محاسبه کنید:

* فاصله ها
* `a`
* `e`
* `i`

---

## تمرین ۹ — پسوند فایل

نام یک فایل را از کاربر دریافت کنید.

اگر با:

```text
.py
```

تمام شد، چاپ کنید:

```text
Python file
```

در غیر این صورت:

```text
Not a Python file
```

---

## تمرین ۱۰ — اعتبارسنجی Username

برنامه ای بنویسید که Username را از کاربر دریافت کند.

Username فقط زمانی معتبر است که:

* خالی نباشد.
* فقط شامل حروف و اعداد باشد.
* حداقل ۵ کاراکتر داشته باشد.

در صورت معتبر بودن:

```text
Valid username
```

و در غیر این صورت:

```text
Invalid username
```

را نمایش دهید.

---

# چالش بخش — Text Analyzer

برنامه ای طراحی کنید که یک جمله را از کاربر دریافت کند و یک تحلیل ساده روی آن انجام دهد.

برنامه باید:

1. جمله را با `input()` دریافت کند.
2. فاصله های اضافی ابتدا و انتهای آن را حذف کند.
3. بررسی کند که جمله خالی نباشد.
4. جمله را با حروف کوچک نمایش دهد.
5. جمله را با حروف بزرگ نمایش دهد.
6. جمله را به حالت Title نمایش دهد.
7. تعداد کاراکترها را نمایش دهد.
8. تعداد فاصله ها را بشمارد.
9. تعداد `a`ها را بشمارد.
10. بررسی کند که آیا جمله با `"I"` شروع می شود.
11. بررسی کند که آیا جمله با `"."` تمام می شود.
12. یک کلمه دیگر از کاربر دریافت کند.
13. آن کلمه را در جمله جستجو کند.
14. مشخص کند که کلمه پیدا شده است یا نه.
15. از کاربر بپرسد که آیا می خواهد جمله دیگری را بررسی کند.

### نکته مهم

فعلاً جواب نهایی را ننویسید.

ابتدا الگوریتم را طراحی کنید.

برای مثال:

```text
شروع
  ↓
دریافت جمله
  ↓
پاک سازی جمله
  ↓
بررسی خالی بودن
  ↓
تحلیل جمله
  ↓
نمایش نتایج
  ↓
دریافت کلمه برای جستجو
  ↓
جستجوی کلمه
  ↓
نمایش نتیجه
  ↓
پرسیدن ادامه دادن یا توقف
  ↓
تکرار یا پایان
```

هدف این بخش فقط حفظ کردن متدهای String نیست.

هدف این است که یاد بگیریم چگونه **چند متد و چند ساختار کنترلی را برای حل یک مسئله ترکیب کنیم.**

---

# سؤال الگوریتمی نهایی بخش ۵

قبل از ورود به مرحله تمرین، این مسئله را ابتدا به صورت الگوریتمی حل کنید:

> برنامه ای بنویسید که یک متن را از کاربر دریافت کند و بر اساس چند قانون مشخص کند که آیا متن وارد شده می تواند یک Username معتبر باشد یا خیر.

برنامه باید بررسی کند:

* آیا ورودی خالی است؟
* آیا فاصله های اضافی دارد؟
* آیا فقط شامل حروف و اعداد است؟
* آیا حداقل ۵ کاراکتر دارد؟
* آیا با یک Prefix مشخص شروع می شود؟

### وظیفه شما

فعلاً کد را ننویسید.

ابتدا الگوریتم را با زبان خودتان بنویسید.

سپس الگوریتم را به Python تبدیل کنید.

هدف این است که مسیر زیر را به صورت عملی تمرین کنیم:

```text
مسئله
   ↓
قوانین
   ↓
الگوریتم
   ↓
کد Python
```

حل نهایی این سؤال را در مرحله بعد، **بعد از اینکه کاربر فرصت حل مستقل مسئله را داشت**، پیاده سازی خواهیم کرد.

---

# بخش ۶ — قالب بندی رشته ها

تا اینجا یاد گرفتیم چگونه String بسازیم، به کاراکترهای آن دسترسی پیدا کنیم، بخشی از آن را با Slicing استخراج کنیم و با String Methodها کار کنیم.

اما یک سؤال مهم دیگر وجود دارد:

چطور می توانیم خروجی برنامه را مرتب، خوانا و حرفه ای نمایش دهیم؟

برای مثال فرض کنید برنامه این اطلاعات را دارد:

name = "Ahmad"
age = 25
score = 92.5

ممکن است بخواهیم خروجی به این شکل باشد:

Name: Ahmad
Age: 25
Score: 92.5

به این فرآیند **String Formatting** یا قالب بندی رشته می گوییم.

---

## چرا به String Formatting نیاز داریم؟

برنامه ها دائماً باید متن را با داده های مختلف ترکیب کنند.

برای مثال:

- یک بازی امتیاز بازیکن را نمایش می دهد.
- یک برنامه بانکی موجودی حساب را نمایش می دهد.
- یک برنامه ثبت نام نام کاربر را نمایش می دهد.
- یک برنامه فروشگاهی قیمت محصول را نمایش می دهد.
- یک برنامه آموزشی اطلاعات دانش آموز را نمایش می دهد.

ما به روشی نیاز داریم که بتوانیم مقدارها را داخل متن قرار دهیم.

پایتون روش های مختلفی برای این کار دارد.

مهم ترین روش مدرن:

**f-string**

است.

---

# String Concatenation

ساده ترین روش ترکیب Stringها استفاده از `+` است.

برای مثال:

first_name = "Ahmad"
last_name = "Ahmadi"

full_name = first_name + " " + last_name

print(full_name)

خروجی:

Ahmad Ahmadi

عملگر `+` چند String را به یکدیگر متصل می کند.

---

## ترکیب چند مقدار

می توانیم چند String را نیز با هم ترکیب کنیم:

first_name = "Ahmad"
last_name = "Ahmadi"
city = "Tehran"

message = first_name + " " + last_name + " lives in " + city

print(message)

خروجی:

Ahmad Ahmadi lives in Tehran

این روش کار می کند، اما وقتی تعداد مقدارها زیاد شود، کد طولانی و سخت خوانا می شود.

---

# مشکل ترکیب Data Typeهای مختلف

کد زیر را در نظر بگیرید:

age = 25

print("I am " + age + " years old.")

این کد خطا ایجاد می کند.

چرا؟

چون:

"I am "

یک String است، اما:

age

یک Integer است.

پایتون اجازه نمی دهد Integer را مستقیماً با `+` به String متصل کنیم.

باید Integer را به String تبدیل کنیم:

age = 25

print("I am " + str(age) + " years old.")

خروجی:

I am 25 years old.

---

# تابع `str()`

تابع `str()` یک مقدار را به String تبدیل می کند.

برای مثال:

age = 25

text = str(age)

print(text)
print(type(text))

خروجی:

25
<class 'str'>

قبل از تبدیل:

age

یک Integer بود.

بعد از:

str(age)

یک String داریم.

همین کار با عدد اعشاری نیز امکان پذیر است:

score = 92.5

print("My score is " + str(score))

خروجی:

My score is 92.5

---

# چرا Concatenation می تواند سخت شود؟

این کد را ببینید:

name = "Ahmad"
age = 25
city = "Tehran"
score = 92.5

print(
    "My name is " + name +
    ", I am " + str(age) +
    " years old, I live in " + city +
    ", and my score is " + str(score) + "."
)

برنامه درست کار می کند، اما عبارت طولانی و نگهداری آن سخت است.

پایتون راه تمیزتری ارائه می دهد.

---

# f-String

f-string به ما اجازه می دهد مقدار متغیرها را مستقیماً داخل متن قرار دهیم.

ساختار پایه:

f"text {variable}"

برای مثال:

name = "Ahmad"
age = 25

print(f"My name is {name} and I am {age} years old.")

خروجی:

My name is Ahmad and I am 25 years old.

به `f` قبل از علامت نقل قول توجه کنید:

f"..."

متغیر داخل آکولاد قرار می گیرد:

{name}

و:

{age}

این یکی از مهم ترین روش های String Formatting در پایتون است.

---

# قرار دادن چند متغیر در f-String

می توانیم چند متغیر را داخل یک f-string قرار دهیم:

name = "Ahmad"
age = 25
city = "Tehran"

print(f"My name is {name}, I am {age} years old, and I live in {city}.")

خروجی:

My name is Ahmad, I am 25 years old, and I live in Tehran.

---

# قرار دادن Expression داخل `{}`

محتوای داخل `{}` فقط نباید یک متغیر باشد.

می توانیم Expression نیز داخل آن قرار دهیم.

برای مثال:

age = 25

print(f"Next year I will be {age + 1}.")

خروجی:

Next year I will be 26.

مثال دیگر:

a = 10
b = 20

print(f"The sum is {a + b}.")

خروجی:

The sum is 30.

حتی می توانیم تابع استفاده کنیم:

name = "ahmad"

print(f"Hello {name.title()}!")

خروجی:

Hello Ahmad!

یا از Method استفاده کنیم:

text = "python programming"

print(f"Uppercase: {text.upper()}")

خروجی:

Uppercase: PYTHON PROGRAMMING

نکته مهم:

Expression داخل `{}` توسط پایتون محاسبه می شود.

---

# ترکیب مطالب بخش های قبلی با f-String

حالا می توانیم مطالب بخش های قبلی را با هم ترکیب کنیم.

فرض کنید:

text = "Python Programming"

می توانیم از Indexing استفاده کنیم:

print(f"First character: {text[0]}")

خروجی:

First character: P

از Slicing استفاده کنیم:

print(f"First three characters: {text[:3]}")

خروجی:

First three characters: Pyt

از String Method استفاده کنیم:

print(f"Lowercase: {text.lower()}")

خروجی:

Lowercase: python programming

از `len()` استفاده کنیم:

print(f"Length: {len(text)}")

خروجی:

Length: 18

این دقیقاً همان جایی است که مفاهیم مختلف شروع به ترکیب شدن می کنند.

---

# قالب بندی اعداد

String Formatting هنگام کار با اعداد اهمیت بسیار زیادی پیدا می کند.

فرض کنید:

price = 19.987654

اگر بنویسیم:

print(f"Price: {price}")

خروجی:

Price: 19.987654

اما شاید فقط دو رقم اعشار بخواهیم.

می توانیم بنویسیم:

print(f"Price: {price:.2f}")

خروجی:

Price: 19.99

ساختار کلی:

{value:.2f}

در اینجا:

- `:` شروع دستور قالب بندی است.
- `.2` یعنی دو رقم اعشار.
- `f` یعنی Fixed-Point notation.

---

# مثال های بیشتر با `.2f`

number = 10

print(f"{number:.2f}")

خروجی:

10.00

مثال دیگر:

number = 3.14159265

print(f"{number:.2f}")

خروجی:

3.14

و:

print(f"{number:.4f}")

خروجی:

3.1416

---

# گرد کردن و قالب بندی

وقتی یک عدد را با دو رقم اعشار نمایش می دهیم، نحوه نمایش آن تغییر می کند.

برای مثال:

number = 7.456

print(f"{number:.2f}")

خروجی:

7.46

اما مقدار اصلی متغیر تغییر نکرده است:

number = 7.456

print(f"{number:.2f}")
print(number)

خروجی:

7.46
7.456

قالب بندی فقط نحوه نمایش مقدار را کنترل می کند.

---

# جداکننده هزارگان

اعداد بزرگ ممکن است خواندن سختی داشته باشند.

برای مثال:

population = 12500000

print(f"{population:,}")

خروجی:

12,500,000

می توانیم جداکننده هزارگان را با قالب بندی اعشار ترکیب کنیم:

number = 1234567.891

print(f"{number:,.2f}")

خروجی:

1,234,567.89

این قابلیت برای مواردی مثل:

- پول
- جمعیت
- آمار
- مقادیر بزرگ
- داده های مالی

بسیار کاربردی است.

---

# قالب بندی درصد

فرض کنید:

rate = 0.875

اگر بنویسیم:

print(f"{rate}")

خروجی:

0.875

اما شاید بخواهیم:

87.5%

نمایش داده شود.

از قالب بندی `%` استفاده می کنیم:

print(f"{rate:.1%}")

خروجی:

87.5%

پایتون مقدار را به درصد تبدیل می کند و علامت `%` را اضافه می کند.

مثال دیگر:

success_rate = 0.9234

print(f"Success rate: {success_rate:.2%}")

خروجی:

Success rate: 92.34%

---

# تفاوت `.2f` و `.2%`

این دو قالب با هم متفاوت هستند.

برای:

rate = 0.92

اگر بنویسیم:

print(f"{rate:.2f}")

خروجی:

0.92

اما:

print(f"{rate:.2%}")

خروجی:

92.00%

پس:

`.2f`

یعنی دو رقم اعشار.

`.2%`

یعنی درصد با دو رقم اعشار.

---

# نمایش علامت مثبت و منفی

می توانیم نحوه نمایش علامت اعداد را نیز کنترل کنیم.

برای مثال:

profit = 2500

print(f"Profit: {profit:+}")

خروجی:

Profit: +2500

و:

loss = -500

print(f"Loss: {loss:+}")

خروجی:

Loss: -500

گزینه `+` باعث می شود علامت عدد به صورت صریح نمایش داده شود.

---

# Width

گاهی می خواهیم مقدار در یک فضای مشخص قرار بگیرد.

برای مثال:

name = "Ahmad"

print(f"{name:10}")

String داخل یک Field با عرض ۱۰ کاراکتر قرار می گیرد.

این قابلیت هنگام ساخت جدول بسیار کاربردی است.

---

# تراز کردن از چپ

برای تراز کردن از سمت چپ از:

`<`

استفاده می کنیم.

مثال:

name = "Ahmad"

print(f"{name:<10}")

متن از سمت چپ Field قرار می گیرد.

به صورت مفهومی:

Ahmad     

---

# تراز کردن از راست

برای تراز کردن از سمت راست از:

`>`

استفاده می کنیم.

مثال:

name = "Ahmad"

print(f"{name:>10}")

به صورت مفهومی:

     Ahmad

متن از سمت راست Field قرار می گیرد.

---

# تراز کردن در مرکز

برای قرار دادن متن در مرکز از:

`^`

استفاده می کنیم.

مثال:

name = "Ahmad"

print(f"{name:^10}")

متن در مرکز Field قرار می گیرد.

---

# کاراکتر پرکننده

می توانیم تعیین کنیم فضای خالی با چه کاراکتری پر شود.

برای مثال:

name = "Ahmad"

print(f"{name:*<10}")

خروجی:

Ahmad*****

کاراکتر `*` به عنوان Fill Character استفاده شده است.

می توانیم با Right Alignment نیز استفاده کنیم:

print(f"{name:*>10}")

خروجی:

*****Ahmad

یا Center Alignment:

print(f"{name:*^10}")

خروجی:

**Ahmad***

این قابلیت برای ساخت رابط های ساده در Console مفید است.

---

# قالب بندی اعداد با Width

Width را می توان برای اعداد نیز استفاده کرد.

score = 95

print(f"{score:>10}")

عدد در سمت راست یک Field با عرض ۱۰ قرار می گیرد.

این روش هنگام ساخت ستون های عددی بسیار کاربردی است.

---

# ساخت یک جدول ساده

فرض کنید:

name1 = "Ahmad"
score1 = 95

name2 = "Sara"
score2 = 88

می توانیم بنویسیم:

print(f"{'Name':<10}{'Score':>10}")
print(f"{name1:<10}{score1:>10}")
print(f"{name2:<10}{score2:>10}")

خروجی:

Name           Score
Ahmad             95
Sara              88

حالا خروجی بسیار مرتب تر شده است.

---

# ترکیب Width و قالب بندی اعشار

می توانیم چند دستور قالب بندی را با هم ترکیب کنیم.

برای مثال:

price = 1234.5678

print(f"{price:>15,.2f}")

خروجی:

       1,234.57

در اینجا داریم:

`>` → تراز کردن از راست

`15` → عرض Field

`,` → جداکننده هزارگان

`.2f` → دو رقم اعشار

این مثال خوبی برای ترکیب چند دستور قالب بندی است.

---

# ساختار کلی Format Specifier

به صورت ساده می توانیم قالب بندی را این طور تصور کنیم:

{value:[fill][align][width][,][.precision][type]}

لازم نیست همیشه همه قسمت ها را بنویسیم.

مثلاً:

{price:.2f}

فقط Precision و Type را دارد.

یا:

{name:<10}

از Alignment و Width استفاده می کند.

یا:

{number:,.2f}

از جداکننده هزارگان و Precision استفاده می کند.

وقتی اجزای مختلف را بشناسیم، قالب بندی های پیچیده تر نیز بسیار ساده تر می شوند.

---

# قالب بندی با `format()`

قبل از اینکه f-string به روش رایج تبدیل شود، برنامه نویسان پایتون زیاد از متد `format()` استفاده می کردند.

مثال:

name = "Ahmad"
age = 25

print("My name is {} and I am {} years old.".format(name, age))

خروجی:

My name is Ahmad and I am 25 years old.

علامت های `{}` نقش Placeholder دارند.

مقدارها با:

format()

تأمین می شوند.

---

# آرگومان های Position در `format()`

می توانیم موقعیت آرگومان ها را مشخص کنیم.

name = "Ahmad"
age = 25

print("Name: {0}, Age: {1}".format(name, age))

خروجی:

Name: Ahmad, Age: 25

می توانیم ترتیب را نیز تغییر دهیم:

print("Age: {1}, Name: {0}".format(name, age))

خروجی:

Age: 25, Name: Ahmad

---

# آرگومان های نام گذاری شده در `format()`

می توانیم از آرگومان های نام گذاری شده نیز استفاده کنیم.

print(
    "Name: {name}, Age: {age}".format(
        name="Ahmad",
        age=25
    )
)

خروجی:

Name: Ahmad, Age: 25

این روش در Formattingهای پیچیده می تواند خوانایی را بهتر کند.

---

# قالب بندی اعداد با `format()`

همان روش های قالب بندی را می توانیم با `format()` نیز استفاده کنیم.

price = 19.987654

print("Price: {:.2f}".format(price))

خروجی:

Price: 19.99

جداکننده هزارگان:

number = 1234567

print("{:,}".format(number))

خروجی:

1,234,567

درصد:

rate = 0.875

print("{:.1%}".format(rate))

خروجی:

87.5%

---

# مقایسه f-String و `format()`

مقایسه کنید:

### f-string

name = "Ahmad"
age = 25

print(f"My name is {name} and I am {age} years old.")

### `format()`

name = "Ahmad"
age = 25

print("My name is {} and I am {} years old.".format(name, age))

هر دو روش درست هستند.

اما در Python مدرن معمولاً f-string به دلیل کوتاه تر و خواناتر بودن ترجیح داده می شود.

---

# قالب بندی Expressionها

در f-string می توانیم نتیجه یک Expression را نیز قالب بندی کنیم.

a = 10
b = 3

print(f"Result: {a / b:.2f}")

خروجی:

Result: 3.33

در اینجا:

a / b

ابتدا محاسبه می شود.

سپس نتیجه با دو رقم اعشار نمایش داده می شود.

---

# قالب بندی نتیجه یک محاسبه

می توانیم محاسبات و Formatting را با هم ترکیب کنیم.

price = 100
discount = 0.15

final_price = price * (1 - discount)

print(f"Final price: ${final_price:.2f}")

خروجی:

Final price: $85.00

این مثال نسبت به قالب بندی یک متغیر ساده، کاربرد واقعی تری دارد.

---

# قالب بندی ورودی کاربر

به یاد داشته باشید که `input()` همیشه یک String برمی گرداند.

فرض کنید:

age = input("Enter your age: ")

اگر کاربر وارد کند:

25

متغیر:

age

هنوز String است.

اگر به Integer نیاز داشته باشیم:

age = int(input("Enter your age: "))

حالا می توانیم محاسبات انجام دهیم:

age = int(input("Enter your age: "))

print(f"Next year you will be {age + 1}.")

---

# مثال کاربردی — گزارش دانش آموز

فرض کنید:

name = "Ahmad"
math = 18.5
physics = 17.75
programming = 19.25

average = (math + physics + programming) / 3

print(f"Student: {name}")
print(f"Math: {math:.2f}")
print(f"Physics: {physics:.2f}")
print(f"Programming: {programming:.2f}")
print(f"Average: {average:.2f}")

خروجی:

Student: Ahmad
Math: 18.50
Physics: 17.75
Programming: 19.25
Average: 18.50

---

# مثال کاربردی — رسید خرید

product = "Keyboard"
price = 49.987
quantity = 2

total = price * quantity

print("----- Receipt -----")
print(f"Product: {product}")
print(f"Price: ${price:.2f}")
print(f"Quantity: {quantity}")
print(f"Total: ${total:.2f}")

خروجی:

----- Receipt -----
Product: Keyboard
Price: $49.99
Quantity: 2
Total: $99.97

---

# مثال کاربردی — امتیاز بازی

player = "Ahmad"
score = 12500
accuracy = 0.9345

print(f"Player: {player}")
print(f"Score: {score:,}")
print(f"Accuracy: {accuracy:.1%}")

خروجی:

Player: Ahmad
Score: 12,500
Accuracy: 93.5%

---

# مثال کاربردی — تایمر

seconds = 125

minutes = seconds // 60
remaining_seconds = seconds % 60

print(f"Time remaining: {minutes}:{remaining_seconds:02d}")

خروجی:

Time remaining: 2:05

قسمت مهم:

`02d`

یعنی عدد باید حداقل دو رقم داشته باشد.

بنابراین:

5

به شکل:

05

نمایش داده می شود.

این تکنیک برای مواردی مثل:

- Timer
- ساعت
- تاریخ
- امتیاز
- شمارنده

بسیار کاربردی است.

---

# Zero Padding

فرض کنید:

number = 7

print(f"{number:02d}")

خروجی:

07

برای سه رقم:

print(f"{number:03d}")

خروجی:

007

مثال دیگر:

hour = 9
minute = 5
second = 3

print(f"{hour:02d}:{minute:02d}:{second:02d}")

خروجی:

09:05:03

این یکی از تکنیک های رایج Formatting است.

---

# نمایش آکولادهای واقعی

آکولادها داخل f-string معنای خاصی دارند.

برای مثال:

name = "Ahmad"

print(f"Hello {name}")

اینجا:

{name}

یعنی مقدار متغیر `name` را قرار بده.

اما اگر واقعاً بخواهیم آکولاد نمایش دهیم چه؟

از آکولاد دوتایی استفاده می کنیم:

print(f"{{name}}")

خروجی:

{name}

بنابراین:

`{{`

یک:

{

می سازد.

و:

`}}`

یک:

}

می سازد.

---

# قالب بندی Boolean

می توانیم مقدارهای Boolean را نیز داخل f-string قرار دهیم.

is_logged_in = True

print(f"Logged in: {is_logged_in}")

خروجی:

Logged in: True

می توانیم Expression نیز استفاده کنیم:

age = 20

print(f"Adult: {age >= 18}")

خروجی:

Adult: True

این مثال نشان می دهد Expression داخل `{}` می تواند یک مقدار Boolean نیز تولید کند.

---

# استفاده از Conditional Expression

پایتون اجازه می دهد Conditional Expression را نیز داخل f-string قرار دهیم.

age = 20

print(f"Status: {'Adult' if age >= 18 else 'Minor'}")

خروجی:

Status: Adult

این قابلیت قدرتمند است، اما بهتر است قبل از استفاده از Expressionهای پیچیده، ساختار ساده f-string را کاملاً یاد بگیریم.

---

# Formatting و خوانایی

String Formatting فقط برای زیباتر کردن خروجی نیست.

باعث خواناتر شدن خود کد نیز می شود.

این دو کد را مقایسه کنید:

name = "Ahmad"
score = 95

print("Student " + name + " has a score of " + str(score) + ".")

و:

print(f"Student {name} has a score of {score}.")

نسخه دوم بسیار ساده تر خوانده می شود.

Formatting خوب کمک می کند کدی بنویسیم که افراد دیگر نیز بتوانند آن را راحت تر بخوانند و نگهداری کنند.

---

# یک مثال کامل

حالا چند مفهوم بخش های قبلی را با هم ترکیب کنیم.

برنامه از کاربر:

- نام
- سن
- نمره

را دریافت می کند و یک گزارش مرتب می سازد.

name = input("Enter your name: ").strip().title()
age = int(input("Enter your age: "))
score = float(input("Enter your score: "))

print()
print("----- Student Report -----")
print(f"Name: {name}")
print(f"Age: {age}")
print(f"Score: {score:.2f}")

خروجی می تواند چیزی شبیه این باشد:

----- Student Report -----
Name: Ahmad
Age: 25
Score: 92.50

در این مثال چند مفهوم را با هم ترکیب کرده ایم:

- `input()`
- `strip()`
- `title()`
- `int()`
- `float()`
- f-string
- Number Formatting

این دقیقاً نوع ترکیبی است که باید در ادامه پروژه بیشتر تمرین کنیم.

---

# تمرین ها

## تمرین ۱ — f-String ساده

کد زیر را ایجاد کنید:

name = "Ali"
age = 20

با استفاده از f-string خروجی زیر را ایجاد کنید:

My name is Ali and I am 20 years old.

---

## تمرین ۲ — چند متغیر

ایجاد کنید:

name = "Sara"
city = "Shiraz"
age = 22

هر سه مقدار را با استفاده از یک f-string در یک جمله نمایش دهید.

---

## تمرین ۳ — Expression داخل `{}`

ایجاد کنید:

a = 15
b = 7

خروجی:

The sum is 22.

را تولید کنید.

این بار Expression را مستقیماً داخل f-string قرار دهید.

---

## تمرین ۴ — استفاده از String Method داخل f-String

ایجاد کنید:

name = "aHMAD"

با استفاده از `title()` داخل f-string خروجی:

Hello Ahmad!

را ایجاد کنید.

---

## تمرین ۵ — Indexing و Formatting

ایجاد کنید:

text = "Python"

با استفاده از یک f-string نمایش دهید:

First character: P
Last character: n

برای پیدا کردن این دو کاراکتر از String Indexing استفاده کنید.

---

## تمرین ۶ — Slicing و Formatting

ایجاد کنید:

text = "Programming"

خروجی:

First four characters: Prog

را با استفاده از Slicing داخل f-string تولید کنید.

---

## تمرین ۷ — قالب بندی اعشار

ایجاد کنید:

price = 19.98765

قیمت را دقیقاً با دو رقم اعشار نمایش دهید.

نتیجه:

19.99

---

## تمرین ۸ — درصد

ایجاد کنید:

success_rate = 0.8765

خروجی:

87.65%

را با استفاده از Percentage Formatting نمایش دهید.

---

## تمرین ۹ — جداکننده هزارگان

ایجاد کنید:

population = 12500000

خروجی:

12,500,000

را تولید کنید.

---

## تمرین ۱۰ — ترکیب قالب های عددی

ایجاد کنید:

price = 1234567.8912

خروجی:

1,234,567.89

را تولید کنید.

از:

- جداکننده هزارگان
- دو رقم اعشار

هم زمان استفاده کنید.

---

## تمرین ۱۱ — Alignment

ایجاد کنید:

name = "Ahmad"

نام را:

- از چپ در یک Field با عرض ۱۵
- از راست در یک Field با عرض ۱۵
- در مرکز یک Field با عرض ۱۵

نمایش دهید.

---

## تمرین ۱۲ — Custom Fill

ایجاد کنید:

name = "Python"

با استفاده از `*` به عنوان Fill Character خروجی هایی مشابه این ایجاد کنید:

Python*********
*********Python
****Python*****

سعی کنید دقیقاً متوجه شوید Width و Alignment چگونه کار می کنند.

---

## تمرین ۱۳ — میانگین دانش آموز

ایجاد کنید:

math = 18.5
physics = 17.25
programming = 19.75

میانگین را محاسبه کنید و با دو رقم اعشار نمایش دهید.

---

## تمرین ۱۴ — رسید خرید

ایجاد کنید:

product = "Mouse"
price = 25.987
quantity = 3

مجموع قیمت را محاسبه کنید.

خروجی:

----- Receipt -----
Product: Mouse
Price: $25.99
Quantity: 3
Total: $77.96

---

## تمرین ۱۵ — ورودی کاربر

از کاربر:

- نام
- سن
- شهر

را دریافت کنید.

سپس تمام اطلاعات را با استفاده از f-string نمایش دهید.

نام را حتماً با `strip()` تمیز کنید.

---

## تمرین ۱۶ — محاسبه سن

سن کاربر را دریافت کنید.

نمایش دهید:

Current age: 25
Next year: 26
In five years: 30

عددها باید توسط برنامه محاسبه شوند و نباید دستی نوشته شوند.

---

## تمرین ۱۷ — قالب بندی Timer

از کاربر تعداد ثانیه را دریافت کنید.

آن را به:

minutes
seconds

تبدیل کنید.

سپس در قالب زیر نمایش دهید:

02:05

از Zero Padding استفاده کنید.

---

## تمرین ۱۸ — امتیاز بازی

ایجاد کنید:

player = "Ahmad"
score = 12500
accuracy = 0.9345

خروجی:

Player: Ahmad
Score: 12,500
Accuracy: 93.45%

را ایجاد کنید.

---

# چالش نهایی الگوریتمی

برنامه ای با نام:

Student Report Generator

بسازید.

برنامه باید از کاربر اطلاعات زیر را دریافت کند:

1. نام دانش آموز
2. سن دانش آموز
3. نمره ریاضی
4. نمره فیزیک
5. نمره برنامه نویسی

سپس برنامه باید:

1. نام دانش آموز را با `strip()` تمیز کند.
2. نام را با `title()` قالب بندی کند.
3. سن را به Integer تبدیل کند.
4. نمره ها را به Floating-Point تبدیل کند.
5. میانگین نمره ها را محاسبه کند.
6. درصد میانگین نسبت به ۲۰ را محاسبه کند.
7. مشخص کند دانش آموز قبول شده یا نه.
8. یک گزارش مرتب و قالب بندی شده نمایش دهد.

خروجی باید چیزی شبیه این باشد:

----- Student Report -----

Name: Ahmad Ahmadi
Age: 20

Math:         18.50
Physics:      17.75
Programming:  19.25

Average:      18.50
Percentage:   92.50%
Status:       Passed

تمام مقدارها باید به صورت Dynamic محاسبه شوند.

نباید عددهای نهایی را به صورت دستی داخل خروجی بنویسید.

---

# با تفکر الگوریتمی شروع کنید

قبل از نوشتن کد، مسئله را به چند مرحله کوچک تقسیم کنید.

به این روند فکر کنید:

دریافت نام
↓
تمیز کردن نام
↓
قالب بندی نام
↓
دریافت سن
↓
تبدیل سن به Integer
↓
دریافت نمره ریاضی
↓
تبدیل به Float
↓
دریافت نمره فیزیک
↓
تبدیل به Float
↓
دریافت نمره برنامه نویسی
↓
تبدیل به Float
↓
محاسبه میانگین
↓
محاسبه درصد
↓
بررسی وضعیت قبولی
↓
قالب بندی اعداد
↓
نمایش گزارش

حالا مشخص کنید برای حل این مسئله به کدام مفاهیم بخش های قبلی نیاز دارید.

باید متوجه شوید که این چالش چند مفهوم را با هم ترکیب می کند:

- input
- String
- String Method
- `strip()`
- `title()`
- Type Conversion
- Integer
- Float
- Arithmetic
- Condition
- f-String
- Number Formatting

این ترکیب کاملاً عمدی است.

هدف فقط یادگیری String Formatting نیست.

هدف این است که یاد بگیریم چگونه چند مفهوم برنامه نویسی را برای حل یک مسئله واقعی با هم ترکیب کنیم.

---

# پاسخ چالش نهایی

قبل از دیدن جواب، ابتدا خودتان مسئله را حل کنید.

یک راه حل ممکن:

name = input("Enter student name: ").strip().title()
age = int(input("Enter student age: "))

math = float(input("Enter Math score: "))
physics = float(input("Enter Physics score: "))
programming = float(input("Enter Programming score: "))

average = (math + physics + programming) / 3
percentage = (average / 20) * 100

if average >= 10:
    status = "Passed"
else:
    status = "Failed"

print()
print("----- Student Report -----")
print()
print(f"Name: {name}")
print(f"Age: {age}")
print()
print(f"Math:         {math:.2f}")
print(f"Physics:      {physics:.2f}")
print(f"Programming:  {programming:.2f}")
print()
print(f"Average:      {average:.2f}")
print(f"Percentage:   {percentage:.2f}%")
print(f"Status:       {status}")

نکته مهم این است که هدف، حفظ کردن این جواب نیست.

هدف این است که بفهمیم چگونه الگوریتم را به کد تبدیل کرده ایم.

---

