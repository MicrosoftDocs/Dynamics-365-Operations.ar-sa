---
title: محتوى "التعويض والميزات" في Power BI
description: تصف هذه المقالة محتوى التعويض والميزات في Power BI.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.openlocfilehash: 978aa4897c58518c430decd8570fa30c851349aa
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291847"
---
# <a name="compensation-and-benefits-power-bi-content"></a>محتوى "التعويض والميزات" في Power BI

[!include [banner](../includes/banner.md)]

تصف هذه المقالة محتوى التعويض والميزات في Power BI. 

## <a name="reports-that-are-included-in-the-content-pack"></a>التقارير المضمنة في حزمة المحتوى
بعد أن تقوم بربط حزمة المحتوى ببياناتك، يعرض التقرير بيانات المؤسسة. إذا لم يسبق لك استخدام Microsoft Power BI، فيمكنك معرفة المزيد حول هذا التطبيق على [صفحة التعليم الموجّه لـ Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). تحتوي التقارير المضمنة في حزمة المحتوى على كل من المخططات والجداول التي تحتوي على معلومات إضافية. يصف الجدول التالي التقارير.

| تقرير                     | المحتويات                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| التعويض وتحليل الفوائد | الموظفين العاملين بالساعة والموظفين بمرتب من قبل الشركة، متوسط الدفع بالسعة ومتوسط دفع الراتب، الموظفين بحسب نوع التوظيف وتسجيل الخطة |
| مزايا الموظف          | تسجيل الموظف بحسب الميزة المحددة                                                                                               |

يمكنك تصفية المخططات والتجانبات في هذه التقارير، وتثبيت المخططات والتجانبات بلوحة المعلومات. لمزيد من المعلومات حول كيفية التصفية والتثبيت في Power BI، راجع [إنشاء لوحة معلومات وتكوينها](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>فهم نموذج البيانات والكيانات
تستخدم بيانات التطبيق لملء التقارير في حزمة المحتوى الخاصة بالتعويض والميزات. يعرض الجدول التالي الكيانات التي استندت عليها حزمة المحتوى.

| الكيان                            | المحتويات                                                                                                   | العلاقات مع الكيانات الأخرى |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | مقاصات التقويم إلى تقارير الشرائح                                                                          | Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_WorkerTrend, Workforce\_TerminatedWorker |
| Workforce\_Company                | تقوم الشركات بتصفية التقارير حسب                                                                             | Workforce\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Compensation           | معدل الدفع والتكرار على مدار الوقت                                                                           | Workforce\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_CurrentCompensation    | معدل الدفع والتكرار اعتبارًا من التاريخ الحالي                                                              | Workforce\_Company, Workforce\_Compensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentPosition        | المناصب اعتبارًا من التاريخ الحالي، نظام مكافئ للدوام الكامل، والمناصب المفتوحة والمناصب المفتوحة لشغلها | Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentWorker          | العمال اعتبارًا من التاريخ الحالي والعمر، وعدد الأشخاص                                                         | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position, Workforce\_WorkerBenefit |
| Workforce\_Date                   | الأيام والأسابيع والشهور والسنوات                                                                             | Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Demographics           | تاريخ الميلاد، والجنس والأصل العرقي والحالة الاجتماعية                                                   | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Employment             | تاريخ البدء، وتاريخ الانتهاء، وتاريخ الانتقال                                                                  | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_GeographicLocation     | المدينة، والمقاطعة، والرمز البريدي، والمنطقة أو المقاطعة                                                           | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Job                    | الوظيفة، النوع والعنوان                                                                                  | Workforce\_CurrentPosition, Workforce\_CurrentWorker |
| Workforce\_PastPositionAssignment | سبب التعيين، وتاريخ البدء، وتاريخ الانتهاء، والوظيفة                                                           | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_Performance            | التقييم والوصف ونموذج التقييم                                                                      | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Position               | القسم، والنظام المكافئ للدوام الكامل، والمنصب، ونوع المنصب، والمسمى الوظيفي                                                        | Workforce\_CurrentPosition, Workforce\_CurrentWorker |
| Workforce\_PositionTrend          | المناصب على مدار الوقت، ومكافئ الدوام الكامل، والوظيفة                                                                          | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_ReportsToWorkerName    | الاسم الأول والاسم الأخير والاسم بالكامل                                                                       | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Skill                  | المهارة، ونوع المهارة، والتقييم                                                                              | |
| Workforce\_TerminatedWorker       | عمال تم إنهاء خدمتهم، وتاريخ الإنهاء، والمسمى الوظيفي، والمنصب، والوظيفة                                             | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position, Workforce\_WorkerBenefit |
| Workforce\_WorkerBenefit          | تاريخ السريان، وخيار الميزة، وخطة الميزة، ونوع الميزة                                             | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_WorkerName             | الاسم الأول والاسم الأخير والاسم بالكامل                                                                       | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_WorkerTitle            | المسمى الوظيفي وتاريخ الأقدمية                                                                                   | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_WorkerTrend            | الوقت الإضافي للعمال، وعدد الأشخاص، والشركة، والمنصب                                                        | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_WorkerBenefit |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
