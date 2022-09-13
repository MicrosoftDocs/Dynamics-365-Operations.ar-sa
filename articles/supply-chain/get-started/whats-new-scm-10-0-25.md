---
title: ما الجديد أو المتغير في Dynamics 365 Supply Chain Management 10.0.25 (أبريل 2022)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في 10.0.25. Microsoft Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 03/14/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: d6aa5a0cb49e5871a50a2ac5ac2c29cc09e232fc
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403640"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10025-april-2022"></a>ما الجديد أو المتغير في Dynamics 365 Supply Chain Management 10.0.25 (أبريل 2022)

[!include [banner](../includes/banner.md)]

تصف هذا المقالات الميزات الجديدة أو المتغيرة في إصدار 10.0.25 من Microsoft Dynamics 365 Supply Chain Management. رقم بنية هذا الإصدار هي 10.0.1149، وهو يتوفر كما يلي

- **إصدار المعاينة:** فبراير 2022
- **التوفر العام للإصدار (تحديث ذاتي):** مارس 2022
- **التوفر العام للإصدار (تحديث تلقائي):** أبريل 2022

## <a name="features-included-in-this-release"></a>الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي الميزات المضمنة في هذا الإصدار. قد نقوم بتحديث هذا المقال ليشمل الميزات التي تم إدراجها في البناء بعد أن يتم نشر هذا المقال في البداية.

| منطقة الميزة | الميزة | معلومات إضافية | تم التمكين بواسطة |
|---|---|---|---|
| المخزون&nbsp;و&nbsp;اللوجستيات | [تحسينات المواد الخطرة](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/hazardous-materials-enhancements) | قريبًا | إدارة الميزات:<br>*تحسينات المواد الخطرة* |
| المخزون&nbsp;و&nbsp;اللوجستيات | [أعمال التعبئة لمحطات التعبئة](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/packing-work-packing-stations) | [اعمال التعبئة لحزم الحاويات الخارجية ومعالجه شحنات](../warehousing/packing-work.md) | إدارة الميزات:<br>*أعمال التعبئة لمحطات التعبئة* |
| المخزون&nbsp;و&nbsp;اللوجستيات | [مسح الرموز الشريطية في المستودع باستخدام معايير تنسيق GS1](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [الأكواد الشريطية GS1 ورموز الاستجابة السريعة (QR)](../warehousing/gs1-barcodes.md) | إدارة الميزات:<br>*مسح رموز GS1 الشريطية* |
| التصنيع | [استهلاك المواد وإجراء الحجوزات في واجهة تنفيذ منطقة الإنتاج](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [طريقة استخدام العمال لواجهة تنفيذ طابق الإنتاج](../production-control/production-floor-execution-use.md) | إدارة الميزات:<br>*تسجيل استهلاك المواد في واجهة تنفيذ أرضية الإنتاج (خلاف WMS)*<br><br>و/أو:<br><br>إدارة الميزات:<br>*(إصدار أولي) تسجيل استهلاك المواد على واجهة تنفيذ طابق الإنتاج (تمكين WMS)* |
| التخطيط | [صيانة تقويم تحسين التخطيط المركزي](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-centralized-calendar-maintenance) | [التقويمات والتخطيط الرئيسي](../master-planning/supply-chain-calendars-master-planning.md) | ممكّن بشكل افتراضي |
| التخطيط | [تخطيط اقتراحات التحسين لتحسين التوريد الموجود](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [رسائل الإجراءات](../master-planning/action-messages.md) | ممكّن بشكل افتراضي |
| التخطيط | تم تبسيط الأوامر المخططة | [تم تبسيط الأوامر المخططة](../master-planning/planning-optimization/planned-orders-simplified.md ) | إدارة الميزات:<br>*تم تبسيط الأوامر المخططة* |

## <a name="feature-enhancements-included-in-this-release"></a>تحسينات الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي تحسينات الميزات المضمنة في هذا الإصدار. وتوفر كل واحدة منها تحسين تزايدي لميزة موجودة. ونظرًا لأنها تكون تحسينات فقط، فلن يتم سردها في [خطة الإصدار](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). ومع ذلك، لضمان عدم تعارض هذه التحسينات مع التخصيصات أو التفضيلات الموجودة لديك، يتم إيقاف تشغيل كل منها بشكل افتراضي (ما لم يذكر خلاف ذلك).

إذا كنت ترغب في تشغيل أي من هذه الميزات أو إيقاف تشغيلها، فإنه يجب عليك القيام بذلك في [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| الوحدة النمطية | اسم الميزة في إدارة الميزات | معلومات إضافية |
|---|---|---|
| إدارة المخزون والمستودعات | (بولندا) السماح بربط العديد من فواتير SAD ببند أمر شراء واحد في SAD واحد | تتيح لك هذه الميزة تقسيم بنود أوامر الشراء وربطها بمستند إداري واحد (SAD) عندما يتم ترحيل بنود أوامر الشراء هذه لعدة فواتير مختلفة (مثل الشحنات المختلفة). |
| التدبير وتحديد الموارد | تجميع طلبات الشراء المتعددة في أمر شراء واحد حسب تاريخ المحاسبة | تسمح هذه الميزة بدمج طلبات الشراء المتعددة في أمر شراء واحد إذا كانت طلبات الشراء المختلفة لها تواريخ محاسبة مختلفة. يمكن إعداد قواعد سياسة الشراء الخاصة بإنشاء أوامر الشراء وتوحيد الطلبات لأتمتة قرار تجميع بنود الطلبات حسب تاريخ المحاسبة على مستوى أمر الشراء. لا يتم دعم توحيد أوامر الشراء حسب تاريخ المحاسبة إذا تم تمكين مراقبة الميزانية لأن تاريخ المحاسبة يُستخدم لحجوزات الميزانية والعبء. وبالتالي، يجب الاحتفاظ به أثناء الانتقال من طلب الشراء إلى أمر الشراء. |
| التدبير وتحديد الموارد | عرض إعدادات حقل ردود طلبات عروض الأسعار (RFQ)‬ الافتراضية القديمة | تعيد هذه الميزة تقديم طلب عرض الأسعار الافتراضي القديم لإعدادات الحقل، التي تمت إزالتها في السابق من واجهة المستخدم. ولا توفر هذه الإعدادات أي وظائف جاهزة، ولكن يمكن تخصيصها لتقديمها كما هو المطلوب. قم بتمكين هذه الميزة إذا كانت مؤسستك قد أضافت بالفعل وظائف لإعدادات حقل الرد عل طلب عرض الأسعار الافتراضي أو إذا كانت تخطط لذلك. عند تمكين هذه الميزة، يمكنك الوصول إلى الإعدادات عن طريق الانتقال إلى الصفحة **معلمات التدبير والتوريد**، وفتح علامة التبويب **طلب عرض الأسعار**، وتحديد حقول **الرد علي طلب عرض الأسعار الافتراضي**. |
| التدبير وتحديد الموارد | دمج الأبعاد المالية من المورد مع البعد المالي لرابط البُعد النشط في أمر الشراء | تتيح لك هذه الميزة دمج الأبعاد المالية من الموردين ذوي الأبعاد المالية لارتباط البعد النشط بعد الموافقة على طلب الشراء إذا قمت بإعداد ارتباط بين بُعد مالي وبُعد مخزون الموقع. يمكن إعداد قواعد سياسة الشراء الخاصة بإنشاء أمر الشراء وتوحيد الطلب لدفع قرار دمج الأبعاد المالية من الموردين ذوي البعد المالي لرابط البعد النشط على مستوى رأس أمر الشراء. |
| التحكم بالإنتاج | (روسيا) تمكين إعداد الموقع الافتراضي لقائمة مكونات صنف/معادلة الإنتاج والاستهلاك/الحجز التلقائي للأعمال تحت التنفيذ‬ (GTD) في الإنتاج | تعمل الميزة علي تمكين الخيارات الإضافية للإنتاج من المواد الخام المستوردة (الترجمة الروسية فقط):<ul><li>خيار لتعيين الموقع الافتراضي التلقائي لصيغ الإنتاج وقوائم مكونات الأصناف في كل من مجموعات الموارد والمستودعات.</li><li>حجز تلقائي للمواد الخام بواسطة بُعد *رقم GTD* في المستودعات التي تم تنشيطها بواسطة WMS بالاستناد إلى خوارزميه الحجز غير WMS. ينطبق هذا الأمر في الحالات التي تكون فيها سياسة عمل *انتقاء المواد الخام* موجودة مع تعيين **أسلوب إنشاء العمل** إلى *أبدًا*، ويتطابق المستودع والموقع ورقم الصنف مع حركات المخزون لأمر الإنتاج (الدفعة).</li><li>الاستهلاك التلقائي للمواد الخام بواسطة بُعد *رقم GTD* عند ترحيل قائمة الانتقاء، وفقًا لعمليه الحجز المكتسبة التي ورد وصفها سابقًا.</li></ul> |
| Warehouse management | (إصدار أولي) دعم وحدة القياس لأوامر المستودعات الواردة والصادرة | تتسبب هذه الميزة في قيام النظام بإنشاء أوامر مستودعات صادرة أثناء عملية الإصدار إلى المستودع، وإنشاء أوامر مستودعات لواردة عند ترحيل أوامر النقل باعتبارها مشحونة. يقوم النظام بعد ذلك بمزامنة كل أمر مستودع صادر أو وارد مع وحدة القياس المسؤولة عن الشحن أو استلام الأمر. بعد تمكين هذه الميزة، يجب ترقية أحمال عمل التنفيذ الخاصة بالمستودع. للحصول على مزيد من المعلومات، راجع [أحمال عمل إدارة المستودعات لوحدات قياس السحابة والحافة](../cloud-edge/cloud-edge-workload-warehousing.md).<br><br>تحتاج هذه الميزة إلى ميزة *فصل عمل التخزين عن إشعارات الشحن المسبق (ASN)‬* وستمكّن القدرة على استلام أوامر النقل باستخدام عملية استلام لوحة الترخيص على تطبيق الأجهزة المحمولة Warehouse Management. |

## <a name="feature-state-changes-in-this-release"></a>التغييرات في حالة الميزات في هذا الإصدار

يسرد الجدول التالي الميزات التي أصبحت إلزامية في الإصدار 10.0.25 أو اعتبارًا منه. سيتم تشغيل جميع هذه الميزات بشكل تلقائي للنظام بمجرد التحديث إلى الإصدار 10.0.25. لا يمكن إيقاف تشغيل الميزات الإلزامية، ولكن يمكن إيقاف تشغيل الميزات قيد التشغيل بشكل افتراضي باستخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

يسرد الجدول أيضًا الميزات التي كانت موجودة سابقًا في الإصدار الأولي للاستخدام العام، ولكنها تغيرت لتصبح متاحة بشكل عام في 10.0.25، مما يعني أنه يوصى باستخدامها الآن في بيئات الإنتاج. تكون هذه الميزات متوقفة عن التشغيل بشكل افتراضي ما لم تتم ملاحظة عكس ذلك، وبالتالي عليك استخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتمكينها إذا كنت تريد استخدامها.

| الوحدة النمطية | اسم الميزة | حالة الميزة |
| --- | --- | --- |
| إدارة الأصول | [تطبيق القواعد لتجميع أوامر العمل أثناء تشغيل خطة الصيانة](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md) | متوفرة بشكل عام |
| إدارة الأصول | [تحسينات الصيانة القائمة على العداد](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md) | متوفرة بشكل عام |
| إدارة التكلفة | [مستوى حساب التكلفة](../cost-management/cost-calculation-level.md) | متوفرة بشكل عام |
| إدارة التكلفة | تمكين إعداد رقم الدُفعة المعرف من قِبَل المستخدم لعكس إقفال المخزون | متوفرة بشكل عام |
| إدارة التكلفة | [تفاصيل تقدم إقفال المخزون](whats-new-scm-10-0-21.md) | متوفرة بشكل عام |
| إدارة التكلفة | [خيارات الأبعاد المالية الافتراضية لإعادة تقييم التكلفة القياسية للمخزون](../cost-management/manage-standard-cost-updates.md) | متوفرة بشكل عام |
| إدارة التكلفة | تنظيف بيانات تقرير قيمة المخزون | قيد التشغيل بشكل افتراضي |
| إدارة التكلفة | [‏‫مساحة تخزين تقارير قيمة المخزون](../cost-management/inventory-value-report-storage.md) | قيد التشغيل بشكل افتراضي |
| إدارة التكلفة | إظهار سجل إقفال المخزون في الشبكة | قيد التشغيل بشكل افتراضي |
| إدارة التغيير الهندسي | [تمكين إدارة التغيير على المنتجات الحالية](../engineering-change-management/change-management-existing-products.md) | قيد التشغيل بشكل افتراضي |
| إدارة التغيير الهندسي | [إدارة التغيير الهندسي](../engineering-change-management/product-engineering-overview.md) | قيد التشغيل بشكل افتراضي |
| إدارة التغيير الهندسي | [إخطارات هندسية لمسؤولي الإنتاج](../engineering-change-management/engineering-change-management.md) | قيد التشغيل بشكل افتراضي |
| إدارة التغيير الهندسي | [وراثة سمات محسنة لإدارة التغيير الهندسي](../engineering-change-management/engineering-attributes-and-search.md) | قيد التشغيل بشكل افتراضي |
| إدارة التغيير الهندسي | [إدارة التغييرات في المعادلات ومكوناتها](../engineering-change-management/manage-formula-changes.md) | قيد التشغيل بشكل افتراضي |
| إدارة التغيير الهندسي | [فحوصات جاهزية المنتج](../engineering-change-management/product-readiness.md) | قيد التشغيل بشكل افتراضي |
| إدارة التغيير الهندسي | [إنشاء متغيرات للمنتجات الهندسية](../engineering-change-management/engineering-variants.md) | قيد التشغيل بشكل افتراضي |
| إدارة المخزون والمستودعات | التنقل إلى إصدار BOM من بنود BOM | إلزامي |
| التخطيط الرئيسي | [تأكيد الأوامر المجمعة وأوامر التعبئة المخططة ودمجها بطريقة دُفعية.](whats-new-scm-10-0-20.md) | متوفرة بشكل عام |
| التخطيط الرئيسي | تخطيط الموارد مع الصيانة | متوفرة بشكل عام |
| التخطيط الرئيسي | تمكين ميزات معالج إعداد الخطة الرئيسية | إلزامي |
| التخطيط الرئيسي | [تحديد نموذج التنبؤ في تفاصيل التنبؤ بالطلب](../master-planning/manual-adjustments-baseline-forecast.md) | إلزامي |
| التخطيط الرئيسي | [مرئيات تقدم التخطيط الرئيسي](../master-planning/tasks/monitor-master-planning-run.md) | إلزامي |
| التخطيط الرئيسي | [التأكيد المتوازي للأوامر المخططة](../master-planning/planning-optimization/planned-order-firming.md) | إلزامي |
| التخطيط الرئيسي | [تأكيد الأوامر المخططة بواسطة التصفية](../master-planning/planning-optimization/planned-order-firming.md) | قيد التشغيل بشكل افتراضي |
| التخطيط الرئيسي | [طرق العرض المحفوظة للأوامر المخططة](saved-views-scm.md) | قيد التشغيل بشكل افتراضي |
| التدبير وتحديد الموارد | تعطيل زر إعادة تعيين توزيع طلب الشراء | متوفرة بشكل عام |
| التدبير وتحديد الموارد | [تمكين إعادة تعيين عمليات سير العمل ذات الصلة بالتدبير](whats-new-scm-10-0-20.md) | متوفرة بشكل عام |
| التدبير وتحديد الموارد | القدرة على تأكيد أوامر الشراء المقبولة من تعاون المورد في الدفعة | إلزامي |
| التدبير وتحديد الموارد | حالة مقفلة لاتفاقية الشراء | إلزامي |
| التدبير وتحديد الموارد | إضافة بنود لفواتير أمر الشراء المقترنة باتفاقية شراء | قيد التشغيل بشكل افتراضي |
| التدبير وتحديد الموارد | إضافة حقل الكمية المطلوبة إلى صفحة إيصال استلام المنتجات | قيد التشغيل بشكل افتراضي |
| التدبير وتحديد الموارد | [السماح للموردين بالتطبيق على فئات التدبير من خلال تعاون المورد](../procurement/category-requests-from-vendors.md) | قيد التشغيل بشكل افتراضي |
| التدبير وتحديد الموارد | مبالغ التكاليف من وإلي في أوامر الشراء | قيد التشغيل بشكل افتراضي |
| التدبير وتحديد الموارد | إعداد التكاليف بالموقع والمستودع | قيد التشغيل بشكل افتراضي |
| التدبير وتحديد الموارد | تمكين حساب رسوم المشتريات وفقًا لتعريفة سنوية | قيد التشغيل بشكل افتراضي |
| التدبير وتحديد الموارد | [الطرف المسؤول عن اتفاقية الشراء](../procurement/purchase-agreements.md) | قيد التشغيل بشكل افتراضي |
| التدبير وتحديد الموارد | [طرق العرض المحفوظة لأوامر الشراء](saved-views-scm.md) | قيد التشغيل بشكل افتراضي |
| إدارة معلومات المنتج | [التحقق المُقيد من صحة كميات الأمر الافتراضية](../production-control/default-order-settings.md) | إلزامي |
| إدارة معلومات المنتج | معالجة مسبقة لتقرير قائمة مكونات الصنف لتجنب انقضاء المهلة | قيد التشغيل بشكل افتراضي |
| إدارة معلومات المنتج | الأبعاد المالية الافتراضية بشكل منفصل عند استخدام قوالب الأصناف | قيد التشغيل بشكل افتراضي |
| إدارة معلومات المنتج | تمكين مجموعات أبعاد المنتج لقوالب الأصناف المشتركة | قيد التشغيل بشكل افتراضي |
| إدارة معلومات المنتج | إعادة إنشاء أسماء متغيرات المنتجات استنادًا إلى المصطلحات | قيد التشغيل بشكل افتراضي |
| إدارة معلومات المنتج | [تحسينات صفحة اقتراحات المتغيرات](../pim/tasks/create-predefined-product-variants.md) | قيد التشغيل بشكل افتراضي |
| التحكم بالإنتاج | انتقاء كمية وزن تعبئة الإنتاج المحسنة | متوفرة بشكل عام |
| التحكم بالإنتاج | تمت إضافة زر جديد لإيقاف الفاصل إلى صفحة محطة بطاقة العمل | إلزامي |
| التحكم بالإنتاج | [تمكين إنشاء رقم لوحة الترخيص عند الإبلاغ عن الانتهاء في ‏‫جهاز بطاقة الوظيفة‬ بشكل تلقائي.](../production-control/production-floor-execution-configure.md) | إلزامي |
| التحكم بالإنتاج | تمكين الاستلام الجزئي للأصناف المتعاقد عليها من الباطن وإصلاح المشكلة المتعلقة بحساب التخريد لبنود قائمة مكونات الصنف من النوع "مورّد" | إلزامي |
| التحكم بالإنتاج | [ميزة قفل جهاز بطاقة العمل ومحطة بطاقة العمل بحيث يمكن تنظيفهما.](../production-control/production-floor-execution-configure.md) | إلزامي |
| التحكم بالإنتاج | تحسينات على مربعات حوار وظائف الموافقة والتحويل | إلزامي |
| التحكم بالإنتاج | [لوحة الترخيص للإبلاغ عند الانتهاء والمضافة إلى ‏‫جهاز بطاقة الوظيفة‬](../production-control/production-floor-execution-configure.md) | إلزامي |
| التحكم بالإنتاج | [طباعة التسمية من جهاز بطاقة الوظيفة](../production-control/production-floor-execution-configure.md) | إلزامي |
| التحكم بالإنتاج | [التنفيذ في طابق الإنتاج](../production-control/production-floor-execution-configure.md) | إلزامي |
| التحكم بالإنتاج | [وظيفة إدارة الأصول لواجهة التنفيذ في طابق الإنتاج](../production-control/production-floor-execution-configure.md) | قيد التشغيل بشكل افتراضي |
| التحكم بالإنتاج | [بحث عن وظيفة لواجهة تنفيذ صالة الإنتاج‬](../production-control/production-floor-execution-configure.md) | قيد التشغيل بشكل افتراضي |
| التحكم بالإنتاج | [تجاوز حجز الإنتاج الافتراضي](../production-control/override-default-reservation-principle.md) | قيد التشغيل بشكل افتراضي |
| التحكم بالإنتاج | [إظهار لوحة ترخيص المستخدم، والرقم التسلسلي، ورقم الدُفعة بالكامل في واجهة تنفيذ طابق الإنتاج‬](whats-new-scm-10-0-21.md) | قيد التشغيل بشكل افتراضي |
| المبيعات والتسويق | [تحسين أداء تفاصيل أمر المبيعات](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | متوفرة بشكل عام |
| المبيعات والتسويق | تحسين أداء تفاصيل عرض أسعار المبيعات | متوفرة بشكل عام |
| المبيعات والتسويق | سياسة تصدير البيانات المرجعية لأمر المبيعات | إلزامي |
| المبيعات والتسويق | [سياسة حذف أمر المبيعات إلى سطر أمر الشراء](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-purchase-order-line-deletion-policy) | إلزامي |
| المبيعات والتسويق | [سياسة تصدير البيانات المرجعية لعرض أسعار المبيعات](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy)| إلزامي |
| المبيعات والتسويق | [تحسين تصدير كيان بيانات جهة الاتصال‬](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | قيد التشغيل بشكل افتراضي |
| المبيعات والتسويق | تمكين البحث عن حقلي مقدمة وخاتمة مستند عرض أسعار المبيعات | قيد التشغيل بشكل افتراضي |
| المبيعات والتسويق | [تحسين أداء تقرير "أفضل 100" عميل](whats-new-scm-10-0-23.md) | قيد التشغيل بشكل افتراضي |
| المبيعات والتسويق | إعادة حساب رصيد العميل المقدر | قيد التشغيل بشكل افتراضي |
| المبيعات والتسويق | [تسجيل سطر أمر إرجاع المبيعات بالدقة العشرية مع وزن التعبئة وبدونه](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | قيد التشغيل بشكل افتراضي |
| المبيعات والتسويق | [طرق العرض المحفوظة للمبيعات والتسويق](saved-views-scm.md) | قيد التشغيل بشكل افتراضي |
| المبيعات والتسويق | تأكيد أمر المبيعات بنقرة واحدة | قيد التشغيل بشكل افتراضي |
| Warehouse management | [قوالب توزيع البضائع مع توجيهات المواقع](../warehousing/planned-cross-docking.md) | متوفرة بشكل عام |
| Warehouse management | [تعطيل عمليات الاستلام المتوقعة من أوامر الجودة التي تقوم بأخذ عينة من المخزون المحظور](../inventory/inventory-blocking.md) | متوفرة بشكل عام |
| Warehouse management | سجل استلام لوحة الترخيص | متوفرة بشكل عام |
| Warehouse management | [واجهة معدات معالجة المواد](../warehousing/mhax.md) | متوفرة بشكل عام |
| Warehouse management | [تقريب الكميات لأسفل إلى أقرب وحدة مبيعات عند الإصدار إلى المستودع](whats-new-scm-10-0-19.md) | متوفرة بشكل عام |
| Warehouse management | دعم وحدة القياس لقوائم عمل تطبيق المستودع | متوفرة بشكل عام |
| Warehouse management | تفاصيل ملصق موجة الشحن | متوفرة بشكل عام |
| Warehouse management | [استخدام واجهة برمجة تطبيقات أسرع لإقفال/إعادة فتح الحاويات في محطة التعبئة](whats-new-scm-10-0-21.md) | متوفرة بشكل عام |
| Warehouse management | [تحقق من صحة من القوالب المحددة لمهام التزويد](whats-new-scm-10-0-20.md) | متوفرة بشكل عام |
| Warehouse management | السماح لقالب التزويد باستخدام أعمال التزويد الفوري الحالية (عبر الوحدات) | إلزامي |
| Warehouse management | التعيين التلقائي لمعرفات GUID عند إنشاء مستخدم WHS | إلزامي |
| Warehouse management | التقاط متغيرات المنتج وأبعاد التعقب في تطبيق التخزين أثناء استلام صنف حمل العمل | إلزامي |
| Warehouse management | [تغيير حالة مخزون الأصناف التي يتم التحكم فيها بواسطة أبعاد التعقب](../inventory/inventory-statuses.md) | إلزامي |
| Warehouse management | [تغيير وعاء العمل في العمل](../warehousing/change-work-pool-on-work.md) | إلزامي |
| Warehouse management | [وضع نظام المجموعة ممتلئ](../warehousing/cluster-position-full.md) | إلزامي |
| Warehouse management | [ميزة ‏‫نظام مجموعة التخزين](../warehousing/putaway-clusters.md) | إلزامي |
| Warehouse management | [التأكيد والتحويل](../warehousing/confirm-and-transfer.md) | إلزامي |
| Warehouse management | [تأكيد الشحنات الخارجية من الوظائف الدفعية](../warehousing/confirm-outbound-shipments-from-batch-jobs.md) | إلزامي |
| Warehouse management | [التحكم في عرض صفحة ملخص الاستلام على الأجهزة المحمولة](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | إلزامي |
| Warehouse management | [المعالجة المؤجلة لعملية حركة المخزون اليدوية](../warehousing/deferred-processing-manual-inventory-movement.md) | إلزامي |
| Warehouse management | لا تسمح بإنشاء أحمال عمل لا تتطابق مع متطلبات قوالب إنشاء حمل عمل الموجة | إلزامي |
| Warehouse management | [تخطيطات تسميات لوحات الترخيص المحسّنة](../warehousing/document-routing-layout-for-license-plates.md) | إلزامي |
| Warehouse management | [تقييم جميع الإجراءات لتوجيهات مواقع وحدة SKU المتعددة](/troubleshoot/dynamics-365/supply-chain/warehousing/evaluate-multiple-location-directive-actions) | إلزامي |
| Warehouse management | إخفاء حقل القيمة الاجمالية في صفحات "كافة الحمولات" و "التفاصيل الحمل" | إلزامي |
| Warehouse management | تكوين إنشاء تسمية لوحة الترخيص | إلزامي |
| Warehouse management | التصحيح اليدوي لبند حمل العمل للمسؤول أو المستخدمين المشابهين الموثوق بهم | إلزامي |
| Warehouse management | [‏‫تحديد موضع لوحة ترخيص الموقع](../warehousing/location-license-plate-positioning.md) | إلزامي |
| Warehouse management | [خلط أبعاد المنتج في الموقع](../warehousing/location-product-dimension-mixing.md) | إلزامي |
| Warehouse management | تعيين حقل حالة المخزون لحركة مخزون الجهاز المحمول إلى قابل للتحرير | إلزامي |
| Warehouse management | [خدمة انتقاء بند المبيعات يدويًا للمسؤول أو مستخدمين موثوقين مماثلين](../warehousing/manual-order-line-picking-exception-handling.md) | إلزامي |
| Warehouse management | [منع استخدام ألواح الترخيص المشحونة لأمر تحويل في مستودعات أخرى غير مستودع الوجهة](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | إلزامي |
| Warehouse management | المطالبة بحل أسماء "الموقع/لوحة الترخيص" الملتبسة | إلزامي |
| Warehouse management | [فحص الجودة](../warehousing/quality-check.md) | إلزامي |
| Warehouse management | [إعدادات المستخدم والأيقونات وعناوين الخطوات لتطبيق المستودع الجديد](../warehousing/install-configure-warehouse-management-app.md) | إلزامي |
| Warehouse management | [مناطق مواقع إضافية](../warehousing/additional-location-zones.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | [إنشاء أوامر تحويل ومعالجتها من تطبيق المستودع](../warehousing/create-transfer-order-from-warehouse-app.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | تمكين التحقق السريع للأجهزة المحمولة للمستودع | قيد التشغيل بشكل افتراضي |
| Warehouse management | [الحد الأقصى لوقت التنفيذ لوظيفة تنظيف المستودعات المتاحة لإدارة المستودعات](../warehousing/onhand-cleanup.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | [مرئيات حمل العمل الصادر](../warehousing/outbound-workload-visualization.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | [معالجة أحداث تطبيق المستودع](../warehousing/warehouse-app-events.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | [طريقة العرض المحفوظة لمنضدة عمل تخطيط الحمل](saved-views-scm.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | [طريقه العرض المحفوظة لصفحة تفاصيل العمل](saved-views-scm.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | [طريقة العرض المحفوظة لمعالجة الموجة](saved-views-scm.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | [طرق العرض المحفوظة لمعالجة الحمل](saved-views-scm.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | [طرق العرض المحفوظة لمعالجة الشحن](saved-views-scm.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | [تفاصيل وظيفة الدفعة للموجة](../warehousing/wave-processing.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | [إخطارات تنفيذ الموجة](../warehousing/wave-execution-notifications.md) | قيد التشغيل بشكل افتراضي |

## <a name="additional-resources"></a>الموارد الإضافية

### <a name="platform-updates-for-finance-and-operations-apps"></a>تحديثات النظام الأساسي لتطبيقات التمويل والعمليات

يتضمن الإصدار 10.0.25 من Microsoft Dynamics 365 Supply Chain Management تحديثات النظام الأساسي. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.25 من تطبيقات التمويل والعمليات (أبريل 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md).

### <a name="bug-fixes"></a>إصلاح الأخطاء

للحصول على معلومات حول إصلاحات الأخطاء المضمنة في كل تحديث من التحديثات التي تعد جزءًا من 10.0.25، قم بتسجيل الدخول إلى Lifecycle Services (LCS) وعرض [مقالة قاعدة المعارف](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 وسحابات الصناعة: خطة إصدار 1 لعام 2022

هل تتساءل عن الإمكانات القادمة والتي تم إصدارها حديثًا في أيٍّ من تطبيقات العمل أو النظام الأساسي الخاص بنا؟

راجع [Dynamics 365 وسحابات الصناعة: خطة إصدار 1 لعام 2022](/dynamics365-release-plan/2022wave1/). لقد التقطنا جميع التفاصيل بشكل شامل، ومن الأعلى إلى الأسفل، في مستند واحد يمكنك استخدامه للتخطيط.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>ميزات Supply Chain Management التي تمت ازالتها وإهمالها

يوضح المقال [الميزات التي تمت ازالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) الميزات التي تمت أو تتم جدولتها لإزالتها أو إهمالها لـ Supply Chain Management.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

قبل إزالة أي ميزة من المنتج، سيتم إعلان إشعار إهمال في المقال [الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 شهرًا قبل الإزالة.

بالنسبة للتغييرات الفاصلة التي تؤثر فقط على وقت التحويل البرمجي، ولكنها متوافقة ثنائيًا مع بيئة الاختبار المعزولة وبيئات الإنتاج، فسيكون وقت الإهلاك أقل من 12 شهرًا. بشكل عام، هذه هي التحديثات الوظيفية التي يجب إجراؤها للمحول البرمجي.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

