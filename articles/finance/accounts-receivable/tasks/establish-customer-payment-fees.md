---
title: ‏‫وضع رسوم دفع العميل‬
description: إنشاء رسوم الدفع لمدفوعات العميل.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6475671002379d84519df05a0198a17ac000677
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143732"
---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="8ab46-103">‏‫وضع رسوم دفع العميل‬</span><span class="sxs-lookup"><span data-stu-id="8ab46-103">Establish customer payment fees</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8ab46-104">إنشاء رسوم الدفع لمدفوعات العميل.</span><span class="sxs-lookup"><span data-stu-id="8ab46-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="8ab46-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="8ab46-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="8ab46-106">في **جزء التنقل**، انتقل إلى **الوحدات النمطية‬ > حسابات مدينة‬ > إعداد المدفوعات‬ > رسوم الدفع‬**.</span><span class="sxs-lookup"><span data-stu-id="8ab46-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Payment fee**.</span></span>
2. <span data-ttu-id="8ab46-107">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8ab46-107">Click **New**.</span></span>
3. <span data-ttu-id="8ab46-108">في الحقل **معرف الرسوم**، أدخل معرف رسوم.</span><span class="sxs-lookup"><span data-stu-id="8ab46-108">In the **Fee ID** field, enter a Fee ID.</span></span> <span data-ttu-id="8ab46-109">يظهر "معرف الرسوم" على دفاتر يومية المدفوعات، لذلك اجعله وصفيًا لفهم ما هي الرسوم التي يتم فرضها.</span><span class="sxs-lookup"><span data-stu-id="8ab46-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="8ab46-110">أدخل اسمًا للرسوم في حقل **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="8ab46-110">In the **Name** field, enter a fee name.</span></span>
5. <span data-ttu-id="8ab46-111">أدخل وصفًا للرسوم في حقل **وصف الرسوم**.</span><span class="sxs-lookup"><span data-stu-id="8ab46-111">In the **Fee description** field, enter a description for the fee.</span></span>
6. <span data-ttu-id="8ab46-112">في حقل **التكلفة**، حدد ما إذا كان سيتم تحميل الرسوم لحساب العميل أو حساب دفتر أستاذ.</span><span class="sxs-lookup"><span data-stu-id="8ab46-112">In the **Charge** field, select whether the fee will be charged to the Customer or a Ledger account.</span></span> <span data-ttu-id="8ab46-113">إذا كانت الرسوم ستُفرض على العميل، فحدد "العميل".</span><span class="sxs-lookup"><span data-stu-id="8ab46-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="8ab46-114">إذا كانت الرسوم ستُفرض على مؤسستك كمصروفات، فحدد "دفتر الأستاذ‬".</span><span class="sxs-lookup"><span data-stu-id="8ab46-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="8ab46-115">لهذه المهمة، حدد "العميل".</span><span class="sxs-lookup"><span data-stu-id="8ab46-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="8ab46-116">في الحقل **نوع دفتر اليومية**، حدد نوع دفتر اليومية الذي يمكنه استخدام رسوم الدفع هذه.</span><span class="sxs-lookup"><span data-stu-id="8ab46-116">In the **Journal type** field, select the type of journal that can use this payment fee.</span></span> <span data-ttu-id="8ab46-117">إذا كانت هذه الرسوم ستُستخدم لمدفوعات العميل، فسيكون نوع دفتر اليومية على الأرجح دفع العميل‬.</span><span class="sxs-lookup"><span data-stu-id="8ab46-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="8ab46-118">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8ab46-118">Click **Save**.</span></span>
9. <span data-ttu-id="8ab46-119">انقر فوق **إعداد رسوم الدفع**.</span><span class="sxs-lookup"><span data-stu-id="8ab46-119">Click **Payment fee setup**.</span></span> <span data-ttu-id="8ab46-120">يتم استخدام إعداد رسوم الدفع لتعريف المعايير عند فرض رسوم الدفع.</span><span class="sxs-lookup"><span data-stu-id="8ab46-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="8ab46-121">على سبيل المثال، يمكنك تحديد أنه سيتم حساب الرسوم إذا كان الحساب البنكي USMF OPER، وطريقة الدفع هي الشيك.</span><span class="sxs-lookup"><span data-stu-id="8ab46-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="8ab46-122">حدد "الجدول" أو "المجموعة" أو "الكل" لتعريف الحسابات البنكية التي سيتم فرض هذه الرسوم عليها في حقل **التجميعات**.</span><span class="sxs-lookup"><span data-stu-id="8ab46-122">In the **Groupings** field, select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span> <span data-ttu-id="8ab46-123">إذا حددت "الكل"، فقد يتم فرض هذه الرسوم على كل الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="8ab46-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="8ab46-124">وإذا حددت "الجدول"، فقد يتم فرض هذه الرسوم فقط على الحساب البنكي الذي تحدده.</span><span class="sxs-lookup"><span data-stu-id="8ab46-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="8ab46-125">إما إذا حددت "المجموعة‬"، فقد يتم فرض هذه الرسوم فقط على الحسابات البنكية في المجموعة المحددة.</span><span class="sxs-lookup"><span data-stu-id="8ab46-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="8ab46-126">في الحقل **علاقة البنك**، حدد مجموعة بنكية أو حساب بنكي.</span><span class="sxs-lookup"><span data-stu-id="8ab46-126">In the **Bank relation** field, select either a bank group or a bank account.</span></span> <span data-ttu-id="8ab46-127">إذا حددت "الجدول"، فسيعرض البحث الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="8ab46-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="8ab46-128">أما إذا حددت "المجموعة"، فسيعرض البحث المجموعات البنكية.</span><span class="sxs-lookup"><span data-stu-id="8ab46-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="8ab46-129">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8ab46-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="8ab46-130">في الحقل **طريقة الدفع**، حدد طريقه الدفع التي سيتم تقييم هذه الرسوم لها.</span><span class="sxs-lookup"><span data-stu-id="8ab46-130">In the **Method of payment** field, select the Method of payment for which this fee will be assessed.</span></span> <span data-ttu-id="8ab46-131">على سبيل المثال، يمكنك فرض رسوم على العملاء إذا قاموا بإرسال الدفعات كشيك، بدلاً من دفعة إلكترونية.</span><span class="sxs-lookup"><span data-stu-id="8ab46-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="8ab46-132">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="8ab46-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="8ab46-133">أدخل عملة دفع، إذا كان ذلك ملائمًا، في حقل **عملة الدفع**.</span><span class="sxs-lookup"><span data-stu-id="8ab46-133">If relevant, in the **Payment currency** field, enter a payment currency.</span></span> <span data-ttu-id="8ab46-134">يتم استخدام عملة الدفع كمعيار إضافي لما إذا كان سيتم فرض الرسوم.</span><span class="sxs-lookup"><span data-stu-id="8ab46-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="8ab46-135">على سبيل المثال، قد يفرض البنك رسمًا إضافيًا للدفعات المستلمة بعملة الدولار الأمريكي، إذ يقوم عادةً بتنفيذ المعاملات باليورو فقط.</span><span class="sxs-lookup"><span data-stu-id="8ab46-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="8ab46-136">حدد ما إذا كانت الرسوم ستكون عبارة عن نسبة أو مبلغ أو فاصل زمني.</span><span class="sxs-lookup"><span data-stu-id="8ab46-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="8ab46-137">في الحقل **النسبة المئوية/المبلغ**، أدخل نسبة مئوية أو مبلغًا للرسوم.</span><span class="sxs-lookup"><span data-stu-id="8ab46-137">In the **Percentage/Amount field**, enter either percentage or amount of the fee.</span></span> <span data-ttu-id="8ab46-138">إذا كان حقل "النسبة المئوية/المبلغ" معينًا إلى "النسبة‬", فستكون عندئذٍ القيمة المدخلة هنا نسبة مئوية.</span><span class="sxs-lookup"><span data-stu-id="8ab46-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="8ab46-139">وإذا كان حقل "النسبة المئوية/المبلغ" معينًا إلى "المبلغ", فستكون عندئذٍ القيمة التي تدخلها هنا مبلغًا.</span><span class="sxs-lookup"><span data-stu-id="8ab46-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="8ab46-140">أما إذا كان حقل "النسبة المئوية/المبلغ" معينًا إلى "الفاصل الزمني‬", فاستخدم علامة التبويب "الفاصل الزمني‬" لتحديد المستويات.</span><span class="sxs-lookup"><span data-stu-id="8ab46-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="8ab46-141">في حقل **عملة الرسوم**، حدد عملة الرسوم.</span><span class="sxs-lookup"><span data-stu-id="8ab46-141">In the **Fee currency** field, select the currency of the fee.</span></span> <span data-ttu-id="8ab46-142">هذه هي العملة التي سيتم استخدامها لإنشاء الرسوم.</span><span class="sxs-lookup"><span data-stu-id="8ab46-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="8ab46-143">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="8ab46-143">Click **Save**.</span></span>
