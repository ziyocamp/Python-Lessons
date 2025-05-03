# 📚 Mavzu: Python – Dictionary (Lug‘at)

---

## 🎯 Dars maqsadi:

* O‘quvchilar `dictionary` nima ekanligini tushunadi.
* Ular dictionary yaratish, o‘zgartirish, o‘qish va o‘chirishni o‘rganadi.
* Amaliy misollar orqali mustahkamlaydi.

---

## 🧠 1-bosqich: Tushuncha

### ❓ Dictionary nima?

> Python'da dictionary bu: **kalit (key)** va **qiymat (value)** juftligi orqali ma'lumotlarni saqlaydigan tuzilma.

👨‍🏫 Hayotiy misol:
Daftarimda do‘stlarimning ismlari va telefon raqamlari bor:

```python
contacts = {
    "Ali": "+998901234567",
    "Laylo": "+998935551212"
}
```

### ✅ Qoidalar:

* Har bir kalit yagona bo'lishi kerak
* Kalitlar odatda `string`, qiymatlar esa `string`, `int`, `bool`, `list`, yoki hatto boshqa `dictionary` bo‘lishi mumkin

---

## 💻 2-bosqich: Amaliy kodlar

### 📌 Dictionary yaratish:

```python
student = {
    "name": "Ali",
    "age": 18,
    "is_student": True
}
```

### 📌 Ma'lumot olish:

```python
print(student["name"])       # Ali
print(student.get("age"))    # 18
```

### 📌 Yangi element qo‘shish:

```python
student["grade"] = "A"
```

### 📌 Elementni o‘zgartirish:

```python
student["age"] = 19
```

### 📌 Elementni o‘chirish:

```python
del student["grade"]
```

Yoki:

```python
student.pop("is_student")
```

### 📌 Barcha elementlarni ko‘rish:

```python
for key, value in student.items():
    print(key, ":", value)
```

---

## 🏋️‍♂️ 3-bosqich: Mustahkamlovchi mashqlar

O‘quvchilarga topshiriq sifatida:

> Quyidagi amallarni bajaring:

1. `book` nomli dictionary yarating va quyidagi ma’lumotlarni yozing: `title`, `author`, `year`.
2. `year` qiymatini 1 yilga yangilang.
3. `pages` nomli yangi kalit qo‘shing.
4. `author`ni `pop()` yordamida olib tashlang.
5. `for` yordamida barcha kalit va qiymatlarni ekranga chiqaring.

---

## 📝 Uyga vazifa (ajoyib mustahkamlash uchun):

> Quyidagi dictionary ustida ish bajaring:

```python
user = {
    "username": "diyorbek01",
    "email": "diyor@gmail.com",
    "password": "abc123"
}
```

1. `email` qiymatini yangilang.
2. Yangi kalit `is_active = True` ni qo‘shing.
3. `username` kalitini `get()` yordamida o‘qing.
4. Barcha elementlarni `for` yordamida ekranga chiqaring.
