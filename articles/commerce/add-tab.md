---
title: وحدة علامة التبويب
description: يتناول هذا الموضوع وحدات علامات التبويب ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8375c33bd6ffd3004cfc9d7b686d9a0edc77cdef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209217"
---
# <a name="tab-module"></a><span data-ttu-id="bd794-103">وحدة علامة تبويب</span><span class="sxs-lookup"><span data-stu-id="bd794-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bd794-104">يتناول هذا الموضوع وحدات علامات التبويب ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bd794-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="bd794-105">وحدات علامات التبويب هي وحدات حاوية يتم استخدامها لتنظيم المعلومات في صفحة الموقع على علامات تبويب.</span><span class="sxs-lookup"><span data-stu-id="bd794-105">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="bd794-106">ويمكن استخدامها على أي صفحة حيث يجب عرض المعلومات في علامات تبويب.</span><span class="sxs-lookup"><span data-stu-id="bd794-106">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="bd794-107">داخل كل وحدة علامة تبويب‬، يمكن إضافة وحدة أو أكثر لعناصر علامة التبويب.</span><span class="sxs-lookup"><span data-stu-id="bd794-107">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="bd794-108">كل وحدة عنصر علامة تبويب تمثل علامة تبويب واحدة. في كل وحدة عنصر علامة تبويب، يمكن إضافة وحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="bd794-108">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="bd794-109">لا توجد قيود على أنواع الوحدات التي يمكن إضافتها إلى وحدة عنصر علامة التبويب.</span><span class="sxs-lookup"><span data-stu-id="bd794-109">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="bd794-110">تعرض الصورة التالية مثالاً عن وحدة علامة تبويب في صفحة موقع.</span><span class="sxs-lookup"><span data-stu-id="bd794-110">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="bd794-111">في هذا المثال، تم تحديد علامة تبويب **الشحن**.</span><span class="sxs-lookup"><span data-stu-id="bd794-111">In this example, the **Shipping** tab selected.</span></span>

![مثال عن وحدة علامة تبويب](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="bd794-113">خصائص وحدة علامة التبويب</span><span class="sxs-lookup"><span data-stu-id="bd794-113">Tab module properties</span></span>

| <span data-ttu-id="bd794-114">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="bd794-114">Property name</span></span> | <span data-ttu-id="bd794-115">القيم</span><span class="sxs-lookup"><span data-stu-id="bd794-115">Values</span></span> | <span data-ttu-id="bd794-116">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="bd794-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="bd794-117">العنوان</span><span class="sxs-lookup"><span data-stu-id="bd794-117">Heading</span></span> | <span data-ttu-id="bd794-118">النص</span><span class="sxs-lookup"><span data-stu-id="bd794-118">Text</span></span> | <span data-ttu-id="bd794-119">تحدد هذه الخاصية عنوان نص اختياري لوحدة علامة التبويب.</span><span class="sxs-lookup"><span data-stu-id="bd794-119">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="bd794-120">فهرس علامة التبويب النشطة</span><span class="sxs-lookup"><span data-stu-id="bd794-120">Active Tab Index</span></span> | <span data-ttu-id="bd794-121">رقم</span><span class="sxs-lookup"><span data-stu-id="bd794-121">Number</span></span> | <span data-ttu-id="bd794-122">تحدد هذه الخاصية علامة التبويب التي يجب أن تكون نشطة بشكل افتراضي عند تحميل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bd794-122">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="bd794-123">إذا لم يتم توفير أي قيمة، يكون عنصر علامة التبويب الأولى نشطًا بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="bd794-123">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="bd794-124">خصائص وحدة عنصر علامة التبويب</span><span class="sxs-lookup"><span data-stu-id="bd794-124">Tab item module properties</span></span>

| <span data-ttu-id="bd794-125">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="bd794-125">Property name</span></span> | <span data-ttu-id="bd794-126">القيم</span><span class="sxs-lookup"><span data-stu-id="bd794-126">Values</span></span> | <span data-ttu-id="bd794-127">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="bd794-127">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="bd794-128">المسمى الوظيفي</span><span class="sxs-lookup"><span data-stu-id="bd794-128">Title</span></span> | <span data-ttu-id="bd794-129">النص</span><span class="sxs-lookup"><span data-stu-id="bd794-129">Text</span></span> | <span data-ttu-id="bd794-130">تحدد هذه الخاصية عنوانًا نصيًا لوحدة عنصر علامة التبويب.</span><span class="sxs-lookup"><span data-stu-id="bd794-130">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="bd794-131">إضافة وحدة علامة تبويب إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="bd794-131">Add a tab module to a page</span></span>

<span data-ttu-id="bd794-132">لإضافة وحدة علامة تبويب إلى صفحة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="bd794-132">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="bd794-133">استخدم قالب التسويق Fabrikam (أو أي قالب لا توجد في قيود) لإنشاء صفحة جديدة تسمى **صفحة سياسات المتجر**.</span><span class="sxs-lookup"><span data-stu-id="bd794-133">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="bd794-134">في الفتحة **الرئيسية‏‎** في **الصفحة الافتراضية**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="bd794-134">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bd794-135">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**الحاوية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bd794-135">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bd794-136">في فتحة **الحاوية‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="bd794-136">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bd794-137">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**علامة التبويب‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bd794-137">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bd794-138">في جزء الخصائص لوحدة علامة التبويب، حدد **العنوان** بجوار رمز القلم الرصاص.</span><span class="sxs-lookup"><span data-stu-id="bd794-138">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="bd794-139">في مربع الحوار **العنوان**، ضمن **نص العنوان**، أدخل نص العنوان (على سبيل المثال، **السياسات**).</span><span class="sxs-lookup"><span data-stu-id="bd794-139">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="bd794-140">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bd794-140">Then select **OK**.</span></span>
1. <span data-ttu-id="bd794-141">في فتحة **علامة التبويب‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="bd794-141">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bd794-142">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**عنصر علامة التبويب‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bd794-142">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bd794-143">في جزء الخصائص لوحدة عنصر علامة التبويب، ضمن **العنوان**، أدخل نص العنوان (على سبيل المثال، **التسليم**).</span><span class="sxs-lookup"><span data-stu-id="bd794-143">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="bd794-144">في فتحة **عنصر علامة التبويب‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="bd794-144">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bd794-145">في مربع الحوار **إضافة وحدة**، حدد وحدة **كتلة النص‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bd794-145">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bd794-146">في جزء الخصائص لوحدة كتلة النص، ضمن **النص المنسق**، أدخل فقرة من النص.</span><span class="sxs-lookup"><span data-stu-id="bd794-146">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="bd794-147">في فتحة **علامة التبويب**، أضف بعض وحدات عناصر علامة التبويب التي لديها عناوين.</span><span class="sxs-lookup"><span data-stu-id="bd794-147">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="bd794-148">في كل وحدة عنصر علامة تبويب، أضف وحدة كتلة نص تتضمن هذا المحتوى.</span><span class="sxs-lookup"><span data-stu-id="bd794-148">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="bd794-149">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="bd794-149">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="bd794-150">ستعرض الصفحة وحدة علامة تبويب تحتوي على وحدات عناصر علامة التبويب التي تحتوي على المحتوى الذي أضفته.</span><span class="sxs-lookup"><span data-stu-id="bd794-150">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="bd794-151">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="bd794-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd794-152">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="bd794-152">Additional resources</span></span>

[<span data-ttu-id="bd794-153">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="bd794-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bd794-154">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="bd794-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="bd794-155">وحدة أككورديون</span><span class="sxs-lookup"><span data-stu-id="bd794-155">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="bd794-156">وحدة كتلة النص</span><span class="sxs-lookup"><span data-stu-id="bd794-156">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]