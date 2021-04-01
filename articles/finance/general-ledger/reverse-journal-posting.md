---
title: عكس ترحيل دفتر اليومية
description: يصف هذا الموضوع القدرات التي تتيح لك عكس الإيصالات من قائمة  حركات الإيصال أو من دفاتر اليومية المالية.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19f7ea540035a3bc9eba445c508cb6f29e4bd20f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204992"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="d82c3-103">عكس ترحيل دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="d82c3-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d82c3-104">يصف هذا الموضوع إمكانيات Dynamics 365 Finance Microsoft التي تتيح لك إلغاء دفتر يومية بأكمله أو عكس إيصال واحد أو أكثر من قائمة حركات الإيصال بغض النظر عن أصلهما.</span><span class="sxs-lookup"><span data-stu-id="d82c3-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="d82c3-105">عكس دفاتر اليومية</span><span class="sxs-lookup"><span data-stu-id="d82c3-105">Reversing journals</span></span>

<span data-ttu-id="d82c3-106">يمكن عكس بنود دفتر اليومية بشكل فردي.</span><span class="sxs-lookup"><span data-stu-id="d82c3-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="d82c3-107">باستخدام عمليه الترحيل العكسي لدفتر اليومية، يمكنك أيضا عكس دفتر اليومية المالي بأكمله.</span><span class="sxs-lookup"><span data-stu-id="d82c3-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="d82c3-108">لعكس دفتر اليومية:</span><span class="sxs-lookup"><span data-stu-id="d82c3-108">To reverse a journal:</span></span> 

- <span data-ttu-id="d82c3-109">فتح دفتر اليومية المالي والتصفية من خلال دفاتر اليومية المرحلة.</span><span class="sxs-lookup"><span data-stu-id="d82c3-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="d82c3-110">حدد القائمة **عكس** الموجودة أعلى الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d82c3-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="d82c3-111">ستشاهد العدد الإجمالي للإيصالات وبنود الإيصالات بالإضافة إلى المبلغ الإجمالي للبنود التي يتم عكسها</span><span class="sxs-lookup"><span data-stu-id="d82c3-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="d82c3-112">حدد **نعم** لاستخدام تواريخ الحركة الموجودة أو **لا** لإدخال تواريخ جديدة.</span><span class="sxs-lookup"><span data-stu-id="d82c3-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="d82c3-113">في بعض الحالات، قد يتم إغلاق فترة الحركة الأصلية ويجب عليك إدخال تاريخ حركة جديد لعمليه العكس.</span><span class="sxs-lookup"><span data-stu-id="d82c3-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="d82c3-114">إذا قمت بتحديد **لا**، أدخل تاريخ الحركة التي تريد عكسها.</span><span class="sxs-lookup"><span data-stu-id="d82c3-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="d82c3-115">أدخل التعليق الذي ترغب في إضافته إلى حركه العكس.</span><span class="sxs-lookup"><span data-stu-id="d82c3-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="d82c3-116">حدد الزر **عكس**.</span><span class="sxs-lookup"><span data-stu-id="d82c3-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="d82c3-117">سيتم عكس الحركات.</span><span class="sxs-lookup"><span data-stu-id="d82c3-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="d82c3-118">إذا كان الإيصال أكثر من 100 بند، فسوف يتم تشغيل عملية العكس باستخدام معالجة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="d82c3-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="d82c3-119">يمكنك مراجعة النتائج عن طريق عرض التعليقات في الوظيفة الدفعية.</span><span class="sxs-lookup"><span data-stu-id="d82c3-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="d82c3-120">سيتم سرد أية حركات يتعذر إلغاؤها في سجل الوظائف الجمعية.</span><span class="sxs-lookup"><span data-stu-id="d82c3-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="d82c3-121">إذا كان الإيصال يحتوي على 100 بند أو أقل، سيتم تشغيل عملية العكس فورًا.</span><span class="sxs-lookup"><span data-stu-id="d82c3-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="d82c3-122">سيتم تقديم النتائج في مربع حوار يعرض أية إيصالات تعذر عكسها، مع ذكر سبب تعذر عملية العكس.</span><span class="sxs-lookup"><span data-stu-id="d82c3-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="d82c3-123">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="d82c3-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="d82c3-124">عكس الإيصالات من قائمة  حركات الإيصال.</span><span class="sxs-lookup"><span data-stu-id="d82c3-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="d82c3-125">يمكنك أيضا عكس الإيصالات من **قائمه حركات الإيصال** عبر كافة دفاتر الأستاذ الفرعية.</span><span class="sxs-lookup"><span data-stu-id="d82c3-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="d82c3-126">بالإضافة إلى ذلك، يمكنك عكس إيصال واحد في كل مرة.</span><span class="sxs-lookup"><span data-stu-id="d82c3-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="d82c3-127">لعكس إيصال واحد أو أكثر:</span><span class="sxs-lookup"><span data-stu-id="d82c3-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="d82c3-128">حدد القائمة **عكس** الموجودة أعلى الصفحة</span><span class="sxs-lookup"><span data-stu-id="d82c3-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="d82c3-129">ستشاهد العدد الإجمالي للإيصالات وبنود الإيصالات بالإضافة إلى المبلغ الإجمالي للبنود التي يتم عكسها.</span><span class="sxs-lookup"><span data-stu-id="d82c3-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="d82c3-130">حدد **نعم** لاستخدام تواريخ الحركة الموجودة أو **لا** لإدخال تواريخ جديدة.</span><span class="sxs-lookup"><span data-stu-id="d82c3-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="d82c3-131">في بعض الحالات، قد يتم إغلاق فترة الحركة الأصلية ويجب عليك إدخال تاريخ حركة جديدة لعكسها.</span><span class="sxs-lookup"><span data-stu-id="d82c3-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="d82c3-132">إذا قمت بتحديد **لا**، أدخل تاريخ الحركة التي تريد عكسها.</span><span class="sxs-lookup"><span data-stu-id="d82c3-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="d82c3-133">أدخل تعليقًا لوصف حركة العكس.</span><span class="sxs-lookup"><span data-stu-id="d82c3-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="d82c3-134">حدد الزر **عكس**.</span><span class="sxs-lookup"><span data-stu-id="d82c3-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="d82c3-135">سيتم عكس الحركات.</span><span class="sxs-lookup"><span data-stu-id="d82c3-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="d82c3-136">إذا كان هناك أكثر من 100 بند في الإيصال، فسوف يتم تشغيل عملية العكس باستخدام معالجة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="d82c3-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="d82c3-137">يمكنك مراجعة النتائج عن طريق عرض التعليقات في الوظيفة الدفعية.</span><span class="sxs-lookup"><span data-stu-id="d82c3-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="d82c3-138">ستتم ملاحظة أية حركات يتعذر إلغاؤها في سجل الوظائف الجمعية.</span><span class="sxs-lookup"><span data-stu-id="d82c3-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="d82c3-139">إذا كان عدد بنود الإيصال 100 بند أو أقل، سيتم تشغيل عملية العكس فورًا.</span><span class="sxs-lookup"><span data-stu-id="d82c3-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="d82c3-140">سيتم عرض النتائج في مربع حوار يعرض أية إيصالات تعذر عكسها، مع ذكر السبب.</span><span class="sxs-lookup"><span data-stu-id="d82c3-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="d82c3-141">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="d82c3-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="d82c3-142">يمكن عكس الحركات فقط إذا كانت تفي بقواعد الأعمال لعكسها.</span><span class="sxs-lookup"><span data-stu-id="d82c3-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="d82c3-143">يتعذر عكس مدفوعات المورد باستخدام القدرة الموضحة في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="d82c3-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="d82c3-144">يجب أن يتم عكس مدفوعات المورد باتباع الخطوات المذكورة في [إلغاء دفعة مورد](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span><span class="sxs-lookup"><span data-stu-id="d82c3-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]