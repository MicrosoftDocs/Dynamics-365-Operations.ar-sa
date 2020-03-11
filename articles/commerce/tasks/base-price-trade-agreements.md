---
title: " اتفاقيات الأسعار والتجارة الأساسية"
description: يتناول هذا الإجراء إنشاء اتفاقيات تجارية على أسعار المبيعات الخاصة بالقناة.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7576c4218118724562ff739ff9805a06b7ba22d5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021489"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="cc726-103"> اتفاقيات الأسعار والتجارة الأساسية</span><span class="sxs-lookup"><span data-stu-id="cc726-103">Base price and trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="cc726-104">يتناول هذا الإجراء إنشاء اتفاقيات تجارية على أسعار المبيعات الخاصة بالقناة.</span><span class="sxs-lookup"><span data-stu-id="cc726-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="cc726-105">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="cc726-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="cc726-106">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > البيع بالتجزئة والتجارة > إدارة الأسعار والخصومات > مجموعات الأسعار > جميع مجموعات الأسعار**.</span><span class="sxs-lookup"><span data-stu-id="cc726-106">In the **Navigation pane**, go to **Modules > Retail and Commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="cc726-107">توضح مجموعات الأسعار كيفية تعيين الاتفاقيات التجارية لقنوات معينة.</span><span class="sxs-lookup"><span data-stu-id="cc726-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="cc726-108">يؤدي استخدام مجموعات الأسعار لتعيين الاتفاقيات التجارية لقناة إلى تمكين التسعير الخاص بالقناة.</span><span class="sxs-lookup"><span data-stu-id="cc726-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="cc726-109">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="cc726-109">Click **New**.</span></span>
3. <span data-ttu-id="cc726-110">في حقل **مجموعات الأسعار**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cc726-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="cc726-111">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cc726-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="cc726-112">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="cc726-112">Click **Save**.</span></span>
6. <span data-ttu-id="cc726-113">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cc726-113">Close the page.</span></span>
7. <span data-ttu-id="cc726-114">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > البيع بالتجزئة والتجارة > القنوات > المتاجر > جميع المتاجر**.</span><span class="sxs-lookup"><span data-stu-id="cc726-114">In the **Navigation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
8. <span data-ttu-id="cc726-115">في القائمة، حدد "نيويورك".</span><span class="sxs-lookup"><span data-stu-id="cc726-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="cc726-116">في جزء "الإجراءات"، انقر فوق **المتجر**.</span><span class="sxs-lookup"><span data-stu-id="cc726-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="cc726-117">انقر فوق **مجموعات الأسعار**.</span><span class="sxs-lookup"><span data-stu-id="cc726-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="cc726-118">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="cc726-118">Click **New**.</span></span>
12. <span data-ttu-id="cc726-119">في حقل **مجموعات الأسعار**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="cc726-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="cc726-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="cc726-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="cc726-121">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="cc726-121">Click **Save**.</span></span>
15. <span data-ttu-id="cc726-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cc726-122">Close the page.</span></span>
16. <span data-ttu-id="cc726-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cc726-123">Close the page.</span></span>
17. <span data-ttu-id="cc726-124">في **جزء التنقل**، انتقل إلى **الوحدات النمطية > البيع بالتجزئة والتجارة > المنتجات والفئات > المنتجات التي تم إصدارها حسب الفئة**.</span><span class="sxs-lookup"><span data-stu-id="cc726-124">In the **Navigation pane**, go to **Modules > Retail and Commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="cc726-125">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="cc726-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="cc726-126">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="cc726-126">Click **Edit**.</span></span>
20. <span data-ttu-id="cc726-127">وسّع علامة التبويب السريعة **بيع**.</span><span class="sxs-lookup"><span data-stu-id="cc726-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="cc726-128">في حقل **السعر**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="cc726-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="cc726-129">يتم استخدام هذا السعر إذا لم يتم العثور على أي اتفاقات تجارية قابلة للتطبيق.</span><span class="sxs-lookup"><span data-stu-id="cc726-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="cc726-130">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="cc726-130">Click **Save**.</span></span>
23. <span data-ttu-id="cc726-131">في **جزء الإجراء**، انقر فوق **بيع**.</span><span class="sxs-lookup"><span data-stu-id="cc726-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="cc726-132">انقر فوق **إنشاء اتفاقيات تجارية**.</span><span class="sxs-lookup"><span data-stu-id="cc726-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="cc726-133">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="cc726-133">Click **New**.</span></span>
26. <span data-ttu-id="cc726-134">في الحقل **الاسم**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="cc726-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="cc726-135">في القائمة، حدد **التجارة**.</span><span class="sxs-lookup"><span data-stu-id="cc726-135">In the list, select **Commerce**.</span></span> <span data-ttu-id="cc726-136">في بيانات العرض التوضيحي، يكون لاسم دفتر اليومية **التجارة** العلاقة الافتراضية **سعر (المبيعات)**.</span><span class="sxs-lookup"><span data-stu-id="cc726-136">In the demo data, the **Commerce** journal name has the default relation of **Price (sales)**.</span></span> <span data-ttu-id="cc726-137">وهذا يعني أن كافة البنود الجديدة التي تم إنشاؤها ستكون افتراضية للاتفاقيات التجارية على أسعار المبيعات.</span><span class="sxs-lookup"><span data-stu-id="cc726-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="cc726-138">في **جزء الإجراءات**، انقر فوق **البنود**.</span><span class="sxs-lookup"><span data-stu-id="cc726-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="cc726-139">في حقل **كود الحساب**، حدد "المجموعة".</span><span class="sxs-lookup"><span data-stu-id="cc726-139">In the **Account code** field, select 'Group'.</span></span>
30. <span data-ttu-id="cc726-140">في الحقل **اختيار الحساب**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="cc726-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="cc726-141">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="cc726-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="cc726-142">وهذا سيكمل الارتباط من القناة لمجموعة الأسعار إلى الاتفاقية التجارية.</span><span class="sxs-lookup"><span data-stu-id="cc726-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="cc726-143">في حقل **علاقة الصنف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="cc726-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="cc726-144">في حقل **المبلغ بالعملة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="cc726-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="cc726-145">على علامة التبويب السريعة **التفاصيل**، حدد خانة الاختيار **بحث عن التالي** أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="cc726-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="cc726-146">عندما يتم تعيين **بحث عن التالي** إلى "نعم"، سيواصل محرك التسعير البحث عن اتفاقات تجارية قابلة للتطبيق بسعر بيع أقل.</span><span class="sxs-lookup"><span data-stu-id="cc726-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="cc726-147">عندما يتم تعيين **بحث عن التالي** إلى "لا"، يتوقف محرك التسعير عن البحث ويستخدم الاتفاقية التجارية.</span><span class="sxs-lookup"><span data-stu-id="cc726-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="cc726-148">انقر فوق **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="cc726-148">Click **Post**.</span></span>
36. <span data-ttu-id="cc726-149">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cc726-149">Click **OK**.</span></span>
37. <span data-ttu-id="cc726-150">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cc726-150">Close the page.</span></span>
38. <span data-ttu-id="cc726-151">في **جزء الإجراءات**، انقر فوق "بيع‬".</span><span class="sxs-lookup"><span data-stu-id="cc726-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="cc726-152">انقر فوق **سعر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="cc726-152">Click **Sales price**.</span></span>
