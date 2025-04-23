# Python Dasturlash Asoslari: Mustahkamlash Tutoriali

## Kirish

Ushbu tutorialda siz Python dasturlash tilining asosiy tushunchalarini mustahkamlashingiz va ularni amaliyotda qo'llashingiz mumkin. Quyidagi mavzularni qamrab olamiz:
- Built-in funksiyalar
- Primitive ma'lumot turlari va o'zgaruvchilar
- Operatorlar
- Satrlar (Strings)
- Shartli operatorlar (if-elif-else)

## 1. Built-in Funksiyalar

Python tili bilan birga keladigan foydali funksiyalar:

### Asosiy built-in funksiyalar:

```python
# print() - chop etish
print("Hello World!")

# len() - uzunlik
print(len("Python"))  # 6

# type() - ma'lumot turi
print(type(10))      # <class 'int'>
print(type(3.14))    # <class 'float'>
print(type("text"))  # <class 'str'>

# input() - foydalanuvchi kiritimi
ism = input("Ismingizni kiriting: ")
print(f"Salom, {ism}!")

# int(), float(), str() - tur o'zgartirish
yosh = int(input("Yoshingiz: "))
print(f"Siz {yosh + 5} yildan keyin {yosh + 5} yoshda bo'lasiz")

# abs() - modul
print(abs(-10))  # 10

# round() - yaxlitlash
print(round(3.14159, 2))  # 3.14
```

### Amaliy mashq:
1. Foydalanuvchidan ikkita son qabul qiling va ularning yig'indisi, ayirmasi, ko'paytmasi va bo'linmasini hisoblang.
2. Foydalanuvchidan ismini so'rang va uning uzunligini hisoblab, ekranga chiqaring.

## 2. Primitive Ma'lumot Turlari va O'zgaruvchilar

Python asosiy ma'lumot turlari:

```python
# Integer (Butun son)
a = 10
b = -5

# Float (Haqiqiy son)
pi = 3.14159
temp = -2.5

# String (Satr)
ism = "Ali"
familiya = 'Valiyev'

# Boolean (Mantiqiy)
togri = True
notogri = False

# NoneType
qiymat = None
```

### O'zgaruvchilar bilan ishlash:

```python
# Qiymat berish
x = 5
y = 3.14
matn = "Salom"

# Bir nechta o'zgaruvchiga qiymat berish
a, b, c = 1, 2, 3

# O'zgaruvchi turini o'zgartirish
yosh = "25"
yosh_int = int(yosh)  # 25
```

### Amaliy mashq:
1. Quyidagi o'zgaruvchilarni yarating:
   - Ismingiz (string)
   - Yoshingiz (integer)
   - Bo'yingiz (float)
   - Talabamisiz? (boolean)
2. Ularni f-string yordamida chiroyli qilib ekranga chiqaring.

## 3. Operatorlar

### Arifmetik operatorlar:

```python
a = 10
b = 3

print(a + b)   # 13
print(a - b)   # 7
print(a * b)   # 30
print(a / b)   # 3.333...
print(a // b)  # 3 (butun bo'lish)
print(a % b)   # 1 (qoldiq)
print(a ** b)  # 1000 (daraja)
```

### Taqqoslash operatorlari:

```python
x = 5
y = 8

print(x == y)  # False
print(x != y)  # True
print(x > y)   # False
print(x < y)   # True
print(x >= y)  # False
print(x <= y)  # True
```

### Mantiqiy operatorlar:

```python
a = True
b = False

print(a and b)  # False
print(a or b)   # True
print(not a)    # False
```

### Amaliy mashq:
1. Foydalanuvchidan ikkita son qabul qiling va quyidagilarni tekshiring:
   - Birinchi son ikkinchisidan kattami?
   - Ikkala son tengmi?
   - Ikkala son ham 0 dan kattami?

## 4. Satrlar (Strings)

### Satrlar bilan ishlash:

```python
s = "Python Dasturlash"

# Indekslash
print(s[0])    # 'P'
print(s[-1])   # 'h'

# Kesib olish
print(s[2:5])  # 'tho'
print(s[:6])   # 'Python'
print(s[7:])   # 'Dasturlash'

# Metodlar
print(s.lower())      # 'python dasturlash'
print(s.upper())      # 'PYTHON DASTURLASH'
print(s.split())      # ['Python', 'Dasturlash']
print(s.replace('Python', 'JavaScript'))  # 'JavaScript Dasturlash'
print(len(s))         # 17
```

### F-string:

```python
ism = "Ali"
yosh = 25
print(f"{ism} {yosh} yoshda")  # Ali 25 yoshda
```

### Amaliy mashq:
1. Foydalanuvchidan matn qabul qiling va:
   - Matnni teskari tartibda chiqaring
   - Matndagi harflarni katta harfga o'zgartiring
   - Matnning uzunligini hisoblang

## 5. Shartli Operatorlar (if-elif-else)

### Oddiy shart:

```python
yosh = 18

if yosh >= 18:
    print("Siz voyaga yetgansiz")
else:
    print("Siz hali voyaga yetmagansiz")
```

### Bir nechta shart:

```python
baho = 85

if baho >= 90:
    print("A'lo")
elif baho >= 80:
    print("Yaxshi")
elif baho >= 70:
    print("Qoniqarli")
else:
    print("Qoniqarsiz")
```

### Ichma-ich shartlar:

```python
login = "admin"
parol = "12345"

if login == "admin":
    if parol == "12345":
        print("Xush kelibsiz!")
    else:
        print("Noto'g'ri parol")
else:
    print("Noto'g'ri login")
```

### Amaliy mashq:
1. Foydalanuvchidan son qabul qiling va:
   - Agar son musbat bo'lsa "Musbat"
   - Agar son manfiy bo'lsa "Manfiy"
   - Agar son 0 ga teng bo'lsa "Nol" deb chiqaring
2. Foydalanuvchidan login va parol so'rang. Agar:
   - Login "admin" va parol "12345" bo'lsa - "Xush kelibsiz"
   - Login "admin" lekin parol noto'g'ri bo'lsa - "Noto'g'ri parol"
   - Boshqa hollarda - "Noto'g'ri login" chiqaring

## Yakuniy Loyiha

Quyidagi dasturni yozing:
1. Foydalanuvchidan quyidagi ma'lumotlarni so'rang:
   - Ism
   - Yosh
   - Sevimli dasturlash tili
2. Quyidagilarni tekshiring:
   - Agar yosh 18 dan katta bo'lsa, "Siz dasturlashni o'rganishingiz mumkin"
   - Agar sevimli til "Python" bo'lsa, "Ajoyib tanlov!"
3. Barcha ma'lumotlarni chiroyli qilib ekranga chiqaring

```python
# Yechim namuna
ism = input("Ismingizni kiriting: ")
yosh = int(input("Yoshingizni kiriting: "))
til = input("Sevimli dasturlash tilingiz: ")

print(f"\nFoydalanuvchi ma'lumotlari:")
print(f"Ism: {ism}")
print(f"Yosh: {yosh}")
print(f"Sevimli til: {til}")

if yosh > 18:
    print("Siz dasturlashni o'rganishingiz mumkin")
else:
    print("Siz hali dasturlashni o'rganish uchun yoshsiz")

if til.lower() == "python":
    print("Ajoyib tanlov!")
```

Ushbu tutorial orqali siz Python dasturlash asoslarini mustahkamlashingiz va amaliy ko'nikmalarga ega bo'lishingiz mumkin. Har bir mavzuga oid mashqlarni bajarish orqali bilimingizni mustahkamlang!
