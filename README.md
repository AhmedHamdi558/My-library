# مكتبتي - دليل الاستخدام

## هيكل المشروع

```
/
├── index.html
└── Files/
    ├── engine.json          ← قاعدة بيانات الكتب
    ├── Images/              ← صور الأغلفة
    │   ├── كتابي.jpg
    │   └── ...
    ├── Texts/               ← ملفات الوصف
    │   ├── كتابي.txt
    │   └── ...
    └── *.pdf                ← ملفات الكتب
        ├── كتابي.pdf
        └── ...
```

---

## كيفية إضافة كتاب

### 1. ارفع الملفات
- الـ PDF في مجلد `Files/`
- صورة الغلاف في `Files/Images/`
- ملف الوصف (نص عادي) في `Files/Texts/`

### 2. عدّل engine.json
أضف كائناً جديداً للمصفوفة:

```json
{
  "title": "اسم الكتاب",
  "category": "رواية",
  "image": "Files/Images/اسم-الكتاب.jpg",
  "descFile": "Files/Texts/اسم-الكتاب.txt",
  "pdf": "Files/اسم-الكتاب.pdf",
  "color": "#3a1020"
}
```

**ملاحظات:**
- `image` اختياري - إذا حذفته سيظهر غلاف ملون تلقائياً
- `color` اختياري - لون خلفية الغلاف البديل
- الأصناف المتاحة: رواية، قصة، شعر، مقالات، أخرى (أو أي صنف تريده)

---

## رفع الموقع على GitHub Pages

```bash
# 1. أنشئ مستودعاً جديداً على GitHub

# 2. ارفع الملفات
git init
git add .
git commit -m "أول رفع"
git remote add origin https://github.com/USERNAME/REPO.git
git push -u origin main

# 3. فعّل GitHub Pages
# Settings → Pages → Branch: main → / (root) → Save
```

رابط موقعك سيكون: `https://USERNAME.github.io/REPO`

---

## مثال على engine.json

```json
[
  {
    "title": "رواية الظل الأخير",
    "category": "رواية",
    "image": "Files/Images/الظل-الأخير.jpg",
    "descFile": "Files/Texts/الظل-الأخير.txt",
    "pdf": "Files/الظل-الأخير.pdf",
    "color": "#4a1a10"
  },
  {
    "title": "قصيدة المساء",
    "category": "شعر",
    "descFile": "Files/Texts/قصيدة-المساء.txt",
    "pdf": "Files/قصيدة-المساء.pdf",
    "color": "#1a2040"
  }
]
```
