---
title: الأسئلة الشائعة حول ترحيل عملاء الموارد البشرية
description: تجيب هذه المقالة على الأسئلة المتداولة حول ترحيل Microsoft Dynamics 365 Human Resources إلى البنية التحتية المدمجة للتمويل والعمليات.
author: twheeloc
ms.date: 07/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0e11d26ebe084762a8616c8aa0aa041a87306473
ms.sourcegitcommit: e25fe4228add88dd37f4f38ece86979e1c621f6a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/01/2022
ms.locfileid: "9734348"
---
# <a name="human-resources-customer-migration"></a>ترحيل عملاء الموارد البشرية

## <a name="how-should-dynamics-365-human-resources-customers-plan-to-move-to-the-finance-and-operations-infrastructure"></a>كيف يجب أن يخطط عملاء Dynamics 365 Human Resources للانتقال إلى البنية التحتية للتمويل والعمليات؟

ستتأثر فئتان من عملاء Microsoft Dynamics 365 Human Resources وسيتعين عليهم إجراء تغييرات للتأكد من أنهم يستخدمون أحدث بنية تحتية للتمويل والعمليات:

- العملاء الذين يستخدمون Dynamics 365 Human Resources وليس لديهم أي تطبيقات عمليات أخرى من Dynamics 365
- العملاء الذين يستخدمون كلاً من Dynamics 365 Human Resources وDynamics 365 Finance أو Dynamics 365 Supply Chain Management أو Dynamics 365 Commerce أو Dynamics 365 Project Operations

بغض النظر عن الفئة التي ينتمون إليها، سيتعين على العملاء نقل البيانات إلى بيئة تم إنشاؤها حديثًا على البنية التحتية للتمويل والعمليات والتحقق من اكتمال الدمج بنجاح.

من الآن فصاعدًا، سيكون لتطبيق Dynamics 365 Human Resources بيئة مالية وتشغيلية خاصة به منفصلة عن تطبيقات العمليات الأخرى. بهذه الطريقة، سيتمكن العملاء من الاستفادة من خيارات القابلية للتوسعة دون الحاجة إلى دمج بياناتهم الحالية. ستوفر Microsoft الأدوات وبيئة الحماية التي يمكن للعملاء استخدامها لاختبار ترحيل البيانات والتحقق من صحته قبل انتقالهم إلى بيئة الإنتاج. ستعمل الأدوات على تمكين عملية شبه آلية وستكون متاحة بين أغسطس ونوفمبر 2022.

العملاء الذين يستخدمون تطبيقات أخرى في البنية التحتية للتمويل والعمليات سيكون لديهم خيار دمج بيانات الموارد البشرية الخاصة بهم مع البيئة الحالية. 

## <a name="when-will-customers-be-moved-to-the-finance-and-operations-infrastructure"></a>متى سيتم نقل العملاء إلى البنية التحتية للتمويل والعمليات؟

سيعتمد انتقال كل شركة على التكوين الحالي لتلك الشركة واستعدادها للانتقال إلى البنية التحتية للتمويل والعمليات. نوصي بأن يعمل العملاء مع شريك Microsoft لتحديد أفضل مسار للمضي قدمًا.

- ستتمكن المؤسسات التي تستخدم وحدة **الموارد البشرية** في Dynamics 365 Finance من تمكين الإمكانات الجديدة من Dynamics 365 Human Resources كجزء من عملية تحديث One Version العادية. من المقرر أن تصبح الميزات الجديدة متاحة بشكل عام اعتبارًا من يناير 2022.
- ستتمتع المنظمات التي تستخدمها Dynamics 365 Human Resources بإمكانية الوصول إلى الأدوات التي يمكنها استخدامها لإكمال دمج البنية التحتية. ستعمل Microsoft مع العملاء في عملية النقل، للمساعدة في منع أي انقطاع في الخدمة. سيكون أمام العملاء 12 شهرًا لإجراء النقل، بدءًا من الوقت الذي تصبح فيه أدوات الترحيل متاحة.
- يمكن للمؤسسات التي تستخدم كلاً من Dynamics 365 Human Resources وحدة **الموارد البشرية** أن تنقل البنية التحتية للموارد البشرية القائمة بذاتها إلى البنية التحتية للتمويل والعمليات. خيار آخر هو استخدام أدوات الدمج لجلب البيئات في بيئة واحدة. لا توجد متطلبات أو إطار زمني لدمج البيئتين.

للحصول على معلومات محدثة، تحقق بانتظام من [خطط الإصدار](/dynamics365/release-plans/).

## <a name="will-customers-still-need-custom-integrations-between-dynamics-365-human-resources-and-the-human-resources-module"></a>هل سيظل العملاء بحاجة إلى عمليات تكامل مخصصة بين Dynamics 365 Human Resources ووحدة الموارد البشرية؟

- سيتعين على العملاء الذين لديهم بيئات Dynamics 365 Human Resources والبنية التحتية للتمويل والعمليات الأخرى المدمجة حاليًا الاستمرار في دمج البيئتين بعد الدمج.
- سيتعين على العملاء الذين يختارون إبقاء بيئة Dynamics 365 Human Resources الخاصة بهم منفصلة عن بيئة تطبيقات التمويل والعمليات الحالية لديهم الاستمرار في دمج البيئات لإتاحة البيانات في كلتا البيئتين.
- يمكن للعملاء الاستمرار في استخدام Data Integrator لنسخ البيانات بين البيئتين. لن يضطر العملاء الذين يدمجون البيانات في بيئة واحدة بعد الترحيل إلى دمج البيانات، لأن جميع البيانات ستكون في قاعدة بيانات واحدة.

## <a name="will-customer-isv-solutions-automatically-be-migrated"></a>هل سيتم ترحيل حلول ISV للعملاء تلقائيًا؟

تختلف تجربة الترحيل لكل مورد برامج مستقل (ISV) الحل، اعتمادا على أسلوب التكامل للحل. ستعمل Microsoft بشكل وثيق مع موردي البرامج المستقلين (ISVs) للمساعدة في توفير انتقال سلس إلى البنية التحتية للتمويل والعمليات. تم بناء العديد من حلول ISV على Dataverse باستخدام إمكانيات Microsoft Power Platform. تعتمد هذه الحلول على تكامل Dataverse بين بيئة Dynamics 365 Human Resources وبيئة Dataverse. يتم إهمال تكامل Dataverse كجزء من دمج البنية التحتية. في البنية التحتية للتمويل والعمليات، تم التخطيط لخرائط الكتابة المزدوجة الجديدة لتحل محل وظيفة تكامل Dataverse.

## <a name="how-will-the-data-integrator-that-moves-data-between-dynamics-365-human-resources-and-other-dynamics-365-apps-be-affected"></a>كيف سيتأثر تكامل البيانات الذي ينقل البيانات بين Dynamics 365 Human Resources وتطبيقات Dynamics 365 الأخرى؟

بعد انتقال العملاء إلى البنية التحتية للتمويل والعمليات، سيتعين عليهم الاستمرار في دمج البيانات بين البيئتين. يمكن للعملاء الاستمرار في استخدام Data Integrator لأداء مهام ترحيل البيانات هذه. سيتعين على العملاء الذين يخططون للإبقاء على بيئة Dynamics 365 Human Resources منفصلة عن بيئة تطبيقات التمويل والعمليات الحالية لديهم الاستمرار في دمج البيانات بين البيئتين. بالنسبة للعملاء الذين يدمجون البيئتين في بيئة واحدة، لن يكون التكامل بين البيئتين مطلوبًا بعد الآن.

## <a name="how-will-data-be-moved-between-dynamics-365-human-resources-on-the-finance-and-operations-infrastructure-and-dataverse-after-the-migration"></a>كيف سيتم نقل البيانات بين Dynamics 365 Human Resources على البنية التحتية للتمويل والعمليات وDataverse بعد الترحيل؟

يتم إهمال تكامل Dataverse الحالي بين Dynamics 365 Human Resources وDataverse كجزء من البنية التحتية للتمويل والعمليات. هناك خطط لإدخال خرائط مزدوجة الكتابة لتعيين كيانات التمويل والعمليات على جداول Dataverse. سيتعين على العملاء تحديد خرائط الكتابة المزدوجة المطلوبة لتنفيذها. نوصي باستخدام الجداول الافتراضية لعمليات التكامل وحلول ISV، ما لم تكن هناك حاجة عمل محددة لتكرار البيانات Dataverse لتشغيل منطق الأعمال.

## <a name="how-does-the-migration-affect-dataverse-extensions-for-dynamics-365-human-resources"></a>كيف يؤثر الترحيل على ملحقات Dataverse لـ Dynamics 365 Human Resources؟

سيُطلب من العملاء الانتقال إلى بيئة وضع الحماية قبل ترحيل بيئة التشغيل الخاصة بهم. عندما يقوم العملاء بترحيل بيئة وضع الحماية الخاصة بهم، سيتعين عليهم إنشاء نسخة من بيئة Dataverse للاتصال بالبيئة المالية والعمليات التي تم ترحيلها الجديدة. نوصي بأن يقوم العميل بنسخ كل من البيانات والحلول الخاصة بالبيئة، بحيث تتطابق مع بيئة التشغيل الحالية للعميل.

عندما يكون العملاء مستعدين لترحيل بيئة الإنتاج من Dynamics 365 Human Resources الخاصة بهم، ستقوم Microsoft تلقائيًا بترحيل قاعدة البيانات وتخزين كائن ثنائي كبير الحجم من Azure. ستوجه قاعدة البيانات والتخزين التي تم ترحيلها البيئة الجديدة على البنية التحتية للتمويل والعمليات إلى نفس بيئة إنتاج Dataverse. قبل أن تتمكن من الاستمرار في نسخ البيانات، سيتعين على عملاء Dataverse تمكين أي خرائط ثنائية الكتابة مطلوبة لعمليات التكامل والإضافات وحلول ISV المبنية على Dataverse.

## <a name="will-microsoft-power-platform-components-that-were-built-for-dynamics-365-human-resources-automatically-work-after-the-infrastructure-migration-is-completed"></a>هل ستعمل مكونات Microsoft Power Platform التي تم إنشاؤها لـ Dynamics 365 Human Resources للعمل تلقائيًا بعد اكتمال ترحيل البنية التحتية؟

التطبيقات التي تم إنشاؤها في Power Apps، والتدفقات التي تم إنشاؤها فيها Power Automate والتخصيصات الأخرى من Microsoft Power Platform مثل ملحقات Dataverse. أثناء ترحيل بيئات إنتاج العملاء، لا يوجد تأثير على بيئات Dataverse، بما في ذلك أي ملحقات. يجب أن تستمر التطبيقات والتدفقات وتخصيصات Power Microsoft Platform الأخرى في العمل دون الحاجة إلى تكوين إضافي.

## <a name="what-will-happen-to-dataverse-virtual-table-entities-for-dynamics-365-human-resources-during-the-migration"></a>ماذا سيحدث لكيانات جداول Dataverse الافتراضية لـ Dynamics 365 Human Resources أثناء الترحيل؟

عندما يقوم عملاء بترحيل بيئة Dynamics 365 Human Resources الخاصة بهم إلى البنية التحتية للتمويل والعمليات، ستظل بيئة Dataverse المتصلة بالبيئة المتصلة بـ Dynamics 365 Human Resources حاليًا. ستستمر جداول Dataverse الافتراضية التي تم إنشاؤها في البيئة في العمل دون الحاجة إلى أي تكوين إضافي. قد يلزم إعادة إنشاء الجداول الافتراضية في بيئة Dataverse المتصلة ببيئة العمليات والتمويل الحالية للعميل.

## <a name="how-will-an-integration-that-uses-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-work-after-the-infrastructure-merge-is-completed"></a>كيف سيعمل التكامل الذي يستخدم واجهة برمجة تطبيقات "نظام تعقب مقدم الطلب" (ATS) أو واجهة برمجة تطبيقات الرواتب أو جداول Dataverse الافتراضية لـ Dynamics 365 Human Resources أو الكيانات الأخرى في Dataverse Web API بعد اكتمال دمج البنية التحتية؟

عندما يقوم عملاء بترحيل بيئة Dynamics 365 Human Resources الخاصة بهم إلى البنية التحتية للتمويل والعمليات، ستظل بيئة Dataverse المتصلة بالبيئة المتصلة بـ Dynamics 365 Human Resources حاليًا. ستستمر أي عمليات تكامل تم تطويرها مقابل Dataverse Web API في العمل بعد اكتمال الترحيل.

## <a name="our-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-it-still-be-applied-after-the-infrastructure-migration-is-completed"></a>قامت مؤسستنا بتكوين أمان مخصص في Dynamics 365 Human Resources. هل سيستمر تطبيقه بعد اكتمال ترحيل البنية التحتية؟

نعم، سيتم تضمين تكوينات الأمان المخصصة في ترحيل البيانات.

## <a name="will-workflows-in-dynamics-365-human-resources-automatically-be-migrated"></a>هل سيتم ترحيل مهام سير العمل في Dynamics 365 Human Resources تلقائيًا؟

نعم، سيتم ترحيل تكوينات سير العمل ومحفوظات سير العمل ومهام سير العمل قيد المعالجة الحالية إلى البنية التحتية المدمجة.

## <a name="will-saved-views-in-dynamics-365-human-resources-automatically-be-migrated"></a>هل سيتم ترحيل المشاهدات الشخصية في Dynamics 365 Human Resources المحفوظة تلقائيًا؟

نعم، سيتم ترحيل الملفات الشخصية المحفوظة إلى البنية التحتية المدمجة.

## <a name="will-features-that-are-enabled-in-dynamics-365-human-resources-automatically-be-available-after-the-infrastructure-merge"></a>هل ستتوفر الميزات التي تم تمكينها في Dynamics 365 Human Resources تلقائيًا بعد دمج البنية التحتية؟

- بالنسبة للعملاء الذين يستخدمون وحدة **الموارد البشرية**، ستتم إدارة الميزات المتوفرة في Dynamics 365 Human Resources فقط من خلال إدارة الميزات. عادةً، لن يتم تمكين هذه الميزات افتراضيًا. سيتم توثيق أي ميزات يجب تمكينها افتراضيًا.
- بالنسبة للعملاء الذين يستخدمون Dynamics 365 Human Resources، ستتوفر الميزات في البنية التحتية. سيتم توثيق أي ميزات غير متوفرة. سيتم تمكين كل مفتاح إدارة ميزة يتم تمكينه في بيئة Dynamics 365 Human Resources الحالية في البنية التحتية المدمجة. لمزيد من المعلومات، راجع [‏‫نظرة عامة على إدارة الميزات](/fin-ops/get-started/feature-management-overview.md).

## <a name="what-happens-to-byod-databases-during-the-migration"></a>ماذا يحدث لقواعد بيانات BYOD أثناء الترحيل؟

سيتم ترحيل تكوينات الاستيراد والتصدير لجلب قاعدة البيانات الخاصة بك (BYOD) إلى البنية التحتية المالية والعمليات.

## <a name="is-there-an-impact-on-the-azure-region-when-the-customer-environment-is-migrated"></a>هل هناك تأثير على منطقة Azure عندما يتم ترحيل بيئة العميل؟

ستبقى بيئة Dynamics 365 Human Resources في نفس منطقة Azure من أجل الترحيل. إذا كان هناك متطلب لنقل بيئة إلى منطقة Azure مختلفة، فسيتعين على العملاء اتباع الخطوات القياسية للترحيل إلى منطقة جديدة بعد اكتمال الترحيل.

## <a name="what-happens-to-azure-data-lakes-during-the-migration"></a>ماذا يحدث لبحيرات بيانات Azure أثناء الترحيل؟

سيحتفظ أي تصدير تم تكوينه حاليًا لـ Azure Data Lake في تطبيقات التمويل والعمليات بنفس التكوين بعد الترحيل.

> [!NOTE]
> يجب تمكين خرائط الكتابة المزدوجة للاستمرار في كتابة البيانات من بيئة الموارد البشرية في Dataverse.

يمكن للعملاء الذين يرغبون في تصدير بيانات الموارد البشرية إلى مستودع البيانات تمكين هذه الميزة بعد اكتمال الترحيل إلى البنية التحتية للتمويل والعمليات. لمزيد من المعلومات، راجع [مستودعات البيانات - Azure Architecture Center](/azure/architecture/data-guide/scenarios/data-lake).

يمكن للعملاء ربط العديد من بيئات التمويل والعمليات بنفس مستودع البيانات. ومع ذلك، ستشير كل بيئة إلى مجلد وحاوية مختلفة. يجب على العملاء الذين يخططون لدمج البيئات لاحقًا التخطيط بعناية لنهجهم.
 
## <a name="what-migration-will-be-required-if-a-customer-is-currently-using-the-human-resources-module"></a>ما الترحيل المطلوب إذا كان العميل يستخدم حاليًا وحدة "الموارد البشرية"؟

سيحصل العملاء الذين يستخدمون وحدة **الموارد البشرية** على وظيفة الميزة الجديدة من Dynamics 365 Human Resources التي تم تطبيقها على بيئتهم من خلال عملية تحديث الإصدار الواحد القياسية. يمكن للعملاء توقع رؤية الوظيفة الجديدة في بيئتهم عندما تصبح متوفرة في كل تحديث. يمكن للعملاء استخدام إدارة الميزات لتمكين الميزات. يجب أن يخطط العملاء للتحقق من صحة هذه الميزات الجديدة باستخدام العمليات التي لديهم بالفعل واستخدامها للتحقق من صحة التحديثات الأخرى لبيئتهم.

## <a name="what-will-happen-to-custom-integrations-to-external-systems"></a>ماذا سيحدث لعمليات الدمج المخصصة للأنظمة الخارجية؟

سيتعين على العملاء ترحيل عمليات التكامل الخاصة بهم إلى بيئة التمويل والعمليات. نظرًا لاختلاف نقطة نهاية هذه البيئة، فقد يضطر العملاء إلى تحديث عمليات الدمج أو تغييرها بحيث يشيرون إلى البيئة الجديدة. ستكون هذه المهمة في الأساس عملية يدوية، وستعتمد التغييرات المطلوبة على بنية التكامل. يجب على العملاء العمل مع شركائهم في Microsoft لتحديد أفضل نهج لنقل عمليات التكامل.

## <a name="what-will-happen-to-microsoft-power-platform-dataverse-extensions-if-customers-merge-a-dynamics-365-human-resources-environment-with-an-existing-finance-and-operations-environment"></a>ماذا سيحدث لملحقات Microsoft Power Platform (Dataverse) إذا قام العملاء بدمج بيئة Dynamics 365 Human Resources مع بيئة مالية وعمليات حالية؟

إذا قرر العملاء دمج بيئة Dynamics 365 Human Resources وبيئة مالية وعمليات حالية في مثيل Dataverse واحد بعد الترحيل، فيجب دمج بيئات Dataverse الخاصة بهم كجزء من عملية الدمج. ستتطلب هذه المهمة إعادة نشر أي تطبيقات تم إنشاؤها باستخدام Power Apps، وأي تخصيصات أخرى، في البيئة الجديدة.

## <a name="what-will-happen-to-documents-during-the-migration"></a>ماذا سيحدث للوثائق أثناء الترحيل؟

عندما يقوم العملاء بترحيل بيئة Dynamics 365 Human Resources الخاصة بهم إلى البنية التحتية للتمويل والعمليات، ستبقى المستندات في مخزن المستندات الحالي وسيتم تعيينها تلقائيًا إلى البيئة الجديدة في البنية التحتية للتمويل والعمليات.

في إصدار مستقبلي، سيتم توفير كيانات بيانات جديدة. بعد إجراء هذا التغيير، سيتمكن العملاء الذين يختارون دمج بيئة Dynamics 365 Human Resources الخاصة بهم مع بيئة العمليات والتمويل الحالية من تصدير المستندات ونقلها إلى البيئة الحالية.

## <a name="after-the-migration-what-happens-to-the-batch-jobs-that-were-configured-in-dynamics-365-human-resources"></a>بعد الترحيل، ماذا يحدث للوظائف المجمعة التي تم تكوينها في Dynamics 365 Human Resources؟

سيتعين إعادة تكوين وظائف الدُفعات في بيئة التمويل والعمليات. سيتعين على العملاء تقييم كل وظيفة مجمعة ومقارنتها بالقائمة الحالية للوظائف المجمّعة في بيئة العمليات المالية. يجب على العملاء أيضًا تحليل جدول الدُفعات الكلي عند دمج مجموعتي وظائف الدُفعات لتحديد ما إذا كان ينبغي إجراء تغييرات على جدول الدُفعة أو الأولويات أو مجموعات الدُفعات.

## <a name="how-will-the-migration-affect-the-lcs-project-for-dynamics-365-human-resources"></a>كيف سيؤثر الترحيل على مشروع LCS لـ Dynamics 365 Human Resources؟

سيُطلب من العملاء إنشاء مشروع Microsoft Dynamics Lifecycle Service (LCS) جديد، وسيتعين عليهم تحديد تطبيقات التمويل والعمليات باعتبارها المنتج و **التنفيذ** كنوع المشروع. بالإضافة إلى ذلك، يتوفر حقل جديد لنوع المشروع الفرعي عند إنشاء مشروع LCS. سيتعين على العملاء تحديد خيار لترحيل Dynamics 365 Human Resources لترحيل مشروع LCS الحالي للموارد البشرية إلى البنية التحتية للتمويل والعمليات.

تختلف ميزات مشروعات LCS للتمويل والعمليات عن ميزات مشروعات LCS للموارد البشرية.

لبدء البث المباشر، سيتعين على العملاء الجدد إكمال المهام التالية:

- أكمل إلحاق المشروع.
- أكمل المنهجية.
- املأ مقدِّر الاشتراك.
- أكمل عملية الاستعداد لبدء البث المباشر.

## <a name="how-will-the-business-process-modeler-be-migrated"></a>كيف سيتم ترحيل مصمم إجراءات الأعمال؟

سيُطلب من العملاء تصدير مكتبة مصمم نماذج عمليات الأعمال الخاصة بهم من مشروع LCS للموارد البشرية واستيرادها إلى مشروع LCS للتمويل والعمليات. بالإضافة إلى ذلك، سيتعين على العملاء تحديث إعدادات التعليمات في التطبيق بحيث يشيرون إلى مشروع LCS الجديد.

## <a name="how-will-the-service-update-process-be-affected-by-the-migration"></a>كيف ستتأثر عملية تحديث الخدمة بالترحيل؟

بعد الترحيل، سيتمتع العملاء بقدر أكبر من المرونة لـ "إدارة دورة حياة التطبيق" (ALM) وتحديثات الخدمة. لن يتم تطبيق تحديثات الخدمة تلقائيًا على بيئات الموارد البشرية بعد الآن. بدلاً من ذلك، ستتبع الخدمة عمليات ووظائف تحديث خدمة الإصدار الواحد، وسيتم تمكين خيارات التكوين للتحديثات من خلال LCS.

## <a name="will-customers-be-eligible-for-fasttrack-assistance-with-the-infrastructure-merge"></a>هل سيكون العملاء مؤهلين للحصول على مساعدة FastTrack في دمج البنية التحتية؟

لا تزال Microsoft تحدد الأدوات والموارد التي ستتوفر من FastTrack للمساعدة في الدمج.

## <a name="licensing-impact"></a>تأثير الترخيص

لمزيد من المعلومات حول كيفية تأثر الترخيص، راجع [دمج البنية الأساسية لـ Dynamics 365 Human Resources](hr-infrastructure-merge.md#licensing).
