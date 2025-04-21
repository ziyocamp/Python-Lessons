# 🐍 Python String Tutorial  
## 🎯 Mavzular:  
- String yaratish  
- String operatorlari  
- String indexing  
- String slicing  
- String metodlari  

---

## 1️⃣ **String yaratish (String Creation)**

Python'da string matnli ma’lumotlarni saqlash uchun ishlatiladi. Ular **ikki (" ") yoki bitta (‘ ’) qo‘shtirnoq** ichida yoziladi.

```python
name = "Ali"
city = 'Toshkent'
```

✅ **Izoh:** O‘zgaruvchi ichida saqlanayotgan qiymat - string (`str`) turida bo‘ladi.

---

## 2️⃣ **String operatorlari**

### ➕ Qo‘shish (Concatenation)

```python
first = "Hello"
second = "World"
result = first + " " + second
print(result)   # Hello World
```

### ✖️ Ko‘paytirish (Repetition)

```python
word = "Hi"
print(word * 3)   # HiHiHi
```

✅ **Izoh:** `+` stringlarni birlashtiradi, `*` esa takrorlaydi.

---

## 3️⃣ **String indekslash (Indexing)**

String ichidagi harflar **0 dan boshlab** indekslanadi:

```python
text = "Python"
print(text[0])   # P
print(text[5])   # n
```

Manfiy indekslar oxirdan boshlab sanaydi:

```python
print(text[-1])  # n
print(text[-2])  # o
```

✅ **Izoh:** `text[0]` – birinchi harf, `text[-1]` – oxirgi harf.

---

## 4️⃣ **String kesish (Slicing)**

Slicing orqali stringning bir qismini ajratib olish mumkin:

```python
text = "Hello, World!"
print(text[0:5])     # Hello
print(text[7:12])    # World
```

### Teskari qilish (Reverse)

```python
print(text[::-1])   # !dlroW ,olleH
```

✅ **Format:** `string[start:end]`  
✅ **Izoh:** `start` dan `end-1` gacha bo‘lgan qismini ajratadi.

---

## 5️⃣ **String metodlari (String Methods)**

Python stringlar bilan ishlash uchun juda ko‘p **metodlar** beradi:

| Metod | Tavsifi | Misol |
|-------|---------|-------|
| `.upper()` | Hammasini katta harf | `"ali".upper()` → `'ALI'` |
| `.lower()` | Hammasini kichik harf | `"Ali".lower()` → `'ali'` |
| `.title()` | Har bir so‘z bosh harfi katta | `"python is fun".title()` → `'Python Is Fun'` |
| `.strip()` | Bo‘sh joylarni olib tashlaydi | `"  hello  ".strip()` → `'hello'` |
| `.replace(old, new)` | So‘z almashtiradi | `"apple".replace("a", "b")` → `'bpple'` |
| `.find()` | Belgining indeksini topadi | `"apple".find("p")` → `1` |
| `.count()` | Belgini necha marta qatnashganini hisoblaydi | `"apple".count("p")` → `2` |

---

## 💡 BONUS: Foydalanuvchidan ma’lumot olish
```python
name = input("Ismingizni kiriting: ")
print("Salom, " + name)
```

---

## ✅ Yakuniy tavsiyalar

📌 String – dasturlashda eng ko‘p ishlatiladigan ma’lumot turi.  
📌 Har bir metodni o‘zing mustaqil sinab ko‘r!  
📌 `dir(str)` buyrug‘i orqali stringga tegishli barcha metodlarni ko‘rish mumkin.

---
