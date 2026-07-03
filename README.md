# llm-code-packer 🌲🚀

**llm-code-packer** هو أداة ذكية وخفيفة الوزن بواجهة رسومية (GUI) مبنية بالكامل باستخدام PowerShell. تهدف الأداة إلى تسهيل حياة المطورين عند التعامل مع نماذج الذكاء الاصطناعي (مثل ChatGPT, Claude, DeepSeek) من خلال توليد خريطة هيكلية كاملة للمشروع (Project Tree) ودمج ملفات برمجية محددة في ملف نصي واحد منظم ومنسق بدقة لتوفير السياق الكامل (Context) للـ LLM بدون تشتيت.

A smart, lightweight PowerShell GUI tool designed to pack your source code and generate a full project structure tree into a single optimized text file, providing the perfect context for LLMs (like ChatGPT, Claude, DeepSeek) without hitting token limits.

---

## ✨ المميزات / Features

* **خريطة المشروع كاملة (Full Project Tree):** يولد شجرة مجلدات وملفات تفصيلية للموقع بالكامل ليفهم الذكاء الاصطناعي العلاقات والـ Imports بدقة.
* **إضافة تراكمية للملفات (Multi-Folder Selection):** يمكنك التنقل بين مجلدات مختلفة واختيار ملفات من مسارات متعددة لتضاف إلى القائمة دون أن تمسح الاختيارات السابقة.
* **إدارة مرنة للقائمة (List Management):** إمكانية تحديد أي ملف زائد والضغط على زر `Delete` في لوحة المفاتيح لحذفه فوراً من القائمة.
* **تخطي المجلدات الضخمة تلقائياً (Smart Exclusion):** يتم استبعاد مجلدات مثل `node_modules` و `.git` برمجياً لتسريع العملية وحفظ مساحة الذاكرة (Tokens).
* **تسمية مخصصة (Custom Naming):** إمكانية اختيار اسم الملف النصي الناتج في كل مرة قبل التجميع.
* **حزمة مستقلة (Portable EXE):** واجهة رسومية أنيقة بأيقونة مخصصة تعمل كملف `.exe` مستقل بضغطة زر واحدة.

---

## 🚀 طريقة الاستخدام / How to Use

1. **الخطوة الأولى / Step 1:** اضغط على زر اختيار مجلد المشروع الرئيسي (مثال: مجلد `src`) لتوليد الخريطة الهيكلية الكاملة.
2. **الخطوة الثانية / Step 2:** اضغط على زر إضافة الملفات المحددة التي تعمل عليها وتريد حل مشكلة بها أو إضافة ميزة لها لدمج أكوادها الفعلية.
3. **الخطوة الثالثة / Step 3:** اكتب الاسم الذي تفضله للملف الناتج، ثم اضغط على زر **"تجميع الأكواد وتوليد الشجرة الكاملة للموقع 🚀"**.
4. **الخطوة الرابعة / Step 4:** اسحب الملف الناتج وانقله مباشرة إلى شات الذكاء الاصطناعي (LLM) مع البرومبت الخاص بك.

---

## 🛠️ المتطلبات والتشغيل للمطورين / Requirements for Developers

إذا كنت ترغب في تشغيل الكود المصدري مباشرة عبر سكريبت PowerShell:

```powershell
# لتشغيل السكريبت لأول مرة قد تحتاج لتفعيل صلاحيات تشغيل السكريبتات في جهازك:
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser

# ثم قم بتشغيل السكريبت:
.\files.ps1
```

### تحويل السكريبت إلى ملف EXE مستقل:
نقوم باستخدام مكتبة `ps2exe` لبناء الملف التنفيذي بدون شاشة الكونسول السوداء ومع إضافة الأيقونة وحقوق الملكية:
```powershell
ps2exe -inputFile .\files.ps1 -outputFile .\BundlerTool.exe -noConsole -icon .\app.ico -title "LLM Code Packer" -description "Pack code files with a full project tree for LLM context" -version "1.0.0"
```

---

## 🧑‍💻 المطور / Developer
* **Name:** [اكتب اسمك هنا]
* **Email:** [اكتب إيميلك هنا]

---
⭐ إذا أعجبتك الأداة وساعدتك في عملك اليومي مع الذكاء الاصطناعي، لا تبخل علينا بوضع **Star** للمستودع!  
⭐ If you find this tool helpful for your daily AI workflows, please consider giving this repository a **Star**!
