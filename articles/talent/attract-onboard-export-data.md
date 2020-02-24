---
title: تصدير البيانات من Attract وOnboard
description: تصدير البيانات من Dynamics 365 Talent - Attract وOnboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
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
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: acdd93637385246f9c5c652cccdf2cbfb263cc33
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/23/2020
ms.locfileid: "2975924"
---
# <a name="export-data-from-attract-and-onboard"></a><span data-ttu-id="feae9-103">تصدير البيانات من Attract وOnboard</span><span class="sxs-lookup"><span data-stu-id="feae9-103">Export data from Attract and Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="feae9-104">كما تم الإعلان عنه في [إيقاف العمل بتطبيقات Dynamics 365 Talent: Attract وDynamics 365 Talent: Onboard](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)، نحن بصدد إيقاف العمل بتطبيق Dynamics 365 Talent: Attract وDynamics 365 Talent: Onboard في 1 فبراير 2022.</span><span class="sxs-lookup"><span data-stu-id="feae9-104">As announced in [Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), we're retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard on February 1, 2022.</span></span> <span data-ttu-id="feae9-105">للمساعدة في عملية الترحيل إلى منتج آخر، يوفر التطبيقان الآن قدرات تصدير البيانات.</span><span class="sxs-lookup"><span data-stu-id="feae9-105">To help with your migration to another product, both apps now provide data export capabilities.</span></span>

## <a name="export-data-from-attract"></a><span data-ttu-id="feae9-106">تصدير البيانات من Attract</span><span class="sxs-lookup"><span data-stu-id="feae9-106">Export data from Attract</span></span>

<span data-ttu-id="feae9-107">يمكنك تصدير بياناتك من دون تقييد الوصول إلى بيئتك.</span><span class="sxs-lookup"><span data-stu-id="feae9-107">You can export your data without restricting access to your environment.</span></span> <span data-ttu-id="feae9-108">قد ترغب في القيام بذلك لأغراض الاختبار أو لفهم بنية بياناتك.</span><span class="sxs-lookup"><span data-stu-id="feae9-108">You might want to do this for testing purposes or to understand our data structure.</span></span> <span data-ttu-id="feae9-109">عندما تصبح جاهزًا للترحيل، قيّد الوصول إلى بيئة Attract باستخدام الإرشادات بعد هذا الاجراء.</span><span class="sxs-lookup"><span data-stu-id="feae9-109">When you're ready to migrate, restrict access to your Attract environment using the instructions after this procedure.</span></span> <span data-ttu-id="feae9-110">تأكد من تصدير بياناتك مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="feae9-110">Be sure to export your data again.</span></span> 

1. <span data-ttu-id="feae9-111">الانتقال إلى [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="feae9-111">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="feae9-112">ضمن **تصدير البيانات**، حدد **طلب تصدير البيانات**.</span><span class="sxs-lookup"><span data-stu-id="feae9-112">Under **Data export**, select **Request a data export**.</span></span>

   ![[<span data-ttu-id="feae9-113">طلب تصدير بيانات من Attract‎</span><span class="sxs-lookup"><span data-stu-id="feae9-113">Request a data export from Attract</span></span>](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. <span data-ttu-id="feae9-114">عند ظهور مربع الرسالة **طلبك قيد المراجعة**، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="feae9-114">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="feae9-115">بإمكان عملية تصدير البيانات أن تستغرق 20 دقيقة 20 استنادًا إلى حجم التصدير.</span><span class="sxs-lookup"><span data-stu-id="feae9-115">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="feae9-116">عند اكتمال التصدير، حدد الزر **تنزيل** بجواره.</span><span class="sxs-lookup"><span data-stu-id="feae9-116">When your export completes, select the **Download** button next to it.</span></span> 

   >[!NOTE]
   ><span data-ttu-id="feae9-117">تتوفر كافة عمليات تصدير البيانات لسبعه أيام تنتهي عندها صلاحية ارتباط **التنزيل**.</span><span class="sxs-lookup"><span data-stu-id="feae9-117">All data exports are available for seven days, at which point the **Download** link expires.</span></span></br>
   
<span data-ttu-id="feae9-118">يحتوي ارتباط التنزيل على ملف zip. مع بيانات Attract، بما في ذلك المجلدات التالية:</span><span class="sxs-lookup"><span data-stu-id="feae9-118">The download contains a .zip file with your Attract data, including the following folders:</span></span>

| <span data-ttu-id="feae9-119">اسم المجلد</span><span class="sxs-lookup"><span data-stu-id="feae9-119">Folder name</span></span> | <span data-ttu-id="feae9-120">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="feae9-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="feae9-121">إعدادات المسؤول</span><span class="sxs-lookup"><span data-stu-id="feae9-121">Admin settings</span></span> | <span data-ttu-id="feae9-122">تكوينات مركز إدارة Attract.</span><span class="sxs-lookup"><span data-stu-id="feae9-122">Attract admin center configurations.</span></span> |
| <span data-ttu-id="feae9-123">المرشحون</span><span class="sxs-lookup"><span data-stu-id="feae9-123">Candidates</span></span> | <span data-ttu-id="feae9-124">جميع المرشحين الذين تمت اضافتهم إلى المهام أو تجمعات المواهب.</span><span class="sxs-lookup"><span data-stu-id="feae9-124">All candidates that were added to jobs or talent pools.</span></span> |
| <span data-ttu-id="feae9-125">قوالب البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="feae9-125">Email templates</span></span> | <span data-ttu-id="feae9-126">جميع قوالب البريد الكتروني التي تم تكوينها للبيئة.</span><span class="sxs-lookup"><span data-stu-id="feae9-126">All email templates that were configured for the environment.</span></span> |
| <span data-ttu-id="feae9-127">قوالب حزم عروض الوظائف</span><span class="sxs-lookup"><span data-stu-id="feae9-127">Job offer package templates</span></span> | <span data-ttu-id="feae9-128">جميع قوالب حزم عروض الوظائف التي تم إنشاؤها، بالإضافة إلى التكوينات المقترنة بها.</span><span class="sxs-lookup"><span data-stu-id="feae9-128">All job offer package templates that were created, plus their associated configurations.</span></span> |
| <span data-ttu-id="feae9-129">مجموعات قواعد عروض الوظائف</span><span class="sxs-lookup"><span data-stu-id="feae9-129">Job offer rule sets</span></span> |  <span data-ttu-id="feae9-130">جميع ملفات مجموعات القواعد التي تم تحميلها لإدارة العروض.</span><span class="sxs-lookup"><span data-stu-id="feae9-130">All rule set files that were uploaded for offer management.</span></span> |
| <span data-ttu-id="feae9-131">قوالب عروض الوظائف</span><span class="sxs-lookup"><span data-stu-id="feae9-131">Job offer templates</span></span> | <span data-ttu-id="feae9-132">جميع قوالب مستندات عروض الوظائف التي تم إنشاؤها للبيئة.</span><span class="sxs-lookup"><span data-stu-id="feae9-132">All job offer document templates created for the environment.</span></span> |
| <span data-ttu-id="feae9-133">فرص التوظيف</span><span class="sxs-lookup"><span data-stu-id="feae9-133">Job openings</span></span> | <span data-ttu-id="feae9-134">جميع الوظائف التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="feae9-134">All created jobs.</span></span> <span data-ttu-id="feae9-135">لا يتم تصدير الوظائف المحذوفة.</span><span class="sxs-lookup"><span data-stu-id="feae9-135">Deleted jobs aren't exported.</span></span> <span data-ttu-id="feae9-136">تحتوي المجلدات الفرعية على طلب المرشحين، مع مجلدات فرعية لمرفقات طلبات المرشحين وحزم عروض الوظائف، حيث كان ذلك ممكنًا.</span><span class="sxs-lookup"><span data-stu-id="feae9-136">The sub-folders contain candidate applications, with sub-folders for candidate application attachments and offer packages, where applicable.</span></span> |
| <span data-ttu-id="feae9-137">قوالب فرص التوظيف</span><span class="sxs-lookup"><span data-stu-id="feae9-137">Job opening templates</span></span> | <span data-ttu-id="feae9-138">قوالب عمليات التوظيف التي تم تكوينها للبيئة.</span><span class="sxs-lookup"><span data-stu-id="feae9-138">Job process templates that were configured in the environment.</span></span> |
| <span data-ttu-id="feae9-139">مجموعات المواهب</span><span class="sxs-lookup"><span data-stu-id="feae9-139">Talent pools</span></span> | <span data-ttu-id="feae9-140">جميع مجموعات المواهب‬‬ التي تم إنشاؤها وقوائم المساهمين الخاصة بها وقوائم المرشحين لمجموعات المواهب.</span><span class="sxs-lookup"><span data-stu-id="feae9-140">All created talent pools, their contributors lists, and the candidates lists for the talent pools.</span></span> |
| <span data-ttu-id="feae9-141">العاملون</span><span class="sxs-lookup"><span data-stu-id="feae9-141">Workers</span></span> | <span data-ttu-id="feae9-142">قائمة بجميع العاملين الموجودين في البيئة، بالإضافة إلى أدوارهم.</span><span class="sxs-lookup"><span data-stu-id="feae9-142">List of all the workers who are present in the environment, plus their roles.</span></span> |
| <span data-ttu-id="feae9-143">(المجلد الجذر)</span><span class="sxs-lookup"><span data-stu-id="feae9-143">(root folder)</span></span> | <span data-ttu-id="feae9-144">ملف مخطط JSON يصف حقول بنية البيانات.</span><span class="sxs-lookup"><span data-stu-id="feae9-144">A JSON schema file that describes the data structure fields.</span></span> |

### <a name="restrict-access-to-attract"></a><span data-ttu-id="feae9-145">تقييد الوصول إلى Attract</span><span class="sxs-lookup"><span data-stu-id="feae9-145">Restrict access to Attract</span></span>

<span data-ttu-id="feae9-146">عندما تصبح جاهزًا للترحيل، قيّد وصول الأشخاص من غير المسولين إلى بيئة Attract وتصدير بياناتك.</span><span class="sxs-lookup"><span data-stu-id="feae9-146">When you're ready to migrate, restrict non-admins from accessing your Attract environment and export your data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="feae9-147">يعتبر تقييد الوصول إلى بيئة Attract دائمًا ولا يمكن التراجع عنه.</span><span class="sxs-lookup"><span data-stu-id="feae9-147">Restricting access to your Attract environment is permanent and can't be undone.</span></span> <span data-ttu-id="feae9-148">إذا أردت تمكين المستخدمين من غير المسؤولين من مواصلة الوصول إلى بيئتك، فعليك تخطي هذه الخطوة.</span><span class="sxs-lookup"><span data-stu-id="feae9-148">If you want non-admin users to continue accessing your environment, skip this step.</span></span>

1. <span data-ttu-id="feae9-149">الانتقال إلى [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="feae9-149">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="feae9-150">لمنع وصول مستخدمين من غير المسؤولين إلى بيئة Attract، حدد **تقييد الوصول الآن** ضمن **تقييد الوصول إلى هذا التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="feae9-150">To restrict non-admins from accessing your Attract environment, under **Restrict access to this app**, select **Restrict access now**.</span></span> <span data-ttu-id="feae9-151">يؤدي أيضًا تقييد الوصول إلى إلغاء نشر أي وظائف نشطة تم نشرها.</span><span class="sxs-lookup"><span data-stu-id="feae9-151">Restricting access also unposts any active jobs that have been posted.</span></span>

   ![[<span data-ttu-id="feae9-152">تقييد وصول مستخدمين من غير المسؤولين إلى Attract</span><span class="sxs-lookup"><span data-stu-id="feae9-152">Restrict non-admin access to Attract</span></span>](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. <span data-ttu-id="feae9-153">عندما يظهر التحذير **هذا تغيير دائم**، حدد **تقييد الوصول** لمنع وصول مستخدمين من غير المسؤولين إلى هذه البيئة.</span><span class="sxs-lookup"><span data-stu-id="feae9-153">When you see the warning **This is a permanent change**, select **Restrict access** to permanently restrict non-admin users from this environment.</span></span> <span data-ttu-id="feae9-154">إذا لم تكن جاهزًا لإكمال هذه الخطوة، فحدد **إلغاء**.</span><span class="sxs-lookup"><span data-stu-id="feae9-154">If you're not ready to complete this step, select **Cancel**.</span></span>

   ![[<span data-ttu-id="feae9-155">تحذير بأن تقييد الوصول هو تغيير دائم</span><span class="sxs-lookup"><span data-stu-id="feae9-155">Warning that restricting access is a permanent change</span></span>](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   ><span data-ttu-id="feae9-156">بإمكان المسؤولين متابعة الوصول إلى صفحة تصدير البيانات وتقرير الشخص بعد تقييد الوصول إلى بيئة Attract.</span><span class="sxs-lookup"><span data-stu-id="feae9-156">Admins can continue to access the data export and person report pages after you restrict access to the Attract environment.</span></span>

## <a name="export-data-from-onboard"></a><span data-ttu-id="feae9-157">تصدير البيانات من Onboard</span><span class="sxs-lookup"><span data-stu-id="feae9-157">Export data from Onboard</span></span>

<span data-ttu-id="feae9-158">عندما تصبح جاهزًا، يمكنك تحميل القوالب والأدلة وبيانات المرشحين من Onboard.</span><span class="sxs-lookup"><span data-stu-id="feae9-158">When you're ready, you can download templates, guides, and candidate data from Onboard.</span></span>

1. <span data-ttu-id="feae9-159">الانتقال إلى [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span><span class="sxs-lookup"><span data-stu-id="feae9-159">Go to [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span></span>

2. <span data-ttu-id="feae9-160">ضمن **تصدير البيانات**، حدد **طلب تصدير البيانات**.</span><span class="sxs-lookup"><span data-stu-id="feae9-160">Under **Data export**, select **Request a data export**.</span></span> 

   ![[<span data-ttu-id="feae9-161">طلب تصدير بيانات من Onboard‎‎</span><span class="sxs-lookup"><span data-stu-id="feae9-161">Request a data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. <span data-ttu-id="feae9-162">عند ظهور مربع الرسالة **طلبك قيد المراجعة**، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="feae9-162">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="feae9-163">بإمكان عملية تصدير البيانات أن تستغرق 20 دقيقة 20 استنادًا إلى حجم التصدير.</span><span class="sxs-lookup"><span data-stu-id="feae9-163">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="feae9-164">عند اكتمال التصدير، حدد الزر **تنزيل** بجواره.</span><span class="sxs-lookup"><span data-stu-id="feae9-164">When your export completes, select the **Download** button next to it.</span></span> 

   ![[<span data-ttu-id="feae9-165">تنزيل تصدير البيانات من Onboard</span><span class="sxs-lookup"><span data-stu-id="feae9-165">Download data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   ><span data-ttu-id="feae9-166">يتوفر تصدير البيانات لمدة سبعة أيام.</span><span class="sxs-lookup"><span data-stu-id="feae9-166">Your data export is available for seven days.</span></span> <span data-ttu-id="feae9-167">بعد سبعة أيام، تنتهي صلاحية ارتباط **التنزيل**، ويجب أن تطلب عملية تصدير جديدة إذا احتجت إلى تنزيل بياناتك من جديد.</span><span class="sxs-lookup"><span data-stu-id="feae9-167">After seven days, the **Download** link expires, and you must request a new export if you need to download your data again.</span></span> <span data-ttu-id="feae9-168">عندما تبدأ عملية تصدير جديدة للبيانات، ستنتهي صلاحية التنزيلات الموجودة بعد نجاح عملية التصدير الجديدة.</span><span class="sxs-lookup"><span data-stu-id="feae9-168">When you start a new data export, any existing downloads will expire after the new export succeeds.</span></span>

<span data-ttu-id="feae9-169">ملف التنزيل عبارة عن ملف zip. يحتوي علي:</span><span class="sxs-lookup"><span data-stu-id="feae9-169">The download is a .zip file that contains:</span></span>

- <span data-ttu-id="feae9-170">مجلد **قوالب** يحتوي على قوالب Onboard بتنسيق مستند Word.</span><span class="sxs-lookup"><span data-stu-id="feae9-170">A **Templates** folder that contains your Onboard templates in Word document format.</span></span>

- <span data-ttu-id="feae9-171">مجلد **أدلة** الذي يحتوي على أدلة Onboard بتنسيق مستند Word.</span><span class="sxs-lookup"><span data-stu-id="feae9-171">A **Guides** folder that contains your Onboard guides in Word document format.</span></span>

## <a name="see-also"></a><span data-ttu-id="feae9-172">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="feae9-172">See also</span></span>

[<span data-ttu-id="feae9-173">إيقاف العمل بتطبيقات Dynamics 365 Talent: Attract وDynamics 365 Talent: Onboard</span><span class="sxs-lookup"><span data-stu-id="feae9-173">Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)