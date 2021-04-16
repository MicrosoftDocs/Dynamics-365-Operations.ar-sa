---
title: ‏‫معالجة دفتر يومية توزيع دفتر الأستاذ‬
description: يشرح هذا الموضوع كيفية معالجة طلب تخصيص في Dynamics 365 Finance.
author: aprilolson
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e89aa21f988d50bc1a922e053be0ff2dcd196268
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834395"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="129f3-103">‏‫معالجة دفتر يومية توزيع دفتر الأستاذ‬</span><span class="sxs-lookup"><span data-stu-id="129f3-103">Process ledger allocation journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="129f3-104">يشرح هذا الموضوع كيفية معالجة طلب تخصيص.</span><span class="sxs-lookup"><span data-stu-id="129f3-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="129f3-105">استخدم صفحة طلب تخصيص العملية لإنشاء دفتر يومية تخصيص يمكن مراجعته واعتماده قبل الترحيل إلى دفتر الأستاذ العام أو ترحيله مباشرةً إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="129f3-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="129f3-106">قبل أن تتمكن من إنشاء دفتر يومية التخصيصات، يجب أن تتوفر قاعدة واحدة نشطة على الأقل لتخصيص دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="129f3-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="129f3-107">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="129f3-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="129f3-108">في جزء التنقل، انتقل إلى **الوحدات النمطية > دفتر الأستاذ العام > تخصيصات > طلب تخصيص العملية**.</span><span class="sxs-lookup"><span data-stu-id="129f3-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="129f3-109">في حقل **القاعدة**، حدد السجل المطلوب في القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="129f3-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="129f3-110">أدخل تاريخاً في الحقل **اعتبارًا من تاريخ**.</span><span class="sxs-lookup"><span data-stu-id="129f3-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="129f3-111">يُعد **اعتبارًا من تاريخ** مهمًا جداً عندما يكون دفتر الأستاذ هو مصدر البيانات للقاعدة.</span><span class="sxs-lookup"><span data-stu-id="129f3-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="129f3-112">يتحكم هذا التاريخ في دفتر الأستاذ المطلوب تضمينه للتخصيص.</span><span class="sxs-lookup"><span data-stu-id="129f3-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="129f3-113">في الحقل **قيمة المصدر صفر** حدد **إيقاف**.</span><span class="sxs-lookup"><span data-stu-id="129f3-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="129f3-114">يؤدي هذا إلى إيقاف عملية التخصيص وعرض رسالة توضح أنه تم تحديد مبلغ بقيمة المصدر صفر.</span><span class="sxs-lookup"><span data-stu-id="129f3-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="129f3-115">في الحقل **خيارات المقترح**، حدد **مقترح فقط**.</span><span class="sxs-lookup"><span data-stu-id="129f3-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="129f3-116">حدد **مقترح فقط** لمراجعة النتيجة الواردة في دفاتر يومية التخصيص واعتمادها قبل ترحيل التخصيص إلى دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="129f3-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="129f3-117">في الحقل "ترحيل دفتر الأستاذ العام"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="129f3-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="129f3-118">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="129f3-118">Select **OK**.</span></span>
7. <span data-ttu-id="129f3-119">في جزء التنقل، انتقل إلى **الوحدات النمطية > دفتر الأستاذ العام > تخصيصات > دفاتر يومية التخصيص**.</span><span class="sxs-lookup"><span data-stu-id="129f3-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="129f3-120">حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="129f3-120">Select **Lines**.</span></span>
9. <span data-ttu-id="129f3-121">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="129f3-121">Select **Post**.</span></span>
10. <span data-ttu-id="129f3-122">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="129f3-122">Select **Post**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]