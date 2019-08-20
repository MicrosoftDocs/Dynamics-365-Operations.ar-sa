---
title: مراقبة تشغيل التخطيط الرئيسي
description: يريد مخطط الإنتاج معرفة ما إذا كان تشغيل تخطيط أساسي قيد التقدم.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b923b215528ecceaed9b5057ddb736ec959f1d65
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845103"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="acb3f-103">مراقبة تشغيل التخطيط الرئيسي</span><span class="sxs-lookup"><span data-stu-id="acb3f-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="acb3f-104">يريد مخطط الإنتاج معرفة ما إذا كان تشغيل تخطيط أساسي قيد التقدم.</span><span class="sxs-lookup"><span data-stu-id="acb3f-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="acb3f-105">استخدم شركة بيانات العرض التوضيحي USMF لإكمال هذا الإجراء.</span><span class="sxs-lookup"><span data-stu-id="acb3f-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="acb3f-106">تشغيل التخطيط الرئيسي</span><span class="sxs-lookup"><span data-stu-id="acb3f-106">Run master planning</span></span>
1. <span data-ttu-id="acb3f-107">انقر فوق "التخطيط الرئيسي‬".</span><span class="sxs-lookup"><span data-stu-id="acb3f-107">Click Master planning.</span></span>
    * <span data-ttu-id="acb3f-108">ستجد هذا على لوحة المعلومات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="acb3f-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="acb3f-109">في حقل "الخطة"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="acb3f-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="acb3f-110">على سبيل المثال: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="acb3f-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="acb3f-111">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="acb3f-111">Click Run.</span></span>
4. <span data-ttu-id="acb3f-112">حدد "نعم" في الحقل "تتبع وقت المعالجة".</span><span class="sxs-lookup"><span data-stu-id="acb3f-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="acb3f-113">في حالة تحديد الحقل بالفعل، قم بتخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="acb3f-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="acb3f-114">في الحقل "عدد السلاسل"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="acb3f-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="acb3f-115">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="acb3f-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="acb3f-116">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="acb3f-116">Click Filter.</span></span>
8. <span data-ttu-id="acb3f-117">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="acb3f-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="acb3f-118">وضع علامة على الصف حيث الحقل = رقم الصنف.</span><span class="sxs-lookup"><span data-stu-id="acb3f-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="acb3f-119">في الحقل "المعايير‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="acb3f-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="acb3f-120">على سبيل المثال: T0001</span><span class="sxs-lookup"><span data-stu-id="acb3f-120">Example: T0001</span></span>  
10. <span data-ttu-id="acb3f-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="acb3f-121">Click OK.</span></span>
11. <span data-ttu-id="acb3f-122">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="acb3f-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="acb3f-123">مراقبة تشغيل التخطيط الرئيسي</span><span class="sxs-lookup"><span data-stu-id="acb3f-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="acb3f-124">انقر فوق "التاريخ".</span><span class="sxs-lookup"><span data-stu-id="acb3f-124">Click History.</span></span>
2. <span data-ttu-id="acb3f-125">انقر فوق "استعلامات".</span><span class="sxs-lookup"><span data-stu-id="acb3f-125">Click Inquiries.</span></span>
3. <span data-ttu-id="acb3f-126">انقر فوق "مدة مهمة المعالجة".</span><span class="sxs-lookup"><span data-stu-id="acb3f-126">Click Process task duration.</span></span>
4. <span data-ttu-id="acb3f-127">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="acb3f-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="acb3f-128">لكل عنصر، يمكنك الحصول على نظرة عامة حول المدة المستغرقة لإكمال كل خطوة تخطيط.</span><span class="sxs-lookup"><span data-stu-id="acb3f-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  

