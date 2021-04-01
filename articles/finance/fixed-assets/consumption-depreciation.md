---
title: إهلاك الاستهلاك
description: توفر هذه المقالة نظرة عامة على أسلوب الاستهلاك للإهلاك.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6309f8225bc82639d3e0e9effa7b0dcc4b5ccc50
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241256"
---
# <a name="consumption-depreciation"></a><span data-ttu-id="8b779-103">إهلاك الاستهلاك</span><span class="sxs-lookup"><span data-stu-id="8b779-103">Consumption depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b779-104">توفر هذه المقالة نظرة عامة على أسلوب الاستهلاك للإهلاك.</span><span class="sxs-lookup"><span data-stu-id="8b779-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="8b779-105">عند إعداد ملف تعريف إهلاك للأصول الثابتة وتحديد **استهلاك** في حقل **الطريقة** في صفحة **ملفات تعريف الإهلاك**، تستند الأصول الثابتة المعيَّنة إلى ملف تعريف الإهلاك إلى استخدامها.</span><span class="sxs-lookup"><span data-stu-id="8b779-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="8b779-106">ولا يلزمك إعداد النسب المئوية والفترات في صفحة **ملفات تعريف الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="8b779-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="8b779-107">وبعد قيامك بإنشاء ملف تعريف إهلاك يستخدم طريقة الاستهلاك، يمكنك إعداد الطريقة بطرق متعددة.</span><span class="sxs-lookup"><span data-stu-id="8b779-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="8b779-108">إعداد واستخدام إهلاك الاستهلاك</span><span class="sxs-lookup"><span data-stu-id="8b779-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="8b779-109">في صفحة **ملفات تعريف الإهلاك**، قم بإنشاء ملف تعريف الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="8b779-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="8b779-110">بالنسبة لحسابات الاستهلاك، يجب أن يتضمن ملف تعريف الإهلاك معرفًا واسمًا، ويجب تحديد **الاستهلاك** في حقل **الطريقة**.</span><span class="sxs-lookup"><span data-stu-id="8b779-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="8b779-111">في صفحة **معامِلات الاستهلاك**، قم بإعداد معامِلات الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="8b779-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="8b779-112">يجب أن يشتمل كل معامِل استهلاك على معرف واسم، ومعامل استهلاك تم تحديده كنسبة مئوية أو كمية.</span><span class="sxs-lookup"><span data-stu-id="8b779-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="8b779-113">في صفحة **وحدات الاستهلاك**، قم بإعداد وحدات الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="8b779-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="8b779-114">يجب أن تشتمل كل وحدة استهلاك على معرف واسم.</span><span class="sxs-lookup"><span data-stu-id="8b779-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="8b779-115">ويتم استخدام وحدات الاستهلاك لحساب إهلاك الاستهلاك في صفحة **إهلاك الاستهلاك**.</span><span class="sxs-lookup"><span data-stu-id="8b779-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="8b779-116">ومن أمثلة الوحدات الكيلومتر (كم) والكيلوجرام (كجم) والساعة.</span><span class="sxs-lookup"><span data-stu-id="8b779-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="8b779-117">في صفحة **الأصول الثابتة**، قم بإعداد الأصول الثابتة الفردية.</span><span class="sxs-lookup"><span data-stu-id="8b779-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="8b779-118">وللحصول على كل أصل ثابت، حدد نماذج القيم ودفاتر الإهلاك التي تشتمل على ملفات تعريف الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="8b779-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="8b779-119">ويجب عليك إعداد نماذج القيم أو دفاتر لإهلاك الاستهلاك، في حالة قيام أي أصول من أصولك الثابتة باستخدام ملف تعريف الإهلاك المستند إلى طريقة الاستهلاك.</span><span class="sxs-lookup"><span data-stu-id="8b779-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="8b779-120">ويتم إجراء هذا الإعداد في علامة التبويب **الإهلاك** في صفحة **نماذج القيم** الصفحة أو في علامة التبويب السريعة **عام** في صفحة **ملف تعريف الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="8b779-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="8b779-121">ويمكنك استخدام نفس نموذج القيمة للعديد من الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="8b779-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="8b779-122">تعد ملفات تعريف الإهلاك جزءًا من نموذج القيمة أو دفتر الإهلاك المحدد لكل أصل ثابت.</span><span class="sxs-lookup"><span data-stu-id="8b779-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="8b779-123">لا يمكنك إضافة أو تعديل ملفات تعريف الإهلاك مباشرةً في صفحة **الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="8b779-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="8b779-124">ويمكنك تعديل ملفات تعريف الإهلاك في صفحة **دفاتر الإهلاك**.</span><span class="sxs-lookup"><span data-stu-id="8b779-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="8b779-125">في صفحة **نماذج القيم** أو صفحة **دفاتر الإهلاك** في مجموعة حقول **إهلاك الاستهلاك**، أدخل المعلومات في الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="8b779-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="8b779-126">معامل الاستهلاك</span><span class="sxs-lookup"><span data-stu-id="8b779-126">Consumption factor</span></span>
    -   <span data-ttu-id="8b779-127">الوحدة</span><span class="sxs-lookup"><span data-stu-id="8b779-127">Unit</span></span>
    -   <span data-ttu-id="8b779-128">إهلاك الوحدة</span><span class="sxs-lookup"><span data-stu-id="8b779-128">Unit depreciation</span></span>
    -   <span data-ttu-id="8b779-129">الاستهلاك المقدر</span><span class="sxs-lookup"><span data-stu-id="8b779-129">Estimated consumption</span></span>

    <span data-ttu-id="8b779-130">يقوم حقل **الاستهلاك المرّحل** بعرض إهلاك الاستهلاك، بالوحدات، الذي تم ترحيله بالفعل لمجموعة من الأصل الثابت ونموذج القيمة، أو لدفتر الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="8b779-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="8b779-131">لا يمكنك تحديث القيمة الموجودة في هذا الحقل يدوياً.</span><span class="sxs-lookup"><span data-stu-id="8b779-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="8b779-132">أمثلة</span><span class="sxs-lookup"><span data-stu-id="8b779-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="8b779-133">مثال 1</span><span class="sxs-lookup"><span data-stu-id="8b779-133">Example 1</span></span>

<span data-ttu-id="8b779-134">تم إعداد معامل الاستهلاك التالي لتاريخ 31 يناير:</span><span class="sxs-lookup"><span data-stu-id="8b779-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="8b779-135">الكمية تساوي 1,000.</span><span class="sxs-lookup"><span data-stu-id="8b779-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="8b779-136">سعر إهلاك الوحدة المحدد للأصل الثابت المحدد هو 1.5.</span><span class="sxs-lookup"><span data-stu-id="8b779-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="8b779-137">فيما يلي مقترح الإهلاك في 31 يناير: الكمية × إهلاك الوحدة 1,000 × 1.5 = 1,500 إذا كان المعامِل الذي تم تحديده للأصل الثابت هو معامل نسبة مئوية، ويتم ضرب الكمية المقدرة في حقل **الاستهلاك المقدر** لنموذج قيمة الأصل الثابت في النسبة المئوية التي تم إعدادها لتاريخ الانتهاء المحدد.</span><span class="sxs-lookup"><span data-stu-id="8b779-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="8b779-138">يتم فيما بعد اقتراح الكمية الناتجة باعتبارها كمية الإهلاك للفترة.</span><span class="sxs-lookup"><span data-stu-id="8b779-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="8b779-139">مثال 2</span><span class="sxs-lookup"><span data-stu-id="8b779-139">Example 2</span></span>

<span data-ttu-id="8b779-140">تم إعداد معامل إهلاك الاستهلاك التالي لتاريخ 31 يناير:</span><span class="sxs-lookup"><span data-stu-id="8b779-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="8b779-141">النسبة المئوية هي 10 في المائة.</span><span class="sxs-lookup"><span data-stu-id="8b779-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="8b779-142">سعر إهلاك الوحدة المحدد للأصل الثابت المحدد هو 1.5.</span><span class="sxs-lookup"><span data-stu-id="8b779-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="8b779-143">الكمية المقدرة للأصل الثابت هي 2,000.</span><span class="sxs-lookup"><span data-stu-id="8b779-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="8b779-144">فيما يلي مقترح الإهلاك في 31 يناير: الكمية المقدرة × النسبة المئوية × إهلاك الوحدة 2,000 × 10 × 1.5 = 300</span><span class="sxs-lookup"><span data-stu-id="8b779-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]