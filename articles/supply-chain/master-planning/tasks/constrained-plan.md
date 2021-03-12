---
title: إنشاء خطة مقيدة
description: يوضح هذا الموضوع كيفية إنشاء خطة تأخذ في الاعتبار القيود المادية وقيود القدرة.
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d4af946a8dd4e5311bcb90386c88d5e7f205c4eb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999846"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="b827f-103">إنشاء خطة مقيدة</span><span class="sxs-lookup"><span data-stu-id="b827f-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b827f-104">يوضح هذا الموضوع كيفية إنشاء خطة تأخذ في الاعتبار القيود المادية وقيود القدرة.</span><span class="sxs-lookup"><span data-stu-id="b827f-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="b827f-105">تضمن الخطة عدم بدء التصنيع قبل أن تتوفر المواد وعدم تعرض الموارد لزيادة في الحجز.</span><span class="sxs-lookup"><span data-stu-id="b827f-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="b827f-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="b827f-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b827f-107">هذا الإجراء مخصص لمخطط الإنتاج‬.</span><span class="sxs-lookup"><span data-stu-id="b827f-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="b827f-108">إعداد خطة مقيدة</span><span class="sxs-lookup"><span data-stu-id="b827f-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="b827f-109">في الصفحة الرئيسية، حدد مساحة عمل **التخطيط الرئيسي**.</span><span class="sxs-lookup"><span data-stu-id="b827f-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="b827f-110">حدد **الخطط الرئيسية** في قائمة الارتباطات إلى أقصى يسار مساحة العمل.</span><span class="sxs-lookup"><span data-stu-id="b827f-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="b827f-111">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b827f-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="b827f-112">مثال: **StaticPlan**</span><span class="sxs-lookup"><span data-stu-id="b827f-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="b827f-113">حدد **نعم** في الحقل **قدرة محدودة‬**.</span><span class="sxs-lookup"><span data-stu-id="b827f-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="b827f-114">في الحقل **الحد الزمني للقدرة المحدودة‬**، أدخل `30`.</span><span class="sxs-lookup"><span data-stu-id="b827f-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="b827f-115">قم بتوسيع القسم **الحدود الزمنية بالأيام**.</span><span class="sxs-lookup"><span data-stu-id="b827f-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="b827f-116">حدد **نعم** في الحقل **قدرة**.</span><span class="sxs-lookup"><span data-stu-id="b827f-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="b827f-117">في الحقل **الحد الزمني لجدولة القدرة (بالأيام)‬**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="b827f-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="b827f-118">مثال: `60`</span><span class="sxs-lookup"><span data-stu-id="b827f-118">Example: `60`</span></span>  
9. <span data-ttu-id="b827f-119">حدد **نعم** في الحقل **التأخيرات المحسوبة**‬.</span><span class="sxs-lookup"><span data-stu-id="b827f-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="b827f-120">في الحقل **الحد الزمني لحساب التأخيرات (بالأيام)‬‬**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="b827f-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="b827f-121">مثال: `60`</span><span class="sxs-lookup"><span data-stu-id="b827f-121">Example: `60`</span></span> 
11. <span data-ttu-id="b827f-122">وسّع القسم **التأخيرات المحسوبة**.</span><span class="sxs-lookup"><span data-stu-id="b827f-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="b827f-123">حدد **نعم** في الحقل **إضافة التأخير المحسوب إلى تاريخ المتطلبات**‬.</span><span class="sxs-lookup"><span data-stu-id="b827f-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="b827f-124">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b827f-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="b827f-125">إنشاء خطة مقيدة</span><span class="sxs-lookup"><span data-stu-id="b827f-125">Create a constrained plan</span></span>
1. <span data-ttu-id="b827f-126">حدد **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="b827f-126">Select **Run**.</span></span>
2. <span data-ttu-id="b827f-127">في حقل **الخطة الرئيسية**، أدخل أو حدد الخطة التي قمت بإعداد قيود لها.</span><span class="sxs-lookup"><span data-stu-id="b827f-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="b827f-128">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b827f-128">Select **OK**.</span></span>
4. <span data-ttu-id="b827f-129">حدد **الأوامر المخططة‬**.</span><span class="sxs-lookup"><span data-stu-id="b827f-129">Select **Planned orders**.</span></span>

