---
title: تطبيق Human Resources في Teams
description: يقدم لك هذا الموضوع تطبيق Microsoft Dynamics 365 Human Resources في Microsoft Teams.
author: andreabichsel
manager: tfehr
ms.date: 09/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba520f873de5b20111f9134e87281bcdf4025785
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111341"
---
# <a name="human-resources-app-in-teams"></a>تطبيق Human Resources في Teams

[!include [banner](includes/preview-feature.md)]

يتيح تطبيق Microsoft Dynamics 365 Human Resources في Microsoft Teams للموظفين طلب إجازة بسرعة وعرض معلومات رصيد إجازاتهم في Microsoft Teams. ويمكن للموظفين التفاعل مع روبوت لطلب المعلومات. توفر علامة التبويب **إجازة** مزيدًا من المعلومات التفصيلية. علاوةً على ذلك، يمكنهم إرسال معلومات الأشخاص حول وقت الإجازة القادم في الفرق والدردشات خارج تطبيق Human Resources.

![روبوت تطبيق الإجازات لـ Human Resources في Teams](./media/hr-admin-teams-leave-app-bot.png)

![علامة تبويب الإجازة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![بطاقة طلب إجازة في Human Resources](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>التثبيت والإعداد

يمكنك العثور على تطبيق Human Resources في متجر Teams. للحصول على معلومات حول تثبيت تطبيق Teams، راجع [إدارة طلبات الإجازة في Teams](hr-teams-leave-app.md).

للحصول على معلومات حول إدارة أذونات التطبيق في Teams، راجع [إدارة نهج أذونات التطبيق في Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>تمكين الإعلامات لتطبيق Human Resources في Teams

إذا أردت أن يتلقى المستخدمون إعلامات تتعلق بطلبات الإجازات في تطبيق Teams، يجب عليك تمكين الإعلامات في Human Resources.

>[!NOTE]
>وحدهم المستخدمون الذين سجلوا دخولهم إلى Teams ويستخدمون تطبيق Human Resources سيتلقون إعلامات.

1. في Human Resources، حدد **إدارة النظام**.

2. حدد **الارتباطات**.

3. ضمن **الإعداد**، حدد **معلمات النظام**.

4. من علامة التبويب **عام**، قم بتعيين الخيار **تمكين الاعلامات لتطبيق Teams** إلى **نعم**.

   ![تمكين إعلامات تطبيق Teams في معلمات النظام](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. لتشغيل إعلامات Teams لجميع المستخدمين، حدد **نعم** عند المطالبة.

   ![تمكين إعلامات Teams لجميع المستخدمين](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>تشغيل إعلامات Teams أو إيقاف تشغيلها لمستخدمين فرديين

بعد تمكين الإعلامات لتطبيق Human Resources Teams، يمكنك تشغيل الإعلامات أو إيقاف تشغيلها لمستخدمين فرديين.

1. في Human Resources، حدد **إدارة النظام**.

2. حدد **الارتباطات**.

3. ضمن **المستخدمون**، حدد **خيارات المستخدم**.

4. حدد علامة التبويب **سير العمل**.

5. عيّن الخيار **تمكين الإعلامات لتطبيق Teams** إلى **نعم** لتمكين الإعلامات للمستخدم أو إلى **لا** لتعطيل الإعلامات للمستخدم.

   ![تمكين إعلامات تطبيق Teams في خيارات المستخدم على علامة تبويب سير العمل](./media/hr-admin-teams-leave-app-notifications.png)

6. حدد **حفظ**.

## <a name="known-issues"></a>مشكلات معروفة

| إصدار | الحالة |
| --- | --- |
| يصبح الرصيد غير صحيح عند إرسال إجازة لتاريخ مستقبلي. | التنبؤ غير متوفر بعد. يتم عرض الرصيد للتاريخ الحالي. |
| تعذر إلغاء طلب **قيد المراجعة**. | هذه الوظيفة غير مدعومة في الوقت الحالي وستتم إضافتها في إصدار مستقبلي. |
| يتم حساب معلومات الرصيد اعتبارًا من اليوم. | لا يعرض النظام حاليًا الأرصدة اعتبارًا من فترة الاستحقاق، حتى إذا تم تكوينه في معلمات الإجازة والغياب. |

## <a name="troubleshooting"></a>استكشاف الأخطاء وإصلاحها

إذا كان المستخدم يواجه مشكله في تسجيل الدخول أو باستخدام تطبيق فرق الموارد البشرية، حاول اتباع إرشادات استكشاف الأخطاء وإصلاحها. إذا كنت لا تزال تواجه مشاكل بعد استكشاف الأخطاء وإصلاحها، اتصل بالدعم. لمزيد من المعلومات، راجع [الحصول على الدعم](hr-admin-troubleshooting-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>لا يمكن التسجيل في تطبيق الموارد البشرية في الفرق

إذا قام مستخدم بالاتصال بك لأنه لا يمكنه تسجيل الدخول إلى التطبيق، تحقق من ان المستخدم لديه سجل موظف مقترن في الموارد البشرية.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>حدث خطا عند اعتماد طلبات المغادرة في تطبيق الموارد البشرية في الفرق

في حاله تلقي المستخدم خطا اثناء محاولة الموافقة علي طلبات الإجازات في تطبيق الفرق، قم باجراء خطوات استكشاف الأخطاء وإصلاحها التالية:

1. تحقق من ان حساب الفرق الخاص بهم هو نفسه الذي يستخدم للوصول إلى الموارد البشرية.

2. تحقق من انهم موافقون صالحون للطلب من خلال التحقق من إعدادات سير العمل للموافقة على المغادرة. لمزيد من المعلومات حول إنهاء مهام سير العمل، راجع [إنشاء سير عمل لطلب أجازه](hr-leave-and-absence-workflow.md).

## <a name="privacy-notice"></a>إشعار الخصوصية

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>خدمة الفهم الذكي للغة (LUIS) من Microsoft.

باستخدام روبوت Dynamics 365 Human Resources في Microsoft Teams، يتم تحليل الإدخالات النصية للمستخدم لفهم الاستعلام/المقصد الأساسي. يتم توجيه إدخال المستخدم مثل "البحث في حساب Contoso" إلى إحدى الخدمات المعرفية من Microsoft تسمى التي خدمة الفهم الذكي للغة (LUIS). أقرا المزيد حول خدمة LUIS  [هنا](https://www.luis.ai/). تزيل خدمة LUIS الغموض أو تفهم المقصد من إدخال المستخدم (في هذه الحالة، يتمثل المقصد في العثور على المعلومات) والكيان المستهدف (وفي هذه الحالة الكيان المقصود هو الحساب المسمى Contoso). يتم بعد ذلك تمرير هذه المعلومات إلى  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) من Microsoft الذي يتفاعل مع البيانات من Dynamics 365 Human Resources ويسترد المعلومات المطلوبة لاستعلام المستخدم. 

من خلال التثبيت والسماح بالوصول لاستخدام الروبوت، فإنك توافق على السماح لخدمة LUIS وإطار عمل روبوت Azure بمعالجة القصد من الإدخال، والذي ينتج عنه تجربة محسنة للمحادثة مع المستخدم. قد يكون لدي خدمةLUIS و إطار عمل روبوت Azure مستويات متنوعة من التوافق مقارنة بـ Dynamics 365 Human Resources. في حين أن خدمة LUIS يمكنها الوصول إلى استعلامات المستخدمين فقط ولم يتم تصميمها ليتم ربطها ببيانات أو حساب Dynamics 365 Human Resources للمستخدم، لكن يمكن لمستخدم روبوت Dynamics 365 Human Resources إدخال استعلام طواعية يحتوي على بيانات العميل أو البيانات الشخصية أو البيانات الأخرى، وكذلك يمكن يتم إرسال محتويات الاستعلام إلى خدمة LUIS وإطار عمل روبوت Azure. 

يتم الاحتفاظ بمحتويات استعلامات المستخدم ورسائله في نظام LUIS لمدة 30 يومًا بحد أقصى، ويتم تشفيرها عند تثبيت البيانات، ولا يتم استخدامها في التدريب أو تحسين الخدمة. أقرا المزيد حول الخدمات المعرفية  [هنا](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

لإدارة إعدادات المسؤول للتطبيقات في Microsoft Teams، انتقل إلى [مركز إدارة Microsoft Teams](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams وشبكة أحداث Azure وAzure Cosmos DB

عند استخدام تطبيق Dynamics 365 Human Resources في Microsoft Teams، قد تتدفق بعض بيانات العملاء خارج المنطقة الجغرافية التي يتم فيها توزيع خدمة Human Resources للمستأجر.

يرسل Dynamics 365 Human Resources تفاصيل طلب الإجازة الخاص بالموظف وتفاصيل سير العمل إلى شبكة الأحداث في Microsoft Azure وMicrosoft Teams قد يتم تخزين هذه البيانات لمدة تصل إلى 24 ساعة في شبكة أحداث Microsoft Azure وستتم معالجتها في الولايات المتحدة، ويتم تشفيرها أثناء نقلها وتخزينها، ولا تستخدم من قبل Microsoft أو الشركات المعالجة الفرعية لأغراض التدريب أو إدخال تحسينات على الخدمة. لمعرفة مكان تخزين البيانات في Teams، الرجاء مراجعة: [موقع البيانات في Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)

اثناء التحدث مع روبوت الدردشة في تطبيق Human Resources، قد يتم تخزين محتوى المحادثة في Azure Cosmos DB وإرساله إلى Microsoft Teams. قد يتم تخزين هذه البيانات في Azure Cosmos DB لمدة 24 ساعة وقد تتم معالجتها خارج المنطقة الجغرافية التي يتم فيها توزيع خدمة Human Resources للمستأجر، ويتم تشفيرها أثناء نقلها وتخزينها، ولا تستخدم من قبل Microsoft أو الشركات المعالجة الفرعية لأغراض التدريب أو إدخال تحسينات على الخدمة.‬ لمعرفة مكان تخزين البيانات في Teams، الرجاء مراجعة: [موقع البيانات في Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true)
 
لتقييد الوصول إلى تطبيق Human Resources في Microsoft Teams لمؤسستك أو المستخدمين في مؤسستك، راجع [إدارة سياسات أذونات التطبيق في Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>راجع أيضًا 

[تنزيل وتثبيت Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[مركز تعليمات Microsoft Teams](https://support.office.com/teams)</br>
[إدارة طلبات الإجازة في Teams](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]