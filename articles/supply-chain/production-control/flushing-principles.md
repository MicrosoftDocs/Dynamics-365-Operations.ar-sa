---
title: "مبادئ التفريغ"
description: "يصف هذا الموضوع مبادئ التفريغ الأربعة التي يتم استخدامها لاستهلاك المواد الخام."
author: johanhoffmann
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgShopSupervisorReleaseOrders
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: ba426692e2e404ab75e5730b8205115fc59e402f
ms.openlocfilehash: f5fc4db479852ffac5f2b3401a0c1bd92c35a7cb
ms.contentlocale: ar-sa
ms.lasthandoff: 02/08/2018

---

# <a name="controlling-raw-material-consumption-by-using-flushing-principles"></a><span data-ttu-id="1b337-103">التحكم استهلاك المادة الخام عن طريق استخدام قواعد التفريغ</span><span class="sxs-lookup"><span data-stu-id="1b337-103">Controlling raw material consumption by using flushing principles</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1b337-104">تعكس مبادئ التفريغ خطط الاستهلاك المختلفة للمواد الخام المستخدمة في عمليات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="1b337-104">The flushing principles reflect different consumption strategies for raw materials that are used in production processes.</span></span> <span data-ttu-id="1b337-105">يعتبر الاستهلاك بمثابة العملية التي تخصم المواد من المخزون الفعلي وتعين قيمة المواد المستهلكة إلى **الأعمال تحت التنفيذ** (WIP) لأوامر الإنتاج والأوامر الدفعية‬.</span><span class="sxs-lookup"><span data-stu-id="1b337-105">Consumption is the process that deducts material from the on-hand inventory and sets the value of the consumed materials to **Work in progress** (WIP) for production orders and batch orders.</span></span> <span data-ttu-id="1b337-106">تستهلك المواد الخام عادة من موقع تم تكوينه للعملية التي تسهلك المواد.</span><span class="sxs-lookup"><span data-stu-id="1b337-106">Raw materials are usually consumed from a location that is configured for the process that consumes the material.</span></span> <span data-ttu-id="1b337-107">يعرف هذا الموقع بأنه موقع إدخال الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="1b337-107">This location is known as the production input location.</span></span>

<span data-ttu-id="1b337-108">تُنقل المواد، قبل استهلاكها، إلى موقع الإدخال.</span><span class="sxs-lookup"><span data-stu-id="1b337-108">Before material consumption, the materials are moved to the input location.</span></span> <span data-ttu-id="1b337-109">يبين الرسم التوضيحي التالي العملية.</span><span class="sxs-lookup"><span data-stu-id="1b337-109">The following illustration shows the process.</span></span>

<span data-ttu-id="1b337-110">[![scenario4a](./media/scenario4a.png)](./media/scenario4a.png)</span><span class="sxs-lookup"><span data-stu-id="1b337-110">[![scenario4a](./media/scenario4a.png)](./media/scenario4a.png)</span></span>

1. <span data-ttu-id="1b337-111">مستودع المواد</span><span class="sxs-lookup"><span data-stu-id="1b337-111">Material warehouse</span></span>
2. <span data-ttu-id="1b337-112">انتقاء المواد الخام</span><span class="sxs-lookup"><span data-stu-id="1b337-112">Raw material picking</span></span>
3. <span data-ttu-id="1b337-113">موقع إدخال الإنتاج</span><span class="sxs-lookup"><span data-stu-id="1b337-113">Production input location</span></span>
4. <span data-ttu-id="1b337-114">استهلاك المواد الخام</span><span class="sxs-lookup"><span data-stu-id="1b337-114">Raw material consumption</span></span>
5. <span data-ttu-id="1b337-115">عملية الإنتاج</span><span class="sxs-lookup"><span data-stu-id="1b337-115">Production process</span></span>

<span data-ttu-id="1b337-116">يخضع استهلاك المواد لمبادئ التفريغ الأربعة التالية:</span><span class="sxs-lookup"><span data-stu-id="1b337-116">Material consumption is controlled by the following four flushing principles:</span></span>

- <span data-ttu-id="1b337-117">يدوي</span><span class="sxs-lookup"><span data-stu-id="1b337-117">Manual</span></span>
- <span data-ttu-id="1b337-118">البدء</span><span class="sxs-lookup"><span data-stu-id="1b337-118">Start</span></span>
- <span data-ttu-id="1b337-119">إنهاء</span><span class="sxs-lookup"><span data-stu-id="1b337-119">Finish</span></span>
- <span data-ttu-id="1b337-120">متوفر في الموقع</span><span class="sxs-lookup"><span data-stu-id="1b337-120">Available at location</span></span>

<span data-ttu-id="1b337-121">يتم تكوين مبادئ التفريغ في تدرج هرمي للقيم الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="1b337-121">The flushing principles are configured in a hierarchy of default values.</span></span> <span data-ttu-id="1b337-122">يبدأ التدرج الهرمي عند المنتج الصادر، حيث تكون قيمة مبدأ التفريغ **البدء**.</span><span class="sxs-lookup"><span data-stu-id="1b337-122">The hierarchy starts at the released product, where the flushing principle has the value **Start**.</span></span> <span data-ttu-id="1b337-123">في بند قائمة مكونات الصنف (BOM) أو بند المعادلة، يمكن تجاوز مبدأ التفريغ من المنتج.</span><span class="sxs-lookup"><span data-stu-id="1b337-123">On the bill of materials (BOM) or formula line, the flushing principle from the product can be overridden.</span></span> <span data-ttu-id="1b337-124">يتم استخدام مبدأ التفريغ الافتراضي في بنود قائمة مكونات الصنف أو بنود معادلة الأوامر الدفعية من المنتج أو القيمة التي تم تجاوزها في قائمة مكونات الصنف أو المعادلات.</span><span class="sxs-lookup"><span data-stu-id="1b337-124">The default flushing principle on the production BOM lines or batch order formula lines is taken from the product or the overridden value on the BOM or formulas.</span></span>

## <a name="description-of-the-flushing-principles"></a><span data-ttu-id="1b337-125">وصف مبادئ التفريغ</span><span class="sxs-lookup"><span data-stu-id="1b337-125">Description of the flushing principles</span></span>

### <a name="manual"></a><span data-ttu-id="1b337-126">يدوي</span><span class="sxs-lookup"><span data-stu-id="1b337-126">Manual</span></span>
<span data-ttu-id="1b337-127">يشير مبدأ التفريغ اليدوي إلى أن تسجيل المواد الخام عبارة عن عملية يدوية.</span><span class="sxs-lookup"><span data-stu-id="1b337-127">The Manual flushing principle indicates that the registration of material consumption is a manual operation.</span></span> <span data-ttu-id="1b337-128">يعتبر المبدأ مناسبًا إذا، على سبيل المثال، أردت أن تكون قادرًا على تعقب الوقت، ويجب أن تؤخذ في الحسبان كمية أرقام الدُفعات المستهلكة أو الأرقام التسلسلية، لأغراض التعقب.</span><span class="sxs-lookup"><span data-stu-id="1b337-128">This principle is relevant if, for example, you want to be able to track time, and the quantity of consumed batch numbers or serial numbers must be accounted for, for tracking purposes.</span></span> <span data-ttu-id="1b337-129">يتم تسجيل الاستهلاك اليدوي في دفتر يومية قائمة انتقاء الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="1b337-129">Manual consumption is registered in a production picking list journal.</span></span> <span data-ttu-id="1b337-130">بالنسبة إلى الأصناف التي تم تمكينها لعمليات المستودع المتقدمة، يمكن تطبيق تدفق محمول باليد.</span><span class="sxs-lookup"><span data-stu-id="1b337-130">For items that are enabled for advanced warehouse processes, a hand-held flow can be applied.</span></span>

### <a name="start"></a><span data-ttu-id="1b337-131">البدء</span><span class="sxs-lookup"><span data-stu-id="1b337-131">Start</span></span>
<span data-ttu-id="1b337-132">يشير مبدأ التفريغ "البدء" إلى أن المواد ستُستهلك تلقائيًا عند بدء أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="1b337-132">The Start flushing principle indicates that material will be automatically consumed when the production order is started.</span></span> <span data-ttu-id="1b337-133">ويكون مقدار المواد المستهلكة متناسبًا مع الكمية التي بدأ إنتاجها.</span><span class="sxs-lookup"><span data-stu-id="1b337-133">The amount of material that is consumed is proportional to the quantity that is started.</span></span> <span data-ttu-id="1b337-134">عند استخدام مبدأ التفريغ "البدء" مع نظام تنفيذ التصنيع، يمكن أيضًا استخدامه لتفريغ المواد عند بدء عملية أو وظيفة عملية.</span><span class="sxs-lookup"><span data-stu-id="1b337-134">When the Start flushing principle is used together with the manufacturing execution system, it can also be used to flush materials when an operation or a process job is started.</span></span> <span data-ttu-id="1b337-135">يكون هذا المبدأ مناسبًا، إذا، على سبيل المثال، كان الاختلاف في الاستهلاك منخفضًا أو إذا كانت المواد عبارة عن مواد منخفضة القيمة أو لا توجد متطلبات خاصة بالتعقب أو في حال وجود وقت تشغيل قصير على العمليات.</span><span class="sxs-lookup"><span data-stu-id="1b337-135">This principle is relevant if, for example, the variance in the consumption is low, the materials are low-value materials, there are no tracking requirements, or there is a short run time on operations.</span></span> 

### <a name="finish"></a><span data-ttu-id="1b337-136">إنهاء</span><span class="sxs-lookup"><span data-stu-id="1b337-136">Finish</span></span>
<span data-ttu-id="1b337-137">يشير مبدأ التفريغ "إنهاء" إلى أن المواد ستُستهلك تلقائيًا عندما يتم الإعلام عن أمر الإنتاج كمنتهٍ، أو عند تسجيل عملية تم إعدادها لاستهلاك المواد كمكتملة.</span><span class="sxs-lookup"><span data-stu-id="1b337-137">The Finish flushing principle indicates that material will be automatically consumed when the production order is reported as finished, or when an operation that is set up to consume the materials is registered as completed.</span></span> <span data-ttu-id="1b337-138">ويكون مقدار المواد المستهلكة متناسبًا مع الكمية التي تم الإعلام عنها كمنتهية.</span><span class="sxs-lookup"><span data-stu-id="1b337-138">The amount of material that is consumed is proportional to the quantity that is reported as finished.</span></span> <span data-ttu-id="1b337-139">عند استخدام مبدأ التفريغ "إنهاء" مع نظام تنفيذ التصنيع، يمكن أيضًا استخدامه لتفريغ المواد عند اكتمال عملية أو وظيفة عملية.</span><span class="sxs-lookup"><span data-stu-id="1b337-139">When the Finish flushing principle is used together with the manufacturing execution system, it can also be used to flush materials when an operation or a process job is completed.</span></span> <span data-ttu-id="1b337-140">يُعتبر هذا المبدأ مناسبًا في الحالات نفسها لمبدأ "البدء".</span><span class="sxs-lookup"><span data-stu-id="1b337-140">This principle is relevant in the same situations as the Start principle.</span></span> <span data-ttu-id="1b337-141">ومع ذلك، فإن مبدأ التفريغ "إنهاء" يتعلق بالعملية التي لديها وقت تشغيل أطول، حيث يجب ألا يتم تعيين المواد إلى الأعمال تحت التنفيذ (WIP) قبل اكتمال العملية.</span><span class="sxs-lookup"><span data-stu-id="1b337-141">However, the Finish principle is for operations that have a longer run time, where materials should not be set to WIP before the operation is completed.</span></span> 

### <a name="available-at-location"></a><span data-ttu-id="1b337-142">متوفر في الموقع</span><span class="sxs-lookup"><span data-stu-id="1b337-142">Available at location</span></span>
<span data-ttu-id="1b337-143">يشير مبدأ التفريغ "متوفر في الموقع" إلى أن المواد ستُستهلك تلقائيًا عندما يتم تسجيلها كمواد منتقاة للإنتاج.</span><span class="sxs-lookup"><span data-stu-id="1b337-143">The Available at location flushing principle indicates that the material will be automatically consumed when it's registered as picked for production.</span></span> <span data-ttu-id="1b337-144">يتم تسجيل المواد كمنتقاة من الموقع عند اكتمال العمل المتعلق بانتقاء المواد أو عندما تتوفر المواد في موقع إدخال الإنتاج ويتم إصدار بند المواد إلى المستودع.</span><span class="sxs-lookup"><span data-stu-id="1b337-144">The material is registered as picked from location when work for the raw material picking is completed, or when material is available on the production input location and the material line is released to the warehouse.</span></span> <span data-ttu-id="1b337-145">يتم ترحيل قائمة الانتقاء التي يتم إنشاؤها خلال العملية في وظيفة دفعية.</span><span class="sxs-lookup"><span data-stu-id="1b337-145">The picking list that is generated during the process is posted in a batch job.</span></span> <span data-ttu-id="1b337-146">يُعتبر هذا المبدأ مناسبًا، إذا، على سبيل المثال، كان لديك الكثير من أنشطة الانتقاء في مقابل أمر إنتاج واحد.</span><span class="sxs-lookup"><span data-stu-id="1b337-146">This principle is relevant if, for example, you have many picking activities against one production order.</span></span> <span data-ttu-id="1b337-147">في هذه الحالة، لا تحتاج إلى تحديث قائمة الانتقاء يدويًا، ويمكنك الحصول على طريقة عرض حالية لرصيد الأعمال تحت التنفيذ (WIP).</span><span class="sxs-lookup"><span data-stu-id="1b337-147">In this case, you don't have to update the picking list manually, and you can get a current view of the WIP balance.</span></span>

