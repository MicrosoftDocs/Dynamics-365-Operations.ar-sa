---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources 6 سبتمبر، 2021
description: توضح هذه المقالة الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 6 سبتمبر 2021.
author: marcelbf
ms.date: 09/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 03f832a6a3a099c472b781f7e2258ac575127101
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069989"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-6-2021"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources 6 سبتمبر، 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة الميزات الجديدة أو المتغيرة أو الصادرة قريبًا في Microsoft Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.4443.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزات التالية بشكل عام مع هذا الإصدار.

| الميزة | خطة الإصدار | الوثائق |
|---|---|---|
| تمكين مدير الغياب لإدارة الإجازة | [تمكين مدير الغياب لإدارة الإجازة](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | في هذا الإصدار، نحن نقوم بتحديث طريقة عرض مساحة عمل مدير الغياب. لمزيد من المعلومات، راجع [تكوين دور إدارة الغياب](https://go.microsoft.com/fwlink/?linkid=2168107). |
| تكوين متطلبات المرفق لكل نوع إجازة | [تكوين متطلبات المرفق لكل نوع إجازة](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) | [تكوين أنواع الإجازة والغياب](https://go.microsoft.com/fwlink/?linkid=2168108) |
| تكوين وحدات الإجازات لكل نوع إجازة | [تكوين وحدات الإجازات لكل نوع إجازة](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) | [تكوين أنواع الإجازة والغياب](https://go.microsoft.com/fwlink/?linkid=2168215) |

### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. يمكن أن نقوم بتحديث هذه المقالة لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذه المقالة بشكل مبدئي.

| رقم الإصدار | المشكلة | ‏‏الوصف‬ |
|---|---|---|
| 610128 | خطا في نشر البيانات عند استخدام HcmDiscussionOverallCommentEntity | عند نشر البيانات من مصنف Excel إلى كيان HcmDiscussionOverralCommentEntity، يحدث الخطأ التالي: "لا يمكن تحديد موقع سجل مصدر البيانات من النوع HcmTopicOverrall." |
| 589073 | يبلغ التقرير EEO-1 عن قيم "غير محددة" وقيم فارغة لحقل **الجنس** كالقيمة "أنثى". | إذا لم يتم تحديد **ذكر** لحقل **الجنس**، فسينشئ التقرير EEO-1 قيمة افتراضية **أنثى**. |
| 589617 | رصيد بطاقة الإجازة، لا تظهر الأرصدة المتوفرة للشراء والأرصدة المتوفرة للبيع عندما تكون أدوار المستخدم مقيدة لكيان قانوني معين. | إذا تم تقييد المستخدم (دور الموظف) بكيان قانوني محدد، فلن تظهر الأرصدة بشكل صحيح في **أرصدة الإجازة** وفي الحقلين **متوفرة للبيع** و **متوفرة للشراء**. |
| 604310 | يجب أن تكون علامة التبويب "مدير الغياب" مخفية عند عدم وجود تدرج هرمي معين للمستخدم. | بالنسبة لكيان قانوني محدد، يجب أن تكون علامة التبويب **مدير الغياب** مخفية في مدخل الخدمة الذاتية الا إذا كانت المعلمة عبر الشركة ممكّنة وهناك تدرج هرمي واحد على الأقل للغياب مرتبط بالمستخدم. |

## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول كيفية تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
|---|---|---|
| تمكين تكامل كشوف المرتبات المبسط (واجهات برمجة تطبيقات تكامل الرواتب) | [تمكين التكامل المبسط مع موفري كشوف المرتبات](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [‏‫واجهة برمجة التطبيقات لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md) |
| مساحة عمل إدارة المزايا | [مساحة عمل إدارة المزايا (معاينة)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [مساحة عمل إدارة المزايا](hr-benefits-management-workspace.md) |
| تمكين وضع علامة جاهز للدفع للموظفين | [تمكين وضع علامة جاهز للدفع للموظفين](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [جاهز للدفع](/dynamics365/human-resources/hr-compensation-payroll) |
| الحقول المخصصة في الأهلية |[دعم الحقول المخصصة في معالجة الأهلية](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [استخدام الحقول المخصصة في معالجة الأهلية](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |

## <a name="coming-soon"></a>قريبًا

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| الميزة | تفاصيل |
|---|---|
| Platform update 10.0.21 (45) | من المقرر أن يبدأ طرح تحديث النظام الأساسي 10.0.21 مع إصدار الخدمة في 4 أكتوبر 2021. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.21 من تطبيقات التمويل والعمليات (أكتوبر 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
| بيان المزايا | بيان المزايا لعرض اختيارات المزايا الحالية للموظف. لمزيد من المعلومات، راجع [بيان المزايا](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) في مستند موجة الإصدار |

## <a name="see-also"></a>راجع أيضًا

[الميزات ‏‫الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

