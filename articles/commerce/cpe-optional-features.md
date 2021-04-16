---
title: تكوين الميزات الاختيارية لبيئة تقييم Dynamics 365 Commerce
description: يوضح هذا الموضوع كيفية تكوين الميزات الاختيارية لبيئة تقييم Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6bc968c2659380bb8c92292ee19e3a7ec8a20a2b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795897"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="a3d31-103">تكوين ميزات اختيارية في بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a3d31-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a3d31-104">يوضح هذا الموضوع كيفية تكوين الميزات الاختيارية لبيئة تقييم Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a3d31-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a3d31-105">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="a3d31-105">Prerequisites</span></span>

<span data-ttu-id="a3d31-106">إذا كنت ترغب في تقييم ميزات البريد الإلكتروني للمعاملات، يجب استيفاء المتطلبات الأساسية التالية:</span><span class="sxs-lookup"><span data-stu-id="a3d31-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="a3d31-107">لديك خادم بريد إلكتروني متاح (خادم البروتوكول البسيط لنقل رسائل البريد \[SMTP\] ) والذي يمكن استخدامه من اشتراك Microsoft Azure حيث قمت بتوفير بيئة التقييم.</span><span class="sxs-lookup"><span data-stu-id="a3d31-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="a3d31-108">لديك اسم المجال المؤهل بالكامل للخادم (FQDN) / عنوان IP ورقم منفذ SMTP، وتفاصيل المصادقة المتاحة.</span><span class="sxs-lookup"><span data-stu-id="a3d31-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="a3d31-109">تكوين نهاية الصورة الخلفية</span><span class="sxs-lookup"><span data-stu-id="a3d31-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="a3d31-110">ابحث عن عنوان الأساسي للوسائط الخاص بك</span><span class="sxs-lookup"><span data-stu-id="a3d31-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="a3d31-111">قبل أن تتمكن من إكمال هذا الإجراء، يجب عليك إكمال الخطوات الواردة في [إعداد موقعك في التجارة](cpe-post-provisioning.md#set-up-your-site-in-commerce)</span><span class="sxs-lookup"><span data-stu-id="a3d31-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="a3d31-112">سجِّل الدخول إلى منشئ موقع Commerce باستخدام عنوان URL الذي قمت بتدوينه عندما قمت بتهيئة التجارة الإلكترونية أثناء التزويد (راجع [تهيئة التجارة الإلكترونية](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="a3d31-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="a3d31-113">افتح موقع **Fabrikam‎**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="a3d31-114">في القائمة الموجودة بالجزء الأيمن، حدد **مكتبة الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="a3d31-115">حدد أي أصل صورة مفرد.</span><span class="sxs-lookup"><span data-stu-id="a3d31-115">Select any single image asset.</span></span>
1. <span data-ttu-id="a3d31-116">في مفتش الخصائص على اليمين، ابحث عن خاصية **عنوان URL العمومي** .</span><span class="sxs-lookup"><span data-stu-id="a3d31-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="a3d31-117">تكون القيمة هي عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="a3d31-117">The value is a URL.</span></span> <span data-ttu-id="a3d31-118">وفيما يلي مثال على ذلك:</span><span class="sxs-lookup"><span data-stu-id="a3d31-118">Here is an example:</span></span>

    <span data-ttu-id="a3d31-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="a3d31-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="a3d31-120">استبدل المعرف الأخير في عنوان URL (**MA1nQC** في المثال السابق) بالسلسلة التالية: **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="a3d31-121">إليك ما يبدو عليه مثال عنوان URL بعد إجراء هذا التغيير:</span><span class="sxs-lookup"><span data-stu-id="a3d31-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="a3d31-122">عنوان URL هذا هو عنوان URL الأساسي للوسائط.</span><span class="sxs-lookup"><span data-stu-id="a3d31-122">This URL is your media base URL.</span></span> <span data-ttu-id="a3d31-123">قم بتدوينه.</span><span class="sxs-lookup"><span data-stu-id="a3d31-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="a3d31-124">قم بتحديث عنوان URL الأساسي للوسائط</span><span class="sxs-lookup"><span data-stu-id="a3d31-124">Update the media base URL</span></span>

1. <span data-ttu-id="a3d31-125">تسجيل الدخول إلى مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="a3d31-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="a3d31-126">استخدم القائمة الموجودة على اليسار للانتقال إلى **الوحدات النمطية \> Retail وcommerce \> إعداد القناة \> ملفات تعريف القناة**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="a3d31-127">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-127">Select **Edit**.</span></span>
1. <span data-ttu-id="a3d31-128">من **خصائص ملف التعريف**، استبدل قيمة الخاصية لـ‏‫ **عنوان URL الأساسي لخادم الوسائط**‬بـ عنوان URL الأساسي للوسائط‬ الذي أنشأته مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="a3d31-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="a3d31-129">حدد القناة بالاسم **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="a3d31-130">ضمن **خصائص ملف التعريف**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="a3d31-131">بالنسبة للخاصية التي تمت إضافتها، حدد **عنوان URL الأساسي لخادم الوسائط** كمفتاح الخاصية.</span><span class="sxs-lookup"><span data-stu-id="a3d31-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="a3d31-132">كقيمة خاصية، أدخل عنوان URL الأساسي للوسائط الذي قمت بإنشائه مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="a3d31-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="a3d31-133">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="a3d31-134">تكوين خادم البريد الإلكتروني واختباره</span><span class="sxs-lookup"><span data-stu-id="a3d31-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="a3d31-135">يجب أن يكون خادم SMTP أو خدمة البريد الإلكتروني التي تدخلها هنا قابلة للوصول من اشتراك Azure الذي تستخدمه للبيئة.</span><span class="sxs-lookup"><span data-stu-id="a3d31-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="a3d31-136">تسجيل الدخول إلى مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="a3d31-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="a3d31-137">باستخدام القائمة الموجودة على اليمين، انتقل إلى **الوحدات النمطية \> Retail and Commerce \> ‏‫إعداد المركز الرئيسي \> المعلمات \> معلمات البريد الإلكتروني‬**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="a3d31-138">في علامة التبويب **إعدادات SMTP** ، في **‏‫خادم البريد الصادر‬** ، ادخل FQDN أو عنوان IP الخاص بخادم SMTP أو خدمه البريد الكتروني الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="a3d31-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="a3d31-139">في الحقل **رقم منفذ SMTP** ، أدخل رقم المنفذ.</span><span class="sxs-lookup"><span data-stu-id="a3d31-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="a3d31-140">(إذا لم تكن تستخدم طبقة مآخذ التوصيل الآمنة \[SSL\]، يكون الرقم الافتراضي للمنفذ هو **25**.)</span><span class="sxs-lookup"><span data-stu-id="a3d31-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="a3d31-141">إذا كانت المصادقة مطلوبة، أدخل القيم في حقول **اسم المستخدم** و **كلمة المرور** .</span><span class="sxs-lookup"><span data-stu-id="a3d31-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="a3d31-142">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-142">Select **Save**.</span></span>
1. <span data-ttu-id="a3d31-143">حدد **تحديث**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="a3d31-144">في علامة التبويب **رسالة بريد إلكتروني للاختبار** ، في الحقل **موفر البريد الكتروني** ، حدد **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="a3d31-145">في الحقل **إرسال إلى** ، أدخل عنوان البريد الإلكتروني الذي ترغب في إرسال رسالة البريد الإلكتروني للاختبار إليه.</span><span class="sxs-lookup"><span data-stu-id="a3d31-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="a3d31-146">حدد **إرسال بريد إلكتروني للاختبار**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="a3d31-147">تكوين قوالب البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="a3d31-147">Configure email templates</span></span>

<span data-ttu-id="a3d31-148">لكل حدث معاملات تريد إرسال رسائل بريد إلكتروني إليه، يجب عليك تحديث قالب البريد الإلكتروني بعنوان بريد إلكتروني صالح للمرسل.</span><span class="sxs-lookup"><span data-stu-id="a3d31-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="a3d31-149">تسجيل الدخول إلى مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="a3d31-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="a3d31-150">باستخدام القائمة الموجودة على اليمين، انتقل إلى **الوحدات النمطية \> Retail and Commerce \> ‏‫إعداد المركز الرئيسي \> المعلمات \> قوالب البريد الإلكتروني للمؤسسة‬‬**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="a3d31-151">حدد **إظهار القائمة**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-151">Select **Show list**.</span></span>
1. <span data-ttu-id="a3d31-152">لكل قالب في القائمة، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="a3d31-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="a3d31-153">ثم، في الحقل **‏‫البريد الإلكتروني للمرسل‬** ، أدخل عنوان البريد الإلكتروني للمرسل.</span><span class="sxs-lookup"><span data-stu-id="a3d31-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="a3d31-154">اختياري: في حقل **اسم المرسل** ، أدخل الاسم الذي يجب استخدامه كاسم المرسل.</span><span class="sxs-lookup"><span data-stu-id="a3d31-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="a3d31-155">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="a3d31-156">تخصيص قوالب البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="a3d31-156">Customize email templates</span></span>

<span data-ttu-id="a3d31-157">قد ترغب في تخصيص قوالب البريد الإلكتروني بحيث تستخدم صورًا مختلفة.</span><span class="sxs-lookup"><span data-stu-id="a3d31-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="a3d31-158">أو قد ترغب في تحديث الروابط في القوالب بحيث تنتقل إلى بيئة التقييم الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="a3d31-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="a3d31-159">يشرح هذا الإجراء كيفية تنزيل القوالب الافتراضية وتخصيصها وتحديث القوالب في النظام.</span><span class="sxs-lookup"><span data-stu-id="a3d31-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="a3d31-160">باستخدام مستعرض ويب، نزِّل [Microsoft Dynamics 365 Commerceالملف المضغوط لقوالب البريد الإلكتروني الافتراضية لتقييم](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) على الكمبيوتر المحلي لديك.</span><span class="sxs-lookup"><span data-stu-id="a3d31-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="a3d31-161">يحتوي هذا الملف علي مستندات HTML التالية:</span><span class="sxs-lookup"><span data-stu-id="a3d31-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="a3d31-162">قالب تأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="a3d31-162">Order confirmation template</span></span>
    - <span data-ttu-id="a3d31-163">إصدار قالب بطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="a3d31-163">Issue gift card template</span></span>
    - <span data-ttu-id="a3d31-164">قالب الأمر الجديد</span><span class="sxs-lookup"><span data-stu-id="a3d31-164">New order template</span></span>
    - <span data-ttu-id="a3d31-165">قالب أمر الحزمة</span><span class="sxs-lookup"><span data-stu-id="a3d31-165">Pack order template</span></span>
    - <span data-ttu-id="a3d31-166">قالب أمر الانتقاء</span><span class="sxs-lookup"><span data-stu-id="a3d31-166">Pick order template</span></span>

1. <span data-ttu-id="a3d31-167">قم بتخصيص القوالب باستخدام نص أو محرر HTML.</span><span class="sxs-lookup"><span data-stu-id="a3d31-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="a3d31-168">راجع قائمة [الرموز المعتمدة](#supported-tokens-in-the-email-template) لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="a3d31-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="a3d31-169">تسجيل الدخول إلى Commerce</span><span class="sxs-lookup"><span data-stu-id="a3d31-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="a3d31-170">باستخدام القائمة الموجودة على اليسار، انتقل إلى **الوحدات النمطية \> ‏‫إدارة المؤسسة‬ \> ‏‫إعداد \> قوالب البريد الإلكتروني للمؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="a3d31-171">قم بتوسيع القائمة الموجودة على الجانب الأيمن لمشاهدة كافة القوالب.</span><span class="sxs-lookup"><span data-stu-id="a3d31-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="a3d31-172">لكل قالب تريد تخصيصه، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="a3d31-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="a3d31-173">حدد القالب في القائمة.</span><span class="sxs-lookup"><span data-stu-id="a3d31-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="a3d31-174">ضمن **محتوى رسالة البريد الإلكتروني**‬، حدد نسخة اللغة المناسبة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="a3d31-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="a3d31-175">اللغة الافتراضية هي **en-us**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="a3d31-176">ضمن **محتوي رسالة البريد الكتروني**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="a3d31-177">يظهر جزء **قالب البريد الكتروني الخاص بالتحميل**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="a3d31-178">حدد **استعراض**، وابحث عن ملف HTML الذي يحتوي علي المحتوي المخصص.</span><span class="sxs-lookup"><span data-stu-id="a3d31-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="a3d31-179">ثم حدد **تحميل**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-179">Select **Upload**.</span></span> <span data-ttu-id="a3d31-180">يتم تحميل القالب الخاص بك إلى النظام ويتم عرض المعاينة.</span><span class="sxs-lookup"><span data-stu-id="a3d31-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="a3d31-181">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-181">Select **OK**.</span></span>
    1. <span data-ttu-id="a3d31-182">(اختياري): قم بتخصيص خاصيه **الموضوع** للقالب.</span><span class="sxs-lookup"><span data-stu-id="a3d31-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="a3d31-183">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="a3d31-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="a3d31-184">الرموز المعتمدة في قالب البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="a3d31-184">Supported tokens in the email template</span></span>

<span data-ttu-id="a3d31-185">عند تقديم البريد الإلكتروني، يتم استبدال هذه الرموز المميزة بقيم فعلية تنطبق على العميل وطلب العميل.</span><span class="sxs-lookup"><span data-stu-id="a3d31-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="a3d31-186">أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="a3d31-186">Sales order</span></span>

<span data-ttu-id="a3d31-187">تنطبق الرموز المميزة التالية على أمر المبيعات الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="a3d31-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="a3d31-188">اسم الرمز المميز</span><span class="sxs-lookup"><span data-stu-id="a3d31-188">Name of the token</span></span> | <span data-ttu-id="a3d31-189">الرمز المميز</span><span class="sxs-lookup"><span data-stu-id="a3d31-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="a3d31-190">رقم الطلب</span><span class="sxs-lookup"><span data-stu-id="a3d31-190">Order number</span></span>      | <span data-ttu-id="a3d31-191">%salesid%</span><span class="sxs-lookup"><span data-stu-id="a3d31-191">%salesid%</span></span> |
| <span data-ttu-id="a3d31-192">اسم العميل</span><span class="sxs-lookup"><span data-stu-id="a3d31-192">Customer's name</span></span>   | <span data-ttu-id="a3d31-193">%customername%</span><span class="sxs-lookup"><span data-stu-id="a3d31-193">%customername%</span></span> |
| <span data-ttu-id="a3d31-194">عنوان التسليم</span><span class="sxs-lookup"><span data-stu-id="a3d31-194">Delivery address</span></span>  | <span data-ttu-id="a3d31-195">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="a3d31-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="a3d31-196">عنوان الفوترة</span><span class="sxs-lookup"><span data-stu-id="a3d31-196">Billing address</span></span>   | <span data-ttu-id="a3d31-197">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="a3d31-197">%customeraddress%</span></span> |
| <span data-ttu-id="a3d31-198">تاريخ الأمر</span><span class="sxs-lookup"><span data-stu-id="a3d31-198">Order date</span></span>        | <span data-ttu-id="a3d31-199">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="a3d31-199">%shipdate%</span></span> |
| <span data-ttu-id="a3d31-200">وضع التسليم</span><span class="sxs-lookup"><span data-stu-id="a3d31-200">Delivery mode</span></span>     | <span data-ttu-id="a3d31-201">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="a3d31-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="a3d31-202">الخصم</span><span class="sxs-lookup"><span data-stu-id="a3d31-202">Discount</span></span>          | <span data-ttu-id="a3d31-203">%discount%</span><span class="sxs-lookup"><span data-stu-id="a3d31-203">%discount%</span></span> |
| <span data-ttu-id="a3d31-204">ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="a3d31-204">Sales tax</span></span>         | <span data-ttu-id="a3d31-205">%tax%</span><span class="sxs-lookup"><span data-stu-id="a3d31-205">%tax%</span></span> |
| <span data-ttu-id="a3d31-206">إجمالي الأمر</span><span class="sxs-lookup"><span data-stu-id="a3d31-206">Order total</span></span>       | <span data-ttu-id="a3d31-207">%total%</span><span class="sxs-lookup"><span data-stu-id="a3d31-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="a3d31-208">خط مبيعات</span><span class="sxs-lookup"><span data-stu-id="a3d31-208">Sales line</span></span>

<span data-ttu-id="a3d31-209">يتم استبدال الرموز المميزة التالية بقيم لكل منتج بالترتيب.</span><span class="sxs-lookup"><span data-stu-id="a3d31-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="a3d31-210">ضع الرمز المميز **قائمة المنتجات - بداية** في بداية كتلة HTML التي تتكرر لكل منتج، ثم ضع الرمز المميز **قائمة المنتجات - نهاية** عند نهاية الكتلة.</span><span class="sxs-lookup"><span data-stu-id="a3d31-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="a3d31-211">اسم الرمز المميز</span><span class="sxs-lookup"><span data-stu-id="a3d31-211">Name of the token</span></span>      | <span data-ttu-id="a3d31-212">الرمز المميز</span><span class="sxs-lookup"><span data-stu-id="a3d31-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="a3d31-213">قائمة المنتجات - بداية</span><span class="sxs-lookup"><span data-stu-id="a3d31-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="a3d31-214">قائمة المنتجات - نهاية</span><span class="sxs-lookup"><span data-stu-id="a3d31-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="a3d31-215">اسم المنتج</span><span class="sxs-lookup"><span data-stu-id="a3d31-215">Product name</span></span>           | <span data-ttu-id="a3d31-216">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="a3d31-216">%lineproductname%</span></span> |
| <span data-ttu-id="a3d31-217">الوصف</span><span class="sxs-lookup"><span data-stu-id="a3d31-217">Description</span></span>            | <span data-ttu-id="a3d31-218">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="a3d31-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="a3d31-219">الكمية</span><span class="sxs-lookup"><span data-stu-id="a3d31-219">Quantity</span></span>               | <span data-ttu-id="a3d31-220">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="a3d31-220">%linequantity%</span></span> |
| <span data-ttu-id="a3d31-221">سعر وحدة البند</span><span class="sxs-lookup"><span data-stu-id="a3d31-221">Line unit price</span></span>        | <span data-ttu-id="a3d31-222">%lineprice% (التحقق من)</span><span class="sxs-lookup"><span data-stu-id="a3d31-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="a3d31-223">إجمالي أصناف البند</span><span class="sxs-lookup"><span data-stu-id="a3d31-223">line item total</span></span>        | <span data-ttu-id="a3d31-224">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="a3d31-224">%linenetamount%</span></span> |
| <span data-ttu-id="a3d31-225">خصم البند</span><span class="sxs-lookup"><span data-stu-id="a3d31-225">line discount</span></span>          | <span data-ttu-id="a3d31-226">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="a3d31-226">%linediscount%</span></span> |
| <span data-ttu-id="a3d31-227">تاريخ الشحن</span><span class="sxs-lookup"><span data-stu-id="a3d31-227">Ship date</span></span>              | <span data-ttu-id="a3d31-228">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="a3d31-228">%lineshipdate%</span></span> |
| <span data-ttu-id="a3d31-229">أسلوب التدبير</span><span class="sxs-lookup"><span data-stu-id="a3d31-229">Procurement method</span></span>     | <span data-ttu-id="a3d31-230">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="a3d31-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="a3d31-231">عنوان التسليم</span><span class="sxs-lookup"><span data-stu-id="a3d31-231">delivery address</span></span>       | <span data-ttu-id="a3d31-232">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="a3d31-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="a3d31-233">وحده مبيعات البند</span><span class="sxs-lookup"><span data-stu-id="a3d31-233">Sales unit of the line</span></span> | <span data-ttu-id="a3d31-234">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="a3d31-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="a3d31-235">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a3d31-235">Additional resources</span></span>

[<span data-ttu-id="a3d31-236">نظرة عامة على بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a3d31-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="a3d31-237">توفير بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a3d31-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="a3d31-238">تكوين بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a3d31-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="a3d31-239">تكوين BOPIS في بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a3d31-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="a3d31-240">الأسئلة الشائعة حول بيئة تقييم Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a3d31-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="a3d31-241">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="a3d31-241">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="a3d31-242">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="a3d31-242">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="a3d31-243">مدخل Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="a3d31-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="a3d31-244">موقع ويب Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a3d31-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]