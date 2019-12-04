---
title: تعيين مستخدمين إلى أدوار أمان
description: للوصول إلى تطبيقات Finance and Operations، يجب تعيين المستخدمين إلى أدوار الأمان.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4f4ef4535de9e371829c2d86d4fdc1400510c7b
ms.sourcegitcommit: 6aa74f66f1abd3a7977050a5339b0b17e62ff053
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/15/2019
ms.locfileid: "2807986"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="c0d58-103">تعيين مستخدمين إلى أدوار أمان</span><span class="sxs-lookup"><span data-stu-id="c0d58-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0d58-104">لاستخدام أي شيء آخر غير القدرات الشائعة، يجب تعيين أدوار أمان إلى المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="c0d58-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="c0d58-105">يوضح هذا الإجراء كيف يمكن لمسؤولي النظام تعيين مستخدمين إلى أدوار بشكل تلقائي، استنادًا إلى بيانات العمل.</span><span class="sxs-lookup"><span data-stu-id="c0d58-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="c0d58-106">قم بتعيين مستخدمين إلى أدوار تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="c0d58-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="c0d58-107">انتقل إلى **جزء التنقل > الوحدات > إدارة النظام > الأمان > تعيين مستخدمين للأدوار**.</span><span class="sxs-lookup"><span data-stu-id="c0d58-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="c0d58-108">في الشجرة، حدد "المشرف على المحاسبة".</span><span class="sxs-lookup"><span data-stu-id="c0d58-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="c0d58-109">حدد الدور الذي تريده لتكوين القاعدة له.</span><span class="sxs-lookup"><span data-stu-id="c0d58-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="c0d58-110">في هذا المثال، حدد المشرف على المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="c0d58-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="c0d58-111">انقر فوق **إضافة قاعدة** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="c0d58-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="c0d58-112">في قائمة **تحديد فئة**، ابحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c0d58-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="c0d58-113">حدد الاستعلام لاستخدام هذه القاعدة.</span><span class="sxs-lookup"><span data-stu-id="c0d58-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="c0d58-114">في قائمة **اسم قاعدة العضوية**، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c0d58-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c0d58-115">انقر فوق **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="c0d58-115">Click **Edit query**.</span></span> <span data-ttu-id="c0d58-116">قم بتحرير الاستعلام، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="c0d58-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="c0d58-117">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="c0d58-117">Click **OK**.</span></span>
8. <span data-ttu-id="c0d58-118">انقر فوق **التشغيل التلقائي لتعيين الدور**.</span><span class="sxs-lookup"><span data-stu-id="c0d58-118">Click **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="c0d58-119">انتقل إلى **جزء التنقل > الوحدات > إدارة النظام > المستخدمون > المستخدمون** (بشكل مثالي في علامة تبويب منفصلة للمستعرض).</span><span class="sxs-lookup"><span data-stu-id="c0d58-119">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="c0d58-120">راجع الأدوار المعينة لمستخدمين متعددين للتأكد من صحة استعلام تعيين الدور.</span><span class="sxs-lookup"><span data-stu-id="c0d58-120">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="c0d58-121">قم بالتعديل وأعد التشغيل إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="c0d58-121">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="c0d58-122">استبعاد المستخدمين من تعيين الدور التلقائي</span><span class="sxs-lookup"><span data-stu-id="c0d58-122">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="c0d58-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c0d58-123">Close the page.</span></span>
2. <span data-ttu-id="c0d58-124">انتقل إلى **جزء التنقل > الوحدات > إدارة النظام > الأمان > تعيين مستخدمين للأدوار**.</span><span class="sxs-lookup"><span data-stu-id="c0d58-124">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="c0d58-125">في الشجرة، حدد "المشرف على المحاسبة".</span><span class="sxs-lookup"><span data-stu-id="c0d58-125">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="c0d58-126">حدد دورًا.</span><span class="sxs-lookup"><span data-stu-id="c0d58-126">Select a role.</span></span> <span data-ttu-id="c0d58-127">في هذا المثال، حدد المشرف على المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="c0d58-127">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="c0d58-128">في قائمة **المستخدمون المعينون للدور**، حدد **تعيين/استثناء المستخدمين يدويًا**.</span><span class="sxs-lookup"><span data-stu-id="c0d58-128">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="c0d58-129">في القائمة **‏‫تعيين المستخدمين إلى أو استبعاد المستخدمين من الدور**، قم بوضع علامة على الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c0d58-129">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="c0d58-130">حدد مستخدم.</span><span class="sxs-lookup"><span data-stu-id="c0d58-130">Select a user.</span></span>  
6. <span data-ttu-id="c0d58-131">في  **جزء الإجراء**، حدد **استبعاد من الدور**.</span><span class="sxs-lookup"><span data-stu-id="c0d58-131">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="c0d58-132">انقر فوق **استبعاد من الدور** لاستبعاد المستخدمين المحددين من الدور.</span><span class="sxs-lookup"><span data-stu-id="c0d58-132">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="c0d58-133">لإزالة الاستبعادات، حدد المستخدمين الذين تريد إزالة استبعادهم، ثم انقر فوق **حالة إعادة التعيين**.</span><span class="sxs-lookup"><span data-stu-id="c0d58-133">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="c0d58-134">عند إزالة استبعاد بإعادة تعيين حالة المستخدم، فإنه يتم تعيين دور المستخدم تلقائيًا مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="c0d58-134">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="c0d58-135">ومع ذلك، لا يتم تعيين المستخدم على الفور على الدور أو المستبعد من الدور عندما تقوم بإعادة تعيين الحالة.</span><span class="sxs-lookup"><span data-stu-id="c0d58-135">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="c0d58-136">بدلاً من ذلك، إما يتم تعيين المستخدم إلى الدور أو إزالته منه في المرة التالية التي يتم فيها تشغيل تعيين الدور التلقائي.</span><span class="sxs-lookup"><span data-stu-id="c0d58-136">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
