---
title: إنشاء خطط المزايا الخاصة بالعامل
description: يمكنك إنشاء خطط المزايا الخاصة بالعامل في Microsoft Dynamics 365 Human Resources لتحديد خطط المزايا للموظفين ولتأكيد تحديدات خطة الميزة.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitPlanEmployee, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2083d3b18621ec7759b658b5ec34f2371c2ea1df
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111376"
---
# <a name="create-worker-benefit-plans"></a><span data-ttu-id="33779-103">إنشاء خطط المزايا الخاصة بالعامل</span><span class="sxs-lookup"><span data-stu-id="33779-103">Create worker benefit plans</span></span>

<span data-ttu-id="33779-104">يمكنك إنشاء خطط المزايا الخاصة بالعامل في Microsoft Dynamics 365 Human Resources لتحديد خطط المزايا للموظفين ولتأكيد تحديدات خطة الميزة.</span><span class="sxs-lookup"><span data-stu-id="33779-104">You can create worker benefit plans in Microsoft Dynamics 365 Human Resources to select benefit plans for employees and to confirm benefit plan selections.</span></span> <span data-ttu-id="33779-105">عادةً ما يقوم الموظفون بتحديد خطط المزايا بأنفسهم باستخدام الخدمة الذاتية للموظف، ثم يقوم مسؤول المزايا بتأكيد الاختيارات.</span><span class="sxs-lookup"><span data-stu-id="33779-105">Typically, employees select benefit plans themselves by using Employee self service, and then a benefits administrator confirms the selections.</span></span> 

1. <span data-ttu-id="33779-106">في مساحة العمل **إدارة المزايا**، ضمن **الخطط**، حدد **خطط المزايا الخاصة بالعامل**.</span><span class="sxs-lookup"><span data-stu-id="33779-106">In the **Benefits management** workspace, under **Plans**, select **Worker benefit plans**.</span></span>

2. <span data-ttu-id="33779-107">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="33779-107">Select **New**.</span></span>

3. <span data-ttu-id="33779-108">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="33779-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="33779-109">الحقل</span><span class="sxs-lookup"><span data-stu-id="33779-109">Field</span></span> | <span data-ttu-id="33779-110">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="33779-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="33779-111">الفترة</span><span class="sxs-lookup"><span data-stu-id="33779-111">Period</span></span> | <span data-ttu-id="33779-112">يحدد فتره المزايا لاستخدامها لتصفية الخطط في علامة التبويب السريعة للخطط. ثم قم بتصفية الخطط لمساعدتك في تحديد مجموعة فرعية لكافة سجلات الخطط حتى تتمكن من تأكيد المجموعة الفرعية.</span><span class="sxs-lookup"><span data-stu-id="33779-112">Specifies a benefits period to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> <span data-ttu-id="33779-113">على سبيل المثال، حدد الفترة التي قمت بإنشاءها باسم 2015 لتأكيد كافة تحديدات تسجيل الميزات الخاصة بعام 2015.</span><span class="sxs-lookup"><span data-stu-id="33779-113">For example, select a period you created called 2015 to confirm all the benefit enrollment selections for 2015.</span></span> |
   | <span data-ttu-id="33779-114">العامل</span><span class="sxs-lookup"><span data-stu-id="33779-114">Worker</span></span> | <span data-ttu-id="33779-115">يحدد العامل لاستخدامه لتصفية الخطط في علامة التبويب السريعة للخطط. ثم قم بتصفية الخطط لمساعدتك في تحديد مجموعة فرعية لكافة سجلات الخطط حتى تتمكن من تأكيد المجموعة الفرعية.</span><span class="sxs-lookup"><span data-stu-id="33779-115">Specifies a worker to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="33779-116">كيان قانوني</span><span class="sxs-lookup"><span data-stu-id="33779-116">Legal entity</span></span> | <span data-ttu-id="33779-117">يحدد الكيان القانوني لاستخدامه لتصفية الخطط في علامة التبويب السريعة للخطط. ثم قم بتصفية الخطط لمساعدتك في تحديد مجموعة فرعية لكافة سجلات الخطط حتى تتمكن من تأكيد المجموعة الفرعية.</span><span class="sxs-lookup"><span data-stu-id="33779-117">Specifies a legal entity to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="33779-118">خيار التغطية</span><span class="sxs-lookup"><span data-stu-id="33779-118">Coverage option</span></span> | <span data-ttu-id="33779-119">يحدد خيار التغطية لاستخدامه لتصفية الخطط في علامة التبويب السريعة للخطط. ثم قم بتصفية الخطط لمساعدتك في تحديد مجموعة فرعية لكافة سجلات الخطط حتى تتمكن من تأكيد المجموعة الفرعية.</span><span class="sxs-lookup"><span data-stu-id="33779-119">Specifies a coverage option to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="33779-120">افتراضية</span><span class="sxs-lookup"><span data-stu-id="33779-120">Default</span></span> | <span data-ttu-id="33779-121">يقوم بتصفية خطط الميزات استنادًا إلى ما إذا كانت هي خطة افتراضية أم لا.</span><span class="sxs-lookup"><span data-stu-id="33779-121">Filters the benefit plans based on whether they are a default plan.</span></span> <span data-ttu-id="33779-122">قم بتصفية الخطط لمساعدتك في تحديد مجموعة فرعية من جميع سجلات الخطة حتى تتمكن من تأكيد المجموعة الفرعية.</span><span class="sxs-lookup"><span data-stu-id="33779-122">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="33779-123">الحالة</span><span class="sxs-lookup"><span data-stu-id="33779-123">Status</span></span> | <span data-ttu-id="33779-124">تصفيه خطط الميزات استنادًا إلى حالتها.</span><span class="sxs-lookup"><span data-stu-id="33779-124">Filters benefit plans based on their status.</span></span> <span data-ttu-id="33779-125">قم بتصفية الخطط لمساعدتك في تحديد مجموعة فرعية من جميع سجلات الخطة حتى تتمكن من تأكيد المجموعة الفرعية.</span><span class="sxs-lookup"><span data-stu-id="33779-125">Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="33779-126">التأكيد</span><span class="sxs-lookup"><span data-stu-id="33779-126">Confirmation</span></span> | <span data-ttu-id="33779-127">حدد حالة التأكيد لاستخدامه لتصفية الخطط في علامة التبويب السريعة للخطط. ثم قم بتصفية الخطط لمساعدتك في تحديد مجموعة فرعية لكافة سجلات الخطط حتى تتمكن من تأكيد المجموعة الفرعية.</span><span class="sxs-lookup"><span data-stu-id="33779-127">Specifies the confirmation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="33779-128">إلغاء</span><span class="sxs-lookup"><span data-stu-id="33779-128">Cancellation</span></span> | <span data-ttu-id="33779-129">يحدد حالة الإلغاء لاستخدامه لتصفية الخطط في علامة التبويب السريعة للخطط. ثم قم بتصفية الخطط لمساعدتك في تحديد مجموعةفرعية لكافة سجلات الخطط حتى تتمكن من تأكيد المجموعة الفرعية.</span><span class="sxs-lookup"><span data-stu-id="33779-129">Specifies the cancellation status to use to filter the plans in the Plans fast tab. Filter the plans to help you select a subset of all the plan records so that you can confirm the subset.</span></span> |
   | <span data-ttu-id="33779-130">تصفية تاريخ السريان</span><span class="sxs-lookup"><span data-stu-id="33779-130">Effective date filter</span></span> | <span data-ttu-id="33779-131">قم بتصفية الخطط استنادًا إلى ما إذا كانت منتهية الصلاحية أو نشطة أو ستكون نشطة في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="33779-131">Filters the plans based on whether they’re expired, active, or will be active in the future.</span></span> <span data-ttu-id="33779-132">حدد خانات الاختيار الموافقة للخطط التي ترغب في مشاهدتها في علامة التبويب السريعة الخطط.</span><span class="sxs-lookup"><span data-stu-id="33779-132">Select the check boxes that correspond to the plans you want to see in the Plans fast tab.</span></span> |
   | <span data-ttu-id="33779-133">الخطط</span><span class="sxs-lookup"><span data-stu-id="33779-133">Plans</span></span> | <span data-ttu-id="33779-134">تحتوي علامة التبويب السريعة "الخطط" علي الخطط التي تتوافق مع معايير التصفية التي قمت بتحديدها.</span><span class="sxs-lookup"><span data-stu-id="33779-134">The Plans fast tab contains the plans that meet the filter criteria you specified.</span></span> <span data-ttu-id="33779-135">يتم تضمين خيارات التكوين ذات الصلة التي تم تعيينها بواسطة موظفي الموارد البشرية وتحديدات التسجيل التي تم اختيارها من قبل الموظفين في كل بند.</span><span class="sxs-lookup"><span data-stu-id="33779-135">The relevant configuration options that were set by HR staff and the enrollment selections that were chosen by employees are included on each line.</span></span> <span data-ttu-id="33779-136">يحدد الحقل المؤهل ما إذا كان هناك تعارض في التحقق من الصحة مع تحديد الخطة.</span><span class="sxs-lookup"><span data-stu-id="33779-136">The Qualified field specifies whether there is a validation conflict with the plan selection.</span></span> |

4. <span data-ttu-id="33779-137">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="33779-137">Select **Save**.</span></span>
