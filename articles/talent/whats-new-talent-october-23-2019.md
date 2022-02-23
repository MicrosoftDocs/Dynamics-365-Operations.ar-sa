---
title: ما الجديد أو المتغير في Dynamics 365 Talent‏ (23 أكتوبر 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 27cb4a7c125cb2b330dff083c8ed0c1ee89c0e7e
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527993"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-23-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent‏ (23 أكتوبر 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract
يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>التغييرات في Onboard
يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2569. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-30-for-finance-and-operations-apps"></a>تحديث النظام الأساسي 30 لتطبيقات Finance and Operations

لمزيد من المعلومات، راجع [المزايا الجديدة أو المتغيرة في تحديث النظام الأساسي 30 لتطبيقات Finance and Operations (نوفمبر 2019)](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/whats-new-platform-update-30).

### <a name="remove-benefits-open-enrollment-preview-feature"></a>إزالة الميزات التي تفتح ميزة معاينة التسجيل

بالتزامن مع إعلاننا الخاص بالاستثمارات الاستراتيجية المنشور في [مدونة التفوق العملي لتحسين core HR](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence)، تعمل Microsoft على إزالة الميزات التي تفتح ميزة التسجيل المعاينة العامة في 18 أكتوبر 2019. بدلاً من ذلك، سيتم إصدار وظيفة جديدة في المستقبل. لن يتم اعتماد استخدام الإنتاج للميزات التي تفتح ميزة التسجيل المتاحة حاليًا في المعاينة العامة.

### <a name="error-while-selecting-the-countryregion-on-the-worker-form-a-second-time-350294"></a>حدث خطأ أثناء تحديد البلد/المنطقة في نموذج العامل للمرة الثانية (350294)

وباستخدام إصدار هذا الأسبوع، يتم تصحيح المشكلة عند تحديد بلد/منطقه في نموذج **العامل**.

### <a name="financial-dimension-values-default-to-the-combination-display-field-when-do-not-allow-manual-entry-is-set-to-true-340097"></a>يتم تعيين قيم البعد المالي افتراضيًا إلى حقل العرض ‏‫"مجموعة مركبة‬" عند تعيين "‏‫عدم السماح بالإدخال اليدوي‬" إلى القيمة "صواب" (340097)

بهذا التغيير، عند إعداد الأبعاد المالية واستخدام خيار عدم السماح بالإدخال اليدوي، سيقوم النظام بتصحيح تعيين قيم البعد افتراضيًا إلى الحقل **‏‫عرض المجموعة‬**.

### <a name="new-relationship-types-should-be-added-to-relationship-lookup-in-the-personal-contacts-form-347691"></a>يجب إضافة أنواع علاقات جديدة إلى البحث في العلاقة في نموذج جهات الاتصال الشخصية (347691)

يتضمن هذا الإصدار قدرات جديدة لإضافة أنواع علاقات جديدة في جدول **أنواع العلاقات** وتطبيق هذه التغييرات في بحث العلاقة عن جهات الاتصال الشخصية.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-379599"></a>لا تنعكس قيم القائمة الإضافية في الحقول المخصصة في Common Data Service (379599)

في إصدار هذا الأسبوع، بإضافة قيمة قائمة جديدة إلى حقل مخصص موجود تمت مزامنته بالفعل مع Common Data Service، ستظهر قيم قائمة الانتقاء الجديدة بعد تطبيق التغييرات على الكيان.

### <a name="on-the-terms-of-employment-page-all-employees-terms-of-employment-appear-after-selecting-open-in-excel-348073"></a>في صفحة "شروط التوظيف"، تظهر كل شروط الموظفين للتوظيف بعد تحديد فتح في Excel (348073)

في هذا الإصدار، سيتم فقط فتح شروط التوظيف الخاصة بالموظفين المحددين في Excel. كما يتم أيضا سداد الرهن بالكامل للشركة.

### <a name="the-association-between-the-work-calendar-holiday-entity-and-the-work-calendar-entity-is-missing-in-common-data-service-324178"></a>الاقتران بين كيان عطلة تقويم العمل وكيان تقويم العمل مفقود في Common Data Service (324178)

تمت إضافة هذه العلاقة مع الإصدار. سيؤدي هذا التغيير إلى تمكين أيام العمل للموظف للعرض في PowerApps. 

### <a name="error-when-using-employee-self-service-workflows-with-configurable-hierarchies-370132"></a>حدث خطأ عند استخدام عمليات سير عمل الخدمة الذاتية للموظف مع التدرجات الهرمية القابلة للتكوين (370132)

في هذا الإصدار، تتوفر مراسلة أفضل حول كيفية تكوين مهام سير العمل باستخدام التدرجات الهرمية القابلة للتكوين. 

### <a name="system-allows-creation-of-new-positions-where-the-available-for-assignment-date-is-earlier-than-the-activation-date-340103"></a>يسمح النظام بإنشاء مناصب جديدة بحيث يكون تاريخ ‏‫متوفر للتعيين‬ أقدم من تاريخ التنشيط (340103).

سيعرض هذا التغيير تحذيرا عندما يكون تاريخ **‏‫متوفر للتعيين‬** قبل تاريخ **التنشيط** للمنصب.

## <a name="coming-soon"></a>قريبًا

### <a name="print-performance-reviews"></a>طباعة مراجعات الأداء

راجع [‏‫طباعة مراجعات الأداء‬](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) في خطة الموجة 2 من إصدار Dynamics 365: 2019.

### <a name="feature-management-workspace"></a>مساحة عمل إدارة الميزات

تتم إضافة ميزات وتحديثها في كل إصدار. وتوفر تجربة إدارة الميزات مساحة عمل حيث يمكنك عرض قائمه بالميزات التي تم تقديمها في كل إصدار. بشكل افتراضي، تكون الميزات الجديدة متوقفة عن التشغيل. ويمكنك استخدام مساحة العمل لتشغيلها وعرض الوثائق الخاصة بها.

لمعرفة المزيد حول التغييرات المصاحبة لإدارة الميزات، راجع [نظرة على إدارة الميزات‬](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
