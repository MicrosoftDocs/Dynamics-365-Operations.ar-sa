---
title: ما الجديد والمتغير في Dynamics 365 Human Resources  26 يوليو 2021
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 26 يوليو 2021.
author: marcelbf
ms.date: 07/12/2021
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
ms.search.validFrom: 2021-07-26
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 810511c42cd690579d8c8b6ebcc17b0cf7fcb9eb2b999822dc2226fabd127cc6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771505"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-26-2021"></a>ما الجديد والمتغير في Dynamics 365 Human Resources  26 يوليو 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة أو على وشك القدوم في Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.4384.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزات التالية بشكل عام مع هذا الإصدار.

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| update 10.0.20 للنظام الأساسي | -- | [تحديثات النظام الأساسي للإصدار 10.0.20 من تطبيقات Finance and Operations (أغسطس 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20) |

### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. قد نقوم بتحديث هذا الموضوع لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذا الموضوع في البداية.

| رقم الإصدار | المشكلة |  الوصف |
| --- | --- | --- |
| 600422 | فشل التحقق من صحة عنوان الرواتب لـ Ready to Pay. | تم تحديث التحقق من الصحة لطلب عنوان واحد فقط من نوع "موقع الإقامة في الرواتب" وعنوان واحد فقط من نوع "موقع عمل الرواتب". |
| 601226 | مشكلة تكامل البيانات: مشروع تصدير تكامل الرواتب ليس لديه خيار الدفع الكامل | كان تكامل الرواتب إلى Ceridian DayForce يقوم بدفعة تدريجية بدلا من دفعة كاملة. Ceridian يتطلب أن يكون دائما تحديث كامل. هذه المشكلة الآن ثابتة، الكيانات في مشروع تصدير البيانات لن يتم الآن انعكاس دفعة تزايدية. |
| 602272 | الإطارات المتجانبة التي تمت إضافتها إلى مساحة عمل الخدمة الذاتية للموظف مفقودة الآن، ولم يعد من الممكن إضافة التجانبات إليها | لقد قمنا بإصلاح مشكلة التخصيص للخدمة الذاتية للموظف. يمكن إضافة مربعات جديدة إلى طريقة العرض وسيكون أي تخصيص موجود مرئيا للمستخدمين |
| 600711 | حقل تحديد تعريف لمدة نصف يوم ممكن لطلبات إجازة اليوم الكامل | تم إصلاح هذه المشكلة الآن وسيتم تمكين حقل تعريف نصف يوم فقط عندما يحدد الموظفون نوع إجازة مع تمكين تعريف نصف يوم ونصف يوم كقيمة المبلغ المحدد |
| 602208 | وحدات معدل الاستحقاق التي تعرض الساعات بدلا من الأيام | تم إصلاح هذه المشكلة الآن. سيظهر نموذج **إيقاف الوقت** وحدة الإجازة الصحيحة (الساعات أو الأيام) لعمود **معدل الاستحقاق**. |

## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| مساحة عمل إدارة المزايا | [مساحة عمل إدارة المزايا (معاينة)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [مساحة عمل إدارة المزايا](hr-benefits-management-workspace.md) |
| تمكين تكامل كشوف المرتبات المبسط (واجهات برمجة تطبيقات تكامل الرواتب) | [تمكين التكامل المبسط مع موفري كشوف المرتبات](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [‏‫واجهة برمجة التطبيقات لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)|
|  تمكين مدير الغياب لإدارة الإجازة | [تمكين مدير الغياب لإدارة الإجازة](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | مع هذا الإصدار، نحن نقوم بتحديث طريقة عرض مساحة عمل مدير الغياب. لمزيد من المعلومات، راجع [تكوين دور إدارة الغياب](https://go.microsoft.com/fwlink/?linkid=2168107).|
|  تكوين متطلبات المرفق لكل نوع إجازة | [تكوين متطلبات المرفق لكل نوع إجازة](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[تكوين أنواع الإجازة والغياب](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  تكوين وحدات الإجازات لكل نوع إجازة | [تكوين وحدات الإجازات لكل نوع إجازة](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[تكوين أنواع الإجازة والغياب](https://go.microsoft.com/fwlink/?linkid=2168215)|
| تمكين وضع علامة جاهز للدفع للموظفين | [تمكين وضع علامة جاهز للدفع للموظفين](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [جاهز للدفع](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>قريبًا

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>راجع أيضًا

[الميزات ‏‫الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
