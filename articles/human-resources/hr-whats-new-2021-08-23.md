---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources ‏23 أغسطس 2021
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 23 أغسطس 2021.
author: marcelbf
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 21c3448c373600ffebca82be41fb5849b952dfe1
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686816"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-23-2021"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources ‏23 أغسطس 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة أو على وشك القدوم في Microsoft Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.4419.

### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. قد نقوم بتحديث هذا الموضوع لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذا الموضوع في البداية.

| رقم الإصدار | المشكلة | الوصف |
| --- | --- | --- |
| 594066 | تعذر حذف معلومات جهة الاتصال | عند تحديد حذف سجل معلومات جهة اتصال لأحد الموظفين، يتم حذف سجل معلومات جهة الاتصال بخلاف السجل المحدد بدلاً من ذلك. |
| 611339 | تؤدي إضافة تخصيص إلى تجاهل الحساب البنكي لعامل التصفية وجلب السجل الأول | تؤدي إضافة التخصيص إلى قيام قائمة الحسابات البنكية بتشغيل استعلام تخصيص بعد تشغيل استعلام مصدر البيانات، مما يؤدي إلى قيام الاستعلام بجلب أعلى سجل بغض النظر عن العامل الجاري عرض التفاصيل الخاصة به. |
| 591806 | تم حساب مهام تاريخ استحقاق الإعداد بشكل غير صحيح | يتم حساب تواريخ الاستحقاق بشكل غير صحيح في حالة وجود الحالات التالية: قوائم الاختيار التي تم إنشاؤها تستخدم تقويمًا يستخدم نطاق زمني ممتد (على سبيل المثال، من 2005 إلى 2050) وتستخدم تفضيلات المستخدم منطقة زمنية خلاف التوقيت المركزي القياسي. |   
| 592749 | رصيد الإجازة غير صحيح في **الخدمة الذاتية للموظفين** | إذا كان للموظف توظيف في أكثر من كيان قانوني وتم تمكين طريقة العرض الإجازة بين الشركات الشقيقة، فقد يكون رصيد الإجازة غير صحيح. |
| 603133 | تحذير غير متوقع عند طلب إيقاف الوقت | عند طلب إيقاف الوقت، فإن ملء حقل **لنصف يوم** قبل حقل **المبلغ** سيتسبب في ظهور تحذير غير متوقع. |
| 606546 | تحديد حقل غير مرئي في زمن التوقف المعتمد | كانت خانة الاختيار لتحديد العديد من طلبات الإجازة المعتمدة غير مرئية. |
| 597059 | العامل غير مرئي في **تقويم الإجازة والغياب في الشركة** | العامل غير مرئي في **تقويم الإجازة والغياب في الشركة** إذا كان نطاق التاريخ الذي تم تطبيقه يتضمن أي يوم تم رفض طلب الإجازة له. |


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
| Platform update 10.0.21 (45) | من المقرر أن يبدأ طرح تحديث النظام الأساسي 10.0.21 مع إصدار الخدمة في 4 أكتوبر 2021. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.21 من تطبيقات التمويل والعمليات (أكتوبر 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>راجع أيضًا

[الميزات ‏‫الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
