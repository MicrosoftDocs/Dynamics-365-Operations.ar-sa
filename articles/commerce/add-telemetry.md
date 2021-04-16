---
title: إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام
description: يصف هذا الموضوع كيفيه إضافة التعليمات البرمجية لبرنامج نصي من جانب العميل إلى صفحات موقعك لدعم مجموعة تتبع الاستخدام من جانب العميل.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb1773ab10b23a586eb6a8286f145181818585b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797421"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="c7850-103">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="c7850-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c7850-104">يصف هذا الموضوع كيفيه إضافة التعليمات البرمجية لبرنامج نصي من جانب العميل إلى صفحات موقعك لدعم مجموعة تتبع الاستخدام من جانب العميل.</span><span class="sxs-lookup"><span data-stu-id="c7850-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

<span data-ttu-id="c7850-105">تُعد تحليلات الويب أداة أساسية عندما ترغب في فهم كيفية تفاعل عملائك مع موقعك واتخاذ قرارات من شأنها أن تساعد في تحسين التجربة لتحقيق أقصى قدر من التحويل.</span><span class="sxs-lookup"><span data-stu-id="c7850-105">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="c7850-106">تتوفر العديد من حزم تحليلات الويب لمساعدتك في تحقيق هذه الأهداف، مثل Google Analytics وClicky وMoz Analytics وKISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="c7850-106">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="c7850-107">تتطلب معظم حزم تحليلات الويب أن تضيف التعليمات البرمجية لبرنامج نصي في عنصر **\<head\>** من HTML لجميع صفحات موقعك.</span><span class="sxs-lookup"><span data-stu-id="c7850-107">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="c7850-108">تنطبق الإرشادات الواردة في هذا الموضوع أيضًا على الوظائف المخصصة الأخرى من جانب العميل التي لا يوفرها Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c7850-108">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="c7850-109">إنشاء جزء قابل لإعادة الاستخدام للتعليمات البرمجية لبرنامج نصي</span><span class="sxs-lookup"><span data-stu-id="c7850-109">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="c7850-110">يتيح لك الجزء إعادة استخدام التعليمات البرمجية المضمنة أو الخارجية في كافة صفحات موقعك، بغض النظر عن القالب الذي تستخدمه.</span><span class="sxs-lookup"><span data-stu-id="c7850-110">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="c7850-111">إنشاء جزء قابل لإعادة الاستخدام للتعليمات البرمجية لبرنامج نصي مضمن</span><span class="sxs-lookup"><span data-stu-id="c7850-111">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="c7850-112">لإنشاء جزء قابل لإعادة الاستخدام للتعليمات البرمجية للنص المضمن في منشئ المواقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c7850-112">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c7850-113">انتقل إلى **الأجزاء**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c7850-113">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="c7850-114">في مربع الحوار **جزء جديد**، حدد **البرنامج النصي المضمن**.</span><span class="sxs-lookup"><span data-stu-id="c7850-114">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="c7850-115">ضمن **اسم الجزء**، أدخل اسمًا لهذا الجزء، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c7850-115">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="c7850-116">ضمن الجزء الذي قمت بإنشائه، حدد الوحدة **البرنامج النصي الافتراضي المضمن**.</span><span class="sxs-lookup"><span data-stu-id="c7850-116">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="c7850-117">في جزء الخصائص الموجود على الجانب الأيمن، ضمن **البرنامج النصي المضمن**، أدخل البرنامج النصي من جانب العميل.</span><span class="sxs-lookup"><span data-stu-id="c7850-117">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="c7850-118">قم بعد ذلك بتكوين الخيارات الأخرى كما تتطلب.</span><span class="sxs-lookup"><span data-stu-id="c7850-118">Then configure other options as you require.</span></span>
1. <span data-ttu-id="c7850-119">حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="c7850-119">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c7850-120">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="c7850-120">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="c7850-121">إنشاء جزء قابل لإعادة الاستخدام للتعليمات البرمجية لبرنامج نصي خارجي</span><span class="sxs-lookup"><span data-stu-id="c7850-121">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="c7850-122">لإنشاء جزء قابل لإعادة الاستخدام للتعليمات البرمجية للبرنامج النصي الخارجي في منشئ المواقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c7850-122">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c7850-123">انتقل إلى **الأجزاء**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="c7850-123">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="c7850-124">في مربع الحوار **جزء جديد**، حدد **البرنامج النصي الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="c7850-124">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="c7850-125">ضمن **اسم الجزء**، أدخل اسمًا لهذا الجزء، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c7850-125">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="c7850-126">ضمن الجزء الذي قمت بإنشائه، حدد الوحدة **البرنامج النصي الافتراضي الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="c7850-126">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="c7850-127">في جزء الخصائص الموجود على الجانب الأيمن، ضمن **مصدر البرنامج النصي**، أضف عنوان URL خارجيًا أو ذي صلة لمصدر البرنامج النصي الخارجي.</span><span class="sxs-lookup"><span data-stu-id="c7850-127">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="c7850-128">قم بعد ذلك بتكوين الخيارات الأخرى كما تتطلب.</span><span class="sxs-lookup"><span data-stu-id="c7850-128">Then configure other options as you require.</span></span>
1. <span data-ttu-id="c7850-129">حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="c7850-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c7850-130">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="c7850-130">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="c7850-131">إذا تم تمكين نهج أمان المحتوي (CSP) للموقع الخاص بك، فتاكد من أضافه كافة عناوين URL الخارجية إلى توجيه CSP **مصدر النص البرمجي** في أداة إنشاء موقع Commerce.</span><span class="sxs-lookup"><span data-stu-id="c7850-131">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="c7850-132">لمزيد من المعلومات، راجع [إدارة سياسة أمان المحتوى (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="c7850-132">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="c7850-133">أضف جزء يحتوي على التعليمات البرمجية للبرنامج النصي إلى قالب</span><span class="sxs-lookup"><span data-stu-id="c7850-133">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="c7850-134">لإضافة جزء يتضمن التعليمات البرمجية للبرنامج النصي إلى قالب في منشئ المواقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c7850-134">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c7850-135">انتقل إلى **القوالب**، وافتح القالب الخاص بالصفحات التي تريد إضافة التعليمات البرمجية لبرنامج نصي اليها.</span><span class="sxs-lookup"><span data-stu-id="c7850-135">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="c7850-136">في الجزء الأيسر، قم بتوسيع التدرج الهرمي للقالب لإظهار فتحة **عنوان HTML** .</span><span class="sxs-lookup"><span data-stu-id="c7850-136">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="c7850-137">في فتحة **رأس HTML‬‏‫**، حدد زر علامة القطع (**...**)، ثم حدد **إضافة جزء**.</span><span class="sxs-lookup"><span data-stu-id="c7850-137">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="c7850-138">حدد الجزء الذي قمت بإنشاءه للتعليمات البرمجية لبرنامجك النصي.</span><span class="sxs-lookup"><span data-stu-id="c7850-138">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="c7850-139">حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="c7850-139">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c7850-140">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="c7850-140">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="c7850-141">إضافة برنامج نصي خارجي أو برنامج نصي مضمن مباشرةً إلى قالب</span><span class="sxs-lookup"><span data-stu-id="c7850-141">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="c7850-142">إذا كنت ترغب في إدراج برنامج نصي مضمن أو خارجي مباشرةً في مجموعة من الصفحات التي يتم التحكم فيها بواسطة قالب واحد، فلن تحتاج إلى إنشاء جزء أولاً.</span><span class="sxs-lookup"><span data-stu-id="c7850-142">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="c7850-143">إضافة برنامج نصي مضمن مباشرةً إلى قالب</span><span class="sxs-lookup"><span data-stu-id="c7850-143">Add an inline script directly to a template</span></span>

<span data-ttu-id="c7850-144">لإضافة برنامج نصي مضمن مباشرةً إلى قالب في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c7850-144">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c7850-145">انتقل إلى **القوالب**، وافتح القالب الخاص بالصفحات التي تريد إضافة التعليمات البرمجية لبرنامج نصي اليها.</span><span class="sxs-lookup"><span data-stu-id="c7850-145">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="c7850-146">في الجزء الأيسر، قم بتوسيع التدرج الهرمي للقالب لإظهار فتحة **عنوان HTML** .</span><span class="sxs-lookup"><span data-stu-id="c7850-146">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="c7850-147">في فتحة **عنوان HTML‬‏‫**، وحدد علامة الحذف (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="c7850-147">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c7850-148">في مربع الحوار **إضافة وحدة**، حدد **البرنامج النصي المضمن**.</span><span class="sxs-lookup"><span data-stu-id="c7850-148">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="c7850-149">في جزء الخصائص الموجود على الجانب الأيمن، ضمن **البرنامج النصي المضمن**، أدخل البرنامج النصي من جانب العميل.</span><span class="sxs-lookup"><span data-stu-id="c7850-149">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="c7850-150">قم بعد ذلك بتكوين الخيارات الأخرى كما تتطلب.</span><span class="sxs-lookup"><span data-stu-id="c7850-150">Then configure other options as you require.</span></span>
1. <span data-ttu-id="c7850-151">حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="c7850-151">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c7850-152">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="c7850-152">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="c7850-153">إضافة برنامج نصي خارجي مباشرةً إلى قالب</span><span class="sxs-lookup"><span data-stu-id="c7850-153">Add an external script directly to a template</span></span>

<span data-ttu-id="c7850-154">لإضافة برنامج نصي خارجي مباشرةً إلى قالب في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="c7850-154">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c7850-155">انتقل إلى **القوالب**، وافتح القالب الخاص بالصفحات التي تريد إضافة التعليمات البرمجية لبرنامج نصي اليها.</span><span class="sxs-lookup"><span data-stu-id="c7850-155">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="c7850-156">في الجزء الأيسر، قم بتوسيع التدرج الهرمي للقالب لإظهار فتحة **عنوان HTML** .</span><span class="sxs-lookup"><span data-stu-id="c7850-156">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="c7850-157">في فتحة **عنوان HTML‬‏‫**، وحدد علامة الحذف (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="c7850-157">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c7850-158">في مربع الحوار **إضافة وحدة**، حدد **البرنامج النصي الخارجي**.</span><span class="sxs-lookup"><span data-stu-id="c7850-158">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="c7850-159">في جزء الخصائص الموجود على الجانب الأيمن، ضمن **مصدر البرنامج النصي**، أضف عنوان URL خارجيًا أو ذي صلة لمصدر البرنامج النصي الخارجي.</span><span class="sxs-lookup"><span data-stu-id="c7850-159">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="c7850-160">قم بعد ذلك بتكوين الخيارات الأخرى كما تتطلب.</span><span class="sxs-lookup"><span data-stu-id="c7850-160">Then configure other options as you require.</span></span>
1. <span data-ttu-id="c7850-161">حدد **حفظ**، ثم قم بتحديد **إنهاء التحرير**.</span><span class="sxs-lookup"><span data-stu-id="c7850-161">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c7850-162">حدد **نشر**.</span><span class="sxs-lookup"><span data-stu-id="c7850-162">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7850-163">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="c7850-163">Additional resources</span></span>

[<span data-ttu-id="c7850-164">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="c7850-164">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="c7850-165">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="c7850-165">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="c7850-166">العمل CSS مع ملفات التجاوز</span><span class="sxs-lookup"><span data-stu-id="c7850-166">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="c7850-167">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="c7850-167">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="c7850-168">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="c7850-168">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="c7850-169">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="c7850-169">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="c7850-170">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="c7850-170">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
