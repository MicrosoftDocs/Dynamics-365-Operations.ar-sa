---
title: الجديد أو المتغير في Dynamics 365 Human Resources‏ 2 ديسمبر 2020
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 2 ديسمبر 2020.
author: marcelbf
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 36d82efa182bff12442d51908d634cbddbd13fa9
ms.sourcegitcommit: fc852ae4939089a294d00fdf9cad8d6372ffb012
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2021
ms.locfileid: "5080028"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>الجديد أو المتغير في Dynamics 365 Human Resources‏ 2 ديسمبر 2020

يصف هذا الموضوع الميزات الجديدة أو المتغيرة أو على وشك القدوم في Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2020، الموجة 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.3788.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزات التالية بشكل عام مع هذا الإصدار.

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| المديرون قادرون على إرسال طلبات التعيين للمناصب | [المديرون قادرون على إرسال طلب تعيين للمناصب المفتوحة](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [إضافة طلب تعيين](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| ملف تعريف مرشح محسن في إدارة العاملين | [ملف تعريف مرشح محسن في إدارة العاملين](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [إضافة ملف تعريف مرشح أو تحريره](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| تمكين التكاملات المبسطة مع موفري التعيين | [تمكين التكاملات المبسطة مع موفري التعيين](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [تعيين المرشحين للوظائف](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |
| الارتباطات المخصصة في الخدمة الذاتية للمدير | [الارتباطات المخصصة في الخدمة الذاتية للمدير](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [الارتباطات المخصصة في الخدمة الذاتية للمدير](https://aka.ms/MSSCustomLinks) |


### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. قد نقوم بتحديث هذا الموضوع لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذا الموضوع في البداية.

| رقم الإصدار | إصدار | الوصف |
| --- | --- | --- |
| 514087 | يجب أن تتضمن BenefitEligibilityProcessResult التاريخ والوقت الذي تم استخدامه في المعالجة. | تتضمن نتيجة معالجة BenefitEligibity الآن الطابع الزمني للتاريخ لآخر معالجة، والتي كانت مفقودة في وقت سابق. |
| 526903 | فشل تسجيل الميزة للخطط التي لها توابع عند تشغيل **التحديد التلقائي للمعينين** في **المعلمات المشتركة للموارد البشرية**. | تم إصلاح مشكلة فشل تسجيل المزايا للمُعالين عندما تم تشغيل خيار **التحديد التلقائي للمعينين** للمعينين الافتراضيين. |
| 521922 | تعرض معلمة **إظهار الغياب دون تفاصيل** طلبات الإجازة في تقويم غياب الفريق. | تم عرض نوع الإجازة ولون نوع الإجازة وتفاصيل اليوم في تقويم غياب الفريق عندما تم تعيين **إظهار الغياب دون تفاصيل** إلى **نعم** في **معلمات الإجازة والغياب**. تمت معالجة ذلك ، والآن لا يتم عرض نوع الإجازة ويتم استخدام اللون الافتراضي لنوع الإجازة (الأزرق الداكن) لجميع أنواع الإجازات في تقويم غياب الفريق. |
| 527316 | لا تتم مزامنة تغييرات العنوان للوظيفة والمنصب وإشعارات العامل. | تمت إضافة علاقة العنوان مسبقًا إلى كيانات الوظيفة والمنصب والعامل. تعمل المزامنة لهذه العلاقة للمزامنة من Human Resources إلى Dataverse، ولكنها لا تعمل للإعلامات من Dataverse. تمت معالجة هذا. |
| 512275 | قم بإزالة خيارات الألوان من **معلمات الإجازة والغياب**. | الآن بعد أن تم تحديد الألوان في نوع الإجازة، لم تعد هناك حاجة إلى خيارات الألوان في **معلمات الإجازة والغياب**، لذا تمت إزالتها. |
| 437112 | نص رسالة خطأ مضللة أثناء تعيين وظيفة الموظف. | تم تحديث رسالة الخطأ عند تعيين عامل ومحاولة تعيينه لمنصب غير نشط. رسالة محدثة **المنصب المحدد غير نشط اعتبارًا من تاريخ بدء التوظيف. يُرجى التحقق من مدة هذا المنصب.** |
| 527816 | مشكلات الأداء مع صفحة **الإجازة**. | تم تحسين الأداء في صفحة **الإجازة**. |
| 523158 | لا يتم تنفيذ BenefitPeriodMigrationUpgrade وBenefitPlanMigrationUpgrade. | تم حل المشكلات المتعلقة بوظائف ترحيل المزايا المتعلقة بـ **الفترة** و **الخطة** اللذين لا يتم تنفيذهما بشكل صحيح. |

## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| تطبيق Human Resources في Microsoft Teams | [تجربة إجازة وغياب الموظف في Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [تطبيق Human Resources في Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[إدارة طلبات الإجازة في Teams](hr-teams-leave-app.md) |
| طلبات سير العمل المحسنة والموافقات | [تحسينات تجربة سير العمل للمؤسسة وإدارة العاملين](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [خيار التكوين لقائمة وضع عناصر العمل المعينة لي](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| التكامل مع LinkedIn Talent Hub | [التكامل مع LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [التكامل مع LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
|عرض الإجازات عبر الشركات للمديرين | [عرض إجازات الموظفين عبر الشركات للمديرين](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [تكوين معلمات الإجازة والغياب](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |
|تقديم نتيجة تحليلات إضافية في أرصدة الإجازات| [تقديم نتيجة تحليلات إضافية في أرصدة الإجازات](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [إدارة إجازة الموظف](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-employee-leave) |
| المديرون قادرون على إرسال طلبات التعيين للمناصب | [المديرون قادرون على إرسال طلب تعيين للمناصب المفتوحة](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [إضافة طلب تعيين](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| ملف تعريف مرشح محسن في إدارة العاملين | [ملف تعريف مرشح محسن في إدارة العاملين](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [إضافة ملف تعريف مرشح أو تحريره](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| تمكين التكاملات المبسطة مع موفري التعيين | [تمكين التكاملات المبسطة مع موفري التعيين](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [تعيين المرشحين للوظائف](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |

## <a name="coming-soon"></a>قريبًا

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2020، الموجة 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>راجع أيضًا

[الميزات الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2020](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]