---
title: التخلص من أصل ثابت كخردة
description: يصف الموضوع عملية إزالة الحركات الخاصة بأصل ثابت تم التخلص منه كخردة.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 371cc2efa64916698da8e4230825c3c949920698
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975234"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a><span data-ttu-id="3b254-103">التخلص من أصل ثابت كخردة</span><span class="sxs-lookup"><span data-stu-id="3b254-103">Dispose of a fixed asset as scrap</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b254-104">يصف الموضوع عملية إزالة الحركات الخاصة بأصل ثابت تم التخلص منه كخردة.</span><span class="sxs-lookup"><span data-stu-id="3b254-104">The topic describes the process of eliminating transactions for a fixed asset that was disposed of as scrap.</span></span> <span data-ttu-id="3b254-105">تشتمل أنواع الحركات التي يمكن إزالتها على حركات الاستحواذ على أصل والإهلاك التراكمي وحركات الأصول الثابتة الأخرى.</span><span class="sxs-lookup"><span data-stu-id="3b254-105">The transaction types that can be eliminated include an asset's acquisition and accumulated depreciation transactions and other fixed asset transactions.</span></span> <span data-ttu-id="3b254-106">تؤثر إزالة هذه الحركات على حسابات الميزانية العمومية، مثل تسويه الاستحواذ وتسوية الإهلاك وإعادة التقييم وحسابات رفع القيم وخفض القيم.</span><span class="sxs-lookup"><span data-stu-id="3b254-106">Elimination of these transactions affects balance sheet accounts, such as acquisition adjustment, depreciation adjustment, revaluation, write-up, and write-down accounts.</span></span>

| <span data-ttu-id="3b254-107">الحركة</span><span class="sxs-lookup"><span data-stu-id="3b254-107">Transaction</span></span>                                         | <span data-ttu-id="3b254-108">مدين</span><span class="sxs-lookup"><span data-stu-id="3b254-108">Debit (Dr.)</span></span> | <span data-ttu-id="3b254-109">دائن</span><span class="sxs-lookup"><span data-stu-id="3b254-109">Credit (Cr.)</span></span> |
|-----------------------------------------------------|-------------|--------------|
| <span data-ttu-id="3b254-110">مدين الإهلاك التراكمي</span><span class="sxs-lookup"><span data-stu-id="3b254-110">Dr. Accumulated depreciation</span></span>                        | <span data-ttu-id="3b254-111">س</span><span class="sxs-lookup"><span data-stu-id="3b254-111">X</span></span>           |              |
| <span data-ttu-id="3b254-112">دائن أرباح/خسائر الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="3b254-112">Cr. Fixed assets gain/loss</span></span>                          |             | <span data-ttu-id="3b254-113">س</span><span class="sxs-lookup"><span data-stu-id="3b254-113">X</span></span>            |
| <span data-ttu-id="3b254-114">مدين أرباح/خسائر الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="3b254-114">Dr. Fixed assets gain/loss</span></span>                          | <span data-ttu-id="3b254-115">س</span><span class="sxs-lookup"><span data-stu-id="3b254-115">X</span></span>           |              |
| <span data-ttu-id="3b254-116">دائن حساب الاستحواذ على الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="3b254-116">Cr. Fixed asset acquisition account</span></span>                 |             | <span data-ttu-id="3b254-117">س</span><span class="sxs-lookup"><span data-stu-id="3b254-117">X</span></span>            |
| <span data-ttu-id="3b254-118">مدين أرباح/خسائر الأصول الثابتة (صافي القيمة الدفترية \[NBV\])</span><span class="sxs-lookup"><span data-stu-id="3b254-118">Dr. Fixed assets gain/loss (net book value \[NBV\])</span></span> | <span data-ttu-id="3b254-119">س</span><span class="sxs-lookup"><span data-stu-id="3b254-119">X</span></span>           |              |
| <span data-ttu-id="3b254-120">دائن أرباح/خسائر الأصول الثابتة (NBV)</span><span class="sxs-lookup"><span data-stu-id="3b254-120">Cr. Fixed assets gain/loss (NBV)</span></span>                    |             | <span data-ttu-id="3b254-121">س</span><span class="sxs-lookup"><span data-stu-id="3b254-121">X</span></span>            |

> [!NOTE]
> <span data-ttu-id="3b254-122">ننصحك بالتعاون عن كثب مع المدير المالي (CFO) أو المراقب المالي في شركتك لتحديد الحسابات الصحيحة التي يجب استخدامها لكل نوع حركة، وكذلك للتحقق من أن عملية التخلص والحركات التي تقوم بإنشائها تحدّث هذه الحسابات بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="3b254-122">We recommend that you work closely with your company's chief financial officer (CFO) or controller to identify the correct accounts that should be used for each transaction type, and also to verify that the disposal process and the transactions that it generates update those accounts correctly.</span></span>

<span data-ttu-id="3b254-123">قبل التخلص من أصل ثابت كخردة، يجب عليك إنشاء حسابات دفتر الأستاذ المرتبطة بقيمه الاستحواذ وإهلاك السنة الحالية وإهلاك السنوات السابقة وصافي القيمة الدفترية للأصل.</span><span class="sxs-lookup"><span data-stu-id="3b254-123">Before you dispose of a fixed asset as scrap, you must create ledger accounts that are associated with the asset's acquisition value, depreciation for the current year, depreciation for previous years, and the asset's NBV.</span></span> <span data-ttu-id="3b254-124">يتم إدراج أنواع حركات الأصول الثابتة في صفحة **ملف تعريف ترحيل الأصول الثابتة‬** .</span><span class="sxs-lookup"><span data-stu-id="3b254-124">The fixed asset transaction types are listed on the **Fixed assets posting profile** page.</span></span> <span data-ttu-id="3b254-125">انتقل إلى **الأصول الثابتة \> الإعداد \> ملفات تعريف ترحيل الأصول الثابتة** ، ثم على علامة التبويب السريعة **التخلص‬** ، حدد **خردة** في الحقل فوق الشبكة.</span><span class="sxs-lookup"><span data-stu-id="3b254-125">Go to **Fixed assets \> Setup \> Fixed asset posting profiles** , and then, on the **Disposal** FastTab, select **Scrap** in the field above the grid.</span></span> <span data-ttu-id="3b254-126">يبين الشكل التوضيحي التالي قائمة بأنواع حركات الأصول الثابتة في صفحة **ملفات تعريف ترحيل الأصول الثابتة** .</span><span class="sxs-lookup"><span data-stu-id="3b254-126">The following illustration shows the list of fixed asset transaction types on the **Fixed asset posting profiles** page.</span></span>


<span data-ttu-id="3b254-127">[![التخلص من أصل كخردة، الشكل التوضيحي 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span><span class="sxs-lookup"><span data-stu-id="3b254-127">[![Disposing of an asset as scap, Fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span></span>

<span data-ttu-id="3b254-128">فيما يتعلق بالمثال التالي، تم الاستحواذ على أصل ثابت في 1 يناير 2018، وسيتم تخريده في 31 مارس 2019.</span><span class="sxs-lookup"><span data-stu-id="3b254-128">For the following example, a fixed asset was acquired on January 1, 2018, and it will be scrapped on March 31, 2019.</span></span>

- <span data-ttu-id="3b254-129">**سعر الاستحواذ:** 24,000.00 دولار أمريكي</span><span class="sxs-lookup"><span data-stu-id="3b254-129">**Acquisition price:** 24,000.00 US dollars (USD)</span></span>
- <span data-ttu-id="3b254-130">**مدة الخدمة:** سنتان</span><span class="sxs-lookup"><span data-stu-id="3b254-130">**Service life:** Two years</span></span>
- <span data-ttu-id="3b254-131">**أسلوب الإهلاك:** مدة خدمة ثابتة</span><span class="sxs-lookup"><span data-stu-id="3b254-131">**Depreciation method:** Straight line service life</span></span>
- <span data-ttu-id="3b254-132">**مبلغ الإهلاك:** 1,000.00 دولار أمريكي في الشهر</span><span class="sxs-lookup"><span data-stu-id="3b254-132">**Depreciation amount:** 1,000.00 USD per month</span></span>

<span data-ttu-id="3b254-133">يتم حساب صافي القيمة الدفترية باستخدام الصيغة التالية:</span><span class="sxs-lookup"><span data-stu-id="3b254-133">The NBV of a fixed asset is calculated by using the following formula:</span></span>

<span data-ttu-id="3b254-134">صافي القيمة الدفترية = سعر الاستحواذ – الإهلاك</span><span class="sxs-lookup"><span data-stu-id="3b254-134">Net book value = Acquisition price – Depreciation</span></span>

<span data-ttu-id="3b254-135">في هذا المثال، تم الاستحواذ على الأصل الثابت وتم إهلاكه لمدة 15 شهرًا، من 2018 يناير إلى مارس 2019.</span><span class="sxs-lookup"><span data-stu-id="3b254-135">In this example, the fixed asset was acquired and was depreciated for 15 months, from January 2018 through March 2019.</span></span> <span data-ttu-id="3b254-136">وبالتالي، فإن صافي القيمة الدفترية للأصل هي 9,000.00 دولار أمريكي (24,000.00 دولار أمريكي – 15,000.00 دولار أمريكي).</span><span class="sxs-lookup"><span data-stu-id="3b254-136">Therefore, the asset's NBV is 9,000.00 USD (24,000.00 USD – 15,000.00 USD).</span></span>

<span data-ttu-id="3b254-137">[![مثال عن إهلاك أصل ثابت](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span><span class="sxs-lookup"><span data-stu-id="3b254-137">[![Fixed asset depreciation example](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span></span>


<span data-ttu-id="3b254-138">لإنشاء دفتر يومية التخلص، انتقل إلى **الأصول‏‎ الثابتة \> إدخالات دفتر اليومية \> دفتر يومية الأصول‏‎ الثابتة** ، ثم حدد **البنود** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="3b254-138">To create a disposal journal, go to **Fixed assets \> Journal entries \> Fixed assets journal** , and then, on the Action Pane, select **Lines** .</span></span> <span data-ttu-id="3b254-139">حدد **التخلص - الخردة‬** ، ثم حدد معرّف الأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="3b254-139">Select **Disposal – scrap** , and then select a fixed asset ID.</span></span> <span data-ttu-id="3b254-140">للتخلص من الأصل بشكل تام، لا تدخل قيمة سواء في الحقل **مدين** أو **دائن** .</span><span class="sxs-lookup"><span data-stu-id="3b254-140">To fully dispose of the asset, don't enter a value in either the **Debit** field or the **Credit** field.</span></span>

<span data-ttu-id="3b254-141">[![دفتر يومية الأصول الثابتة](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span><span class="sxs-lookup"><span data-stu-id="3b254-141">[![Fixed assets journal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span></span>

<span data-ttu-id="3b254-142">تقوم حركة التخلص (الخردة) الذي تم على الأصل الثابت بتغيير قيم الحقول لدفتر الأصل الثابت بالطرق التالية:</span><span class="sxs-lookup"><span data-stu-id="3b254-142">The fixed asset disposal scrap transaction changes the field values for the fixed asset book in the following ways:</span></span>

- <span data-ttu-id="3b254-143">في قسم **الرصيد** ، يتم تحديث حقل **الحالة** إلى **مخرد‬** .</span><span class="sxs-lookup"><span data-stu-id="3b254-143">In the **Balance** section, the **Status** field is updated to **Scrapped** .</span></span>
- <span data-ttu-id="3b254-144">في قسم **الإصدار‬** ، تم تعيين حقل **تاريخ التخلص** إلى التاريخ الذي تم فيه تخريد الأصل.</span><span class="sxs-lookup"><span data-stu-id="3b254-144">In the **Issue** section, the **Disposal date** field is set to the date when the asset was scrapped.</span></span>

<span data-ttu-id="3b254-145">[![تفصيل دفتر يومية الأصول الثابتة](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span><span class="sxs-lookup"><span data-stu-id="3b254-145">[![Fixed assets journal detail](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span></span>

<span data-ttu-id="3b254-146">يبين الشكل التوضيحي التالي رصيد الأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="3b254-146">The following illustration shows the fixed asset balance.</span></span>

<span data-ttu-id="3b254-147">[![رصيد الأصل الثابت](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span><span class="sxs-lookup"><span data-stu-id="3b254-147">[![Fixed asset balance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span></span>

<span data-ttu-id="3b254-148">يبين الشكل التوضيحي التالي الإيصال الذي تم ترحيله.</span><span class="sxs-lookup"><span data-stu-id="3b254-148">The following illustration shows the voucher that is posted.</span></span>

<span data-ttu-id="3b254-149">[![صافي القيمة الدفترية](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span><span class="sxs-lookup"><span data-stu-id="3b254-149">[![Net book value](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span></span>
