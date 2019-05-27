---
title: نظرة عامة على مدفوعات العملاء
description: يوضح دليل المهام هذا مختلف الطرق التي تُستخدم لإدخال مدفوعات العميل.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e82be0d68165f62bbdc72a70b0675c7418b14ae
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566123"
---
# <a name="customer-payment-overview"></a><span data-ttu-id="37823-103">نظرة عامة على مدفوعات العملاء</span><span class="sxs-lookup"><span data-stu-id="37823-103">Customer payment overview</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37823-104">يوضح دليل المهام هذا مختلف الطرق التي تُستخدم لإدخال مدفوعات العميل.</span><span class="sxs-lookup"><span data-stu-id="37823-104">This task guide walks through various methods used to enter customer payments.</span></span> <span data-ttu-id="37823-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="37823-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="37823-106">انتقل إلى الحسابات المدينة > المدفوعات‬ > دفتر يومية المدفوعات‬‬.</span><span class="sxs-lookup"><span data-stu-id="37823-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="37823-107">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="37823-107">Click New.</span></span>
3. <span data-ttu-id="37823-108">حدد دفتر يومية المدفوعات الذي ستُحفظ به مدفوعات العميل.</span><span class="sxs-lookup"><span data-stu-id="37823-108">Select the payment journal which the customer payments will be saved.</span></span>
4. <span data-ttu-id="37823-109">حدد دفتر اليومية أو قم بإدخاله يدوياً.</span><span class="sxs-lookup"><span data-stu-id="37823-109">Select or manually enter the journal.</span></span>
5. <span data-ttu-id="37823-110">انقر فوق إدخال مدفوعات العميل.</span><span class="sxs-lookup"><span data-stu-id="37823-110">Click Enter customer payments.</span></span>
    * <span data-ttu-id="37823-111">يستخدم خيار "إدخال مدفوعات العميل" لتسجيل مدفوعات عميل واحد في كل مرة.</span><span class="sxs-lookup"><span data-stu-id="37823-111">Enter customer payments is used to record one customer payment at a time.</span></span> <span data-ttu-id="37823-112">تقوم بإدخال معلومات الدفع في الجزء العلوي، ثم يمكنك وضع علامة تميز بها الفواتير التي تم دفعها خلال عملية الدفع، وتقوم بذلك كله من نفس الصفحة.</span><span class="sxs-lookup"><span data-stu-id="37823-112">You enter the payment information at the top, and then you can mark the invoices that were paid by the payment, all from the same page.</span></span>  
6. <span data-ttu-id="37823-113">أدخل اسم العميل الذي تلقيت الدفع منه.</span><span class="sxs-lookup"><span data-stu-id="37823-113">Enter the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="37823-114">إذا لم تكن تعرف العميل، ولكنك تعرف الحركة التي تم دفعها، يمكنك استخدام حقل "الحركة" لإدخال الدفع.</span><span class="sxs-lookup"><span data-stu-id="37823-114">If you don't know the customer but do know a transaction that was paid, you can use the Transaction field to enter the payment.</span></span> <span data-ttu-id="37823-115">قم بإدخال أو تحديد الفاتورة في حقل "الحركة".</span><span class="sxs-lookup"><span data-stu-id="37823-115">Enter or select the invoice in the Transaction field.</span></span> <span data-ttu-id="37823-116">سوف يتم تعيين العميل افتراضيًا بشكل تلقائي بعد تحديد الحركة.</span><span class="sxs-lookup"><span data-stu-id="37823-116">The customer will automatically default after you select the transaction.</span></span>  
7. <span data-ttu-id="37823-117">في الحقل "مرجع الدفع"، أدخل مرجع الدفع.</span><span class="sxs-lookup"><span data-stu-id="37823-117">In the Payment reference field, enter a payment reference.</span></span>
    * <span data-ttu-id="37823-118">قد يكون مرجع الدفع هو رقم الشيك الخاص بالعميل أو مرجع من الدفع الإلكتروني الخاص بالعميل.</span><span class="sxs-lookup"><span data-stu-id="37823-118">The payment reference could be the customer's check number or a reference from the customer's electronic payment.</span></span> <span data-ttu-id="37823-119">ويكون مرجع الدفع مطلوبًا فقط إذا قمت بوضع علامة لاختيار تضمين الدفع في إيصال الإيداع.</span><span class="sxs-lookup"><span data-stu-id="37823-119">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="37823-120">حدد ما إذا كان سيتم تضمين الدفع في قسيمة إيداع.</span><span class="sxs-lookup"><span data-stu-id="37823-120">Select whether the payment will be included on a deposit slip.</span></span> 
9. <span data-ttu-id="37823-121">أدخل مبلغ دفع العميل.</span><span class="sxs-lookup"><span data-stu-id="37823-121">Enter the amount of the customer payment.</span></span>
    * <span data-ttu-id="37823-122">ولن يُعين مبلغ الدفع افتراضيًا.</span><span class="sxs-lookup"><span data-stu-id="37823-122">The payment amount will not default.</span></span> <span data-ttu-id="37823-123">بل يجب إدخاله يدوياً.</span><span class="sxs-lookup"><span data-stu-id="37823-123">It must be manually entered.</span></span>  
10. <span data-ttu-id="37823-124">قم بوضع علامة على الفواتير التي دُفعت بواسطة العميل.</span><span class="sxs-lookup"><span data-stu-id="37823-124">Mark the invoices that were paid by the customer.</span></span>
    * <span data-ttu-id="37823-125">إذا كان الدفع في صورة دفعة مقدمة، فلن تضطر إلى وضع علامة لتمييز أية فواتير للتسوية.</span><span class="sxs-lookup"><span data-stu-id="37823-125">If the payment is a prepayment, you are not required to mark any invoices for settlement.</span></span> <span data-ttu-id="37823-126">ولا يزال من الممكن حفظ الدفع وترحيله.</span><span class="sxs-lookup"><span data-stu-id="37823-126">The payment can still be saved and posted.</span></span> <span data-ttu-id="37823-127">وقد تحدث تسوية إحدى الفواتير في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="37823-127">Settlement to an invoice can happen at a later time.</span></span>  
11. <span data-ttu-id="37823-128">أدخل مبلغ الدفع المطلوب تسويته للفاتورة المميزة بعلامة.</span><span class="sxs-lookup"><span data-stu-id="37823-128">Enter the amount of the payment that should be settled to the marked invoice.</span></span> 
    * <span data-ttu-id="37823-129">يمكن استخدام هذا الحقل عندما يكون الدفع خاص بدفع جزئي.</span><span class="sxs-lookup"><span data-stu-id="37823-129">This field can be used when the payment is for a partial payment.</span></span> <span data-ttu-id="37823-130">إذا لم يتم إدخال مبلغ، سيُحدد المبلغ المراد تسويته تلقائياً.</span><span class="sxs-lookup"><span data-stu-id="37823-130">If you don't enter an amount, the amount to settle will automatically be determined for you.</span></span>  
12. <span data-ttu-id="37823-131">انقر فوق "حفظ" في دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="37823-131">Click Save in journal.</span></span>
    * <span data-ttu-id="37823-132">قبل حفظ الدفع في دفتر اليومية، تأكد من تحديد الحساب المقابل.</span><span class="sxs-lookup"><span data-stu-id="37823-132">Before you save the payment to the journal, make sure that the offset account is defined.</span></span> <span data-ttu-id="37823-133">سيؤدي استخدام خيار الحفظ في دفتر اليومية إلى حفظ الدفع ونقله إلى دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="37823-133">Using Save in journal will save the payment and move it to the journal.</span></span> <span data-ttu-id="37823-134">ثم يمكنك المتابعة بإدخال الدفع التالي.</span><span class="sxs-lookup"><span data-stu-id="37823-134">You can then continue entering the next payment.</span></span>  
13. <span data-ttu-id="37823-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="37823-135">Close the page.</span></span>
14. <span data-ttu-id="37823-136">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="37823-136">Click Lines.</span></span>
    * <span data-ttu-id="37823-137">عند فتح البنود، ستشاهد أية مدفوعات سجلتَها على صفحة "إدخال مدفوعات العميل" وحفظتَها في دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="37823-137">When opening Lines, you will see any payments you recorded on the Enter customer payments page and saved into the journal.</span></span> <span data-ttu-id="37823-138">ويمكنك أيضًا استخدام هذه الصفحة لإدخال مدفوعات عميل جديدة أو تحرير دفع عميل موجود قبل ترحيله.</span><span class="sxs-lookup"><span data-stu-id="37823-138">You can also use this page to enter new customer payments, or edit existing customer payment before they are posted.</span></span>  
15. <span data-ttu-id="37823-139">انقر فوق "جديد" لإنشاء دفع آخر.</span><span class="sxs-lookup"><span data-stu-id="37823-139">Click New to create another payment.</span></span> 
16. <span data-ttu-id="37823-140">حدد العميل الذي تلقيت الدفع منه.</span><span class="sxs-lookup"><span data-stu-id="37823-140">Select the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="37823-141">إذا لم تكن تعرف العميل ولكن تعرف إحدى الفواتير المدفوعة عبر الدفع، فاستخدم الحقل "الفاتورة" لإدخال الفاتورة يدوياً أو تحديدها.</span><span class="sxs-lookup"><span data-stu-id="37823-141">If you don't know the customer but know an invoice paid by the payment, use the Invoice field to manually enter or select the invoice.</span></span> <span data-ttu-id="37823-142">سيتم تعيين العميل افتراضيًا بعد تحديد الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="37823-142">The customer will default after the invoice is selected.</span></span>  
17. <span data-ttu-id="37823-143">انقر فوق "تسوية الحركات" لتمييز الفواتير التي تم دفعها بعلامة.</span><span class="sxs-lookup"><span data-stu-id="37823-143">Click Settle transctions to mark invoices that were paid.</span></span>
    * <span data-ttu-id="37823-144">ولن تُضطر إلى تسوية الدفع الخاص بأية فواتير.</span><span class="sxs-lookup"><span data-stu-id="37823-144">You are not required to settle the payment to any invoices.</span></span> <span data-ttu-id="37823-145">إذا كان الدفع في صورة دفعة مقدمة أو كنت لا تعرف الفاتورة التي تم دفعها، يمكنك إدخال الدفع وترحيله.</span><span class="sxs-lookup"><span data-stu-id="37823-145">If this is a prepayment or if you don't know what invoice was paid, you can enter and post the payment.</span></span> <span data-ttu-id="37823-146">يمكن تسوية الدفع لفاتورة في وقت لاحق.</span><span class="sxs-lookup"><span data-stu-id="37823-146">The payment can be settled to an invoice at a later point.</span></span>  
18. <span data-ttu-id="37823-147">قم بتمييز الفواتير المدفوعة بواسطة الدفع بعلامة.</span><span class="sxs-lookup"><span data-stu-id="37823-147">Mark the invoices paid by the payment.</span></span> 
19. <span data-ttu-id="37823-148">أدخل مبلغ الدفع الذي سيتم تسويته للفاتورة.</span><span class="sxs-lookup"><span data-stu-id="37823-148">Enter the amount of the payment that will be settled to the invoice.</span></span>
20. <span data-ttu-id="37823-149">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="37823-149">Click OK.</span></span>
21. <span data-ttu-id="37823-150">في الحقل "مرجع الدفع"، أدخل مرجع الدفع.</span><span class="sxs-lookup"><span data-stu-id="37823-150">In the Payment reference field, Enter a payment reference.</span></span> <span data-ttu-id="37823-151">.</span><span class="sxs-lookup"><span data-stu-id="37823-151">.</span></span>
    * <span data-ttu-id="37823-152">ويكون مرجع الدفع مطلوبًا فقط إذا قمت بوضع علامة لاختيار تضمين الدفع في إيصال الإيداع.</span><span class="sxs-lookup"><span data-stu-id="37823-152">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
22. <span data-ttu-id="37823-153">قم بترحيل مدفوعات العميل.</span><span class="sxs-lookup"><span data-stu-id="37823-153">Post the customer payments.</span></span> 

