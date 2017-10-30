---
title: "مشاريع التوظيف الجماعي"
description: "تسمح مشاريع التوظيف الجماعي لأخصائي الموارد البشرية بإنشاء مناصب متعددة وتوظيف عدد من العاملين في تلك المناصب بطريقة فعالة."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HRMMassHireProject
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e57db8f4b692aa9c27916625897e268f63031782
ms.openlocfilehash: ab074b3ad72ab96ffb9c95005f22dc023fc923e4
ms.contentlocale: ar-sa
ms.lasthandoff: 10/30/2017

---

# <a name="mass-hire-projects"></a><span data-ttu-id="6ca8b-103">مشاريع التوظيف الجماعي</span><span class="sxs-lookup"><span data-stu-id="6ca8b-103">Mass hire projects</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6ca8b-104">تسمح مشاريع التوظيف الجماعي لأخصائي الموارد البشرية بإنشاء مناصب متعددة وتوظيف عدد من العاملين في تلك المناصب بطريقة فعالة.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-104">Mass hire projects allow human resources specialists to create multiple positions and efficiently hire workers into those positions.</span></span>

<a name="overview"></a><span data-ttu-id="6ca8b-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="6ca8b-105">Overview</span></span>
--------

<span data-ttu-id="6ca8b-106">استخدم مشاريع التوظيف الجماعي عند توظيف عدة موظفين في نفس الوقت، مثلاً، عند القيام بالتوظيف لتلبية احتياجات أحد المواسم.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-106">Use mass hire projects when you hire multiple workers at one time, such as when you hire to meet a seasonal demand.</span></span> <span data-ttu-id="6ca8b-107">ويُعد إنشاء مشروع توظيف جماعي مفيدًا، لأنه يمكنك إنشاء سجلات المناصب، وسجلات العاملين، وتعيينات العمال للمناصب في نفس الوقت.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-107">Creating a mass hire project is useful because you can create position records, worker records, and worker assignments for positions at the same time.</span></span> <span data-ttu-id="6ca8b-108">وعندما تقوم بإنشاء مناصب لمشروع توظيف جماعي، فإنه يمكنك تحديد المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="6ca8b-108">When you create positions for a mass hire project, you can specify the following information:</span></span>
-   <span data-ttu-id="6ca8b-109">عدد المناصب المراد إنشاؤها</span><span class="sxs-lookup"><span data-stu-id="6ca8b-109">The number of positions to create</span></span>
-   <span data-ttu-id="6ca8b-110">نوع العامل للأشخاص الذين سيتم توظيفهم لشغل المناصب</span><span class="sxs-lookup"><span data-stu-id="6ca8b-110">The worker type of the people that you will hire for the positions</span></span>
-   <span data-ttu-id="6ca8b-111">القسم والوظيفة المقترنان بالمناصب</span><span class="sxs-lookup"><span data-stu-id="6ca8b-111">The department and the job that are associated with the positions</span></span>
-   <span data-ttu-id="6ca8b-112">قيمة الدوام الكامل المكافئة للمنصب</span><span class="sxs-lookup"><span data-stu-id="6ca8b-112">The full-time equivalent value of the position</span></span>

## <a name="example"></a><span data-ttu-id="6ca8b-113">مثال</span><span class="sxs-lookup"><span data-stu-id="6ca8b-113">Example</span></span>
<span data-ttu-id="6ca8b-114">في فصل الصيف، يمكنك عادةً استخدام 15-20 طالب كلية لبعض الوقت لملء فترات التدريب المتوفرة في الشركة.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-114">In the summer, you usually hire 15-20 part-time college students to fill available internships in your company.</span></span> <span data-ttu-id="6ca8b-115">وفي هذا العام، تحتاج إلى توظيف خمسة محاسبين، وخمسة معالجين للأوامر، وخمسة كاشيرات.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-115">This year, you want to hire five accountants, five order processors, and five cashiers.</span></span> <span data-ttu-id="6ca8b-116">وبدلاً من إنشاء كل سجل منصب وسجل عامل بشكل منفصل، يمكنك إنشاء مشروع التوظيف الجماعي باسم "فترات التدريب الصيفية".</span><span class="sxs-lookup"><span data-stu-id="6ca8b-116">Instead of creating each position record and worker record separately, you create one mass hire project called “SummerInterns”.</span></span> <span data-ttu-id="6ca8b-117">وترتبط تواريخ بدء زانتهاء المشاريع بتواريخ البدء والانتهاء لمدد المناصب للمناصب التي تقوم بإنشائها لمشروع التوظيف الجماعي.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-117">The project start and end dates correlate with the start and end dates of the position durations for the positions you create for the mass hire project.</span></span> 

<span data-ttu-id="6ca8b-118">وفي صفحة **مشاريع التوظيف الجماعي**، حدد مشروع "فترات التدريب الصيفية"، ثم انقر فوق **فتح مشروع**.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-118">In the **Mass hire projects** page, select the “SummerInterns” project and then click **Open project**.</span></span> <span data-ttu-id="6ca8b-119">وفي مشروع التوظيف الجماعي المفتوح، انقر فوق **إنشاء مناصب** وأدخل المعلومات المتعلقة بمنصب المحاسب.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-119">In the open mass hire project, click **Create positions** and enter information about the accountant position.</span></span> <span data-ttu-id="6ca8b-120">ويمكنك الإشارة إلى أن مناصب المحاسب الخمسة يجب إنشاؤها باستخدام نفس المعلومات لكل واحد منها، ثم انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="6ca8b-120">You can indicate that five accountant positions should be created using the same information for each one, and then click OK.</span></span> <span data-ttu-id="6ca8b-121">كرر هذه العملية لمناصب معالجي الأوامر والكاشيرات.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-121">Repeat this process for the order processor and cashier positions.</span></span> 

<span data-ttu-id="6ca8b-122">وبعد تحديد الطلاب للتعيين لشغل وظائف التدريب الداخلي، ستقوم بإدخال معلومات كل طالب في **تفاصيل المنصب** للمنصب الذي تقوم بتعيينهم له.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-122">After selecting students to hire for the internship positions, you'll enter each student’s information in the **Position details** for the position that you're hiring them for.</span></span> <span data-ttu-id="6ca8b-123">وبعد قيامك بإدخال كافة تفاصيل المناصب، حدد المنصب في صفحة مشاريع التوظيف الجماعي، ثم انقر فوق **توظيف**.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-123">When you have entered all of the position details, select the position in the Mass hire projects page, and then click **Hire**.</span></span> <span data-ttu-id="6ca8b-124">سيتم إنشاء سجل منصب لكل منصب وسيتم إنشاء سجل عامل وتعيينه للمنصب الصحيح لكل شخص تقوم بتوظيفه.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-124">A position record will be created for each position and a worker record will be created and assigned to the correct position for each person who you hire.</span></span>

## <a name="mass-hire-project-statuses"></a><span data-ttu-id="6ca8b-125">حالات مشاريع التوظيف الجماعي</span><span class="sxs-lookup"><span data-stu-id="6ca8b-125">Mass hire project statuses</span></span>
<span data-ttu-id="6ca8b-126">قد يشمل مشروع التوظيف الجماعي الحالات التالية:</span><span class="sxs-lookup"><span data-stu-id="6ca8b-126">A mass hire project can have the following statuses.</span></span>
-   <span data-ttu-id="6ca8b-127">تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="6ca8b-127">Created</span></span>
-   <span data-ttu-id="6ca8b-128">المفتوح</span><span class="sxs-lookup"><span data-stu-id="6ca8b-128">Open</span></span>
-   <span data-ttu-id="6ca8b-129">‏‏مغلق</span><span class="sxs-lookup"><span data-stu-id="6ca8b-129">Closed</span></span>

<span data-ttu-id="6ca8b-130">في صفحة **مشروع التوظيف الجماعي**، انقر فوق **فتح مشروع** أو **إغلاق مشروع** لتغيير حالة مشروع التوظيف الجماعي.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-130">On the **Mass hire project** page, click **Open project** or **Close project** to change the status of a mass hire project.</span></span> <span data-ttu-id="6ca8b-131">ويصف الجدول التالي ما يمكن عمله مع المشروع طبقًا لحالته.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-131">The following table describes what you can do with a project according to its status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6ca8b-132">الحالة</span><span class="sxs-lookup"><span data-stu-id="6ca8b-132">Status</span></span></th>
<th><span data-ttu-id="6ca8b-133">الوصف</span><span class="sxs-lookup"><span data-stu-id="6ca8b-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6ca8b-134">تم إنشاؤه</span><span class="sxs-lookup"><span data-stu-id="6ca8b-134">Created</span></span></td>
<td><span data-ttu-id="6ca8b-135">يمكن إنشاء المعلومات وتعديلها، ولكن لا يمكن إنشاء مناصب للمشروع.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-135">You can create and modify information, but cannot create positions for the project.</span></span> <span data-ttu-id="6ca8b-136">وهذه هي الحالة الافتراضية للمشاريع الجديدة.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-136">This is the default status for new projects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ca8b-137">المفتوح</span><span class="sxs-lookup"><span data-stu-id="6ca8b-137">Open</span></span></td>
<td><span data-ttu-id="6ca8b-138">يمكنك تعديل تفاصيل المشروع وإنشاء مناصب لمشروع التوظيف الجماعي وتوظيف أشخاص لشغل المناصب.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-138">You can modify the project details, create positions for the mass hire project, and hire people for the positions.</span></span> <span data-ttu-id="6ca8b-139">وهذه هي حالة المشاريع النشطة.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-139">This is the status for active projects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ca8b-140">‏‏مغلق</span><span class="sxs-lookup"><span data-stu-id="6ca8b-140">Closed</span></span></td>
<td><span data-ttu-id="6ca8b-141">لا يمكنك إضافة مناصب إلى المشروع.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-141">You cannot add positions to the project.</span></span> <span data-ttu-id="6ca8b-142">ولإضافة المناصب إلى مشروع التوظيف الجماعي، افتح المشروع مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-142">To add positions to the mass hire project, open the project again.</span></span> <span data-ttu-id="6ca8b-143">وهذه هي حالة المشاريع المكتملة.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-143">This is the status for completed projects.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6ca8b-144"><strong>ملاحظة </strong></span><span class="sxs-lookup"><span data-stu-id="6ca8b-144"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6ca8b-145">وقبل التمكن من إغلاق مشروع توظيف جماعي، يجب أن تكون حالة كل المناصب في المشروع "تم إنشاؤها" أو "مغلقة".</span><span class="sxs-lookup"><span data-stu-id="6ca8b-145">Before you can close a mass hire project, all positions in the project must have a status of either Created or Closed.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
</tbody>
</table>

 






