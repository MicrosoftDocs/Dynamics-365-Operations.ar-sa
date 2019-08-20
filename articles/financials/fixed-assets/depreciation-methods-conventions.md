---
title: أساليب الإهلاك والقواعد
description: توفر هذه المقالة نظرة عامة حول قواعد الإهلاك وطرق الإهلاك المعتمدة من قبل Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a7bce93c955ce64da129bdb1a3e9905279838c3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840615"
---
# <a name="depreciation-methods-and-conventions"></a><span data-ttu-id="39ec9-103">طرق الإهلاك والقواعد</span><span class="sxs-lookup"><span data-stu-id="39ec9-103">Depreciation methods and conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39ec9-104">توفر هذه المقالة نظرة عامة حول قواعد الإهلاك وطرق الإهلاك المعتمدة من قبل Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="39ec9-104">This article provides an overview of the depreciation conventions and depreciation methods that are supported by Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="39ec9-105">يُمكنك تحديد أساليب وقواعد إهلاك متعددة.</span><span class="sxs-lookup"><span data-stu-id="39ec9-105">You can select various depreciation methods and conventions.</span></span> <span data-ttu-id="39ec9-106">تهدف هذه الطرق إلى تخصيص القيمة الممكن إهلاكها للأصل الثابت إلى فترات مالية.</span><span class="sxs-lookup"><span data-stu-id="39ec9-106">The purpose of the methods is to allocate the depreciable value of the fixed asset into fiscal periods.</span></span> <span data-ttu-id="39ec9-107">والقيمة الممكن إهلاكها للأصل الثابت هي عبارة عن سعر الامتلاك الذي يتم خصم قيمة الخردة منه، إن وُجدت.</span><span class="sxs-lookup"><span data-stu-id="39ec9-107">The depreciable value of the fixed asset is the acquisition price, reduced by a scrap value, if any.</span></span> 

<span data-ttu-id="39ec9-108">إذا كنت تستخدم قواعد الإهلاك وقمت بتعديل تاريخ تشغيل آخر إهلاك لأحد الأصول، والذي يؤدي إلى تخطي بعض عمليات الإهلاك، فقد يزيد إهلاك العام الأخير أو يقل عما هو مُتوقع.</span><span class="sxs-lookup"><span data-stu-id="39ec9-108">If you are using depreciation conventions and you modify the last depreciation run date for an asset, which then causes some depreciations to be skipped, the depreciation for the last year might be more than or less than is expected.</span></span> <span data-ttu-id="39ec9-109">ويتم تعديل الإهلاك بعدد فترات الإهلاك التي تأثرت بتعديل آخر تاريخ لتشغيل الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="39ec9-109">The depreciation is adjusted by the number of depreciation periods affected by the modification of the last depreciation run date.</span></span>

<span data-ttu-id="39ec9-110">على سبيل المثال، إذا كنت تستخدم قاعدة الإهلاك نصف السنوية على مدار ثلاث سنوات، فسيقع الإهلاك عادةً على مدار 3 سنوات ونصف.</span><span class="sxs-lookup"><span data-stu-id="39ec9-110">For example, if you are using the Half year depreciation convention over three years, depreciation ordinarily occurs over 3 1/2 years.</span></span> <span data-ttu-id="39ec9-111">وإذا قمت بتغيير آخر تاريخ لتشغيل الإهلاك خلال مدة 3 سنوات ونصف، فسيخرج العام الأخير للإهلاك عن عدد الفترات المتأثرة.</span><span class="sxs-lookup"><span data-stu-id="39ec9-111">If you change the last depreciation run date during the 3 1/2 years, the last year of depreciation moves out the number of periods affected.</span></span> <span data-ttu-id="39ec9-112">وفي حالة تقديم التاريخ بثلاثة أشهر، فسيشتمل العام الأخير على تسعة أشهر تستحق الإهلاك، في حين أنه يكون هناك عادةً ستة أشهر تستحق الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="39ec9-112">If you move the date by three months, the last year will have nine months’ worth of depreciation, when ordinarily there would be six months’ worth of depreciation.</span></span>

<span data-ttu-id="39ec9-113">ويُمكنك الاختيار من بين قواعد الإهلاك التالية.</span><span class="sxs-lookup"><span data-stu-id="39ec9-113">You can select from the following depreciation conventions.</span></span>


-   <span data-ttu-id="39ec9-114">نصف السنة</span><span class="sxs-lookup"><span data-stu-id="39ec9-114">Half year</span></span>
-   <span data-ttu-id="39ec9-115">شهر كامل</span><span class="sxs-lookup"><span data-stu-id="39ec9-115">Full month</span></span>
-   <span data-ttu-id="39ec9-116">منتصف الربع</span><span class="sxs-lookup"><span data-stu-id="39ec9-116">Mid quarter</span></span>
-   <span data-ttu-id="39ec9-117">منتصف الشهر (أول الشهر)</span><span class="sxs-lookup"><span data-stu-id="39ec9-117">Mid month (1st of month)</span></span>
-   <span data-ttu-id="39ec9-118">منتصف الشهر(الخامس عشر من الشهر)</span><span class="sxs-lookup"><span data-stu-id="39ec9-118">Mid month (15th of month)</span></span>
-   <span data-ttu-id="39ec9-119">نصف السنة (بداية السنة)</span><span class="sxs-lookup"><span data-stu-id="39ec9-119">Half year (start of year)</span></span>
-   <span data-ttu-id="39ec9-120">نصف سنة (السنة التالية)</span><span class="sxs-lookup"><span data-stu-id="39ec9-120">Half year (next year)</span></span>

<span data-ttu-id="39ec9-121">يمكنك التحديد من طرق الإهلاك التالية.</span><span class="sxs-lookup"><span data-stu-id="39ec9-121">You can select from the following depreciation methods.</span></span>
-   <span data-ttu-id="39ec9-122">مدة خدمة القسط الثابت</span><span class="sxs-lookup"><span data-stu-id="39ec9-122">Straight line service life</span></span>
-   <span data-ttu-id="39ec9-123">تقليل الرصيد</span><span class="sxs-lookup"><span data-stu-id="39ec9-123">Reducing balance</span></span>
-   <span data-ttu-id="39ec9-124">يدوي</span><span class="sxs-lookup"><span data-stu-id="39ec9-124">Manual</span></span>
-   <span data-ttu-id="39ec9-125">المعامل</span><span class="sxs-lookup"><span data-stu-id="39ec9-125">Factor</span></span>
-   <span data-ttu-id="39ec9-126">الاستهلاك</span><span class="sxs-lookup"><span data-stu-id="39ec9-126">Consumption</span></span>
-   <span data-ttu-id="39ec9-127">المتبقي من مدة خدمة القسط الثابت</span><span class="sxs-lookup"><span data-stu-id="39ec9-127">Straight line life remaining</span></span>
-   <span data-ttu-id="39ec9-128">تقليل الرصيد بنسبة 200%</span><span class="sxs-lookup"><span data-stu-id="39ec9-128">200% reducing balance</span></span>
-   <span data-ttu-id="39ec9-129">تقليل الرصيد بنسبة 175%</span><span class="sxs-lookup"><span data-stu-id="39ec9-129">175% reducing balance</span></span>
-   <span data-ttu-id="39ec9-130">تقليل الرصيد بنسبة 150%</span><span class="sxs-lookup"><span data-stu-id="39ec9-130">150% reducing balance</span></span>
-   <span data-ttu-id="39ec9-131">تقليل الرصيد بنسبة 125%</span><span class="sxs-lookup"><span data-stu-id="39ec9-131">125% reducing balance</span></span>





<a name="additional-resources"></a><span data-ttu-id="39ec9-132">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="39ec9-132">Additional resources</span></span>
--------

[<span data-ttu-id="39ec9-133">إهلاك الأصل الثابت</span><span class="sxs-lookup"><span data-stu-id="39ec9-133">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)

[<span data-ttu-id="39ec9-134">إهلاك مدة خدمة القسط الثابت</span><span class="sxs-lookup"><span data-stu-id="39ec9-134">Straight line service life depreciation</span></span>](Straight-line-service-life-depreciation.md)

[<span data-ttu-id="39ec9-135">إهلاك القسط المتناقص</span><span class="sxs-lookup"><span data-stu-id="39ec9-135">Reducing balance depreciation</span></span>](reduce-balance-depreciation.md)

[<span data-ttu-id="39ec9-136">الإهلاك اليدوي</span><span class="sxs-lookup"><span data-stu-id="39ec9-136">Manual depreciation</span></span>](manual-depreciation.md)

[<span data-ttu-id="39ec9-137">إهلاك العامل</span><span class="sxs-lookup"><span data-stu-id="39ec9-137">Factor depreciation</span></span>](factor-depreciation.md)

[<span data-ttu-id="39ec9-138">إهلاك الاستهلاك</span><span class="sxs-lookup"><span data-stu-id="39ec9-138">Consumption depreciation</span></span>](consumption-depreciation.md)

[<span data-ttu-id="39ec9-139">إهلاك المتبقي من مدة خدمة القسط الثابت</span><span class="sxs-lookup"><span data-stu-id="39ec9-139">Straight line life remaining depreciation</span></span>](straight-line-life-remaining-depreciation.md)

[<span data-ttu-id="39ec9-140">إهلاك الرصيد المتناقص بنسبة 125 بالمائة</span><span class="sxs-lookup"><span data-stu-id="39ec9-140">125 percent reducing balance depreciation</span></span>](125-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="39ec9-141">إهلاك الرصيد المتناقص بنسبة 150 بالمائة</span><span class="sxs-lookup"><span data-stu-id="39ec9-141">150 percent reducing balance depreciation</span></span>](150-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="39ec9-142">إهلاك الرصيد المتناقص بنسبة 175 بالمائة</span><span class="sxs-lookup"><span data-stu-id="39ec9-142">175 percent reducing balance depreciation</span></span>](175-percent-reducing-balance-depreciation.md)

[<span data-ttu-id="39ec9-143">إهلاك الرصيد المتناقص بنسبة 200 بالمائة</span><span class="sxs-lookup"><span data-stu-id="39ec9-143">200 percent reducing balance depreciation</span></span>](200-percent-reducing-balance-depreciation.md)



