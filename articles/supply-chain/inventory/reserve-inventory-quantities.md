---
title: حجز كميات المخزون
description: يصف هذا المقال الخيارات المختلفة المتوفرة لحجز المخزون.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 207264
ms.assetid: 47537e4f-cdf6-4813-96fd-c945b2dfe9d4
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0c0e283189998473469164398fa6f43c8e8825e
ms.sourcegitcommit: 3a882de1f1c27654a8e92ebc1999c75678cc9a53
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/27/2022
ms.locfileid: "9201855"
---
# <a name="reserve-inventory-quantities"></a>حجز كميات المخزون

[!include [banner](../includes/banner.md)]

يصف هذا المقال الخيارات المختلفة المتوفرة لحجز المخزون.

يمكن تلقائيًا حجز كميات مخزون لأمر توريد محدد. ويعني هذا أنه لا يمكن سحب المخزون المحجوز من المستودع لأوامر أخرى إلا إذا تم إلغاء حجز المخزون أو جزء منه.

هناك أسباب كثيرة لحجز المخزون:
-   ما يُطلب أولاً يُسلم أولاً، مما يعني أن العملاء يحصلون على الأصناف المتوفرة بنفس ترتيب طلبهم لتلك الأصناف.
-   نقص الأصناف بسبب طول مدة التسليم أو عدم معرفة وقت التسليم من المورّد. قد ترغب في التأكد من حصول عملاء أو أوامر محددة على أول الأصناف المتوفرة.
-   وجود أولوية للتسليم أولاً لعملاء محددين أو لنوعيات محددة من الأوامر.
-   الأصناف التي تحتوي على أرقام تسلسلية أو أرقام مجموعات. يمكن تمييز أصناف محددة تم أو سيتم تسليمها لأوامر بعينها.
-   الأصناف المطلوبة خصيصًا التي تم حجزها لأوامر محددة.
-   أوامر الإنتاج. على سبيل المثال، يمكنك وضع علامة على الأصناف التي تم إنتاجها وتعديلها لتلبية أوامر معينة.

يمكن حجز المخزون تلقائيًا عندما يتم إنشاء بند أمر جديد، أو يمكن حجز المخزون يدويًا لأوامر فردية. ‬‏‫من الممكن أيضًا حجز المخزون في مراحل مختلفة من عملية الإنتاج.‬‏‫ يمكن حجز المنتجات المخزنة فقط. ولا يمكن حجز الخدمات، نظرًا لعدم وجود مخزون فعلي. يمكن حجز المخزون لكل من المخزون المادي الفعلي والمخزون الذي تم طلبه، ولم يُستلم حتى الآن. إذا تم حجز كمية أكبر من الكمية التي يحتويها المخزون الفعلي، فستظهر رسالة تفيد بتعذر حجز مثل تلك الكمية الكبيرة. يمكن عندئذٍ إما حجز تلك الكمية بأية طريقة، أو تغيير الكمية المطلوبة. من الممكن حجز الكمية أو تغييرها. إذا تم حجز عدد من الأصناف يزيد عن تلك المتوفرة، فستتم تغطية النقص في المرة القادمة التي تتوفر فيها تلك الأصناف عند التسليم.

## <a name="inventory-reservation-policies"></a>سياسات حجز المخزون
يتم تعيين سياسات حجز المخزون في صفحة **مجموعات نموذج الصنف** وصفحة **محددات إدارة المستودعات والمخزون‬** وصفحة **محددات الإنتاج**.
### <a name="policies-on-the-item-model-groups-page"></a>السياسات في صفحة مجموعات نماذج الصنف‬

يحتوي المقطع **سياسات المخزون** على سياسات الحجز التالية.

| &nbsp;                  | &nbsp;                                                                                                                                     |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **سياسة الحجز**  | **الوصف**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| FIFO المتحكَّم فيه حسب التاريخ    | إذا حددت الخيار **FIFO المتحكَّم فيه حسب التاريخ‬**، فسيتم التحكم في حجز المخزون بواسطة تاريخ فرز وفقًا لمبدأ ما يرد أولاً يصرف أولاً‬ (FIFO). يتم حجز الدُفعات استنادًا إلى أقرب تاريخ لاستلام الأصناف وفقًا لمبدأ ما يرد أولاً يصرف أولاً‬ (FIFO).                                                                                                                                                                                                                                                                       |
| تراجع عن تاريخ الشحن | يصبح هذا الخيار متوفرًا إذا حددت الخيار **FIFO المتحكَّم فيه حسب التاريخ‬**. إذا حددت الخيار **تراجع عن تاريخ الشحن‬**، فسيتم حجز المخزون بأثر رجعي من تاريخ الشحن المطلوب وفقا لمبدأ ما يرد أخيرًا يصرف أولاً‬ (LIFO). إذا لم تتوفر أي عملية استلام قبل تاريخ الشحن، فسيتم استخدام الحجز وفقًا لمبدأ ما يرد أولاً يصرف أولاً‬ (FIFO).                                                                                                                                                                                                           |
| حجز مبيعات الصنف  | يحدد هذا الخيار ما إذا كان حجز الأصناف يتم يدويًا أو تلقائيًا. إذا كان الحجز تلقائيًا، فسيتم حجز المخزون عند إنشاء بنود الأمر. ويمكن إجراء عمليات الحجز على مستوى رقم الصنف لقوائم مكونات الصنف (الخيار **تلقائي**)، أو للعناصر الفردية في قائمة مكونات الصنف (الخيار **تحديد إجمالي المكونات المطلوبة‬**). قد تكون قيمة **حجز مبيعات الصنف** الافتراضية متوارثة من **معلمات الحسابات المدينة.** على هذه الصفحة، يتم تعيين القيمة في حقل "الحجز" في **المقطع** **قيم المبيعات الافتراضية** على علامة التبويب **عام**. |
| تحديد الدفعة ذاتها    | يتيح لك حجز نفس الدُفعة إمكانية حجز مخزون لبند أمر مبيعات مقابل دُفعة واحدة من المخزون. إذا أردت استخدام هذا الخيار، فيجب أيضًا تعيين الخيار **دمج المتطلبات‬** إلى **نعم**. هناك إعدادات إضافية مطلوبة لمجموعة بُعد التعقب‬ ومجموعة أبعاد التخزين. لمزيد من المعلومات، راجع [حجز نفس الدُفعة لأمر مبيعات](../sales-marketing/reserve-same-batch-sales-order.md).                                                          |
| دمج المتطلبات | يُعد هذا الخيار مماثلاً للخيار **تحديد الدفعة ذاتها‬**، ويدمج المخزون المحجوزة لبنود أمر المبيعات في مطلب واحد.                                                                                                                                                                                                                                                                                                                                                                                      |
| ما تنتهي صلاحيته أولاً يصرف أولاً المتحكَّم فيه حسب التاريخ    | يسمح لك هذا الخيار بحجز الدُفعات التي تقترب من تاريخ انتهاء الصلاحية أو تاريخ الأفضلية. تحتاج أيضًا إلى تعيين الحقل **معايير الانتقاء‬** إلى **تاريخ انتهاء الصلاحية** أو **تاريخ الأفضلية**.                                                                                                                                                                                                                                                                                                                              |

#### <a name="example-for-fifo-date-controlled-and-backward-from-ship-date"></a>مثال لخيار FIFO المتحكَّم فيه حسب التاريخ‬ وخيار التراجع عن تاريخ الشحن‬

في هذا المثال، يوجد مخزون فعلي لرقم الصنف أ لثلاثة أرقام دُفعات مختلفة.

| رقم الصنف | رقم الدُفعة | الكمية | التاريخ             |
|-------------|--------------|----------|------------------|
| أ           | 1000         | 5        | 2 فبراير 2016 |
| أ           | 1001         | 3        | 1 يناير 2016  |
| أ           | 1002         | 7        | 3 مارس، 2016    |

يقوم أمر المبيعات الذي ينبغي حجزه تلقائيًا وتسليمه في 4 أبريل 2016 بحجز الدُفعة التالية:
-   في حال تم إلغاء تحديد خانتي الاختيار **FIFO المتحكَّم فيه حسب التاريخ‬** و **‏‫تراجع عن تاريخ الشحن‬**، فسيتم حجز الدُفعة 1000 لأنها الدُفعة بأقل رقم.
-   في حال تم تحديد خانة الاختيار **FIFO المتحكَّم فيه حسب التاريخ‬** وإلغاء تحديد خانة الاختيار **تراجع عن تاريخ الشحن**، فسيتم حجز الدُفعة 1001 لأنها الدُفعة ذات أول تاريخ استلام (FIFO)
-   في حال تم تحديد خانتي الاختيار **FIFO المتحكَّم فيه حسب التاريخ‬** و **‏‫تراجع عن تاريخ الشحن‬**، فسيتم حجز الدُفعة 1002 لأن تاريخ استلام الدُفعة هو الأقرب إلى تاريخ شحن أمر المبيعات.

### <a name="policies-on-the-inventory-and-warehouse-management-parameter-page"></a>السياسات في صفحة محددات إدارة المستودعات والمخزون‬

هناك خياران يتعلقان بعمليات الحجز في صفحة **محددات إدارة المستودعات والمخزون‬**:
-   يسمح لك الخيار **حجز الأصناف المطلوبة‬** على علامة التبويب **عام** بحجز عمليات استلام الأصناف التي تم طلبها في مقابل إصدارات الأصناف في الحسابات المدينة، وإدارة المشاريع والمحاسبة، ومراقبة الإنتاج. وإذا قمت بإلغاء تحديد هذا الخيار، فيمكنك فقط حجز الأصناف التي تم استلامها فعليًا. وفي حالة إعداد صنف معين لقبول مخزون سالب، لا يكون هذا الحقل ذا صلة.
-   يحدد الخير **حجز الأصناف تلقائيًا‬** على علامة التبويب **التحويل‬** الإعداد الافتراضي إذا تم حجز الأصناف تلقائيًا لأوامر التحويل. يمكن تجاوز الإعداد الافتراضي في أوامر التحويل الفردية.

### <a name="inventory-reservation-policies-on-the-production-parameters-page"></a>سياسات حجز المخزون في صفحة محددات الإنتاج

تحدد قيمة حقل **الحجز** على علامة التبويب **عام** في صفحة **محددات الإنتاج** النقطة الافتراضية في عملية الإنتاج التي يجب حجز المخزون عندها. على سبيل المثال، يمكن حجز المخزون عند جدولة العمل أو عند بدء العمل.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
