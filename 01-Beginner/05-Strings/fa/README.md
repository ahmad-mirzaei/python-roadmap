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
