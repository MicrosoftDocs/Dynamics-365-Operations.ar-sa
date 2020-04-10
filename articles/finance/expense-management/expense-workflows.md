---
title: إعداد مهام سير العمل لإدارة المصروفات
description: يمكنك إعداد عملية سير عمل يتم استخدامها لمراجعة مستندات السفر والمصروفات والموافقة عليها.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdd4d69cb86da12e4a265f89c021c238d00cad08
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/21/2020
ms.locfileid: "3153973"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="dc489-103">إعداد مهام سير العمل لإدارة المصروفات</span><span class="sxs-lookup"><span data-stu-id="dc489-103">Set up workflows for Expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc489-104">يمكنك إعداد عملية سير عمل يتم استخدامها لمراجعة مستندات السفر والمصروفات والموافقة عليها.</span><span class="sxs-lookup"><span data-stu-id="dc489-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="dc489-105">تتضمن المستندات التي يمكن تحديد عمليات سير عمل لها تقارير المصروفات وطلبات السفر وطلبات السلف النقدية.</span><span class="sxs-lookup"><span data-stu-id="dc489-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="dc489-106">يعد سير العمل بمثابة عملية تجارية.</span><span class="sxs-lookup"><span data-stu-id="dc489-106">A workflow represents a business process.</span></span> <span data-ttu-id="dc489-107">فهو يحدد كيفية تدفق المستند عبر النظام ويشير إلى الفرد المنوط بإكمال المهمة أو الموافقة على المستند.</span><span class="sxs-lookup"><span data-stu-id="dc489-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="dc489-108">ويترتب على استخدام نظام سير العمل في المؤسسة العديد من الفوائد:</span><span class="sxs-lookup"><span data-stu-id="dc489-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="dc489-109">**عمليات متسقة** — يمكنك تحديد عملية الموافقة على مستندات بعينها، مثل طلبات الشراء وتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="dc489-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="dc489-110">ويساعدك استخدام نظام سير العمل على ضمان معالجة المستندات والموافقة عليها بأسلوب متسق وفعال.</span><span class="sxs-lookup"><span data-stu-id="dc489-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="dc489-111">وضوح العمليات - يمكنك تتبع حالة مثيل سير عمل معين وتاريخه ومعايير الأداء الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="dc489-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="dc489-112">ويساعدك هذا الأمر على تحديد ما إذا كانت هناك ضرورة لإجراء تغييرات على سير العمل لتحسين كفاءته أم لا.</span><span class="sxs-lookup"><span data-stu-id="dc489-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="dc489-113">قائمة العمل المركزية — يمكن للمستخدمين عرض قائمة عمل مركزية لعرض مهام سير العمل والموافقات المعينة لها.</span><span class="sxs-lookup"><span data-stu-id="dc489-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="dc489-114">**أنواع سير العمل التي تستطيع إنشائها**</span><span class="sxs-lookup"><span data-stu-id="dc489-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="dc489-115">يسرد الجدول التالي أنواع عمليات سير العمل التي تستطيع إنشاءها في **المصروفات**.</span><span class="sxs-lookup"><span data-stu-id="dc489-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="dc489-116"><strong>النوع</strong></span><span class="sxs-lookup"><span data-stu-id="dc489-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="dc489-117"><strong>استخدم هذا النوع لـ</strong></span><span class="sxs-lookup"><span data-stu-id="dc489-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="dc489-118"><strong>تقرير المصروفات</strong></span><span class="sxs-lookup"><span data-stu-id="dc489-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="dc489-119">إنشاء عمليات سير عمل الموافقة لتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="dc489-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="dc489-120"><strong>ترحيل تلقائي لتقرير المصروفات</strong></span><span class="sxs-lookup"><span data-stu-id="dc489-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="dc489-121">إنشاء عمليات سير عمل ترحيل تلقائي لتقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="dc489-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="dc489-122"><strong>عنصر بند المصروفات</strong></span><span class="sxs-lookup"><span data-stu-id="dc489-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="dc489-123">إنشاء عمليات سير عمل الموافقة لبنود تقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="dc489-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="dc489-124"><strong>ترحيل تلقائي لعنصر بند المصروفات</strong></span><span class="sxs-lookup"><span data-stu-id="dc489-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="dc489-125">إنشاء عمليات سير عمل ترحيل تلقائي لبنود تقارير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="dc489-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="dc489-126"><strong>طلب السفر</strong></span><span class="sxs-lookup"><span data-stu-id="dc489-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="dc489-127">إنشاء عمليات سير عمل الموافقة لطلبات الشراء.</span><span class="sxs-lookup"><span data-stu-id="dc489-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="dc489-128"><strong>طلب سلفة نقدية</strong></span><span class="sxs-lookup"><span data-stu-id="dc489-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="dc489-129">إنشاء عمليات سير عمل الموافقة لطلبات السلفة النقدية.</span><span class="sxs-lookup"><span data-stu-id="dc489-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="dc489-130"><strong>استرداد ضريبة القيمة المضافة</strong></span><span class="sxs-lookup"><span data-stu-id="dc489-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="dc489-131">إنشاء عمليات سير عمل الموافقة لاسترداد ضريبة القيمة المضافة (VAT).</span><span class="sxs-lookup"><span data-stu-id="dc489-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

