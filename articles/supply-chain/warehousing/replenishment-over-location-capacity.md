---
title: تزويد أعلى من سعة الموقع
description: يوفر هذا الموضوع معلومات حول ميزة التزويد الأعلى من سعة الموقع. تعمل هذه الميزة على تمكين عمل التزويد بكامله المطلوب إنشاؤه في اليوم وتدير توافر عمل التزويد لضمان عدم نفاد موقع الانتقاء من المخزون أو انتقاله إلى وضع تجاوز السعة.
author: mirzaab
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
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 5591af5fce4eb3fc901919b98f654faa5e160c54
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652207"
---
# <a name="replenishment-over-location-capacity"></a>تزويد أعلى من سعة الموقع

[!include [banner](../includes/banner.md)]

يجب أن تقوم بعض المستودعات الكبيرة الحجم أو المقيدة المساحة بشحن كمية أكبر مما يستطيع موقع الانتقاء استيعابه خلال اليوم. تمكّن الميزة *تزويد أعلى من سعة الموقع* عمل التزويد بكامله المطلوب إنشاؤه في اليوم وتدير توافر عمل التزويد لضمان عدم نفاد موقع الانتقاء من المخزون أو انتقاله إلى وضع تجاوز السعة.

تمكّن الميزة إنشاء عمل تزويد يزيد عما يستطيع الموقع استيعابه، وهي تمنع إكمال عمل التزويد عندما يكون الموقع ممتلئًا. عندما ينخفض المخزون في موقع الانتقاء إلى أقل من الحد القابل للتكوين، يُتاح المزيد من عمل التزويد.

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a>تشغيل ميزة التزويد الأعلى من سعة الموقع

لإتاحة هذه الميزة، شغِّل الميزات التالية في [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (بالترتيب التالي):

1. حظر العمل على مستوى المؤسسة
1. تزويد أعلى من سعة الموقع

## <a name="set-up-the-feature-for-the-example-scenario"></a>إعداد الميزة السيناريو المثال

يوفر هذا القسم إرشادات ومثال يوضح كيفيه إعداد هذه الميزة وتجهيز عينة البيانات للسيناريو المثال الذي يتم توفيره لاحقًا في هذا الموضوع.

### <a name="enable-sample-data"></a>تمكين عينة البيانات

للعمل عبر [السيناريو المثال](#example-scenario) باستخدام عينات البيانات والسجلات المحددة هنا، يجب أن تكون في نظام تم فيه تثبيت [بيانات العرض التوضيحي](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed. بالإضافة إلى ذلك، يجب أن تحدد الكيان القانوني **USMF** قبل البدء.

### <a name="location-profile"></a>ملف تعريف الموقع

تمكين ميزة التزويد الأعلى من سعة الموقع في ملف تعريف الموقع.

1. انتقل إلى **إدارة المستودعات \> الإعداد \> المستودع \> ملفات تعريف الموقع**.
1. في الجزء الأيمن، حدد **PICK-06**.
1. في جزء الإجراءات، حدد **تحرير**.
1. في علامة التبويب السريعة **التزويد**، عيّن القيم التالية:

    - **تجاوز سعة الموقع:** *نعم*

        عند تمكين هذا الحقل، سيسمح بتجاوز السعة القصوى للموقع بواسطة عمل التزويد. ويؤدي ذلك أيضًا إلى تمكين الحقول الأخرى الموجودة علامة التبويب السريع **تزويد**.

    - **نوع حد توافر العمل:** *الكمية*

        يحدد هذا الحقل الطريقة التي يتم استخدامها لتحديد الوقت الذي ينبغي فيه إصدار مزيد من العمل. يمكنك إصداره حسب الكمية أو النسبة المئوية.

        - *النسبة المئوية* – حدد هذا الخيار لاستخدام سعة النسبة المئوية التي تستند إلى حدود المخزون أو مقاييس الحجم. يؤدي تحديد هذا الخيار إلى تمكين حقل **النسبة المئوية للتجاوز** وتعطيل حقلي الكمية المرتبطين، **كمية تجاوز السعة** و**وحدة تجاوز السعة**.

            يمكنك استخدام هذا الخيار إذا كانت مواقع الانتقاء تستخدم مقاييس الحجم.

            إذا تم تحديد هذا الخيار، فعيّن الحقل **النسبة المئوية لتجاوز السعة** إلى النسبة المئوية التي سيتم عندما جعل عمل التزويد متاحًا.

        - *الكمية* – حدد هذا الخيار لاستخدام قيمة كمية محددة.. يؤدي تحديد هذا الخيار إلى تعطيل حقل **النسبة المئوية لتجاوز السعة** وتمكين الحقلين **كمية تجاوز السعة** و**وحدة تجاوز السعة**.

            استخدم هذا الخيار عندما لا تستخدم مقاييس الحجم للمواقع التي يجري تزويدها، أو عندما يكون لديك كميات متناسقة التي يتم عندها إحضار المخزون إلى الموقع.

           إذا تم تحديد هذا الخيار، فقم بتعيين الحقلين **كمية تجاوز السعة** و**وحدة تجاوز السعة** إلى الكمية والوحدة التي سيتم عندها إتاحة عمل التزويد.

    - **كمية تجاوز السعة:** *0.65*

        يحدد هذا الحقل الكمية التي يحدث عندها تجاوز سعة الموقع.

        سيكون العمل متوفرًا كلما كان مجموع الكمية المتاحة في الموقع وكمية العمل أقل من هذه القيمة. سيتم حظر أي عمل تزويد يفوق هذه القيمة، ويجب إلغاء حظره يدويًا.

        تؤخذ حدود مخزون الموقع في الاعتبار عند حساب كمية العمل.

    - **وحدة تجاوز السعة:** *PL*

        يحدد هذا الحقل الوحدة المرتبطة بكمية تجاوز السعه.

        في هذه الحالة، سيتوفر مزيد من عمل التزويد عندما يصل الموقع إلى 0.65 بالته (بل).

    - **النسبة المئوية للتجاوز**

        يحدد هذا الحقل النسبة المئوية التي يحدث عندها تجاوز سعة الموقع.

        سيكون العمل متوفرًا كلما كان مجموع الكمية المتاحة في الموقع وكمية العمل أقل من هذه النسبة المئوية. سيتم حظر أي نسبة مئوية لكمية أعمال التزويد فوق هذه القيمة، ويجب إلغاء حظرها يدويًا.

        تؤخذ حدود مخزون الموقع في الاعتبار عند حساب النسبة المئوية لكمية العمل. إذا لم يتم تحديد حدود تخزين الموقع، فسيتم حساب النسبة المئوية لكمية العمل حسب الحجم إذا تم تحديد قيود الحجم لملف تعريف الموقع.

> [!IMPORTANT]
> إذا كنت تستخدم بيانات العرض التوضيحي للكيان القانوني **USMF** وقمت في وقت سابق بتشغيل الميزة *تحديد موضع لوحة ترخيص الموقع‬*، فيجب عليك إيقاف تشغيل الإعداد **تمكين تحديد موضع لوحة ترخيص الموقع** لملف تعريف الموقع **BULK-06** لإكمال خطوات المحمول في هذا السيناريو المثال.

### <a name="wave-step-code"></a>رمز خطوة الموجة

> [!NOTE]
> لإعداد رمز خطوة الموجة كما هو موضح هنا، قد يتعين عليك أولا استخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتشغيل الميزة المسماة *رمز خطوة الموجة على مستوى المؤسسة*.

1. انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> أكواد خطوة الموجة**.
1. حدد **جديد**، ثم قم بتعيين القيم التالية:

    - **كود خطوة الموجة:** *تزويد*
    - **وصف خطوة الموجة:** *تزويد*
    - **نوع خطوة الموجة:** *تزويد*

1. حدد **حفظ**.

### <a name="replenishment-template"></a>قالب التزويد

قوالب التزويد هي مجموعة من القواعد التي تتحكم في وقت تزويد الموقع وكيفية تزويده.

1. انتقل إلى **إدارة المستودعات \> الإعداد \> التزويد \> قوالب التزويد**.
1. في جزء الإجراءات، حدد **تحرير**.
1. في القسم **نظرة عامة**، حدد البند حيث تم تعيين الحقل **قالب إعادة التزويد** إلى *طلب التزويد*.
1. قم بتعيين القيم التالية:

    - **كود خطوة الموجة:** *تزويد*
    - **السماح بطلب الموجه لاستخدام كميات غير محجوزة:** *نعم*

1. حدد **حفظ**.

### <a name="wave-template"></a>قالب الموجة

1. انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجة**.
1. في الجزء الأيمن، قم بتعيين حقل **نوع قالب الموجة** إلى *شحن*.
1. حدد القالب **61 شحن** في القائمة.
1. في جزء الإجراءات، حدد **تحرير**.
1. في علامة التبويب السريعة **عام**، قم بتعيين خيار **أتمتة إصدار عمل التزويد‬** إلى *نعم*.

    عيّن هذا الخيار إلى *لا* لإنشاء عمل التزويد على أساس الطلب وإصداره تلقائيًا. يجب إضافة أسلوب موجة التزويد إلى قالب الموجة، وإنشاء قالب تزويد من نوع **طلب الموجة**. قم بإعداد قالب تزويد في صفحة **قوالب التزويد**. لإعداد قالب تزويد، يجب إضافة أسلوب التزويد إلى قالب الموجة.

1. على علامة التبويب السريع **الأساليب**، في عمود **الأساليب المحددة**، ابحث عن البند التالي:

    - **اسم الأسلوب:** *تزويد*
    - **الاسم:** *تزويد*

1. قم بتعيين الحقل **كود خطوة الموجة** لهذا البند إلى *تزويد*.
1. حدد **حفظ**.

## <a name="example-scenario"></a>سيناريو كمثال

بعد جعل كافة عينات البيانات التي تم وصفها سابقًا متوفرة ثم إعدادها، يمكنك العمل عبر هذا السيناريو لتجربة ميزة *تزويد أعلى من سعة الموقع‬*. تفترض القيم التي يتم عرضها في هذا السيناريو أنك تعمل مع بيانات العرض التوضيحي القياسية، وأنك حددت الكيان القانوني **USMF**، وأنك أعددت عينات السجلات التي ورد وصفها سابقًا في هذا الموضوع. يعمل هذا السيناريو أيضًا كمثال يوضح كيفية استخدام الميزة في إعداد الإنتاج.

### <a name="create-replenishment-work"></a>إنشاء عمل التزويد

#### <a name="create-sales-order-1"></a>إنشاء أمر مبيعات 1

1. انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.
1. في جزء الإجراءات، حدد **جديد** لفتح مربع حوار لإنشاء أمر مبيعات جديد.
1. في مربع الحوار، قم بتعيين القيم التالية:

    - **حساب العميل:** *US-007*
    - **المستودع:** *61*

1. حدد **موافق** لإنشاء أمر مبيعات وإغلاق مربع الحوار.
1. يتم فتح أمر المبيعات الجديد. ويتضمن بندًا جديدًا فارغًا في علامة التبويب السريعة **بنود أمر المبيعات**. في هذا السطر، قم بتعيين القيم التالية:

    - **رقم الصنف:** *T0100*
    - **الكمية:** *40*

1. على علامة التبويب السريعة **بنود أمر المبيعات**، حدد **المخزون‏‎ \> الحجز**.
1. في صفحة **الحجز**، حدد **حجز دفعة**.
1. قم بإغلاق الصفحة.
1. في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬**.

    ستتلقى رسائل إخبارية تعرض معرف الموجة ومعرف الشحنة التي تم إنشاؤها. كما يتم إنشاء موجة تزويد.

    تتلقى أيضًا رسالة تحذير تفيد بما يلي "لا يمكن إلغاء حظر معرف العمل XXXX بسبب وجود عمل تزويد غير منجز."

#### <a name="create-sales-order-2"></a>إنشاء أمر مبيعات 2

1. في صفحة **كافة أوامر المبيعات**، في جزء الإجراءات، حدد **جديد** لفتح مربع حوار لإنشاء أمر مبيعات جديد.
1. في مربع الحوار، قم بتعيين القيمة التالية:

    - **حساب العميل:** *US-001*
    - **المستودع:** *61*

1. حدد **موافق** لإنشاء أمر مبيعات وإغلاق مربع الحوار.
1. يتم فتح أمر المبيعات الجديد. ويتضمن بندًا جديدًا فارغًا في علامة التبويب السريعة **بنود أمر المبيعات**. في هذا السطر، قم بتعيين القيم التالية:

    - **رقم الصنف:** *T0100*
    - **الكمية:** *60*

1. على علامة التبويب السريعة **بنود أمر المبيعات**، حدد **المخزون‏‎ \> الحجز**.
1. في صفحة **الحجز**، حدد **حجز دفعة**.
1. قم بإغلاق الصفحة.
1. في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬**.

    ستتلقى رسائل إخبارية تعرض معرف الموجة ومعرف الشحنة التي تم إنشاؤها. كما يتم إنشاء موجة تزويد.

    تتلقى أيضًا رسالة تحذير تفيد بما يلي "لا يمكن إلغاء حظر معرف العمل XXXX بسبب وجود عمل تزويد غير منجز."

#### <a name="create-sales-order-3"></a>إنشاء أمر مبيعات 3

1. في صفحة **كافة أوامر المبيعات**، في جزء الإجراءات، حدد **جديد** لفتح مربع حوار لإنشاء أمر مبيعات جديد.
1. في مربع الحوار، قم بتعيين القيم التالية:

    - **حساب العميل:** *US-004*
    - **المستودع:** *61*

1. حدد **موافق** لإنشاء أمر مبيعات وإغلاق مربع الحوار.
1. يتم فتح أمر المبيعات الجديد. ويتضمن بندًا جديدًا فارغًا في علامة التبويب السريعة **بنود أمر المبيعات**. في هذا السطر، قم بتعيين القيم التالية:

    - **رقم الصنف:** *T0100*
    - **الكمية:** *30*

1. على علامة التبويب السريعة **بنود أمر المبيعات**، حدد **المخزون‏‎ \> الحجز**.
1. في صفحة **الحجز**، حدد **حجز دفعة**.
1. قم بإغلاق الصفحة.
1. في جزء الإجراءات، ضمن علامة التبويب **المستودع**، حدد **إصدار إلى المستودع‬**.

    ستتلقى رسائل إخبارية تعرض معرف الموجة ومعرف الشحنة التي تم إنشاؤها. كما يتم إنشاء موجة تزويد.

    تتلقى أيضًا رسالة تحذير تفيد بما يلي "لا يمكن إلغاء حظر معرف العمل XXXX بسبب وجود عمل تزويد غير منجز."

#### <a name="view-work-details"></a>عرض تفاصيل العمل

1. انتقل إلى **إدارة المستودعات \> العمل \> تفاصيل العمل**.
1. في القسم **نظرة عامة**، قم بتصفية عمود **المستودع** للمستودع *61*.
1. يجب أن يتبين لك أنه تم إنشاء سبعة معرفات عمل لأوامر المبيعات الثلاث عند الطلب.

    - تتضمن ثلاثة معرفات من معرفات العمل السبعة قيمة **التزويد** بالنسبة إلى *نوع أمر العمل*، وتتضمن أربعة من هذه المعرفات قيمة **أوامر المبيعات** بالنسبة إلى *نوع أمر العمل*.
    - تتضمن معرفات العمل الثلاثة التي لديها قيمة **التزويد** بالنسبة إلى *نوع أمر العمل* مواقع *الانتقاء* و*التخزين* نفسها في قسم **البنود**:

        - **انتقاء:** *02A01R5S1B*
        - **تخزين:** *06A01R2S1B*

    - تم إنشاء معرفي عمل لأمر المبيعات 1.

1. قم بتدوين معرفات العمل لأوامر المبيعات.

بحسب الكميات الفعلية، قد تختلف كميات العمل التي يتم إنشاؤها بشكل طفيف. ومع ذلك، يجب ان تتطابق رؤوس العمل التي يتم إنشاؤها مع مثال السيناريو هذا بشكل عام.

#### <a name="on-hand-inventory-license-plate-id"></a>معرف لوحة ترخيص المخزون الفعلي

في وقت لاحق في هذا السيناريو، ستستخدم تطبيق المستودع (أو المحاكي) ، حيث يجب عليك تحديد لوحة الترخيص لإكمال سيناريوهات الانتقاء والتزويد.

للعثور على معرفات لوحة الترخيص التي ستحتاج اليها لاحقًا، اتبع الخطوات التالية.

1. انتقل إلى **إدارة المخزون \> الاستعلامات والتقارير \> قائمة المخزون الفعلي**.
1. حدد الزر **إظهار عوامل التصفية** لفتح جزء عامل التصفية.
1. أدخل معايير التصفية التالية للحصول على لوحات الترخيص للسيناريو. استخدم عامل التصفية *يبدأ بـ*.

    - **رقم الصنف:** *T0100*
    - **المستودع:** *61*

1. حدد **تطبيق**.
1. في جزء الإجراءات، حدد **الأبعاد**.
1. في مربع الحوار **عرض الأبعاد**، في قسم **أبعاد التخزين**، حدد جميع القيم.
1. في قسم **الحركات**، حدد **رقم الصنف** و**الكمية \<\> 0**.
1. عند الانتهاء، حدد **موافق** لإغلاق مربع الحوار.
1. تعرض شبكة **المخزون الفعلي** أرقام ألواح الترخيص للصنف *T0100* في كل موقع. قم بتدوين لوحة الترخيص الموجودة في كل موقع، لأنك ستحتاج إلى هذه المعلومات لاحقًا.
1. قم بإغلاق الصفحة.

### <a name="process-steps"></a>خطوات العملية

ستقوم بتنفيذ تزويد موقع المستودع لأول معرّفي عمل. سيتم حظر العمل على عمل التزويد الثالث حتى ينخفض مستوى المخزون في موقع الانتقاء إلى أقل من الحد.

#### <a name="replenishment"></a>تزويد

1. سجل الدخول إلى تطبيق المستودع كمستخدم في المستودع *61*. (قم بإدخال *61* كمعرف المستخدم و*1* ككلمة مرور.)
1. انتقل إلى **المخزون \> التزويد**.

    تتم مطالبتك بإكمال عمل التزويد الأول. يظهر رقم الصنف والكمية وموقع الانتقاء.

1. في الحقل **LP**، أدخل رقم لوحة الترخيص للصنف في الموقع الذي يظهر.
1. حدد الزر **موافق** (أيقونة علامة الاختيار).

    يقوم النظام بإنشاء رقم لوحة الترخيص الهدف للوحة الترخيص الجديدة للصنف المنتقى.

1. حدد **موافق** لتأكيد القيمة.

    يظهر عمل التخزين الذي يرشد المستخدم لوضع لوحة الترخيص الهدف في موقع التزويد. موقع *التخزين‏‎* يجب أن يكون **06A01R2S1B**.

1. أكد تفاصيل التخزين، ثم حدد **موافق**.

    تتلقى رسالة "اكتمل العمل"، وتظهر تفاصيل مهمة انتقاء التزويد التالية: رقم الصنف والكمية والموقع للانتقاء منه. سيكون موقع الانتقاء هو نفسه موقع التزويد الأول. وبالتالي، سيكون للوحة الترخيص معرف لوحة الترخيص نفسه الذي تم استخدامه لمهمة عمل التزويد الأول.

1. كرر الخطوات السابقة لإكمال عمل التزويد لمهمة العمل الثانية. سوف تختلف لوحة الترخيص الهدف والكمية عن لوحة الترخيص والكمية الهدف لمهمة العمل الأولى.

بعد اكتمال عمل التزويد الثاني، ستتلقى رسالة "اكتمل العمل". يعلمك الجهاز المحمول أيضًا بعدم وجود عمل متاح، حتى لو تبقى بعض عمل التزويد. يحدث هذا السلوك لأن حالة توافر عمل التزويد هي *معلّق* وبالتالي يحمل علامة **محظور**.

تم تشغيل الحالة *معلّق* لأن قيمة ملف تعريف الموقع لموقع الانتقاء الذي تم تعيين العمل له هي **كمية تجاوز السعة** من *0.65 PL*. قامت المهمتان السابقتان لعمل التزويد بملء الموقع وصولاً إلى حد تجاوز السعة تقريبًا للصنف *T0100*. (وحدة التحويل للصنف هي *1 PL = 100 ea*.) وبالتالي، قد يتسبب عمل التزويد المتبقي في تجاوز الموقع حد تجاوز السعة.

حتى يتم انتقاء مخزون كافٍ من الموقع لخفضه إلى أقل من حد إصدار العمل على قائمة الجهاز المحمول، سيبقى عمل التزويد هذا محظورًا.

#### <a name="sales-order-pick"></a>انتقاء أمر المبيعات

قبل إتمام مهمة أمر عمل التزويد المتبقي، يجب تفريغ موقع الانتقاء من المخزون إلى مستوى حيث يمكن إلغاء حظر عمل التزويد المتبقي. بمعنى آخر ، لا يمكن لمجموع كمية المخزون الفعلي في الموقع وكمية التزويد تجاوز القيمة **قيمة تجاوز السعة**. عندما يكون هذا المجموعة أقل من كمية تجاوز السعة، سيتم حظر عمل التزويد المتبقي.

1. سجل الدخول إلى تطبيق المستودع كمستخدم في المستودع *61*. (قم بإدخال *61* كمعرف المستخدم و*1* ككلمة مرور.)
1. انتقل إلى **الصادر \> انتقاء المبيعات**.
1. ادخل معرف العمل الأول لأمر المبيعات رقم 1.

    راجع معرفات العمل الخاصة بأوامر المبيعات التي سجلتها في وقت سابق، في صفحة **تفاصيل العمل**. سيقوم معرف العمل الذي تقوم بإدخاله هنا بإنشاء عمل الانتقاء للكمية 10 وحدات من موقعين منفصلين.

1. حدد **موافق**.

    تعرض صفحة **أوامر المبيعات: انتقاء** رقم الصنف والكمية والموقع المراد الانتقاء منه للموقع الأول.

1. في الحقل **LP**، أدخل رقم لوحة الترخيص للصنف في الموقع الذي يظهر.
1. حدد الزر **موافق** (أيقونة علامة الاختيار).

    تعرض صفحة **أوامر المبيعات: انتقاء** رقم الصنف والكمية والموقع المراد الانتقاء منه للموقع التالي.

1. في الحقل **LP**، أدخل رقم لوحة الترخيص للصنف في الموقع الذي يظهر.
1. حدد الزر **موافق** (أيقونة علامة الاختيار).

    ترشدك صفحة **أوامر المبيعات: تخزين** إلى تخزين عملي الانتقاء المكتملين في الموقع المرحلي الصادر.

1. حدد **موافق**.

    سوف تستلم رسالة "اكتمل العمل".

1. ادخل معرف العمل الثاني لأمر المبيعات رقم 1.

    توجد مهمة انتقاء واحدة فقط لمعرف العمل هذا.

1. حدد **موافق**.

    تعرض صفحة **أوامر المبيعات: انتقاء** رقم الصنف والكمية والموقع المراد الانتقاء منه.

1. في الحقل **LP**، أدخل رقم لوحة الترخيص للصنف في الموقع الذي يظهر.

    ستكون لوحة الترخيص التي تحددها إحدى لوحات الترخيص التي أنشأها النظام من مهام عمل التزويد. للتأكد من التقاط المعرف الصحيح للوحة الترخيص، راجع المخزون في صفحة **قائمة المخزون الفعلي** للصنف والموقع والكمية.

1. حدد الزر **موافق** (أيقونة علامة الاختيار).
1. أكد الإرشادات الخاصة بمهمة التخزين في الموقع المرحلي الصادر.
1. حدد **موافق**.

    سوف تستلم رسالة "اكتمل العمل".

يتم حظر أمر المبيعات من الانتقاء لأن مهمة التزويد المرتبط بها غير مكتملة. في الوقت الحالي، لا يزال هناك كميه تبلغ 30 وحدة في موقع الانتقاء، وكمية التزويد لأمر المبيعات 2 هي 60 وحدة. يتجاوز مجموع المخزون الفعلي ومخزون التزويد (90 وحدة) كمية التجاوز التي تبلغ 0.65 بل (أو 65 وحدة). قبل أن يتم إكمال عمل التزويد، يجب انتقاء أمر المبيعات 3.

1. ادخل معرف العمل لأمر المبيعات رقم 3.

    توجد مهمة انتقاء واحدة فقط لمعرف العمل هذا.

1. حدد **موافق**.

    تعرض صفحة **أوامر المبيعات: انتقاء** رقم الصنف والكمية والموقع المراد الانتقاء منه.

1. في الحقل **LP**، أدخل رقم لوحة الترخيص للصنف في الموقع الذي يظهر.

    ستكون لوحة الترخيص التي تحددها إحدى لوحات الترخيص التي أنشأها النظام من مهام عمل التزويد. للتأكد من التقاط المعرف الصحيح للوحة الترخيص، راجع المخزون في صفحة **قائمة المخزون الفعلي** للصنف والموقع والكمية.

1. حدد الزر **موافق** (أيقونة علامة الاختيار).
1. أكد الإرشادات الخاصة بمهمة التخزين في الموقع المرحلي الصادر.
1. حدد **موافق**.

    سوف تستلم رسالة "اكتمل العمل".

فور أن يصبح مجموعة الكمية الفعلية في موقع الانتقاء وكمية التزويد أقل من الحد، ستتمكن من معالجة عمل التزويد المتبقي.

عد إلى صفحة **تفاصيل العمل**، ولاحظ أن توافر عمل التزويد للقطعة الأخيرة من التزويد (لأمر المبيعات 2) هي *مفتوح*، بسبب وجود مساحة كافية في الموقع لقبول التزويد.

يمكنك الآن معالجة عمل التزويد عبر الجهاز المحمول.

1. انتقل إلى **المخزون \> التزويد**.

    تتم مطالبتك بإكمال عمل التزويد المتبقي. يظهر رقم الصنف والكمية وموقع الانتقاء.

1. في الحقل **LP**، أدخل رقم لوحة الترخيص للصنف في الموقع الذي يظهر.
1. حدد الزر **موافق** (أيقونة علامة الاختيار).

    يقوم النظام بإنشاء رقم لوحة الترخيص الهدف للوحة الترخيص الجديدة للصنف المنتقى.

1. حدد **موافق** لتأكيد القيمة.

    يظهر عمل التخزين الذي يرشد المستخدم لوضع لوحة الترخيص الهدف في موقع التزويد. موقع *التخزين‏‎* يجب أن يكون **06A01R2S1B**.

1. أكد تفاصيل التخزين، ثم حدد **موافق**.

    تتلقى الرسالتين "اكتمل العمل" و"لا يوجد عمل متاح".

يمكنك الآن انتقاء أمر المبيعات رقم 2. أصبح غير محظور عند اكتمال عمل التزويد المرتبط بأمر المبيعات.

1. ادخل معرف العمل لأمر المبيعات رقم 2.

    توجد مهمة انتقاء واحدة فقط لمعرف العمل هذا.

1. حدد **موافق**.

    تعرض صفحة **أوامر المبيعات: انتقاء** رقم الصنف والكمية والموقع المراد الانتقاء منه.

1. في الحقل **LP**، أدخل رقم لوحة الترخيص للصنف في الموقع الذي يظهر.

    ستكون لوحة الترخيص التي تحددها لوحة الترخيص التي أنشأها النظام من مهمة عمل التزويد. للتأكد من التقاط المعرف الصحيح للوحة الترخيص، راجع المخزون في صفحة **قائمة المخزون الفعلي** للصنف والموقع والكمية.

1. حدد الزر **موافق** (أيقونة علامة الاختيار).
1. أكد الإرشادات الخاصة بمهمة التخزين في الموقع المرحلي الصادر.
1. حدد **موافق**.

    سوف تستلم رسالة "اكتمل العمل".

## <a name="notes-and-tips"></a>ملاحظات وتلميحات

- تعمل هذه الوظيفة مع كافة أنواع التزويد: طلب الموجة والحد الأدنى/الحد الأقصى وطلب التحميل وتقسيم المستودع.
- يمكنك تجاوز توافر عمل التزويد يدويًا لكل رأس عمل من صفحة **تفاصيل العمل** إذا كنت ترغب في ذلك.
- عندما يقوم النظام بتعيين توافر عمل التزويد، يأخذ في الاعتبار أي مخزون موجود في الموقع قبل إكمال أي عمل.
- يتم ربط كل قطة من عمل أمر المبيعات بعمل تزويد معين. لا توجد وظيفة توافر أمر مبيعات مقابل.