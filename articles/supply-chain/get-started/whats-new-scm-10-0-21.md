---
title: إصدار أولي Dynamics 365 Supply Chain Management 10.0.21 (أكتوبر 2021)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في الإصدار 10.0.21 من Dynamics 365 Supply Chain Management.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 42d296cb0402b5e96f23d628f08a28fb35683d5f
ms.sourcegitcommit: 5a44eb4f555bf5ee0b1293f0ecdc37ee8b53aa24
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/17/2021
ms.locfileid: "7391198"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10021-october-2021"></a>إصدار أولي Dynamics 365 Supply Chain Management 10.0.21 (أكتوبر 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في معينة الإصدار 10.0.21 من Microsoft Dynamics 365 Supply Chain Management. رقم بنية هذا الإصدار هي 10.0.960، وهو يتوفر كما يلي

- **إصدار أولي الإصدار:** أغسطس 2021
- **التوفر العام للإصدار (تحديث ذاتي):** سبتمبر 2021
- **التوفر العام للإصدار (تحديث تلقائي):** أكتوبر 2020

## <a name="known-deployment-issue"></a>مشكلة النشر المعروفة

عند نشر الإصدار 10.0.21 على IaaS قد تتلقى تحذير النشر التالي:

**كود التحذير:** 95017

**رسالة تحذير:** فشل تنفيذ البرنامج النصي \[SetupDiagnostics\] مقابل الجهاز الظاهري

سيعمل النشر على الرغم من التحذير. ومع ذلك، قد تحدث المشكلات المعروفة التالية في Lifecycle Services (LCS):

- في صفحة **مراقبة البيئة**، لن يظهر ارتباط **عرض معلومات الإصدار التفصيلية**، لذا لن تتمكن من رؤية الإصدارات المحددة من الوحدات المثبتة في بيئتك. بدون هذه البيانات، قد تفشل الإصلاحات العاجلة اللاحقة لأن العملية التي تطبق الإصلاحات العاجلة يستخدم هذه البيانات للتحقق من أن يتم استيفاء المتطلبات الأساسية لإصدار الوحدة النمطية. لأنه من غير الممكن استخدام بناء PEAP/معاينة في الإنتاج أو تطبيق الإصلاحات العاجلة، يجب أن يكون التأثير الحد الأدنى.
- لن تعرض علامات التبويب **مقاييس الأداء** وخ **تحليل الفهرس** على صفحة **مراقبة البيئة** ضمن SQL Insights، لن تعرض أي بيانات. ستعمل كافة ميزات **مراقبة البيئة** الأخرى كما هو مقصود.
- لن تكون صفحة **تشخيصات النظام الكاملة** قابلة للوصول. لن تظهر البيانات المرتبطة بحالة تشغيل المجمع الليلي والمشكلات التي اكتشفتها قواعده أيضا.

## <a name="features-included-in-this-release"></a>الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي الميزات المضمنة في هذا الإصدار. يوفر عمود *الميزة* ارتباطات إلى [خطة الإصدار](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features)، حيث يمكنك الاطلاع على تواريخ الإصدار الرسمية لكل ميزة. يوفر عمود *مزيد من المعلومات* المزيد من التفاصيل و/أو الارتباطات عن المستندات ذات الصلة.

يجب تمكين معظم هذه الميزات باستخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) قبل التمكن من استخدامها. لا تزال بعض الميزات المدرجة في المعاينة، بينما قد يكون الآخرون متاحون بشكل عام.

| منطقة الميزة | الميزة | معلومات إضافية |
|---|---|---|
| المخزون&nbsp;و&nbsp;اللوجستيات | [تُعد محاسبة المخزون العالمي وظيفة إضافية لـ Dynamics 365 Supply Chain Management](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [الصفحة الرئيسية لمحاسبة المخزون العمومي](../global-inventory-accounting/global-inventory-accounting-home.md) |
| المخزون&nbsp;و&nbsp;اللوجستيات | [ترحيل التسويات الحالية باستخدام أكواد متصلة بحسابات المقابلة](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [أكواد أسباب جرد المخزون](../warehousing/reason-codes-for-counting-journals.md) |
| المخزون&nbsp;و&nbsp;اللوجستيات | [سياسة تصدير البيانات المرجعية لعرض أسعار المبيعات](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | اختر ما إذا كانت التغييرات التي تم إجراؤها على البيانات المشار إليها بواسطة عروض الأسعار ستتسبب في تضمين عروض الأسعار (أو السطور) في التصدير التزايدي التالي. سيتم تشغيل الصادرات المتزايدة بسرعة أكبر إذا اخترت عدم تضمين عروض الأسعار أو البنود.<br><br>تضيف هذه الميزة إعدادا يسمى **تخطي بيانات عرض أسعار المبيعات المشار إليها أثناء تعقب التغيير** إلى صفحة **معلمات الحسابات المدينة**. |
| المخزون&nbsp;و&nbsp;اللوجستيات | [مسح الرموز الشريطية في المستودع باستخدام معايير تنسيق GS1](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [الأكواد الشريطية GS1 ورموز الاستجابة السريعة (QR)](../warehousing/gs1-barcodes.md) |
| المخزون&nbsp;و&nbsp;اللوجستيات | [حجز سهل للوظيفة الإضافية لرؤية المخزون](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [حجوزات رؤية المخزون](../inventory/inventory-visibility-reservations.md) |
| المخزون&nbsp;و&nbsp;اللوجستيات | [تحسينات الخصم ووزن التعبئة لإدارة الخصومات](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [إدارة الخصومات باستخدام منضدة عمل الخصم](../rebate-management/deduction-workbench.md )<br><br>[معالجة الخصومات ومراجعتها وترحيلها](../rebate-management/process-review-post.md)<br><br>[صفقات إدارة الخصومات](../rebate-management/rebate-management-deals.md) |
| المخزون&nbsp;و&nbsp;اللوجستيات | [إرشادات خطوة تطبيق المستودع](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [تخصيص عناوين الخطوات وإرشاداتها لتطبيق Warehouse Management للأجهزة المحمولة](../warehousing/mobile-app-titles-instructions.md) |
| المخزون&nbsp;و&nbsp;اللوجستيات | [فواصل العمل وتحديثات التتبع للتكلفة المستلمة](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [تحديث التعقب لإبعاده](../landed-cost/update-tracking-putaway.md )<br><br>[معالجة البضاعة بالطريق](../landed-cost/in-transit-processing.md) |
| التخطيط الرئيسي | [الأيام السالبة لتحسين التخطيط](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [التسامح مع التأخير (الأيام السالبة)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>تحسينات الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي تحسينات الميزات المضمنة في هذا الإصدار. ويوفر كل منها تحسين تزايدي لميزة موجودة. ونظرًا لأنها تكون تحسينات فقط، فلن يتم سردها في [خطه الإصدار](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). ومع ذلك، لضمان عدم تعارض هذه التحسينات مع التخصيصات أو التفضيلات الموجودة لديك، يتم إيقاف تشغيل كل منها بشكل افتراضي (ما لم يذكر خلاف ذلك). إذا كنت ترغب في استخدام أي من هذه الميزات، يجب عليك تمكينها بشكل صريح في [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| منطقة الميزة | الميزة&nbsp;الاسم&nbsp;في إدارة&nbsp;الميزة | معلومات إضافية |
|---|---|---|
| إدارة التكلفة | تفاصيل تقدم إقفال المخزون | تتيح ميزة المعاينة هذه عرضا مفصلا لتقدم إغلاق المخزون. |
| التدبير وتحديد الموارد | منع الاستهلاك الزائد لعمليات حجز الموازنة العامة عند وجود طلبات شراء متعددة في سير العمل | تعمل ميزة المعاينة هذه على تحسين التحقق من الأخطاء عند إرسال المستخدمين طلبات الشراء والموافقة عليها التي تتجاوز الرصيد المتبقي من بند حجز الموازنة العامة. يساعد هذا في منع الإفراط في الحجوزات العامة للميزانية عند وجود طلبات شراء متعددة في سير العمل. |
| التحكم بالإنتاج | إظهار لوحة ترخيص المستخدم، والرقم التسلسلي، ورقم الدُفعة بالكامل في واجهة تنفيذ طابق الإنتاج‬ | توفر هذه الميزة تجربة محسنة لعرض قوائم أرقام لوحات تسلسلية ودفعية ومرخصة في واجهة تنفيذ طابق الإنتاج. تتغير الشاشة من طريقة عرض بطاقة بعدد محدود من الأحرف إلى طريقة عرض قائمة توفر مساحة كافية لإظهار القيم الكاملة. توفر القائمة أيضا القدرة على البحث عن أرقام محددة. |
| المبيعات والتسويق | تقييد عدد أوامر المبيعات التي يمكن تحديدها للترحيل | تتيح لك هذه الميزة تحديد الحد الأقصى لعدد أوامر التوريد التي يمكن تحديدها عند ترحيل التأكيدات وقوائم الانتقاء وإيصالات التعبئة والفواتير من صفحة قائمة أوامر التوريد. يتم تمكينه تلقائيا. تضيف الميزة إعدادا يسمى **الحد الأقصى لعدد أوامر التوريد للترحيل** إلى صفحة **معلمات الحسابات المدينة**. الإعداد الجديد الافتراضي إلى قيمة *100*. تساعد الميزة على تحسين أداء صفحة قائمة أوامر التوريد عند تحديد عدد كبير من أوامر التوريد. ليس له أي تأثير على عدد أوامر التوريد التي يمكن معالجتها بواسطة مهمة دورية. |
| إدارة المستودعات | فصل عمل التخزين عن إشعارات الشحن المسبق (ASN) | هذه الميزة مطلوبة لإرسال وتلقي إشعارات الشحن المسبق (ASNs) عند تشغيل حمل عمل إدارة مستودع على وحدة مقياس (كجزء من طبولوجيا مختلطة موزعة). ويضيف جدول قاعدة بيانات جديدة مخصصة لتخزين المعلومات حول العمل وضع. سابقا، تم تخزين هذه المعلومات في جداول تستخدم أيضا لـ ASNs. |
| إدارة المستودعات | تقسيم الوحدات المختلطة | يسمح للنظام بفتح العناصر في المواقع التي تتضمن وحدات مختلطة (مثل كلا المربعين والحالات). لكل سطر قالب تحديد فترات زمنية محددة، تتيح لك هذه الميزة اختيار ما إذا كان يجب أن يقوم البند بفتح العناصر في مواقع مختلطة أو أحادية الوحدة. |
| إدارة المستودعات | استخدام واجهة برمجة تطبيقات أسرع لإقفال/إعادة فتح الحاويات في محطة التعبئة | عند تمكين ميزة المعاينة هذه، يتم إنشاء حركات المخزون المتعلقة بالحاويات باستخدام عملية خفيفة الوزن جديدة تحسن أداء إغلاق أو إعادة فتح الحاويات أثناء المعالجة اليدوية لمحطة التعبئة. |

## <a name="new-and-updated-documentation-resources"></a>موارد وثائق جديده ومحدثه

لقد قمنا مؤخرا باضافه موضوعات التعليمات التالية أو تحديثها بشكل ملحوظ. ليس بالضرورة ان تكون مرتبطة بالميزات الجديدة المضافة لهذا الإصدار ، كما هو موضح في القسم السابق ، ولكن قد يساعدك ذلك علي الحصول علي مزيد من الميزات الموجودة.

| منطقة الميزة | الموضوعات الجديدة أو المحدثة |
|---|---|
| التخطيط الرئيسي | [التنبؤات بالمخزون](../master-planning/inventory-forecast.md) |
| التخطيط الرئيسي | [المعلمات غير المستخدمة في تحسين التخطيط](../master-planning/planning-optimization/not-used-parameters.md) |
| التخطيط الرئيسي | [أساليب التزويد وتعديل الكمية](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| التخطيط الرئيسي | [جدولة ذات سعة لا نهائية](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| التخطيط الرئيسي | [عرض سجلات التخطيط ومحفوظات الخطط](../master-planning/planning-optimization/plan-history-logs.md) |
| إدارة المستودعات | [استراتيجيات التعبئة في الحاويات](../warehousing/container-packing-strategy-overview.md) |
| إدارة المستودعات | [سيناريوهات مثال عن جرد دوري](../warehousing/cycle-counting-scenarios.md) |
| إدارة المستودعات | [استيراد إشعارات ASN الواردة عبر كيان البيانات V2](../warehousing/import-asn-v2-data-entity.md) |
| إدارة المستودعات | [الانتقاء المفرط لأوامر المبيعات وأوامر التحويل](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| إدارة المستودعات | [جدولة طباعة تسمية الموجة‬ أثناء الموجة‬](../warehousing/configure-task-based-wave-label-printing.md) |
| إدارة المستودعات | [ما الجديد أو الذي تم تغييره في تطبيق Warehouse Management للأجهزة المحمولة](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>الموارد الإضافية

### <a name="platform-updates-for-finance-and-operations-apps"></a>تحديث النظام الأساسي لتطبيقات Finance and Operations

يتضمن الإصدار 10.0.21 من Microsoft Dynamics 365 Supply Chain Management تحديثات النظام الأساسي. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.21 من تطبيقات Finance and Operations (أكتوبر 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

### <a name="bug-fixes"></a>إصلاح الأخطاء

للحصول على معلومات حول إصلاحات الأخطاء المضمنة في كل تحديث من التحديثات التي تعد جزءًا من 10.0.21، قم بتسجيل الدخول إلى Lifecycle Services (LCS) وعرض [مقالة قاعدة المعارف](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 وسحابات الصناعة: خطة إصدار 2 لعام 2021

هل تتساءل عن الإمكانات القادمة والتي تم إصدارها حديثًا في أيٍّ من تطبيقات العمل أو النظام الأساسي الخاص بنا؟

راجع [Dynamics 365 وسحابات الصناعة: خطة إصدار 2 لعام 2021](/dynamics365-release-plan/2021wave2/). لقد التقطنا جميع التفاصيل بشكل شامل، ومن الأعلى إلى الأسفل، في مستند واحد يمكنك استخدامه للتخطيط.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>ميزات Supply Chain Management التي تمت ازالتها وإهمالها

يوضح الموضوع [الميزات التي تمت ازالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) الميزات التي تمت أو تتم جدولتها لإزالتها أو إهمالها لـ Supply Chain Management.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

قبل إزالة أي ميزة من المنتج، سيتم إعلان إشعار إهمال في الموضوع [الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 شهرًا قبل الإزالة.

بالنسبة للتغييرات الفاصلة التي تؤثر فقط على وقت التحويل البرمجي، ولكنها متوافقة ثنائيًا مع بيئة الاختبار المعزولة وبيئات الإنتاج، فسيكون وقت الإهلاك أقل من 12 شهرًا. بشكل عام، هذه هي التحديثات الوظيفية التي يجب إجراؤها للمحول البرمجي.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
