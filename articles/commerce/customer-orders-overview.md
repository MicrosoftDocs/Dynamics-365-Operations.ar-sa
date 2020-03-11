---
title: أوامر العميل في ‏‫نقطة بيع حديثة‬ (MPOS)
description: يقدم هذا الموضوع معلومات حول أوامر العميل في نقطة البيع الحديثة (MPOS). تُعرف أوامر العملاء أيضًا بالأوامر الخاصة. يشمل الموضوع مناقشة المحددات ذات الصلة وتدفقات الحركة.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
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
ms.openlocfilehash: b8ea8339c2ad25ceed2415eb5ccf5e2048c612fa
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021439"
---
# <a name="customer-orders-in-modern-pos-mpos"></a><span data-ttu-id="a8121-105">أوامر العميل في ‏‫نقطة بيع حديثة‬ (MPOS)</span><span class="sxs-lookup"><span data-stu-id="a8121-105">Customer orders in Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a8121-106">يقدم هذا الموضوع معلومات حول أوامر العميل في نقطة البيع الحديثة (MPOS).</span><span class="sxs-lookup"><span data-stu-id="a8121-106">This topic provides information about customer orders in Modern POS (MPOS).</span></span> <span data-ttu-id="a8121-107">تُعرف أوامر العملاء أيضًا بالأوامر الخاصة.</span><span class="sxs-lookup"><span data-stu-id="a8121-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="a8121-108">يشمل الموضوع مناقشة المحددات ذات الصلة وتدفقات الحركة.</span><span class="sxs-lookup"><span data-stu-id="a8121-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="a8121-109">في عالم تهمين عليه قنوات التجارة، يقدم العديد من بائعي التجزئة خيار أوامر العميل أو الأوامر الخاصة، لاستيفاء المنتجات المختلفة وتلبية المتطلبات.</span><span class="sxs-lookup"><span data-stu-id="a8121-109">In an omni-channel commerce world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="a8121-110">وفيما يلي بعض السيناريوهات النموذجية:</span><span class="sxs-lookup"><span data-stu-id="a8121-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="a8121-111">يريد أحد العملاء أن يتم تسليم المنتجات إلى عنوان محدد في تاريخ محدد.</span><span class="sxs-lookup"><span data-stu-id="a8121-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="a8121-112">يرغب أحد العملاء في انتقاء المنتجات من متجر أو من موقع يختلف عن المتجر أو الموقع الذي اشتري منه العميل تلك المنتجات.</span><span class="sxs-lookup"><span data-stu-id="a8121-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="a8121-113">ويرغب العميل في قيام شخص آخر بانتقاء المنتجات التي اشتراها العميل.</span><span class="sxs-lookup"><span data-stu-id="a8121-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="a8121-114">يستخدم تجار التجزئة أيضًا أوامر العميل للحد من المبيعات المفقودة والتي قد يتسبب فيها انقطاع المخزون، لأنه يمكن تسليم البضاعة أو انتقائها في وقت أو مكان آخر.</span><span class="sxs-lookup"><span data-stu-id="a8121-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="a8121-115">إعداد أوامر العملاء</span><span class="sxs-lookup"><span data-stu-id="a8121-115">Set up customer orders</span></span>

<span data-ttu-id="a8121-116">فيما يلي بعض المعلمات التي يمكن تعيينها على صفحة **معلمات التجارة** لتحديد كيفية استيفاء طلبات العملاء:</span><span class="sxs-lookup"><span data-stu-id="a8121-116">Here are some of the parameters that can be set on the **Commerce parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="a8121-117">**النسبة المئوية الافتراضية للإيداع** – قم بتحديد المبلغ الذي يجب على العميل دفعه كإيداع قبل تأكيد الأمر.</span><span class="sxs-lookup"><span data-stu-id="a8121-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="a8121-118">يتم حساب مبلغ الإيداع الافتراضي كنسبة مئوية لقيمة الأمر.</span><span class="sxs-lookup"><span data-stu-id="a8121-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="a8121-119">بناءً على الامتيازات، قد يصبح موظف المتجر قادرًا على تجاوز المبلغ باستخدم **تجاوز الإيداع**.</span><span class="sxs-lookup"><span data-stu-id="a8121-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="a8121-120">**النسبة المئوية لرسوم الإلغاء** – إذا كان سيتم تطبيق رسوم عند إلغاء أمر العميل، حدد مبلغ هذه الرسوم.</span><span class="sxs-lookup"><span data-stu-id="a8121-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="a8121-121">**رمز رسوم الإلغاء** – إذا كان سيتم تطبيق رسوم عند إلغاء أمر العميل، فسوف تنعكس هذه الرسوم تحت رمز الرسوم في أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="a8121-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="a8121-122">استخدم هذه المعلمة لتخديد رمز رسوم الإلغاء.</span><span class="sxs-lookup"><span data-stu-id="a8121-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="a8121-123">**رمز رسوم الشحن** – يمكن لتجار التجزئة تحصيل رسوم إضافية لشحن البضائع إلى أحد العملاء.</span><span class="sxs-lookup"><span data-stu-id="a8121-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="a8121-124">وسوف ينعكس مبلغ رسوم الشحن هذه ضمن رمز الرسوم في أمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="a8121-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="a8121-125">استخدم هذه المعلمة لتعيين رمز رسوم الشحن إلى رسوم الشحن على أمر العميل.</span><span class="sxs-lookup"><span data-stu-id="a8121-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="a8121-126">**المبلغ المسترد من تكاليف الشحن** -حدد إذا ماكنت رسوم الشحن المرتبطة بأمر العميل قابلة للاسترداد أم لا.</span><span class="sxs-lookup"><span data-stu-id="a8121-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="a8121-127">**الحد الأقصى للمبلغ بدون الموافقة** – إذا كانت مصاريف الشحن قابلة للاسترداد، حدد الحد الأقصى لمبلغ رسوم الشحن الذي سيتم استرداده عبر أوامر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="a8121-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="a8121-128">إذا تم تجاوز هذا المبلغ، فمن ثم يلزم تجاوز المدير من أجل الاستمرار في إرجاع المبلغ المسترد.</span><span class="sxs-lookup"><span data-stu-id="a8121-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="a8121-129">لاستيعاب السيناريوهات التالية، يمكن أن يتجاوز رد رسوم الشحن المبلغ المدفوع أصلًا:</span><span class="sxs-lookup"><span data-stu-id="a8121-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="a8121-130">يتم تطبيق الرسوم على مستوى عنوان أمر المبيعات، وعندما يتم إرجاع بعض كميات من سطر المنتج، لا يمكن تحديد الحد الأقصى لاسترداد رسوم الشحن المسموح بها للمنتجات والكمية، بنفس طريقة تحديدها لكافة العملاء.</span><span class="sxs-lookup"><span data-stu-id="a8121-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all customers.</span></span>
    - <span data-ttu-id="a8121-131">يتم تحمل مصاريف الشحن لكل مثيل للشحن.</span><span class="sxs-lookup"><span data-stu-id="a8121-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="a8121-132">إذا قام عميل بإرجاع منتجات لعدة مرات، وكانت سياسة تاجر التجزئة تنص على أنه يتعين على تاجر التجزئة تحمل تكلفة مصاريف إعادة الشحن، فستكون مصاريف إعادة الشحن أكثر من مصاريف الشحن الفعلية.</span><span class="sxs-lookup"><span data-stu-id="a8121-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="a8121-133">تدفق الحركة لأوامر العملاء</span><span class="sxs-lookup"><span data-stu-id="a8121-133">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-modern-pos"></a><span data-ttu-id="a8121-134">إنشاء أمر عميل في نقطة بيع حديثة</span><span class="sxs-lookup"><span data-stu-id="a8121-134">Create a customer order in Modern POS</span></span>

1. <span data-ttu-id="a8121-135">أضف عميلاً للحركة.</span><span class="sxs-lookup"><span data-stu-id="a8121-135">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="a8121-136">أضف منتجات إلى عربة التسوق.</span><span class="sxs-lookup"><span data-stu-id="a8121-136">Add products to the cart.</span></span>
3. <span data-ttu-id="a8121-137">انقر فوق **إنشاء أمر العميل**، ثم حدد نوع الأمر.</span><span class="sxs-lookup"><span data-stu-id="a8121-137">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="a8121-138">يمكن أن يكون نوع الأمر إما **أمر العميل** أو **عرض الأسعار**.</span><span class="sxs-lookup"><span data-stu-id="a8121-138">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="a8121-139">انقر فوق **تم تحديد الشحن** أو **شحن الكل** لشحن المنتجات إلى عنوان موجود في حساب العميل، حدد تاريخ الشحن المطلوب، وحدد مصاريف الشحن.</span><span class="sxs-lookup"><span data-stu-id="a8121-139">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="a8121-140">انقر فوق **انتقاء المُحدّد** أو **انتقاء الكل** لتحديد المنتجات التي سيتم انتقاؤها من المخزن الحالي أو من متجر آخر في تاريخ محدد.</span><span class="sxs-lookup"><span data-stu-id="a8121-140">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="a8121-141">قم بتحصيل مبلغ الإيداع، إذا كان الإيداع مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="a8121-141">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="a8121-142">تحرير أمر عميل موجود</span><span class="sxs-lookup"><span data-stu-id="a8121-142">Edit an existing customer order</span></span>

1. <span data-ttu-id="a8121-143">في الصفحة الرئيسية، انقر فوق **البحث عن أمر**.</span><span class="sxs-lookup"><span data-stu-id="a8121-143">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="a8121-144">البحث عن وتحدد الأمر المُراد تحريره.</span><span class="sxs-lookup"><span data-stu-id="a8121-144">Find and select the order to edit.</span></span> <span data-ttu-id="a8121-145">انقر فوق **تحرير**، الموجودة في أسفل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a8121-145">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="a8121-146">انتقاء أمر</span><span class="sxs-lookup"><span data-stu-id="a8121-146">Pick up an order</span></span>

1. <span data-ttu-id="a8121-147">في الصفحة الرئيسية، انقر فوق **البحث عن أمر**.</span><span class="sxs-lookup"><span data-stu-id="a8121-147">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="a8121-148">حدد الأمر المراد انتقائه.</span><span class="sxs-lookup"><span data-stu-id="a8121-148">Select the order to pick up.</span></span> <span data-ttu-id="a8121-149">انقر فوق زر **الانتقاء والتعبئة**، الموجود في أسفل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a8121-149">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="a8121-150">انقر فوق **انتقاء**.</span><span class="sxs-lookup"><span data-stu-id="a8121-150">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="a8121-151">إلغاء أمر</span><span class="sxs-lookup"><span data-stu-id="a8121-151">Cancel an order</span></span>

1. <span data-ttu-id="a8121-152">في الصفحة الرئيسية، انقر فوق **البحث عن أمر**.</span><span class="sxs-lookup"><span data-stu-id="a8121-152">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="a8121-153">حدد الأمر المُراد إلغاؤه.</span><span class="sxs-lookup"><span data-stu-id="a8121-153">Select the order to cancel.</span></span> <span data-ttu-id="a8121-154">انقر فوق **إلغاء**، الموجودة في أسفل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a8121-154">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="a8121-155">إنشاء أمر إرجاع</span><span class="sxs-lookup"><span data-stu-id="a8121-155">Create a return order</span></span>

1. <span data-ttu-id="a8121-156">في الصفحة الرئيسية، انقر فوق **البحث عن أمر**.</span><span class="sxs-lookup"><span data-stu-id="a8121-156">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="a8121-157">حدد الأمر المُراد إرجاعه، حدد فاتورة الامر، ثم حدد سطر المنتج للبضاعة المُراد إرجاعها.</span><span class="sxs-lookup"><span data-stu-id="a8121-157">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="a8121-158">انقر فوق **أمر إرجاع**، الموجودة في أسفل الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a8121-158">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="a8121-159">تدفق الحركة غير المتزامن لأوامر العملاء</span><span class="sxs-lookup"><span data-stu-id="a8121-159">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="a8121-160">يمكن إنشاء أوامر العملاء من عميل نقطة البيع سواءً في وضع متزامن أو غير متزامن.</span><span class="sxs-lookup"><span data-stu-id="a8121-160">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="a8121-161">تمكين إنشاء أوامر العملاء في وضع غير متزامن</span><span class="sxs-lookup"><span data-stu-id="a8121-161">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="a8121-162">انقر **البيع بالتجزئة والتجارة** &gt; **إعداد القناة** &gt; **إعداد نقطة البيع** &gt; **ملف تعريف نقطة البيع** &gt; **ملفات تعريف الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="a8121-162">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="a8121-163">في علامة التبويب السريعة **عام**، قم بتعيين خيار **إنشاء أمر عميل في الوضع "غير متزامن"** على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="a8121-163">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="a8121-164">عند تعيين الخيار **إنشاء أمر عميل في الوضع "غير متزامن"‬** إلى **نعم**، يتم إنشاء أوامر العملاء دائمًا في وضع "غير متزامن"، حتى في حال توفرت Retail Transaction Service (RTS).</span><span class="sxs-lookup"><span data-stu-id="a8121-164">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="a8121-165">إذا قمت بتعيين هذا الخيار إلى **لا**، يتم إنشاء أوامر العميل دائماً في وضع متزامن باستخدام خدمة حركة البيع بالتجزئة RTS.</span><span class="sxs-lookup"><span data-stu-id="a8121-165">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="a8121-166">عند إنشاء أوامر العملاء في الوضع "غير متزامن"، يتم سحبها وإدراجها في Commerce بسحب وظائف (P).</span><span class="sxs-lookup"><span data-stu-id="a8121-166">When customer orders are created in asynchronous mode, they are pulled and inserted into Commerce by Pull (P) jobs.</span></span> <span data-ttu-id="a8121-167">يتم إنشاء أوامر التوريد الطابقة عندما يتم تشغيل **مزامنة الأوامر** يدويًا أو من خلال معالجة دفعة.</span><span class="sxs-lookup"><span data-stu-id="a8121-167">The corresponding sales orders are created when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a8121-168">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a8121-168">Additional resources</span></span>

[<span data-ttu-id="a8121-169">أوامر العملاء المختلطة</span><span class="sxs-lookup"><span data-stu-id="a8121-169">Hybrid customer orders</span></span>](hybrid-customer-orders.md)