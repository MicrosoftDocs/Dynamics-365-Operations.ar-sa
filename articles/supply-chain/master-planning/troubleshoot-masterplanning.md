---
title: استكشاف أخطاء وظيفة التخطيط الرئيسي وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع التخطيط الرئيسي.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 44291f5bcd9ffedf717150f8efe32e9eeda02f2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011337"
---
# <a name="troubleshoot-master-planning"></a><span data-ttu-id="f7b9e-103">استكشاف أخطاء وظيفة التخطيط الرئيسي وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="f7b9e-103">Troubleshoot master planning</span></span>

<span data-ttu-id="f7b9e-104">يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-104">This topic describes how to fix issues that you might encounter while you work with master planning.</span></span>

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a><span data-ttu-id="f7b9e-105">يعمل تحديد إجمالي قائمه مكونات الصنف بشكل مختلف لأوامر الإنتاج المؤكدة ولأوامر الإنتاج المقدرة للعمل الذي تم إنشاؤه يدويا.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-105">Bill of materials explosion behaves differently for firmed production orders and for estimated production orders for manually created work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f7b9e-106">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="f7b9e-106">Issue description</span></span>

<span data-ttu-id="f7b9e-107">عند تاكيد أمر الإنتاج ، لن تكون الأصناف مجزاه عند تحديد قائمة مكونات الصنف (BOM).</span><span class="sxs-lookup"><span data-stu-id="f7b9e-107">When a production order is firmed, the items aren't exploded when you explode the bill of materials (BOM).</span></span> <span data-ttu-id="f7b9e-108">ومع ذلك ، عند إنشاء أمر العمل يدويا ، ثم تقدير أمر الإنتاج ، يتم التعامل مع الأصناف.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-108">However, when you manually create a work order and then estimate the production order, the items are exploded.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f7b9e-109">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="f7b9e-109">Issue resolution</span></span>

<span data-ttu-id="f7b9e-110">النظام يعمل كما هو متوقع.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-110">The system is working as expected.</span></span> <span data-ttu-id="f7b9e-111">ستشير عمليات التحديد التي تحدث عند تاكيد أمر الإنتاج إلى الأمر المخطط ، ولكنه لا يبدو ان الأمر المخطط مؤكد حاليا في هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-111">The explosion that occurs when the production order is firmed will point to the planned order, but it doesn't appear that the planned order is currently firmed in this case.</span></span> <span data-ttu-id="f7b9e-112">ومع ذلك ، إذا تم تقدير أمر الإنتاج ، يتم تشغيل عمليه تحديد إجمالي المكونات المطلوبة من أمر الإنتاج الذي تم إصداره في حاله عدم وجود أمر مخطط.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-112">However, if the production order has been estimated, the explosion is triggered from the released production order where no planned order exists.</span></span>

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a><span data-ttu-id="f7b9e-113">لا يتم تحديث قيمه التاخير عند أعاده جدوله أمر مخطط.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-113">The Delay value isn't updated when I reschedule a planned order.</span></span>

<span data-ttu-id="f7b9e-114">لتحديث تاخير الأوامر المخططة ، افتح مربع الحوار **أعاده الجدولة** للأمر المخطط.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-114">To update the delay for planned orders, open the **Rescheduling** dialog box for the planned order.</span></span> <span data-ttu-id="f7b9e-115">في علامة التبويب السريعة **تقسيم**، تأكد من تعيين الخيار **إجراء التقسيم بعد إعادة الجدولة** على القيمة *نعم*.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-115">On the **Explosion** FastTab, make sure that the **Perform explosion after rescheduling** option is set to *Yes*.</span></span>

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a><span data-ttu-id="f7b9e-116">لا تعد جدوله الإنتاج بعين الاعتبار حدود الأمان التي تم تعيينها في تغطيه الصنف لتوريد مثبت.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-116">Production scheduling doesn't consider the safety margins that are set on the item coverage for pegged supply.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f7b9e-117">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="f7b9e-117">Issue description</span></span>

<span data-ttu-id="f7b9e-118">يعتبر التخطيط الرئيسي بالمثل حدود الأمان.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-118">Master planning considers the safety margins.</span></span> <span data-ttu-id="f7b9e-119">ومع ذلك ، يتم تجاهل حدود الأمان عندما تتم جدوله أوامر الإنتاج المخططة.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-119">However, the safety margins are ignored when planned production orders are scheduled.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f7b9e-120">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="f7b9e-120">Issue resolution</span></span>

<span data-ttu-id="f7b9e-121">يتم التعامل مع الهوامش فقط اثناء التخطيط الرئيسي ، وليس اثناء الجدولة اليدوية.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-121">Margins are considered only during master planning, not during manual scheduling.</span></span> <span data-ttu-id="f7b9e-122">يتم تصميم الهوامش لتعمل كمخزن مؤقت اثناء مرحله التخطيط ، وذلك لإعطاء بعض "الهوامش" للعملية الفعلية.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-122">Margins are designed to act as a buffer during the planning phase, to give some "margin" for the actual process.</span></span>

<span data-ttu-id="f7b9e-123">للحصول علي النتيجة المطلوبة ، يمكنك أزاله الهامش.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-123">To get the desired result, you can remove the margin.</span></span> <span data-ttu-id="f7b9e-124">ويجب بعد ذلك تحديث المسار حتى يتضمن الوقت المرغوب فيه (علي سبيل المثال ، وقت قائمه الانتظار).</span><span class="sxs-lookup"><span data-stu-id="f7b9e-124">The route must then be updated so that it includes the desired time (for example, as queue time).</span></span> <span data-ttu-id="f7b9e-125">يجب ان ينتج عن كل من التخطيط الرئيسي والجدولة اليدوية بعد ذلك النتيجة.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-125">Both master planning and manual scheduling should then produce the same result.</span></span>

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a><span data-ttu-id="f7b9e-126">ويتم إنشاء الأوامر المخططة علي الرغم من وجود أصناف في أوامر المخزون والإنتاج موجودة بالفعل لها.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-126">Planned orders are generated even though we have items in stock and production orders already exist for them.</span></span>

<span data-ttu-id="f7b9e-127">قد تتمكن من حل هذه المشكلة عن طريق زيادة قيمه **الأيام الموجبة** للمجموعات ذات الصلة في صفحه **مجموعه التغطية**.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-127">You might be able to fix this issue by increasing the **Positive days** value for the relevant groups on the **Coverage group** page.</span></span> <span data-ttu-id="f7b9e-128">سيؤدي هذا التغيير إلى تحديد ما إذا كان من الممكن استخدام المخزون الفعلي للطلب ام لا.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-128">This change will cause the system to determine whether on-hand inventory can be used for the demand.</span></span> <span data-ttu-id="f7b9e-129">وبعد ذلك لن يتم إنشاء أمر مخطط جديد للأصناف الموجودة بالمخزن.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-129">Then a new planned order won't be generated for the items that are in stock.</span></span>

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a><span data-ttu-id="f7b9e-130">يبدو ان التخطيط الرئيسي لا يتعلق بقيود القدرة ويقوم بجدوله أكبر من القدرة المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-130">Master planning doesn't seem to respect capacity limitations and is scheduling more than the available capacity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f7b9e-131">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="f7b9e-131">Issue description</span></span>

<span data-ttu-id="f7b9e-132">عند استخدام جدوله العمليات حيث توجد قدره محدوده ، وعندما يحدد المسار مزيجا من المتطلبات لكل من مجموعه الموارد والموارد الفردية ، فهناك فرصه صغيره من عمليات الحجز الزائدة بسبب الطريقة التي تقوم بها الخوارزميه بالتحقق من وجود تعارضات في القدرة.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-132">When you use operation scheduling where there is finite capacity, and where the route specifies a mix of requirements for both a resource group and individual resources, there is a small chance of overbooking because of the way that the algorithm validates for capacity conflicts.</span></span> <span data-ttu-id="f7b9e-133">يمكن ان يحدث هذا الحجز الزائد عند استخدام المساعدين لتشغيل التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-133">This overbooking can occur when you use helpers to run master planning.</span></span> <span data-ttu-id="f7b9e-134">من المحتمل ان يحدث ذلك في حاله وجود العديد من المهام التي لها وقت تشغيل قصير نسبيا.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-134">It's most likely to occur if there are many jobs that have a relatively short runtime.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f7b9e-135">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="f7b9e-135">Issue resolution</span></span>

<span data-ttu-id="f7b9e-136">إذا كان من الضروري عدم حدوث حجز زائد لجدوله العمليات ، فيمكنك جعل جزء الجدولة جزءا من مؤشر الترابط الرئيسي في التخطيط الرئيسي وذلك بتشغيل خيار **جدوله العمليات المحدودة الدقيق** علي **صفحه معلمات التخطيط الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-136">If it's essential that no overbooking occur for operation scheduling, you can make the scheduling part of master planning single-threaded by turning on the **Accurate finite capacity for Operation Scheduling** option on the **Master planning parameters** page.</span></span> <span data-ttu-id="f7b9e-137">هذا الخيار غير متوفر بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-137">This option isn't available by default.</span></span> <span data-ttu-id="f7b9e-138">يجب اضافته يدويا إلى الصفحة باستخدام ميزات التخصيص.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-138">You must manually add it to the page by using personalization features.</span></span> <span data-ttu-id="f7b9e-139">عند استخدام هذا الخيار ، ستعمل الجدولة ببطء بسبب نقص المعالجة المتوازية.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-139">When you use this option, scheduling will run more slowly because of the lack of parallel processing.</span></span>

## <a name="planned-orders-take-a-long-time-to-update"></a><span data-ttu-id="f7b9e-140">ويستغرق تحديث الأوامر المخططة وقتا طويلا للتحديث.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-140">Planned orders take a long time to update.</span></span>

### <a name="issue-description"></a><span data-ttu-id="f7b9e-141">وصف المشكلة</span><span class="sxs-lookup"><span data-stu-id="f7b9e-141">Issue description</span></span>

<span data-ttu-id="f7b9e-142">عند تحديث كميه الطلب و/أو تاريخ التسليم في أمر مخطط ، فانه عاده ما يستغرق 30 ثانيه علي الأقل لحفظ التحديث.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-142">When updating the requirement quantity and/or delivery date on a planned order, it typically takes at least 30 seconds per order to save the update.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f7b9e-143">حل المشكلة</span><span class="sxs-lookup"><span data-stu-id="f7b9e-143">Issue resolution</span></span>

<span data-ttu-id="f7b9e-144">هذه مشكله معروفه في مشغل التخطيط الرئيسي المضمن.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-144">This is a known issue with the built-in master planning engine.</span></span> <span data-ttu-id="f7b9e-145">ويرجع السبب في ذلك إلى ان التصنيف التلقائي الأساسي خلال بنيه قائمة مكونات الصنف اثناء عمليات التحرير.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-145">It is caused by the underlying auto explosion through the BOM structure during edits.</span></span> <span data-ttu-id="f7b9e-146">يتم التعامل مع هذه المشكلة في تحسين التخطيط ، حيث يمكن للمخطِط تحديث الأوامر ذات الصلة واعتمادها ، وعند الرغبة ، تشغيل تخطيط لتشغيل لتحديث الأوامر المخططة الخاصة ببنيه قائمة مكونات الصنف الاساسيه.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-146">This issue is addressed in Planning Optimization, where a planner can update and approve the relevant orders and, when desired, trigger a planning run to update planned orders for the underlying BOM structure.</span></span>

<span data-ttu-id="f7b9e-147">والطريقة الوحيدة لتحسين الأداء باستخدام مشغل التخطيط الرئيسي المضمن هي القيام بما يلي:</span><span class="sxs-lookup"><span data-stu-id="f7b9e-147">One way to improve performance with the built-in master planning engine is to do the following:</span></span>

1. <span data-ttu-id="f7b9e-148">انتقل إلى **التخطيط الرئيسي \> الإعداد \> الخطط \> الخطط الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-148">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="f7b9e-149">حدد خطة.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-149">Select a plan.</span></span>
1. <span data-ttu-id="f7b9e-150">قم بتوسيع علامة التبويب السريعة **الحدود الزمنية بالأيام**.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-150">Expand the **Time fence in days** FastTab.</span></span>
1. <span data-ttu-id="f7b9e-151">قم بتعيين **تقسيم** إلى *نعم*، وقم بتعيين الحقل أسفل هذا الاعداد إلى 0 (صفر).</span><span class="sxs-lookup"><span data-stu-id="f7b9e-151">Set **Explosion** to *Yes*, and set the field below this setting to 0 (zero).</span></span>

> [!NOTE]
> <span data-ttu-id="f7b9e-152">سيؤدي ذلك إلى الحد من الفترة لنظر المنجزة لهذه الخطة الرئيسية إلى يوم واحد.</span><span class="sxs-lookup"><span data-stu-id="f7b9e-152">This will limit the period for explosions performed for this master plan to a single day.</span></span>
