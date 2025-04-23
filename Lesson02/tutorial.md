# Python Dasturlash Tili: Primitive Ma'lumot Turlari va O'zgaruvchilar

## Kirish

Python dasturlash tilida ishlashni boshlash uchun birinchi o'rganiladigan mavzulardan biri - primitive (oddiy) ma'lumot turlari va o'zgaruvchilar (variables). Ushbu tutorialda biz batafsil va amaliy misollar bilan bu tushunchalarni o'rganamiz.

## O'zgaruvchilar (Variables) nima?

O'zgaruvchilar - bu kompyuter xotirasida ma'lumotlarni saqlash uchun ajratilgan joylar. Siz ularga nom berasiz va qiymatlar tayinlaysiz (assign qilasiz).

```python
ism = "Ali"
yosh = 25
```

Yuqoridagi misolda:
- `ism` - o'zgaruvchi nomi
- `"Ali"` - o'zgaruvchiga tayinlangan qiymat
- `=` - tayinlash operatori (assignment operator)

## Primitive Ma'lumot Turlari

Pythonda asosiy (primitive) ma'lumot turlari quyidagilardan iborat:

### 1. Butun sonlar (Integers - int)

Butun sonlarni ifodalash uchun ishlatiladi.

```python
a = 10
b = -5
c = 0
```

Xususiyatlari:
- Hech qanday kasr qismi yo'q
- Ijobiy, manfiy yoki 0 bo'lishi mumkin
- Cheksiz katta yoki kichik bo'lishi mumkin (faqat kompyuter xotirasi bilan cheklangan)

Amaliy misol:
```python
# Aholi soni
aholi = 37_000_000  # Pastki chiziq (_) sonlarni o'qishni osonlashtiradi
print(aholi)  # 37000000

# Harorat
harorat = -15
print(f"Tashqarida {harorat} gradus sovuq")  # Tashqarida -15 gradus sovuq
```

### 2. Haqiqiy sonlar (Floating-point numbers - float)

Kasrli sonlarni ifodalash uchun ishlatiladi.

```python
pi = 3.14159
salom = -0.5
katta_son = 2.5e6  # 2.5 * 10^6 = 2500000.0
```

Xususiyatlari:
- Kasr nuqtasi bilan ifodalanadi
- `e` yoki `E` bilan ilmiy ko'rinishda yozilishi mumkin
- Aniqlik cheklovlari mavjud (floating point precision)

Amaliy misol:
```python
# O'rtacha ball
average = 4.75
print(f"O'rtacha baho: {average}")  # O'rtacha baho: 4.75

# Ilmiy ko'rinishda
avogadro_soni = 6.022e23
print(f"Avogadro soni: {avogadro_soni}")  # Avogadro soni: 6.022e+23
```

### 3. Mantiqiy qiymatlar (Booleans - bool)

Faqat ikkita qiymat qabul qiladi: `True` (rost) yoki `False` (yolg'on).

```python
togri = True
notogri = False
```

Xususiyatlari:
- Mantiqiy amallar (comparisons) natijasida hosil bo'ladi
- Shartli operatorlarda (if/else) ishlatiladi
- `True` qiymati 1 ga, `False` esa 0 ga teng deb hisoblanadi

Amaliy misol:
```python
yomgir_yogayapti = True
qor_yogayapti = False

if yomgir_yogayapti:
    print("Soyabon oling!")  # Soyabon oling!
    
print(True + True)  # 2 (1 + 1)
```

### 4. Satrlar (Strings - str)

Matnli ma'lumotlarni ifodalash uchun ishlatiladi. Bitta (' ') yoki ikkita (" ") qo'shtirnoq ichida yoziladi.

```python
ism = "Anvar"
familiya = 'Hasanov'
manzil = """Toshkent shahar,
Chilonzor tumani"""
```

Xususiyatlari:
- Unicode belgilar ketma-ketligi
- Indekslanishi mumkin (har bir belgiga alohida murojat qilish)
- O'zgarmas (immutable) ma'lumot turi

Amaliy misol:
```python
# Ko'p qatorli matn
she_r = """
Seni sevaman,
Yuraklar shod,
Hayot achchiq,
Lekin shirin.
"""
print(she_r)

# F-string (Python 3.6+)
yosh = 20
print(f"Men {yosh} yoshdaman")  # Men 20 yoshdaman
```

## O'zgaruvchilar bilan ishlash

### O'zgaruvchi nomlash qoidalari

1. Faqat harflar (a-z, A-Z), raqamlar (0-9) va pastki chiziq (_) ishlatilishi mumkin
2. Raqam bilan boshlanmaydi
3. Katta-kichik harflar farqlanadi (`yosh` va `Yosh` - turli o'zgaruvchilar)
4. Python kalit so'zlaridan (keywords) foydalanib bo'lmaydi (`if`, `else`, `for` va h.k.)

Yaxshi nomlash misollari:
```python
ism = "Ali"
familya = "Valiyev"
yosh = 25
_oilaviy_holati = "uylanmagan"
```

Yomon nomlash misollari:
```python
1ism = "Ali"  # Xato: raqam bilan boshlangan
is m = "Ali"  # Xato: bo'shliq ishlatilgan
if = 5  # Xato: kalit so'z ishlatilgan
```

### O'zgaruvchilarga qiymat berish

Python dinamik tipizatsiyalangan (dynamically typed) til bo'lib, o'zgaruvchining turi unga berilgan qiymatga qarab avtomatik aniqlanadi.

```python
x = 5       # int
x = "salom" # endi str
x = 3.14    # endi float
```

Bir nechta o'zgaruvchiga bir vaqtda qiymat berish:
```python
a, b, c = 1, 2, 3
x = y = z = 0
```

### Type Conversion (Tur o'zgartirish)

Ba'zan ma'lumot turlarini bir turdan ikkinchi turga o'zgartirish talab qilinishi mumkin.

```python
# str dan int ga
yosh = "25"
yosh_int = int(yosh)  # 25

# int dan float ga
butun_son = 10
kasr_son = float(butun_son)  # 10.0

# float dan int ga (kasr qismi yo'qotiladi)
pi = 3.14159
pi_int = int(pi)  # 3

# str dan float ga
narx = "15.99"
narx_float = float(narx)  # 15.99

# Har qanday narsadan str ga
son = 42
son_matn = str(son)  # "42"
```

### Type Checking (Turini tekshirish)

`type()` funksiyasi yordamida o'zgaruvchining turini aniqlash mumkin.

```python
print(type(10))        # <class 'int'>
print(type(3.14))      # <class 'float'>
print(type(True))      # <class 'bool'>
print(type("salom"))   # <class 'str'>
```

### O'zgaruvchilarni o'chirish

`del` operatori yordamida o'zgaruvchini o'chirish mumkin.

```python
x = 5
print(x)  # 5
del x
print(x)  # NameError: name 'x' is not defined
```

## Konstantalarga oid

Pythonda konstanta (o'zgarmas qiymat) tushunchasi mavjud emas, lekin dasturchilar odatda katta harflar bilan yozilgan nomlardan foydalanadilar.

```python
PI = 3.14159
MAX_USERS = 1000
```

## Foydali amaliyotlar

1. **O'zgaruvchilar bilan ishlash:**
```python
# O'zgaruvchilar yaratish
ism = "Sarvar"
yosh = 22
bo_yi = 1.75
talaba = True

# Qiymatlarni chop etish
print(f"Ism: {ism}")
print(f"Yosh: {yosh}")
print(f"Bo'y: {bo_yi}")
print(f"Talabami? {'Ha' if talaba else 'Yo'q'}")

# Tur o'zgartirish
yosh_matn = str(yosh)
print("Yosh matn ko'rinishida: " + yosh_matn)
```

2. **Matnlar bilan ishlash:**
```python
# Matnlarni birlashtirish
familiya = "Nosirov"
toliq_ism = ism + " " + familiya
print(toliq_ism)  # Sarvar Nosirov

# Matn metodlari
print(ism.upper())  # SARVAR
print(familiya.lower())  # nosirov
print(toliq_ism.title())  # Sarvar Nosirov
```

3. **Sonlar bilan ishlash:**
```python
# Matematik amallar
a = 10
b = 3
print(a + b)  # 13
print(a - b)  # 7
print(a * b)  # 30
print(a / b)  # 3.333...
print(a // b) # 3 (butun bo'lish)
print(a % b)  # 1 (qoldiq)
print(a ** b) # 1000 (daraja)

# Kompleks sonlar
c = 3 + 4j
print(c.real)  # 3.0
print(c.imag)  # 4.0
```

## Xatoliklar va ularning oldini olish

1. **Nomlash xatolari:**
```python
# 1son = 5  # SyntaxError: invalid syntax
son1 = 5    # To'g'ri
```

2. **Tur mos kelmasligi:**
```python
yosh = "yigirma"
# yosh + 5  # TypeError: can only concatenate str to str
```

3. **Mavjud bo'lmagan o'zgaruvchi:**
```python
# print(nomaqul_ozgaruvchi)  # NameError: name 'nomaqul_ozgaruvchi' is not defined
```

## Yakun

Ushbu tutorialda Python dasturlash tilidagi asosiy ma'lumot turlari va o'zgaruvchilar bilan tanishdingiz. Bu bilimlar har qanday dasturlash loyihasining asosini tashkil etadi. Keyingi qadamlar sifatida murakkab ma'lumot turlari (ro'yxatlar, lug'atlar, to'plamlar), operatorlar va nazorat tuzilmalarini o'rganishingiz mumkin.

Amaliyot - bu bilimlarni mustahkamlashning eng yaxshi usuli, shuning uchun ko'proq kod yozishga harakat qiling!
