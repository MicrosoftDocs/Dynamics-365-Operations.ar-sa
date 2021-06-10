---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (6 أكتوبر 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 6 أكتوبر، 2020.
author: jcart1106
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 640fca3c2c5dcd3a383b9a4a16e4933e3503b8ab
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054274"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-6-2020"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (6 أكتوبر 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة أو على وشك القدوم في Dynamics 365 Human Resources. لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2020، الموجة 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.3636.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزة التالية بشكل عام مع هذا الإصدار.

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| نتيجة تحليلات إضافية في تقويمات الإجازة | [تقديم نتيجة تحليلات إضافية في طرق عرض تقويم الإجازات](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-leave-calendar-views) | [عرض تقويم الفريق والشركة](hr-employee-self-service-calendar.md) |

### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

>[!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. قد تكون هناك تحديثات لهذا الموضوع لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذا الموضوع في البداية.

| رقم الإصدار | إصدار | الوصف |
| --- | --- | --- |
| 448806 | **نوع الهوية الافتراضي** يعمل على تصدير **RecID** في معلمات HCM | يعمل هذا التغيير في كيان معلمات الموارد البشرية إلى إضافة عمود إضافي يعرض **نوع الهوية الافتراضي**. |
| 492923 | لا يتم حفظ تسجيلات المهام في Lifecycle Services (LCS) | يمكن حفظ تسجيلات المهام الآن في LCS. |
| 429950 | لا تنتهي فترة صلاحية التعويض الثابت بشكل صحيح أثناء تغيير الموضع | عند تغيير موضع العامل في الصفحة **تحويل العامل**، تم تعيين تاريخ نهاية التعويض يومًا واحدًا قبل نهاية المنصب. تاريخ نهاية التعويض هو نفس تاريخ نهاية المنصب. |
| 467214 | يتم عرض **تحليلات الرواتب** فقط إذا تم تعيين **اسم تحويل معدل الدفع** إلى **سنوي** | لا تظهر معدلات دفع المرتب باسم يختلف عن **سنوي** في تحليلات التعويض. من خلال هذا التحديث، تستخدم الآن تحليلات التعويض كافة تحويلات معدل الدفع. عند تشغيل التقارير حسب **الساعة** أو **المرتب**، فإنه يتم تضمين تحويل معدل الراتب الذي يستخدم فترة غير الساعات في عامل تصفية **المرتب**. يتم تضمين معدلات الدفع التي تحتوي على الفترة **بالساعة** في عامل التصفية **بالساعة**. |
| 482464 | عند عرض **المراجعات**، لا تتغير طريقة عرض **التفاصيل** إلى طريقة عرض الشبكة بعد أن تقوم بتطبيق عامل تصفية. | بعد تطبيق عامل التصفية، تعرض شبكة المراجعات كما هو متوقع. |
| 483184 | لا تقوم Human Resources بإنشاء استحقاقات المغادرة عند تحديد **أساس المستوى** كـ **تاريخ البدء المعدل** في السجل **تسجيل الإجازة** |تتم تعبئة **تاريخ البدء المعدل** واستخدامه عند إنشاء استحقاقات الإجازة.  |
| 509731 | يُسبب طلب الإجازة لعامل سيتم إنهاء خدمته في المستقبل إذا قام بتطبيق الإجازة بعد تاريخ إنهاء الخدمة | يمكن الآن إرسال طلبات الإجازة للموظفين الذين لديهم تاريخ إنهاء الخدمة في المستقبل طالما أن الطلب قبل تاريخ إنهاء الخدمة. |
| 510716 | تتضمن تحليلات التعويض كل من الموظفين الذكور والإناث لـ **متوسط راتب الذكور في الساعة** | في تحليلات التعويض، يحتوي **متوسط راتب الذكور في الساعة** في **التحليل السكاني الخاص بالتعويض** على متوسط راتب الإناث. والآن يتضمن الذكور فقط. |
| 511348 | يجب أن تعرض الخدمة الذاتية للمزايا خطط المزايا الصالحة فقط من اليوم وحتى نهاية فترة الميزة | تم عرض خطط المزايا المنتهية الصلاحية للموظفين في الصفحة **تسجيل المزايا**. يعمل هذا الإصلاح على إزالة هذه الخطط. |
| 512706 | قم بتعيين الحقول التالية للقراءة فقط:<ul><li>BenefitPlanEmployeeEntity</li><li>EnrollmentConfirmed</li><li>EnrollmentConfirmedBy</li><li>EnrollmentConfirmedDateTime | تم تمكين الزرين **إضافة** و **إزالة** لتفاصيل الأبعاد بشكل صحيح بعد إكمال الإجراء. يجعل هذا التحديث على الصفحة **تفاصيل اجراء المنصب** الحقول غير قابلة للتحرير بعد إكمال الإجراء. |

## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| تطبيق Human Resources في Microsoft Teams | [تجربة إجازة وغياب الموظف في Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [تطبيق Human Resources في Teams](./hr-admin-teams-leave-app.md)<br>[إدارة طلبات الإجازة في Teams](hr-teams-leave-app.md) |
| طلبات سير العمل المحسنة والموافقات | [تحسينات تجربة سير العمل للمؤسسة وإدارة العاملين](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [خيار التكوين لقائمة وضع عناصر العمل المعينة لي](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| الكيانات الظاهرية في Dataverse لـ Human Resources | [توسيع Dynamics 365 Human Resources البيانات الأساسية في Dataverse](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [تكوين كيانات Dataverse الظاهرية](hr-admin-integration-common-data-service-virtual-entities.md) |

## <a name="coming-soon"></a>قريبًا

يتم جدولة الميزات الجديدة التالية لإصدارات مستقبلية:

- **تضمين كيانات قائمة الاختيار في Dataverse**: ستتوفر كيانات قائمة الاختيار لعمليات الإلحاق وإلغاء الإلحاق والتحويلات وعمليات الأعمال قريبًا في Dataverse.

- **أكواد سبب إدارة الميزات**: سيتم دمج أكواد سبب إدارة الميزات في وقت قريب مع أكواد السبب الموجودة في Human Resources. إذا قمت بإنشاء أكواد أسباب في إدارة الميزات تزيد عن 15 حرفًا، فيجب تغيير اسم كود السبب في نموذج **أكواد السبب** في إدارة الميزات بحيث تتكون من 15 حرفًا أو أقل. بعد تحديث الاسم، سيظهر كود السبب ضمن نموذج كود السبب في إدارة العاملين. سيتوفر هذا التغيير في المستقبل ولن يؤثر على الوظيفة الموجودة.

- **ارتباطات مخصصة في الخدمة الذاتية للمدير**: لدعم المديرين، نقوم الآن بتوسيع القدرات في الخدمة الذاتية للمدير. نقوم بإضافة الإمكانية لإضافة ارتباطات مخصصة ضمن علامة التبويب **فريقي**. تشبه هذه الميزة ميزة الارتباطات المخصصة في **علامة التبويب المعلومات الخاصة بي** في الخدمة الذاتية للموظف. لمزيد من المعلومات، راجع [ارتباطات مخصصة في الخدمة الذاتية للمدير‬](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service).

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2019، الموجة 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>الموارد الإضافية

[الميزات الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2020](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]