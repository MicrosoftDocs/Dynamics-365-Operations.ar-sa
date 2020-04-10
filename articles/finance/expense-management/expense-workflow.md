---
title: سير عمل إدارة المصروفات
description: يشرح هذا الموضوع كيفية استخدام نظام سير العمل في Microsoft Dynamics 365 Finance، لإعداد عملية مراجعة لتقارير المصروفات في إدارة المصروفات.
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
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/21/2020
ms.locfileid: "3153961"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="4afd5-103">سير عمل إدارة المصروفات</span><span class="sxs-lookup"><span data-stu-id="4afd5-103">Expense management workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4afd5-104">يمكنك استخدام نظام سير العمل لإعداد عملية مراجعة لتقارير المصروفات في إدارة المصروفات.</span><span class="sxs-lookup"><span data-stu-id="4afd5-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="4afd5-105">يمكنك إعداد سير عمل يستخدم المعايير التالية لتحديد الجهة التي توافق على تقارير المصروفات:</span><span class="sxs-lookup"><span data-stu-id="4afd5-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="4afd5-106">التدرج الهرمي لتقارير الموظفين وحدود الموافقة المعرفة مسبقًا</span><span class="sxs-lookup"><span data-stu-id="4afd5-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="4afd5-107">موافقة متعددة المستويات تدعم معتمدين مؤقتًا ومعتمدًا نهائيًا</span><span class="sxs-lookup"><span data-stu-id="4afd5-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="4afd5-108">الأبعاد المالية ومسؤولية المشروع</span><span class="sxs-lookup"><span data-stu-id="4afd5-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="4afd5-109">تعيين إلى مستخدمين معينين أو مجموعات معينة من المستخدمين</span><span class="sxs-lookup"><span data-stu-id="4afd5-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="4afd5-110">يمكن إنشاء الموافقة على عمليات سير العمل لتقارير المصروفات ومتطلبات السفر والسُلف النقدية‬ واسترداد ضريبة القيمة المضافة (VAT).</span><span class="sxs-lookup"><span data-stu-id="4afd5-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="4afd5-111">**مثال**</span><span class="sxs-lookup"><span data-stu-id="4afd5-111">**Example**</span></span>

<span data-ttu-id="4afd5-112">العملية التالية هي مثال لسير عمل إدارة المصروفات لتقرير مصروفات.</span><span class="sxs-lookup"><span data-stu-id="4afd5-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="4afd5-113">يقوم موظف بإنشاء وحفظ تقرير مصروفات.</span><span class="sxs-lookup"><span data-stu-id="4afd5-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="4afd5-114">يرسل الموظف تقرير المصروفات للموافقة عليه.</span><span class="sxs-lookup"><span data-stu-id="4afd5-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="4afd5-115">يتم تعريف المعتمد استنادًا إلى القواعد التي تم تحديدها عند إعداد سير العمل.</span><span class="sxs-lookup"><span data-stu-id="4afd5-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="4afd5-116">يتلقى المعتمد إشعارًا يفيد بأن تقرير المصروفات جاهز للاعتماد.</span><span class="sxs-lookup"><span data-stu-id="4afd5-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="4afd5-117">يراجع المعتمد تقرير المصروفات ويتحقق من استيفاء الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="4afd5-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="4afd5-118">المصروفات لا تنتهك أي سياسة من سياسات المصروفات.</span><span class="sxs-lookup"><span data-stu-id="4afd5-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="4afd5-119">إذا انتهك أي بند مصروفات سياسة مصروفات، يتحقق المعتمد من أن تقرير المصروفات يتضمن تبريرًا مهنيًا صالحًا.</span><span class="sxs-lookup"><span data-stu-id="4afd5-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="4afd5-120">ترفق الإيصالات الإلكترونية بتقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="4afd5-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="4afd5-121">يوافق المعتمد على تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="4afd5-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="4afd5-122">يتم تعيين تقرير المصروفات إلى منسق الحسابات الدائنة لترحيله.</span><span class="sxs-lookup"><span data-stu-id="4afd5-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="4afd5-123">تحدث أي خطوة من الخطوات التالية، استنادًا إلى ما إذا تم تكوين الترحيل التلقائي أم لا:</span><span class="sxs-lookup"><span data-stu-id="4afd5-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="4afd5-124">إذا تم تكوين الترحيل التلقائي، فستتم معالجة تقرير المصروفات للدفع، ويتم تحديث حالة تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="4afd5-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="4afd5-125">إذا لم يتم تكوين الترحيل التلقائي، فإن منسحق الحسابات الدائنة يتحقق من إرسال كافة الإيصالات الأصلية، ومن أن الإيصالات تتوافق مع المصروفات في تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="4afd5-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="4afd5-126">يجب أيضًا التحقق من صحة كل أكواد الضريبة التي تم إدخالها في تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="4afd5-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="4afd5-127">بعد أن يتم التحقق من صحة هذه المتطلبات، يتم ترحيل تقرير المصروفات.</span><span class="sxs-lookup"><span data-stu-id="4afd5-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="4afd5-128">بعد ترحيل تقرير المصروفات، يتم تخويل الدفع لتقرير المصروفات، ويتم تعويض الموظف.</span><span class="sxs-lookup"><span data-stu-id="4afd5-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
