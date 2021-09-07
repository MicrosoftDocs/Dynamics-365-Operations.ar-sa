---
title: ‏‫الأسئلة المتداولة حول التكامل مع Finance
description: يوضح هذا الموضوع البيانات التي تتم مزامنتها في تكامل Human Resources وFinance.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8c368f916a199c7472f6f886d143048487a38ecc
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413353"
---
# <a name="integration-with-finance-faq"></a>‏‫الأسئلة المتداولة حول التكامل مع Finance

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يجيب هذا الموضوع عن الأسئلة الشائعة حول البيانات التي تتم مزامنتها عندما يتكامل Dynamics 365 Human Resources مع Dynamics 365 Finance.

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a>هل يمكنني تحرير مستخدم تطبيق Dynamics 365 Talent في Power Apps؟

الرقم إذا قمت بتحرير مستخدم تطبيق Human Resources، فقد يفشل التكامل بين Human Resources وDataverse. يوضح الجدول التالي الإعدادات الافتراضية لمستخدم تطبيق Talent.

| الاسم الكامل | مُعرِّف التطبيق | معرف كائن Azure AD | عنوان URI لمُعرِّف التطبيق |
| --- | --- | --- | --- |
| Dynamics 365 for Talent | f9be0c49-aa22-4ec6-911a-c5da515226ff | 27fd8129-4b3c-43f7-b1bf-47495d3a049b | f9be0c49-aa22-4ec6-911a-c5da515226ff |

![الإعدادات الافتراضية لمستخدم تطبيق Talent.](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>هل تتم مزامنة جميع البيانات أو بعض كيانات البيانات فقط؟

تتم مزامنة مجموعة فرعية من البيانات. للحصول على قائمة بجميع الكيانات، راجع [التكامل مع Dynamics 365 Finance](hr-admin-integration-finance.md).

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a>لماذا لا أرى أية بيانات متزامنة مع Dataverse؟

افتراضيًا، يكون تكامل خدمة Dataverse متوقف في البيئات الجديدة التي لا تتضمن بيانات العرض التوضيحي المتوفرة. بشكل افتراضي، يتم تشغيله في بيئات جديده تتضمن البيانات التجريبية، وتبدأ مزامنة البيانات عند توفير البيئة. بعد تجهيز البيئة الخاصة بك لمزامنة البيانات، يمكنك تشغيل التكامل. وللحصول على المزيد من المعلومات، راجع قسم [تكوين تكامل Dataverse](hr-admin-integration-common-data-service.md)

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>هل يمكنني إنشاء تعيين جديد من دون استخدام القوالب؟

تعتبر القوالب نقطة بداية. يمكنك إنشاء قالبك الخاص، ولكنك تحتاج دائمًا إلى قالب عند إنشاء مشروع تكامل. للحصول على مزيد من المعلومات حول موحد البيانات (DI) والقوالب والمشاريع، راجع [دمج البيانات في Microsoft Dataverse](/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a>هل يمكنني تعيين الأبعاد المالية للتحويل بين Human Resources وFinance؟

الأبعاد المالية غير موجودة حاليًا في Dataverse ونتيجة لذلك لا تشكل جزءًا من القالب الافتراضي. تم التخطيط لهذا الكيان، ولكن لا يتوفر حاليًا أي مخطط زمني للإصدار.

بالنسبة إلى البيانات الموجودة في Finance and Operations ولكن غير الموجودة في Human Resources، يمكن ربط النظامين معًا باستخدام **تكوين الارتباطات** في Human Resources.

![تعيين الأبعاد المالية.](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a>عندما أستورد موظفين، ينتقل هؤلاء في بعض الأحيان إلى عاملين غير نشطين في Finance. ما السبب؟

قد تتلقى رسالة الخطأ هذه إذا لم يكن لدى الموظفين سجل تفاصيل التوظيف نشط في Human Resources. لحل هذه المشكلة، انتقل إلى **إدارة الموظفين \> الموظفون \> سجل التوظيف‬ \> مدير التاريخ**، وتأكد من وجود سجل يتضمن تفاصيل التوظيف النشط.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>إذا اخترت تعيين مجموعة فرعية فقط من الحقول، فهل ستؤدي التغييرات التي تم إدخالها على حقول غير معينة إلى تشغيل عملية مزامنة؟

تتبع مزامنة البيانات جدول التنفيذ. ستختار عملية التكامل سجلاً إذا تم تغيير أي حقل في السجل بصرف النظر عما إذا كان الحقل جزءًا من تعيين التكامل.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>كيف يمكنني إرسال تغييرات العاملين النشطاء فقط وليس سجلات العاملين المنتهية خدماتهم؟

باستخدام "الاستعلام المتقدم"، يمكنك تصفية البيانات المصدر وإعادة تشكيلها قبل تمريرها إلى الوجهة.

![الاستعلام المتقدم للعاملين النشطين.](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a>هل يمكنني تحديد الحقول التي سيتم إرسالها إلى Finance لكيان معين؟

يمكنك إضافة حقول أو إزالتها من مهمة التكامل. لن يتم ملء كافة حقول البيانات الموجودة على جدول Dataverse من Human Resources.
يمكنك ملء بيانات إضافية عبر Power Apps.

![إضافة حقول أو إزالتها من مهمة تكامل.](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>بعد إعداد التكامل كوظيفة دفعية، ولكن فقد Human Resources الاتصال بالنظام الوجهة. كيف يمكنني إرسال مجموعة التغييرات نفسها إلى النظام الوجهة؟

لا حاجة إلى أي إعداد خاص لمعالجة الاستثناء. سيقوم موحد البيانات بشكل تلقائي بالتقاط الأخطاء التي تحدث في المصدر والوجهة وسيبلغ عنها وسيسمح بإعادة المحاولة يدويًا. ومع ذلك، فهو لا يسمح بتصحيح البيانات يدويًا. إن كان هناك حاجة إلى إجراء عمليات تحديث للبيانات، فيجب أن تحدث في المصدر أو الوجهة.

## <a name="can-i-set-up-bi-directional-integration"></a>هل يمكنني إعداد تكامل ثنائي الاتجاه؟

لا، يكون التكامل حاليًا ذو اتجاه واحد (من Human Resources إلى Finance and Operations). ومع ذلك، يوجد قالب افتراضي لإرسال البيانات من Human Resources إلى Finance.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>هل يمكنني السماح بحذف السجلات كجزء من عملية التكامل؟

لا، لن يلتقط موحد البيانات السجلات المحذوفة لنقل البيانات. في الوقت الحالي، لم يتم تضمين سواء عمليات إنشاء وتحديث البيانات (UPSERT).

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>هل يمكن إعادة تشغيل التنفيذ الذي يتضمن أخطاء؟ إذا كان الأمر كذلك، فهل سيرسل ملفًا كاملاً أو التغييرات فقط؟

عملية التشغيل الأولى لموحد البيانات هي دائمًا عملية تشغيل كاملة. وتستند عمليات التشغيل التالية إلى تعقب التغييرات. يستخرج تشغيل الخطأ، عند تنفيذه، السجلات الموجودة في نطاق التشغيل ويرسل أحدث التغييرات من Dataverse.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>عند حفظ المشروع، أتلقى رسالة الخطأ: "يتضمن المشروع أخطاء تعيين". ماذا أفعل؟

تحقق من إعداد مفاتيح التكامل، وأدخل أية تغييرات مطلوبة على الإعداد، ثم قم بتحديث الكيانات في المشروع.

عند استخدام القالب الافتراضي، سيتم استيراد مفاتيح التكامل بشكل تلقائي. قد تحدث هذه المشكلة عند إضافة مهام جديدة إلى القالب الموجود.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>إذا كان لديّ العدد N من الكيانات القانونية حتى توجد توظيفات للعاملين، هل أحتاج إلى إنشاء تعيين لكل واحد منهم؟

نعم، لكل كيان قانوني في Finance، ستحتاج إلى مشروع تكامل منفصل في تكامل البيانات.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>أحتاج إلى نقل البيانات التي لا تشكل جزءًا من القالب الافتراضي التي وفرته Microsoft. هل يمكنني القيام بذلك؟

نعم، يمكن إضافة حقول أو إزالتها من القالب الموجود. ويمكن تعديل القالب لتضمين بيانات إضافية من جداول أخرى في Dataverse. يجب أن يكون الكيان في Dataverse لكي يتم تضمينه في القالب. 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>لقد انتهيت الآن من إنشاء بيئات Finance وHuman Resources الجديدة، وتلقيت رسالة الخطأ "‏‫انتهكت قيمة البيانات قيود التكامل." ما السبب؟

بإمكان أسباب هذا الخطأ أن تشتمل على:

- أدى نقل البيانات إلى استخراج سجلات مكررة في المصدر (Dataverse).

- تتضمن عملية نقل البيانات قيمًا فارغة للحقول المطلوبة في Finance and Operations. تأكد من أن البيانات موجودة في Dataverse وتستوفي شروط Finance and Operations.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>إذا ظهرت أخطاء تتعلق بالتنفيذ ولم تتم مزامنة معرّف الموظف، كيف يمكنني العثور على محفوظات الوظيفة التي تتضمن سجل الموظف الفاشل؟

سينشئ موحد البيانات عدة مشاريع في Finance. وتكون العلاقة بين مهمة موحد البيانات ومشروع Finance علاقة واحد بواحد.

تتبع الوقت اعتبارًا من سجل تنفيذ موحد البيانات وابحث عن مشروع الفهرس-1 في Finance. إذا كان رقم مهمة 9 في موحد البيانات"، فسيكون الفهرس 8 في Finance.

1. التقط فهرس المهمة من موحد البيانات (إنه "9" في هذا المثال).

    ![التقاط فهرس المهمة من موحد البيانات.](media/CaptureTaskIndex.png)

2. تعقب وقت تنفيذ المشروع.

    ![تعقب وقت تنفيذ المشروع.](media/CaptureTimeOfExecution.png)

3. في Finance، قم بتعريف الفهرس-1. في هذا المثال، يتوافق المشروع مع اللاحقة "8" ووقت تنفيذ مشروع الفهرس "0" مع وقت التنفيذ في الخطوة 2.

    ![تعريف الفهرس.](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a>بعد تكامل Human Resources وFinance، لا يمكنني رؤية بيانات Human Resources الخاصة بي في Finance. ماذا أفعل؟

التكامل مع Finance عبارة عن عملية تتكون من خطوتين. أولاً، تحقق من تحديث بيانات Human Resources ومن توفرها في Dataverse. هذا الأمر عبارة عن مزامنة قريبة من الوقت الحقيقي ويمكن التحقق منها في Power Apps عن طريق مراجعة البيانات في جداول البيانات.

![البيانات الموجودة في Dataverse.](media/DataInCDS.png)

إذا لم تظهر البيانات كما هو متوقع في Dataverse، فتأكد من دعم الكيان في التكامل. لتضمين بيانات إضافية في Dataverse، ستتم مطالبة بإجراء تغيير من جانب Microsoft.

إذا كان الكيان مدعومًا والبيانات متوفرة في Dataverse، فتأكد من صحة التعيين في موحد البيانات. إذا كان تعيين موحد البيانات مقبولاً، فتحقق عندئذِ من نجاح تشغيل مهام إدارة البيانات. قد تحدث بعض الأخطاء أثناء تنفيذ الوظائف الدفعية. لمزيد من المعلومات حول إدارة البيانات، راجع [إدارة البيانات](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a>عناوين الموظفين غير صحيحة بعد استيرادها إلى Finance. ماذا أفعل؟

يستخدم التسلسل الرقمي في **معرّف الموقع** النمط نفسه في كل من Human Resources وFinance. يجب أن يكون التسلسل الرقمي فريدًا على الجانبين لتفادي حدوث تضارب في العناوين عند تنفيذ تكامل البيانات من Dataverse إلى Finance and Operations.

أثناء تنفيذ Human Resources، تأكد من أن التسلسلات الرقمية ليست هي نفسها في Human Resources وFinance. تأكد من أن كافة التسلسلات الرقمية ليست مماثلة حيث قد يتم الاحتفاظ بالبيانات في كلا النظامين.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>عند إنشاء مجموعة الاتصالات، لا يمكنني رؤية الاتصال في القائمة المنسدلة "اتصال". ماذا أفعل؟

عند إنشاء اتصالاتك، تأكد من اختيار Dynamics 365 Finance و Dataverse.

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>عند مزامنة عمليات التوظيف، أتلقى رسائل الخطأ "CompanyInfo_FK غير موجود" أو "القيمة '12/31/2154 11:59:59 ص" في الحقل "تاريخ انتهاء التوظيف" غير موجودة في الجدول ذي الصلة "التوظيف"." ماذا أفعل؟‬

تأكد من أنك تقوم بالتعيين إلى الكيانات القانونية الصحيحة. لا تمثل مزامنة الكيان القانوني جزءًا من القالب الافتراضي، وبالتالي من المتوقع أن يكون كل كيان قانوني موجود في Human Resources و Dataverse موجود أيضًا في Finance. تأكد أيضًا من أنك تحدد الكيانات القانونية الصحيحة لمجموعة الاتصالات المرتبطة.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a>بعد إعداد مشروعي، يبدو تعيين الحقول في Finance فارغًا. ماذا أفعل؟

يمكنك تحديث كيانات البيانات في Finance بالانتقال إلى **إدارة البيانات \> محددات إطار العمل‬ \> إعدادات الكيان‬ \> تحديث قائمة الكيانات.** قد يستغرق استكمال هذا الإجراء دقائق قليلة تتمكن بعدها من رؤية هذه التعيينات. تحدث هذه المشكلة عند إنشاء مشاريع جديدة.

![تعيين حقول مفقود.](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>الموارد الإضافية

- موحد البيانات (DI): 

  - [دمج البيانات في Microsoft Dataverse](/powerapps/administrator/data-integrator)

  - [إدارة أخطاء موحد البيانات واستكشاف الأخطاء وإصلاحها](/powerapps/administrator/data-integrator-error-management)

  - [الاستجابة لطلبات DSR للسجلات التي أنشأها النظام في Power Apps و Microsoft Power AutomateوDataverse](/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- إدارة البيانات:

  - [إدارة البيانات](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
