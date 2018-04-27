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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: cf35406b43c1ec40a7c248b970559b65fcd8a6c6
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="22608-103">إعداد عمليات سير العمل للمصروفات</span><span class="sxs-lookup"><span data-stu-id="22608-103">Set up workflows for expense</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="22608-104"> يمكنك إعداد عملية سير عمل يتم استخدامها لمراجعة مستندات السفر والمصروفات والموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="22608-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="22608-105">تتضمن المستندات التي يمكن تحديد عمليات سير عمل لها تقارير المصروفات وطلبات السفر وطلبات السلف النقدية.</span><span class="sxs-lookup"><span data-stu-id="22608-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="22608-106">يعد سير العمل بمثابة عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="22608-106">A workflow represents a business process.</span></span> <span data-ttu-id="22608-107">فهو يحدد كيفية تدفق المستند عبر النظام ويشير إلى الفرد المنوط بإكمال المهمة أو الموافقة على المستند.</span><span class="sxs-lookup"><span data-stu-id="22608-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="22608-108">ويترتب على استخدام نظام سير العمل في المؤسسة العديد من الفوائد:</span><span class="sxs-lookup"><span data-stu-id="22608-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="22608-109">**عمليات متسقة** — يمكنك تحديد عملية الموافقة على مستندات بعينها، مثل طلبات الشراء وتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="22608-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="22608-110">ويساعدك استخدام نظام سير العمل على ضمان معالجة المستندات والموافقة عليها بأسلوب متسق وفعال.</span><span class="sxs-lookup"><span data-stu-id="22608-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="22608-111">وضوح العمليات - يمكنك تتبع حالة مثيل سير عمل معين وتاريخه ومعايير الأداء الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="22608-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="22608-112">ويساعدك هذا الأمر على تحديد ما إذا كانت هناك ضرورة لإجراء تغييرات على سير العمل لتحسين كفاءته أم لا.</span><span class="sxs-lookup"><span data-stu-id="22608-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="22608-113">قائمة العمل المركزية — يمكن للمستخدمين عرض قائمة عمل مركزية لعرض مهام سير العمل والموافقات المعينة لها.</span><span class="sxs-lookup"><span data-stu-id="22608-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="22608-114">**أنواع سير العمل التي تستطيع إنشائها**</span><span class="sxs-lookup"><span data-stu-id="22608-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="22608-115">يسرد الجدول التالي أنواع عمليات سير العمل التي تستطيع إنشاءها في **المصروفات**.</span><span class="sxs-lookup"><span data-stu-id="22608-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="22608-116"><strong>النوع</strong></span><span class="sxs-lookup"><span data-stu-id="22608-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="22608-117"><strong>استخدم هذا النوع لـ</strong></span><span class="sxs-lookup"><span data-stu-id="22608-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="22608-118"><strong>تقرير المصروفات</strong></span><span class="sxs-lookup"><span data-stu-id="22608-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="22608-119">إنشاء عمليات سير عمل الموافقة لتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="22608-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="22608-120"><strong>ترحيل تلقائي لتقرير المصروفات</strong></span><span class="sxs-lookup"><span data-stu-id="22608-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="22608-121">إنشاء عمليات سير عمل ترحيل تلقائي لتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="22608-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="22608-122"><strong>عنصر بند المصروفات</strong></span><span class="sxs-lookup"><span data-stu-id="22608-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="22608-123">إنشاء عمليات سير عمل الموافقة لبنود تقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="22608-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="22608-124"><strong>ترحيل تلقائي لعنصر بند المصروفات</strong></span><span class="sxs-lookup"><span data-stu-id="22608-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="22608-125">إنشاء عمليات سير عمل ترحيل تلقائي لبنود تقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="22608-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="22608-126"><strong>طلب السفر</strong></span><span class="sxs-lookup"><span data-stu-id="22608-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="22608-127">إنشاء عمليات سير عمل الموافقة لطلبات الشراء.</span><span class="sxs-lookup"><span data-stu-id="22608-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="22608-128"><strong>طلب سلفة نقدية</strong></span><span class="sxs-lookup"><span data-stu-id="22608-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="22608-129">إنشاء عمليات سير عمل الموافقة لطلبات السلفة النقدية.</span><span class="sxs-lookup"><span data-stu-id="22608-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="22608-130"><strong>استرداد ضريبة القيمة المضافة</strong></span><span class="sxs-lookup"><span data-stu-id="22608-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="22608-131">إنشاء عمليات سير عمل الموافقة لاسترداد ضريبة القيمة المضافة (VAT).</span><span class="sxs-lookup"><span data-stu-id="22608-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |


