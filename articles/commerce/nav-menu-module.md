---
title: الوحدة النمطية لقائمة التنقل
description: يتناول هذا الموضوع الوحدات النمطية لقائمة التنقل ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 65f8b6128b140f3fa776659d8920dfc5e095213f
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097380"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="135b2-103">الوحدة النمطية لقائمة التنقل</span><span class="sxs-lookup"><span data-stu-id="135b2-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="135b2-104">يتناول هذا الموضوع الوحدات النمطية لقائمة التنقل ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="135b2-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="135b2-105">الغرض الأساسي من الوحدات النمطية لقائمة التنقل هو السماح لمستخدمي الموقع باستعراض المنتجات وصفحات الموقع وفقًا للتدرج الهرمي للتنقل في مركز Dynamics 365 Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="135b2-105">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="135b2-106">تظهر العناصر التي تم تكوينها في الوحدة النمطية لقائمة التنقل كتنقل في رأس الموقع.</span><span class="sxs-lookup"><span data-stu-id="135b2-106">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="135b2-107">تدعم أيضًا الوحدات النمطية لقائمة التنقل عناصر القائمة الثابتة التي ترتبط بصفحات أخرى في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="135b2-107">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="135b2-108">يمكن إضافة الوحدة النمطية لقائمة التنقل إلى الوحدة النمطية لرأس الصفحة.</span><span class="sxs-lookup"><span data-stu-id="135b2-108">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="135b2-109">في نسق Fabrikam، تعرض قائمة التنقل مستويين بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="135b2-109">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="135b2-110">في نسق البادئ، تعرض قائمة التنقل ثلاثة مستويات بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="135b2-110">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="135b2-111">للتغيير إلى عدد المستويات، يكون امتداد العرض مطلوبًا على النسق.</span><span class="sxs-lookup"><span data-stu-id="135b2-111">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="135b2-112">يبين الرسم التوضيحي التالي مثالاً على قائمة تنقل لموقع Fabrikam مع مستويين من التدرج الهرمي للفئات وبعض عناصر القائمة الثابتة.</span><span class="sxs-lookup"><span data-stu-id="135b2-112">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="135b2-113">![مثال عن وحدة نمطية لقائمة التنقل](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="135b2-113">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="135b2-114">خصائص الوحدة النمطية لقائمة التنقل</span><span class="sxs-lookup"><span data-stu-id="135b2-114">Navigation menu module properties</span></span>

| <span data-ttu-id="135b2-115">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="135b2-115">Property name</span></span>             | <span data-ttu-id="135b2-116">قيمة</span><span class="sxs-lookup"><span data-stu-id="135b2-116">Value</span></span>                 | <span data-ttu-id="135b2-117">الوصف</span><span class="sxs-lookup"><span data-stu-id="135b2-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="135b2-118">المصدر</span><span class="sxs-lookup"><span data-stu-id="135b2-118">Source</span></span>                  | <span data-ttu-id="135b2-119">**البيع بالتجزئة**، **الإنشاء اليدوي**، **البيع بالتجزئة والإنشاء اليدوي**</span><span class="sxs-lookup"><span data-stu-id="135b2-119">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="135b2-120">تسمح قيمة **البيع بالتجزئة** بعرض التدرج الهرمي للتنقل في القناة من مركز Commerce الرئيسي في قائمة التنقل.</span><span class="sxs-lookup"><span data-stu-id="135b2-120">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="135b2-121">تسمح قيمة **الإنشاء اليدوي** بتجميع عناصر القائمة الثابتة.</span><span class="sxs-lookup"><span data-stu-id="135b2-121">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="135b2-122">تسمح قيمة **البيع بالتجزئة والإنشاء اليدوي** بخليط من الخيارين.</span><span class="sxs-lookup"><span data-stu-id="135b2-122">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="135b2-123">إظهار صور الفئات</span><span class="sxs-lookup"><span data-stu-id="135b2-123">Show category images</span></span> | <span data-ttu-id="135b2-124">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="135b2-124">**True** or **False**</span></span>    | <span data-ttu-id="135b2-125">تعرض هذه الخاصية، عند تمكينها، صور الفئات على قائمة التنقل كما هو محدد في مركز Commerce الرئيسي لكل فئة.</span><span class="sxs-lookup"><span data-stu-id="135b2-125">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="135b2-126">تمت إضافتها في الإصدار 10.0.14 من Commerce.</span><span class="sxs-lookup"><span data-stu-id="135b2-126">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="135b2-127">إظهار العروض الترويجية</span><span class="sxs-lookup"><span data-stu-id="135b2-127">Show promotions</span></span> | <span data-ttu-id="135b2-128">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="135b2-128">**True** or **False**</span></span> | <span data-ttu-id="135b2-129">عند تمكين هذه الخاصية، يمكن تكوين الترقيات باستخدام الصور والارتباطات والنصوص.</span><span class="sxs-lookup"><span data-stu-id="135b2-129">When this property is enabled, promotions can be configured by using images, links, and text.</span></span> <span data-ttu-id="135b2-130">تمت إضافة هذه الخاصية في إصدار 10.0.17 من Commerce.</span><span class="sxs-lookup"><span data-stu-id="135b2-130">This property was added in the Commerce version 10.0.17 release.</span></span> |
| <span data-ttu-id="135b2-131">إضافة العروض الترويجية</span><span class="sxs-lookup"><span data-stu-id="135b2-131">Add promotions</span></span> | <span data-ttu-id="135b2-132">نص أو صورة أو ارتباط</span><span class="sxs-lookup"><span data-stu-id="135b2-132">Text, image, or link</span></span> | <span data-ttu-id="135b2-133">عند تمكين الخاصية **إظهار العروض الترويجية**، يمكنك إضافة نص أو صورة أو ارتباط كمحتوى ترويجي في قائمة التنقل.</span><span class="sxs-lookup"><span data-stu-id="135b2-133">When the **Show promotions** property is enabled, you can add text, an image, or a link as promotional content on the navigation menu.</span></span> |
| <span data-ttu-id="135b2-134">تمكين قائمة التنقل متعددة المستويات</span><span class="sxs-lookup"><span data-stu-id="135b2-134">Enable multi-level navigation menu</span></span> | <span data-ttu-id="135b2-135">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="135b2-135">**True** or **False**</span></span> | <span data-ttu-id="135b2-136">عند تمكين هذه الخاصية، يمكن أن تعرض قائمة التنقل مستويات متعددة من التسلسل الهرمي للتنقل.</span><span class="sxs-lookup"><span data-stu-id="135b2-136">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="135b2-137">تتوفر هذه الميزة في إصدار Commerce رقم 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="135b2-137">This feature is available in the Commerce version 10.0.15 release.</span></span> |
| <span data-ttu-id="135b2-138">عدد المستويات</span><span class="sxs-lookup"><span data-stu-id="135b2-138">Number of levels</span></span> | <span data-ttu-id="135b2-139">عدد صحيح</span><span class="sxs-lookup"><span data-stu-id="135b2-139">integer</span></span> | <span data-ttu-id="135b2-140">تحدد هذه الخاصية عدد المستويات التي يجب إظهارها إذا **تم تعيين الخاصية تمكين قائمة التنقل متعددة المستويات** على **صحيح**.</span><span class="sxs-lookup"><span data-stu-id="135b2-140">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="135b2-141">عنصر قائمة ثابتة</span><span class="sxs-lookup"><span data-stu-id="135b2-141">Static menu item</span></span>| <span data-ttu-id="135b2-142">صفيف من القيم</span><span class="sxs-lookup"><span data-stu-id="135b2-142">Array of values</span></span>| <span data-ttu-id="135b2-143">عناصر القائمة الثابتة التي تربط اسم عنصر قائمة بواسطة ارتباط إلى صفحة موقع ثابت.</span><span class="sxs-lookup"><span data-stu-id="135b2-143">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="135b2-144">يمكنك إنشاء عناصر القائمة تحت عناصر القائمة الأخرى.</span><span class="sxs-lookup"><span data-stu-id="135b2-144">You can create menu items below other menu items.</span></span> <span data-ttu-id="135b2-145">بشكل افتراضي، تظهر القوائم الثابتة عند مستوى الجذر وسيتم إلحاقها بالتدرج الهرمي للتنقل في القناة، إذا كان موجودًا.</span><span class="sxs-lookup"><span data-stu-id="135b2-145">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="135b2-146">إظهار قائمة الجذر</span><span class="sxs-lookup"><span data-stu-id="135b2-146">Show root menu</span></span> | <span data-ttu-id="135b2-147">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="135b2-147">**True** or **False**</span></span> | <span data-ttu-id="135b2-148">عند تمكين هذه الخاصية، يمكن تعريف قائمة التنقل ضمن جذر مخصص (على سبيل المثال، **التسوق الآن**).</span><span class="sxs-lookup"><span data-stu-id="135b2-148">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now**).</span></span> <span data-ttu-id="135b2-149">تتوفر هذه الميزة في الإصدار 10.0.15 من Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="135b2-149">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="135b2-150">قائمة الجذر</span><span class="sxs-lookup"><span data-stu-id="135b2-150">Root menu</span></span> | <span data-ttu-id="135b2-151">سلسلة</span><span class="sxs-lookup"><span data-stu-id="135b2-151">string</span></span> | <span data-ttu-id="135b2-152">يمكن استخدام هذه الخاصية لتعريف النص للحصول على جذر مخصص إذا تم تعيين الخاصية **إظهار قائمة الجذر** إلى **صحيح**.</span><span class="sxs-lookup"><span data-stu-id="135b2-152">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="135b2-153">يبين الرسم التوضيحي التالي مثالاً لصورة فئة معروضة على قائمة التنقل في موقع Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="135b2-153">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="135b2-154">![مثال عن الوحدة النمطية لقائمة التنقل مع صور فئات](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="135b2-154">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="135b2-155">إضافة وحدة نمطية لقائمة تنقل إلى وحدة نمطية للرأس</span><span class="sxs-lookup"><span data-stu-id="135b2-155">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="135b2-156">للحصول على تفاصيل حول كيفية إضافة وحدة نمطية لقائمة تنقل إلى وحدة نمطية للرأس، راجع [الوحدة النمطية للرأس](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="135b2-156">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="135b2-157">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="135b2-157">Additional resources</span></span>

[<span data-ttu-id="135b2-158">نظرة عامة على مكتبة الوحدات</span><span class="sxs-lookup"><span data-stu-id="135b2-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="135b2-159">الوحدة النمطية لمسار التنقل</span><span class="sxs-lookup"><span data-stu-id="135b2-159">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="135b2-160">الوحدة النمطية لمحدد الموقع</span><span class="sxs-lookup"><span data-stu-id="135b2-160">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="135b2-161">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="135b2-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="135b2-162">توافق ملفات تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="135b2-162">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="135b2-163">الوحدة النمطية للرؤوس</span><span class="sxs-lookup"><span data-stu-id="135b2-163">Header module</span></span>](author-header-module.md)
