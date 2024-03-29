---
title: العمل باستخدام نمط الإعدادات المسبقة
description: يصف هذا المقال كيفية استخدام الإعدادات المسبقة لأنماط الموقع في منشئ الموقع في Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: ea22c4c50a25c18d25980b8d2ce9bcf8cd315e87
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267502"
---
# <a name="work-with-style-presets"></a>العمل باستخدام نمط الإعدادات المسبقة

[!include [banner](includes/banner.md)]

يصف هذا المقال كيفية استخدام الإعدادات المسبقة لأنماط الموقع في منشئ الموقع في Microsoft Dynamics 365 Commerce.

الإعداد المسبق للنمط هو مجموعة مخزنة من جميع قيم النمط القابلة للاستخدام في نسق نمط. ويمكن استخدامه لتغيير شكل أحد المواقع على الفور من منشئ الموقع. تسمح الإعدادات المسبقة للأنماط للمؤلفين في منشئ الموقع في Commerce بتغيير مجموعة من قيم الأنماط في موقعهم ومعاينتها وتنشيطها، من دون استخدام أوراق الأنماط المتتالية (CSS) أو نشر النُسق. تعتبر أنماط الخطوط وأنماط الأزرار وألوان الموقع أمثلة نموذجية عن متغيرات الأنماط التي يمكن إدارتها عبر الإعدادات المسبقة للأنماط.

تتحدد مجموعة متغيرات الأنماط المتوفرة في موقع ما حسب مكتبة النُسق والوحدات النمطية التي يتم نشرها في مستأجر الموقع. تسمح مجموعة تطوير البرامج (SDK) الخاصة بـ Dynamics 365 Commerce عبر الإنترنت (SDK) للمطورين بتطبيق العدد الذي يحتاجون إليه من متغيرات الأنماط القابلة للاستخدام لنسق معين. ومن خلال تمكين عدد أكبر من متغيرات الأنماط، بإمكان مطور النسق تقديم الاختيارات النهائية حول أنماط الموقع للمؤلفين في منشئ الموقع. وبالتالي، بإمكان المستخدمين من غير المطورين تحديث أنماط الموقع ومعاينتها باستخدام مجموعة الأدوات. تعتبر الإمكانية مفيدة أيضًا لأي سيناريو حيث ستؤدي التغييرات المباشرة على النُسق أو CSS إلى مصروفات زائدة غير ضرورية.

تحتاج النُسق حيث تم تمكين متغيرات الأنماط القابلة للاستخدام إلى إعداد مسبق افتراضي للنمط. وبإمكانها أن تتضمن، بشكل اختياري، خيارات إعدادات مسبقة إضافية كجزء من حزمة نُسق منشورة. على سبيل المثال، يمكن نشر نسق يتضمن إعدادًا مسبقًا واحدًا افتراضيًا للنمط "الضوء العصري". أو قد تتضمن خيارات إعدادات مسبقة إضافية إلى جانب الإعداد الافتراضي، مثل "داكن حديث" أو "فاتح عتيق" أو "داكن عتيق". يتم إنشاء هذه الإعدادات المسبقة المضمنة للنُسق من قبل المطورين ويمكن استخدامها كنقاط بداية لتصميمات مواقع الجديدة.

في منشئ الموقع، بإمكان المؤلفين الاختيار من ضمن مجموعة من الإعدادات المسبقة المضمنة لنسق، أو يمكنهم إنشاء إعدادات مسبقة لأنماط خاصة بهم وتخصيصها باستخدام متغيرات الأنماط التي تم تمكينها. يمكن معاينة الإعدادات المسبقة للنمط في منشئ الموقع قبل تنشيطها في الموقع المباشر. بعد مراجعة تغييرات النمط التي قام بها المؤلف، يمكنك عندئذٍ تعيين الإعداد المسبق للنمط إلى "نشط" في الموقع المباشر.

## <a name="preview-a-style-preset"></a>معاينة إعداد مسبق لنمط

لمعاينة إعداد مسبق لنمط على موقعك في منشئ الموقع، اتبع الخطوات التالية.

1. في جزء التنقل الأيمن الخاص بموقعك، انتقل إلى **إعدادات الموقع \> تصميم**.
1. في صفحة **الإعدادات المسبقة للأنماط** في أعلى محرر التصميم، في قائمة **الإعدادات المسبقة المتوفرة**، حدد إعدادًا مسبقًا، ثم حدد **عرض** للانتقال إلى محرر الإعداد المسبق.

    في حال عدم وجود إعدادات مسبقة في قائمة **الإعدادات المسبقة المتوفرة**، راجع [إنشاء إعداد مسبق مخصص لنمط](#create-a-custom-style-preset) للحصول على معلومات حول كيفية إنشاء إعداد مسبق مخصص لنمط.

    > [!NOTE]
    > يشار إلى الإعدادات المسبقة التي كانت مضمنة مع النسق بشارة **مضمن**. هذه الإعدادات المسبقة المضمنة هي للقراءة فقط. لنسخ إعداد مسبق مضمن كإعداد مسبق جديد قابل للتخصيص، حدد زر علامة القطع (**...**) للإعداد المسبق، ثم حدد **حفظ باسم**.

1. في شريط الأوامر، حدد **معاينة**.
1. حدد عنوان URL من موقعك لاستخدامه لمعاينة الإعداد المسبق للنمط، ثم حدد **موافق**.
1. حدد متغير عنوان URL الخاص بالقناة والخاص بالإعدادات المحلية لمعاينته عن طريق تحديد اسم المتغير. تفتح نافذة مستعرض جديدة للمعاينة، حيث يتم تطبيق الإعداد المسبق للنمط على الصفحة المحددة.

> [!NOTE]
> عنوان URL الخاص بالمعاينة دائم ومصادق عليه. وبالتالي، يمكنك نسخه ولصقه وإرساله إلى زملاء آخرين مصادق عليه لمراجعته قبل أن تقوم بتعيينه إلى "نشط" على موقعك المباشر. ويعتبر أيضًا عنوان URL للمعاينة مفيدًا لتدقيق الأنماط على أجهزة مختلفة وفي مستعرضات مختلفة وعلى شاشات مختلفة.

> [!TIP]
> بينما تقوم بتحرير إعداد مسبق لنمط، قد يتبين لك أنه من المفيد ترك نافذة مستعرض المعاينة الخاصة به مفتوحة في نافذة مستعرض منفصلة، بحيث يمكنك التحقق بسرعة من صحة تغييراتك بعد حفظ تغييراتك في إعداد مسبق، يمكنك تحديث نافذة مستعرض المعاينة المفتوحة للتحقق من تجربة المستخدم.

## <a name="create-a-custom-style-preset"></a>إنشاء إعداد مسبق مخصص لنمط

لإنشاء إنشاء إعداد مسبق مخصص لنمط في منشئ الموقع، اتبع الخطوات التالية.

1. في جزء التنقل الأيمن الخاص بموقعك، انتقل إلى **إعدادات الموقع \> تصميم**.
1. على علامة التبويب **الإعدادات المسبقة للأنماط** في أعلى محرر التصميم، على شريط الأوامر، حدد **إعداد مسبق جديد**.
1. أدخل اسمًا ووصفًا للإعداد الجديد، ثم حدد **حفظ** يتم إنشاء إعداد مسبق جديد قابل للتخصيص يستخدم القيم الافتراضية للنسق كنقطة بداية.

> [!NOTE]
> يمكنك أيضًا إنشاء إعداد مسبق مخصص للنمط من أي إعداد مسبق موجود عن طريق تحديد زر علامة القطع (**...**) لهذا الإعداد المسبق ثم تحديد **حفظ باسم**. أو يمكنك تحديد **حفظ باسم** على شريط الأوامر في محرر الإعداد المسبق.

## <a name="modify-global-and-module-type-style-values"></a>تعديل قيم الأنماط العمومية ومن نوع الوحدة النمطية

تتم مشاركة بعض متغيرات أنماط النسق بين أنواع وحدات نمطية متعددة. يشار إلى متغيرات الأنماط هذه باسم متغيرات الأنماط *العمومية*. تتضمن الأمثلة ألوان الموقع الأساسية وأنماط الخطوط الافتراضية وأنماط الأزرار. ومن خلال تعيين المتغيرات العامة، قد تقوم بتغيير شكل الموقع عبر عدة أنواع مختلفة من الوحدات النمطية.

بإمكان بعض قيم الأنماط أن تكون فريدة لنوع وحدة نمطية، أو قد تحتاج إلى تجاوز قيمة عمومية افتراضية بشكل اختياري. إذا قام نسق موقع بتطبيق متغيرات أنماط من نوع الوحدة النمطية، فبإمكان المؤلفين في منشئ الموقع تخصيص نمط من نوع الوحدة النمطية بشكل مستقل عن الإعدادات العمومية. بإمكان المتغيرات من نوع الوحدة النمطية أن تزيد أو تتجاوز متغيرات الأنماط العمومية في النسق.

> [!NOTE]
> سلوك التدرج الهرمي لقيم النمط في موقع ما هو كالتالي: تتجاوز قيم الأنماط التي تظهر إلى أقصى اليمين قيم الأنماط الموجودة إلى يسارها.
>
> القيم الافتراضية للنسق \< القيم العمومية للأنماط \< قيم الأنماط من نوع الوحدة النمطية \< تجاوز CSS

لتغيير القيم العمومية أو القيم من نوع الوحدة النمطية لنمط معين في منشئ الموقع، اتبع الخطوات التالية.

1. في جزء التنقل الأيمن الخاص بموقعك، انتقل إلى **إعدادات الموقع \> تصميم**.
1. على علامة التبويب **الإعدادات المسبقة للأنماط** في أعلى محرر التصميم، حدد **عرض** لأي إعداد مسبق للنمط للانتقال إلى محرر الإعداد المسبق.
1. حدد **معاينة**، ثم اتبع خطوات تحديد عنوان URL لفتح معاينة نافذة مستعرض كاملة لإعدادك المسبق. اترك نافذة مستعرض المعاينة هذه مفتوحة.
1. في محرر الإعداد المسبق، حدد **تحرير** في الجزء الأيمن العلوي.
1. استخدم عناصر تحكم متغيرات الأنماط في المحرر لتغيير بعض قيم الأنماط العمومية.
1. في أعلى المحرر، على علامة تبويب **الوحدات النمطية** إلى يسار علامة التبويب **عمومي**، حدد نوع وحدة نمطية لتطبيق الأنماط عليها.
1. استخدم عناصر تحكم النمط لتغيير بعض القيم لنوع الوحدة النمطية.
1. عندما تصبح جاهزًا لمعاينة التغييرات، حدد **حفظ** على شريط الأوامر.
1. عد إلى نافذه مستعرض المعاينة المفتوحة، وقم بتحديثها. تعتبر المعاينة في نافذة المستعرض الكاملة مفيدة للتحقق من تغييرات الأنماط عند نقاط توقف مختلفة في طريقة العرض وفي مستعرضات مختلفة وعلى أنظمة أساسية لأجهزة مختلفة.
1. عند اكتمال كافة التغييرات والتحقق من صحتها، حدد **إنهاء** في أعلى يسار المحرر.

> [!NOTE]
> إذا كنت تعمل على تحرير إعداد مسبق لنمط نشط حاليًا في موقعك، سترى الشارة الزرقاء **نشط** في المحرر. تشير هذه الشارة إلى أن الإعداد المسبق موجود حاليًا في العرض المباشر على موقعك على الويب. إذا قمت بتغيير الإعداد المسبق النشط، فحدد **نشر** لدفع تلك التغييرات إلى موقعك المباشر.

## <a name="make-a-new-style-preset-active-on-your-live-site"></a>تنشيط إعداد مسبق لنمط جديد في موقعك المباشر

لتعيين إعداد مسبق لنمط على أنه الإعداد المسبق النشط الجديد في موقعك، اتبع الخطوات التالية.

- حدد **الزر تعيين كنشط** في أحد الأماكن التالية:

    - شريط الأوامر في محرر الإعداد المسبق للنمط
    - قائمة زر القطع (**...**) لأي إعداد مسبق متوفر في طريقة إعداد الرئيسية على علامة التبويب **الإعدادات المسبقة للأنماط** في **إعدادات الموقع \> التصميم**

يتم تنشيط قيم أنماط الإعداد المسبق عبر موقعك العام على الويب.

## <a name="additional-resources"></a>الموارد الإضافية

[إضافة شعار](add-logo.md)

[تحديد سمة الموقع](select-site-theme.md)

[العمل CSS مع ملفات التجاوز](css-override-files.md)

[إضافة أيقونة المفضلة](add-favicon.md)

[إضافة إشعار لحقوق النشر](add-copyright-notice.md)

[إضافة لغات إلى الموقع الخاص بك](add-languages-to-site.md)

[إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
