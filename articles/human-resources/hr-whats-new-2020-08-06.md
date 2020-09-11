---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources (06 أغسطس 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 06 أغسطس 2020.
author: darinkramer
manager: AnnBe
ms.date: 8/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-08-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 94d8291190b6c08c6e0e5241513989354df7939d
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/20/2020
ms.locfileid: "3711832"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-06-2020"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources (06 أغسطس 2020)

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.3444. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.

## <a name="platform-update-1001236-is-now-available"></a>يتوفر الآن تحديث النظام الأساسي 10.0.12(36)

لمزيد من المعلومات، راجع [تحديثات النظام الأساسي للإصدار 10.0.12 من تطبيقات Finance and Operations (أغسطس 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12).

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>كيانات إطار عمل إدارة البيانات (DMF) لإدارة المزايا
 
يتم إصدار كيانات إدارة المزايا. تتيح كيانات DMF استيراد البيانات وتصديرها لتكوين إدارة المزايا بسهولة. كما سيتوفر قالب إدارة المزايا لنقل البيانات. يقوم هذا القالب بتصدير البيانات واستيرادها بطريقة تسلسلية لمراعاة تبعيات البيانات. لمزيد من المعلومات، راجع:

- [دعم كيان DMF](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support) في خطة الموجة 1 من إصدار 2020 لتطبيق Dynamics 365
- [نظرة عامة حول إدارة البيانات](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages)


## <a name="claire-creates-a-workflow-for-buying-and-selling-leave-requests-446557"></a>تقوم كلير بإنشاء سير عمل لطلبات شراء وبيع الإجازات (446557)

لمزيد من المعلومات، راجع:

- [السماح للموظفين ببيع وشراء الإجازات](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365
- [إدارة سياسات شراء الإجازة وبيعها](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [شراء الإجازة وبيعها](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)


## <a name="worker-postal-addresses-v2-entity-has-access-across-legal-entities-with-restricted-access-459126"></a>يتوفر للإصدار V2 من العناوين البريدية للعامل حق الوصول عبر الكيانات القانونية مع وصول مقيد (459126)

ومع هذا التغيير، سيقوم كيان **الإصدار V2 من العنوان البريدي للعامل** بتقييد الوصول إلى الكيان القانوني الذي تم إعطاؤه للمستخدم.

## <a name="workflow-email-hyperlink-fails-to-open-relevant-reviews-437398"></a>فشل ارتباط البريد الإلكتروني لسير العمل بفتح مراجعات ذات صلة (437398)

عند استخدام العنصر النائب لفتح مراجعة أداء في سير عمل المراجعة، يقوم الآن الارتباط التشعبي الذي تم إنشاؤه في البريد الإلكتروني بفتح السجل المحدد.

## <a name="new-entities-for-buying-and-selling-leave-473180"></a>كيانات جديدة لإجازات لبيع وشراء الإجازات (473180)

تتوفر الآن كيانات إطار عمل إدارة البيانات لبيع وشراء الإجازات. لمزيد من المعلومات، راجع [‏‫نظرة عامة على إدارة البيانات](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).

## <a name="when-viewing-record-information-and-using-advanced-filters-a-user-could-gain-access-to-other-employees-records-472490"></a>عند عرض معلومات السجل واستخدام عوامل التصفية المتقدمة، قد يصل المستخدم إلى سجلات الموظفين الآخرين (472490)

ومع هذا التغيير، يمكن لمستخدمي الخدمة الذاتية للموظفين الوصول إلى السجلات الخاصة بهم فقط أثناء استخدام الخدمة الذاتية للموظفين. لم يعد عرض معلومات السجل أثناء تغيير خيار التصفية لم يكشف عن بيانات إضافية.

## <a name="personnel-management-analytics-include-exited-worker-records-382893"></a>تتضمن تحليلات إدارة العاملين سجلات العاملين المغادرين (382893)

مع هذا الإصدار، تتضمن تحليلات إدارة العاملين الآن العاملين النشطاء فقط. 
 
## <a name="unable-to-process-a-merit-increase-for-an-employee-473125"></a>تعذّر معالجه زيادة الأهلية للموظف (473125)

يسمح لك هذا التغيير بإدخال زيادات الأهلية عند تغيير تاريخ السريان لزيادة الأهلية الجديدة.

## <a name="review-workflow-can-be-started-more-than-once-467541"></a>يمكن بدء سير عمل المراجعة أكثر من مرة (467541)

مع هذا التغيير، يمكنك بدء سير عمل مراجعة الأداء مرة واحدة فقط. لم تعد حالة المدير تعرض خيار بدء المراجعة.

## <a name="leave-request-work-flow-ends-in-error-when-canceling-an-approved-leave-request-472063"></a>ينتهي سير عمل طلب الإجازة عند إلغاء طلب إجازة موافق عليه (472063)

في هذا الإصدار، عندما تلغي طلب إجازة موافق عليها، لن يعود الطلب بحالة موافق عليها، وسيستمر سير العمل.

## <a name="system-suggests-exited-workers-when-creating-a-new-review-form-the-template-460624"></a>يقترح النظام عاملين مغادرين عند إنشاء مراجعة جديدة من القالب (460624)

ومع هذا التغيير، لن يعود العاملون المغادرون متاحين عند إنشاء مراجعات جديدة من قالب. لا يمكنك إنشاء مراجعات للموظفين الذين هم خارج تواريخ توظيفهم.

## <a name="position-hierarchy-circular-reference-detection-415879"></a>الكشف عن المرجع الدائري للتدرج الهرمي للمناصب (415879)

مع هذا التغيير، يقتصر الكشف عن المرجع الدائري للتدرج الهرمي للمناصب على وقت معين. يمكنك تشغيل الكشف عن المراجع الدائرية لتواريخ مختلفة للتحقق من عدم وجود أي مراجع دائرية في بنية التدرج الهرمي للمناصب.

## <a name="buy-and-sell-leave"></a>شراء الإجازة وبيعها 

توفر بعض المؤسسات ميزة تتيح للموظفين شراء الإجازات أو بيعها. غالبا ما تُدار هذه العملية يدويًا. تقوم هذه الميزة بأتمتة سياسات وطلبات الإدارة الخاصة بقسم الموارد البشرية. إذا تُبسط عملية عملية إدارة الإجازات وتساعد علي تقليل الأخطاء. لمزيد من المعلومات، راجع:

- [السماح للموظفين ببيع وشراء الإجازات](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365
- [إدارة سياسات شراء الإجازة وبيعها](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [شراء الإجازة وبيعها](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>استحقاق الإجازة‬‏‫ لشركة فردية أو خطة فردية

يمكن للعملاء معالجة الاستحقاقات لشركة فردية أو إجازة فردية وخطه غياب. وبذلك تصبح عملية الاستحقاق واضحة للعملاء الذين لديهم سياسات مختلفة تتعلق بسنوات الإجازة أو استحقاقات الإجازات. لمزيد من المعلومات، راجع [‏‫استحقاق الإجازات لكل شركة أو خطة إجازة‬](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>إضافة مرفقات إلى طلبات الإجازة

تعد القدرة على إضافه مرفقات إلى طلبات الإجازات المعتمدة عاملا مهما في بيئة مرض كوفيد-19 الحالي. يمكن للموظفين الآن إضافه هذه المرفقات. كما يتوفر لديهم المعرفة الكافية حول كيفية إجراء التحديثات على طلبات الإجازات. لمزيد من المعلومات، راجع [‏‫إضافة مرفق إلى طلب موجود‬](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>إضافة كود السبب إلى تعليقات الاستحقاق 

تمت إضافه أكواد السبب إلى تعليق الاستحقاق.

## <a name="carry-forward-rules"></a>قواعد نقل الإجازة 

يمكنك تحديد نوع الإجازة المنقولة للأرصدة المنقولة حيث يتم تحويل تسويات النقل. على سبيل المثال، إذا قام أحد الموظفين بنقل إجازة من 10 أيام، يمكنك انتقاء نوع إجازة آخر لمدة العشرة أيام هذه. لمزيد من المعلومات، راجع [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>تعليق استحقاق الإجازه لأنواع الإجازات المحددة

يمكن للموارد البشرية إنشاء قاعده لكي يتم تعليق استحقاق الإجازات للموظفين الذين لديهم طلبات الاجازه التي تم إدخالها لإجازه غير مدفوعة. يمكن أن تكون الإجازة غير المدفوع نوعا، ولكن ليس من الضروري أن تكون كذلك. يمكنك تعليق أي إجازة استنادا إلى نوع إجازة آخر.

## <a name="in-preview"></a>قيد المعاينة

### <a name="mandatory-fields"></a>حقول إلزامية

يمكنك جعل الحقول إلزامية باستخدام إمكانيات التخصيص في Human Resources. تتطلب هذه الميزة **طرق عرض محفوظة**. لمزيد من المعلومات حول طرق العرض المحفوظة، راجع:

- [طرق العرض المحفوظة - التوفر العام](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬
- [إنشاء نماذج تستخدم طرق العرض المحفوظة بشكل كامل](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a>تطبيق Human Resources في Teams

بإمكان الموظفين عرض وطلب الوقت بعيدًا عن العمل ضمن Microsoft Teams يمكنهم التفاعل مع روبوت لإنشاء طلبات الإجازات. لمزيد من المعلومات، راجع:

- [تجربة إجازة وغياب الموظف في Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬
- [تطبيق Human Resources في Teams](https://go.microsoft.com/fwlink/?linkid=2127841)

### <a name="dmf-entity-available-for-accrual-suspensions"></a>يتوفر كيان DMF لتعليقات الاستحقاق

يتوفر كيان DMF الآن لتعليقات الاستحقاق.

## <a name="coming-soon"></a>قريبًا

## <a name="checklist-entities-included-in-common-data-service"></a>تضمين كيانات قائمة الاختيار في Common Data Service

ستتوفر كيانات قائمة الاختيار لعمليات الإلحاق وإلغاء الإلحاق والتحويلات وعمليات الأعمال قريبًا في Common Data Service.

## <a name="known-issues"></a>مشكلات معروفة

قد تعرض مساحة عمل **إدارة الميزات** ميزات معطلة كميزات معاينة عندما تكون متوفرة بشكل عام. فيما يلي قائمة بالميزات المتوفرة بشكل عام والتي تعرض حالة غير صحيحة. 

1.  إدارة المزايا
2.  إدارة الحالة
3.  تسجيل قاعدة البيانات (تدقيق)
4.  استحقاق الإجازة لشركة واحدة أو خطة واحدة
5.  تعليق استحقاق الإجازة والغياب
6.  كود سبب تسوية الرصيد والتعليق
7.  شراء الإجازة وبيعها
8.  تقويم الإجازة والغياب
9.  قواعد الرصيد المحول للإجازة
10. تدقيق استحقاق الإجازة
11. حذف استحقاقات الإجازة
12. تقريب استحقاق الإجازة‬
13. تكوين أنواع إجازات متعددة في خطة إجازة واحدة
14. تحسينات تحديث تفاصيل الإجازات
15. استخدام تكافؤ الدوام الكامل‬ للموظف للاستحقاقات‬
16. طريقة عرض التعويض الثابت عبر الشركة
17. طباعة مراجعات الأداء
18. تصحيحات العطلات في استحقاق الإجازة

## <a name="see-also"></a>راجع أيضًا

[الجديد أو المتغير في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)
