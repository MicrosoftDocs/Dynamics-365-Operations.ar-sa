---
title: تمكين التكاليف التلقائية وتكوينها حسب القناة
description: يوضح هذا المقال كيفية تمكين التكاليف التلقائية وتكوينها حسب القناة في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 079d2bc1a5edb499181ecd69fa6448b672decbdf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275721"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a>تمكين التكاليف التلقائية وتكوينها حسب القناة

يوضح هذا المقال كيفية تمكين التكاليف التلقائية وتكوينها حسب القناة في Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>نظرة عامة

وقد تواجه وحدات سيناريو حيث يجب تطبيق رسوم التدوير أو رسوم أخرى على مجموعة من المنتجات التي يتم بيعها في جميع المتاجر أو بعضها في ولاية معينة (على سبيل المثال، كاليفورنيا). تتيح لك ميزة **تمكين تصفية التكاليف التلقائية حسب القناة** في Commerce تحديد التكاليف التلقائية حسب القناة (على سبيل المثال، قناة تقليدية معينة). هذه الميزة متوفرة في Dynamics 365 Commerce الإصدار 10.0.10 والإصدارات الأحدث.

لتمكين التكاليف التلقائية حسب القناة وتكوينها، يجب إكمال المهام التالية:

- قم بتشغيل ميزة **تمكين تصفية التكاليف التلقائية حسب القناة**.
- قم بتكوين غرض التدرج الهرمي للمؤسسة
- حدد التكاليف التلقائية حسب القناة.

> [!NOTE]
> تعمل ميزة **تمكين تصفية التكاليف التلقائية حسب القناة** فقط إذا تم تشغيل ميزة التكاليف التلقائية المتقدمة أيضًا. للحصول على معلومات حول كيفية تشغيل ميزة التكاليف التلقائية المتقدمة، راجع [التكاليف التلقائية المتقدمة ‬للقناة متعددة الاتجاهات](omni-auto-charges.md).

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a>قم بتشغيل ميزة تمكين تصفية التكاليف التلقائية حسب القناة.

لتمكين التكاليف التلقائية حسب القناة في Commerce، اتبع الخطوات التالية.

1. انتقل إلى **إدارة النظام \> مساحات العمل \> إدارة الميزات**.
1. في علامة التبويب **غير ممكّن**، في قائمة **اسم الميزة**، ابحث عن **تمكين تصفية التكاليف التلقائية حسب القناة** وحددها.
1. في الزاوية اليمنى السفلية اليمنى، حدد **تمكين الآن**. بعد تشغيل الميزة، ستظهر في القائمة الموجودة ضمن علامة التبويب **الكل**.
1. انتقل إلى **البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> جدول التوزيع**.
1. في الجزء الأيمن، ابحث عن وظيفة **1110** (**التكوين العمومي**) وحددها.
1. في جزء الإجراء، حدد **التشغيل الآن** لنشر تغييرات التكوين.

> [!WARNING]
> إذا قمت بإيقاف تشغيل ميزة **تمكين تصفية التكاليف التلقائية حسب القناة** بعد استخدامها بالفعل، سوف لن يظهر حقل **علاقة قناة البيع بالتجزئة** تحت **التكاليف التلقائية** بعد الآن، وستفقد كافة التكوينات الموجودة. إذا كانت عملية إزالة تكوينات **علاقة قناة البيع بالتجزئة** ستسبب تكرار قواعد التكاليف التلقائية، ستفشل محاولة إيقاف تشغيل هذه الميزة. قبل إيقاف تشغيل الميزة، تأكد من مراجعة كافة قواعد التكاليف التلقائية وإجراء أي تغييرات مطلوبة.

## <a name="configure-the-organization-hierarchy-purpose"></a>تكوين غرض التدرج الهرمي للمؤسسة

تم إنشاء غرض التدرج الهرمي للمؤسسة الذي يسمى **التكلفة التلقائية للبيع بالتجزئة** لإدارة التدرج الهرمي للتكاليف التلقائية حسب القناة.

لتعيين تدرج هرمي افتراضي لغرض التدرج الهرمي للمؤسسة في Commerce، اتبع هذه الخطوات.
        
1. انتقل إلى **إدارة المؤسسة** \> المؤسسات \> أغراض التدرج الهرمي للمؤسسات.
1. في الجزء الأيمن، حدد **التكلفة التلقائية للبيع بالتجزئة**.
1. تحت **التدرجات الهرمية المعينة**، حدد **إضافة**.
1. في مربع الحوار **التدرجات الهرمية للمؤسسات**، حدد تدرجًا هرميًا للمؤسسة (على سبيل المثال، **متاجر البيع بالتجزئة حسب المنطقة**)، ثم حدد **موافق**.
1. تحت **التدرجات الهرمية المعينة**، حدد **تعيين كافتراضي**.
1. انتقل إلى **البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> جدول التوزيع**.
1. في الجزء الأيمن، ابحث عن وظيفة **1040** (**المنتجات**) وحددها.
1. في جزء الإجراءات، حدد **تشغيل الآن**.
1. كرر الخطوتين السابقتين لتشغيل الوظيفتين **1070** (**تكوين القناة**) و **1110** (**التكوين العمومي**).

![تكوين غرض التدرج الهرمي لمؤسسة للتكلفة التلقائية للبيع بالتجزئة.](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a>تحديد التكاليف التلقائية حسب القناة

بعد تشغيل ميزة **تمكين تصفية التكاليف التلقائية حسب القناة** وتكوين غرض التدرج المؤسسة لـ **التكلفة التلقائية للبيع بالتجزئة**، يمكن تحديد التكاليف التلقائية حسب القناة إما على مستوى عنوان الأمر أو على مستوى بند الأمر.

لتحديد التكاليف التلقائية حسب القناة في Commerce، اتبع هذه الخطوات.

1. انتقل إلى **الحسابات المدينة \> إعداد التكاليف \> التكاليف التلقائية**.
1. في الجزء الأيمن، في حقل **المستوي**، حدد إما **رأس** أو **بند**، وفقًا لمتطلبات العمل.
1. في الحقل **كود قناة البيع بالتجزئة**، حدد كود القناة المناسب (على سبيل المثال، **جدول** أو **مجموعة**). في حال استخدام الإعداد الافتراضي **الكل**، يتم تطبيق قواعد التكلفة على كافة القنوات.

    - ذا قمت بتحديد **مجموعة‏‎**، فتأكد من إنشاء مجموعة تكاليف قناة البيع بالتجزئة في **Retail and Commerce \> إعداد القناة \> التكاليف \> مجموعات تكاليف قنوات البيع بالتجزئة**.
    - إذا قمت بتحديد **جدول**، يمكنك تحديد قناة معينة (على سبيل المثال، **سان فرانسيسكو**) في الحقل **علاقة قناة البيع بالتجزئة**.

1. انتقل إلى **البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> جدول التوزيع**.
1. في الجزء الأيمن، ابحث عن وظيفة **1040** (**المنتجات**) وحددها.
1. في جزء الإجراءات، حدد **تشغيل الآن**.
1. كرر الخطوتين السابقتين لتشغيل الوظيفتين **1070** (**تكوين القناة**) و **1110** (**التكوين العمومي**).
    
![التكاليف التلقائية المحددة حسب القناة.](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a>سيناريو كمثال

يوضح المثال التالي الخطوات المطلوبة لتكوين منتج بحيث يتم فرض رسوم إعادة التدوير عند بيع المنتج من خلال قناة سان فرانسيسكو التقليدية. يوضح المثال أيضًا كيفية ظهور التكاليف التلقائية في تطبيق نقطة البيع في Commerce.

تقوم المؤسسة بتحديد كود التكاليف المسماة **إعادة التدوير**، كما هو مبين في الرسم التوضيحي التالي.

![كود تكاليف إعادة التدوير.](media/Auto-charges-charge-code.png)

يتم إنشاء تكلفة تلقائية على مستوى البند. لها التكوين التالي:

- يتم تعيين‏‎ حقل **كود الحساب** إلى **الكل**.
- يتم تعيين‏‎ حقل **كود الصنف** إلى **جدول**.
- يتم تعيين **علاقة الصنف** إلى معرف المنتج **91001**.
- يتم تعيين‏‎ حقل **كود وضع التسليم** إلى **الكل**.
- يتم تعيين‏‎ حقل **كود قناة البيع بالتجزئة** إلى **جدول**.
- يتم تعيين حقل **علاقة قناه البيع بالتجزئة** إلى متجر  **سان فرانسيسكو**.

يتم إنشاء بند التكاليف التلقائية. لها التكوين التالي:

- يتم تعيين حقل **العملة** إلى **دولار أمريكي**.
- يتم تعيين‏‎ حقل **كود التكاليف** إلى **إعادة التدوير**.
- يتم تعيين‏‎ حقل **الفئة** إلى **ثابت**.
- ويتم تعيين حقل **التكاليف** إلى **6.25$**.

![تكوين التكلفة التلقائية على مستوى البند وبند التكاليف التلقائية.](media/Auto-charges-recyclingfee-line-fee.png)

في تطبيق نقطه البيع POS، يتم إنشاء أمر مبيعات في قناة متجر **سان فرانسيسكو**. يعرض بند **التكاليف** رسوم إعادة التدوير **$6.25**.

ومن خلال تحديد **خيارات الحركة \> التكاليف \> إدارة التكاليف** في تطبيق POS نقطه البيع، يمكنك عرض كود التكاليف ووصف رسوم إعادة التدوير.

![رسوم إعادة التدوير في تطبيق نقطة البيع POS.](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a>الموارد الإضافية

[التكاليف التلقائية المتقدمة ‬للقناة متعددة الاتجاهات](omni-auto-charges.md)

[توزيع تكاليف الرأس لمطابقة بنود المبيعات](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
