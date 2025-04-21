# 🧠 **Lesson 05: `if`, `else`, `elif` Statement in Python**

---

## 🎯 Darsning asosiy maqsadi:

- Shart operatorlari (`if`, `else`, `elif`) bilan ishlashni o‘rganish  
- Dastur qanday qaror chiqarishini tushunish  
- Mantiqiy ifodalarni tahlil qilish  
- Haqiqiy hayotiy muammolarni `if-else` yordamida yechish

---

## 🔹 1. `if` — **Shart rost bo‘lsa, bajariladigan kod**

```python
temp = 30
if temp > 25:
    print("Bugun issiq kun!")
```

🧠 **Tushuncha:** `if` dan keyingi shart (`temp > 25`) rost bo‘lsa, pastdagi `print` bajariladi.

---

## 🔹 2. `if-else` — **Shart noto‘g‘ri bo‘lsa, boshqa kod bajariladi**

```python
temp = 18
if temp > 25:
    print("Bugun issiq kun!")
else:
    print("Bugun unchalik issiq emas.")
```

---

## 🔹 3. `elif` — **Bir nechta shartlarni ketma-ket tekshirish**

```python
mark = 65

if mark >= 90:
    print("A")
elif mark >= 80:
    print("B")
elif mark >= 70:
    print("C")
else:
    print("D")
```

---

## 🔹 4. Ichma-ich (`nested`) `if`

```python
username = "admin"
password = "1234"

if username == "admin":
    if password == "1234":
        print("Kirish muvaffaqiyatli!")
    else:
        print("Parol noto‘g‘ri!")
else:
    print("Foydalanuvchi topilmadi.")
```

---

## 🔹 5. Mantiqiy operatorlar bilan

| Operator | Ma’nosi        | Misol                  |
|----------|----------------|------------------------|
| `and`    | Har ikkala shart rost bo‘lsa | `x > 5 and y < 10` |
| `or`     | Bittasi rost bo‘lsa yetarli | `x < 0 or x > 100` |
| `not`    | Shartni inkor etadi  | `not(x > 5)`         |

```python
age = 25
name = "Ali"

if age > 18 and name == "Ali":
    print("Xush kelibsiz, Ali!")
```

---

## 🔸 BONUS: Foydalanuvchidan qiymat olish

```python
age = int(input("Yoshingizni kiriting: "))
if age >= 18:
    print("Sizga ruxsat berildi!")
else:
    print("Kechirasiz, yoshingiz yetmaydi.")
```

---

# ✅ Amaliy mashqlar (dars davomida bajariladigan)

---

### 1. Juft yoki toq sonni aniqlash  
🔹 **Vazifa:** Foydalanuvchi kiritgan son juftmi yoki toqmi aniqlang.

💡 *Hint:* `son % 2 == 0` — juft sonni bildiradi.

---

### 2. Musbat, manfiy yoki nol  
🔹 **Vazifa:** Raqamni tekshiring — musbat, manfiy yoki nol.

---

### 3. Baholash tizimi  
🔹 **Vazifa:** 0–100 oralig‘ida baho kiriting. Quyidagi shartlarga qarab harfli bahoni chiqaring:  
- 90-100: A  
- 80-89: B  
- 70-79: C  
- 60-69: D  
- <60: F

---

### 4. Kirish tekshiruvi  
🔹 **Vazifa:** Foydalanuvchi login va parol kiritadi. Agar ikkalasi to‘g‘ri bo‘lsa — “Kirish muvaffaqiyatli” chiqsin, aks holda “Kirish rad etildi”.

💡 *Hint:* `if login == "admin" and password == "1234":`

---

### 5. Tenglikni tekshirish  
🔹 **Vazifa:** 2 ta son kiritiladi.  
Ular:  
- teng bo‘lsa: `"Sonlar teng"`  
- birinchi katta bo‘lsa: `"Birinchi katta"`  
- ikkinchisi katta bo‘lsa: `"Ikkinchi katta"`

---

### 6. Yil kabisa yili ekanligini aniqlang  
🔹 **Vazifa:** Foydalanuvchi yil kiritadi. Kabisa yili bo‘lsa `"Kabisa yili"` chiqsin.

💡 *Hint:* `(yil % 4 == 0 and yil % 100 != 0) or yil % 400 == 0`

---

### 7. Parol kuchliligini tekshiring  
🔹 **Vazifa:** Agar parol uzunligi 8 dan katta bo‘lsa va ichida `@` belgisi bo‘lsa — “Kuchli parol” deb chiqsin.

---

## 📌 Savol-javoblar

1. `if` va `elif` farqi nimada?  
2. `not` operatori nimaga xizmat qiladi?  
3. Quyidagi kod natijasi nima?

```python
x = 5
if x > 10:
    print("Katta")
else:
    print("Kichik")
```
