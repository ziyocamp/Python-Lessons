# **Python For Loop - Oddiy va Amaliy Qo'llanma**

## **🔹 For Loop Asoslari**
For Loop - bu ketma-ketlikdagi elementlar bo'yicha aylanish uchun ishlatiladi.

**Oddiy misol:**
```python
mevalar = ['olma', 'banan', 'nok']
for meva in mevalar:
    print(meva)
```
👉 *Har bir meva nomini alohida qatorda chiqaradi*

## **🔹 String (Matn) bilan For Loop**
Matndagi har bir belgini ajratib olish:

```python
ism = "Python"
for harf in ism:
    print(harf)
```
👉 *P-y-t-h-o-n harflarini alohida chiqaradi*

**Amaliy misol:** Unlilarni sanash
```python
matn = "Dasturlash"
unlilar = 0
for harf in matn.lower():
    if harf in 'aeiou':
        unlilar += 1
print(f"Unlilar soni: {unlilar}")
```

## **🔹 Range() bilan For Loop**
**Oddiy range:**
```python
for i in range(5):
    print(i)  # 0 1 2 3 4
```

**Qadam bilan:**
```python
for i in range(2, 11, 2):
    print(i)  # 2 4 6 8 10
```

**Teskari hisoblash:**
```python
for i in range(5, 0, -1):
    print(i)  # 5 4 3 2 1
```

## **🔹 List (Ro'yxat) bilan For Loop**
**Oddiy ishlatilishi:**
```python
sonlar = [10, 20, 30, 40]
for son in sonlar:
    print(son * 2)  # 20 40 60 80
```

**Elementlarni o'zgartirish:**
```python
mevalar = ['olma', 'banan', 'nok']
for i in range(len(mevalar)):
    mevalar[i] = mevalar[i].upper()
print(mevalar)  # ['OLMA', 'BANAN', 'NOK']
```

## **🔹 Break va Continue**
**Break misoli:**
```python
for i in range(10):
    if i == 5:
        break
    print(i)  # 0 1 2 3 4
```

**Continue misoli:**
```python
for i in range(10):
    if i % 2 == 0:
        continue
    print(i)  # 1 3 5 7 9
```

## **🔹 Amaliy Vazifalar**

### **1. Darajalarni hisoblash**
```python
n = int(input("Son: "))
for i in range(1, 11):
    print(f"{n} ning {i}-darajasi: {n**i}")
```

### **2. So'z uzunligi**
```python
sozlar = ['python', 'dasturlash', 'algoritm']
for soz in sozlar:
    print(f"{soz} - {len(soz)} harf")
```

### **3. Teskari matn**
```python
matn = input("Matn kiriting: ")
teskari = ""
for harf in matn:
    teskari = harf + teskari
print(teskari)
```

### **4. Sonlar filtrlash**
```python
sonlar = [23, 45, 12, 67, 89, 34]
juftlar = []
for son in sonlar:
    if son % 2 == 0:
        juftlar.append(son)
print("Juft sonlar:", juftlar)
```

## **🔹 Qo'shimcha Maslahatlar**
1. Har doim o'zgaruvchilarga tushunarli nom bering
2. Kichik qismlarga bo'lib ishlang
3. print() funksiyasi bilan har qadamni tekshiring
4. Xatolarni topish uchun kodni qismma-qism ishga tushiring

**Misol:** Debug qilish
```python
mevalar = ['olma', 'banan', 'nok']
for i, meva in enumerate(mevalar):
    print(f"{i}. {meva}")  # Har bir qadamni ko'rish
```
