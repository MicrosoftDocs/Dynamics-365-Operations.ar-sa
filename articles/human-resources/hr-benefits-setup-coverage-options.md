---
title: إنشاء خيارات تغطية
description: تُعد خيارات التغطية في Microsoft Dynamics 365 Human Resources مستويات التغطية لاختيار المشارك في خطة أو برنامج الميزة، مثل الموظف فقط لخطة طبية أو مضاعفة راتب لخطة التأمين على الحياة.
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
ms.openlocfilehash: 0af2b6ae0853b4c7f64c4d4f04299c87089d622b
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092696"
---
# <a name="create-coverage-options"></a><span data-ttu-id="cfb9f-103">إنشاء خيارات تغطية</span><span class="sxs-lookup"><span data-stu-id="cfb9f-103">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="cfb9f-104">تُعد خيارات التغطية في Microsoft Dynamics 365 Human Resources مستويات التغطية لاختيار المشارك في خطة أو برنامج الميزة، مثل الموظف فقط لخطة طبية أو مضاعفة راتب لخطة التأمين على الحياة.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="cfb9f-105">وبمجرد التحديد، تتم إعادة استخدام خيارات تغطية الميزة ويمكن ربط خيار بخطة واحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-105">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="cfb9f-106">بمجرد تحديد خيارات التغطية، قم بإرفاق خيارات التغطية بنوع خطة الميزة.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-106">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="cfb9f-107">ثم يتم إقران نوع الخطة بنوع خطة أو برنامج الميزة.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-107">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="cfb9f-108">ستكون خيارات التغطية المقترنة بنوع الخطة متاحة لكافة الخطط التي يتم إنشاؤها باستخدام نوع الخطة هذا.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-108">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="cfb9f-109">في مساحة العمل **إدارة الميزات**، ضمن **إعداد**، حدد **خيارات التغطية**.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-109">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="cfb9f-110">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-110">Select **New**.</span></span>

3. <span data-ttu-id="cfb9f-111">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="cfb9f-111">Specify values for the following fields:</span></span>

   | <span data-ttu-id="cfb9f-112">الحقل</span><span class="sxs-lookup"><span data-stu-id="cfb9f-112">Field</span></span> | <span data-ttu-id="cfb9f-113">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="cfb9f-113">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="cfb9f-114">**خيار التغطية**</span><span class="sxs-lookup"><span data-stu-id="cfb9f-114">**Coverage option**</span></span> | <span data-ttu-id="cfb9f-115">اسم خيار تغطية فريد.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-115">A unique coverage option name.</span></span> |
   | <span data-ttu-id="cfb9f-116">**‏‏الوصف**</span><span class="sxs-lookup"><span data-stu-id="cfb9f-116">**Description**</span></span> | <span data-ttu-id="cfb9f-117">وصف خيار التغطية.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-117">A description of the coverage option.</span></span> |
   | <span data-ttu-id="cfb9f-118">**كود التغطية**</span><span class="sxs-lookup"><span data-stu-id="cfb9f-118">**Coverage code**</span></span> | <span data-ttu-id="cfb9f-119">تعمل أكواد التغطية على تعيين الحد الأدنى والأقصى للمبالغ لكل نوع شخص مغطى مؤهل.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-119">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="cfb9f-120">يشير كود التغطية إلى الشخص الذي تمت تغطيته أو مبلغ التغطية المسموح به لنوع الخطة.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-120">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="cfb9f-121">يمكنك التعبير عن مبلغ التغطية كمبلغًا بالدولار أو بالنسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-121">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="cfb9f-122">على سبيل المثال:</span><span class="sxs-lookup"><span data-stu-id="cfb9f-122">For example:</span></span></br></br><span data-ttu-id="cfb9f-123">- **موظف+1** – ليكون مؤهلاً، يجب على الموظف أن يحدد معال واحد (إذا تم تحديد أكثر من معال، لن يكون مؤهلاً بعد ذلك).</span><span class="sxs-lookup"><span data-stu-id="cfb9f-123">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="cfb9f-124">- **موظف + الأسرة** – ليكون مؤهلاً، يجب على الموظف أن يحدد معالين على الأقل.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-124">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="cfb9f-125">**أقصى عدد**</span><span class="sxs-lookup"><span data-stu-id="cfb9f-125">**Maximum number**</span></span> | <span data-ttu-id="cfb9f-126">الحد الأقصى لعدد المعالين.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-126">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="cfb9f-127">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="cfb9f-127">**Status**</span></span> | <span data-ttu-id="cfb9f-128">حالة خيار التغطية.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-128">The status of the coverage option.</span></span> <span data-ttu-id="cfb9f-129">في حالة تعيين حالة خيار التغطية على "غير نشط"، فإنه يتعذر تحديد خيار التغطية في أنواع الخطط.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-129">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="cfb9f-130">**النسبة المئوية**</span><span class="sxs-lookup"><span data-stu-id="cfb9f-130">**Percent**</span></span> | <span data-ttu-id="cfb9f-131">النسبة المئوية للمبلغ.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-131">The percent amount.</span></span> <span data-ttu-id="cfb9f-132">لا يكون هذا الحقل نشطًا إلا في حالة تحديد راتب قدره % x في حقل كود التغطية.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-132">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="cfb9f-133">**المقسوم عليه**</span><span class="sxs-lookup"><span data-stu-id="cfb9f-133">**Divisor**</span></span> | <span data-ttu-id="cfb9f-134">القاسم الذي يتم استخدامه في الحساب عندما تقوم بتحديد كود التغطية راتب قدره % x.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-134">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="cfb9f-135">**النسبة المئوية الدنيا**</span><span class="sxs-lookup"><span data-stu-id="cfb9f-135">**Percent minimum**</span></span> | <span data-ttu-id="cfb9f-136">الحد الأدنى للنسبة المئوية عندما تحدد كود تغطية النسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-136">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="cfb9f-137">**النسبة المئوية القصوى**</span><span class="sxs-lookup"><span data-stu-id="cfb9f-137">**Percent maximum**</span></span> | <span data-ttu-id="cfb9f-138">الحد الأقصى للنسبة المئوية عندما تحدد كود تغطية النسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-138">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="cfb9f-139">ضمن **خيارات أهلية جهات الاتصال الشخصية**، قم بإرفاق خيار أهلية جهات الاتصال الشخصية المناسبة بكل خيار من خيارات التغطية.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-139">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="cfb9f-140">ضمن **الخدمة الذاتية**، حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="cfb9f-140">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="cfb9f-141">الحقل</span><span class="sxs-lookup"><span data-stu-id="cfb9f-141">Field</span></span> | <span data-ttu-id="cfb9f-142">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="cfb9f-142">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="cfb9f-143">**السماح بمبلغ مساهمة الموظف**</span><span class="sxs-lookup"><span data-stu-id="cfb9f-143">**Allow employee contribution amount**</span></span> | <span data-ttu-id="cfb9f-144">يحدد ما إذا كان سيتم السماح للموظفين بتعديل مبلغ المساهمة في الخدمة الذاتية للميزات عندما يحددون ميزات.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-144">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="cfb9f-145">إذا قمت بتحديد خانة الاختيار هذه، فسيقوم النظام بحساب محددات خطة الميزة استنادًا إلى مبلغ المساهمة الذي يدخله الموظف في الخدمة الذاتية للميزات.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-145">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="cfb9f-146">**السماح بمبلغ تغطية الموظف**</span><span class="sxs-lookup"><span data-stu-id="cfb9f-146">**Allow employee coverage amount**</span></span> | <span data-ttu-id="cfb9f-147">يحدد ما إذا كان سيتم السماح للموظفين بتعديل مبلغ التغطية في الخدمة الذاتية للميزات عندما يحددون ميزات.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-147">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="cfb9f-148">إذا قمت بتحديد خانة الاختيار هذه، فسيقوم النظام بحساب محددات خطة الميزة استنادًا إلى مبلغ التغطية الذي يدخله الموظف في الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-148">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="cfb9f-149">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="cfb9f-149">Select **Save**.</span></span> 
