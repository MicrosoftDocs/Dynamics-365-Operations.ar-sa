---
title: "المبلغ التقريبي لعمليات حساب الإهلاك"
description: "تتناول هذه المقالة حقل \"تقريب الإهلاك\" الموجود في صفحات إعداد الدفتر."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 7721e46a72e0f8133ed67c597a066a97ffd61669
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---

# <a name="round-off-amount-for-depreciation-calculations"></a><span data-ttu-id="f7e01-103">المبلغ التقريبي لعمليات حساب الإهلاك</span><span class="sxs-lookup"><span data-stu-id="f7e01-103">Round-off amount for depreciation calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7e01-104">تتناول هذه المقالة حقل "تقريب الإهلاك" الموجود في صفحات إعداد الدفتر.</span><span class="sxs-lookup"><span data-stu-id="f7e01-104">This article discusses the Round-off depreciation field that is found on the Book setup pages.</span></span>

<span data-ttu-id="f7e01-105">‏‫يتم تعيين مبالغ تقريب الإهلاك لكل دفتر.</span><span class="sxs-lookup"><span data-stu-id="f7e01-105">Round-off depreciation amounts are set for each book.</span></span> <span data-ttu-id="f7e01-106">وتُستخدم مبالغ الإهلاك التقريبية في ملف تعريف إهلاك الأصول الثابتة، الذي يوضح الإهلاك المستقبلي وقيمة الأصل الثابت، وكذلك في مقترحات الإهلاك.‬</span><span class="sxs-lookup"><span data-stu-id="f7e01-106">Round-off depreciation amounts are used in the fixed asset depreciation profile that shows the future depreciation and value of the fixed asset, and also in depreciation proposals.</span></span> <span data-ttu-id="f7e01-107">أدخل الحد الأدنى لمبلغ إهلاك المسموح به للدفتر.</span><span class="sxs-lookup"><span data-stu-id="f7e01-107">Enter the lowest depreciation amount that is allowed for the book.</span></span> 

<span data-ttu-id="f7e01-108">وبغض النظر عن التقريب الذي تم إعداده، يتم تقريب مبلغ الإهلاك في فترة الإهلاك الأخيرة.</span><span class="sxs-lookup"><span data-stu-id="f7e01-108">Regardless of the rounding that is set up, the depreciation amount in the last depreciation period isn't rounded.</span></span> <span data-ttu-id="f7e01-109">وفي نهاية فترة الإهلاك الأخيرة، يجب أن تكون قيمة الأصل الثابت 0 (صفر) أو قيمة الخردة، إذا تم استخدام قيمة الخردة.</span><span class="sxs-lookup"><span data-stu-id="f7e01-109">At the end of the last depreciation period, the value of the fixed asset must be 0 (zero) or the scrap value, if scrap value is used.</span></span>

### <a name="example"></a><span data-ttu-id="f7e01-110">مثال</span><span class="sxs-lookup"><span data-stu-id="f7e01-110">Example</span></span>

<span data-ttu-id="f7e01-111">يتم حساب الإهلاك بدون أي تقريب على شكل 2,444.44.</span><span class="sxs-lookup"><span data-stu-id="f7e01-111">Depreciation without rounding is calculated as 2,444.44.</span></span> <span data-ttu-id="f7e01-112">وكما يُظهر الجدول التالي، تختلف المبالغ المقترحة، استنادًا إلى كيفية إعداد التقريب.</span><span class="sxs-lookup"><span data-stu-id="f7e01-112">As the following table shows, the amounts that are suggested vary, depending on how rounding is set up.</span></span>

| <span data-ttu-id="f7e01-113">أسلوب التقريب</span><span class="sxs-lookup"><span data-stu-id="f7e01-113">Rounding method</span></span> | <span data-ttu-id="f7e01-114">مبلغ الإهلاك</span><span class="sxs-lookup"><span data-stu-id="f7e01-114">Depreciation amount</span></span> |
|-----------------|---------------------|
| <span data-ttu-id="f7e01-115">التقريب 0.1</span><span class="sxs-lookup"><span data-stu-id="f7e01-115">Rounding 0.1</span></span>    | <span data-ttu-id="f7e01-116">2,444.40</span><span class="sxs-lookup"><span data-stu-id="f7e01-116">2,444.40</span></span>            |
| <span data-ttu-id="f7e01-117">التقريب 1.00</span><span class="sxs-lookup"><span data-stu-id="f7e01-117">Rounding 1.00</span></span>   | <span data-ttu-id="f7e01-118">2,444.00</span><span class="sxs-lookup"><span data-stu-id="f7e01-118">2,444.00</span></span>            |
| <span data-ttu-id="f7e01-119">التقريب 10.00</span><span class="sxs-lookup"><span data-stu-id="f7e01-119">Rounding 10.00</span></span>  | <span data-ttu-id="f7e01-120">2,440.00</span><span class="sxs-lookup"><span data-stu-id="f7e01-120">2,440.00</span></span>            |
| <span data-ttu-id="f7e01-121">التقريب 100.00</span><span class="sxs-lookup"><span data-stu-id="f7e01-121">Rounding 100.00</span></span> | <span data-ttu-id="f7e01-122">2,400.00</span><span class="sxs-lookup"><span data-stu-id="f7e01-122">2,400.00</span></span>            |






