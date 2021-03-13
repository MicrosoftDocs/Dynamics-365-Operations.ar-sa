---
title: تكوين الخصومات
description: استخدم الخصومات في Microsoft Dynamics 365 Human Resources لتحديد مقدار، إن وُجد، الخصم من شيكات أجور العمل للموظف مقابل كل ميزة.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: c84e44e784e18c82098d63909f198049ae5f995c
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111335"
---
# <a name="configure-deductions"></a><span data-ttu-id="01385-103">تكوين الخصومات</span><span class="sxs-lookup"><span data-stu-id="01385-103">Configure deductions</span></span>

<span data-ttu-id="01385-104">استخدم الخصومات في Microsoft Dynamics 365 Human Resources لتحديد مقدار، إن وُجد، الخصم من شيكات أجور العمل للموظف مقابل كل ميزة.</span><span class="sxs-lookup"><span data-stu-id="01385-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="01385-105">الخصومات لها تاريخ سريان، بحيث يمكنك الاحتفاظ بسجل محفوظات خاص بمعلومات الخصم.</span><span class="sxs-lookup"><span data-stu-id="01385-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="01385-106">في مساحة العمل **إدارة الميزات**، ضمن **إعداد**، حدد **الخصومات**.</span><span class="sxs-lookup"><span data-stu-id="01385-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="01385-107">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="01385-107">Select **New**.</span></span>

3. <span data-ttu-id="01385-108">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="01385-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="01385-109">الحقل</span><span class="sxs-lookup"><span data-stu-id="01385-109">Field</span></span> | <span data-ttu-id="01385-110">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="01385-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="01385-111">**خصم**</span><span class="sxs-lookup"><span data-stu-id="01385-111">**Deduction**</span></span> | <span data-ttu-id="01385-112">معرف فريد يستخدم لتحديد الخصم الخاص بالميزة.</span><span class="sxs-lookup"><span data-stu-id="01385-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="01385-113">**‏‏الوصف**</span><span class="sxs-lookup"><span data-stu-id="01385-113">**Description**</span></span> | <span data-ttu-id="01385-114">وصف الخصم.</span><span class="sxs-lookup"><span data-stu-id="01385-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="01385-115">**فعالة**</span><span class="sxs-lookup"><span data-stu-id="01385-115">**Effective**</span></span> | <span data-ttu-id="01385-116">تاريخ البدء.</span><span class="sxs-lookup"><span data-stu-id="01385-116">The start date.</span></span> <span data-ttu-id="01385-117">والقيمة الافتراضية هي تاريخ النظام الحالي.</span><span class="sxs-lookup"><span data-stu-id="01385-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="01385-118">**انتهاء الصلاحية**</span><span class="sxs-lookup"><span data-stu-id="01385-118">**Expiration**</span></span> | <span data-ttu-id="01385-119">تاريخ الانتهاء.</span><span class="sxs-lookup"><span data-stu-id="01385-119">The end date.</span></span> <span data-ttu-id="01385-120">القيمة الافتراضية هي 12/31/2154، والتي تشير إلى ابدًا.</span><span class="sxs-lookup"><span data-stu-id="01385-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="01385-121">**العنوان**</span><span class="sxs-lookup"><span data-stu-id="01385-121">**Heading**</span></span> | <span data-ttu-id="01385-122">كود العنوان من نظام الرواتب الذي سيستخدمه هذا الخصم لجزء الموظف من الخصم عند معالجة الميزات لكشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="01385-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="01385-123">يستخدم هذا عند استخدام موفر رواتب من طرف آخر.</span><span class="sxs-lookup"><span data-stu-id="01385-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="01385-124">**مرجع الخصم في كشف رواتب الموظف**</span><span class="sxs-lookup"><span data-stu-id="01385-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="01385-125">كود الخصم من نظام كشف الرواتب الذي سيستخدمه هذا الخصم لجزء الموظف من الخصم عند معالجة المزايا لكشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="01385-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="01385-126">**عنوان المبلغ**</span><span class="sxs-lookup"><span data-stu-id="01385-126">**Amount heading**</span></span> | <span data-ttu-id="01385-127">كود العنوان من نظام الرواتب الذي سيستخدمه مبلغ الخصم هذا لجزء الموظف من الخصم عند معالجة الميزات لكشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="01385-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="01385-128">عادة ما يستخدم هذا عند استخدام موفر رواتب من طرف آخر.</span><span class="sxs-lookup"><span data-stu-id="01385-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="01385-129">**يمكن حذف**</span><span class="sxs-lookup"><span data-stu-id="01385-129">**Can delete**</span></span> | <span data-ttu-id="01385-130">يحدد ما إذا كانت القيمة المصدرة من Dynamics 365 for Finance and Operations يمكن أن تؤدي إلى حذف القيمة في نظام الرواتب.</span><span class="sxs-lookup"><span data-stu-id="01385-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="01385-131">**الأعمدة المقترنة**</span><span class="sxs-lookup"><span data-stu-id="01385-131">**Paired columns**</span></span> | <span data-ttu-id="01385-132">يحدد ما إذا كان سيتم تصدير مبلغ العنوان والخصم في أعمدة متجاورة مزدوجة إلى نظام الرواتب.</span><span class="sxs-lookup"><span data-stu-id="01385-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="01385-133">**تاريخ سريان التغيير**</span><span class="sxs-lookup"><span data-stu-id="01385-133">**Change effective date**</span></span> | <span data-ttu-id="01385-134">سيصبح التاريخ الذي يتغير به خصم الميزة ساريًا.</span><span class="sxs-lookup"><span data-stu-id="01385-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="01385-135">في هذا التاريخ، سيقوم النظام تلقائيًا بتغيير خصم الميزات وتحديث كافة خطط الميزات المرتبطة بهذا الخصم، طالما قمت بتشغيل معالجة **تحديث تغيير الخصم**.</span><span class="sxs-lookup"><span data-stu-id="01385-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="01385-136">**اكتمل تغيير الخصم**</span><span class="sxs-lookup"><span data-stu-id="01385-136">**Deduction change completed**</span></span> | <span data-ttu-id="01385-137">سيتم تحديد خانة الاختيار **اكتمل تغيير الخصم‬** تلقائيًا بمجرد اكتمال تغييرات خصم الميزة عن طريق معالجة تغيير تحديث الخصم.</span><span class="sxs-lookup"><span data-stu-id="01385-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="01385-138">لتتبع التغييرات التي تم إجراؤها على إعداد معدل الميزة والاحتفاظ بها، حدد **إجراءات**، ثم حدد **الاحتفاظ بالإصدارات**.</span><span class="sxs-lookup"><span data-stu-id="01385-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="01385-139">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="01385-139">Select **Save**.</span></span> 
