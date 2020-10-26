---
title: تشغيل تجربة ومراقبتها
description: يصف هذا الموضوع كيفيه تشغيل ومراقبه تجربه في خدمه جهة خارجيه. كما يوضح كيفيه اجراء تغييرات علي التباينات بعد بدء التجربة.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4cb7d863d9d69612aa0c340099c1f7861c9d12ba
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930131"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="b89f3-104">تشغيل تجربة ومراقبتها</span><span class="sxs-lookup"><span data-stu-id="b89f3-104">Run and monitor an experiment</span></span>

<span data-ttu-id="b89f3-105">يصف هذا الموضوع كيفيه تشغيل ومراقبه التجربة الخاصة بأحد التطبيقات التابعة لجهة خارجيه، وتغيير الاختلافات إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="b89f3-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="b89f3-106">قبل إكمال الخطوات الواردة في هذا الموضوع، ستحتاج إلى [نشر ](experimentation-preview-publish.md)التجربة الخاصة بك في التجارة.</span><span class="sxs-lookup"><span data-stu-id="b89f3-106">Before you complete the steps in this topic, you'll need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> <span data-ttu-id="b89f3-107">يوضح الرسم التخطيطي التالي كافة الخطوات المتضمنة في اعداد وتشغيل تجربه علي أحد مواقع التجارة الالكترونيه في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b89f3-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="b89f3-108">وتتم تغطيه الخطوات الاضافيه في موضوعات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="b89f3-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="b89f3-109">[![رحلة مستخدم التجربة - التشغيل والمراقبة](./media/experimentation_run_monitor.svg)](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="b89f3-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="b89f3-110">بعد نشر الاختلافات الخاصة بك، يتم القيام بكل الخطوات التي تحتاجها للقيام بها في التجارة لتشغيل التجربة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="b89f3-110">After you publish your variations, all the steps you need to do in Commerce to run your experiment are done.</span></span> <span data-ttu-id="b89f3-111">الخطوة التالية تحدد اي تباين سيتم إظهاره لكل مستخدم عند طلب الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b89f3-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="b89f3-112">تقوم الخدمة التابعة لجهة أخرى باجراء التحديد، ولكن أولا يجب عليك تنشيط التجربة داخل الخدمة.</span><span class="sxs-lookup"><span data-stu-id="b89f3-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="b89f3-113">ونظرا لان خطوات تنشيط التجربة تختلف عن الخدمة إلى الخدمة، ستحتاج إلى اتباع الإرشادات الموجودة في الخدمة أو الموفر.</span><span class="sxs-lookup"><span data-stu-id="b89f3-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="b89f3-114">إذا لم يتم تنشيط التجربة، سيري المستخدمون فقط الإصدار الافتراضي من الصفحة -لن يتم عرض إيه تباينات.</span><span class="sxs-lookup"><span data-stu-id="b89f3-114">If the experiment is not activated, users will only see the default version of the page - no variations will be displayed.</span></span>

<span data-ttu-id="b89f3-115">يجب عليك الحفاظ علي ان التجربة يعمل بفترة كافيه لجمع البيانات للحصول على نتائج إحصائية صالحه.</span><span class="sxs-lookup"><span data-stu-id="b89f3-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="b89f3-116">استخدم خدمه الجهة الخارجية لمراقبه البيانات المتعلقة بالتجربة والتحليلات اثناء تشغيل التجربة.</span><span class="sxs-lookup"><span data-stu-id="b89f3-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="b89f3-117">ضبط التباينات</span><span class="sxs-lookup"><span data-stu-id="b89f3-117">Adjust your variations</span></span>
<span data-ttu-id="b89f3-118">إذا كنت تحتاج إلى تعديل الاختلافات لأي سبب، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b89f3-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b89f3-119">إذا قمت باجراء تغييرات علي تجربه مباشره في التجارة أو في خدمه الجهة الخارجية، فقد تتاثر النتائج بشكل ملحوظ.</span><span class="sxs-lookup"><span data-stu-id="b89f3-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="b89f3-120">خذ بعين الاعتبار السماح للتجربة بتشغيل الدورة التدريبية الخاصة بها ثم إنشاء تجربه جديده للتغييرات الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="b89f3-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="b89f3-121">انتقل إلى علامة التبويب **التجارب** في منشئ الموقع وحدد التجربة.</span><span class="sxs-lookup"><span data-stu-id="b89f3-121">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
1. <span data-ttu-id="b89f3-122">حدد التباين الذي تريد تحديثه من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="b89f3-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="b89f3-123">قم باجراء التغييرات المطلوبة ، ثم قم بمعاينه التباينات ونشرها.</span><span class="sxs-lookup"><span data-stu-id="b89f3-123">Make needed changes, then preview and publish the variations.</span></span> <span data-ttu-id="b89f3-124">لمزيد من المعلومات ، راجع [معاينة ونشر التجربة](experimentation-preview-publish.md).</span><span class="sxs-lookup"><span data-stu-id="b89f3-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="b89f3-125">انتقل إلى خدمه الجهة الخارجية لاجراء إيه تغييرات تتعلق بالاعداد بتجربة.</span><span class="sxs-lookup"><span data-stu-id="b89f3-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="b89f3-126">الخطوة السابقة</span><span class="sxs-lookup"><span data-stu-id="b89f3-126">Previous step</span></span>
[<span data-ttu-id="b89f3-127">معاينه التجربة ونشرها</span><span class="sxs-lookup"><span data-stu-id="b89f3-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="b89f3-128">الخطوة التالية</span><span class="sxs-lookup"><span data-stu-id="b89f3-128">Next step</span></span>
[<span data-ttu-id="b89f3-129">ترقية التباين وإكمال تجربة</span><span class="sxs-lookup"><span data-stu-id="b89f3-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)
