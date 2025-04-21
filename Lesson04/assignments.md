## 🟢 **Oson darajadagi mashqlar (boshlang‘ichlar uchun)**

### 1. **String yaratish va chiqarish**
```python
# 1.1. Quyidagi o'zgaruvchini yarat:
name = "Ali"

# 1.2. Uni ekranga chiqar. 
# 👉 Hint: print() funksiyasidan foydalan.
```

### 2. **String operatorlari: qo‘shish va ko‘paytirish**
```python
a = "Hello"
b = "World"

# 2.1. a va b ni birlashtirib, "HelloWorld" hosil qil.
# 👉 Hint: "+" operatori stringlarni birlashtiradi.

# 2.2. "Hello" so'zini 3 marta takrorlab chiqar.
# 👉 Hint: "*" operatori stringni ko‘paytiradi.
```

### 3. **Stringdagi harflarni olish (indexing)**
```python
word = "Python"

# 3.1. Birinchi harfni chiqar (ya'ni 'P')
# 👉 Hint: Stringda harflar 0-dan boshlanadi.

# 3.2. Oxirgi harfni chiqar (ya'ni 'n')
# 👉 Hint: Manfiy indeksdan (-1) foydalansang bo‘ladi.
```

### 4. **Stringdan bo‘lak ajratish (slicing)**
```python
message = "Hello, Python World!"

# 4.1. Faqat "Hello" qismini ajratib ol.
# 👉 Hint: [0:5] kabi slicing ishlatiladi.

# 4.2. "Python" qismini ajratib ol.
# 👉 Hint: Belgilar sanog‘ini to‘g‘ri hisobla.
```

### 5. **String methodlaridan foydalanish**
```python
text = "i love python"

# 5.1. Barcha harflarni katta harfga o‘zgartir.
# 👉 Hint: upper() methodidan foydalan.

# 5.2. "python" so'zini "programming" bilan almashtir.
# 👉 Hint: replace() methodi yordam beradi.
```

---

## 🟡 **O‘rta darajadagi mashqlar (biroz murakkabroq)**

### 1. **Foydalanuvchidan ism olish va chiqarish**
```python
# Foydalanuvchidan ismingizni kiriting:
# So'ng: "Salom, [ism]!" deb chiqarilsin.
# 👉 Hint: input() funksiyasi bilan ism ol va print() bilan chiqar.
```

### 2. **Slicing va teskari yozish**
```python
word = "Programming"

# 2.1. "gram" qismini ajratib ol.
# 👉 Hint: "g" harfi qayerda boshlanadi?

# 2.2. So'zni teskari qilib chiqar. Ya'ni "gnimmargorP"
# 👉 Hint: slicingda [::-1] yozsa teskari bo‘ladi.
```

### 3. **Methodlar bilan ishlash**
```python
sentence = "  Python is Fun!  "

# 3.1. Harflarni kichik qilib chiqar.
# 👉 Hint: lower() methodi.

# 3.2. Ortidagi bo‘sh joylarni olib tashla.
# 👉 Hint: strip() methodi bo‘sh joylarni olib tashlaydi.

# 3.3. 'Fun' so’zining qaysi indexda joylashganini top.
# 👉 Hint: find("Fun")
```

### 4. **Ism va familiyani birlashtirish**
```python
# Foydalanuvchidan ism va familiya so‘raladi.
# Ularni birlashtirib "Ismingiz: Ali Valiyev" ko‘rinishida chiqar.
# 👉 Hint: input() + "+" yoki f-string.
```

---

## 🔴 **Qiyin darajadagi mashqlar (challenge)**

### 1. **Palindrom tekshirish**
```python
# Foydalanuvchi bir so‘z kiritadi.
# Agar bu so‘z teskari o‘qiganda ham o‘sha bo‘lsa, "Palindrom" deb chiqar.
# Aks holda "Palindrom emas" deb yoz.

# 👉 Hint: so‘zni teskari qilib [::-1] bilan solishtir.
```

### 2. **Har bir so‘zni katta harf bilan boshlash**
```python
sentence = "python is amazing"

# Natija: "Python Is Amazing"
# 👉 Hint: title() methodi har bir so‘zni bosh harf bilan boshlaydi.
```

### 3. **Belgilarni sanash**
```python
text = "Python programming is powerful and popular."

# 'p' harfi necha marta qatnashganini aniqlang (katta-kichik farqsiz).
# 👉 Hint: text.lower().count("p")
```

### 4. **Oddiy shifrlash (Caesar cipher)**
```python
# Foydalanuvchi so‘z kiritadi.
# Har bir harfni alifbodagi keyingi harfga o‘zgartir:
# Masalan: "abc" → "bcd"

# 👉 Hint: chr() va ord() funksiyalaridan foydalan.
# ord('a') → 97, chr(98) → 'b'
```
