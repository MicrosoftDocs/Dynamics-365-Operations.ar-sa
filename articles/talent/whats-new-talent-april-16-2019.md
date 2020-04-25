---
title: ما الجديد أو المتغير في Dynamics 365 Talent (16 أبريل 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/16/2019
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
ms.search.validFrom: 2019-04-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aa61a70e14b7997258376beaf389129a4ad2fa73
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197257"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-16-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent (16 أبريل 2019)

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

### <a name="process-auditing"></a>معالجة التدقيق

يمكنك الآن تعقب التغييرات التي تتم على المرشحين والوظائف الشاغرة واستمارات التقديم للوظائف. لمزيد من المعلومات، راجع [تعقب التغييرات في بيانات التعيين‬](process-auditing.md).

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2239. تشير الأرقام الموجودة بين أقواس إلى أرقام الدعم في Lifecycle Services (LCS).

### <a name="compensation-region-compensation-level-benefit-option-and-skill-type-entities-in-common-data-service-updated-to-include-customer-field-support"></a>تم تحديث كيانات منطقه التعويض ومستوى التعويض وخيار الميزة ونوع المهارة في Common Data Service لتضمين دعم حقل العميل.

مع هذا الإصدار، تم تحديث كيانات Common Data Service بحيث تتضمن القدرة على تضمين حقل مخصص تمت إضافته عبر خلال Talent: Core HR.

### <a name="powerbi-refresh-issues-314342"></a>مشكلات تحديث PowerBI (314342)

يعمل هذا التغيير على تصحيح مشكلة تتعلق بتحديث تقارير PowerBI بشكل صحيح.

### <a name="unable-to-click-directly-through-on-transition-tasks-in-employee-self-service-303309"></a>يتعذر النقر فوق المهام الانتقالية بشكل مباشر في الخدمة الذاتية للموظف (303309)

يتيح هذا التغيير للمستخدمين الذين لديهم دور الموظف تحديد مهام انتقالية وتحديثها من قائمة المهام في Talent.

### <a name="performance-feedback-email-message-updated-309615"></a>تحديث رسائل البريد الإلكتروني حول ملاحظات الأداء (309615)

مع هذا التغيير، تظهر رسالة تأكيد عند إرسال الملاحظات بنجاح.

### <a name="missing-tables-in-word-template-308048"></a>جداول مفقودة في قالب Word (308048)

مع هذا التغيير، عند إنشاء قالب Word يحتوي على معلومات حول الموظفين والمهارات، تظهر المهارات الخاصة بالموظف المحدد فقط في مستند Word.

### <a name="when-applying-an-offboarding-checklist-an-error-is-displayed-299877"></a>عند تطبيق قائمة اختيار إلغاء الإعداد، تظهر رسالة خطأ. (299877)

يعمل هذا التغيير على تصحيح مشكلة عند تطبيق قائمة اختيار إلغاء الإعداد مباشرة من النموذج الخاص بالعامل.

## <a name="in-preview"></a>قيد المعاينة

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>السماح بتعيين أكواد الأسباب على أنواع الإجازات

قد تحتاج المؤسسات إلى معلومات إضافية حول طلبات الإجازات. يمكنك الآن تحديد أكواد الأسباب لأنواع الإجازات وتمكين الموظفين من تحديد كود سبب في طلبات الإجازات.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>المطالبة بأكواد الأسباب لأنواع إجازات معينة على طلبات الإجازة

قد تطالب المؤسسات بتعيين أكواد الأسباب لأنواع إجازات معينة عند قيام الموظفين بتقديم طلب إجازة. قد يعود سبب ذلك إلى سياسة الشركة أو إلى متطلبات تنظيمية. يمكنك الآن تعيين أنواع الإجازات التي تحتاج إلى كود سبب، ويمكنك مطالبة الموظفين بتوفير كود سبب لنوع الإجازة في طلبات الإجازة.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>توفير قائمة حركات الغياب والإجازة لقسم الموارد البشرية

يؤدي تعقب وقت إجازات الموظفين وفهم كيفية احتساب الإجازات ليس فقط إلى مساعدة قسم الموارد البشرية على الرد على استفسارات الموظفين ولكنه يضمن أيضًا منح مكافآت إجازات دقيقة للموظفين. تتوفر لدى قسم الموارد البشرية الآن طريقة عرض جديدة للحركات (المُنح والاستحقاقات والتسويات والطلبات) للاطلاع على الأسباب التي تكمن خلف الأرصدة.

## <a name="coming-soon"></a>قريبًا

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>تحسينات في واجهة المستخدم للتحقق من وجود موظفين مكررين

مع هذا التغيير، يتم الكشف عن التكرارات عند إدخال حقول الأسماء، وتعرض الحالة عدد التكرارات التي تم العثور عليها. يمكنك تحديد الارتباط المتوفر لفتح صفحة جديدة لتقييم ما إذا كان يجب استخدام المطابقة التي تم الكشف عنها. لتجنب مقاطعة إدخال البيانات، لا يفتح نموذج التكرارات بشكل تلقائي.

### <a name="email-support-for-alerts"></a>دعم البريد الإلكتروني للتنبيهات

مع إصدار Platform update 25 لـ Finance and Operations، بإمكان المستخدمين إنشاء قواعد تنبيه ترسل بشكل تلقائي إعلامات بالبريد الإلكتروني إلى جهات الاتصال عند تشغيلها بواسطة حدث.


