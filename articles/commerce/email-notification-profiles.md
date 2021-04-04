---
title: إعداد ملف تعريف إخطار البريد الإلكتروني
description: يوضح هذا الموضوع كيفية إنشاء ملف تعريف إخطار البريد الإلكتروني في Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d82a1abe68ff6e162acb75c6fdc1e207af11c279
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555297"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="5e03e-103">إنشاء ملف تعريف الإخطار بالبريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="5e03e-103">Set up an email notification profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5e03e-104">يوضح هذا الموضوع كيفية إنشاء ملف تعريف إخطار البريد الإلكتروني في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5e03e-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5e03e-105">عند إنشاء القنوات، يمكنك إعداد ملف تعريف الإخطار بالبريد الكتروني.</span><span class="sxs-lookup"><span data-stu-id="5e03e-105">When you create channels, you can set up an email notification profile.</span></span> <span data-ttu-id="5e03e-106">بهذه الطريقة، يمكن إرسال رسائل البريد الإلكتروني إلى العملاء بشأن احداث الحركات المتنوعة، مثل إنشاء أمر وحالة شحن الطلب وفشل الدفع.</span><span class="sxs-lookup"><span data-stu-id="5e03e-106">In that way, emails can be sent to customers for various transactional events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="5e03e-107">للحصول على مزيد من المعلومات حول تكوين البريد الإلكتروني، راجع [تكوين البريد الإلكتروني وإرساله](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="5e03e-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="5e03e-108">إنشاء ملف تعريف إخطار البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="5e03e-108">Create an email notification profile</span></span>

<span data-ttu-id="5e03e-109">لإنشاء ملف تعريف إخطار البريد الإلكتروني، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5e03e-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="5e03e-110">في جزء التنقل، انتقل إلى **الوحدات النمطية \> Retail وcommerce \> إعداد Headquarters \> ملف تعريف إخطار البريد الإلكتروني لـ Commerce**‬.</span><span class="sxs-lookup"><span data-stu-id="5e03e-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="5e03e-111">انقر فوق **جديد** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="5e03e-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="5e03e-112">في الحقل **ملف تعريف إخطار البريد الإلكتروني**، أدخل اسمًا لتحديد ملف التعريف.</span><span class="sxs-lookup"><span data-stu-id="5e03e-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="5e03e-113">في حقل **الوصف**، أدخل وصفًا ذا صلة.</span><span class="sxs-lookup"><span data-stu-id="5e03e-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="5e03e-114">عيِّن المفتاح **نشط** على القيمة **نعم**.</span><span class="sxs-lookup"><span data-stu-id="5e03e-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="5e03e-115">إنشاء قالب بريد إلكتروني</span><span class="sxs-lookup"><span data-stu-id="5e03e-115">Create an email template</span></span>

<span data-ttu-id="5e03e-116">قبل تمكين نوع الإخطار بالبريد الإلكتروني، يجب إنشاء قالب بريد الكتروني للمؤسسة في المركز الرئيسي لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="5e03e-116">Before an email notification type can be enabled, you must create an organization email template in Commerce headquarters.</span></span> <span data-ttu-id="5e03e-117">يُعرِّف هذا القالب موضوع البريد الإلكتروني والمرسل واللغة الافتراضية ونص البريد الإلكتروني لكل لغة تريد دعمها.</span><span class="sxs-lookup"><span data-stu-id="5e03e-117">This template defines the email subject, sender, default language, and email body for each language that you want to support.</span></span>

<span data-ttu-id="5e03e-118">لإنشاء قالب بريد إلكتروني، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="5e03e-118">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="5e03e-119">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد المراكز الرئيسية \> المعلمات \> قوالب البريد الإلكتروني للمؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="5e03e-119">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="5e03e-120">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="5e03e-120">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5e03e-121">في الحقل **معرف البريد الإلكتروني**، أدخل معرفًا للمساعدة في تعريف هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="5e03e-121">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="5e03e-122">في حقل **اسم المرسل**، أدخل اسم المرسل‏‎.</span><span class="sxs-lookup"><span data-stu-id="5e03e-122">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="5e03e-123">في **وصف البريد الإلكتروني**، أدخل وصفًا هادفًا.</span><span class="sxs-lookup"><span data-stu-id="5e03e-123">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="5e03e-124">في **‏‫البريد الإلكتروني للمرسل‬** ، أدخل عنوان البريد الإلكتروني للمرسل.</span><span class="sxs-lookup"><span data-stu-id="5e03e-124">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="5e03e-125">في القسم **عام**، حدد اللغة الافتراضية لقالب البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="5e03e-125">In the **General** section, select a default language for the email template.</span></span> <span data-ttu-id="5e03e-126">سيتم استخدام اللغة الافتراضية في حالة عدم وجود أي قالب مترجم خاص باللغة المحددة.</span><span class="sxs-lookup"><span data-stu-id="5e03e-126">The default language will be used when no localized template exists for the specified language.</span></span>
1. <span data-ttu-id="5e03e-127">وسَّع قسم **محتوى رسالة البريد الإلكتروني** وحدد **جديد** لإنشاء محتوى القالب.</span><span class="sxs-lookup"><span data-stu-id="5e03e-127">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="5e03e-128">بالنسبة لكل عنصر محتوى، حدد اللغة وأدخل سطر موضوع البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="5e03e-128">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="5e03e-129">إذا كان البريد الإلكتروني يحتوي على نص، تأكد من تحديد خانة **‏‫يتضمن نص‬**.</span><span class="sxs-lookup"><span data-stu-id="5e03e-129">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="5e03e-130">في جزء الإجراءات، حدد **رسالة بريد إلكتروني** لتوفير قالب نص البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="5e03e-130">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="5e03e-131">توضح الصورة التالية بعض أمثلة لإعدادات قالب البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="5e03e-131">The following image shows some example email template settings.</span></span>

![إعدادات قالب البريد الإلكتروني](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="5e03e-133">إنشاء حدث بالبريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="5e03e-133">Create an email event</span></span>

<span data-ttu-id="5e03e-134">لإنشاء حدث بالبريد الإلكتروني، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="5e03e-134">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="5e03e-135">في جزء التنقل، انتقل إلى **الوحدات النمطية \> Retail وcommerce \> إعداد Headquarters \> ملف تعريف إخطار البريد الإلكتروني لـ Commerce**‬.</span><span class="sxs-lookup"><span data-stu-id="5e03e-135">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="5e03e-136">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5e03e-136">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="5e03e-137">حدد قالب البريد الإلكتروني من قائمة **معرف البريد الإلكتروني** المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="5e03e-137">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="5e03e-138">حدد **نوع إخطار البريد الإلكتروني** المناسب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="5e03e-138">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="5e03e-139">حدد خانة الاختيار **نشط**.</span><span class="sxs-lookup"><span data-stu-id="5e03e-139">Select the **Active** check box.</span></span>
1. <span data-ttu-id="5e03e-140">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5e03e-140">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5e03e-141">توضح الصورة التالية بعض أمثلة لإعدادات إخطار حدث.</span><span class="sxs-lookup"><span data-stu-id="5e03e-141">The following image shows some example event notification settings.</span></span>

![إعدادات الإخطار بالحدث](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="5e03e-143">الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="5e03e-143">Next steps</span></span>

<span data-ttu-id="5e03e-144">قبل أن تتمكن من إرسال رسائل البريد، يجب تكوين خدمة البريد الصادرة وإعداد وظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="5e03e-144">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="5e03e-145">لمزيد من المعلومات، راجع [تكوين البريد الإلكتروني وإرساله](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="5e03e-145">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="5e03e-146">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5e03e-146">Additional resources</span></span>

[<span data-ttu-id="5e03e-147">تكوين وإرسال البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="5e03e-147">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="5e03e-148">نظره عامة حول القنوات</span><span class="sxs-lookup"><span data-stu-id="5e03e-148">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="5e03e-149">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="5e03e-149">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="5e03e-150">نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="5e03e-150">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
