
## 🌀 Python `while` takrorlash operatori — To‘liq qo‘llanma

### 📌 1. `while` operatori nima?

`while` — bu shart asosida takrorlanadigan sikl (loop). Shart `True` bo‘lsa, u har doim ishlaydi. Shart `False` bo‘lganda esa to‘xtaydi.

**Umumiy sintaksisi:**

```python
while shart:
    # bu yerda bajariladigan kodlar
```

### 🎯 2. Oddiy misol

```python
i = 1
while i <= 5:
    print(i)
    i += 1
```

**Natija:**

```
1
2
3
4
5
```

### 🧠 3. Ichki mantiq

* Dastlab `i = 1`
* `while i <= 5` → `True` bo‘ladi, `print(i)` ishlaydi
* `i` har safar 1 ga oshiriladi (`i += 1`)
* `i` 6 bo‘lganda shart `False` bo‘ladi va sikl to‘xtaydi

---

### ⚠️ 4. Cheksiz sikl (Infinite Loop)

Agar shart hech qachon `False` bo‘lmasa, sikl hech qachon tugamaydi.

```python
while True:
    print("Salom!")
```

Bunday holatlarda `break` operatoridan foydalanish mumkin:

```python
while True:
    javob = input("To'xtatish uchun 'stop' deb yozing: ")
    if javob == "stop":
        break
```

---

### 🔁 5. `break` va `continue`

* `break` → siklni to‘xtatadi
* `continue` → qolgan kodlarni o‘tkazib yuboradi va siklning keyingi aylanishiga o‘tadi

```python
i = 0
while i < 5:
    i += 1
    if i == 3:
        continue
    print(i)
```

**Natija:**

```
1
2
4
5
```

---

### 🧪 6. Amaliy mashqlar

#### 1-masala: 1 dan 10 gacha bo‘lgan sonlarni chiqaruvchi kod yozing.

```python
i = 1
while i <= 10:
    print(i)
    i += 1
```

#### 2-masala: Foydalanuvchi `0` kiritsincha sonlar kiritilsin va yig‘indisi hisoblasin.

```python
yigindi = 0
son = int(input("Son kiriting: "))

while son != 0:
    yigindi += son
    son = int(input("Yana son kiriting: "))

print("Yig'indi:", yigindi)
```

#### 3-masala: Parol to‘g‘ri kiritilmaguncha foydalanuvchidan so‘rash

```python
parol = "1234"
kiritilgan = ""

while kiritilgan != parol:
    kiritilgan = input("Parolni kiriting: ")

print("To‘g‘ri parol!")
```

---

### ✅ 7. Xulosa

* `while` sharti `True` bo‘lsa, sikl ishlaydi
* Har bir siklda shart yangilanishiga e'tibor bering (`i += 1` yoki `input`)
* `break` va `continue` orqali siklni boshqarish mumkin

