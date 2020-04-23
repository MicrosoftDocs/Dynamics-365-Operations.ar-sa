---
title: إعداد ملف تعريف إخطار البريد الإلكتروني
description: يوضح هذا الموضوع كيفية إنشاء ملف تعريف إخطار البريد الإلكتروني في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c0ab56c15a37313d0a88b1174d5bcf51d391dcec
ms.sourcegitcommit: 17ffdcbf4b1801bd6ee9c9ddc18622d5d04b8a98
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2020
ms.locfileid: "3180185"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="7c70a-103">إعداد ملف تعريف إخطار البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="7c70a-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7c70a-104">يوضح هذا الموضوع كيفية إنشاء ملف تعريف إخطار البريد الإلكتروني في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7c70a-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7c70a-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="7c70a-105">Overview</span></span>

<span data-ttu-id="7c70a-106">قبل إنشاء قنوات، ستحتاج إلى إعداد ملف تعريف للتأكد من إمكانية إرسال إخطارات البريد الإلكتروني لأحداث مختلفة، مثل إنشاء الأمر وحالة شحن الطلب وفشل الدفع.</span><span class="sxs-lookup"><span data-stu-id="7c70a-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="7c70a-107">للحصول على مزيد من المعلومات حول تكوين البريد الإلكتروني، راجع [تكوين البريد الإلكتروني وإرساله](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="7c70a-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="7c70a-108">إنشاء ملف تعريف إخطار البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="7c70a-108">Create an email notification profile</span></span>

<span data-ttu-id="7c70a-109">لإنشاء ملف تعريف إخطار البريد الإلكتروني، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="7c70a-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="7c70a-110">في جزء التنقل، انتقل إلى **الوحدات النمطية \> Retail وcommerce \> إعداد Headquarters \> ملف تعريف إخطار البريد الإلكتروني لـ Commerce**‬.</span><span class="sxs-lookup"><span data-stu-id="7c70a-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="7c70a-111">انقر فوق **جديد** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="7c70a-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="7c70a-112">في الحقل **ملف تعريف إخطار البريد الإلكتروني**، أدخل اسمًا لتحديد ملف التعريف.</span><span class="sxs-lookup"><span data-stu-id="7c70a-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="7c70a-113">في حقل **الوصف**، أدخل وصفًا ذا صلة.</span><span class="sxs-lookup"><span data-stu-id="7c70a-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="7c70a-114">عيِّن المفتاح **نشط** على القيمة **نعم**.</span><span class="sxs-lookup"><span data-stu-id="7c70a-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="7c70a-115">إنشاء قالب بريد إلكتروني</span><span class="sxs-lookup"><span data-stu-id="7c70a-115">Create an email template</span></span>

<span data-ttu-id="7c70a-116">قبل التمكين من إنشاء إخطار البريد الإلكتروني، يجب إنشاء قالب بريد إلكتروني للمؤسسة يحتوي على معلومات البريد الإلكتروني للمرسلين وقالب البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="7c70a-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="7c70a-117">لإنشاء قالب بريد إلكتروني، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="7c70a-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="7c70a-118">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد المراكز الرئيسية \> المعلمات \> قوالب البريد الإلكتروني للمؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="7c70a-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="7c70a-119">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="7c70a-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7c70a-120">في الحقل **معرف البريد الإلكتروني**، أدخل معرفًا للمساعدة في تعريف هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="7c70a-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="7c70a-121">في حقل **اسم المرسل**، أدخل اسم المرسل‏‎.</span><span class="sxs-lookup"><span data-stu-id="7c70a-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="7c70a-122">في **وصف البريد الإلكتروني**، أدخل وصفًا هادفًا.</span><span class="sxs-lookup"><span data-stu-id="7c70a-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="7c70a-123">في **‏‫البريد الإلكتروني للمرسل‬** ، أدخل عنوان البريد الإلكتروني للمرسل.</span><span class="sxs-lookup"><span data-stu-id="7c70a-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="7c70a-124">في القسم **عام**، املأ أي معلومات اختيارية مطلوبة (مثل أولوية البريد الإلكتروني).</span><span class="sxs-lookup"><span data-stu-id="7c70a-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="7c70a-125">وسَّع قسم **محتوى رسالة البريد الإلكتروني** وحدد **جديد** لإنشاء محتوى القالب.</span><span class="sxs-lookup"><span data-stu-id="7c70a-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="7c70a-126">بالنسبة لكل عنصر محتوى، حدد اللغة وأدخل سطر موضوع البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="7c70a-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="7c70a-127">إذا كان البريد الإلكتروني يحتوي على نص، تأكد من تحديد خانة **‏‫يتضمن نص‬**.</span><span class="sxs-lookup"><span data-stu-id="7c70a-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="7c70a-128">في جزء الإجراءات، حدد **رسالة بريد إلكتروني** لتوفير قالب نص البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="7c70a-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="7c70a-129">توضح الصورة التالية بعض أمثلة لإعدادات قالب البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="7c70a-129">The following image shows some example email template settings.</span></span>

![إعدادات قالب البريد الإلكتروني](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="7c70a-131">إنشاء حدث بالبريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="7c70a-131">Create an email event</span></span>

<span data-ttu-id="7c70a-132">لإنشاء حدث بالبريد الإلكتروني، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="7c70a-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="7c70a-133">في جزء التنقل، انتقل إلى **الوحدات النمطية \> Retail وcommerce \> إعداد Headquarters \> ملف تعريف إخطار البريد الإلكتروني لـ Commerce**‬.</span><span class="sxs-lookup"><span data-stu-id="7c70a-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="7c70a-134">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7c70a-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="7c70a-135">حدد قالب البريد الإلكتروني من قائمة **معرف البريد الإلكتروني** المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="7c70a-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="7c70a-136">حدد **نوع إخطار البريد الإلكتروني** المناسب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="7c70a-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="7c70a-137">حدد خانة الاختيار **نشط**.</span><span class="sxs-lookup"><span data-stu-id="7c70a-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="7c70a-138">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="7c70a-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7c70a-139">توضح الصورة التالية بعض أمثلة لإعدادات إخطار حدث.</span><span class="sxs-lookup"><span data-stu-id="7c70a-139">The following image shows some example event notification settings.</span></span>

![إعدادات الإخطار بالحدث](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="7c70a-141">الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="7c70a-141">Next steps</span></span>

<span data-ttu-id="7c70a-142">قبل أن تتمكن من إرسال رسائل البريد، يجب تكوين خدمة البريد الصادرة وإعداد وظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="7c70a-142">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="7c70a-143">لمزيد من المعلومات، راجع [تكوين البريد الإلكتروني وإرساله](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="7c70a-143">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="7c70a-144">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="7c70a-144">Additional resources</span></span>

[<span data-ttu-id="7c70a-145">تكوين وإرسال البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="7c70a-145">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="7c70a-146">نظره عامة حول القنوات</span><span class="sxs-lookup"><span data-stu-id="7c70a-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7c70a-147">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="7c70a-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="7c70a-148">نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="7c70a-148">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
