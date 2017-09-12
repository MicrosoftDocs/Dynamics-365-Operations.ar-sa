--- 
title: "‏‫وضع رسوم دفع العميل‬"
description: "إنشاء رسوم الدفع لمدفوعات العميل."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 411d2eeebcbf0a78203ac440968b559088a2fcf5
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="57fae-103">‏‫وضع رسوم دفع العميل‬</span><span class="sxs-lookup"><span data-stu-id="57fae-103">Establish customer payment fees</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57fae-104">إنشاء رسوم الدفع لمدفوعات العميل.</span><span class="sxs-lookup"><span data-stu-id="57fae-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="57fae-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="57fae-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="57fae-106">انتقل إلى الحسابات المدينة > إعداد المدفوعات‬ > رسوم الدفع‬.</span><span class="sxs-lookup"><span data-stu-id="57fae-106">Go to Accounts receivable > Payments setup > Payment fee.</span></span>
2. <span data-ttu-id="57fae-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="57fae-107">Click New.</span></span>
3. <span data-ttu-id="57fae-108">في الحقل "معرف الرسوم"، أدخل معرف رسوم.</span><span class="sxs-lookup"><span data-stu-id="57fae-108">In the Fee ID field, enter a Fee ID.</span></span>
    * <span data-ttu-id="57fae-109">يظهر "معرف الرسوم" على دفاتر يومية المدفوعات، لذلك اجعله وصفيًا لفهم ما هي الرسوم التي يتم فرضها.</span><span class="sxs-lookup"><span data-stu-id="57fae-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="57fae-110">في الحقل "الاسم"، أدخل اسمًا للرسوم.</span><span class="sxs-lookup"><span data-stu-id="57fae-110">In the Name field, enter a fee Name.</span></span>
5. <span data-ttu-id="57fae-111">في حقل "وصف الرسوم"، أدخل وصفًا للرسوم.</span><span class="sxs-lookup"><span data-stu-id="57fae-111">In the Fee description field, enter a description for the fee.</span></span>
6. <span data-ttu-id="57fae-112">حدد ما إذا كان سيتم تحميل الرسوم للعميل أو حساب دفتر أستاذ.</span><span class="sxs-lookup"><span data-stu-id="57fae-112">Select whether the fee will be charged to the Customer or a Ledger account.</span></span>
    * <span data-ttu-id="57fae-113">إذا كانت الرسوم ستُفرض على العميل، فحدد "العميل".</span><span class="sxs-lookup"><span data-stu-id="57fae-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="57fae-114">إذا كانت الرسوم ستُفرض على مؤسستك كمصروفات، فحدد "دفتر الأستاذ‬".</span><span class="sxs-lookup"><span data-stu-id="57fae-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="57fae-115">لهذه المهمة، حدد "العميل".</span><span class="sxs-lookup"><span data-stu-id="57fae-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="57fae-116">حدد نوع دفتر اليومية الذي يمكنه استخدام رسوم الدفع هذه.</span><span class="sxs-lookup"><span data-stu-id="57fae-116">Select the type of  journal that can use this payment fee.</span></span>
    * <span data-ttu-id="57fae-117">إذا كانت هذه الرسوم ستُستخدم لمدفوعات العميل، فسيكون نوع دفتر اليومية على الأرجح دفع العميل‬.</span><span class="sxs-lookup"><span data-stu-id="57fae-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="57fae-118">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="57fae-118">Click Save.</span></span>
9. <span data-ttu-id="57fae-119">انقر فوق "إعداد رسوم الدفع‬".</span><span class="sxs-lookup"><span data-stu-id="57fae-119">Click Payment fee setup.</span></span>
    * <span data-ttu-id="57fae-120">يتم استخدام إعداد رسوم الدفع لتعريف المعايير عند فرض رسوم الدفع.</span><span class="sxs-lookup"><span data-stu-id="57fae-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="57fae-121">على سبيل المثال، يمكنك تحديد أنه سيتم حساب الرسوم إذا كان الحساب البنكي USMF OPER، وطريقة الدفع هي الشيك.</span><span class="sxs-lookup"><span data-stu-id="57fae-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="57fae-122">حدد "الجدول" أو "المجموعة" أو "الكل" لتعريف الحسابات البنكية التي سيتم فرض هذه الرسوم عليها.</span><span class="sxs-lookup"><span data-stu-id="57fae-122">Select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span>
    * <span data-ttu-id="57fae-123">إذا حددت "الكل"، فقد يتم فرض هذه الرسوم على كل الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="57fae-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="57fae-124">وإذا حددت "الجدول"، فقد يتم فرض هذه الرسوم فقط على الحساب البنكي الذي تحدده.</span><span class="sxs-lookup"><span data-stu-id="57fae-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="57fae-125">إما إذا حددت "المجموعة‬"، فقد يتم فرض هذه الرسوم فقط على الحسابات البنكية في المجموعة المحددة.</span><span class="sxs-lookup"><span data-stu-id="57fae-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="57fae-126">حدد مجموعة بنكية أو حسابًا بنكيًا.</span><span class="sxs-lookup"><span data-stu-id="57fae-126">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="57fae-127">إذا حددت "الجدول"، فسيعرض البحث الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="57fae-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="57fae-128">أما إذا حددت "المجموعة"، فسيعرض البحث المجموعات البنكية.</span><span class="sxs-lookup"><span data-stu-id="57fae-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="57fae-129">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="57fae-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="57fae-130">حدد طريقة الدفع التي سيتم فرض هذه الرسوم عليها.</span><span class="sxs-lookup"><span data-stu-id="57fae-130">Select the Method of payment for which this fee will be assessed.</span></span>
    * <span data-ttu-id="57fae-131">على سبيل المثال، يمكنك فرض رسوم على العملاء إذا قاموا بإرسال الدفعات كشيك، بدلاً من دفعة إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="57fae-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="57fae-132">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="57fae-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="57fae-133">إذا كان ذلك مناسبًا، أدخل عملة دفع.</span><span class="sxs-lookup"><span data-stu-id="57fae-133">If relevant, enter a payment currency.</span></span>
    * <span data-ttu-id="57fae-134">يتم استخدام عملة الدفع كمعيار إضافي لما إذا كان سيتم فرض الرسوم.</span><span class="sxs-lookup"><span data-stu-id="57fae-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="57fae-135">على سبيل المثال، قد يفرض البنك رسمًا إضافيًا للدفعات المستلمة بعملة الدولار الأمريكي، إذ يقوم عادةً بتنفيذ المعاملات باليورو فقط.</span><span class="sxs-lookup"><span data-stu-id="57fae-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="57fae-136">حدد ما إذا كانت الرسوم ستكون عبارة عن نسبة أو مبلغ أو فاصل زمني.</span><span class="sxs-lookup"><span data-stu-id="57fae-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="57fae-137">أدخل نسبة أو مبلغ الرسوم.</span><span class="sxs-lookup"><span data-stu-id="57fae-137">Enter either percentage or amount of the fee.</span></span>
    * <span data-ttu-id="57fae-138">إذا كان حقل "النسبة المئوية/المبلغ" معينًا إلى "النسبة‬", فستكون عندئذٍ القيمة المدخلة هنا نسبة مئوية.</span><span class="sxs-lookup"><span data-stu-id="57fae-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="57fae-139">وإذا كان حقل "النسبة المئوية/المبلغ" معينًا إلى "المبلغ", فستكون عندئذٍ القيمة التي تدخلها هنا مبلغًا.</span><span class="sxs-lookup"><span data-stu-id="57fae-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="57fae-140">أما إذا كان حقل "النسبة المئوية/المبلغ" معينًا إلى "الفاصل الزمني‬", فاستخدم علامة التبويب "الفاصل الزمني‬" لتحديد المستويات.</span><span class="sxs-lookup"><span data-stu-id="57fae-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="57fae-141">في حقل "عملة الرسوم"، حدد عملة الرسوم.</span><span class="sxs-lookup"><span data-stu-id="57fae-141">In the Fee currency field, select the currency of the fee.</span></span>
    * <span data-ttu-id="57fae-142">هذه هي العملة التي سيتم استخدامها لإنشاء الرسوم.</span><span class="sxs-lookup"><span data-stu-id="57fae-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="57fae-143">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="57fae-143">Click Save.</span></span>


