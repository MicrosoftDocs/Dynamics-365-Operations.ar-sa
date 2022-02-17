---
title: تطبيق Human Resources في Teams
description: يقدم لك هذا الموضوع تطبيق Microsoft Dynamics 365 Human Resources في Microsoft Teams.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ffd6967431227b578e227ee570dbe06c356fb8d6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067041"
---
# <a name="human-resources-app-in-teams"></a>تطبيق Human Resources في Teams


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

يتيح تطبيق Microsoft Dynamics 365 Human Resources في Microsoft Teams للموظفين طلب إجازة بسرعة وعرض معلومات رصيد إجازاتهم في Microsoft Teams. ويمكن للموظفين التفاعل مع روبوت لطلب المعلومات. توفر علامة التبويب **إجازة** مزيدًا من المعلومات التفصيلية. علاوةً على ذلك، يمكنهم إرسال معلومات الأشخاص حول وقت الإجازة القادم في الفرق والدردشات خارج تطبيق Human Resources.

![روبوت تطبيق الإجازات لـ Human Resources في Teams.](./media/hr-teams-leave-app-bot.png)

![علامة تبويب الإجازة في تطبيق الإجازات لـ Human Resources في Teams.](./media/hr-teams-leave-app-timeoff-tab.png)

![بطاقة طلب إجازة في Human Resources.](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>التثبيت والإعداد

يمكنك العثور على تطبيق Dynamics 365 Human Resources في متجر Teams. للحصول على معلومات حول تثبيت تطبيق Teams، راجع [إدارة طلبات الإجازة في Teams](hr-teams-leave-app.md).

للحصول على معلومات حول إدارة أذونات التطبيق في Teams، راجع [إدارة نهج أذونات التطبيق في Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies)

إذا كنت ترغب أن يقوم المستخدمون بعرض تقويم الإجازة والغياب في التطبيق، فستحتاج إلى تمكين **‏‫تقويم الإجازة والغياب في Teams** في إدارة الميزات. لمزيد من المعلومات حول تمكين الميزات، راجع [إدارة الميزات](hr-admin-manage-features.md).

## <a name="update-app"></a>تحديث التطبيق
>[!NOTE]
> اعتبارًا من 20 ديسمبر 2021، سيتم إيقاف تشغيل خدمات الروبوت لتطبيق الموارد البشرية المستضافة في مستأجر Microsoft. لن يكون هناك أي تأثير للتمديد المحدث (الإصدار 1.1.5) المتاح للتثبيت. سيكون التأثير الرئيسي على الامتداد القديم (الإصدار 1.1.4). سيتوقف برنامج الدردشة الآلي في هذا الإصدار عن العمل. ستستمر علامة التبويب **الإجازة** في العمل في كلا الامتدادين.

بالنسبة للإصدار 1.1.4، سيتوقف روبوت الدردشة عن الاستجابة لأي رسالة. على سبيل المثال، **تسجيل الدخول**، و **عرض الأرصدة**، و **الاطلاع على الإجازة**. يجب تحديث التطبيق يدويًا إلى أحدث إصدار. لمزيد من المعلومات، راجع [تحديث التطبيقات في Microsoft Teams](/MicrosoftTeams/apps-update-experience).

للتحديث إلى الإصدار 1.1.5، أكمل الخطوات التالية:
1. في Microsoft Teams، انتقل إلى **التطبيقات**.
2. ابحث عن تطبيق **Human Resources**.
3. حدد **ترقية**.

يمكنك التحقق من إصدار تطبيق الموارد البشرية إما بالانتقال إلى علامة التبويب **حول** أو بالانتقال إلى قسم **التطبيق الشخصي**. 

![علامة التبويب **حول** في Human Resources.](./media/HR-teams-about.png)

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>تمكين الإعلامات لتطبيق Human Resources في Teams

إذا أردت أن يتلقى المستخدمون إعلامات تتعلق بطلبات الإجازات في تطبيق Teams، يجب عليك تمكين الإعلامات في Dynamics 365 Human Resources.

>[!NOTE]
>وحدهم المستخدمون الذين سجلوا دخولهم إلى Teams ويستخدمون تطبيق Dynamics 365 Human Resources سيتلقون إعلامات.

1. في Human Resources، حدد **إدارة النظام**.

2. حدد **الارتباطات**.

3. ضمن **الإعداد**، حدد **معلمات النظام**.

4. من علامة التبويب **عام**، قم بتعيين الخيار **تمكين الاعلامات لتطبيق Teams** إلى **نعم**.

   ![تمكين إعلامات تطبيق Teams في معلمات النظام.](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. لتشغيل إعلامات Teams لجميع المستخدمين، حدد **نعم** عند المطالبة.

   ![تمكين إعلامات Teams لجميع المستخدمين.](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>تشغيل إعلامات Teams أو إيقاف تشغيلها لمستخدمين فرديين

بعد تمكين الإعلامات لتطبيق Dynamics 365 Human Resources Teams، يمكنك تشغيل الإعلامات أو إيقاف تشغيلها لمستخدمين فرديين.

1. في Human Resources، حدد **إدارة النظام**.

2. حدد **الارتباطات**.

3. ضمن **المستخدمون**، حدد **خيارات المستخدم**.

4. حدد علامة التبويب **سير العمل**.

5. عيّن الخيار **تمكين الإعلامات لتطبيق Teams** إلى **نعم** لتمكين الإعلامات للمستخدم أو إلى **لا** لتعطيل الإعلامات للمستخدم.

   ![تمكين إعلامات تطبيق Teams في خيارات المستخدم على علامة تبويب سير العمل.](./media/hr-admin-teams-leave-app-notifications.png)

6. حدد **حفظ**.

## <a name="supported-languages"></a>اللغات المدعومة

يدعم التطبيق Dynamics 365 Human Resources الموجود في Teams اللغات التالية:

| معرف الإعدادات المحلية | اللغة |
| --- | --- |
| de-DE | الألمانية (ألمانيا) |
| es-ES | الأسبانية (أسبانيا) |
| es-MX | الأسبانية (المكسيك) |
| fr-CA | الفرنسية (كندا) |
| fr-FR | الفرنسية (فرنسا) |
| it-IT | الإيطالية (إيطاليا) |
| nl-NL | الهولندية (هولندا) |
| pt-BR | البرتغالية (البرازيل) |
| tr-TR | التركية (تركيا) |
| zh-CN | الصينية (المبسطة) |

## <a name="notes"></a>الملاحظات

يتم تحديد عناصر العمل التالية للإصدارات المستقبلية:

| عنصر العمل | الحالة |
| --- | --- |
| يصبح الرصيد غير صحيح عند إرسال إجازة لتاريخ مستقبلي. | التنبؤ غير متوفر بعد. يتم عرض الرصيد للتاريخ الحالي. |
| تعذر إلغاء طلب **قيد المراجعة**. | هذه الوظيفة غير مدعومة في الوقت الحالي وستتم إضافتها في إصدار مستقبلي. |
| يتم حساب معلومات الرصيد اعتبارًا من اليوم. | لا يعرض النظام حاليًا الأرصدة اعتبارًا من فترة الاستحقاق، حتى إذا تم تكوينها في صفحة **معلمات الإجازة والغياب**. |

## <a name="troubleshooting"></a>استكشاف الأخطاء وإصلاحها

إذا كان المستخدم يواجه مشكله في تسجيل الدخول أو باستخدام تطبيق فرق الموارد البشرية، حاول اتباع إرشادات استكشاف الأخطاء وإصلاحها. إذا كنت لا تزال تواجه مشاكل بعد استكشاف الأخطاء وإصلاحها، اتصل بالدعم. لمزيد من المعلومات، راجع [الحصول على الدعم](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="ensure-the-teams-human-resources-application-is-up-to-date"></a>التأكد من تحديث تطبيق Human Resources في Teams
إذا واجهت مشكلات في تطبيق Human Resources في Teams، فإنك بحاجة إلى تأكيد أنك تقوم بتشغيل أحدث إصدار. الحد الأدنى المعتمد للإصدار هو 1.1.5. للحصول على إرشادات حول كيفية تحديث تطبيق Teams، راجع [وثائق Teams](/MicrosoftTeams/apps-update-experience).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>لا يمكن التسجيل في تطبيق الموارد البشرية في الفرق

إذا قام مستخدم بالاتصال بك لأنه لا يمكنه تسجيل الدخول إلى التطبيق، تحقق من أن المستخدم لديه سجل موظف مقترن في الموارد البشرية.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>حدث خطا عند اعتماد طلبات المغادرة في تطبيق الموارد البشرية في الفرق

إذا تلقى المستخدم خطأً أثناء محاولته الموافقة على طلبات الإجازة في تطبيق Teams، فجرّب خطوات استكشاف الأخطاء وإصلاحها التالية:

1. تحقق من ان حساب الفرق الخاص بهم هو نفسه الذي يستخدم للوصول إلى الموارد البشرية.

2. تحقق من انهم موافقون صالحون للطلب من خلال التحقق من إعدادات سير العمل للموافقة على المغادرة. لمزيد من المعلومات حول إنهاء مهام سير العمل، راجع [إنشاء سير عمل لطلب أجازه](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>لا يتلقى معتمدون الإجازات رسائل دردشة Teams للموافقة على طلبات الإجازة

1. تأكد من تمكين الإعلامات للبيئة والمستخدم. لمزيد من المعلومات، راجع [تمكين الإعلامات لتطبيق الموارد البشرية في Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) و[تشغيل إعلامات Teams أو إيقاف تشغيلها للمستخدمين الفرديين](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. تأكد من تسجيل المستخدمين الدخول إلى علامة التبويب **الدردشة** بنفس بيانات الاعتماد التي يستخدمونها للموافقة على طلبات الإجازة. استخدم رسائل "تسجيل الخروج" ثم "تسجيل الدخول" لتسجيل الدخول باستخدام بيانات الاعتماد الصحيحة.

3. إذا استمرت المشكلة، فتحقق من حالة الوظيفة الدفعية **نظام أحداث الأعمال** كمسؤول النظام. إذا كان في مرحلة **انتظار** أو **أو تنفيذ**، تحقق مرة أخرى في غضون بضع دقائق. إذا ظلت الحالة دون تغيير، فقم بتسجيل بطاقة دعم حتى يتمكن فريقنا من المساعدة في حل المشكلة.

## <a name="privacy-notice"></a>إشعار الخصوصية

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>خدمة الفهم الذكي للغة (LUIS) من Microsoft.

باستخدام روبوت Dynamics 365 Human Resources في Microsoft Teams، يتم تحليل الإدخالات النصية للمستخدم لفهم الاستعلام/المقصد الأساسي. يتم توجيه إدخال المستخدم مثل "البحث في حساب Contoso" إلى إحدى الخدمات المعرفية من Microsoft تسمى التي خدمة الفهم الذكي للغة (LUIS). أقرا المزيد حول خدمة LUIS  [هنا](https://www.luis.ai/). تزيل خدمة LUIS الغموض أو تفهم المقصد من إدخال المستخدم (في هذه الحالة، يتمثل المقصد في العثور على المعلومات) والكيان المستهدف (وفي هذه الحالة الكيان المقصود هو الحساب المسمى Contoso). يتم بعد ذلك تمرير هذه المعلومات إلى  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) من Microsoft الذي يتفاعل مع البيانات من Dynamics 365 Human Resources ويسترد المعلومات المطلوبة لاستعلام المستخدم.

من خلال التثبيت والسماح بالوصول لاستخدام الروبوت، فإنك توافق على السماح لخدمة LUIS وإطار عمل روبوت Azure بمعالجة القصد من الإدخال، والذي ينتج عنه تجربة محسنة للمحادثة مع المستخدم. قد يكون لدي خدمةLUIS و إطار عمل روبوت Azure مستويات متنوعة من التوافق مقارنة بـ Dynamics 365 Human Resources. في حين أن خدمة LUIS يمكنها الوصول إلى استعلامات المستخدمين فقط ولم يتم تصميمها ليتم ربطها ببيانات أو حساب Dynamics 365 Human Resources للمستخدم، لكن يمكن لمستخدم روبوت Dynamics 365 Human Resources إدخال استعلام طواعية يحتوي على بيانات العميل أو البيانات الشخصية أو البيانات الأخرى، وكذلك يمكن يتم إرسال محتويات الاستعلام إلى خدمة LUIS وإطار عمل روبوت Azure. 

يتم الاحتفاظ بمحتويات استعلامات المستخدم ورسائله في نظام LUIS لمدة 30 يومًا بحد أقصى، ويتم تشفيرها عند تثبيت البيانات، ولا يتم استخدامها في التدريب أو تحسين الخدمة. أقرا المزيد حول الخدمات المعرفية  [هنا](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

لإدارة إعدادات المسؤول للتطبيقات في Microsoft Teams، انتقل إلى [مركز إدارة Microsoft Teams](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams وشبكة أحداث Azure وAzure Cosmos DB

عند استخدام تطبيق Dynamics 365 Human Resources في Microsoft Teams، قد تتدفق بعض بيانات العملاء خارج المنطقة الجغرافية التي يتم فيها توزيع خدمة Human Resources للمستأجر.

يرسل Dynamics 365 Human Resources تفاصيل طلب الإجازة الخاص بالموظف وتفاصيل سير العمل إلى شبكة الأحداث في Microsoft Azure وMicrosoft Teams قد يتم تخزين هذه البيانات لمدة تصل إلى 24 ساعة في شبكة أحداث Microsoft Azure وستتم معالجتها في الولايات المتحدة، ويتم تشفيرها أثناء نقلها وتخزينها، ولا تستخدم من قبل Microsoft أو الشركات المعالجة الفرعية لأغراض التدريب أو إدخال تحسينات على الخدمة. لمعرفة مكان تخزين البيانات في Teams، الرجاء مراجعة: [موقع البيانات في Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide)

اثناء التحدث مع روبوت الدردشة في تطبيق Human Resources، قد يتم تخزين محتوى المحادثة في Azure Cosmos DB وإرساله إلى Microsoft Teams. قد يتم تخزين هذه البيانات في Azure Cosmos DB لمدة 24 ساعة وقد تتم معالجتها خارج المنطقة الجغرافية التي يتم فيها توزيع خدمة Human Resources للمستأجر، ويتم تشفيرها أثناء نقلها وتخزينها، ولا تستخدم من قبل Microsoft أو الشركات المعالجة الفرعية لأغراض التدريب أو إدخال تحسينات على الخدمة.‬ لمعرفة مكان تخزين البيانات في Teams، الرجاء مراجعة: [موقع البيانات في Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide)
 
لتقييد الوصول إلى تطبيق Human Resources في Microsoft Teams لمؤسستك أو المستخدمين في مؤسستك، راجع [إدارة سياسات أذونات التطبيق في Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>راجع أيضًا 

[تنزيل وتثبيت Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[مركز تعليمات Microsoft Teams](https://support.office.com/teams)</br>
[إدارة طلبات الإجازة في Teams](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
