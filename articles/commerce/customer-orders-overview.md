---
title: أوامر العميل في ‏‫نقطة بيع حديثة‬ (MPOS)
description: يقدم هذا الموضوع معلومات حول أوامر العميل في نقطة البيع الحديثة (MPOS). تُعرف أوامر العملاء أيضًا بالأوامر الخاصة. يشمل الموضوع مناقشة المحددات ذات الصلة وتدفقات الحركة.
author: josaw1
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 87d1217204e0c5cb22f567793b043bf399ca5685
ms.sourcegitcommit: b07434f2bd6db67d8dd712f096329acc902751ae
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/18/2020
ms.locfileid: "3699359"
---
# <a name="customer-orders-in-modern-pos-mpos"></a><span data-ttu-id="db088-105">أوامر العميل في ‏‫نقطة بيع حديثة‬ (MPOS)</span><span class="sxs-lookup"><span data-stu-id="db088-105">Customer orders in Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="db088-106">يقدم هذا الموضوع معلومات حول أوامر العميل في نقطة البيع الحديثة (MPOS).</span><span class="sxs-lookup"><span data-stu-id="db088-106">This topic provides information about customer orders in Modern POS (MPOS).</span></span> <span data-ttu-id="db088-107">تُعرف أوامر العملاء أيضًا بالأوامر الخاصة.</span><span class="sxs-lookup"><span data-stu-id="db088-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="db088-108">يشمل الموضوع مناقشة المحددات ذات الصلة وتدفقات الحركة.</span><span class="sxs-lookup"><span data-stu-id="db088-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="db088-109">في عالم تهمين عليه قنوات التجارة، يقدم العديد من بائعي التجزئة خيار أوامر العميل أو الأوامر الخاصة، لاستيفاء المنتجات المختلفة وتلبية المتطلبات.</span><span class="sxs-lookup"><span data-stu-id="db088-109">In an omni-channel commerce world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="db088-110">وفيما يلي بعض السيناريوهات النموذجية:</span><span class="sxs-lookup"><span data-stu-id="db088-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="db088-111">يريد أحد العملاء أن يتم تسليم المنتجات إلى عنوان محدد في تاريخ محدد.</span><span class="sxs-lookup"><span data-stu-id="db088-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="db088-112">يرغب أحد العملاء في انتقاء المنتجات من متجر أو من موقع يختلف عن المتجر أو الموقع الذي اشتري منه العميل تلك المنتجات.</span><span class="sxs-lookup"><span data-stu-id="db088-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="db088-113">ويرغب العميل في قيام شخص آخر بانتقاء المنتجات التي اشتراها العميل.</span><span class="sxs-lookup"><span data-stu-id="db088-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="db088-114">يستخدم تجار التجزئة أيضًا أوامر العميل للحد من المبيعات المفقودة والتي قد يتسبب فيها انقطاع المخزون، لأنه يمكن تسليم البضاعة أو انتقائها في وقت أو مكان آخر.</span><span class="sxs-lookup"><span data-stu-id="db088-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="db088-115">إعداد أوامر العملاء</span><span class="sxs-lookup"><span data-stu-id="db088-115">Set up customer orders</span></span>

<span data-ttu-id="db088-116">فيما يلي بعض المعلمات التي يمكن تعيينها على صفحة **معلمات التجارة** لتحديد كيفية استيفاء طلبات العملاء:</span><span class="sxs-lookup"><span data-stu-id="db088-116">Here are some of the parameters that can be set on the **Commerce parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="db088-117">**النسبة المئوية الافتراضية للإيداع** – قم بتحديد المبلغ الذي يجب على العميل دفعه كإيداع قبل تأكيد الأمر.</span><span class="sxs-lookup"><span data-stu-id="db088-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="db088-118">يتم حساب مبلغ الإيداع الافتراضي كنسبة مئوية لقيمة الأمر.</span><span class="sxs-lookup"><span data-stu-id="db088-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="db088-119">بناءً على الامتيازات، قد يصبح موظف المتجر قادرًا على تجاوز المبلغ باستخدم **تجاوز الإيداع**.</span><span class="sxs-lookup"><span data-stu-id="db088-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="db088-120">**النسبة المئوية لرسوم الإلغاء** – إذا كان سيتم تطبيق رسوم عند إلغاء أمر العميل، حدد مبلغ هذه الرسوم.</span><span class="sxs-lookup"><span data-stu-id="db088-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="db088-121">**رمز رسوم الإلغاء** – إذا كان سيتم تطبيق رسوم عند إلغاء أمر العميل، فسوف تنعكس هذه الرسوم تحت رمز الرسوم في أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="db088-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="db088-122">استخدم هذه المعلمة لتخديد رمز رسوم الإلغاء.</span><span class="sxs-lookup"><span data-stu-id="db088-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="db088-123">**رمز رسوم الشحن** – يمكن لتجار التجزئة تحصيل رسوم إضافية لشحن البضائع إلى أحد العملاء.</span><span class="sxs-lookup"><span data-stu-id="db088-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="db088-124">وسوف ينعكس مبلغ رسوم الشحن هذه ضمن رمز الرسوم في أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="db088-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="db088-125">استخدم هذه المعلمة لتعيين رمز رسوم الشحن إلى رسوم الشحن على أمر العميل.</span><span class="sxs-lookup"><span data-stu-id="db088-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="db088-126">**المبلغ المسترد من تكاليف الشحن** -حدد إذا ماكنت رسوم الشحن المرتبطة بأمر العميل قابلة للاسترداد أم لا.</span><span class="sxs-lookup"><span data-stu-id="db088-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="db088-127">**الحد الأقصى للمبلغ بدون الموافقة** – إذا كانت مصاريف الشحن قابلة للاسترداد، حدد الحد الأقصى لمبلغ رسوم الشحن الذي سيتم استرداده عبر أوامر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="db088-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="db088-128">إذا تم تجاوز هذا المبلغ، فمن ثم يلزم تجاوز المدير من أجل الاستمرار في إرجاع المبلغ المسترد.</span><span class="sxs-lookup"><span data-stu-id="db088-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="db088-129">لاستيعاب السيناريوهات التالية، يمكن أن يتجاوز رد رسوم الشحن المبلغ المدفوع أصلًا:</span><span class="sxs-lookup"><span data-stu-id="db088-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="db088-130">يتم تطبيق الرسوم على مستوى عنوان أمر المبيعات، وعندما يتم إرجاع بعض كميات من سطر المنتج، لا يمكن تحديد الحد الأقصى لاسترداد رسوم الشحن المسموح بها للمنتجات والكمية، بنفس طريقة تحديدها لكافة العملاء.</span><span class="sxs-lookup"><span data-stu-id="db088-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all customers.</span></span>
    - <span data-ttu-id="db088-131">يتم تحمل مصاريف الشحن لكل مثيل للشحن.</span><span class="sxs-lookup"><span data-stu-id="db088-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="db088-132">إذا قام عميل بإرجاع منتجات لعدة مرات، وكانت سياسة تاجر التجزئة تنص على أنه يتعين على تاجر التجزئة تحمل تكلفة مصاريف إعادة الشحن، فستكون مصاريف إعادة الشحن أكثر من مصاريف الشحن الفعلية.</span><span class="sxs-lookup"><span data-stu-id="db088-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>
    
- <span data-ttu-id="db088-133">**سلوك حساب الضرائب** - **إعادة الحساب** هي الإعداد الافتراضي والتقليدي لكيفية إعادة حساب الضرائب عند إعادة استيراد الأمر إلى المكتب الخلفي.</span><span class="sxs-lookup"><span data-stu-id="db088-133">**Tax calculation behavior** - **Recalculate** is the default and traditional setting for how taxes are recalculated when the order is imported into the back office.</span></span> <span data-ttu-id="db088-134">**لا تقم بإعادة الحساب** يعطّل إعادة حساب الضريبة حتى يتم تحرير الأمر في المكتب الخلفي أو إلا إذا تم تحريره، عند تشغيل إعادة الحساب.</span><span class="sxs-lookup"><span data-stu-id="db088-134">**Don't recalculate** disables tax recalculation until or unless the order is edited in the back office, when recalculation is triggered.</span></span> 

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="db088-135">تدفق الحركة لأوامر العملاء</span><span class="sxs-lookup"><span data-stu-id="db088-135">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-modern-pos"></a><span data-ttu-id="db088-136">إنشاء أمر عميل في نقطة بيع حديثة</span><span class="sxs-lookup"><span data-stu-id="db088-136">Create a customer order in Modern POS</span></span>

1. <span data-ttu-id="db088-137">أضف عميلاً للحركة.</span><span class="sxs-lookup"><span data-stu-id="db088-137">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="db088-138">أضف منتجات إلى عربة التسوق.</span><span class="sxs-lookup"><span data-stu-id="db088-138">Add products to the cart.</span></span>
3. <span data-ttu-id="db088-139">انقر فوق **إنشاء أمر العميل**، ثم حدد نوع الأمر.</span><span class="sxs-lookup"><span data-stu-id="db088-139">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="db088-140">يمكن أن يكون نوع الأمر إما **أمر العميل** أو **عرض الأسعار**.</span><span class="sxs-lookup"><span data-stu-id="db088-140">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="db088-141">انقر فوق **تم تحديد الشحن** أو **شحن الكل** لشحن المنتجات إلى عنوان موجود في حساب العميل، حدد تاريخ الشحن المطلوب، وحدد مصاريف الشحن.</span><span class="sxs-lookup"><span data-stu-id="db088-141">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="db088-142">انقر فوق **انتقاء المُحدّد** أو **انتقاء الكل** لتحديد المنتجات التي سيتم انتقاؤها من المخزن الحالي أو من متجر آخر في تاريخ محدد.</span><span class="sxs-lookup"><span data-stu-id="db088-142">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="db088-143">قم بتحصيل مبلغ الإيداع، إذا كان الإيداع مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="db088-143">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="db088-144">تحرير أمر عميل موجود</span><span class="sxs-lookup"><span data-stu-id="db088-144">Edit an existing customer order</span></span>

1. <span data-ttu-id="db088-145">في الصفحة الرئيسية، انقر فوق **البحث عن أمر**.</span><span class="sxs-lookup"><span data-stu-id="db088-145">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="db088-146">البحث عن وتحدد الأمر المُراد تحريره.</span><span class="sxs-lookup"><span data-stu-id="db088-146">Find and select the order to edit.</span></span> <span data-ttu-id="db088-147">انقر فوق **تحرير**، الموجودة في أسفل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="db088-147">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="db088-148">انتقاء أمر</span><span class="sxs-lookup"><span data-stu-id="db088-148">Pick up an order</span></span>

1. <span data-ttu-id="db088-149">في الصفحة الرئيسية، انقر فوق **البحث عن أمر**.</span><span class="sxs-lookup"><span data-stu-id="db088-149">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="db088-150">حدد الأمر المراد انتقائه.</span><span class="sxs-lookup"><span data-stu-id="db088-150">Select the order to pick up.</span></span> <span data-ttu-id="db088-151">انقر فوق زر **الانتقاء والتعبئة**، الموجود في أسفل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="db088-151">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="db088-152">انقر فوق **انتقاء**.</span><span class="sxs-lookup"><span data-stu-id="db088-152">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="db088-153">إلغاء أمر</span><span class="sxs-lookup"><span data-stu-id="db088-153">Cancel an order</span></span>

1. <span data-ttu-id="db088-154">في الصفحة الرئيسية، انقر فوق **البحث عن أمر**.</span><span class="sxs-lookup"><span data-stu-id="db088-154">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="db088-155">حدد الأمر المُراد إلغاؤه.</span><span class="sxs-lookup"><span data-stu-id="db088-155">Select the order to cancel.</span></span> <span data-ttu-id="db088-156">انقر فوق **إلغاء**، الموجودة في أسفل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="db088-156">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="db088-157">إنشاء أمر إرجاع</span><span class="sxs-lookup"><span data-stu-id="db088-157">Create a return order</span></span>

1. <span data-ttu-id="db088-158">في الصفحة الرئيسية، انقر فوق **البحث عن أمر**.</span><span class="sxs-lookup"><span data-stu-id="db088-158">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="db088-159">حدد الأمر المُراد إرجاعه، حدد فاتورة الامر، ثم حدد سطر المنتج للبضاعة المُراد إرجاعها.</span><span class="sxs-lookup"><span data-stu-id="db088-159">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="db088-160">انقر فوق **أمر إرجاع**، الموجودة في أسفل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="db088-160">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="db088-161">تدفق الحركة غير المتزامن لأوامر العملاء</span><span class="sxs-lookup"><span data-stu-id="db088-161">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="db088-162">يمكن إنشاء أوامر العملاء من عميل نقطة البيع سواءً في وضع متزامن أو غير متزامن.</span><span class="sxs-lookup"><span data-stu-id="db088-162">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="db088-163">تمكين إنشاء أوامر العملاء في وضع غير متزامن</span><span class="sxs-lookup"><span data-stu-id="db088-163">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="db088-164">انقر **البيع بالتجزئة والتجارة** &gt; **إعداد القناة** &gt; **إعداد نقطة البيع** &gt; **ملف تعريف نقطة البيع** &gt; **ملفات تعريف الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="db088-164">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="db088-165">في علامة التبويب السريعة **عام**، قم بتعيين خيار **إنشاء أمر عميل في الوضع "غير متزامن"** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="db088-165">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="db088-166">عند تعيين الخيار **إنشاء أمر عميل في الوضع "غير متزامن"‬** إلى **نعم**، يتم إنشاء أوامر العملاء دائمًا في وضع "غير متزامن"، حتى في حال توفرت Retail Transaction Service (RTS).</span><span class="sxs-lookup"><span data-stu-id="db088-166">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="db088-167">إذا قمت بتعيين هذا الخيار إلى **لا**، يتم إنشاء أوامر العميل دائماً في وضع متزامن باستخدام خدمة حركة البيع بالتجزئة RTS.</span><span class="sxs-lookup"><span data-stu-id="db088-167">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="db088-168">عند إنشاء أوامر العملاء في الوضع "غير متزامن"، يتم سحبها وإدراجها في Commerce بسحب وظائف (P).</span><span class="sxs-lookup"><span data-stu-id="db088-168">When customer orders are created in asynchronous mode, they are pulled and inserted into Commerce by Pull (P) jobs.</span></span> <span data-ttu-id="db088-169">يتم إنشاء أوامر التوريد الطابقة عندما يتم تشغيل **مزامنة الأوامر** يدويًا أو من خلال معالجة دفعة.</span><span class="sxs-lookup"><span data-stu-id="db088-169">The corresponding sales orders are created when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db088-170">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="db088-170">Additional resources</span></span>

[<span data-ttu-id="db088-171">أوامر العملاء المختلطة</span><span class="sxs-lookup"><span data-stu-id="db088-171">Hybrid customer orders</span></span>](hybrid-customer-orders.md)
