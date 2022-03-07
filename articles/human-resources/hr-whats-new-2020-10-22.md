---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources 22 أكتوبر 2020
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 22 أكتوبر، 2020.
author: jcart1106
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 84bcf2ce850de95186c1ffee3bdd152255fc0d5c2832e47ea61918d240bcb1c6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772630"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources 22 أكتوبر 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة أو على وشك القدوم في Dynamics 365 Human Resources. لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2020، الموجة 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.3680.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزات التالية بشكل عام مع هذا الإصدار.

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| تحديث النظام الأساسي 10.0.14 (38) | -- | [تحديثات النظام الأساسي للإصدار 10.0.14 من تطبيقات Finance and Operations (نوفمبر 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14.md) |
| تحسينات تجربة عمليات سير العمل للمؤسسة وإدارة العاملين | [تحسينات تجربة سير العمل للمؤسسة وإدارة العاملين](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [خيار التكوين لقائمة وضع عناصر العمل المعينة لي](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. قد نقوم بتحديث هذا الموضوع لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذا الموضوع في البداية.

| رقم الإصدار| إصدار  | الوصف|
| --- | --- | --- |
| 437922 | يؤدي استيراد ساعات FMLA باستخدام كيان DMF إلى حدوث خطأ للقراءة فقط. | فشل استخدام ساعات FMLA لاستيراد الساعات المقترنة بحالة FMLA. أضفنا منطقًا للتأكد من أن الساعات المستوردة لا تتجاوز الساعات المتبقية للحالة. |
| 512019 | مبلغ **الرصيد المحول الأخير** غير صحيح. | في الصفحة **الإجازة**، عرض تغيير **اعتبارًا من** إلى اليوم الأول من الفترة المالية التالية مبلغ **الرصيد المحول الأخير** غير صحيح لنوع **الإجازة السنوية**. يعرض الآن المبلغ الصحيح. |
| 458639 | لا يدعم الكيان **جهات اتصال العامل** وضع تعقب التغييرات. | قمنا بتحديث الكيان **جهات اتصال العامل** بحيث يمكنك استخدامها في سيناريوهات ميزة ‏‫إحضار قاعدة بياناتك الخاصة‬ (BYOD).|
| 505347 | يمكن لمديري التدريب إرسال طلب إجازة لموظف عند تمكين ميزة العامل المبسط. | لا يُسمح لأدوار غير مساعد الموارد البشرية و مدير الموارد البشرية بإرسال طلبات الإجازات للموظفين. |
| 513490 | تسجيل إدارة الميزات: إضافة تسجيل لخطط بدون خيارات تغطية. | تم تمكين نتائج التسجيل لـ **خطة بدون خيارات تغطية**. ويتم عرضها الآن في جدول **نتائج العملية** ويتم فرزها بشكل صحيح لعرضها في الأعلى. |
| 517021 | لا يمكن تحديد خطط متعددة بنفس كود **نوع الخطة** إذا كان **نوع الخطة** يحتوي على تسجيل واحد لكل نوع. | تم تغيير القيود الخاصة بتحديد الخطط عند السماح بتسجيل واحد فقط. تتوفر القيود الآن على مستوى **كود نوع الخطة** بدلاً من **نوع الخطة**. يسمح هذا التغيير بالتخطيطات مثل HSA وFSA، والتي تكون من نفس النوع، ولكن يمكنك إعطاؤها **كود نوع خطة** منفصل. وبهذه الطريقة، يمكنك تحديد كليهما لفترة التسجيل نفسها. |
| 444791 | لا يمكن عرض التعويض في الخدمة الذاتية للموظف في حالة تشغيل **تقييد الوصول** في خطة التعويض. | في بطاقة **التعويض** للخدمة الذاتية للموظف، تم عرض مبلغ التعويض الحالي ونسبة الزيادة على أنه "0" إذا تم تسجيل الموظف في خطة مع تشغيل **تقييد الوصول** وتعيينه إلى أدوار معينة. تم حل هذه المشكلة لكي يتمكن الموظف والمدير دائمًا من رؤية تفاصيل التعويض لنفسه والتقارير المباشرة. |
| 457542 | لا يؤدي تحديث تفاصيل الدورة التدريبية بعد إغلاق الدورة التدريبية أيضًا إلى تحديث المعلومات نفسها الخاصة بالموظف الذي حضر الدورة التدريبية. | يتم الآن تحديث معلومات الموظف بشكل صحيح عندما تقوم بتغيير تفاصيل الدورة التدريبية بعد إغلاق دورة تدريبية وإعادة فتحها. |
| 515342 | يتعذر إدراج البيانات من خلال **CDSLeaveRequestDetailEntity**. لم يتم العثور على الشركة أو إنها غير موجودة. | يمكنك الآن استخدام **CDSLeaveRequestDetailEntity** لإدخال البيانات. |
| 514743 | خطأ في نموذج **معلمة البريد الإلكتروني** عند استخدام Microsoft Exchange. | تم عرض الرسالة "تعذر تحميل الملفات أو التجميع..." في الصفحة **معلمات البريد الإلكتروني** عند تعيين موفر البريد الإلكتروني إلى **Exchange**. كما يسمح هذا الإصلاح بتحميل الصفحة **معلمات البريد الإلكتروني** وحفظها كما هو متوقع. |


## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| تطبيق Human Resources في Microsoft Teams | [تجربة إجازة وغياب الموظف في Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [تطبيق Human Resources في Teams](./hr-admin-teams-leave-app.md)<br>[إدارة طلبات الإجازة في Teams](hr-teams-leave-app.md) |
| طلبات سير العمل المحسنة والموافقات | [تحسينات تجربة سير العمل للمؤسسة وإدارة العاملين](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [خيار التكوين لقائمة وضع عناصر العمل المعينة لي](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| الكيانات الظاهرية في Dataverse لـ Human Resources | [توسيع Dynamics 365 Human Resources البيانات الأساسية في Dataverse](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [تكوين كيانات Dataverse الظاهرية](hr-admin-integration-common-data-service-virtual-entities.md) |
| التكامل مع LinkedIn Talent Hub | [التكامل مع LinkedIn Talent Hub](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [التكامل مع LinkedIn Talent Hub](./hr-admin-integration-linkedin.md) |
| الارتباطات المخصصة في الخدمة الذاتية للمدير | [الارتباطات المخصصة في الخدمة الذاتية للمدير](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [الارتباطات المخصصة في الخدمة الذاتية للمدير](./hr-employee-manager-self-service-custom-links.md) |

## <a name="coming-soon"></a>قريبًا

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2020، الموجة 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="see-also"></a>راجع أيضًا

[الميزات الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2020](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]