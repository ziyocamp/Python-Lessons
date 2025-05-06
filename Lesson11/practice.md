
## 🎯 10 ta real hayotga oid `list[dict]` bilan bog‘liq Python mashqlari

### 1. 🎬 Kinoni nomi bo‘yicha qidirish

```python
movies = [
    {"title": "Inception", "year": 2010},
    {"title": "The Matrix", "year": 1999},
    {"title": "Interstellar", "year": 2014},
]

search = input("Qaysi kinoni qidiryapsiz? ").lower()

for movie in movies:
    if search in movie["title"].lower():
        print(f"Topildi: {movie['title']} ({movie['year']})")
```

---

### 2. 🛒 Mahsulotlarni narxi bo‘yicha filterlash

```python
products = [
    {"name": "Laptop", "price": 450},
    {"name": "Mouse", "price": 20},
    {"name": "Monitor", "price": 200},
]

limit = int(input("Eng yuqori narxni kiriting: "))

for product in products:
    if product["price"] <= limit:
        print(product["name"], "-", product["price"])
```

---

### 3. 👩‍🎓 Talabalarni bahosi bo‘yicha ajratish

```python
students = [
    {"name": "Ali", "score": 85},
    {"name": "Laylo", "score": 92},
    {"name": "Hasan", "score": 68},
]

for student in students:
    if student["score"] >= 90:
        print(f"{student['name']} - A baho")
    elif student["score"] >= 70:
        print(f"{student['name']} - B baho")
    else:
        print(f"{student['name']} - C baho")
```

---

### 4. 📚 Kitoblarni muallif bo‘yicha filterlash

```python
books = [
    {"title": "Python 101", "author": "Alison"},
    {"title": "C Guide", "author": "Brian"},
    {"title": "Web Dev", "author": "Alison"},
]

author = input("Muallif ismini kiriting: ")

for book in books:
    if book["author"] == author:
        print(book["title"])
```

---

### 5. 🧍 Yoshi eng katta odamni topish

```python
people = [
    {"name": "Aziz", "age": 23},
    {"name": "Malika", "age": 31},
    {"name": "Karim", "age": 28},
]

max_person = people[0]
for person in people:
    if person["age"] > max_person["age"]:
        max_person = person

print("Yoshi eng katta:", max_person["name"], "-", max_person["age"])
```

---

### 6. 🛍 Mahsulotlar narxining o‘rtacha qiymatini hisoblash

```python
products = [
    {"name": "Phone", "price": 500},
    {"name": "Tablet", "price": 300},
    {"name": "Headphones", "price": 150},
]

total = 0
for product in products:
    total += product["price"]

avg = total / len(products)
print("O‘rtacha narx:", avg)
```

---

### 7. 🕒 Filmlarni yil bo‘yicha saralash (2000 yildan keyingi)

```python
movies = [
    {"title": "Titanic", "year": 1997},
    {"title": "Avatar", "year": 2009},
    {"title": "Tenet", "year": 2020},
]

for movie in movies:
    if movie["year"] >= 2000:
        print(movie["title"], "-", movie["year"])
```

---

### 8. 📋 Ro‘yxatdagi eng arzon mahsulotni topish

```python
products = [
    {"name": "Keyboard", "price": 25},
    {"name": "Mouse", "price": 10},
    {"name": "USB", "price": 5},
]

cheapest = products[0]
for product in products:
    if product["price"] < cheapest["price"]:
        cheapest = product

print("Eng arzon mahsulot:", cheapest["name"], "-", cheapest["price"])
```

---

### 9. 🏷 Har bir mahsulotga soliq qo‘shib yangi ro‘yxat yaratish

```python
products = [
    {"name": "TV", "price": 600},
    {"name": "Speaker", "price": 150},
]

new_products = []
for product in products:
    new_price = round(product["price"] * 1.15, 2)
    new_products.append({"name": product["name"], "price_with_tax": new_price})

print(new_products)
```

---

### 10. 📦 Ombordagi mahsulotlar sonini umumlashtirish

```python
items = [
    {"name": "Chair", "qty": 10},
    {"name": "Table", "qty": 5},
    {"name": "Chair", "qty": 3},
]

summary = {}

for item in items:
    name = item["name"]
    if name in summary:
        summary[name] += item["qty"]
    else:
        summary[name] = item["qty"]

print(summary)
```

