# مشروع Android لتطبيق إيجار (Capacitor)

هذا المجلد هو اللي يُرفع على مستودع GitHub (`ejar-native`) ليبني الـ APK تلقائيًا.

**الدليل الكامل بالخطوات المرقّمة:** ملف `../docs/GITHUB-SETUP-AR.md`

## محتويات المجلد
- `www/index.html` — التطبيق نفسه (نفس ملف `../source/index.html`، لازم يكونان متطابقين)
- `package.json` / `capacitor.config.json` — إعدادات Capacitor والإضافات (Notifications, Filesystem, Share, App, SplashScreen)
- `.github/workflows/build-apk.yml` — سير البناء: يبني APK ثم **يوقّعه بالمفتاح الدائم** من Secrets (`KEYSTORE_BASE64`, `KEYSTORE_PASSWORD`)
- `icon-assets/` `splash-assets/` `sound-assets/` — الأيقونات وشاشات البداية ونغمات التنبيه

## ملاحظات سريعة
- أول APK موقّع بالمفتاح الجديد يحتاج حذف النسخة القديمة؛ بعدها التحديثات فوق بعض.
- الصور محفوظة على الجهاز فقط: خذ «نسخة احتياطية للصور» من الإعدادات قبل أي حذف للتطبيق.
- المفتاح السري **ليس** داخل هذه الحزمة (حزمة منفصلة) ولا يُرفع على GitHub.
