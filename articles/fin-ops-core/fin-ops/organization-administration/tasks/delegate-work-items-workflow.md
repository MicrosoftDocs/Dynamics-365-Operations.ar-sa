---
title: تفويض عناصر العمل في سير عمل
description: إذا كنت تخطط للتواجد خارج المكتب مما يعني أنك لن تكون متاحًا لاتخاذ الإجراءات اللازمة على عناصر العمل، فيمكنك تفويض عناصر العمل أو إعادة تعيينها إلى مستخدمين آخرين.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aceafbe8dfcdac2ac7b97a4f77a9a30599c60c51
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140572"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="63646-103">تفويض عناصر العمل في سير عمل</span><span class="sxs-lookup"><span data-stu-id="63646-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="63646-104">تفويض عنصر عمل يدويًا</span><span class="sxs-lookup"><span data-stu-id="63646-104">Manually delegate a work item</span></span>

<span data-ttu-id="63646-105">تفويض عنصر عمل فردي، حدد الخيار **تفويض** في قائمة **سير العمل**، ثم أدخل المستخدم الذي تريد تفويضه لسير العمل مع إضافة تعليق.</span><span class="sxs-lookup"><span data-stu-id="63646-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="63646-106">سيؤدي ذلك إلى إعادة تعيين عنصر العمل إلى هذا المستخدم لتمكينه من إتمامه.</span><span class="sxs-lookup"><span data-stu-id="63646-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="63646-107">تفويض عناصر العمل تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="63646-107">Automatically delegate work items</span></span>

<span data-ttu-id="63646-108">إذا كنت تخطط للبقاء خارج المكتب أو بشكل آخر غير متوفر للعمل على عناصر عمل لفترة من الوقت، فيمكنك تفويض عناصر العمل الجديدة بشكل تلقائي لمستخدمين آخرين باستخدام صفحة **خيارات المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="63646-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="63646-109">إعداد تفويض تلقائي</span><span class="sxs-lookup"><span data-stu-id="63646-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="63646-110">انتقل إلى **عام > الإعداد > خيارات المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="63646-110">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="63646-111">انقر فوق علامة‏‎ التبويب **سير العمل**. تأكد من توسيع قسم "التفويض".</span><span class="sxs-lookup"><span data-stu-id="63646-111">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="63646-112">لتكوين النظام بحيث يقوم النظام بتفويض عناصر عملك إلى مستخدمين الآخرين بشكل تلقائي، يجب إنشاء قواعد تفويض تحدد متى يتم تفويض أنواع معينة من عناصر العمل.</span><span class="sxs-lookup"><span data-stu-id="63646-112">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="63646-113">اتبع هذه الخطوات لإنشاء قاعدة تفويض.</span><span class="sxs-lookup"><span data-stu-id="63646-113">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="63646-114">انقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="63646-114">Click **Add**.</span></span>
4. <span data-ttu-id="63646-115">في حقل **النطاق**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="63646-115">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="63646-116">الكل - تفويض كل عناصر العمل المعينة لك.</span><span class="sxs-lookup"><span data-stu-id="63646-116">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="63646-117">وحدة نمطية - تفويض فقط عناصر العمل المرتبطة بنوع سير عمل معين.</span><span class="sxs-lookup"><span data-stu-id="63646-117">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="63646-118">إذا قمت بتحديد هذا الخيار، فيجب تحديد نوع سير العمل في حقل "الاسم".</span><span class="sxs-lookup"><span data-stu-id="63646-118">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="63646-119">سير العمل - تفويض فقط عناصر العمل المرتبطة بنوع سير عمل معين.</span><span class="sxs-lookup"><span data-stu-id="63646-119">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="63646-120">إذا قمت بتحديد هذا الخيار، فيجب تحديد سير العمل في حقل "الاسم".</span><span class="sxs-lookup"><span data-stu-id="63646-120">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="63646-121">في حقل **التفويض**، حدد المستخدم الذي تريد تفويض عناصر العمل إليه.</span><span class="sxs-lookup"><span data-stu-id="63646-121">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="63646-122">استخدم الحقلين "تاريخ/وقت البدء" و"تاريخ/وقت الانتهاء" لتحديد متى تريد تفويض عناصر العمل تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="63646-122">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="63646-123">في الحقل **تاريخ/وقت البدء**، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="63646-123">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="63646-124">في الحقل **‏‫تاريخ/وقت الانتهاء**، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="63646-124">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="63646-125">حدد خانة الاختيار **ممكّن‬** لتنشيط قاعدة التفويض.</span><span class="sxs-lookup"><span data-stu-id="63646-125">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="63646-126">إذا حددت **وحدة نمطية** كنطاق، فيجب عندئذٍ تحديد الوحدة النمطية في حقل "الاسم".</span><span class="sxs-lookup"><span data-stu-id="63646-126">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="63646-127">إذا حددت **سير العمل** كنطاق، فيجب عندئذٍ سير العمل المحدد الذي تريد تفوضه في حقل "الاسم".</span><span class="sxs-lookup"><span data-stu-id="63646-127">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="63646-128">في حقل **التعليق**، أدخل تعليقًا يوضح سبب تفويض عناصر العمل.</span><span class="sxs-lookup"><span data-stu-id="63646-128">In the **Comment** field, enter a comment that explains why you are delegating the work items.</span></span>

