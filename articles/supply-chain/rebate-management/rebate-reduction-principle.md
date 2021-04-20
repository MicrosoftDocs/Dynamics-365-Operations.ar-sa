---
title: قواعد خفض الخصومات
description: يصف هذا الموضوع كيفية إعداد قواعد التخفيض. تتحكم قواعد التخفيض في السلوك عند تطبيق خصومات متعددة علي نفس الصنف أو الحركة.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 79f7e481b65ec40f0fb7e259037cd4988b3b5c07
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831688"
---
# <a name="rebate-reduction-principles"></a><span data-ttu-id="488b1-104">قواعد خفض الخصومات</span><span class="sxs-lookup"><span data-stu-id="488b1-104">Rebate reduction principles</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="488b1-105">يمكنك تجميع صفقات أداره الخصومات في *قواعد التخفيض* لتقليل المخصصات الأخرى المرتبطة بأحد الأصناف، و/أو لتقليل القيم الناتجة لحسابات الخصم.</span><span class="sxs-lookup"><span data-stu-id="488b1-105">You can group Rebate management deals into *reduction principles* to reduce other provisions that are associated with an item, and/or to reduce the resulting values of rebate calculations.</span></span> <span data-ttu-id="488b1-106">بعد اعداد قواعد تخفيض الخصم، يمكنك اختياريا تعيينها، حسب الحاجة، إلى بنود مجموعات أداره الخصم.</span><span class="sxs-lookup"><span data-stu-id="488b1-106">After the rebate reduction principles are set up, you can optionally assign them, as required, to the lines of your Rebate management deals.</span></span>

<span data-ttu-id="488b1-107">تنطبق قواعد قاعده خفض الخصم فقط عند تداخل الخصومات.</span><span class="sxs-lookup"><span data-stu-id="488b1-107">The rebate reduction principle rules apply only when rebate deals overlap.</span></span> <span data-ttu-id="488b1-108">ولذلك، قد تمنح هذه الادوات خصومات متعددة في المواقف التي لا يمكن فيها الحصول علي خصومات متعددة.</span><span class="sxs-lookup"><span data-stu-id="488b1-108">Therefore, they might grant multiple rebates in situations where multiple rebates aren't owed.</span></span>

## <a name="manage-rebate-reduction-principles"></a><span data-ttu-id="488b1-109">إدارة قواعد خفض الخصومات</span><span class="sxs-lookup"><span data-stu-id="488b1-109">Manage rebate reduction principles</span></span>

<span data-ttu-id="488b1-110">للعمل مع قواعد تخفيض الخصم، انتقل إلى **إدارة الخصومات \> إعداد \> قواعد تخفيض الخصومات**.</span><span class="sxs-lookup"><span data-stu-id="488b1-110">To work with rebate reduction principles, go to **Rebate management \> Setup \> Rebate reduction principles**.</span></span> <span data-ttu-id="488b1-111">ثم استخدم الأزرار الموجودة في جزء الإجراءات لإضافة وإزالة قواعد التخفيض كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="488b1-111">Then use the buttons on the Action Pane to add and remove reduction principles as required.</span></span> <span data-ttu-id="488b1-112">بالنسبة لكل قاعدة، قم بتعيين الحقول كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="488b1-112">For each principle, set the fields as described in the following table.</span></span>

| <span data-ttu-id="488b1-113">الحقل</span><span class="sxs-lookup"><span data-stu-id="488b1-113">Field</span></span> | <span data-ttu-id="488b1-114">الوصف</span><span class="sxs-lookup"><span data-stu-id="488b1-114">Description</span></span> |
|---|---|
| <span data-ttu-id="488b1-115">قاعدة خفض الخصومات</span><span class="sxs-lookup"><span data-stu-id="488b1-115">Rebate reduction principle</span></span> | <span data-ttu-id="488b1-116">ادخل اسما فريدا لقاعده تخفيض الخصم.</span><span class="sxs-lookup"><span data-stu-id="488b1-116">Enter a unique name for the rebate reduction principle.</span></span> |
| <span data-ttu-id="488b1-117">الوصف</span><span class="sxs-lookup"><span data-stu-id="488b1-117">Description</span></span> | <span data-ttu-id="488b1-118">أدخل وصفًا لقاعدة تخفيض الخصم.</span><span class="sxs-lookup"><span data-stu-id="488b1-118">Enter a description of the rebate reduction principle.</span></span> |
| <span data-ttu-id="488b1-119">تطبيق التخفيض</span><span class="sxs-lookup"><span data-stu-id="488b1-119">Apply reduction</span></span> | <span data-ttu-id="488b1-120">حدد خانه الاختيار هذه لتطبيق أساس الخفض علي الخصومات التي تنتمي إلى قاعده تقليل الخصم.</span><span class="sxs-lookup"><span data-stu-id="488b1-120">Select this check box to apply a reduction basis to rebates that belong to this rebate reduction principle.</span></span> |
| <span data-ttu-id="488b1-121">أساس التخفيض</span><span class="sxs-lookup"><span data-stu-id="488b1-121">Reduction basis</span></span> | <span data-ttu-id="488b1-122">إذا حددت خانة الاختيار **تطبيق التخفيض**، فحدد أساس التخفيض (*التوفير* أو *الخصومات* أو *كلاهما*).</span><span class="sxs-lookup"><span data-stu-id="488b1-122">If you selected the **Apply reduction** check box, select the reduction basis (*Provision*, *Rebates*, or *Both*).</span></span> <span data-ttu-id="488b1-123">إذا حددت *كليهما*، وإذا تم ترحيل كل من المخصص والخصم لصفقة سابقه، سيتم تطبيق الخصم فقط.</span><span class="sxs-lookup"><span data-stu-id="488b1-123">If you select *Both*, and if both a provision and a rebate have been posted for a previous deal, only the rebate will be applied.</span></span> |
| <span data-ttu-id="488b1-124">استبعاد من الخفض</span><span class="sxs-lookup"><span data-stu-id="488b1-124">Exclude from reduction</span></span> | <span data-ttu-id="488b1-125">في حاله تحديد خانه الاختيار هذه، سيتم استبعاد المخصصات والخصومات التي تنتمي إلى مبدا خفض الخصم من التخفيضات التالية.</span><span class="sxs-lookup"><span data-stu-id="488b1-125">If this check box is selected, provisions and rebates that belong to this rebate reduction principle will be excluded from subsequent reductions.</span></span> <span data-ttu-id="488b1-126">لا ينطبق اعداد حقل **أساس الخفض** علي هذا الاعداد.</span><span class="sxs-lookup"><span data-stu-id="488b1-126">The setting of the **Reduction basis** field doesn't apply to this setting.</span></span> |

## <a name="examples-of-rebate-reduction-principle-setups"></a><span data-ttu-id="488b1-127">أمثله لإعدادات قاعده خفض الخصم</span><span class="sxs-lookup"><span data-stu-id="488b1-127">Examples of rebate reduction principle setups</span></span>

<span data-ttu-id="488b1-128">يوضح الجدول التالي بعض الامثله النموذجية لإعدادات قاعده تقليل الخصم.</span><span class="sxs-lookup"><span data-stu-id="488b1-128">The following table shows some typical examples of rebate reduction principle setups.</span></span> <span data-ttu-id="488b1-129">بالنسبة لكل قاعده من قواعد تخفيض الخصم، تصف قيمة حقل **الوصف** الغرض من قاعده خفض الخصم.</span><span class="sxs-lookup"><span data-stu-id="488b1-129">For each of these rebate reduction principles, the value of the **Description** field describes the purpose of the rebate reduction principle.</span></span>

| <span data-ttu-id="488b1-130">قاعدة خفض الخصومات</span><span class="sxs-lookup"><span data-stu-id="488b1-130">rebate reduction principle</span></span> | <span data-ttu-id="488b1-131">الوصف</span><span class="sxs-lookup"><span data-stu-id="488b1-131">Description</span></span> | <span data-ttu-id="488b1-132">تطبيق التخفيض</span><span class="sxs-lookup"><span data-stu-id="488b1-132">Apply reduction</span></span> | <span data-ttu-id="488b1-133">أساس التخفيض</span><span class="sxs-lookup"><span data-stu-id="488b1-133">Reduction basis</span></span> | <span data-ttu-id="488b1-134">استبعاد من الخفض</span><span class="sxs-lookup"><span data-stu-id="488b1-134">Exclude from reduction</span></span> |
|---|---|---|---|---|
| <span data-ttu-id="488b1-135">مؤجل</span><span class="sxs-lookup"><span data-stu-id="488b1-135">Deferred</span></span> | <span data-ttu-id="488b1-136">تخفيض الخصم</span><span class="sxs-lookup"><span data-stu-id="488b1-136">Reduce rebate</span></span> | <span data-ttu-id="488b1-137">نعم</span><span class="sxs-lookup"><span data-stu-id="488b1-137">Yes</span></span> | <span data-ttu-id="488b1-138">كلاهما</span><span class="sxs-lookup"><span data-stu-id="488b1-138">Both</span></span> | <span data-ttu-id="488b1-139">لا</span><span class="sxs-lookup"><span data-stu-id="488b1-139">No</span></span> |
| <span data-ttu-id="488b1-140">Exclreb</span><span class="sxs-lookup"><span data-stu-id="488b1-140">Exclreb</span></span> | <span data-ttu-id="488b1-141">استبعاد الخصم</span><span class="sxs-lookup"><span data-stu-id="488b1-141">Exclude rebate</span></span> | <span data-ttu-id="488b1-142">نعم</span><span class="sxs-lookup"><span data-stu-id="488b1-142">Yes</span></span> | <span data-ttu-id="488b1-143">خصم</span><span class="sxs-lookup"><span data-stu-id="488b1-143">Rebate</span></span> | <span data-ttu-id="488b1-144">نعم</span><span class="sxs-lookup"><span data-stu-id="488b1-144">Yes</span></span> |
| <span data-ttu-id="488b1-145">متعددة</span><span class="sxs-lookup"><span data-stu-id="488b1-145">Multiple</span></span> | <span data-ttu-id="488b1-146">خصومات متعددة</span><span class="sxs-lookup"><span data-stu-id="488b1-146">Multiple rebates</span></span> | <span data-ttu-id="488b1-147">نعم</span><span class="sxs-lookup"><span data-stu-id="488b1-147">Yes</span></span> | <span data-ttu-id="488b1-148">كلاهما</span><span class="sxs-lookup"><span data-stu-id="488b1-148">Both</span></span> | <span data-ttu-id="488b1-149">نعم</span><span class="sxs-lookup"><span data-stu-id="488b1-149">Yes</span></span> |
| <span data-ttu-id="488b1-150">بلا</span><span class="sxs-lookup"><span data-stu-id="488b1-150">None</span></span> | <span data-ttu-id="488b1-151">التوفير والخصم فقط</span><span class="sxs-lookup"><span data-stu-id="488b1-151">Prov and Rebate only</span></span> | <span data-ttu-id="488b1-152">لا</span><span class="sxs-lookup"><span data-stu-id="488b1-152">No</span></span> | <span data-ttu-id="488b1-153">كلاهما</span><span class="sxs-lookup"><span data-stu-id="488b1-153">Both</span></span> | <span data-ttu-id="488b1-154">نعم</span><span class="sxs-lookup"><span data-stu-id="488b1-154">Yes</span></span> |
| <span data-ttu-id="488b1-155">توفير</span><span class="sxs-lookup"><span data-stu-id="488b1-155">Provision</span></span> | <span data-ttu-id="488b1-156">التوفير فقط</span><span class="sxs-lookup"><span data-stu-id="488b1-156">Provision only</span></span> | <span data-ttu-id="488b1-157">نعم</span><span class="sxs-lookup"><span data-stu-id="488b1-157">Yes</span></span> | <span data-ttu-id="488b1-158">توفير</span><span class="sxs-lookup"><span data-stu-id="488b1-158">Provision</span></span> | <span data-ttu-id="488b1-159">لا</span><span class="sxs-lookup"><span data-stu-id="488b1-159">No</span></span> |
| <span data-ttu-id="488b1-160">خصم</span><span class="sxs-lookup"><span data-stu-id="488b1-160">Rebate</span></span> | <span data-ttu-id="488b1-161">الخصم فقط</span><span class="sxs-lookup"><span data-stu-id="488b1-161">Rebate only</span></span> | <span data-ttu-id="488b1-162">نعم</span><span class="sxs-lookup"><span data-stu-id="488b1-162">Yes</span></span> | <span data-ttu-id="488b1-163">خصم</span><span class="sxs-lookup"><span data-stu-id="488b1-163">Rebate</span></span> | <span data-ttu-id="488b1-164">نعم</span><span class="sxs-lookup"><span data-stu-id="488b1-164">Yes</span></span> |

## <a name="examples-of-rebate-reduction-principle-calculations"></a><span data-ttu-id="488b1-165">أمثله لعمليات حساب قاعده خفض الخصم</span><span class="sxs-lookup"><span data-stu-id="488b1-165">Examples of rebate reduction principle calculations</span></span>

<span data-ttu-id="488b1-166">لديك أمر مبيعات يشتمل علي بند أمر مبيعات واحد.</span><span class="sxs-lookup"><span data-stu-id="488b1-166">You have a sales order that has a single sales order line.</span></span> <span data-ttu-id="488b1-167">يحتوي هذا السطر على قيمه 1,000 دولار.</span><span class="sxs-lookup"><span data-stu-id="488b1-167">This line has a value of $1,000.</span></span> <span data-ttu-id="488b1-168">تنطبق الصفقات التالية على الأمر:</span><span class="sxs-lookup"><span data-stu-id="488b1-168">The following deals apply to the order:</span></span>

- <span data-ttu-id="488b1-169">**الصفقة 1:** 10 بالمائة على 1,000 دولار</span><span class="sxs-lookup"><span data-stu-id="488b1-169">**Deal 1:** 10 percent on $1,000</span></span>
- <span data-ttu-id="488b1-170">**الصفقة 2:** 15 بالمائة على 1,000 دولار</span><span class="sxs-lookup"><span data-stu-id="488b1-170">**Deal 2:** 15 percent on $1,000</span></span>
- <span data-ttu-id="488b1-171">**الصفقة 3:** 20 بالمائة على 1,000 دولار</span><span class="sxs-lookup"><span data-stu-id="488b1-171">**Deal 3:** 20 percent on $1,000</span></span>
- <span data-ttu-id="488b1-172">**الصفقة 4:** 25 بالمائة على 1,000 دولار</span><span class="sxs-lookup"><span data-stu-id="488b1-172">**Deal 4:** 25 percent on $1,000</span></span>

<span data-ttu-id="488b1-173">ترتيب المعالجة مهم جدًا.</span><span class="sxs-lookup"><span data-stu-id="488b1-173">The order of processing is very important.</span></span> <span data-ttu-id="488b1-174">يستند أمر المعالجة إلى الطريقة التي تعمل بها، كما هو موضح في [معالجة الخصومات ومراجعتها وترحيلها](process-review-post.md).</span><span class="sxs-lookup"><span data-stu-id="488b1-174">The processing order is based on the way that you work, as described in [Process, review, and post rebates](process-review-post.md).</span></span>

<span data-ttu-id="488b1-175">علي سبيل المثال، يلخص الجدول التالي النتيجة إذا كنت تستخدم الأمر *1 و2 و3 و4* وإذا قمت بمعالجه المخصصات فقط.</span><span class="sxs-lookup"><span data-stu-id="488b1-175">For example, the following table summarizes the result if you use the order *1, 2, 3, 4*, and if you process only the provisions.</span></span>

| <span data-ttu-id="488b1-176">صفقة</span><span class="sxs-lookup"><span data-stu-id="488b1-176">Deal</span></span> | <span data-ttu-id="488b1-177">الوصف والإعدادات</span><span class="sxs-lookup"><span data-stu-id="488b1-177">Description and settings</span></span> | <span data-ttu-id="488b1-178">نتيجة التوفير</span><span class="sxs-lookup"><span data-stu-id="488b1-178">Provision result</span></span> |
|---|---|---|
| <span data-ttu-id="488b1-179">1</span><span class="sxs-lookup"><span data-stu-id="488b1-179">1</span></span> | <p><span data-ttu-id="488b1-180">لا يقوم التصنيف بالتحقق من العروض الأخرى لأجل التخفيض.</span><span class="sxs-lookup"><span data-stu-id="488b1-180">The classification doesn't check other deals for reductions.</span></span> <span data-ttu-id="488b1-181">يتم اجراء التحقق لكل من التوفيرات والخصومات.</span><span class="sxs-lookup"><span data-stu-id="488b1-181">The check is done for both provisions and rebates.</span></span></p><ul><li><span data-ttu-id="488b1-182">**تطبيق التخفيض:** *لا*</span><span class="sxs-lookup"><span data-stu-id="488b1-182">**Apply reduction:** *No*</span></span></li><li><span data-ttu-id="488b1-183">**أساس التخفيض:** *كلاهما*</span><span class="sxs-lookup"><span data-stu-id="488b1-183">**Reduction basis:** *Both*</span></span></li><li><span data-ttu-id="488b1-184">**استبعاد من الخفض:** *لا*</span><span class="sxs-lookup"><span data-stu-id="488b1-184">**Exclude from reduction:** *No*</span></span></li></ul> | <span data-ttu-id="488b1-185">1,000 دولار × 10% = 100 دولار</span><span class="sxs-lookup"><span data-stu-id="488b1-185">$1,000 × 10% = $100</span></span> |
| <span data-ttu-id="488b1-186">2</span><span class="sxs-lookup"><span data-stu-id="488b1-186">2</span></span> | <p><span data-ttu-id="488b1-187">يتحقق التصنيف من العروض الأخرى لعمليه التخفيض لكن تم وضع علامة عليه بحيث يتم تجاهله.</span><span class="sxs-lookup"><span data-stu-id="488b1-187">The classification checks other deals for reductions but is flagged so that it itself is ignored.</span></span> <span data-ttu-id="488b1-188">ولا يحدث التحقق إلا للخصومات.</span><span class="sxs-lookup"><span data-stu-id="488b1-188">The check is done only for rebates.</span></span></p><ul><li><span data-ttu-id="488b1-189">**تطبيق التخفيض:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="488b1-189">**Apply reduction:** *Yes*</span></span></li><li><span data-ttu-id="488b1-190">**أساس التخفيض:** *الخصم*</span><span class="sxs-lookup"><span data-stu-id="488b1-190">**Reduction basis:** *Rebate*</span></span></li><li><span data-ttu-id="488b1-191">**استبعاد من الخفض:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="488b1-191">**Exclude from reduction:** *Yes*</span></span></li></ul> | <span data-ttu-id="488b1-192">1,000 دولار × 15% = 150 دولار</span><span class="sxs-lookup"><span data-stu-id="488b1-192">$1,000 × 15% = $150</span></span> |
| <span data-ttu-id="488b1-193">3</span><span class="sxs-lookup"><span data-stu-id="488b1-193">3</span></span> | <p><span data-ttu-id="488b1-194">يقوم التصنيف بالتحقق من الصفقات الأخرى لأجل التخفيض.</span><span class="sxs-lookup"><span data-stu-id="488b1-194">The classification checks other deals for reductions.</span></span> <span data-ttu-id="488b1-195">يتم اجراء التحقق لكل من التوفيرات والخصومات.</span><span class="sxs-lookup"><span data-stu-id="488b1-195">The check is done for both provisions and rebates.</span></span></p><ul><li><span data-ttu-id="488b1-196">**تطبيق التخفيض:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="488b1-196">**Apply reduction:** *Yes*</span></span></li><li><span data-ttu-id="488b1-197">**أساس التخفيض:** *كلاهما*</span><span class="sxs-lookup"><span data-stu-id="488b1-197">**Reduction basis:** *Both*</span></span></li><li><span data-ttu-id="488b1-198">**استبعاد من الخفض:** *لا*</span><span class="sxs-lookup"><span data-stu-id="488b1-198">**Exclude from reduction:** *No*</span></span></li></ul> | <span data-ttu-id="488b1-199">(1,000 دولار – الصفقة 1) × 20% = 180 دولارًا</span><span class="sxs-lookup"><span data-stu-id="488b1-199">($1,000 – Deal 1) × 20% = $180</span></span> |
| <span data-ttu-id="488b1-200">4</span><span class="sxs-lookup"><span data-stu-id="488b1-200">4</span></span> | <p><span data-ttu-id="488b1-201">يقوم التصنيف بالتحقق من الصفقات الأخرى لأجل التخفيض.</span><span class="sxs-lookup"><span data-stu-id="488b1-201">The classification checks other deals for reductions.</span></span> <span data-ttu-id="488b1-202">يتم اجراء التحقق لكل من التوفيرات والخصومات.</span><span class="sxs-lookup"><span data-stu-id="488b1-202">The check is done for both provisions and rebates.</span></span></p><ul><li><span data-ttu-id="488b1-203">**تطبيق التخفيض:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="488b1-203">**Apply reduction:** *Yes*</span></span></li><li><span data-ttu-id="488b1-204">**أساس التخفيض:** *كلاهما*</span><span class="sxs-lookup"><span data-stu-id="488b1-204">**Reduction basis:** *Both*</span></span></li><li><span data-ttu-id="488b1-205">**استبعاد من الخفض:** *لا*</span><span class="sxs-lookup"><span data-stu-id="488b1-205">**Exclude from reduction:** *No*</span></span></li></ul> | <span data-ttu-id="488b1-206">(1,000 دولار – الصفقة 1 – الصفقة 3) × 25% = 180 دولارًا</span><span class="sxs-lookup"><span data-stu-id="488b1-206">($1,000 – Deal 1 – Deal 3) × 25% = $180</span></span> |

<span data-ttu-id="488b1-207">يعرض الجدول التالي بعض الامثله التي تتم فيها معالجه المخصصات في أوامر مختلفه، التالي يتم تحقيق إجمالي الإجماليات المختلفة.</span><span class="sxs-lookup"><span data-stu-id="488b1-207">The following table shows some examples where the provision is processed in different orders, and where different totals are therefore achieved.</span></span> <span data-ttu-id="488b1-208">ويعتمد الفرق في المخصصات علي الأمر الذي يعالجه النظام العروض في.</span><span class="sxs-lookup"><span data-stu-id="488b1-208">The variance in the provisions depends on the order that the system processes the deals in.</span></span> <span data-ttu-id="488b1-209">ومن المهم ان تفهم كيفيه تاثير ترتيب المعالجة علي مبلغ الخصم النهائي.</span><span class="sxs-lookup"><span data-stu-id="488b1-209">It's important that you understand how the order of processing affects the final rebate amount.</span></span>

| <span data-ttu-id="488b1-210">تسلسل</span><span class="sxs-lookup"><span data-stu-id="488b1-210">Sequence</span></span> | <span data-ttu-id="488b1-211">حساب</span><span class="sxs-lookup"><span data-stu-id="488b1-211">Calculation</span></span> |
|---|---|
| <span data-ttu-id="488b1-212">1</span><span class="sxs-lookup"><span data-stu-id="488b1-212">1</span></span><br><span data-ttu-id="488b1-213">(1، و2، و3، و4)</span><span class="sxs-lookup"><span data-stu-id="488b1-213">(1, 2, 3, 4)</span></span> | <ul><li><span data-ttu-id="488b1-214">**الصفقة 1:** 1,000 دولار × 10% = 100 دولار</span><span class="sxs-lookup"><span data-stu-id="488b1-214">**Deal 1:** $1,000 × 10% = $100</span></span></li><li><span data-ttu-id="488b1-215">**الصفقة 2:** 1,000 دولار × 15% = 150 دولار</span><span class="sxs-lookup"><span data-stu-id="488b1-215">**Deal 2:** $1,000 × 15% = $150</span></span></li><li><span data-ttu-id="488b1-216">**الصفقة 3:** (1,000 دولار – الصفقة 1) × 20% = 180 دولارًا</span><span class="sxs-lookup"><span data-stu-id="488b1-216">**Deal 3:** ($1,000 – Deal 1) × 20% = $180</span></span></li><li><span data-ttu-id="488b1-217">**الصفقة 4:** (1,000 دولار – الصفقة 1 – الصفقة 2) × 25% = 180 دولارًا</span><span class="sxs-lookup"><span data-stu-id="488b1-217">**Deal 4:** ($1,000 – Deal 1 – Deal 2) × 25% = $180</span></span></li><li><span data-ttu-id="488b1-218">**التوفير الإجمالي:** 610 دولارات</span><span class="sxs-lookup"><span data-stu-id="488b1-218">**Total provision:** $610</span></span></li></ul> |
| <span data-ttu-id="488b1-219">2</span><span class="sxs-lookup"><span data-stu-id="488b1-219">2</span></span><br><span data-ttu-id="488b1-220">(4, 3, 2, 1)</span><span class="sxs-lookup"><span data-stu-id="488b1-220">(4, 3, 2, 1)</span></span> | <ul><li><span data-ttu-id="488b1-221">**الصفقة 4:** 1,000 دولار x‏ 25% = 250 دولارًا</span><span class="sxs-lookup"><span data-stu-id="488b1-221">**Deal 4:** $1,000 x 25% = $250</span></span></li><li><span data-ttu-id="488b1-222">**الصفقة 3:** (1,000 دولار – الصفقة 4) × 20% = 150 دولارًا</span><span class="sxs-lookup"><span data-stu-id="488b1-222">**Deal 3:** ($1,000 – Deal 4) × 20% = $150</span></span></li><li><span data-ttu-id="488b1-223">**الصفقة 2:** 1,000 دولار x‏ 15% = 150 دولارًا</span><span class="sxs-lookup"><span data-stu-id="488b1-223">**Deal 2:** $1,000 x 15% = $150</span></span></li><li><span data-ttu-id="488b1-224">**الصفقة 1:** 1,000 دولار x‏ 10% = 100 دولارًا</span><span class="sxs-lookup"><span data-stu-id="488b1-224">**Deal 1:** $1,000 x 10% = $100</span></span></li><li><span data-ttu-id="488b1-225">**التوفير الإجمالي:** 650 دولارات</span><span class="sxs-lookup"><span data-stu-id="488b1-225">**Total provision:** $650</span></span></li></ul> |
| <span data-ttu-id="488b1-226">3</span><span class="sxs-lookup"><span data-stu-id="488b1-226">3</span></span><br><span data-ttu-id="488b1-227">(3, 2, 1, 4)</span><span class="sxs-lookup"><span data-stu-id="488b1-227">(3, 2, 1, 4)</span></span> | <ul><li><span data-ttu-id="488b1-228">**الصفقة 3:** 1,000 دولار x‏ 20% = 200 دولارًا</span><span class="sxs-lookup"><span data-stu-id="488b1-228">**Deal 3:** $1,000 x 20% = $200</span></span></li><li><span data-ttu-id="488b1-229">**الصفقة 2:** 1,000 دولار x‏ 15% = 150 دولارًا</span><span class="sxs-lookup"><span data-stu-id="488b1-229">**Deal 2:** $1,000 x 15% = $150</span></span></li><li><span data-ttu-id="488b1-230">**الصفقة 1:** 1,000 دولار x‏ 10% = 100 دولارًا</span><span class="sxs-lookup"><span data-stu-id="488b1-230">**Deal 1:** $1,000 x 10% = $100</span></span></li><li><span data-ttu-id="488b1-231">**الصفقة 4:** (1,000 دولار – الصفقة 3 – الصفقة 1) × 25% = 175 دولارًا</span><span class="sxs-lookup"><span data-stu-id="488b1-231">**Deal 4:** ($1,000 – Deal 3 – Deal 1) × 25% = $175</span></span></li><li><span data-ttu-id="488b1-232">**التوفير الإجمالي:** 625 دولارات</span><span class="sxs-lookup"><span data-stu-id="488b1-232">**Total provision:** $625</span></span></li></ul> |
| <span data-ttu-id="488b1-233">4</span><span class="sxs-lookup"><span data-stu-id="488b1-233">4</span></span><br><span data-ttu-id="488b1-234">(2, 4, 1, 3)</span><span class="sxs-lookup"><span data-stu-id="488b1-234">(2, 4, 1, 3)</span></span> | <ul><li><span data-ttu-id="488b1-235">**الصفقة 2:** 1,000 دولار × 15% = 150 دولار</span><span class="sxs-lookup"><span data-stu-id="488b1-235">**Deal 2:** $1,000 × 15% = $150</span></span></li><li><span data-ttu-id="488b1-236">**الصفقة 4:** 1,000 دولار × 25% = 250 دولار</span><span class="sxs-lookup"><span data-stu-id="488b1-236">**Deal 4:** $1,000 × 25% = $250</span></span></li><li><span data-ttu-id="488b1-237">**الصفقة 1:** 1,000 دولار × 10% = 100 دولار</span><span class="sxs-lookup"><span data-stu-id="488b1-237">**Deal 1:** $1,000 × 10% = $100</span></span></li><li><span data-ttu-id="488b1-238">**الصفقة 3:** (1,000 دولار – الصفقة 4 – الصفقة 1) × 20% = 130 دولارًا</span><span class="sxs-lookup"><span data-stu-id="488b1-238">**Deal 3:** ($1,000 – Deal 4 – Deal 1) × 20% = $130</span></span></li><li><span data-ttu-id="488b1-239">**التوفير الإجمالي:** 630 دولارات</span><span class="sxs-lookup"><span data-stu-id="488b1-239">**Total provision:** $630</span></span></li></ul> |