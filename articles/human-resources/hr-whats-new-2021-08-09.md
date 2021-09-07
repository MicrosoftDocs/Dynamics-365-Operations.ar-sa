---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources ‏9 أغسطس 2021
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 9 أغسطس 2021.
author: marcelbf
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0f515b614aedce3d58994bf21104ada25702a71e
ms.sourcegitcommit: fc19ee0aba2a6174fef305d151f1eb23ca6c0346
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/13/2021
ms.locfileid: "7385690"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-9-2021"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources ‏9 أغسطس 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة أو على وشك القدوم في Microsoft Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.4393.

### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. قد نقوم بتحديث هذا الموضوع لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذا الموضوع في البداية.

| رقم الإصدار | المشكلة | الوصف |
| --- | --- | --- |
| 558385 | لا يتم تحديد المصمم الافتراضي عند تشغيل خيار **مصممي التحديد التلقائي** للمصممين الافتراضيين. | تم إصلاح هذه المشكلة الآن. يتم تحديد العديد من التصميمات الافتراضية تلقائيًا في الخطط المؤهلة عند تشغيل **مصممي التحديد التلقائي** في صفحة **المعلمات المشتركة للموارد البشرية**. |
| 589617 | في صفحة **الإجازة**، تكون الأرصدة **المتوفرة للشراء** و **المتوفرة للبيع** فارغة عندما يقتصر الوصول على شركة معينة. | تم إصلاح هذه المشكلة الآن. تعرض صفحة **الإجازة** الأرصدة **المتوفرة للشراء** و **المتوفرة للبيع** الصحيحة عندما يقتصر الوصول على شركة معينة. |

## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول كيفية تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| مساحة عمل إدارة المزايا | [مساحة عمل إدارة المزايا (معاينة)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [مساحة عمل إدارة المزايا](hr-benefits-management-workspace.md) |
| تمكين تكامل كشوف المرتبات المبسط (واجهات برمجة تطبيقات تكامل الرواتب) | [تمكين التكامل المبسط مع موفري كشوف المرتبات](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [‏‫واجهة برمجة التطبيقات لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)|
| تمكين مدير الغياب لإدارة الإجازة | [تمكين مدير الغياب لإدارة الإجازة](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | في هذا الإصدار، نحن نقوم بتحديث طريقة عرض مساحة عمل مدير الغياب. لمزيد من المعلومات، راجع [تكوين دور إدارة الغياب](https://go.microsoft.com/fwlink/?linkid=2168107). |
| تكوين متطلبات المرفق لكل نوع إجازة | [تكوين متطلبات المرفق لكل نوع إجازة](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[تكوين أنواع الإجازة والغياب](https://go.microsoft.com/fwlink/?linkid=2168108)|
| تكوين وحدات الإجازات لكل نوع إجازة | [تكوين وحدات الإجازات لكل نوع إجازة](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[تكوين أنواع الإجازة والغياب](https://go.microsoft.com/fwlink/?linkid=2168215)|
| تمكين وضع علامة جاهز للدفع للموظفين | [تمكين وضع علامة جاهز للدفع للموظفين](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [جاهز للدفع](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>قريبًا

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| الميزة | تفاصيل |
| --- | --- |
| Platform update 10.0.21 (45) | من المقرر أن يبدأ طرح تحديث النظام الأساسي 10.0.21 مع إصدار الخدمة في 4 أكتوبر 2021. لمزيد من المعلومات، راجع [تحديثات النظام الأساسي للإصدار 10.0.21 من تطبيقات Finance and Operations (أكتوبر 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>راجع أيضًا

[الميزات ‏‫الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
