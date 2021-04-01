---
title: تقليل إهلاك الرصيد بعد التقسيم
description: يصف هذا الموضوع الأسلوب المستخدم في الأصول الثابتة لحساب الإهلاك بعد تقسيم أحد الأصول باستخدام أسلوب تقليل الرصيد.
author: moaamer
manager: Ann Beebe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f276f49e5b1bc2814dc851f1ad4204a151d86c43
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222373"
---
# <a name="reduce-balance-depreciation-after-a-split"></a><span data-ttu-id="5072c-103">تقليل إهلاك الرصيد بعد التقسيم</span><span class="sxs-lookup"><span data-stu-id="5072c-103">Reduce balance depreciation after a split</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5072c-104">يصف هذا الموضوع الأسلوب المستخدم في الأصول الثابتة لحساب الإهلاك بعد تقسيم أحد الأصول إلى أصل آخر باستخدام أسلوب تقليل الرصيد.</span><span class="sxs-lookup"><span data-stu-id="5072c-104">This topic describes the method that is used in Fixed assets to calculate depreciation after an asset is split to another asset by using the reduce balance method.</span></span> <span data-ttu-id="5072c-105">وتكون سنة الإهلاك التي يتم تكوينها في دفتر الأصول هي السنه المالية.</span><span class="sxs-lookup"><span data-stu-id="5072c-105">The depreciation year that is configured in the asset book is the fiscal year.</span></span> <span data-ttu-id="5072c-106">لمزيد من المعلومات، راجع [تقليل إهلاك الرصيد](reduce-balance-depreciation.md) و [تقسيم الأصل الثابت](tasks/split-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="5072c-106">For more information, see [Reduce balance depreciation](reduce-balance-depreciation.md) and [Split a fixed asset](tasks/split-fixed-asset.md).</span></span>

<span data-ttu-id="5072c-107">إذا قمت بتقسيم أصل ثابت خلال فترة مالية بعد فترة امتلاك الأصل، سيقوم إهلاك الرصيد المخفض بحساب صافي القيمة الدفترية للأصل (NBV) للسنة السابقة.</span><span class="sxs-lookup"><span data-stu-id="5072c-107">If you split a fixed asset during a fiscal period that is later than the period when the asset was acquired, the reduced balance depreciation will account for the asset's net book value (NBV) for the previous year.</span></span> <span data-ttu-id="5072c-108">كما سيقوم أيضًا بحساب الامتلاك وحركات تسوية الإهلاك التي تم إنشاؤها من الحركة التي تقوم بتقسيم الأصل.</span><span class="sxs-lookup"><span data-stu-id="5072c-108">It will also account for the acquisition and depreciation adjustment transactions that were generated from the transaction that split the asset.</span></span> <span data-ttu-id="5072c-109">ويفترض هذا السلوك أنه قد تم امتلاك الأصل في سنة مالية واحدة وتم تقسيمه في سنة مالية لاحقة.</span><span class="sxs-lookup"><span data-stu-id="5072c-109">This behavior assumes that the asset was acquired in one fiscal year and split in a later fiscal year.</span></span> <span data-ttu-id="5072c-110">ويعكس المبلغ الذي يجب إهلاكه للأصل الأصلي بعد التقسيم NBV للأصل قبل تقسيم الأصل، وحركة تسوية الإهلاك والامتلاك التي تم ترحيلها للتقسيم.</span><span class="sxs-lookup"><span data-stu-id="5072c-110">The amount that must be depreciated for the original asset after the split reflects the asset's NBV before the asset was split, and the acquisition and depreciation adjustment transaction that was posted for the split.</span></span>

<span data-ttu-id="5072c-111">على سبيل المثال، تكون الحالات التالية سارية المفعول:</span><span class="sxs-lookup"><span data-stu-id="5072c-111">For example, the following conditions are in effect:</span></span>

- <span data-ttu-id="5072c-112">تتراوح الفترة المالية من 30 يونيو إلى 1 يوليو.</span><span class="sxs-lookup"><span data-stu-id="5072c-112">The fiscal period is from June 30 to July 1.</span></span>
- <span data-ttu-id="5072c-113">النسبة المئوية لتقليل الرصيد هي 18%، ويتم امتلاك أحد الأصول في يونيو 2019 بسعر امتلاك بقيمة 10.000 دولار.</span><span class="sxs-lookup"><span data-stu-id="5072c-113">The reducing balance percentage is 18 percent, and an asset is acquired in June 2019 at an acquisition price of $10,000.</span></span>
- <span data-ttu-id="5072c-114">ويساوي إهلاك السنه المالية الأولى 18.000 دولار، ويساوي الإهلاك الشهري 150 دولار، ويتم إهلاك الأصل حتى نوفمبر، 2019، بمقدار 738.75 دولار.</span><span class="sxs-lookup"><span data-stu-id="5072c-114">The depreciation of the first fiscal year equals $18,000, the monthly depreciation equals $150, and the asset is then depreciated until November 2019, in the amount of $738.75.</span></span>
- <span data-ttu-id="5072c-115">في نوفمبر 2019، يتم تقسيم 80 بالمائة من الأصل إلى أصل ثابت آخر.</span><span class="sxs-lookup"><span data-stu-id="5072c-115">In November 2019, 80 percent of the asset is split to another fixed asset.</span></span>

<span data-ttu-id="5072c-116">[![تقليل إهلاك الرصيد بعد التقسيم](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span><span class="sxs-lookup"><span data-stu-id="5072c-116">[![Reduce balance depreciation after a split](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span></span>

<span data-ttu-id="5072c-117">المبلغ المراد إهلاكه للأصل الأصلي يكون بقيم 1.822.25 دولار.</span><span class="sxs-lookup"><span data-stu-id="5072c-117">The amount to depreciate for the original asset is $1,822.25.</span></span> <span data-ttu-id="5072c-118">ويساوي هذا المبلغ صافي القيمة الدفترية قبل ترحيل حركة التقسيم (9.111.25 دولار)، بالإضافة إلى تسوية الامتلاك الذي يتم إنشاؤه أثناء ترحيل الحركة المقسمة (-8.000 دولار)، بالإضافة إلى تسوية الإهلاك التي يتم إنشاؤها خلال حركه التقسيم (711 دولار).</span><span class="sxs-lookup"><span data-stu-id="5072c-118">This amount equals the NBV before the split transaction is posted ($9,111.25), plus the acquisition adjustment that is generated during posting of the split transaction (-$8,000), plus the depreciation adjustment that is generated during the split transaction ($711).</span></span> <span data-ttu-id="5072c-119">وبالتالي، فإن إهلاك السنة الثانية هو (1,822.25 × 18%) ÷ 12 = 27.33 دولار.</span><span class="sxs-lookup"><span data-stu-id="5072c-119">Therefore, the depreciation for the second year is (1,822.25 × 18 percent) ÷ 12 = $27.33.</span></span>

<span data-ttu-id="5072c-120">المبلغ الذي يتم إهلاكه للأصل الثابت الجديد في السنه الأولى هو (8.000 × 18%) ÷ 12 = 120دولار.</span><span class="sxs-lookup"><span data-stu-id="5072c-120">The amount to depreciate for the new fixed asset in the first year is (8,000 × 18 percent) ÷ 12 = $120.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]