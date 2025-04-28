# 🐍 Python For Loop - To'liq Dars va Qo'llanma

---

## 1. For Loop nima?

Python'da **for loop** yordamida biror ro'yxat, matn yoki ketma-ketlikdagi barcha elementlarni navbat bilan ko'rib chiqish mumkin.

**Asosiy shakli:**
```python
for element in collection:
    # har bir element uchun bajariladigan kod
```

- `element` — har bir aylanada ro'yxatdagi bitta qiymat bo'ladi
- `collection` — ro'yxat (list), matn (string), range va boshqalar bo'lishi mumkin

---

## 2. Oddiy misol: Ro'yxatni chiqarish

```python
mevalar = ['olma', 'banan', 'gilos']
for meva in mevalar:
    print(meva)
```

**Natija:**
```
olma
banan
gilos
```

> ❗ Har safar `for` ichida `meva` o'zgaruvchisi ro'yxatdagi keyingi elementni oladi.

---

## 3. String (matn) ustida For Loop

Matn ham belgilar ketma-ketligi (string = sequence).  
Shuning uchun matndagi har bir harfni ko'rib chiqish mumkin:

```python
ism = "Python"
for harf in ism:
    print(harf)
```

**Natija:**
```
P
y
t
h
o
n
```

---

## 4. Range() va For Loop

Agar ro'yxatimiz bo'lmasa, lekin ma'lum sonlar ketma-ketligini yaratmoqchi bo'lsak — **range()** funksiyasidan foydalanamiz.

```python
for son in range(5):
    print(son)
```

**Natija:**
```
0
1
2
3
4
```

> `range(5)` — bu 0 dan 4 gacha bo'lgan sonlar ketma-ketligi.

---

## 5. Amaliy For Loop Misollar

### 5.1 Ro'yxatdagi sonlarni ikki barobar oshirish

```python
sonlar = [1, 2, 3, 4, 5]
for son in sonlar:
    print(son * 2)
```
➡️ Har bir son 2 barobarga ko'payadi.

---

### 5.2 Stringni teskari o'qish

```python
matn = "hello"
teskari = ""

for harf in matn:
    teskari = harf + teskari

print(teskari)
```
➡️ Matn teskari o'qiladi.

---

### 5.3 Har bir mevaning uzunligini chiqarish

```python
mevalar = ['olma', 'banan', 'gilos']
for meva in mevalar:
    print(f"{meva} - {len(meva)} harf")
```
➡️ Mevalar va ularning uzunliklari ko'rsatiladi.

---

## 6. Shart bilan For Loop (if ichida)

For loop ichida shart (`if`) ishlatish ham mumkin.  
Misol uchun, faqat juft sonlarni chiqarish:

```python
sonlar = [12, 7, 9, 24, 5, 18]
for son in sonlar:
    if son % 2 == 0:
        print(son)
```

➡️ Faqat juft sonlar chiqariladi: 12, 24, 18

---

## 7. Break va Continue

**Break** — for loopni to'xtatadi.

```python
for i in range(10):
    if i == 5:
        break
    print(i)
```
➡️ 0 dan 4 gacha chiqaradi, 5 ga kelganda to'xtaydi.

---

**Continue** — faqat shu bosqichni o'tkazib yuboradi.

```python
for i in range(10):
    if i % 2 == 0:
        continue
    print(i)
```
➡️ Faqat toq sonlar chiqariladi.

---

## 8. Narxlar bilan amaliy mashqlar

Narxlar ro'yxati ustida ishlashni o'rganamiz.

---

### 8.1 Narxlarni ikki barobarga oshirish

```python
narxlar = [10000, 25000, 5000, 12000]
for narx in narxlar:
    print(narx * 2)
```

---

### 8.2 10000 so'mdan katta narxlarni chiqarish

```python
narxlar = [7000, 15000, 20000, 5000]
for narx in narxlar:
    if narx > 10000:
        print(narx)
```

---

### 8.3 Har bir narxga 5000 qo'shish

```python
narxlar = [8000, 14000, 23000, 9000]
for narx in narxlar:
    print(narx + 5000)
```

---

### 8.4 15% chegirma bilan narxlarni chiqarish

```python
narxlar = [20000, 30000, 15000, 40000]
for narx in narxlar:
    chegirma = narx * 0.15
    yangi_narx = narx - chegirma
    print(f"Asl narx: {narx}, Chegirmali narx: {int(yangi_narx)}")
```

---
