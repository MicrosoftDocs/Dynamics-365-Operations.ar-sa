---
title: إنشاء قوالب مواعيد العمل
description: تعرف قوالب أوقات العمل ساعات العمل خلال أسبوع ويتم استخدامها لإنشاء أوقات العمل لفترة من الوقت.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c82126d64954f8691571b80ab97b198d58a9e2cb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837695"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="37185-103">إنشاء قوالب مواعيد العمل</span><span class="sxs-lookup"><span data-stu-id="37185-103">Create working time templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37185-104">تعرف قوالب أوقات العمل ساعات العمل خلال أسبوع ويتم استخدامها لإنشاء أوقات العمل لفترة من الوقت.</span><span class="sxs-lookup"><span data-stu-id="37185-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="37185-105">يوضح هذا الإجراء كيفية تعريف قالب أوقات عمل باستخدام خصائص جدولة أوقات العمل لتصنيف الفواصل الزمنية لأوقات العمل.</span><span class="sxs-lookup"><span data-stu-id="37185-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="37185-106">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="37185-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="37185-107">انتقل إلى كافة مساحات العمل > إدارة دورة حياة الموارد.</span><span class="sxs-lookup"><span data-stu-id="37185-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="37185-108">انقر فوق نسخ "قوالب أوقات العمل".</span><span class="sxs-lookup"><span data-stu-id="37185-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="37185-109">إنشاء قالب أوقات العمل</span><span class="sxs-lookup"><span data-stu-id="37185-109">Create working time template</span></span>
1. <span data-ttu-id="37185-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="37185-110">Click New.</span></span>
2. <span data-ttu-id="37185-111">في الحقل "قالب أوقات العمل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="37185-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="37185-112">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="37185-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="37185-113">قم بتوسيع القسم "الاثنين".</span><span class="sxs-lookup"><span data-stu-id="37185-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="37185-114">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="37185-114">Click Add.</span></span>
6. <span data-ttu-id="37185-115">في الحقل "من"، أدخل وقتًا.</span><span class="sxs-lookup"><span data-stu-id="37185-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="37185-116">تحديد وقت بدء العمل في الصباح.</span><span class="sxs-lookup"><span data-stu-id="37185-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="37185-117">في الحقل "إلى"، أدخل وقتًا.</span><span class="sxs-lookup"><span data-stu-id="37185-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="37185-118">حدد وقت استراحة العمال لتناول الغداء.</span><span class="sxs-lookup"><span data-stu-id="37185-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="37185-119">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="37185-119">Click Add.</span></span>
9. <span data-ttu-id="37185-120">في الحقل "من"، أدخل وقتًا.</span><span class="sxs-lookup"><span data-stu-id="37185-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="37185-121">حدد وقت استئناف العمل بعد تناول الغداء.</span><span class="sxs-lookup"><span data-stu-id="37185-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="37185-122">في الحقل "إلى"، أدخل وقتًا.</span><span class="sxs-lookup"><span data-stu-id="37185-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="37185-123">حدد وقت نهاية يوم العمل.</span><span class="sxs-lookup"><span data-stu-id="37185-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="37185-124">تكرار أوقات العمل لجميع أيام الأسبوع</span><span class="sxs-lookup"><span data-stu-id="37185-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="37185-125">انقر فوق "نسخ اليوم".</span><span class="sxs-lookup"><span data-stu-id="37185-125">Click Copy day.</span></span>
    * <span data-ttu-id="37185-126">انسخ تعريفات أوقات العمل من يوم الاثنين إلى يوم الثلاثاء.</span><span class="sxs-lookup"><span data-stu-id="37185-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="37185-127">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="37185-127">Click OK.</span></span>
3. <span data-ttu-id="37185-128">انقر فوق "نسخ اليوم".</span><span class="sxs-lookup"><span data-stu-id="37185-128">Click Copy day.</span></span>
    * <span data-ttu-id="37185-129">انسخ تعريفات أوقات العمل من يوم الاثنين إلى يوم الأربعاء.</span><span class="sxs-lookup"><span data-stu-id="37185-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="37185-130">في الحقل "إلى يوم الأسبوع"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="37185-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="37185-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="37185-131">Click OK.</span></span>
6. <span data-ttu-id="37185-132">انقر فوق "نسخ اليوم".</span><span class="sxs-lookup"><span data-stu-id="37185-132">Click Copy day.</span></span>
    * <span data-ttu-id="37185-133">انسخ تعريفات أوقات العمل من يوم الاثنين إلى يوم الخميس.</span><span class="sxs-lookup"><span data-stu-id="37185-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="37185-134">في الحقل "إلى يوم الأسبوع"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="37185-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="37185-135">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="37185-135">Click OK.</span></span>
9. <span data-ttu-id="37185-136">انقر فوق "نسخ اليوم".</span><span class="sxs-lookup"><span data-stu-id="37185-136">Click Copy day.</span></span>
    * <span data-ttu-id="37185-137">انسخ تعريفات أوقات العمل من يوم الاثنين إلى الجمعة.</span><span class="sxs-lookup"><span data-stu-id="37185-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="37185-138">في الحقل "إلى يوم الأسبوع"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="37185-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="37185-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="37185-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="37185-140">تحديد فترات زمنية للعمليات الخاصة</span><span class="sxs-lookup"><span data-stu-id="37185-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="37185-141">قم بتوسيع القسم "الجمعة".</span><span class="sxs-lookup"><span data-stu-id="37185-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="37185-142">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="37185-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="37185-143">في الحقل "الخاصية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37185-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="37185-144">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="37185-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="37185-145">في الحقل "الخاصية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37185-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="37185-146">وضع علامة "مُغلق للانتقاء" لأيام عطلات نهاية الأسبوع</span><span class="sxs-lookup"><span data-stu-id="37185-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="37185-147">قم بتوسيع القسم "السبت".</span><span class="sxs-lookup"><span data-stu-id="37185-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="37185-148">حدد "نعم" في القسم "مُغلق للانتقاء".</span><span class="sxs-lookup"><span data-stu-id="37185-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="37185-149">قم بتوسيع القسم "الأحد".</span><span class="sxs-lookup"><span data-stu-id="37185-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="37185-150">حدد "نعم" في القسم "مُغلق للانتقاء".</span><span class="sxs-lookup"><span data-stu-id="37185-150">Select Yes in the Closed for pickup field.</span></span>

