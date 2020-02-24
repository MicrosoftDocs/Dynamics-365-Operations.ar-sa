---
title: عملية التحديث
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1817e072805bafbf0d5a9eb2698ef75abc75ad68
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031080"
---
# <a name="update-process"></a><span data-ttu-id="f081b-102">عملية التحديث</span><span class="sxs-lookup"><span data-stu-id="f081b-102">Update process</span></span>

<span data-ttu-id="f081b-103">يُعد Microsoft Dynamics 365 Human Resources بمثابة خدمة تأجير برامج (SaaS) حقيقة توفير تحديثات خدمة مستمرة بدون لمس.</span><span class="sxs-lookup"><span data-stu-id="f081b-103">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="f081b-104">تحتوي هذه التحديثات علي تغييرات في كل من التطبيق والنظام الأساسي التي غالبًا ما توفر تحسينات هامة للخدمة، بما في ذلك التحديثات التنظيمية.</span><span class="sxs-lookup"><span data-stu-id="f081b-104">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="f081b-105">سياسة التحديث</span><span class="sxs-lookup"><span data-stu-id="f081b-105">Update policy</span></span>

<span data-ttu-id="f081b-106">يتم إصدار التحديثات في وتيرة منتظمة لجميع البيئات.</span><span class="sxs-lookup"><span data-stu-id="f081b-106">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="f081b-107">يتم دعم Human Resources وفقًا لـ [سياسة دورة حياة Microsoft](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy)،  التي توفر إرشادات متناسقة ومتوقعة لتوفر الدعم.</span><span class="sxs-lookup"><span data-stu-id="f081b-107">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="f081b-108">وتيرة الإصدار</span><span class="sxs-lookup"><span data-stu-id="f081b-108">Release cadence</span></span>

<span data-ttu-id="f081b-109">يتم تطبيق تحديثات Human Resources علي كافة البيئات تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="f081b-109">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="f081b-110">يوفر Human Resources نوعين من الإصدارات:</span><span class="sxs-lookup"><span data-stu-id="f081b-110">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="f081b-111">**تحديثات الخدمة**: تحديثات أسبوعية تشمل إصلاحات الأخطاء والميزات الجديدة.</span><span class="sxs-lookup"><span data-stu-id="f081b-111">**Service updates**: Weekly updates that include bug fixes and new features.</span></span> <span data-ttu-id="f081b-112">وتتضمن تحديثات الخدمة أيضًا تحديثا النظام الأساسي المطبقة عند إصدارها.</span><span class="sxs-lookup"><span data-stu-id="f081b-112">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="f081b-113">للحصول على فكرة عن وقت إصدار تحديثات النظام الأساسي، راجع [الجدول 3: إصدارات النظام الأساسي](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="f081b-113">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="f081b-114">يتم إصدار التحديثات الأسبوعية عادةً في أيام الأربعاء.</span><span class="sxs-lookup"><span data-stu-id="f081b-114">Weekly updates usually release on Wednesdays.</span></span> <span data-ttu-id="f081b-115">لمزيد من المعلومات حول التحديثات الأسبوعية، راجع [راجع ما هو الجديد أو المتغير في Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).</span><span class="sxs-lookup"><span data-stu-id="f081b-115">For more information about weekly updates, see [What's new or changed in Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).</span></span>

    <span data-ttu-id="f081b-116">يتم تحديث كافة مراكز بيانات المدعومة أسبوعيًا، ما لم يرد خلاف ذلك.</span><span class="sxs-lookup"><span data-stu-id="f081b-116">All supported data centers update weekly, unless otherwise noted.</span></span> <span data-ttu-id="f081b-117">تبدأ التحديثات الأسبوعية عادةًا في يوم الأربعاء وتنتهي بحلول يوم الأحد.</span><span class="sxs-lookup"><span data-stu-id="f081b-117">Weekly updates typically begin on Wednesday and complete by Sunday.</span></span> <span data-ttu-id="f081b-118">يتم تضمين مناطق الولايات المتحدة الأمريكية وأوروبا والمملكة المتحدة وآسيا وكندا في التحديثات الأسبوعية.</span><span class="sxs-lookup"><span data-stu-id="f081b-118">US, Australia, Europe, UK, Asia, and Canada regions are included in weekly updates.</span></span> 

- <span data-ttu-id="f081b-119">**تحديثات حل Common Data Service**: تُجرى هذه التحديثات كل ستة أسابيع تقريبًا، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="f081b-119">**Common Data Service solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="f081b-120">وهي تتضمن كيانات جديدة وتغييرات للكيانات الموجودة في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f081b-120">They include new entities and changes to existing entities in Common Data Service.</span></span> <span data-ttu-id="f081b-121">وتصدر هذه التحديثات لنفس المناطق بوصفها التحديثات الأسبوعية، وتستغرق حوالي ستة أسابيع للنسخ المتماثل عبر كافة مراكز البيانات.</span><span class="sxs-lookup"><span data-stu-id="f081b-121">These updates release to the same regions as the weekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="f081b-122">قد تتوافق أو لا تتوافق تحديثات الحلول مع تحديثات الخدمة الأسبوعية.</span><span class="sxs-lookup"><span data-stu-id="f081b-122">Solution updates may or may not align with weekly service updates.</span></span>

<span data-ttu-id="f081b-123">يعرض الجدول التالي عينه من الجدول:</span><span class="sxs-lookup"><span data-stu-id="f081b-123">The following table shows a sample schedule:</span></span>

| <span data-ttu-id="f081b-124">الأسبوع</span><span class="sxs-lookup"><span data-stu-id="f081b-124">Week</span></span> | <span data-ttu-id="f081b-125">نوع التحديث</span><span class="sxs-lookup"><span data-stu-id="f081b-125">Update type</span></span> |
| --- | --- |
| <span data-ttu-id="f081b-126">1</span><span class="sxs-lookup"><span data-stu-id="f081b-126">1</span></span> | <span data-ttu-id="f081b-127">تحديث الخدمة (كافة المناطق)</span><span class="sxs-lookup"><span data-stu-id="f081b-127">Service update (all regions)</span></span> |
| <span data-ttu-id="f081b-128">2</span><span class="sxs-lookup"><span data-stu-id="f081b-128">2</span></span> | <span data-ttu-id="f081b-129">تحديث الخدمة (كافة المناطق) + تحديث الحل (مناطق الأسبوع 1)</span><span class="sxs-lookup"><span data-stu-id="f081b-129">Service update (all regions) + Solution update (Week 1 regions)</span></span> |
| <span data-ttu-id="f081b-130">3</span><span class="sxs-lookup"><span data-stu-id="f081b-130">3</span></span> | <span data-ttu-id="f081b-131">تحديث الخدمة (كافة المناطق) + تحديث الحل (مناطق الأسبوع 2)</span><span class="sxs-lookup"><span data-stu-id="f081b-131">Service update (all regions) + Solution update (Week 2 regions)</span></span> |
| <span data-ttu-id="f081b-132">4</span><span class="sxs-lookup"><span data-stu-id="f081b-132">4</span></span> | <span data-ttu-id="f081b-133">تحديث الخدمة (كافة المناطق) + تحديث الحل (مناطق الأسبوع 3)</span><span class="sxs-lookup"><span data-stu-id="f081b-133">Service update (all regions) + Solution update (Week 3 regions)</span></span> |
| <span data-ttu-id="f081b-134">5</span><span class="sxs-lookup"><span data-stu-id="f081b-134">5</span></span> | <span data-ttu-id="f081b-135">تحديث الخدمة (كافة المناطق) + تحديث الحل (مناطق الأسبوع 4)</span><span class="sxs-lookup"><span data-stu-id="f081b-135">Service update (all regions) + Solution update (Week 4 regions)</span></span> |
| <span data-ttu-id="f081b-136">6</span><span class="sxs-lookup"><span data-stu-id="f081b-136">6</span></span> | <span data-ttu-id="f081b-137">تحديث الخدمة (كافة المناطق) + تحديث الحل (مناطق الأسبوع 5)</span><span class="sxs-lookup"><span data-stu-id="f081b-137">Service update (all regions) + Solution update (Week 5 regions)</span></span> |
| <span data-ttu-id="f081b-138">7</span><span class="sxs-lookup"><span data-stu-id="f081b-138">7</span></span> | <span data-ttu-id="f081b-139">تحديث الخدمة (كافة المناطق) + تحديث الحل (مناطق الأسبوع 6)</span><span class="sxs-lookup"><span data-stu-id="f081b-139">Service update (all regions) + Solution update (Week 6 regions)</span></span> |
| <span data-ttu-id="f081b-140">8</span><span class="sxs-lookup"><span data-stu-id="f081b-140">8</span></span> | <span data-ttu-id="f081b-141">تحديث الخدمة (كافة المناطق)</span><span class="sxs-lookup"><span data-stu-id="f081b-141">Service update (all regions)</span></span> |

> [!NOTE]
> <span data-ttu-id="f081b-142">تتوفر تحديثات الحلول في كافة مراكز البيانات بمجرد إصدارها.</span><span class="sxs-lookup"><span data-stu-id="f081b-142">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="f081b-143">إذا كنت لا ترغب في انتظار التحديثات للنسخ المتماثل تلقائيًا، يُمكن تطبيق هذه التحديثات يدويًا على أي بيئة في أي مركز بيانات.</span><span class="sxs-lookup"><span data-stu-id="f081b-143">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="f081b-144">عند الحاجة، يوفر Human Resources أيضًا الأنواع التالية من الإصلاحات:</span><span class="sxs-lookup"><span data-stu-id="f081b-144">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="f081b-145">**مراجعة (إصلاح عاجل)**: إصلاحات الأخطاء التي قد تحدث مع أو بعيدًا عن إصدار تحديث الخدمة الأسبوعي</span><span class="sxs-lookup"><span data-stu-id="f081b-145">**Revision (hotfix)**: bug fixes that can occur either with or apart from a weekly service update release</span></span>

- <span data-ttu-id="f081b-146">**إصلاح طارئ**: يُمكن أن تشمل الاصلاحات العاجلة الاستباقية والتفاعلية ذات الطبيعة المستقلة التكوين فقط أو تغييرات الكود لحل مشاكل العرض المباشر، وقد تحدث بغض النظر عن إصدار تحديث الخدمة الأسبوعي.</span><span class="sxs-lookup"><span data-stu-id="f081b-146">**Emergency fix**: proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a weekly service update release</span></span>

<span data-ttu-id="f081b-147">تتم مراجعة الإصدارات واختبارها والتحقق من صحتها في بيئة داخلية.</span><span class="sxs-lookup"><span data-stu-id="f081b-147">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="f081b-148">بعد تسجيل الخروج من الإصدارات، يتم نشرها بعد ذلك إلى الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f081b-148">After builds are signed off, they're then deployed to production.</span></span>

## <a name="exceptions-in-2019"></a><span data-ttu-id="f081b-149">الاستثناءات في 2019</span><span class="sxs-lookup"><span data-stu-id="f081b-149">Exceptions in 2019</span></span>

<span data-ttu-id="f081b-150">تعتبر التواريخ التالية استثناءات لجدول الإصدار المنتظم:</span><span class="sxs-lookup"><span data-stu-id="f081b-150">The following dates are exceptions to the regular release schedule:</span></span>

| <span data-ttu-id="f081b-151">التاريخ</span><span class="sxs-lookup"><span data-stu-id="f081b-151">Date</span></span> | <span data-ttu-id="f081b-152">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="f081b-152">Description</span></span> |
| --- | --- |
| <span data-ttu-id="f081b-153">أسبوع من 25 نوفمبر</span><span class="sxs-lookup"><span data-stu-id="f081b-153">Week of November 25</span></span> | <span data-ttu-id="f081b-154">لا توجد تحديثات</span><span class="sxs-lookup"><span data-stu-id="f081b-154">No updates</span></span> |
| <span data-ttu-id="f081b-155">أسبوع من 16 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="f081b-155">Week of December 16</span></span> | <span data-ttu-id="f081b-156">تحديثات ثانوية فقط</span><span class="sxs-lookup"><span data-stu-id="f081b-156">Minor updates only</span></span> |
| <span data-ttu-id="f081b-157">أسبوع من 23 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="f081b-157">Week of December 23</span></span> | <span data-ttu-id="f081b-158">لا توجد تحديثات</span><span class="sxs-lookup"><span data-stu-id="f081b-158">No updates</span></span> |
| <span data-ttu-id="f081b-159">أسبوع من 30 ديسمبر</span><span class="sxs-lookup"><span data-stu-id="f081b-159">Week of December 30</span></span> | <span data-ttu-id="f081b-160">لا توجد تحديثات</span><span class="sxs-lookup"><span data-stu-id="f081b-160">No updates</span></span> |

## <a name="communications"></a><span data-ttu-id="f081b-161">المراسلات</span><span class="sxs-lookup"><span data-stu-id="f081b-161">Communications</span></span>

<span data-ttu-id="f081b-162">يُمكنك معرفة ما هو الموجود في الأعمال الخاصة بـ Human Resources وما قمنا بإصداره في المواقع التالية:</span><span class="sxs-lookup"><span data-stu-id="f081b-162">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="f081b-163">مخطط Dynamics 365 Human Resources </span><span class="sxs-lookup"><span data-stu-id="f081b-163">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/talent/)

- [<span data-ttu-id="f081b-164">خطط إصدار Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="f081b-164">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="f081b-165">ما الجديد أو المتغير‬ في Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="f081b-165">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="f081b-166">[البحث عن المشاكل في Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (لإصلاح الأخطاء المتعلقة بالنظام الأساسي فقط)</span><span class="sxs-lookup"><span data-stu-id="f081b-166">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="f081b-167">مدونة Human Resources</span><span class="sxs-lookup"><span data-stu-id="f081b-167">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="f081b-168">مجتمع Human Resources Yammer</span><span class="sxs-lookup"><span data-stu-id="f081b-168">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="f081b-169">ميزات المعاينة في بيئة الحماية</span><span class="sxs-lookup"><span data-stu-id="f081b-169">Preview features in a sandbox environment</span></span>

<span data-ttu-id="f081b-170">يُمكنك التحقق من صحة ميزات المعاينة في بيئة الحماية قبل تمكينها في بيئة الإنتاج الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="f081b-170">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="f081b-171">لمزيد من المعلومات حول تمكين الميزات، راجع [نظرة عامة على إدارة الميزات](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="f081b-171">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="f081b-172">تبقي كافة الميزات الجديدة في معاينه لمده 30 يوما علي الأقل ، وبشكل نموذجي 30-60 يوما.</span><span class="sxs-lookup"><span data-stu-id="f081b-172">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="f081b-173">تتوفر الميزات الرئيسية بشكل عام في أكتوبر و ابريل من كل عام يتبع فتره المعاينة.</span><span class="sxs-lookup"><span data-stu-id="f081b-173">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="f081b-174">بمجرد ان تشاهد إمكانيات جديده في مساحة عمل إدارة الميزات، يمكنك تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="f081b-174">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="f081b-175">قد تكون بعض الميزات قيد التشغيل بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="f081b-175">Some features may be on by default.</span></span>

<span data-ttu-id="f081b-176">في بعض الأوقات، سيتم تشغيل ميزه متكاملة بشكل افتراضي ولا يمكن إيقاف تشغيلها (على سبيل المثال مساحة عمل إدارة الميزات).</span><span class="sxs-lookup"><span data-stu-id="f081b-176">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="f081b-177">وبمجرد توفر إحدى الميزات بصفه عامه ، قد يتم تشغيلها أو إيقاف تشغيلها في بيئات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f081b-177">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="f081b-178">وتشير مساحة عمل إدارة الميزات إلى ان ميزه المعاينة ستصبح إلزاميه.</span><span class="sxs-lookup"><span data-stu-id="f081b-178">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="f081b-179">وعاده ما يكون هذا التاريخ في يوم 1 أكتوبر أو 1 إبريل لكي تتم محاذاته مع خطط الإصدار نصف السنوية.</span><span class="sxs-lookup"><span data-stu-id="f081b-179">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="f081b-180">لا يمكنك إيقاف تشغيل الميزات الإلزامية.</span><span class="sxs-lookup"><span data-stu-id="f081b-180">You can't turn off mandatory features.</span></span> <span data-ttu-id="f081b-181">وحتى تصبح إلزاميا، يمكنك تشغيل أحدي الميزات وإيقاف تشغيلها في كافة البيئات.</span><span class="sxs-lookup"><span data-stu-id="f081b-181">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="f081b-182">نوصي بشدة بمعاينة الميزات في بيئة الحماية أو البيئة التجريبية.</span><span class="sxs-lookup"><span data-stu-id="f081b-182">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="f081b-183">من الأفضل إنشاء نسخة من بيئة الإنتاج الحالية أو قاعدة البيانات في بيئة الحماية بحيث يمكنك الحصول على التجربة الكاملة للميزات الجديدة مع الميزات الجديدة مع البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="f081b-183">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="f081b-184">لمزيد من المعلومات حول توفير بيئة حماية، راجع [توفير مشروع Human Resources](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="f081b-184">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="f081b-185">لإزالة بيئة اختبار، راجع [إزالة مثيل](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="f081b-185">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="f081b-186">الإبلاغ عن الأخطاء</span><span class="sxs-lookup"><span data-stu-id="f081b-186">Report bugs</span></span>

<span data-ttu-id="f081b-187">أثناء اختبار ميزات المعاينة أو تجربة إمكانيات جديدة، قد تجد عناصر لا تعمل بالشكل المتوقع.</span><span class="sxs-lookup"><span data-stu-id="f081b-187">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="f081b-188">يُرجى الإبلاغ عن أي أخطاء من خلال [دعم Microsoft Dynamics 365](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="f081b-188">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="f081b-189">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="f081b-189">See also</span></span>

- [<span data-ttu-id="f081b-190">خطط إصدار Dynamics 365 و Power Platform</span><span class="sxs-lookup"><span data-stu-id="f081b-190">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)
- [<span data-ttu-id="f081b-191">ما هو الجديد أو المتغير في Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="f081b-191">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="f081b-192">سياسة دورة حياة البرامج</span><span class="sxs-lookup"><span data-stu-id="f081b-192">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

