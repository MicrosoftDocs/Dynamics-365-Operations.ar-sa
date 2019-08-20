---
title: إنشاء علاقة نشاط - عنصر لاحق
description: يتم توثيق تدفق الأنشطة في تدفق إنتاج محدود الفاقد من خلال علاقات النشاط.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58e003c6521c4ef007b8e0e1e17d51715435e875
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838717"
---
# <a name="create-activity-relation-successor"></a><span data-ttu-id="2810f-103">إنشاء علاقة نشاط: عنصر لاحق</span><span class="sxs-lookup"><span data-stu-id="2810f-103">Create activity relation: Successor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2810f-104">يتم توثيق تدفق الأنشطة في تدفق إنتاج محدود الفاقد من خلال علاقات النشاط.</span><span class="sxs-lookup"><span data-stu-id="2810f-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="2810f-105">يوضح هذا التسجيل كيفية إنشاء علاقة نشاط.</span><span class="sxs-lookup"><span data-stu-id="2810f-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="2810f-106">المتطلبات الأساسية:</span><span class="sxs-lookup"><span data-stu-id="2810f-106">Prerequisites:</span></span>

- <span data-ttu-id="2810f-107">تدفق إنتاج وإصدار في وضع المسودة.</span><span class="sxs-lookup"><span data-stu-id="2810f-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="2810f-108">يتم إنشاء نشاطين يتبعان بعضهما البعض في تدفق الإنتاج لكن لا يتم ربطهما.</span><span class="sxs-lookup"><span data-stu-id="2810f-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="2810f-109">البحث عن إصدار تدفق الإنتاج</span><span class="sxs-lookup"><span data-stu-id="2810f-109">Find the production flow version</span></span> 
1. <span data-ttu-id="2810f-110">انتقل إلى عنصر التحكم بالإنتاج > الإعداد > تدفق الإنتاج محدود الفاقد > تدفقات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="2810f-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="2810f-111">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="2810f-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2810f-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2810f-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2810f-113">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2810f-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="2810f-114">في القائمة، حدد إصدارًا مسودة.</span><span class="sxs-lookup"><span data-stu-id="2810f-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="2810f-115">يمكن إضافة علاقات للإصدارات المسودة أو الإصدارات النشطة لتدفق إنتاج.</span><span class="sxs-lookup"><span data-stu-id="2810f-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="2810f-116">فتح نظرة عامة عن النشاط</span><span class="sxs-lookup"><span data-stu-id="2810f-116">Open the activity overview</span></span>
1. <span data-ttu-id="2810f-117">انقر فوق "الأنشطة".</span><span class="sxs-lookup"><span data-stu-id="2810f-117">Click Activities.</span></span>
    * <span data-ttu-id="2810f-118">لاحظ أن النموذج يُظهر جميع أنشطة تدفق الإنتاج التي تم تخصيصها لإصدار تدفقات الإنتاج التي تعمل فيه.</span><span class="sxs-lookup"><span data-stu-id="2810f-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="2810f-119">إضافة عنصر لاحق</span><span class="sxs-lookup"><span data-stu-id="2810f-119">Add a Successor</span></span>
1. <span data-ttu-id="2810f-120">انقر فوق "إضافة عنصر لاحق".</span><span class="sxs-lookup"><span data-stu-id="2810f-120">Click Add successor.</span></span>
2. <span data-ttu-id="2810f-121">في الحقل "النشاط"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="2810f-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="2810f-122">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="2810f-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="2810f-123">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2810f-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2810f-124">حدد خانة اختيار "التقييد".</span><span class="sxs-lookup"><span data-stu-id="2810f-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="2810f-125">في الحقل "قيمة التقييد"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2810f-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="2810f-126">وقت التقييد هو الوقت المطلوب جدولته بين النهاية المجدولة للنشاط السابق (تاريخ الاستحقاق ووقته) والبداية المجدولة للنشاط التالي.</span><span class="sxs-lookup"><span data-stu-id="2810f-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="2810f-127">في الحقل "الوحدات"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2810f-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="2810f-128">في الحقل "نسبة زمن الدورة"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2810f-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="2810f-129">في حالة تشغيل النشاطين في المنتج نفسه، يجب أن تكون نسبة زمن الدورة 1.</span><span class="sxs-lookup"><span data-stu-id="2810f-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="2810f-130">في حالة تشغيل المهمة السابقة بسرعة مضاعفة مقارنة بالمهمة اللاحقة، يجب أن تكون النسبة 2.</span><span class="sxs-lookup"><span data-stu-id="2810f-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="2810f-131">تُستخدم نسب زمن الدورة لحساب أزمان الدورة الفردية لأنشطة تدفق الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="2810f-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="2810f-132">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="2810f-132">Click OK.</span></span>
10. <span data-ttu-id="2810f-133">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2810f-133">Close the page.</span></span>
11. <span data-ttu-id="2810f-134">انقر فوق علامة التبويب "GridPanel".</span><span class="sxs-lookup"><span data-stu-id="2810f-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="2810f-135">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2810f-135">Close the page.</span></span>
13. <span data-ttu-id="2810f-136">قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="2810f-136">Refresh the page.</span></span>

