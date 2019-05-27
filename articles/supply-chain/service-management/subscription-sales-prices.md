---
title: أسعار مبيعات الاشتراكات
description: عند إنشاء اشتراك، فإن سعر المبيعات يكون مشتقًا من إعداد سعر المبيعات الذي تم إنشاؤه في النموذج سعر المبيعات (اشتراك).
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e18690f7e9b790ecbd0ac0de1955fc95ab1f082
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560679"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="500f7-103">أسعار مبيعات الاشتراكات</span><span class="sxs-lookup"><span data-stu-id="500f7-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="500f7-104">عند إنشاء اشتراك، فإن سعر المبيعات يكون مشتقًا من إعداد سعر المبيعات الذي تم إنشاؤه في النموذج **سعر المبيعات (اشتراك)**.</span><span class="sxs-lookup"><span data-stu-id="500f7-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="500f7-105">في النموذج **سعر المبيعا (اشتراك)**، يمكن إنشاء أسعار مبيعات لاشتراك محدد لو يمكنك إنشاء أسعار مبيعات يتم تطبيقها بشكل أوسع.</span><span class="sxs-lookup"><span data-stu-id="500f7-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="500f7-106">بالنسبة لسعر مبيعات المراد تطبيقه على اشتراك ما، فإنه يجب أن يكون كل من كود الفترة وعملة الاشتراك مماثلا لكود الفترة والعملة لسعر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="500f7-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="500f7-107">إذا كان كل من كود الفترة والعملة متماثلين مع الاشتراك وسعر المبيعات، فإنه يتم تحديد أسعار مبيعات الاشتراك بناءً على قواعد الأولويات الموضحة في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="500f7-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="500f7-108">تشير الخليفة الفارغة في الجدول إلى وجود حقل فارغ وتوضح علامة X قيمة مساوية للقيمة الموجودة في الاشتراك الذي يتم إنشاء الحركة منه.</span><span class="sxs-lookup"><span data-stu-id="500f7-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="500f7-109">الأولوية </span><span class="sxs-lookup"><span data-stu-id="500f7-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="500f7-110"><strong>الفئة</strong></span><span class="sxs-lookup"><span data-stu-id="500f7-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="500f7-111"><strong>معرف المشروع</strong></span><span class="sxs-lookup"><span data-stu-id="500f7-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="500f7-112"><strong>الاشتراك</strong></span><span class="sxs-lookup"><span data-stu-id="500f7-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="500f7-113"><strong>عملة المبيعات</strong></span><span class="sxs-lookup"><span data-stu-id="500f7-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="500f7-114"><strong>كود الفترة</strong></span><span class="sxs-lookup"><span data-stu-id="500f7-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="500f7-115">1</span><span class="sxs-lookup"><span data-stu-id="500f7-115">1</span></span></p></td>
<td><p><span data-ttu-id="500f7-116">س</span><span class="sxs-lookup"><span data-stu-id="500f7-116">X</span></span></p></td>
<td><p><span data-ttu-id="500f7-117">س</span><span class="sxs-lookup"><span data-stu-id="500f7-117">X</span></span></p></td>
<td><p><span data-ttu-id="500f7-118">س</span><span class="sxs-lookup"><span data-stu-id="500f7-118">X</span></span></p></td>
<td><p><span data-ttu-id="500f7-119">س</span><span class="sxs-lookup"><span data-stu-id="500f7-119">X</span></span></p></td>
<td><p><span data-ttu-id="500f7-120">س</span><span class="sxs-lookup"><span data-stu-id="500f7-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="500f7-121">2</span><span class="sxs-lookup"><span data-stu-id="500f7-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="500f7-122">س</span><span class="sxs-lookup"><span data-stu-id="500f7-122">X</span></span></p></td>
<td><p><span data-ttu-id="500f7-123">س</span><span class="sxs-lookup"><span data-stu-id="500f7-123">X</span></span></p></td>
<td><p><span data-ttu-id="500f7-124">س</span><span class="sxs-lookup"><span data-stu-id="500f7-124">X</span></span></p></td>
<td><p><span data-ttu-id="500f7-125">س</span><span class="sxs-lookup"><span data-stu-id="500f7-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="500f7-126">3</span><span class="sxs-lookup"><span data-stu-id="500f7-126">3</span></span></p></td>
<td><p><span data-ttu-id="500f7-127">س</span><span class="sxs-lookup"><span data-stu-id="500f7-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="500f7-128">س</span><span class="sxs-lookup"><span data-stu-id="500f7-128">X</span></span></p></td>
<td><p><span data-ttu-id="500f7-129">س</span><span class="sxs-lookup"><span data-stu-id="500f7-129">X</span></span></p></td>
<td><p><span data-ttu-id="500f7-130">س</span><span class="sxs-lookup"><span data-stu-id="500f7-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="500f7-131">4</span><span class="sxs-lookup"><span data-stu-id="500f7-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="500f7-132">س</span><span class="sxs-lookup"><span data-stu-id="500f7-132">X</span></span></p></td>
<td><p><span data-ttu-id="500f7-133">س</span><span class="sxs-lookup"><span data-stu-id="500f7-133">X</span></span></p></td>
<td><p><span data-ttu-id="500f7-134">س</span><span class="sxs-lookup"><span data-stu-id="500f7-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="500f7-135">5</span><span class="sxs-lookup"><span data-stu-id="500f7-135">5</span></span></p></td>
<td><p><span data-ttu-id="500f7-136">س</span><span class="sxs-lookup"><span data-stu-id="500f7-136">X</span></span></p></td>
<td><p><span data-ttu-id="500f7-137">س</span><span class="sxs-lookup"><span data-stu-id="500f7-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="500f7-138">س</span><span class="sxs-lookup"><span data-stu-id="500f7-138">X</span></span></p></td>
<td><p><span data-ttu-id="500f7-139">س</span><span class="sxs-lookup"><span data-stu-id="500f7-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="500f7-140">6</span><span class="sxs-lookup"><span data-stu-id="500f7-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="500f7-141">س</span><span class="sxs-lookup"><span data-stu-id="500f7-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="500f7-142">س</span><span class="sxs-lookup"><span data-stu-id="500f7-142">X</span></span></p></td>
<td><p><span data-ttu-id="500f7-143">س</span><span class="sxs-lookup"><span data-stu-id="500f7-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="500f7-144">7</span><span class="sxs-lookup"><span data-stu-id="500f7-144">7</span></span></p></td>
<td><p><span data-ttu-id="500f7-145">س</span><span class="sxs-lookup"><span data-stu-id="500f7-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="500f7-146">س</span><span class="sxs-lookup"><span data-stu-id="500f7-146">X</span></span></p></td>
<td><p><span data-ttu-id="500f7-147">س</span><span class="sxs-lookup"><span data-stu-id="500f7-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="500f7-148">8</span><span class="sxs-lookup"><span data-stu-id="500f7-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="500f7-149">س</span><span class="sxs-lookup"><span data-stu-id="500f7-149">X</span></span></p></td>
<td><p><span data-ttu-id="500f7-150">س</span><span class="sxs-lookup"><span data-stu-id="500f7-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="500f7-151">عند إنشاء رسم اشتراك، فإن سعر المبيعات المحتوي على أعلى مستوى من التفاصيل، مثلما هو ملاحظ في الجدول أعلاه، هو الذي يتم تحديده كسعر مبيعات الاشتراك.</span><span class="sxs-lookup"><span data-stu-id="500f7-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="500f7-152">تحديث أسعار مبيعات الاشتراك وفهرستها</span><span class="sxs-lookup"><span data-stu-id="500f7-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="500f7-153">يمكن تحديث سعر مبيعات الاشتراك عن طريق تحديث السعر الأساسي أو الفهرس.</span><span class="sxs-lookup"><span data-stu-id="500f7-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="500f7-154">يمكن التحديث باستخدام نسبة مئوية أو إلى قيمة جديدة.</span><span class="sxs-lookup"><span data-stu-id="500f7-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="500f7-155">أسعار مبيعات رسم الاشتراك</span><span class="sxs-lookup"><span data-stu-id="500f7-155">Subscription fee sales prices</span></span>

<span data-ttu-id="500f7-156">عند إنشاء رسم اشتراك، فإن سعر المبيعات يعتمد على إعداد سعر المبيعات الخاص بالاشتراك.</span><span class="sxs-lookup"><span data-stu-id="500f7-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="500f7-157">من الممكن استخدام السعر الأساسي من إعداد سعر الاشتراك أو إنشاء أسعار مبيعات مفهرسة.</span><span class="sxs-lookup"><span data-stu-id="500f7-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="500f7-158">مثال</span><span class="sxs-lookup"><span data-stu-id="500f7-158">Example</span></span>

<span data-ttu-id="500f7-159">ترغب في إعداد أسعار مبيعات اشتراك بمبلغ 500 ريال سعودي لمشروع جديد 9030.</span><span class="sxs-lookup"><span data-stu-id="500f7-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="500f7-160">في النموذج **سعر المبيعات (الاشتراك)**، عليك إنشاء بند سعر مبيعات اشتراك كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="500f7-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="500f7-161">صالح من</span><span class="sxs-lookup"><span data-stu-id="500f7-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="500f7-162">الفئة</span><span class="sxs-lookup"><span data-stu-id="500f7-162">Category</span></span></p></th>
<th><p><span data-ttu-id="500f7-163">Project</span><span class="sxs-lookup"><span data-stu-id="500f7-163">Project</span></span></p></th>
<th><p><span data-ttu-id="500f7-164">الاشتراك</span><span class="sxs-lookup"><span data-stu-id="500f7-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="500f7-165">كود الفترة</span><span class="sxs-lookup"><span data-stu-id="500f7-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="500f7-166">عملة المبيعات</span><span class="sxs-lookup"><span data-stu-id="500f7-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="500f7-167">سعر المبيعات</span><span class="sxs-lookup"><span data-stu-id="500f7-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="500f7-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="500f7-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="500f7-169">9030</span><span class="sxs-lookup"><span data-stu-id="500f7-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="500f7-170">الشهر</span><span class="sxs-lookup"><span data-stu-id="500f7-170">Month</span></span></p></td>
<td><p><span data-ttu-id="500f7-171">يورو</span><span class="sxs-lookup"><span data-stu-id="500f7-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="500f7-172">500</span><span class="sxs-lookup"><span data-stu-id="500f7-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="500f7-173">لاحظ أن حقلي **الفئة** و**الاشتراك** فارغين.</span><span class="sxs-lookup"><span data-stu-id="500f7-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="500f7-174">عليك بعد ذلك إنشاء الاشتراكات التالية:</span><span class="sxs-lookup"><span data-stu-id="500f7-174">You then create the following subscriptions.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="500f7-175">اشتراك في الخدمة</span><span class="sxs-lookup"><span data-stu-id="500f7-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="500f7-176">Project</span><span class="sxs-lookup"><span data-stu-id="500f7-176">Project</span></span></p></th>
<th><p><span data-ttu-id="500f7-177">مجموعة المشتركين</span><span class="sxs-lookup"><span data-stu-id="500f7-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="500f7-178">الفئة</span><span class="sxs-lookup"><span data-stu-id="500f7-178">Category</span></span></p></th>
<th><p><span data-ttu-id="500f7-179">العملة</span><span class="sxs-lookup"><span data-stu-id="500f7-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="500f7-180">كود الفترة</span><span class="sxs-lookup"><span data-stu-id="500f7-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="500f7-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="500f7-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="500f7-182">9030</span><span class="sxs-lookup"><span data-stu-id="500f7-182">9030</span></span></p></td>
<td><p><span data-ttu-id="500f7-183">الاشتراك 1</span><span class="sxs-lookup"><span data-stu-id="500f7-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="500f7-184">فئة الاشتراك 1</span><span class="sxs-lookup"><span data-stu-id="500f7-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="500f7-185">ريال سعودي</span><span class="sxs-lookup"><span data-stu-id="500f7-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="500f7-186">شهري</span><span class="sxs-lookup"><span data-stu-id="500f7-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="500f7-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="500f7-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="500f7-188">9030</span><span class="sxs-lookup"><span data-stu-id="500f7-188">9030</span></span></p></td>
<td><p><span data-ttu-id="500f7-189">الاشتراك 1</span><span class="sxs-lookup"><span data-stu-id="500f7-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="500f7-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="500f7-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="500f7-191">ريال سعودي</span><span class="sxs-lookup"><span data-stu-id="500f7-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="500f7-192">شهري</span><span class="sxs-lookup"><span data-stu-id="500f7-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="500f7-193">قم الآن بإنشاء رسوم اشتراك للاشتراكين الموجودين في مجموعة الاشتراك Sub1:</span><span class="sxs-lookup"><span data-stu-id="500f7-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="500f7-194">انقر فوق **إدارة الخدمة** \> **إعداد** \> **اشتراكات الخدمة** \> **مجموعات الاشتراك**.</span><span class="sxs-lookup"><span data-stu-id="500f7-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="500f7-195">في نموذج **مجموعات المشتركين**، انقر فوق **الوظيفة** \> **إنشاء رسوم اشتراك**.</span><span class="sxs-lookup"><span data-stu-id="500f7-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="500f7-196">في نموذج **إنشاء رسوم اشتراك**، أدخل المعلومات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="500f7-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="500f7-197">لمزيد من المعلومات، راجع [إنشاء حركات رسوم الاشتراك](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="500f7-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="500f7-198">يتم إنشاء رسوم الاشتراك التي تحتوي على سعر مبيعات 500 يورو للاشتراكات، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="500f7-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="500f7-199">تاريخ المشروع</span><span class="sxs-lookup"><span data-stu-id="500f7-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="500f7-200">اشتراك في الخدمة</span><span class="sxs-lookup"><span data-stu-id="500f7-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="500f7-201">Project</span><span class="sxs-lookup"><span data-stu-id="500f7-201">Project</span></span></p></th>
<th><p><span data-ttu-id="500f7-202">الفئة</span><span class="sxs-lookup"><span data-stu-id="500f7-202">Category</span></span></p></th>
<th><p><span data-ttu-id="500f7-203">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="500f7-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="500f7-204">تاريخ الانتهاء</span><span class="sxs-lookup"><span data-stu-id="500f7-204">End date</span></span></p></th>
<th><p><span data-ttu-id="500f7-205">عملة المبيعات</span><span class="sxs-lookup"><span data-stu-id="500f7-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="500f7-206">سعر المبيعات</span><span class="sxs-lookup"><span data-stu-id="500f7-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="500f7-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="500f7-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="500f7-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="500f7-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="500f7-209">9030</span><span class="sxs-lookup"><span data-stu-id="500f7-209">9030</span></span></p></td>
<td><p><span data-ttu-id="500f7-210">فئة الاشتراك 1</span><span class="sxs-lookup"><span data-stu-id="500f7-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="500f7-211">01-012007-</span><span class="sxs-lookup"><span data-stu-id="500f7-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="500f7-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="500f7-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="500f7-213">ريال سعودي</span><span class="sxs-lookup"><span data-stu-id="500f7-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="500f7-214">500</span><span class="sxs-lookup"><span data-stu-id="500f7-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="500f7-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="500f7-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="500f7-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="500f7-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="500f7-217">9030</span><span class="sxs-lookup"><span data-stu-id="500f7-217">9030</span></span></p></td>
<td><p><span data-ttu-id="500f7-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="500f7-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="500f7-219">01-012007-</span><span class="sxs-lookup"><span data-stu-id="500f7-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="500f7-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="500f7-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="500f7-221">ريال سعودي</span><span class="sxs-lookup"><span data-stu-id="500f7-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="500f7-222">500</span><span class="sxs-lookup"><span data-stu-id="500f7-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="500f7-223">قرر بعد ذلك أنك ترغب في تحديد أسعار مبيعات للفئة SubCat1 في المشروع 9030.</span><span class="sxs-lookup"><span data-stu-id="500f7-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="500f7-224">وبالتالي يمكنك إنشاء بند سعر مبيعات جديد بقيمة 550 يورو للمجموعة المؤلفة من المشروع 9030 وفئة الرسوم SubCat1.</span><span class="sxs-lookup"><span data-stu-id="500f7-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="500f7-225">يوجد الآن بندان جديدان لسعر مبيعات الاشتراك للمشروع 9030، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="500f7-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="500f7-226">صالح من</span><span class="sxs-lookup"><span data-stu-id="500f7-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="500f7-227">الفئة</span><span class="sxs-lookup"><span data-stu-id="500f7-227">Category</span></span></p></th>
<th><p><span data-ttu-id="500f7-228">Project</span><span class="sxs-lookup"><span data-stu-id="500f7-228">Project</span></span></p></th>
<th><p><span data-ttu-id="500f7-229">الاشتراك</span><span class="sxs-lookup"><span data-stu-id="500f7-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="500f7-230">كود الفترة</span><span class="sxs-lookup"><span data-stu-id="500f7-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="500f7-231">العملة</span><span class="sxs-lookup"><span data-stu-id="500f7-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="500f7-232">سعر المبيعات</span><span class="sxs-lookup"><span data-stu-id="500f7-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="500f7-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="500f7-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="500f7-234">9030</span><span class="sxs-lookup"><span data-stu-id="500f7-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="500f7-235">شهر</span><span class="sxs-lookup"><span data-stu-id="500f7-235">Month</span></span></p></td>
<td><p><span data-ttu-id="500f7-236">ريال سعودي</span><span class="sxs-lookup"><span data-stu-id="500f7-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="500f7-237">500</span><span class="sxs-lookup"><span data-stu-id="500f7-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="500f7-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="500f7-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="500f7-239">فئة الاشتراك 1</span><span class="sxs-lookup"><span data-stu-id="500f7-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="500f7-240">9030</span><span class="sxs-lookup"><span data-stu-id="500f7-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="500f7-241">شهر</span><span class="sxs-lookup"><span data-stu-id="500f7-241">Month</span></span></p></td>
<td><p><span data-ttu-id="500f7-242">ريال سعودي</span><span class="sxs-lookup"><span data-stu-id="500f7-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="500f7-243">550</span><span class="sxs-lookup"><span data-stu-id="500f7-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="500f7-244">كرر الإجراء الموضح أعلاه لإنشاء رسوم اشتراك للاشتراكين الموجودين في مجموعة الاشتراك Sub1.</span><span class="sxs-lookup"><span data-stu-id="500f7-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="500f7-245">يوضح الجدول التالي الحركات التي تم إنشائها لكل اشتراك ويتم إرفاق كل منها بمجموعة الاشتراك.</span><span class="sxs-lookup"><span data-stu-id="500f7-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="500f7-246">تاريخ المشروع</span><span class="sxs-lookup"><span data-stu-id="500f7-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="500f7-247">الاشتراك</span><span class="sxs-lookup"><span data-stu-id="500f7-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="500f7-248">Project</span><span class="sxs-lookup"><span data-stu-id="500f7-248">Project</span></span></p></th>
<th><p><span data-ttu-id="500f7-249">الفئة</span><span class="sxs-lookup"><span data-stu-id="500f7-249">Category</span></span></p></th>
<th><p><span data-ttu-id="500f7-250">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="500f7-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="500f7-251">تاريخ الإنهاء</span><span class="sxs-lookup"><span data-stu-id="500f7-251">End date</span></span></p></th>
<th><p><span data-ttu-id="500f7-252">عملة المبيعات</span><span class="sxs-lookup"><span data-stu-id="500f7-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="500f7-253">سعر المبيعات</span><span class="sxs-lookup"><span data-stu-id="500f7-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="500f7-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="500f7-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="500f7-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="500f7-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="500f7-256">9030</span><span class="sxs-lookup"><span data-stu-id="500f7-256">9030</span></span></p></td>
<td><p><span data-ttu-id="500f7-257">فئة الاشتراك 1</span><span class="sxs-lookup"><span data-stu-id="500f7-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="500f7-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="500f7-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="500f7-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="500f7-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="500f7-260">ريال سعودي</span><span class="sxs-lookup"><span data-stu-id="500f7-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="500f7-261">550</span><span class="sxs-lookup"><span data-stu-id="500f7-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="500f7-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="500f7-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="500f7-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="500f7-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="500f7-264">9030</span><span class="sxs-lookup"><span data-stu-id="500f7-264">9030</span></span></p></td>
<td><p><span data-ttu-id="500f7-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="500f7-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="500f7-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="500f7-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="500f7-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="500f7-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="500f7-268">يورو</span><span class="sxs-lookup"><span data-stu-id="500f7-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="500f7-269">500</span><span class="sxs-lookup"><span data-stu-id="500f7-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="500f7-270">في الحركة الأولى للاشتراك 00020\_135 يُشتق سعر المبيعات بقيمة 550 يورو من سعر مبيعات الاشتراك الذي تم إعداده لمجموعة معينة من المشروع والفئة.</span><span class="sxs-lookup"><span data-stu-id="500f7-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="500f7-271">في الحركة الثانية للاشتراك 00021\_135 سعر المبيعات بقيمة 500 يورو يستخدم كسعر مبيعات الاشتراك للمشروع وذلك لعدم وجود أي سعر تم إعداده لمجموعة المشروع 9030 والفئة SubCat2.</span><span class="sxs-lookup"><span data-stu-id="500f7-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="500f7-272">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="500f7-272">See also</span></span>

[<span data-ttu-id="500f7-273">تحديث أسعار مبيعات الاشتراك وفهرستها</span><span class="sxs-lookup"><span data-stu-id="500f7-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


