---
title: معالجة أهلية التسجيل‬
description: يوضح هذا المقال كيفية تشغيل معالجة أهلية التسجيل.
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
ms.openlocfilehash: dfb7f13dce48f33c111af491918702763f7e3b8a
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429279"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="66170-103">معالجة أهلية التسجيل‬</span><span class="sxs-lookup"><span data-stu-id="66170-103">Process enrollment eligibility</span></span>

<span data-ttu-id="66170-104">يوضح هذا المقال كيفية تشغيل معالجة أهلية التسجيل.</span><span class="sxs-lookup"><span data-stu-id="66170-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="66170-105">في مساحة العمل **إدارة المزايا**، ضمن **معالجة**، حدد **معالجة أهلية التسجيل**.</span><span class="sxs-lookup"><span data-stu-id="66170-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="66170-106">في مربع الحوار **تشغيل معالجة أهلية التسجيل**، حدد قيم الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="66170-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="66170-107">الحقل</span><span class="sxs-lookup"><span data-stu-id="66170-107">Field</span></span> | <span data-ttu-id="66170-108">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="66170-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="66170-109">**فترة التسجيل**</span><span class="sxs-lookup"><span data-stu-id="66170-109">**Enrollment period**</span></span> | <span data-ttu-id="66170-110">فترة التسجيل المراد معالجة أهلية التسجيل لها.</span><span class="sxs-lookup"><span data-stu-id="66170-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="66170-111">**كيان قانوني**</span><span class="sxs-lookup"><span data-stu-id="66170-111">**Legal entity**</span></span> | <span data-ttu-id="66170-112">الكيان القانوني المراد معالجة أهلية التسجيل له.</span><span class="sxs-lookup"><span data-stu-id="66170-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="66170-113">**العامل**</span><span class="sxs-lookup"><span data-stu-id="66170-113">**Worker**</span></span> | <span data-ttu-id="66170-114">العامل المراد معالجة أهلية التسجيل له.</span><span class="sxs-lookup"><span data-stu-id="66170-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="66170-115">في حالة ترك هذا الحقل فارغًا، فإنه ستتم معالجة أهلية التسجيل لكافة العاملين.</span><span class="sxs-lookup"><span data-stu-id="66170-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="66170-116">**خطة الميزة**</span><span class="sxs-lookup"><span data-stu-id="66170-116">**Benefit plan**</span></span> | <span data-ttu-id="66170-117">خطة الميزة المراد معالجة أهلية التسجيل لها.</span><span class="sxs-lookup"><span data-stu-id="66170-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="66170-118">إذا كنت ترغب في تشغيل العملية في الخلفية، حدد **تشغيل في الخلفية** وقم بالمهام التالية:</span><span class="sxs-lookup"><span data-stu-id="66170-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="66170-119">إدخال المعلومات للمعالجة.</span><span class="sxs-lookup"><span data-stu-id="66170-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="66170-120">لإعداد مهمة متكررة، حدد **التكرار**، وادخل معلومات التكرار، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="66170-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="66170-121">لإعداد تنبيه بالمهمة، حدد **التنبيهات**، وحدد التنبيهات المراد استلامها، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="66170-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="66170-122">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="66170-122">Select **OK**.</span></span> <span data-ttu-id="66170-123">سيتم تشغيل العملية باستخدام المعلمات التي قمت بتعيينها.</span><span class="sxs-lookup"><span data-stu-id="66170-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="66170-124">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="66170-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="66170-125">عرض نتائج العملية</span><span class="sxs-lookup"><span data-stu-id="66170-125">View Process Results</span></span>

<span data-ttu-id="66170-126">يوضح هذا المقال كيفية عرض نتائج عملية التأهل.</span><span class="sxs-lookup"><span data-stu-id="66170-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="66170-127">في مساحة العمل **إدارة المزايا**، ضمن **معالجة**، حدد **نتائج العملية**.</span><span class="sxs-lookup"><span data-stu-id="66170-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="66170-128">في النموذج **نتائج العملية**، يتم تحديد الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="66170-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="66170-129">الحقل</span><span class="sxs-lookup"><span data-stu-id="66170-129">Field</span></span> | <span data-ttu-id="66170-130">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="66170-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="66170-131">**معرف العملية**</span><span class="sxs-lookup"><span data-stu-id="66170-131">**Process ID**</span></span> | <span data-ttu-id="66170-132">المعرف الفريد لمجموعة العامل والكيان القانوني وتشغيل العملية.</span><span class="sxs-lookup"><span data-stu-id="66170-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="66170-133">**نوع العملية**</span><span class="sxs-lookup"><span data-stu-id="66170-133">**Process type**</span></span> | <span data-ttu-id="66170-134">وهذا يحدد العملية التي تم تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="66170-134">This identifies the process that was run.</span></span> <span data-ttu-id="66170-135">على سبيل المثال، التسجيل.</span><span class="sxs-lookup"><span data-stu-id="66170-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="66170-136">**طابع زمني**</span><span class="sxs-lookup"><span data-stu-id="66170-136">**Time stamp**</span></span> | <span data-ttu-id="66170-137">الوقت الذي تم فيه تشغيل عملية التأهل.</span><span class="sxs-lookup"><span data-stu-id="66170-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="66170-138">**كيان قانوني**</span><span class="sxs-lookup"><span data-stu-id="66170-138">**Legal entity**</span></span> | <span data-ttu-id="66170-139">الكيان القانوني المحدد أثناء عمليه التسجيل.</span><span class="sxs-lookup"><span data-stu-id="66170-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="66170-140">**العامل**</span><span class="sxs-lookup"><span data-stu-id="66170-140">**Worker**</span></span> | <span data-ttu-id="66170-141">العامل الذي تمت معالجته.</span><span class="sxs-lookup"><span data-stu-id="66170-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="66170-142">\*\*الخطة</span><span class="sxs-lookup"><span data-stu-id="66170-142">\*\*Plan</span></span> | <span data-ttu-id="66170-143">خطة المزايا التي جرت محاولة التسجيل لها.</span><span class="sxs-lookup"><span data-stu-id="66170-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="66170-144">**قاعدة الاستحقاق**</span><span class="sxs-lookup"><span data-stu-id="66170-144">**Eligibility rule**</span></span> | <span data-ttu-id="66170-145">قاعدة الأهلية التي تمت معالجتها.</span><span class="sxs-lookup"><span data-stu-id="66170-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="66170-146">إذا تمت مصادفة خطأ قبل يتم تشغيل الأهلية، سيكون هذا الخيار فارغًا.</span><span class="sxs-lookup"><span data-stu-id="66170-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="66170-147">على سبيل المثال: إذا لم يتم تحديد التعويض لأحد العاملين، فلن يتم تشغيل عملية التأهل، وسيُترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="66170-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="66170-148">**حالة النتائج**</span><span class="sxs-lookup"><span data-stu-id="66170-148">**Result status**</span></span> | <span data-ttu-id="66170-149">ستكون النتيجة "مؤهلة" أو "غير مؤهلة".</span><span class="sxs-lookup"><span data-stu-id="66170-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="66170-150">ستكون حالة النتيجة "غير مؤهلة" إذا لم يتمكن العامل من تلبية معايير قاعدة الأهلية، أو إذا كان العامل يفتقد معلومات مطلوبة مثل تكرار الدفع أو تعويض ثابت، أو إذا كان هناك معلومات مفقودة على خطة المزايا تمنع تسجيل العاملين.</span><span class="sxs-lookup"><span data-stu-id="66170-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="66170-151">**رسالة النتيجة**</span><span class="sxs-lookup"><span data-stu-id="66170-151">**Result message**</span></span> | <span data-ttu-id="66170-152">يشير إلى سبب عدم تأهل العامل لخطة مزايا أو إذا نجحت قاعدة الأهلية.</span><span class="sxs-lookup"><span data-stu-id="66170-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |

