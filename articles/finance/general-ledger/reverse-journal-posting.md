---
title: عكس ترحيل دفتر اليومية
description: يصف هذا الموضوع القدرات التي تتيح لك عكس الإيصالات من قائمه حركات الإيصال أو من دفاتر اليومية المالية.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248575"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="1e82d-103">عكس ترحيل دفتر اليومية</span><span class="sxs-lookup"><span data-stu-id="1e82d-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e82d-104">يصف هذا الموضوع إمكانيات Dynamics 365 Finance Microsoft التي تتيح لك إلغاء دفتر يوميه بأكمله أو عكس إيصال واحد أو أكثر من قائمة حركات الإيصال بغض النظر عن أصلهما.</span><span class="sxs-lookup"><span data-stu-id="1e82d-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="1e82d-105">عكس دفاتر اليومية</span><span class="sxs-lookup"><span data-stu-id="1e82d-105">Reversing journals</span></span>

<span data-ttu-id="1e82d-106">يمكن عكس بنود دفتر اليومية بشكل فردي.</span><span class="sxs-lookup"><span data-stu-id="1e82d-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="1e82d-107">باستخدام عمليه الترحيل العكسي لدفتر اليومية، يمكنك أيضا عكس دفتر اليومية المالي بأكمله.</span><span class="sxs-lookup"><span data-stu-id="1e82d-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="1e82d-108">لعكس دفتر اليومية:</span><span class="sxs-lookup"><span data-stu-id="1e82d-108">To reverse a journal:</span></span> 
- <span data-ttu-id="1e82d-109">فتح دفتر اليومية المالي والتصفية من خلال دفاتر اليومية المرحلة</span><span class="sxs-lookup"><span data-stu-id="1e82d-109">Open the financial journal and filter on posted journals</span></span>
- <span data-ttu-id="1e82d-110">انقر على قائمة العكس الموجودة أعلى الصفحة</span><span class="sxs-lookup"><span data-stu-id="1e82d-110">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="1e82d-111">ستشاهد العدد الإجمالي للإيصالات وبنود الإيصالات بالإضافة إلى المبلغ الإجمالي للبنود التي يتم عكسها</span><span class="sxs-lookup"><span data-stu-id="1e82d-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="1e82d-112">حدد "نعم" لاستخدام تواريخ الحركة الموجودة أو "لا" لإدخال تواريخ جديدة.</span><span class="sxs-lookup"><span data-stu-id="1e82d-112">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="1e82d-113">في بعض الحالات، قد يتم إغلاق فترة الحركة الاصليه وترغب في إدخال تاريخ حركة جديد لعمليه العكس.</span><span class="sxs-lookup"><span data-stu-id="1e82d-113">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="1e82d-114">إذا قمت بتحديد لا، ادخل تاريخ الحركة التي تريد عكسها.</span><span class="sxs-lookup"><span data-stu-id="1e82d-114">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="1e82d-115">أدخل التعليق الذي ترغب في إضافته إلى حركه العكس</span><span class="sxs-lookup"><span data-stu-id="1e82d-115">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="1e82d-116">انقر فوق زر العكس</span><span class="sxs-lookup"><span data-stu-id="1e82d-116">Click the Reverse button</span></span>

<span data-ttu-id="1e82d-117">سيتم عكس الحركات.</span><span class="sxs-lookup"><span data-stu-id="1e82d-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="1e82d-118">إذا تجاوز عدد بنود الإيصال 100 بند، فسوف يتم تشغيل عملية العكس باستخدام معالجة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="1e82d-118">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="1e82d-119">يمكنك مراجعه نتائج عملية العكس عن طريق عرض التعليقات في الوظيفة الدفعية التي تم تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="1e82d-119">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="1e82d-120">ستتم ملاحظه كافة حالات الإخفاق في سجل الوظيفة الدفعية.</span><span class="sxs-lookup"><span data-stu-id="1e82d-120">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="1e82d-121">إذا كان عدد بنود الإيصال 100 بند أو اقل، سيتم تشغيل عمليه العكس فورًا.</span><span class="sxs-lookup"><span data-stu-id="1e82d-121">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="1e82d-122">سيتم تقديم النتائج في مربع حوار يعرض أي إيصالات تعذر عكسها وسبب تعذر عملية العكس.</span><span class="sxs-lookup"><span data-stu-id="1e82d-122">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="1e82d-123">انقر فوق موافق لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="1e82d-123">Click on Ok to close the dialog.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="1e82d-124">عكس الإيصالات من قائمه حركات الإيصال.</span><span class="sxs-lookup"><span data-stu-id="1e82d-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="1e82d-125">يمكنك أيضا عكس الإيصالات من **قائمه حركات الإيصال** عبر كافة دفاتر الأستاذ الفرعية.</span><span class="sxs-lookup"><span data-stu-id="1e82d-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="1e82d-126">بالإضافة إلى ذلك، يمكنك عكس إيصال واحد في كل مرة.</span><span class="sxs-lookup"><span data-stu-id="1e82d-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="1e82d-127">لعكس إيصال واحد أو أكثر:</span><span class="sxs-lookup"><span data-stu-id="1e82d-127">To reverse one or more vouchers:</span></span> 
- <span data-ttu-id="1e82d-128">انقر على قائمة العكس الموجودة أعلى الصفحة</span><span class="sxs-lookup"><span data-stu-id="1e82d-128">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="1e82d-129">ستشاهد العدد الإجمالي للإيصالات وبنود الإيصالات بالإضافة إلى المبلغ الإجمالي للبنود التي يتم عكسها</span><span class="sxs-lookup"><span data-stu-id="1e82d-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="1e82d-130">حدد "نعم" لاستخدام تواريخ الحركة الموجودة أو "لا" لإدخال تواريخ جديدة.</span><span class="sxs-lookup"><span data-stu-id="1e82d-130">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="1e82d-131">في بعض الحالات، قد يتم إغلاق فترة الحركة الاصليه وترغب في إدخال تاريخ حركة جديد لعمليه العكس.</span><span class="sxs-lookup"><span data-stu-id="1e82d-131">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="1e82d-132">إذا قمت بتحديد لا، ادخل تاريخ الحركة التي تريد عكسها.</span><span class="sxs-lookup"><span data-stu-id="1e82d-132">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="1e82d-133">أدخل التعليق الذي ترغب في إضافته إلى حركه العكس</span><span class="sxs-lookup"><span data-stu-id="1e82d-133">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="1e82d-134">انقر فوق زر العكس</span><span class="sxs-lookup"><span data-stu-id="1e82d-134">Click the Reverse button</span></span>

<span data-ttu-id="1e82d-135">سيتم عكس الحركات.</span><span class="sxs-lookup"><span data-stu-id="1e82d-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="1e82d-136">إذا تجاوز عدد بنود الإيصال 100 بند، فسوف يتم تشغيل عملية العكس باستخدام معالجة الدُفعة.</span><span class="sxs-lookup"><span data-stu-id="1e82d-136">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="1e82d-137">يمكنك مراجعه نتائج عملية العكس عن طريق عرض التعليقات في الوظيفة الدفعية التي تم تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="1e82d-137">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="1e82d-138">ستتم ملاحظه كافة حالات الإخفاق في سجل الوظيفة الدفعية.</span><span class="sxs-lookup"><span data-stu-id="1e82d-138">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="1e82d-139">إذا كان عدد بنود الإيصال 100 بند أو اقل، سيتم تشغيل عمليه العكس فورًا.</span><span class="sxs-lookup"><span data-stu-id="1e82d-139">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="1e82d-140">سيتم تقديم النتائج في مربع حوار يعرض أي إيصالات تعذر عكسها وسبب تعذر عملية العكس.</span><span class="sxs-lookup"><span data-stu-id="1e82d-140">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="1e82d-141">انقر فوق موافق لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="1e82d-141">Click on Ok to close the dialog.</span></span>

