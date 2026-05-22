---
layout: page
title: استيراد الاشتراكات
parent: الاستخدام
permalink: /ar/usage/importing-subscriptions/
lang: ar
---

يدعم FreeTube استيراد اشتراكاتك من عدة خدمات. فيما يلي طريقة الاستيراد من كل منها.

## من YouTube

1. سجّل الدخول إلى حساب YouTube
2. انقر صورة ملفك الشخصي في الزاوية العلوية اليمنى
3. اختر «Your data in YouTube» من القائمة
4. انقر «More» في بطاقة «Your YouTube dashboard»
5. انقر «Download data»
6. ضمن «Create a New Export»، تأكد من اختيار «YouTube and YouTube Music»
7. انقر «All YouTube data included» وألغِ تحديد كل شيء ما عدا «Subscriptions»
8. انقر «OK»
9. انقر «Next step»
10. اختر طريقة التسليم (بريد، Dropbox، إلخ) ثم «Create Export» (الخطوات التالية تفترض التسليم بالبريد)
11. افتح بريدك ونزّل ملف `.zip`
12. فكّ ضغط الملف
13. الملف المطلوب: `Takeout/YouTube and YouTube Music/subscriptions/subscriptions.csv`

بعد ذلك، في FreeTube: **الإعدادات ← البيانات ← استيراد الاشتراكات**

## من Invidious

بعد تسجيل الدخول إلى حساب Invidious، افتح الإعدادات وانتقل إلى أسفل الصفحة وابحث عن «Import/Export Data». في الصفحة الجديدة، في الأسفل: «Import Subscriptions as OPML (for NewPipe and FreeTube)».

ثم في FreeTube: **الإعدادات ← البيانات ← استيراد الاشتراكات**

## من NewPipe

افتح صفحة الاشتراكات (وليس الإعدادات). انقر عنوان «Subscriptions» لفتح قائمة، ثم «Export to File». انقل الملف إلى جهازك الذي يشغّل FreeTube.

ثم: **الإعدادات ← البيانات ← استيراد الاشتراكات**

## من نسخة FreeTube أخرى

في الإعدادات، ضمن «Subscription Settings»، اختر نوع التصدير «FreeTube» وانقر «Export Subscriptions». بعد نقل الملف إلى الجهاز الجديد:

**الإعدادات ← البيانات ← استيراد الاشتراكات**

## من مصدر آخر

حاليًا لا ندعم الاستيراد إلا من الطرق أعلاه. اطلب من مطوّر التطبيق الآخر دعم التصدير بأحد هذه الصيغ ثم استخدمه في FreeTube.

## استكشاف الأخطاء

إذا فشل الاستيراد، جرّب:

- تغيير تفضيل API ([محلي](/usage/local-api) / [Invidious](/usage/invidious-api))، أو مثيل Invidious آخر من [api.invidious.io](https://api.invidious.io/)
- البحث عن قنوات مكررة في ملف التصدير. يعرض FreeTube رسالة إن لم تُستورد كل القنوات؛ التكرار في تصدير YouTube شائع وليس دائمًا خطأً حقيقيًا
- التحقق من قنوات محظورة أو محذوفة في الملف؛ YouTube قد يبقيها في التصدير بينما لا يستطيع FreeTube استيرادها

إن استمرت المشكلة، [افتح مشكلة](/community/creating-an-issue) وقد تحتاج إلى إرفاق رابط لملف التصدير.
