---
title: ما الجديد أو المتغير في Dynamics 365 Talent - Core HR(10 سبتمبر 2018)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: ff5d21a8a71b068a276bedaf6e4b9964adcb4027
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896740"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-10-2018"></a><span data-ttu-id="7b009-103">ما الجديد أو المتغير في Dynamics 365 Talent - Core HR(10 سبتمبر 2018)</span><span class="sxs-lookup"><span data-stu-id="7b009-103">What's new or changed in Dynamics 365 Talent - Core HR (September 10, 2018)</span></span>

<span data-ttu-id="7b009-104">**الإصدار 8.1.138.0**</span><span class="sxs-lookup"><span data-stu-id="7b009-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="7b009-105">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent: Core HR.</span><span class="sxs-lookup"><span data-stu-id="7b009-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 Talent: Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="7b009-106">السماح بوقت معين في اليوم في طلبات الإجازات (أنصاف الأيام)</span><span class="sxs-lookup"><span data-stu-id="7b009-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="7b009-107">إذا تم إعداد الإجازة والغياب بحيث يُرسل زمن التوقف بالأيام، يمكن الآن أيضًا تمكين تعريف نصف اليوم.</span><span class="sxs-lookup"><span data-stu-id="7b009-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="7b009-108">وبعد ذلك، عندما يقوم المستخدمون بإرسال طلبات زمن التوقف،  يمكنهم تحديد إذا ما كان ذلك يعني قيامهم بطلب النصف الأول أو النصف الثاني من يوم الإجازة.</span><span class="sxs-lookup"><span data-stu-id="7b009-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="7b009-109">يتم إيقاف تشغيل هذا الخيار افتراضيًا.</span><span class="sxs-lookup"><span data-stu-id="7b009-109">By default, this option is turned off.</span></span> <span data-ttu-id="7b009-110">بالنسبة للموظفين الذين يطلبون النص الأول أو النصف الثاني من اليوم إجازة، يجب عليك تشغيل هذا الخيار في منطقة **الإجازة والغياب** لمُحددات الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="7b009-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="7b009-111">امتياز الأمان لهذه الميزة هو الاحتفاظ بمحددات الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="7b009-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="7b009-112">التحقق من إدخالات الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="7b009-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="7b009-113">بناءً عل كيفية تكوين الإجازة، يتلقى الموظفون الذي يحاولون إرسال طلب إجازة أطول من يوم العمل الخاصة بهم، رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="7b009-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="7b009-114">بمعنى آخر، يتم تحذيرهم إذا حاولوا أخذ أكثر من يوم كامل إجازة في أي تاريخ محدد.</span><span class="sxs-lookup"><span data-stu-id="7b009-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="7b009-115">يتم دائمًا تشغيل ميزة التحقق من الصحة هذه.</span><span class="sxs-lookup"><span data-stu-id="7b009-115">This validation is always turned on.</span></span> <span data-ttu-id="7b009-116">في أي وقت يتجاوز الموظف حد اليوم المُحدد، يتلقي تحذير في طلب الإجازة الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="7b009-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="7b009-117">حقول إضافية للعبارات الشرطية في مهام سير العمل.</span><span class="sxs-lookup"><span data-stu-id="7b009-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="7b009-118">تمت إضافة حقول إضافية إلى العبارات الشرطية وعناصر نائبة لمهام سير عمل متعددة في Core HR.</span><span class="sxs-lookup"><span data-stu-id="7b009-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="7b009-119">تمت إضافة الحقول التالية إلى عمليات سير عمل التعويض والإنهاء والنقل:</span><span class="sxs-lookup"><span data-stu-id="7b009-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="7b009-120">EmploymentType</span><span class="sxs-lookup"><span data-stu-id="7b009-120">EmploymentType</span></span>
- <span data-ttu-id="7b009-121">LegalEntity</span><span class="sxs-lookup"><span data-stu-id="7b009-121">LegalEntity</span></span>
- <span data-ttu-id="7b009-122">AdjustedWorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="7b009-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="7b009-123">EmployerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="7b009-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="7b009-124">EmployerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="7b009-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="7b009-125"> TransitionDate</span><span class="sxs-lookup"><span data-stu-id="7b009-125">TransitionDate</span></span>
- <span data-ttu-id="7b009-126">WorkerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="7b009-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="7b009-127">WorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="7b009-127">WorkerStartDate</span></span>
- <span data-ttu-id="7b009-128">WorkerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="7b009-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="7b009-129">ProbationEndDate</span><span class="sxs-lookup"><span data-stu-id="7b009-129">ProbationEndDate</span></span>
- <span data-ttu-id="7b009-130">المهنة</span><span class="sxs-lookup"><span data-stu-id="7b009-130">Position</span></span>
- <span data-ttu-id="7b009-131">الاتحاد</span><span class="sxs-lookup"><span data-stu-id="7b009-131">Union</span></span>
- <span data-ttu-id="7b009-132">القسم</span><span class="sxs-lookup"><span data-stu-id="7b009-132">Department</span></span>
- <span data-ttu-id="7b009-133">PositionType</span><span class="sxs-lookup"><span data-stu-id="7b009-133">PositionType</span></span>
- <span data-ttu-id="7b009-134">CompLocation</span><span class="sxs-lookup"><span data-stu-id="7b009-134">CompLocation</span></span>
- <span data-ttu-id="7b009-135">المسمى الوظيفي</span><span class="sxs-lookup"><span data-stu-id="7b009-135">Title</span></span>
- <span data-ttu-id="7b009-136">وظيفة</span><span class="sxs-lookup"><span data-stu-id="7b009-136">Job</span></span>
- <span data-ttu-id="7b009-137">JobType</span><span class="sxs-lookup"><span data-stu-id="7b009-137">JobType</span></span>
- <span data-ttu-id="7b009-138">JobFamily</span><span class="sxs-lookup"><span data-stu-id="7b009-138">JobFamily</span></span>
- <span data-ttu-id="7b009-139">JobFunction</span><span class="sxs-lookup"><span data-stu-id="7b009-139">JobFunction</span></span>

<span data-ttu-id="7b009-140">تمت إضافة الحقول التالية إلى سير عمل المنصب:</span><span class="sxs-lookup"><span data-stu-id="7b009-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="7b009-141">المهنة</span><span class="sxs-lookup"><span data-stu-id="7b009-141">Position</span></span>
- <span data-ttu-id="7b009-142">الاتحاد</span><span class="sxs-lookup"><span data-stu-id="7b009-142">Union</span></span>
- <span data-ttu-id="7b009-143">القسم</span><span class="sxs-lookup"><span data-stu-id="7b009-143">Department</span></span>
- <span data-ttu-id="7b009-144">PositionType</span><span class="sxs-lookup"><span data-stu-id="7b009-144">PositionType</span></span>
- <span data-ttu-id="7b009-145">CompLocation</span><span class="sxs-lookup"><span data-stu-id="7b009-145">CompLocation</span></span>
- <span data-ttu-id="7b009-146">المسمى الوظيفي</span><span class="sxs-lookup"><span data-stu-id="7b009-146">Title</span></span>
- <span data-ttu-id="7b009-147">وظيفة</span><span class="sxs-lookup"><span data-stu-id="7b009-147">Job</span></span>
- <span data-ttu-id="7b009-148">JobType</span><span class="sxs-lookup"><span data-stu-id="7b009-148">JobType</span></span>
- <span data-ttu-id="7b009-149">JobFamily</span><span class="sxs-lookup"><span data-stu-id="7b009-149">JobFamily</span></span>
- <span data-ttu-id="7b009-150">JobFunction</span><span class="sxs-lookup"><span data-stu-id="7b009-150">JobFunction</span></span>

<span data-ttu-id="7b009-151">تتوفر الحقول في العبارات الشرطية والعناصر النائبة لجميع المستخدمين الذين لديهم صلاحية الوصول لتكوين عمليات سير العمل المذكورة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="7b009-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="7b009-152">الانتقال إلى Attract من إدارة الموظفين</span><span class="sxs-lookup"><span data-stu-id="7b009-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="7b009-153">في إدارة الموظفين، إذا لم يتم إعداد Attract، فمن ثم يوجه قسم**المرشحون المُراد توظيفهم** البدء باستخدام Attract بدلًا من عرض الرسالة "لم يتم العثور على أي شئ لعرضه هنا."</span><span class="sxs-lookup"><span data-stu-id="7b009-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="7b009-154">التغييرات الأخرى</span><span class="sxs-lookup"><span data-stu-id="7b009-154">Other changes</span></span>

<span data-ttu-id="7b009-155">يشمل هذا الإصدار عددًا من إصلاحات الأخطاء الإضافية:</span><span class="sxs-lookup"><span data-stu-id="7b009-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="7b009-156">عند توظيف مقاول، يجب ألا تتوافر علامة تبويب**التعويض** على صفحة الطلب/الإجراء.</span><span class="sxs-lookup"><span data-stu-id="7b009-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="7b009-157">أثناء عملية إنهاء لطلب، لا يمكنك المتابعة حتى تحتوي كافة الحقول المطلوبة على بيانات.</span><span class="sxs-lookup"><span data-stu-id="7b009-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="7b009-158">تمت معالجة مشاكل ترتيب الفرز وعرض التاريخ في تحليلات إدارة الموظفين.</span><span class="sxs-lookup"><span data-stu-id="7b009-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
