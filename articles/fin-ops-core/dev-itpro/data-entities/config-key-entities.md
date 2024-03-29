---
title: مفاتيح التكوين وكيانات البيانات
description: تصف هذه المقالة العلاقة بين مفاتيح التكوين وكيانات البيانات.
author: peakerbl
ms.date: 05/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 8083c8c053197f685985f340281c43f30053d2a5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885251"
---
# <a name="configuration-keys-and-data-entities"></a>مفاتيح التكوين وكيانات البيانات

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

قبل استخدام كيانات البيانات لاستيراد أو تصدير البيانات، ننصح بأن تحدد أولاً تأثير مفاتيح التكوين على كيانات البيانات التي تخطط لاستخدامها.

لمزيد من المعلومات حول مفاتيح التكوين، راجع [تقرير أكواد التراخيص ومفاتيح التكوين](../sysadmin/license-codes-configuration-keys-report.md).

### <a name="configuration-key-assignments"></a>مهمات مفاتيح التكوين
يمكن تعيين مفاتيح التكوين إلى واحد من المنتجات التالية أو كلها.

- كيانات البيانات
- الجداول المستخدمة كمصادر بيانات
- حقول الجدول
- حقول كيانات البيانات

يلخص الجدول التالي إلى أي مدى تغير قيم مفاتيح التكوين في المنتجات المختلفة التي تشكل كائنًا السلوك المتوقع لهذا الكائن.

| إعداد مفاتيح التكوين في كيان البيانات | إعداد مفاتيح التكوين في الجدول | إعداد مفاتيح التكوين في حقل الجدول | مفتاح التكوين في حقل كيان البيانات | السلوك المتوقع |
|-----------------------------------------|------------------------------------|------------------------------------------|----------------------------------------|------------------|
| معطل                                | غير مقيم                      | غير مقيم                            | غير مقيم                          | إذا تم تعطيل مفتاح التكوين الخاص بكيان بيانات، فلن يعمل كيان البيانات. لا يهم ما إذا تم تمكين أو تعطيل مفاتيح التكوين في الجداول والحقول الأساسية. |
| ممكّن                                 | معطل                           | غير مقيم                            | غير مقيم                          | إذا تم تمكين مفتاح التكوين الخاص بكيان بيانات، يتحقق إطار عمل إدارة البيانات من مفتاح التكوين في كل جدول من الجداول الأساسية. إذا تم تعطيل مفتاح التكوين الخاص بجدول، فلن يتوفر هذا الجدول في كيان البيانات الخاص باستخدام الوظائف. إذا تم تعطيل مفتاح تكوين جدول، لا يتم تقييم إعدادات مفاتيح تكوين كيان البيانات والجدول. إذا تم تعطيل مفتاح تكوين الجدول الرئيسي في الكيان، فسيعمل النظام كما لو أنه تم تعطيل مفتاح تكوين الكيان. |
| ممكّن                                 | ممكّن                            | معطل                                 | غير مقيم                          | إذا تم تمكين مفتاح التكوين الخاص بكيان بيانات، ويتم تمكين مفاتيح تكوين الجداول الأساسية، فسيتحقق إطار إدارة البيانات من مفتاح التكوين الخاص بالحقول الموجودة في الجداول. إذا تم تعطيل مفتاح التكوين الخاص بحقل، فلن يتوفر هذا الحقل في كيان البيانات لاستخدام الوظائف حتى إذا تم تمكين مفتاح تكوين كيان البيانات المناسب. |
| ممكّن                                 | ممكّن                            | ممكّن                                  | معطل                               | إذا تم تمكين مفتاح التكوين على جميع المستويات الأخرى، إلا أنه لم يتم تمكين مفتاح تكوين حقل الكيان، فلن يتوفر الحقل للاستخدام في كيان البيانات. |

> [!NOTE]
> إذا كان أحد الكيانات يشتمل على كيان آخر كمصدر بيانات، فإنه يتم تطبيق الدلالات السابقة بشكل متكرر.

### <a name="entity-list-refresh"></a>تحديث قائمة الكيانات
عند تحديث قائمة الكيانات، يُنشئ إطار عمل إدارة البيانات بيانات تعريف مفتاح التكوين للاستخدام في وقت التشغيل. يتم إنشاء بيانات التعريف هذه باستخدام المنطق الموضح أعلاه. نوصي بشدة بالانتظار حتى يكتمل تحديث قائمة الكيانات قبل استخدام الوظائف والكيانات في إطار عمل إدارة البيانات. إذا لم تكن تنتظر، فقد لا تكون بيانات تعريف مفتاح التكوين محدثة وقد يؤدي هذا إلى نتائج غير متوقعة. عند تحديث قائمة الكيانات، يتم عرض الرسالة التالية في صفحة قائمة الكيانات.

![تحديث قائمة الكيانات.](./media/Entity_refresh_list.png)

### <a name="data-entity-list-page"></a>صفحة قائمة كيانات البيانات
تعرض صفحة قائمة كيانات البيانات في مساحة عمل إدارة البيانات إعدادات مفاتيح التكوين الخاصة بالكيانات. ابدأ من هذه الصفحة لفهم تأثير مفاتيح التكوين في كيان البيانات.

يتم عرض هذه المعلومات باستخدام بيانات التعريف التي يتم إنشاؤها أثناء تحديث الكيان. يعرض عمود مفاتيح التكوين اسم مفتاح التكوين المقترن بكيان البيانات. إذا كان هذا العمود فارغًا، فإن هذا يعني أنه لا يوجد أي مفتاح تكوين مقترن بكيان البيانات. يعرض عمود حالة مفتاح التكوين حالة مفتاح التكوين. إذا كان العمود يشتمل على علامة اختيار، فإن هذا يعني أن المفتاح ممكَّن. إذا كان العمود فارغًا، فإن هذا يعني أما أن المفتاح معطل أو أنه ليس هناك أي مفتاح مقترن.

![صفحة قائمة الكيانات.](./media/Data_entity_list_page.png)

### <a name="target-fields"></a>الحقول الهدف
الخطوة التالية هي تصفح كيان البيانات لعرض تأثير مفاتيح التكوين في الجداول والحقول. يعرض نموذج الحقول الهدف لكيان بيانات مفتاح التكوين ومعلومات حالة المفتاح للجداول والحقول ذات الصلة في كيان البيانات. إذا تم تعطيل مفتاح تكوين كيان البيانات نفسه، يتم عرض رسالة تحذير تفيد بأن الجداول والحقول الموجودة في نموذج الحقول الهدف لهذا الكيان لن تكون متوفرة على الإطلاق بغض النظر عن حالة مفتاح التكوين الخاص بها.

![الحقول الهدف.](./media/Target_fields_1.png)

### <a name="child-entities"></a>الكيانات الفرعية 
تشتمل بعض الكيانات على كيانات أخرى كمصادر بيانات أو عبارة عن كيانات بيانات مركبة: يتم عرض معلومات مفتاح التكوين لهذه الكيانات في نموذج الكيانات التابعة. استخدم هذا النموذج بطريقة مشابهة لصفحة قائمة الكيانات الموضحة أعلاه. كما يشبه سلوك نموذج الحقول الهدف في الكيان الفرعي الموضح أعلاه.

![الحقول الهدف.](./media/Target_fields_2.png)

### <a name="using-data-entities"></a>استخدام كيانات البيانات
بعد فهم التأثير الكامل، إن وُجد، لأي مفتاح من مفاتيح التكوين في كيانات البيانات التي ترغب في استخدامها، يمكنك الآن متابعة استخدام كيانات البيانات عن طريق إضافتها إلى مشاريع البيانات. 

### <a name="run-time-validations-for-configuration-keys"></a>عمليات التحقق من الصحة في وقت التشغيل لمفاتيح التكوين
من خلال استخدام بيانات تعريف مفاتيح التكوين التي تم إنشاؤها أثناء قائمة تحديث الكيانات، يتم تنفيذ عمليات التحقق من الصحة في وقت التشغيل في حالات الاستخدام التالية.

- عند إضافة كيان بيانات إلى وظيفة
- عند قيام المستخدم بالنقر فوق "التحقق من الصحة" في قائمة الكيانات
- عند قيام المستخدم بتحميل حزمة بيانات في مشروع بيانات
- عند قيام المستخدم بتحميل قالب في مشروع بيانات
- عند تحميل مشروع بيانات موجود
- عند تحميل قالب في مشروع بيانات
- قبل تنفيذ وظيفة التصدير/الاستيراد (دُفعة، غير دُفعية، تكرار، OData)
- عند قيام المستخدم بإنشاء تعيين
- عند قيام المستخدم بتعيين الحقول في واجهة مستخدم التعيين
- عند قيام المستخدم بإضافة "حقول قابلة للاستيراد" فقط

### <a name="managing-configuration-key-changes"></a>إدارة تغييرات مفاتيح التكوين
في أي وقت تقوم فيه بتحديث مفاتيح التكوين في الكيان أو الجدول أو مستوى الحقل، فيجب تحديث قائمة الكيانات في إطار عمل إدارة البيانات. تضمن هذه العملية قيام إطار العمل بانتقاء إعدادات مفاتيح التكوين الأخيرة. حتى يتم تحديث قائمة الكيانات، فسيتم عرض التحذير التالي في صفحة قائمة الكيانات. سوف يسري مفعول تغييرات مفاتيح التكوين المحدثة مباشرةً بعد تحديث قائمة الكيانات. نوصي بأن تتحقق من صحة وظائف ومشاريع البيانات الموجودة للتأكد من أنها تعمل بالشكل المتوقع بعد سريان مفعول تغييرات مفاتيح التكوين.

![الحقول الهدف.](./media/Target_fields_3.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
