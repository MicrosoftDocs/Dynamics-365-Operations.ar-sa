---
title: ما الجديد أو المتغير في Dynamics 365 for Talent (27 أغسطس 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8965636e539345be5ef0ad591f7017938efd322d
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529794"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a>ما الجديد أو المتغير في Dynamics 365 for Talent (27 أغسطس 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2447. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>لا يتم تمكين ميزات المعاينة إلا في مثيلات بيئة الاختبار المعزول

عند توفير مثيل جديد من Talent‬، يمكنك تحديد ما إذا كان نوع المثيل هو إنتاج أو بيئة اختبار معزولة. تسمح أنواع مثيلات بيئة اختبار معزولة بالاختبار المبكر للميزات الجديدة. سيتم تحديث كافة مثيلات Talent الموجودة إلى نوع مثيل الإنتاج. إذا كنت ترغب في تحديث أحد المثيلات الموجودة لديك إلى نوع مثيل بيئة الاختبار المعزولة، اتصل بـ الدعم لبدء طلب التغيير.

لمزيد من المعلومات حول كيفية نشر التغييرات، راجع [توفير Talent‬](./provisioning-talent.md).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>عرض معلومات موسعة حول الأداء في الخدمة الذاتية للمدير

سيسمح خيار جديد للمديرين بعرض أداء التقارير المباشرة والتقارير الملحقة. في الوقت الحالي، يمكن لمديري البنود تعيين أهداف الأداء وتحديثها وإصدار مراجعات جديدة. بالإضافة إلى ذلك، يمكن للمديرين المباشرين وموظفيهم الاحتفاظ بدفاتر يومية الأداء وتحديثها للمساعدة في ضمان كفاءة عملية مراجعه الأداء. عند تطبيق هذا التغيير، سيتمكن المديرون من عرض المعلومات المتعلقة بالأداء وصيانتها للتقارير الموسعة بالإضافة إلى التقارير المباشرة.

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a>لا يُسمح بحذف الكيانات القانونية عند وجود الموظفين داخل الشركة (339849)

مع هذا التغيير، أبريل يمكنك إزالة شركات أو حذفها في حال وجود موظفين وبيانات أخرى ذات صلة للكيان القانوني.

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a>لا تتطابق تحليلات المعلومات المهنية لإدارة التعويض على مساحة عمل التعويض (322493)

في هذا الإصدار، تم تعديل تحليلات التعويض لتعكس الخطط المعينة إلى الموظفين بدقة.

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a>العنصر النائب لسير العمل %company% يعرض DAT عند تعيين الموظفين عبر سير العمل (343905)

مع هذا الإصدار، يعرض العنصر النائب للشركة الكيان القانوني المرتبط بتوظيف الموظف الجديد.

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a>يعرض الكيان CDSJobPosition رسالة خطأ عندما يتم تعيين التاريخ "صالح حتى" (349387)

في هذا الإصدار، تسمح مصادر البيانات **تفاصيل المنصب‬** و **مدة المنصب** في الكيان **CDSJobPosition** بعمليات التحرير من Common Data Service في حقول **تاريخ السريان‬**. 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a>فيما يتعلق بانتهاء خدمات الموظف، تتم تعبئة آخر يوم عمل في تاريخ انتهاء التعيين (332496)

يؤدي هذا التغيير الآن إلى تعيين **تاريخ انتهاء التعيين** للمنصب إلى **تاريخ انتهاء التوظيف** بشكل افتراضي. يمكنك تغيير هذه الإعدادات الافتراضية أثناء إدخال البيانات.

### <a name="legal-entities-arent-limited-with-hire-338871"></a>الكيانات القانونية غير مقيدة بالتوظيف (338871)
 
يعمل هذا التغيير على تقييد عملية التوظيف لإظهار الكيانات القانونية التي يستطيع المستخدم الوصول اليها.  

## <a name="in-preview"></a>قيد المعاينة

### <a name="streamlined-employee-entry-and-navigation"></a>إدخال الموظفين والتنقل المبسط

تتوفر هذه الوظيفة الآن في البيئات التجريبية وبيئات الاختبار المعزولة. لتشغيل هذه الميزة، انتقل إلى **إدارة النظام > الارتباطات > الإعداد > محددات النظام‬ > ميزات المعاينة‬**. حدد **نموذج العامل المحسن والتنقل‬**. سيؤدي ذلك إلى تمكين هذه التغييرات لكافة المستخدمين. يمكنك إيقاف تشغيل هذا الخيار في اي وقت.

لمزيد من المعلومات، راجع [إدخال الموظفين والتنقل المبسط‬](./streamlined-employee-entry.md).

## <a name="coming-soon"></a>قريبًا

### <a name="platform-update-29"></a>update 29 للنظام الأساسي

للحصول على مزيد من التفاصيل حول Platform update 29، راجع [ميزات المعاينة في Dynamics 365 for Finance and Operations platform update 29 (أكتوبر 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).


[!INCLUDE[footer-include](../includes/footer-banner.md)]