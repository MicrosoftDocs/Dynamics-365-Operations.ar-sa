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
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 19d725f15f00afce1a2ae4b336226f1dafa94b41
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="74d4d-103">إعداد عمليات سير العمل للمصروفات</span><span class="sxs-lookup"><span data-stu-id="74d4d-103">Set up workflows for expense</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="74d4d-104"> يمكنك إعداد عملية سير عمل يتم استخدامها لمراجعة مستندات السفر والمصروفات والموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="74d4d-104"> You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="74d4d-105">تتضمن المستندات التي يمكن تحديد عمليات سير عمل لها تقارير المصروفات وطلبات السفر وطلبات السلف النقدية.</span><span class="sxs-lookup"><span data-stu-id="74d4d-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="74d4d-106">يعد سير العمل بمثابة عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="74d4d-106">A workflow represents a business process.</span></span> <span data-ttu-id="74d4d-107">فهو يحدد كيفية تدفق المستند عبر النظام ويشير إلى الفرد المنوط بإكمال المهمة أو الموافقة على المستند.</span><span class="sxs-lookup"><span data-stu-id="74d4d-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="74d4d-108">ويترتب على استخدام نظام سير العمل في المؤسسة العديد من الفوائد:</span><span class="sxs-lookup"><span data-stu-id="74d4d-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="74d4d-109">**عمليات متسقة** — يمكنك تحديد عملية الموافقة على مستندات بعينها، مثل طلبات الشراء وتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="74d4d-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="74d4d-110">ويساعدك استخدام نظام سير العمل على ضمان معالجة المستندات والموافقة عليها بأسلوب متسق وفعال.</span><span class="sxs-lookup"><span data-stu-id="74d4d-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="74d4d-111">وضوح العمليات - يمكنك تتبع حالة مثيل سير عمل معين وتاريخه ومعايير الأداء الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="74d4d-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="74d4d-112">ويساعدك هذا الأمر على تحديد ما إذا كانت هناك ضرورة لإجراء تغييرات على سير العمل لتحسين كفاءته أم لا.</span><span class="sxs-lookup"><span data-stu-id="74d4d-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="74d4d-113">قائمة العمل المركزية — يمكن للمستخدمين عرض قائمة عمل مركزية لعرض مهام سير العمل والموافقات المعينة لها.</span><span class="sxs-lookup"><span data-stu-id="74d4d-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="74d4d-114">**أنواع سير العمل التي تستطيع إنشائها**</span><span class="sxs-lookup"><span data-stu-id="74d4d-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="74d4d-115">يسرد الجدول التالي أنواع عمليات سير العمل التي تستطيع إنشاءها في **المصروفات**.</span><span class="sxs-lookup"><span data-stu-id="74d4d-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>

| <span data-ttu-id="74d4d-116">**النوع**</span><span class="sxs-lookup"><span data-stu-id="74d4d-116">**Type**</span></span>                           | <span data-ttu-id="74d4d-117">**استخدم هذا النوع لـ**</span><span class="sxs-lookup"><span data-stu-id="74d4d-117">**Use this type to**</span></span>                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="74d4d-118">**تقرير المصروفات**</span><span class="sxs-lookup"><span data-stu-id="74d4d-118">**Expense report**</span></span>                 | <span data-ttu-id="74d4d-119">إنشاء عمليات سير عمل الموافقة لتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="74d4d-119">Create approval workflows for expense reports.</span></span>                       |      
| <span data-ttu-id="74d4d-120">**ترحيل تلقائي لتقرير المصروفات**</span><span class="sxs-lookup"><span data-stu-id="74d4d-120">**Expense report auto posting**</span></span>    | <span data-ttu-id="74d4d-121">إنشاء عمليات سير عمل ترحيل تلقائي لتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="74d4d-121">Create automatic posting workflows for expense reports.</span></span>              |     
| <span data-ttu-id="74d4d-122">**عنصر بند المصروفات**</span><span class="sxs-lookup"><span data-stu-id="74d4d-122">**Expense line item**</span></span>              | <span data-ttu-id="74d4d-123">إنشاء عمليات سير عمل الموافقة لبنود تقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="74d4d-123">Create approval workflows for line items on expense reports.</span></span>         |     
| <span data-ttu-id="74d4d-124">**ترحيل تلقائي لعنصر بند المصروفات**</span><span class="sxs-lookup"><span data-stu-id="74d4d-124">**Expense line item auto posting**</span></span> | <span data-ttu-id="74d4d-125">إنشاء عمليات سير عمل ترحيل تلقائي لبنود تقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="74d4d-125">Create automatic posting workflows for line items on expense reports.</span></span>|
| <span data-ttu-id="74d4d-126">**طلب السفر**</span><span class="sxs-lookup"><span data-stu-id="74d4d-126">**Travel requisition**</span></span>             | <span data-ttu-id="74d4d-127">إنشاء عمليات سير عمل الموافقة لطلبات الشراء.</span><span class="sxs-lookup"><span data-stu-id="74d4d-127">Create approval workflows for travel requisitions.</span></span>                   |    
| <span data-ttu-id="74d4d-128">**طلب سلفة نقدية**</span><span class="sxs-lookup"><span data-stu-id="74d4d-128">**Cash advance request**</span></span>           | <span data-ttu-id="74d4d-129">إنشاء عمليات سير عمل الموافقة لطلبات السلفة النقدية.</span><span class="sxs-lookup"><span data-stu-id="74d4d-129">Create approval workflows for cash advance requests.</span></span>                 |     
| <span data-ttu-id="74d4d-130">**استرداد ضريبة القيمة المضافة**</span><span class="sxs-lookup"><span data-stu-id="74d4d-130">**VAT tax recovery**</span></span>               | <span data-ttu-id="74d4d-131">إنشاء عمليات سير عمل الموافقة لاسترداد ضريبة القيمة المضافة (VAT).</span><span class="sxs-lookup"><span data-stu-id="74d4d-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span> |       

