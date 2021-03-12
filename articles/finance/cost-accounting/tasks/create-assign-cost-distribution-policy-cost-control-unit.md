---
title: إنشاء وتعيين سياسة توزيع التكلفة إلى وحدة التحكم في التكلفة
description: يتم استخدام قواعد توزيع التكلفة لتوزيع التكلفة التي تم جردها ماليًا في مركز تكلفة جماعي.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostDistributionRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b269c731776e26df24658feedfa301181c309a14
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969268"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="ab145-103">إنشاء وتعيين سياسة توزيع التكلفة إلى وحدة التحكم في التكلفة</span><span class="sxs-lookup"><span data-stu-id="ab145-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab145-104">يتم استخدام قواعد توزيع التكلفة لتوزيع التكلفة التي تم جردها ماليًا في مركز تكلفة جماعي.</span><span class="sxs-lookup"><span data-stu-id="ab145-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="ab145-105">يتأكد محاسب التكاليف من توزيع التكلفة على مراكز التكلفة، بناء على أساس التوزيع المحدد.</span><span class="sxs-lookup"><span data-stu-id="ab145-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="ab145-106">يتم تعيين سياسة وقواعد مناظرة إلى وحدة التحكم بالتكاليف.</span><span class="sxs-lookup"><span data-stu-id="ab145-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="ab145-107">يستخدم دليل المهام هذا مثالاً لإظهار كيفية إنشاء سياسة توزيع التكلفة والقواعد المناظرة.</span><span class="sxs-lookup"><span data-stu-id="ab145-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="ab145-108">إنشاء سياسة</span><span class="sxs-lookup"><span data-stu-id="ab145-108">Create a policy</span></span>
1. <span data-ttu-id="ab145-109">انتقل إلى محاسبة التكاليف > السياسات > سياسات توزيع التكلفة‬.</span><span class="sxs-lookup"><span data-stu-id="ab145-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="ab145-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ab145-110">Click New.</span></span>
3. <span data-ttu-id="ab145-111">في الحقل "اسم السياسة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ab145-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="ab145-112">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ab145-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ab145-113">في الحقل "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab145-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="ab145-114">حدد "المؤسسة".</span><span class="sxs-lookup"><span data-stu-id="ab145-114">Select Organization.</span></span>  
6. <span data-ttu-id="ab145-115">في الحقل "تدرج بُعد عنصر التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab145-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="ab145-116">حدد CDS P/L.</span><span class="sxs-lookup"><span data-stu-id="ab145-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="ab145-117">في الحقل "البعد الإحصائي"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab145-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="ab145-118">حدد "العناصر الإحصائية".</span><span class="sxs-lookup"><span data-stu-id="ab145-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="ab145-119">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="ab145-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="ab145-120">إنشاء قواعد للسياسة</span><span class="sxs-lookup"><span data-stu-id="ab145-120">Create rules for the policy</span></span>
1. <span data-ttu-id="ab145-121">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ab145-121">Click New.</span></span>
2. <span data-ttu-id="ab145-122">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ab145-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="ab145-123">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab145-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="ab145-124">قم بتوسيع التدرج الهرمي لتحديد 094.</span><span class="sxs-lookup"><span data-stu-id="ab145-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="ab145-125">في الحقل "عقدة التدرج الهرمي لبُعد عنصر التكلفة‬‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab145-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="ab145-126">حدد "مصروفات التشغيل الأخرى"، ثم حدد "605110 تنظيف".</span><span class="sxs-lookup"><span data-stu-id="ab145-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="ab145-127">في الحقل "سلوك التكلفة"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="ab145-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="ab145-128">حدد "التكلفة الثابتة".</span><span class="sxs-lookup"><span data-stu-id="ab145-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="ab145-129">في الحقل "أساس التوزيع"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="ab145-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="ab145-130">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ab145-130">Click New.</span></span>
8. <span data-ttu-id="ab145-131">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ab145-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="ab145-132">في العقدة "تدرج بُعد كائن التكلفة‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab145-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="ab145-133">قم بتوسيع التدرج الهرمي لتحديد 094.</span><span class="sxs-lookup"><span data-stu-id="ab145-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="ab145-134">في الحقل "عقدة التدرج الهرمي لبُعد عنصر التكلفة‬‬‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab145-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="ab145-135">حدد "مصروفات التشغيل الأخرى"، ثم حدد "605150 إيجار".</span><span class="sxs-lookup"><span data-stu-id="ab145-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="ab145-136">في الحقل "سلوك التكلفة"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="ab145-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="ab145-137">حدد "التكلفة الثابتة".</span><span class="sxs-lookup"><span data-stu-id="ab145-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="ab145-138">في الحقل "أساس التوزيع"، أدخل أو حدد قيمة.</span><span class="sxs-lookup"><span data-stu-id="ab145-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="ab145-139">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="ab145-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="ab145-140">تعيين قواعد لوحدة التحكم بالتكاليف</span><span class="sxs-lookup"><span data-stu-id="ab145-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="ab145-141">انقر فوق "تعيينات السياسة" لوحدة التحكم بالتكاليف.</span><span class="sxs-lookup"><span data-stu-id="ab145-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="ab145-142">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="ab145-142">Click New.</span></span>
3. <span data-ttu-id="ab145-143">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="ab145-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ab145-144">أدخل تاريخًا في الحقل "صالح بدءًا من تاريخ المحاسبة‬‬".</span><span class="sxs-lookup"><span data-stu-id="ab145-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="ab145-145">حدد 1 سبتمبر في السنة المالية الصالحة.</span><span class="sxs-lookup"><span data-stu-id="ab145-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="ab145-146">في الحقل "وحدة التحكم بالتكاليف‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="ab145-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="ab145-147">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="ab145-147">Click Save.</span></span>

