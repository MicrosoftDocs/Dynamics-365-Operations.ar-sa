---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources 5 أكتوبر 2021
description: توفر هذه المقالة الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 5 أكتوبر 2021.
author: marcelbf
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cc8cd8616f1b82258fccbb2b41d5e72a90aaed63
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845101"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-5-2021"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources 5 أكتوبر 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة الميزات الجديدة أو المتغيرة أو الصادرة قريبًا في Microsoft Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.4485.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزات التالية بشكل عام مع هذا الإصدار.

| الميزة | خطة الإصدار | الوثائق |
|---|---|---|
| Platform update 10.0.21 (45) | -- | [تحديثات النظام الأساسي للإصدار 10.0.21 من تطبيقات التمويل والعمليات (أكتوبر 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) |


### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. يمكن أن نقوم بتحديث هذه المقالة لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذه المقالة بشكل مبدئي.

| رقم الإصدار | المشكلة | ‏‏الوصف‬ |
|---|---|---|
| 598896 | لا يتم عرض مبلغ الموظف الا بعد ان يقوم الموظف بإكمال التسجيل | في الصفحة **الخدمة الذاتية للموظف** ، لم يتم عرض مبلغ الموظف الخاص بالميزة. لا يتم عرض مبلغ الموظف الآن في الصفحة **الخدمة الذاتية للمنافع**.  |
| 613440 | يتعذر تصدير البيانات من **أداره البيانات** | عند تصدير بيانات لمشروع في **أداره البيانات** ، يفشل التصدير بشكل غير متوقع. |
| 618327 | يتم عرض الفترات المغلقة والمستقبلية في صفحة **معلمات التقارير** لبيان المزايا. | عند الانتقال إلى **بيان المزايا** في **خدمة الموظف الذاتية**، تعرض الصفحة **معلمات التقرير** علامتي التبويب السريعتين **السجلات المطلوب تضمينها‬** و **تشغيل في الخلفية**. تمت أزاله هذه المقاطع.|
| 618326 | تظهر صفحة **معلمات التقرير** غير صحيحة في **خدمة الموظف الذاتية** لبيان المزايا.| عند الانتقال إلى صفحة وجهة **تقرير بيان المزايا**، بإمكان المستخدم تحديد فترات خطط المزايا المغلقة أو ذات تواريخ مستقبلية، مما يؤدي إلى صفحة فارغة. يجب أن تظهر فترة خطة المزايا الحالية فقط في القائمة. |

## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول كيفية تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
|---|---|---|
| مساحة عمل إدارة المزايا | [مساحة عمل إدارة المزايا (معاينة)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [مساحة عمل إدارة المزايا](hr-benefits-management-workspace.md) |
| الحقول المخصصة في الأهلية |[دعم الحقول المخصصة في معالجة الأهلية](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [استخدام الحقول المخصصة في معالجة الأهلية](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| بيان المزايا |[بيان المزايا](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [بيان المزايا](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>المشكلات المعروفة لبيان المزايا

| المشكلة | ‏‏الوصف |
|---|---|
|خطأ عند إرسال تقرير بالبريد الإلكتروني باستخدام **وجهة تقرير GER** | يمكن تعيين بيان المزايا لاستخدام معلمات البريد الإلكتروني داخل صفحة **وجهات تقرير GER**. عند إكمال إعداد التقرير وطباعته، سيتلقى المستخدم رسالة خطأ في التنسيق ولن يتم إرسال بيان المزايا.|

## <a name="feature-management-changes"></a>تغييرات إدارة الميزات

| الميزة | ‏‏الوصف |
|---|---|
|طريقة عرض دفاتر يومية الأداء للمرؤوسين في الفريق الموسع | سيتم تمكين هذه الميزة بشكل افتراضي في عملية الإصدار التالية. |

## <a name="coming-soon"></a>قريبًا

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| الميزة | تفاصيل |
|---|---|
| Platform update 10.0.22 (46) | من المقرر أن يبدأ طرح تحديث النظام الأساسي 10.0.22 مع إصدار الخدمة في 1 نوفمبر 2021. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.22 من تطبيقات التمويل والعمليات (نوفمبر 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22). |



## <a name="see-also"></a>راجع أيضًا

[الميزات ‏‫الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
