--- 
title: "‏‫وضع شروط دفع العميل‬"
description: "يعرّف هذا الإجراء إعداد خصم نقدي وتاريخ استحقاق."
author: aprilolson
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: c35c608dc5e9b4790a81a8dadb716157fa740e8c
ms.contentlocale: ar-sa
ms.lasthandoff: 08/07/2018

---
# <a name="establish-customer-payment-terms"></a><span data-ttu-id="f65e9-103">‏‫وضع شروط دفع العميل‬</span><span class="sxs-lookup"><span data-stu-id="f65e9-103">Establish customer payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f65e9-104">يعرّف هذا الإجراء إعداد خصم نقدي وتاريخ استحقاق.</span><span class="sxs-lookup"><span data-stu-id="f65e9-104">This procedure defines a cash discount and due date setup.</span></span> <span data-ttu-id="f65e9-105">يستخدم دليل المهمة هذا شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="f65e9-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="f65e9-106">انتقل إلى الحسابات المدينة > إعداد المدفوعات‬ > أيام الدفع‬.</span><span class="sxs-lookup"><span data-stu-id="f65e9-106">Go to Accounts receivable > Payments setup > Payment days.</span></span>
    * <span data-ttu-id="f65e9-107">يكون إعداد شروط الدفع مشتركًا للحسابات المدينة والحسابات الدائنة.</span><span class="sxs-lookup"><span data-stu-id="f65e9-107">The setup for the Terms of payment is shared for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="f65e9-108">إذا قمت بتعريفها في الوحدة النمطية، فستكون متوفرة في الوحدة النمطية الأخرى أيضًا.</span><span class="sxs-lookup"><span data-stu-id="f65e9-108">If you define it in module, it will be available in the other module also.</span></span> <span data-ttu-id="f65e9-109">بالنسبة إلى دليل المهمة هذا، تم بإعداد شروط الدفع تحت "الحسابات المدينة".</span><span class="sxs-lookup"><span data-stu-id="f65e9-109">For this task guide, I set up all the terms of payment under Accounts receivable.</span></span>  
2. <span data-ttu-id="f65e9-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f65e9-110">Click New.</span></span>
    * <span data-ttu-id="f65e9-111">أنشئ يوم دفع إذا كانت شروط الدفع تتطلب يومًا معينًا في الأسبوع (الاثنين, الثلاثاء, إلخ) أو تاريخًا معينًا في الشهر (الخامس، العاشر، إلخ).</span><span class="sxs-lookup"><span data-stu-id="f65e9-111">Create a payment day if your terms of payment require a specific day of the week (Monday, Tuesday, etc) or a specific date of the month (5th, 10th, etc).</span></span>  
3. <span data-ttu-id="f65e9-112">في الحقل "يوم الدفع"، أدخل معرف يوم الدفع في الحقل "يوم الدفع".</span><span class="sxs-lookup"><span data-stu-id="f65e9-112">In the Payment day field, enter an ID for the Payment day in the payment day field.</span></span>
4. <span data-ttu-id="f65e9-113">في حقل "الوصف"، أدخل وصفًا ليوم الدفع.</span><span class="sxs-lookup"><span data-stu-id="f65e9-113">In the Description field, enter a description of the payment day.</span></span>
5. <span data-ttu-id="f65e9-114">في الحقل "الأسبوع/الشهر‬"، حدد إما الأسبوع أو الشهر.</span><span class="sxs-lookup"><span data-stu-id="f65e9-114">In the Week/Month field, select either Week or Month.</span></span>
    * <span data-ttu-id="f65e9-115">إذا أردت إدخال يوم من الأسبوع، مثل يوم الاثنين، فحدد "الأسبوع".</span><span class="sxs-lookup"><span data-stu-id="f65e9-115">If you want to enter a day of the week, such as Monday, select Week.</span></span> <span data-ttu-id="f65e9-116">إذا أردت إدخال تاريخ في الشهر، مثل العاشر، فحدد "الشهر".</span><span class="sxs-lookup"><span data-stu-id="f65e9-116">If you want to enter a date in the month, such as the 10th, select Month.</span></span> <span data-ttu-id="f65e9-117">حدد "الشهر" لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="f65e9-117">Select Month for this example.</span></span>  
6. <span data-ttu-id="f65e9-118">في الحقل "يوم من الشهر" أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="f65e9-118">In the Day of month field, enter a date.</span></span>
    * <span data-ttu-id="f65e9-119">يجب إدخال التاريخ كرقم "10"' وليس "العاشر".</span><span class="sxs-lookup"><span data-stu-id="f65e9-119">The date should be entered as a number, such as '10', and not as '10th'.</span></span>  
7. <span data-ttu-id="f65e9-120">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f65e9-120">Click Save.</span></span>
8. <span data-ttu-id="f65e9-121">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f65e9-121">Close the page.</span></span>
9. <span data-ttu-id="f65e9-122">انتقل إلى الحسابات المدينة > إعداد المدفوعات‬ > شروط الدفع.</span><span class="sxs-lookup"><span data-stu-id="f65e9-122">Go to Accounts receivable > Payments setup > Terms of payment.</span></span>
10. <span data-ttu-id="f65e9-123">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f65e9-123">Click New.</span></span>
    * <span data-ttu-id="f65e9-124">تُستخدم شروط الدفع لتعريف الطريقة التي سيتم بها حساب تواريخ الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="f65e9-124">Terms of payment is used to define how the due dates will be calculated.</span></span> <span data-ttu-id="f65e9-125">يتم إعداد تاريخ الخصم النقدي في صفحة منفصلة.</span><span class="sxs-lookup"><span data-stu-id="f65e9-125">The cash discount date setup is defined in a separate page.</span></span>  
11. <span data-ttu-id="f65e9-126">في الحقل "شروط الدفع"، أدخل معرفًا في الحقل "شروط الدفع".</span><span class="sxs-lookup"><span data-stu-id="f65e9-126">In the Terms of payment field, enter an ID in the Terms of payment field.</span></span>
12. <span data-ttu-id="f65e9-127">في الحقل "الوصف"، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="f65e9-127">In the Description field, enter a description.</span></span>
13. <span data-ttu-id="f65e9-128">حدد طريقة دفع مثل الدفع عند التسليم والمبلغ الصافي والشهر الحالي، إلخ.</span><span class="sxs-lookup"><span data-stu-id="f65e9-128">Select a Payment method such as COD, Net, Current month, etc.</span></span>
    * <span data-ttu-id="f65e9-129">تُستخدم طريقة الدفع لتعريف الطريقة التي سيتم بها حساب تواريخ الاستحقاق.</span><span class="sxs-lookup"><span data-stu-id="f65e9-129">The Payment method is used to define the start of how the due will be calculated.</span></span>  <span data-ttu-id="f65e9-130">على سبيل المثال، يتم استخدام "الصافي‬" إذا كان تاريخ الاستحقاق دائمًا عبارة عن عدد معين من الأشهر أو الأيام بعد تاريخ الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="f65e9-130">For example, Net is used if the due date is always a set number of months or days after the invoice date.</span></span> <span data-ttu-id="f65e9-131">يمكن استخدام "الدفع عند التسليم" عندما يكون الدفع مطلوبًا عند تقديم الفاتورة، حيث لا يتم حساب تاريخ استحقاق.</span><span class="sxs-lookup"><span data-stu-id="f65e9-131">COD can be used to when payment is required upon invoice, so a due date wouldn't be calculated.</span></span> <span data-ttu-id="f65e9-132">حدد "الشهر الحالي" لدليل المهمة هذا.</span><span class="sxs-lookup"><span data-stu-id="f65e9-132">Select Current month for this task guide.</span></span>  
14. <span data-ttu-id="f65e9-133">حدد يوم دفع إذا تم تضمين يوم معين في الأسبوع أو تاريخ معين في الحساب.</span><span class="sxs-lookup"><span data-stu-id="f65e9-133">Select a Payment day if a specific day of the  week or date are included in the calculation.</span></span>
    * <span data-ttu-id="f65e9-134">استنادًا إلى شروط الدفع، يمكنك إدخال كمية في الشهور أو الأيام.</span><span class="sxs-lookup"><span data-stu-id="f65e9-134">Depending on your terms of payment, you may enter a quantity in Months or Days.</span></span> <span data-ttu-id="f65e9-135">أو يمكنك استخدام جدول الدفع أو يوم الدفع من أجل "إضافته" إلى نهاية لطريقة الدفع.</span><span class="sxs-lookup"><span data-stu-id="f65e9-135">Or you can use the Payment schedule or Payment day to 'add' to the end of the Payment method.</span></span> <span data-ttu-id="f65e9-136">إذا كان تاريخ الاستحقاق سيكون دائمًا في اليوم العاشر من الشهر التالي، فحدد اليوم العاشر كيوم دفع.</span><span class="sxs-lookup"><span data-stu-id="f65e9-136">If the due date will always be the 10th of the next month, select a Payment day of the 10th.</span></span>  
15. <span data-ttu-id="f65e9-137">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f65e9-137">Click Save.</span></span>
16. <span data-ttu-id="f65e9-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="f65e9-138">Close the page.</span></span>
17. <span data-ttu-id="f65e9-139">انتقل إلى الحسابات المدينة > إعداد المدفوعات‬ > الخصومات النقدية‬‬.</span><span class="sxs-lookup"><span data-stu-id="f65e9-139">Go to Accounts receivable > Payments setup > Cash discounts.</span></span>
18. <span data-ttu-id="f65e9-140">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="f65e9-140">Click New.</span></span>
    * <span data-ttu-id="f65e9-141">تستخدم هذه الصفحة لتعريف كيف سيتم حساب تاريخ الخصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="f65e9-141">This page is used to define how the cash discount date will be calculated.</span></span>  
19. <span data-ttu-id="f65e9-142">في الحقل "الخصم النقدي"، أدخل معرفًا في الحقل "الخصم النقدي".</span><span class="sxs-lookup"><span data-stu-id="f65e9-142">In the Cash discount field, enter an ID in the Cash discount field.</span></span>
20. <span data-ttu-id="f65e9-143">في الحقل "الوصف"، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="f65e9-143">In the Description field, enter a description.</span></span>
21. <span data-ttu-id="f65e9-144">إذا توفر خصم نقدي مرتبط بمستوى، فحدد كود الخصم التالي ذي الصلة بعد الخصم النقدي الجديد هذا.</span><span class="sxs-lookup"><span data-stu-id="f65e9-144">If a tiered cash discount is available, select the Next discount code that is relevant after this new cash discount.</span></span>
22. <span data-ttu-id="f65e9-145">أدخل عدد الأيام التي يجب استخدامها لحساب تاريخ الخصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="f65e9-145">Enter the number of days used to calculate the cash discount date.</span></span>
    * <span data-ttu-id="f65e9-146">إذا تم تحديد مبدأ "الصافي"، فسيضاف عدد الأيام إلى تاريخ الفاتورة لحساب تاريخ الخصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="f65e9-146">If Net principle is selected, the number of days will be added to the invoice date to calculate the cash discount date.</span></span>  
23. <span data-ttu-id="f65e9-147">أدخل النسبة المئوية للخصم النقدي.</span><span class="sxs-lookup"><span data-stu-id="f65e9-147">Enter the percentage of the cash discount.</span></span>
24. <span data-ttu-id="f65e9-148">أدخل الحساب الرئيسي حيث سيقوم الخصم النقدي بترحيل فواتير العميل.</span><span class="sxs-lookup"><span data-stu-id="f65e9-148">Enter the main account to which the cash discount will post for customer invoices.</span></span>
25. <span data-ttu-id="f65e9-149">في الحقل "الحسابات المقابلة للخصومات"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="f65e9-149">In the Discount offset accounts field, select an option.</span></span>
    * <span data-ttu-id="f65e9-150">إذا قمت بتحديد "الحسابات الموجودة في بنود الفاتورة"، فسيتم ترحيل الخصم النقدي إلى الحساب الرئيسي نفسه للأصول/المصروفات على بنود فاتورة المورّد.</span><span class="sxs-lookup"><span data-stu-id="f65e9-150">If you select 'Accounts on the invoice lines', the cash discount will post to the same asset/expense main account on the lines of the vendor invoice.</span></span> <span data-ttu-id="f65e9-151">إذا قمت بتحديد "استخدام الحساب الرئيسي لفواتير المورّد"، فسيتم ترحيل الخصم النقدي إلى الحساب الرئيسي الذي قمت بتعريفه في "الحساب الرئيسي لفواتير المورّد".</span><span class="sxs-lookup"><span data-stu-id="f65e9-151">If you select 'Use main account for vendor invoices', the cash discount will post to the main account you define in the 'Main account for vendor invoices'.</span></span> <span data-ttu-id="f65e9-152">على سبيل المثال، حدد "استخدام الحساب الرئيسي لفواتير المورّد".</span><span class="sxs-lookup"><span data-stu-id="f65e9-152">For this example, select 'Use main account for vendor invoices.'</span></span>  
26. <span data-ttu-id="f65e9-153">أدخل الحساب الرئيسي حيث سيقوم الخصم النقدي بترحيل فواتير المورّد.</span><span class="sxs-lookup"><span data-stu-id="f65e9-153">Enter the main account to which the cash discount will post for vendor invoices.</span></span>
27. <span data-ttu-id="f65e9-154">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="f65e9-154">Click Save.</span></span>


