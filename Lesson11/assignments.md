## 🧑‍💼 1. Ishchilar boshqaruv dasturi (Employee Management Console App)

**Loyiha tavsifi:**
Foydalanuvchi konsol orqali ishchilar ro‘yxatini yaratishi, ko‘rishi, o‘zgartirishi va o‘chirishi mumkin bo‘lgan kichik CRUD tizimi.

**Talab qilinadigan tushunchalar:**
`list`, `dict`, `for loop`, `if-else`, `input()`, CRUD (Create, Read, Update, Delete)

**Topshiriq shartlari:**

* Har bir ishchi haqida quyidagilar saqlanadi:

  ```python
  {
    "id": 1,
    "ism": "Ali",
    "lavozim": "Dasturchi",
    "oylik": 5000000
  }
  ```
* Barcha ishchilar `list` ko‘rinishida saqlanadi.
* Konsolda menyu ko‘rsatiladi:

  ```
  1. Ishchi qo‘shish
  2. Ishchilar ro‘yxati
  3. Oylikni o‘zgartirish (ID bo‘yicha)
  4. Ishchini o‘chirish (ID bo‘yicha)
  5. O‘rtacha oylikni hisoblash
  0. Chiqish
  ```

**Qo‘shimcha g‘oyalar (Bonus):**

* `id` avtomatik tarzda oshib boradigan qilib yozing.
* Foydalanuvchidan tasdiqlov olish (haqiqatdan o‘chirishni xohlaysizmi?).

---

## 🛒 2. Mahsulotlar savatchasi (Shopping Cart System)

**Loyiha tavsifi:**
Foydalanuvchi mahsulotlarni tanlab savatchaga joylaydi va oxirida umumiy narx hisoblanadi.

**Tushunchalar:**
`dict`, `list`, `while loop`, `input()`, `if-else`

**Topshiriq shartlari:**

* Mahsulotlar `dict` ko‘rinishida berilgan:

  ```python
  products = {
      "non": 5000,
      "sut": 8000,
      "gosht": 60000,
      "pishloq": 30000
  }
  ```
* Foydalanuvchi mahsulot nomlarini kiritadi, har biri `cart` degan ro‘yxatga qo‘shiladi.
* `checkout` so‘zi kiritilgach, quyidagilar chiqadi:

  * Har bir mahsulot nomi
  * Jami narx

**Qo‘shimcha g‘oyalar:**

* Mahsulot sonini ham so‘rash (`quantity`)
* Chek ko‘rinishida chiqarish (mahsulot, soni, narxi, jami)

---

## 📚 3. Kitoblar katalogi (Book Catalog)

**Loyiha tavsifi:**
Kitoblar ro‘yxatini yuritish, yangi kitob qo‘shish va qidiruv amalga oshirish.

**Tushunchalar:**
`list of dicts`, `for loop`, `filter`, `input()`

**Topshiriq shartlari:**

* Har bir kitob quyidagicha ko‘rinishda saqlanadi:

  ```python
  {
      "sarlavha": "Ufq",
      "muallif": "Said Ahmad",
      "yil": 1980,
      "janr": "Tarixiy"
  }
  ```
* Quyidagi funksiyalar mavjud bo‘lishi kerak:

  * Yangi kitob qo‘shish
  * Barcha kitoblarni ko‘rish
  * Muallif bo‘yicha qidirish
  * Yil bo‘yicha filter qilish

**Qo‘shimcha g‘oyalar:**

* Har bir kitobga `id` berish
* Kitobni o‘zgartirish yoki o‘chirish imkoniyati

---

## ✅ 4. To-do ro‘yxati (To-do App)

**Loyiha tavsifi:**
Foydalanuvchi o‘z vazifalarini yozadi, belgilaydi va boshqaradi.

**Tushunchalar:**
`list`, `dict`, `loop`, `status`, `input()`

**Topshiriq shartlari:**

* Har bir `task` quyidagicha bo‘ladi:

  ```python
  {
      "id": 1,
      "matn": "Darsga tayyorlanish",
      "status": "pending"  # yoki "done"
  }
  ```
* Amal menyusi:

  1. Task qo‘shish
  2. Barcha tasklarni ko‘rish
  3. ID bo‘yicha bajarilgan deb belgilash
  4. `done` va `pending` tasklarni ajratib ko‘rsatish
  5. Taskni o‘chirish
  6. Chiqish

**Qo‘shimcha g‘oyalar:**

* Har bir ishga `deadline` qo‘shish
* Statusni faqat `"done"` yoki `"pending"` deb tekshirish

---

## 💰 5. Bank tizimi (Simple Bank System)

**Loyiha tavsifi:**
Foydalanuvchi mijozlar bilan ishlaydigan oddiy bank tizimini boshqaradi.

**Tushunchalar:**
`list`, `dict`, `input()`, `balance`, `loop`, `if`

**Topshiriq shartlari:**

* Har bir mijoz haqida saqlang:

  ```python
  {
      "id": 1,
      "ism": "Aziz",
      "balans": 2500000
  }
  ```
* Amal menyusi:

  1. Mijoz qo‘shish
  2. Balans ko‘rish (ID bo‘yicha)
  3. Pul qo‘shish (deposit)
  4. Pul yechish (withdraw)
  5. Eng boy mijozni ko‘rsatish

**Qo‘shimcha g‘oyalar:**

* Balans manfiy bo‘lib qolmasin (tekshiruv)
* Pul o‘tkazish funksiyasi (bir mijozdan boshqasiga)

---

## 📊 6. So‘rovnoma statistikasi (Survey App)

**Loyiha tavsifi:**
Foydalanuvchilardan so‘rovnoma olib, natijalarni statistik tahlil qiladi.

**Tushunchalar:**
`list`, `dict`, `counter`, `loop`, `input()`

**Topshiriq shartlari:**

* Foydalanuvchiga savol beriladi:
  **“Python sizga yoqdimi?”**
  Javob: `yes` yoki `no`
* Har bir javob `dict` ichida saqlanadi: `{"user": "Ali", "answer": "yes"}`
* Tugagach quyidagilar chiqadi:

  * Umumiy ishtirokchilar soni
  * `yes` va `no` foizlarda
  * `yes` javoblari ko‘pchilikda bo‘lsa, "Ko‘pchilikka yoqdi" degan xulosa

