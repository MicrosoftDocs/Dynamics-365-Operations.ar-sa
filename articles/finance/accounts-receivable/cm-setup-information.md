---
title: إعداد إدارة الائتمان‬
description: يصف هذا الموضوع الإعداد المطلوب لإدارة الائتمان.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 65b1d1a232558efbe05e83d51706a78b12439e47
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124129"
---
# <a name="credit-management-setup"></a><span data-ttu-id="d2dd8-103">إعداد إدارة الائتمان‬</span><span class="sxs-lookup"><span data-stu-id="d2dd8-103">Credit management setup</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="credit-management-workflows"></a><span data-ttu-id="d2dd8-104">عمليات سير عمل إدارة الائتمان</span><span class="sxs-lookup"><span data-stu-id="d2dd8-104">Credit management workflows</span></span>

<span data-ttu-id="d2dd8-105">انتقل إلى **عمليات التحصيل والائتمان‬ \> الإعداد \> عمليات سير عمل إدارة الائتمان** لتعريف عمليات سير العمل المستخدمة لإدارة تسويات الحدود الائتمانية.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-105">Go to **Credit and collections \> Setup \> Credit management workflows** to define the workflows that are used to manage credit limit adjustments.</span></span>

- <span data-ttu-id="d2dd8-106">يمكنك إنشاء سير عمل يتيح لك الموافقة على دُفعة من تسويات الحدود الائتمانية من خلال موافقة واحدة.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-106">You can create a workflow that lets you approve a batch of credit limits adjustments through a single approval.</span></span>
- <span data-ttu-id="d2dd8-107">يمكنك إضافة سير عمل على مستوى البنود، بحيث يمكن الموافقة على تسويات الحدود الائتمانية بشكل فردي..</span><span class="sxs-lookup"><span data-stu-id="d2dd8-107">You can add a workflow at the line level, so that credit limit adjustments can be approved individually.</span></span>
- <span data-ttu-id="d2dd8-108">يمكنك إنشاء سير عمل لتحرير أمر المبيعات يقوم بشكل تلقائي بتوجيه حالات التعليق إلى عملية سير عمل.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-108">You can create a release workflow that automatically routes holds to a workflow process.</span></span>

## <a name="blocking-rules"></a><span data-ttu-id="d2dd8-109">قواعد الحظر</span><span class="sxs-lookup"><span data-stu-id="d2dd8-109">Blocking rules</span></span>

### <a name="ranking-payment-terms"></a><span data-ttu-id="d2dd8-110">تصنيف شروط الدفع</span><span class="sxs-lookup"><span data-stu-id="d2dd8-110">Ranking payment terms</span></span>

<span data-ttu-id="d2dd8-111">يمكنك وضع أمر مبيعات قيد التعليق إذا لم تتطابق شروط الدفع على أمر المبيعات مع شروط الدفع الافتراضية الخاصة بالعميل.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-111">You can put a sales order on hold if the payment terms on the order don't match the default payment terms for the customer.</span></span> <span data-ttu-id="d2dd8-112">ومع ذلك، فإن شروط الدفع قد تختلف في بعض الأحيان ولكنها مماثلة بشكل كافٍ بحيث لا تريد وضع أمر المبيعات قيد التعليق.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-112">However, sometimes the payment terms differ but are similar enough that you don't want to put the order on hold.</span></span> <span data-ttu-id="d2dd8-113">يمكنك تصنيف شروط الدفع بحيث يكون لبعضها المرتبة نفسها، في حين تكون شروط دفع أخرى ذات مرتبة أعلى و اقل.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-113">You can rank payment terms so that some of them have the same rank, whereas others have a higher or lower rank.</span></span>

<span data-ttu-id="d2dd8-114">إذا كانت تصنيفات شروط الدفع نشطة، فستوضع أوامر المبيعات قيد التعليق إذا كانت شروط الدفع على أمر المبيعات ذات ترتيب أعلى من شروط الدفع الافتراضية الخاصة بالعميل.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-114">If the rankings for payment terms are active, the sales orders will be put on hold if the payment terms on the order have a higher rank than the default payment terms for the customer.</span></span>

### <a name="ranking-settlement-discounts"></a><span data-ttu-id="d2dd8-115">تصنيف خصومات التسوية</span><span class="sxs-lookup"><span data-stu-id="d2dd8-115">Ranking settlement discounts</span></span>

<span data-ttu-id="d2dd8-116">يمكنك وضع أمر مبيعات قيد التعليق إذا لم يتطابق الخصم النقدي على أمر المبيعات مع الخصم النقدي الافتراضي الخاص بالعميل.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-116">You can put a sales order on hold if the cash discount on the order doesn't match the default cash discount for the customer.</span></span> <span data-ttu-id="d2dd8-117">ومع ذلك، فإن الخصومات النقدية قد تختلف في بعض الأحيان ولكنها مماثلة بشكل كافٍ بحيث لا تريد وضع أمر المبيعات قيد التعليق.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-117">However, sometimes the cash discounts differ but are similar enough that you don't want to put the order on hold.</span></span> <span data-ttu-id="d2dd8-118">يمكنك تصنيف الخصومات النقدية بحيث يكون لبعضها المرتبة نفسها، في حين تكون خصومات نقدية أخرى ذات مرتبة أعلى و اقل.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-118">You can rank cash discounts so that some of them have the same rank, whereas others have a higher or lower rank.</span></span>

<span data-ttu-id="d2dd8-119">إذا كانت تصنيفات خصومات التسوية نشطة، فستوضع أوامر المبيعات قيد التعليق إذا كان الخصم النقدي على أمر المبيعات ذو ترتيب أعلى من الخصم النقدي الافتراضي الخاص بالعميل.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-119">If rankings for settlement discounts are active, the sales orders will be put on hold if the cash discount on the order has a higher rank than the default cash discount for the customer.</span></span>

## <a name="reasons"></a><span data-ttu-id="d2dd8-120">الأسباب</span><span class="sxs-lookup"><span data-stu-id="d2dd8-120">Reasons</span></span>

<span data-ttu-id="d2dd8-121">تُستخدم أنواع أسباب متعددة في إدارة الائتمان:</span><span class="sxs-lookup"><span data-stu-id="d2dd8-121">Several types of reasons are used in Credit management:</span></span>

- <span data-ttu-id="d2dd8-122">تشير أسباب الوضع قيد التعليق إلى سبب وضع أمر المبيعات قيد التعليق.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-122">Hold reasons indicate why a sales order was put on hold.</span></span>
- <span data-ttu-id="d2dd8-123">يتم تعيين أسباب التحرير إلى أمر مبيعات عند تحريره من الوضع قيد التعليق.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-123">Release reasons are assigned to an order when it's released from hold.</span></span>
- <span data-ttu-id="d2dd8-124">تشير أسباب الحالة إلى سبب تعيين حالة حساب إلى عميل.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-124">Status reasons indicate why an account status was assigned to a customer.</span></span>

<span data-ttu-id="d2dd8-125">يمكنك إعداد الأسباب في صفحة **أسباب إدارة الائتمان** (**إدارة الائتمان \> الإعداد \> إدارة الائتمان \> أسباب إدارة الائتمان**).</span><span class="sxs-lookup"><span data-stu-id="d2dd8-125">You can set up reasons on the **Credit management reasons** page (**Credit management \> Setup \> Credit management \> Credit management reasons**).</span></span>

1. <span data-ttu-id="d2dd8-126">في حقل **نوع السبب**، حدد نوع السبب: **قيد التعليق** أو **تحرير** أو **الحالة**.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-126">In the **Reason type** field, select the type of reason: **Hold**, **Release**, or **Status**.</span></span>
2. <span data-ttu-id="d2dd8-127">في حقل **السبب**، أدخل اسمًا للسبب.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-127">In the **Reason** field, enter a name for the reason.</span></span>
3. <span data-ttu-id="d2dd8-128">في الحقل **الوصف**، أخل وصفًا لرمز السبب.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-128">In the **Description** field, enter a description of the reason code.</span></span>

## <a name="credit-management-groups"></a><span data-ttu-id="d2dd8-129">مجموعات إدارة الائتمان</span><span class="sxs-lookup"><span data-stu-id="d2dd8-129">Credit management groups</span></span>

<span data-ttu-id="d2dd8-130">يتم استخدام مجموعات إدارة الائتمان لتحديد العملاء أو مجموعات العملاء الذين لديهم الخصائص نفسها لإدارة الائتمان.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-130">Credit management groups are used to identify customers or groups of customers that have the same credit management properties.</span></span> <span data-ttu-id="d2dd8-131">على سبيل المثال، يمكن استخدام مجموعات إدارة الائتمان لتحديد قواعد الحظر والاستثناء لإدارة الائتمان للعملاء.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-131">For example, credit management groups can be used to determine the blocking and exclusion credit management rules for customers.</span></span>

<span data-ttu-id="d2dd8-132">يمكنك إنشاء مجموعات إدارة الائتمان في صفحة **مجموعات إدارة الائتمان** (**إدارة الائتمان \> الإعداد> إعداد المجموعات \> مجموعات إدارة الائتمان**).</span><span class="sxs-lookup"><span data-stu-id="d2dd8-132">You can create credit management groups on the **Credit management groups** page (**Credit management \> Setup> Groups setup \> Credit management groups**).</span></span>

1. <span data-ttu-id="d2dd8-133">حدد **جديد** لإنشاء بند.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-133">Select **New** to create a line.</span></span>
2. <span data-ttu-id="d2dd8-134">أدخل معرف للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-134">Enter an ID for the group.</span></span> <span data-ttu-id="d2dd8-135">يتكون المعرف من 10 أحرف كحدٍ أقصى.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-135">The ID can have up to 10 characters.</span></span>
3. <span data-ttu-id="d2dd8-136">في حقل **الوصف**، أدخل اسمًا للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-136">In the **Description** field, enter a name for the group.</span></span> <span data-ttu-id="d2dd8-137">يتكون الاسم من 60 أحرف كحدٍ أقصى.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-137">The name can have up to 60 characters.</span></span>

<span data-ttu-id="d2dd8-138">يتم تعيين مجموعة إدارة الائتمان إلى عميل في علامة التبويب السريعة **عمليات التحصيل والائتمان‬** في صفحة **كافة العملاء‬** (**الحسابات المدينة \> العملاء \> كافة العملاء‬**).</span><span class="sxs-lookup"><span data-stu-id="d2dd8-138">The credit management group is assigned to a customer on the **Credit and collections** FastTab of the **All customers** page (**Account receivable \> Customers \> All customers**).</span></span>

## <a name="account-statuses"></a><span data-ttu-id="d2dd8-139">حالات الحساب</span><span class="sxs-lookup"><span data-stu-id="d2dd8-139">Account statuses</span></span>

<span data-ttu-id="d2dd8-140">يمكن إنشاء حالات الحساب لتحديد مركز الائتمان لحساب عميل.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-140">You can create account statuses to identify the credit standing of a customer account.</span></span> <span data-ttu-id="d2dd8-141">يمكنك تحديد الحالة وتأثيرها على عمليات الفوترة والتسليم قيد التعليق.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-141">You can define a status and its effect on the invoicing and delivery on-hold processes.</span></span> <span data-ttu-id="d2dd8-142">ويمكن أيضًا استخدام حالات الحساب لتحديد قواعد الحظر المطبقة على عميل.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-142">Account statuses can also be used to determine blocking rules for a customer.</span></span>

<span data-ttu-id="d2dd8-143">يمكن إنشاء حالات الحساب في صفحة **حالات الحساب** (**إدارة الائتمان \> الإعداد> إعداد المجموعات \> حالات الحساب**).</span><span class="sxs-lookup"><span data-stu-id="d2dd8-143">You can create account statuses on the **Account statuses** page (**Credit management \> Setup> Groups setup \> Account statuses**).</span></span>

1. <span data-ttu-id="d2dd8-144">أضف حالة حساب وادخل وصفًا يمثل مركز الائتمان لعميل.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-144">Add an account status, and enter a description that represents the credit standing for a customer.</span></span> <span data-ttu-id="d2dd8-145">على سبيل المثال استخدم **عادة** للإشارة إلى أن العميل في مركز جيد وإلى أن الأوامر المفتوحة تخضع لعملية إدارة الائتمان القياسية.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-145">For example, use **Normal** to indicate that a customer is in good standing and open orders are subject to standard credit management processing.</span></span>
2. <span data-ttu-id="d2dd8-146">في حقلي **الفوترة** و**التسليم قيد التعليق‬**، حدد نوع الوضع قيد التعليق الذي يجب أن يحدث للعملاء الذين لديهم حالة الحساب هذه.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-146">In the **Invoicing** and **Delivery on Hold** fields, select the type of hold that should occur for customers who have this account status.</span></span> <span data-ttu-id="d2dd8-147">يمكنك وضع عمليات المعالجة كلها قيد التعليق، أو وضع معالجة الفواتير فقط قيد التعليق، أو عدم وضع أي معالجة قيد التعليق عند تطبيق قواعد الحدود الائتمانية.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-147">You can hold all processing, hold only invoice processing, or hold no processing when the credit limit rules are applied.</span></span>

## <a name="scoring-groups"></a><span data-ttu-id="d2dd8-148">مجموعات النقاط</span><span class="sxs-lookup"><span data-stu-id="d2dd8-148">Scoring groups</span></span>

<span data-ttu-id="d2dd8-149">يمكن إعداد مجموعات النقاط لتحديد عوامل المخاطر والمعايير المستخدمة لقياسها.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-149">You can set up scoring groups to define risk factors and the criteria that are used to measure them.</span></span> <span data-ttu-id="d2dd8-150">عند تطبيق معلومات حول عميل على مجموعة نقاط، يتم حساب مجموع نقاط لكل عامل خطر ويستخدم لوضع العميل في مجموعة المخاطر.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-150">When information about a customer is applied to a scoring group, a score is calculated for each risk factor and used to put the customer in a risk group.</span></span> <span data-ttu-id="d2dd8-151">يمكن استخدام مجموعة المخاطر لتحديد الجدارة الائتمانية وحساب الحدود الائتمانية التلقائية.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-151">The risk group can be used to identify credit worthiness and calculate automatic credit limits.</span></span>

<span data-ttu-id="d2dd8-152">يمكنك إنشاء مجموعات نقاط في صفحة **مجموعات النقاط** (**إدارة الائتمان \> الإعداد \> إعداد المخاطر \> مجموعات النقاط**).</span><span class="sxs-lookup"><span data-stu-id="d2dd8-152">You can create scoring groups on the **Scoring groups** page (**Credit management \> Setup \> Risk setup \> Scoring groups**).</span></span>

1. <span data-ttu-id="d2dd8-153">أنشئ مجموعة نقاط، ثم قم بتسميتها.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-153">Create a scoring group, and enter a name for it.</span></span>
2. <span data-ttu-id="d2dd8-154">أدخل وصفًا لمجموعة النقاط.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-154">Enter a description to further describe the scoring group.</span></span>
3. <span data-ttu-id="d2dd8-155">حدد نوع مجموعة.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-155">Select a group type.</span></span> <span data-ttu-id="d2dd8-156">هناك ثمانية أنواع محددة بشكل مسبق.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-156">There are eight predefined types.</span></span> <span data-ttu-id="d2dd8-157">يمكنك أيضًا تحديد **معرّف من قبل المستخدم** لتحديد نوع مجموعة يتلاءم بشكل أفضل مع مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-157">You can also select **User defined** to define a group type that's better suited to your organization.</span></span>
4. <span data-ttu-id="d2dd8-158">حدد نوع النقاط لتحديد كيفية قيام مجموعة النقاط بحساب المخاطر.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-158">Select a score type to define how the scoring group calculates the risk score.</span></span> <span data-ttu-id="d2dd8-159">وتتوفر الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="d2dd8-159">The following options are available:</span></span>

    - <span data-ttu-id="d2dd8-160">**النطاق** – استخدم هذا الخيار لتحديد نطاق من القيم التي يجب استخدامها لحساب النقاط.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-160">**Range** – Use this option to define a range of values that should be used to calculate a score.</span></span>
    - <span data-ttu-id="d2dd8-161">**معرّف من قبل المستخدم** – استخدم هذا الخيار لتحديد قائمة بالقيم التي يجب استخدامها لمجموع النقاط.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-161">**User defined** – Use this option to manually define a list of values that should be used for the score.</span></span>

5. <span data-ttu-id="d2dd8-162">إذا حددت **النطاق‏‎** كنوع لمجموع النقاط، فأضف البنود لتحديد نطاق القيم والنقاط المقابلة.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-162">If you selected **Range** as the score type, add lines to define the range of values and the corresponding scores.</span></span>

    1. <span data-ttu-id="d2dd8-163">في الحقل **من القيمة**، حدد أقل قيمة في النطاق.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-163">In the **From value** field, specify the lowest value in the range.</span></span>
    2. <span data-ttu-id="d2dd8-164">في الحقل **إلى القيمة**، حدد أعلى قيمة في النطاق.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-164">In the **To value** field, specify the highest value in the range.</span></span>
    3. <span data-ttu-id="d2dd8-165">في الحقل‏‎ **مجموع النقاط‬**، أدخل مجموع النقاط الذي يجب تعيينه عندما تكون القيمة التي تم توفيرها موجودة في النطاق "من"/"إلى".</span><span class="sxs-lookup"><span data-stu-id="d2dd8-165">In the **Score** field, enter the score that should be assigned when the value that is provided is in the "from"/"to" range.</span></span>

    <span data-ttu-id="d2dd8-166">إذا حددت **معرّف من قبل المستخدم‏‎** كنوع لمجموع النقاط، فأضف البنود لتحديد القيم المعرّفة من قبل المستخدم والنقاط المقابلة.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-166">If you selected **User defined** as the score type, add lines to define the user-defined values and the corresponding scores.</span></span>

    1. <span data-ttu-id="d2dd8-167">في حقل **القيمة**، أدخل القيمة المعرّفة من قبل المستخدم التي يجب توفيرها من معلومات العميل.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-167">In the **Value** field, enter the user-defined value that should be provided from the customer information.</span></span>
    2. <span data-ttu-id="d2dd8-168">في الحقل‏‎ **مجموع النقاط‬**، أدخل مجموع النقاط الذي يجب تعيينه عندما تكون القيمة التي تم توفيرها موجودة في النطاق "من"/"إلى".</span><span class="sxs-lookup"><span data-stu-id="d2dd8-168">In the **Score** field, enter the score that should be assigned when the value that is provided is in the "from"/"to" range.</span></span>

## <a name="risk-assessments"></a><span data-ttu-id="d2dd8-169">تقييمات المخاطر</span><span class="sxs-lookup"><span data-stu-id="d2dd8-169">Risk assessments</span></span>

<span data-ttu-id="d2dd8-170">يمكنك تحديد تقييمات المخاطر التي يمكن تعيينها للعملاء، استنادًا إلى نقاط المخاطرة الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-170">You can define risk assessments that can be assigned to customers, based on their risk score.</span></span> <span data-ttu-id="d2dd8-171">يتم حساب نقاط المخاطرة من خلال مقارنة معلومات العميل بكل مجموعة نقاط.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-171">A risk score is calculated by comparing customer information to each scoring group.</span></span> <span data-ttu-id="d2dd8-172">يتم جمع النقاط، وتتم مقارنة إجمالي النقاط بالقيم الموجودة في إعداد مجموعة المخاطر للتعرف على مجموعة المخاطر التي ينتمي اليها العميل.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-172">The scores are summed, and the total score is compared to the values in the risk group setup to identify the risk group that the customer belongs to.</span></span> <span data-ttu-id="d2dd8-173">عندئذ يتم استخدام نقاط مجموعة المخاطر لتحديد قواعد الحظر والاستثناء لإدارة الائتمان للعملاء.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-173">The risk group score is then used to define credit management blocking and exclusion rules for the customer.</span></span>

<span data-ttu-id="d2dd8-174">يمكنك إعداد مجموعات مخاطر في صفحة **تقييمات المخاطر** (**إدارة الائتمان \> الإعداد \> إعداد المخاطر \> تقييمات المخاطر**).</span><span class="sxs-lookup"><span data-stu-id="d2dd8-174">You can set up risk groups on the **Risk assessments** page (**Credit management \> Setup \> Risk setup \> Risk assessments**).</span></span>

1. <span data-ttu-id="d2dd8-175">أدخل معرف مجموعة المخاطر.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-175">Enter a risk group ID.</span></span>
2. <span data-ttu-id="d2dd8-176">أدخل وصفًا لوصف مجموعة المخاطر بشكل أفضل.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-176">Enter a description to further explain the risk group.</span></span>
3. <span data-ttu-id="d2dd8-177">ادخل نطاقًا من النقاط يتم استخدامه لتحديد العملاء الذين ينتمون إلى مجموعة المخاطر.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-177">Enter a range of scores that is used to determine which customers belong to the risk group.</span></span>
4. <span data-ttu-id="d2dd8-178">حدد مؤشر مجموعة مخاطر لتحديد الرمز الذي يمثل مجموعة المخاطر.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-178">Select a risk group indicator to specify the symbol that represents the risk group.</span></span>

## <a name="guaranteeinsurance-types"></a><span data-ttu-id="d2dd8-179">أنواع الضمان/التأمين</span><span class="sxs-lookup"><span data-stu-id="d2dd8-179">Guarantee/insurance types</span></span>

<span data-ttu-id="d2dd8-180">يمكنك إعداد أنواع الضمان/التأمين في صفحة **أنواع الضمان/التأمين** (**إدارة الائتمان \> الإعداد \> إعداد الضمان/التأمين \> أنواع الضمان/التأمين**).</span><span class="sxs-lookup"><span data-stu-id="d2dd8-180">You can set up guarantee/insurance types on the **Guarantee/insurance types** page (**Credit management \> Setup \> Guarantee/insurance setup \> Guarantee/insurance types**).</span></span>

1. <span data-ttu-id="d2dd8-181">أدخل نوع الضمان أو التأمين الذي يحدد اسم الضامن أو وسيط التأمين.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-181">Enter a guarantee or insurance type that identifies the name of the guarantor or insurance broker.</span></span>
2. <span data-ttu-id="d2dd8-182">أدخل وصف الضمان/وسيط التأمين.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-182">Enter a description to describe the guarantor/insurance broker.</span></span>

## <a name="coverage-types"></a><span data-ttu-id="d2dd8-183">أنواع التغطية</span><span class="sxs-lookup"><span data-stu-id="d2dd8-183">Coverage types</span></span>

<span data-ttu-id="d2dd8-184">يمكن استخدام أنواع التغطية لتصنيف وثائق التأمين بشكل أفضل.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-184">Coverage types can be used to further classify insurance policies.</span></span> <span data-ttu-id="d2dd8-185">ولا يمكن استخدامها مع الضمانات.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-185">They can't be used with guarantees.</span></span>

<span data-ttu-id="d2dd8-186">يمكنك إضافة أنواع التغطية في صفحة **أنواع التغطية** (**إدارة الائتمان \> الإعداد \> إعداد الضمان/التأمين \> أنواع التغطية**).</span><span class="sxs-lookup"><span data-stu-id="d2dd8-186">You can add coverage types on the **Coverage types** page (**Credit management \> Setup \> Guarantee/insurance setup \> Coverage types**).</span></span>

1. <span data-ttu-id="d2dd8-187">أدخل نوع تغطية لتحديد نوع التغطية الذي ينبغي إضافته كتأمين أو ضمان.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-187">Enter a coverage type to identify the type of coverage that should be added as insurance or a guarantee.</span></span>
2. <span data-ttu-id="d2dd8-188">أدخل وصفًا لنوع التغطية.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-188">Enter a description to describe of the coverage type.</span></span>

## <a name="automatic-credit-limits"></a><span data-ttu-id="d2dd8-189">الحدود الائتمانية التلقائية</span><span class="sxs-lookup"><span data-stu-id="d2dd8-189">Automatic credit limits</span></span>

<span data-ttu-id="d2dd8-190">يمكنك إنشاء معايير للحدود الائتمانية التلقائية في صفحة **الحدود الائتمانية التلقائية** (**إدارة الائتمان \> الإعداد \> إعداد المخاطر \> الحدود الائتمانية التلقائية**).</span><span class="sxs-lookup"><span data-stu-id="d2dd8-190">You can create criteria for automatic credit limits on the **Automatic credit limits** page (**Credit management \> Setup \> Risk setup \> Automatic credit limits**).</span></span>

1. <span data-ttu-id="d2dd8-191">حدد مجموعة مخاطر يجب تعيين الحدود الائتمانية التلقائية لها.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-191">Select a risk group that the automatic credit limit should be assigned to.</span></span>
2. <span data-ttu-id="d2dd8-192">حدد عملة الحدود الائتمانية التلقائية.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-192">Select the currency for the automatic credit limit.</span></span> <span data-ttu-id="d2dd8-193">يمكنك إنشاء حدود ائتمانية تلقائية متعددة بعملات مختلفة لمجموعة المخاطر نفسها.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-193">You can create multiple automatic credit limits in different currencies for the same risk group.</span></span>
3. <span data-ttu-id="d2dd8-194">ادخل قيمة الإيرادات التي تمثل الحد الأقصى لإيرادات الشركة التي يمكن استخدامها للحد الائتماني التلقائي هذه.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-194">Enter the revenue amount that represents the maximum company revenue that can be used for this automatic credit limit.</span></span> <span data-ttu-id="d2dd8-195">عند إنشاء الحدود الائتمانية، تتم مقارنة قيمة الإيرادات بقيمة إيراد موجودة في صفحة **الماليات‏‎** (**الحسابات المدينة‬ \> كافة العملاء‬ \> حدد عميلاً \> عام \> الإحصاءات‬ \> الماليات‏‎‏‎**).</span><span class="sxs-lookup"><span data-stu-id="d2dd8-195">When credit limits are created, the revenue amount is compared to a revenue value that is found on the **Financials** page (**Accounts receivable \> All customers \> Select a customer \> General \> Statistics \> Financial**).</span></span> <span data-ttu-id="d2dd8-196">يستخدم النظام آخر قيمة في القسم **نظرة عامة**.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-196">The system uses the latest value in the **Overview** section.</span></span>

<span data-ttu-id="d2dd8-197">اتبع هذه الخطوات لإضافة بنود تمثل الحد الائتماني الذي سيتم إنشاؤه استنادًا إلى المعايير المحددة.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-197">Follow these steps to add lines that represent the credit limit that will be generated based on the selected criteria.</span></span>

1. <span data-ttu-id="d2dd8-198">حدد مجموعة النقاط التي تحدد معلومات العميل التي يجب استخدامها لحساب الحد الائتماني.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-198">Select the scoring group that defines the customer information that should be used to calculate the credit limit.</span></span>
2. <span data-ttu-id="d2dd8-199">حدد عامل المقارنة الذي يحدد كيف يجب تقييم معلومات مجموعة النقاط.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-199">Select the comparison operator that defines how the scoring group information should be evaluated.</span></span>
3. <span data-ttu-id="d2dd8-200">أدخل القيمة التي يجب مقارنتها بالقيمة المحددة لمجموعة النقاط.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-200">Enter the value that should be compared to the value that is specified for the scoring group.</span></span>
4. <span data-ttu-id="d2dd8-201">ادخل الحد الائتماني الذي يجب تعيينه إذا كانت معلومات العميل مطابقة للقيمة التي تم تحديدها لمجموعة النقاط.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-201">Enter the credit limit that should be assigned if the customer information matches the value that is specified for the scoring group.</span></span> <span data-ttu-id="d2dd8-202">على سبيل المثال، تقوم بإنشاء حد ائتماني تلقائي في مجموعة النقاط **منخفض**.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-202">For example, you create an automatic credit limit for the **Low** scoring group.</span></span> <span data-ttu-id="d2dd8-203">إذا كانت سنوات العمل تشكّل إحدى مجموعات النقاط، فيمكنك تعريف بند واحد يعيّن حدًا ائتمانيًا من 100,000 إذا أمضى العميل خمس سنوات في مجال الأعمال، وبند آخر يعيّن حدًا ائتمانيًا من 200,000 إذا أمضى العميل 10 سنوات في مجال الأعمال.</span><span class="sxs-lookup"><span data-stu-id="d2dd8-203">If the years in business is one of the scoring groups, you can define one line that assigns a 100,000 credit limit if the customer has been in business five years and another line that assigns a 200,000 credit limit if the customer has been in business for 10 years.</span></span>
