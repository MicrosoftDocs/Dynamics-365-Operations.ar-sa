---
title: إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام
description: يصف هذا الموضوع كيفيه إضافة التعليمات البرمجية لبرنامج نصي من جانب العميل إلى صفحات موقعك لدعم مجموعة تتبع الاستخدام من جانب العميل.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 81c36685c1eccceb2f1854fe7c866186120c08a3
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154076"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="7a99f-103">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="7a99f-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7a99f-104">يصف هذا الموضوع كيفيه إضافة التعليمات البرمجية لبرنامج نصي من جانب العميل إلى صفحات موقعك لدعم مجموعة تتبع الاستخدام من جانب العميل.</span><span class="sxs-lookup"><span data-stu-id="7a99f-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="7a99f-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="7a99f-105">Overview</span></span>

<span data-ttu-id="7a99f-106">تُعد تحليلات الويب أداة أساسية عندما ترغب في فهم كيفية تفاعل عملائك مع موقعك واتخاذ قرارات من شأنها أن تساعد في تحسين التجربة لتحقيق أقصى قدر من التحويل.</span><span class="sxs-lookup"><span data-stu-id="7a99f-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="7a99f-107">تتوفر العديد من حزم تحليلات الويب لمساعدتك في تحقيق هذه الأهداف، مثل Google Analytics وClicky وMoz Analytics وKISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="7a99f-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="7a99f-108">تتطلب معظم حزم تحليلات الويب أن تضيف التعليمات البرمجية لبرنامج نصي في عنصر **\<العنوان\>** من HTML لجميع صفحات موقعك.</span><span class="sxs-lookup"><span data-stu-id="7a99f-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="7a99f-109">تنطبق الإرشادات الواردة في هذا الموضوع أيضًا على الوظائف المخصصة الأخرى من جانب العميل التي لا يوفرها Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7a99f-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a><span data-ttu-id="7a99f-110">إنشاء جزء صفحة قابل لإعادة الاستخدام للتعليمات البرمجية لبرنامج نصي</span><span class="sxs-lookup"><span data-stu-id="7a99f-110">Create a reusable page fragment for your script code</span></span>

<span data-ttu-id="7a99f-111">يتيح جزء الصفحة إمكانية إعادة استخدام التعليمات البرمجية المضمنة أو الخارجية في كافة صفحات موقعك، بغض النظر عن القالب الذي تستخدمه.</span><span class="sxs-lookup"><span data-stu-id="7a99f-111">A page fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a><span data-ttu-id="7a99f-112">إنشاء جزء صفحة قابل لإعادة الاستخدام للتعليمات البرمجية لبرنامج نصي مضمن</span><span class="sxs-lookup"><span data-stu-id="7a99f-112">Create a reusable page fragment for your inline script code</span></span>

<span data-ttu-id="7a99f-113">لإنشاء جزء الصفحة القابل لإعادة الاستخدام للتعليمات البرمجية للنص المضمن في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="7a99f-113">To create a reusable page fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7a99f-114">انتقل إلى **أجزاء الصفحات**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-114">Go to **Page Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="7a99f-115">في مربع الحوار **جزء الصفحة**، حدد **البرنامج النصي المضمن**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-115">In the **New Page Fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="7a99f-116">ضمن **اسم جزء الصفحة**، أدخل اسمًا لهذا الجزء ، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-116">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="7a99f-117">ضمن جزء الصفحة الذي قمت بإنشائه، حدد وحدة **البرنامج النصي الافتراضي المضمن**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-117">Under the page fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="7a99f-118">في جزء الخصائص الموجود على الجانب الأيمن، ضمن **البرنامج النصي المضمن**، أدخل البرنامج النصي من جانب العميل.</span><span class="sxs-lookup"><span data-stu-id="7a99f-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="7a99f-119">قم بعد ذلك بتكوين الخيارات الأخرى كما تتطلب.</span><span class="sxs-lookup"><span data-stu-id="7a99f-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="7a99f-120">حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7a99f-121">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a><span data-ttu-id="7a99f-122">إنشاء جزء صفحة قابل لإعادة الاستخدام للتعليمات البرمجية لبرنامج نصي خارجي</span><span class="sxs-lookup"><span data-stu-id="7a99f-122">Create a reusable page fragment for your external script code</span></span>

<span data-ttu-id="7a99f-123">لإنشاء جزء الصفحة القابل لإعادة الاستخدام للتعليمات البرمجية للبرنامج النصي الخارجي في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="7a99f-123">To create a reusable page fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7a99f-124">انتقل إلى **أجزاء الصفحات**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-124">Go to **Page Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="7a99f-125">في مربع الحوار **جزء الصفحة الجديد**، حدد **البرنامج النصي الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-125">In the **New Page Fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="7a99f-126">ضمن **اسم جزء الصفحة**، أدخل اسمًا لهذا الجزء ، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-126">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="7a99f-127">ضمن جزء الصفحة الذي قمت بإنشائه، حدد وحدة **البرنامج النصي الافتراضي الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-127">Under the page fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="7a99f-128">في جزء الخصائص الموجود على الجانب الأيمن، ضمن **مصدر البرنامج النصي**، أضف عنوان URL خارجيًا أو ذي صلة لمصدر البرنامج النصي الخارجي.</span><span class="sxs-lookup"><span data-stu-id="7a99f-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="7a99f-129">قم بعد ذلك بتكوين الخيارات الأخرى كما تتطلب.</span><span class="sxs-lookup"><span data-stu-id="7a99f-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="7a99f-130">حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7a99f-131">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-131">Select **Publish**.</span></span>

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="7a99f-132">أضف جزء الصفحة الذي يحتوي على التعليمات البرمجية للبرنامج النصي إلى قالب</span><span class="sxs-lookup"><span data-stu-id="7a99f-132">Add a page fragment that includes script code to a template</span></span>

<span data-ttu-id="7a99f-133">لإضافة جزء صفحة يتضمن التعليمات البرمجية للبرنامج النصي إلى قالب في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="7a99f-133">To add a page fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7a99f-134">انتقل إلى **القوالب**، وافتح القالب الخاص بالصفحات التي تريد إضافة التعليمات البرمجية لبرنامج نصي اليها.</span><span class="sxs-lookup"><span data-stu-id="7a99f-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="7a99f-135">في الجزء الأيسر، قم بتوسيع التدرج الهرمي للقالب لإظهار فتحة **عنوان HTML** .</span><span class="sxs-lookup"><span data-stu-id="7a99f-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="7a99f-136">في فتحة **عنوان HTML‬‏‫**، وحدد علامة الحذف (**...**)، ثم حدد **إضافة جزء الصفحة**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="7a99f-137">حدد الجزء الذي قمت بإنشاءه للتعليمات البرمجية لبرنامجك النصي.</span><span class="sxs-lookup"><span data-stu-id="7a99f-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="7a99f-138">حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7a99f-139">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="7a99f-140">إضافة برنامج نصي خارجي أو برنامج نصي مضمن مباشرةً إلى قالب</span><span class="sxs-lookup"><span data-stu-id="7a99f-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="7a99f-141">إذا كنت ترغب في إدراج برنامج نصي مضمن أو خارجي مباشرةً في مجموعة من الصفحات التي يتم التحكم فيها بواسطة قالب واحد، فلن تحتاج إلى إنشاء جزء صفحة أولاً.</span><span class="sxs-lookup"><span data-stu-id="7a99f-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a page fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="7a99f-142">إضافة برنامج نصي مضمن مباشرةً إلى قالب</span><span class="sxs-lookup"><span data-stu-id="7a99f-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="7a99f-143">لإضافة برنامج نصي مضمن مباشرةً إلى قالب في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="7a99f-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7a99f-144">انتقل إلى **القوالب**، وافتح القالب الخاص بالصفحات التي تريد إضافة التعليمات البرمجية لبرنامج نصي اليها.</span><span class="sxs-lookup"><span data-stu-id="7a99f-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="7a99f-145">في الجزء الأيسر، قم بتوسيع التدرج الهرمي للقالب لإظهار فتحة **عنوان HTML** .</span><span class="sxs-lookup"><span data-stu-id="7a99f-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="7a99f-146">في فتحة **عنوان HTML‬‏‫**، وحدد علامة الحذف (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7a99f-147">في مربع الحوار **إضافة وحدة**، حدد **البرنامج النصي المضمن**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="7a99f-148">في جزء الخصائص الموجود على الجانب الأيمن، ضمن **البرنامج النصي المضمن**، أدخل البرنامج النصي من جانب العميل.</span><span class="sxs-lookup"><span data-stu-id="7a99f-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="7a99f-149">قم بعد ذلك بتكوين الخيارات الأخرى كما تتطلب.</span><span class="sxs-lookup"><span data-stu-id="7a99f-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="7a99f-150">حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7a99f-151">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="7a99f-152">إضافة برنامج نصي خارجي مباشرةً إلى قالب</span><span class="sxs-lookup"><span data-stu-id="7a99f-152">Add an external script directly to a template</span></span>

<span data-ttu-id="7a99f-153">لإضافة برنامج نصي خارجي مباشرةً إلى قالب في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="7a99f-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7a99f-154">انتقل إلى **القوالب**، وافتح القالب الخاص بالصفحات التي تريد إضافة التعليمات البرمجية لبرنامج نصي اليها.</span><span class="sxs-lookup"><span data-stu-id="7a99f-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="7a99f-155">في الجزء الأيسر، قم بتوسيع التدرج الهرمي للقالب لإظهار فتحة **عنوان HTML** .</span><span class="sxs-lookup"><span data-stu-id="7a99f-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="7a99f-156">في فتحة **عنوان HTML‬‏‫**، وحدد علامة الحذف (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7a99f-157">في مربع الحوار **إضافة وحدة**، حدد **البرنامج النصي الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="7a99f-158">في جزء الخصائص الموجود على الجانب الأيمن، ضمن **مصدر البرنامج النصي**، أضف عنوان URL خارجيًا أو ذي صلة لمصدر البرنامج النصي الخارجي.</span><span class="sxs-lookup"><span data-stu-id="7a99f-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="7a99f-159">قم بعد ذلك بتكوين الخيارات الأخرى كما تتطلب.</span><span class="sxs-lookup"><span data-stu-id="7a99f-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="7a99f-160">حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7a99f-161">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="7a99f-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7a99f-162">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="7a99f-162">Additional resources</span></span>

[<span data-ttu-id="7a99f-163">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="7a99f-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="7a99f-164">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="7a99f-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="7a99f-165">العمل CSS مع ملفات التجاوز</span><span class="sxs-lookup"><span data-stu-id="7a99f-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="7a99f-166">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="7a99f-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="7a99f-167">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="7a99f-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="7a99f-168">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="7a99f-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="7a99f-169">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="7a99f-169">Add languages to your site</span></span>](add-languages-to-site.md)
