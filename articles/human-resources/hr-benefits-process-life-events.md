---
title: معالجة الأحداث الحياتية
description: أثناء دورة حياة الموظف في Microsoft Dynamics 365 Human Resources، قد يواجه كل موظف العديد من تغييرات الأحداث الحياتية المختلفة.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 91812432ead4b0afccfba30f8023f014e216236a
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007970"
---
# <a name="process-life-events"></a><span data-ttu-id="79224-103">معالجة الأحداث الحياتية</span><span class="sxs-lookup"><span data-stu-id="79224-103">Process life events</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="79224-104">أثناء دورة حياة الموظف في Microsoft Dynamics 365 Human Resources، قد يواجه كل موظف العديد من تغييرات الأحداث الحياتية المختلفة.</span><span class="sxs-lookup"><span data-stu-id="79224-104">During the employee lifecycle in Microsoft Dynamics 365 Human Resources, each employee may encounter various life event changes.</span></span> <span data-ttu-id="79224-105">على سبيل المثال، الزواج أو التغيير في التوظيف أو في المعال/المستفيد.</span><span class="sxs-lookup"><span data-stu-id="79224-105">For example, marriage, change in employment, or dependent/beneficiary change.</span></span> <span data-ttu-id="79224-106">لاستخدام الأحداث الحياتية، يجب تمكين الأحداث الحياتية في نموذج محددات الميزات وإعداد أنواع الأحداث الحياتية وإعداد خيارات الأحداث الحياتية لأنواع الخطط.</span><span class="sxs-lookup"><span data-stu-id="79224-106">To use life events, you must enable life events in the benefits parameters form, set up life event types, and set up life event options for plan types.</span></span>

<span data-ttu-id="79224-107">قبل أن تتمكن من معالجة الأحداث الحياتية، فإنه يجب أن تقوم بالفعل بتشغيل التسجيل المفتوح مرة واحدة على الأقل خلال الإطار الزمني للتوظيف.</span><span class="sxs-lookup"><span data-stu-id="79224-107">Before you can process life events, you must have already run open enrollment at least once during a hiring time frame.</span></span> <span data-ttu-id="79224-108">في الولايات المتحدة، عادة ما يكون التسجيل المفتوح مرة سنويًا.</span><span class="sxs-lookup"><span data-stu-id="79224-108">In the United States, open enrollment is typically once per year.</span></span> <span data-ttu-id="79224-109">وخارج الولايات المتحدة، فإنه يمكن تشغيل التسجيل المفتوح في وقت التوظيف.</span><span class="sxs-lookup"><span data-stu-id="79224-109">Outside the United States, open enrollment may be run at the time of hire.</span></span> <span data-ttu-id="79224-110">لا يحتاج العامل إلى تحديد خطة الميزة لكي تتم معالجة الأحداث الحياتية، ولكن يجب تضمينها في معالجة التسجيل المفتوح.</span><span class="sxs-lookup"><span data-stu-id="79224-110">A worker does not need to select a benefit plan in order for life events to be processed, but they need to have been included in open enrollment processing.</span></span> 

<span data-ttu-id="79224-111">استخدم معالجة حدث الحياتي عندما يكون لديك عاملين لديهم أحداث حياتية تحدث في تاريخ مستقبلي.</span><span class="sxs-lookup"><span data-stu-id="79224-111">Use life event processing when you have workers who have life events that take place on a future date.</span></span> <span data-ttu-id="79224-112">سيقوم هذا الحدث بمعالجة كافة الأحداث الحياتية التي لم تتم معالجتها (مثل الأحداث الحياتية المستقبلية، أو الأحداث الحياتية التي تمت إضافتها والتي ليست محددة بأي عامل – ميزة جديدة).</span><span class="sxs-lookup"><span data-stu-id="79224-112">This event will process all life events that have not been processed (like future life events, or life events that have been added that are not specific to any one worker – one example is a new benefit).</span></span> <span data-ttu-id="79224-113">تكون الأحداث الحياتية في الوقت الفعلي مخفية.</span><span class="sxs-lookup"><span data-stu-id="79224-113">Real time life events are hidden.</span></span>

<span data-ttu-id="79224-114">على سبيل المثال، إذا كان اليوم هو 1 فبراير، وتم تحديد يوم 14 فبراير للعامل يوسف سامح لتغيير الكيانات القانونية، إذا قمت بتشغيل معالجة الحدث الحياتي لمده 15 فبراير، يقوم النظام بمعالجة كافة الأحداث حتى 15 فبراير.</span><span class="sxs-lookup"><span data-stu-id="79224-114">For example, if today is February 1, and on February 14 worker Joe Smith is scheduled to change legal entities, if you run life event processing for February 15, the system processes all events up until February 15.</span></span> 

1. <span data-ttu-id="79224-115">في مساحة العمل **إدارة الميزات**، ضمن **معالجة**، حدد **معالجة الحدث الحياتي**.</span><span class="sxs-lookup"><span data-stu-id="79224-115">In the **Benefits management** workspace, under **Processing**, select **Life event processing**.</span></span>

2. <span data-ttu-id="79224-116">في مربع الحوار **تشغيل معالجة الحدث الحياتي**، حدد قيم الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="79224-116">In the **Run life event process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="79224-117">الحقل</span><span class="sxs-lookup"><span data-stu-id="79224-117">Field</span></span> | <span data-ttu-id="79224-118">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="79224-118">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="79224-119">فترة التسجيل</span><span class="sxs-lookup"><span data-stu-id="79224-119">Enrollment period</span></span> | <span data-ttu-id="79224-120">فترة التسجيل المراد معالجة الأحداث الحياتية بها.</span><span class="sxs-lookup"><span data-stu-id="79224-120">The enrollment period to process life events for.</span></span> |
   | <span data-ttu-id="79224-121">كيان قانوني</span><span class="sxs-lookup"><span data-stu-id="79224-121">Legal entity</span></span> | <span data-ttu-id="79224-122">الكيان القانوني المراد معالجة الأحداث الحياتية به.</span><span class="sxs-lookup"><span data-stu-id="79224-122">The legal entity to process life events for.</span></span> |
   | <span data-ttu-id="79224-123">تاريخ حدث الحياة</span><span class="sxs-lookup"><span data-stu-id="79224-123">Life event date</span></span> | <span data-ttu-id="79224-124">يقوم النظام بمعالجة كافة الأحداث الحياتية خلال فترة التسجيل التي تتم حتى هذا التاريخ.</span><span class="sxs-lookup"><span data-stu-id="79224-124">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="79224-125">العامل</span><span class="sxs-lookup"><span data-stu-id="79224-125">Worker</span></span> | <span data-ttu-id="79224-126">العامل المراد معالجة الأحداث الحياتية له.</span><span class="sxs-lookup"><span data-stu-id="79224-126">The worker to process life events for.</span></span> <span data-ttu-id="79224-127">في حالة ترك هذا الحقل فارغًا، فإنه ستتم معالجة الأحداث الحياتية لكافة العاملين.</span><span class="sxs-lookup"><span data-stu-id="79224-127">If you leave this field blank, life events will be processed for all workers.</span></span> |

3. <span data-ttu-id="79224-128">إذا كنت ترغب في تشغيل العملية في الخلفية ، حدد **تشغيل في الخلفية** وقم بالمهام التالية:</span><span class="sxs-lookup"><span data-stu-id="79224-128">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="79224-129">إدخال المعلومات للمعالجة.</span><span class="sxs-lookup"><span data-stu-id="79224-129">Enter information for the process.</span></span>

   2. <span data-ttu-id="79224-130">لإعداد مهمة متكررة، حدد **التكرار**، وادخل معلومات التكرار، وحدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="79224-130">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="79224-131">لإعداد تنبيه بالمهمة، حدد **التنبيهات**، وحدد التنبيهات المراد استلامها، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="79224-131">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="79224-132">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="79224-132">Select **OK**.</span></span> <span data-ttu-id="79224-133">سيتم تشغيل العملية باستخدام المعلمات التي قمت بتعيينها.</span><span class="sxs-lookup"><span data-stu-id="79224-133">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="79224-134">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="79224-134">Select **OK**.</span></span>
