---
title: ما الجديد أو المتغير في Dynamics 365 Talent‏ (21‏ يناير 2020)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e9dee64e94c904cfe07c6a7766f6a60b1d60a2db
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528103"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a>ما الجديد أو المتغير في Dynamics 365 Talent‏ (21‏ يناير 2020)

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract. أضفنا وظيفة إلى Attract لدعم آخر إعلان، [ببناء عامل زيادة في العمل مع Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/).

### <a name="download-environment-data"></a>تنزيل بيانات البيئة

يمكن للمسؤولين تنزيل بيانات البيئة الخاصة بهم. يتم تصدير البيانات بتنسيق JSON القياسي مع كافة المهام والمرشحات والتكوين الذي تم تصديره في ملف مضغوط من نوع zip. لمزيد من المعلومات، راجع [تصدير بيانات من Attract وOnboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

### <a name="restricting-access-to-environments-for-non-admin-users"></a>تقييد الوصول إلى البيئات للمستخدمين غير المسؤولين

يمكن للمسؤولين الآن تقييد الوصول إلى البيئة للمستخدمين غير المسؤولين. لا يمكن التراجع عن هذا الإجراء. لمزيد من المعلومات، راجع [تقييد الوصول إلى Attract](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract).

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

### <a name="exporting-onboarding-guides"></a>تصدير أدلة الإعداد

يمكن للمستخدمين الآن تصدير كافة دلائل الإعداد الخاصة بهم وقوالب إلحاق بتنسيق مستند Word. لمزيد من المعلومات، راجع [تصدير بيانات من Attract وOnboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2726. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a>آخر حقل للتعويض السنوية في نموذج التحقق من التوظيف غير متناسق (392092)

يتضمن هذا الإصدار تغييرا سيعرض آخر عمله بشكل متناسق استنادا إلى محدد الشركة في نموذج **التحقق من التوظيف**.

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a>يعرف بحقل تمت اضافته إلى بحث مستلم الملاحظات (407789)

عند توفير ملاحظات الأداء ، لا يوفر البحث عن العاملين معلومات كافيه لتحديد ما إذا كان سيتم إرسال الملاحظات إلى الشخص الصحيح. أضفنا عمودًا **معروفًا** للمساعدة في التعرف علي الاسم الفريد للموظف.
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a>تم إنشاء سجل HcmWorkerPayrollInfo دون الاقتران بعامل (394526)

يتضمن هذا الإصدار تغييرا لعدم كتابه سجلات HCMWorkerPayrollInfo دون الاشاره إلى الموظف.

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a>التمكن من تحرير القسم عند التنقل من التسلسل الهرمي للمنصب (341001)

وعند اعداد الأمان لرفض الوصول لتحرير الأقسام ، يتم تعطيل التحرير عند التنقل إلى نموذج **الأقسام** في كافة السيناريوهات.

## <a name="coming-soon"></a>قريبًا

سيتوفر حل Common Data Service قريبًا بالتغييرات التالية:

| ‏‏الوصف | التغيير |
| --- | --- |
| تغييرات كيان **الوظيفة/المنصب** | <ul><li>تم إضافة **منطقة التعويض**</li><li>تمت إضافة **الأبعاد المالية**</li></ul> |
| تغييرات كيان **العامل** | <ul><li>تمت إضافة **تسلسل الاسم**</li><li>تم إضافة **الأعمال من الصفحة الرئيسية**</li><li>تمت إضافة **اللغة**</li><li>تمت إضافة **تاريخ الأقدمية**</li><li>تمت إضاف **تاريخ التفعيل السنوي**</li><li>تمت إضافة **تاريخ التوظيف الأصلي**</li></ul> |
| تغييرات كيان **التوظيف** | <ul><li>تمت إضافة **الأبعاد المالية**</li><li>تمت إضافة **سبب الإنهاء**</li><li>تمت إعادة تسمية **تاريخ الإنهاء** من **تاريخ الانتقال**</li><li>تمت إضافة **تاريخ فترة الاختبار**</li></ul> |
| تغييرات كيان **عنوان العامل** | <ul><li>تمت إضافة **عنوان الشارع**</li><li>**سطر العنوان 1**، و **سطر العنوان 2**، و **سطر العنوان 3** المميز للإهلاك</li></ul> |
| كيانات إعداد التعويض المتغيرة الجديدة | <ul><li>**نوع خطة التعويض المتغير**</li><li>**خطة التعويض المتغيرة**</li><li>**قواعد الاستحقاق**</li><li>**مستوى خطة التعويض المتغير**</li></ul> |
| كيان **توظيف تقويم العامل** الجديد | <ul><li>تمت إضافة **كيان تقويم العمل**</li></ul> |
