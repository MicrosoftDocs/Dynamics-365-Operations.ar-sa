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
ms.openlocfilehash: dd5b8d9f3fd2edab50b52a8345f254ebc6b31d0a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140388"
---
# <a name="view-workflow-history"></a><span data-ttu-id="3284b-103">عرض محفوظات سير العمل</span><span class="sxs-lookup"><span data-stu-id="3284b-103">View workflow history</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3284b-104">يصف هذا الموضوع الخطوات لعرض حالة مستند تم إرساله إلى نظام سير العمل من أجل المعالجة والموافقة.</span><span class="sxs-lookup"><span data-stu-id="3284b-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="3284b-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="3284b-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="3284b-106">انتقل إلى **جزء التنقل > الوحدات النمطية > عام > استعلامات > سير العمل > محفوظات سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="3284b-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="3284b-107">استخدم هذا النموذج لعرض حالة مستند تم إرساله إلى نظام سير العمل من أجل المعالجة والموافقة.</span><span class="sxs-lookup"><span data-stu-id="3284b-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="3284b-108">**معرف المثيل** هو كود التعريف الخاص بمثيل بسير العمل الذي يقوم بمعالجة المستند أو الذي قام بمعالجته بالفعل.</span><span class="sxs-lookup"><span data-stu-id="3284b-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="3284b-109">**الحالة** هي حالة سير العمل الخاصة بالمستند.</span><span class="sxs-lookup"><span data-stu-id="3284b-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="3284b-110">**معرف سير العمل** هو كود التعريف الخاص بسير العمل الذي يقوم بمعالجة المستند أو الذي قام بمعالجته بالفعل.</span><span class="sxs-lookup"><span data-stu-id="3284b-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="3284b-111">**المستند** هو كود التعريف للمستند.</span><span class="sxs-lookup"><span data-stu-id="3284b-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="3284b-112">**نوع المستند** هو نوع المستند الذي تم إرساله للمعالجة.</span><span class="sxs-lookup"><span data-stu-id="3284b-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="3284b-113">**سير العمل** هو اسم سير العمل الذي يقوم بمعالجة المستند أو الذي قام بمعالجته بالفعل.</span><span class="sxs-lookup"><span data-stu-id="3284b-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="3284b-114">**الإصدار** هو رقم إصدار سير العمل الذي يقوم بمعالجة المستند أو الذي قام بمعالجته بالفعل.</span><span class="sxs-lookup"><span data-stu-id="3284b-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="3284b-115">**تاريخ ووقت الإنشاء** هو تاريخ ووقت إرسال المستند.</span><span class="sxs-lookup"><span data-stu-id="3284b-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="3284b-116">**الوقت المنقضي** هو مقدار الوقت الذي انقضى منذ إرسال المستند.</span><span class="sxs-lookup"><span data-stu-id="3284b-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="3284b-117">يسمح لك الزر **استئناف** باستئناف عملية سير العمل للمستند المحدد.</span><span class="sxs-lookup"><span data-stu-id="3284b-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="3284b-118">يسمح لك الزر **استدعاء** باستدعاء المستند المحدد بحيث لا تتم معالجته.</span><span class="sxs-lookup"><span data-stu-id="3284b-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="3284b-119">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="3284b-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="3284b-120">تأكد من توسيع المقطع **عناصر العمل**.</span><span class="sxs-lookup"><span data-stu-id="3284b-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="3284b-121">في هذا المقطع، يمكنك عرض عناصر العمل المقترنة بالمستند المحدد.</span><span class="sxs-lookup"><span data-stu-id="3284b-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="3284b-122">على سبيل المثال، قد يلزم إكمال إحدى المهام، أو قد يلزم الموافقة على المستند.</span><span class="sxs-lookup"><span data-stu-id="3284b-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="3284b-123">سيقوم الزر **إعادة تعيين** بفتح مربع حوار يمكنك من خلاله إعادة تعيين عنصر عمل لمستخدم آخر.</span><span class="sxs-lookup"><span data-stu-id="3284b-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="3284b-124">تأكد من توسيع المقطع **تعقب التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="3284b-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="3284b-125">في هذا المقطع، يمكنك عرض محفوظات سير العمل للمستند المحدد.</span><span class="sxs-lookup"><span data-stu-id="3284b-125">In this section you can view the workflow history of the selected document.</span></span>  

