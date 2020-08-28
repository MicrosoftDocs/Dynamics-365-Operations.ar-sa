---
title: وضع على الحائط - وضع في المتجر
description: يوفر هذا الموضوع معلومات حول وظيفة وضع على الحائط - وضع في المتجر. تتيح لك هذه الوظيفة معالجة السيناريوهات التي يجب فيها تجميع منتج في منطقة مرحلية للتحزيم المسبق، استنادًا إلى معايير يمكن تكوينها. وساعد على تقليل وقت الانتقاء نظرًا لإتاحة الانتقاء إلى لوحة ترخيص هدف واحدة كما يمكنها استخدام المزيد من أماكن الوضع أكثر من انتقاء نظام المجموعة.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 10eb32f75ccfe1521af9ebfe1e73ef08ea4238f7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597523"
---
# <a name="put-to-wall---put-to-store"></a>وضع على الحائط - وضع في المتجر

[!include [banner](../includes/banner.md)]

تتيح لك الوظيفة *وضع على الحائط - وضع في المتجر* معالجة السيناريوهات التي يجب فيها تجميع منتج في منطقة مرحلية للتحزيم المسبق، استنادًا إلى معايير يمكن تكوينها. ونظرًا لأن هذه الوظيفة تتيح الانتقاء إلى لوحة ترخيص هدف واحدة ويمكنكها استخدام المزيد من أماكن الوضع أكثر من انتقاء نظام المجموعة، فإن الشركات التي تقوم بالشحن إلى المتاجر أو تتعامل مع أصناف صغيرة ستستفيد من خفض وقت الانتقاء.

يوجه سير عمل هذه الوظيفة المنتج المنتقى إلى موقع فرز لتوزيعه في أنواع مختلفة من الحاويات. وبشكل عام، يتضمن كل موقع من مواقع الفرز عدة مواضع للفرز. يتم تعيين كل موضع فرز وفقًا للمعايير التي تعينها إجراءات العمل. المعايير النموذجية هي الوجهة الأخيرة أو الشحنة أو الحمل. بعد وصول منتج، يتم توزيعه لكل موضع فرز استنادًا إلى الكمية المقترنة بالأمر أو الوجهة أو الشحنة أو الحمل. عندما تكون الحاوية كامله أو مكتملة، يتم نقلها إلى موقع مرحلي أو موقع شحن لإجراء مزيد من المعالجات، وذلك وفقًا لإجراءات العمل.

يُشار إلى وظيفة التخزين هذه أيضًا بواسطة أسماء أخرى، مثل الفتح من "التجزئة" و "الفصل".

## <a name="turn-on-the-outbound-sorting-feature"></a>تشغيل ميزة الفرز الخارجي

قبل أن تتمكن من استخدام الوظيفة *وضع على الحائط - وضع في المتجر*، يجب تشغيل ميزة *الفرز الخارجي* في النظام لديك. بإمكان المسؤولين استخدام مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة. هناك، يتم إدراج الميزة بالطريقة التالية:

- **الوحدة:** *إدارة المستودعات*
- **اسم الميزة:** *الفرز الخارجي*

يمكن استخدام ميزة *الفرز الخارجي* جنبًا إلى جنب مع الميزة *كود خطوة الموجة على مستوى المؤسسة* إذا كانت قيد التشغيل. يجب أيضًا تشغيل هذه الميزة إذا كنت ستستخدم الأكواد المحددة مسبقًا والتي تم إعدادها في أكواد خطوة الموجة. في مساحة عمل **إدارة الميزات**، تكون هذه الميزة مدرجة بالطريقة التالية:

- **الوحدة:** *إدارة المستودعات*
- **اسم الموجة:** *كود خطوة الموجة على مستوى المؤسسة*

## <a name="setup"></a>الإعداد

بالنسبة لهذا العرض التوضيحي، يتم استخدام بيانات Contoso القياسية والمستودع *62*. كما يتم أيضًا استخدام بعض الإضافات الموضحة لاحقًا.

### <a name="location-type"></a>نوع الموقع

1. انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> أنواع المواقع**.
1. في جزء الإجراءات، حدد **جديد** لإنشاء نوع موقع للفرز.
1. قم بتعيين القيم التالية:

    - **نوع الموقع:** *SORT*
    - **الوصف:** *فرز*

1. حدد **حفظ**.

### <a name="warehouse-management-parameters"></a>محددات إدارة المستودعات

1. انتقل إلى **إدارة المستودعات‬\> إعداد‬ \> محددات إدارة المستودعات**.
1. في علامة التبويب **عام**، في علامة التبويب السريعة **أنواع المواقع**، في الحقل **نوع موقع الفرز**، أدخل *SORT*.
1. حدد **حفظ**.

### <a name="location-profile"></a>ملف تعريف الموقع

1. انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> ملفات تعريف الموقع**.
1. في جزء الإجراءات، حدد **جديد** لإنشاء ملف تعريف موقع لموقع الفرز.
1. في الرأس، عيّن القيم التالية:

    - **معرف ملف تعريف الموقع:** *فرز*
    - **الاسم:** *فرز*

1. في علامة التبويب السريعة **عام**، عيّن القيم التالية:

    - **تنسيق الموقع:** *PACK*
    - **نوع الموقع:** *SORT*
    - **استخدام تعقب لوحة الترخيص:** *نعم*
    - **السماح بالأصناف المختلطة:** *نعم*
    - **السماح بحالات المخزون المختلطة:** *نعم*

1. حدد **حفظ**.

### <a name="locations"></a>المواقع

1. انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> المواقع**.
1. امسح خانة الاختيار **إنشاء أرقام شيكات للموقع**.
1. في جزء الإجراءات، حدد **جديد**، ثم عيِّن القيم التالية:

    - **المستودع:** *62*
    - **الموقع:** *فرز*
    - **معرف ملف تعريف الموقع:** *فرز*

1. حدد **حفظ**.

### <a name="packing-profiles"></a>ملف تعريف التعبئة

1. انتقل إلى **إدارة المستودعات \> الإعداد \> التعبئة \> ملفات تعريف التعبئة**.
1. في جزء الإجراءات، حدد **جديد**، ثم عيِّن القيم التالية:

    - **معرف ملف تعريف التعبئة:** *فرز*
    - **الوصف:** *فرز*
    - **سياسة تعبئة الحاوية:** اترك هذا الحقل فارغًا.
    - **وضع معرف الحاوية:** *تلقائي*
    - **نوع الحاوية:** *PALLET 48X48*
    - **إنشاء حاوية تلقائيًا عند إغلاق الحاوية:** اترك هذا الحقل فارغًا.

1. حدد **حفظ**.

### <a name="wave-step-codes"></a>رموز خطوة الموجة

عند تشغيل الميزة *كود خطوة الموجة على مستوى المؤسسة*، قم بإعداد الكود التالي.

1. انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> أكواد خطوة الموجة**.
1. في جزء الإجراءات، حدد **جديد**، ثم عيِّن القيم التالية:

    - **كود خطوة الموجة:** *فرز*
    - **وصف خطوة الموجة:** *فرز*
    - **نوع خطوة الموجة:** *قالب فرز*

1. حدد **حفظ**.

### <a name="outbound-sorting-template"></a>قالب الفرز الصادر

يتحكم قالب الفرز فيما إذا كان سيتم إنشاء مواضع الفرز وتحديد المعايير المستخدمة والسمات الأخرى لعملية الفرز.

1. انتقل إلى **إدارة المستودعات \> الإعداد \> التعبئة \> قالب الفرز الخارجي**.
1. في جزء الإجراءات، حدد **جديد** لإنشاء قالب فرز.
1. في رأس القالب الجديد، عيِّن القيم التالية:

    - **معرف قالب الفرز الخارجي:** *فرز الموجة*
    - **لوصف:** *فرز الموجة*
    - **نوع قالب الفرز:** *طلب الموجة*

        يحدد هذا الحقل العملية التي يتم استخدام قالب الفرز لها. تتوفر القيم التالية:

        - **طلب الموجة** – يتم استخدام قالب الفرز للعملية *وضع على الحائط*. يُستخدم نوع القاالب هذا لتجاوز محطة التعبئة ومعالجة المخزون الوارد من الموجة مباشرة. لا يمكن استخدام هذا النوع إلا في حالة تضمين طريقة معالجة موجة **الفرز** في قالب الموجة.
        - **الحاوية** – يتم استخدام قالب الفرز لمعالجة *بناء البالتة بعد التعبئة*. يُستخدم هذا القالب لمعالجة الحاويات المغلقة في محطة التعبئة والتي يجب فرزها إلى بالتات.

    - **المستودع:** *62*
    - **الموقع:** *فرز*

1. في علامة التبويب السريعة **عام**، عيّن القيم التالية:

    - **التحقق من الفرز:** *مسح الموضع*

        يحدد هذا الحقل التحقق من الصحة المطلوب أثناء الفرز. تتوفر القيم التالية:

        - بلا‬‬
        - مسح لوحة الترخيص ضوئيًا
        - مسح منصب

    - **إنشاء عمل عند إغلاق الموضع:** *نعم*

        عند تحديد هذا الخيار على القيمة *نعم*، سيتم إنشاء عمل عند إغلاق الموضع لنقل المخزون إلى موقع الشحن النهائي. وعند التعيين على القيمة *لا*، سيتم انتقاء المخزون إلى الأمر فورًا عند إغلاق الموضع.

    - **تعيين الموضع:** *يدويًا*

        يحدد هذا الحقل نوع تعيين الموضع. تتوفر القيم التالية:

        - **يدويًا** – يجب على المستخدم الإشارة دائمًا إلى الموضع الذي ينبغي فرز المخزون به.
        - **تلقائيًا** – سيرشد النظام المخزون تلقائيًا إلى موضع إذا أمكن، استنادًا إلى فواصل قالب الفرز.

    - **تعيين معايير موضع الفرز:** *استخدام الموضع الفارغ فقط*

        يتحكم هذا الحقل فيما إذا كان ستتم مراعاة المخزون الموجود بالفعل في مواضع الفرز عند تعيين موضع للطلب. تتوفر القيم التالية:

        - **استخدام الموضع الفارغ فقط** – ستتم مراعاة المواضع التي لديها بالفعل مخزون مقترن بها
        - **افتراض الموضع فارغ** – سيتم تجاهل أي مخزون موجود بالفعل في الموضع أثناء التعيين. سيتم استخدام كافة المواضع المتاحة.

    - **كود خطوة الموجة:** *فرز*

        إذا كانت الميزة *كود خطوة الموجة على مستوى المؤسسة* قيد التشغيل، يجب أيضًا إعداد كود خطوة موجة *الفرز* في أكواد خطوة الموجة.

    - **الإغلاق التلقائي لموضع الفرز:** *نعم*

        عند تعيين هذا الخيار على *نعم*، يتم إغلاق موضع الفرز تلقائيًا عند اكتمال كافة الأعمال الواردة إلى الموضع.

    - **عدد مواضع الفرز:** *3*

        يحدد هذا الحقل الحد الأقصى لعدد مواضع الفرز التي سينشئها النظام.

    - **بادئة موضع الفرز:** *SP-*

        يحدد هذا الحقل البادئة التي يعينها النظام قبل رقم الموضع.

    - **تعبئة موضع الفرز تلقائيًا:** *نعم*

        عند تعيين هذا الخيار على *نعم*، تتم تعبئة المخزون الموجود في موضع الفرز بإحدي الحاويات عند إغلاق الموضع.

    - **معرف ملف تعريف التعبئة:** *فرز*

        يحدد هذا الحقل ملف تعريف التعبئة الذي سيتم استخدامه عند تعبئة موضع الفرز في إحدي الحاويات.

1. في جزء الإجراءات، حدد **تحرير الاستعلام** لتحديد المعايير المستخدمة لقالب الفرز الحالي.
1. في مربع حوار الاستعلام، ضمن علامة التبويب **الفرز**، حدد **جديد** لإضافة سطر، ثم عيِّن القيم التالية:

    - **الجدول:** *تفاصيل الحمل*
    - **الجدول المشتق:** *تفاصيل الحمل*
    - **الحقل:** *معرف الشحنة*
    - **اتجاه البحث:** *تصاعدي*

1. حدد **موافق**.
1. قد تتلقى الرسالة التالية: "ستتم إعادة تعيين التجميع، هل تريد المتابعة؟" حدد **نعم**.

    يصبح الزر **فواصل قوالب الفرز الخارجي** في جزء الإجراءات متاحًا.

1. في جزء الإجراءات، حدد **فواصل قوالب الفرز الخارجي**.
1. حدد خانة الاختيار **تجميع حسب الحقل** للتجميع حسب معرفة الشحنة.

    يؤدي هذا الإعداد إلى إنشاء موضع فرز واحد لكل شحنة تمثل حاية في الموجة.

1. حدد **موافق**.

### <a name="wave-process-methods"></a>طرق معالجة الموجة

1. انتقل إلى **إدارة المستودعات \> إعداد \> الموجات \> أساليب عملي الموجة**.
1. في جزء الإجراءات، حدد **طرق إعادة الإنشاء**.

    يتم إضافة أسلوب **الفرز** إلى قائمة الأساليب المتوفرة، ويتم تحديد نوع قالب موجة *الشحن* له.

### <a name="wave-templates"></a>قوالب الموجة

تحرير قالب الموجة المستخدم لفرز طلب الموجة.

1. انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجة**.
1. في الحقل **نوع قالب الموجة**، حدد *الشحن*.
1. حدد القالب **افتراضي الشحن 62** الموجود.
1. في جزء الإجراءات، حدد **تحرير**.
1. في علامة التبويب السريعة **عام**، قم بإجراء التغييرات التالية:

    - قم بتعيين الخيار **معالجة الموجة عند الإصدار إلى المستودع** إلى *لا*.
    - عيّن الخيار **التعيين إلى الموجات المفتوحة** على *نعم*.

1. في علامة التبويب السريعة **الأساليب**، قم بإعداد أسلوب **الفرز**:

    1. في شبكة **الأساليب المتبقية**، حدد **الفرز**.
    2. حدد زر السهم الأيمن لنقل **الأسلوب** إلى شبكة **الأساليب المحددة**.
    3. في شبكة **الأساليب المحددة**، حدد **الفرز**.
    4. عيِّن الحقل **رمز خطوة الموجة** على *الفرز*.

1. حدد **حفظ**.

### <a name="mobile-device-menu-items"></a>أصناف قائمة الجهاز المحمول

1. انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> عناصر قائمة الجهاز المحمول**.
1. في جزء الإجراء، حدد **جديد**.
1. في الرأس، عيّن القيم التالية:

    - **اسم عنصر القائمة:** *فرز*
    - **العنوان:** *الفرز*
    - **الوضع:** *غير مباشر*
    - **استخدام العمل الموجود:** *لا*

1. في علامة التبويب السريعة **عام**، عيّن القيم التالية:

    - **رمز النشاط:** *فرز خارجي*
    - **استخدام دليل المعالجة:** *نعم* (القيمة الافتراضية)
    - **معرف قالب الفرز الخارجي:** *فرز الموجة*

1. حدد **حفظ**.

### <a name="mobile-device-menu"></a>قائمة الجهاز المحمول

1. انتقل إلى **إدارة المستودعات \> إعداد \> جهاز محمول \> قائمة الجهاز المحمول**.
1. في قائمة القوائم، حدد **خارجي**.
1. في جزء الإجراءات، حدد **تحرير**.
1. في شبكة **القوائم المتوفرة وعناصر القائمة**، ابحث عن عنصر القائمة **الفرز** الذي أنشأته وحدده.
1. حدد زر السهم الأيمن لنقل **الفرز** إلى شبكة **بنية القائمة**. بهذه الطريقة، تضيف عنصر القائمة الجديد إلى القائمة **خارجي**.
1. حدد **حفظ**.

### <a name="location-directives"></a>توجيهات الموقع

يجب إنشاء توجيهات الموقع لإرشاد العمل الذي يتم إنشاؤه بعد اكتمال الفرز.

1. انتقل إلى **إدارة المستودعات ‬\> الإعداد‬ \> توجيهات الموقع**.
1. في الحقل **نوع أمر العمل**، حدد *انتقاء المخزون الذي تم فرزه*.
1. في جزء الإجراء، حدد **جديد**.
1. في الرأس، عيّن القيم التالية:

    - **التسلسل:** *1*
    - **الاسم:** *وضع على Baydoor*

1. في علامة التبويب السريعة **توجيهات الموقع**، عيّن القيم التالية:

    - **نوع العمل:** *إيداع*
    - **الموقع:** *6*
    - **المستودع:** *62*
    - **كود التوجيه:** اترك هذا الحقل فارغًا.
    - **وحدة SKU متعددة:** *لا*

1. حدد **حفظ** لجعل علامة التبويب السريعة **السطور** متاحة.
1. في علامة التبويب السريعة **السطور**، حدد **جديد**، ثم عيِّن القيم التالية. اقبل القيم الافتراضية لكافة الحقول الأخرى.

    - **رقم المسلسل:** *1*
    - **من الكمية:** *0*
    - **إلى الكمية:** *1000000*

1. حدد **حفظ** لجعل علامة التبويب السريعة **إجراءات توجيه الموقع** متاحة.
1. في علامة التبويب السريعة **إجراءات توجيه الموقع**، حدد **جديد**، ثم عيِّن القيم التالية. اقبل القيم الافتراضية لكافة الحقول الأخرى.

    - **رقم المسلسل:** *1*
    - **الاسم:** *Baydoor*

1. حدد **حفظ** لإتاحة الزر **تحرير الاستعلام** في علامة التبويب السريعة **إجراءات توجيه الموقع**.
1. في علامة التبويب السريعة **إجراءات توجيه المواقع**، حدد **تحرير الاستعلام**.
1. في مربع حوار الاستعلام، في علامة التبويب **النطاق**، ابحث عن الصف الذي يحتوي على حقل **المجال** المعين إلى *الموقع*. عيِّن حقل **المعايير** لهذا الصف على *Baydoor*.
1. حدد **موافق** لتأكيد التحرير.

### <a name="work-classes"></a>فئات العمل

1. انتقل إلى **إدارة المستودعات \> الإعداد \> العمل \> فئات العمل**.
1. في جزء الإجراء، حدد **جديد**.
1. في الرأس، عيّن القيم التالية:

    - **معرف فئة العمل:** *الفرز*
    - **الوصف:** *الفرز*
    - **نوع أمر العمل:** *انتقاء المخزون الذي تم فرزه*

1. حدد **حفظ**.

### <a name="work-templates"></a>قوالب العمل

1. انتقل إلى **إدارة المستودعات \> العمل \> قوالب العمل**.
1. في الحقل **نوع أمر العمل**، حدد *أوامر المبيعات*.
1. في الشبكة، حدد قالب العمل **انتقاء 62 للتعبئة**.
1. في جزء الإجراءات، حدد **فواصل رأس العمل**.
1. في جزء الإجراءات، حدد **تحرير**.
1. في السطر الذي يحتوي على الحقل **اسم الحقل** المعين على *معرف الشحنة*، امسح خانة الاختيار **تجميع حسب هذا الحقل**.
1. حدد **حفظ**، ثم اغلق مربع الحوار **فواصل رأس العمل**.
1. في الحقل **نوع أمر العمل**، حدد *انتقاء المخزون الذي تم فرزه*.
1. حدد **جديد**، لإنشاء قالب عمل.
1. في القسم **نظرة عامة**، عيّن القيم التالية. اقبل القيم الافتراضية لكافة الحقول الأخرى.

    - **قالب العمل:** *انتقاء ما تم فرزه*
    - **وصف قالب العمل:** *انتقاء ما تم فرزه*

1. حدد **حفظ** لإتاحة القسم **تفاصيل قالب العمل**.
1. ستنشئ سطرين في القسم **تفاصيل قالب العمل**. حدد **جديد**، ثم عيِّن القيم التالية للسطر 1:

    - **نوع العمل:** *انتقاء*
    - **إلزامي:** محدد (= *نعم*)
    - **معرف فئة العمل:** *الفرز*

1. حدد **جديد** مرة أخرى، ثم عيِّن القيم التالية للسطر 2:

    - **نوع العمل:** *إيداع*
    - **إلزامي:** محدد (= *نعم*)
    - **معرف فئة العمل:** *الفرز*

1. حدد **حفظ**.

## <a name="example-scenario"></a>سيناريو كمثال

يحاكي هذا السيناريو موقفًا حيث يخزن المستودع الأصناف الصغيرة في المواقع ويجب حزمها في صناديق قبل شحنها، عندما تكون وظيفة محطة التعبئة غير مناسبة تمامًا. يقوم العاملون بانتقاء الأوامر للعديد من العملاء والعناوين المختلفة في نفس الوقت لزيادة سرعة الانتقاء. بعد اكتمال الانتقاءد، يصل العاملون إلى موقع الفرز، حيث يمكن فرز الأصناف المنتقاة في الصندوق الصحيح، استنادًا إلى المعايير المطلوبة. في هذا المثال، سيتم استخدام معرف الشحنة لتحديد الصندوق الصحيح، نظرًا لأن كل شحنة لها عنوان مختلف. بعد تعبئة كافة الأصناف من التحميل وفرزها حسب الشحنة، سيتم نقل الصناديق إلى المنطقة المرحلية وتحميلها في النهاية إلى الشاحنة.

قبل بدء السيناريو، تأكد من إعداد كافة وظائف المستودع القياسية بشكل صحيح للمستودع لديك. يستخدم مستودع Contoso القياسي *62* لهذا الغرض. لم يتم تغيير التكوينات القياسية، بالإضافة إلى ما هو موضح في الإعداد.

### <a name="create-demand"></a>إنشاء طلب

قبل التمكن من شرح الوظيفة، يجب إنشاء طلب. بالنسبة لهذا السيناريو، ستقوم بإنشاء ثلاثه أوامر مبيعات لثلاثة عملاء مختلفين لمحاكاة عناوين تسليم مختلفة. وبهذه الطريقة ستنشئ ثلاث شحنات منفصلة.

قبل إنشاء أوامر المبيعات والشحنات، تأكد أن مواقع الانتقاء بها مخزون كاف لكافة الأصناف في الأوامر. راجع إعدادات توجيه الموقع لتأكيد مواقع الانتقاء التي يتم استخدامها لانتقاء أمر المبيعات. إذا كان من الضروري تسوية المخزون، فيمكنك إنشاء حركات يدوية أو استخدام تزويد أو استخدام أي سير عمل آخر. ثم احجز المخزون.

1. انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.
1. حدد **جديد** لإنشاء أمر مبيعات للأمر 1.
1. في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:

    - **العميل:** *US-001*
    - **المستودع:** *62*

1. حدد **موافق**.
1. تتم إضافة سطر جديد إلى الشبكة في علامة التبويب السريعة **سطر أمر المبيعات**. قم بتعيين القيم التالية:

    - **رقم الصنف:** *A0001*
    - **الكمية:** *5*

1. حدد **إضافة سطر** لإضافة سطر ثان، ثم قم بتعيين القيم التالية:

    - **رقم الصنف:** *A0002*
    - **الكمية:** *10*

1. كرر الخطوات التالية مع كل سطر مبيعات في الأمر لحجز المخزون له:

    1. في علامة التبويب السريعة **بنود أمر المبيعات**، في قائمة **المخزون**، حدد **الحجز**.
    1. في صفحة **الحجز**، حدد **حجز دفعة** ثم اغلق الصفحة.
    1. حدد **حفظ**.

1. حدد **جديد** لإنشاء أمر مبيعات للأمر 2.
1. في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:

    - **العميل:** *US-004*
    - **المستودع:** *62*

1. حدد **موافق**.
1. تتم إضافة سطر جديد إلى الشبكة في علامة التبويب السريعة **سطر أمر المبيعات**. قم بتعيين القيم التالية:

    - **رقم الصنف:** *A0001*
    - **الكمية:** *7*

1. حدد **إضافة سطر** لإضافة سطر ثان، ثم قم بتعيين القيم التالية:

    - **رقم الصنف:** *A0002*
    - **الكمية:** *3*

1. كرر الخطوات التالية مع كل سطر مبيعات في الأمر لحجز المخزون له:

    1. في علامة التبويب السريعة **بنود أمر المبيعات**، في قائمة **المخزون**، حدد **الحجز**.
    1. في صفحة **الحجز**، حدد **حجز دفعة** ثم اغلق الصفحة.
    1. حدد **حفظ**.

1. حدد **جديد** لإنشاء أمر مبيعات للأمر 3.
1. في مربع الحوار **إنشاء أمر المبيعات**، قم بتعيين القيم التالية:

    - **العميل:** *US-007*
    - **المستودع:** *62*

1. حدد **موافق**.
1. تتم إضافة سطر جديد إلى الشبكة في علامة التبويب السريعة **سطر أمر المبيعات**. قم بتعيين القيم التالية:

    - **رقم الصنف:** *A0001*
    - **الكمية:** *8*

1. اتبع الخطوات التالية لحجز مخزون لسطر المبيعات:

    1. في علامة التبويب السريعة **بنود أمر المبيعات**، في قائمة **المخزون**، حدد **الحجز**.
    1. في صفحة **الحجز**، حدد **حجز دفعة** ثم اغلق الصفحة.
    1. حدد **حفظ**.

أكمل الإجراء التالي لإصدار كل أمر من أوامر المبيعات للمستودع. سيتم إنشاء ثلاث شحنات مختلفة. ستضيف بعدها الشحنات الثلاث إلى موجة واحدة جديدة.

1. انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.
1. حدد أول أمر مبيعات أنشأته في الشبكة.
1. في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬**.

    ستتلقى رسالة معلوماتية تعرض معرف الموجة ومعرف الشحنة التي تم إنشاؤها.

1. كرر الخطوات السابقة لإصدار أمري المبيعات 2 و 3 للمستودع. لاحظ أن الرسالة المعلوماتية التي تتلقاها تشير إلى أنه قد تمت إضافة شحنة إلى الموجة التي تم إنشاؤه عند إصدارك أمر المبيعات رقم 1.
1. انتقل إلى **إدارة المستودعات \> الموجات الصادرة‬ \> موجات الشحنة‬ \> كافة الموجات‬**.
1. حدد معرف الموجة الذي تم إنشاؤه من إصدار أوامر المبيعات لفتح صفحة **الموجات**. تعرض هذه الصفحة تفاصيل الموجة. تعرض علامة التبويب السريعة **بنود الموجة** الشحنات التي تم إنشاؤها.

    يجب الآن إنشاء عمل لإحضار الأصناف من مواقع الانتقاء إلى موقع الفرز.

1. في جزء الإجراءات، حدد **معالجة**.

    أثناء معالجة الموجة، سيستخدم أسلوب الفرز قالب الفرز لتعيين المخزون لمواضع الفرز. عند اكتمال معالجة الموجة، تتلقى رسالة معلوماتية توضح أنه تم ترحيل الموجة وإنشاء العمل.

1. في جزء الإجراءات، ضمن علامة التبويب **الموجة**، في مجموعة **المعلومات ذات الصلة**، حدد **العمل** لعرض العمل الذي تم إنشاؤه. قم بتدوين ملاحظة بمُعرف العمل.
1. انتقل إلى **إدارة المستودعات \> التعبئة والتعبئة في حاويات \> تعيينات موضع الفرز الخارجي**.
1. في العمود الأيمن، يمكنك عرض موضع الفرز الخارجي الذي تم إنشاؤه لكل شحنة.
1. في علامة التبويب السريعة **معايير موضع الفرز**، يمكنك عرض معرف الشحنة لهذا الموضع.

تم إنشاء معرف عمل واحد لإحضار المخزون من مواقع الانتقاء إلى موقع الفرز. لإكمال العمل، ستحتاج إلى معرف العمل الذي تم إنشاؤه أثناء معالجة الموجة.

### <a name="sales-order-picking-to-the-sorting-location"></a>انتقاء أمر المبيعات لموقع الفرز

1. سجِّل الدخول إلى تطبيق الأجهزة المحمولة كعامل في المستودع *62*.
1. من القائمة الرئيسية، حدد **خارجي**.
1. من القائمة **خارجي**، حدد **انتقاء المبيعات**.
1. حدد الحقل **المعرف**، ثم أدخل معرف العمل من معالجة الموجة.
1. قم بتأكيد الإدخال.

    ستكون مطالبًا بعدها بإدخال لوحة الترخيص الهدف (LP). لاحظ أن السطر 1 في أمر المبيعات 1 هو ما يجب انتقاؤه وإضافته إلى لوحة الترخيص الهدف. يتم إظهار رقم الصنف والكمية ووصف الصنف وموقع الانتقاء.

1. في الحقل **لوحة الترخيص الهدف**، أدخل رقم لوحة ترخيص.

    ستنتقِ كافة السطور التي تم إنشاؤها من الموجة التي تمت معالجتها إلى نفس لوحة الترخيص الهدف.

1. قم بتأكيد الإدخال.

    يقدم تطبيق الأجهزة المحمولة الآن سلسلة من صفحات **الانتقاء** التي توجهك إلى موقع الانتقاء، والصنف والكمية التي يجب انتقاؤهما. بعد إضافة الصنف المنتقى إلى لوحة الترخيص، ستقوم بتأكيد عمل الانتقاء. ستكون الصفحة الأخيرة هي العمل لوضع العناصر المنتقاة في موقع الفرز.

1. قم بتأكيد عمل الانتقاء الأول.
1. يتم عرض عمل الانتقاء التالي. قم بتأكيد الانتقاء.
1. استمر في تأكيد عمل الانتقاء المتبقي.
1. الخطوة الأخيرة هي إكمال عمل الوضع. قم بتأكيد الاحتفاظ في موقع الفرز.

    ستتلقى رسالة "اكتمل العمل".

1. انهِ **انتقاء المبيعات** على تطبيق الأجهزة المحمولة.

### <a name="sortingput-to-wall"></a>الفرز/وضع على الحائط

الآن وبعد وضع كل المخزون في موقع الفرز، يجب فرزه في موضع الفرز الصحيح.

1. سجِّل الدخول إلى تطبيق الأجهزة المحمولة.
1. من القائمة الرئيسية، حدد **خارجي**.
1. في القائمة **خارجي**، حدد **فرز** للبدء في فرز العناصر.
1. في الحقل **لوحة الترخيص/الحاوية**، أدخل لوحة الترخيص الهدف لعمل أمر المبيعات الذي تم انتقاؤه.
1. قم بتأكيد الإدخال.
1. أدخل رقم الصنف المراد فرزه أولاً.
1. يحدد النظام موضع الفرز الأول الذي ينبغي إظهاره. قم بتأكيد موضع الفرز.
1. أنت مطالب بتعيين لوحة ترخيص إلى موضع الفرز. حدد الحقل **لوحة الترخيص**، وأدخل رقم لوحة الترخيص، ثم قم بأاكيد الإدخال.

    نظرًا لارتباط موضع الفرز بمعرف الشحنة، ستقوم بفرز الأصناف المنتقاة في لوحة ترخيص خاصة بالشحنة الخارجية وأمر المبيعات.

    تعرض الصفحة التالية معرف الصنف والكمية ومعرف موضع الفرز ومعرفات لوحات ترخيص "من" (الانتقاء) و "إلى" (الفرز). وترشدك المعلومات الموجودة في هذه الصفحة إلى فرز الأصناف والكميات المحددة من لوحة ترخيص الانتقاء إلى لوحة ترخيص الفرز.

1. قم بتأكيد موضع الفرز.
1. افرز العناصر الموجودة في موضع الفرز الأول. وعند الانتهاء من ذلك، يوجهك النظام إلى موضع الفرز التالي.
1. كرر هذه العملية لكافة السطور المنتقاة في أمر العمل. وينبغي لك أيضًا استخدام هذه العملية عند وجود سطور انتقاء متعددة لها نفس رقم الصنف.

    بتكرار هذه العملية لكافة الأصناف، يقيِّم النظام المعايير من الصنف التالي الممسوح ضوئيًا (سطر العمل) ويحدد موضع الفرز الذي ينبغي وضعه فيه. يتم توجيهك تلقائيًا لوضع العنصر في موضع الفرز الصحيح. وفقًا لإعداد التأكيد، يتم أيضًا توجيهك لتأكيد هذا الإجراء عن طريق إدخال رقم الموضع أو معرف لوحة الترخيص.

    > [!NOTE]
    > في حالة تشغيل الفرز التلقائي، لا يتوفر التخطي اليدوي.

1. عند الانتهاء من ذلك، في Microsoft Dynamics 365 Supply Chain Management، افتح صفحة **تعيينات موضع الفرز الخارجي** لمراجعة حالة المواضع.

    - إذا كانت المواضع مغلقة تلقائيًا، فحدد **إظهار المغلق** لإظهار المواضع المغلقة.
    - لاحظ أنه يتم عرض حركات موضع الفرز. يتم إظهار الصنف والكمية التي تمت معالجتها في الموضع.

    عند إعداد قالب الفرز الخارجي، عيِّن الخيار **إغلاق موضع الفرز تلقائيًا** على *نعم*. وبالتالي يتم إغلاق الموضع تلقائيًا بعد وضع آخر مخزون متوقع به. تكون مواضع الفرز بالحالة **مغلق**، وقد تم إنشاء العمل لنقل المخزون الذي تم فرزه إلى موقع *Baydoor*.

1. أكمل عمل انتقاء المخزون الذي تم فرزه لنقل المخزون إلى موقع الشحن. عندما يكون المخزون جاهزًا قم بتأكيد شحنه.

> [!NOTE]
> لكي تتم معالجة عمل انتقاء المخزون الذي تم فرزه بشكل صحيح، ينبغي استخدام عنصر قائمة الأجهزة المحمولة الذي يحتوي على معرف فئة عمل يكون الحقل **نوع أمر العمل** فيه معينًا على *انتقاء المخزون الذي تم فرزه* لعملية التحميل والحركة.

### <a name="manually-close-a-position-optional"></a>إغلاق موضع يدويًا (اختياري)

إذا كان ينبغي إغلاق مواضع الفرز يدويًا، يجب تعيين الخيار **إغلاق موضع الفرز تلقائيًا** لقالب الفرز الخارجي على *لا*، ويجب إجراء الإغلاق قبل إمكانية نقل المخزون إلى منطقه باب المرسى. يمكن إغلاق المواضع بعدة طرق:

- عبر تطبيق المستودع:

    - يمكن للمستخدم إجراء المسح الضوئي لأحد الأصناف الموجودة بالفعل في الموضع ثم تحديد **إغلاق** لإغلاق الموضع.
    - إذا قام المستخدم بالمسح الوئي لحاوية تم فرزها بالفعل، تظهر رسالة خطأ. ولكن لا يزال بإمكان المستخدم الاستمرار في إغلاق الموضع.

- من صفحة **تعيينات موضع الفرز الخارجي** في Microsoft Dynamics 365 Supply Chain Management:

    - يمكن للمستخدم تحديد سجل موضع الفرز الخارجي ثم تحديد **إغلاق الوضع** في جزء الإجراءات.

## <a name="tips"></a>تلميحات

- لا يمكن نقل الأصناف بين المواضع بعد تعيينها إلى موضع. يقيِّم النظام عدد العناصر التي ينبغي نقلها إلى موضع معين.
- يمكن تكوين قالب الفرز لإنشاء الحاويات تلقائيًا عند إغلاق المواضع. سيؤدي هذا الأسلوب إلى إنشاء بنية معرف حاوية قياسية استنادًا إلى ملف تعريف التعبئة المحدد.

> [!IMPORTANT]
> بعد إنشاء عمل الحركة من موقع الفرز، يجب ألا يتم إلغاء العمل. وبخلاف ذلك، سيتم حذف الموضع والحاويات الموجودة فيه من النظام ولن تكون متوفرة لإجراء مزيد من المعالجة. ستتم إزالة المخزون أيضًا.