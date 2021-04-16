---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources 28 يناير 2021
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 28 يناير 2021.
author: marcelbf
ms.date: 01/28/2021
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
ms.author: marcelbf
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 36509cc5663073fd1e3b7f41a600c7816bfbdff6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791235"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-28-2021"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources 28 يناير 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة أو على وشك القدوم في Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 1](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.3906.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزات التالية بشكل عام مع هذا الإصدار.

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| دمج أكواد أسباب الميزات في مساحة عمل **إدارة العاملين** | -- | [إعداد أكواد السبب](hr-benefits-setup-reason-codes.md) |

### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. قد نقوم بتحديث هذا الموضوع لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذا الموضوع في البداية.


| رقم الإصدار | إصدار |  الوصف |
| --- | --- | --- |
| 539456 | يظهر التقويم نوع الأجازة في نص التحليق عند تمكين المعلمة **إظهار الغياب فقط دون تفاصيل**. | عند تمكين خيار **إظهار الغياب بدون تفاصيل فقط**، يتم عرض تاريخ الطلب الآن عند التحليق. |
| 528907 | يؤدي منح حق الوصول إلى كيان قانوني في دور الموظف إلى عدم تكمن المديرين من رؤية نشاط رصيد الأجازات للموظفين في منطقة **فريقي** في الخدمة الذاتية للموظفين. |يسمح تعيين هذا الخيار الآن للمديرين متابعة الاطلاع على نشاط رصيد الأجازات. |
| 526280 | خطأ الأذونات في HcmWorkerEntity وHcmEmployeeEntity وHcmContractorEntity. | لم يتمكن المستخدمون الموجودون في دور مسؤول غير النظام من تصدير الكيانات المدرجة بسبب خطأ أذونات في الحقل NationalityCountryRegion. سيستمر المستخدمون في الاحتياج إلى الامتيازات التالية لتصدير هذه المعلومات: HcmWorkerEntityMaintain وHcmWorkerEntityView وHcmEmployeeEntityMaintain وHcmEmployeeEntityMaintain وHcmEmployeeEntityView وHcmContractorEntityMaintain وHCMContractorEntityView |
| 542147 | تصبح حقول **رقم حساب البنك** و **رقم التوجيه** إلزامية عند إضافة حساب بنكي عن طريق الخدمة الذاتية للموظف. | لقد أصلحنا الخطا حيث كانت الموظفون مطالبون بإدخال حقلي **رقم الحساب البنكي** و **رقم التوجيه** أثناء إضافة تفاصيل حساب البنك. ولم تعد هذه الحقول إلزامية عند حفظ معلومات الحساب البنكي الجديدة. |
| 543641 | لا يتم ملء الرمز البريدي بالتقارير الإلكترونية. | تم إصلاح خطأ حيث كان لا يتم ملء الكود البريدي بتقرير ACA لأكواد التغطية من L إلى Q. |
| 545402 | تمت إضافة تغيير التوجيه لملف UserBranding.js file لإزالة أخطاء 404. | ينبغي ألا يشاهد المستخدم الخطأ 404 في وحدة التحكم. |

## <a name="in-preview"></a>قيد المعاينة   

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| تطبيق Human Resources في Microsoft Teams | [تجربة إجازة وغياب الموظف في Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [تطبيق Human Resources في Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[إدارة طلبات الإجازة في Teams](hr-teams-leave-app.md) |
| عرض الإجازات عبر الشركات للمديرين | [عرض إجازات الموظفين عبر الشركات للمديرين](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [تكوين معلمات الإجازة والغياب](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |

## <a name="coming-soon"></a>قريبًا

| الميزة | تفاصيل |
| --- | --- |
| تأكيد البريد الإلكتروني لتسجيلات المزايا | سوف توفر الميزة خيار إرسال بريد إلكتروني للتأكيد إلى الموظفين عند تسجيل الخروج من تجربة تسجيل المزايا في الخدمة الذاتية للموظف. ستصبح هذه الميزة متاحة في الأول من فبراير. لمزيد من المعلومات، راجع [تكوين معلمات إدارة المزايا لكل شركة](hr-benefits-setup-parameters-per-company.md). |
| المهارات التي تم إدخالها بواسطة مدير للموظفين يمكن اعتمادها تلقائيًا من خلال سير عمل | قريبًا. |

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 1](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>تحديثات المصطلحات لـ Microsoft Dataverse

بدء من نوفمبر 2020، تمت إعادة تسمية Common Data Service إلى [Microsoft Dataverse](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro). راجع [الإعلانات الرسمية](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/)الموجودة على مدونة Power Apps لمعرفة المزيد. بالترابط مع تغيير هذا الاسم، تم تحديث بعض المصطلحات في Dataverse. علي سبيل المثال ،تم تعيير مصطلح *كيان* إلى مصطلح *جدول* و *حقل* إلى *عمود*. لمزيد من المعلومات، راجع [تحديثات المصطلحات](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

في هذا الإصدار، تم تحديث المصطلحات ذات الصلة بتكامل Dynamics 365 Human Resources مع Dataverse في كافة أنحاء التطبيق لتعكس هذه التغييرات. على سبيل المثال، نموذج **تكامل Common Data Service** أصبح الآن **تكامل Microsoft Dataverse**.

لمعرفة المزيد حول تكامل Dynamics 365 Human Resources مع Microsoft Dataverse، راجع [تكوين تكامل Microsoft Dataverse ](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service) و[تكوين جداول Microsoft Dataverse الظاهرية](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

## <a name="see-also"></a>راجع أيضًا

[ما الجديد أو المتغير في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 1 من إصدار Dynamics 365 Human Resources  2021](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]