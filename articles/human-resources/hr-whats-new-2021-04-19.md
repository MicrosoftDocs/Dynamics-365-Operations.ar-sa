---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources ‏(19 أبريل 2021)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 19 أبريل 2021.
author: marcelbf
ms.date: 04/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8968c9cb849901288d75cd5e539a57faf0045337
ms.sourcegitcommit: e24e335811727c4b12152323b2bcb25495c08c5b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/22/2021
ms.locfileid: "5934882"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-19-2021"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources ‏(19 أبريل 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة أو على وشك القدوم في Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.4113.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزات التالية بشكل عام مع هذا الإصدار.

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| Platform update 10.0.17 (41) | -- | [تحديثات النظام الأساسي للإصدار 10.0.17 من تطبيقات Finance and Operations (أبريل 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md) |
| دعم الحقول المخصصة في نماذج إدارة الميزات | [دعم الحقول المخصصة في إدارة الميزات](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management)| [نظرة عامة على إدارة المزايا](hr-benefits-management-overview.md)|

### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. قد نقوم بتحديث هذا الموضوع لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذا الموضوع في البداية.

| رقم الإصدار | إصدار |  الوصف |
| --- | --- | --- |
| 552164 | **طريقة العرض المحفوظة** في **الخدمة الذاتية للموظفين > فتح الدورات التدريبية** لا تعمل للدورات التدريبية التي تحتوي على جدول أعمال | إذا تم استخدام طريقة العرض المحفوظة في الدورات التدريبية المفتوحة (ESS)، وكانت إحدى الدورات التدريبية بها أجندة مرفقة بها، فلن تعرض طريقة العرض بعد ذلك سطورًا متعددة لتلك الدورة التدريبية |
| 560614 | تُظهر **الميزات > خيارات أحداث الحياة** الاختلافات في مستندات شريط الأدوات وسلوك التعليمات البرمجية. | تم تحديث تلميحات الأدوات في **خيارات أحداث الحياة** لإظهار السلوك الصحيح. |
| 560616 | يمكن تحرير **الميزات > خيارات أحداث الحياة** في خطة ميزات العمال، ولكن لا تتأثر بالتغييرات. | السلوك المحدث لمفاتيح تبديل خيار حدث الحياة للتمكين أو التعطيل، بناءً على الخيارات التابعة، لكل وثائق تلميح الأداة. |
| 565054 | يتعذر عرض محتوى قائمة **العمال بدون عمل** عند تشغيل **الوصول المتقدم**. | يعمل هذا الإصدار على إصلاح المشكلة حيث ومتى تم تشغيل **الوصول المتقدم**، يمكن لمسؤولي النظام فقط عرض محتويات قائمة **العمال بدون عمل**. نظرًا لأن هذا الإصلاح يعد تغييرًا أمنيًا، فستحتاج إلى الاشتراك فيه في إدارة الميزات. بمجرد تشغيل الميزة، سترى تلك الأدوار التي لديها حق الوصول إلى النموذج المحتويات، على الرغم من تشغيل الوصول المتقدم. لمزيد من المعلومات، راجع [العمال بدون عمل](hr-personnel-workers-without-employment.md). |
| 570586 | فشل التحقق من صحة طلب الإجازة عند انتهاء التوظيف قبل آخر معاملة لذلك العامل عبر جميع خطط الإجازة. | بعد انتهاء العمل، لا يفشل التحقق من صحة طلب الإجازة بناءً على معاملات إجازة الموظف.|
| 570783 | يؤدي تمكين وتعطيل الإجازة عبر الشركة في الموارد البشرية المشتركة المعلمات إلى تغيير ما يراه الموظفون العاملون في شركة واحدة في طلبات الإجازة. | لا يرى الموظفون العاملون في شركة واحدة أي تغييرات في طلب إجازة إذا تم تمكين المعلمة أو تعطيلها. |
| 572343 | لا يتم عرض كود السبب المطلوب عند تمكين ميزة عرض الإجازة عبر الشركة. | عند تمكين ميزة الإجازة عبر الشركة، يتم عرض كود السبب الآن كما هو متوقع. |
| 573676 | لا يمكن إضافة **الفترة** إلى **إدارة الميزات > الارتباطات > خطط الميزات**. | الأخطاء التي تم إصلاحها حيث تعذر إضافة **الفترة** أو تحديثها في نموذج **خطة الميزة**. |

## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| مساحة عمل إدارة المزايا | [مساحة عمل إدارة المزايا (معاينة)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [مساحة عمل إدارة المزايا](hr-benefits-management-workspace.md) |
| تحسينات تجربة سير العمل للإجازة والغياب | [تحسينات تجربة سير العمل للإجازة والغياب](https://go.microsoft.com/fwlink/?linkid=2147528) | [طلب إجازة](hr-employee-self-service-request-time-off.md)|
| تمكين تكامل كشوف المرتبات المبسط (واجهات برمجة تطبيقات تكامل الرواتب) | [تمكين التكامل المبسط مع موفري كشوف المرتبات](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [‏‫واجهة API لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)|

## <a name="coming-soon"></a>قريبًا

| الميزة | تفاصيل |
| --- | --- |
| المهارات التي تم إدخالها بواسطة مدير للموظفين يمكن اعتمادها تلقائيًا من خلال سير عمل | قريبًا. |
| Platform update 10.0.18 (42) | تمت جدولة تحديث النظام الأساسي 10.0.18 بحيث يبدأ نشره مع إصدار الخدمة في 17 مايو 2021. لمزيد من المعلومات، راجع [تحديثات النظام الأساسي للإصدار 10.0.18 من تطبيقات Finance and Operations (مايو 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| دعم الحقول المخصصة في قواعد الأهلية لإدارة الميزات  | [دعم الحقول المخصصة لمعالجة الأهلية](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>راجع أيضًا

[ما الجديد أو المتغير في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 1 من إصدار Dynamics 365 Human Resources  2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
