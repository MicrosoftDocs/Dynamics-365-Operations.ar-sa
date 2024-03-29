---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources‏ 19 نوفمبر 2021
description: توضح هذه المقالة الميزات الجديدة أو المتغيرة في إصدار Microsoft Dynamics 365 Human Resources المستقل بتاريخ 19 نوفمبر 2021.
author: marcelbf
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d3e08432a4ce4d73cd67ad839191abe9f6e691a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886062"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources‏ 19 نوفمبر 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة الميزات الجديدة أو المتغيرة أو الصادرة قريبًا في Microsoft Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [Dynamics 365 Human Resources الإصدار 2021 الموجة 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار إصلاحات الأخطاء التالية. يتم تطبيق التغييرات على رقم الإصدار 8.1.4591.

### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. يمكن أن نقوم بتحديث هذه المقالة لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذه المقالة بشكل مبدئي.

| رقم الإصدار | المشكلة | ‏‏الوصف‬ |
|---|---|---|
| 626178 | التنقل مفقود من لوحات العامل في **خدمة المدير الذاتية** | تم إصلاح هذه المشكلة الآن. يتوفر التنقل لعرض تفاصيل التقرير في **الخدمة الذاتية للمدير**. |
| 632573 | لا يوجد خطأ في التحقق من الصحة عند حفظ **دورة تدريبية** | تم إصلاح هذه المشكلة الآن. لا يزال مسموحًا، عند إنشاء دورة تدريبية مع تعيين **الحد الأدنى لعدد المشاركين** على أكبر من 0، بالحفظ حتى عندما يكون **الحد الأقصى لعدد المشاركين** هو 0. |
| 615955 | رسالة الخطأ "يجب ملء الحقل **الغرض** عند إنشاء موقع طلب توظيف جديد. | عند إنشاء عنوان لموقع طلب توظيف جديد، فإنه يظهر الخطأ: "يجب ملء الحقل 'الغرض'." ومع ذلك، لا يتوفر الحقل **الغرض** في الصفحة. |
| 620797 | خطأ الحقل **الجنس** مضلل | عندما لا يتم إدخال جنس لجهة اتصال شخصية، يعرض التقرير "النقر أو اللمس هنا لإدخال النص" – مضلل لأنه لا يمكن إدخال أي شيء في الحقل. |
| 620800 | ارتباط كشف الميزات مخفي | لا يمكن عرض بيان المزايا افتراضيًا في **خدمة الموظف الذاتية**.  تمت إضافة ارتباط إلى الجانب الأيمن من **الخدمة الذاتية للموظف** ضمن القسم **ارتباطات** |
| 629778 | مشكلة في الأداء مع تكامل CDS. | تسبب الطلب المتعلق بالتخويل في حدوث مشكلة في الأداء. |

## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول كيفية تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
|---|---|---|
| مساحة عمل إدارة المزايا | [مساحة عمل إدارة المزايا (معاينة)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [مساحة عمل إدارة المزايا](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>قريبًا
للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [Dynamics 365 وسحابات الصناعة: إصدار 2 لعام 2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
