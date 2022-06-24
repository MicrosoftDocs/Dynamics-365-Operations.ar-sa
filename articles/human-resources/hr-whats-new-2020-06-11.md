---
title: ما الجديد والمتغير في Dynamics 365 Human Resources (11 يونيو 2020)
description: توضح هذه المقالة الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 11 يونيو 2020.
author: andreabichsel
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 78d0adbfea19ce9d77b74cd44dbf19366ae37ff7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852918"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a>ما الجديد والمتغير في Dynamics 365 Human Resources (11 يونيو 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.3316. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a>يعمل نموذج الموظف المبسط على إيقاف أزرار الإغلاق (X) للنموذج التابع (442369)

عند تمكين نموذج **العامل** الجديد، لا يعمل زر الإغلاق (**X**) أحيانا على النماذج التابعة. هذه المشكلة متقطعه. يمكنك إغلاق النموذج بعد تركه والعودة اليه. علي سبيل المثال، يمكنك تحديد عنصر قائمة على اليسار، والتنقل للخلف إلى نموذج **العامل** ، ثم إغلاقه. يعمل إصدار هذا الأسبوع على إصلاح هذه المشكلة. 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a>كيان شخص جهة الاتصال الشخصية للعامل لا يقوم بتصدير جهات الاتصال الشخصية بنوع علاقة رئيسي

ومع هذا الإصدار، يقوم كيان **شخص جهة الاتصال الشخصية للعامل** بتصدير كافة أنواع العلاقات.

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a>يجب أن يكون HcmPositionWorkerAssignmentV2Entity جزءًا من حزمة ‏‫تكامل كشف المرتبات Ceridian‬ بشكل افتراضي (448506)

وبهذا التغيير، يتم تضمين **HcmPositionWorkerAssignmentV2Entity** في حزمة ‏‫تكامل كشف المرتبات Ceridian‬.

## <a name="in-preview"></a>قيد المعاينة

## <a name="database-logging"></a>تسجيل قاعدة البيانات

تسمح ميزة تسجيل قاعدة البيانات بتحديد الجدول والحقول التي يجب مراقبتها. كما تسمح لك بتحديد الأحداث التي يجب أن تشغّل تعقب التغييرات. يمكنك استخدام إمكانيات تسجيل قاعده البيانات لرؤية هذه التغييرات بمرور الوقت. لمزيد من المعلومات، راجع [‏‫تكوين وإدارة تسجيل قاعده البيانات‬](hr-admin-database-logging.md).

## <a name="human-resources-application-in-teams"></a>تطبيق Human Resources في Teams

بإمكان الموظفين عرض وطلب الوقت بعيدًا عن العمل ضمن Microsoft Teams يمكنهم التفاعل مع روبوت لإنشاء طلبات الإجازات. لمزيد من المعلومات، راجع [تطبيق Human Resources في Teams‎](./hr-admin-teams-leave-app.md). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>كيانات إطار عمل إدارة البيانات (DMF) لإدارة المزايا
 
يتم إصدار كيانات إدارة المزايا. تتيح كيانات DMF استيراد البيانات وتصديرها لتكوين إدارة المزايا بسهولة. كما سيتوفر قالب إدارة المزايا لنقل البيانات. يقوم هذا القالب بتصدير البيانات واستيرادها بطريقة تسلسلية لمراعاة تبعيات البيانات.

## <a name="buy-and-sell-leave"></a>شراء الإجازة وبيعها 

توفر بعض المؤسسات ميزة تتيح للموظفين شراء الإجازات أو بيعها. غالبا ما تُدار هذه العملية يدويًا. تقوم هذه الميزة بأتمتة سياسات وطلبات الإدارة الخاصة بقسم الموارد البشرية. إذا تُبسط عملية عملية إدارة الإجازات وتساعد علي تقليل الأخطاء. لمزيد من المعلومات، راجع:

- [إدارة سياسات شراء الإجازة وبيعها](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [شراء الإجازة وبيعها](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>استحقاق الإجازة‬‏‫ لشركة فردية أو خطة فردية

يمكن للعملاء معالجة الاستحقاقات لشركة فردية أو إجازة فردية وخطه غياب. وبذلك تصبح عملية الاستحقاق واضحة للعملاء الذين لديهم سياسات مختلفة تتعلق بسنوات الإجازة أو استحقاقات الإجازات. لمزيد من المعلومات، راجع [‏‫استحقاق الإجازات لكل شركة أو خطة إجازة‬](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>إضافة مرفقات إلى طلبات زمن التوقف‬

تعد القدرة على إضافه مرفقات إلى طلبات الإجازات المعتمدة عاملا مهما في بيئة مرض كوفيد-19 الحالي. يمكن للموظفين الآن إضافه هذه المرفقات. كما يتوفر لديهم المعرفة الكافية حول كيفية إجراء التحديثات على طلبات الإجازات. لمزيد من المعلومات، راجع [‏‫إضافة مرفق إلى طلب موجود‬](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>إضافة كود السبب إلى تعليقات الاستحقاق 

تمت إضافه أكواد السبب إلى تعليق الاستحقاق.

## <a name="carry-forward-rules"></a>قواعد نقل الإجازة 

يمكنك تحديد نوع الإجازة المنقولة للأرصدة المنقولة حيث يتم تحويل تسويات النقل. على سبيل المثال، إذا قام أحد الموظفين بنقل إجازة من 10 أيام، يمكنك انتقاء نوع إجازة آخر لمدة العشرة أيام هذه. لمزيد من المعلومات، راجع [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>تعليق استحقاق الإجازه لأنواع الإجازات المحددة

يمكن للموارد البشرية إنشاء قاعده لكي يتم تعليق استحقاق الإجازات للموظفين الذين لديهم طلبات الاجازه التي تم إدخالها لإجازه غير مدفوعة. يمكن أن تكون الإجازة غير المدفوع نوعا، ولكن ليس من الضروري أن تكون كذلك. يمكنك تعليق أي إجازة استنادا إلى نوع إجازة آخر.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>يتوفر كيان DMF لتعليقات الاستحقاق 

يتوفر كيان DMF الآن لتعليقات الاستحقاق.

## <a name="coming-soon"></a>قريبًا

## <a name="new-platform-capabilities"></a>إمكانات النظام الأساسي الجديدة 

ستتمكن من جعل الحقول إلزاميه باستخدام التخصيص. ستلزمك هذه الميزة بتمكين **طرق العرض المحفوظة**.

## <a name="configure-the-name-of-employee-self-service"></a>تكوين اسم خدمة الموظف الذاتية

سيتوفر خيار جديد في محددات الموارد البشرية لتحديث اسم مساحة عمل خدمة الموظف الذاتية إلى الخدمة الذاتية. 

## <a name="see-also"></a>راجع أيضًا

[المزايا الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]