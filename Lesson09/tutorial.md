# Python: Tuple va Setlar - To'liq Qo'llanma

## Kirish

Python dasturlash tilida tuple va set muhim ma'lumotlar tuzilmalaridir. Ushbu tutorialda biz bu tuzilmalarni har tomonlama o'rganamiz, ularning afzalliklari, cheklovlari va amaliy qo'llanilishini ko'rib chiqamiz.

## 1. Tuple (O'zgarmas Ro'yxat)

Tuple - bu tartiblangan, o'zgarmas (immutable) va takrorlangan elementlarga ruxsat beruvchi ma'lumotlar strukturasi.

### 1.1 Tuple yaratish

```python
# Bo'sh tuple
empty_tuple = ()
empty_tuple = tuple()

# Elementlari bilan tuple
numbers = (1, 2, 3, 4, 5)
fruits = ('olma', 'banan', 'nok')

# Qavsiz ham yaratish mumkin
colors = 'qizil', 'yashil', 'ko'k'  # Bu ham tuple

# Bitta elementli tuple
single = (42,)  # Vergul muhim!
not_tuple = (42)  # Bu tuple emas, oddiy son
```

### 1.2 Tuple xususiyatlari

- **O'zgarmaslik (Immutable)**: Yaratilgandan keyin o'zgartirib bo'lmaydi
- **Tartiblangan**: Elementlar ketma-ketligi saqlanadi
- **Tezkor**: Listga qaraganda tezroq ishlaydi
- **Xavfsiz**: O'zgarmasligi tufayli dictionary kaliti sifatida ishlatish mumkin

### 1.3 Tuple metodlari

```python
my_tuple = (1, 2, 3, 2, 4, 2)

# count() - elementlar sonini hisoblash
print(my_tuple.count(2))  # 3

# index() - element indeksini topish
print(my_tuple.index(4))  # 4

# len() - uzunlik
print(len(my_tuple))  # 6

# max()/min() - maksimum/minimum
print(max(my_tuple))  # 4
print(min(my_tuple))  # 1
```

### 1.4 Tuple unpacking

```python
# Oddiy unpacking
coordinates = (10, 20, 30)
x, y, z = coordinates
print(x, y, z)  # 10 20 30

# * operatori bilan
values = (1, 2, 3, 4, 5)
a, b, *rest = values
print(a, b, rest)  # 1 2 [3, 4, 5]
```

## 2. Set (To'plam)

Set - bu tartiblanganmagan, unikal elementlardan tashkil topgan va o'zgartirilishi mumkin (mutable) ma'lumotlar strukturasi.

### 2.1 Set yaratish

```python
# Bo'sh set
empty_set = set()  # {} bo'sh dictionary yaratadi

# Elementlari bilan set
numbers = {1, 2, 3, 4, 5}
fruits = {'olma', 'banan', 'nok'}

# Listdan set yaratish
unique_chars = set('hello')  # {'h', 'e', 'l', 'o'}
```

### 2.2 Set operatsiyalari

```python
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}

# Birlashma (union)
print(A | B)  # {1, 2, 3, 4, 5, 6}
print(A.union(B))  # Ekvivalent

# Kesishma (intersection)
print(A & B)  # {3, 4}
print(A.intersection(B))

# Farq (difference)
print(A - B)  # {1, 2}
print(A.difference(B))

# Simmetrik farq (symmetric difference)
print(A ^ B)  # {1, 2, 5, 6}
print(A.symmetric_difference(B))
```

### 2.3 Set metodlari

```python
my_set = {1, 2, 3}

# Element qo'shish
my_set.add(4)          # {1, 2, 3, 4}
my_set.update([5, 6])  # {1, 2, 3, 4, 5, 6}

# Element o'chirish
my_set.remove(3)       # Agar element bo'lmasa KeyError
my_set.discard(10)     # Agar element bo'lmasa xatolik bermaydi
popped = my_set.pop()  # Tasodifiy elementni o'chiradi va qaytaradi

# Boshqa metodlar
my_set.clear()        # Tozalash
len(my_set)           # Elementlar soni
2 in my_set           # Tekshirish
```

## 3. Tuple va Set farqlari

| Xususiyat          | Tuple                  | Set                    |
|--------------------|------------------------|------------------------|
| Tartib             | Saqlanadi              | Saqlanmaydi            |
| Unikallik          | Takrorlanish mumkin    | Faqat unikal elementlar |
| O'zgartirish      | Immutable              | Mutable                |
| Indekslash         | Mavjud (my_tuple[0])   | Mavjud emas            |
| Tezlik (search)    | Sekin (O(n))           | Tez (O(1))             |
| Xotiradan foydalash | Samaraliroq            | Ko'proq joy egallaydi  |

## 4. Amaliy Mashqlar

### 4.1 Tuple mashqlari

**Mashq 1:** Tuple elementlarini teskari tartibda chiqaring
```python
my_tuple = (1, 2, 3, 4, 5)
# Yechim:
reversed_tuple = my_tuple[::-1]
print(reversed_tuple)  # (5, 4, 3, 2, 1)
```

**Mashq 2:** Ikkita tupleni birlashtirib, har bir element juftligini chiqaring
```python
tuple1 = ('a', 'b', 'c')
tuple2 = (1, 2, 3)
# Yechim:
combined = tuple(zip(tuple1, tuple2))
print(combined)  # (('a', 1), ('b', 2), ('c', 3))
```

**Mashq 3:** Tuple ichidagi barcha stringlarni bosh harf bilan chiqaring
```python
mixed = ('apple', 42, 'banana', 3.14, 'cherry')
# Yechim:
capitalized = tuple(x.capitalize() if isinstance(x, str) else x for x in mixed)
print(capitalized)  # ('Apple', 42, 'Banana', 3.14, 'Cherry')
```

### 4.2 Set mashqlari

**Mashq 1:** Matndagi unikal harflarni toping
```python
text = "programming"
# Yechim:
unique_chars = set(text)
print(unique_chars)  # {'p', 'r', 'o', 'g', 'a', 'm', 'i', 'n'}
```

**Mashq 2:** Ikki setda faqat bittasida bo'lgan elementlarni toping
```python
set1 = {1, 2, 3, 4, 5}
set2 = {4, 5, 6, 7, 8}
# Yechim:
unique = set1.symmetric_difference(set2)
print(unique)  # {1, 2, 3, 6, 7, 8}
```

**Mashq 3:** Listdagi barcha takrorlangan elementlarni olib tashlang
```python
numbers = [1, 2, 2, 3, 4, 4, 5, 5, 5]
# Yechim:
unique_numbers = list(set(numbers))
print(unique_numbers)  # [1, 2, 3, 4, 5] (tartib o'zgarishi mumkin)
```

### 4.3 Murakkab mashqlar

**Mashq 1:** Tuple ichidagi eng ko'p takrorlangan elementni toping
```python
my_tuple = (1, 3, 2, 3, 4, 2, 3, 5, 3, 1, 3)
# Yechim:
most_common = max(set(my_tuple), key=my_tuple.count)
print(most_common)  # 3
```

**Mashq 2:** Quyi setlarni birlashtirib, faqat barcha setlarda mavjud bo'lgan elementlarni toping
```python
sets = [{1, 2, 3}, {2, 3, 4}, {3, 4, 5}, {1, 3, 5}]
# Yechim:
common_elements = set.intersection(*sets)
print(common_elements)  # {3}
```

**Mashq 3:** Tuple va setdan foydalanib, matndagi eng ko'p ishlatilgan 3 ta harfni toping
```python
text = "Python dasturlash tili juda ham kuchli va qulay tili"
# Yechim:
# Tinish belgilarini olib tashlash
cleaned = [char.lower() for char in text if char.isalpha()]
# Har bir harfning sonini hisoblash
counts = {}
for char in set(cleaned):
    counts[char] = cleaned.count(char)
# Eng ko'p uchragan 3 ta harf
top_three = sorted(counts.items(), key=lambda x: x[1], reverse=True)[:3]
print(top_three)  # [('i', 5), ('l', 5), ('a', 4)]
```

## 5. Qo'shimcha Ma'lumotlar

### 5.1 Nusxa olish va referenslar

Tuplar immutable bo'lgani uchun ularni nusxalash oddiy:

```python
tuple1 = (1, 2, 3)
tuple2 = tuple1  # Haqiqiy nusxa
```

Setlar uchun:

```python
set1 = {1, 2, 3}
set2 = set1.copy()  # To'g'ri nusxa olish
```

### 5.2 Performance (Ishlash tezligi)

- **Tuple**: Listga qaraganda tezroq, chunki immutable
- **Set**: Element qidirish O(1) - doimiy vaqt

### 5.3 Dictionary kaliti sifatida

```python
# Tuple dictionary kaliti bo'lishi mumkin
locations = {
    (35.6895, 139.6917): "Tokyo",
    (40.7128, 74.0060): "New York"
}

# Set dictionary kaliti bo'la olmaydi (mutable)
# {set([1,2]): "value"}  # TypeError beradi
```

### 5.4 Foydali ilovalar

**Tuple uchun:**
- Funktsiyalardan bir nechta qiymat qaytarish
- Dictionary kaliti sifatida ishlatish
- O'zgarmas ma'lumotlar to'plami

**Set uchun:**
- Unikal elementlarni saqlash
- Tez qidiruv operatsiyalari
- Matematik to'plam operatsiyalari

Ushbu tutorial tuple va setlarning barcha muhim jihatlarini qamrab oldi. Amaliy mashqlarni bajaring va loyihalaringizda qo'llab, bilimingizni mustahkamlang!
