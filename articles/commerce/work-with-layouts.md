---
title: العمل مع التخطيطات سابقة الإعداد
description: يصف هذا الموضوع كيفية العمل مع التخطيطات المعينة مسبقًا في Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ce54be1032777ffcaac474773cdeeef3b9028110
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793911"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="1f62e-103">العمل مع التخطيطات سابقة الإعداد</span><span class="sxs-lookup"><span data-stu-id="1f62e-103">Work with preset layouts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1f62e-104">يصف هذا الموضوع كيفية العمل مع التخطيطات المعينة مسبقًا في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1f62e-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1f62e-105">قبل إكمال الإجراءات الواردة في هذا الموضوع، تأكد من قراءة [التخطيطات المخصصة والمعينة مسبقًا](templates-layouts-overview.md#preset-and-custom-layouts).</span><span class="sxs-lookup"><span data-stu-id="1f62e-105">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="1f62e-106">للحصول على نظرة عامة، راجع [نظرة عامة حول القوالب والتخطيطات](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1f62e-106">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="1f62e-107">إنشاء تخطيط معين مسبقًا جديد</span><span class="sxs-lookup"><span data-stu-id="1f62e-107">Create a new preset layout</span></span>

<span data-ttu-id="1f62e-108">هناك طريقتان لإنشاء مخطط معين مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="1f62e-108">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="1f62e-109">يمكنك حفظ تخطيط مخصص موجود كتخطيط معين مسبقًا جديد، أو يمكنك إنشاء تخطيط معين مسبقًا من البداية.</span><span class="sxs-lookup"><span data-stu-id="1f62e-109">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="1f62e-110">إنشاء تخطيط معين مسبقًا من تخطيط مخصص موجود</span><span class="sxs-lookup"><span data-stu-id="1f62e-110">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="1f62e-111">لإنشاء تخطيط معين مسبقًا من تخطيط مخصص موجود، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="1f62e-111">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="1f62e-112">افتح صفحة موجودة لا تستخدم تخطيطًا معين مسبقًا حاليًا ويحتوي على بنية وحدة نمطية ترغب في إعادة استخدامها لصفحات أخرى على الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="1f62e-112">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="1f62e-113">حدد **تحرير** لإخراج الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1f62e-113">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="1f62e-114">حدد **حفظ كتخطيط جديد**.</span><span class="sxs-lookup"><span data-stu-id="1f62e-114">Select **Save as new layout**.</span></span> <span data-ttu-id="1f62e-115">يظهر مربع الحوار **حفظ كتخطيط جديد**.</span><span class="sxs-lookup"><span data-stu-id="1f62e-115">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="1f62e-116">أدخل اسمًا ووصفًا للتخطيط المعين مسبقًا الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="1f62e-116">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="1f62e-117">سيتم عرض القيم التي تقوم بإدخالها للمؤلفين الآخرين عند قيامهم بإنشاء صفحات جديدة من التخطيط أو التبديل إليه.</span><span class="sxs-lookup"><span data-stu-id="1f62e-117">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="1f62e-118">وبالتالي، أدخل القيم التي ستكون مفيدة لمؤلفي الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1f62e-118">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="1f62e-119">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="1f62e-119">Select **OK**.</span></span>

<span data-ttu-id="1f62e-120">سيتوفر الآن التخطيط المعين مسبقًا عند إنشاء صفحات جديدة أو تحديد تخطيط مختلف لصفحة في نفس التسلسل الهرمي للقالب.</span><span class="sxs-lookup"><span data-stu-id="1f62e-120">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="1f62e-121">لمعرفة ما إذا كانت صفحة معينة مرتبطة حاليًا بتخطيط معين مسبقًا أم لا، حدد الصفحة في طريقة عرض قائمة الصفحات وافحص بيانات تعريف التخطيط في جزء الخصائص الموجود على الجانب الأيمن.</span><span class="sxs-lookup"><span data-stu-id="1f62e-121">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="1f62e-122">إنشاء تخطيط معين مسبقًا جديد</span><span class="sxs-lookup"><span data-stu-id="1f62e-122">Create a new preset layout</span></span>

<span data-ttu-id="1f62e-123">لإنشاء تخطيط معين مسبقًا من البداية، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="1f62e-123">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="1f62e-124">في جزء التنقل على اليسار، حدد **التخطيطات**.</span><span class="sxs-lookup"><span data-stu-id="1f62e-124">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="1f62e-125">حدد **تخطيط جديد**.</span><span class="sxs-lookup"><span data-stu-id="1f62e-125">Select **New Layout**.</span></span> <span data-ttu-id="1f62e-126">يظهر مربع الحوار **تخطيط جديد**.</span><span class="sxs-lookup"><span data-stu-id="1f62e-126">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="1f62e-127">حدد القالب المراد استخدامه لتخطيط معين مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="1f62e-127">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="1f62e-128">أدخل اسمًا ووصفًا للتخطيط المعين مسبقًا الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="1f62e-128">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="1f62e-129">سيتم عرض القيم التي تقوم بإدخالها للمؤلفين الآخرين عند قيامهم بإنشاء صفحات جديدة من التخطيط أو التبديل إليه.</span><span class="sxs-lookup"><span data-stu-id="1f62e-129">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="1f62e-130">وبالتالي، أدخل القيم التي ستكون مفيدة لمؤلفي الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1f62e-130">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="1f62e-131">حدد **موافق** لإنشاء التخطيط المعين مسبقًا وفتح محرر التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1f62e-131">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="1f62e-132">في محرر التخطيط، قم بإضافة الوحدات النمطية وتكوينها باستخدام شجرة المخطط التفصيلي على اليسار وجزء الخصائص على اليمين.</span><span class="sxs-lookup"><span data-stu-id="1f62e-132">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="1f62e-133">(تشبه العملية عملية إضافة الوحدات النمطية وتكوينها لقالب في محرر القالب). ويصبح ترتيب الوحدات النمطية والإعدادات الافتراضية المؤمنة هو تكوين الوحدة النمطية المركزية لأية صفحات تستخدم هذا التخطيط المعين مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="1f62e-133">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="1f62e-134">تعديل تخطيط معين مسبقًا</span><span class="sxs-lookup"><span data-stu-id="1f62e-134">Modify a preset layout</span></span>

<span data-ttu-id="1f62e-135">لتعديل تخطيط معين مسبقًا، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="1f62e-135">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="1f62e-136">في جزء التنقل على اليسار، حدد **التخطيطات**.</span><span class="sxs-lookup"><span data-stu-id="1f62e-136">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="1f62e-137">في محرر التخطيط، في شجرة المخطط التفصيلي الموجود على اليسار، حدد الوحدة النمطية المراد تعديلها.</span><span class="sxs-lookup"><span data-stu-id="1f62e-137">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="1f62e-138">ثم اتبع أيًا من الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="1f62e-138">Then follow any of these steps:</span></span>

    - <span data-ttu-id="1f62e-139">لتحريك وحدة نمطية لأعلى أو لأسفل داخل الأصل، حدد زر علامة الحذف (**...**) للوحدة النمطية، ثم حدد **تحريك لأعلى** أو **تحريك لأسفل**.</span><span class="sxs-lookup"><span data-stu-id="1f62e-139">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="1f62e-140">لتغيير الإعدادات الافتراضية للوحدة النمطية، استخدم جزء الخصائص لإدخال القيم الافتراضية وقم بتأمينها اختياريًا لكافة الصفحات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="1f62e-140">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="1f62e-141">لإضافة وحدات نمطية أو أجزاء جديدة إلى الوحدات النمطية للحاوية، حدد زر علامة الحذف، ثم حدد **إضافة وحدة** أو **إضافة جزء**.</span><span class="sxs-lookup"><span data-stu-id="1f62e-141">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="1f62e-142">لإزالة وحدة نمطية من المخطط، حدد زر علامة الحذف، ثم حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="1f62e-142">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="1f62e-143">تغيير سمة تخطيط معين مسبقًا</span><span class="sxs-lookup"><span data-stu-id="1f62e-143">Change a preset layout theme</span></span>

<span data-ttu-id="1f62e-144">تُعد الممارسة النموذجية تعيين سمة افتراضية لكافة الصفحات التي تستخدم تخطيط معين مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="1f62e-144">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="1f62e-145">لتعيين أو تغيير السمة لكافة الصفحات الفرعية التي تستخدم التخطيط المعين مسبقًا الخاص بك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="1f62e-145">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="1f62e-146">في محرر التخطيط، في شجرة المخطط التفصيلي الموجود على اليسار، حدد الوحدة النمطية لحاوية صفحة.</span><span class="sxs-lookup"><span data-stu-id="1f62e-146">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="1f62e-147">(عادة ما تكون هذه الوحدة النمطية هي العقدة الثانية وتسمى **الصفحة الافتراضية**).</span><span class="sxs-lookup"><span data-stu-id="1f62e-147">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="1f62e-148">في جزء الخصائص على اليمين، في حقل **السمة**، حدد سمة.</span><span class="sxs-lookup"><span data-stu-id="1f62e-148">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="1f62e-149">حفظ تخطيط معين مسبقًا وإيداعه ومعاينته ونشره</span><span class="sxs-lookup"><span data-stu-id="1f62e-149">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="1f62e-150">للحفظ والإيداع في تخطيط معين مسبقًا، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="1f62e-150">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="1f62e-151">حدد **حفظ** في أعلى محرر التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1f62e-151">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="1f62e-152">لا تؤثر التغييرات المحفوظة على الصفحات اللاحقة حتى يتم إيداعها.</span><span class="sxs-lookup"><span data-stu-id="1f62e-152">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="1f62e-153">حدد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="1f62e-153">Select **Finish editing**.</span></span> <span data-ttu-id="1f62e-154">تكون التغييرات الخاصة بك قابلة للاكتشاف الآن لعمليات سير العمل اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="1f62e-154">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="1f62e-155">لمعاينة التغييرات الخاصة بك، فإما أن تقوم بفتح صفحة موجودة تستخدم التخطيط المعين مسبقًا أو إنشاء صفحة جديدة من التخطيط.</span><span class="sxs-lookup"><span data-stu-id="1f62e-155">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="1f62e-156">بعد الانتهاء من معاينة التغييرات التي تمت على التخطيط المعين مسبقًا، اتبع إحدى هذه الخطوات لنشر التخطيط على موقعك المباشر:</span><span class="sxs-lookup"><span data-stu-id="1f62e-156">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="1f62e-157">انتقل إلى **التخطيطات**، حدد التخطيط، ثم حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="1f62e-157">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="1f62e-158">حدد اسم المخطط لفتح محرر التخطيط، ثم حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="1f62e-158">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="1f62e-159">انشر صفحة تشير إلى التخطيط غير المنشور.</span><span class="sxs-lookup"><span data-stu-id="1f62e-159">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="1f62e-160">سيتم نشر التخطيط تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="1f62e-160">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="1f62e-161">يمكن الإشارة إلى التخطيطات المعينة مسبقًا بواسطة عدة صفحات.</span><span class="sxs-lookup"><span data-stu-id="1f62e-161">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="1f62e-162">عند نشر تخطيط معين مسبقًا، فانتبه إلى أنك قد تؤثر على تخطيط الصفحات المتعددة.</span><span class="sxs-lookup"><span data-stu-id="1f62e-162">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1f62e-163">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="1f62e-163">Additional resources</span></span>

[<span data-ttu-id="1f62e-164">نظرة عامة على القوالب والتخطيطات</span><span class="sxs-lookup"><span data-stu-id="1f62e-164">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="1f62e-165">العمل مع القوالب</span><span class="sxs-lookup"><span data-stu-id="1f62e-165">Work with templates</span></span>](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
