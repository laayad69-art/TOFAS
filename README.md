# 🎓 TOFAS Exam System

> نظام اختبار تفاعلي لمادة JavaScript مع ترتيب تنافسي وتخزين لحظي للنتائج

---

## 📌 Overview

**TOFAS Exam System** هو نظام اختبار متكامل مصمم لتقديم تجربة تقييم واقعية للطلاب، مع دعم التفاعل الكامل، ترتيب المتصدرين، وإرسال النتائج بشكل تلقائي.

تم تطوير المشروع خصيصًا لطلاب  
**مدرسة علاء زكي زكي الثانوية المشتركة - أم رماد**

---

## 🚀 Live Demo

🔗 https://chapter-chat-9690e.web.app

---

## 🛠️ Tech Stack

| التقنية | الاستخدام |
|--------|----------|
| HTML5 | هيكل الصفحات |
| CSS3 | تصميم متجاوب |
| JavaScript (ES6) | منطق التطبيق |
| Firebase Realtime DB | تخزين البيانات |
| Telegram Bot API | إرسال النتائج |

---

## ✨ Features

### 👨‍🎓 Student Features
- ✅ 20 سؤال JavaScript (أكواد حقيقية)
- ✅ ترتيب عشوائي للأسئلة في كل محاولة
- ✅ مؤقت 40 دقيقة
- ✅ نظام تأكيد الإجابة (لا يمكن التعديل)
- ✅ تنقل سلس بين الأسئلة
- ✅ عرض النتيجة بشكل فوري
- ✅ صفحة Leaderboard

---

### ⚙️ System Features
- 🔥 تخزين لحظي باستخدام Firebase
- 🤖 إرسال تلقائي إلى Telegram
- 🏆 نظام ترتيب تنافسي
- 🔒 مركز أول مقفل (Admin Protected)
- 📱 Responsive على جميع الأجهزة

---

## 🧠 How It Works

```mermaid
graph TD
A[Enter Name] --> B[Start Exam]
B --> C[Answer Questions]
C --> D[Submit Exam]
D --> E[Calculate Score]
E --> F[Save to Firebase]
F --> G[Send to Telegram]
G --> H[Show Result & Leaderboard]


---

📁 Database Structure

/all_results
[
  {
    "id": "1734567890123",
    "name": "Ahmed",
    "score": 18,
    "total": 20,
    "percentage": 90,
    "date": "2026-03-26T10:30:00Z",
    "duration": "35:22"
  }
]


---

🔐 Firebase Rules

{
  "rules": {
    ".read": true,
    ".write": true,
    "all_results": {
      ".indexOn": ["percentage", "score", "date"]
    }
  }
}


---

🤖 Telegram Integration

const botToken = "YOUR_BOT_TOKEN";
const chatId = "YOUR_CHAT_ID";

📩 Example Message

✅ اختبار توفاس
👤 أحمد
📊 18/20
📈 90%
⏱️ 35:22


---

⚙️ Configuration

تغيير عدد الأسئلة

shuffled.slice(0, 20);

تغيير مدة الاختبار

let timeSeconds = 40 * 60;

إضافة سؤال

{
  code: `console.log(typeof 42);`,
  question: "ما الناتج؟",
  options: ["number", "string", "object", "undefined"],
  correct: 0,
  difficulty: 1
}


---

📱 Compatibility

✅ Chrome

✅ Firefox

✅ Safari

✅ Edge

✅ Mobile Browsers



---

🐛 Troubleshooting

Firebase لا يعمل

تأكد من firebaseConfig


Telegram لا يرسل

تأكد من botToken و chatId


الأسئلة لا تظهر

console.log(MASTER_QUESTIONS.length);


---

👨‍💻 Author

Eyad Alaa (ZMAX)
📧 laayad69@gmail.com


---

📄 License

© 2026 ZMAX - All Rights Reserved
