---
title: إعداد تكامل LinkedIn مع Attract
description: يشرح هذا الموضوع كيفيه تكوين تكامل LinkedIn لـ Microsoft Dynamics 365 Talent - Attract كي تتمكن من نشر الوظائف بسهولة في LinkedIn من Attract، مما يسمح لمسؤولي التعيين بمزامنة معلومات التعيين لديهم مع ملف تعريف المرشح في LinkedIn.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 4c518fb7036d44aa52c8db859ee3616fc4e58a06
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833174"
---
# <a name="set-up-linkedin-integration-with-attract"></a><span data-ttu-id="07a70-103">إعداد تكامل LinkedIn مع Attract</span><span class="sxs-lookup"><span data-stu-id="07a70-103">Set up LinkedIn integration with Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="07a70-104">ساعد مسؤولي التعيين ومدراء التوظيف على جذب أهم المواهب من خلال تكوين تكامل LinkedIn مع Microsoft Dynamics 365 Talent: Attract:.</span><span class="sxs-lookup"><span data-stu-id="07a70-104">Help your recruiters and hiring managers attract top talent by configuring LinkedIn integration with Microsoft Dynamics 365 Talent: Attract.</span></span> <span data-ttu-id="07a70-105">يسمح لك Attract بنشر الوظائف مباشره في LinkedIn، أكبر شركة احترافية في العالم.‬</span><span class="sxs-lookup"><span data-stu-id="07a70-105">Attract lets you post jobs directly to LinkedIn, the largest professional online network.</span></span>

<span data-ttu-id="07a70-106">تعتبر الوظائف التي تنشرها في LinkedIn عبر Attract عروض وظائف محدودة وهي متوفر لشركتك من دون أي تكلفة إضافية.</span><span class="sxs-lookup"><span data-stu-id="07a70-106">Jobs that you post to LinkedIn through Attract are Limited Listings and are provided at no extra cost to your company.</span></span> <span data-ttu-id="07a70-107">تتوفر إدخالات عروض الوظائف هذه فقط من خلال شركاء برنامج LinkedIn مثل Attract.</span><span class="sxs-lookup"><span data-stu-id="07a70-107">These listings are available only through LinkedIn software partners such as Attract.</span></span> <span data-ttu-id="07a70-108">وهي لا تظهر في لوحة **المهن** في صفحة LinkedIn الخاصة بشركتك، لأن الإدخالات المدفوعة وحدها تظهر هناك.</span><span class="sxs-lookup"><span data-stu-id="07a70-108">They don't appear in the **Careers** panel on your company's LinkedIn page, because only paid listings appear there.</span></span> <span data-ttu-id="07a70-109">ومع ذلك، فهي تظهر عندما يستعرض المرشحون المحتملون كافة الوظائف المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="07a70-109">However, they are shown when potential candidates view all available jobs.</span></span> <span data-ttu-id="07a70-110">تظهر أيضًا عروض الوظائف المحدودة في عمليات البحث عن الوظائف في LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="07a70-110">Limited Listings are also shown in LinkedIn job searches.</span></span>

<span data-ttu-id="07a70-111">يوفر Attract طريقتين للتكامل مع LinkedIn لمساعدتك في البحث عن المرشحين من موقع الوظائف الرائج هذا:</span><span class="sxs-lookup"><span data-stu-id="07a70-111">Attract provides two ways to integrate with LinkedIn to help you source candidates from this popular career site:</span></span>

- <span data-ttu-id="07a70-112">نشر الوظائف من Attract في LinkedIn</span><span class="sxs-lookup"><span data-stu-id="07a70-112">Post jobs from Attract to LinkedIn.</span></span>
- <span data-ttu-id="07a70-113">نقل المرشحين من LinkedIn إلى Attract</span><span class="sxs-lookup"><span data-stu-id="07a70-113">Source candidates from LinkedIn to Attract.</span></span>

<span data-ttu-id="07a70-114">يمكنك تكوين الخيارات في علامة التبويب **تكامل LinkedIn** في مركز الإدارة.</span><span class="sxs-lookup"><span data-stu-id="07a70-114">You configure both options on the **LinkedIn Integration** tab in the Admin center.</span></span> <span data-ttu-id="07a70-115">لفتح مركز الإدارة، انتقل إلى <https://attract.talent.dynamics.com/adminsettings>.</span><span class="sxs-lookup"><span data-stu-id="07a70-115">To open the Admin center, go to <https://attract.talent.dynamics.com/adminsettings>.</span></span>

> [!NOTE]
> <span data-ttu-id="07a70-116">لاستخدام تكامل LinkedIn Recruiter مع Attract، تحتاج إلى [المكون الإضافي "التوظيف الشامل"](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) بالإضافة إلى [تراخيص LinkedIn Recruiter](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18).</span><span class="sxs-lookup"><span data-stu-id="07a70-116">To use LinkedIn Recruiter integration with Attract, you need the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) and [LinkedIn Recruiter licenses](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18).</span></span> <span data-ttu-id="07a70-117">لمزيد من المعلومات، راجع [أي إصدار من Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).</span><span class="sxs-lookup"><span data-stu-id="07a70-117">For more information, see [Which version of Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).</span></span>

<span data-ttu-id="07a70-118">إذا واجهت مشكلة ما في نشر الوظائف في LinkedIn، راجع [استكشاف أخطاء التكامل وإصلاحها مع LinkedIn‏‎ وMicrosoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="07a70-118">If you're having trouble posting jobs to LinkedIn, see [Troubleshooting integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md).</span></span>

<span data-ttu-id="07a70-119">للحصول على معلومات حول طرق أخرى لنشر الوظائف في LinkedIn، راجع [الأسئلة المتداولة حول تكامل Attract مع LinkedIn](./attract-linkedin-faq.md).</span><span class="sxs-lookup"><span data-stu-id="07a70-119">For information about other ways to post jobs to LinkedIn, see [Attract integration with LinkedIn FAQ](./attract-linkedin-faq.md).</span></span>

## <a name="configure-job-posting-to-linkedin"></a><span data-ttu-id="07a70-120">تكوين نشر الوظائف في LinkedIn</span><span class="sxs-lookup"><span data-stu-id="07a70-120">Configure job posting to LinkedIn</span></span>

<span data-ttu-id="07a70-121">قبل ان تتمكن من نشر الوظائف من Attract في LinkedIn، تحتاج إلى [معرّف شركة في LinkedIn](https://aka.ms/findID).</span><span class="sxs-lookup"><span data-stu-id="07a70-121">Before you can post jobs from Attract to LinkedIn, you need a [LinkedIn Company ID](https://aka.ms/findID).</span></span> <span data-ttu-id="07a70-122">يتكوّن معرّف الشركة في LinkedIn من سلسلة من الأرقام التي تعرف شركتك في LinkedIn بشكل فريد.</span><span class="sxs-lookup"><span data-stu-id="07a70-122">Your LinkedIn Company ID is a string of numbers that uniquely identifies your company in LinkedIn.</span></span> <span data-ttu-id="07a70-123">لمزيد من المعلومات، راجع [ربط معرّف شركتك في LinkedIn بلوحة وظائف LinkedIn - الأسئلة المتداولة](https://aka.ms/findID).</span><span class="sxs-lookup"><span data-stu-id="07a70-123">For more information, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://aka.ms/findID).</span></span>

<span data-ttu-id="07a70-124">يرسل Attract موجزًا لعمليات نشر الوظائف في LinkedIn، وتتحقق LinkedIn من الموجز مرة واحدة في اليوم تقريبًا.</span><span class="sxs-lookup"><span data-stu-id="07a70-124">Attract sends a feed of your job postings to LinkedIn, and LinkedIn checks for the feed approximately once per day.</span></span> <span data-ttu-id="07a70-125">قد يستغرق نشر الوظائف في الموقع حوالي 48 ساعة.</span><span class="sxs-lookup"><span data-stu-id="07a70-125">It can take up to 48 hours for your jobs to be posted to the site.</span></span>

<span data-ttu-id="07a70-126">تظهر إعلانات الوظائف المنشورة على LinkedIn في موقع LinkedIn المباشر.</span><span class="sxs-lookup"><span data-stu-id="07a70-126">Jobs that are posted to LinkedIn appear on the live LinkedIn site.</span></span> <span data-ttu-id="07a70-127">لا توجد لدى LinkedIn بيئة اختبار لنشر إعلانات الوظائف.</span><span class="sxs-lookup"><span data-stu-id="07a70-127">LinkedIn doesn't have a test environment for posting jobs.</span></span> <span data-ttu-id="07a70-128">لذلك، تأكد من عدم نشر أي وظائف اختبارية عن طريق الخطأ.</span><span class="sxs-lookup"><span data-stu-id="07a70-128">Therefore, make sure that you don't accidentally post any test jobs.</span></span> 

1. <span data-ttu-id="07a70-129">في قائمة **الإعداد** (رمز الترس) في الزاوية العلوية اليسرى، حدد **مركز الإدارة**.</span><span class="sxs-lookup"><span data-stu-id="07a70-129">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span> <span data-ttu-id="07a70-130">بدلاً من ذلك، انتقل إلى <https://attract.talent.dynamics.com/adminsettings>.</span><span class="sxs-lookup"><span data-stu-id="07a70-130">Alternatively, go to <https://attract.talent.dynamics.com/adminsettings>.</span></span>
2. <span data-ttu-id="07a70-131">حدد علامة التبويب **تكامل LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="07a70-131">Select the **LinkedIn Integration** tab.</span></span>
3. <span data-ttu-id="07a70-132">ضمن **اسم الشركة**، أدخل اسم شركتك، وضمن **معرّف الشركة**، أدخل معرّف شركتك في LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="07a70-132">Under **Company name**, enter the name of your company, and under **Company ID**, enter your LinkedIn Company ID.</span></span> <span data-ttu-id="07a70-133">تأكد من تطابق اسم الشركة مع الاسم الذي يظهر في صفحة شركتك على LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="07a70-133">Make sure that the company name matches the name that appears on your company's LinkedIn page.</span></span> <span data-ttu-id="07a70-134">لمزيد من المعلومات حول معرّفات الشركات في LinkedIn، راجع [ربط معرّف شركتك في LinkedIn بلوحة وظائف LinkedIn - الأسئلة المتداولة](https://www.linkedin.com/help/linkedin/answer/98972).</span><span class="sxs-lookup"><span data-stu-id="07a70-134">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>

    <span data-ttu-id="07a70-135">إذا احتجت إلى تغيير أي معلومات خاصة بمؤسستك، فراجع [تغيير عنوان مؤسستك وجهة الاتصال التقنية فيها والمزيد](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more).</span><span class="sxs-lookup"><span data-stu-id="07a70-135">If you need to change any information for your organization, see [Change your organization's address, technical contact, and more](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more).</span></span> <span data-ttu-id="07a70-136">وإذا بقيت تواجه بعض المشاكل، فاتصل بقسم [دعم LinkedIn](https://www.linkedin.com/help/linkedin).</span><span class="sxs-lookup"><span data-stu-id="07a70-136">If you still have issues, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>

4. <span data-ttu-id="07a70-137">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="07a70-137">Select **Save**.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="07a70-138">إعداد LinkedIn Recruiter مع Attract</span><span class="sxs-lookup"><span data-stu-id="07a70-138">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="07a70-139">للسماح لمسؤولي التعيين بالبحث عن الوظائف من خلال LinkedIn Recruiter، يجب تكوين التكامل مع LinkedIn Recruiter في Attract.</span><span class="sxs-lookup"><span data-stu-id="07a70-139">To allow recruiters to source jobs through LinkedIn Recruiter, you must configure integration with LinkedIn Recruiter in Attract.</span></span> <span data-ttu-id="07a70-140">لإكمال عملية التكوين، ستحتاج إلى العمل مع المستخدم الذي يؤدي دور المسؤول في عقد LinkedIn Recruiter الخاص بمؤسستك.</span><span class="sxs-lookup"><span data-stu-id="07a70-140">To complete the configuration process, you must work with the user who is an admin on your organization's LinkedIn Recruiter contract.</span></span>

1. <span data-ttu-id="07a70-141">في قائمة **الإعداد** (رمز الترس) في الزاوية العلوية اليسرى، حدد **مركز الإدارة**.</span><span class="sxs-lookup"><span data-stu-id="07a70-141">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span> <span data-ttu-id="07a70-142">بدلاً من ذلك، انتقل إلى <https://attract.talent.dynamics.com/adminsettings>.</span><span class="sxs-lookup"><span data-stu-id="07a70-142">Alternatively, go to <https://attract.talent.dynamics.com/adminsettings>.</span></span>
2. <span data-ttu-id="07a70-143">حدد علامة التبويب **تكامل LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="07a70-143">Select the **LinkedIn Integration** tab.</span></span>

    <span data-ttu-id="07a70-144">[![طريقة عرض مسؤول Attract لبدء تكامل LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="07a70-144">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3. <span data-ttu-id="07a70-145">حدد **اتصال** لبدء الإعداد.</span><span class="sxs-lookup"><span data-stu-id="07a70-145">Select **Connect** to start the setup.</span></span> <span data-ttu-id="07a70-146">سيتم إرشادك من خلال عملية تسجيل الدخول إلى LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="07a70-146">You will be guided through the LinkedIn sign-in process.</span></span>
4. <span data-ttu-id="07a70-147">إذا كان لديك مقاعد في عقود LinkedIn متعددة، فحدد العقد الذي تريد توصيله بنظام Attract.</span><span class="sxs-lookup"><span data-stu-id="07a70-147">If you have seats on multiple LinkedIn contracts, select the contract that you want to connect to the Attract system.</span></span> <span data-ttu-id="07a70-148">إذا كان لديك مقعد في عقد LinkedIn واحد فقط، فيمكنك تخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="07a70-148">If you have a seat on only one LinkedIn contract, you can skip this step.</span></span>
5. <span data-ttu-id="07a70-149">ضمن **Recruiter System Connect (RSC)**، حدد **طلب‏‎**.</span><span class="sxs-lookup"><span data-stu-id="07a70-149">Under **Recruiter System Connect (RSC)**, select **Request**.</span></span>

    <span data-ttu-id="07a70-150">[![طريقة عرض مسؤول Attract لطلب تكامل LinkedIn Recruiter](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="07a70-150">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6. <span data-ttu-id="07a70-151">من المفترض أن يظهر إعداد **Recruiter System Connect (RSC)** الآن على الشكل **الشريك جاهز‬‏‫**.</span><span class="sxs-lookup"><span data-stu-id="07a70-151">The **Recruiter System Connect (RSC)** setting should now appear as **Partner ready**.</span></span> <span data-ttu-id="07a70-152">إذا رأيت **إعلام الشريك** على هذه الصفحة، فانتظر بضع ثوان، وحدد **إعلام الشريك**، ثم قم بتحديث الصفحة.</span><span class="sxs-lookup"><span data-stu-id="07a70-152">If you see **Notify partner** on this page, wait a few seconds, select **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="07a70-153">يجب أن يظهر الإعداد الآن على الشكل **الشريك جاهز**.</span><span class="sxs-lookup"><span data-stu-id="07a70-153">The setting should now appear as **Partner ready**.</span></span>

    <span data-ttu-id="07a70-154">[![طريقة عرض المسؤول في Attract للإشارة إلى استكمال الطلبات من جانب Attract](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="07a70-154">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

7. <span data-ttu-id="07a70-155">لإكمال الخطوات التالية، تحتاج إلى امتيازات المسؤول على عقد LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="07a70-155">To complete the following steps, you must have admin privileges on your LinkedIn Recruiter contract.</span></span>

    1. <span data-ttu-id="07a70-156">سجل دخولك إلى LinkedIn باستخدام حساب المسؤول، ثم حدد **LinkedIn Recruiter**في الجزء العلوي الأيسر.</span><span class="sxs-lookup"><span data-stu-id="07a70-156">Sign in to LinkedIn by using your admin account, and then select **LinkedIn Recruiter** in the upper right.</span></span> 
    2. <span data-ttu-id="07a70-157">في قائمة **المزيد** في أعلى الشاشة، حدد **إعدادات المسؤول**، ثم حدد علامة التبويب **ATS**.</span><span class="sxs-lookup"><span data-stu-id="07a70-157">On the **More** menu at the top of the page, select **Admin Settings**, and then select the **ATS** tab.</span></span>
    3. <span data-ttu-id="07a70-158">لتمكين التصدير بنقرة واحدة لعقد واحد فقط، قم بتشغيل الخيار **الوصول على مستوي العقد (لكل مقعد على هذا العقد)**.</span><span class="sxs-lookup"><span data-stu-id="07a70-158">To enable one-click export for just one contract, turn on **Contract Level access (for every seat on this contract**.</span></span> <span data-ttu-id="07a70-159">لتمكينه للشركة بكاملها، قم بتشغيل الخيار **الوصول على مستوى الشركة‬‏‫ (لكل عقد في شركتك)**.</span><span class="sxs-lookup"><span data-stu-id="07a70-159">To enable it for the whole company, turn on **Company Level access (for every contract in your company**.</span></span>

    <span data-ttu-id="07a70-160">[![تشغيل تكامل Attract من طريقة عرض مسؤول LinkedIn Recruiter](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="07a70-160">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

8. <span data-ttu-id="07a70-161">في مركز إدارة Attract، حدد علامة التبويب **تكامل LinkedIn**. من المفترض أن يظهر الآن الإعداد **Recruiter System Connect (RSC)** على الشكل **ممكّن**.</span><span class="sxs-lookup"><span data-stu-id="07a70-161">In the Attract Admin center, select the **LinkedIn integration** tab. The **Recruiter System Connect (RSC)** setting should now appear as **Enabled**.</span></span>

    <span data-ttu-id="07a70-162">[![اكتمال تكامل LinkedIn Recruiter](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="07a70-162">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="set-up-apply-with-linkedin-in-attract"></a><span data-ttu-id="07a70-163">إعداد "التقدم بطلب عبر LinkedIn" في Attract</span><span class="sxs-lookup"><span data-stu-id="07a70-163">Set up Apply with LinkedIn in Attract</span></span>

<span data-ttu-id="07a70-164">يمكنك السماح للمرشحين بتقديم طلبات للحصول على وظائفك باستخدام ملفات تعريفهم في LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="07a70-164">You can allow candidates to apply to your jobs by using their LinkedIn profiles.</span></span> <span data-ttu-id="07a70-165">لمزيد من المعلومات حول إعداد "التقدم بطلب عبر LinkedIn، راجع [قوة LinkedIn في كل مكان: التقدم بطلب عبر LinkedIn](https://blog.linkedin.com/2011/07/24/apply-with-linkedin).</span><span class="sxs-lookup"><span data-stu-id="07a70-165">For more information about Apply with LinkedIn, see [The Power of LinkedIn Everywhere: Apply with LinkedIn](https://blog.linkedin.com/2011/07/24/apply-with-linkedin).</span></span>

<span data-ttu-id="07a70-166">هذه الميزة قيد المعاينة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="07a70-166">This feature is currently in preview.</span></span> <span data-ttu-id="07a70-167">قبل اتباع هذه الخطوات، تأكد من تمكين "التقدم بطلب عبر LinkedIn".</span><span class="sxs-lookup"><span data-stu-id="07a70-167">Before you follow these steps, make sure that Apply with LinkedIn is enabled.</span></span> <span data-ttu-id="07a70-168">لمزيد من المعلومات حول كيفية تمكين ميزات المعاينة، راجع [الوصول إلى ميزات المعاينة في Microsoft Dynamics 365 Talent](./access-preview-feature.md).</span><span class="sxs-lookup"><span data-stu-id="07a70-168">For more information about how to enable preview features, see [Access preview features in Microsoft Dynamics 365 Talent](./access-preview-feature.md).</span></span>

1. <span data-ttu-id="07a70-169">في قائمة **الإعداد** (رمز الترس) في الزاوية العلوية اليسرى، حدد **مركز الإدارة**.</span><span class="sxs-lookup"><span data-stu-id="07a70-169">On the **Setup** menu (the gear symbol) in the upper-right corner, select **Admin center**.</span></span> <span data-ttu-id="07a70-170">بدلاً من ذلك، انتقل إلى <https://attract.talent.dynamics.com/adminsettings>.</span><span class="sxs-lookup"><span data-stu-id="07a70-170">Alternatively, go to <https://attract.talent.dynamics.com/adminsettings>.</span></span>
2. <span data-ttu-id="07a70-171">حدد علامة التبويب **تكامل LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="07a70-171">Select the **LinkedIn Integration** tab.</span></span>

    <span data-ttu-id="07a70-172">[![طريقة عرض مسؤول Attract لبدء تكامل LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="07a70-172">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3. <span data-ttu-id="07a70-173">إلى جانب **التقدم بطلب عبر LinkedIn**، حدد **اتصال** لبدء الإعداد.</span><span class="sxs-lookup"><span data-stu-id="07a70-173">Next to **Apply with LinkedIn**, select **Connect** to start the setup.</span></span> <span data-ttu-id="07a70-174">سيتم إرشادك عبر الجزء المتبقي من العملية مع LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="07a70-174">You will be guided through the rest of the process with LinkedIn.</span></span>

## <a name="see-also"></a><span data-ttu-id="07a70-175">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="07a70-175">See also</span></span>

[<span data-ttu-id="07a70-176">الأسئلة المتداولة حول تكامل Attract مع LinkedIn</span><span class="sxs-lookup"><span data-stu-id="07a70-176">Attract integration with LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="07a70-177">نشر الوظائف في مواقع مهن خارجية من Attract</span><span class="sxs-lookup"><span data-stu-id="07a70-177">Post jobs to external career sites from Attract</span></span>](./posting-jobs-external.md)

[<span data-ttu-id="07a70-178">بحث عن المرشحين باستخدام LinkedIn Recruiter في Microsoft Dynamics 365 Talent - Attract</span><span class="sxs-lookup"><span data-stu-id="07a70-178">Source candidates with LinkedIn Recruiter in Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="07a70-179">إنشاء الوظائف والموافقة عليها ونشرها في Attract</span><span class="sxs-lookup"><span data-stu-id="07a70-179">Create, approve, and post jobs in Attract</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="07a70-180">استكشاف أخطاء التكامل وإصلاحها مع LinkedIn وMicrosoft Dynamics 365 Talent - Attract</span><span class="sxs-lookup"><span data-stu-id="07a70-180">Troubleshooting integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-troubleshoot-linkedin.md)
