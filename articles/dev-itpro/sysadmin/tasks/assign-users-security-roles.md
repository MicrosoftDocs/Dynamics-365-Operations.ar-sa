---
title: تعيين مستخدمين إلى أدوار أمان
description: للوصول إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition، يجب تعيين المستخدمين إلى أدوار الأمان.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c0afd0f5754e59307a82af9c9700b36c31edcc4
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851349"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="a8c6a-103">تعيين مستخدمين إلى أدوار أمان</span><span class="sxs-lookup"><span data-stu-id="a8c6a-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a8c6a-104">للوصول إلى Microsoft Dynamics 365 for Finance and Operations, Enterprise edition، يجب تعيين المستخدمين إلى أدوار الأمان.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="a8c6a-105">يوضح هذا الإجراء كيف يمكن لمسؤولي النظام تعيين مستخدمين إلى أدوار تلقائيًا، استنادًا إلى بيانات العمل.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="a8c6a-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="a8c6a-107">قم بتعيين مستخدمين إلى أدوار تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="a8c6a-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="a8c6a-108">انتقل إلى **جزء التنقل > الوحدات > إدارة النظام > الأمان > تعيين مستخدمين للأدوار**.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="a8c6a-109">في الشجرة، حدد "المشرف على المحاسبة".</span><span class="sxs-lookup"><span data-stu-id="a8c6a-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="a8c6a-110">حدد الدور الذي تريده لتكوين القاعدة له.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="a8c6a-111">في هذا المثال، حدد المشرف على المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="a8c6a-112">انقر فوق **إضافة قاعدة** لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-112">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="a8c6a-113">في قائمة **تحديد فئة**، ابحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-113">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="a8c6a-114">حدد الاستعلام لاستخدام هذه القاعدة.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="a8c6a-115">في قائمة **اسم قاعدة العضوية**، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a8c6a-116">انقر فوق **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-116">Click **Edit query**.</span></span> <span data-ttu-id="a8c6a-117">قم بتحرير الاستعلام، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="a8c6a-118">انقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-118">Click **OK**.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="a8c6a-119">استبعاد المستخدمين من تعيين الدور التلقائي</span><span class="sxs-lookup"><span data-stu-id="a8c6a-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="a8c6a-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-120">Close the page.</span></span>
2. <span data-ttu-id="a8c6a-121">انتقل إلى **جزء التنقل > الوحدات > إدارة النظام > الأمان > تعيين مستخدمين للأدوار**.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-121">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="a8c6a-122">في الشجرة، حدد "المشرف على المحاسبة".</span><span class="sxs-lookup"><span data-stu-id="a8c6a-122">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="a8c6a-123">حدد دورًا.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-123">Select a role.</span></span> <span data-ttu-id="a8c6a-124">في هذا المثال، حدد المشرف على المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="a8c6a-125">في قائمة **المستخدمون المعينون للدور**، حدد **تعيين/استثناء المستخدمين يدويًا**.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-125">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="a8c6a-126">في القائمة **‏‫تعيين المستخدمين إلى أو استبعاد المستخدمين من الدور**، قم بوضع علامة على الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-126">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="a8c6a-127">حدد مستخدم.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-127">Select a user.</span></span>  
6. <span data-ttu-id="a8c6a-128">في  **جزء الإجراء**، حدد **استبعاد من الدور**.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-128">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="a8c6a-129">انقر فوق **استبعاد من الدور** لاستبعاد المستخدمين المحددين من الدور.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-129">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="a8c6a-130">لإزالة الاستبعادات، حدد المستخدمين الذين تريد إزالة استبعادهم، ثم انقر فوق **حالة إعادة التعيين**.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-130">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="a8c6a-131">عند إزالة استبعاد بإعادة تعيين حالة المستخدم، فإنه يتم تعيين دور المستخدم تلقائيًا مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="a8c6a-132">ومع ذلك، لا يتم تعيين المستخدم على الفور على الدور أو المستبعد من الدور عندما تقوم بإعادة تعيين الحالة.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="a8c6a-133">بدلاً من ذلك، إما يتم تعيين المستخدم إلى الدور أو إزالته منه في المرة التالية التي يتم فيها تشغيل تعيين الدور التلقائي.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
