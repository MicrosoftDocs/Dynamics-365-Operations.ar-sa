---
title: ما الجديد أو المتغير في Dynamics 365 Talent‏ (6‏ مايو 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c04af27bcc446b516f14125e71fb707bfd1d7708
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529698"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-6-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent‏ (6‏ مايو 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

### <a name="select-optional-documents-upon-offer-creation"></a>تحديد مستندات اختيارية بعد إنشاء العرض

عندما تقوم بتحديد قالب حزمة عرض، يطالبك الآن Attract بتحديد المستندات الاختيارية القابلة للتطبيق من قالب الحزمة هذا. يمكنك إضافة مستندات اختيارية أخرى أثناء تحضير العرض.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2282. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-26-for-finance-and-operations"></a>تحديث النظام الأساسي 26 لـ Finance and Operations

للحصول على مزيد من التفاصيل حول تحديث النظام الأساسي 26 لـ Finance and Operations، راجع [ميزات المعاينة في تحديث النظام الأساسي 26 لـ Dynamics 365 Finance and Operations (مايو 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26). 

### <a name="common-data-service-entity-support-for-custom-fields"></a>دعم كيان Common Data Service للحقول المخصصة

في إصدار الأسبوع هذا، تدعم الكيانات التالية الآن الحقول المخصصة: تكرار حساب الميزات ومعدل حساب الميزات ونوع الميزة وتقويم العمل وأيام العطل في تقويم العمل ودوره الدفع وأنواع تعريف العامل.

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a>التسجيل الجماعي في العطل وتغيير أساس المستوى إلى "تاريخ الأقدمية" لا يؤدي إلى تحديث معدل الاستحقاق الأولي (318526)

عند تسجيل الموظفين بشكل جماعي وتغيير أساس المستوى، يعكس الاستحقاق الأولي الآن أساس المستوى الذي قمت بتحديده.

### <a name="workflow-showing-duplicate-place-holders-313636"></a>سير عمل يعرض عناصر نائبة مكررة (313636)

التغييرات في هذا الإصدار تزيل تكرار العناصر النائبة عند إرسال إخطارات سير العمل.

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a>لا يتم تحديث حقول الأبعادة عند استخدام "فتح في Excel" ‏(176261)

مع هذا الإصدار، يمكنك الآن تحديث البعد المالي باستخدام **فتح في Excel** من صفحة **العامل**. 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a>لا تتم مزامنة عنوان العامل المُنشأ في Common Data Service مع Talent‏ (317555)

مع هذا التغيير، يتم تحديث العناوين المُنشأة في Common Data Service في Talent: Core HR.


## <a name="in-preview"></a>قيد المعاينة

### <a name="new-page-to-validate-position-hierarchy-data"></a>صفحة جديدة للتحقق من صحة بيانات التدرج الهرمي للمناصب

بإمكان قسم الموارد البشرية (البشرية) والمسؤولين الآن التحقق من صحة التدرج الهرمي الإداري لأي مراجع دائرية قد يتم استيرادها بشكل غير مقصود. يمكنك الوصول إلى هذه الصفحة الجديدة من **الإدارة التنظيمية > الارتباطات > المناصب > التحقق من صحة بيانات التدرج الهرمي للمناصب‬**.

### <a name="specify-reason-codes-on-leave-types"></a>تحديد أكواد الأسباب في أنواع الإجازات

قد تحتاج المؤسسات إلى معلومات إضافية حول طلبات الإجازات. يمكنك الآن تحديد أكواد الأسباب لأنواع الإجازات وتمكين الموظفين من تحديد كود سبب في طلبات الإجازات.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>المطالبة بأكواد الأسباب لأنواع إجازات معينة على طلبات الإجازة

قد تطالب المؤسسات بتعيين أكواد الأسباب لأنواع إجازات معينة عند قيام الموظفين بتقديم طلبات إجازة. قد يكون هذا الشرط موجودًا بسبب سياسة الشركة أو المتطلبات التنظيمية. يمكنك الآن تعيين أنواع الإجازات التي تحتاج إلى كود سبب، ويمكنك مطالبة الموظفين بتوفير كود سبب لنوع الإجازة في طلبات الإجازة.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>توفير قائمة حركات الغياب والإجازة لقسم الموارد البشرية

تؤدي القدرة على تعقب وقت إجازات الموظفين وفهم كيفية احتساب الإجازات ليس فقط إلى مساعدة قسم الموارد البشرية على الرد على استفسارات الموظفين ولكنها تساعد أيضًا على ضمان منح مكافآت إجازات دقيقة للموظفين. تتوفر لدى قسم الموارد البشرية الآن طريقة عرض جديدة للحركات (المُنح والاستحقاقات والتسويات والطلبات) لتمكين موظفي الموارد البشرية من الاطلاع على الأسباب التي تكمن خلف الأرصدة.

## <a name="coming-soon"></a>قريبًا

### <a name="indicate-instance-type-when-provisioning-talent"></a>الإشارة إلى نوع المثيل عند تزويد Talent

عند تزويد مثيل Talent جديد، ستتمكن من الإشارة إلى ما إذا كان نوع المثيل هو **إنتاج** أو **بيئة اختبار معزولة**، مما يسمح بالاختبار المبكر للميزات الجديدة. سيتم تحديث كافة مثيلات Talent الموجودة إلى نوع مثيل الإنتاج. إذا كنت ترغب في تحديث أحد المثيلات الموجودة لديك إلى نوع مثيل بيئة الاختيار المعزولة، الرجاء الاتصال بالدعم لبدء طلب التغيير.


[!INCLUDE[footer-include](../includes/footer-banner.md)]