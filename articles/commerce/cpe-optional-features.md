---
title: تكوين الميزات الاختيارية لبيئة معاينة Dynamics 365 Commerce
description: يشرح هذا الموضوع كيفية تكوين الميزات الاختيارية لبيئة معاينة Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 43b23b9ef881b2ab2f3d005d4ba761848a7fa4ed
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024719"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="81b12-103">تكوين الميزات الاختيارية لبيئة معاينة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="81b12-103">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="81b12-104">يشرح هذا الموضوع كيفية تكوين الميزات الاختيارية لبيئة معاينة Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="81b12-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="81b12-105">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="81b12-105">Prerequisites</span></span>

<span data-ttu-id="81b12-106">إذا كنت ترغب في تقييم ميزات البريد الإلكتروني للمعاملات، يجب استيفاء المتطلبات الأساسية التالية:</span><span class="sxs-lookup"><span data-stu-id="81b12-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="81b12-107">لديك خادم بريد إلكتروني متاح (خادم البروتوكول البسيط لنقل رسائل البريد \[SMTP\] ) والذي يمكن استخدامه من اشتراك Microsoft Azure حيث قمت بتوفير بيئة المعاينة.</span><span class="sxs-lookup"><span data-stu-id="81b12-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="81b12-108">لديك اسم المجال المؤهل بالكامل للخادم (FQDN) / عنوان IP ورقم منفذ SMTP، وتفاصيل المصادقة المتاحة.</span><span class="sxs-lookup"><span data-stu-id="81b12-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="81b12-109">إذا كنت ترغب في تقييم ميزات "إدارة الأصول الرقمية" عن طريق استيعاب صور جديدة لكل القنوات، فيجب أن يكون مُتاح لديك اسم المستأجر الخاص بنظام إدارة المحتوى (CMS).</span><span class="sxs-lookup"><span data-stu-id="81b12-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="81b12-110">يتم توفير التعليمات الخاصة بالعثور علي هذا الاسم لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="81b12-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="81b12-111">>>> (س: أين هي التعليمات؟)</span><span class="sxs-lookup"><span data-stu-id="81b12-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="81b12-112">تكوين نهاية الصورة الخلفية</span><span class="sxs-lookup"><span data-stu-id="81b12-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="81b12-113">ابحث عن عنوان الأساسي للوسائط الخاص بك</span><span class="sxs-lookup"><span data-stu-id="81b12-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="81b12-114">قبل أن تتمكن من إكمال هذا الإجراء، يجب عليك إكمال الخطوات الواردة في [إعداد موقعك في التجارة](cpe-post-provisioning.md#set-up-your-site-in-commerce)</span><span class="sxs-lookup"><span data-stu-id="81b12-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="81b12-115">قم بتسجيل الدخول إلى أداة إدارة موقع التجارة باستخدام عنوان URL الذي قمت بتدوينه عندما قمت بتهيئة التجارة الإلكترونية أثناء التزويد (راجع [تهيئة التجارة الإلكترونية](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="81b12-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="81b12-116">افتح موقع **Fabrikam‎**.</span><span class="sxs-lookup"><span data-stu-id="81b12-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="81b12-117">في القائمة على اليسار ، حدد **الأصول**.</span><span class="sxs-lookup"><span data-stu-id="81b12-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="81b12-118">حدد أي أصل صورة مفرد.</span><span class="sxs-lookup"><span data-stu-id="81b12-118">Select any single image asset.</span></span>
1. <span data-ttu-id="81b12-119">في مفتش الخصائص على اليمين، ابحث عن خاصية **عنوان URL العمومي** .</span><span class="sxs-lookup"><span data-stu-id="81b12-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="81b12-120">تكون القيمة هي عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="81b12-120">The value is a URL.</span></span> <span data-ttu-id="81b12-121">وفيما يلي مثال على ذلك:</span><span class="sxs-lookup"><span data-stu-id="81b12-121">Here is an example:</span></span>

    <span data-ttu-id="81b12-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="81b12-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="81b12-123">استبدل المعرف الأخير في عنوان URL (**MA1nQC** في المثال السابق) بالسلسلة التالية: **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="81b12-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="81b12-124">إليك ما يبدو عليه مثال عنوان URL بعد إجراء هذا التغيير:</span><span class="sxs-lookup"><span data-stu-id="81b12-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="81b12-125">عنوان URL هذا هو عنوان URL الأساسي للوسائط.</span><span class="sxs-lookup"><span data-stu-id="81b12-125">This URL is your media base URL.</span></span> <span data-ttu-id="81b12-126">قم بتدوينه.</span><span class="sxs-lookup"><span data-stu-id="81b12-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="81b12-127">قم بتحديث عنوان URL الأساسي للوسائط</span><span class="sxs-lookup"><span data-stu-id="81b12-127">Update the media base URL</span></span>

1. <span data-ttu-id="81b12-128">سجل دخولك إلى Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="81b12-128">Sign in to Dynamics 365 Retail.</span></span>
1. <span data-ttu-id="81b12-129">استخدم القائمة الموجودة على اليسار للانتقال إلى **الوحدات النمطية \> البيع بالتجزئة \> إعداد القناة \> ملفات تعريف القناة**.</span><span class="sxs-lookup"><span data-stu-id="81b12-129">Use the menu on the left to go to **Modules \> Retail \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="81b12-130">حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="81b12-130">Select **Edit**.</span></span>
1. <span data-ttu-id="81b12-131">من **خصائص ملف التعريف**، استبدل قيمة الخاصية لـ‏‫ **عنوان URL الأساسي لخادم الوسائط**‬بـ عنوان URL الأساسي للوسائط‬ الذي أنشأته مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="81b12-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="81b12-132">في القائمة الموجودة على اليسار، ضمن القناة **الافتراضية** ، حدد القناة الأخرى.</span><span class="sxs-lookup"><span data-stu-id="81b12-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="81b12-133">ضمن **خصائص ملف التعريف**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="81b12-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="81b12-134">بالنسبة للخاصية التي تمت إضافتها، حدد **عنوان URL الأساسي لخادم الوسائط** كمفتاح الخاصية.</span><span class="sxs-lookup"><span data-stu-id="81b12-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="81b12-135">كقيمة خاصية، أدخل عنوان URL الأساسي للوسائط الذي قمت بإنشائه مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="81b12-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="81b12-136">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="81b12-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="81b12-137">تكوين خادم البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="81b12-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="81b12-138">يجب أن يكون خادم SMTP أو خدمة البريد الإلكتروني التي تدخلها هنا قابلة للوصول من اشتراك Azure الذي تستخدمه للبيئة.</span><span class="sxs-lookup"><span data-stu-id="81b12-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="81b12-139">سجل الدخول إلى Retail.</span><span class="sxs-lookup"><span data-stu-id="81b12-139">Sign in to Retail.</span></span>
1. <span data-ttu-id="81b12-140">استخدم القائمة الموجودة على اليسار للانتقال إلى **الوحدات النمطية \> إدارة النظام \> الإعداد \> البريد الإلكتروني \> محددات البريد الإلكتروني**.</span><span class="sxs-lookup"><span data-stu-id="81b12-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="81b12-141">في علامة التبويب **إعدادات SMTP** ، في **‏‫خادم البريد الصادر‬** ، ادخل FQDN أو عنوان IP الخاص بخادم SMTP أو خدمه البريد الكتروني الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="81b12-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="81b12-142">في الحقل **رقم منفذ SMTP** ، أدخل رقم المنفذ.</span><span class="sxs-lookup"><span data-stu-id="81b12-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="81b12-143">(إذا لم تكن تستخدم طبقة مآخذ التوصيل الآمنة \[SSL\]، يكون الرقم الافتراضي للمنفذ هو **25**.)</span><span class="sxs-lookup"><span data-stu-id="81b12-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="81b12-144">إذا كانت المصادقة مطلوبة، أدخل القيم في حقول **اسم المستخدم** و **كلمة المرور** .</span><span class="sxs-lookup"><span data-stu-id="81b12-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="81b12-145">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="81b12-145">Select **Save**.</span></span>
1. <span data-ttu-id="81b12-146">حدد **تحديث**.</span><span class="sxs-lookup"><span data-stu-id="81b12-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="81b12-147">في علامة التبويب **رسالة بريد إلكتروني للاختبار** ، في الحقل **موفر البريد الكتروني** ، حدد **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="81b12-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="81b12-148">في الحقل **إرسال إلى** ، أدخل عنوان البريد الإلكتروني الذي ترغب في إرسال رسالة البريد الإلكتروني للاختبار إليه.</span><span class="sxs-lookup"><span data-stu-id="81b12-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="81b12-149">حدد **إرسال بريد إلكتروني للاختبار**.</span><span class="sxs-lookup"><span data-stu-id="81b12-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="81b12-150">تكوين قوالب البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="81b12-150">Configure email templates</span></span>

<span data-ttu-id="81b12-151">لكل حدث معاملات تريد إرسال رسائل بريد إلكتروني إليه، يجب عليك تحديث قالب البريد الإلكتروني بعنوان بريد إلكتروني صالح للمرسل.</span><span class="sxs-lookup"><span data-stu-id="81b12-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="81b12-152">سجل الدخول إلى Retail.</span><span class="sxs-lookup"><span data-stu-id="81b12-152">Sign in to Retail.</span></span>
1. <span data-ttu-id="81b12-153">باستخدام القائمة الموجودة على اليسار، انتقل إلى **الوحدات النمطية \> ‏‫إدارة المؤسسة‬ \> ‏‫إعداد \> قوالب البريد الإلكتروني للمؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="81b12-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="81b12-154">حدد **إظهار القائمة**.</span><span class="sxs-lookup"><span data-stu-id="81b12-154">Select **Show list**.</span></span>
1. <span data-ttu-id="81b12-155">لكل قالب في القائمة، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="81b12-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="81b12-156">ثم، في الحقل **‏‫البريد الإلكتروني للمرسل‬** ، أدخل عنوان البريد الإلكتروني للمرسل.</span><span class="sxs-lookup"><span data-stu-id="81b12-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="81b12-157">اختياري: في حقل **اسم المرسل** ، أدخل الاسم الذي يجب استخدامه كاسم المرسل.</span><span class="sxs-lookup"><span data-stu-id="81b12-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="81b12-158">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="81b12-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="81b12-159">تخصيص قوالب البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="81b12-159">Customize email templates</span></span>

<span data-ttu-id="81b12-160">قد ترغب في تخصيص قوالب البريد الإلكتروني بحيث تستخدم صورًا مختلفة.</span><span class="sxs-lookup"><span data-stu-id="81b12-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="81b12-161">أو قد ترغب في تحديث الروابط في القوالب بحيث تنتقل إلى بيئة المعاينة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="81b12-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="81b12-162">يشرح هذا الإجراء كيفية تنزيل القوالب الافتراضية وتخصيصها وتحديث القوالب في النظام.</span><span class="sxs-lookup"><span data-stu-id="81b12-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="81b12-163">باستخدام مستعرض، قم بتنزيل [ملف zip. المضغوط لقوالب البريد الإلكتروني الافتراضية لـ Microsoft Dynamics 365 Commerce Preview](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) على الكمبيوتر المحلي الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="81b12-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="81b12-164">يحتوي هذا الملف علي مستندات HTML التالية:</span><span class="sxs-lookup"><span data-stu-id="81b12-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="81b12-165">قالب تأكيد الأمر</span><span class="sxs-lookup"><span data-stu-id="81b12-165">Order confirmation template</span></span>
    - <span data-ttu-id="81b12-166">إصدار قالب بطاقة الهدايا</span><span class="sxs-lookup"><span data-stu-id="81b12-166">Issue gift card template</span></span>
    - <span data-ttu-id="81b12-167">قالب الأمر الجديد</span><span class="sxs-lookup"><span data-stu-id="81b12-167">New order template</span></span>
    - <span data-ttu-id="81b12-168">قالب أمر الحزمة</span><span class="sxs-lookup"><span data-stu-id="81b12-168">Pack order template</span></span>
    - <span data-ttu-id="81b12-169">قالب أمر الانتقاء</span><span class="sxs-lookup"><span data-stu-id="81b12-169">Pick order template</span></span>

1. <span data-ttu-id="81b12-170">قم بتخصيص القوالب باستخدام نص أو محرر HTML.</span><span class="sxs-lookup"><span data-stu-id="81b12-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="81b12-171">راجع قائمة [الرموز المعتمدة](#supported-tokens-in-the-email-template) لاحقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="81b12-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="81b12-172">سجل الدخول إلى Retail.</span><span class="sxs-lookup"><span data-stu-id="81b12-172">Sign in to Retail.</span></span>
1. <span data-ttu-id="81b12-173">باستخدام القائمة الموجودة على اليسار، انتقل إلى **الوحدات النمطية \> ‏‫إدارة المؤسسة‬ \> ‏‫إعداد \> قوالب البريد الإلكتروني للمؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="81b12-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="81b12-174">قم بتوسيع القائمة الموجودة على الجانب الأيمن لمشاهدة كافة القوالب.</span><span class="sxs-lookup"><span data-stu-id="81b12-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="81b12-175">لكل قالب تريد تخصيصه، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="81b12-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="81b12-176">حدد القالب في القائمة.</span><span class="sxs-lookup"><span data-stu-id="81b12-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="81b12-177">ضمن **محتوى رسالة البريد الإلكتروني**‬، حدد نسخة اللغة المناسبة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="81b12-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="81b12-178">اللغة الافتراضية هي **en-us**.</span><span class="sxs-lookup"><span data-stu-id="81b12-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="81b12-179">ضمن **محتوي رسالة البريد الكتروني**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="81b12-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="81b12-180">يظهر جزء **قالب البريد الكتروني الخاص بالتحميل**.</span><span class="sxs-lookup"><span data-stu-id="81b12-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="81b12-181">حدد **استعراض**، وابحث عن ملف HTML الذي يحتوي علي المحتوي المخصص.</span><span class="sxs-lookup"><span data-stu-id="81b12-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="81b12-182">ثم حدد **تحميل**.</span><span class="sxs-lookup"><span data-stu-id="81b12-182">Select **Upload**.</span></span> <span data-ttu-id="81b12-183">يتم تحميل القالب الخاص بك إلى النظام ويتم عرض المعاينة.</span><span class="sxs-lookup"><span data-stu-id="81b12-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="81b12-184">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="81b12-184">Select **OK**.</span></span>
    1. <span data-ttu-id="81b12-185">(اختياري): قم بتخصيص خاصيه **الموضوع** للقالب.</span><span class="sxs-lookup"><span data-stu-id="81b12-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="81b12-186">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="81b12-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="81b12-187">الرموز المعتمدة في قالب البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="81b12-187">Supported tokens in the email template</span></span>

<span data-ttu-id="81b12-188">عند تقديم البريد الإلكتروني، يتم استبدال هذه الرموز المميزة بقيم فعلية تنطبق على العميل وطلب العميل.</span><span class="sxs-lookup"><span data-stu-id="81b12-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="81b12-189">أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="81b12-189">Sales order</span></span>

<span data-ttu-id="81b12-190">تنطبق الرموز المميزة التالية على أمر المبيعات الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="81b12-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="81b12-191">اسم الرمز المميز</span><span class="sxs-lookup"><span data-stu-id="81b12-191">Name of the token</span></span> | <span data-ttu-id="81b12-192">الرمز المميز</span><span class="sxs-lookup"><span data-stu-id="81b12-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="81b12-193">رقم الطلب</span><span class="sxs-lookup"><span data-stu-id="81b12-193">Order number</span></span>      | <span data-ttu-id="81b12-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="81b12-194">%salesid%</span></span> |
| <span data-ttu-id="81b12-195">اسم العميل</span><span class="sxs-lookup"><span data-stu-id="81b12-195">Customer's name</span></span>   | <span data-ttu-id="81b12-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="81b12-196">%customername%</span></span> |
| <span data-ttu-id="81b12-197">عنوان التسليم</span><span class="sxs-lookup"><span data-stu-id="81b12-197">Delivery address</span></span>  | <span data-ttu-id="81b12-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="81b12-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="81b12-199">عنوان الفوترة</span><span class="sxs-lookup"><span data-stu-id="81b12-199">Billing address</span></span>   | <span data-ttu-id="81b12-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="81b12-200">%customeraddress%</span></span> |
| <span data-ttu-id="81b12-201">تاريخ الأمر</span><span class="sxs-lookup"><span data-stu-id="81b12-201">Order date</span></span>        | <span data-ttu-id="81b12-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="81b12-202">%shipdate%</span></span> |
| <span data-ttu-id="81b12-203">وضع التسليم</span><span class="sxs-lookup"><span data-stu-id="81b12-203">Delivery mode</span></span>     | <span data-ttu-id="81b12-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="81b12-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="81b12-205">الخصم</span><span class="sxs-lookup"><span data-stu-id="81b12-205">Discount</span></span>          | <span data-ttu-id="81b12-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="81b12-206">%discount%</span></span> |
| <span data-ttu-id="81b12-207">ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="81b12-207">Sales tax</span></span>         | <span data-ttu-id="81b12-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="81b12-208">%tax%</span></span> |
| <span data-ttu-id="81b12-209">إجمالي الأمر</span><span class="sxs-lookup"><span data-stu-id="81b12-209">Order total</span></span>       | <span data-ttu-id="81b12-210">%total%</span><span class="sxs-lookup"><span data-stu-id="81b12-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="81b12-211">بند مبيعات</span><span class="sxs-lookup"><span data-stu-id="81b12-211">Sales line</span></span>

<span data-ttu-id="81b12-212">يتم استبدال الرموز المميزة التالية بقيم لكل منتج بالترتيب.</span><span class="sxs-lookup"><span data-stu-id="81b12-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="81b12-213">ضع الرمز المميز **قائمة المنتجات - بداية** في بداية كتلة HTML التي تتكرر لكل منتج، ثم ضع الرمز المميز **قائمة المنتجات - نهاية** عند نهاية الكتلة.</span><span class="sxs-lookup"><span data-stu-id="81b12-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="81b12-214">اسم الرمز المميز</span><span class="sxs-lookup"><span data-stu-id="81b12-214">Name of the token</span></span>      | <span data-ttu-id="81b12-215">الرمز المميز</span><span class="sxs-lookup"><span data-stu-id="81b12-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="81b12-216">قائمة المنتجات - بداية</span><span class="sxs-lookup"><span data-stu-id="81b12-216">Product list - start</span></span>   | <span data-ttu-id="81b12-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="81b12-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="81b12-218">قائمة المنتجات - نهاية</span><span class="sxs-lookup"><span data-stu-id="81b12-218">Product list - end</span></span>     | <span data-ttu-id="81b12-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="81b12-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="81b12-220">اسم المنتج</span><span class="sxs-lookup"><span data-stu-id="81b12-220">Product name</span></span>           | <span data-ttu-id="81b12-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="81b12-221">%lineproductname%</span></span> |
| <span data-ttu-id="81b12-222">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="81b12-222">Description</span></span>            | <span data-ttu-id="81b12-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="81b12-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="81b12-224">الكمية</span><span class="sxs-lookup"><span data-stu-id="81b12-224">Quantity</span></span>               | <span data-ttu-id="81b12-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="81b12-225">%linequantity%</span></span> |
| <span data-ttu-id="81b12-226">سعر وحدة البند</span><span class="sxs-lookup"><span data-stu-id="81b12-226">Line unit price</span></span>        | <span data-ttu-id="81b12-227">%lineprice% (التحقق)</span><span class="sxs-lookup"><span data-stu-id="81b12-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="81b12-228">إجمالي أصناف البند</span><span class="sxs-lookup"><span data-stu-id="81b12-228">line item total</span></span>        | <span data-ttu-id="81b12-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="81b12-229">%linenetamount%</span></span> |
| <span data-ttu-id="81b12-230">خصم البند</span><span class="sxs-lookup"><span data-stu-id="81b12-230">line discount</span></span>          | <span data-ttu-id="81b12-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="81b12-231">%linediscount%</span></span> |
| <span data-ttu-id="81b12-232">تاريخ الشحن</span><span class="sxs-lookup"><span data-stu-id="81b12-232">Ship date</span></span>              | <span data-ttu-id="81b12-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="81b12-233">%lineshipdate%</span></span> |
| <span data-ttu-id="81b12-234">أسلوب التدبير</span><span class="sxs-lookup"><span data-stu-id="81b12-234">Procurement method</span></span>     | <span data-ttu-id="81b12-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="81b12-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="81b12-236">عنوان التسليم</span><span class="sxs-lookup"><span data-stu-id="81b12-236">delivery address</span></span>       | <span data-ttu-id="81b12-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="81b12-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="81b12-238">وحده مبيعات البند</span><span class="sxs-lookup"><span data-stu-id="81b12-238">Sales unit of the line</span></span> | <span data-ttu-id="81b12-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="81b12-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="81b12-240">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="81b12-240">Additional resources</span></span>

[<span data-ttu-id="81b12-241">نظرة عامة على بيئة معاينة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="81b12-241">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="81b12-242">تشغيل بيئة معاينة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="81b12-242">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="81b12-243">تكوين بيئة معاينة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="81b12-243">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="81b12-244">الأسئلة المتداولة حول بيئة معاينة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="81b12-244">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="81b12-245">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="81b12-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="81b12-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="81b12-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="81b12-247">مدخل Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="81b12-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="81b12-248">موقع ويب Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="81b12-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
