---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources 22 فبراير، 2021
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 22 فبراير 2021.
author: marcelbf
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d07e73ccd922e9d52a9de9260577087a50ef1da4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897824"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-22-2021"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources 22 فبراير، 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة الميزات الجديدة أو المتغيرة أو التي ستصدر قريبًا في Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.3988.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزات التالية بشكل عام مع هذا الإصدار.

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| تطبيق Dynamics 365 Human Resources لـ Microsoft Teams | [تجربة إجازة وغياب الموظف في Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [تطبيق Human Resources في Teams](./hr-admin-teams-leave-app.md)<br>[إدارة طلبات الإجازة في Teams](hr-teams-leave-app.md) |

### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. يمكن أن نقوم بتحديث هذه المقالة لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذه المقالة مبدئيًا.

| رقم الإصدار | المشكلة |  ‏‏الوصف‬ |
| --- | --- | --- |
| 529994 | لا يعمل تعديل الحقل **معروف باسم** في النموذج **عامل** على تشغيل تحديث Dataverse | تم إصلاح مشكلة حيث لا يمكن تحديث Dataverse عندما يتم تحديث الحقل **معروف باسم** في النموذج **العامل**. |
| 532651 | لا يستخدم تقرير تحليلات التعويض PBI تحويل العملة عند حساب معايير كافة الشركات | تم إصلاح مشكلة حيث لم يقم تقرير تحليلات التعويض PBI بتحويلات العملات بشكل صحيح. |
| 552226 | إغلاق معالجة حدث الحياة وإعادة فتح خطط عدة مرات لحدث حياة واحدة  | تم إصلاح مشكلة حيث كان هناك موظف في كيانات قانونية متعددة أثناء حدوث حدث الحياة، يتم إنشاء سجل حدث الحياة لكل كيان قانوني يتواجد به الموظف. عند معالجة أحداث الحياة، يجب تحديد الكيان القانوني المطلوب معالجته. ومع ذلك، لا يقوم منطق المعالجة بتقييد نفسه بهذا الكيان القانوني. بدلاً من ذلك، يقوم بعمليات لكافة الكيانات القانونية وإغلاق الخطط وإعادة فتحها في الكيان القانوني المحدد. يؤدي هذا الإجراء إلى معالجة حدث الحياة لعدة مرات في الكيان القانوني نفسه، مما ينتج عنه إغلاق/إعادة فتح كل خطة متأثرة بحدث الحياة. |
| 518064 | يمكن تحديد تابع واحد فقط من الخطط التابعة المستحقة عندما يتم تمييز أكثر من تابع كمعينين‬‏‫ افتراضيين | تم إصلاح مشكلة حيث لا يتم التحديد التلقائي للمعينين‬‏‫ الافتراضيين المتعددين في الخطط المستحقة. كما يمكنك الآن تعيين مستفيد أساسي لجهة اتصال شخصية. يتم إدراج المستفيد الرئيسي على إنه 100% في الخطط المستحقة عند وجود العديد من المستفيدين. |
| 552365 | تصدير وظائف إحضار قاعدة بياناتك الخاصة (BYOD) فشل بعد الترقية إلى تحديث النظام الأساسي 40 | تم إصلاح مشكلة حيث فشلت عمليات تصدير BYOD بعد تطبيق تحديث النظام الأساسي 40 علي البيئة. |
| 547123 | تحديد عدد المهام التي تم الاستعلام عنها في قائمة مهام لوحة المعلومات | يقتصر الآن عدد المهام المعروضة في قائمة المهام على 15 لإصلاح مشكلة الأداء الناتجة عن عدد كبير من المهام التي تحاول تحميلها. |

## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| عرض الإجازات عبر الشركات للمديرين | [عرض إجازات الموظفين عبر الشركات للمديرين](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [تكوين معلمات الإجازة والغياب](./hr-leave-and-absence-parameters.md) |
| مساحة عمل إدارة المزايا | [مساحة عمل إدارة المزايا (معاينة)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [مساحة عمل إدارة المزايا](hr-benefits-management-workspace.md) |
| تقييد الموظفين من تحرير تفاصيل جهة اتصال العمل | [تقييد الموظفين من تحرير تفاصيل جهة اتصال العمل](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [تقييد تحرير المعلومات الشخصية](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>قريبًا

| الميزة | تفاصيل |
| --- | --- |
| المهارات التي تم إدخالها بواسطة مدير للموظفين يمكن اعتمادها تلقائيًا من خلال سير عمل | قريبًا. |

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>تحديثات المصطلحات لـ Microsoft Dataverse

بدء من نوفمبر 2020، تمت إعادة تسمية Common Data Service إلى [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). راجع [الإعلانات الرسمية](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/)الموجودة على مدونة Power Apps لمعرفة المزيد. بتغيير هذا الاسم، تم تحديث بعض المصطلحات في Dataverse. علي سبيل المثال ،تم تعيير مصطلح *كيان* إلى مصطلح *جدول* و *حقل* إلى *عمود*. لمزيد من المعلومات، راجع [تحديثات المصطلحات](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

في هذا الإصدار، تم تحديث المصطلحات ذات الصلة بتكامل Dynamics 365 Human Resources مع Dataverse في كافة أنحاء التطبيق لتعكس هذه التغييرات. على سبيل المثال، نموذج **تكامل Common Data Service** أصبح الآن **تكامل Microsoft Dataverse**.

لمعرفة المزيد حول تكامل Dynamics 365 Human Resources مع Microsoft Dataverse، راجع [تكوين تكامل Microsoft Dataverse ](./hr-admin-integration-common-data-service.md) و[تكوين جداول Microsoft Dataverse الظاهرية](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="updates-to-service-deployment"></a>التحديثات المطلوبة لنشر الخدمة

بدءًا من تاريخ 22 فبراير، 2021، نقوم بتعديل نشر تحديث الخدمة الإقليمي. ستتضمن التسويات تدوير الأمر الذي تتلقى فيه المناطق العمومية التحديثات الخاصة بخدمة الموارد البشرية والتعديلات في وقت الانتظار بين مراحل التحديث. ستجعلنا هذه التغييرات أكثر انسجامًا مع ممارسات التوزيع الآمنة (SDP) لتحسين استقرار الخدمة والجودة والدعم.

سنستمر في اتباع وتيرة التوزيع على أسبوعين. ومع ذلك، قد يلاحظ العملاء أن التحديثات يتم تطبيقها عادة على بيئات الموارد البشرية الخاصة بهم في يوم مختلف من دورة الأسبوعين من الإصدارات السابقة.

لمزيد من المعلومات حول عملية تحديث الخدمة، راجع [عملية التحديث](./hr-admin-setup-update-process.md).

## <a name="see-also"></a>راجع أيضًا

[ما الجديد أو المتغير في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 1 من إصدار Dynamics 365 Human Resources  2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]