---
title: الأسئلة المتداول حول تكامل Dynamics 365 for Talent إلى Dynamics 365 for Finance and Operations
description: يوضح هذا الموضوع البيانات التي تتم مزامنتها في تكامل Talent وFinance and Operations.
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: cb9e01316f4b154a3e9a73042eaf0492f016c46c
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742685"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a>الأسئلة المتداول حول تكامل Dynamics 365 for Talent إلى Dynamics 365 for Finance and Operations

[!include [banner](includes/banner.md)]

يجيب هذا الموضوع عن الأسئلة الشائعة حول البيانات التي تتم مزامنتها عندما يتكامل Dynamics 365 for Talent مع Dynamics 365 for Finance and Operations.

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>هل تتم مزامنة جميع البيانات أو بعض كيانات البيانات فقط؟

مع Core Human Resources (HR)، تتم مزامنة مجموعة فرعية من البيانات. للحصول على قائمة بجميع الكيانات، راجع [التكامل من Dynamics 365 for Talent إلى Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md).

بالنسبة إلى Attract وOnboard، تعتبر كافة البيانات أصلية في Common Data Service.

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>هل يمكنني إنشاء تعيين جديد من دون استخدام القوالب؟

تعتبر القوالب نقطة بداية. يمكنك إنشاء قالبك الخاص، ولكنك تحتاج دائمًا إلى قالب عند إنشاء مشروع تكامل. للحصول على مزيد من المعلومات حول موحد البيانات (DI) والقوالب والمشاريع، راجع [دمج البيانات في Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a>هل يمكنني تعيين الأبعاد المالية للتحويل بين Talent وFinance and Operations؟

الأبعاد المالية غير موجودة حاليًا في Common Data Service ونتيجة لذلك لا تشكل جزءًا من القالب الافتراضي. تم التخطيط لهذا الكيان، ولكن لا يتوفر حاليًا أي مخطط زمني للإصدار.

بالنسبة إلى البيانات الموجودة في Finance and Operations ولكن غير الموجودة في Talent، يمكن ربط النظامين معًا باستخدام **تكوين الارتباطات** في Talent. للحصول على مزيد من المعلومات حول كيفية تكوين الارتباطات بين Talent وFinance and Operations، راجع [ما الجديد أو المتغير في Dynamics 365 for Talent Core HR (31 أكتوبر 2018)](whats-new-talent-october-31.md).

![تعيين الأبعاد المالية](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a>عندما أستورد موظفين، ينتقل هؤلاء في بعض الأحيان إلى عاملين غير نشطين في Finance and Operations. ما السبب؟

قد تتلقى رسالة الخطأ هذه إذا لم يكن لدى الموظفين أي سجل يتضمن تفاصيل التوظيف النشط في Talent. لحل هذه المشكلة، انتقل إلى **إدارة الموظفين \> الموظفون \> سجل التوظيف‬ \> مدير التاريخ**، وتأكد من وجود سجل يتضمن تفاصيل التوظيف النشط.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>إذا اخترت تعيين مجموعة فرعية فقط من الحقول، فهل ستؤدي التغييرات التي تم إدخالها على حقول غير معينة إلى تشغيل عملية مزامنة؟

تتبع مزامنة البيانات جدول التنفيذ. ستختار عملية التكامل سجلاً إذا تم تغيير أي حقل في السجل بصرف النظر عما إذا كان الحقل جزءًا من تعيين التكامل.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>كيف يمكنني إرسال تغييرات العاملين النشطاء فقط وليس سجلات العاملين المنتهية خدماتهم؟

باستخدام "الاستعلام المتقدم"، يمكنك تصفية البيانات المصدر وإعادة تشكيلها قبل تمريرها إلى الوجهة.

![الاستعلام المتقدم للعاملين النشطين](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a>هل يمكنني تحديد الحقول التي سيتم إرسالها إلى Finance and Operations لكيان معين؟

يمكنك إضافة حقول أو إزالتها من مهمة التكامل. لن يتم ملء كافة حقول البيانات الموجودة على كيان Common Data Service من Core HR.
يمكنك ملء بيانات إضافية عبر PowerApps.

![إضافة حقول إلى أو إزالتها من مهمة تكامل](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>بعد إعداد التكامل كوظيفة دفعية، فقد Talent الاتصال بالنظام الوجهة. كيف يمكنني إرسال مجموعة التغييرات نفسها إلى النظام الوجهة؟

لا حاجة إلى أي إعداد خاص لمعالجة الاستثناء. سيقوم موحد البيانات بشكل تلقائي بالتقاط الأخطاء التي تحدث في المصدر والوجهة وسيبلغ عنها وسيسمح بإعادة المحاولة يدويًا. ومع ذلك، فهو لا يسمح بتصحيح البيانات يدويًا. إن كان هناك حاجة إلى إجراء عمليات تحديث للبيانات، فيجب أن تحدث في المصدر أو الوجهة.

## <a name="can-i-set-up-bi-directional-integration"></a>هل يمكنني إعداد تكامل ثنائي الاتجاه؟

لا، التكامل أحادي الاتجاه في الوقت الحالي (Talent إلى Finance and Operations). ومع ذلك، يوجد قالب افتراضي لإرسال البيانات من Talent إلى Finance and Operations.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>هل يمكنني السماح بحذف السجلات كجزء من عملية التكامل؟

لا، لن يلتقط موحد البيانات السجلات المحذوفة لنقل البيانات. في الوقت الحالي، لم يتم تضمين سواء عمليات إنشاء وتحديث البيانات (UPSERT).

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>هل يمكن إعادة تشغيل التنفيذ الذي يتضمن أخطاء؟ إذا كان الأمر كذلك، فهل سيرسل ملفًا كاملاً أو التغييرات فقط؟

عملية التشغيل الأولى لموحد البيانات هي دائمًا عملية تشغيل كاملة. وتستند عمليات التشغيل التالية إلى تعقب التغييرات. يستخرج تشغيل الخطأ، عند تنفيذه، السجلات الموجودة في نطاق التشغيل ويرسل أحدث التغييرات من Common Data Service.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>عند حفظ المشروع، أتلقى رسالة الخطأ: "يتضمن المشروع أخطاء تعيين". ماذا أفعل؟

تحقق من إعداد مفاتيح التكامل، وأدخل أية تغييرات مطلوبة على الإعداد، ثم قم بتحديث الكيانات في المشروع.

عند استخدام القالب الافتراضي، سيتم استيراد مفاتيح التكامل بشكل تلقائي. قد تحدث هذه المشكلة عند إضافة مهام جديدة إلى القالب الموجود.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>إذا كان لديّ العدد N من الكيانات القانونية حتى توجد توظيفات للعاملين، هل أحتاج إلى إنشاء تعيين لكل واحد منهم؟

نعم، لكل كيان قانوني في Finance and Operations، ستحتاج إلى مشروع تكامل منفصل في تكامل البيانات.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>أحتاج إلى نقل البيانات التي لا تشكل جزءًا من القالب الافتراضي التي وفرته Microsoft. هل يمكنني القيام بذلك؟

نعم، يمكن إضافة حقول أو إزالتها من القالب الموجود. ويمكن تعديل القالب لتضمين بيانات إضافية من كيانات أخرى في Common Data Service. يجب أن يكون الكيان في Common Data Service لكي يتم تضمينه في القالب. 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>لقد انتهيت الآن من إنشاء بيئات Finance and Operations وTalent، وتلقيت رسالة الخطأ "قيمة البيانات انتهاك قيود التكامل." ما السبب؟

بإمكان أسباب هذا الخطأ أن تشتمل على:

- أدى نقل البيانات إلى استخراج سجلات مكررة في المصدر (Common Data Service).

- تتضمن عملية نقل البيانات قيمًا فارغة للحقول المطلوبة في Finance and Operations. تأكد من أن البيانات موجودة في Common Data Service وتستوفي شروط Finance and Operations.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>إذا ظهرت أخطاء تتعلق بالتنفيذ ولم تتم مزامنة معرّف الموظف، كيف يمكنني العثور على محفوظات الوظيفة التي تتضمن سجل الموظف الفاشل؟

سينشئ موحد البيانات عدة مشاريع في Finance and Operations. وتكون العلاقة بين مهمة موحد البيانات ومشروع Finance and Operations علاقة واحد بواحد.

تتبع الوقت اعتبارًا من سجل تنفيذ موحد البيانات وابحث عن مشروع الفهرس-1 في Finance and Operations. إذا كان رقم مهمة 9 في موحد البيانات"، فسيكون الفهرس 8 في Finance and Operations.

1. التقط فهرس المهمة من موحد البيانات (إنه "9" في هذا المثال).

![التقاط فهرس المهمة من موحد البيانات](media/CaptureTaskIndex.png)

2. تعقب وقت تنفيذ المشروع.

![تعقب وقت تنفيذ المشروع](media/CaptureTimeOfExecution.png)

3. في Finance and Operations، حدد الفهرس - 1. في هذا المثال، يتوافق المشروع مع اللاحقة "8" ووقت تنفيذ مشروع الفهرس "0" مع وقت التنفيذ في الخطوة 2.

![تعريف الفهرس](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a>بعد تمكين التكامل بين Talent وFinance and Operations، لا يمكنني رؤية بيانات Talent في Finance and Operations. ماذا أفعل؟

التكامل مع Finance and Operations عبارة عن عملية تتكون من خطوتين. أولاً، تحقق من تحديث بيانات Talent ومن توفرها في Common Data Service. هذا الأمر عبارة عن مزامنة قريبة من الوقت الحقيقي ويمكن التحقق منها في PowerApps عن طريق مراجعة البيانات في كيانات البيانات.

![البيانات الموجودة في Common Data Service](media/DataInCDS.png)

إذا لم تظهر البيانات كما هو متوقع في Common Data Service، فتأكد من دعم الكيان في التكامل. لتضمين بيانات إضافية في Common Data Service، ستتم مطالبة بإجراء تغيير من جانب Microsoft.

إذا كان الكيان مدعومًا والبيانات متوفرة في Common Data Service، فتأكد من صحة التعيين في موحد البيانات. إذا كان تعيين موحد البيانات مقبولاً، فتحقق عندئذِ من نجاح تشغيل مهام إدارة البيانات. قد تحدث بعض الأخطاء أثناء تنفيذ الوظائف الدفعية. لمزيد من المعلومات حول إدارة البيانات، راجع [إدارة البيانات](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a>عناوين الموظفين غير صحيحة بعد استيرادها إلى Finance and Operations. ماذا أفعل؟

يستخدم التسلسل الرقمي في **معرّف الموقع** النمط نفسه في كل من Talent وFinance and Operations. يجب أن يكون التسلسل الرقمي فريدًا على الجانبين لتفادي حدوث تضارب في العناوين عند تنفيذ تكامل البيانات من Common Data Service إلى Finance and Operations.

أثناء تنفيذ Talent، تأكد من أن التسلسلات الرقمية ليست نفسها في Talent قدرات وFinance and Operations. تأكد من أن كافة التسلسلات الرقمية ليست مماثلة حيث قد يتم الاحتفاظ بالبيانات في كلا النظامين.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>عند إنشاء مجموعة الاتصالات، لا يمكنني رؤية الاتصال في القائمة المنسدلة "اتصال". ماذا أفعل؟

عند إنشاء اتصالاتك، تأكد من اختيار Dynamics 365 for Finance and Operations (حاليًا في المعاينة) وCommon Data Service.

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>عند مزامنة عمليات التوظيف، أتلقى رسائل الخطأ "CompanyInfo_FK غير موجود" أو "القيمة '12/31/2154 11:59:59 ص" في الحقل "تاريخ انتهاء التوظيف" غير موجودة في الجدول ذي الصلة "التوظيف"." ماذا أفعل؟‬

تأكد من أنك تقوم بالتعيين إلى الكيانات القانونية الصحيحة. مزامنة الكيان القانوني ليست جزءًا من القالب الافتراضي، وبالتالي من المتوقع أن يكون كل كيان قانوني موجود في Talent وCommon Data Service موجود أيضًا في Finance and Operations.
تأكد أيضًا من أنك تحدد الكيانات القانونية الصحيحة لمجموعة الاتصالات المرتبطة.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a>بعد إعداد مشروعي، يبدو تعيين الحقول في Finance and Operations فارغًا. ماذا أفعل؟

يمكنك تحديث كيانات البيانات في Finance and Operations بالانتقال إلى **إدارة البيانات \> محددات إطار العمل‬ \> إعدادات الكيان‬ \> تحديث قائمة الكيانات.** قد يستغرق استكمال هذا الإجراء دقائق قليلة تتمكن بعدها من رؤية هذه التعيينات. تحدث هذه المشكلة عند إنشاء مشاريع جديدة.

![تعيين حقول مفقود](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>الموارد الإضافية

- موحد البيانات (DI): 

  - [دمج البيانات في Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [إدارة أخطاء موحد البيانات واستكشاف الأخطاء وإصلاحها](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [الاستجابة لطلبات DSR للسجلات التي أنشأها النظام في PowerApps وMicrosoft Flow وCommon Data Service](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- إدارة البيانات:

  - [إدارة البيانات](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
