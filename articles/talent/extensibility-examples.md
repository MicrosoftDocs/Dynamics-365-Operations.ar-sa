---
title: توسيع Talent باستخدام Power Apps وPower Automate
description: يوضح هذا المقال بعض الأمثلة عن سيناريوهات قابلية توسعة Microsoft Dynamics 365 Talent - Attract التي تستخدم Microsoft Power Apps وPower Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529624"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="d1ce1-103">توسيع Talent باستخدام Power Apps وPower Automate</span><span class="sxs-lookup"><span data-stu-id="d1ce1-103">Extend Talent with Power Apps and Power Automate</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d1ce1-104">يوضح هذا المقال بعض الأمثلة عن سيناريوهات قابلية توسعة Microsoft Dynamics 365 Talent: Attract التي تستخدم Microsoft Power Apps وMicrosoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent: Attract that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="d1ce1-105">يمكنك استيراد حزمة الحل المقترنة بكل مثال إلى بيئتك في Power Apps.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="d1ce1-106">بعد ذلك، يمكنك استخدام الحزم كنقاط إرشادية أو كنقاط بداية لتنفيذ السيناريوهات التي تنطبق على مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1ce1-107">إذا أردت استخدام القوالب والتطبيقات التي تم وصفها في هذا المقال "كما هي"، فتأكد من اختبارها للتأكد من أنها تغطي كافة السيناريوهات المتعلقة بعملية التنفيذ التي تقوم بها.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-107">If you want to use the templates and app that are described in this article "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="d1ce1-108">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="d1ce1-108">Prerequisites</span></span>

- <span data-ttu-id="d1ce1-109">لاستيراد الحزم، يجب أن يتوفر إذن **أداة إنشاء البيئة** لدى المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="d1ce1-110">لتصدير التطبيقات أو استيرادها، يجب أن يتوفر لدى المستخدمين ترخيص Power Apps Plan 2 أو ترخيص إصدار تجريبي Power Apps Plan 2.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="d1ce1-111">Power Automate – توصيل النماذج</span><span class="sxs-lookup"><span data-stu-id="d1ce1-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="d1ce1-112">يمكن استخدام القالب **Power Automate – توصيل النماذج** لقراءة البيانات من Microsoft Forms وتخزينها في كيان Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="d1ce1-113">ويمكن توسيع هذا القالب لتمكين سيناريوهات أخرى من استخدامه.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="d1ce1-114">فيما يلي بعض الأمثلة:</span><span class="sxs-lookup"><span data-stu-id="d1ce1-114">Here are some examples:</span></span>

- <span data-ttu-id="d1ce1-115">التقاط تقييمات المرشح.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="d1ce1-116">التقاط النتائج من استبيانات الدورة التدريبية.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="d1ce1-117">تجميع مكتبة تتضمن أسئلة المقابلات لمسؤولي الموارد البشرية (HR).</span><span class="sxs-lookup"><span data-stu-id="d1ce1-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="d1ce1-118">التقاط تقييم المرشح أثناء عملية المقابلة</span><span class="sxs-lookup"><span data-stu-id="d1ce1-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="d1ce1-119">في Microsoft Dynamics 365: Attract، بإمكانك استخدام النماذج في مدخل المرشحين، التي يملأ المرشحون التفاصيل فيها.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-119">In Microsoft Dynamics 365: Attract, you can use forms in the candidate portal, where candidates fill in details.</span></span> <span data-ttu-id="d1ce1-120">ويمكنك أيضًا تضمين النماذج كأنشطة في قالب وظيفة.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-120">You can also embed forms as activities in a job template.</span></span>

<span data-ttu-id="d1ce1-121">عندما يرسل المرشح نموذجًا، يلتقط Microsoft Power Automate عملية إرسال النموذج ويقرأ البيانات ويخزنها في كيان Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="d1ce1-122">لتنزيل القالب **Power Automate – توصيل النماذج** وبنية الكيان المخصص، انتقل إلى [Power Automate – توصيل النماذج](https://go.microsoft.com/fwlink/?linkid=2081988) على مركز التنزيل لـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="d1ce1-123">تكامل Power Automate – SharePoint</span><span class="sxs-lookup"><span data-stu-id="d1ce1-123">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="d1ce1-124">يمكن استخدام القالب **تكامل Power Automate – SharePoint** لقراءة البيانات من قائمة Microsoft SharePoint ومقارنة القائمة مع قيم الحقول لأي من كيانات Common Data Service وإرسال نتائج المقارنة كبريد إلكتروني للإخطار.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-124">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="d1ce1-125">قد تتوفر لدى مؤسسة مجموعة من المهارات تحتاج إليها بطريقة ملحة.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-125">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="d1ce1-126">يمكن تخزين هذه المهارات في SharePoint كقائمة SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-126">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="d1ce1-127">عندما يقدم أحد المرشحين طلب الحصول على أي وظيفة تم إدراج مجموعة المهارات المطلوبة لها، يتم إرسال بريد إلكتروني للإعلام عند وجود تطابق ملحوظ بين مهارات المرشح والمهارات المخزنة في SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-127">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="d1ce1-128">ويساعد هذا في ملء المناصب المطلوبة بشكل مُلح بسرعة أكبر، لأن الإخطارات تساعد مسؤولي التعيين على توظيف المرشحين عبر المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-128">This helps fill positions that are urgently required faster, because the notifications help recruiters cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="d1ce1-129">يمكن توسيع هذا القالب لتمكين استخدامه لأي سيناريو يشتمل على تكامل SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-129">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="d1ce1-130">لتنزيل القالب **تكامل Power Automate – SharePoint**، انتقل إلى [تكامل Power Automate – SharePoint](https://go.microsoft.com/fwlink/?linkid=2082109) على مركز التنزيل لـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-130">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="d1ce1-131">تطبيق Referral</span><span class="sxs-lookup"><span data-stu-id="d1ce1-131">Referral App</span></span>

<span data-ttu-id="d1ce1-132">يمكنك استخدام التطبيق Referral لإضافة مرشحين إلى مجموعة مواهب مشتركة.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-132">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="d1ce1-133">بإمكان المحيل إدخال **الاسم الأول** و **اسم العائلة** و **البريد الإلكتروني** و **Linkedln URL** عند إرسال مرشح.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-133">The referrer can enter **Firstname**, **Lastname**, **Email**, and **LinkedIn URL** when submitting a candidate.</span></span> <span data-ttu-id="d1ce1-134">يتم بعد ذلك ملء بيانات تعريف مصدر المرشح بواسطة معلومات المحيل.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-134">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="d1ce1-135">يمكنك تضمين هذا التطبيق في الخدمة الذاتية للموظف لإرسال الإحالات، أو يمكنك استخدامه كارتباط تشعبي في مدخل الشركة وتشغيله كتطبيق مستقل.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-135">You can embed this app in Employee self service for submitting referrals, or you can use it as a hyperlink in the corporate portal and run it as a stand-alone app.</span></span>

<span data-ttu-id="d1ce1-136">لتنزيل **تطبيق Referral**، انتقل إلى [حل قابلية التوسعة في Dynamics 365 Talent: تطبيق Referral](https://www.microsoft.com/download/details.aspx?id=58497) في مركز التنزيل لـ Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-136">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) on the Microsoft Download Center.</span></span> <span data-ttu-id="d1ce1-137">يمكنك استيراد هذا التطبيق وتخصيصه لإضافة المزيد من الوظائف.</span><span class="sxs-lookup"><span data-stu-id="d1ce1-137">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1ce1-138">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="d1ce1-138">Additional resources</span></span>

[<span data-ttu-id="d1ce1-139">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="d1ce1-139">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="d1ce1-140">ترحيل التطبيق بين المستأجرين والبيئات</span><span class="sxs-lookup"><span data-stu-id="d1ce1-140">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
