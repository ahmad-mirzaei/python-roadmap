# برنامه نویسی شی گرا   

🌐 زبان: **فارسی** | [English](../README.md)

## فهرست مطالب

| پارت | موضوع |
|---|---|
| ۱ | مقدمه ای بر Object-Oriented Programming |
| ۲ | Classها |
| ۳ | Objectها |
| ۴ | متد `__init__()` |
| ۵ | Instance Attributeها |
| ۶ | Instance Methodها |
| ۷ | پارامتر `self` |
| ۸ | Class Attributeها |
| ۹ | Class Methodها |
| ۱۰ | Static Methodها |
| ۱۱ | تعامل بین Objectها |
| ۱۲ | Inheritance |
| ۱۳ | Method Overriding |
| ۱۴ | `super()` |
| ۱۵ | Encapsulation |
| ۱۶ | Propertyها |
| ۱۷ | `__str__()` و `__repr__()` |
| ۱۸ | Special Methodها |
| ۱۹ | اشتباهات رایج و Best Practiceها |
| ۲۰ | مرور نهایی: OOP |
| ۲۱ | پروژه کوچک OOP |

---

# پارت ۱: مقدمه ای بر شی گرایی

## ۱. برنامه نویسی شی گرا چیست؟

**Object-Oriented Programming** یا به اختصار **OOP**، یک سبک برنامه نویسی است که در آن کد را حول **Objectها** سازمان دهی می کنیم.

یک Object می تواند چیزی مانند موارد زیر را نمایش دهد:

- یک کاربر
- یک محصول
- یک حساب بانکی
- یک دانش آموز
- یک خودرو
- یک کتاب
- یک شخصیت بازی

هر Object می تواند شامل دو بخش مهم باشد:

- **Data** — اطلاعات مربوط به Object
- **Behavior** — کارهایی که Object می تواند انجام دهد

برای مثال، یک Object مربوط به خودرو می تواند اطلاعات زیر را داشته باشد:

```python
brand = "Toyota"
color = "Red"
speed = 80
```

و می تواند کارهایی مانند موارد زیر انجام دهد:

```python
start()
stop()
accelerate()
brake()
```

بنابراین می توانیم یک Object را ترکیبی از **Data و Behavior** در نظر بگیریم.

---

## ۲. چرا به OOP نیاز داریم؟

هرچه برنامه ها بزرگ تر می شوند، مدیریت همه چیز با Variableها و Functionهای ساده می تواند سخت تر شود.

فرض کنید برنامه ای برای مدیریت دانش آموزان داریم.

بدون OOP ممکن است چنین چیزی بنویسیم:

```python
student1_name = "Ali"
student1_age = 20
student1_grade = 18.5

student2_name = "Sara"
student2_age = 21
student2_grade = 19.0
```

هرچه تعداد دانش آموزان بیشتر شود، سازمان دهی این کد سخت تر می شود.

ممکن است Function جداگانه ای هم برای نمایش اطلاعات بنویسیم:

```python
def print_student(name, age, grade):
    print(name)
    print(age)
    print(grade)
```

این روش کار می کند، اما اطلاعات مربوط به هر دانش آموز در Variableهای جداگانه پخش شده است.

با OOP می توانیم هر دانش آموز را به صورت یک Object نمایش دهیم.

از نظر مفهومی:

```text
Student
│
├── name
├── age
├── grade
│
├── study()
└── introduce()
```

در این حالت اطلاعات و رفتارهای مربوط به یک دانش آموز می توانند در کنار یکدیگر قرار بگیرند.

---

## ۳. Objectها به عنوان مدل دنیای واقعی

یکی از بهترین روش ها برای درک OOP این است که به Objectهای دنیای واقعی فکر کنیم.

فرض کنید می خواهیم یک برنامه برای یک کتابخانه بسازیم.

یک کتابخانه می تواند تعداد زیادی کتاب داشته باشد.

هر کتاب می تواند اطلاعاتی مانند موارد زیر داشته باشد:

```text
Book
├── title
├── author
├── year
└── price
```

یک کتاب همچنین می تواند رفتارهایی مانند موارد زیر داشته باشد:

```text
borrow()
return_book()
display_info()
```

به جای اینکه Variableها و Functionهای نامرتبط زیادی ایجاد کنیم، می توانیم ساختاری ایجاد کنیم که مفهوم «کتاب» را در برنامه نمایش دهد.

به این کار **Modeling** یا مدل سازی گفته می شود.

ما در واقع یک مفهوم دنیای واقعی را داخل برنامه خود مدل می کنیم.

---

## ۴. تفاوت Class و Object

دو مفهوم بسیار مهم در OOP عبارتند از:

- **Class**
- **Object**

این دو مفهوم به یکدیگر مرتبط هستند، اما یکسان نیستند.

یک **Class** مانند یک Blueprint یا الگو است.

یک **Object** یک Instance واقعی ساخته شده از آن Class است.

برای درک بهتر، یک خانه را تصور کنید.

نقشه معماری خانه شبیه Class است:

```text
House Blueprint
├── number of rooms
├── color
├── doors
└── windows
```

یک خانه واقعی شبیه Object است:

```text
House #1
├── 3 rooms
├── white
├── 2 doors
└── 6 windows
```

یک خانه دیگر نیز می تواند از همان Blueprint ساخته شود:

```text
House #2
├── 4 rooms
├── blue
├── 3 doors
└── 8 windows
```

هر دو خانه از یک ساختار کلی استفاده می کنند، اما اطلاعات آنها می تواند متفاوت باشد.

در Python:

```text
Class
  ↓
Blueprint

Object
  ↓
Actual Instance
```

در Partهای بعدی یاد می گیریم که چگونه Classها و Objectها را در Python ایجاد کنیم.

---

## ۵. Data و Behavior

Objectها معمولاً شامل دو دسته مهم از اطلاعات هستند.

### Data

Data اطلاعاتی است که Object را توصیف می کند.

برای مثال، یک `Student` می تواند این موارد را داشته باشد:

```text
name
age
grade
```

یک `Car` می تواند داشته باشد:

```text
brand
model
color
speed
```

یک `BankAccount` می تواند داشته باشد:

```text
owner
balance
account_number
```

### Behavior

Behavior کارهایی است که Object می تواند انجام دهد.

یک `Student` می تواند:

```text
study()
take_exam()
introduce()
```

یک `Car` می تواند:

```text
start()
accelerate()
brake()
stop()
```

یک `BankAccount` می تواند:

```text
deposit()
withdraw()
check_balance()
```

در Python، Behavior معمولاً با استفاده از **Method**ها نمایش داده می شود.

Method در واقع Functionای است که به یک Class یا Object مربوط است.

در Partهای بعدی Methodها را با جزئیات بیشتری بررسی می کنیم.

---

## ۶. مدل ذهنی ساده برای OOP

یک مدل ذهنی مفید برای OOP این است:

```text
Class
  │
  ├── Data
  │
  └── Behavior
        │
        ↓
     Objects
```

برای مثال:

```text
Class: Student

Data:
    name
    age
    grade

Behavior:
    study()
    introduce()
    take_exam()
```

از این Class می توانیم چند Object مختلف ایجاد کنیم:

```text
student1 → Ali
student2 → Sara
student3 → Reza
```

هر سه Object از یک ساختار کلی استفاده می کنند، اما Data آنها می تواند متفاوت باشد.

---

## ۷. OOP به این معنی نیست که همه چیز باید Object باشد

یک اشتباه رایج در شروع OOP این است که فکر کنیم:

> «چون Python از OOP پشتیبانی می کند، پس باید برای همه چیز Class بسازم.»

این تصور درست نیست.

Python از چند سبک مختلف برنامه نویسی پشتیبانی می کند.

برای مثال، یک محاسبه ساده الزاماً به Class نیاز ندارد:

```python
def calculate_total(price, quantity):
    return price * quantity
```

ساختن یک Class فقط برای این Function می تواند باعث پیچیده شدن غیرضروری برنامه شود.

OOP زمانی مفیدتر است که:

- برنامه چند Entity مرتبط داشته باشد
- هر Entity اطلاعات مخصوص خودش را داشته باشد
- هر Entity رفتار مخصوص خودش را داشته باشد
- Objectها با یکدیگر تعامل داشته باشند
- برنامه در حال بزرگ و پیچیده شدن باشد
- به ساختارهای قابل استفاده مجدد نیاز داشته باشیم

هدف این نیست که همه جا از Class استفاده کنیم.

هدف این است که هرجا Class باعث واضح تر و قابل نگه داری تر شدن کد می شود، از آن استفاده کنیم.

---

## ۸. OOP و سازمان دهی کد

یکی از مهم ترین مزیت های OOP، سازمان دهی بهتر کد است.

فرض کنید یک بازی داریم.

بدون OOP ممکن است چنین Variableها و Functionهایی داشته باشیم:

```text
player_name
player_health
player_score

enemy_name
enemy_health
enemy_damage

move_player()
attack_enemy()
take_damage()
```

هرچه بازی بزرگ تر شود، تعداد Variableها و Functionها می تواند خیلی زیاد شود.

با OOP می توانیم مفاهیم مختلف را جداگانه مدل کنیم:

```text
Player
├── name
├── health
├── score
├── move()
└── attack()

Enemy
├── name
├── health
├── damage
└── attack()
```

این ساختار باعث می شود معماری برنامه راحت تر قابل درک باشد.

---

## ۹. قابلیت استفاده مجدد

یکی دیگر از مزیت های مهم OOP، **Reusability** یا قابلیت استفاده مجدد است.

فرض کنید یک بار Class مربوط به `Student` را ایجاد کرده ایم.

حالا می توانیم Objectهای زیادی از آن بسازیم:

```text
Student class
     │
     ├── student1
     ├── student2
     ├── student3
     └── student4
```

لازم نیست ساختار کامل را برای هر دانش آموز دوباره بنویسیم.

همین ایده برای موارد زیر هم کاربرد دارد:

- Userها
- Productها
- Employeeها
- Customerها
- Vehicleها
- Bookها
- Game Characterها

این یکی از دلایل اصلی مفید بودن Classها در برنامه های بزرگ تر است.

---

## ۱۰. OOP و Encapsulation

OOP همچنین ابزارهایی برای کنار هم نگه داشتن Data و Behavior مرتبط با یک مفهوم در اختیار ما قرار می دهد.

برای مثال، یک حساب بانکی دارای موجودی است.

به جای اینکه فقط داشته باشیم:

```python
balance = 1000
```

و تعداد زیادی Function نامرتبط برای تغییر این Variable ایجاد کنیم، می توانیم در نهایت ساختاری مانند زیر داشته باشیم:

```text
BankAccount
├── balance
├── deposit()
└── withdraw()
```

در این حالت عملیات مربوط به حساب بانکی در کنار خود حساب قرار می گیرد.

این ایده به یکی از مفاهیم مهم OOP به نام **Encapsulation** منجر می شود.

Encapsulation را در Partهای بعدی بررسی خواهیم کرد.

---

## ۱۱. OOP و Abstraction

یکی دیگر از مفاهیم مهم OOP، **Abstraction** است.

Abstraction یعنی بتوانیم با یک مفهوم کار کنیم، بدون اینکه مجبور باشیم تمام جزئیات داخلی پیاده سازی آن را بدانیم.

برای مثال، وقتی می نویسیم:

```python
numbers.append(10)
```

لازم نیست بدانیم Python دقیقاً چگونه حافظه مربوط به List را مدیریت می کند.

ما فقط از عملیاتی که نیاز داریم استفاده می کنیم.

در سیستم های بزرگ تر OOP، Classها می توانند یک Interface ساده در اختیار ما قرار دهند و جزئیات غیرضروری پیاده سازی را پنهان کنند.

در ادامه این مفهوم را عمیق تر بررسی خواهیم کرد.

---

## ۱۲. OOP و Inheritance

OOP همچنین این امکان را می دهد که یک Class را بر اساس Class دیگری بسازیم.

برای مثال:

```text
Animal
  │
  ├── Dog
  └── Cat
```

یک `Dog` می تواند ویژگی های مشترک خود را از `Animal` دریافت کند.

از نظر مفهومی:

```text
Animal
├── name
├── eat()
└── sleep()

Dog
├── bark()
└── inherited eat()
└── inherited sleep()
```

به این مفهوم **Inheritance** یا وراثت گفته می شود.

Inheritance می تواند باعث جلوگیری از تکرار کدهای مشترک شود.

البته باید با دقت از آن استفاده کنیم؛ چون Inheritance همیشه بهترین راه حل برای هر رابطه ای نیست.

در Partهای بعدی آن را به صورت کامل بررسی می کنیم.

---

## ۱۳. OOP و Polymorphism

یکی دیگر از مفاهیم مهم OOP، **Polymorphism** است.

این واژه به معنی «چند شکل» است.

در برنامه نویسی، Polymorphism به ما اجازه می دهد Objectهای مختلف به یک عملیات یکسان، به شکل های متفاوت پاسخ دهند.

برای مثال:

```text
Animal
   │
   ├── Dog → speak() → "Woof"
   └── Cat → speak() → "Meow"
```

هر دو Object دارای Behaviorای به نام `speak()` هستند، اما پیاده سازی آنها متفاوت است.

این قابلیت باعث می شود کد بتواند با Typeهای مختلف Objectها از طریق یک Interface مشترک کار کند.

این مفهوم را بعد از یادگیری Classها و Objectها بررسی خواهیم کرد.

---

## ۱۴. یک پیش نمایش ساده

هنوز قرار نیست یک Class کامل ایجاد کنیم، اما مثال زیر دیدی کلی از ادامه این درس به ما می دهد:

```python
class Student:
    pass
```

در اینجا یک Class با نام `Student` ایجاد کرده ایم.

بعداً می توانیم Objectهایی از آن ایجاد کنیم:

```python
student1 = Student()
student2 = Student()
```

در این حالت:

```text
Student
   │
   ├── student1
   └── student2
```

این دو، Objectهای متفاوتی هستند که از یک Class ساخته شده اند.

در ادامه قدم به قدم یاد می گیریم که چگونه به این Objectها Data و Behavior اضافه کنیم.

---

## ۱۵. چه زمانی باید از OOP استفاده کنیم؟

OOP معمولاً زمانی مفید است که برنامه چند Entity مختلف داشته باشد که هرکدام Data و Behavior مخصوص خودشان را دارند.

مثال های مناسب:

- برنامه های بانکی
- فروشگاه های اینترنتی
- سیستم های مدیریت مدرسه
- بازی ها
- سیستم های مدیریت انبار
- سیستم های مدیریت کارمندان
- سیستم های رزرو
- APIها و Applicationهای بزرگ

برای مثال، یک فروشگاه اینترنتی می تواند شامل مفاهیم زیر باشد:

```text
User
Product
ShoppingCart
Order
Payment
Address
```

هرکدام از این مفاهیم می توانند Data و Behavior مخصوص خودشان را داشته باشند.

OOP روشی برای مدل سازی و سازمان دهی این مفاهیم در برنامه در اختیار ما قرار می دهد.

---

## ۱۶. چه زمانی بهتر است از OOP استفاده نکنیم؟

هر برنامه ای به Class نیاز ندارد.

برای مثال:

```python
numbers = [10, 20, 30, 40]

total = sum(numbers)

print(total)
```

در این برنامه دلیل خاصی برای ایجاد یک Class فقط برای محاسبه مجموع وجود ندارد.

همچنین:

```python
def greet(name):
    return f"Hello, {name}!"
```

برای این Function ساده هم نیازی به Class نداریم.

یک قانون مفید این است:

> از ساده ترین ساختاری استفاده کن که مسئله را به شکل واضح حل می کند.

OOP یک ابزار است، نه یک الزام.

---

## ۱۷. اشتباهات رایج

### اشتباه ۱: فکر کردن به اینکه Class و Object یکی هستند

Class یک Blueprint یا الگو است.

Object یک Instance ساخته شده از آن Blueprint است.

```text
Class → Blueprint
Object → Instance
```

---

### اشتباه ۲: ساختن Class برای همه چیز

Class لزوماً بهتر از Function نیست.

اگر یک Function ساده می تواند مسئله را به شکل واضح حل کند، از همان Function استفاده کنید.

---

### اشتباه ۳: یادگیری Syntax بدون درک مدل ذهنی

ممکن است Syntax زیر را حفظ کنیم:

```python
class Student:
    pass
```

اما هنوز ندانیم Class واقعاً چه چیزی را نمایش می دهد.

ابتدا باید مفاهیم اصلی را درک کنیم:

```text
Class
   ↓
Blueprint

Object
   ↓
Instance

Attributes
   ↓
Data

Methods
   ↓
Behavior
```

وقتی این مدل ذهنی مشخص باشد، یادگیری Syntax بسیار ساده تر می شود.

---

### اشتباه ۴: تصور اینکه OOP فقط درباره Inheritance است

Inheritance فقط یکی از بخش های OOP است.

مفاهیم مهم OOP شامل موارد زیر هستند:

- Classها
- Objectها
- Attributeها
- Methodها
- Encapsulation
- Abstraction
- Inheritance
- Polymorphism

در ادامه این مفاهیم را قدم به قدم یاد می گیریم.

---

## ۱۸. مرور نهایی

در این Part یاد گرفتیم که:

- OOP مخفف **Object-Oriented Programming** است.
- OOP برنامه را حول Objectها سازمان دهی می کند.
- Objectها می توانند Data و Behavior داشته باشند.
- **Class** مانند یک Blueprint یا الگو است.
- **Object** یک Instance از Class است.
- Methodها معمولاً Behavior را نمایش می دهند.
- Attributeها معمولاً Data را نمایش می دهند.
- OOP می تواند سازمان دهی و Reusability کد را بهتر کند.
- OOP برای برنامه های بزرگ تر و ساختارمندتر مفید است.
- همه مسائل به Class نیاز ندارند.
- Encapsulation، Abstraction، Inheritance و Polymorphism از مفاهیم مهم OOP هستند که در ادامه یاد می گیریم.

مهم ترین مدل ذهنی این Part:

```text
Class
  ↓
Blueprint

Object
  ↓
Instance

Attributes
  ↓
Data

Methods
  ↓
Behavior
```

---

## سوال ها

### سوال ۱

تفاوت اصلی بین یک Class و یک Object چیست؟

### سوال ۲

چرا OOP می تواند سازمان دهی یک برنامه بزرگ را ساده تر کند؟

### سوال ۳

آیا همه برنامه های Python باید از Class استفاده کنند؟ توضیح دهید چرا یا چرا نه.

---

## سوال جامع

فرض کنید قرار است یک **سیستم مدیریت کتابخانه** بسازید.

این سیستم باید کتاب ها را مدیریت کند.

هر کتاب دارای موارد زیر است:

- عنوان
- نویسنده
- سال انتشار
- قیمت

هر کتاب در آینده باید بتواند کارهایی مانند موارد زیر را انجام دهد:

- نمایش اطلاعات
- امانت داده شدن
- پس گرفته شدن

به سوال های زیر پاسخ دهید:

1. Class چه چیزی را می تواند نمایش دهد؟
2. Objectها چه چیزی را می توانند نمایش دهند؟
3. کدام موارد Attribute هستند؟
4. کدام موارد Method هستند؟
5. چرا استفاده از OOP در اینجا می تواند بهتر از نگه داری اطلاعات در Variableها و Functionهای جداگانه باشد؟

فعلاً لازم نیست Class کامل را بنویسید. هدف این سوال طراحی مفهومی ساختار برنامه است.