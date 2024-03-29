---
title: العمل مع ملفات تجاوز CSS
description: يصف هذا  المقال لماذا، ومتى، وكيفية استخدام ملفات التجاوز الخاصة بأوراق الأنماط المتتالية (CSS) في Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 3cb0307ab708a430d01610c5afb2802d650a068a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270029"
---
# <a name="work-with-css-override-files"></a>العمل مع ملفات تجاوز CSS

[!include [banner](includes/banner.md)]

يصف هذا  المقال لماذا، ومتى، وكيفية استخدام ملفات التجاوز الخاصة بأوراق الأنماط المتتالية (CSS) في Microsoft Dynamics 365 Commerce.

يجب دائمًا معالجة أنماط الموقع الدائمة من خلال سمة الموقع. توفر المظاهر إعدادات CSS وإعدادات النمط للوحدات النمطية في أي صفحة من موقعك. يتم إنشاء السمات باستخدام مجموعة تطوير البرامج (SDK) الخاصة بـ Dynamics 365 Commerce عبر الإنترنت، ويتم نشرها على مواقع الويب الخاصة بك من خلال Microsoft Dynamics Lifecycle Services (LCS). تساعد قدرات تصحيح السمات وتكوينات واجهة الوحدة النمطية في SDK مطوري المواقع على إنشاء حزم تصميم موقع قابلة للتخصيص ومتماسكة. عند نشر حزم التصميم هذه على موقع ما، يمكن لمؤلفي الموقع التركيز على إنشاء محتوى وتحريره ونشره بدلاً من تطوير الموقع.

بالنظر إلى دورة الحياة المعتادة للسمة، فإن الاعتماد على المطورين لإجراء تغييرات على النمط من خلال تدفقات نشر SDK و LCS قد يكون باهظ الثمن في بعض السيناريوهات. قد تبدو النماذج الأولية أو الإصلاحات العاجلة للموقع مرهقة إذا لم يتم تكوين SDK، أو إذا لم يكن لديك الوقت لانتظار نشر LCS.

في هذه السيناريوهات، يمكن ان تساعد ملفات التجاوز الخاصة بـ CSS . في أدوات التأليف التجارة، يمكن للمستخدمين المصادق عليهم تحميل ملف CSS، ومعاينته، ثم تنشيطه لتجاوز سمة الموقع. لا نحتاج إلى مصروفات زائدة‬ لنشر SDK أو LCS. يمكن أن تكون التجاوزات المحددة في ملف التجاوز الخاص بـ CSS صغيرة مثل التغيير في نمط نص واحد أو واسعة النطاق مثل إصلاح العلامة التجارية بالكامل.

قبل استخدام ملفات التجاوز الخاصة بـ CSS، يجب أن تكون علي علم بالقيود التالية:

- يمكن فقط تنشيط ملف تجاوز CSS واحد فقط علي الموقع في كل مرة. لذا، يجب أن تكون كافة التجاوزات النشطة موجودة في ملف تجاوز واحد.
- على الرغم من أنه يمكنك معاينة التجاوزات في أدوات تأليف التجارة، إلا أنه لا توجد ميزات مخصصة لتصحيح الأخطاء للمساعدة في تحديد أي أخطاء تقدمها التجاوزات. وبعبارة أخرى، عند استخدام ملفات CSS للتجاوز، لا تملك نفس مجموعة الأدوات التي يوفرها SDK لوحدة التحقق من صحة الوحدة والتأليف.

ومع ذلك، توفر ملفات CSS للتجاوز طريقه سريعة لنموذج تصميم أو تطبيق إصلاح عاجل قبل تحديث سمه كامله تطوير ونشرها.

## <a name="create-a-css-override-file"></a>إنشاء ملف CSS للتجاوز

لإنشاء ملف CSS للتجاوز، يمكنك استخدام اي بيئة تطوير متكاملة (IDE) أو محرر نص أو محرر التعليمات البرمجية المصدر. تتمثل الطريقة المعتادة في استخدام مصحح أخطاء الويب القياسية في المستعرض الخاص بك لتحديد محددات النمط والخصائص والقيم على موقعك الحالي. تسمح لك معظم المستعرضات بتغيير القيم ومعاينتها في مصحح الأخطاء. بعد تحديد التغييرات التي تريد اجراؤها، يمكنك حفظها في ملف CSS الخاص بك.

## <a name="upload-a-css-override-file"></a>تحميل ملف CSS للتجاوز

لتحميل ملف CSS إلى موقعك في التجارة، اتبع الخطوات التالية.

1. في أدوات التأليف، انتقل إلى الموقع الخاص بك.
1. في جزء التنقل على اليسار، حدد **التصميم**.

    > [!NOTE]
    > استنادًا إلى إصدار أدوات تأليف التجارة التي تستخدمها، قد تضطر إلى توسيع **الإعدادات** في جزء التنقل قبل ان تتمكن من تحديد **التصميم**.

1. في الجزء العلوي من جزء التصميم الرئيسي، حدد علامة التبويب **CSS للتجاوز**، إذا لم تكن محددة بالفعل.
1. ضمن **ملفات CSS للتجاوز المتوفرة**، حدد **تحميل ملف CSS**. يظهر إطار مستكشف الملفات.
1. في "مستكشف الملفات"، استعرض ملف CSS وحدده، ثم حدد **فتح**. يظهر ملف CSS الذي تم تحميله الآن ضمن **ملفات CSS للتجاوز المتوفرة**.

## <a name="preview-a-css-override-file"></a>معاينة ملف CSS للتجاوز

لمعاينة ملف CSS للتجاوز قبل جعله نشطًا علي موقعك المباشر، اتبع الخطوات التالية.

1. في جزء التنقل علي اليسار، حدد **تصميم**، ثم في علامة التبويب ملفات **CSS للتجاوز**، ضمن **ملفات CSS للتجاوز المتوفرة**، ابحث عن ملف CSS الذي تريد معاينته.
1. بجوار اسم ملف CSS، حدد **معاينه الموقع**.
1. في مربع الحوار **حدد عنوان URL**، حدد عنوان URL الخاص بالموقع الذي ترغب في رؤية التجاوز المطبق عليه، ثم حدد **موافق**.
1. إذا كان هناك العديد من المتغيرات لعنوان URL المحدد، فحدد المتغير المطلوب في مربع الحوار **معاينة التغييرات** التي تظهر.

يتم فتح علامة تبويب أو نافذة مستعرض جديدة، حيث يمكنك التحقق من صحة تجاوزات النمط الخاصة بك مقابل موقعك. يمكنك بعد ذلك مشاركة عنوان URL مع مستخدمي التجارة المعتمدين الآخرين للمراجعة والتعليقات.

## <a name="activate-a-css-override-file-on-your-live-site"></a>قم بتنشيط ملف CSS للتجاوز على موقع العرض المباشر الخاص بك

بعد معاينة ملف CSS للتجاوز واعتماده، يمكنك تنشيطه على موقع العرض المباشر الخاص بك.

> [!NOTE]
> يمكن فقط تنشيط ملف CSS للتجاوز واحد فقط علي موقعك في كل مرة. إذا قمت بتنشيط ملف تجاوز جديد، يتم إلغاء تنشيط ملف التجاوز السابق. لذا، تأكد من أن كافة التجاوزات المطلوبة موجودة في ملف CSS للتجاوز واحد.

لتنشيط ملف CSS للتجاوز، اتبع الخطوات التالية:

1. في جزء التنقل علي اليسار، حدد **تصميم**، ثم في علامة التبويب ملفات **CSS للتجاوز**، ضمن **ملفات CSS للتجاوز المتوفرة**، ابحث عن ملف CSS الذي تريد تنشيطه.
1. ضمن اسم ملف CSS، حدد **تنشيط**. يصبح ملف التجاوز نشطًا على الفور في موقع العرض المباشر الخاص بك.

## <a name="deactivate-a-css-override-file-on-your-live-site"></a>إلغاء تنشيط ملف CSS للتجاوز على موقع العرض المباشر الخاص بك

لإلغاء تنشيط CSS ملف تجاوز علي موقعك، اتبع الخطوات التالية.

1. في جزء التنقل علي اليسار، حدد **تصميم**، ثم في علامة التبويب ملفات **CSS للتجاوز**، ضمن **ملفات CSS للتجاوز المتوفرة**، ابحث عن ملف CSS الذي تريد إلغاء تنشيطه.
1. ضمن اسم ملف CSS، حدد **إلغاء التنشيط**. يصبح ملف التجاوز غير نشط على الفور في موقع العرض المباشر الخاص بك.

> [!TIP]
> للوصول إلى خيارات ملفات CSS للتجاوز الإضافية، حدد علامة القطع (**...**) بجوار اسم ملف CSS . تعتبر خيارات **التنزيل**، و **إعادة التسمية**، و **الاستبدال** مفيدة للتغييرات السريعة على ملف CSS للتجاوز الموجود.

## <a name="additional-resources"></a>الموارد الإضافية

[إضافة شعار](add-logo.md)

[تحديد سمة الموقع](select-site-theme.md)

[استخدام الإعدادات المسبقة للأنماط](style-presets.md)

[إضافة أيقونة المفضلة](add-favicon.md)

[إضافة إشعار لحقوق النشر](add-copyright-notice.md)

[إضافة لغات إلى الموقع الخاص بك](add-languages-to-site.md)

[إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
