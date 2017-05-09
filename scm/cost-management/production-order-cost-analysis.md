---
title: "تحليل تكلفة أمر الإنتاج"
description: "توفر هذه المقالة معلومات حول تحليل التكاليف الذي يمكنك القيام به لأوامر الإنتاج الحالية والمكتملة. يمكنك تحليل التكاليف المقدرة والتكاليف الفعلية باستخدام صفحة حساب السعر أو تقرير تقديرات التكلفة والتكاليف‬. يمكنك عرض معلومات حول التكاليف المقدرة والفعلية (والكمية) لكل صنف مكون وعملية توجيه وتكلفة غير مباشرة."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-04-11 13 - 25 - 42
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79634
ms.assetid: ded5da04-f787-49f7-b5e5-75c2a2b92930
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f931432f6dc919d448ed690a1deae3d64bebe455
ms.lasthandoff: 03/29/2017


---

# <a name="production-order-cost-analysis"></a>تحليل تكلفة أمر الإنتاج

توفر هذه المقالة معلومات حول تحليل التكاليف الذي يمكنك القيام به لأوامر الإنتاج الحالية والمكتملة. يمكنك تحليل التكاليف المقدرة والتكاليف الفعلية باستخدام صفحة حساب السعر أو تقرير تقديرات التكلفة والتكاليف‬. يمكنك عرض معلومات حول التكاليف المقدرة والفعلية (والكمية) لكل صنف مكون وعملية توجيه وتكلفة غير مباشرة.

وتعتمد التكاليف الفعلية لأمر إنتاج على استهلاك المواد الذي تم الإبلاغ عنه وكذلك على عمليات التوجيه. يمكنك الوصول إلى الحركات التفصيلية حول استهلاك المواد الذي تم الإبلاغ عنه وعمليات التوجيه والتكاليف غير المباشرة لأمر إنتاج في صفحة **ترحيل الإنتاج‬**.

## <a name="variance-analysis-for-a-completed-production-order"></a>تحليل الفرق لأمر إنتاج مكتمل
تعكس الفروقات مقارنة بين أنشطة الإنتاج التي تم الإبلاغ عنها وحساب التكاليف المعيارية لصنف الإنتاج. ولا تعكس الفروقات مقارنة بالتكاليف المقدرة الخاصة بأمر الإنتاج. تتضمن أنشطة الإنتاج التي يتم الإبلاغ عنها عمليات استهلاك المواد والتوجيه، إلى جانب التكاليف غير المباشرة المقترنة وكذلك الكمية التي يتم الإبلاغ عنها كمنتهية. يتم حساب أنواع الفروقات الأربعة التالية:

-   نسبة الفرق في حجم الدفعة
-   نسبة الفرق في كمية الإنتاج
-   فرق سعر الإنتاج
-   نسبة فرق تبديل الإنتاج

يُظهر المخطط التالي أنواع الفروقات الأربعة التي تقوم بحساب الفرق بين التكاليف الفعلية لأمر الإنتاج والتكاليف المحسوبة داخل سجل تكلفة الصنف عند انتهاء أمر الإنتاج. ![الفروقات التي يتم أخذها في الاعتبار للاختلافات في أمر إنتاج مكتمل](./media/control.jpg) يمكنك تحليل فروقات الإنتاج باستخدام صفحة **الفرق** أو تقرير **فرق الإنتاج**. استخدم خيارات العرض لعرض الفروقات المفصلة حسب الصنف ومورد العمليات، أو حسب مجموعة التكلفة. يحدد نهج تصنيف التكاليف في محددات المخزون ما إذا كان تعقب الفروقات يتم حسب مجموعة التكلفة أم لا. يمكنك أيضًا استخدام خيارات العرض **فردي** و**متعدد** و**إجمالي** لعرض الفروقات الملخصة. بإمكان المعلومات حول الفروقات التفصيلية مساعدتك على فهم مصدر كل فرق. من أجل توقع الفروقات قبل إنهاء أمر الإنتاج، حلل المعلومات التفصيلية المقدمة في التقرير **تقديرات التكلفة والتكاليف**.

## <a name="cost-analysis-for-current-production-orders"></a>تحليل التكلفة لأوامر الإنتاج الحالية
وتوفر التقارير المنفصلة معلومات حول كل نوع من الحركة. استخدم هذه التقارير لتحليل التكاليف لأنشطة الإنتاج التي يتم الإبلاغ عنها. يتم عرض المعلومات فقط لأوامر الإنتاج الحالية ذات حالة **مبدوء** أو ** تم الإبلاغ عنه كمنتهٍ‬**.

-   **المواد قيد التنفيذ‬ **− يذكر هذا التقرير حركات قائمة الانتقاء التي تم الإبلاغ عنها في مقابل أوامر الإنتاج الحالية اعتبارًا من تاريخ حركة معينة. ويشير التقرير إلى كمية المكونات التي تم إصدارها ومبلغ التكلفة لكل حركة. استخدم معايير التحديد لصنف مكون مفرد. على سبيل المثال، يمكنك طباعة معلومات حول الكمية التي تم إصدارها للمكون في مقابل أوامر الإنتاج المعمول بها. لن يتم تحديث الكمية التي تم إصدارها بالكميات التي تم التبليغ عن انتهائها للصنف الأصل. وبالتالي، فقد تكون الكمية الفعلية للمواد الخام في العملية مبالغ فيها.
-   **العمل قيد التنفيذ **− يذكر هذا التقرير حركات المسار (أو حركات الوظيفة) التي تم الإبلاغ عنها في مقابل أوامر الإنتاج الحالية اعتبارًا من تاريخ حركة معينة. يشير التقرير إلى الساعات والمبلغ والكمية (كمية البضائع وكمية الخطأ) التي يتم الإبلاغ عنها لكل حركة. ويتضمن أيضًا معلومات مثل رقم العملية ومعرف العملية ومورد العمليات. علاوةً على ذلك، يُظهر هذا التقرير إجمالي الوقت والمبلغ لكافة الحركات مقابل أمر الإنتاج والكمية التي تم التبليغ عنها كمنتهية.
-   **التكاليف غير المباشرة قيد التنفيذ **− يذكر هذا التقرير التكاليف غير المباشرة التي تم تكبدها في مقابل أوامر الإنتاج. تستند هذه البيانات إلى الاستهلاك المبلغ عنه لعمليات التوجيه ومكوناته اعتبارًا من تاريخ حركة معينة. يحدد التقرير نوع التكاليف غير المباشرة (مصاريف إضافية أو رسوم) وكود كشف التكاليف غير المباشرة ومبلغ التكلفة الخاص بكل حركة. لا يوفر هذا التقرير معلومات حول حركة قائمة الانتقاء أو بطاقة المسار التي أدت إلى توليد التكلفة غير المباشرة.
-   **تكلفة الإنتاج قيد التنفيذ‬ **− يذكر هذا التقرير الاستهلاك المدمج للمواد وعمليات التوجيه والتكلفة غير المباشرة في مقابل أوامر الإنتاج اعتبارًا من تاريخ حركة معينة.
-   **الأصناف المنتهية قيد التنفيذ‬ **− يذكر هذا التقرير أوامر الإنتاج الحالية والحركات التي تم الإبلاغ عنها كمنتهية اعتبارًا من تاريخ حركة معينة.


<a name="see-also"></a>راجع أيضًا
--------

[المصادر العامة لفروقات الإنتاج](common-sources-of-production-variances.md)

