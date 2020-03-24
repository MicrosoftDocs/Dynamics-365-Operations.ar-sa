---
title: استخدام التقارير التحليلية‬ في Attract
description: يصف هذا الموضوع التقارير التحليلية للرؤى الخاصة بعملية التوظيف في Microsoft Dynamics 365 Talent - Attract
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: 081988e8b8cfe1e2ddb533247b678ba38a07f5f1
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092166"
---
# <a name="use-analytic-reports-in-attract"></a><span data-ttu-id="1471e-103">استخدام التقارير التحليلية‬ في Attract</span><span class="sxs-lookup"><span data-stu-id="1471e-103">Use analytic reports in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1471e-104">توفر التقارير التحليلية في Microsoft Dynamics 365 Talent: Attract حلا جاهزا (OOTB) لرؤى عملية التوظيف.</span><span class="sxs-lookup"><span data-stu-id="1471e-104">Analytic reports in Microsoft Dynamics 365 Talent: Attract provide an out-of-the-box (OOTB) solution for hiring process insights.</span></span> <span data-ttu-id="1471e-105">تتضمن الميزات المتوفرة:</span><span class="sxs-lookup"><span data-stu-id="1471e-105">Availabe features include:</span></span>

- <span data-ttu-id="1471e-106">**تحليلات الوظيفة:** انقر فوق علامة التبويب **التحليلات** ضمن وظيفة ما للاطلاع على مقاييس حول مقدمي طلبات الحصول على الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="1471e-106">**Job analytics:** Click the **Analytics** tab within a job for metrics on the job's applicants.</span></span>
- <span data-ttu-id="1471e-107">**مركز التحليلات:** انقر فوق **التحليلات** على قسم التنقل الأيمن للحصول على مقاييس مجمعة عبر الوظائف.</span><span class="sxs-lookup"><span data-stu-id="1471e-107">**Analytics hub:** Click **Analytics** on the left navigation for aggregated metrics across jobs.</span></span>
- <span data-ttu-id="1471e-108">**الأمان الخاص بالمستخدم:** إمكانية الوصول إلى التقارير يتحكم فيها [دور](security-attract.md) Attract ودور المشارك في الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="1471e-108">**User-specific security:** Access to reports is controlled by Attract [role](security-attract.md) and job participant role.</span></span>
- <span data-ttu-id="1471e-109">**التصفية المتقاطعة:** انقر فوق المرئيات ضمن تقرير لعرض مقاييس أخرى تمت تصفيتها حسب البيانات المحددة.</span><span class="sxs-lookup"><span data-stu-id="1471e-109">**Cross-filtering:** Click visuals within a report to view other metrics filtered by selected data.</span></span>

>[!NOTE] 
>- <span data-ttu-id="1471e-110">في الوقت الحالي، هذه الميزة قيد [المعاينة](access-preview-feature.md).</span><span class="sxs-lookup"><span data-stu-id="1471e-110">This feature is currently in [preview](access-preview-feature.md).</span></span> <span data-ttu-id="1471e-111">لتجربتها، يجب أن يتوفر لديك [**المكون الإضافي "التوظيف الشامل"‬**](attract-comprehensive-hiring.md).</span><span class="sxs-lookup"><span data-stu-id="1471e-111">To try it, you must have the [**Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span></span>
>- <span data-ttu-id="1471e-112">تظهر كافة تقارير المعاينة العامة باللغة الإنجليزية.</span><span class="sxs-lookup"><span data-stu-id="1471e-112">All public preview reports are displayed in English.</span></span>
>- <span data-ttu-id="1471e-113">يتم تحديث التقارير كل 3 ساعات.</span><span class="sxs-lookup"><span data-stu-id="1471e-113">Reports refresh every 3 hours.</span></span> <span data-ttu-id="1471e-114">ويقع وقت التحديث الأخير (في المنطقة الزمنية المحلية) في أعلى التقرير.</span><span class="sxs-lookup"><span data-stu-id="1471e-114">The last refresh time (in the local timezone) is located at the top of the report.</span></span> <span data-ttu-id="1471e-115">تعتبر أوقات التحديث تقريبيه وتختلف بناء على حجم البيانات وتحميل الموارد في منطقتك.</span><span class="sxs-lookup"><span data-stu-id="1471e-115">Refresh times are an approximation and vary based on data volume and resource load in your region.</span></span>

## <a name="job-analytics"></a><span data-ttu-id="1471e-116">تحليلات الوظيفة</span><span class="sxs-lookup"><span data-stu-id="1471e-116">Job Analytics</span></span>

<span data-ttu-id="1471e-117">تقدم تقارير تحليلات الوظيفة لقطة لعملية التوظيف الخاصة بوظيفة ما.</span><span class="sxs-lookup"><span data-stu-id="1471e-117">Job Analytics reports are a snapshot of the hiring process for a job.</span></span>  <span data-ttu-id="1471e-118">تتضمن المقاييس الأساسية:</span><span class="sxs-lookup"><span data-stu-id="1471e-118">Key metrics include:</span></span>

- <span data-ttu-id="1471e-119">مقدمو الطلبات النشطاء حسب المرحلة</span><span class="sxs-lookup"><span data-stu-id="1471e-119">Active applicants by stage</span></span>
- <span data-ttu-id="1471e-120">مصدر مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="1471e-120">Applicant source</span></span>
- <span data-ttu-id="1471e-121">نوع مقدم الطلب (داخلي أو خارجي)</span><span class="sxs-lookup"><span data-stu-id="1471e-121">Applicant type (internal or external)</span></span>

## <a name="analytics-hub"></a><span data-ttu-id="1471e-122">مركز التحليلات</span><span class="sxs-lookup"><span data-stu-id="1471e-122">Analytics Hub</span></span>

<span data-ttu-id="1471e-123">تقوم تقارير مركز التحليلات بتجميع البيانات عبر الوظائف للكشف عن الاتجاهات في عملية التوظيف.</span><span class="sxs-lookup"><span data-stu-id="1471e-123">Analytics Hub reports aggregate data across jobs to surface trends in the hiring process.</span></span> <span data-ttu-id="1471e-124">يتضمن Attract تقريرين جاهزين: ملخص المسار والتحليلات القُمعية.</span><span class="sxs-lookup"><span data-stu-id="1471e-124">Attract includes two OOTB reports: Pipeline Summary and Funnel Analysis.</span></span>

### <a name="pipeline-summary"></a><span data-ttu-id="1471e-125">ملخص المسار</span><span class="sxs-lookup"><span data-stu-id="1471e-125">Pipeline Summary</span></span>

<span data-ttu-id="1471e-126">يقوم تقرير ملخص المسار بتجميع البيانات للوظائف المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="1471e-126">The Pipeline Summary report aggregates data for open jobs.</span></span> <span data-ttu-id="1471e-127">تتضمن المقاييس الأساسية:</span><span class="sxs-lookup"><span data-stu-id="1471e-127">Key metrics include:</span></span>

- <span data-ttu-id="1471e-128">مقدمو الطلبات عبر جميع الوظائف حسب المرحلة</span><span class="sxs-lookup"><span data-stu-id="1471e-128">Applicants across all jobs by stage</span></span>
- <span data-ttu-id="1471e-129">مصدر مقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="1471e-129">Applicant source</span></span>
- <span data-ttu-id="1471e-130">الوظائف المفتوحة حسب مستوى الأقدمية</span><span class="sxs-lookup"><span data-stu-id="1471e-130">Open jobs by seniority level</span></span>

### <a name="funnel-analysis"></a><span data-ttu-id="1471e-131">التحليلات القُمعية</span><span class="sxs-lookup"><span data-stu-id="1471e-131">Funnel Analysis</span></span>

<span data-ttu-id="1471e-132">يقوم تقرير التحليلات القُمعية بتجميع البيانات للوظائف التي تم إغلاقها كوظائف لم تعد شاغرة.</span><span class="sxs-lookup"><span data-stu-id="1471e-132">The Funnel Analysis report aggregates data for jobs that have been closed as filled.</span></span> <span data-ttu-id="1471e-133">تتضمن المقاييس الأساسية:</span><span class="sxs-lookup"><span data-stu-id="1471e-133">Key metrics include:</span></span>

- <span data-ttu-id="1471e-134">الوقت المطلوب للتوظيف</span><span class="sxs-lookup"><span data-stu-id="1471e-134">Time to hire</span></span>
- <span data-ttu-id="1471e-135">مقاييس التحويل (عند تمرير الماوس)</span><span class="sxs-lookup"><span data-stu-id="1471e-135">Conversion metrics (on hover)</span></span>
- <span data-ttu-id="1471e-136">معدل قبول العرض</span><span class="sxs-lookup"><span data-stu-id="1471e-136">Offer acceptance rate</span></span>

<span data-ttu-id="1471e-137">ملاحظة: للحصول على الوقت الأكثر دقه لإعداد تقرير التوظيف، من المستحسن استخدام‏‎ ميزة [إدارة العروض](offer-setup.md) المتاحة كجزء من المكون الإضافي "التوظيف الشامل".</span><span class="sxs-lookup"><span data-stu-id="1471e-137">Note: For the most accurate time to hire reporting, it is recommended that you use [Offer management](offer-setup.md), a feature available as part of the Comprehensive Hiring Add-On.</span></span>

>[!TIP] 
><span data-ttu-id="1471e-138">حاول تمرير الماوس فوق المرئيات للحصول على معلومات إضافية.</span><span class="sxs-lookup"><span data-stu-id="1471e-138">Try hovering over visuals for additional information.</span></span> <span data-ttu-id="1471e-139">على سبيل المثال، سيؤدي تمرير الماوس فوق مرئيات **مقدمو الطلبات النشطاء** إلى عرض متوسط الأيام في المرحلة.</span><span class="sxs-lookup"><span data-stu-id="1471e-139">For example, hovering over **Active applicants** visuals will display the average days in stage.</span></span> <span data-ttu-id="1471e-140">قد يوفر تحليل هذه المعلومات تفاصيل مهمة حول تقليل الوقت المطلوب للتوظيف وتمكين مسؤولي التعيين من التركيز على الطرق التي تسمح بتقليل الوقت المنقضي في كل مرحلة.</span><span class="sxs-lookup"><span data-stu-id="1471e-140">Analyzing this information can provide insights critical to reducing time to hire and enable recruiters to focus on ways to reduce the time spent in each stage.</span></span>

## <a name="user-specific-security"></a><span data-ttu-id="1471e-141">الأمان الخاص بالمستخدم</span><span class="sxs-lookup"><span data-stu-id="1471e-141">User-specific security</span></span>

<span data-ttu-id="1471e-142">بإمكان الأشخاص الذين يؤدون [أدوار](security-attract.md) المسؤول وقراءة الكل ومسؤول التعيين ومدير التوظيف الوصول إلى تقارير Attract.</span><span class="sxs-lookup"><span data-stu-id="1471e-142">Attract reports are accessible for Admin, Read All, Recruiter, and Hiring Manager [roles](security-attract.md).</span></span> <span data-ttu-id="1471e-143">لا يتوفر لدى المستخدمين الذين لا يؤدون هذه الأدوار الوصول إلى أي من صفحات التقارير التحليلية (تحليلات الوظيفة أو مركز التحليلات).</span><span class="sxs-lookup"><span data-stu-id="1471e-143">Unassigned users do not have access to either of the analytic report pages (Job Analytics or Analytics Hub).</span></span>

<span data-ttu-id="1471e-144">تعرض تقارير تحليلات الوظيفة بيانات للوظيفة المحددة.</span><span class="sxs-lookup"><span data-stu-id="1471e-144">Job Analytics reports display data for the selected job.</span></span> <span data-ttu-id="1471e-145">تقوم تقارير مركز التحليلات بتجميع البيانات عبر كافة الوظائف التي يمكن للمستخدم عرضها.</span><span class="sxs-lookup"><span data-stu-id="1471e-145">Analytics Hub reports aggregate data across all jobs a user can view.</span></span> <span data-ttu-id="1471e-146">تتوفر لدى المستخدمين الذين يمكنهم عرض "الوظائف الخاصة بي‬" و"كل الوظائف‬" على صفحة الوظائف طرق العرض نفسها المتوفرة في مركز التحليلات.</span><span class="sxs-lookup"><span data-stu-id="1471e-146">Users that can view both My jobs and All jobs on the Jobs page have the same views available in the Analytics Hub.</span></span>

## <a name="cross-filter"></a><span data-ttu-id="1471e-147">التصفية المتقاطعة</span><span class="sxs-lookup"><span data-stu-id="1471e-147">Cross-filter</span></span>

<span data-ttu-id="1471e-148">إحدى أهم الميزات الرائعة في Power BI هي الطريقة التي ترتبط بها جميع المرئيات في صفحة التقرير.</span><span class="sxs-lookup"><span data-stu-id="1471e-148">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="1471e-149">إذا قمت بتحديد نقطه بيانات على إحدى المرئيات، ستتغير جميع المرئيات الأخرى التي تحتوي على تلك البيانات، استنادًا إلى ذلك التحديد.</span><span class="sxs-lookup"><span data-stu-id="1471e-149">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> <span data-ttu-id="1471e-150">تعرف على المزيد وراجع مثالاً في [كيف تجري المرئيات تصفية متقاطعة عبر بعضها البعض في تقرير Power BI](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span><span class="sxs-lookup"><span data-stu-id="1471e-150">Find out more and see an example in [How visuals cross-filter each other in a Power BI report](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="1471e-151">تصدير إلى Excel</span><span class="sxs-lookup"><span data-stu-id="1471e-151">Export to Excel</span></span>

<span data-ttu-id="1471e-152">لعرض بيانات التقرير في Excel، يمكنك النقر فوق القائمة "خيارات" (ثلاث نقاط) على رسم مرئي وتحديد **تصدير البيانات الأساسية**.</span><span class="sxs-lookup"><span data-stu-id="1471e-152">To view report data in Excel, you can click the options menu (three dots) on a visual and select **Export underlying data**.</span></span> <span data-ttu-id="1471e-153">سيتم تصدير البيانات المصدّرة كبيانات تمت تصفيتها، مما يسمح بمراعاة أذونات المستخدم في Attract.</span><span class="sxs-lookup"><span data-stu-id="1471e-153">Exported data will export as filtered, respecting user permissions in Attract.</span></span> <span data-ttu-id="1471e-154">لمزيد من المعلومات، راجع [تصدير بيانات من الرسوم المرئية](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span><span class="sxs-lookup"><span data-stu-id="1471e-154">For more information, see [Export data from visualizations](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span></span>
