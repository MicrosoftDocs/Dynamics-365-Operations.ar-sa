---
title: تفاصيل حركة المخزون
description: يوفر هذا المقال نظرة عامة على صفحة تفاصيل الحركات التي تعرض تفاصيل حركة مخزون محددة.
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventTrans, InventTransDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 55e29d5804f57cd86fb5ddac5d6c5576b7ea5f61
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859376"
---
# <a name="inventory-transaction-details"></a>تفاصيل حركة المخزون

استخدم الصفحة **تفاصيل الحركة** لعرض تفاصيل أي حركة مخزون محددة.

## <a name="open-the-transaction-details-page"></a>فتح صفحة تفاصيل الحركة

لفتح الصفحة **تفاصيل الحركة‬**، اتبع الخطوات التالية.

1. انتقل إلى **إدارة المخزون \> الاستعلامات والتقارير \> الحركات**.
1. حدد الحركة التي تريد فحصها.
1. في جزء الإجراءات، حدد **تفاصيل الحركة**.

## <a name="fasttabs-overview"></a>نظرة عامة على علامة التبويب السريعة

تنقسم صفحة **تفاصيل الحركة** إلى عدة علامات تبويب سريعة. يصف الجدول التالي غرض كل علامة تبويب سريعة.

| علامة التبويب السريعة | ‏‏الوصف‬ |
|---|---|
| عام | تعرض علامة التبويب السريعة هذه معلومات أساسية حول حركة المخزون المحددة. بالإضافة إلى الحقول التي تظهر في صفحة **حركات المخزون**، فإنها تتضمن الحقول الإضافية التي سيرد وصفها لاحقًا في هذا المقال. |
| التحديثات | تعرض علامة التبويب السريعة هذه المعلومات المتعلقة بالجوانب المادية والمالية والمتعلقة بالتسوية لحركة المخزون المحددة. قد تكون بعض الحقول فارغة بحسب الحالة الحالية للحركة. ولكن سيتم تعيين هذه الحقول بشكل تلقائي عند ترحيل الحركات. بالإضافة إلى الحقول التي تظهر في صفحة **حركات المخزون**، تتضمن علامة التبويب السريعة هذه الحقول الإضافية التي سيرد وصفها لاحقًا في هذا المقال. |
| ترحيلات دفتر الأستاذ | تعرض علامة التبويب السريعة هذه نوع الترحيل وحساب دفتر الأستاذ اللذين يتم استخدامهما للتحديث المادي والتحديث المالي والإيرادات المادية والمصروفات المادية والإيرادات المالية والمصروفات المالية المرتبطة بحركة المخزون المحددة. |
| المراجع | تعرض علامة التبويب السريعة هذه معلومات إضافية حول الحركة المصدر التي أنشأت حركة المخزون المحددة. على سبيل المثال، قد تتضمن هذه المعلومات تفاصيل من أمر الشراء أو أمر المبيعات. |
| المعلومات ذات الصلة | تعرض علامة التبويب السريعة هذه معلومات إضافية حول حركة المخزون المحددة. قد لا يتم تعيين هذه الحقول إذا كنت لا تستخدم بعض الميزات، مثل فئات التدبير أو المشاريع. |
| أبعاد مالية - فعلية | تعرض علامة التبويب السريعة هذه قيم الأبعاد المالية التي تم استخدامها عند ترحيل التحديث الفعلي. إذا لم يتم ترحيل التحديث الفعلي، فستكون الحقول فارغة. |
| أبعاد مالية - مالية | تعرض علامة التبويب السريعة هذه قيم الأبعاد المالية التي تم استخدامها عند ترحيل التحديث المالي. إذا لم يتم ترحيل التحديث المالي، فستكون الحقول فارغة. |
| أبعاد المخزون | تعرض علامة التبويب السريعة هذه قيم أبعاد المخزون التي تم تعيينها لحركة المخزون المحددة. تتضمن هذه القيم الموقع والمستودع والحجم واللون والتكوين والموقع ورقم الدُفعة والرقم التسلسلي وحالة المخزون ولوحة الترخيص والمالك. |

## <a name="fields-on-the-general-fasttab"></a>الحقول في علامة التبويب السريعة "عام"

يصف الجدول التالي الحقول على علامة التبويب السريعة **عام** التي لا تظهر أيضًا في صفحة **حركات المخزون**.

| الحقل | ‏‏الوصف‬ |
|---|---|
| الطرف | اسم الطرف ذي الصلة لحركة المخزون المحددة. على سبيل المثال، تعرض حركة أمر الشراء اسم المورّد في أمر الشراء، بينما تعرض حركة أمر المبيعات اسم العميل. لا يتوفر هذا الحقل لكافة أنواع حركات المخزون. |
| مرجع المخزون | عند وجود حركة مخزون أخرى مرتبطة بحركة المخزون المحددة، نوع تلك الحركة. علي سبيل المثال، إذا تم وضع علامة على أمر شراء في مقابل أمر مبيعات، فسيتم تعيين حقل **مرجع المخزون** لحركة أمر الشراء إلى *أمر مبيعات*. يحدث وضع العلامات تلقائيًا لأوامر التسليم المباشرة والأوامر بين الشركات الشقيقة. عند استخدام وضع العلامات مع أساليب تحديد التكلفة غير *التكلفة القياسية* و *المتوسط المتحرك*، سيقوم النظام بإنشاء التسويات والتعديلات على الحركات المحددة التي تم وضع علامة عليها. بهذه الطريقة، يمكنك تحديد التكلفة "الفعلية" التي تتجاوز منطق ما يرد أولاً يصرف أولاً (FIFO)؛ أو ما يرد أخيرا يصرف أولاً أو المتوسط المرجح. |
| رقم المخزون | الحركة المحددة المرتبطة بحركة المخزون المحددة. علي سبيل المثال، إذا تم وضع علامة على أمر شراء في مقابل أمر مبيعات، فسيتم تعيين حقل **رقم المخزون** لحركة أمر الشراء إلى رقم أمر المبيعات. |
| معرف المشروع | إذا كانت حركة المخزون المحددة مرتبطة بمشروع، فسيتم تعيين هذا الحقل إلى رقم المشروع. |
| كود الدفعة | معرف الشحنة الفريد الذي قام النظام بتعيينه إلى حركة المخزون المحددة. |
| دفعة المرجع | عند وجود حركة مخزون أخرى مرتبطة بحركة المخزون المحددة، معرف الشحنة لتلك الحركة. علي سبيل المثال، إذا تم وضع علامة على أمر شراء في مقابل أمر مبيعات، فسيكون حقل **دفعة المرجع**‬ لحركة أمر الشراء قيمة **كود الشحنة‬** لحركة مخزون بند أمر المبيعات. |
| رقم البُعد | معرّف فريد يمثل مجموعة كل قيم أبعاد المخزون التي تم تعيينها لحركة المخزون المحددة. |
| قيمة مفتوحة | قيمة تشير إلى ما إذا كانت حركة المخزون المحددة قد تمت تسويتها بواسطة عملية إقفال المخزون. إذا تم تعيين هذا الحقل إلى *نعم*، فهذا يعني أن تسوية الحركة لم تتم. |
| التاريخ المتوقع | بالنسبة لحركات إيصالات الاستلام، التاريخ الذي من المتوقع أن يحدث فيه إيصال استلام المخزون. على سبيل المثال، قد يُظهر هذا الحقل تاريخ الاستلام المتوقع في أمر حظر المخزون أو تاريخ التسليم في بند أمر الشراء. |
| تاريخ المخزون | يتم تعيين هذا الحقل عند إجراء حركة تسجيل في أمر الاستلام قبل ترحيل إيصال فعلي. |
| تحويل غير مالي | قيمة تشير إلى ما إذا كانت حركة المخزون المحددة هي تحويل غير مالي. يحدث التحويل غير المالي عندما لا يتم تعقب تغيير في أبعاد المخزون ماليًا في صفحة **مجموعة نماذج الصنف**. |
| معرف دفعة التحويل | إذا كانت حركة المخزون المحددة عبارة عن تحويل غير مالي، يتم تعيين هذا الحقل إلى قيمة **كود الشحنة** لحركة المخزون الأخرى التي تتم تسوية المعاملة المحددة مقابلها. |

## <a name="fields-on-the-updates-fasttab"></a>الحقول في علامة التبويب السريعة "تحديثات"

يصف الجدول التالي الحقول على علامة التبويب السريعة **تحديثات** التي لا تظهر أيضًا في صفحة **حركات المخزون**.

| الحقل | ‏‏الوصف‬ |
|---|---|
| الإيصال الفعلي | رقم الإيصال من دفتر الأستاذ العام حيث تم إنشاء الترحيل الفعلي لحركة المخزون المحددة. |
| المسار | المسار المرتبط بحركة المخزون المحددة. تم تعيين هذا الحقل فقط لحركات قائمة انتقاء الإنتاج حيث ترتبط قائمة مكونات الصنف (BOM) أو بند الصيغة بصنف معين. |
| إيصال التعبئة | رقم إيصال التعبئة الذي تم إدخاله لحركة استلام منتج أمر شراء. |
| مبلغ تكلفة المخزون الفعلية | المبلغ الذي تم ترحيله إلى دفتر الأستاذ العام للتحديث الفعلي. بالنسبة لمنتج التكلفة القياسية، يمثل هذا المبلغ التكلفة القياسية. بالنسبة لأساليب التكلفة الأخرى، إنها تمثل المتوسط المرجح للمنتج في وقت الترحيل. |
| إيراد فعلي | المبلغ الإيرادات المؤجلة‬ الذي تم ترحيله إلى دفتر الأستاذ العام للتحديث الفعلي. |
| معرف الحمولة | إذا كانت الحركة الحالية مرتبطة بحمل في إدارة النقل، فسيعرض هذا الحقل الرقم الفريد للحمل الذي تضمن الصنف. |
| مرحل فعليًا | قيمة تشير إلى ما إذا كان قد تم ترحيل حركة المخزون المحددة بشكل فعلي. إذا تم ترحيل الحركة الحالية إلى دفتر الأستاذ العام، سيكون هناك أيضًا إيصال فعلي. |
| مرحل ماليًا | قيمة تشير إلى ما إذا كان قد تم ترحيل حركة المخزون المحددة بشكل مالي. إذا تم ترحيل الحركة الحالية إلى دفتر الأستاذ العام، سيكون هناك أيضًا إيصال مالي. |
| تم ترحيل رسوم فعلية | قيمة تشير إلى ما إذا كان قد تم ترحيل المصروفات المادية المرتبطة بحركة المخزون المحددة أم لا. |
| تم ترحيل رسوم مالية | قيمة تشير إلى ما إذا كان قد تم ترحيل المصروفات المالية المرتبطة بحركة المخزون المحددة أم لا. |
| الإيصال المالي | رقم الإيصال في دفتر الأستاذ العام الذي تم إنشاء الترحيل المالي فيه. |
| الفاتورة | رقم الفاتورة التي تم إنشاؤها، على سبيل المثال، بالنسبة لأمر شراء أو أمر مبيعات. |
| تسوية | المبلغ الذي تم تعديله في حركة المخزون المحددة من عملية إقفال وتعديل المخزون. |
| الأرباح والخسائر، المبلغ المرحل | مقدار حركة المخزون المحددة التي تم ترحيلها إلى بيان الأرباح والخسائر. |
| فاتورة غير مرحلة | رقم الفاتورة لأمر الشراء المرتبط الذي يظهر في الصفحة **فاتورة المورّد المعلقة**. |
| مُقفل ماليًا | تاريخ تسوية الحركة بالكامل. |
| كمية وزن التعبئة المغطاة | كمية وزن التعبئة‬ التي تغطيها التسوية. |
| الكمية التي تمت تسويتها | الكمية التي تمت تسويتها لحركة المخزون المحددة. |
| المبلغ الذي تمت تسويته | القيمة التي تمت تسويتها لحركة المخزون المحددة. |
