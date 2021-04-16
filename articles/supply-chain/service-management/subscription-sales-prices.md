---
title: أسعار مبيعات الاشتراكات
description: عند إنشاء اشتراك، فإن سعر المبيعات يكون مشتقًا من إعداد سعر المبيعات الذي تم إنشاؤه في النموذج سعر المبيعات (اشتراك).
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b4b02af0a535e67818751c437482c3663524474
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817403"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="14b38-103">أسعار مبيعات الاشتراكات</span><span class="sxs-lookup"><span data-stu-id="14b38-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="14b38-104">عند إنشاء اشتراك، فإن سعر المبيعات يكون مشتقًا من إعداد سعر المبيعات الذي تم إنشاؤه في النموذج **سعر المبيعات (اشتراك)**.</span><span class="sxs-lookup"><span data-stu-id="14b38-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="14b38-105">في النموذج **سعر المبيعا (اشتراك)**، يمكن إنشاء أسعار مبيعات لاشتراك محدد لو يمكنك إنشاء أسعار مبيعات يتم تطبيقها بشكل أوسع.</span><span class="sxs-lookup"><span data-stu-id="14b38-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="14b38-106">بالنسبة لسعر مبيعات المراد تطبيقه على اشتراك ما، فإنه يجب أن يكون كل من كود الفترة وعملة الاشتراك مماثلا لكود الفترة والعملة لسعر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="14b38-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="14b38-107">إذا كان كل من كود الفترة والعملة متماثلين مع الاشتراك وسعر المبيعات، فإنه يتم تحديد أسعار مبيعات الاشتراك بناءً على قواعد الأولويات الموضحة في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="14b38-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="14b38-108">تشير الخليفة الفارغة في الجدول إلى وجود حقل فارغ وتوضح علامة X قيمة مساوية للقيمة الموجودة في الاشتراك الذي يتم إنشاء الحركة منه.</span><span class="sxs-lookup"><span data-stu-id="14b38-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="14b38-109">الأولوية </span><span class="sxs-lookup"><span data-stu-id="14b38-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="14b38-110"><strong>الفئة</strong></span><span class="sxs-lookup"><span data-stu-id="14b38-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="14b38-111"><strong>معرف المشروع</strong></span><span class="sxs-lookup"><span data-stu-id="14b38-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="14b38-112"><strong>الاشتراك</strong></span><span class="sxs-lookup"><span data-stu-id="14b38-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="14b38-113"><strong>عملة المبيعات</strong></span><span class="sxs-lookup"><span data-stu-id="14b38-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="14b38-114"><strong>كود الفترة</strong></span><span class="sxs-lookup"><span data-stu-id="14b38-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14b38-115">1</span><span class="sxs-lookup"><span data-stu-id="14b38-115">1</span></span></p></td>
<td><p><span data-ttu-id="14b38-116">س</span><span class="sxs-lookup"><span data-stu-id="14b38-116">X</span></span></p></td>
<td><p><span data-ttu-id="14b38-117">س</span><span class="sxs-lookup"><span data-stu-id="14b38-117">X</span></span></p></td>
<td><p><span data-ttu-id="14b38-118">س</span><span class="sxs-lookup"><span data-stu-id="14b38-118">X</span></span></p></td>
<td><p><span data-ttu-id="14b38-119">س</span><span class="sxs-lookup"><span data-stu-id="14b38-119">X</span></span></p></td>
<td><p><span data-ttu-id="14b38-120">س</span><span class="sxs-lookup"><span data-stu-id="14b38-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14b38-121">2</span><span class="sxs-lookup"><span data-stu-id="14b38-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14b38-122">س</span><span class="sxs-lookup"><span data-stu-id="14b38-122">X</span></span></p></td>
<td><p><span data-ttu-id="14b38-123">س</span><span class="sxs-lookup"><span data-stu-id="14b38-123">X</span></span></p></td>
<td><p><span data-ttu-id="14b38-124">س</span><span class="sxs-lookup"><span data-stu-id="14b38-124">X</span></span></p></td>
<td><p><span data-ttu-id="14b38-125">س</span><span class="sxs-lookup"><span data-stu-id="14b38-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14b38-126">3</span><span class="sxs-lookup"><span data-stu-id="14b38-126">3</span></span></p></td>
<td><p><span data-ttu-id="14b38-127">س</span><span class="sxs-lookup"><span data-stu-id="14b38-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14b38-128">س</span><span class="sxs-lookup"><span data-stu-id="14b38-128">X</span></span></p></td>
<td><p><span data-ttu-id="14b38-129">س</span><span class="sxs-lookup"><span data-stu-id="14b38-129">X</span></span></p></td>
<td><p><span data-ttu-id="14b38-130">س</span><span class="sxs-lookup"><span data-stu-id="14b38-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14b38-131">4</span><span class="sxs-lookup"><span data-stu-id="14b38-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14b38-132">س</span><span class="sxs-lookup"><span data-stu-id="14b38-132">X</span></span></p></td>
<td><p><span data-ttu-id="14b38-133">س</span><span class="sxs-lookup"><span data-stu-id="14b38-133">X</span></span></p></td>
<td><p><span data-ttu-id="14b38-134">س</span><span class="sxs-lookup"><span data-stu-id="14b38-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14b38-135">5</span><span class="sxs-lookup"><span data-stu-id="14b38-135">5</span></span></p></td>
<td><p><span data-ttu-id="14b38-136">س</span><span class="sxs-lookup"><span data-stu-id="14b38-136">X</span></span></p></td>
<td><p><span data-ttu-id="14b38-137">س</span><span class="sxs-lookup"><span data-stu-id="14b38-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14b38-138">س</span><span class="sxs-lookup"><span data-stu-id="14b38-138">X</span></span></p></td>
<td><p><span data-ttu-id="14b38-139">س</span><span class="sxs-lookup"><span data-stu-id="14b38-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14b38-140">6</span><span class="sxs-lookup"><span data-stu-id="14b38-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14b38-141">س</span><span class="sxs-lookup"><span data-stu-id="14b38-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14b38-142">س</span><span class="sxs-lookup"><span data-stu-id="14b38-142">X</span></span></p></td>
<td><p><span data-ttu-id="14b38-143">س</span><span class="sxs-lookup"><span data-stu-id="14b38-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14b38-144">7</span><span class="sxs-lookup"><span data-stu-id="14b38-144">7</span></span></p></td>
<td><p><span data-ttu-id="14b38-145">س</span><span class="sxs-lookup"><span data-stu-id="14b38-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14b38-146">س</span><span class="sxs-lookup"><span data-stu-id="14b38-146">X</span></span></p></td>
<td><p><span data-ttu-id="14b38-147">س</span><span class="sxs-lookup"><span data-stu-id="14b38-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14b38-148">8</span><span class="sxs-lookup"><span data-stu-id="14b38-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="14b38-149">س</span><span class="sxs-lookup"><span data-stu-id="14b38-149">X</span></span></p></td>
<td><p><span data-ttu-id="14b38-150">س</span><span class="sxs-lookup"><span data-stu-id="14b38-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="14b38-151">عند إنشاء رسم اشتراك، فإن سعر المبيعات المحتوي على أعلى مستوى من التفاصيل، مثلما هو ملاحظ في الجدول أعلاه، هو الذي يتم تحديده كسعر مبيعات الاشتراك.</span><span class="sxs-lookup"><span data-stu-id="14b38-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="14b38-152">تحديث أسعار مبيعات الاشتراك وفهرستها</span><span class="sxs-lookup"><span data-stu-id="14b38-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="14b38-153">يمكن تحديث سعر مبيعات الاشتراك عن طريق تحديث السعر الأساسي أو الفهرس.</span><span class="sxs-lookup"><span data-stu-id="14b38-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="14b38-154">يمكن التحديث باستخدام نسبة مئوية أو إلى قيمة جديدة.</span><span class="sxs-lookup"><span data-stu-id="14b38-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="14b38-155">أسعار مبيعات رسم الاشتراك</span><span class="sxs-lookup"><span data-stu-id="14b38-155">Subscription fee sales prices</span></span>

<span data-ttu-id="14b38-156">عند إنشاء رسم اشتراك، فإن سعر المبيعات يعتمد على إعداد سعر المبيعات الخاص بالاشتراك.</span><span class="sxs-lookup"><span data-stu-id="14b38-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="14b38-157">من الممكن استخدام السعر الأساسي من إعداد سعر الاشتراك أو إنشاء أسعار مبيعات مفهرسة.</span><span class="sxs-lookup"><span data-stu-id="14b38-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="14b38-158">مثال</span><span class="sxs-lookup"><span data-stu-id="14b38-158">Example</span></span>

<span data-ttu-id="14b38-159">ترغب في إعداد أسعار مبيعات اشتراك بمبلغ 500 ريال سعودي لمشروع جديد 9030.</span><span class="sxs-lookup"><span data-stu-id="14b38-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="14b38-160">في النموذج **سعر المبيعات (الاشتراك)**، عليك إنشاء بند سعر مبيعات اشتراك كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="14b38-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="14b38-161">صالح من</span><span class="sxs-lookup"><span data-stu-id="14b38-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="14b38-162">الفئة</span><span class="sxs-lookup"><span data-stu-id="14b38-162">Category</span></span></p></th>
<th><p><span data-ttu-id="14b38-163">Project</span><span class="sxs-lookup"><span data-stu-id="14b38-163">Project</span></span></p></th>
<th><p><span data-ttu-id="14b38-164">الاشتراك</span><span class="sxs-lookup"><span data-stu-id="14b38-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="14b38-165">كود الفترة</span><span class="sxs-lookup"><span data-stu-id="14b38-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="14b38-166">عملة المبيعات</span><span class="sxs-lookup"><span data-stu-id="14b38-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="14b38-167">سعر المبيعات</span><span class="sxs-lookup"><span data-stu-id="14b38-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14b38-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="14b38-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="14b38-169">9030</span><span class="sxs-lookup"><span data-stu-id="14b38-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="14b38-170">الشهر</span><span class="sxs-lookup"><span data-stu-id="14b38-170">Month</span></span></p></td>
<td><p><span data-ttu-id="14b38-171">يورو</span><span class="sxs-lookup"><span data-stu-id="14b38-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="14b38-172">500</span><span class="sxs-lookup"><span data-stu-id="14b38-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="14b38-173">لاحظ أن حقلي **الفئة** و **الاشتراك** فارغين.</span><span class="sxs-lookup"><span data-stu-id="14b38-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="14b38-174">عليك بعد ذلك إنشاء الاشتراكات التالية:</span><span class="sxs-lookup"><span data-stu-id="14b38-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="14b38-175">اشتراك في الخدمة</span><span class="sxs-lookup"><span data-stu-id="14b38-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="14b38-176">Project</span><span class="sxs-lookup"><span data-stu-id="14b38-176">Project</span></span></p></th>
<th><p><span data-ttu-id="14b38-177">مجموعة المشتركين</span><span class="sxs-lookup"><span data-stu-id="14b38-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="14b38-178">الفئة</span><span class="sxs-lookup"><span data-stu-id="14b38-178">Category</span></span></p></th>
<th><p><span data-ttu-id="14b38-179">العملة</span><span class="sxs-lookup"><span data-stu-id="14b38-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="14b38-180">كود الفترة</span><span class="sxs-lookup"><span data-stu-id="14b38-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14b38-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="14b38-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="14b38-182">9030</span><span class="sxs-lookup"><span data-stu-id="14b38-182">9030</span></span></p></td>
<td><p><span data-ttu-id="14b38-183">الاشتراك 1</span><span class="sxs-lookup"><span data-stu-id="14b38-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="14b38-184">فئة الاشتراك 1</span><span class="sxs-lookup"><span data-stu-id="14b38-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="14b38-185">ريال سعودي</span><span class="sxs-lookup"><span data-stu-id="14b38-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="14b38-186">شهري</span><span class="sxs-lookup"><span data-stu-id="14b38-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14b38-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="14b38-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="14b38-188">9030</span><span class="sxs-lookup"><span data-stu-id="14b38-188">9030</span></span></p></td>
<td><p><span data-ttu-id="14b38-189">الاشتراك 1</span><span class="sxs-lookup"><span data-stu-id="14b38-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="14b38-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="14b38-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="14b38-191">ريال سعودي</span><span class="sxs-lookup"><span data-stu-id="14b38-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="14b38-192">شهري</span><span class="sxs-lookup"><span data-stu-id="14b38-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="14b38-193">قم الآن بإنشاء رسوم اشتراك للاشتراكين الموجودين في مجموعة الاشتراك Sub1:</span><span class="sxs-lookup"><span data-stu-id="14b38-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="14b38-194">انقر فوق **إدارة الخدمة** \> **إعداد** \> **اشتراكات الخدمة** \> **مجموعات الاشتراك**.</span><span class="sxs-lookup"><span data-stu-id="14b38-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="14b38-195">في نموذج **مجموعات المشتركين**، انقر فوق **الوظيفة** \> **إنشاء رسوم اشتراك**.</span><span class="sxs-lookup"><span data-stu-id="14b38-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="14b38-196">في نموذج **إنشاء رسوم اشتراك**، أدخل المعلومات المناسبة.</span><span class="sxs-lookup"><span data-stu-id="14b38-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="14b38-197">لمزيد من المعلومات، راجع [إنشاء حركات رسوم الاشتراك](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="14b38-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="14b38-198">يتم إنشاء رسوم الاشتراك التي تحتوي على سعر مبيعات 500 يورو للاشتراكات، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="14b38-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="14b38-199">تاريخ المشروع</span><span class="sxs-lookup"><span data-stu-id="14b38-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="14b38-200">اشتراك في الخدمة</span><span class="sxs-lookup"><span data-stu-id="14b38-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="14b38-201">Project</span><span class="sxs-lookup"><span data-stu-id="14b38-201">Project</span></span></p></th>
<th><p><span data-ttu-id="14b38-202">الفئة</span><span class="sxs-lookup"><span data-stu-id="14b38-202">Category</span></span></p></th>
<th><p><span data-ttu-id="14b38-203">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="14b38-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="14b38-204">تاريخ الانتهاء</span><span class="sxs-lookup"><span data-stu-id="14b38-204">End date</span></span></p></th>
<th><p><span data-ttu-id="14b38-205">عملة المبيعات</span><span class="sxs-lookup"><span data-stu-id="14b38-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="14b38-206">سعر المبيعات</span><span class="sxs-lookup"><span data-stu-id="14b38-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14b38-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="14b38-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="14b38-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="14b38-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="14b38-209">9030</span><span class="sxs-lookup"><span data-stu-id="14b38-209">9030</span></span></p></td>
<td><p><span data-ttu-id="14b38-210">فئة الاشتراك 1</span><span class="sxs-lookup"><span data-stu-id="14b38-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="14b38-211">01-012007-</span><span class="sxs-lookup"><span data-stu-id="14b38-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="14b38-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="14b38-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="14b38-213">ريال سعودي</span><span class="sxs-lookup"><span data-stu-id="14b38-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="14b38-214">500</span><span class="sxs-lookup"><span data-stu-id="14b38-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14b38-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="14b38-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="14b38-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="14b38-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="14b38-217">9030</span><span class="sxs-lookup"><span data-stu-id="14b38-217">9030</span></span></p></td>
<td><p><span data-ttu-id="14b38-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="14b38-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="14b38-219">01-012007-</span><span class="sxs-lookup"><span data-stu-id="14b38-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="14b38-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="14b38-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="14b38-221">ريال سعودي</span><span class="sxs-lookup"><span data-stu-id="14b38-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="14b38-222">500</span><span class="sxs-lookup"><span data-stu-id="14b38-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="14b38-223">قرر بعد ذلك أنك ترغب في تحديد أسعار مبيعات للفئة SubCat1 في المشروع 9030.</span><span class="sxs-lookup"><span data-stu-id="14b38-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="14b38-224">وبالتالي يمكنك إنشاء بند سعر مبيعات جديد بقيمة 550 يورو للمجموعة المؤلفة من المشروع 9030 وفئة الرسوم SubCat1.</span><span class="sxs-lookup"><span data-stu-id="14b38-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="14b38-225">يوجد الآن بندان جديدان لسعر مبيعات الاشتراك للمشروع 9030، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="14b38-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="14b38-226">صالح من</span><span class="sxs-lookup"><span data-stu-id="14b38-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="14b38-227">الفئة</span><span class="sxs-lookup"><span data-stu-id="14b38-227">Category</span></span></p></th>
<th><p><span data-ttu-id="14b38-228">Project</span><span class="sxs-lookup"><span data-stu-id="14b38-228">Project</span></span></p></th>
<th><p><span data-ttu-id="14b38-229">الاشتراك</span><span class="sxs-lookup"><span data-stu-id="14b38-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="14b38-230">كود الفترة</span><span class="sxs-lookup"><span data-stu-id="14b38-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="14b38-231">العملة</span><span class="sxs-lookup"><span data-stu-id="14b38-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="14b38-232">سعر المبيعات</span><span class="sxs-lookup"><span data-stu-id="14b38-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14b38-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="14b38-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="14b38-234">9030</span><span class="sxs-lookup"><span data-stu-id="14b38-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="14b38-235">شهر</span><span class="sxs-lookup"><span data-stu-id="14b38-235">Month</span></span></p></td>
<td><p><span data-ttu-id="14b38-236">ريال سعودي</span><span class="sxs-lookup"><span data-stu-id="14b38-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="14b38-237">500</span><span class="sxs-lookup"><span data-stu-id="14b38-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14b38-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="14b38-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="14b38-239">فئة الاشتراك 1</span><span class="sxs-lookup"><span data-stu-id="14b38-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="14b38-240">9030</span><span class="sxs-lookup"><span data-stu-id="14b38-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="14b38-241">شهر</span><span class="sxs-lookup"><span data-stu-id="14b38-241">Month</span></span></p></td>
<td><p><span data-ttu-id="14b38-242">ريال سعودي</span><span class="sxs-lookup"><span data-stu-id="14b38-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="14b38-243">550</span><span class="sxs-lookup"><span data-stu-id="14b38-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="14b38-244">كرر الإجراء الموضح أعلاه لإنشاء رسوم اشتراك للاشتراكين الموجودين في مجموعة الاشتراك Sub1.</span><span class="sxs-lookup"><span data-stu-id="14b38-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="14b38-245">يوضح الجدول التالي الحركات التي تم إنشائها لكل اشتراك ويتم إرفاق كل منها بمجموعة الاشتراك.</span><span class="sxs-lookup"><span data-stu-id="14b38-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="14b38-246">تاريخ المشروع</span><span class="sxs-lookup"><span data-stu-id="14b38-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="14b38-247">الاشتراك</span><span class="sxs-lookup"><span data-stu-id="14b38-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="14b38-248">Project</span><span class="sxs-lookup"><span data-stu-id="14b38-248">Project</span></span></p></th>
<th><p><span data-ttu-id="14b38-249">الفئة</span><span class="sxs-lookup"><span data-stu-id="14b38-249">Category</span></span></p></th>
<th><p><span data-ttu-id="14b38-250">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="14b38-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="14b38-251">تاريخ الإنهاء</span><span class="sxs-lookup"><span data-stu-id="14b38-251">End date</span></span></p></th>
<th><p><span data-ttu-id="14b38-252">عملة المبيعات</span><span class="sxs-lookup"><span data-stu-id="14b38-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="14b38-253">سعر المبيعات</span><span class="sxs-lookup"><span data-stu-id="14b38-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14b38-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="14b38-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="14b38-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="14b38-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="14b38-256">9030</span><span class="sxs-lookup"><span data-stu-id="14b38-256">9030</span></span></p></td>
<td><p><span data-ttu-id="14b38-257">فئة الاشتراك 1</span><span class="sxs-lookup"><span data-stu-id="14b38-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="14b38-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="14b38-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="14b38-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="14b38-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="14b38-260">ريال سعودي</span><span class="sxs-lookup"><span data-stu-id="14b38-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="14b38-261">550</span><span class="sxs-lookup"><span data-stu-id="14b38-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14b38-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="14b38-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="14b38-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="14b38-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="14b38-264">9030</span><span class="sxs-lookup"><span data-stu-id="14b38-264">9030</span></span></p></td>
<td><p><span data-ttu-id="14b38-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="14b38-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="14b38-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="14b38-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="14b38-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="14b38-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="14b38-268">يورو</span><span class="sxs-lookup"><span data-stu-id="14b38-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="14b38-269">500</span><span class="sxs-lookup"><span data-stu-id="14b38-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="14b38-270">في الحركة الأولى للاشتراك 00020\_135 يُشتق سعر المبيعات بقيمة 550 يورو من سعر مبيعات الاشتراك الذي تم إعداده لمجموعة معينة من المشروع والفئة.</span><span class="sxs-lookup"><span data-stu-id="14b38-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="14b38-271">في الحركة الثانية للاشتراك 00021\_135 سعر المبيعات بقيمة 500 يورو يستخدم كسعر مبيعات الاشتراك للمشروع وذلك لعدم وجود أي سعر تم إعداده لمجموعة المشروع 9030 والفئة SubCat2.</span><span class="sxs-lookup"><span data-stu-id="14b38-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="14b38-272">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="14b38-272">See also</span></span>

[<span data-ttu-id="14b38-273">تحديث أسعار مبيعات الاشتراك وفهرستها</span><span class="sxs-lookup"><span data-stu-id="14b38-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]