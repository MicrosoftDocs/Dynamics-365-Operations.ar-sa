---
title: "وظيفة موقع الوظائف في Attract"
description: "توفر هذه المقالة نظرة عامة على وظيفة موقع الوظائف المخصص للمرشحين في Microsoft Dynamics 365 for Talent - Attract. وتشرح أيضًا كيفية إعداد هذه الوظيفة."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: ar-sa
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="b4157-104">وظيفة موقع الوظائف في Attract</span><span class="sxs-lookup"><span data-stu-id="b4157-104">Career site functionality in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b4157-105">توفر هذه المقالة نظرة عامة على وظيفة موقع الوظائف المخصص للمرشحين في Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="b4157-105">This article provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="b4157-106">وتشرح أيضًا كيفية إعداد هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="b4157-106">It also explains how to set up this functionality.</span></span>

## <a name="overview"></a><span data-ttu-id="b4157-107">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="b4157-107">Overview</span></span>

<span data-ttu-id="b4157-108">يوفر Attract موقع وظائف لكل بيئة مستأجر.</span><span class="sxs-lookup"><span data-stu-id="b4157-108">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="b4157-109">على سبيل المثال، إذا كان لدى إحدى المؤسسات بيئة تطوير وبيئة اختبار، فسيتم توفير موقع وظائف لبيئة التطوير، وموقع وظائف آخر لبيئة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="b4157-109">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="b4157-110">ويعتبر كل موقع وظائف **معزولاً بشكل كامل** ولديه آلية مصادقة خاصة به.</span><span class="sxs-lookup"><span data-stu-id="b4157-110">Each career site is **completely isolated** and has its own authentication mechanism.</span></span> <span data-ttu-id="b4157-111">لا تتم مشاركة ملفات تعريف المرشحين بين مواقع الوظائف.</span><span class="sxs-lookup"><span data-stu-id="b4157-111">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="b4157-112">بشكل افتراضي، موقع الوظائف هو موقع عام.</span><span class="sxs-lookup"><span data-stu-id="b4157-112">By default, the career site is public.</span></span> <span data-ttu-id="b4157-113">وبالتالي، بإمكان المرشحين عرض جميع الوظائف الموضع عليها علامة كوظائف خارجية من دون الحاجة إلى تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="b4157-113">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="b4157-114">ومع ذلك، تتطلب كافة الإجراءات الأخرى قيام المرشحين بتسجيل دخولهم.</span><span class="sxs-lookup"><span data-stu-id="b4157-114">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="b4157-115">إدارة موقع الوظائف</span><span class="sxs-lookup"><span data-stu-id="b4157-115">Career site management</span></span>

<span data-ttu-id="b4157-116">يتم التحكم في العناصر التالية في موقع الوظائف بواسطة الإعدادات:</span><span class="sxs-lookup"><span data-stu-id="b4157-116">The following items on the career site are controlled by settings:</span></span>

- <span data-ttu-id="b4157-117">**اسم المؤسسة:** يظهر اسم المؤسسة على شريط التنقل الموجود أعلى موقع الوظائف.</span><span class="sxs-lookup"><span data-stu-id="b4157-117">**Organization name:** The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="b4157-118">من خلال تحديد اسم المؤسسة، ينتقل المرشحون إلى صفحة تسرد جميع الوظائف المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="b4157-118">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>
- <span data-ttu-id="b4157-119">**شعار المؤسسة:** تظهر صورة شعار المؤسسة في الجزء الأيمن العلوي من موقع الوظائف.</span><span class="sxs-lookup"><span data-stu-id="b4157-119">**Organization logo:** An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="b4157-120">من خلال تحديد صورة الشعار، ينتقل المرشحون إلى صفحة تسرد جميع الوظائف المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="b4157-120">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

<span data-ttu-id="b4157-121">لتعيين قيم لاسم وشعار المؤسسة، سجّل الدخول إلى Attract كمسؤول، وحدد **مركز الإدارة** في قائمة **الإعدادات** (رمز الترس)، ثم حدد علامة التبويب **معلومات الشركة**.</span><span class="sxs-lookup"><span data-stu-id="b4157-121">To set the values for the organization name and logo, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="b4157-122">يبلغ الطول الثابت لصورة الشعار التي تظهر في موقع الوظائف 20 بكسل (px).</span><span class="sxs-lookup"><span data-stu-id="b4157-122">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="b4157-123">ويتغير حجم الصورة التي تضيفها في مركز الإدارة لتمكين الاحتواء.</span><span class="sxs-lookup"><span data-stu-id="b4157-123">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="b4157-124">وبالتالي، قد يتغير العرض استنادًا إلى الصورة.</span><span class="sxs-lookup"><span data-stu-id="b4157-124">Therefore, depending on the image, the width might change.</span></span>

## <a name="career-site-url"></a><span data-ttu-id="b4157-125">عنوان URL لموقع الوظائف</span><span class="sxs-lookup"><span data-stu-id="b4157-125">Career site URL</span></span>

<span data-ttu-id="b4157-126">عند [نشر وظيفة خارجية](./Creating-jobs-Attract.md#postings) للمرة الأولى، يمكنك نسخ الارتباط **تقديم طلب** من تطبيق Attract.</span><span class="sxs-lookup"><span data-stu-id="b4157-126">When you [post an external job](./Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="b4157-127">سيكون عنوان URL لهذا الارتباط بالتنسيق التالي: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span><span class="sxs-lookup"><span data-stu-id="b4157-127">The URL for this link will be in the following format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span></span>

<span data-ttu-id="b4157-128">عنوان URL لموقع الوظائف هو سلسلة فرعية من عنوان URL **تقديم طلب**.</span><span class="sxs-lookup"><span data-stu-id="b4157-128">The URL of the career site is a substring of the **Apply** URL.</span></span> <span data-ttu-id="b4157-129">وهو يتكوّن من كل شيء وصولاً إلى اسم الشركة.</span><span class="sxs-lookup"><span data-stu-id="b4157-129">It consists of everything up through the company name.</span></span> <span data-ttu-id="b4157-130">وبالتالي، لعنوان URL السابق **تقديم طلب**، عنوان URL لموقع الوظائف هو `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span><span class="sxs-lookup"><span data-stu-id="b4157-130">Therefore, for the preceding **Apply** URL, the career site URL is `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span></span>

## <a name="authentication-options"></a><span data-ttu-id="b4157-131">خيارات المصادقة</span><span class="sxs-lookup"><span data-stu-id="b4157-131">Authentication options</span></span>

<span data-ttu-id="b4157-132">تتوفر للمرشحين خيارات تسجيل الدخول التالية في موقع وظائف Attract:</span><span class="sxs-lookup"><span data-stu-id="b4157-132">Candidates have the following sign-in options for an Attract career site:</span></span>

- <span data-ttu-id="b4157-133">الحساب الشخصي:</span><span class="sxs-lookup"><span data-stu-id="b4157-133">Personal account:</span></span>

    - <span data-ttu-id="b4157-134">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="b4157-134">LinkedIn</span></span>
    - <span data-ttu-id="b4157-135">Microsoft</span><span class="sxs-lookup"><span data-stu-id="b4157-135">Microsoft</span></span>
    - <span data-ttu-id="b4157-136">Google</span><span class="sxs-lookup"><span data-stu-id="b4157-136">Google</span></span>
    - <span data-ttu-id="b4157-137">Facebook</span><span class="sxs-lookup"><span data-stu-id="b4157-137">Facebook</span></span>

- <span data-ttu-id="b4157-138">حساب عمل أو مدرسة:</span><span class="sxs-lookup"><span data-stu-id="b4157-138">Work or school account:</span></span>

    - <span data-ttu-id="b4157-139">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="b4157-139">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="b4157-140">معلومات تسجيل الدخول إلى Azure AD مخصصة فقط للمرشحين الداخليين.</span><span class="sxs-lookup"><span data-stu-id="b4157-140">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="b4157-141">وبالتالي، فهي تُستخدم فقط من قِبل المرشحين الداخليين الذين يستخدمون أوراق اعتماد Azure AD لشركتهم.</span><span class="sxs-lookup"><span data-stu-id="b4157-141">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="b4157-142">على سبيل المثال، يريد مرشح يعمل حاليًا لدى Contoso Ltd تقديم طلب الحصول على وظيفة في شركة ليست ذات صلة بها، Alpine Ski House</span><span class="sxs-lookup"><span data-stu-id="b4157-142">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="b4157-143">في هذه الحالة، لن ينجح التسجيل الدخول إذا حاول الموظف استخدام بيانات اعتماده في Azure AD من Contoso Ltd.</span><span class="sxs-lookup"><span data-stu-id="b4157-143">In this case, the sign-in will be unsuccessful if the employee tries to use his or her Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="b4157-144">إنشاء ملف تعريف والمحافظة عليه.</span><span class="sxs-lookup"><span data-stu-id="b4157-144">Create and maintain a profile</span></span>

<span data-ttu-id="b4157-145">بعد قيام المرشحين بتسجيل الدخول إلى موقع الوظائف، بإمكانهم اختيار **ملف التعريف الخاص بي** على شريط التنقل الموجود أعلى الصفحة لإنشاء ملف تعريفهم والمحافظة عليه.</span><span class="sxs-lookup"><span data-stu-id="b4157-145">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span> <span data-ttu-id="b4157-146">يتضمن ملف التعريف معلومات شخصية ومعلومات حول الخبرة المهنية وتفاصيل حول التعليم ومستندات وارتباطات ومعلومات حول مجموعات المهارات.</span><span class="sxs-lookup"><span data-stu-id="b4157-146">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="b4157-147">يمكن استخدام ملف التعريف، بعد إنشائه، لتقديم طلبات الحصول على الوظائف التي يهتم بها المرشح.</span><span class="sxs-lookup"><span data-stu-id="b4157-147">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="b4157-148">باستطاعة ملفات تعريف أيضًا أن تساعد Attract على التوصية بالوظائف المناسبة للمرشحين.</span><span class="sxs-lookup"><span data-stu-id="b4157-148">Profiles also help Attract recommend the right jobs to candidates.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="b4157-149">العثور على الوظيفة الصحيحة</span><span class="sxs-lookup"><span data-stu-id="b4157-149">Find the right job</span></span>

<span data-ttu-id="b4157-150">في صفحة القائمة الوظائف، بإمكان المرشحين البحث عن وظيفة معينة عن طريق إدخال مصطلحات البحث.</span><span class="sxs-lookup"><span data-stu-id="b4157-150">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="b4157-151">تبحث وظيفة البحث عن مصطلحات البحث في المسميات الوظيفية وأوصاف الوظيفة، وتعرض الوظائف ذات الصلة كنتائج.</span><span class="sxs-lookup"><span data-stu-id="b4157-151">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="b4157-152">بإمكان المرشحين تصفية النتائج في أي وقت، استنادًا إلى موقع الوظيفة أو مهمة الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="b4157-152">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="b4157-153">وبإمكان المرشحين أيضًا عرض مجموعة من الوظائف الموصى بها في موقع الوظائف.</span><span class="sxs-lookup"><span data-stu-id="b4157-153">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="b4157-154">تستند الوظائف الموصى بها لمرشح مرشح إلى استمارات التقديم السابقة للمرشح وملف تعريفه وسيرها الذاتية.</span><span class="sxs-lookup"><span data-stu-id="b4157-154">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE]
> <span data-ttu-id="b4157-155">تظهر توصيات الوظائف فقط إذا تم نشر 10 وظائف على الأقل في موقع الوظائف، وإذا كان الموظف قد أكمل ملف تعريفها.</span><span class="sxs-lookup"><span data-stu-id="b4157-155">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed his or her profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="b4157-156">تقديم طلبات للحصول على وظيفة</span><span class="sxs-lookup"><span data-stu-id="b4157-156">Apply for jobs</span></span>

<span data-ttu-id="b4157-157">بعد عثور المرشحين على الوظيفة الصحيحة، يمكنهم تقديم الطلب باستخدام الزر **تقديم طلب** في صفحة تفاصيل الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="b4157-157">After candidates find the right job, they can apply by using the **Apply** button on the job details page.</span></span> <span data-ttu-id="b4157-158">في هذه المرحلة، بإمكان المرشحين إنشاء ملف تعريف جديد بالكامل أو مراجعة المعلومات الموجودة في ملف تعريفهم الموجود.</span><span class="sxs-lookup"><span data-stu-id="b4157-158">At this point, candidates can either create a brand-new profile or review the information in their existing profile.</span></span> <span data-ttu-id="b4157-159">بإمكان المرشحين أيضًا تحميل سيرة ذاتية، كما هو مطلوب، ثم إرسال استمارة التقديم للوظيفة.</span><span class="sxs-lookup"><span data-stu-id="b4157-159">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="b4157-160">التحقق من حالة استمارة التقديم‬</span><span class="sxs-lookup"><span data-stu-id="b4157-160">Check application status</span></span>

<span data-ttu-id="b4157-161">بعد تقدم المرشحين بطلبات لوظيفة أو أكثر، يمكنهم تحديد **استمارات التقديم** على شريط التنقل الموجود أعلى الصفحة لعرض استمارات التقديم المفتوحة والمغلقة</span><span class="sxs-lookup"><span data-stu-id="b4157-161">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="b4157-162">عندما يفتح المرشحون إحدى استمارات التقديم الخاصة بهم، يمكنهم الاطلاع على المرحلة الحالية وعلى أي إجراءات معلقة يجب عليهم إكمالها.</span><span class="sxs-lookup"><span data-stu-id="b4157-162">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="b4157-163">على سبيل المثال، إذا كان يجب على المرشح توفير التواريخ المحتملة لموعد مقابلة شخصية، تعرض له الصفحة خياراته.</span><span class="sxs-lookup"><span data-stu-id="b4157-163">For example, if a candidate must provide potential dates for an in-person interview, the page shows his or her options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="b4157-164">الوظائف الداخلية</span><span class="sxs-lookup"><span data-stu-id="b4157-164">Internal jobs</span></span>

<span data-ttu-id="b4157-165">في الوقت الحالي، الوظائف المميزة كوظائف داخلية ومنشورة في موقع الوظائف في Attract لا تظهر في موقع الوظائف</span><span class="sxs-lookup"><span data-stu-id="b4157-165">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="b4157-166">ويمكن الوصول إليها فقط عبر عنوان URL المباشر **تقديم طلب** الذي يمكن نسخه من استمارة التقديم في Attract.</span><span class="sxs-lookup"><span data-stu-id="b4157-166">They are accessible only via the direct **Apply** URL that can be copied from the Attract application.</span></span>

