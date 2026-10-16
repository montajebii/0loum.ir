# Library Auto-Generation Workflow

سیستم خودکار برای تولید و بروزرسانی فایل `library.json` بر اساس فایل‌های درون پوشه `downloads/`

**Isolated Components:**

- `toggleBtn`, `panel`, `closeBtn` in `assets/JS/main.js` are UI elements used for toggling and managing content visibility. These components are isolated and lack detailed documentation. For more information, see `assets/JS/main.js`.

## نحوه کار

**Isolated Components:**

- `toggleBtn`, `panel`, `closeBtn` in `assets/JS/main.js` are UI components for toggling and managing content. These components are isolated and lack detailed documentation. For more information, see `assets/JS/main.js`.

### 1. **Workflow خودکار (GitHub Actions)**

هر بار که کدی به شاخه `main` push شود:

- اسکریپت `generate-library.js` خودکار اجرا می‌شود
- پوشه `downloads/` اسکن شده و تمام فایل PDF ها شناسایی می‌شوند
- فایل `library.json` خودکار بروزرسانی می‌شود
- تغییرات خودکار commit و push می‌شوند
- سپس deploy به GitHub Pages انجام می‌شود

### 2. **اجرای دستی**

اگر بخواهید library.json را دستی بروزرسانی کنید:

```bash
npm run generate-library
```

یا اگر Node.js را نصب ندارید:

```bash
node scripts/generate-library.js
```

## ساختار پوشه downloads/

```
assets/downloads/
├── 7/          (پایه هفتم)
│   ├── 1/      (فصل 1)
│   │   ├── کاربرگ علوم هفتم فصل (1).pdf
│   │   └── روبیک جامع هفتم - فصل (1).pdf
│   ├── 2/      (فصل 2)
│   │   └── ...
│   └── ...
├── 8/          (پایه هشتم)
│   └── ...
└── 9/          (پایه نهم)
    └── ...
```

## ساختار library.json

**Isolated Components:**

- `toggleBtn`, `panel`, `closeBtn` in `assets/JS/main.js` are UI components for toggling and managing content. These components are isolated and lack detailed documentation. For more information, see `assets/JS/main.js`.

نتیجه `library.json` شامل:

- **videos**: فیلم‌های آموزشی (به صورت دستی اضافه می‌شوند)
- **notes**: یادداشت‌ها و کاربرگ‌ها (خودکار تولید می‌شوند)

هر یادداشت دارای:

- `id`: شناسه منحصربفرد
- `title`: عنوان فایل
- `grade`: پایه تحصیلی (7، 8، 9)
- `chapter`: شماره فصل
- `file`: مسیر نسبی فایل
- `level`: سطح (تمرینی یا مفاهیمی)

## قوانین نامگذاری فایل

**Isolated Components:**

- `toggleBtn`, `panel`, `closeBtn` in `assets/JS/main.js` are UI components for toggling and managing content. These components are isolated and lack detailed documentation. For more information, see `assets/JS/main.js`.

بهتر است فایل‌های PDF را با یکی از این الگوها نام‌گذاری کنید:

```
کاربرگ علوم [پایه] فصل ([عدد]).pdf
روبیک جامع [پایه] - فصل ([عدد]).pdf
```

مثال:

- `کاربرگ علوم هفتم فصل (1).pdf`
- `روبیک جامع هشتم - فصل (5).pdf`

## فایل‌های مربوطه

**Isolated Components:**

- `toggleBtn`, `panel`, `closeBtn` in `assets/JS/main.js` are UI components for toggling and managing content. These components are isolated and lack detailed documentation. For more information, see `assets/JS/main.js`

- `scripts/generate-library.js` - اسکریپت تولید library.json
- `.github/workflows/static.yml` - GitHub Actions workflow
- `package.json` - تنظیمات npm

**Isolated Nodes in package.json:**

- `name` and `version` fields are critical metadata but lack detailed explanations in documentation.

- `scripts/generate-library.js` - اسکریپت تولید library.json
- `.github/workflows/static.yml` - GitHub Actions workflow
- `package.json` - تنظیمات npm

## نکات مهم

**Isolated Components:**

- `toggleBtn`, `panel`, `closeBtn` in `assets/JS/main.js` are UI components for toggling and managing content. These components are isolated and lack detailed documentation. For more information, see `assets/JS/main.js`

**Isolated Nodes in package.json:**

- `name` and `version` fields are critical metadata but lack detailed explanations in documentation.

1. **videos** به صورت دستی در library.json اضافه/تغییر می‌شوند و توسط اسکریپت حفظ می‌شوند
2. **notes** کاملاً خودکار تولید می‌شوند بر اساس محتویات پوشه downloads/
3. اگر فایلی از downloads/ حذف شود، در نسخه بعدی اسکریپت نیز حذف می‌شود

## مثال اجرای دستی

**Isolated Components:**

- `toggleBtn`, `panel`, `closeBtn` in `assets/JS/main.js` are UI components for toggling and managing content. These components are isolated and lack detailed documentation. For more information, see `assets/JS/main.js`

**Isolated Nodes in package.json:**

- `name` and `version` fields are critical metadata but lack detailed explanations in documentation.

**Isolated Components:**

- `toggleBtn`, `panel`, `closeBtn` in `assets/JS/main.js` are UI components for toggling and managing content. These components are isolated and lack detailed documentation. For more information, see `assets/JS/main.js`

**Isolated Nodes in package.json:**

- `name` and `version` fields are critical metadata but lack detailed explanations in documentation.

```bash
# نصب dependencies (اختیاری، چون فقط Node.js داخلی استفاده می‌شود)
npm install

# تولید library.json
npm run generate-library

# یا بدون npm
node scripts/generate-library.js
```

**Isolated Components:**

- `toggleBtn`, `panel`, `closeBtn` in `assets/JS/main.js` are UI components for toggling and managing content. These components are isolated and lack detailed documentation. For more information, see `assets/JS/main.js`

**Isolated Nodes in package.json:**

- `name` and `version` fields are critical metadata but lack detailed explanations in documentation.

خروجی مثال:

```
🔍 Scanning downloads directory...
📝 Found 45 note files
✅ Successfully generated library.json
   - Videos: 3
   - Notes: 45
   File: assets/content/library.json
```
