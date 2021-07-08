---
title: أساليب التزويد وتعديل الكمية
description: يوفر هذا الموضوع معلومات حول أساليب التزويد في تحسين التخطيط. ويوضح أيضًا كيفية تأثير كمية الأمر المتعدد لمنتج على النتيجة.
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261686"
---
# <a name="replenishment-methods-and-quantity-modification"></a><span data-ttu-id="e00ef-104">أساليب التزويد وتعديل الكمية</span><span class="sxs-lookup"><span data-stu-id="e00ef-104">Replenishment methods and quantity modification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e00ef-105">يوفر هذا الموضوع معلومات حول أساليب التزويد في تحسين التخطيط.</span><span class="sxs-lookup"><span data-stu-id="e00ef-105">This topic provides information about replenishment methods in Planning Optimization.</span></span> <span data-ttu-id="e00ef-106">ويوضح أيضًا كيفية تأثير كمية الأمر المتعدد لمنتج على النتيجة.</span><span class="sxs-lookup"><span data-stu-id="e00ef-106">It also explains how the multiple order quantity for a product affects the result.</span></span>

<span data-ttu-id="e00ef-107">تعرف أساليب التزويد أيضًا بأساليب التغطية وأساليب تغيير حجم الدفعة.</span><span class="sxs-lookup"><span data-stu-id="e00ef-107">Replenishment methods are also known as coverage methods and lot-sizing methods.</span></span>

## <a name="coverage-codes"></a><span data-ttu-id="e00ef-108">أكواد التغطية</span><span class="sxs-lookup"><span data-stu-id="e00ef-108">Coverage codes</span></span>

<span data-ttu-id="e00ef-109">يمكن تكوين تحسين التخطيط لاستخدام أساليب تزويد مختلفة.</span><span class="sxs-lookup"><span data-stu-id="e00ef-109">Planning Optimization can be configured to use different replenishment methods.</span></span> <span data-ttu-id="e00ef-110">وأساليب التزويد هي التقنيات التي يستخدمها النظام لحساب المتطلبات الخاصة بأحد المنتجات.</span><span class="sxs-lookup"><span data-stu-id="e00ef-110">The replenishment methods are the techniques that the system uses to calculate requirements for a product.</span></span> <span data-ttu-id="e00ef-111">يتم تحديد أساليب التزويد بواسطة أكواد التغطية التي يمكنك إعدادها إما في مجموعة التغطية أو المنتج.</span><span class="sxs-lookup"><span data-stu-id="e00ef-111">Replenishment methods are defined by coverage codes that you can set up on either the coverage group or the product.</span></span>

<span data-ttu-id="e00ef-112">يمكن استخدام أكواد التغطية التالية في تحسين التخطيط:</span><span class="sxs-lookup"><span data-stu-id="e00ef-112">The following coverage codes can be used in Planning Optimization:</span></span>

- <span data-ttu-id="e00ef-113">**الفترة** -أسلوب التزويد يضم كافة الطلبات لفترة ما في أمر واحد للمنتج.</span><span class="sxs-lookup"><span data-stu-id="e00ef-113">**Period** – The replenishment method combines all the demand for a period into one order for the product.</span></span> <span data-ttu-id="e00ef-114">سيتم التخطيط للأمر لأول يوم من الفترة، وستستوفي كميته صافي المتطلبات خلال الفترة التي تم تعيينها.</span><span class="sxs-lookup"><span data-stu-id="e00ef-114">The order will be planned for the first day of the period, and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="e00ef-115">تبدأ الفترة مع الطلب الأول للمنتج وتغطي المدة المحددة.</span><span class="sxs-lookup"><span data-stu-id="e00ef-115">The period starts with the first demand of the product and covers the defined length of time.</span></span> <span data-ttu-id="e00ef-116">ستبدأ الفترة التالية مع المتطلبات التالية للمنتج.</span><span class="sxs-lookup"><span data-stu-id="e00ef-116">The next period will start with the next requirements of the product.</span></span> <span data-ttu-id="e00ef-117">وغالبًا ما يتم استخدام كود تغطية *الفترة* لسحب المخزون غير القابل للتوقع أو المنتجات التي تتأثر بالمواسم أو المنتجات عالية التكلفة.</span><span class="sxs-lookup"><span data-stu-id="e00ef-117">The *Period* coverage code is often used for non-predictable inventory draw, season-influenced products, or high-cost products.</span></span> <span data-ttu-id="e00ef-118">يبين الرسم التوضيحي التالي مثالاً.</span><span class="sxs-lookup"><span data-stu-id="e00ef-118">The following illustration shows an example.</span></span>

    <span data-ttu-id="e00ef-119">![مثال على استخدام كود تغطية الفترة](./media/coverage-code-period.png "مثال على استخدام كود تغطية الفترة")</span><span class="sxs-lookup"><span data-stu-id="e00ef-119">![Example of Period coverage code use](./media/coverage-code-period.png "Example of Period coverage code use")</span></span>

- <span data-ttu-id="e00ef-120">**التزويد** – في أسلوب التزويد، يقوم النظام بإنشاء أمر شراء أو تحويل أو أمر إنتاج مخطط لكل متطلب خاص بالمنتج.</span><span class="sxs-lookup"><span data-stu-id="e00ef-120">**Requirement** – In the replenishment method, the system creates a planned purchase, transfer, or production order per requirement for the product.</span></span> <span data-ttu-id="e00ef-121">يتم استخدام هذه الطريقة للمنتجات الغالية التي لها طلب متقطع.</span><span class="sxs-lookup"><span data-stu-id="e00ef-121">This method is used for expensive products that have intermittent demand.</span></span> <span data-ttu-id="e00ef-122">وغالبًا ما يتم استخدام كود التغطية *المتطلب* للمنتجات القابلة للتكوين أو سيناريوهات الإدراج في الأمر.</span><span class="sxs-lookup"><span data-stu-id="e00ef-122">The *Requirement* coverage code is often used for configurable products or make-to-order scenarios.</span></span> <span data-ttu-id="e00ef-123">يبين الرسم التوضيحي التالي مثالاً.</span><span class="sxs-lookup"><span data-stu-id="e00ef-123">The following illustration shows an example.</span></span>

    <span data-ttu-id="e00ef-124">![مثال على استخدام كود تغطية المتطلب](./media/coverage-code-requirement.png "مثال على استخدام كود تغطية المتطلب")</span><span class="sxs-lookup"><span data-stu-id="e00ef-124">![Example of Requirement coverage code use](./media/coverage-code-requirement.png "Example of Requirement coverage code use")</span></span>

- <span data-ttu-id="e00ef-125">**الحد الأدنى/الحد الأقصى**</span><span class="sxs-lookup"><span data-stu-id="e00ef-125">**Min./Max.**</span></span> <span data-ttu-id="e00ef-126">– يستند أسلوب التزويد إلى مستوى المخزون.</span><span class="sxs-lookup"><span data-stu-id="e00ef-126">– The replenishment method is based on the inventory level.</span></span> <span data-ttu-id="e00ef-127">إنه يحدد تزويد المخزون أعلى إلى مستوى معين عندما يكون المستوى الفعلي المتنبؤ به أقل من حد معين.</span><span class="sxs-lookup"><span data-stu-id="e00ef-127">It defines the replenishment of inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span> <span data-ttu-id="e00ef-128">ستكون كمية التزويد الفرق بين الحد الأقصى لمستوى المخزون والمستوى الفعلي المتوقع.</span><span class="sxs-lookup"><span data-stu-id="e00ef-128">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span> <span data-ttu-id="e00ef-129">*الحد الأدني/الحد الأقصى*</span><span class="sxs-lookup"><span data-stu-id="e00ef-129">The *Min./Max.*</span></span> <span data-ttu-id="e00ef-130">غالبًا ما يتم استخدام كود التغطية لسحب المخزون المتنبؤ به أو مشغلات عالية أو منتجات أقل تكلفة.</span><span class="sxs-lookup"><span data-stu-id="e00ef-130">coverage code is often used for predictable inventory draw, high runners, or less expensive products.</span></span> <span data-ttu-id="e00ef-131">يبين الرسم التوضيحي التالي مثالاً.</span><span class="sxs-lookup"><span data-stu-id="e00ef-131">The following illustration shows an example.</span></span>

    <span data-ttu-id="e00ef-132">![مثال على استخدام كود تغطية الحد الأدنى/الحد الأقصى](./media/coverage-code-min-max.png "مثال على استخدام كود تغطية الحد الأدنى/الحد الأقصى")</span><span class="sxs-lookup"><span data-stu-id="e00ef-132">![Example of Min./Max. coverage code use](./media/coverage-code-min-max.png "Example of Min./Max. coverage code use")</span></span>

- <span data-ttu-id="e00ef-133">**يدوي** – في أسلوب التزويد، لا يقترح النظام أوامر الشراء أو التحويل أو الإنتاج الخاصة بالمنتج.</span><span class="sxs-lookup"><span data-stu-id="e00ef-133">**Manual** – In the replenishment method, the system doesn't suggest purchase, transfer, or production orders for the product.</span></span> <span data-ttu-id="e00ef-134">وبدلاً من ذلك، يكون مخطط المنتج مسؤولاً عن إنشاء الأوامر المطلوبة لتزويد المنتج.</span><span class="sxs-lookup"><span data-stu-id="e00ef-134">Instead, the planner for the product is responsible for creating the required orders for the replenishment of the product.</span></span> <span data-ttu-id="e00ef-135">غالبًا ما يتم استخدام كود التغطية *يدوي* للمنتجات التي لا يلزم لها أوامر مخططة منشاة بواسطة النظام.</span><span class="sxs-lookup"><span data-stu-id="e00ef-135">The *Manual* coverage code is often used for products that system-generated planned orders aren't wanted for.</span></span>

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a><span data-ttu-id="e00ef-136">التأثير على كمية الأمر من إعدادات الأوامر الافتراضية</span><span class="sxs-lookup"><span data-stu-id="e00ef-136">Impact of the order quantity from default order settings</span></span>

<span data-ttu-id="e00ef-137">في الصفحة **إعداد الأوامر الافتراضية** لمنتج تم إصداره، يمكنك تحديد كل من إعدادات الكمية التالية في علامات التبويب السريعة **أمر الشراء** و **المخزون** و **أمر المبيعات**.</span><span class="sxs-lookup"><span data-stu-id="e00ef-137">On the **Default order setting** page for a released product, you can specify each of following quantity settings on the **Purchase order**, **Inventory**, and **Sales order** FastTabs.</span></span> <span data-ttu-id="e00ef-138">(يتم استخدام علامة التبويب السريعة **المخزون** لكل من أوامر التحويل وأوامر الإنتاج.)</span><span class="sxs-lookup"><span data-stu-id="e00ef-138">(The **Inventory** FastTab is used for both transfer orders and production orders.)</span></span>

- <span data-ttu-id="e00ef-139">**متعدد** – ستكون الأوامر المخططة مضاعفة لهذه الكمية.</span><span class="sxs-lookup"><span data-stu-id="e00ef-139">**Multiple** – Planned orders will be a multiple of this quantity.</span></span>

    <span data-ttu-id="e00ef-140">على سبيل المثال، إذا تم تعيين الحقل **متعدد** إلى *5*، يمكن أن يكون الأمر للكمية 5 و10 و15 و20 وهكذا.</span><span class="sxs-lookup"><span data-stu-id="e00ef-140">For example, if the **Multiple** field is set to *5*, an order can be for a quantity of 5, 10, 15, 20, and so on.</span></span>

- <span data-ttu-id="e00ef-141">**الحد الأدنى لكمية الأمر** – لن تكون الأوامر المخططة أقل من القيمة المحددة.</span><span class="sxs-lookup"><span data-stu-id="e00ef-141">**Min. order quantity** – Planned orders won't be less than the specified value.</span></span>

    <span data-ttu-id="e00ef-142">على سبيل المثال، إذا تم تعيين الحقل **الحد الأدنى لكمية الأمر** إلى *10*، فإنه سيتم إنشاء أمر مخطط لكمية مقدارها 10، حتى في حالة طلب الأربعة فقط لاستيفاء الطلب.</span><span class="sxs-lookup"><span data-stu-id="e00ef-142">For example, if the **Min. order quantity** field is set to *10*, a planned order for a quantity of 10 will be created, even if only four are required to fulfill the demand.</span></span>

- <span data-ttu-id="e00ef-143">**الحد الأدنى لكمية الأمر** – لن تتجاوز الأوامر المخططة القيمة المحددة.</span><span class="sxs-lookup"><span data-stu-id="e00ef-143">**Max. order quantity** – Planned orders won't exceed the specified value.</span></span> <span data-ttu-id="e00ef-144">إذا كان الطلب أكثر من قيمة **الحد الأقصى لقيمة كمية الأمر**، فإنه سيتم إنشاء الأوامر المخططة المتعددة لتغطيتها.</span><span class="sxs-lookup"><span data-stu-id="e00ef-144">If the demand is more than the **Max. order quantity** value, multiple planned orders will be created to cover it.</span></span>

    <span data-ttu-id="e00ef-145">على سبيل المثال، إذا تم تعيين الحقل **الحد الأقصى لكمية الأمر** إلى *100*، وكان الطلب هو 450، يتم إنشاء أربعة أوامر مخططة لكمية مقدارها 100 ويتم إنشاء أمر مخطط لكمية بالقيمة 50.</span><span class="sxs-lookup"><span data-stu-id="e00ef-145">For example, if the **Max. order quantity** field is set to *100*, and the demand is 450, four planned orders for a quantity of 100 and one planned order for a quantity of 50 will be created.</span></span>

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a><span data-ttu-id="e00ef-146">أمثلة على التزويد التي تستخدم الحد الأدنى/الحد الأقصى</span><span class="sxs-lookup"><span data-stu-id="e00ef-146">Examples of replenishment that use the Min./Max.</span></span> <span data-ttu-id="e00ef-147">كود التغطية</span><span class="sxs-lookup"><span data-stu-id="e00ef-147">coverage code</span></span>

<span data-ttu-id="e00ef-148">إذا لم تقم بتحديد قيمة في الحقل **متعدد** لمنتج الصفحة في **إعداد الأمر الافتراضي**، وإذا كنت تستخدم *الحد الأدنى/الحد الأقصى*</span><span class="sxs-lookup"><span data-stu-id="e00ef-148">If you don't specify a value in the **Multiple** field for a product on the **Default order setting** page, and if you're using the *Min./Max.*</span></span> <span data-ttu-id="e00ef-149">أسلوب التزويد، سيعمل تحسين التخطيط على تزويد المخزون أعلى إلى مستوى معين عندما يكون المستوى الفعلي المتنبؤ به أقل من حد معين.</span><span class="sxs-lookup"><span data-stu-id="e00ef-149">replenishment method, Planning Optimization will replenish the inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span>

<span data-ttu-id="e00ef-150">إذا قمت بتحديد كمية متعددة لأحد المنتجات، يكون *الحد الأدنى/الحد الأقصى.*</span><span class="sxs-lookup"><span data-stu-id="e00ef-150">If you define a multiple quantity for a product, the *Min./Max.*</span></span> <span data-ttu-id="e00ef-151">يقوم أسلوب التزويد بتغيير سلوكه ووضع القيمة **المتعددة** في الاعتبار.</span><span class="sxs-lookup"><span data-stu-id="e00ef-151">replenishment method changes its behavior and considers the **Multiple** value.</span></span>

<span data-ttu-id="e00ef-152">بمعني آخر، لا يزال تحسين التخطيط يعمل على تزويد المخزون حتى مستوى الحد الأقصى المحدد عندما يكون المستوى الفعلي الذي تم توقعه أقل من مستوى الحد الأدنى المحدد.</span><span class="sxs-lookup"><span data-stu-id="e00ef-152">In other words, Planning Optimization will still replenish the inventory up to the defined maximum level when the predicted on-hand level is less than the defined minimum level.</span></span> <span data-ttu-id="e00ef-153">ومع ذلك، يجب أن تكون كمية التزويد مضاعفة للقيمة **المتعددة**.</span><span class="sxs-lookup"><span data-stu-id="e00ef-153">However, the replenishment quantity must be a multiple of the **Multiple** value.</span></span>

<span data-ttu-id="e00ef-154">إذا لم تكن كمية التزويد (الفرق بين مستوى الحد الأقصى والمستوى الفعلي الذي تم توقعه) متعددة للكمية المتعددة المحددة، فإن تحسين التخطيط يستخدم أول قيمة محتملة، والتي تكون مع مستوى التوقع الفعلي، تكون أقل من مستوى الحد الأقصى.</span><span class="sxs-lookup"><span data-stu-id="e00ef-154">If the replenishment quantity (the difference between the maximum level and the predicted on-hand level) isn't a multiple of the defined multiple quantity, Planning Optimization uses the first possible value that, together with predicted on-hand level, will be below the maximum level.</span></span> <span data-ttu-id="e00ef-155">وإذا كان المجموع أقل من الحد الأدنى للمستوى، فإن تحسين التخطيط يستخدم القيمة الأولى التي، مع التوقع الفعلي، ستكون أعلى من مستوى الحد الأقصى.</span><span class="sxs-lookup"><span data-stu-id="e00ef-155">If the sum is less than the minimum level, Planning Optimization uses the first value that, together with predicted on-hand, will be above the maximum level.</span></span>

<span data-ttu-id="e00ef-156">توفر الأقسام الفرعية التالية بعض الأمثلة التي توضح كيف تؤثر كمية الأمر المتعددة لمنتج على نتيجة *الحد الأدنى/الحد الأقصى.*</span><span class="sxs-lookup"><span data-stu-id="e00ef-156">The following subsections provide some examples that show how the multiple order quantity for a product affects the result of the *Min./Max.*</span></span> <span data-ttu-id="e00ef-157">أسلوب التزويد.</span><span class="sxs-lookup"><span data-stu-id="e00ef-157">replenishment method.</span></span>

### <a name="example-1"></a><span data-ttu-id="e00ef-158">مثال1</span><span class="sxs-lookup"><span data-stu-id="e00ef-158">Example 1</span></span>

<span data-ttu-id="e00ef-159">يتمتع المنتج بالتكوين التالي:</span><span class="sxs-lookup"><span data-stu-id="e00ef-159">A product has the following configuration:</span></span>

- <span data-ttu-id="e00ef-160">**كود التغطية:** *الحد الأدنى/الحد الأقصى.*</span><span class="sxs-lookup"><span data-stu-id="e00ef-160">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="e00ef-161">**الحد الأدنى:** *15*</span><span class="sxs-lookup"><span data-stu-id="e00ef-161">**Minimum:** *15*</span></span>
- <span data-ttu-id="e00ef-162">**الحد الأقصى:** *22*</span><span class="sxs-lookup"><span data-stu-id="e00ef-162">**Maximum:** *22*</span></span>
- <span data-ttu-id="e00ef-163">**متعدد:** *0*</span><span class="sxs-lookup"><span data-stu-id="e00ef-163">**Multiple:** *0*</span></span>

<span data-ttu-id="e00ef-164">توجد 10 قطع من المخزون الفعلي للمنتج، ولا يوجد طلب أو توريد آخر.</span><span class="sxs-lookup"><span data-stu-id="e00ef-164">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="e00ef-165">عند تشغيل التخطيط الرئيسي، يتم إنشاء أمر مخطط لـ 12 قطعة لتزويد المخزون إلى الحد الأقصى للكمية.</span><span class="sxs-lookup"><span data-stu-id="e00ef-165">When master planning runs, a planned order for 12 pieces is created to replenish inventory to the maximum quantity.</span></span>

### <a name="example-2"></a><span data-ttu-id="e00ef-166">مثال2</span><span class="sxs-lookup"><span data-stu-id="e00ef-166">Example 2</span></span>

<span data-ttu-id="e00ef-167">يتمتع المنتج بالتكوين التالي:</span><span class="sxs-lookup"><span data-stu-id="e00ef-167">A product has the following configuration:</span></span>

- <span data-ttu-id="e00ef-168">**كود التغطية:** *الحد الأدنى/الحد الأقصى.*</span><span class="sxs-lookup"><span data-stu-id="e00ef-168">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="e00ef-169">**الحد الأدنى:** *15*</span><span class="sxs-lookup"><span data-stu-id="e00ef-169">**Minimum:** *15*</span></span>
- <span data-ttu-id="e00ef-170">**الحد الأقصى:** *22*</span><span class="sxs-lookup"><span data-stu-id="e00ef-170">**Maximum:** *22*</span></span>
- <span data-ttu-id="e00ef-171">**متعدد:** *5*</span><span class="sxs-lookup"><span data-stu-id="e00ef-171">**Multiple:** *5*</span></span>

<span data-ttu-id="e00ef-172">توجد 10 قطع من المخزون الفعلي للمنتج، ولا يوجد طلب أو توريد آخر.</span><span class="sxs-lookup"><span data-stu-id="e00ef-172">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="e00ef-173">عند تشغيل التخطيط الرئيسي، يتم إنشاء أمر مخطط لكل 10 قطع (لأن 15 قطعة من التزويد بالإضافة إلى 10 قطع من المخزون الفعلي ستتجاوز الحد الأقصى للكمية).</span><span class="sxs-lookup"><span data-stu-id="e00ef-173">When master planning runs, a planned order for 10 pieces is created (because 15 pieces of replenishment plus 10 pieces of on-hand inventory will exceed the maximum quantity).</span></span>

### <a name="example-3"></a><span data-ttu-id="e00ef-174">المثال الثالث</span><span class="sxs-lookup"><span data-stu-id="e00ef-174">Example 3</span></span>

<span data-ttu-id="e00ef-175">يتمتع المنتج بالتكوين التالي:</span><span class="sxs-lookup"><span data-stu-id="e00ef-175">A product has the following configuration:</span></span>

- <span data-ttu-id="e00ef-176">**كود التغطية:** *الحد الأدنى/الحد الأقصى.*</span><span class="sxs-lookup"><span data-stu-id="e00ef-176">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="e00ef-177">**الحد الأدنى:** *21*</span><span class="sxs-lookup"><span data-stu-id="e00ef-177">**Minimum:** *21*</span></span>
- <span data-ttu-id="e00ef-178">**الحد الأقصى:** *24*</span><span class="sxs-lookup"><span data-stu-id="e00ef-178">**Maximum:** *24*</span></span>
- <span data-ttu-id="e00ef-179">**متعدد:** *5*</span><span class="sxs-lookup"><span data-stu-id="e00ef-179">**Multiple:** *5*</span></span>

<span data-ttu-id="e00ef-180">توجد 10 قطع من المخزون الفعلي للمنتج، ولا يوجد طلب أو توريد آخر.</span><span class="sxs-lookup"><span data-stu-id="e00ef-180">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="e00ef-181">عند تشغيل التخطيط الرئيسي، يتم إنشاء الأمر المخطط لكل 15 قطعة (لأن 10 قطعة من التزويد بالإضافة إلى 10 قطع من المخزون الفعلي ستكون أقل من الحد الأدنى للكمية).</span><span class="sxs-lookup"><span data-stu-id="e00ef-181">When master planning runs, the planned order for 15 pieces is created (because 10 pieces of replenishment plus 10 pieces of on-hand inventory will be less than the minimum quantity).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
