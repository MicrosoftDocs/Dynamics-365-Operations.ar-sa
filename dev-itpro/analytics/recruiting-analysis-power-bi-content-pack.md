---
title: "محتوى Power BI للتوظيف"
description: "يوضح هذا الموضوع محتوى Power BI للتوظيف في Dynamics 365 for Operations. وتوضح هذه المقالة كيفية الوصول إلى التقارير التي تم تضمينها في حزمة المحتوى، وتوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء حزمة المحتوى."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4b12a2c8983cf7bef770417f76df324293f06fb2
ms.contentlocale: ar-sa
ms.lasthandoff: 05/25/2017


---

# <a name="recruiting-power-bi-content"></a>محتوى Power BI للتوظيف

[!include[banner](../includes/banner.md)]


يوضح هذا الموضوع محتوى Power BI للتوظيف في Dynamics 365 for Operations. وتوضح هذه المقالة كيفية الوصول إلى التقارير التي تم تضمينها في حزمة المحتوى، وتوفر معلومات حول نموذج البيانات والكيانات المستخدمة لإنشاء حزمة المحتوى.

<a name="accessing-the-content-pack"></a>الوصول إلى حزمة المحتوى
--------------------------

يمكنك العثور على حزمة محتوى التوظيف في مكتبة الأصول المشتركة في Microsoft Dynamics Lifecycle Services. لمزيد من المعلومات حول كيفية تحميل حزمة المحتوى وربطها ببيانات Microsoft Dynamics 365 for Operations، راجع [محتوى "Power Bi" في LCS من Microsoft والشركاء](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>التقارير المضمنة في حزمة المحتوى
بعد أن تقوم بتوصيل محتوى الحزمة ببيانات Microsoft Dynamics 365 for Operations، تعرض التقارير بيانات المؤسسة. إذا لم يسبق لك استخدام Microsoft Power BI، فيمكنك معرفة المزيد حول هذا التطبيق على [صفحة التعليم الموجّه لـ Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). تحتوي التقارير المضمنة في حزمة المحتوى على كل من المخططات والجداول التي تحتوي على معلومات إضافية. يصف الجدول التالي التقارير.

| تقرير                       | المحتويات                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| تحليل مقدم الطلب           | مقدمو الطلبات حسب الوظيفة، ومصادر مقدمي الطلبات، ومقدمو الطلبات حسب الموقع، والعدد الإجمالي لمقدمي الطلبات           |
| حالة مقدم الطلب             | مقدمو الطلبات حسب النوع والحالة، وحالة مقدم الطلب                                                    |
| ‏‫التوزيع الجغرافي لمقدمي الطلبات       | مقدمو الطلبات حسب العمر والجنس، ومقدمو الطلبات حسب مستوى التعليم والحالة                             |
| تحليل التوظيف          | صافي نسبة التوظيف، ومتوسط الأيام للتوظيف، نسبة حالات التوظيف السيئة، وتكاليف التوظيف                    |
| تحليل مشاريع التوظيف | عدد مشاريع التوظيف، وفرص العمل الشاغرة حسب مشروع التوظيف، ومقدمو الطلبات حسب مشروع التوظيف |

يمكنك تصفية المخططات والتجانبات في هذه التقارير، وتثبيت المخططات والتجانبات بلوحة المعلومات. لمزيد من المعلومات حول كيفية التصفية والتثبيت في Power BI، راجع [إنشاء لوحة معلومات وتكوينها](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>فهم نموذج البيانات والكيانات
تُستخدم بيانات Dynamics 365 for Operations لملء التقارير في حزمة محتوى التوظيف. يعرض الجدول التالي الكيانات التي استندت عليها حزمة المحتوى.

| الكيان                          | المحتويات                                                         | العلاقات مع الكيانات الأخرى                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recruiting\_Applicant           | مقدمو الطلبات، ومقدمو الطلبات الذين تم توظيفهم، وصافي نسبة التوظيف، والتكاليف          | Recruiting\_ApplicantName Recruiting\_Company Recruiting\_CalendarOffset Recuriting\_Date Recruiting\_GeographicLocation Recruiting\_Demographics Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject                                |
| Recruiting\_ApplicantName       | الاسم الأول لمقدم الطلب، والاسم الأخير، والاسم بالكامل                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_CalendarOffset      | مقاصات التقويم إلى تقارير الشرائح                                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Company             | تقوم الشركات بتصفية التقارير حسب                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Date                | الأيام والأسابيع والشهور والسنوات                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Demographics        | تاريخ الميلاد، والجنس والأصل العرقي والحالة الاجتماعية         | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_EmployedApplicant   | مقدم الطلب، والأداء، وتاريخ البدء، ونوع مقدم الطلب           | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_ApplicantName Recruiting\_Employment Recruiting\_Performance Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject          |
| Recruiting\_Employment          | تاريخ البدء، وتاريخ الانتهاء، وتاريخ الانتقال                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_GeographicLocation  | المدينة، والمقاطعة، والرمز البريدي، والمنطقة أو المقاطعة                 | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Job                 | الوظيفة، النوع والعنوان                                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Media               | مصدر مقدمي الطلبات                                             | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Performance         | التقييم والوصف ونموذج التقييم                            | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_RecruitmentProject  | وصف المشروع، وحالة المشروع، وفرص العمل الشاغرة                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_TerminatedApplicant | مقدمو الطلبات المفصولون، والسبب، والأداء، وتاريخ الفصل | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_Performance Recruiting\_Demographics Recruiting\_Employment Recruiting\_Media Recruiting\_RecruitmentProject Recruiting\_ApplicantName |

استُخدمت هذه الكيانات لإنشاء القياسات المحسوبة. ثم استخدمت القياسات المحسوبة لإنشاء مؤشرات الأداء الرئيسية والتقارير المستخدمة في حزمة المحتوى. إذا كنت تريد تضمين حسابات إضافية في تقاريرك ولوحة المعلومات، يمكنك تنزيل وتعديل ملف Recruiting.pbix من LCS. هذا الملف هو نموذج البيانات الافتراضي الذي تم استخدامه لإنشاء حزمة المحتوى. بعد إجراء التعديلات، يمكنك إنشاء حزمة المحتوى التنظيمية ولوحة المعلومات التي تحتوي على المعلومات التي قمت بإضافتها.

## <a name="additional-resources"></a>الموارد الإضافية
فيما يلي بعض الارتباطات المفيدة المتعلقة بالكيانات وإنشاء محتوى Power BI:

-   [كيانات البيانات](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [إنشاء حزم المحتوى التنظيمية](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [تصميم البيانات باستخدام Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [إضافة إطارات Power BI المتجانبة إلى مساحات العمل](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





