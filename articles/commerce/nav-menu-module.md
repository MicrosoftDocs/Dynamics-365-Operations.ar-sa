---
title: الوحدة النمطية لقائمة التنقل
description: يتناول هذا الموضوع الوحدات النمطية لقائمة التنقل ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 91239bd1db3f5819b7ad8d45ccfd8ab0d88b1b41
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817864"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="31b64-103">الوحدة النمطية لقائمة التنقل</span><span class="sxs-lookup"><span data-stu-id="31b64-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="31b64-104">يتناول هذا الموضوع الوحدات النمطية لقائمة التنقل ويصف كيفية إضافتها إلى صفحات الموقع في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="31b64-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="31b64-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="31b64-105">Overview</span></span>

<span data-ttu-id="31b64-106">الغرض الأساسي من الوحدات النمطية لقائمة التنقل هو السماح لمستخدمي الموقع باستعراض المنتجات وصفحات الموقع وفقًا للتدرج الهرمي للتنقل في مركز Dynamics 365 Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="31b64-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="31b64-107">تظهر العناصر التي تم تكوينها في الوحدة النمطية لقائمة التنقل كتنقل في رأس الموقع.</span><span class="sxs-lookup"><span data-stu-id="31b64-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="31b64-108">تدعم أيضًا الوحدات النمطية لقائمة التنقل عناصر القائمة الثابتة التي ترتبط بصفحات أخرى في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="31b64-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="31b64-109">يمكن إضافة الوحدة النمطية لقائمة التنقل إلى الوحدة النمطية لرأس الصفحة.</span><span class="sxs-lookup"><span data-stu-id="31b64-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="31b64-110">في نسق Fabrikam، تعرض قائمة التنقل مستويين بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="31b64-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="31b64-111">في نسق البادئ، تعرض قائمة التنقل ثلاثة مستويات بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="31b64-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="31b64-112">للتغيير إلى عدد المستويات، يكون امتداد العرض مطلوبًا على النسق.</span><span class="sxs-lookup"><span data-stu-id="31b64-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="31b64-113">يبين الرسم التوضيحي التالي مثالاً على قائمة تنقل لموقع Fabrikam مع مستويين من التدرج الهرمي للفئات وبعض عناصر القائمة الثابتة.</span><span class="sxs-lookup"><span data-stu-id="31b64-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="31b64-114">![مثال عن وحدة نمطية لقائمة التنقل](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="31b64-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="31b64-115">خصائص الوحدة النمطية لقائمة التنقل</span><span class="sxs-lookup"><span data-stu-id="31b64-115">Navigation menu module properties</span></span>

| <span data-ttu-id="31b64-116">اسم الخاصية</span><span class="sxs-lookup"><span data-stu-id="31b64-116">Property name</span></span>             | <span data-ttu-id="31b64-117">قيمة</span><span class="sxs-lookup"><span data-stu-id="31b64-117">Value</span></span>                 | <span data-ttu-id="31b64-118">الوصف</span><span class="sxs-lookup"><span data-stu-id="31b64-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="31b64-119">المصدر</span><span class="sxs-lookup"><span data-stu-id="31b64-119">Source</span></span>                  | <span data-ttu-id="31b64-120">**البيع بالتجزئة**، **الإنشاء اليدوي**، **البيع بالتجزئة والإنشاء اليدوي**</span><span class="sxs-lookup"><span data-stu-id="31b64-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="31b64-121">تسمح قيمة **البيع بالتجزئة** بعرض التدرج الهرمي للتنقل في القناة من مركز Commerce الرئيسي في قائمة التنقل.</span><span class="sxs-lookup"><span data-stu-id="31b64-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="31b64-122">تسمح قيمة **الإنشاء اليدوي** بتجميع عناصر القائمة الثابتة.</span><span class="sxs-lookup"><span data-stu-id="31b64-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="31b64-123">تسمح قيمة **البيع بالتجزئة والإنشاء اليدوي** بخليط من الخيارين.</span><span class="sxs-lookup"><span data-stu-id="31b64-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="31b64-124">إظهار صور الفئات</span><span class="sxs-lookup"><span data-stu-id="31b64-124">Show category images</span></span> | <span data-ttu-id="31b64-125">**صحيح** أم **خطأ**</span><span class="sxs-lookup"><span data-stu-id="31b64-125">**True** or **False**</span></span>    | <span data-ttu-id="31b64-126">تعرض هذه الخاصية، عند تمكينها، صور الفئات على قائمة التنقل كما هو محدد في مركز Commerce الرئيسي لكل فئة.</span><span class="sxs-lookup"><span data-stu-id="31b64-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="31b64-127">تمت إضافتها في الإصدار 10.0.14 من Commerce.</span><span class="sxs-lookup"><span data-stu-id="31b64-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="31b64-128">عنصر قائمة ثابتة</span><span class="sxs-lookup"><span data-stu-id="31b64-128">Static menu item</span></span>| <span data-ttu-id="31b64-129">صفيف من القيم</span><span class="sxs-lookup"><span data-stu-id="31b64-129">Array of values</span></span>| <span data-ttu-id="31b64-130">عناصر القائمة الثابتة التي تربط اسم عنصر قائمة بواسطة ارتباط إلى صفحة موقع ثابت.</span><span class="sxs-lookup"><span data-stu-id="31b64-130">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="31b64-131">يمكنك إنشاء عناصر القائمة تحت عناصر القائمة الأخرى.</span><span class="sxs-lookup"><span data-stu-id="31b64-131">You can create menu items below other menu items.</span></span> <span data-ttu-id="31b64-132">بشكل افتراضي، تظهر القوائم الثابتة عند مستوى الجذر وسيتم إلحاقها بالتدرج الهرمي للتنقل في القناة، إذا كان موجودًا.</span><span class="sxs-lookup"><span data-stu-id="31b64-132">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |

<span data-ttu-id="31b64-133">يبين الرسم التوضيحي التالي مثالاً لصورة فئة معروضة على قائمة التنقل في موقع Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="31b64-133">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="31b64-134">![مثال عن الوحدة النمطية لقائمة التنقل مع صور فئات](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="31b64-134">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="31b64-135">إضافة وحدة نمطية لقائمة تنقل إلى وحدة نمطية للرأس</span><span class="sxs-lookup"><span data-stu-id="31b64-135">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="31b64-136">للحصول على تفاصيل حول كيفية إضافة وحدة نمطية لقائمة تنقل إلى وحدة نمطية للرأس، راجع [الوحدة النمطية للرأس](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="31b64-136">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31b64-137">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="31b64-137">Additional resources</span></span>

[<span data-ttu-id="31b64-138">نظرة عامة حول مكتبة الوحدات النمطية</span><span class="sxs-lookup"><span data-stu-id="31b64-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="31b64-139">الوحدة النمطية لصندوق الشراء</span><span class="sxs-lookup"><span data-stu-id="31b64-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="31b64-140">توافق ملفات تعريف الارتباط</span><span class="sxs-lookup"><span data-stu-id="31b64-140">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="31b64-141">الوحدة النمطية للرؤوس</span><span class="sxs-lookup"><span data-stu-id="31b64-141">Header module</span></span>](author-header-module.md)
