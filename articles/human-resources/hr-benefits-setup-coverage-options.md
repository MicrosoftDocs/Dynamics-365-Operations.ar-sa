---
title: إنشاء خيارات تغطية
description: خيارات التغطية في Microsoft Dynamics 365 Human Resources عبارة عن مستويات تغطية لاختيار مشاركة في خطة أو برنامج مزايا.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6d304b0cf65c7833ebc7f21323efc59540289de8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803671"
---
# <a name="create-coverage-options"></a><span data-ttu-id="4d5eb-103">إنشاء خيارات تغطية</span><span class="sxs-lookup"><span data-stu-id="4d5eb-103">Create coverage options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4d5eb-104">خيارات التغطية في Microsoft Dynamics 365 Human Resources عبارة عن مستويات تغطية لاختيار مشاركة في خطة أو برنامج مزايا.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program.</span></span> <span data-ttu-id="4d5eb-105">على سبيل المثال، بإمكان خيارات التغطية أن تتضمن **الموظف فقط** لخطة طبية، أو **2x الراتب** لخطة تأمين على الحياة.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-105">For example, coverage options could include **Employee Only** for a medical plan, or **2x Salary** for a life insurance plan.</span></span> <span data-ttu-id="4d5eb-106">يمكنك إعادة استخدام خيارات تغطية المزايا بعد تحديدها.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-106">Once defined, you can reuse benefit coverage options.</span></span> <span data-ttu-id="4d5eb-107">يمكنك ربط خيار بخطة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-107">You can associate an option with one or more plans.</span></span>

<span data-ttu-id="4d5eb-108">بعد تحديد خيارات التغطية، قم بإرفاق خيارات التغطية بنوع خطة مزايا.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-108">After you define coverage options, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="4d5eb-109">ثم يتم إقران نوع الخطة بنوع خطة أو برنامج الميزة.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-109">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="4d5eb-110">تتوفر خيارات التغطية المقترنة بنوع خطة لكافة الخطط التي يتم إنشاؤها باستخدام نوع الخطة هذا.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-110">Coverage options that are associated with a plan type are available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="4d5eb-111">في مساحة العمل **إدارة الميزات**، ضمن **إعداد**، حدد **خيارات التغطية**.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-111">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="4d5eb-112">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-112">Select **New**.</span></span>

3. <span data-ttu-id="4d5eb-113">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="4d5eb-113">Specify values for the following fields:</span></span>

   | <span data-ttu-id="4d5eb-114">الحقل</span><span class="sxs-lookup"><span data-stu-id="4d5eb-114">Field</span></span> | <span data-ttu-id="4d5eb-115">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="4d5eb-115">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4d5eb-116">**خيار التغطية**</span><span class="sxs-lookup"><span data-stu-id="4d5eb-116">**Coverage option**</span></span> | <span data-ttu-id="4d5eb-117">اسم خيار تغطية فريد.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-117">A unique coverage option name.</span></span> |
   | <span data-ttu-id="4d5eb-118">**‏‏الوصف**</span><span class="sxs-lookup"><span data-stu-id="4d5eb-118">**Description**</span></span> | <span data-ttu-id="4d5eb-119">وصف خيار التغطية.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-119">A description of the coverage option.</span></span> |
   | <span data-ttu-id="4d5eb-120">**كود التغطية**</span><span class="sxs-lookup"><span data-stu-id="4d5eb-120">**Coverage code**</span></span> | <span data-ttu-id="4d5eb-121">تعمل أكواد التغطية على تعيين الحد الأدنى والأقصى للمبالغ لكل نوع شخص مغطى مؤهل.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-121">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="4d5eb-122">يشير كود التغطية إلى الشخص الذي تمت تغطيته أو مبلغ التغطية المسموح به لنوع الخطة.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-122">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="4d5eb-123">يمكنك التعبير عن مبلغ التغطية كمبلغًا بالدولار أو بالنسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-123">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="4d5eb-124">على سبيل المثال:</span><span class="sxs-lookup"><span data-stu-id="4d5eb-124">For example:</span></span></br></br><span data-ttu-id="4d5eb-125">- **موظف+1** – ليكون مؤهلاً، يجب على الموظف أن يحدد معال واحد (إذا تم تحديد أكثر من معال، لن يكون مؤهلاً بعد ذلك).</span><span class="sxs-lookup"><span data-stu-id="4d5eb-125">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="4d5eb-126">- **موظف + الأسرة** – ليكون مؤهلاً، يجب على الموظف أن يحدد معالين على الأقل.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-126">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="4d5eb-127">**أقصى عدد**</span><span class="sxs-lookup"><span data-stu-id="4d5eb-127">**Maximum number**</span></span> | <span data-ttu-id="4d5eb-128">الحد الأقصى لعدد المعالين.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-128">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="4d5eb-129">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="4d5eb-129">**Status**</span></span> | <span data-ttu-id="4d5eb-130">حالة خيار التغطية.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-130">The status of the coverage option.</span></span> <span data-ttu-id="4d5eb-131">في حالة تعيين حالة خيار التغطية على "غير نشط"، فإنه يتعذر تحديد خيار التغطية في أنواع الخطط.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-131">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="4d5eb-132">**النسبة المئوية**</span><span class="sxs-lookup"><span data-stu-id="4d5eb-132">**Percent**</span></span> | <span data-ttu-id="4d5eb-133">النسبة المئوية للمبلغ.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-133">The percent amount.</span></span> <span data-ttu-id="4d5eb-134">لا يكون هذا الحقل نشطًا إلا في حالة تحديد راتب قدره % x في حقل كود التغطية.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-134">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="4d5eb-135">**المقسوم عليه**</span><span class="sxs-lookup"><span data-stu-id="4d5eb-135">**Divisor**</span></span> | <span data-ttu-id="4d5eb-136">القاسم الذي يتم استخدامه في الحساب عندما تقوم بتحديد كود التغطية راتب قدره % x.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-136">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="4d5eb-137">**النسبة المئوية الدنيا**</span><span class="sxs-lookup"><span data-stu-id="4d5eb-137">**Percent minimum**</span></span> | <span data-ttu-id="4d5eb-138">الحد الأدنى للنسبة المئوية عندما تحدد كود تغطية النسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-138">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="4d5eb-139">**النسبة المئوية القصوى**</span><span class="sxs-lookup"><span data-stu-id="4d5eb-139">**Percent maximum**</span></span> | <span data-ttu-id="4d5eb-140">الحد الأقصى للنسبة المئوية عندما تحدد كود تغطية النسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-140">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="4d5eb-141">ضمن **خيارات أهلية جهات الاتصال الشخصية**، قم بإرفاق خيار أهلية جهات الاتصال الشخصية المناسبة بكل خيار من خيارات التغطية.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-141">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="4d5eb-142">ضمن **الخدمة الذاتية**، حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="4d5eb-142">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="4d5eb-143">الحقل</span><span class="sxs-lookup"><span data-stu-id="4d5eb-143">Field</span></span> | <span data-ttu-id="4d5eb-144">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="4d5eb-144">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4d5eb-145">**السماح بمبلغ مساهمة الموظف**</span><span class="sxs-lookup"><span data-stu-id="4d5eb-145">**Allow employee contribution amount**</span></span> | <span data-ttu-id="4d5eb-146">يحدد ما إذا كان سيتم السماح للموظفين بتعديل مبلغ المساهمة في الخدمة الذاتية للميزات عندما يحددون ميزات.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-146">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="4d5eb-147">إذا قمت بتحديد خانة الاختيار هذه، فسيقوم النظام بحساب محددات خطة الميزة استنادًا إلى مبلغ المساهمة الذي يدخله الموظف في الخدمة الذاتية للميزات.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-147">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="4d5eb-148">**السماح بمبلغ تغطية الموظف**</span><span class="sxs-lookup"><span data-stu-id="4d5eb-148">**Allow employee coverage amount**</span></span> | <span data-ttu-id="4d5eb-149">يحدد ما إذا كان سيتم السماح للموظفين بتعديل مبلغ التغطية في الخدمة الذاتية للميزات عندما يحددون ميزات.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-149">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="4d5eb-150">إذا قمت بتحديد خانة الاختيار هذه، فسيقوم النظام بحساب محددات خطة الميزة استنادًا إلى مبلغ التغطية الذي يدخله الموظف في الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-150">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="4d5eb-151">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="4d5eb-151">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]