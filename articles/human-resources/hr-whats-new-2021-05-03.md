---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources 3‏ مايو، 2021
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 3 مايو 2021.
author: marcelbf
ms.date: 05/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 01ebd15e09e181a7ea0ec5bf70c8df731d2169c0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902849"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-3-2021"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources 3‏ مايو، 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة الميزات الجديدة أو المتغيرة أو التي ستصدر قريبًا في Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.4140.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزات التالية بشكل عام مع هذا الإصدار.

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| قم بإضافة شريط المعلومات عندما يتم إنشاء أحداث الحياة. | - | عند إنشاء حدث حياة، يعرض شريط المعلومات رسالة تشير إلى نوع حدث الحياة الذي تم إنشاؤه.

### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. يمكن أن نقوم بتحديث هذه المقالة لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذه المقالة مبدئيًا.

| رقم الإصدار | المشكلة |  ‏‏الوصف‬ |
| --- | --- | --- |
| 559312 |  لا يتم إظهار المستوى عند إنشاء خطة تعويض ثابتة لأحد الموظفين. |  عند وجود عدم تطابق في المنطقة الزمنية بين المنطقة الزمنية للمستخدم والمنطقة الزمنية للشركة، تعذر قراءة مستوى التعويض في المهمة. تم تحديث الاستعلام ليتم إحضاره استنادًا إلى وقت UTC. |
| 573676  | لا يمكن إضافة فترة جديدة في نموذج **خطة الميزات**. | تم تحديث النموذج بحيث يتم تمكين الزر **جديد** ضمن علامة التبويب السريعة **الفترة** في **خطط الميزات**. |

## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| مساحة عمل إدارة المزايا | [مساحة عمل إدارة المزايا (معاينة)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [مساحة عمل إدارة المزايا](hr-benefits-management-workspace.md) |
| تحسينات تجربة سير العمل للإجازة والغياب | [تحسينات تجربة سير العمل للإجازة والغياب](https://go.microsoft.com/fwlink/?linkid=2147528) | [طلب إجازة](hr-employee-self-service-request-time-off.md)|
| تمكين تكامل كشوف المرتبات المبسط (واجهات برمجة تطبيقات تكامل الرواتب) | [تمكين التكامل المبسط مع موفري كشوف المرتبات](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [‏‫واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)|
| تدقيق حركة استحقاقات الإجازة | - | [تدقيق حركة استحقاقات الإجازة](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>قريبًا

| الميزة | تفاصيل |
| --- | --- |
| Platform update 10.0.18 (42) | تمت جدولة تحديث النظام الأساسي 10.0.18 بحيث يبدأ نشره مع إصدار الخدمة في 17 مايو 2021. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.18 من تطبيقات التمويل والعمليات (مايو 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| دعم الحقول المخصصة في قواعد الأهلية لإدارة الميزات  | [دعم الحقول المخصصة لمعالجة الأهلية](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>راجع أيضًا

[ما الجديد أو المتغير في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 1 من إصدار Dynamics 365 Human Resources  2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
