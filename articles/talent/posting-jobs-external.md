---
title: نشر الوظائف في مواقع وظائف خارجية من Attract
description: يشرح هذا الموضوع كيفية استخدام Dynamics 365 for Talent - Attract لنشر الوظائف في مواقع توظيف خارجية.
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 1653d1e28d02f8a9a4bea8df562ac98d7a350ed1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/15/2019
ms.locfileid: "993658"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="312f5-103">نشر الوظائف في مواقع وظائف خارجية من Attract</span><span class="sxs-lookup"><span data-stu-id="312f5-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="312f5-104">تريد عرض المناصب المفتوحة أمام عدد أكبر عدد ممكن من المرشحين المؤهلين.</span><span class="sxs-lookup"><span data-stu-id="312f5-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="312f5-105">تساعدك مواقع التوظيف مثل Broadbean في تحقيق هذا الهدف.</span><span class="sxs-lookup"><span data-stu-id="312f5-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="312f5-106">يسمح لك الآن Microsoft Dynamics 365 Talent: Attract بنشر الوظائف في Broadbean، وتعمل Microsoft بشكل مستمر على تقديم عروض جديدة في هذا المجال.</span><span class="sxs-lookup"><span data-stu-id="312f5-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="312f5-107">نشر وظائف في Broadbean</span><span class="sxs-lookup"><span data-stu-id="312f5-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="312f5-108">قبل أن تتمكن من نشر الوظائف في Broadbean، يجب عليك تكوين تكامل Broadbean.</span><span class="sxs-lookup"><span data-stu-id="312f5-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="312f5-109">لنشر الوظائف في مواقع خارجية، يجب استخدام [المكون الإضافي "التوظيف الشامل"](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="312f5-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="312f5-110">هذه الميزة قيد المعاينة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="312f5-110">This feature is currently in preview.</span></span> <span data-ttu-id="312f5-111">إذا أردت تجربتها، فيجب [تشغيلها في إعدادات إدارة Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="312f5-111">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="312f5-112">تكوين تكامل Broadbean</span><span class="sxs-lookup"><span data-stu-id="312f5-112">Configure Broadbean integration</span></span>

1. <span data-ttu-id="312f5-113">سجل دخولك إلى Attract كمسؤول.</span><span class="sxs-lookup"><span data-stu-id="312f5-113">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="312f5-114">حدد زر **الإعدادات** (رمز الترس) في الزاوية العلوية اليسرى من الصفحة، ثم حدد **مركز الإدارة**.</span><span class="sxs-lookup"><span data-stu-id="312f5-114">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="312f5-115">على علامة التبويب **إعدادات لوحة الوظائف**، في القسم **تمكين تكامل Broadbean**، قم بتشغيل التكامل.</span><span class="sxs-lookup"><span data-stu-id="312f5-115">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="312f5-116">اتصل بموقع Broadbean، وأدخل معلوماتك في **Username, Client ID, Encryption Token**.</span><span class="sxs-lookup"><span data-stu-id="312f5-116">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="312f5-117">تعتبر بيانات اعتمادك في Broadbean سرية وحساسة لحالة الأحرف.</span><span class="sxs-lookup"><span data-stu-id="312f5-117">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="312f5-118">وبالتالي، يجب تخزينها ومشاركتها بطريقة مسؤولة.</span><span class="sxs-lookup"><span data-stu-id="312f5-118">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="312f5-119">بإمكان أي شخص يؤدي دور المسؤول في Attract عرض بيانات الاعتماد هذه.</span><span class="sxs-lookup"><span data-stu-id="312f5-119">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="312f5-120">لا تشارك Microsoft كما لا يشارك Attract في إنشاء هذه القيم والمحافظة عليها.</span><span class="sxs-lookup"><span data-stu-id="312f5-120">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="312f5-121">تقع على عاتقك مسؤولية تحديثها بشكل مستمر في Attract والعمل مع Broadbean على حل أي مشكلة تتعلق ببيانات اعتمادك.</span><span class="sxs-lookup"><span data-stu-id="312f5-121">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="312f5-122">نشر وظيفة في Broadbean</span><span class="sxs-lookup"><span data-stu-id="312f5-122">Post a job to Broadbean</span></span>

<span data-ttu-id="312f5-123">بعد تشغيل Broadbean، بإمكان المسؤولين ومسؤولي التعيين نشر وظائف فيه.</span><span class="sxs-lookup"><span data-stu-id="312f5-123">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="312f5-124">يجب أن يتوفر لديك عنوان URL لتقديم الطلب للوظيفة.</span><span class="sxs-lookup"><span data-stu-id="312f5-124">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="312f5-125">في Attract، افتح الوظيفة التي تريد نشرها في Broadbean.</span><span class="sxs-lookup"><span data-stu-id="312f5-125">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="312f5-126">في قسم **عمليات النشر**، حدد الزر **نشر الآن** الذي يتوافق مع Broadbean.</span><span class="sxs-lookup"><span data-stu-id="312f5-126">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="312f5-127">اتبع الإرشادات في نافذة Broadbean.</span><span class="sxs-lookup"><span data-stu-id="312f5-127">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="312f5-128">يقوم Attract بتمرير المعلومات التالية إلى Broadbean:</span><span class="sxs-lookup"><span data-stu-id="312f5-128">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="312f5-129">معرف الطلب</span><span class="sxs-lookup"><span data-stu-id="312f5-129">Request ID</span></span>
- <span data-ttu-id="312f5-130">المسمى الوظيفي</span><span class="sxs-lookup"><span data-stu-id="312f5-130">Job title</span></span>
- <span data-ttu-id="312f5-131">وصف الوظيفة</span><span class="sxs-lookup"><span data-stu-id="312f5-131">Job description</span></span>
- <span data-ttu-id="312f5-132">موقع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="312f5-132">Job location</span></span>
- <span data-ttu-id="312f5-133">عنوان URL لتقديم الطلب</span><span class="sxs-lookup"><span data-stu-id="312f5-133">Apply URL</span></span>
- <span data-ttu-id="312f5-134">معلومات مسؤول التعيين</span><span class="sxs-lookup"><span data-stu-id="312f5-134">Recruiter information</span></span>

<span data-ttu-id="312f5-135">بعد أن يكمل Broadbean عملية نشر الوظيفة بنجاح، يعرض القسم **عمليات النشر** للوظيفة في Attract حالة Broadbean **منشور**.</span><span class="sxs-lookup"><span data-stu-id="312f5-135">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="312f5-136">يحتاج Broadbean إلى حقل **المجال**.</span><span class="sxs-lookup"><span data-stu-id="312f5-136">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="312f5-137">تم تعيين هذا الحقل إلى **تكنولوجيا المعلومات**، بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="312f5-137">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="312f5-138">ومع ذلك، يمكنك تغيير القيمة إلى المجال الصحيح في نافذة نشر الوظائف في Broadbean.</span><span class="sxs-lookup"><span data-stu-id="312f5-138">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="312f5-139">يحتاج Broadbean إلى بعض الوقت لإتمام نشر وظيفتك في جميع لوحات الوظائف التي حددتها.</span><span class="sxs-lookup"><span data-stu-id="312f5-139">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="312f5-140">ولذلك، قد يحدث بعض التأخير قبل أن يتمكن Attract من توفير تحديث الحالة للوظيفة.</span><span class="sxs-lookup"><span data-stu-id="312f5-140">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="312f5-141">عرض منشور وظيفة في Broadbean</span><span class="sxs-lookup"><span data-stu-id="312f5-141">View a Broadbean job posting</span></span>

<span data-ttu-id="312f5-142">بعد نشر وظيفة في Broadbean، يمكنك عرضها من Attract.</span><span class="sxs-lookup"><span data-stu-id="312f5-142">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="312f5-143">في Attract، افتح الوظيفة التي تريد عرضها في Broadbean.</span><span class="sxs-lookup"><span data-stu-id="312f5-143">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="312f5-144">في قسم **عمليات النشر** ، حدد زر علامة القطع (**...**) الذي يتطابق مع Broadbean، ثم حدد **عرض**.</span><span class="sxs-lookup"><span data-stu-id="312f5-144">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="312f5-145">يظهر منشور الوظيفة في Broadbean في نافذة جديدة.</span><span class="sxs-lookup"><span data-stu-id="312f5-145">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="312f5-146">تحديث منشور وظيفة في Broadbean</span><span class="sxs-lookup"><span data-stu-id="312f5-146">Update a Broadbean job posting</span></span>

<span data-ttu-id="312f5-147">يمكنك تحديث منشور وظيفة في Broadbean باستخدام طريقتين.</span><span class="sxs-lookup"><span data-stu-id="312f5-147">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="312f5-148">في Attract، افتح الوظيفة التي تريد تحديثها.</span><span class="sxs-lookup"><span data-stu-id="312f5-148">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="312f5-149">في قسم **عمليات النشر**، حدد الزر **تحديث المنشور** الذي يتوافق مع Broadbean.</span><span class="sxs-lookup"><span data-stu-id="312f5-149">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="312f5-150">حرر المنشور في نافذة Broadbean.</span><span class="sxs-lookup"><span data-stu-id="312f5-150">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="312f5-151">–أو –</span><span class="sxs-lookup"><span data-stu-id="312f5-151">–or–</span></span>

1. <span data-ttu-id="312f5-152">في Attract، افتح الوظيفة التي تريد عرضها في Broadbean.</span><span class="sxs-lookup"><span data-stu-id="312f5-152">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="312f5-153">في قسم **عمليات النشر** ، حدد زر علامة القطع (**...**) الذي يتطابق مع Broadbean، ثم حدد **عرض**.</span><span class="sxs-lookup"><span data-stu-id="312f5-153">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="312f5-154">في نافذة Broadbean، حرر تفاصيل الوظيفة، ثم انشر الوظيفة من جديد.</span><span class="sxs-lookup"><span data-stu-id="312f5-154">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="312f5-155">لا يطرأ أي تغيير على تفاصيل الوظيفة في Attract.</span><span class="sxs-lookup"><span data-stu-id="312f5-155">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="312f5-156">إزالة منشور وظيفة في Broadbean</span><span class="sxs-lookup"><span data-stu-id="312f5-156">Remove a Broadbean job posting</span></span>

<span data-ttu-id="312f5-157">يمكنك إزالة منشور وظيفة من Broadbean كما تقتضي الحاجة.</span><span class="sxs-lookup"><span data-stu-id="312f5-157">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="312f5-158">في Attract، افتح الوظيفة التي تريد إزالتها.</span><span class="sxs-lookup"><span data-stu-id="312f5-158">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="312f5-159">في قسم **عمليات النشر** ، حدد زر علامة القطع (**...**) الذي يتطابق مع Broadbean، ثم حدد **إزالة المنشور**.</span><span class="sxs-lookup"><span data-stu-id="312f5-159">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="312f5-160">بعد قيام Broadbean بإزالة الوظيفة، يتضمن عنصر Broadbean في Attract الزر **نشر الآن**.</span><span class="sxs-lookup"><span data-stu-id="312f5-160">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="312f5-161">يشير وجود هذا الزر إلى أن إزالة الوظيفة وإلى إمكانية نشرها من جديد.</span><span class="sxs-lookup"><span data-stu-id="312f5-161">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="312f5-162">استكشاف أخطاء تكامل Broadbean وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="312f5-162">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="312f5-163">إذا كنت تواجه مشكلة ما في نشر وظيفة في Broadbean، فجرّب الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="312f5-163">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="312f5-164">تأكد من أن بيانات اعتماد Broadbean التي أدخلتها في Attract صالحة وصحيحة.</span><span class="sxs-lookup"><span data-stu-id="312f5-164">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="312f5-165">إذا كانت بيانات الاعتماد صالحة وصحيحة، فاتصل بقسم [دعم Broadbean](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="312f5-165">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="312f5-166">إذا استمرت المشكلة، فاتصل بقسم [دعم Microsoft](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="312f5-166">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
