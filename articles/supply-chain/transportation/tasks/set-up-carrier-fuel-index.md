---
title: إعداد مؤشر وقود الناقل‬
description: يوضح هذا الدليل كيفية إنشاء منطقة مؤشر وقود ومؤشر وقود ومؤشر وقود الناقل.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFuelIndexRegion,TMSCarrierFuelIndexTable,TMSFuelIndex
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12ade30b63454dfd997aa47a62cde21b066140fa
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/29/2020
ms.locfileid: "4421834"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="1efa9-103">إعداد مؤشر وقود الناقل‬</span><span class="sxs-lookup"><span data-stu-id="1efa9-103">Set up a carrier fuel index</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1efa9-104">يوضح هذا الدليل كيفية إنشاء منطقة مؤشر وقود ومؤشر وقود ومؤشر وقود الناقل.</span><span class="sxs-lookup"><span data-stu-id="1efa9-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="1efa9-105">تحديد منطقة مؤشر الوقود المنطقة التي يجب تطبيق مؤشر الوقود عليها، ويحدد مؤشر الوقود سعر وقود لفترة معينة من الوقت.</span><span class="sxs-lookup"><span data-stu-id="1efa9-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="1efa9-106">لعكس التغيير في أسعار الوقود مع مرور الوقت، يمكنك إقران مؤشرات وقود متعددة مع ناقل.</span><span class="sxs-lookup"><span data-stu-id="1efa9-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="1efa9-107">عادة ما يتم تنفيذ هذه المهام من قِبل منسق نقل.</span><span class="sxs-lookup"><span data-stu-id="1efa9-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="1efa9-108">يمكنك استخدام هذا الإجراء في شركة بيانات العرض التوضيحي USMF أو باستخدام بياناتك الخاصة.</span><span class="sxs-lookup"><span data-stu-id="1efa9-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="1efa9-109">إنشاء منطقة مؤشر الوقود</span><span class="sxs-lookup"><span data-stu-id="1efa9-109">Create a fuel index region</span></span>
1. <span data-ttu-id="1efa9-110">انتقل إلى إدارة النقل > إعداد > مؤشرات الوقود‬ > مناطق مؤشر الوقود.</span><span class="sxs-lookup"><span data-stu-id="1efa9-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="1efa9-111">أولاً، يجب عليك إنشاء مناطق مختلفة، حيث تعمل وتحسب التكاليف الإضافية للوقود‬.</span><span class="sxs-lookup"><span data-stu-id="1efa9-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="1efa9-112">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="1efa9-112">Click New.</span></span>
3. <span data-ttu-id="1efa9-113">في الحقل "المنطقة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1efa9-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="1efa9-114">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1efa9-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="1efa9-115">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="1efa9-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="1efa9-116">إنشاء مؤشر وقود</span><span class="sxs-lookup"><span data-stu-id="1efa9-116">Create a fuel index</span></span>
1. <span data-ttu-id="1efa9-117">انتقل إلى إدارة النقل > إعداد > مؤشرات الوقود > مؤشرات الوقود.</span><span class="sxs-lookup"><span data-stu-id="1efa9-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="1efa9-118">بالنسبة إلى المناطق التي قمت بإعدادها، تحتاج إلى إدخال الأسعار الحالية للوقود.</span><span class="sxs-lookup"><span data-stu-id="1efa9-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="1efa9-119">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="1efa9-119">Click New.</span></span>
3. <span data-ttu-id="1efa9-120">في الحقل "المنطقة‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1efa9-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1efa9-121">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1efa9-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1efa9-122">في حقل "السعر لكل جالون‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1efa9-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="1efa9-123">في الحقل "‏‫تاريخ بدء السريان ووقته‬‬‬"، أدخل التاريخ والوقت.</span><span class="sxs-lookup"><span data-stu-id="1efa9-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="1efa9-124">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="1efa9-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="1efa9-125">إنشاء مؤشر وقود الناقل</span><span class="sxs-lookup"><span data-stu-id="1efa9-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="1efa9-126">انتقل إلى إدارة النقل > إعداد > مؤشرات الوقود > مؤشرات وقود الناقل.</span><span class="sxs-lookup"><span data-stu-id="1efa9-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="1efa9-127">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="1efa9-127">Click New.</span></span>
3. <span data-ttu-id="1efa9-128">في الحقل "مؤشر وقود الناقل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1efa9-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="1efa9-129">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1efa9-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1efa9-130">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="1efa9-130">Click New.</span></span>
6. <span data-ttu-id="1efa9-131">في الحقل "‏‫تاريخ بدء السريان ووقته‬‬‬"، أدخل التاريخ والوقت.</span><span class="sxs-lookup"><span data-stu-id="1efa9-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="1efa9-132">في الحقل "السعر لكل جالون من‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1efa9-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="1efa9-133">في هذا المثال، يمكنك تعيين الحقل "السعر لكل جالون من‬" إلى 1.95.</span><span class="sxs-lookup"><span data-stu-id="1efa9-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="1efa9-134">في الحقل "‏‫السعر لكل جالون إلى‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1efa9-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="1efa9-135">في هذا المثال، يمكنك تعيين الحقل "السعر لكل جالون إلى‬" إلى 2.</span><span class="sxs-lookup"><span data-stu-id="1efa9-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="1efa9-136">في الحقل "النسبة المئوية‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="1efa9-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="1efa9-137">في هذا المثال، يمكنك تعيين النسبة المئوية إلى 3.</span><span class="sxs-lookup"><span data-stu-id="1efa9-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="1efa9-138">في الحقل "العملة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="1efa9-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="1efa9-139">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="1efa9-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="1efa9-140">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="1efa9-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="1efa9-141">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="1efa9-141">Click Save.</span></span>

