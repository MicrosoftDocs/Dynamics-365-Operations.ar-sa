---
title: نشر الوظائف في مواقع وظائف خارجية من Attract
description: يشرح هذا الموضوع كيفية استخدام Dynamics 365 for Talent - Attract لنشر الوظائف في مواقع توظيف خارجية.
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
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
ms.openlocfilehash: 9c27d1810a89ed7d7a7745e41c5f118dbdfe5dda
ms.sourcegitcommit: cadce85ca3004d53caf6bc49147a524c1bfd421f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/16/2019
ms.locfileid: "1590472"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="6e0e2-103">نشر الوظائف في مواقع وظائف خارجية من Attract</span><span class="sxs-lookup"><span data-stu-id="6e0e2-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e0e2-104">تريد عرض المناصب المفتوحة أمام عدد أكبر عدد ممكن من المرشحين المؤهلين.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="6e0e2-105">تساعدك مواقع التوظيف مثل Broadbean في تحقيق هذا الهدف.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="6e0e2-106">يسمح لك الآن Microsoft Dynamics 365 Talent: Attract بنشر الوظائف في Broadbean، وتعمل Microsoft بشكل مستمر على تقديم عروض جديدة في هذا المجال.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="6e0e2-107">نشر وظائف في Broadbean</span><span class="sxs-lookup"><span data-stu-id="6e0e2-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="6e0e2-108">قبل أن تتمكن من نشر الوظائف في Broadbean، يجب عليك تكوين تكامل Broadbean.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="6e0e2-109">لنشر الوظائف في مواقع خارجية، يجب استخدام [المكون الإضافي "التوظيف الشامل"](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="6e0e2-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="6e0e2-110">لترحيل الوظائف إلى Broadbean من خلال Attract، يجب أن يكون لديك اشتراك Broadbean.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-110">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="6e0e2-111">هذه الميزة قيد المعاينة حاليًا.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-111">This feature is currently in preview.</span></span> <span data-ttu-id="6e0e2-112">إذا أردت تجربتها، فيجب [تشغيلها في إعدادات إدارة Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="6e0e2-112">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="6e0e2-113">تكوين تكامل Broadbean</span><span class="sxs-lookup"><span data-stu-id="6e0e2-113">Configure Broadbean integration</span></span>

1. <span data-ttu-id="6e0e2-114">سجل دخولك إلى Attract كمسؤول.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-114">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="6e0e2-115">حدد زر **الإعدادات** (رمز الترس) في الزاوية العلوية اليسرى من الصفحة، ثم حدد **مركز الإدارة**.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-115">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="6e0e2-116">على علامة التبويب **إعدادات لوحة الوظائف**، في القسم **تمكين تكامل Broadbean**، قم بتشغيل التكامل.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-116">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="6e0e2-117">اتصل بموقع Broadbean، وأدخل معلوماتك في **Username, Client ID, Encryption Token**.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-117">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="6e0e2-118">تعتبر بيانات اعتمادك في Broadbean سرية وحساسة لحالة الأحرف.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-118">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="6e0e2-119">وبالتالي، يجب تخزينها ومشاركتها بطريقة مسؤولة.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-119">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="6e0e2-120">بإمكان أي شخص يؤدي دور المسؤول في Attract عرض بيانات الاعتماد هذه.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-120">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="6e0e2-121">لا تشارك Microsoft كما لا يشارك Attract في إنشاء هذه القيم والمحافظة عليها.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-121">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="6e0e2-122">تقع على عاتقك مسؤولية تحديثها بشكل مستمر في Attract والعمل مع Broadbean على حل أي مشكلة تتعلق ببيانات اعتمادك.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-122">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="6e0e2-123">نشر وظيفة في Broadbean</span><span class="sxs-lookup"><span data-stu-id="6e0e2-123">Post a job to Broadbean</span></span>

<span data-ttu-id="6e0e2-124">بعد تشغيل Broadbean، بإمكان المسؤولين ومسؤولي التعيين نشر وظائف فيه.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-124">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="6e0e2-125">يجب أن يتوفر لديك عنوان URL لتقديم الطلب للوظيفة.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-125">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="6e0e2-126">في Attract، افتح الوظيفة التي تريد نشرها في Broadbean.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-126">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="6e0e2-127">في قسم **عمليات النشر**، حدد الزر **نشر الآن** الذي يتوافق مع Broadbean.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-127">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="6e0e2-128">اتبع الإرشادات في نافذة Broadbean.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-128">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="6e0e2-129">يقوم Attract بتمرير المعلومات التالية إلى Broadbean:</span><span class="sxs-lookup"><span data-stu-id="6e0e2-129">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="6e0e2-130">معرف الطلب</span><span class="sxs-lookup"><span data-stu-id="6e0e2-130">Request ID</span></span>
- <span data-ttu-id="6e0e2-131">المسمى الوظيفي</span><span class="sxs-lookup"><span data-stu-id="6e0e2-131">Job title</span></span>
- <span data-ttu-id="6e0e2-132">وصف الوظيفة</span><span class="sxs-lookup"><span data-stu-id="6e0e2-132">Job description</span></span>
- <span data-ttu-id="6e0e2-133">موقع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="6e0e2-133">Job location</span></span>
- <span data-ttu-id="6e0e2-134">عنوان URL لتقديم الطلب</span><span class="sxs-lookup"><span data-stu-id="6e0e2-134">Apply URL</span></span>
- <span data-ttu-id="6e0e2-135">معلومات مسؤول التعيين</span><span class="sxs-lookup"><span data-stu-id="6e0e2-135">Recruiter information</span></span>

<span data-ttu-id="6e0e2-136">بعد أن يكمل Broadbean عملية نشر الوظيفة بنجاح، يعرض القسم **عمليات النشر** للوظيفة في Attract حالة Broadbean **منشور**.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-136">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="6e0e2-137">يحتاج Broadbean إلى حقل **المجال**.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-137">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="6e0e2-138">تم تعيين هذا الحقل إلى **تكنولوجيا المعلومات**، بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-138">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="6e0e2-139">ومع ذلك، يمكنك تغيير القيمة إلى المجال الصحيح في نافذة نشر الوظائف في Broadbean.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-139">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="6e0e2-140">يحتاج Broadbean إلى بعض الوقت لإتمام نشر وظيفتك في جميع لوحات الوظائف التي حددتها.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-140">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="6e0e2-141">ولذلك، قد يحدث بعض التأخير قبل أن يتمكن Attract من توفير تحديث الحالة للوظيفة.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-141">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="6e0e2-142">عرض منشور وظيفة في Broadbean</span><span class="sxs-lookup"><span data-stu-id="6e0e2-142">View a Broadbean job posting</span></span>

<span data-ttu-id="6e0e2-143">بعد نشر وظيفة في Broadbean، يمكنك عرضها من Attract.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-143">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="6e0e2-144">في Attract، افتح الوظيفة التي تريد عرضها في Broadbean.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-144">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="6e0e2-145">في قسم **عمليات النشر** ، حدد زر علامة القطع (**...**) الذي يتطابق مع Broadbean، ثم حدد **عرض**.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-145">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="6e0e2-146">يظهر منشور الوظيفة في Broadbean في نافذة جديدة.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-146">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="6e0e2-147">تحديث منشور وظيفة في Broadbean</span><span class="sxs-lookup"><span data-stu-id="6e0e2-147">Update a Broadbean job posting</span></span>

<span data-ttu-id="6e0e2-148">يمكنك تحديث منشور وظيفة في Broadbean باستخدام طريقتين.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-148">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="6e0e2-149">في Attract، افتح الوظيفة التي تريد تحديثها.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-149">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="6e0e2-150">في قسم **عمليات النشر**، حدد الزر **تحديث المنشور** الذي يتوافق مع Broadbean.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-150">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="6e0e2-151">حرر المنشور في نافذة Broadbean.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-151">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="6e0e2-152">–أو –</span><span class="sxs-lookup"><span data-stu-id="6e0e2-152">–or–</span></span>

1. <span data-ttu-id="6e0e2-153">في Attract، افتح الوظيفة التي تريد عرضها في Broadbean.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-153">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="6e0e2-154">في قسم **عمليات النشر** ، حدد زر علامة القطع (**...**) الذي يتطابق مع Broadbean، ثم حدد **عرض**.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-154">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="6e0e2-155">في نافذة Broadbean، حرر تفاصيل الوظيفة، ثم انشر الوظيفة من جديد.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-155">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="6e0e2-156">لا يطرأ أي تغيير على تفاصيل الوظيفة في Attract.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-156">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="6e0e2-157">إزالة منشور وظيفة في Broadbean</span><span class="sxs-lookup"><span data-stu-id="6e0e2-157">Remove a Broadbean job posting</span></span>

<span data-ttu-id="6e0e2-158">يمكنك إزالة منشور وظيفة من Broadbean كما تقتضي الحاجة.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-158">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="6e0e2-159">في Attract، افتح الوظيفة التي تريد إزالتها.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-159">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="6e0e2-160">في قسم **عمليات النشر** ، حدد زر علامة القطع (**...**) الذي يتطابق مع Broadbean، ثم حدد **إزالة المنشور**.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-160">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="6e0e2-161">بعد قيام Broadbean بإزالة الوظيفة، يتضمن عنصر Broadbean في Attract الزر **نشر الآن**.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-161">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="6e0e2-162">يشير وجود هذا الزر إلى أن إزالة الوظيفة وإلى إمكانية نشرها من جديد.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-162">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="6e0e2-163">استكشاف أخطاء تكامل Broadbean وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="6e0e2-163">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="6e0e2-164">إذا كنت تواجه مشكلة ما في نشر وظيفة في Broadbean، فجرّب الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-164">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="6e0e2-165">تأكد من أن بيانات اعتماد Broadbean التي أدخلتها في Attract صالحة وصحيحة.</span><span class="sxs-lookup"><span data-stu-id="6e0e2-165">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="6e0e2-166">إذا كانت بيانات الاعتماد صالحة وصحيحة، فاتصل بقسم [دعم Broadbean](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="6e0e2-166">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="6e0e2-167">إذا استمرت المشكلة، فاتصل بقسم [دعم Microsoft](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="6e0e2-167">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
