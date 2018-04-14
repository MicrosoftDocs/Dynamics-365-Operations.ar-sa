--- 
title: "تسوية شيك بتاريخ لاحق لمورد"
description: "قم بتسوية الشيك الذي تم إصداره بتاريخ لاحق إلى المورد عند قيام البنك بتسوية حركة الشيك بعد أن يصبح الشيك متأخرًا وتتم تسويته من قبل البنك."
author: kweekley
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
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 80ee7ea11c42c2f6bd7b3be8b0aa72b11fa0f0dd
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="2f513-103">تسوية شيك بتاريخ لاحق لمورد</span><span class="sxs-lookup"><span data-stu-id="2f513-103">Settle a postdated check for a vendor</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2f513-104">قم بتسوية الشيك الذي تم إصداره بتاريخ لاحق إلى المورد عند قيام البنك بتسوية حركة الشيك بعد أن يصبح الشيك متأخرًا وتتم تسويته من قبل البنك.</span><span class="sxs-lookup"><span data-stu-id="2f513-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="2f513-105">قم باستكمال الإجراءات التالية قبل البدء في هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="2f513-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="2f513-106">إعداد شيكات بتاريخ لاحق</span><span class="sxs-lookup"><span data-stu-id="2f513-106">Set up postdated checks</span></span>

2) <span data-ttu-id="2f513-107">تسجيل شيك بتاريخ لاحق لمورد وترحيله</span><span class="sxs-lookup"><span data-stu-id="2f513-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="2f513-108">ويتمثل دور هذا الإجراء في أمين الخزانة.</span><span class="sxs-lookup"><span data-stu-id="2f513-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="2f513-109">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="2f513-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="2f513-110">انتقل إلى الحسابات الدائنة > المدفوعات > ‏‫شيكات الموردين بتواريخ لاحقة.</span><span class="sxs-lookup"><span data-stu-id="2f513-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="2f513-111">انقر فوق "تسوية".</span><span class="sxs-lookup"><span data-stu-id="2f513-111">Click Settle.</span></span>
3. <span data-ttu-id="2f513-112">انقر فوق "تسوية إدخالات التسوية".</span><span class="sxs-lookup"><span data-stu-id="2f513-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="2f513-113">قم بتسوية حساب المورد لحركة الشيك.</span><span class="sxs-lookup"><span data-stu-id="2f513-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="2f513-114">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2f513-114">Close the page.</span></span>
5. <span data-ttu-id="2f513-115">انتقل إلى دفتر الأستاذ العام > إدخالات دفتر اليومية > دفاتر اليومية العامة‬.</span><span class="sxs-lookup"><span data-stu-id="2f513-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="2f513-116">في حقل "إظهار"، حدد "الكل".</span><span class="sxs-lookup"><span data-stu-id="2f513-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="2f513-117">حدد خانة اختيار "إظهار العناصر التي أنشاها المستخدم فقط" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="2f513-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="2f513-118">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2f513-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="2f513-119">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="2f513-119">Click Lines.</span></span>
10. <span data-ttu-id="2f513-120">انقر فوق "الإيصال".</span><span class="sxs-lookup"><span data-stu-id="2f513-120">Click Voucher.</span></span>
11. <span data-ttu-id="2f513-121">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2f513-121">Close the page.</span></span>


