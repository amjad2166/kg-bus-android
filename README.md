# تطبيق أندرويد — باص الروضة

يبني GitHub تلقائيًا ملف **APK** لتطبيق أندرويد يفتح نظام الروضة كتطبيق مستقل
(Trusted Web Activity)، مع استقبال الإشعارات حتى والتطبيق مغلق.

## خطوات التشغيل
1. عدّل `SITE_HOST` و `START_PATH` في ملف `app-config.properties`.
2. أضف السرّين في Settings ← Secrets and variables ← Actions:
   `ANDROID_KEYSTORE_BASE64` و `ANDROID_KEYSTORE_PASSWORD`.
3. أي تعديل يُحفظ في الفرع main يبدأ البناء تلقائيًا (تبويب Actions، حوالي 5 دقائق).
4. رابط التحميل الثابت لآخر إصدار:
   `https://github.com/<اسم-الحساب>/<اسم-المستودع>/releases/latest/download/kg-bus.apk`
5. ضع ملف `assetlinks.json` (المرفق مع كل إصدار) على موقع الروضة في:
   `https://نطاق-الموقع/.well-known/assetlinks.json` — ليفتح التطبيق بملء الشاشة دون شريط العنوان.
