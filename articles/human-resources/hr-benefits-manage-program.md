---
title: تحديد وإدارة برنامج ميزات
description: توفر الموارد البشرية مجموعة من الأدوات التي يمكن استخدامها لإعداد وحفظ الميزات والخصومات وخطط تعويض العمال التي تقدمها مؤسسة أو تعالجها لعمالها. وتوفر هذه المقالة معلومات حول كيفية إعداد ميزات إدارة.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: c7ad8c6ee3450d57656f8c167ea8aa7554ac575a
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008023"
---
# <a name="define-and-manage-a-benefits-program"></a><span data-ttu-id="e47f8-104">تحديد وإدارة برنامج ميزات</span><span class="sxs-lookup"><span data-stu-id="e47f8-104">Define and manage a benefits program</span></span>

<span data-ttu-id="e47f8-105">توفر الموارد البشرية مجموعة من الأدوات التي يمكن استخدامها لإعداد وحفظ الميزات والخصومات وخطط تعويض العمال التي تقدمها مؤسسة أو تعالجها لعمالها.</span><span class="sxs-lookup"><span data-stu-id="e47f8-105">Human resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers.</span></span> <span data-ttu-id="e47f8-106">توفر هذه المقالة معلومات حول كيفية إعداد الميزات وإدارتها.</span><span class="sxs-lookup"><span data-stu-id="e47f8-106">This article provides information about how to set up and manage benefits.</span></span>

## <a name="benefit-setup"></a><span data-ttu-id="e47f8-107">إعداد الميزة‬</span><span class="sxs-lookup"><span data-stu-id="e47f8-107">Benefit setup</span></span>

<span data-ttu-id="e47f8-108">قبل أن يمكن تسجيل العمال في الميزات، يجب عليك إنشاء العناصر لكل ميزة.</span><span class="sxs-lookup"><span data-stu-id="e47f8-108">Before workers can be enrolled in benefits, you must create the elements of each benefit.</span></span> <span data-ttu-id="e47f8-109">وتشتمل هذه العناصر على خطط ميزات مماثلة وتحدد الإعدادات الافتراضية، مثل أسعار الخصم، وتفاصيل المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="e47f8-109">These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details.</span></span> <span data-ttu-id="e47f8-110">ويمكن ضبط العديد من هذه الإعدادات عند تسجيل العمال لاحقاً في الميزة.</span><span class="sxs-lookup"><span data-stu-id="e47f8-110">Many of these settings can be adjusted when workers are later enrolled in the benefit.</span></span> <span data-ttu-id="e47f8-111">وفي كل خطة ميزة، يمكن لمؤسسة تقديم عدة خيارات التسجيل، أو يمكن لعامل التنازل عن التسجيل في الخطة.</span><span class="sxs-lookup"><span data-stu-id="e47f8-111">For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan.</span></span> 

<span data-ttu-id="e47f8-112">[![تدفق عملية الميزات](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="e47f8-112">[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span></span>

## <a name="benefit-elements"></a><span data-ttu-id="e47f8-113">عناصر المزايا</span><span class="sxs-lookup"><span data-stu-id="e47f8-113">Benefit elements</span></span>

<span data-ttu-id="e47f8-114">قبل البدء في إنشاء ميزات وتسجيل العمال فيها، يجب عليك تحديد العناصر التي تشكل ميزة: النوع والخطة والخيارات.</span><span class="sxs-lookup"><span data-stu-id="e47f8-114">Before you begin to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.</span></span>

-   <span data-ttu-id="e47f8-115">**النوع** – مجموعة من الخطط لميزة محددة، مثل ميزة طبية أو ميزة خاصة بالانتظار.</span><span class="sxs-lookup"><span data-stu-id="e47f8-115">**Type** – A collection of plans for a specific benefit, such as medical or parking.</span></span>
-   <span data-ttu-id="e47f8-116">**الخطة** – ميزة محددة يتم التعاقد عليها من قِبل موفر.</span><span class="sxs-lookup"><span data-stu-id="e47f8-116">**Plan** – A specific benefit that is contracted from a provider.</span></span>
-   <span data-ttu-id="e47f8-117">**الخيار** – مستوى التغطية، مثل الموظف فقط أو الموظف وزوجته/شريكته.</span><span class="sxs-lookup"><span data-stu-id="e47f8-117">**Option** – The coverage level, such as employee only, or employee and spouse/partner.</span></span>

<span data-ttu-id="e47f8-118">في كل نوع من الميزات، مثل الرؤية أو علاج الأسنان، يمكن لمؤسسة توفير خطة واحدة أو أكثر لعمالها.</span><span class="sxs-lookup"><span data-stu-id="e47f8-118">For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers.</span></span> <span data-ttu-id="e47f8-119">في كل خطة، يمكن للمؤسسة تقديم خيارات مختلفة.</span><span class="sxs-lookup"><span data-stu-id="e47f8-119">For each plan, the organization can offer different options.</span></span> <span data-ttu-id="e47f8-120">على سبيل المثال، يمكن للعمال شراء تغطية تأمين على الحياة إضافية بما يعادل الراتب السنوي مرة واحدة أو مرتين أو ثلاثة.</span><span class="sxs-lookup"><span data-stu-id="e47f8-120">For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary.</span></span> <span data-ttu-id="e47f8-121">تصبح كل مجموعة تضمّ الخطة والخيارات ميزة يمكن للعمال التسجيل فيها.</span><span class="sxs-lookup"><span data-stu-id="e47f8-121">Each combination of a plan and options becomes a benefit that workers can enroll in.</span></span> 

<span data-ttu-id="e47f8-122">[![صورة الميزة](./media/benefit-pic.png)](./media/benefit-pic.png)</span><span class="sxs-lookup"><span data-stu-id="e47f8-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span></span>

## <a name="eligibility"></a><span data-ttu-id="e47f8-123">الاستحقاق</span><span class="sxs-lookup"><span data-stu-id="e47f8-123">Eligibility</span></span>
<span data-ttu-id="e47f8-124">تحدد عدة عوامل أهلية العامل لأنواع مختلفة من الميزات التي يقدم صاحب العمل.</span><span class="sxs-lookup"><span data-stu-id="e47f8-124">Many factors determine worker eligibility for the various types of benefits that an employer offers.</span></span> <span data-ttu-id="e47f8-125">وعند قيامك بإنشاء إحدى الميزات في Dynamics 365 Human Resources، يمكنك تعيين نوع الأهلية الذي ينطبق على هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="e47f8-125">When you create a benefit in Dynamics 365 Human Resources, you can set the type of eligibility that applies to that benefit.</span></span> 

<span data-ttu-id="e47f8-126">يمكنك توفير ميزة لجميع العمال.</span><span class="sxs-lookup"><span data-stu-id="e47f8-126">You can make a benefit available to all workers.</span></span> <span data-ttu-id="e47f8-127">على سبيل المثال، تقدم بعض الشركات مسارات وقوف السيارات لكافة الموظفين كإحدى الميزات الإضافية.‬</span><span class="sxs-lookup"><span data-stu-id="e47f8-127">For example, some companies offer parking passes to all employees as a fringe benefit.</span></span> <span data-ttu-id="e47f8-128">وعندما تقوم بإنشاء هذه الميزة، تقوم بتعيين الأهلية إلى **جميع العمال مؤهلون**.</span><span class="sxs-lookup"><span data-stu-id="e47f8-128">When you create this benefit, you set the eligibility to **All workers are eligible**.</span></span> 

<span data-ttu-id="e47f8-129">‏‫وفي الميزات الأخرى، مثل الزينة والرسوم الضريبية، لا يتم تطبيق الأهلية.</span><span class="sxs-lookup"><span data-stu-id="e47f8-129">For other benefits, such as garnishments and tax levies, eligibility doesn't apply.</span></span> <span data-ttu-id="e47f8-130">وعند إنشاء هذه الأنواع من الميزات، يمكنك تعيين الأهلية إلى **تجاوز عملية الأهلية**.</span><span class="sxs-lookup"><span data-stu-id="e47f8-130">Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**.</span></span> 

<span data-ttu-id="e47f8-131">‏‫وأخيراً، يمكن أن يقوم استحقاق الميزات على قاعدة.</span><span class="sxs-lookup"><span data-stu-id="e47f8-131">Finally, benefit eligibility can be rule-based.</span></span> <span data-ttu-id="e47f8-132">على سبيل المثال، تقدم شركة نوعين من ميزات التأمين على الحياة للموظفين.</span><span class="sxs-lookup"><span data-stu-id="e47f8-132">For example, a company offers two types of life insurance benefit to employees.</span></span> <span data-ttu-id="e47f8-133">والموظفون التنفيذيون مؤهلون لخطة التأمين على الحياة، بينما يكون جميع موظفي الدوام الكامل مؤهلين لخطة التأمين على الحياة الأخرى.</span><span class="sxs-lookup"><span data-stu-id="e47f8-133">Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan.</span></span> <span data-ttu-id="e47f8-134">في Human Resources، يمكنك إنشاء قاعدة استحقاق ميزة للبحث عن كافة الموظفين التنفيذيين وقاعدة أخرى للبحث عن جميع الموظفين بدوام كامل، ثم تطبيق هذه القواعد على الميزة المناسبة.</span><span class="sxs-lookup"><span data-stu-id="e47f8-134">In Human Resources, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.</span></span>

## <a name="enrollment"></a><span data-ttu-id="e47f8-135">التسجيل</span><span class="sxs-lookup"><span data-stu-id="e47f8-135">Enrollment</span></span>
<span data-ttu-id="e47f8-136">بعد إنشاء الميزات التي تقدمها المؤسسة الخاصة بك وتحديد الأهلية، يمكنك تسجيل العاملين في الميزات.</span><span class="sxs-lookup"><span data-stu-id="e47f8-136">After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits.</span></span> <span data-ttu-id="e47f8-137">ويمكنك تسجيل عامل واحد في الميزات، أو يمكنك تسجيل العديد من العمال في ميزة واحدة أو أكثر أثناء عملية واحدة.</span><span class="sxs-lookup"><span data-stu-id="e47f8-137">You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process.</span></span> 

<span data-ttu-id="e47f8-138">وفي بعض الأحيان، تتوقف المؤسسة عن تقديم بعض الميزات.</span><span class="sxs-lookup"><span data-stu-id="e47f8-138">Sometimes, an organization stops offering certain benefits.</span></span> <span data-ttu-id="e47f8-139">في هذه الحالة، يجب عليك تحديث الميزة والعاملين المسجلين فيها.</span><span class="sxs-lookup"><span data-stu-id="e47f8-139">In this case, you must update the benefit and the workers who are enrolled in.</span></span> <span data-ttu-id="e47f8-140">ويتيح لك انتهاء صلاحية الميزات الجماعي تغيير تاريخ انتهاء صلاحية كلٍّ من الميزة وعمليات تسجيل العمال لهذه الميزة في الوقت نفسه.‬</span><span class="sxs-lookup"><span data-stu-id="e47f8-140">Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time.</span></span> <span data-ttu-id="e47f8-141">يمكنك أيضا تحديد عدة عاملين مسجلون في ميزة وتغيير تاريخ الانتهاء لتغطيتها.</span><span class="sxs-lookup"><span data-stu-id="e47f8-141">You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage.</span></span> 

<span data-ttu-id="e47f8-142">وبالمثل، يتيح لك تمديد الميزات الجماعي إمكانية تمديد تاريخ انتهاء صلاحية لكلٍّ من الميزة وعمليات تسجيل العمال لهذه الميزة، إذا قررت تقديم ميزة لمدة أطول من المدة المخطط لها في الأصل.</span><span class="sxs-lookup"><span data-stu-id="e47f8-142">Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.</span></span>

