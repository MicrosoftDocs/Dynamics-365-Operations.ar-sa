---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources 21 يناير 2021
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 21 يناير 2021.
author: marcelbf
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: be50596cd64839ba82b847b2fabb0f46dc749a3f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686844"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-21-2021"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources 21 يناير 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة أو على وشك القدوم في Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2020، الموجة 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.3866.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزات التالية بشكل عام مع هذا الإصدار.

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| تحديث النظام الأساسي 10.0.16 (40) | -- | [تحديثات النظام الأساسي للإصدار 10.0.16 من تطبيقات التمويل والعمليات (فبراير 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16.md) |
| طلبات سير العمل المحسنة والموافقات | [تحسينات تجربة سير العمل للمؤسسة وإدارة العاملين](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [خيار التكوين لقائمة وضع عناصر العمل المعينة لي](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| تحديثات التوافق مع قانون الرعاية ميسورة التكلفة للنموذج 1095-C، والنموذج 1095-B، والتقارير الإلكترونية في المزايا القديمة | -- | -- | 
| تدعم إدارة الميزات الآن تقارير التوافق مع قانون الرعاية ميسورة التكلفة للكيانات القانونية التي يوجد مقرها في الولايات المتحدة. | -- | [إنشاء تقارير قانون الرعاية ميسورة التكلفة في إدارة الميزات](hr-benefits-management-aca-reports.md) |
| تحتوي إدارة الميزات الآن على كيانات معروضة لمستويات أسعار الميزات ومستويات أسعار المزايا المضاعفة  | -- | -- |

### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. قد نقوم بتحديث هذا الموضوع لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذا الموضوع في البداية.

| رقم الإصدار | إصدار |  الوصف |
| --- | --- | --- |
| 533079 | خطأ في التنقل "تم استدعاء النموذج بشكل غير صحيح" عندما نحاول النظر إلى الخصومات. | إصلاح الخطأ الذي يظهر أثناء النظر إلى خصومات المزايا مع طريقة العرض **اعتبارا من التاريخ**. |
| 543641 | لا يتم ملء الرمز البريدي بالتقارير الإلكترونية.  | إصلاح خطأ داخلي بشأن عدم ظهور الرمز البريدي في التقارير الإلكترونية لقانون الرعاية ميسورة التكلفة لإدارة الميزات عندما يكون كود التغطية من M إلى Q. |
| 542815 | شاشة جهة الاتصال الشخصية في خدمة الموظف الذاتية تسمح للموظفين برؤية جهات الاتصال الشخصية الأخرى. | إصلاح الخطأ حيث كان النموذج **تحرير** لجهات الاتصال الشخصية لللخدمة الذاتية للموظف الاستعلام الخاص به بما يكفي لضمان استرداد جهة اتصال شخصية واحدة فقط، مما يسمح للمستخدم باستخدام اختصارات لوحة المفاتيح لعرض جهات اتصال الأشخاص الآخرين. |
| 536157 | لا يمكن صفحة **تكامل Microsoft Dataverse** في إدارة النظام بسبب استدعاء IsVirtualEntityPackageInstalled(). | مشكلة تمنع صفحة **تكامل Microsoft Dataverse** من التحميل في الموارد البشرية. |
| 533079 | خطأ في التنقل "تم استدعاء النموذج بشكل غير صحيح" عندما نحاول النظر إلى الخصومات. | إصلاح الخطأ الذي يحدث في نموذج **الخصومات** لإدارة الميزات عند عرضه **اعتبارًا من تاريخ**. |
| 537264 | علامة التبويب السريعة **المعلومات الشخصية** مفقودة من سجل المرشح. | تتوفر الآن المعلومات الشخصية الخاصة بالمرشح في سجل المرشح. |
| 537267 | لا يتم عرض **الخبرة المهنية** في سجلات المرشح الداخلية. | لا يتم عرض علامة التبويب السريعة **الخبرة المهنية** في سجلات المرشح الداخلية. في السابق، إذا كان المرشح داخليًا، يتم استبدال **الخبرة المهنية** بـ **تاريخ التوظيف**، وهو عبارة عن سجل توظيف المرشح داخل المؤسسة. وكلاهما قابل للتطبيق ويجب أن يتم عرضه للمرشحين الداخليين. |
| 537067 | لا يتم عرض **مسموح بالاتصال بصاحب العمل**. | تمت إضافة عنصر تحكم **مسموح بالاتصال بصاحب العمل** إلى جزء **تحرير الخبرة المهنية** لسجل المرشح. |
| 525957 | لا يتم تحديث **حالة المرشح** مع المرشحين الداخليين عند اكتمال النقل. | عند اكتمال النقل (تحديد زر **تغيير المنصب** أو **استمرار** في صفحة **نقل العامل إلى تعيين منصب جديد**)، يجب أن تتغير **الحالة** في سجل المرشح إلى **تم توظيفه**. |
| 537051 | لا تتم مزامنة رموز العملة للروبية الهندية والليرة التركية بشكل صحيح مع Dataverse | تتم الآن مزامنة الرموز للروبية الهندية والليرة التركية بشكل صحيح مع Dataverse. |
| 534846 | يجب تمكين جداول التوظيف لإدارة البيانات. | تم الآن تمكين الجداول الجديدة التي تم إنشاؤها لطلبات التعيين والمرشحين لإدارة البيانات. وهذا يسمح بتمكين تعقب التغييرات للجداول، مما يمكّن تعقب تغييرات OData في جداول Dataverse الظاهرية. |
| 533474 | تصحيح المرجع المفقود إلى Microsoft.SqlServer.XEvent.dll. | تسببت استثناءات تحميل التجميع لـ Microsoft.SqlServer.XEvent.dll في منع جداول Dataverse الظاهرية من الإعداد في بعض البيئات. |
| 481122 | تعرض مساحة عمل **الأشخاص** مناصب التقاعد. | كان يتم عرض مناصب التقاعد كمناصب مفتوحة في مساحة عمل **الأشخاص**. لم تعد مناصب التقاعد معروضة. | 
| 541978 | إضافة عنوان البريد الإلكتروني الأساسي إلى كيان BaseWorker. | أضاف هذا التغيير عنوان البريد الإلكتروني الأساسي للعامل إلى HcmWorkerBaseEntity. |

## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| تطبيق Human Resources في Microsoft Teams | [تجربة إجازة وغياب الموظف في Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [تطبيق Human Resources في Teams](./hr-admin-teams-leave-app.md)<br>[إدارة طلبات الإجازة في Teams](hr-teams-leave-app.md) |
| التكامل مع LinkedIn Talent Hub | [التكامل مع LinkedIn Talent Hub](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [التكامل مع LinkedIn Talent Hub](./hr-admin-integration-linkedin.md) |
| عرض الإجازات عبر الشركات للمديرين | [عرض إجازات الموظفين عبر الشركات للمديرين](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [تكوين معلمات الإجازة والغياب](./hr-leave-and-absence-parameters.md) |
|تقديم نتيجة تحليلات إضافية في أرصدة الإجازات| [تقديم نتيجة تحليلات إضافية في أرصدة الإجازات](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [إدارة إجازة الموظف](./hr-leave-and-absence-manage-employee-leave.md) |
| المديرون قادرون على إرسال طلبات التعيين للمناصب | [المديرون قادرون على إرسال طلب تعيين للمناصب المفتوحة](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [إضافة طلب تعيين](./hr-personnel-recruit.md#add-a-recruiting-request) |
| ملف تعريف مرشح محسن في إدارة العاملين | [ملف تعريف مرشح محسن في إدارة العاملين](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [إضافة ملف تعريف مرشح أو تحريره](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| تمكين التكاملات المبسطة مع موفري التعيين | [تمكين التكاملات المبسطة مع موفري التعيين](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [تعيين المرشحين للوظائف](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>قريبًا
| الميزة | تفاصيل |
| --- | --- |
| تأكيد البريد الإلكتروني لتسجيلات المزايا | سوف توفر الميزة خيار إرسال بريد إلكتروني للتأكيد إلى الموظفين عند تسجيل الخروج من تجربة تسجيل المزايا في الخدمة الذاتية للموظف. لمزيد من المعلومات، راجع [تكوين معلمات إدارة المزايا لكل شركة](hr-benefits-setup-parameters-per-company.md). |
| المهارات التي تم إدخالها بواسطة مدير للموظفين يمكن اعتمادها تلقائيًا من خلال سير عمل | قريبًا. |

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2020، الموجة 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>تحديثات المصطلحات لـ Microsoft Dataverse

بدء من نوفمبر 2020، تمت إعادة تسمية Common Data Service إلى [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). راجع [الإعلانات الرسمية](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/)الموجودة على مدونة Power Apps لمعرفة المزيد. بالترابط مع تغيير هذا الاسم، تم تحديث بعض المصطلحات في Dataverse. علي سبيل المثال ،تم تعيير مصطلح *كيان* إلى مصطلح *جدول* و *حقل* إلى *عمود*. لمزيد من المعلومات، راجع [تحديثات المصطلحات](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

في هذا الإصدار، تم تحديث المصطلحات ذات الصلة بتكامل Dynamics 365 Human Resources مع Dataverse في كافة أنحاء التطبيق لتعكس هذه التغييرات. على سبيل المثال، نموذج **تكامل Common Data Service** أصبح الآن **تكامل Microsoft Dataverse**.

لمعرفة المزيد حول تكامل Dynamics 365 Human Resources مع Microsoft Dataverse، راجع [تكوين تكامل Microsoft Dataverse ](./hr-admin-integration-common-data-service.md) و[تكوين جداول Microsoft Dataverse الظاهرية](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>راجع أيضًا

[ما الجديد أو المتغير في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2020](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]