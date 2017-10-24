---
title: "المبلغ التقريبي لعمليات حساب الإهلاك"
description: "تتناول هذه المقالة حقل \"تقريب الإهلاك\" الموجود في صفحات إعداد الدفتر."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ae5c24633a9ce4ce43e213581eb64c8548eecf5d
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="c4b8a-103">المبلغ التقريبي لعمليات حساب الإهلاك</span><span class="sxs-lookup"><span data-stu-id="c4b8a-103">Round-off amount for depreciation calculations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c4b8a-104">تتناول هذه المقالة حقل "تقريب الإهلاك" الموجود في صفحات إعداد الدفتر.</span><span class="sxs-lookup"><span data-stu-id="c4b8a-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="c4b8a-105">‏‫يتم تعيين مبالغ تقريب الإهلاك لكل دفتر.</span><span class="sxs-lookup"><span data-stu-id="c4b8a-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="c4b8a-106">وتُستخدم مبالغ الإهلاك التقريبية في ملف تعريف إهلاك الأصول الثابتة، الذي يوضح الإهلاك المستقبلي وقيمة الأصل الثابت، وكذلك في مقترحات الإهلاك.‬</span><span class="sxs-lookup"><span data-stu-id="c4b8a-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="c4b8a-107">أدخل الحد الأدنى لمبلغ إهلاك المسموح به للدفتر.</span><span class="sxs-lookup"><span data-stu-id="c4b8a-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="c4b8a-108">وبغض النظر عن التقريب الذي تم إعداده، يتم تقريب مبلغ الإهلاك في فترة الإهلاك الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="c4b8a-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="c4b8a-109">وفي نهاية فترة الإهلاك الأخيرة، يجب أن تكون قيمة الأصل الثابت 0 (صفر) أو قيمة الخردة، إذا تم استخدام قيمة الخردة.</span><span class="sxs-lookup"><span data-stu-id="c4b8a-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="c4b8a-110">مثال</span><span class="sxs-lookup"><span data-stu-id="c4b8a-110">Example</span></span>

<span data-ttu-id="c4b8a-111">يتم حساب الإهلاك بدون أي تقريب على شكل 2,444.44.</span><span class="sxs-lookup"><span data-stu-id="c4b8a-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="c4b8a-112">وكما يُظهر الجدول التالي، تختلف المبالغ المقترحة، استنادًا إلى كيفية إعداد التقريب.</span><span class="sxs-lookup"><span data-stu-id="c4b8a-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="c4b8a-113">أسلوب التقريب</span><span class="sxs-lookup"><span data-stu-id="c4b8a-113">Rounding method</span></span> | <span data-ttu-id="c4b8a-114">مبلغ الإهلاك</span><span class="sxs-lookup"><span data-stu-id="c4b8a-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="c4b8a-115">التقريب 0.1</span><span class="sxs-lookup"><span data-stu-id="c4b8a-115">Rounding 0.1</span></span>    | <span data-ttu-id="c4b8a-116">2,444.40</span><span class="sxs-lookup"><span data-stu-id="c4b8a-116">2,444.40</span></span>            |
| <span data-ttu-id="c4b8a-117">التقريب 1.00</span><span class="sxs-lookup"><span data-stu-id="c4b8a-117">Rounding 1.00</span></span>   | <span data-ttu-id="c4b8a-118">2,444.00</span><span class="sxs-lookup"><span data-stu-id="c4b8a-118">2,444.00</span></span>            |
| <span data-ttu-id="c4b8a-119">التقريب 10.00</span><span class="sxs-lookup"><span data-stu-id="c4b8a-119">Rounding 10.00</span></span>  | <span data-ttu-id="c4b8a-120">2,440.00</span><span class="sxs-lookup"><span data-stu-id="c4b8a-120">2,440.00</span></span>            |
| <span data-ttu-id="c4b8a-121">التقريب 100.00</span><span class="sxs-lookup"><span data-stu-id="c4b8a-121">Rounding 100.00</span></span> | <span data-ttu-id="c4b8a-122">2,400.00</span><span class="sxs-lookup"><span data-stu-id="c4b8a-122">2,400.00</span></span>            |






