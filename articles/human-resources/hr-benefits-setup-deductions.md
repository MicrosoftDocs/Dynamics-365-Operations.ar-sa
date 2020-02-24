---
title: تكوين الخصومات
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007980"
---
# <a name="configure-deductions"></a><span data-ttu-id="d7277-102">تكوين الخصومات</span><span class="sxs-lookup"><span data-stu-id="d7277-102">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="d7277-103">استخدم الخصومات في Microsoft Dynamics 365 Human Resources لتحديد مقدار، إن وُجد، الخصم من شيكات أجور العمل للموظف مقابل كل ميزة.</span><span class="sxs-lookup"><span data-stu-id="d7277-103">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="d7277-104">وإن الخصومات ذات تاريخ سريان، بحيث يمكنك الاحتفاظ بسجل محفوظات خاص بمعلومات الخصم.</span><span class="sxs-lookup"><span data-stu-id="d7277-104">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="d7277-105">في مساحة العمل **إدارة الميزات**، ضمن **إعداد**، حدد **الخصومات**.</span><span class="sxs-lookup"><span data-stu-id="d7277-105">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="d7277-106">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d7277-106">Select **New**.</span></span>

3. <span data-ttu-id="d7277-107">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="d7277-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="d7277-108">الحقل</span><span class="sxs-lookup"><span data-stu-id="d7277-108">Field</span></span> | <span data-ttu-id="d7277-109">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="d7277-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d7277-110">خصم</span><span class="sxs-lookup"><span data-stu-id="d7277-110">Deduction</span></span> | <span data-ttu-id="d7277-111">معرف فريد يستخدم لتحديد الخصم الخاص بالميزة.</span><span class="sxs-lookup"><span data-stu-id="d7277-111">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="d7277-112">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="d7277-112">Description</span></span> | <span data-ttu-id="d7277-113">وصف الخصم.</span><span class="sxs-lookup"><span data-stu-id="d7277-113">A description for the deduction.</span></span> |
   | <span data-ttu-id="d7277-114">فعالة</span><span class="sxs-lookup"><span data-stu-id="d7277-114">Effective</span></span> | <span data-ttu-id="d7277-115">تاريخ البدء.</span><span class="sxs-lookup"><span data-stu-id="d7277-115">The start date.</span></span> <span data-ttu-id="d7277-116">والقيمة الافتراضية هي تاريخ النظام الحالي.</span><span class="sxs-lookup"><span data-stu-id="d7277-116">The default value is the current system date.</span></span> |
   | <span data-ttu-id="d7277-117">انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="d7277-117">Expiration</span></span> | <span data-ttu-id="d7277-118">تاريخ الانتهاء.</span><span class="sxs-lookup"><span data-stu-id="d7277-118">The end date.</span></span> <span data-ttu-id="d7277-119">القيمة الافتراضية هي 12/31/2154، والتي تشير إلى ابدًا.</span><span class="sxs-lookup"><span data-stu-id="d7277-119">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="d7277-120">العنوان</span><span class="sxs-lookup"><span data-stu-id="d7277-120">Heading</span></span> | <span data-ttu-id="d7277-121">كود العنوان من نظام الرواتب الذي سيستخدمه هذا الخصم لجزء الموظف من الخصم عند معالجة الميزات لكشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="d7277-121">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="d7277-122">يستخدم هذا عند استخدام موفر رواتب بطرف آخر.</span><span class="sxs-lookup"><span data-stu-id="d7277-122">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="d7277-123">مرجع الخصم في كشف رواتب الموظف</span><span class="sxs-lookup"><span data-stu-id="d7277-123">Employee payroll deduction reference</span></span> | <span data-ttu-id="d7277-124">كود الخصم من نظام كشف الرواتب الذي سيستخدمه هذا الخصم لجزء الموظف من الخصم عند معالجة المزايا لكشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="d7277-124">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="d7277-125">عنوان المبلغ</span><span class="sxs-lookup"><span data-stu-id="d7277-125">Amount heading</span></span> | <span data-ttu-id="d7277-126">كود العنوان من نظام الرواتب الذي سيستخدمه مبلغ الخصم هذا لجزء الموظف من الخصم عند معالجة الميزات لكشف الرواتب.</span><span class="sxs-lookup"><span data-stu-id="d7277-126">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="d7277-127">عادة ما يستخدم هذا عند استخدام موفر رواتب بطرف آخر.</span><span class="sxs-lookup"><span data-stu-id="d7277-127">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="d7277-128">يمكن حذف</span><span class="sxs-lookup"><span data-stu-id="d7277-128">Can delete</span></span> | <span data-ttu-id="d7277-129">يحدد ما إذا كانت القيمة المصدرة من Dynamics 365 for Finance and Operations يمكن أن تؤدي إلى حذف القيمة في نظام الرواتب.</span><span class="sxs-lookup"><span data-stu-id="d7277-129">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="d7277-130">الأعمدة المقترنة</span><span class="sxs-lookup"><span data-stu-id="d7277-130">Paired columns</span></span> | <span data-ttu-id="d7277-131">يحدد ما إذا كان سيتم تصدير مبلغ العنوان والخصم في أعمدة متجاورة مزدوجة إلى نظام الرواتب.</span><span class="sxs-lookup"><span data-stu-id="d7277-131">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="d7277-132">تاريخ سريان التغيير</span><span class="sxs-lookup"><span data-stu-id="d7277-132">Change effective date</span></span> | <span data-ttu-id="d7277-133">سيصبح التاريخ الذي يتغير به خصم الميزة ساريًا.</span><span class="sxs-lookup"><span data-stu-id="d7277-133">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="d7277-134">في هذا التاريخ، سيقوم النظام تلقائيًا بتغيير خصم الميزات وتحديث كافة خطط الميزات المرتبطة بهذا الخصم، طالما قمت بتشغيل معالجة تحديث تغيير الخصم.</span><span class="sxs-lookup"><span data-stu-id="d7277-134">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="d7277-135">اكتمل تغيير الخصم</span><span class="sxs-lookup"><span data-stu-id="d7277-135">Deduction change completed</span></span> | <span data-ttu-id="d7277-136">سيتم تحديد خانة الاختيار "تغيير الخصم اكتمل" تلقائيًا بمجرد اكتمال تغييرات خصم الميزة عن طريق معالجة تغيير تحديث الخصم.</span><span class="sxs-lookup"><span data-stu-id="d7277-136">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="d7277-137">لتتبع التغييرات التي تم إجراؤها على إعداد معدل الميزة والاحتفاظ بها، حدد **إجراءات**، ثم حدد **الاحتفاظ بالإصدارات**.</span><span class="sxs-lookup"><span data-stu-id="d7277-137">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="d7277-138">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d7277-138">Select **Save**.</span></span> 
