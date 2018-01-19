---
title: "إعداد عمليات سير العمل للمصروفات"
description: "يمكنك إعداد عملية سير عمل يتم استخدامها لمراجعة مستندات السفر والمصروفات والموافقة عليها."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: fb729a56919eb50cdff8318138986152bb65a083
ms.contentlocale: ar-sa
ms.lasthandoff: 01/19/2018

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="09299-103">إعداد عمليات سير العمل للمصروفات</span><span class="sxs-lookup"><span data-stu-id="09299-103">Set up workflows for expense</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="09299-104"> يمكنك إعداد عملية سير عمل يتم استخدامها لمراجعة مستندات السفر والمصروفات والموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="09299-104"> You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="09299-105">تتضمن المستندات التي يمكن تحديد عمليات سير عمل لها تقارير المصروفات وطلبات السفر وطلبات السلف النقدية.</span><span class="sxs-lookup"><span data-stu-id="09299-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="09299-106">يعد سير العمل بمثابة عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="09299-106">A workflow represents a business process.</span></span> <span data-ttu-id="09299-107">فهو يحدد كيفية تدفق المستند عبر النظام ويشير إلى الفرد المنوط بإكمال المهمة أو الموافقة على المستند.</span><span class="sxs-lookup"><span data-stu-id="09299-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="09299-108">ويترتب على استخدام نظام سير العمل في المؤسسة العديد من الفوائد:</span><span class="sxs-lookup"><span data-stu-id="09299-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="09299-109">**عمليات متسقة** — يمكنك تحديد عملية الموافقة على مستندات بعينها، مثل طلبات الشراء وتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="09299-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="09299-110">ويساعدك استخدام نظام سير العمل على ضمان معالجة المستندات والموافقة عليها بأسلوب متسق وفعال.</span><span class="sxs-lookup"><span data-stu-id="09299-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="09299-111">وضوح العمليات - يمكنك تتبع حالة مثيل سير عمل معين وتاريخه ومعايير الأداء الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="09299-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="09299-112">ويساعدك هذا الأمر على تحديد ما إذا كانت هناك ضرورة لإجراء تغييرات على سير العمل لتحسين كفاءته أم لا.</span><span class="sxs-lookup"><span data-stu-id="09299-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="09299-113">قائمة العمل المركزية — يمكن للمستخدمين عرض قائمة عمل مركزية لعرض مهام سير العمل والموافقات المعينة لها.</span><span class="sxs-lookup"><span data-stu-id="09299-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="09299-114">**أنواع سير العمل التي تستطيع إنشائها**</span><span class="sxs-lookup"><span data-stu-id="09299-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="09299-115">يسرد الجدول التالي أنواع عمليات سير العمل التي تستطيع إنشاءها في **المصروفات**.</span><span class="sxs-lookup"><span data-stu-id="09299-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>

| <span data-ttu-id="09299-116">**النوع**</span><span class="sxs-lookup"><span data-stu-id="09299-116">**Type**</span></span>                           | <span data-ttu-id="09299-117">**استخدم هذا النوع لـ**</span><span class="sxs-lookup"><span data-stu-id="09299-117">**Use this type to**</span></span>                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="09299-118">**تقرير المصروفات**</span><span class="sxs-lookup"><span data-stu-id="09299-118">**Expense report**</span></span>                 | <span data-ttu-id="09299-119">إنشاء عمليات سير عمل الموافقة لتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="09299-119">Create approval workflows for expense reports.</span></span>                       |      
| <span data-ttu-id="09299-120">**ترحيل تلقائي لتقرير المصروفات**</span><span class="sxs-lookup"><span data-stu-id="09299-120">**Expense report auto posting**</span></span>    | <span data-ttu-id="09299-121">إنشاء عمليات سير عمل ترحيل تلقائي لتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="09299-121">Create automatic posting workflows for expense reports.</span></span>              |     
| <span data-ttu-id="09299-122">**عنصر بند المصروفات**</span><span class="sxs-lookup"><span data-stu-id="09299-122">**Expense line item**</span></span>              | <span data-ttu-id="09299-123">إنشاء عمليات سير عمل الموافقة لبنود تقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="09299-123">Create approval workflows for line items on expense reports.</span></span>         |     
| <span data-ttu-id="09299-124">**ترحيل تلقائي لعنصر بند المصروفات**</span><span class="sxs-lookup"><span data-stu-id="09299-124">**Expense line item auto posting**</span></span> | <span data-ttu-id="09299-125">إنشاء عمليات سير عمل ترحيل تلقائي لبنود تقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="09299-125">Create automatic posting workflows for line items on expense reports.</span></span>|
| <span data-ttu-id="09299-126">**طلب السفر**</span><span class="sxs-lookup"><span data-stu-id="09299-126">**Travel requisition**</span></span>             | <span data-ttu-id="09299-127">إنشاء عمليات سير عمل الموافقة لطلبات الشراء.</span><span class="sxs-lookup"><span data-stu-id="09299-127">Create approval workflows for travel requisitions.</span></span>                   |    
| <span data-ttu-id="09299-128">**طلب سلفة نقدية**</span><span class="sxs-lookup"><span data-stu-id="09299-128">**Cash advance request**</span></span>           | <span data-ttu-id="09299-129">إنشاء عمليات سير عمل الموافقة لطلبات السلفة النقدية.</span><span class="sxs-lookup"><span data-stu-id="09299-129">Create approval workflows for cash advance requests.</span></span>                 |     
| <span data-ttu-id="09299-130">**استرداد ضريبة القيمة المضافة**</span><span class="sxs-lookup"><span data-stu-id="09299-130">**VAT tax recovery**</span></span>               | <span data-ttu-id="09299-131">إنشاء عمليات سير عمل الموافقة لاسترداد ضريبة القيمة المضافة (VAT).</span><span class="sxs-lookup"><span data-stu-id="09299-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span> |       

