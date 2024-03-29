---
title: إدارة دورة حياة تكوين إعداد التقارير الإلكترونية (ER)
description: توضح هذه المقالة كيفية إدارة دورة حياة تكوينات التقارير الإلكترونية لحل Dynamics 365 Finance.
author: kfend
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 0209679c9882d87edab68d043fba9e7b3400a2a2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337185"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>إدارة دورة حياة تكوين إعداد التقارير الإلكترونية (ER)

[!include [banner](../includes/banner.md)]

توضح هذه المقالة كيفية إدارة دورة حياة ملفات [إعداد التقارير الإلكترونية](general-electronic-reporting.md) (ER) [التكوينات](general-electronic-reporting.md#Configuration) ل Dynamics 365 Finance.

## <a name="overview"></a>نظرة عامة

تُعد التقارير الإلكترونية محركًا يدعم المستندات الإلكترونية المطلوبة قانونًا والخاصة ببلد معين. بشكل عام، تفترض التقارير الإلكترونية إمكانية تنفيذ المهام التالية لمستند إلكتروني واحد. للحصول على مزيد من التفاصيل، راجع [نظرة عامة على التقارير الإلكترونية (ER)](general-electronic-reporting.md).

- تصميم قالب لمستند إلكتروني:

    - تحديد مصادر البيانات اللازمة التي يمكن تقديمها في هذا المستند:

        - البيانات الرئيسية مثل جداول البيانات وكيانات البيانات والفئات.
        - خصائص خاصة بالعملية مثل تاريخ ووقت التنفيذ والمنطقة الزمنية.
        - معلمات إدخال المستخدم، يتم تحديدها من قِبل المستخدم في وقت التشغيل.

    - تعريف عناصر المستندات اللازمة، فضلاً عن مخططها لتحديد تنسيق المستند النهائي.
    - تكوين تدفق البيانات المطلوب من مصادر البيانات المحددة إلى عناصر المستند المحددة (عبر ارتباطات مصادر البيانات بمكونات تنسيق المستند) وتحديد منطق التحكم في العملية.

- جعل قالب متوفرًا بحيث يمكن استخدامه في مثيلات أخرى:

    - تحويل قالب مستند تم إنشاؤه إلى تكوين التقارير الإلكترونية (ER) وتصدير التكوين من مثيل التطبيق الحالي كحزمة XML يمكن تخزينها محليًا أو في Lifecycle Services (LCS).
    - تحويل تكوين التقارير الإلكترونية إلى قالب مستند تطبيق.
    - استيراد حزمة XML مخزنة محليًا أو في LCS إلى المثيل الحالي.

- تخصيص قالب مستند إلكتروني:

    - إحضار قالب من LCS إلى المثيل الحالي كتكوين تقرير إلكتروني.
    - تصميم إصدار مخصص من تكوين تقرير إلكتروني، والاحتفاظ بمرجع إلى الإصدار الأساسي.

- دمج قالب بعملية تجارية معينة، بحيث يكون متوفرًا في التطبيق:

    - تكوين الإعدادات بحيث يبدأ التطبيق باستخدام تكوين التقارير الإلكترونية، من خلال الإشارة إلى ذلك التكوين في معلمة مرتبطة بالعملية. على سبيل المثال، يمكنك الإشارة إلى تكوين التقرير الإلكتروني في طريقة دفع حسابات دائنة لإنشاء رسالة دفع إلكترونية لمعالجة الفواتير.

- استخدام قالب في عملية تجارية معينة:

    - ‏‫تشغيل تكوين تقرير إلكتروني في عملية تجارية معينة. على سبيل المثال، لإنشاء رسالة دفع إلكترونية لمعالجة الفواتير عند تحديد طريقة دفع تشير إلى تكوين تقرير إلكتروني.

## <a name="concepts"></a>المفاهيم
تقترن الأدوار والأنشطة ذات الصلة التالية بدورة حياة تكوين التقارير الإلكترونية.

| الدور                                       | الأنشطة                                                      | ‏‏الوصف |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| مستشار وظيفي لإعداد التقارير الإلكتروني | إنشاء وإدارة مكونات التقارير الإلكترونية (نماذج وتنسيقات).           | رجل أعمال يصمم نماذج بيانات خاصة بمجال التقارير الإلكترونية ويصمم القوالب المطلوبة للمستندات الإلكترونية ويربطها معًا وفقًا لذلك. |
| مطور إعداد التقارير الإلكتروني             | إنشاء وإدارة تعيينات نموذج البيانات.                          | الأخصائي الذي يحدد مصادر بيانات Finance المطلوبة ويربطها بنماذج البيانات الخاصة بمجال التقارير الإلكترونية. |
| المشرف على المحاسبة                      | تكوين الإعدادات المتعلقة بالعملية التي تشير إلى نتائج التقارير الإلكترونية. | على سبيل المثال، دور **المشرف على المحاسبة** الذي يسمح باستخدام إعدادات تكوين التقارير الإلكترونية في طريقة دفع حسابات دائنة معينة لإنشاء رسالة دفع إلكترونية لمعالجة الفواتير. |
| موظف مدفوعات الحسابات الدائنة            | استخدام نتائج التقارير الإلكترونية في عملية تجارية معينة:                | على سبيل المثال، دور **موظف مدفوعات الحسابات الدائنة** الذي يسمح بإنشاء رسائل دفع إلكترونية لمعالجة الفواتير، استنادًا إلى تنسيق التقارير الإلكترونية الذي تم تكوينه لطريقة دفع محددة. |

## <a name="er-configuration-development-lifecycle"></a>دورة حياة تطوير تكوين التقارير الإلكترونية
للأسباب التالية المتعلقة بالتقارير الإلكترونية ، نوصي بتصميم تكوينات إعداد التقارير الإلكترونية في بيئة التطوير ، كمثيل منفصل للتمويل والعمليات:

- باستطاعة المستخدمين الذين يؤدون دور **مطور إعداد التقارير الإلكتروني** أو **مستشار وظيفي لإعداد التقارير الإلكتروني‬** تحرير التكوينات وتشغيلها لأغراض الاختبار. باستطاعة هذا السيناريو أن يؤدي إلى استدعاءات أساليب الفئات والجداول التي يمكن أن تكون ضارة لبيانات الأعمال وأداء المثيل.
- لا تتقيد استدعاءات أساليب الفئات والجداول كمصادر بيانات التقارير الإلكترونية لتكوينات التقارير الإلكترونية بنقاط دخول ومحتوى الشركة المسجل. وبالتالي، يستطيع المستخدمون الذين يؤدون دور **مطور إعداد التقارير الإلكتروني‬** أو **مستشار وظيفي لإعداد التقارير الإلكتروني‬** الوصول إلى بيانات الأعمال الحساسة.

يمكن [تحميل](#data-persistence-consideration) تكوينات التقارير الإلكترونية التي تم تصميمها في بيئة التطوير إلى بيئة الاختبار لتقييم التكوين (تكامل العملية المناسب وصحة النتائج والأداء) وضمان الجودة مثل صحة حقوق الوصول المدفوعة بالأدوار والفصل بين المهام. يمكن استخدام الميزات التي تتيح تبادل تكوين التقارير الإلكترونية لهذا الغرض. يمكن تحميل تكوينات التقارير الإلكترونية المثبتة إلى LCS لمشاركتها مع المشتركين في الخدمة أو يمكن [استيراداها](#data-persistence-consideration) إلى بيئة الانتاج للاستخدام الداخلي.

![دورة حياة تكوين التقارير الإلكترونية.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>اعتبار استمرارية البيانات

يمكنك [استيراد‏‎](tasks/er-import-configuration-lifecycle-services.md) بطريقة فردية [إصدارات‏‎](general-electronic-reporting.md#Configuration) مختلفة من تكوين تقارير إلكترونية إلى مثيل Finance. عند استيراد إصدار جديد من تكوين التقارير الإلكترونية، يتحكم النظام في محتوة إصدار المسودة لهذا التكوين:

- عندما يكون الإصدار المستورد أقل من الإصدار الأعلى لهذا التكوين في مثيل Finance الحالي، يبقي المحتوى الخاص بإصدار المسودة من هذا التكوين بدون تغيير.
- عندما يكون الإصدار المستورد أعلى من أي إصدار آخر من هذا التكوين في مثيل Finance الحالي، يتم نسخ محتو الإصدار المستورد إلى إصدار المسودة من هذا التكوين ليتيح لك متابعة تحرير آخر إصدار مكتمل.

إذا كان هذا التكوين مملوكًا من قبل [موفر](general-electronic-reporting.md#Provider) التكوين النشط حاليًا، فسيكون إصدار المسودة لهذا التكوين مرئيًا على علامة التبويب السريعة **الإصدارات** من صفحة **التكوينات** (**مسؤول المؤسسة** > **إعداد التقارير الإلكترونية** > **التكوينات‏‎**). يمكنك تحديد إصدار المسودة من التكوين و[تعديل](er-quick-start2-customize-report.md#ConfigureDerivedFormat) محتواه من خلال استخدام مصمم التقارير الإلكترونية المناسب. عندما تنتهي من تحرير إصدار المسودة لتكوين التقارير الإلكترونية، لن يعود محتواه مطابقًا لمحتوى الإصدار الأعلى من هذا التكوين في مثيل Finance الحالي. لمنع فقدان التغييرات التي أجريتها، يعرض النظام رسالة خطأ تفيد بتعذر متابعة عملية الاستيراد لإن إصدار هذا التكوين أعلى من أعلى إصدار من هذا التكوين في مثيل Finance الحالي. عند حدوث ذلك، علي سبيل المثال، تكوين التنسيق **X**، تظهر رسالة الخطأ **إصدار التنسيق 'X' غير مكتمل**.

للتراجع عن التغييرات التي أجريتها في إصدار المسودة، حدد الإصدار الأعلى المكتمل أو المشترك لتكوين التقارير الإلكترونية في Finance على علامة التبويب السريعة **الإصدارات**، ثم حدد **الحصول على هذا الإصدار**. يتم نسخ محتوى الإصدار المحدد إلى إصدار المسودة.

## <a name="applicability-consideration"></a>النظر في إمكانية التطبيق

عند تصميم إصدار جديد من تكوين ER، يمكنك تعريف [التبعية](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) الخاصة به على مكونات البرامج الأخرى. تعتبر هذه الخطوة مطلبًا أساسيًا للتحكم في تنزيل إصدار التكوين هذا من مستودع التقارير الإلكترونية أو ملف XML خارجي ولأي استخدام إضافي لهذا الإصدار. عند محاولة استيراد إصدار جديد من تكوين ER، يستخدم النظام المتطلبات الأساسية المكونة للتحكم فيما إذا كان يمكن استيراد الإصدار.

في بعض الحالات، قد تتطلب أن يتجاهل النظام المتطلبات الأساسية المكونة عند استيراد إصدارات جديدة من تكوينات ER. لجعل النظام تجاهل المتطلبات الأساسية أثناء الاستيراد اتبع الخطوات التالية.

1. انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.
2. في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.
3. تعيين الخيار **تخطي تحديثات المنتج والإصدار المطلوب مسبقا أثناء الاستيراد** إلى **نعم**.

    > [!NOTE]
    > هذه المعلمة خاصة بالمستخدم والشركة.

## <a name="dependencies-on-other-components"></a>التبعيات علي المكونات الأخرى

يمكن تكوين تكوينات التقارير الإلكترونية على أنها [تعتمد](er-download-configurations-global-repo.md#import-filtered-configurations) على تكوينات أخرى. علي سبيل المثال ، يمكنك [استيراد تكوين](er-download-configurations-global-repo.md) [نموذج البيانات الخاص بـER](er-overview-components.md#data-model-component) من المستودع العمومي إلى [Microsoft Regulatory Configuration Services (RCS)](../../../finance/localizations/rcs-overview.md) أو مثيل Dynamics 365 Finance، ثم قم بإنشاء تكوين ER [جديد](er-overview-components.md#format-component) وهو [مشتق](er-quick-start2-customize-report.md#DeriveProvidedFormat) من تكوين نموذج بيانات التقارير الإلكترونية المستوردة. سيعتمد تكوين تنسيق التقارير الإلكترونية المشتق على تكوين نموذج بيانات التقارير الإلكترونية الأساسي.

![تكوين تنسيق التقارير الإلكترونية المشتق في صفحة التكوينات.](./media/ger-configuration-lifecycle-img1.png)

عند الانتهاء من تصميم التنسيق ، يمكنك تغيير حالة الإصدار الأولي لتكوين تنسيق التقارير الإلكترونية من **مسودة** إلى **مكتمل**. يمكنك بعد ذلك مشاركة الإصدار المكتمل من تكوين تنسيق التقارير الإلكترونية عن طريق [النشر](../../../finance/localizations/rcs-global-repo-upload.md) إلى المستودع العالمي. بعد ذلك ، يمكنك الوصول إلى المستودع العالمي من أي مثيل لـ RCS أو Finance. يمكنك بعد ذلك استيراد أي إصدار من إصدارات تكوين التقارير الإلكترونية ينطبق على التطبيق من المستودع العام إلى هذا التطبيق.

![تكوين تنسيق التقارير الإلكترونية المنشور في صفحة مستودع التكوين.](./media/ger-configuration-lifecycle-img2.png)

استنادًا إلى تبعية التكوين، عند تحديد تكوين تنسيق التقارير الإلكترونية في المستودع العام لاستيراده إلى RCS أو مثيل Finance الذي تم نشره حديثًا، يتم العثور على تكوين نموذج بيانات التقارير الإلكترونية الأساسي تلقائيًا في المستودع العام واستيراده مع تنسيق التقارير الإلكترونية المحدد التكوين باعتباره التكوين الأساسي.

يمكنك أيضًا تصدير إصدار تكوين تنسيق التقارير الإلكترونية من RCS أو مثيل Finance الحالي وتخزينه محليًا كملف XML.

![تصدير إصدار تكوين تنسيق التقارير الإلكترونية على هيئة XML في صفحة التكوين.](./media/ger-configuration-lifecycle-img3.png)

في إصدارات Finance **قبل الإصدار 10.0.29**، عند محاولة استيراد إصدار تكوين تنسيق التقارير الإلكترونية من ملف XML هذا أو من أي مستودع بخلاف المستودع العام إلى مخزن حديث تم نشر مثيل RCS أو Finance الذي لا يحتوي حتى الآن على أي تكوينات ER ، سيتم طرح الاستثناء التالي لإعلامك بأنه لا يمكن الحصول على التكوين الأساسي:

> المراجع التي لم يتم حلها الباقية<br>
لا يمكن تحديد مرجع الكائن "\<imported configuration name\>" إلى الكائن "\<globally unique identifier of the missed base configuration\>" (\<version of the missed base configuration\>)

![استيراد إصدار تكوين تنسيق التقارير الإلكترونية في صفحة مستودع التكوين.](./media/ger-configuration-lifecycle-img4.gif)

في الإصدار **10.0.29 والإصدارات الأحدث**، عندما تحاول إجراء استيراد التكوين نفسه، إذا تعذر العثور على التكوين الأساسي في مثيل التطبيق الحالي أو في المستودع المصدر الذي تستخدمه حاليًا (إذا كان ذلك ممكنًا)، سيحاول إطار عمل إعداد التقارير الإلكترونية تلقائيًا العثور على اسم التكوين الأساسي المفقود في مخزن المستودع العمومي المؤقت. سيقدم بعد ذلك الاسم والمعرف الفريد العمومي (GUID) للتكوين الأساسي المفقود في نص الاستثناء الذي تم طرحه.

> المراجع التي لم يتم حلها الباقية<br>
لا يمكن تحديد مرجع الكائن '\<imported configuration name\>' إلى ‏‫الكائن الأساسي (\<name of the missed base configuration\> \<globally unique identifier of the missed base configuration\>,\<version of the missed base configuration\>)

![استثناء في صفحة مستودع التكوين عندما يتعذر العثور على التكوين الأساسي.](./media/ger-configuration-lifecycle-img5.png)

يمكنك استخدام الاسم المقدم للعثور على التكوين الأساسي ثم استيراده يدويًا.

> [!NOTE]
> يعمل هذا الخيار الجديد فقط عندما يقوم مستخدم واحد على الأقل بتسجيل الدخول بالفعل إلى المستودع العمومي باستخدام [‏‫صفحة مستودعات التكوين](er-download-configurations-global-repo.md#open-configurations-repository) أو أحد حقول [بحث](er-extended-format-lookup.md) المستودع العام في نسخة Finance الحالية، وعندما يتم تخزين محتوى المستودع العام في الذاكرة المخبئية.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على إعداد التقارير الإلكترونية (ER)](general-electronic-reporting.md)

[تحديد تبعية تكوينات التقارير الإلكترونية في المكونات الأخرى](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

