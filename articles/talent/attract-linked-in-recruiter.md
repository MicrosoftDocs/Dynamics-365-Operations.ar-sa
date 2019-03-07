---
title: التوريد باستخدام LinkedIn Recruiter
description: يوفر هذا الموضوع معلومات حول استخدام التعلم الآلي‬ للحصول على توصيات بشأن وظيفة ومرشح الوظيفة.
author: josaw
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 9bb323728923ff3b09ff0bfba3849f3c5d84eb34
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "303053"
---
# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="4c459-103">التوريد باستخدام LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="4c459-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="4c459-104">يُعتبر LinkedIn أكبر قاعدة بيانات للمواهب في العالم، وهو في أغلب الأحيان النظام الرئيسي الذي يستعين به مسؤولو التعيين للبحث عن مرشحين للوظائف التي يسعون إلى ملئها وللتواصل مع هؤلاء المرشحين وتوريدهم.</span><span class="sxs-lookup"><span data-stu-id="4c459-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="4c459-105">بفضل تكامل LinkedIn Recruiter مع Dynamics 365 for Talent: Attract بإمكان المستخدمين تنفيذ عملية التوظيف والمحافظة على مزامنة البيانات بين النظامين.</span><span class="sxs-lookup"><span data-stu-id="4c459-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="4c459-106">إنك تحتاج إلى المكون الإضافي Comprehensive Hiring ومقاعد LinkedIn Recruiter كي تتمكن من استخدام تكامل LinkedIn Recruiter مع Attract.</span><span class="sxs-lookup"><span data-stu-id="4c459-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="4c459-107">إعداد LinkedIn Recruiter مع Attract</span><span class="sxs-lookup"><span data-stu-id="4c459-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="4c459-108">قبل أن تتمكن من استخدام قدرات LinkedIn Recruiter، يجب عليك تكوين الوصول على مستوى العقد أو على مستوى الشركة مع مثيل Attract.</span><span class="sxs-lookup"><span data-stu-id="4c459-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="4c459-109">لإكمال عملية التكوين، ستحتاج إلى العمل مع المستخدم الذي يؤدي دور المسؤول في عقد LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="4c459-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="4c459-110">أكمل الخطوات التالية لتكوين LinkedIn Recruiter مع Attract.</span><span class="sxs-lookup"><span data-stu-id="4c459-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="4c459-111">سجّل الدخول إلى Attract كمسؤول، وانتقل إلى **إعدادات المسؤول**.</span><span class="sxs-lookup"><span data-stu-id="4c459-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="4c459-112">في الجزء الأيمن، انقر فوق علامة تبويب **تكامل LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="4c459-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="4c459-113">[![طريقة عرض مسؤول Attract لبدء تكامل LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="4c459-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="4c459-114">انقر فوق **اتصال** لبدء الإعداد وكي يتم توجيهك من خلال عملية تسجيل الدخول LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="4c459-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="4c459-115">إذا كان لديك مقاعد في عقود LinkedIn متعددة، فحدد العقد الذي تريد توصيله بنظام Attract.</span><span class="sxs-lookup"><span data-stu-id="4c459-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="4c459-116">إذا كان لديك مقعد في عقد LinkedIn واحد فقط، فلن تحتاج إلى هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="4c459-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="4c459-117">يتم الآن تحميل عنصر واجهة مستخدم LinkedIn في إعدادات المسؤول مع قائمة عمليات التكامل التي تظهر.</span><span class="sxs-lookup"><span data-stu-id="4c459-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="4c459-118">ضمن **Recruiter System connect**، انقر فوق **طلب**.</span><span class="sxs-lookup"><span data-stu-id="4c459-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="4c459-119">[![طريقة عرض مسؤول Attract لطلب تكامل LinkedIn Recruiter](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="4c459-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="4c459-120">بعد طلب التكامل من Attract، سوف يظهر على شكل **الشريك جاهز** وسيكون جاهزًا لتشغيله من **إعدادات مسؤول التعيين**.</span><span class="sxs-lookup"><span data-stu-id="4c459-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="4c459-121">إذا رأيت **إعلام الشريك** على هذه الصفحة، فانتظر بضع ثوان، وانقر فوق **إعلام الشريك**، ثم قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4c459-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="4c459-122">يجب أن يظهر الآن على الشكل **الشريك جاهز**.</span><span class="sxs-lookup"><span data-stu-id="4c459-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="4c459-123">[![طريقة عرض المسؤول في Attract للإشارة إلى استكمال الطلبات من جانب Attract](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="4c459-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="4c459-124">لإكمال الخطوة التالية، تحتاج إلى امتياز المسؤول على عقد LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="4c459-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="4c459-125">سجّل دخولك إلى LinkedIn باستخدام حساب المسؤول وانتقل إلى LinkedIn Recruiter في الجانب العلوي الأيسر.</span><span class="sxs-lookup"><span data-stu-id="4c459-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="4c459-126">في قائمة **المزيد** في أعلى الشاشة، انقر فوق **إعدادات المسؤول**، ثم فوق علامة التبويب **ATS**.</span><span class="sxs-lookup"><span data-stu-id="4c459-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="4c459-127">سيكون نظام Attract مدرجًا مع بعض الخيارات التي يمكن تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="4c459-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="4c459-128">إذا أردت تمكين التصدير بنقرة واحدة **لمؤشر In-ATS** و**عنصر واجهة مستخدم ملف تعريف In-ATS**، حدد **الوصول على مستوى الشركة**.</span><span class="sxs-lookup"><span data-stu-id="4c459-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="4c459-129">إذا أردت تمكين كافة ميزات الوصول على مستوى الشركة بالإضافة إلى محفوظات InMail ومحفوظات الملاحظات والوصول إلى ملف تعريف InMail الموجز، فحدد **الوصول على مستوى العقد**.</span><span class="sxs-lookup"><span data-stu-id="4c459-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="4c459-130">قم بتشغيل مستوى الوصول المطلوب من إعدادات LinkedIn Recruiter **Admin-ATS**.</span><span class="sxs-lookup"><span data-stu-id="4c459-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="4c459-131">[![تشغيل تكامل Attract من طريقة عرض مسؤول LinkedIn Recruiter](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="4c459-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="4c459-132">عد إلى إعدادات مسؤول Attract بصفتك AttractAdmin وحدد علامة التبويب **تكامل LinkedIn**. من المفترض أن ترى الآن تحميل عنصر واجهة مستخدم LinkedIn الذي يعرض **ممكّن** مع تشغيل مستوى الوصول المحدد.</span><span class="sxs-lookup"><span data-stu-id="4c459-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="4c459-133">[![اكتمال تكامل LinkedIn Recruiter](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="4c459-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="4c459-134">استخدام قدرات LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="4c459-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="4c459-135">بعد تمكين قدرات LinkedIn بواسطة مسؤول Attract، يمكن لمسؤولي التعيين ومدراء التوظيف الوصول إليها.</span><span class="sxs-lookup"><span data-stu-id="4c459-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="4c459-136">لاستخدام هذه القدرات، قم بتوصيل حسابك في LinkedIn ضمن **إعدادات المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="4c459-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="4c459-137">ستتوفر قدرات متعددة بعد توصيل إعدادات المسؤول والمستخدم.</span><span class="sxs-lookup"><span data-stu-id="4c459-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="4c459-138">عنصر واجهة المستخدم لملف التعريف In-ATS</span><span class="sxs-lookup"><span data-stu-id="4c459-138">In-ATS profile widget</span></span>

<span data-ttu-id="4c459-139">يمكن عرض ملف تعريف LinkedIn للمرشح في Attract.</span><span class="sxs-lookup"><span data-stu-id="4c459-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="4c459-140">سيعرض عنصر واجهة مستخدم LinkedIn ملف تعريف المرشح عندما تتطابق معلومات ATS مع معلومات LinkedIn لمستخدميها.</span><span class="sxs-lookup"><span data-stu-id="4c459-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="4c459-141">لعرض ملف تعريف، انتقل إلى ملف تعريف المرشح من مجموعة وظائف أو مجموعة مواهب.</span><span class="sxs-lookup"><span data-stu-id="4c459-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="4c459-142">في ملف تعريف المرشح، حدد علامة تبويب **LinkedIn**، وسيتم تحميل عنصر واجهة مستخدم ملف التعريف.</span><span class="sxs-lookup"><span data-stu-id="4c459-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="4c459-143">يمكنك أيضًا حفظ المرشح إلى مشاريعك في LinkedIn Recruiter من هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4c459-143">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>
1. <span data-ttu-id="4c459-144">إذا عثر LinkedIn على التطابق استنادًا إلى البريد الإلكتروني ومعرّف عضو LinkedIn (تطابق تام)، فسيظهر ملف تعريف المرشح.</span><span class="sxs-lookup"><span data-stu-id="4c459-144">If LinkedIn found the match based on email and LinkedIn member ID (exact match), the candidate's profile will be shown.</span></span> <span data-ttu-id="4c459-145">يبقى باستطاعة المستخدم ربط/إلغاء ربط ملف التعريف.</span><span class="sxs-lookup"><span data-stu-id="4c459-145">The user still has an option to link/unlink the profile.</span></span>

2. <span data-ttu-id="4c459-146">إذا تعذر على LinkedIn العثور على المرشح استنادًا إلى البريد الإلكتروني أو معرّف العضو، فسيعرض قائمة تتضمن تطابقات المرشحين المحتملة استنادًا إلى اسم المرشح ويستطيع المستخدم اختيار أحدها وربط ملف التعريف.</span><span class="sxs-lookup"><span data-stu-id="4c459-146">If LinkedIn cannot find the candidate based on their email or member ID, it will show a list of possible candidate matches based on candidate name and the user can choose one of them and link the profile.</span></span>  

3. <span data-ttu-id="4c459-147">إذا تعذر على LinkedIn العثور على أي مرشح استنادًا إلى الاسم، فإن النتائج التي سيرجعها ستشير إلى عدم العثور على أي تطابق.</span><span class="sxs-lookup"><span data-stu-id="4c459-147">If LinkedIn cannot find any candidate based on the name, it will return that no match was found.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="4c459-148">التصدير بنقرة واحدة</span><span class="sxs-lookup"><span data-stu-id="4c459-148">1-click export</span></span> 

<span data-ttu-id="4c459-149">أثناء توريد المرشحين في LinkedIn، يمكنك تصدير بنقرة واحدة مرشح الوظائف المفتوحة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="4c459-149">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="4c459-150">أكمل الخطوات التالية للتصدير بنقرة واحدة.</span><span class="sxs-lookup"><span data-stu-id="4c459-150">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="4c459-151">قبل إتمام هذه الخطوات، تأكد من أنك تملك دور مدير التوظيف أو مسؤول التعيين للوظيفة وأن هذه الوظيفة موجودة في مرحلة **الموظف المحتمل**.</span><span class="sxs-lookup"><span data-stu-id="4c459-151">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="4c459-152">أنشئ الوظيفة وعيّن الأدوار المناسبة وقم بتنشيط الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="4c459-152">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="4c459-153">عندما يتم تنشيط الوظيفة، انتقل إلى LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="4c459-153">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="4c459-154">ابحث عن المرشح الذي تراه مناسبًا للوظيفة ثم انتقل إلى ملف تعريفه.</span><span class="sxs-lookup"><span data-stu-id="4c459-154">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="4c459-155">باستخدام مربع بحث الوظيفة الموجود في بطاقة جهة الاتصال، ابحث عن الوظيفة باستخدام المسمى الوظيفي أو معرّف الوظيفة الذي تم تنشيطه في Attract.</span><span class="sxs-lookup"><span data-stu-id="4c459-155">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="4c459-156">إذا لم تعثر على الوظيفة، فانقر فوق **تغيير ATS‎** للعثور على مثيل Attract الصحيح.</span><span class="sxs-lookup"><span data-stu-id="4c459-156">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="4c459-157">بعد تحديد الوظيفة، انقر فوق **تصدير**.</span><span class="sxs-lookup"><span data-stu-id="4c459-157">After the job is selected, click **Export**.</span></span> <span data-ttu-id="4c459-158">تم الآن إحضار الموظف بواسطة Attract.</span><span class="sxs-lookup"><span data-stu-id="4c459-158">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="4c459-159">انتقل إلى Attract وافتح الوظيفة المناظرة.</span><span class="sxs-lookup"><span data-stu-id="4c459-159">Go to Attract and open the respective job.</span></span> <span data-ttu-id="4c459-160">سوف تعثر على المرشح الذي قمت للتوّ بتصديره في مرحلة **الموظف المحتمل** للوظيفة.</span><span class="sxs-lookup"><span data-stu-id="4c459-160">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="4c459-161">مؤشر In-ATS</span><span class="sxs-lookup"><span data-stu-id="4c459-161">In-ATS indicator</span></span> 

<span data-ttu-id="4c459-162">باستخدام LinkedIn Recruiter، يمكنك تعقب ما إذا كان المرشح قد تقدم بطلبات حصول على وظائف أخرى في مؤسستك، والاطلاع على وجودهم في مختلف مراحل تقديم طلبات الوظائف وعرض الملاحظات والتعليقات من LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="4c459-162">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="4c459-163">افتح LinkedIn Recruiter وحدد موقع ملف تعريف المرشح الذي تبحث عنه.</span><span class="sxs-lookup"><span data-stu-id="4c459-163">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="4c459-164">قم بالتمرير لأسفل لعرض القسم **In-ATS** في ملف تعريف المرشح.</span><span class="sxs-lookup"><span data-stu-id="4c459-164">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="4c459-165">يمكنك استخدام عنصر واجهة المستخدم هذا لعرض كافة المعلومات المتعلقة بالمرشح الموجود في Attract من ضمن طريقة عرض LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="4c459-165">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="4c459-166">حدد علامة التبويب **الوظائف والحالات** للاطلاع على الوظائف التي هي عبارة عن جزء منها، والحالات الأخيرة، وكيف تم نقلها في مقابل كل وظيفة.</span><span class="sxs-lookup"><span data-stu-id="4c459-166">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="4c459-167">حدد علامة التبويب **ملاحظات المقابلة** للاطلاع على الملاحظات التي أرسلها المحاورون في Attract.</span><span class="sxs-lookup"><span data-stu-id="4c459-167">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="4c459-168">حدد علامة تبويب **الملاحظات** لمشاهدة الملاحظات التي تم التقاطها لمقدم الطلب هذا في Attract.</span><span class="sxs-lookup"><span data-stu-id="4c459-168">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="4c459-169">لن تتم مزامنة بيانات المرشح واستمارة التقديم مع LinkedIn Recruiter إذا لم ينتقل المرشح إلى مرحلة الموظف المحتمل.</span><span class="sxs-lookup"><span data-stu-id="4c459-169">Candidate and application data will not be synced to LinkedIn Recruiter if the candidate hasn't moved past the prospect stage.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="4c459-170">محفوظات InMail</span><span class="sxs-lookup"><span data-stu-id="4c459-170">InMail history</span></span>

<span data-ttu-id="4c459-171">تتوفر محفوظات LinkedIn InMail من خلال وصول على مستوى العقد مع LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="4c459-171">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="4c459-172">عند تمكينها، يمكنك عرض محفوظات InMail بالكامل مع المرشح.</span><span class="sxs-lookup"><span data-stu-id="4c459-172">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="4c459-173">يمكنك أيضًا معرفة من هم الأشخاص الآخرون في مؤسستك الذين تبادلوا InMail مع المرشح، ولكن لا يمكنك الاطلاع على محتوى الرسائل بينهم.</span><span class="sxs-lookup"><span data-stu-id="4c459-173">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="4c459-174">لعرض محفوظات InMail، انتقل إلى ملف تعريف المرشح، وانتقل إلى علامة التبويب **LinkedIn** وقم بالتمرير إلى أسفل الصفحة لعرض المحفوظات.</span><span class="sxs-lookup"><span data-stu-id="4c459-174">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="4c459-175">يمكنك عرض محفوظات InMail إذا أجريت مناقشة مع المرشح.</span><span class="sxs-lookup"><span data-stu-id="4c459-175">You can view InMail history if you have had a discussion with the candidate.</span></span> <span data-ttu-id="4c459-176">ستتزامن الرسائل من InMail مع Attract كل ساعتين.</span><span class="sxs-lookup"><span data-stu-id="4c459-176">The messages from InMail will sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="4c459-177">محفوظات الملاحظات</span><span class="sxs-lookup"><span data-stu-id="4c459-177">Notes history</span></span> 

<span data-ttu-id="4c459-178">تتوفر محفوظات ملاحظات LinkedIn مع وصول على مستوى العقد مع LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="4c459-178">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="4c459-179">عند تمكين هذه المحفوظات، يمكنك عرض الملاحظات حول المرشح التي التقطها مسؤولو تعيين مختلفين من مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="4c459-179">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="4c459-180">لعرض محفوظات الملاحظات، انتقل إلى ملف تعريف المرشح، وانتقل إلى علامة التبويب **LinkedIn** وقم بالتمرير إلى أسفل الصفحة لعرض المحفوظات.</span><span class="sxs-lookup"><span data-stu-id="4c459-180">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="4c459-181">يمكنك عرض كافة الملاحظات حول المرشح من LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="4c459-181">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="4c459-182">ملف تعريف InMail الموجز</span><span class="sxs-lookup"><span data-stu-id="4c459-182">InMail stub profile</span></span>

<span data-ttu-id="4c459-183">يتوفر ملف تعريف InMail الموجز مع وصول على مستوى العقد مع LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="4c459-183">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="4c459-184">إذا وافق المرشح على مشاركة ملفات تعريفه في LinkedIn مع أي مستخدم في مؤسستك، فيمكن تعقب المرشحين في Attract، وسيتم إنشاء سجل مرشح جديد لكل المرشح.</span><span class="sxs-lookup"><span data-stu-id="4c459-184">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span> <span data-ttu-id="4c459-185">يمكنك عرض عنوان البريد الإلكتروني للمرشح إذا كان المرشح موجودًا في النظام ولديه عنوان بريد إلكتروني أو إذا اختار مشاركة عنوانه مع مسؤول التعيين.</span><span class="sxs-lookup"><span data-stu-id="4c459-185">You can view candidate's email address if the candidate already exists in the system with an email address or has chosen to share their address with the recruiter.</span></span>

<span data-ttu-id="4c459-186">لعرض قائمة المرشحين، انتقل إلى **مجموعات المواهب** للاطلاع على مجموعة مواهب LinkedIn أنشأها النظام.</span><span class="sxs-lookup"><span data-stu-id="4c459-186">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="4c459-187">تحتوي مجموعة المواهب هذه على المرشحين المدرجين وملفات تعريفهم الموجزة كما تم استلامها من LinkedIn، حيث يظهر الاسم الأول للمرشح واسم عائلته.</span><span class="sxs-lookup"><span data-stu-id="4c459-187">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="4c459-188">سيظهر معرّف البريد الإلكتروني للمرشح إذا اختار المرشح مشاركة عنوان بريده الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="4c459-188">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>
