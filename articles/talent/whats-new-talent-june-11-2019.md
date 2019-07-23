---
title: ما الجديد والمتغير في Dynamics 365 for Talent (11 يونيو 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
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
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 42b9541b152d2a6daa1dbf95ecf30a2f51eb36f3
ms.sourcegitcommit: 31a918d357a7182f3870713a9c4455bd5c44cd58
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/18/2019
ms.locfileid: "1634470"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-11-2019"></a><span data-ttu-id="55539-103">ما الجديد والمتغير في Dynamics 365 for Talent (11 يونيو 2019)</span><span class="sxs-lookup"><span data-stu-id="55539-103">What's new or changed in Dynamics 365 for Talent (June 11, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="55539-104">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="55539-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="55539-105">التغييرات في Attract</span><span class="sxs-lookup"><span data-stu-id="55539-105">Changes in Attract</span></span>

### <a name="search-engine-optimization-for-job-posts"></a><span data-ttu-id="55539-106">تحسين محرك البحث لعمليات نشر المهام</span><span class="sxs-lookup"><span data-stu-id="55539-106">Search engine optimization for job posts</span></span>

<span data-ttu-id="55539-107">بعد قيامك بتشغيل **تحسين محرك البحث** في Dynamics 365 for Talent: مركز الإدارة‬‏‫‬‏‫ في Attract، يقوم Attract بإعلام واجهة برمجة التطبيق (API) في فهرسة Google لتتبع صفحة الويب في حالة تنشيط وظيفة جديدة ونشرها أو تحديث وظيفة موجودة.</span><span class="sxs-lookup"><span data-stu-id="55539-107">After you turn on **Search Engine Optimization** in the Dynamics 365 for Talent: Attract Admin center, Attract informs the Google Indexing application programming interface (API) to crawl the webpage whenever you activate and post a new job or update an existing job.</span></span> <span data-ttu-id="55539-108">وبهذه الطريقة، ستظهر الوظيفة في نتائج البحث في Google ومحركات البحث الأخرى.</span><span class="sxs-lookup"><span data-stu-id="55539-108">In this way, the job will appear in the search results for Google and other search engines.</span></span>

<span data-ttu-id="55539-109">وبالمثل، في حالة إلغاء نشر وظيفة، يقوم Attract بإعلام واجهة برمجة تطبيق الفهرسة ليتوقف ظهور الوظيفة التي تم إلغاء نشرها عن الظهور في نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="55539-109">Likewise, whenever you unpost a job, Attract informs the Indexing API, so that the unposted job will stop appearing in search results.</span></span>

> [!NOTE]
> <span data-ttu-id="55539-110">لا تحتوي متتبعات ارتباطات الويب علي إطار زمني معرف لتتبع ارتباطات صفحات الويب أو تحديث نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="55539-110">Web crawlers don't have a defined timeframe for crawling webpages or updating search results.</span></span>

## <a name="coming-soon-in-attract"></a><span data-ttu-id="55539-111">قريبًا في Attract</span><span class="sxs-lookup"><span data-stu-id="55539-111">Coming soon in Attract</span></span>

### <a name="job-approvals-appear-on-the-home-page"></a><span data-ttu-id="55539-112">تظهر الموافقات على الوظائف في الصفحة الرئيسية</span><span class="sxs-lookup"><span data-stu-id="55539-112">Job approvals appear on the home page</span></span>

<span data-ttu-id="55539-113">تظهر الموافقات في قسم **الموافقات** على لوحة المعلومات.</span><span class="sxs-lookup"><span data-stu-id="55539-113">Approvals appear in an **Approvals** section on the dashboard.</span></span> <span data-ttu-id="55539-114">يستطيع المعتمدون مراجعة موافقاتهم ضمن **المعينة لك**، التي تعرض معرف الوظيفة والمسمى الوظيفي والمعتمدين الآخرين وتاريخ تعيين الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="55539-114">Approvers can review their approvals under **Assigned to you**, which shows the job ID, the job title, other approvers, and the date when the job was assigned.</span></span> <span data-ttu-id="55539-115">يستطيع المستخدمين الذين يقومون بإرسال وظيفة للاعتماد مراجعة الوظائف الخاصة بهم ضمن **طلبتها**، التي تعرض المعتمدين الذين لا يزالوا يحتاجون إلى اعتماد الوظيفة التي تم إرسالها.</span><span class="sxs-lookup"><span data-stu-id="55539-115">Users who submit a job for approval can review their jobs under **Requested by you**, which shows the approvers who must still approve the submitted job.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="55539-116">التغييرات في Onboard</span><span class="sxs-lookup"><span data-stu-id="55539-116">Changes in Onboard</span></span>

<span data-ttu-id="55539-117">يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 for Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="55539-117">This release includes minor bug fixes for Dynamics 365 for Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="55539-118">التغييرات في Core HR</span><span class="sxs-lookup"><span data-stu-id="55539-118">Changes in Core HR</span></span>

<span data-ttu-id="55539-119">تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2337.</span><span class="sxs-lookup"><span data-stu-id="55539-119">The changes that are described in this section apply to build number 8.1.2337.</span></span>

### <a name="platform-update-27"></a><span data-ttu-id="55539-120">update 27 للنظام الأساسي</span><span class="sxs-lookup"><span data-stu-id="55539-120">Platform update 27</span></span>

<span data-ttu-id="55539-121">للحصول على مزيد من التفاصيل حول Platform update 27، راجع [ميزات المعاينة في Dynamics 365 for Finance and Operations platform update 27 (مايو 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).</span><span class="sxs-lookup"><span data-stu-id="55539-121">For more details about Platform update 27, see [Preview features in Dynamics 365 for Finance and Operations platform update 27 (June 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).</span></span>

### <a name="feature-management-workspace-in-talent"></a><span data-ttu-id="55539-122">مساحة عمل إدارة الميزات في Talent</span><span class="sxs-lookup"><span data-stu-id="55539-122">Feature management workspace in Talent</span></span>

<span data-ttu-id="55539-123">تتيح مساحة عمل **إدارة الميزات** في **إدارة النظام** عرض الميزات التي تم تسليمها في كل إصدار من الإصدارات وتمكينها وتعطيلها وجدولتها.</span><span class="sxs-lookup"><span data-stu-id="55539-123">The **Feature management** workspace in **System administration** lets you view, enable, disable, and schedule features that have been delivered in each release.</span></span> <span data-ttu-id="55539-124">بشكل افتراضي، تكون الميزات الجديدة متوقفة عن التشغيل.</span><span class="sxs-lookup"><span data-stu-id="55539-124">By default, new features are turned off.</span></span> <span data-ttu-id="55539-125">ويمكنك استخدام مساحة عمل **إدارة الميزات** لتشغيلها وعرض الوثائق الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="55539-125">You can use the **Feature management** workspace to turn them on and view the documentation for them.</span></span>

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="55539-126">دعم كيان Common Data Service للحقول المخصصة</span><span class="sxs-lookup"><span data-stu-id="55539-126">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="55539-127">يدعم كيان إصدار الوكالة الآن الحقول المخصصة.</span><span class="sxs-lookup"><span data-stu-id="55539-127">The Issuing agency entity now supports custom fields.</span></span>

### <a name="new-common-data-service-entities"></a><span data-ttu-id="55539-128">كيانات Common Data Service جديدة</span><span class="sxs-lookup"><span data-stu-id="55539-128">New Common Data Service entities</span></span>

<span data-ttu-id="55539-129">تمت إضافة كيان مجموعة المهام.</span><span class="sxs-lookup"><span data-stu-id="55539-129">The Task group entity has been added.</span></span>

## <a name="in-preview"></a><span data-ttu-id="55539-130">قيد المعاينة</span><span class="sxs-lookup"><span data-stu-id="55539-130">In preview</span></span>

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a><span data-ttu-id="55539-131">لن يتم تمكين ميزات المعاينة إلا في بيئات الاختبار المعزولة‬</span><span class="sxs-lookup"><span data-stu-id="55539-131">Preview features will be enabled only in sandbox environments</span></span>

<span data-ttu-id="55539-132">لمزيد من المعلومات حول كيفية نشر التغييرات، راجع [توفير Talent‬](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="55539-132">For more information about how changes are published, see [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="55539-133">عند توفير مثيل جديد من Talent‬، يمكنك الاشار إلى ما إذا كان نوع المثيل هو إنتاج أو ابيئة اختبار معزولة.</span><span class="sxs-lookup"><span data-stu-id="55539-133">When you provision a new instance of Talent, you can indicate whether the instance type is Production or Sandbox.</span></span> <span data-ttu-id="55539-134">يسمح نوع المثيل "بيئة اختبار معزولة" بالاختبار المبكر للميزات الجديدة.</span><span class="sxs-lookup"><span data-stu-id="55539-134">The Sandbox instance type allows for early testing of new features.</span></span> <span data-ttu-id="55539-135">سيتم تحديث كافة مثيلات Talent الموجودة إلى نوع مثيل **الإنتاج**.</span><span class="sxs-lookup"><span data-stu-id="55539-135">All existing Talent instances will be updated to the **Production** instance type.</span></span> <span data-ttu-id="55539-136">إذا كنت ترغب في تحديث أحد المثيلات الموجودة لديك إلى نوع مثيل **بيئة الاختبار المعزولة**، اتصل بـ [الدعم](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support) لبدء طلب التغيير.</span><span class="sxs-lookup"><span data-stu-id="55539-136">If you want one of your existing instances to be updated to the **Sandbox** instance type, contact [Support](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support) to initiate the change request.</span></span>

### <a name="restrict-the-leave-types-in-time-off-requests"></a><span data-ttu-id="55539-137">تقييد أنواع الإجازات في طلب أيام الإجازات</span><span class="sxs-lookup"><span data-stu-id="55539-137">Restrict the leave types in time-off requests</span></span>

<span data-ttu-id="55539-138">يمكن للمؤسسات تقديم العديد من أنواع الإجازات إلى الموظفين.</span><span class="sxs-lookup"><span data-stu-id="55539-138">Organizations can offer many types of leave to employees.</span></span> <span data-ttu-id="55539-139">ولكن، قد لا يكون مناسبًا للموظفين تقديم طلبات الإجازات لبعض أنواع الإجازات.</span><span class="sxs-lookup"><span data-stu-id="55539-139">However, it might not be appropriate for employees to submit time-off requests for some leave types.</span></span> <span data-ttu-id="55539-140">وقد تتم إدارة أنواع الإجازات هذه بواسطة الموارد البشرية (HR) بدلاً من ذلك.</span><span class="sxs-lookup"><span data-stu-id="55539-140">Those leave types might be managed by Human resources (HR) instead.</span></span> <span data-ttu-id="55539-141">يمكنك في هذا الإصدار تكوين أنواع الإجازات التي يمكن للموظفين تقديم طلبات أيام الإجازة لها.</span><span class="sxs-lookup"><span data-stu-id="55539-141">In this release, you can configure which leave types employees can submit time-off requests for.</span></span> 

## <a name="coming-soon-in-core-hr"></a><span data-ttu-id="55539-142">قريبًا من Core HR</span><span class="sxs-lookup"><span data-stu-id="55539-142">Coming soon in Core HR</span></span>

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a><span data-ttu-id="55539-143">عرض معلومات موسعة حول أداء التقارير في الخدمة الذاتية للمدير</span><span class="sxs-lookup"><span data-stu-id="55539-143">View extended information about report performance in manager self-service</span></span>

<span data-ttu-id="55539-144">سيسمح خيار جديد للمديرين بعرض أداء التقارير المباشرة والتقارير الملحقة.</span><span class="sxs-lookup"><span data-stu-id="55539-144">A new option will let managers view the performance of both their direct reports and their extended reports.</span></span> <span data-ttu-id="55539-145">في الوقت الحالي، يمكن لمديري البنود تعيين أهداف الأداء وتحديثها وإصدار مراجعات جديدة.</span><span class="sxs-lookup"><span data-stu-id="55539-145">Currently, line managers can assign and update performance goals and issue new reviews.</span></span> <span data-ttu-id="55539-146">وبالإضافة إلى ذلك، يمكن للمديرين المباشرين وموظفيهم الاحتفاظ بدفاتر يومية الأداء وتحديثها للمساعدة في ضمان كفاءة عملية مراجعه الأداء.</span><span class="sxs-lookup"><span data-stu-id="55539-146">In addition, direct managers and their employees can maintain and update performance journals to help guarantee that the performance review process goes smoothly.</span></span> <span data-ttu-id="55539-147">عند تطبيق هذا التغيير، سيتمكن المديرون من عرض المعلومات المتعلقة بالأداء وصيانتها للتقارير الموسعة بالإضافة إلى التقارير المباشرة.</span><span class="sxs-lookup"><span data-stu-id="55539-147">When this change is implemented, managers will be able to view and maintain performance-related information for their extended reports in addition to their direct reports.</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="55539-148">طباعة مراجعات الأداء</span><span class="sxs-lookup"><span data-stu-id="55539-148">Print performance reviews</span></span>

<span data-ttu-id="55539-149">سيتمكن الموظفون والمديرون وموظفي الموارد البشرية من طباعة مراجعة أداء الموظف.</span><span class="sxs-lookup"><span data-stu-id="55539-149">Employees, managers, and HR will be able to print an employee's performance review.</span></span>
