---
title: ما الجديد أو المتغير في Dynamics 365 Supply Chain Management 10.0.29 (أكتوبر 2022)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في 10.0.29. Microsoft Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 08/12/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d12932f35b3b451577d38948f60bc3a73c10e2a0
ms.sourcegitcommit: 86c0562ce1ecdf7937125c0f5a6771f178b459e7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/24/2022
ms.locfileid: "9714823"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10029-october-2022"></a>ما الجديد أو المتغير في Dynamics 365 Supply Chain Management 10.0.29 (أكتوبر 2022)

[!include [banner](../includes/banner.md)]

يصف هذا المقالا الميزات الجديدة أو المتغيرة في إصدار 10.0.29 من Microsoft Dynamics 365 Supply Chain Management. رقم بنية هذا الإصدار هي 10.0.1326، وهو يتوفر وفق الجدول التالي:

- **إصدار أولي الإصدار:** أغسطس 2022
- **التوفر العام للإصدار (تحديث ذاتي):** سبتمبر 2022
- **التوفر العام للإصدار (تحديث تلقائي):** أكتوبر 2022

## <a name="features-included-in-this-release"></a>الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي الميزات المضمنة في هذا الإصدار. قد نقوم بتحديث هذا الموضوع ليشمل الميزات التي تمت إضافتها إلى البنية بعد نشر هذا الموضوع.

| منطقة الميزة | الميزة | معلومات إضافية | تم التمكين بواسطة |
|---|---|---|---|
| المخزون واللوجستيات | [تخصيص عناصر WMS والاحتفاظ بها في رؤية المخزون](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/allocate-reserve-whs-items-inventory-visibility) | قريبًا | ممكّن بشكل افتراضي |
| المخزون واللوجستيات | [تحميل مسبق لقوائم المخزون الفعلي الانسيابية](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/query-inventory-visibility-summary-entity) | [استخدام تطبيق Inventory Visibility](../inventory/inventory-visibility-power-platform.md) | تم التمكين من خلال تكوين الخدمة |
| التنفيذ التلقائي للتوريد حسب الأمر | [التنفيذ التلقائي للتوريد حسب الأمر](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-to-order-supply-automation) | [التنفيذ التلقائي للتوريد حسب الأمر](../master-planning/make-to-order-supply-automation.md) | إدارة الميزات:<br>*التنفيذ التلقائي للتوريد حسب الأمر* |
| التخطيط | [عرض الرؤى التفصيلية وتطبيقها لدمرب](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/view-apply-detailed-insights-ddmrp) | [نظرة عامة على تخطيط متطلبات المواد المدفوعة بالطلب](../master-planning/planning-optimization/ddmrp-overview.md) | إدارة الميزات:<br>*(إصدار أولي) DDMRP لتحسين التخطيط‬* |
| التحكم بالإنتاج | [قم بإتاحة البضائع النهائية فعليًا قبل ترحيلها إلى دفاتر اليومية](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-finished-goods-physically-before-posting) | [قم بإتاحة البضائع النهائية فعليًا قبل ترحيلها إلى دفاتر اليومية](../production-control/deferred-posting.md) | إدارة الميزات:<br>*(إصدار أولي) جعل البضائع الجاهزة متوفرة فعليًا قبل الترحيل إلى دفاتر اليومية* |
| Warehouse management | [البحث عن البيانات ذات الصلة داخل warehouse mobile app](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/look-up-relevant-data-within-warehouse-mobile-app) | [الاستعلام عن البيانات باستخدام تحويلات تطبيقات الأجهزة المحمولة "إدارة المستودعات"](../warehousing/warehouse-app-data-inquiry.md) | إدارة الميزات:<br>*تدفق الاستعلام عن بيانات تطبيق Warehouse management* |

## <a name="feature-enhancements-included-in-this-release"></a>تحسينات الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي تحسينات الميزات المضمنة في هذا الإصدار. وتوفر كل واحدة منها تحسين تزايدي لميزة موجودة. ونظرًا لأنها تكون تحسينات فقط، فلن يتم سردها في [خطة الإصدار](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). ومع ذلك، لضمان عدم تعارض هذه التحسينات مع التخصيصات أو التفضيلات الموجودة لديك، يتم إيقاف تشغيل كل منها بشكل افتراضي (ما لم يذكر خلاف ذلك).

إذا كنت ترغب في تشغيل أي من هذه الميزات أو إيقاف تشغيلها، فيجب عليك القيام بذلك في [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| الوحدة النمطية | اسم الميزة في إدارة الميزات | معلومات إضافية |
|---|---|---|
| إدارة التكلفة | تحسين حساب السعر المعلق للمنتج المشترك | تعمل هذه الميزة علي إصلاح تعارض قد يحدث أحيانا عند حساب أسعار المنتجات المساعدة باستخدام مؤشرات ترابط متعددة. يتسبب في ان يتاكد النظام من ان كل سعر منتج مساعد يتم حسابه مره واحده فقط. وعندئذ يتم استخدام نتيجة الحساب كادخال لكافة الحسابات الأخرى. في حاله وجود سعر معلق بالفعل ، يتم استخدام هذا السعر. |
| التخطيط الرئيسي | تجميع الحركات في تحسين التخطيط | يمكن ان تساعد هذه الميزة في تقليل عدد الأوامر المخططة التي يتم إنشاؤها لتقديم بند أمر توريد واحد عند استخدام تحسين التخطيط. عند تشغيل هذه الميزة ، سيقوم تحسين التخطيط بتجميع كافة العمليات المخزنية لبند أمر في متطلب واحد للكمية الكاملة. (يتطابق هذا السلوك مع سلوك مشغل التخطيط المضمن.) يتم تجميع التوريد والطلب بشكل منفصل. التالي ، تساعد هذه الميزة علي تقليل حجم صوت الحركة عند قيامك بتقسيم الحركات وعند استخدام الابعاد (مثل أرقام المجموعات أو الأرقام المسلسلة) التي لا تغطي الابعاد. |
| التدبير وتحديد الموارد | وضع المورد قيد الانتظار لأوامر الشراء | تتيح لك هذه الميزة وضع مورد قيد الانتظار لأوامر الشراء. ويقوم باضافه نوع الاحتفاظ بامر *شراء جديد* الذي يضع علامة علي المورد علي انه معلق لأوامر الشراء. لن تتمكن من إنشاء أوامر شراء جديده لموردين قيد الانتظار لأوامر الشراء ، ولكن سيظل بإمكانك الاستمرار في إيه فواتير مفتوحة أو مدفوعات للموردين. |
| المبيعات والتسويق | حساب المبلغ الصافي للبند عند الاستيراد | تتيح لك هذه الميزة التحكم في ما إذا كان يجب علي النظام أعاده حساب إجمالي البنود عند استيراد البيانات من خلال بنود *أمر التوريد أو* بنود *عرض* أسعار المبيعات *أو كيان بنود* أمر الإرجاع باستخدام النوع OData أو الكتابة المزدوجة. يكون له تأثير فقط عندما يكون لديك أيضًا سياسات تقييم اتفاقية تجارية مطبقة تقيد التغييرات على حقل **كمية الشبكة** لبنود أوامر المبيعات و / أو بنود عروض أسعار المبيعات و / أو بنود أوامر الإرجاع. يقوم باضافه اعداد يسمي **حساب صافي مبلغ** البند إلى صفحه الحسابات المدينة **> اعداد معلمات** حسابات ال>آت المدينة. عند تعيين هذا الاعداد علي *"نعم*" ، يقوم النظام دائما باعاده حساب مبالغ البنود عند الحاجة (التالي تجاهل اي سياسة تقييم اتفاقيه تجاريه للبند بالنسبة للمبلغ الصافي). عند تعيين الاعداد علي *"لا* " ، لن يقوم النظام أبدا تلقائيا بحساب المبلغ الصافي للبند ، حتى وان كانت التغييرات الواردة في سعر البند والكمية و/أو الخصم تتضمن انه يجب أعاده حساب المبلغ الصافي للبند. يتم تمكين هذه الميزة افتراضيا وتقوم مبدئيا بتعيين **المبلغ** الصافي للبند إلى *"نعم"*. لا *يتطابق الاعداد* مع سلوك النظام السابق للإصدار 10.0.23 ويتم توفيره بشكل أساسي لدعم سيناريوهات التكامل القديمة<br><br>لمزيد من المعلومات، راجع [إعادة حساب صافي مبالغ البند عند استيراد أوامر المبيعات وعروض الأسعار والمرتجعات](../sales-marketing/calc-line-net-amounts-import.md). |
| المبيعات والتسويق | حساب إجماليات المبيعات باستخدام سلاسل متعددة | تساعد هذه الميزة علي تحسين الأداء من خلال تمكين النظام لاستخدام المعالجة المتوازية عند حساب إجماليات المبيعات في المجموعة. تضيف الميزة عددا جديدا **من حقول مؤشرات الترابط** إلى **مربع الحوار حساب إجمالي** المبيعات. إذا اخترت تشغيل العملية الحسابية في مجموعه ، فيمكنك استخدام هذا الحقل لتعيين الحد الأقصى لعدد مؤشرات الترابط. إذا قمت بتعيين القيمة إلى *0* (صفر) أو *سيتم* ، استخدام مؤشر ترابط واحد. تتيح القيم الموجودة اعلي 1 تعدد القيمات. |
| المبيعات والتسويق | تحديث الأسعار والخصومات التي تم إدخالها يدويًا للشركات الشقيقة | تضيف هذه الميزة الدعم لنهج التغيير اليدوي للأوامر بين الشركات الشقيقة. ويتضمن ذلك دعما لتحويل نهج التغيير اليدوي بين أوامر التوريد والشراء بين الشركات الشقيقة. كانت نهج التغيير اليدوية معتمده مسبقا للأوامر غير بين الشركات الشقيقة. عند تمكين هذه الميزة ، سيقوم النظام بمنحك خيار تحديث الأسعار والخصومات بعد حفظ التغييرات إلى أمر بين الشركات الشقيقة. يتيح لك هذا الخيار اختيار ما إذا كنت ترغب في تطبيق تفاصيل الأسعار والخصومات الجديدة علي الأمر بين الشركات الشقيقة أو ترك الطلب بدون تغيير. |

## <a name="new-and-updated-documentation-resources"></a>موارد وثائق جديده ومحدثه

لقد قمنا مؤخرا بإضافة مقالات التعليمات التالية أو تحديثها بشكل ملحوظ. ليس بالضرورة أن تكون هذه المقالات مرتبطة بالميزات الجديدة التي تمت إضافتها لهذا الإصدار، كما هو موضح في الأقسام السابقة. ومع ذلك، قد تساعدك في الحصول على مزيد من الميزات الموجودة.

| منطقة الميزة | المقالات الجديدة أو المحدثة |
|---|---|
| التخطيط الرئيسي، CTP | [حساب تواريخ تسليم أوامر المبيعات باستخدام CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) |
| التخطيط الرئيسي ، DDMRP | [نظرة عامة على تخطيط متطلبات المواد المدفوعة بالطلب](../master-planning/planning-optimization/ddmrp-overview.md)<br>[تشغيل ميزة DDMRP هذه في نظامك](../master-planning/planning-optimization/ddmrp-enable.md)<br>[وضع المخزون](../master-planning/planning-optimization/ddmrp-inventory-positioning.md)<br>[ملف تعريف Buffer والمستويات](../master-planning/planning-optimization/ddmrp-buffer-profile-and-levels.md)<br>[التخطيط المدفوع بالطلب](../master-planning/planning-optimization/ddmrp-planning.md)<br>[التنفيذ المرئي والتعاوني](../master-planning/planning-optimization/ddmrp-visual-and-collaborative-execution.md) |
| Warehouse management | [حزم الحاويات للشحن](../warehousing/packing-containers.md)<br>[اعمال التعبئة لحزم الحاويات الخارجية ومعالجه شحنات](../warehousing/packing-work.md) |

## <a name="feature-state-changes-in-this-release"></a>التغييرات في حالة الميزات في هذا الإصدار

يسرد الجدول التالي الميزات التي أصبحت إلزامية أو قيد التشغيل افتراضيًا في الإصدار 10.0.29. سيتم تشغيل كل هذه الميزات تلقائيًا لنظامك بمجرد التحديث إلى 10.0.29. لا يمكن إيقاف تشغيل الميزات الإلزامية، ولكن يمكن إيقاف تشغيل الميزات قيد التشغيل بشكل افتراضي باستخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

يسرد الجدول أيضًا الميزات التي كانت موجودة سابقًا في المعاينة العامة ولكنها تغيرت لتصبح متاحة بشكل عام في الإصدار 10.0.29. يشير هذا التغيير إلى ان الميزات مستحسنه الآن للاستخدام في بيئات الإنتاج. يتم إيقاف تشغيل هذه الميزات افتراضيًا ما لم يُذكر خلاف ذلك. لذلك ، يجب عليك استخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) لتمكينها إذا كنت تريد استخدامها.

| الوحدة النمطية | اسم الميزة | حالة الميزة الجديدة |
| --- | --- | --- |
| إدارة الأصول | [وظيفة إدارة الأصول لواجهة التنفيذ في طابق الإنتاج](../production-control/production-floor-execution-configure.md) | إلزامي |
| إدارة التكلفة | [تغيير تسمية الإلغاء في الإغلاق والتسوية إلى "عكس"](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse) | إلزامي |
| إدارة التكلفة | تنظيف تفاصيل حساب قائمة مكونات الصنف‬ عبر إصدارات التكاليف. | إلزامي |
| إدارة التكلفة | [مخزن مقارنة أسعار الأصناف](../cost-management/compare-item-price.md) | إلزامي |
| إدارة التكلفة | [مستوى حساب التكلفة](../cost-management/cost-calculation-level.md) | قيد التشغيل بشكل افتراضي |
| إدارة التكلفة | تمكين إعداد رقم الدُفعة المعرف من قِبَل المستخدم لعكس إقفال المخزون | قيد التشغيل بشكل افتراضي |
| إدارة التكلفة | [تفاصيل تقدم إقفال المخزون](whats-new-scm-10-0-21.md) | قيد التشغيل بشكل افتراضي |
| إدارة التكلفة | [‏‫مساحة تخزين تقارير قيمة المخزون](../cost-management/inventory-value-report-storage.md) | إلزامي |
| إدارة التكلفة | تنظيف بيانات تقرير قيمة المخزون | إلزامي |
| إدارة التكلفة | المتوسط المتحرك، تسلسل التكلفة الاحتياطي‬ | إلزامي |
| إدارة التكلفة | إظهار سجل إقفال المخزون في الشبكة | إلزامي |
| إدارة التكلفة | إظهار الأصناف التي تحتوي على أصناف لم تتم تسويتها بالكامل في تنسيق ملخص | إلزامي |
| إدارة المخزون والمستودعات | السماح بقيم مواصفات التشغيلة الفارغة | إلزامي |
| إدارة المخزون والمستودعات | أرقام بنود الزيادة التلقائية لبنود أمر تحويل المخزون | إلزامي |
| إدارة المخزون والمستودعات | إنشاء أمر تحويل من بند المبيعات | إلزامي |
| إدارة المخزون والمستودعات | تعطيل حقل سطر دفتر يومية المخزون في سير العمل | إلزامي |
| إدارة المخزون والمستودعات | تمكين ميزة التحذير لمعلمات إدارة جودة المخزون | إلزامي |
| إدارة المخزون والمستودعات | (الصين) استبعاد تكاليف الإصدار والاستلام الفعلي من متوسط التكلفة الشهرية | قيد التشغيل بشكل افتراضي |
| إدارة المخزون والمستودعات | [سير عمل الموافقة على دفتر يومية المخزون](../inventory/inventory-journal-workflow.md) | إلزامي |
| إدارة المخزون والمستودعات | [تخزين تقارير المخزون الفعلي](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/inventory-on-hand-report-storage) | إلزامي |
| إدارة المخزون والمستودعات | [طرق العرض المحفوظة لإدارة المخزون](saved-views-scm.md) | إلزامي |
| إدارة المخزون والمستودعات | إلغاء أمر التحويل | إلزامي |
| إدارة المخزون والمستودعات | استخدام وحدة القياس وكمية الوحدة في دفاتر يومية المخزون | إلزامي |
| إدارة المخزون والمستودعات | فتح مجلة المخزون | إلزامي |
| التصنيع | [انتقاء تلقائي للمواد الممكّنة للمستودع لقوائم الانتقاء المرحّلة بشكل تلقائي](whats-new-scm-10-0-23.md) | متوفرة بشكل عام |
| التصنيع | تمكين عرض أبعاد المخزون في قائمة المواد لعمليات مسار الإنتاج | إلزامي |
| التصنيع | [يمكنك تمكين إدخال أرقام الدُفعات والأرقام التسلسلية أثناء الإبلاغ عنها كمنتهية من "جهاز بطاقة الوظيفة".](../production-control/report-finished-job-device.md) | قيد التشغيل بشكل افتراضي |
| التصنيع | انتقاء كمية وزن تعبئة الإنتاج المحسنة | قيد التشغيل بشكل افتراضي |
| التصنيع | [بحث عن وظيفة لواجهة تنفيذ صالة الإنتاج‬](../production-control/production-floor-execution-configure.md) | إلزامي |
| التصنيع | [تكامل نظام تنفيذ التصنيع](../production-control/mes-integration.md) | قيد التشغيل بشكل افتراضي |
| التصنيع | [عرض "يومي" لواجهة تنفيذ أرضية الإنتاج](../production-control/production-floor-execution-configure.md) | قيد التشغيل بشكل افتراضي |
| التصنيع | [فحص توفر المادة حسب الطلب لأوامر الإنتاج](whats-new-scm-10-0-24.md) | قيد التشغيل بشكل افتراضي |
| التصنيع | [تجاوز حجز الإنتاج الافتراضي](../production-control/override-default-reservation-principle.md) | إلزامي |
| التصنيع | [تسجيل استهلاك المواد في واجهة تنفيذ أرضية الإنتاج (خلاف WMS)](../production-control/production-floor-execution-configure.md) | متوفرة بشكل عام |
| التصنيع | [تقرير عن أصناف وزن التعبئة من واجهة تنفيذ أرضية الإنتاج](../production-control/production-floor-execution-configure.md) | متوفرة بشكل عام |
| التصنيع | [الإبلاغ عن المنتجات المساعدة والثانوية من واجهة تنفيذ صالة الإنتاج‬](../production-control/production-floor-execution-configure.md) | قيد التشغيل بشكل افتراضي |
| التصنيع | [تقرير عن عناصر التخطيط في واجهة تنفيذ أرضية الإنتاج](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | قيد التشغيل بشكل افتراضي |
| التصنيع | [طرق العرض المحفوظة لتحكم الإنتاج](saved-views-scm.md) | إلزامي |
| التصنيع | [إظهار لوحة ترخيص المستخدم، والرقم التسلسلي، ورقم الدُفعة بالكامل في واجهة تنفيذ طابق الإنتاج‬](../production-control/production-floor-execution-configure.md) | إلزامي |
| التصنيع | [التحقق من انتهاء صلاحيه المواد الخام مقابل تاريخ الاستهلاك المخطط](whats-new-scm-10-0-23.md) | قيد التشغيل بشكل افتراضي |
| التخطيط الرئيسي | [التأكيد التلقائي لتحسين التخطيط](../master-planning/planning-optimization/planned-order-firming.md) | إلزامي |
| التخطيط الرئيسي | [تأكيد الأوامر المجمعة وأوامر التعبئة المخططة ودمجها بطريقة دُفعية.](whats-new-scm-10-0-20.md) | قيد التشغيل بشكل افتراضي |
| التخطيط الرئيسي | [تضمين الأصناف بالكمية المتاحة عند تمكين عوامل تصفية المعالجة المسبقة](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/master-planning-include-items-on-hand-when-pre-processing-filters-are-enabled) | قيد التشغيل بشكل افتراضي |
| التخطيط الرئيسي | [جدولة سعة غير محدودة لتحسين التخطيط](../master-planning/planning-optimization/infinite-capacity-planning.md) | قيد التشغيل بشكل افتراضي |
| التخطيط الرئيسي | [هوامش تحسين التخطيط](../master-planning/planning-optimization/safety-margins.md) | إلزامي |
| التخطيط الرئيسي | [الأيام السالبة لتحسين التخطيط](../master-planning/planning-optimization/delay-tolerance.md) | إلزامي |
| التخطيط الرئيسي | [التخويل المتوازي للتنبؤ بالطلب المعدّل](whats-new-scm-10-0-20.md) | إلزامي |
| التخطيط الرئيسي | [تأكيد الأوامر المخططة بواسطة التصفية](../master-planning/planning-optimization/planned-order-firming.md) | إلزامي |
| التخطيط الرئيسي | [أوامر الإنتاج المخططة لتحسين التخطيط](../master-planning/planning-optimization/production-planning.md) | إلزامي |
| التخطيط الرئيسي | [الاتفاقيات التجارية للشراء لتحسين التخطيط](../master-planning/planning-optimization/purchase-trade-agreement.md) | إلزامي |
| التخطيط الرئيسي | [طرق العرض المحفوظة للأوامر المخططة](saved-views-scm.md) | إلزامي |
| التدبير وتحديد الموارد | مبالغ التكاليف من وإلي في أوامر الشراء | إلزامي |
| التدبير وتحديد الموارد | تعطيل زر إعادة تعيين توزيع طلب الشراء | قيد التشغيل بشكل افتراضي |
| التدبير وتحديد الموارد | [تمكين إعادة تعيين عمليات سير العمل ذات الصلة بالتدبير](whats-new-scm-10-0-20.md) | قيد التشغيل بشكل افتراضي |
| التدبير وتحديد الموارد | [تحديد عدد بنود أمر الشراء لكل مهمة دُفعية](whats-new-scm-10-0-27.md) | قيد التشغيل بشكل افتراضي |
| التدبير وتحديد الموارد | [دمج الأبعاد المالية من المورد مع البعد المالي لرابط البُعد النشط في أمر الشراء](whats-new-scm-10-0-25.md) | إلزامي |
| التدبير وتحديد الموارد | [ترحيل الكميات المسجلة من المنتجات المخزنة وبقية المنتجات غير المخزنة للإيصالات وفواتير المورد](whats-new-scm-10-0-26.md) | متوفرة بشكل عام |
| التدبير وتحديد الموارد | [منع الاستهلاك الزائد لعمليات حجز الموازنة العامة عند وجود طلبات شراء متعددة في سير العمل](whats-new-scm-10-0-21.md) | قيد التشغيل بشكل افتراضي |
| التدبير وتحديد الموارد | [الطرف المسؤول عن اتفاقية الشراء](../procurement/purchase-agreements.md) | إلزامي |
| التدبير وتحديد الموارد | [طرق العرض المحفوظة لأوامر الشراء](saved-views-scm.md) | إلزامي |
| إدارة معلومات المنتج | معالجة مسبقة لتقرير قائمة مكونات الصنف لتجنب انقضاء المهلة | إلزامي |
| إدارة معلومات المنتج | الأبعاد المالية الافتراضية بشكل منفصل عند استخدام قوالب الأصناف | إلزامي |
| إدارة معلومات المنتج | تمكين مجموعات أبعاد المنتج لقوالب الأصناف المشتركة | إلزامي |
| إدارة معلومات المنتج | الصنف - تحسينات في كيان الكود الشريطي | إلزامي |
| إدارة معلومات المنتج | إعادة إنشاء أسماء متغيرات المنتجات استنادًا إلى المصطلحات | إلزامي |
| إدارة معلومات المنتج | [طرق العرض المحفوظة للمنتجات الصادرة](saved-views-scm.md) | إلزامي |
| إدارة معلومات المنتج | [تحسينات صفحة اقتراحات المتغيرات](../pim/tasks/create-predefined-product-variants.md) | إلزامي |
| المبيعات والتسويق | [توزيع التكاليف في أمر مبيعات](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/miscellaneous-charges-enhancements) | إلزامي |
| المبيعات والتسويق | تنظيف محفوظات تحديث أمر المبيعات | إلزامي |
| المبيعات والتسويق | [تنظيف محفوظات تحديث المبيعات بناءً على العمر](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) | إلزامي |
| المبيعات والتسويق | [تحسين تصدير كيان بيانات جهة الاتصال‬](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | إلزامي |
| المبيعات والتسويق | نسخ مجموعة الخصومات الإجمالية‬ لإشعار دائن المبيعات | إلزامي |
| المبيعات والتسويق | [تمكين البحث عن حقلي مقدمة وخاتمة مستند عرض أسعار المبيعات](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | إلزامي |
| المبيعات والتسويق | [تحسين أداء تقرير "أفضل 100" عميل](whats-new-scm-10-0-23.md) | إلزامي |
| المبيعات والتسويق | تضمين سجلات الانتظار في مهام تنظيف المحفوظات | إلزامي |
| المبيعات والتسويق | تحديد عدد بنود أمر المبيعات لكل مهمة دُفعية | قيد التشغيل بشكل افتراضي |
| المبيعات والتسويق | [تقييد عدد أوامر المبيعات التي يمكن تحديدها للترحيل](whats-new-scm-10-0-21.md) | إلزامي |
| المبيعات والتسويق | إعادة حساب رصيد العميل المقدر | إلزامي |
| المبيعات والتسويق | [تسجيل سطر أمر إرجاع المبيعات بالدقة العشرية مع وزن التعبئة وبدونه](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | إلزامي |
| المبيعات والتسويق | [طرق العرض المحفوظة للمبيعات والتسويق](saved-views-scm.md) | إلزامي |
| المبيعات والتسويق | [تأكيد أمر المبيعات بنقرة واحدة](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation) | إلزامي |
| إدارة النقل | السماح بعدم مطابقة كمبيالات الشحن‬ من بنود فواتير الشحن من دون دفتر يومية فاتورة مورّد مرحّلة | قيد التشغيل بشكل افتراضي |
| إدارة النقل | [تمكين إنشاء دفتر يومية فواتير المورّد عند تجاهل فاتورة الشحن](whats-new-scm-10-0-20.md) | قيد التشغيل بشكل افتراضي |
| إدارة النقل | [شحن طرد صغير](../warehousing/small-parcel-shipping.md) | إلزامي |
| إدارة النقل | [مستند شهادة المنشأ USMCA](../transportation/usmca-certification-of-origin.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | [مناطق مواقع إضافية](../warehousing/additional-location-zones.md) | إلزامي |
| Warehouse management | [إلغاء العمل](../warehousing/cancel-warehouse-work.md) | إلزامي |
| Warehouse management | [دمج الشحنة](../warehousing/configure-shipment-consolidation-policies.md) | إلزامي |
| Warehouse management | [إنشاء أوامر تحويل ومعالجتها من تطبيق المستودع](../warehousing/create-transfer-order-from-warehouse-app.md) | إلزامي |
| Warehouse management | قوالب توزيع البضائع مع توجيهات المواقع | قيد التشغيل بشكل افتراضي |
| Warehouse management | [فصل عمل التخزين عن إشعارات الشحن المسبق (ASN)](whats-new-scm-10-0-21.md) | إلزامي |
| Warehouse management | [عمليات الوضع المؤجلة](../warehousing/deferred-processing-manual-inventory-movement.md) | إلزامي |
| Warehouse management | الوضع المؤجل - الحاوية | قيد التشغيل بشكل افتراضي |
| Warehouse management | معالجة الوضع المؤجل - تمكين ميزة قالب التدقيق مع تعيين حدث التشغيل على القيمة "السابق" | إلزامي |
| Warehouse management | [تعطيل عمليات الاستلام المتوقعة من أوامر الجودة التي تقوم بأخذ عينة من المخزون المحظور](../inventory/inventory-blocking.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | تمكين التحقق السريع للأجهزة المحمولة للمستودع | إلزامي |
| Warehouse management | [المحلل المحسن لرموز GS1 الشريطية](../warehousing/gs1-barcodes.md) | متوفرة بشكل عام |
| Warehouse management | [الحجز المرن للوحة الترخيص المرتبط بالأمر](../warehousing/flexible-warehouse-level-dimension-reservation.md) | إلزامي |
| Warehouse management | [حجز بُعد مرن على مستوى المستودع](../warehousing/flexible-warehouse-level-dimension-reservation.md) | إلزامي |
| Warehouse management | [استخدام موقع دمج الأصناف](../warehousing/item-consolidation-location-utilization.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | سجل استلام لوحة الترخيص | قيد التشغيل بشكل افتراضي |
| Warehouse management | [دمج الشحنات يدويًا](../warehousing/consolidate-shipments-manual-workbench.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | [خدمة انتقاء بند التحويل يدويًا للمسؤول أو مستخدمين موثوقين مماثلين](whats-new-scm-10-0-28.md) | متوفرة بشكل عام |
| Warehouse management | [واجهة معدات معالجة المواد](../warehousing/mhax.md) | إلزامي |
| Warehouse management | [صفحات جدول عمل تخطيط الحِمل الجديدة](whats-new-scm-10-0-24.md) | متوفرة بشكل عام |
| Warehouse management | [مرئيات حمل العمل الصادر](../warehousing/outbound-workload-visualization.md) | إلزامي |
| Warehouse management | [توزيع البضائع المخطط](../warehousing/planned-cross-docking.md) | إلزامي |
| Warehouse management | [معالجة أحداث تطبيق المستودع](../warehousing/warehouse-app-events.md) | إلزامي |
| Warehouse management | تحسين الاستعلام لقالب عمل تخزين المنتج المساعد والمنتج الثانوي | إلزامي |
| Warehouse management | [تقريب الكميات لأسفل إلى أقرب وحدة مبيعات عند الإصدار إلى المستودع](whats-new-scm-10-0-19.md) | إلزامي |
| Warehouse management | [طريقة العرض المحفوظة لمنضدة عمل تخطيط الحمل](saved-views-scm.md) | إلزامي |
| Warehouse management | [طريقه العرض المحفوظة لصفحة تفاصيل العمل](saved-views-scm.md) | إلزامي |
| Warehouse management | [طريقة العرض المحفوظة لمعالجة الموجة](saved-views-scm.md) | إلزامي |
| Warehouse management | [طرق العرض المحفوظة لمعالجة الحمل](saved-views-scm.md) | إلزامي |
| Warehouse management | [طرق العرض المحفوظة لمعالجة الشحن](saved-views-scm.md) | إلزامي |
| Warehouse management | [مسح رموز GS1 الشريطية](../warehousing/gs1-barcodes.md) | متوفرة بشكل عام |
| Warehouse management | تفاصيل ملصق موجة الشحن | إلزامي |
| Warehouse management | [تقسيم الوحدات المختلطة](whats-new-scm-10-0-21.md) | إلزامي |
| Warehouse management | [استخدام واجهة برمجة تطبيقات أسرع لإقفال/إعادة فتح الحاويات في محطة التعبئة](whats-new-scm-10-0-21.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | [تحقق من صحة من القوالب المحددة لمهام التزويد](whats-new-scm-10-0-20.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | [الحقول المرقّاة‬ في تطبيق المستودع](../warehousing/warehouse-app-promoted-fields.md) | إلزامي |
| Warehouse management | [إرشادات خطوة تطبيق المستودع](../warehousing/mobile-app-titles-instructions.md) | إلزامي |
| Warehouse management | [حالة موقع المستودع](../warehousing/warehouse-location-status.md) | إلزامي |
| Warehouse management | [منعطفات تطبيق Warehouse Management](../warehousing/warehouse-app-detours.md) | قيد التشغيل بشكل افتراضي |
| Warehouse management | [تفاصيل وظيفة الدفعة للموجة](../warehousing/wave-processing.md) | إلزامي |
| Warehouse management | [إخطارات تنفيذ الموجة](../warehousing/wave-execution-notifications.md) | إلزامي |

## <a name="additional-resources"></a>الموارد الإضافية

### <a name="platform-updates-for-finance-and-operations-apps"></a>تحديثات النظام الأساسي لتطبيقات التمويل والعمليات

يتضمن الإصدار 10.0.29 من Microsoft Dynamics 365 Supply Chain Management تحديثات النظام الأساسي. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.29 من تطبيقات التمويل والعمليات (أكتوبر 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md).

### <a name="bug-fixes"></a>إصلاح الأخطاء

للحصول على معلومات حول إصلاحات الأخطاء المضمنة في كل تحديث من التحديثات التي تعد جزءًا من نسخة 10.0.29، قم بتسجيل الدخول إلى Lifecycle Services (LCS) وعرض [مقالة قاعدة المعارف](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 وسحابات الصناعة: خطة إصدار 1 لعام 2022

هل تتساءل عن الإمكانات القادمة والتي تم إصدارها حديثًا في أيٍّ من تطبيقات العمل أو النظام الأساسي الخاص بنا؟

راجع [Dynamics 365 وسحابات الصناعة: خطة إصدار 2 لعام 2022](/dynamics365-release-plan/2022wave2/). لقد التقطنا جميع التفاصيل بشكل شامل، ومن الأعلى إلى الأسفل، في مستند واحد يمكنك استخدامه للتخطيط.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>ميزات Supply Chain Management التي تمت ازالتها وإهمالها

يوضح المقال [الميزات التي تمت ازالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) الميزات التي تمت أو تتم جدولتها لإزالتها أو إهمالها لـ Supply Chain Management.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

قبل إزالة أي ميزة من المنتج، سيتم إعلان إشعار إهمال في المقال [الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 شهرًا قبل الإزالة.

بالنسبة للتغييرات الفاصلة التي تؤثر فقط على وقت التحويل البرمجي، ولكنها متوافقة ثنائيًا مع بيئة الاختبار المعزولة وبيئات الإنتاج، فسيكون وقت الإهلاك أقل من 12 شهرًا. بشكل عام، هذه هي التحديثات الوظيفية التي يجب إجراؤها للمحول البرمجي.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
