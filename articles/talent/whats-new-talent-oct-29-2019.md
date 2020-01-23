---
title: ما الجديد أو المتغير في Dynamics 365 Talent‏ (29 أكتوبر 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e2d79ee9e182df4a4efe65beb685567b1e7446ce
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897432"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a><span data-ttu-id="19cdf-103">ما الجديد أو المتغير في Dynamics 365 Talent‏ (29 أكتوبر 2019)</span><span class="sxs-lookup"><span data-stu-id="19cdf-103">What's new or changed in Dynamics 365 Talent (October 29, 2019)</span></span>

<span data-ttu-id="19cdf-104">يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="19cdf-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="19cdf-105">التغييرات في Attract</span><span class="sxs-lookup"><span data-stu-id="19cdf-105">Changes in Attract</span></span>

<span data-ttu-id="19cdf-106">يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="19cdf-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="19cdf-107">التغييرات في Onboard</span><span class="sxs-lookup"><span data-stu-id="19cdf-107">Changes in Onboard</span></span>

<span data-ttu-id="19cdf-108">يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="19cdf-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="19cdf-109">التغييرات في Core HR</span><span class="sxs-lookup"><span data-stu-id="19cdf-109">Changes in Core HR</span></span>

<span data-ttu-id="19cdf-110">تنطبق التغييرات التي ورد وصفها في هذا القسم على الإصدار رقم 8.1.2586.</span><span class="sxs-lookup"><span data-stu-id="19cdf-110">Changes described in this section apply to build number 8.1.2586.</span></span> <span data-ttu-id="19cdf-111">تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام الدعم في Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="19cdf-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a><span data-ttu-id="19cdf-112">يجب أن يتم حذف الأطراف التي ليس لها أدوار افتراضيًا (371233)</span><span class="sxs-lookup"><span data-stu-id="19cdf-112">Delete parties with no roles should be on by default (371233)</span></span>

<span data-ttu-id="19cdf-113">عند توفير بيئة جديده في Talent، **احذف الأطراف في حاله عدم وجود أي أدوار** قيد التشغيل افتراضيا.</span><span class="sxs-lookup"><span data-stu-id="19cdf-113">When you provision a new environment in Talent, **Delete parties if no roles exist** is turned on by default.</span></span> <span data-ttu-id="19cdf-114">عندما تقوم بحذف عامل ، لا تتم أزاله الطرف المقترن بالعامل ما لم يكن هذا الاعداد قيد التشغيل.</span><span class="sxs-lookup"><span data-stu-id="19cdf-114">When you delete a worker, the party associated with the worker is not removed unless this setting is on.</span></span> <span data-ttu-id="19cdf-115">يحد هذا التغيير من السجلات المكررة في دفتر العناوين العام عندما تحتاج إلى استيراد العمال أو تغييرهم أو إعادة استيرادهم.</span><span class="sxs-lookup"><span data-stu-id="19cdf-115">This change limits duplicate records in the global address book when you need to import, change, or reimport workers.</span></span>

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a><span data-ttu-id="19cdf-116">يجب السماح بحذف طلبات المسودة وطلبات المغادرة الملغية في Common Data Service (376999)</span><span class="sxs-lookup"><span data-stu-id="19cdf-116">Draft and cancelled leave requests should be allowed to be deleted in Common Data Service (376999)</span></span>

<span data-ttu-id="19cdf-117">بهذا التغيير، يمكنك الآن حذف طلبات الاجازه التي بحالة **مسودة** أو **تم الإلغاء** في Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="19cdf-117">With this change, you can now delete leave requests with a status of **Draft** or **Cancelled** in Common Data Service.</span></span>

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a><span data-ttu-id="19cdf-118">لا تنعكس قيم القائمة الاضافيه في الحقول المخصصة في Common Data Service بعد النقر فوق تطبيق على نموذج الحقول المخصصة (379599)</span><span class="sxs-lookup"><span data-stu-id="19cdf-118">Additional list values in custom fields aren't reflected in Common Data Service after clicking Apply on the Custom fields form (379599)</span></span>

<span data-ttu-id="19cdf-119">عند أضافه قيم قائمه جديده إلى حقل مخصص موجود تمت مزامنته بالفعل مع Common Data Service، تكون الآن متاحه في Common Data Serivce بعد تطبيق تغييراتك في نموذج **الحقول المخصصة**.</span><span class="sxs-lookup"><span data-stu-id="19cdf-119">When you add new list values to an existing custom field that has already synchronized with Common Data Service, they're now available in Common Data Serivce after you apply your changes in the **Custom fields** form.</span></span>

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a><span data-ttu-id="19cdf-120">تطبيق قوائم الاختيار الخاصة بإلحاق عبر الكيانات القانونية عندما يوجد أكثر من توظيف واحد (371270)</span><span class="sxs-lookup"><span data-stu-id="19cdf-120">Apply onboarding checklists across legal entities when more than one employment exists (371270)</span></span>

<span data-ttu-id="19cdf-121">في الإصدار الخاص بهذا الأسبوع، يمكنك تطبيق قوائم الاختيار للموظفين الذين لديهم أكثر من توظيف واحد في **نموذج العامل > قوائم الاختيار**.</span><span class="sxs-lookup"><span data-stu-id="19cdf-121">In this week's release, you can apply checklists to employees with more than one employment in **Worker form > Checklists**.</span></span>

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a><span data-ttu-id="19cdf-122">تمت إزالة الميزات التي تفتح ميزة معاينة التسجيل</span><span class="sxs-lookup"><span data-stu-id="19cdf-122">Benefits open enrollment preview feature has been removed</span></span>

<span data-ttu-id="19cdf-123">بالتزامن مع إعلاننا الخاص [بالاستثمارات الاستراتيجية المنشور في مدونة التفوق العملي لتحسين core HR](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence)، عملت Microsoft على إزالة الميزات التي تفتح ميزة التسجيل المعاينة العامة.</span><span class="sxs-lookup"><span data-stu-id="19cdf-123">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog post, Microsoft has removed the benefits open enrollment feature from public preview.</span></span> <span data-ttu-id="19cdf-124">سيتم إصدار وظيفة جديدة في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="19cdf-124">New functionality will be released in the future.</span></span> <span data-ttu-id="19cdf-125">استخدام الإنتاج للميزات التي تفتح ميزة التسجيل غير مدعوم</span><span class="sxs-lookup"><span data-stu-id="19cdf-125">Production use of the benefits open enrollment feature isn't be supported.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="19cdf-126">قريبًا</span><span class="sxs-lookup"><span data-stu-id="19cdf-126">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="19cdf-127">طباعة مراجعات الأداء</span><span class="sxs-lookup"><span data-stu-id="19cdf-127">Print performance reviews</span></span>

<span data-ttu-id="19cdf-128">راجع [‏‫طباعة مراجعات الأداء‬](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) في خطة الموجة 2 من إصدار Dynamics 365: 2019.</span><span class="sxs-lookup"><span data-stu-id="19cdf-128">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="19cdf-129">مساحة عمل إدارة الميزات</span><span class="sxs-lookup"><span data-stu-id="19cdf-129">Feature management workspace</span></span>

<span data-ttu-id="19cdf-130">تتم إضافة ميزات وتحديثها في كل إصدار.</span><span class="sxs-lookup"><span data-stu-id="19cdf-130">Features are added and updated in every release.</span></span> <span data-ttu-id="19cdf-131">وتوفر تجربة إدارة الميزات مساحة عمل حيث يمكنك عرض قائمه بالميزات التي تم تقديمها في كل إصدار.</span><span class="sxs-lookup"><span data-stu-id="19cdf-131">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="19cdf-132">بشكل افتراضي، تكون الميزات الجديدة متوقفة عن التشغيل.</span><span class="sxs-lookup"><span data-stu-id="19cdf-132">By default, new features are turned off.</span></span> <span data-ttu-id="19cdf-133">ويمكنك استخدام مساحة العمل لتشغيلها وعرض الوثائق الخاصة بها.</span><span class="sxs-lookup"><span data-stu-id="19cdf-133">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="19cdf-134">لمعرفة المزيد حول التغييرات المصاحبة لإدارة الميزات، راجع [نظرة على إدارة الميزات‬](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="19cdf-134">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
