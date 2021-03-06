---
title: مراقبة تشغيل التخطيط الرئيسي
description: يوضح هذا الموضوع كيف يمكن لمخطط الإنتاج معرفه ما إذا كانت هناك عمليه تشغيل تخطيط رئيسي قيد التقدم ام لا.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cbe2c55ef9e3ed35db30ca927f3472c750c1db5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999796"
---
# <a name="monitor-a-master-planning-run"></a>مراقبة تشغيل التخطيط الرئيسي

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a>استخدام مخطط Gantt لتمثيل تقدم التخطيط الرئيسي

من صفحة **عرض تقدم التخطيط الرئيسي**، يمكنك عرض تفاصيل تشغيل التخطيط الرئيسي التاريخي كمخطط Gantt. يمكن أن تساعدك هذه الوظيفة علي فهم الوقت المستغرق في المراحل المتنوعة للتخطيط الرئيسي. بالنسبة لوظيفة التخطيط النشطة الحالية، يمكن استخدام صفحه **عرض تقدم التخطيط الرئيسي** لتعقب التقدم وعرض الوقت المتبقي المقدر.

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a>تشغيل واستخدام ميزه المرئيات لتقدم الخطة الرئيسية

لاستخدام هذه الوظيفة، اتبع الخطوات التالية:

1. في مساحة عمل **إدارة الميزات**، في علامة التبويب **جديد**، حدد **مرئيات تقدم التخطيط الرئيسي** في القائمة. إذا لم تظهر الميزة على علامة التبويب **جديد**، فانظر إلى علامتي التبويب **غير ممكن** و **الكل**.
1. حدد **تمكين الآن**. بدلاً من ذلك، حدد **جدولة**، ثم حدد الوقت الذي تريد فيه تشغيل الميزة.

يمكن لصفحة **عرض تقدم التخطيط الرئيسي** عرض كل من مهام التخطيط التاريخية ووظائف التخطيط النشطة. 

لعرض مهام التخطيط التاريخية، يوجد خياران. 

1. انتقل إلى **التخطيط الرئيسي \> إعداد \> خطط \> الخطط الرئيسية**، ثم في جزء الإجراء، حدد **المحفوظات**. من خلال تحديد المهمة المطلوبة، حدد **استعلامات**، ثم حدد **عرض التقدم**
1. انتقل إلى **التخطيط الرئيسي \> مساحات العمل \> التخطيط الرئيسي**، في تجانب التخطيط الرئيسي، انقر فوق **المحفوظات**. من خلال تحديد المهمة المطلوبة، حدد **استعلامات**، ثم حدد **عرض التقدم**

لعرض مهام التخطيط النشطة، يوجد خياران. 
1. انتقل إلى **التخطيط الرئيسي \> مساحات العمل \> التخطيط الرئيسي**، في جزء الإجراء، حدد **عمليه التخطيط غير المنتهية**. من خلال تحديد المهمة المطلوبة، حدد **استعلامات**، ثم حدد **عرض التقدم**.
1. انتقل إلى **التخطيط الرئيسي \> مساحات العمل \> التخطيط الرئيسي**، في تجانب التخطيط الرئيسي، انقر فوق **عرض التقدم**. من خلال تحديد المهمة المطلوبة، حدد **استعلامات**، ثم حدد **عرض التقدم**

لاحظ أنه يمكنك عرض الوظائف النشطة فقط عند قيام وظيفة تخطيط بالمعالجة.

### <a name="analyze-a-master-planning-job"></a>تحليل مهمة تخطيط رئيسيه

في مخطط Gantt ، يمكنك توسيع كل من عمليات التخطيط التالية لعرض تفاصيل اضافيه حول الوقت المستغرق:

- جارٍ تهيئة
- حذف بيانات وإدراجها
- التخطيط للتغطية
- التأخيرات
- رسائل الإجراءات
- إكمال
- التنفيذ التلقائي

يعتبر مخطط Gantt أداه مفيده إذا كنت ترغب في عرض تاثير استخدام رسائل الإجراءات.

#### <a name="navigation-in-the-gantt-chart"></a>التنقل في مخطط Gantt

- لتوسيع المجموعة المحددة وإظهار التفاصيل ، حدد علامة الجمع (**+**) في طريقه العرض الشجري.
- لطي المجموعة المحددة ، حدد علامة الطرح (**–**) في طريقة عرض الشجرة.
- يمكنك استخدام لوحه المفاتيح للتنقل. استخدم مفتاحي **سهم لأعلى** و **سهم لأسفل** للتنقل بين الصفوف. استخدم مفتاحي **السهم لليمين** و **السهم لليسار** لتوسيع وطي المجموعات.
- لفتح كافة المستويات في مخطط Gantt أو إغلاقها، حدد **توسيع الكل** أو **طي الكل**.
- لعرض وقت المعالجة المرتبط ، قم بالمرور فوق أحدي المهام. (تعتبر المهام هي المستوي الأدنى في مخطط Gantt.)

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a>عرض تخطيط رئيسي إضافي التشغيل لمقارنه الوظائف

ومن خلال تحديد مهمة تخطيط رئيسيه في الحقل **إظهار تشغيل التخطيط الرئيسي الإضافي**، يمكنك عرض تخطيط رئيسي إضافي في مخطط Gantt ومقارنه الوظيفتين.

#### <a name="bom-level-display"></a>العرض على مستوي قائمة مكونات الصنف

يتم عرض مستويات قائمة مكونات الصنف بشكل مختلف لتخطيط التغطية والتاخيرات والإجراءات والتاكيد.

- **تخطيط التغطية** – تظهر مستويات قائمة مكونات الصنف بالشكل المتوقع. يتم حسابها من الأعلى إلى أسفل.

    **مثال:** مستوي قائمة مكونات الصنف 0، 1، 2

- **التأخيرات** - يتم عرض مستويات قائمة مكونات الصنف علي انها مستويات قائمة مكونات الصنف لتخطيط التغطية مضروبةً في –1. (بمعني آخر، يكون لها علامة سالبة).

    **مثال:** مستوي قائمة مكونات الصنف –2، –1، 0

- **رسالة الإجراء** – تظهر مستويات قائمة مكونات الصنف بالشكل المتوقع. يتم حسابها من الأعلى إلى أسفل.

    **مثال:** مستوي قائمة مكونات الصنف 0، 1، 2

- **التأكيد التلقائي** – يتم عرض مستويات قائمة مكونات الصنف كـ 999 ناقص مستوى قائمة مكونات الصنف لتخطيط التغطية.

    **مثال:** مستوي قائمة مكونات الصنف 999، 998، 997

يلخص الجدول التالي السلوك.

| مستوي قائمة مكونات الصنف المعروض | الصنف النهائي | المكون الفرعي | المادة الخام |
|---|---|---|---|
| التخطيط للتغطية | 0 | 1 | 2 |
| التأخيرات | 0 | –1 | –2 |
| رسالة إجراء | 0 | 1 | 2 |
| التنفيذ التلقائي | 999 | 998 | 997 |

#### <a name="visualize-progress"></a>تمثيل التقدم

إذا قمت بعرض مهمة تخطيط رئيسيه قيد التشغيل حاليا، يتم عرض التقدم من خلال ألوان الموجودة في مخطط Gantt. تنطبق الألوان التالية على النسق الأزرق. بالنسبة لنسق الألوان الأخرى ، ستختلف ألوان.

- **ازرق داكن** – مهام التخطيط المكتملة.
- **برتقالي** -المهمة قيد التقدم في الوقت الحالي.
- **ازرق فاتح** - تقدير المهام المتبقية.

يتم عرض اللون فقط على المستوي الأقل في مخطط Gantt. حدد **توسيع الكل** لعرض كافة المهام الموجودة في مهمة التخطيط الرئيسية. يعتمد تقدير المهام المتبقية على وظائف التخطيط الرئيسية التاريخية.

## <a name="run-master-planning-and-track-processing-time"></a>تشغيل التخطيط الرئيسي وتعقب وقت المعالجة

1. في لوحة المعلومات الافتراضية، حدد **‏‫التخطيط الرئيسي**.
1. في حقل **الخطة**، أدخل قيمة أو حددها.
1. حدد **تشغيل**.
1. قم بتعيين خيار **تعقب وقت المعالجة** إلى **نعم**.
1. في الحقل **عدد السلاسل**، أدخل رقمًا.
1. في علامة التبويب السريعة **السجلات المُراد تضمينها**، حدد **تصفية**.
1. في الشبكة، حدد الصف الذي فيه تعيين حقل **الحقل** إلى **قم الصنف**.
1. في حقل **المعايير**، أدخل قيمة.
1. حدد **موافق**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]