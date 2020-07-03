---
title: تطبيق Human Resources في Teams
description: يقدم لك هذا الموضوع تطبيق Microsoft Dynamics 365 Human Resources في Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
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
ms.openlocfilehash: 36684710e39c27840cc4aaa259a85579104fd8d6
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431120"
---
# <a name="human-resources-app-in-teams"></a>تطبيق Human Resources في Teams

[!include [banner](includes/preview-feature.md)]

يتيح تطبيق Microsoft Dynamics 365 Human Resources في Microsoft Teams للموظفين طلب إجازة بسرعة وعرض معلومات رصيد إجازاتهم في Microsoft Teams. ويمكن للموظفين التفاعل مع روبوت لطلب المعلومات. توفر علامة التبويب **إجازة** مزيدًا من المعلومات التفصيلية.

![روبوت تطبيق الإجازات لـ Human Resources في Teams](./media/hr-admin-teams-leave-app-bot.png)

![علامة تبويب الإجازة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>التثبيت والإعداد

يمكنك العثور على تطبيق Human Resources في متجر Teams. للحصول على معلومات حول تثبيت تطبيق Teams، راجع [إدارة طلبات الإجازة في Teams](hr-teams-leave-app.md).

للحصول على معلومات حول إدارة أذونات التطبيق في Teams، راجع [إدارة نهج أذونات التطبيق في Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)

## <a name="known-issues"></a>مشكلات معروفة

| المشكلة | الحالة |
| --- | --- |
| خطأ: توجد مشكلة في العثور على بيئة للاتصال بها. | قد تتلقى رسالة الخطأ هذه حتى لو تأكدت من أنه باستطاعة المستخدم الوصول إلى بيئة واحدة أو أكثر من بيئات Human Resources. علاوةً على ذلك، قد لا ترى كافة البيئات التي تتوقعها. وحتى نقوم بإصلاح هذه المشكلة، يمكنك حذف المستخدم ثم استيراده مرة أخرى لحل المشكلة. |
| يصبح الرصيد غير صحيح عند إرسال إجازة لتاريخ مستقبلي. | التنبؤ غير متوفر بعد. يتم عرض الرصيد للتاريخ الحالي. |
| عند تقليل عدد الساعات المستغرقة في طلب موجود، فان **الرصيد المتبقي** ينتقل لأسفل بدلا من أعلى. | سنقوم بمعالجة هذه المشكلة المعروفة في المستقبل. يكون العرض غير صحيح، لكن يتم تعديل الأعداد الصحيحة عند الإرسال. |
| تعرض بطاقتان **لإجازة قادمة** نفس التواريخ. | وتمثل البطاقات عمليات إرسال فردية. سنستمر في تدوين الملاحظات وإجراء تعديلات. |
| تعذر إلغاء طلب **قيد المراجعة**. | هذه الوظيفة غير مدعومة في الوقت الحالي وستتم إضافتها في إصدار مستقبلي. |
| يتم حساب معلومات الرصيد اعتبارًا من اليوم. | لا يعرض النظام حاليًا الأرصدة اعتبارًا من فترة الاستحقاق، حتى إذا تم تكوينه في معلمات الإجازة والغياب. |

## <a name="privacy-notice"></a>إشعار الخصوصية

باستخدام روبوت Dynamics 365 Human Resources في Microsoft Teams، يتم تحليل الإدخالات النصية للمستخدم لفهم الاستعلام/المقصد الأساسي. يتم توجيه إدخال المستخدم مثل "البحث في حساب Contoso" إلى إحدى الخدمات المعرفية من Microsoft تسمى التي خدمة الفهم الذكي للغة (LUIS). أقرا المزيد حول خدمة LUIS  [هنا](https://www.luis.ai/). تزيل خدمة LUIS الغموض أو تفهم المقصد من إدخال المستخدم (في هذه الحالة، يتمثل المقصد في العثور على المعلومات) والكيان المستهدف (وفي هذه الحالة الكيان المقصود هو الحساب المسمى Contoso). يتم بعد ذلك تمرير هذه المعلومات إلى  [إطار عمل روبوت Azure من Microsoft](https://azure.microsoft.com/services/bot-service/)  الذي يتفاعل مع البيانات من Dynamics 365 Human Resources ويسترد المعلومات المطلوبة لاستعلام المستخدم. 

من خلال التثبيت والسماح بالوصول لاستخدام الروبوت، فإنك توافق على السماح لخدمة LUIS وإطار عمل روبوت Azure بمعالجة القصد من الإدخال، والذي ينتج عنه تجربة محسنة للمحادثة مع المستخدم. قد يكون لدي خدمةLUIS و إطار عمل روبوت Azure مستويات متنوعة من التوافق مقارنة بـ Dynamics 365 Human Resources. في حين أن خدمة LUIS يمكنها الوصول إلى استعلامات المستخدمين فقط ولم يتم تصميمها ليتم ربطها ببيانات أو حساب Dynamics 365 Human Resources للمستخدم، لكن يمكن لمستخدم روبوت Dynamics 365 Human Resources إدخال استعلام طواعية يحتوي على بيانات العميل أو البيانات الشخصية أو البيانات الأخرى، وكذلك يمكن يتم إرسال محتويات الاستعلام إلى خدمة LUIS وإطار عمل روبوت Azure. 

يتم الاحتفاظ بمحتويات استعلامات المستخدم ورسائله في نظام LUIS لمدة 30 يومًا بحد أقصى، ويتم تشفيرها عند تثبيت البيانات، ولا يتم استخدامها في التدريب أو تحسين الخدمة. أقرا المزيد حول الخدمات المعرفية  [هنا](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

لإدارة إعدادات المسؤول للتطبيقات في Microsoft Teams، انتقل إلى [مركز إدارة Microsoft Teams](https://admin.teams.microsoft.com/). 

## <a name="see-also"></a>راجع أيضًا 

[تنزيل وتثبيت Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[مركز تعليمات Microsoft Teams](https://support.office.com/teams)</br>
[إدارة طلبات الإجازة في Teams](hr-teams-leave-app.md)

