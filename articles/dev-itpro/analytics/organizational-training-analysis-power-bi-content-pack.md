---
title: "محتوى Power BI للتدريب المؤسسي"
description: "يشرح هذا الموضوع Finance and Operations - محتوى Power BI للتدريب التنظيمي."
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
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 19cc8f92b5bb6d9ddfdc77785e48de17ed005703
ms.openlocfilehash: 18567a3241fce02e17df368f544e545fad93e1d9
ms.contentlocale: ar-sa
ms.lasthandoff: 03/23/2018

---

# <a name="organizational-training-power-bi-content"></a>محتوى Power BI للتدريب المؤسسي

[!include[banner](../includes/banner.md)]


يشرح هذا الموضوع Finance and Operations - محتوى Power BI للتدريب التنظيمي. 

## <a name="reports-that-are-included-in-the-content-pack"></a>التقارير المضمنة في حزمة المحتوى
بعد أن تقوم بربط حزمة المحتوى ببيانات Finance and Operations، يعرض التقرير بيانات المؤسسة. إذا لم يسبق لك استخدام Microsoft Power BI، فيمكنك معرفة المزيد حول هذا التطبيق على [صفحة التعليم الموجّه لـ Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). تحتوي التقارير المضمنة في حزمة المحتوى على كل من المخططات والجداول التي تحتوي على معلومات إضافية. يصف الجدول التالي التقارير.

| تقرير          | المحتويات                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| تحليل الدورة التدريبية | التسجيل حسب الموقع، وحضور الدورة التدريبية حسب الحالة، وقائمة التسجيل |
| أنواع الدورات التدريبية    | أنواع الدورات التدريبية حسب المهارة                                                       |

يمكنك تصفية المخططات والتجانبات في هذه التقارير، وتثبيت المخططات والتجانبات بلوحة المعلومات. لمزيد من المعلومات حول كيفية التصفية والتثبيت في Power BI، راجع [إنشاء لوحة معلومات وتكوينها](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>فهم نموذج البيانات والكيانات
تستخدم بيانات Finance and Operations لملء التقارير في حزمة محتوى التدريب التنظيمي. يعرض الجدول التالي الكيانات التي استندت عليها حزمة المحتوى.

| الكيان                    | المحتويات                                                         | العلاقات مع الكيانات الأخرى                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Training\_CalendarOffset  | مقاصات التقويم إلى تقارير الشرائح                                | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Company         | تقوم الشركات بتصفية التقارير حسب                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Course          | الدورة التدريبية، والوصف، واسم المعلم، والموقع، والغرفة، والحالة | Training\_CourseAgenda Training\_CourseAttendees Training\_CourseSkill                                                                                                                             |
| Training\_CourseAgenda    | جدول الأعمال، والدورة التدريبية، وأوقات البدء والانتهاء                          | Training\_Company Training\_CalendarOffset Training\_Date Training\_Course                                                                                                                         |
| Training\_CourseAttendees | الاسم، والحالة، والمهمة، وتاريخ التسجيل                         | Training\_Company Training\_CalendarOffset Training\_Date Training\_Demographics Training\_Employment Training\_Course Training\_WorkerName Training\_WorkerTitle Training\_Job Training\_Position |
| Training\_CourseSkill     | المهارة، ونوع المهارة، والمستوى                                     | Training\_Course                                                                                                                                                                                   |
| Training\_Date            | الأيام والأسابيع والشهور والسنوات                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Demographics    | تاريخ الميلاد، والجنس والأصل العرقي والحالة الاجتماعية         | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Employment      | تاريخ البدء، وتاريخ الانتهاء، وتاريخ الانتقال                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Job             | الوظيفة، النوع والعنوان                                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Position        | المنصب، والمسمى الوظيفي، ومكافئ الدوام الكامل‬                  | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_WorkerName      | الاسم الأول والاسم الأخير والاسم بالكامل                             | Training\_CourseAttendees                                                                                                                                                                          |
| Training\_WorkerTitle     | المسمى الوظيفي وتاريخ الأقدمية                                         | Training\_CourseAttendees                                                                                                                                                                          |





