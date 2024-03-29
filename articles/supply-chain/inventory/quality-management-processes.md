---
title: نظرة عامة على إدارة عدم المطابقة والجودة
description: يقدم هذا المقال ميزات أداره عدم التوافق والجودة في Microsoft Dynamics 365 Supply Chain Management ويشرح كيف يمكنهم المساعدة في تحسين جوده المنتج في سلسله التوريد الخاصة بك.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling, InventNonConformanceHistory, InventNonConformanceTable, InventQualityOrderLineResults, InventQualityOrderTable, InventTestCorrection, InventTestDiagnosticType, InventTestInstrument, InventTestReportSetup, InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "11574"
- intro-internal
ms.assetid: 5ac8a059-5cb4-4cb5-ba14-b944bd08dae9
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 510dee78f6fed02e6511aedad00fcb1b15195470
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907482"
---
# <a name="quality-and-nonconformance-management-overview"></a>نظرة عامة على إدارة عدم المطابقة والجودة

[!include [banner](../includes/banner.md)]

يقدم هذا المقال ميزات أداره عدم التوافق والجودة في Microsoft Dynamics 365 Supply Chain Management ويشرح كيف يمكنهم المساعدة في تحسين جوده المنتج في سلسله التوريد الخاصة بك.

يشتمل ضمان الجودة على اختبار المنتج وإدارة المواد غير المتوافقة. وتساعد عمليات إدارة جودة في ضمان مستوى عال من جودة المنتج في سلسلة التوريد الخاصة بك. كما تساعد هذه العمليات على تحسين عمليات سلاسل التوريد وزيادة رضا العملاء. ويمكن أن تساعدك إدارة الجودة في إدارة تنظيم أوقات الإنتاج عندما تتعامل مع المنتجات غير المتوافقة، بغض النظر عن نقطة الأصل لهذه المنتجات. ويمكنك ربط نتائج التشخيص بمهام التصحيح. ‏‫ويمكن للنظام جدولة المهام لحل المشاكل، لذا يساعد على منع تكرار تلك المشاكل في المستقبل. كما تتيح إدارة الجودة تعقب المشاكل (بما في ذلك المشاكل الداخلية) حسب نوع المشكلة، وتتيح لك تحديد الحلول كقصيرة الأجل أو طويلة الأجل.‬ وتوفر إحصاءات مؤشرات الأداء الرئيسية (KPIs) رؤية في مشاكل عدم التوافق التي حدثت مسبقاً والحلول التي تم تطبيقها لتصحيحها. ويمكنك استخدام البيانات التاريخية للمساعدة على مراجعة فعالية تدابير الجودة التي تم اتخاذها سابقًا لتحديد التدابير المناسبة في المستقبل.

ويمكن أن تساعدك إدارة الجودة في إدارة تنظيم أوقات الإنتاج عندما تتعامل مع المنتجات غير المتوافقة، بغض النظر عن نقطة الأصل. ولأن أنواع التشخيص مرتبطة بالإبلاغ عن التصحيحات، بإمكان Supply Chain Management جدولة المهام لحل المشاكل ومنع تكرارها.

وبالإضافة إلى وظيفة إدارة عدم التوافق، تتضمن إدارة الجودة وظيفة تعقب المشكلات حسب نوع المشكلة (حتى عندما تكون المشكلات مشكلات داخلية)، ولتحديد الحلول قصيرة الأجل أو طويلة الأجل. وتوفر إحصاءات مؤشرات الأداء الرئيسية (KPIs) رؤية في مشاكل عدم التوافق التي حدثت مسبقاً والحلول التي تم تطبيقها لتصحيحها. ويمكنك استخدام البيانات التاريخية للمساعدة على مراجعة فعالية تدابير الجودة التي تم اتخاذها سابقًا لتحديد التدابير المناسبة في المستقبل.

عند إعداد اقتران جودة، يمكن لتطبيق Supply Chain Management إنشاء أوامر الجودة لمختلف الأعمال والأحداث والشروط. ويمكن لاقتران الجودة تغطية صنف محدد أو مجموعة محددة من الأصناف أو كافة الأصناف.

## <a name="examples-of-the-use-of-quality-management"></a>أمثلة على استخدام إدارة الجودة

تتسم إدارة الجودة بالمرونة ويمكن تنفيذها بطرق مختلفة للوفاء بمتطلبات مستويات محددة من عمليات سلاسل التوريد. توضح الأمثلة التالية الاستخدامات المحتملة لهذه الميزات:

- ابدأ تلقائيًا عملية مراقبة الجودة، استنادًا إلى معايير محددة مسبقًا (على سبيل المثال، عند تسجيل المستودع لأمر شراء من بائع معين).
- حظر المخزون أثناء الفحص لمنع استخدام المخزون غير المعتمد (الحظر الكامل لكميات أمر الشراء).
- استخدام عينات الصنف كجزء من اقتران الجودة لتحديد كمية المخزون الفعلي الحالي الذي يجب فحصه. يمكن أن يستند أخذ العينات إلى كميات ثابتة أو نسبة مئوية أو لوحة الترخيص الكاملة.
- إنشاء أوامر الجودة لإيصالات الاستلام الجزئية. لإنشاء أمر جودة يستند إلى الكمية التي تم استلامها فعليًا مع أمر ما، يجب عليك تحديد خانة الاختيار **حسب الكمية المحدثة** في صفحة **أخذ عينات للصنف**.
- إنشاء أنواع الاختبار التي تتضمن الحد الأدنى، والحد الأقصى، وقيم الاختبار المستهدفة، وإجراء اختبار النوعية مقابل الكمية الذي له نتائج تحقق محددة مسبقًا.
- تحديد مستوى جودة مقبول (AQL) للتحكم في تفاوتات قياس الجودة.
- تحديد الموارد التي تتطلب عملية فحص، مثل منطقة اختبار وأدوات الاختبار.

> [!NOTE]
> تعمل ميزة _إدارة الجودة لعمليات المستودع_ على توسيع قدرات إدارة الجودة. إذا كنت تستخدم هذه الميزة، فراجع [إدارة الجودة لعمليات المستودع](quality-management-for-warehouses-processes.md) للحصول على أمثلة حول كيفية عمل إدارة الجودة عند تمكينها.

## <a name="controlling-the-quality-management-process"></a>التحكم في عملية إدارة الجودة

فيما يلي بعض الطرق التي يمكنك من خلالها التحكم في عملية إدارة الجودة:

- إنشاء أوامر الجودة التي تستند إلى نقاط التشغيل مثل "في إيصال استلام المنتجات" للعمليات الداخلية أو "في شحن المنتج" للعمليات الخارجية.
- توثيق نتائج الاختبار، وتحديد ما إذا كانت النتائج تفي بمعايير الاختبار المحددة ومستويات الجودة المقبولة.
- استخدام إدارة المستندات لمواصفات المنتج المفصلة والملاحظات الخاصة بالمستخدم كجزء من التقارير خلال عملية الفحص.
- الاحتفاظ بالمنتجات غير المتوافقة، وربط هذه المنتجات بمعلومات إضافية لعدم التوافق لتعقب السبب الأصلي للمشكلة.
- توثيق تكلفة إدارة حالة عدم توافق. يمكن أن تشمل التكلفة الأصناف (مثل قطع الغيار)، والمصاريف المتنوعة، وساعات الجدول الزمني اللازم توافرها لتصحيح حالة عدم التوافق.
- جدولة عمليات تصحيح الأخطاء باستخدام معالجة التصحيح المرتبط بأوامر الجودة.

[![عملية إدارة الجودة.](media/quality-management-process-diagram.png)](media/quality-management-process-diagram.png)

## <a name="product-testing-and-quality-orders"></a>اختبارات المنتجات وأوامر الجودة

وعادةً ما يشار إلى اختبار المنتج بالتحكم في الجودة، ويستخدم أوامر الجودة. وباستخدام وظيفة التحكم في الجودة، يمكنك تنفيذ ما يلي:

- تحديد الاختبارات التي يجب تنفيذها للمادة. وتشمل هذه الاختبارات مواصفات الجودة ومستند الاختبار القابل للتطبيق والمستندات التي تصف الاختبار وخطة أخذ العينات ومستويات الجودة المقبولة (AQL).
- إنشاء أمر جودة لتحديد الاختبارات التي يجب إجراؤها بالنسبة لأمر معين (مثل أمر الشراء أو أمر الإنتاج) أو كمية مخزون معينة. ويمكن القيام يدويًا بإنشاء أمر جودة أو القيام تلقائيًا بتوليد أمر إنشاء بناءً على إرشادات الجودة.
- تحديد إرشادات الجودة في كل عملية تجارية (مرتبطة بالشراء أو الفحص أو أوامر الإنتاج أو أوامر التوريد) للقيام تلقائيًا بتوليد أمر الجودة الذي يحدد متطلبات إجراء الاختبار للمواد الواردة والصادرة.
- تسجيل نتائج الاختبار في أمر الجودة، والتحقق من صحة نتائج الاختبار على أساس مستوى الجودة المقبول، وطباعة شهادة تحليل تظهر نتائج الاختبار.

## <a name="nonconformance"></a>عدم المطابقة

يصف عدم المطابقة صنفًا به مشكلة في الجودة. تسمح لك عملية عدم المطابقة بإنشاء أمر عدم مطابقة يصف كمية المواد غير المطابقة ومصدر المشكلة ونوعها والملاحظات التوضيحية. ويمكنك تحديد تصنيف لأنواع المشاكل لتيسير عملية تحليل المواد غير المتوافقة. ويمكنك أيضًا طباعة علامة عدم توافق وتقرير عدم توافق لتحديد ترتيب المواد غير المتوافقة. على سبيل المثال، قد تشير العلامة والتقرير إلى شرط **غير قابل للاستخدام** أو **الاستخدام المقيد**.

يسرد الجدول التالي أنواع عدم التوافق الافتراضية الستة ويصف المعلومات التي يجب تسجيلها لكل نوع.

| نوع عدم التوافق | معلومات المصدر |
|---|---|
| العميل | رقم حساب العميل أو رقم أمر المبيعات أو رقم الدفعة الخاص بحركة أمر المبيعات. على سبيل المثال، يمكن أن يتعلق عدم التوافق بشحنة أمر توريد بعينها أو بملاحظات عميل حول جودة المنتج. |
| طلب الخدمة | رقم حساب العميل أو رقم أمر المبيعات أو رقم الدفعة الخاص بحركة أمر المبيعات. على سبيل المثال، يمكن أن يتعلق عدم التوافق بشحنة أمر توريد بعينها أو شكوى العميل من جودة الصنف. |
| المورِد | رقم حساب المورد أو رقم أمر الشراء أو رقم الدفعة الخاص بحركة أمر الشراء. على سبيل المثال، قد يتعلق عدم التوافق باستلام أمر الشراء أو تخوف المورّد بشأن الجزء الذي يقوم بتوريده. |
| الإنتاج | رقم أمر الإنتاج أو رقم الدفعة الخاص بحركة أمر الإنتاج. على سبيل المثال، يمكن أن يتعلق عدم التوافق بمجموعة محددة تم إنتاجها. |
| داخلي | رقم أمر الجودة أو رقم الدفعة الخاص بحركة أمر الجودة. على سبيل المثال، يمكن أن يتعلق عدم التوافق بالاختبارات التي يتم إجراؤها كجزء من أمر الجودة أو تخوف الموظف بشأن جودة المنتج. |
| إنتاج المنتج المساعد | يرتبط عدم توافق أمر إنتاج المنتج المساعد بأوامر الإنتاج الدُفعة. |

ترتبط حالات عدم التوافق بنوع مشكلة. ويتم أنواع المشاكل في صفحة **أنواع المشاكل**، حيث تحدد أنواع المشكلات التي يمكن أن تقترن بكل نوع من أنواع عدم التوافق. على سبيل المثال، يمكن أن تُظهر أنواع المشكلات الخاصة بحالات عدم التوافق الخاصة بنوع **طلب الخدمة** تصنيف لشكاوى العميل، في حين أنه يمكن لأنواع حالات عدم التوافق من النوع **الداخلي** أن تمثل تصنيفًا لأكواد العيوب.

وعندما تقوم بإنشاء حالة عدم توافق جديدة، تحدد نوع حالة عدم التوافق ونوع المشكلة. وحالة الموافقة المبدئية هي **جديدة**، التي تمثل طلبًا للإجراء. وتتمثل الخطوة التالية في تغيير حالة الاعتماد إلى **معتمدة** أو **مرفوضة**, للإشارة إلى أنك ستقوم أو لن تقوم باتخاذ إجراء تجاه عدم التوافق. كما يمكنك إغلاق عدم التوافق (عن طريق تحديد خانة اختيار منفصلة) للإشارة إلى أنك قد انتهيت منه، أو يمكنك إعادة فتح عدم التوافق للإشارة إلى الحاجة إلى مزيد من التفكير.

ويمكنك إدخال تعليقات لعدم توافق بإرفاق مستند. وإنها لفكرة جيدة أن يتم تحديد نوع مستند فريد لحالات عدم التوافق باستخدام صفحة **نوع المستند**. ويمكنك فيما بعد استخدام صفحة **إعداد التقرير** لتحديد ما إذا كان يجب طباعة تعليقات لنوع المستند هذا على علامة عدم التوافق وتقرير عدم التوافق. ويمكن أن يساعدك تقرير التوافق وعلامة عدم التوافق في التخلص من المواد. واختياريًا، يمكن إنشاء تقارير وعلامات استنادًا إلى معايير التحديد المقترنة بعدم التوافق. وتشمل هذه المعايير رقم وصنف وعميل ومورد وحالة عدم التوافق.

ويعرض تقرير عدم التوافق رقم وصنف ونوع مشكلة عدم التوافق. واعتماداً على نهج إعداد التقرير الخاص بك، قد يعرض التقرير أيضًا ملاحظات ذات صلة حول عدم التوافق. كما تقوم علامة عدم التوافق بعرض العلامات المشابهة، وتشمل أيضًا منطقة الفحص ونوعه (مثل **الاستخدام المقيد** أو **عدم القابلية للاستخدام**) الذي قمت بتعيينهما إلى عدم التوافق للإرشاد عبر التخلص من المواد المعيبة.

## <a name="approved-nonconformance"></a>الموافقة على عدم التوافق

يمكنك بشكلٍ اختياري تحديد عملية ذات صلة واحدة أو أكثر لعدم توافق معتمد. وتصف العملية ذات الصلة العمل الذي ينبغي أداؤه، وتحتوي على قائمة بعمليات الجودة التي قمت بتحديدها ونص وصفي حول أسباب العمل.‬ وبعد قيامك بتحديد عملية، يمكنك بشكلٍ اختياري تحديد المصاريف المتنوعة والأصناف وساعات عمل الجدول الزمني اللازمة لإنجاز العمل. ويتم عرض التكاليف المحسوبة للعملية ذات الصلة، كما يتم عرض إجمالي التكاليف المحسوبة لعدم التوافق. وتمثل التكلفة المحسوبة والتفاصيل الأساسية (حول الأصناف وساعات العمل والمصاريف المتنوعة) معلومات مرجعية تستخدم فقط داخل وظيفة إدارة الجودة.

ويمكنك بشكلٍ اختياري إنشاء أمر جودة من عدم التوافق وذلك عبر القيام أولاً باستعلام لأوامر الجودة، ثم بواسطة إنشاء أمر الجودة الجديد. على سبيل المثال، يمكن أن يحدد أمر الجودة الحاجة إلى اختبار (أو إعادة اختبار) المواد المعيبة. ويقوم أمر الجودة الذي تم إنشاؤه حديثًا بعرض الارتباط إلى عدم التوافق الأصلي.

ويمكنك بشكلٍ اختياري إنشاء ارتباط بين عدم توافق وآخر، وإنشاء عدم توافق جديد من آخر موجود. على سبيل المثال، يمكن للارتباط إظهار الاتصال المتبادل بين مشكلات الجودة.

## <a name="correction-handling"></a>معالجة التصحيح

تتيح لك صفحة **التصحيحات** إمكانية إنشاء قائمة بحالات عدم التوافق التي يجب تصحيحها. ويقترن كل صنف تصحيح بالنوع التشخيصي الذي تسبب في اكتشاف المشكلة. تحتوي صفحة **‬‏‫التصحيحات‬‏‫** على معلومات حول الذين يجب عليهم تنفيذ الإجراءات التصحيحية ووقت ذلك. ويمكنك وصف تفاصيل المشكلة والإجراءات التصحيحية المطلوبة عن طريق إرفاق مستند بالتصحيح.‬ وبعد معالجة عدم التوافق أو تصحيحها، تقوم "بإغلاق" صنف التصحيح عن طريق تحديد خيار **مكتمل**. كما يمكنك الإشارة إلى أن الحل كان حلاً قصير الأجل.

وإنها لفكرة جيدة أن يتم تحديد نوع مستند فريد للتصحيحات باستخدام صفحة **نوع المستند**. ويمكنك فيما بعد استخدام صفحة **إعداد التقرير** لتحديد ما إذا كان يجب طباعة تعليقات لنوع المستند هذا في تقرير التصحيح. ويعرض تقرير التصحيح المطبوع معلومات حول حالة عدم التوافق والملاحظات ذات الصلة بعدم التوافق. كما يتضمن التقرير معلومات التصحيح، مثل نوع التشخيص، وملاحظات التصحيح المتعلقة.

## <a name="additional-resources"></a>الموارد الإضافية

- [تمكين إدارة عدم المطابقة والجودة](enable-quality-management.md)
- [حظر المخزون](inventory-blocking.md)
- [أوامر إدخال مخزن العزل](quarantine-orders.md)
- [فحص جودة البضائع](tasks/inspect-quality-goods.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
