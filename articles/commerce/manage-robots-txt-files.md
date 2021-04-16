---
title: إدارة ملفات robots.txt
description: يصف هذا الموضوع كيفية إدارة ملفات robots.txt في Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9b832d6714447f8957095c8c87d48527087f12d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794225"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="cfe79-103">إدارة ملفات robots.txt</span><span class="sxs-lookup"><span data-stu-id="cfe79-103">Manage robots.txt files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cfe79-104">يصف هذا الموضوع كيفية إدارة ملفات robots.txt في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cfe79-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cfe79-105">يُعد معيار استبعاد الروبوتات، أو robots.txt، معيارًا تستخدمه المواقع الإلكترونية للتواصل مع روبوتات الويب.</span><span class="sxs-lookup"><span data-stu-id="cfe79-105">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="cfe79-106">فإنه يرشد روبوتات الويب إلى أية مناطق من موقع ويب لا ينبغي زيارته.</span><span class="sxs-lookup"><span data-stu-id="cfe79-106">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="cfe79-107">وغالبا ما تستخدم الروبوتات من قبل محركات البحث لفهرسة مواقع الويب.</span><span class="sxs-lookup"><span data-stu-id="cfe79-107">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="cfe79-108">لاستبعاد الروبوتات من خادم، فإنه يمكنك إنشاء ملف على الخادم.</span><span class="sxs-lookup"><span data-stu-id="cfe79-108">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="cfe79-109">في هذا الملف، يمكنك تحديد نهج وصول للروبوتات.</span><span class="sxs-lookup"><span data-stu-id="cfe79-109">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="cfe79-110">يجب أن يكون الملف قابلاً للوصول عبر HTTP في عنوان URL المحلي **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="cfe79-110">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="cfe79-111">يساعد ملف robots.txt محركات البحث في فهرسة المحتوى على موقعك.</span><span class="sxs-lookup"><span data-stu-id="cfe79-111">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="cfe79-112">يتيح لك Dynamics 365 Commerce تحميل ملف robots.txt للمجال الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="cfe79-112">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="cfe79-113">بالنسبة لكل مجال في بيئة Commerce الخاصة بك، يمكنك تحميل ملف robots.txt واحد وربطه بذلك المجال.</span><span class="sxs-lookup"><span data-stu-id="cfe79-113">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="cfe79-114">لمزيد من المعلومات حول ملف robots.txt، قم بزيارة [صفحات روبوتات الويب](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="cfe79-114">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="cfe79-115">تحميل ملف robots.txt</span><span class="sxs-lookup"><span data-stu-id="cfe79-115">Upload a robots.txt file</span></span>

<span data-ttu-id="cfe79-116">بعد أن تقوم بإنشاء ملف robots.txt وتحريره وفقًا [لمعيار استبعاد الروبوتات](https://www.robotstxt.org/orig.html)، تأكد من إمكانية الوصول إلى الملف على الكمبيوتر حيث ستقوم باستخدام أدوات تأليف Commerce .</span><span class="sxs-lookup"><span data-stu-id="cfe79-116">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="cfe79-117">يجب أن يكون الملف باسم **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="cfe79-117">The file must be named **robots.txt**.</span></span> <span data-ttu-id="cfe79-118">للحصول على أفضل النتائج، فإنه يجب أن يكون بالتنسيق المُشار إليه في المعيار.</span><span class="sxs-lookup"><span data-stu-id="cfe79-118">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="cfe79-119">يكون كل عميل من عملاء Commerce مسؤولاً عن التحقق من صحة محتويات ملف robots.txt الخاص به والاحتفاظ به.</span><span class="sxs-lookup"><span data-stu-id="cfe79-119">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="cfe79-120">لتحميل ملف robots.txt، فإنه يجب أن تقوم بتسجيل الدخول إلى Commerce بصفتك مسؤول نظام.</span><span class="sxs-lookup"><span data-stu-id="cfe79-120">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="cfe79-121">لتحميل ملف robots.txt إلى موقعك في Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="cfe79-121">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="cfe79-122">قم بتسجيل الدخول إلى Commerce بصفتك مسؤول نظام.</span><span class="sxs-lookup"><span data-stu-id="cfe79-122">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="cfe79-123">في جزء التنقل الأيمن، حدد **إعدادات المستأجر** (بجانب رمز الترس) لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="cfe79-123">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="cfe79-124">ضمن **إعدادات المستأجر**، حدد **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="cfe79-124">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="cfe79-125">تظهر قائمة بكافة المجالات المقترنة بالبيئة الخاصة بك في الجزء الرئيسي من النافذة.</span><span class="sxs-lookup"><span data-stu-id="cfe79-125">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="cfe79-126">حدد **إدارة** لتحميل ملف robots.txt لمجال في البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="cfe79-126">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="cfe79-127">في القائمة الموجودة على اليمين، حدد الزر **تحميل** (السهم المشير لأعلى) بجوار المجال المقترن بملف robots.txt.</span><span class="sxs-lookup"><span data-stu-id="cfe79-127">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="cfe79-128">يظهر مربع حوار مستعرض ملف.</span><span class="sxs-lookup"><span data-stu-id="cfe79-128">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="cfe79-129">في مربع الحوار، استعرض ملف robots.txt الذي تريد تحميله للمجال المقترن وحدده، ثم حدد **فتح** لإكمال التحميل.</span><span class="sxs-lookup"><span data-stu-id="cfe79-129">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="cfe79-130">أثناء التحميل، يتحقق Commerce من أن الملف هو ملف نصي، ولكنه لا يتحقق من صحة محتويات الملف.</span><span class="sxs-lookup"><span data-stu-id="cfe79-130">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="cfe79-131">تنزيل ملف robots.txt</span><span class="sxs-lookup"><span data-stu-id="cfe79-131">Download a robots.txt file</span></span>

<span data-ttu-id="cfe79-132">لتنزيل ملف robots.txt إلى موقعك في Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="cfe79-132">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="cfe79-133">قم بتسجيل الدخول إلى Commerce بصفتك مسؤول نظام.</span><span class="sxs-lookup"><span data-stu-id="cfe79-133">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="cfe79-134">في جزء التنقل الأيمن، حدد **إعدادات المستأجر** (بجانب رمز الترس) لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="cfe79-134">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="cfe79-135">ضمن **إعدادات المستأجر**، حدد **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="cfe79-135">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="cfe79-136">تظهر قائمة بكافة المجالات المقترنة بالبيئة الخاصة بك في الجزء الرئيسي من النافذة.</span><span class="sxs-lookup"><span data-stu-id="cfe79-136">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="cfe79-137">حدد **إدارة** لتنزيل ملف robots.txt لمجال في البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="cfe79-137">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="cfe79-138">في القائمة الموجودة على اليمين، حدد الزر **تنزيل** (السهم المشير لأسفل) بجوار المجال المقترن بملف robots.txt.</span><span class="sxs-lookup"><span data-stu-id="cfe79-138">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="cfe79-139">يظهر مربع حوار مستعرض ملف.</span><span class="sxs-lookup"><span data-stu-id="cfe79-139">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="cfe79-140">في مربع الحوار، انتقل إلى الموقع المطلوب على محرك الأقراص المحلي، وقم بتأكيد اسم الملف أو إدخاله، ثم حدد **حفظ** لإكمال التنزيل.</span><span class="sxs-lookup"><span data-stu-id="cfe79-140">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="cfe79-141">يمكن استخدام هذا الإجراء لتنزيل ملفات robots.txt فقط التي تم تحميلها مسبقًا عبر أدوات تأليف Commerce.</span><span class="sxs-lookup"><span data-stu-id="cfe79-141">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="cfe79-142">حذف ملف robots.txt</span><span class="sxs-lookup"><span data-stu-id="cfe79-142">Delete a robots.txt file</span></span>

<span data-ttu-id="cfe79-143">لحذف ملف robots.txt إلى موقعك في Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="cfe79-143">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="cfe79-144">قم بتسجيل الدخول إلى Commerce بصفتك مسؤول نظام.</span><span class="sxs-lookup"><span data-stu-id="cfe79-144">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="cfe79-145">في جزء التنقل الأيمن، حدد **إعدادات المستأجر** (بجانب رمز الترس) لتوسيعه.</span><span class="sxs-lookup"><span data-stu-id="cfe79-145">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="cfe79-146">ضمن **إعدادات المستأجر**، حدد **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="cfe79-146">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="cfe79-147">تظهر قائمة بكافة المجالات المقترنة بالبيئة الخاصة بك في الجزء الرئيسي من النافذة.</span><span class="sxs-lookup"><span data-stu-id="cfe79-147">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="cfe79-148">حدد **إدارة** لحذف ملف robots.txt لمجال في البيئة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="cfe79-148">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="cfe79-149">في القائمة الموجودة على اليمين، حدد الزر **حذف** (رمز سلة المهملات) بجوار المجال المقترن بملف robots.txt.</span><span class="sxs-lookup"><span data-stu-id="cfe79-149">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="cfe79-150">تظهر نافذة مستعرض الملف.</span><span class="sxs-lookup"><span data-stu-id="cfe79-150">A file browser window appears.</span></span>
6. <span data-ttu-id="cfe79-151">في نافذة مستعرض الملف، استعرض ملف robots.txt الذي تريد حذفه للمجال المقترن وحدده، ثم حدد **فتح**.</span><span class="sxs-lookup"><span data-stu-id="cfe79-151">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="cfe79-152">يظهر مربع رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="cfe79-152">A warning message box appears.</span></span>
7. <span data-ttu-id="cfe79-153">في مربع الرسالة، حدد **حذف** لتأكيد حذف ملف robots.txt.</span><span class="sxs-lookup"><span data-stu-id="cfe79-153">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="cfe79-154">يمكن استخدام هذا الإجراء لحذف ملفات robots.txt فقط التي تم تحميلها مسبقًا عبر أدوات تأليف Commerce.</span><span class="sxs-lookup"><span data-stu-id="cfe79-154">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cfe79-155">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="cfe79-155">Additional resources</span></span>

[<span data-ttu-id="cfe79-156">تكوين اسم مجالك</span><span class="sxs-lookup"><span data-stu-id="cfe79-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="cfe79-157">نشر مستأجر التجارة الإلكترونية الجديد</span><span class="sxs-lookup"><span data-stu-id="cfe79-157">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="cfe79-158">إنشاء موقع تجارة إلكترونية</span><span class="sxs-lookup"><span data-stu-id="cfe79-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="cfe79-159">إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="cfe79-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="cfe79-160">تحميل عناوين URL لإعادة التوجيه‬ بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="cfe79-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="cfe79-161">إعداد مستأجر متاجرة عمل-مستهلك في Commerce</span><span class="sxs-lookup"><span data-stu-id="cfe79-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="cfe79-162">إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين</span><span class="sxs-lookup"><span data-stu-id="cfe79-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="cfe79-163">تكوين مستأجرين متعددين لمتاجرة عمل-مستهلك في بيئة Commerce</span><span class="sxs-lookup"><span data-stu-id="cfe79-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="cfe79-164">إضافة الدعم إلى شبكة تسليم المحتوى (CDN)</span><span class="sxs-lookup"><span data-stu-id="cfe79-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="cfe79-165">تمكين اكتشاف المتجر استنادًا إلى الموقع</span><span class="sxs-lookup"><span data-stu-id="cfe79-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
