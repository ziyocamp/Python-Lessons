# **For Loop bo'yicha uyga vazifalar**

## **Asosiy vazifalar**

### **1. Sonlar oralig'ini chiqarish**
```python
"""
1. Foydalanuvchi kiritgan a va b sonlari orasidagi 
   barcha sonlarni chiqaring (a va b ni ham)
"""
```

### **2. Karra jadvali**
```python
"""
2. Foydalanuvchi kiritgan son (1-9 oralig'ida) 
   uchun karra jadvalini chiqaring. Misol uchun:
   5 x 1 = 5
   5 x 2 = 10
   ...
   5 x 10 = 50
"""
```

### **3. Matn tahlili**
```python
"""
3. Foydalanuvchi kiritgan matnda nechta katta harf 
   va nechta kichik harf borligini hisoblang
"""
```

## **O'rta darajali vazifalar**

### **4. Tub sonlarni topish**
```python
"""
4. Foydalanuvchi kiritgan N sonigacha bo'lgan 
   barcha tub sonlarni toping va chiqaring
"""
```

### **5. So'zlarni teskari chiqarish**
```python
"""
5. Foydalanuvchi kiritgan gapdagi har bir so'zni 
   teskari tartibda chiqaring. Misol uchun:
   "Python is great" -> "nohtyP si taerg"
"""
```

### **6. Password generator**
```python
"""
6. Foydalanuvchi kiritgan uzunlikda tasodifiy 
   parol yaratadigan dastur tuzing (harflar va 
   raqamlardan iborat bo'lsin)
"""
```

## **Murakkab vazifalar**

### **7. Fibonacci ketma-ketligi**
```python
"""
7. Foydalanuvchi kiritgan N sonigacha bo'lgan 
   Fibonachchi ketma-ketligini chiqaring
   0, 1, 1, 2, 3, 5, 8...
"""
```

### **8. To'plamlarni solishtirish**
```python
"""
8. Ikki ro'yxat kiritilganda, ularning:
   - Umumiy elementlarini
   - Farq qiladigan elementlarini chiqaring
"""
```

### **9. Matn shifrlash**
```python
"""
9. Foydalanuvchi kiritgan matnni shifrlang:
   - Har bir harf alifboda keyingi harf bilan almashtirilsin
   - 'z' dan keyin 'a' keladi
   - Masalan: "python" -> "qzuipo"
"""
```

## **Qo'shimcha masalalar**

### **10. Mukammal sonlar**
```python
"""
10. Foydalanuvchi kiritgan N sonigacha bo'lgan 
    barcha mukammal sonlarni toping (o'zidan 
    boshqa bo'luvchilari yig'indisi o'ziga teng 
    bo'lgan sonlar)
"""
```

### **11. Kalkulyator**
```python
"""
11. Foydalanuvchi kiritgan ikkita son va amal 
    (+, -, *, /) bo'yicha hisoblovchi dastur tuzing. 
    Har bir amal for loop orqali bajarilsin.
"""
```

### **12. Yulduzchalar bilan chizish**
```python
"""
12. Foydalanuvchi kiritgan son bo'yicha 
    yulduzchalar (*) bilan uchburchak chizing.
    Masalan (3 uchun):
    *
    **
    ***
"""
```

## **Vazifalarni bajarish uchun maslahatlar**

1. Har bir vazifani alohida Python faylida bajaring
2. Kodlaringizga izohlar qo'shing (# belgisi bilan)
3. print() yordamida har bir qadamni tekshiring
4. Xatolarga yo'l qo'ymaslik uchun foydalanuvchi kiritimini tekshiring
5. Murakkab vazifalarni kichik qismlarga bo'lib bajaring

**Misol yechim (1-vazifa uchun):**
```python
a = int(input("Birinchi son: "))
b = int(input("Ikkinchi son: "))

for i in range(a, b+1):
    print(i, end=" ")
```

**Misol yechim (5-vazifa uchun):**
```python
gap = input("Gap kiriting: ")
for soz in gap.split():
    print(soz[::-1], end=" ")
```
