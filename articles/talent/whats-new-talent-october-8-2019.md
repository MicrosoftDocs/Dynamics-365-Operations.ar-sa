---
title: ما الجديد أو المتغير في Dynamics 365 Talent‏ (8 أكتوبر 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
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
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 159320dcbdf257862378b347172ef71832e293dc
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626052"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent‏ (8 أكتوبر 2019)

[!include [banner](includes/banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR

تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2542. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a>إزالة الميزات التي تفتح التسجيل من المعاينة العامة

بالتزامن مع إعلاننا الخاص بالاستثمارات الاستراتيجية المنشور في [مدونة التفوق العملي لتحسين core HR](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/)، تعمل Microsoft على إزالة الميزات التي تفتح ميزة التسجيل المعاينة العامة في 18 أكتوبر 2019. بدلاً من ذلك، سيتم إصدار وظيفة جديدة في المستقبل. لن يتم اعتماد استخدام الإنتاج للميزات التي تفتح ميزة التسجيل المتاحة حاليًا في المعاينة العامة. 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a>تكامل Common Data Service متوقف حاليًا بشكل افتراضي في الأحكام الجديدة (343675)
 
عند توفير بيئات جديده، تكامل Common Data Service متوقف في الوقت الحالي. وللحصول على المزيد من المعلومات، راجع قسم [تكوين تكامل Common Data Service](hr-common-data-service-integration.md)

### <a name="streamlined-employee-entry-and-navigation"></a>إدخال الموظفين والتنقل المبسط

تتوفر الآن وظيفة لإدخال الموظف والتنقل في كافة البيئات. لتشغيل هذه الميزة، انتقل إلى **إدارة النظام \> الارتباطات‬ \> الإعداد \> ‏‫محددات النظام‬ \>‏‫ميزات المعاينة**، وحدد **نموذج العامل المحسن والتنقل**. يتم حينئذ تشغيل الميزة لكافة المستخدمين. يمكنك إيقاف تشغيل هذا الخيار في اي وقت.

لمزيد من المعلومات، راجع [إدخال بيانات الموظف المبسطة](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry) في خطة الموجة 2 من إصدار Dynamics 365: 2019.

### <a name="issue-attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a>المشكلة: في Attract وOnboard يتم إنشاء عمال غير نشطين في Core HR (380517)

في إصدار هذا الأسبوع يتم تصحيح مشكلة إنشاء Attract وOnboard لعمال غير نشطين في Core HR.

### <a name="issue-the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a>المشكلة: يفشل سير العمل عند تسجيل دخول المدير إلى شركة أخرى أثناء إنهاء الموظف (346852)

لم يعد سير العمل يفشل بناءً على الكيان القانوني الذي قام المدير بتسجيل الدخول إليه.

### <a name="issue-missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a>المشكلة: معلومات مفقوده في HcmOnboardingWorkerChecklistTaskEntity (349591)

يتضمن هذا الإصدار معلومات إضافية في **HcmOnboardingWorkerChecklistTaskEntity**. فيما يلي بعض الأمثلة:

- **اسم المجموعة** عندما يكون النوع المعين هو **مجموعة**
- **اسم الموظف** عندما يكون النوع المعين هو **موظف**
- **اسم المدير** عندما يكون النوع المعين هو **مدير**

### <a name="issue-entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a>المشكلة: الكيانات غير مدرجة بترتيب أبجدي في إدارة Common Data Service (377414)

الكيانات مدرجة الآن بترتيب أبجدي في صفحة **إدارة CDS**.

### <a name="issue-changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a>المشكلة: يؤدي تغيير نوع التوظيف بتاريخ مستقبلي لا يسمح بتعيين مهمة (339958)

يسمح هذا التغيير بتعيينات المناصب عند تغيير أنواع العمال (على سبيل المثال، من الموظف إلى المقاول).

### <a name="issue-updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a>المشكلة: يعمل تحديث كيان حركة إجازة البنك في Common Data Service على إنشاء سجل جديد في Talent (352938)

يتم الآن تحديث حركة الإجازة عند إجراء تحديث على Common Data Service لحركات إجازة البنك.

### <a name="issue-the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a>المشكلة: عنوان المرفقات لعناصر الملاحظات يُظهر وصف الملاحظات (343765)

لم يعد وصف الملاحظات يظهر في عنوان المرفق.

### <a name="issue-compensation-workflow-comments-field-shows-incorrect-content-339297"></a>المشكلة: يُظهر حقل تعليقات سير عمل التعويض محتوى غير صحيح (339297)

يعرض هذا التغيير محتوي الحقل **HcmActionState.HcmWorkerActionComment.Comments%**.

### <a name="issue-workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a>المشكلة: WorkCalendarEntity وWorkCalendarDayEntity غير معروضين خلال OData (376329)

في هذا الإصدار، يتوفر كل من **WorkCalendarEntity‎**و **WorkCalendarDayEntity‎** حاليًا من خلال بروتوكول البيانات المفتوحة (OData).

### <a name="issue-hcmworkerentity-is-slow-when-odata-is-used-375221"></a>المشكلة: HCMWorkerEntity بطيء عند استخدام OData (375221)

تعمل التغييرات على تحسين أداء **HCMWorkerEntity** عند استخدام مصمم مصنفات Microsoft Excel.

### <a name="issue-manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a>المشكلة: يعرض إدخال دفتر يومية أداء المدير خطأ بعد حذف دفتر يومية الأداء وإنشاء واحد جديد (336061)

يعمل هذا الإصدار على تصحيح مشكلة تحدث بعد حذف دفتر يومية أداء ويتم إنشاء واحد جديد علي الفور بعد ذلك. يقوم هذا التصحيح بتغيير السلوك في الخدمة الذاتية للمدراء.

## <a name="coming-soon"></a>قريبًا

### <a name="print-performance-reviews"></a>طباعة مراجعات الأداء

راجع [‏‫طباعة مراجعات الأداء‬](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) في خطة الموجة 2 من إصدار Dynamics 365: 2019.
