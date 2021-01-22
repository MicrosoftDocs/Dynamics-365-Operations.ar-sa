---
title: تسوية شيك بتاريخ لاحق من عميل
description: يمكنك تسوية شيك بتاريخ لاحق بعد أن تتم تسوية الشيك من قبل البنك.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bc6f90e7adb3facdfa1facb50fecb0de4ccb04d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141570"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="fe8f5-103">تسوية شيك بتاريخ لاحق من عميل</span><span class="sxs-lookup"><span data-stu-id="fe8f5-103">Settle a postdated check from a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fe8f5-104">يمكنك تسوية شيك بتاريخ لاحق بعد أن تتم تسوية الشيك من قبل البنك.</span><span class="sxs-lookup"><span data-stu-id="fe8f5-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="fe8f5-105">تعمل هذه الحركة المالية أيضًا على تسوية حركة الحساب الوسيط للشيك بتاريخ لاحق.</span><span class="sxs-lookup"><span data-stu-id="fe8f5-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="fe8f5-106">يجب إكمال المهام التالية قبل بدء هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="fe8f5-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="fe8f5-107">إعداد شيكات بتاريخ لاحق</span><span class="sxs-lookup"><span data-stu-id="fe8f5-107">Set up postdated checks</span></span>

2) <span data-ttu-id="fe8f5-108">تسجيل شيك بتاريخ لاحق لعميل وترحيله</span><span class="sxs-lookup"><span data-stu-id="fe8f5-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="fe8f5-109">ويتمثل دور دلائل المهام هذه في أمين الخزانة.</span><span class="sxs-lookup"><span data-stu-id="fe8f5-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="fe8f5-110">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="fe8f5-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="fe8f5-111">انتقل إلى الائتمان والتحصيلات > الاستعلامات والتقارير > المدفوعات > شيكات العميل ذات التواريخ اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="fe8f5-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="fe8f5-112">انقر فوق "تسوية".</span><span class="sxs-lookup"><span data-stu-id="fe8f5-112">Click Settle.</span></span>
3. <span data-ttu-id="fe8f5-113">انقر فوق "تسوية إدخالات التسوية".</span><span class="sxs-lookup"><span data-stu-id="fe8f5-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="fe8f5-114">قم بتسوية حساب العميل لحركة الشيك.</span><span class="sxs-lookup"><span data-stu-id="fe8f5-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="fe8f5-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fe8f5-115">Close the page.</span></span>
5. <span data-ttu-id="fe8f5-116">انتقل إلى دفتر الأستاذ العام > إدخالات دفتر اليومية > دفاتر اليومية العامة‬.</span><span class="sxs-lookup"><span data-stu-id="fe8f5-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="fe8f5-117">في الحقل "إظهار"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="fe8f5-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="fe8f5-118">حدد خانة اختيار "إظهار العناصر التي أنشاها المستخدم فقط" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="fe8f5-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="fe8f5-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="fe8f5-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="fe8f5-120">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="fe8f5-120">Click Lines.</span></span>
10. <span data-ttu-id="fe8f5-121">انقر فوق "الإيصال".</span><span class="sxs-lookup"><span data-stu-id="fe8f5-121">Click Voucher.</span></span>
11. <span data-ttu-id="fe8f5-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="fe8f5-122">Close the page.</span></span>
