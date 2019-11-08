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
ms.openlocfilehash: 1340f17e57f49d6adb9dc0a7c769bafa655de56e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551232"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-10-2018"></a><span data-ttu-id="4aa8f-103">ما الجديد أو المتغير في Dynamics 365 Talent - Core HR(10 سبتمبر 2018)</span><span class="sxs-lookup"><span data-stu-id="4aa8f-103">What's new or changed in Dynamics 365 Talent - Core HR (September 10, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4aa8f-104">**الإصدار 8.1.138.0**</span><span class="sxs-lookup"><span data-stu-id="4aa8f-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="4aa8f-105">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent: Core HR.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 Talent: Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="4aa8f-106">السماح بوقت معين في اليوم في طلبات الإجازات (أنصاف الأيام)</span><span class="sxs-lookup"><span data-stu-id="4aa8f-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="4aa8f-107">إذا تم إعداد الإجازة والغياب بحيث يُرسل زمن التوقف بالأيام، يمكن الآن أيضًا تمكين تعريف نصف اليوم.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="4aa8f-108">وبعد ذلك، عندما يقوم المستخدمون بإرسال طلبات زمن التوقف،  يمكنهم تحديد إذا ما كان ذلك يعني قيامهم بطلب النصف الأول أو النصف الثاني من يوم الإجازة.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="4aa8f-109">يتم إيقاف تشغيل هذا الخيار افتراضيًا.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-109">By default, this option is turned off.</span></span> <span data-ttu-id="4aa8f-110">بالنسبة للموظفين الذين يطلبون النص الأول أو النصف الثاني من اليوم إجازة، يجب عليك تشغيل هذا الخيار في منطقة **الإجازة والغياب** لمُحددات الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="4aa8f-111">امتياز الأمان لهذه الميزة هو الاحتفاظ بمحددات الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="4aa8f-112">التحقق من إدخالات الإجازة والغياب</span><span class="sxs-lookup"><span data-stu-id="4aa8f-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="4aa8f-113">بناءً عل كيفية تكوين الإجازة، يتلقى الموظفون الذي يحاولون إرسال طلب إجازة أطول من يوم العمل الخاصة بهم، رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="4aa8f-114">بمعنى آخر، يتم تحذيرهم إذا حاولوا أخذ أكثر من يوم كامل إجازة في أي تاريخ محدد.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="4aa8f-115">يتم دائمًا تشغيل ميزة التحقق من الصحة هذه.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-115">This validation is always turned on.</span></span> <span data-ttu-id="4aa8f-116">في أي وقت يتجاوز الموظف حد اليوم المُحدد، يتلقي تحذير في طلب الإجازة الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="4aa8f-117">حقول إضافية للعبارات الشرطية في مهام سير العمل.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="4aa8f-118">تمت إضافة حقول إضافية إلى العبارات الشرطية وعناصر نائبة لمهام سير عمل متعددة في Core HR.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="4aa8f-119">تمت إضافة الحقول التالية إلى عمليات سير عمل التعويض والإنهاء والنقل:</span><span class="sxs-lookup"><span data-stu-id="4aa8f-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="4aa8f-120">EmploymentType</span><span class="sxs-lookup"><span data-stu-id="4aa8f-120">EmploymentType</span></span>
- <span data-ttu-id="4aa8f-121">LegalEntity</span><span class="sxs-lookup"><span data-stu-id="4aa8f-121">LegalEntity</span></span>
- <span data-ttu-id="4aa8f-122">AdjustedWorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="4aa8f-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="4aa8f-123">EmployerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="4aa8f-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="4aa8f-124">EmployerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="4aa8f-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="4aa8f-125"> TransitionDate</span><span class="sxs-lookup"><span data-stu-id="4aa8f-125">TransitionDate</span></span>
- <span data-ttu-id="4aa8f-126">WorkerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="4aa8f-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="4aa8f-127">WorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="4aa8f-127">WorkerStartDate</span></span>
- <span data-ttu-id="4aa8f-128">WorkerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="4aa8f-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="4aa8f-129">ProbationEndDate</span><span class="sxs-lookup"><span data-stu-id="4aa8f-129">ProbationEndDate</span></span>
- <span data-ttu-id="4aa8f-130">المهنة</span><span class="sxs-lookup"><span data-stu-id="4aa8f-130">Position</span></span>
- <span data-ttu-id="4aa8f-131">الاتحاد</span><span class="sxs-lookup"><span data-stu-id="4aa8f-131">Union</span></span>
- <span data-ttu-id="4aa8f-132">القسم</span><span class="sxs-lookup"><span data-stu-id="4aa8f-132">Department</span></span>
- <span data-ttu-id="4aa8f-133">PositionType</span><span class="sxs-lookup"><span data-stu-id="4aa8f-133">PositionType</span></span>
- <span data-ttu-id="4aa8f-134">CompLocation</span><span class="sxs-lookup"><span data-stu-id="4aa8f-134">CompLocation</span></span>
- <span data-ttu-id="4aa8f-135">المسمى الوظيفي</span><span class="sxs-lookup"><span data-stu-id="4aa8f-135">Title</span></span>
- <span data-ttu-id="4aa8f-136">وظيفة</span><span class="sxs-lookup"><span data-stu-id="4aa8f-136">Job</span></span>
- <span data-ttu-id="4aa8f-137">JobType</span><span class="sxs-lookup"><span data-stu-id="4aa8f-137">JobType</span></span>
- <span data-ttu-id="4aa8f-138">JobFamily</span><span class="sxs-lookup"><span data-stu-id="4aa8f-138">JobFamily</span></span>
- <span data-ttu-id="4aa8f-139">JobFunction</span><span class="sxs-lookup"><span data-stu-id="4aa8f-139">JobFunction</span></span>

<span data-ttu-id="4aa8f-140">تمت إضافة الحقول التالية إلى سير عمل المنصب:</span><span class="sxs-lookup"><span data-stu-id="4aa8f-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="4aa8f-141">المهنة</span><span class="sxs-lookup"><span data-stu-id="4aa8f-141">Position</span></span>
- <span data-ttu-id="4aa8f-142">الاتحاد</span><span class="sxs-lookup"><span data-stu-id="4aa8f-142">Union</span></span>
- <span data-ttu-id="4aa8f-143">القسم</span><span class="sxs-lookup"><span data-stu-id="4aa8f-143">Department</span></span>
- <span data-ttu-id="4aa8f-144">PositionType</span><span class="sxs-lookup"><span data-stu-id="4aa8f-144">PositionType</span></span>
- <span data-ttu-id="4aa8f-145">CompLocation</span><span class="sxs-lookup"><span data-stu-id="4aa8f-145">CompLocation</span></span>
- <span data-ttu-id="4aa8f-146">المسمى الوظيفي</span><span class="sxs-lookup"><span data-stu-id="4aa8f-146">Title</span></span>
- <span data-ttu-id="4aa8f-147">وظيفة</span><span class="sxs-lookup"><span data-stu-id="4aa8f-147">Job</span></span>
- <span data-ttu-id="4aa8f-148">JobType</span><span class="sxs-lookup"><span data-stu-id="4aa8f-148">JobType</span></span>
- <span data-ttu-id="4aa8f-149">JobFamily</span><span class="sxs-lookup"><span data-stu-id="4aa8f-149">JobFamily</span></span>
- <span data-ttu-id="4aa8f-150">JobFunction</span><span class="sxs-lookup"><span data-stu-id="4aa8f-150">JobFunction</span></span>

<span data-ttu-id="4aa8f-151">تتوفر الحقول في العبارات الشرطية والعناصر النائبة لجميع المستخدمين الذين لديهم صلاحية الوصول لتكوين عمليات سير العمل المذكورة مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="4aa8f-152">الانتقال إلى Attract من إدارة الموظفين</span><span class="sxs-lookup"><span data-stu-id="4aa8f-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="4aa8f-153">في إدارة الموظفين، إذا لم يتم إعداد Attract، فمن ثم يوجه قسم**المرشحون المُراد توظيفهم** البدء باستخدام Attract بدلًا من عرض الرسالة "لم يتم العثور على أي شئ لعرضه هنا."</span><span class="sxs-lookup"><span data-stu-id="4aa8f-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="4aa8f-154">التغييرات الأخرى</span><span class="sxs-lookup"><span data-stu-id="4aa8f-154">Other changes</span></span>

<span data-ttu-id="4aa8f-155">يشمل هذا الإصدار عددًا من إصلاحات الأخطاء الإضافية:</span><span class="sxs-lookup"><span data-stu-id="4aa8f-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="4aa8f-156">عند توظيف مقاول، يجب ألا تتوافر علامة تبويب**التعويض** على صفحة الطلب/الإجراء.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="4aa8f-157">أثناء عملية إنهاء لطلب، لا يمكنك المتابعة حتى تحتوي كافة الحقول المطلوبة على بيانات.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="4aa8f-158">تمت معالجة مشاكل ترتيب الفرز وعرض التاريخ في تحليلات إدارة الموظفين.</span><span class="sxs-lookup"><span data-stu-id="4aa8f-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
