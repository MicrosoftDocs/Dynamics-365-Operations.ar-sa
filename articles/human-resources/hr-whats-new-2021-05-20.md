---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources 20‏ مايو، 2021
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 20 مايو 2021.
author: marcelbf
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dc7e89fabe1651c858097a6c564b4910a524331f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692740"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-20-2021"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources 20‏ مايو، 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة أو على وشك القدوم في Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.4189.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزات التالية بشكل عام مع هذا الإصدار.

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| Platform update 10.0.18 (42) | -- | [تحديثات النظام الأساسي للإصدار 10.0.18 من تطبيقات التمويل والعمليات (مايو 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| يدعم تطبيق الموارد البشرية لـ Microsoft Teams الآن تعريفات نصف اليوم وقدرة تقسيم اليوم | -- | [إدارة طلبات الإجازة في Teams](/dynamics365/human-resources/hr-teams-leave-app#create-a-new-request) |

### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. قد نقوم بتحديث هذا الموضوع لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذا الموضوع في البداية.

| رقم الإصدار | المشكلة |  الوصف |
| --- | --- | --- |
| 583776 | تتسبب عمليات التسجيل الجماعي للموظفين بخطط الإجازة في حدوث خطأ سجل مكرر | تم إصلاح هذا الخطأ بالإصدار الأحدث ويجب معالجة عمليات تسجيل خطط الإجازات الشاملة بنجاح. |
| 582263 | يتعذر تشغيل معالجة حدث الحياة لكافة العاملين في الوقت نفسه | عند ترك الحقل **العامل** فارغًا لمعالجة أحداث الحياة، ستتم معالجة كافة العاملين. |
| 558383 | لا يتم وضع علامة على المستفيد الرئيسي بأنه 100% في حالة عدم تحديد المعني الافتراضي | تم إصلاح الخطأ بحيث يحتاج المستخدم فقط إلى تحديد تبديل المستفيد الرئيسي.|
| 509404 | لا تأخذ تحليلات عدد موظفي القسم حركة الموظفين بين الأقسام في الاعتبار |تم تحديث التحليلات لتضمين عمليات نقل الموظفين بين الأقسام|
| 579420 | يجب عدم توفر ميزة تجميد الأعمدة في الشبكات بعد | تم إدارج الميزة **تجميد الأعمدة في الشبكات**، والتي لا تتوفر في الموارد البشرية، كمتوفرة في إدارة الميزات. تمت إزالة الميزة من قائمة الميزات التي سيتم تمكينها. |

## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| دعم الحقول المخصصة في قواعد الأهلية لإدارة الميزات | [دعم الحقول المخصصة لمعالجة الأهلية](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[تكوين قواعد الأهلية](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| مساحة عمل إدارة المزايا | [مساحة عمل إدارة المزايا (معاينة)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [مساحة عمل إدارة المزايا](hr-benefits-management-workspace.md) |
| تحسينات تجربة سير العمل للإجازة والغياب | [تحسينات تجربة سير العمل للإجازة والغياب](https://go.microsoft.com/fwlink/?linkid=2147528) | [طلب إجازة](hr-employee-self-service-request-time-off.md)|
| تمكين تكامل كشوف المرتبات المبسط (واجهات برمجة تطبيقات تكامل الرواتب) | [تمكين التكامل المبسط مع موفري كشوف المرتبات](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [‏‫واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)|
| تدقيق حركة استحقاقات الإجازة | - | [تدقيق حركة استحقاقات الإجازة](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>قريبًا

| الميزة | تفاصيل |
| --- | --- |
|  تمكين مدير الغياب لإدارة الإجازة | [تمكين مدير الغياب لإدارة الإجازة](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>راجع أيضًا

[ما الجديد أو المتغير في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 1 من إصدار Dynamics 365 Human Resources  2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
