---
title: إنشاء خيارات تغطية
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
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007904"
---
# <a name="create-coverage-options"></a><span data-ttu-id="9d928-102">إنشاء خيارات تغطية</span><span class="sxs-lookup"><span data-stu-id="9d928-102">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="9d928-103">تُعد خيارات التغطية في Microsoft Dynamics 365 Human Resources مستويات التغطية لاختيار المشارك في خطة أو برنامج الميزة، مثل الموظف فقط لخطة طبية أو مضاعفة راتب لخطة التأمين على الحياة.</span><span class="sxs-lookup"><span data-stu-id="9d928-103">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="9d928-104">وبمجرد التحديد، تتم إعادة استخدام خيارات تغطية الميزة ويمكن ربط خيار بخطة واحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="9d928-104">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="9d928-105">بمجرد تحديد خيارات التغطية، قم بإرفاق خيارات التغطية بنوع خطة الميزة.</span><span class="sxs-lookup"><span data-stu-id="9d928-105">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="9d928-106">ثم يتم إقران نوع الخطة بنوع خطة أو برنامج الميزة.</span><span class="sxs-lookup"><span data-stu-id="9d928-106">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="9d928-107">ستكون خيارات التغطية المقترنة بنوع الخطة متاحة لكافة الخطط التي يتم إنشاؤها باستخدام نوع الخطة هذا.</span><span class="sxs-lookup"><span data-stu-id="9d928-107">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="9d928-108">في مساحة العمل **إدارة الميزات**، ضمن **إعداد**، حدد **خيارات التغطية**.</span><span class="sxs-lookup"><span data-stu-id="9d928-108">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="9d928-109">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9d928-109">Select **New**.</span></span>

3. <span data-ttu-id="9d928-110">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="9d928-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="9d928-111">الحقل</span><span class="sxs-lookup"><span data-stu-id="9d928-111">Field</span></span> | <span data-ttu-id="9d928-112">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="9d928-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9d928-113">**خيار التغطية**</span><span class="sxs-lookup"><span data-stu-id="9d928-113">**Coverage option**</span></span> | <span data-ttu-id="9d928-114">اسم خيار تغطية فريد.</span><span class="sxs-lookup"><span data-stu-id="9d928-114">A unique coverage option name.</span></span> |
   | <span data-ttu-id="9d928-115">**‏‏الوصف**</span><span class="sxs-lookup"><span data-stu-id="9d928-115">**Description**</span></span> | <span data-ttu-id="9d928-116">وصف خيار التغطية.</span><span class="sxs-lookup"><span data-stu-id="9d928-116">A description of the coverage option.</span></span> |
   | <span data-ttu-id="9d928-117">**كود التغطية**</span><span class="sxs-lookup"><span data-stu-id="9d928-117">**Coverage code**</span></span> | <span data-ttu-id="9d928-118">تعمل أكواد التغطية على تعيين الحد الأدنى والأقصى للمبالغ لكل نوع شخص مغطى مؤهل.</span><span class="sxs-lookup"><span data-stu-id="9d928-118">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="9d928-119">يشير كود التغطية إلى الشخص الذي تمت تغطيته أو مبلغ التغطية المسموح به لنوع الخطة.</span><span class="sxs-lookup"><span data-stu-id="9d928-119">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="9d928-120">يمكنك التعبير عن مبلغ التغطية كمبلغًا بالدولار أو بالنسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="9d928-120">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="9d928-121">على سبيل المثال:</span><span class="sxs-lookup"><span data-stu-id="9d928-121">For example:</span></span></br></br><span data-ttu-id="9d928-122">- **موظف+1** – ليكون مؤهلاً، يجب على الموظف أن يحدد معال واحد (إذا تم تحديد أكثر من معال، لن يكون مؤهلاً بعد ذلك).</span><span class="sxs-lookup"><span data-stu-id="9d928-122">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="9d928-123">- **موظف + الأسرة** – ليكون مؤهلاً، يجب على الموظف أن يحدد معالين على الأقل.</span><span class="sxs-lookup"><span data-stu-id="9d928-123">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="9d928-124">**أقصى عدد**</span><span class="sxs-lookup"><span data-stu-id="9d928-124">**Maximum number**</span></span> | <span data-ttu-id="9d928-125">الحد الأقصى لعدد المعالين.</span><span class="sxs-lookup"><span data-stu-id="9d928-125">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="9d928-126">**الحالة**</span><span class="sxs-lookup"><span data-stu-id="9d928-126">**Status**</span></span> | <span data-ttu-id="9d928-127">حالة خيار التغطية.</span><span class="sxs-lookup"><span data-stu-id="9d928-127">The status of the coverage option.</span></span> <span data-ttu-id="9d928-128">في حالة تعيين حالة خيار التغطية على "غير نشط"، فإنه يتعذر تحديد خيار التغطية في أنواع الخطط.</span><span class="sxs-lookup"><span data-stu-id="9d928-128">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="9d928-129">**النسبة المئوية**</span><span class="sxs-lookup"><span data-stu-id="9d928-129">**Percent**</span></span> | <span data-ttu-id="9d928-130">النسبة المئوية للمبلغ.</span><span class="sxs-lookup"><span data-stu-id="9d928-130">The percent amount.</span></span> <span data-ttu-id="9d928-131">لا يكون هذا الحقل نشطًا إلا في حالة تحديد راتب قدره % x في حقل كود التغطية.</span><span class="sxs-lookup"><span data-stu-id="9d928-131">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="9d928-132">**المقسوم عليه**</span><span class="sxs-lookup"><span data-stu-id="9d928-132">**Divisor**</span></span> | <span data-ttu-id="9d928-133">القاسم الذي يتم استخدامه في الحساب عندما تقوم بتحديد كود التغطية راتب قدره % x.</span><span class="sxs-lookup"><span data-stu-id="9d928-133">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="9d928-134">**النسبة المئوية الدنيا**</span><span class="sxs-lookup"><span data-stu-id="9d928-134">**Percent minimum**</span></span> | <span data-ttu-id="9d928-135">الحد الأدنى للنسبة المئوية عندما تحدد كود تغطية النسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="9d928-135">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="9d928-136">**النسبة المئوية القصوى**</span><span class="sxs-lookup"><span data-stu-id="9d928-136">**Percent maximum**</span></span> | <span data-ttu-id="9d928-137">الحد الأقصى للنسبة المئوية عندما تحدد كود تغطية النسبة المئوية.</span><span class="sxs-lookup"><span data-stu-id="9d928-137">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="9d928-138">ضمن **خيارات أهلية جهات الاتصال الشخصية**، قم بإرفاق خيار أهلية جهات الاتصال الشخصية المناسبة بكل خيار من خيارات التغطية.</span><span class="sxs-lookup"><span data-stu-id="9d928-138">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="9d928-139">ضمن **الخدمة الذاتية**، حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="9d928-139">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="9d928-140">الحقل</span><span class="sxs-lookup"><span data-stu-id="9d928-140">Field</span></span> | <span data-ttu-id="9d928-141">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="9d928-141">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9d928-142">**السماح بمبلغ مساهمة الموظف**</span><span class="sxs-lookup"><span data-stu-id="9d928-142">**Allow employee contribution amount**</span></span> | <span data-ttu-id="9d928-143">يحدد ما إذا كان سيتم السماح للموظفين بتعديل مبلغ المساهمة في الخدمة الذاتية للميزات عندما يحددون ميزات.</span><span class="sxs-lookup"><span data-stu-id="9d928-143">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="9d928-144">إذا قمت بتحديد خانة الاختيار هذه، فسيقوم النظام بحساب محددات خطة الميزة استنادًا إلى مبلغ المساهمة الذي يدخله الموظف في الخدمة الذاتية للميزات.</span><span class="sxs-lookup"><span data-stu-id="9d928-144">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="9d928-145">**السماح بمبلغ تغطية الموظف**</span><span class="sxs-lookup"><span data-stu-id="9d928-145">**Allow employee coverage amount**</span></span> | <span data-ttu-id="9d928-146">يحدد ما إذا كان سيتم السماح للموظفين بتعديل مبلغ التغطية في الخدمة الذاتية للميزات عندما يحددون ميزات.</span><span class="sxs-lookup"><span data-stu-id="9d928-146">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="9d928-147">إذا قمت بتحديد خانة الاختيار هذه، فسيقوم النظام بحساب محددات خطة الميزة استنادًا إلى مبلغ التغطية الذي يدخله الموظف في الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="9d928-147">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="9d928-148">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9d928-148">Select **Save**.</span></span> 
