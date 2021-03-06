---
title: محتوى "التعلم" في Power BI
description: يصف هذا الموضوع محتوى "التعلم" في Power BI
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 46b7a442470d1fe78ebc5c9d5a0c6e155c0d9918
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685239"
---
# <a name="learning-power-bi-content"></a>محتوى "التعلم" في Power BI

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع محتوى **التعلم** في Microsoft Power BI.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>التقارير المضمنة في محتوى Power BI

تحتوي التقارير المضمنة في محتوى **التعلم** في Power BI على المخططات والجداول التي تحتوي على معلومات إضافية. يصف الجدول التالي التقارير.

| تقرير                | المحتويات |
|-----------------------|----------|
| نظرة عامة على التعلم     | ملخص التقارير |
| تحليل الدورة التدريبية       | التسجيل حسب الموقع والحضور حسب الحالة والدورات التدريبية حسب نوع الشركة، وحضور الدورة التدريبية حسب الوظيفة |
| تحليل التسجيل | قائمة التسجيل |
| أنواع الدورات التدريبية          | أنواع الدورات التدريبية حسب المهارة |
| تحليل المعلم‬   | نسبة الدورات التدريبية للمعلمين وعدد المعلمين والدورات التدريبية حسب المعلم والدورات التدريبية لكل معلم وجدول أعمال الدورة التدريبية حسب المعلم |
| الدورات التدريبية المقدمة       | قائمة الدورات التدريبية |
| تصميم الدورات التدريبية        | جدول أعمال الدورة التدريبية |

يمكنك تصفية المخططات والتجانبات في هذه التقارير، وتثبيت المخططات والتجانبات بلوحة المعلومات. لمزيد من المعلومات حول كيفية التصفية والتثبيت في Power BI، راجع [إنشاء لوحة معلومات وتكوينها](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>فهم نموذج البيانات والكيانات

تستخدم البيانات التالية لملء التقارير في محتوى **التعلم** في Power BI. يوضح هذا الجدول الكيانات التي استند عليها المحتوى.

| الكيان           | المحتويات                                                         | العلاقات مع الكيانات الأخرى |
|------------------|------------------------------------------------------------------|-----------------------------------|
| مقاصة التقويم  | مقاصات التقويم إلى تقارير الشرائح                                | جدول أعمال الدورة التدريبية، حضور الدورة التدريبية |
| الشركة          | تقوم الشركات بتصفية التقارير حسب                                   | جدول أعمال الدورة التدريبية، حضور الدورة التدريبية |
| الدورة التدريبية           | الدورة التدريبية، والوصف، واسم المعلم، والموقع، والغرفة، والحالة | جدول أعمال الدورة التدريبية، حضور الدورة التدريبية، مهارات الدورة التدريبية |
| جدول أعمال الدورة التدريبية    | جدول الأعمال، والدورة التدريبية، وأوقات البدء والانتهاء                          | تاريخ الشركة، مقاصة التقويم، التاريخ، الدورة التدريبية |
| حضور الدورة التدريبية | الاسم، والحالة، والمهمة، وتاريخ التسجيل                         | الشركة، مقاصة التقويم، التاريخ، الدورة التدريبية، التوزيع الجغرافي، التوظيف، الدورة التدريبية، اسم الموظف، المسمى الوظيفي للموظف، الوظيفة، المنصب |
| مهارات الدورة التدريبية     | المهارة، ونوع المهارة، والمستوى                                     | الدورة التدريبية |
| التاريخ             | الأيام والأسابيع والشهور والسنوات                                   | جدول أعمال الدورة التدريبية، حضور الدورة التدريبية |
| التوزيع الجغرافي     | تاريخ الميلاد، والجنس والأصل العرقي والحالة الاجتماعية         | جدول أعمال الدورة التدريبية، حضور الدورة التدريبية |
| التوظيف       | تاريخ البدء، وتاريخ الانتهاء، وتاريخ الانتقال                        | جدول أعمال الدورة التدريبية، حضور الدورة التدريبية |
| الوظيفة              | الوظيفة، النوع والعنوان                                        | جدول أعمال الدورة التدريبية، حضور الدورة التدريبية |
| المهنة         | المنصب، والمسمى الوظيفي، ومكافئ الدوام الكامل‬                  | جدول أعمال الدورة التدريبية، حضور الدورة التدريبية |
| اسم الموظف    | الاسم الأول والاسم الأخير والاسم بالكامل                             | حضور الدورة التدريبية |
| المسمى الوظيفي للموظف   | المسمى الوظيفي وتاريخ الأقدمية                                         | حضور الدورة التدريبية |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]