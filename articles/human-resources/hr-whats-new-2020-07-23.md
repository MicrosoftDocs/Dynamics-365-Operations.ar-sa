---
title: ما الجديد والمتغير في Dynamics 365 Human Resources (23 يوليو 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 23 يوليو 2020.
author: andreabichsel
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb4ef2bf335e19d0d890465c851c46f66ef8bd8e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891855"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a>ما الجديد والمتغير في Dynamics 365 Human Resources (23 يوليو 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.3416. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a>لا يعمل حذف الأبعاد المالية في أحد المناصب كما هو متوقع (445476)

تؤدي الآن إزالة الأبعاد من منصب إلى إزالة هذه المناصب نفسها من Dataverse.

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a>المناصب غير الموجودة في التدرج الهرمي تظهر كمناصب غير نشطة (397257)

المناصب غير النشطة (التي انتهت مدة صلاحيتها)، لم تعد تظهر في التدرج الهرمي للمناصب على أنها **مناصب غير موجودة في التدرج الهرمي**. 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a>يتسبب التحقق من الصحة الذي يحدث بين LeaveEnrollmentEntity وHcmWorkerEntity على إطار عمل إدارة البيانات (DMF) في حدوث تحميلات بيانات بطيئة (442324)

تؤدي التغييرات في هذا الإصدار إلى زيادة أداء **LeaveEnrollmentEntity**.

## <a name="unable-to-personalize-in-organization-administration-447490"></a>يتعذر التخصيص في إدارة المؤسسة (447490)

وبهذا التغيير، يمكنك الآن تخصيص الارتباطات في **إدارة المؤسسة**.

## <a name="in-preview"></a>قيد المعاينة

## <a name="mandatory-fields"></a>حقول إلزامية 

يمكنك الآن جعل الحقول إلزامية باستخدام إمكانيات إضفاء طابع شخصي للموارد البشرية. تتطلب هذه الميزة **طرق عرض محفوظة**.

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

## <a name="add-attachments-to-time-off-requests"></a>إضافة مرفقات إلى طلبات الإجازة

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

## <a name="checklist-entities-included-in-dataverse"></a>تضمين كيانات قائمة الاختيار في Dataverse

ستتوفر كيانات قائمة الاختيار لعمليات الإلحاق وإلغاء الإلحاق والتحويلات وعمليات الأعمال قريبًا في Dataverse.

## <a name="platform-changes"></a>تغييرات النظام الأساسي

Platform update 10.0.12 (36)

## <a name="see-also"></a>راجع أيضًا

[الجديد أو المتغير في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]