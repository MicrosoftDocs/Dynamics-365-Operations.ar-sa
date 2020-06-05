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
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 423ec36a73e8af9d915c5cfe16bd4d552448e2b6
ms.sourcegitcommit: d1541831d556b722a71aed442043ffb4a4576d87
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/20/2020
ms.locfileid: "3388106"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="f2446-103">تطبيق Human Resources في Teams</span><span class="sxs-lookup"><span data-stu-id="f2446-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="f2446-104">يتيح تطبيق Microsoft Dynamics 365 Human Resources في Microsoft Teams للموظفين طلب إجازة بسرعة وعرض معلومات رصيد إجازاتهم في Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f2446-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="f2446-105">ويمكن للموظفين التفاعل مع روبوت لطلب المعلومات.</span><span class="sxs-lookup"><span data-stu-id="f2446-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="f2446-106">توفر علامة التبويب **إجازة** مزيدًا من المعلومات التفصيلية.</span><span class="sxs-lookup"><span data-stu-id="f2446-106">The **Time off** tab provides more detailed information.</span></span>

![روبوت تطبيق الإجازات لـ Human Resources في Teams](./media/hr-admin-teams-leave-app-bot.png)

![علامة تبويب الإجازة في تطبيق الإجازات لـ Human Resources في Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="f2446-109">التثبيت والإعداد</span><span class="sxs-lookup"><span data-stu-id="f2446-109">Install and setup</span></span>

<span data-ttu-id="f2446-110">يمكنك العثور على تطبيق Human Resources في متجر Teams.</span><span class="sxs-lookup"><span data-stu-id="f2446-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="f2446-111">للحصول على معلومات حول تثبيت تطبيق Teams، راجع [إدارة طلبات الإجازة في Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="f2446-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="f2446-112">للحصول على معلومات حول إدارة أذونات التطبيق في Teams، راجع [إدارة نهج أذونات التطبيق في Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies)</span><span class="sxs-lookup"><span data-stu-id="f2446-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="known-issues"></a><span data-ttu-id="f2446-113">مشكلات معروفة</span><span class="sxs-lookup"><span data-stu-id="f2446-113">Known issues</span></span>

| <span data-ttu-id="f2446-114">المشكلة</span><span class="sxs-lookup"><span data-stu-id="f2446-114">Issue</span></span> | <span data-ttu-id="f2446-115">الحالة</span><span class="sxs-lookup"><span data-stu-id="f2446-115">Status</span></span> |
| --- | --- |
| <span data-ttu-id="f2446-116">يصبح الرصيد غير صحيح عند إرسال إجازة لتاريخ مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="f2446-116">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="f2446-117">التنبؤ غير متوفر بعد.</span><span class="sxs-lookup"><span data-stu-id="f2446-117">Forecasting isn't yet available.</span></span> <span data-ttu-id="f2446-118">يتم عرض الرصيد للتاريخ الحالي.</span><span class="sxs-lookup"><span data-stu-id="f2446-118">The balance displays for the current date.</span></span> |
| <span data-ttu-id="f2446-119">عند تقليل عدد الساعات المستغرقة في طلب موجود، فان **الرصيد المتبقي** ينتقل لأسفل بدلا من أعلى.</span><span class="sxs-lookup"><span data-stu-id="f2446-119">When reducing the number of hours taken in an existing request, the **Remaining balance** goes down instead of up.</span></span> | <span data-ttu-id="f2446-120">سنقوم بمعالجة هذه المشكلة المعروفة في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="f2446-120">We'll address this known issue in the future.</span></span> <span data-ttu-id="f2446-121">يكون العرض غير صحيح، لكن يتم تعديل الأعداد الصحيحة عند الإرسال.</span><span class="sxs-lookup"><span data-stu-id="f2446-121">The display is incorrect, but the correct amounts are adjusted upon submission.</span></span> |
| <span data-ttu-id="f2446-122">تعرض بطاقتان **لإجازة قادمة** نفس التواريخ.</span><span class="sxs-lookup"><span data-stu-id="f2446-122">Two **Upcoming time off** cards display for the same dates.</span></span> | <span data-ttu-id="f2446-123">وتمثل البطاقات عمليات إرسال فردية.</span><span class="sxs-lookup"><span data-stu-id="f2446-123">The cards represent individual submissions.</span></span> <span data-ttu-id="f2446-124">سنستمر في تدوين الملاحظات وإجراء تعديلات.</span><span class="sxs-lookup"><span data-stu-id="f2446-124">We'll continue to take feedback and make adjustments.</span></span> |
| <span data-ttu-id="f2446-125">تعذر إلغاء طلب **قيد المراجعة**.</span><span class="sxs-lookup"><span data-stu-id="f2446-125">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="f2446-126">هذه الوظيفة غير مدعومة في الوقت الحالي وستتم إضافتها في إصدار مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="f2446-126">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="f2446-127">يتم حساب معلومات الرصيد اعتبارًا من اليوم.</span><span class="sxs-lookup"><span data-stu-id="f2446-127">Balance information is calculated as of today.</span></span> | <span data-ttu-id="f2446-128">لا يعرض النظام حاليًا الأرصدة اعتبارًا من فترة الاستحقاق، حتى إذا تم تكوينه في معلمات الإجازة والغياب.</span><span class="sxs-lookup"><span data-stu-id="f2446-128">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="f2446-129">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="f2446-129">Privacy notice</span></span>

<span data-ttu-id="f2446-130">باستخدام روبوت Dynamics 365 Human Resources في Microsoft Teams، يتم تحليل الإدخالات النصية للمستخدم لفهم الاستعلام/المقصد الأساسي.</span><span class="sxs-lookup"><span data-stu-id="f2446-130">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="f2446-131">يتم توجيه إدخال المستخدم مثل "البحث في حساب Contoso" إلى إحدى الخدمات المعرفية من Microsoft تسمى التي خدمة الفهم الذكي للغة (LUIS).</span><span class="sxs-lookup"><span data-stu-id="f2446-131">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="f2446-132">أقرا المزيد حول خدمة LUIS  [هنا](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="f2446-132">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="f2446-133">تزيل خدمة LUIS الغموض أو تفهم المقصد من إدخال المستخدم (في هذه الحالة، يتمثل المقصد في العثور على المعلومات) والكيان المستهدف (وفي هذه الحالة الكيان المقصود هو الحساب المسمى Contoso).</span><span class="sxs-lookup"><span data-stu-id="f2446-133">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="f2446-134">يتم بعد ذلك تمرير هذه المعلومات إلى  [إطار عمل روبوت Azure من Microsoft](https://azure.microsoft.com/services/bot-service/)  الذي يتفاعل مع البيانات من Dynamics 365 Human Resources ويسترد المعلومات المطلوبة لاستعلام المستخدم.</span><span class="sxs-lookup"><span data-stu-id="f2446-134">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="f2446-135">من خلال التثبيت والسماح بالوصول لاستخدام الروبوت، فإنك توافق على السماح لخدمة LUIS وإطار عمل روبوت Azure بمعالجة القصد من الإدخال، والذي ينتج عنه تجربة محسنة للمحادثة مع المستخدم.</span><span class="sxs-lookup"><span data-stu-id="f2446-135">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="f2446-136">قد يكون لدي خدمةLUIS و إطار عمل روبوت Azure مستويات متنوعة من التوافق مقارنة بـ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f2446-136">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="f2446-137">في حين أن خدمة LUIS يمكنها الوصول إلى استعلامات المستخدمين فقط ولم يتم تصميمها ليتم ربطها ببيانات أو حساب Dynamics 365 Human Resources للمستخدم، لكن يمكن لمستخدم روبوت Dynamics 365 Human Resources إدخال استعلام طواعية يحتوي على بيانات العميل أو البيانات الشخصية أو البيانات الأخرى، وكذلك يمكن يتم إرسال محتويات الاستعلام إلى خدمة LUIS وإطار عمل روبوت Azure.</span><span class="sxs-lookup"><span data-stu-id="f2446-137">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="f2446-138">يتم الاحتفاظ بمحتويات استعلامات المستخدم ورسائله في نظام LUIS لمدة 30 يومًا بحد أقصى، ويتم تشفيرها عند تثبيت البيانات، ولا يتم استخدامها في التدريب أو تحسين الخدمة.</span><span class="sxs-lookup"><span data-stu-id="f2446-138">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="f2446-139">أقرا المزيد حول الخدمات المعرفية  [هنا](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="f2446-139">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="f2446-140">لإدارة إعدادات المسؤول للتطبيقات في Microsoft Teams، انتقل إلى [مركز إدارة Microsoft Teams](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="f2446-140">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="f2446-141">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="f2446-141">See also</span></span> 

[<span data-ttu-id="f2446-142">تنزيل وتثبيت Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f2446-142">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="f2446-143">مركز تعليمات Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="f2446-143">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="f2446-144">إدارة طلبات الإجازة في Teams</span><span class="sxs-lookup"><span data-stu-id="f2446-144">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

