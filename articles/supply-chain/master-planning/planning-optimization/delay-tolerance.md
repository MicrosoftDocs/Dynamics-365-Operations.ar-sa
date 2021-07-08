---
title: تفاوت التأخير (الأيام السالبة)
description: يوفر هذا الموضوع معلومات حول حساب تفاوت التأخير وكيفية تأثيره على إنشاء الأمر المخطط في تحسين التخطيط.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306453"
---
# <a name="delay-tolerance-negative-days"></a><span data-ttu-id="6c9e7-103">تفاوت التأخير (الأيام السالبة)</span><span class="sxs-lookup"><span data-stu-id="6c9e7-103">Delay tolerance (negative days)</span></span>

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="6c9e7-104">تتيح وظيفة تفاوت التأخير إمكانية تحسين التخطيط لاعتبار قيمة **الأيام السالبة** التي يتم تعيينها لمجموعات التغطية.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-104">The delay tolerance functionality enables Planning Optimization to consider the **Negative days** value that is set for coverage groups.</span></span> <span data-ttu-id="6c9e7-105">ويستخدم لتمديد فترة تفاوت التأخير التي يتم تطبيقها أثناء التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-105">It's used to extend the delay tolerance period that is applied during master planning.</span></span> <span data-ttu-id="6c9e7-106">بهذه الطريقة، يمكنك تجنب إنشاء أوامر توريد جديدة إذا كان التوريد الموجود قادرًا على تغطية الطلب بعد فترة تأخير قصيرة.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-106">In this way, you can avoid creating new supply orders if existing supply will be able to cover the demand after a short delay.</span></span> <span data-ttu-id="6c9e7-107">إن الغرض من الوظيفة هو تحديد ما إذا كان من المنطقي إنشاء أمر توريد جديد لطلب معين.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-107">The purpose of the functionality is to determine whether it makes sense to create a new supply order for a given demand.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="6c9e7-108">تشغيل الميزة في النظام</span><span class="sxs-lookup"><span data-stu-id="6c9e7-108">Turn on the feature in your system</span></span>

<span data-ttu-id="6c9e7-109">لجعل وظيفة تفاوت التأخير متوفرة في النظام، انتقل إلى [إدارة الميزات](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)، وتشغيل الميزة *‏‫الأيام السالبة لتحسين التخطيط‬‬*.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-109">To make the delay tolerance functionality available in your system, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Negative days for Planning Optimization* feature.</span></span>

## <a name="delay-tolerance-in-planning-optimization"></a><span data-ttu-id="6c9e7-110">تفاوت التأخير في تحسين التخطيط</span><span class="sxs-lookup"><span data-stu-id="6c9e7-110">Delay tolerance in Planning Optimization</span></span>

<span data-ttu-id="6c9e7-111">يمثل تفاوت التأخير عدد الأيام التي تتجاوز الحد الأدنى لوقت الإنتاج الذي ترغب في انتظاره قبل تزويد الأمر الجديد عند تخطيط التوريد الموجود بالفعل.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-111">Delay tolerance represents the number of days beyond the lead time that you're willing to wait before you order new replenishment when existing supply is already planned.</span></span> <span data-ttu-id="6c9e7-112">يتم تحديد تفاوت التأخير باستخدام أيام التقويم وليس أيام العمل.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-112">Delay tolerance is defined by using calendar days, not business days.</span></span>

<span data-ttu-id="6c9e7-113">في وقت التخطيط الرئيسي، عند حساب النظام لتفاوت التأخير، فإنه يعتبر إعداد **الأيام السالبة**.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-113">At the time of master planning, when the system calculates the delay tolerance, it considers the **Negative days** setting.</span></span> <span data-ttu-id="6c9e7-114">يمكنك تحديد القيمة **الأيام السالبة** إما في الصفحة **مجموعات التغطية** أو الصفحة **تغطية الصنف**.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-114">You can set the **Negative days** value on either the **Coverage groups** page or the **Item coverage** page.</span></span>

<span data-ttu-id="6c9e7-115">يقوم النظام بربط حساب تفاوت التأخير بـ *بأقرب تاريخ تزويد*، والذي يساوي تاريخ اليوم مضافًا إليه الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-115">The system links the delay tolerance calculation to the *earliest replenishment date*, which equals today's date plus the lead time.</span></span> <span data-ttu-id="6c9e7-116">يتم حساب تفاوت التأخير باستخدام المعادلة التالية، حيث تجد *max()* أكبر قيمتين:</span><span class="sxs-lookup"><span data-stu-id="6c9e7-116">The delay tolerance is calculated by using following formula, where *max()* finds the larger of two values:</span></span>

<span data-ttu-id="6c9e7-117">*الحد الأقصى (أقرب تاريخ تزويد، تاريخ استحقاق الطلب)* – *تاريخ استحقاق الطلب* + *الأيام السالبة*</span><span class="sxs-lookup"><span data-stu-id="6c9e7-117">*max(Earliest replenishment date, Demand due date)* – *Demand due date* + *Negative days*</span></span>

<span data-ttu-id="6c9e7-118">تضمن هذه الصيغة ان التخطيط الرئيسي لا يقوم بإنشاء أوامر توريد جديده عند وجود توريد كاف اثناء وقت وصول المنتج.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-118">This formula ensures that master planning doesn't create new supply orders when enough supply exists during the product lead time.</span></span>

> [!NOTE]
> <span data-ttu-id="6c9e7-119">يستخدم حساب تفاوت التأخير في تحسين التخطيط دائمًا حساب الأيام السالبة الديناميكية من التخطيط الرئيسي المضمن.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-119">The delay tolerance calculation in Planning Optimization always uses the dynamic negative days calculation from built-in master planning.</span></span> <span data-ttu-id="6c9e7-120">لا يؤثر الإعداد **استخدام الأيام السالبة الديناميكية** في الصفحة **امعلمات التخطيط الرئيسية** على هذا السلوك.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-120">The **Use dynamic negative days** setting on the **Master planning parameters** page has no effect on this behavior.</span></span>

<span data-ttu-id="6c9e7-121">إذا كان التوريد الموجود يتضمن تأخير الطلب الأقل من أو يساوي الحد الأدنى لتفاوت التأخير، فإن تحسين التخطيط يرتبط بالتوريد الموجود بالطلب.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-121">If the existing supply implies a demand delay that is less than or equal to the calculated delay tolerance, Planning Optimization pegs existing supply with the demand.</span></span> <span data-ttu-id="6c9e7-122">في بعض الحالات، من الأفضل تأخير الطلب من الانتهاء بالتوريد الزائد.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-122">In some cases, it's better to delay the demand than to end up with oversupply.</span></span>

<span data-ttu-id="6c9e7-123">توفر الأقسام الفرعية التالية أمثلة تظهر كيفية تأثير التفاوت المسموح على إنشاء الأوامر المخططة في تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-123">The following subsections provide examples that show how delay tolerance affects the creation of planned orders in Planning Optimization.</span></span>

### <a name="example-1"></a><span data-ttu-id="6c9e7-124">مثال1</span><span class="sxs-lookup"><span data-stu-id="6c9e7-124">Example 1</span></span>

<span data-ttu-id="6c9e7-125">يتمتع المنتج بالتكوين التالي:</span><span class="sxs-lookup"><span data-stu-id="6c9e7-125">A product has the following configuration:</span></span>

- <span data-ttu-id="6c9e7-126">**الحد الأدنى لوقت الإنتاج:** *10*</span><span class="sxs-lookup"><span data-stu-id="6c9e7-126">**Lead time:** *10*</span></span>
- <span data-ttu-id="6c9e7-127">**الأيام السالبة:** *2*</span><span class="sxs-lookup"><span data-stu-id="6c9e7-127">**Negative days:** *2*</span></span>

<span data-ttu-id="6c9e7-128">بتوافر التوريد والطلب التاليين للمنتج:</span><span class="sxs-lookup"><span data-stu-id="6c9e7-128">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="6c9e7-129">**طلب اليوم:** أمر مبيعات لكمية قيمتها 10</span><span class="sxs-lookup"><span data-stu-id="6c9e7-129">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="6c9e7-130">**التوريد في غضون 12 يومًا:** أمر شراء بكمية قيمتها 10</span><span class="sxs-lookup"><span data-stu-id="6c9e7-130">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="6c9e7-131">يمكن أن يغطي التوريد الموجود الطلب خلال 12 يومًا، وتكون هذه الفترة مساوية لتفاوت التأخير.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-131">Existing supply can cover the demand within 12 days, and that period equals the delay tolerance.</span></span> <span data-ttu-id="6c9e7-132">وبالتالي، عند تشغيل التخطيط الرئيسي، لا يتم إنشاء أية أوامر مخططة.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-132">Therefore, when master planning runs, no planned orders are created.</span></span>

### <a name="example-2"></a><span data-ttu-id="6c9e7-133">مثال2</span><span class="sxs-lookup"><span data-stu-id="6c9e7-133">Example 2</span></span>

<span data-ttu-id="6c9e7-134">يتمتع المنتج بالتكوين التالي:</span><span class="sxs-lookup"><span data-stu-id="6c9e7-134">A product has the following configuration:</span></span>

- <span data-ttu-id="6c9e7-135">**الحد الأدنى لوقت الإنتاج:** *10*</span><span class="sxs-lookup"><span data-stu-id="6c9e7-135">**Lead time:** *10*</span></span>
- <span data-ttu-id="6c9e7-136">**الأيام السالبة:** *0*</span><span class="sxs-lookup"><span data-stu-id="6c9e7-136">**Negative days:** *0*</span></span>

<span data-ttu-id="6c9e7-137">بتوافر التوريد والطلب التاليين للمنتج:</span><span class="sxs-lookup"><span data-stu-id="6c9e7-137">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="6c9e7-138">**طلب اليوم:** أمر مبيعات لكمية قيمتها 10</span><span class="sxs-lookup"><span data-stu-id="6c9e7-138">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="6c9e7-139">**التوريد في غضون 12 يومًا:** أمر شراء بكمية قيمتها 10</span><span class="sxs-lookup"><span data-stu-id="6c9e7-139">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="6c9e7-140">يمكن أن يغطي التوريد الموجود الطلب فقط بعد مرور 12 يومًا.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-140">Existing supply can cover the demand only after 12 days.</span></span> <span data-ttu-id="6c9e7-141">ومع ذلك، فإن تفاوت التأخير هو 10 أيام.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-141">However, the delay tolerance is 10 days.</span></span> <span data-ttu-id="6c9e7-142">وبالتالي، عند تشغيل التخطيط الرئيسي، يتم إنشاء أمر مخطط لكمية 10.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-142">Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>

### <a name="example-3"></a><span data-ttu-id="6c9e7-143">المثال الثالث</span><span class="sxs-lookup"><span data-stu-id="6c9e7-143">Example 3</span></span>

<span data-ttu-id="6c9e7-144">يتمتع المنتج بالتكوين التالي:</span><span class="sxs-lookup"><span data-stu-id="6c9e7-144">A product has the following configuration:</span></span>

- <span data-ttu-id="6c9e7-145">**الحد الأدنى لوقت الإنتاج:** *10*</span><span class="sxs-lookup"><span data-stu-id="6c9e7-145">**Lead time:** *10*</span></span>
- <span data-ttu-id="6c9e7-146">**الأيام السالبة:** *2*</span><span class="sxs-lookup"><span data-stu-id="6c9e7-146">**Negative days:** *2*</span></span>

<span data-ttu-id="6c9e7-147">بتوافر التوريد والطلب التاليين للمنتج:</span><span class="sxs-lookup"><span data-stu-id="6c9e7-147">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="6c9e7-148">**طلب خلال 10 أيام:** أمر مبيعات لكمية قيمتها 10</span><span class="sxs-lookup"><span data-stu-id="6c9e7-148">**Demand in 11 days:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="6c9e7-149">**التوريد في غضون 14 يومًا:** أمر شراء بكمية قيمتها 10</span><span class="sxs-lookup"><span data-stu-id="6c9e7-149">**Supply in 14 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="6c9e7-150">يمكن أن يغطي التوريد الموجود الطلب فقط بعد مرور ثلاثة أيام.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-150">Existing supply can cover the demand only after three days.</span></span> <span data-ttu-id="6c9e7-151">ومع ذلك، فإن تفاوت التأخير هو يومين.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-151">However, the delay tolerance is two days.</span></span> <span data-ttu-id="6c9e7-152">(في هذه الحالة، يتضمن تفاوت التأخير اليومين السالبين فقط.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-152">(In this case, the delay tolerance includes only the two negative days.</span></span> <span data-ttu-id="6c9e7-153">لم يتم تضمين تاريخ الطلب لأنه بعد الحد الأدنى لوقت إنتاج المنتج.) وبالتالي، عند تشغيل التخطيط الرئيسي، يتم إنشاء أمر مخطط لكمية قيمتها 10.</span><span class="sxs-lookup"><span data-stu-id="6c9e7-153">The demand date isn't included because it's after the product lead time.) Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>
