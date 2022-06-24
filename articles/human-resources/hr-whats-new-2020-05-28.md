---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (28‏ مايو 2020)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 28 مايو 2020.
author: andreabichsel
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42cb9e595c2997f17f487c31f674d1c099a3c80d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902936"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (28‏ مايو 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.3287. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a>لا يعمل كيان LeaveRequest عند تمكين أنواع متعددة لكل خطة إجازة (447498)

مع هذا التغيير، يتوفر **LeaveEnrollmentV2Entity** الآن لتصحيح الخطأ الذي يحدث عند تمكين أنواع إجازات متعددة.

## <a name="batch-contention-reduction-feature-preview-446619"></a>ميزة تقليل تعارضات الدُفعات (معاينة) (446619)

عند تمكين هذه الميزة، يمكنك توقع انخفاض الحظر على جداول إطار عمل الدُفعة مع تحديد المهام وإنجازها.

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a>UpdateConflict أثناء حفظ سجل عامل يمنع تحرير سجل في "الأشخاص" (427915)

يعمل هذا التغيير على تصحيح خطأ عند إضافة عامل جديد وتحديث معلومات العنوان وتغيير تفضيل اللغة. في هذا السيناريو الفريد، يظهر خطأ يشير إلى تعذر تحديث السجل. 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a>تعذر إضافة مرفق بطلب إجازة موافق عليه لإعادة إرساله (425407)

يسمح هذا التغيير الآن للمرفقات بالموافقة على طلبات الإجازات.

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a>بإمكان المستخدم إدخال تعويض لأحد الموظفين في نموذج كيان قانوني مختلف (409529)

يؤدي هذا التغيير إلى تعطيل خيارات التعويض لمنع الإدخال غير المقصود لسجلات التعويض للكيان القانوني غير الصحيح.

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a>خطأ عندما تقوم بتحويل الموظف وتاريخ تعيين منصب العامل يقع قبل مدة المنصب (429402)

تم تحديث رسائل الخطأ عند تحويل أحد الموظفين في هذا السيناريو كي يتم وصف التغييرات المطلوبة لتصحيح المشكلة بشكل أفضل.

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a>قدرات المرفقات في تسجيل مزايا الخدمة الذاتية للموظفين
 
يمكنك الآن إضافة مرفقات أثناء عملية تسجيل المزايا لكل خطة قام الموظف بالتسجيل فيها. يمكنك بعد ذلك عرض المرفقات داخل نموذج **ميزات العامل المسجل**.

## <a name="in-preview"></a>قيد المعاينة

## <a name="human-resources-application-in-teams"></a>تطبيق Human Resources في Teams

بإمكان الموظفين عرض وطلب الوقت بعيدًا عن العمل ضمن Microsoft Teams يمكنهم التفاعل مع روبوت لإنشاء طلبات الإجازات. لمزيد من المعلومات، راجع [تطبيق Human Resources في Teams‎](./hr-admin-teams-leave-app.md). 

## <a name="leave-suspension"></a>تعليق الإجازة

يمكنك تعليق الإجازة والغياب في Human Resources لأحد الموظفين. يؤدي تعليق الإجازة إلى إيقاف استحقاقات أنواع الإجازة المحددة. إذا حدث التعليق بعد معالجة الاستحقاق، فإن تعليق الإجازة يؤدي إلى إنشاء تسوية تناسبية لرصيد إجازات الموظف. لمزيد من المعلومات، راجع [تعليق الإجازة](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>تحديث تجربة المستخدم للاشاره إلى ان الاستحقاق معلق (429550)

وتشير تجربة المستخدم الآن إلى انه تم تعليق الاستحقاق لإحدى الخطط.

## <a name="coming-soon"></a>قريبًا

## <a name="database-logging-in-preview-in-june"></a>تسجيل قاعدة البيانات (في المعاينة في يونيو)

تسمح ميزة تسجيل قاعدة البيانات بتحديد الجدول والحقول التي يجب مراقبتها. كما تسمح لك بتحديد الأحداث التي يجب أن تشغّل تعقب التغييرات. تتوفر إمكانيات الاستعلام لرؤية هذه التغييرات مع مرور الوقت.

## <a name="buy-and-sell-leave-in-preview-june-1"></a>شراء الإجازات وبيعها (في المعاينة 1 يونيو)

توفر بعض المؤسسات ميزة تتيح للموظفين شراء الإجازات أو بيعها. غالبا ما تُدار هذه العملية يدويًا. توفر هذه الميزة طريقة تلقائية لإدارة السياسات والطلبات الخاصة بقسم الموارد البشرية، وتساعد على إزالة الأخطاء مع تنظيم عملية إدارة الإجازات. لمزيد من المعلومات، راجع:

- [إدارة سياسات شراء الإجازة وبيعها](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [شراء الإجازة وبيعها](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>كيانات إطار عمل إدارة البيانات (DMF) لإدارة المزايا
 
يتم إصدار كيانات إدارة المزايا. تتيح كيانات DMF استيراد البيانات وتصديرها لتكوين إدارة المزايا بسهولة. كما سيتوفر قالب إدارة المزايا لنقل البيانات. يقوم هذا القالب بتصدير البيانات واستيرادها بطريقة تسلسلية لمراعاة تبعيات البيانات.

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a>إضافة كود السبب إلى تعليقات الاستحقاق (1 يونيو)

تمت إضافه أكواد السبب إلى تعليق الاستحقاق.

## <a name="carry-forward-rules-june-1"></a>قواعد نقل الإجازة (1 يونيو)

يمكنك تحديد نوع الإجازة المنقولة للأرصدة المنقولة حيث يتم تحويل تسويات النقل. على سبيل المثال، إذا قام أحد الموظفين بنقل إجازة من 10 أيام، يمكنك انتقاء نوع إجازة آخر لمدة العشرة أيام هذه. لمزيد من المعلومات، راجع [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a>تعليق استحقاق الإجازة لأنواع الإجازات المحددة (1 يونيو)

في هذا الإصدار، يمكن للموارد البشرية إنشاء قاعده لكي يتم تعليق استحقاق الإجازات للموظفين الذين لديهم طلبات الاجازه التي تم إدخالها لإجازه غير مدفوعة. يمكن أن تكون الإجازة غير المدفوع نوعا، ولكن ليس من الضروري أن تكون كذلك. يمكنك تعليق أي إجازة استنادا إلى نوع إجازة آخر.

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a>يتوفر كيان DMF لتعليقات الاستحقاق (1 يونيو)

يتوفر كيان DMF الآن لتعليقات الاستحقاق.

## <a name="see-also"></a>راجع أيضًا

[المزايا الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]