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
ms.openlocfilehash: 8cc9fc58c9a14c20eecd486e3869a9b00c54c2c5
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149126"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="fcf3f-103">إنشاء قوالب مواعيد العمل</span><span class="sxs-lookup"><span data-stu-id="fcf3f-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fcf3f-104">تعرف قوالب أوقات العمل ساعات العمل خلال أسبوع ويتم استخدامها لإنشاء أوقات العمل لفترة من الوقت.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="fcf3f-105">يوضح هذا الإجراء كيفية تعريف قالب أوقات عمل باستخدام خصائص جدولة أوقات العمل لتصنيف الفواصل الزمنية لأوقات العمل.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="fcf3f-106">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="fcf3f-107">انتقل إلى كافة مساحات العمل > إدارة دورة حياة الموارد.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="fcf3f-108">انقر فوق نسخ "قوالب أوقات العمل".</span><span class="sxs-lookup"><span data-stu-id="fcf3f-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="fcf3f-109">إنشاء قالب أوقات العمل</span><span class="sxs-lookup"><span data-stu-id="fcf3f-109">Create working time template</span></span>
1. <span data-ttu-id="fcf3f-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="fcf3f-110">Click New.</span></span>
2. <span data-ttu-id="fcf3f-111">في الحقل "قالب أوقات العمل"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="fcf3f-112">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="fcf3f-113">قم بتوسيع القسم "الاثنين".</span><span class="sxs-lookup"><span data-stu-id="fcf3f-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="fcf3f-114">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-114">Click Add.</span></span>
6. <span data-ttu-id="fcf3f-115">في الحقل "من"، أدخل وقتًا.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="fcf3f-116">تحديد وقت بدء العمل في الصباح.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="fcf3f-117">في الحقل "إلى"، أدخل وقتًا.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="fcf3f-118">حدد وقت استراحة العمال لتناول الغداء.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="fcf3f-119">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-119">Click Add.</span></span>
9. <span data-ttu-id="fcf3f-120">في الحقل "من"، أدخل وقتًا.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="fcf3f-121">حدد وقت استئناف العمل بعد تناول الغداء.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="fcf3f-122">في الحقل "إلى"، أدخل وقتًا.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="fcf3f-123">حدد وقت نهاية يوم العمل.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="fcf3f-124">تكرار أوقات العمل لجميع أيام الأسبوع</span><span class="sxs-lookup"><span data-stu-id="fcf3f-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="fcf3f-125">انقر فوق "نسخ اليوم".</span><span class="sxs-lookup"><span data-stu-id="fcf3f-125">Click Copy day.</span></span>
    * <span data-ttu-id="fcf3f-126">انسخ تعريفات أوقات العمل من يوم الاثنين إلى يوم الثلاثاء.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="fcf3f-127">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fcf3f-127">Click OK.</span></span>
3. <span data-ttu-id="fcf3f-128">انقر فوق "نسخ اليوم".</span><span class="sxs-lookup"><span data-stu-id="fcf3f-128">Click Copy day.</span></span>
    * <span data-ttu-id="fcf3f-129">انسخ تعريفات أوقات العمل من يوم الاثنين إلى يوم الأربعاء.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="fcf3f-130">في الحقل "إلى يوم الأسبوع"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="fcf3f-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fcf3f-131">Click OK.</span></span>
6. <span data-ttu-id="fcf3f-132">انقر فوق "نسخ اليوم".</span><span class="sxs-lookup"><span data-stu-id="fcf3f-132">Click Copy day.</span></span>
    * <span data-ttu-id="fcf3f-133">انسخ تعريفات أوقات العمل من يوم الاثنين إلى يوم الخميس.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="fcf3f-134">في الحقل "إلى يوم الأسبوع"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="fcf3f-135">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fcf3f-135">Click OK.</span></span>
9. <span data-ttu-id="fcf3f-136">انقر فوق "نسخ اليوم".</span><span class="sxs-lookup"><span data-stu-id="fcf3f-136">Click Copy day.</span></span>
    * <span data-ttu-id="fcf3f-137">انسخ تعريفات أوقات العمل من يوم الاثنين إلى الجمعة.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="fcf3f-138">في الحقل "إلى يوم الأسبوع"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="fcf3f-139">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="fcf3f-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="fcf3f-140">تحديد فترات زمنية للعمليات الخاصة</span><span class="sxs-lookup"><span data-stu-id="fcf3f-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="fcf3f-141">قم بتوسيع القسم "الجمعة".</span><span class="sxs-lookup"><span data-stu-id="fcf3f-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="fcf3f-142">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="fcf3f-143">في الحقل "الخاصية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="fcf3f-144">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="fcf3f-145">في الحقل "الخاصية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="fcf3f-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="fcf3f-146">وضع علامة "مُغلق للانتقاء" لأيام عطلات نهاية الأسبوع</span><span class="sxs-lookup"><span data-stu-id="fcf3f-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="fcf3f-147">قم بتوسيع القسم "السبت".</span><span class="sxs-lookup"><span data-stu-id="fcf3f-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="fcf3f-148">حدد "نعم" في القسم "مُغلق للانتقاء".</span><span class="sxs-lookup"><span data-stu-id="fcf3f-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="fcf3f-149">قم بتوسيع القسم "الأحد".</span><span class="sxs-lookup"><span data-stu-id="fcf3f-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="fcf3f-150">حدد "نعم" في القسم "مُغلق للانتقاء".</span><span class="sxs-lookup"><span data-stu-id="fcf3f-150">Select Yes in the Closed for pickup field.</span></span>

