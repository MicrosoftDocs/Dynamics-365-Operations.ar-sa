--- 
title: "تعيين مستخدمين إلى أدوار الأمان"
description: "للوصول إلى Microsoft Dynamics 365 for Finance and Operations، يجب تعيين المستخدمين إلى أدوار الأمان."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c7f35f57223798e91fc2a81c0821a2dc81512624
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="76a2d-103">تعيين مستخدمين إلى أدوار أمان</span><span class="sxs-lookup"><span data-stu-id="76a2d-103">Assign users to security roles</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76a2d-104">للوصول إلى Microsoft Dynamics 365 for Finance and Operations، يجب تعيين المستخدمين إلى أدوار الأمان.</span><span class="sxs-lookup"><span data-stu-id="76a2d-104">To access Microsoft Dynamics 365 for Finance and Operations, users must be assigned to security roles.</span></span> <span data-ttu-id="76a2d-105">يوضح هذا الإجراء كيف يمكن لمسؤولي النظام تعيين مستخدمين إلى أدوار تلقائيًا، استنادًا إلى بيانات العمل.</span><span class="sxs-lookup"><span data-stu-id="76a2d-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="76a2d-106">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="76a2d-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="76a2d-107">قم بتعيين مستخدمين إلى أدوار تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="76a2d-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="76a2d-108">انتقل إلى إدارة النظام > الأمان > تعيين مستخدمين للأدوار.</span><span class="sxs-lookup"><span data-stu-id="76a2d-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="76a2d-109">في الشجرة، حدد "المشرف على المحاسبة".</span><span class="sxs-lookup"><span data-stu-id="76a2d-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="76a2d-110">حدد الدور الذي تريده لتكوين القاعدة له.</span><span class="sxs-lookup"><span data-stu-id="76a2d-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="76a2d-111">في هذا المثال، حدد المشرف على المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="76a2d-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="76a2d-112">انقر فوق "إضافة قاعدة" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="76a2d-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="76a2d-113">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="76a2d-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="76a2d-114">حدد الاستعلام لاستخدام هذه القاعدة.</span><span class="sxs-lookup"><span data-stu-id="76a2d-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="76a2d-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="76a2d-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="76a2d-116">انقر فوق "تحرير استعلام".</span><span class="sxs-lookup"><span data-stu-id="76a2d-116">Click Edit query.</span></span>
    * <span data-ttu-id="76a2d-117">قم بتحرير الاستعلام، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="76a2d-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="76a2d-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="76a2d-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="76a2d-119">استبعاد المستخدمين من تعيين الدور التلقائي</span><span class="sxs-lookup"><span data-stu-id="76a2d-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="76a2d-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="76a2d-120">Close the page.</span></span>
2. <span data-ttu-id="76a2d-121">انتقل إلى إدارة النظام > الأمان > تعيين مستخدمين للأدوار.</span><span class="sxs-lookup"><span data-stu-id="76a2d-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="76a2d-122">في الشجرة، حدد "المشرف على المحاسبة".</span><span class="sxs-lookup"><span data-stu-id="76a2d-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="76a2d-123">حدد دورًا.</span><span class="sxs-lookup"><span data-stu-id="76a2d-123">Select a role.</span></span> <span data-ttu-id="76a2d-124">في هذا المثال، حدد المشرف على المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="76a2d-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="76a2d-125">انقر فوق تعيين/استبعاد المستخدمين يدويًا.</span><span class="sxs-lookup"><span data-stu-id="76a2d-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="76a2d-126">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="76a2d-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="76a2d-127">حدد مستخدم.</span><span class="sxs-lookup"><span data-stu-id="76a2d-127">Select a user.</span></span>  
6. <span data-ttu-id="76a2d-128">انقر فوق "استبعاد من الدور".</span><span class="sxs-lookup"><span data-stu-id="76a2d-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="76a2d-129">انقر فوق استبعاد من الدور لاستبعاد المستخدمين المحددين من الدور.</span><span class="sxs-lookup"><span data-stu-id="76a2d-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="76a2d-130">لإزالة الاستبعادات، حدد المستخدمين الذين تريد إزالة استبعادهم، ثم انقر فوق حالة إعادة التعيين.</span><span class="sxs-lookup"><span data-stu-id="76a2d-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="76a2d-131">عند إزالة استبعاد بإعادة تعيين حالة المستخدم، فإنه يتم تعيين دور المستخدم تلقائيًا مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="76a2d-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="76a2d-132">ومع ذلك، لا يتم تعيين المستخدم على الفور على الدور أو المستبعد من الدور عندما تقوم بإعادة تعيين الحالة.</span><span class="sxs-lookup"><span data-stu-id="76a2d-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="76a2d-133">بدلاً من ذلك، إما يتم تعيين المستخدم إلى الدور أو إزالته منه في المرة التالية التي يتم فيها تشغيل تعيين الدور التلقائي.</span><span class="sxs-lookup"><span data-stu-id="76a2d-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  


