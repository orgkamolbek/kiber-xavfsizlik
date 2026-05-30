# 🛡️ Cyber Shield: Interactive Password Strength & Cryptanalysis Engine

Kiber-xavfsizlik qoidalari asosida parollarning murakkablik darajasini real vaqt rejimida tahlil qiluvchi (Password Strength Checker) interaktiv veb-ilova. Loyiha muntazam ifodalar (Regular Expressions) hamda shartli filtrlash algoritmlari yordamida parollarning entropiya quvvatini baholash mexanizmini namoyish etadi.

---

## 📝 Loyiha haqida

Ushbu vosita klassik kiberpank (Terminal Matrix) uslubida vizuallashtirilgan bo'lib, foydalanuvchi kiritayotgan parolni Brute-Force (barcha kombinatsiyalarni sinab ko'rish orqali buzish) hujumlariga bardoshliligini tekshiradi. Kiritilgan belgilar tarkibidagi xilma-xillikka qarab progressiv indikator rangini o'zgartiradi va taxminiy buzilish vaqtini hisoblab beradi.

---

## 📐 Kriptografik Baholash va RegEx Algoritmi (Entropy Scoring System)

Dastur parolni kiritish jarayonida har bir belgi kombinatsiyasini tekshirib, jami $100\%$ lik reyting tizimi bo'yicha quyidagi inkremental ballash zanjirini amalga oshiradi:

1. **Uzunlik nazorati:** Kamida 1 ta belgi bo'lsa $+10$ ball, uzunlik 8 tadan oshsa qo'shimcha $+20$ ball.
2. **Raqamlar mavjudligi (`/[0-9]/`):** Parolda kamida bitta raqam ishtirok etsa $+20$ ball.
3. **Registrlar balansi (`/[a-z]/` va `/[A-Z]/`):** Bir vaqtning o'zida ham kichik, ham katta harflar ishlatilsa $+20$ ball.
4. **Maxsus belgilar (`/[^A-Za-z0-9]/`):** Simvollar, nuqta yoki bo'shliq kabi alfa-raqamli bo'lmagan belgilar uchun $+30$ ball.

---

## ⚡ Asosiy xususiyatlari (Features)

* 🔍 **Real-Time RegEx Parsing:** `oninput` hodisasi orqali klaviaturadan har bir belgi bosilganda xotirani yuklamasdan lahzali parslash algoritmi.
* 📊 **Dynamic Cryptanalysis Feedback:** Ballar yig'indisiga qarab foydalanuvchiga 4 xil holat va xavfsizlik indikatorini ko'rsatish:
  * `< 30%`  ──► **JUDA ZAIF** (Qizil: `#ff4d4d`) | Hujum bardoshliligi: 1 soniya.
  * `< 60%`  ──► **O'RTA** (To'q sariq: `#ffa500`) | Hujum bardoshliligi: 2 daqiqa.
  * `< 90%`  ──► **KUCHLI** (Sariq: `#ffff00`) | Hujum bardoshliligi: 5 yil.
  * `≥ 90%`  ──► **MUKAMMAL** (Yashil: `#00ff41`) | Hujum bardoshliligi: 800+ asr.
* 🧬 **Matrix Visual Theme:** To'q fon (`#0d0d0d`), kiber-yashil neon neon nurlanishlar va monospasli shriftlar uyg'unligi.
* 🧹 **Soft Reset Engine:** Kiritish maydoni butunlay bo'shatilganda barcha ko'rsatkichlarni va ranglarni avtomatik boshlang'ich "Kutilmoqda..." holatiga qaytarish.

---

## 🛠️ Texnologiyalar (Tech Stack)

* **HTML5** — Semantik matn shakllari, maxfiy kiritish maydoni (`type="password"`) va metrik panellar.
* **CSS3 Advanced UI** — `transition: 0.5s` yordamida o'lcham va ranglarning silliq almashinishi, shaffoflik effektlari.
* **Vanilla JavaScript (ES6+)** — Regular Expressions (Muntazam ifodalar), hodisalar boshqaruvi va DOM-ning kiber-boshqaruvi.

---

## 🚀 Ishga tushirish (How to Run)

Loyiha hech qanday backend serverlari yoki tashqi ma'lumotlar bazalariga bog'lanmagan, barcha hisob-kitoblar brauzer ichida xavfsiz bajariladi:

1. Repozitoriyni kompyuterga yuklab oling:
   ```bash
   git clone [https://github.com/orgkamolbek/cyber-shield.git](https://github.com/orgkamolbek/cyber-shield.git)
