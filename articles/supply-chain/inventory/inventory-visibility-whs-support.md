---
title: دعم Inventory Visibility لأصناف WHS
description: يصف هذا الموضوع دعم رؤية المخزون للأصناف التي تم تمكينها لعمليات المستودعات المتقدمة (أصناف WHS).
author: yufeihuang
ms.date: 03/10/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: cfbff05697f4159cb74d110887b8029f28fbf96b
ms.sourcegitcommit: 1050e58e621d9a0454895ed07c286936f8c03320
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2022
ms.locfileid: "8625373"
---
# <a name="inventory-visibility-support-for-whs-items"></a>دعم Inventory Visibility لأصناف WHS

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع دعم رؤية المخزون للأصناف التي تم تمكينها لعمليات المستودعات المتقدمة (أصناف WHS). تسمى الميزة التي تضيف هذه القدرة إلى رؤية المخزون *Advanced WHS*.

## <a name="whs-items"></a>أصناف WHS

إن صنف WHS هو صنف تم تمكينه لعمليات المستودعات المتقدمة (WHS) ومعالجته في مستودع تم تمكين لـ WHS أيضًا.

لمزيد من المعلومات WHS والوحدة النمطية **إدارة المستودعات** في Microsoft Dynamics 365 Supply Chain Management، راجع [نظرة عامة على إدارة المستودعات](../warehousing/warehouse-management-overview.md).

## <a name="scope-of-the-feature"></a>نطاق الميزة

تركز ميزة WHS المتقدمة الخاصة برؤية المخزون على حسابات الكمية المتاحة التي تستند إلى الاستعلامات الفعلية. لا تهدف هذه الميزة إلى السماح لك باستخدام رؤية المخزون لإدارة أنشطة معالجة المستودعات بشكل عام. لا تعرض ميزة رؤية المخزون المفاهيم الخاصة بالمستودع لمستخدميها. فيما يلي بعض الأمثلة عن هذه المفاهيم:

- التدرج الهرمي للحجز
- ما إذا تم تمكين صنف أو مستودع لـ WHS
- معرف مجموعة تسلسلات الوحدة
- العمليات الخاصة بالمستودع، مثل الشحنات والأحمال والموجات والعمل

تستنج رؤية المخزون هذه المعلومات، بالاستناد إلى البيانات المرسلة من Supply Chain Management. لا تكون البيانات الخاصة بـ WHS (بمعنىً آخر، البيانات من جدول `WHSInventReserve`) مرئية للمستخدمين.

عند استخدام ميزة WHS المتقدمة لرؤية المخزون، ستكون جميع نتائج الاستعلام مطابقة لنتائج الاستعلامات التي تم إجراؤها مباشرةً في Supply Chain Management. ومع ذلك، لن تكون متطابقة مع نتائج الاستعلامات التي تم إجراؤها باستخدام تطبيق Warehouse Management للأجهزة المحمولة، لأن تطبيق الأجهزة المحمولة يستخدم منطق حساب مختلف قليلاً.

## <a name="when-to-use-the-feature"></a>متى يجب استخدام الميزة

من المستحسن استخدام ميزة WHS المتقدمة لرؤية المخزون في السيناريوهات التي تتحقق فيها كافة الشروط التالية:

- تقوم بمزامنة بيانات Supply Chain Management مع رؤية المخزون.
- تستخدم WHS في Supply Chain Management.
- يقوم المستخدمون بإجراء حجوزات لأصناف WHS على مستويات أخرى غير مستوى المستودع (على سبيل المثال، لأنك تستخدم عمل المستودع).

في السيناريوهات الأخرى، ستكون نتائج الاستعلام الفعلي هي نفسها، بغض النظر عما إذا كانت ميزة WHS المتقدمة لرؤية المخزون ممكّنة. بالإضافة إلى ذلك، سيكون الأداء أفضل إذا لم تقم بتمكين الميزة في هذه السيناريوهات، نظرًا لوجود عدد أقل من العمليات الحسابية ونفقات أقل.

## <a name="enable-the-advanced-whs-feature-for-inventory-visibility"></a>تمكين ميزة WHS المتقدمة لرؤية المخزون

لتمكين ميزة WHS المتقدمة لرؤية المخزون، اتبع هذه الخطوات.

1. سجل دخولك إلى Supply Chain Management كمسؤول.
1. افتح مساحة عمل [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)، ثم قم بتمكين الميزات التالية بهذا الترتيب:

    1. *تكامل رؤية المخزون*
    1. *تمكين أصناف المستودعات في رؤية المخزون*

1. انتقل إلى **إدارة المخزون \> إعداد \> معلمات تكامل رؤية المخزون**.
1. في علامة التبويب السريعة **تمكين أصناف WHS**، عيّن خيار **تمكين أصناف WHS** إلى *نعم*.
1. سجل دخولك إلى Power Apps.
1. لاستخدامها، افتح صفحة **التكوين**، ثم على علامة التبويب **إدارة الميزات**، قم بتشغيل الميزة *AdvancedWHS*.
1. في Supply Chain Management، انتقل إلى **إدارة المخزون \> مهام دورية \> تكامل رؤية المخزون**.
1. في جزء الإجراءات، حدد **تعطيل** لتعطيل رؤية المخزون بشكل مؤقت.
1. في جزء الإجراءات، حدد **تمكين** لإعادة تمكين رؤية المخزون. يُعاد تحميل الوظيفة الإضافية، وتم الآن تمكين الميزة الجديدة. تبدأ مزامنة البيانات المرتبطة بـ WHS مع رؤية المخزون.

## <a name="query-on-hand-quantities-of-whs-items"></a>الاستعلام عن الكميات المتاحة لأصناف WHS

للاستعلام عن أصناف WHS، استخدم [واجهة برمجة التطبيقات (API) نفسها وتركيب جملة الرسالة نفسها](inventory-visibility-api.md) التي تستخدمها لأصناف غير WHS. لست بحاجة إلى تحديد ما إذا كان الصنف هو صنف WHS أو غير WHS. تقوم رؤية المخزون بتمييز الأصناف تلقائيًا، بالاستناد إلى البيانات التي تم تخزينها.

وتكون نتائج الاستعلامات عن أصناف WHS بشكل أساسي مماثلة لنتائج الأصناف غير WHS. الاختلاف الوحيد هو أن المقاييس المادية التالية من مصدر بيانات `fno` تُحتسب بالاستناد إلى منطق WHS في Supply Chain Management:

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

تُحتسب جميع القياسات المادية الأخرى كما هي عندما تكون ميزة WHS المتقدمة لرؤية المخزون معطلة.

للحصول على معلومات مفصلة حول كيفية عمل الحسابات الفعلية لعمل أصناف WHS، راجع المستند التقني [الحجوزات في إدارة المستودعات](https://www.microsoft.com/download/details.aspx?id=43284).

حتى الآن، ليس بإمكان كيانات البيانات التي يتم تصديرها إلى Dataverse تحديث الكميات الخاصة بأصناف WHS. الكميات التي تظهر في كيانات البيانات صحيحة لكلٍ من الأصناف غير WHS وللكميات التي لا تتأثر بمنطق WHS (أي، القياسات باستثناء `AvailPhysical` و`AvailOrdered` و`ReservPhysical`و`ReservOrdered` في مصدر البيانات `fno`).

تُعد التغييرات التي يتم إدخالها كميات أصناف WHS المخزنة في مصدر بيانات Supply Chain Management محظورة. بالنسبة للميزات الأخرى الخاصة برؤية المخزون، يتم فرض هذا القيد للمساعدة في منع حدوث التعارضات.

## <a name="soft-reservations-on-whs-items-in-inventory-visibility"></a>الحجوزات المرنة على أصناف WHS في رؤية المخزون

بشكل عام، [الحجوزات المرنة](inventory-visibility-reservations.md) على أصناف WHS مدعومة. يمكنك تضمين القياسات المادية ذات الصلة بـ WHS في حسابات الحجوزات المرنة. 

في إطار قيد معروف، حساب *المتوفر للحجز* غير مدعوم حاليًا لأصناف WHS. وبالتالي، في حالة وجود حجز فوق الأبعاد الحالية حيث يحدث حجز مرن، حساب *المتوفر للحجز* غير صحيح. لن تتأثر الحجوزات المرنة عند تعطيل الخيار **ifCheckAvailForReserv** في [واجهة API‏‎ للحجز المرن](inventory-visibility-api.md#create-one-reservation-event).

ينطبق هذا القيد أيضًا على الميزات والتخصيصات التي تستند إلى عمليات الحجز المرنة (مثل التوزيع).

## <a name="calculate-available-to-promise-quantities"></a>حساب الكميات المتوفرة حسب التعهد

يدعم الحل بشكل كامل الكميات [المتوفرة حسب التعهد‬ (ATP)](inventory-visibility-available-to-promise.md) لأصناف WHS. يمكنك تحديد حسابات ATP دون القلق حول التفاصيل الخاصة بـ WHS.