---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources 8 مارس، 2021
description: يصف هذا الموضوع المزايا الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 8 مارس، 2021.
author: marcelbf
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7b1e616f9bc72ab1f30f69671c673241096f3276
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687857"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-08-2021"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources 08 مارس 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة أو على وشك القدوم في Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.4017.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزات التالية بشكل عام مع هذا الإصدار.

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| عرض الإجازات عبر الشركات للمديرين | [عرض إجازات الموظفين عبر الشركات للمديرين](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [تكوين معلمات الإجازة والغياب](./hr-leave-and-absence-parameters.md) |

### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. قد نقوم بتحديث هذا الموضوع لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذا الموضوع في البداية.

| رقم الإصدار | إصدار |  الوصف |
| --- | --- | --- |
| 486611 | يظهر الغياب في تقويم الإجازات عند تمكين **تعطيل الإجازة في كافة التقويمات** | في حالة تمكين **تعطيل الإجازة في كافة التقويمات**، فإنه لا يتم عرض معلومات الإجازة حينها عندما يتم تمكين ميزة تحسينات تقويم الإجازة والغياب.|
| 508972 | كيان حركة إجازة البنك والغياب ينقصه التحقق من صحة التسجيل | عند استخدام كيان حركة إجازة البنك والغياب، فإنه يتعذر استيراد الموظفين غير المسجلين في خطة بعد الآن. |
| 554854 | تحديث التقويم في أخطاء كيان التوظيف إذا كان الكيان القانوني الافتراضي في خيارات المستخدم مختلفًا | استخدام كيان التوظيف لتحديث التقويم لموظف ما لم يعد يعطي خطأ إذا كان الكيان القانوني الافتراضي في خيارات المستخدم مختلفًا. |
| 558347 | يظهر الحقل "يتعذر إنشاء سجل في تكوينات النموذج (FormRunConfiguration)" عند تحميل صفحة البدء. | تتسبب التخصيصات في ظهور الخطأ الحقل "يتعذر إنشاء سجل في تكوينات النموذج (FormRunConfiguration)" عند تحميل صفحة البدء. |
| 557327 | مساحة عمل إدارة المزايا: تظهر الفجوة فوق الشبكة. | مشكلة تجربة المستخدم الثابتة مع فجوة غير مقصودة تظهر على حدود شبكة الجدول في مساحة عمل المزايا. |
| 557334 | مساحة عمل إدارة المزايا: يجب أن يظهر المربع المنسدل لتحديد **الفترة** في علامة التبويب **ملخص** فقط. | يظهر الآن المربع المنسدل لتحديد **الفترة** المزايا فقط عندما تكون علامة التبويب **ملخص** نشطة في مساحة عمل المزايا، وليس في تحديدات **نتائج العملية** و **الارتباطات**. |
| 557336 | مساحة عمل إدارة الميزات: يتم اقتطاع النص **فتح التسجيل باستخدام خطط مسحوبة** في طريقة عرض اللوحة | تم تغيير النص في طريقة عرض اللوحة إلى **خطط مسحوبة...فتح التسجيل** لتجنب اقتطاع السياق الضروري. |

## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| مساحة عمل إدارة المزايا | [مساحة عمل إدارة المزايا (معاينة)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [مساحة عمل إدارة المزايا](hr-benefits-management-workspace.md) |
| تقييد الموظفين من تحرير تفاصيل جهة اتصال العمل | [تقييد الموظفين من تحرير تفاصيل جهة اتصال العمل](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [تقييد تحرير المعلومات الشخصية](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>قريبًا

| الميزة | تفاصيل |
| --- | --- |
| المهارات التي تم إدخالها بواسطة مدير للموظفين يمكن اعتمادها تلقائيًا من خلال سير عمل | قريبًا. |

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>راجع أيضًا

[ما الجديد أو المتغير في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 1 من إصدار Dynamics 365 Human Resources  2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]