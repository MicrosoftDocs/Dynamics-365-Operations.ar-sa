---
title: تعيين مستخدمين إلى أدوار أمان
description: للوصول إلى تطبيقات Finance and Operations، يجب تعيين المستخدمين إلى أدوار الأمان.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
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
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180957"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="37763-103">تعيين مستخدمين إلى أدوار أمان</span><span class="sxs-lookup"><span data-stu-id="37763-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37763-104">لاستخدام أي شيء آخر غير القدرات الشائعة، يجب تعيين أدوار أمان إلى المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="37763-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="37763-105">يوضح هذا الإجراء كيف يمكن لمسؤولي النظام تعيين مستخدمين إلى أدوار بشكل تلقائي، استنادًا إلى بيانات العمل.</span><span class="sxs-lookup"><span data-stu-id="37763-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="37763-106">قم بتعيين مستخدمين إلى أدوار تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="37763-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="37763-107">انتقل إلى **جزء التنقل > الوحدات > إدارة النظام > الأمان > تعيين مستخدمين للأدوار**.</span><span class="sxs-lookup"><span data-stu-id="37763-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="37763-108">في الشجرة، حدد "المشرف على المحاسبة".</span><span class="sxs-lookup"><span data-stu-id="37763-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="37763-109">حدد الدور الذي تريده لتكوين القاعدة له.</span><span class="sxs-lookup"><span data-stu-id="37763-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="37763-110">في هذا المثال، حدد المشرف على المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="37763-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="37763-111">انقر فوق **إضافة قاعدة** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="37763-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="37763-112">في قائمة **تحديد فئة**، ابحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="37763-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="37763-113">حدد الاستعلام لاستخدام هذه القاعدة.</span><span class="sxs-lookup"><span data-stu-id="37763-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="37763-114">في قائمة **اسم قاعدة العضوية**، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="37763-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="37763-115">انقر فوق **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="37763-115">Click **Edit query**.</span></span> <span data-ttu-id="37763-116">قم بتحرير الاستعلام، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="37763-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="37763-117">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="37763-117">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="37763-118">استبعاد المستخدمين من تعيين الدور التلقائي</span><span class="sxs-lookup"><span data-stu-id="37763-118">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="37763-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="37763-119">Close the page.</span></span>
2. <span data-ttu-id="37763-120">انتقل إلى **جزء التنقل > الوحدات > إدارة النظام > الأمان > تعيين مستخدمين للأدوار**.</span><span class="sxs-lookup"><span data-stu-id="37763-120">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="37763-121">في الشجرة، حدد "المشرف على المحاسبة".</span><span class="sxs-lookup"><span data-stu-id="37763-121">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="37763-122">حدد دورًا.</span><span class="sxs-lookup"><span data-stu-id="37763-122">Select a role.</span></span> <span data-ttu-id="37763-123">في هذا المثال، حدد المشرف على المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="37763-123">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="37763-124">في قائمة **المستخدمون المعينون للدور**، حدد **تعيين/استثناء المستخدمين يدويًا**.</span><span class="sxs-lookup"><span data-stu-id="37763-124">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="37763-125">في القائمة **‏‫تعيين المستخدمين إلى أو استبعاد المستخدمين من الدور**، قم بوضع علامة على الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="37763-125">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="37763-126">حدد مستخدم.</span><span class="sxs-lookup"><span data-stu-id="37763-126">Select a user.</span></span>  
6. <span data-ttu-id="37763-127">في  **جزء الإجراء**، حدد **استبعاد من الدور**.</span><span class="sxs-lookup"><span data-stu-id="37763-127">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="37763-128">انقر فوق **استبعاد من الدور** لاستبعاد المستخدمين المحددين من الدور.</span><span class="sxs-lookup"><span data-stu-id="37763-128">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="37763-129">لإزالة الاستبعادات، حدد المستخدمين الذين تريد إزالة استبعادهم، ثم انقر فوق **حالة إعادة التعيين**.</span><span class="sxs-lookup"><span data-stu-id="37763-129">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="37763-130">عند إزالة استبعاد بإعادة تعيين حالة المستخدم، فإنه يتم تعيين دور المستخدم تلقائيًا مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="37763-130">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="37763-131">ومع ذلك، لا يتم تعيين المستخدم على الفور على الدور أو المستبعد من الدور عندما تقوم بإعادة تعيين الحالة.</span><span class="sxs-lookup"><span data-stu-id="37763-131">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="37763-132">بدلاً من ذلك، إما يتم تعيين المستخدم إلى الدور أو إزالته منه في المرة التالية التي يتم فيها تشغيل تعيين الدور التلقائي.</span><span class="sxs-lookup"><span data-stu-id="37763-132">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
