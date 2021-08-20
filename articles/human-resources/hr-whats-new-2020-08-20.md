---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources (20 أغسطس 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 20 أغسطس 2020.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 32535c1f93990306ffaa0a5d97b48d3e6fdda7d014ceeeb2552960cd08b4be6c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775833"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources (20 أغسطس 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.3478. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم المرجع في  Lifecycle Services (LCS).

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a>إظهار معلومات إجازات الغياب القادمة والمعلقة إلى البطاقات في مساحة عمل الأشخاص

تتوفر الآن خيارات طلبات الإجازات المعلقة والقادمة في بطاقات الإجازة والغياب في مساحة عمل **الأشخاص**.

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a>لا يُعين الحقل الخاص إلى نعم بشكل افتراضي لدور الموظف في الخدمة الذاتية للموظف (477106)

يتم الآن تعيين حقل **خاص** افتراضيًا إلى **نعم** عندما يقوم الموظفين بإضافة سجلات عناوين جديدة من خلال صفحة **المعلومات الشخصية** في الخدمة الذاتية للموظف. 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a>تعرض علامة التبويب السريعة المرشحين المُراد توظيفهم في إدارة العاملين عدد غير صحيح من المرشحين (470110) 

تعرض الآن صفحة **إدارة العاملين** عدد المرشحين المراد توظيفهم بدقة. 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a>لا يُمكن إدخال إجازات مرضية لموظف تم إنهاء خدمته عند تعيين الاستحقاق إلى صفر (446195)

يُسمح الآن بحركات الإجازات للموظفين الذين تم إنهاء خدمتهم في المستقبل وتم تعيين الاستحقاق إلى صفر. يُمكن إدخال حركات الإجازات حتى تاريخ إنهاء الموظف. 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a>تؤدي إضافة حقول مخصصة إلى نموذج عامل جديد إلى تعطيل الحقول الموجودة في جزء الإجراءات لإدارة الإجازة (473314)

لن يتم تعطيل خيارات جزء الإجراء في نموذج **العامل** الجديد في **إدارة الإجازة** إذا تمت إضافة حقول مخصصة إلى نموذج **العامل** الجديد.

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a>يسمح جعل حقل التعليق على الإجازة إلزامي بإرسال طلب الإجازة عند عدم إدخال أي تعليق (473543)

يُمكن أن تكون حقول التعليقات إلزامية الآن، وتراعي طلبات الإجازة هذا الإعداد. الحقول الإلزامية هي ميزة للمعاينة.

### <a name="dmf-entity-available-for-accrual-suspensions"></a>يتوفر كيان DMF لتعليقات الاستحقاق

يتوفر كيان DMF الآن لتعليقات الاستحقاق.

## <a name="in-preview"></a>قيد المعاينة

### <a name="mandatory-fields"></a>حقول إلزامية

يمكنك جعل الحقول إلزامية باستخدام إمكانيات التخصيص في Human Resources. تتطلب هذه الميزة **طرق عرض محفوظة**. لمزيد من المعلومات حول طرق العرض المحفوظة، راجع:

- [طرق العرض المحفوظة - التوفر العام](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬
- [إنشاء نماذج تستخدم طرق العرض المحفوظة بشكل كامل](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>تطبيق Human Resources في Teams

بإمكان الموظفين عرض وطلب الوقت بعيدًا عن العمل ضمن Microsoft Teams يمكنهم التفاعل مع روبوت لإنشاء طلبات الإجازات. لمزيد من المعلومات، راجع:

- [تجربة إجازة وغياب الموظف في Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬
- [تطبيق Human Resources في Teams](./hr-admin-teams-leave-app.md)

## <a name="coming-soon"></a>قريبًا

### <a name="human-resources-app-in-teams-preview-features"></a>تطبيق Human Resources في ميزات المعاينة لـ Teams
 
-  **الإخطارات**: سوف يتم إعلام المُرسلين والمعتمدين لطلبات الإجازات في تطبيق Human Resources في Teams. سوف يتمكن المعتمدون من اعتماد طلبات الإجازة أو رفضها، وسوف يتم إخطار المرسلون إذا تم اعتماد الطلب أو رفضه.
 
- **تقويم إجازة المُدير**: سوف يتمكن المديرون من رؤية الإجازات المعتمدة والمعلقة لتقاريرهم المباشرة في طريقة عرض التقويم. توفر طريقة العرض هذه طريقة سهلة في الفهم عند انقطاع أعضاء فريقهم عن العمل.

### <a name="checklist-entities-included-in-dataverse"></a>تضمين كيانات قائمة الاختيار في Dataverse

ستتوفر كيانات قائمة الاختيار لعمليات الإلحاق وإلغاء الإلحاق والتحويلات وعمليات الأعمال قريبًا في Dataverse.

## <a name="known-issues"></a>مشكلات معروفة

قد تعرض مساحة عمل **إدارة الميزات** ميزات معطلة كميزات معاينة عندما تكون متوفرة بشكل عام. فيما يلي قائمة بالميزات المتوفرة بشكل عام والتي تعرض حالة غير صحيحة. 

- إدارة المزايا
- إدارة الحالة
- تسجيل قاعدة البيانات (تدقيق)
- استحقاق الإجازة لشركة واحدة أو خطة واحدة
- تعليق استحقاق الإجازة والغياب
- كود سبب تسوية الرصيد والتعليق
- شراء الإجازة وبيعها
- تقويم الإجازة والغياب
- قواعد الرصيد المحول للإجازة
- تدقيق استحقاق الإجازة
- حذف استحقاقات الإجازة
- تقريب استحقاق الإجازة‬
- تكوين أنواع إجازات متعددة في خطة إجازة واحدة
- تحسينات تحديث تفاصيل الإجازات
- استخدام تكافؤ الدوام الكامل‬ للموظف للاستحقاقات‬
- طريقة عرض التعويض الثابت عبر الشركة
- طباعة مراجعات الأداء
- تصحيحات العطلات في استحقاق الإجازة

### <a name="benefit-plan-employee-entity"></a>كيان الموظف في خطة الميزة 

اكتشفنا مؤخرًا مشكلتين بخصوص كيان **BenefitsPlanEmployee**.  عند استيراد سجلات العامل، يتم تعيين **كود التغطية** و **كود نوع الخطة** بشكل غير صحيح. تؤدي هذه المشكلة إلى عرض خطط مزايا الموظف بشكل غير صحيح في نموذج **خطة ميزات العامل** وفي نموذج **تسجيل مفتوح** في الخدمة الذاتية للموظف. قد تؤثر هذه المشكلة أيضًا على قدرة الموظف على تحديد الخطط في الخدمة الذاتية للموظف. لا يوجد حل حاليًا. نُعامل هذه المسألة على أنه إصلاح ذو أولوية عالية وسوف نقوم بحل هذه المشكلة في إصدارنا القادم.

## <a name="see-also"></a>راجع أيضًا

[الجديد أو المتغير في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]