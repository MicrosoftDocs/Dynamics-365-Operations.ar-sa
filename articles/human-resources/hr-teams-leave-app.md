---
title: إدارة طلبات الإجازة في Teams
description: يوضح هذا الموضوع كيفية طلب إجازة في تطبيقات Dynamics 365 Human Resources في Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0fbf44fe35af3147fd5fb478b6cbfc5a5d0b109d
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766750"
---
# <a name="manage-leave-requests-in-teams"></a>إدارة طلبات الإجازة في Teams

[!include [banner](includes/preview-feature.md)]

يتيح لك تطبيق Microsoft Dynamics 365 Human Resources في Microsoft Teams طلب إجازة بسرعة وعرض معلومات رصيد إجازاتك مباشرة في Microsoft Teams. ويمكنك التفاعل مع روبوت لطلب المعلومات. توفر علامة التبويب **إجازة** مزيدًا من المعلومات التفصيلية.

## <a name="install-the-app"></a>تثبيت التطبيق

يمكنك العثور على تطبيق Human Resources في متجر Teams.

1. في Microsoft Teams، حدد علامة القطع.

   ![علامة القطع لتطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. ابحث عن Dynamics 365 Human Resources، ثم حدد تجانب **Human Resources**.

   ![تجانب HR لتطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. حدد زر **إضافة** لتثبيت التطبيق.

   ![تثبيت تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-in-store.png)

إذا لم يقم التطبيق بتسجيل الدخول تلقائيًا، حدد علامة التبويب **إعدادات** لتسجيل الدخول.

![علامة تبويب الإعدادات في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> إذا كنت لا ترى مربع حوار تسجيل الدخول، فتحقق من إعدادات المستعرض للسماح بالإطارات المنبثقة. 

إذا كان لديك حق الوصول إلى أكثر من مثيل واحد من Human Resources، فيمكنك تحديد البيئة التي ترغب في الاتصال بها في علامة تبويب **إعدادات**.

> [!WARNING]
> لا يدعم التطبيق حاليًا دور أمان مسؤول النظام، وسيعرض رسالة خطأ إذا قمت بتسجيل الدخول باستخدام حساب مسؤول نظام. لتسجيل الدخول باستخدام حساب مختلف، في علامة تبويب **الإعدادات**، حدد زر **تبديل الحسابات**، ثم قم بتسجيل الدخول باستخدام حساب مستخدم ليس لديه امتيازات مسؤول النظام.
 
## <a name="use-the-bot"></a>استخدام الروبوت

بعد تثبيت التطبيق، تظهر رسالة ترحيب تسمح لك بمعرفة أنواع الإجراءات التي يمكن للروبوت القيام بها بالنيابة عنك.

![رسالة الترحيب من روبوت تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> عند التفاعل الأول مع الروبوت، قد تحتاج إلى تسجيل الدخول. إذا كنت لا ترى مربع حوار تسجيل الدخول، فتحقق من إعدادات المستعرض للسماح بالإطارات المنبثقة.

يمكنك مطالبة الروبوت بما يلي:

- إظهار معلومات رصيد الإجازات لكل نوع من أنواع الإجازات التي قمت بتسجيلها.

   ![إظهار الأرصدة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- قم بعرض تفاصيل إضافية حول نوع إجازة معين.

   ![إظهار التفاصيل في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot-details.png)

- ابدأ طلب إجازة لك.

   ![طلب إجازة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot-request.png)
 
بعد بدء طلب إجازة، يمكنك ضبط الأيام داخل البطاقة.

![تحرير طلب في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot-edit.png)
 
عندما تنتهي من إدخال المعلومات، حدد **إرسال** لإرسال الطلب للموافقة. يمكنك أيضًا تحديد **حفظ كمسودة** للعودة إلى المسودة لاحقًا.

![تقديم طلب في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a>إدارة إجازتك في Teams

تتيح لك علامة التبويب **إجازة** عرض ما يلي:

- معلومات الرصيد لكل نوع من أنواع الإجازات التي قمت بتسجيلها

- طلبات الإجازة القادمة

- طلبات الإجازة

- مسودات طلبات الإجازات

![علامة تبويب الإجازة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>إنشاء طلب جديد

1. لإنشاء طلب إجازة جديد، حدد **طلب جديد**.

   ![طلب جديد في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. أدخل اليوم أو الأيام التي تريد أخذها إجازة، ثم حدد **إضافة**.

   ![إضافة إجازة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. إن أمكن، أدخل رمز السبب. وقم أيضا بإدخال أية تعليقات وإضافة أية مرفقات.

4. عند الانتهاء من إدخال المعلومات، اكتب **إرسال** لإرسال الطلب للموافقة. يمكنك أيضًا كتابة **حفظ كمسودة** للعودة إليه لاحقًا.

### <a name="manage-draft-requests"></a>إدارة مسودات الطلبات

1. حدد علامة التبويب **المسودات**.

   ![علامة تبويب المسودات في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. حدد القلم الرصاص لتحرير الطلب، أو حدد سلة المهملات لكي يمكنك حذف الطلب.

3. قم بإجراء أية تغييرات ضرورية. عند الانتهاء من إدخال المعلومات، اكتب **إرسال** لإرسال الطلب للموافقة. يمكنك أيضًا تحديد **حفظ كمسودة** للعودة إلى المسودة لاحقًا.

   ![تحرير مسودة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="teams-notifications"></a>إعلامات Teams

عندما تقوم أنت أو عامل أنت القائم بالموافقة بالنسبة له بإرسال طلب إجازة، ستتلقى إعلامًا في تطبيق Human Resources في Teams. يمكنك تحديد الإعلام لعرضه. تظهر الإعلامات أيضًا في منطقة **الدردشة**.

إذا كنت القائم بالموافقة، فيمكنك تحديد **موافقة** أو **رفض** في الإعلام. يمكنك أيضًا توفير رسالة اختيارية.

![إعلام طلب إجازة في تطبيق Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="view-your-teams-leave-calendar"></a>عرض تقويم الإجازات لفريقك

إذا كنت مديرًا مسؤولاً عن مرؤوسين مباشرين، فيمكنك عرض إجازات الفريق الموافق عليها والمعلقة.

1. في تطبيق Human Resources في Teams، حدد **إجازة**.

2. حدد **تقويم الفريق**.

   ![عرض التقويم في تطبيق Human Resources Teams](./media/hr-teams-leave-app-view-calendar.png)

يعرض التقويم إجازات المرؤوسين المباشرين الموافق عليها والمعلقة.

![تقويم الإجازات في تطبيق Human Resources Teams](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a>إشعار الخصوصية

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>خدمة الفهم الذكي للغة (LUIS) من Microsoft.

باستخدام روبوت Dynamics 365 Human Resources في Microsoft Teams، يتم تحليل الإدخالات النصية للمستخدم لفهم الاستعلام/المقصد الأساسي. يتم توجيه إدخال المستخدم مثل "البحث في حساب Contoso" إلى إحدى الخدمات المعرفية من Microsoft تسمى التي خدمة الفهم الذكي للغة (LUIS). أقرا المزيد حول خدمة LUIS  [هنا](https://www.luis.ai/). تزيل خدمة LUIS الغموض أو تفهم المقصد من إدخال المستخدم (في هذه الحالة، يتمثل المقصد في العثور على المعلومات) والكيان المستهدف (وفي هذه الحالة الكيان المقصود هو الحساب المسمى Contoso). يتم بعد ذلك تمرير هذه المعلومات إلى  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) من Microsoft الذي يتفاعل مع البيانات من Dynamics 365 Human Resources ويسترد المعلومات المطلوبة لاستعلام المستخدم. 

من خلال التثبيت والسماح بالوصول لاستخدام الروبوت، فإنك توافق على السماح لخدمة LUIS وإطار عمل روبوت Azure بمعالجة القصد من الإدخال، والذي ينتج عنه تجربة محسنة للمحادثة مع المستخدم. قد يكون لدي خدمةLUIS و إطار عمل روبوت Azure مستويات متنوعة من التوافق مقارنة بـ Dynamics 365 Human Resources. في حين أن خدمة LUIS يمكنها الوصول إلى استعلامات المستخدمين فقط ولم يتم تصميمها ليتم ربطها ببيانات أو حساب Dynamics 365 Human Resources للمستخدم، لكن يمكن لمستخدم روبوت Dynamics 365 Human Resources إدخال استعلام طواعية يحتوي على بيانات العميل أو البيانات الشخصية أو البيانات الأخرى، وكذلك يمكن يتم إرسال محتويات الاستعلام إلى خدمة LUIS وإطار عمل روبوت Azure. 

يتم الاحتفاظ بمحتويات استعلامات المستخدم ورسائله في نظام LUIS لمدة 30 يومًا بحد أقصى، ويتم تشفيرها عند تثبيت البيانات، ولا يتم استخدامها في التدريب أو تحسين الخدمة. أقرا المزيد حول الخدمات المعرفية  [هنا](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

لإدارة إعدادات المسؤول للتطبيقات في Microsoft Teams، انتقل إلى [مركز إدارة Microsoft Teams](https://admin.teams.microsoft.com/).

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a>شبكة الأحداث في Microsoft Azure وMicrosoft Teams

عند استخدام ميزة الإعلامات لتطبيق Dynamics 365 Human Resources في Teams، ستتدفق بعض بيانات العملاء خارج المنطقة الجغرافية التي يتم فيها توزيع خدمة Human Resources للمستأجر. يرسل Dynamics 365 Human Resources تفاصيل طلب الإجازة الخاص بالموظف وتفاصيل سير العمل إلى شبكة الأحداث في Microsoft Azure وMicrosoft Teams قد يتم تخزين هذه البيانات لمدة تصل إلى 24 ساعة وتتم معالجتها في الولايات المتحدة، ويتم تشفيرها أثناء نقلها وتخزينها، ولا تستخدم من قبل Microsoft أو الشركات المعالجة الفرعية لأغراض التدريب أو إدخال تحسينات على الخدمة.

## <a name="see-also"></a>راجع أيضًا

[تنزيل وتثبيت Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[مركز تعليمات Microsoft Teams](https://support.office.com/teams)</br>
[تطبيق Human Resources في Teams](hr-admin-teams-leave-app.md)
