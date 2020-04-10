---
title: تسوية شيك بتاريخ لاحق لمورد
description: قم بتسوية الشيك الذي تم إصداره بتاريخ لاحق إلى المورد عند قيام البنك بتسوية حركة الشيك بعد أن يصبح الشيك متأخرًا وتتم تسويته من قبل البنك.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee66bdb93d1252486efc7be25adeb6ee7cc6ce05
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144223"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="01f35-103">تسوية شيك بتاريخ لاحق لمورد</span><span class="sxs-lookup"><span data-stu-id="01f35-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01f35-104">قم بتسوية الشيك الذي تم إصداره بتاريخ لاحق إلى المورد عند قيام البنك بتسوية حركة الشيك بعد أن يصبح الشيك متأخرًا وتتم تسويته من قبل البنك.</span><span class="sxs-lookup"><span data-stu-id="01f35-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="01f35-105">قم باستكمال الإجراءات التالية قبل البدء في هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="01f35-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="01f35-106">إعداد شيكات بتاريخ لاحق</span><span class="sxs-lookup"><span data-stu-id="01f35-106">Set up postdated checks</span></span>

2) <span data-ttu-id="01f35-107">تسجيل شيك بتاريخ لاحق لمورد وترحيله</span><span class="sxs-lookup"><span data-stu-id="01f35-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="01f35-108">ويتمثل دور هذا الإجراء في أمين الخزانة.</span><span class="sxs-lookup"><span data-stu-id="01f35-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="01f35-109">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="01f35-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="01f35-110">انتقل إلى الحسابات الدائنة > المدفوعات > ‏‫شيكات الموردين بتواريخ لاحقة.</span><span class="sxs-lookup"><span data-stu-id="01f35-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="01f35-111">انقر فوق "تسوية".</span><span class="sxs-lookup"><span data-stu-id="01f35-111">Click Settle.</span></span>
3. <span data-ttu-id="01f35-112">انقر فوق "تسوية إدخالات التسوية".</span><span class="sxs-lookup"><span data-stu-id="01f35-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="01f35-113">قم بتسوية حساب المورد لحركة الشيك.</span><span class="sxs-lookup"><span data-stu-id="01f35-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="01f35-114">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="01f35-114">Close the page.</span></span>
5. <span data-ttu-id="01f35-115">انتقل إلى دفتر الأستاذ العام > إدخالات دفتر اليومية > دفاتر اليومية العامة‬.</span><span class="sxs-lookup"><span data-stu-id="01f35-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="01f35-116">في حقل "إظهار"، حدد "الكل".</span><span class="sxs-lookup"><span data-stu-id="01f35-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="01f35-117">حدد خانة اختيار "إظهار العناصر التي أنشاها المستخدم فقط" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="01f35-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="01f35-118">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="01f35-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="01f35-119">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="01f35-119">Click Lines.</span></span>
10. <span data-ttu-id="01f35-120">انقر فوق "الإيصال".</span><span class="sxs-lookup"><span data-stu-id="01f35-120">Click Voucher.</span></span>
11. <span data-ttu-id="01f35-121">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="01f35-121">Close the page.</span></span>

