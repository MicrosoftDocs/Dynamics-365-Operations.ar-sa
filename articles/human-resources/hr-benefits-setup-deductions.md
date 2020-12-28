---
title: تكوين الخصومات
description: استخدم الخصومات في Microsoft Dynamics 365 Human Resources لتحديد مقدار، إن وُجد، الخصم من شيكات أجور العمل للموظف مقابل كل ميزة.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c59fa09e83ca91e0ad866e5875ff06370b7491d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417027"
---
# <a name="configure-deductions"></a><span data-ttu-id="2cff5-103">تكوين الخصومات</span><span class="sxs-lookup"><span data-stu-id="2cff5-103">Configure deductions</span></span>

<span data-ttu-id="2cff5-104">استخدم الخصومات في Microsoft Dynamics 365 Human Resources لتحديد مقدار، إن وُجد، الخصم من شيكات أجور العمل للموظف مقابل كل ميزة.</span><span class="sxs-lookup"><span data-stu-id="2cff5-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="2cff5-105">الخصومات لها تاريخ سريان، بحيث يمكنك الاحتفاظ بسجل محفوظات خاص بمعلومات الخصم.</span><span class="sxs-lookup"><span data-stu-id="2cff5-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="2cff5-106">في مساحة العمل **إدارة الميزات**، ضمن **إعداد**، حدد **الخصومات**.</span><span class="sxs-lookup"><span data-stu-id="2cff5-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="2cff5-107">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="2cff5-107">Select **New**.</span></span>

3. <span data-ttu-id="2cff5-108">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="2cff5-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="2cff5-109">الحقل</span><span class="sxs-lookup"><span data-stu-id="2cff5-109">Field</span></span> | <span data-ttu-id="2cff5-110">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="2cff5-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="2cff5-111">**خصم**</span><span class="sxs-lookup"><span data-stu-id="2cff5-111">**Deduction**</span></span> | <span data-ttu-id="2cff5-112">معرف فريد يستخدم لتحديد الخصم الخاص بالميزة.</span><span class="sxs-lookup"><span data-stu-id="2cff5-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="2cff5-113">**‏‏الوصف**</span><span class="sxs-lookup"><span data-stu-id="2cff5-113">**Description**</span></span> | <span data-ttu-id="2cff5-114">وصف الخصم.</span><span class="sxs-lookup"><span data-stu-id="2cff5-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="2cff5-115">**فعالة**</span><span class="sxs-lookup"><span data-stu-id="2cff5-115">**Effective**</span></span> | <span data-ttu-id="2cff5-116">تاريخ البدء.</span><span class="sxs-lookup"><span data-stu-id="2cff5-116">The start date.</span></span> <span data-ttu-id="2cff5-117">والقيمة الافتراضية هي تاريخ النظام الحالي.</span><span class="sxs-lookup"><span data-stu-id="2cff5-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="2cff5-118">**انتهاء الصلاحية**</span><span class="sxs-lookup"><span data-stu-id="2cff5-118">**Expiration**</span></span> | <span data-ttu-id="2cff5-119">تاريخ الانتهاء.</span><span class="sxs-lookup"><span data-stu-id="2cff5-119">The end date.</span></span> <span data-ttu-id="2cff5-120">القيمة الافتراضية هي 12/31/2154، والتي تشير إلى ابدًا.</span><span class="sxs-lookup"><span data-stu-id="2cff5-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="2cff5-121">**العنوان**</span><span class="sxs-lookup"><span data-stu-id="2cff5-121">**Heading**</span></span> | <span data-ttu-id="2cff5-122">كود العنوان من نظام الرواتب الذي سيستخدمه هذا الخصم لجزء الموظف من الخصم عند معالجة الميزات لكشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="2cff5-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="2cff5-123">يستخدم هذا عند استخدام موفر رواتب من طرف آخر.</span><span class="sxs-lookup"><span data-stu-id="2cff5-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="2cff5-124">**مرجع الخصم في كشف رواتب الموظف**</span><span class="sxs-lookup"><span data-stu-id="2cff5-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="2cff5-125">كود الخصم من نظام كشف الرواتب الذي سيستخدمه هذا الخصم لجزء الموظف من الخصم عند معالجة المزايا لكشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="2cff5-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="2cff5-126">**عنوان المبلغ**</span><span class="sxs-lookup"><span data-stu-id="2cff5-126">**Amount heading**</span></span> | <span data-ttu-id="2cff5-127">كود العنوان من نظام الرواتب الذي سيستخدمه مبلغ الخصم هذا لجزء الموظف من الخصم عند معالجة الميزات لكشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="2cff5-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="2cff5-128">عادة ما يستخدم هذا عند استخدام موفر رواتب من طرف آخر.</span><span class="sxs-lookup"><span data-stu-id="2cff5-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="2cff5-129">**يمكن حذف**</span><span class="sxs-lookup"><span data-stu-id="2cff5-129">**Can delete**</span></span> | <span data-ttu-id="2cff5-130">يحدد ما إذا كانت القيمة المصدرة من Dynamics 365 for Finance and Operations يمكن أن تؤدي إلى حذف القيمة في نظام الرواتب.</span><span class="sxs-lookup"><span data-stu-id="2cff5-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="2cff5-131">**الأعمدة المقترنة**</span><span class="sxs-lookup"><span data-stu-id="2cff5-131">**Paired columns**</span></span> | <span data-ttu-id="2cff5-132">يحدد ما إذا كان سيتم تصدير مبلغ العنوان والخصم في أعمدة متجاورة مزدوجة إلى نظام الرواتب.</span><span class="sxs-lookup"><span data-stu-id="2cff5-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="2cff5-133">**تاريخ سريان التغيير**</span><span class="sxs-lookup"><span data-stu-id="2cff5-133">**Change effective date**</span></span> | <span data-ttu-id="2cff5-134">سيصبح التاريخ الذي يتغير به خصم الميزة ساريًا.</span><span class="sxs-lookup"><span data-stu-id="2cff5-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="2cff5-135">في هذا التاريخ، سيقوم النظام تلقائيًا بتغيير خصم الميزات وتحديث كافة خطط الميزات المرتبطة بهذا الخصم، طالما قمت بتشغيل معالجة **تحديث تغيير الخصم**.</span><span class="sxs-lookup"><span data-stu-id="2cff5-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="2cff5-136">**اكتمل تغيير الخصم**</span><span class="sxs-lookup"><span data-stu-id="2cff5-136">**Deduction change completed**</span></span> | <span data-ttu-id="2cff5-137">سيتم تحديد خانة الاختيار **اكتمل تغيير الخصم‬** تلقائيًا بمجرد اكتمال تغييرات خصم الميزة عن طريق معالجة تغيير تحديث الخصم.</span><span class="sxs-lookup"><span data-stu-id="2cff5-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="2cff5-138">لتتبع التغييرات التي تم إجراؤها على إعداد معدل الميزة والاحتفاظ بها، حدد **إجراءات**، ثم حدد **الاحتفاظ بالإصدارات**.</span><span class="sxs-lookup"><span data-stu-id="2cff5-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="2cff5-139">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="2cff5-139">Select **Save**.</span></span> 
