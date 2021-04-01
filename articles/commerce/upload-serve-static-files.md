---
title: تحميل الملفات الثابتة وخدمتها
description: يوضح هذا الموضوع كيفية تحميل ملف ثابت إلى منشئ موقع Microsoft Dynamics 365 Commerce ، وكيفية إنشاء عنوان URL مخصص واسم ملف يمكن استخدامه لطلب هذا الملف.
author: StuHarg
manager: annbe
ms.date: 11/16/2020
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
ms.openlocfilehash: aba9dde2ed9d5fa09e92fcdd784a53f208930eda
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211009"
---
# <a name="upload-and-serve-static-files"></a><span data-ttu-id="0c160-103">تحميل الملفات الثابتة وخدمتها</span><span class="sxs-lookup"><span data-stu-id="0c160-103">Upload and serve static files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0c160-104">يوضح هذا الموضوع كيفية تحميل ملف ثابت إلى منشئ موقع Microsoft Dynamics 365 Commerce ، وكيفية إنشاء عنوان URL مخصص واسم ملف يمكن استخدامه لطلب هذا الملف.</span><span class="sxs-lookup"><span data-stu-id="0c160-104">This topic describes how to upload a static file into Microsoft Dynamics 365 Commerce site builder, and how to create a custom URL and file name that can be used to request that file.</span></span>

<span data-ttu-id="0c160-105">تتطلب بعض موصلات الجهات الخارجية استضافة ملف وعرضه من موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="0c160-105">Some third-party connectors require that a file be hosted and served from the e-commerce site.</span></span> <span data-ttu-id="0c160-106">وتتوقع هذه الموصلات أنه سيتم إرجاع الملف عن طريق الطلبات إلى مسار URL واسم الملف لرد الاتصال.</span><span class="sxs-lookup"><span data-stu-id="0c160-106">These connectors expect that the file will be returned by requests to a specific callback URL path and file name.</span></span> <span data-ttu-id="0c160-107">لذلك، يشرح هذا الموضوع كيفية تحميل وتقديم ملف ثابت يحتوي على عنوان URL واسم ملف يمكن تعريفهما بواسطة المستخدم على موقع التجارة الإلكترونية لـ Dynamics 365 Commerce .</span><span class="sxs-lookup"><span data-stu-id="0c160-107">Therefore, this topic explains how to upload and serve a static file that has a user-definable URL and file name on a Dynamics 365 Commerce e-commerce site.</span></span>

## <a name="create-a-site-url-that-returns-a-static-file"></a><span data-ttu-id="0c160-108">إنشاء عنوان URL لموقع يقوم بإرجاع ملف ثابت</span><span class="sxs-lookup"><span data-stu-id="0c160-108">Create a site URL that returns a static file</span></span>

<span data-ttu-id="0c160-109">لإنشاء عنوان URL لموقع يقوم بإرجاع ملف ثابت في منشئ موقع التجارة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0c160-109">To create a site URL that returns a static file in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0c160-110">انتقل إلى مكتبة الوسائط الخاصة بموقعك، وقم بتحميل الملف الذي يجب أن تقدمه بواسطة الطلبات إلى عنوان URL الذي ستقوم بتعريفه.</span><span class="sxs-lookup"><span data-stu-id="0c160-110">Go to your site's Media library, and upload the file that should be served by requests to the URL that you will define.</span></span> <span data-ttu-id="0c160-111">إذا قمت بالفعل بتحميل الملف، يمكنك تخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="0c160-111">If you've already uploaded the file, you can skip this step.</span></span>
1. <span data-ttu-id="0c160-112">انتقل إلى **عناوين URL** لموقعك.</span><span class="sxs-lookup"><span data-stu-id="0c160-112">Go to **URLs** for your site.</span></span>
1. <span data-ttu-id="0c160-113">حدد **جديد \> عنوان URL جديد**.</span><span class="sxs-lookup"><span data-stu-id="0c160-113">Select **New \> New URL**.</span></span>
1. <span data-ttu-id="0c160-114">في مربع الحوار **عنوان URL جديد** ، حدد **أصول مكتبة الوسائط**.</span><span class="sxs-lookup"><span data-stu-id="0c160-114">In the **New URL** dialog box, select **Media library asset**.</span></span>
1. <span data-ttu-id="0c160-115">في الحقل **مسار URL** ، أدخل مسار URL.</span><span class="sxs-lookup"><span data-stu-id="0c160-115">In the **URL path** field, enter the URL path.</span></span> <span data-ttu-id="0c160-116">قم بتضمين اسم الملف في المسار.</span><span class="sxs-lookup"><span data-stu-id="0c160-116">Include the file name in the path.</span></span>
1. <span data-ttu-id="0c160-117">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="0c160-117">Select **Next**.</span></span> <span data-ttu-id="0c160-118">يتم فتح مكتبة الوسائط وعرض جميع أصول الوسائط من نوع **المستند** الذي تم تحميله.</span><span class="sxs-lookup"><span data-stu-id="0c160-118">The Media library is opened and shows all media assets of the **document** type that have been uploaded.</span></span>
1. <span data-ttu-id="0c160-119">حدد الملف الذي يجب تقديمه للطلبات إلى عنوان URL الذي حددته في الخطوة 5.</span><span class="sxs-lookup"><span data-stu-id="0c160-119">Select the file that should be served for requests to the URL that you defined in step 5.</span></span>
1. <span data-ttu-id="0c160-120">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0c160-120">Select **Save**.</span></span>

<span data-ttu-id="0c160-121">وفي هذه المرحلة، يكون عنوان URL الذي قمت بإنشائه في حالة المسودة.</span><span class="sxs-lookup"><span data-stu-id="0c160-121">At this point, the URL that you created is in a draft state.</span></span> <span data-ttu-id="0c160-122">لن يتم إرجاع الملف الذي يشير إليه عنوان URL حتى تقوم بنشر عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="0c160-122">The file that the URL points to won't be returned until you publish the URL.</span></span> <span data-ttu-id="0c160-123">قبل نشر عنوان URL، يمكنك التحقق من أنه يقوم بإرجاع البيانات الصحيحة.</span><span class="sxs-lookup"><span data-stu-id="0c160-123">Before you publish the URL, you can validate that it returns the correct data.</span></span>

## <a name="validate-and-publish-a-url"></a><span data-ttu-id="0c160-124">تحقق من صحة عنوان URL وانشره</span><span class="sxs-lookup"><span data-stu-id="0c160-124">Validate and publish a URL</span></span>

<span data-ttu-id="0c160-125">للتحقق من صحة عنوان URL قبل نشره، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="0c160-125">To validate an URL before you publish it, follow these steps.</span></span>

1. <span data-ttu-id="0c160-126">انتقل إلى **عناوين URL** لموقعك، وحدد عنوان URL لمعاينته.</span><span class="sxs-lookup"><span data-stu-id="0c160-126">Go to **URLs** for your site, and select the URL to preview.</span></span>
2. <span data-ttu-id="0c160-127">في جزء الخصائص على اليمين، أسفل الزر **تحرير** ، حدد ارتباط عنوان URL الصحيح.</span><span class="sxs-lookup"><span data-stu-id="0c160-127">In the properties pane on the right, below the **Edit** button, select the correct URL link.</span></span> <span data-ttu-id="0c160-128">يتم فتح نافذة متصفح جديدة، ويتعين أن تتلقى خطأ 404.</span><span class="sxs-lookup"><span data-stu-id="0c160-128">A new browser window is opened, and you should receive a 404 error.</span></span>
3. <span data-ttu-id="0c160-129">قم بإلحاق سلسلة الاستعلام **?preview=inprogress** بعنوان URL (على سبيل المثال، `https://yoursite.com/callback.html?preview=inprogress`)، وأعد تحميل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0c160-129">Append the **?preview=inprogress** query string to the URL (for example, `https://yoursite.com/callback.html?preview=inprogress`), and reload the page.</span></span> <span data-ttu-id="0c160-130">يجب إرجاع الملف الذي قمت بتحميله إلى مكتبة الوسائط في الاستجابة.</span><span class="sxs-lookup"><span data-stu-id="0c160-130">The file that you uploaded to the Media library should be returned in the response.</span></span>

<span data-ttu-id="0c160-131">بعد التحقق من صحة عنوان URL، يمكنك نشره.</span><span class="sxs-lookup"><span data-stu-id="0c160-131">After you've validated the URL, you can publish it.</span></span>

1. <span data-ttu-id="0c160-132">انتقل إلى **عناوين URL** لموقعك، وحدد عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="0c160-132">Go to **URLs** for your site, and select the URL.</span></span>
2. <span data-ttu-id="0c160-133">في شريط الأوامر، حدد **نشر** .</span><span class="sxs-lookup"><span data-stu-id="0c160-133">Select **Publish** on the command bar.</span></span>

## <a name="update-the-file-that-a-url-points-to"></a><span data-ttu-id="0c160-134">قم بتحديث الملف الذي يشير إليه عنوان URL</span><span class="sxs-lookup"><span data-stu-id="0c160-134">Update the file that a URL points to</span></span>

<span data-ttu-id="0c160-135">بعد نشر عنوان URL، يمكنك تحديثه بحيث يشير إلى ملف مختلف.</span><span class="sxs-lookup"><span data-stu-id="0c160-135">After a URL is published, you can update it so that it points to a different file.</span></span> <span data-ttu-id="0c160-136">بدلاً من ذلك، يمكنك تحديث عنوان URL بحيث يشير إلى نوع مختلف من الموارد، كما هو موضح في القسم التالي.</span><span class="sxs-lookup"><span data-stu-id="0c160-136">Alternatively, you can update the URL so that it points to a different the type of resource, as described in the next section.</span></span> <span data-ttu-id="0c160-137">على سبيل المثال، يمكنك توجيه عنوان URL إلى صفحة داخلية أو إعادة توجيه.</span><span class="sxs-lookup"><span data-stu-id="0c160-137">For example, you can point the URL to an internal page or a redirect.</span></span>

<span data-ttu-id="0c160-138">لتحديث الملف الذي يشير إليه عنوان URL، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="0c160-138">To update the file that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="0c160-139">انتقل إلى **عناوين URL** لموقعك، وحدد عنوان URL لتحديثه.</span><span class="sxs-lookup"><span data-stu-id="0c160-139">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="0c160-140">في جزء الخصائص على اليمين، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="0c160-140">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="0c160-141">ضمن **تعيين عنوان URL**، حدد المربع **الخطوة 2** ، ثم حدد مستندًا جديدًا من مكتبه الوسائط.</span><span class="sxs-lookup"><span data-stu-id="0c160-141">Under **URL assignment**, select the **Step 2** box, and then select a new document from the Media library.</span></span>
1. <span data-ttu-id="0c160-142">حدد **تطبيق**.</span><span class="sxs-lookup"><span data-stu-id="0c160-142">Select **Apply**.</span></span>

## <a name="update-the-asset-type-that-a-url-points-to"></a><span data-ttu-id="0c160-143">قم بتحديث نوع الأصل الذي يشير إليه عنوان URL</span><span class="sxs-lookup"><span data-stu-id="0c160-143">Update the asset type that a URL points to</span></span>

<span data-ttu-id="0c160-144">يمكنك أيضًا تحديث عنوان URL بحيث يشير إلى نوع مختلف من الأصول (الموارد)، مثل صفحة داخلية أو إعادة توجيه.</span><span class="sxs-lookup"><span data-stu-id="0c160-144">You can also update a URL so that it points to a different type of asset (resource), such as an internal page or a redirect.</span></span>

<span data-ttu-id="0c160-145">لتحديث نوع الأصل الذي يشير إليه عنوان URL، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="0c160-145">To update the asset type that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="0c160-146">انتقل إلى **عناوين URL** لموقعك، وحدد عنوان URL لتحديثه.</span><span class="sxs-lookup"><span data-stu-id="0c160-146">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="0c160-147">في جزء الخصائص على اليمين، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="0c160-147">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="0c160-148">ضمن **تعيين عنوان URL** ، ضمن **الخطوة 1**، حدد نوع أصل مختلف.</span><span class="sxs-lookup"><span data-stu-id="0c160-148">Under **URL assignment**, under **Step 1**, select a different asset type.</span></span>
1. <span data-ttu-id="0c160-149">حدد المربع **الخطوة 2** ، ثم حدد الأصل الجديد.</span><span class="sxs-lookup"><span data-stu-id="0c160-149">Select the **Step 2** box, and then select the new asset.</span></span>
1. <span data-ttu-id="0c160-150">حدد **تطبيق**.</span><span class="sxs-lookup"><span data-stu-id="0c160-150">Select **Apply**.</span></span>

## <a name="change-the-url-path"></a><span data-ttu-id="0c160-151">تغيير مسار URL</span><span class="sxs-lookup"><span data-stu-id="0c160-151">Change the URL path</span></span>

<span data-ttu-id="0c160-152">بعد إنشاء عنوان URL، لا يمكن تغيير مساره.</span><span class="sxs-lookup"><span data-stu-id="0c160-152">After a URL is created, its path can't be changed.</span></span> <span data-ttu-id="0c160-153">إذا كان يجب عليك تغيير مسار عنوان URL الذي يخدم ملفًا أو أي نوع آخر من الموارد، فيتعين عليك إنشاء عنوان URL جديد، وتعيينه إلى الملف الموجود أو مورد آخر، ثم إلغاء نشر عنوان URL القديم وحذفه.</span><span class="sxs-lookup"><span data-stu-id="0c160-153">If you must change the URL path that serves a file or any other type of resource, you have to create a new URL, map it to the existing file or other resource, and then unpublish and delete the old URL.</span></span>

<span data-ttu-id="0c160-154">لتغيير مسار عنوان URL، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="0c160-154">To change the URL path, follow these steps.</span></span>

1. <span data-ttu-id="0c160-155">لإنشاء عنوان URL جديد وتعيينه إلى الملف الحالي أو مورد آخر، اتبع التعليمات الواردة في القسم [‏‫إنشاء عنوان URL لموقع يقوم بإرجاع ملف ثابت](#create-a-site-url-that-returns-a-static-file) سابقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="0c160-155">To create a new URL and map it to the existing file or another resource, follow the instructions in the [Create a site URL that returns a static file](#create-a-site-url-that-returns-a-static-file) section earlier in this topic.</span></span>
1. <span data-ttu-id="0c160-156">حدد عنوان URL الجديد، وحدد **نشر** في شريط الأوامر.</span><span class="sxs-lookup"><span data-stu-id="0c160-156">Select the new URL, and select **Publish** on the command bar.</span></span> <span data-ttu-id="0c160-157">يتم نشر عنوان URL الجديد.</span><span class="sxs-lookup"><span data-stu-id="0c160-157">The new URL is published.</span></span>
1. <span data-ttu-id="0c160-158">لإلغاء نشر عنوان URL القديم، حدده ، ثم حدد **إلغاء النشر** في شريط الأوامر.</span><span class="sxs-lookup"><span data-stu-id="0c160-158">To unpublish the old URL, select it, and then select **Unpublish** on the command bar.</span></span> <span data-ttu-id="0c160-159">يمكنك الآن حذف عنوان URL القديم إذا كنت تري ذلك.</span><span class="sxs-lookup"><span data-stu-id="0c160-159">You can now delete the old URL if you want.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c160-160">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0c160-160">Additional resources</span></span>

[<span data-ttu-id="0c160-161">نظرة عامة على إدارة الأصول الرقمية</span><span class="sxs-lookup"><span data-stu-id="0c160-161">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="0c160-162">تحميل صور</span><span class="sxs-lookup"><span data-stu-id="0c160-162">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="0c160-163">تحميل مقاطع فيديو</span><span class="sxs-lookup"><span data-stu-id="0c160-163">Upload videos</span></span>](dam-upload-video.md)

[<span data-ttu-id="0c160-164">تحميل ملفات غير الصور ومقاطع الفيديو</span><span class="sxs-lookup"><span data-stu-id="0c160-164">Upload files other than images and videos</span></span>](dam-upload-files.md)

[<span data-ttu-id="0c160-165">اقتصاص الصور</span><span class="sxs-lookup"><span data-stu-id="0c160-165">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="0c160-166">تخصيص نقاط تركيز الصورة</span><span class="sxs-lookup"><span data-stu-id="0c160-166">Customize image focal points</span></span>](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]