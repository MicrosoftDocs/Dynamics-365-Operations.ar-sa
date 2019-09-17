---
title: توسيع قدرات Talent باستخدام PowerApps وMicrosoft Flow - سيناريوهات أمثلة
description: يصف هذا الموضوع بعض الأمثلة عن سيناريوهات قابلية التوسعة في Microsoft Dynamics 365 for Talent التي تستخدم Microsoft PowerApps وMicrosoft Flow.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 0b455a8194f58b41a349f004ceda8183c7ee3f7c
ms.sourcegitcommit: 9f94eff93d29bc27352569824e00bbccc2f961b8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/22/2019
ms.locfileid: "1781432"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="30d20-103">توسيع قدرات Talent باستخدام PowerApps وMicrosoft Flow - سيناريوهات أمثلة</span><span class="sxs-lookup"><span data-stu-id="30d20-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="30d20-104">يصف هذا الموضوع بعض الأمثلة عن سيناريوهات قابلية التوسعة في Microsoft Dynamics 365 for Talent التي تستخدم Microsoft PowerApps وMicrosoft Flow.</span><span class="sxs-lookup"><span data-stu-id="30d20-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="30d20-105">يمكنك استيراد حزمة الحل المقترنة بكل مثال إلى بيئتك في PowerApps.</span><span class="sxs-lookup"><span data-stu-id="30d20-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="30d20-106">بعد ذلك، يمكنك استخدام الحزم كنقاط إرشادية أو كنقاط بداية لتنفيذ السيناريوهات التي تنطبق على مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="30d20-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="30d20-107">إذا أردت استخدام القوالب والتطبيقات التي تم وصفها في الموضوع "كما هي"، فتأكد من اختبارها للتأكد من أنها تغطي كافة السيناريوهات المتعلقة بعملية التنفيذ التي تقوم بها.</span><span class="sxs-lookup"><span data-stu-id="30d20-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="30d20-108">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="30d20-108">Prerequisites</span></span>

- <span data-ttu-id="30d20-109">لاستيراد الحزم، يجب أن يتوفر إذن **أداة إنشاء البيئة** لدى المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="30d20-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="30d20-110">لتصدير التطبيقات أو استيرادها، يجب أن يتوفر لدى المستخدمين ترخيص PowerApps Plan 2 أو ترخيص إصدار تجريبي PowerApps Plan 2.</span><span class="sxs-lookup"><span data-stu-id="30d20-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="30d20-111">القالب "Flow – توصيل النماذج"</span><span class="sxs-lookup"><span data-stu-id="30d20-111">Flow – Form Connect</span></span>

<span data-ttu-id="30d20-112">يمكن استخدام القالب **Flow – توصيل النماذج** لقراءة البيانات من Microsoft Forms وتخزينها في كيان Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="30d20-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="30d20-113">ويمكن توسيع هذا القالب لتمكين سيناريوهات أخرى من استخدامه.</span><span class="sxs-lookup"><span data-stu-id="30d20-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="30d20-114">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="30d20-114">Here are some examples:</span></span>

- <span data-ttu-id="30d20-115">التقاط تقييمات المرشح.</span><span class="sxs-lookup"><span data-stu-id="30d20-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="30d20-116">التقاط النتائج من استبيانات الدورة التدريبية.</span><span class="sxs-lookup"><span data-stu-id="30d20-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="30d20-117">تجميع مكتبة تتضمن أسئلة المقابلات لمسؤولي الموارد البشرية (HR).</span><span class="sxs-lookup"><span data-stu-id="30d20-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="30d20-118">التقاط تقييم المرشح أثناء عملية المقابلة</span><span class="sxs-lookup"><span data-stu-id="30d20-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="30d20-119">في Microsoft Dynamics 365: Attract، بإمكان النماذج أن تظهر في مدخل المرشحين، وبإمكان المرشحين ملء التفاصيل فيها.</span><span class="sxs-lookup"><span data-stu-id="30d20-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="30d20-120">ويمكن أيضًا تضمين النماذج كأنشطة في قالب وظيفة.</span><span class="sxs-lookup"><span data-stu-id="30d20-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="30d20-121">عندما يرسل المرشح نموذجًا، يلتقط Microsoft Flow عملية إرسال النموذج ويقرأ البيانات ويخزنها في كيان Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="30d20-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="30d20-122">لتنزيل القالب **Flow – توصيل النماذج** وبنية الكيان المخصص، انتقل إلى [Flow – توصيل النماذج](https://go.microsoft.com/fwlink/?linkid=2081988) في مركز التنزيل لـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="30d20-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="30d20-123">القالب "تهيئة واستخراج المعلمات التي تم تمريرها إلى Powerapps"</span><span class="sxs-lookup"><span data-stu-id="30d20-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="30d20-124">يمكن استخدام القالب **تهيئة واستخراج المعلمات التي تم تمريرها إلى Powerapps** كنقطة بداية لأي سيناريو PowerApps يتعلق بتطبيق Attract.</span><span class="sxs-lookup"><span data-stu-id="30d20-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="30d20-125">ويتضمن هذا القالب جميع المعلمات الافتراضية التي تم تمريرها بواسطة Attract، مثل **استمارة التقديم للوظيفة** و**معرف المرشح** و**معرف الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="30d20-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="30d20-126">يمكن استخدام هذا القالب للعثور على نموذج تقييم المرشح لتمكين مدير التوظيف من عرض التقييم الذي قام المرشح بتعبئته.</span><span class="sxs-lookup"><span data-stu-id="30d20-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="30d20-127">يمكن تضمين التطبيقات التي يتم إنشاؤها باستخدام PowerApps في قالب الوظيفة في Attract.</span><span class="sxs-lookup"><span data-stu-id="30d20-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="30d20-128">لتنزيل القالب **تهيئة واستخراج المعلمات التي تم تمريرها إلى Powerapps** وبنية الكيان المخصص، انتقل إلى [تهيئة واستخراج المعلمات التي تم تمريرها إلى Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) في مركز التنزيل لـ Microsoft.‬</span><span class="sxs-lookup"><span data-stu-id="30d20-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="30d20-129">التكامل مع Office 365</span><span class="sxs-lookup"><span data-stu-id="30d20-129">Integration with Office 365</span></span>

<span data-ttu-id="30d20-130">يمكن استخدام تطبيق **التكامل مع Office 365** لاستخراج معلومات الفريق للمستخدمين الذين سجلوا دخولهم من Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="30d20-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="30d20-131">وهو يشير إلى العاملين في Talent لاستخراج تسجيلات تفاصيل بدء العمل وانتهاء العمل والاستثناءات.</span><span class="sxs-lookup"><span data-stu-id="30d20-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="30d20-132">يتم تخزين تفاصيل بدء العمل وانتهاء العمل في كيانات مخصصة في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="30d20-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="30d20-133">ويتم الافتراض أن تعبئة هذه التفاصيل يتم من أنظمة خارجية عن طريق التكامل.</span><span class="sxs-lookup"><span data-stu-id="30d20-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="30d20-134">يمكن توسيع هذا التطبيق لتمكين سيناريوهات أخرى من استخدامه.</span><span class="sxs-lookup"><span data-stu-id="30d20-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="30d20-135">على سبيل المثال، يمكن استخدامه لإظهار معلومات العطلة الخاصة بالفريق بالإضافة إلى أحداث التقويم وأي أحداث خاصة بالفريق.</span><span class="sxs-lookup"><span data-stu-id="30d20-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="30d20-136">لتنزيل تطبيق **التكامل مع Office 365** وبنية الكيان المخصص، انتقل إلى [التكامل مع Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) في مركز التنزيل لـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="30d20-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="30d20-137">القالب "Flow – إعلام بواسطة البريد الإلكتروني"</span><span class="sxs-lookup"><span data-stu-id="30d20-137">Flow – Email Notification</span></span>

<span data-ttu-id="30d20-138">يمكن استخدام القالب **Flow – إعلام بواسطة البريد الإلكتروني** لسيناريوهات الإعلام بواسطة البريد الإلكتروني.</span><span class="sxs-lookup"><span data-stu-id="30d20-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="30d20-139">ويمكن استخدامه لتشغيل الإعلامات بواسطة البريد الإلكتروني الموجهة للمرشحين الذين رفضهم فريق التوظيف أثناء أي مرحلة من مراحل التعيين.</span><span class="sxs-lookup"><span data-stu-id="30d20-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="30d20-140">يمكن توسيع هذا القالب لتعقب التغييرات في مرحلة المرشح عبر عملية التعيين، ولإرسال إعلامات إلى فريق التوظيف والمرشح.</span><span class="sxs-lookup"><span data-stu-id="30d20-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="30d20-141">بشكل عام، بالنسبة إلى الكيانات المخزنة في Common Data Service، يمكن إعداد مهام سير العمل لإرسال إعلامات تتعلق بالأحداث التي تقع في Core HR أو Attract أو Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="30d20-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="30d20-142">لتنزيل القالب **Flow – إعلام بواسطة البريد الإلكتروني**، انتقل إلى [Flow – إعلام بواسطة البريد الإلكتروني](https://go.microsoft.com/fwlink/?linkid=2082103) في مركز التنزيل لـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="30d20-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="30d20-143">القالب "Flow – توصيل وتنفيذ SQL"</span><span class="sxs-lookup"><span data-stu-id="30d20-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="30d20-144">يقوم القالب **Flow – توصيل وتنفيذ SQL‬** بالتوصيل بخادم Microsoft SQL Server ويسمح بتشغيل استعلامات SQL.</span><span class="sxs-lookup"><span data-stu-id="30d20-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="30d20-145">على الرغم من تصميم هذا القالب لقراءة وتحديث جداول SQL، إلا أنه من الممكن توسيعه لتمكين استخدامه لسيناريوهات أخرى.</span><span class="sxs-lookup"><span data-stu-id="30d20-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="30d20-146">على سبيل المثال، يمكن استخدامه لتعبئة جدول مرحلي في Common Data Service بواسطة سجلات من SQL Server، ولمزامنة الجدول المرحلي بشكل دوري باستخدام توزيع تزايدي من SQL Server.</span><span class="sxs-lookup"><span data-stu-id="30d20-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="30d20-147">لتنزيل القالب **Flow – توصيل وتنفيذ SQL**، انتقل إلى [Flow – توصيل وتنفيذ SQL](https://go.microsoft.com/fwlink/?linkid=2081789) في مركز التنزيل لـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="30d20-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="30d20-148">القالب "Flow – تكامل SharePoint"</span><span class="sxs-lookup"><span data-stu-id="30d20-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="30d20-149">يمكن استخدام القالب **Flow – تكامل SharePoint** لقراءة البيانات من قائمة Microsoft SharePoint ومقارنة القائمة مع قيم الحقول لأي من كيانات Common Data Service وإرسال نتائج المقارنة كبريد إلكتروني للإعلام.</span><span class="sxs-lookup"><span data-stu-id="30d20-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="30d20-150">قد تتوفر لدى مؤسسة مجموعة من المهارات تحتاج إليها بطريقة ملحة.</span><span class="sxs-lookup"><span data-stu-id="30d20-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="30d20-151">يمكن تخزين هذه المهارات في SharePoint كقائمة SharePoint.</span><span class="sxs-lookup"><span data-stu-id="30d20-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="30d20-152">عندما يقدم أحد المرشحين طلب الحصول على أي وظيفة تم إدراج مجموعة المهارات المطلوبة لها، يتم إرسال بريد إلكتروني للإعلام عند وجود تطابق ملحوظ بين مهارات المرشح والمهارات المخزنة في SharePoint.</span><span class="sxs-lookup"><span data-stu-id="30d20-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="30d20-153">وبهذه الطريقة، يتم ملء المناصب المطلوبة بشكل ملح بسرعة أكبر، لأن الإعلامات تساعد مسؤولي التعيين على الوصول إلى المرشحين عبر المؤسسة وتوظيفهم.</span><span class="sxs-lookup"><span data-stu-id="30d20-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="30d20-154">يمكن توسيع هذا القالب لتمكين استخدامه لأي سيناريو يشتمل على تكامل SharePoint.</span><span class="sxs-lookup"><span data-stu-id="30d20-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="30d20-155">لتنزيل القالب **Flow – تكامل SharePoint**، انتقل إلى [Flow – تكامل SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) في مركز التنزيل لـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="30d20-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="30d20-156">تطبيق Referral</span><span class="sxs-lookup"><span data-stu-id="30d20-156">Referral App</span></span>
<span data-ttu-id="30d20-157">يمكنك استخدام التطبيق Referral لإضافة مرشحين إلى مجموعة مواهب مشتركة.</span><span class="sxs-lookup"><span data-stu-id="30d20-157">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="30d20-158">بإمكان المحيل إدخال **الاسم الأول** و**اسم العائلة** و**البريد الإلكتروني** و**Linkedln URL** عند إرسال مرشح.</span><span class="sxs-lookup"><span data-stu-id="30d20-158">The referrer can enter **Firstname**, **Lastname**, **Email**, and **Linkedln URL** when submitting a candidate.</span></span> <span data-ttu-id="30d20-159">يتم بعد ذلك ملء بيانات تعريف مصدر المرشح بواسطة معلومات المحيل.</span><span class="sxs-lookup"><span data-stu-id="30d20-159">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="30d20-160">يمكنك تضمين هذا التطبيق في الخدمة الذاتية للموظف (ESS) لإرسال الإحالات، أو يمكنك استخدامه كارتباط تشعبي في مدخل الشركة وتشغيله كتطبيق مستقل.</span><span class="sxs-lookup"><span data-stu-id="30d20-160">You can embed this app in Employee self-service (ESS) for submitting referrals, or you can be use it as a hyperlink in the Corporate Portal and run as a stand-alone app.</span></span>

<span data-ttu-id="30d20-161">لتنزيل **تطبيق Referral**، انتقل إلى [حل قابلية التوسعة في Dynamics 365 for Talent: تطبيق Referral](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) في مركز التنزيل لـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="30d20-161">To download **Referral App**, go to [Dynamics 365 for Talent extensibility solution: Referral App](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) on the Microsoft Download Center.</span></span> <span data-ttu-id="30d20-162">يمكنك استيراد هذا التطبيق وتخصيصه لإضافة المزيد من الوظائف.</span><span class="sxs-lookup"><span data-stu-id="30d20-162">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30d20-163">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="30d20-163">Additional resources</span></span>

[<span data-ttu-id="30d20-164">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="30d20-164">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="30d20-165">ترحيل التطبيق بين المستأجرين والبيئات</span><span class="sxs-lookup"><span data-stu-id="30d20-165">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
