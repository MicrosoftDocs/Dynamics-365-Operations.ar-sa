---
title: ‏‫معالجة دفتر يومية توزيع دفتر الأستاذ‬
description: استخدم صفحة طلب تخصيص العملية لإنشاء دفتر يومية تخصيص يمكن مراجعته واعتماده قبل الترحيل إلى دفتر الأستاذ العام أو ترحيله مباشرةً إلى دفتر الأستاذ العام.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2046e25719c9023bee99736488a4ee6f22723fe
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "335636"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="c3f84-103">‏‫معالجة دفتر يومية توزيع دفتر الأستاذ‬</span><span class="sxs-lookup"><span data-stu-id="c3f84-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c3f84-104">استخدم صفحة طلب تخصيص العملية لإنشاء دفتر يومية تخصيص يمكن مراجعته واعتماده قبل الترحيل إلى دفتر الأستاذ العام أو ترحيله مباشرةً إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="c3f84-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="c3f84-105">قبل أن تتمكن من إنشاء دفتر يومية التخصيصات، يجب أن تتوفر قاعدة واحدة نشطة على الأقل لتخصيص دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="c3f84-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="c3f84-106">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="c3f84-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c3f84-107">انتقل إلى دفتر الأستاذ العام > التوزيعات > طلب توزيع العملية.</span><span class="sxs-lookup"><span data-stu-id="c3f84-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="c3f84-108">في الحقل "القاعدة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c3f84-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c3f84-109">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c3f84-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c3f84-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c3f84-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c3f84-111">في الحقل "تاريخ البدء" أدخل تاريخاً.</span><span class="sxs-lookup"><span data-stu-id="c3f84-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="c3f84-112">يُعد تاريخ البدء مهمًا جداً عندما يكون دفتر الأستاذ هو مصدر البيانات للقاعدة.</span><span class="sxs-lookup"><span data-stu-id="c3f84-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="c3f84-113">يتحكم هذا التاريخ في دفتر الأستاذ المطلوب تضمينه للتخصيص.</span><span class="sxs-lookup"><span data-stu-id="c3f84-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="c3f84-114">في الحقل "قيمة المصدر صفر" حدد "إيقاف".</span><span class="sxs-lookup"><span data-stu-id="c3f84-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="c3f84-115">يؤدي هذا لإيقاف عملية التخصيص وعرض رسالة توضح أنه تم تحديد مبلغ بقيمة المصدر صفر.</span><span class="sxs-lookup"><span data-stu-id="c3f84-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="c3f84-116">في الحقل "خيارات المقترح" حدد "مقترح فقط".</span><span class="sxs-lookup"><span data-stu-id="c3f84-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="c3f84-117">حدد "مقترح فقط" لمراجعة النتيجة الواردة في دفاتر يومية التخصيص واعتمادها قبل ترحيل التخصيص لدفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="c3f84-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="c3f84-118">في الحقل "ترحيل دفتر الأستاذ العام"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="c3f84-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="c3f84-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c3f84-119">Click OK.</span></span>
9. <span data-ttu-id="c3f84-120">انتقل إلى دفتر الأستاذ العام > التوزيعات > دفاتر يومية التوزيع.</span><span class="sxs-lookup"><span data-stu-id="c3f84-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="c3f84-121">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="c3f84-121">Click Lines.</span></span>
11. <span data-ttu-id="c3f84-122">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="c3f84-122">Click Post.</span></span>
12. <span data-ttu-id="c3f84-123">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="c3f84-123">Click Post.</span></span>

