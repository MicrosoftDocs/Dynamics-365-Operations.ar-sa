---
title: إكمال الإعداد الأساسي لأصل منتج تم إصداره
description: يوضح هذا الموضوع كيفية إكمال إعداد الحد الأدنى المطلوب قبل إمكانية استخدام أصل المنتج في إصدارات قائمة مكونات الصنف.
author: ShylaThompson
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bd7e02c9aea17fbc3312660d0e50cd8bbf39aa3d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844959"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="98683-103">إكمال الإعداد الأساسي لأصل منتج تم إصداره</span><span class="sxs-lookup"><span data-stu-id="98683-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="98683-104">يوضح هذا الموضوع كيفية إكمال إعداد الحد الأدنى المطلوب قبل إمكانية استخدام أصل المنتج في إصدارات قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="98683-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="98683-105">هذا هو الإجراء الثالث من أصل ثمانية إجراءات الذي يوضح كيفية إنشاء مجموعات للتكوين المستند إلى بُعد.</span><span class="sxs-lookup"><span data-stu-id="98683-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="98683-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="98683-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="98683-107">‏‫انتقل إلى ‬**جزء التنقل > الوحدات > إدارة معلومات المنتج > المنتجات > المنتجات الصادرة‬** .</span><span class="sxs-lookup"><span data-stu-id="98683-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="98683-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="98683-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="98683-109">حدد أصل المنتج الذي أصدرتَه في الإجراء الثاني.</span><span class="sxs-lookup"><span data-stu-id="98683-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="98683-110">يتم إنشاء أصل المنتج هذا باستخدام تقنية التكوين المستند إلى ُبعد.</span><span class="sxs-lookup"><span data-stu-id="98683-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="98683-111">في جزء الإجراءات، حدد **المنتج**.</span><span class="sxs-lookup"><span data-stu-id="98683-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="98683-112">انقر فوق **مجموعات الأبعاد** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="98683-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="98683-113">في الحقل **مجموعة أبعاد التخزين**، حدد زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="98683-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="98683-114">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="98683-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="98683-115">تحدد مجموعة بُعد التخزين أبعاد التخزين التي تُستخدم لحركة المنتج.</span><span class="sxs-lookup"><span data-stu-id="98683-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="98683-116">حدد **موقع** هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="98683-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="98683-117">في الحقل **مجموعة أبعاد التعقب**‬، حدد زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="98683-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="98683-118">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="98683-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="98683-119">تحدد مجموعة بُعد التعقب أبعاد التعقب التي تُستخدم لحركة المنتج.</span><span class="sxs-lookup"><span data-stu-id="98683-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="98683-120">حدد **بلا** لهذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="98683-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="98683-121">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="98683-121">Click **OK**.</span></span>
10. <span data-ttu-id="98683-122">انقر فوق **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="98683-122">Click **Edit**.</span></span>
11. <span data-ttu-id="98683-123">في الحقل **مجموعة نماذج الصنف**، حدد زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="98683-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="98683-124">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="98683-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="98683-125">تحتوي مجموعات نموذج الصنف على الإعدادات التي تحدد كيفية التحكم في الأصناف ومعالجتها في إيصالات الأصناف وإصداراتها.</span><span class="sxs-lookup"><span data-stu-id="98683-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="98683-126">كما تحدد أيضًا كيفية حساب استهلاك الصنف.</span><span class="sxs-lookup"><span data-stu-id="98683-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="98683-127">حدد **FIFO** لهذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="98683-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="98683-128">قم بتوسيع القسم **إدارة التكاليف**.</span><span class="sxs-lookup"><span data-stu-id="98683-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="98683-129">في الحقل **مجموعة الأصناف**، حدد زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="98683-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="98683-130">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="98683-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="98683-131">يتم استخدام مجموعات الأصناف لإدارة المخزون بتقسيم أصناف المخزون إلى مجموعات.</span><span class="sxs-lookup"><span data-stu-id="98683-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="98683-132">حدد **CarAudio** لهذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="98683-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="98683-133">في جزء الإجراءات، حدد **خطة**.</span><span class="sxs-lookup"><span data-stu-id="98683-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="98683-134">حدد **إعدادات الأوامر الافتراضية**.</span><span class="sxs-lookup"><span data-stu-id="98683-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="98683-135">في الحقل **نوع الأمر الافتراضي**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="98683-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="98683-136">حدد **الإنتاج** لتحديد أن خيار التوريد الافتراضي لأصل المنتج هذا هو إنتاجه.</span><span class="sxs-lookup"><span data-stu-id="98683-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="98683-137">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="98683-137">Select **Save**.</span></span>
20. <span data-ttu-id="98683-138">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="98683-138">Close the page.</span></span>
21. <span data-ttu-id="98683-139">أغلق نموذج **تفاصيل المنتجات الصادرة‬**.</span><span class="sxs-lookup"><span data-stu-id="98683-139">Close the **Released product details** form.</span></span>

