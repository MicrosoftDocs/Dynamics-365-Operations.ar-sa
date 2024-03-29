---
title: خلط أبعاد المنتج في الموقع
description: يوفر هذا المقال معلومات حول مزج أبعاد المنتج في الموقع. تساعد وظيفة ملف تعريف الموقع هذه في تحسين إدارة الموقع عند استخدام متغيرات منتجات أو منتجات لها أبعاد، كما هو الحال في صناعة الأزياء. ويتيح لك تحديد ما إذا كان يمكن خلط التكوينات والألوان والأنماط والأحجام لملف تعريف موقع معين، أو ما إذا كان من الممكن وضع إحدى هذه الأبعاد أو توليفة منها فقط في نفس الموقع.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 9daf6061d56ef004753114aaffa8eb580cea1186
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885714"
---
# <a name="location-product-dimension-mixing"></a>خلط أبعاد المنتج في الموقع

[!include [banner](../includes/banner.md)]

مزج أبعاد المنتج في الموقع هي وظيفة ملف تعريف الموقع التي تساعد في تحسين إدارة الموقع عند استخدام متغيرات منتجات أو منتجات لها أبعاد، كما هو الحال في صناعة الأزياء. ويتيح لك تحديد ما إذا كان يمكن خلط التكوينات والألوان والأنماط والأحجام لملف تعريف موقع معين، أو ما إذا كان من الممكن وضع إحدى هذه الأبعاد أو توليفة منها فقط في نفس الموقع.

## <a name="turn-the-location-product-dimension-mixing-feature-on-or-off"></a>تشغيل ميزة خلط أبعاد المنتج في الموقع‬ أو إيقاف تشغيلها

لاستخدام الوظيفة الموضحة في هذا المقال ، يجب أن تكون الميزة *خلط أبعاد المنتج في الموقع‬‬‬* قيد التشغيل في النظام. هذه الميزة إلزامية ولا يمكن إيقاف تشغيلها، اعتبارًا من Supply Chain Management 10.0.25. إذا كنت تقوم بتشغيل إصدار أقدم من 10.0.25، فبإمكان المسؤولين تشغيل هذه الوظيفة أو إيقاف تشغيلها عن طريق البحث عن ميزة *خلط أبعاد المنتج في الموقع‬* في مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="setup"></a>الإعداد

يحتاج كل موقع في المستودع إلى ملف تعريف موقع يقترن به ويصف خصائص الموقع. بالتالي، ستتمكن كافة المواقع التي تستخدم نفس ملف التعريف من السماح بمزج أبعاد المنتج بعد إعدادها.

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a>تكوين ملفات تعريف المواقع للسماح بمزج أبعاد المنتج

1. انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> ملفات تعريف الموقع**.
1. في قائمه ملفات تعريف المواقع، حدد **مجمع**.
1. في جزء الإجراءات، حدد **تحرير**.
1. في علامة التبويب السريعة **عام**، قم بتعيين خيار **تمكين مزج أبعاد المنتج للموقع** إلى *نعم*.

    > [!NOTE]
    > يمكنك تعيين هذا الخيار إلى *نعم* فقط إذا تم تعيين خيار **السماح بالعناصر المختلطة** إلى *لا*.

1. في علامة التبويب السريعة **مزج أبعاد المنتج المسموح بها**، قم بتعيين خيار **الحجم** إلى *نعم*. في السيناريو الموضح في هذا المقال، يمكن إجراء المزج فقط للمنتجات التي لها أبعاد **حجم** مختلفة. مع ذلك، تتوفر أيضًا خيارات أخرى.
1. حدد **حفظ**.

### <a name="create-a-new-product-master-and-product-variants"></a>إنشاء أصل منتج واحد ومتغيرات المنتجات

1. ‏‫انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> أصول المنتجات‬‬**.
1. في جزء الإجراءات، حدد **جديد** لإنشاء أصل منتج.
1. في مربع الحوار **منتج جديد**، قم بتعيين القيم التالية:

    - **نوع المنتج:** *الصنف*
    - **النوع الفرعي للمنتج:** *أصل المنتج*
    - **رقم المنتج:** *B0001*
    - **اسم المنتج:** *حجم B0001*
    - **مجموعة أبعاد المنتج:** *الحجم*
    - **تقنية التكوين:** *متغير محدد مسبقًا*

1. حدد **موافق**.
1. في صفحة **تفاصيل المنتج**، ضمن علامة التبويب **عام**، قم بتعيين القيم التالية:

    - **إنشاء متغيرات تلقائيًا:** *نعم*
    - **مجموعة الحجم:** *CASUALDHIR*

1. لعرض المتغيرات المعرفة مسبقًا، في جزء الإجراءات، حدد **متغيرات المنتج**.

    تظهر صفحة **متغيرات المنتج** وتعرض قائمة بالمتغيرات من تكوين مجموعة الحجم.

### <a name="release-products-to-the-usmf-company"></a>إصدار المنتجات إلى شركة USMF

1. في جزء الإجراءات، حدد **إصدار المنتج**.
1. في صفحة **تحديد منتجات لإصدارها**، تأكد من وجود رقم المنتج *B0001* في القائمة، ثم حدد **التالي**.
1. حدد **التالي** لتأكيد متغيرات المنتج المطلوب إصدارها.
1. من صفحة **تحديد الشركات للإصدار إليها**، حدد *USMF*، ثم حدد **التالي** لتأكيد التحديد.
1. في صفحة **تأكيد التحديد**، حدد **إنهاء** لإكمال الإصدار.

    تظهر لك رسالة "اكتملت العملية".

### <a name="update-a-released-product-in-the-usmf-company"></a>تحديث منتج تم إصداره في شركة USMF

1. تأكد من أنك قمت بتسجيل الدخول إلى شركة **USMF**.
1. انتقل إلى **إدارة معلومات المنتج \> المنتجات \> المنتجات المُصدرة** لإنهاء إنشاء المنتج المُصدر.
1. ابحث عن وحدد رقم الصنف *B0001* لفتح صفحة **تفاصيل المنتج التي تم إصدارها**.
1. في جزء الإجراءات، حدد **تحرير**.
1. في علامة التبويب السريعة **عام**، تأكد من تعيين حقل **مجموعة نماذج الأصناف** إلى *FIFO*.
1. في جزء الإجراءات، في علامة تبويب **المنتج** في مجموعة **إعداد‬**، حدد **مجموعات الأبعاد**.
1. قم بتعيين القيم التالية:

    - **مجموعة أبعاد التخزين:** *Ware*
    - **مجموعة أبعاد التعقب:** *بلا*

1. حدد **موافق**.
1. في جزء الإجراءات، في علامة تبويب **المنتج** في مجموعة **إعداد‬**، حدد **‏‫التدرج الهرمي للحجز‬**.
1. قم بتعيين حقل **التدرج الهرمي للحجز** إلى *الافتراضي*، ثم حدد **موافق**.
1. في علامة التبويب السريعة **عام**، في قسم **الإدارة**، لاحظ أنه تم تحديث التحديدات الخاصة بك.
1. في علامة التبويب السريعة **الشراء**، في حقل **السعر**، أدخل *10*.
1. في علامة التبويب السريعة **إدارة التكاليف**، في حقل **مجموعة الأصناف**، أدخل *صوتيات*.
1. في علامة التبويب السريعة **الشراء**، في حقل **السعر**، أدخل *10*.
1. في علامة التبويب السريعة **المستودع**، في حقل **معرف مجموعة تسلسل الوحدة**، أدخل *ea*.
1. حدد **حفظ**.

### <a name="create-a-location-directive"></a>إنشاء توجيه موقع

1. انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.
1. في الجزء الأيسر في حقل **نوع أمر العمل**، حدد *أوامر الشراء*.
1. في القائمة، حدد توجيه الموقع الذي يسمي *24 أمر شراء مباشر*.
1. في علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد **جديد** لإضافة سطر إلى الشبكة.
1. في البند الجديد، قم بتعيين القيم التالية:

    - **رقم المسلسل:** *1*

        يجب أن يكون البند الجديد أالبند الموجود سابقا. لإجراء التغيير، استخدم الزرين **تحريك لأعلى** و **تحريك لأسفل** على شريط الأدوات، أو قم بتغيير قيمة **رقم التسلسل** للبند الموجود إلى *2*.

    - **الاسم:** *الوضع في ملف تعريف الموقع BULK*
    - **استخدام الموقع الثابت:** *المواقع الثابتة وغير الثابتة*
    - **السماح بالمخزون السالب:** *قم بإلغاء تحديد خانة الاختيار هذه (= لا)*
    - **تمكين الدفعة:** *قم بإلغاء تحديد خانة الاختيار هذه (= لا)*
    - **الاستراتيجية:** *بلا*

1. في أثناء تحديد السطر الجديد ، حدد **تحرير استعلام** فوق الشبكة.
1. في مربع حوار الاستعلام، ضمن علامة التبويب **النطاق**، حدد **إضافة** لإضافة بند إلى الشبكة.
1. في البند الجديد، قم بتعيين القيم التالية:

    - **الجدول:** *المواقع*
    - **الجدول المشتق:** *المواقع*
    - **الحقل:** *معرف ملف الموقع*
    - **المعايير:** *BULK*

1. حدد **موافق**.
1. في صفحة **توجيهات الموقع**، في جزء الإجراءات، حدد **حفظ**.

> [!NOTE]
> في علامة التبويب السريعة **إجراءات توجيه المواقع** حقل **الاستراتيجية**، إذا كنت تستخدم استراتيجية الموقع *دمج*، فإن إعداد **مزج أبعاد المنتج المسموح به** في **ملفات تعريف الموقع**، سيتم تجاوزه وسيتم وضع الأصناف في نفس الموقع حتى وإن كان هذا السلوك غير مسموح به بواسطة الإعداد.

### <a name="create-a-mobile-device-menu-item"></a>إنشاء عنصر قائمة جهاز محمول

1. انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.
1. في جزء الإجراءات، حدد **جديد** لإنشاء عنصر قائمة لاستخدامه في الفرز.
1. في الرأس، عيّن القيم التالية:

    - **اسم عنصر القائمة:** *استلام سطر أمر الشراء*
    - **العنوان:** *استلام سطر أمر الشراء*
    - **الوضع:** *العمل*
    - **استخدام العمل الموجود:** *لا*

1. في علامة التبويب السريعة **عام**، عيّن القيم التالية:

    - **عملية إنشاء العمل:** *استلام سطر أمر الشراء وتخزينه*
    - **إنشاء لوحة الترخيص:** *نعم*

1. حدد **حفظ**.

### <a name="configure-the-mobile-device-menu"></a>تكوين قائمة الجهاز المحمول

1. انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> قائمة الجهاز المحمول**.
1. في قائمة القوائم، حدد **وارد**.
1. في جزء الإجراءات، حدد **تحرير**.
1. في قائمة **القوائم المتوفرة وعناصر القائمة**، ابحث عن عنصر القائمة **الاستلام سطر أمر الشراء** وحدده.
1. حدد الزر سهم لليمين لنقل عنصر قائمة **استلام سطر أمر الشراء** إلى قائمة **بنية القائمة**. بهذه الطريقة، تضيف عنصر القائمة الجديد إلى القائمة المحددة.
1. حدد **حفظ**.

## <a name="scenario"></a>سيناريو

يعرض سيناريو العرض التوضيحي هذا كيف يمكن وضع متغيرين مختلفين للمنتج في نفس الموقع عند عدم سماح ملف تعريف الموقع بالأصناف المختلطة، ولكن يتم تمكين *ميزة مزج أبعاد المنتج للموقع*. في هذه الحالة، ستستخدم متغير **الحجم** كمعيار.

قبل البدء، تأكد من وجود مواقع فارغة في المستودع *24* الذي يستخدم ملف تعريف الموقع *BULK*.

### <a name="create-a-purchase-order"></a>إنشاء أمر شراء

ستقوم بإنشاء أمر شراء يحتوي على ثلاثة سطور: سطرين لنفس رقم المنتج ولكن بمتغيرات **حجم** مختلفة، وسطر ثالث لمنتج مختلف ليس له متغيرات.

1. انتقل إلى **الحسابات الدائنة \> أوامر الشراء \> جميع أوامر الشراء**.
1. في جزء الإجراء، حدد **جديد**.
1. في مربع الحوار **إنشاء أمر شراء**، قم بتعيين القيم التالية:

    - **حساب المورّد:** *1001*
    - **المستودع:** *24*

1. حدد **موافق**.
1. يتم إنشاء أمر الشراء، وتتم إضافة سطر جديد في علامة التبويب السريعة **سطور أمر الشراء**. تدوين ملاحظة برقم أمر الشراء.
1. في البند الجديد، قم بتعيين القيم التالية:

    - **رقم الصنف:** *B0001*
    - **الحجم** *L*
    - **الكمية:** *2*

1. حدد **إضافة سطر** أعلى الشبكة لإضافة سطر أمر شراء ثان، ثم قم بتعيين القيم التالية:

    - **رقم الصنف:** *B0001*
    - **الحجم** *XL*
    - **الكمية:** *2*

1. حدد **إضافة سطر** لإضافة سطر أمر شراء ثالث، ثم قم بتعيين القيم التالية:

    - **رقم الصنف:** *A0001*
    - **الكمية:** *1*

1.حدد **حفظ**.

### <a name="receive-purchase-order-lines-in-the-warehouse-management-mobile-app"></a>استلام سطور أوامر الشراء في تطبيق إدارة المستودع للأجهزة المحمولة

1. سجل الدخول إلى تطبيق إدارة المستودع للأجهزة المحمولة كمستخدم ممكّن للمستودع *24*.
1. حدد قائمة **الوارد**.
1. حدد **استلام سطر أمر الشراء**.
1. حدد حقل **رقك أمر الشراء**، ثم أدخل رقم أمر الشراء.
1. قم بتأكيد الإدخال بتحديد زر التأكيد (✔) في أسفل الصفحة.
1. أدخل رقم السطر من أمر الشراء الذي يجري استلامه. حدد حقل **رقم البند**، ثم استخدم لوحة الأرقام لإدخال القيمة *1*.
1. قم بتأكيد الإدخال.
1. أدخل الكمية المطلوب استلامها. حدد زر علامة زائد (**+**) مرتين لزيادة القيمة في حقل **الكمية** إلى *2*.
1. سجل الإدخال الخاص بك وذلك بتحديد الزر (✔) الموجود أسفل الصفحة، ثم قم بتأكيد الإدخال بتحديد الزر (✔) مرة أخرى.
1. اعرض المعلومات الموجودة في صفحة **أوامر الشراء: وضع**. تعرض هذه الصفحة العمل الذي تم إنشاؤه لحالة التخزين (العمل 1).

    يتم عرض الموقع الذي سيتم فيه تخزين الصنف المستلم وكذلك لوحة الترخيص والصنف والحجم والكمية الخاصة مهمة **استلام سطر أمر الشراء** التي قمت بإكمالها للتو.

1. قم بتأكيد عمل التخزين.
1. قم بتكرار الخطوات من 4 إلى 11 لسطر أمر الشراء 2. مع ذلك، في الخطوة 8، حدد الكمية *1*.

    يتم إنشاء عمل تخزين (العمل 2) جديد لنفس الموقع مثل العمل 1.

1. قم بتكرار الخطوات من 4 إلى 11 مرة أخرى أمر الشراء 2. في الخطوة 8، حدد الكمية المتبقية *1*.

    يتم إنشاء عمل تخزين (العمل 3) جديد لنفس الموقع مثل العمل 1 والعمل 2. يحدث هذا السلوك بسبب استخدام استراتيجية التوجيه لموقع *الدمج*، وعلامة التبويب السريعة **مزج أبعاد المنتج المسموح به** في إعداد *ملفات تعريف الموقع* بالقيمة **Bulk** تسمح بمزج متغير **الحجم** في الموقع.

1. قم بتكرار الخطوات من 4 إلى 11 لسطر أمر الشراء 3. في الخطوة 8، حدد الكمية *1* لرقم الصنف *A0001*.

    يتم إنشاء عمل تخزين (العمل 4) جديد لموقع مختلف عن الموقع المستخدم لبنود أمر الشراء 1 و 2. يحدث هذا السلوك بسبب عدم سماح ملف تعريف الموقع بالمنتجات الممزوجة، ولكنه يسمح بأبعاد ممزوجة لنفس أصل المنتج.

1. حدد زر القائمة أعلى الصفحة (أحيانًا يُشار إليه بهامبورجير أو الزر هامبورجير)، ثم حدد **إلغاء** لإنهاء **استلام سطر أمر الشراء**.

> [!TIP]
> يمكنك تكرار هذا السيناريو، ولكن في هذه المرة، قم بتعيين **الحجم** - *لا* ضمن علامة التبويب السريعة **السماح بمزج أبعاد المنتج** في *BULK* **ملفات تعريف الموقع**، بحيث لا يمكن مزج أي أبعاد للمنتج. في هذه الحالة، عند استلام أمر الشراء، سيتم وضع كل متغير منتج في موقع جديد.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]