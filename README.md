# ProtiVue

تطبيق ويب (PWA) لتحليل الوجبات بالصور ومتابعة البروتين والسعرات. بيشتغل على الموبايل زي أي تطبيق، ومجاني بالكامل.

| الجزء | الخدمة | التكلفة |
| --- | --- | --- |
| الاستضافة | GitHub Pages | مجاني |
| تحليل الصور | Google Gemini API (الخطة المجانية) | مجاني بحدود استخدام يومية |
| القيم الغذائية | جدول USDA مدمج + بحث USDA FoodData Central | مجاني |
| حفظ البيانات | على الموبايل نفسه (IndexedDB) | مجاني، ومفيش سيرفر |

## ١) رفع التطبيق على GitHub Pages (مرة واحدة، حوالي ١٠ دقايق)

1. اعمل حساب مجاني على github.com.
2. اضغط **+** فوق ← **New repository**، واكتب الاسم `protivue`، واختار **Public**، وبعدين **Create repository**.
3. في صفحة الـrepository اضغط **uploading an existing file**، واسحب **كل محتويات** فولدر `protivue` (index.html، manifest.webmanifest، sw.js، فولدر icons)، واضغط **Commit changes**.
4. روح **Settings** ← **Pages**. تحت **Branch** اختار `main` و `/ (root)` واضغط **Save**.
5. استنى دقيقة أو اتنين، الرابط هيظهر فوق الصفحة، شكله كده:
   `https://اسم-حسابك.github.io/protivue/`

## ٢) مفتاح Gemini المجاني (لتحليل الصور)

1. افتح aistudio.google.com/apikey وادخل بحساب Google.
2. اضغط **Create API key** وانسخ المفتاح.
3. في ProtiVue: **الملف** ← **تحليل الصور (مجاني)** ← الصق المفتاح ← **حفظ الإعدادات**.

المفتاح بيتحفظ على موبايلك بس. لو حد تاني هيستخدم التطبيق، يعمل مفتاحه المجاني بنفسه.

**ملاحظات على الخطة المجانية:**
- فيها حد للطلبات في الدقيقة واليوم. لو عديته هتظهرلك رسالة؛ استنى شوية أو سجّل الوجبة يدويًا.
- في الخطة المجانية، Google ممكن تستخدم الصور اللي بتتبعت لتحسين منتجاتها.
- لو ظهر خطأ «النموذج غير موجود»، غيّر اسم النموذج من الإعدادات لاسم نموذج Flash الحالي من صفحة نماذج Gemini.

## ٣) تنصيب التطبيق على الموبايل

- **iPhone (Safari):** افتح الرابط ← زرار المشاركة ← **إضافة إلى الشاشة الرئيسية**.
- **Android (Chrome):** افتح الرابط ← القائمة ⋮ ← **تثبيت التطبيق** أو **إضافة إلى الشاشة الرئيسية**.

التطبيق هيفتح ملء الشاشة من غير شريط المتصفح، وبيشتغل من غير إنترنت في الإدخال اليدوي والتقارير. تحليل الصور والبحث في USDA محتاجين إنترنت.

## ٤) بياناتك

- كل حاجة محفوظة على الموبايل بس. لو مسحت بيانات المتصفح أو شلت التطبيق، البيانات هتتمسح.
- من **الملف** ← **النسخ الاحتياطي** ← **تصدير نسخة**، واحفظ الملف على Drive أو ابعته لنفسك بالإيميل. تقدر **تستورده** على أي جهاز.

## (اختياري) مفتاح USDA

البحث الموسّع في أصناف USDA شغال من غير مفتاح بس بحد صغير. لو عايز حد أكبر، اعمل مفتاح مجاني من fdc.nal.usda.gov/api-key-signup وحطه في الإعدادات.

## تحديث التطبيق

لو عدلت أي ملف، ارفعه تاني على نفس الـrepository. الموبايل هياخد النسخة الجديدة أول ما تفتح التطبيق وانت متصل بالإنترنت.

---

# ProtiVue (English)

A free PWA for meal-photo analysis and protein/calorie tracking.

1. **Host** on GitHub Pages: new public repo `protivue` → upload all files → Settings → Pages → branch `main`, `/ (root)` → Save. Your link: `https://<username>.github.io/protivue/`.
2. **Free Gemini key:** aistudio.google.com/apikey → Create API key → paste it in ProtiVue → Profile → Photo analysis → Save settings. Free-tier limits apply, and on the free tier Google may use submitted content to improve its products.
3. **Install:** iPhone Safari → Share → Add to Home Screen. Android Chrome → ⋮ → Install app.
4. **Data** stays on the device only. Use Profile → Backup → Export regularly.
