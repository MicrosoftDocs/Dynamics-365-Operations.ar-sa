---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources ‏(5 أبريل 2021)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 5 أبريل 2021.
author: marcelbf
ms.date: 04/05/2021
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
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ffb1d8966cb7e41a7032c6d4449b9e332c0e4703
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890591"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-5-2021"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources ‏(5 أبريل 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة أو على وشك القدوم في Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.4074.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزات التالية بشكل عام مع هذا الإصدار.

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| تقييد الموظفين من تحرير تفاصيل جهة اتصال العمل | [تقييد الموظفين من تحرير تفاصيل جهة اتصال العمل](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [تقييد تحرير المعلومات الشخصية](./hr-employee-self-service-restrict-editing.md)|

### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. قد نقوم بتحديث هذا الموضوع لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذا الموضوع في البداية.

| رقم الإصدار | إصدار |  الوصف |
| --- | --- | --- |
| 550852 | لا يتحقق زر **الموافقة** من صحة الحقول الإلزامية التي تم تعيينها على نموذج **المراجعة**. | عندما تقوم بتعيين حقل في نموذج **المراجعة‏‎** على أنه إلزامي وتنشر التغييرات لدور المدير، لا يتم التحقق من صحة النموذج كما هو متوقع. |
| 559564 | تصدر إجراءات العامل السابقة لتغيير التعويض الثابت رسالة خطأ للمستخدمين الذين تم إنهاء خدمتهم. | يصدر اجراء عامل لتعويض الموظف الذي تم إنهاء خدمته رسالة خطأ. بعد إنهاء خدمة أحد الموظفين، يصدر اجراء العامل للترقية قبل إنهاء خدمته رسالة خطأ. |
| 560074 | عدم تصفية المنسدلة لفئة التوظيف على **نوع العامل** وتعرض فئات للموظفين والمقاولين. | على نموذج **الموظف**، يجب على القائمة المنسدلة **فئة التوظيف** إظهار فئات الموظفين أو المقاولين، بالاستناد إلى نوع العامل الموظف. |
| 567388 | عدم مزامنة بعض المعلومات الخاصة بالموظفين الذين تم إنشاؤهم مؤخرًا على الجدول **cdm_worker** في Dataverse. | عند إنشاء سجل موظف جديد، ستتم مزامنة السجل الجديد مع الجدول **cdm_worker** في Dataverse، ولكن لن يتم تضمين جميع الخصائص في سجل Dataverse. |
| 563837 | ظهور الميزات غير المتوفرة في Human Resources. | يظهر عدد كبير من الميزات التي لا تنطبق على Human Resources في إدارة الميزات. تمت الآن إزالة هذه الميزات من قائمة الميزات المتاحة لتمكينها في Human Resources. |

## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| مساحة عمل إدارة المزايا | [مساحة عمل إدارة المزايا (معاينة)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [مساحة عمل إدارة المزايا](hr-benefits-management-workspace.md) |

## <a name="coming-soon"></a>قريبًا

| الميزة | تفاصيل |
| --- | --- |
| المهارات التي تم إدخالها بواسطة مدير للموظفين يمكن اعتمادها تلقائيًا من خلال سير عمل | قريبًا. |
| Platform update 10.0.17 (41) | تمت جدولة تحديث النظام الأساسي 10.0.17 بحيث يبدأ نشره مع الإصدار التالي في 19 أبريل 2021. لمزيد من المعلومات، راجع [تحديثات النظام الأساسي للإصدار 10.0.17 من تطبيقات Finance and Operations (أبريل 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md). |

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>راجع أيضًا

[ما الجديد أو المتغير في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 1 من إصدار Dynamics 365 Human Resources  2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]