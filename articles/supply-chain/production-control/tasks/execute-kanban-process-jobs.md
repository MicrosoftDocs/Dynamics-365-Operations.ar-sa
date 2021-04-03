---
title: تنفيذ وظائف عملية كانبان
description: يركز هذا الإجراء على تنفيذ وظائف عملية كانبان.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10f8a464207fc3b1c34638a9f55df7b53a69b357
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259784"
---
# <a name="execute-kanban-process-jobs"></a><span data-ttu-id="18f4a-103">تنفيذ وظائف عملية كانبان</span><span class="sxs-lookup"><span data-stu-id="18f4a-103">Execute kanban process jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="18f4a-104">يركز هذا الإجراء على تنفيذ وظائف عملية كانبان.</span><span class="sxs-lookup"><span data-stu-id="18f4a-104">This procedure focuses on executing kanban process jobs.</span></span> <span data-ttu-id="18f4a-105">الوظيفة الأولى مكتملة بالكمية المتوقعة ولا تحتوي على أخطاء.</span><span class="sxs-lookup"><span data-stu-id="18f4a-105">The first job is completed with the expected quantity and has no errors.</span></span> <span data-ttu-id="18f4a-106">الوظيفة الثانية مكتملة مع وجود أخطاء.</span><span class="sxs-lookup"><span data-stu-id="18f4a-106">The second job is completed with errors.</span></span> <span data-ttu-id="18f4a-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="18f4a-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="18f4a-108">هذا الإجراء مخصص لعامل تشغيل الجهاز.</span><span class="sxs-lookup"><span data-stu-id="18f4a-108">This procedure is intended for the machine operator.</span></span>


## <a name="select-a-kanban-job"></a><span data-ttu-id="18f4a-109">تحديد وظيفة كانبان</span><span class="sxs-lookup"><span data-stu-id="18f4a-109">Select a kanban job</span></span>
1. <span data-ttu-id="18f4a-110">انتقل إلى التحكم بالإنتاج‬ > كانبان > لوحة كانبان لوظائف المعالجة‬.</span><span class="sxs-lookup"><span data-stu-id="18f4a-110">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="18f4a-111">في الحقل "خلية العمل"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="18f4a-111">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="18f4a-112">انقر فوق الصف الذي يحتوي على مجموعة الموارد 1250.</span><span class="sxs-lookup"><span data-stu-id="18f4a-112">Click the row with resource group 1250.</span></span> <span data-ttu-id="18f4a-113">وهذا يعمل على تصفية قائمة الوظائف لعرض الوظائف الموجودة في خلية العمل 1250 فقط.</span><span class="sxs-lookup"><span data-stu-id="18f4a-113">This filters the Jobs list to display only the jobs for work cell 1250.</span></span>
    * <span data-ttu-id="18f4a-114">ضع علامة على الصف الذي يحتوي على حالة المهمة المخططة.</span><span class="sxs-lookup"><span data-stu-id="18f4a-114">Mark the row that has the Planned job status.</span></span>  

## <a name="complete-a-job-with-expected-quantity"></a><span data-ttu-id="18f4a-115">إكمال مهمة بالكمية المتوقعة</span><span class="sxs-lookup"><span data-stu-id="18f4a-115">Complete a job with expected quantity</span></span>
1. <span data-ttu-id="18f4a-116">قم بتوسيع أو طي قسم التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="18f4a-116">Expand or collapse the Details section.</span></span>
    * <span data-ttu-id="18f4a-117">يعرض هذا المقطع معلومات هامة حول رقم البطاقة ورقم الصنف والكمية المطلوبة واسم النشاط.</span><span class="sxs-lookup"><span data-stu-id="18f4a-117">This section displays important information about card number, item number, quantity ordered, and activity name.</span></span>  
2. <span data-ttu-id="18f4a-118">قم بتوسيع قسم تعليمات الإنتاج أو طيه.</span><span class="sxs-lookup"><span data-stu-id="18f4a-118">Expand or collapse the Production instructions section.</span></span>
    * <span data-ttu-id="18f4a-119">يعرض هذا المقطع إرشادات الإنتاج للنشاط.</span><span class="sxs-lookup"><span data-stu-id="18f4a-119">This section displays production instructions for the activity.</span></span> <span data-ttu-id="18f4a-120">يمكن أن تكون التعليمات عبارة عن نص وصور ورسومات ومستندات أخرى.</span><span class="sxs-lookup"><span data-stu-id="18f4a-120">The instructions can be text, pictures, drawings, and other documents.</span></span>  
3. <span data-ttu-id="18f4a-121">انقر فوق "بدء".</span><span class="sxs-lookup"><span data-stu-id="18f4a-121">Click Start.</span></span>
    * <span data-ttu-id="18f4a-122">حدد وظيفة غير مكتملة.</span><span class="sxs-lookup"><span data-stu-id="18f4a-122">Select a job that is not completed.</span></span> <span data-ttu-id="18f4a-123">استخدم أيقونات الحالة في حقل حالة الوظيفة لعرض حالة المهمة.</span><span class="sxs-lookup"><span data-stu-id="18f4a-123">Use status icons in the Job status field to view job status.</span></span>      
4. <span data-ttu-id="18f4a-124">انقر فوق "مكتمل".</span><span class="sxs-lookup"><span data-stu-id="18f4a-124">Click Complete.</span></span>
    * <span data-ttu-id="18f4a-125">يتم إكمال الوظيفة بالجودة المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="18f4a-125">The job is completed with the expected quality.</span></span>  

## <a name="complete-a-job-with-errors"></a><span data-ttu-id="18f4a-126">إكمال وظيفة تحتوي على أخطاء</span><span class="sxs-lookup"><span data-stu-id="18f4a-126">Complete a job with errors</span></span>
1. <span data-ttu-id="18f4a-127">انقر فوق "بدء".</span><span class="sxs-lookup"><span data-stu-id="18f4a-127">Click Start.</span></span>
    * <span data-ttu-id="18f4a-128">عند اكتمال وظيفة ما، فإنه يتم تحديد الوظيفة التالية في القائمة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="18f4a-128">When a job is completed, the next job on the list is selected automatically.</span></span> <span data-ttu-id="18f4a-129">هذا بسبب أنك لا تحتاج إلى تحديد وظيفة قبل النقر فوق "ابدأ".</span><span class="sxs-lookup"><span data-stu-id="18f4a-129">This is why you don't need to select a job before you click Start.</span></span>  
2. <span data-ttu-id="18f4a-130">في جزء "الإجراءات"، انقر فوق "تصنيع".</span><span class="sxs-lookup"><span data-stu-id="18f4a-130">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="18f4a-131">انقر فوق اكتمال (التفاصيل).</span><span class="sxs-lookup"><span data-stu-id="18f4a-131">Click Complete (details).</span></span>
4. <span data-ttu-id="18f4a-132">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="18f4a-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="18f4a-133">في الحقل "كمية الخطأ"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="18f4a-133">In the Error quantity field, enter a number.</span></span>
6. <span data-ttu-id="18f4a-134">في الحقل "كمية البضائع"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="18f4a-134">In the Good quantity field, enter a number.</span></span>
7. <span data-ttu-id="18f4a-135">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="18f4a-135">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]