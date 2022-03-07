---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (14‏ مايو 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 14 مايو 2020.
author: andreabichsel
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cb4693f3c856e7abcc39cbd658183d01ec98a066
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063737"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (14‏ مايو 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.3244. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم المرجع في  Lifecycle Services (LCS).

## <a name="platform-changes"></a>تغييرات النظام الأساسي

يتم تضمين تغييرات النظام الأساسي في إصدار هذا الأسبوع. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.10 من تطبيقات التمويل والعمليات (مايو 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34.md). يتضمن هذا الإصدار إصلاحات الأخطاء والتغييرات التي تمت على طرق العرض المحفوظة.
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a>تأكد من أن قوائم اختيار Dataverse متسقة مع تعدادات الإجازات (436343)

قوائم اختيار Dataverse متسقة الآن مع تعدادات الإجازات.

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a>السماح للمستخدمين بتكوين سير عمل طلب الإجازة استنادا إلى مقدار الطلب (300044)

يمكن للمستخدمين تكوين سير عمل طلبات الإجازة استنادا إلى مقادير الطلبات.
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a>نموذج العامل الجديد يعرض البيانات عبر قائمة طرق العرض عند تمكين الأمان المتقدم (403185)

يصحح هذا الإصدار كيفية عمل عرض العاملين عبر الكيانات القانونية عند تمكين الوصول المتقدم ويمكن الوصول إلى العاملين في شركات أخرى.

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a>السماح بتشغيل استحقاقات الإجازة لخطة فردية أو شركة فردية (318844)

مع هذا التغيير، يمكنك تشغيل استحقاقات لإحدى الشركات أو إحدى الخطط.
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a>إظهار مكافئ الدوام الكامل (FTE) للمنصب في نموذج العمال المسجلين (414658)

وتحدد قيمة FTE من منصب العامل معدل استحقاق العامل عند تمكين الخيار FTE في نوع الإجازة. يتم الآن تضمين هذا الحقل في نموذج **العاملين المسجلين** ومربع حوار **التسجيل الجماعي**.

## <a name="add-leave-balance-expiration-batch-job-431266"></a>إضافة وظيفة دفعية لانتهاء صلاحيه رصيد الإجازة (431266)

تتوفر الآن وظيفة دفعية جديدة يتم تشغيلها يوميًا. وهي تقلل رصيد الإجازة المتبقي عندما تصبح تواريخ انتهاء الصلاحية حديثة.

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a>تصدير جهات الاتصال الشخصية لأحد الموظفين باستخدام كيان شخص جهة الاتصال الشخصية للعامل لا يصدر جهات الاتصال الشخصية بنوع العلاقة الرئيسية (345893)

يتعذر على كيان بيانات **شخص جهة الاتصال الشخصية للعام** (**HcmPersonalContactPersonEntity** في DMF و **PersonalContactPerson** في OData) تصدير جهات الاتصال الشخصية التي تتضمن نوع العلاقة **رئيسي**. تم إصلاح هذه المشكلة لجهات الاتصال الشخصية التي يتم إنشاؤها بعد هذا التغيير. سيتم حل جهات الاتصال الشخصية الموجودة من النوع **رئيسي** في إصدار لاحق.

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a>تمكين عرض أكواد السبب عبر سيناريوهات مختلفة عند تعليمها على أنها إجازة وغياب وتمكين نموذج الموظف انسيابي (434163)

يقيد هذا التغيير أكواد السبب على رموز الإجازة والغياب فقط عند تمكين إدخال الموظف الانسيابي.

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a>ميزة المعاينة التي تعيين خطة إجازة للموظفين في المستقبل تعرض خطأ (433555)

يعمل هذا التغيير على تصحيح الخطأ عندما تتضمن خطة الإجازة نوعي إجازة معينين وأنت تحاول تعيين موظف.

## <a name="getting-started-banner-appears-for-all-users-441731"></a>ظهور شعار الشروع في العمل لكافة المستخدمين (441731)

بهذا التغيير، يتم إخفاء شعار الشروع في العمل للمستخدمين الذين لا يكونون من مسؤولي النظام أو مسؤولي إدارة البيانات. 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a>يعمل كيان عنوان العامل في Dataverse بشكل مختلف من حيث تواريخ وقت سريان في Human Resources (425071)

يؤدي هذا التغيير إلى الاحتفاظ بمعلومات العنوان التي تمت محاذاتها في سيناريوهات معينة، استنادا إلى تواريخ العنوان.

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a>تعذر إضافة مرفق لطلب إجازة معتمد (425407)

باستخدام إصدار هذا الأسبوع ، يمكنك إضافة مرفقات إلى طلبات الإجازة المعتمدة دون تغيير طلب الإجازة.

## <a name="in-preview"></a>قيد المعاينة

## <a name="leave-suspension"></a>تعليق الإجازة

يمكنك تعليق الإجازة والغياب في Human Resources لأحد الموظفين. يؤدي تعليق الإجازة إلى إيقاف استحقاقات أنواع الإجازة المحددة. إذا حدث التعليق بعد معالجة الاستحقاق، فإن تعليق الإجازة يؤدي إلى إنشاء تسوية تناسبية لرصيد إجازات الموظف. لمزيد من المعلومات، راجع [تعليق الإجازة](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>تحديث تجربة المستخدم للاشاره إلى ان الاستحقاق معلق (429550)

وتشير تجربة المستخدم الآن إلى انه تم تعليق الاستحقاق لإحدى الخطط.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>تعليق استحقاق الإجازه لأنواع الإجازات المحددة (272447)

في هذا الإصدار، يمكن للموارد البشرية إنشاء قاعده لكي يتم تعليق استحقاق الإجازات للموظفين الذين لديهم طلبات الاجازه التي تم إدخالها لإجازه غير مدفوعة. يمكن أن تكون الإجازة غير المدفوع نوعا، ولكن ليس من الضروري أن تكون كذلك. يمكنك تعليق أي إجازة استنادا إلى نوع إجازة آخر.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>يتوفر كيان DMF لتعليقات الاستحقاق (429549)

يتوفر كيان DMF الآن لتعليقات الاستحقاق.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>إضافة كود السبب إلى تعليقات الاستحقاق (429547)

تمت إضافه أكواد السبب إلى تعليق الاستحقاق.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>بدء النقل من معلمات الموارد البشرية إلى معلمات الإجازة والغياب‬

يبدأ هذا الإصدار في دمج معلمات الموارد البشرية بمعلمات الإجازة والغياب‬.

## <a name="carry-forward-rules"></a>قواعد نقل الإجازة

يمكنك تحديد نوع الإجازة المنقولة للأرصدة المنقولة حيث يتم تحويل تسويات النقل. على سبيل المثال، إذا قام أحد الموظفين بنقل إجازة من 10 أيام، يمكنك انتقاء نوع إجازة آخر لمدة العشرة أيام هذه. لمزيد من المعلومات، راجع [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md).

## <a name="see-also"></a>راجع أيضًا

[المزايا الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]