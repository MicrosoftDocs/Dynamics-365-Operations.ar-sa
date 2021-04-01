---
title: وحدة Iframe
description: يتناول هذا الموضوع الوحدة iframe ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 178469d58e5cb619c3eacfa6760f0eaec18be0dc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206122"
---
# <a name="iframe-module"></a><span data-ttu-id="0370f-103">وحدة Iframe</span><span class="sxs-lookup"><span data-stu-id="0370f-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0370f-104">يتناول هذا الموضوع الوحدة iframe ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0370f-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0370f-105">وحدة iframe توفر iframe (اطار مضمن) يستضيف المحتوى الخارجي في موقع.</span><span class="sxs-lookup"><span data-stu-id="0370f-105">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="0370f-106">على سبيل المثال، يمكن استخدامه لاستضافة فيديو YouTube أو عارض ملفات PDF على أي صفحة موقع.</span><span class="sxs-lookup"><span data-stu-id="0370f-106">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="0370f-107">تتطلب وحدة iframe عنوان URL مستهدف.</span><span class="sxs-lookup"><span data-stu-id="0370f-107">An iframe module requires a target URL.</span></span> <span data-ttu-id="0370f-108">ثم تستضيف محتوى الصفحة المستهدفة داخل عنصر **iframe‎** HTML.</span><span class="sxs-lookup"><span data-stu-id="0370f-108">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="0370f-109">يجب أن تكون عناوين URL الخارجية على قائمة السماح وفقًا لتوجيهات سياسة أمان المحتوى (CSP) الخاصة بالموقع.</span><span class="sxs-lookup"><span data-stu-id="0370f-109">External URLs must be on the allow list per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="0370f-110">بالنسبة لمحتوى iframe، يجب أن تكون عناوين URL مسموحة وفقًا لتوجيه **frame-ancestor**.</span><span class="sxs-lookup"><span data-stu-id="0370f-110">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="0370f-111">لمزيد من المعلومات، راجع [إدارة سياسة أمان المحتوى (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="0370f-111">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

> [!NOTE]
> <span data-ttu-id="0370f-112">تتوفر الوحدة النمطية iframe في Dynamics 365 Commerce الإصدار 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="0370f-112">The iframe module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="0370f-113">تعرض الصورة التالية أمثلة عن وحدات iframe التي تعرض مقاطع فيديو خارجية على صفحات الموقع.</span><span class="sxs-lookup"><span data-stu-id="0370f-113">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![مثال عن وحدات iframe تعرض مقاطع فيديو خارجية](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="0370f-115">خصائص ‏‫وحدة Iframe</span><span class="sxs-lookup"><span data-stu-id="0370f-115">Iframe module properties</span></span>

| <span data-ttu-id="0370f-116">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="0370f-116">Property name</span></span>             | <span data-ttu-id="0370f-117">قيمة</span><span class="sxs-lookup"><span data-stu-id="0370f-117">Value</span></span>                 | <span data-ttu-id="0370f-118">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="0370f-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="0370f-119">العنوان</span><span class="sxs-lookup"><span data-stu-id="0370f-119">Heading</span></span> | <span data-ttu-id="0370f-120">النص</span><span class="sxs-lookup"><span data-stu-id="0370f-120">Text</span></span> | <span data-ttu-id="0370f-121">عنوان الوحدة النمطية.</span><span class="sxs-lookup"><span data-stu-id="0370f-121">The heading for the module.</span></span> |
| <span data-ttu-id="0370f-122">URL هدف</span><span class="sxs-lookup"><span data-stu-id="0370f-122">Target URL</span></span> | <span data-ttu-id="0370f-123">URL</span><span class="sxs-lookup"><span data-stu-id="0370f-123">URL</span></span> | <span data-ttu-id="0370f-124">عنوان URL المستضاف في الوحدة.</span><span class="sxs-lookup"><span data-stu-id="0370f-124">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="0370f-125">الارتفاع</span><span class="sxs-lookup"><span data-stu-id="0370f-125">Height</span></span> | <span data-ttu-id="0370f-126">الرقم أو النسبة المئوية</span><span class="sxs-lookup"><span data-stu-id="0370f-126">Number or percentage</span></span> | <span data-ttu-id="0370f-127">ارتفاع الوحدة، بالبكسل أو كنسبة مئوية.</span><span class="sxs-lookup"><span data-stu-id="0370f-127">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="0370f-128">على سبيل المثال، ستتم معاملة القيمة **100** كعدد وحدات البكسل والقيمة **100%** كنسبة مئوية.</span><span class="sxs-lookup"><span data-stu-id="0370f-128">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="0370f-129">تسمية المنطقة</span><span class="sxs-lookup"><span data-stu-id="0370f-129">Aria label</span></span> | <span data-ttu-id="0370f-130">النص</span><span class="sxs-lookup"><span data-stu-id="0370f-130">Text</span></span> | <span data-ttu-id="0370f-131">يمكن تحديد تسمية تطبيقات الإنترنت الغنية القابلة للوصول (ARIA) لأغراض إمكانية الوصول.</span><span class="sxs-lookup"><span data-stu-id="0370f-131">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="0370f-132">إضافة وحدة iframe إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="0370f-132">Add an iframe module to a page</span></span>

<span data-ttu-id="0370f-133">لإضافة وحدة iframe إلى صفحة لعرض فيديو خارجي، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0370f-133">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="0370f-134">انتقل إلى **القوالب**، ثم حدد **جديد** لإنشاء قالب جديد.</span><span class="sxs-lookup"><span data-stu-id="0370f-134">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="0370f-135">في مربع الحوار **قالب جديد**، تحت **اسم القالب**، أدخل **قالب التسويق**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0370f-135">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="0370f-136">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع القالب، ثم حدد **نشر** لنشره.</span><span class="sxs-lookup"><span data-stu-id="0370f-136">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="0370f-137">انتقل إلى **الصفحات**، ثم حدد **جديد** لإنشاء صفحة جديدة.</span><span class="sxs-lookup"><span data-stu-id="0370f-137">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="0370f-138">في مربع الحوار **اختيار قالب**، حدد القالب **قالب التسويق**.</span><span class="sxs-lookup"><span data-stu-id="0370f-138">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="0370f-139">ضمن **اسم الصفحة**، أدخل **صفحة تسويق**، ثم حدد **موافق‏‎**.</span><span class="sxs-lookup"><span data-stu-id="0370f-139">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="0370f-140">في الفتحة **الرئيسية** للصفحة الجديدة، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="0370f-140">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0370f-141">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**الحاوية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0370f-141">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0370f-142">في جزء خصائص الوحدة النمطية، قم بتعيين قيمة **العرض** إلى **ملء الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="0370f-142">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="0370f-143">في فتحة **الحاوية‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="0370f-143">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0370f-144">في مربع الحوار **إضافة وحدة**، حدد وحدة **iframe‎‬‏‎**، ثم حدد **موافق‏‎**.</span><span class="sxs-lookup"><span data-stu-id="0370f-144">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0370f-145">في جزء خصائص الوحدة، قم بتعيين iframe‎ **عنوان URL‎ المستهدف** إلى عنوان URL‎ خارجي لملف فيديو.</span><span class="sxs-lookup"><span data-stu-id="0370f-145">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="0370f-146">قم بتعيين الخصائص الأخرى، مثل **العنوان** و **الارتفاع**، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="0370f-146">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="0370f-147">حدد **حفظ**، وحدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="0370f-147">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="0370f-148">انتقل إلى صفحة التسويق على موقعك.</span><span class="sxs-lookup"><span data-stu-id="0370f-148">Go to the marketing page on your site.</span></span> <span data-ttu-id="0370f-149">يجب أن ترى أن الفيديو معروضًا في وحدة iframe.</span><span class="sxs-lookup"><span data-stu-id="0370f-149">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="0370f-150">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0370f-150">Additional resources</span></span>

[<span data-ttu-id="0370f-151">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="0370f-151">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0370f-152">إدارة سياسة أمان المحتوى (CSP)</span><span class="sxs-lookup"><span data-stu-id="0370f-152">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]