# Python Dasturlash Uyga Vazifalari (15 ta Task)

## Asosiy Ma'lumot Turlari va O'zgaruvchilar

**1. O'zgaruvchilar bilan ishlash**
```python
# Foydalanuvchidan ismi, yoshi va bo'yini so'rab, 
# quyidagi formatda chiqaring:
# "Mening ismim [Ism]. Men [Yosh] yoshdaman. Bo'yim [Bo'y] metr."
```

**2. Tur konvertatsiyasi**
```python
# Foydalanuvchidan ikkita son qabul qiling (string sifatida),
# ularni integerga o'zgartirib, yig'indisini hisoblang
```

**3. Doimiy qiymatlar**
```python
# PI (3.14159) va GRAVITATSIYA (9.8) konstantalarini e'lon qiling,
# ular yordamida aylana yuzi (πr²) va og'irlik (m*g) ni hisoblang
```

## Operatorlar

**4. Arifmetik amallar**
```python
# Foydalanuvchidan 3 ta son qabul qilib, ularning:
# - O'rta arifmetigi
# - Ko'paytmasi
# - Eng kattasini toping
```

**5. Taqqoslash operatorlari**
```python
# Foydalanuvchidan parol kiritishni so'rang.
# Agar parol "secret123" ga teng bo'lsa, "Xush kelibsiz!",
# aks holda "Noto'g'ri parol" chiqaring
```

**6. Mantiqiy operatorlar**
```python
# Foydalanuvchidan yoshini so'rang. Agar yosh:
# - 13 dan kichik bo'lsa - "Siz hali juda yoshsiz"
# - 13-18 oralig'ida - "Siz o'smir siz"
# - 18-60 oralig'ida - "Siz kattasiz"
# - 60+ - "Siz pensionersiz" chiqaring
```

## Satrlar (Strings)

**7. Satr metodlari**
```python
# Foydalanuvchidan ixtiyoriy matn qabul qilib:
# - Barcha harflarni katta qiling
# - Barcha harflarni kichik qiling
# - Matnni teskari tartibda chiqaring
```

**8. Satr formatlash**
```python
# Quyidagi ma'lumotlarni f-string yordamida chiqaring:
# product = "Olma", price = 15000, quantity = 2.5
# "2.5 kg Olma narxi: 37500 so'm"
```

**9. Satrni tekshirish**
```python
# Foydalanuvchidan email kiritishni so'rang.
# Agar emailda '@' belgisi bo'lmasa, "Noto'g'ri email" chiqaring
```

## Shartli Operatorlar (if-elif-else)

**10. Oddiy shart**
```python
# Foydalanuvchidan son kiritishni so'rang.
# Agar son juft bo'lsa "Juft son", toq bo'lsa "Toq son" chiqaring
```

**11. Murakkab shart**
```python
# Foydalanuvchidan 3 ta son kiritishni so'rang.
# Ularning eng kattasini topib, ekranga chiqaring
```

**12. Ichki shartlar**
```python
# Foydalanuvchidan login va parol so'rang:
# - Agar login "admin" va parol "12345" bo'lsa - "Xush kelibsiz!"
# - Agar login "admin" bo'lsa, lekin parol noto'g'ri - "Noto'g'ri parol"
# - Boshqa hollarda - "Noto'g'ri login"
```

## Integratsiyalashgan Mashqlar

**13. Kalkulyator**
```python
# Foydalanuvchidan 2 ta son va amal (+, -, *, /) so'rang.
# Kiritilgan amalga ko'ra hisoblovchi dastur yozing
```

**14. BMI hisoblagich**
```python
# Foydalanuvchidan bo'y (metrda) va vazn (kg) so'rang.
# BMI = vazn / (bo'y * bo'y)
# Agar BMI:
# - <18.5 - "Kam vazn"
# - 18.5-25 - "Normal"
# - 25-30 - "Ortiqcha vazn"
# - >30 - "Semizlik" chiqaring
```

**15. Ro'yxatdan o'tishda username tavsiya qiling**
Quyidagi formatlarda username generatsiya qiling:

1. ism_familiya (masalan: ali_valiyev)
2. ismfamiliya (masalan: alivaliyev)
3. ism[0]familiya[0] (masalan: av)
4. ism.otasining_ismi (masalan: ali.sharof)
5. familiya2024 (masalan: valiyev2024)

## Qo'shimcha Tavsiyalar

1. Har bir vazifani alohida .py fayl sifatida yozing
2. Kodlaringizga izohlar qo'shing (# yordamida)
3. Foydalanuvchi kiritishini har doim to'g'ri formatta olishga harakat qiling
4. Dasturlaringizda xatoliklarni (errors) oldini olish uchun tekshiruvlar qo'shing

## Namuna Yechimlar (1 va 2-vazifalar uchun)

**1-vazifa yechimi:**
```python
ism = input("Ismingizni kiriting: ")
yosh = input("Yoshingizni kiriting: ")
boy = input("Bo'yingizni kiriting (metrda): ")

print(f"Mening ismim {ism}. Men {yosh} yoshdaman. Bo'yim {boy} metr.")
```

**2-vazifa yechimi:**
```python
son1 = input("Birinchi sonni kiriting: ")
son2 = input("Ikkinchi sonni kiriting: ")

yigindi = int(son1) + int(son2)
print(f"{son1} + {son2} = {yigindi}")
```

Har bir vazifani mustaqil bajaring va kodlaringizni sinab ko'ring. Agar qiynalsangiz, Stack Overflow yoki boshqa resurslardan yordam olishingiz mumkin. Omad!
