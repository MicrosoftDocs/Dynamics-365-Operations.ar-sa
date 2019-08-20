---
title: عرض محفوظات سير العمل
description: يصف هذا الموضوع الخطوات لعرض حالة مستند تم إرساله إلى نظام سير العمل من أجل المعالجة والموافقة.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16c6594161f1fecd36183a6b8f2c798f52d70a9c
ms.sourcegitcommit: 81e6eaa2178fda7f7d086ad978f4c891bc4ec10a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/10/2019
ms.locfileid: "1738778"
---
# <a name="view-workflow-history"></a><span data-ttu-id="9d32c-103">عرض محفوظات سير العمل</span><span class="sxs-lookup"><span data-stu-id="9d32c-103">View workflow history</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9d32c-104">يصف هذا الموضوع الخطوات لعرض حالة مستند تم إرساله إلى نظام سير العمل من أجل المعالجة والموافقة.</span><span class="sxs-lookup"><span data-stu-id="9d32c-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="9d32c-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="9d32c-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="9d32c-106">انتقل إلى **جزء التنقل > الوحدات النمطية > عام > استعلامات > سير العمل > محفوظات سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="9d32c-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="9d32c-107">استخدم هذا النموذج لعرض حالة مستند تم إرساله إلى نظام سير العمل من أجل المعالجة والموافقة.</span><span class="sxs-lookup"><span data-stu-id="9d32c-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="9d32c-108">**معرف المثيل** هو كود التعريف الخاص بمثيل بسير العمل الذي يقوم بمعالجة المستند أو الذي قام بمعالجته بالفعل.</span><span class="sxs-lookup"><span data-stu-id="9d32c-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="9d32c-109">**الحالة** هي حالة سير العمل الخاصة بالمستند.</span><span class="sxs-lookup"><span data-stu-id="9d32c-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="9d32c-110">**معرف سير العمل** هو كود التعريف الخاص بسير العمل الذي يقوم بمعالجة المستند أو الذي قام بمعالجته بالفعل.</span><span class="sxs-lookup"><span data-stu-id="9d32c-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="9d32c-111">**المستند** هو كود التعريف للمستند.</span><span class="sxs-lookup"><span data-stu-id="9d32c-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="9d32c-112">**نوع المستند** هو نوع المستند الذي تم إرساله للمعالجة.</span><span class="sxs-lookup"><span data-stu-id="9d32c-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="9d32c-113">**سير العمل** هو اسم سير العمل الذي يقوم بمعالجة المستند أو الذي قام بمعالجته بالفعل.</span><span class="sxs-lookup"><span data-stu-id="9d32c-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="9d32c-114">**الإصدار** هو رقم إصدار سير العمل الذي يقوم بمعالجة المستند أو الذي قام بمعالجته بالفعل.</span><span class="sxs-lookup"><span data-stu-id="9d32c-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="9d32c-115">**تاريخ ووقت الإنشاء** هو تاريخ ووقت إرسال المستند.</span><span class="sxs-lookup"><span data-stu-id="9d32c-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="9d32c-116">**الوقت المنقضي** هو مقدار الوقت الذي انقضى منذ إرسال المستند.</span><span class="sxs-lookup"><span data-stu-id="9d32c-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="9d32c-117">يسمح لك الزر **استئناف** باستئناف عملية سير العمل للمستند المحدد.</span><span class="sxs-lookup"><span data-stu-id="9d32c-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="9d32c-118">يسمح لك الزر **استدعاء** باستدعاء المستند المحدد بحيث لا تتم معالجته.</span><span class="sxs-lookup"><span data-stu-id="9d32c-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="9d32c-119">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="9d32c-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="9d32c-120">تأكد من توسيع المقطع **عناصر العمل**.</span><span class="sxs-lookup"><span data-stu-id="9d32c-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="9d32c-121">في هذا المقطع، يمكنك عرض عناصر العمل المقترنة بالمستند المحدد.</span><span class="sxs-lookup"><span data-stu-id="9d32c-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="9d32c-122">على سبيل المثال، قد يلزم إكمال إحدى المهام، أو قد يلزم الموافقة على المستند.</span><span class="sxs-lookup"><span data-stu-id="9d32c-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="9d32c-123">سيقوم الزر **إعادة تعيين** بفتح مربع حوار يمكنك من خلاله إعادة تعيين عنصر عمل لمستخدم آخر.</span><span class="sxs-lookup"><span data-stu-id="9d32c-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="9d32c-124">تأكد من توسيع المقطع **تعقب التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="9d32c-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="9d32c-125">في هذا المقطع، يمكنك عرض محفوظات سير العمل للمستند المحدد.</span><span class="sxs-lookup"><span data-stu-id="9d32c-125">In this section you can view the workflow history of the selected document.</span></span>  

