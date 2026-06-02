# GOO Android App — دليل البناء

## الطريقة الأسرع: GitHub Actions (بدون أي أدوات)

### الخطوات:
1. أنشئ **repository جديد** على GitHub (اسمه مثلاً `goo-android`)
2. ارفع **جميع ملفات هذا المجلد** كما هي مع المجلدات
3. اذهب لـ **Actions** في الـ repository
4. ستجد workflow اسمه **"Build GOO APK"** يعمل تلقائياً
5. بعد 3-5 دقائق → اضغط على الـ workflow → **Artifacts** → حمّل APK

**أو** اضغط يدوياً: Actions → Build GOO APK → **Run workflow**

---

## البناء المحلي (اختياري)

### المتطلبات:
- Android Studio أو Android SDK
- JDK 17+

### الأوامر:
```bash
# Debug APK
./gradlew assembleDebug

# Release APK
./gradlew assembleRelease

# الناتج في:
# app/build/outputs/apk/debug/app-debug.apk
# app/build/outputs/apk/release/app-release.apk
```

---

## ملاحظات

- التطبيق يفتح `https://fa78383012736al-a11y.github.io/goo/accounting_system.html`
- عند عدم الإنترنت يعمل من النسخة المحلية في `assets/index.html`
- روابط Wordwall و Forms تفتح في المتصفح الخارجي
- minSdk: 21 (Android 5.0+) — يدعم 99% من الأجهزة
