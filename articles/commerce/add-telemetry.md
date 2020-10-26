---
title: إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام
description: يصف هذا الموضوع كيفيه إضافة التعليمات البرمجية لبرنامج نصي من جانب العميل إلى صفحات موقعك لدعم مجموعة تتبع الاستخدام من جانب العميل.
author: bicyclingfool
manager: annbe
ms.date: 09/29/2020
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
ms.openlocfilehash: e15ba6a0d624bd97c25936aa6d3bfafb844b66c0
ms.sourcegitcommit: 7e8a9f92a2675bf5b620889678a2918f63f3e199
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2020
ms.locfileid: "3901486"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="77375-103">إضافة تعليمات برمجية لبرنامج نصي إلى صفحات الموقع لدعم تتبع الاستخدام</span><span class="sxs-lookup"><span data-stu-id="77375-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="77375-104">يصف هذا الموضوع كيفيه إضافة التعليمات البرمجية لبرنامج نصي من جانب العميل إلى صفحات موقعك لدعم مجموعة تتبع الاستخدام من جانب العميل.</span><span class="sxs-lookup"><span data-stu-id="77375-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="77375-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="77375-105">Overview</span></span>

<span data-ttu-id="77375-106">تُعد تحليلات الويب أداة أساسية عندما ترغب في فهم كيفية تفاعل عملائك مع موقعك واتخاذ قرارات من شأنها أن تساعد في تحسين التجربة لتحقيق أقصى قدر من التحويل.</span><span class="sxs-lookup"><span data-stu-id="77375-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="77375-107">تتوفر العديد من حزم تحليلات الويب لمساعدتك في تحقيق هذه الأهداف، مثل Google Analytics وClicky وMoz Analytics وKISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="77375-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="77375-108">تتطلب معظم حزم تحليلات الويب أن تضيف التعليمات البرمجية لبرنامج نصي في عنصر **\<head\>** من HTML لجميع صفحات موقعك.</span><span class="sxs-lookup"><span data-stu-id="77375-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="77375-109">تنطبق الإرشادات الواردة في هذا الموضوع أيضًا على الوظائف المخصصة الأخرى من جانب العميل التي لا يوفرها Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="77375-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="77375-110">إنشاء جزء قابل لإعادة الاستخدام للتعليمات البرمجية لبرنامج نصي</span><span class="sxs-lookup"><span data-stu-id="77375-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="77375-111">يتيح لك الجزء إعادة استخدام التعليمات البرمجية المضمنة أو الخارجية في كافة صفحات موقعك، بغض النظر عن القالب الذي تستخدمه.</span><span class="sxs-lookup"><span data-stu-id="77375-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="77375-112">إنشاء جزء قابل لإعادة الاستخدام للتعليمات البرمجية لبرنامج نصي مضمن</span><span class="sxs-lookup"><span data-stu-id="77375-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="77375-113">لإنشاء جزء قابل لإعادة الاستخدام للتعليمات البرمجية للنص المضمن في منشئ المواقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="77375-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="77375-114">انتقل إلى **الأجزاء** ، ثم حدد **جديد** .</span><span class="sxs-lookup"><span data-stu-id="77375-114">Go to **Fragments** , and then select **New** .</span></span>
1. <span data-ttu-id="77375-115">في مربع الحوار **جزء جديد** ، حدد **البرنامج النصي المضمن** .</span><span class="sxs-lookup"><span data-stu-id="77375-115">In the **New fragment** dialog box, select **Inline script** .</span></span>
1. <span data-ttu-id="77375-116">ضمن **اسم الجزء** ، أدخل اسمًا لهذا الجزء، ثم حدد **موافق** .</span><span class="sxs-lookup"><span data-stu-id="77375-116">Under **Fragment name** , enter a name for the fragment, and then select **OK** .</span></span>
1. <span data-ttu-id="77375-117">ضمن الجزء الذي قمت بإنشائه، حدد الوحدة **البرنامج النصي الافتراضي المضمن** .</span><span class="sxs-lookup"><span data-stu-id="77375-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="77375-118">في جزء الخصائص الموجود على الجانب الأيمن، ضمن **البرنامج النصي المضمن** ، أدخل البرنامج النصي من جانب العميل.</span><span class="sxs-lookup"><span data-stu-id="77375-118">In the property pane on the right, under **Inline script** , enter your client-side script.</span></span> <span data-ttu-id="77375-119">قم بعد ذلك بتكوين الخيارات الأخرى كما تتطلب.</span><span class="sxs-lookup"><span data-stu-id="77375-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="77375-120">حدد **حفظ** ، ثم قم بتحديد **إنهاء التحرير** .</span><span class="sxs-lookup"><span data-stu-id="77375-120">Select **Save** , and then select **Finish editing** .</span></span>
1. <span data-ttu-id="77375-121">حدد **نشر** .</span><span class="sxs-lookup"><span data-stu-id="77375-121">Select **Publish** .</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="77375-122">إنشاء جزء قابل لإعادة الاستخدام للتعليمات البرمجية لبرنامج نصي خارجي</span><span class="sxs-lookup"><span data-stu-id="77375-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="77375-123">لإنشاء جزء قابل لإعادة الاستخدام للتعليمات البرمجية للبرنامج النصي الخارجي في منشئ المواقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="77375-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="77375-124">انتقل إلى **الأجزاء** ، ثم حدد **جديد** .</span><span class="sxs-lookup"><span data-stu-id="77375-124">Go to **Fragments** , and then select **New** .</span></span>
1. <span data-ttu-id="77375-125">في مربع الحوار **جزء جديد** ، حدد **البرنامج النصي الخارجي** .</span><span class="sxs-lookup"><span data-stu-id="77375-125">In the **New fragment** dialog box, select **External script** .</span></span>
1. <span data-ttu-id="77375-126">ضمن **اسم الجزء** ، أدخل اسمًا لهذا الجزء، ثم حدد **موافق** .</span><span class="sxs-lookup"><span data-stu-id="77375-126">Under **Fragment name** , enter a name for the fragment, and then select **OK** .</span></span>
1. <span data-ttu-id="77375-127">ضمن الجزء الذي قمت بإنشائه، حدد الوحدة **البرنامج النصي الافتراضي الخارجي** .</span><span class="sxs-lookup"><span data-stu-id="77375-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="77375-128">في جزء الخصائص الموجود على الجانب الأيمن، ضمن **مصدر البرنامج النصي** ، أضف عنوان URL خارجيًا أو ذي صلة لمصدر البرنامج النصي الخارجي.</span><span class="sxs-lookup"><span data-stu-id="77375-128">In the property pane on the right, under **Script source** , add an external or relative URL for the external script source.</span></span> <span data-ttu-id="77375-129">قم بعد ذلك بتكوين الخيارات الأخرى كما تتطلب.</span><span class="sxs-lookup"><span data-stu-id="77375-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="77375-130">حدد **حفظ** ، ثم قم بتحديد **إنهاء التحرير** .</span><span class="sxs-lookup"><span data-stu-id="77375-130">Select **Save** , and then select **Finish editing** .</span></span>
1. <span data-ttu-id="77375-131">حدد **نشر** .</span><span class="sxs-lookup"><span data-stu-id="77375-131">Select **Publish** .</span></span>

> [!NOTE]
> <span data-ttu-id="77375-132">إذا تم تمكين نهج أمان المحتوي (CSP) للموقع الخاص بك، فتاكد من أضافه كافة عناوين URL الخارجية إلى توجيه CSP **مصدر النص البرمجي** في أداة إنشاء موقع Commerce.</span><span class="sxs-lookup"><span data-stu-id="77375-132">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="77375-133">لمزيد من المعلومات، راجع [إدارة سياسة أمان المحتوى (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="77375-133">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="77375-134">أضف جزء يحتوي على التعليمات البرمجية للبرنامج النصي إلى قالب</span><span class="sxs-lookup"><span data-stu-id="77375-134">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="77375-135">لإضافة جزء يتضمن التعليمات البرمجية للبرنامج النصي إلى قالب في منشئ المواقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="77375-135">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="77375-136">انتقل إلى **القوالب** ، وافتح القالب الخاص بالصفحات التي تريد إضافة التعليمات البرمجية لبرنامج نصي اليها.</span><span class="sxs-lookup"><span data-stu-id="77375-136">Go to **Templates** , and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="77375-137">في الجزء الأيسر، قم بتوسيع التدرج الهرمي للقالب لإظهار فتحة **عنوان HTML** .</span><span class="sxs-lookup"><span data-stu-id="77375-137">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="77375-138">في فتحة **رأس HTML‬‏‫** ، حدد زر علامة القطع ( **...** )، ثم حدد **إضافة جزء** .</span><span class="sxs-lookup"><span data-stu-id="77375-138">In the **HTML Head** slot, select the ellipsis button ( **...** ), and then select **Add fragment** .</span></span>
1. <span data-ttu-id="77375-139">حدد الجزء الذي قمت بإنشاءه للتعليمات البرمجية لبرنامجك النصي.</span><span class="sxs-lookup"><span data-stu-id="77375-139">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="77375-140">حدد **حفظ** ، ثم قم بتحديد **إنهاء التحرير** .</span><span class="sxs-lookup"><span data-stu-id="77375-140">Select **Save** , and then select **Finish editing** .</span></span>
1. <span data-ttu-id="77375-141">حدد **نشر** .</span><span class="sxs-lookup"><span data-stu-id="77375-141">Select **Publish** .</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="77375-142">إضافة برنامج نصي خارجي أو برنامج نصي مضمن مباشرةً إلى قالب</span><span class="sxs-lookup"><span data-stu-id="77375-142">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="77375-143">إذا كنت ترغب في إدراج برنامج نصي مضمن أو خارجي مباشرةً في مجموعة من الصفحات التي يتم التحكم فيها بواسطة قالب واحد، فلن تحتاج إلى إنشاء جزء أولاً.</span><span class="sxs-lookup"><span data-stu-id="77375-143">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="77375-144">إضافة برنامج نصي مضمن مباشرةً إلى قالب</span><span class="sxs-lookup"><span data-stu-id="77375-144">Add an inline script directly to a template</span></span>

<span data-ttu-id="77375-145">لإضافة برنامج نصي مضمن مباشرةً إلى قالب في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="77375-145">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="77375-146">انتقل إلى **القوالب** ، وافتح القالب الخاص بالصفحات التي تريد إضافة التعليمات البرمجية لبرنامج نصي اليها.</span><span class="sxs-lookup"><span data-stu-id="77375-146">Go to **Templates** , and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="77375-147">في الجزء الأيسر، قم بتوسيع التدرج الهرمي للقالب لإظهار فتحة **عنوان HTML** .</span><span class="sxs-lookup"><span data-stu-id="77375-147">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="77375-148">في فتحة **عنوان HTML‬‏‫** ، وحدد علامة الحذف ( **...** )، ثم حدد **إضافة وحدة** .</span><span class="sxs-lookup"><span data-stu-id="77375-148">In the **HTML Head** slot, select the ellipsis button ( **...** ), and then select **Add Module** .</span></span>
1. <span data-ttu-id="77375-149">في مربع الحوار **إضافة وحدة** ، حدد **البرنامج النصي المضمن** .</span><span class="sxs-lookup"><span data-stu-id="77375-149">In the **Add Module** dialog box, select **Inline script** .</span></span>
1. <span data-ttu-id="77375-150">في جزء الخصائص الموجود على الجانب الأيمن، ضمن **البرنامج النصي المضمن** ، أدخل البرنامج النصي من جانب العميل.</span><span class="sxs-lookup"><span data-stu-id="77375-150">In the property pane on the right, under **Inline script** , enter your client-side script.</span></span> <span data-ttu-id="77375-151">قم بعد ذلك بتكوين الخيارات الأخرى كما تتطلب.</span><span class="sxs-lookup"><span data-stu-id="77375-151">Then configure other options as you require.</span></span>
1. <span data-ttu-id="77375-152">حدد **حفظ** ، ثم قم بتحديد **إنهاء التحرير** .</span><span class="sxs-lookup"><span data-stu-id="77375-152">Select **Save** , and then select **Finish editing** .</span></span>
1. <span data-ttu-id="77375-153">حدد **نشر** .</span><span class="sxs-lookup"><span data-stu-id="77375-153">Select **Publish** .</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="77375-154">إضافة برنامج نصي خارجي مباشرةً إلى قالب</span><span class="sxs-lookup"><span data-stu-id="77375-154">Add an external script directly to a template</span></span>

<span data-ttu-id="77375-155">لإضافة برنامج نصي خارجي مباشرةً إلى قالب في منشئ الموقع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="77375-155">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="77375-156">انتقل إلى **القوالب** ، وافتح القالب الخاص بالصفحات التي تريد إضافة التعليمات البرمجية لبرنامج نصي اليها.</span><span class="sxs-lookup"><span data-stu-id="77375-156">Go to **Templates** , and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="77375-157">في الجزء الأيسر، قم بتوسيع التدرج الهرمي للقالب لإظهار فتحة **عنوان HTML** .</span><span class="sxs-lookup"><span data-stu-id="77375-157">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="77375-158">في فتحة **عنوان HTML‬‏‫** ، وحدد علامة الحذف ( **...** )، ثم حدد **إضافة وحدة** .</span><span class="sxs-lookup"><span data-stu-id="77375-158">In the **HTML Head** slot, select the ellipsis button ( **...** ), and then select **Add Module** .</span></span>
1. <span data-ttu-id="77375-159">في مربع الحوار **إضافة وحدة** ، حدد **البرنامج النصي الخارجي** .</span><span class="sxs-lookup"><span data-stu-id="77375-159">In the **Add Module** dialog box, select **External script** .</span></span>
1. <span data-ttu-id="77375-160">في جزء الخصائص الموجود على الجانب الأيمن، ضمن **مصدر البرنامج النصي** ، أضف عنوان URL خارجيًا أو ذي صلة لمصدر البرنامج النصي الخارجي.</span><span class="sxs-lookup"><span data-stu-id="77375-160">In the property pane on the right, under **Script source** , add an external or relative URL for the external script source.</span></span> <span data-ttu-id="77375-161">قم بعد ذلك بتكوين الخيارات الأخرى كما تتطلب.</span><span class="sxs-lookup"><span data-stu-id="77375-161">Then configure other options as you require.</span></span>
1. <span data-ttu-id="77375-162">حدد **حفظ** ، ثم قم بتحديد **إنهاء التحرير** .</span><span class="sxs-lookup"><span data-stu-id="77375-162">Select **Save** , and then select **Finish editing** .</span></span>
1. <span data-ttu-id="77375-163">حدد **نشر** .</span><span class="sxs-lookup"><span data-stu-id="77375-163">Select **Publish** .</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77375-164">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="77375-164">Additional resources</span></span>

[<span data-ttu-id="77375-165">إضافة شعار</span><span class="sxs-lookup"><span data-stu-id="77375-165">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="77375-166">تحديد سمة الموقع</span><span class="sxs-lookup"><span data-stu-id="77375-166">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="77375-167">العمل CSS مع ملفات التجاوز</span><span class="sxs-lookup"><span data-stu-id="77375-167">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="77375-168">إضافة أيقونة المفضلة</span><span class="sxs-lookup"><span data-stu-id="77375-168">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="77375-169">إضافة رسالة ترحيب</span><span class="sxs-lookup"><span data-stu-id="77375-169">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="77375-170">إضافة إشعار لحقوق النشر</span><span class="sxs-lookup"><span data-stu-id="77375-170">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="77375-171">إضافة لغات إلى الموقع الخاص بك</span><span class="sxs-lookup"><span data-stu-id="77375-171">Add languages to your site</span></span>](add-languages-to-site.md)
