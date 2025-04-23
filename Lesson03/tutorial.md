# Python Dasturlash Tili: Satrlar (Strings) bilan Ishlash

## Kirish

Satrlar (strings) - bu matnli ma'lumotlarni ifodalash uchun ishlatiladigan asosiy ma'lumot turlaridan biri. Python dasturlash tilida satrlar juda keng imkoniyatlarga ega bo'lib, ular bilan ishlashni tushunish har bir dasturchi uchun muhimdir.

## Satrlar nima?

Satr - bu belgilar ketma-ketligi. Pythonda satrlar bitta (`' '`) yoki ikkita (`" "`) qo'shtirnoq yoki uchta (`''' '''` yoki `""" """`) qo'shtirnoq orasida yoziladi.

```python
ism = "Anvar"
familiya = 'Hasanov'
manzil = """Toshkent shahri,
Chilonzor tumani"""
izoh = '''Bu ko'p qatorli
satr misoli'''
```

## Satr Yaratish Usullari

1. **Oddiy qo'shtirnoqlar bilan:**
```python
s1 = 'Salom dunyo!'
```

2. **Ikkitalik qo'shtirnoqlar bilan:**
```python
s2 = "Python dasturlash tili"
```

3. **Uchtalik qo'shtirnoqlar bilan (ko'p qatorli satrlar uchun):**
```python
s3 = """Bu birinchi qator.
Bu ikkinchi qator.
Bu uchinchi qator."""
```

4. **str() konstruktori orqali:**
```python
s4 = str(123)  # "123"
s5 = str(3.14)  # "3.14"
```

## Satrlar bilan Asosiy Amallar

### 1. Satrlarni birlashtirish (Concatenation)

`+` operatori yordamida satrlarni birlashtirish mumkin:

```python
ism = "Ali"
familiya = "Valiyev"
toliq_ism = ism + " " + familiya
print(toliq_ism)  # Ali Valiyev
```

### 2. Satrlarni takrorlash (Repetition)

`*` operatori yordamida satrni takrorlash mumkin:

```python
s = "Ha "
print(s * 3)  # Ha Ha Ha 
```

### 3. Satr uzunligi

`len()` funksiyasi satr uzunligini (belgilar sonini) qaytaradi:

```python
matn = "Dasturlash"
print(len(matn))  # 10
```

### 4. Satrga kirish (Indexing)

Satrlardagi har bir belgiga indeks orqali murojat qilish mumkin (indekslash 0 dan boshlanadi):

```python
s = "Python"
print(s[0])  # 'P'
print(s[3])  # 'h'
print(s[-1])  # 'n' (oxirgi belgi)
```

### 5. Kesib olish (Slicing)

`[start:stop:step]` sintaksisi yordamida satrning bir qismini kesib olish mumkin:

```python
s = "Dasturlash"
print(s[2:5])    # 'stu'
print(s[:4])     # 'Dast'
print(s[4:])     # 'urlash'
print(s[::2])    # 'Dsla' (har ikkinchi belgi)
print(s[::-1])   # 'hsalrutsaD' (teskari satr)
```

## Satr Metodlari

Python satrlar uchun juda ko'p foydali metodlarni taqdim etadi.

### 1. Katta/kichik harflarga o'zgartirish

```python
s = "Python Dasturlash"
print(s.lower())      # python dasturlash
print(s.upper())      # PYTHON DASTURLASH
print(s.capitalize()) # Python dasturlash
print(s.title())      # Python Dasturlash
print(s.swapcase())   # pYTHON dASTURLASH
```

### 2. Qidiruv metodlari

```python
s = "Python dasturlash asosi"
print(s.find('as'))       # 7 (birinchi topilgan joy)
print(s.rfind('as'))      # 17 (oxiridan qidirish)
print(s.index('thon'))    # 2
print(s.count('a'))       # 3 ('a' harfi soni)
print('python' in s)      # False (mavjudligini tekshirish)
```

### 3. Satrlarni tekshirish metodlari

```python
num = "123"
word = "Python"
space = "   "
print(num.isdigit())    # True
print(word.isalpha())   # True
print(space.isspace())  # True
print(word.islower())   # False
print(s.isupper())      # False
print(s.istitle())      # False
```

### 4. Tozalash va formatlash metodlari

```python
s = "   Python dasturlash   "
print(s.strip())        # "Python dasturlash"
print(s.lstrip())       # "Python dasturlash   "
print(s.rstrip())       # "   Python dasturlash"
print(s.center(30, '-')) # ---   Python dasturlash   ---
```

### 5. Satrlarni bo'lish va birlashtirish

```python
s = "Python,Java,C++,JavaScript"
print(s.split(','))     # ['Python', 'Java', 'C++', 'JavaScript']
print(' '.join(['Python', 'Dasturlash'])) # Python Dasturlash
```

### 6. Almashtirish

```python
s = "Python dasturlash"
print(s.replace('Python', 'JavaScript')) # JavaScript dasturlash
```

## Satr Formati (String Formatting)

### 1. f-string (Python 3.6+)

```python
ism = "Ali"
yosh = 25
print(f"{ism} {yosh} yoshda")  # Ali 25 yoshda
```

### 2. format() metodi

```python
print("{} {} yoshda".format(ism, yosh))  # Ali 25 yoshda
print("{1} {0} yoshda".format(yosh, ism)) # Ali 25 yoshda
```

### 3. % operatori (eski usul)

```python
print("%s %d yoshda" % (ism, yosh))  # Ali 25 yoshda
```

## Maxsus belgilar (Escape sequences)

Satrlarda maxsus belgilar `\` orqali ifodalanadi:

```python
print("Bu birinchi qator.\nBu ikkinchi qator.")  # \n - yangi qator
print("Bu \"qo'shtirnoq\" ichida")  # \" - qo'shtirnoq
print('Bu \'qo\'sh tirnoq\' ichida')  # \' - bittalik qo'shtirnoq
print("C:\\Users\\Document")  # \\ - backslash
print("Bu\tgorizontal\ttab")  # \t - tab
```

## Unicode va Satrlar

Python 3 da satrlar utf-8 kodirovkada saqlanadi:

```python
print("Привет")  # Ruscha
print("こんにちは")  # Yaponcha
print("سلام")  # Forscha
```

## Satrlar va Immutability

Satrlar o'zgarmas (immutable) ma'lumot turi hisoblanadi:

```python
s = "Python"
# s[0] = 'J'  # Xato: TypeError
# To'g'ri usul:
s = 'J' + s[1:]  # Jython
```

## Foydali Amaliyotlar

1. **Foydalanuvchi kiritgan matnni tahlil qilish:**
```python
matn = input("Matn kiriting: ")
print(f"Matn uzunligi: {len(matn)}")
print(f"Birinchi belgi: {matn[0]}")
print(f"Oxirgi belgi: {matn[-1]}")
print(f"Katta harflar: {matn.upper()}")
```

2. **Parol generatori:**
```python
import random
import string

uzunlik = 8
belgilar = string.ascii_letters + string.digits + "!@#$%^&*"
parol = ''.join(random.choice(belgilar) for _ in range(uzunlik))
print(f"Yangi parol: {parol}")
```

3. **Palindrom tekshiruvi:**
```python
soz = input("So'z kiriting: ")
if soz == soz[::-1]:
    print(f"{soz} - palindrom")
else:
    print(f"{soz} - palindrom emas")
```

4. **Matnni formatlash:**
```python
ism = "anvar"
familiya = "hasanov"
yosh = 30
print(f"Foydalanuvchi: {ism.title()} {familiya.title()}, {yosh} yosh")
# Foydalanuvchi: Anvar Hasanov, 30 yosh
```

## Xatoliklar va Echimlari

1. **Indeks chetdan chiqib ketishi:**
```python
s = "Python"
# print(s[10])  # IndexError
print(s[-6])  # P - to'g'ri
```

2. **Satr va sonlarni noto'g'ri birlashtirish:**
```python
yosh = 25
# print("Yosh: " + yosh)  # TypeError
print("Yosh: " + str(yosh))  # To'g'ri
```

3. **Formatlashda xatolik:**
```python
# print("Yosh: {age}".format(age=yosh))  # KeyError agar 'age' aniqlanmagan bo'lsa
print("Yosh: {}".format(yosh))  # To'g'ri
```

## Yakun

Satrlar - Python dasturlash tilining eng muhim qismlaridan biri bo'lib, ular bilan ishlashni yaxshi o'zlashtirish har bir dasturchi uchun zarur. Ushbu tutorialda siz satrlar bilan ishlashning asosiy usullari, metodlari va amaliy qo'llanilishlarini o'rgandingiz.

Keyingi qadamlar sifatida satrlar bilan murakkabroq amallar (regular expressions), fayllar bilan ishlash va ma'lumotlarni tahlil qilishni o'rganishingiz mumkin.

Ko'proq kod yozish orqali bilimingizni mustahkamlang!
