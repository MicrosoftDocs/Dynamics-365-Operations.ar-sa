---
title: سعر تكلفة الإرجاع وكود شحنة الإرجاع
description: قد تحتاج إلى أن تكون التكلفة للمنتجات المرتجعة تساوي التكلفة للمنتجات في وقت بيع المنتجات للعميل. يمكنك القيام بذلك باستخدام **كود شحنة الإرجاع** .
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnInventTransIdLookup, ReturnItemNumLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d5ac48dd390e2f57a7312e3c54af53dd49fd4f7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975574"
---
# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="95ab5-104">سعر تكلفة الإرجاع وكود شحنة الإرجاع</span><span class="sxs-lookup"><span data-stu-id="95ab5-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="95ab5-105">يتم حساب التكلفة للمنتجات التي يتم إرجاعها إلى المخزون باستخدام التكلفة الحالية للمنتجات.</span><span class="sxs-lookup"><span data-stu-id="95ab5-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="95ab5-106">مع ذلك، قد تحتاج إلى أن تكون التكلفة للمنتجات المرتجعة تساوي التكلفة للمنتجات في وقت بيع المنتجات للعميل.</span><span class="sxs-lookup"><span data-stu-id="95ab5-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="95ab5-107">يمكنك القيام بذلك باستخدام حقل **كود شحنة الإرجاع** في علامة التبويب السريعة **تفاصيل بند** في النموذج **أمر المبيعات** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="95ab5-108">فكر في السيناريو التالي على سبيل المثال.</span><span class="sxs-lookup"><span data-stu-id="95ab5-108">For example, consider the following scenario.</span></span> <span data-ttu-id="95ab5-109">أن تقوم بعمل فاتورة لعميل.</span><span class="sxs-lookup"><span data-stu-id="95ab5-109">You invoice a customer.</span></span> <span data-ttu-id="95ab5-110">وبعد ذلك، قام العميل بإرجاع المنتجات التي تم تسليمها لك.</span><span class="sxs-lookup"><span data-stu-id="95ab5-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="95ab5-111">وأنت أرجعت المنتجات إلى المخزون.</span><span class="sxs-lookup"><span data-stu-id="95ab5-111">You return the products to stock.</span></span> <span data-ttu-id="95ab5-112">في هذه الحالة، عندما تقوم برد ثمن المنتجات المرتجعة إلى العميل، يتم حساب التكلفة لتلك المنتجات باستخدام التكلفة الحالية للمنتجات.</span><span class="sxs-lookup"><span data-stu-id="95ab5-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="95ab5-113">ومع ذلك، إذا قمت باستخدام حقل **كود شحنة الإرجاع** ، يتم حساب التكلفة للمنتجات المرتجعة باستخدام التكلفة في فاتورة البيع الأصلي إلى العميل.</span><span class="sxs-lookup"><span data-stu-id="95ab5-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="95ab5-114">لاستخدام تكلفة أخرى غير التكلفة الحالية للمرتجعات من عميل، استخدم إحدى الطرق التالية.</span><span class="sxs-lookup"><span data-stu-id="95ab5-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="95ab5-115">الطريقة الأولى: إدخال سعر تكلفة الإرجاع يدوياً</span><span class="sxs-lookup"><span data-stu-id="95ab5-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="95ab5-116">بشكل افتراضي، عندما تقوم بإضافة أصناف إلى أمر إرجاع، يتم إرجاع الأصناف إلى المخزون بسعر التكلفة الحالي.</span><span class="sxs-lookup"><span data-stu-id="95ab5-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="95ab5-117">لتحديد سعر تكلفة إرجاع مختلف، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="95ab5-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="95ab5-118">انقر فوق **المبيعات والتسويق** \> **عام** \> **أوامر الإرجاع** \> **كل أوامر الإرجاع** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders** .</span></span>

2.  <span data-ttu-id="95ab5-119">في **جزء الإجراءات** ، في المجموعة **جديد** ، انقر فوق **أمر إرجاع** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-119">On the **Action Pane** , in the **New** group, click **Return order** .</span></span>

3.  <span data-ttu-id="95ab5-120">في نموذج **إنشاء أمر إرجاع** ، حدد حساب عميل ومن ثم انقر فوق **موافق** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-120">In the **Create return order** form, select a customer account, and then click **OK** .</span></span>

4.  <span data-ttu-id="95ab5-121">في النموذج **أمر الإرجاع - رقم ترخيص المواد المسترجعة: %1, %2** ، حدد أحد الأصناف ومن ثم أدخل كمية سالبة في حقل **الكمية‏‎** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="95ab5-122">انقر فوق علامة التبويب السريعة **تفاصيل البند** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="95ab5-123">من علامة التبويب **عام** ، حدد قيمة في الحقل **سعر تكلفة الإرجاع** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="95ab5-124">يتم استخدام هذه القيمة عند إرجاع البضائع إلى المخزون.</span><span class="sxs-lookup"><span data-stu-id="95ab5-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="95ab5-125">إذا لم تقم بإدخال قيمة، يتم استخدام سعر التكلفة الحالي عند إرجاع البضائع إلى المخزون.</span><span class="sxs-lookup"><span data-stu-id="95ab5-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="95ab5-126">الطريقة الثانية: إنشاء سعر التكلفة تلقائيًا وفقا لبند فاتورة العميل</span><span class="sxs-lookup"><span data-stu-id="95ab5-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="95ab5-127">هذه هي الطريقة المفضل استخدامها لإنشاء بنود الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="95ab5-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="95ab5-128">لاستخدام تكلفة المنتجات في قت بيع المنتجات للعميل، قم بإنشاء أمر إرجاع وحدد بند مبيعات للإرجاع.</span><span class="sxs-lookup"><span data-stu-id="95ab5-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="95ab5-129">انقر فوق **المبيعات والتسويق** \> **عام** \> **أوامر الإرجاع** \> **كل أوامر الإرجاع** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders** .</span></span>

2.  <span data-ttu-id="95ab5-130">في **جزء الإجراءات** ، في المجموعة **جديد** ، انقر فوق **أمر إرجاع** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-130">On the **Action Pane** , in the **New** group, click **Return order** .</span></span>

3.  <span data-ttu-id="95ab5-131">في نموذج **إنشاء أمر إرجاع** ، حدد حساب عميل ومن ثم انقر فوق **موافق** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-131">In the **Create return order** form, select a customer account, and then click **OK** .</span></span>

4.  <span data-ttu-id="95ab5-132">في النموذج **أمر الإرجاع - رقم ترخيص المواد المسترجعة: %1, %2** ، في **جزء الإجراءات** ، انقر فوق **العثور على أمر المبيعات‬** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane** , click **Find sales order** .</span></span>

5.  <span data-ttu-id="95ab5-133">في النموذج **العثور على أمر المبيعات‬** ، حدد بند الفاتورة للإرجاع، ثم انقر فوق **موافق** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-133">In the **Find sales order** form, select the invoice line to return, and then click **OK** .</span></span>
    
    <span data-ttu-id="95ab5-134">في علامة التبويب السريعة **تفاصيل البند** ، في علامة التبويب **عام** ، يتم عرض حقل **كود شحنة الإرجاع** من بند المبيعات الأصلي.</span><span class="sxs-lookup"><span data-stu-id="95ab5-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="95ab5-135">بالإضافة إلى ذلك، يعرض **سعر تكلفة الإرجاع** قيمة التكلفة من بند المبيعات الأصلي.</span><span class="sxs-lookup"><span data-stu-id="95ab5-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="95ab5-136">مثال حساب التكلفة</span><span class="sxs-lookup"><span data-stu-id="95ab5-136">Cost calculation example</span></span>

<span data-ttu-id="95ab5-137">عندما تستخدم حقل **كود شحنة الإرجاع** في بند أمر إرجاع لتحديد سعر تكلفة الإرجاع، يتم استخدام التكلفة في بند أمر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="95ab5-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="95ab5-138">إذا قمت بتشغيل وظيفة إقفال أو إعادة حساب المخزون، يتم تعديل التكلفة في بند المبيعات الأصلي.</span><span class="sxs-lookup"><span data-stu-id="95ab5-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="95ab5-139">يتم تعطيل التكلفة في بند أمر الإرجاع تلقائياً لتعكس نفس التكلفة لكل قطعة.</span><span class="sxs-lookup"><span data-stu-id="95ab5-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="95ab5-140">قم بإنشاء وإصدار منتج الذي يسمى Test.</span><span class="sxs-lookup"><span data-stu-id="95ab5-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="95ab5-141">في نموذج **‏‫تفاصيل المنتج الذي تم إصداره‬** ، حدد المعلومات التالية:</span><span class="sxs-lookup"><span data-stu-id="95ab5-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="95ab5-142">في علامة التبويب السريعة **إدارة التكاليف** ، في حقل **مجموعة الأصناف** ، حدد مجموعة **أجزاء** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="95ab5-143">في علامة التبويب السريعة **عام** ، في الحقل **مجموعة نماذج الصنف‬** ، حدد **DEF** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-143">On the **General** FastTab, in the **Item model group** field, select **DEF** .</span></span>
    
    3.  <span data-ttu-id="95ab5-144">في علامة التبويب السريعة **شراء** ، في حقل **السعر** اكتب 10.00 كسعر تكلفة للبند.</span><span class="sxs-lookup"><span data-stu-id="95ab5-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="95ab5-145">في **جزء الإجراءات** ، انقر فوق **مجموعات الأبعاد** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-145">On the **Action Pane** , click **Dimension groups** .</span></span> <span data-ttu-id="95ab5-146">في حقل **مجموعة أبعاد التخزين** ، حدد **الموقع والمستودع فقط** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-146">In the **Storage dimension group** field, select **Site and Warehouse only** .</span></span> <span data-ttu-id="95ab5-147">في حقل **مجموعة أبعاد التعقب** ، حدد **بدون أبعاد التعقب النشطة** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-147">In the **Tracking dimension group** field, select **No active tracking dimensions** .</span></span>

2.  <span data-ttu-id="95ab5-148">قم بإنشاء أمر شراء لـ 10 قطع من الصنف Test بسعر 6.00 لكل قطعة، وقم بترحيل فاتورة لأمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="95ab5-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="95ab5-149">قم بإنشاء أمر شراء ثان لـ 10 قطع من الصنف Test بسعر 8.00 لكل قطعة، وقم بترحيل فاتورة لأمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="95ab5-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="95ab5-150">قم بترحيل فاتورة لأمر المبيعات لبيع خمسة أجزاء من العنصر Test.</span><span class="sxs-lookup"><span data-stu-id="95ab5-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="95ab5-151">في هذه الحالة، يتم تحديد تكلفة بند أمر المبيعات بسعر 35.00 (خمس قطع \* 7.00 متوسط التكلفة لكل قطعة).</span><span class="sxs-lookup"><span data-stu-id="95ab5-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="95ab5-152">قم بإنشاء أمر إرجاع للعميل.</span><span class="sxs-lookup"><span data-stu-id="95ab5-152">Create a return order for the customer.</span></span> <span data-ttu-id="95ab5-153">في النموذج **العثور على أمر المبيعات‬** ، حدد بند الفاتورة، ثم انقر فوق **موافق** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-153">In the **Find sales order** form, select the invoice line, and then click **OK** .</span></span>

5.  <span data-ttu-id="95ab5-154">في النموذج **أمر الإرجاع - رقم ترخيص المواد المسترجعة: %1, %2** ، تحقق من إنشاء أمر إرجاع لإرجاع الصنف Test.</span><span class="sxs-lookup"><span data-stu-id="95ab5-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="95ab5-155">تم تعيين كمية أمر الإرجاع على 5.00.</span><span class="sxs-lookup"><span data-stu-id="95ab5-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="95ab5-156">يعرض حقل **كود شحنة الإرجاع** معرف الشحنة.</span><span class="sxs-lookup"><span data-stu-id="95ab5-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="95ab5-157">يتم استخدام رقم الشحنة هذا من أمر المبيعات الأصلي الخاص بالصنف الذي تم بيعه للعميل.</span><span class="sxs-lookup"><span data-stu-id="95ab5-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="95ab5-158">يعرض **سعر تكلفة الإرجاع** سعر التكلفة من بند المبيعات الأصلي.</span><span class="sxs-lookup"><span data-stu-id="95ab5-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="95ab5-159">سجل استلام الأصناف المرجعة.</span><span class="sxs-lookup"><span data-stu-id="95ab5-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="95ab5-160">قم بترحيل كشف تعبئة للأصناف المرتجعة.</span><span class="sxs-lookup"><span data-stu-id="95ab5-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="95ab5-161">قم بترحيل فاتورة لأمر الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="95ab5-161">Post an invoice for the return order.</span></span> <span data-ttu-id="95ab5-162">في صفحة قائمة **كافة أوامر المبيعات** ، حدد أمر توريد الذي يكون نوع الأمر له **‏‫الأمر المرجع‬** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="95ab5-163">افتح نموذج **حركات المخزون** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="95ab5-164">تحقق من تحديد تكلفة الإرجاع بسعر 7.00 لكل جزء باستخدام القيمة الموجودة في حل **سعر تكلفة الإرجاع** ، بمجموع 35.00 في حقل **مبلغ التكلفة** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="95ab5-165">يمكنك فتح نموذج **حركات المخزون** من النموذج **أمر الإرجاع - رقم ترخيص المواد المسترجعة: %1, %2** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="95ab5-166">في الشبكة **بنود** ، انقر فوق **مخزون** \> **حركات** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-166">In the **Lines** grid, click **Inventory** \> **Transactions** .</span></span>

10. <span data-ttu-id="95ab5-167">في إدارة المخزون والمستودعات، استخدم نموذج **الإقفال والتعديل** لتشغيل الإجراء **3. الإغلاق** .</span><span class="sxs-lookup"><span data-stu-id="95ab5-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="95ab5-168">يعدل هذا الإجراء التكلفة في بند المبيعات الأصلي الذي تم تحديد تكلفة بسعر 35.00 (5 قطع \*7.00) إلى-30.00 (5 قطع \*6.00).</span><span class="sxs-lookup"><span data-stu-id="95ab5-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="95ab5-169">نظرًا لأن مجموعة نموذج المخزون تستخدم قاعدة "ما يدخل أولاً يخرج أولاً" (FIFO)، وسعر 6.00 لكل قطعة هو تكلفة FIFO من أمر الشراء الأول.</span><span class="sxs-lookup"><span data-stu-id="95ab5-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="95ab5-170">بالإضافة إلى ذلك، يعدل الإجراء التكلفة في بند مبيعات الإرجاع لتطابق التكلفة لكل قطعة في بند المبيعات الأصلي.</span><span class="sxs-lookup"><span data-stu-id="95ab5-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="95ab5-171">لذلك، يتم تعديل تكلفة بند الإرجاع من 35.00 إلى 30.00.</span><span class="sxs-lookup"><span data-stu-id="95ab5-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>




