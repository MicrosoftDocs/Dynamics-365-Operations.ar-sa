---
title: تكوين التكاليف القياسية للعمالة والمصروفات
description: يشرح هذا الموضوع كيفية إعداد التكاليف القياسية للعمالة والمصروفات لمشروع.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867716"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="8c13d-103">تكوين التكاليف القياسية للعمالة والمصروفات</span><span class="sxs-lookup"><span data-stu-id="8c13d-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8c13d-104">يشرح هذا الموضوع كيفية إعداد التكاليف القياسية للعمالة والمصروفات لمشروع.</span><span class="sxs-lookup"><span data-stu-id="8c13d-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="8c13d-105">تستخدم هذه المهمة مجموعة بيانات USSI.</span><span class="sxs-lookup"><span data-stu-id="8c13d-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="8c13d-106">في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة المشاريع ومحاسبتها > الإعداد > الأسعار > سعر التكلفة (الساعة)‬‬**.</span><span class="sxs-lookup"><span data-stu-id="8c13d-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="8c13d-107">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8c13d-107">Select **New**.</span></span>
3. <span data-ttu-id="8c13d-108">في حقل **تاريخ السريان**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="8c13d-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="8c13d-109">في حقل **سعر التكلفة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="8c13d-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="8c13d-110">يمكنك إعداد سعر تكلفة قياسي لفئة المشروع أو يمكنك إعداد سعر تكلفة حسب رقم العامل أو رقم المشروع أو الفئة أو التاريخ أو أي مجموعة من هذه العناصر.</span><span class="sxs-lookup"><span data-stu-id="8c13d-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="8c13d-111">وسيكون سعر التكلفة الذي يتم تطبيقه سعر التكلفة الذي يتسم بأعلى مستوى من التفصيل.</span><span class="sxs-lookup"><span data-stu-id="8c13d-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="8c13d-112">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8c13d-112">Select **Save**.</span></span>
6. <span data-ttu-id="8c13d-113">في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة المشاريع ومحاسبتها > الإعداد > الأسعار > سعر المبيعات (الساعة)‬‬**.</span><span class="sxs-lookup"><span data-stu-id="8c13d-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="8c13d-114">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8c13d-114">Select **New**.</span></span>
8. <span data-ttu-id="8c13d-115">في حقل **تاريخ السريان**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="8c13d-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="8c13d-116">في الحقل **صالح لـ**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="8c13d-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="8c13d-117">في حقل **التسعير‬**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="8c13d-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="8c13d-118">يمكنك إعداد سعر المبيعات القياسي للحركات بالساعة أو لفئة المشروع.</span><span class="sxs-lookup"><span data-stu-id="8c13d-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="8c13d-119">ويمكنك أيضًا إعداد أسعار المبيعات حسب رقم العامل أو رقم المشروع أو الفئة أو تاريخ الحركة أو أية مجموعة من هذه العناصر.</span><span class="sxs-lookup"><span data-stu-id="8c13d-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="8c13d-120">ويكون سعر المبيعات الفعلي، الذي يتم استخدامه عندما يقوم العامل بإدخال حركة في دفتر يومية الساعات، سعر المبيعات بأعلى مستوى من التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="8c13d-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="8c13d-121">على سبيل المثال، عند إعداد سعر مبيعات عام وسعر مبيعات خاص بالعامل، يتم استخدام سعر المبيعات الخاص بالعامل.</span><span class="sxs-lookup"><span data-stu-id="8c13d-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="8c13d-122">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8c13d-122">Select **Save**.</span></span>
12. <span data-ttu-id="8c13d-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="8c13d-123">Close the page.</span></span>
13. <span data-ttu-id="8c13d-124">في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة المشاريع ومحاسبتها > الإعداد > الأسعار > سعر التكلفة (المصروفات)‬‬**.</span><span class="sxs-lookup"><span data-stu-id="8c13d-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="8c13d-125">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8c13d-125">Select **New**.</span></span>
15. <span data-ttu-id="8c13d-126">في حقل **تاريخ السريان**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="8c13d-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="8c13d-127">في حقل **سعر التكلفة**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="8c13d-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="8c13d-128">يمكن تعبئة حقول متعددة، ولكن هذا هو الحد الأدنى المطلوب لحفظ السجل.</span><span class="sxs-lookup"><span data-stu-id="8c13d-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="8c13d-129">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8c13d-129">Select **Save**.</span></span>
18. <span data-ttu-id="8c13d-130">في جزء التنقل، انتقل إلى **الوحدات النمطية > إدارة المشاريع ومحاسبتها > الإعداد > الأسعار > سعر المبيعات (المصروفات)‬‬**.</span><span class="sxs-lookup"><span data-stu-id="8c13d-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="8c13d-131">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8c13d-131">Select **New**.</span></span>
20. <span data-ttu-id="8c13d-132">في حقل **تاريخ السريان**، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="8c13d-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="8c13d-133">في الحقل **صالح لـ**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="8c13d-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="8c13d-134">في حقل **التسعير‬**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="8c13d-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="8c13d-135">يعتبر سعر المبيعات الفعلي، الذي يتم تطبيقه عندما يقوم العامل بإدخال الحركات في دفتر يومية المصروفات، سعر المبيعات بأعلى مستوى من التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="8c13d-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="8c13d-136">على سبيل المثال، عند إعداد سعر مبيعات عام وسعر مبيعات خاص بالعامل، يتم استخدام سعر المبيعات الخاص بالعامل.</span><span class="sxs-lookup"><span data-stu-id="8c13d-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="8c13d-137">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8c13d-137">Select **Save**.</span></span>

