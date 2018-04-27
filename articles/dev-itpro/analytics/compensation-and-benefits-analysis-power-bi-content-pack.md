---
title: "محتوى تعويض وميزات Power BI"
description: "يوضح هذا الموضوع محتوى تعويض وميزات Power BI في Finance and Operations."
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: cb43245afe578341251b140383a3b03ba2abd962
ms.openlocfilehash: 510064a462258b2a632eaa2a5ffd341950775b89
ms.contentlocale: ar-sa
ms.lasthandoff: 12/19/2017

---

# <a name="compensation-and-benefits-power-bi-content"></a>محتوى تعويض وميزات Power BI

[!INCLUDE [banner](../includes/banner.md)]

يوضح هذا الموضوع محتوى تعويض وميزات Power BI في Finance and Operations. 

## <a name="reports-that-are-included-in-the-content-pack"></a>التقارير المضمنة في حزمة المحتوى
بعد أن تقوم بربط حزمة المحتوى ببيانات Finance and Operations، يعرض التقرير بيانات المؤسسة. إذا لم يسبق لك استخدام Microsoft Power BI، فيمكنك معرفة المزيد حول هذا التطبيق على [صفحة التعليم الموجّه لـ Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). تحتوي التقارير المضمنة في حزمة المحتوى على كل من المخططات والجداول التي تحتوي على معلومات إضافية. يصف الجدول التالي التقارير.

| تقرير                     | المحتويات                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| التعويض وتحليل الفوائد | الموظفين العاملين بالساعة والموظفين بمرتب من قبل الشركة، متوسط الدفع بالسعة ومتوسط دفع الراتب، الموظفين بحسب نوع التوظيف وتسجيل الخطة |
| مزايا الموظف          | تسجيل الموظف بحسب الميزة المحددة                                                                                               |

يمكنك تصفية المخططات والتجانبات في هذه التقارير، وتثبيت المخططات والتجانبات بلوحة المعلومات. لمزيد من المعلومات حول كيفية التصفية والتثبيت في Power BI، راجع [إنشاء لوحة معلومات وتكوينها](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>فهم نموذج البيانات والكيانات
تستخدم بيانات Finance and Operations لملء التقارير في حزمة المحتوى الخاصة بالتعويض والميزات. يعرض الجدول التالي الكيانات التي استندت عليها حزمة المحتوى.

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
| Workforce\_Job                    | الوظيفة، النوع والعنوان                                                                                  | القوى العاملة\_CurrentPosition Workforce\_CurrentWorker                                                                                                                                                                                                                                                                              |
| القوى العاملة\_PastPositionAssignment | سبب التعيين، وتاريخ البدء، وتاريخ الانتهاء، والوظيفة                                                           | القوى العاملة\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                     |
| Workforce\_Performance            | التقييم والوصف ونموذج التقييم                                                                      | القوى العاملة\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| القوى العاملة\_المنصب               | القسم، والنظام المكافئ للدوام الكامل، والمنصب، ونوع المنصب، والمسمى الوظيفي                                                        | Workforce\_CurrentPosition Workforce\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Workforce\_PositionTrend          | المناصب على مدار الوقت، ومكافئ الدوام الكامل، والوظيفة                                                                          | القوى العاملة\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                     |
| Workforce\_ReportsToWorkerName    | الاسم الأول والاسم الأخير والاسم بالكامل                                                                       | القوى العاملة\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| القوى العاملة\_المهارة                  | المهارة، ونوع المهارة، والتقييم                                                                              |                                                                                                                                                                                                                                                                                                                                  |
| القوى العاملة\_TerminatedWorker       | عمال تم إنهاء خدمتهم، وتاريخ الإنهاء، والمسمى الوظيفي، والمنصب، والوظيفة                                             | القوى العاملة\_القوى العاملة بالشركة\_تعويض القوى العاملة\_GeographicLocation Workforce\_أداء القوى العاملة\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_تاريخ القوى العاملة\_WorkerTitle Workforce\_التوزيع الجغرافي للقوى العاملة\_توظيف القوى العاملة\_وظيفة القوى العاملة\_مناصب القوى العاملة\_WorkerBenefit |
| Workforce\_WorkerBenefit          | تاريخ السريان، وخيار الميزة، وخطة الميزة، ونوع الميزة                                             | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_WorkerName             | الاسم الأول والاسم الأخير والاسم بالكامل                                                                       | القوى العاملة\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| القوى العاملة\_WorkerTitle            | المسمى الوظيفي وتاريخ الأقدمية                                                                                   | القوى العاملة\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | الوقت الإضافي للعمال، وعدد الأشخاص، والشركة، والمنصب                                                        | القوى العاملة\_‬‏‫القوى العاملة بالشركة\_تعويض القوى العاملة\_GeographicLocation Workforce\_‬‏‫أداء القوى العاملة‬‏‫\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_تاريخ القوى العاملة‬‏\_WorkerTitle Workforce\_‬‏‫التوزيع الجغرافي للقوى العاملة\_توظيف القوى العاملة\_وظائف القوى العاملة\_WorkerBenefit                     |







