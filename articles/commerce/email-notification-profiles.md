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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9378fb200a239433f2023bb90f72840dace1c0eb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000814"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="d3856-103">إعداد ملف تعريف إخطار البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="d3856-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d3856-104">يوضح هذا الموضوع كيفية إنشاء ملف تعريف إخطار البريد الإلكتروني في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d3856-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d3856-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="d3856-105">Overview</span></span>

<span data-ttu-id="d3856-106">قبل إنشاء قنوات، ستحتاج إلى إعداد ملف تعريف للتأكد من إمكانية إرسال إخطارات البريد الإلكتروني لأحداث مختلفة، مثل إنشاء الأمر وحالة شحن الطلب وفشل الدفع.</span><span class="sxs-lookup"><span data-stu-id="d3856-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="d3856-107">للحصول على مزيد من المعلومات حول تكوين البريد الإلكتروني، راجع [تكوين البريد الإلكتروني وإرساله](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="d3856-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="d3856-108">إنشاء ملف تعريف إخطار البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="d3856-108">Create an email notification profile</span></span>

<span data-ttu-id="d3856-109">لإنشاء ملف تعريف إخطار البريد الإلكتروني، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="d3856-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="d3856-110">في جزء التنقل، انتقل إلى **الوحدات النمطية \> Retail وcommerce \> إعداد Headquarters \> ملف تعريف إخطار البريد الإلكتروني لـ Commerce**‬.</span><span class="sxs-lookup"><span data-stu-id="d3856-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="d3856-111">انقر فوق **جديد** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="d3856-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="d3856-112">في الحقل **ملف تعريف إخطار البريد الإلكتروني**، أدخل اسمًا لتحديد ملف التعريف.</span><span class="sxs-lookup"><span data-stu-id="d3856-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="d3856-113">في حقل **الوصف**، أدخل وصفًا ذا صلة.</span><span class="sxs-lookup"><span data-stu-id="d3856-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="d3856-114">عيِّن المفتاح **نشط** على القيمة **نعم**.</span><span class="sxs-lookup"><span data-stu-id="d3856-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="d3856-115">إنشاء قالب بريد إلكتروني</span><span class="sxs-lookup"><span data-stu-id="d3856-115">Create an email template</span></span>

<span data-ttu-id="d3856-116">قبل التمكين من إنشاء إخطار البريد الإلكتروني، يجب إنشاء قالب بريد إلكتروني للمؤسسة يحتوي على معلومات البريد الإلكتروني للمرسلين وقالب البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="d3856-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="d3856-117">لإنشاء قالب بريد إلكتروني، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="d3856-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="d3856-118">في جزء التنقل، انتقل إلى **الوحدات النمطية \> البيع بالتجزئة والتجارة \> إعداد المراكز الرئيسية \> المعلمات \> قوالب البريد الإلكتروني للمؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="d3856-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="d3856-119">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d3856-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d3856-120">في الحقل **معرف البريد الإلكتروني**، أدخل معرفًا للمساعدة في تعريف هذا القالب.</span><span class="sxs-lookup"><span data-stu-id="d3856-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="d3856-121">في حقل **اسم المرسل**، أدخل اسم المرسل‏‎.</span><span class="sxs-lookup"><span data-stu-id="d3856-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="d3856-122">في **وصف البريد الإلكتروني**، أدخل وصفًا هادفًا.</span><span class="sxs-lookup"><span data-stu-id="d3856-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="d3856-123">في **‏‫البريد الإلكتروني للمرسل‬** ، أدخل عنوان البريد الإلكتروني للمرسل.</span><span class="sxs-lookup"><span data-stu-id="d3856-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="d3856-124">في القسم **عام**، املأ أي معلومات اختيارية مطلوبة (مثل أولوية البريد الإلكتروني).</span><span class="sxs-lookup"><span data-stu-id="d3856-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="d3856-125">وسَّع قسم **محتوى رسالة البريد الإلكتروني** وحدد **جديد** لإنشاء محتوى القالب.</span><span class="sxs-lookup"><span data-stu-id="d3856-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="d3856-126">بالنسبة لكل عنصر محتوى، حدد اللغة وأدخل سطر موضوع البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="d3856-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="d3856-127">إذا كان البريد الإلكتروني يحتوي على نص، تأكد من تحديد خانة **‏‫يتضمن نص‬**.</span><span class="sxs-lookup"><span data-stu-id="d3856-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="d3856-128">في جزء الإجراءات، حدد **رسالة بريد إلكتروني** لتوفير قالب نص البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="d3856-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="d3856-129">توضح الصورة التالية بعض أمثلة لإعدادات قالب البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="d3856-129">The following image shows some example email template settings.</span></span>

![إعدادات قالب البريد الإلكتروني](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="d3856-131">إنشاء حدث بالبريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="d3856-131">Create an email event</span></span>

<span data-ttu-id="d3856-132">لإنشاء حدث بالبريد الإلكتروني، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="d3856-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="d3856-133">في جزء التنقل، انتقل إلى **الوحدات النمطية \> Retail وcommerce \> إعداد Headquarters \> ملف تعريف إخطار البريد الإلكتروني لـ Commerce**‬.</span><span class="sxs-lookup"><span data-stu-id="d3856-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="d3856-134">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d3856-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="d3856-135">حدد قالب البريد الإلكتروني من قائمة **معرف البريد الإلكتروني** المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="d3856-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="d3856-136">حدد **نوع إخطار البريد الإلكتروني** المناسب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="d3856-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="d3856-137">حدد خانة الاختيار **نشط**.</span><span class="sxs-lookup"><span data-stu-id="d3856-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="d3856-138">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d3856-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="d3856-139">توضح الصورة التالية بعض أمثلة لإعدادات إخطار حدث.</span><span class="sxs-lookup"><span data-stu-id="d3856-139">The following image shows some example event notification settings.</span></span>

![إعدادات الإخطار بالحدث](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="d3856-141">الخطوات التالية</span><span class="sxs-lookup"><span data-stu-id="d3856-141">Next steps</span></span>

<span data-ttu-id="d3856-142">قبل أن تتمكن من إرسال رسائل البريد، يجب تكوين خدمة البريد الصادرة وإعداد وظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="d3856-142">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="d3856-143">لمزيد من المعلومات، راجع [تكوين البريد الإلكتروني وإرساله](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="d3856-143">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="d3856-144">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d3856-144">Additional resources</span></span>

[<span data-ttu-id="d3856-145">تكوين وإرسال البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="d3856-145">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d3856-146">نظره عامة حول القنوات</span><span class="sxs-lookup"><span data-stu-id="d3856-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d3856-147">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="d3856-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="d3856-148">نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="d3856-148">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
