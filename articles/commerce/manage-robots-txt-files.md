---
title: إدارة ملفات robots.txt
description: يصف هذا الموضوع كيفية إدارة ملفات robots.txt في Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: ad87594b9c20d0c2b53e8d4e7c1170a78babe74b
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517442"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="a3906-103">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="a3906-103">Manage robots.txt files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a3906-104">يصف هذا الموضوع كيفية إدارة ملفات robots.txt في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a3906-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a3906-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="a3906-105">Overview</span></span>

<span data-ttu-id="a3906-106">يُعد معيار استبعاد الروبوتات، أو robots.txt، معيارًا تستخدمه المواقع الإلكترونية للتواصل مع روبوتات الويب.</span><span class="sxs-lookup"><span data-stu-id="a3906-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="a3906-107">فإنه يرشد روبوتات الويب إلى أية مناطق من موقع ويب لا ينبغي زيارته.</span><span class="sxs-lookup"><span data-stu-id="a3906-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="a3906-108">وغالبا ما تستخدم الروبوتات من قبل محركات البحث لفهرسة مواقع الويب.</span><span class="sxs-lookup"><span data-stu-id="a3906-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="a3906-109">لاستبعاد الروبوتات من خادم، فإنه يمكنك إنشاء ملف على الخادم.</span><span class="sxs-lookup"><span data-stu-id="a3906-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="a3906-110">في هذا الملف، يمكنك تحديد نهج وصول للروبوتات.</span><span class="sxs-lookup"><span data-stu-id="a3906-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="a3906-111">يجب أن يكون الملف قابلاً للوصول عبر HTTP في عنوان URL المحلي **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="a3906-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="a3906-112">يساعد ملف robots.txt محركات البحث في فهرسة المحتوى على موقعك.</span><span class="sxs-lookup"><span data-stu-id="a3906-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="a3906-113">يتيح لك Dynamics 365 Commerce تحميل ملف robots.txt للمجال الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="a3906-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="a3906-114">بالنسبة لكل مجال في بيئة Commerce الخاصة بك، يمكنك تحميل ملف robots.txt واحد وربطه بذلك المجال.</span><span class="sxs-lookup"><span data-stu-id="a3906-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="a3906-115">لمزيد من المعلومات حول ملف robots.txt، قم بزيارة [صفحات روبوتات الويب](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="a3906-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="a3906-116">تحميل ملف robots.txt</span><span class="sxs-lookup"><span data-stu-id="a3906-116">Upload a robots.txt file</span></span>

<span data-ttu-id="a3906-117">بعد أن تقوم بإنشاء ملف robots.txt وتحريره وفقًا [لمعيار استبعاد الروبوتات](https://www.robotstxt.org/orig.html)، تأكد من إمكانية الوصول إلى الملف على الكمبيوتر حيث ستقوم باستخدام أدوات تأليف Commerce .</span><span class="sxs-lookup"><span data-stu-id="a3906-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="a3906-118">يجب أن يكون الملف باسم **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="a3906-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="a3906-119">للحصول على أفضل النتائج، فإنه يجب أن يكون بالتنسيق المُشار إليه في المعيار.</span><span class="sxs-lookup"><span data-stu-id="a3906-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="a3906-120">يكون كل عميل من عملاء Commerce مسؤولاً عن التحقق من صحة محتويات ملف robots.txt الخاص به والاحتفاظ به.</span><span class="sxs-lookup"><span data-stu-id="a3906-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="a3906-121">لتحميل ملف robots.txt، فإنه يجب أن تقوم بتسجيل الدخول إلى Commerce بصفتك مسؤول نظام.</span><span class="sxs-lookup"><span data-stu-id="a3906-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="a3906-122">لتحميل ملف robots.txt إلى موقعك في Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="a3906-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="a3906-123">قم بتسجيل الدخول إلى Commerce بصفتك مسؤول نظام.</span><span class="sxs-lookup"><span data-stu-id="a3906-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="a3906-124">في جزء التنقل الأيمن، حدد **إعدادات المستأجر** (بجانب رمز الترس) لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="a3906-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="a3906-125">ضمن **إعدادات المستأجر**، حدد **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="a3906-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="a3906-126">تظهر قائمة بكافة المجالات المقترنة بالبيئة الخاصة بك في الجزء الرئيسي من النافذة.</span><span class="sxs-lookup"><span data-stu-id="a3906-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="a3906-127">حدد **إدارة** لتحميل ملف robots.txt لمجال في البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="a3906-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="a3906-128">في القائمة الموجودة على اليمين، حدد الزر **تحميل** (السهم المشير لأعلى) بجوار المجال المقترن بملف robots.txt.</span><span class="sxs-lookup"><span data-stu-id="a3906-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="a3906-129">يظهر مربع حوار مستعرض ملف.</span><span class="sxs-lookup"><span data-stu-id="a3906-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="a3906-130">في مربع الحوار، استعرض ملف robots.txt الذي تريد تحميله للمجال المقترن وحدده، ثم حدد **فتح** لإكمال التحميل.</span><span class="sxs-lookup"><span data-stu-id="a3906-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="a3906-131">أثناء التحميل، يتحقق Commerce من أن الملف هو ملف نصي، ولكنه لا يتحقق من صحة محتويات الملف.</span><span class="sxs-lookup"><span data-stu-id="a3906-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="a3906-132">تنزيل ملف robots.txt</span><span class="sxs-lookup"><span data-stu-id="a3906-132">Download a robots.txt file</span></span>

<span data-ttu-id="a3906-133">لتنزيل ملف robots.txt إلى موقعك في Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="a3906-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="a3906-134">قم بتسجيل الدخول إلى Commerce بصفتك مسؤول نظام.</span><span class="sxs-lookup"><span data-stu-id="a3906-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="a3906-135">في جزء التنقل الأيمن، حدد **إعدادات المستأجر** (بجانب رمز الترس) لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="a3906-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="a3906-136">ضمن **إعدادات المستأجر**، حدد **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="a3906-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="a3906-137">تظهر قائمة بكافة المجالات المقترنة بالبيئة الخاصة بك في الجزء الرئيسي من النافذة.</span><span class="sxs-lookup"><span data-stu-id="a3906-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="a3906-138">حدد **إدارة** لتنزيل ملف robots.txt لمجال في البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="a3906-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="a3906-139">في القائمة الموجودة على اليمين، حدد الزر **تنزيل** (السهم المشير لأسفل) بجوار المجال المقترن بملف robots.txt.</span><span class="sxs-lookup"><span data-stu-id="a3906-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="a3906-140">يظهر مربع حوار مستعرض ملف.</span><span class="sxs-lookup"><span data-stu-id="a3906-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="a3906-141">في مربع الحوار، انتقل إلى الموقع المطلوب على محرك الأقراص المحلي، وقم بتأكيد اسم الملف أو إدخاله، ثم حدد **حفظ** لإكمال التنزيل.</span><span class="sxs-lookup"><span data-stu-id="a3906-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="a3906-142">يمكن استخدام هذا الإجراء لتنزيل ملفات robots.txt فقط التي تم تحميلها مسبقًا عبر أدوات تأليف Commerce.</span><span class="sxs-lookup"><span data-stu-id="a3906-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="a3906-143">حذف ملف robots.txt</span><span class="sxs-lookup"><span data-stu-id="a3906-143">Delete a robots.txt file</span></span>

<span data-ttu-id="a3906-144">لحذف ملف robots.txt إلى موقعك في Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="a3906-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="a3906-145">قم بتسجيل الدخول إلى Commerce بصفتك مسؤول نظام.</span><span class="sxs-lookup"><span data-stu-id="a3906-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="a3906-146">في جزء التنقل الأيمن، حدد **إعدادات المستأجر** (بجانب رمز الترس) لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="a3906-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="a3906-147">ضمن **إعدادات المستأجر**، حدد **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="a3906-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="a3906-148">تظهر قائمة بكافة المجالات المقترنة بالبيئة الخاصة بك في الجزء الرئيسي من النافذة.</span><span class="sxs-lookup"><span data-stu-id="a3906-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="a3906-149">حدد **إدارة** لحذف ملف robots.txt لمجال في البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="a3906-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="a3906-150">في القائمة الموجودة على اليمين، حدد الزر **حذف** (رمز سلة المهملات) بجوار المجال المقترن بملف robots.txt.</span><span class="sxs-lookup"><span data-stu-id="a3906-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="a3906-151">تظهر نافذة مستعرض الملف.</span><span class="sxs-lookup"><span data-stu-id="a3906-151">A file browser window appears.</span></span>
6. <span data-ttu-id="a3906-152">في نافذة مستعرض الملف، استعرض ملف robots.txt الذي تريد حذفه للمجال المقترن وحدده، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="a3906-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="a3906-153">يظهر مربع رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="a3906-153">A warning message box appears.</span></span>
7. <span data-ttu-id="a3906-154">في مربع الرسالة، حدد **حذف** لتأكيد حذف ملف robots.txt.</span><span class="sxs-lookup"><span data-stu-id="a3906-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="a3906-155">يمكن استخدام هذا الإجراء لحذف ملفات robots.txt فقط التي تم تحميلها مسبقًا عبر أدوات تأليف Commerce.</span><span class="sxs-lookup"><span data-stu-id="a3906-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a3906-156">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a3906-156">Additional resources</span></span>

[<span data-ttu-id="a3906-157">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="a3906-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="a3906-158">نشر مستأجر التجارة الإلكترونية الجديد</span><span class="sxs-lookup"><span data-stu-id="a3906-158">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="a3906-159">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="a3906-159">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="a3906-160">إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="a3906-160">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="a3906-161">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="a3906-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="a3906-162">إعداد مستأجر متاجرة عمل-مستهلك في Commerce</span><span class="sxs-lookup"><span data-stu-id="a3906-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="a3906-163">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="a3906-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="a3906-164">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="a3906-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="a3906-165">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="a3906-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="a3906-166">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="a3906-166">Enable location-based store detection</span></span>](enable-store-detection.md)
