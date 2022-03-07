---
title: المحتوى "اختصاصات الموظفين وتطويرهم‬" في Power BI
description: يصف هذا الموضوع محتوى "اختصاصات الموظفين وتطويرهم‬" في Power BI.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 86988438d19fcfcef637df9789f23c86831edddd
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569677"
---
# <a name="employee-competencies-and-development-power-bi-content"></a>المحتوى "اختصاصات الموظفين وتطويرهم‬" في Power BI

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع محتوى "اختصاصات الموظفين وتطويرهم‬" في Power BI. 

## <a name="reports-that-are-included-in-the-content-pack"></a>التقارير المضمنة في حزمة المحتوى
بعد أن تقوم بربط حزمة المحتوى ببياناتك، يعرض التقرير بيانات المؤسسة. إذا لم يسبق لك استخدام Microsoft Power BI، فيمكنك معرفة المزيد حول هذا التطبيق على [صفحة التعليم الموجّه لـ Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). تحتوي التقارير المضمنة في حزمة المحتوى على كل من المخططات والجداول التي تحتوي على معلومات إضافية. يصف الجدول التالي التقارير.

| تقرير                            | المحتويات                                               |
|-----------------------------------|--------------------------------------------------------|
| تحليل الاختصاصات والتطوير | أنواع مهارات أعضاء الفريق ومهارات أعضاء الفريق حسب النوع |
| ملف تعريف المهارات                     | ملف تعريف المهارات الخاص بالموظف المحدد                |
| تحليل المهارات                    | المهارات حسب النوع والتقييم                              |

يمكنك تصفية المخططات والتجانبات في هذه التقارير، وتثبيت المخططات والتجانبات بلوحة المعلومات. لمزيد من المعلومات حول كيفية التصفية والتثبيت في Power BI، راجع [إنشاء لوحة معلومات وتكوينها](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>فهم نموذج البيانات والكيانات
تُستخدم بيانات التطبيق لتعبئة التقارير في حزمة المحتوى "اختصاصات الموظفين وتطويرهم‬". يعرض الجدول التالي الكيانات التي استندت عليها حزمة المحتوى.

| الكيان                            | المحتويات                                                                                                   | العلاقات مع الكيانات الأخرى |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | مقاصات التقويم إلى تقارير الشرائح                                                                          | |
| Workforce\_Company                | تقوم الشركات بتصفية التقارير حسب                                                                             | |
| Workforce\_Compensation           | معدل الدفع والتكرار على مدار الوقت                                                                           | |
| Workforce\_CurrentCompensation    | معدل الدفع والتكرار اعتبارًا من التاريخ الحالي                                                              | Workforce\_Company, Workforce\_CurrentCompensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentPosition        | المناصب اعتبارًا من التاريخ الحالي، نظام مكافئ للدوام الكامل، والمناصب المفتوحة والمناصب المفتوحة لشغلها | Workforce\_Job Workforce\_Position |
| Workforce\_CurrentWorker          | العمال اعتبارًا من التاريخ الحالي والعمر، وعدد الأشخاص                                                         | Workforce\_Company Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_PersonSkill, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position |
| Workforce\_Date                   | الأيام والأسابيع والشهور والسنوات                                                                             | |
| Workforce\_Demographics           | تاريخ الميلاد، والجنس والأصل العرقي والحالة الاجتماعية                                                   | |
| Workforce\_Employment             | تاريخ البدء، وتاريخ الانتهاء، وتاريخ الانتقال                                                                  | |
| Workforce\_GeographicLocation     | المدينة، والمقاطعة، والرمز البريدي، والمنطقة أو المقاطعة                                                           | |
| Workforce\_Job                    | الوظيفة، النوع والعنوان                                                                                  | |
| Workforce\_JobPreferredSkill      | الأهمية، التقييم، المهارات، مستوى المهارات                                                                 | Workforce\_Skill, Workforce\_Job |
| Workforce\_PastPositionAssignment | سبب التعيين، وتاريخ البدء، وتاريخ الانتهاء، والوظيفة                                                           | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_Performance            | التقييم والوصف ونموذج التقييم                                                                      | |
| Workforce\_PersonSkill            | المستوى، تاريخ المستوى، المهارة                                                                               | Workforce\_Skill |
| Workforce\_PersonSkillAnalysis    | معتمد، المستوى، تاريخ المستوى، المهارة                                                                    | Workforce\_WorkerName, Workforce\_Skill |
| Workforce\_Position               | القسم، والنظام المكافئ للدوام الكامل، والمنصب، ونوع المنصب، والمسمى الوظيفي                                                        | |
| Workforce\_PositionTrend          | المناصب على مدار الوقت، ومكافئ الدوام الكامل، والوظيفة                                                                          | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_ReportsToWorkerName    | الاسم الأول والاسم الأخير والاسم بالكامل                                                                       | |
| Workforce\_Skill                  | المهارة، ونوع المهارة، والتقييم                                                                              | |
| Workforce\_TerminatedWorker       | عمال تم إنهاء خدمتهم، وتاريخ الإنهاء، والمسمى الوظيفي، والمنصب، والوظيفة                                             | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position |
| Workforce\_WorkerName             | الاسم الأول والاسم الأخير والاسم بالكامل                                                                       | |
| Workforce\_WorkerTitle            | المسمى الوظيفي وتاريخ الأقدمية                                                                                   | |
| Workorce\_WorkerTrend             | الوقت الإضافي للعمال، وعدد الأشخاص، والشركة، والمنصب                                                        | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]