---
title: تعديل صفحة موقع موجودة
description: يصف هذا الموضوع كيفية تعديل صفحة موقع موجودة في Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b633965e45c16cb4e5991fab67783b867223f6ec
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803719"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="ea7c4-103">تعديل صفحة موقع موجودة</span><span class="sxs-lookup"><span data-stu-id="ea7c4-103">Modify an existing site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ea7c4-104">يصف هذا الموضوع كيفية تعديل صفحة موقع موجودة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ea7c4-105">عندما تكون مضطرًا لتعديل صفحة، تكون الخطوة الأولي هي فتحها في محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-105">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="ea7c4-106">انتقل إلى الموقع الذي يحتوي على الصفحة الخاصة بك، ثم في قائمة الصفحات، ابحث عن الصفحة التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-106">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="ea7c4-107">إذا لم تتمكن من العثور على الصفحة، يمكنك استخدام وظيفة البحث المتعمق لأداه التأليف.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-107">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="ea7c4-108">إما أن تكتب اسم الصفحة بالضبط، أو تكتب الأحرف الأولى منها ثم علامة (\*).</span><span class="sxs-lookup"><span data-stu-id="ea7c4-108">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="ea7c4-109">تظهر قائمة من الصفحات المصفاة.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-109">A filtered list of pages appears.</span></span> <span data-ttu-id="ea7c4-110">يمكنك استخدام هذه القائمة للعثور على الصفحة التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-110">You can use this list to find the page that you want.</span></span> <span data-ttu-id="ea7c4-111">بعد العثور علي الصفحة الصحيحة، حدد اسم الصفحة لفتح الصفحة في محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-111">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="ea7c4-112">إذا كانت الصفحة مرئية في مفتش الصفحة، يمكنك تحديد **تحرير** الصفحة وإخراجها قبل فتحها في محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-112">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="ea7c4-113">بهذه الطريقة، يمكنك سحب صفحات متعددة في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-113">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="ea7c4-114">بعد فتح الصفحة في محرر الصفحة، يجب التأكد منه قد تم سحبها.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-114">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="ea7c4-115">شريط الأوامر في أداه التأليف يكون ديناميكيًا، حساس للسياق، وحساس للحالة.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-115">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="ea7c4-116">لذلك، يعرض فقط الإجراءات التي يمكنك تنفيذها حاليًا في الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-116">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="ea7c4-117">على سبيل المثال، إذا لم يتم إخراج الصفحة لك، فلن يظهر الزران **حفظ** و **إنهاء التحرير** في شريط الأوامر.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-117">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="ea7c4-118">تظهر حالة الصفحة كذلك في الجانب الأيسر من النافذة.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-118">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="ea7c4-119">إذا لم يتم إخراج الصفحة بالفعل لك، فحدد **تحرير** في شريط الأوامر.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-119">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="ea7c4-120">يتغير شريط الأوامر ليعكس الحالة الجديدة للصفحة.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-120">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="ea7c4-121">كما تتلقي إعلامًا يوضح أن الصفحة تم سحبها لك.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-121">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="ea7c4-122">الخطوة التالية هي إجراء تغييرات فعلية.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-122">The next step is to make your actual changes.</span></span> <span data-ttu-id="ea7c4-123">غالبا، ستستخدم شجرة المخطط التفصيلي للصفحة الموجود على الجانب الأيمن للبحث عن الوحدة النمطية التي ترغب في تغييرها وتحديدها، ثم إجراء التغييرات في جزء الخصائص الموجود على الجانب الأيسر.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-123">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="ea7c4-124">ومع ذلك، قد يتضمن التغيير الخاص بك أحيانا إضافه نماذج أو أجزاء أو إزالتها.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-124">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="ea7c4-125">لإضافة جزء أو وحدة نمطية، استخدم شجره المخطط التفصيلي للصفحة للعثور علي الفتحة التي تريد إضافة الوحدة النمطية أو الجزء إليها، ثم حدد زر علامة الحذف (**...**) لهذه الفتحة.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-125">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="ea7c4-126">تظهر قائمة تتضمن أوامر لإضافة وحدة نمطية أو جزء.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-126">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="ea7c4-127">لإزالة وحدة نمطية أو جزء، ابحث عنه وحدده في شجرة المخطط التفصيلي للصفحة، وحدد زر علامة الحذف، ثم حدد الأمر لحذف الوحدة النمطية أو الجزء.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-127">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="ea7c4-128">يمكنك أيضًا عرض وتحرير الخصائص لأي وحدة نمطية مرئية في معاينة أداة إنشاء الصفحات المرئية بتحديدها مباشرة.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-128">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="ea7c4-129">بعد الانتهاء من إجراء التغييرات ومعاينة تأثيرها، يجب عليك إخراج الصفحة عن طريق تحديد **إنهاء التحرير** في شريط الأوامر.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-129">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="ea7c4-130">لنشر التغييرات مباشرة، حدد **نشر** من شريط الأوامر.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-130">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="ea7c4-131">يتم نشر آخر إصدار تم إيداعه من الصفحة التي قمت بتعديلها ويصبح متوفرا للمستخدمين الخارجيين الذين يعرضون الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-131">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="ea7c4-132">مثال: تغيير الفيديو على الصفحة الرئيسية</span><span class="sxs-lookup"><span data-stu-id="ea7c4-132">Example: Change the video on the home page</span></span>

<span data-ttu-id="ea7c4-133">يوضح المثال التالي كيفية تعديل الصفحة الرئيسية بتغيير الفيديو الذي يظهر في الوحدة النمطية لقارئ الفيديو.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-133">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="ea7c4-134">تحت **المواقع**، حدد **شركه الاتحاد للتصنيع** (أو اسم موقعك).</span><span class="sxs-lookup"><span data-stu-id="ea7c4-134">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="ea7c4-135">في جزء التنقل على اليسار، حدد **الصفحات**.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-135">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="ea7c4-136">ابحث عن الصفحة الرئيسية وحددها لفتحها في محرر الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-136">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="ea7c4-137">في شريط الأوامر، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-137">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="ea7c4-138">في المخطط التفصيلي للصفحة، حدد الفتحة **الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-138">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="ea7c4-139">ضمن الفتحة **الرئيسية**، قم بتوسيع كافة الوحدات النمطية لحاوية السوائل.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-139">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="ea7c4-140">ابحث عن الوحدة النمطية لقارئ الفيديو وحددها.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-140">Find and select the video player module.</span></span>
1. <span data-ttu-id="ea7c4-141">ثم في جزء الخصائص الموجود على اليمين، حدد خاصية **الفيديو**.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-141">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="ea7c4-142">يظهر منتقي الأصول.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-142">The asset picker appears.</span></span>
1. <span data-ttu-id="ea7c4-143">في منتقي الأصول، حدد أحد أصول الفيديو المتوفرة، أو حدد **‏‫تحميل أصل جديد** لتحميل أصل فيديو جديد.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-143">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="ea7c4-144">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-144">Select **OK**.</span></span>
1. <span data-ttu-id="ea7c4-145">حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-145">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="ea7c4-146">في حقل **التعليقات**، أدخل **تغيير الفيديو**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-146">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="ea7c4-147">حدد **معاينة** لمعاينة الصفحة المحدثة.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-147">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="ea7c4-148">عند الانتهاء، قم بإغلاق علامة تبويب المعاينة للرجوع إلى أداة التأليف.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-148">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="ea7c4-149">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea7c4-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ea7c4-150">Additional resources</span></span>

[<span data-ttu-id="ea7c4-151">إضافة صفحة موقع جديدة</span><span class="sxs-lookup"><span data-stu-id="ea7c4-151">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="ea7c4-152">تحديد تخطيطات الصفحة</span><span class="sxs-lookup"><span data-stu-id="ea7c4-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="ea7c4-153">إدارة بيانات تعريف SEO</span><span class="sxs-lookup"><span data-stu-id="ea7c4-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="ea7c4-154">حفظ صفحة ومعاينتها ونشرها</span><span class="sxs-lookup"><span data-stu-id="ea7c4-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="ea7c4-155">إثراء صفحة منتج</span><span class="sxs-lookup"><span data-stu-id="ea7c4-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="ea7c4-156">إثراء صفحة فئة منتقل إليها‬</span><span class="sxs-lookup"><span data-stu-id="ea7c4-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="ea7c4-157">التحقق من إمكانية الوصول إلى محتوى الصفحة</span><span class="sxs-lookup"><span data-stu-id="ea7c4-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="ea7c4-158">إنشاء صفحات التجارة الإلكترونية الديناميكية استنادا إلى معلمات URL</span><span class="sxs-lookup"><span data-stu-id="ea7c4-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
