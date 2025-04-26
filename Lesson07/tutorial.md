# Non-Primitive Ma'lumot Turlari - Ro'yxatlar (Lists)

## Kirish

Python dasturlash tilida ma'lumot turlari ikkita asosiy toifaga bo'linadi:
1. **Primitive (Oddiy) Ma'lumot Turlari**
2. **Non-Primitive (Murakkab) Ma'lumot Turlari**

## Primitive va Non-Primitive Farqlari

### Primitive Ma'lumot Turlari:
- **Integer (int)** - butun sonlar (10, -5, 0)
- **Float (float)** - kasr sonlar (3.14, -0.001)
- **Boolean (bool)** - mantiqiy qiymatlar (True, False)
- **String (str)** - matnlar ("salom", 'dunyo')
- **NoneType** - qiymat yo'qligi (None)

**Xususiyatlari:**
- O'zgarmas (immutable) - yaratilgandan keyin o'zgartirib bo'lmaydi
- Oddiy strukturalar
- Xotirada kamroq joy egallaydi

### Non-Primitive Ma'lumot Turlari:
- **List (ro'yxat)** - [1, 2, 3]
- **Tuple (kortej)** - (1, 2, 3)
- **Set (to'plam)** - {1, 2, 3}
- **Dictionary (lug'at)** - {"nomi": "Ali", "yosh": 25}

**Xususiyatlari:**
- O'zgaruvchan (mutable) - yaratilgandan keyin o'zgartirish mumkin
- Murakkab strukturalar
- Bir nechta qiymatlarni saqlaydi
- Xotirada ko'proq joy egallaydi
- Metodlar va funksiyalar bilan boy

## **📌 Ro'yxat (List) nima?**
Ro'yxat - bu bir nechta elementlarni tartiblangan shaklda saqlash uchun ishlatiladigan **o'zgaruvchan (mutable)** ma'lumot turi.

**Namuna:**
```python
mevalar = ['olma', 'banan', 'nok']
sonlar = [1, 2, 3, 4, 5]
aralash = [10, 'olma', True, 3.14]
```

---

## **📌 Ro'yxat Yaratish Usullari**
1. **To'g'ridan-to'g'ri yozish**
   ```python
   mevalar = ['olma', 'banan', 'nok']
   ```

2. **`list()` konstruktori orqali**
   ```python
   sonlar = list(range(1, 6))  # [1, 2, 3, 4, 5]
   ```

3. **Bo'sh ro'yxat**
   ```python
   boshlangich = []
   ```

---

## **📌 Ro'yxat Elementlariga Murojat**
```python
fruits = ['apple', 'banana', 'cherry', 'date']

# Indeks orqali (0 dan boshlanadi)
print(fruits[0])   # 'apple'
print(fruits[2])   # 'cherry'
print(fruits[-1])  # 'date' (oxirgi element)

# Qismlarga bo'lish (slicing)
print(fruits[1:3])  # ['banana', 'cherry']
print(fruits[:2])   # ['apple', 'banana']
print(fruits[2:])   # ['cherry', 'date']
```

---

## **📌 Ro'yxat Metodlari**

### **1. Element Qo'shish**
| **Metod**       | **Tavsif**                          | **Misol**                          |
|----------------|------------------------------------|------------------------------------|
| `.append(x)`   | Ro'yxat oxiriga `x` qo'shadi       | `mevalar.append("olma")`           |
| `.insert(i,x)` | `i`-indeksga `x` qo'shadi          | `mevalar.insert(1, "banan")`       |

**Namuna:**
```python
mevalar = ['olma', 'nok']
mevalar.append('banan')    # ['olma', 'nok', 'banan']
mevalar.insert(1, 'uzum')  # ['olma', 'uzum', 'nok', 'banan']
```

### **2. Element O'chirish**
| **Metod**       | **Tavsif**                          | **Misol**                          |
|----------------|------------------------------------|------------------------------------|
| `.remove(x)`   | Birinchi uchragan `x` ni o'chiradi  | `mevalar.remove("nok")`            |
| `.pop(i)`      | `i`-indeksdagi elementni o'chiradi | `mevalar.pop(2)`                   |
| `.clear()`     | Ro'yxatni tozalaydi                | `mevalar.clear()`                  |

**Namuna:**
```python
mevalar = ['olma', 'banan', 'nok', 'uzum']
mevalar.remove('banan')  # ['olma', 'nok', 'uzum']
mevalar.pop(1)           # ['olma', 'uzum']
mevalar.clear()          # []
```

### **3. Ro'yxatni Tartiblash**
| **Metod**       | **Tavsif**                          | **Misol**                          |
|----------------|------------------------------------|------------------------------------|
| `.sort()`      | Ro'yxatni tartiblaydi              | `sonlar.sort()`                    |
| `.reverse()`   | Ro'yxatni teskari aylantiradi      | `sonlar.reverse()`                 |

**Namuna:**
```python
sonlar = [3, 1, 4, 2]
sonlar.sort()     # [1, 2, 3, 4]
sonlar.reverse()  # [4, 3, 2, 1]
```

### **4. Boshqa Muhim Metodlar**
| **Metod**       | **Tavsif**                          | **Misol**                          |
|----------------|------------------------------------|------------------------------------|
| `.index(x)`    | `x` elementining indeksini topadi  | `mevalar.index("olma")`            |
| `.count(x)`    | `x` necha marta takrorlanganini sanaydi | `mevalar.count("olma")`     |
| `.copy()`      | Ro'yxatning nusxasini yaratadi     | `yangi_list = eski_list.copy()`    |

**Namuna:**
```python
mevalar = ['olma', 'banan', 'olma']
print(mevalar.index('banan'))  # 1
print(mevalar.count('olma'))   # 2
```

---

## **📌 Ro'yxatlar bilan Amallar**
### **1. Ro'yxatlarni Birlashtirish (+ operatori)**
```python
list1 = [1, 2]
list2 = [3, 4]
combined = list1 + list2  # [1, 2, 3, 4]
```

### **2. Ro'yxatni Takrorlash (* operatori)**
```python
numbers = [1, 2] * 3  # [1, 2, 1, 2, 1, 2]
```

### **3. Element Mavjudligini Tekshirish (in operatori)**
```python
mevalar = ['olma', 'banan']
print('olma' in mevalar)    # True
print('nok' not in mevalar) # True
```

---

## **📌 Amaliy Misollar**
### **1. Ro'yxat yaratish va element qo'shish**
```python
telefonlar = ['iPhone', 'Samsung']
telefonlar.append('Xiaomi')      # ['iPhone', 'Samsung', 'Xiaomi']
telefonlar.insert(1, 'Huawei')  # ['iPhone', 'Huawei', 'Samsung', 'Xiaomi']
```

### **2. Elementlarni o'chirish**
```python
telefonlar = ['iPhone', 'Huawei', 'Samsung', 'Xiaomi']
telefonlar.remove('Huawei')  # ['iPhone', 'Samsung', 'Xiaomi']
telefonlar.pop(1)            # ['iPhone', 'Xiaomi']
```

### **3. Ro'yxatni saralash**
```python
ballar = [85, 92, 78, 90]
ballar.sort()      # [78, 85, 90, 92]
ballar.reverse()   # [92, 90, 85, 78]
```

---

## **📌 Xatoliklar va Echimlari**
```python
mevalar = ['olma', 'banan']

# ❌ Noto'g'ri indeks
# print(mevalar[5])  # IndexError
# ✅ To'g'ri usul
print(mevalar[-1])  # 'banan'

# ❌ Mavjud bo'lmagan element
# mevalar.remove('nok')  # ValueError
# ✅ Avval tekshirish
if 'nok' in mevalar:
    mevalar.remove('nok')
```

---

## **📌 Yakuniy Mashqlar**
1. **`sonlar = [5, 2, 9, 1]` ro'yxati uchun:**
   - **`.sort()` bilan tartiblang**
   - **`.append(10)` bilan yangi son qo'shing**
   - **`.count(5)` bilan 5 soni necha marta kelganini toping**

2. **`mevalar = ['olma', 'banan', 'nok']` ro'yxati uchun:**
   - **`.insert(1, 'uzum')` bilan yangi meva qo'shing**
   - **`.pop()` bilan oxirgi mevani o'chiring**
   - **`'banan' in mevalar` tekshiring**

---

### **Javoblar:**
```python
# 1-misol
sonlar = [5, 2, 9, 1]
sonlar.sort()         # [1, 2, 5, 9]
sonlar.append(10)     # [1, 2, 5, 9, 10]
print(sonlar.count(5)) # 1

# 2-misol
mevalar = ['olma', 'banan', 'nok']
mevalar.insert(1, 'uzum')  # ['olma', 'uzum', 'banan', 'nok']
mevalar.pop()              # ['olma', 'uzum', 'banan']
print('banan' in mevalar)   # True
```
