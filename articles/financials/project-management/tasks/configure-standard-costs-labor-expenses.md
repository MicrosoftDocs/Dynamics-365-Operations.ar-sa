---
title: تكوين التكاليف المعيارية للعمالة والمصروفات
description: يوضح هذا الإجراء كيفية إعداد التكاليف القياسية للعمالة والمصروفات لمشروع.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: b76956e9b1ce1a1e977aaa7c4974e73754e0d261
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845873"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="cac17-103">تكوين التكاليف المعيارية للعمالة والمصروفات</span><span class="sxs-lookup"><span data-stu-id="cac17-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cac17-104">يوضح هذا الإجراء كيفية إعداد التكاليف القياسية للعمالة والمصروفات لمشروع.</span><span class="sxs-lookup"><span data-stu-id="cac17-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="cac17-105">تستخدم هذه المهمة مجموعة بيانات USSI.</span><span class="sxs-lookup"><span data-stu-id="cac17-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="cac17-106">انتقل إلى إدارة المشروع‬ والمحاسبة‬ > الإعداد > الأسعار > سعر التكلفة (الساعة)‬.</span><span class="sxs-lookup"><span data-stu-id="cac17-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="cac17-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cac17-107">Click New.</span></span>
3. <span data-ttu-id="cac17-108">في الحقل "تاريخ السريان"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="cac17-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="cac17-109">في حقل "سعر التكلفة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="cac17-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="cac17-110">يمكنك إعداد سعر تكلفة قياسي لفئة المشروع أو يمكنك إعداد سعر تكلفة حسب رقم العامل أو رقم المشروع أو الفئة أو التاريخ أو أي مجموعة من هذه العناصر.</span><span class="sxs-lookup"><span data-stu-id="cac17-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="cac17-111">وسيكون سعر التكلفة الذي يتم تطبيقه سعر التكلفة الذي يتسم بأعلى مستوى من التفصيل.</span><span class="sxs-lookup"><span data-stu-id="cac17-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="cac17-112">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cac17-112">Click Save.</span></span>
6. <span data-ttu-id="cac17-113">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cac17-113">Close the page.</span></span>
7. <span data-ttu-id="cac17-114">انتقل إلى إدارة المشروع‬ والمحاسبة‬ > الإعداد > الأسعار > سعر المبيعات (الساعة)‬.</span><span class="sxs-lookup"><span data-stu-id="cac17-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="cac17-115">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cac17-115">Click New.</span></span>
9. <span data-ttu-id="cac17-116">في الحقل "تاريخ السريان"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="cac17-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="cac17-117">في الحقل "صالح لـ"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="cac17-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="cac17-118">في حقل "التسعير‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="cac17-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="cac17-119">يمكنك إعداد سعر المبيعات القياسي للحركات بالساعة أو لفئة المشروع.</span><span class="sxs-lookup"><span data-stu-id="cac17-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="cac17-120">ويمكنك أيضًا إعداد أسعار المبيعات حسب رقم العامل أو رقم المشروع أو الفئة أو تاريخ الحركة أو أية مجموعة من هذه العناصر.</span><span class="sxs-lookup"><span data-stu-id="cac17-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="cac17-121">ويكون سعر المبيعات الفعلي، الذي يتم استخدامه عندما يقوم العامل بإدخال حركة في دفتر يومية الساعات، سعر المبيعات بأعلى مستوى من التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="cac17-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="cac17-122">على سبيل المثال، عند إعداد سعر مبيعات عام وسعر مبيعات خاص بالعامل، يتم استخدام سعر المبيعات الخاص بالعامل.</span><span class="sxs-lookup"><span data-stu-id="cac17-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="cac17-123">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cac17-123">Click Save.</span></span>
13. <span data-ttu-id="cac17-124">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cac17-124">Close the page.</span></span>
14. <span data-ttu-id="cac17-125">انتقل إلى إدارة المشروع‬ والمحاسبة‬ > الإعداد > الأسعار > سعر التكلفة (المصروفات)‬.</span><span class="sxs-lookup"><span data-stu-id="cac17-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="cac17-126">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cac17-126">Click New.</span></span>
16. <span data-ttu-id="cac17-127">في الحقل "تاريخ السريان"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="cac17-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="cac17-128">في حقل "سعر التكلفة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="cac17-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="cac17-129">يمكن تعبئة حقول متعددة، ولكن هذا هو الحد الأدنى المطلوب لحفظ السجل.</span><span class="sxs-lookup"><span data-stu-id="cac17-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="cac17-130">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cac17-130">Click Save.</span></span>
19. <span data-ttu-id="cac17-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="cac17-131">Close the page.</span></span>
20. <span data-ttu-id="cac17-132">انتقل إلى إدارة المشروع‬ والمحاسبة‬ > الإعداد > الأسعار > سعر المبيعات (المصروفات)‬.</span><span class="sxs-lookup"><span data-stu-id="cac17-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="cac17-133">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="cac17-133">Click New.</span></span>
22. <span data-ttu-id="cac17-134">في الحقل "تاريخ السريان"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="cac17-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="cac17-135">في الحقل "صالح لـ"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="cac17-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="cac17-136">في حقل "التسعير‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="cac17-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="cac17-137">يعتبر سعر المبيعات الفعلي، الذي يتم تطبيقه عندما يقوم العامل بإدخال الحركات في دفتر يومية المصروفات، سعر المبيعات بأعلى مستوى من التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="cac17-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="cac17-138">على سبيل المثال، عند إعداد سعر مبيعات عام وسعر مبيعات خاص بالعامل، يتم استخدام سعر المبيعات الخاص بالعامل.</span><span class="sxs-lookup"><span data-stu-id="cac17-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="cac17-139">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="cac17-139">Click Save.</span></span>

