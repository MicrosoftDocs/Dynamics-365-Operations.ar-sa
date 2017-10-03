---
title: "مواصفات التشغيلة"
description: "توفر هذه المقالة معلومات حول مواصفات التشغيلة. مواصفات التشغيلة هي الصفات المميزة للمواد الخام والمنتجات التامة الصنع والتي تشكل مجموعات المخزون. كما توضح هذه المقالة كيفية تعيين مواصفات التشغيلة، وكيف يمكنك البحث فيها عند حجز الدُفعات."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 80e64323700dad5cb93539a46fdc858a6f555a34
ms.contentlocale: ar-sa
ms.lasthandoff: 05/25/2017

---

# <a name="batch-attributes"></a>مواصفات التشغيلة

[!include[banner](../includes/banner.md)]


توفر هذه المقالة معلومات حول مواصفات التشغيلة. مواصفات التشغيلة هي الصفات المميزة للمواد الخام والمنتجات التامة الصنع والتي تشكل مجموعات المخزون. كما توضح هذه المقالة كيفية تعيين مواصفات التشغيلة، وكيف يمكنك البحث فيها عند حجز الدُفعات.

مواصفات التشغيلة هي الصفات المميزة للمواد الخام والمنتجات التامة الصنع والتي تشكل مجموعات المخزون. ويمكن أن تختلف المواصفات التشغيلية، تبعاً لعوامل مثل الظروف البيئية، أو جودة المواد الخام التي تُستخدم لإنتاج الدُفعة، أو نتيجة المنتج النهائي. عدد وأنواع المواصفات التشغيلية المستخدمة يمكن أن تتفاوت تفاوتاً كبيرًا من صناعة إلى أخرى. فيما يلي مثالين يوضحان كيفية استخدام المواصفات التشغيلية:

-   في صناعة الجبن، يمكن أن يشتمل اللبن، وهو من المواد الخام التي تُستخدم لإنتاج الجبن، على سمات مثل وزن محتوى الدهون والوزن بالنسبة المئوية. ويمكن أن يشتمل الجبن الذي تم إنتاجه من الحليب سمات أخرى، مثل الرطوبة والعمر.
-   وفي صناعة الصلب، قد يشمل الحديد سمات مثل النسب المئوية لمحتوى الماغنسيوم، ومحتوى الفضة، ومحتوى الزنك.

ولإدارة عدد وأنواع السمات بشكل أفضل، يمكنك استخدام مجموعات المواصفات التشغيلية. وبهذه الطريقة، لا يلزمك إضافة كل سمة على حدة.

## <a name="assign-batch-attributes"></a>تعيين المواصفات التشغيلة
يمكنك تعيين المواصفات التشغيلية للمنتجات الفردية التي يُحتفظ يها في دُفعات المخزون، أو يمكنك تعيينها للمنتجات المرتبطة بعملاء معينين. وقبل تعيين مواصفة تشغيلية على مستوى العميل، يجب تعيينها على مستوى المنتج. يجب تعيين المنتج على مجموعة أبعاد الدُفعة إلى **نشطة** في مجموعة أبعاد التعقب. ولتعيين مواصفة تشغيلية لمنتج واحد، استخدم الصفحة الخاصة بالمنتج. وإذا كانت السمة خاصة بمنتج عميل، استخدم الصفحة الخاصة بالعميل. وعند إضافة سمة إلى منتج، يمكنك أيضًا تحديد معلمات أخرى. فيما يلي بعض الأمثلة:

-   الحد الأدنى والحد الأقصى للسمة من نوع **العدد الصحيح** أو **الكسر**.
-   ‏‫إجراءات التفاوت للسمة من نوع **العدد الصحيح** أو **الكسر‬‏‫**. إذا كانت قيمة السمة تقع خارج نطاق الحد الأدنى والحد الأقصى، يمكن أن يكون الإجراء إما رسالة تحذير أو رسالة خطأ.‬
-   القيمة الهدف للسمة. هذه القيمة هي القيمة المثلى للسمة، ويتم تطبيقها على كافة أنواع السمات.

يمكنك الوصول إلى صفحات المنتجات التي تحددها في صفحة **المنتجات التي تم إصدارها** في إدارة معلومات المنتج. وبعد تعيين المواصفات التشغيلية لمنتج، يمكنك إضافة قيم معينة إلى السمات في صفحة **المواصفات التشغيلية للمخزون**.

## <a name="reserve-batches"></a>حجز الدُفعات
يمكنك البحث في المواصفات التشغيلية عند قيامك بإجراء عمليات حجر الدُفعات لأمر مبيعات لتنفيذ أمر عميل أو عند انتقاء وحجز الدُعات لأمر إنتاج. ويساعد البحث في تحديد موقع دُفعة مخزون الذي يحتوي على المنتج الذي يحتوي على المواصفة التشغيلية التي تريدها. وبعد تحديد موقع الدُفعة أو الدُفعات، يمكنك حجز المنتج لبند حركة المخزون الأصلي.



