---
title: تعديل صفحة موقع موجودة
description: يصف هذا الموضوع كيفية تعديل صفحة موقع موجودة في Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 47a7d17b97631ba469a9b68f5f6cf492ebccde6f
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097296"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="9c4db-103">تعديل صفحة موقع موجودة</span><span class="sxs-lookup"><span data-stu-id="9c4db-103">Modify an existing site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9c4db-104">يصف هذا الموضوع كيفية تعديل صفحة موقع موجودة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9c4db-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9c4db-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="9c4db-105">Overview</span></span>

<span data-ttu-id="9c4db-106">عندما تكون مضطرًا لتعديل صفحة، تكون الخطوة الأولي هي فتحها في محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9c4db-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="9c4db-107">انتقل إلى الموقع الذي يحتوي على الصفحة الخاصة بك، ثم في قائمة الصفحات، ابحث عن الصفحة التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="9c4db-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="9c4db-108">إذا لم تتمكن من العثور على الصفحة، يمكنك استخدام وظيفة البحث المتعمق لأداه التأليف.</span><span class="sxs-lookup"><span data-stu-id="9c4db-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="9c4db-109">إما أن تكتب اسم الصفحة بالضبط، أو تكتب الأحرف الأولى منها ثم علامة (\*).</span><span class="sxs-lookup"><span data-stu-id="9c4db-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="9c4db-110">تظهر قائمة من الصفحات المصفاة.</span><span class="sxs-lookup"><span data-stu-id="9c4db-110">A filtered list of pages appears.</span></span> <span data-ttu-id="9c4db-111">يمكنك استخدام هذه القائمة للعثور على الصفحة التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="9c4db-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="9c4db-112">بعد العثور علي الصفحة الصحيحة، حدد اسم الصفحة لفتح الصفحة في محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9c4db-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="9c4db-113">إذا كانت الصفحة مرئية في مفتش الصفحة، يمكنك تحديد **تحرير** الصفحة وإخراجها قبل فتحها في محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9c4db-113">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="9c4db-114">بهذه الطريقة، يمكنك سحب صفحات متعددة في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="9c4db-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="9c4db-115">بعد فتح الصفحة في محرر الصفحة، يجب التأكد منه قد تم سحبها.</span><span class="sxs-lookup"><span data-stu-id="9c4db-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="9c4db-116">شريط الأوامر في أداه التأليف يكون ديناميكيًا، حساس للسياق، وحساس للحالة.</span><span class="sxs-lookup"><span data-stu-id="9c4db-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="9c4db-117">لذلك، يعرض فقط الإجراءات التي يمكنك تنفيذها حاليًا في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9c4db-117">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="9c4db-118">على سبيل المثال، إذا لم يتم إخراج الصفحة لك، فلن يظهر الزران **حفظ** و **إنهاء التحرير** في شريط الأوامر.</span><span class="sxs-lookup"><span data-stu-id="9c4db-118">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="9c4db-119">تظهر حالة الصفحة كذلك في الجانب الأيسر من النافذة.</span><span class="sxs-lookup"><span data-stu-id="9c4db-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="9c4db-120">إذا لم يتم إخراج الصفحة بالفعل لك، فحدد **تحرير** في شريط الأوامر.</span><span class="sxs-lookup"><span data-stu-id="9c4db-120">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="9c4db-121">يتغير شريط الأوامر ليعكس الحالة الجديدة للصفحة.</span><span class="sxs-lookup"><span data-stu-id="9c4db-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="9c4db-122">كما تتلقي إعلامًا يوضح أن الصفحة تم سحبها لك.</span><span class="sxs-lookup"><span data-stu-id="9c4db-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="9c4db-123">الخطوة التالية هي إجراء تغييرات فعلية.</span><span class="sxs-lookup"><span data-stu-id="9c4db-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="9c4db-124">غالبا، ستستخدم شجرة المخطط التفصيلي للصفحة الموجود على الجانب الأيمن للبحث عن الوحدة النمطية التي ترغب في تغييرها وتحديدها، ثم إجراء التغييرات في جزء الخصائص الموجود على الجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="9c4db-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="9c4db-125">ومع ذلك، قد يتضمن التغيير الخاص بك أحيانا إضافه نماذج أو أجزاء أو إزالتها.</span><span class="sxs-lookup"><span data-stu-id="9c4db-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="9c4db-126">لإضافة جزء أو وحدة نمطية، استخدم شجره المخطط التفصيلي للصفحة للعثور علي الفتحة التي تريد إضافة الوحدة النمطية أو الجزء إليها، ثم حدد زر علامة الحذف (**...**) لهذه الفتحة.</span><span class="sxs-lookup"><span data-stu-id="9c4db-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="9c4db-127">تظهر قائمة تتضمن أوامر لإضافة وحدة نمطية أو جزء.</span><span class="sxs-lookup"><span data-stu-id="9c4db-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="9c4db-128">لإزالة وحدة نمطية أو جزء، ابحث عنه وحدده في شجرة المخطط التفصيلي للصفحة، وحدد زر علامة الحذف، ثم حدد الأمر لحذف الوحدة النمطية أو الجزء.</span><span class="sxs-lookup"><span data-stu-id="9c4db-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="9c4db-129">يمكنك أيضًا عرض وتحرير الخصائص لأي وحدة نمطية مرئية في معاينة أداة إنشاء الصفحات المرئية بتحديدها مباشرة.</span><span class="sxs-lookup"><span data-stu-id="9c4db-129">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="9c4db-130">بعد الانتهاء من إجراء التغييرات ومعاينة تأثيرها، يجب عليك إخراج الصفحة عن طريق تحديد **إنهاء التحرير** في شريط الأوامر.</span><span class="sxs-lookup"><span data-stu-id="9c4db-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="9c4db-131">لنشر التغييرات مباشرة، حدد **نشر** من شريط الأوامر.</span><span class="sxs-lookup"><span data-stu-id="9c4db-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="9c4db-132">يتم نشر آخر إصدار تم إيداعه من الصفحة التي قمت بتعديلها ويصبح متوفرا للمستخدمين الخارجيين الذين يعرضون الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="9c4db-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="9c4db-133">مثال: تغيير الفيديو على الصفحة الرئيسية</span><span class="sxs-lookup"><span data-stu-id="9c4db-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="9c4db-134">يوضح المثال التالي كيفية تعديل الصفحة الرئيسية بتغيير الفيديو الذي يظهر في الوحدة النمطية لقارئ الفيديو.</span><span class="sxs-lookup"><span data-stu-id="9c4db-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="9c4db-135">تحت **المواقع**، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="9c4db-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="9c4db-136">في جزء التنقل على اليسار، حدد **الصفحات**.</span><span class="sxs-lookup"><span data-stu-id="9c4db-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="9c4db-137">ابحث عن الصفحة الرئيسية وحددها لفتحها في محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="9c4db-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="9c4db-138">في شريط الأوامر، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="9c4db-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="9c4db-139">في المخطط التفصيلي للصفحة، حدد الفتحة **الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="9c4db-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="9c4db-140">ضمن الفتحة **الرئيسية**، قم بتوسيع كافة الوحدات النمطية لحاوية السوائل.</span><span class="sxs-lookup"><span data-stu-id="9c4db-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="9c4db-141">ابحث عن الوحدة النمطية لقارئ الفيديو وحددها.</span><span class="sxs-lookup"><span data-stu-id="9c4db-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="9c4db-142">ثم في جزء الخصائص الموجود على اليمين، حدد خاصية **الفيديو**.</span><span class="sxs-lookup"><span data-stu-id="9c4db-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="9c4db-143">يظهر منتقي الأصول.</span><span class="sxs-lookup"><span data-stu-id="9c4db-143">The asset picker appears.</span></span>
1. <span data-ttu-id="9c4db-144">في منتقي الأصول، حدد أحد أصول الفيديو المتوفرة، أو حدد **‏‫تحميل أصل جديد** لتحميل أصل فيديو جديد.</span><span class="sxs-lookup"><span data-stu-id="9c4db-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="9c4db-145">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9c4db-145">Select **OK**.</span></span>
1. <span data-ttu-id="9c4db-146">حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="9c4db-146">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="9c4db-147">في حقل **التعليقات**، أدخل **تغيير الفيديو**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="9c4db-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="9c4db-148">حدد **معاينة** لمعاينة الصفحة المحدثة.</span><span class="sxs-lookup"><span data-stu-id="9c4db-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="9c4db-149">عند الانتهاء، قم بإغلاق علامة تبويب المعاينة للرجوع إلى أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="9c4db-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="9c4db-150">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="9c4db-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c4db-151">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="9c4db-151">Additional resources</span></span>

[<span data-ttu-id="9c4db-152">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="9c4db-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="9c4db-153">تحديد تخطيطات الصفحة</span><span class="sxs-lookup"><span data-stu-id="9c4db-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="9c4db-154">إدارة بيانات تعريف SEO</span><span class="sxs-lookup"><span data-stu-id="9c4db-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="9c4db-155">حفظ صفحة ومعاينتها ونشرها</span><span class="sxs-lookup"><span data-stu-id="9c4db-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="9c4db-156">إثراء صفحة منتج</span><span class="sxs-lookup"><span data-stu-id="9c4db-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="9c4db-157">إثراء الصفحة المنتقل إليها‬ لفئة</span><span class="sxs-lookup"><span data-stu-id="9c4db-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="9c4db-158">التحقق من إمكانية الوصول إلى محتوى الصفحة</span><span class="sxs-lookup"><span data-stu-id="9c4db-158">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="9c4db-159">إنشاء صفحات التجارة الإلكترونية الديناميكية استنادا إلى معلمات URL</span><span class="sxs-lookup"><span data-stu-id="9c4db-159">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)
