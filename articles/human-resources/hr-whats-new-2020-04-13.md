---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources (13 أبريل 2020)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 13 أبريل 2020.
author: andreabichsel
ms.date: 04/13/2020
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
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 93873707703ce7148c353735ce1abce795796a5e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891999"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources (13 أبريل 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.3136. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.

## <a name="new-production-release-cadence"></a>وتيرة إصدار الإنتاج الجديدة

مع إصدار هذا الأسبوع، ينتقل إيقاع تحديث Human Resources من تحديث أسبوعي إلى تحديث كل أسبوعين. لضمان التوافق مع ممارسات النشر الآمنة، والمحافظة على أعلى معايير الاستقرار والموثوقية في الخدمة، أصبحت الآن عملية نشر تحديثات الخدمة في كل المناطق تتم كل أسبوعين. وقد تم وضع عمليات اختبار ومراقبة إضافية للتحقق من نجاح عملية النشر في كل مرحلة من مراحل العملية. لمزيد من المعلومات حول وتيرة الإصدار، راجع [عملية التحديث](hr-admin-setup-update-process.md).

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a>حقل "دقة التقريب" غير قابل للتحرير بعد تحديد نوع التقريب (435616)

مع هذا التغيير ، أصبح الآن حقل **دقة التقريب** متوفرًا بعد تحديث حقل **نوع التقريب**.

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a>يتعذر تحرير تاريخ انتهاء تسجيل الإجازة عندما لا تتضمن خطة الإجازة فترات استحقاق (413628)

يمكنك الآن تحرير تاريخ انتهاء التسجيل دون الحصول على رسالة الخطأ "يجب ملء حقل أساس تاريخ الاستحقاق‬".

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a>لا يتزامن كيان التوظيف مع Dataverse (430834)

يعمل هذا التغيير على تصحيح مشكلة عدم مزامنة بيانات التوظيف مع Dataverse بعد إضافة الأبعاد المالية. 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a>إزالة تعدد الأصول لكيان الفاصل الزمني لتقويم العمل‬ (431775)

يؤدي هذا التغيير إلى إزالة تعدد الأصول لكيان **الفاصل الزمني لتقويم العمل‬**.

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a>لا تعمل التصفية بواسطة الدالة CAST ضمن استدعاء OData على كيان تعيين العامل بالمنصب‬‏ (431699)

يتضمن هذا التحديث تغييرًا للسماح بالتصفية بواسطة الدالة CAST ضمن OData للكيان **تعيين العامل بالمنصب‬**.

## <a name="in-preview"></a>قيد المعاينة

## <a name="leave-suspension"></a>تعليق الإجازة

يمكنك تعليق الإجازة والغياب في Human Resources لأحد الموظفين. يؤدي تعليق الإجازة إلى إيقاف استحقاقات أنواع الإجازة المحددة. إذا حدث التعليق بعد معالجة الاستحقاق، فإن تعليق الإجازة يؤدي إلى إنشاء تسوية تناسبية لرصيد إجازات الموظف. لمزيد من المعلومات، راجع [تعليق الإجازة](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>قواعد نقل الإجازة

يمكنك تحديد نوع الإجازة المنقولة للأرصدة المنقولة حيث يتم تحويل تسويات النقل. على سبيل المثال، إذا قام أحد الموظفين بنقل إجازة من 10 أيام، يمكنك انتقاء نوع إجازة آخر لمدة العشرة أيام هذه. لمزيد من المعلومات، راجع [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>مشكلات معروفة

## <a name="employment-details-entity"></a>كيان تفاصيل التوظيف

تم تحديث كيان **تفاصيل التوظيف** بواسطة الحقول التالية:

- **تكرار الدفع**
- **معرف فئة التوظيف**
- **نوع التوظيف**
- **معرف نوع التوظيف**
- **حالة ميزة التوظيف**

يعتمد إعداد بيانات لهذه الحقول على إدارة المزايا التي يتم تمكينها في مساحة العمل **إدارة المزايا**. لا تقم بملء هذه الحقول أو تحديثها في كيان **تفاصيل التوظيف**، لأن ذلك سيؤدي إلى حدوث أخطاء أثناء الاستيراد.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>معاينة SharePoint لا تعمل في بعض البيئات

إذا كانت معاينة المستندات للمستندات المخزنة في SharePoint لا تعمل، جرب الإجراء التالي:

1. تحقق من وجود بريد إلكتروني مقترن بحساب المستخدم المسؤول. يمكنك عرض هذه المعلومات في صفحة **المستخدم**. إذا لم يتم إعداد البريد الإلكتروني، فأنت بحاجة إلى إضافة البريد الإلكتروني والموفر مع وظيفة Excel في OData. افتراضيًا، لا يكون عنوان البريد الإلكتروني موجودًا في تصميم Excel. ستحتاج إلى تحرير تصميم Excel، وإضافة جميع الحقول والتطبيق والتحديث. بمجرد إكمال هذه الخطوات، يمكنك تحديث حساب المسؤول.

2. بعد أن يحتوي حساب المسؤول على حساب بريد إلكتروني مقترن، قم بتسجيل الدخول إلى Human Resources باستخدام بيانات اعتماد المسؤول.

3. يمكنك الوصول إلى مرفق في SharePoint لبدء معاينة المستند.

4. قم بتسجيل الدخول باستخدام حساب مستخدم آخر له حق الوصول إلى المرفقات وتحقق من أن المعاينة تعمل كما هو متوقع.

## <a name="see-also"></a>راجع أيضًا

[المزايا الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]