---
title: إنشاء أوامر تحويل من تطبيق المستودع
description: يوضح هذا المقال كيفيه إنشاء أوامر تحويل ومعالجتها من تطبيق إدارة المستودع للأجهزة المحمولة
author: perlynne
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 45cbf7aca431c19e58de75355579304baef3cf7d
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336444"
---
# <a name="create-transfer-orders-from-the-warehouse-app"></a>إنشاء أوامر تحويل من تطبيق المستودع

[!include [banner](../includes/banner.md)]

تتيح هذه الميزة للعاملين إنشاء أوامر تحويل ومعالجتها مباشرةمن تطبيق إدارة المستودع للأجهزة المحمولة. ويبدأ العامل عن طريق تحديد مستودع الوجهة، ثم يمكنهم مسح لوحه ترخيص واحده أو أكثر باستخدام التطبيق لأضافه لوحات الترخيص إلى أمر التحويل. عندما يحدد عامل المستودع **الطلب الكامل**، تقوم وظيفة المجموعة بإنشاء أمر التحويل وبنود الأمر المطلوبة بناء علي المخزون الفعلي الذي تم تسجيله لألواح الترخيص هذه.

## <a name="turn-on-this-feature-and-its-prerequisites"></a><a name="enable-create-transfer-order-from-warehouse-app"></a>قم بتشغيل هذه الميزة ومتطلباتها الأساسية

قبل أن تتمكن من استخدام هذه الميزة، يجب تمكينها وتمكين متطلباتها الأساسية على النظام. بإمكان المسؤولين استخدام صفحة [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتمكينها إذا لزم الأمر.

1. استخدم مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتمكين الميزات التالية (بالترتيب): اعتبارًا من الإصدار 10.0.25 من Supply Chain Management، يتم تشغيل هاتين الميزتين افتراضيًا.
    1. *معالجة أحداث تطبيق المستودع*<br>(اعتبارًا من الإصدار 10.0.29 من Supply Chain Management، هذه الميزة إلزامية ولا يمكن إيقاف تشغيلها.)
    1. *إنشاء أوامر تحويل ومعالجتها من تطبيق المستودع*<br>(اعتبارًا من الإصدار 10.0.29 من Supply Chain Management، هذه الميزة إلزامية ولا يمكن إيقاف تشغيلها.)
1. لتنفيذ معالجه الشحنات الصادرة تلقائيًا، يجب أيضًا تمكين الميزة [*تأكيد الشحنات الصادرة من الوظائف الدفعية*](confirm-outbound-shipments-from-batch-jobs.md) feature. اعتبارًا من الإصدار 10.0.21 من Supply Chain Management، يتم تشغيل هذه الميزة افتراضيًا. هذه الميزة إلزامية ولا يمكن إيقاف تشغيلها، اعتبارًا من Supply Chain Management 10.0.25.

## <a name="set-up-a-mobile-device-menu-item-to-create-transfer-orders"></a><a name="setup-warehouse-app-menu"></a>إعداد صنف قائمة الأجهزة المحمولة لإنشاء أوامر التحويل

فيما يلي إرشادات عامه حول اعداد عنصر قائمه الجهاز المحمول لإنشاء أمر التحويل. وفقا لمتطلبات العمل الخاصة بك لمستوي التنفيذ التلقائي المطلوب تعيينه عند قيام المستخدمين بإنشاء أوامر التحويل من الارضيه، سيتم تمكين عمليات تكوين مختلفه. سيصف السيناريو في هذا المستند عمليه التكوين الأخرى.

1. انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.
1. حدد **جديد** لإضافة عنصر قائمة جديد. ثم قم بالإعدادات التالية لبدء الاستخدام:

    - **اسم عنصر القائمة** - تعيين اسم كما يجب ان يظهر في Supply Chain Management.
    - **العنوان** - تعيين اسم القائمة كما يجب تقديمه للعاملين في تطبيق إدارة المستودع للأجهزة المحمولة.
    - **الوضع** - يتم تعيينه إلى *غير مباشر* (لن يقوم عنصر القائمة هذا بإنشاء عمل).
    - **كود النشاط** - تعيين على *إنشاء أمر تحويل من لوحات الترخيص* لتمكين عمال المستودع من إنشاء أمر تحويل استنادا إلى لوحه ترخيص ممسوحة ضوئيا أو أكثر.

1. استخدم اعداد **النهج إنشاء سطر أمر التحويل** للتحكم في كيفيه إنشاء بنود أمر التحويل بواسطة عنصر القائمة هذا. سوف يتم إنشاء/تحديث الخطوط استنادًا إلى المخزون الموجود والمسجل للوحات الترخيص الممسوحة ضوئيًا. اختر إحدى القيم التالية:

    - **عدم الحجز** - لن يتم حجز سطور أمر التحويل.
    - **لوحه الترخيص الموجهة بحجز البنود** – سيتم حجز سطور أمر التحويل واستخدام خيار الاستراتيجية الموجهة للوحه الترخيص، والذي يقوم بتخزين المعرفات الخاصة بلوح الترخيص المناسبة المرتبطة ببنود الأمر. ولذلك يمكن استخدام قيم معرف لوحة الترخيص الموجود كجزء من عملية إنشاء العمل لخطوط أمر التحويل.

1. استخدم اعداد **نهج الشحنة الصادر** لأضافه مزيد من التنفيذ التلقائي إلى عمليه الشحن لأمر التحويل الصادر، حسب الحاجة. عندما يختار العامل الزر **إكمال الأمر**، ينشئ التطبيق حدث تطبيق المستودع *إكمال الأمر* الذي سيطبق قيمة الحقل **سياسة الشحن الصادر** لجميع البنود في أمر التحويل الحالي. وبعد ذلك، عند معالجه قائمه انتظار الحدث بواسطة مهمة مجموعه لإنشاء أمر التحويل، يمكن قراءه القيمة المخزنة في هذا الحقل بواسطة وظيفة المجموعة، التالي يمكن التحكم في كيفيه معالجه الوظيفة لكل بند. اختر واحدًا مما يلي:

    - **بلا** - لم يتم اجراء المعالجة التلقائية.
    - **إصدار إلى المستودع** - يقوم باتمته الإصدار لعمليه المستودع.
    - **تاكيد الشحن** - أتمته عمليه تاكيد الشحن.
    - **تاكيد الطرح والشحن** - يقوم بأتمتة كل من عمليات الإصدار إلى المستودع وتاكيد الشحن.

## <a name="add-the-mobile-device-menu-item-to-a-menu"></a>إضافة عنصر قائمة جهاز محمول إلى قائمة

1. انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> قائمة الجهاز المحمول**.
1. حدد **تحرير**.
1. حدد قائمه موجودة بعد تحديد القائمة الجديدة الموجودة في **القوائم وعناصر القوائم المتوفرة**. قم باضافه عنصر القائمة عن طريق تحديد الزر سهم لليمين.

## <a name="create-a-transfer-order-based-on-license-plates"></a>إنشاء أمر تحويل بناء علي ألواح الترخيص

يتضمن تطبيق إدارة المستودع للأجهزة المحمولة عمليه بسيطه لإنشاء أوامر التحويل استنادا إلى لوحات الترخيص. للقيام بذلك، يقوم العامل بما يلي باستخدام تطبيق إدارة المستودع للأجهزة المحمولة:

1. قم بإنشاء أمر التحويل وتحديد مستودع الوجهة.
1. حدد كل لوحه ترخيص ليتم شحنها.
1. حدد **أمر مكتمل**.

>[!NOTE]
> يمكن لعده عاملين تعيين لوحات الترخيص المخصصة لنفس أمر التحويل وذلك باستخدام الزر **تحديد أمر تحويل** لتحديد رقم أمر تحويل موجود وغير معالج من قائمه انتظار احداث تطبيق المستودع. للحصول علي معلومات حول كيفيه العثور علي قيم أرقام أمر التحويل ، راجع [الاستعلام عن احداث تطبيق المستودع](#inquire-the-warehouse-app-events).

## <a name="example-scenario"></a>سيناريو كمثال

يقدم هذا السيناريو نظره عامه علي العملية الخاصة بالحصول علي أوامر التحويل التي تم إنشاؤها ومعالجتها تلقائيا بناء علي المخزون الفعلي المسجل في لوحات الترخيص المحددة.

للعمل من خلال هذا السيناريو باستخدام القيم المقترحة، يجب العمل علي نظام يحتوي علي بيانات العرض التوضيحي مثبته وحدد الكيان القانوني *USMF* قبل البدء.

ويفترض هذا السيناريو انك قد قمت بالفعل بتمكين [إنشاء أوامر التحويل ومعالجتها من ميزه تطبيق المستودع ](#enable-create-transfer-order-from-warehouse-app)، وقدرة [معالجه حدث المستودع](warehouse-app-events.md).

بالاضافه إلى اعداد إنشاء أمر التحويل في عناصر قائمه الجهاز المحمول، يجب أيضا اعداد القوالب الاضافيه وتوجيهات المواقع وكذلك وظائف المجموعات وتمكينها.

### <a name="example-scenario-blueprint"></a>مثال لمخطط السيناريو

أنت بائع تجزئه ولديك عده لوحات ترخيص، وتحتوي كل منها علي مزيج من الأصناف الموضوعة في موقع معين داخل أحد المستودعات الخاصة بك ( *المستودع 51*). ترغب في تمكين العملية التي تتيح للعاملين إنشاء أمر تحويل إلى مستودع آخر ( *المستودع 61*) لمجموعه من لوحات الترخيص الممسوحة ضوئيا. ستقوم تلقائيا بشحن-تحديث أمر التحويل بمجرد تحديد لوح الترخيص الأخير للأمر.

![مثال عملية أمر تحويل مؤتمت.](media/create-transfer-order-from-app-example.png "مثال عمليه أمر تحويل مؤتمت")

### <a name="create-a-mobile-device-menu-item-for-creating-transfer-orders"></a>إنشاء عنصر قائمة الأجهزة المحمولة لإنشاء أوامر التحويل

يوضح هذا القسم كيفيه إنشاء عنصر قائمه جهاز محمول جديد لإنشاء أوامر التحويل. قم بتعيين **الوضع** علي *غير مباشر* و **كود النشاط** على *إنشاء أمر تحويل من لوحات الترخيص*.

1. انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.
1. حدد **جديد**.
1. في الحقل **اسم عنصر القائمة**، ادخل الاسم *إنشاء إلى*.
1. في حقل **العنوان** ، ادخل وصف *الإنشاء الى*.
1. في الحقل **الوضع**، حدد *غير مباشر*.
1. في **كود النشاط**، حدد *إنشاء أمر تحويل من ألواح الترخيص*
1. في **نهج إنشاء سطر الأمر**، حدد *لوحه الترخيص الموجهة بحجز البنود*.
1. في **نهج الشحنة الصادرة**، حدد *تاكيد الإصدار والشحن*.
1. انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> قائمة الجهاز المحمول**.
1. حدد **تحرير**.
1. حدد قائمه **المستودع** بعد تحديد عنصر القائمة الجديد الموجود في **القوائم وعناصر القوائم المتوفرة**. قم باضافه عنصر القائمة إلى قائمة **المخزون** عن طريق تحديد الزر سهم لليمين.

### <a name="set-up-work-templates-to-auto-process-and-break-work-by-located-license-plate"></a>اعداد قوالب العمل لمعالجتها تلقائيا وتقسيم العمل باستخدام لوح الترخيص الموضوع

يوضح هذا القسم كيفيه تمكين قالب عمل لمعالجه العمل تلقائيا والذي تم إنشاؤه بواسطة القالب عند تحرير الموجة.

1. انتقل إلى **إدارة المستودعات \> إعداد \> عمل \> قوالب العمل**.
1. في الحقل **نوع أمر العمل**، حدد *مشكلة التحويل*.
1. حدد **جديد**، لإنشاء قالب عمل.
1. في حقل **قالب العمل**، قم بإدخال *51 Auto process LP*.
1. في حقل **وصف قالب العمل**، قم بإدخال *51 Auto process LP*.
1. حدد خانه الاختيار **معالجه تلقائية**. ويجب تحديد هذا الأمر لمعالجه أيه خطوات تنفيذ تلقائي.
1. في بيانات العرض التوضيحي ، يوجد بالفعل قالب عمل *نقل 51*، قم بتحرير الحقل **رقم التسلسل** بحيث يكون لقالب العمل الجديد رقم تسلسل اقل من قالب العمل الموجود *نقل 51*.
1. حدد **حفظ** شريط الأدوات لتمكين إتاحة علامة التبويب السريعة **تفاصيل قالب العمل**.
1. في علامة التبويب السريعة **تفاصيل قالب العمل** حدد **جديد** في شريط الأدوات. ستقوم باضافه بندين.
1. في الحقل **نوع العمل**، حدد *انتقاء*.
1. في الحقل **معرف فئة العمل**، حدد *TransfOut*.
1. حدد **جديد**، في شريط أدوات **تفاصيل قالب العمل**.
1. في الحقل **نوع العمل**، حدد *تم وضعه*.
1. في الحقل **معرف فئة العمل**، حدد *TransfOut*.
1. حدد **حفظ** لتمكين حقل **رمز التوجيه**.
1. في **نوع العمل** بند *الوضع*، حدد **كود الموجه** *Baydoor*. تاكد من حصول قالب العمل الجديد هذا علي اقل **رقم تسلسل**.
1. في شريط الأدوات، حدد **تحرير الاستعلام** لفتح محرر الاستعلام.
1. في علامة التبويب **نطاق**، حدد **إضافة**.
1. علي البند المضاف ، في **الحقل** حدد *مستودع*.
1. في الحقل **المعايير**، حدد *51*.
1. حدد علامة تبويب **الفرز**.
1. حدد **إضافة** واضبط **الحقل** على *معرف لوح الترخيص الموجود*. يؤدي تحديد هذا الحقل إلى تمكين زر شريط الادوات **فواصل راس عمل**.
1. حدد **موافق** متبوعا **بنعم** لأعاده تعيين التجميع والعودة إلى صفحه **قوالب العمل**.
1. حدد **فواصل راس العمل** وقم بتمكين **التجميع حسب هذا الحقل** لـ **معرف لوح الترخيص الذي تم تحديده** وإغلاقه.

> [!NOTE]
> ليس من الممكن معالجه كافة الإعدادات تلقائيا، علي سبيل المثال، أصناف وزن الصنف واستخدام ابعاد التعقب المختلطة.

### <a name="set-up-location-directives-for-the-license-plate-guided-strategy"></a>اعداد توجيهات المواقع لاستراتيجية المعالج الموجه للوحه الترخيص

يوضح هذا القسم كيفيه اعداد عمليه الانتقاء الموجه للموقع لاستخدام استراتيجية **لوحه الترخيص الموجهة**.

1. انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.
1. حدد **تحرير**.
1. في راس قائمه التنقل، حدد **نوع أمر العمل** *إصدار عمليه تحويل*.
1. في قائمه التنقل، حدد الموقع الموجود التوجيه **51 للانتقاء**.
1. في علامة التبويب السريعة **البنود**، حدد خانه الاختيار **السماح بالتقسيم**.
1. في علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد **جديد** لإضافة سطر جدبد.
1. في حقل **الاسم**، أدخل *‏‫LP Guided‬*.
1. في الحقل **الاستراتيجية**، حدد *لوحة ترخيص موجهة*. يحتاج هذا الاجراء إلى اقل رقم تسلسل.
1. حدد **حفظ** في شريط الأدوات.
1. حدد أيقونه صفحة **التحديث** من شريط الادوات.
1. في علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد السطر الخاص بالإجراء *TOPick*.
1. في شريط أدوات **الإجراءات الموجه للموقع**، حدد **تحريك لأسفل** لتغيير الرقم التسلسلي ليكون أكبر من رقم التسلسل للاجراء *LP الموجه* الذي تم إنشاؤه للتو.

> [!NOTE]
> ستحاول استراتيجية دفتر التراخيص الارشاديه حجز عمل الانتقاء وإنشاءه مقابل المواقع التي تحتفظ بألواح الترخيص المطلوبة التي تم اقرانها ببنود أمر التحويل. ولكن إذا لم يكن ذلك ممكنا وكانت لا تزال ترغب في إنشاء عمل الانتقاء ، فيجب العودة إلى استراتيجية اجراء التوجيه لموقع آخر، وربما تقوم أيضا بالبحث عن مخزون في منطقه أخرى بالمستودع، وذلك وفقا لاحتياجات العملية التجارية الخاصة بك.

### <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>اعداد مهمة دُفعة لمعالجه احداث التطبيق الخاص بالمستودع

يوضح هذا القسم كيفيه اعداد وظيفة مجموعه مجدولة لمعالجه احداث التطبيق الخاصة بالمستودع.

1. انتقل إلى **إدارة المستودعات‬ \> المهام الدورية \> أحداث تطبيق مستودع العملية**.
2. في مربع الحوار ، قم بتمكين **معالجه المجموعة** ضمن المقطع **تشغيل في الخلفية**.
3. حدد **تكرار** وقم باعداد وظيفة المجموعة لمعالجتها استنادا إلى الفترة المطلوبة لأعمالك.
4. حدد **موافق** للعودة إلى مربع الحوار الرئيسي.
5. حدد **موافق** في مربع الحوار الرئيسي لأضافه الوظيفة إلى قائمه انتظار المجموعة.

### <a name="set-up-a-batch-job-to-release-transfer-orders-automatically"></a>إعداد وظيفة دفعية لإصدار أوامر النقل تلقائيًا

يوضح هذا القسم كيفيه اعداد وظيفة مجموعه مجدولة لإصدار أوامر التحويل التي تم وضع علامة "جاهز للتحرير" عليها.

1. انتقل إلى **إدارة المستودعات \> الإصدار إلى المستودع \> الإصدار التلقائي لأوامر التحويل**.
1. في مربع الحوار ، قم بتوسيع المقطع **السجلات المطلوب تضمينها**.
1. ضمن قسم **السجلات المُراد تضمينها**، حدد **تصفية**.
1. في صفحة الاستعلام **WHSTransferAutoRTWQuery**، علامة التبويب **نطاق**، حدد **أضافه** لأضافه بند جديد إلى الاستعلام.
1. في الحقل **جدول**  السطر الجديد، حدد القائمة المنسدلة وحدد الجدول **إصدار سطر التحويل إلى المستودع**.
1. في القائمة المنسدلة **الحقل**، حدد‏‎ **سياسة الشحن الصادر**
1. في حقل **المعايير**، حدد **تاكيد الإصدار والشحن**.
1. في البند حيث تم تعيين **الحقل** علي *من المستودع*، في الحقل **المعايير**، حدد *51*.
1. حدد **موافق** للعودة إلى مربع الحوار الرئيسي.
1. قم بتوسيع القسم **التشغيل في الخلفية** لإعداد المعالجة الدُفعية‬.
1. قم بتمكين **معالجه المجموعة** ضمن المقطع **تشغيل في الخلفية**.
1. حدد **تكرار** وقم باعداد وظيفة المجموعة لمعالجتها استنادا إلى الفترة المطلوبة لأعمالك.
1. حدد **موافق** للعودة إلى مربع الحوار الرئيسي.
1. حدد **موافق** في مربع الحوار الرئيسي لأضافه وظيفة المجموعة إلى قائمه انتظار المجموعة.

### <a name="set-up-the-process-outbound-shipment-batch-job"></a>اعداد وظيفة مجموعه "معالجه الشحن الصادر"

يوضح هذا القسم كيفيه اعداد مهمة مجموعه مجدولة لتشغيل تاكيد الشحن الصادر لعمليات التحميل الجاهزة للشحن المرتبطة ببنود أمر التحويل التي تكون "جاهزه للشحن".

1. انتقل إلى **إدارة المستودعات‬ \> المهام الدورية \> معالجة الشحنات الصادرة**.
1. وسّع القسم **السجلات المطلوب تضمينها**.
1. حدد **عامل تصفية**.
1. في الاستعلام **WHSLoadShipConfirm**، حدد علامة التبويب **الصلات**.
1. قم بتوسيع التسلسل الهرمي للجداول بحيث يكون **الحمولات** و **تفاصيل التحميل** موسعان.
1. حدد الجدول **تفاصيل التحميل**.
1. حدد زر **أضافه صله جدول**.
1. في قائمه علاقات الجداول، قم بتصفية أو البحث في عمود **العلاقة** لعمود *بنود أمر التحويل (مرجع)*.
1. قم بالتركيز علي علاقة الجدول في القائمة ثم اضغط علي الزر **تحديد**.
1. حدد جدول **سطور أمر التحويل**.
1. حدد زر **أضافه صله جدول**.
1. في قائمه علاقات الجداول، قم بتصفية أو البحث في عمود **العلاقة** لـ *إنشاء حقول إضافية للتحويل (معرف التسجيل)*.
1. قم بالتركيز علي علاقة الجدول في القائمة ثم اضغط علي الزر **تحديد**.
1. حدد علامة التبويب **النطاق**.
1. في جداول استعلام **النطاق**، ستقوم باعداد ثلاثه نطاقات لمعايير الاستعلام. حدد الزر **إضافة** لإضافة سطر.
1. قم باضافه نطاق لجدول **التحميلات**. قم بتعيين **الحقل** على *حاله التحميل* وقم بتعيين **المعايير** على *تم تحميله*.
1. أضافه نطاق آخر للجدول **إنشاء حقول إضافية للتحويل**. قم بتعيين **الحقل** إلى *سياسة الشحن الصادر* وتعيين **المعايير** إلى *تاكيد الإصدار والشحن*.
1. أضافه نطاق آخر للجدول **تفاصيل التحميل**. قم بتعيين **الحقل** إلى *مرجع* وتعيين **المعايير** إلى *شحن أمر التحويل*.
1. حدد **موافق** للعودة إلى مربع الحوار الرئيسي.
1. وسّع القسم **تشغيل في الخلفية‬‬**.
1. قم بتمكين **معالجة المجموعة**.
1. حدد **تكرار** وقم باعداد وظيفة المجموعة لمعالجتها استنادا إلى الفترة المطلوبة لأعمالك.
1. حدد **موافق** للعودة إلى مربع الحوار الرئيسي.
1. حدد **موافق** في مربع الحوار الرئيسي لأضافه وظيفة المجموعة إلى قائمه انتظار المجموعة.

> [!NOTE]
> لمزيد من المعلومات، راجع [تأكيد الشحنات الصادرة من وظائف المجموعة](confirm-outbound-shipments-from-batch-jobs.md).

## <a name="processing-the-example-for-create-transfer-order-from-the-warehouse-app"></a>معالجه المثال لـ "إنشاء أمر تحويل من تطبيق المستودع"

### <a name="add-on-hand-on-a-license-plate"></a>أضافه الكمية الحالية علي لوحه الترخيص

كنقطه بداية لهذا السيناريو، ستحتاج إلى وجود لوحه ترخيص تحتوي علي مخزون متوفر فعلي.

| الصنف | المستودع | حالة المخزون |  الموق | لوحة الترخيص | الكمية |
| --- | --- | --- | --- | --- | --- |
| A0001 | 51 | متوفر‬ة | LP-010 | LP10 | 1 |
| A0002 | 51 | متوفر‬ة | LP-010 | LP10 | 2 |

إضافه كميات الأصناف إلى المخزون الفعلي من خلال استخدام القيم التالية:

> [!NOTE]
> ستحتاج إلى إنشاء لوحه الترخيص واستخدام المواقع التي تسمح لك بتنفيذ الأصناف المختلطة، مثل LP-010.

### <a name="create-and-process-transfer-orders-from-the-warehouse-app"></a>إنشاء أوامر تحويل ومعالجتها من تطبيق المستودع

1. افتح التطبيق وقم بتسجيل الدخول باعتبارك المستخدم *51*. سيكون مستودع المستخدمين الحالي 51.
1. حدد عنصر القائمة **إنشاء إلى** من موقع القائمة الذي قمت بإضافته اليها اثناء الاعداد.
1. ابدأ إنشاء أمر تحويل من خلال إدخال مستودع الوجهة (إلى المستودع) في الحقل **المستودع**، ادخل *61*. سيتم الانتقال إلى أمر التحويل الجديد من المستودع 51 (من المستودع) إلى مستودع الوجهة *61*.
1. حدد **موافق**.
1. مسح معرف لوح الترخيص في **حقل لوحه الترخيص**. ادخل لوحه الترخيص الخاصة بالمخزون المضافة في خطوه سابقه، *LP10*.
1. حدد **موافق**.
1. حدد زر القائمة ثم حدد **الأمر مكتمل** لإنهاء إنشاء أمر تحويل تطبيق المستودع.

بالنسبة للمثال المذكور، يتم استخدام اثنين من **احداث تطبيق المستودع** (*إنشاء أمر تحويل* و *أمر تحويل مكتمل*).

### <a name="inquire-the-warehouse-app-events"></a><a name="#inquire-the-warehouse-app-events"></a>الاستعلام عن احداث تطبيق المستودع

يمكنك عرض قائمه انتظار الاحداث ورسائل الاحداث التي تم إنشاؤها بواسطة تطبيق إدارة المستودع للأجهزة المحمولة عن طريق الانتقال إلى **استعلامات أداره المستودعات \> الاستعلامات والتقارير \> سجلات الاجهزه المحمولة \> احداث تطبيق مستودع**.

ستتلقى رسائل حدث *إنشاء أمر التحويل* حاله *الانتظار*، والتي تعني ان وظيفة مجموعه **معالجة مناسبات تطبيق المستودع** لن تلتقط وتعالج رسائل الحدث. بمجرد تحديث رسالة الحدث إلى الحالة *في قائمه الانتظار*، تقوم وظيفة المجموعة بمعالجه الاحداث. سيحدث هذا في نفس الوقت الذي يتم فيه إنشاء حدث *أمر التحويل الكامل* (عندما يقوم العامل بتحديد الزر **الطلب الكامل** في تطبيق إدارة المستودع للأجهزة المحمولة). عند معالجه رسائل حدث *إنشاء أمر التحويل*، يتم تحديث الحالة إلى *مكتملة* أو *فاشلة*. عند تحديث حاله *أمر التحويل الكامل* إلى *مكتمل*، يتم حذف كافة الاحداث المرتبطة من قائمه الانتظار.

ونظرا لأنه لن تتم معالجه **احداث تطبيق المستودع** الخاصة بإنشاء بيانات أمر التحويل بواسطة وظيفة المجموعة قبل ان يتم تحديث الرسائل إلى الحالة *في قائمه الانتظار*، فسوف تحتاج إلى البحث عن أرقام أوامر التحويل المطلوبة كجزء من حقل **المعرف**. يقع حقل **المعرف** في راس صفحه **احداث تطبيق المستودع**.

وكجزء من معالجه حدث المستودع، قد يفشل إنشاء سطر أمر التحويل. في هذه الحالة، يتم تحديث حاله رسالة الحدث إلى *فاشلة* ويمكنك استخدام معلومات **سجل الدُفعة** لمعرفه السبب واتخاذ اجراء ما لحل إيه مشكلات.

قد ترتبط المشكلات النموذجية بالاعداد المفقود للعملية، مثل مستودع بضاعة بالطريق مفقود لحدث *إنشاء أمر التحويل*. وفي مثل هذه الحالة، يمكنك أضافه مستودع بضاعة بالطريق إلى مستودع الشحن واستخدام خيار **أعاده التعيين** لتغيير الحالة الخاصة بكافة رسائل احداث تطبيق المستودع من *فاشلة* إلى *في قائمة الانتظار*، مما يعني ان وظيفة المجموعة ستقوم بمعالجه رسائل الحدث مره أخرى بعد تصحيح بيانات الاعداد.

في بيئات الإنتاج، قد تكون الاستثناءات ذات صله بالعملية، مثل وجود لوحه ترخيص مطلوبه، والتي تكون فارغة في وقت معالجه وظيفة الدُفعة وبالتالي لا يتم إنشاء بنود أمر تحويل. يمكن أزاله رسالة الحدث الفاشل هذه باستخدام الخيار **حذف** أو يمكنك أضافه الكمية الفعلية الفعلية إلى لوحه الترخيص واستخدام خيار **أعاده التعيين** لكافة رسائل الاحداث ذات الصلة.

لمزيد من المعلومات، راجع [معالجه حدث تطبيق المستودع](warehouse-app-events.md).

### <a name="follow-up-on-the-example-scenario-processing"></a>متابعه في مثال معالجه السيناريو

خلال هذا السيناريو، يتم إجراء الأحداث التالية:

1. باستخدام تطبيق إدارة المستودع للأجهزة المحمولة، قمت بتحديد عنصر قائمه يستخدم كود النشاط **إنشاء أمر تحويل من لوحات الترخيص**.
1. يطالبك التطبيق بتحديد المستودع الوجهة لأمر التحويل. دائما ما يكون المستودع المصدر هو المستودع الذي قمت بتسجيل الدخول اليه حاليا كعامل.
1. في تحديد المستودع الوجهة ، قام النظام بحجز رقم معرف لأمر التحويل القادم (استنادا إلى التسلسل الرقمي لأمر التحويل المعرف في النظام لديك) ولكنه لم يقم بإنشاء أمر التحويل بعد.
1. عند مسح لوح الترخيص *LP10* الذي يحتوي علي المخزون الفعلي الذي ينبغي نقله إلى المستودع الجديد، تتم أضافه **حدث تطبيق المستودع** إلى قائمه انتظار الاحداث التي ستتم معالجتها لاحقا. يحتوي حدث المستودع علي تفاصيل الرسالة الخاصة بالفحص، بما في ذلك رقم أمر التحويل المقصود.
1. في تطبيق إدارة المستودع للأجهزة المحمولة عند تحديد الزر **الأمر الكامل**، يتم إنشاء حدث تطبيق مستودع جديد، **أمر تحويل كامل**، والحدث الموجود ذي الصلة، **وإنشاء أمر تحويل**، وتغيير الحاله إلى **في قائمه الانتظار**.
1. وفي النهاية الخلفية، تقوم **مهمة دُفعة احداث التطبيق الخاصة بمستودع العملية** بانتقاء الحدث **في قائمه الانتظار** وتجميع الكمية الفعلية المرتبطة بلوحه الترخيص الممسوحة ضوئيا. استنادا إلى الكمية الفعلية التي تم إنشاء سجل أمر التحويل الفعلي عليها والبنود المرتبطة. تقوم الوظيفة أيضا بملء حقل **سياسة الشحنة الصادرة** لأمر التحويل بالقيمة التي تستند إلى *الإصدار المكون وتاكيد الشحن* والمرتبط بلوحه الترخيص الخاصة ببنود استراتيجية **الموجهة للوحة الترخيص**.
1. بناء علي سطر أمر التحويل لقيمه حقل **سياسة الشحن الخارجي**، تسبب **الإصدار التلقائي لاستعلام الوظيفة الدفعيه الخاص بأوامر التحويل** الآن نتج عنه إصدار أمر التحويل إلى مستودع الشحن. وبسبب اعداد **قالب الموجة** المستخدم، و **قالب العمل**، و **توجيهات الموقع** المستخدمة للعمليات التلقائية الناتجة عن العمل تم تحديث **حاله التحميل** إلى *محمل*.
1. يتم تنفيذ **عملية مهمة الدُفعة للشحنات الخارجية** للتحميل، مما يؤدي إلى شحن أمر التحويل وإنشاء اشعار الشحن المقدم (ASN).
1. يعتمد توقيت كافة هذه الاحداث علي إعدادات **التكرار** لوظائف الدُفعة التي تم إنشاؤها.

## <a name="frequently-asked-questions"></a>الأسئلة المتداولة

### <a name="mobile-device-menu-item-setup"></a>إعداد عنصر قائمة الجهاز المحمول

#### <a name="why-cant-i-see-create-transfer-order-from-license-plate-in-the-menu-item-work-activity-drop-down-list"></a>لماذا لا يمكنني رؤية "إنشاء أمر تحويل من لوحه الترخيص" في القائمة المنسدلة نشاط العمل لعنصر القائمة؟

يجب تمكين الميزة *إنشاء ومعالجة أوامر التحويل من تطبيق المستودع* لمزيد من المعلومات، راجع [تمكين إنشاء أوامر تحويل من تطبيق المستودع](#enable-create-transfer-order-from-warehouse-app).

### <a name="warehouse-management-mobile-app-processes"></a>عمليات تطبيق إدارة المستودع للأجهزة المحمولة

#### <a name="why-cant-i-see-the-menu-button-complete-order"></a>لماذا يتعذر علي رؤية زر القائمة "الأمر المكتمل"؟

يجب ان يكون لديك لوحه ترخيص واحده علي الأقل مخصصه لأمر التحويل.

#### <a name="can-several-warehouse-management-mobile-app-users-add-license-plates-to-the-same-transfer-order-at-the-same-time"></a>هل يمكن لمستخدمي تطبيق إدارة المستودع للأجهزة المحمولة المتعددين أضافه ألواح الترخيص إلى نفس أمر التحويل في نفس الوقت ؟

نعم، يستطيع العديد من العاملين في المستودع مسح لوحات الترخيص إلى نفس أمر التحويل.

#### <a name="can-the-same-license-plate-be-added-to-different-transfer-orders"></a>هل يمكن أضافه نفس لوحة الترخيص إلى أوامر تحويل مختلفه؟

لا يمكن أضافه لوحه الترخيص الا إلى أمر تحويل واحد في الوقت الحالي.

#### <a name="after-having-selected-the-complete-order-button-can-i-then-add-more-license-plates-for-that-transfer-order"></a>بعد تحديد الزر "الأمر المكتمل"، هل يمكنني أضافه لوحات ترخيص اضافيه لأمر التحويل هذا؟

لا يمكنك أضافه لوحات ترخيص اضافيه إلى  أمر تحويل يحتوي على حدث تطبيق المستودع **أمر تحويل مكتمل**.

#### <a name="how-can-i-find-existing-transfer-orders-to-be-used-via-the-select-transfer-order-button-in-the-warehouse-management-mobile-app-if-the-order-has-not-yet-been-created-in-the-backend-system"></a>كيف يمكن العثور علي أوامر التحويل الحالية لاستخدامها من خلال الزر "تحديد أمر التحويل" في تطبيق إدارة المستودع للأجهزة المحمولة، إذا لم يكن قد تم إنشاء الأمر في نظام الخلفية؟

يمكنك تمكين العاملين من البحث عن أرقام أوامر التحويل في تطبيق الاجهزه المحمولة لأداره المستودعات باستخدام قدره استعلام [البيانات الخاصة بها](warehouse-app-data-inquiry.md). علي سبيل المثال ، يمكنك إنشاء [عنصر قائمه الجهاز المحمول الديتر](warehouse-app-detours.md) الذي يستعلم عن البيانات المعروضة في الصفحة احداث **تطبيق مستودع** الويب (`WHSMobileDeviceQueueMessageCollection`) كجزء من *خطوه MobileDeviceQueueMessageCollectionIdentifierId* الأمر المحددة. يطابق رقم أمر التحويل القيمة الموضحة في حقل **المعرف** . راجع أيضا [استعلم عن أحداث تطبيق المستودع](#inquire-the-warehouse-app-events).

#### <a name="can-i-manually-select-the-transfer-order-number-to-be-used-from-the-warehouse-management-mobile-app"></a>هل يمكنني تحديد رقم أمر التحويل يدويا ليتم استخدامه من تطبيق إدارة المستودع للأجهزة المحمولة؟

يتم اعتماد أرقام أمر التحويل الذي تم إنشاؤه تلقائيا بواسطة التسلسلات الرقمية فقط. راجع أيضا الاجابه علي السؤال السابق فيما يتعلق بكيفية اعداد **زر تحديد أمر** التحويل. لمزيد من المعلومات حول كيفية العثور على أرقام أوامر التحويل ، راجع [الاستعلام عن احداث تطبيق المستودع](#inquire-the-warehouse-app-events).

### <a name="background-processing"></a>معالجة في الخلفية

#### <a name="how-should-i-clean-up-records-in-my-warehouse-app-events-queue-message-tables"></a>كيف يمكنني تنظيف السجلات في جداول رسائل قائمه انتظار احداث تطبيق المستودع؟

يمكنك عرض هذا العنصر في الصفحة **احداث تطبيق المستودع** والاحتفاظ به. لمزيد من المعلومات، راجع [الاستعلام عن أحداث تطبيق المستودع](#inquire-the-warehouse-app-events).

#### <a name="why-is-the-transfer-order-receipt-date-not-updated-according-to-my-delivery-date-control-setup"></a>لماذا لا يتم تحديث أمر التحويل "تاريخ الاستلام" وفقا لاعداد "التحكم في تاريخ التسليم"؟

يتم إنشاء أوامر التحويل دون استخدام إمكانيات **التحكم في تاريخ التسليم**.

#### <a name="can-i-use-a-license-plate-having-physical-negative-inventory-on-hand"></a>هل يمكنني استخدام لوحه ترخيص لها مخزون سلبي مادي؟

تدعم الميزة الكميات الفعلية الحالية الإيجابية الموجودة على مستوي لوحة الترخيص فقط، ولكن يمكنك الحصول على كميات فعلية على مستويات المستودع الأعلى ومستوى حالة المخزون عند تعيين لوحات الترخيص لأوامر التحويل.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]