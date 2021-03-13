---
title: تحديث العملية
description: إن Microsoft Dynamics 365 Human Resources عبارة عن خدمة تأجير برامج (SaaS) حقيقية توفر تحديثات خدمة مستمرة بدون لمس للتغييرات في التطبيق والنظام الأساسي.
author: andreabichsel
manager: tfehr
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bb5f7dc17c8f4f3a54bd285cb55088f2176db4a
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111311"
---
# <a name="update-process"></a><span data-ttu-id="b39d7-103">تحديث العملية</span><span class="sxs-lookup"><span data-stu-id="b39d7-103">Update process</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b39d7-104">يُعد Microsoft Dynamics 365 Human Resources بمثابة خدمة تأجير برامج (SaaS) حقيقة توفير تحديثات خدمة مستمرة بدون لمس.</span><span class="sxs-lookup"><span data-stu-id="b39d7-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="b39d7-105">تحتوي هذه التحديثات على تغييرات في كل من التطبيق والنظام الأساسي التي غالبًا ما توفر تحسينات هامة للخدمة، بما في ذلك التحديثات التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="b39d7-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="b39d7-106">سياسة التحديث</span><span class="sxs-lookup"><span data-stu-id="b39d7-106">Update policy</span></span>

<span data-ttu-id="b39d7-107">يتم إصدار التحديثات في وتيرة منتظمة لجميع البيئات.</span><span class="sxs-lookup"><span data-stu-id="b39d7-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="b39d7-108">يتم دعم Human Resources وفقًا لـ [سياسة دورة حياة Microsoft](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy)،  التي توفر إرشادات متناسقة ومتوقعة لتوفر الدعم.</span><span class="sxs-lookup"><span data-stu-id="b39d7-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="b39d7-109">وتيرة الإصدار</span><span class="sxs-lookup"><span data-stu-id="b39d7-109">Release cadence</span></span> 

<span data-ttu-id="b39d7-110">يتم تطبيق تحديثات Human Resources على كافة البيئات تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="b39d7-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="b39d7-111">يوفر Human Resources نوعين من الإصدارات:</span><span class="sxs-lookup"><span data-stu-id="b39d7-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="b39d7-112">**تحديثات الخدمة**: تتم التحديثات كل أسبوعين وتشمل إصلاحات الأخطاء والميزات الجديدة.</span><span class="sxs-lookup"><span data-stu-id="b39d7-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="b39d7-113">وتتضمن تحديثات الخدمة أيضًا تحديثا النظام الأساسي المطبقة عند إصدارها.</span><span class="sxs-lookup"><span data-stu-id="b39d7-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="b39d7-114">للحصول على فكرة عن وقت إصدار تحديثات النظام الأساسي، راجع [الجدول 3: إصدارات النظام الأساسي](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="b39d7-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="b39d7-115">تحتوي التحديثات كل أسبوعين على عملية تمهيدية عامة مقسمة عبر مناطق.</span><span class="sxs-lookup"><span data-stu-id="b39d7-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="b39d7-116">لمزيد من المعلومات حول التحديثات كل أسبوعين، راجع [راجع ما هو الجديد أو المتغير في Dynamics 365 Human Resources](hr-admin-whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="b39d7-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="b39d7-117">يتم تحديث كافة مراكز بيانات المدعومة كل أسبوعين، ما لم يرد خلاف ذلك.</span><span class="sxs-lookup"><span data-stu-id="b39d7-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="b39d7-118">يتم تضمين مناطق الولايات المتحدة الأمريكية وأوروبا والمملكة المتحدة وآسيا وكندا في التحديثات كل أسبوعين.</span><span class="sxs-lookup"><span data-stu-id="b39d7-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="b39d7-119">**تحديثات حل Dataverse**: تُجرى هذه التحديثات كل ستة أسابيع تقريبًا، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="b39d7-119">**Dataverse solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="b39d7-120">وهي تتضمن كيانات جديدة وتغييرات للكيانات الموجودة في Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b39d7-120">They include new entities and changes to existing entities in Dataverse.</span></span> <span data-ttu-id="b39d7-121">وتصدر هذه التحديثات لنفس المناطق بوصفها التحديثات كل أسبوعين، وتستغرق حوالي ستة أسابيع للنسخ المتماثل عبر كافة مراكز البيانات.</span><span class="sxs-lookup"><span data-stu-id="b39d7-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="b39d7-122">قد تتوافق أو لا تتوافق تحديثات الحلول مع تحديثات الخدمة كل أسبوعين.</span><span class="sxs-lookup"><span data-stu-id="b39d7-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="b39d7-123">تتوفر تحديثات الحلول في كافة مراكز البيانات بمجرد إصدارها.</span><span class="sxs-lookup"><span data-stu-id="b39d7-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="b39d7-124">إذا كنت لا ترغب في انتظار التحديثات للنسخ المتماثل تلقائيًا، يُمكن تطبيق هذه التحديثات يدويًا على أي بيئة في أي مركز بيانات.</span><span class="sxs-lookup"><span data-stu-id="b39d7-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="b39d7-125">عند الحاجة، يوفر Human Resources أيضًا الأنواع التالية من الإصلاحات:</span><span class="sxs-lookup"><span data-stu-id="b39d7-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="b39d7-126">**مراجعة (إصلاح عاجل)**: إصلاحات الأخطاء التي قد تحدث مع أو بعيدًا عن إصدار تحديث الخدمة كل أسبوعين</span><span class="sxs-lookup"><span data-stu-id="b39d7-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="b39d7-127">**إصلاح طارئ**: يُمكن أن تشمل الاصلاحات العاجلة الاستباقية والتفاعلية ذات الطبيعة المستقلة التكوين فقط أو تغييرات الكود لحل مشاكل العرض المباشر، وقد تحدث بغض النظر عن إصدار تحديث الخدمة كل أسبوعين.</span><span class="sxs-lookup"><span data-stu-id="b39d7-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="b39d7-128">تتم مراجعة الإصدارات واختبارها والتحقق من صحتها في بيئة داخلية.</span><span class="sxs-lookup"><span data-stu-id="b39d7-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="b39d7-129">بعد تسجيل الخروج من الإصدارات، يتم نشرها بعد ذلك إلى الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="b39d7-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2020"></a><span data-ttu-id="b39d7-130">إصدار استثناءات الوتيرة في 2020</span><span class="sxs-lookup"><span data-stu-id="b39d7-130">Release cadence exceptions in 2020</span></span>

<span data-ttu-id="b39d7-131">لحساب الإجازات، يكون جدول الإصدار لشهري نوفمبر وديسمبر 2020 كالتالي:</span><span class="sxs-lookup"><span data-stu-id="b39d7-131">To account for holidays, the release schedule for November and December 2020 is as follows:</span></span>

- <span data-ttu-id="b39d7-132">إصدار شهر نوفمبر: 2 نوفمبر - 13 نوفمبر</span><span class="sxs-lookup"><span data-stu-id="b39d7-132">November release: November 2 - November 13</span></span>
- <span data-ttu-id="b39d7-133">إصدار شهر ديسمبر: 30 نوفمبر - 11 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="b39d7-133">December release: November 30 - December 11</span></span>
 
<span data-ttu-id="b39d7-134">سيتم استئناف وتيرة الإصدار من أسبوعين بالشكل المعتاد في 11 يناير 2021.</span><span class="sxs-lookup"><span data-stu-id="b39d7-134">The two-week release cadence will resume as usual on January 11, 2021.</span></span>

## <a name="communications"></a><span data-ttu-id="b39d7-135">المراسلات</span><span class="sxs-lookup"><span data-stu-id="b39d7-135">Communications</span></span>

<span data-ttu-id="b39d7-136">يُمكنك معرفة ما هو الموجود في الأعمال الخاصة بـ Human Resources وما قمنا بإصداره في المواقع التالية:</span><span class="sxs-lookup"><span data-stu-id="b39d7-136">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="b39d7-137">مخطط Dynamics 365 Human Resources </span><span class="sxs-lookup"><span data-stu-id="b39d7-137">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="b39d7-138">خطط إصدار Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b39d7-138">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="b39d7-139">ما الجديد أو المتغير‬ في Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="b39d7-139">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="b39d7-140">[البحث عن المشاكل في Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (لإصلاح الأخطاء المتعلقة بالنظام الأساسي فقط)</span><span class="sxs-lookup"><span data-stu-id="b39d7-140">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="b39d7-141">مدونة Human Resources</span><span class="sxs-lookup"><span data-stu-id="b39d7-141">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="b39d7-142">مجتمع Human Resources Yammer</span><span class="sxs-lookup"><span data-stu-id="b39d7-142">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="b39d7-143">ميزات المعاينة في بيئة الحماية</span><span class="sxs-lookup"><span data-stu-id="b39d7-143">Preview features in a sandbox environment</span></span>

<span data-ttu-id="b39d7-144">يُمكنك التحقق من صحة ميزات المعاينة في بيئة الحماية قبل تمكينها في بيئة الإنتاج الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="b39d7-144">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="b39d7-145">لمزيد من المعلومات حول تمكين الميزات، راجع [نظرة عامة على إدارة الميزات](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="b39d7-145">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="b39d7-146">تبقي كافة الميزات الجديدة في معاينه لمده 30 يوما على الأقل، وبشكل نموذجي 30-60 يوما.</span><span class="sxs-lookup"><span data-stu-id="b39d7-146">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="b39d7-147">تتوفر الميزات الرئيسية بشكل عام في أكتوبر و ابريل من كل عام يتبع فتره المعاينة.</span><span class="sxs-lookup"><span data-stu-id="b39d7-147">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="b39d7-148">بمجرد ان تشاهد إمكانيات جديده في مساحة عمل إدارة الميزات، يمكنك تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="b39d7-148">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="b39d7-149">قد تكون بعض الميزات قيد التشغيل بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="b39d7-149">Some features may be on by default.</span></span>

<span data-ttu-id="b39d7-150">في بعض الأوقات، سيتم تشغيل ميزه متكاملة بشكل افتراضي ولا يمكن إيقاف تشغيلها (على سبيل المثال مساحة عمل إدارة الميزات).</span><span class="sxs-lookup"><span data-stu-id="b39d7-150">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="b39d7-151">وبمجرد توفر إحدى الميزات بصفه عامه، قد يتم تشغيلها أو إيقاف تشغيلها في بيئات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="b39d7-151">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="b39d7-152">وتشير مساحة عمل إدارة الميزات إلى ان ميزه المعاينة ستصبح إلزاميه.</span><span class="sxs-lookup"><span data-stu-id="b39d7-152">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="b39d7-153">وعاده ما يكون هذا التاريخ في يوم 1 أكتوبر أو 1 إبريل لكي تتم محاذاته مع خطط الإصدار نصف السنوية.</span><span class="sxs-lookup"><span data-stu-id="b39d7-153">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="b39d7-154">لا يمكنك إيقاف تشغيل الميزات الإلزامية.</span><span class="sxs-lookup"><span data-stu-id="b39d7-154">You can't turn off mandatory features.</span></span> <span data-ttu-id="b39d7-155">وحتى تصبح إلزاميا، يمكنك تشغيل أحدي الميزات وإيقاف تشغيلها في كافة البيئات.</span><span class="sxs-lookup"><span data-stu-id="b39d7-155">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="b39d7-156">نوصي بشدة بمعاينة الميزات في بيئة الحماية أو البيئة التجريبية.</span><span class="sxs-lookup"><span data-stu-id="b39d7-156">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="b39d7-157">من الأفضل إنشاء نسخة من بيئة الإنتاج الحالية أو قاعدة البيانات في بيئة الحماية بحيث يمكنك الحصول على التجربة الكاملة للميزات الجديدة مع الميزات الجديدة مع البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="b39d7-157">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="b39d7-158">لمزيد من المعلومات حول توفير بيئة حماية، راجع [توفير مشروع Human Resources](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="b39d7-158">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="b39d7-159">لإزالة بيئة اختبار، راجع [إزالة مثيل](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="b39d7-159">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="b39d7-160">الإبلاغ عن الأخطاء</span><span class="sxs-lookup"><span data-stu-id="b39d7-160">Report bugs</span></span>

<span data-ttu-id="b39d7-161">أثناء اختبار ميزات المعاينة أو تجربة إمكانيات جديدة، قد تجد عناصر لا تعمل بالشكل المتوقع.</span><span class="sxs-lookup"><span data-stu-id="b39d7-161">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="b39d7-162">يُرجى الإبلاغ عن أي أخطاء من خلال [دعم Microsoft Dynamics 365](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="b39d7-162">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="b39d7-163">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="b39d7-163">See also</span></span>

[<span data-ttu-id="b39d7-164">خطط إصدار Dynamics 365 و Power Platform</span><span class="sxs-lookup"><span data-stu-id="b39d7-164">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)</br>
[<span data-ttu-id="b39d7-165">ما هو الجديد أو المتغير في Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="b39d7-165">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="b39d7-166">سياسة دورة حياة البرامج</span><span class="sxs-lookup"><span data-stu-id="b39d7-166">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

