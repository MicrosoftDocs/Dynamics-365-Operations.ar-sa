---
title: دعم لوحة تحويل كانبان للماسحات الضوئية للرمز الشريطي
description: تدعم لوحة تحويل كانبان‬ إدخال الماسح الضوئي من ماسح ضوئي للرمز الشريطي لعنصر واجهة مستخدم لتحديد وظيفة كانبان وبدء تنفيذها وإكمالها وإفراغها.
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e63a33af63144b78d0c375022b9802e11c255598
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "319444"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="9ffce-103">دعم لوحة تحويل كانبان للماسحات الضوئية للرمز الشريطي</span><span class="sxs-lookup"><span data-stu-id="9ffce-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ffce-104">تدعم لوحة تحويل كانبان‬ إدخال الماسح الضوئي من ماسح ضوئي للرمز الشريطي لعنصر واجهة مستخدم لتحديد وظيفة كانبان وبدء تنفيذها وإكمالها وإفراغها.</span><span class="sxs-lookup"><span data-stu-id="9ffce-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="9ffce-105">أوضاع التسجيل</span><span class="sxs-lookup"><span data-stu-id="9ffce-105">Registration modes</span></span>
------------------

<span data-ttu-id="9ffce-106">في علامة التبويب السريع **تسجيل الماسح الضوئي**، يمكنك تحديد وضع التسجيل، التي تتحكم في الإجراء عند قيامك بمسح رقم بطاقة كانبان ضوئيًا أو بكتابة الرقم في حقل رقم بطاقة كانبان يدوياً.</span><span class="sxs-lookup"><span data-stu-id="9ffce-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="9ffce-107">تعيين وضع التسجيل</span><span class="sxs-lookup"><span data-stu-id="9ffce-107">Set registration mode</span></span> | <span data-ttu-id="9ffce-108">الوصف</span><span class="sxs-lookup"><span data-stu-id="9ffce-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ffce-109">بداية</span><span class="sxs-lookup"><span data-stu-id="9ffce-109">Start</span></span>                 | <span data-ttu-id="9ffce-110">تسجيل وظيفة تحويل كانبان في حالة قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="9ffce-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="9ffce-111">إكمال</span><span class="sxs-lookup"><span data-stu-id="9ffce-111">Complete</span></span>              | <span data-ttu-id="9ffce-112">تسجيل وظيفة تحويل كانبان في حالة مكتملة.</span><span class="sxs-lookup"><span data-stu-id="9ffce-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="9ffce-113">فارغ</span><span class="sxs-lookup"><span data-stu-id="9ffce-113">Empty</span></span>                 | <span data-ttu-id="9ffce-114">تسجيل وحدة معالجة المواد المشار إليها ببطاقة كانبان على أنها وحدة فارغة.</span><span class="sxs-lookup"><span data-stu-id="9ffce-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="9ffce-115">تحديد</span><span class="sxs-lookup"><span data-stu-id="9ffce-115">Select</span></span>                | <span data-ttu-id="9ffce-116">تسجيل رقم بطاقة كانبان وتحديد الوظيفة المشار إليها تلقائيًا في قائمة كانبان.</span><span class="sxs-lookup"><span data-stu-id="9ffce-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<span data-ttu-id="9ffce-117">تحديد وضع التسجيل</span><span class="sxs-lookup"><span data-stu-id="9ffce-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="9ffce-118">عند استخدام قارئ الرمز الشريطي لتحديد وظيفة، يتغير وضع عرض تغييرات لوحة كانبان.</span><span class="sxs-lookup"><span data-stu-id="9ffce-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span><span data-ttu-id="9ffce-119"> في هذا الوضع، تنطبق الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="9ffce-119"> In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="9ffce-120">يتم عرض وظيفة كانبان التي تم مسحها ضوئياً فقط.</span><span class="sxs-lookup"><span data-stu-id="9ffce-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="9ffce-121">يتم عرض تفاصيل الوظيفة المحددة في علامة التبويب السريع **تفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="9ffce-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="9ffce-122">تعرض علامة التبويب السريع **الرسائل** الرسائل للوظيفة المحددة فقط.</span><span class="sxs-lookup"><span data-stu-id="9ffce-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="9ffce-123">يمكنك تغيير حالة الوظيفة باستخدام الدالات المتوفرة في "جزء الإجراءات".</span><span class="sxs-lookup"><span data-stu-id="9ffce-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="9ffce-124">وتواصل لوحة تحويل كانبان عرض وظيفة واحدة فقط خلال هذه الفترة.</span><span class="sxs-lookup"><span data-stu-id="9ffce-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="9ffce-125">ويمكنك تحديث المعلومات الموجودة في قائمة الوظائف يدوياً بالنقر فوق **تحديث** ‏(Shift+F5) في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="9ffce-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="9ffce-126">وبعد تحديث المعلومات، يتم عرض النتائج الكاملة لعامل تصفية الوظائف مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="9ffce-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="9ffce-127">حالة الوظائف والإجراءات الممكنة</span><span class="sxs-lookup"><span data-stu-id="9ffce-127">Job status and possible actions</span></span>
<span data-ttu-id="9ffce-128">حالة الوظيفة المحددة وحالة أي وظائف مثبتة لوظائف كانبان الحدث، تحديد ما إذا كان يمكنك معالجة الوظيفة بشكل أكبر.</span><span class="sxs-lookup"><span data-stu-id="9ffce-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="9ffce-129">يعرض الجدول التالي معلومات حول هذه الحالات والمهام:</span><span class="sxs-lookup"><span data-stu-id="9ffce-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="9ffce-130">الحالات التي تتوفر للوظائف أو لوحدات المعالجة التي يتم يُشار إليها بالوظائف.</span><span class="sxs-lookup"><span data-stu-id="9ffce-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="9ffce-131">كل مهمة يمكنك تنفيذها للوظيفة.</span><span class="sxs-lookup"><span data-stu-id="9ffce-131">Each task that you can perform for the job.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9ffce-132">نوع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="9ffce-132">Job type</span></span></th>
<th><span data-ttu-id="9ffce-133">حالة الوظائف أو حالة وحدة المعالجة</span><span class="sxs-lookup"><span data-stu-id="9ffce-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="9ffce-134">تحديث قائمة الانتقاء</span><span class="sxs-lookup"><span data-stu-id="9ffce-134">Update picking list</span></span></th>
<th><span data-ttu-id="9ffce-135">بداية</span><span class="sxs-lookup"><span data-stu-id="9ffce-135">Start</span></span></th>
<th><span data-ttu-id="9ffce-136">تحديث التسجيل</span><span class="sxs-lookup"><span data-stu-id="9ffce-136">Update registration</span></span></th>
<th><span data-ttu-id="9ffce-137">إكمال</span><span class="sxs-lookup"><span data-stu-id="9ffce-137">Complete</span></span></th>
<th><span data-ttu-id="9ffce-138">فارغ</span><span class="sxs-lookup"><span data-stu-id="9ffce-138">Empty</span></span></th>
<th><span data-ttu-id="9ffce-139">إنشاء كانبان للأحداث</span><span class="sxs-lookup"><span data-stu-id="9ffce-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ffce-140">تحويل</span><span class="sxs-lookup"><span data-stu-id="9ffce-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="9ffce-141">غير مخطط</span><span class="sxs-lookup"><span data-stu-id="9ffce-141">Not planned</span></span></li>
<li><span data-ttu-id="9ffce-142">لا توجد أي وظائف مثبتة أو الوظائف المثبتة مكتملة</span><span class="sxs-lookup"><span data-stu-id="9ffce-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="9ffce-143">نعم</span><span class="sxs-lookup"><span data-stu-id="9ffce-143">Yes</span></span></td>
<td><span data-ttu-id="9ffce-144">نعم</span><span class="sxs-lookup"><span data-stu-id="9ffce-144">Yes</span></span></td>
<td><span data-ttu-id="9ffce-145">نعم</span><span class="sxs-lookup"><span data-stu-id="9ffce-145">Yes</span></span></td>
<td><span data-ttu-id="9ffce-146">نعم</span><span class="sxs-lookup"><span data-stu-id="9ffce-146">Yes</span></span></td>
<td><span data-ttu-id="9ffce-147">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-147">No</span></span></td>
<td><span data-ttu-id="9ffce-148">نعم</span><span class="sxs-lookup"><span data-stu-id="9ffce-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ffce-149">تحويل</span><span class="sxs-lookup"><span data-stu-id="9ffce-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="9ffce-150">غير مخطط</span><span class="sxs-lookup"><span data-stu-id="9ffce-150">Not planned</span></span></li>
<li><span data-ttu-id="9ffce-151">الوظيفة المثبتة لم تكتمل</span><span class="sxs-lookup"><span data-stu-id="9ffce-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="9ffce-152">نعم</span><span class="sxs-lookup"><span data-stu-id="9ffce-152">Yes</span></span></td>
<td><span data-ttu-id="9ffce-153">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-153">No</span></span></td>
<td><span data-ttu-id="9ffce-154">نعم</span><span class="sxs-lookup"><span data-stu-id="9ffce-154">Yes</span></span></td>
<td><span data-ttu-id="9ffce-155">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-155">No</span></span></td>
<td><span data-ttu-id="9ffce-156">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-156">No</span></span></td>
<td><span data-ttu-id="9ffce-157">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ffce-158">تحويل</span><span class="sxs-lookup"><span data-stu-id="9ffce-158">Transfer</span></span></td>
<td><span data-ttu-id="9ffce-159">قيد التقدم</span><span class="sxs-lookup"><span data-stu-id="9ffce-159">In progress</span></span></td>
<td><span data-ttu-id="9ffce-160">نعم</span><span class="sxs-lookup"><span data-stu-id="9ffce-160">Yes</span></span></td>
<td><span data-ttu-id="9ffce-161">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-161">No</span></span></td>
<td><span data-ttu-id="9ffce-162">نعم</span><span class="sxs-lookup"><span data-stu-id="9ffce-162">Yes</span></span></td>
<td><span data-ttu-id="9ffce-163">نعم</span><span class="sxs-lookup"><span data-stu-id="9ffce-163">Yes</span></span></td>
<td><span data-ttu-id="9ffce-164">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-164">No</span></span></td>
<td><span data-ttu-id="9ffce-165">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ffce-166">تحويل</span><span class="sxs-lookup"><span data-stu-id="9ffce-166">Transfer</span></span></td>
<td><span data-ttu-id="9ffce-167">‏‏‏‏مكتمل</span><span class="sxs-lookup"><span data-stu-id="9ffce-167">Completed</span></span></td>
<td><span data-ttu-id="9ffce-168">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-168">No</span></span></td>
<td><span data-ttu-id="9ffce-169">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-169">No</span></span></td>
<td><span data-ttu-id="9ffce-170">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-170">No</span></span></td>
<td><span data-ttu-id="9ffce-171">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-171">No</span></span></td>
<td><span data-ttu-id="9ffce-172">نعم</span><span class="sxs-lookup"><span data-stu-id="9ffce-172">Yes</span></span></td>
<td><span data-ttu-id="9ffce-173">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ffce-174">التحويل أو العملية</span><span class="sxs-lookup"><span data-stu-id="9ffce-174">Transfer or process</span></span></td>
<td><span data-ttu-id="9ffce-175">فارغ</span><span class="sxs-lookup"><span data-stu-id="9ffce-175">Empty</span></span></td>
<td><span data-ttu-id="9ffce-176">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-176">No</span></span></td>
<td><span data-ttu-id="9ffce-177">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-177">No</span></span></td>
<td><span data-ttu-id="9ffce-178">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-178">No</span></span></td>
<td><span data-ttu-id="9ffce-179">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-179">No</span></span></td>
<td><span data-ttu-id="9ffce-180">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-180">No</span></span></td>
<td><span data-ttu-id="9ffce-181">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ffce-182">التحويل أو العملية</span><span class="sxs-lookup"><span data-stu-id="9ffce-182">Transfer or process</span></span></td>
<td><span data-ttu-id="9ffce-183">بطاقة كانبان غير موجودة</span><span class="sxs-lookup"><span data-stu-id="9ffce-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="9ffce-184">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-184">No</span></span></td>
<td><span data-ttu-id="9ffce-185">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-185">No</span></span></td>
<td><span data-ttu-id="9ffce-186">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-186">No</span></span></td>
<td><span data-ttu-id="9ffce-187">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-187">No</span></span></td>
<td><span data-ttu-id="9ffce-188">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-188">No</span></span></td>
<td><span data-ttu-id="9ffce-189">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ffce-190">التحويل أو العملية</span><span class="sxs-lookup"><span data-stu-id="9ffce-190">Transfer or process</span></span></td>
<td><span data-ttu-id="9ffce-191">تم العثور على بطاقة كانبان، ولكن لم يتم تعيينها إلى كانبان</span><span class="sxs-lookup"><span data-stu-id="9ffce-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="9ffce-192">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-192">No</span></span></td>
<td><span data-ttu-id="9ffce-193">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-193">No</span></span></td>
<td><span data-ttu-id="9ffce-194">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-194">No</span></span></td>
<td><span data-ttu-id="9ffce-195">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-195">No</span></span></td>
<td><span data-ttu-id="9ffce-196">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-196">No</span></span></td>
<td><span data-ttu-id="9ffce-197">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ffce-198">عملية</span><span class="sxs-lookup"><span data-stu-id="9ffce-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="9ffce-199">غير مخطط</span><span class="sxs-lookup"><span data-stu-id="9ffce-199">Not planned</span></span></li>
<li><span data-ttu-id="9ffce-200">مُعد</span><span class="sxs-lookup"><span data-stu-id="9ffce-200">Prepared</span></span></li>
<li><span data-ttu-id="9ffce-201">قيد التقدم</span><span class="sxs-lookup"><span data-stu-id="9ffce-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="9ffce-202">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-202">No</span></span></td>
<td><span data-ttu-id="9ffce-203">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-203">No</span></span></td>
<td><span data-ttu-id="9ffce-204">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-204">No</span></span></td>
<td><span data-ttu-id="9ffce-205">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-205">No</span></span></td>
<td><span data-ttu-id="9ffce-206">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-206">No</span></span></td>
<td><span data-ttu-id="9ffce-207">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ffce-208">عملية</span><span class="sxs-lookup"><span data-stu-id="9ffce-208">Process</span></span></td>
<td><span data-ttu-id="9ffce-209">‏‏‏‏مكتمل</span><span class="sxs-lookup"><span data-stu-id="9ffce-209">Completed</span></span></td>
<td><span data-ttu-id="9ffce-210">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-210">No</span></span></td>
<td><span data-ttu-id="9ffce-211">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-211">No</span></span></td>
<td><span data-ttu-id="9ffce-212">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-212">No</span></span></td>
<td><span data-ttu-id="9ffce-213">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-213">No</span></span></td>
<td><span data-ttu-id="9ffce-214">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-214">No</span></span></td>
<td><span data-ttu-id="9ffce-215">لا</span><span class="sxs-lookup"><span data-stu-id="9ffce-215">No</span></span></td>
</tr>
</tbody>
</table>





