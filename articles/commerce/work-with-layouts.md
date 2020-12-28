---
title: العمل مع التخطيطات سابقة الإعداد
description: يصف هذا الموضوع كيفية العمل مع التخطيطات المعينة مسبقًا في Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f31dfa1fdbb3732610748abe4a9de851033f2b89
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409910"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="fea3e-103">العمل مع التخطيطات سابقة الإعداد</span><span class="sxs-lookup"><span data-stu-id="fea3e-103">Work with preset layouts</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fea3e-104">يصف هذا الموضوع كيفية العمل مع التخطيطات المعينة مسبقًا في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fea3e-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fea3e-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="fea3e-105">Overview</span></span>

<span data-ttu-id="fea3e-106">قبل إكمال الإجراءات الواردة في هذا الموضوع، تأكد من قراءة [التخطيطات المخصصة والمعينة مسبقًا](templates-layouts-overview.md#preset-and-custom-layouts).</span><span class="sxs-lookup"><span data-stu-id="fea3e-106">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="fea3e-107">للحصول على نظرة عامة، راجع [نظرة عامة حول القوالب والتخطيطات](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fea3e-107">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="fea3e-108">إنشاء تخطيط معين مسبقًا جديد</span><span class="sxs-lookup"><span data-stu-id="fea3e-108">Create a new preset layout</span></span>

<span data-ttu-id="fea3e-109">هناك طريقتان لإنشاء مخطط معين مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="fea3e-109">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="fea3e-110">يمكنك حفظ تخطيط مخصص موجود كتخطيط معين مسبقًا جديد، أو يمكنك إنشاء تخطيط معين مسبقًا من البداية.</span><span class="sxs-lookup"><span data-stu-id="fea3e-110">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="fea3e-111">إنشاء تخطيط معين مسبقًا من تخطيط مخصص موجود</span><span class="sxs-lookup"><span data-stu-id="fea3e-111">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="fea3e-112">لإنشاء تخطيط معين مسبقًا من تخطيط مخصص موجود، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="fea3e-112">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="fea3e-113">افتح صفحة موجودة لا تستخدم تخطيطًا معين مسبقًا حاليًا ويحتوي على بنية وحدة نمطية ترغب في إعادة استخدامها لصفحات أخرى على الموقع الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="fea3e-113">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="fea3e-114">حدد **تحرير** لإخراج الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fea3e-114">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="fea3e-115">حدد **حفظ كتخطيط جديد**.</span><span class="sxs-lookup"><span data-stu-id="fea3e-115">Select **Save as new layout**.</span></span> <span data-ttu-id="fea3e-116">يظهر مربع الحوار **حفظ كتخطيط جديد**.</span><span class="sxs-lookup"><span data-stu-id="fea3e-116">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="fea3e-117">أدخل اسمًا ووصفًا للتخطيط المعين مسبقًا الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="fea3e-117">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="fea3e-118">سيتم عرض القيم التي تقوم بإدخالها للمؤلفين الآخرين عند قيامهم بإنشاء صفحات جديدة من التخطيط أو التبديل إليه.</span><span class="sxs-lookup"><span data-stu-id="fea3e-118">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="fea3e-119">وبالتالي، أدخل القيم التي ستكون مفيدة لمؤلفي الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fea3e-119">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="fea3e-120">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="fea3e-120">Select **OK**.</span></span>

<span data-ttu-id="fea3e-121">سيتوفر الآن التخطيط المعين مسبقًا عند إنشاء صفحات جديدة أو تحديد تخطيط مختلف لصفحة في نفس التسلسل الهرمي للقالب.</span><span class="sxs-lookup"><span data-stu-id="fea3e-121">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="fea3e-122">لمعرفة ما إذا كانت صفحة معينة مرتبطة حاليًا بتخطيط معين مسبقًا أم لا، حدد الصفحة في طريقة عرض قائمة الصفحات وافحص بيانات تعريف التخطيط في جزء الخصائص الموجود على الجانب الأيمن.</span><span class="sxs-lookup"><span data-stu-id="fea3e-122">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="fea3e-123">إنشاء تخطيط معين مسبقًا جديد</span><span class="sxs-lookup"><span data-stu-id="fea3e-123">Create a new preset layout</span></span>

<span data-ttu-id="fea3e-124">لإنشاء تخطيط معين مسبقًا من البداية، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="fea3e-124">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="fea3e-125">في جزء التنقل على اليسار، حدد **التخطيطات**.</span><span class="sxs-lookup"><span data-stu-id="fea3e-125">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="fea3e-126">حدد **تخطيط جديد**.</span><span class="sxs-lookup"><span data-stu-id="fea3e-126">Select **New Layout**.</span></span> <span data-ttu-id="fea3e-127">يظهر مربع الحوار **تخطيط جديد**.</span><span class="sxs-lookup"><span data-stu-id="fea3e-127">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="fea3e-128">حدد القالب المراد استخدامه لتخطيط معين مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="fea3e-128">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="fea3e-129">أدخل اسمًا ووصفًا للتخطيط المعين مسبقًا الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="fea3e-129">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="fea3e-130">سيتم عرض القيم التي تقوم بإدخالها للمؤلفين الآخرين عند قيامهم بإنشاء صفحات جديدة من التخطيط أو التبديل إليه.</span><span class="sxs-lookup"><span data-stu-id="fea3e-130">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="fea3e-131">وبالتالي، أدخل القيم التي ستكون مفيدة لمؤلفي الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fea3e-131">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="fea3e-132">حدد **موافق** لإنشاء التخطيط المعين مسبقًا وفتح محرر التخطيط.</span><span class="sxs-lookup"><span data-stu-id="fea3e-132">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="fea3e-133">في محرر التخطيط، قم بإضافة الوحدات النمطية وتكوينها باستخدام شجرة المخطط التفصيلي على اليسار وجزء الخصائص على اليمين.</span><span class="sxs-lookup"><span data-stu-id="fea3e-133">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="fea3e-134">(تشبه العملية عملية إضافة الوحدات النمطية وتكوينها لقالب في محرر القالب). ويصبح ترتيب الوحدات النمطية والإعدادات الافتراضية المؤمنة هو تكوين الوحدة النمطية المركزية لأية صفحات تستخدم هذا التخطيط المعين مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="fea3e-134">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="fea3e-135">تعديل تخطيط معين مسبقًا</span><span class="sxs-lookup"><span data-stu-id="fea3e-135">Modify a preset layout</span></span>

<span data-ttu-id="fea3e-136">لتعديل تخطيط معين مسبقًا، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="fea3e-136">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="fea3e-137">في جزء التنقل على اليسار، حدد **التخطيطات**.</span><span class="sxs-lookup"><span data-stu-id="fea3e-137">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="fea3e-138">في محرر التخطيط، في شجرة المخطط التفصيلي الموجود على اليسار، حدد الوحدة النمطية المراد تعديلها.</span><span class="sxs-lookup"><span data-stu-id="fea3e-138">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="fea3e-139">ثم اتبع أيًا من الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="fea3e-139">Then follow any of these steps:</span></span>

    - <span data-ttu-id="fea3e-140">لتحريك وحدة نمطية لأعلى أو لأسفل داخل الأصل، حدد زر علامة الحذف (**...**) للوحدة النمطية، ثم حدد **تحريك لأعلى** أو **تحريك لأسفل**.</span><span class="sxs-lookup"><span data-stu-id="fea3e-140">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="fea3e-141">لتغيير الإعدادات الافتراضية للوحدة النمطية، استخدم جزء الخصائص لإدخال القيم الافتراضية وقم بتأمينها اختياريًا لكافة الصفحات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="fea3e-141">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="fea3e-142">لإضافة وحدات نمطية أو أجزاء جديدة إلى الوحدات النمطية للحاوية، حدد زر علامة الحذف، ثم حدد **إضافة وحدة** أو **إضافة جزء**.</span><span class="sxs-lookup"><span data-stu-id="fea3e-142">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="fea3e-143">لإزالة وحدة نمطية من المخطط، حدد زر علامة الحذف، ثم حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="fea3e-143">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="fea3e-144">تغيير سمة تخطيط معين مسبقًا</span><span class="sxs-lookup"><span data-stu-id="fea3e-144">Change a preset layout theme</span></span>

<span data-ttu-id="fea3e-145">تُعد الممارسة النموذجية تعيين سمة افتراضية لكافة الصفحات التي تستخدم تخطيط معين مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="fea3e-145">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="fea3e-146">لتعيين أو تغيير السمة لكافة الصفحات الفرعية التي تستخدم التخطيط المعين مسبقًا الخاص بك، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="fea3e-146">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="fea3e-147">في محرر التخطيط، في شجرة المخطط التفصيلي الموجود على اليسار، حدد الوحدة النمطية لحاوية صفحة.</span><span class="sxs-lookup"><span data-stu-id="fea3e-147">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="fea3e-148">(عادة ما تكون هذه الوحدة النمطية هي العقدة الثانية وتسمى **الصفحة الافتراضية**).</span><span class="sxs-lookup"><span data-stu-id="fea3e-148">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="fea3e-149">في جزء الخصائص على اليمين، في حقل **السمة**، حدد سمة.</span><span class="sxs-lookup"><span data-stu-id="fea3e-149">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="fea3e-150">حفظ تخطيط معين مسبقًا وإيداعه ومعاينته ونشره</span><span class="sxs-lookup"><span data-stu-id="fea3e-150">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="fea3e-151">للحفظ والإيداع في تخطيط معين مسبقًا، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="fea3e-151">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="fea3e-152">حدد **حفظ** في أعلى محرر التخطيط.</span><span class="sxs-lookup"><span data-stu-id="fea3e-152">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="fea3e-153">لا تؤثر التغييرات المحفوظة على الصفحات اللاحقة حتى يتم إيداعها.</span><span class="sxs-lookup"><span data-stu-id="fea3e-153">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="fea3e-154">حدد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="fea3e-154">Select **Finish editing**.</span></span> <span data-ttu-id="fea3e-155">تكون التغييرات الخاصة بك قابلة للاكتشاف الآن لعمليات سير العمل اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="fea3e-155">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="fea3e-156">لمعاينة التغييرات الخاصة بك، فإما أن تقوم بفتح صفحة موجودة تستخدم التخطيط المعين مسبقًا أو إنشاء صفحة جديدة من التخطيط.</span><span class="sxs-lookup"><span data-stu-id="fea3e-156">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="fea3e-157">بعد الانتهاء من معاينة التغييرات التي تمت على التخطيط المعين مسبقًا، اتبع إحدى هذه الخطوات لنشر التخطيط على موقعك المباشر:</span><span class="sxs-lookup"><span data-stu-id="fea3e-157">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="fea3e-158">انتقل إلى **التخطيطات**، حدد التخطيط، ثم حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="fea3e-158">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="fea3e-159">حدد اسم المخطط لفتح محرر التخطيط، ثم حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="fea3e-159">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="fea3e-160">انشر صفحة تشير إلى التخطيط غير المنشور.</span><span class="sxs-lookup"><span data-stu-id="fea3e-160">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="fea3e-161">سيتم نشر التخطيط تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="fea3e-161">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="fea3e-162">يمكن الإشارة إلى التخطيطات المعينة مسبقًا بواسطة عدة صفحات.</span><span class="sxs-lookup"><span data-stu-id="fea3e-162">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="fea3e-163">عند نشر تخطيط معين مسبقًا، فانتبه إلى أنك قد تؤثر على تخطيط الصفحات المتعددة.</span><span class="sxs-lookup"><span data-stu-id="fea3e-163">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fea3e-164">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="fea3e-164">Additional resources</span></span>

[<span data-ttu-id="fea3e-165">نظرة عامة على القوالب والتخطيطات</span><span class="sxs-lookup"><span data-stu-id="fea3e-165">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="fea3e-166">العمل مع القوالب</span><span class="sxs-lookup"><span data-stu-id="fea3e-166">Work with templates</span></span>](work-with-templates.md)
