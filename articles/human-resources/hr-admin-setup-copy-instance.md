---
title: نسخ مثيل
description: يمكنك استخدام Microsoft Dynamics Lifecycle Services (LCS) لنسخ قاعدة بيانات Microsoft Dynamics 365 Human Resources إلى بيئة وضع الحماية.
author: andreabichsel
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 48fef68dc3e5935f0032ca006840202b53d577e06e5376ead0b66eca2a9c36bb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740829"
---
# <a name="copy-an-instance"></a>نسخ مثيل

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يمكنك استخدام Microsoft Dynamics Lifecycle Services (LCS) لنسخ قاعدة بيانات Microsoft Dynamics 365 Human Resources إلى بيئة وضع الحماية. إذا كان لديك بيئة وضع حماية أخرى، يمكنك أيضًا نسخ قاعدة البيانات من تلك البيئة إلى بيئة وضع حماية مستهدفة.

لنسخ مثيل، ضع التلميحات التالية في الاعتبار:

- يجب أن يكون مثيل Human Resources الذي ترغب في استبداله بيئة وضع الحماية.

- يجب أن تكون البيئات التي تقوم بالنسخ منها وإليها في نفس المنطقة. لا يُمكنك النسخ عبر المناطق.

- يجب أن تكون مسؤولًا في البيئة الهدف بحيث يُمكنك تسجيل الدخول إليها بعد نسخ المثيل.

- عند نسخ قاعدة Human Resources، لا تقوم بنسخ العناصر (التطبيقات أو البيانات) المُضمنة في بيئة Microsoft Power Apps. للحصول على معلومات حول كيفية نسخ العناصر في بيئة Power Apps، راجع [نسخ بيئة ](/power-platform/admin/copy-environment). يجب أن تكون بيئة Power Apps التي تريد استبدالها بيئة وضع الحماية. يجب أن تكون مسؤول مستأجر عمومي لتغيير بيئة انتاج Power Apps إلى بيئة حماية. لمزيد من المعلومات حول تغيير بيئة Power Apps، راجع [تبديل مثيل](/dynamics365/admin/switch-instance).

- إذا قمت بنسخ مثيل إلى بيئة الحماية الخاصة بك وترغب في دمج بيئة الحماية مع Dataverse ، فمن ثم يجب عليك إعادة تطبيق الحقول المخصصة على جداول Dataverse. راجع [تطبيق الحقول المخصصة علي Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).

## <a name="effects-of-copying-a-human-resources-database"></a>تأثيرات نسخ قاعدة بيانات Human Resources

تحدث الأحداث التالية عندما تقوم بنسخ قاعدة بيانات Human Resources:

- تؤدي عمليه النسخ إلى مسح قاعده البيانات الموجودة في البيئة الهدف. بعد اكتمال عملية النسخ، لا يُمكنك استرجاع قاعدة البيانات الموجودة.

- لن تكون البيئة الهدف متوفرة حتى اكتمال عملية النسخ.

- لا يتم نسخ المستندات الموجودة في مخزن البيانات الثنائية الكبيرة الحجم لـ Microsoft Azure من بيئة إلى أخرى. ونتيجة لذلك، لن يتم نسخ أي مستندات وقوالب مرفقة وسوف تظل في البيئة المصدر.

- لن تتوفر كافة المستخدمين باستثناء المستخدمين الذين لديهم دور أمان "مسؤول النظام" وحسابات مستخدم الخدمة الداخلية الأخرى. يُمكن للمستخدم المسؤول حذف البيانات أو جعلها مبهمة قبل السماح لمستخدمين آخرين العودة إلى النظام.

- أي مستخدم بدور الأمان "مسؤول النظام" يجب عليه إجراء تغييرات التكوينات المطلوبة، مثل إعادة توصيل النقاط النهائية للتكامل إلى خدمات أو عناوين URL مُعينة.

## <a name="copy-the-human-resources-database"></a>نسخ قاعدة بيانات Human Resources

لإكمال هذه المهمة، يجب عليك أولًا نسخ مثيل، ثم تسجيل الدخول إلى مركز مسؤول Microsoft Power Platform لنسخ بيئة Power Apps الخاصة بك.

> [!WARNING]
> عندما تقوم بنسخ مثيل، يتم مسح قاعدة البيانات في المثيل الهدف. المثيل الهدف غير متوفر في أثناء هذه العملية.

1. قم بتسجيل الدخول إلى LCS، وحدد مشروع LCS الذي يحتوي على المثيل الذي ترغب في نسخه.

2. في مشروع LCS، حدد تجانب **"إدارة تطبيق Human Resources**.

3. حدد المثيل المراد نسخه، ثم حدد **نسخ**.

4. في جزء المهام **نسخ مثيل**، حدد المثيل المراد استبداله، ثم حدد **نسخ**. انتظر حتي يتم تحديث قيمة حقل **نسخ الحالة** إلى **مكتمل**.

   ![[حدد مثيلًا لاستبداله.](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. حدد **Power Platform**، وقم بتسجيل الدخول إلى مركز مسؤول Microsoft Power Platform.

   ![[تحديد Power Platform.](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. حدد بيئة Power Apps المراد نسخها، ثم حدد **نسخ**.

7. عند اكتمال عمليه النسخ ، قم بتسجيل الدخول إلى المثيل الهدف، وتمكين تكامل Dataverse. لمزيد من المعلومات والتعليمات، راجع [تكوين تكامل Dataverse ](./hr-admin-integration-common-data-service.md).

## <a name="data-elements-and-statuses"></a>عناصر البيانات والحالات

لا يتم نسخ عناصر البيانات التالية عندما تقوم بنسخ مثيل Human Resources:

- عناوين البريد الكتروني في الجدول **LogisticsElectronicAddress**

- سجل الوظيفة الدفعية في الجداول **BatchJobHistory** و **BatchHistory** و **BatchConstraintHistory**. 

- كلمة مرور البروتوكول البسيط لنقل رسائل البريد (SMTP) في جدول **SysEmailSMTPPassword**.

- خادم ترحيل SMTP في الجدول **SysEmailParameters** 

- إعدادات إدارة الطباعة في جداول **PrintMgmtSettings** و **PrintMgmtDocInstance** 

- سجلات البيئة المُحددة في جداول **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig**, و **BatchServerGroup** 

- مرفقات المستندات في جدول DocuValue. تتضمن هذه المرفقات أي قوالب Microsoft Office تم استبدالها في البيئة المصدر

- سلسلة الاتصال في جدول **PersonnelIntegrationConfiguration** 

لم يتم نسخ بعض هذه العناصر لأنها خاصة ببيئة معينة. تتضمن الأمثلة سجلات **BatchServerConfig** و **SysCorpNetPrinters**.  لا يتم نسخ العناصر الأخرى بسبب حجم تذاكر الدعم. على سبيل المثال:

- يجوز إرسال رسائل بريد إلكتروني مُكررة لأن SMTP لا يزال ممُكنًا في بيئة (حماية) اختبار قبول المستخدم.

- قد يتم إرسال رسائل تكامل غير صحيحة لأن الوظائف الدفعية لا تزال ممكنة.

- قد يتم تمكين المستخدمين قبل أن يتمكن المسؤولون من تنفيذ إجراءات تنظيف ما بعد التحديث.

بالإضافة إلى ذلك، تتغير الحالات التالية عند نسخ مثيل:

- يتم تعيين كافة المستخدمين باستثناء أولئك الذين لديهم دور الأمان "مسؤول النظام" إلى **معطل**.

- يتم تعيين كافة الوظائف الدفعية، باستثناء بعض وظائف النظام، إلى **اقتطاع**.

## <a name="environment-admin"></a>مسؤول البيئة

يتم استبدال كافة المستخدمين في بيئة الحماية الهدف، بما في ذلك المسؤولين، بالمستخدمين في البيئة المصدر. قبل نسخ مثيل، تأكد من أنك مسؤول في البيئة المصدر. إذا لم تقم بذلك، فلن تتمكن من تسجيل الدخول إلى بيئة الحماية الهدف بعد اكتمال عملية النسخ.

يتم تعطيل كافة المستخدمين غير المسؤولين في بيئة الحماية الهدف لمنع تسجيلات الدخول غير المرعوب فيها في بيئة الحماية. يمكن للمسؤولين إعادة تمكين المستخدمين عند الحاجة.

## <a name="apply-custom-fields-to-dataverse"></a>تطبيق الحقول المخصصة على Dataverse

إذا قمت بنسخ مثيل إلى بيئة الحماية الخاصة بك وترغب في دمج بيئة الحماية مع Dataverse ، فمن ثم يجب عليك إعادة تطبيق الحقول المخصصة على جداول Dataverse.

بالنسبة لكل حقل مخصص معروض في جداول Dataverse، قم بالخطوات التالية:

1. انتقل إلى الحقل المخصص، وحدد **تحرير**.

2. قم بإلغاء تحديد حقل **ممّكن** لكل كيان cdm_* تم تمكين الحقل المخصص فيه. 

3. حدد **تطبيق التغييرات**.

4. حدد **تحرير** مرة أخرى.

5. حدد حقل **ممّكن** لكل كيان cdm_* تم تمكين الحقل المخصص فيه. 

6. حدد **تطبيق التغييرات** مرة أخرى.

تطالبك عمليات إلغاء التحديد وتطبيق التغييرات وإعادة التحديد وإعادة تطبيق التغييرات تحديث المخطط في Dataverse لتضمين الحقول المخصصة.

لمزيد من المعلومات حول الحقول المخصصة، راجع [‏‫إنشاء حقول مخصصة والعمل باستخدامها‬](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).

## <a name="see-also"></a>راجع أيضًا

[تزويد Human Resources](hr-admin-setup-provision.md)</br>
[إزالة مثيل](hr-admin-setup-remove-instance.md)</br>
[تحديث العملية](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
