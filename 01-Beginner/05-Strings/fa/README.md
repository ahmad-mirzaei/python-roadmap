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

# بخش ۶ — قالب‌بندی رشته‌ها (String Formatting)

در بخش‌های قبلی یاد گرفتیم که چگونه رشته‌ها را بسازیم، به کاراکترهای آن‌ها دسترسی پیدا کنیم، آن‌ها را Slicing کنیم و از متدهای رشته استفاده کنیم.

حالا می‌خواهیم یاد بگیریم چطور رشته‌ها را **کاربردی‌تر و خواناتر** کنیم؛ یعنی بتوانیم مقادیر متغیرها را داخل متن قرار دهیم.

به این کار **String Formatting** یا **قالب‌بندی رشته‌ها** می‌گوییم.

قالب‌بندی رشته‌ها در برنامه‌های واقعی بسیار مهم است، چون برنامه‌ها معمولاً باید اطلاعاتی را که داخل متغیرها قرار دارند به کاربر نمایش دهند.

مثلاً به جای اینکه بنویسیم:

```python
name = "Ahmad"
age = 25

print("My name is Ahmad and I am 25 years old.")
```

می‌خواهیم برنامه خودش از متغیرها استفاده کند:

```python
name = "Ahmad"
age = 25

print(f"My name is {name} and I am {age} years old.")
```

روش دوم بسیار کاربردی‌تر است، چون مقدار متغیرها می‌تواند تغییر کند.

---

## چرا به String Formatting نیاز داریم؟

فرض کنید اطلاعات یک دانش‌آموز را داریم:

```python
name = "Sara"
age = 20
score = 18.75
```

می‌توانیم هر مقدار را جداگانه چاپ کنیم:

```python
print("Name:", name)
print("Age:", age)
print("Score:", score)
```

این روش درست است، اما گاهی می‌خواهیم یک جمله کامل بسازیم:

```python
print(f"{name} is {age} years old and scored {score}.")
```

خروجی:

```text
Sara is 20 years old and scored 18.75.
```

قالب‌بندی رشته به ما اجازه می‌دهد این موارد را داخل یک رشته ترکیب کنیم:

- متن
- متغیرها
- مقادیر محاسبه‌شده
- اعداد
- عبارت‌های پایتون

---

# f-String چیست؟

رایج‌ترین و پیشنهادی‌ترین روش قالب‌بندی رشته‌ها در پایتون امروزی، استفاده از **f-string** است.

حرف `f` را قبل از علامت نقل قول قرار می‌دهیم.

مثلاً:

```python
name = "Ahmad"

print(f"Hello, {name}!")
```

خروجی:

```text
Hello, Ahmad!
```

اگر `f` را فراموش کنیم:

```python
name = "Ahmad"

print("Hello, {name}!")
```

خروجی:

```text
Hello, {name}!
```

پس این دو با هم تفاوت دارند.

درست:

```python
f"Hello, {name}!"
```

نادرست برای جایگذاری متغیر:

```python
"Hello, {name}!"
```

---

# f-String چگونه کار می‌کند؟

به این مثال توجه کن:

```python
name = "Ahmad"
age = 25

message = f"My name is {name} and I am {age} years old."

print(message)
```

پایتون این قسمت را می‌بیند:

```python
f"My name is {name} and I am {age} years old."
```

هر چیزی که داخل `{}` قرار گرفته باشد، به عنوان یک عبارت پایتون ارزیابی می‌شود.

بنابراین:

```python
{name}
```

به:

```text
Ahmad
```

تبدیل می‌شود.

و:

```python
{age}
```

به:

```text
25
```

تبدیل می‌شود.

در نتیجه رشته نهایی می‌شود:

```text
My name is Ahmad and I am 25 years old.
```

---

# قرار دادن چند متغیر در یک رشته

هر تعداد متغیر که نیاز داشته باشیم می‌توانیم داخل یک f-string قرار دهیم.

```python
first_name = "Ali"
last_name = "Ahmadi"
age = 22

print(f"Name: {first_name} {last_name}")
print(f"Age: {age}")
```

خروجی:

```text
Name: Ali Ahmadi
Age: 22
```

مثال دیگر:

```python
product = "Keyboard"
price = 49.99
quantity = 2

print(f"Product: {product}")
print(f"Price: {price}")
print(f"Quantity: {quantity}")
```

خروجی:

```text
Product: Keyboard
Price: 49.99
Quantity: 2
```

---

# قرار دادن Expression داخل f-String

یکی از ویژگی‌های بسیار مهم f-string این است که فقط مجبور نیستیم نام متغیر را داخل `{}` قرار دهیم.

می‌توانیم یک **Expression** یا عبارت پایتون را نیز داخل آن بنویسیم.

مثلاً:

```python
a = 10
b = 5

print(f"Sum: {a + b}")
```

خروجی:

```text
Sum: 15
```

می‌توانیم ضرب انجام دهیم:

```python
price = 20
quantity = 3

print(f"Total: {price * quantity}")
```

خروجی:

```text
Total: 60
```

حتی می‌توانیم محاسبات پیچیده‌تر انجام دهیم:

```python
math = 18
physics = 16
programming = 20

average = (math + physics + programming) / 3

print(f"Average: {average}")
```

خروجی:

```text
Average: 18.0
```

پس یک قانون مهم داریم:

> هر چیزی که داخل `{}` در یک f-string قرار می‌گیرد، به عنوان یک Expression پایتون ارزیابی می‌شود.

مثلاً:

```python
name = "Ahmad"
age = 25

print(f"{name} will be {age + 1} next year.")
```

خروجی:

```text
Ahmad will be 26 next year.
```

---

# استفاده از متدهای رشته داخل f-String

حتی می‌توانیم داخل `{}` از متدها استفاده کنیم.

مثلاً:

```python
name = "ahmad"

print(f"Hello, {name.title()}!")
```

خروجی:

```text
Hello, Ahmad!
```

مثال دیگر:

```python
name = "  ahmad  "

print(f"Hello, {name.strip().title()}!")
```

خروجی:

```text
Hello, Ahmad!
```

این ویژگی زمانی بسیار کاربردی است که ورودی کاربر ممکن است فاصله‌های اضافی یا حروف با حروف بزرگ و کوچک نامنظم داشته باشد.

مثلاً:

```python
name = input("Enter your name: ").strip().title()

print(f"Welcome, {name}!")
```

اگر کاربر وارد کند:

```text
   ahmad
```

خروجی می‌شود:

```text
Welcome, Ahmad!
```

---

# قالب‌بندی اعداد

قالب‌بندی رشته زمانی اهمیت بیشتری پیدا می‌کند که با اعداد کار می‌کنیم.

فرض کنیم:

```python
price = 49.99
```

می‌توانیم آن را مستقیماً چاپ کنیم:

```python
print(f"Price: {price}")
```

خروجی:

```text
Price: 49.99
```

اما گاهی می‌خواهیم مشخص کنیم چند رقم اعشار نمایش داده شود.

مثلاً:

```python
price = 49.999999

print(f"Price: {price:.2f}")
```

خروجی:

```text
Price: 50.00
```

قسمت مهم اینجاست:

```python
:.2f
```

بیایید آن را باز کنیم.

---

## `:.2f` یعنی چه؟

به این عبارت توجه کن:

```python
f"{price:.2f}"
```

ساختار کلی این است:

```text
{value:format}
```

در اینجا:

- `price` مقدار مورد نظر است.
- `:` شروع دستور قالب‌بندی است.
- `.2` یعنی دو رقم بعد از ممیز نمایش داده شود.
- `f` یعنی عدد به صورت اعشاری با تعداد مشخصی رقم اعشار نمایش داده شود.

مثلاً:

```python
number = 12.34567

print(f"{number:.1f}")
print(f"{number:.2f}")
print(f"{number:.3f}")
```

خروجی:

```text
12.3
12.35
12.346
```

پایتون در صورت نیاز عدد را گرد می‌کند.

مثلاً:

```python
score = 17.876

print(f"Score: {score:.2f}")
```

خروجی:

```text
Score: 17.88
```

---

# قالب‌بندی درصد

فرض کنیم نمره به صورت اعشاری ذخیره شده است:

```python
score = 0.875
```

اگر معمولی چاپ کنیم:

```python
print(score)
```

خروجی:

```text
0.875
```

اما ممکن است بخواهیم خروجی این شکلی باشد:

```text
87.50%
```

می‌توانیم از `%` در قالب‌بندی استفاده کنیم:

```python
print(f"{score:.2%}")
```

خروجی:

```text
87.50%
```

قسمت:

```python
.2%
```

دو کار انجام می‌دهد:

1. مقدار اعشاری را به درصد تبدیل می‌کند.
2. دو رقم اعشار نمایش می‌دهد.

مثلاً:

```python
value = 0.5

print(f"{value:.2%}")
```

خروجی:

```text
50.00%
```

مثال دیگر:

```python
value = 0.875

print(f"{value:.1%}")
```

خروجی:

```text
87.5%
```

---

# قالب‌بندی قیمت و پول

یکی از کاربردهای بسیار رایج قالب‌بندی، نمایش قیمت است.

مثلاً:

```python
price = 1499.5

print(f"${price:.2f}")
```

خروجی:

```text
$1499.50
```

می‌توانیم قالب‌بندی را با محاسبات ترکیب کنیم:

```python
price = 49.99
quantity = 3

total = price * quantity

print(f"Total: ${total:.2f}")
```

خروجی:

```text
Total: $149.97
```

---

# جداکننده هزارگان

اعداد بزرگ ممکن است سخت خوانده شوند.

مثلاً:

```python
population = 12500000

print(population)
```

خروجی:

```text
12500000
```

می‌توانیم از جداکننده هزارگان استفاده کنیم:

```python
print(f"{population:,}")
```

خروجی:

```text
12,500,000
```

این ویژگی برای مواردی مثل موارد زیر بسیار کاربردی است:

- جمعیت
- پول
- اندازه‌های بزرگ
- آمار
- امتیازها
- اندازه فایل‌ها

مثال:

```python
salary = 125000

print(f"Salary: ${salary:,}")
```

خروجی:

```text
Salary: $125,000
```

---

# ترکیب چند نوع قالب‌بندی

می‌توانیم چند دستور قالب‌بندی را با هم ترکیب کنیم.

مثلاً:

```python
price = 1234567.89123

print(f"${price:,.2f}")
```

خروجی:

```text
$1,234,567.89
```

اینجا:

```text
,
```

جداکننده هزارگان اضافه می‌کند.

و:

```text
.2f
```

باعث می‌شود دو رقم اعشار نمایش داده شود.

این الگو برای نمایش اطلاعات مالی بسیار کاربردی است.

---

# Alignment یا تراز کردن متن

گاهی می‌خواهیم اطلاعات در خروجی مرتب و هم‌راستا باشند.

پایتون به ما اجازه می‌دهد عرض مشخصی برای مقدار در نظر بگیریم.

مثلاً:

```python
name = "Ali"

print(f"{name:10}")
```

اینجا فضای مشخصی برای ۱۰ کاراکتر در نظر گرفته می‌شود.

می‌توانیم متن را به سمت چپ تراز کنیم:

```python
name = "Ali"

print(f"{name:<10}")
```

تراز از سمت راست:

```python
name = "Ali"

print(f"{name:>10}")
```

تراز در مرکز:

```python
name = "Ali"

print(f"{name:^10}")
```

این ویژگی زمانی بسیار کاربردی است که بخواهیم یک جدول ساده در خروجی ایجاد کنیم.

---

# ساخت یک جدول ساده

مثلاً:

```python
name1 = "Ali"
score1 = 18

name2 = "Sara"
score2 = 19

print(f"{'Name':<10}{'Score':>10}")
print(f"{name1:<10}{score1:>10}")
print(f"{name2:<10}{score2:>10}")
```

خروجی:

```text
Name           Score
Ali               18
Sara              19
```

قالب‌بندی باعث شده خروجی مرتب‌تر و خواناتر باشد.

---

# قالب‌بندی مقادیر Boolean

مقادیر Boolean نیز می‌توانند داخل f-string قرار بگیرند.

```python
is_student = True

print(f"Student: {is_student}")
```

خروجی:

```text
Student: True
```

مثال دیگر:

```python
age = 20
is_adult = age >= 18

print(f"Age: {age}")
print(f"Adult: {is_adult}")
```

خروجی:

```text
Age: 20
Adult: True
```

---

# نمایش نتیجه شرط‌ها

می‌توانیم یک مقدار را محاسبه کنیم و همان لحظه آن را نمایش دهیم.

```python
age = 20

print(f"Can vote: {age >= 18}")
```

خروجی:

```text
Can vote: True
```

این روش برای Debug کردن برنامه‌ها و نمایش نتیجه عملیات منطقی نیز مفید است.

---

# استفاده از Conditional Expression

پایتون اجازه می‌دهد یک عبارت شرطی را نیز داخل f-string قرار دهیم.

مثلاً:

```python
age = 20

print(f"Status: {'Adult' if age >= 18 else 'Minor'}")
```

خروجی:

```text
Status: Adult
```

مثال دیگر:

```python
score = 17

print(f"Result: {'Passed' if score >= 10 else 'Failed'}")
```

خروجی:

```text
Result: Passed
```

این روش برای شرط‌های ساده خوب است، اما اگر منطق برنامه پیچیده باشد، بهتر است ابتدا نتیجه را در یک متغیر ذخیره کنیم.

مثلاً:

```python
score = 17

if score >= 10:
    result = "Passed"
else:
    result = "Failed"

print(f"Result: {result}")
```

این روش معمولاً خواناتر است.

---

# ساخت خروجی چندخطی

f-string فقط برای یک خط نیست.

می‌توانیم از `\n` استفاده کنیم:

```python
name = "Ahmad"
age = 25
score = 18.5

print(f"Name: {name}\nAge: {age}\nScore: {score}")
```

خروجی:

```text
Name: Ahmad
Age: 25
Score: 18.5
```

برای متن‌های بزرگ‌تر نیز می‌توانیم از Triple Quotes استفاده کنیم:

```python
name = "Ahmad"
age = 25

message = f"""
----- Student Profile -----
Name: {name}
Age: {age}
---------------------------
"""

print(message)
```

خروجی:

```text
----- Student Profile -----
Name: Ahmad
Age: 25
---------------------------
```

این روش برای ساخت گزارش‌ها و خروجی‌های مرتب بسیار کاربردی است.

---

# قالب‌بندی ورودی کاربر

قالب‌بندی رشته وقتی با `input()` ترکیب شود، بسیار کاربردی‌تر می‌شود.

مثلاً:

```python
name = input("Enter your name: ").strip().title()
age = int(input("Enter your age: "))

print(f"Hello, {name}!")
print(f"You are {age} years old.")
```

اگر کاربر وارد کند:

```text
ahmad
25
```

خروجی:

```text
Hello, Ahmad!
You are 25 years old.
```

در این مثال چند مفهوم از بخش‌های قبلی با هم کار می‌کنند:

- `input()` اطلاعات را از کاربر می‌گیرد.
- `.strip()` فاصله‌های اضافی را حذف می‌کند.
- `.title()` حروف را برای نمایش بهتر قالب‌بندی می‌کند.
- `int()` سن را به عدد صحیح تبدیل می‌کند.
- f-string خروجی نهایی را قالب‌بندی می‌کند.

این دقیقاً همان چیزی است که در ادامه پروژه بیشتر با آن کار خواهیم کرد: **ترکیب مفاهیم قبلی برای ساخت برنامه‌های واقعی‌تر.**

---

# قالب‌بندی مقادیر محاسبه‌شده

فرض کنیم کاربر سه نمره وارد می‌کند.

```python
math = float(input("Enter Math score: "))
physics = float(input("Enter Physics score: "))
programming = float(input("Enter Programming score: "))

average = (math + physics + programming) / 3

print(f"Average: {average:.2f}")
```

اگر کاربر وارد کند:

```text
18
16
19
```

خروجی:

```text
Average: 17.67
```

می‌توانیم درصد را نیز محاسبه کنیم:

```python
percentage = (average / 20) * 100

print(f"Percentage: {percentage:.2f}%")
```

خروجی:

```text
Percentage: 88.33%
```

---

# یک گزارش کامل از اطلاعات دانش‌آموز

حالا بیایید همه مفاهیمی را که تا اینجا یاد گرفته‌ایم با هم ترکیب کنیم.

```python
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
print(f"Name: {name}")
print(f"Age: {age}")
print(f"Math: {math:.2f}")
print(f"Physics: {physics:.2f}")
print(f"Programming: {programming:.2f}")
print(f"Average: {average:.2f}")
print(f"Percentage: {percentage:.2f}%")
print(f"Status: {status}")
```

نمونه ورودی:

```text
Enter student name:   alex
Enter student age: 20
Enter Math score: 18
Enter Physics score: 17
Enter Programming score: 18.5
```

خروجی:

```text
----- Student Report -----
Name: Alex
Age: 20
Math: 18.00
Physics: 17.00
Programming: 18.50
Average: 17.83
Percentage: 89.17%
Status: Passed
```

این برنامه کوچک، چند مفهوم مختلف را با هم ترکیب می‌کند:

- متغیرها
- رشته‌ها
- `input()`
- `int()`
- `float()`
- `.strip()`
- `.title()`
- عملیات ریاضی
- مقایسه
- `if / else`
- f-string
- قالب‌بندی اعداد

این همان جایی است که مفاهیم مختلف برنامه‌نویسی کم‌کم شروع می‌کنند به تبدیل شدن به برنامه‌های کاربردی.

---

# اشتباه رایج — فراموش کردن `f`

اشتباه:

```python
name = "Ahmad"

print("Hello, {name}!")
```

خروجی:

```text
Hello, {name}!
```

درست:

```python
print(f"Hello, {name}!")
```

خروجی:

```text
Hello, Ahmad!
```

---

# اشتباه رایج — قرار دادن علامت نقل قول داخل `{}`

این حالت اشتباه است:

```python
name = "Ahmad"

print(f"Hello, {"name"}!")
```

این کد باعث خطای Syntax می‌شود.

حالت درست:

```python
print(f"Hello, {name}!")
```

نام متغیر نیازی به علامت نقل قول ندارد.

---

# اشتباه رایج — اشتباه گرفتن مقدار با نحوه نمایش آن

به این مثال توجه کن:

```python
score = 0.875

print(f"{score:.2f}")
```

خروجی:

```text
0.88
```

اما:

```python
print(f"{score:.2%}")
```

خروجی:

```text
87.50%
```

این تفاوت بسیار مهم است.

`.2f` یعنی:

> عدد را با دو رقم اعشار نمایش بده.

`.2%` یعنی:

> عدد اعشاری را به درصد تبدیل کن و با دو رقم اعشار نمایش بده.

---

# اشتباه رایج — Formatting مقدار اصلی متغیر را تغییر نمی‌دهد

به این مثال توجه کن:

```python
price = 12.3456

print(f"{price:.2f}")
print(price)
```

خروجی:

```text
12.35
12.3456
```

قالب‌بندی فقط نحوه نمایش مقدار را تغییر داده است.

مقدار اصلی `price` همچنان همان مقدار قبلی است.

اگر واقعاً بخواهیم مقدار ذخیره‌شده را گرد کنیم، می‌توانیم از `round()` استفاده کنیم:

```python
price = 12.3456

price = round(price, 2)

print(price)
```

خروجی:

```text
12.35
```

پس این دو مفهوم را از هم جدا نگه دار:

- Formatting روی **نحوه نمایش** تأثیر می‌گذارد.
- `round()` مقدار ذخیره‌شده را تغییر می‌دهد.

---

# تمرین‌ها

## تمرین ۱ — معرفی شخصی

متغیرهای زیر را ایجاد کن:

```python
name = "Ali"
age = 21
city = "Tehran"
```

خروجی زیر را ایجاد کن:

```text
My name is Ali.
I am 21 years old.
I live in Tehran.
```

حتماً از f-string استفاده کن.

---

## تمرین ۲ — اطلاعات محصول

متغیرهای زیر را ایجاد کن:

```python
product = "Keyboard"
price = 49.99
quantity = 2
```

خروجی:

```text
Product: Keyboard
Price: $49.99
Quantity: 2
```

از f-string استفاده کن.

---

## تمرین ۳ — محاسبه قیمت کل

با استفاده از:

```python
price = 49.99
quantity = 2
```

قیمت کل را محاسبه کن و نمایش بده:

```text
Total: $99.98
```

قیمت باید دقیقاً با دو رقم اعشار نمایش داده شود.

---

## تمرین ۴ — میانگین نمرات

سه نمره ایجاد کن:

```python
math = 18
physics = 16
programming = 19
```

میانگین را محاسبه کن و با دو رقم اعشار نمایش بده.

خروجی مورد انتظار:

```text
Average: 17.67
```

---

## تمرین ۵ — درصد

با داشتن:

```python
score = 0.875
```

خروجی زیر را ایجاد کن:

```text
Score: 87.50%
```

حتماً از Percentage Formatting استفاده کن.

---

## تمرین ۶ — پروفایل کاربر

از کاربر موارد زیر را دریافت کن:

- نام
- سن
- شهر

سپس خروجی مشابه زیر نمایش بده:

```text
----- User Profile -----
Name: Alex
Age: 25
City: Tehran
```

نام کاربر باید با:

```python
.strip().title()
```

تمیز و قالب‌بندی شود.

---

## تمرین ۷ — گزارش مستطیل

مقادیر زیر را ایجاد کن:

```python
width = 12.5
height = 8.2
```

موارد زیر را محاسبه کن:

- مساحت
- محیط

هر دو مقدار را با دو رقم اعشار نمایش بده.

فرمت خروجی:

```text
Width: 12.50
Height: 8.20
Area: 102.50
Perimeter: 41.40
```

---

## تمرین ۸ — رسید خرید

از کاربر موارد زیر را دریافت کن:

- نام محصول
- قیمت
- تعداد

قیمت کل را محاسبه کن و خروجی مشابه زیر بساز:

```text
----- Receipt -----
Product: Keyboard
Price: $49.99
Quantity: 2
Total: $99.98
```

از قالب‌بندی مناسب برای قیمت استفاده کن.

---

## تمرین ۹ — تبدیل دما

از کاربر دما را بر حسب Celsius دریافت کن.

سپس آن را به Fahrenheit تبدیل کن.

فرمول:

```text
F = C × 9 / 5 + 32
```

خروجی باید چیزی شبیه این باشد:

```text
Celsius: 25.00°C
Fahrenheit: 77.00°F
```

---

## تمرین ۱۰ — پروفایل دانش‌آموز

از کاربر موارد زیر را دریافت کن:

- نام
- سن
- نمره

سپس نمایش بده:

```text
----- Student Profile -----
Name: Alex
Age: 20
Score: 87.50%
```

نمره باید به صورت اعشاری مثل زیر وارد شود:

```text
0.875
```

و به صورت زیر نمایش داده شود:

```text
87.50%
```

---

## تمرین ۱۱ — ساخت جدول ساده

سه دانش‌آموز ایجاد کن:

```python
name1 = "Ali"
score1 = 18

name2 = "Sara"
score2 = 19

name3 = "Reza"
score3 = 17
```

آن‌ها را به شکل یک جدول مرتب نمایش بده:

```text
Name           Score
Ali               18
Sara              19
Reza              17
```

برای تراز کردن ستون‌ها از Alignment Formatting استفاده کن.

---

## تمرین ۱۲ — حساب بانکی

متغیرهای زیر را ایجاد کن:

```python
name = "Ahmad"
balance = 1250000.5
```

خروجی:

```text
----- Bank Account -----
Name: Ahmad
Balance: $1,250,000.50
```

از جداکننده هزارگان و دو رقم اعشار استفاده کن.

---

# چالش نهایی — سیستم گزارش دانش‌آموز

قبل از دیدن پاسخ، خودت مسئله را حل کن.

برنامه‌ای بنویس که اطلاعات زیر را از کاربر دریافت کند:

- نام دانش‌آموز
- سن دانش‌آموز
- نمره ریاضی
- نمره فیزیک
- نمره برنامه‌نویسی

نام باید با استفاده از:

```python
.strip().title()
```

تمیز و قالب‌بندی شود.

نمره‌ها باید اعدادی بین `0` و `20` باشند.

سپس موارد زیر را محاسبه کن:

- میانگین نمرات
- درصد

درصد باید نسبت به حداکثر نمره `20` محاسبه شود.

سپس مشخص کن که دانش‌آموز قبول شده یا مردود.

اگر میانگین حداقل `10` باشد، دانش‌آموز قبول است.

در نهایت گزارشی شبیه این نمایش بده:

```text
----- Student Report -----
Name: Alex
Age: 20
Math: 18.00
Physics: 17.00
Programming: 18.50
Average: 17.83
Percentage: 89.17%
Status: Passed
```

### الزامات

برنامه باید از موارد زیر استفاده کند:

- `input()`
- `int()`
- `float()`
- `.strip()`
- `.title()`
- متغیرها
- عملگرهای ریاضی
- `if / else`
- f-string
- قالب‌بندی عدد با `.2f`
- قالب‌بندی درصد یا محاسبه درصد

سعی کن قبل از دیدن پاسخ، خودت مسئله را حل کنی.

---

# پاسخ چالش نهایی

یک راه‌حل ممکن:

```python
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
print(f"Name: {name}")
print(f"Age: {age}")
print(f"Math: {math:.2f}")
print(f"Physics: {physics:.2f}")
print(f"Programming: {programming:.2f}")
print(f"Average: {average:.2f}")
print(f"Percentage: {percentage:.2f}%")
print(f"Status: {status}")
```

هدف این نیست که دقیقاً همین برنامه را حفظ کنی.

هدف این است که بفهمی قسمت‌های مختلف چگونه با یکدیگر کار می‌کنند:

```text
input
  ↓
تمیز کردن / تبدیل داده
  ↓
ذخیره در متغیرها
  ↓
محاسبه نتایج
  ↓
تصمیم‌گیری
  ↓
قالب‌بندی خروجی
```

این دقیقاً شروع **تفکر الگوریتمی** است:

گرفتن اطلاعات خام، تبدیل مرحله‌به‌مرحله آن‌ها، تصمیم‌گیری و در نهایت تولید یک نتیجه قابل استفاده.

---

# بخش ۸ — رشته‌ها و ورودی کاربر

در بخش‌های قبلی یاد گرفتید که چگونه:

- رشته بسازید
- از علامت‌های نقل‌قول استفاده کنید
- با Indexing به کاراکترها دسترسی پیدا کنید
- با Slicing بخشی از رشته را استخراج کنید
- از متدهای رشته استفاده کنید
- با f-string رشته‌ها را قالب‌بندی کنید

حالا قرار است این مفاهیم را با ورودی گرفتن از کاربر ترکیب کنیم.

وقتی یک برنامه بتواند اطلاعات را از کاربر دریافت کند، آن اطلاعات را پردازش کند و نتیجه مناسبی تولید کند، برنامه بسیار کاربردی‌تر می‌شود.

یک الگوی رایج در برنامه‌های واقعی این است:

    Input
    ↓
    Clean
    ↓
    Process
    ↓
    Format
    ↓
    Output

تمرین‌های این بخش به‌صورت تدریجی سخت‌تر می‌شوند و در تمرین‌های پایانی چند مفهوم را با یکدیگر ترکیب می‌کنیم.

---

## تمرین ۱ — دریافت نام

از کاربر نامش را دریافت کنید.

سپس خروجی زیر را نمایش دهید:

    Hello, Ahmad!

به‌جای `Ahmad` از ورودی کاربر استفاده کنید.

برای خروجی از f-string استفاده کنید.

---

## تمرین ۲ — پاک‌سازی نام

از کاربر نامش را دریافت کنید.

ممکن است کاربر قبل یا بعد از نام خود فاصله وارد کند.

مثلاً:

    "   Ahmad   "

فاصله‌های اضافی را حذف کنید و خروجی زیر را نمایش دهید:

    Hello, Ahmad!

از `.strip()` استفاده کنید.

---

## تمرین ۳ — قالب‌بندی نام

از کاربر نامش را با حروف کوچک دریافت کنید.

مثال:

    Enter your name: ahmad

خروجی:

    Name: Ahmad

از یک متد مناسب رشته استفاده کنید.

---

## تمرین ۴ — تحلیل نام

از کاربر نامش را دریافت کنید.

خروجی زیر را نمایش دهید:

    Name: Ahmad
    Length: 5
    First character: A
    Last character: d

از موارد زیر استفاده کنید:

- `.strip()`
- `.title()`
- `len()`
- Indexing
- f-string

---

## تمرین ۵ — ساخت Username

از کاربر موارد زیر را دریافت کنید:

- نام
- نام خانوادگی

یک Username با ساختار زیر ایجاد کنید:

    first.last

مثال:

    First name: Ahmad
    Last name: Rezaei

    Username: ahmad.rezaei

Username باید با حروف کوچک باشد.

قبل از ساخت Username ورودی‌ها را پاک‌سازی کنید.

---

## تمرین ۶ — ساخت Email

از کاربر موارد زیر را دریافت کنید:

- نام
- نام خانوادگی

یک ایمیل با ساختار زیر ایجاد کنید:

    first.last@example.com

مثال:

    First name: Ahmad
    Last name: Rezaei

    Email: ahmad.rezaei@example.com

قبل از ساخت ایمیل، نام‌ها را پاک‌سازی و قالب‌بندی کنید.

---

## تمرین ۷ — استخراج Username از Email

از کاربر یک آدرس ایمیل دریافت کنید.

مثال:

    Enter email: ahmad@example.com

خروجی:

    Username: ahmad

از متدهای رشته یا Slicing استفاده کنید.

Username را به‌صورت دستی وارد نکنید.

---

## تمرین ۸ — استخراج Domain

از کاربر یک آدرس ایمیل دریافت کنید.

مثال:

    Enter email: ahmad@example.com

خروجی:

    Domain: example.com

به موقعیت `@` و نحوه استفاده از Slicing فکر کنید.

---

## تمرین ۹ — تحلیل Email

از کاربر یک آدرس ایمیل دریافت کنید.

مثال:

    Enter email: ahmad@example.com

خروجی:

    Email: ahmad@example.com
    Username: ahmad
    Domain: example.com
    Length: 17

مفاهیم زیر را ترکیب کنید:

- متدهای رشته
- Indexing یا Slicing
- `len()`
- f-string

---

## تمرین ۱۰ — پاک‌سازی جمله

از کاربر یک جمله دریافت کنید.

برنامه باید:

1. فاصله‌های اضافی را حذف کند.
2. جمله را به حروف کوچک تبدیل کند.
3. جمله پاک‌سازی‌شده را نمایش دهد.

مثال:

    Input:
       PYTHON IS FUN

    Output:
    python is fun

---

## تمرین ۱۱ — اطلاعات جمله

از کاربر یک جمله دریافت کنید.

خروجی زیر را نمایش دهید:

    Sentence: Python is easy.
    Length: 16
    Uppercase: PYTHON IS EASY.
    Lowercase: python is easy.

از متدهای رشته استفاده کنید.

---

## تمرین ۱۲ — جستجو در جمله

از کاربر موارد زیر را دریافت کنید:

- یک جمله
- کلمه‌ای که باید جستجو شود

مثال:

    Sentence: Python is easy to learn.
    Search: easy

خروجی:

    Found: True
    Position: 10

از `.find()` استفاده کنید.

موقعیت را دستی محاسبه نکنید.

---

## تمرین ۱۳ — شمارش یک کاراکتر

از کاربر موارد زیر را دریافت کنید:

- یک جمله
- یک کاراکتر

مثال:

    Sentence: programming
    Character: m

خروجی:

    Character: m
    Count: 2

از `.count()` استفاده کنید.

---

## تمرین ۱۴ — جایگزین کردن یک کلمه

از کاربر موارد زیر را دریافت کنید:

- یک جمله
- کلمه‌ای که باید جایگزین شود
- کلمه جایگزین

مثال:

    Sentence: I like Java
    Word to replace: Java
    Replacement: Python

خروجی:

    Result: I like Python

از `.replace()` استفاده کنید.

---

## تمرین ۱۵ — بررسی Email

از کاربر یک آدرس ایمیل دریافت کنید.

بررسی کنید که آیا:

- شامل `@` است.
- به `.com` ختم می‌شود.

مثال:

    Email: ahmad@example.com

    Contains @: True
    Ends with .com: True

از متدهای مناسب رشته استفاده کنید.

---

## تمرین ۱۶ — بررسی نام فایل

از کاربر نام یک فایل را دریافت کنید.

بررسی کنید که آیا فایل پایتون است یا خیر.

مثال:

    Filename: calculator.py

    Python file: True

از `.endswith()` استفاده کنید.

---

## تمرین ۱۷ — ساخت Initials

از کاربر موارد زیر را دریافت کنید:

- نام
- نام خانوادگی

مثال:

    First name: Ahmad
    Last name: Rezaei

خروجی:

    Full name: Ahmad Rezaei
    Initials: AR

برای ساخت Initials از Indexing استفاده کنید.

---

## تمرین ۱۸ — ساخت یک ID کوتاه

از کاربر موارد زیر را دریافت کنید:

- نام
- نام خانوادگی
- سال تولد

یک ID با ساختار زیر ایجاد کنید:

    سه حرف اول نام
    +
    سه حرف اول نام خانوادگی
    +
    سال تولد

مثال:

    First name: Ahmad
    Last name: Rezaei
    Birth year: 2001

    ID: ahmrez2001

الزامات:

- نام‌ها را به حروف کوچک تبدیل کنید.
- از Slicing استفاده کنید.
- مقادیر را با f-string ترکیب کنید.

---

## تمرین ۱۹ — مخفی کردن رمز عبور

از کاربر یک رمز عبور دریافت کنید.

خود رمز عبور را نمایش ندهید.

به‌جای آن به تعداد کاراکترهای رمز عبور، `*` نمایش دهید.

مثال:

    Enter password: python123

    Password: *********
    Length: 9

از موارد زیر استفاده کنید:

- `len()`
- ضرب رشته

---

## تمرین ۲۰ — تحلیل رمز عبور

از کاربر یک رمز عبور دریافت کنید.

خروجی زیر را نمایش دهید:

    Password length: 10
    Contains @: True
    Starts with P: True
    Ends with 123: False

از متدهای مناسب رشته استفاده کنید.

خود رمز عبور را نمایش ندهید.

---

## تمرین ۲۱ — اطلاعات محصول

از کاربر موارد زیر را دریافت کنید:

- نام محصول
- قیمت
- تعداد

مثال:

    Product: Keyboard
    Price: 49.99
    Quantity: 2

خروجی:

    ----- Product Information -----

    Product: Keyboard
    Price: $49.99
    Quantity: 2
    Total: $99.98

الزامات:

- نام محصول را پاک‌سازی کنید.
- قیمت را به `float` تبدیل کنید.
- تعداد را به `int` تبدیل کنید.
- مجموع قیمت را محاسبه کنید.
- مقادیر پولی را با دو رقم اعشار نمایش دهید.
- از f-string استفاده کنید.

---

## تمرین ۲۲ — پروفایل دانش‌آموز

از کاربر موارد زیر را دریافت کنید:

- نام
- سن
- نمره

مثال:

    Name:   alex
    Age: 20
    Score: 0.875

خروجی:

    ----- Student Profile -----

    Name: Alex
    Age: 20
    Score: 87.50%

الزامات:

- فاصله‌های اضافی را حذف کنید.
- نام را قالب‌بندی کنید.
- سن را به `int` تبدیل کنید.
- نمره را به `float` تبدیل کنید.
- نمره را به‌صورت درصد نمایش دهید.
- از f-string استفاده کنید.

---

## تمرین ۲۳ — ساخت Username و Email

از کاربر موارد زیر را دریافت کنید:

- نام
- نام خانوادگی

هر دو مورد زیر را تولید کنید:

    Username: ahmad.rezaei
    Email: ahmad.rezaei@example.com

الزامات:

- فاصله‌های اضافی را حذف کنید.
- نام‌ها را به حروف کوچک تبدیل کنید.
- از f-string استفاده کنید.

---

## تمرین ۲۴ — پاک‌سازی متن

از کاربر یک جمله دریافت کنید.

برنامه باید:

1. فاصله‌های ابتدا و انتهای جمله را حذف کند.
2. جمله را به حروف کوچک تبدیل کند.
3. `python` را با `Python` جایگزین کند.
4. نتیجه را نمایش دهد.

مثال:

    Input:
       I LOVE PYTHON PROGRAMMING

    Output:
    i love Python programming

به ترتیب انجام عملیات دقت کنید.

---

## تمرین ۲۵ — معکوس کردن کلمه

از کاربر یک کلمه دریافت کنید.

خروجی:

    Original: Python
    Reversed: nohtyP

از Slicing استفاده کنید.

از Loop استفاده نکنید.

---

## تمرین ۲۶ — سه کاراکتر اول و آخر

از کاربر یک کلمه دریافت کنید.

سه کاراکتر اول و سه کاراکتر آخر آن را نمایش دهید.

مثال:

    Word: Programming

    First three: Pro
    Last three: ing

از Slicing استفاده کنید.

---

## تمرین ۲۷ — تحلیل کلمه

از کاربر یک کلمه دریافت کنید.

خروجی:

    Word: Python
    Length: 6
    First character: P
    Last character: n
    First three: Pyt
    Last three: hon
    Reversed: nohtyP
    Uppercase: PYTHON
    Lowercase: python

باید مفاهیم زیر را با یکدیگر ترکیب کنید:

- `len()`
- Indexing
- Slicing
- متدهای رشته
- f-string

---

## تمرین ۲۸ — تحلیل جمله

از کاربر یک جمله دریافت کنید.

خروجی:

    Sentence: Python is easy to learn.
    Length: 25
    Uppercase: PYTHON IS EASY TO LEARN.
    Lowercase: python is easy to learn.
    Starts with Python: True
    Ends with learn.: True

در جاهایی که مناسب است از متدهای رشته استفاده کنید.

---

## تمرین ۲۹ — رسید خرید ساده

از کاربر موارد زیر را دریافت کنید:

- نام محصول
- قیمت
- تعداد

مثال:

    Product: Mouse
    Price: 25.5
    Quantity: 3

خروجی:

    ----- Receipt -----

    Product: Mouse
    Price: $25.50
    Quantity: 3
    Total: $76.50

الزامات:

- نام محصول را پاک‌سازی کنید.
- قیمت را به `float` تبدیل کنید.
- تعداد را به `int` تبدیل کنید.
- مجموع را محاسبه کنید.
- قیمت و مجموع را با دو رقم اعشار نمایش دهید.
- از f-string استفاده کنید.

---

## تمرین ۳۰ — گزارش دانش‌آموز

از کاربر موارد زیر را دریافت کنید:

- نام دانش‌آموز
- سن
- نمره ریاضی
- نمره فیزیک
- نمره برنامه‌نویسی

هر نمره از ۲۰ است.

میانگین و درصد را محاسبه کنید.

مثال:

    ----- Student Report -----

    Name: Alex
    Age: 20

    Math: 18.00
    Physics: 17.50
    Programming: 19.00

    Average: 18.17
    Percentage: 90.83%

الزامات:

- نام دانش‌آموز را پاک‌سازی و قالب‌بندی کنید.
- ورودی‌های عددی را به نوع مناسب تبدیل کنید.
- میانگین را محاسبه کنید.
- میانگین را به درصد تبدیل کنید.
- مقادیر اعشاری را با دو رقم اعشار نمایش دهید.
- از f-string استفاده کنید.

---

# چالش نهایی — ساخت کارت اطلاعات کاربر

قبل از دیدن جواب، ابتدا خودتان برای حل مسئله تلاش کنید.

برنامه‌ای بسازید که یک کارت اطلاعات کاربر را به‌صورت مرتب تولید کند.

برنامه باید موارد زیر را از کاربر دریافت کند:

- نام
- نام خانوادگی
- ایمیل
- سن
- شهر

سپس برنامه باید:

1. فاصله‌های اضافی تمام ورودی‌های متنی را حذف کند.
2. نام و نام خانوادگی را به شکل مناسب قالب‌بندی کند.
3. نام کامل را ایجاد کند.
4. Username را از ایمیل استخراج کند.
5. Domain را از ایمیل استخراج کند.
6. سن را به عدد صحیح تبدیل کند.
7. با استفاده از نام و نام خانوادگی یک Username جدید بسازد.
8. تمام اطلاعات را به‌شکل مرتب نمایش دهد.

مثال ورودی:

    First name:   alex
    Last name: johnson
    Email: alex.johnson@example.com
    Age: 20
    City:   London

خروجی باید شبیه این باشد:

    ----- User Information -----

    Full name: Alex Johnson
    Age: 20
    City: London

    Email: alex.johnson@example.com
    Email username: alex.johnson
    Email domain: example.com

    Generated username: alex.johnson

مفاهیمی که باید با یکدیگر ترکیب کنید:

- `input()`
- متغیرها
- String
- `.strip()`
- `.lower()`
- `.title()`
- Indexing
- Slicing
- `.find()`
- `len()`
- f-string
- `int()`

مسئله را به شکل یک الگوریتم ببینید:

    Input
    ↓
    Clean
    ↓
    Format
    ↓
    Extract
    ↓
    Convert
    ↓
    Generate
    ↓
    Display

هدف فقط این نیست که برنامه کار کند.

هدف این است که یاد بگیرید یک مسئله بزرگ‌تر را به چند مرحله کوچک و منطقی تقسیم کنید.

---

# جواب چالش نهایی

ابتدا خودتان چالش را حل کنید.

یکی از راه‌حل‌های ممکن:

    first_name = input("First name: ").strip().title()
    last_name = input("Last name: ").strip().title()
    email = input("Email: ").strip().lower()
    age = int(input("Age: "))
    city = input("City: ").strip().title()

    full_name = f"{first_name} {last_name}"

    at_position = email.find("@")

    email_username = email[:at_position]
    email_domain = email[at_position + 1:]

    generated_username = f"{first_name.lower()}.{last_name.lower()}"

    print()
    print("----- User Information -----")
    print()
    print(f"Full name: {full_name}")
    print(f"Age: {age}")
    print(f"City: {city}")
    print()
    print(f"Email: {email}")
    print(f"Email username: {email_username}")
    print(f"Email domain: {email_domain}")
    print()
    print(f"Generated username: {generated_username}")

نکته مهم حفظ کردن این جواب نیست.

روی ترتیب عملیات تمرکز کنید:

    Input
    ↓
    Clean
    ↓
    Format
    ↓
    Find
    ↓
    Slice
    ↓
    Convert
    ↓
    Generate
    ↓
    Format output

این نوع تفکر با بزرگ‌تر شدن برنامه‌ها اهمیت بیشتری پیدا می‌کند.

---

# بخش ۹ — عملیات پیشرفته‌ تر روی رشته‌ ها

تا اینجا یاد گرفتیم که چگونه:

- رشته بسازیم
- رشته را داخل متغیر ذخیره کنیم
- با Indexing به کاراکترها دسترسی پیدا کنیم
- با Slicing بخشی از رشته را استخراج کنیم
- با متدهای رشته متن را تغییر دهیم
- با `f-string` متن را قالب‌ بندی کنیم
- از کاربر متن دریافت کنیم
- ورودی کاربر را پاک‌ سازی و پردازش کنیم

در این بخش یک قدم جلوتر می‌ رویم.

هدف این بخش این است که رشته‌ ها را فقط به‌ عنوان متن ساده نبینیم، بلکه بتوانیم آن‌ ها را به‌ عنوان **داده‌ های ساختار یافته** پردازش کنیم.

برای مثال:

    alex.johnson@example.com

در ظاهر فقط یک رشته است، اما درون آن چند بخش مختلف وجود دارد:

    username → alex.johnson
    domain   → example.com

یا:

    Python,Java,C++,JavaScript

این رشته در واقع شامل چهار مقدار جداگانه است.

برای کار با چنین داده‌ هایی باید یاد بگیریم چگونه رشته‌ ها را جدا کنیم، پاک‌ سازی کنیم، بررسی کنیم، دوباره به هم وصل کنیم و مرحله‌ به‌ مرحله پردازش کنیم.

---

## ۱. جدا کردن رشته با `split()`

یکی از مهم‌ ترین عملیات روی رشته‌ ها، متد `split()` است.

این متد یک رشته را به چند بخش تقسیم می‌ کند.

مثلاً:

    text = "Python is easy"

    words = text.split()

به‌ صورت مفهومی نتیجه شامل این بخش‌ ها خواهد بود:

    Python
    is
    easy

اگر جدا کننده مشخص نکنیم، `split()` معمولاً بر اساس فاصله‌ های خالی رشته را تقسیم می‌ کند.

می‌ توانیم جدا کننده را نیز مشخص کنیم.

مثلاً:

    fruits = "apple,banana,orange"

    result = fruits.split(",")

نتیجه:

    apple
    banana
    orange

پس یک مفهوم مهم داریم:

    یک رشته
        ↓
      split()
        ↓
    چند بخش

---

## ۲. استفاده از `split()` برای ورودی کاربر

فرض کنید کاربر چند نام را با کاما وارد می‌ کند:

    Ahmad, Sara, Alex

می‌ توانیم ورودی را پردازش کنیم:

    names = input("Enter names: ").split(",")

اما ممکن است بعضی از مقادیر دارای فاصله‌ های اضافی باشند:

    "Ahmad"
    " Sara"
    " Alex"

بنابراین بهتر است آن‌ ها را پاک‌ سازی کنیم.

مثلاً:

    names = input("Enter names: ").split(",")

    first_name = names[0].strip()
    second_name = names[1].strip()
    third_name = names[2].strip()

این الگو بسیار مهم است:

    دریافت داده
        ↓
    جدا کردن داده
        ↓
    پاک‌ سازی داده
        ↓
    پردازش داده

---

## ۳. جدا کردن با یک جدا کننده مشخص

محدود به کاما نیستیم.

مثلاً:

    date = "2026-08-05"

    parts = date.split("-")

نتیجه:

    2026
    08
    05

این روش به برنامه اجازه می‌ دهد اطلاعات ساختار یافته را از یک رشته ساده استخراج کند.

---

## ۴. اتصال رشته‌ ها با `join()`

عملیات بسیار مهم دیگری `join()` است.

فرض کنید:

    words = ["Python", "is", "powerful"]

می‌ توانیم آن‌ ها را به یک رشته تبدیل کنیم:

    sentence = " ".join(words)

نتیجه:

    Python is powerful

رشته‌ ای که قبل از `join()` قرار می‌ دهیم مشخص می‌ کند چه چیزی بین عناصر قرار بگیرد.

مثلاً:

    "-".join(["2026", "08", "05"])

نتیجه:

    2026-08-05

و:

    ", ".join(["Python", "Java", "C++"])

نتیجه:

    Python, Java, C++

بنابراین:

    split()
    رشته → چند بخش

    join()
    چند بخش → رشته

---

## ۵. استفاده از `split()` و `join()` در کنار یکدیگر

یکی از تکنیک‌ های قدرتمند این است که رشته را جدا کنیم، بخش‌ های آن را تغییر دهیم و دوباره آن‌ ها را به هم متصل کنیم.

مثلاً:

    text = "python programming language"

    words = text.split()

    words = [word.title() for word in words]

    result = " ".join(words)

نتیجه:

    Python Programming Language

روند کلی این عملیات:

    رشته اولیه
        ↓
      split()
        ↓
    کلمات جداگانه
        ↓
      پردازش
        ↓
      join()
        ↓
    رشته جدید

این الگو در برنامه‌ های واقعی بسیار کاربرد دارد.

---

## ۶. بررسی وجود یک متن در رشته

می‌ توانیم با `in` بررسی کنیم که آیا یک رشته کوچک‌ تر داخل رشته دیگری وجود دارد یا خیر.

مثلاً:

    text = "Python is powerful"

    print("Python" in text)

نتیجه:

    True

اما:

    print("Java" in text)

نتیجه:

    False

این قابلیت برای جستجو در متن بسیار مفید است.

---

## ۷. استفاده از `not in`

عملگر مخالف `in` عبارت `not in` است.

مثلاً:

    text = "Python is powerful"

    print("Java" not in text)

نتیجه:

    True

این روش می‌ تواند بعضی شرط‌ ها را خواناتر کند.

---

## ۸. بررسی وجود یک کاراکتر

عملگر `in` برای کاراکترها نیز کار می‌ کند.

مثلاً:

    text = "Python"

    print("P" in text)

نتیجه:

    True

و:

    print("z" in text)

نتیجه:

    False

این قابلیت می‌ تواند در اعتبار سنجی ورودی کاربر استفاده شود.

---

## ۹. بررسی اعداد با `isdigit()`

متد `isdigit()` بررسی می‌ کند که آیا تمام کاراکترهای رشته رقم هستند یا خیر.

مثلاً:

    text = "12345"

    print(text.isdigit())

نتیجه:

    True

اما:

    text = "123abc"

    print(text.isdigit())

نتیجه:

    False

این متد زمانی کاربرد دارد که برنامه انتظار داشته باشد ورودی فقط شامل ارقام باشد.

---

## ۱۰. بررسی حروف با `isalpha()`

متد `isalpha()` بررسی می‌ کند که آیا تمام کاراکترهای رشته حروف هستند یا خیر.

مثلاً:

    text = "Python"

    print(text.isalpha())

نتیجه:

    True

اما:

    text = "Python3"

    print(text.isalpha())

نتیجه:

    False

وجود فاصله نیز باعث می‌ شود نتیجه `False` باشد.

مثلاً:

    text = "Python Programming"

    print(text.isalpha())

نتیجه:

    False

---

## ۱۱. بررسی حروف و اعداد با `isalnum()`

متد `isalnum()` بررسی می‌ کند که آیا تمام کاراکترهای رشته حروف یا اعداد هستند یا خیر.

مثلاً:

    print("Python123".isalnum())

نتیجه:

    True

اما:

    print("Python 123".isalnum())

نتیجه:

    False

زیرا فاصله یک کاراکتر alphanumeric نیست.

---

## ۱۲. بررسی فاصله‌ های خالی با `isspace()`

متد `isspace()` بررسی می‌ کند که آیا رشته فقط شامل کاراکترهای فضای خالی است یا خیر.

مثلاً:

    text = "   "

    print(text.isspace())

نتیجه:

    True

اما:

    text = " Python "

    print(text.isspace())

نتیجه:

    False

این متد در اعتبار سنجی ورودی‌ های ظاهراً خالی می‌ تواند مفید باشد.

---

## ۱۳. رشته خالی

یک رشته خالی هیچ کاراکتری ندارد.

می‌ توانیم آن را این‌ گونه ایجاد کنیم:

    text = ""

طول آن:

    len(text)

برابر است با:

    0

اما رشته خالی با رشته‌ ای که فقط شامل فاصله است تفاوت دارد.

مثلاً:

    text1 = ""

    text2 = "   "

رشته اول طول `0` دارد.

رشته دوم طول `3` دارد.

این تفاوت هنگام اعتبار سنجی ورودی بسیار مهم است.

---

## ۱۴. بررسی ورودی خالی کاربر

فرض کنید از کاربر نامش را دریافت می‌ کنیم:

    name = input("Enter your name: ").strip()

اگر کاربر فقط Enter را فشار دهد، مقدار `name` برابر با رشته خالی خواهد بود.

می‌ توانیم بررسی کنیم:

    if name == "":
        print("Name cannot be empty.")

این کار بهتر از آن است که مقدار خالی بدون بررسی وارد مراحل بعدی برنامه شود.

---

## ۱۵. روش کوتاه‌ تر برای بررسی رشته خالی

پایتون اجازه می‌ دهد این کار را به شکل کوتاه‌ تری بنویسیم:

    if not name:
        print("Name cannot be empty.")

برای یک رشته خالی، پایتون مقدار را در شرط `False` در نظر می‌ گیرد.

به این مفهوم **Truthiness** گفته می‌ شود.

فعلاً قانون مهم این است:

    "" → False

در مقابل، یک رشته غیر خالی در شرط مانند `True` رفتار می‌ کند.

مثلاً:

    name = "Ahmad"

    if name:
        print("Name was entered.")

---

## ۱۶. شمارش کلمات

فرض کنید جمله زیر را داریم:

    Python is easy to learn

می‌ توانیم تعداد کلمات را محاسبه کنیم:

    sentence = "Python is easy to learn"

    words = sentence.split()

    count = len(words)

نتیجه:

    5

در این مثال چند مفهوم با هم ترکیب شده‌ اند:

    String
        ↓
    split()
        ↓
    چند کلمه
        ↓
    len()
        ↓
    تعداد کلمات

---

## ۱۷. شمارش کلمات از ورودی کاربر

از کاربر یک جمله دریافت کنید و تعداد کلمات آن را محاسبه کنید:

    sentence = input("Enter a sentence: ").strip()

    words = sentence.split()

    word_count = len(words)

    print(f"Word count: {word_count}")

اگر کاربر وارد کند:

    Python is easy to learn

خروجی:

    Word count: 5

نکته مهم این است که `split()` در برخورد با چند فاصله متوالی بسیار بهتر از شمارش دستی فاصله‌ ها عمل می‌ کند.

---

## ۱۸. ساخت یک جمله تمیز

فرض کنید کاربر این متن را وارد کند:

    Python    is     very     powerful

فاصله‌ های زیادی بین کلمات وجود دارد.

با:

    words = text.split()

فاصله‌ های اضافی حذف می‌ شوند.

سپس:

    clean_text = " ".join(words)

نتیجه:

    Python is very powerful

روند تبدیل:

    "Python    is     very     powerful"
                    ↓
                split()
                    ↓
        ["Python", "is", "very", "powerful"]
                    ↓
                join()
                    ↓
        "Python is very powerful"

این یک تکنیک مهم برای پاک‌ سازی متن است.

---

## ۱۹. استخراج بخش‌ های یک نام

فرض کنید:

    full_name = "Alex Johnson"

می‌ توانیم آن را تقسیم کنیم:

    parts = full_name.split()

سپس:

    first_name = parts[0]
    last_name = parts[1]

اکنون می‌ توانیم هر قسمت را جداگانه استفاده کنیم:

    print(f"First name: {first_name}")
    print(f"Last name: {last_name}")

خروجی:

    First name: Alex
    Last name: Johnson

اما یک محدودیت مهم وجود دارد.

اگر ورودی این باشد:

    Alex Michael Johnson

اکنون سه بخش داریم.

بنابراین در برنامه‌ های واقعی نباید بدون فکر کردن درباره ساختار داده، فرض کنیم که همیشه فقط دو بخش وجود دارد.

---

## ۲۰. جدا کردن فقط یک بار

گاهی نمی‌ خواهیم رشته در تمام جدا کننده‌ های موجود تقسیم شود.

مثلاً:

    text = "name@example.com"

می‌ توانیم فقط در اولین `@` آن را جدا کنیم:

    username, domain = text.split("@", 1)

عدد `1` مشخص می‌ کند که عملیات تقسیم حداکثر یک بار انجام شود.

نتیجه:

    username → name
    domain   → example.com

این قابلیت هنگام پردازش داده‌ های ساختار یافته بسیار مفید است.

---

## ۲۱. پاک‌ سازی فهرستی از نام‌ ها

فرض کنید کاربر وارد کند:

    Ahmad, Sara, Alex

می‌ توانیم نام‌ ها را پاک‌ سازی کنیم:

    names = input("Enter names: ").split(",")

    clean_names = [name.strip().title() for name in names]

روند کار:

    Split
        ↓
    انتخاب هر نام
        ↓
    حذف فاصله‌ ها
        ↓
    قالب‌ بندی نام
        ↓
    ذخیره نتیجه

اگر `List Comprehension` هنوز برایتان جدید است، مشکلی نیست.

همین الگوریتم را می‌ توان به شکل واضح‌ تر نیز نوشت.

---

## ۲۲. نسخه واضح‌ تر با Loop

مثال قبل را می‌ توان با یک `for` معمولی نوشت:

    names = input("Enter names: ").split(",")

    clean_names = []

    for name in names:
        clean_name = name.strip().title()
        clean_names.append(clean_name)

این نسخه طولانی‌ تر است، اما الگوریتم را واضح‌ تر نشان می‌ دهد.

در یادگیری برنامه‌ نویسی، درک روند اجرای برنامه مهم‌ تر از کوتاه کردن کد است.

---

## ۲۳. اتصال دوباره نام‌ های پاک‌ شده

بعد از پاک‌ سازی نام‌ ها می‌ توانیم آن‌ ها را دوباره به یک رشته تبدیل کنیم:

    names = ["Ahmad", "Sara", "Alex"]

    result = ", ".join(names)

نتیجه:

    Ahmad, Sara, Alex

در اینجا یک چرخه کامل داریم:

    ورودی کاربر
        ↓
    Split
        ↓
    Clean
        ↓
    Format
        ↓
    Join
        ↓
    متن نهایی

---

## ۲۴. ساخت برنامه جستجوی متن

از کاربر یک جمله و یک کلمه دریافت کنید:

    sentence = input("Enter a sentence: ")
    search_word = input("Search for: ")

    if search_word in sentence:
        print("Word found.")
    else:
        print("Word not found.")

این یک نمونه ساده از برنامه‌ ای است که بر اساس محتوای متن تصمیم می‌ گیرد.

---

## ۲۵. جستجوی بدون توجه به حروف بزرگ و کوچک

مثال قبلی یک مشکل دارد.

فرض کنید جمله:

    Python is powerful

باشد و کاربر جستجو کند:

    python

در این حالت ممکن است جستجو موفق نشود، چون:

    Python

و:

    python

دو رشته متفاوت هستند.

یک راه‌ حل رایج این است که هر دو مقدار را به یک شکل تبدیل کنیم:

    sentence = input("Enter a sentence: ").lower()
    search_word = input("Search for: ").lower()

    if search_word in sentence:
        print("Word found.")
    else:
        print("Word not found.")

اکنون تفاوت حروف بزرگ و کوچک روی این جستجوی ساده تأثیری ندارد.

---

## ۲۶. ساخت Text Normalizer

یک Text Normalizer ورودی کاربر را برای پردازش یکدست آماده می‌ کند.

مثلاً:

    text = input("Enter text: ")

    text = text.strip()
    text = text.lower()

حالا ورودی‌ های مختلف:

    " PYTHON "
    "Python"
    "PYTHON"

می‌ توانند همگی به:

    "python"

تبدیل شوند.

این کار قبل از عملیات زیر بسیار مفید است:

- جستجو
- مقایسه
- اعتبار سنجی
- ذخیره اطلاعات

---

## ۲۷. نکته مهم: قبل از مقایسه Normalize کنید

فرض کنید می‌ خواهیم دو نام را مقایسه کنیم.

کاربر وارد کرده است:

    first_name = " Ahmad "
    second_name = "ahmad"

اگر مستقیماً مقایسه کنیم:

    first_name == second_name

نتیجه:

    False

اما اگر ابتدا آن‌ ها را Normalize کنیم:

    first_name = first_name.strip().lower()
    second_name = second_name.strip().lower()

حالا:

    first_name == second_name

نتیجه:

    True

این مثال یک اصل مهم برنامه‌ نویسی را نشان می‌ دهد:

**قبل از مقایسه متن وارد شده توسط کاربر، بهتر است آن متن را به یک فرم یکسان تبدیل کنیم.**

---

## ۲۸. اشتباه رایج — فراموش کردن `strip()`

به این کد توجه کنید:

    name = input("Name: ")

ممکن است کاربر بنویسد:

    Ahmad

اما ممکن است این مقدار را وارد کند:

    "   Ahmad   "

اگر ورودی را بدون پاک‌ سازی ذخیره کنیم، فاصله‌ ها بخشی از رشته باقی می‌ مانند.

بهتر است در صورت نیاز از همان ابتدا بنویسیم:

    name = input("Name: ").strip()

پاک‌ سازی داده در ابتدای مسیر معمولاً باعث می‌ شود مراحل بعدی ساده‌ تر شوند.

---

## ۲۹. اشتباه رایج — فرض کردن ساختار ورودی

فرض کنید برنامه انتظار دارد ورودی این شکل باشد:

    first_name,last_name

و کاربر وارد کند:

    Ahmad,Rezaei

در این حالت:

    parts = text.split(",")

به‌ درستی کار می‌ کند.

اما اگر کاربر فقط بنویسد:

    Ahmad

مقدار دوم وجود ندارد.

بنابراین نباید بدون بررسی فرض کنیم ورودی کاربر همیشه معتبر است.

این موضوع ما را به یک مفهوم مهم‌ تر می‌ رساند:

**قبل از پردازش ورودی، باید ساختار و اعتبار آن را بررسی کنیم.**

اعتبار سنجی و مدیریت خطا را در بخش‌ های آینده عمیق‌ تر بررسی خواهیم کرد.

---

# تمرین ۱ — شمارنده کلمات

برنامه‌ ای بنویسید که از کاربر یک جمله دریافت کند.

برنامه باید خروجی مشابه این داشته باشد:

    ----- Text Analysis -----

    Sentence: Python is easy to learn.
    Word count: 5

الزامات:

- فاصله‌ های اضافی را حذف کنید.
- جمله را به کلمات تقسیم کنید.
- تعداد کلمات را محاسبه کنید.
- از `f-string` استفاده کنید.

---

# تمرین ۲ — پاک‌ سازی فهرست نام‌ ها

از کاربر چند نام را که با کاما جدا شده‌ اند دریافت کنید.

مثال:

    Enter names:   ahmad, sara , ALEX, john

برنامه باید:

    ----- Names -----

    Ahmad
    Sara
    Alex
    John

را نمایش دهد.

الزامات:

- ورودی را با `,` جدا کنید.
- فاصله‌ های اضافی را حذف کنید.
- نام‌ ها را قالب‌ بندی کنید.
- نتیجه را نمایش دهید.

---

# تمرین ۳ — تحلیل Email

از کاربر یک آدرس ایمیل دریافت کنید.

برنامه باید نمایش دهد:

    ----- Email Analysis -----

    Email: ahmad@example.com
    Username: ahmad
    Domain: example.com

الزامات:

- ورودی را پاک‌ سازی کنید.
- آن را به حروف کوچک تبدیل کنید.
- Username و Domain را جدا کنید.
- نتیجه را با استفاده از عملیات روی رشته تولید کنید.

---

# تمرین ۴ — Text Normalizer

از کاربر یک جمله دریافت کنید.

جمله ممکن است شامل موارد زیر باشد:

- فاصله‌ های اضافی
- حروف بزرگ
- حروف کوچک

آن را به یک جمله تمیز تبدیل کنید که:

- بین کلمات فقط یک فاصله داشته باشد.
- تمام حروف آن کوچک باشند.

مثال:

    Input:
       PYTHON     IS       VERY     POWERFUL

    Output:
    python is very powerful

به این فکر کنید که چرا ترکیب `split()` و `join()` برای این کار مناسب است.

---

# تمرین ۵ — موتور جستجوی ساده

از کاربر موارد زیر را دریافت کنید:

- یک جمله
- یک کلمه برای جستجو

جستجو باید نسبت به حروف بزرگ و کوچک حساس نباشد.

مثال:

    Sentence: Python is a powerful programming language.
    Search: PYTHON

خروجی:

    Result: Found

اگر کلمه وجود نداشت:

    Result: Not found

---

# چالش نهایی — پردازش فهرست مخاطبین

قبل از دیدن جواب، ابتدا خودتان برای حل مسئله تلاش کنید.

برنامه‌ ای بسازید که چند مخاطب را از کاربر دریافت کند.

کاربر مخاطبین را با ساختار زیر وارد می‌ کند:

    Ahmad Rezaei:ahmad@example.com,Sara Smith:sara@example.com,Alex Johnson:alex@example.com

برنامه باید خروجی مشابه زیر تولید کند:

    ----- Contact List -----

    1. Ahmad Rezaei
       Email: ahmad@example.com

    2. Sara Smith
       Email: sara@example.com

    3. Alex Johnson
       Email: alex@example.com

برنامه باید:

1. رشته کامل را از کاربر دریافت کند.
2. مخاطبین را با `,` از یکدیگر جدا کند.
3. هر مخاطب را جداگانه پردازش کند.
4. نام و ایمیل را با `:` از یکدیگر جدا کند.
5. فاصله‌ های اضافی را حذف کند.
6. نام را قالب‌ بندی کند.
7. ایمیل را به حروف کوچک تبدیل کند.
8. مخاطبین را به‌ صورت خوانا نمایش دهد.

مسئله را به‌ صورت یک زنجیره از تبدیل‌ ها ببینید:

    ورودی خام
        ↓
    جدا کردن مخاطبین
        ↓
    پردازش یک مخاطب
        ↓
    جدا کردن نام و ایمیل
        ↓
    پاک‌ سازی مقادیر
        ↓
    قالب‌ بندی مقادیر
        ↓
    نمایش نتیجه

هدف اصلی این چالش فقط یادگیری Syntax نیست.

هدف این است که یاد بگیرید چگونه یک رشته بزرگ که شامل اطلاعات ساختار یافته است را مرحله‌ به‌ مرحله به داده‌ ای قابل استفاده تبدیل کنید.

---

# جواب چالش نهایی

ابتدا خودتان چالش را حل کنید.

یکی از راه‌ حل‌ های ممکن:

    contacts_text = input("Enter contacts: ").strip()

    contacts = contacts_text.split(",")

    print()
    print("----- Contact List -----")
    print()

    number = 1

    for contact in contacts:
        name, email = contact.split(":", 1)

        name = name.strip().title()
        email = email.strip().lower()

        print(f"{number}. {name}")
        print(f"   Email: {email}")
        print()

        number += 1

این راه‌ حل از همان الگوریتمی پیروی می‌ کند که در طول بخش یاد گرفتیم:

    Input
        ↓
    Split contacts
        ↓
    Loop through contacts
        ↓
    Split each contact
        ↓
    Clean values
        ↓
    Format values
        ↓
    Display

نکته اصلی این بخش این است که رشته‌ ها می‌ توانند شامل اطلاعات ساختار یافته باشند.

وقتی یاد بگیرید چگونه رشته‌ ها را Split، Clean، Search، Normalize و Join کنید، می‌ توانید متن خام را به داده‌ ای تبدیل کنید که برنامه واقعاً بتواند روی آن کار کند.

---

