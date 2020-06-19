---
title: نسخ مثيل
description: يمكنك استخدام Microsoft Dynamics Lifecycle Services (LCS) لنسخ قاعدة بيانات Microsoft Dynamics 365 Human Resources إلى بيئة وضع الحماية.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8385b7dfcd1d7294542c7f54f609b26b7988ac4
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431235"
---
# <a name="copy-an-instance"></a>نسخ مثيل

يمكنك استخدام Microsoft Dynamics Lifecycle Services (LCS) لنسخ قاعدة بيانات Microsoft Dynamics 365 Human Resources إلى بيئة وضع الحماية. إذا كان لديك بيئة وضع حماية أخرى، يمكنك أيضًا نسخ قاعدة البيانات من تلك البيئة إلى بيئة وضع حماية مستهدفة.

لنسخ مثيل، تحتاج إلى التأكد من التالي:

- يجب أن يكون مثيل Human Resources الذي ترغب في استبداله بيئة وضع الحماية.

- يجب أن تكون البيئات التي تقوم بالنسخ منها وإليها في نفس المنطقة. لا يُمكنك النسخ عبر المناطق.

- يجب أن تكون مسؤولًا في البيئة الهدف بحيث يُمكنك تسجيل الدخول إليها بعد نسخ المثيل.

- عند نسخ قاعدة Human Resources، لا تقوم بنسخ العناصر (التطبيقات أو البيانات) المُضمنة في بيئة Microsoft PowerApps. للحصول على معلومات حول كيفية نسخ العناصر في بيئة PowerApps، راجع [نسخ بيئة ](https://docs.microsoft.com/power-platform/admin/copy-environment). يجب أن تكون بيئة PowerApps التي تريد استبدالها بيئة وضع الحماية. يجب أن تكون مسؤول مستأجر عمومي لتغيير بيئة انتاج PowerApps إلى بيئة حماية. لمزيد من المعلومات حول تغيير بيئة PowerApps، راجع [تبديل مثيل](https://docs.microsoft.com/dynamics365/admin/switch-instance).

## <a name="effects-of-copying-a-human-resources-database"></a>تأثيرات نسخ قاعدة بيانات Human Resources

تحدث الأحداث التالية عندما تقوم بنسخ قاعدة بيانات Human Resources:

- تؤدي عمليه النسخ إلى مسح قاعده البيانات الموجودة في البيئة الهدف. بعد اكتمال عملية النسخ، لا يُمكنك استرجاع قاعدة البيانات الموجودة.

- لن تكون البيئة الهدف متوفرة حتى اكتمال عملية النسخ.

- لا يتم نسخ المستندات الموجودة في مخزن البيانات الثنائية الكبيرة الحجم لـ Microsoft Azure من بيئة إلى أخرى. وبالتالي، لن يتم نسخ أي مستندات وقوالب مرفقة وسوف تظل في البيئة المصدر.

- لن يكون جميع المستخدمين باستثناء المستخدم المسؤول وحسابات مستخدمين الخدمة الداخليين الأخرى متوفرة. بالتالي، يُمكن للمستخدم المسؤول حذف البيانات أو جعلها مبهمة قبل السماح لمستخدمين آخرين العودة إلى النظام.

- يجب على المستخدم المسؤول إجراء تغييرات التكوينات المطلوبة، مثل إعادة توصيل النقاط النهائية للتكامل إلى خدمات أو عناوين URL مُعينة.

## <a name="copy-the-human-resources-database"></a>نسخ قاعدة بيانات Human Resources

لإكمال هذه المهمة، يجب عليك أولًا نسخ مثيل، ثم تسجيل الدخول إلى مركز مسؤول Microsoft Power Platform لنسخ بيئة PowerApps الخاصة بك.

> [!WARNING]
> عندما تقوم بنسخ مثيل، يتم مسح قاعدة البيانات في المثيل الهدف. المثيل الهدف غير متوفر في أثناء هذه العملية.

1. قم بتسجيل الدخول إلى LCS، وحدد مشروع LCS الذي يحتوي على المثيل الذي ترغب في نسخه.

2. في مشروع LCS، حدد تجانب **"إدارة تطبيق Human Resources**.

3. حدد المثيل المراد نسخه، ثم حدد **نسخ**.

4. في جزء المهام **نسخ مثيل**، حدد المثيل المراد استبداله، ثم حدد **نسخ**. انتظر حتي يتم تحديث قيمة حقل **نسخ الحالة** إلى **مكتمل**.

   ![[تحديد مثيل لاستبداله](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. حدد **Power Platform**، وقم بتسجيل الدخول إلى مركز مسؤول Microsoft Power Platform.

   ![[تحديد Power Platform](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. حدد بيئة PowerApps المراد نسخها، ثم حدد **نسخ**.

7. عند اكتمال عمليه النسخ، قم بتسجيل الدخول إلى المثيل الهدف، وتمكين تكامل Common Data Service. لمزيد من المعلومات والتعليمات، راجع [تكوين تكامل Common Data Service ](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).

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

لم يتم نسخ بعض هذه العناصر لأنها خاصة ببيئة معينة. تتضمن الأمثلة سجلات **BatchServerConfig** و **SysCorpNetPrinters**.  لا يتم نسخ العناصر الأخرى بسبب حجم تذاكر الدعم. على سبيل المثال، يجوز إرسال رسائل البريد الإلكتروني المُكررة لأن SMTP لا يزال مُمكننًا في بيئة اختبار قبول المستخدم (الحماية)، وقد يتم إرسال رسائل تكامل غير صالحة لأن الوظائف الدفعية لا تزال ممكنة، ويجوز تمكين المستخدمين قبل أن يتمكن المسؤولون من تنفيذ إجراءات تنظيف ما بعد التحديث.

بالإضافة إلى ذلك، تتغير الحالات التالية عند نسخ مثيل:

- تم تعيين كافة المستخدمين باستثناء المسؤول إلى **مُعطل**.

- يتم تعيين كافة الوظائف الدفعية، باستثناء بعض وظائف النظام، إلى **اقتطاع**.

## <a name="environment-admin"></a>مسؤول البيئة

يتم استبدال كافة المستخدمين في بيئة الحماية الهدف، بما في ذلك المسؤولين، بالمستخدمين في البيئة المصدر. قبل نسخ مثيل، تأكد من أنك مسؤول في البيئة الهدف. إذا لم تقم بذلك، فلن تتمكن من تسجيل الدخول إلى بيئة الحماية الهدف بعد اكتمال عملية النسخ.

يتم تعطيل كافة المستخدمين غير المسؤولين في بيئة الحماية الهدف لمنع تسجيلات الدخول غير المرعوب فيها في بيئة الحماية. يمكن للمسؤولين إعادة تمكين المستخدمين عند الحاجة.
