---
title: عرض محفوظات سير العمل
description: يصف هذا الموضوع الخطوات لعرض حالة مستند تم إرساله إلى نظام سير العمل من أجل المعالجة والموافقة.
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a7c6edd53ebafb0bab894fec9c50d834d24b990
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567994"
---
# <a name="view-workflow-history"></a><span data-ttu-id="ff490-103">عرض محفوظات سير العمل</span><span class="sxs-lookup"><span data-stu-id="ff490-103">View workflow history</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff490-104">يصف هذا الموضوع الخطوات لعرض حالة مستند تم إرساله إلى نظام سير العمل من أجل المعالجة والموافقة.</span><span class="sxs-lookup"><span data-stu-id="ff490-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="ff490-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="ff490-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="ff490-106">انتقل إلى **جزء التنقل > الوحدات النمطية > عام > استعلامات > سير العمل > محفوظات سير العمل**.</span><span class="sxs-lookup"><span data-stu-id="ff490-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="ff490-107">استخدم هذا النموذج لعرض حالة مستند تم إرساله إلى نظام سير العمل من أجل المعالجة والموافقة.</span><span class="sxs-lookup"><span data-stu-id="ff490-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="ff490-108">**معرف المثيل** هو كود التعريف الخاص بمثيل بسير العمل الذي يقوم بمعالجة المستند أو الذي قام بمعالجته بالفعل.</span><span class="sxs-lookup"><span data-stu-id="ff490-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="ff490-109">**الحالة** هي حالة سير العمل الخاصة بالمستند.</span><span class="sxs-lookup"><span data-stu-id="ff490-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="ff490-110">**معرف سير العمل** هو كود التعريف الخاص بسير العمل الذي يقوم بمعالجة المستند أو الذي قام بمعالجته بالفعل.</span><span class="sxs-lookup"><span data-stu-id="ff490-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="ff490-111">**المستند** هو كود التعريف للمستند.</span><span class="sxs-lookup"><span data-stu-id="ff490-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="ff490-112">**نوع المستند** هو نوع المستند الذي تم إرساله للمعالجة.</span><span class="sxs-lookup"><span data-stu-id="ff490-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="ff490-113">**سير العمل** هو اسم سير العمل الذي يقوم بمعالجة المستند أو الذي قام بمعالجته بالفعل.</span><span class="sxs-lookup"><span data-stu-id="ff490-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="ff490-114">**الإصدار** هو رقم إصدار سير العمل الذي يقوم بمعالجة المستند أو الذي قام بمعالجته بالفعل.</span><span class="sxs-lookup"><span data-stu-id="ff490-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="ff490-115">**تاريخ ووقت الإنشاء** هو تاريخ ووقت إرسال المستند.</span><span class="sxs-lookup"><span data-stu-id="ff490-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="ff490-116">**الوقت المنقضي** هو مقدار الوقت الذي انقضى منذ إرسال المستند.</span><span class="sxs-lookup"><span data-stu-id="ff490-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="ff490-117">يسمح لك الزر **استئناف** باستئناف عملية سير العمل للمستند المحدد.</span><span class="sxs-lookup"><span data-stu-id="ff490-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="ff490-118">يسمح لك الزر **استدعاء** باستدعاء المستند المحدد بحيث لا تتم معالجته.</span><span class="sxs-lookup"><span data-stu-id="ff490-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="ff490-119">في القائمة، حدد الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ff490-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="ff490-120">تأكد من توسيع المقطع **عناصر العمل**.</span><span class="sxs-lookup"><span data-stu-id="ff490-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="ff490-121">في هذا المقطع، يمكنك عرض عناصر العمل المقترنة بالمستند المحدد.</span><span class="sxs-lookup"><span data-stu-id="ff490-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="ff490-122">على سبيل المثال، قد يلزم إكمال إحدى المهام، أو قد يلزم الموافقة على المستند.</span><span class="sxs-lookup"><span data-stu-id="ff490-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="ff490-123">سيقوم الزر **إعادة تعيين** بفتح مربع حوار يمكنك من خلاله إعادة تعيين عنصر عمل لمستخدم آخر.</span><span class="sxs-lookup"><span data-stu-id="ff490-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="ff490-124">تأكد من توسيع المقطع **تعقب التفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="ff490-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="ff490-125">في هذا المقطع، يمكنك عرض محفوظات سير العمل للمستند المحدد.</span><span class="sxs-lookup"><span data-stu-id="ff490-125">In this section you can view the workflow history of the selected document.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]