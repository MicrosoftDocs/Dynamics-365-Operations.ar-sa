---
title: الأسئلة المتداولة حول العرض المباشر
description: يسرد هذا الموضوع الأسئلة المتداولة حول كيفية القيام بالعرض المباشر باستخدام مشروع تنفيذ Dynamics 365 Human Resources.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cbf00f7428c9b1852a5bf54fd7e30a3bddc1a31e
ms.sourcegitcommit: 0e60df840688932795b9c8f8fd45d98f5ab6ba8c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/03/2020
ms.locfileid: "4668935"
---
# <a name="go-live-faq"></a><span data-ttu-id="4bddf-103">الأسئلة المتداولة حول العرض المباشر</span><span class="sxs-lookup"><span data-stu-id="4bddf-103">Go-live FAQ</span></span> 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4bddf-104">يسرد هذا الموضوع الأسئلة المتداولة حول كيفية القيام بالعرض المباشر باستخدام مشروع تنفيذ Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4bddf-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="4bddf-105">متى يمكنني تكوين بيئة تشغيل وطلبها؟</span><span class="sxs-lookup"><span data-stu-id="4bddf-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="4bddf-106">وعادة ما يتم نشر بيئة التشغيل بعد تلبية المعايير التالية:</span><span class="sxs-lookup"><span data-stu-id="4bddf-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="4bddf-107">تكون كافة التخصيصات كاملة الأكواد.</span><span class="sxs-lookup"><span data-stu-id="4bddf-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="4bddf-108">تم إكمال اختبارات قبول المستخدم (UAT).</span><span class="sxs-lookup"><span data-stu-id="4bddf-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="4bddf-109">قام العميل بتسجيل الخروج من الحل.</span><span class="sxs-lookup"><span data-stu-id="4bddf-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="4bddf-110">لا توجد مشكلات حظر عن العرض المباشر.</span><span class="sxs-lookup"><span data-stu-id="4bddf-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="4bddf-111">عندما يكون العملاء المؤهلين في هذه المرحلة، سيعمل فريق Microsoft FastTrack بفريق المشروع على القيام بتقييم العرض المباشر.</span><span class="sxs-lookup"><span data-stu-id="4bddf-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="4bddf-112">ما المتطلبات الأساسية لنشر بيئة تشغيل؟</span><span class="sxs-lookup"><span data-stu-id="4bddf-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="4bddf-113">للحصول على قائمة بالمتطلبات الأساسية، راجع [إعداد العرض المباشر](hr-admin-go-live-prepare.md).</span><span class="sxs-lookup"><span data-stu-id="4bddf-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="4bddf-114">ما المقصود بتقييم العرض المباشر؟</span><span class="sxs-lookup"><span data-stu-id="4bddf-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="4bddf-115">يُعد تقييم العرض المباشر جزءًا من  [برنامج Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span><span class="sxs-lookup"><span data-stu-id="4bddf-115">The go-live assessment is part of the [Microsoft FastTrack program](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span></span> <span data-ttu-id="4bddf-116">أثناء هذه المراجعة، يقيم مهندس الحلول ما إذا كان مشروع التنفيذ جاهزًا للتحول الناجح والعرض المباشر.</span><span class="sxs-lookup"><span data-stu-id="4bddf-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="4bddf-117">هذه المراجعة إلزامية بالنسبة لكل مشروع تنفيذ قبل أن تتمكن من طلب العرض المباشر في بيئة التشغيل.</span><span class="sxs-lookup"><span data-stu-id="4bddf-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="4bddf-118">يتم نشر بيئات الحماية في مركز بيانات وسط الولايات المتحدة.</span><span class="sxs-lookup"><span data-stu-id="4bddf-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="4bddf-119">نحن نريد نشر بيئات التشغيل التابعة لنا في مركز بيانات غرب الولايات المتحدة.</span><span class="sxs-lookup"><span data-stu-id="4bddf-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="4bddf-120">هل يمكنني تحديد غرب الولايات المتحدة كمركز بيانات في تكوين التشغيل؟</span><span class="sxs-lookup"><span data-stu-id="4bddf-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="4bddf-121">لا تقيدك خدمات LCS عن تحديد مركز بيانات مختلف عند نشر بيئة موارد بشرية، ولكننا نوصي بشدة بعدم تحديد مركز بيانات مختلف.</span><span class="sxs-lookup"><span data-stu-id="4bddf-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="4bddf-122">إذا كنت ترغب في أن تكون بيئة التشغيل الخاصة بك في مركز بيانات غرب الولايات المتحدة، يجب أولاً إعادة نشر بيئات الحماية الخاصة بك على مركز بيانات غرب الولايات المتحدة واختبارها وتسجيل الخروج منها.</span><span class="sxs-lookup"><span data-stu-id="4bddf-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="4bddf-123">للحصول على معلومات حول تحديد مركز البيانات الصحيح، راجع [متطلبات الشبكة](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span><span class="sxs-lookup"><span data-stu-id="4bddf-123">For information about selecting the correct datacenter, see [Network requirements](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="4bddf-124">ما مستوى الوصول الذي يوجد لدي لموارد Azure لبيئات الموارد البشرية الخاصة بي؟</span><span class="sxs-lookup"><span data-stu-id="4bddf-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="4bddf-125">يقتصر الوصول إلى بيئات الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="4bddf-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="4bddf-126">لا يمكنك الوصول إلى الجهاز الظاهري (VM) أو Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="4bddf-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="4bddf-127">ولا يمكنك أيضًا الوصول إلى قاعدة البيانات عبر Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="4bddf-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="4bddf-128">على الرغم من أنه يتعذر عليك الوصول إلى موارد Azure الخاصة بك أو بيئة Dynamics 365 Human Resources مباشرة، إلا أنه توجد ميزات إضافية يمكنك استخدامها للوصول إلى البيانات الخاصة بك:</span><span class="sxs-lookup"><span data-stu-id="4bddf-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="4bddf-129">يمكنك نشر قاعدة بيانات Azure SQL في مستأجر Azure الخاص بك واستخدام ميزة "‏‫إحضار قاعدة بياناتك الخاصة" (BYOD) لمزامنة البيانات.</span><span class="sxs-lookup"><span data-stu-id="4bddf-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="4bddf-130">لمزيد من المعلومات، راجع [إحضار قاعدة بياناتك الخاصة‬ (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span><span class="sxs-lookup"><span data-stu-id="4bddf-130">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span>

- <span data-ttu-id="4bddf-131">يمكنك استخدام تكامل Common Data Service لمزامنة تحديد الكيانات في قاعدة بيانات Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4bddf-131">You can use Common Data Service integration to synchronize select entities into the Common Data Service database.</span></span> <span data-ttu-id="4bddf-132">لمزيد من المعلومات، راجع [Common Data Service كيانات](hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="4bddf-132">For more information, see [Common Data Service entities](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="4bddf-133">كم مرة يتم نسخ قاعدة بيانات الإنتاج احتياطيًا؟</span><span class="sxs-lookup"><span data-stu-id="4bddf-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="4bddf-134">تتم حماية قواعد البيانات بواسطة النسخ الاحتياطي التلقائي بالتكرارات التالية:</span><span class="sxs-lookup"><span data-stu-id="4bddf-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="4bddf-135">نوع النسخ الاحتياطي</span><span class="sxs-lookup"><span data-stu-id="4bddf-135">Type of backup</span></span> | <span data-ttu-id="4bddf-136">التكرار</span><span class="sxs-lookup"><span data-stu-id="4bddf-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="4bddf-137">عملية النسخ الاحتياطي الكاملة لقاعدة البيانات‬</span><span class="sxs-lookup"><span data-stu-id="4bddf-137">Full database backup</span></span> | <span data-ttu-id="4bddf-138">أسبوعي</span><span class="sxs-lookup"><span data-stu-id="4bddf-138">Weekly</span></span> |
| <span data-ttu-id="4bddf-139">نسخ احتياطي تفاضلي لقاعدة بيانات</span><span class="sxs-lookup"><span data-stu-id="4bddf-139">Differential database backup</span></span> | <span data-ttu-id="4bddf-140">كل 12-24 ساعة</span><span class="sxs-lookup"><span data-stu-id="4bddf-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="4bddf-141">نسخ احتياطي لسجل الحركة</span><span class="sxs-lookup"><span data-stu-id="4bddf-141">Transaction log backup</span></span> | <span data-ttu-id="4bddf-142">كل 5 إلى 10 دقائق</span><span class="sxs-lookup"><span data-stu-id="4bddf-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="4bddf-143">تحتفظ Microsoft بالنسخ الاحتياطية الكافية للسماح لاستعادة النقطة الزمنية (PITR) خلال الـ 14 يومًا الماضية.</span><span class="sxs-lookup"><span data-stu-id="4bddf-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last 14 days.</span></span> 

<span data-ttu-id="4bddf-144">للحصول على مزيد من المعلومات، راجع  [تعرف على عمليات النسخ الاحتياطي التلقائي لقاعدة بيانات SQL](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span><span class="sxs-lookup"><span data-stu-id="4bddf-144">For more information, see [Learn about automatic SQL Database backups](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="4bddf-145">هل يمكنني طلب نسخة من النسخ الاحتياطي لقاعدة بيانات الإنتاج الخاصة بي؟</span><span class="sxs-lookup"><span data-stu-id="4bddf-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="4bddf-146">الرقم</span><span class="sxs-lookup"><span data-stu-id="4bddf-146">No.</span></span> <span data-ttu-id="4bddf-147">ومع ذلك، يمكنك إرسال طلب خدمة تحديث قاعدة البيانات لنسخ بيئة التشغيل الخاصة بك إلى بيئة الحماية.</span><span class="sxs-lookup"><span data-stu-id="4bddf-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="4bddf-148">يمكنك نشر قاعدة بيانات Azure SQL في مستأجر Azure الخاص بك واستخدام ميزة BYOD لمزامنة البيانات من بيئة التشغيل الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="4bddf-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="4bddf-149">لمزيد من المعلومات، راجع [إحضار قاعدة بياناتك الخاصة‬ (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span><span class="sxs-lookup"><span data-stu-id="4bddf-149">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="4bddf-150">كيف يمكنني نقل بيئة الحماية الخاصة بك إلى إنتاج العرض المباشر؟</span><span class="sxs-lookup"><span data-stu-id="4bddf-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="4bddf-151">ونظرًا لأن ميزة النسخ غير متاحة لنقل البيئة الخاصة بك من بيئة الحماية إلى بيئة التشغيل، فإنه يجب عليك استخدام حزم البيانات لنقل البيانات إلى بيئة التشغيل الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="4bddf-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="4bddf-152">نوصي بالاحتفاظ بقائمة واضحة من الكيانات التي تم تكوينها في بيئة الحماية خلال المشروع.</span><span class="sxs-lookup"><span data-stu-id="4bddf-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="4bddf-153">ثم اختبار عملية التكوين المرحلي وترحيل أية حزم بيانات مطلوبة للانتقال للعرض المباشر.</span><span class="sxs-lookup"><span data-stu-id="4bddf-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="4bddf-154">يجب عليك نقل أية حزم بيانات يدويًا إلى بيئة التشغيل عندما تكون جاهزًا للعرض المباشر.</span><span class="sxs-lookup"><span data-stu-id="4bddf-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="4bddf-155">ما الذي ينبغي على فعله إذا ما توقفت بيئة التشغيل الخاصة بي؟</span><span class="sxs-lookup"><span data-stu-id="4bddf-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="4bddf-156">للإبلاغ عن انقطاع الإنتاج، اتبع العملية الموضحة في [الإبلاغ عن انقطاع الإنتاج](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span><span class="sxs-lookup"><span data-stu-id="4bddf-156">To report a Production outage, follow the process described in [Report a production outage](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="4bddf-157">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="4bddf-157">See also</span></span>

 [<span data-ttu-id="4bddf-158">الإعداد للعرض المباشر</span><span class="sxs-lookup"><span data-stu-id="4bddf-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)
