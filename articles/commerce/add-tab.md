---
title: وحدة علامة التبويب
description: يغطي هذا الموضوع وحدات علامة التبويب ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b4187dfd704c78d506d7840b04c986687fe807a3
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621002"
---
# <a name="tab-module"></a><span data-ttu-id="8d65c-103">وحدة علامة التبويب</span><span class="sxs-lookup"><span data-stu-id="8d65c-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8d65c-104">يغطي هذا الموضوع وحدات علامة التبويب ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8d65c-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8d65c-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="8d65c-105">Overview</span></span>

<span data-ttu-id="8d65c-106">وحدات علامات التبويب هي وحدات حاوية يتم استخدامها لتنظيم المعلومات في صفحة الموقع على علامات تبويب.</span><span class="sxs-lookup"><span data-stu-id="8d65c-106">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="8d65c-107">ويمكن استخدامها على أي صفحة حيث يجب عرض المعلومات في علامات تبويب.</span><span class="sxs-lookup"><span data-stu-id="8d65c-107">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="8d65c-108">داخل كل وحدة علامة تبويب‬، يمكن إضافة وحدة أو أكثر لعناصر علامة التبويب.</span><span class="sxs-lookup"><span data-stu-id="8d65c-108">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="8d65c-109">كل وحدة عنصر علامة تبويب تمثل علامة تبويب واحدة. في كل وحدة عنصر علامة تبويب، يمكن إضافة وحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="8d65c-109">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="8d65c-110">لا توجد قيود على أنواع الوحدات التي يمكن إضافتها إلى وحدة عنصر علامة التبويب.</span><span class="sxs-lookup"><span data-stu-id="8d65c-110">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="8d65c-111">تعرض الصورة التالية مثالاً عن وحدة علامة تبويب في صفحة موقع.</span><span class="sxs-lookup"><span data-stu-id="8d65c-111">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="8d65c-112">في هذا المثال، تم تحديد علامة تبويب **الشحن**.</span><span class="sxs-lookup"><span data-stu-id="8d65c-112">In this example, the **Shipping** tab selected.</span></span>

![مثال عن وحدة علامة تبويب](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="8d65c-114">خصائص وحدة علامة التبويب</span><span class="sxs-lookup"><span data-stu-id="8d65c-114">Tab module properties</span></span>

| <span data-ttu-id="8d65c-115">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="8d65c-115">Property name</span></span> | <span data-ttu-id="8d65c-116">القيم</span><span class="sxs-lookup"><span data-stu-id="8d65c-116">Values</span></span> | <span data-ttu-id="8d65c-117">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="8d65c-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="8d65c-118">العنوان</span><span class="sxs-lookup"><span data-stu-id="8d65c-118">Heading</span></span> | <span data-ttu-id="8d65c-119">النص</span><span class="sxs-lookup"><span data-stu-id="8d65c-119">Text</span></span> | <span data-ttu-id="8d65c-120">تحدد هذه الخاصية عنوان نص اختياري لوحدة علامة التبويب.</span><span class="sxs-lookup"><span data-stu-id="8d65c-120">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="8d65c-121">فهرس علامة التبويب النشطة</span><span class="sxs-lookup"><span data-stu-id="8d65c-121">Active Tab Index</span></span> | <span data-ttu-id="8d65c-122">رقم</span><span class="sxs-lookup"><span data-stu-id="8d65c-122">Number</span></span> | <span data-ttu-id="8d65c-123">تحدد هذه الخاصية علامة التبويب التي يجب أن تكون نشطة بشكل افتراضي عند تحميل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8d65c-123">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="8d65c-124">إذا لم يتم توفير أي قيمة، يكون عنصر علامة التبويب الأولى نشطًا بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="8d65c-124">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="8d65c-125">خصائص وحدة عنصر علامة التبويب</span><span class="sxs-lookup"><span data-stu-id="8d65c-125">Tab item module properties</span></span>

| <span data-ttu-id="8d65c-126">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="8d65c-126">Property name</span></span> | <span data-ttu-id="8d65c-127">القيم</span><span class="sxs-lookup"><span data-stu-id="8d65c-127">Values</span></span> | <span data-ttu-id="8d65c-128">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="8d65c-128">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="8d65c-129">المسمى الوظيفي</span><span class="sxs-lookup"><span data-stu-id="8d65c-129">Title</span></span> | <span data-ttu-id="8d65c-130">النص</span><span class="sxs-lookup"><span data-stu-id="8d65c-130">Text</span></span> | <span data-ttu-id="8d65c-131">تحدد هذه الخاصية عنوانًا نصيًا لوحدة عنصر علامة التبويب.</span><span class="sxs-lookup"><span data-stu-id="8d65c-131">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="8d65c-132">إضافة وحدة علامة تبويب إلى صفحة</span><span class="sxs-lookup"><span data-stu-id="8d65c-132">Add a tab module to a page</span></span>

<span data-ttu-id="8d65c-133">لإضافة وحدة علامة تبويب إلى صفحة وتعيين الخصائص المطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="8d65c-133">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="8d65c-134">استخدم قالب التسويق Fabrikam (أو أي قالب لا توجد في قيود) لإنشاء صفحة جديدة تسمى **صفحة سياسات المتجر**.</span><span class="sxs-lookup"><span data-stu-id="8d65c-134">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="8d65c-135">في الفتحة **الرئيسية‏‎** في **الصفحة الافتراضية**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="8d65c-135">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8d65c-136">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**الحاوية‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8d65c-136">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8d65c-137">في فتحة **الحاوية‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="8d65c-137">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8d65c-138">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**علامة التبويب‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8d65c-138">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8d65c-139">في جزء الخصائص لوحدة علامة التبويب، حدد **العنوان** بجوار رمز القلم الرصاص.</span><span class="sxs-lookup"><span data-stu-id="8d65c-139">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="8d65c-140">في مربع الحوار **العنوان**، ضمن **نص العنوان**، أدخل نص العنوان (على سبيل المثال، **السياسات**).</span><span class="sxs-lookup"><span data-stu-id="8d65c-140">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="8d65c-141">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8d65c-141">Then select **OK**.</span></span>
1. <span data-ttu-id="8d65c-142">في فتحة **علامة التبويب‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="8d65c-142">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8d65c-143">في مربع الحوار **إضافة وحدة**، حدد وحدة ‬‏‫**عنصر علامة التبويب‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8d65c-143">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8d65c-144">في جزء الخصائص لوحدة عنصر علامة التبويب، ضمن **العنوان**، أدخل نص العنوان (على سبيل المثال، **التسليم**).</span><span class="sxs-lookup"><span data-stu-id="8d65c-144">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="8d65c-145">في فتحة **عنصر علامة التبويب‬‬‏‫**، حدد علامة القطع (**...**)، ثم حدد **إضافة وحدة**.</span><span class="sxs-lookup"><span data-stu-id="8d65c-145">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8d65c-146">في مربع الحوار **إضافة وحدة**، حدد وحدة **كتلة النص‬**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="8d65c-146">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8d65c-147">في جزء الخصائص لوحدة كتلة النص، ضمن**النص المنسق**، أدخل فقرة من النص.</span><span class="sxs-lookup"><span data-stu-id="8d65c-147">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="8d65c-148">في فتحة **علامة التبويب**، أضف بعض وحدات عناصر علامة التبويب التي لديها عناوين.</span><span class="sxs-lookup"><span data-stu-id="8d65c-148">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="8d65c-149">في كل وحدة عنصر علامة تبويب، أضف وحدة كتلة نص تتضمن هذا المحتوى.</span><span class="sxs-lookup"><span data-stu-id="8d65c-149">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="8d65c-150">حدد **حفظ**، ثم حدد **معاينة** لمعاينة الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8d65c-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="8d65c-151">ستعرض الصفحة وحدة علامة تبويب تحتوي على وحدات عناصر علامة التبويب التي تحتوي على المحتوى الذي أضفته.</span><span class="sxs-lookup"><span data-stu-id="8d65c-151">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="8d65c-152">حدد **إنهاء التحرير** لإيداع الصفحة، ثم حدد **نشر** لنشرها.</span><span class="sxs-lookup"><span data-stu-id="8d65c-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d65c-153">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8d65c-153">Additional resources</span></span>

[<span data-ttu-id="8d65c-154">نظرة عامة حول أدوات البداية</span><span class="sxs-lookup"><span data-stu-id="8d65c-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8d65c-155">وحدة الحاوية</span><span class="sxs-lookup"><span data-stu-id="8d65c-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="8d65c-156">وحدة الأكورديون</span><span class="sxs-lookup"><span data-stu-id="8d65c-156">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="8d65c-157">وحدة كتلة النص</span><span class="sxs-lookup"><span data-stu-id="8d65c-157">Text block module</span></span>](add-content-rich-block.md)
