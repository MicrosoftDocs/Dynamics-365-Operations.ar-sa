---
title: ‏‫تحديد رسوم دفع المورّد‬
description: إعداد رسوم مدفوعات المورّد.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 399291a98ddc6b01fb08f7a5c629ec7a6f8acfbf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "363190"
---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="a2b1b-103">‏‫تحديد رسوم دفع المورّد‬</span><span class="sxs-lookup"><span data-stu-id="a2b1b-103">Define vendor payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a2b1b-104">إعداد رسوم مدفوعات المورّد.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-104">Set up vendor payment fees.</span></span> <span data-ttu-id="a2b1b-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a2b1b-106">انتقل إلى الحسابات المدينة > إعداد الدفع‬ > رسوم الدفع‬.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="a2b1b-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="a2b1b-107">Click New.</span></span>
3. <span data-ttu-id="a2b1b-108">في الحقل "معرف الرسوم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="a2b1b-109">يجب أن يصف "معرف الرسوم" الوقت الذي سيتم استخدام هذه الرسوم، مثل "EFT_Fee".</span><span class="sxs-lookup"><span data-stu-id="a2b1b-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="a2b1b-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a2b1b-111">في حقل "وصف الرسوم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="a2b1b-112">أضف وصفًا لتوفير مزيد من التفاصيل حول الوقت الذي سيتم فيه فرض الرسوم.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="a2b1b-113">في الحقل "التكلفة‬"، حدد المورّد أو دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="a2b1b-114">يتم استخدام دفتر الأستاذ عندما يتم تسجيل نفقات الرسوم لمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="a2b1b-115">يتم استخدام المورّد عند فرض الرسوم على المورّد.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="a2b1b-116">أدخل حسابًا رئيسيًا حيث سيتم تسجيل نفقات الرسوم.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="a2b1b-117">يتوفر هذا الخيار فقط عند تحديد "دفتر الأستاذ" كخيار "تكلفة".</span><span class="sxs-lookup"><span data-stu-id="a2b1b-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="a2b1b-118">حدد دفتر اليومية الذي يمكن استخدام هذه الرسوم عليه.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="a2b1b-119">بالنسبة إلى رسوم الدفع الخاصة بالمورّد، يمكنك تحديد "نفقة المورّد" لدفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="a2b1b-120">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="a2b1b-120">Click Save.</span></span>
10. <span data-ttu-id="a2b1b-121">انقر فوق "إعداد رسوم الدفع‬".</span><span class="sxs-lookup"><span data-stu-id="a2b1b-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="a2b1b-122">تابع إلى "إعداد رسوم الدفع" لتعريف متى يجب تعيين الرسوم كافتراضية في دفتر اليومية الذي قمت بتحديده.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="a2b1b-123">حدد "الجدول" أو "المجموعة" أو "الكل".</span><span class="sxs-lookup"><span data-stu-id="a2b1b-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="a2b1b-124">يُستخدم خيار "الجدول" لتحديد حساب بنكي واحد, ويُستخدم خيار "المجموعة" لتحديد مجموعة بنكية ويُستخدم خيار "الكل" لاستخدام إعداد الرسوم هذا لجميع الحسابات البنكية</span><span class="sxs-lookup"><span data-stu-id="a2b1b-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="a2b1b-125">حدد مجموعة بنكية أو حسابًا بنكيًا.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="a2b1b-126">سوف يعرض البحث المجموعة البنكية إذا قمت بتحديد "المجموعة"، وسيعرض الحسابات البنكية إذا قمت بتحديد "الجدول".</span><span class="sxs-lookup"><span data-stu-id="a2b1b-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="a2b1b-127">حدد طريقة الدفع التي يجب فرض هذه الرسوم عليها.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="a2b1b-128">حدد مواصفات الدفع لطريقة الدفع المحددة.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="a2b1b-129">يتم استخدام مواصفات الدفع مع طرق الدفع التي تتم بواسطة تحويل الأموال إلكترونيًا.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="a2b1b-130">حدد ما إذا كانت الرسوم عبارة عن نسبة مئوية أو مبلغ أو فاصل زمني.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="a2b1b-131">أدخل النسبة المئوية للرسوم أو مبلغ الرسوم.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="a2b1b-132">إذا كانت الرسوم عبارة عن نسبة مئوية، فأدخل النسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="a2b1b-133">وإذا كانت الرسوم عبارة عن مبلغ، فأدخل مبلغ الرسوم.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="a2b1b-134">أما إذا كانت الرسوم عبارة عن "فاصل زمني"، فاستخدم علامة التبويب "الفاصل الزمني" لتحديد الرسوم المتدرجة.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="a2b1b-135">في حقل "عملة الرسوم‬"، حدد العملة التي سيتم فرض الرسوم بها.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="a2b1b-136">هذه العملة تتعلق بالرسوم.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-136">This currency is for the fee.</span></span> <span data-ttu-id="a2b1b-137">يتم استخدام عملة الدفع لتعريف متى ينبغي أن يتم تقييم قاعدة الرسوم استنادًا إلى عملة الدفع.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="a2b1b-138">على سبيل المثال، قد يفرض عليك البنك رسومًا عند إجراء الدفع باليورو، ولكن لا يتم فرض أي رسوم على جميع المدفوعات الأخرى.</span><span class="sxs-lookup"><span data-stu-id="a2b1b-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="a2b1b-139">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="a2b1b-139">Click Save.</span></span>

