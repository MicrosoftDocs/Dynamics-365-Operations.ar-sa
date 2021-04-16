---
title: تفويض عناصر العمل في سير عمل
description: إذا كنت تخطط للتواجد خارج المكتب مما يعني أنك لن تكون متاحًا لاتخاذ الإجراءات اللازمة على عناصر العمل، فيمكنك تفويض عناصر العمل أو إعادة تعيينها إلى مستخدمين آخرين.
author: ChrisGarty
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed21f6d32cdcf74eb153daba32c20b7cef94d4e4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747359"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="42cfa-103">تفويض عناصر العمل في سير عمل</span><span class="sxs-lookup"><span data-stu-id="42cfa-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="42cfa-104">تفويض عنصر عمل يدويًا</span><span class="sxs-lookup"><span data-stu-id="42cfa-104">Manually delegate a work item</span></span>

<span data-ttu-id="42cfa-105">تفويض عنصر عمل فردي، حدد الخيار **تفويض** في قائمة **سير العمل**، ثم أدخل المستخدم الذي تريد تفويضه لسير العمل مع إضافة تعليق.</span><span class="sxs-lookup"><span data-stu-id="42cfa-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="42cfa-106">سيؤدي ذلك إلى إعادة تعيين عنصر العمل إلى هذا المستخدم لتمكينه من إتمامه.</span><span class="sxs-lookup"><span data-stu-id="42cfa-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="42cfa-107">تفويض عدة أصناف عمل يدويًا</span><span class="sxs-lookup"><span data-stu-id="42cfa-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="42cfa-108">يمكن تفويض عدة أصناف عمل معا من صفحة **أصناف العمل المعينة إلىّ**.</span><span class="sxs-lookup"><span data-stu-id="42cfa-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="42cfa-109">تعتبر أنواع سير العمل التالية مؤهلة للتفويض الجماعي: سير عمل الموافقة على اتفاقية الشراء وسير عمل أمر الشراء ومراجعة طلب الشراء وسير عمل فاتورة المورد.</span><span class="sxs-lookup"><span data-stu-id="42cfa-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="42cfa-110">يتم تعطيل ميزة **تفويض أصناف العمل المتعددة** بشكل افتراضي ويمكن تمكينها في **مساحات العمل > إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="42cfa-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="42cfa-111">اتصل بمسؤول النظام للمساعدة في تمكين هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="42cfa-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="42cfa-112">انتقل إلى **عام > عام >أصناف العمل > أصناف العمل المعينة إليّ**.</span><span class="sxs-lookup"><span data-stu-id="42cfa-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="42cfa-113">حدد أصناف العمل التي سيتم تفويضها.</span><span class="sxs-lookup"><span data-stu-id="42cfa-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="42cfa-114">انقر فوق قائمة **تفويض أصناف العمل**.</span><span class="sxs-lookup"><span data-stu-id="42cfa-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="42cfa-115">في حقل **المستخدم**، حدد المستخدم الذي تريد تفويض أصناف العمل إليه.</span><span class="sxs-lookup"><span data-stu-id="42cfa-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="42cfa-116">في حقل **التعليق**، أدخل تعليقًا يوضح سبب تفويض أصناف العمل.</span><span class="sxs-lookup"><span data-stu-id="42cfa-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="42cfa-117">انقر فوق زر **تفويض أصناف العمل** لإكمال تفويض صنف العمل.</span><span class="sxs-lookup"><span data-stu-id="42cfa-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="42cfa-118">تفويض عناصر العمل تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="42cfa-118">Automatically delegate work items</span></span>

<span data-ttu-id="42cfa-119">إذا كنت تخطط للبقاء خارج المكتب أو بشكل آخر غير متوفر للعمل على عناصر عمل لفترة من الوقت، فيمكنك تفويض عناصر العمل الجديدة بشكل تلقائي لمستخدمين آخرين باستخدام صفحة **خيارات المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="42cfa-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="42cfa-120">إعداد تفويض تلقائي</span><span class="sxs-lookup"><span data-stu-id="42cfa-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="42cfa-121">انتقل إلى **عام > الإعداد > خيارات المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="42cfa-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="42cfa-122">انقر فوق علامة‏‎ التبويب **سير العمل**. تأكد من توسيع قسم "التفويض".</span><span class="sxs-lookup"><span data-stu-id="42cfa-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="42cfa-123">لتكوين النظام بحيث يقوم النظام بتفويض عناصر عملك إلى مستخدمين الآخرين بشكل تلقائي، يجب إنشاء قواعد تفويض تحدد متى يتم تفويض أنواع معينة من عناصر العمل.</span><span class="sxs-lookup"><span data-stu-id="42cfa-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="42cfa-124">اتبع هذه الخطوات لإنشاء قاعدة تفويض.</span><span class="sxs-lookup"><span data-stu-id="42cfa-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="42cfa-125">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="42cfa-125">Click **Add**.</span></span>
4. <span data-ttu-id="42cfa-126">في حقل **النطاق**، حدد خيارًا:</span><span class="sxs-lookup"><span data-stu-id="42cfa-126">In the **Scope** field, select an option:</span></span>
    - <span data-ttu-id="42cfa-127">الكل - تفويض كل عناصر العمل المعينة لك.</span><span class="sxs-lookup"><span data-stu-id="42cfa-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="42cfa-128">وحدة نمطية - تفويض فقط عناصر العمل المرتبطة بنوع سير عمل معين.</span><span class="sxs-lookup"><span data-stu-id="42cfa-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="42cfa-129">عند تحديد هذا الخيار، يجب تحديد نوع سير العمل في حقل **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="42cfa-129">If you select this option, you must select the type of workflow in the **Name** field.</span></span>
    - <span data-ttu-id="42cfa-130">سير العمل - تفويض فقط عناصر العمل المرتبطة بنوع سير عمل معين.</span><span class="sxs-lookup"><span data-stu-id="42cfa-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="42cfa-131">عند بتحديد هذا الخيار، يجب تحديد سير العمل في حقل **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="42cfa-131">If you select this option, you must select the workflow in the **Name** field.</span></span>  
5. <span data-ttu-id="42cfa-132">في حقل **الاسم**:</span><span class="sxs-lookup"><span data-stu-id="42cfa-132">In the **Name** field:</span></span>
    - <span data-ttu-id="42cfa-133">بالنسبة لنطاق **الوحدة النمطية**، حدد الوحدة النمطية الهدف.</span><span class="sxs-lookup"><span data-stu-id="42cfa-133">For **Module** scope, select the target module.</span></span>
    - <span data-ttu-id="42cfa-134">بالنسبة لنطاق **سير العمل**، حدد سير العمل الهدف.</span><span class="sxs-lookup"><span data-stu-id="42cfa-134">For **Workflow** scope, select the target workflow.</span></span>
6. <span data-ttu-id="42cfa-135">في حقل **التفويض**، حدد المستخدم الذي تريد تفويض عناصر العمل إليه.</span><span class="sxs-lookup"><span data-stu-id="42cfa-135">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="42cfa-136">استخدم الحقلين **تاريخ/وقت البدء** و **تاريخ/وقت الانتهاء** لتحديد متى تريد تفويض عناصر العمل تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="42cfa-136">Use the **Start date/time** and **End date/time** fields to specify when you want the work items to be automatically delegated.</span></span>  
7. <span data-ttu-id="42cfa-137">في الحقل **تاريخ/وقت البدء**، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="42cfa-137">In the **Start date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="42cfa-138">في الحقل **‏‫تاريخ/وقت الانتهاء**، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="42cfa-138">In the **End date/time** field, enter a date and time.</span></span>
9. <span data-ttu-id="42cfa-139">حدد خانة الاختيار **ممكّن‬** لتنشيط قاعدة التفويض.</span><span class="sxs-lookup"><span data-stu-id="42cfa-139">Select the **Enabled** check box to activate the delegation rule.</span></span> 
10. <span data-ttu-id="42cfa-140">في حقل **التعليق**، أدخل تعليقًا يوضح سبب تفويض أصناف العمل.</span><span class="sxs-lookup"><span data-stu-id="42cfa-140">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]