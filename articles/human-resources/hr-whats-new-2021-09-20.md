---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources 20 سبتمبر، 2021
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 20 سبتمبر 2021.
author: marcelbf
ms.date: 09/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a3fd8705c7735cb3c0945f71651fafa767a7addf
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691571"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-20-2021"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources 20 سبتمبر، 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة أو على وشك القدوم في Microsoft Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.4464.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزات التالية بشكل عام مع هذا الإصدار.

| الميزة | خطة الإصدار | الوثائق |
|---|---|---|
| تمكين تكامل كشوف المرتبات المبسط (واجهات برمجة تطبيقات تكامل الرواتب) | [تمكين التكامل المبسط مع موفري كشوف المرتبات](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [‏‫واجهة برمجة التطبيقات لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md) |
| تمكين وضع علامة جاهز للدفع للموظفين | [تمكين وضع علامة جاهز للدفع للموظفين](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [جاهز للدفع](/dynamics365/human-resources/hr-compensation-payroll) |

### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. قد نقوم بتحديث هذا الموضوع لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذا الموضوع في البداية.

| رقم الإصدار | المشكلة | ‏‏الوصف |
|---|---|---|
| 619774 | لا تتم مزامنة تحرير وصف العنوان إلى Dataverse في الوقت الحقيقي. | عند تحرير وصف عنوان العامل، لا تتم مزامنة الوصف المحدث في الوقت الحقيقي في Dataverse. تم تحديث الاشتراك الموجود في جدول **موقع التجهيزات** لإرسال تحديث. |
| 614603| خطأ في صفحة **العامل** عندما لا تكون المعلمة **إجراءات العاملين** محددة. | عند توظيف عامل جديد أو الانتقال إلى صفحة **العامل**، يظهر الخطأ التالي" يجب تعبئة حقل **نوع اجراء العامل**"، حتى إذا كان الخيار **إجراءات العاملين** متوقفًا عن التشغيل. |
| 615367 | تعرض علامة التبويب **الإجازات الموافق عليها** تحذيرًا وتظهر بشكل غير صحيح. | إذا تم تعيين وحدة الإجازة إلى **الأيام** قبل تمكين الميزة **تكوين وحدات الإجازات لكل نوع إجازة‬**، تعرض علامة التبويب **الإجازات الموافق عليها‬‏‫** تحذيرًا غير صالح وأعمدة غير صحيحة. |


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
| صفحة **معلمات التقرير** في **خدمة الموظف الذاتية** لبيان المزايا غير صحيحة. | عند الانتقال إلى **بيان المزايا** في **خدمة الموظف الذاتية**، تعرض الصفحة **معلمات التقرير** علامتي التبويب السريعتين **السجلات المطلوب تضمينها‬** و **تشغيل في الخلفية**.  يجب إزالتها. |
| يتم عرض الفترات المغلقة والمستقبلية في صفحة **معلمات التقرير** لبيان المزايا. | عند الانتقال إلى صفحة وجهة **تقرير بيان المزايا**، بإمكان المستخدم تحديد فترات خطط المزايا المغلقة أو ذات تواريخ مستقبلية، مما يؤدي إلى صفحة فارغة. يجب أن تظهر فترة خطة المزايا الحالية فقط في القائمة. |
|خطأ عند إرسال تقرير بالبريد الإلكتروني باستخدام وجهة تقرير GER. | يمكن تعيين بيان المزايا لاستخدام معلمات البريد الإلكتروني داخل صفحة **وجهات تقرير GER**. عند إكمال إعداد التقرير وطباعته، سيتلقى المستخدم رسالة خطأ في التنسيق ولن يتم إرسال بيان المزايا.|


## <a name="coming-soon"></a>قريبًا

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| الميزة | تفاصيل |
|---|---|
| Platform update 10.0.21 (45) | من المقرر أن يبدأ طرح تحديث النظام الأساسي 10.0.21 مع إصدار الخدمة في 4 أكتوبر 2021. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.21 من تطبيقات التمويل والعمليات (أكتوبر 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
|طريقة عرض دفاتر يومية الأداء للمرؤوسين في الفريق الموسع | سيتم تمكين هذه الميزة بشكل افتراضي في عملية النشر التالية. |


## <a name="see-also"></a>راجع أيضًا

[الميزات ‏‫الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
