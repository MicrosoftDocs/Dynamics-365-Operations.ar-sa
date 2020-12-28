---
title: توزيع تكاليف الرأس لمطابقة بنود المبيعات
description: يصف هذا الموضوع قدرات إضافية لحساب وتطبيق التكاليف التلقائية على أوامر قناة التجارة باستخدام ميزة التكاليف التلقائية المتقدمة.
author: hhaines
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 048885cac7a316e144b2df072da405d74096203f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409766"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a><span data-ttu-id="7d854-103">توزيع تكاليف الرأس لمطابقة بنود المبيعات</span><span class="sxs-lookup"><span data-stu-id="7d854-103">Prorate header charges to matching sales lines</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7d854-104">يصف هذا الموضوع الوظيفة المتعلقة بتجميع التكاليف التلقائية على مستوى الرأس وتوزيعها على بنود مبيعات التجارة.</span><span class="sxs-lookup"><span data-stu-id="7d854-104">This topic describes the functionality for grouping header-level auto-charges and prorating them to commerce sales lines.</span></span> <span data-ttu-id="7d854-105">وتتوفر هذه الوظيفة للحركات التي تم إنشاؤها عند نقطة البيع (POS) في الإصدار 10.0.1 من Retail والمبيعات التي تم إنشاؤها في مركز اتصال في الإصدار 10.0.2 من Retail.</span><span class="sxs-lookup"><span data-stu-id="7d854-105">This functionality is available for transactions that are created at the point of sale (POS) in Retail version 10.0.1 and sales that are created in a call center in Retail version 10.0.2.</span></span>

<span data-ttu-id="7d854-106">تتوفر هذه الوظيفة فقط عند تشغيل ميزة [التكاليف التلقائية المتقدمة](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) باستخدام الخيار في صفحة **معلمات التجارة**.</span><span class="sxs-lookup"><span data-stu-id="7d854-106">This functionality is available only if the [advanced auto-charges](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) feature is turned on by using the option on the **Commerce parameters** page.</span></span> <span data-ttu-id="7d854-107">بالإضافة إلى ذلك، يمكن تطبيق طريقة الحساب المحسنة للتكاليف التلقائية فقط على أوامر مبيعات البيع بالتجزئة التي يتم إنشاؤها من خلال قنوات التجارة (نقطة البيع ومركز الاتصال والنظام الأساسي Dynamics للتجارة الإلكترونية).</span><span class="sxs-lookup"><span data-stu-id="7d854-107">Additionally, the enhanced calculation method for auto-charges can be applied only to sales orders that are created through commerce channels (the POS, a call center, and the Dynamics e-Commerce platform).</span></span>

<span data-ttu-id="7d854-108">تمنح هذه الوظيفة الجديدة المؤسسات مرونة أكثر في طريقة حساب التكاليف التلقائية على مستوى الرأس وتطبيقها على حركات البيع.</span><span class="sxs-lookup"><span data-stu-id="7d854-108">This new functionality gives organizations more flexibility in the way that header-level auto-charges are calculated and applied to sales transactions.</span></span>

<span data-ttu-id="7d854-109">في إصدارات التطبيق التي تسبق الإصدار 10.0.1، يتم حساب التكاليف التلقائية على مستوى الرأس التي لديها علاقة وضع تسليم معينة فقط عند وجود تطابق مع وضع التسليم المحدد في رأس أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7d854-109">In versions of the app earlier than version 10.0.1, header-level auto-charges that have a specific mode of delivery relation are calculated only when there is a match with the mode of delivery that is defined on the sales order header.</span></span>

<span data-ttu-id="7d854-110">على سبيل المثال، يتم تحديد التكاليف التلقائية على مستوى الرأس لوضع التسليم **99** ووضع التسليم **11**.</span><span class="sxs-lookup"><span data-stu-id="7d854-110">For example, header-level auto-charges are defined for mode of delivery **99** and mode of delivery **11**.</span></span> <span data-ttu-id="7d854-111">يتم إنشاء أمر مبيعات، ويتم تحديد وضع التسليم **99** في رأس أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7d854-111">A sales order is created, and mode of delivery **99** is defined on the order header.</span></span> <span data-ttu-id="7d854-112">ومع ذلك، يتم إعداد بعض بنود المبيعات بحيث يتم شحنها باستخدام وضع التسليم **11**.</span><span class="sxs-lookup"><span data-stu-id="7d854-112">However, some of the sale lines are set up so that they're shipped by using mode of delivery **11**.</span></span> <span data-ttu-id="7d854-113">في هذه الحالة، تؤخذ في الاعتبار فقط التكاليف على مستوى الرأس المرتبطة بطريقة التسليم **99** ويتم تطبيقها على أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7d854-113">In this case, only the header-level charges that are linked to mode of delivery **99** are considered and applied to the sales order.</span></span>

<span data-ttu-id="7d854-114">في Commerce، تتسم التكاليف على مستوى الرأس بميزة إضافية تسمح لك بتحديد [تكوين التكاليف المرتبطة بمستويات](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) التي تستند إلى قيمة الأمر.</span><span class="sxs-lookup"><span data-stu-id="7d854-114">In Commerce, the header-level charges have an additional feature that lets you define a [tiered charge configuration](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) that is based on the order value.</span></span> <span data-ttu-id="7d854-115">على سبيل المثال، إذا تراوحت قيمة أمر المبيعات بين 50.00 و200.00 دولار، فقد ترغب المؤسسة في فرض تكلفة شحن قيمتها 5.00 دولار.</span><span class="sxs-lookup"><span data-stu-id="7d854-115">For example, if the order value is between $50.00 and $200.00, an organization might want to charge a freight charge of $5.00.</span></span> <span data-ttu-id="7d854-116">ولكن إذا تراوحت قيمة أمر المبيعات بين 200.01 و500.00، فإن تكلفة الشحن قد تكون 4.00 دولار.</span><span class="sxs-lookup"><span data-stu-id="7d854-116">However, if the order value is between $200.01 and $500.00, the freight charge might be $4.00.</span></span>

<span data-ttu-id="7d854-117">تريد بعض المؤسسات الاستفادة من فوائد حساب التكاليف المرتبطة بمستويات المتوفرة مع التكاليف على مستوى الرأس.</span><span class="sxs-lookup"><span data-stu-id="7d854-117">Some organizations want the benefits of the tiered charge calculation that is provided with header-level charges.</span></span> <span data-ttu-id="7d854-118">ولكن في السيناريوهات التي تتضمن أوضاع تسيم مختلطة، تريد هذه المؤسسات التأكد من أن التكاليف المحسوبة تستند إلى مطابقة مع وضع التسليم المحدد لكل بند مبيعات.</span><span class="sxs-lookup"><span data-stu-id="7d854-118">However, in scenarios that involve mixed modes of delivery, they also want to make sure that the charges that are calculated are based on a match with the mode of delivery that is defined on each sales line.</span></span>

<span data-ttu-id="7d854-119">يمكنك الآن تكوين التكاليف التلقائية على مستوى الرأس بحيث تؤخذ في الاعتبار جميع =أوضاع التسليم في أمر المبيعات عند حساب التكاليف.</span><span class="sxs-lookup"><span data-stu-id="7d854-119">You can now configure header-level auto-charges so that all modes of delivery on the order are considered when charges are calculated.</span></span> <span data-ttu-id="7d854-120">تتطلب هذه الوظيفة منطق حساب أكثر تعقيدًا لاحتساب التكاليف على مستوى الرأس.</span><span class="sxs-lookup"><span data-stu-id="7d854-120">This functionality requires a more complex calculation logic to calculate the header-level charges.</span></span> <span data-ttu-id="7d854-121">يجمع المنطق جميع الأصناف التي يتم شحنها باستخدام وضع التسليم نفسه، ويُعامل هذه المجموعة على أنها مجموعة الحساب للأصناف عند حساب التكاليف التلقائية على مستوى الرأس.</span><span class="sxs-lookup"><span data-stu-id="7d854-121">The logic groups together all the items that are shipped using the same mode of delivery, and it treats that group as the calculation group for the items when it calculates the header-level auto-charges.</span></span> <span data-ttu-id="7d854-122">فيما يتعلق بالأصناف التي لديها وضع التسليم نفسه، يتم حساب التكاليف التلقائية استنادًا إلى قيمة المبيعات المجمعة للأصناف.</span><span class="sxs-lookup"><span data-stu-id="7d854-122">For items that have the same mode of delivery, auto-charges are calculated based on the combined sales value of the items.</span></span> <span data-ttu-id="7d854-123">وبهذه الطريقة، يتم تحديد مستوى التكاليف التلقائية المناسبة.</span><span class="sxs-lookup"><span data-stu-id="7d854-123">In this way, the appropriate auto-charge tier is determined.</span></span>

<span data-ttu-id="7d854-124">بعد الحصول على التكاليف التلقائية المناسبة على مستوى الرأس لبنود المبيعات التي يتم شحنها باستخدام وضع التسليم نفسه، يتم توزيع التكاليف المحسوبة على مستوى بنود المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7d854-124">After the appropriate header-level charges are obtained for the sales lines that are shipped using the same mode of delivery, the calculated charges are prorated down to the sales line level.</span></span> <span data-ttu-id="7d854-125">ولأن هذه التكاليف هي على مستوى بنود المبيعات وليس على مستوى الرأس، يتم إنشاء ارتباط أكثر تحديدًا بين الصنف وقيمة التكاليف التي يتم حسابه له.</span><span class="sxs-lookup"><span data-stu-id="7d854-125">Because these charges are at the line level and not kept at the header level, a more specific link is made between the item and the charge value that calculated for it.</span></span> <span data-ttu-id="7d854-126">قد يكون هذا السلوك مفيدًا في سيناريوهات الإرجاع الجزئية، حيث تريد المؤسسة استرداد جزء فقط من التكاليف بدلاً من التكاليف الكاملة عند إرجاع بعض الأصناف فقط.</span><span class="sxs-lookup"><span data-stu-id="7d854-126">This behavior can be useful in partial return scenarios, where an organization wants to refund only part of the charge instead of the whole charge when only some items are returned.</span></span>

## <a name="scenarios"></a><span data-ttu-id="7d854-127">السيناريوهات</span><span class="sxs-lookup"><span data-stu-id="7d854-127">Scenarios</span></span>

<span data-ttu-id="7d854-128">سنقدم فيما يلي سيناريوهين نموذجيين يوضحان كيفية حساب هذه المصاريف عند استخدام الوظيفة الجديدة ومتى يتم استخدامها.</span><span class="sxs-lookup"><span data-stu-id="7d854-128">The following two sample scenarios outline how these charges are calculated both when the new functionality is used and when it isn't used.</span></span>

### <a name="scenario-1"></a><span data-ttu-id="7d854-129">السيناريو 1</span><span class="sxs-lookup"><span data-stu-id="7d854-129">Scenario 1</span></span>

<span data-ttu-id="7d854-130">يوضح هذا السيناريو السلوك عند تعيين الخيار **توزيع تكاليف الرأس لمطابقة بنود المبيعات‬** إلى **لا** في إعداد التكاليف التلقائية.</span><span class="sxs-lookup"><span data-stu-id="7d854-130">This scenario outlines the behavior when the **Pro-rate to matching sales lines** option is set to **No** in the auto-charge setup.</span></span> <span data-ttu-id="7d854-131">(السلوك يعادل سلوك التكاليف التلقائية على مستوى الرأس في إصدارات التطبيق التي تسبق الإصدار 10.0.1.)</span><span class="sxs-lookup"><span data-stu-id="7d854-131">(The behavior is equivalent to the behavior of header-level charges in app versions that are earlier than version 10.0.1.)</span></span>

<span data-ttu-id="7d854-132">في هذا السيناريو، قامت المؤسسة بتعريف التكاليف التلقائية على مستوى الرأس لعلاقة وضع التسليم **99** وعلاقة وضع التسليم **11**.</span><span class="sxs-lookup"><span data-stu-id="7d854-132">In this scenario, the organization has defined header-level charges for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="7d854-133">لم يتم تكوين تكاليف تلقائية لوضع التسليم **21**.</span><span class="sxs-lookup"><span data-stu-id="7d854-133">No auto-charges are configured for mode of delivery **21**.</span></span>

![التكاليف التلقائية لوضع التسليم 99 عند مطابقة توزيع البنود متوقفة عن تشغيل](media/99_disabled.png)

![التكاليف التلقائية لوضع التسليم 11 عند مطابقة توزيع البنود متوقفة عن تشغيل](media/11_disabled.png)

<span data-ttu-id="7d854-136">يتم إنشاء أمر مبيعات في مركز الاتصال مع تعيين وضع التسليم إلى **99**.</span><span class="sxs-lookup"><span data-stu-id="7d854-136">A sales order is created in the call center, and the mode of delivery is set to **99**.</span></span> <span data-ttu-id="7d854-137">يتضمن هذا الأمر خمسة أصناف.</span><span class="sxs-lookup"><span data-stu-id="7d854-137">This order contains five items.</span></span> <span data-ttu-id="7d854-138">تم تكوين بندين في أمر المبيعات لاستخدام وضع التسليم **99**، وتم تكوين بندين لاستخدام وضع التسليم **11**، وتم تكوين بند واحد لاستخدام وضع التسليم **21**، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="7d854-138">Two order lines have been configured to use mode of delivery **99**, two lines have been configured to use mode of delivery **11**, and one line has been configured to use mode of delivery **21**, as shown in the following table.</span></span>

| <span data-ttu-id="7d854-139">الصنف</span><span class="sxs-lookup"><span data-stu-id="7d854-139">Item</span></span>  | <span data-ttu-id="7d854-140">كمية السطر</span><span class="sxs-lookup"><span data-stu-id="7d854-140">Line quantity</span></span> | <span data-ttu-id="7d854-141">وضع التسليم</span><span class="sxs-lookup"><span data-stu-id="7d854-141">Delivery mode</span></span> | <span data-ttu-id="7d854-142">السعر لكل وحدة</span><span class="sxs-lookup"><span data-stu-id="7d854-142">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="7d854-143">81331</span><span class="sxs-lookup"><span data-stu-id="7d854-143">81331</span></span> | <span data-ttu-id="7d854-144">1</span><span class="sxs-lookup"><span data-stu-id="7d854-144">1</span></span>             | <span data-ttu-id="7d854-145">11</span><span class="sxs-lookup"><span data-stu-id="7d854-145">11</span></span>            | <span data-ttu-id="7d854-146">10 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-146">$10</span></span>            |
| <span data-ttu-id="7d854-147">81332</span><span class="sxs-lookup"><span data-stu-id="7d854-147">81332</span></span> | <span data-ttu-id="7d854-148">1</span><span class="sxs-lookup"><span data-stu-id="7d854-148">1</span></span>             | <span data-ttu-id="7d854-149">99</span><span class="sxs-lookup"><span data-stu-id="7d854-149">99</span></span>            | <span data-ttu-id="7d854-150">50 دولارًا</span><span class="sxs-lookup"><span data-stu-id="7d854-150">$50</span></span>            |
| <span data-ttu-id="7d854-151">81333</span><span class="sxs-lookup"><span data-stu-id="7d854-151">81333</span></span> | <span data-ttu-id="7d854-152">2</span><span class="sxs-lookup"><span data-stu-id="7d854-152">2</span></span>             | <span data-ttu-id="7d854-153">11</span><span class="sxs-lookup"><span data-stu-id="7d854-153">11</span></span>            | <span data-ttu-id="7d854-154">30 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-154">$30</span></span>            |
| <span data-ttu-id="7d854-155">81334</span><span class="sxs-lookup"><span data-stu-id="7d854-155">81334</span></span> | <span data-ttu-id="7d854-156">3</span><span class="sxs-lookup"><span data-stu-id="7d854-156">3</span></span>             | <span data-ttu-id="7d854-157">99</span><span class="sxs-lookup"><span data-stu-id="7d854-157">99</span></span>            | <span data-ttu-id="7d854-158">10 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-158">$10</span></span>            |
| <span data-ttu-id="7d854-159">81334</span><span class="sxs-lookup"><span data-stu-id="7d854-159">81334</span></span> | <span data-ttu-id="7d854-160">3</span><span class="sxs-lookup"><span data-stu-id="7d854-160">3</span></span>             | <span data-ttu-id="7d854-161">21</span><span class="sxs-lookup"><span data-stu-id="7d854-161">21</span></span>            | <span data-ttu-id="7d854-162">5 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-162">$5</span></span>             |

<span data-ttu-id="7d854-163">في هذا السيناريو، يتم تقييم الأمر بكامله في مقابل جدول التكاليف التلقائية لوضع التسليم **99**.</span><span class="sxs-lookup"><span data-stu-id="7d854-163">In this scenario, the whole order is evaluated against the auto-charge table for mode of delivery **99**.</span></span> <span data-ttu-id="7d854-164">ويتم استخدام المجموع الكامل لبنود أمر المبيعات لتحديد مستوى مطابق في تكوين التكاليف التلقائية، ويتم تطبيق هذه التكاليف على مستوى رأس أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7d854-164">The full total of all sales lines is used to determine a matching tier in the auto-charge configuration, and this charge is applied at the order header level.</span></span> <span data-ttu-id="7d854-165">في هذا المثال، المبلغ الإجمالي لأمر المبيعات هو 165.00 دولار ويتم تطبيق تكاليف الشحن بقيمة 15.00 دولار على رأس أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7d854-165">In this example, the order total is $165.00, and the $15.00 freight charge is applied to the order header.</span></span> <span data-ttu-id="7d854-166">لا يتم إطلاقًا الإشارة إلى التكاليف التلقائية التي تم تكوينها لوضع التسليم **11** أو تطبيقها.</span><span class="sxs-lookup"><span data-stu-id="7d854-166">Auto-charges that are configured for mode of delivery **11** are never referenced or applied.</span></span>

<span data-ttu-id="7d854-167">في هذا السيناريو، إذا قام أحد العملاء بإرجاع بعض الأصناف في أمر المبيعات، وإذا [تم تكوين كود التكلفة بحيث يمكن استرداده](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2)، يتم تطبيق التكاليف التلقائية الإجمالية على مستوى الرأس بطريقة منهجية على المبلغ المسترد، حتى لو تم إرجاع بعض الأصناف فقط.</span><span class="sxs-lookup"><span data-stu-id="7d854-167">In this scenario, if a customer returns some of the items on the order, and if the [charge code has been configured so that it will be refunded](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), the total header-level charge is systematically applied to the refund, even if only some of the items are returned.</span></span>

### <a name="scenario-2"></a><span data-ttu-id="7d854-168">السيناريو 2</span><span class="sxs-lookup"><span data-stu-id="7d854-168">Scenario 2</span></span>

<span data-ttu-id="7d854-169">في هذا السيناريو، تم تعريف التكاليف التلقائية على مستوى الرأس لعلاقة وضع التسليم **99** وعلاقة وضع التسليم **11**.</span><span class="sxs-lookup"><span data-stu-id="7d854-169">In this scenario, header-level charges are defined for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="7d854-170">ومع ذلك، تم تعيين الخيار **توزيع تكاليف الرأس لمطابقة بنود المبيعات‬** إلى **نعم** لجداول التكاليف التلقائية هذه.</span><span class="sxs-lookup"><span data-stu-id="7d854-170">However, the **Pro-rate to matching sales lines** option is set to **Yes** for these auto-charge tables.</span></span>

![التكاليف التلقائية لوضع التسليم 99 عند مطابقة توزيع البنود قيد التشغيل](media/99_enabled.png)

![التكاليف التلقائية لوضع التسليم 11 عند مطابقة توزيع البنود قيد التشغيل](media/11_enabled.png)

<span data-ttu-id="7d854-173">يستخدم هذا السيناريو أمر المبيعات نفسه الذي يتضمن خمسة بنود.</span><span class="sxs-lookup"><span data-stu-id="7d854-173">This scenario uses the same sales order that contains five lines.</span></span> <span data-ttu-id="7d854-174">تم تعيين وضع التسليم على رأس الأمر إلى **99**، ولكن تم تكوين وضع التسليم لكل صنف في أمر المبيعات كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="7d854-174">The mode of delivery on the order header is set to **99**, but the mode of delivery for each item on the sales order is configured as shown in the following table.</span></span>

| <span data-ttu-id="7d854-175">الصنف</span><span class="sxs-lookup"><span data-stu-id="7d854-175">Item</span></span>  | <span data-ttu-id="7d854-176">كمية السطر</span><span class="sxs-lookup"><span data-stu-id="7d854-176">Line quantity</span></span> | <span data-ttu-id="7d854-177">وضع التسليم</span><span class="sxs-lookup"><span data-stu-id="7d854-177">Delivery mode</span></span> | <span data-ttu-id="7d854-178">السعر لكل وحدة</span><span class="sxs-lookup"><span data-stu-id="7d854-178">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="7d854-179">81331</span><span class="sxs-lookup"><span data-stu-id="7d854-179">81331</span></span> | <span data-ttu-id="7d854-180">1</span><span class="sxs-lookup"><span data-stu-id="7d854-180">1</span></span>             | <span data-ttu-id="7d854-181">11</span><span class="sxs-lookup"><span data-stu-id="7d854-181">11</span></span>            | <span data-ttu-id="7d854-182">10 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-182">$10</span></span>            |
| <span data-ttu-id="7d854-183">81332</span><span class="sxs-lookup"><span data-stu-id="7d854-183">81332</span></span> | <span data-ttu-id="7d854-184">1</span><span class="sxs-lookup"><span data-stu-id="7d854-184">1</span></span>             | <span data-ttu-id="7d854-185">99</span><span class="sxs-lookup"><span data-stu-id="7d854-185">99</span></span>            | <span data-ttu-id="7d854-186">50 دولارًا</span><span class="sxs-lookup"><span data-stu-id="7d854-186">$50</span></span>            |
| <span data-ttu-id="7d854-187">81333</span><span class="sxs-lookup"><span data-stu-id="7d854-187">81333</span></span> | <span data-ttu-id="7d854-188">2</span><span class="sxs-lookup"><span data-stu-id="7d854-188">2</span></span>             | <span data-ttu-id="7d854-189">11</span><span class="sxs-lookup"><span data-stu-id="7d854-189">11</span></span>            | <span data-ttu-id="7d854-190">30 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-190">$30</span></span>            |
| <span data-ttu-id="7d854-191">81334</span><span class="sxs-lookup"><span data-stu-id="7d854-191">81334</span></span> | <span data-ttu-id="7d854-192">3</span><span class="sxs-lookup"><span data-stu-id="7d854-192">3</span></span>             | <span data-ttu-id="7d854-193">99</span><span class="sxs-lookup"><span data-stu-id="7d854-193">99</span></span>            | <span data-ttu-id="7d854-194">10 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-194">$10</span></span>            |
| <span data-ttu-id="7d854-195">81334</span><span class="sxs-lookup"><span data-stu-id="7d854-195">81334</span></span> | <span data-ttu-id="7d854-196">3</span><span class="sxs-lookup"><span data-stu-id="7d854-196">3</span></span>             | <span data-ttu-id="7d854-197">21</span><span class="sxs-lookup"><span data-stu-id="7d854-197">21</span></span>            | <span data-ttu-id="7d854-198">5 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-198">$5</span></span>             |

<span data-ttu-id="7d854-199">نظرًا لتعيين تكوين التكاليف التلقائية بحيث يتم توزيعها لمطابقة بنود المبيعات‬، ينفذ النظام خطوات الحساب التالية.</span><span class="sxs-lookup"><span data-stu-id="7d854-199">Because the auto-charge configuration is set to prorate to matching sales lines, the system performs the following calculation steps.</span></span>

1. <span data-ttu-id="7d854-200">تُجمع معًا جميع الأصناف التي لديها وضع التسليم نفسه، ويقوم النظام بحساب إجمالي قيمة المنتجات للأصناف الموجودة في المجموعة.</span><span class="sxs-lookup"><span data-stu-id="7d854-200">All items that have the same mode of delivery are grouped together, and the system calculates the total product value of the items in the group.</span></span>

    <span data-ttu-id="7d854-201">**وضع التسليم 11**</span><span class="sxs-lookup"><span data-stu-id="7d854-201">**Delivery mode 11**</span></span>

    - <span data-ttu-id="7d854-202">الصنف 81331، الكمية 1 = 10 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-202">Item 81331, quantity 1 = $10</span></span>
    - <span data-ttu-id="7d854-203">الصنف 81333، الكمية 2 = 60 دولار صافي المبلغ (30 دولار لكل وحدة)</span><span class="sxs-lookup"><span data-stu-id="7d854-203">Item 81333, quantity 2 = $60 net ($30 per unit)</span></span>
    - <span data-ttu-id="7d854-204">**إجمالي قيمة المنتجات لوضع التسليم 11 = 70‏‎ دولار**</span><span class="sxs-lookup"><span data-stu-id="7d854-204">**Total product value for delivery mode 11 = $70**</span></span>

    <span data-ttu-id="7d854-205">**وضع التسليم 99**</span><span class="sxs-lookup"><span data-stu-id="7d854-205">**Delivery mode 99**</span></span>

    - <span data-ttu-id="7d854-206">الصنف 81332، الكمية 1 = 50 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-206">Item 81332, quantity 1 = $50</span></span>
    - <span data-ttu-id="7d854-207">الصنف 81334، الكمية 3 = 30 دولار صافي المبلغ</span><span class="sxs-lookup"><span data-stu-id="7d854-207">Item 81334, quantity 3 = $30 net</span></span>
    - <span data-ttu-id="7d854-208">**إجمالي قيمة المنتجات لوضع التسليم 99 = 80‏‎ دولار**</span><span class="sxs-lookup"><span data-stu-id="7d854-208">**Total product value for delivery mode 99 = $80**</span></span>

    <span data-ttu-id="7d854-209">**وضع التسليم 21**</span><span class="sxs-lookup"><span data-stu-id="7d854-209">**Delivery mode 21**</span></span>

    - <span data-ttu-id="7d854-210">الصنف 81334، الكمية 3 = 15 دولار صافي المبلغ</span><span class="sxs-lookup"><span data-stu-id="7d854-210">Item 81334, quantity 3 = $15 net</span></span>
    - <span data-ttu-id="7d854-211">**إجمالي قيمة المنتجات لوضع التسليم 21 = 15‏‎ دولار**</span><span class="sxs-lookup"><span data-stu-id="7d854-211">**Total product value for delivery mode 21 = $15**</span></span>

2. <span data-ttu-id="7d854-212">يبحث النظام عن تكوين التكاليف التلقائية على مستوى الرأس التي تتطابق مع إعدادات وضع التسليم والعميل لكل مجموعة أصناف.</span><span class="sxs-lookup"><span data-stu-id="7d854-212">The system looks for the configuration for header-level auto-charges that matches the customer and mode of delivery settings for each group of items.</span></span> <span data-ttu-id="7d854-213">وإذا تم العثور على التكوين، فسيبحث النظام في التكوين المرتبط بالطبقات للعثور على التكاليف التي يجب تطبيقها، استنادًا إلى إجمالي قيمة المنتجات للأصناف في مجموعة وضع التسليم.</span><span class="sxs-lookup"><span data-stu-id="7d854-213">If the configuration is found, the system looks in the tiered configuration to find the charge that should be applied, based on the total product value of items in the mode of delivery group.</span></span>

    <span data-ttu-id="7d854-214">**وضع التسليم 11**</span><span class="sxs-lookup"><span data-stu-id="7d854-214">**Delivery mode 11**</span></span>

    - <span data-ttu-id="7d854-215">إجمالي قيمة المنتج = 70 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-215">Total product value = $70</span></span>
    - <span data-ttu-id="7d854-216">**قيمة التكاليف = 7 دولار**</span><span class="sxs-lookup"><span data-stu-id="7d854-216">**Charge value = $7**</span></span>

    <span data-ttu-id="7d854-217">**وضع التسليم 99**</span><span class="sxs-lookup"><span data-stu-id="7d854-217">**Delivery mode 99**</span></span>

    - <span data-ttu-id="7d854-218">إجمالي قيمة المنتج = 80 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-218">Total product value = $80</span></span>
    - <span data-ttu-id="7d854-219">**قيمة التكاليف = 15 دولار**</span><span class="sxs-lookup"><span data-stu-id="7d854-219">**Charge value = $15**</span></span>

    <span data-ttu-id="7d854-220">**وضع التسليم 21**</span><span class="sxs-lookup"><span data-stu-id="7d854-220">**Delivery mode 21**</span></span>

    - <span data-ttu-id="7d854-221">إجمالي قيمة المنتج = 15 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-221">Total product value = $15</span></span>
    - <span data-ttu-id="7d854-222">**قيمة التكاليف = 0 دولار** (لم يتم تكوين التكاليف التلقائية لهذه المجموعة المكونة من عميل ووضع تسليم.)</span><span class="sxs-lookup"><span data-stu-id="7d854-222">**Charge value = $0** (No auto-charges have been configured for this combination of a customer and a mode of delivery.)</span></span>

    ![تقع تكاليف وضع التسليم 11 في المستوى المميز](media/step2mode11.png)

    ![تقع تكاليف وضع التسليم 99 في المستوى المميز](media/step2mode99.png)

3. <span data-ttu-id="7d854-225">يقوم النظام بحساب قيمة التكاليف التي يجب تطبيقها على كل بند، استنادًا إلى منطق التوزيع الذي يأخذ في الاعتبار القيمة النسبية للبند بالنسبة إلى إجمالي قيمة المنتجات للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="7d854-225">The system calculates the charge value that should be applied to each line, based on proration logic that considers the proportional value of the line in relation to the group's total product value.</span></span>

    <span data-ttu-id="7d854-226">**وضع التسليم 11**</span><span class="sxs-lookup"><span data-stu-id="7d854-226">**Delivery mode 11**</span></span>

    - <span data-ttu-id="7d854-227">قيمة التكاليف = 7 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-227">Charge value = $7</span></span>
    - <span data-ttu-id="7d854-228">قيمة منتجات المجموعة= 70 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-228">Group product value = $70</span></span>
    - <span data-ttu-id="7d854-229">قيمة البند 1 = 10 دولار (= 14.2857 بالمئة من قيمة المجموعة)</span><span class="sxs-lookup"><span data-stu-id="7d854-229">Line 1 value = $10 (= 14.2857 percent of the group value)</span></span>
    - <span data-ttu-id="7d854-230">قيمة البند 3 = 60 دولار (= 85.7143 بالمئة من قيمة المجموعة)</span><span class="sxs-lookup"><span data-stu-id="7d854-230">Line 3 value = $60 (= 85.7143 percent of the group value)</span></span>
    - <span data-ttu-id="7d854-231">**تكاليف البند للبند 1 = 1 دولار**</span><span class="sxs-lookup"><span data-stu-id="7d854-231">**Line charge for line 1 = $1**</span></span>
    - <span data-ttu-id="7d854-232">**تكاليف البند للبند 3 = 6 دولار**</span><span class="sxs-lookup"><span data-stu-id="7d854-232">**Line charge for line 3 = $6**</span></span>

    <span data-ttu-id="7d854-233">**وضع التسليم 99**</span><span class="sxs-lookup"><span data-stu-id="7d854-233">**Delivery mode 99**</span></span>

    - <span data-ttu-id="7d854-234">قيمة التكاليف = 15 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-234">Charge value = $15</span></span>
    - <span data-ttu-id="7d854-235">قيمة منتجات المجموعة= 80 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-235">Group product value = $80</span></span>
    - <span data-ttu-id="7d854-236">قيمة البند 2 = 50 دولار (= 62.5 بالمئة من قيمة المجموعة)</span><span class="sxs-lookup"><span data-stu-id="7d854-236">Line 2 value = $50 (= 62.5 percent of the group value)</span></span>
    - <span data-ttu-id="7d854-237">قيمة البند 4 = 30 دولار (= 37.5 بالمئة من قيمة المجموعة)</span><span class="sxs-lookup"><span data-stu-id="7d854-237">Line 4 value = $30 (= 37.5 percent of the group value)</span></span>
    - <span data-ttu-id="7d854-238">**تكاليف البند للبند 2 = 9.38 دولار**</span><span class="sxs-lookup"><span data-stu-id="7d854-238">**Line charge for line 2 = $9.38**</span></span>
    - <span data-ttu-id="7d854-239">**تكاليف البند للبند 4 = 5.62 دولار**</span><span class="sxs-lookup"><span data-stu-id="7d854-239">**Line charge for line 4 = $5.62**</span></span>

    <span data-ttu-id="7d854-240">**وضع التسليم 21**</span><span class="sxs-lookup"><span data-stu-id="7d854-240">**Delivery mode 21**</span></span>

    - <span data-ttu-id="7d854-241">قيمة التكاليف = 0 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-241">Charge value = $0</span></span>
    - <span data-ttu-id="7d854-242">قيمة منتجات المجموعة= 15 دولار</span><span class="sxs-lookup"><span data-stu-id="7d854-242">Group product value = $15</span></span>
    - <span data-ttu-id="7d854-243">قيمة البند 5 = 15 دولار (= 100 بالمئة من قيمة المجموعة)</span><span class="sxs-lookup"><span data-stu-id="7d854-243">Line 5 value = $15 (= 100 percent of the group value)</span></span>
    - <span data-ttu-id="7d854-244">**تكاليف البند للبند 5 = 0 دولار**</span><span class="sxs-lookup"><span data-stu-id="7d854-244">**Line charge for line 5 = $0**</span></span>

<span data-ttu-id="7d854-245">وبالتالي، سيتم تعيين تكاليف شحن بقيمة 5.62 دولار للصنف 81334، لهذا المثال.</span><span class="sxs-lookup"><span data-stu-id="7d854-245">Therefore, for this example, item 81334 will be assigned a freight charge of $5.62.</span></span> <span data-ttu-id="7d854-246">يمكنك عرض هذه التكاليف في صفحة **الاحتفاظ بالتكاليف** لبند المبيعات.</span><span class="sxs-lookup"><span data-stu-id="7d854-246">You can view these charges on the **Maintain charges** page for the sales line.</span></span> <span data-ttu-id="7d854-247">يُظهر الرسم التوضيحي التالي كيف تبدو هذه الصفحة للصنف 81334.</span><span class="sxs-lookup"><span data-stu-id="7d854-247">The following illustration shows what this page looks like for item 81334.</span></span>

![التكاليف الموزعة على بند أمر المبيعات للصنف 81334](media/proratedlinecharge.png)

<span data-ttu-id="7d854-249">عند استخدام أسلوب الحساب هذا في سيناريو إرجاع جزئي، إذا كان كود التكاليف قابلاً الاسترداد، فسيتم استرداد فقط جزء التكاليف الذي تم تخصيصه لهذا البند فقط عند إرجاع الصنف.</span><span class="sxs-lookup"><span data-stu-id="7d854-249">When this method of calculation is used in a partial return scenario, if the charge code is refundable, only the part of the charge that is allocated to that line will be refunded when the item is returned.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d854-250">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="7d854-250">Additional resources</span></span>

[<span data-ttu-id="7d854-251">التكاليف التلقائية المتقدمة ‬للقناة متعددة الاتجاهات</span><span class="sxs-lookup"><span data-stu-id="7d854-251">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="7d854-252">تمكين التكاليف التلقائية وتكوينها حسب القناة</span><span class="sxs-lookup"><span data-stu-id="7d854-252">Enable and configure auto charges by channel</span></span>](auto-charges-by-channel.md)
