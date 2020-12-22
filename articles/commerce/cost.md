---
title: تكوين التكلفة لإدارة الأوامر الموزعة (DOM)
description: يصف هذا الموضوع تكوين التكلفة لوظيفة إدارة الأوامر الموزعة (DOM) في Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7644cb9800a418fd123b32a0257b787277fcb19f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458340"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a><span data-ttu-id="ce7ee-103">تكوين التكلفة لإدارة الأوامر الموزعة (DOM)</span><span class="sxs-lookup"><span data-stu-id="ce7ee-103">Cost configuration for distributed order management (DOM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce7ee-104">تراعي المؤسسات العديد من مكونات التكلفة لتحديد الموقع الأمثل لتنفيذ أمر منه.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-104">Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</span></span> <span data-ttu-id="ce7ee-105">بعض مكونات التكلفة هذه هي تكلفة الشحن وتكلفة المناولة وتكلفة التعبئة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-105">Some of these cost components are shipping cost, handling cost, and packaging cost.</span></span> <span data-ttu-id="ce7ee-106">ويتم حساب مجموعة من هذه التكاليف لتحديد موقع التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-106">A combination of these costs is calculated to determine the fulfillment location.</span></span>

<span data-ttu-id="ce7ee-107">عندما قام التكرار الأول لإدارة الأوامر الموزعة (DOM) في Dynamics 365 Commerce بتحسين تعيين الأوامر إلى مواقع التنفيذ، أخذ في الاعتبار عامل المسافة فقط.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-107">When the first iteration of distributed order management (DOM) in Dynamics 365 Commerce optimized the assignment of orders to fulfillment locations, it factored in distance only.</span></span> <span data-ttu-id="ce7ee-108">وعلى الرغم من إمكانية ربط المسافة بالتكلفة، إلا أنها غير مماثلة للتكلفة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-108">Although distance can be correlated with cost, it isn't the same as cost.</span></span> <span data-ttu-id="ce7ee-109">على سبيل المثال، تكلف طريقة الشحن الليلي أكثر من ثلاثة أيام أو سبعة أيام شحن للمسافة نفسها.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-109">For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</span></span>

<span data-ttu-id="ce7ee-110">تسمح ميزة تكوين التكلفة لبائعي التجزئة بتعريف وتكوين مكونات التكلفة الإضافية التي سيتم حسابها وأخذها في الاعتبار لتحديد الموقع الأمثل لتنفيذ بنود الأمر منه.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-110">The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</span></span>

<span data-ttu-id="ce7ee-111">عند تكوين مكونات التكلفة، تستخدم حلول DOM تعريفات التكلفة هذه فقط لتحديد الموقع الأمثل لتنفيذ الأمر.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-111">When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</span></span> <span data-ttu-id="ce7ee-112">ولا تعتبر مكون المسافة كتكلفة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-112">It doesn't consider the distance component as a cost.</span></span> <span data-ttu-id="ce7ee-113">ومع ذلك، إذا لم يتم تكوين مكونات التكلفة، فإن حلول DOM تستخدم مكون المسافة كتكلفة لتحديد الموقع الأمثل لتنفيذ الأمر.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-113">However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</span></span>

## <a name="set-up-cost-components"></a><span data-ttu-id="ce7ee-114">إعداد مكونات التكلفة</span><span class="sxs-lookup"><span data-stu-id="ce7ee-114">Set up cost components</span></span>

<span data-ttu-id="ce7ee-115">يمكن تعريف نوعين من مكونات التكلفة الرئيسية في النظام: **الشحن** و **غير ذلك**.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-115">Two major cost component types can be defined in the system: **Shipping** and **Other**.</span></span>

<span data-ttu-id="ce7ee-116">يدعم هذان النوعان من مكونات التكلفة أساسات حسابات متعددة، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-116">Both cost component types support multiple calculation bases, as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ce7ee-117">نوع مكون التكلفة</span><span class="sxs-lookup"><span data-stu-id="ce7ee-117">Cost component type</span></span></th>
<th><span data-ttu-id="ce7ee-118">أساس الحساب</span><span class="sxs-lookup"><span data-stu-id="ce7ee-118">Calculation basis</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce7ee-119">الشحن</span><span class="sxs-lookup"><span data-stu-id="ce7ee-119">Shipping</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ce7ee-120">بسيط</span><span class="sxs-lookup"><span data-stu-id="ce7ee-120">Simple</span></span></li>
<li><span data-ttu-id="ce7ee-121">مرتبط بمستوى</span><span class="sxs-lookup"><span data-stu-id="ce7ee-121">Tiered</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="ce7ee-122">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="ce7ee-122">Other</span></span></td>
<td>
<ul>
<li><span data-ttu-id="ce7ee-123">أمر مبيعات</span><span class="sxs-lookup"><span data-stu-id="ce7ee-123">Sales order</span></span></li>
<li><span data-ttu-id="ce7ee-124">بند مبيعات</span><span class="sxs-lookup"><span data-stu-id="ce7ee-124">Sales line</span></span></li>
<li><span data-ttu-id="ce7ee-125">الموقع</span><span class="sxs-lookup"><span data-stu-id="ce7ee-125">Location</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a><span data-ttu-id="ce7ee-126">نوع مكون تكلفة الشحن</span><span class="sxs-lookup"><span data-stu-id="ce7ee-126">Shipping cost component type</span></span>

<span data-ttu-id="ce7ee-127">يوضح هذا القسم كيفية اعداد كل مجموعة من نوع مكون تكلفة **الشحن** وأساس حساب لتكاليف الشحن.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-127">This section explains how to set up each combination of the **Shipping** cost component type and a calculation basis for shipping costs.</span></span> <span data-ttu-id="ce7ee-128">ويوضح أيضًا كيف تستخدم حلول DOM كل مجموعة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-128">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a><span data-ttu-id="ce7ee-129">نوع مكون التكلفة = الشحن وأساس الحساب = بسيط</span><span class="sxs-lookup"><span data-stu-id="ce7ee-129">Cost component type = Shipping and Calculation basis = Simple</span></span>

<span data-ttu-id="ce7ee-130">إذا تم استخدام مجموعة مكونة من نوع مكون تكلفة **الشحن** وأساس الحساب **البسيط**، فإن تكلفة الشحن لوضع التسليم تستند إلى مسافة أو تكلفة ثابتة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-130">If a combination of the **Shipping** cost component type and the **Simple** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span>

<span data-ttu-id="ce7ee-131">يجب إعداد الحقول التالية لهذه المجموعة:</span><span class="sxs-lookup"><span data-stu-id="ce7ee-131">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ce7ee-132">**عامل التكلفة** – أدخل معرفًا فريدًا لعامل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-132">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ce7ee-133">**الوصف** – أدخل اسمًا ووصفًا لعامل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-133">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ce7ee-134">**تاريخ البدء** و **تاريخ الانتهاء** – يمكن استخدام هذين الحقلين لتقييد عامل التكلفة بنطاق تاريخ محدد.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-134">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ce7ee-135">في حال تركت هذين الحقلين فارغين، فسيكون عامل التكلفة صالحًا لفتره غير محدده.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-135">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ce7ee-136">**نشط** – للإشارة إلى ما إذا كان عام التكلفة نشطًا.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-136">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ce7ee-137">تأخذ DOM في الاعتبار فقط عوامل التكلفة النشطة المرتبطة بملف تعريف التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-137">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ce7ee-138">**الشركة** – حدد الكيان القانوني الذي تم تكوين عامل التكلفة له.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-138">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="ce7ee-139">يجب أن تكون كافة بنود معايير الحساب لنفس الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-139">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="ce7ee-140">**أوضاع التسليم** – حدد أوضاع التسليم التي تم تكوين التكلفة لها.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-140">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="ce7ee-141">**نوع الحساب** – حدد كيفية حساب التكلفة لوضع تسليم معين.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-141">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery.</span></span> <span data-ttu-id="ce7ee-142">هناك نوعان مدعومان من الحسابات:</span><span class="sxs-lookup"><span data-stu-id="ce7ee-142">Two calculation types are supported:</span></span>

    - <span data-ttu-id="ce7ee-143">**ثابت** – يتم استخدام تكلفة ثابتة لوضع التسليم.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-143">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="ce7ee-144">إذا قمت بتحديد نوع الحساب هذا، فإن حقل **التكلفة** يحدد التكلفة الثابتة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-144">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="ce7ee-145">**لكل وحدة مسافة‬** – يتم حساب تكلفة وضع التسليم كقيمة التكلفة المحددة في حقل **التكلفة** مضروبة في المسافة بين عنوان التسليم والمواقع.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-145">**Per-distance unit** – The cost for the mode of delivery is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="ce7ee-146">**التكلفة** - حدد قيمه التكلفة المستخدمة بالتزامن مع حقل **نوع الحساب** لحساب التكلفة لوضع التسليم.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-146">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a><span data-ttu-id="ce7ee-147">نوع مكون التكلفة = الشحن وأساس الحساب = مرتبط بمستوى‬</span><span class="sxs-lookup"><span data-stu-id="ce7ee-147">Cost component type = Shipping and Calculation basis = Tiered</span></span>

<span data-ttu-id="ce7ee-148">إذا تم استخدام مجموعة مكونة من نوع مكون تكلفة **الشحن** وأساس الحساب **مرتبط بمستوى‬**، فإن تكلفة الشحن لوضع التسليم تستند إلى مسافة أو تكلفة ثابتة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-148">If a combination of the **Shipping** cost component type and the **Tiered** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span> <span data-ttu-id="ce7ee-149">ولكن المسافة في هذه المجموعة تستند إلى مجموعة من مسافات مرتبطة بمستوى.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-149">However, in this combination, the distance is based on a tiered range of distances.</span></span>

<span data-ttu-id="ce7ee-150">يجب إعداد الحقول التالية لهذه المجموعة:</span><span class="sxs-lookup"><span data-stu-id="ce7ee-150">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ce7ee-151">**عامل التكلفة** – أدخل معرفًا فريدًا لعامل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-151">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ce7ee-152">**الوصف** – أدخل اسمًا ووصفًا لعامل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-152">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ce7ee-153">**التكلفة الافتراضية** – تحديد التكلفة التي يجب استخدامها لوضع التسليم إذا لم تقع المسافة بين عنوان التسليم والموقع في أي من المسافات المرتبطة بمستويات لوضع التسليم.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-153">**Default cost** – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</span></span>
- <span data-ttu-id="ce7ee-154">**تاريخ البدء** و **تاريخ الانتهاء** – يمكن استخدام هذين الحقلين لتقييد عامل التكلفة بنطاق تاريخ محدد.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-154">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ce7ee-155">في حال تركت هذين الحقلين فارغين، فسيكون عامل التكلفة صالحًا لفتره غير محدده.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-155">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ce7ee-156">**نشط** – للإشارة إلى ما إذا كان عام التكلفة نشطًا.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-156">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ce7ee-157">تأخذ DOM في الاعتبار فقط عوامل التكلفة النشطة المرتبطة بملف تعريف التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-157">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ce7ee-158">**الشركة** – حدد الكيان القانوني الذي تم تكوين عامل التكلفة له.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-158">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="ce7ee-159">يجب أن تكون كافة بنود معايير الحساب لنفس الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-159">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="ce7ee-160">**أوضاع التسليم** – حدد أوضاع التسليم التي تم تكوين التكلفة لها.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-160">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="ce7ee-161">**نوع المسافة** – حدد ما إذا كان تعريف المسافة المرتبطة عبارة عن مسافة جوية أو برية.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-161">**Distance type** – Specify whether the tiered distance definition is an aerial distance or a road distance.</span></span>
- <span data-ttu-id="ce7ee-162">**وحدات‏‎ المسافة** – حدد الوحدة التي يتم بها قياس المسافة المرتبط بمستوى.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-162">**Distance units** – Specify the unit that the tiered distance is measured in.</span></span>
- <span data-ttu-id="ce7ee-163">**مسافة من** – حدد نطاق البدء للمسافة المرتبطة بمستوى.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-163">**Distance from** – Specify the start range for the tiered distance.</span></span>
- <span data-ttu-id="ce7ee-164">**مسافة إلى** – حدد نطاق الانتهاء للمسافة المرتبطة بمستوى.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-164">**Distance to** – Specify the end range for the tiered distance.</span></span>
- <span data-ttu-id="ce7ee-165">**نوع الحساب** – حدد كيفية حساب التكلفة لوضع تسليم معين ومسافة مرتبطة بمستوى.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-165">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</span></span> <span data-ttu-id="ce7ee-166">هناك نوعان مدعومان من الحسابات:</span><span class="sxs-lookup"><span data-stu-id="ce7ee-166">Two calculation types are supported:</span></span>

    - <span data-ttu-id="ce7ee-167">**ثابت** – يتم استخدام تكلفة ثابتة لوضع التسليم.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-167">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="ce7ee-168">إذا قمت بتحديد نوع الحساب هذا، فإن حقل **التكلفة** يحدد التكلفة الثابتة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-168">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="ce7ee-169">**لكل وحدة مسافة‬** – يتم حساب تكلفة وضع التسليم والمسافة المرتبطة بمستوى كقيمة التكلفة المحددة في حقل **التكلفة** مضروبة في المسافة بين عنوان التسليم والمواقع.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-169">**Per distance unit** – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="ce7ee-170">**التكلفة** - حدد قيمه التكلفة المستخدمة بالتزامن مع حقل **نوع الحساب** لحساب التكلفة لوضع التسليم.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-170">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

> [!NOTE]
> - <span data-ttu-id="ce7ee-171">عندما تقوم بتعريف مسافات مرتبطة بمستويات، يتحقق النظام من عدم وجود مسافات مفقودة أو متراكبة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-171">When you define tiered distances, the system validates that there are no missing or overlapping distances.</span></span>
> - <span data-ttu-id="ce7ee-172">يجب ان يكون نوع المسافة المستخدم لوضع التسليم هو نفسه عبر كافة المسافات المرتبطة بمستويات.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-172">The distance type that is used for a mode of delivery must be the same across all the tiered distances.</span></span>

### <a name="other-cost-component-type"></a><span data-ttu-id="ce7ee-173">نوع مكون التكلفة "غير ذلك"</span><span class="sxs-lookup"><span data-stu-id="ce7ee-173">Other cost component type</span></span>

<span data-ttu-id="ce7ee-174">يوضح هذا القسم كيفية اعداد كل مجموعة من نوع مكون التكلفة **غير ذلك** ونوع تكلفة آخر للتكاليف غير المرتبطة بالشحن.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-174">This section explains how to set up each combination of the **Other** cost component type and an other cost type for non-shipping costs.</span></span> <span data-ttu-id="ce7ee-175">ويوضح أيضًا كيف تستخدم حلول DOM كل مجموعة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-175">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a><span data-ttu-id="ce7ee-176">نوع مكون التكلفة = غير ذلك ونوع تكلفة آخر = أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="ce7ee-176">Cost component type = Other and Other cost type = Sales order</span></span>

<span data-ttu-id="ce7ee-177">يتم استخدام مجموعة من نوع مكون التكلفة **غير ذلك** ونوع التكلفة الآخر **أمر المبيعات** لتعريف تكاليف غير مرتبطة بالشحن على مستوى أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-177">A combination of the **Other** cost component type and the **Sales order** other cost type is used to define non-shipping costs at the sales order level.</span></span>

<span data-ttu-id="ce7ee-178">يجب إعداد الحقول التالية لهذه المجموعة:</span><span class="sxs-lookup"><span data-stu-id="ce7ee-178">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ce7ee-179">**عامل التكلفة** – أدخل معرفًا فريدًا لعامل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-179">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ce7ee-180">**الوصف** – أدخل اسمًا ووصفًا لعامل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-180">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ce7ee-181">**تاريخ البدء** و **تاريخ الانتهاء** – يمكن استخدام هذين الحقلين لتقييد عامل التكلفة بنطاق تاريخ محدد.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-181">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ce7ee-182">في حال تركت هذين الحقلين فارغين، فسيكون عامل التكلفة صالحًا لفتره غير محدده.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-182">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ce7ee-183">**نشط** – للإشارة إلى ما إذا كان عام التكلفة نشطًا.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-183">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ce7ee-184">تأخذ DOM في الاعتبار فقط عوامل التكلفة النشطة المرتبطة بملف تعريف التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-184">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ce7ee-185">**التكلفة** – حدد قيمه التكلفة لتكلفة غير مرتبطة بالشحن على مستوى أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-185">**Cost** – Specify the cost value for a non-shipping cost at the sales order level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a><span data-ttu-id="ce7ee-186">نوع مكون التكلفة = غير ذلك ونوع تكلفة آخر = بند المبيعات</span><span class="sxs-lookup"><span data-stu-id="ce7ee-186">Cost component type = Other and Other cost type = Sales line</span></span>

<span data-ttu-id="ce7ee-187">يتم استخدام مجموعة من نوع مكون التكلفة **غير ذلك** ونوع التكلفة الآخر **بند المبيعات** لتعريف تكاليف غير مرتبطة بالشحن على مستوى بند المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-187">A combination of the **Other** cost component type and the **Sales line** other cost type is used to define non-shipping costs at the sales order line level.</span></span>

<span data-ttu-id="ce7ee-188">يجب إعداد الحقول التالية لهذه المجموعة:</span><span class="sxs-lookup"><span data-stu-id="ce7ee-188">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ce7ee-189">**عامل التكلفة** – أدخل معرفًا فريدًا لعامل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-189">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ce7ee-190">**الوصف** – أدخل اسمًا ووصفًا لعامل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-190">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ce7ee-191">**تاريخ البدء** و **تاريخ الانتهاء** – يمكن استخدام هذين الحقلين لتقييد عامل التكلفة بنطاق تاريخ محدد.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-191">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ce7ee-192">في حال تركت هذين الحقلين فارغين، فسيكون عامل التكلفة صالحًا لفتره غير محدده.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-192">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ce7ee-193">**نشط** – للإشارة إلى ما إذا كان عام التكلفة نشطًا.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-193">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ce7ee-194">تأخذ DOM في الاعتبار فقط عوامل التكلفة النشطة المرتبطة بملف تعريف التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-194">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ce7ee-195">**التكلفة** – حدد قيمه التكلفة لتكلفة غير مرتبطة بالشحن على مستوى بند المبيعات.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-195">**Cost** – Specify the cost value for a non-shipping cost at the sales order line level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--location"></a><span data-ttu-id="ce7ee-196">نوع مكون التكلفة = غير ذلك ونوع تكلفة آخر = الموقع</span><span class="sxs-lookup"><span data-stu-id="ce7ee-196">Cost component type = Other and Other cost type = Location</span></span>

<span data-ttu-id="ce7ee-197">يتم استخدام مجموعة من نوع مكون التكلفة **غير ذلك** ونوع التكلفة الآخر **الموقع** لتعريف تكاليف غير مرتبطة بالشحن لمجموعة من المواقع أو لموقع فردي.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-197">A combination of the **Other** cost component type and the **Location** other cost type is used to define non-shipping costs for a group of locations or an individual location.</span></span>

<span data-ttu-id="ce7ee-198">يجب إعداد الحقول التالية لهذه المجموعة:</span><span class="sxs-lookup"><span data-stu-id="ce7ee-198">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="ce7ee-199">**عامل التكلفة** – أدخل معرفًا فريدًا لعامل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-199">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="ce7ee-200">**الوصف** – أدخل اسمًا ووصفًا لعامل التكلفة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-200">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="ce7ee-201">**تاريخ البدء** و **تاريخ الانتهاء** – يمكن استخدام هذين الحقلين لتقييد عامل التكلفة بنطاق تاريخ محدد.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-201">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="ce7ee-202">في حال تركت هذين الحقلين فارغين، فسيكون عامل التكلفة صالحًا لفتره غير محدده.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-202">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="ce7ee-203">**نشط** – للإشارة إلى ما إذا كان عام التكلفة نشطًا.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-203">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="ce7ee-204">تأخذ DOM في الاعتبار فقط عوامل التكلفة النشطة المرتبطة بملف تعريف التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-204">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="ce7ee-205">**مجموعة التنفيذ‬** – حدد مجموعة المواقع التي تم تعريف التكلفة المرتبطة بالشحن لها.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-205">**Fulfillment group** – Specify the group of locations that the non-shipping cost is defined for.</span></span>
- <span data-ttu-id="ce7ee-206">**موقع التنفيذ‬** – حدد الموقع الذي تم تعريف التكلفة المرتبطة بالشحن له.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-206">**Fulfillment location** – Specify the location that the non-shipping cost is defined for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ce7ee-207">لا يمكنك تحديد مجموعة تنفيذ وموقع تنفيذ على البند نفسه لمعايير الحساب المستندة إلى الموقع.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-207">You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</span></span>

- <span data-ttu-id="ce7ee-208">**التكلفة** – حدد قيمه التكلفة للتكلفة غير المرتبطة بالشحن على مستوي مجموعه التنفيذ أو مستوى موقع التنفيذ.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-208">**Cost** – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ce7ee-209">لكي تأخذ DOM هذه التكاليف في الاعتبار عند تشغيلها، يجب إضافة عامل التكلفة إلى ملف تعريف التنفيذ ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="ce7ee-209">For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</span></span>
