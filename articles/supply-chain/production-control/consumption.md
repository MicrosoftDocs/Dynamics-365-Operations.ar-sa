---
title: "حساب استهلاك المواد"
description: "توفر هذه المقالة معلومات حول مختلف الخيارات المتعلقة بحساب استهلاك المواد."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f674a1f0051ee4b228b8a92f717ef5348a452bed
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="calculate-material-consumption"></a><span data-ttu-id="8200d-103">حساب استهلاك المواد</span><span class="sxs-lookup"><span data-stu-id="8200d-103">Calculate material consumption</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8200d-104">توفر هذه المقالة معلومات حول مختلف الخيارات المتعلقة بحساب استهلاك المواد.</span><span class="sxs-lookup"><span data-stu-id="8200d-104">This article provides information about various options that are related to the calculation of material consumption.</span></span> 

<span data-ttu-id="8200d-105">تتوفر الخيارات التالية المتعلقة بحساب استهلاك المواد في علامتي التبويب **إعداد** و**استهلاك الخطوة** في علامة التبويب السريع **تفاصيل البند** في صفحة **قائمة مكونات الصنف**.</span><span class="sxs-lookup"><span data-stu-id="8200d-105">The following options that are related to the calculation of material consumption are available on the **Setup** and **Step consumption** tabs on the **Line details** FastTab of the **Bill of materials** page.</span></span>

## <a name="variable-and-constant-consumption"></a><span data-ttu-id="8200d-106">الاستهلاك المتغير والثابت</span><span class="sxs-lookup"><span data-stu-id="8200d-106">Variable and constant consumption</span></span>
<span data-ttu-id="8200d-107">‏‫في حقل **الاستهلاك هو**، يمكنك تحديد ما إذا كان يجب حساب استهلاك كمية ثابتة أو كمية متغيرة. </span><span class="sxs-lookup"><span data-stu-id="8200d-107">In the **Consumption is** field, you can select whether consumption should be calculated as a constant quantity or a variable quantity.</span></span> <span data-ttu-id="8200d-108">حدد **ثابت** إذا كان حجم أو كمية ثابتة مطلوبًا للإنتاج، بغض النظر عن الكمية التي تم إنتاجها.‬</span><span class="sxs-lookup"><span data-stu-id="8200d-108">Select **Constant** if a fixed quantity or volume is required for the production, regardless of the quantity that is produced.</span></span> <span data-ttu-id="8200d-109">حدد **متغير**، وهو الإعداد الافتراضي، إذا كانت الكمية المطلوبة من المادة في السلعة المنتهية تتناسب مع عدد السلع المنتهية التي تم إنتاجها.</span><span class="sxs-lookup"><span data-stu-id="8200d-109">Select **Variable**, which is the default setting, if the required amount of material in the finished goods is proportional to the number of finished goods that are produced.</span></span>

## <a name="calculating-consumption-from-a-formula"></a><span data-ttu-id="8200d-110">حساب الاستهلاك من معادلة</span><span class="sxs-lookup"><span data-stu-id="8200d-110">Calculating consumption from a formula</span></span>
<span data-ttu-id="8200d-111">في حقل **المعادلة**، يمكنك إعداد معادلات مختلفة لحساب استهلاك المواد.</span><span class="sxs-lookup"><span data-stu-id="8200d-111">In the **Formula** field, you can set up various formulas for calculating material consumption.</span></span> <span data-ttu-id="8200d-112">وإذا كنت تستخدم القيمة الافتراضية، **قياسي**، لا يتم حساب الاستهلاك من معادلة.</span><span class="sxs-lookup"><span data-stu-id="8200d-112">If you use the default value, **Standard**, the consumption isn't calculated from a formula.</span></span> <span data-ttu-id="8200d-113">تعمل المعادلات التالية مع حقول **الارتفاع**، و**العرض**، و**العمق**، و**الكثافة**، و**ثابت**:</span><span class="sxs-lookup"><span data-stu-id="8200d-113">The following formulas work together with the **Height**, **Width**, **Depth**, **Density**, and **Constant** fields:</span></span>

-   <span data-ttu-id="8200d-114">الارتفاع \* ثابت</span><span class="sxs-lookup"><span data-stu-id="8200d-114">Height \* Constant</span></span>
-   <span data-ttu-id="8200d-115">الارتفاع \* العرض \* ثابت</span><span class="sxs-lookup"><span data-stu-id="8200d-115">Height \* Width \* Constant</span></span>
-   <span data-ttu-id="8200d-116">الارتفاع \* العرض \* العمق \* ثابت</span><span class="sxs-lookup"><span data-stu-id="8200d-116">Height \* Width \* Depth \* Constant</span></span>
-   <span data-ttu-id="8200d-117">(الارتفاع \* العرض \* العمق / الكثافة) \* ثابت</span><span class="sxs-lookup"><span data-stu-id="8200d-117">(Height \* Width \* Depth / Density) \* Constant</span></span>

## <a name="rounding-up-and-multiples"></a><span data-ttu-id="8200d-118">التقريب والمضاعفات</span><span class="sxs-lookup"><span data-stu-id="8200d-118">Rounding up and multiples</span></span>
<span data-ttu-id="8200d-119">معًا، يتيح حقلا **التقريب** و**المضاعفات** لك إمكانية تقريب قيمة استهلاك المواد لأعلى.</span><span class="sxs-lookup"><span data-stu-id="8200d-119">Together, the **Rounding up** and **Multiples** fields let you round up the material consumption value.</span></span> <span data-ttu-id="8200d-120">على سبيل المثال، يمكنك تقريب القيمة وفقًا لوحدة المعالجة التي يتم فيها انتقاء المواد الخام للإنتاج.</span><span class="sxs-lookup"><span data-stu-id="8200d-120">For example, you can round up the value according to the handling unit in which the raw material is picked for production.</span></span> <span data-ttu-id="8200d-121">تتوفر الخيارات التالية في حقل **التقريب**: **الكمية**، و**القياس**، و**الاستهلاك**.</span><span class="sxs-lookup"><span data-stu-id="8200d-121">The following options are available in the **Rounding up** field: **Quantity**, **Measurement**, and **Consumption**.</span></span>

### <a name="quantity"></a><span data-ttu-id="8200d-122">الكمية</span><span class="sxs-lookup"><span data-stu-id="8200d-122">Quantity</span></span>

<span data-ttu-id="8200d-123">إذا قمت بتحديد **كمية** كآلية التقريب للأعلى، فيجب أن تكون الكمية ضعف الكمية المحددة.</span><span class="sxs-lookup"><span data-stu-id="8200d-123">If you select **Quantity** as the rounding-up mechanism, the quantity must be a multiple of the specified quantity.</span></span> <span data-ttu-id="8200d-124">على سبيل المثال، في حالة طلب الأرقام الصحيحة، فحدد **1** في حقل **المضاعفات**.</span><span class="sxs-lookup"><span data-stu-id="8200d-124">For example, if whole numbers are required, select **1** in the **Multiples** field.</span></span> <span data-ttu-id="8200d-125">ويتم فيما بعد تقريب الأرقام إلى كمية يمكن قسمتها على 1.</span><span class="sxs-lookup"><span data-stu-id="8200d-125">Numbers are then rounded up to a quantity that is divisible by 1.</span></span>

### <a name="measurement"></a><span data-ttu-id="8200d-126">القياس</span><span class="sxs-lookup"><span data-stu-id="8200d-126">Measurement</span></span>

<span data-ttu-id="8200d-127">بشكل عام، يمكنك تحديد **القياس** كآلية تقريب لأعلى عندما تأتي مادة خام بإبعاد محددة.</span><span class="sxs-lookup"><span data-stu-id="8200d-127">Typically, you select **Measurement** as the rounding-up mechanism when the raw material comes in specific dimensions.</span></span> <span data-ttu-id="8200d-128">على سبيل المثال، مطلوب قطعة من أنبوب معدني 2 متر لسلعة منتهية، ويتم تخزين أنبوب معدني بطول 4.5 متر.</span><span class="sxs-lookup"><span data-stu-id="8200d-128">For example, a piece of 2-meter metal tube is required for a finished good, and the metal tube is stored in 4.5-meter lengths.</span></span> <span data-ttu-id="8200d-129">في هذه الحالة، يمكن استخدام آلية تقريب **القياس** لأعلى لحساب عدد الأنابيب المعدنية المطلوبة لإنتاج عدد معين من أجزاء السلعة المنتهية.</span><span class="sxs-lookup"><span data-stu-id="8200d-129">In this case, the **Measurement** rounding-up mechanism can be used to calculate how many metal tubes are required to produce a specific number of pieces of the finished good.</span></span> <span data-ttu-id="8200d-130">في هذا المثال، يتم تعيين حقل **‬‏‫المعادلة** إلى **الارتفاع \* ثابت**.</span><span class="sxs-lookup"><span data-stu-id="8200d-130">For this example, the **Formula** field is set to **Height \* Constant**.</span></span> <span data-ttu-id="8200d-131">ويتم تعيين حقل **الارتفاع** إلى **2** للإشارة إلى طول الأنبوب المطلوب للسلعة المنتهية.‬</span><span class="sxs-lookup"><span data-stu-id="8200d-131">The **Height** field is set to **2** to indicate the length of the tube that is required for the finished good.</span></span> <span data-ttu-id="8200d-132">يتم تعيين حقل **مضاعفة** إلى **4.5** للإشارة إلى أن يتم انتقاء الأنبوب بطول 4.5 متر.</span><span class="sxs-lookup"><span data-stu-id="8200d-132">The **Multiple** field is set to **4.5** to indicate that the tube is picked in lengths of 4.5 meters.</span></span> <span data-ttu-id="8200d-133">فتكون العملية الحسابية كالتالي:</span><span class="sxs-lookup"><span data-stu-id="8200d-133">Here is the calculation:</span></span>

1.  <span data-ttu-id="8200d-134">عدد المضاعفات المطلوبة لـ 10 قطع من البضائع الجاهزة: 10 ÷ 2 = 5 قطع</span><span class="sxs-lookup"><span data-stu-id="8200d-134">Number of multiples that are required for 10 pieces of the finished good: 10 ÷ 2 = 5 pieces</span></span>
2.  <span data-ttu-id="8200d-135">الاستهلاك الإجمالي: 4.5 × 5 = 22.5 متر من الأنبوب المعدني</span><span class="sxs-lookup"><span data-stu-id="8200d-135">Total consumption:  4.5 × 5 = 22.5 meters of metal tube</span></span>

<span data-ttu-id="8200d-136">ويفترض تخريد 0.5 متر من الأنابيب المعدنية لكل خمس قطع من الأنبوب يتم استهلاكها.</span><span class="sxs-lookup"><span data-stu-id="8200d-136">It's assumed that 0.5 meter of tube is scrapped for every five pieces of tube that are consumed.</span></span>

### <a name="consumption"></a><span data-ttu-id="8200d-137">الاستهلاك</span><span class="sxs-lookup"><span data-stu-id="8200d-137">Consumption</span></span>

<span data-ttu-id="8200d-138">وبشكل عام، تحدد**استهلاك** كآلية للتقريب عندما يجب انتقاء المواد الخام بكميات الكاملة لوحدة معالجة محددة للمنتج.</span><span class="sxs-lookup"><span data-stu-id="8200d-138">Typically, you select **Consumption** as the rounding-up mechanism when raw material must be picked in whole quantities of a specific handling unit of the product.</span></span> <span data-ttu-id="8200d-139">على سبيل المثال، يتم استخدام 2 كوارت من الطلاء لإنتاج قطعة واحدة من سلعة نهائية، ويتم انتقاء الطلاء في علب سعة 25 كوارت.</span><span class="sxs-lookup"><span data-stu-id="8200d-139">For example, 2 quarts of paint are used to produce one piece of a finished good, and the paint is picked in 25-quart cans.</span></span> <span data-ttu-id="8200d-140">وفي هذه الحالة، يمكن استخدام آلية تقريب **الاستهلاك** لأعلى لتقريب الاستهلاك لأعلى إلى الأعداد الصحيحة للعلب سعة 25 كوارت.</span><span class="sxs-lookup"><span data-stu-id="8200d-140">In this case, the **Consumption** rounding-up mechanism can be used to round up consumption to whole numbers of 25-quart cans.</span></span> <span data-ttu-id="8200d-141">وفيما يلي حساب كمية الطلاء المطلوبة إذا كان يجب إنتاج 180 قطعة من البضائع الجاهزة:</span><span class="sxs-lookup"><span data-stu-id="8200d-141">Here is the calculation for the amount of paint that is required if 180 pieces of the finished good must be produced:</span></span>

1.  <span data-ttu-id="8200d-142">الطلاء المطلوب، باستثناء الخردة: 180 × 2 = 360 جالونًا</span><span class="sxs-lookup"><span data-stu-id="8200d-142">Paint that is required, excluding scrap: 180 × 2 = 360 quarts</span></span>
2.  <span data-ttu-id="8200d-143">عدد العلب: 360 ÷ 25 = 14.4، الذي يتم تقريبه إلى 15</span><span class="sxs-lookup"><span data-stu-id="8200d-143">Number of cans: 360 ÷ 25 = 14.4, which is rounded up to 15</span></span>
3.  <span data-ttu-id="8200d-144">الطلاء المطلوب، بما في ذلك الخردة: 15 × 25 = 375 كوارت</span><span class="sxs-lookup"><span data-stu-id="8200d-144">Paint that is required, including scrap: 15 × 25 = 375 quarts</span></span>

## <a name="step-consumption"></a><span data-ttu-id="8200d-145">استهلاك مرحلي</span><span class="sxs-lookup"><span data-stu-id="8200d-145">Step consumption</span></span>
<span data-ttu-id="8200d-146">يُستخدم استهلاك الخطوة لحساب الاستهلاك الثابت في فواصل زمنية للكمية.</span><span class="sxs-lookup"><span data-stu-id="8200d-146">Step consumption is used to calculate constant consumption in quantity intervals.</span></span> <span data-ttu-id="8200d-147">إذا حددت **خطوة الاستهلاك** في حقل **الصيغة** على علامة تبويب **الإعداد**، فيمكنك إضافة معلومات حول الخطوات في علامة التبويب **خطوة الاستهلاك**. يمكن إعداد الكمية الثابتة المستهلكة عبر فواصل زمنية للكمية المنتجة.</span><span class="sxs-lookup"><span data-stu-id="8200d-147">If you select **Step consumption** in the **Formula** field on the **Setup** tab, you can add information about the steps on the **Step consumption** tab. The fixed consumed quantity can be set up in intervals of the produced quantity.</span></span> <span data-ttu-id="8200d-148">على سبيل المثال، يتم إعداد استهلاك الخطوة كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="8200d-148">For example, step consumption is set up as shown in the following table.</span></span>

| <span data-ttu-id="8200d-149">السلسلة من</span><span class="sxs-lookup"><span data-stu-id="8200d-149">From series</span></span> | <span data-ttu-id="8200d-150">الكمية</span><span class="sxs-lookup"><span data-stu-id="8200d-150">Quantity</span></span> |
|-------------|----------|
| <span data-ttu-id="8200d-151">0.00</span><span class="sxs-lookup"><span data-stu-id="8200d-151">0.00</span></span>        | <span data-ttu-id="8200d-152">10.0000</span><span class="sxs-lookup"><span data-stu-id="8200d-152">10.0000</span></span>  |
| <span data-ttu-id="8200d-153">100.00</span><span class="sxs-lookup"><span data-stu-id="8200d-153">100.00</span></span>      | <span data-ttu-id="8200d-154">20.0000</span><span class="sxs-lookup"><span data-stu-id="8200d-154">20.0000</span></span>  |
| <span data-ttu-id="8200d-155">200.00</span><span class="sxs-lookup"><span data-stu-id="8200d-155">200.00</span></span>      | <span data-ttu-id="8200d-156">40.0000</span><span class="sxs-lookup"><span data-stu-id="8200d-156">40.0000</span></span>  |

<span data-ttu-id="8200d-157">كمية قائمة مكونات الصنف هي 1، وكمية الإنتاج هي 110.</span><span class="sxs-lookup"><span data-stu-id="8200d-157">The bill of materials (BOM) quantity is 1, and the production quantity is 110.</span></span> <span data-ttu-id="8200d-158">المعادلة الخاصة بالاستهلاك هي من سلسلة (الكمية) = الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="8200d-158">The formula for the consumption is From series (Quantity) = Consumption.</span></span> <span data-ttu-id="8200d-159">ونظراً لأن كمية الإنتاج تساوي 110، فإنها تقع في "من السلسلة 100."</span><span class="sxs-lookup"><span data-stu-id="8200d-159">Because the production quantity is 110, it falls into the "From 100 series."</span></span> <span data-ttu-id="8200d-160">ولذلك، الكمية تساوي 20.</span><span class="sxs-lookup"><span data-stu-id="8200d-160">Therefore, the quantity is 20.</span></span>




