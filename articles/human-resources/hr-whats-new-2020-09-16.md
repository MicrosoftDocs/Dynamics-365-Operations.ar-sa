---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (16 سبتمبر 2020)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 16 سبتمبر 2020.
author: jcart1106
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cd3424db6bf918b4041f6d12e5d840bc3a8dfef7
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061563"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (16 سبتمبر 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.3557. تشير الأرقام الموجودة بين أقواس إلى جانب بعض العناوين إلى أرقام دعم كمرجع في Lifecycle Services (LCS).

## <a name="included-in-this-release"></a>الميزات المضمنة في هذا الإصدار

-  [طرق العرض المحفوظة - التوفر العام](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br>- لمزيد من المعلومات، راجع [طرق العرض المحفوظة](../fin-ops-core/fin-ops/get-started/saved-views.md). 

- يتضمن النموذج **إجراءات المنصب** شبكة أبعاد محدّثة بالإضافة إلى مربع حوار جديد (469495).

- إذا قمت بتعيين الخيار **تقييد الوصول إلى معلومات العامل** إلى "نعم" في **الوصول المتقدم** في  **المعلمات المشتركة لـ Human resources**‬، تعرض الآن نماذج المزايا العاملين المناسبين فقط (393384).

- خيارات جديدة لإنشاء التقويم في كيان **WorkCalendar** ‏(477055):<br>- وقت الانتهاء الافتراضي<br>- وقت البدء الافتراضي<br>- هل يوم الجمعة يوم عمل<br>- هل يوم الإثنين يوم عمل<br>- هل يوم السبت يوم عمل<br>- هل يوم الأحد يوم عمل<br>- هل يوم الخميس يوم عمل<br>- هل يوم الثلاثاء يوم عمل<br>- هل يوم الأربعاء يوم عمل<br>- معرف إجازة تقويم العمل

- يتضمن الآن الكيان **LeaveBankTransactionV1** كود السبب (477823).

- يمكنك الآن حفظ تسجيلات المهمة (492923).

- يتم الآن نشر البيانات بنجاح من **HCMWorkerContactEntity** (427620).

- تظهر الآن علامة التبويب السريعة **التعويض** لنوع العامل المقاول في النموذج **إجراءات العامل** (482494).

- الحقلان **المستوى** و **الخطة** إلزاميان الآن إذا قمت بتعيين **التعويض الثابت**. تظهر رسالة خطأ إذا تركت هذه الحقول فارغة (482497).

- الحقل **نوع الخطة** في **المزايا** هو الآن قائمة منسدلة (488768).

- يتلقى مسؤولو النظام الآن إعلامًا إذا تم حذف حقل مخصص من Human Resources (481408).

- أثناء عملية إنهاء خدمات الموظف، يتصرف Human Resources كما هو متوقع، ولا يغيّر الشركة المحددة بعد أن يبدو وكأنه تم تأمينه (479877). 

- لم يعد بإمكان المدراء إضافة عمود رقمي من خلال التخصيص (485317).

- لن يعد بإمكان المدراء إزالة عامل تصفية نطاق البيانات من أرقام التعريف التي ستنتهي صلاحيتها (485321).

- عندما يكون الحقل **مسؤول أمام** فارغًا، تستمر تفاصيل المنصب في الظهور عند تمرير الماوس فوق المنصب (433328).

- بإمكان الموظفين الآن عرض معلومات خطة المزايا في خدمة الموظف الذاتية (481676).

- بإمكان الموظفين الآن رؤية كافة الدورات التدريبية المسجلة (429048).

- يمكنك الآن تقييد خيارات العرض لصفحة **الشهادات المهنية**. يمكنك تقييد خيارات العرض للكيان القانوني الحالي حسب  حالة العامل ونوع العامل (451501). 


## <a name="in-preview"></a>قيد المعاينة

### <a name="human-resources-app-in-teams"></a>تطبيق Human Resources في Teams

بإمكان الموظفين عرض وطلب الوقت بعيدًا عن العمل ضمن Microsoft Teams يمكنهم التفاعل مع روبوت لإنشاء طلبات الإجازات. لمزيد من المعلومات، راجع:

- [تجربة إجازة وغياب الموظف في Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬
- [تطبيق Human Resources في Teams](./hr-admin-teams-leave-app.md) في وثائق Human Resources

### <a name="human-resources-app-in-teams-preview-features"></a>تطبيق Human Resources في ميزات المعاينة لـ Teams
 
-  **الإخطارات**: سوف يتم إعلام المُرسلين والمعتمدين لطلبات الإجازات في تطبيق Human Resources في Teams. بإمكان الموافقين الموافقة على طلبات الإجازة أو رفضها. سيتم اعلام مقدمي الطلبات ما إذا تمت الموافقة على طلبهم أم رفضه. لمزيد من المعلومات، راجع:
   - [تجربة إجازة وغياب الموظف في Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬‬
   - [تمكين الإعلامات لتطبيق Human Resources في Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) في وثائق Human Resources
   - [تشغيل إعلامات Teams أو إيقاف تشغيلها لمستخدمين فرديين](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) في وثائق Human Resources
   - [إعلامات Teams](./hr-teams-leave-app.md#respond-to-teams-notifications) في وثائق Human Resources
   - [عرض تقويم إجازة الفريق](./hr-teams-leave-app.md#view-your-teams-leave-calendar) في وثائق Human Resources
 
- **تقويم إجازة المُدير**: بإمكان المدراء رؤية الإجازات الموافق عليها والمعلقة لمرؤوسيهم المباشرين في طريقة عرض التقويم. توفر طريقة العرض هذه طريقة سهلة في الفهم عند انقطاع أعضاء فريقهم عن العمل. لمزيد من المعلومات، راجع:
   - [تجربة إجازة وغياب الموظف في Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬‬
   - [عرض تقويم إجازة الفريق](./hr-teams-leave-app.md#view-your-teams-leave-calendar) في وثائق Human Resources

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>خيار التكوين لوضع عناصر العمل المعينة لي في قائمة (477004)

يتوفر الآن خيار جديد الآن لوضع قائمة **عناصر العمل التي تم تعيينها لي** في العمود الأيسر في لوحه المعلومات. مع هذا التغيير، تظهر كافة عناصر العمل وقوائم المهام في نفس الناحية. يمكنك تمكين هذه الوظيفة عن طريق تشغيل **المعاينة - تحسينات تجربة سير العمل** في إدارة الميزات. للحصول على مزيد من المعلومات حول تشغيل ميزات المعاينة، راجع [إدارة الميزات](hr-admin-manage-features.md).

تقوم هذه الميزة أيضًا بترقية خيارات سير العمل التي تظهر في نماذج إجراءات العاملين. تظهر خيارات سير العمل أيضًا أعلى علامة التبويب السريعة للإجراءات لتمكين الوصول السريع إليها. لمزيد من المعلومات، راجع: 

- [تحسينات في تجربة سير عمل إدارة المؤسسة والموظفين](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) في خطة الموجة 2 لإصدار 2020‬ لتطبيق Dynamics 365‬‬

![عناصر عمل تم تعيينها إلي.](./media/hr-workflow-work-items-assigned-to-me.png)

![الوصول السريع إلى عناصر سير العمل.](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a>تقويم الإجازة والغياب

يتضمن هذا الإصدار خيارات تقويم إضافية لتقويمات الإجازة والغياب. لمزيد من المعلومات، راجع [عرض تقويمات الفريق والشركة](./hr-employee-self-service-calendar.md).

## <a name="coming-soon"></a>قريبًا

### <a name="checklist-entities-included-in-dataverse"></a>تضمين كيانات قائمة الاختيار في Dataverse

ستتوفر كيانات قائمة الاختيار لعمليات الإلحاق وإلغاء الإلحاق والتحويلات وعمليات الأعمال قريبًا في Dataverse.

### <a name="benefits-management-reason-codes"></a>أكواد سبب إدارة الميزات

سيتم دمج أكواد سبب إدارة الميزات في وقت قريب مع أكواد السبب الموجودة في Human Resources. إذا قمت بإنشاء أكواد أسباب في إدارة الميزات تزيد عن 15 حرفًا، فيجب تغيير اسم كود السبب في نموذج **أكواد السبب** في إدارة الميزات بحيث تتكون من 15 حرفًا أو أقل. بعد تحديث الاسم، سيظهر كود السبب ضمن نموذج كود السبب في إدارة العاملين. سيتوفر هذا التغيير في المستقبل ولن يؤثر على الوظيفة الموجودة.

## <a name="see-also"></a>راجع أيضًا

[الميزات الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
