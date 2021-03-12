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
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7f8f2f8fe0dfd0eccd61ef76242e2a77c75b3983
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976231"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="c40e6-103">تسوية شيك بتاريخ لاحق من عميل</span><span class="sxs-lookup"><span data-stu-id="c40e6-103">Settle a postdated check from a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c40e6-104">يمكنك تسوية شيك بتاريخ لاحق بعد أن تتم تسوية الشيك من قبل البنك.</span><span class="sxs-lookup"><span data-stu-id="c40e6-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="c40e6-105">تعمل هذه الحركة المالية أيضًا على تسوية حركة الحساب الوسيط للشيك بتاريخ لاحق.</span><span class="sxs-lookup"><span data-stu-id="c40e6-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="c40e6-106">يجب إكمال المهام التالية قبل بدء هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="c40e6-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="c40e6-107">إعداد شيكات بتاريخ لاحق</span><span class="sxs-lookup"><span data-stu-id="c40e6-107">Set up postdated checks</span></span>

2) <span data-ttu-id="c40e6-108">تسجيل شيك بتاريخ لاحق لعميل وترحيله</span><span class="sxs-lookup"><span data-stu-id="c40e6-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="c40e6-109">ويتمثل دور دلائل المهام هذه في أمين الخزانة.</span><span class="sxs-lookup"><span data-stu-id="c40e6-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="c40e6-110">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="c40e6-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="c40e6-111">انتقل إلى الائتمان والتحصيلات > الاستعلامات والتقارير > المدفوعات > شيكات العميل ذات التواريخ اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="c40e6-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="c40e6-112">انقر فوق "تسوية".</span><span class="sxs-lookup"><span data-stu-id="c40e6-112">Click Settle.</span></span>
3. <span data-ttu-id="c40e6-113">انقر فوق "تسوية إدخالات التسوية".</span><span class="sxs-lookup"><span data-stu-id="c40e6-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="c40e6-114">قم بتسوية حساب العميل لحركة الشيك.</span><span class="sxs-lookup"><span data-stu-id="c40e6-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="c40e6-115">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c40e6-115">Close the page.</span></span>
5. <span data-ttu-id="c40e6-116">انتقل إلى دفتر الأستاذ العام > إدخالات دفتر اليومية > دفاتر اليومية العامة‬.</span><span class="sxs-lookup"><span data-stu-id="c40e6-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="c40e6-117">في الحقل "إظهار"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="c40e6-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="c40e6-118">حدد خانة اختيار "إظهار العناصر التي أنشاها المستخدم فقط" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="c40e6-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="c40e6-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c40e6-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="c40e6-120">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="c40e6-120">Click Lines.</span></span>
10. <span data-ttu-id="c40e6-121">انقر فوق "الإيصال".</span><span class="sxs-lookup"><span data-stu-id="c40e6-121">Click Voucher.</span></span>
11. <span data-ttu-id="c40e6-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c40e6-122">Close the page.</span></span>

