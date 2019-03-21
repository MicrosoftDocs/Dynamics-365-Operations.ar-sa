---
title: وظيفة موقع الوظائف في Attract
description: يوفر هذا الموضوع نظرة عامة حول وظيفة موقع الوظائف المخصص للمرشحين في Attract.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/13/2019
ms.locfileid: "389946"
---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="06e71-103">وظيفة موقع الوظائف في Attract</span><span class="sxs-lookup"><span data-stu-id="06e71-103">Career site functionality in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="06e71-104">يوفر هذا الموضوع نظرة عامة حول وظيفة موقع الوظائف المخصص للمرشحين في Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="06e71-104">This topic provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="06e71-105">ويشرح أيضًا كيفية إعداد هذه الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="06e71-105">It also explains how to set up this functionality.</span></span>

<span data-ttu-id="06e71-106">يوفر Attract موقع وظائف لكل بيئة في المستأجر.</span><span class="sxs-lookup"><span data-stu-id="06e71-106">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="06e71-107">على سبيل المثال، إذا كان لدى إحدى المؤسسات بيئة تطوير وبيئة اختبار، فسيتم توفير موقع وظائف لبيئة التطوير، وموقع وظائف آخر لبيئة الاختبار.</span><span class="sxs-lookup"><span data-stu-id="06e71-107">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="06e71-108">ويعتبر كل موقع وظائف معزولاً بشكل كامل ولديه آلية مصادقة خاصة به.</span><span class="sxs-lookup"><span data-stu-id="06e71-108">Each career site is completely isolated and has its own authentication mechanism.</span></span> <span data-ttu-id="06e71-109">لا تتم مشاركة ملفات تعريف المرشحين بين مواقع الوظائف.</span><span class="sxs-lookup"><span data-stu-id="06e71-109">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="06e71-110">بشكل افتراضي، موقع الوظائف هو موقع عام.</span><span class="sxs-lookup"><span data-stu-id="06e71-110">By default, the career site is public.</span></span> <span data-ttu-id="06e71-111">وبالتالي، بإمكان المرشحين عرض جميع الوظائف الموضوع عليها علامة كوظائف خارجية من دون الحاجة إلى تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="06e71-111">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="06e71-112">ومع ذلك، تتطلب كافة الإجراءات الأخرى قيام المرشحين بتسجيل دخولهم.</span><span class="sxs-lookup"><span data-stu-id="06e71-112">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="06e71-113">إدارة موقع الوظائف</span><span class="sxs-lookup"><span data-stu-id="06e71-113">Career site management</span></span>

<span data-ttu-id="06e71-114">لتعيين قيم للعناصر التالية، سجّل الدخول إلى Attract كمسؤول، وحدد **مركز الإدارة** في قائمة **الإعدادات** (رمز الترس)، ثم حدد علامة التبويب **معلومات الشركة**.</span><span class="sxs-lookup"><span data-stu-id="06e71-114">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

-   <span data-ttu-id="06e71-115">**اسم المؤسسة** - يظهر اسم المؤسسة على شريط التنقل الموجود أعلى موقع الوظائف.</span><span class="sxs-lookup"><span data-stu-id="06e71-115">**Organization name** - The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="06e71-116">من خلال تحديد اسم المؤسسة، ينتقل المرشحون إلى صفحة تسرد جميع الوظائف المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="06e71-116">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>

-   <span data-ttu-id="06e71-117">**شعار المؤسسة** - تظهر صورة شعار المؤسسة في الجزء الأيمن العلوي من موقع الوظائف.</span><span class="sxs-lookup"><span data-stu-id="06e71-117">**Organization logo** - An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="06e71-118">من خلال تحديد صورة الشعار، ينتقل المرشحون إلى صفحة تسرد جميع الوظائف المفتوحة.</span><span class="sxs-lookup"><span data-stu-id="06e71-118">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="06e71-119">يبلغ الطول الثابت لصورة الشعار التي تظهر في موقع الوظائف 20 بكسل (px).</span><span class="sxs-lookup"><span data-stu-id="06e71-119">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="06e71-120">ويتغير حجم الصورة التي تضيفها في مركز الإدارة لتمكين الاحتواء.</span><span class="sxs-lookup"><span data-stu-id="06e71-120">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="06e71-121">وبالتالي، قد يتغير العرض استنادًا إلى الصورة.</span><span class="sxs-lookup"><span data-stu-id="06e71-121">Therefore, depending on the image, the width might change.</span></span>
 
<span data-ttu-id="06e71-122">لتعيين قيم للعناصر التالية، سجّل الدخول إلى Attract كمسؤول، وحدد **مركز الإدارة** في قائمة **الإعدادات**، ثم حدد علامة التبويب **إدارة موقع الوظائف‬**.</span><span class="sxs-lookup"><span data-stu-id="06e71-122">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="06e71-123">**تحسين محرك البحث** عند تمكينه، سيصبح البحث عن جميع الوظائف العامة المنشورة في موقع وظائف Attract ممكنًا باستخدام محركات بحث مثل Bing وGoogle.</span><span class="sxs-lookup"><span data-stu-id="06e71-123">**Search Engine Optimization** - When enabled, all public jobs posted to Attract career site will be searchable using search engines like Bing and Google.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="06e71-124">قد يحدث تأخير بين تشغيل هذا الإعداد وظهور نتائج البحث، استنادًا إلى مشغل البحث الذي تستخدمه.</span><span class="sxs-lookup"><span data-stu-id="06e71-124">There might be a delay between turning this setting on and search results appearing, depending on the search engine that you are using.</span></span>
         
## <a name="career-site-urls"></a><span data-ttu-id="06e71-125">عناوين URL لموقع الوظائف</span><span class="sxs-lookup"><span data-stu-id="06e71-125">Career site URLs</span></span>

<span data-ttu-id="06e71-126">تتضمن القائمة التالية عناوين URL الأكثر استخدامًا لموقع الوظائف وكيفية الوصول إليها.</span><span class="sxs-lookup"><span data-stu-id="06e71-126">The following list contains the commonly used career site URLs and how to access them.</span></span>

-   <span data-ttu-id="06e71-127">**عنوان URL‎ للصفحة الرئيسية لموقع الوظائف** - لعرض عنوان URL‎ للصفحة الرئيسية لموقع الوظائف، سجل دخولك إلى Attract كمسؤول، وحدد **مركز الإدارة** في قائمة **الإعدادات**، ثم حدد علامة التبويب **إدارة موقع الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="06e71-127">**Career site home page URL** - To view the career site home page URL, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="06e71-128">**عنوان URL‎ لتقديم الطلب لإعلان وظيفة فردية** - عند [نشر وظيفة خارجية](Creating-jobs-Attract.md#postings) للمرة الأولى، يمكنك نسخ الارتباط **تقديم طلب** من تطبيق Attract.</span><span class="sxs-lookup"><span data-stu-id="06e71-128">**Individual job post apply URL** - When you [post an external job](Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="06e71-129">سيكون عنوان URL لهذا الارتباط بالتنسيق التالي: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span><span class="sxs-lookup"><span data-stu-id="06e71-129">The URL for this link will be in the following format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span></span>

-   <span data-ttu-id="06e71-130">**عنوان URL‎ لإعلان وظيفة فردية** - عنوان URL لإعلان الوظيفة هو سلسلة فرعية من عنوان URL لتقديم الطلب.</span><span class="sxs-lookup"><span data-stu-id="06e71-130">**Individual job post URL** - The URL of the job post is a substring of the Apply URL.</span></span> <span data-ttu-id="06e71-131">وهو يتكوّن من كل شيء وصولاً إلى رقم الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="06e71-131">It consists of everything up through the job number.</span></span> <span data-ttu-id="06e71-132">وبالتالي، فيما يتعلق بعنوان URL السابق لتقديم الطلب، سيكون عنوان URL لإعلان الوظيفة [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span><span class="sxs-lookup"><span data-stu-id="06e71-132">Therefore, for the preceding Apply URL, the job post URL is [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span></span>

## <a name="authentication-options"></a><span data-ttu-id="06e71-133">خيارات المصادقة</span><span class="sxs-lookup"><span data-stu-id="06e71-133">Authentication options</span></span>

<span data-ttu-id="06e71-134">تتوفر للمرشحين خيارات تسجيل الدخول التالية في موقع وظائف Attract:</span><span class="sxs-lookup"><span data-stu-id="06e71-134">Candidates have the following sign-in options for an Attract career site:</span></span>

-   <span data-ttu-id="06e71-135">الحساب الشخصي:</span><span class="sxs-lookup"><span data-stu-id="06e71-135">Personal account:</span></span>

    -   <span data-ttu-id="06e71-136">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="06e71-136">LinkedIn</span></span>

    -   <span data-ttu-id="06e71-137">Microsoft</span><span class="sxs-lookup"><span data-stu-id="06e71-137">Microsoft</span></span>

    -   <span data-ttu-id="06e71-138">Google</span><span class="sxs-lookup"><span data-stu-id="06e71-138">Google</span></span>

    -   <span data-ttu-id="06e71-139">Facebook</span><span class="sxs-lookup"><span data-stu-id="06e71-139">Facebook</span></span>

-   <span data-ttu-id="06e71-140">حساب عمل أو مدرسة:</span><span class="sxs-lookup"><span data-stu-id="06e71-140">Work or school account:</span></span>

    -   <span data-ttu-id="06e71-141">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="06e71-141">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="06e71-142">معلومات تسجيل الدخول إلى Azure AD مخصصة فقط للمرشحين الداخليين.</span><span class="sxs-lookup"><span data-stu-id="06e71-142">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="06e71-143">وبالتالي، فهي تُستخدم فقط من قِبل المرشحين الداخليين الذين يستخدمون أوراق اعتماد Azure AD لشركتهم.</span><span class="sxs-lookup"><span data-stu-id="06e71-143">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="06e71-144">على سبيل المثال، يريد مرشح يعمل حاليًا لدى Contoso Ltd تقديم طلب الحصول على وظيفة في شركة ليست ذات صلة بها، Alpine Ski House.</span><span class="sxs-lookup"><span data-stu-id="06e71-144">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="06e71-145">في هذه الحالة، لن ينجح تسجيل الدخول إذا حاول الموظف استخدام بيانات اعتماده في Azure AD من Contoso Ltd.</span><span class="sxs-lookup"><span data-stu-id="06e71-145">In this case, the sign-in will be unsuccessful if the employee tries to use Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="06e71-146">إنشاء ملف تعريف والمحافظة عليه</span><span class="sxs-lookup"><span data-stu-id="06e71-146">Create and maintain a profile</span></span>

<span data-ttu-id="06e71-147">بعد قيام المرشحين بتسجيل الدخول إلى موقع الوظائف، بإمكانهم اختيار **ملف التعريف الخاص بي** على شريط التنقل الموجود أعلى الصفحة لإنشاء ملف تعريفهم والمحافظة عليه.</span><span class="sxs-lookup"><span data-stu-id="06e71-147">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span>
<span data-ttu-id="06e71-148">يتضمن ملف التعريف معلومات شخصية ومعلومات حول الخبرة المهنية وتفاصيل حول التعليم ومستندات وارتباطات ومعلومات حول مجموعات المهارات.</span><span class="sxs-lookup"><span data-stu-id="06e71-148">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="06e71-149">يمكن استخدام ملف التعريف، بعد إنشائه، لتقديم طلبات الحصول على الوظائف التي يهتم بها المرشح.</span><span class="sxs-lookup"><span data-stu-id="06e71-149">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="06e71-150">باستطاعة ملفات التعريف أيضًا أن تساعد Attract على التوصية بالوظائف المناسبة للمرشحين.</span><span class="sxs-lookup"><span data-stu-id="06e71-150">Profiles also help Attract recommend the right jobs to candidates.</span></span>

>   [!NOTE]
>   <span data-ttu-id="06e71-151">إذا استخدم المرشح معرّف البريد الإلكتروني لتسجيل الدخول باستخدام أحد موفري المصادقة المذكورين أعلاه، فسيكون معرّف البريد الإلكتروني الافتراضي معرّف البريد الإلكتروني لجهة الاتصال المقترن بملف التعريف.</span><span class="sxs-lookup"><span data-stu-id="06e71-151">If a candidate uses an email ID to sign in using one of the authentication providers listed above, that email ID will default to the contact email ID associated with the profile.</span></span> <span data-ttu-id="06e71-152">ومع ذلك، يمكن تغيير هذا الأخير في أي وقت وهو مستقل تمامًا عن الأول.</span><span class="sxs-lookup"><span data-stu-id="06e71-152">However, the latter can be changed at any time and is completely independent of the former.</span></span> <span data-ttu-id="06e71-153">سوف يستخدم Attract دائمًا معرّف البريد الإلكتروني لجهة الاتصال لربط ملف تعريفك لجميع مراسلات البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="06e71-153">Attract will always use the contact email ID to associate with your profile for all email communications.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="06e71-154">العثور على الوظيفة المناسبة</span><span class="sxs-lookup"><span data-stu-id="06e71-154">Find the right job</span></span>

<span data-ttu-id="06e71-155">في صفحة قائمة الوظائف، بإمكان المرشحين البحث عن وظيفة معينة عن طريق إدخال مصطلحات البحث.</span><span class="sxs-lookup"><span data-stu-id="06e71-155">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="06e71-156">تبحث وظيفة البحث عن مصطلحات البحث في المسميات الوظيفية وأوصاف الوظيفة، وتعرض الوظائف ذات الصلة كنتائج.</span><span class="sxs-lookup"><span data-stu-id="06e71-156">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="06e71-157">بإمكان المرشحين تصفية النتائج في أي وقت، استنادًا إلى موقع الوظيفة أو مهمة الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="06e71-157">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="06e71-158">وبإمكان المرشحين أيضًا عرض مجموعة من الوظائف الموصى بها في موقع الوظائف.</span><span class="sxs-lookup"><span data-stu-id="06e71-158">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="06e71-159">تستند الوظائف الموصى بها لأحد المرشحين إلى استمارات التقديم السابقة للمرشح وملف تعريفه وسيره الذاتية.</span><span class="sxs-lookup"><span data-stu-id="06e71-159">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

>   [!NOTE] 
>   <span data-ttu-id="06e71-160">وتظهر توصيات الوظائف فقط إذا تم نشر 10 وظائف على الأقل في موقع الوظائف، وإذا كان الموظف قد أكمل ملف تعريفه.</span><span class="sxs-lookup"><span data-stu-id="06e71-160">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed a profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="06e71-161">تقديم طلبات للحصول على وظيفة</span><span class="sxs-lookup"><span data-stu-id="06e71-161">Apply for jobs</span></span>

<span data-ttu-id="06e71-162">بعد عثور المرشحين على الوظيفة المناسبة، يمكنهم تقديم الطلب باستخدام الزر **تقديم طلب** في صفحة **تفاصيل الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="06e71-162">After candidates find the right job, they can apply by using the **Apply** button on the **Job details** page.</span></span> <span data-ttu-id="06e71-163">في هذه المرحلة، بإمكان المرشحين إنشاء ملف تعريف جديد أو مراجعة المعلومات الموجودة في ملف تعريفهم الموجود.</span><span class="sxs-lookup"><span data-stu-id="06e71-163">At this point, candidates can either create a new profile or review the information in their existing profile.</span></span>
<span data-ttu-id="06e71-164">بإمكان المرشحين أيضًا تحميل سيرة ذاتية، كما هو مطلوب، ثم إرسال استمارة التقديم للوظيفة.</span><span class="sxs-lookup"><span data-stu-id="06e71-164">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="06e71-165">التحقق من حالة استمارة التقديم‬</span><span class="sxs-lookup"><span data-stu-id="06e71-165">Check application status</span></span>

<span data-ttu-id="06e71-166">بعد تقدم المرشحين بطلبات لوظيفة أو أكثر، يمكنهم تحديد **استمارات التقديم** على شريط التنقل الموجود أعلى الصفحة لعرض استمارات التقديم المفتوحة والمغلقة.</span><span class="sxs-lookup"><span data-stu-id="06e71-166">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="06e71-167">عندما يفتح المرشحون إحدى استمارات التقديم الخاصة بهم، يمكنهم الاطلاع على المرحلة الحالية وعلى أي إجراءات معلقة يجب عليهم إكمالها.</span><span class="sxs-lookup"><span data-stu-id="06e71-167">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="06e71-168">على سبيل المثال، إذا كان يجب على المرشح توفير التواريخ المحتملة لموعد مقابلة شخصية، يجب أن تعرض الصفحة الخيارات المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="06e71-168">For example, if a candidate must provide potential dates for an in-person interview, the page shows the available options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="06e71-169">الوظائف الداخلية</span><span class="sxs-lookup"><span data-stu-id="06e71-169">Internal jobs</span></span>

<span data-ttu-id="06e71-170">في الوقت الحالي، لا تظهر في موقع الوظائف الوظائف المميزة كوظائف داخلية ومنشورة في موقع الوظائف في Attract.</span><span class="sxs-lookup"><span data-stu-id="06e71-170">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="06e71-171">ويمكن الوصول إليها فقط عبر استخدام عنوان URL المباشر **تقديم طلب** الذي يمكن نسخه من استمارة التقديم في Attract.</span><span class="sxs-lookup"><span data-stu-id="06e71-171">They are only accessible using the direct **Apply** URL that can be copied from the Attract application.</span></span>
