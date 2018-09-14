--- 
title: "تثبيت السعر محدود الفاقد من أوامر المبيعات"
description: "يركز هذا الإجراء على التحقق من صحة شجرة تثبيت السعر من سطر المبيعات حيثما يتم إنتاج الصنف بحلول كانبان."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 2e2448dfd83304d4f7e5dfc8ce0d02cdac998779
ms.contentlocale: ar-sa
ms.lasthandoff: 09/14/2018

---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="2a13d-103">تثبيت السعر محدود الفاقد من أوامر المبيعات</span><span class="sxs-lookup"><span data-stu-id="2a13d-103">Lean pegging from sales orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2a13d-104">يركز هذا الإجراء على التحقق من صحة شجرة تثبيت السعر من سطر المبيعات حيثما يتم إنتاج الصنف بحلول كانبان.</span><span class="sxs-lookup"><span data-stu-id="2a13d-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="2a13d-105">بعد التحقق من صحة شجرة تثبيت السعر، يتم تخطيط كافة وظائف كانبان.</span><span class="sxs-lookup"><span data-stu-id="2a13d-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="2a13d-106">وهذا مفيد لسيناريوهات الطلبات حيث يحتاج متلقي الطلب إلى التأكد من أنه يمكن بدء الإنتاج على الفور.</span><span class="sxs-lookup"><span data-stu-id="2a13d-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="2a13d-107">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="2a13d-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2a13d-108">ويُعد هذا الإجراء مخصصًا لمتلقي الطلب المتقدم في شركة lean.</span><span class="sxs-lookup"><span data-stu-id="2a13d-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="2a13d-109">إنشاء أمر مبيعات لعنصر التحكم في كانبان</span><span class="sxs-lookup"><span data-stu-id="2a13d-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="2a13d-110">انتقل إلى "كافة أوامر المبيعات‬".</span><span class="sxs-lookup"><span data-stu-id="2a13d-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="2a13d-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2a13d-111">Click New.</span></span>
3. <span data-ttu-id="2a13d-112">في الحقل "حساب العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2a13d-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="2a13d-113">استخدم US-001.</span><span class="sxs-lookup"><span data-stu-id="2a13d-113">Use US-001.</span></span>  
4. <span data-ttu-id="2a13d-114">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2a13d-114">Click OK.</span></span>
5. <span data-ttu-id="2a13d-115">في الحقل "رقم الصنف، اكتب "L0001".</span><span class="sxs-lookup"><span data-stu-id="2a13d-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="2a13d-116">تعيين الكمية إلى "30".</span><span class="sxs-lookup"><span data-stu-id="2a13d-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="2a13d-117">من المهم أن تكون الكمية أكبر من 24 من أجل تشغيل قاعدة كانبان الحدث.</span><span class="sxs-lookup"><span data-stu-id="2a13d-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="2a13d-118">فتح شجرة تثبيت السعر</span><span class="sxs-lookup"><span data-stu-id="2a13d-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="2a13d-119">انقر فوق "المنتج والتوريد".</span><span class="sxs-lookup"><span data-stu-id="2a13d-119">Click Product and supply.</span></span>
2. <span data-ttu-id="2a13d-120">انقر فوق "عرض شجرة تثبيت السعر".</span><span class="sxs-lookup"><span data-stu-id="2a13d-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="2a13d-121">لاحظ أن شجرة تثبيت السعر توضح كافة مستويات تثبيت السعر المطلوبة لسطر أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="2a13d-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="2a13d-122">في هذه الحالة، هناك مستويان من كانبان وكافة المكونات المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="2a13d-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="2a13d-123">تخطيط شجرة تثبيت السعر</span><span class="sxs-lookup"><span data-stu-id="2a13d-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="2a13d-124">في الشجرة، حدد "سطر المبيعات 000832\Kanban 000558".</span><span class="sxs-lookup"><span data-stu-id="2a13d-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="2a13d-125">قم بتوسيع قسم "وظائف كانبان".</span><span class="sxs-lookup"><span data-stu-id="2a13d-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="2a13d-126">لاحظ أنه لم يتم تخطيط حالة الوظيفة لوظيفة كانبان.</span><span class="sxs-lookup"><span data-stu-id="2a13d-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="2a13d-127">انقر فوق تخطيط شجرة تثبيت السعر بالكامل.</span><span class="sxs-lookup"><span data-stu-id="2a13d-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="2a13d-128">وهذا سيقوم بتخطيط كافة وظائف كانبان في شجرة تثبيت السعر، وتغيير حالة الوظيفة من غير مخططة إلى مخططة.</span><span class="sxs-lookup"><span data-stu-id="2a13d-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="2a13d-129">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2a13d-129">Refresh the page.</span></span>
    * <span data-ttu-id="2a13d-130">لاحظ أنه تم تغيير حالة وظيفة كانبان من غير مخططة إلى مخططة.</span><span class="sxs-lookup"><span data-stu-id="2a13d-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="2a13d-131">في الشجرة، حدد "سطر المبيعات 000832\Kanban 000558\Issue لـ L0001\Kanban 000559".</span><span class="sxs-lookup"><span data-stu-id="2a13d-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="2a13d-132">كما تم تخطيط الوظيفة لكانبان الثاني، لأنه تم تخطيط شجرة تثبيت السعر بالكامل.</span><span class="sxs-lookup"><span data-stu-id="2a13d-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="2a13d-133">لاحظ أنه تم تغيير حالة وظيفة كانبان من غير مخططة إلى مخططة.</span><span class="sxs-lookup"><span data-stu-id="2a13d-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  


