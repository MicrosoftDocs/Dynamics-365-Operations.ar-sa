---
title: إنشاء ومعالجته توافق
description: يشرح هذا الموضوع كيفية تنفيذ إدارة عدم المطابقة استناداً إلى أمر جودة موجود.
author: perlynne
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c4f7e61adf37e74bdb082270b689cf0375ccc7f7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833943"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="b33ac-103">إنشاء ومعالجته توافق</span><span class="sxs-lookup"><span data-stu-id="b33ac-103">Create and process a conformance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b33ac-104">يشرح هذا الموضوع كيفية تنفيذ إدارة عدم المطابقة استناداً إلى أمر جودة موجود.</span><span class="sxs-lookup"><span data-stu-id="b33ac-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="b33ac-105">يمكنك تشغيل هذا التسجيل في شركة العرض التوضيحي USMF ويمكنك استخدام القيم المقترحة.</span><span class="sxs-lookup"><span data-stu-id="b33ac-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="b33ac-106">عادة ما يتم تنفيذ هذا الإجراء بواسطة كاتب جودة.</span><span class="sxs-lookup"><span data-stu-id="b33ac-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="b33ac-107">كشرط مسبق، أكمل الإرشادات في [فحص جودة البضائع‬](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="b33ac-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="b33ac-108">لمعالجة اعتماد عدم المطابقة، يجب أن تكون للمستخدم الذي يقوم بتشغيل تسجيل المهمة قيمة "اسم" معينة بصفحة "المستخدمين".</span><span class="sxs-lookup"><span data-stu-id="b33ac-108">To process the approval of a nonconformance, the user who runs the task recording must have a "Name" value assigned on the Users page.</span></span> <span data-ttu-id="b33ac-109">لاستخدام ملاحظات المستند، يجب أيضًا تنشيط "معالجة المستندات" للمستخدم في خيارات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="b33ac-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="b33ac-110">تحديد أمر جودة</span><span class="sxs-lookup"><span data-stu-id="b33ac-110">Select a quality order</span></span>
1. <span data-ttu-id="b33ac-111">في جزء التنقل، انتقل إلى **الوحدات النمطية >‬ ‏‫إدارة المخزون > المهام الدورية‬ > إدارة الجودة > أوامر الجودة**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="b33ac-112">في القائمة، حدد أمر الجودة الذي تم إنشاؤه في [فحص جودة البضائع](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span><span class="sxs-lookup"><span data-stu-id="b33ac-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="b33ac-113">إنشاء عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="b33ac-113">Create a nonconformance</span></span>
1. <span data-ttu-id="b33ac-114">في جزء الإجراءات، حدد **استعلامات**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-114">On the Action Pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="b33ac-115">حدد **حالات عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="b33ac-116">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-116">Select **New**.</span></span>
4. <span data-ttu-id="b33ac-117">في القائمة المنسدلة لحقل **نوع المشكلة**، حدد المشكلة التي تم العثور عليها أثناء عملية الفحص.</span><span class="sxs-lookup"><span data-stu-id="b33ac-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="b33ac-118">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="b33ac-119">اعتماد/رفض عدم المطابقة</span><span class="sxs-lookup"><span data-stu-id="b33ac-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="b33ac-120">حدد **الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-120">Select **Functions**.</span></span>
2. <span data-ttu-id="b33ac-121">حدد **الموافقة على عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="b33ac-122">على سبيل المثال، قم باعتماد عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="b33ac-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="b33ac-123">يمكن ربط حالات عدم المطابقة الموافق عليها بالعمليات ذات الصلة لتسجيل العمل الذي يتم تنفيذه كجزء من معالجة عدم المطابقة وكما ورد في هذا الموضوع، معالجة التعامل مع التصحيح.</span><span class="sxs-lookup"><span data-stu-id="b33ac-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="b33ac-124">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="b33ac-125">إنشاء إجراء تصحيح</span><span class="sxs-lookup"><span data-stu-id="b33ac-125">Create a correction action</span></span>
1. <span data-ttu-id="b33ac-126">حدد **التصحيحات**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="b33ac-127">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-127">Select **New**.</span></span>
3. <span data-ttu-id="b33ac-128">في الحقل **رقم الموظف‬** في الصف الجديد، حدد السجل المطلوب من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="b33ac-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="b33ac-129">انقر فوق **تحديد**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-129">Click **Select**.</span></span>
5. <span data-ttu-id="b33ac-130">حدد **إرفاق**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-130">Select **Attach**.</span></span> <span data-ttu-id="b33ac-131">قم بإنشاء ملاحظة حول التصحيح.</span><span class="sxs-lookup"><span data-stu-id="b33ac-131">Create a note about the correction.</span></span> <span data-ttu-id="b33ac-132">على سبيل المثال، يتمثل الإجراء في الاتصال بالمورد لمناقشة حالة عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="b33ac-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="b33ac-133">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-133">Select **New**.</span></span>
7. <span data-ttu-id="b33ac-134">حدد **ملاحظة**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-134">Select **Note**.</span></span> <span data-ttu-id="b33ac-135">تبعًا لإعداد التقرير، يمكن طباعة أنواع مختلفة من المستندات على التقارير المتعلقة بإدارة عدم المطابقة.</span><span class="sxs-lookup"><span data-stu-id="b33ac-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="b33ac-136">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="b33ac-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="b33ac-137">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b33ac-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="b33ac-138">الاحتفاظ بإجراء التصحيح</span><span class="sxs-lookup"><span data-stu-id="b33ac-138">Maintain a correction</span></span>
1. <span data-ttu-id="b33ac-139">حدد **وضع علامة كمكتمل**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="b33ac-140">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-140">Select **OK**.</span></span>
3. <span data-ttu-id="b33ac-141">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b33ac-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="b33ac-142">إغلاق حالة عدم مطابقة</span><span class="sxs-lookup"><span data-stu-id="b33ac-142">Close a nonconformance</span></span>
1. <span data-ttu-id="b33ac-143">حدد **الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-143">Select **Functions**.</span></span>
2. <span data-ttu-id="b33ac-144">حدد **إغلاق عدم المطابقة**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="b33ac-145">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="b33ac-145">Select **Yes**.</span></span>
4. <span data-ttu-id="b33ac-146">قم بإغلاق الصفحات.</span><span class="sxs-lookup"><span data-stu-id="b33ac-146">Close the pages.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]