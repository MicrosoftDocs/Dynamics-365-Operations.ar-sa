---
title: تفويض عناصر العمل في سير عمل
description: إذا كنت تخطط للتواجد خارج المكتب مما يعني أنك لن تكون متاحًا لاتخاذ الإجراءات اللازمة على عناصر العمل، فيمكنك تفويض عناصر العمل أو إعادة تعيينها إلى مستخدمين آخرين.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: f85a1318822ceaf829134bf2eb3581e350d5bea4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "346239"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="e968d-103">تفويض عناصر العمل في سير عمل</span><span class="sxs-lookup"><span data-stu-id="e968d-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e968d-104">إذا كنت تخطط للتواجد خارج المكتب مما يعني أنك لن تكون متاحًا لاتخاذ الإجراءات اللازمة على عناصر العمل، فيمكنك تفويض عناصر العمل أو إعادة تعيينها إلى مستخدمين آخرين.</span><span class="sxs-lookup"><span data-stu-id="e968d-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="e968d-105">يساعدك هذا الإجراء في تكوين النظام لتفويض عناصر العمل لمستخدم آخر تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="e968d-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="e968d-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="e968d-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="e968d-107">إعداد تفويض تلقائي</span><span class="sxs-lookup"><span data-stu-id="e968d-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="e968d-108">انتقل إلى عام > الإعداد > خيارات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="e968d-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="e968d-109">انقر فوق علامة التبويب "سير العمل".</span><span class="sxs-lookup"><span data-stu-id="e968d-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="e968d-110">تأكد من توسيع المقطع "تفويض".</span><span class="sxs-lookup"><span data-stu-id="e968d-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="e968d-111">لتكوين النظام بحيث يقوم النظام بتفويض عناصر عملك إلى مستخدمين الآخرين بشكل تلقائي، يجب إنشاء قواعد تفويض تحدد متى يتم تفويض أنواع معينة من عناصر العمل.</span><span class="sxs-lookup"><span data-stu-id="e968d-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="e968d-112">اتبع هذه الخطوات لإنشاء قاعدة تفويض.</span><span class="sxs-lookup"><span data-stu-id="e968d-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="e968d-113">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="e968d-113">Click Add.</span></span>
4. <span data-ttu-id="e968d-114">في حقل "النطاق"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="e968d-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="e968d-115">الكل - تفويض كل عناصر العمل المعينة لك.</span><span class="sxs-lookup"><span data-stu-id="e968d-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="e968d-116">وحدة نمطية - تفويض فقط عناصر العمل المرتبطة بنوع سير عمل معين.</span><span class="sxs-lookup"><span data-stu-id="e968d-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="e968d-117">إذا قمت بتحديد هذا الخيار، فيجب تحديد نوع سير العمل في حقل "الاسم".</span><span class="sxs-lookup"><span data-stu-id="e968d-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="e968d-118">سير العمل - تفويض فقط عناصر العمل المرتبطة بنوع سير عمل معين.</span><span class="sxs-lookup"><span data-stu-id="e968d-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="e968d-119">إذا قمت بتحديد هذا الخيار، فيجب تحديد سير العمل في حقل "الاسم".</span><span class="sxs-lookup"><span data-stu-id="e968d-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="e968d-120">في حقل "التفويض"، حدد المستخدم الذي تريد تفويض عناصر العمل إليه.</span><span class="sxs-lookup"><span data-stu-id="e968d-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="e968d-121">استخدم الحقلين "تاريخ/وقت البدء" و"تاريخ/وقت الانتهاء" لتحديد متى تريد تفويض عناصر العمل تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="e968d-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="e968d-122">في الحقل "تاريخ/وقت البدء‬"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="e968d-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="e968d-123">في الحقل "‏‫تاريخ/وقت الانتهاء"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="e968d-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="e968d-124">حدد خانة الاختيار "ممكّن‬" لتنشيط قاعدة التفويض.</span><span class="sxs-lookup"><span data-stu-id="e968d-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="e968d-125">إذا حددت "وحدة نمطية" كنطاق، فيجب عندئذٍ تحديد الوحدة النمطية في حقل "الاسم".</span><span class="sxs-lookup"><span data-stu-id="e968d-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="e968d-126">إذا حددت "سير العمل" كنطاق، فيجب عندئذٍ سير العمل المحدد الذي تريد تفوضه في حقل "الاسم".</span><span class="sxs-lookup"><span data-stu-id="e968d-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="e968d-127">في حقل "التعليقات"، أدخل تعليقًا يوضح سبب تفويض عناصر العمل.</span><span class="sxs-lookup"><span data-stu-id="e968d-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>

