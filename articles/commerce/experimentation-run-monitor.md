---
title: تشغيل تجربة ومراقبتها
description: يصف هذا الموضوع كيفيه تشغيل ومراقبه تجربه في خدمه جهة خارجيه. كما يوضح كيفيه اجراء تغييرات علي التباينات بعد بدء التجربة.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4afc19ed103f204fec61ab20b88f767ad5f05b38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792525"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="be458-104">تشغيل تجربة ومراقبتها</span><span class="sxs-lookup"><span data-stu-id="be458-104">Run and monitor an experiment</span></span>

<span data-ttu-id="be458-105">يصف هذا الموضوع كيفيه تشغيل ومراقبه التجربة الخاصة بأحد التطبيقات التابعة لجهة خارجيه، وتغيير الاختلافات إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="be458-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="be458-106">قبل إكمال الخطوات الواردة في هذا الموضوع، ستحتاج أولاً إلى [نشر ](experimentation-preview-publish.md) التجربة الخاصة بك في Commerce.</span><span class="sxs-lookup"><span data-stu-id="be458-106">Before you complete the steps in this topic, you'll first need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> 

<span data-ttu-id="be458-107">يوضح الرسم التخطيطي التالي كافة الخطوات المتضمنة في اعداد وتشغيل تجربه علي أحد مواقع التجارة الالكترونيه في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="be458-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="be458-108">وتتم تغطيه الخطوات الاضافيه في موضوعات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="be458-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="be458-109">[![رحلة مستخدم التجربة - التشغيل والمراقبة](./media/experimentation_run_monitor.svg)](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="be458-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="be458-110">بعد نشر التباينات الخاصة بك، يتم إكمال كل الخطوات التي تحتاجها للقيام بها في Commerce لتشغيل التجربة الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="be458-110">After you publish your variations, all of the steps you need to do in Commerce to run your experiment are complete.</span></span> <span data-ttu-id="be458-111">الخطوة التالية تحدد اي تباين سيتم إظهاره لكل مستخدم عند طلب الصفحة.</span><span class="sxs-lookup"><span data-stu-id="be458-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="be458-112">تقوم الخدمة التابعة لجهة أخرى باجراء التحديد، ولكن أولا يجب عليك تنشيط التجربة داخل الخدمة.</span><span class="sxs-lookup"><span data-stu-id="be458-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="be458-113">ونظرا لان خطوات تنشيط التجربة تختلف عن الخدمة إلى الخدمة، ستحتاج إلى اتباع الإرشادات الموجودة في الخدمة أو الموفر.</span><span class="sxs-lookup"><span data-stu-id="be458-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="be458-114">إذا لم يتم تنشيط التجربة، سيري المستخدمون فقط الإصدار الافتراضي من الصفحة (لن يتم عرض أية تباينات).</span><span class="sxs-lookup"><span data-stu-id="be458-114">If the experiment is not activated, users will only see the default version of the page (no variations will be displayed).</span></span>

<span data-ttu-id="be458-115">يجب عليك الحفاظ علي ان التجربة يعمل بفترة كافيه لجمع البيانات للحصول على نتائج إحصائية صالحه.</span><span class="sxs-lookup"><span data-stu-id="be458-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="be458-116">استخدم خدمه الجهة الخارجية لمراقبه البيانات المتعلقة بالتجربة والتحليلات اثناء تشغيل التجربة.</span><span class="sxs-lookup"><span data-stu-id="be458-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="be458-117">ضبط التباينات</span><span class="sxs-lookup"><span data-stu-id="be458-117">Adjust your variations</span></span>
<span data-ttu-id="be458-118">إذا كنت تحتاج إلى تعديل الاختلافات لأي سبب، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="be458-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be458-119">إذا قمت باجراء تغييرات علي تجربه مباشره في التجارة أو في خدمه الجهة الخارجية، فقد تتاثر النتائج بشكل ملحوظ.</span><span class="sxs-lookup"><span data-stu-id="be458-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="be458-120">خذ بعين الاعتبار السماح للتجربة بتشغيل الدورة التدريبية الخاصة بها ثم إنشاء تجربه جديده للتغييرات الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="be458-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="be458-121">في منشئ موقع Commerce، حدد **التجارب** في جزء التنقل الأيسر، ثم حدد التجربة.</span><span class="sxs-lookup"><span data-stu-id="be458-121">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
1. <span data-ttu-id="be458-122">حدد التباين الذي تريد تحديثه من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="be458-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="be458-123">قم بإجراء أية تغييرات المطلوبة، ثم قم بمعاينة التباينات ونشرها.</span><span class="sxs-lookup"><span data-stu-id="be458-123">Make any needed changes, and then preview and publish the variations.</span></span> <span data-ttu-id="be458-124">لمزيد من المعلومات ، راجع [معاينة ونشر التجربة](experimentation-preview-publish.md).</span><span class="sxs-lookup"><span data-stu-id="be458-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="be458-125">انتقل إلى خدمه الجهة الخارجية لاجراء إيه تغييرات تتعلق بالاعداد بتجربة.</span><span class="sxs-lookup"><span data-stu-id="be458-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="be458-126">الخطوة السابقة</span><span class="sxs-lookup"><span data-stu-id="be458-126">Previous step</span></span>
[<span data-ttu-id="be458-127">معاينه التجربة ونشرها</span><span class="sxs-lookup"><span data-stu-id="be458-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="be458-128">الخطوة التالية</span><span class="sxs-lookup"><span data-stu-id="be458-128">Next step</span></span>
[<span data-ttu-id="be458-129">ترقية التباين وإكمال تجربة</span><span class="sxs-lookup"><span data-stu-id="be458-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]