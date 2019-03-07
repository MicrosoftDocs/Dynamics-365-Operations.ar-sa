---
title: إكمال الإعداد الأساسي لأصل منتج تم إصداره
description: يوضح هذا الإجراء كيفية إكمال إعداد الحد الأدنى المطلوب قبل أن يمكن استخدام أصل المنتج في إصدارات قائمة مكونات الصنف.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d3a91977c38c0ce0f9fe114bec943c7cb32a5d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "354772"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="4f8f0-103">إكمال الإعداد الأساسي لأصل منتج تم إصداره</span><span class="sxs-lookup"><span data-stu-id="4f8f0-103">Complete basic setup of a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4f8f0-104">يوضح هذا الإجراء كيفية إكمال إعداد الحد الأدنى المطلوب قبل أن يمكن استخدام أصل المنتج في إصدارات قائمة مكونات الصنف.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="4f8f0-105">هذا هو الإجراء الثالث من أصل ثمانية إجراءات الذي يوضح كيفية إنشاء مجموعات للتكوين المستند إلى بُعد.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="4f8f0-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="4f8f0-107">انتقل إلى إدارة معلومات المنتج > المنتجات > المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="4f8f0-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4f8f0-109">حدد أصل المنتج الذي أصدرتَه في الإجراء الثاني.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="4f8f0-110">يتم إنشاء أصل المنتج هذا باستخدام تقنية التكوين المستند إلى ُبعد.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="4f8f0-111">في جزء الإجراءات، انقر فوق "المنتج".</span><span class="sxs-lookup"><span data-stu-id="4f8f0-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="4f8f0-112">انقر فوق "مجموعات الأبعاد" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="4f8f0-113">في الحقل "مجموعة أبعاد التخزين‬‬‬‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4f8f0-114">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4f8f0-115">تحدد مجموعة بُعد التخزين أبعاد التخزين التي تُستخدم لحركة المنتج.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="4f8f0-116">حدد "موقع هذا الإجراء".</span><span class="sxs-lookup"><span data-stu-id="4f8f0-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="4f8f0-117">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4f8f0-118">في الحقل "مجموعة أبعاد التعقب‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="4f8f0-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4f8f0-120">تحدد مجموعة بُعد التعقب أبعاد التعقب التي تُستخدم لحركة المنتج.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="4f8f0-121">حدد "بلا" بالنسبة لهذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="4f8f0-122">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="4f8f0-123">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="4f8f0-123">Click OK.</span></span>
12. <span data-ttu-id="4f8f0-124">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="4f8f0-125">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="4f8f0-125">Click Edit.</span></span>
    * <span data-ttu-id="4f8f0-126">افتح نموذج تفاصيل المنتج لمواصلة مهمة الإعداد.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="4f8f0-127">في الحقل "مجموعة نماذج الصنف‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="4f8f0-128">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4f8f0-129">تحتوي مجموعات نموذج الصنف على الإعدادات التي تحدد كيفية التحكم في الأصناف ومعالجتها في إيصالات الأصناف وإصداراتها.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="4f8f0-130">كما تحدد أيضًا كيفية حساب استهلاك الصنف.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="4f8f0-131">حدد "FIFO" بالنسبة لهذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="4f8f0-132">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="4f8f0-133">قم بتوسيع قسم إدارة التكاليف أو طيه.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="4f8f0-134">في الحقل "مجموعة الأصناف‬‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="4f8f0-135">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4f8f0-136">يتم استخدام مجموعات الأصناف لإدارة المخزون بتقسيم أصناف المخزون إلى مجموعات.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="4f8f0-137">حدد "CarAudio" بالنسبة لهذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="4f8f0-138">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="4f8f0-139">في جزء "الإجراءات"، انقر فوق "خطة".</span><span class="sxs-lookup"><span data-stu-id="4f8f0-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="4f8f0-140">انقر فوق "إعدادات الأوامر الافتراضية".</span><span class="sxs-lookup"><span data-stu-id="4f8f0-140">Click Default order settings.</span></span>
23. <span data-ttu-id="4f8f0-141">في الحقل "نوع الأمر الافتراضي"، حدد خيارًا ما.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="4f8f0-142">حدد "الإنتاج" لتحديد أن خيار العرض الافتراضي لأصل المنتج هذا هو إصداره.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="4f8f0-143">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-143">Close the page.</span></span>
25. <span data-ttu-id="4f8f0-144">أغلق نموذج تفاصيل المنتجات التي تم إصدارها.</span><span class="sxs-lookup"><span data-stu-id="4f8f0-144">Close the Released product details form.</span></span>

