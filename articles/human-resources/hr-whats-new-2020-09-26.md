---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources 26 سبتمبر، 2020
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 26 سبتمبر 2020.
author: jcart1106
ms.date: 09/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cc730bca25293e7dbc78d72834dc8abf9b2a1ec4
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892671"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-26-2020"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources 26 سبتمبر، 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة أو على وشك القدوم في Dynamics 365 Human Resources. لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2020، الموجة 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.3589-hf.3.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزة التالية بشكل عام مع هذا الإصدار:

- **تحديث النظام الأساسي 10.0.13 متوفر الآن**: لمزيد من المعلومات عن التحديث، راجع [تحديثات النظام الأساسي للإصدار 10.0.13 لتطبيقات Finance and Operations (أكتوبر، 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-13.md).

### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. قد تكون هناك تحديثات لهذا الموضوع لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذا الموضوع في البداية.

| رقم الإصدار | إصدار | الوصف |
| --- | --- | --- |
| 469495 | تحديث شبكة الأبعاد المالية الافتراضية ومربع الحوار | يتم تحديث شبكة الأبعاد المالية الافتراضية ومربع الحوار في Human Resources. |
| 474887 | يفتح عنصر عمل طلب إجازة ارتباط خاطئ في قرار يدوي | عندما يحتوي تكوين سير العمل على قرار يدوي، فإن الانتقال إلى طلب الإجازة من **عناصر العمل المعينة إليّ** يفتح الارتباط الخطأ، ويظهر إما نموذج فارغ أو طلب إجازة تم إنشاؤه بواسطة المستخدم الحالي بدلاً من النموذج المعين له للقرار اليدوي. |
| 474962 | يحتوي كيان معلمات الإجازة والغياب على حقول ذات تسميات مبهمة | يتم تحديث تسميات كيانات الإجازة والغياب بحيث تكون واضحة. |
| 481401 | يتم تعليق معالجة الاستحقاق عندما يكون أساس تاريخ الاستحقاق بعد تاريخ بدء الاستحقاق وفي نهاية الشهر | يتم تحديث معالجة الاستحقاق بحيث لا يكون بها تأخير عندما يكون أساس تاريخ الاستحقاق بعد تاريخ بدء الاستحقاق وفي نهاية الشهر. |
| 447167 | تتضمن قوائم السجلات منتهية الصلاحية العاملين غير النشطين | تضم علامة التبويب **السجلات منتهية الصلاحية** في **إدارة العاملين** العاملين غير النشطين. والآن تحتوي على العاملين النشطين فقط. |
| 486840 | يتم فتح طلب إجازة أو غياب خاطئ من **‏‫عناصر عمل تم تعيينها إلي‬** | يعمل تحديد طلب إجازة بغياب من **عناصر العمل المعينة إليّ** على عدم فتح أحدث طلب إجازة بغياب تم تعيينه للمستخدم الحالي. |
| 506868 | Dataverse الحقل **العنوان** لم يتم تعيينه للكيان **منصب الوظيفة**. | لا يُعرض الحقل **العنوان** في الكيانات **الوظيفة** و **منصب الوظيفة** على أنه غير محدد. يتم الآن عرض الحقل **العنوان**. |
| 430359 | يتعذر الوصول إلى مهام قائمة اختيار إلغاء الإعداد باستخدام أدوار المدير والموظف المعينة | يتعذر على العاملين الذين لديهم تاريخ إنهاء مستقبلي الوصول إلى مهام قوائم الاختيار الخاصة بهم إذا كان لديهم دور "موظف" أو "مدير" فقط. يمكن الآن للمستخدمين الذين لديهم دور "موظف" أو "مدير" الوصول إلى مهام إلغاء الإعداد بتاريخ إنهاء مستقبلي. |
| 458102 | لا يظهر الموظف الجديد على الكيان **معلومات كشف رواتب العاملين** عندما تم إنشاؤه | يتم تضمين الموظفين الجدد في الكيان "معلومات كشف الرواتب للعامل" دون الحاجة إلى فتح معلومات كشف الرواتب للموظف قبل تصدير الكيان. |

## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| تطبيق Human Resources في Microsoft Teams | [تجربة إجازة وغياب الموظف في Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [تطبيق Human Resources في Teams](./hr-admin-teams-leave-app.md)<br>[إدارة طلبات الإجازة في Teams](hr-teams-leave-app.md) |
| طلبات سير العمل المحسنة والموافقات | [تحسينات تجربة سير العمل للمؤسسة وإدارة العاملين](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [خيار التكوين لقائمة وضع عناصر العمل المعينة لي](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |

## <a name="coming-soon"></a>قريبًا

يتم جدولة الميزة الجديدة التالية لإصدار مستقبلي:

- [الارتباطات المخصصة في الخدمة الذاتية للمدير](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service)

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2019، الموجة 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>الموارد الإضافية

[ما الجديد في Human Resources](hr-admin-whats-new.md)
[نظرة عامة على Dynamics 365 Human Resources الإصدار 2020، الموجة 2 wave 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)
[عملية التحديث](hr-admin-setup-update-process.md)
[إدارة الميزات](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]