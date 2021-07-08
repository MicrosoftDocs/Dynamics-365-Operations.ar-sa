---
title: استراتيجيات تعبئة الحاويات
description: يصف هذا الموضوع الاختلافات بين استراتيجيات تعبئة الحاويات ويوفر أمثلة.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292751"
---
# <a name="container-packing-strategies"></a><span data-ttu-id="0a551-103">استراتيجيات تعبئة الحاويات</span><span class="sxs-lookup"><span data-stu-id="0a551-103">Container packing strategies</span></span>

<span data-ttu-id="0a551-104">*إستراتيجية تعبئة الحاويات* هي إستراتيجية يمكنك استخدامها لتحديد توزيعات الأصناف عبر الحاويات.</span><span class="sxs-lookup"><span data-stu-id="0a551-104">A *container packing strategy* is a strategy that you can use to define item allocations across containers.</span></span> <span data-ttu-id="0a551-105">يوضح هذا الموضوع الفروق بين إستراتيجيات *التعبئة في كافة الحاويات المفتوحة* و *التعبئة في الحاوية الحالية فقط*.</span><span class="sxs-lookup"><span data-stu-id="0a551-105">This topic explains the differences between the *Pack into all open containers* and *Pack into current container only* strategies.</span></span>

- <span data-ttu-id="0a551-106">**التعبئة في كافة الحاويات المفتوحة** – يجب أن يقوم النظام بالتحقق من كافة الحاويات المفتوحة التي تم إنشاؤها بالفعل أثناء دورة التعبئة في حاويات ، للتأكد من أن الصنف سيتناسب مع أحدها.</span><span class="sxs-lookup"><span data-stu-id="0a551-106">**Pack into all open containers** – The system must check all open containers that have already been created during the containerization cycle, to make sure that the item will fit into one of them.</span></span> <span data-ttu-id="0a551-107">أثناء التعبئة، يقوم النظام بالتحقق من كل صنف لتحديد ما إذا كان سيتم احتواؤه في أي من الحاويات التي تم إنشاؤها مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="0a551-107">During packing, the system checks each item to determine whether it will fit into any of the previously created containers.</span></span> <span data-ttu-id="0a551-108">وفي حالة عدم تناسب الصنف في حاوية موجودة، يقوم النظام بإنشاء حاوية جديدة والمتابعة حتى ينتهي من تعبئة الأمر بالكامل.</span><span class="sxs-lookup"><span data-stu-id="0a551-108">If the item won't fit into an existing container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="0a551-109">على سبيل المثال، تتطلب الأصناف المطلوبة *n* التعبئة في حاويات.</span><span class="sxs-lookup"><span data-stu-id="0a551-109">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="0a551-110">في أسوأ الحالات، في كل مرة يقوم النظام بمعالجة صنف لا يتناسب مع أي حاوية حالية، فإنه سيقوم بإجمالي عمليات فحص (\[(*n* – 1) × (*n* + 1)\] ÷ 2) لتقييم ما إذا كان الصنف يتناسب مع الحاويات الموجودة أم لا.</span><span class="sxs-lookup"><span data-stu-id="0a551-110">In the worst case, every time that the system processes an item that doesn't fit into any existing container, it will do a total of (\[(*n* – 1) × (*n* + 1)\] ÷ 2) checks to evaluate whether the item fits into the existing containers.</span></span>

- <span data-ttu-id="0a551-111">**التعبئة في الحاوية الحالية فقط** – يجب أن يقوم النظام بفحص أحدث حاوية تم إنشائها فقط للتأكد من أن الصنف يتناسب معها.</span><span class="sxs-lookup"><span data-stu-id="0a551-111">**Pack into current container only** – The system must check only the most recently created container to make sure that the item will fit into it.</span></span> <span data-ttu-id="0a551-112">أثناء التعبئة، يقوم النظام بالتحقق من كل صنف لتحديد ما إذا كان سيتم احتواؤه في أحدث حاوية تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="0a551-112">During packing, the system checks each item to determine whether it will fit into the most recently created container.</span></span> <span data-ttu-id="0a551-113">وفي حالة عدم تناسب الصنف في تلك الحاوية، يقوم النظام بإنشاء حاوية جديدة والمتابعة حتى ينتهي من تعبئة الأمر بالكامل.</span><span class="sxs-lookup"><span data-stu-id="0a551-113">If the item won't fit into that container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="0a551-114">على سبيل المثال، تتطلب الأصناف المطلوبة *n* التعبئة في حاويات.</span><span class="sxs-lookup"><span data-stu-id="0a551-114">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="0a551-115">وفي أسوأ الحالات، سيقوم النظام بإجراء إجمالي عمليات فحص (*n* – 1) لتقييم ما إذا كان الصنف سيتناسب مع الحاويات أم لا.</span><span class="sxs-lookup"><span data-stu-id="0a551-115">In the worst case, the system will do a total of (*n* – 1) checks to evaluate whether the item fits into the containers.</span></span>

## <a name="example-of-the-flow-for-container-packing-strategies"></a><span data-ttu-id="0a551-116">مثال على تدفق ‏‫استراتيجيات تعبئة الحاويات‬</span><span class="sxs-lookup"><span data-stu-id="0a551-116">Example of the flow for container packing strategies</span></span>

<span data-ttu-id="0a551-117">قم بإعداد الأصناف التالية للتعبئة في حاويات.</span><span class="sxs-lookup"><span data-stu-id="0a551-117">You set up the following items for containerization.</span></span>

| <span data-ttu-id="0a551-118">الصنف</span><span class="sxs-lookup"><span data-stu-id="0a551-118">Item</span></span> | <span data-ttu-id="0a551-119">الأبعاد الفعلية (العرض × العمق × الارتفاع)</span><span class="sxs-lookup"><span data-stu-id="0a551-119">Physical dimensions (width × depth × height)</span></span> | <span data-ttu-id="0a551-120">الوزن</span><span class="sxs-lookup"><span data-stu-id="0a551-120">Weight</span></span> |
|---|---|---|
| <span data-ttu-id="0a551-121">كبل HDMI 6</span><span class="sxs-lookup"><span data-stu-id="0a551-121">HDMI Cable 6'</span></span> | <span data-ttu-id="0a551-122">1 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="0a551-122">1 × 1 × 1</span></span> | <span data-ttu-id="0a551-123">1</span><span class="sxs-lookup"><span data-stu-id="0a551-123">1</span></span> |
| <span data-ttu-id="0a551-124">كبل HDMI 12</span><span class="sxs-lookup"><span data-stu-id="0a551-124">HDMI Cable 12'</span></span> | <span data-ttu-id="0a551-125">2 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="0a551-125">2 × 1 × 1</span></span> | <span data-ttu-id="0a551-126">1</span><span class="sxs-lookup"><span data-stu-id="0a551-126">1</span></span> |
| <span data-ttu-id="0a551-127">كبل HDMI 18</span><span class="sxs-lookup"><span data-stu-id="0a551-127">HDMI Cable 18'</span></span> | <span data-ttu-id="0a551-128">3 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="0a551-128">3 × 1 × 1</span></span> | <span data-ttu-id="0a551-129">2</span><span class="sxs-lookup"><span data-stu-id="0a551-129">2</span></span> |

<span data-ttu-id="0a551-130">كما يمكنك أيضًا إعداد الصندوق التالية التي سيتم استخدامها لإجراء التعبئة.</span><span class="sxs-lookup"><span data-stu-id="0a551-130">You also set up the following box that will be used for packaging.</span></span>

| <span data-ttu-id="0a551-131">الحاوية</span><span class="sxs-lookup"><span data-stu-id="0a551-131">Container</span></span> | <span data-ttu-id="0a551-132">الأبعاد الفعلية (الطول × العرض × الارتفاع)</span><span class="sxs-lookup"><span data-stu-id="0a551-132">Physical dimensions (length × width × height)</span></span> | <span data-ttu-id="0a551-133">الوزن</span><span class="sxs-lookup"><span data-stu-id="0a551-133">Weight</span></span> | <span data-ttu-id="0a551-134">الحجم</span><span class="sxs-lookup"><span data-stu-id="0a551-134">Volume</span></span> |
|---|---|---|---|
| <span data-ttu-id="0a551-135">صندوق متوسط</span><span class="sxs-lookup"><span data-stu-id="0a551-135">Medium Box</span></span> | <span data-ttu-id="0a551-136">6 × 3 × 2</span><span class="sxs-lookup"><span data-stu-id="0a551-136">6 × 3 × 2</span></span> | <span data-ttu-id="0a551-137">10</span><span class="sxs-lookup"><span data-stu-id="0a551-137">10</span></span> | <span data-ttu-id="0a551-138">100</span><span class="sxs-lookup"><span data-stu-id="0a551-138">100</span></span> |

<span data-ttu-id="0a551-139">وأخيرًا، قم بإعداد الأمر الذي يحتوي على المنتجات والكميات التالية.</span><span class="sxs-lookup"><span data-stu-id="0a551-139">Finally, you set up an order that has the following products and quantities.</span></span>

| <span data-ttu-id="0a551-140">سطر أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="0a551-140">Sales order line</span></span> | <span data-ttu-id="0a551-141">الكمية</span><span class="sxs-lookup"><span data-stu-id="0a551-141">Quantity</span></span> |
|---|---|
| <span data-ttu-id="0a551-142">كبل HDMI 12</span><span class="sxs-lookup"><span data-stu-id="0a551-142">HDMI Cable 12'</span></span> | <span data-ttu-id="0a551-143">9</span><span class="sxs-lookup"><span data-stu-id="0a551-143">9</span></span> |
| <span data-ttu-id="0a551-144">كبل HDMI 18</span><span class="sxs-lookup"><span data-stu-id="0a551-144">HDMI Cable 18'</span></span> | <span data-ttu-id="0a551-145">8</span><span class="sxs-lookup"><span data-stu-id="0a551-145">8</span></span> |
| <span data-ttu-id="0a551-146">كبل HDMI 6</span><span class="sxs-lookup"><span data-stu-id="0a551-146">HDMI Cable 6'</span></span> | <span data-ttu-id="0a551-147">13</span><span class="sxs-lookup"><span data-stu-id="0a551-147">13</span></span> |

<span data-ttu-id="0a551-148">يلخص الجدول التالي كيفية عمل إعداد التعبئة عند استخدام إستراتيجية *التعبئة في كافة الحاويات المفتوحة* وعند استخدام إستراتيجية *التعبئة في الحاوية الحالية فقط*.</span><span class="sxs-lookup"><span data-stu-id="0a551-148">The following table summarizes how containerization works when you use the *Pack into all open containers* strategy and when you use the *Pack into current container only* strategy.</span></span>

| <span data-ttu-id="0a551-149">تعبئة في جميع الحاويات المفتوحة</span><span class="sxs-lookup"><span data-stu-id="0a551-149">Pack into all open containers</span></span> | <span data-ttu-id="0a551-150">التعبئة في الحاوية الحالية</span><span class="sxs-lookup"><span data-stu-id="0a551-150">Pack into current container</span></span> |
|---|---|
| <p><span data-ttu-id="0a551-151">كبل HDMI 12:</span><span class="sxs-lookup"><span data-stu-id="0a551-151">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="0a551-152">إنشاء حاوية جديد، CONT0001.</span><span class="sxs-lookup"><span data-stu-id="0a551-152">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="0a551-153">ضع 9 ea في حاوية CONT0001 الحاوية.</span><span class="sxs-lookup"><span data-stu-id="0a551-153">Put 9 ea into container CONT0001.</span></span></li></ol> | <p><span data-ttu-id="0a551-154">كبل HDMI 12:</span><span class="sxs-lookup"><span data-stu-id="0a551-154">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="0a551-155">إنشاء حاوية جديد، CONT0001.</span><span class="sxs-lookup"><span data-stu-id="0a551-155">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="0a551-156">ضع 9 ea في حاوية CONT0001 الحاوية.</span><span class="sxs-lookup"><span data-stu-id="0a551-156">Put 9 ea into container CONT0001.</span></span></li></ol> |
| <p><span data-ttu-id="0a551-157">كبل HDMI 18:</span><span class="sxs-lookup"><span data-stu-id="0a551-157">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="0a551-158">تحقق مما إذا كان يمكن أن يتناسب الصنف مع الحاوية CONT0001.</span><span class="sxs-lookup"><span data-stu-id="0a551-158">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="0a551-159">إنشاء حاوية جديد، CONT0002.</span><span class="sxs-lookup"><span data-stu-id="0a551-159">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="0a551-160">ضع 5 ea في حاوية CONT0002 الحاوية.</span><span class="sxs-lookup"><span data-stu-id="0a551-160">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="0a551-161">إنشاء حاوية جديد، CONT0003.</span><span class="sxs-lookup"><span data-stu-id="0a551-161">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="0a551-162">ضع 3 ea في حاوية CONT0003 الحاوية.</span><span class="sxs-lookup"><span data-stu-id="0a551-162">Put 3 ea into container CONT0003.</span></span></li></ol> | <p><span data-ttu-id="0a551-163">كبل HDMI 18:</span><span class="sxs-lookup"><span data-stu-id="0a551-163">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="0a551-164">تحقق مما إذا كان يمكن أن يتناسب الصنف مع الحاوية CONT0001.</span><span class="sxs-lookup"><span data-stu-id="0a551-164">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="0a551-165">إنشاء حاوية جديد، CONT0002.</span><span class="sxs-lookup"><span data-stu-id="0a551-165">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="0a551-166">ضع 5 ea في حاوية CONT0002 الحاوية.</span><span class="sxs-lookup"><span data-stu-id="0a551-166">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="0a551-167">إنشاء حاوية جديد، CONT0003.</span><span class="sxs-lookup"><span data-stu-id="0a551-167">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="0a551-168">ضع 3 ea في حاوية CONT0003 الحاوية.</span><span class="sxs-lookup"><span data-stu-id="0a551-168">Put 3 ea into container CONT0003.</span></span></li></ol> |
| <p><span data-ttu-id="0a551-169">كبل HDMI 6:</span><span class="sxs-lookup"><span data-stu-id="0a551-169">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="0a551-170">تحقق مما إذا كان يمكن أن يتناسب الصنف مع الحاوية CONT0001.</span><span class="sxs-lookup"><span data-stu-id="0a551-170">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="0a551-171">ضع 1 ea في حاوية CONT0001 الحاوية.</span><span class="sxs-lookup"><span data-stu-id="0a551-171">Put 1 ea into container CONT0001.</span></span></li><li><span data-ttu-id="0a551-172">تحقق مما إذا كان يمكن أن يتناسب الصنف مع الحاوية CONT0002.</span><span class="sxs-lookup"><span data-stu-id="0a551-172">Check whether the item can fit into container CONT0002.</span></span></li><li><span data-ttu-id="0a551-173">تحقق مما إذا كان يمكن أن يتناسب الصنف مع الحاوية CONT0003.</span><span class="sxs-lookup"><span data-stu-id="0a551-173">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="0a551-174">ضع 4 ea في حاوية CONT0003 الحاوية.</span><span class="sxs-lookup"><span data-stu-id="0a551-174">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="0a551-175">إنشاء حاوية جديد، CONT0004.</span><span class="sxs-lookup"><span data-stu-id="0a551-175">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="0a551-176">ضع 8 ea في حاوية CONT0004 الحاوية.</span><span class="sxs-lookup"><span data-stu-id="0a551-176">Put 8 ea into container CONT0004.</span></span></li></ol> | <p><span data-ttu-id="0a551-177">كبل HDMI 6:</span><span class="sxs-lookup"><span data-stu-id="0a551-177">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="0a551-178">تحقق مما إذا كان يمكن أن يتناسب الصنف مع الحاوية CONT0003.</span><span class="sxs-lookup"><span data-stu-id="0a551-178">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="0a551-179">ضع 4 ea في حاوية CONT0003 الحاوية.</span><span class="sxs-lookup"><span data-stu-id="0a551-179">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="0a551-180">إنشاء حاوية جديد، CONT0004.</span><span class="sxs-lookup"><span data-stu-id="0a551-180">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="0a551-181">ضع 9 ea في حاوية CONT0004 الحاوية.</span><span class="sxs-lookup"><span data-stu-id="0a551-181">Put 9 ea into container CONT0004.</span></span></li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a><span data-ttu-id="0a551-182">السيناريو المثال: تعبئة الأوامر المفردة لكل حاوية</span><span class="sxs-lookup"><span data-stu-id="0a551-182">Example scenario: Pack single orders per container</span></span>

<span data-ttu-id="0a551-183">يقدم هذا القسم سيناريو حيث يتم إعداد النظام فيه لتوحيد الأوامر المتعددة في شحنة واحدة.</span><span class="sxs-lookup"><span data-stu-id="0a551-183">This section presents a scenario where the system is set up to consolidate multiple orders into one shipment.</span></span> <span data-ttu-id="0a551-184">وبالتالي، سيتم القيام بالتعبئة في حاوية من أمر المبيعات لضمان أن كل أمر يحتوي على منتجات متعددة يتم تعبئته في الحاوية الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="0a551-184">Therefore, containerization will be done from the sales order to ensure that every order that contains multiple products is packed into its own container.</span></span>

<span data-ttu-id="0a551-185">تتيح لك هذه الوظيفة معالجة السيناريوهات التي يجب فيها تعبئة أمر مبيعات واحد فقط في كل حاوية، وبالتالي يمكن لمركز التوزيع أن يقوم بتوزيع بضائع حاويات كاملة بين متاجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="0a551-185">This functionality lets you handle scenarios where you must pack only one sales order into each container, so that the distribution center can cross-dock full containers between retail stores.</span></span> <span data-ttu-id="0a551-186">بالإضافة إلى سيناريوهات البيع بالتجزئة (طلب لكل متجر بيع بالتجزئة والشحن لمركز التوزيع لتوزيع البضائع)، يتم استخدام هذه التقنية أيضًا بشكل عام في سلاسل توريد محدودة الفاقد (أمر المبيعات لكل بند إنتاج في الوقت المناسب).</span><span class="sxs-lookup"><span data-stu-id="0a551-186">In addition to the retail scenarios (order per retail store and shipping to a distribution center for cross-docking) this technique is also commonly used in lean supply chains (sales order per just-in-time production line).</span></span>

<span data-ttu-id="0a551-187">يوضح هذا السيناريو كيف يمكنك تخفيض عدد الحاويات التي يتم تقييمها أثناء التعبئة باستخدام إستراتيجية *التعبئة في الحاوية الحالية فقط* للتعبئة في الحاويات.</span><span class="sxs-lookup"><span data-stu-id="0a551-187">This scenario shows how you can decrease the number of containers that are evaluated during packing by using the *Pack into current container only* strategy for containerization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0a551-188">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="0a551-188">Prerequisites</span></span>

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a><span data-ttu-id="0a551-189">تشغيل ميزة دمج الشحنات في النظام</span><span class="sxs-lookup"><span data-stu-id="0a551-189">Turn on the Consolidate shipments feature in your system</span></span>

<span data-ttu-id="0a551-190">يستخدم هذا السيناريو الميزة *دمج الشحنات*.</span><span class="sxs-lookup"><span data-stu-id="0a551-190">This scenario uses the *Consolidate shipments* feature.</span></span> <span data-ttu-id="0a551-191">إذا لم تكن هذه الميزة متوفرة بالفعل في النظام، فإنه يجب تشغيلها باستخدام [إدارة الميزات](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0a551-191">If that feature isn't already available in your system, you must turn it on by using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

#### <a name="make-demo-data-available"></a><span data-ttu-id="0a551-192">جعل بيانات العرض التوضيحي متاحة</span><span class="sxs-lookup"><span data-stu-id="0a551-192">Make demo data available</span></span>

<span data-ttu-id="0a551-193">يشير هذا السيناريو إلى قيم وسجلات مضمنة في بيانات العرض التوضيحي القياسية المتوفرة لـ Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="0a551-193">This scenario references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0a551-194">إذا كنت ترغب في استخدام القيم الواردة هنا أثناء تنفيذ التمرينات، فتأكد من العمل في بيئة تم فيها تثبيت بيانات العرض التوضيحي، وقم بتعيين الكيان القانوني إلى **USMF** قبل أن تبدأ.</span><span class="sxs-lookup"><span data-stu-id="0a551-194">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

### <a name="inspect-or-create-container-types"></a><span data-ttu-id="0a551-195">فحص أنواع الحاويات أو إنشاؤها</span><span class="sxs-lookup"><span data-stu-id="0a551-195">Inspect or create container types</span></span>

<span data-ttu-id="0a551-196">لفحص أنواع الحاويات الخاصة بك، أو لإنشاء أنواع حاويات جديدة إذا كانت مطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0a551-196">To inspect your container types, or to create new container types if they are required, follow these steps.</span></span>

1. <span data-ttu-id="0a551-197">انتقل إلى **إدارة المستودعات** \> **إعداد** \> **الحاويات** \> **أنواع الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="0a551-197">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>
1. <span data-ttu-id="0a551-198">تأكد من توفر كل نوع من الحاويات التالية في بيانات العرض التوضيحي الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="0a551-198">Make sure that each of the following container types is available in your demo data.</span></span> <span data-ttu-id="0a551-199">قم بتحرير أنواع الحاويات أو إنشائها حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="0a551-199">Edit or create container types as required.</span></span>

    - <span data-ttu-id="0a551-200">نوع الحاوية 1:</span><span class="sxs-lookup"><span data-stu-id="0a551-200">Container type 1:</span></span>

        - <span data-ttu-id="0a551-201">**كود نوع الحاوية:** *صندوق كبير*</span><span class="sxs-lookup"><span data-stu-id="0a551-201">**Container type code:** *Box-Large*</span></span>
        - <span data-ttu-id="0a551-202">**الوصف:** *صندوق كبير*</span><span class="sxs-lookup"><span data-stu-id="0a551-202">**Description:** *Large Box*</span></span>
        - <span data-ttu-id="0a551-203">**الحد الأقصى للوزن الصافي:** *100*</span><span class="sxs-lookup"><span data-stu-id="0a551-203">**Maximum net weight:** *100*</span></span>
        - <span data-ttu-id="0a551-204">**الحجم:** *400*</span><span class="sxs-lookup"><span data-stu-id="0a551-204">**Volume:** *400*</span></span>
        - <span data-ttu-id="0a551-205">**الطول:** *4*</span><span class="sxs-lookup"><span data-stu-id="0a551-205">**Length:** *4*</span></span>
        - <span data-ttu-id="0a551-206">**العرض:** *10*</span><span class="sxs-lookup"><span data-stu-id="0a551-206">**Width:** *10*</span></span>
        - <span data-ttu-id="0a551-207">**الارتفاع:** *10*</span><span class="sxs-lookup"><span data-stu-id="0a551-207">**Height:** *10*</span></span>

    - <span data-ttu-id="0a551-208">نوع الحاوية 2:</span><span class="sxs-lookup"><span data-stu-id="0a551-208">Container type 2:</span></span>

        - <span data-ttu-id="0a551-209">**كود نوع الحاوية:** *صندوق متوسط*</span><span class="sxs-lookup"><span data-stu-id="0a551-209">**Container type code:** *Box-Medium*</span></span>
        - <span data-ttu-id="0a551-210">**الوصف:** *صندوق متوسط*</span><span class="sxs-lookup"><span data-stu-id="0a551-210">**Description:** *Medium Box*</span></span>
        - <span data-ttu-id="0a551-211">**الحد الأقصى للوزن الصافي:** *50*</span><span class="sxs-lookup"><span data-stu-id="0a551-211">**Maximum net weight:** *50*</span></span>
        - <span data-ttu-id="0a551-212">**الحجم:** *200*</span><span class="sxs-lookup"><span data-stu-id="0a551-212">**Volume:** *200*</span></span>
        - <span data-ttu-id="0a551-213">**الطول:** *2*</span><span class="sxs-lookup"><span data-stu-id="0a551-213">**Length:** *2*</span></span>
        - <span data-ttu-id="0a551-214">**العرض:** *10*</span><span class="sxs-lookup"><span data-stu-id="0a551-214">**Width:** *10*</span></span>
        - <span data-ttu-id="0a551-215">**الارتفاع:** *10*</span><span class="sxs-lookup"><span data-stu-id="0a551-215">**Height:** *10*</span></span>

    - <span data-ttu-id="0a551-216">نوع الحاوية 3:</span><span class="sxs-lookup"><span data-stu-id="0a551-216">Container type 3:</span></span>

        - <span data-ttu-id="0a551-217">**كود نوع الحاوية:** *صندوق صغير*</span><span class="sxs-lookup"><span data-stu-id="0a551-217">**Container type code:** *Box-Small*</span></span>
        - <span data-ttu-id="0a551-218">**الوصف:** *صندوق صغير*</span><span class="sxs-lookup"><span data-stu-id="0a551-218">**Description:** *Small Box*</span></span>
        - <span data-ttu-id="0a551-219">**الحد الأقصى للوزن الصافي:** *20*</span><span class="sxs-lookup"><span data-stu-id="0a551-219">**Maximum net weight:** *20*</span></span>
        - <span data-ttu-id="0a551-220">**الحجم:** *100*</span><span class="sxs-lookup"><span data-stu-id="0a551-220">**Volume:** *100*</span></span>
        - <span data-ttu-id="0a551-221">**الطول:** *1*</span><span class="sxs-lookup"><span data-stu-id="0a551-221">**Length:** *1*</span></span>
        - <span data-ttu-id="0a551-222">**العرض:** *10*</span><span class="sxs-lookup"><span data-stu-id="0a551-222">**Width:** *10*</span></span>
        - <span data-ttu-id="0a551-223">**الارتفاع:** *10*</span><span class="sxs-lookup"><span data-stu-id="0a551-223">**Height:** *10*</span></span>

### <a name="inspect-or-create-container-groups"></a><span data-ttu-id="0a551-224">فحص مجموعات الحاويات أو إنشاؤها</span><span class="sxs-lookup"><span data-stu-id="0a551-224">Inspect or create container groups</span></span>

<span data-ttu-id="0a551-225">لفحص مجموعات الحاويات الخاصة بك، أو لإنشاء مجموعات حاويات جديدة إذا كانت مطلوبة، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0a551-225">To inspect your container groups, or to create new container groups if they are required, follow these steps.</span></span>

1. <span data-ttu-id="0a551-226">انتقل إلى **إدارة المستودعات** \> **إعداد** \> **الحاويات** \> **مجموعات الحاويات**.</span><span class="sxs-lookup"><span data-stu-id="0a551-226">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="0a551-227">تأكد من توفر كل مجموعة من الحاويات التالية في بيانات العرض التوضيحي الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="0a551-227">Make sure that the following container group is available in your demo data.</span></span> <span data-ttu-id="0a551-228">إذا لم يكن متاحًا، فحدد **جديد** لإنشاءه.</span><span class="sxs-lookup"><span data-stu-id="0a551-228">If it isn't available, select **New** to create it.</span></span>

    - <span data-ttu-id="0a551-229">**معرف مجموعة الحاويات:** *صناديق*</span><span class="sxs-lookup"><span data-stu-id="0a551-229">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="0a551-230">**الوصف:** *أحجام الصناديق*</span><span class="sxs-lookup"><span data-stu-id="0a551-230">**Description:** *Box sizes*</span></span>

1. <span data-ttu-id="0a551-231">في علامة التبويب السريعة **تفاصيل** لمجموعة حاوية *الصناديق*، تأكد من وجود البنود التالية.</span><span class="sxs-lookup"><span data-stu-id="0a551-231">On the **Details** FastTab for the *Boxes* container group, make sure that the following lines exist.</span></span> <span data-ttu-id="0a551-232">في حالة عدم تحديدها، حدد **جديد** لإضافتها.</span><span class="sxs-lookup"><span data-stu-id="0a551-232">If they don't, select **New** to add them.</span></span>

    - <span data-ttu-id="0a551-233">السطر 1:</span><span class="sxs-lookup"><span data-stu-id="0a551-233">Line 1:</span></span>

        - <span data-ttu-id="0a551-234">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="0a551-234">**Sequence number:** *1*</span></span>
        - <span data-ttu-id="0a551-235">**نوع الحاوية:** *صندوق كبير*</span><span class="sxs-lookup"><span data-stu-id="0a551-235">**Container type:** *Box-Large*</span></span>
        - <span data-ttu-id="0a551-236">**النسبة المئوية لاستخدام الحاوية:** *100*</span><span class="sxs-lookup"><span data-stu-id="0a551-236">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="0a551-237">السطر 2:</span><span class="sxs-lookup"><span data-stu-id="0a551-237">Line 2:</span></span>

        - <span data-ttu-id="0a551-238">**رقم المسلسل:** *2*</span><span class="sxs-lookup"><span data-stu-id="0a551-238">**Sequence number:** *2*</span></span>
        - <span data-ttu-id="0a551-239">**نوع الحاوية:** *صندوق متوسط*</span><span class="sxs-lookup"><span data-stu-id="0a551-239">**Container type:** *Box-Medium*</span></span>
        - <span data-ttu-id="0a551-240">**النسبة المئوية لاستخدام الحاوية:** *100*</span><span class="sxs-lookup"><span data-stu-id="0a551-240">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="0a551-241">السطر 3:</span><span class="sxs-lookup"><span data-stu-id="0a551-241">Line 3:</span></span>

        - <span data-ttu-id="0a551-242">**رقم المسلسل:** *3*</span><span class="sxs-lookup"><span data-stu-id="0a551-242">**Sequence number:** *3*</span></span>
        - <span data-ttu-id="0a551-243">**نوع الحاوية:** *صندوق صغير*</span><span class="sxs-lookup"><span data-stu-id="0a551-243">**Container type:** *Box-Small*</span></span>
        - <span data-ttu-id="0a551-244">**النسبة المئوية لاستخدام الحاوية:** *100*</span><span class="sxs-lookup"><span data-stu-id="0a551-244">**Container utilization percentage:** *100*</span></span>

### <a name="create-a-new-container-build-template"></a><span data-ttu-id="0a551-245">إنشاء قالب بنية حاوية جديد</span><span class="sxs-lookup"><span data-stu-id="0a551-245">Create a new container build template</span></span>

<span data-ttu-id="0a551-246">لإنشاء قالب بناء حاوية جديد، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="0a551-246">To create a new container build template, follow these steps.</span></span>

1. <span data-ttu-id="0a551-247">انتقل إلى **إدارة المستودعات** \> **إعداد** \> **الحاويات** \> **قالب بنية الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="0a551-247">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="0a551-248">حدد **جديد** لإنشاء قالب بناء حاوية يوجد به الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="0a551-248">Select **New** to create a container build template that has the following settings:</span></span>

    - <span data-ttu-id="0a551-249">**رقم المسلسل:** *1*</span><span class="sxs-lookup"><span data-stu-id="0a551-249">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="0a551-250">**معرف قالب الحاوية:** *صندوق*</span><span class="sxs-lookup"><span data-stu-id="0a551-250">**Container template ID:** *Box*</span></span>
    - <span data-ttu-id="0a551-251">**معرف مجموعة الحاويات:** *صناديق*</span><span class="sxs-lookup"><span data-stu-id="0a551-251">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="0a551-252">**أنواع الاستعلام الأساسية:** *بند توزيع المبيعات*</span><span class="sxs-lookup"><span data-stu-id="0a551-252">**Base query types:** *Sales allocation line*</span></span>
    - <span data-ttu-id="0a551-253">**رمز خطوة الموجة:** *234*</span><span class="sxs-lookup"><span data-stu-id="0a551-253">**Wave step code:** *234*</span></span>
    - <span data-ttu-id="0a551-254">**‬‏‫السماح بتقسيم الانتقاءات:** *نعم*</span><span class="sxs-lookup"><span data-stu-id="0a551-254">**Allow split picks:** *Yes*</span></span>
    - <span data-ttu-id="0a551-255">**‬‏‫إستراتيجية تعبئة الحاويات:** *التعبئة في الحاوية الحالية فقط*</span><span class="sxs-lookup"><span data-stu-id="0a551-255">**Container packing strategy:** *Pack into current container only*</span></span>
    - <span data-ttu-id="0a551-256">**‬‏‫الوحدة الموجهة‬‏‫:** *لا*</span><span class="sxs-lookup"><span data-stu-id="0a551-256">**Pack by directive unit:** *No*</span></span>

1. <span data-ttu-id="0a551-257">في حين أن الصف للقالب الجديد لا يزال محددًا، حدد **تحرير الاستعلام** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="0a551-257">While the row for the new template is still selected, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="0a551-258">يظهر مربع حوار محرر Power Query القياسية.</span><span class="sxs-lookup"><span data-stu-id="0a551-258">A standard query editor dialog box appears.</span></span> <span data-ttu-id="0a551-259">في علامة التبويب **الفرز** حدد **إضافة** لإضافة صف يتضمن الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="0a551-259">On the **Sorting** tab, select **Add** to add a row that has the following settings:</span></span>

    - <span data-ttu-id="0a551-260">**الجدول:** *حركات العمل المؤقتة*</span><span class="sxs-lookup"><span data-stu-id="0a551-260">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="0a551-261">**الجدول المشتق:** *حركات العمل المؤقتة*</span><span class="sxs-lookup"><span data-stu-id="0a551-261">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="0a551-262">**الحقل:** *رقم الأمر*</span><span class="sxs-lookup"><span data-stu-id="0a551-262">**Field:** *Order number*</span></span>
    - <span data-ttu-id="0a551-263">**اتجاه البحث:** *تصاعدي*</span><span class="sxs-lookup"><span data-stu-id="0a551-263">**Search direction:** *Ascending*</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="0a551-264">لتجنب الدوران حول كافة الحاويات المفتوحة الأخرى، ولزيادة سرعة العملية عن طريق التحقق من حاوية واحدة في كل مرة، استخدم إستراتيجية *التعبئة في الحاوية الحالية فقط* بالإضافة إلى الفرز حسب رقم الأمر.</span><span class="sxs-lookup"><span data-stu-id="0a551-264">To avoid cycling over all the other open containers, and to speed up the process by checking one container at a time, use the *Pack into current container only* strategy in addition to sorting by order number.</span></span> <span data-ttu-id="0a551-265">وسوف تعمل هذه المجموعة كفاصل عمل في قالب عمل.</span><span class="sxs-lookup"><span data-stu-id="0a551-265">This combination will work like a work break on a work template.</span></span>

1. <span data-ttu-id="0a551-266">حدد **موافق** لإغلاق مربع حوار محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="0a551-266">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="0a551-267">في حين أن الصف للقالب الجديد لا يزال محددًا، حدد **قيود خلط الحاويات** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="0a551-267">While the row for the new template is still selected, select **Container mixing constraints** on the Action Pane.</span></span>

    <span data-ttu-id="0a551-268">ستقوم الآن بإضافة قيد يضع الأصناف من ترتيب فردي واحد في حاوية واحدة.</span><span class="sxs-lookup"><span data-stu-id="0a551-268">You will now add a constraint that puts items from a single order into a single container.</span></span> <span data-ttu-id="0a551-269">سيتم وضع الأصناف من أي أمر آخر في حاوية منفصلة.</span><span class="sxs-lookup"><span data-stu-id="0a551-269">Items from any other order will be put into a separate container.</span></span>

1. <span data-ttu-id="0a551-270">حدد **جديد** لإنشاء قيود خلط يوجد به الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="0a551-270">Select **New** to create a mixing constraint that has the following settings:</span></span>

    - <span data-ttu-id="0a551-271">**الجدول:** *أوامر المبيعات*</span><span class="sxs-lookup"><span data-stu-id="0a551-271">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="0a551-272">**تحديد الحقل:** *SalesId* (سيظهر الحقل كـ *أمر مبيعات* في الشبكة.)</span><span class="sxs-lookup"><span data-stu-id="0a551-272">**Field select:** *SalesId* (The field will appear as *Sales order* in the grid.)</span></span>

1. <span data-ttu-id="0a551-273">حدد **موافق** لإضافة القيد.</span><span class="sxs-lookup"><span data-stu-id="0a551-273">Select **OK** to add the constraint.</span></span>
1. <span data-ttu-id="0a551-274">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0a551-274">Close the page.</span></span>

### <a name="set-up-a-wave-template-for-containerization"></a><span data-ttu-id="0a551-275">إعداد قالب موجة للتعبئة في الحاويات</span><span class="sxs-lookup"><span data-stu-id="0a551-275">Set up a wave template for containerization</span></span>

<span data-ttu-id="0a551-276">لإعداد قالب موجة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="0a551-276">To set up a wave template, follow these steps.</span></span>

1. <span data-ttu-id="0a551-277">انتقل إلى **إدارة المستودعات \> الإعداد \> الموجات \> قوالب الموجة**.</span><span class="sxs-lookup"><span data-stu-id="0a551-277">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="0a551-278">في جزء القائمة، قم بتعيين حقل **نوع قالب الموجة** إلى *شحن*.</span><span class="sxs-lookup"><span data-stu-id="0a551-278">In the list pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="0a551-279">حدد القالب **التعبئة في الحاويات 63** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="0a551-279">Select the **63 Containerization** template in the list.</span></span>
1. <span data-ttu-id="0a551-280">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="0a551-280">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="0a551-281">على علامة التبويب السريع **الأساليب**، في عمود **الأساليب المحددة**، ابحث عن البند التالي:</span><span class="sxs-lookup"><span data-stu-id="0a551-281">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="0a551-282">**اسم الأسلوب:** *التعبئة في الحاويات*</span><span class="sxs-lookup"><span data-stu-id="0a551-282">**Method name:** *containerization*</span></span>
    - <span data-ttu-id="0a551-283">**الاسم:** *التعبئة في حاويات*</span><span class="sxs-lookup"><span data-stu-id="0a551-283">**Name:** *Containerization*</span></span>

1. <span data-ttu-id="0a551-284">قم بتعيين الحقل **كود خطوة الموجة** للبند إلى *234*.</span><span class="sxs-lookup"><span data-stu-id="0a551-284">Set the **Wave step code** field for the line to *234*.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="0a551-285">إعداد قالب عمل</span><span class="sxs-lookup"><span data-stu-id="0a551-285">Set up a work template</span></span>

<span data-ttu-id="0a551-286">لإعداد قالب عمل، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="0a551-286">To set up a work template, follow these steps.</span></span>

1. <span data-ttu-id="0a551-287">انتقل إلى **إدارة المستودعات \> إعداد \> عمل \> قوالب العمل**.</span><span class="sxs-lookup"><span data-stu-id="0a551-287">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="0a551-288">قم بتعيين الحقل **نوع أمر العمل** إلى *أوامر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="0a551-288">Set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="0a551-289">في شبكة **النظرة العامة**، ابحث عن وحدد قالب العمل الذي يجب استخدامه لتعبئة الأوامر الفردية لكل حاوية.</span><span class="sxs-lookup"><span data-stu-id="0a551-289">In the **Overview** grid, find and select the work template that should be used for packing single orders per container.</span></span> <span data-ttu-id="0a551-290">بالنسبة لهذا السيناريو، حدد قالب **63 انتقاء إلى الحاوية**.</span><span class="sxs-lookup"><span data-stu-id="0a551-290">For this scenario, select the **63 Pick to container** template.</span></span>
1. <span data-ttu-id="0a551-291">في جزء الإجراءات، حدد **تحرير استعلام**.</span><span class="sxs-lookup"><span data-stu-id="0a551-291">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="0a551-292">يظهر مربع حوار محرر Power Query القياسية.</span><span class="sxs-lookup"><span data-stu-id="0a551-292">A standard query editor dialog box appears.</span></span> <span data-ttu-id="0a551-293">في علامة التبويب **فرز**، قم بتعيين البنود التالية:</span><span class="sxs-lookup"><span data-stu-id="0a551-293">On the **Sorting** tab, add the following lines:</span></span>

    - <span data-ttu-id="0a551-294">السطر 1:</span><span class="sxs-lookup"><span data-stu-id="0a551-294">Line 1:</span></span>

        - <span data-ttu-id="0a551-295">**الجدول:** *حركات العمل المؤقتة*</span><span class="sxs-lookup"><span data-stu-id="0a551-295">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="0a551-296">**الجدول المشتق:** *حركات العمل المؤقتة*</span><span class="sxs-lookup"><span data-stu-id="0a551-296">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="0a551-297">**الحقل:** *معرف الشحنة*</span><span class="sxs-lookup"><span data-stu-id="0a551-297">**Field:** *Shipment ID*</span></span>
        - <span data-ttu-id="0a551-298">**اتجاه البحث:** *تصاعدي*</span><span class="sxs-lookup"><span data-stu-id="0a551-298">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="0a551-299">السطر 2:</span><span class="sxs-lookup"><span data-stu-id="0a551-299">Line 2:</span></span>

        - <span data-ttu-id="0a551-300">**الجدول:** *حركات العمل المؤقتة*</span><span class="sxs-lookup"><span data-stu-id="0a551-300">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="0a551-301">**الجدول المشتق:** *حركات العمل المؤقتة*</span><span class="sxs-lookup"><span data-stu-id="0a551-301">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="0a551-302">**الحقل:** *رقم الأمر*</span><span class="sxs-lookup"><span data-stu-id="0a551-302">**Field:** *Order number*</span></span>
        - <span data-ttu-id="0a551-303">**اتجاه البحث:** *تصاعدي*</span><span class="sxs-lookup"><span data-stu-id="0a551-303">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="0a551-304">السطر 3:</span><span class="sxs-lookup"><span data-stu-id="0a551-304">Line 3:</span></span>

        - <span data-ttu-id="0a551-305">**الجدول:** *حركات العمل المؤقتة*</span><span class="sxs-lookup"><span data-stu-id="0a551-305">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="0a551-306">**الجدول المشتق:** *حركات العمل المؤقتة*</span><span class="sxs-lookup"><span data-stu-id="0a551-306">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="0a551-307">**الحقل:** *معرف الحاوية*</span><span class="sxs-lookup"><span data-stu-id="0a551-307">**Field:** *Container ID*</span></span>
        - <span data-ttu-id="0a551-308">**اتجاه البحث:** *تصاعدي*</span><span class="sxs-lookup"><span data-stu-id="0a551-308">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="0a551-309">حدد **موافق** لإغلاق مربع حوار محرر الاستعلام.</span><span class="sxs-lookup"><span data-stu-id="0a551-309">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="0a551-310">تتلقى الرسالة التالية: "ستتم إعادة تعيين التجميع، هل تريد المتابعة؟"</span><span class="sxs-lookup"><span data-stu-id="0a551-310">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="0a551-311">للمتابعة، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="0a551-311">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="0a551-312">في حين أنه لا يزال يتم تحديد القالب **انتقاء للحاوية 63**، حدد **فواصل رأس العمل** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="0a551-312">While the **63 Pick to container** template is still selected, select **Work header breaks** on the Action Pane.</span></span>

    <span data-ttu-id="0a551-313">ستقوم الآن بتطبيق الإعدادات لقطع العمل بحيث يتم ربط كل حاوية في الأمر بأمر عمل واحد.</span><span class="sxs-lookup"><span data-stu-id="0a551-313">You will now apply settings to break the work so that each container in the order is linked to one work order.</span></span>

1. <span data-ttu-id="0a551-314">حدد خانة الاختيار **‬‏‫التجميع حسب هذا الحقل** لكل صف في الصفحة **فواصل رأس العمل** (**معرف الشحنة** و **رقم الأمر** و **معرف الحاوية**).</span><span class="sxs-lookup"><span data-stu-id="0a551-314">Select the **Group by this field** checkbox for each row on the **Work header breaks** page (**Shipment ID**, **Order number**, and **Container ID**).</span></span>
1. <span data-ttu-id="0a551-315">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0a551-315">Close the page.</span></span>

### <a name="set-up-shipment-consolidation-policies"></a><span data-ttu-id="0a551-316">إعداد سياسات دمج الشحنات</span><span class="sxs-lookup"><span data-stu-id="0a551-316">Set up shipment consolidation policies</span></span>

<span data-ttu-id="0a551-317">اتبع هذه الخطوات لإعداد سياسة دمج الشحن.</span><span class="sxs-lookup"><span data-stu-id="0a551-317">To set up a shipment consolidation policy, follow these steps.</span></span>

1. <span data-ttu-id="0a551-318">انتقل إلى **إدارة المستودعات \> الإعداد \> الإصدار إلى المستودع \> نُهج دمج الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="0a551-318">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="0a551-319">في جزء القائمة، قم بتعيين الحقل **نوع السياسة** إلى *أوامر المبيعات*.</span><span class="sxs-lookup"><span data-stu-id="0a551-319">In the list pane, set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="0a551-320">حدد السياسة **الافتراضية** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="0a551-320">Select the **Default** policy in the list.</span></span>
1. <span data-ttu-id="0a551-321">في جزء الإجراءات، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="0a551-321">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="0a551-322">في علامة التبويب السريعة **حقول الدمج**، في قائمة **الحقول المحددة**، حدد الصف الذي يتم فيه تعيين حقل **اسم الحقل** إلى *رقم الأمر*.</span><span class="sxs-lookup"><span data-stu-id="0a551-322">On the **Consolidation fields** FastTab, in the **Selected fields** list, select the row where the **Field name** field is set to *Order number*.</span></span>
1. <span data-ttu-id="0a551-323">حدد زر **إزالة** ![سهم لليسار](media/backward-button.png) لنقل الحقل إلى قائمة **الحقول المتبقية**.</span><span class="sxs-lookup"><span data-stu-id="0a551-323">Select the **Remove** button ![Left arrow](media/backward-button.png) to move the field to the **Remaining fields** list.</span></span>
1. <span data-ttu-id="0a551-324">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="0a551-324">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-physical-dimensions-for-the-product"></a><span data-ttu-id="0a551-325">إعداد الأبعاد الفعلية للمنتج</span><span class="sxs-lookup"><span data-stu-id="0a551-325">Set up physical dimensions for the product</span></span>

<span data-ttu-id="0a551-326">لإعداد الأبعاد الفعلية للمنتجات التي سيتم استخدامها في هذا السيناريو ، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0a551-326">To set up physical dimensions for the products that will be used in this scenario, follow these steps.</span></span>

1. <span data-ttu-id="0a551-327">انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.</span><span class="sxs-lookup"><span data-stu-id="0a551-327">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="0a551-328">حدد المنتج الذي يتم فيه تعيين الحقل **رقم الصنف** إلى *A0001*.</span><span class="sxs-lookup"><span data-stu-id="0a551-328">Select the product where the **Item number** field is set to *A0001*.</span></span>
1. <span data-ttu-id="0a551-329">في جزء الإجراءات، في علامة التبويب **إدارة المخزون**، في مجموعة **المستودعات**، حدد **الأبعاد الفعلية**.</span><span class="sxs-lookup"><span data-stu-id="0a551-329">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="0a551-330">في الصفحة **الأبعاد الفعلية**، يجب الاطلاع على البند التالي في الشبكة:</span><span class="sxs-lookup"><span data-stu-id="0a551-330">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="0a551-331">**الوحدة:** *قطع*</span><span class="sxs-lookup"><span data-stu-id="0a551-331">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="0a551-332">**الوزن الإجمالي:** *3.00*</span><span class="sxs-lookup"><span data-stu-id="0a551-332">**Gross weight:** *3.00*</span></span>
    - <span data-ttu-id="0a551-333">**العرض:** *2.00*</span><span class="sxs-lookup"><span data-stu-id="0a551-333">**Width:** *2.00*</span></span>
    - <span data-ttu-id="0a551-334">**العمق:** *2.00*</span><span class="sxs-lookup"><span data-stu-id="0a551-334">**Depth:** *2.00*</span></span>
    - <span data-ttu-id="0a551-335">**الارتفاع:** *4.00*</span><span class="sxs-lookup"><span data-stu-id="0a551-335">**Height:** *4.00*</span></span>
    - <span data-ttu-id="0a551-336">**الحجم:** *16.00*</span><span class="sxs-lookup"><span data-stu-id="0a551-336">**Volume:** *16.00*</span></span>

1. <span data-ttu-id="0a551-337">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0a551-337">Close the page.</span></span>
1. <span data-ttu-id="0a551-338">حدد المنتج الذي يتم فيه تعيين الحقل **رقم الصنف** إلى *A0002*.</span><span class="sxs-lookup"><span data-stu-id="0a551-338">Select the product where the **Item number** field is set to *A0002*.</span></span>
1. <span data-ttu-id="0a551-339">في جزء الإجراءات، في علامة التبويب **إدارة المخزون**، في مجموعة **المستودعات**، حدد **الأبعاد الفعلية**.</span><span class="sxs-lookup"><span data-stu-id="0a551-339">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="0a551-340">في الصفحة **الأبعاد الفعلية**، يجب الاطلاع على البند التالي في الشبكة:</span><span class="sxs-lookup"><span data-stu-id="0a551-340">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="0a551-341">**الوحدة:** *قطع*</span><span class="sxs-lookup"><span data-stu-id="0a551-341">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="0a551-342">**الوزن الإجمالي:** *4.00*</span><span class="sxs-lookup"><span data-stu-id="0a551-342">**Gross weight:** *4.00*</span></span>
    - <span data-ttu-id="0a551-343">**العرض:** *3.00*</span><span class="sxs-lookup"><span data-stu-id="0a551-343">**Width:** *3.00*</span></span>
    - <span data-ttu-id="0a551-344">**العمق:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="0a551-344">**Depth:** *1.00*</span></span>
    - <span data-ttu-id="0a551-345">**الارتفاع:** *3.00*</span><span class="sxs-lookup"><span data-stu-id="0a551-345">**Height:** *3.00*</span></span>
    - <span data-ttu-id="0a551-346">**الحجم:** *9.00*</span><span class="sxs-lookup"><span data-stu-id="0a551-346">**Volume:** *9.00*</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="0a551-347">إنشاء أمر مبيعات 1</span><span class="sxs-lookup"><span data-stu-id="0a551-347">Create sales order 1</span></span>

<span data-ttu-id="0a551-348">لإنشاء أمر مبيعات، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="0a551-348">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="0a551-349">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="0a551-349">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="0a551-350">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0a551-350">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0a551-351">يظهر مربع حوار لإنشاء أمر مبيعات جديد.</span><span class="sxs-lookup"><span data-stu-id="0a551-351">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="0a551-352">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="0a551-352">Set the following values:</span></span>

    - <span data-ttu-id="0a551-353">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="0a551-353">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="0a551-354">**المستودع:** *63*</span><span class="sxs-lookup"><span data-stu-id="0a551-354">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="0a551-355">حدد **موافق** لإنشاء أمر مبيعات وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="0a551-355">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="0a551-356">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="0a551-356">The new sales order is opened.</span></span> <span data-ttu-id="0a551-357">في علامة التبويب السريعة **سطور أمر المبيعات**، أضف سطور المبيعات التالية:</span><span class="sxs-lookup"><span data-stu-id="0a551-357">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="0a551-358">السطر 1:</span><span class="sxs-lookup"><span data-stu-id="0a551-358">Line 1:</span></span>

        - <span data-ttu-id="0a551-359">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="0a551-359">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="0a551-360">**الكمية:** *2*</span><span class="sxs-lookup"><span data-stu-id="0a551-360">**Quantity:** *2*</span></span>

    - <span data-ttu-id="0a551-361">السطر 2:</span><span class="sxs-lookup"><span data-stu-id="0a551-361">Line 2:</span></span>

        - <span data-ttu-id="0a551-362">**رقم الصنف:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="0a551-362">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="0a551-363">**الكمية:** *2*</span><span class="sxs-lookup"><span data-stu-id="0a551-363">**Quantity:** *2*</span></span>

1. <span data-ttu-id="0a551-364">حدد البند الأول، ثم حدد **المخزون \> الحجز**.</span><span class="sxs-lookup"><span data-stu-id="0a551-364">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="0a551-365">في صفحة **الحجز**، حدد **حجز دفعة**.</span><span class="sxs-lookup"><span data-stu-id="0a551-365">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="0a551-366">ثم أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0a551-366">Then close the page.</span></span>
1. <span data-ttu-id="0a551-367">كرر الخطوتين السابقتين للسطر الثاني.</span><span class="sxs-lookup"><span data-stu-id="0a551-367">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="0a551-368">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0a551-368">Close the page.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="0a551-369">إنشاء أمر مبيعات 2</span><span class="sxs-lookup"><span data-stu-id="0a551-369">Create sales order 2</span></span>

<span data-ttu-id="0a551-370">لإنشاء أمر مبيعات ثاني، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="0a551-370">To create a second sales order, follow these steps.</span></span>

1. <span data-ttu-id="0a551-371">انتقل إلى **المبيعات والتسويق \> أوامر المبيعات \> كافة أوامر المبيعات‬**.</span><span class="sxs-lookup"><span data-stu-id="0a551-371">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="0a551-372">في جزء الإجراء، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="0a551-372">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="0a551-373">يظهر مربع حوار لإنشاء أمر مبيعات جديد.</span><span class="sxs-lookup"><span data-stu-id="0a551-373">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="0a551-374">قم بتعيين القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="0a551-374">Set the following values:</span></span>

    - <span data-ttu-id="0a551-375">**حساب العميل:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="0a551-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="0a551-376">**المستودع:** *63*</span><span class="sxs-lookup"><span data-stu-id="0a551-376">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="0a551-377">حدد **موافق** لإنشاء أمر مبيعات وإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="0a551-377">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="0a551-378">يتم فتح أمر المبيعات الجديد.</span><span class="sxs-lookup"><span data-stu-id="0a551-378">The new sales order is opened.</span></span> <span data-ttu-id="0a551-379">في علامة التبويب السريعة **سطور أمر المبيعات**، أضف سطور المبيعات التالية:</span><span class="sxs-lookup"><span data-stu-id="0a551-379">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="0a551-380">السطر 1:</span><span class="sxs-lookup"><span data-stu-id="0a551-380">Line 1:</span></span>

        - <span data-ttu-id="0a551-381">**رقم الصنف:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="0a551-381">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="0a551-382">**الكمية:** *4*</span><span class="sxs-lookup"><span data-stu-id="0a551-382">**Quantity:** *4*</span></span>

    - <span data-ttu-id="0a551-383">السطر 2:</span><span class="sxs-lookup"><span data-stu-id="0a551-383">Line 2:</span></span>

        - <span data-ttu-id="0a551-384">**رقم الصنف:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="0a551-384">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="0a551-385">**الكمية:** *4*</span><span class="sxs-lookup"><span data-stu-id="0a551-385">**Quantity:** *4*</span></span>

1. <span data-ttu-id="0a551-386">حدد البند الأول، ثم حدد **المخزون \> الحجز**.</span><span class="sxs-lookup"><span data-stu-id="0a551-386">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="0a551-387">في صفحة **الحجز**، حدد **حجز دفعة**.</span><span class="sxs-lookup"><span data-stu-id="0a551-387">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="0a551-388">ثم أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0a551-388">Then close the page.</span></span>
1. <span data-ttu-id="0a551-389">كرر الخطوتين السابقتين للسطر الثاني.</span><span class="sxs-lookup"><span data-stu-id="0a551-389">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="0a551-390">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="0a551-390">Close the page.</span></span>

### <a name="create-the-load"></a><span data-ttu-id="0a551-391">إنشاء الحمل</span><span class="sxs-lookup"><span data-stu-id="0a551-391">Create the load</span></span>

<span data-ttu-id="0a551-392">لإنشاء حمل لكل أمر قمت بإنشائه لهذا السيناريو ثم إصداره إلى المستودع، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0a551-392">To create a load for each order that you created for this scenario and then release it to the warehouse, follow these steps.</span></span>

1. <span data-ttu-id="0a551-393">انتقل إلى **إدارة المستودعات \> الأحمال \> منضدة عمل تخطيط الحِمل‬**.</span><span class="sxs-lookup"><span data-stu-id="0a551-393">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="0a551-394">من علامة التبويب **بنود المبيعات**، ابحث عن كافة بنود أمر المبيعات وحددها من أوامر المبيعات التي قمت بإنشائها لهذا السيناريو.</span><span class="sxs-lookup"><span data-stu-id="0a551-394">On the **Sales lines** tab, find and select all the sales order lines from the sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="0a551-395">في جزء الإجراءات، في علامة التبويب **العرض والطلب**، في مجموعة **إضافة**، حدد **إلى حمل جديد**.</span><span class="sxs-lookup"><span data-stu-id="0a551-395">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span> <span data-ttu-id="0a551-396">تتم إضافة بنود الأوامر المحددة إلى تحميل جديد.</span><span class="sxs-lookup"><span data-stu-id="0a551-396">The selected order lines are added to a new load.</span></span>
1. <span data-ttu-id="0a551-397">في مربع الحوار **تعيين قالب الحمل**، في الحقل **معرف قالب الحمل**، حدد قالب حمل، مثل *حاوية 40*.</span><span class="sxs-lookup"><span data-stu-id="0a551-397">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *40' Container*.</span></span>
1. <span data-ttu-id="0a551-398">حدد **موافق** لإغلاق مربع الحوار.</span><span class="sxs-lookup"><span data-stu-id="0a551-398">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="0a551-399">في قسم **الأحمال**، ابحث عن الحمل الذي أنشأته للتو وحدده.</span><span class="sxs-lookup"><span data-stu-id="0a551-399">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="0a551-400">حدد **إصدار \> إصدار إلى مستودع**.</span><span class="sxs-lookup"><span data-stu-id="0a551-400">Select **Release \> Release to warehouse**.</span></span>
1. <span data-ttu-id="0a551-401">في مربع الحوار **إصدار إلى المستودع**، حدد **موافق** لإصدار الحمل المحدد إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="0a551-401">In the **Release to warehouse** dialog box, select **OK** to release the selected load to the warehouse.</span></span>

### <a name="verify-the-shipments-and-containers"></a><span data-ttu-id="0a551-402">التحقق من الشحنات والحاويات</span><span class="sxs-lookup"><span data-stu-id="0a551-402">Verify the shipments and containers</span></span>

<span data-ttu-id="0a551-403">يتيح لك الإجراء التالي التحقق من الشحنات التي تم إنشاؤها.</span><span class="sxs-lookup"><span data-stu-id="0a551-403">The following procedure lets you verify the shipments that have been created.</span></span> <span data-ttu-id="0a551-404">استخدم هذا الإجراء لمراجعة الأمر الذي قمت بإنشائه لهذا السيناريو، وذلك للتأكد من حصولك على النتائج المتوقعة.</span><span class="sxs-lookup"><span data-stu-id="0a551-404">Use it to review the order that you created for this scenario, to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="0a551-405">انتقل إلى **إدارة المستودعات \> الشحنات \> جميع الشحنات**.</span><span class="sxs-lookup"><span data-stu-id="0a551-405">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="0a551-406">ابحث عن الشحنة التي تم إنشائها للحمل الذي قمت بإصداره للتو وحددها.</span><span class="sxs-lookup"><span data-stu-id="0a551-406">Find and select the shipment that was created for the load that you just released.</span></span>
1. <span data-ttu-id="0a551-407">في جزء الإجراءات، في علامة تبويب **المواصلات**، وحدد **عرض الحاويات**.</span><span class="sxs-lookup"><span data-stu-id="0a551-407">On the Action Pane, on the **Transportation** tab, select **View containers**.</span></span>
1. <span data-ttu-id="0a551-408">تأكد من أنه تم تعبئة الأصناف الواردة من أوامر المبيعات إلى حاويتين مختلفتين.</span><span class="sxs-lookup"><span data-stu-id="0a551-408">Confirm that the items from the sales orders were containerized into two different containers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0a551-409">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0a551-409">Additional resources</span></span>

- [<span data-ttu-id="0a551-410">التعبئة في حاويات</span><span class="sxs-lookup"><span data-stu-id="0a551-410">Containerization</span></span>](wave-containerization.md)
