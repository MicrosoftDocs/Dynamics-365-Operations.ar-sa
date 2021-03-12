---
title: تحديد وحل التعارضات في الفصل بين المهام
description: يشرح هذا الموضوع كيفية التعرّف على التعارضات وحلها في الفصل بين المهام.
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deff97c7728db91089d3ea834d15de738da500fa
ms.sourcegitcommit: 316200579dd5b04ad76f276a2ed6b0f55fa8c812
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/05/2021
ms.locfileid: "4826358"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a><span data-ttu-id="aacd6-103">تحديد وحل التعارضات في الفصل بين المهام</span><span class="sxs-lookup"><span data-stu-id="aacd6-103">Identify and resolve conflicts in segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aacd6-104">يشرح هذا الموضوع كيفية التعرّف على التعارضات وحلها في الفصل بين المهام.</span><span class="sxs-lookup"><span data-stu-id="aacd6-104">This topic explains how to identify and resolve conflicts in segregation of duties.</span></span> <span data-ttu-id="aacd6-105">يمكنك إعداد قواعد لفصل الواجبات التي يجب تنفيذها بواسطة مستخدمين مختلفين.</span><span class="sxs-lookup"><span data-stu-id="aacd6-105">You can set up rules to separate duties that must be performed by different users.</span></span> <span data-ttu-id="aacd6-106">يسمى هذا المفهوم الفصل بين المهام.</span><span class="sxs-lookup"><span data-stu-id="aacd6-106">This concept is named segregation of duties.</span></span> <span data-ttu-id="aacd6-107">عندما يخالف تعريف دور أمان أو تعيينات أدوار لأحد المستخدمين القواعد، سيتم تسجيل التعارض.</span><span class="sxs-lookup"><span data-stu-id="aacd6-107">When the definition of a security role or the role assignments of a user violate the rules, the conflict is logged.</span></span> <span data-ttu-id="aacd6-108">يجب حل جميع التعارضات بواسطة المسؤول.</span><span class="sxs-lookup"><span data-stu-id="aacd6-108">All conflicts must be resolved by the administrator.</span></span> <span data-ttu-id="aacd6-109">أكمل الإجراء التالي لتحديد التعارضات وحلها.</span><span class="sxs-lookup"><span data-stu-id="aacd6-109">Complete the following procedure to identify and resolve conflicts.</span></span>

<span data-ttu-id="aacd6-110">بعد أضافه قاعده، تحقق من توافق كافة الأدوار الموجودة.</span><span class="sxs-lookup"><span data-stu-id="aacd6-110">After a rule has been added, verify that all existing roles are compliant.</span></span> 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="aacd6-111">التحقق مما إذا كانت تعيينات دور المستخدم الموجودة تتوافق مع القواعد الجديدة للفصل بين المهام</span><span class="sxs-lookup"><span data-stu-id="aacd6-111">Verify that existing roles and duties comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="aacd6-112">انتقل إلى **إدارة النظام**  > **الأمان** > **الفصل بين المهام** > **قواعد الفصل بين المهام**.</span><span class="sxs-lookup"><span data-stu-id="aacd6-112">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
3. <span data-ttu-id="aacd6-113">حدد **التحقق من صحة المهام والأدوار**.</span><span class="sxs-lookup"><span data-stu-id="aacd6-113">Select **Validate duties and roles**.</span></span> <span data-ttu-id="aacd6-114">إذا كانت أي أدوار موجودة تخالف القواعد المحددة، سيتم عرض رسالة تحتوي على اسم القاعدة والدور وأسماء المهام المتعارضة.</span><span class="sxs-lookup"><span data-stu-id="aacd6-114">If any roles violate the rules, a message is displayed that contains the name of the rule, the role, and the names of the conflicting duties.</span></span> <span data-ttu-id="aacd6-115">يجب تعديل الأدوار المتعارضة باستخدام **تكوين الأمان** ولا يمكن ان تتضمن مهام متعارضة.</span><span class="sxs-lookup"><span data-stu-id="aacd6-115">Conflicting roles must be modified using **Security configuration** and can't include conflicting duties.</span></span> <span data-ttu-id="aacd6-116">إذا لم تخالف أية أدوار القاعدة المحددة، ستشير إحدى الرسائل إلى أن جميع الأدوار متوافقة مع القاعدة المحددة.</span><span class="sxs-lookup"><span data-stu-id="aacd6-116">If no roles violate the selected rule, a message indicates that all roles comply.</span></span>   

> [!NOTE]
> <span data-ttu-id="aacd6-117">يتم اجراء التحقق من الصحة فقط للقاعدة المحددة.</span><span class="sxs-lookup"><span data-stu-id="aacd6-117">The validation is only performed for the selected rule.</span></span> <span data-ttu-id="aacd6-118">من المهم التحقق من صحة التوافق لكل قاعده.</span><span class="sxs-lookup"><span data-stu-id="aacd6-118">It is important to validate compliance for each rule.</span></span>   

<span data-ttu-id="aacd6-119">عند إنشاء دور أو تعديله ، يتم فرض قواعد الفصل بين المهام تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="aacd6-119">When you create or modify a role, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="aacd6-120">ولا يمكنك تعيين مهام متعارضة إلى أحد الأدوار.</span><span class="sxs-lookup"><span data-stu-id="aacd6-120">You cannot assign conflicting duties to a role.</span></span>

<span data-ttu-id="aacd6-121">بعد ذلك، تحقق من توافق كافة تعيينات الأدوار الموجودة.</span><span class="sxs-lookup"><span data-stu-id="aacd6-121">Next, verify that all existing role assignments are compliant.</span></span>

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="aacd6-122">التحقق مما إذا كانت تعيينات دور المستخدم تتوافق مع القواعد الجديدة للفصل بين المهام</span><span class="sxs-lookup"><span data-stu-id="aacd6-122">Verify that user role assignments comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="aacd6-123">انتقل إلى **إدارة النظام > الأمان > الفصل بين المهام > التحقق من توافق تعيينات دور المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="aacd6-123">Go to **System administration > Security > Segregation of duties > Verify compliance of user-role assignments**.</span></span>
2. <span data-ttu-id="aacd6-124">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="aacd6-124">Select **OK**.</span></span> <span data-ttu-id="aacd6-125">يعرض أحد الإخطارات نتائج التحقق.</span><span class="sxs-lookup"><span data-stu-id="aacd6-125">A notification displays the results of the validation.</span></span> <span data-ttu-id="aacd6-126">يتم تسجيل التعارضات في صفحة **التعارضات غير المحلولة في الفصل بين المهام**.</span><span class="sxs-lookup"><span data-stu-id="aacd6-126">Conflicts are logged on the **Segregation of duties unresolved conflicts** page.</span></span>   

<span data-ttu-id="aacd6-127">عند تعيين المستخدمين في أدوار، يتم فرض قواعد الفصل بين المهام تلقائيا.</span><span class="sxs-lookup"><span data-stu-id="aacd6-127">When you assign users to roles, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="aacd6-128">إذا حاولت تعيين مستخدم للأدوار التي تحتوي علي مهام متعارضة، ستتلقى رسالة خطا.</span><span class="sxs-lookup"><span data-stu-id="aacd6-128">If you try to assign a user to roles that contain conflicting duties, you receive an error message.</span></span> <span data-ttu-id="aacd6-129">يجب حل التعارض من خلال رفض السماح بتعيين الدور الإضافي أو رفضه.</span><span class="sxs-lookup"><span data-stu-id="aacd6-129">You must then resolve the conflict by denying or allowing the additional role assignment.</span></span> <span data-ttu-id="aacd6-130">سيتم تعيين الدور الإضافي بعد السماح بالتعيين.</span><span class="sxs-lookup"><span data-stu-id="aacd6-130">The additional role will be assigned after the assignment is allowed.</span></span> 

> [!NOTE]
> <span data-ttu-id="aacd6-131">لا يتم التحقق من التعارضات حاليا للمستخدمين الذين يتم تعيين ادوار لها استنادا إلى مجموعات مجال خدمه Active Directory.</span><span class="sxs-lookup"><span data-stu-id="aacd6-131">Conflicts are currently not verified for users that are assigned roles based on the Active Directory Domain groups.</span></span>

## <a name="view-and-resolve-conflicting-user-role-assignments"></a><span data-ttu-id="aacd6-132">عرض تعيينات دور المستخدم المتعارضة وحلها</span><span class="sxs-lookup"><span data-stu-id="aacd6-132">View and resolve conflicting user role assignments</span></span>
1. <span data-ttu-id="aacd6-133">انتقل إلى **إدارة النظام** > **الأمان** > **الفصل بين المهام** > **التعارضات غير المحلولة في الفصل بين المهام**.</span><span class="sxs-lookup"><span data-stu-id="aacd6-133">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties unresolved conflicts**.</span></span> 
2. <span data-ttu-id="aacd6-134">حدد تعارضًا، ثم حدد أحد الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="aacd6-134">Select a conflict, and then select one of the following actions:</span></span> 

  - <span data-ttu-id="aacd6-135">**رفض التعيين**: رفض تعيين المستخدم إلى دور الأمان الإضافي.</span><span class="sxs-lookup"><span data-stu-id="aacd6-135">**Deny assignment**: This will deny the assignment of the user to the additional security role.</span></span> <span data-ttu-id="aacd6-136">إذا قمت برفض تعيين دور تلقائي، سيتم تمييز المستخدم بوصف "مستبعد من الدور".</span><span class="sxs-lookup"><span data-stu-id="aacd6-136">If you deny an automatic role assignment, the user is marked as excluded from the role.</span></span> <span data-ttu-id="aacd6-137">ولا يُمنح المستخدم المستبعد الوصول المقترن بالدور، ولا يمكن تعيين المستخدم إلى الدور حتى يزيل المسؤول الاستبعاد.</span><span class="sxs-lookup"><span data-stu-id="aacd6-137">The excluded user isn't granted the access associated with the role and can't be assigned to the role until the administrator removes the exclusion.</span></span> 
-  <span data-ttu-id="aacd6-138">**السماح بالتعيين**: تجاوز التعارض والسماح بتعيين المستخدم لدور أمان إضافي.</span><span class="sxs-lookup"><span data-stu-id="aacd6-138">**Allow assignment**: This will override the conflict and allow the user to be assigned to the additional security role.</span></span> <span data-ttu-id="aacd6-139">إذا تجاوزتَ تعارضًا ما، يجب عليك إدخال سبب في الحقل **سبب التجاوز**.</span><span class="sxs-lookup"><span data-stu-id="aacd6-139">If you override a conflict, you must enter a reason in the **Reason for override** field.</span></span> <span data-ttu-id="aacd6-140">يمكن عرض كافة تعيينات الأدوار التي تم تجاوزها في الصفحة **الفصل بين تعارضات المهام**.</span><span class="sxs-lookup"><span data-stu-id="aacd6-140">All overridden role assignments can be viewed on the **Segregation of duties conflicts** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="aacd6-141">في حاله سرد عده تعارضات لنفس المستخدم، حدد سجل المستخدم وقم بتقييم الأدوار المعينة في الصفحة **المستخدمون**</span><span class="sxs-lookup"><span data-stu-id="aacd6-141">If several conflicts are listed for the same user, select the user record and evaluate assigned roles on the **Users** page.</span></span> <span data-ttu-id="aacd6-142">لتجنب هذا التعارض، قم بالتحقق من صحة كل قاعده بعد اضافتها أو تعديلها.</span><span class="sxs-lookup"><span data-stu-id="aacd6-142">To avoid this conflict, validate each rule after it's added or modified.</span></span>
