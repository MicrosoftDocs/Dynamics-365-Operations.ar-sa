---
title: إنشاء ومعالجته توافق
description: يشرح هذا الموضوع كيفية تنفيذ إدارة عدم المطابقة استناداً إلى أمر جودة موجود.
author: perlynne
manager: AnnBe
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d012af1924e9eedee41f46de6c253d009cb52d2
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145699"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="ad59f-103">إنشاء ومعالجته توافق</span><span class="sxs-lookup"><span data-stu-id="ad59f-103">Create and process a conformance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad59f-104">يشرح هذا الموضوع كيفية تنفيذ إدارة عدم المطابقة استناداً إلى أمر جودة موجود.</span><span class="sxs-lookup"><span data-stu-id="ad59f-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="ad59f-105">يمكنك تشغيل هذا التسجيل في شركة العرض التوضيحي USMF ويمكنك استخدام القيم المقترحة.</span><span class="sxs-lookup"><span data-stu-id="ad59f-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="ad59f-106">عادة ما يتم تنفيذ هذا الإجراء بواسطة كاتب جودة.</span><span class="sxs-lookup"><span data-stu-id="ad59f-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="ad59f-107">كشرط مسبق، أكمل الإرشادات في [فحص جودة البضائع‬](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="ad59f-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="ad59f-108">لمعالجة اعتماد عدم المطابقة، يجب أن تكون للمستخدم الذي يقوم بتشغيل تسجيل المهمة قيمة "اسم" معينة بصفحة "المستخدمين".</span><span class="sxs-lookup"><span data-stu-id="ad59f-108">To process the approval of a nonconformance, the user who runs the task recording must have a "Name" value assigned on the Users page.</span></span> <span data-ttu-id="ad59f-109">لاستخدام ملاحظات المستند، يجب أيضًا تنشيط "معالجة المستندات" للمستخدم في خيارات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="ad59f-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="ad59f-110">تحديد أمر جودة</span><span class="sxs-lookup"><span data-stu-id="ad59f-110">Select a quality order</span></span>
1. <span data-ttu-id="ad59f-111">في جزء التنقل، انتقل إلى **الوحدات النمطية >‬ ‏‫إدارة المخزون > المهام الدورية‬ > إدارة الجودة > أوامر الجودة**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="ad59f-112">في القائمة، حدد أمر الجودة الذي تم إنشاؤه في [فحص جودة البضائع](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="ad59f-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="ad59f-113">إنشاء عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="ad59f-113">Create a nonconformance</span></span>
1. <span data-ttu-id="ad59f-114">في جزء الإجراءات، حدد **استعلامات**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-114">In the action pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="ad59f-115">حدد **حالات عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="ad59f-116">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-116">Select **New**.</span></span>
4. <span data-ttu-id="ad59f-117">في القائمة المنسدلة لحقل **نوع المشكلة**، حدد المشكلة التي تم العثور عليها أثناء عملية الفحص.</span><span class="sxs-lookup"><span data-stu-id="ad59f-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="ad59f-118">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="ad59f-119">اعتماد/رفض عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="ad59f-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="ad59f-120">حدد **الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-120">Select **Functions**.</span></span>
2. <span data-ttu-id="ad59f-121">حدد **الموافقة على عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="ad59f-122">على سبيل المثال، قم باعتماد عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="ad59f-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="ad59f-123">يمكن ربط حالات عدم المطابقة الموافق عليها بالعمليات ذات الصلة لتسجيل العمل الذي يتم تنفيذه كجزء من معالجة عدم المطابقة وكما ورد في هذا الموضوع، معالجة التعامل مع التصحيح.</span><span class="sxs-lookup"><span data-stu-id="ad59f-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="ad59f-124">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="ad59f-125">إنشاء إجراء تصحيح</span><span class="sxs-lookup"><span data-stu-id="ad59f-125">Create a correction action</span></span>
1. <span data-ttu-id="ad59f-126">حدد **التصحيحات**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="ad59f-127">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-127">Select **New**.</span></span>
3. <span data-ttu-id="ad59f-128">في الحقل **رقم الموظف‬** في الصف الجديد، حدد السجل المطلوب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="ad59f-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="ad59f-129">انقر فوق **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-129">Click **Select**.</span></span>
5. <span data-ttu-id="ad59f-130">حدد **إرفاق**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-130">Select **Attach**.</span></span> <span data-ttu-id="ad59f-131">قم بإنشاء ملاحظة حول التصحيح.</span><span class="sxs-lookup"><span data-stu-id="ad59f-131">Create a note about the correction.</span></span> <span data-ttu-id="ad59f-132">على سبيل المثال، يتمثل الإجراء في الاتصال بالمورد لمناقشة حالة عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="ad59f-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="ad59f-133">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-133">Select **New**.</span></span>
7. <span data-ttu-id="ad59f-134">حدد **ملاحظة**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-134">Select **Note**.</span></span> <span data-ttu-id="ad59f-135">تبعًا لإعداد التقرير، يمكن طباعة أنواع مختلفة من المستندات على التقارير المتعلقة بإدارة عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="ad59f-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="ad59f-136">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="ad59f-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="ad59f-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ad59f-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="ad59f-138">الاحتفاظ بإجراء التصحيح</span><span class="sxs-lookup"><span data-stu-id="ad59f-138">Maintain a correction</span></span>
1. <span data-ttu-id="ad59f-139">حدد **وضع علامة كمكتمل**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="ad59f-140">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-140">Select **OK**.</span></span>
3. <span data-ttu-id="ad59f-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ad59f-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="ad59f-142">إغلاق حالة عدم مطابقة</span><span class="sxs-lookup"><span data-stu-id="ad59f-142">Close a nonconformance</span></span>
1. <span data-ttu-id="ad59f-143">حدد **الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-143">Select **Functions**.</span></span>
2. <span data-ttu-id="ad59f-144">حدد **إغلاق عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="ad59f-145">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="ad59f-145">Select **Yes**.</span></span>
4. <span data-ttu-id="ad59f-146">قم بإغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="ad59f-146">Close the pages.</span></span>
