---
title: "محتوى Power BI للتدريب التنظيمي"
description: "يوضح هذا الموضوع محتوى Power BI للتدريب التنظيمي في Dynamics 365 for Operations. ويوضح كيفية الوصول إلى حزمة المحتوى، ويصف نموذج البيانات والكيانات المستخدمة لإنشاء حزمة المحتوى."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 104164f8ffd0d2bc3a64bf15d2fb5213234046ce
ms.lasthandoff: 03/31/2017


---

# <a name="organizational-training-power-bi-content"></a>محتوى Power BI للتدريب التنظيمي

[!include[banner](../includes/banner.md)]


يوضح هذا الموضوع محتوى Power BI للتدريب التنظيمي في Dynamics 365 for Operations. ويوضح كيفية الوصول إلى حزمة المحتوى، ويصف نموذج البيانات والكيانات المستخدمة لإنشاء حزمة المحتوى.

<a name="accessing-the-content-pack"></a>الوصول إلى حزمة المحتوى
--------------------------

يمكنك العثور على حزمة محتوى التدريب التنظيمي في مكتبة الأصول المشتركة في Microsoft Dynamics Lifecycle Services. لمزيد من المعلومات حول كيفية تحميل حزمة المحتوى وربطها ببيانات Microsoft Dynamics 365 for Operations، راجع [محتوى "Power Bi" في LCS من Microsoft والشركاء](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>التقارير المضمنة في حزمة المحتوى
بعد أن تقوم بربط محتوى الحزمة ببيانات Microsoft Dynamics 365 for Operations، تعرض التقارير بيانات المؤسسة. إذا لم يسبق لك استخدام Microsoft Power BI، فيمكنك معرفة المزيد حول هذا التطبيق على [صفحة التعليم الموجّه لـ Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). تحتوي التقارير المضمنة في حزمة المحتوى على كل من المخططات والجداول التي تحتوي على معلومات إضافية. يصف الجدول التالي التقارير.

| تقرير          | المحتويات                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| تحليل الدورة التدريبية | التسجيل حسب الموقع، وحضور الدورة التدريبية حسب الحالة، وقائمة التسجيل |
| أنواع الدورات التدريبية    | أنواع الدورات التدريبية حسب المهارة                                                       |

يمكنك تصفية المخططات والتجانبات في هذه التقارير، وتثبيت المخططات والتجانبات بلوحة المعلومات. لمزيد من المعلومات حول كيفية التصفية والتثبيت في Power BI، راجع [إنشاء لوحة معلومات وتكوينها](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>فهم نموذج البيانات والكيانات
تستخدم بيانات Dynamics 365 for Operations لملء التقارير في حزمة محتوى التدريب التنظيمي. يعرض الجدول التالي الكيانات التي استندت عليها حزمة المحتوى.

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

استخدمت هذه الكيانات لإنشاء القياسات المحسوبة في نموذج البيانات. ثم استخدمت القياسات المحسوبة لإنشاء مؤشرات الأداء الرئيسية والتقارير المستخدمة في حزمة المحتوى. إذا كنت تريد تضمين حسابات إضافية في تقاريرك ولوحة المعلومات، يمكنك تحميل وتعديل ملف Training.pbix من LCS.  هذا الملف هو نموذج البيانات الافتراضي الذي تم استخدامه لإنشاء حزمة المحتوى. بعد إجراء التعديلات، يمكنك إنشاء حزمة المحتوى التنظيمية ولوحة المعلومات التي تحتوي على المعلومات التي قمت بإضافتها.

## <a name="additional-resources"></a>الموارد الإضافية
فيما يلي بعض الارتباطات المفيدة المتعلقة بالكيانات وإنشاء محتوى Power BI:

-   [كيانات البيانات](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [إنشاء حزم المحتوى التنظيمية](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [تصميم البيانات باستخدام Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [إضافة إطارات Power BI المتجانبة إلى مساحات العمل](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





