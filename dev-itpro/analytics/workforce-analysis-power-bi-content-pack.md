---
title: "محتوى Power BI لمقاييس القوى العاملة"
description: "يوضح هذا الموضوع محتوى Power BI لمقاييس القوى العاملة في Dynamics 365 for Operations. وتوضح هذه المقالة كيفية الوصول إلى التقارير التي تم تضمينها في حزمة المحتوى، وتوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء حزمة المحتوى."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 351306857ae62496fb28e9bb55dcbb11e7c3fd00
ms.contentlocale: ar-sa
ms.lasthandoff: 04/25/2017


---

# <a name="workforce-metrics-power-bi-content"></a>محتوى Power BI لمقاييس القوى العاملة

[!include[banner](../includes/banner.md)]


يوضح هذا الموضوع محتوى Power BI لمقاييس القوى العاملة في Dynamics 365 for Operations. وتوضح هذه المقالة كيفية الوصول إلى التقارير التي تم تضمينها في حزمة المحتوى، وتوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء حزمة المحتوى.

<a name="accessing-the-content-pack"></a>الوصول إلى حزمة المحتوى
--------------------------

يمكنك العثور على حزمة محتوى مقاييس القوى العاملة في مكتبة الأصول المشتركة في Microsoft Dynamics Lifecycle Services. لمزيد من المعلومات حول كيفية تحميل حزمة المحتوى وربطها ببيانات Microsoft Dynamics 365 for Operations، راجع [محتوى "Power Bi" في LCS من Microsoft والشركاء](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>التقارير المضمنة في حزمة المحتوى
بعد أن تقوم بتوصيل محتوى الحزمة ببيانات Microsoft Dynamics 365 for Operations، تعرض التقارير بيانات المؤسسة. إذا لم يسبق لك استخدام Microsoft Power BI، فيمكنك معرفة المزيد حول هذا التطبيق على [صفحة التعليم الموجّه لـ Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). تحتوي التقارير المضمنة في حزمة المحتوى على كل من المخططات والجداول التي تحتوي على معلومات إضافية. يصف الجدول التالي التقارير.

| تقرير                                           | المحتويات                                                                                                                                                                                                            |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| تحليل ‏‫عدد الموظفين بالشركة، القسم، الموقع | عدد الموظفين بالشركة، وعدد الموظفين بالقسم، وعدد الموظفين بالموقع، وإجمالي عدد الموظفين                                                                                                                           |
| تحليل عدد الموظفين حسب المهمة، الخطوة، المدير            | عدد الموظفين حسب المهمة، وعدد الموظفين حسب الخطوة، وعدد الموظفين حسب المدير، وإجمالي عدد الموظفين                                                                                                                                      |
| تحليل اتجاهات عدد الموظفين                         | عدد الموظفين هذا العام مقابل العام الماضي بالشركة وعدد الموظفين المتداول في الأشهر الاثنى عشر الأخيرة                                                                                                                        |
| التوزيع الجغرافي للقوى العاملة                           | عدد الموظفين حسب العمر والجنس، وعدد الموظفين حسب الأصل العرقي، وعدد الموظفين حسب حالة الخبرة، وعدد الموظفين حسب الحالة الاجتماعية، وعدد الطلبة المتفرغين، ومتوسط مدة الخدمة، ومتوسط العمر، ونسبة الإناث إلى الذكور من الموظفين |
| تحليل المناصب                                | المناصب الشاغرة حسب القسم، والمناصب الشاغرة إلى المشغولة، والمناصب النشطة إلى غير النشطة، والمناصب حسب القسم                                                                                                   |
| تحليل ترك العمل                               | ترك العمل هذا العام مقابل العام الماضي، وترك العمل، ومتوسط مدة خدمة الأشخاص تاركي العمل، ومتوسط عمر الأشخاص تاركي العمل، والموظفون تاركو العمل بالسبب                                                                   |
| الأشخاص حسب القسم                             | الموظفين مع عدد الموظفين حسب القسم، والمنصب، وتاريخا بدء وانتهاء التعيين                                                                                                                       |
| تحليل الأقدمية                               | متوسط عدد سنوات الخدمة حسب الشركة وقائمة الأقدمية                                                                                                                                                              |
| الذكريات السنوية وسنوات الخدمة               | الموظفون حسب الذكريات السنوية وسنوات الخدمة                                                                                                                                                                    |

يمكنك تصفية المخططات والتجانبات في هذه التقارير، وتثبيت المخططات والتجانبات بلوحة المعلومات. لمزيد من المعلومات حول كيفية التصفية والتثبيت في Power BI، راجع [إنشاء لوحة معلومات وتكوينها](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>فهم نموذج البيانات والكيانات
تُستخدم بيانات Dynamics 365 for Operations لملء التقارير في حزمة محتوى مقاييس القوى العاملة. يعرض الجدول التالي الكيانات التي استندت عليها حزمة المحتوى.

| الكيان                            | المحتويات                                                                                                   | العلاقات مع الكيانات الأخرى                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Workforce\_CalendarOffset         | مقاصات التقويم إلى تقارير الشرائح                                                                          | القوى العاملة\_PastPositionAssignment Workforce\_PositionTrend Workorce\_WorkerTrend Workforce\_TerminatedWorker                                                                                                                                                                                                                     |
| Workforce\_Company                | تقوم الشركات بتصفية التقارير حسب                                                                             | القوى العاملة\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Workforce\_Compensation           | معدل الدفع والتكرار على مدار الوقت                                                                           | القوى العاملة\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Workforce\_CurrentCompensation    | معدل الدفع والتكرار اعتبارًا من التاريخ الحالي                                                              | القوى العاملة\_القوى العاملة بالشركة\_تعويض القوى العاملة\_التوزيع الجغرافي للقوى العاملة\_وظيفة القوة العاملة\_المنصب                                                                                                                                                                                                                            |
| Workforce\_CurrentPosition        | المناصب اعتبارًا من التاريخ الحالي، نظام مكافئ للدوام الكامل، والمناصب المفتوحة والمناصب المفتوحة لشغلها | Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                                                               |
| Workforce\_CurrentWorker          | العمال اعتبارًا من التاريخ الحالي والعمر، وعدد الأشخاص                                                         | القوى العاملة\_القوى العاملة بالشركة\_تعويض القوى العاملة\_GeographicLocation Workforce\_أداء القوى العاملة\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_التوزيع الجغرافي للقوى العاملة\_وظيفة القوى العاملة\_توظيف القوى العاملة\_منصب القوى العاملة\_WorkerBenefit                                            |
| Workforce\_Date                   | الأيام والأسابيع والشهور والسنوات                                                                             | القوى العاملة\_PastPositionAssignment Workforce\_PositionTrend Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                     |
| Workforce\_Demographics           | تاريخ الميلاد، والجنس والأصل العرقي والحالة الاجتماعية                                                   | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Employment             | تاريخ البدء، وتاريخ الانتهاء، وتاريخ الانتقال                                                                  | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_GeographicLocation     | المدينة، والمقاطعة، والرمز البريدي، والمنطقة أو المقاطعة                                                           | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Job                    | الوظيفة، النوع والعنوان                                                                                  | Workforce\_CurrentPosition Workforce\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Workforce\_JobPerferredSkill      |                                                                                                            |                                                                                                                                                                                                                                                                                                                                  |
| Workforce\_PastPositionAssignment | سبب التعيين، وتاريخ البدء، وتاريخ الانتهاء، والوظيفة                                                           | القوى العاملة\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                     |
| Workforce\_Performance            | التقييم والوصف ونموذج التقييم                                                                      | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_PersonSkill            | المستوى والمهارة                                                                                            | Workforce\_Skill                                                                                                                                                                                                                                                                                                                 |
| Workforce\_PersonSkillAnalysis    | الاعتماد والمستوى والمهارة                                                                                | Workforce\_Skill Workforce\_WorkerName                                                                                                                                                                                                                                                                                           |
| Workforce\_Position               | القسم، والنظام المكافئ للدوام الكامل، والمنصب، ونوع المنصب، والمسمى الوظيفي                                                        | Workforce\_CurrentPosition Workforce\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Workforce\_PositionTrend          | المناصب على مدار الوقت، ومكافئ الدوام الكامل، والوظيفة                                                                          | القوى العاملة\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                     |
| Workforce\_ReportsToWorkerName    | الاسم الأول والاسم الأخير والاسم بالكامل                                                                       | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Skill                  | المهارة، ونوع المهارة، والتقييم                                                                              | Workforce\_PersonSkill Workforce\_PersonSkillAnalysis                                                                                                                                                                                                                                                                            |
| Workforce\_TerminatedWorker       | عمال تم إنهاء خدمتهم، وتاريخ الإنهاء، والمسمى الوظيفي، والمنصب، والوظيفة                                             | القوى العاملة\_القوى العاملة بالشركة\_تعويض القوى العاملة\_GeographicLocation Workforce\_أداء القوى العاملة\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_تاريخ القوى العاملة\_WorkerTitle Workforce\_التوزيع الجغرافي للقوى العاملة\_توظيف القوى العاملة\_وظيفة القوى العاملة\_مناصب القوى العاملة\_WorkerBenefit |
| Workforce\_WorkerBenefit          | تاريخ السريان، وخيار الميزة، وخطة الميزة، ونوع الميزة                                             | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_WorkerName             | الاسم الأول والاسم الأخير والاسم بالكامل                                                                       | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend Workforce\_PersonSkillAnalysis                                                                                                                                                                                                                        |
| Workforce\_WorkerTitle            | المسمى الوظيفي وتاريخ الأقدمية                                                                                   | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | الوقت الإضافي للعمال، وعدد الأشخاص، والشركة، والمنصب                                                        | القوى العاملة\_‬‏‫القوى العاملة بالشركة\_تعويض القوى العاملة\_GeographicLocation Workforce\_‬‏‫أداء القوى العاملة‬‏‫\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_تاريخ القوى العاملة‬‏\_WorkerTitle Workforce\_‬‏‫التوزيع الجغرافي للقوى العاملة\_توظيف القوى العاملة\_وظائف القوى العاملة\_WorkerBenefit                     |

استخدمت هذه الكيانات لإنشاء القياسات المحسوبة في نموذج البيانات. ثم استخدمت القياسات المحسوبة لإنشاء مؤشرات الأداء الرئيسية والتقارير المستخدمة في حزمة المحتوى. إذا كنت تريد تضمين حسابات إضافية في تقاريرك ولوحة المعلومات، يمكنك تحميل وتعديل CompensationandBenefits.pbix من LCS. هذا الملف هو نموذج البيانات الافتراضي الذي تم استخدامه لإنشاء حزمة المحتوى. بعد إجراء التعديلات، يمكنك إنشاء حزمة المحتوى التنظيمية ولوحة المعلومات التي تحتوي على المعلومات التي قمت بإضافتها.

## <a name="additional-resources"></a>الموارد الإضافية
فيما يلي بعض الارتباطات المفيدة المتعلقة بالكيانات وإنشاء محتوى Power BI:

-   [كيانات البيانات](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [إنشاء حزم المحتوى التنظيمية](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [تصميم البيانات باستخدام Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [إضافة إطارات Power BI المتجانبة إلى مساحات العمل](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





