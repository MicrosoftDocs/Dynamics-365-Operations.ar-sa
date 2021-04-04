---
title: تعيين مستخدمين إلى أدوار أمان
description: للوصول إلى تطبيقات Finance and Operations، يجب تعيين المستخدمين إلى أدوار الأمان.
author: Peakerbl
manager: AnnBe
ms.date: 05/06/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1a6d904ae3df23dd1c602cfdfecc40411aba5724
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569864"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="17aba-103">تعيين مستخدمين إلى أدوار أمان</span><span class="sxs-lookup"><span data-stu-id="17aba-103">Assign users to security roles</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17aba-104">لاستخدام أي شيء آخر غير القدرات الشائعة في تطبيقات Finance and Operations يجب تعيين أدوار أمان إلى المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="17aba-104">To use anything other than common capabilities in Finance and Operations apps, users must be assigned to security roles.</span></span> <span data-ttu-id="17aba-105">يمكنك تعيين المستخدمين إلى الأدوار تلقائيا، استنادا إلى القواعد وبيانات الاعمال، أو استثناء المستخدمين من التعيين التلقائي للدور، أو إضافه مستخدمين إلى الأدوار يدويا.</span><span class="sxs-lookup"><span data-stu-id="17aba-105">You can assign users to roles automatically, based on rules and business data, exclude users from automatic role assignment, or add users to roles manually.</span></span>

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="17aba-106">قم بتعيين مستخدمين إلى أدوار تلقائيًا</span><span class="sxs-lookup"><span data-stu-id="17aba-106">Automatically assign users to roles</span></span>
<span data-ttu-id="17aba-107">يوضح هذا الإجراء كيف يمكن لمسؤولي النظام تعيين مستخدمين إلى أدوار بشكل تلقائي، استنادًا إلى بيانات العمل.</span><span class="sxs-lookup"><span data-stu-id="17aba-107">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 
1. <span data-ttu-id="17aba-108">انتقل إلى **جزء التنقل > الوحدات > إدارة النظام > الأمان > تعيين مستخدمين للأدوار**.</span><span class="sxs-lookup"><span data-stu-id="17aba-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="17aba-109">في الشجرة، حدد "المشرف على المحاسبة".</span><span class="sxs-lookup"><span data-stu-id="17aba-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="17aba-110">حدد الدور الذي تريده لتكوين القاعدة له.</span><span class="sxs-lookup"><span data-stu-id="17aba-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="17aba-111">في هذا المثال، حدد المشرف على المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="17aba-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="17aba-112">حدد **إضافة قاعدة** لفتح قائمة مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="17aba-112">Select **Add rule** to open the dialog menu.</span></span>
4. <span data-ttu-id="17aba-113">في قائمة **تحديد فئة**، ابحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="17aba-113">In the **Select a query** list, find and select the desired record.</span></span> <span data-ttu-id="17aba-114">حدد الاستعلام لاستخدام هذه القاعدة.</span><span class="sxs-lookup"><span data-stu-id="17aba-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="17aba-115">في قائمة **اسم قاعدة العضوية**، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="17aba-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="17aba-116">حدد **تحرير الاستعلام**.</span><span class="sxs-lookup"><span data-stu-id="17aba-116">Select **Edit query**.</span></span> <span data-ttu-id="17aba-117">قم بتحرير الاستعلام، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="17aba-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="17aba-118">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="17aba-118">Select **OK**.</span></span>
8. <span data-ttu-id="17aba-119">حدد **التشغيل التلقائي لتعيين الدور**.</span><span class="sxs-lookup"><span data-stu-id="17aba-119">Select **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="17aba-120">انتقل إلى **جزء التنقل > الوحدات > إدارة النظام > المستخدمون > المستخدمون** (بشكل مثالي في علامة تبويب منفصلة للمستعرض).</span><span class="sxs-lookup"><span data-stu-id="17aba-120">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="17aba-121">راجع الأدوار المعينة لمستخدمين متعددين للتأكد من صحة استعلام تعيين الدور.</span><span class="sxs-lookup"><span data-stu-id="17aba-121">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="17aba-122">قم بالتعديل وأعد التشغيل إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="17aba-122">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="17aba-123">استبعاد المستخدمين من تعيين الدور التلقائي</span><span class="sxs-lookup"><span data-stu-id="17aba-123">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="17aba-124">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="17aba-124">Close the page.</span></span>
2. <span data-ttu-id="17aba-125">انتقل إلى **جزء التنقل > الوحدات > إدارة النظام > الأمان > تعيين مستخدمين للأدوار**.</span><span class="sxs-lookup"><span data-stu-id="17aba-125">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="17aba-126">في الشجرة، حدد "المشرف على المحاسبة".</span><span class="sxs-lookup"><span data-stu-id="17aba-126">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="17aba-127">حدد دورًا.</span><span class="sxs-lookup"><span data-stu-id="17aba-127">Select a role.</span></span> <span data-ttu-id="17aba-128">في هذا المثال، حدد المشرف على المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="17aba-128">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="17aba-129">في قائمة **المستخدمون المعينون للدور**، حدد **تعيين/استثناء المستخدمين يدويًا**.</span><span class="sxs-lookup"><span data-stu-id="17aba-129">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="17aba-130">في القائمة **‏‫تعيين المستخدمين إلى أو استبعاد المستخدمين من الدور**، قم بوضع علامة على الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="17aba-130">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="17aba-131">حدد مستخدم.</span><span class="sxs-lookup"><span data-stu-id="17aba-131">Select a user.</span></span>  
6. <span data-ttu-id="17aba-132">في  **جزء الإجراء**، حدد **استبعاد من الدور**.</span><span class="sxs-lookup"><span data-stu-id="17aba-132">On the **Action pane**, select **Exclude from role**.</span></span>
7. <span data-ttu-id="17aba-133">حدد **استبعاد من الدور** لاستبعاد المستخدمين المحددين من الدور.</span><span class="sxs-lookup"><span data-stu-id="17aba-133">Select **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="17aba-134">لإزالة الاستبعادات، حدد المستخدمين الذين تريد إزالة استبعادهم، ثم انقر فوق **حالة إعادة التعيين**.</span><span class="sxs-lookup"><span data-stu-id="17aba-134">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="17aba-135">عند إزالة استبعاد بإعادة تعيين حالة المستخدم، فإنه يتم تعيين دور المستخدم تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="17aba-135">When you remove an exclusion by resetting the user's status, the user's role is assigned automatically.</span></span> <span data-ttu-id="17aba-136">ومع ذلك، لا يتم تعيين المستخدم على الفور على الدور أو المستبعد من الدور عندما تقوم بإعادة تعيين الحالة.</span><span class="sxs-lookup"><span data-stu-id="17aba-136">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="17aba-137">بدلاً من ذلك، إما يتم تعيين المستخدم إلى الدور أو إزالته منه في المرة التالية التي يتم فيها تشغيل تعيين الدور التلقائي.</span><span class="sxs-lookup"><span data-stu-id="17aba-137">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

## <a name="manually-assign-users-to-roles"></a><span data-ttu-id="17aba-138">تعيين مستخدمين إلى أدوار يدوياً</span><span class="sxs-lookup"><span data-stu-id="17aba-138">Manually assign users to roles</span></span>
<span data-ttu-id="17aba-139">كما أنه يجب إزالة المستخدمين الذين يتم تعيين أدوار الأمان لهم يدويًا بشكل يدوي بواسطة المسؤول.</span><span class="sxs-lookup"><span data-stu-id="17aba-139">Users who are manually assigned to security roles must also be manually removed by the administrator.</span></span> <span data-ttu-id="17aba-140">هؤلاء المستخدين لا يتم إزالتهم من الأدوار بواسطة الأدوار للتعيين التلقائي للدور.</span><span class="sxs-lookup"><span data-stu-id="17aba-140">These users are not removed from roles by rules for automatic role assignment.</span></span>

1. <span data-ttu-id="17aba-141">انتقل إلى **جزء التنقل > الوحدات > إدارة النظام > الأمان > تعيين مستخدمين للأدوار**.</span><span class="sxs-lookup"><span data-stu-id="17aba-141">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="17aba-142">في الشجرة، حدد دور، في قائمة **المستخدمون المعينون للدور** حدد **تعيين/استثناء المستخدمين يدويًا**.</span><span class="sxs-lookup"><span data-stu-id="17aba-142">In the tree, select a role, and in the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
4. <span data-ttu-id="17aba-143">في **تعيين المستخدمين إلى أو استبعاد المستخدمين من الدور** يتم سرد المستخدمين الذين لم يتم تعيين الدور لهم بتعيين **وضع التعيين** على **بلا**.</span><span class="sxs-lookup"><span data-stu-id="17aba-143">In the **Assign users to or exclude users from role**, users that have not been assigned the role are listed with the **Assignment mode** set to **None**.</span></span> <span data-ttu-id="17aba-144">حدد مستخدما واحدا أو أكثر ينبغي تعيين الدور له.</span><span class="sxs-lookup"><span data-stu-id="17aba-144">Select one or more users that should be assigned the role.</span></span>
5. <span data-ttu-id="17aba-145">في **جزء الإجراء**، حدد **تعيين إلى الدور**.</span><span class="sxs-lookup"><span data-stu-id="17aba-145">On the **Action pane**, select **Assign to role**.</span></span> <span data-ttu-id="17aba-146">يتم تحديث **وضع التعيين** إلى **يدوي** وأصبح للمستخدمين دور جديد معيّن الآن.</span><span class="sxs-lookup"><span data-stu-id="17aba-146">The **Assignment mode** is updated to **Manual** and the users now have a new role assigned.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]