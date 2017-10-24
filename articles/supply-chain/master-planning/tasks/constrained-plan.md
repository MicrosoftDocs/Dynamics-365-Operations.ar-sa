--- 
title: "إنشاء خطة مقيدة"
description: "يوضح هذا الإجراء كيفية إنشاء خطة تأخذ في الاعتبار القيود المادية وقيود القدرة."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 59c6a4a2b239b3fd6b6ddc8f06bfd007f0191f0a
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="37077-103">إنشاء خطة مقيدة</span><span class="sxs-lookup"><span data-stu-id="37077-103">Generate a constrained plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37077-104">يوضح هذا الإجراء كيفية إنشاء خطة تأخذ في الاعتبار القيود المادية وقيود القدرة.</span><span class="sxs-lookup"><span data-stu-id="37077-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="37077-105">تضمن الخطة عدم بدء التصنيع قبل أن تتوفر المواد وعدم تعرض الموارد لزيادة في الحجز.</span><span class="sxs-lookup"><span data-stu-id="37077-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="37077-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="37077-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="37077-107">هذا الإجراء مخصص لمخطط الإنتاج‬.</span><span class="sxs-lookup"><span data-stu-id="37077-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="37077-108">إعداد خطة مقيدة</span><span class="sxs-lookup"><span data-stu-id="37077-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="37077-109">انقر فوق "التخطيط الرئيسي‬".</span><span class="sxs-lookup"><span data-stu-id="37077-109">Click Master planning.</span></span>
2. <span data-ttu-id="37077-110">انقر فوق "التخطيطات الرئيسية‬".</span><span class="sxs-lookup"><span data-stu-id="37077-110">Click Master plans.</span></span>
3. <span data-ttu-id="37077-111">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="37077-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="37077-112">على سبيل المثال: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="37077-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="37077-113">حدد "نعم" في الحقل "قدرة محدودة‬".</span><span class="sxs-lookup"><span data-stu-id="37077-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="37077-114">في الحقل "الحد الزمني للقدرة المحدودة‬"، أدخل "30".</span><span class="sxs-lookup"><span data-stu-id="37077-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="37077-115">قم بتوسيع المقطع "الحدود الزمنية بالأيام‬".</span><span class="sxs-lookup"><span data-stu-id="37077-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="37077-116">حدد "نعم" في الحقل "قدرة".</span><span class="sxs-lookup"><span data-stu-id="37077-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="37077-117">في الحقل "الحد الزمني لجدولة القدرة (بالأيام)‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="37077-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="37077-118">على سبيل المثال: 60</span><span class="sxs-lookup"><span data-stu-id="37077-118">Example: 60</span></span>  
9. <span data-ttu-id="37077-119">حدد "نعم" في الحقل "التأخيرات المحسوبة‬‬".</span><span class="sxs-lookup"><span data-stu-id="37077-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="37077-120">في الحقل "الحد الزمني لحساب التأخيرات (بالأيام)‬‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="37077-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="37077-121">على سبيل المثال: 60</span><span class="sxs-lookup"><span data-stu-id="37077-121">Example: 60</span></span>  
11. <span data-ttu-id="37077-122">وسّع المقطع "التأخيرات المحسوبة".</span><span class="sxs-lookup"><span data-stu-id="37077-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="37077-123">حدد "نعم" في الحقل "إضافة التأخير المحسوب إلى تاريخ المتطلبات‬".</span><span class="sxs-lookup"><span data-stu-id="37077-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="37077-124">حدد "نعم" في الحقل "إضافة التأخير المحسوب إلى تاريخ المتطلبات‬".</span><span class="sxs-lookup"><span data-stu-id="37077-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="37077-125">حدد "نعم" في الحقل "إضافة التأخير المحسوب إلى تاريخ المتطلبات‬".</span><span class="sxs-lookup"><span data-stu-id="37077-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="37077-126">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="37077-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="37077-127">إنشاء خطة مقيدة</span><span class="sxs-lookup"><span data-stu-id="37077-127">Create a constrained plan</span></span>
1. <span data-ttu-id="37077-128">انقر فوق "تشغيل".</span><span class="sxs-lookup"><span data-stu-id="37077-128">Click Run.</span></span>
2. <span data-ttu-id="37077-129">في حقل "الخطة الرئيسية‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="37077-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="37077-130">حدد الخطة التي قمت بإعداد القيود لها.</span><span class="sxs-lookup"><span data-stu-id="37077-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="37077-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="37077-131">Click OK.</span></span>
    * <span data-ttu-id="37077-132">قد يستغرق هذا الأمر بعض الوقت.</span><span class="sxs-lookup"><span data-stu-id="37077-132">This may take a while.</span></span>  
4. <span data-ttu-id="37077-133">انقر فوق "الأوامر المخططة".</span><span class="sxs-lookup"><span data-stu-id="37077-133">Click Planned orders.</span></span>


