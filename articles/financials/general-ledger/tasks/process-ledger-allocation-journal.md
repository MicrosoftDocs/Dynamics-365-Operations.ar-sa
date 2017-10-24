--- 
title: "‏‫معالجة دفتر يومية توزيع دفتر الأستاذ‬"
description: "استخدم صفحة طلب تخصيص العملية لإنشاء دفتر يومية تخصيص يمكن مراجعته واعتماده قبل الترحيل إلى دفتر الأستاذ العام أو ترحيله مباشرةً إلى دفتر الأستاذ العام."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7d299657758b1e1322aef07bfe8c71f7bf00b0ca
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="8612b-103">‏‫معالجة دفتر يومية توزيع دفتر الأستاذ‬</span><span class="sxs-lookup"><span data-stu-id="8612b-103">Process ledger allocation journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8612b-104">استخدم صفحة طلب تخصيص العملية لإنشاء دفتر يومية تخصيص يمكن مراجعته واعتماده قبل الترحيل إلى دفتر الأستاذ العام أو ترحيله مباشرةً إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="8612b-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="8612b-105">قبل أن تتمكن من إنشاء دفتر يومية التخصيصات، يجب أن تتوفر قاعدة واحدة نشطة على الأقل لتخصيص دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="8612b-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="8612b-106">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="8612b-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="8612b-107">انتقل إلى دفتر الأستاذ العام > التوزيعات > طلب توزيع العملية.</span><span class="sxs-lookup"><span data-stu-id="8612b-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="8612b-108">في الحقل "القاعدة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="8612b-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="8612b-109">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="8612b-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="8612b-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8612b-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="8612b-111">في الحقل "تاريخ البدء" أدخل تاريخاً.</span><span class="sxs-lookup"><span data-stu-id="8612b-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="8612b-112">يُعد تاريخ البدء مهمًا جداً عندما يكون دفتر الأستاذ هو مصدر البيانات للقاعدة.</span><span class="sxs-lookup"><span data-stu-id="8612b-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="8612b-113">يتحكم هذا التاريخ في دفتر الأستاذ المطلوب تضمينه للتخصيص.</span><span class="sxs-lookup"><span data-stu-id="8612b-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="8612b-114">في الحقل "قيمة المصدر صفر" حدد "إيقاف".</span><span class="sxs-lookup"><span data-stu-id="8612b-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="8612b-115">يؤدي هذا لإيقاف عملية التخصيص وعرض رسالة توضح أنه تم تحديد مبلغ بقيمة المصدر صفر.</span><span class="sxs-lookup"><span data-stu-id="8612b-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="8612b-116">في الحقل "خيارات المقترح" حدد "مقترح فقط".</span><span class="sxs-lookup"><span data-stu-id="8612b-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="8612b-117">حدد "مقترح فقط" لمراجعة النتيجة الواردة في دفاتر يومية التخصيص واعتمادها قبل ترحيل التخصيص لدفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="8612b-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="8612b-118">في الحقل "ترحيل دفتر الأستاذ العام"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="8612b-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="8612b-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="8612b-119">Click OK.</span></span>
9. <span data-ttu-id="8612b-120">انتقل إلى دفتر الأستاذ العام > التوزيعات > دفاتر يومية التوزيع.</span><span class="sxs-lookup"><span data-stu-id="8612b-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="8612b-121">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="8612b-121">Click Lines.</span></span>
11. <span data-ttu-id="8612b-122">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="8612b-122">Click Post.</span></span>
12. <span data-ttu-id="8612b-123">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="8612b-123">Click Post.</span></span>


