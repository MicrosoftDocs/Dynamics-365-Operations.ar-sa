---
title: استراتيجيات التزويد
description: يوفر هذا الموضوع معلومات حول استراتيجيات التزويد ويشرح كيفيه استخدام حقل استراتيجية التزويد في بنود قالب التزويد المطالبة بالموجه لتحديد كيفيه اجراء التزويد.
author: mirzaab
manager: tfehr
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 9c23126c6ab15a1924b34f98d33a0661011ba8bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996088"
---
# <a name="replenishment-strategies"></a><span data-ttu-id="78763-103">استراتيجيات التزويد</span><span class="sxs-lookup"><span data-stu-id="78763-103">Replenishment strategies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78763-104">تتضمن القوالب التي تم تعريفها في صفحه **قوالب التزويد** بنود قالب تزويد طلب الموجه التي تتيح لك تحديد كيفيه القيام بالتزويد.</span><span class="sxs-lookup"><span data-stu-id="78763-104">The templates that are defined on the **Replenishment templates** page include wave demand replenishment template lines that let you select how replenishment is done.</span></span> <span data-ttu-id="78763-105">يتضمن كل بند الآن حقل **استراتيجية التزويد**.</span><span class="sxs-lookup"><span data-stu-id="78763-105">Each line now includes a **Replenishment strategy** field.</span></span>

<span data-ttu-id="78763-106">وتعتبر استراتيجية *الكمية لطلب الموجه* هي الاستراتيجية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="78763-106">The *Wave demand quantity* strategy is the default strategy.</span></span> <span data-ttu-id="78763-107">انها استراتيجية التزويد التي تم استخدامها قبل مقدمه الحقل **استراتيجية التزويد**.</span><span class="sxs-lookup"><span data-stu-id="78763-107">It's the replenishment strategy that was used before the introduction of the **Replenishment strategy** field.</span></span> <span data-ttu-id="78763-108">ويستخدم توجيهات موقع التزويد للبحث عن مواقع يمكن تزويدها.</span><span class="sxs-lookup"><span data-stu-id="78763-108">It uses the replenishment location directives to find locations that can be replenished.</span></span> <span data-ttu-id="78763-109">ثم يتم تزويد هذه المواقع حتى تتم تغطيه الطلب.</span><span class="sxs-lookup"><span data-stu-id="78763-109">It then replenishes those locations until the demand is covered.</span></span>

<span data-ttu-id="78763-110">وتقدم استراتيجية *الحد الأقصى لقدرة الموقع* بعض الوظائف الجديدة.</span><span class="sxs-lookup"><span data-stu-id="78763-110">The *Maximum location capacity* strategy introduces some new functionality.</span></span> <span data-ttu-id="78763-111">ومثل استراتيجية *كمية طلب الموجة*، تستخدم هذه الاستراتيجية موجات مواقع التزويد للبحث عن مواقع يمكن تزويدها، ثم تزويد تلك المواقع إلى ان تتم تغطيه الطلب.</span><span class="sxs-lookup"><span data-stu-id="78763-111">Like the *Wave demand quantity* strategy, this strategy uses the replenishment location directives to find locations that can be replenished, and then it replenishes those locations until the demand is covered.</span></span> <span data-ttu-id="78763-112">يختلف ذلك عن استراتيجية *كميه طلب الموجه* وذلك بحيث يتم تزويد كافة المواقع التي تم تزويدها إلى الحد الأقصى للقدرة الخاصة بها ، كما هو محدد بواسطة حدود المخزون الخاصة بالموقع.</span><span class="sxs-lookup"><span data-stu-id="78763-112">It differs from the *Wave demand quantity* strategy in that all the replenished locations are replenished to their maximum capacity, as defined by the location stocking limits.</span></span> <span data-ttu-id="78763-113">تحاول استراتيجية *الحد الأقصى لقدرة الموقع* الذي يحاول إنشاء عمل لإحضار الكمية المطلوبة بالاضافه إلى الكمية الاضافيه لملء المواقع التي يتم تزويدها.</span><span class="sxs-lookup"><span data-stu-id="78763-113">The *Maximum location capacity* strategy tries to create work to bring in the requested quantity, plus some extra quantity, to fill the locations that are being replenished.</span></span> <span data-ttu-id="78763-114">ومع ذلك ، في بعض الحالات ، قد تفشل هذه المحاولة.</span><span class="sxs-lookup"><span data-stu-id="78763-114">However, in some cases, that attempt might fail.</span></span> <span data-ttu-id="78763-115">علي سبيل المثال ، قد لا يكون لدي مواقع الكميات الكبيرة مخزون كاف لتغطيه الكمية الاضافيه.</span><span class="sxs-lookup"><span data-stu-id="78763-115">For example, the bulk locations might not have enough inventory to cover the extra quantity.</span></span> <span data-ttu-id="78763-116">في هذه الحالات ، يكشف النظام عن الفشل ويحاول الاسترداد.</span><span class="sxs-lookup"><span data-stu-id="78763-116">In these cases, the system detects the failure and tries to recover.</span></span>

<span data-ttu-id="78763-117">يعد "موسم الذروة" مثالا علي الموقف الذي يفضل استراتيجية *الحد الأقصى للقدرة الانتاجيه للموقع* لاستراتيجية  *كميه طلب الموجه*.</span><span class="sxs-lookup"><span data-stu-id="78763-117">Peak season is one example of a situation where the *Maximum location capacity* strategy is preferable to the *Wave demand quantity* strategy.</span></span> <span data-ttu-id="78763-118">واثناء الموسم في الذروة ، قد يتم بيع بعض الأصناف بحجم كبير.</span><span class="sxs-lookup"><span data-stu-id="78763-118">During peak season, some items might be selling at high volume.</span></span> <span data-ttu-id="78763-119">ولذلك ، قد ترغب في القيام بتزويد مواقع الانتقاء ذات الصلة بالقدر المستطاع ، لتقليل عدد معرفات العمل التي تم إنشاؤها لتزويدها.</span><span class="sxs-lookup"><span data-stu-id="78763-119">Therefore, you might want to proactively replenish the relevant picking locations as much as possible, to reduce the number of work IDs that are created for replenishment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78763-120">للاستفادة الكاملة من استراتيجية *الحد الأقصى لقدرة الإنتاج الخاصة بالموقع*، يجب أعاده تعريف حدود المخزون الخاصة بالمواقع ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="78763-120">To take full advantage of the *Maximum location capacity* strategy, you must redefine the stocking limits for the relevant locations.</span></span> <span data-ttu-id="78763-121">وبخلاف ذلك ، تعمل هذه الاستراتيجية تماما مثل استراتيجية *الكمية الخاصة بطلب الموجه*.</span><span class="sxs-lookup"><span data-stu-id="78763-121">Otherwise, this strategy works just like the *Wave demand quantity* strategy.</span></span>

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a><span data-ttu-id="78763-122">تشغيل التزويد إلى الحد الأقصى استنادا إلى ميزه حدود المخزون</span><span class="sxs-lookup"><span data-stu-id="78763-122">Turn on the Replenish to max based on stocking limits feature</span></span>

<span data-ttu-id="78763-123">قبل أن تتمكن من استخدام هذه الميزة، يجب تشغيلها في النظام.</span><span class="sxs-lookup"><span data-stu-id="78763-123">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="78763-124">يمكن للمسؤولين استخدام إعدادات [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) للتحقق من حالة الميزة وتشغيلها إذا كانت مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="78763-124">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of this feature and turn it on if it's required.</span></span> <span data-ttu-id="78763-125">هناك، يتم إدراج الميزة بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="78763-125">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="78763-126">**الوحدة:** *إدارة المستودعات*</span><span class="sxs-lookup"><span data-stu-id="78763-126">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="78763-127">**اسم الميزة:** *تشغيل التزويد إلى الحد الأقصى استنادا إلى ميزه حدود المخزون*</span><span class="sxs-lookup"><span data-stu-id="78763-127">**Feature name:** *Replenish to max based on stocking limits*</span></span>

## <a name="set-up-replenishment-strategies"></a><span data-ttu-id="78763-128">إعداد استراتيجيات التزويد</span><span class="sxs-lookup"><span data-stu-id="78763-128">Set up replenishment strategies</span></span>

<span data-ttu-id="78763-129">للوصول إلى القوالب، انتقل إلى **إدارة المستودعات \> الإعداد \> التزويد \>  قوالب التزويد**.</span><span class="sxs-lookup"><span data-stu-id="78763-129">To access the templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span> <span data-ttu-id="78763-130">في القسم **نظره عامه**، حدد أو أنشئ قالب تزويد طلبات الموجات حيث تم تعيين الحقل **نوع التزويد** إلى *طلب الموجه*.</span><span class="sxs-lookup"><span data-stu-id="78763-130">In the **Overview** section, select or create a wave demand replenishment template where the **Replenishment type** field is set to *Wave demand*.</span></span> <span data-ttu-id="78763-131">ثم قم باعداد بنود قالب التزويد في قسم **تفاصيل قالب التزويد**.</span><span class="sxs-lookup"><span data-stu-id="78763-131">Then set up the replenishment template lines in the **Replenishment template details** section.</span></span> <span data-ttu-id="78763-132">بالنسبة لكل بند، في الحقل **استراتيجية التزويد**، حدد استراتيجية التزويد التي ترغب في استخدامها.</span><span class="sxs-lookup"><span data-stu-id="78763-132">For each line, in the **Replenishment strategy** field, select the replenishment strategy that you want to use.</span></span>

<span data-ttu-id="78763-133">![صفحة قوالب التزويد](media/ReplenTempWaveDmdMaxLocCap.png "صفحة قوالب التزويد")</span><span class="sxs-lookup"><span data-stu-id="78763-133">![Replenishment templates page](media/ReplenTempWaveDmdMaxLocCap.png "Replenishment templates page")</span></span>

<span data-ttu-id="78763-134">إذا لم يظهر عمود **استراتيجية التزويد** في الشبكة الموجودة في القسم **تفاصيل قالب التزويد**، فتاكد من انه تم تشغيل الميزة، وان قالب الاستعاضة المحدد يحتوي علي نوع التزويد *لطلب الموجه*.</span><span class="sxs-lookup"><span data-stu-id="78763-134">If the **Replenishment strategy** column doesn't appear in the grid in the **Replenishment template details** section, make sure that the feature has been turned on, and that the selected replenishment template has a replenishment type of *Wave demand*.</span></span>

> [!NOTE]
> <span data-ttu-id="78763-135">وتعتبر استراتيجية *الكمية لطلب الموجه* هي الاستراتيجية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="78763-135">The *Wave demand quantity* strategy is the default strategy.</span></span> <span data-ttu-id="78763-136">التالي ، يجب عليك فقط تحديث بنود قالب التزويد حيث تريد استخدام استراتيجية *الحد الأقصى لقدرة الموقع* بدلا من ذلك.</span><span class="sxs-lookup"><span data-stu-id="78763-136">Therefore, you just have to update the replenishment template lines where you want to use the *Maximum location capacity* strategy instead.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="78763-137">سيناريوهات مقدمة كمثال</span><span class="sxs-lookup"><span data-stu-id="78763-137">Example scenarios</span></span>

### <a name="example-1"></a><span data-ttu-id="78763-138">مثال1</span><span class="sxs-lookup"><span data-stu-id="78763-138">Example 1</span></span>

<span data-ttu-id="78763-139">بالنسبة لهذا المثال ، يوجد فقط قالب تزويد واحد يحتوي علي بند قالب تزويد واحد فقط.</span><span class="sxs-lookup"><span data-stu-id="78763-139">For this example, there is only one replenishment template that has only one replenishment template line.</span></span>

<span data-ttu-id="78763-140">تقوم بإنشاء أمر مبيعات لعدد 130 قطعة للصنف A0001.</span><span class="sxs-lookup"><span data-stu-id="78763-140">You create a sales order for 130 pieces (pcs) of item A0001.</span></span> <span data-ttu-id="78763-141">قبل إصدار الأمر إلى المستودع ، يتم اعداد المستودع بالطريقة التالية:</span><span class="sxs-lookup"><span data-stu-id="78763-141">Before you release the order to the warehouse, the warehouse is set up in the following way:</span></span>

- <span data-ttu-id="78763-142">يوجد موقع كبير واحد فقط يتضمن 500 قطعة من المخزون الفعلي المتاح.</span><span class="sxs-lookup"><span data-stu-id="78763-142">There is only one bulk location, and it has 500 pcs of available on-hand inventory.</span></span>
- <span data-ttu-id="78763-143">توجد ثلاث مواقع انتقاء، ويكون لكل منها حد مخزون يصل إلى 100قطعة.</span><span class="sxs-lookup"><span data-stu-id="78763-143">There are three pick locations, each of which has a stocking limit of 100 pcs.</span></span> <span data-ttu-id="78763-144">(تذكر ان حدود المخزون مطلوبه لاستراتيجية *الحد الاقصي للقدرة علي الموقع*.)</span><span class="sxs-lookup"><span data-stu-id="78763-144">(Remember that stocking limits are required for the *Maximum location capacity* strategy.)</span></span>
- <span data-ttu-id="78763-145">ستكون مواقع تخزين التزويد هي نفسها مواقع انتقاء المبيعات.</span><span class="sxs-lookup"><span data-stu-id="78763-145">The replenishment put locations are the same as the sales pick locations.</span></span>
- <span data-ttu-id="78763-146">وحده التزويد هي صندوق (1 صندوق = 20 قطعة).</span><span class="sxs-lookup"><span data-stu-id="78763-146">The replenishment unit is a box (1 box = 20 pcs).</span></span>

<span data-ttu-id="78763-147">وفي وقت الطلب ، يكون المخزون التالي متوافرا في مواقع انتقاء المبيعات:</span><span class="sxs-lookup"><span data-stu-id="78763-147">At the time of the order, the following inventory is on hand at the sales pick locations:</span></span>

- <span data-ttu-id="78763-148">**انتقاء 001:** عدد 20 قطعة (صندوق واحد)</span><span class="sxs-lookup"><span data-stu-id="78763-148">**Pick-001:** 20 pcs (1 box)</span></span>
- <span data-ttu-id="78763-149">**انتقاء-002:** عدد 0 قطعة</span><span class="sxs-lookup"><span data-stu-id="78763-149">**Pick-002:** 0 pcs</span></span>
- <span data-ttu-id="78763-150">**انتقاء-003:** عدد 0 قطعة</span><span class="sxs-lookup"><span data-stu-id="78763-150">**Pick-003:** 0 pcs</span></span>

<span data-ttu-id="78763-151">بشكل مبدئي ، يتم تعيين استراتيجية التزويد علي *كميه الطلب الموجه*.</span><span class="sxs-lookup"><span data-stu-id="78763-151">Initially, the replenishment strategy is set to *Wave demand quantity*.</span></span>

<span data-ttu-id="78763-152">بعد إصدار أمر المبيعات إلى المستودع ، وتشغيل معالجه الموجه للموجه ، ستحصل علي عمل التزويد التالي:</span><span class="sxs-lookup"><span data-stu-id="78763-152">After you release the sales order to the warehouse, and wave processing runs for the wave, you get the following replenishment work:</span></span>

- <span data-ttu-id="78763-153">**عمل التزويد 1:** انتقاء 4 صناديق من موقع الكمية الكبيرة، ووضعها في انتقاء-001 للموقع.</span><span class="sxs-lookup"><span data-stu-id="78763-153">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
- <span data-ttu-id="78763-154">**عمل التزويد 2:** انتقاء 2 صناديق من موقع الكمية الكبيرة، ووضعها في انتقاء-002 للموقع.</span><span class="sxs-lookup"><span data-stu-id="78763-154">**Replenishment work 2:** Pick 2 boxes from the bulk location, and put them in location pick-002.</span></span>

<span data-ttu-id="78763-155">يمكنك الحصول علي معرفي عمل التزويد نظرا لأنه يجب تزويد الموقعين ، ولا يتم دعم العديد من الوضعين.</span><span class="sxs-lookup"><span data-stu-id="78763-155">You get two replenishment work IDs because you must replenish two locations, and multi-puts aren't supported.</span></span>

<span data-ttu-id="78763-156">إذا قمت بتعيين استراتيجية التزويد إلى *الحد الأقصى لقدرة الموقع* بدلا من ذلك ، ستحصل علي عمل التزويد التالي:</span><span class="sxs-lookup"><span data-stu-id="78763-156">If you set the replenishment strategy to *Maximum location capacity* instead, you get the following replenishment work:</span></span>

- <span data-ttu-id="78763-157">**عمل التزويد 1:** انتقاء 4 صناديق من موقع الكمية الكبيرة، ووضعها في انتقاء-001 للموقع.</span><span class="sxs-lookup"><span data-stu-id="78763-157">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
- <span data-ttu-id="78763-158">**عمل التزويد 2:** انتقاء 5 صناديق من موقع الكمية الكبيرة، ووضعها في انتقاء-002 للموقع.</span><span class="sxs-lookup"><span data-stu-id="78763-158">**Replenishment work 2:** Pick 5 boxes from the bulk location, and put them in location pick-002.</span></span>

<span data-ttu-id="78763-159">[![مثال1](media/ReplenTemp_example_1.png "مثال1")](media/ReplenTemp_example_1_large.png)</span><span class="sxs-lookup"><span data-stu-id="78763-159">[![Example 1](media/ReplenTemp_example_1.png "Example 1")](media/ReplenTemp_example_1_large.png)</span></span>

### <a name="example-2"></a><span data-ttu-id="78763-160">مثال2</span><span class="sxs-lookup"><span data-stu-id="78763-160">Example 2</span></span>

<span data-ttu-id="78763-161">يوضح هذا المثال ما يحدث عندما لا يحتوي موقع الكميات الكبيرة علي مخزون كافي لتغطيه الكمية الاضافيه.</span><span class="sxs-lookup"><span data-stu-id="78763-161">This example shows what happens when the bulk location doesn't have enough inventory to cover the extra quantity.</span></span> <span data-ttu-id="78763-162">يستخدم السيناريو نفسه مثل المثال 1، ولكن موقع الكمية الكبيرة يحتوي علي 160قطعة (8 صناديق).</span><span class="sxs-lookup"><span data-stu-id="78763-162">It uses the same scenario as example 1, but the bulk location has 160 pcs (8 boxes).</span></span>

<span data-ttu-id="78763-163">تقوم استراتيجية *الكمية الخاصة بطلب الموجه* بإنشاء نفس العمل الذي كانت عليه في المثال 1.</span><span class="sxs-lookup"><span data-stu-id="78763-163">The *Wave demand quantity* strategy creates the same work that it did in example 1.</span></span>

<span data-ttu-id="78763-164">ومع ذلك ، نظرا لان استراتيجية *الحد الأقصى لقدره الموقع* تحاول إنشاء معرفات العمل كما كانت في المثال 1، قد تفشل العملية.</span><span class="sxs-lookup"><span data-stu-id="78763-164">However, because the *Maximum location capacity* strategy tries to create the work IDs as it did in example 1, it might fail.</span></span> <span data-ttu-id="78763-165">وفي هذه المرحلة ، يحاول النظام الاسترداد.</span><span class="sxs-lookup"><span data-stu-id="78763-165">At that point, the system tries to recover.</span></span>

<span data-ttu-id="78763-166">اعتمادا علي اعداد **السماح بالتقسيم** علي موجات المواقع الخاصة بانتقاء التزويد ، فانه يمكن للنتيجتين:</span><span class="sxs-lookup"><span data-stu-id="78763-166">Depending on the setting of the **Allow split** option on the location directives for replenishment picking, two outcomes are possible:</span></span>

- <span data-ttu-id="78763-167">إذا تم تعيين الخيار **السماح بالتقسيم** إلى *نعم*، يتم إنشاء عمل التزويد التالي:</span><span class="sxs-lookup"><span data-stu-id="78763-167">If the **Allow split** option is set to *Yes*, the following replenishment work is created:</span></span>

    - <span data-ttu-id="78763-168">**عمل التزويد 1:** انتقاء 4 صناديق من موقع الكمية الكبيرة، ووضعها في انتقاء-001 للموقع.</span><span class="sxs-lookup"><span data-stu-id="78763-168">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
    - <span data-ttu-id="78763-169">**عمل التزويد 2:** انتقاء 4 صناديق من موقع الكمية الكبيرة، ووضعها في انتقاء-002 للموقع.</span><span class="sxs-lookup"><span data-stu-id="78763-169">**Replenishment work 2:** Pick 4 boxes from the bulk location, and put them in location pick-002.</span></span>

- <span data-ttu-id="78763-170">إذا تم تعيين الخيار **السماح بالتقسيم** إلى *لا*، يتم إنشاء عمل التزويد التالي:</span><span class="sxs-lookup"><span data-stu-id="78763-170">If the **Allow split** option is set to *No*, the following replenishment work is created:</span></span>

    - <span data-ttu-id="78763-171">**عمل التزويد 1:** انتقاء 4 صناديق من موقع الكمية الكبيرة، ووضعها في انتقاء-001 للموقع.</span><span class="sxs-lookup"><span data-stu-id="78763-171">**Replenishment work 1:** Pick 4 boxes from the bulk location, and put them in location pick-001.</span></span>
    - <span data-ttu-id="78763-172">**عمل التزويد 2:** انتقاء 2 صناديق من موقع الكمية الكبيرة، ووضعها في انتقاء-002 للموقع.</span><span class="sxs-lookup"><span data-stu-id="78763-172">**Replenishment work 2:** Pick 2 boxes from the bulk location, and put them in location pick-002.</span></span>

<span data-ttu-id="78763-173">تختلف النتائج بسبب المعلومات المتاحة عند إنشاء العمل.</span><span class="sxs-lookup"><span data-stu-id="78763-173">The outcomes differ because of the information that is available when you create the work.</span></span> <span data-ttu-id="78763-174">عند تعيين **السماح بالتقسيم** إلى *نعم* في موجهات المواقع الخاصة بانتقاء التزويد، فأنت تعرف انك قمت بالاداره للعثور علي 160 قطعة.</span><span class="sxs-lookup"><span data-stu-id="78763-174">When the **Allow split** is set to *Yes* on the location directives for replenishment picking, you know that you managed to find 160 pcs.</span></span> <span data-ttu-id="78763-175">التالي ، يمكنك إنشاء عمل لهذه الكمية.</span><span class="sxs-lookup"><span data-stu-id="78763-175">Therefore, you can create work for that quantity.</span></span> <span data-ttu-id="78763-176">ومع ذلك ، عندما يكون الخيار **السماح بالتقسيم** معينا إلى *لا*، فانك لا تعرف بوجود 160 قطعة.</span><span class="sxs-lookup"><span data-stu-id="78763-176">However, when the **Allow split** option is set to *No*, you don't know about the existence of the 160 pcs.</span></span> <span data-ttu-id="78763-177">ونظرا لان الكمية الزائدة التي قمت بتحديدها للتزويد كانت 3 صناديق، فانك تقوم بإسقاط الكمية الاضافيه ومحاولة الكمية الاصليه مره أخرى.</span><span class="sxs-lookup"><span data-stu-id="78763-177">Because the extra quantity that you decided to replenish was 3 boxes, you drop that extra quantity and try the original quantity again.</span></span>

<span data-ttu-id="78763-178">[![مثال 2](media/ReplenTemp_example_2.png "مثال2")](media/ReplenTemp_example_2_large.png)</span><span class="sxs-lookup"><span data-stu-id="78763-178">[![Example 2](media/ReplenTemp_example_2.png "Example 2")](media/ReplenTemp_example_2_large.png)</span></span>

<span data-ttu-id="78763-179">التالي ، للحصول علي الحد الأقصى من الكمية للمواقع التي تمت تزويدها، يجب تعيين الخيار **السماح بالتقسيم** إلى *نعم* في موجات المواقع الخاصة بانتقاء التزويد.</span><span class="sxs-lookup"><span data-stu-id="78763-179">Therefore, to get the maximum quantity to the replenished locations, you should set the **Allow split** option to *Yes* on the location directives for replenishment picking.</span></span>
