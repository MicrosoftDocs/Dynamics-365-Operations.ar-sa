---
title: ما الجديد أو المتغير في Dynamics 365 Talent (30 أبريل 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/30/2019
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
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2539baba84bffeb21d351cc307191eea3e940515
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528185"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-30-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent (30 أبريل 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2270. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).

### <a name="provide-feedback"></a>تقديم ملاحظات

يقع الخيار الذي يسمح لك بتوفير الملاحظات في القائمة **تعليمات** (**?**) في Talent. توفر هذه القائمة الوصول إلى الموارد التالية:

- ملاحظات
- تعليمات
- البدء
- الدعم
- الأفكار
- حول

### <a name="improvements-to-the-user-interface-for-duplicate-employee-detection"></a>تحسينات في واجهة المستخدم للكشف عن وجود موظفين مكررين

بسبب هذا التغيير ، يتم الكشف عن التكرارات الآن عندما تقوم بتعيين حقول الأسماء، ويعرض مؤشر الحالة عدد التكرارات التي تم الكشف عنها. يفتح ارتباط متوفر صفحة حيث يمكنك تقييم ما إذا كان يجب عليك استخدام أحد التكرارات. لتجنب مقاطعة إدخال البيانات، لا تفتح صفحة التكرارات بشكل تلقائي. يجب تحديد الارتباط لفتح الصفحة.

### <a name="common-data-service-entity-support-for-custom-fields"></a>دعم كيان Common Data Service للحقول المخصصة

في إصدار الأسبوع هذا، تدعم الكيانات التالية الآن الحقول المخصصة: التوظيف ونوع الميزة ودورة الدفع.

### <a name="an-error-occurs-when-an-off-boarding-checklist-is-assigned-299877"></a>يحدث خطأ عند تعيين قائمة اختيار إلغاء الإعداد (299877)

يعمل هذا التغيير على تصحيح رسالة خطأ تظهر عند تعيين قائمة اختيار الخروج من الإعداد إلى أحد الموظفين خارج عملية الإنهاء.

### <a name="the-exited-workers-link-opens-the-wrong-worker-309939"></a>يفتح ارتباط العاملين المغادرين العامل الخاطئ (309939)

يعمل هذا التغيير على تصحيح مشكلة تحدث عندما تقوم بإعادة تعيين موظف من كيان قانوني آخر وتحاول الانتقال إلى الموظف من قائمة العمال المغادرين.

### <a name="the-employee-self-service-compensation-card-doesnt-show-summary-values-when-advanced-security-is-turned-on-315231"></a>لا تعرض بطاقة تعويضات الخدمة الذاتية للموظف القيم الملخصة عند تشغيل الأمان المتقدم (315231)

يعمل هذا التغيير على تصحيح مشكلة تحدث عند استخدام أمان التعويض المتقدم. عند تشغيل الأمان المتقدم، تُظهر الآن الخدمة الذاتية للموظف مبالغ التعويض الملخصة لكل من الموظفين والمديرين. قبل اجراء هذا التغيير، تظهر القيم الملخصة كصفر (0).

### <a name="if-a-position-without-a-title-is-created-in-common-data-service-no-position-is-created-in-talent-314562"></a>إذا تم إنشاء منصب بدون مسمى وظيفي في Common Data Service، فلن يتم إنشاء منصب في Talent (314562)

تصحح تغييرات هذا الأسبوع مشكلة تحدث عند إنشاء مناصب في Common Data Service ولكنها لا توفر مسمى وظيفيًا.

### <a name="error-message-in-performance-journal-entries-in-employee-self-service-314134"></a>رسالة خطأ في إدخالات دفتر يومية الأداء في الخدمة الذاتية للموظف (314134)

يعمل هذا التغيير على تصحيح مشكلة تحدث عند إرفاق أهداف الأداء بإدخالات دفتر يومية الأداء في الخدمة الذاتية للموظف.

## <a name="in-preview"></a>قيد المعاينة

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>السماح بتعيين أكواد الأسباب على أنواع الإجازات

قد تحتاج المؤسسات إلى معلومات إضافية حول طلبات الإجازات. يمكنك الآن تحديد أكواد الأسباب لأنواع الإجازات وتمكين الموظفين من تحديد كود سبب في طلبات الإجازات.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>المطالبة بأكواد الأسباب لأنواع إجازات معينة على طلبات الإجازة

قد تطالب المؤسسات بتعيين أكواد الأسباب لأنواع إجازات معينة عند قيام الموظفين بتقديم طلبات إجازة. قد يكون هذا الشرط موجودًا بسبب سياسة الشركة أو المتطلبات التنظيمية. يمكنك الآن تعيين أنواع الإجازات التي تحتاج إلى كود سبب، ويمكنك مطالبة الموظفين بتوفير كود سبب لنوع الإجازة في طلبات الإجازة.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>توفير قائمة حركات الغياب والإجازة لقسم الموارد البشرية

تؤدي القدرة على تعقب وقت إجازات الموظفين وفهم كيفية احتساب الإجازات ليس فقط إلى مساعدة قسم الموارد البشرية على الرد على استفسارات الموظفين ولكنها تضمن أيضًا منح مكافآت إجازات دقيقة للموظفين. تتوفر لدى قسم الموارد البشرية الآن طريقة عرض جديدة للحركات (المُنح والاستحقاقات والتسويات والطلبات) لتمكين موظفي الموارد البشرية من الاطلاع على الأسباب التي تكمن خلف الأرصدة.

## <a name="coming-soon"></a>قريبًا

### <a name="email-support-for-alerts"></a>دعم البريد الإلكتروني للتنبيهات

في تحديث النظام الأساسي 26 لـ Finance and Operations، بإمكان المستخدمين إنشاء قواعد تنبيه ترسل بشكل تلقائي إعلامات بالبريد الإلكتروني إلى جهات الاتصال عند تشغيل الإعلامات بواسطة حدث.


[!INCLUDE[footer-include](../includes/footer-banner.md)]